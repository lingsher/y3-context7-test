---
sidebarDepth: 1
---
# SaveData (存档系统)

# 索引

玩家存档系统，支持保存和读取多种类型的数据（布尔、整数、实数、字符串、表）。数据会自动同步到服务器。

---

## 方法

| 接口 | 描述 |
| --- | --- |
| [load_boolean](#load_boolean) | 读取布尔存档 |
| [save_boolean](#save_boolean) | 保存布尔存档 |
| [load_integer](#load_integer) | 读取整数存档 |
| [save_integer](#save_integer) | 保存整数存档 |
| [add_integer](#add_integer) | 增加整数存档 |
| [load_real](#load_real) | 读取实数存档 |
| [save_real](#save_real) | 保存实数存档 |
| [add_real](#add_real) | 增加实数存档 |
| [load_string](#load_string) | 读取字符串存档 |
| [save_string](#save_string) | 保存字符串存档 |
| [load_table](#load_table) | 读取表存档 |

---

## load_boolean

function in y3.save_data

`y3.save_data.load_boolean(player: Player, slot: integer) -> boolean`

- 描述

    读取玩家的布尔型存档数据

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家对象 |
    | slot | integer | 存档槽位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 存档值（默认 false） |

- 示例

```lua
-- 读取布尔存档
local player = y3.player(1)
local has_tutorial = y3.save_data.load_boolean(player, 1)
if not has_tutorial then
    print('玩家尚未完成教程')
end
```

---

## save_boolean

function in y3.save_data

`y3.save_data.save_boolean(player: Player, slot: integer, value: boolean)`

- 描述

    保存玩家的布尔型存档数据

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家对象 |
    | slot | integer | 存档槽位 |
    | value | boolean | 要保存的值 |

- 示例

```lua
-- 保存布尔存档
local player = y3.player(1)
y3.save_data.save_boolean(player, 1, true)  -- 标记教程完成
```

---

## load_integer

function in y3.save_data

`y3.save_data.load_integer(player: Player, slot: integer) -> integer`

- 描述

    读取玩家的整数型存档数据

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 存档值（默认 0） |

- 示例

```lua
-- 读取整数存档
local player = y3.player(1)
local total_wins = y3.save_data.load_integer(player, 10)
print('总胜利次数:', total_wins)
```

---

## save_integer

function in y3.save_data

`y3.save_data.save_integer(player: Player, slot: integer, value: integer)`

- 描述

    保存玩家的整数型存档数据

- 示例

```lua
-- 保存整数存档
local player = y3.player(1)
y3.save_data.save_integer(player, 10, 100)  -- 保存胜利次数
```

---

## add_integer

function in y3.save_data

`y3.save_data.add_integer(player: Player, slot: integer, value: integer)`

- 描述

    增加玩家的整数型存档数据

- 示例

```lua
-- 增加整数存档
local player = y3.player(1)
y3.save_data.add_integer(player, 10, 1)  -- 胜利次数 +1
```

---

## load_real

function in y3.save_data

`y3.save_data.load_real(player: Player, slot: integer) -> number`

- 描述

    读取玩家的实数型存档数据

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 存档值（默认 0.0） |

- 示例

```lua
-- 读取实数存档
local player = y3.player(1)
local play_time = y3.save_data.load_real(player, 20)
print('游戏时长:', play_time, '小时')
```

---

## save_real

function in y3.save_data

`y3.save_data.save_real(player: Player, slot: integer, value: number)`

- 描述

    保存玩家的实数型存档数据

- 示例

```lua
-- 保存实数存档
local player = y3.player(1)
y3.save_data.save_real(player, 20, 12.5)  -- 保存游戏时长
```

---

## add_real

function in y3.save_data

`y3.save_data.add_real(player: Player, slot: integer, value: number)`

- 描述

    增加玩家的实数型存档数据

- 示例

```lua
-- 增加实数存档
local player = y3.player(1)
y3.save_data.add_real(player, 20, 0.5)  -- 游戏时长 +0.5 小时
```

---

## load_string

function in y3.save_data

`y3.save_data.load_string(player: Player, slot: integer) -> string`

- 描述

    读取玩家的字符串型存档数据

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 存档值（默认空字符串） |

- 示例

```lua
-- 读取字符串存档
local player = y3.player(1)
local nickname = y3.save_data.load_string(player, 30)
print('玩家昵称:', nickname)
```

---

## save_string

function in y3.save_data

`y3.save_data.save_string(player: Player, slot: integer, value: string)`

- 描述

    保存玩家的字符串型存档数据

- 示例

```lua
-- 保存字符串存档
local player = y3.player(1)
y3.save_data.save_string(player, 30, '勇者小明')
```

---

## load_table

function in y3.save_data

`y3.save_data.load_table(player: Player, slot: integer, disable_cover?: boolean) -> table`

- 描述

    读取玩家的表型存档数据。返回的表是代理表，修改字段会自动同步到存档。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家对象 |
    | slot | integer | 存档槽位 |
    | disable_cover? | boolean | 是否禁用覆盖（默认 true） |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | table | 代理表，修改会自动保存 |

- 示例

```lua
-- 读取表存档
local player = y3.player(1)
local save = y3.save_data.load_table(player, 100)

-- 直接修改会自动保存
save.level = 10
save.gold = 5000
save.items = {}
save.items[1] = 1001
save.items[2] = 1002
```
