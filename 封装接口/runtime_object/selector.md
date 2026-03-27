---
sidebarDepth: 1
---
# Selector (运行时对象)

# 索引

Y3 编辑器 Selector 封装接口，提供高级方法操作 Selector 对象。

---

| 接口 | 描述 |
| --- | --- |
| [in_shape](#in_shape) | 形状 - 添加形状对象 |
| [in_range](#in_range) | 形状 - 在圆形区域内 |
| [is_enemy](#is_enemy) | 条件 - 是某个玩家的敌人 |
| [is_ally](#is_ally) | 条件 - 是某个玩家的同盟 |
| [of_player](#of_player) | 条件 - 属于某个玩家或某个玩家组 |
| [is_visible](#is_visible) | 条件 - 对某个玩家可见 |
| [not_visible](#not_visible) | 条件 - 对某个玩家不可见 |
| [not_in_group](#not_in_group) | 条件 - 不在某个单位组中 |
| [with_tag](#with_tag) | 条件 - 拥有特定标签 |
| [without_tag](#without_tag) | 条件 - 不拥有特定标签 |
| [not_is](#not_is) | 条件 - 不是某个特定的单位 |
| [in_state](#in_state) | 条件 - 拥有某个特定的状态 |
| [not_in_state](#not_in_state) | 条件 - 不拥有某个特定的状态 |
| [is_unit_key](#is_unit_key) | 条件 - 是某个特定的单位类型 |
| [is_unit_type](#is_unit_type) | 条件 - 是某个特定的单位类型 |
| [include_dead](#include_dead) | 选项 - 包含死亡的单位 |
| [count](#count) | 选项 - 选取的数量 |
| [sort_type](#sort_type) | 排序 - 按照某种方式排序 |
| [get](#get) | 进行选取 |
| [pick](#pick) | 进行选取 |
| [ipairs](#ipairs) | 进行遍历 |
| [create](#create) | 创建选取器 |

---

## in_shape

method in Selector

- 描述

    形状 - 添加形状对象

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | pos | Point |  |
    | shape | Shape |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local selector = y3.selector.create()
local point = y3.point(0, 0)
local shape = y3.shape.create_circular_shape(500)

local result = selector:in_shape(point, shape)
```

---

## in_range

method in Selector

- 描述

    形状 - 在圆形区域内

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | cent | Point \| Unit \| Item |  |
    | radius | number |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local selector = y3.selector.create()

local result = selector:in_range("cent", 1.0)
```

---

## is_enemy

method in Selector

- 描述

    条件 - 是某个玩家的敌人

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | p | Player |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local selector = y3.selector.create()
local player = y3.player.get_by_id(1)

local result = selector:is_enemy(player)
```

---

## is_ally

method in Selector

- 描述

    条件 - 是某个玩家的同盟

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | p | Player |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local selector = y3.selector.create()
local player = y3.player.get_by_id(1)

local result = selector:is_ally(player)
```

---

## of_player

method in Selector

- 描述

    条件 - 属于某个玩家或某个玩家组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | p | Player \| PlayerGroup |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local selector = y3.selector.create()

local result = selector:of_player("p")
```

---

## is_visible

method in Selector

- 描述

    条件 - 对某个玩家可见

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | p | Player |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local selector = y3.selector.create()
local player = y3.player.get_by_id(1)

local result = selector:is_visible(player)
```

---

## not_visible

method in Selector

- 描述

    条件 - 对某个玩家不可见

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | p | Player |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local selector = y3.selector.create()
local player = y3.player.get_by_id(1)

local result = selector:not_visible(player)
```

---

## not_in_group

method in Selector

- 描述

    条件 - 不在某个单位组中

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ug | UnitGroup |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local selector = y3.selector.create()
local ug = y3.unit_group.create()

local result = selector:not_in_group(ug)
```

---

## with_tag

method in Selector

- 描述

    条件 - 拥有特定标签

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local selector = y3.selector.create()

local result = selector:with_tag("tag")
```

---

## without_tag

method in Selector

- 描述

    条件 - 不拥有特定标签

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string? |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local selector = y3.selector.create()

local result = selector:without_tag(nil)
```

---

## not_is

method in Selector

- 描述

    条件 - 不是某个特定的单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | u | Unit |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local selector = y3.selector.create()
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = selector:not_is(unit)
```

---

## in_state

method in Selector

- 描述

    条件 - 拥有某个特定的状态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | state | integer \| y3.Const.UnitEnumState |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local selector = y3.selector.create()

local result = selector:in_state("state")
```

---

## not_in_state

method in Selector

- 描述

    条件 - 不拥有某个特定的状态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | state | integer \| y3.Const.UnitEnumState |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local selector = y3.selector.create()

local result = selector:not_in_state("state")
```

---

## is_unit_key

method in Selector

- 描述

    条件 - 是某个特定的单位类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local selector = y3.selector.create()
local unit_key = 134274569

local result = selector:is_unit_key(unit_key)
```

---

## is_unit_type

method in Selector

- 描述

    条件 - 是某个特定的单位类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_type | py.UnitType |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local selector = y3.selector.create()
local unit_type = 1

local result = selector:is_unit_type(unit_type)
```

---

## include_dead

method in Selector

- 描述

    选项 - 包含死亡的单位

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local selector = y3.selector.create()

local result = selector:include_dead()
```

---

## count

method in Selector

- 描述

    选项 - 选取的数量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | count | integer |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local selector = y3.selector.create()

local result = selector:count(1)
```

---

## sort_type

method in Selector

- 描述

    排序 - 按照某种方式排序

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | st | Selector.SortType |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Selector |  |

- 示例

```lua
local selector = y3.selector.create()
local st = '由近到远'

local result = selector:sort_type(st)
```

---

## get

method in Selector

- 描述

    进行选取

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | UnitGroup |  |

- 示例

```lua
local selector = y3.selector.create()

local result = selector:get()
```

---

## pick

method in Selector

- 描述

    进行选取

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Unit[] |  |

- 示例

```lua
local selector = y3.selector.create()

local result = selector:pick()
```

---

## ipairs

method in Selector

- 描述

    进行遍历

- 参数

    无

- 返回值

    无

- 示例

```lua
local selector = y3.selector.create()

selector:ipairs()
```

---

## create

method in Selector

- 描述

    创建选取器

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Selector |  |

- 示例

```lua
local result = y3.selector.create()
```

---
