---
sidebarDepth: 1
---
# ItemGroup (运行时对象)

# 索引

Y3 编辑器 ItemGroup 封装接口，提供高级方法操作 ItemGroup 对象。

---

| 接口 | 描述 |
| --- | --- |
| [create_lua_item_group_from_py](#create_lua_item_group_from_py) |  |
| [get_by_handle](#get_by_handle) |  |
| [pick](#pick) | 遍历物品组中玩家做动作 |
| [pairs](#pairs) | 遍历物品组，请勿在遍历过程中修改物品组。 |
| [get_all_items_in_shapes](#get_all_items_in_shapes) | 筛选范围内的所有物品 |
| [create](#create) |  |

---

## create_lua_item_group_from_py

method in ItemGroup

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | py_item_group | py.ItemGroup |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | ItemGroup |  |

- 示例

```lua
local result = y3.item_group.create_lua_item_group_from_py(item_group)
```

---

## get_by_handle

method in ItemGroup

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | py_item_group | py.ItemGroup |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | ItemGroup |  |

- 示例

```lua
local result = y3.item_group.get_by_handle(item_group)
```

---

## pick

method in ItemGroup

- 描述

    遍历物品组中玩家做动作

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Item[] |  |

- 示例

```lua
local item_group = y3.item_group.create()

local result = item_group:pick()
```

---

## pairs

method in ItemGroup

- 描述

    遍历物品组，请勿在遍历过程中修改物品组。

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | fun(): | Item? |

- 示例

```lua
local item_group = y3.item_group.create()

local result = item_group:pairs()
```

---

## get_all_items_in_shapes

method in ItemGroup

- 描述

    筛选范围内的所有物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | Point | 点 |
    | shape | Shape | 筛选范围 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | ItemGroup |  |

- 示例

```lua
local point = y3.point(0, 0)
local shape = y3.shape.create_circular_shape(500)

local result = y3.item_group.get_all_items_in_shapes(point, shape)
```

---

## create

method in ItemGroup

- 描述

    

- 参数

    无

- 返回值

    无

- 示例

```lua
y3.item_group.create()
```

---
