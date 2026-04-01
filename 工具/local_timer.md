---
sidebarDepth: 1
---
# LocalTimer (本地计时器)

# 索引

本地计时器，支持异步创建或回调。如果是同步执行的，那么会确保同步回调。

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
| [clock](#clock) | 获取当前逻辑时间（毫秒） |
| [current_frame](#current_frame) | 获取当前逻辑帧号 |

## 实例方法

| 接口 | 描述 |
| --- | --- |
| [execute](#execute) | 立即执行 |
| [remove](#remove) | 移除计时器 |
| [pause](#pause) | 暂停计时器 |
| [resume](#resume) | 恢复计时器 |
| [is_running](#is_running) | 是否正在运行 |
| [get_elapsed_time](#get_elapsed_time) | 获取经过的时间 |
| [get_init_count](#get_init_count) | 获取初始计数 |
| [get_remaining_time](#get_remaining_time) | 获取剩余时间 |
| [set_remaining_time](#set_remaining_time) | 设置剩余时间 |
| [get_remaining_count](#get_remaining_count) | 获取剩余计数 |
| [set_remaining_count](#set_remaining_count) | 设置剩余计数 |
| [get_time_out_time](#get_time_out_time) | 获取计时器周期 |
| [set_time_out_time](#set_time_out_time) | 设置计时器周期 |
| [get_include_name](#get_include_name) | 获取包含名 |

---

# 静态方法

## wait

function in LocalTimer

- 描述

    等待时间后执行

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | timeout | number | 等待时间（秒） |
    | on_timer | fun(timer: LocalTimer, count: integer) | 回调函数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | LocalTimer | 计时器实例 |

- 示例

```lua
-- 3秒后执行一次
y3.ltimer.wait(3, function(timer, count)
    print("3秒已过！")
end)
```

---

## wait_frame

function in LocalTimer

- 描述

    等待一定帧数后执行

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | frame | integer | 等待帧数 |
    | on_timer | fun(timer: LocalTimer, count: integer) | 回调函数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | LocalTimer | 计时器实例 |

- 示例

```lua
-- 60帧后执行一次
y3.ltimer.wait_frame(60, function(timer, count)
    print("60帧已过！")
end)
```

---

## loop

function in LocalTimer

- 描述

    循环执行（无限次）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | timeout | number | 间隔时间（秒） |
    | on_timer | fun(timer: LocalTimer, count: integer) | 回调函数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | LocalTimer | 计时器实例 |

- 示例

```lua
-- 每1秒执行一次
local timer = y3.ltimer.loop(1, function(timer, count)
    print("第" .. count .. "次执行")
end)
```

---

## loop_frame

function in LocalTimer

- 描述

    每经过一定帧数后执行（无限次）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | frame | integer | 间隔帧数 |
    | on_timer | fun(timer: LocalTimer, count: integer) | 回调函数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | LocalTimer | 计时器实例 |

- 示例

```lua
-- 每30帧执行一次
local timer = y3.ltimer.loop_frame(30, function(timer, count)
    print("每30帧执行，第" .. count .. "次")
end)
```

---

## loop_count

function in LocalTimer

- 描述

    循环执行，可以指定最大次数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | timeout | number | 间隔时间（秒） |
    | count | integer | 最大执行次数 |
    | on_timer | fun(timer: LocalTimer, count: integer) | 回调函数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | LocalTimer | 计时器实例 |

- 示例

```lua
-- 每1秒执行一次，共执行5次
local timer = y3.ltimer.loop_count(1, 5, function(timer, count)
    print("第" .. count .. "次执行，共5次")
    if count == 5 then
        print("执行完毕！")
    end
end)
```

---

## loop_count_frame

function in LocalTimer

- 描述

    每经过一定帧数后执行，可以指定最大次数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | frame | integer | 间隔帧数 |
    | count | integer | 最大执行次数 |
    | on_timer | fun(timer: LocalTimer, count: integer) | 回调函数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | LocalTimer | 计时器实例 |

- 示例

```lua
-- 每10帧执行一次，共执行10次
local timer = y3.ltimer.loop_count_frame(10, 10, function(timer, count)
    print("第" .. count .. "次执行")
end)
```

---

## pairs

function in LocalTimer

- 描述

    遍历所有的计时器，仅用于调试（可能会遍历到已经失效的）

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | fun():LocalTimer? | 迭代器函数 |

- 示例

```lua
-- 遍历所有计时器
for timer in y3.ltimer.pairs() do
    print("是否运行:", timer:is_running())
end
```

---

## clock

function in LocalTimer

- 描述

    获取当前逻辑时间（毫秒）

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 当前逻辑时间（毫秒） |

- 示例

```lua
local ms = y3.ltimer.clock()
print("当前逻辑时间: " .. ms .. " 毫秒")
```

---

## current_frame

function in LocalTimer

- 描述

    获取当前逻辑帧号

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 当前逻辑帧号 |

- 示例

```lua
local frame = y3.ltimer.current_frame()
print("当前帧号: " .. frame)
```

---

# 实例方法

## execute

method in LocalTimer

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
local timer = y3.ltimer.loop(5, function(timer, count)
    print("执行了！")
end)

-- 立即执行一次，传递额外参数
timer:execute("自定义数据")
```

---

## remove

method in LocalTimer

- 描述

    移除计时器

- 参数

    无

- 返回值

    无

- 示例

```lua
local timer = y3.ltimer.loop(1, function(timer, count)
    print("第" .. count .. "次")
    if count >= 3 then
        timer:remove()
        print("计时器已移除")
    end
end)
```

---

## pause

method in LocalTimer

- 描述

    暂停计时器

- 参数

    无

- 返回值

    无

- 示例

```lua
local timer = y3.ltimer.loop(1, function(timer, count)
    print("执行中...")
end)

-- 3秒后暂停
y3.ltimer.wait(3, function()
    timer:pause()
    print("计时器已暂停")
end)
```

---

## resume

method in LocalTimer

- 描述

    恢复计时器

- 参数

    无

- 返回值

    无

- 示例

```lua
local timer = y3.ltimer.loop(1, function(timer, count)
    print("执行中...")
end)

-- 3秒后暂停
y3.ltimer.wait(3, function()
    timer:pause()
    print("计时器已暂停")
    
    -- 再过2秒恢复
    y3.ltimer.wait(2, function()
        timer:resume()
        print("计时器已恢复")
    end)
end)
```

---

## is_running

method in LocalTimer

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
local timer = y3.ltimer.loop(1, function() end)

print("运行中:", timer:is_running())  -- true

timer:pause()
print("暂停后:", timer:is_running())  -- false

timer:resume()
print("恢复后:", timer:is_running())  -- true
```

---

## get_elapsed_time

method in LocalTimer

- 描述

    获取经过的时间

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 经过的时间（秒） |

- 示例

```lua
local timer = y3.ltimer.loop(5, function(timer, count)
    local elapsed = timer:get_elapsed_time()
    print("距上次执行已过: " .. elapsed .. " 秒")
end)
```

---

## get_init_count

method in LocalTimer

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
local timer = y3.ltimer.loop_count(1, 10, function() end)

local init_count = timer:get_init_count()
print("初始计数: " .. init_count)  -- 10
```

---

## get_remaining_time

method in LocalTimer

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
local timer = y3.ltimer.wait(10, function()
    print("10秒到了！")
end)

-- 每秒检查剩余时间
y3.ltimer.loop(1, function()
    local remaining = timer:get_remaining_time()
    print("剩余: " .. string.format("%.1f", remaining) .. " 秒")
end)
```

---

## set_remaining_time

method in LocalTimer

- 描述

    设置剩余时间（不能在计时器到期时设置）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | sec | number | 剩余时间（秒） |

- 返回值

    无

- 示例

```lua
local timer = y3.ltimer.wait(10, function()
    print("时间到！")
end)

-- 2秒后将剩余时间设置为1秒
y3.ltimer.wait(2, function()
    timer:set_remaining_time(1)
    print("剩余时间已设置为1秒")
end)
```

---

## get_remaining_count

method in LocalTimer

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
local timer = y3.ltimer.loop_count(1, 5, function(timer, count)
    local remaining = timer:get_remaining_count()
    print("第" .. count .. "次，剩余: " .. remaining .. " 次")
end)
```

---

## set_remaining_count

method in LocalTimer

- 描述

    设置剩余计数（设置为 <= 0 的数值将变为无次数限制）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | count | integer | 剩余计数 |

- 返回值

    无

- 示例

```lua
local timer = y3.ltimer.loop_count(1, 3, function(timer, count)
    print("第" .. count .. "次执行")
end)

-- 将剩余次数改为10次
timer:set_remaining_count(10)
```

---

## get_time_out_time

method in LocalTimer

- 描述

    获取计时器周期

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 计时器周期（秒或帧） |

- 示例

```lua
local timer = y3.ltimer.loop(2.5, function() end)

local period = timer:get_time_out_time()
print("周期: " .. period .. " 秒")  -- 2.5
```

---

## set_time_out_time

method in LocalTimer

- 描述

    设置计时器周期（从下个循环开始生效）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | time | number | 新的周期（秒或帧） |

- 返回值

    无

- 示例

```lua
local timer = y3.ltimer.loop(1, function(timer, count)
    print("第" .. count .. "次，周期: " .. timer:get_time_out_time())
    
    -- 第3次后将周期改为0.5秒
    if count == 3 then
        timer:set_time_out_time(0.5)
        print("周期已改为0.5秒")
    end
end)
```

---

## get_include_name

method in LocalTimer

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
local timer = y3.ltimer.loop(1, function() end)

local include_name = timer:get_include_name()
print("包含名:", include_name)
```
