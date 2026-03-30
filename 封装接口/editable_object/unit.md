---
sidebarDepth: 1
---
# Unit (物编对象)

# 索引

Y3 编辑器 Unit 封装接口，提供高级方法操作 Unit 对象。

---

| 接口 | 描述 |
| --- | --- |
| [get_by_handle](#get_by_handle) | 通过py层的单位实例获取lua层的单位实例 |
| [get_by_id](#get_by_id) | 根据唯一ID获取单位。 |
| [get_by_res_id](#get_by_res_id) | 获取摆放在场景上的单位 |
| [get_by_string](#get_by_string) | 根据字符串获取单位，字符串是通过 `tostring(Unit)` |
| [is_exist](#is_exist) | 是否存在 |
| [get_id](#get_id) | 获取唯一ID |
| [remove_ability_by_key](#remove_ability_by_key) | 移除技能(指定类型) |
| [add_item](#add_item) | 单位添加物品 |
| [remove_item](#remove_item) | 单位移除物品 |
| [shift_item](#shift_item) | 移动物品 |
| [exchange_item](#exchange_item) | 交换物品 |
| [get_abilities_by_type](#get_abilities_by_type) | 获取指定类型的所有技能 |
| [get_buffs](#get_buffs) | 获取单位身上的魔法效果 |
| [switch_ability](#switch_ability) | 交换技能位置 |
| [switch_ability_by_slot](#switch_ability_by_slot) | 根据坑位交换技能 |
| [stop_all_abilities](#stop_all_abilities) | 停止所有技能 |
| [add_ability](#add_ability) | 添加技能 |
| [remove_ability](#remove_ability) | 移除技能 |
| [find_ability](#find_ability) | 通过技能名寻找技能 |
| [get_ability_by_slot](#get_ability_by_slot) | 获得某个技能位的的技能 |
| [get_ability_by_seq](#get_ability_by_seq) | 根据技能序号获取技能 |
| [get_common_attack](#get_common_attack) | comment 获取普攻技能 |
| [get_item_by_slot](#get_item_by_slot) | 获取单位背包槽位上的物品 |
| [get_all_items](#get_all_items) | 单位的所有物品 |
| [unit_gains_tech](#unit_gains_tech) | 单位获得科技 |
| [create_unit](#create_unit) | 创建单位 |
| [kill_by](#kill_by) | 杀死单位 |
| [is_casting](#is_casting) | 单位是否有正在释放的技能 |
| [get_casting_ability](#get_casting_ability) | 获取正在释放的技能 |
| [create_illusion](#create_illusion) | 创建幻象 |
| [remove](#remove) | 删除单位 |
| [blink](#blink) | 传送到点 |
| [set_point](#set_point) | 强制传送到点 |
| [reborn](#reborn) | 复活单位 |
| [heals](#heals) | 造成治疗 |
| [add_tag](#add_tag) | 添加标签 |
| [remove_tag](#remove_tag) | 移除标签 |
| [add_state](#add_state) | 添加状态 |
| [remove_state](#remove_state) | 移除状态 |
| [add_multi_state](#add_multi_state) | 添加多个状态 |
| [remove_multi_state](#remove_multi_state) | 移除多个状态 |
| [has_state](#has_state) | 是否有某个状态 |
| [add_state_gc](#add_state_gc) | 添加状态 |
| [learn](#learn) | 学习技能 |
| [command](#command) | 发布命令 |
| [move_to_pos](#move_to_pos) | 命令移动 |
| [stop](#stop) | 命令停止 |
| [hold](#hold) | 命令驻守 |
| [attack_move](#attack_move) | 命令攻击移动 |
| [attack_target](#attack_target) | 命令攻击目标 |
| [move_along_road](#move_along_road) | 命令沿路径移动 |
| [cast](#cast) | 命令发动技能 |
| [pick_item](#pick_item) | 命令拾取物品 |
| [drop_item](#drop_item) | 命令丢弃物品 |
| [give_item](#give_item) | 命令给予物品 |
| [use_item](#use_item) | 命令使用物品 |
| [follow](#follow) | 命令跟随单位 |
| [set_facing](#set_facing) | 设置朝向 |
| [set_name](#set_name) | 设置名称 |
| [set_name_show_type](#set_name_show_type) | 设置名称显示方式 |
| [set_description](#set_description) | 设置描述 |
| [set_attr](#set_attr) | 设置属性 |
| [add_attr](#add_attr) | 增加属性 |
| [add_attr_gc](#add_attr_gc) | 增加属性 |
| [set_level](#set_level) | 设置等级 |
| [add_level](#add_level) | 增加等级 |
| [set_exp](#set_exp) | 设置经验 |
| [add_exp](#add_exp) | 增加经验值 |
| [set_hp](#set_hp) | 设置当前生命值 |
| [add_hp](#add_hp) | 增加当前生命值 |
| [set_mp](#set_mp) | 设置当前魔法值 |
| [add_mp](#add_mp) | 增加当前魔法值 |
| [set_ability_point](#set_ability_point) | 设置技能点 |
| [add_ability_point](#add_ability_point) | 增加技能点 |
| [change_owner](#change_owner) | 改变所属玩家 |
| [set_height](#set_height) | 设置飞行高度 |
| [set_life_cycle](#set_life_cycle) | 设置生命周期 |
| [pause_life_cycle](#pause_life_cycle) | 设置生命周期暂停状态 |
| [set_alert_range](#set_alert_range) | 设置警戒范围 |
| [set_cancel_alert_range](#set_cancel_alert_range) | 设置取消警戒范围 |
| [set_pkg_cnt](#set_pkg_cnt) | 设置背包栏的槽位数 |
| [set_bar_cnt](#set_bar_cnt) | 设置物品栏的槽位数 |
| [set_behavior](#set_behavior) | 设置默认单位行为 |
| [set_attr_growth](#set_attr_growth) | ****************************************** |
| [set_reward_exp](#set_reward_exp) | 设置被击杀的经验值奖励 |
| [set_reward_res](#set_reward_res) | 设置被击杀的玩家属性奖励 |
| [set_attack_type](#set_attack_type) | 设置攻击类型 |
| [set_armor_type](#set_armor_type) | 设置护甲类型 |
| [start_ghost](#start_ghost) | ************************残影优化 |
| [stop_ghost](#stop_ghost) | 关闭残影 |
| [set_ghost_color](#set_ghost_color) | 设置残影颜色 |
| [set_afterimage_time](#set_afterimage_time) | 设置残影时间 |
| [set_icon](#set_icon) | 设置单位头像 |
| [set_blood_bar_type](#set_blood_bar_type) | 设置血条样式 |
| [set_blood_bar_text](#set_blood_bar_text) | 设置血条文本 |
| [set_billboard_progress](#set_billboard_progress) | 设置血条进度 |
| [set_health_bar_display](#set_health_bar_display) | 设置血条显示方式 |
| [set_minimap_icon](#set_minimap_icon) | ***************敌我合并一条 |
| [set_enemy_minimap_icon](#set_enemy_minimap_icon) | 设置敌方单位小地图头像 |
| [set_select_effect_visible](#set_select_effect_visible) | 设置单位选择框的可见性 |
| [set_scale](#set_scale) | 设置模型缩放 |
| [set_unit_scale](#set_unit_scale) | 设置单位三轴缩放 |
| [set_outline_visible](#set_outline_visible) | 设置单位描边开启 |
| [set_outlined_color](#set_outlined_color) | 设置单位描边颜色 |
| [set_turning_speed](#set_turning_speed) | 设置转身速度 |
| [replace_model](#replace_model) | 替换模型 |
| [cancel_replace_model](#cancel_replace_model) | 取消模型替换 |
| [set_transparent_when_invisible](#set_transparent_when_invisible) | **********************这是啥 |
| [set_recycle_on_remove](#set_recycle_on_remove) | 设置尸体消失后是否回收 |
| [set_Xray_is_open](#set_Xray_is_open) | 设置透视状态 |
| [add_tech](#add_tech) | 单位添加科技 |
| [remove_tech](#remove_tech) | 单位删除科技 |
| [research_tech](#research_tech) | 研究科技 |
| [get_tech_list](#get_tech_list) | 获取单位可研究的所有科技 |
| [get_affect_techs](#get_affect_techs) | 获取单位受到影响的所有科技 |
| [set_day_vision](#set_day_vision) | 设置白天的视野范围 |
| [set_night_value](#set_night_value) | 设置夜晚的视野范围 |
| [play_animation](#play_animation) | *******************播放动画全局统一 |
| [stop_animation](#stop_animation) | 停止动画 |
| [change_animation](#change_animation) | 替换动画 |
| [cancel_change_animation](#cancel_change_animation) | 取消动画替换 |
| [clear_change_animation](#clear_change_animation) | 重置动画替换 |
| [stop_cur_animation](#stop_cur_animation) | 停止当前正在播放的动画 |
| [set_animation_speed](#set_animation_speed) | 设置动画播放速率 |
| [set_base_speed](#set_base_speed) | 设置走路动画基准速度 |
| [add_goods](#add_goods) | 添加可贩卖的商品 |
| [remove_goods](#remove_goods) | 移除可贩卖的商品 |
| [set_goods_stack](#set_goods_stack) | 设置商品库存 |
| [sell](#sell) | 单位向商店出售物品 |
| [buy](#buy) | 从商店购买商品 |
| [add_buff](#add_buff) | 给单位添加魔法效果 |
| [remove_buffs_by_key](#remove_buffs_by_key) | 单位移除所有指定id的魔法效果 |
| [remove_buffs_by_effect_type](#remove_buffs_by_effect_type) | 单位移除所有指定类型的魔法效果 |
| [find_buff](#find_buff) | 获取单位指定id的魔法效果 |
| [get_goods_cd](#get_goods_cd) | 获取商店商品的库存间隔 |
| [get_goods_remaining_cd](#get_goods_remaining_cd) | 获取商店商品的剩余恢复时间 |
| [get_shop_item_list](#get_shop_item_list) | 获取所有的商店物品 |
| [get_hp](#get_hp) | 获取当前生命值 |
| [get_mp](#get_mp) | 获取当前魔法值 |
| [get_final_attr](#get_final_attr) | 获取最终属性 |
| [get_attr_other](#get_attr_other) | 获取属性（额外） |
| [get_attr_base](#get_attr_base) | 获取单属性（基础） |
| [get_attr_base_ratio](#get_attr_base_ratio) | 获取属性（基础加成） |
| [get_attr_bonus](#get_attr_bonus) | 获取属性（增益） |
| [get_attr_all_ratio](#get_attr_all_ratio) | 获取属性（最终加成） |
| [get_attr_bonus_ratio](#get_attr_bonus_ratio) | 获取属性（增益加成） |
| [get_attr](#get_attr) | 获取属性（默认为实际属性） |
| [get_attr_growth_by_key](#get_attr_growth_by_key) | 获取单位属性成长 |
| [get_life_cycle](#get_life_cycle) | 获取单位剩余生命周期 |
| [get_height](#get_height) | 获取单位飞行高度 |
| [get_turning_speed](#get_turning_speed) | 获取单位转身速度 |
| [get_alert_range](#get_alert_range) | 获取单位警戒范围 |
| [get_cancel_alert_range](#get_cancel_alert_range) | 获取单位取消警戒的范围 |
| [get_collision_radius](#get_collision_radius) | 获取单位碰撞半径 |
| [get_owner](#get_owner) | 获取单位所属玩家 |
| [get_unit_resource_cost](#get_unit_resource_cost) | 获取建造此单位消耗的资源（玩家属性） |
| [get_reward_res](#get_reward_res) | 获取击杀可获得的资源（玩家属性） |
| [get_scale](#get_scale) | 获取单位缩放 |
| [get_unit_selection_range_scale](#get_unit_selection_range_scale) | 获取单位选择圈缩放 |
| [get_x_scale](#get_x_scale) | 获取单位的X轴缩放 |
| [get_z_scale](#get_z_scale) | 获取单位的Z轴缩放 |
| [get_y_scale](#get_y_scale) | 获取单位的Y轴缩放 |
| [get_shop_range](#get_shop_range) | 获取商店的购买范围 |
| [get_level](#get_level) | 获取单位等级 |
| [get_type](#get_type) | 获取单位的单位类型ID |
| [get_key](#get_key) | 获取单位类型的ID |
| [get_exp](#get_exp) | 获取单位当前的经验值 |
| [get_upgrade_exp](#get_upgrade_exp) | 获取单位当前升级所需经验 |
| [get_ability_point](#get_ability_point) | 获取英雄的技能点数量 |
| [get_pkg_cnt](#get_pkg_cnt) | 获取单位背包栏的槽位数 |
| [get_bar_cnt](#get_bar_cnt) | 获取单位物品栏的槽位数 |
| [get_item_type_number_of_unit](#get_item_type_number_of_unit) | 获取单位拥有的物品类型数量 |
| [get_exp_reward](#get_exp_reward) | 获取单位被击杀经验 |
| [get_shield](#get_shield) | 获取单位指定护盾类型的护盾值 |
| [get_shop_tab_number](#get_shop_tab_number) | 获取商店页签数量 |
| [get_goods_stack](#get_goods_stack) | 获取商店的物品商品库存 |
| [get_name](#get_name) | 获取单位名称 |
| [get_description](#get_description) | 获取单位的描述 |
| [get_name_by_key](#get_name_by_key) | 获取单位类型名称 |
| [get_description_by_key](#get_description_by_key) | 获取单位类型的描述 |
| [get_shop_tab_name](#get_shop_tab_name) | 获取商店的页签名 |
| [get_subtype](#get_subtype) | 获取单位分类 |
| [is_hero](#is_hero) | 是否是英雄 |
| [get_icon](#get_icon) | 获取单位的头像 |
| [is_building](#is_building) | 是否是建筑 |
| [get_icon_by_key](#get_icon_by_key) | 获取单位类型的头像 |
| [get_last_created_unit](#get_last_created_unit) | 最后创建的单位 |
| [get_parent_unit](#get_parent_unit) | 获取单位的拥有者（单位） |
| [get_illusion_owner](#get_illusion_owner) | 获取幻象的召唤者 |
| [get_facing](#get_facing) | 获取单位的朝向 |
| [get_armor_type](#get_armor_type) | 获得护甲类型 |
| [get_attack_type](#get_attack_type) | 获得攻击类型 |
| [get_goods_key](#get_goods_key) | 获取商店的物品id |
| [get_model](#get_model) | 获取单位的当前模型 |
| [get_source_model](#get_source_model) | 获取单位的原本模型 |
| [get_point](#get_point) | 获取单位所在点 |
| [get_nearest_valid_point](#get_nearest_valid_point) | 获取单位最近的可通行点 |
| [get_team](#get_team) | 获取单位的队伍 |
| [has_tag](#has_tag) | 是否具有标签 |
| [is_alive](#is_alive) | 是否存活 |
| [can_visible](#can_visible) | 是否可见 |
| [is_moving](#is_moving) | 是否正在移动 |
| [is_in_radius](#is_in_radius) | 是否在另一个单位或点附近 |
| [is_shop](#is_shop) | 是否是商店 |
| [is_illusion](#is_illusion) | 是否是幻象单位 |
| [is_in_group](#is_in_group) | 是否在单位组中 |
| [is_in_battle](#is_in_battle) | 是否在战斗状态 |
| [has_ability_by_key](#has_ability_by_key) | 是否有指定id的技能 |
| [has_item](#has_item) | 是否有指定物品 |
| [has_item_by_key](#has_item_by_key) | 是否有指定类型的物品 |
| [has_buff_by_key](#has_buff_by_key) | 是否有指定id的魔法效果 |
| [has_buff_by_effect_type](#has_buff_by_effect_type) | 是否有指定类型的魔法效果 |
| [unit_has_modifier_tag](#unit_has_modifier_tag) | 是否有指定标签的魔法效果 |
| [check_precondition_by_key](#check_precondition_by_key) | 单位类型前置条件是否通过 |
| [is_ally](#is_ally) | 是否是友方 |
| [is_enemy](#is_enemy) | 是否是敌人 |
| [can_blink_to](#can_blink_to) | 能否传送到点 |
| [is_collided_with_point](#is_collided_with_point) | 是否与点碰撞 |
| [can_walk_to](#can_walk_to) | 是否寻路可达 |
| [has_move_collision](#has_move_collision) | 是否拥有指定碰撞类型 |
| [set_move_collision](#set_move_collision) | 设置单位是否计算某种碰撞类型 |
| [get_owner_player](#get_owner_player) | 获取所属玩家 |
| [player_shop_check](#player_shop_check) | 玩家是否可以购买商店的物品 |
| [get_model_by_key](#get_model_by_key) | 获取单位类型的模型 |
| [get_type_by_id](#get_type_by_id) | 获取单位类型的分类 |
| [attr_to_name](#attr_to_name) | 单位属性转单位属性名字 |
| [damage](#damage) |  |
| [get_main_attr](#get_main_attr) | 获取单位主属性(需要开启复合属性) |
| [set_move_channel_land](#set_move_channel_land) | 设置单位的移动类型为地面 |
| [set_move_channel_air](#set_move_channel_air) | 设置单位的移动类型为空中 |
| [get_camp_id](#get_camp_id) | 获取单位阵营ID |
| [change_model_texture](#change_model_texture) |  |
| [transformation](#transformation) | 变身 |
| [set_shadow_radius](#set_shadow_radius) | 设置单位内切圆半径(索敌、范围查找等使用) |
| [set_collision_radius](#set_collision_radius) | 设置单位占用格边长(影响寻路) |
| [is_destroyed](#is_destroyed) |  |

---

## get_by_handle

method in Unit

- 描述

    通过py层的单位实例获取lua层的单位实例

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | py_unit | py.Unit |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Unit? |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = y3.unit.get_by_handle(unit.handle)
```

---

## get_by_id

method in Unit

- 描述

    根据唯一ID获取单位。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | id | py.UnitID |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Unit? |  |

- 示例

```lua
local unit_id = 1

local result = y3.unit.get_by_id(unit_id)
```

---

## get_by_res_id

method in Unit

- 描述

    获取摆放在场景上的单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | res_id | integer |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Unit |  |

- 示例

```lua
local result = y3.unit.get_by_res_id(1)
```

---

## get_by_string

method in Unit

- 描述

    根据字符串获取单位，字符串是通过 `tostring(Unit)`

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | str | string |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Unit? |  |

- 示例

```lua
local result = y3.unit.get_by_string("str")
```

---

## is_exist

method in Unit

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

local result = unit:is_exist()
```

---

## get_id

method in Unit

- 描述

    获取唯一ID

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_id()
```

---

## remove_ability_by_key

method in Unit

- 描述

    移除技能(指定类型)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | type | y3.Const.AbilityType \| y3.Const.AbilityTypeAlias | 技能类型 |
    | ability_key | py.AbilityKey | 物编id |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability_key = 134274569

unit:remove_ability_by_key("type", ability_key)
```

---

## add_item

method in Unit

- 描述

    单位添加物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_id | py.ItemKey | 物品id |
    | slot_type? | y3.Const.ShiftSlotTypeAlias | 槽位类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Item? |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item_key = 134274569

local result = unit:add_item(item_key)
```

---

## remove_item

method in Unit

- 描述

    单位移除物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_id | py.ItemKey | 物品id |
    | num? | integer | 数量 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item_key = 134274569

unit:remove_item(item_key, 1)
```

---

## shift_item

method in Unit

- 描述

    移动物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item | Item | 物品 |
    | type | y3.Const.ShiftSlotTypeAlias |  |
    | index? | integer | 槽位 |
    | force? | boolean | 是否强制移动，`true`: 如果目标有物品，则移动到另一个空格中；`false`: 如果目标有物品，则要移动的物品会掉落 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

unit:shift_item(item, "type", 1, true)
```

---

## exchange_item

method in Unit

- 描述

    交换物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item | Item | 物品 |
    | type | y3.Const.ShiftSlotTypeAlias |  |
    | index | integer | 槽位 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

unit:exchange_item(item, "type", 1)
```

---

## get_abilities_by_type

method in Unit

- 描述

    获取指定类型的所有技能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | type | y3.Const.AbilityType |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Ability[] |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_abilities_by_type("type")
```

---

## get_buffs

method in Unit

- 描述

    获取单位身上的魔法效果

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Buff[] | 魔法效果表 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_buffs()
```

---

## switch_ability

method in Unit

- 描述

    交换技能位置

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_1 | Ability | 第一个技能 |
    | ability_2 | Ability | 第二个技能 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

unit:switch_ability(ability, ability)
```

---

## switch_ability_by_slot

method in Unit

- 描述

    根据坑位交换技能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | type_1 | y3.Const.AbilityType | 第一个技能类型 |
    | slot_1 | y3.Const.AbilityIndex | 第一个技能坑位 |
    | type_2 | y3.Const.AbilityType | 第二个技能类型 |
    | slot_2 | y3.Const.AbilityIndex | 第二个技能坑位 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:switch_ability_by_slot("type_1", "slot_1", "type_2", "slot_2")
```

---

## stop_all_abilities

method in Unit

- 描述

    停止所有技能

- 参数

    无

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:stop_all_abilities()
```

---

## add_ability

method in Unit

- 描述

    添加技能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | type | y3.Const.AbilityType \| y3.Const.AbilityTypeAlias | 技能类型 |
    | id | py.AbilityKey | 物编id |
    | slot? | y3.Const.AbilityIndex | 技能位 |
    | level? | integer | 等级 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Ability? |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability_key = 134274569

local result = unit:add_ability("type", ability_key, "slot", 1)
```

---

## remove_ability

method in Unit

- 描述

    移除技能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | type | y3.Const.AbilityType | 技能类型 |
    | slot | y3.Const.AbilityIndex | 技能位 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:remove_ability("type", "slot")
```

---

## find_ability

method in Unit

- 描述

    通过技能名寻找技能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | type | y3.Const.AbilityType \| y3.Const.AbilityTypeAlias | 技能类型 |
    | id | py.AbilityKey | 物编id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Ability? | 技能 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability_key = 134274569

local result = unit:find_ability("type", ability_key)
```

---

## get_ability_by_slot

method in Unit

- 描述

    获得某个技能位的的技能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | type | y3.Const.AbilityType \| y3.Const.AbilityTypeAlias | 技能类型 |
    | slot | integer | 技能位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Ability? | 技能 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_ability_by_slot("type", 1)
```

---

## get_ability_by_seq

method in Unit

- 描述

    根据技能序号获取技能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | seq | py.AbilitySeq |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Ability? |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_ability_by_seq("seq")
```

---

## get_common_attack

method in Unit

- 描述

    comment 获取普攻技能

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Ability? |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_common_attack()
```

---

## get_item_by_slot

method in Unit

- 描述

    获取单位背包槽位上的物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | type | y3.Const.SlotType \| y3.Const.ShiftSlotTypeAlias | 槽位类型 |
    | slot | integer | 位置 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Item? | 物品 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local slot_type = y3.const.SlotType['NOT_IN_BAG']

local result = unit:get_item_by_slot(slot_type, 1)
```

---

## get_all_items

method in Unit

- 描述

    单位的所有物品

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | ItemGroup | 所有物品 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_all_items()
```

---

## unit_gains_tech

method in Unit

- 描述

    单位获得科技

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技类型 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local tech_key = 134274569

unit:unit_gains_tech(tech_key)
```

---

## create_unit

method in Unit

- 描述

    创建单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | owner | Player\|Unit |  |
    | unit_id | py.UnitKey | 单位类型 |
    | point | Point | 点 |
    | direction | number | 方向 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Unit |  |

- 示例

```lua
local point = y3.point(0, 0)
local player = y3.player.get_by_id(1)
local unit_key = 134274569

local result = y3.unit.create_unit(owner, unit_key, point, 1.0)
```

---

## kill_by

method in Unit

- 描述

    杀死单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | killer? | Unit | 凶手单位 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:kill_by()
```

---

## is_casting

method in Unit

- 描述

    单位是否有正在释放的技能

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:is_casting()
```

---

## get_casting_ability

method in Unit

- 描述

    获取正在释放的技能

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Ability? |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_casting_ability()
```

---

## create_illusion

method in Unit

- 描述

    创建幻象

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | illusion_unit | Unit | 幻象复制的单位 |
    | call_unit | Unit | 召唤单位 |
    | player | Player | 玩家 |
    | point | Point | 点 |
    | direction | number | 方向 |
    | clone_hp_mp | boolean | 复制当前的生命值和魔法值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Unit? |  |

- 示例

```lua
local point = y3.point(0, 0)
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

local result = y3.unit.create_illusion(unit, unit, player, point, 1.0, true)
```

---

## remove

method in Unit

- 描述

    删除单位

- 参数

    无

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:remove()
```

---

## blink

method in Unit

- 描述

    传送到点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | Point | 点 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local point = y3.point(0, 0)

unit:blink(point)
```

---

## set_point

method in Unit

- 描述

    强制传送到点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | Point | 点 |
    | isSmooth | boolean | 是否丝滑 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local point = y3.point(0, 0)

unit:set_point(point, true)
```

---

## reborn

method in Unit

- 描述

    复活单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point? | Point | 点 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:reborn()
```

---

## heals

method in Unit

- 描述

    造成治疗

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | number | 治疗值 |
    | skill? | Ability | 技能 |
    | source_unit? | Unit | 单位 |
    | text_type? | string | 跳字类型 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:heals(1.0, ability, unit, "text_type")
```

---

## add_tag

method in Unit

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

unit:add_tag("tag")
```

---

## remove_tag

method in Unit

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

unit:remove_tag("tag")
```

---

## add_state

method in Unit

- 描述

    添加状态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | state_enum | integer\|y3.Const.UnitEnumState | 状态名 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:add_state(1)
```

---

## remove_state

method in Unit

- 描述

    移除状态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | state_enum | integer\|y3.Const.UnitEnumState | 状态名 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:remove_state(1)
```

---

## add_multi_state

method in Unit

- 描述

    添加多个状态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | state_enum | integer | 状态 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:add_multi_state(1)
```

---

## remove_multi_state

method in Unit

- 描述

    移除多个状态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | state_enum | integer | 状态 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:remove_multi_state(1)
```

---

## has_state

method in Unit

- 描述

    是否有某个状态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | state_enum | integer\|y3.Const.UnitEnumState | 状态名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:has_state(1)
```

---

## add_state_gc

method in Unit

- 描述

    添加状态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | state_enum | integer\|y3.Const.UnitEnumState | 状态名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | GCNode |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:add_state_gc(1)
```

---

## learn

method in Unit

- 描述

    学习技能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能id |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability_key = 134274569

unit:learn(ability_key)
```

---

## command

method in Unit

- 描述

    发布命令

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | command | py.UnitCommand | 命令 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local unit_command = unit.handle:api_release_command_stop()

unit:command(unit_command.handle)
```

---

## move_to_pos

method in Unit

- 描述

    命令移动

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | Point | 点 |
    | range? | number | 范围 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommand | 命令 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local point = y3.point(0, 0)

local result = unit:move_to_pos(point, 1.0)
```

---

## stop

method in Unit

- 描述

    命令停止

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommand | 命令 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:stop()
```

---

## hold

method in Unit

- 描述

    命令驻守

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | Point | 点 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommand | 命令 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local point = y3.point(0, 0)

local result = unit:hold(point)
```

---

## attack_move

method in Unit

- 描述

    命令攻击移动

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | Point | 点 |
    | range? | number | 范围 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommand | 命令 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local point = y3.point(0, 0)

local result = unit:attack_move(point, 1.0)
```

---

## attack_target

method in Unit

- 描述

    命令攻击目标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | target | Unit | 目标 |
    | range | number | 范围 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommand | 命令 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:attack_target(unit, 1.0)
```

---

## move_along_road

method in Unit

- 描述

    命令沿路径移动

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | road | Road | 路径 |
    | patrol_mode | y3.Const.RoadPatrolType | 移动模式 |
    | can_attack | boolean | 是否自动攻击 |
    | start_from_nearest | boolean | 就近选择起始点 |
    | back_to_nearest | boolean | 偏离后就近返回 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommand | 命令 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:move_along_road("road", "patrol_mode", true, true, true)
```

---

## cast

method in Unit

- 描述

    命令发动技能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability | Ability | 技能 |
    | target? | Point\|Unit\|Item\|Destructible | 目标 |
    | extra_target? | Point | 额外目标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommand |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = unit:cast(ability)
```

---

## pick_item

method in Unit

- 描述

    命令拾取物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item | Item |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommand |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = unit:pick_item(item)
```

---

## drop_item

method in Unit

- 描述

    命令丢弃物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item | Item |  |
    | point | Point |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommand |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local point = y3.point(0, 0)
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = unit:drop_item(item, point)
```

---

## give_item

method in Unit

- 描述

    命令给予物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item | Item |  |
    | target | Unit |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommand |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = unit:give_item(item, unit)
```

---

## use_item

method in Unit

- 描述

    命令使用物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item | Item |  |
    | target? | Point\|Unit\|Item\|Destructible |  |
    | extra_target? | Point |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommand |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = unit:use_item(item)
```

---

## follow

method in Unit

- 描述

    命令跟随单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | target | Unit |  |
    | refresh_interval? | number | 刷新间隔 |
    | near_offset? | number | 跟随距离 |
    | far_offset? | number | 重新跟随距离 |
    | follow_angle? | number | 跟随角度 |
    | follow_dead_target? | boolean | 是否跟随死亡单位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommand |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:follow(unit, 1.0, 1.0, 1.0, 1.0, true)
```

---

## set_facing

method in Unit

- 描述

    设置朝向

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | direction | number | 朝向 |
    | turn_time | number | 转向时间 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:set_facing(1.0, 1.0)
```

---

## set_name

method in Unit

- 描述

    设置名称

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | name | string | 名称 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:set_name("name")
```

---

## set_name_show_type

method in Unit

- 描述

    设置名称显示方式

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | show_type | y3.Const.BarNameShowType | 名称显示方式 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:set_name_show_type("show_type")
```

---

## set_description

method in Unit

- 描述

    设置描述

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | description | string | 描述 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:set_description("description")
```

---

## set_attr

method in Unit

- 描述

    设置属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr_name | string \| y3.Const.UnitAttr | 属性名 |
    | value | number | 属性值 |
    | attr_type? | string \| y3.Const.UnitAttrType | 属性类型，默认为“基础” |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:set_attr("attr_name", 1.0, "attr_type")
```

---

## add_attr

method in Unit

- 描述

    增加属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr_name | string \| y3.Const.UnitAttr | 属性名 |
    | value | number | 属性值 |
    | attr_type? | string \| y3.Const.UnitAttrType | 属性类型，默认为“增益” |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:add_attr("attr_name", 1.0, "attr_type")
```

---

## add_attr_gc

method in Unit

- 描述

    增加属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr_name | string \| y3.Const.UnitAttr | 属性名 |
    | value | number | 属性值 |
    | attr_type | string \| y3.Const.UnitAttrType | 属性类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | GCNode |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:add_attr_gc("attr_name", 1.0, "attr_type")
```

---

## set_level

method in Unit

- 描述

    设置等级

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | level | integer | 等级 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:set_level(1)
```

---

## add_level

method in Unit

- 描述

    增加等级

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | level | integer | 等级 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:add_level(1)
```

---

## set_exp

method in Unit

- 描述

    设置经验

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | exp | number | 经验 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:set_exp(1.0)
```

---

## add_exp

method in Unit

- 描述

    增加经验值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | exp | number | 经验 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:add_exp(1.0)
```

---

## set_hp

method in Unit

- 描述

    设置当前生命值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | hp | number | 当前生命值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:set_hp(1.0)
```

---

## add_hp

method in Unit

- 描述

    增加当前生命值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | hp | number | 当前生命值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:add_hp(1.0)
```

---

## set_mp

method in Unit

- 描述

    设置当前魔法值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | mp | number | 当前魔法值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:set_mp(1.0)
```

---

## add_mp

method in Unit

- 描述

    增加当前魔法值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | mp | number | 当前魔法值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:add_mp(1.0)
```

---

## set_ability_point

method in Unit

- 描述

    设置技能点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | skill_point | integer | 技能点 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:set_ability_point(1)
```

---

## add_ability_point

method in Unit

- 描述

    增加技能点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | skill_point | integer | 技能点 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:add_ability_point(1)
```

---

## change_owner

method in Unit

- 描述

    改变所属玩家

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 所属玩家 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

unit:change_owner(player)
```

---

## set_height

method in Unit

- 描述

    设置飞行高度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | height | number | 高度 |
    | trans_time | number | 过渡时间 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:set_height(1.0, 1.0)
```

---

## set_life_cycle

method in Unit

- 描述

    设置生命周期

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | time | number | 生命周期 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:set_life_cycle(1.0)
```

---

## pause_life_cycle

method in Unit

- 描述

    设置生命周期暂停状态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_stop | boolean | 生命周期暂停状态 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:pause_life_cycle(true)
```

---

## set_alert_range

method in Unit

- 描述

    设置警戒范围

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | range | number | 范围 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:set_alert_range(1.0)
```

---

## set_cancel_alert_range

method in Unit

- 描述

    设置取消警戒范围

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | range | number | 取消警戒范围 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:set_cancel_alert_range(1.0)
```

---

## set_pkg_cnt

method in Unit

- 描述

    设置背包栏的槽位数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | number | integer | 槽位数 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:set_pkg_cnt(1)
```

---

## set_bar_cnt

method in Unit

- 描述

    设置物品栏的槽位数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | number | integer | 槽位数 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:set_bar_cnt(1)
```

---

## set_behavior

method in Unit

- 描述

    设置默认单位行为

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | behavior | py.UnitBehavior | 单位行为 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local unit_behavior = "unit_behavior"

unit:set_behavior(unit_behavior)
```

---

## set_attr_growth

method in Unit

- 描述

    ******************************************

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位id |
    | attr_name | string | 属性名 |
    | value | number | 属性成长 |

- 返回值

    无

- 示例

```lua
local unit_key = 134274569

y3.unit.set_attr_growth(unit_key, "attr_name", 1.0)
```

---

## set_reward_exp

method in Unit

- 描述

    设置被击杀的经验值奖励

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | exp | number | 经验 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:set_reward_exp(1.0)
```

---

## set_reward_res

method in Unit

- 描述

    设置被击杀的玩家属性奖励

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player_attr_name | py.RoleResKey | 属性名 |
    | value | number | 属性奖励 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local role_res_key = "res_key"

unit:set_reward_res(role_res_key, 1.0)
```

---

## set_attack_type

method in Unit

- 描述

    设置攻击类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attack_type | integer | 攻击类型 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:set_attack_type(1)
```

---

## set_armor_type

method in Unit

- 描述

    设置护甲类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | armor_type | integer | 护甲类型 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:set_armor_type(1)
```

---

## start_ghost

method in Unit

- 描述

    ************************残影优化

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | red | number | 红 |
    | green | number | 绿 |
    | blue | number | 蓝 |
    | alpha | number | 透明度 |
    | interval | number | 间隔时间 |
    | duration | number | 显示时间 |
    | start_time | number | 开始时间 |
    | end_time | number | 结束时间 |
    | is_origin_martial | boolean | 使用原生材质 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:start_ghost(1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, true)
```

---

## stop_ghost

method in Unit

- 描述

    关闭残影

- 参数

    无

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:stop_ghost()
```

---

## set_ghost_color

method in Unit

- 描述

    设置残影颜色

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | red | number | 绿 |
    | green | number | 绿 |
    | blue | number | 蓝 |
    | alpha | number | 透明度 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:set_ghost_color(1.0, 1.0, 1.0, 1.0)
```

---

## set_afterimage_time

method in Unit

- 描述

    设置残影时间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | interval | number | 间隔时间 |
    | duration | number | 显示时间 |
    | start_time | number | 开始时间 |
    | end_time | number | 结束时间 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:set_afterimage_time(1.0, 1.0, 1.0, 1.0)
```

---

## set_icon

method in Unit

- 描述

    设置单位头像

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | img_id | py.Texture | 单位头像 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local texture = 1

unit:set_icon(texture)
```

---

## set_blood_bar_type

method in Unit

- 描述

    设置血条样式

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | bar_type | integer \| y3.Const.BloodBarType | 血条样式 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:set_blood_bar_type(1)
```

---

## set_blood_bar_text

method in Unit

- 描述

    设置血条文本

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | node_name | string | 血条命名 |
    | text | string | 文本 |
    | role? | Player | 可见玩家 |
    | font? | string | 字体 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:set_blood_bar_text("node_name", "text", player, "font")
```

---

## set_billboard_progress

method in Unit

- 描述

    设置血条进度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | node_name | string | 血条命名 |
    | progress | number | 进度 |
    | role? | Player | 可见玩家 |
    | transition_time? | number | 过渡时间 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:set_billboard_progress("node_name", 1.0, player, 1.0)
```

---

## set_health_bar_display

method in Unit

- 描述

    设置血条显示方式

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | bar_show_type | integer | 血条显示方式 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:set_health_bar_display(1)
```

---

## set_minimap_icon

method in Unit

- 描述

    ***************敌我合并一条

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | img_id | py.Texture | 单位小地图头像 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local texture = 1

unit:set_minimap_icon(texture)
```

---

## set_enemy_minimap_icon

method in Unit

- 描述

    设置敌方单位小地图头像

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | img_id | py.Texture | 敌方单位小地图头像 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local texture = 1

unit:set_enemy_minimap_icon(texture)
```

---

## set_select_effect_visible

method in Unit

- 描述

    设置单位选择框的可见性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | bool | boolean | 布尔值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:set_select_effect_visible(true)
```

---

## set_scale

method in Unit

- 描述

    设置模型缩放

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | scale | number | 模型缩放 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:set_scale(1.0)
```

---

## set_unit_scale

method in Unit

- 描述

    设置单位三轴缩放

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | sx | number | X轴缩放 |
    | sy | number | Y轴缩放 |
    | sz | number | Z轴缩放 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:set_unit_scale(1.0, 1.0, 1.0)
```

---

## set_outline_visible

method in Unit

- 描述

    设置单位描边开启

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | bool | boolean | 布尔值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:set_outline_visible(true)
```

---

## set_outlined_color

method in Unit

- 描述

    设置单位描边颜色

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | color_r | number | R |
    | color_g | number | G |
    | color_b | number | B |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:set_outlined_color(1.0, 1.0, 1.0)
```

---

## set_turning_speed

method in Unit

- 描述

    设置转身速度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | speed | number | 转身速度 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:set_turning_speed(1.0)
```

---

## replace_model

method in Unit

- 描述

    替换模型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | model_id | py.ModelKey | 模型id |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local model_key = 1

unit:replace_model(model_key)
```

---

## cancel_replace_model

method in Unit

- 描述

    取消模型替换

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | model_id | py.ModelKey | 模型id |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local model_key = 1

unit:cancel_replace_model(model_key)
```

---

## set_transparent_when_invisible

method in Unit

- 描述

    **********************这是啥

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_visible | boolean | 是否半透明 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:set_transparent_when_invisible(true)
```

---

## set_recycle_on_remove

method in Unit

- 描述

    设置尸体消失后是否回收

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_recycle | boolean | 是否回收 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:set_recycle_on_remove(true)
```

---

## set_Xray_is_open

method in Unit

- 描述

    设置透视状态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_open | boolean | 是否透视 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:set_Xray_is_open(true)
```

---

## add_tech

method in Unit

- 描述

    单位添加科技

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_id | py.TechKey | 科技id |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local tech_key = 134274569

unit:add_tech(tech_key)
```

---

## remove_tech

method in Unit

- 描述

    单位删除科技

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_id | py.TechKey | 科技id |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local tech_key = 134274569

unit:remove_tech(tech_key)
```

---

## research_tech

method in Unit

- 描述

    研究科技

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_id | py.TechKey | 科技id |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local tech_key = 134274569

unit:research_tech(tech_key)
```

---

## get_tech_list

method in Unit

- 描述

    获取单位可研究的所有科技

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.TechKey[] |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_tech_list()
```

---

## get_affect_techs

method in Unit

- 描述

    获取单位受到影响的所有科技

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.TechKey[] |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_affect_techs()
```

---

## set_day_vision

method in Unit

- 描述

    设置白天的视野范围

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | number |  |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:set_day_vision(1.0)
```

---

## set_night_value

method in Unit

- 描述

    设置夜晚的视野范围

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | number |  |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:set_night_value(1.0)
```

---

## play_animation

method in Unit

- 描述

    *******************播放动画全局统一

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | anim_name | string | 动画名 |
    | speed? | number | 速度 |
    | start_time? | number | 开始时间 |
    | end_time? | number | 结束时间(默认-1表示播到最后) |
    | is_loop? | boolean | 是否循环 |
    | is_back_normal? | boolean | 是否返回默认状态 |
    | transition_time? | number | 过度时间 |
    | force_play? | boolean | 即使死了也播播 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:play_animation("anim_name", 1.0, 1.0, 1.0, true, true, 1.0, true)
```

---

## stop_animation

method in Unit

- 描述

    停止动画

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | anim_name | string | 动画名 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:stop_animation("anim_name")
```

---

## change_animation

method in Unit

- 描述

    替换动画

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | replace_anim_name | string | 动画名 |
    | bereplace_anim_name | string | 动画名 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:change_animation("replace_anim_name", "bereplace_anim_name")
```

---

## cancel_change_animation

method in Unit

- 描述

    取消动画替换

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | replace_anim_name | string | 动画名 |
    | bereplace_anim_name | string | 动画名 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:cancel_change_animation("replace_anim_name", "bereplace_anim_name")
```

---

## clear_change_animation

method in Unit

- 描述

    重置动画替换

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | anim_name | string | 动画名 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:clear_change_animation("anim_name")
```

---

## stop_cur_animation

method in Unit

- 描述

    停止当前正在播放的动画

- 参数

    无

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:stop_cur_animation()
```

---

## set_animation_speed

method in Unit

- 描述

    设置动画播放速率

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | speed | number | 速度 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:set_animation_speed(1.0)
```

---

## set_base_speed

method in Unit

- 描述

    设置走路动画基准速度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | speed | number | 速度 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:set_base_speed(1.0)
```

---

## add_goods

method in Unit

- 描述

    添加可贩卖的商品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag_name | py.TabName | 标签名 |
    | item_key | py.ItemKey | 物品id |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item_key = 134274569

unit:add_goods("tag_name", item_key)
```

---

## remove_goods

method in Unit

- 描述

    移除可贩卖的商品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_name | py.TabName | 物品名 |
    | item_key | py.ItemKey | 物品id |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item_key = 134274569

unit:remove_goods("item_name", item_key)
```

---

## set_goods_stack

method in Unit

- 描述

    设置商品库存

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag_name | py.TabName | 标签名 |
    | item_key | py.ItemKey | 物品id |
    | number | integer | 物品库存 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item_key = 134274569

unit:set_goods_stack("tag_name", item_key, 1)
```

---

## sell

method in Unit

- 描述

    单位向商店出售物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 单位 |
    | item | Item | 物品 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

unit:sell(unit, item)
```

---

## buy

method in Unit

- 描述

    从商店购买商品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 单位 |
    | tag_num | py.TabIdx | 页签id |
    | item_key | py.ItemKey | 物品id |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item_key = 134274569

unit:buy(unit, 134274569, item_key)
```

---

## add_buff

method in Unit

- 描述

    给单位添加魔法效果

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | data | Buff.AddData |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Buff? |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:add_buff("data")
```

---

## remove_buffs_by_key

method in Unit

- 描述

    单位移除所有指定id的魔法效果

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | buff_key | py.ModifierKey | 影响类型的魔法效果 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier_key = 134274569

unit:remove_buffs_by_key(modifier_key)
```

---

## remove_buffs_by_effect_type

method in Unit

- 描述

    单位移除所有指定类型的魔法效果

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | effect_type | y3.Const.EffectType | 影响类型的魔法效果 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:remove_buffs_by_effect_type("effect_type")
```

---

## find_buff

method in Unit

- 描述

    获取单位指定id的魔法效果

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | buff_key | py.ModifierKey | 魔法效果id |
    | index? | integer | 第几个 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Buff? | 单位指定类型的魔法效果 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier_key = 134274569

local result = unit:find_buff(modifier_key, 1)
```

---

## get_goods_cd

method in Unit

- 描述

    获取商店商品的库存间隔

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | page | py.TabIdx | 页签id |
    | index | integer | 序号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 默认间隔时间 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_goods_cd(134274569, 1)
```

---

## get_goods_remaining_cd

method in Unit

- 描述

    获取商店商品的剩余恢复时间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | page | py.TabIdx | 页签id |
    | index | integer | 序号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 剩余恢复时间 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_goods_remaining_cd(134274569, 1)
```

---

## get_shop_item_list

method in Unit

- 描述

    获取所有的商店物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | page | py.TabIdx | 页签 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemKey[] |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_shop_item_list(134274569)
```

---

## get_hp

method in Unit

- 描述

    获取当前生命值

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 当前生命值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_hp()
```

---

## get_mp

method in Unit

- 描述

    获取当前魔法值

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 当前魔法值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_mp()
```

---

## get_final_attr

method in Unit

- 描述

    获取最终属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr_name | string \| y3.Const.UnitAttr | 属性名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_final_attr("attr_name")
```

---

## get_attr_other

method in Unit

- 描述

    获取属性（额外）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr_name | string \| y3.Const.UnitAttr | 属性名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_attr_other("attr_name")
```

---

## get_attr_base

method in Unit

- 描述

    获取单属性（基础）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr_name | string \| y3.Const.UnitAttr |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 单位基础属性类型的属性 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_attr_base("attr_name")
```

---

## get_attr_base_ratio

method in Unit

- 描述

    获取属性（基础加成）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr_name | string \| y3.Const.UnitAttr |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_attr_base_ratio("attr_name")
```

---

## get_attr_bonus

method in Unit

- 描述

    获取属性（增益）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr_name | string \| y3.Const.UnitAttr |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_attr_bonus("attr_name")
```

---

## get_attr_all_ratio

method in Unit

- 描述

    获取属性（最终加成）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr_name | string \| y3.Const.UnitAttr |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_attr_all_ratio("attr_name")
```

---

## get_attr_bonus_ratio

method in Unit

- 描述

    获取属性（增益加成）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr_name | string \| y3.Const.UnitAttr |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_attr_bonus_ratio("attr_name")
```

---

## get_attr

method in Unit

- 描述

    获取属性（默认为实际属性）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr_name | y3.Const.UnitAttr |  |
    | attr_type? | '实际' \| '额外' \| y3.Const.UnitAttrType |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_attr("attr_name")
```

---

## get_attr_growth_by_key

method in Unit

- 描述

    获取单位属性成长

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey |  |
    | attr_name | string \| y3.Const.UnitAttr |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 单位属性成长 |

- 示例

```lua
local unit_key = 134274569

local result = y3.unit.get_attr_growth_by_key(unit_key, "attr_name")
```

---

## get_life_cycle

method in Unit

- 描述

    获取单位剩余生命周期

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_life_cycle()
```

---

## get_height

method in Unit

- 描述

    获取单位飞行高度

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 单位飞行高度 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_height()
```

---

## get_turning_speed

method in Unit

- 描述

    获取单位转身速度

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 单位转身速度 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_turning_speed()
```

---

## get_alert_range

method in Unit

- 描述

    获取单位警戒范围

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 单位警戒范围 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_alert_range()
```

---

## get_cancel_alert_range

method in Unit

- 描述

    获取单位取消警戒的范围

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 单位取消警戒的范围 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_cancel_alert_range()
```

---

## get_collision_radius

method in Unit

- 描述

    获取单位碰撞半径

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 单位碰撞半径 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_collision_radius()
```

---

## get_owner

method in Unit

- 描述

    获取单位所属玩家

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Player | 单位所属玩家 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_owner()
```

---

## get_unit_resource_cost

method in Unit

- 描述

    获取建造此单位消耗的资源（玩家属性）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_id | py.UnitKey | 单位类型 |
    | player_attr_name | py.RoleResKey | 玩家属性名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 单位被击杀玩家属性 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local unit_key = 134274569
local role_res_key = "res_key"

local result = unit:get_unit_resource_cost(unit_key, role_res_key)
```

---

## get_reward_res

method in Unit

- 描述

    获取击杀可获得的资源（玩家属性）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player_attr_name | py.RoleResKey | 玩家属性名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 单位被击杀玩家属性 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local role_res_key = "res_key"

local result = unit:get_reward_res(role_res_key)
```

---

## get_scale

method in Unit

- 描述

    获取单位缩放

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 单位缩放 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_scale()
```

---

## get_unit_selection_range_scale

method in Unit

- 描述

    获取单位选择圈缩放

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 选择圈缩放 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_unit_selection_range_scale()
```

---

## get_x_scale

method in Unit

- 描述

    获取单位的X轴缩放

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | X轴缩放 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_x_scale()
```

---

## get_z_scale

method in Unit

- 描述

    获取单位的Z轴缩放

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | Z轴缩放 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_z_scale()
```

---

## get_y_scale

method in Unit

- 描述

    获取单位的Y轴缩放

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | Y轴缩放 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_y_scale()
```

---

## get_shop_range

method in Unit

- 描述

    获取商店的购买范围

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 购买范围 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_shop_range()
```

---

## get_level

method in Unit

- 描述

    获取单位等级

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 单位等级 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_level()
```

---

## get_type

method in Unit

- 描述

    获取单位的单位类型ID

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitType | 单位类型ID |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_type()
```

---

## get_key

method in Unit

- 描述

    获取单位类型的ID

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitKey | 单位类型的ID |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_key()
```

---

## get_exp

method in Unit

- 描述

    获取单位当前的经验值

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 单位当前的经验值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_exp()
```

---

## get_upgrade_exp

method in Unit

- 描述

    获取单位当前升级所需经验

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 单位当前升级所需经验 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_upgrade_exp()
```

---

## get_ability_point

method in Unit

- 描述

    获取英雄的技能点数量

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 英雄的技能点数量 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_ability_point()
```

---

## get_pkg_cnt

method in Unit

- 描述

    获取单位背包栏的槽位数

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 单位背包栏的槽位数 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_pkg_cnt()
```

---

## get_bar_cnt

method in Unit

- 描述

    获取单位物品栏的槽位数

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 单位物品栏的槽位数 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_bar_cnt()
```

---

## get_item_type_number_of_unit

method in Unit

- 描述

    获取单位拥有的物品类型数量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品类型id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 物品类型数量 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item_key = 134274569

local result = unit:get_item_type_number_of_unit(item_key)
```

---

## get_exp_reward

method in Unit

- 描述

    获取单位被击杀经验

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 单位被击杀经验 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_exp_reward()
```

---

## get_shield

method in Unit

- 描述

    获取单位指定护盾类型的护盾值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | shield_type | integer | 护盾类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 护盾类型的护盾值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_shield(1)
```

---

## get_shop_tab_number

method in Unit

- 描述

    获取商店页签数量

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 页签数量 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_shop_tab_number()
```

---

## get_goods_stack

method in Unit

- 描述

    获取商店的物品商品库存

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag_index | py.TabIdx | 页签 |
    | item_key | py.ItemKey | 物品类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 商品库存 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item_key = 134274569

local result = unit:get_goods_stack(134274569, item_key)
```

---

## get_name

method in Unit

- 描述

    获取单位名称

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 单位名称 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_name()
```

---

## get_description

method in Unit

- 描述

    获取单位的描述

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 单位的描述 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_description()
```

---

## get_name_by_key

method in Unit

- 描述

    获取单位类型名称

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 单位类型名称 |

- 示例

```lua
local unit_key = 134274569

local result = y3.unit.get_name_by_key(unit_key)
```

---

## get_description_by_key

method in Unit

- 描述

    获取单位类型的描述

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 单位类型的描述 |

- 示例

```lua
local unit_key = 134274569

local result = y3.unit.get_description_by_key(unit_key)
```

---

## get_shop_tab_name

method in Unit

- 描述

    获取商店的页签名

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag_index | py.TabIdx | 页签 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 页签名 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_shop_tab_name(134274569)
```

---

## get_subtype

method in Unit

- 描述

    获取单位分类

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitType | 单位分类 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_subtype()
```

---

## is_hero

method in Unit

- 描述

    是否是英雄

- 参数

    无

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:is_hero()
```

---

## get_icon

method in Unit

- 描述

    获取单位的头像

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Texture | 单位的头像 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_icon()
```

---

## is_building

method in Unit

- 描述

    是否是建筑

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:is_building()
```

---

## get_icon_by_key

method in Unit

- 描述

    获取单位类型的头像

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Texture | 单位类型的头像 |

- 示例

```lua
local unit_key = 134274569

local result = y3.unit.get_icon_by_key(unit_key)
```

---

## get_last_created_unit

method in Unit

- 描述

    最后创建的单位

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Unit? | 最后创建的单位 |

- 示例

```lua
local result = y3.unit.get_last_created_unit()
```

---

## get_parent_unit

method in Unit

- 描述

    获取单位的拥有者（单位）

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Unit? | 单位的拥有者 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_parent_unit()
```

---

## get_illusion_owner

method in Unit

- 描述

    获取幻象的召唤者

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Unit? | 幻象的召唤者 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_illusion_owner()
```

---

## get_facing

method in Unit

- 描述

    获取单位的朝向

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 单位的朝向 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_facing()
```

---

## get_armor_type

method in Unit

- 描述

    获得护甲类型

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 护甲类型 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_armor_type()
```

---

## get_attack_type

method in Unit

- 描述

    获得攻击类型

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 攻击类型 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_attack_type()
```

---

## get_goods_key

method in Unit

- 描述

    获取商店的物品id

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag_index | py.TabIdx | 页签 |
    | item_index | integer | 序号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemKey | 物品类型 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_goods_key(134274569, 1)
```

---

## get_model

method in Unit

- 描述

    获取单位的当前模型

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModelKey | 当前模型 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_model()
```

---

## get_source_model

method in Unit

- 描述

    获取单位的原本模型

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModelKey | 原本模型 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_source_model()
```

---

## get_point

method in Unit

- 描述

    获取单位所在点

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Point | 单位所在点 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_point()
```

---

## get_nearest_valid_point

method in Unit

- 描述

    获取单位最近的可通行点

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Point | 单位最近的可通行点 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_nearest_valid_point()
```

---

## get_team

method in Unit

- 描述

    获取单位的队伍

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Camp | 获取单位的队伍 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_team()
```

---

## has_tag

method in Unit

- 描述

    是否具有标签

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag_name | string | 标签 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 具有标签 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:has_tag("tag_name")
```

---

## is_alive

method in Unit

- 描述

    是否存活

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存活 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:is_alive()
```

---

## can_visible

method in Unit

- 描述

    是否可见

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | target_unit | Unit | 目标单位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 目标是否可见 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:can_visible(unit)
```

---

## is_moving

method in Unit

- 描述

    是否正在移动

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 正在移动 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:is_moving()
```

---

## is_in_radius

method in Unit

- 描述

    是否在另一个单位或点附近

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | other | Unit\|Point | 单位/点 |
    | range | number | 范围 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 在单位附近 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:is_in_radius(unit, 1.0)
```

---

## is_shop

method in Unit

- 描述

    是否是商店

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是商店 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:is_shop()
```

---

## is_illusion

method in Unit

- 描述

    是否是幻象单位

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是幻象单位 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:is_illusion()
```

---

## is_in_group

method in Unit

- 描述

    是否在单位组中

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | group | UnitGroup | 单位组 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 在单位组中 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ug = y3.unit_group.create()

local result = unit:is_in_group(ug)
```

---

## is_in_battle

method in Unit

- 描述

    是否在战斗状态

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 在战斗状态 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:is_in_battle()
```

---

## has_ability_by_key

method in Unit

- 描述

    是否有指定id的技能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 有指定类型的技能 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability_key = 134274569

local result = unit:has_ability_by_key(ability_key)
```

---

## has_item

method in Unit

- 描述

    是否有指定物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item | Item | 物品 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 有物品 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = unit:has_item(item)
```

---

## has_item_by_key

method in Unit

- 描述

    是否有指定类型的物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 有指定类型的物品 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item_key = 134274569

local result = unit:has_item_by_key(item_key)
```

---

## has_buff_by_key

method in Unit

- 描述

    是否有指定id的魔法效果

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | buff_key | py.ModifierKey | 魔法效果id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 有魔法效果 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier_key = 134274569

local result = unit:has_buff_by_key(modifier_key)
```

---

## has_buff_by_effect_type

method in Unit

- 描述

    是否有指定类型的魔法效果

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | effect_type | y3.Const.EffectType | 魔法效果类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 有指定类型的魔法效果 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:has_buff_by_effect_type("effect_type")
```

---

## unit_has_modifier_tag

method in Unit

- 描述

    是否有指定标签的魔法效果

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag_name | string | 标签 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 有指定标签的魔法效果 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:unit_has_modifier_tag("tag_name")
```

---

## check_precondition_by_key

method in Unit

- 描述

    单位类型前置条件是否通过

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | unit_key | py.UnitKey | 单位类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 单位类型前置条件是否通过 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local unit_key = 134274569

local result = y3.unit.check_precondition_by_key(player, unit_key)
```

---

## is_ally

method in Unit

- 描述

    是否是友方

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | target_unit | Unit | 目标单位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是敌对关系 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:is_ally(unit)
```

---

## is_enemy

method in Unit

- 描述

    是否是敌人

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | target_unit | Unit | 目标单位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是敌对关系 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:is_enemy(unit)
```

---

## can_blink_to

method in Unit

- 描述

    能否传送到点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | Point | 点 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 能否传送到点 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local point = y3.point(0, 0)

local result = unit:can_blink_to(point)
```

---

## is_collided_with_point

method in Unit

- 描述

    是否与点碰撞

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | Point | 点 |
    | range | number | 范围 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否与点碰撞 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local point = y3.point(0, 0)

local result = unit:is_collided_with_point(point, 1.0)
```

---

## can_walk_to

method in Unit

- 描述

    是否寻路可达

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | start_point | Point | 起始点 |
    | end_point | Point | 终点 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否寻路可达 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local point = y3.point(0, 0)

local result = unit:can_walk_to(point, point)
```

---

## has_move_collision

method in Unit

- 描述

    是否拥有指定碰撞类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | collision_layer | integer \| y3.Const.CollisionLayers | 碰撞类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否拥有指定碰撞类型 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:has_move_collision(1)
```

---

## set_move_collision

method in Unit

- 描述

    设置单位是否计算某种碰撞类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | collision_layer | integer \| y3.Const.CollisionLayers | 碰撞mask |
    | enable | boolean | 开启状态 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:set_move_collision(1, true)
```

---

## get_owner_player

method in Unit

- 描述

    获取所属玩家

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Player |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_owner_player()
```

---

## player_shop_check

method in Unit

- 描述

    玩家是否可以购买商店的物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

local result = unit:player_shop_check(player)
```

---

## get_model_by_key

method in Unit

- 描述

    获取单位类型的模型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModelKey | 模型 |

- 示例

```lua
local unit_key = 134274569

local result = y3.unit.get_model_by_key(unit_key)
```

---

## get_type_by_id

method in Unit

- 描述

    获取单位类型的分类

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer |  |

- 示例

```lua
local unit_key = 134274569

local result = y3.unit.get_type_by_id(unit_key)
```

---

## attr_to_name

method in Unit

- 描述

    单位属性转单位属性名字

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 属性key |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string |  |

- 示例

```lua
local result = y3.unit.attr_to_name("key")
```

---

## damage

method in Unit

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | data | Unit.DamageData |  |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:damage("data")
```

---

## get_main_attr

method in Unit

- 描述

    获取单位主属性(需要开启复合属性)

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_main_attr()
```

---

## set_move_channel_land

method in Unit

- 描述

    设置单位的移动类型为地面

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | land_limitation? | boolean | 陆地限制 |
    | item_limitation? | boolean | 物件限制 |
    | water_limitation? | boolean | 海洋限制 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:set_move_channel_land(true, true, true)
```

---

## set_move_channel_air

method in Unit

- 描述

    设置单位的移动类型为空中

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | air_limitation? | boolean | 空中限制 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:set_move_channel_air(true)
```

---

## get_camp_id

method in Unit

- 描述

    获取单位阵营ID

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CampID |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit:get_camp_id()
```

---

## change_model_texture

method in Unit

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | model | py.ModelKey | 目标模型编号 |
    | material | integer | 材质 id |
    | layer | integer | layer id |
    | texture | py.Texture | 贴图 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local model_key = 1
local texture = 1

unit:change_model_texture(model_key, 1, 1, texture)
```

---

## transformation

method in Unit

- 描述

    变身

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位类型key |
    | options? | Unit.TransformationOptions |  |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local unit_key = 134274569

unit:transformation(unit_key)
```

---

## set_shadow_radius

method in Unit

- 描述

    设置单位内切圆半径(索敌、范围查找等使用)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | radius | number | 半径 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:set_shadow_radius(1.0)
```

---

## set_collision_radius

method in Unit

- 描述

    设置单位占用格边长(影响寻路)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | radius | number | 半径 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:set_collision_radius(1.0)
```

---

## is_destroyed

method in Unit

- 描述

    

- 参数

    无

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:is_destroyed()
```

---
