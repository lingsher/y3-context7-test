---
sidebarDepth: 1
---
# Ground (Game)

# 索引

Y3 编辑器 Ground 游戏接口，提供游戏相关功能。

---

| 接口 | 描述 |
| --- | --- |
| [set_collision](#set_collision) | 设置碰撞 |
| [get_collision](#get_collision) | 获取地图在该点位置的碰撞类型 |
| [get_view_block_type](#get_view_block_type) | 获取地图在该点位置的视野类型 |
| [get_height_level](#get_height_level) | 获取地图在该点位置的层级 |

---

## set_collision

method in Ground

- 描述

    设置碰撞

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | Point | 碰撞点 |
    | is_collision_effect | boolean | 碰撞是否生效 |
    | is_land_effect | boolean | 地面碰撞开关 |
    | is_air_effect | boolean | 空中碰撞开关 |

- 返回值

    无

- 示例

```lua
local point = y3.point(0, 0)

y3.ground.set_collision(point, true, true, true)
```

---

## get_collision

method in Ground

- 描述

    获取地图在该点位置的碰撞类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | Point | 碰撞点 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer |  |

- 示例

```lua
local point = y3.point(0, 0)

local result = y3.ground.get_collision(point)
```

---

## get_view_block_type

method in Ground

- 描述

    获取地图在该点位置的视野类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | Point |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer |  |

- 示例

```lua
local point = y3.point(0, 0)

local result = y3.ground.get_view_block_type(point)
```

---

## get_height_level

method in Ground

- 描述

    获取地图在该点位置的层级

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | Point | 点 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 层级 |

- 示例

```lua
local point = y3.point(0, 0)

local result = y3.ground.get_height_level(point)
```

---
