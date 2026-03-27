---
sidebarDepth: 1
---
# Timer (运行时对象)

# 索引

Y3 编辑器 Timer 封装接口，提供高级方法操作 Timer 对象。

---

| 接口 | 描述 |
| --- | --- |
| [get_by_handle](#get_by_handle) |  |
| [wait](#wait) | 等待时间后执行 |
| [wait_frame](#wait_frame) | 等待一定帧数后执行 |
| [loop](#loop) | 循环执行 |
| [loop_frame](#loop_frame) | 每经过一定帧数后执行 |
| [count_loop](#count_loop) | 循环执行，可以指定最大次数 |
| [count_loop_frame](#count_loop_frame) | 每经过一定帧数后执行，可以指定最大次数 |
| [execute](#execute) | 立即执行 |
| [remove](#remove) | 移除计时器 |
| [is_removed](#is_removed) |  |
| [pause](#pause) | 暂停计时器 |
| [resume](#resume) | 继续计时器 |
| [is_running](#is_running) | 是否在运行 |
| [get_elapsed_time](#get_elapsed_time) | 获取计时器经过的时间 |
| [get_init_count](#get_init_count) | 获取计时器初始计数 |
| [get_remaining_time](#get_remaining_time) | 获取计时器剩余时间 |
| [get_remaining_count](#get_remaining_count) | 获取计时器剩余计数 |
| [get_time_out_time](#get_time_out_time) | 获取计时器设置的时间 |
| [get_include_name](#get_include_name) |  |
| [pairs](#pairs) | 遍历所有的计时器，仅用于调试（可能会遍历到已经失效的） |

---

## get_by_handle

method in Timer

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | py_timer | py.Timer |  |
    | on_timer | Timer.OnTimer |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Timer |  |

- 示例

```lua
local on_timer = function() end

local result = y3.timer.get_by_handle(timer, on_timer)
```

---

## wait

method in Timer

- 描述

    等待时间后执行

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | timeout | number |  |
    | on_timer | fun(timer: | Timer) |
    | desc? | string | 描述 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Timer |  |

- 示例

```lua
local result = y3.timer.wait(1.0, function() end, "desc")
```

---

## wait_frame

method in Timer

- 描述

    等待一定帧数后执行

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | frame | integer |  |
    | on_timer | fun(timer: | Timer) |
    | desc? | string | 描述 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Timer |  |

- 示例

```lua
local result = y3.timer.wait_frame(1, function() end, "desc")
```

---

## loop

method in Timer

- 描述

    循环执行

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | timeout | number |  |
    | on_timer | fun(timer: | Timer, count: integer) |
    | desc? | string | 描述 |
    | immediate? | boolean | 是否立即执行一次 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Timer |  |

- 示例

```lua
local result = y3.timer.loop(1.0, function() end, "desc", true)
```

---

## loop_frame

method in Timer

- 描述

    每经过一定帧数后执行

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | frame | integer |  |
    | on_timer | fun(timer: | Timer, count: integer) |
    | desc? | string | 描述 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Timer |  |

- 示例

```lua
local result = y3.timer.loop_frame(1, function() end, "desc")
```

---

## count_loop

method in Timer

- 描述

    循环执行，可以指定最大次数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | timeout | number |  |
    | times | integer |  |
    | on_timer | fun(timer: | Timer, count: integer) |
    | desc? | string | 描述 |
    | immediate? | boolean | 是否立即执行一次(计入最大次数) |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Timer |  |

- 示例

```lua
local result = y3.timer.count_loop(1.0, 1, function() end, "desc", true)
```

---

## count_loop_frame

method in Timer

- 描述

    每经过一定帧数后执行，可以指定最大次数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | frame | integer |  |
    | times | integer |  |
    | on_timer | fun(timer: | Timer, count: integer) |
    | desc? | string | 描述 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Timer |  |

- 示例

```lua
local result = y3.timer.count_loop_frame(1, 1, function() end, "desc")
```

---

## execute

method in Timer

- 描述

    立即执行

- 参数

    无

- 返回值

    无

- 示例

```lua
local timer = y3.timer.loop(1, function() end)

timer:execute()
```

---

## remove

method in Timer

- 描述

    移除计时器

- 参数

    无

- 返回值

    无

- 示例

```lua
local timer = y3.timer.loop(1, function() end)

timer:remove()
```

---

## is_removed

method in Timer

- 描述

    

- 参数

    无

- 返回值

    无

- 示例

```lua
local timer = y3.timer.loop(1, function() end)

timer:is_removed()
```

---

## pause

method in Timer

- 描述

    暂停计时器

- 参数

    无

- 返回值

    无

- 示例

```lua
local timer = y3.timer.loop(1, function() end)

timer:pause()
```

---

## resume

method in Timer

- 描述

    继续计时器

- 参数

    无

- 返回值

    无

- 示例

```lua
local timer = y3.timer.loop(1, function() end)

timer:resume()
```

---

## is_running

method in Timer

- 描述

    是否在运行

- 参数

    无

- 返回值

    无

- 示例

```lua
local timer = y3.timer.loop(1, function() end)

timer:is_running()
```

---

## get_elapsed_time

method in Timer

- 描述

    获取计时器经过的时间

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 计时器经过的时间 |

- 示例

```lua
local timer = y3.timer.loop(1, function() end)

local result = timer:get_elapsed_time()
```

---

## get_init_count

method in Timer

- 描述

    获取计时器初始计数

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 初始计数 |

- 示例

```lua
local timer = y3.timer.loop(1, function() end)

local result = timer:get_init_count()
```

---

## get_remaining_time

method in Timer

- 描述

    获取计时器剩余时间

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 计时器剩余时间 |

- 示例

```lua
local timer = y3.timer.loop(1, function() end)

local result = timer:get_remaining_time()
```

---

## get_remaining_count

method in Timer

- 描述

    获取计时器剩余计数

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 剩余计数 |

- 示例

```lua
local timer = y3.timer.loop(1, function() end)

local result = timer:get_remaining_count()
```

---

## get_time_out_time

method in Timer

- 描述

    获取计时器设置的时间

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 设置的时间 |

- 示例

```lua
local timer = y3.timer.loop(1, function() end)

local result = timer:get_time_out_time()
```

---

## get_include_name

method in Timer

- 描述

    

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string? |  |

- 示例

```lua
local timer = y3.timer.loop(1, function() end)

local result = timer:get_include_name()
```

---

## pairs

method in Timer

- 描述

    遍历所有的计时器，仅用于调试（可能会遍历到已经失效的）

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | fun():Timer? |  |

- 示例

```lua
local result = y3.timer.pairs()
```

---
