---
sidebarDepth: 1
---
# UnitGroup (运行时对象)

# 索引

Y3 编辑器 UnitGroup 封装接口，提供高级方法操作 UnitGroup 对象。

---

| 接口 | 描述 |
| --- | --- |
| [get_by_handle](#get_by_handle) |  |
| [create](#create) | 创建空单位组 |
| [pick](#pick) | 将单位组转换为Lua的单位数组 |
| [pairs](#pairs) | 遍历单位组，请勿在遍历过程中修改单位组。 |
| [select_units](#select_units) | 根据单位组选中单位 |
| [add_unit](#add_unit) | 添加单位 |
| [remove_unit](#remove_unit) | 移除单位 |
| [remove_units_by_key](#remove_units_by_key) | 移除单位类型 |
| [clear](#clear) | 清空单位组 |
| [pick_random_n](#pick_random_n) | 单位组中随机整数个单位 |
| [pick_by_key](#pick_by_key) | 挑选指定单位类型的单位 |
| [count](#count) | 获取单位组中单位数量 |
| [count_by_key](#count_by_key) | 单位组中单位类型的数量 |
| [get_first](#get_first) | 获取单位组内第一个单位 |
| [get_random](#get_random) | 获取单位组中随机一个单位 |
| [get_last](#get_last) | 获取单位组内最后一个单位 |

---

## get_by_handle

method in UnitGroup

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | py_unit_group | py.UnitGroup |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | UnitGroup |  |

- 示例

```lua
local result = y3.unit_group.get_by_handle(unit_group)
```

---

## create

method in UnitGroup

- 描述

    创建空单位组

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | UnitGroup |  |

- 示例

```lua
local result = y3.unit_group.create()
```

---

## pick

method in UnitGroup

- 描述

    将单位组转换为Lua的单位数组

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Unit[] |  |

- 示例

```lua
local unit_group = y3.unit_group.create()

local result = unit_group:pick()
```

---

## pairs

method in UnitGroup

- 描述

    遍历单位组，请勿在遍历过程中修改单位组。

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | fun(): | Unit? |

- 示例

```lua
local unit_group = y3.unit_group.create()

local result = unit_group:pairs()
```

---

## select_units

method in UnitGroup

- 描述

    根据单位组选中单位

- 参数

    无

- 返回值

    无

- 示例

```lua
local unit_group = y3.unit_group.create()

unit_group:select_units()
```

---

## add_unit

method in UnitGroup

- 描述

    添加单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 单位 |

- 返回值

    无

- 示例

```lua
local unit_group = y3.unit_group.create()
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit_group:add_unit(unit)
```

---

## remove_unit

method in UnitGroup

- 描述

    移除单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 单位 |

- 返回值

    无

- 示例

```lua
local unit_group = y3.unit_group.create()
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit_group:remove_unit(unit)
```

---

## remove_units_by_key

method in UnitGroup

- 描述

    移除单位类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位类型id |

- 返回值

    无

- 示例

```lua
local unit_group = y3.unit_group.create()
local unit_key = 134274569

unit_group:remove_units_by_key(unit_key)
```

---

## clear

method in UnitGroup

- 描述

    清空单位组

- 参数

    无

- 返回值

    无

- 示例

```lua
local unit_group = y3.unit_group.create()

unit_group:clear()
```

---

## pick_random_n

method in UnitGroup

- 描述

    单位组中随机整数个单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | count | integer |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | UnitGroup | 随机整数个单位 |

- 示例

```lua
local unit_group = y3.unit_group.create()

local result = unit_group:pick_random_n(1)
```

---

## pick_by_key

method in UnitGroup

- 描述

    挑选指定单位类型的单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位类型id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | UnitGroup | 单位组 |

- 示例

```lua
local unit_key = 134274569

local result = y3.unit_group.pick_by_key(unit_key)
```

---

## count

method in UnitGroup

- 描述

    获取单位组中单位数量

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 单位数量 |

- 示例

```lua
local unit_group = y3.unit_group.create()

local result = unit_group:count()
```

---

## count_by_key

method in UnitGroup

- 描述

    单位组中单位类型的数量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 单位类型的数量 |

- 示例

```lua
local unit_group = y3.unit_group.create()
local unit_key = 134274569

local result = unit_group:count_by_key(unit_key)
```

---

## get_first

method in UnitGroup

- 描述

    获取单位组内第一个单位

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Unit? | 单位组内第一个单位 |

- 示例

```lua
local unit_group = y3.unit_group.create()

local result = unit_group:get_first()
```

---

## get_random

method in UnitGroup

- 描述

    获取单位组中随机一个单位

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Unit? | 单位组中随机一个单位 |

- 示例

```lua
local unit_group = y3.unit_group.create()

local result = unit_group:get_random()
```

---

## get_last

method in UnitGroup

- 描述

    获取单位组内最后一个单位

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Unit? | 最后一个单位 |

- 示例

```lua
local unit_group = y3.unit_group.create()

local result = unit_group:get_last()
```

---
