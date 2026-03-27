---
sidebarDepth: 1
---
# 技能 (Ability)

# 索引

Y3 编辑器技能对象相关接口，用于操作技能的属性、冷却、等级等。

---

| 接口 | 描述 |
| --- | --- |
| [api_get_str_attr](#api_get_str_attr) | 获取技能字符串属性 |
| [api_set_str_attr](#api_set_str_attr) | 设置技能字符串属性 |
| [api_set_name](#api_set_name) | 设置技能名字 |
| [api_get_owner](#api_get_owner) | 获取技能拥有者 |
| [api_get_owner_id](#api_get_owner_id) | 获取技能拥有者id |
| [api_get_type](#api_get_type) | 获取技能类型 |
| [api_get_ability_index](#api_get_ability_index) | 获取技能类型 |
| [api_get_ability_seq](#api_get_ability_seq) | 获取技能序列号 |
| [api_get_ability_cast_type](#api_get_ability_cast_type) | 获取技能释放类型 |
| [api_get_ability_global_id](#api_get_ability_global_id) | 获取技能全局唯一id |
| [api_remove](#api_remove) | 移除技能 |
| [api_get_level](#api_get_level) | 获取技能的等级 |
| [has_tag](#has_tag) | 是否拥有标记 |
| [api_remove_kv](#api_remove_kv) | 移除键值对 |
| [api_calc_ability_formula_kv](#api_calc_ability_formula_kv) | 计算公式类型KV |
| [add_timer](#add_timer) | 添加定时器 |
| [api_has_target](#api_has_target) | 技能对象是否拥有目标 |
| [api_get_release_position](#api_get_release_position) | 获取技能释放的位置 |
| [api_get_release_direction](#api_get_release_direction) | 获取技能释放的方向 |
| [api_get_float_attr](#api_get_float_attr) | 获取技能实数属性值 |
| [api_get_int_attr](#api_get_int_attr) | 获取技能整数属性值 |
| [api_get_bool_attr](#api_get_bool_attr) | 获取技能布尔属性值 |
| [api_get_ability_cast_range](#api_get_ability_cast_range) | 获取技能释放范围 |
| [api_set_ability_cast_range](#api_set_ability_cast_range) | 设置技能释放范围 |
| [api_set_ability_build_rotate](#api_set_ability_build_rotate) | 设置技能的建造朝向 |
| [api_set_ability_sector_radius](#api_set_ability_sector_radius) | 设置扇形指示器半径 |
| [api_set_ability_sector_angle](#api_set_ability_sector_angle) | 设置扇形指示器角度 |
| [api_set_ability_arrow_width](#api_set_ability_arrow_width) | 设置箭头/多段指示器宽度 |
| [api_set_ability_arrow_length](#api_set_ability_arrow_length) | 设置箭头/多段指示器长度 |
| [api_set_ability_circle_radius](#api_set_ability_circle_radius) | 设置圆形指示器半径 |
| [api_set_ability_pointer_type](#api_set_ability_pointer_type) | 设置技能指示器类型 |
| [api_get_ability_skill_pointer](#api_get_ability_skill_pointer) | 获取技能指示器类型 |
| [api_set_ability_icon](#api_set_ability_icon) | 设置技能图标 |
| [api_get_ability_player_attr_cost](#api_get_ability_player_attr_cost) | 获取技能玩家属性消耗 |
| [api_set_ability_player_attr_cost](#api_set_ability_player_attr_cost) | 设置技能玩家属性消耗 |
| [api_add_ability_player_attr_cost](#api_add_ability_player_attr_cost) | 增加技能玩家属性消耗 |
| [api_set_level](#api_set_level) | 设置技能等级 |
| [api_learn_ability](#api_learn_ability) | 学习技能 |
| [api_add_level](#api_add_level) | 增加技能等级 |
| [api_add_float_attr](#api_add_float_attr) | 增量修改技能实数属性值 |
| [api_set_float_attr](#api_set_float_attr) | 设置技能实数属性值 |
| [api_add_int_attr](#api_add_int_attr) | 增量修改技能整数属性值 |
| [api_set_int_attr](#api_set_int_attr) | 设置技能整数属性值 |
| [api_set_bool_attr](#api_set_bool_attr) | 设置技能布尔属性值 |
| [api_break_ability_in_cs](#api_break_ability_in_cs) | 阻止当前技能施法 |
| [api_get_ability_nearest_upgradable_unit_level](#api_get_ability_nearest_upgradable_unit_level) | 获取最近的技能可升级等级 |
| [api_get_ability_id](#api_get_ability_id) | 获取技能编号 |
| [api_is_melee_ability](#api_is_melee_ability) | 是否是近战技能 |
| [api_is_common_atk](#api_is_common_atk) | 是否是普攻 |
| [is_passive_ability](#is_passive_ability) | 是否是被动 |
| [api_get_cost_hp_can_die](#api_get_cost_hp_can_die) | 获取消耗生命是否致死 |
| [api_set_cost_hp_can_die](#api_set_cost_hp_can_die) | 设置消耗生命是否致死 |
| [api_get_can_cast_when_hp_insufficient](#api_get_can_cast_when_hp_insufficient) | 获取生命不足能否施放 |
| [api_set_can_cast_when_hp_insufficient](#api_set_can_cast_when_hp_insufficient) | 设置生命不足能否施放 |
| [api_get_name](#api_get_name) | 获取技能名称 |
| [api_set_influenced_by_cd_reduce](#api_set_influenced_by_cd_reduce) | 设置技能是否受冷却缩减影响 |
| [api_get_influenced_by_cd_reduce](#api_get_influenced_by_cd_reduce) | 是否受冷却缩减影响 |
| [api_get_ability_stack](#api_get_ability_stack) | 获取技能的充能层数 |
| [api_add_ability_stack_count](#api_add_ability_stack_count) | 增加技能充能层数 |
| [api_set_ability_stack_count](#api_set_ability_stack_count) | 设置技能充能层数 |
| [api_get_cd_left_time](#api_get_cd_left_time) | 获取当前技能剩余冷却时间 |
| [api_immediately_clear_cd](#api_immediately_clear_cd) | 技能立即冷却 |
| [api_change_ability_cd_cold_down](#api_change_ability_cd_cold_down) | 改变技能冷却时间 |
| [api_set_ability_cd](#api_set_ability_cd) | 设置技能冷却时间 |
| [api_add_ability_cd](#api_add_ability_cd) | 增加技能冷却时间 |
| [api_restart_cd](#api_restart_cd) | 从头开始冷却 |
| [api_set_ability_cur_stack_cd](#api_set_ability_cur_stack_cd) | 改变当次充能时间 |
| [api_get_stack_cd_left_time](#api_get_stack_cd_left_time) | 获取技能当前剩余充能时间 |
| [api_enable](#api_enable) | 启用技能 |
| [api_disable](#api_disable) | 禁用技能 |
| [api_play_sound_by_ability_for_role_relation](#api_play_sound_by_ability_for_role_relation) | 对技能所属单位的所属玩家关系播放音乐 |
| [api_set_autocast_enabled](#api_set_autocast_enabled) | 开关自动施法 |
| [api_is_autocast_enabled](#api_is_autocast_enabled) | 自动施法是否开启 |
| [api_set_ability_build_id](#api_set_ability_build_id) | 设置技能的建造目标类型(build_id) |
| [api_get_ability_build_id](#api_get_ability_build_id) | 获取技能的建造目标类型 |
| [api_set_ability_build_area](#api_set_ability_build_area) | 设置技能的限制建造区域 |
| [api_pause_cd](#api_pause_cd) | 暂停技能冷却 |
| [api_resume_cd](#api_resume_cd) | 恢复技能冷却 |
| [api_get_item](#api_get_item) | 获取技能绑定的物品 |
| [api_add_tag](#api_add_tag) | 技能添加键值对 |
| [api_remove_tag](#api_remove_tag) | 技能移除键值对 |
| [api_clear_tag](#api_clear_tag) | 清空键值对 |
| [api_set_ability_is_permanent](#api_set_ability_is_permanent) | 设置是否为永久性技能 |
| [api_add_filter_unit_tag](#api_add_filter_unit_tag) | 增加技能的筛选单位的tag |
| [api_remove_filter_unit_tag](#api_remove_filter_unit_tag) | 移除技能的筛选单位的tag |
| [api_add_filter_item_tag](#api_add_filter_item_tag) | 增加技能的筛选物品的tag |
| [api_remove_filter_item_tag](#api_remove_filter_item_tag) | 移除技能的筛选物品的tag |
| [api_add_collection_destructible_tags](#api_add_collection_destructible_tags) | 增加技能的筛选可破坏物的tag |
| [api_remove_collection_destructible_tags](#api_remove_collection_destructible_tags) | 移除技能的筛选可破坏物的tag |
| [api_ability_stop](#api_ability_stop) | 技能停止 |
| [api_ability_set_stash](#api_ability_set_stash) | 设置技能缓存 |
| [api_can_be_filtered_by_ability](#api_can_be_filtered_by_ability) | 是否可被当前技能筛选 |
| [api_ability_fast_forward_ability_state](#api_ability_fast_forward_ability_state) | 推进技能到下一个阶段 |
| [api_get_is_ability_forbidden](#api_get_is_ability_forbidden) | 当前技能是否被禁用 |
| [api_set_ability_pointer_transition_start_time](#api_set_ability_pointer_transition_start_time) | 设置技能指示器过渡起始时间 |
| [api_set_ability_pointer_transition_duration](#api_set_ability_pointer_transition_duration) | 设置技能指示器过渡时间 |
| [api_get_charge_time](#api_get_charge_time) | 获取技能的蓄力时长 |

---

## api_get_str_attr

method in Ability

- 描述

    获取技能字符串属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr | py.AbilityStrAttr | 标记名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string? | 字符串属性 |

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability.handle:api_get_str_attr(1)
```

---

## api_set_str_attr

method in Ability

- 描述

    设置技能字符串属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr | py.AbilityStrAttr | 标记名 |
    | value | string | 字符串值 |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_set_str_attr(1, "value")
```

---

## api_set_name

method in Ability

- 描述

    设置技能名字

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | string | 字符串值 |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_set_name("value")
```

---

## api_get_owner

method in Ability

- 描述

    获取技能拥有者

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit? | 技能拥有者 |

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability.handle:api_get_owner()
```

---

## api_get_owner_id

method in Ability

- 描述

    获取技能拥有者id

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitID? | 技能拥有者id |

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability.handle:api_get_owner_id()
```

---

## api_get_type

method in Ability

- 描述

    获取技能类型

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityType? | 技能类型 |

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability.handle:api_get_type()
```

---

## api_get_ability_index

method in Ability

- 描述

    获取技能类型

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityIndex? | 技能序号 |

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability.handle:api_get_ability_index()
```

---

## api_get_ability_seq

method in Ability

- 描述

    获取技能序列号

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilitySeq? | 技能Seq |

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability.handle:api_get_ability_seq()
```

---

## api_get_ability_cast_type

method in Ability

- 描述

    获取技能释放类型

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityCastType? | 技能释放类型 |

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability.handle:api_get_ability_cast_type()
```

---

## api_get_ability_global_id

method in Ability

- 描述

    获取技能全局唯一id

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 技能全局唯一id |

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability.handle:api_get_ability_global_id()
```

---

## api_remove

method in Ability

- 描述

    移除技能

- 参数

    无

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_remove()
```

---

## api_get_level

method in Ability

- 描述

    获取技能的等级

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 技能等级 |

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability.handle:api_get_level()
```

---

## has_tag

method in Ability

- 描述

    是否拥有标记

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | 标记名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 是否有标记 |

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability.handle:has_tag("tag")
```

---

## api_remove_kv

method in Ability

- 描述

    移除键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | k | string | 键 |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_remove_kv("k")
```

---

## api_calc_ability_formula_kv

method in Ability

- 描述

    计算公式类型KV

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | k | string | 键 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 值 |

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability.handle:api_calc_ability_formula_kv("k")
```

---

## add_timer

method in Ability

- 描述

    添加定时器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | time | py.Fixed | 定时时长 |
    | callback | function | 超时函数 |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:add_timer(Fix32(1), function() end)
```

---

## api_has_target

method in Ability

- 描述

    技能对象是否拥有目标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | runtime_id? | integer | runtime_id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 技能对象是否拥有目标 |

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability.handle:api_has_target(1)
```

---

## api_get_release_position

method in Ability

- 描述

    获取技能释放的位置

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | runtime_id? | integer | runtime_id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FPoint? | 技能释放的位置 |

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability.handle:api_get_release_position(1)
```

---

## api_get_release_direction

method in Ability

- 描述

    获取技能释放的方向

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | runtime_id? | integer | runtime_id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 技能释放的方向 |

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability.handle:api_get_release_direction(1)
```

---

## api_get_float_attr

method in Ability

- 描述

    获取技能实数属性值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr | string | 属性名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 实数属性值 |

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability.handle:api_get_float_attr("attr")
```

---

## api_get_int_attr

method in Ability

- 描述

    获取技能整数属性值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr | string | 属性名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 整数属性值 |

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability.handle:api_get_int_attr("attr")
```

---

## api_get_bool_attr

method in Ability

- 描述

    获取技能布尔属性值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr | string | 属性名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 布尔属性值 |

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability.handle:api_get_bool_attr("attr")
```

---

## api_get_ability_cast_range

method in Ability

- 描述

    获取技能释放范围

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 释放范围 |

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability.handle:api_get_ability_cast_range()
```

---

## api_set_ability_cast_range

method in Ability

- 描述

    设置技能释放范围

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | py.Fixed | 释放范围 |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_set_ability_cast_range(Fix32(1))
```

---

## api_set_ability_build_rotate

method in Ability

- 描述

    设置技能的建造朝向

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | py.Fixed | 建造朝向 |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_set_ability_build_rotate(Fix32(1))
```

---

## api_set_ability_sector_radius

method in Ability

- 描述

    设置扇形指示器半径

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | py.Fixed | 指示器半径 |
    | is_target? | boolean | 是否为目标大小 |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_set_ability_sector_radius(Fix32(1), true)
```

---

## api_set_ability_sector_angle

method in Ability

- 描述

    设置扇形指示器角度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | py.Fixed | 指示器角度 |
    | is_target? | boolean | 是否为目标大小 |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_set_ability_sector_angle(Fix32(1), true)
```

---

## api_set_ability_arrow_width

method in Ability

- 描述

    设置箭头/多段指示器宽度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | py.Fixed | 释放范围 |
    | is_target? | boolean | 是否为目标大小 |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_set_ability_arrow_width(Fix32(1), true)
```

---

## api_set_ability_arrow_length

method in Ability

- 描述

    设置箭头/多段指示器长度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | py.Fixed | 释放范围 |
    | is_target? | boolean | 是否为目标大小 |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_set_ability_arrow_length(Fix32(1), true)
```

---

## api_set_ability_circle_radius

method in Ability

- 描述

    设置圆形指示器半径

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | py.Fixed | 释放范围 |
    | is_target? | boolean | 是否为目标大小 |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_set_ability_circle_radius(Fix32(1), true)
```

---

## api_set_ability_pointer_type

method in Ability

- 描述

    设置技能指示器类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | pointer_type | integer | 指示器类型 |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_set_ability_pointer_type(1)
```

---

## api_get_ability_skill_pointer

method in Ability

- 描述

    获取技能指示器类型

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 指示器类型 |

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability.handle:api_get_ability_skill_pointer()
```

---

## api_set_ability_icon

method in Ability

- 描述

    设置技能图标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | integer | 图标 |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_set_ability_icon(1)
```

---

## api_get_ability_player_attr_cost

method in Ability

- 描述

    获取技能玩家属性消耗

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr | string | 玩家属性名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 玩家属性消耗 |

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability.handle:api_get_ability_player_attr_cost("attr")
```

---

## api_set_ability_player_attr_cost

method in Ability

- 描述

    设置技能玩家属性消耗

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr | string | 玩家属性名 |
    | value | py.Fixed | 玩家属性消耗 |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_set_ability_player_attr_cost("attr", Fix32(1))
```

---

## api_add_ability_player_attr_cost

method in Ability

- 描述

    增加技能玩家属性消耗

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr | string | 玩家属性名 |
    | value | py.Fixed | 玩家属性消耗 |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_add_ability_player_attr_cost("attr", Fix32(1))
```

---

## api_set_level

method in Ability

- 描述

    设置技能等级

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | level | integer | 技能等级 |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_set_level(1)
```

---

## api_learn_ability

method in Ability

- 描述

    学习技能

- 参数

    无

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_learn_ability()
```

---

## api_add_level

method in Ability

- 描述

    增加技能等级

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | level | integer | 技能等级 |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_add_level(1)
```

---

## api_add_float_attr

method in Ability

- 描述

    增量修改技能实数属性值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr | string | 属性名 |
    | value | py.Fixed | 实数属性值 |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_add_float_attr("attr", Fix32(1))
```

---

## api_set_float_attr

method in Ability

- 描述

    设置技能实数属性值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr | string | 属性名 |
    | value | py.Fixed | 实数属性值 |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_set_float_attr("attr", Fix32(1))
```

---

## api_add_int_attr

method in Ability

- 描述

    增量修改技能整数属性值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr | string | 属性名 |
    | value | integer | 整数属性值 |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_add_int_attr("attr", 1)
```

---

## api_set_int_attr

method in Ability

- 描述

    设置技能整数属性值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr | string | 属性名 |
    | value | integer | 整数属性值 |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_set_int_attr("attr", 1)
```

---

## api_set_bool_attr

method in Ability

- 描述

    设置技能布尔属性值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr | string | 属性名 |
    | value | boolean | 布尔属性值 |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_set_bool_attr("attr", true)
```

---

## api_break_ability_in_cs

method in Ability

- 描述

    阻止当前技能施法

- 参数

    无

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_break_ability_in_cs()
```

---

## api_get_ability_nearest_upgradable_unit_level

method in Ability

- 描述

    获取最近的技能可升级等级

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 等级 |

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability.handle:api_get_ability_nearest_upgradable_unit_level()
```

---

## api_get_ability_id

method in Ability

- 描述

    获取技能编号

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityKey? | 技能编号 |

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability.handle:api_get_ability_id()
```

---

## api_is_melee_ability

method in Ability

- 描述

    是否是近战技能

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 布尔值 |

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability.handle:api_is_melee_ability()
```

---

## api_is_common_atk

method in Ability

- 描述

    是否是普攻

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 布尔值 |

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability.handle:api_is_common_atk()
```

---

## is_passive_ability

method in Ability

- 描述

    是否是被动

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 布尔值 |

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability.handle:is_passive_ability()
```

---

## api_get_cost_hp_can_die

method in Ability

- 描述

    获取消耗生命是否致死

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 消耗生命是否致死 |

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability.handle:api_get_cost_hp_can_die()
```

---

## api_set_cost_hp_can_die

method in Ability

- 描述

    设置消耗生命是否致死

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | boolean | 能否释放 |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_set_cost_hp_can_die(true)
```

---

## api_get_can_cast_when_hp_insufficient

method in Ability

- 描述

    获取生命不足能否施放

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 生命不足能否施放 |

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability.handle:api_get_can_cast_when_hp_insufficient()
```

---

## api_set_can_cast_when_hp_insufficient

method in Ability

- 描述

    设置生命不足能否施放

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | boolean | 能否释放 |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_set_can_cast_when_hp_insufficient(true)
```

---

## api_get_name

method in Ability

- 描述

    获取技能名称

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string? | 技能名称 |

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability.handle:api_get_name()
```

---

## api_set_influenced_by_cd_reduce

method in Ability

- 描述

    设置技能是否受冷却缩减影响

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | boolean | 布尔属性值 |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_set_influenced_by_cd_reduce(true)
```

---

## api_get_influenced_by_cd_reduce

method in Ability

- 描述

    是否受冷却缩减影响

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 布尔值 |

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability.handle:api_get_influenced_by_cd_reduce()
```

---

## api_get_ability_stack

method in Ability

- 描述

    获取技能的充能层数

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 技能层数 |

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability.handle:api_get_ability_stack()
```

---

## api_add_ability_stack_count

method in Ability

- 描述

    增加技能充能层数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | integer | 充能层数 |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_add_ability_stack_count(1)
```

---

## api_set_ability_stack_count

method in Ability

- 描述

    设置技能充能层数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | integer | 充能层数 |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_set_ability_stack_count(1)
```

---

## api_get_cd_left_time

method in Ability

- 描述

    获取当前技能剩余冷却时间

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 剩余冷却时间 |

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability.handle:api_get_cd_left_time()
```

---

## api_immediately_clear_cd

method in Ability

- 描述

    技能立即冷却

- 参数

    无

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_immediately_clear_cd()
```

---

## api_change_ability_cd_cold_down

method in Ability

- 描述

    改变技能冷却时间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | py.Fixed | 冷却时间 |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_change_ability_cd_cold_down(Fix32(1))
```

---

## api_set_ability_cd

method in Ability

- 描述

    设置技能冷却时间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | py.Fixed | 冷却时间 |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_set_ability_cd(Fix32(1))
```

---

## api_add_ability_cd

method in Ability

- 描述

    增加技能冷却时间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | py.Fixed | 冷却时间 |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_add_ability_cd(Fix32(1))
```

---

## api_restart_cd

method in Ability

- 描述

    从头开始冷却

- 参数

    无

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_restart_cd()
```

---

## api_set_ability_cur_stack_cd

method in Ability

- 描述

    改变当次充能时间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | py.Fixed | 冷却时间 |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_set_ability_cur_stack_cd(Fix32(1))
```

---

## api_get_stack_cd_left_time

method in Ability

- 描述

    获取技能当前剩余充能时间

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 剩余充能时间 |

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability.handle:api_get_stack_cd_left_time()
```

---

## api_enable

method in Ability

- 描述

    启用技能

- 参数

    无

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_enable()
```

---

## api_disable

method in Ability

- 描述

    禁用技能

- 参数

    无

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_disable()
```

---

## api_play_sound_by_ability_for_role_relation

method in Ability

- 描述

    对技能所属单位的所属玩家关系播放音乐

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | camp_target | py.RoleRelation | 玩家关系 |
    | sid | py.AudioKey | 乐曲编号 |
    | loop | boolean | 是否循环 |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)
local relation = 1
local audio_key = 134274569

ability.handle:api_play_sound_by_ability_for_role_relation(relation, audio_key, true)
```

---

## api_set_autocast_enabled

method in Ability

- 描述

    开关自动施法

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | b | boolean | 开关 |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_set_autocast_enabled(true)
```

---

## api_is_autocast_enabled

method in Ability

- 描述

    自动施法是否开启

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 是否开启 |

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability.handle:api_is_autocast_enabled()
```

---

## api_set_ability_build_id

method in Ability

- 描述

    设置技能的建造目标类型(build_id)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | new_build_id | py.UnitKey | 单位物编ID |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)
local unit_key = 134274569

ability.handle:api_set_ability_build_id(unit_key)
```

---

## api_get_ability_build_id

method in Ability

- 描述

    获取技能的建造目标类型

- 参数

    无

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_get_ability_build_id()
```

---

## api_set_ability_build_area

method in Ability

- 描述

    设置技能的限制建造区域

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.Area | 区域对象 |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)
local area = y3.area.create_circle_area(y3.point.create(0, 0, 0), 500)

ability.handle:api_set_ability_build_area(area.handle)
```

---

## api_pause_cd

method in Ability

- 描述

    暂停技能冷却

- 参数

    无

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_pause_cd()
```

---

## api_resume_cd

method in Ability

- 描述

    恢复技能冷却

- 参数

    无

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_resume_cd()
```

---

## api_get_item

method in Ability

- 描述

    获取技能绑定的物品

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Item? | 物品实体 |

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability.handle:api_get_item()
```

---

## api_add_tag

method in Ability

- 描述

    技能添加键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | TAG |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_add_tag("tag")
```

---

## api_remove_tag

method in Ability

- 描述

    技能移除键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | TAG |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_remove_tag("tag")
```

---

## api_clear_tag

method in Ability

- 描述

    清空键值对

- 参数

    无

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_clear_tag()
```

---

## api_set_ability_is_permanent

method in Ability

- 描述

    设置是否为永久性技能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_permanent_ability | boolean | 是否为永久性技能 |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_set_ability_is_permanent(true)
```

---

## api_add_filter_unit_tag

method in Ability

- 描述

    增加技能的筛选单位的tag

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | 标签 |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_add_filter_unit_tag("tag")
```

---

## api_remove_filter_unit_tag

method in Ability

- 描述

    移除技能的筛选单位的tag

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | 标签 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string? | 标签 |

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability.handle:api_remove_filter_unit_tag("tag")
```

---

## api_add_filter_item_tag

method in Ability

- 描述

    增加技能的筛选物品的tag

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | 标签 |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_add_filter_item_tag("tag")
```

---

## api_remove_filter_item_tag

method in Ability

- 描述

    移除技能的筛选物品的tag

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | 标签 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string? | 标签 |

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability.handle:api_remove_filter_item_tag("tag")
```

---

## api_add_collection_destructible_tags

method in Ability

- 描述

    增加技能的筛选可破坏物的tag

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | 标签 |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_add_collection_destructible_tags("tag")
```

---

## api_remove_collection_destructible_tags

method in Ability

- 描述

    移除技能的筛选可破坏物的tag

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | 标签 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string? | 标签 |

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability.handle:api_remove_collection_destructible_tags("tag")
```

---

## api_ability_stop

method in Ability

- 描述

    技能停止

- 参数

    无

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_ability_stop()
```

---

## api_ability_set_stash

method in Ability

- 描述

    设置技能缓存

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | can_stash | boolean | 是否缓存 |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_ability_set_stash(true)
```

---

## api_can_be_filtered_by_ability

method in Ability

- 描述

    是否可被当前技能筛选

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位/物品/可破坏物 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 是否可被筛选 |

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)
local actor = unit.handle

local result = ability.handle:api_can_be_filtered_by_ability(actor)
```

---

## api_ability_fast_forward_ability_state

method in Ability

- 描述

    推进技能到下一个阶段

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | runtime_id? | integer | runtime_id |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_ability_fast_forward_ability_state(1)
```

---

## api_get_is_ability_forbidden

method in Ability

- 描述

    当前技能是否被禁用

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 当前技能是否被禁用 |

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability.handle:api_get_is_ability_forbidden()
```

---

## api_set_ability_pointer_transition_start_time

method in Ability

- 描述

    设置技能指示器过渡起始时间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | start_time | py.Fixed | 过渡起始时间 |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_set_ability_pointer_transition_start_time(Fix32(1))
```

---

## api_set_ability_pointer_transition_duration

method in Ability

- 描述

    设置技能指示器过渡时间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | duration | py.Fixed | 过渡时间 |

- 返回值

    无

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability.handle:api_set_ability_pointer_transition_duration(Fix32(1))
```

---

## api_get_charge_time

method in Ability

- 描述

    获取技能的蓄力时长

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 技能的蓄力时长 |

- 示例

```lua
-- 获取单位和技能对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ability.handle:api_get_charge_time()
```

---
