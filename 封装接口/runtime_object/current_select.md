---
sidebarDepth: 1
---
# Player (运行时对象)

# 索引

Y3 编辑器 Player 封装接口，提供高级方法操作 Player 对象。

---

| 接口 | 描述 |
| --- | --- |
| [get_selecting_unit](#get_selecting_unit) | 获取选中的单位（同步） |
| [get_selecting_unit_group](#get_selecting_unit_group) | 获取选中的单位组（同步） |
| [get_local_selecting_unit](#get_local_selecting_unit) | 获取本地选中的单位（本地） |
| [get_local_selecting_unit_group](#get_local_selecting_unit_group) | 获取本地选中的单位组（本地） |

---

## get_selecting_unit

method in Player

- 描述

    获取选中的单位（同步）

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Unit? |  |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = player:get_selecting_unit()
```

---

## get_selecting_unit_group

method in Player

- 描述

    获取选中的单位组（同步）

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | UnitGroup? |  |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = player:get_selecting_unit_group()
```

---

## get_local_selecting_unit

method in Player

- 描述

    获取本地选中的单位（本地）

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Unit? |  |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = player:get_local_selecting_unit()
```

---

## get_local_selecting_unit_group

method in Player

- 描述

    获取本地选中的单位组（本地）

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | UnitGroup? |  |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = player:get_local_selecting_unit_group()
```

---
