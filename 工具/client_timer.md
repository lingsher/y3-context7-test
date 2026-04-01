---
sidebarDepth: 1
---
# ClientTimer (客户端计时器)

# 索引

客户端计时器，由本地电脑的 CPU 驱动，完全是异步的（即使是同步执行）。在游戏暂停时也会继续计时并回调。

> ⚠️ **警告**：如果你不知道什么是异步，请不要使用这个模块！

---

## 静态方法

| 接口 | 描述 |
| --- | --- |
| [wait](#wait) | 等待时间后执行 |
| [wait_frame](#wait_frame) | 等待一定帧数后执行 |
| [loop](#loop) | 循环执行 |
| [loop_frame](#loop_frame) | 每经过一定帧数后执行 |
| [loop_count](#loop_count) | 循环执行，可以指定最大次数 |
| [loop_count_frame](#loop_count_frame) | 每经过一定帧数后执行，可以指定最大次数 |
| [pairs](#pairs) | 遍历所有的计时器 |
| [update_frame](#update_frame) | 立即更新到下一帧 |

## 实例方法

| 接口 | 描述 |
| --- | --- |
| [execute](#execute) | 立即执行 |
| [remove](#remove) | 移除计时器 |
| [pause](#pause) | 暂停计时器 |
| [resume](#resume) | 恢复计时器 |
| [is_running](#is_running) | 是否正在运行 |
| [get_elapsed_time](#get_elapsed_time) | 获取经过的时间 |
| [get_elapsed_frame](#get_elapsed_frame) | 获取经过的帧数 |
| [get_init_count](#get_init_count) | 获取初始计数 |
| [get_remaining_time](#get_remaining_time) | 获取剩余时间 |
| [get_remaining_frame](#get_remaining_frame) | 获取剩余帧数 |
| [get_remaining_count](#get_remaining_count) | 获取剩余计数 |
| [get_time_out_time](#get_time_out_time) | 获取计时器设置的时间 |
| [get_include_name](#get_include_name) | 获取包含名 |

---

# 静态方法

## wait

function in ClientTimer

- 描述

    等待时间后执行

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | timeout | number | 等待时间（秒） |
    | on_timer | fun(timer: ClientTimer, count: integer, local_player: Player) | 回调函数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | ClientTimer | 计时器实例 |

- 示例

```lua
-- 3秒后执行一次（即使游戏暂停也会执行）
y3.ctimer.wait(3, function(timer, count, local_player)
    print("3秒已过！当前玩家:", local_player:get_name())
end)
```

---

## wait_frame

function in ClientTimer

- 描述

    等待一定帧数后执行

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | frame | integer | 等待帧数 |
    | on_timer | fun(timer: ClientTimer, count: integer, local_player: Player) | 回调函数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | ClientTimer | 计时器实例 |

- 示例

```lua
-- 60帧后执行一次
y3.ctimer.wait_frame(60, function(timer, count, local_player)
    print("60帧已过！")
end)
```

---

## loop

function in ClientTimer

- 描述

    循环执行（无限次）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | timeout | number | 间隔时间（秒） |
    | on_timer | fun(timer: ClientTimer, count: integer, local_player: Player) | 回调函数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | ClientTimer | 计时器实例 |

- 示例

```lua
-- 每1秒执行一次（游戏暂停时也会继续）
local timer = y3.ctimer.loop(1, function(timer, count, local_player)
    print("客户端计时器执行第" .. count .. "次")
end)
```

---

## loop_frame

function in ClientTimer

- 描述

    每经过一定帧数后执行（无限次）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | frame | integer | 间隔帧数 |
    | on_timer | fun(timer: ClientTimer, count: integer, local_player: Player) | 回调函数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | ClientTimer | 计时器实例 |

- 示例

```lua
-- 每30帧执行一次
local timer = y3.ctimer.loop_frame(30, function(timer, count, local_player)
    print("每30帧执行，第" .. count .. "次")
end)
```

---

## loop_count

function in ClientTimer

- 描述

    循环执行，可以指定最大次数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | timeout | number | 间隔时间（秒） |
    | count | integer | 最大执行次数 |
    | on_timer | fun(timer: ClientTimer, count: integer, local_player: Player) | 回调函数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | ClientTimer | 计时器实例 |

- 示例

```lua
-- 每1秒执行一次，共执行5次
local timer = y3.ctimer.loop_count(1, 5, function(timer, count, local_player)
    print("第" .. count .. "次执行，共5次")
end)
```

---

## loop_count_frame

function in ClientTimer

- 描述

    每经过一定帧数后执行，可以指定最大次数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | frame | integer | 间隔帧数 |
    | count | integer | 最大执行次数 |
    | on_timer | fun(timer: ClientTimer, count: integer, local_player: Player) | 回调函数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | ClientTimer | 计时器实例 |

- 示例

```lua
-- 每10帧执行一次，共执行10次
local timer = y3.ctimer.loop_count_frame(10, 10, function(timer, count, local_player)
    print("第" .. count .. "次执行")
end)
```

---

## pairs

function in ClientTimer

- 描述

    遍历所有的计时器，仅用于调试（可能会遍历到已经失效的）

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | fun():ClientTimer? | 迭代器函数 |

- 示例

```lua
-- 遍历所有客户端计时器
for timer in y3.ctimer.pairs() do
    print("是否运行:", timer:is_running())
end
```

---

## update_frame

function in ClientTimer

- 描述

    立即更新到下一帧

- 参数

    无

- 返回值

    无

- 示例

```lua
-- 手动触发帧更新
y3.ctimer.update_frame()
```

---

# 实例方法

## execute

method in ClientTimer

- 描述

    立即执行计时器回调

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ... | any | 传递给回调的额外参数 |

- 返回值

    无

- 示例

```lua
local timer = y3.ctimer.loop(5, function(timer, count, local_player)
    print("执行了！")
end)

-- 立即执行一次，传递额外参数
timer:execute("自定义数据")
```

---

## remove

method in ClientTimer

- 描述

    移除计时器

- 参数

    无

- 返回值

    无

- 示例

```lua
local timer = y3.ctimer.loop(1, function(timer, count)
    print("第" .. count .. "次")
    if count >= 3 then
        timer:remove()
        print("计时器已移除")
    end
end)
```

---

## pause

method in ClientTimer

- 描述

    暂停计时器

- 参数

    无

- 返回值

    无

- 示例

```lua
local timer = y3.ctimer.loop(1, function(timer, count)
    print("执行中...")
end)

-- 3秒后暂停
y3.ctimer.wait(3, function()
    timer:pause()
    print("计时器已暂停")
end)
```

---

## resume

method in ClientTimer

- 描述

    恢复计时器

- 参数

    无

- 返回值

    无

- 示例

```lua
local timer = y3.ctimer.loop(1, function(timer, count)
    print("执行中...")
end)

-- 暂停后恢复
y3.ctimer.wait(3, function()
    timer:pause()
    print("计时器已暂停")
    
    y3.ctimer.wait(2, function()
        timer:resume()
        print("计时器已恢复")
    end)
end)
```

---

## is_running

method in ClientTimer

- 描述

    是否正在运行

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否正在运行 |

- 示例

```lua
local timer = y3.ctimer.loop(1, function() end)

print("运行中:", timer:is_running())  -- true

timer:pause()
print("暂停后:", timer:is_running())  -- false
```

---

## get_elapsed_time

method in ClientTimer

- 描述

    获取经过的时间（仅对秒模式的计时器有效）

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 经过的时间（秒） |

- 示例

```lua
local timer = y3.ctimer.loop(5, function(timer, count)
    local elapsed = timer:get_elapsed_time()
    print("距上次执行已过: " .. elapsed .. " 秒")
end)
```

---

## get_elapsed_frame

method in ClientTimer

- 描述

    获取经过的帧数（仅对帧模式的计时器有效）

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 经过的帧数 |

- 示例

```lua
local timer = y3.ctimer.loop_frame(60, function(timer, count)
    local elapsed = timer:get_elapsed_frame()
    print("距上次执行已过: " .. elapsed .. " 帧")
end)
```

---

## get_init_count

method in ClientTimer

- 描述

    获取初始计数

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 初始计数（0表示无限） |

- 示例

```lua
local timer = y3.ctimer.loop_count(1, 10, function() end)

local init_count = timer:get_init_count()
print("初始计数: " .. init_count)  -- 10
```

---

## get_remaining_time

method in ClientTimer

- 描述

    获取剩余时间

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 剩余时间（秒） |

- 示例

```lua
local timer = y3.ctimer.wait(10, function()
    print("10秒到了！")
end)

-- 检查剩余时间
y3.ctimer.loop(1, function()
    local remaining = timer:get_remaining_time()
    print("剩余: " .. string.format("%.1f", remaining) .. " 秒")
end)
```

---

## get_remaining_frame

method in ClientTimer

- 描述

    获取剩余帧数

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 剩余帧数 |

- 示例

```lua
local timer = y3.ctimer.wait_frame(100, function()
    print("100帧到了！")
end)

-- 检查剩余帧数
y3.ctimer.loop_frame(10, function()
    local remaining = timer:get_remaining_frame()
    print("剩余: " .. remaining .. " 帧")
end)
```

---

## get_remaining_count

method in ClientTimer

- 描述

    获取剩余计数

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 剩余计数（-1表示无限） |

- 示例

```lua
local timer = y3.ctimer.loop_count(1, 5, function(timer, count)
    local remaining = timer:get_remaining_count()
    print("第" .. count .. "次，剩余: " .. remaining .. " 次")
end)
```

---

## get_time_out_time

method in ClientTimer

- 描述

    获取计时器设置的时间

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 计时器设置的时间（秒或帧） |

- 示例

```lua
local timer = y3.ctimer.loop(2.5, function() end)

local time = timer:get_time_out_time()
print("设置的时间: " .. time)  -- 2.5
```

---

## get_include_name

method in ClientTimer

- 描述

    获取包含名（用于热重载）

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string? | 包含名 |

- 示例

```lua
local timer = y3.ctimer.loop(1, function() end)

local include_name = timer:get_include_name()
print("包含名:", include_name)
```
