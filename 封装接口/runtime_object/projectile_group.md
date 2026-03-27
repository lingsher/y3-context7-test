---
sidebarDepth: 1
---
# ProjectileGroup (运行时对象)

# 索引

Y3 编辑器 ProjectileGroup 封装接口，提供高级方法操作 ProjectileGroup 对象。

---

| 接口 | 描述 |
| --- | --- |
| [create_lua_projectile_group_from_py](#create_lua_projectile_group_from_py) |  |
| [get_all_projectile_in_shapes](#get_all_projectile_in_shapes) | 筛选范围内的所有投射物 |
| [get_all_projectiles_with_tag](#get_all_projectiles_with_tag) | 获取拥有指定标签的投射物 |
| [intersection](#intersection) | 取两个投射物组的交集 |
| [difference](#difference) | 取两个投射物组的差集（属于本组但不属于另一组的投射物） |
| [pick](#pick) | 遍历投射物组中投射物做动作 |
| [pairs](#pairs) | 遍历投射物组，请勿在遍历过程中修改投射物组。 |

---

## create_lua_projectile_group_from_py

method in ProjectileGroup

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | py_projectile_group | py.ProjectileGroup |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | ProjectileGroup |  |

- 示例

```lua
local other_projectile_group = y3.projectile_group.get_all_projectile_in_shapes(y3.point(1, 0), y3.shape.create_circular_shape(500))

local result = y3.projectile_group.create_lua_projectile_group_from_py(other_projectile_group.handle)
```

---

## get_all_projectile_in_shapes

method in ProjectileGroup

- 描述

    筛选范围内的所有投射物

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | Point | 点 |
    | shape | Shape | 筛选范围 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | ProjectileGroup |  |

- 示例

```lua
local point = y3.point(0, 0)
local shape = y3.shape.create_circular_shape(500)

local result = y3.projectile_group.get_all_projectile_in_shapes(point, shape)
```

---

## get_all_projectiles_with_tag

method in ProjectileGroup

- 描述

    获取拥有指定标签的投射物

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | 点 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | ProjectileGroup |  |

- 示例

```lua
local result = y3.projectile_group.get_all_projectiles_with_tag("tag")
```

---

## intersection

method in ProjectileGroup

- 描述

    取两个投射物组的交集

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_group | ProjectileGroup | 另一个投射物组 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | ProjectileGroup |  |

- 示例

```lua
local projectile_group = y3.projectile_group.get_all_projectile_in_shapes(y3.point(0, 0), y3.shape.create_circular_shape(500))
local other_projectile_group = y3.projectile_group.get_all_projectile_in_shapes(y3.point(1, 0), y3.shape.create_circular_shape(500))

local result = projectile_group:intersection(other_projectile_group)
```

---

## difference

method in ProjectileGroup

- 描述

    取两个投射物组的差集（属于本组但不属于另一组的投射物）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_group | ProjectileGroup | 另一个投射物组 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | ProjectileGroup |  |

- 示例

```lua
local projectile_group = y3.projectile_group.get_all_projectile_in_shapes(y3.point(0, 0), y3.shape.create_circular_shape(500))
local other_projectile_group = y3.projectile_group.get_all_projectile_in_shapes(y3.point(1, 0), y3.shape.create_circular_shape(500))

local result = projectile_group:difference(other_projectile_group)
```

---

## pick

method in ProjectileGroup

- 描述

    遍历投射物组中投射物做动作

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Projectile[] |  |

- 示例

```lua
local projectile_group = y3.projectile_group.get_all_projectile_in_shapes(y3.point(0, 0), y3.shape.create_circular_shape(500))

local result = projectile_group:pick()
```

---

## pairs

method in ProjectileGroup

- 描述

    遍历投射物组，请勿在遍历过程中修改投射物组。

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | fun(): | Projectile? |

- 示例

```lua
local projectile_group = y3.projectile_group.get_all_projectile_in_shapes(y3.point(0, 0), y3.shape.create_circular_shape(500))

local result = projectile_group:pairs()
```

---
