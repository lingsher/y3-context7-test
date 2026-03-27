---
sidebarDepth: 1
---
# Cast (运行时对象)

# 索引

Y3 编辑器 Cast 封装接口，提供高级方法操作 Cast 对象。

---

| 接口 | 描述 |
| --- | --- |
| [get_ability](#get_ability) | 获取技能 |
| [get_angle](#get_angle) | 获取施法方向 |
| [get_target_item](#get_target_item) | 获取施法目标物品 |
| [get_target_unit](#get_target_unit) | 获取施法目标单位 |
| [get_target_destructible](#get_target_destructible) | 获取施法目标可破坏物 |
| [get_target_point](#get_target_point) | 获取施法目标点 |
| [get](#get) |  |

---

## get_ability

method in Cast

- 描述

    获取技能

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Ability |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)
local cast = ability:get_current_cast()

local result = cast:get_ability()
```

---

## get_angle

method in Cast

- 描述

    获取施法方向

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)
local cast = ability:get_current_cast()

local result = cast:get_angle()
```

---

## get_target_item

method in Cast

- 描述

    获取施法目标物品

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Item? |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)
local cast = ability:get_current_cast()

local result = cast:get_target_item()
```

---

## get_target_unit

method in Cast

- 描述

    获取施法目标单位

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Unit? |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)
local cast = ability:get_current_cast()

local result = cast:get_target_unit()
```

---

## get_target_destructible

method in Cast

- 描述

    获取施法目标可破坏物

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Destructible? |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)
local cast = ability:get_current_cast()

local result = cast:get_target_destructible()
```

---

## get_target_point

method in Cast

- 描述

    获取施法目标点

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Point? |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)
local cast = ability:get_current_cast()

local result = cast:get_target_point()
```

---

## get

method in Cast

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability | Ability |  |
    | cast_id | integer |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Cast |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = y3.cast.get(ability, 1)
```

---
