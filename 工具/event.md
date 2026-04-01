---
sidebarDepth: 1
---
# Event (事件)

# 索引

事件对象，用于管理触发器的注册、移除和触发。支持三种事件参数模式：无参数、数组参数和自定义参数。是触发器系统的底层核心。

---

## 构造

| 接口 | 描述 |
| --- | --- |
| [Event](#event-构造) | 创建事件对象 |

## 方法

| 接口 | 描述 |
| --- | --- |
| [add_trigger](#add_trigger) | 添加触发器 |
| [remove_trigger](#remove_trigger) | 移除触发器 |
| [has_matched_trigger](#has_matched_trigger) | 检查是否有匹配的触发器 |
| [notify](#notify) | 通知事件（无返回值） |
| [dispatch](#dispatch) | 分发事件（可获取返回值） |
| [is_firing](#is_firing) | 检查是否正在触发 |
| [pairs](#pairs) | 遍历所有触发器 |

---

## Event 构造

`Event(event_name: string) -> Event`

- 描述

    创建一个事件对象

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | event_name | string | 事件名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Event | 事件对象 |

- 示例

```lua
-- 创建一个事件
local my_event = New 'Event' ('my_custom_event')
```

---

## add_trigger

method in Event

- 描述

    添加触发器到事件。如果事件正在触发，触发器会被加入等待队列，触发结束后再实际添加。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | trigger | Trigger | 触发器对象 |

- 返回值

    无

- 示例

```lua
-- 注意：通常不直接调用 add_trigger，而是通过 EventManager 系统
-- 这里展示底层原理

local my_event = New 'Event' ('test_event')

-- 创建触发器（通过 EventManager:event 创建）
local event_manager = New 'EventManager' ({})
local trigger = event_manager:event('test_event', nil, function()
    print('触发器被执行')
end)

my_event:add_trigger(trigger)
```

---

## remove_trigger

method in Event

- 描述

    从事件中移除触发器。如果事件正在触发，移除操作会被延迟到触发结束后执行。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | trigger | Trigger | 触发器对象 |

- 返回值

    无

- 示例

```lua
-- 移除触发器示例
local my_event = New 'Event' ('remove_test')

local event_manager = New 'EventManager' ({})
local trigger = event_manager:event('remove_test', nil, function()
    print('这个触发器会被移除')
end)

my_event:add_trigger(trigger)
my_event:remove_trigger(trigger)
```

---

## has_matched_trigger

method in Event

- 描述

    检查是否有与指定参数匹配的触发器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | args? | any[] | 事件参数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在匹配的触发器 |

- 示例

```lua
local my_event = New 'Event' ('check_event')

-- 添加一个无参数触发器
local event_manager = New 'EventManager' ({})
local trigger = event_manager:event('check_event', nil, function() end)
my_event:add_trigger(trigger)

print(my_event:has_matched_trigger(nil))  -- true
print(my_event:has_matched_trigger({'不存在的参数'}))  -- false
```

---

## notify

method in Event

- 描述

    触发事件并通知所有匹配的触发器。不获取返回值，所有触发器都会执行。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | event_args? | any[] | 事件参数（用于匹配触发器） |
    | ... | any | 传递给回调的参数 |

- 返回值

    无

- 示例

```lua
local my_event = New 'Event' ('notify_test')

local event_manager = New 'EventManager' ({})
local trigger = event_manager:event('notify_test', nil, function(trg, value)
    print('收到通知:', value)
end)
my_event:add_trigger(trigger)

-- 触发事件
my_event:notify(nil, '测试数据')
```

---

## dispatch

method in Event

- 描述

    分发事件并获取返回值。当任意触发器返回非 nil 值时，后续触发器不再执行。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | event_args? | any[] | 事件参数 |
    | ... | any | 传递给回调的参数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | any, any, any, any | 触发器返回值（最多4个） |

- 示例

```lua
local my_event = New 'Event' ('dispatch_test')

local event_manager = New 'EventManager' ({})
local trigger = event_manager:event('dispatch_test', nil, function(trg, a, b)
    return a * b
end)
my_event:add_trigger(trigger)

-- 分发事件并获取返回值
local result = my_event:dispatch(nil, 10, 5)
print('计算结果:', result)  -- 50
```

---

## is_firing

method in Event

- 描述

    检查事件是否正在触发中

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否正在触发 |

- 示例

```lua
local my_event = New 'Event' ('firing_test')

local event_manager = New 'EventManager' ({})
local trigger = event_manager:event('firing_test', nil, function(trg)
    -- 在触发器内部检查
    print('正在触发:', my_event:is_firing())  -- true
end)
my_event:add_trigger(trigger)

print('触发前:', my_event:is_firing())  -- false
my_event:notify(nil)
print('触发后:', my_event:is_firing())  -- false
```

---

## pairs

method in Event

- 描述

    遍历事件中所有注册的触发器，按触发器 ID 排序

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | fun(): Trigger | 迭代器函数 |

- 示例

```lua
local my_event = New 'Event' ('pairs_test')

local event_manager = New 'EventManager' ({})
local trigger1 = event_manager:event('pairs_test', nil, function() end)
local trigger2 = event_manager:event('pairs_test', nil, function() end)
local trigger3 = event_manager:event('pairs_test', nil, function() end)

my_event:add_trigger(trigger1)
my_event:add_trigger(trigger2)
my_event:add_trigger(trigger3)

-- 遍历所有触发器
for trigger in my_event:pairs() do
    print('触发器 ID:', trigger:get_id())
end
```
