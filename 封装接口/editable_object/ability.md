---
sidebarDepth: 1
---
# Ability (物编对象)

# 索引

Y3 编辑器 Ability 封装接口，提供高级方法操作 Ability 对象。

---

| 接口 | 描述 |
| --- | --- |
| [get_by_handle](#get_by_handle) | 通过py层的技能实例获取lua层的技能实例 |
| [get_key](#get_key) |  |
| [is_cd_reduce](#is_cd_reduce) | 是否受冷却缩减影响 |
| [is_cost_hp_can_die](#is_cost_hp_can_die) | 消耗生命是否会死亡 |
| [can_cast_when_hp_insufficient](#can_cast_when_hp_insufficient) | 生命不足是否可以释放 |
| [has_tag](#has_tag) | 是否具有标签 |
| [get_tags_by_key](#get_tags_by_key) | 获取技能类型的所有标签 |
| [has_tag_by_key](#has_tag_by_key) | 技能类型是否具有标签 |
| [add_tag](#add_tag) | 添加标签 |
| [remove_tag](#remove_tag) | 移除标签 |
| [enable](#enable) | 启用技能 |
| [disable](#disable) | 禁用技能 |
| [restart_cd](#restart_cd) | 进入冷却 |
| [complete_cd](#complete_cd) | 完成冷却 |
| [stop_cast](#stop_cast) | 停止施放技能 |
| [remove](#remove) | 移除技能 |
| [set_level](#set_level) | 设置技能等级 |
| [get_level](#get_level) | 获取技能等级 |
| [add_cd](#add_cd) | 增加冷却时间 |
| [set_stack](#set_stack) | 设置充能层数 |
| [get_name](#get_name) |  |
| [set_float_attr](#set_float_attr) | 设置实数属性 |
| [set_int_attr](#set_int_attr) | 设置整数属性 |
| [set_cd](#set_cd) | 设置剩余冷却时间 |
| [add_level](#add_level) | 增加技能等级 |
| [add_stack](#add_stack) | 增加技能充能层数 |
| [add_remaining_cd](#add_remaining_cd) | 增加技能剩余冷却时间 |
| [add_float_attr](#add_float_attr) | 增加实数属性 |
| [add_int_attr](#add_int_attr) | 增加整数属性 |
| [set_name](#set_name) | 设置技能名字 |
| [set_description](#set_description) | 设置技能描述 |
| [get_description](#get_description) | 获取技能描述 |
| [learn](#learn) | 学习技能 |
| [set_charge_time](#set_charge_time) | 设置技能剩余充能时间 |
| [set_range](#set_range) | 设置技能施法范围 |
| [get_range](#get_range) | 获取技能施法范围 |
| [set_player_attr_cost](#set_player_attr_cost) | 设置技能玩家属性消耗 |
| [add_player_attr_cost](#add_player_attr_cost) | 增加技能玩家属性消耗 |
| [set_cd_reduce](#set_cd_reduce) | 设置技能是否受冷却缩减的影响 |
| [set_is_cost_hp_can_die](#set_is_cost_hp_can_die) | 设置消耗生命是否会死亡 |
| [set_can_cast_when_hp_insufficient](#set_can_cast_when_hp_insufficient) | 设置生命不足时是否可以释放技能 |
| [set_sector_radius](#set_sector_radius) | 设置扇形指示器半径 |
| [set_sector_angle](#set_sector_angle) | 设置扇形指示器夹角 |
| [set_arrow_length](#set_arrow_length) | 设置箭头/多段指示器长度 |
| [set_arrow_width](#set_arrow_width) | 设置箭头/多段指示器宽度 |
| [set_circle_radius](#set_circle_radius) | 设置箭圆形指示器半径 |
| [set_pointer_type](#set_pointer_type) | 设置技能指示器类型 |
| [get_charge_time](#get_charge_time) | 获取技能当前剩余充能时间 |
| [get_type](#get_type) | 获取技能种类 |
| [get_slot](#get_slot) | 获取技能所在技能位 |
| [get_seq](#get_seq) | 获取技能在单位身上的序号 |
| [get_player_attr_cost](#get_player_attr_cost) | 获取技能消耗的玩家属性值 |
| [get_cast_type](#get_cast_type) | 获取技能释放类型 AbilityCastType |
| [is_autocast_enabled](#is_autocast_enabled) | 自动施法是否开启 |
| [get_formula_kv](#get_formula_kv) | 获取技能公式类型的kv |
| [get_float_attr](#get_float_attr) | 获取实数属性 |
| [get_int_attr](#get_int_attr) | 获取整数属性 |
| [get_string_attr](#get_string_attr) | 获取字符串属性 |
| [get_owner](#get_owner) | 获取技能的拥有者 |
| [get_cd](#get_cd) | 获取当前冷却时间 |
| [is_exist](#is_exist) | 是否存在 |
| [get_target](#get_target) |  |
| [show_indicator](#show_indicator) | 显示技能指示器 |
| [set_autocast](#set_autocast) | 开关自动施法 |
| [check_precondition_by_key](#check_precondition_by_key) | 检查技能类型前置条件 |
| [is_cd_reduce_by_key](#is_cd_reduce_by_key) | 技能类型是否受冷却缩减影响 |
| [set_normal_attack_preview_state](#set_normal_attack_preview_state) | 设置玩家的普攻预览状态 |
| [set_smart_cast_with_pointer](#set_smart_cast_with_pointer) | 设置玩家的指示器在智能施法时是否显示 |
| [hide_pointer](#hide_pointer) | 关闭技能指示器 |
| [get_icon_by_key](#get_icon_by_key) | 获取技能类型的icon图标的图片ID |
| [get_icon](#get_icon) | 获取技能图标 |
| [get_formula_attr_by_key](#get_formula_attr_by_key) | 获取技能类型公式属性 |
| [get_name_by_key](#get_name_by_key) | 根据技能的key获取技能名字 |
| [get_description_by_key](#get_description_by_key) | 根据技能的key获取技能描述 |
| [set_icon](#set_icon) | 设置技能图标 |
| [set_build_rotate](#set_build_rotate) | 设置技能的建造朝向 |
| [get_skill_pointer](#get_skill_pointer) | 获取技能的指示器类型 |
| [get_skill_type_pointer](#get_skill_type_pointer) | 获取技能类型的指示器类型 |
| [set_max_cd](#set_max_cd) | 设置技能最大CD |
| [get_max_cd](#get_max_cd) | 获取技能最大CD |
| [pre_cast](#pre_cast) | 进入技能准备施法状态 |
| [prevent_cast](#prevent_cast) | 阻止即将开始的施法，只能在“施法-即将开始”事件中使用 |
| [get_item](#get_item) | 获取技能绑定的物品（技能对象在哪个物品对象上） |
| [set_ability_build_id](#set_ability_build_id) | 设置技能的建造目标类型(build_id) |
| [is_destroyed](#is_destroyed) |  |

---

## get_by_handle

method in Ability

- 描述

    通过py层的技能实例获取lua层的技能实例

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | py_ability | py.Ability | py层的技能实例 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Ability? | 返回在lua层初始化后的lua层技能实例 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = y3.ability.get_by_handle(ability.handle)
```

---

## get_key

method in Ability

- 描述

    

- 参数

    无

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:get_key()
```

---

## is_cd_reduce

method in Ability

- 描述

    是否受冷却缩减影响

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否受冷却缩减影响 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability:is_cd_reduce()
```

---

## is_cost_hp_can_die

method in Ability

- 描述

    消耗生命是否会死亡

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 消耗生命是否会死亡 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability:is_cost_hp_can_die()
```

---

## can_cast_when_hp_insufficient

method in Ability

- 描述

    生命不足是否可以释放

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 生命不足是否可以释放 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability:can_cast_when_hp_insufficient()
```

---

## has_tag

method in Ability

- 描述

    是否具有标签

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | 标签 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability:has_tag("tag")
```

---

## get_tags_by_key

method in Ability

- 描述

    获取技能类型的所有标签

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string[] |  |

- 示例

```lua
local item_key = 134274569

local result = y3.ability.get_tags_by_key(item_key)
```

---

## has_tag_by_key

method in Ability

- 描述

    技能类型是否具有标签

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey |  |
    | tag | string | 标签 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean |  |

- 示例

```lua
local item_key = 134274569

local result = y3.ability.has_tag_by_key(item_key, "tag")
```

---

## add_tag

method in Ability

- 描述

    添加标签

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | 标签 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:add_tag("tag")
```

---

## remove_tag

method in Ability

- 描述

    移除标签

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | 标签 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:remove_tag("tag")
```

---

## enable

method in Ability

- 描述

    启用技能

- 参数

    无

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:enable()
```

---

## disable

method in Ability

- 描述

    禁用技能

- 参数

    无

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:disable()
```

---

## restart_cd

method in Ability

- 描述

    进入冷却

- 参数

    无

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:restart_cd()
```

---

## complete_cd

method in Ability

- 描述

    完成冷却

- 参数

    无

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:complete_cd()
```

---

## stop_cast

method in Ability

- 描述

    停止施放技能

- 参数

    无

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:stop_cast()
```

---

## remove

method in Ability

- 描述

    移除技能

- 参数

    无

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:remove()
```

---

## set_level

method in Ability

- 描述

    设置技能等级

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | level | integer | 等级 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:set_level(1)
```

---

## get_level

method in Ability

- 描述

    获取技能等级

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 等级 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability:get_level()
```

---

## add_cd

method in Ability

- 描述

    增加冷却时间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | number | 冷却 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:add_cd(1.0)
```

---

## set_stack

method in Ability

- 描述

    设置充能层数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | integer | 层数 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:set_stack(1)
```

---

## get_name

method in Ability

- 描述

    

- 参数

    无

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:get_name()
```

---

## set_float_attr

method in Ability

- 描述

    设置实数属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | y3.Const.AbilityFloatAttr \| string | 属性key |
    | value | number | 属性值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:set_float_attr("key", 1.0)
```

---

## set_int_attr

method in Ability

- 描述

    设置整数属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | y3.Const.AbilityIntAttr \| string | 属性key |
    | value | integer | 属性值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:set_int_attr("key", 1)
```

---

## set_cd

method in Ability

- 描述

    设置剩余冷却时间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | number | 剩余冷却时间 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:set_cd(1.0)
```

---

## add_level

method in Ability

- 描述

    增加技能等级

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | integer | 等级 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:add_level(1)
```

---

## add_stack

method in Ability

- 描述

    增加技能充能层数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | integer | 层数 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:add_stack(1)
```

---

## add_remaining_cd

method in Ability

- 描述

    增加技能剩余冷却时间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | number | 剩余冷却时间 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:add_remaining_cd(1.0)
```

---

## add_float_attr

method in Ability

- 描述

    增加实数属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 属性key |
    | value | number | 属性值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:add_float_attr("key", 1.0)
```

---

## add_int_attr

method in Ability

- 描述

    增加整数属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 属性key |
    | value | integer | 属性值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:add_int_attr("key", 1)
```

---

## set_name

method in Ability

- 描述

    设置技能名字

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | name | string | 技能名字 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:set_name("name")
```

---

## set_description

method in Ability

- 描述

    设置技能描述

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | des | string | 描述 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:set_description("des")
```

---

## get_description

method in Ability

- 描述

    获取技能描述

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability:get_description()
```

---

## learn

method in Ability

- 描述

    学习技能

- 参数

    无

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:learn()
```

---

## set_charge_time

method in Ability

- 描述

    设置技能剩余充能时间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | number | 剩余充能时间 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:set_charge_time(1.0)
```

---

## set_range

method in Ability

- 描述

    设置技能施法范围

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | number | 施法范围 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:set_range(1.0)
```

---

## get_range

method in Ability

- 描述

    获取技能施法范围

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 施法范围 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability:get_range()
```

---

## set_player_attr_cost

method in Ability

- 描述

    设置技能玩家属性消耗

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 属性key |
    | value | number | 属性值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:set_player_attr_cost("key", 1.0)
```

---

## add_player_attr_cost

method in Ability

- 描述

    增加技能玩家属性消耗

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 属性key |
    | value | number | 属性值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:add_player_attr_cost("key", 1.0)
```

---

## set_cd_reduce

method in Ability

- 描述

    设置技能是否受冷却缩减的影响

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_influenced | boolean | 属性key |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:set_cd_reduce(true)
```

---

## set_is_cost_hp_can_die

method in Ability

- 描述

    设置消耗生命是否会死亡

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | can_die | boolean | 是否会死亡 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:set_is_cost_hp_can_die(true)
```

---

## set_can_cast_when_hp_insufficient

method in Ability

- 描述

    设置生命不足时是否可以释放技能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | can_cast | boolean | 是否可以释放 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:set_can_cast_when_hp_insufficient(true)
```

---

## set_sector_radius

method in Ability

- 描述

    设置扇形指示器半径

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | number | 半径 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:set_sector_radius(1.0)
```

---

## set_sector_angle

method in Ability

- 描述

    设置扇形指示器夹角

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | number | 角度 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:set_sector_angle(1.0)
```

---

## set_arrow_length

method in Ability

- 描述

    设置箭头/多段指示器长度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | number | 长度 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:set_arrow_length(1.0)
```

---

## set_arrow_width

method in Ability

- 描述

    设置箭头/多段指示器宽度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | number | 宽度 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:set_arrow_width(1.0)
```

---

## set_circle_radius

method in Ability

- 描述

    设置箭圆形指示器半径

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | number | 半径 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:set_circle_radius(1.0)
```

---

## set_pointer_type

method in Ability

- 描述

    设置技能指示器类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | type | y3.Const.AbilityPointerType | 技能指示器类型 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:set_pointer_type("type")
```

---

## get_charge_time

method in Ability

- 描述

    获取技能当前剩余充能时间

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

local result = ability:get_charge_time()
```

---

## get_type

method in Ability

- 描述

    获取技能种类

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | y3.Const.AbilityType | 技能种类 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability:get_type()
```

---

## get_slot

method in Ability

- 描述

    获取技能所在技能位

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | y3.Const.AbilityIndex | 技能所在技能位 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability:get_slot()
```

---

## get_seq

method in Ability

- 描述

    获取技能在单位身上的序号

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilitySeq | 技能序号 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability:get_seq()
```

---

## get_player_attr_cost

method in Ability

- 描述

    获取技能消耗的玩家属性值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | y3.Const.PlayerAttr \| string | 属性key |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 玩家属性值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability:get_player_attr_cost("key")
```

---

## get_cast_type

method in Ability

- 描述

    获取技能释放类型 AbilityCastType

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityCastType | 技能释放类型 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability:get_cast_type()
```

---

## is_autocast_enabled

method in Ability

- 描述

    自动施法是否开启

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否开启 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability:is_autocast_enabled()
```

---

## get_formula_kv

method in Ability

- 描述

    获取技能公式类型的kv

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 键值key |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability:get_formula_kv("key")
```

---

## get_float_attr

method in Ability

- 描述

    获取实数属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | y3.Const.AbilityFloatAttr \| string | 键值key |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability:get_float_attr("key")
```

---

## get_int_attr

method in Ability

- 描述

    获取整数属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | y3.Const.AbilityIntAttr \| string | 键值key |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability:get_int_attr("key")
```

---

## get_string_attr

method in Ability

- 描述

    获取字符串属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 键值key |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability:get_string_attr("key")
```

---

## get_owner

method in Ability

- 描述

    获取技能的拥有者

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Unit? | 技能拥有者 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability:get_owner()
```

---

## get_cd

method in Ability

- 描述

    获取当前冷却时间

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 当前冷却时间 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability:get_cd()
```

---

## is_exist

method in Ability

- 描述

    是否存在

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability:is_exist()
```

---

## get_target

method in Ability

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | cast | integer | 施法ID |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Unit|Destructible|Item|Point|nil | 目标 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability:get_target(1)
```

---

## show_indicator

method in Ability

- 描述

    显示技能指示器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)
local player = y3.player.get_by_id(1)

ability:show_indicator(player)
```

---

## set_autocast

method in Ability

- 描述

    开关自动施法

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | enable | boolean | 开关 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:set_autocast(true)
```

---

## check_precondition_by_key

method in Ability

- 描述

    检查技能类型前置条件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | ability_key | py.AbilityKey | 技能类型id (物编id) |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 技能类型前置条件是否满足 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ability_key = 134274569

local result = y3.ability.check_precondition_by_key(player, ability_key)
```

---

## is_cd_reduce_by_key

method in Ability

- 描述

    技能类型是否受冷却缩减影响

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能类型id (物编id) |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 技能类型是否受冷却缩减影响 |

- 示例

```lua
local ability_key = 134274569

local result = y3.ability.is_cd_reduce_by_key(ability_key)
```

---

## set_normal_attack_preview_state

method in Ability

- 描述

    设置玩家的普攻预览状态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | state | boolean | 状态 开/关 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

y3.ability.set_normal_attack_preview_state(player, true)
```

---

## set_smart_cast_with_pointer

method in Ability

- 描述

    设置玩家的指示器在智能施法时是否显示

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | state | boolean | 状态 开/关 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

y3.ability.set_smart_cast_with_pointer(player, true)
```

---

## hide_pointer

method in Ability

- 描述

    关闭技能指示器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

y3.ability.hide_pointer(player)
```

---

## get_icon_by_key

method in Ability

- 描述

    获取技能类型的icon图标的图片ID

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能类型id (物编id) |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Texture | 图片ID |

- 示例

```lua
local ability_key = 134274569

local result = y3.ability.get_icon_by_key(ability_key)
```

---

## get_icon

method in Ability

- 描述

    获取技能图标

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Texture | 图片ID |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability:get_icon()
```

---

## get_formula_attr_by_key

method in Ability

- 描述

    获取技能类型公式属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_id | py.AbilityKey | 技能类型id(物编id) |
    | attr_name | string | 属性名称 |
    | level | integer | 技能等级 |
    | stack_count | integer | 技能层数 |
    | unit_hp_max | number | 单位最大生命 |
    | unit_hp_cur | number | 单位当前生命 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 值 |

- 示例

```lua
local ability_key = 134274569

local result = y3.ability.get_formula_attr_by_key(ability_key, "attr_name", 1, 1, 1.0, 1.0)
```

---

## get_name_by_key

method in Ability

- 描述

    根据技能的key获取技能名字

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 技能名字 |

- 示例

```lua
local ability_key = 134274569

local result = y3.ability.get_name_by_key(ability_key)
```

---

## get_description_by_key

method in Ability

- 描述

    根据技能的key获取技能描述

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 描述 |

- 示例

```lua
local ability_key = 134274569

local result = y3.ability.get_description_by_key(ability_key)
```

---

## set_icon

method in Ability

- 描述

    设置技能图标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | integer | 图片id |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:set_icon(1)
```

---

## set_build_rotate

method in Ability

- 描述

    设置技能的建造朝向

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | angle | number | 角度 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:set_build_rotate(1.0)
```

---

## get_skill_pointer

method in Ability

- 描述

    获取技能的指示器类型

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | y3.Const.AbilityPointerType |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability:get_skill_pointer()
```

---

## get_skill_type_pointer

method in Ability

- 描述

    获取技能类型的指示器类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | name | py.AbilityKey |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | y3.Const.AbilityPointerType |  |

- 示例

```lua
local ability_key = 134274569

local result = y3.ability.get_skill_type_pointer(ability_key)
```

---

## set_max_cd

method in Ability

- 描述

    设置技能最大CD

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | number |  |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:set_max_cd(1.0)
```

---

## get_max_cd

method in Ability

- 描述

    获取技能最大CD

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

local result = ability:get_max_cd()
```

---

## pre_cast

method in Ability

- 描述

    进入技能准备施法状态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)
local player = y3.player.get_by_id(1)

ability:pre_cast(player)
```

---

## prevent_cast

method in Ability

- 描述

    阻止即将开始的施法，只能在“施法-即将开始”事件中使用

- 参数

    无

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:prevent_cast()
```

---

## get_item

method in Ability

- 描述

    获取技能绑定的物品（技能对象在哪个物品对象上）

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

local result = ability:get_item()
```

---

## set_ability_build_id

method in Ability

- 描述

    设置技能的建造目标类型(build_id)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | build_id | py.UnitKey | 单位物编ID |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)
local unit_key = 134274569

ability:set_ability_build_id(unit_key)
```

---

## is_destroyed

method in Ability

- 描述

    

- 参数

    无

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:is_destroyed()
```

---
