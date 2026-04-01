---
sidebarDepth: 1
---
# CustomEvent (自定义事件)

# 索引

自定义事件系统，提供对象级别的事件注册、通知和回执功能。可以混入到任何类中使用。

---

## 方法

| 接口 | 描述 |
| --- | --- |
| [event_on](#event_on) | 注册自定义事件 |
| [event_notify](#event_notify) | 发起自定义事件（通知模式） |
| [event_notify_with_args](#event_notify_with_args) | 发起带事件参数的自定义事件（通知模式） |
| [event_dispatch](#event_dispatch) | 发起自定义事件（回执模式） |
| [event_dispatch_with_args](#event_dispatch_with_args) | 发起带事件参数的自定义事件（回执模式） |
| [get_custom_event_manager](#get_custom_event_manager) | 获取自定义事件管理器 |

---

## event_on

method in CustomEvent

- 描述

    注册自定义事件，当触发时，会执行回调函数。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | event_name | string | 事件名称 |
    | args? | any[] \| any | 事件参数（可选） |
    | callback | Trigger.CallBack | 回调函数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Trigger | 触发器对象 |

- 示例

```lua
-- 基础用法：注册事件
local obj = {}
Extends(obj, 'CustomEvent')

obj:event_on('输入', function(trigger, ...)
    print('触发了输入事件', ...)
end)

obj:event_notify('输入', '123', '456')
-- 输出：触发了输入事件 123 456
```

```lua
-- 带参数的事件注册
local obj = {}
Extends(obj, 'CustomEvent')

obj:event_on('输入', {'123'}, function(trigger, ...)
    print('触发了输入事件', ...)
end)

obj:event_notify('输入', 1)                          -- 不能触发事件
obj:event_notify_with_args('输入', {'123'}, 2)       -- 可以触发事件
obj:event_notify_with_args('输入', {'456'}, 3)       -- 不能触发事件
obj:event_notify_with_args('输入', {'123', '666'}, 4) -- 可以触发事件
```

---

## event_notify

method in CustomEvent

- 描述

    发起自定义事件（通知模式）。同一个对象身上只会有一个正在执行的事件，当发生插入结算时，后面的事件会进入队列。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | event_name | string | 事件名称 |
    | ... | any | 传递给回调的参数 |

- 返回值

    无

- 示例

```lua
-- 通知模式的事件队列机制
local obj = {}
Extends(obj, 'CustomEvent')

obj:event_on('获得', function()
    print('触发获得')
    print('发起移除前')
    obj:event_notify('移除')  -- 进入队列，等当前事件执行完再执行
    print('发起移除后')
end)

obj:event_on('移除', function()
    print('触发移除')
end)

obj:event_notify('获得')

-- 输出顺序：
-- 触发获得
-- 发起移除前
-- 发起移除后
-- 触发移除
```

---

## event_notify_with_args

method in CustomEvent

- 描述

    发起带事件参数的自定义事件（通知模式）。只有注册时指定了匹配参数的事件才会被触发。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | event_name | string | 事件名称 |
    | args | any[] | 事件参数 |
    | ... | any | 传递给回调的参数 |

- 返回值

    无

- 示例

```lua
local obj = {}
Extends(obj, 'CustomEvent')

-- 注册一个只响应特定参数的事件
obj:event_on('技能释放', {'火球术'}, function(trigger, damage)
    print('释放火球术，伤害:', damage)
end)

obj:event_on('技能释放', {'冰霜新星'}, function(trigger, damage)
    print('释放冰霜新星，伤害:', damage)
end)

obj:event_notify_with_args('技能释放', {'火球术'}, 100)    -- 触发火球术
obj:event_notify_with_args('技能释放', {'冰霜新星'}, 150)  -- 触发冰霜新星
obj:event_notify_with_args('技能释放', {'闪电链'}, 80)     -- 不会触发任何事件
```

---

## event_dispatch

method in CustomEvent

- 描述

    发起自定义事件（回执模式）。与通知模式不同，允许插入结算。可以接收到事件的返回值，有多处注册事件时会按照注册顺序调用，当任何事件回调返回了非 `nil` 的值后，后续触发器将不再调用。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | event_name | string | 事件名称 |
    | ... | any | 传递给回调的参数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | any, any, any, any | 事件返回值（最多4个） |

- 示例

```lua
local obj = {}
Extends(obj, 'CustomEvent')

obj:event_on('获取', function(trigger, ...)
    print('获取1')
    return 1
end)

obj:event_on('获取', function(trigger, ...)
    print('获取2')  -- 不会被执行，因为第一个已经返回了值
    return 2
end)

local result = obj:event_dispatch('获取')
print('结果为:', result)

-- 输出：
-- 获取1
-- 结果为: 1
```

---

## event_dispatch_with_args

method in CustomEvent

- 描述

    发起带事件参数的自定义事件（回执模式）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | event_name | string | 事件名称 |
    | args | any[] \| any | 事件参数 |
    | ... | any | 传递给回调的参数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | any, any, any, any | 事件返回值（最多4个） |

- 示例

```lua
local obj = {}
Extends(obj, 'CustomEvent')

obj:event_on('计算伤害', {'物理'}, function(trigger, base_damage)
    return base_damage * 1.5  -- 物理伤害增加50%
end)

obj:event_on('计算伤害', {'魔法'}, function(trigger, base_damage)
    return base_damage * 1.2  -- 魔法伤害增加20%
end)

local physical_damage = obj:event_dispatch_with_args('计算伤害', {'物理'}, 100)
local magic_damage = obj:event_dispatch_with_args('计算伤害', {'魔法'}, 100)

print('物理伤害:', physical_damage)  -- 150
print('魔法伤害:', magic_damage)     -- 120
```

---

## get_custom_event_manager

method in CustomEvent

- 描述

    获取自定义事件管理器

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | EventManager? | 事件管理器实例 |

- 示例

```lua
local obj = {}
Extends(obj, 'CustomEvent')

obj:event_on('测试', function() end)

local manager = obj:get_custom_event_manager()
if manager then
    print('事件管理器已创建')
end
```
