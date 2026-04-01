---
sidebarDepth: 1
---
# EventManager (事件管理器)

# 索引

事件管理器，用于管理对象级别的事件订阅、通知和分发。支持事件队列防止死循环，自动处理插入结算。

---

## 方法

| 接口 | 描述 |
| --- | --- |
| [event](#event) | 注册事件 |
| [has_event](#has_event) | 检查是否有匹配的事件 |
| [notify](#notify) | 发送事件通知 |
| [dispatch](#dispatch) | 分发事件（可获取返回值） |
| [is_firing](#is_firing) | 检查是否正在触发事件 |
| [pairs](#pairs) | 遍历所有触发器 |

---

## event

method in EventManager

- 描述

    注册事件监听器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | event_name | Event.Name | 事件名称 |
    | event_args? | any[] | 事件参数（用于匹配） |
    | callback | Trigger.CallBack | 回调函数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Trigger | 触发器对象 |

- 示例

```lua
-- 创建事件管理器
local my_object = {}
local event_manager = New 'EventManager' (my_object)

-- 注册事件（第二个参数为事件参数，不需要时传 nil）
event_manager:event('damage', nil, function(trigger, value)
    print('受到伤害:', value)
end)
```

```lua
-- 带参数的事件注册
local event_manager = New 'EventManager' ({})

-- 只响应特定参数的事件
event_manager:event('skill', {'火球术'}, function(trigger, damage)
    print('火球术伤害:', damage)
end)

event_manager:event('skill', {'冰霜新星'}, function(trigger, damage)
    print('冰霜新星伤害:', damage)
end)
```

---

## has_event

method in EventManager

- 描述

    检查是否有匹配的事件监听器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | event_name | Event.Name | 事件名称 |
    | event_args? | any[] | 事件参数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在匹配的监听器 |

- 示例

```lua
local event_manager = New 'EventManager' ({})

event_manager:event('test', nil, function() end)

print(event_manager:has_event('test'))       -- true
print(event_manager:has_event('not_exist'))  -- false
```

---

## notify

method in EventManager

- 描述

    发送事件通知。当事件正在触发时，新事件会进入队列，避免死循环。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | event_name | Event.Name | 事件名称 |
    | event_args? | any[] | 事件参数（用于匹配） |
    | ... | any | 传递给回调的参数 |

- 返回值

    无

- 示例

```lua
local event_manager = New 'EventManager' ({})

event_manager:event('damage', nil, function(trigger, value)
    print('受到伤害:', value)
end)

-- 触发事件
event_manager:notify('damage', nil, 100)
```

```lua
-- 带参数匹配的事件通知
local event_manager = New 'EventManager' ({})

event_manager:event('skill', {'火球术'}, function(trigger, damage)
    print('火球术:', damage)
end)

-- 使用参数匹配
event_manager:notify('skill', {'火球术'}, 150)  -- 触发
event_manager:notify('skill', {'冰霜'}, 100)    -- 不触发
```

---

## dispatch

method in EventManager

- 描述

    分发事件并获取返回值。当任意监听器返回非 nil 值时，后续监听器不再执行。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | event_name | Event.Name | 事件名称 |
    | event_args? | any[] | 事件参数 |
    | ... | any | 传递给回调的参数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | any, any, any, any | 事件返回值（最多4个） |

- 示例

```lua
local event_manager = New 'EventManager' ({})

event_manager:event('calculate', nil, function(trigger, a, b)
    return a + b
end)

local result = event_manager:dispatch('calculate', nil, 10, 20)
print('结果:', result)  -- 30
```

---

## is_firing

method in EventManager

- 描述

    检查事件管理器是否正在触发事件

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否正在触发 |

- 示例

```lua
local event_manager = New 'EventManager' ({})

event_manager:event('test', nil, function(trigger)
    print('正在触发:', event_manager:is_firing())  -- true
end)

print('触发前:', event_manager:is_firing())  -- false
event_manager:notify('test', nil)
print('触发后:', event_manager:is_firing())  -- false
```

---

## pairs

method in EventManager

- 描述

    遍历所有注册的触发器

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | fun():Trigger? | 迭代器函数 |

- 示例

```lua
local event_manager = New 'EventManager' ({})

event_manager:event('event1', nil, function() end)
event_manager:event('event2', nil, function() end)
event_manager:event('event3', nil, function() end)

-- 遍历所有触发器
for trigger in event_manager:pairs() do
    print('触发器:', trigger)
end
```
