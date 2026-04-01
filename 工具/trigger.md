---
sidebarDepth: 1
---
# Trigger (触发器)

# 索引

触发器类，用于管理事件回调的生命周期。支持启用/禁用、标签管理、唯一性约束等功能。

---

## 构造

| 接口 | 描述 |
| --- | --- |
| [Trigger](#trigger-构造) | 创建触发器 |

## 方法

| 接口 | 描述 |
| --- | --- |
| [get_id](#get_id) | 获取触发器 ID |
| [disable](#disable) | 禁用触发器 |
| [enable](#enable) | 启用触发器 |
| [is_enable](#is_enable) | 检查是否启用 |
| [disable_once](#disable_once) | 本次事件中禁用 |
| [execute](#execute) | 执行触发器 |
| [remove](#remove) | 移除触发器 |
| [add_tag](#add_tag) | 添加标签 |
| [has_tag](#has_tag) | 检查标签 |
| [remove_tag](#remove_tag) | 移除标签 |
| [unique](#unique) | 设置唯一性 |

---

## Trigger 构造

`New 'Trigger' (event: Event, event_args?: any[], callback: Trigger.CallBack) -> Trigger`

- 描述

    创建一个触发器并关联到事件。通常通过 `EventManager:event` 创建。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | event | Event | 关联的事件 |
    | event_args? | any[] | 事件参数匹配条件 |
    | callback | Trigger.CallBack | 回调函数 |

- 示例

```lua
-- 通常通过 EventManager 创建触发器
local event_manager = New 'EventManager' ({})
local trigger = event_manager:event('my_event', nil, function(trg)
    print('触发器执行')
end)
```

---

## get_id

method in Trigger

`trigger:get_id() -> integer`

- 描述

    获取触发器的唯一 ID

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 触发器 ID |

- 示例

```lua
local event_manager = New 'EventManager' ({})
local trigger = event_manager:event('test', nil, function() end)
print('触发器 ID:', trigger:get_id())
```

---

## disable

method in Trigger

`trigger:disable()`

- 描述

    禁用触发器。禁用后触发器不会响应事件。

- 示例

```lua
local event_manager = New 'EventManager' ({})
local trigger = event_manager:event('test', nil, function()
    print('这不会被打印')
end)

-- 禁用触发器
trigger:disable()

-- 事件触发时，被禁用的触发器不会执行
event_manager:notify('test', nil)
```

---

## enable

method in Trigger

`trigger:enable()`

- 描述

    启用触发器

- 示例

```lua
local event_manager = New 'EventManager' ({})
local trigger = event_manager:event('test', nil, function()
    print('触发器重新启用')
end)

trigger:disable()
trigger:enable()  -- 重新启用

event_manager:notify('test', nil)  -- 会执行
```

---

## is_enable

method in Trigger

`trigger:is_enable() -> boolean`

- 描述

    检查触发器是否启用

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否启用 |

- 示例

```lua
local event_manager = New 'EventManager' ({})
local trigger = event_manager:event('test', nil, function() end)

print('启用状态:', trigger:is_enable())  -- true
trigger:disable()
print('启用状态:', trigger:is_enable())  -- false
```

---

## disable_once

method in Trigger

`trigger:disable_once()`

- 描述

    在本次事件中禁用此触发器。下次事件时自动恢复。

- 示例

```lua
local event_manager = New 'EventManager' ({})
local count = 0

local trigger = event_manager:event('test', nil, function(trg)
    count = count + 1
    print('执行次数:', count)
    
    if count >= 3 then
        -- 本次事件后禁用
        trg:disable_once()
    end
end)
```

---

## execute

method in Trigger

`trigger:execute(...) -> any, any, any, any`

- 描述

    手动执行触发器。最多返回 4 个返回值。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ... | any | 传递给回调的参数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | any, any, any, any | 回调的返回值（最多4个） |

- 示例

```lua
local event_manager = New 'EventManager' ({})
local trigger = event_manager:event('calc', nil, function(trg, a, b)
    return a + b
end)

-- 手动执行触发器
local result = trigger:execute(10, 20)
print('计算结果:', result)  -- 30
```

---

## remove

method in Trigger

`trigger:remove()`

- 描述

    移除触发器

- 示例

```lua
local event_manager = New 'EventManager' ({})
local trigger = event_manager:event('test', nil, function()
    print('这个触发器将被移除')
end)

-- 移除触发器
trigger:remove()
```

---

## add_tag

method in Trigger

`trigger:add_tag(tag: any)`

- 描述

    为触发器添加标签

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | any | 标签值 |

- 示例

```lua
local event_manager = New 'EventManager' ({})
local trigger = event_manager:event('test', nil, function() end)

-- 添加标签
trigger:add_tag('combat')
trigger:add_tag('player1')
```

---

## has_tag

method in Trigger

`trigger:has_tag(tag: any) -> boolean`

- 描述

    检查触发器是否有指定标签

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否有该标签 |

- 示例

```lua
local event_manager = New 'EventManager' ({})
local trigger = event_manager:event('test', nil, function() end)

trigger:add_tag('combat')

print(trigger:has_tag('combat'))  -- true
print(trigger:has_tag('ui'))      -- false
```

---

## remove_tag

method in Trigger

`trigger:remove_tag(tag: any)`

- 描述

    移除触发器的标签

- 示例

```lua
local event_manager = New 'EventManager' ({})
local trigger = event_manager:event('test', nil, function() end)

trigger:add_tag('temp')
print(trigger:has_tag('temp'))  -- true

trigger:remove_tag('temp')
print(trigger:has_tag('temp'))  -- false
```

---

## unique

method in Trigger

`trigger:unique(name: string) -> Trigger`

- 描述

    设置触发器的唯一性名称。如果已存在同名触发器，会先移除旧的。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | name | string | 唯一性名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Trigger | 返回自身 |

- 示例

```lua
local event_manager = New 'EventManager' ({})

-- 第一个触发器
local trigger1 = event_manager:event('test', nil, function()
    print('触发器 1')
end):unique('only_one')

-- 第二个同名触发器会替换第一个
local trigger2 = event_manager:event('test', nil, function()
    print('触发器 2')
end):unique('only_one')

-- 只有触发器 2 会执行
event_manager:notify('test', nil)
```
