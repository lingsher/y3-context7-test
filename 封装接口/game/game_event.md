---
sidebarDepth: 1
---
# Game (Game)

# 索引

Y3 编辑器 Game 游戏接口，提供游戏相关功能。

---

| 接口 | 描述 |
| --- | --- |
| [event](#event) | 注册引擎事件 |
| [get_event_manager](#get_event_manager) |  |
| [subscribe_event](#subscribe_event) |  |

---

## event

method in Game

- 描述

    注册引擎事件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | event_type | y3.Const.EventType |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Trigger |  |

- 示例

```lua

local result = y3.game:event("游戏-初始化", function(trg, data) end)
```

---

## get_event_manager

method in Game

- 描述

    

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | EventManager |  |

- 示例

```lua


local result = y3.game:get_event_manager()
```

---

## subscribe_event

method in Game

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | event_type | y3.Const.EventType |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | any[]? |  |
    | Trigger.CallBack |  |
    | function |  |

- 示例

```lua

local event_type = y3.const.GlobalEventType['GAME_INIT']

local result = y3.game:subscribe_event(event_type)
```

---
