---
sidebarDepth: 1
---
# 单位 (Unit)

# 索引

Y3 编辑器单位对象相关接口，用于操作单位的属性、位置、状态等。

---

| 接口 | 描述 |
| --- | --- |
| [api_get_id](#api_get_id) | 获取单位ID |
| [api_get_key](#api_get_key) | 获取单位编号 |
| [api_get_camp_id](#api_get_camp_id) | 获取单位所属阵营id |
| [api_get_role_id](#api_get_role_id) | 获取单位所属玩家ID |
| [api_get_role](#api_get_role) | 获取单位所属玩家 |
| [api_get_camp](#api_get_camp) | 获取单位所属阵营 |
| [api_get_type](#api_get_type) | 获取单位类型 |
| [add_timer](#add_timer) | 添加定时器 |
| [add_repeat_timer](#add_repeat_timer) | 添加周期定时器 |
| [cancel_timer](#cancel_timer) | 取消定时器 |
| [api_remove_kv](#api_remove_kv) | 单位移除键值对 |
| [api_is_alive](#api_is_alive) | 单位是否存活 |
| [api_hide_head_bar](#api_hide_head_bar) | 隐藏头顶信息 |
| [has_tag](#has_tag) | 单位是否拥有标签 |
| [api_revive](#api_revive) | 复活单位 |
| [api_is_destroyed](#api_is_destroyed) | 单位是否已销毁 |
| [api_delete](#api_delete) | 删除单位 |
| [api_kill](#api_kill) | 强制单位死亡 |
| [api_get_icon](#api_get_icon) | 获取单位图标路径 |
| [api_get_unit_pic](#api_get_unit_pic) | 获取单位图片路径 |
| [api_get_parent_unit](#api_get_parent_unit) | 获取单位的父单位 |
| [api_set_hp_color](#api_set_hp_color) | 改变单位血条颜色 |
| [api_switch_atk_assist_record](#api_switch_atk_assist_record) | 开启/关闭伤害及助攻统计 |
| [api_is_in_range](#api_is_in_range) | 单位/点是否在范围内 |
| [api_is_point_in_range](#api_is_point_in_range) | 点是否在范围内 |
| [api_set_life_cycle](#api_set_life_cycle) | 设置单位生命周期 |
| [api_pause_life_cycle](#api_pause_life_cycle) | 暂停单位生命周期 |
| [api_get_life_cycle](#api_get_life_cycle) | 获取单位当前生命周期 |
| [api_get_total_life_cycle](#api_get_total_life_cycle) | 获取单位总生命周期时长 |
| [api_set_attack_type](#api_set_attack_type) | 设置单位攻击类型 |
| [api_get_atk_type](#api_get_atk_type) | 获取单位攻击类型 |
| [api_is_attack_type](#api_is_attack_type) | 攻击类型判断 |
| [api_set_armor_type](#api_set_armor_type) | 设置单位护甲类型 |
| [api_get_armor_type](#api_get_armor_type) | 获取单位护甲类型 |
| [api_is_armor_type](#api_is_armor_type) | 护甲类型判断 |
| [api_get_x_scale](#api_get_x_scale) | 获取单位的x轴缩放 |
| [api_get_y_scale](#api_get_y_scale) | 获取单位的y轴缩放 |
| [api_get_z_scale](#api_get_z_scale) | 获取单位的z轴缩放 |
| [api_get_ai_battle_target_unit](#api_get_ai_battle_target_unit) | 获取单位的仇恨单位 |
| [api_get_ai_follow_target_unit](#api_get_ai_follow_target_unit) | 获取单位的跟随单位 |
| [api_get_attr_other](#api_get_attr_other) | 获取 attr_other |
| [api_get_attr_base](#api_get_attr_base) | 获取attr_base |
| [api_get_attr_base_ratio](#api_get_attr_base_ratio) | 获取attr_base_ratio |
| [api_get_attr_bonus](#api_get_attr_bonus) | 获取attr_bonus |
| [api_get_attr_bonus_ratio](#api_get_attr_bonus_ratio) | 获取attr_bonus_ratio |
| [api_get_attr_all_ratio](#api_get_attr_all_ratio) | 获取attr_all_ratio |
| [api_get_main_attr](#api_get_main_attr) | 获取单位主属性 |
| [api_set_attr](#api_set_attr) | 设置纯值类型的值 |
| [api_set_attr_by_attr_element](#api_set_attr_by_attr_element) | 设置单位属性（根据属性分类） |
| [api_set_attr_base](#api_set_attr_base) | 设置单位属性基础值部分 |
| [api_add_attr_by_attr_element](#api_add_attr_by_attr_element) | 增加单位属性（根据属性分类） |
| [api_add_attr_base](#api_add_attr_base) | 增加单位属性基础值 |
| [api_set_attr_bonus](#api_set_attr_bonus) | 设置单位属性 attr_bonus |
| [api_add_attr_bonus](#api_add_attr_bonus) | 增加单位属性 attr_bonus |
| [api_set_attr_bonus_ratio](#api_set_attr_bonus_ratio) | 设置单位属性 attr_bouns_ratio |
| [api_add_attr_bonus_ratio](#api_add_attr_bonus_ratio) | 增加单位属性 attr_bouns_ratio |
| [api_set_attr_all_ratio](#api_set_attr_all_ratio) | 设置单位属性 基础值和额外值 加成比例 |
| [api_add_attr_all_ratio](#api_add_attr_all_ratio) | 增加单位属性 基础值和额外值 加成比例 |
| [api_set_attr_base_ratio](#api_set_attr_base_ratio) | 设置单位属性 基础值 加成比例 |
| [api_add_attr_base_ratio](#api_add_attr_base_ratio) | 增加单位属性基础值百分比加成 |
| [api_set_level](#api_set_level) | 设置单位等级 |
| [api_add_level](#api_add_level) | 增加单位等级 |
| [api_get_attr](#api_get_attr) | 获取单位实数属性 |
| [api_get_float_attr](#api_get_float_attr) | 获取单位实数属性 |
| [api_get_str_attr](#api_get_str_attr) | 获取单位字符串属性 |
| [api_set_str_attr](#api_set_str_attr) | 设置单位字符串属性 |
| [api_get_level](#api_get_level) | 获取单位等级 |
| [api_get_hp](#api_get_hp) | 获取单位血量 |
| [api_get_hpp](#api_get_hpp) | 获取单位血量百分比 |
| [api_heal](#api_heal) | 治疗单位 |
| [api_get_dmg_statistics](#api_get_dmg_statistics) | 获取输出伤害统计值 |
| [api_clear_dmg_statistics](#api_clear_dmg_statistics) | 清空输出伤害统计值 |
| [api_add_exp](#api_add_exp) | 增加经验，增加值为正数 |
| [api_set_exp](#api_set_exp) | 设置经验 |
| [api_get_exp](#api_get_exp) | 获取单位当前经验, 如果达到了顶级，就返回-1 |
| [api_get_upgrade_exp](#api_get_upgrade_exp) | 获取当前升级所需经验, 如果达到了顶级，就返回-1 |
| [api_add_tag](#api_add_tag) | 单位移除键值对 |
| [api_remove_tag](#api_remove_tag) | 单位移除键值对 |
| [api_set_recycle_on_remove](#api_set_recycle_on_remove) | 设置单位删除时是否回收 |
| [api_set_name](#api_set_name) | 设置单位名称 |
| [api_get_name](#api_get_name) | 获取单位名称 |
| [api_set_unit_day_vision](#api_set_unit_day_vision) | 设置单位白天视野 |
| [api_get_unit_day_vision](#api_get_unit_day_vision) | 获取单位白天视野 |
| [api_set_unit_night_vision](#api_set_unit_night_vision) | 设置单位夜晚视野 |
| [api_get_unit_night_vision](#api_get_unit_night_vision) | 获取单位夜晚视野 |
| [api_set_unit_alarm_range](#api_set_unit_alarm_range) | 设置单位警戒范围 |
| [api_get_unit_alarm_range](#api_get_unit_alarm_range) | 获取单位警戒范围 |
| [api_set_unit_cancel_alarm_range](#api_set_unit_cancel_alarm_range) | 设置单位取消警戒范围 |
| [api_get_unit_cancel_alarm_range](#api_get_unit_cancel_alarm_range) | 获取单位取消警戒范围 |
| [api_get_unit_bar_cnt](#api_get_unit_bar_cnt) | 获取单位物品栏数量 |
| [api_get_unit_pkg_cnt](#api_get_unit_pkg_cnt) | 获取单位背包栏数量 |
| [api_get_unit_collision_radius](#api_get_unit_collision_radius) | 获取单位动态碰撞半径 |
| [api_get_unit_reward_exp](#api_get_unit_reward_exp) | 获取单位被击杀经验 |
| [api_get_unit_reward_res](#api_get_unit_reward_res) | 获取单位被击杀的玩家属性 |
| [api_set_unit_reward_exp](#api_set_unit_reward_exp) | 设置单位被击杀经验 |
| [api_set_unit_reward_res](#api_set_unit_reward_res) | 设置单位被击杀的玩家属性 |
| [api_get_unit_shield_value](#api_get_unit_shield_value) | 获取单位的护盾值 |
| [api_set_unit_icon](#api_set_unit_icon) | 设置单位的头像 |
| [api_get_unit_main_attr](#api_get_unit_main_attr) | 获取单位主属性 |
| [api_stop_move](#api_stop_move) | 单位停止移动 |
| [api_transmit](#api_transmit) | 单位传送到指定坐标 |
| [api_force_transmit](#api_force_transmit) | 单位强制传送到指定坐标 |
| [api_force_transmit_new](#api_force_transmit_new) | 单位强制传送到指定坐标 |
| [api_set_face_dir](#api_set_face_dir) | 单位设置朝向 |
| [api_set_face_angle](#api_set_face_angle) | 单位设置朝向角度 |
| [api_set_face_angle_inner_usage](#api_set_face_angle_inner_usage) | 单位设置朝向角度 |
| [api_can_teleport_to](#api_can_teleport_to) | 单位是否能传送到目标点 |
| [api_find_nearest_valid_position](#api_find_nearest_valid_position) | 获取单位在目标点附近的最近可通行点 |
| [api_get_position](#api_get_position) | 获取单位位置 |
| [api_get_face_dir](#api_get_face_dir) | 获取单位朝向 |
| [get_face_angle](#get_face_angle) | 获取单位面向角度 |
| [api_set_turn_speed](#api_set_turn_speed) | 设置单位转身速度 |
| [api_get_turn_speed](#api_get_turn_speed) | 获得单位转身速度 |
| [api_is_moving](#api_is_moving) | 单位是否在移动 |
| [api_get_move_collision](#api_get_move_collision) | 获取单位是否计算某种碰撞类型 |
| [set_move_channel_land](#set_move_channel_land) | 设置单位的移动类型为地面 |
| [set_move_channel_air](#set_move_channel_air) | 设置单位的移动类型为空中 |
| [get_unit_path_length_between_points](#get_unit_path_length_between_points) | 获取单位从点到点的寻路距离 |
| [api_play_animation](#api_play_animation) | 播放动画 |
| [api_play_animation_inner_usage](#api_play_animation_inner_usage) | 播放动画 内部 |
| [api_set_animation_graph_inner_usage](#api_set_animation_graph_inner_usage) | 设置动画graph 内部 |
| [api_stop_animation](#api_stop_animation) | 停止播放动画 |
| [api_stop_cur_animation](#api_stop_cur_animation) | 停止当前正在播放的动画 |
| [api_set_animation_speed](#api_set_animation_speed) | 设置动画速度 |
| [api_play_sfx](#api_play_sfx) | 单位播放特效 |
| [api_unit_play_sfx_on_socket](#api_unit_play_sfx_on_socket) | 在单位挂接点播放特效 |
| [api_play_sfx_with_return](#api_play_sfx_with_return) | 在单位上播放特效并返回特效实体 |
| [api_change_animation](#api_change_animation) | 单位替换播放动画 |
| [api_cancel_change_animation](#api_cancel_change_animation) | 取消单位替换播放动画 |
| [api_clear_change_animation](#api_clear_change_animation) | 取消单位所有替换播放动画 |
| [api_change_model](#api_change_model) | 单位替换模型 |
| [api_cancel_change_model](#api_cancel_change_model) | 取消单位替换模型 |
| [api_clear_change_model](#api_clear_change_model) | 取消单位所有替换模型 |
| [api_replace_model](#api_replace_model) | 单位替换模型 |
| [api_cancel_replace_model](#api_cancel_replace_model) | 取消单位替换模型 |
| [api_show_health_bar_count_down](#api_show_health_bar_count_down) | 显示血条倒计时 |
| [api_get_model](#api_get_model) | 获取单位模型 |
| [api_get_source_model](#api_get_source_model) | 获取单位原模型 |
| [api_show_text](#api_show_text) | 显示单位头顶文本 |
| [api_set_title](#api_set_title) | 更改单位称号 |
| [api_set_title_visible](#api_set_title_visible) | 设置单位称号可见性 |
| [api_set_name_visible](#api_set_name_visible) | 隐藏显示单位名称,对于无头顶UI的单位该API不生效,每次隐藏计数+1,每次显示计数-1,计数归零显示单位名称 |
| [api_set_bar_name_visible](#api_set_bar_name_visible) | 隐藏显示单位名称,对于无头顶UI的单位该API不生效,每次隐藏计数+1,每次显示计数-1,计数归零显示单位名称 |
| [api_set_bar_name](#api_set_bar_name) | 设置血条显示名字 |
| [set_bar_name_scale](#set_bar_name_scale) | 设置血条显示名字缩放 |
| [api_set_bar_name_font_type](#api_set_bar_name_font_type) | 设置血条显示名字字体 |
| [api_set_bar_name_font_size](#api_set_bar_name_font_size) | 设置血条显示名字字体大小 |
| [api_set_bar_text_visible](#api_set_bar_text_visible) | 隐藏显示单位头顶文本,每次隐藏计数+1,每次显示计数-1,计数归零显示单位头顶文本 |
| [api_set_bar_text_scale](#api_set_bar_text_scale) | 设置头顶显示文字缩放 |
| [api_set_bar_text_type](#api_set_bar_text_type) | 设置头顶显示文字类型 |
| [api_set_bar_text_font_type](#api_set_bar_text_font_type) | 设置头顶显示文字字体 |
| [api_set_bar_text_font_size](#api_set_bar_text_font_size) | 设置头顶显示文字字号 |
| [api_set_bar_name_show_type](#api_set_bar_name_show_type) | 设置血条名称显示样式 |
| [api_set_hp_bar_visible](#api_set_hp_bar_visible) | 隐藏显示单位血条,对于无头顶UI的单位该API不生效,每次隐藏计数+1,每次显示计数-1,计数归零显示单位血条 |
| [api_set_hp_bar_show_type](#api_set_hp_bar_show_type) | 设置单位血条显示样式,对于无头顶UI的单位该API不生效 |
| [api_set_hp_bar_type](#api_set_hp_bar_type) | 设置单位血条样式,对于无头顶UI的单位该API不生效 |
| [api_add_ui_comp](#api_add_ui_comp) | 绑定UI控件 |
| [api_change_title_font_size](#api_change_title_font_size) | 修改单位称号字号 |
| [api_change_title_scale](#api_change_title_scale) | 修改单位称号缩放 |
| [api_change_title_font_type](#api_change_title_font_type) | 修改单位称号字体 |
| [api_change_title_type](#api_change_title_type) | 修改单位称号样式 |
| [api_set_title_bg_opacity](#api_set_title_bg_opacity) | 修改单位称号背景不透明度 |
| [api_set_title_bg_scale](#api_set_title_bg_scale) | 修改单位称号背景缩放 |
| [api_set_blood_scale_visible](#api_set_blood_scale_visible) | 修改单位血条刻度可见性 |
| [api_set_title_bar_pos_offset](#api_set_title_bar_pos_offset) | 修改单位称号位置偏移 |
| [api_set_hp_bar_pos_offset](#api_set_hp_bar_pos_offset) | 修改单位血条位置偏移 |
| [api_set_name_bar_pos_offset](#api_set_name_bar_pos_offset) | 修改单位名称位置偏移 |
| [api_set_text_bar_pos_offset](#api_set_text_bar_pos_offset) | 修改单位文本位置偏移 |
| [api_set_countdown_bar_pos_offset](#api_set_countdown_bar_pos_offset) | 修改单位倒计时位置偏移 |
| [api_raise_height](#api_raise_height) | 单位抬高 |
| [api_get_height](#api_get_height) | 获取单位高度 |
| [api_set_scale](#api_set_scale) | 设置单位缩放 |
| [api_set_unit_scale](#api_set_unit_scale) | 设置单位三轴缩放 |
| [api_get_scale](#api_get_scale) | 获取单位缩放 |
| [api_get_model_scale](#api_get_model_scale) | 获取单位模型缩放 |
| [api_set_blood_bar_type](#api_set_blood_bar_type) | 修改单位血条样式 |
| [api_set_blood_bar_show_type](#api_set_blood_bar_show_type) | 修改单位血条显示模式 |
| [api_start_ghost](#api_start_ghost) | 开启残影 |
| [api_stop_ghost](#api_stop_ghost) | 关闭残影 |
| [api_start_dissolve](#api_start_dissolve) | 开始溶解效果 |
| [api_stop_dissolve](#api_stop_dissolve) | 关闭溶解效果 |
| [api_set_ghost_color](#api_set_ghost_color) | 设置残影颜色 |
| [api_set_ghost_time](#api_set_ghost_time) | 设置残影时间 |
| [api_play_sound_by_unit_for_role_relation](#api_play_sound_by_unit_for_role_relation) | 对单位所属玩家关系播放音乐 |
| [api_set_Xray_is_open](#api_set_Xray_is_open) | 设置XRay是否开启 |
| [api_set_transparent_when_invisible](#api_set_transparent_when_invisible) | 设置单位隐身被探测到时是否半透明 |
| [api_set_mini_map_icon](#api_set_mini_map_icon) | 设置单位小地图头像 |
| [api_set_enemy_mini_map_icon](#api_set_enemy_mini_map_icon) | 设置敌方单位小地图头像 |
| [api_set_unit_select_effect_visible](#api_set_unit_select_effect_visible) | 设置单位选择框的可见性 |
| [api_active_gm1_look_at_camera](#api_active_gm1_look_at_camera) | 开关阴阳师模型IDLE时看向摄像机是否开启 |
| [api_set_disk_shadow_open](#api_set_disk_shadow_open) | 设置单位圆盘阴影开关 |
| [api_set_unit_disk_shadow_size](#api_set_unit_disk_shadow_size) | 设置单位圆盘阴影大小 |
| [api_add_modifier](#api_add_modifier) | 单位添加指定编号的效果 |
| [api_get_modifier_stack_count](#api_get_modifier_stack_count) | 获取单位身上指定编号的的效果层数 |
| [api_has_modifier](#api_has_modifier) | 单位身上是否拥有指定编号的效果 |
| [api_has_modifier_with_tag](#api_has_modifier_with_tag) | 单位身上是否拥有指定标签的效果 |
| [api_get_modifier](#api_get_modifier) | 获取单位身上指定编号的第i个效果实例 |
| [api_get_modifier_count](#api_get_modifier_count) | 获取单位身上指定编号的第i个效果的个数 |
| [api_remove_modifier_instance](#api_remove_modifier_instance) | 移除目标单位身上的目标modifier实例 |
| [api_remove_modifier_type](#api_remove_modifier_type) | 移除目标单位身上的目标modifier类型的所有实例 |
| [api_has_modifier_type](#api_has_modifier_type) | 单位身上是否拥有指定类别的效果 |
| [api_delete_all_modifiers_by_effect_type](#api_delete_all_modifiers_by_effect_type) | 删除单位指定影响类型的魔法效果 |
| [api_get_all_modifiers](#api_get_all_modifiers) | 获取单位身上所有的魔法效果 |
| [api_add_ability](#api_add_ability) | 单位添加技能 |
| [api_remove_ability_by_index](#api_remove_ability_by_index) | 单位根据槽位移除技能 |
| [api_remove_abilities_in_type](#api_remove_abilities_in_type) | 单位移除某种类型里所有是指定技能ID的技能 |
| [api_set_ability_level](#api_set_ability_level) | 单位设置技能等级。 |
| [api_unit_learn_ability](#api_unit_learn_ability) | 单位学习技能 |
| [api_get_ability_point](#api_get_ability_point) | 获取英雄的技能点 |
| [api_set_ability_point](#api_set_ability_point) | 设置英雄的技能点 |
| [api_add_ability_point](#api_add_ability_point) | 增加英雄的技能点 |
| [api_get_ability](#api_get_ability) | 通过技能槽位获取技能 |
| [api_get_ability_by_type](#api_get_ability_by_type) | 通过技能类型加技能ID获取技能 |
| [api_get_abilities_by_type](#api_get_abilities_by_type) | 获取某种类型的技能列表 |
| [api_check_has_ability_type](#api_check_has_ability_type) | 是否有对应技能类型的技能 |
| [api_get_all_abilities_can_show](#api_get_all_abilities_can_show) | 获取单位技能列表 |
| [api_switch_ability_by_index](#api_switch_ability_by_index) | 根据坑位交换技能 |
| [api_switch_ability](#api_switch_ability) | 交换技能 |
| [api_disable_ability](#api_disable_ability) | 单位禁用技能。 |
| [api_enable_ability](#api_enable_ability) | 单位解禁技能。 |
| [api_stop_all_abilities](#api_stop_all_abilities) | 停止单位所有技能 |
| [api_unit_has_running_ability](#api_unit_has_running_ability) | 单位是否有正在释放的技能 |
| [api_get_ability_str_attr_value](#api_get_ability_str_attr_value) | 返回单位实体指定槽位技能的字符串属性值 |
| [api_get_ability_by_seq](#api_get_ability_by_seq) | 根据技能序号获取技能对象 |
| [api_add_state](#api_add_state) | 给单位施加状态 |
| [api_remove_state](#api_remove_state) | 给单位去除状态 |
| [api_is_in_battle_state](#api_is_in_battle_state) | 是否在战斗状态 |
| [api_has_state](#api_has_state) | 单位是否处于某状态 |
| [api_release_ability_by_index](#api_release_ability_by_index) | 单位施放技能 |
| [api_release_ability_at_position](#api_release_ability_at_position) | 单位施放技能，具有释放目标地点 |
| [api_create_building_on_point](#api_create_building_on_point) | 发布建造命令(目标点) |
| [api_create_building_on_position](#api_create_building_on_position) | 发布建造命令(坐标) |
| [api_has_item](#api_has_item) | 单位是否拥有物品 |
| [api_has_item_key](#api_has_item_key) | 单位是否拥有特定编号物品 |
| [api_add_item](#api_add_item) | 给单位添加物品名 |
| [api_delete_item](#api_delete_item) | 给单位删除物品名 |
| [api_drop_item](#api_drop_item) | 单位丢弃物品实体到场景中 |
| [api_remove_item](#api_remove_item) | 单位删除物品实体 |
| [api_get_item_by_slot](#api_get_item_by_slot) | 获取单位背包槽位的物品 |
| [api_shift_item](#api_shift_item) | 移动物品 |
| [api_shift_item_new](#api_shift_item_new) | 移动物品 |
| [api_get_all_item_pids](#api_get_all_item_pids) | 单位身上所有物品 |
| [api_set_unit_bar_cnt](#api_set_unit_bar_cnt) | 设置单位物品栏的格子数量 |
| [api_set_unit_pkg_cnt](#api_set_unit_pkg_cnt) | 设置单位背包栏的格子数量 |
| [api_get_num_of_item_type](#api_get_num_of_item_type) | 单位身上拥有指定类型的物品数量 |
| [api_get_item_type_by_slot](#api_get_item_type_by_slot) | 获取单位持有的物品类型 |
| [api_is_shop](#api_is_shop) | 单位是否商店 |
| [api_get_shop_range](#api_get_shop_range) | 获取商店单位范围 |
| [api_add_shop_item](#api_add_shop_item) | 添加物品商品到商店 |
| [api_get_shop_item_list](#api_get_shop_item_list) | 获取商店某页签的商品列表 |
| [api_get_shop_item_cd](#api_get_shop_item_cd) | 获取商店商品的恢复时间 |
| [api_get_shop_item_default_cd](#api_get_shop_item_default_cd) | 获取商店商品的库存恢复间隔 |
| [api_get_shop_item_residual_cd](#api_get_shop_item_residual_cd) | 获取商店商品的剩余恢复时间 |
| [api_get_shop_tab_cnt](#api_get_shop_tab_cnt) | 获取商店页签数量 |
| [api_get_shop_tab_name](#api_get_shop_tab_name) | 获取商店的页签名 |
| [api_get_shop_tab_item_type](#api_get_shop_tab_item_type) | 获取商店指定页签第N个商品的类型 |
| [api_add_shop_unit](#api_add_shop_unit) | 添加单位商品到商店 |
| [api_remove_shop_item](#api_remove_shop_item) | 删除商店物品商品 |
| [api_remove_shop_unit](#api_remove_shop_unit) | 删除商店单位商品 |
| [api_set_shop_item_stock](#api_set_shop_item_stock) | 设置物品商品库存 |
| [api_set_shop_unit_stock](#api_set_shop_unit_stock) | 设置单位商品库存 |
| [api_set_is_shop](#api_set_is_shop) | 设置商店开关 |
| [api_buy_item_with_tab_name](#api_buy_item_with_tab_name) | 单位购买物品 |
| [api_buy_unit_with_tab_name](#api_buy_unit_with_tab_name) | 单位购买单位 |
| [api_sell_item](#api_sell_item) | 单位出售物品 |
| [api_set_shop_target](#api_set_shop_target) | 设置商店目标 |
| [api_get_shop_item_stock](#api_get_shop_item_stock) | 获取单位商店物品商品库存 |
| [api_get_shop_unit_stock](#api_get_shop_unit_stock) | 获取单位商店单位商品库存 |
| [api_get_shop_item_price](#api_get_shop_item_price) | 获取单位商店单位商品售价 |
| [api_shop_check_camp](#api_shop_check_camp) | 玩家是否可以购买商店的物品 |
| [api_upgrade_tech](#api_upgrade_tech) | 科技升级 |
| [api_get_tech_list](#api_get_tech_list) | 获取科技列表 |
| [api_get_affect_techs](#api_get_affect_techs) | 获取科技列表 |
| [api_check_tech_precondition](#api_check_tech_precondition) | 获取科技是否满足前置条件 |
| [api_add_tech](#api_add_tech) | 添加科技 |
| [api_remove_tech](#api_remove_tech) | 删除科技 |
| [api_release_command](#api_release_command) | 发布命令 |
| [api_set_default_switch_behavior](#api_set_default_switch_behavior) | 单位 - 设置默认跳转状态 |
| [api_set_construction_progress](#api_set_construction_progress) | 设置单位建造进度 |
| [api_set_upgrade_progress](#api_set_upgrade_progress) | 设置单位升级进度 |
| [api_set_ai_exit_follow_on_succ_once](#api_set_ai_exit_follow_on_succ_once) | 设置跟随单位成功后是否退出跟随 |
| [api_set_is_sleeping](#api_set_is_sleeping) | 设置单位是否休眠 |
| [api_get_is_sleeping](#api_get_is_sleeping) | 获取单位是否休眠 |
| [api_get_is_in_pool](#api_get_is_in_pool) | 获取单位是否处于缓存池中 |
| [api_unit_transformation](#api_unit_transformation) | 单位变身 |
| [api_queue_reset](#api_queue_reset) | 单位-队列重置 |
| [api_switch_main_attr](#api_switch_main_attr) | 切换主属性 |
| [api_open_attr_cheating_detected](#api_open_attr_cheating_detected) | 开启单位属性作弊检查 |
| [api_get_attr_name](#api_get_attr_name) | 获取单位属性本地化名 |
| [api_set_changed_exp_in_event](#api_set_changed_exp_in_event) | 设置事件中的经验值 |
| [api_get_abilityKey_by_type_and_index](#api_get_abilityKey_by_type_and_index) | 获取单位类型某个技能位的技能类型 |
| [api_get_hprec_pertick](#api_get_hprec_pertick) | 获取每tick的单位生命恢复 |
| [api_set_unit_flying_vision](#api_set_unit_flying_vision) | 设置单位是否飞行视野 |
| [api_set_base_speed](#api_set_base_speed) | 设置动画移动基准速度。会同时修改跑和走的基准速度，如果要区分跑和走，还需额外单独设置走的基准速度(api_set_anim_walk_speed) |
| [api_set_anim_walk_speed](#api_set_anim_walk_speed) | 设置动画移动基准速度(仅走) |
| [api_is_picking_item](#api_is_picking_item) | 单位是否在执行拾取物品命令 |
| [api_is_move_type](#api_is_move_type) | 判断单位的移动类型 |
| [api_set_block_others](#api_set_block_others) | 设置是否阻挡其他单位 |
| [api_set_lock_yaw](#api_set_lock_yaw) | 开启锁定移动 |
| [api_set_unlock_yaw](#api_set_unlock_yaw) | 结束锁定移动 |
| [set_joystick_base_direction](#set_joystick_base_direction) | 设置摇杆基方向 |
| [set_joystick_input](#set_joystick_input) | 设置摇杆输入 |
| [directional_move_to_pos](#directional_move_to_pos) | 径直移动 |
| [set_path_finding_step_bound](#set_path_finding_step_bound) | 设置寻路消耗上限 |
| [set_model_by_tag](#set_model_by_tag) | 单位设置指定标签模型 |
| [remove_model_by_tag](#remove_model_by_tag) | 单位删除设置指定标签模型 |
| [change_model_texture](#change_model_texture) | 替换模型贴图 |
| [api_set_forbid_aligned_terrain](#api_set_forbid_aligned_terrain) | 单位禁止贴地 |
| [api_set_scale_2](#api_set_scale_2) | 设置单位缩放 |
| [api_start_windforce](#api_start_windforce) | 开启风场 |
| [api_set_ghost_color_norm](#api_set_ghost_color_norm) | 设置残影颜色 |
| [api_set_ghost_color_hex](#api_set_ghost_color_hex) | 设置残影颜色(HEX) |
| [api_set_unit_is_mini_map_show](#api_set_unit_is_mini_map_show) | 小地图 - 设置单位小地图头像可见性 |
| [api_set_unit_anim_state_name](#api_set_unit_anim_state_name) | 设置单位动画状态名 |
| [set_unit_outlined_color](#set_unit_outlined_color) | 设置单位的描边颜色 |
| [set_unit_outlined_color_hex](#set_unit_outlined_color_hex) | 设置单位的描边颜色(HEX) |
| [set_unit_outlined_enable](#set_unit_outlined_enable) | 开关单位描边效果 |
| [play_upper_body_anim](#play_upper_body_anim) | 播放上半身动画 |
| [set_bone_filter_config](#set_bone_filter_config) | 自定义骨骼分层 |
| [play_additive_anim](#play_additive_anim) | 播放叠加动画 |
| [set_unit_outside_outline_width](#set_unit_outside_outline_width) | 设置单位外轮廓描边厚度 |
| [set_unit_outside_outline_color](#set_unit_outside_outline_color) | 设置单位外轮廓描边颜色 |
| [set_unit_outside_outlined_enable](#set_unit_outside_outlined_enable) | 设置单位外轮廓描边是否开启 |
| [unit_loadGraph](#unit_loadGraph) | 单位加载自定义的graph |
| [unit_Graph_SetVariable](#unit_Graph_SetVariable) | 自定义Graph设置变量 |
| [unit_Graph_FireEvent](#unit_Graph_FireEvent) | 自定义Graph发送事件 |
| [unit_Graph_SetSpeed](#unit_Graph_SetSpeed) | 自定义Graph设置速度 |
| [unit_Graph_Pause](#unit_Graph_Pause) | 暂停Graph |
| [unit_Graph_RunOneFrame](#unit_Graph_RunOneFrame) | 暂停中跑一帧Graph |
| [api_add_multi_state](#api_add_multi_state) | 给单位施加状态 |
| [api_remove_multi_state](#api_remove_multi_state) | 给单位去除状态 |
| [api_get_unit_attack_interval](#api_get_unit_attack_interval) | 获取单位攻击间隔 |
| [api_get_unit_attack_count_per_second](#api_get_unit_attack_count_per_second) | 获取单位每秒攻击次数 |
| [api_get_common_atk_ability](#api_get_common_atk_ability) | 获取普攻技能 |
| [api_set_simple_atk_dice_max_value](#api_set_simple_atk_dice_max_value) | 设置单位简易普攻骰子最大值 |
| [api_get_simple_atk_dice_max_value](#api_get_simple_atk_dice_max_value) | 获取单位简易普攻骰子最大值 |
| [api_set_simple_atk_dice_count](#api_set_simple_atk_dice_count) | 设置单位简易普攻骰子最大值 |
| [api_get_simple_atk_dice_count](#api_get_simple_atk_dice_count) | 获取单位简易普攻骰子个数 |
| [api_get_cur_record_ability](#api_get_cur_record_ability) | 获取单位正在释放的技能 |
| [api_pause_all_ability_cd](#api_pause_all_ability_cd) | 暂停单位所有技能的CD |
| [api_resume_all_ability_cd](#api_resume_all_ability_cd) | 恢复单位所有技能的CD |
| [api_clear_all_abilities](#api_clear_all_abilities) | 移除单位所有技能 |
| [api_get_slot_capacity](#api_get_slot_capacity) | 获取单位栏位剩余空间 |
| [api_set_default_switch_command](#api_set_default_switch_command) | 单位 - 设置默认跳转命令 |
| [api_load_default_ai](#api_load_default_ai) | 单位 - 跳转到默认命令或状态 |
| [api_trigger_rescue](#api_trigger_rescue) | 单位 - 单位发起求救 |
| [api_set_rescue_seeker_type](#api_set_rescue_seeker_type) | 单位 - 设置单位求救类型 |
| [api_set_rescuer_type](#api_set_rescuer_type) | 单位 - 设置单位救援类型 |
| [api_set_rescue_seeker_distance](#api_set_rescue_seeker_distance) | 单位 - 设置单位求救距离 |
| [api_set_rescue_seeker_interval](#api_set_rescue_seeker_interval) | 单位 - 设置单位求救间隔 |
| [api_set_rescue_finish_return](#api_set_rescue_finish_return) | 单位 - 设置单位救援后返回 |
| [api_get_rescue_seeker_type](#api_get_rescue_seeker_type) | 单位 - 获取单位求救类型 |
| [api_get_rescuer_type](#api_get_rescuer_type) | 单位 - 获取单位救援类型 |
| [api_get_rescue_seeker_distance](#api_get_rescue_seeker_distance) | 单位 - 获取单位求救距离 |
| [api_get_rescue_seeker_interval](#api_get_rescue_seeker_interval) | 单位 - 获取单位求救间隔 |
| [api_get_rescue_finish_return](#api_get_rescue_finish_return) | 单位 - 获取单位救援后返回 |
| [api_get_is_rescuing](#api_get_is_rescuing) | 单位 - 获取单位是否正在救援 |
| [api_get_is_rescue_returning](#api_get_is_rescue_returning) | 单位 - 获取单位是否正在救援后返回 |
| [api_try_update_ai](#api_try_update_ai) | 单位 - 尝试触发AI更新 |
| [api_do_next_command](#api_do_next_command) | 单位 - 执行下一命令 |
| [api_is_command_queue_empty](#api_is_command_queue_empty) | 单位 - 获取命令队列是否为空 |
| [api_set_repair_target_unit](#api_set_repair_target_unit) | 单位 - 设置维修目标单位 |
| [api_set_repair_ability](#api_set_repair_ability) | 单位 - 设置维修技能 |

---

## api_get_id

method in Unit

- 描述

    获取单位ID

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitID? | 单位ID |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_id()
```

---

## api_get_key

method in Unit

- 描述

    获取单位编号

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitKey? | 单位编号 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_key()
```

---

## api_get_camp_id

method in Unit

- 描述

    获取单位所属阵营id

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CampID? | 阵营ID |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_camp_id()
```

---

## api_get_role_id

method in Unit

- 描述

    获取单位所属玩家ID

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleID? | 玩家ID |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_role_id()
```

---

## api_get_role

method in Unit

- 描述

    获取单位所属玩家

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Role? | 玩家 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_role()
```

---

## api_get_camp

method in Unit

- 描述

    获取单位所属阵营

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Camp? | 阵营 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_camp()
```

---

## api_get_type

method in Unit

- 描述

    获取单位类型

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitType? | 单位类型 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_type()
```

---

## add_timer

method in Unit

- 描述

    添加定时器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | time | py.Fixed | 定时时长 |
    | callback | function | 超时函数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 定时器ID |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:add_timer(Fix32(1), function() end)
```

---

## add_repeat_timer

method in Unit

- 描述

    添加周期定时器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | time | py.Fixed | 定时时长 |
    | callback | function | 超时函数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 定时器ID |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:add_repeat_timer(Fix32(1), function() end)
```

---

## cancel_timer

method in Unit

- 描述

    取消定时器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | timer_id | integer | 定时器ID |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:cancel_timer(1)
```

---

## api_remove_kv

method in Unit

- 描述

    单位移除键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | k | string | 键名 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_remove_kv("k")
```

---

## api_is_alive

method in Unit

- 描述

    单位是否存活

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 单位是否存活 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_is_alive()
```

---

## api_hide_head_bar

method in Unit

- 描述

    隐藏头顶信息

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | show | boolean | 是否隐藏头顶信息 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_hide_head_bar(true)
```

---

## has_tag

method in Unit

- 描述

    单位是否拥有标签

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | 标签 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 单位是否拥有标签 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:has_tag("tag")
```

---

## api_revive

method in Unit

- 描述

    复活单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | position? | py.Point | 复活位置 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local point = Fix32Vec3(0, 0, 0)

unit.handle:api_revive()
```

---

## api_is_destroyed

method in Unit

- 描述

    单位是否已销毁

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 单位是否已销毁 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_is_destroyed()
```

---

## api_delete

method in Unit

- 描述

    删除单位

- 参数

    无

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_delete()
```

---

## api_kill

method in Unit

- 描述

    强制单位死亡

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | source_unit? | py.Unit | 杀手单位 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_kill()
```

---

## api_get_icon

method in Unit

- 描述

    获取单位图标路径

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string? | 单位图标路径 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_icon()
```

---

## api_get_unit_pic

method in Unit

- 描述

    获取单位图片路径

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | pic_type | string | 图片类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string? | 单位图片路径 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_unit_pic("pic_type")
```

---

## api_get_parent_unit

method in Unit

- 描述

    获取单位的父单位

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit? | 单位的父单位 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_parent_unit()
```

---

## api_set_hp_color

method in Unit

- 描述

    改变单位血条颜色

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | color | string | 单位血条颜色值 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_hp_color("color")
```

---

## api_switch_atk_assist_record

method in Unit

- 描述

    开启/关闭伤害及助攻统计

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | enable | boolean | 开启 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_switch_atk_assist_record(true)
```

---

## api_is_in_range

method in Unit

- 描述

    单位/点是否在范围内

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | radius | number | 范围 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 是否在范围内 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_is_in_range(unit.handle, 1.0)
```

---

## api_is_point_in_range

method in Unit

- 描述

    点是否在范围内

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.Point | 点 |
    | radius | number | 范围 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 是否在范围内 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local point = Fix32Vec3(0, 0, 0)

local result = unit.handle:api_is_point_in_range(point, 1.0)
```

---

## api_set_life_cycle

method in Unit

- 描述

    设置单位生命周期

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | life_time | number | 生命周期 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_life_cycle(1.0)
```

---

## api_pause_life_cycle

method in Unit

- 描述

    暂停单位生命周期

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | pause | boolean | 是否暂停 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_pause_life_cycle(true)
```

---

## api_get_life_cycle

method in Unit

- 描述

    获取单位当前生命周期

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 生命周期 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_life_cycle()
```

---

## api_get_total_life_cycle

method in Unit

- 描述

    获取单位总生命周期时长

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 生命周期 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_total_life_cycle()
```

---

## api_set_attack_type

method in Unit

- 描述

    设置单位攻击类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attack_type | integer | 攻击类型 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_attack_type(1)
```

---

## api_get_atk_type

method in Unit

- 描述

    获取单位攻击类型

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 攻击类型 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_atk_type()
```

---

## api_is_attack_type

method in Unit

- 描述

    攻击类型判断

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attack_type | integer | 攻击类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 攻击类型判断 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_is_attack_type(1)
```

---

## api_set_armor_type

method in Unit

- 描述

    设置单位护甲类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | armor_type | integer | 护甲类型 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_armor_type(1)
```

---

## api_get_armor_type

method in Unit

- 描述

    获取单位护甲类型

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 护甲类型 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_armor_type()
```

---

## api_is_armor_type

method in Unit

- 描述

    护甲类型判断

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | armor_type | integer | 护甲类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 护甲类型判断 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_is_armor_type(1)
```

---

## api_get_x_scale

method in Unit

- 描述

    获取单位的x轴缩放

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number? | 缩放的值 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_x_scale()
```

---

## api_get_y_scale

method in Unit

- 描述

    获取单位的y轴缩放

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number? | 缩放的值 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_y_scale()
```

---

## api_get_z_scale

method in Unit

- 描述

    获取单位的z轴缩放

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number? | 缩放的值 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_z_scale()
```

---

## api_get_ai_battle_target_unit

method in Unit

- 描述

    获取单位的仇恨单位

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit? | 仇恨的单位 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_ai_battle_target_unit()
```

---

## api_get_ai_follow_target_unit

method in Unit

- 描述

    获取单位的跟随单位

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit? | 跟随的单位 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_ai_follow_target_unit()
```

---

## api_get_attr_other

method in Unit

- 描述

    获取 attr_other

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 属性名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 属性值 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_attr_other("key")
```

---

## api_get_attr_base

method in Unit

- 描述

    获取attr_base

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 属性名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 属性值 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_attr_base("key")
```

---

## api_get_attr_base_ratio

method in Unit

- 描述

    获取attr_base_ratio

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 属性名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 属性值 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_attr_base_ratio("key")
```

---

## api_get_attr_bonus

method in Unit

- 描述

    获取attr_bonus

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 属性名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 属性值 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_attr_bonus("key")
```

---

## api_get_attr_bonus_ratio

method in Unit

- 描述

    获取attr_bonus_ratio

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 属性名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 属性值 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_attr_bonus_ratio("key")
```

---

## api_get_attr_all_ratio

method in Unit

- 描述

    获取attr_all_ratio

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 属性名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 属性值 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_attr_all_ratio("key")
```

---

## api_get_main_attr

method in Unit

- 描述

    获取单位主属性

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string? | 主属性 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_main_attr()
```

---

## api_set_attr

method in Unit

- 描述

    设置纯值类型的值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 属性名 |
    | val | py.Fixed | 值 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_attr("key", Fix32(1))
```

---

## api_set_attr_by_attr_element

method in Unit

- 描述

    设置单位属性（根据属性分类）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 属性名 |
    | val | py.Fixed | 值 |
    | attr_element | string | 属性分类 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_attr_by_attr_element("key", Fix32(1), "attr_element")
```

---

## api_set_attr_base

method in Unit

- 描述

    设置单位属性基础值部分

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 属性名 |
    | val | py.Fixed | 基础值 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_attr_base("key", Fix32(1))
```

---

## api_add_attr_by_attr_element

method in Unit

- 描述

    增加单位属性（根据属性分类）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 属性名 |
    | val | py.Fixed | 值 |
    | attr_element | string | 属性分类 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_add_attr_by_attr_element("key", Fix32(1), "attr_element")
```

---

## api_add_attr_base

method in Unit

- 描述

    增加单位属性基础值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 属性名 |
    | delta | py.Fixed | 增加值 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_add_attr_base("key", Fix32(1))
```

---

## api_set_attr_bonus

method in Unit

- 描述

    设置单位属性 attr_bonus

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 属性名 |
    | val | py.Fixed | 设置值 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_attr_bonus("key", Fix32(1))
```

---

## api_add_attr_bonus

method in Unit

- 描述

    增加单位属性 attr_bonus

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 属性名 |
    | delta | py.Fixed | 增加值 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_add_attr_bonus("key", Fix32(1))
```

---

## api_set_attr_bonus_ratio

method in Unit

- 描述

    设置单位属性 attr_bouns_ratio

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 属性名 |
    | val | py.Fixed | 设置值 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_attr_bonus_ratio("key", Fix32(1))
```

---

## api_add_attr_bonus_ratio

method in Unit

- 描述

    增加单位属性 attr_bouns_ratio

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 属性名 |
    | delta | py.Fixed | 加成比例 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_add_attr_bonus_ratio("key", Fix32(1))
```

---

## api_set_attr_all_ratio

method in Unit

- 描述

    设置单位属性 基础值和额外值 加成比例

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 属性名 |
    | val | py.Fixed | 设置值 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_attr_all_ratio("key", Fix32(1))
```

---

## api_add_attr_all_ratio

method in Unit

- 描述

    增加单位属性 基础值和额外值 加成比例

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 属性名 |
    | delta | py.Fixed | 加成比例 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_add_attr_all_ratio("key", Fix32(1))
```

---

## api_set_attr_base_ratio

method in Unit

- 描述

    设置单位属性 基础值 加成比例

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 属性名 |
    | val | py.Fixed | 设置值 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_attr_base_ratio("key", Fix32(1))
```

---

## api_add_attr_base_ratio

method in Unit

- 描述

    增加单位属性基础值百分比加成

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 属性名 |
    | delta | py.Fixed | 加成比例 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_add_attr_base_ratio("key", Fix32(1))
```

---

## api_set_level

method in Unit

- 描述

    设置单位等级

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | level | integer | 等级 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_level(1)
```

---

## api_add_level

method in Unit

- 描述

    增加单位等级

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | level | integer | 等级 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_add_level(1)
```

---

## api_get_attr

method in Unit

- 描述

    获取单位实数属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 属性类型 |
    | attr | string | 属性名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 实数属性值 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_attr("key", "attr")
```

---

## api_get_float_attr

method in Unit

- 描述

    获取单位实数属性

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
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_float_attr("attr")
```

---

## api_get_str_attr

method in Unit

- 描述

    获取单位字符串属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr | string | 属性名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string? | 字符串属性值 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_str_attr("attr")
```

---

## api_set_str_attr

method in Unit

- 描述

    设置单位字符串属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr | string | 属性名 |
    | value | string | 字符串值 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_str_attr("attr", "value")
```

---

## api_get_level

method in Unit

- 描述

    获取单位等级

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 单位等级 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_level()
```

---

## api_get_hp

method in Unit

- 描述

    获取单位血量

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 单位血量 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_hp()
```

---

## api_get_hpp

method in Unit

- 描述

    获取单位血量百分比

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 单位血量百分比 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_hpp()
```

---

## api_heal

method in Unit

- 描述

    治疗单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | hp_change | py.Fixed | 治疗的数值 |
    | jump_word? | boolean | 是否跳字 |
    | related_ability? | py.Ability | 关联技能 |
    | source_unit? | py.Unit | 来源单位 |
    | harm_text_enum? | string | 跳字枚举 |
    | jump_word_track? | integer | 跳字轨迹 |
    | pos_socket? | string | 挂接点 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

unit.handle:api_heal(Fix32(1), true, nil, nil, "harm_text_enum", 1, "pos_socket")
```

---

## api_get_dmg_statistics

method in Unit

- 描述

    获取输出伤害统计值

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 输出伤害统计值 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_dmg_statistics()
```

---

## api_clear_dmg_statistics

method in Unit

- 描述

    清空输出伤害统计值

- 参数

    无

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_clear_dmg_statistics()
```

---

## api_add_exp

method in Unit

- 描述

    增加经验，增加值为正数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | exp | py.Fixed | 经验 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_add_exp(Fix32(1))
```

---

## api_set_exp

method in Unit

- 描述

    设置经验

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | exp | py.Fixed | 经验 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_exp(Fix32(1))
```

---

## api_get_exp

method in Unit

- 描述

    获取单位当前经验, 如果达到了顶级，就返回-1

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 单位当前经验值 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_exp()
```

---

## api_get_upgrade_exp

method in Unit

- 描述

    获取当前升级所需经验, 如果达到了顶级，就返回-1

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 当前升级所需经验值 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_upgrade_exp()
```

---

## api_add_tag

method in Unit

- 描述

    单位移除键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | TAG |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_add_tag("tag")
```

---

## api_remove_tag

method in Unit

- 描述

    单位移除键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | TAG |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_remove_tag("tag")
```

---

## api_set_recycle_on_remove

method in Unit

- 描述

    设置单位删除时是否回收

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | recycle? | boolean | 是否回收 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_recycle_on_remove(true)
```

---

## api_set_name

method in Unit

- 描述

    设置单位名称

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | name | string | 名称 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_name("name")
```

---

## api_get_name

method in Unit

- 描述

    获取单位名称

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string? | 单位名称 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_name()
```

---

## api_set_unit_day_vision

method in Unit

- 描述

    设置单位白天视野

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | number | 视野 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_unit_day_vision(1.0)
```

---

## api_get_unit_day_vision

method in Unit

- 描述

    获取单位白天视野

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 白天视野 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_unit_day_vision()
```

---

## api_set_unit_night_vision

method in Unit

- 描述

    设置单位夜晚视野

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | number | 视野 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_unit_night_vision(1.0)
```

---

## api_get_unit_night_vision

method in Unit

- 描述

    获取单位夜晚视野

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 夜晚视野 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_unit_night_vision()
```

---

## api_set_unit_alarm_range

method in Unit

- 描述

    设置单位警戒范围

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | number | 警戒范围 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_unit_alarm_range(1.0)
```

---

## api_get_unit_alarm_range

method in Unit

- 描述

    获取单位警戒范围

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 警戒范围 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_unit_alarm_range()
```

---

## api_set_unit_cancel_alarm_range

method in Unit

- 描述

    设置单位取消警戒范围

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | number | 取消警戒范围 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_unit_cancel_alarm_range(1.0)
```

---

## api_get_unit_cancel_alarm_range

method in Unit

- 描述

    获取单位取消警戒范围

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 取消警戒范围 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_unit_cancel_alarm_range()
```

---

## api_get_unit_bar_cnt

method in Unit

- 描述

    获取单位物品栏数量

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 数量 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_unit_bar_cnt()
```

---

## api_get_unit_pkg_cnt

method in Unit

- 描述

    获取单位背包栏数量

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 数量 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_unit_pkg_cnt()
```

---

## api_get_unit_collision_radius

method in Unit

- 描述

    获取单位动态碰撞半径

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 动态碰撞半径 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_unit_collision_radius()
```

---

## api_get_unit_reward_exp

method in Unit

- 描述

    获取单位被击杀经验

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 经验值 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_unit_reward_exp()
```

---

## api_get_unit_reward_res

method in Unit

- 描述

    获取单位被击杀的玩家属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | res_key | py.RoleResKey | 玩家属性资源 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 经验值 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local role_res_key = "res_key"

local result = unit.handle:api_get_unit_reward_res(role_res_key)
```

---

## api_set_unit_reward_exp

method in Unit

- 描述

    设置单位被击杀经验

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | res_value | py.Fixed | 经验值 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_unit_reward_exp(Fix32(1))
```

---

## api_set_unit_reward_res

method in Unit

- 描述

    设置单位被击杀的玩家属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | res_key | py.RoleResKey | 玩家属性资源 |
    | res_value | py.Fixed | 经验值 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local role_res_key = "res_key"

unit.handle:api_set_unit_reward_res(role_res_key, Fix32(1))
```

---

## api_get_unit_shield_value

method in Unit

- 描述

    获取单位的护盾值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | shield_type | integer | 护盾类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 护盾值 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_unit_shield_value(1)
```

---

## api_set_unit_icon

method in Unit

- 描述

    设置单位的头像

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon | py.Texture | 图片 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_unit_icon(1)
```

---

## api_get_unit_main_attr

method in Unit

- 描述

    获取单位主属性

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string? | 属性 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_unit_main_attr()
```

---

## api_stop_move

method in Unit

- 描述

    单位停止移动

- 参数

    无

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_stop_move()
```

---

## api_transmit

method in Unit

- 描述

    单位传送到指定坐标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.FVector3 | 目标坐标 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

unit.handle:api_transmit(fvector3)
```

---

## api_force_transmit

method in Unit

- 描述

    单位强制传送到指定坐标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | pos | py.FVector3 | 目标坐标 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

unit.handle:api_force_transmit(fvector3)
```

---

## api_force_transmit_new

method in Unit

- 描述

    单位强制传送到指定坐标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | pos | py.FVector3 | 目标坐标 |
    | interpolation? | boolean | 是否平滑 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

unit.handle:api_force_transmit_new(fvector3, true)
```

---

## api_set_face_dir

method in Unit

- 描述

    单位设置朝向

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | face_dir | py.FVector3 | 朝向 |
    | speed_effect? | boolean | 是否受转身速度影响 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

unit.handle:api_set_face_dir(fvector3, true)
```

---

## api_set_face_angle

method in Unit

- 描述

    单位设置朝向角度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | face_angle | py.Fixed | 朝向角度 |
    | turn_time_ms? | integer | 转身时间毫秒 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_face_angle(Fix32(1), 1)
```

---

## api_set_face_angle_inner_usage

method in Unit

- 描述

    单位设置朝向角度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | face_angle | py.Fixed | 朝向角度 |
    | turn_type? | integer | 动画旋转类型 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_face_angle_inner_usage(Fix32(1), 1)
```

---

## api_can_teleport_to

method in Unit

- 描述

    单位是否能传送到目标点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | pos | py.FVector3 | 目标点 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 单位是否能传送到目标点 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

local result = unit.handle:api_can_teleport_to(fvector3)
```

---

## api_find_nearest_valid_position

method in Unit

- 描述

    获取单位在目标点附近的最近可通行点

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3? | 最近可通行点 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_find_nearest_valid_position()
```

---

## api_get_position

method in Unit

- 描述

    获取单位位置

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3? | 单位位置 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_position()
```

---

## api_get_face_dir

method in Unit

- 描述

    获取单位朝向

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3? | 单位朝向 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_face_dir()
```

---

## get_face_angle

method in Unit

- 描述

    获取单位面向角度

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 单位面向角度 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:get_face_angle()
```

---

## api_set_turn_speed

method in Unit

- 描述

    设置单位转身速度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | turn_speed | py.Fixed | 转身速度 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_turn_speed(Fix32(1))
```

---

## api_get_turn_speed

method in Unit

- 描述

    获得单位转身速度

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 转身速度 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_turn_speed()
```

---

## api_is_moving

method in Unit

- 描述

    单位是否在移动

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 是否在移动 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_is_moving()
```

---

## api_get_move_collision

method in Unit

- 描述

    获取单位是否计算某种碰撞类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | collision_layer | integer | 碰撞mask |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 是否开启 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_move_collision(1)
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
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:set_move_channel_land(true, true, true)
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
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:set_move_channel_air(true)
```

---

## get_unit_path_length_between_points

method in Unit

- 描述

    获取单位从点到点的寻路距离

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point_start | py.Unit | 单位 |
    | point_end | py.Point | 起始点 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local point = Fix32Vec3(0, 0, 0)

unit.handle:get_unit_path_length_between_points(unit.handle, point)
```

---

## api_play_animation

method in Unit

- 描述

    播放动画

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | name | string | 动画名称 |
    | rate? | number | 播放倍率 |
    | init_time? | number | 开始时间(s) |
    | end_time? | number | 结束时间(s)，正数 -1 表示不结束 |
    | loop? | boolean | 是否循环 |
    | return_idle? | boolean | 播放结束后是否恢复idle |
    | transition_time? | number | 过渡时间(s)，负数代表用全局默认值 |
    | force_play? | boolean | 即使死了也播播 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_play_animation("name", 1.0, 1.0, 1.0, true, true, 1.0, true)
```

---

## api_play_animation_inner_usage

method in Unit

- 描述

    播放动画 内部

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | name | string | 动画名称 |
    | turn_type? | number | 播放倍率 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_play_animation_inner_usage("name", 1.0)
```

---

## api_set_animation_graph_inner_usage

method in Unit

- 描述

    设置动画graph 内部

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | animation_graph_path | string | 动画graph路径 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_animation_graph_inner_usage("animation_graph_path")
```

---

## api_stop_animation

method in Unit

- 描述

    停止播放动画

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | name | string | 动画名称 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_stop_animation("name")
```

---

## api_stop_cur_animation

method in Unit

- 描述

    停止当前正在播放的动画

- 参数

    无

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_stop_cur_animation()
```

---

## api_set_animation_speed

method in Unit

- 描述

    设置动画速度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | speed | py.Fixed | 速度 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_animation_speed(Fix32(1))
```

---

## api_play_sfx

method in Unit

- 描述

    单位播放特效

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | socket_name | string | 挂节点名字 |
    | sfx_res_id | py.SfxKey | 特效编号 |
    | keep_time | py.Fixed | 持续时间，单位：秒 |
    | scale? | number | 缩放比例 |
    | inherit_pos? | boolean | 是否跟随单位位置 |
    | inherit_rotate? | boolean | 是否跟随单位旋转 |
    | inherit_scale? | boolean | 是否跟随缩放 |
    | role? | py.Role | 所属单位 |
    | visible_type? | py.SfxVisibleType | 可见性规则 |
    | rotation? | number | 初始旋转 角度制 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)
local sfx_key = 134274569

unit.handle:api_play_sfx("socket_name", sfx_key, Fix32(1), 1.0, true, true, true, nil, 1, 1.0)
```

---

## api_unit_play_sfx_on_socket

method in Unit

- 描述

    在单位挂接点播放特效

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | socket_name | string | 挂节点名字 |
    | sfx_id | py.SfxKey | 特效编号 |
    | keep_time | py.Fixed | 持续时间，单位：秒 |
    | scale? | number | 缩放比例 |
    | inherit_rotate? | boolean | 是否跟随单位旋转 |
    | inherit_scale? | boolean | 是否跟随缩放 |
    | role? | py.Role | 所属玩家 |
    | visible_type? | py.SfxVisibleType | 可见性规则 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)
local sfx_key = 134274569

unit.handle:api_unit_play_sfx_on_socket("socket_name", sfx_key, Fix32(1), 1.0, true, true, nil, 1)
```

---

## api_play_sfx_with_return

method in Unit

- 描述

    在单位上播放特效并返回特效实体

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | socket_name | string | 挂节点名字 |
    | sfx_res_id | py.SfxKey | 特效编号 |
    | keep_time | py.Fixed | 持续时间，单位：秒 |
    | scale? | number | 缩放比例 |
    | inherit_pos? | boolean | 是否跟随单位位置 |
    | inherit_rotate? | boolean | 是否跟随单位旋转 |
    | inherit_scale? | boolean | 是否跟随缩放 |
    | role? | py.Role | 所属单位 |
    | visible_type? | py.SfxVisibleType | 可见性规则 |
    | rotation? | number | 初始旋转 角度制 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sfx? | 特效 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)
local sfx_key = 134274569

local result = unit.handle:api_play_sfx_with_return("socket_name", sfx_key, Fix32(1), 1.0, true, true, true, nil, 1, 1.0)
```

---

## api_change_animation

method in Unit

- 描述

    单位替换播放动画

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | target_ani | string | 目标动画名字 |
    | source_ani | string | 原动画名字 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_change_animation("target_ani", "source_ani")
```

---

## api_cancel_change_animation

method in Unit

- 描述

    取消单位替换播放动画

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | target_ani | string | 目标动画名字 |
    | source_ani | string | 原动画名字 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_cancel_change_animation("target_ani", "source_ani")
```

---

## api_clear_change_animation

method in Unit

- 描述

    取消单位所有替换播放动画

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | source_ani | string | 原动画名字 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_clear_change_animation("source_ani")
```

---

## api_change_model

method in Unit

- 描述

    单位替换模型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | target_model | py.ModelKey | 目标模型编号 |
    | source_model | py.ModelKey | 原模型编号 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local model_key = 1

unit.handle:api_change_model(model_key, model_key)
```

---

## api_cancel_change_model

method in Unit

- 描述

    取消单位替换模型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | target_model | py.ModelKey | 目标模型编号 |
    | source_model | py.ModelKey | 原模型编号 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local model_key = 1

unit.handle:api_cancel_change_model(model_key, model_key)
```

---

## api_clear_change_model

method in Unit

- 描述

    取消单位所有替换模型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | source_model | py.ModelKey | 原模型编号 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local model_key = 1

unit.handle:api_clear_change_model(model_key)
```

---

## api_replace_model

method in Unit

- 描述

    单位替换模型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | target_model | py.ModelKey | 目标模型编号 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local model_key = 1

unit.handle:api_replace_model(model_key)
```

---

## api_cancel_replace_model

method in Unit

- 描述

    取消单位替换模型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | target_model | py.ModelKey | 目标模型名字 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local model_key = 1

unit.handle:api_cancel_replace_model(model_key)
```

---

## api_show_health_bar_count_down

method in Unit

- 描述

    显示血条倒计时

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | left_time | py.Fixed | 倒计时时长, 单位秒 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_show_health_bar_count_down(Fix32(1))
```

---

## api_get_model

method in Unit

- 描述

    获取单位模型

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModelKey? | 模型编号 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_model()
```

---

## api_get_source_model

method in Unit

- 描述

    获取单位原模型

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModelKey? | 模型编号 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_source_model()
```

---

## api_show_text

method in Unit

- 描述

    显示单位头顶文本

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | text | string | 显示信息 |
    | second | py.Fixed | 持续时间, 单位秒 |
    | localize? | integer | 多语言环境 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_show_text("text", Fix32(1), 1)
```

---

## api_set_title

method in Unit

- 描述

    更改单位称号

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | title_str | string | 称号 |
    | localize? | boolean | 多语言转化 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_title("title_str", true)
```

---

## api_set_title_visible

method in Unit

- 描述

    设置单位称号可见性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | visible | boolean | 是否显示 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_title_visible(true)
```

---

## api_set_name_visible

method in Unit

- 描述

    隐藏显示单位名称,对于无头顶UI的单位该API不生效,每次隐藏计数+1,每次显示计数-1,计数归零显示单位名称

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | visible | boolean | 是否显示 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_name_visible(true)
```

---

## api_set_bar_name_visible

method in Unit

- 描述

    隐藏显示单位名称,对于无头顶UI的单位该API不生效,每次隐藏计数+1,每次显示计数-1,计数归零显示单位名称

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | visible | boolean | 是否显示 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_bar_name_visible(true)
```

---

## api_set_bar_name

method in Unit

- 描述

    设置血条显示名字

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | name | string | 名字 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_bar_name("name")
```

---

## set_bar_name_scale

method in Unit

- 描述

    设置血条显示名字缩放

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | scale | number | 缩放 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:set_bar_name_scale(1.0)
```

---

## api_set_bar_name_font_type

method in Unit

- 描述

    设置血条显示名字字体

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | font_name | string | 字体名称 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_bar_name_font_type("font_name")
```

---

## api_set_bar_name_font_size

method in Unit

- 描述

    设置血条显示名字字体大小

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | size | integer | 字号 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_bar_name_font_size(1)
```

---

## api_set_bar_text_visible

method in Unit

- 描述

    隐藏显示单位头顶文本,每次隐藏计数+1,每次显示计数-1,计数归零显示单位头顶文本

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | visible | boolean | 是否显示 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_bar_text_visible(true)
```

---

## api_set_bar_text_scale

method in Unit

- 描述

    设置头顶显示文字缩放

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | scale | number | 缩放 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_bar_text_scale(1.0)
```

---

## api_set_bar_text_type

method in Unit

- 描述

    设置头顶显示文字类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | bar_text_type | integer | 类型 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_bar_text_type(1)
```

---

## api_set_bar_text_font_type

method in Unit

- 描述

    设置头顶显示文字字体

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | font_type | string | 字体 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_bar_text_font_type("font_type")
```

---

## api_set_bar_text_font_size

method in Unit

- 描述

    设置头顶显示文字字号

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | font_size | integer | 字号 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_bar_text_font_size(1)
```

---

## api_set_bar_name_show_type

method in Unit

- 描述

    设置血条名称显示样式

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | t | integer | 样式,具体参见**HeadBarShowNameType** |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_bar_name_show_type(1)
```

---

## api_set_hp_bar_visible

method in Unit

- 描述

    隐藏显示单位血条,对于无头顶UI的单位该API不生效,每次隐藏计数+1,每次显示计数-1,计数归零显示单位血条

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | visible | boolean | 是否显示 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_hp_bar_visible(true)
```

---

## api_set_hp_bar_show_type

method in Unit

- 描述

    设置单位血条显示样式,对于无头顶UI的单位该API不生效

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | t | integer | 显示样式,具体参见**HeadBarShowType** |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_hp_bar_show_type(1)
```

---

## api_set_hp_bar_type

method in Unit

- 描述

    设置单位血条样式,对于无头顶UI的单位该API不生效

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | t | integer | 血条样式 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_hp_bar_type(1)
```

---

## api_add_ui_comp

method in Unit

- 描述

    绑定UI控件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ui_comp | py.WorldUINode | UI控件 |
    | socket_name | string | 挂接点(需确认模型拥有该挂接点,挂接点可在模型属性中查看,具体挂接点类型参见**ModelSocket**) |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_add_ui_comp("ui_comp", "socket_name")
```

---

## api_change_title_font_size

method in Unit

- 描述

    修改单位称号字号

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | font_size | integer | 字号 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_change_title_font_size(1)
```

---

## api_change_title_scale

method in Unit

- 描述

    修改单位称号缩放

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | scale | number | 缩放比例 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_change_title_scale(1.0)
```

---

## api_change_title_font_type

method in Unit

- 描述

    修改单位称号字体

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | font_name | string | 字体 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_change_title_font_type("font_name")
```

---

## api_change_title_type

method in Unit

- 描述

    修改单位称号样式

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | style_type | integer | 称号样式 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_change_title_type(1)
```

---

## api_set_title_bg_opacity

method in Unit

- 描述

    修改单位称号背景不透明度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | opacity | number | 不透明度 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_title_bg_opacity(1.0)
```

---

## api_set_title_bg_scale

method in Unit

- 描述

    修改单位称号背景缩放

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | scale | number | 缩放 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_title_bg_scale(1.0)
```

---

## api_set_blood_scale_visible

method in Unit

- 描述

    修改单位血条刻度可见性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | visible | boolean | 可见性 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_blood_scale_visible(true)
```

---

## api_set_title_bar_pos_offset

method in Unit

- 描述

    修改单位称号位置偏移

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | offset | py.Vector2 | 位置偏移 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_title_bar_pos_offset("offset")
```

---

## api_set_hp_bar_pos_offset

method in Unit

- 描述

    修改单位血条位置偏移

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | offset | py.Vector2 | 位置偏移 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_hp_bar_pos_offset("offset")
```

---

## api_set_name_bar_pos_offset

method in Unit

- 描述

    修改单位名称位置偏移

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | offset | py.Vector2 | 位置偏移 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_name_bar_pos_offset("offset")
```

---

## api_set_text_bar_pos_offset

method in Unit

- 描述

    修改单位文本位置偏移

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | offset | py.Vector2 | 位置偏移 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_text_bar_pos_offset("offset")
```

---

## api_set_countdown_bar_pos_offset

method in Unit

- 描述

    修改单位倒计时位置偏移

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | offset | py.Vector2 | 位置偏移 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_countdown_bar_pos_offset("offset")
```

---

## api_raise_height

method in Unit

- 描述

    单位抬高

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | y | py.Fixed | 抬高高度 |
    | dt | py.Fixed | 时间 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_raise_height(Fix32(1), Fix32(1))
```

---

## api_get_height

method in Unit

- 描述

    获取单位高度

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 模型高度 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_height()
```

---

## api_set_scale

method in Unit

- 描述

    设置单位缩放

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | scale | number | 缩放 |
    | duration? | number | 过渡时间 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_scale(1.0, 1.0)
```

---

## api_set_unit_scale

method in Unit

- 描述

    设置单位三轴缩放

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | scale_x | number | x缩放 |
    | scale_y | number | y缩放 |
    | scale_z | number | z缩放 |
    | duration? | number | 过渡时间 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_unit_scale(1.0, 1.0, 1.0, 1.0)
```

---

## api_get_scale

method in Unit

- 描述

    获取单位缩放

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 获取缩放 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_scale()
```

---

## api_get_model_scale

method in Unit

- 描述

    获取单位模型缩放

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 获取缩放 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_model_scale()
```

---

## api_set_blood_bar_type

method in Unit

- 描述

    修改单位血条样式

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | blood_bar_type | integer | 血条样式 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_blood_bar_type(1)
```

---

## api_set_blood_bar_show_type

method in Unit

- 描述

    修改单位血条显示模式

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | blood_bar_show_type | integer | 血条显示模式 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_blood_bar_show_type(1)
```

---

## api_start_ghost

method in Unit

- 描述

    开启残影

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | r? | py.Fixed | r |
    | g? | py.Fixed | g |
    | b? | py.Fixed | b |
    | a? | py.Fixed | a |
    | interval? | py.Fixed | interval |
    | duration? | py.Fixed | duration |
    | start? | py.Fixed | start |
    | end_? | py.Fixed | end |
    | use_raw_texture? | boolean | Use origin texture |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_start_ghost(Fix32(1), Fix32(1), Fix32(1), Fix32(1), Fix32(1), Fix32(1), Fix32(1), Fix32(1), true)
```

---

## api_stop_ghost

method in Unit

- 描述

    关闭残影

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destroy_immediately? | boolean | 立即销毁 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_stop_ghost(true)
```

---

## api_start_dissolve

method in Unit

- 描述

    开始溶解效果

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | dissolve_time | py.Fixed | 溶解时间 |
    | sink_dis | py.Fixed | 下沉距离 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_start_dissolve(Fix32(1), Fix32(1))
```

---

## api_stop_dissolve

method in Unit

- 描述

    关闭溶解效果

- 参数

    无

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_stop_dissolve()
```

---

## api_set_ghost_color

method in Unit

- 描述

    设置残影颜色

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | r | py.Fixed | r |
    | g | py.Fixed | g |
    | b | py.Fixed | b |
    | a | py.Fixed | a |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_ghost_color(Fix32(1), Fix32(1), Fix32(1), Fix32(1))
```

---

## api_set_ghost_time

method in Unit

- 描述

    设置残影时间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | interval | py.Fixed | interval |
    | duration | py.Fixed | duration |
    | start | py.Fixed | start |
    | end_ | py.Fixed | end |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_ghost_time(Fix32(1), Fix32(1), Fix32(1), Fix32(1))
```

---

## api_play_sound_by_unit_for_role_relation

method in Unit

- 描述

    对单位所属玩家关系播放音乐

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
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local relation = 1
local audio_key = 134274569

unit.handle:api_play_sound_by_unit_for_role_relation(relation, audio_key, true)
```

---

## api_set_Xray_is_open

method in Unit

- 描述

    设置XRay是否开启

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | boolean | 布尔值 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_Xray_is_open(true)
```

---

## api_set_transparent_when_invisible

method in Unit

- 描述

    设置单位隐身被探测到时是否半透明

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | boolean | 布尔值 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_transparent_when_invisible(true)
```

---

## api_set_mini_map_icon

method in Unit

- 描述

    设置单位小地图头像

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon | py.Texture | 图片 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_mini_map_icon(1)
```

---

## api_set_enemy_mini_map_icon

method in Unit

- 描述

    设置敌方单位小地图头像

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon | py.Texture | 图片 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_enemy_mini_map_icon(1)
```

---

## api_set_unit_select_effect_visible

method in Unit

- 描述

    设置单位选择框的可见性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | boolean | 布尔值 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_unit_select_effect_visible(true)
```

---

## api_active_gm1_look_at_camera

method in Unit

- 描述

    开关阴阳师模型IDLE时看向摄像机是否开启

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | value | boolean | 布尔值 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

unit.handle:api_active_gm1_look_at_camera(player.handle, true)
```

---

## api_set_disk_shadow_open

method in Unit

- 描述

    设置单位圆盘阴影开关

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_open | boolean | 布尔值 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_disk_shadow_open(true)
```

---

## api_set_unit_disk_shadow_size

method in Unit

- 描述

    设置单位圆盘阴影大小

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | shadow_size | number | 大小 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_unit_disk_shadow_size(1.0)
```

---

## api_add_modifier

method in Unit

- 描述

    单位添加指定编号的效果

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 效果编号 |
    | from_unit? | py.Unit | 来源单位对象 |
    | from_ability? | py.Ability | 关联技能 |
    | time? | py.Fixed | 持续时间 |
    | cycle_time? | py.Fixed | 循环周期 |
    | stack_count? | integer | 效果层数 |
    | lua_table? | py.Table | 用户自定义配置表 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierEntity? | 魔法效果 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)
local modifier_key = 134274569
local tbl = {}

local result = unit.handle:api_add_modifier(modifier_key, nil, nil, Fix32(1), Fix32(1), 1)
```

---

## api_get_modifier_stack_count

method in Unit

- 描述

    获取单位身上指定编号的的效果层数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 效果编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 效果层数 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier_key = 134274569

local result = unit.handle:api_get_modifier_stack_count(modifier_key)
```

---

## api_has_modifier

method in Unit

- 描述

    单位身上是否拥有指定编号的效果

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 效果编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 单位身上是否有指定编号的效果 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier_key = 134274569

local result = unit.handle:api_has_modifier(modifier_key)
```

---

## api_has_modifier_with_tag

method in Unit

- 描述

    单位身上是否拥有指定标签的效果

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | 标签 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 单位身上是否拥有指定标签的效果 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_has_modifier_with_tag("tag")
```

---

## api_get_modifier

method in Unit

- 描述

    获取单位身上指定编号的第i个效果实例

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | add_index | integer | 效果位置 |
    | modifier_key | py.ModifierKey | 效果编号 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier_key = 134274569

unit.handle:api_get_modifier(1, modifier_key)
```

---

## api_get_modifier_count

method in Unit

- 描述

    获取单位身上指定编号的第i个效果的个数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 效果编号 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier_key = 134274569

unit.handle:api_get_modifier_count(modifier_key)
```

---

## api_remove_modifier_instance

method in Unit

- 描述

    移除目标单位身上的目标modifier实例

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tar_modifier | py.ModifierEntity | 效果编号 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

unit.handle:api_remove_modifier_instance(modifier.handle)
```

---

## api_remove_modifier_type

method in Unit

- 描述

    移除目标单位身上的目标modifier类型的所有实例

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 效果编号 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier_key = 134274569

unit.handle:api_remove_modifier_type(modifier_key)
```

---

## api_has_modifier_type

method in Unit

- 描述

    单位身上是否拥有指定类别的效果

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_effect_type | py.ModifierEffectType | 魔法效果类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 单位身上是否拥有指定类型的魔法效果 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_has_modifier_type(1)
```

---

## api_delete_all_modifiers_by_effect_type

method in Unit

- 描述

    删除单位指定影响类型的魔法效果

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | effect_type | py.ModifierEffectType | 效果影响类型 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_delete_all_modifiers_by_effect_type(1)
```

---

## api_get_all_modifiers

method in Unit

- 描述

    获取单位身上所有的魔法效果

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierEntity? | 魔法效果 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_all_modifiers()
```

---

## api_add_ability

method in Unit

- 描述

    单位添加技能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_type | py.AbilityType | 技能类型 |
    | ability_id | py.AbilityKey | 技能编号 |
    | ability_index? | py.AbilityIndex | 技能槽位编号 |
    | ability_level? | integer | 技能等级 |
    | lua_table? | py.Table | 用户自定义配置表 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Ability? | 技能 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability_type = y3.const.AbilityType.HERO
local ability_key = 134274569
local ability_index = 0
local tbl = {}

local result = unit.handle:api_add_ability(ability_type, ability_key, nil, 1)
```

---

## api_remove_ability_by_index

method in Unit

- 描述

    单位根据槽位移除技能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_type | integer | 技能类型 |
    | ability_index | integer | 技能槽位 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_remove_ability_by_index(1, 1)
```

---

## api_remove_abilities_in_type

method in Unit

- 描述

    单位移除某种类型里所有是指定技能ID的技能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_type | integer | 技能类型 |
    | ability_id | py.AbilityKey | 技能ID |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability_key = 134274569

unit.handle:api_remove_abilities_in_type(1, ability_key)
```

---

## api_set_ability_level

method in Unit

- 描述

    单位设置技能等级。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modify | integer | 修改方式 |
    | ability_type | py.AbilityType | 技能类型 |
    | ability_index | py.AbilityIndex | 技能槽位 |
    | level | integer | 技能等级 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability_type = y3.const.AbilityType.HERO
local ability_index = 0

unit.handle:api_set_ability_level(1, ability_type, ability_index, 1)
```

---

## api_unit_learn_ability

method in Unit

- 描述

    单位学习技能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能类型 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability_key = 134274569

unit.handle:api_unit_learn_ability(ability_key)
```

---

## api_get_ability_point

method in Unit

- 描述

    获取英雄的技能点

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 技能点 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_ability_point()
```

---

## api_set_ability_point

method in Unit

- 描述

    设置英雄的技能点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_point | integer | 技能点 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_ability_point(1)
```

---

## api_add_ability_point

method in Unit

- 描述

    增加英雄的技能点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | integer | 技能点 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_add_ability_point(1)
```

---

## api_get_ability

method in Unit

- 描述

    通过技能槽位获取技能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_type | py.AbilityType | 技能类型 |
    | ability_index | py.AbilityIndex | 技能槽位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Ability? | 技能对象 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability_type = y3.const.AbilityType.HERO
local ability_index = 0

local result = unit.handle:api_get_ability(ability_type, ability_index)
```

---

## api_get_ability_by_type

method in Unit

- 描述

    通过技能类型加技能ID获取技能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_type | py.AbilityType | 技能类型 |
    | ability_id | py.AbilityKey | 技能编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Ability? | 技能对象 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability_type = y3.const.AbilityType.HERO
local ability_key = 134274569

local result = unit.handle:api_get_ability_by_type(ability_type, ability_key)
```

---

## api_get_abilities_by_type

method in Unit

- 描述

    获取某种类型的技能列表

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_type | py.AbilityType | 技能类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Ability? | 技能对象 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability_type = y3.const.AbilityType.HERO

local result = unit.handle:api_get_abilities_by_type(ability_type)
```

---

## api_check_has_ability_type

method in Unit

- 描述

    是否有对应技能类型的技能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_id | py.AbilityKey | 技能类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 是否有对应技能类型的技能 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability_key = 134274569

local result = unit.handle:api_check_has_ability_type(ability_key)
```

---

## api_get_all_abilities_can_show

method in Unit

- 描述

    获取单位技能列表

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Ability? | 技能对象 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_all_abilities_can_show()
```

---

## api_switch_ability_by_index

method in Unit

- 描述

    根据坑位交换技能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_1_type | py.AbilityType | 技能类型 |
    | ability_1_index | py.AbilityIndex | 技能槽位 |
    | ability_2_type | py.AbilityType | 技能类型 |
    | ability_2_index | py.AbilityIndex | 技能槽位 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability_type = y3.const.AbilityType.HERO
local ability_index = 0

unit.handle:api_switch_ability_by_index(ability_type, ability_index, ability_type, ability_index)
```

---

## api_switch_ability

method in Unit

- 描述

    交换技能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_1 | py.Ability | 技能 |
    | ability_2 | py.Ability | 技能 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

unit.handle:api_switch_ability(ability.handle, ability.handle)
```

---

## api_disable_ability

method in Unit

- 描述

    单位禁用技能。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_type | py.AbilityType | 技能类型 |
    | ability_index | py.AbilityIndex | 技能槽位 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability_type = y3.const.AbilityType.HERO
local ability_index = 0

unit.handle:api_disable_ability(ability_type, ability_index)
```

---

## api_enable_ability

method in Unit

- 描述

    单位解禁技能。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_type | py.AbilityType | 技能类型 |
    | ability_index | py.AbilityIndex | 技能槽位 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability_type = y3.const.AbilityType.HERO
local ability_index = 0

unit.handle:api_enable_ability(ability_type, ability_index)
```

---

## api_stop_all_abilities

method in Unit

- 描述

    停止单位所有技能

- 参数

    无

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_stop_all_abilities()
```

---

## api_unit_has_running_ability

method in Unit

- 描述

    单位是否有正在释放的技能

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 是否有正在释放的技能 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_unit_has_running_ability()
```

---

## api_get_ability_str_attr_value

method in Unit

- 描述

    返回单位实体指定槽位技能的字符串属性值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_type | py.AbilityType | 技能类型 |
    | ability_index | py.AbilityIndex | 技能槽位 |
    | prop | string | 属性名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string? | 字符 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability_type = y3.const.AbilityType.HERO
local ability_index = 0

local result = unit.handle:api_get_ability_str_attr_value(ability_type, ability_index, "prop")
```

---

## api_get_ability_by_seq

method in Unit

- 描述

    根据技能序号获取技能对象

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | seq | py.AbilitySeq | 技能序号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Ability? | 技能对象 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_ability_by_seq(1)
```

---

## api_add_state

method in Unit

- 描述

    给单位施加状态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | state_id | integer | 状态ID |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_add_state(1)
```

---

## api_remove_state

method in Unit

- 描述

    给单位去除状态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | state_id | integer | 状态ID |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_remove_state(1)
```

---

## api_is_in_battle_state

method in Unit

- 描述

    是否在战斗状态

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 是否在战斗状态 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_is_in_battle_state()
```

---

## api_has_state

method in Unit

- 描述

    单位是否处于某状态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | state_bit | integer | 状态 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 单位是否处于某状态 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_has_state(1)
```

---

## api_release_ability_by_index

method in Unit

- 描述

    单位施放技能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_type | integer | 技能类型 |
    | ability_index | integer | 技能槽位 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_release_ability_by_index(1, 1)
```

---

## api_release_ability_at_position

method in Unit

- 描述

    单位施放技能，具有释放目标地点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_type | integer | 技能类型 |
    | ability_index | integer | 技能坑位 |
    | postion | py.Point | 技能目标位置 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local point = Fix32Vec3(0, 0, 0)

unit.handle:api_release_ability_at_position(1, 1, point)
```

---

## api_create_building_on_point

method in Unit

- 描述

    发布建造命令(目标点)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | build_key | py.UnitKey | 建筑类型 |
    | point | py.Point | 目标位置 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local point = Fix32Vec3(0, 0, 0)
local unit_key = 134274569

unit.handle:api_create_building_on_point(unit_key, point)
```

---

## api_create_building_on_position

method in Unit

- 描述

    发布建造命令(坐标)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | build_key | py.UnitKey | 建筑类型 |
    | pos_x | py.Fixed | 坐标X |
    | pos_z | py.Fixed | 坐标Z |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local unit_key = 134274569

unit.handle:api_create_building_on_position(unit_key, Fix32(1), Fix32(1))
```

---

## api_has_item

method in Unit

- 描述

    单位是否拥有物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item | py.Item | 物品 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 单位是否拥有物品 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = unit.handle:api_has_item(item.handle)
```

---

## api_has_item_key

method in Unit

- 描述

    单位是否拥有特定编号物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_no | py.ItemKey | 物品编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 单位是否拥有特定编号物品 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item_key = 134274569

local result = unit.handle:api_has_item_key(item_key)
```

---

## api_add_item

method in Unit

- 描述

    给单位添加物品名

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_no | py.ItemKey | 物品编号 |
    | slot_type? | py.SlotType | 槽位类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Item? | 创建的物品实体 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item_key = 134274569
local slot_type = y3.const.SlotType.BAR

local result = unit.handle:api_add_item(item_key)
```

---

## api_delete_item

method in Unit

- 描述

    给单位删除物品名

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | num? | integer | 数量 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item_key = 134274569

unit.handle:api_delete_item(item_key, 1)
```

---

## api_drop_item

method in Unit

- 描述

    单位丢弃物品实体到场景中

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item | py.Item | 物品 |
    | pos | py.FPoint | 点 |
    | stack_cnt | integer | 数量 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)
local fpoint = GameAPI.get_point_by_res_id(1)

unit.handle:api_drop_item(item.handle, fpoint, 1)
```

---

## api_remove_item

method in Unit

- 描述

    单位删除物品实体

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | stack_cnt | integer | 数量 |
    | item | py.Item | 物品 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

unit.handle:api_remove_item(1, item.handle)
```

---

## api_get_item_by_slot

method in Unit

- 描述

    获取单位背包槽位的物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | slot_type | py.SlotType | 背包槽位 |
    | slot_idx | integer | 格子下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Item? | 物品对象 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local slot_type = y3.const.SlotType.BAR

local result = unit.handle:api_get_item_by_slot(slot_type, 1)
```

---

## api_shift_item

method in Unit

- 描述

    移动物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item | py.Item | 物品 |
    | slot_type | py.SlotType | 背包槽位 |
    | slot_idx | integer | 格子下标 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)
local slot_type = y3.const.SlotType.BAR

unit.handle:api_shift_item(item.handle, slot_type, 1)
```

---

## api_shift_item_new

method in Unit

- 描述

    移动物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item | py.Item | 物品 |
    | slot_type | py.SlotType | 背包槽位 |
    | slot_idx? | integer | 格子下标 |
    | is_force_shift? | boolean | 格子被占是否转移 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)
local slot_type = y3.const.SlotType.BAR

unit.handle:api_shift_item_new(item.handle, slot_type, 1, true)
```

---

## api_get_all_item_pids

method in Unit

- 描述

    单位身上所有物品

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemGroup? | 物品组 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_all_item_pids()
```

---

## api_set_unit_bar_cnt

method in Unit

- 描述

    设置单位物品栏的格子数量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | cnt | integer | 个数 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_unit_bar_cnt(1)
```

---

## api_set_unit_pkg_cnt

method in Unit

- 描述

    设置单位背包栏的格子数量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | cnt | integer | 个数 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_unit_pkg_cnt(1)
```

---

## api_get_num_of_item_type

method in Unit

- 描述

    单位身上拥有指定类型的物品数量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_type | py.ItemKey | 物品编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 数量 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item_key = 134274569

local result = unit.handle:api_get_num_of_item_type(item_key)
```

---

## api_get_item_type_by_slot

method in Unit

- 描述

    获取单位持有的物品类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | slot_type | py.SlotType | 槽位类型 |
    | slot_idx | integer | 整数下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemKey? | 物品编号 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local slot_type = y3.const.SlotType.BAR

local result = unit.handle:api_get_item_type_by_slot(slot_type, 1)
```

---

## api_is_shop

method in Unit

- 描述

    单位是否商店

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 单位是否商店 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_is_shop()
```

---

## api_get_shop_range

method in Unit

- 描述

    获取商店单位范围

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 商店范围 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_shop_range()
```

---

## api_add_shop_item

method in Unit

- 描述

    添加物品商品到商店

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tab_name | py.TabName | 页签 |
    | item_no | py.ItemKey | 道具编号 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item_key = 134274569

unit.handle:api_add_shop_item("tab_name", item_key)
```

---

## api_get_shop_item_list

method in Unit

- 描述

    获取商店某页签的商品列表

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tab_idx | py.TabIdx | 页签id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List? | 道具编号 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_shop_item_list(1)
```

---

## api_get_shop_item_cd

method in Unit

- 描述

    获取商店商品的恢复时间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tab_idx | py.TabIdx | 页签id |
    | item_no | py.ItemKey | 道具编号 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item_key = 134274569

unit.handle:api_get_shop_item_cd(1, item_key)
```

---

## api_get_shop_item_default_cd

method in Unit

- 描述

    获取商店商品的库存恢复间隔

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tab_idx | py.TabIdx | 页签id |
    | item_num | integer | 第N个道具 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 恢复间隔 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_shop_item_default_cd(1, 1)
```

---

## api_get_shop_item_residual_cd

method in Unit

- 描述

    获取商店商品的剩余恢复时间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tab_idx | py.TabIdx | 页签id |
    | item_num | integer | 第N个道具 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 恢复间隔 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_shop_item_residual_cd(1, 1)
```

---

## api_get_shop_tab_cnt

method in Unit

- 描述

    获取商店页签数量

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 页签数量 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_shop_tab_cnt()
```

---

## api_get_shop_tab_name

method in Unit

- 描述

    获取商店的页签名

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tab_idx | py.TabIdx | 页签id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string? | 页签名 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_shop_tab_name(1)
```

---

## api_get_shop_tab_item_type

method in Unit

- 描述

    获取商店指定页签第N个商品的类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tab_idx | py.TabIdx | 页签id |
    | item_idx | integer | 商品编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemKey? | 物品类型 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_shop_tab_item_type(1, 1)
```

---

## api_add_shop_unit

method in Unit

- 描述

    添加单位商品到商店

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tab_name | py.TabName | 页签 |
    | entity_no | py.UnitKey | 单位编号 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local unit_key = 134274569

unit.handle:api_add_shop_unit("tab_name", unit_key)
```

---

## api_remove_shop_item

method in Unit

- 描述

    删除商店物品商品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tab_name | py.TabName | 页签 |
    | item_no | py.ItemKey | 道具编号 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item_key = 134274569

unit.handle:api_remove_shop_item("tab_name", item_key)
```

---

## api_remove_shop_unit

method in Unit

- 描述

    删除商店单位商品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tab_name | py.TabName | 页签 |
    | entity_no | py.UnitKey | 单位编号 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local unit_key = 134274569

unit.handle:api_remove_shop_unit("tab_name", unit_key)
```

---

## api_set_shop_item_stock

method in Unit

- 描述

    设置物品商品库存

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tab_name | py.TabName | 页签 |
    | item_no | py.ItemKey | 道具编号 |
    | cnt | integer | 库存 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item_key = 134274569

unit.handle:api_set_shop_item_stock("tab_name", item_key, 1)
```

---

## api_set_shop_unit_stock

method in Unit

- 描述

    设置单位商品库存

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tab_name | py.TabName | 页签 |
    | entity_no | py.UnitKey | 单位编号 |
    | cnt | integer | 库存 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local unit_key = 134274569

unit.handle:api_set_shop_unit_stock("tab_name", unit_key, 1)
```

---

## api_set_is_shop

method in Unit

- 描述

    设置商店开关

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_shop | boolean | 开关 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_is_shop(true)
```

---

## api_buy_item_with_tab_name

method in Unit

- 描述

    单位购买物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | shop_unit | py.Unit | 商店 |
    | tab_idx | py.TabIdx | 页签id |
    | item_no | py.ItemKey | 物品编号 |
    | item_num? | integer | 购买数量 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item_key = 134274569

unit.handle:api_buy_item_with_tab_name(unit.handle, 1, item_key, 1)
```

---

## api_buy_unit_with_tab_name

method in Unit

- 描述

    单位购买单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | shop_unit | py.Unit | 商店 |
    | tab_name | py.TabName | 页签 |
    | entity_no | py.UnitKey | 单位编号 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local unit_key = 134274569

unit.handle:api_buy_unit_with_tab_name(unit.handle, "tab_name", unit_key)
```

---

## api_sell_item

method in Unit

- 描述

    单位出售物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | shop_unit | py.Unit | 商店 |
    | item | py.Item | 道具 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

unit.handle:api_sell_item(unit.handle, item.handle)
```

---

## api_set_shop_target

method in Unit

- 描述

    设置商店目标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | target_unit | py.Unit | 目标 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_shop_target(unit.handle)
```

---

## api_get_shop_item_stock

method in Unit

- 描述

    获取单位商店物品商品库存

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tab_idx | py.TabIdx | 页签id |
    | item_no | py.ItemKey | 物品编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 商品库存 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item_key = 134274569

local result = unit.handle:api_get_shop_item_stock(1, item_key)
```

---

## api_get_shop_unit_stock

method in Unit

- 描述

    获取单位商店单位商品库存

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tab_name | py.TabName | 页签 |
    | entity_no | py.UnitKey | 单位编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 商品库存 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local unit_key = 134274569

local result = unit.handle:api_get_shop_unit_stock("tab_name", unit_key)
```

---

## api_get_shop_item_price

method in Unit

- 描述

    获取单位商店单位商品售价

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tab_name | py.TabName | 页签 |
    | entity_no | py.UnitKey | 单位编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 商品售价 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local unit_key = 134274569

local result = unit.handle:api_get_shop_item_price("tab_name", unit_key)
```

---

## api_shop_check_camp

method in Unit

- 描述

    玩家是否可以购买商店的物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 能否购买 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

local result = unit.handle:api_shop_check_camp(player.handle)
```

---

## api_upgrade_tech

method in Unit

- 描述

    科技升级

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_no | py.TechKey | 科技编号 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local tech_key = 134274569

unit.handle:api_upgrade_tech(tech_key)
```

---

## api_get_tech_list

method in Unit

- 描述

    获取科技列表

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List? | 科技编号 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_tech_list()
```

---

## api_get_affect_techs

method in Unit

- 描述

    获取科技列表

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List? | 科技编号 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_affect_techs()
```

---

## api_check_tech_precondition

method in Unit

- 描述

    获取科技是否满足前置条件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_no | py.TechKey | 科技编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.TechKey? | 科技编号 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local tech_key = 134274569

local result = unit.handle:api_check_tech_precondition(tech_key)
```

---

## api_add_tech

method in Unit

- 描述

    添加科技

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_no | py.TechKey | 科技编号 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local tech_key = 134274569

unit.handle:api_add_tech(tech_key)
```

---

## api_remove_tech

method in Unit

- 描述

    删除科技

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_no | py.TechKey | 科技编号 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local tech_key = 134274569

unit.handle:api_remove_tech(tech_key)
```

---

## api_release_command

method in Unit

- 描述

    发布命令

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | command | py.UnitCommand | 命令 |
    | enqueue? | boolean | 是否进队列 |
    | load_ai_directly? | boolean | 是否直接加载ai |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local unit_command = unit.handle:api_release_command_stop()

unit.handle:api_release_command(unit_command, true, true)
```

---

## api_set_default_switch_behavior

method in Unit

- 描述

    单位 - 设置默认跳转状态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | behavior | py.UnitBehavior | 默认跳转状态 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local unit_behavior = "unit_behavior"

unit.handle:api_set_default_switch_behavior(unit_behavior)
```

---

## api_set_construction_progress

method in Unit

- 描述

    设置单位建造进度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | progress | py.Fixed | 建造进度 |
    | is_percent? | boolean | 是否百分比 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_construction_progress(Fix32(1), true)
```

---

## api_set_upgrade_progress

method in Unit

- 描述

    设置单位升级进度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | progress | py.Fixed | 升级进度 |
    | is_percent? | boolean | 是否百分比 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_upgrade_progress(Fix32(1), true)
```

---

## api_set_ai_exit_follow_on_succ_once

method in Unit

- 描述

    设置跟随单位成功后是否退出跟随

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | exit_follow_on_succ | boolean | 是否退出 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_ai_exit_follow_on_succ_once(true)
```

---

## api_set_is_sleeping

method in Unit

- 描述

    设置单位是否休眠

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_sleeping | boolean | 是否休眠 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_is_sleeping(true)
```

---

## api_get_is_sleeping

method in Unit

- 描述

    获取单位是否休眠

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 是否休眠 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_is_sleeping()
```

---

## api_get_is_in_pool

method in Unit

- 描述

    获取单位是否处于缓存池中

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | value |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_is_in_pool()
```

---

## api_unit_transformation

method in Unit

- 描述

    单位变身

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | entity_no | py.UnitKey | 新的物编ID |
    | inherit_composite_attr? | boolean | 是否继承复合属性 |
    | inherit_unit_attr? | boolean | 是否继承单位属性 |
    | inherit_kv? | boolean | 是否继承kv |
    | inherit_hero_ability? | boolean | 是否继承英雄技能 |
    | inherit_common_ability? | boolean | 是否继承通用技能 |
    | inherit_passive_ability? | boolean | 是否继承隐藏技能 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local unit_key = 134274569

unit.handle:api_unit_transformation(unit_key, true, true, true, true, true, true)
```

---

## api_queue_reset

method in Unit

- 描述

    单位-队列重置

- 参数

    无

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_queue_reset()
```

---

## api_switch_main_attr

method in Unit

- 描述

    切换主属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | main_attr | string | 属性名 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_switch_main_attr("main_attr")
```

---

## api_open_attr_cheating_detected

method in Unit

- 描述

    开启单位属性作弊检查

- 参数

    无

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_open_attr_cheating_detected()
```

---

## api_get_attr_name

method in Unit

- 描述

    获取单位属性本地化名

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr_key | string | 属性索引 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string? | 属性本地化名 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_attr_name("attr_key")
```

---

## api_set_changed_exp_in_event

method in Unit

- 描述

    设置事件中的经验值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | val | py.Fixed | 经验值 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_changed_exp_in_event(Fix32(1))
```

---

## api_get_abilityKey_by_type_and_index

method in Unit

- 描述

    获取单位类型某个技能位的技能类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | abilityType | py.AbilityType | 技能类型 |
    | abilityIndex | py.AbilityIndex | 技能槽位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityKey? | 技能类型 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability_type = y3.const.AbilityType.HERO
local ability_index = 0

local result = unit.handle:api_get_abilityKey_by_type_and_index(ability_type, ability_index)
```

---

## api_get_hprec_pertick

method in Unit

- 描述

    获取每tick的单位生命恢复

- 参数

    无

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_get_hprec_pertick()
```

---

## api_set_unit_flying_vision

method in Unit

- 描述

    设置单位是否飞行视野

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_flying_vision | boolean | 布尔值 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_unit_flying_vision(true)
```

---

## api_set_base_speed

method in Unit

- 描述

    设置动画移动基准速度。会同时修改跑和走的基准速度，如果要区分跑和走，还需额外单独设置走的基准速度(api_set_anim_walk_speed)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | base_speed | py.Fixed | 动画移动速度 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_base_speed(Fix32(1))
```

---

## api_set_anim_walk_speed

method in Unit

- 描述

    设置动画移动基准速度(仅走)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | speed | py.Fixed | 动画移动速度 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_anim_walk_speed(Fix32(1))
```

---

## api_is_picking_item

method in Unit

- 描述

    单位是否在执行拾取物品命令

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 是否在执行命令 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_is_picking_item()
```

---

## api_is_move_type

method in Unit

- 描述

    判断单位的移动类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | move_type | integer | 移动类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 是否为该移动类型 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_is_move_type(1)
```

---

## api_set_block_others

method in Unit

- 描述

    设置是否阻挡其他单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_on | boolean | 是否阻挡 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_block_others(true)
```

---

## api_set_lock_yaw

method in Unit

- 描述

    开启锁定移动

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | angle_or_target | number | 角度 |
    | turn_time_ms? | number | 转身时间 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_lock_yaw(1.0, 1.0)
```

---

## api_set_unlock_yaw

method in Unit

- 描述

    结束锁定移动

- 参数

    无

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_unlock_yaw()
```

---

## set_joystick_base_direction

method in Unit

- 描述

    设置摇杆基方向

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | facing | number | 基方向 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:set_joystick_base_direction(1.0)
```

---

## set_joystick_input

method in Unit

- 描述

    设置摇杆输入

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | input_x | number | InputX |
    | input_y | number | InputY |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:set_joystick_input(1.0, 1.0)
```

---

## directional_move_to_pos

method in Unit

- 描述

    径直移动

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | target_pos | py.Point | 目标点 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local point = Fix32Vec3(0, 0, 0)

unit.handle:directional_move_to_pos(point)
```

---

## set_path_finding_step_bound

method in Unit

- 描述

    设置寻路消耗上限

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | step_bound | integer | 步数上限 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:set_path_finding_step_bound(1)
```

---

## set_model_by_tag

method in Unit

- 描述

    单位设置指定标签模型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | 标签 |
    | model_id | py.ModelKey | 目标模型编号 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local model_key = 1

unit.handle:set_model_by_tag("tag", model_key)
```

---

## remove_model_by_tag

method in Unit

- 描述

    单位删除设置指定标签模型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | 标签 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:remove_model_by_tag("tag")
```

---

## change_model_texture

method in Unit

- 描述

    替换模型贴图

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
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local model_key = 1

unit.handle:change_model_texture(model_key, 1, 1, 1)
```

---

## api_set_forbid_aligned_terrain

method in Unit

- 描述

    单位禁止贴地

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_forbid_aligned_terrain | boolean | 是否禁止贴地 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_forbid_aligned_terrain(true)
```

---

## api_set_scale_2

method in Unit

- 描述

    设置单位缩放

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | scale | number | 缩放 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_scale_2(1.0)
```

---

## api_start_windforce

method in Unit

- 描述

    开启风场

- 参数

    无

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_start_windforce()
```

---

## api_set_ghost_color_norm

method in Unit

- 描述

    设置残影颜色

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | r | py.Fixed | r |
    | g | py.Fixed | g |
    | b | py.Fixed | b |
    | a | py.Fixed | a |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_ghost_color_norm(Fix32(1), Fix32(1), Fix32(1), Fix32(1))
```

---

## api_set_ghost_color_hex

method in Unit

- 描述

    设置残影颜色(HEX)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | color | string | hex |
    | a | py.Fixed | a |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_ghost_color_hex("color", Fix32(1))
```

---

## api_set_unit_is_mini_map_show

method in Unit

- 描述

    小地图 - 设置单位小地图头像可见性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | boolean | 是否可见 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_unit_is_mini_map_show(true)
```

---

## api_set_unit_anim_state_name

method in Unit

- 描述

    设置单位动画状态名

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | anim_state_name | string | 状态名 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_unit_anim_state_name("anim_state_name")
```

---

## set_unit_outlined_color

method in Unit

- 描述

    设置单位的描边颜色

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
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:set_unit_outlined_color(1.0, 1.0, 1.0)
```

---

## set_unit_outlined_color_hex

method in Unit

- 描述

    设置单位的描边颜色(HEX)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | color | string | R |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:set_unit_outlined_color_hex("color")
```

---

## set_unit_outlined_enable

method in Unit

- 描述

    开关单位描边效果

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | flag | boolean | 开关 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:set_unit_outlined_enable(true)
```

---

## play_upper_body_anim

method in Unit

- 描述

    播放上半身动画

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | anim_name | string | 动画名 |
    | speed? | number | 速率 |
    | repeat_? | boolean | 是否循环 |
    | begin_t? | number | 起始时间比例（0-1之间） |
    | end_t? | number | 结束时间比例（0-1之间） |
    | ratio? | number | 融合比例（0-1之间） |
    | transition_time? | number | 过渡时间(s)，负数代表用全局默认值 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:play_upper_body_anim("anim_name", 1.0, true, 1.0, 1.0, 1.0, 1.0)
```

---

## set_bone_filter_config

method in Unit

- 描述

    自定义骨骼分层

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | root_bone | string | 根骨骼 |
    | upper_body_bone | string | 上半身骨骼 |
    | head_bone | string | 头部骨骼 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:set_bone_filter_config("root_bone", "upper_body_bone", "head_bone")
```

---

## play_additive_anim

method in Unit

- 描述

    播放叠加动画

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | anim | string | 动画名 |
    | speed | number | 速率 |
    | loop | boolean | 是否循环 |
    | begin | number | 起始时间比例（0-1之间） |
    | end_ | number | 结束时间比例（0-1之间） |
    | weight | number | 叠加权重（大于0） |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:play_additive_anim("anim", 1.0, true, 1.0, 1.0, 1.0)
```

---

## set_unit_outside_outline_width

method in Unit

- 描述

    设置单位外轮廓描边厚度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | width | number | width |
    | role? | py.Role | Role |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

unit.handle:set_unit_outside_outline_width(1.0)
```

---

## set_unit_outside_outline_color

method in Unit

- 描述

    设置单位外轮廓描边颜色

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | color_r | number | R |
    | color_g | number | G |
    | color_b | number | B |
    | role? | py.Role | Role |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

unit.handle:set_unit_outside_outline_color(1.0, 1.0, 1.0)
```

---

## set_unit_outside_outlined_enable

method in Unit

- 描述

    设置单位外轮廓描边是否开启

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | enabled | boolean | Enable |
    | role? | py.Role | Role |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

unit.handle:set_unit_outside_outlined_enable(true)
```

---

## unit_loadGraph

method in Unit

- 描述

    单位加载自定义的graph

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | graphaName | string | 动画graph文件名,不需要包含扩展名 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:unit_loadGraph("graphaName")
```

---

## unit_Graph_SetVariable

method in Unit

- 描述

    自定义Graph设置变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | VariableName | string | 变量名 |
    | VariableStr | string | 变量值为字符串形式 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:unit_Graph_SetVariable("VariableName", "VariableStr")
```

---

## unit_Graph_FireEvent

method in Unit

- 描述

    自定义Graph发送事件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | EventName | string | 事件名 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:unit_Graph_FireEvent("EventName")
```

---

## unit_Graph_SetSpeed

method in Unit

- 描述

    自定义Graph设置速度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | speedValue | string | 相对速度值 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:unit_Graph_SetSpeed("speedValue")
```

---

## unit_Graph_Pause

method in Unit

- 描述

    暂停Graph

- 参数

    无

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:unit_Graph_Pause()
```

---

## unit_Graph_RunOneFrame

method in Unit

- 描述

    暂停中跑一帧Graph

- 参数

    无

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:unit_Graph_RunOneFrame()
```

---

## api_add_multi_state

method in Unit

- 描述

    给单位施加状态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | state_id | integer | 状态ID |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_add_multi_state(1)
```

---

## api_remove_multi_state

method in Unit

- 描述

    给单位去除状态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | state_id | integer | 状态ID |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_remove_multi_state(1)
```

---

## api_get_unit_attack_interval

method in Unit

- 描述

    获取单位攻击间隔

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 攻击间隔 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_unit_attack_interval()
```

---

## api_get_unit_attack_count_per_second

method in Unit

- 描述

    获取单位每秒攻击次数

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 攻击次数 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_unit_attack_count_per_second()
```

---

## api_get_common_atk_ability

method in Unit

- 描述

    获取普攻技能

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Ability? | 普攻 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_common_atk_ability()
```

---

## api_set_simple_atk_dice_max_value

method in Unit

- 描述

    设置单位简易普攻骰子最大值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | dice_max_value | integer | 最大值 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_simple_atk_dice_max_value(1)
```

---

## api_get_simple_atk_dice_max_value

method in Unit

- 描述

    获取单位简易普攻骰子最大值

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 骰子最大值 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_simple_atk_dice_max_value()
```

---

## api_set_simple_atk_dice_count

method in Unit

- 描述

    设置单位简易普攻骰子最大值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | dice_count | integer | 最大值 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_simple_atk_dice_count(1)
```

---

## api_get_simple_atk_dice_count

method in Unit

- 描述

    获取单位简易普攻骰子个数

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 骰子最大值 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_simple_atk_dice_count()
```

---

## api_get_cur_record_ability

method in Unit

- 描述

    获取单位正在释放的技能

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Ability? | 技能 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_cur_record_ability()
```

---

## api_pause_all_ability_cd

method in Unit

- 描述

    暂停单位所有技能的CD

- 参数

    无

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_pause_all_ability_cd()
```

---

## api_resume_all_ability_cd

method in Unit

- 描述

    恢复单位所有技能的CD

- 参数

    无

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_resume_all_ability_cd()
```

---

## api_clear_all_abilities

method in Unit

- 描述

    移除单位所有技能

- 参数

    无

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_clear_all_abilities()
```

---

## api_get_slot_capacity

method in Unit

- 描述

    获取单位栏位剩余空间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | slot_type | py.SlotType | 背包槽位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 整型 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local slot_type = y3.const.SlotType.BAR

local result = unit.handle:api_get_slot_capacity(slot_type)
```

---

## api_set_default_switch_command

method in Unit

- 描述

    单位 - 设置默认跳转命令

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | command | py.UnitCommand | 默认跳转命令 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local unit_command = unit.handle:api_release_command_stop()

unit.handle:api_set_default_switch_command(unit_command)
```

---

## api_load_default_ai

method in Unit

- 描述

    单位 - 跳转到默认命令或状态

- 参数

    无

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_load_default_ai()
```

---

## api_trigger_rescue

method in Unit

- 描述

    单位 - 单位发起求救

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | source_unit | py.Unit | 攻击目标 |
    | seek_range | number | 搜寻范围 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_trigger_rescue(unit.handle, 1.0)
```

---

## api_set_rescue_seeker_type

method in Unit

- 描述

    单位 - 设置单位求救类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | v | py.ERescueSeekerType | 值 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_rescue_seeker_type(1)
```

---

## api_set_rescuer_type

method in Unit

- 描述

    单位 - 设置单位救援类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | v | py.ERescuerType | 值 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_rescuer_type(1)
```

---

## api_set_rescue_seeker_distance

method in Unit

- 描述

    单位 - 设置单位求救距离

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | v | number | 值 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_rescue_seeker_distance(1.0)
```

---

## api_set_rescue_seeker_interval

method in Unit

- 描述

    单位 - 设置单位求救间隔

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | v | number | 值 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_rescue_seeker_interval(1.0)
```

---

## api_set_rescue_finish_return

method in Unit

- 描述

    单位 - 设置单位救援后返回

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | v | boolean | 值 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_rescue_finish_return(true)
```

---

## api_get_rescue_seeker_type

method in Unit

- 描述

    单位 - 获取单位求救类型

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ERescueSeekerType? | 值 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_rescue_seeker_type()
```

---

## api_get_rescuer_type

method in Unit

- 描述

    单位 - 获取单位救援类型

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ERescuerType? | 值 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_rescuer_type()
```

---

## api_get_rescue_seeker_distance

method in Unit

- 描述

    单位 - 获取单位求救距离

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number? | 值 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_rescue_seeker_distance()
```

---

## api_get_rescue_seeker_interval

method in Unit

- 描述

    单位 - 获取单位求救间隔

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number? | 值 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_rescue_seeker_interval()
```

---

## api_get_rescue_finish_return

method in Unit

- 描述

    单位 - 获取单位救援后返回

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 值 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_rescue_finish_return()
```

---

## api_get_is_rescuing

method in Unit

- 描述

    单位 - 获取单位是否正在救援

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 值 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_is_rescuing()
```

---

## api_get_is_rescue_returning

method in Unit

- 描述

    单位 - 获取单位是否正在救援后返回

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 值 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_get_is_rescue_returning()
```

---

## api_try_update_ai

method in Unit

- 描述

    单位 - 尝试触发AI更新

- 参数

    无

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_try_update_ai()
```

---

## api_do_next_command

method in Unit

- 描述

    单位 - 执行下一命令

- 参数

    无

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_do_next_command()
```

---

## api_is_command_queue_empty

method in Unit

- 描述

    单位 - 获取命令队列是否为空

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 值 |

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = unit.handle:api_is_command_queue_empty()
```

---

## api_set_repair_target_unit

method in Unit

- 描述

    单位 - 设置维修目标单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | repair_target | py.Unit | 维修目标单位 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit.handle:api_set_repair_target_unit(unit.handle)
```

---

## api_set_repair_ability

method in Unit

- 描述

    单位 - 设置维修技能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability | py.Ability | 维修技能 |

- 返回值

    无

- 示例

```lua
-- 获取单位对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

unit.handle:api_set_repair_ability(ability.handle)
```

---
