---
sidebarDepth: 1
---
# PlayerGroup (运行时对象)

# 索引

Y3 编辑器 PlayerGroup 封装接口，提供高级方法操作 PlayerGroup 对象。

---

| 接口 | 描述 |
| --- | --- |
| [get_by_handle](#get_by_handle) |  |
| [create](#create) | 创建空玩家组 |
| [count](#count) | 获取玩家组中玩家数量 |
| [pick](#pick) | 将玩家组转换为Lua的玩家数组 |
| [pairs](#pairs) | 遍历玩家组，请勿在遍历过程中修改玩家组。 |
| [add_player](#add_player) | 添加玩家 |
| [remove_player](#remove_player) | 移除玩家 |
| [clear](#clear) | 清空玩家组 |
| [get_all_players](#get_all_players) | 获取所有玩家 |
| [get_player_group_by_camp](#get_player_group_by_camp) | 阵营內所有玩家 |
| [get_enemy_player_group_by_player](#get_enemy_player_group_by_player) | 玩家的所有敌对玩家 |
| [get_ally_player_group_by_player](#get_ally_player_group_by_player) | 玩家的所有同盟玩家 |
| [get_victorious_player_group](#get_victorious_player_group) | 获取所有胜利的玩家 |
| [get_defeated_player_group](#get_defeated_player_group) | 获取所有失败的玩家 |
| [get_neutral_player_group](#get_neutral_player_group) | 所有非中立玩家 |

---

## get_by_handle

method in PlayerGroup

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | py_role_group | py.RoleGroup |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | PlayerGroup |  |

- 示例

```lua
local result = y3.player_group.get_by_handle(player_group)
```

---

## create

method in PlayerGroup

- 描述

    创建空玩家组

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | PlayerGroup |  |

- 示例

```lua
local result = y3.player_group.create()
```

---

## count

method in PlayerGroup

- 描述

    获取玩家组中玩家数量

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer |  |

- 示例

```lua
local player_group = y3.player_group.create()

local result = player_group:count()
```

---

## pick

method in PlayerGroup

- 描述

    将玩家组转换为Lua的玩家数组

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Player[] |  |

- 示例

```lua
local player_group = y3.player_group.create()

local result = player_group:pick()
```

---

## pairs

method in PlayerGroup

- 描述

    遍历玩家组，请勿在遍历过程中修改玩家组。

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | fun(): | Player? |

- 示例

```lua
local player_group = y3.player_group.create()

local result = player_group:pairs()
```

---

## add_player

method in PlayerGroup

- 描述

    添加玩家

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |

- 返回值

    无

- 示例

```lua
local player_group = y3.player_group.create()
local player = y3.player.get_by_id(1)

player_group:add_player(player)
```

---

## remove_player

method in PlayerGroup

- 描述

    移除玩家

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |

- 返回值

    无

- 示例

```lua
local player_group = y3.player_group.create()
local player = y3.player.get_by_id(1)

player_group:remove_player(player)
```

---

## clear

method in PlayerGroup

- 描述

    清空玩家组

- 参数

    无

- 返回值

    无

- 示例

```lua
local player_group = y3.player_group.create()

player_group:clear()
```

---

## get_all_players

method in PlayerGroup

- 描述

    获取所有玩家

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | PlayerGroup | 单位组 |

- 示例

```lua
local result = y3.player_group.get_all_players()
```

---

## get_player_group_by_camp

method in PlayerGroup

- 描述

    阵营內所有玩家

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | camp | py.Camp | 阵营 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | PlayerGroup | 单位组 |

- 示例

```lua
local camp = GameAPI.get_camp_by_camp_id(1)

local result = y3.player_group.get_player_group_by_camp(camp)
```

---

## get_enemy_player_group_by_player

method in PlayerGroup

- 描述

    玩家的所有敌对玩家

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | PlayerGroup | 单位组 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = y3.player_group.get_enemy_player_group_by_player(player)
```

---

## get_ally_player_group_by_player

method in PlayerGroup

- 描述

    玩家的所有同盟玩家

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | PlayerGroup | 单位组 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = y3.player_group.get_ally_player_group_by_player(player)
```

---

## get_victorious_player_group

method in PlayerGroup

- 描述

    获取所有胜利的玩家

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | PlayerGroup | 单位组 |

- 示例

```lua
local result = y3.player_group.get_victorious_player_group()
```

---

## get_defeated_player_group

method in PlayerGroup

- 描述

    获取所有失败的玩家

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | PlayerGroup | 单位组 |

- 示例

```lua
local result = y3.player_group.get_defeated_player_group()
```

---

## get_neutral_player_group

method in PlayerGroup

- 描述

    所有非中立玩家

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | PlayerGroup | 单位组 |

- 示例

```lua
local result = y3.player_group.get_neutral_player_group()
```

---
