---
sidebarDepth: 1
---
# PYEventRegister (Game)

# 索引

Y3 编辑器 PYEventRegister 游戏接口，提供游戏相关功能。

---

| 接口 | 描述 |
| --- | --- |
| [event_register](#event_register) |  |
| [event_unregister](#event_unregister) |  |
| [new_global_trigger](#new_global_trigger) |  |

---

## event_register

method in PYEventRegister

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | event_name | y3.Const.EventType | 注册给引擎的事件名 |
    | extra_args? | any[] | 额外参数 |

- 返回值

    无

- 示例

```lua
local event_type = y3.const.GlobalEventType['GAME_INIT']

y3.py_event_sub.event_register(event_type)
```

---

## event_unregister

method in PYEventRegister

- 描述

    

- 参数

    无

- 返回值

    无

- 示例

```lua
y3.py_event_sub.event_unregister()
```

---

## new_global_trigger

method in PYEventRegister

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | event_id | string |  |
    | callback | fun(data: | table) |

- 返回值

    无

- 示例

```lua
local result =  y3.py_event_sub.new_global_trigger("event_id", function() end)
```

---
