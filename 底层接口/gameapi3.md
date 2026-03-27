---
sidebarDepth: 1
---
# GameAPI (Part 3)

# 索引

Y3 编辑器 GameAPI 接口集合（第 3 部分），包含游戏核心功能。

---

| 接口 | 描述 |
| --- | --- |
| [set_trigger_list_actor_variable_joint](#set_trigger_list_actor_variable_joint) | 设置全局触发器JOINT数组 组变量子项 |
| [set_trigger_variable_joint](#set_trigger_variable_joint) | 设置全局触发器JOINT非数组变量 |
| [set_trigger_actor_variable_joint](#set_trigger_actor_variable_joint) | 设置全局触发器JOINT非数组 组变量 |
| [set_trigger_list_variable_reaction](#set_trigger_list_variable_reaction) | 设置全局触发器REACTION数组变量子项 |
| [set_trigger_list_actor_variable_reaction](#set_trigger_list_actor_variable_reaction) | 设置全局触发器REACTION数组 组变量子项 |
| [set_trigger_variable_reaction](#set_trigger_variable_reaction) | 设置全局触发器REACTION非数组变量 |
| [set_trigger_actor_variable_reaction](#set_trigger_actor_variable_reaction) | 设置全局触发器REACTION非数组 组变量 |
| [set_trigger_list_variable_reaction_group](#set_trigger_list_variable_reaction_group) | 设置全局触发器REACTION_GROUP数组变量子项 |
| [set_trigger_list_actor_variable_reaction_group](#set_trigger_list_actor_variable_reaction_group) | 设置全局触发器REACTION_GROUP数组 组变量子项 |
| [set_trigger_variable_reaction_group](#set_trigger_variable_reaction_group) | 设置全局触发器REACTION_GROUP非数组变量 |
| [set_trigger_actor_variable_reaction_group](#set_trigger_actor_variable_reaction_group) | 设置全局触发器REACTION_GROUP非数组 组变量 |
| [set_trigger_list_variable_physics_filter](#set_trigger_list_variable_physics_filter) | 设置全局触发器PHYSICS_FILTER数组变量子项 |
| [set_trigger_list_actor_variable_physics_filter](#set_trigger_list_actor_variable_physics_filter) | 设置全局触发器PHYSICS_FILTER数组 组变量子项 |
| [set_trigger_variable_physics_filter](#set_trigger_variable_physics_filter) | 设置全局触发器PHYSICS_FILTER非数组变量 |
| [set_trigger_actor_variable_physics_filter](#set_trigger_actor_variable_physics_filter) | 设置全局触发器PHYSICS_FILTER非数组 组变量 |
| [set_trigger_list_variable_int_save](#set_trigger_list_variable_int_save) | 设置全局触发器INT_SAVE数组变量子项 |
| [set_trigger_list_actor_variable_int_save](#set_trigger_list_actor_variable_int_save) | 设置全局触发器INT_SAVE数组 组变量子项 |
| [set_trigger_variable_int_save](#set_trigger_variable_int_save) | 设置全局触发器INT_SAVE非数组变量 |
| [set_trigger_actor_variable_int_save](#set_trigger_actor_variable_int_save) | 设置全局触发器INT_SAVE非数组 组变量 |
| [set_trigger_list_variable_str_save](#set_trigger_list_variable_str_save) | 设置全局触发器STR_SAVE数组变量子项 |
| [set_trigger_list_actor_variable_str_save](#set_trigger_list_actor_variable_str_save) | 设置全局触发器STR_SAVE数组 组变量子项 |
| [set_trigger_variable_str_save](#set_trigger_variable_str_save) | 设置全局触发器STR_SAVE非数组变量 |
| [set_trigger_actor_variable_str_save](#set_trigger_actor_variable_str_save) | 设置全局触发器STR_SAVE非数组 组变量 |
| [set_trigger_list_variable_float_save](#set_trigger_list_variable_float_save) | 设置全局触发器FLOAT_SAVE数组变量子项 |
| [set_trigger_list_actor_variable_float_save](#set_trigger_list_actor_variable_float_save) | 设置全局触发器FLOAT_SAVE数组 组变量子项 |
| [set_trigger_variable_float_save](#set_trigger_variable_float_save) | 设置全局触发器FLOAT_SAVE非数组变量 |
| [set_trigger_actor_variable_float_save](#set_trigger_actor_variable_float_save) | 设置全局触发器FLOAT_SAVE非数组 组变量 |
| [set_trigger_list_variable_bool_save](#set_trigger_list_variable_bool_save) | 设置全局触发器BOOL_SAVE数组变量子项 |
| [set_trigger_list_actor_variable_bool_save](#set_trigger_list_actor_variable_bool_save) | 设置全局触发器BOOL_SAVE数组 组变量子项 |
| [set_trigger_variable_bool_save](#set_trigger_variable_bool_save) | 设置全局触发器BOOL_SAVE非数组变量 |
| [set_trigger_actor_variable_bool_save](#set_trigger_actor_variable_bool_save) | 设置全局触发器BOOL_SAVE非数组 组变量 |
| [set_trigger_list_variable_table_save](#set_trigger_list_variable_table_save) | 设置全局触发器TABLE_SAVE数组变量子项 |
| [set_trigger_list_actor_variable_table_save](#set_trigger_list_actor_variable_table_save) | 设置全局触发器TABLE_SAVE数组 组变量子项 |
| [set_trigger_variable_table_save](#set_trigger_variable_table_save) | 设置全局触发器TABLE_SAVE非数组变量 |
| [set_trigger_actor_variable_table_save](#set_trigger_actor_variable_table_save) | 设置全局触发器TABLE_SAVE非数组 组变量 |
| [set_trigger_list_variable_global_archive_slot](#set_trigger_list_variable_global_archive_slot) | 设置全局触发器GLOBAL_ARCHIVE_SLOT数组变量子项 |
| [set_trigger_list_actor_variable_global_archive_slot](#set_trigger_list_actor_variable_global_archive_slot) | 设置全局触发器GLOBAL_ARCHIVE_SLOT数组 组变量子项 |
| [set_trigger_variable_global_archive_slot](#set_trigger_variable_global_archive_slot) | 设置全局触发器GLOBAL_ARCHIVE_SLOT非数组变量 |
| [set_trigger_actor_variable_global_archive_slot](#set_trigger_actor_variable_global_archive_slot) | 设置全局触发器GLOBAL_ARCHIVE_SLOT非数组 组变量 |
| [set_trigger_list_variable_random_pool_drop](#set_trigger_list_variable_random_pool_drop) | 设置全局触发器RANDOM_POOL_DROP数组变量子项 |
| [set_trigger_list_actor_variable_random_pool_drop](#set_trigger_list_actor_variable_random_pool_drop) | 设置全局触发器RANDOM_POOL_DROP数组 组变量子项 |
| [set_trigger_variable_random_pool_drop](#set_trigger_variable_random_pool_drop) | 设置全局触发器RANDOM_POOL_DROP非数组变量 |
| [set_trigger_actor_variable_random_pool_drop](#set_trigger_actor_variable_random_pool_drop) | 设置全局触发器RANDOM_POOL_DROP非数组 组变量 |
| [set_trigger_list_variable_dynamic_trigger_instance](#set_trigger_list_variable_dynamic_trigger_instance) | 设置全局触发器DYNAMIC_TRIGGER_INSTANCE数组变量子项 |
| [set_trigger_list_actor_variable_dynamic_trigger_instance](#set_trigger_list_actor_variable_dynamic_trigger_instance) | 设置全局触发器DYNAMIC_TRIGGER_INSTANCE数组 组变量子项 |
| [set_trigger_variable_dynamic_trigger_instance](#set_trigger_variable_dynamic_trigger_instance) | 设置全局触发器DYNAMIC_TRIGGER_INSTANCE非数组变量 |
| [set_trigger_actor_variable_dynamic_trigger_instance](#set_trigger_actor_variable_dynamic_trigger_instance) | 设置全局触发器DYNAMIC_TRIGGER_INSTANCE非数组 组变量 |
| [set_trigger_list_variable_table](#set_trigger_list_variable_table) | 设置全局触发器TABLE数组变量子项 |
| [set_trigger_list_actor_variable_table](#set_trigger_list_actor_variable_table) | 设置全局触发器TABLE数组 组变量子项 |
| [set_trigger_variable_table](#set_trigger_variable_table) | 设置全局触发器TABLE非数组变量 |
| [set_trigger_actor_variable_table](#set_trigger_actor_variable_table) | 设置全局触发器TABLE非数组 组变量 |
| [set_trigger_list_variable_random_pool](#set_trigger_list_variable_random_pool) | 设置全局触发器RANDOM_POOL数组变量子项 |
| [set_trigger_list_actor_variable_random_pool](#set_trigger_list_actor_variable_random_pool) | 设置全局触发器RANDOM_POOL数组 组变量子项 |
| [set_trigger_variable_random_pool](#set_trigger_variable_random_pool) | 设置全局触发器RANDOM_POOL非数组变量 |
| [set_trigger_actor_variable_random_pool](#set_trigger_actor_variable_random_pool) | 设置全局触发器RANDOM_POOL非数组 组变量 |
| [set_trigger_list_variable_scene_ui](#set_trigger_list_variable_scene_ui) | 设置全局触发器SCENE_UI数组变量子项 |
| [set_trigger_list_actor_variable_scene_ui](#set_trigger_list_actor_variable_scene_ui) | 设置全局触发器SCENE_UI数组 组变量子项 |
| [set_trigger_variable_scene_ui](#set_trigger_variable_scene_ui) | 设置全局触发器SCENE_UI非数组变量 |
| [set_trigger_actor_variable_scene_ui](#set_trigger_actor_variable_scene_ui) | 设置全局触发器SCENE_UI非数组 组变量 |
| [set_trigger_list_variable_damage_type](#set_trigger_list_variable_damage_type) | 设置全局触发器DAMAGE_TYPE数组变量子项 |
| [set_trigger_list_actor_variable_damage_type](#set_trigger_list_actor_variable_damage_type) | 设置全局触发器DAMAGE_TYPE数组 组变量子项 |
| [set_trigger_variable_damage_type](#set_trigger_variable_damage_type) | 设置全局触发器DAMAGE_TYPE非数组变量 |
| [set_trigger_actor_variable_damage_type](#set_trigger_actor_variable_damage_type) | 设置全局触发器DAMAGE_TYPE非数组 组变量 |
| [set_trigger_list_variable_new_timer](#set_trigger_list_variable_new_timer) | 设置全局触发器NEW_TIMER数组变量子项 |
| [set_trigger_list_actor_variable_new_timer](#set_trigger_list_actor_variable_new_timer) | 设置全局触发器NEW_TIMER数组 组变量子项 |
| [set_trigger_variable_new_timer](#set_trigger_variable_new_timer) | 设置全局触发器NEW_TIMER非数组变量 |
| [set_trigger_actor_variable_new_timer](#set_trigger_actor_variable_new_timer) | 设置全局触发器NEW_TIMER非数组 组变量 |
| [set_trigger_list_variable_tech_key](#set_trigger_list_variable_tech_key) | 设置全局触发器TECH_KEY数组变量子项 |
| [set_trigger_list_actor_variable_tech_key](#set_trigger_list_actor_variable_tech_key) | 设置全局触发器TECH_KEY数组 组变量子项 |
| [set_trigger_variable_tech_key](#set_trigger_variable_tech_key) | 设置全局触发器TECH_KEY非数组变量 |
| [set_trigger_actor_variable_tech_key](#set_trigger_actor_variable_tech_key) | 设置全局触发器TECH_KEY非数组 组变量 |
| [set_trigger_list_variable_store_key](#set_trigger_list_variable_store_key) | 设置全局触发器STORE_KEY数组变量子项 |
| [set_trigger_list_actor_variable_store_key](#set_trigger_list_actor_variable_store_key) | 设置全局触发器STORE_KEY数组 组变量子项 |
| [set_trigger_variable_store_key](#set_trigger_variable_store_key) | 设置全局触发器STORE_KEY非数组变量 |
| [set_trigger_actor_variable_store_key](#set_trigger_actor_variable_store_key) | 设置全局触发器STORE_KEY非数组 组变量 |
| [set_trigger_list_variable_keyboard_key](#set_trigger_list_variable_keyboard_key) | 设置全局触发器KEYBOARD_KEY数组变量子项 |
| [set_trigger_list_actor_variable_keyboard_key](#set_trigger_list_actor_variable_keyboard_key) | 设置全局触发器KEYBOARD_KEY数组 组变量子项 |
| [set_trigger_variable_keyboard_key](#set_trigger_variable_keyboard_key) | 设置全局触发器KEYBOARD_KEY非数组变量 |
| [set_trigger_actor_variable_keyboard_key](#set_trigger_actor_variable_keyboard_key) | 设置全局触发器KEYBOARD_KEY非数组 组变量 |
| [set_trigger_list_variable_unit_type](#set_trigger_list_variable_unit_type) | 设置全局触发器UNIT_TYPE数组变量子项 |
| [set_trigger_list_actor_variable_unit_type](#set_trigger_list_actor_variable_unit_type) | 设置全局触发器UNIT_TYPE数组 组变量子项 |
| [set_trigger_variable_unit_type](#set_trigger_variable_unit_type) | 设置全局触发器UNIT_TYPE非数组变量 |
| [set_trigger_actor_variable_unit_type](#set_trigger_actor_variable_unit_type) | 设置全局触发器UNIT_TYPE非数组 组变量 |
| [set_trigger_list_variable_curved_path](#set_trigger_list_variable_curved_path) | 设置全局触发器CURVED_PATH数组变量子项 |
| [set_trigger_list_actor_variable_curved_path](#set_trigger_list_actor_variable_curved_path) | 设置全局触发器CURVED_PATH数组 组变量子项 |
| [set_trigger_variable_curved_path](#set_trigger_variable_curved_path) | 设置全局触发器CURVED_PATH非数组变量 |
| [set_trigger_actor_variable_curved_path](#set_trigger_actor_variable_curved_path) | 设置全局触发器CURVED_PATH非数组 组变量 |
| [set_trigger_list_variable_curved_path_3d](#set_trigger_list_variable_curved_path_3d) | 设置全局触发器CURVED_PATH_3D数组变量子项 |
| [set_trigger_list_actor_variable_curved_path_3d](#set_trigger_list_actor_variable_curved_path_3d) | 设置全局触发器CURVED_PATH_3D数组 组变量子项 |
| [set_trigger_variable_curved_path_3d](#set_trigger_variable_curved_path_3d) | 设置全局触发器CURVED_PATH_3D非数组变量 |
| [set_trigger_actor_variable_curved_path_3d](#set_trigger_actor_variable_curved_path_3d) | 设置全局触发器CURVED_PATH_3D非数组 组变量 |
| [get_list_value_by_type](#get_list_value_by_type) | 获取数组中某项（指定类型） |
| [set_list_value_by_type](#set_list_value_by_type) | 设置数组中某项（指定类型） |
| [get_float_list_value](#get_float_list_value) | 获取FLOAT数组中某项 |
| [set_float_list_value](#set_float_list_value) | 设置FLOAT数组中某项 |
| [get_float_n_list](#get_float_n_list) | 生成n个值为v的FLOAT数组 |
| [get_boolean_list_value](#get_boolean_list_value) | 获取BOOLEAN数组中某项 |
| [set_boolean_list_value](#set_boolean_list_value) | 设置BOOLEAN数组中某项 |
| [get_boolean_n_list](#get_boolean_n_list) | 生成n个值为v的BOOLEAN数组 |
| [get_integer_list_value](#get_integer_list_value) | 获取INTEGER数组中某项 |
| [set_integer_list_value](#set_integer_list_value) | 设置INTEGER数组中某项 |
| [get_integer_n_list](#get_integer_n_list) | 生成n个值为v的INTEGER数组 |
| [get_string_list_value](#get_string_list_value) | 获取STRING数组中某项 |
| [set_string_list_value](#set_string_list_value) | 设置STRING数组中某项 |
| [get_string_n_list](#get_string_n_list) | 生成n个值为v的STRING数组 |
| [get_point_list_value](#get_point_list_value) | 获取POINT数组中某项 |
| [set_point_list_value](#set_point_list_value) | 设置POINT数组中某项 |
| [get_point_n_list](#get_point_n_list) | 生成n个值为v的POINT数组 |
| [get_unit_entity_list_value](#get_unit_entity_list_value) | 获取UNIT_ENTITY数组中某项 |
| [set_unit_entity_list_value](#set_unit_entity_list_value) | 设置UNIT_ENTITY数组中某项 |
| [get_unit_entity_n_list](#get_unit_entity_n_list) | 生成n个值为v的UNIT_ENTITY数组 |
| [get_rectangle_list_value](#get_rectangle_list_value) | 获取RECTANGLE数组中某项 |
| [set_rectangle_list_value](#set_rectangle_list_value) | 设置RECTANGLE数组中某项 |
| [get_rectangle_n_list](#get_rectangle_n_list) | 生成n个值为v的RECTANGLE数组 |
| [get_unit_type_list_value](#get_unit_type_list_value) | 获取UNIT_TYPE数组中某项 |
| [set_unit_type_list_value](#set_unit_type_list_value) | 设置UNIT_TYPE数组中某项 |
| [get_unit_type_n_list](#get_unit_type_n_list) | 生成n个值为v的UNIT_TYPE数组 |
| [get_table_list_value](#get_table_list_value) | 获取TABLE数组中某项 |
| [set_table_list_value](#set_table_list_value) | 设置TABLE数组中某项 |
| [get_table_n_list](#get_table_n_list) | 生成n个值为v的TABLE数组 |
| [get_ability_list_value](#get_ability_list_value) | 获取ABILITY数组中某项 |
| [set_ability_list_value](#set_ability_list_value) | 设置ABILITY数组中某项 |
| [get_ability_n_list](#get_ability_n_list) | 生成n个值为v的ABILITY数组 |
| [get_team_list_value](#get_team_list_value) | 获取TEAM数组中某项 |
| [set_team_list_value](#set_team_list_value) | 设置TEAM数组中某项 |
| [get_team_n_list](#get_team_n_list) | 生成n个值为v的TEAM数组 |
| [get_round_area_list_value](#get_round_area_list_value) | 获取ROUND_AREA数组中某项 |
| [set_round_area_list_value](#set_round_area_list_value) | 设置ROUND_AREA数组中某项 |
| [get_round_area_n_list](#get_round_area_n_list) | 生成n个值为v的ROUND_AREA数组 |
| [get_point_list_list_value](#get_point_list_list_value) | 获取POINT_LIST数组中某项 |
| [set_point_list_list_value](#set_point_list_list_value) | 设置POINT_LIST数组中某项 |
| [get_point_list_n_list](#get_point_list_n_list) | 生成n个值为v的POINT_LIST数组 |
| [get_player_list_value](#get_player_list_value) | 获取PLAYER数组中某项 |
| [set_player_list_value](#set_player_list_value) | 设置PLAYER数组中某项 |
| [get_player_n_list](#get_player_n_list) | 生成n个值为v的PLAYER数组 |
| [get_unit_group_list_value](#get_unit_group_list_value) | 获取UNIT_GROUP数组中某项 |
| [set_unit_group_list_value](#set_unit_group_list_value) | 设置UNIT_GROUP数组中某项 |
| [get_unit_group_n_list](#get_unit_group_n_list) | 生成n个值为v的UNIT_GROUP数组 |
| [get_player_group_list_value](#get_player_group_list_value) | 获取PLAYER_GROUP数组中某项 |
| [set_player_group_list_value](#set_player_group_list_value) | 设置PLAYER_GROUP数组中某项 |
| [get_player_group_n_list](#get_player_group_n_list) | 生成n个值为v的PLAYER_GROUP数组 |
| [get_item_entity_list_value](#get_item_entity_list_value) | 获取ITEM_ENTITY数组中某项 |
| [set_item_entity_list_value](#set_item_entity_list_value) | 设置ITEM_ENTITY数组中某项 |
| [get_item_entity_n_list](#get_item_entity_n_list) | 生成n个值为v的ITEM_ENTITY数组 |
| [get_item_name_list_value](#get_item_name_list_value) | 获取ITEM_NAME数组中某项 |
| [set_item_name_list_value](#set_item_name_list_value) | 设置ITEM_NAME数组中某项 |
| [get_item_name_n_list](#get_item_name_n_list) | 生成n个值为v的ITEM_NAME数组 |
| [get_role_res_key_list_value](#get_role_res_key_list_value) | 获取ROLE_RES_KEY数组中某项 |
| [set_role_res_key_list_value](#set_role_res_key_list_value) | 设置ROLE_RES_KEY数组中某项 |
| [get_role_res_key_n_list](#get_role_res_key_n_list) | 生成n个值为v的ROLE_RES_KEY数组 |
| [get_unit_name_pool_list_value](#get_unit_name_pool_list_value) | 获取UNIT_NAME_POOL数组中某项 |
| [set_unit_name_pool_list_value](#set_unit_name_pool_list_value) | 设置UNIT_NAME_POOL数组中某项 |
| [get_unit_name_pool_n_list](#get_unit_name_pool_n_list) | 生成n个值为v的UNIT_NAME_POOL数组 |
| [get_ability_name_list_value](#get_ability_name_list_value) | 获取ABILITY_NAME数组中某项 |
| [set_ability_name_list_value](#set_ability_name_list_value) | 设置ABILITY_NAME数组中某项 |
| [get_ability_name_n_list](#get_ability_name_n_list) | 生成n个值为v的ABILITY_NAME数组 |
| [get_unit_write_attribute_list_value](#get_unit_write_attribute_list_value) | 获取UNIT_WRITE_ATTRIBUTE数组中某项 |
| [set_unit_write_attribute_list_value](#set_unit_write_attribute_list_value) | 设置UNIT_WRITE_ATTRIBUTE数组中某项 |
| [get_unit_write_attribute_n_list](#get_unit_write_attribute_n_list) | 生成n个值为v的UNIT_WRITE_ATTRIBUTE数组 |
| [get_modifier_list_value](#get_modifier_list_value) | 获取MODIFIER数组中某项 |
| [set_modifier_list_value](#set_modifier_list_value) | 设置MODIFIER数组中某项 |
| [get_modifier_n_list](#get_modifier_n_list) | 生成n个值为v的MODIFIER数组 |
| [get_projectile_list_value](#get_projectile_list_value) | 获取PROJECTILE数组中某项 |
| [set_projectile_list_value](#set_projectile_list_value) | 设置PROJECTILE数组中某项 |
| [get_projectile_n_list](#get_projectile_n_list) | 生成n个值为v的PROJECTILE数组 |
| [get_damage_type_list_value](#get_damage_type_list_value) | 获取DAMAGE_TYPE数组中某项 |
| [set_damage_type_list_value](#set_damage_type_list_value) | 设置DAMAGE_TYPE数组中某项 |
| [get_damage_type_n_list](#get_damage_type_n_list) | 生成n个值为v的DAMAGE_TYPE数组 |
| [get_sfx_key_list_value](#get_sfx_key_list_value) | 获取SFX_KEY数组中某项 |
| [set_sfx_key_list_value](#set_sfx_key_list_value) | 设置SFX_KEY数组中某项 |
| [get_sfx_key_n_list](#get_sfx_key_n_list) | 生成n个值为v的SFX_KEY数组 |
| [get_ui_comp_list_value](#get_ui_comp_list_value) | 获取UI_COMP数组中某项 |
| [set_ui_comp_list_value](#set_ui_comp_list_value) | 设置UI_COMP数组中某项 |
| [get_ui_comp_n_list](#get_ui_comp_n_list) | 生成n个值为v的UI_COMP数组 |
| [get_ui_comp_type_list_value](#get_ui_comp_type_list_value) | 获取UI_COMP_TYPE数组中某项 |
| [set_ui_comp_type_list_value](#set_ui_comp_type_list_value) | 设置UI_COMP_TYPE数组中某项 |
| [get_ui_comp_type_n_list](#get_ui_comp_type_n_list) | 生成n个值为v的UI_COMP_TYPE数组 |
| [get_ui_comp_event_type_list_value](#get_ui_comp_event_type_list_value) | 获取UI_COMP_EVENT_TYPE数组中某项 |
| [set_ui_comp_event_type_list_value](#set_ui_comp_event_type_list_value) | 设置UI_COMP_EVENT_TYPE数组中某项 |
| [get_ui_comp_event_type_n_list](#get_ui_comp_event_type_n_list) | 生成n个值为v的UI_COMP_EVENT_TYPE数组 |
| [get_camera_list_value](#get_camera_list_value) | 获取CAMERA数组中某项 |
| [set_camera_list_value](#set_camera_list_value) | 设置CAMERA数组中某项 |
| [get_camera_n_list](#get_camera_n_list) | 生成n个值为v的CAMERA数组 |
| [get_modifier_entity_list_value](#get_modifier_entity_list_value) | 获取MODIFIER_ENTITY数组中某项 |
| [set_modifier_entity_list_value](#set_modifier_entity_list_value) | 设置MODIFIER_ENTITY数组中某项 |
| [get_modifier_entity_n_list](#get_modifier_entity_n_list) | 生成n个值为v的MODIFIER_ENTITY数组 |
| [get_projectile_entity_list_value](#get_projectile_entity_list_value) | 获取PROJECTILE_ENTITY数组中某项 |
| [set_projectile_entity_list_value](#set_projectile_entity_list_value) | 设置PROJECTILE_ENTITY数组中某项 |
| [get_projectile_entity_n_list](#get_projectile_entity_n_list) | 生成n个值为v的PROJECTILE_ENTITY数组 |
| [get_audio_key_list_value](#get_audio_key_list_value) | 获取AUDIO_KEY数组中某项 |
| [set_audio_key_list_value](#set_audio_key_list_value) | 设置AUDIO_KEY数组中某项 |
| [get_audio_key_n_list](#get_audio_key_n_list) | 生成n个值为v的AUDIO_KEY数组 |
| [get_texture_list_value](#get_texture_list_value) | 获取TEXTURE数组中某项 |
| [set_texture_list_value](#set_texture_list_value) | 设置TEXTURE数组中某项 |
| [get_texture_n_list](#get_texture_n_list) | 生成n个值为v的TEXTURE数组 |
| [get_unit_name_list_value](#get_unit_name_list_value) | 获取UNIT_NAME数组中某项 |
| [set_unit_name_list_value](#set_unit_name_list_value) | 设置UNIT_NAME数组中某项 |
| [get_unit_name_n_list](#get_unit_name_n_list) | 生成n个值为v的UNIT_NAME数组 |
| [get_model_list_value](#get_model_list_value) | 获取MODEL数组中某项 |
| [set_model_list_value](#set_model_list_value) | 设置MODEL数组中某项 |
| [get_model_n_list](#get_model_n_list) | 生成n个值为v的MODEL数组 |
| [get_store_key_list_value](#get_store_key_list_value) | 获取STORE_KEY数组中某项 |
| [set_store_key_list_value](#set_store_key_list_value) | 设置STORE_KEY数组中某项 |
| [get_store_key_n_list](#get_store_key_n_list) | 生成n个值为v的STORE_KEY数组 |
| [get_sfx_entity_list_value](#get_sfx_entity_list_value) | 获取SFX_ENTITY数组中某项 |
| [set_sfx_entity_list_value](#set_sfx_entity_list_value) | 设置SFX_ENTITY数组中某项 |
| [get_sfx_entity_n_list](#get_sfx_entity_n_list) | 生成n个值为v的SFX_ENTITY数组 |
| [get_road_group_list_value](#get_road_group_list_value) | 获取ROAD_GROUP数组中某项 |
| [set_road_group_list_value](#set_road_group_list_value) | 设置ROAD_GROUP数组中某项 |
| [get_road_group_n_list](#get_road_group_n_list) | 生成n个值为v的ROAD_GROUP数组 |
| [get_polygon_list_value](#get_polygon_list_value) | 获取POLYGON数组中某项 |
| [set_polygon_list_value](#set_polygon_list_value) | 设置POLYGON数组中某项 |
| [get_polygon_n_list](#get_polygon_n_list) | 生成n个值为v的POLYGON数组 |
| [get_item_group_list_value](#get_item_group_list_value) | 获取ITEM_GROUP数组中某项 |
| [set_item_group_list_value](#set_item_group_list_value) | 设置ITEM_GROUP数组中某项 |
| [get_item_group_n_list](#get_item_group_n_list) | 生成n个值为v的ITEM_GROUP数组 |
| [get_tech_key_list_value](#get_tech_key_list_value) | 获取TECH_KEY数组中某项 |
| [set_tech_key_list_value](#set_tech_key_list_value) | 设置TECH_KEY数组中某项 |
| [get_tech_key_n_list](#get_tech_key_n_list) | 生成n个值为v的TECH_KEY数组 |
| [get_dynamic_trigger_instance_list_value](#get_dynamic_trigger_instance_list_value) | 获取DYNAMIC_TRIGGER_INSTANCE数组中某项 |
| [set_dynamic_trigger_instance_list_value](#set_dynamic_trigger_instance_list_value) | 设置DYNAMIC_TRIGGER_INSTANCE数组中某项 |
| [get_dynamic_trigger_instance_n_list](#get_dynamic_trigger_instance_n_list) | 生成n个值为v的DYNAMIC_TRIGGER_INSTANCE数组 |
| [get_role_type_list_value](#get_role_type_list_value) | 获取ROLE_TYPE数组中某项 |
| [set_role_type_list_value](#set_role_type_list_value) | 设置ROLE_TYPE数组中某项 |
| [get_role_type_n_list](#get_role_type_n_list) | 生成n个值为v的ROLE_TYPE数组 |
| [get_role_status_list_value](#get_role_status_list_value) | 获取ROLE_STATUS数组中某项 |
| [set_role_status_list_value](#set_role_status_list_value) | 设置ROLE_STATUS数组中某项 |
| [get_role_status_n_list](#get_role_status_n_list) | 生成n个值为v的ROLE_STATUS数组 |
| [get_new_timer_list_value](#get_new_timer_list_value) | 获取NEW_TIMER数组中某项 |
| [set_new_timer_list_value](#set_new_timer_list_value) | 设置NEW_TIMER数组中某项 |
| [get_new_timer_n_list](#get_new_timer_n_list) | 生成n个值为v的NEW_TIMER数组 |
| [get_ability_type_list_value](#get_ability_type_list_value) | 获取ABILITY_TYPE数组中某项 |
| [set_ability_type_list_value](#set_ability_type_list_value) | 设置ABILITY_TYPE数组中某项 |
| [get_ability_type_n_list](#get_ability_type_n_list) | 生成n个值为v的ABILITY_TYPE数组 |
| [get_link_sfx_key_list_value](#get_link_sfx_key_list_value) | 获取LINK_SFX_KEY数组中某项 |
| [set_link_sfx_key_list_value](#set_link_sfx_key_list_value) | 设置LINK_SFX_KEY数组中某项 |
| [get_link_sfx_key_n_list](#get_link_sfx_key_n_list) | 生成n个值为v的LINK_SFX_KEY数组 |
| [get_ui_comp_align_type_list_value](#get_ui_comp_align_type_list_value) | 获取UI_COMP_ALIGN_TYPE数组中某项 |
| [set_ui_comp_align_type_list_value](#set_ui_comp_align_type_list_value) | 设置UI_COMP_ALIGN_TYPE数组中某项 |
| [get_ui_comp_align_type_n_list](#get_ui_comp_align_type_n_list) | 生成n个值为v的UI_COMP_ALIGN_TYPE数组 |
| [get_ui_direction_list_value](#get_ui_direction_list_value) | 获取UI_DIRECTION数组中某项 |
| [set_ui_direction_list_value](#set_ui_direction_list_value) | 设置UI_DIRECTION数组中某项 |
| [get_ui_direction_n_list](#get_ui_direction_n_list) | 生成n个值为v的UI_DIRECTION数组 |
| [get_random_pool_list_value](#get_random_pool_list_value) | 获取RANDOM_POOL数组中某项 |
| [set_random_pool_list_value](#set_random_pool_list_value) | 设置RANDOM_POOL数组中某项 |
| [get_random_pool_n_list](#get_random_pool_n_list) | 生成n个值为v的RANDOM_POOL数组 |
| [get_link_sfx_entity_list_value](#get_link_sfx_entity_list_value) | 获取LINK_SFX_ENTITY数组中某项 |
| [set_link_sfx_entity_list_value](#set_link_sfx_entity_list_value) | 设置LINK_SFX_ENTITY数组中某项 |
| [get_link_sfx_entity_n_list](#get_link_sfx_entity_n_list) | 生成n个值为v的LINK_SFX_ENTITY数组 |
| [get_projectile_group_list_value](#get_projectile_group_list_value) | 获取PROJECTILE_GROUP数组中某项 |
| [set_projectile_group_list_value](#set_projectile_group_list_value) | 设置PROJECTILE_GROUP数组中某项 |
| [get_projectile_group_n_list](#get_projectile_group_n_list) | 生成n个值为v的PROJECTILE_GROUP数组 |
| [get_destructible_entity_list_value](#get_destructible_entity_list_value) | 获取DESTRUCTIBLE_ENTITY数组中某项 |
| [set_destructible_entity_list_value](#set_destructible_entity_list_value) | 设置DESTRUCTIBLE_ENTITY数组中某项 |
| [get_destructible_entity_n_list](#get_destructible_entity_n_list) | 生成n个值为v的DESTRUCTIBLE_ENTITY数组 |
| [get_destructible_name_list_value](#get_destructible_name_list_value) | 获取DESTRUCTIBLE_NAME数组中某项 |
| [set_destructible_name_list_value](#set_destructible_name_list_value) | 设置DESTRUCTIBLE_NAME数组中某项 |
| [get_destructible_name_n_list](#get_destructible_name_n_list) | 生成n个值为v的DESTRUCTIBLE_NAME数组 |
| [get_sound_entity_list_value](#get_sound_entity_list_value) | 获取SOUND_ENTITY数组中某项 |
| [set_sound_entity_list_value](#set_sound_entity_list_value) | 设置SOUND_ENTITY数组中某项 |
| [get_sound_entity_n_list](#get_sound_entity_n_list) | 生成n个值为v的SOUND_ENTITY数组 |
| [get_ability_cast_type_list_value](#get_ability_cast_type_list_value) | 获取ABILITY_CAST_TYPE数组中某项 |
| [set_ability_cast_type_list_value](#set_ability_cast_type_list_value) | 设置ABILITY_CAST_TYPE数组中某项 |
| [get_ability_cast_type_n_list](#get_ability_cast_type_n_list) | 生成n个值为v的ABILITY_CAST_TYPE数组 |
| [get_curved_path_list_value](#get_curved_path_list_value) | 获取CURVED_PATH数组中某项 |
| [set_curved_path_list_value](#set_curved_path_list_value) | 设置CURVED_PATH数组中某项 |
| [get_curved_path_n_list](#get_curved_path_n_list) | 生成n个值为v的CURVED_PATH数组 |
| [get_image_key_list_value](#get_image_key_list_value) | 获取IMAGE_KEY数组中某项 |
| [set_image_key_list_value](#set_image_key_list_value) | 设置IMAGE_KEY数组中某项 |
| [get_image_key_n_list](#get_image_key_n_list) | 生成n个值为v的IMAGE_KEY数组 |
| [get_angle_list_value](#get_angle_list_value) | 获取ANGLE数组中某项 |
| [set_angle_list_value](#set_angle_list_value) | 设置ANGLE数组中某项 |
| [get_angle_n_list](#get_angle_n_list) | 生成n个值为v的ANGLE数组 |
| [get_curved_path_3d_list_value](#get_curved_path_3d_list_value) | 获取CURVED_PATH_3D数组中某项 |
| [set_curved_path_3d_list_value](#set_curved_path_3d_list_value) | 设置CURVED_PATH_3D数组中某项 |
| [get_curved_path_3d_n_list](#get_curved_path_3d_n_list) | 生成n个值为v的CURVED_PATH_3D数组 |
| [get_int_save_list_value](#get_int_save_list_value) | 获取INT_SAVE数组中某项 |
| [set_int_save_list_value](#set_int_save_list_value) | 设置INT_SAVE数组中某项 |
| [get_int_save_n_list](#get_int_save_n_list) | 生成n个值为v的INT_SAVE数组 |
| [get_str_save_list_value](#get_str_save_list_value) | 获取STR_SAVE数组中某项 |
| [set_str_save_list_value](#set_str_save_list_value) | 设置STR_SAVE数组中某项 |
| [get_str_save_n_list](#get_str_save_n_list) | 生成n个值为v的STR_SAVE数组 |
| [get_float_save_list_value](#get_float_save_list_value) | 获取FLOAT_SAVE数组中某项 |
| [set_float_save_list_value](#set_float_save_list_value) | 设置FLOAT_SAVE数组中某项 |
| [get_float_save_n_list](#get_float_save_n_list) | 生成n个值为v的FLOAT_SAVE数组 |
| [get_bool_save_list_value](#get_bool_save_list_value) | 获取BOOL_SAVE数组中某项 |
| [set_bool_save_list_value](#set_bool_save_list_value) | 设置BOOL_SAVE数组中某项 |
| [get_bool_save_n_list](#get_bool_save_n_list) | 生成n个值为v的BOOL_SAVE数组 |
| [get_scene_ui_list_value](#get_scene_ui_list_value) | 获取SCENE_UI数组中某项 |
| [set_scene_ui_list_value](#set_scene_ui_list_value) | 设置SCENE_UI数组中某项 |
| [get_scene_ui_n_list](#get_scene_ui_n_list) | 生成n个值为v的SCENE_UI数组 |
| [get_ui_anim_list_value](#get_ui_anim_list_value) | 获取UI_ANIM数组中某项 |
| [set_ui_anim_list_value](#set_ui_anim_list_value) | 设置UI_ANIM数组中某项 |
| [get_ui_anim_n_list](#get_ui_anim_n_list) | 生成n个值为v的UI_ANIM数组 |
| [get_camline_list_value](#get_camline_list_value) | 获取CAMLINE数组中某项 |
| [set_camline_list_value](#set_camline_list_value) | 设置CAMLINE数组中某项 |
| [get_camline_n_list](#get_camline_n_list) | 生成n个值为v的CAMLINE数组 |
| [get_table_save_list_value](#get_table_save_list_value) | 获取TABLE_SAVE数组中某项 |
| [set_table_save_list_value](#set_table_save_list_value) | 设置TABLE_SAVE数组中某项 |
| [get_table_save_n_list](#get_table_save_n_list) | 生成n个值为v的TABLE_SAVE数组 |
| [get_mover_entity_list_value](#get_mover_entity_list_value) | 获取MOVER_ENTITY数组中某项 |
| [set_mover_entity_list_value](#set_mover_entity_list_value) | 设置MOVER_ENTITY数组中某项 |
| [get_mover_entity_n_list](#get_mover_entity_n_list) | 生成n个值为v的MOVER_ENTITY数组 |
| [get_cursor_key_list_value](#get_cursor_key_list_value) | 获取CURSOR_KEY数组中某项 |
| [set_cursor_key_list_value](#set_cursor_key_list_value) | 设置CURSOR_KEY数组中某项 |
| [get_cursor_key_n_list](#get_cursor_key_n_list) | 生成n个值为v的CURSOR_KEY数组 |
| [get_vector3_list_value](#get_vector3_list_value) | 获取VECTOR3数组中某项 |
| [set_vector3_list_value](#set_vector3_list_value) | 设置VECTOR3数组中某项 |
| [get_vector3_n_list](#get_vector3_n_list) | 生成n个值为v的VECTOR3数组 |
| [get_sequence_list_value](#get_sequence_list_value) | 获取SEQUENCE数组中某项 |
| [set_sequence_list_value](#set_sequence_list_value) | 设置SEQUENCE数组中某项 |
| [get_sequence_n_list](#get_sequence_n_list) | 生成n个值为v的SEQUENCE数组 |
| [get_physics_object_list_value](#get_physics_object_list_value) | 获取PHYSICS_OBJECT数组中某项 |
| [set_physics_object_list_value](#set_physics_object_list_value) | 设置PHYSICS_OBJECT数组中某项 |
| [get_physics_object_n_list](#get_physics_object_n_list) | 生成n个值为v的PHYSICS_OBJECT数组 |
| [get_physics_entity_list_value](#get_physics_entity_list_value) | 获取PHYSICS_ENTITY数组中某项 |
| [set_physics_entity_list_value](#set_physics_entity_list_value) | 设置PHYSICS_ENTITY数组中某项 |
| [get_physics_entity_n_list](#get_physics_entity_n_list) | 生成n个值为v的PHYSICS_ENTITY数组 |
| [get_rigid_body_list_value](#get_rigid_body_list_value) | 获取RIGID_BODY数组中某项 |
| [set_rigid_body_list_value](#set_rigid_body_list_value) | 设置RIGID_BODY数组中某项 |
| [get_rigid_body_n_list](#get_rigid_body_n_list) | 生成n个值为v的RIGID_BODY数组 |
| [get_collider_list_value](#get_collider_list_value) | 获取COLLIDER数组中某项 |
| [set_collider_list_value](#set_collider_list_value) | 设置COLLIDER数组中某项 |
| [get_collider_n_list](#get_collider_n_list) | 生成n个值为v的COLLIDER数组 |
| [get_attr_element_list_value](#get_attr_element_list_value) | 获取ATTR_ELEMENT数组中某项 |
| [set_attr_element_list_value](#set_attr_element_list_value) | 设置ATTR_ELEMENT数组中某项 |
| [get_attr_element_n_list](#get_attr_element_n_list) | 生成n个值为v的ATTR_ELEMENT数组 |
| [get_attr_element_read_list_value](#get_attr_element_read_list_value) | 获取ATTR_ELEMENT_READ数组中某项 |
| [set_attr_element_read_list_value](#set_attr_element_read_list_value) | 设置ATTR_ELEMENT_READ数组中某项 |
| [get_attr_element_read_n_list](#get_attr_element_read_n_list) | 生成n个值为v的ATTR_ELEMENT_READ数组 |
| [get_joint_list_value](#get_joint_list_value) | 获取JOINT数组中某项 |
| [set_joint_list_value](#set_joint_list_value) | 设置JOINT数组中某项 |
| [get_joint_n_list](#get_joint_n_list) | 生成n个值为v的JOINT数组 |
| [get_physics_object_key_list_value](#get_physics_object_key_list_value) | 获取PHYSICS_OBJECT_KEY数组中某项 |
| [set_physics_object_key_list_value](#set_physics_object_key_list_value) | 设置PHYSICS_OBJECT_KEY数组中某项 |
| [get_physics_object_key_n_list](#get_physics_object_key_n_list) | 生成n个值为v的PHYSICS_OBJECT_KEY数组 |
| [get_physics_entity_key_list_value](#get_physics_entity_key_list_value) | 获取PHYSICS_ENTITY_KEY数组中某项 |
| [set_physics_entity_key_list_value](#set_physics_entity_key_list_value) | 设置PHYSICS_ENTITY_KEY数组中某项 |
| [get_physics_entity_key_n_list](#get_physics_entity_key_n_list) | 生成n个值为v的PHYSICS_ENTITY_KEY数组 |
| [get_rotation_list_value](#get_rotation_list_value) | 获取ROTATION数组中某项 |
| [set_rotation_list_value](#set_rotation_list_value) | 设置ROTATION数组中某项 |
| [get_rotation_n_list](#get_rotation_n_list) | 生成n个值为v的ROTATION数组 |
| [get_rigid_body_group_list_value](#get_rigid_body_group_list_value) | 获取RIGID_BODY_GROUP数组中某项 |
| [set_rigid_body_group_list_value](#set_rigid_body_group_list_value) | 设置RIGID_BODY_GROUP数组中某项 |
| [get_rigid_body_group_n_list](#get_rigid_body_group_n_list) | 生成n个值为v的RIGID_BODY_GROUP数组 |
| [get_reaction_list_value](#get_reaction_list_value) | 获取REACTION数组中某项 |
| [set_reaction_list_value](#set_reaction_list_value) | 设置REACTION数组中某项 |
| [get_reaction_n_list](#get_reaction_n_list) | 生成n个值为v的REACTION数组 |
| [get_reaction_group_list_value](#get_reaction_group_list_value) | 获取REACTION_GROUP数组中某项 |
| [set_reaction_group_list_value](#set_reaction_group_list_value) | 设置REACTION_GROUP数组中某项 |
| [get_reaction_group_n_list](#get_reaction_group_n_list) | 生成n个值为v的REACTION_GROUP数组 |
| [get_ui_anim_curve_list_value](#get_ui_anim_curve_list_value) | 获取UI_ANIM_CURVE数组中某项 |
| [set_ui_anim_curve_list_value](#set_ui_anim_curve_list_value) | 设置UI_ANIM_CURVE数组中某项 |
| [get_ui_anim_curve_n_list](#get_ui_anim_curve_n_list) | 生成n个值为v的UI_ANIM_CURVE数组 |
| [get_physics_filter_list_value](#get_physics_filter_list_value) | 获取PHYSICS_FILTER数组中某项 |
| [set_physics_filter_list_value](#set_physics_filter_list_value) | 设置PHYSICS_FILTER数组中某项 |
| [get_physics_filter_n_list](#get_physics_filter_n_list) | 生成n个值为v的PHYSICS_FILTER数组 |
| [get_global_archive_slot_list_value](#get_global_archive_slot_list_value) | 获取GLOBAL_ARCHIVE_SLOT数组中某项 |
| [set_global_archive_slot_list_value](#set_global_archive_slot_list_value) | 设置GLOBAL_ARCHIVE_SLOT数组中某项 |
| [get_global_archive_slot_n_list](#get_global_archive_slot_n_list) | 生成n个值为v的GLOBAL_ARCHIVE_SLOT数组 |
| [get_random_pool_drop_list_value](#get_random_pool_drop_list_value) | 获取RANDOM_POOL_DROP数组中某项 |
| [set_random_pool_drop_list_value](#set_random_pool_drop_list_value) | 设置RANDOM_POOL_DROP数组中某项 |
| [get_random_pool_drop_n_list](#get_random_pool_drop_n_list) | 生成n个值为v的RANDOM_POOL_DROP数组 |
| [get_damage_attack_type_list_value](#get_damage_attack_type_list_value) | 获取DAMAGE_ATTACK_TYPE数组中某项 |
| [set_damage_attack_type_list_value](#set_damage_attack_type_list_value) | 设置DAMAGE_ATTACK_TYPE数组中某项 |
| [get_damage_attack_type_n_list](#get_damage_attack_type_n_list) | 生成n个值为v的DAMAGE_ATTACK_TYPE数组 |
| [get_damage_armor_type_list_value](#get_damage_armor_type_list_value) | 获取DAMAGE_ARMOR_TYPE数组中某项 |
| [set_damage_armor_type_list_value](#set_damage_armor_type_list_value) | 设置DAMAGE_ARMOR_TYPE数组中某项 |
| [get_damage_armor_type_n_list](#get_damage_armor_type_n_list) | 生成n个值为v的DAMAGE_ARMOR_TYPE数组 |
| [get_game_mode_list_value](#get_game_mode_list_value) | 获取GAME_MODE数组中某项 |
| [set_game_mode_list_value](#set_game_mode_list_value) | 设置GAME_MODE数组中某项 |
| [get_game_mode_n_list](#get_game_mode_n_list) | 生成n个值为v的GAME_MODE数组 |
| [get_image_quality_list_value](#get_image_quality_list_value) | 获取IMAGE_QUALITY数组中某项 |
| [set_image_quality_list_value](#set_image_quality_list_value) | 设置IMAGE_QUALITY数组中某项 |
| [get_image_quality_n_list](#get_image_quality_n_list) | 生成n个值为v的IMAGE_QUALITY数组 |
| [get_window_type_setting_list_value](#get_window_type_setting_list_value) | 获取WINDOW_TYPE_SETTING数组中某项 |
| [set_window_type_setting_list_value](#set_window_type_setting_list_value) | 设置WINDOW_TYPE_SETTING数组中某项 |
| [get_window_type_setting_n_list](#get_window_type_setting_n_list) | 生成n个值为v的WINDOW_TYPE_SETTING数组 |
| [get_keyboard_key_list_value](#get_keyboard_key_list_value) | 获取KEYBOARD_KEY数组中某项 |
| [set_keyboard_key_list_value](#set_keyboard_key_list_value) | 设置KEYBOARD_KEY数组中某项 |
| [get_keyboard_key_n_list](#get_keyboard_key_n_list) | 生成n个值为v的KEYBOARD_KEY数组 |
| [get_point_light_list_value](#get_point_light_list_value) | 获取POINT_LIGHT数组中某项 |
| [set_point_light_list_value](#set_point_light_list_value) | 设置POINT_LIGHT数组中某项 |
| [get_point_light_n_list](#get_point_light_n_list) | 生成n个值为v的POINT_LIGHT数组 |
| [get_spot_light_list_value](#get_spot_light_list_value) | 获取SPOT_LIGHT数组中某项 |
| [set_spot_light_list_value](#set_spot_light_list_value) | 设置SPOT_LIGHT数组中某项 |
| [get_spot_light_n_list](#get_spot_light_n_list) | 生成n个值为v的SPOT_LIGHT数组 |
| [get_fog_list_value](#get_fog_list_value) | 获取FOG数组中某项 |
| [set_fog_list_value](#set_fog_list_value) | 设置FOG数组中某项 |
| [get_fog_n_list](#get_fog_n_list) | 生成n个值为v的FOG数组 |
| [get_ui_prefab_list_value](#get_ui_prefab_list_value) | 获取UI_PREFAB数组中某项 |
| [set_ui_prefab_list_value](#set_ui_prefab_list_value) | 设置UI_PREFAB数组中某项 |
| [get_ui_prefab_n_list](#get_ui_prefab_n_list) | 生成n个值为v的UI_PREFAB数组 |
| [get_ui_prefab_instance_list_value](#get_ui_prefab_instance_list_value) | 获取UI_PREFAB_INSTANCE数组中某项 |
| [set_ui_prefab_instance_list_value](#set_ui_prefab_instance_list_value) | 设置UI_PREFAB_INSTANCE数组中某项 |
| [get_ui_prefab_instance_n_list](#get_ui_prefab_instance_n_list) | 生成n个值为v的UI_PREFAB_INSTANCE数组 |
| [get_ui_prefab_ins_uid_list_value](#get_ui_prefab_ins_uid_list_value) | 获取UI_PREFAB_INS_UID数组中某项 |
| [set_ui_prefab_ins_uid_list_value](#set_ui_prefab_ins_uid_list_value) | 设置UI_PREFAB_INS_UID数组中某项 |
| [get_ui_prefab_ins_uid_n_list](#get_ui_prefab_ins_uid_n_list) | 生成n个值为v的UI_PREFAB_INS_UID数组 |
| [get_audio_channel_list_value](#get_audio_channel_list_value) | 获取AUDIO_CHANNEL数组中某项 |
| [set_audio_channel_list_value](#set_audio_channel_list_value) | 设置AUDIO_CHANNEL数组中某项 |
| [get_audio_channel_n_list](#get_audio_channel_n_list) | 生成n个值为v的AUDIO_CHANNEL数组 |
| [get_ui_model_camera_mod_list_value](#get_ui_model_camera_mod_list_value) | 获取UI_MODEL_CAMERA_MOD数组中某项 |
| [set_ui_model_camera_mod_list_value](#set_ui_model_camera_mod_list_value) | 设置UI_MODEL_CAMERA_MOD数组中某项 |
| [get_ui_model_camera_mod_n_list](#get_ui_model_camera_mod_n_list) | 生成n个值为v的UI_MODEL_CAMERA_MOD数组 |
| [get_ui_btn_status_list_value](#get_ui_btn_status_list_value) | 获取UI_BTN_STATUS数组中某项 |
| [set_ui_btn_status_list_value](#set_ui_btn_status_list_value) | 设置UI_BTN_STATUS数组中某项 |
| [get_ui_btn_status_n_list](#get_ui_btn_status_n_list) | 生成n个值为v的UI_BTN_STATUS数组 |
| [get_ui_scrollview_type_list_value](#get_ui_scrollview_type_list_value) | 获取UI_SCROLLVIEW_TYPE数组中某项 |
| [set_ui_scrollview_type_list_value](#set_ui_scrollview_type_list_value) | 设置UI_SCROLLVIEW_TYPE数组中某项 |
| [get_ui_scrollview_type_n_list](#get_ui_scrollview_type_n_list) | 生成n个值为v的UI_SCROLLVIEW_TYPE数组 |
| [set_unit_key_boolean_kv](#set_unit_key_boolean_kv) | 预设库 添加BOOLEAN键值对 |
| [set_unit_key_integer_kv](#set_unit_key_integer_kv) | 预设库 添加INTEGER键值对 |
| [set_unit_key_float_kv](#set_unit_key_float_kv) | 预设库 添加FLOAT键值对 |
| [set_unit_key_string_kv](#set_unit_key_string_kv) | 预设库 添加STRING键值对 |
| [set_unit_key_ui_comp_kv](#set_unit_key_ui_comp_kv) | 预设库 添加UI_COMP键值对 |
| [set_unit_key_ui_comp_type_kv](#set_unit_key_ui_comp_type_kv) | 预设库 添加UI_COMP_TYPE键值对 |
| [set_unit_key_ui_comp_event_type_kv](#set_unit_key_ui_comp_event_type_kv) | 预设库 添加UI_COMP_EVENT_TYPE键值对 |
| [set_unit_key_ui_comp_attr_kv](#set_unit_key_ui_comp_attr_kv) | 预设库 添加UI_COMP_ATTR键值对 |
| [set_unit_key_ui_comp_align_type_kv](#set_unit_key_ui_comp_align_type_kv) | 预设库 添加UI_COMP_ALIGN_TYPE键值对 |
| [set_unit_key_ui_prefab_kv](#set_unit_key_ui_prefab_kv) | 预设库 添加UI_PREFAB键值对 |
| [set_unit_key_ui_prefab_instance_kv](#set_unit_key_ui_prefab_instance_kv) | 预设库 添加UI_PREFAB_INSTANCE键值对 |
| [set_unit_key_ui_prefab_ins_uid_kv](#set_unit_key_ui_prefab_ins_uid_kv) | 预设库 添加UI_PREFAB_INS_UID键值对 |
| [set_unit_key_ui_direction_kv](#set_unit_key_ui_direction_kv) | 预设库 添加UI_DIRECTION键值对 |
| [set_unit_key_ui_model_camera_mod_kv](#set_unit_key_ui_model_camera_mod_kv) | 预设库 添加UI_MODEL_CAMERA_MOD键值对 |
| [set_unit_key_ui_btn_status_kv](#set_unit_key_ui_btn_status_kv) | 预设库 添加UI_BTN_STATUS键值对 |
| [set_unit_key_ui_scrollview_type_kv](#set_unit_key_ui_scrollview_type_kv) | 预设库 添加UI_SCROLLVIEW_TYPE键值对 |
| [set_unit_key_ui_anim_kv](#set_unit_key_ui_anim_kv) | 预设库 添加UI_ANIM键值对 |
| [set_unit_key_ui_anim_curve_kv](#set_unit_key_ui_anim_curve_kv) | 预设库 添加UI_ANIM_CURVE键值对 |
| [set_unit_key_audio_channel_kv](#set_unit_key_audio_channel_kv) | 预设库 添加AUDIO_CHANNEL键值对 |
| [set_unit_key_unit_entity_kv](#set_unit_key_unit_entity_kv) | 预设库 添加UNIT_ENTITY键值对 |
| [set_unit_key_unit_group_kv](#set_unit_key_unit_group_kv) | 预设库 添加UNIT_GROUP键值对 |
| [set_unit_key_unit_name_kv](#set_unit_key_unit_name_kv) | 预设库 添加UNIT_NAME键值对 |
| [set_unit_key_unit_name_pool_kv](#set_unit_key_unit_name_pool_kv) | 预设库 添加UNIT_NAME_POOL键值对 |
| [set_unit_key_unit_write_attribute_kv](#set_unit_key_unit_write_attribute_kv) | 预设库 添加UNIT_WRITE_ATTRIBUTE键值对 |
| [set_unit_key_attr_element_kv](#set_unit_key_attr_element_kv) | 预设库 添加ATTR_ELEMENT键值对 |
| [set_unit_key_attr_element_read_kv](#set_unit_key_attr_element_read_kv) | 预设库 添加ATTR_ELEMENT_READ键值对 |
| [set_unit_key_mover_entity_kv](#set_unit_key_mover_entity_kv) | 预设库 添加MOVER_ENTITY键值对 |
| [set_unit_key_image_quality_kv](#set_unit_key_image_quality_kv) | 预设库 添加IMAGE_QUALITY键值对 |
| [set_unit_key_window_type_setting_kv](#set_unit_key_window_type_setting_kv) | 预设库 添加WINDOW_TYPE_SETTING键值对 |
| [set_unit_key_item_entity_kv](#set_unit_key_item_entity_kv) | 预设库 添加ITEM_ENTITY键值对 |
| [set_unit_key_item_group_kv](#set_unit_key_item_group_kv) | 预设库 添加ITEM_GROUP键值对 |
| [set_unit_key_item_name_kv](#set_unit_key_item_name_kv) | 预设库 添加ITEM_NAME键值对 |
| [set_unit_key_ability_kv](#set_unit_key_ability_kv) | 预设库 添加ABILITY键值对 |
| [set_unit_key_ability_type_kv](#set_unit_key_ability_type_kv) | 预设库 添加ABILITY_TYPE键值对 |
| [set_unit_key_ability_cast_type_kv](#set_unit_key_ability_cast_type_kv) | 预设库 添加ABILITY_CAST_TYPE键值对 |
| [set_unit_key_ability_name_kv](#set_unit_key_ability_name_kv) | 预设库 添加ABILITY_NAME键值对 |
| [set_unit_key_skill_pointer_type_kv](#set_unit_key_skill_pointer_type_kv) | 预设库 添加SKILL_POINTER_TYPE键值对 |
| [set_unit_key_modifier_entity_kv](#set_unit_key_modifier_entity_kv) | 预设库 添加MODIFIER_ENTITY键值对 |
| [set_unit_key_modifier_type_kv](#set_unit_key_modifier_type_kv) | 预设库 添加MODIFIER_TYPE键值对 |
| [set_unit_key_modifier_effect_type_kv](#set_unit_key_modifier_effect_type_kv) | 预设库 添加MODIFIER_EFFECT_TYPE键值对 |
| [set_unit_key_modifier_kv](#set_unit_key_modifier_kv) | 预设库 添加MODIFIER键值对 |
| [set_unit_key_projectile_kv](#set_unit_key_projectile_kv) | 预设库 添加PROJECTILE键值对 |
| [set_unit_key_projectile_entity_kv](#set_unit_key_projectile_entity_kv) | 预设库 添加PROJECTILE_ENTITY键值对 |
| [set_unit_key_projectile_group_kv](#set_unit_key_projectile_group_kv) | 预设库 添加PROJECTILE_GROUP键值对 |
| [set_unit_key_destructible_entity_kv](#set_unit_key_destructible_entity_kv) | 预设库 添加DESTRUCTIBLE_ENTITY键值对 |
| [set_unit_key_destructible_name_kv](#set_unit_key_destructible_name_kv) | 预设库 添加DESTRUCTIBLE_NAME键值对 |
| [set_unit_key_sound_entity_kv](#set_unit_key_sound_entity_kv) | 预设库 添加SOUND_ENTITY键值对 |
| [set_unit_key_audio_key_kv](#set_unit_key_audio_key_kv) | 预设库 添加AUDIO_KEY键值对 |
| [set_unit_key_game_mode_kv](#set_unit_key_game_mode_kv) | 预设库 添加GAME_MODE键值对 |
| [set_unit_key_player_kv](#set_unit_key_player_kv) | 预设库 添加PLAYER键值对 |
| [set_unit_key_player_group_kv](#set_unit_key_player_group_kv) | 预设库 添加PLAYER_GROUP键值对 |
| [set_unit_key_role_res_key_kv](#set_unit_key_role_res_key_kv) | 预设库 添加ROLE_RES_KEY键值对 |
| [set_unit_key_role_status_kv](#set_unit_key_role_status_kv) | 预设库 添加ROLE_STATUS键值对 |
| [set_unit_key_role_type_kv](#set_unit_key_role_type_kv) | 预设库 添加ROLE_TYPE键值对 |
| [set_unit_key_role_relation_kv](#set_unit_key_role_relation_kv) | 预设库 添加ROLE_RELATION键值对 |
| [set_unit_key_team_kv](#set_unit_key_team_kv) | 预设库 添加TEAM键值对 |
| [set_unit_key_point_kv](#set_unit_key_point_kv) | 预设库 添加POINT键值对 |
| [set_unit_key_vector3_kv](#set_unit_key_vector3_kv) | 预设库 添加VECTOR3键值对 |
| [set_unit_key_rotation_kv](#set_unit_key_rotation_kv) | 预设库 添加ROTATION键值对 |
| [set_unit_key_point_list_kv](#set_unit_key_point_list_kv) | 预设库 添加POINT_LIST键值对 |
| [set_unit_key_rectangle_kv](#set_unit_key_rectangle_kv) | 预设库 添加RECTANGLE键值对 |
| [set_unit_key_round_area_kv](#set_unit_key_round_area_kv) | 预设库 添加ROUND_AREA键值对 |
| [set_unit_key_polygon_kv](#set_unit_key_polygon_kv) | 预设库 添加POLYGON键值对 |
| [set_unit_key_camera_kv](#set_unit_key_camera_kv) | 预设库 添加CAMERA键值对 |
| [set_unit_key_camline_kv](#set_unit_key_camline_kv) | 预设库 添加CAMLINE键值对 |
| [set_unit_key_point_light_kv](#set_unit_key_point_light_kv) | 预设库 添加POINT_LIGHT键值对 |
| [set_unit_key_spot_light_kv](#set_unit_key_spot_light_kv) | 预设库 添加SPOT_LIGHT键值对 |
| [set_unit_key_fog_kv](#set_unit_key_fog_kv) | 预设库 添加FOG键值对 |
| [set_unit_key_scene_sound_kv](#set_unit_key_scene_sound_kv) | 预设库 添加SCENE_SOUND键值对 |
| [set_unit_key_model_kv](#set_unit_key_model_kv) | 预设库 添加MODEL键值对 |
| [set_unit_key_sfx_entity_kv](#set_unit_key_sfx_entity_kv) | 预设库 添加SFX_ENTITY键值对 |
| [set_unit_key_sfx_key_kv](#set_unit_key_sfx_key_kv) | 预设库 添加SFX_KEY键值对 |
| [set_unit_key_link_sfx_entity_kv](#set_unit_key_link_sfx_entity_kv) | 预设库 添加LINK_SFX_ENTITY键值对 |
| [set_unit_key_link_sfx_key_kv](#set_unit_key_link_sfx_key_kv) | 预设库 添加LINK_SFX_KEY键值对 |
| [set_unit_key_cursor_key_kv](#set_unit_key_cursor_key_kv) | 预设库 添加CURSOR_KEY键值对 |
| [set_unit_key_angle_kv](#set_unit_key_angle_kv) | 预设库 添加ANGLE键值对 |
| [set_unit_key_texture_kv](#set_unit_key_texture_kv) | 预设库 添加TEXTURE键值对 |
| [set_unit_key_sequence_kv](#set_unit_key_sequence_kv) | 预设库 添加SEQUENCE键值对 |
| [set_unit_key_physics_object_kv](#set_unit_key_physics_object_kv) | 预设库 添加PHYSICS_OBJECT键值对 |
| [set_unit_key_physics_entity_kv](#set_unit_key_physics_entity_kv) | 预设库 添加PHYSICS_ENTITY键值对 |
| [set_unit_key_physics_object_key_kv](#set_unit_key_physics_object_key_kv) | 预设库 添加PHYSICS_OBJECT_KEY键值对 |
| [set_unit_key_physics_entity_key_kv](#set_unit_key_physics_entity_key_kv) | 预设库 添加PHYSICS_ENTITY_KEY键值对 |
| [set_unit_key_rigid_body_kv](#set_unit_key_rigid_body_kv) | 预设库 添加RIGID_BODY键值对 |
| [set_unit_key_rigid_body_group_kv](#set_unit_key_rigid_body_group_kv) | 预设库 添加RIGID_BODY_GROUP键值对 |
| [set_unit_key_collider_kv](#set_unit_key_collider_kv) | 预设库 添加COLLIDER键值对 |
| [set_unit_key_joint_kv](#set_unit_key_joint_kv) | 预设库 添加JOINT键值对 |
| [set_unit_key_reaction_kv](#set_unit_key_reaction_kv) | 预设库 添加REACTION键值对 |
| [set_unit_key_reaction_group_kv](#set_unit_key_reaction_group_kv) | 预设库 添加REACTION_GROUP键值对 |
| [set_unit_key_dynamic_trigger_instance_kv](#set_unit_key_dynamic_trigger_instance_kv) | 预设库 添加DYNAMIC_TRIGGER_INSTANCE键值对 |
| [set_unit_key_table_kv](#set_unit_key_table_kv) | 预设库 添加TABLE键值对 |
| [set_unit_key_random_pool_kv](#set_unit_key_random_pool_kv) | 预设库 添加RANDOM_POOL键值对 |
| [set_unit_key_scene_ui_kv](#set_unit_key_scene_ui_kv) | 预设库 添加SCENE_UI键值对 |
| [set_unit_key_damage_type_kv](#set_unit_key_damage_type_kv) | 预设库 添加DAMAGE_TYPE键值对 |
| [set_unit_key_harm_text_type_new_kv](#set_unit_key_harm_text_type_new_kv) | 预设库 添加HARM_TEXT_TYPE_NEW键值对 |
| [set_unit_key_font_type_kv](#set_unit_key_font_type_kv) | 预设库 添加FONT_TYPE键值对 |
| [set_unit_key_jump_word_track_kv](#set_unit_key_jump_word_track_kv) | 预设库 添加JUMP_WORD_TRACK键值对 |
| [set_unit_key_new_timer_kv](#set_unit_key_new_timer_kv) | 预设库 添加NEW_TIMER键值对 |
| [set_unit_key_tech_key_kv](#set_unit_key_tech_key_kv) | 预设库 添加TECH_KEY键值对 |
| [set_unit_key_store_key_kv](#set_unit_key_store_key_kv) | 预设库 添加STORE_KEY键值对 |
| [set_unit_key_keyboard_key_kv](#set_unit_key_keyboard_key_kv) | 预设库 添加KEYBOARD_KEY键值对 |
| [set_unit_key_func_keyboard_key_kv](#set_unit_key_func_keyboard_key_kv) | 预设库 添加FUNC_KEYBOARD_KEY键值对 |
| [set_unit_key_mouse_key_kv](#set_unit_key_mouse_key_kv) | 预设库 添加MOUSE_KEY键值对 |
| [set_unit_key_mouse_wheel_kv](#set_unit_key_mouse_wheel_kv) | 预设库 添加MOUSE_WHEEL键值对 |
| [set_unit_key_post_effect_kv](#set_unit_key_post_effect_kv) | 预设库 添加POST_EFFECT键值对 |
| [set_unit_key_unit_type_kv](#set_unit_key_unit_type_kv) | 预设库 添加UNIT_TYPE键值对 |
| [set_unit_key_unit_command_type_kv](#set_unit_key_unit_command_type_kv) | 预设库 添加UNIT_COMMAND_TYPE键值对 |
| [set_unit_key_mini_map_color_type_kv](#set_unit_key_mini_map_color_type_kv) | 预设库 添加MINI_MAP_COLOR_TYPE键值对 |
| [set_unit_key_unit_behavior_kv](#set_unit_key_unit_behavior_kv) | 预设库 添加UNIT_BEHAVIOR键值对 |
| [set_unit_key_curved_path_kv](#set_unit_key_curved_path_kv) | 预设库 添加CURVED_PATH键值对 |
| [set_unit_key_curved_path_3d_kv](#set_unit_key_curved_path_3d_kv) | 预设库 添加CURVED_PATH_3D键值对 |
| [set_item_key_boolean_kv](#set_item_key_boolean_kv) | 预设库 添加BOOLEAN键值对 |
| [set_item_key_integer_kv](#set_item_key_integer_kv) | 预设库 添加INTEGER键值对 |
| [set_item_key_float_kv](#set_item_key_float_kv) | 预设库 添加FLOAT键值对 |
| [set_item_key_string_kv](#set_item_key_string_kv) | 预设库 添加STRING键值对 |
| [set_item_key_ui_comp_kv](#set_item_key_ui_comp_kv) | 预设库 添加UI_COMP键值对 |
| [set_item_key_ui_comp_type_kv](#set_item_key_ui_comp_type_kv) | 预设库 添加UI_COMP_TYPE键值对 |
| [set_item_key_ui_comp_event_type_kv](#set_item_key_ui_comp_event_type_kv) | 预设库 添加UI_COMP_EVENT_TYPE键值对 |
| [set_item_key_ui_comp_attr_kv](#set_item_key_ui_comp_attr_kv) | 预设库 添加UI_COMP_ATTR键值对 |
| [set_item_key_ui_comp_align_type_kv](#set_item_key_ui_comp_align_type_kv) | 预设库 添加UI_COMP_ALIGN_TYPE键值对 |
| [set_item_key_ui_prefab_kv](#set_item_key_ui_prefab_kv) | 预设库 添加UI_PREFAB键值对 |
| [set_item_key_ui_prefab_instance_kv](#set_item_key_ui_prefab_instance_kv) | 预设库 添加UI_PREFAB_INSTANCE键值对 |
| [set_item_key_ui_prefab_ins_uid_kv](#set_item_key_ui_prefab_ins_uid_kv) | 预设库 添加UI_PREFAB_INS_UID键值对 |
| [set_item_key_ui_direction_kv](#set_item_key_ui_direction_kv) | 预设库 添加UI_DIRECTION键值对 |
| [set_item_key_ui_model_camera_mod_kv](#set_item_key_ui_model_camera_mod_kv) | 预设库 添加UI_MODEL_CAMERA_MOD键值对 |
| [set_item_key_ui_btn_status_kv](#set_item_key_ui_btn_status_kv) | 预设库 添加UI_BTN_STATUS键值对 |
| [set_item_key_ui_scrollview_type_kv](#set_item_key_ui_scrollview_type_kv) | 预设库 添加UI_SCROLLVIEW_TYPE键值对 |
| [set_item_key_ui_anim_kv](#set_item_key_ui_anim_kv) | 预设库 添加UI_ANIM键值对 |
| [set_item_key_ui_anim_curve_kv](#set_item_key_ui_anim_curve_kv) | 预设库 添加UI_ANIM_CURVE键值对 |
| [set_item_key_audio_channel_kv](#set_item_key_audio_channel_kv) | 预设库 添加AUDIO_CHANNEL键值对 |
| [set_item_key_unit_entity_kv](#set_item_key_unit_entity_kv) | 预设库 添加UNIT_ENTITY键值对 |
| [set_item_key_unit_group_kv](#set_item_key_unit_group_kv) | 预设库 添加UNIT_GROUP键值对 |
| [set_item_key_unit_name_kv](#set_item_key_unit_name_kv) | 预设库 添加UNIT_NAME键值对 |
| [set_item_key_unit_name_pool_kv](#set_item_key_unit_name_pool_kv) | 预设库 添加UNIT_NAME_POOL键值对 |
| [set_item_key_unit_write_attribute_kv](#set_item_key_unit_write_attribute_kv) | 预设库 添加UNIT_WRITE_ATTRIBUTE键值对 |
| [set_item_key_attr_element_kv](#set_item_key_attr_element_kv) | 预设库 添加ATTR_ELEMENT键值对 |
| [set_item_key_attr_element_read_kv](#set_item_key_attr_element_read_kv) | 预设库 添加ATTR_ELEMENT_READ键值对 |
| [set_item_key_mover_entity_kv](#set_item_key_mover_entity_kv) | 预设库 添加MOVER_ENTITY键值对 |
| [set_item_key_image_quality_kv](#set_item_key_image_quality_kv) | 预设库 添加IMAGE_QUALITY键值对 |
| [set_item_key_window_type_setting_kv](#set_item_key_window_type_setting_kv) | 预设库 添加WINDOW_TYPE_SETTING键值对 |
| [set_item_key_item_entity_kv](#set_item_key_item_entity_kv) | 预设库 添加ITEM_ENTITY键值对 |
| [set_item_key_item_group_kv](#set_item_key_item_group_kv) | 预设库 添加ITEM_GROUP键值对 |
| [set_item_key_item_name_kv](#set_item_key_item_name_kv) | 预设库 添加ITEM_NAME键值对 |
| [set_item_key_ability_kv](#set_item_key_ability_kv) | 预设库 添加ABILITY键值对 |
| [set_item_key_ability_type_kv](#set_item_key_ability_type_kv) | 预设库 添加ABILITY_TYPE键值对 |
| [set_item_key_ability_cast_type_kv](#set_item_key_ability_cast_type_kv) | 预设库 添加ABILITY_CAST_TYPE键值对 |
| [set_item_key_ability_name_kv](#set_item_key_ability_name_kv) | 预设库 添加ABILITY_NAME键值对 |
| [set_item_key_skill_pointer_type_kv](#set_item_key_skill_pointer_type_kv) | 预设库 添加SKILL_POINTER_TYPE键值对 |
| [set_item_key_modifier_entity_kv](#set_item_key_modifier_entity_kv) | 预设库 添加MODIFIER_ENTITY键值对 |
| [set_item_key_modifier_type_kv](#set_item_key_modifier_type_kv) | 预设库 添加MODIFIER_TYPE键值对 |
| [set_item_key_modifier_effect_type_kv](#set_item_key_modifier_effect_type_kv) | 预设库 添加MODIFIER_EFFECT_TYPE键值对 |
| [set_item_key_modifier_kv](#set_item_key_modifier_kv) | 预设库 添加MODIFIER键值对 |
| [set_item_key_projectile_kv](#set_item_key_projectile_kv) | 预设库 添加PROJECTILE键值对 |
| [set_item_key_projectile_entity_kv](#set_item_key_projectile_entity_kv) | 预设库 添加PROJECTILE_ENTITY键值对 |
| [set_item_key_projectile_group_kv](#set_item_key_projectile_group_kv) | 预设库 添加PROJECTILE_GROUP键值对 |
| [set_item_key_destructible_entity_kv](#set_item_key_destructible_entity_kv) | 预设库 添加DESTRUCTIBLE_ENTITY键值对 |
| [set_item_key_destructible_name_kv](#set_item_key_destructible_name_kv) | 预设库 添加DESTRUCTIBLE_NAME键值对 |
| [set_item_key_sound_entity_kv](#set_item_key_sound_entity_kv) | 预设库 添加SOUND_ENTITY键值对 |
| [set_item_key_audio_key_kv](#set_item_key_audio_key_kv) | 预设库 添加AUDIO_KEY键值对 |
| [set_item_key_game_mode_kv](#set_item_key_game_mode_kv) | 预设库 添加GAME_MODE键值对 |
| [set_item_key_player_kv](#set_item_key_player_kv) | 预设库 添加PLAYER键值对 |
| [set_item_key_player_group_kv](#set_item_key_player_group_kv) | 预设库 添加PLAYER_GROUP键值对 |
| [set_item_key_role_res_key_kv](#set_item_key_role_res_key_kv) | 预设库 添加ROLE_RES_KEY键值对 |
| [set_item_key_role_status_kv](#set_item_key_role_status_kv) | 预设库 添加ROLE_STATUS键值对 |
| [set_item_key_role_type_kv](#set_item_key_role_type_kv) | 预设库 添加ROLE_TYPE键值对 |
| [set_item_key_role_relation_kv](#set_item_key_role_relation_kv) | 预设库 添加ROLE_RELATION键值对 |
| [set_item_key_team_kv](#set_item_key_team_kv) | 预设库 添加TEAM键值对 |
| [set_item_key_point_kv](#set_item_key_point_kv) | 预设库 添加POINT键值对 |
| [set_item_key_vector3_kv](#set_item_key_vector3_kv) | 预设库 添加VECTOR3键值对 |
| [set_item_key_rotation_kv](#set_item_key_rotation_kv) | 预设库 添加ROTATION键值对 |
| [set_item_key_point_list_kv](#set_item_key_point_list_kv) | 预设库 添加POINT_LIST键值对 |
| [set_item_key_rectangle_kv](#set_item_key_rectangle_kv) | 预设库 添加RECTANGLE键值对 |
| [set_item_key_round_area_kv](#set_item_key_round_area_kv) | 预设库 添加ROUND_AREA键值对 |
| [set_item_key_polygon_kv](#set_item_key_polygon_kv) | 预设库 添加POLYGON键值对 |
| [set_item_key_camera_kv](#set_item_key_camera_kv) | 预设库 添加CAMERA键值对 |
| [set_item_key_camline_kv](#set_item_key_camline_kv) | 预设库 添加CAMLINE键值对 |
| [set_item_key_point_light_kv](#set_item_key_point_light_kv) | 预设库 添加POINT_LIGHT键值对 |
| [set_item_key_spot_light_kv](#set_item_key_spot_light_kv) | 预设库 添加SPOT_LIGHT键值对 |
| [set_item_key_fog_kv](#set_item_key_fog_kv) | 预设库 添加FOG键值对 |
| [set_item_key_scene_sound_kv](#set_item_key_scene_sound_kv) | 预设库 添加SCENE_SOUND键值对 |
| [set_item_key_model_kv](#set_item_key_model_kv) | 预设库 添加MODEL键值对 |
| [set_item_key_sfx_entity_kv](#set_item_key_sfx_entity_kv) | 预设库 添加SFX_ENTITY键值对 |
| [set_item_key_sfx_key_kv](#set_item_key_sfx_key_kv) | 预设库 添加SFX_KEY键值对 |
| [set_item_key_link_sfx_entity_kv](#set_item_key_link_sfx_entity_kv) | 预设库 添加LINK_SFX_ENTITY键值对 |
| [set_item_key_link_sfx_key_kv](#set_item_key_link_sfx_key_kv) | 预设库 添加LINK_SFX_KEY键值对 |
| [set_item_key_cursor_key_kv](#set_item_key_cursor_key_kv) | 预设库 添加CURSOR_KEY键值对 |
| [set_item_key_angle_kv](#set_item_key_angle_kv) | 预设库 添加ANGLE键值对 |
| [set_item_key_texture_kv](#set_item_key_texture_kv) | 预设库 添加TEXTURE键值对 |
| [set_item_key_sequence_kv](#set_item_key_sequence_kv) | 预设库 添加SEQUENCE键值对 |
| [set_item_key_physics_object_kv](#set_item_key_physics_object_kv) | 预设库 添加PHYSICS_OBJECT键值对 |
| [set_item_key_physics_entity_kv](#set_item_key_physics_entity_kv) | 预设库 添加PHYSICS_ENTITY键值对 |
| [set_item_key_physics_object_key_kv](#set_item_key_physics_object_key_kv) | 预设库 添加PHYSICS_OBJECT_KEY键值对 |
| [set_item_key_physics_entity_key_kv](#set_item_key_physics_entity_key_kv) | 预设库 添加PHYSICS_ENTITY_KEY键值对 |
| [set_item_key_rigid_body_kv](#set_item_key_rigid_body_kv) | 预设库 添加RIGID_BODY键值对 |
| [set_item_key_rigid_body_group_kv](#set_item_key_rigid_body_group_kv) | 预设库 添加RIGID_BODY_GROUP键值对 |
| [set_item_key_collider_kv](#set_item_key_collider_kv) | 预设库 添加COLLIDER键值对 |
| [set_item_key_joint_kv](#set_item_key_joint_kv) | 预设库 添加JOINT键值对 |
| [set_item_key_reaction_kv](#set_item_key_reaction_kv) | 预设库 添加REACTION键值对 |
| [set_item_key_reaction_group_kv](#set_item_key_reaction_group_kv) | 预设库 添加REACTION_GROUP键值对 |
| [set_item_key_dynamic_trigger_instance_kv](#set_item_key_dynamic_trigger_instance_kv) | 预设库 添加DYNAMIC_TRIGGER_INSTANCE键值对 |
| [set_item_key_table_kv](#set_item_key_table_kv) | 预设库 添加TABLE键值对 |
| [set_item_key_random_pool_kv](#set_item_key_random_pool_kv) | 预设库 添加RANDOM_POOL键值对 |
| [set_item_key_scene_ui_kv](#set_item_key_scene_ui_kv) | 预设库 添加SCENE_UI键值对 |
| [set_item_key_damage_type_kv](#set_item_key_damage_type_kv) | 预设库 添加DAMAGE_TYPE键值对 |
| [set_item_key_harm_text_type_new_kv](#set_item_key_harm_text_type_new_kv) | 预设库 添加HARM_TEXT_TYPE_NEW键值对 |
| [set_item_key_font_type_kv](#set_item_key_font_type_kv) | 预设库 添加FONT_TYPE键值对 |
| [set_item_key_jump_word_track_kv](#set_item_key_jump_word_track_kv) | 预设库 添加JUMP_WORD_TRACK键值对 |
| [set_item_key_new_timer_kv](#set_item_key_new_timer_kv) | 预设库 添加NEW_TIMER键值对 |
| [set_item_key_tech_key_kv](#set_item_key_tech_key_kv) | 预设库 添加TECH_KEY键值对 |
| [set_item_key_store_key_kv](#set_item_key_store_key_kv) | 预设库 添加STORE_KEY键值对 |
| [set_item_key_keyboard_key_kv](#set_item_key_keyboard_key_kv) | 预设库 添加KEYBOARD_KEY键值对 |
| [set_item_key_func_keyboard_key_kv](#set_item_key_func_keyboard_key_kv) | 预设库 添加FUNC_KEYBOARD_KEY键值对 |
| [set_item_key_mouse_key_kv](#set_item_key_mouse_key_kv) | 预设库 添加MOUSE_KEY键值对 |
| [set_item_key_mouse_wheel_kv](#set_item_key_mouse_wheel_kv) | 预设库 添加MOUSE_WHEEL键值对 |
| [set_item_key_post_effect_kv](#set_item_key_post_effect_kv) | 预设库 添加POST_EFFECT键值对 |
| [set_item_key_unit_type_kv](#set_item_key_unit_type_kv) | 预设库 添加UNIT_TYPE键值对 |
| [set_item_key_unit_command_type_kv](#set_item_key_unit_command_type_kv) | 预设库 添加UNIT_COMMAND_TYPE键值对 |
| [set_item_key_mini_map_color_type_kv](#set_item_key_mini_map_color_type_kv) | 预设库 添加MINI_MAP_COLOR_TYPE键值对 |
| [set_item_key_unit_behavior_kv](#set_item_key_unit_behavior_kv) | 预设库 添加UNIT_BEHAVIOR键值对 |
| [set_item_key_curved_path_kv](#set_item_key_curved_path_kv) | 预设库 添加CURVED_PATH键值对 |
| [set_item_key_curved_path_3d_kv](#set_item_key_curved_path_3d_kv) | 预设库 添加CURVED_PATH_3D键值对 |
| [set_ability_key_boolean_kv](#set_ability_key_boolean_kv) | 预设库 添加BOOLEAN键值对 |
| [set_ability_key_integer_kv](#set_ability_key_integer_kv) | 预设库 添加INTEGER键值对 |
| [set_ability_key_float_kv](#set_ability_key_float_kv) | 预设库 添加FLOAT键值对 |
| [set_ability_key_string_kv](#set_ability_key_string_kv) | 预设库 添加STRING键值对 |
| [set_ability_key_ui_comp_kv](#set_ability_key_ui_comp_kv) | 预设库 添加UI_COMP键值对 |
| [set_ability_key_ui_comp_type_kv](#set_ability_key_ui_comp_type_kv) | 预设库 添加UI_COMP_TYPE键值对 |
| [set_ability_key_ui_comp_event_type_kv](#set_ability_key_ui_comp_event_type_kv) | 预设库 添加UI_COMP_EVENT_TYPE键值对 |
| [set_ability_key_ui_comp_attr_kv](#set_ability_key_ui_comp_attr_kv) | 预设库 添加UI_COMP_ATTR键值对 |
| [set_ability_key_ui_comp_align_type_kv](#set_ability_key_ui_comp_align_type_kv) | 预设库 添加UI_COMP_ALIGN_TYPE键值对 |
| [set_ability_key_ui_prefab_kv](#set_ability_key_ui_prefab_kv) | 预设库 添加UI_PREFAB键值对 |
| [set_ability_key_ui_prefab_instance_kv](#set_ability_key_ui_prefab_instance_kv) | 预设库 添加UI_PREFAB_INSTANCE键值对 |
| [set_ability_key_ui_prefab_ins_uid_kv](#set_ability_key_ui_prefab_ins_uid_kv) | 预设库 添加UI_PREFAB_INS_UID键值对 |
| [set_ability_key_ui_direction_kv](#set_ability_key_ui_direction_kv) | 预设库 添加UI_DIRECTION键值对 |
| [set_ability_key_ui_model_camera_mod_kv](#set_ability_key_ui_model_camera_mod_kv) | 预设库 添加UI_MODEL_CAMERA_MOD键值对 |
| [set_ability_key_ui_btn_status_kv](#set_ability_key_ui_btn_status_kv) | 预设库 添加UI_BTN_STATUS键值对 |
| [set_ability_key_ui_scrollview_type_kv](#set_ability_key_ui_scrollview_type_kv) | 预设库 添加UI_SCROLLVIEW_TYPE键值对 |
| [set_ability_key_ui_anim_kv](#set_ability_key_ui_anim_kv) | 预设库 添加UI_ANIM键值对 |
| [set_ability_key_ui_anim_curve_kv](#set_ability_key_ui_anim_curve_kv) | 预设库 添加UI_ANIM_CURVE键值对 |
| [set_ability_key_audio_channel_kv](#set_ability_key_audio_channel_kv) | 预设库 添加AUDIO_CHANNEL键值对 |
| [set_ability_key_unit_entity_kv](#set_ability_key_unit_entity_kv) | 预设库 添加UNIT_ENTITY键值对 |
| [set_ability_key_unit_group_kv](#set_ability_key_unit_group_kv) | 预设库 添加UNIT_GROUP键值对 |
| [set_ability_key_unit_name_kv](#set_ability_key_unit_name_kv) | 预设库 添加UNIT_NAME键值对 |
| [set_ability_key_unit_name_pool_kv](#set_ability_key_unit_name_pool_kv) | 预设库 添加UNIT_NAME_POOL键值对 |
| [set_ability_key_unit_write_attribute_kv](#set_ability_key_unit_write_attribute_kv) | 预设库 添加UNIT_WRITE_ATTRIBUTE键值对 |
| [set_ability_key_attr_element_kv](#set_ability_key_attr_element_kv) | 预设库 添加ATTR_ELEMENT键值对 |
| [set_ability_key_attr_element_read_kv](#set_ability_key_attr_element_read_kv) | 预设库 添加ATTR_ELEMENT_READ键值对 |
| [set_ability_key_mover_entity_kv](#set_ability_key_mover_entity_kv) | 预设库 添加MOVER_ENTITY键值对 |
| [set_ability_key_image_quality_kv](#set_ability_key_image_quality_kv) | 预设库 添加IMAGE_QUALITY键值对 |
| [set_ability_key_window_type_setting_kv](#set_ability_key_window_type_setting_kv) | 预设库 添加WINDOW_TYPE_SETTING键值对 |
| [set_ability_key_item_entity_kv](#set_ability_key_item_entity_kv) | 预设库 添加ITEM_ENTITY键值对 |
| [set_ability_key_item_group_kv](#set_ability_key_item_group_kv) | 预设库 添加ITEM_GROUP键值对 |
| [set_ability_key_item_name_kv](#set_ability_key_item_name_kv) | 预设库 添加ITEM_NAME键值对 |
| [set_ability_key_ability_kv](#set_ability_key_ability_kv) | 预设库 添加ABILITY键值对 |
| [set_ability_key_ability_type_kv](#set_ability_key_ability_type_kv) | 预设库 添加ABILITY_TYPE键值对 |
| [set_ability_key_ability_cast_type_kv](#set_ability_key_ability_cast_type_kv) | 预设库 添加ABILITY_CAST_TYPE键值对 |
| [set_ability_key_ability_name_kv](#set_ability_key_ability_name_kv) | 预设库 添加ABILITY_NAME键值对 |
| [set_ability_key_skill_pointer_type_kv](#set_ability_key_skill_pointer_type_kv) | 预设库 添加SKILL_POINTER_TYPE键值对 |
| [set_ability_key_modifier_entity_kv](#set_ability_key_modifier_entity_kv) | 预设库 添加MODIFIER_ENTITY键值对 |
| [set_ability_key_modifier_type_kv](#set_ability_key_modifier_type_kv) | 预设库 添加MODIFIER_TYPE键值对 |
| [set_ability_key_modifier_effect_type_kv](#set_ability_key_modifier_effect_type_kv) | 预设库 添加MODIFIER_EFFECT_TYPE键值对 |
| [set_ability_key_modifier_kv](#set_ability_key_modifier_kv) | 预设库 添加MODIFIER键值对 |
| [set_ability_key_projectile_kv](#set_ability_key_projectile_kv) | 预设库 添加PROJECTILE键值对 |
| [set_ability_key_projectile_entity_kv](#set_ability_key_projectile_entity_kv) | 预设库 添加PROJECTILE_ENTITY键值对 |
| [set_ability_key_projectile_group_kv](#set_ability_key_projectile_group_kv) | 预设库 添加PROJECTILE_GROUP键值对 |
| [set_ability_key_destructible_entity_kv](#set_ability_key_destructible_entity_kv) | 预设库 添加DESTRUCTIBLE_ENTITY键值对 |
| [set_ability_key_destructible_name_kv](#set_ability_key_destructible_name_kv) | 预设库 添加DESTRUCTIBLE_NAME键值对 |
| [set_ability_key_sound_entity_kv](#set_ability_key_sound_entity_kv) | 预设库 添加SOUND_ENTITY键值对 |
| [set_ability_key_audio_key_kv](#set_ability_key_audio_key_kv) | 预设库 添加AUDIO_KEY键值对 |
| [set_ability_key_game_mode_kv](#set_ability_key_game_mode_kv) | 预设库 添加GAME_MODE键值对 |
| [set_ability_key_player_kv](#set_ability_key_player_kv) | 预设库 添加PLAYER键值对 |
| [set_ability_key_player_group_kv](#set_ability_key_player_group_kv) | 预设库 添加PLAYER_GROUP键值对 |
| [set_ability_key_role_res_key_kv](#set_ability_key_role_res_key_kv) | 预设库 添加ROLE_RES_KEY键值对 |
| [set_ability_key_role_status_kv](#set_ability_key_role_status_kv) | 预设库 添加ROLE_STATUS键值对 |
| [set_ability_key_role_type_kv](#set_ability_key_role_type_kv) | 预设库 添加ROLE_TYPE键值对 |
| [set_ability_key_role_relation_kv](#set_ability_key_role_relation_kv) | 预设库 添加ROLE_RELATION键值对 |
| [set_ability_key_team_kv](#set_ability_key_team_kv) | 预设库 添加TEAM键值对 |
| [set_ability_key_point_kv](#set_ability_key_point_kv) | 预设库 添加POINT键值对 |
| [set_ability_key_vector3_kv](#set_ability_key_vector3_kv) | 预设库 添加VECTOR3键值对 |
| [set_ability_key_rotation_kv](#set_ability_key_rotation_kv) | 预设库 添加ROTATION键值对 |
| [set_ability_key_point_list_kv](#set_ability_key_point_list_kv) | 预设库 添加POINT_LIST键值对 |
| [set_ability_key_rectangle_kv](#set_ability_key_rectangle_kv) | 预设库 添加RECTANGLE键值对 |
| [set_ability_key_round_area_kv](#set_ability_key_round_area_kv) | 预设库 添加ROUND_AREA键值对 |
| [set_ability_key_polygon_kv](#set_ability_key_polygon_kv) | 预设库 添加POLYGON键值对 |
| [set_ability_key_camera_kv](#set_ability_key_camera_kv) | 预设库 添加CAMERA键值对 |
| [set_ability_key_camline_kv](#set_ability_key_camline_kv) | 预设库 添加CAMLINE键值对 |
| [set_ability_key_point_light_kv](#set_ability_key_point_light_kv) | 预设库 添加POINT_LIGHT键值对 |
| [set_ability_key_spot_light_kv](#set_ability_key_spot_light_kv) | 预设库 添加SPOT_LIGHT键值对 |
| [set_ability_key_fog_kv](#set_ability_key_fog_kv) | 预设库 添加FOG键值对 |
| [set_ability_key_scene_sound_kv](#set_ability_key_scene_sound_kv) | 预设库 添加SCENE_SOUND键值对 |
| [set_ability_key_model_kv](#set_ability_key_model_kv) | 预设库 添加MODEL键值对 |
| [set_ability_key_sfx_entity_kv](#set_ability_key_sfx_entity_kv) | 预设库 添加SFX_ENTITY键值对 |
| [set_ability_key_sfx_key_kv](#set_ability_key_sfx_key_kv) | 预设库 添加SFX_KEY键值对 |
| [set_ability_key_link_sfx_entity_kv](#set_ability_key_link_sfx_entity_kv) | 预设库 添加LINK_SFX_ENTITY键值对 |
| [set_ability_key_link_sfx_key_kv](#set_ability_key_link_sfx_key_kv) | 预设库 添加LINK_SFX_KEY键值对 |
| [set_ability_key_cursor_key_kv](#set_ability_key_cursor_key_kv) | 预设库 添加CURSOR_KEY键值对 |
| [set_ability_key_angle_kv](#set_ability_key_angle_kv) | 预设库 添加ANGLE键值对 |
| [set_ability_key_texture_kv](#set_ability_key_texture_kv) | 预设库 添加TEXTURE键值对 |
| [set_ability_key_sequence_kv](#set_ability_key_sequence_kv) | 预设库 添加SEQUENCE键值对 |
| [set_ability_key_physics_object_kv](#set_ability_key_physics_object_kv) | 预设库 添加PHYSICS_OBJECT键值对 |
| [set_ability_key_physics_entity_kv](#set_ability_key_physics_entity_kv) | 预设库 添加PHYSICS_ENTITY键值对 |
| [set_ability_key_physics_object_key_kv](#set_ability_key_physics_object_key_kv) | 预设库 添加PHYSICS_OBJECT_KEY键值对 |
| [set_ability_key_physics_entity_key_kv](#set_ability_key_physics_entity_key_kv) | 预设库 添加PHYSICS_ENTITY_KEY键值对 |
| [set_ability_key_rigid_body_kv](#set_ability_key_rigid_body_kv) | 预设库 添加RIGID_BODY键值对 |
| [set_ability_key_rigid_body_group_kv](#set_ability_key_rigid_body_group_kv) | 预设库 添加RIGID_BODY_GROUP键值对 |
| [set_ability_key_collider_kv](#set_ability_key_collider_kv) | 预设库 添加COLLIDER键值对 |
| [set_ability_key_joint_kv](#set_ability_key_joint_kv) | 预设库 添加JOINT键值对 |
| [set_ability_key_reaction_kv](#set_ability_key_reaction_kv) | 预设库 添加REACTION键值对 |
| [set_ability_key_reaction_group_kv](#set_ability_key_reaction_group_kv) | 预设库 添加REACTION_GROUP键值对 |
| [set_ability_key_dynamic_trigger_instance_kv](#set_ability_key_dynamic_trigger_instance_kv) | 预设库 添加DYNAMIC_TRIGGER_INSTANCE键值对 |
| [set_ability_key_table_kv](#set_ability_key_table_kv) | 预设库 添加TABLE键值对 |
| [set_ability_key_random_pool_kv](#set_ability_key_random_pool_kv) | 预设库 添加RANDOM_POOL键值对 |
| [set_ability_key_scene_ui_kv](#set_ability_key_scene_ui_kv) | 预设库 添加SCENE_UI键值对 |
| [set_ability_key_damage_type_kv](#set_ability_key_damage_type_kv) | 预设库 添加DAMAGE_TYPE键值对 |
| [set_ability_key_harm_text_type_new_kv](#set_ability_key_harm_text_type_new_kv) | 预设库 添加HARM_TEXT_TYPE_NEW键值对 |
| [set_ability_key_font_type_kv](#set_ability_key_font_type_kv) | 预设库 添加FONT_TYPE键值对 |
| [set_ability_key_jump_word_track_kv](#set_ability_key_jump_word_track_kv) | 预设库 添加JUMP_WORD_TRACK键值对 |
| [set_ability_key_new_timer_kv](#set_ability_key_new_timer_kv) | 预设库 添加NEW_TIMER键值对 |
| [set_ability_key_tech_key_kv](#set_ability_key_tech_key_kv) | 预设库 添加TECH_KEY键值对 |
| [set_ability_key_store_key_kv](#set_ability_key_store_key_kv) | 预设库 添加STORE_KEY键值对 |
| [set_ability_key_keyboard_key_kv](#set_ability_key_keyboard_key_kv) | 预设库 添加KEYBOARD_KEY键值对 |
| [set_ability_key_func_keyboard_key_kv](#set_ability_key_func_keyboard_key_kv) | 预设库 添加FUNC_KEYBOARD_KEY键值对 |
| [set_ability_key_mouse_key_kv](#set_ability_key_mouse_key_kv) | 预设库 添加MOUSE_KEY键值对 |
| [set_ability_key_mouse_wheel_kv](#set_ability_key_mouse_wheel_kv) | 预设库 添加MOUSE_WHEEL键值对 |
| [set_ability_key_post_effect_kv](#set_ability_key_post_effect_kv) | 预设库 添加POST_EFFECT键值对 |
| [set_ability_key_unit_type_kv](#set_ability_key_unit_type_kv) | 预设库 添加UNIT_TYPE键值对 |
| [set_ability_key_unit_command_type_kv](#set_ability_key_unit_command_type_kv) | 预设库 添加UNIT_COMMAND_TYPE键值对 |
| [set_ability_key_mini_map_color_type_kv](#set_ability_key_mini_map_color_type_kv) | 预设库 添加MINI_MAP_COLOR_TYPE键值对 |
| [set_ability_key_unit_behavior_kv](#set_ability_key_unit_behavior_kv) | 预设库 添加UNIT_BEHAVIOR键值对 |
| [set_ability_key_curved_path_kv](#set_ability_key_curved_path_kv) | 预设库 添加CURVED_PATH键值对 |
| [set_ability_key_curved_path_3d_kv](#set_ability_key_curved_path_3d_kv) | 预设库 添加CURVED_PATH_3D键值对 |
| [is_modifier_id](#is_modifier_id) | 判断BUFF是否是目标BUFFID的实例 |
| [is_modifier_instance](#is_modifier_instance) | 判断BUFF是否是目标BUFF实例 |
| [judge_modifier_effect_type](#judge_modifier_effect_type) | 判断BUFF是否是为目标类型的buff(正面负面等) |
| [get_type_of_modifier_entity](#get_type_of_modifier_entity) | 获取目标效果(BUFF)的效果类型 |
| [transfer_num_into_modifier_key](#transfer_num_into_modifier_key) | 转换目标数字ID到效果类型 |
| [api_get_name_of_modifier_key](#api_get_name_of_modifier_key) | 获取魔法效果类型的名称 |
| [create_modifier_editor_data](#create_modifier_editor_data) | 创建新魔法效果物编 |
| [get_last_compose_unit](#get_last_compose_unit) | 最近合成物品的单位 |
| [get_last_add_item](#get_last_add_item) | 最近添加物品 |
| [get_last_remove_item](#get_last_remove_item) | 最近移除物品 |
| [get_last_use_item](#get_last_use_item) | 最近使用物品 |
| [get_last_stack_changed_item](#get_last_stack_changed_item) | 最近堆叠变化物品 |
| [get_last_charge_changed_item](#get_last_charge_changed_item) | 最近充能变化物品 |
| [get_last_add_item_unit](#get_last_add_item_unit) | 最近添加物品单位 |
| [get_last_remove_item_unit](#get_last_remove_item_unit) | 最近移除物品单位 |
| [get_last_use_item_unit](#get_last_use_item_unit) | 最近使用物品单位 |
| [get_last_change_item_stack_unit](#get_last_change_item_stack_unit) | 最近物品层数变化单位 |
| [api_get_attr_of_item_key](#api_get_attr_of_item_key) | 获取物品类型附加属性 |
| [api_get_item_type_model](#api_get_item_type_model) | 获取物品类型的模型 |
| [api_get_value_of_item_name_comp_mat](#api_get_value_of_item_name_comp_mat) | 遍历物品类型合成所需的物品类型数量 |
| [api_get_value_of_item_name_comp_res](#api_get_value_of_item_name_comp_res) | 遍历物品类型合成所需的玩家属性数量 |
| [create_item_editor_data](#create_item_editor_data) | 创建新物品物编 |
| [api_get_item_key_res_cnt](#api_get_item_key_res_cnt) | 获取物品类型的购买所需资源 |
| [api_get_item_type_float_attr](#api_get_item_type_float_attr) | 获取物品类型的实数属性 |
| [api_get_item_type_int_attr](#api_get_item_type_int_attr) | 获取物品类型的整数属性 |
| [api_add_item_to_group](#api_add_item_to_group) | 添加物品到物品组 |
| [api_remove_item_in_group](#api_remove_item_in_group) | 删除物品组中某个物品 |
| [api_judge_item_in_group](#api_judge_item_in_group) | 判断物品是否在物品组 |
| [api_get_random_item_in_item_group](#api_get_random_item_in_item_group) | 物品组内随机一个单位 |
| [get_last_buy_shop_item](#get_last_buy_shop_item) | 最近被购买物品 |
| [get_last_sell_shop_item](#get_last_sell_shop_item) | 最近被出售物品 |
| [get_last_buyer_unit](#get_last_buyer_unit) | 最近购买者 |
| [get_last_seller_unit](#get_last_seller_unit) | 最近出售者 |
| [get_last_buy_shop_unit](#get_last_buy_shop_unit) | 最近被购买单位 |
| [get_last_upgraded_tech](#get_last_upgraded_tech) | 最近升级科技 |
| [get_last_operated_tech](#get_last_operated_tech) | 最近升降科技 |
| [get_last_changed_tech](#get_last_changed_tech) | 最近变化科技 |
| [get_last_changed_tech_level](#get_last_changed_tech_level) | 最近变化科技等级 |
| [get_last_added_tech](#get_last_added_tech) | 最近获得科技 |
| [get_last_removed_tech](#get_last_removed_tech) | 最近失去科技 |
| [get_last_upgrade_tech_unit](#get_last_upgrade_tech_unit) | 最近研究科技单位 |
| [get_last_add_tech_unit](#get_last_add_tech_unit) | 最近获得科技单位 |
| [get_last_remove_tech_unit](#get_last_remove_tech_unit) | 最近失去科技单位 |
| [get_tech_name](#get_tech_name) | 获取科技对应等级名字 |
| [get_tech_icon](#get_tech_icon) | 获取科技对应等级icon |
| [get_tech_cost](#get_tech_cost) | 获取科技对应等级的花费 |
| [get_tech_max_level](#get_tech_max_level) | 获取科技最大等级 |
| [create_technology_editor_data](#create_technology_editor_data) | 创建新科技物编 |
| [get_last_use_store_item_role](#get_last_use_store_item_role) | 最近成功使用收费道具玩家 |
| [set_function_return](#set_function_return) | 设置函数返回值 |
| [get_function_return_value](#get_function_return_value) | 获取函数返回值 |
| [send_event_custom](#send_event_custom) | 发送自定义事件 |
| [gen_param_dict](#gen_param_dict) | 生成字典 |
| [get_custom_param](#get_custom_param) | 获取字典中的值 |
| [eval_lua_code](#eval_lua_code) | 执行Lua代码 |
| [remove_unit_mover](#remove_unit_mover) | 删除单位运动器 |
| [break_unit_mover](#break_unit_mover) | 打断单位运动器 |
| [get_mover_collide_unit](#get_mover_collide_unit) | 运动器碰撞单位 |
| [create_chasing_mover](#create_chasing_mover) | 创建追踪运动器 |
| [create_straight_mover](#create_straight_mover) | 创建直线运动器 |
| [create_round_mover](#create_round_mover) | 创建环绕运动器 |
| [create_curved_mover](#create_curved_mover) | 创建曲线运动器 |
| [get_mover_type](#get_mover_type) | 获得运动器类型 |
| [remove_mover](#remove_mover) | 删除运动器 |
| [break_mover](#break_mover) | 打断运动器 |
| [get_unit_mover](#get_unit_mover) | 获得单位的运动器 |
| [get_mover_priority](#get_mover_priority) | 获取运动器的优先级 |
| [set_mover_priority](#set_mover_priority) | 设置运动器的优先级 |
| [set_mover_property](#set_mover_property) | 设置运动器的属性 |
| [get_mover_property](#get_mover_property) | 获取运动器的属性 |
| [get_mover_angle](#get_mover_angle) | 获得运动器的运动方向 |
| [set_mover_angle](#set_mover_angle) | 设置运动器的运动方向 |
| [set_mover_collision_radius](#set_mover_collision_radius) | 设置运动器的碰撞范围 |
| [get_mover_collision_radius](#get_mover_collision_radius) | 获得运动器的碰撞范围 |
| [set_mover_relate_unit](#set_mover_relate_unit) | 设置运动器的关联单位 |
| [get_mover_relate_unit](#get_mover_relate_unit) | 获得运动器的关联单位 |
| [set_mover_relate_ability](#set_mover_relate_ability) | 设置运动器的关联技能 |
| [get_mover_relate_ability](#get_mover_relate_ability) | 获得运动器的关联技能 |
| [create_unit_command_move_to_pos](#create_unit_command_move_to_pos) | 移动 |
| [create_unit_command_stop](#create_unit_command_stop) | 停止 |
| [create_unit_command_empty](#create_unit_command_empty) | 空状态 |
| [create_unit_command_hold](#create_unit_command_hold) | 驻守 |
| [create_unit_command_attack_move](#create_unit_command_attack_move) | 攻击移动 |
| [create_unit_command_attack_target](#create_unit_command_attack_target) | 攻击 |
| [create_unit_command_move_along_road](#create_unit_command_move_along_road) | 沿路径移动 |
| [create_unit_command_use_skill](#create_unit_command_use_skill) | 释放技能 |
| [create_unit_command_use_item](#create_unit_command_use_item) | 使用物品 |
| [create_unit_command_pick_item](#create_unit_command_pick_item) | 拾取物品 |
| [create_unit_command_drop_item](#create_unit_command_drop_item) | 丢弃物品 |
| [create_unit_command_transfer_item](#create_unit_command_transfer_item) | 转移物品 |
| [create_unit_command_follow](#create_unit_command_follow) | 跟随 |
| [get_modifier_key_ui_anim_play_mode_kv](#get_modifier_key_ui_anim_play_mode_kv) | 获取魔法效果特效编号UI_ANIM_PLAY_MODE键值对 |
| [get_projectile_key_ui_anim_play_mode_kv](#get_projectile_key_ui_anim_play_mode_kv) | 获取特效编号UI_ANIM_PLAY_MODE键值对 |
| [get_destructible_key_ui_anim_play_mode_kv](#get_destructible_key_ui_anim_play_mode_kv) | 获取可破坏物编号UI_ANIM_PLAY_MODE键值对 |
| [get_tech_key_ui_anim_play_mode_kv](#get_tech_key_ui_anim_play_mode_kv) | 获取科技编号UI_ANIM_PLAY_MODE键值对 |
| [get_icon_id_ui_anim_play_mode_kv](#get_icon_id_ui_anim_play_mode_kv) | 获取图片UI_ANIM_PLAY_MODE键值对 |
| [get_physics_entity_key_ui_anim_play_mode_kv](#get_physics_entity_key_ui_anim_play_mode_kv) | 获取逻辑物理组件类型UI_ANIM_PLAY_MODE键值对 |
| [get_kv_pair_value_ui_anim_play_mode](#get_kv_pair_value_ui_anim_play_mode) | 获取UI_ANIM_PLAY_MODE键值对 |
| [get_unit_key_ui_text_font_name_kv](#get_unit_key_ui_text_font_name_kv) | 获取单位编号UI_TEXT_FONT_NAME键值对 |
| [get_item_key_ui_text_font_name_kv](#get_item_key_ui_text_font_name_kv) | 获取物品编号UI_TEXT_FONT_NAME键值对 |
| [get_ability_key_ui_text_font_name_kv](#get_ability_key_ui_text_font_name_kv) | 获取技能编号UI_TEXT_FONT_NAME键值对 |
| [get_modifier_key_ui_text_font_name_kv](#get_modifier_key_ui_text_font_name_kv) | 获取魔法效果特效编号UI_TEXT_FONT_NAME键值对 |
| [get_projectile_key_ui_text_font_name_kv](#get_projectile_key_ui_text_font_name_kv) | 获取特效编号UI_TEXT_FONT_NAME键值对 |
| [get_destructible_key_ui_text_font_name_kv](#get_destructible_key_ui_text_font_name_kv) | 获取可破坏物编号UI_TEXT_FONT_NAME键值对 |
| [get_tech_key_ui_text_font_name_kv](#get_tech_key_ui_text_font_name_kv) | 获取科技编号UI_TEXT_FONT_NAME键值对 |
| [get_icon_id_ui_text_font_name_kv](#get_icon_id_ui_text_font_name_kv) | 获取图片UI_TEXT_FONT_NAME键值对 |
| [get_physics_entity_key_ui_text_font_name_kv](#get_physics_entity_key_ui_text_font_name_kv) | 获取逻辑物理组件类型UI_TEXT_FONT_NAME键值对 |
| [get_kv_pair_value_ui_text_font_name](#get_kv_pair_value_ui_text_font_name) | 获取UI_TEXT_FONT_NAME键值对 |
| [get_unit_key_ui_eca_anim_type_kv](#get_unit_key_ui_eca_anim_type_kv) | 获取单位编号UI_ECA_ANIM_TYPE键值对 |
| [get_item_key_ui_eca_anim_type_kv](#get_item_key_ui_eca_anim_type_kv) | 获取物品编号UI_ECA_ANIM_TYPE键值对 |
| [get_ability_key_ui_eca_anim_type_kv](#get_ability_key_ui_eca_anim_type_kv) | 获取技能编号UI_ECA_ANIM_TYPE键值对 |
| [get_modifier_key_ui_eca_anim_type_kv](#get_modifier_key_ui_eca_anim_type_kv) | 获取魔法效果特效编号UI_ECA_ANIM_TYPE键值对 |
| [get_projectile_key_ui_eca_anim_type_kv](#get_projectile_key_ui_eca_anim_type_kv) | 获取特效编号UI_ECA_ANIM_TYPE键值对 |
| [get_destructible_key_ui_eca_anim_type_kv](#get_destructible_key_ui_eca_anim_type_kv) | 获取可破坏物编号UI_ECA_ANIM_TYPE键值对 |
| [get_tech_key_ui_eca_anim_type_kv](#get_tech_key_ui_eca_anim_type_kv) | 获取科技编号UI_ECA_ANIM_TYPE键值对 |
| [get_icon_id_ui_eca_anim_type_kv](#get_icon_id_ui_eca_anim_type_kv) | 获取图片UI_ECA_ANIM_TYPE键值对 |
| [get_physics_entity_key_ui_eca_anim_type_kv](#get_physics_entity_key_ui_eca_anim_type_kv) | 获取逻辑物理组件类型UI_ECA_ANIM_TYPE键值对 |
| [get_kv_pair_value_ui_eca_anim_type](#get_kv_pair_value_ui_eca_anim_type) | 获取UI_ECA_ANIM_TYPE键值对 |
| [get_unit_key_local_unit_group_kv](#get_unit_key_local_unit_group_kv) | 获取单位编号LOCAL_UNIT_GROUP键值对 |
| [get_item_key_local_unit_group_kv](#get_item_key_local_unit_group_kv) | 获取物品编号LOCAL_UNIT_GROUP键值对 |
| [get_ability_key_local_unit_group_kv](#get_ability_key_local_unit_group_kv) | 获取技能编号LOCAL_UNIT_GROUP键值对 |
| [get_modifier_key_local_unit_group_kv](#get_modifier_key_local_unit_group_kv) | 获取魔法效果特效编号LOCAL_UNIT_GROUP键值对 |
| [get_projectile_key_local_unit_group_kv](#get_projectile_key_local_unit_group_kv) | 获取特效编号LOCAL_UNIT_GROUP键值对 |
| [get_destructible_key_local_unit_group_kv](#get_destructible_key_local_unit_group_kv) | 获取可破坏物编号LOCAL_UNIT_GROUP键值对 |
| [get_tech_key_local_unit_group_kv](#get_tech_key_local_unit_group_kv) | 获取科技编号LOCAL_UNIT_GROUP键值对 |
| [get_icon_id_local_unit_group_kv](#get_icon_id_local_unit_group_kv) | 获取图片LOCAL_UNIT_GROUP键值对 |
| [get_physics_entity_key_local_unit_group_kv](#get_physics_entity_key_local_unit_group_kv) | 获取逻辑物理组件类型LOCAL_UNIT_GROUP键值对 |
| [get_kv_pair_value_local_unit_group](#get_kv_pair_value_local_unit_group) | 获取LOCAL_UNIT_GROUP键值对 |
| [get_unit_key_damage_attack_type_kv](#get_unit_key_damage_attack_type_kv) | 获取单位编号DAMAGE_ATTACK_TYPE键值对 |
| [get_item_key_damage_attack_type_kv](#get_item_key_damage_attack_type_kv) | 获取物品编号DAMAGE_ATTACK_TYPE键值对 |
| [get_ability_key_damage_attack_type_kv](#get_ability_key_damage_attack_type_kv) | 获取技能编号DAMAGE_ATTACK_TYPE键值对 |
| [get_modifier_key_damage_attack_type_kv](#get_modifier_key_damage_attack_type_kv) | 获取魔法效果特效编号DAMAGE_ATTACK_TYPE键值对 |
| [get_projectile_key_damage_attack_type_kv](#get_projectile_key_damage_attack_type_kv) | 获取特效编号DAMAGE_ATTACK_TYPE键值对 |
| [get_destructible_key_damage_attack_type_kv](#get_destructible_key_damage_attack_type_kv) | 获取可破坏物编号DAMAGE_ATTACK_TYPE键值对 |
| [get_tech_key_damage_attack_type_kv](#get_tech_key_damage_attack_type_kv) | 获取科技编号DAMAGE_ATTACK_TYPE键值对 |
| [get_icon_id_damage_attack_type_kv](#get_icon_id_damage_attack_type_kv) | 获取图片DAMAGE_ATTACK_TYPE键值对 |
| [get_physics_entity_key_damage_attack_type_kv](#get_physics_entity_key_damage_attack_type_kv) | 获取逻辑物理组件类型DAMAGE_ATTACK_TYPE键值对 |
| [get_kv_pair_value_damage_attack_type](#get_kv_pair_value_damage_attack_type) | 获取DAMAGE_ATTACK_TYPE键值对 |
| [get_unit_key_damage_armor_type_kv](#get_unit_key_damage_armor_type_kv) | 获取单位编号DAMAGE_ARMOR_TYPE键值对 |
| [get_item_key_damage_armor_type_kv](#get_item_key_damage_armor_type_kv) | 获取物品编号DAMAGE_ARMOR_TYPE键值对 |
| [get_ability_key_damage_armor_type_kv](#get_ability_key_damage_armor_type_kv) | 获取技能编号DAMAGE_ARMOR_TYPE键值对 |
| [get_modifier_key_damage_armor_type_kv](#get_modifier_key_damage_armor_type_kv) | 获取魔法效果特效编号DAMAGE_ARMOR_TYPE键值对 |
| [get_projectile_key_damage_armor_type_kv](#get_projectile_key_damage_armor_type_kv) | 获取特效编号DAMAGE_ARMOR_TYPE键值对 |
| [get_destructible_key_damage_armor_type_kv](#get_destructible_key_damage_armor_type_kv) | 获取可破坏物编号DAMAGE_ARMOR_TYPE键值对 |
| [get_tech_key_damage_armor_type_kv](#get_tech_key_damage_armor_type_kv) | 获取科技编号DAMAGE_ARMOR_TYPE键值对 |
| [get_icon_id_damage_armor_type_kv](#get_icon_id_damage_armor_type_kv) | 获取图片DAMAGE_ARMOR_TYPE键值对 |
| [get_physics_entity_key_damage_armor_type_kv](#get_physics_entity_key_damage_armor_type_kv) | 获取逻辑物理组件类型DAMAGE_ARMOR_TYPE键值对 |
| [get_kv_pair_value_damage_armor_type](#get_kv_pair_value_damage_armor_type) | 获取DAMAGE_ARMOR_TYPE键值对 |
| [get_unit_key_item_stack_type_kv](#get_unit_key_item_stack_type_kv) | 获取单位编号ITEM_STACK_TYPE键值对 |
| [get_item_key_item_stack_type_kv](#get_item_key_item_stack_type_kv) | 获取物品编号ITEM_STACK_TYPE键值对 |
| [get_ability_key_item_stack_type_kv](#get_ability_key_item_stack_type_kv) | 获取技能编号ITEM_STACK_TYPE键值对 |
| [get_modifier_key_item_stack_type_kv](#get_modifier_key_item_stack_type_kv) | 获取魔法效果特效编号ITEM_STACK_TYPE键值对 |
| [get_projectile_key_item_stack_type_kv](#get_projectile_key_item_stack_type_kv) | 获取特效编号ITEM_STACK_TYPE键值对 |
| [get_destructible_key_item_stack_type_kv](#get_destructible_key_item_stack_type_kv) | 获取可破坏物编号ITEM_STACK_TYPE键值对 |
| [get_tech_key_item_stack_type_kv](#get_tech_key_item_stack_type_kv) | 获取科技编号ITEM_STACK_TYPE键值对 |
| [get_icon_id_item_stack_type_kv](#get_icon_id_item_stack_type_kv) | 获取图片ITEM_STACK_TYPE键值对 |
| [get_physics_entity_key_item_stack_type_kv](#get_physics_entity_key_item_stack_type_kv) | 获取逻辑物理组件类型ITEM_STACK_TYPE键值对 |
| [get_kv_pair_value_item_stack_type](#get_kv_pair_value_item_stack_type) | 获取ITEM_STACK_TYPE键值对 |
| [get_unit_key_ability_release_id_kv](#get_unit_key_ability_release_id_kv) | 获取单位编号ABILITY_RELEASE_ID键值对 |
| [get_item_key_ability_release_id_kv](#get_item_key_ability_release_id_kv) | 获取物品编号ABILITY_RELEASE_ID键值对 |
| [get_ability_key_ability_release_id_kv](#get_ability_key_ability_release_id_kv) | 获取技能编号ABILITY_RELEASE_ID键值对 |
| [get_modifier_key_ability_release_id_kv](#get_modifier_key_ability_release_id_kv) | 获取魔法效果特效编号ABILITY_RELEASE_ID键值对 |
| [get_projectile_key_ability_release_id_kv](#get_projectile_key_ability_release_id_kv) | 获取特效编号ABILITY_RELEASE_ID键值对 |
| [get_destructible_key_ability_release_id_kv](#get_destructible_key_ability_release_id_kv) | 获取可破坏物编号ABILITY_RELEASE_ID键值对 |
| [get_tech_key_ability_release_id_kv](#get_tech_key_ability_release_id_kv) | 获取科技编号ABILITY_RELEASE_ID键值对 |
| [get_icon_id_ability_release_id_kv](#get_icon_id_ability_release_id_kv) | 获取图片ABILITY_RELEASE_ID键值对 |
| [get_physics_entity_key_ability_release_id_kv](#get_physics_entity_key_ability_release_id_kv) | 获取逻辑物理组件类型ABILITY_RELEASE_ID键值对 |
| [get_kv_pair_value_ability_release_id](#get_kv_pair_value_ability_release_id) | 获取ABILITY_RELEASE_ID键值对 |
| [get_unit_key_slot_type_kv](#get_unit_key_slot_type_kv) | 获取单位编号SLOT_TYPE键值对 |
| [get_item_key_slot_type_kv](#get_item_key_slot_type_kv) | 获取物品编号SLOT_TYPE键值对 |
| [get_ability_key_slot_type_kv](#get_ability_key_slot_type_kv) | 获取技能编号SLOT_TYPE键值对 |
| [get_modifier_key_slot_type_kv](#get_modifier_key_slot_type_kv) | 获取魔法效果特效编号SLOT_TYPE键值对 |
| [get_projectile_key_slot_type_kv](#get_projectile_key_slot_type_kv) | 获取特效编号SLOT_TYPE键值对 |
| [get_destructible_key_slot_type_kv](#get_destructible_key_slot_type_kv) | 获取可破坏物编号SLOT_TYPE键值对 |
| [get_tech_key_slot_type_kv](#get_tech_key_slot_type_kv) | 获取科技编号SLOT_TYPE键值对 |
| [get_icon_id_slot_type_kv](#get_icon_id_slot_type_kv) | 获取图片SLOT_TYPE键值对 |
| [get_physics_entity_key_slot_type_kv](#get_physics_entity_key_slot_type_kv) | 获取逻辑物理组件类型SLOT_TYPE键值对 |
| [get_kv_pair_value_slot_type](#get_kv_pair_value_slot_type) | 获取SLOT_TYPE键值对 |
| [get_unit_key_ui_point_kv](#get_unit_key_ui_point_kv) | 获取单位编号UI_POINT键值对 |
| [get_item_key_ui_point_kv](#get_item_key_ui_point_kv) | 获取物品编号UI_POINT键值对 |
| [get_ability_key_ui_point_kv](#get_ability_key_ui_point_kv) | 获取技能编号UI_POINT键值对 |
| [get_modifier_key_ui_point_kv](#get_modifier_key_ui_point_kv) | 获取魔法效果特效编号UI_POINT键值对 |
| [get_projectile_key_ui_point_kv](#get_projectile_key_ui_point_kv) | 获取特效编号UI_POINT键值对 |
| [get_destructible_key_ui_point_kv](#get_destructible_key_ui_point_kv) | 获取可破坏物编号UI_POINT键值对 |
| [get_tech_key_ui_point_kv](#get_tech_key_ui_point_kv) | 获取科技编号UI_POINT键值对 |
| [get_icon_id_ui_point_kv](#get_icon_id_ui_point_kv) | 获取图片UI_POINT键值对 |
| [get_physics_entity_key_ui_point_kv](#get_physics_entity_key_ui_point_kv) | 获取逻辑物理组件类型UI_POINT键值对 |
| [get_kv_pair_value_ui_point](#get_kv_pair_value_ui_point) | 获取UI_POINT键值对 |
| [get_unit_key_attach_model_entity_kv](#get_unit_key_attach_model_entity_kv) | 获取单位编号ATTACH_MODEL_ENTITY键值对 |
| [get_item_key_attach_model_entity_kv](#get_item_key_attach_model_entity_kv) | 获取物品编号ATTACH_MODEL_ENTITY键值对 |
| [get_ability_key_attach_model_entity_kv](#get_ability_key_attach_model_entity_kv) | 获取技能编号ATTACH_MODEL_ENTITY键值对 |
| [get_modifier_key_attach_model_entity_kv](#get_modifier_key_attach_model_entity_kv) | 获取魔法效果特效编号ATTACH_MODEL_ENTITY键值对 |
| [get_projectile_key_attach_model_entity_kv](#get_projectile_key_attach_model_entity_kv) | 获取特效编号ATTACH_MODEL_ENTITY键值对 |
| [get_destructible_key_attach_model_entity_kv](#get_destructible_key_attach_model_entity_kv) | 获取可破坏物编号ATTACH_MODEL_ENTITY键值对 |
| [get_tech_key_attach_model_entity_kv](#get_tech_key_attach_model_entity_kv) | 获取科技编号ATTACH_MODEL_ENTITY键值对 |
| [get_icon_id_attach_model_entity_kv](#get_icon_id_attach_model_entity_kv) | 获取图片ATTACH_MODEL_ENTITY键值对 |
| [get_physics_entity_key_attach_model_entity_kv](#get_physics_entity_key_attach_model_entity_kv) | 获取逻辑物理组件类型ATTACH_MODEL_ENTITY键值对 |
| [get_kv_pair_value_attach_model_entity](#get_kv_pair_value_attach_model_entity) | 获取ATTACH_MODEL_ENTITY键值对 |
| [get_unit_key_live2d_kv](#get_unit_key_live2d_kv) | 获取单位编号LIVE2D键值对 |
| [get_item_key_live2d_kv](#get_item_key_live2d_kv) | 获取物品编号LIVE2D键值对 |
| [get_ability_key_live2d_kv](#get_ability_key_live2d_kv) | 获取技能编号LIVE2D键值对 |
| [get_modifier_key_live2d_kv](#get_modifier_key_live2d_kv) | 获取魔法效果特效编号LIVE2D键值对 |
| [get_projectile_key_live2d_kv](#get_projectile_key_live2d_kv) | 获取特效编号LIVE2D键值对 |
| [get_destructible_key_live2d_kv](#get_destructible_key_live2d_kv) | 获取可破坏物编号LIVE2D键值对 |
| [get_tech_key_live2d_kv](#get_tech_key_live2d_kv) | 获取科技编号LIVE2D键值对 |
| [get_icon_id_live2d_kv](#get_icon_id_live2d_kv) | 获取图片LIVE2D键值对 |
| [get_physics_entity_key_live2d_kv](#get_physics_entity_key_live2d_kv) | 获取逻辑物理组件类型LIVE2D键值对 |
| [get_kv_pair_value_live2d](#get_kv_pair_value_live2d) | 获取LIVE2D键值对 |
| [get_unit_key_spine_kv](#get_unit_key_spine_kv) | 获取单位编号SPINE键值对 |
| [get_item_key_spine_kv](#get_item_key_spine_kv) | 获取物品编号SPINE键值对 |
| [get_ability_key_spine_kv](#get_ability_key_spine_kv) | 获取技能编号SPINE键值对 |
| [get_modifier_key_spine_kv](#get_modifier_key_spine_kv) | 获取魔法效果特效编号SPINE键值对 |
| [get_projectile_key_spine_kv](#get_projectile_key_spine_kv) | 获取特效编号SPINE键值对 |
| [get_destructible_key_spine_kv](#get_destructible_key_spine_kv) | 获取可破坏物编号SPINE键值对 |
| [get_tech_key_spine_kv](#get_tech_key_spine_kv) | 获取科技编号SPINE键值对 |
| [get_icon_id_spine_kv](#get_icon_id_spine_kv) | 获取图片SPINE键值对 |
| [get_physics_entity_key_spine_kv](#get_physics_entity_key_spine_kv) | 获取逻辑物理组件类型SPINE键值对 |
| [get_kv_pair_value_spine](#get_kv_pair_value_spine) | 获取SPINE键值对 |
| [get_unit_key_force_entity_kv](#get_unit_key_force_entity_kv) | 获取单位编号FORCE_ENTITY键值对 |
| [get_item_key_force_entity_kv](#get_item_key_force_entity_kv) | 获取物品编号FORCE_ENTITY键值对 |
| [get_ability_key_force_entity_kv](#get_ability_key_force_entity_kv) | 获取技能编号FORCE_ENTITY键值对 |
| [get_modifier_key_force_entity_kv](#get_modifier_key_force_entity_kv) | 获取魔法效果特效编号FORCE_ENTITY键值对 |
| [get_projectile_key_force_entity_kv](#get_projectile_key_force_entity_kv) | 获取特效编号FORCE_ENTITY键值对 |
| [get_destructible_key_force_entity_kv](#get_destructible_key_force_entity_kv) | 获取可破坏物编号FORCE_ENTITY键值对 |
| [get_tech_key_force_entity_kv](#get_tech_key_force_entity_kv) | 获取科技编号FORCE_ENTITY键值对 |
| [get_icon_id_force_entity_kv](#get_icon_id_force_entity_kv) | 获取图片FORCE_ENTITY键值对 |
| [get_physics_entity_key_force_entity_kv](#get_physics_entity_key_force_entity_kv) | 获取逻辑物理组件类型FORCE_ENTITY键值对 |
| [get_kv_pair_value_force_entity](#get_kv_pair_value_force_entity) | 获取FORCE_ENTITY键值对 |
| [get_unit_key_goods_key_kv](#get_unit_key_goods_key_kv) | 获取单位编号GOODS_KEY键值对 |
| [get_item_key_goods_key_kv](#get_item_key_goods_key_kv) | 获取物品编号GOODS_KEY键值对 |
| [get_ability_key_goods_key_kv](#get_ability_key_goods_key_kv) | 获取技能编号GOODS_KEY键值对 |
| [get_modifier_key_goods_key_kv](#get_modifier_key_goods_key_kv) | 获取魔法效果特效编号GOODS_KEY键值对 |
| [get_projectile_key_goods_key_kv](#get_projectile_key_goods_key_kv) | 获取特效编号GOODS_KEY键值对 |
| [get_destructible_key_goods_key_kv](#get_destructible_key_goods_key_kv) | 获取可破坏物编号GOODS_KEY键值对 |
| [get_tech_key_goods_key_kv](#get_tech_key_goods_key_kv) | 获取科技编号GOODS_KEY键值对 |
| [get_icon_id_goods_key_kv](#get_icon_id_goods_key_kv) | 获取图片GOODS_KEY键值对 |
| [get_physics_entity_key_goods_key_kv](#get_physics_entity_key_goods_key_kv) | 获取逻辑物理组件类型GOODS_KEY键值对 |
| [get_kv_pair_value_goods_key](#get_kv_pair_value_goods_key) | 获取GOODS_KEY键值对 |
| [get_unit_key_mouse_key_without_middle_kv](#get_unit_key_mouse_key_without_middle_kv) | 获取单位编号MOUSE_KEY_WITHOUT_MIDDLE键值对 |
| [get_item_key_mouse_key_without_middle_kv](#get_item_key_mouse_key_without_middle_kv) | 获取物品编号MOUSE_KEY_WITHOUT_MIDDLE键值对 |
| [get_ability_key_mouse_key_without_middle_kv](#get_ability_key_mouse_key_without_middle_kv) | 获取技能编号MOUSE_KEY_WITHOUT_MIDDLE键值对 |
| [get_modifier_key_mouse_key_without_middle_kv](#get_modifier_key_mouse_key_without_middle_kv) | 获取魔法效果特效编号MOUSE_KEY_WITHOUT_MIDDLE键值对 |
| [get_projectile_key_mouse_key_without_middle_kv](#get_projectile_key_mouse_key_without_middle_kv) | 获取特效编号MOUSE_KEY_WITHOUT_MIDDLE键值对 |
| [get_destructible_key_mouse_key_without_middle_kv](#get_destructible_key_mouse_key_without_middle_kv) | 获取可破坏物编号MOUSE_KEY_WITHOUT_MIDDLE键值对 |
| [get_tech_key_mouse_key_without_middle_kv](#get_tech_key_mouse_key_without_middle_kv) | 获取科技编号MOUSE_KEY_WITHOUT_MIDDLE键值对 |
| [get_icon_id_mouse_key_without_middle_kv](#get_icon_id_mouse_key_without_middle_kv) | 获取图片MOUSE_KEY_WITHOUT_MIDDLE键值对 |
| [get_physics_entity_key_mouse_key_without_middle_kv](#get_physics_entity_key_mouse_key_without_middle_kv) | 获取逻辑物理组件类型MOUSE_KEY_WITHOUT_MIDDLE键值对 |
| [get_kv_pair_value_mouse_key_without_middle](#get_kv_pair_value_mouse_key_without_middle) | 获取MOUSE_KEY_WITHOUT_MIDDLE键值对 |
| [get_unit_key_map_kv](#get_unit_key_map_kv) | 获取单位编号MAP键值对 |
| [get_item_key_map_kv](#get_item_key_map_kv) | 获取物品编号MAP键值对 |
| [get_ability_key_map_kv](#get_ability_key_map_kv) | 获取技能编号MAP键值对 |
| [get_modifier_key_map_kv](#get_modifier_key_map_kv) | 获取魔法效果特效编号MAP键值对 |
| [get_projectile_key_map_kv](#get_projectile_key_map_kv) | 获取特效编号MAP键值对 |
| [get_destructible_key_map_kv](#get_destructible_key_map_kv) | 获取可破坏物编号MAP键值对 |
| [get_tech_key_map_kv](#get_tech_key_map_kv) | 获取科技编号MAP键值对 |
| [get_icon_id_map_kv](#get_icon_id_map_kv) | 获取图片MAP键值对 |
| [get_physics_entity_key_map_kv](#get_physics_entity_key_map_kv) | 获取逻辑物理组件类型MAP键值对 |
| [get_kv_pair_value_map](#get_kv_pair_value_map) | 获取MAP键值对 |
| [get_unit_key_unit_group_command_type_kv](#get_unit_key_unit_group_command_type_kv) | 获取单位编号UNIT_GROUP_COMMAND_TYPE键值对 |

---

## set_trigger_list_actor_variable_joint

method in GameAPI

- 描述

    设置全局触发器JOINT数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Joint | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local joint = GameAPI.get_unit_key_joint_kv(1, "key")

GameAPI.set_trigger_list_actor_variable_joint(actor, "key", 1)
```

---

## set_trigger_variable_joint

method in GameAPI

- 描述

    设置全局触发器JOINT非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.Joint | 值 |

- 返回值

    无

- 示例

```lua
local joint = GameAPI.get_unit_key_joint_kv(1, "key")

GameAPI.set_trigger_variable_joint("key")
```

---

## set_trigger_actor_variable_joint

method in GameAPI

- 描述

    设置全局触发器JOINT非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.Joint | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local joint = GameAPI.get_unit_key_joint_kv(1, "key")

GameAPI.set_trigger_actor_variable_joint(actor, "key")
```

---

## set_trigger_list_variable_reaction

method in GameAPI

- 描述

    设置全局触发器REACTION数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Reaction | 值 |

- 返回值

    无

- 示例

```lua
local physics_entity = GameAPI.get_unit_key_physics_entity_kv(1, "key")
local reaction = GameAPI.api_add_uniform_gravitation_field_to_rigid_body(physics_entity, Fix32(10), Fix32Vec3(0, 0, 0))

GameAPI.set_trigger_list_variable_reaction("key", 1)
```

---

## set_trigger_list_actor_variable_reaction

method in GameAPI

- 描述

    设置全局触发器REACTION数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Reaction | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local physics_entity = GameAPI.get_unit_key_physics_entity_kv(1, "key")
local reaction = GameAPI.api_add_uniform_gravitation_field_to_rigid_body(physics_entity, Fix32(10), Fix32Vec3(0, 0, 0))

GameAPI.set_trigger_list_actor_variable_reaction(actor, "key", 1)
```

---

## set_trigger_variable_reaction

method in GameAPI

- 描述

    设置全局触发器REACTION非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.Reaction | 值 |

- 返回值

    无

- 示例

```lua
local physics_entity = GameAPI.get_unit_key_physics_entity_kv(1, "key")
local reaction = GameAPI.api_add_uniform_gravitation_field_to_rigid_body(physics_entity, Fix32(10), Fix32Vec3(0, 0, 0))

GameAPI.set_trigger_variable_reaction("key")
```

---

## set_trigger_actor_variable_reaction

method in GameAPI

- 描述

    设置全局触发器REACTION非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.Reaction | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local physics_entity = GameAPI.get_unit_key_physics_entity_kv(1, "key")
local reaction = GameAPI.api_add_uniform_gravitation_field_to_rigid_body(physics_entity, Fix32(10), Fix32Vec3(0, 0, 0))

GameAPI.set_trigger_actor_variable_reaction(actor, "key")
```

---

## set_trigger_list_variable_reaction_group

method in GameAPI

- 描述

    设置全局触发器REACTION_GROUP数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.ReactionGroup | 值 |

- 返回值

    无

- 示例

```lua
local reaction_group = GameAPI.get_trigger_variable_reaction_group("key")

GameAPI.set_trigger_list_variable_reaction_group("key", 1)
```

---

## set_trigger_list_actor_variable_reaction_group

method in GameAPI

- 描述

    设置全局触发器REACTION_GROUP数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.ReactionGroup | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local reaction_group = GameAPI.get_trigger_variable_reaction_group("key")

GameAPI.set_trigger_list_actor_variable_reaction_group(actor, "key", 1)
```

---

## set_trigger_variable_reaction_group

method in GameAPI

- 描述

    设置全局触发器REACTION_GROUP非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.ReactionGroup | 值 |

- 返回值

    无

- 示例

```lua
local reaction_group = GameAPI.get_trigger_variable_reaction_group("key")

GameAPI.set_trigger_variable_reaction_group("key")
```

---

## set_trigger_actor_variable_reaction_group

method in GameAPI

- 描述

    设置全局触发器REACTION_GROUP非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.ReactionGroup | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local reaction_group = GameAPI.get_trigger_variable_reaction_group("key")

GameAPI.set_trigger_actor_variable_reaction_group(actor, "key")
```

---

## set_trigger_list_variable_physics_filter

method in GameAPI

- 描述

    设置全局触发器PHYSICS_FILTER数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.PhysicsFilter | 值 |

- 返回值

    无

- 示例

```lua
local physics_filter = GameAPI.api_create_physics_filter(1, 1, false, false, false, false, false)

GameAPI.set_trigger_list_variable_physics_filter("key", 1)
```

---

## set_trigger_list_actor_variable_physics_filter

method in GameAPI

- 描述

    设置全局触发器PHYSICS_FILTER数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.PhysicsFilter | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local physics_filter = GameAPI.api_create_physics_filter(1, 1, false, false, false, false, false)

GameAPI.set_trigger_list_actor_variable_physics_filter(actor, "key", 1)
```

---

## set_trigger_variable_physics_filter

method in GameAPI

- 描述

    设置全局触发器PHYSICS_FILTER非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.PhysicsFilter | 值 |

- 返回值

    无

- 示例

```lua
local physics_filter = GameAPI.api_create_physics_filter(1, 1, false, false, false, false, false)

GameAPI.set_trigger_variable_physics_filter("key")
```

---

## set_trigger_actor_variable_physics_filter

method in GameAPI

- 描述

    设置全局触发器PHYSICS_FILTER非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.PhysicsFilter | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local physics_filter = GameAPI.api_create_physics_filter(1, 1, false, false, false, false, false)

GameAPI.set_trigger_actor_variable_physics_filter(actor, "key")
```

---

## set_trigger_list_variable_int_save

method in GameAPI

- 描述

    设置全局触发器INT_SAVE数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | integer | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_list_variable_int_save("key", 1, 1)
```

---

## set_trigger_list_actor_variable_int_save

method in GameAPI

- 描述

    设置全局触发器INT_SAVE数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | integer | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_list_actor_variable_int_save(actor, "key", 1, 1)
```

---

## set_trigger_variable_int_save

method in GameAPI

- 描述

    设置全局触发器INT_SAVE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | integer | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_int_save("key", 1)
```

---

## set_trigger_actor_variable_int_save

method in GameAPI

- 描述

    设置全局触发器INT_SAVE非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | integer | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_actor_variable_int_save(actor, "key", 1)
```

---

## set_trigger_list_variable_str_save

method in GameAPI

- 描述

    设置全局触发器STR_SAVE数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | string | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_list_variable_str_save("key", 1, "value")
```

---

## set_trigger_list_actor_variable_str_save

method in GameAPI

- 描述

    设置全局触发器STR_SAVE数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | string | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_list_actor_variable_str_save(actor, "key", 1, "value")
```

---

## set_trigger_variable_str_save

method in GameAPI

- 描述

    设置全局触发器STR_SAVE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | string | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_str_save("key", "value")
```

---

## set_trigger_actor_variable_str_save

method in GameAPI

- 描述

    设置全局触发器STR_SAVE非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | string | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_actor_variable_str_save(actor, "key", "value")
```

---

## set_trigger_list_variable_float_save

method in GameAPI

- 描述

    设置全局触发器FLOAT_SAVE数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Fixed | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_list_variable_float_save("key", 1, Fix32(1))
```

---

## set_trigger_list_actor_variable_float_save

method in GameAPI

- 描述

    设置全局触发器FLOAT_SAVE数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Fixed | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_list_actor_variable_float_save(actor, "key", 1, Fix32(1))
```

---

## set_trigger_variable_float_save

method in GameAPI

- 描述

    设置全局触发器FLOAT_SAVE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.Fixed | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_float_save("key", Fix32(1))
```

---

## set_trigger_actor_variable_float_save

method in GameAPI

- 描述

    设置全局触发器FLOAT_SAVE非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.Fixed | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_actor_variable_float_save(actor, "key", Fix32(1))
```

---

## set_trigger_list_variable_bool_save

method in GameAPI

- 描述

    设置全局触发器BOOL_SAVE数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | boolean | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_list_variable_bool_save("key", 1, true)
```

---

## set_trigger_list_actor_variable_bool_save

method in GameAPI

- 描述

    设置全局触发器BOOL_SAVE数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | boolean | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_list_actor_variable_bool_save(actor, "key", 1, true)
```

---

## set_trigger_variable_bool_save

method in GameAPI

- 描述

    设置全局触发器BOOL_SAVE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | boolean | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_bool_save("key", true)
```

---

## set_trigger_actor_variable_bool_save

method in GameAPI

- 描述

    设置全局触发器BOOL_SAVE非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | boolean | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_actor_variable_bool_save(actor, "key", true)
```

---

## set_trigger_list_variable_table_save

method in GameAPI

- 描述

    设置全局触发器TABLE_SAVE数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Table | 值 |

- 返回值

    无

- 示例

```lua
local tbl = {}

GameAPI.set_trigger_list_variable_table_save("key", 1)
```

---

## set_trigger_list_actor_variable_table_save

method in GameAPI

- 描述

    设置全局触发器TABLE_SAVE数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Table | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local tbl = {}

GameAPI.set_trigger_list_actor_variable_table_save(actor, "key", 1)
```

---

## set_trigger_variable_table_save

method in GameAPI

- 描述

    设置全局触发器TABLE_SAVE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.Table | 值 |

- 返回值

    无

- 示例

```lua
local tbl = {}

GameAPI.set_trigger_variable_table_save("key")
```

---

## set_trigger_actor_variable_table_save

method in GameAPI

- 描述

    设置全局触发器TABLE_SAVE非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.Table | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local tbl = {}

GameAPI.set_trigger_actor_variable_table_save(actor, "key")
```

---

## set_trigger_list_variable_global_archive_slot

method in GameAPI

- 描述

    设置全局触发器GLOBAL_ARCHIVE_SLOT数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | string | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_list_variable_global_archive_slot("key", 1, "value")
```

---

## set_trigger_list_actor_variable_global_archive_slot

method in GameAPI

- 描述

    设置全局触发器GLOBAL_ARCHIVE_SLOT数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | string | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_list_actor_variable_global_archive_slot(actor, "key", 1, "value")
```

---

## set_trigger_variable_global_archive_slot

method in GameAPI

- 描述

    设置全局触发器GLOBAL_ARCHIVE_SLOT非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | string | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_global_archive_slot("key", "value")
```

---

## set_trigger_actor_variable_global_archive_slot

method in GameAPI

- 描述

    设置全局触发器GLOBAL_ARCHIVE_SLOT非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | string | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_actor_variable_global_archive_slot(actor, "key", "value")
```

---

## set_trigger_list_variable_random_pool_drop

method in GameAPI

- 描述

    设置全局触发器RANDOM_POOL_DROP数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | integer | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_list_variable_random_pool_drop("key", 1, 1)
```

---

## set_trigger_list_actor_variable_random_pool_drop

method in GameAPI

- 描述

    设置全局触发器RANDOM_POOL_DROP数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | integer | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_list_actor_variable_random_pool_drop(actor, "key", 1, 1)
```

---

## set_trigger_variable_random_pool_drop

method in GameAPI

- 描述

    设置全局触发器RANDOM_POOL_DROP非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | integer | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_random_pool_drop("key", 1)
```

---

## set_trigger_actor_variable_random_pool_drop

method in GameAPI

- 描述

    设置全局触发器RANDOM_POOL_DROP非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | integer | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_actor_variable_random_pool_drop(actor, "key", 1)
```

---

## set_trigger_list_variable_dynamic_trigger_instance

method in GameAPI

- 描述

    设置全局触发器DYNAMIC_TRIGGER_INSTANCE数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.DynamicTriggerInstance | 值 |

- 返回值

    无

- 示例

```lua
local trigger_instance = GameAPI.get_last_created_trigger()

GameAPI.set_trigger_list_variable_dynamic_trigger_instance("key", 1)
```

---

## set_trigger_list_actor_variable_dynamic_trigger_instance

method in GameAPI

- 描述

    设置全局触发器DYNAMIC_TRIGGER_INSTANCE数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.DynamicTriggerInstance | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local trigger_instance = GameAPI.get_last_created_trigger()

GameAPI.set_trigger_list_actor_variable_dynamic_trigger_instance(actor, "key", 1)
```

---

## set_trigger_variable_dynamic_trigger_instance

method in GameAPI

- 描述

    设置全局触发器DYNAMIC_TRIGGER_INSTANCE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.DynamicTriggerInstance | 值 |

- 返回值

    无

- 示例

```lua
local trigger_instance = GameAPI.get_last_created_trigger()

GameAPI.set_trigger_variable_dynamic_trigger_instance("key")
```

---

## set_trigger_actor_variable_dynamic_trigger_instance

method in GameAPI

- 描述

    设置全局触发器DYNAMIC_TRIGGER_INSTANCE非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.DynamicTriggerInstance | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local trigger_instance = GameAPI.get_last_created_trigger()

GameAPI.set_trigger_actor_variable_dynamic_trigger_instance(actor, "key")
```

---

## set_trigger_list_variable_table

method in GameAPI

- 描述

    设置全局触发器TABLE数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Table | 值 |

- 返回值

    无

- 示例

```lua
local tbl = {}

GameAPI.set_trigger_list_variable_table("key", 1)
```

---

## set_trigger_list_actor_variable_table

method in GameAPI

- 描述

    设置全局触发器TABLE数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Table | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local tbl = {}

GameAPI.set_trigger_list_actor_variable_table(actor, "key", 1)
```

---

## set_trigger_variable_table

method in GameAPI

- 描述

    设置全局触发器TABLE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.Table | 值 |

- 返回值

    无

- 示例

```lua
local tbl = {}

GameAPI.set_trigger_variable_table("key")
```

---

## set_trigger_actor_variable_table

method in GameAPI

- 描述

    设置全局触发器TABLE非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.Table | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local tbl = {}

GameAPI.set_trigger_actor_variable_table(actor, "key")
```

---

## set_trigger_list_variable_random_pool

method in GameAPI

- 描述

    设置全局触发器RANDOM_POOL数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.RandomPool | 值 |

- 返回值

    无

- 示例

```lua
local random_pool = GameAPI.create_random_pool()

GameAPI.set_trigger_list_variable_random_pool("key", 1)
```

---

## set_trigger_list_actor_variable_random_pool

method in GameAPI

- 描述

    设置全局触发器RANDOM_POOL数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.RandomPool | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local random_pool = GameAPI.create_random_pool()

GameAPI.set_trigger_list_actor_variable_random_pool(actor, "key", 1)
```

---

## set_trigger_variable_random_pool

method in GameAPI

- 描述

    设置全局触发器RANDOM_POOL非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.RandomPool | 值 |

- 返回值

    无

- 示例

```lua
local random_pool = GameAPI.create_random_pool()

GameAPI.set_trigger_variable_random_pool("key")
```

---

## set_trigger_actor_variable_random_pool

method in GameAPI

- 描述

    设置全局触发器RANDOM_POOL非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.RandomPool | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local random_pool = GameAPI.create_random_pool()

GameAPI.set_trigger_actor_variable_random_pool(actor, "key")
```

---

## set_trigger_list_variable_scene_ui

method in GameAPI

- 描述

    设置全局触发器SCENE_UI数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.SceneNode | 值 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local unit = player:get_all_units()[1]
local scene_node = GameAPI.create_scene_node_on_unit_ex("comp_name", player.handle, unit.handle, "origin", false)

GameAPI.set_trigger_list_variable_scene_ui("key", 1)
```

---

## set_trigger_list_actor_variable_scene_ui

method in GameAPI

- 描述

    设置全局触发器SCENE_UI数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.SceneNode | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local player = y3.player.get_by_id(1)
local scene_node = GameAPI.create_scene_node_on_unit_ex("comp_name", player.handle, unit.handle, "origin", false)

GameAPI.set_trigger_list_actor_variable_scene_ui(actor, "key", 1)
```

---

## set_trigger_variable_scene_ui

method in GameAPI

- 描述

    设置全局触发器SCENE_UI非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.SceneNode | 值 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local unit = player:get_all_units()[1]
local scene_node = GameAPI.create_scene_node_on_unit_ex("comp_name", player.handle, unit.handle, "origin", false)

GameAPI.set_trigger_variable_scene_ui("key")
```

---

## set_trigger_actor_variable_scene_ui

method in GameAPI

- 描述

    设置全局触发器SCENE_UI非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.SceneNode | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local player = y3.player.get_by_id(1)
local scene_node = GameAPI.create_scene_node_on_unit_ex("comp_name", player.handle, unit.handle, "origin", false)

GameAPI.set_trigger_actor_variable_scene_ui(actor, "key")
```

---

## set_trigger_list_variable_damage_type

method in GameAPI

- 描述

    设置全局触发器DAMAGE_TYPE数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | integer | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_list_variable_damage_type("key", 1, 1)
```

---

## set_trigger_list_actor_variable_damage_type

method in GameAPI

- 描述

    设置全局触发器DAMAGE_TYPE数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | integer | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_list_actor_variable_damage_type(actor, "key", 1, 1)
```

---

## set_trigger_variable_damage_type

method in GameAPI

- 描述

    设置全局触发器DAMAGE_TYPE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | integer | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_damage_type("key", 1)
```

---

## set_trigger_actor_variable_damage_type

method in GameAPI

- 描述

    设置全局触发器DAMAGE_TYPE非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | integer | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_actor_variable_damage_type(actor, "key", 1)
```

---

## set_trigger_list_variable_new_timer

method in GameAPI

- 描述

    设置全局触发器NEW_TIMER数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Timer | 值 |

- 返回值

    无

- 示例

```lua
local timer = y3.timer.loop(1, function() end)

GameAPI.set_trigger_list_variable_new_timer("key", 1)
```

---

## set_trigger_list_actor_variable_new_timer

method in GameAPI

- 描述

    设置全局触发器NEW_TIMER数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Timer | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local timer = y3.timer.loop(1, function() end)

GameAPI.set_trigger_list_actor_variable_new_timer(actor, "key", 1)
```

---

## set_trigger_variable_new_timer

method in GameAPI

- 描述

    设置全局触发器NEW_TIMER非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.Timer | 值 |

- 返回值

    无

- 示例

```lua
local timer = y3.timer.loop(1, function() end)

GameAPI.set_trigger_variable_new_timer("key")
```

---

## set_trigger_actor_variable_new_timer

method in GameAPI

- 描述

    设置全局触发器NEW_TIMER非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.Timer | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local timer = y3.timer.loop(1, function() end)

GameAPI.set_trigger_actor_variable_new_timer(actor, "key")
```

---

## set_trigger_list_variable_tech_key

method in GameAPI

- 描述

    设置全局触发器TECH_KEY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.TechKey | 值 |

- 返回值

    无

- 示例

```lua
local tech_key = 134274569

GameAPI.set_trigger_list_variable_tech_key("key", 1)
```

---

## set_trigger_list_actor_variable_tech_key

method in GameAPI

- 描述

    设置全局触发器TECH_KEY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.TechKey | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local tech_key = 134274569

GameAPI.set_trigger_list_actor_variable_tech_key(actor, "key", 1)
```

---

## set_trigger_variable_tech_key

method in GameAPI

- 描述

    设置全局触发器TECH_KEY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.TechKey | 值 |

- 返回值

    无

- 示例

```lua
local tech_key = 134274569

GameAPI.set_trigger_variable_tech_key("key")
```

---

## set_trigger_actor_variable_tech_key

method in GameAPI

- 描述

    设置全局触发器TECH_KEY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.TechKey | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local tech_key = 134274569

GameAPI.set_trigger_actor_variable_tech_key(actor, "key")
```

---

## set_trigger_list_variable_store_key

method in GameAPI

- 描述

    设置全局触发器STORE_KEY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.StoreKey | 值 |

- 返回值

    无

- 示例

```lua
local store_key = 134274569

GameAPI.set_trigger_list_variable_store_key("key", 1)
```

---

## set_trigger_list_actor_variable_store_key

method in GameAPI

- 描述

    设置全局触发器STORE_KEY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.StoreKey | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local store_key = 134274569

GameAPI.set_trigger_list_actor_variable_store_key(actor, "key", 1)
```

---

## set_trigger_variable_store_key

method in GameAPI

- 描述

    设置全局触发器STORE_KEY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.StoreKey | 值 |

- 返回值

    无

- 示例

```lua
local store_key = 134274569

GameAPI.set_trigger_variable_store_key("key")
```

---

## set_trigger_actor_variable_store_key

method in GameAPI

- 描述

    设置全局触发器STORE_KEY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.StoreKey | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local store_key = 134274569

GameAPI.set_trigger_actor_variable_store_key(actor, "key")
```

---

## set_trigger_list_variable_keyboard_key

method in GameAPI

- 描述

    设置全局触发器KEYBOARD_KEY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.KeyboardKey | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_list_variable_keyboard_key("key", 1, 1)
```

---

## set_trigger_list_actor_variable_keyboard_key

method in GameAPI

- 描述

    设置全局触发器KEYBOARD_KEY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.KeyboardKey | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_list_actor_variable_keyboard_key(actor, "key", 1, 1)
```

---

## set_trigger_variable_keyboard_key

method in GameAPI

- 描述

    设置全局触发器KEYBOARD_KEY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.KeyboardKey | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_keyboard_key("key", 1)
```

---

## set_trigger_actor_variable_keyboard_key

method in GameAPI

- 描述

    设置全局触发器KEYBOARD_KEY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.KeyboardKey | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_actor_variable_keyboard_key(actor, "key", 1)
```

---

## set_trigger_list_variable_unit_type

method in GameAPI

- 描述

    设置全局触发器UNIT_TYPE数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.UnitType | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_list_variable_unit_type("key", 1, 1)
```

---

## set_trigger_list_actor_variable_unit_type

method in GameAPI

- 描述

    设置全局触发器UNIT_TYPE数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.UnitType | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_list_actor_variable_unit_type(actor, "key", 1, 1)
```

---

## set_trigger_variable_unit_type

method in GameAPI

- 描述

    设置全局触发器UNIT_TYPE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.UnitType | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_unit_type("key", 1)
```

---

## set_trigger_actor_variable_unit_type

method in GameAPI

- 描述

    设置全局触发器UNIT_TYPE非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.UnitType | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_actor_variable_unit_type(actor, "key", 1)
```

---

## set_trigger_list_variable_curved_path

method in GameAPI

- 描述

    设置全局触发器CURVED_PATH数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.CurvedPath | 值 |

- 返回值

    无

- 示例

```lua
local path = {}

GameAPI.set_trigger_list_variable_curved_path("key", 1)
```

---

## set_trigger_list_actor_variable_curved_path

method in GameAPI

- 描述

    设置全局触发器CURVED_PATH数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.CurvedPath | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local path = {}

GameAPI.set_trigger_list_actor_variable_curved_path(actor, "key", 1)
```

---

## set_trigger_variable_curved_path

method in GameAPI

- 描述

    设置全局触发器CURVED_PATH非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.CurvedPath | 值 |

- 返回值

    无

- 示例

```lua
local path = {}

GameAPI.set_trigger_variable_curved_path("key")
```

---

## set_trigger_actor_variable_curved_path

method in GameAPI

- 描述

    设置全局触发器CURVED_PATH非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.CurvedPath | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local path = {}

GameAPI.set_trigger_actor_variable_curved_path(actor, "key")
```

---

## set_trigger_list_variable_curved_path_3d

method in GameAPI

- 描述

    设置全局触发器CURVED_PATH_3D数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.CurvedPath3D | 值 |

- 返回值

    无

- 示例

```lua
local curved_path_3d = {}

GameAPI.set_trigger_list_variable_curved_path_3d("key", 1)
```

---

## set_trigger_list_actor_variable_curved_path_3d

method in GameAPI

- 描述

    设置全局触发器CURVED_PATH_3D数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.CurvedPath3D | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local curved_path_3d = {}

GameAPI.set_trigger_list_actor_variable_curved_path_3d(actor, "key", 1)
```

---

## set_trigger_variable_curved_path_3d

method in GameAPI

- 描述

    设置全局触发器CURVED_PATH_3D非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.CurvedPath3D | 值 |

- 返回值

    无

- 示例

```lua
local curved_path_3d = {}

GameAPI.set_trigger_variable_curved_path_3d("key")
```

---

## set_trigger_actor_variable_curved_path_3d

method in GameAPI

- 描述

    设置全局触发器CURVED_PATH_3D非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.CurvedPath3D | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local curved_path_3d = {}

GameAPI.set_trigger_actor_variable_curved_path_3d(actor, "key")
```

---

## get_list_value_by_type

method in GameAPI

- 描述

    获取数组中某项（指定类型）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | var_type | string | 类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Actor | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_list_value_by_type(list, 1, "var_type")
```

---

## set_list_value_by_type

method in GameAPI

- 描述

    设置数组中某项（指定类型）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.Actor | 值 |
    | var_type | string | 类型 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local list = {}

GameAPI.set_list_value_by_type(list, 1, actor, "var_type")
```

---

## get_float_list_value

method in GameAPI

- 描述

    获取FLOAT数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_float_list_value(list, 1)
```

---

## set_float_list_value

method in GameAPI

- 描述

    设置FLOAT数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.Fixed | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_float_list_value(list, 1, Fix32(1))
```

---

## get_float_n_list

method in GameAPI

- 描述

    生成n个值为v的FLOAT数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.Fixed | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_float_n_list(1, Fix32(1))
```

---

## get_boolean_list_value

method in GameAPI

- 描述

    获取BOOLEAN数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_boolean_list_value(list, 1)
```

---

## set_boolean_list_value

method in GameAPI

- 描述

    设置BOOLEAN数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | boolean | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_boolean_list_value(list, 1, true)
```

---

## get_boolean_n_list

method in GameAPI

- 描述

    生成n个值为v的BOOLEAN数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | boolean | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_boolean_n_list(1, true)
```

---

## get_integer_list_value

method in GameAPI

- 描述

    获取INTEGER数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_integer_list_value(list, 1)
```

---

## set_integer_list_value

method in GameAPI

- 描述

    设置INTEGER数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | integer | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_integer_list_value(list, 1, 1)
```

---

## get_integer_n_list

method in GameAPI

- 描述

    生成n个值为v的INTEGER数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | integer | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_integer_n_list(1, 1)
```

---

## get_string_list_value

method in GameAPI

- 描述

    获取STRING数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_string_list_value(list, 1)
```

---

## set_string_list_value

method in GameAPI

- 描述

    设置STRING数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | string | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_string_list_value(list, 1, "v")
```

---

## get_string_n_list

method in GameAPI

- 描述

    生成n个值为v的STRING数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | string | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_string_n_list(1, "v")
```

---

## get_point_list_value

method in GameAPI

- 描述

    获取POINT数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FPoint | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_point_list_value(list, 1)
```

---

## set_point_list_value

method in GameAPI

- 描述

    设置POINT数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.FPoint | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local fpoint = GameAPI.get_point_by_res_id(1)

GameAPI.set_point_list_value(list, 1, fpoint)
```

---

## get_point_n_list

method in GameAPI

- 描述

    生成n个值为v的POINT数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.FPoint | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local fpoint = GameAPI.get_point_by_res_id(1)

local result = GameAPI.get_point_n_list(1)
```

---

## get_unit_entity_list_value

method in GameAPI

- 描述

    获取UNIT_ENTITY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_unit_entity_list_value(list, 1)
```

---

## set_unit_entity_list_value

method in GameAPI

- 描述

    设置UNIT_ENTITY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.Unit | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local list = {}

GameAPI.set_unit_entity_list_value(list, 1, unit.handle)
```

---

## get_unit_entity_n_list

method in GameAPI

- 描述

    生成n个值为v的UNIT_ENTITY数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.Unit | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = GameAPI.get_unit_entity_n_list(1)
```

---

## get_rectangle_list_value

method in GameAPI

- 描述

    获取RECTANGLE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RecArea | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_rectangle_list_value(list, 1)
```

---

## set_rectangle_list_value

method in GameAPI

- 描述

    设置RECTANGLE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.RecArea | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local rec_area = GameAPI.create_rec_area_from_two_points(Fix32Vec3(0, 0, 0), Fix32Vec3(100, 100, 0))

GameAPI.set_rectangle_list_value(list, 1, rec_area)
```

---

## get_rectangle_n_list

method in GameAPI

- 描述

    生成n个值为v的RECTANGLE数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.RecArea | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local rec_area = GameAPI.create_rec_area_from_two_points(Fix32Vec3(0, 0, 0), Fix32Vec3(100, 100, 0))

local result = GameAPI.get_rectangle_n_list(1)
```

---

## get_unit_type_list_value

method in GameAPI

- 描述

    获取UNIT_TYPE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitType | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_unit_type_list_value(list, 1)
```

---

## set_unit_type_list_value

method in GameAPI

- 描述

    设置UNIT_TYPE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.UnitType | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_unit_type_list_value(list, 1, 1)
```

---

## get_unit_type_n_list

method in GameAPI

- 描述

    生成n个值为v的UNIT_TYPE数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.UnitType | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_unit_type_n_list(1, 1)
```

---

## get_table_list_value

method in GameAPI

- 描述

    获取TABLE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Table | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_table_list_value(list, 1)
```

---

## set_table_list_value

method in GameAPI

- 描述

    设置TABLE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.Table | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local tbl = {}

GameAPI.set_table_list_value(list, 1, tbl)
```

---

## get_table_n_list

method in GameAPI

- 描述

    生成n个值为v的TABLE数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.Table | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local tbl = {}

local result = GameAPI.get_table_n_list(1)
```

---

## get_ability_list_value

method in GameAPI

- 描述

    获取ABILITY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Ability | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_ability_list_value(list, 1)
```

---

## set_ability_list_value

method in GameAPI

- 描述

    设置ABILITY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.Ability | 值 |

- 返回值

    无

- 示例

```lua
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)
local list = {}

GameAPI.set_ability_list_value(list, 1, ability.handle)
```

---

## get_ability_n_list

method in GameAPI

- 描述

    生成n个值为v的ABILITY数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.Ability | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = GameAPI.get_ability_n_list(1)
```

---

## get_team_list_value

method in GameAPI

- 描述

    获取TEAM数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Camp | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_team_list_value(list, 1)
```

---

## set_team_list_value

method in GameAPI

- 描述

    设置TEAM数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.Camp | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local camp = GameAPI.get_camp_by_camp_id(1)

GameAPI.set_team_list_value(list, 1, camp)
```

---

## get_team_n_list

method in GameAPI

- 描述

    生成n个值为v的TEAM数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.Camp | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local camp = GameAPI.get_camp_by_camp_id(1)

local result = GameAPI.get_team_n_list(1)
```

---

## get_round_area_list_value

method in GameAPI

- 描述

    获取ROUND_AREA数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CirArea | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_round_area_list_value(list, 1)
```

---

## set_round_area_list_value

method in GameAPI

- 描述

    设置ROUND_AREA数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.CirArea | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local cir_area = GameAPI.create_new_cir_area(GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0)), Fix32(100))

GameAPI.set_round_area_list_value(list, 1, cir_area)
```

---

## get_round_area_n_list

method in GameAPI

- 描述

    生成n个值为v的ROUND_AREA数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.CirArea | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local cir_area = GameAPI.create_new_cir_area(GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0)), Fix32(100))

local result = GameAPI.get_round_area_n_list(1)
```

---

## get_point_list_list_value

method in GameAPI

- 描述

    获取POINT_LIST数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Road | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_point_list_list_value(list, 1)
```

---

## set_point_list_list_value

method in GameAPI

- 描述

    设置POINT_LIST数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.Road | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local road = y3.road.get_road_by_res_id(1)

GameAPI.set_point_list_list_value(list, 1, road.handle)
```

---

## get_point_list_n_list

method in GameAPI

- 描述

    生成n个值为v的POINT_LIST数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.Road | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local road = y3.road.get_road_by_res_id(1)

local result = GameAPI.get_point_list_n_list(1)
```

---

## get_player_list_value

method in GameAPI

- 描述

    获取PLAYER数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Role | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_player_list_value(list, 1)
```

---

## set_player_list_value

method in GameAPI

- 描述

    设置PLAYER数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.Role | 值 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local list = {}

GameAPI.set_player_list_value(list, 1, player.handle)
```

---

## get_player_n_list

method in GameAPI

- 描述

    生成n个值为v的PLAYER数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.Role | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_player_n_list(1)
```

---

## get_unit_group_list_value

method in GameAPI

- 描述

    获取UNIT_GROUP数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitGroup | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_unit_group_list_value(list, 1)
```

---

## set_unit_group_list_value

method in GameAPI

- 描述

    设置UNIT_GROUP数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.UnitGroup | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local unit_group = y3.unit_group.create()

GameAPI.set_unit_group_list_value(list, 1, unit_group.handle)
```

---

## get_unit_group_n_list

method in GameAPI

- 描述

    生成n个值为v的UNIT_GROUP数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.UnitGroup | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local unit_group = y3.unit_group.create()

local result = GameAPI.get_unit_group_n_list(1)
```

---

## get_player_group_list_value

method in GameAPI

- 描述

    获取PLAYER_GROUP数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleGroup | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_player_group_list_value(list, 1)
```

---

## set_player_group_list_value

method in GameAPI

- 描述

    设置PLAYER_GROUP数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.RoleGroup | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local player_group = y3.player_group.create()

GameAPI.set_player_group_list_value(list, 1, player_group.handle)
```

---

## get_player_group_n_list

method in GameAPI

- 描述

    生成n个值为v的PLAYER_GROUP数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.RoleGroup | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local player_group = y3.player_group.create()

local result = GameAPI.get_player_group_n_list(1)
```

---

## get_item_entity_list_value

method in GameAPI

- 描述

    获取ITEM_ENTITY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Item | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_item_entity_list_value(list, 1)
```

---

## set_item_entity_list_value

method in GameAPI

- 描述

    设置ITEM_ENTITY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.Item | 值 |

- 返回值

    无

- 示例

```lua
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)
local list = {}

GameAPI.set_item_entity_list_value(list, 1, item.handle)
```

---

## get_item_entity_n_list

method in GameAPI

- 描述

    生成n个值为v的ITEM_ENTITY数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.Item | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = GameAPI.get_item_entity_n_list(1)
```

---

## get_item_name_list_value

method in GameAPI

- 描述

    获取ITEM_NAME数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemKey | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_item_name_list_value(list, 1)
```

---

## set_item_name_list_value

method in GameAPI

- 描述

    设置ITEM_NAME数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.ItemKey | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local item_key = 134274569

GameAPI.set_item_name_list_value(list, 1, item_key)
```

---

## get_item_name_n_list

method in GameAPI

- 描述

    生成n个值为v的ITEM_NAME数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.ItemKey | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_name_n_list(1)
```

---

## get_role_res_key_list_value

method in GameAPI

- 描述

    获取ROLE_RES_KEY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleResKey | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_role_res_key_list_value(list, 1)
```

---

## set_role_res_key_list_value

method in GameAPI

- 描述

    设置ROLE_RES_KEY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.RoleResKey | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local role_res_key = "res_key"

GameAPI.set_role_res_key_list_value(list, 1, role_res_key)
```

---

## get_role_res_key_n_list

method in GameAPI

- 描述

    生成n个值为v的ROLE_RES_KEY数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.RoleResKey | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local role_res_key = "res_key"

local result = GameAPI.get_role_res_key_n_list(1)
```

---

## get_unit_name_pool_list_value

method in GameAPI

- 描述

    获取UNIT_NAME_POOL数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitKeyPool | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_unit_name_pool_list_value(list, 1)
```

---

## set_unit_name_pool_list_value

method in GameAPI

- 描述

    设置UNIT_NAME_POOL数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.UnitKeyPool | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local unit_key_pool = GlobalAPI.get_empty_unit_key_pool()

GameAPI.set_unit_name_pool_list_value(list, 1, unit_key_pool)
```

---

## get_unit_name_pool_n_list

method in GameAPI

- 描述

    生成n个值为v的UNIT_NAME_POOL数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.UnitKeyPool | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local unit_key_pool = GlobalAPI.get_empty_unit_key_pool()

local result = GameAPI.get_unit_name_pool_n_list(1)
```

---

## get_ability_name_list_value

method in GameAPI

- 描述

    获取ABILITY_NAME数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityKey | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_ability_name_list_value(list, 1)
```

---

## set_ability_name_list_value

method in GameAPI

- 描述

    设置ABILITY_NAME数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.AbilityKey | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local ability_key = 134274569

GameAPI.set_ability_name_list_value(list, 1, ability_key)
```

---

## get_ability_name_n_list

method in GameAPI

- 描述

    生成n个值为v的ABILITY_NAME数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.AbilityKey | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_name_n_list(1)
```

---

## get_unit_write_attribute_list_value

method in GameAPI

- 描述

    获取UNIT_WRITE_ATTRIBUTE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_unit_write_attribute_list_value(list, 1)
```

---

## set_unit_write_attribute_list_value

method in GameAPI

- 描述

    设置UNIT_WRITE_ATTRIBUTE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | string | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_unit_write_attribute_list_value(list, 1, "v")
```

---

## get_unit_write_attribute_n_list

method in GameAPI

- 描述

    生成n个值为v的UNIT_WRITE_ATTRIBUTE数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | string | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_unit_write_attribute_n_list(1, "v")
```

---

## get_modifier_list_value

method in GameAPI

- 描述

    获取MODIFIER数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierKey | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_modifier_list_value(list, 1)
```

---

## set_modifier_list_value

method in GameAPI

- 描述

    设置MODIFIER数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.ModifierKey | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local modifier_key = 134274569

GameAPI.set_modifier_list_value(list, 1, modifier_key)
```

---

## get_modifier_n_list

method in GameAPI

- 描述

    生成n个值为v的MODIFIER数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.ModifierKey | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_n_list(1)
```

---

## get_projectile_list_value

method in GameAPI

- 描述

    获取PROJECTILE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileKey | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_projectile_list_value(list, 1)
```

---

## set_projectile_list_value

method in GameAPI

- 描述

    设置PROJECTILE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.ProjectileKey | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local projectile_key = 134274569

GameAPI.set_projectile_list_value(list, 1, projectile_key)
```

---

## get_projectile_n_list

method in GameAPI

- 描述

    生成n个值为v的PROJECTILE数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.ProjectileKey | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_n_list(1)
```

---

## get_damage_type_list_value

method in GameAPI

- 描述

    获取DAMAGE_TYPE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_damage_type_list_value(list, 1)
```

---

## set_damage_type_list_value

method in GameAPI

- 描述

    设置DAMAGE_TYPE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | integer | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_damage_type_list_value(list, 1, 1)
```

---

## get_damage_type_n_list

method in GameAPI

- 描述

    生成n个值为v的DAMAGE_TYPE数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | integer | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_damage_type_n_list(1, 1)
```

---

## get_sfx_key_list_value

method in GameAPI

- 描述

    获取SFX_KEY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SfxKey | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_sfx_key_list_value(list, 1)
```

---

## set_sfx_key_list_value

method in GameAPI

- 描述

    设置SFX_KEY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.SfxKey | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local sfx_key = 134274569

GameAPI.set_sfx_key_list_value(list, 1, sfx_key)
```

---

## get_sfx_key_n_list

method in GameAPI

- 描述

    生成n个值为v的SFX_KEY数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.SfxKey | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local sfx_key = 134274569

local result = GameAPI.get_sfx_key_n_list(1)
```

---

## get_ui_comp_list_value

method in GameAPI

- 描述

    获取UI_COMP数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_ui_comp_list_value(list, 1)
```

---

## set_ui_comp_list_value

method in GameAPI

- 描述

    设置UI_COMP数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | string | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_ui_comp_list_value(list, 1, "v")
```

---

## get_ui_comp_n_list

method in GameAPI

- 描述

    生成n个值为v的UI_COMP数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | string | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_ui_comp_n_list(1, "v")
```

---

## get_ui_comp_type_list_value

method in GameAPI

- 描述

    获取UI_COMP_TYPE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_ui_comp_type_list_value(list, 1)
```

---

## set_ui_comp_type_list_value

method in GameAPI

- 描述

    设置UI_COMP_TYPE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | integer | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_ui_comp_type_list_value(list, 1, 1)
```

---

## get_ui_comp_type_n_list

method in GameAPI

- 描述

    生成n个值为v的UI_COMP_TYPE数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | integer | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_ui_comp_type_n_list(1, 1)
```

---

## get_ui_comp_event_type_list_value

method in GameAPI

- 描述

    获取UI_COMP_EVENT_TYPE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_ui_comp_event_type_list_value(list, 1)
```

---

## set_ui_comp_event_type_list_value

method in GameAPI

- 描述

    设置UI_COMP_EVENT_TYPE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | integer | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_ui_comp_event_type_list_value(list, 1, 1)
```

---

## get_ui_comp_event_type_n_list

method in GameAPI

- 描述

    生成n个值为v的UI_COMP_EVENT_TYPE数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | integer | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_ui_comp_event_type_n_list(1, 1)
```

---

## get_camera_list_value

method in GameAPI

- 描述

    获取CAMERA数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Camera | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_camera_list_value(list, 1)
```

---

## set_camera_list_value

method in GameAPI

- 描述

    设置CAMERA数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.Camera | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local camera = y3.camera.create_camera(y3.point(0, 0), 1000, 500, 0, 45, 3000)

GameAPI.set_camera_list_value(list, 1, camera.handle)
```

---

## get_camera_n_list

method in GameAPI

- 描述

    生成n个值为v的CAMERA数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.Camera | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local camera = y3.camera.create_camera(y3.point(0, 0), 1000, 500, 0, 45, 3000)

local result = GameAPI.get_camera_n_list(1)
```

---

## get_modifier_entity_list_value

method in GameAPI

- 描述

    获取MODIFIER_ENTITY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierEntity | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_modifier_entity_list_value(list, 1)
```

---

## set_modifier_entity_list_value

method in GameAPI

- 描述

    设置MODIFIER_ENTITY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.ModifierEntity | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)
local list = {}

GameAPI.set_modifier_entity_list_value(list, 1, modifier.handle)
```

---

## get_modifier_entity_n_list

method in GameAPI

- 描述

    生成n个值为v的MODIFIER_ENTITY数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.ModifierEntity | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

local result = GameAPI.get_modifier_entity_n_list(1)
```

---

## get_projectile_entity_list_value

method in GameAPI

- 描述

    获取PROJECTILE_ENTITY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileEntity | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_projectile_entity_list_value(list, 1)
```

---

## set_projectile_entity_list_value

method in GameAPI

- 描述

    设置PROJECTILE_ENTITY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.ProjectileEntity | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local unit = y3.player.get_by_id(1):get_all_units()[1]
local target_point = unit:get_point()
local projectile = y3.projectile.create({ key = 134274569, target = target_point })

GameAPI.set_projectile_entity_list_value(list, 1, projectile.handle)
```

---

## get_projectile_entity_n_list

method in GameAPI

- 描述

    生成n个值为v的PROJECTILE_ENTITY数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.ProjectileEntity | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local target_point = unit:get_point()
local projectile = y3.projectile.create({ key = 134274569, target = target_point })

local result = GameAPI.get_projectile_entity_n_list(1)
```

---

## get_audio_key_list_value

method in GameAPI

- 描述

    获取AUDIO_KEY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AudioKey | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_audio_key_list_value(list, 1)
```

---

## set_audio_key_list_value

method in GameAPI

- 描述

    设置AUDIO_KEY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.AudioKey | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local audio_key = 134274569

GameAPI.set_audio_key_list_value(list, 1, audio_key)
```

---

## get_audio_key_n_list

method in GameAPI

- 描述

    生成n个值为v的AUDIO_KEY数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.AudioKey | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local audio_key = 134274569

local result = GameAPI.get_audio_key_n_list(1)
```

---

## get_texture_list_value

method in GameAPI

- 描述

    获取TEXTURE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Texture | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_texture_list_value(list, 1)
```

---

## set_texture_list_value

method in GameAPI

- 描述

    设置TEXTURE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.Texture | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_texture_list_value(list, 1, 1)
```

---

## get_texture_n_list

method in GameAPI

- 描述

    生成n个值为v的TEXTURE数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.Texture | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_texture_n_list(1, 1)
```

---

## get_unit_name_list_value

method in GameAPI

- 描述

    获取UNIT_NAME数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitKey | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_unit_name_list_value(list, 1)
```

---

## set_unit_name_list_value

method in GameAPI

- 描述

    设置UNIT_NAME数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.UnitKey | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local unit_key = 134274569

GameAPI.set_unit_name_list_value(list, 1, unit_key)
```

---

## get_unit_name_n_list

method in GameAPI

- 描述

    生成n个值为v的UNIT_NAME数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.UnitKey | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_name_n_list(1)
```

---

## get_model_list_value

method in GameAPI

- 描述

    获取MODEL数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModelKey | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_model_list_value(list, 1)
```

---

## set_model_list_value

method in GameAPI

- 描述

    设置MODEL数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.ModelKey | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local model_key = 1

GameAPI.set_model_list_value(list, 1, model_key)
```

---

## get_model_n_list

method in GameAPI

- 描述

    生成n个值为v的MODEL数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.ModelKey | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local model_key = 1

local result = GameAPI.get_model_n_list(1)
```

---

## get_store_key_list_value

method in GameAPI

- 描述

    获取STORE_KEY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.StoreKey | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_store_key_list_value(list, 1)
```

---

## set_store_key_list_value

method in GameAPI

- 描述

    设置STORE_KEY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.StoreKey | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local store_key = 134274569

GameAPI.set_store_key_list_value(list, 1, store_key)
```

---

## get_store_key_n_list

method in GameAPI

- 描述

    生成n个值为v的STORE_KEY数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.StoreKey | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local store_key = 134274569

local result = GameAPI.get_store_key_n_list(1)
```

---

## get_sfx_entity_list_value

method in GameAPI

- 描述

    获取SFX_ENTITY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sfx | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_sfx_entity_list_value(list, 1)
```

---

## set_sfx_entity_list_value

method in GameAPI

- 描述

    设置SFX_ENTITY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.Sfx | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local sfx = y3.particle.create({ type = 134274569, target = y3.point(0, 0) }).handle

GameAPI.set_sfx_entity_list_value(list, 1, sfx)
```

---

## get_sfx_entity_n_list

method in GameAPI

- 描述

    生成n个值为v的SFX_ENTITY数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.Sfx | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local sfx = y3.particle.create({ type = 134274569, target = y3.point(0, 0) }).handle

local result = GameAPI.get_sfx_entity_n_list(1)
```

---

## get_road_group_list_value

method in GameAPI

- 描述

    获取ROAD_GROUP数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoadGroup | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_road_group_list_value(list, 1)
```

---

## set_road_group_list_value

method in GameAPI

- 描述

    设置ROAD_GROUP数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.RoadGroup | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local road_group = GameAPI.get_trigger_variable_road_group("key")

GameAPI.set_road_group_list_value(list, 1, road_group)
```

---

## get_road_group_n_list

method in GameAPI

- 描述

    生成n个值为v的ROAD_GROUP数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.RoadGroup | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local road_group = GameAPI.get_trigger_variable_road_group("key")

local result = GameAPI.get_road_group_n_list(1)
```

---

## get_polygon_list_value

method in GameAPI

- 描述

    获取POLYGON数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PolyArea | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_polygon_list_value(list, 1)
```

---

## set_polygon_list_value

method in GameAPI

- 描述

    设置POLYGON数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.PolyArea | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local poly_area = GameAPI.create_polygon_area(Fix32Vec3(0, 0, 0), Fix32Vec3(100, 0, 0), Fix32Vec3(100, 100, 0))

GameAPI.set_polygon_list_value(list, 1, poly_area)
```

---

## get_polygon_n_list

method in GameAPI

- 描述

    生成n个值为v的POLYGON数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.PolyArea | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local poly_area = GameAPI.create_polygon_area(Fix32Vec3(0, 0, 0), Fix32Vec3(100, 0, 0), Fix32Vec3(100, 100, 0))

local result = GameAPI.get_polygon_n_list(1)
```

---

## get_item_group_list_value

method in GameAPI

- 描述

    获取ITEM_GROUP数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemGroup | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_item_group_list_value(list, 1)
```

---

## set_item_group_list_value

method in GameAPI

- 描述

    设置ITEM_GROUP数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.ItemGroup | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local item_group = y3.item_group.create()

GameAPI.set_item_group_list_value(list, 1, item_group.handle)
```

---

## get_item_group_n_list

method in GameAPI

- 描述

    生成n个值为v的ITEM_GROUP数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.ItemGroup | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local item_group = y3.item_group.create()

local result = GameAPI.get_item_group_n_list(1)
```

---

## get_tech_key_list_value

method in GameAPI

- 描述

    获取TECH_KEY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.TechKey | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_tech_key_list_value(list, 1)
```

---

## set_tech_key_list_value

method in GameAPI

- 描述

    设置TECH_KEY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.TechKey | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local tech_key = 134274569

GameAPI.set_tech_key_list_value(list, 1, tech_key)
```

---

## get_tech_key_n_list

method in GameAPI

- 描述

    生成n个值为v的TECH_KEY数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.TechKey | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_n_list(1)
```

---

## get_dynamic_trigger_instance_list_value

method in GameAPI

- 描述

    获取DYNAMIC_TRIGGER_INSTANCE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DynamicTriggerInstance | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_dynamic_trigger_instance_list_value(list, 1)
```

---

## set_dynamic_trigger_instance_list_value

method in GameAPI

- 描述

    设置DYNAMIC_TRIGGER_INSTANCE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.DynamicTriggerInstance | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local trigger_instance = GameAPI.get_last_created_trigger()

GameAPI.set_dynamic_trigger_instance_list_value(list, 1, trigger_instance)
```

---

## get_dynamic_trigger_instance_n_list

method in GameAPI

- 描述

    生成n个值为v的DYNAMIC_TRIGGER_INSTANCE数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.DynamicTriggerInstance | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local trigger_instance = GameAPI.get_last_created_trigger()

local result = GameAPI.get_dynamic_trigger_instance_n_list(1)
```

---

## get_role_type_list_value

method in GameAPI

- 描述

    获取ROLE_TYPE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleType | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_role_type_list_value(list, 1)
```

---

## set_role_type_list_value

method in GameAPI

- 描述

    设置ROLE_TYPE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.RoleType | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_role_type_list_value(list, 1, 1)
```

---

## get_role_type_n_list

method in GameAPI

- 描述

    生成n个值为v的ROLE_TYPE数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.RoleType | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_role_type_n_list(1, 1)
```

---

## get_role_status_list_value

method in GameAPI

- 描述

    获取ROLE_STATUS数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleStatus | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_role_status_list_value(list, 1)
```

---

## set_role_status_list_value

method in GameAPI

- 描述

    设置ROLE_STATUS数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.RoleStatus | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_role_status_list_value(list, 1, 1)
```

---

## get_role_status_n_list

method in GameAPI

- 描述

    生成n个值为v的ROLE_STATUS数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.RoleStatus | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_role_status_n_list(1, 1)
```

---

## get_new_timer_list_value

method in GameAPI

- 描述

    获取NEW_TIMER数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Timer | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_new_timer_list_value(list, 1)
```

---

## set_new_timer_list_value

method in GameAPI

- 描述

    设置NEW_TIMER数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.Timer | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local timer = y3.timer.loop(1, function() end)

GameAPI.set_new_timer_list_value(list, 1, timer.handle)
```

---

## get_new_timer_n_list

method in GameAPI

- 描述

    生成n个值为v的NEW_TIMER数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.Timer | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local timer = y3.timer.loop(1, function() end)

local result = GameAPI.get_new_timer_n_list(1)
```

---

## get_ability_type_list_value

method in GameAPI

- 描述

    获取ABILITY_TYPE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_ability_type_list_value(list, 1)
```

---

## set_ability_type_list_value

method in GameAPI

- 描述

    设置ABILITY_TYPE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | integer | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_ability_type_list_value(list, 1, 1)
```

---

## get_ability_type_n_list

method in GameAPI

- 描述

    生成n个值为v的ABILITY_TYPE数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | integer | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_ability_type_n_list(1, 1)
```

---

## get_link_sfx_key_list_value

method in GameAPI

- 描述

    获取LINK_SFX_KEY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LinkSfxKey | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_link_sfx_key_list_value(list, 1)
```

---

## set_link_sfx_key_list_value

method in GameAPI

- 描述

    设置LINK_SFX_KEY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.LinkSfxKey | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_link_sfx_key_list_value(list, 1, 1)
```

---

## get_link_sfx_key_n_list

method in GameAPI

- 描述

    生成n个值为v的LINK_SFX_KEY数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.LinkSfxKey | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_link_sfx_key_n_list(1, 1)
```

---

## get_ui_comp_align_type_list_value

method in GameAPI

- 描述

    获取UI_COMP_ALIGN_TYPE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_ui_comp_align_type_list_value(list, 1)
```

---

## set_ui_comp_align_type_list_value

method in GameAPI

- 描述

    设置UI_COMP_ALIGN_TYPE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | integer | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_ui_comp_align_type_list_value(list, 1, 1)
```

---

## get_ui_comp_align_type_n_list

method in GameAPI

- 描述

    生成n个值为v的UI_COMP_ALIGN_TYPE数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | integer | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_ui_comp_align_type_n_list(1, 1)
```

---

## get_ui_direction_list_value

method in GameAPI

- 描述

    获取UI_DIRECTION数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_ui_direction_list_value(list, 1)
```

---

## set_ui_direction_list_value

method in GameAPI

- 描述

    设置UI_DIRECTION数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | integer | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_ui_direction_list_value(list, 1, 1)
```

---

## get_ui_direction_n_list

method in GameAPI

- 描述

    生成n个值为v的UI_DIRECTION数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | integer | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_ui_direction_n_list(1, 1)
```

---

## get_random_pool_list_value

method in GameAPI

- 描述

    获取RANDOM_POOL数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RandomPool | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_random_pool_list_value(list, 1)
```

---

## set_random_pool_list_value

method in GameAPI

- 描述

    设置RANDOM_POOL数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.RandomPool | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local random_pool = GameAPI.create_random_pool()

GameAPI.set_random_pool_list_value(list, 1, random_pool)
```

---

## get_random_pool_n_list

method in GameAPI

- 描述

    生成n个值为v的RANDOM_POOL数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.RandomPool | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local random_pool = GameAPI.create_random_pool()

local result = GameAPI.get_random_pool_n_list(1)
```

---

## get_link_sfx_entity_list_value

method in GameAPI

- 描述

    获取LINK_SFX_ENTITY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LinkSfx | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_link_sfx_entity_list_value(list, 1)
```

---

## set_link_sfx_entity_list_value

method in GameAPI

- 描述

    设置LINK_SFX_ENTITY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.LinkSfx | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local unit = y3.player.get_by_id(1):get_all_units()[1]
local link_sfx = GameAPI.create_link_sfx_from_unit_to_point(134274569, unit.handle, "origin", GlobalAPI.coord_to_point(Fix32(100), Fix32(100), Fix32(0)), Fix32(0))

GameAPI.set_link_sfx_entity_list_value(list, 1, link_sfx)
```

---

## get_link_sfx_entity_n_list

method in GameAPI

- 描述

    生成n个值为v的LINK_SFX_ENTITY数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.LinkSfx | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local link_sfx = GameAPI.create_link_sfx_from_unit_to_point(134274569, unit.handle, "origin", GlobalAPI.coord_to_point(Fix32(100), Fix32(100), Fix32(0)), Fix32(0))

local result = GameAPI.get_link_sfx_entity_n_list(1)
```

---

## get_projectile_group_list_value

method in GameAPI

- 描述

    获取PROJECTILE_GROUP数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileGroup | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_projectile_group_list_value(list, 1)
```

---

## set_projectile_group_list_value

method in GameAPI

- 描述

    设置PROJECTILE_GROUP数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.ProjectileGroup | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local projectile_group = y3.projectile_group.create_lua_projectile_group_from_py(GameAPI.create_projectile_group())

GameAPI.set_projectile_group_list_value(list, 1, projectile_group.handle)
```

---

## get_projectile_group_n_list

method in GameAPI

- 描述

    生成n个值为v的PROJECTILE_GROUP数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.ProjectileGroup | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local projectile_group = y3.projectile_group.create_lua_projectile_group_from_py(GameAPI.create_projectile_group())

local result = GameAPI.get_projectile_group_n_list(1)
```

---

## get_destructible_entity_list_value

method in GameAPI

- 描述

    获取DESTRUCTIBLE_ENTITY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Destructible | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_destructible_entity_list_value(list, 1)
```

---

## set_destructible_entity_list_value

method in GameAPI

- 描述

    设置DESTRUCTIBLE_ENTITY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.Destructible | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local destructible = y3.destructible.get_by_id(1)
if destructible then

GameAPI.set_destructible_entity_list_value(list, 1, destructible.handle)
end
```

---

## get_destructible_entity_n_list

method in GameAPI

- 描述

    生成n个值为v的DESTRUCTIBLE_ENTITY数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.Destructible | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

local result = GameAPI.get_destructible_entity_n_list(1)
end
```

---

## get_destructible_name_list_value

method in GameAPI

- 描述

    获取DESTRUCTIBLE_NAME数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DestructibleKey | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_destructible_name_list_value(list, 1)
```

---

## set_destructible_name_list_value

method in GameAPI

- 描述

    设置DESTRUCTIBLE_NAME数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.DestructibleKey | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local destructible_key = 1

GameAPI.set_destructible_name_list_value(list, 1, destructible_key)
```

---

## get_destructible_name_n_list

method in GameAPI

- 描述

    生成n个值为v的DESTRUCTIBLE_NAME数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.DestructibleKey | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_name_n_list(1)
```

---

## get_sound_entity_list_value

method in GameAPI

- 描述

    获取SOUND_ENTITY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SoundEntity | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_sound_entity_list_value(list, 1)
```

---

## set_sound_entity_list_value

method in GameAPI

- 描述

    设置SOUND_ENTITY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.SoundEntity | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local player = y3.player.get_by_id(1)
local sound_entity = GameAPI.play_sound_for_player(player.handle, 134274569, false)

GameAPI.set_sound_entity_list_value(list, 1, sound_entity)
```

---

## get_sound_entity_n_list

method in GameAPI

- 描述

    生成n个值为v的SOUND_ENTITY数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.SoundEntity | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local sound_entity = GameAPI.play_sound_for_player(player.handle, 134274569, false)

local result = GameAPI.get_sound_entity_n_list(1)
```

---

## get_ability_cast_type_list_value

method in GameAPI

- 描述

    获取ABILITY_CAST_TYPE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_ability_cast_type_list_value(list, 1)
```

---

## set_ability_cast_type_list_value

method in GameAPI

- 描述

    设置ABILITY_CAST_TYPE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | integer | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_ability_cast_type_list_value(list, 1, 1)
```

---

## get_ability_cast_type_n_list

method in GameAPI

- 描述

    生成n个值为v的ABILITY_CAST_TYPE数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | integer | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_ability_cast_type_n_list(1, 1)
```

---

## get_curved_path_list_value

method in GameAPI

- 描述

    获取CURVED_PATH数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CurvedPath | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_curved_path_list_value(list, 1)
```

---

## set_curved_path_list_value

method in GameAPI

- 描述

    设置CURVED_PATH数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.CurvedPath | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local path = {}

GameAPI.set_curved_path_list_value(list, 1, path)
```

---

## get_curved_path_n_list

method in GameAPI

- 描述

    生成n个值为v的CURVED_PATH数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.CurvedPath | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local path = {}

local result = GameAPI.get_curved_path_n_list(1)
```

---

## get_image_key_list_value

method in GameAPI

- 描述

    获取IMAGE_KEY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_image_key_list_value(list, 1)
```

---

## set_image_key_list_value

method in GameAPI

- 描述

    设置IMAGE_KEY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | integer | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_image_key_list_value(list, 1, 1)
```

---

## get_image_key_n_list

method in GameAPI

- 描述

    生成n个值为v的IMAGE_KEY数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | integer | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_image_key_n_list(1, 1)
```

---

## get_angle_list_value

method in GameAPI

- 描述

    获取ANGLE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_angle_list_value(list, 1)
```

---

## set_angle_list_value

method in GameAPI

- 描述

    设置ANGLE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.Fixed | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_angle_list_value(list, 1, Fix32(1))
```

---

## get_angle_n_list

method in GameAPI

- 描述

    生成n个值为v的ANGLE数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.Fixed | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_angle_n_list(1, Fix32(1))
```

---

## get_curved_path_3d_list_value

method in GameAPI

- 描述

    获取CURVED_PATH_3D数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CurvedPath3D | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_curved_path_3d_list_value(list, 1)
```

---

## set_curved_path_3d_list_value

method in GameAPI

- 描述

    设置CURVED_PATH_3D数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.CurvedPath3D | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local curved_path_3d = {}

GameAPI.set_curved_path_3d_list_value(list, 1, curved_path_3d)
```

---

## get_curved_path_3d_n_list

method in GameAPI

- 描述

    生成n个值为v的CURVED_PATH_3D数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.CurvedPath3D | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local curved_path_3d = {}

local result = GameAPI.get_curved_path_3d_n_list(1)
```

---

## get_int_save_list_value

method in GameAPI

- 描述

    获取INT_SAVE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_int_save_list_value(list, 1)
```

---

## set_int_save_list_value

method in GameAPI

- 描述

    设置INT_SAVE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | integer | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_int_save_list_value(list, 1, 1)
```

---

## get_int_save_n_list

method in GameAPI

- 描述

    生成n个值为v的INT_SAVE数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | integer | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_int_save_n_list(1, 1)
```

---

## get_str_save_list_value

method in GameAPI

- 描述

    获取STR_SAVE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_str_save_list_value(list, 1)
```

---

## set_str_save_list_value

method in GameAPI

- 描述

    设置STR_SAVE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | string | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_str_save_list_value(list, 1, "v")
```

---

## get_str_save_n_list

method in GameAPI

- 描述

    生成n个值为v的STR_SAVE数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | string | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_str_save_n_list(1, "v")
```

---

## get_float_save_list_value

method in GameAPI

- 描述

    获取FLOAT_SAVE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_float_save_list_value(list, 1)
```

---

## set_float_save_list_value

method in GameAPI

- 描述

    设置FLOAT_SAVE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.Fixed | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_float_save_list_value(list, 1, Fix32(1))
```

---

## get_float_save_n_list

method in GameAPI

- 描述

    生成n个值为v的FLOAT_SAVE数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.Fixed | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_float_save_n_list(1, Fix32(1))
```

---

## get_bool_save_list_value

method in GameAPI

- 描述

    获取BOOL_SAVE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_bool_save_list_value(list, 1)
```

---

## set_bool_save_list_value

method in GameAPI

- 描述

    设置BOOL_SAVE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | boolean | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_bool_save_list_value(list, 1, true)
```

---

## get_bool_save_n_list

method in GameAPI

- 描述

    生成n个值为v的BOOL_SAVE数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | boolean | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_bool_save_n_list(1, true)
```

---

## get_scene_ui_list_value

method in GameAPI

- 描述

    获取SCENE_UI数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SceneNode | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_scene_ui_list_value(list, 1)
```

---

## set_scene_ui_list_value

method in GameAPI

- 描述

    设置SCENE_UI数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.SceneNode | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local player = y3.player.get_by_id(1)
local unit = player:get_all_units()[1]
local scene_node = GameAPI.create_scene_node_on_unit_ex("comp_name", player.handle, unit.handle, "origin", false)

GameAPI.set_scene_ui_list_value(list, 1, scene_node)
```

---

## get_scene_ui_n_list

method in GameAPI

- 描述

    生成n个值为v的SCENE_UI数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.SceneNode | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local unit = player:get_all_units()[1]
local scene_node = GameAPI.create_scene_node_on_unit_ex("comp_name", player.handle, unit.handle, "origin", false)

local result = GameAPI.get_scene_ui_n_list(1)
```

---

## get_ui_anim_list_value

method in GameAPI

- 描述

    获取UI_ANIM数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UIAnimKey | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_ui_anim_list_value(list, 1)
```

---

## set_ui_anim_list_value

method in GameAPI

- 描述

    设置UI_ANIM数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.UIAnimKey | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local ui_anim_key = GameAPI.get_unit_key_ui_anim_kv(1, "key")

GameAPI.set_ui_anim_list_value(list, 1, ui_anim_key)
```

---

## get_ui_anim_n_list

method in GameAPI

- 描述

    生成n个值为v的UI_ANIM数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.UIAnimKey | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local ui_anim_key = GameAPI.get_unit_key_ui_anim_kv(1, "key")

local result = GameAPI.get_ui_anim_n_list(1)
```

---

## get_camline_list_value

method in GameAPI

- 描述

    获取CAMLINE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CamlineID | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_camline_list_value(list, 1)
```

---

## set_camline_list_value

method in GameAPI

- 描述

    设置CAMLINE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.CamlineID | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_camline_list_value(list, 1, 1)
```

---

## get_camline_n_list

method in GameAPI

- 描述

    生成n个值为v的CAMLINE数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.CamlineID | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_camline_n_list(1, 1)
```

---

## get_table_save_list_value

method in GameAPI

- 描述

    获取TABLE_SAVE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Table | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_table_save_list_value(list, 1)
```

---

## set_table_save_list_value

method in GameAPI

- 描述

    设置TABLE_SAVE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.Table | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local tbl = {}

GameAPI.set_table_save_list_value(list, 1, tbl)
```

---

## get_table_save_n_list

method in GameAPI

- 描述

    生成n个值为v的TABLE_SAVE数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.Table | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local tbl = {}

local result = GameAPI.get_table_save_n_list(1)
```

---

## get_mover_entity_list_value

method in GameAPI

- 描述

    获取MOVER_ENTITY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Mover | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_mover_entity_list_value(list, 1)
```

---

## set_mover_entity_list_value

method in GameAPI

- 描述

    设置MOVER_ENTITY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.Mover | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })
local mover = GameAPI.get_projectile_mover(projectile.handle)

GameAPI.set_mover_entity_list_value(list, 1, mover)
```

---

## get_mover_entity_n_list

method in GameAPI

- 描述

    生成n个值为v的MOVER_ENTITY数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.Mover | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })
local mover = GameAPI.get_projectile_mover(projectile.handle)

local result = GameAPI.get_mover_entity_n_list(1)
```

---

## get_cursor_key_list_value

method in GameAPI

- 描述

    获取CURSOR_KEY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CursorKey | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_cursor_key_list_value(list, 1)
```

---

## set_cursor_key_list_value

method in GameAPI

- 描述

    设置CURSOR_KEY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.CursorKey | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_cursor_key_list_value(list, 1, 1)
```

---

## get_cursor_key_n_list

method in GameAPI

- 描述

    生成n个值为v的CURSOR_KEY数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.CursorKey | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_cursor_key_n_list(1, 1)
```

---

## get_vector3_list_value

method in GameAPI

- 描述

    获取VECTOR3数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3 | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_vector3_list_value(list, 1)
```

---

## set_vector3_list_value

method in GameAPI

- 描述

    设置VECTOR3数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.FVector3 | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

GameAPI.set_vector3_list_value(list, 1, fvector3)
```

---

## get_vector3_n_list

method in GameAPI

- 描述

    生成n个值为v的VECTOR3数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.FVector3 | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

local result = GameAPI.get_vector3_n_list(1)
```

---

## get_sequence_list_value

method in GameAPI

- 描述

    获取SEQUENCE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sequence | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_sequence_list_value(list, 1)
```

---

## set_sequence_list_value

method in GameAPI

- 描述

    设置SEQUENCE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.Sequence | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_sequence_list_value(list, 1, 1)
```

---

## get_sequence_n_list

method in GameAPI

- 描述

    生成n个值为v的SEQUENCE数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.Sequence | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_sequence_n_list(1, 1)
```

---

## get_physics_object_list_value

method in GameAPI

- 描述

    获取PHYSICS_OBJECT数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsObject | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_physics_object_list_value(list, 1)
```

---

## set_physics_object_list_value

method in GameAPI

- 描述

    设置PHYSICS_OBJECT数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.PhysicsObject | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local physics_object = GameAPI.get_unit_key_physics_object_kv(1, "key")

GameAPI.set_physics_object_list_value(list, 1, physics_object)
```

---

## get_physics_object_n_list

method in GameAPI

- 描述

    生成n个值为v的PHYSICS_OBJECT数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.PhysicsObject | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local physics_object = GameAPI.get_unit_key_physics_object_kv(1, "key")

local result = GameAPI.get_physics_object_n_list(1)
```

---

## get_physics_entity_list_value

method in GameAPI

- 描述

    获取PHYSICS_ENTITY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsEntity | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_physics_entity_list_value(list, 1)
```

---

## set_physics_entity_list_value

method in GameAPI

- 描述

    设置PHYSICS_ENTITY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.PhysicsEntity | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local physics_entity = GameAPI.get_unit_key_physics_entity_kv(1, "key")

GameAPI.set_physics_entity_list_value(list, 1, physics_entity)
```

---

## get_physics_entity_n_list

method in GameAPI

- 描述

    生成n个值为v的PHYSICS_ENTITY数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.PhysicsEntity | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local physics_entity = GameAPI.get_unit_key_physics_entity_kv(1, "key")

local result = GameAPI.get_physics_entity_n_list(1)
```

---

## get_rigid_body_list_value

method in GameAPI

- 描述

    获取RIGID_BODY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RigidBody | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_rigid_body_list_value(list, 1)
```

---

## set_rigid_body_list_value

method in GameAPI

- 描述

    设置RIGID_BODY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.RigidBody | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local rigid_body = GameAPI.get_unit_key_rigid_body_kv(1, "key")

GameAPI.set_rigid_body_list_value(list, 1, rigid_body)
```

---

## get_rigid_body_n_list

method in GameAPI

- 描述

    生成n个值为v的RIGID_BODY数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.RigidBody | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local rigid_body = GameAPI.get_unit_key_rigid_body_kv(1, "key")

local result = GameAPI.get_rigid_body_n_list(1)
```

---

## get_collider_list_value

method in GameAPI

- 描述

    获取COLLIDER数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Collider | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_collider_list_value(list, 1)
```

---

## set_collider_list_value

method in GameAPI

- 描述

    设置COLLIDER数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.Collider | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local collider = GameAPI.get_unit_key_collider_kv(1, "key")

GameAPI.set_collider_list_value(list, 1, collider)
```

---

## get_collider_n_list

method in GameAPI

- 描述

    生成n个值为v的COLLIDER数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.Collider | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local collider = GameAPI.get_unit_key_collider_kv(1, "key")

local result = GameAPI.get_collider_n_list(1)
```

---

## get_attr_element_list_value

method in GameAPI

- 描述

    获取ATTR_ELEMENT数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_attr_element_list_value(list, 1)
```

---

## set_attr_element_list_value

method in GameAPI

- 描述

    设置ATTR_ELEMENT数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | string | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_attr_element_list_value(list, 1, "v")
```

---

## get_attr_element_n_list

method in GameAPI

- 描述

    生成n个值为v的ATTR_ELEMENT数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | string | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_attr_element_n_list(1, "v")
```

---

## get_attr_element_read_list_value

method in GameAPI

- 描述

    获取ATTR_ELEMENT_READ数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_attr_element_read_list_value(list, 1)
```

---

## set_attr_element_read_list_value

method in GameAPI

- 描述

    设置ATTR_ELEMENT_READ数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | string | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_attr_element_read_list_value(list, 1, "v")
```

---

## get_attr_element_read_n_list

method in GameAPI

- 描述

    生成n个值为v的ATTR_ELEMENT_READ数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | string | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_attr_element_read_n_list(1, "v")
```

---

## get_joint_list_value

method in GameAPI

- 描述

    获取JOINT数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Joint | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_joint_list_value(list, 1)
```

---

## set_joint_list_value

method in GameAPI

- 描述

    设置JOINT数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.Joint | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local joint = GameAPI.get_unit_key_joint_kv(1, "key")

GameAPI.set_joint_list_value(list, 1, joint)
```

---

## get_joint_n_list

method in GameAPI

- 描述

    生成n个值为v的JOINT数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.Joint | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local joint = GameAPI.get_unit_key_joint_kv(1, "key")

local result = GameAPI.get_joint_n_list(1)
```

---

## get_physics_object_key_list_value

method in GameAPI

- 描述

    获取PHYSICS_OBJECT_KEY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsObjectKey | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_physics_object_key_list_value(list, 1)
```

---

## set_physics_object_key_list_value

method in GameAPI

- 描述

    设置PHYSICS_OBJECT_KEY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.PhysicsObjectKey | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_physics_object_key_list_value(list, 1, 1)
```

---

## get_physics_object_key_n_list

method in GameAPI

- 描述

    生成n个值为v的PHYSICS_OBJECT_KEY数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.PhysicsObjectKey | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_physics_object_key_n_list(1, 1)
```

---

## get_physics_entity_key_list_value

method in GameAPI

- 描述

    获取PHYSICS_ENTITY_KEY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsEntityKey | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_physics_entity_key_list_value(list, 1)
```

---

## set_physics_entity_key_list_value

method in GameAPI

- 描述

    设置PHYSICS_ENTITY_KEY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.PhysicsEntityKey | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_physics_entity_key_list_value(list, 1, 1)
```

---

## get_physics_entity_key_n_list

method in GameAPI

- 描述

    生成n个值为v的PHYSICS_ENTITY_KEY数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.PhysicsEntityKey | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_n_list(1, 1)
```

---

## get_rotation_list_value

method in GameAPI

- 描述

    获取ROTATION数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FRotation | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_rotation_list_value(list, 1)
```

---

## set_rotation_list_value

method in GameAPI

- 描述

    设置ROTATION数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.FRotation | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_rotation_list_value(list, 1, GlobalAPI.vector3_to_euler(Fix32Vec3(0, 0, 0)))
```

---

## get_rotation_n_list

method in GameAPI

- 描述

    生成n个值为v的ROTATION数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.FRotation | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_rotation_n_list(1)
```

---

## get_rigid_body_group_list_value

method in GameAPI

- 描述

    获取RIGID_BODY_GROUP数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RigidBodyGroup | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_rigid_body_group_list_value(list, 1)
```

---

## set_rigid_body_group_list_value

method in GameAPI

- 描述

    设置RIGID_BODY_GROUP数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.RigidBodyGroup | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local rigid_body_group = GameAPI.get_unit_key_rigid_body_group_kv(1, "key")

GameAPI.set_rigid_body_group_list_value(list, 1, rigid_body_group)
```

---

## get_rigid_body_group_n_list

method in GameAPI

- 描述

    生成n个值为v的RIGID_BODY_GROUP数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.RigidBodyGroup | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local rigid_body_group = GameAPI.get_unit_key_rigid_body_group_kv(1, "key")

local result = GameAPI.get_rigid_body_group_n_list(1)
```

---

## get_reaction_list_value

method in GameAPI

- 描述

    获取REACTION数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Reaction | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_reaction_list_value(list, 1)
```

---

## set_reaction_list_value

method in GameAPI

- 描述

    设置REACTION数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.Reaction | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local physics_entity = GameAPI.get_unit_key_physics_entity_kv(1, "key")
local reaction = GameAPI.api_add_uniform_gravitation_field_to_rigid_body(physics_entity, Fix32(10), Fix32Vec3(0, 0, 0))

GameAPI.set_reaction_list_value(list, 1, reaction)
```

---

## get_reaction_n_list

method in GameAPI

- 描述

    生成n个值为v的REACTION数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.Reaction | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local physics_entity = GameAPI.get_unit_key_physics_entity_kv(1, "key")
local reaction = GameAPI.api_add_uniform_gravitation_field_to_rigid_body(physics_entity, Fix32(10), Fix32Vec3(0, 0, 0))

local result = GameAPI.get_reaction_n_list(1)
```

---

## get_reaction_group_list_value

method in GameAPI

- 描述

    获取REACTION_GROUP数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ReactionGroup | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_reaction_group_list_value(list, 1)
```

---

## set_reaction_group_list_value

method in GameAPI

- 描述

    设置REACTION_GROUP数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.ReactionGroup | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local reaction_group = GameAPI.get_trigger_variable_reaction_group("key")

GameAPI.set_reaction_group_list_value(list, 1, reaction_group)
```

---

## get_reaction_group_n_list

method in GameAPI

- 描述

    生成n个值为v的REACTION_GROUP数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.ReactionGroup | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local reaction_group = GameAPI.get_trigger_variable_reaction_group("key")

local result = GameAPI.get_reaction_group_n_list(1)
```

---

## get_ui_anim_curve_list_value

method in GameAPI

- 描述

    获取UI_ANIM_CURVE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_ui_anim_curve_list_value(list, 1)
```

---

## set_ui_anim_curve_list_value

method in GameAPI

- 描述

    设置UI_ANIM_CURVE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | integer | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_ui_anim_curve_list_value(list, 1, 1)
```

---

## get_ui_anim_curve_n_list

method in GameAPI

- 描述

    生成n个值为v的UI_ANIM_CURVE数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | integer | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_ui_anim_curve_n_list(1, 1)
```

---

## get_physics_filter_list_value

method in GameAPI

- 描述

    获取PHYSICS_FILTER数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsFilter | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_physics_filter_list_value(list, 1)
```

---

## set_physics_filter_list_value

method in GameAPI

- 描述

    设置PHYSICS_FILTER数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.PhysicsFilter | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local physics_filter = GameAPI.api_create_physics_filter(1, 1, false, false, false, false, false)

GameAPI.set_physics_filter_list_value(list, 1, physics_filter)
```

---

## get_physics_filter_n_list

method in GameAPI

- 描述

    生成n个值为v的PHYSICS_FILTER数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.PhysicsFilter | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local physics_filter = GameAPI.api_create_physics_filter(1, 1, false, false, false, false, false)

local result = GameAPI.get_physics_filter_n_list(1)
```

---

## get_global_archive_slot_list_value

method in GameAPI

- 描述

    获取GLOBAL_ARCHIVE_SLOT数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_global_archive_slot_list_value(list, 1)
```

---

## set_global_archive_slot_list_value

method in GameAPI

- 描述

    设置GLOBAL_ARCHIVE_SLOT数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | string | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_global_archive_slot_list_value(list, 1, "v")
```

---

## get_global_archive_slot_n_list

method in GameAPI

- 描述

    生成n个值为v的GLOBAL_ARCHIVE_SLOT数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | string | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_global_archive_slot_n_list(1, "v")
```

---

## get_random_pool_drop_list_value

method in GameAPI

- 描述

    获取RANDOM_POOL_DROP数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_random_pool_drop_list_value(list, 1)
```

---

## set_random_pool_drop_list_value

method in GameAPI

- 描述

    设置RANDOM_POOL_DROP数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | integer | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_random_pool_drop_list_value(list, 1, 1)
```

---

## get_random_pool_drop_n_list

method in GameAPI

- 描述

    生成n个值为v的RANDOM_POOL_DROP数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | integer | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_random_pool_drop_n_list(1, 1)
```

---

## get_damage_attack_type_list_value

method in GameAPI

- 描述

    获取DAMAGE_ATTACK_TYPE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_damage_attack_type_list_value(list, 1)
```

---

## set_damage_attack_type_list_value

method in GameAPI

- 描述

    设置DAMAGE_ATTACK_TYPE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | integer | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_damage_attack_type_list_value(list, 1, 1)
```

---

## get_damage_attack_type_n_list

method in GameAPI

- 描述

    生成n个值为v的DAMAGE_ATTACK_TYPE数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | integer | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_damage_attack_type_n_list(1, 1)
```

---

## get_damage_armor_type_list_value

method in GameAPI

- 描述

    获取DAMAGE_ARMOR_TYPE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_damage_armor_type_list_value(list, 1)
```

---

## set_damage_armor_type_list_value

method in GameAPI

- 描述

    设置DAMAGE_ARMOR_TYPE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | integer | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_damage_armor_type_list_value(list, 1, 1)
```

---

## get_damage_armor_type_n_list

method in GameAPI

- 描述

    生成n个值为v的DAMAGE_ARMOR_TYPE数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | integer | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_damage_armor_type_n_list(1, 1)
```

---

## get_game_mode_list_value

method in GameAPI

- 描述

    获取GAME_MODE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.GameMode | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_game_mode_list_value(list, 1)
```

---

## set_game_mode_list_value

method in GameAPI

- 描述

    设置GAME_MODE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.GameMode | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_game_mode_list_value(list, 1, 1)
```

---

## get_game_mode_n_list

method in GameAPI

- 描述

    生成n个值为v的GAME_MODE数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.GameMode | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_game_mode_n_list(1, 1)
```

---

## get_image_quality_list_value

method in GameAPI

- 描述

    获取IMAGE_QUALITY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_image_quality_list_value(list, 1)
```

---

## set_image_quality_list_value

method in GameAPI

- 描述

    设置IMAGE_QUALITY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | string | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_image_quality_list_value(list, 1, "v")
```

---

## get_image_quality_n_list

method in GameAPI

- 描述

    生成n个值为v的IMAGE_QUALITY数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | string | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_image_quality_n_list(1, "v")
```

---

## get_window_type_setting_list_value

method in GameAPI

- 描述

    获取WINDOW_TYPE_SETTING数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_window_type_setting_list_value(list, 1)
```

---

## set_window_type_setting_list_value

method in GameAPI

- 描述

    设置WINDOW_TYPE_SETTING数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | string | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_window_type_setting_list_value(list, 1, "v")
```

---

## get_window_type_setting_n_list

method in GameAPI

- 描述

    生成n个值为v的WINDOW_TYPE_SETTING数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | string | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_window_type_setting_n_list(1, "v")
```

---

## get_keyboard_key_list_value

method in GameAPI

- 描述

    获取KEYBOARD_KEY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.KeyboardKey | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_keyboard_key_list_value(list, 1)
```

---

## set_keyboard_key_list_value

method in GameAPI

- 描述

    设置KEYBOARD_KEY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.KeyboardKey | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_keyboard_key_list_value(list, 1, 1)
```

---

## get_keyboard_key_n_list

method in GameAPI

- 描述

    生成n个值为v的KEYBOARD_KEY数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.KeyboardKey | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_keyboard_key_n_list(1, 1)
```

---

## get_point_light_list_value

method in GameAPI

- 描述

    获取POINT_LIGHT数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PointLight | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_point_light_list_value(list, 1)
```

---

## set_point_light_list_value

method in GameAPI

- 描述

    设置POINT_LIGHT数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.PointLight | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local point_light = GameAPI.get_point_light_res_by_res_id(1)

GameAPI.set_point_light_list_value(list, 1, point_light)
```

---

## get_point_light_n_list

method in GameAPI

- 描述

    生成n个值为v的POINT_LIGHT数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.PointLight | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local point_light = GameAPI.get_point_light_res_by_res_id(1)

local result = GameAPI.get_point_light_n_list(1)
```

---

## get_spot_light_list_value

method in GameAPI

- 描述

    获取SPOT_LIGHT数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SpotLight | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_spot_light_list_value(list, 1)
```

---

## set_spot_light_list_value

method in GameAPI

- 描述

    设置SPOT_LIGHT数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.SpotLight | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local spot_light = GameAPI.get_spot_light_res_by_res_id(1)

GameAPI.set_spot_light_list_value(list, 1, spot_light)
```

---

## get_spot_light_n_list

method in GameAPI

- 描述

    生成n个值为v的SPOT_LIGHT数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.SpotLight | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local spot_light = GameAPI.get_spot_light_res_by_res_id(1)

local result = GameAPI.get_spot_light_n_list(1)
```

---

## get_fog_list_value

method in GameAPI

- 描述

    获取FOG数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fog | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_fog_list_value(list, 1)
```

---

## set_fog_list_value

method in GameAPI

- 描述

    设置FOG数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.Fog | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local fog = GameAPI.get_fog_res_by_res_id(1)

GameAPI.set_fog_list_value(list, 1, fog)
```

---

## get_fog_n_list

method in GameAPI

- 描述

    生成n个值为v的FOG数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.Fog | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local fog = GameAPI.get_fog_res_by_res_id(1)

local result = GameAPI.get_fog_n_list(1)
```

---

## get_ui_prefab_list_value

method in GameAPI

- 描述

    获取UI_PREFAB数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_ui_prefab_list_value(list, 1)
```

---

## set_ui_prefab_list_value

method in GameAPI

- 描述

    设置UI_PREFAB数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | string | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_ui_prefab_list_value(list, 1, "v")
```

---

## get_ui_prefab_n_list

method in GameAPI

- 描述

    生成n个值为v的UI_PREFAB数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | string | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_ui_prefab_n_list(1, "v")
```

---

## get_ui_prefab_instance_list_value

method in GameAPI

- 描述

    获取UI_PREFAB_INSTANCE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UIPrefabIns | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_ui_prefab_instance_list_value(list, 1)
```

---

## set_ui_prefab_instance_list_value

method in GameAPI

- 描述

    设置UI_PREFAB_INSTANCE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.UIPrefabIns | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local player = y3.player.get_by_id(1)
local ui_prefab_ins = GameAPI.get_ui_prefab_ins(player.handle, "prefab_uid")

GameAPI.set_ui_prefab_instance_list_value(list, 1, ui_prefab_ins)
```

---

## get_ui_prefab_instance_n_list

method in GameAPI

- 描述

    生成n个值为v的UI_PREFAB_INSTANCE数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.UIPrefabIns | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui_prefab_ins = GameAPI.get_ui_prefab_ins(player.handle, "prefab_uid")

local result = GameAPI.get_ui_prefab_instance_n_list(1)
```

---

## get_ui_prefab_ins_uid_list_value

method in GameAPI

- 描述

    获取UI_PREFAB_INS_UID数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_ui_prefab_ins_uid_list_value(list, 1)
```

---

## set_ui_prefab_ins_uid_list_value

method in GameAPI

- 描述

    设置UI_PREFAB_INS_UID数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | string | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_ui_prefab_ins_uid_list_value(list, 1, "v")
```

---

## get_ui_prefab_ins_uid_n_list

method in GameAPI

- 描述

    生成n个值为v的UI_PREFAB_INS_UID数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | string | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_ui_prefab_ins_uid_n_list(1, "v")
```

---

## get_audio_channel_list_value

method in GameAPI

- 描述

    获取AUDIO_CHANNEL数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_audio_channel_list_value(list, 1)
```

---

## set_audio_channel_list_value

method in GameAPI

- 描述

    设置AUDIO_CHANNEL数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | integer | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_audio_channel_list_value(list, 1, 1)
```

---

## get_audio_channel_n_list

method in GameAPI

- 描述

    生成n个值为v的AUDIO_CHANNEL数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | integer | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_audio_channel_n_list(1, 1)
```

---

## get_ui_model_camera_mod_list_value

method in GameAPI

- 描述

    获取UI_MODEL_CAMERA_MOD数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_ui_model_camera_mod_list_value(list, 1)
```

---

## set_ui_model_camera_mod_list_value

method in GameAPI

- 描述

    设置UI_MODEL_CAMERA_MOD数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | integer | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_ui_model_camera_mod_list_value(list, 1, 1)
```

---

## get_ui_model_camera_mod_n_list

method in GameAPI

- 描述

    生成n个值为v的UI_MODEL_CAMERA_MOD数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | integer | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_ui_model_camera_mod_n_list(1, 1)
```

---

## get_ui_btn_status_list_value

method in GameAPI

- 描述

    获取UI_BTN_STATUS数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_ui_btn_status_list_value(list, 1)
```

---

## set_ui_btn_status_list_value

method in GameAPI

- 描述

    设置UI_BTN_STATUS数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | integer | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_ui_btn_status_list_value(list, 1, 1)
```

---

## get_ui_btn_status_n_list

method in GameAPI

- 描述

    生成n个值为v的UI_BTN_STATUS数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | integer | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_ui_btn_status_n_list(1, 1)
```

---

## get_ui_scrollview_type_list_value

method in GameAPI

- 描述

    获取UI_SCROLLVIEW_TYPE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_ui_scrollview_type_list_value(list, 1)
```

---

## set_ui_scrollview_type_list_value

method in GameAPI

- 描述

    设置UI_SCROLLVIEW_TYPE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | integer | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_ui_scrollview_type_list_value(list, 1, 1)
```

---

## get_ui_scrollview_type_n_list

method in GameAPI

- 描述

    生成n个值为v的UI_SCROLLVIEW_TYPE数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | integer | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_ui_scrollview_type_n_list(1, 1)
```

---

## set_unit_key_boolean_kv

method in GameAPI

- 描述

    预设库 添加BOOLEAN键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_boolean_kv(1, 1, "value")
```

---

## set_unit_key_integer_kv

method in GameAPI

- 描述

    预设库 添加INTEGER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_integer_kv(1, 1, "value")
```

---

## set_unit_key_float_kv

method in GameAPI

- 描述

    预设库 添加FLOAT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_float_kv(1, 1, "value")
```

---

## set_unit_key_string_kv

method in GameAPI

- 描述

    预设库 添加STRING键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_string_kv(1, 1, "value")
```

---

## set_unit_key_ui_comp_kv

method in GameAPI

- 描述

    预设库 添加UI_COMP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_ui_comp_kv(1, 1, "value")
```

---

## set_unit_key_ui_comp_type_kv

method in GameAPI

- 描述

    预设库 添加UI_COMP_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_ui_comp_type_kv(1, 1, "value")
```

---

## set_unit_key_ui_comp_event_type_kv

method in GameAPI

- 描述

    预设库 添加UI_COMP_EVENT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_ui_comp_event_type_kv(1, 1, "value")
```

---

## set_unit_key_ui_comp_attr_kv

method in GameAPI

- 描述

    预设库 添加UI_COMP_ATTR键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_ui_comp_attr_kv(1, 1, "value")
```

---

## set_unit_key_ui_comp_align_type_kv

method in GameAPI

- 描述

    预设库 添加UI_COMP_ALIGN_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_ui_comp_align_type_kv(1, 1, "value")
```

---

## set_unit_key_ui_prefab_kv

method in GameAPI

- 描述

    预设库 添加UI_PREFAB键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_ui_prefab_kv(1, 1, "value")
```

---

## set_unit_key_ui_prefab_instance_kv

method in GameAPI

- 描述

    预设库 添加UI_PREFAB_INSTANCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_ui_prefab_instance_kv(1, 1, "value")
```

---

## set_unit_key_ui_prefab_ins_uid_kv

method in GameAPI

- 描述

    预设库 添加UI_PREFAB_INS_UID键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_ui_prefab_ins_uid_kv(1, 1, "value")
```

---

## set_unit_key_ui_direction_kv

method in GameAPI

- 描述

    预设库 添加UI_DIRECTION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_ui_direction_kv(1, 1, "value")
```

---

## set_unit_key_ui_model_camera_mod_kv

method in GameAPI

- 描述

    预设库 添加UI_MODEL_CAMERA_MOD键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_ui_model_camera_mod_kv(1, 1, "value")
```

---

## set_unit_key_ui_btn_status_kv

method in GameAPI

- 描述

    预设库 添加UI_BTN_STATUS键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_ui_btn_status_kv(1, 1, "value")
```

---

## set_unit_key_ui_scrollview_type_kv

method in GameAPI

- 描述

    预设库 添加UI_SCROLLVIEW_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_ui_scrollview_type_kv(1, 1, "value")
```

---

## set_unit_key_ui_anim_kv

method in GameAPI

- 描述

    预设库 添加UI_ANIM键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_ui_anim_kv(1, 1, "value")
```

---

## set_unit_key_ui_anim_curve_kv

method in GameAPI

- 描述

    预设库 添加UI_ANIM_CURVE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_ui_anim_curve_kv(1, 1, "value")
```

---

## set_unit_key_audio_channel_kv

method in GameAPI

- 描述

    预设库 添加AUDIO_CHANNEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_audio_channel_kv(1, 1, "value")
```

---

## set_unit_key_unit_entity_kv

method in GameAPI

- 描述

    预设库 添加UNIT_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_unit_entity_kv(1, 1, "value")
```

---

## set_unit_key_unit_group_kv

method in GameAPI

- 描述

    预设库 添加UNIT_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_unit_group_kv(1, 1, "value")
```

---

## set_unit_key_unit_name_kv

method in GameAPI

- 描述

    预设库 添加UNIT_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_unit_name_kv(1, 1, "value")
```

---

## set_unit_key_unit_name_pool_kv

method in GameAPI

- 描述

    预设库 添加UNIT_NAME_POOL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_unit_name_pool_kv(1, 1, "value")
```

---

## set_unit_key_unit_write_attribute_kv

method in GameAPI

- 描述

    预设库 添加UNIT_WRITE_ATTRIBUTE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_unit_write_attribute_kv(1, 1, "value")
```

---

## set_unit_key_attr_element_kv

method in GameAPI

- 描述

    预设库 添加ATTR_ELEMENT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_attr_element_kv(1, 1, "value")
```

---

## set_unit_key_attr_element_read_kv

method in GameAPI

- 描述

    预设库 添加ATTR_ELEMENT_READ键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_attr_element_read_kv(1, 1, "value")
```

---

## set_unit_key_mover_entity_kv

method in GameAPI

- 描述

    预设库 添加MOVER_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_mover_entity_kv(1, 1, "value")
```

---

## set_unit_key_image_quality_kv

method in GameAPI

- 描述

    预设库 添加IMAGE_QUALITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_image_quality_kv(1, 1, "value")
```

---

## set_unit_key_window_type_setting_kv

method in GameAPI

- 描述

    预设库 添加WINDOW_TYPE_SETTING键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_window_type_setting_kv(1, 1, "value")
```

---

## set_unit_key_item_entity_kv

method in GameAPI

- 描述

    预设库 添加ITEM_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_item_entity_kv(1, 1, "value")
```

---

## set_unit_key_item_group_kv

method in GameAPI

- 描述

    预设库 添加ITEM_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_item_group_kv(1, 1, "value")
```

---

## set_unit_key_item_name_kv

method in GameAPI

- 描述

    预设库 添加ITEM_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_item_name_kv(1, 1, "value")
```

---

## set_unit_key_ability_kv

method in GameAPI

- 描述

    预设库 添加ABILITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_ability_kv(1, 1, "value")
```

---

## set_unit_key_ability_type_kv

method in GameAPI

- 描述

    预设库 添加ABILITY_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_ability_type_kv(1, 1, "value")
```

---

## set_unit_key_ability_cast_type_kv

method in GameAPI

- 描述

    预设库 添加ABILITY_CAST_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_ability_cast_type_kv(1, 1, "value")
```

---

## set_unit_key_ability_name_kv

method in GameAPI

- 描述

    预设库 添加ABILITY_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_ability_name_kv(1, 1, "value")
```

---

## set_unit_key_skill_pointer_type_kv

method in GameAPI

- 描述

    预设库 添加SKILL_POINTER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_skill_pointer_type_kv(1, 1, "value")
```

---

## set_unit_key_modifier_entity_kv

method in GameAPI

- 描述

    预设库 添加MODIFIER_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_modifier_entity_kv(1, 1, "value")
```

---

## set_unit_key_modifier_type_kv

method in GameAPI

- 描述

    预设库 添加MODIFIER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_modifier_type_kv(1, 1, "value")
```

---

## set_unit_key_modifier_effect_type_kv

method in GameAPI

- 描述

    预设库 添加MODIFIER_EFFECT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_modifier_effect_type_kv(1, 1, "value")
```

---

## set_unit_key_modifier_kv

method in GameAPI

- 描述

    预设库 添加MODIFIER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_modifier_kv(1, 1, "value")
```

---

## set_unit_key_projectile_kv

method in GameAPI

- 描述

    预设库 添加PROJECTILE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_projectile_kv(1, 1, "value")
```

---

## set_unit_key_projectile_entity_kv

method in GameAPI

- 描述

    预设库 添加PROJECTILE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_projectile_entity_kv(1, 1, "value")
```

---

## set_unit_key_projectile_group_kv

method in GameAPI

- 描述

    预设库 添加PROJECTILE_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_projectile_group_kv(1, 1, "value")
```

---

## set_unit_key_destructible_entity_kv

method in GameAPI

- 描述

    预设库 添加DESTRUCTIBLE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_destructible_entity_kv(1, 1, "value")
```

---

## set_unit_key_destructible_name_kv

method in GameAPI

- 描述

    预设库 添加DESTRUCTIBLE_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_destructible_name_kv(1, 1, "value")
```

---

## set_unit_key_sound_entity_kv

method in GameAPI

- 描述

    预设库 添加SOUND_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_sound_entity_kv(1, 1, "value")
```

---

## set_unit_key_audio_key_kv

method in GameAPI

- 描述

    预设库 添加AUDIO_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_audio_key_kv(1, 1, "value")
```

---

## set_unit_key_game_mode_kv

method in GameAPI

- 描述

    预设库 添加GAME_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_game_mode_kv(1, 1, "value")
```

---

## set_unit_key_player_kv

method in GameAPI

- 描述

    预设库 添加PLAYER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_player_kv(1, 1, "value")
```

---

## set_unit_key_player_group_kv

method in GameAPI

- 描述

    预设库 添加PLAYER_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_player_group_kv(1, 1, "value")
```

---

## set_unit_key_role_res_key_kv

method in GameAPI

- 描述

    预设库 添加ROLE_RES_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_role_res_key_kv(1, 1, "value")
```

---

## set_unit_key_role_status_kv

method in GameAPI

- 描述

    预设库 添加ROLE_STATUS键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_role_status_kv(1, 1, "value")
```

---

## set_unit_key_role_type_kv

method in GameAPI

- 描述

    预设库 添加ROLE_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_role_type_kv(1, 1, "value")
```

---

## set_unit_key_role_relation_kv

method in GameAPI

- 描述

    预设库 添加ROLE_RELATION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_role_relation_kv(1, 1, "value")
```

---

## set_unit_key_team_kv

method in GameAPI

- 描述

    预设库 添加TEAM键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_team_kv(1, 1, "value")
```

---

## set_unit_key_point_kv

method in GameAPI

- 描述

    预设库 添加POINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_point_kv(1, 1, "value")
```

---

## set_unit_key_vector3_kv

method in GameAPI

- 描述

    预设库 添加VECTOR3键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_vector3_kv(1, 1, "value")
```

---

## set_unit_key_rotation_kv

method in GameAPI

- 描述

    预设库 添加ROTATION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_rotation_kv(1, 1, "value")
```

---

## set_unit_key_point_list_kv

method in GameAPI

- 描述

    预设库 添加POINT_LIST键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_point_list_kv(1, 1, "value")
```

---

## set_unit_key_rectangle_kv

method in GameAPI

- 描述

    预设库 添加RECTANGLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_rectangle_kv(1, 1, "value")
```

---

## set_unit_key_round_area_kv

method in GameAPI

- 描述

    预设库 添加ROUND_AREA键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_round_area_kv(1, 1, "value")
```

---

## set_unit_key_polygon_kv

method in GameAPI

- 描述

    预设库 添加POLYGON键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_polygon_kv(1, 1, "value")
```

---

## set_unit_key_camera_kv

method in GameAPI

- 描述

    预设库 添加CAMERA键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_camera_kv(1, 1, "value")
```

---

## set_unit_key_camline_kv

method in GameAPI

- 描述

    预设库 添加CAMLINE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_camline_kv(1, 1, "value")
```

---

## set_unit_key_point_light_kv

method in GameAPI

- 描述

    预设库 添加POINT_LIGHT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_point_light_kv(1, 1, "value")
```

---

## set_unit_key_spot_light_kv

method in GameAPI

- 描述

    预设库 添加SPOT_LIGHT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_spot_light_kv(1, 1, "value")
```

---

## set_unit_key_fog_kv

method in GameAPI

- 描述

    预设库 添加FOG键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_fog_kv(1, 1, "value")
```

---

## set_unit_key_scene_sound_kv

method in GameAPI

- 描述

    预设库 添加SCENE_SOUND键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_scene_sound_kv(1, 1, "value")
```

---

## set_unit_key_model_kv

method in GameAPI

- 描述

    预设库 添加MODEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_model_kv(1, 1, "value")
```

---

## set_unit_key_sfx_entity_kv

method in GameAPI

- 描述

    预设库 添加SFX_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_sfx_entity_kv(1, 1, "value")
```

---

## set_unit_key_sfx_key_kv

method in GameAPI

- 描述

    预设库 添加SFX_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_sfx_key_kv(1, 1, "value")
```

---

## set_unit_key_link_sfx_entity_kv

method in GameAPI

- 描述

    预设库 添加LINK_SFX_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_link_sfx_entity_kv(1, 1, "value")
```

---

## set_unit_key_link_sfx_key_kv

method in GameAPI

- 描述

    预设库 添加LINK_SFX_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_link_sfx_key_kv(1, 1, "value")
```

---

## set_unit_key_cursor_key_kv

method in GameAPI

- 描述

    预设库 添加CURSOR_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_cursor_key_kv(1, 1, "value")
```

---

## set_unit_key_angle_kv

method in GameAPI

- 描述

    预设库 添加ANGLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_angle_kv(1, 1, "value")
```

---

## set_unit_key_texture_kv

method in GameAPI

- 描述

    预设库 添加TEXTURE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_texture_kv(1, 1, "value")
```

---

## set_unit_key_sequence_kv

method in GameAPI

- 描述

    预设库 添加SEQUENCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_sequence_kv(1, 1, "value")
```

---

## set_unit_key_physics_object_kv

method in GameAPI

- 描述

    预设库 添加PHYSICS_OBJECT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_physics_object_kv(1, 1, "value")
```

---

## set_unit_key_physics_entity_kv

method in GameAPI

- 描述

    预设库 添加PHYSICS_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_physics_entity_kv(1, 1, "value")
```

---

## set_unit_key_physics_object_key_kv

method in GameAPI

- 描述

    预设库 添加PHYSICS_OBJECT_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_physics_object_key_kv(1, 1, "value")
```

---

## set_unit_key_physics_entity_key_kv

method in GameAPI

- 描述

    预设库 添加PHYSICS_ENTITY_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_physics_entity_key_kv(1, 1, "value")
```

---

## set_unit_key_rigid_body_kv

method in GameAPI

- 描述

    预设库 添加RIGID_BODY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_rigid_body_kv(1, 1, "value")
```

---

## set_unit_key_rigid_body_group_kv

method in GameAPI

- 描述

    预设库 添加RIGID_BODY_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_rigid_body_group_kv(1, 1, "value")
```

---

## set_unit_key_collider_kv

method in GameAPI

- 描述

    预设库 添加COLLIDER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_collider_kv(1, 1, "value")
```

---

## set_unit_key_joint_kv

method in GameAPI

- 描述

    预设库 添加JOINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_joint_kv(1, 1, "value")
```

---

## set_unit_key_reaction_kv

method in GameAPI

- 描述

    预设库 添加REACTION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_reaction_kv(1, 1, "value")
```

---

## set_unit_key_reaction_group_kv

method in GameAPI

- 描述

    预设库 添加REACTION_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_reaction_group_kv(1, 1, "value")
```

---

## set_unit_key_dynamic_trigger_instance_kv

method in GameAPI

- 描述

    预设库 添加DYNAMIC_TRIGGER_INSTANCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_dynamic_trigger_instance_kv(1, 1, "value")
```

---

## set_unit_key_table_kv

method in GameAPI

- 描述

    预设库 添加TABLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_table_kv(1, 1, "value")
```

---

## set_unit_key_random_pool_kv

method in GameAPI

- 描述

    预设库 添加RANDOM_POOL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_random_pool_kv(1, 1, "value")
```

---

## set_unit_key_scene_ui_kv

method in GameAPI

- 描述

    预设库 添加SCENE_UI键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_scene_ui_kv(1, 1, "value")
```

---

## set_unit_key_damage_type_kv

method in GameAPI

- 描述

    预设库 添加DAMAGE_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_damage_type_kv(1, 1, "value")
```

---

## set_unit_key_harm_text_type_new_kv

method in GameAPI

- 描述

    预设库 添加HARM_TEXT_TYPE_NEW键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_harm_text_type_new_kv(1, 1, "value")
```

---

## set_unit_key_font_type_kv

method in GameAPI

- 描述

    预设库 添加FONT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_font_type_kv(1, 1, "value")
```

---

## set_unit_key_jump_word_track_kv

method in GameAPI

- 描述

    预设库 添加JUMP_WORD_TRACK键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_jump_word_track_kv(1, 1, "value")
```

---

## set_unit_key_new_timer_kv

method in GameAPI

- 描述

    预设库 添加NEW_TIMER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_new_timer_kv(1, 1, "value")
```

---

## set_unit_key_tech_key_kv

method in GameAPI

- 描述

    预设库 添加TECH_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_tech_key_kv(1, 1, "value")
```

---

## set_unit_key_store_key_kv

method in GameAPI

- 描述

    预设库 添加STORE_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_store_key_kv(1, 1, "value")
```

---

## set_unit_key_keyboard_key_kv

method in GameAPI

- 描述

    预设库 添加KEYBOARD_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_keyboard_key_kv(1, 1, "value")
```

---

## set_unit_key_func_keyboard_key_kv

method in GameAPI

- 描述

    预设库 添加FUNC_KEYBOARD_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_func_keyboard_key_kv(1, 1, "value")
```

---

## set_unit_key_mouse_key_kv

method in GameAPI

- 描述

    预设库 添加MOUSE_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_mouse_key_kv(1, 1, "value")
```

---

## set_unit_key_mouse_wheel_kv

method in GameAPI

- 描述

    预设库 添加MOUSE_WHEEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_mouse_wheel_kv(1, 1, "value")
```

---

## set_unit_key_post_effect_kv

method in GameAPI

- 描述

    预设库 添加POST_EFFECT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_post_effect_kv(1, 1, "value")
```

---

## set_unit_key_unit_type_kv

method in GameAPI

- 描述

    预设库 添加UNIT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_unit_type_kv(1, 1, "value")
```

---

## set_unit_key_unit_command_type_kv

method in GameAPI

- 描述

    预设库 添加UNIT_COMMAND_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_unit_command_type_kv(1, 1, "value")
```

---

## set_unit_key_mini_map_color_type_kv

method in GameAPI

- 描述

    预设库 添加MINI_MAP_COLOR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_mini_map_color_type_kv(1, 1, "value")
```

---

## set_unit_key_unit_behavior_kv

method in GameAPI

- 描述

    预设库 添加UNIT_BEHAVIOR键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_unit_behavior_kv(1, 1, "value")
```

---

## set_unit_key_curved_path_kv

method in GameAPI

- 描述

    预设库 添加CURVED_PATH键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_curved_path_kv(1, 1, "value")
```

---

## set_unit_key_curved_path_3d_kv

method in GameAPI

- 描述

    预设库 添加CURVED_PATH_3D键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_curved_path_3d_kv(1, 1, "value")
```

---

## set_item_key_boolean_kv

method in GameAPI

- 描述

    预设库 添加BOOLEAN键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_boolean_kv(1, 1, "value")
```

---

## set_item_key_integer_kv

method in GameAPI

- 描述

    预设库 添加INTEGER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_integer_kv(1, 1, "value")
```

---

## set_item_key_float_kv

method in GameAPI

- 描述

    预设库 添加FLOAT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_float_kv(1, 1, "value")
```

---

## set_item_key_string_kv

method in GameAPI

- 描述

    预设库 添加STRING键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_string_kv(1, 1, "value")
```

---

## set_item_key_ui_comp_kv

method in GameAPI

- 描述

    预设库 添加UI_COMP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_ui_comp_kv(1, 1, "value")
```

---

## set_item_key_ui_comp_type_kv

method in GameAPI

- 描述

    预设库 添加UI_COMP_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_ui_comp_type_kv(1, 1, "value")
```

---

## set_item_key_ui_comp_event_type_kv

method in GameAPI

- 描述

    预设库 添加UI_COMP_EVENT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_ui_comp_event_type_kv(1, 1, "value")
```

---

## set_item_key_ui_comp_attr_kv

method in GameAPI

- 描述

    预设库 添加UI_COMP_ATTR键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_ui_comp_attr_kv(1, 1, "value")
```

---

## set_item_key_ui_comp_align_type_kv

method in GameAPI

- 描述

    预设库 添加UI_COMP_ALIGN_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_ui_comp_align_type_kv(1, 1, "value")
```

---

## set_item_key_ui_prefab_kv

method in GameAPI

- 描述

    预设库 添加UI_PREFAB键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_ui_prefab_kv(1, 1, "value")
```

---

## set_item_key_ui_prefab_instance_kv

method in GameAPI

- 描述

    预设库 添加UI_PREFAB_INSTANCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_ui_prefab_instance_kv(1, 1, "value")
```

---

## set_item_key_ui_prefab_ins_uid_kv

method in GameAPI

- 描述

    预设库 添加UI_PREFAB_INS_UID键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_ui_prefab_ins_uid_kv(1, 1, "value")
```

---

## set_item_key_ui_direction_kv

method in GameAPI

- 描述

    预设库 添加UI_DIRECTION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_ui_direction_kv(1, 1, "value")
```

---

## set_item_key_ui_model_camera_mod_kv

method in GameAPI

- 描述

    预设库 添加UI_MODEL_CAMERA_MOD键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_ui_model_camera_mod_kv(1, 1, "value")
```

---

## set_item_key_ui_btn_status_kv

method in GameAPI

- 描述

    预设库 添加UI_BTN_STATUS键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_ui_btn_status_kv(1, 1, "value")
```

---

## set_item_key_ui_scrollview_type_kv

method in GameAPI

- 描述

    预设库 添加UI_SCROLLVIEW_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_ui_scrollview_type_kv(1, 1, "value")
```

---

## set_item_key_ui_anim_kv

method in GameAPI

- 描述

    预设库 添加UI_ANIM键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_ui_anim_kv(1, 1, "value")
```

---

## set_item_key_ui_anim_curve_kv

method in GameAPI

- 描述

    预设库 添加UI_ANIM_CURVE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_ui_anim_curve_kv(1, 1, "value")
```

---

## set_item_key_audio_channel_kv

method in GameAPI

- 描述

    预设库 添加AUDIO_CHANNEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_audio_channel_kv(1, 1, "value")
```

---

## set_item_key_unit_entity_kv

method in GameAPI

- 描述

    预设库 添加UNIT_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_unit_entity_kv(1, 1, "value")
```

---

## set_item_key_unit_group_kv

method in GameAPI

- 描述

    预设库 添加UNIT_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_unit_group_kv(1, 1, "value")
```

---

## set_item_key_unit_name_kv

method in GameAPI

- 描述

    预设库 添加UNIT_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_unit_name_kv(1, 1, "value")
```

---

## set_item_key_unit_name_pool_kv

method in GameAPI

- 描述

    预设库 添加UNIT_NAME_POOL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_unit_name_pool_kv(1, 1, "value")
```

---

## set_item_key_unit_write_attribute_kv

method in GameAPI

- 描述

    预设库 添加UNIT_WRITE_ATTRIBUTE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_unit_write_attribute_kv(1, 1, "value")
```

---

## set_item_key_attr_element_kv

method in GameAPI

- 描述

    预设库 添加ATTR_ELEMENT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_attr_element_kv(1, 1, "value")
```

---

## set_item_key_attr_element_read_kv

method in GameAPI

- 描述

    预设库 添加ATTR_ELEMENT_READ键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_attr_element_read_kv(1, 1, "value")
```

---

## set_item_key_mover_entity_kv

method in GameAPI

- 描述

    预设库 添加MOVER_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_mover_entity_kv(1, 1, "value")
```

---

## set_item_key_image_quality_kv

method in GameAPI

- 描述

    预设库 添加IMAGE_QUALITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_image_quality_kv(1, 1, "value")
```

---

## set_item_key_window_type_setting_kv

method in GameAPI

- 描述

    预设库 添加WINDOW_TYPE_SETTING键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_window_type_setting_kv(1, 1, "value")
```

---

## set_item_key_item_entity_kv

method in GameAPI

- 描述

    预设库 添加ITEM_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_item_entity_kv(1, 1, "value")
```

---

## set_item_key_item_group_kv

method in GameAPI

- 描述

    预设库 添加ITEM_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_item_group_kv(1, 1, "value")
```

---

## set_item_key_item_name_kv

method in GameAPI

- 描述

    预设库 添加ITEM_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_item_name_kv(1, 1, "value")
```

---

## set_item_key_ability_kv

method in GameAPI

- 描述

    预设库 添加ABILITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_ability_kv(1, 1, "value")
```

---

## set_item_key_ability_type_kv

method in GameAPI

- 描述

    预设库 添加ABILITY_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_ability_type_kv(1, 1, "value")
```

---

## set_item_key_ability_cast_type_kv

method in GameAPI

- 描述

    预设库 添加ABILITY_CAST_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_ability_cast_type_kv(1, 1, "value")
```

---

## set_item_key_ability_name_kv

method in GameAPI

- 描述

    预设库 添加ABILITY_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_ability_name_kv(1, 1, "value")
```

---

## set_item_key_skill_pointer_type_kv

method in GameAPI

- 描述

    预设库 添加SKILL_POINTER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_skill_pointer_type_kv(1, 1, "value")
```

---

## set_item_key_modifier_entity_kv

method in GameAPI

- 描述

    预设库 添加MODIFIER_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_modifier_entity_kv(1, 1, "value")
```

---

## set_item_key_modifier_type_kv

method in GameAPI

- 描述

    预设库 添加MODIFIER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_modifier_type_kv(1, 1, "value")
```

---

## set_item_key_modifier_effect_type_kv

method in GameAPI

- 描述

    预设库 添加MODIFIER_EFFECT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_modifier_effect_type_kv(1, 1, "value")
```

---

## set_item_key_modifier_kv

method in GameAPI

- 描述

    预设库 添加MODIFIER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_modifier_kv(1, 1, "value")
```

---

## set_item_key_projectile_kv

method in GameAPI

- 描述

    预设库 添加PROJECTILE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_projectile_kv(1, 1, "value")
```

---

## set_item_key_projectile_entity_kv

method in GameAPI

- 描述

    预设库 添加PROJECTILE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_projectile_entity_kv(1, 1, "value")
```

---

## set_item_key_projectile_group_kv

method in GameAPI

- 描述

    预设库 添加PROJECTILE_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_projectile_group_kv(1, 1, "value")
```

---

## set_item_key_destructible_entity_kv

method in GameAPI

- 描述

    预设库 添加DESTRUCTIBLE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_destructible_entity_kv(1, 1, "value")
```

---

## set_item_key_destructible_name_kv

method in GameAPI

- 描述

    预设库 添加DESTRUCTIBLE_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_destructible_name_kv(1, 1, "value")
```

---

## set_item_key_sound_entity_kv

method in GameAPI

- 描述

    预设库 添加SOUND_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_sound_entity_kv(1, 1, "value")
```

---

## set_item_key_audio_key_kv

method in GameAPI

- 描述

    预设库 添加AUDIO_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_audio_key_kv(1, 1, "value")
```

---

## set_item_key_game_mode_kv

method in GameAPI

- 描述

    预设库 添加GAME_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_game_mode_kv(1, 1, "value")
```

---

## set_item_key_player_kv

method in GameAPI

- 描述

    预设库 添加PLAYER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_player_kv(1, 1, "value")
```

---

## set_item_key_player_group_kv

method in GameAPI

- 描述

    预设库 添加PLAYER_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_player_group_kv(1, 1, "value")
```

---

## set_item_key_role_res_key_kv

method in GameAPI

- 描述

    预设库 添加ROLE_RES_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_role_res_key_kv(1, 1, "value")
```

---

## set_item_key_role_status_kv

method in GameAPI

- 描述

    预设库 添加ROLE_STATUS键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_role_status_kv(1, 1, "value")
```

---

## set_item_key_role_type_kv

method in GameAPI

- 描述

    预设库 添加ROLE_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_role_type_kv(1, 1, "value")
```

---

## set_item_key_role_relation_kv

method in GameAPI

- 描述

    预设库 添加ROLE_RELATION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_role_relation_kv(1, 1, "value")
```

---

## set_item_key_team_kv

method in GameAPI

- 描述

    预设库 添加TEAM键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_team_kv(1, 1, "value")
```

---

## set_item_key_point_kv

method in GameAPI

- 描述

    预设库 添加POINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_point_kv(1, 1, "value")
```

---

## set_item_key_vector3_kv

method in GameAPI

- 描述

    预设库 添加VECTOR3键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_vector3_kv(1, 1, "value")
```

---

## set_item_key_rotation_kv

method in GameAPI

- 描述

    预设库 添加ROTATION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_rotation_kv(1, 1, "value")
```

---

## set_item_key_point_list_kv

method in GameAPI

- 描述

    预设库 添加POINT_LIST键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_point_list_kv(1, 1, "value")
```

---

## set_item_key_rectangle_kv

method in GameAPI

- 描述

    预设库 添加RECTANGLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_rectangle_kv(1, 1, "value")
```

---

## set_item_key_round_area_kv

method in GameAPI

- 描述

    预设库 添加ROUND_AREA键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_round_area_kv(1, 1, "value")
```

---

## set_item_key_polygon_kv

method in GameAPI

- 描述

    预设库 添加POLYGON键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_polygon_kv(1, 1, "value")
```

---

## set_item_key_camera_kv

method in GameAPI

- 描述

    预设库 添加CAMERA键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_camera_kv(1, 1, "value")
```

---

## set_item_key_camline_kv

method in GameAPI

- 描述

    预设库 添加CAMLINE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_camline_kv(1, 1, "value")
```

---

## set_item_key_point_light_kv

method in GameAPI

- 描述

    预设库 添加POINT_LIGHT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_point_light_kv(1, 1, "value")
```

---

## set_item_key_spot_light_kv

method in GameAPI

- 描述

    预设库 添加SPOT_LIGHT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_spot_light_kv(1, 1, "value")
```

---

## set_item_key_fog_kv

method in GameAPI

- 描述

    预设库 添加FOG键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_fog_kv(1, 1, "value")
```

---

## set_item_key_scene_sound_kv

method in GameAPI

- 描述

    预设库 添加SCENE_SOUND键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_scene_sound_kv(1, 1, "value")
```

---

## set_item_key_model_kv

method in GameAPI

- 描述

    预设库 添加MODEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_model_kv(1, 1, "value")
```

---

## set_item_key_sfx_entity_kv

method in GameAPI

- 描述

    预设库 添加SFX_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_sfx_entity_kv(1, 1, "value")
```

---

## set_item_key_sfx_key_kv

method in GameAPI

- 描述

    预设库 添加SFX_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_sfx_key_kv(1, 1, "value")
```

---

## set_item_key_link_sfx_entity_kv

method in GameAPI

- 描述

    预设库 添加LINK_SFX_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_link_sfx_entity_kv(1, 1, "value")
```

---

## set_item_key_link_sfx_key_kv

method in GameAPI

- 描述

    预设库 添加LINK_SFX_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_link_sfx_key_kv(1, 1, "value")
```

---

## set_item_key_cursor_key_kv

method in GameAPI

- 描述

    预设库 添加CURSOR_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_cursor_key_kv(1, 1, "value")
```

---

## set_item_key_angle_kv

method in GameAPI

- 描述

    预设库 添加ANGLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_angle_kv(1, 1, "value")
```

---

## set_item_key_texture_kv

method in GameAPI

- 描述

    预设库 添加TEXTURE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_texture_kv(1, 1, "value")
```

---

## set_item_key_sequence_kv

method in GameAPI

- 描述

    预设库 添加SEQUENCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_sequence_kv(1, 1, "value")
```

---

## set_item_key_physics_object_kv

method in GameAPI

- 描述

    预设库 添加PHYSICS_OBJECT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_physics_object_kv(1, 1, "value")
```

---

## set_item_key_physics_entity_kv

method in GameAPI

- 描述

    预设库 添加PHYSICS_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_physics_entity_kv(1, 1, "value")
```

---

## set_item_key_physics_object_key_kv

method in GameAPI

- 描述

    预设库 添加PHYSICS_OBJECT_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_physics_object_key_kv(1, 1, "value")
```

---

## set_item_key_physics_entity_key_kv

method in GameAPI

- 描述

    预设库 添加PHYSICS_ENTITY_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_physics_entity_key_kv(1, 1, "value")
```

---

## set_item_key_rigid_body_kv

method in GameAPI

- 描述

    预设库 添加RIGID_BODY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_rigid_body_kv(1, 1, "value")
```

---

## set_item_key_rigid_body_group_kv

method in GameAPI

- 描述

    预设库 添加RIGID_BODY_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_rigid_body_group_kv(1, 1, "value")
```

---

## set_item_key_collider_kv

method in GameAPI

- 描述

    预设库 添加COLLIDER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_collider_kv(1, 1, "value")
```

---

## set_item_key_joint_kv

method in GameAPI

- 描述

    预设库 添加JOINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_joint_kv(1, 1, "value")
```

---

## set_item_key_reaction_kv

method in GameAPI

- 描述

    预设库 添加REACTION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_reaction_kv(1, 1, "value")
```

---

## set_item_key_reaction_group_kv

method in GameAPI

- 描述

    预设库 添加REACTION_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_reaction_group_kv(1, 1, "value")
```

---

## set_item_key_dynamic_trigger_instance_kv

method in GameAPI

- 描述

    预设库 添加DYNAMIC_TRIGGER_INSTANCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_dynamic_trigger_instance_kv(1, 1, "value")
```

---

## set_item_key_table_kv

method in GameAPI

- 描述

    预设库 添加TABLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_table_kv(1, 1, "value")
```

---

## set_item_key_random_pool_kv

method in GameAPI

- 描述

    预设库 添加RANDOM_POOL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_random_pool_kv(1, 1, "value")
```

---

## set_item_key_scene_ui_kv

method in GameAPI

- 描述

    预设库 添加SCENE_UI键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_scene_ui_kv(1, 1, "value")
```

---

## set_item_key_damage_type_kv

method in GameAPI

- 描述

    预设库 添加DAMAGE_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_damage_type_kv(1, 1, "value")
```

---

## set_item_key_harm_text_type_new_kv

method in GameAPI

- 描述

    预设库 添加HARM_TEXT_TYPE_NEW键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_harm_text_type_new_kv(1, 1, "value")
```

---

## set_item_key_font_type_kv

method in GameAPI

- 描述

    预设库 添加FONT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_font_type_kv(1, 1, "value")
```

---

## set_item_key_jump_word_track_kv

method in GameAPI

- 描述

    预设库 添加JUMP_WORD_TRACK键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_jump_word_track_kv(1, 1, "value")
```

---

## set_item_key_new_timer_kv

method in GameAPI

- 描述

    预设库 添加NEW_TIMER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_new_timer_kv(1, 1, "value")
```

---

## set_item_key_tech_key_kv

method in GameAPI

- 描述

    预设库 添加TECH_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_tech_key_kv(1, 1, "value")
```

---

## set_item_key_store_key_kv

method in GameAPI

- 描述

    预设库 添加STORE_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_store_key_kv(1, 1, "value")
```

---

## set_item_key_keyboard_key_kv

method in GameAPI

- 描述

    预设库 添加KEYBOARD_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_keyboard_key_kv(1, 1, "value")
```

---

## set_item_key_func_keyboard_key_kv

method in GameAPI

- 描述

    预设库 添加FUNC_KEYBOARD_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_func_keyboard_key_kv(1, 1, "value")
```

---

## set_item_key_mouse_key_kv

method in GameAPI

- 描述

    预设库 添加MOUSE_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_mouse_key_kv(1, 1, "value")
```

---

## set_item_key_mouse_wheel_kv

method in GameAPI

- 描述

    预设库 添加MOUSE_WHEEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_mouse_wheel_kv(1, 1, "value")
```

---

## set_item_key_post_effect_kv

method in GameAPI

- 描述

    预设库 添加POST_EFFECT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_post_effect_kv(1, 1, "value")
```

---

## set_item_key_unit_type_kv

method in GameAPI

- 描述

    预设库 添加UNIT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_unit_type_kv(1, 1, "value")
```

---

## set_item_key_unit_command_type_kv

method in GameAPI

- 描述

    预设库 添加UNIT_COMMAND_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_unit_command_type_kv(1, 1, "value")
```

---

## set_item_key_mini_map_color_type_kv

method in GameAPI

- 描述

    预设库 添加MINI_MAP_COLOR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_mini_map_color_type_kv(1, 1, "value")
```

---

## set_item_key_unit_behavior_kv

method in GameAPI

- 描述

    预设库 添加UNIT_BEHAVIOR键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_unit_behavior_kv(1, 1, "value")
```

---

## set_item_key_curved_path_kv

method in GameAPI

- 描述

    预设库 添加CURVED_PATH键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_curved_path_kv(1, 1, "value")
```

---

## set_item_key_curved_path_3d_kv

method in GameAPI

- 描述

    预设库 添加CURVED_PATH_3D键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_curved_path_3d_kv(1, 1, "value")
```

---

## set_ability_key_boolean_kv

method in GameAPI

- 描述

    预设库 添加BOOLEAN键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_boolean_kv(1, 1, "value")
```

---

## set_ability_key_integer_kv

method in GameAPI

- 描述

    预设库 添加INTEGER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_integer_kv(1, 1, "value")
```

---

## set_ability_key_float_kv

method in GameAPI

- 描述

    预设库 添加FLOAT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_float_kv(1, 1, "value")
```

---

## set_ability_key_string_kv

method in GameAPI

- 描述

    预设库 添加STRING键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_string_kv(1, 1, "value")
```

---

## set_ability_key_ui_comp_kv

method in GameAPI

- 描述

    预设库 添加UI_COMP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_ui_comp_kv(1, 1, "value")
```

---

## set_ability_key_ui_comp_type_kv

method in GameAPI

- 描述

    预设库 添加UI_COMP_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_ui_comp_type_kv(1, 1, "value")
```

---

## set_ability_key_ui_comp_event_type_kv

method in GameAPI

- 描述

    预设库 添加UI_COMP_EVENT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_ui_comp_event_type_kv(1, 1, "value")
```

---

## set_ability_key_ui_comp_attr_kv

method in GameAPI

- 描述

    预设库 添加UI_COMP_ATTR键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_ui_comp_attr_kv(1, 1, "value")
```

---

## set_ability_key_ui_comp_align_type_kv

method in GameAPI

- 描述

    预设库 添加UI_COMP_ALIGN_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_ui_comp_align_type_kv(1, 1, "value")
```

---

## set_ability_key_ui_prefab_kv

method in GameAPI

- 描述

    预设库 添加UI_PREFAB键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_ui_prefab_kv(1, 1, "value")
```

---

## set_ability_key_ui_prefab_instance_kv

method in GameAPI

- 描述

    预设库 添加UI_PREFAB_INSTANCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_ui_prefab_instance_kv(1, 1, "value")
```

---

## set_ability_key_ui_prefab_ins_uid_kv

method in GameAPI

- 描述

    预设库 添加UI_PREFAB_INS_UID键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_ui_prefab_ins_uid_kv(1, 1, "value")
```

---

## set_ability_key_ui_direction_kv

method in GameAPI

- 描述

    预设库 添加UI_DIRECTION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_ui_direction_kv(1, 1, "value")
```

---

## set_ability_key_ui_model_camera_mod_kv

method in GameAPI

- 描述

    预设库 添加UI_MODEL_CAMERA_MOD键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_ui_model_camera_mod_kv(1, 1, "value")
```

---

## set_ability_key_ui_btn_status_kv

method in GameAPI

- 描述

    预设库 添加UI_BTN_STATUS键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_ui_btn_status_kv(1, 1, "value")
```

---

## set_ability_key_ui_scrollview_type_kv

method in GameAPI

- 描述

    预设库 添加UI_SCROLLVIEW_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_ui_scrollview_type_kv(1, 1, "value")
```

---

## set_ability_key_ui_anim_kv

method in GameAPI

- 描述

    预设库 添加UI_ANIM键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_ui_anim_kv(1, 1, "value")
```

---

## set_ability_key_ui_anim_curve_kv

method in GameAPI

- 描述

    预设库 添加UI_ANIM_CURVE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_ui_anim_curve_kv(1, 1, "value")
```

---

## set_ability_key_audio_channel_kv

method in GameAPI

- 描述

    预设库 添加AUDIO_CHANNEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_audio_channel_kv(1, 1, "value")
```

---

## set_ability_key_unit_entity_kv

method in GameAPI

- 描述

    预设库 添加UNIT_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_unit_entity_kv(1, 1, "value")
```

---

## set_ability_key_unit_group_kv

method in GameAPI

- 描述

    预设库 添加UNIT_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_unit_group_kv(1, 1, "value")
```

---

## set_ability_key_unit_name_kv

method in GameAPI

- 描述

    预设库 添加UNIT_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_unit_name_kv(1, 1, "value")
```

---

## set_ability_key_unit_name_pool_kv

method in GameAPI

- 描述

    预设库 添加UNIT_NAME_POOL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_unit_name_pool_kv(1, 1, "value")
```

---

## set_ability_key_unit_write_attribute_kv

method in GameAPI

- 描述

    预设库 添加UNIT_WRITE_ATTRIBUTE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_unit_write_attribute_kv(1, 1, "value")
```

---

## set_ability_key_attr_element_kv

method in GameAPI

- 描述

    预设库 添加ATTR_ELEMENT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_attr_element_kv(1, 1, "value")
```

---

## set_ability_key_attr_element_read_kv

method in GameAPI

- 描述

    预设库 添加ATTR_ELEMENT_READ键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_attr_element_read_kv(1, 1, "value")
```

---

## set_ability_key_mover_entity_kv

method in GameAPI

- 描述

    预设库 添加MOVER_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_mover_entity_kv(1, 1, "value")
```

---

## set_ability_key_image_quality_kv

method in GameAPI

- 描述

    预设库 添加IMAGE_QUALITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_image_quality_kv(1, 1, "value")
```

---

## set_ability_key_window_type_setting_kv

method in GameAPI

- 描述

    预设库 添加WINDOW_TYPE_SETTING键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_window_type_setting_kv(1, 1, "value")
```

---

## set_ability_key_item_entity_kv

method in GameAPI

- 描述

    预设库 添加ITEM_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_item_entity_kv(1, 1, "value")
```

---

## set_ability_key_item_group_kv

method in GameAPI

- 描述

    预设库 添加ITEM_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_item_group_kv(1, 1, "value")
```

---

## set_ability_key_item_name_kv

method in GameAPI

- 描述

    预设库 添加ITEM_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_item_name_kv(1, 1, "value")
```

---

## set_ability_key_ability_kv

method in GameAPI

- 描述

    预设库 添加ABILITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_ability_kv(1, 1, "value")
```

---

## set_ability_key_ability_type_kv

method in GameAPI

- 描述

    预设库 添加ABILITY_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_ability_type_kv(1, 1, "value")
```

---

## set_ability_key_ability_cast_type_kv

method in GameAPI

- 描述

    预设库 添加ABILITY_CAST_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_ability_cast_type_kv(1, 1, "value")
```

---

## set_ability_key_ability_name_kv

method in GameAPI

- 描述

    预设库 添加ABILITY_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_ability_name_kv(1, 1, "value")
```

---

## set_ability_key_skill_pointer_type_kv

method in GameAPI

- 描述

    预设库 添加SKILL_POINTER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_skill_pointer_type_kv(1, 1, "value")
```

---

## set_ability_key_modifier_entity_kv

method in GameAPI

- 描述

    预设库 添加MODIFIER_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_modifier_entity_kv(1, 1, "value")
```

---

## set_ability_key_modifier_type_kv

method in GameAPI

- 描述

    预设库 添加MODIFIER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_modifier_type_kv(1, 1, "value")
```

---

## set_ability_key_modifier_effect_type_kv

method in GameAPI

- 描述

    预设库 添加MODIFIER_EFFECT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_modifier_effect_type_kv(1, 1, "value")
```

---

## set_ability_key_modifier_kv

method in GameAPI

- 描述

    预设库 添加MODIFIER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_modifier_kv(1, 1, "value")
```

---

## set_ability_key_projectile_kv

method in GameAPI

- 描述

    预设库 添加PROJECTILE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_projectile_kv(1, 1, "value")
```

---

## set_ability_key_projectile_entity_kv

method in GameAPI

- 描述

    预设库 添加PROJECTILE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_projectile_entity_kv(1, 1, "value")
```

---

## set_ability_key_projectile_group_kv

method in GameAPI

- 描述

    预设库 添加PROJECTILE_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_projectile_group_kv(1, 1, "value")
```

---

## set_ability_key_destructible_entity_kv

method in GameAPI

- 描述

    预设库 添加DESTRUCTIBLE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_destructible_entity_kv(1, 1, "value")
```

---

## set_ability_key_destructible_name_kv

method in GameAPI

- 描述

    预设库 添加DESTRUCTIBLE_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_destructible_name_kv(1, 1, "value")
```

---

## set_ability_key_sound_entity_kv

method in GameAPI

- 描述

    预设库 添加SOUND_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_sound_entity_kv(1, 1, "value")
```

---

## set_ability_key_audio_key_kv

method in GameAPI

- 描述

    预设库 添加AUDIO_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_audio_key_kv(1, 1, "value")
```

---

## set_ability_key_game_mode_kv

method in GameAPI

- 描述

    预设库 添加GAME_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_game_mode_kv(1, 1, "value")
```

---

## set_ability_key_player_kv

method in GameAPI

- 描述

    预设库 添加PLAYER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_player_kv(1, 1, "value")
```

---

## set_ability_key_player_group_kv

method in GameAPI

- 描述

    预设库 添加PLAYER_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_player_group_kv(1, 1, "value")
```

---

## set_ability_key_role_res_key_kv

method in GameAPI

- 描述

    预设库 添加ROLE_RES_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_role_res_key_kv(1, 1, "value")
```

---

## set_ability_key_role_status_kv

method in GameAPI

- 描述

    预设库 添加ROLE_STATUS键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_role_status_kv(1, 1, "value")
```

---

## set_ability_key_role_type_kv

method in GameAPI

- 描述

    预设库 添加ROLE_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_role_type_kv(1, 1, "value")
```

---

## set_ability_key_role_relation_kv

method in GameAPI

- 描述

    预设库 添加ROLE_RELATION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_role_relation_kv(1, 1, "value")
```

---

## set_ability_key_team_kv

method in GameAPI

- 描述

    预设库 添加TEAM键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_team_kv(1, 1, "value")
```

---

## set_ability_key_point_kv

method in GameAPI

- 描述

    预设库 添加POINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_point_kv(1, 1, "value")
```

---

## set_ability_key_vector3_kv

method in GameAPI

- 描述

    预设库 添加VECTOR3键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_vector3_kv(1, 1, "value")
```

---

## set_ability_key_rotation_kv

method in GameAPI

- 描述

    预设库 添加ROTATION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_rotation_kv(1, 1, "value")
```

---

## set_ability_key_point_list_kv

method in GameAPI

- 描述

    预设库 添加POINT_LIST键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_point_list_kv(1, 1, "value")
```

---

## set_ability_key_rectangle_kv

method in GameAPI

- 描述

    预设库 添加RECTANGLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_rectangle_kv(1, 1, "value")
```

---

## set_ability_key_round_area_kv

method in GameAPI

- 描述

    预设库 添加ROUND_AREA键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_round_area_kv(1, 1, "value")
```

---

## set_ability_key_polygon_kv

method in GameAPI

- 描述

    预设库 添加POLYGON键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_polygon_kv(1, 1, "value")
```

---

## set_ability_key_camera_kv

method in GameAPI

- 描述

    预设库 添加CAMERA键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_camera_kv(1, 1, "value")
```

---

## set_ability_key_camline_kv

method in GameAPI

- 描述

    预设库 添加CAMLINE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_camline_kv(1, 1, "value")
```

---

## set_ability_key_point_light_kv

method in GameAPI

- 描述

    预设库 添加POINT_LIGHT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_point_light_kv(1, 1, "value")
```

---

## set_ability_key_spot_light_kv

method in GameAPI

- 描述

    预设库 添加SPOT_LIGHT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_spot_light_kv(1, 1, "value")
```

---

## set_ability_key_fog_kv

method in GameAPI

- 描述

    预设库 添加FOG键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_fog_kv(1, 1, "value")
```

---

## set_ability_key_scene_sound_kv

method in GameAPI

- 描述

    预设库 添加SCENE_SOUND键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_scene_sound_kv(1, 1, "value")
```

---

## set_ability_key_model_kv

method in GameAPI

- 描述

    预设库 添加MODEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_model_kv(1, 1, "value")
```

---

## set_ability_key_sfx_entity_kv

method in GameAPI

- 描述

    预设库 添加SFX_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_sfx_entity_kv(1, 1, "value")
```

---

## set_ability_key_sfx_key_kv

method in GameAPI

- 描述

    预设库 添加SFX_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_sfx_key_kv(1, 1, "value")
```

---

## set_ability_key_link_sfx_entity_kv

method in GameAPI

- 描述

    预设库 添加LINK_SFX_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_link_sfx_entity_kv(1, 1, "value")
```

---

## set_ability_key_link_sfx_key_kv

method in GameAPI

- 描述

    预设库 添加LINK_SFX_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_link_sfx_key_kv(1, 1, "value")
```

---

## set_ability_key_cursor_key_kv

method in GameAPI

- 描述

    预设库 添加CURSOR_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_cursor_key_kv(1, 1, "value")
```

---

## set_ability_key_angle_kv

method in GameAPI

- 描述

    预设库 添加ANGLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_angle_kv(1, 1, "value")
```

---

## set_ability_key_texture_kv

method in GameAPI

- 描述

    预设库 添加TEXTURE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_texture_kv(1, 1, "value")
```

---

## set_ability_key_sequence_kv

method in GameAPI

- 描述

    预设库 添加SEQUENCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_sequence_kv(1, 1, "value")
```

---

## set_ability_key_physics_object_kv

method in GameAPI

- 描述

    预设库 添加PHYSICS_OBJECT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_physics_object_kv(1, 1, "value")
```

---

## set_ability_key_physics_entity_kv

method in GameAPI

- 描述

    预设库 添加PHYSICS_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_physics_entity_kv(1, 1, "value")
```

---

## set_ability_key_physics_object_key_kv

method in GameAPI

- 描述

    预设库 添加PHYSICS_OBJECT_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_physics_object_key_kv(1, 1, "value")
```

---

## set_ability_key_physics_entity_key_kv

method in GameAPI

- 描述

    预设库 添加PHYSICS_ENTITY_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_physics_entity_key_kv(1, 1, "value")
```

---

## set_ability_key_rigid_body_kv

method in GameAPI

- 描述

    预设库 添加RIGID_BODY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_rigid_body_kv(1, 1, "value")
```

---

## set_ability_key_rigid_body_group_kv

method in GameAPI

- 描述

    预设库 添加RIGID_BODY_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_rigid_body_group_kv(1, 1, "value")
```

---

## set_ability_key_collider_kv

method in GameAPI

- 描述

    预设库 添加COLLIDER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_collider_kv(1, 1, "value")
```

---

## set_ability_key_joint_kv

method in GameAPI

- 描述

    预设库 添加JOINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_joint_kv(1, 1, "value")
```

---

## set_ability_key_reaction_kv

method in GameAPI

- 描述

    预设库 添加REACTION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_reaction_kv(1, 1, "value")
```

---

## set_ability_key_reaction_group_kv

method in GameAPI

- 描述

    预设库 添加REACTION_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_reaction_group_kv(1, 1, "value")
```

---

## set_ability_key_dynamic_trigger_instance_kv

method in GameAPI

- 描述

    预设库 添加DYNAMIC_TRIGGER_INSTANCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_dynamic_trigger_instance_kv(1, 1, "value")
```

---

## set_ability_key_table_kv

method in GameAPI

- 描述

    预设库 添加TABLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_table_kv(1, 1, "value")
```

---

## set_ability_key_random_pool_kv

method in GameAPI

- 描述

    预设库 添加RANDOM_POOL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_random_pool_kv(1, 1, "value")
```

---

## set_ability_key_scene_ui_kv

method in GameAPI

- 描述

    预设库 添加SCENE_UI键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_scene_ui_kv(1, 1, "value")
```

---

## set_ability_key_damage_type_kv

method in GameAPI

- 描述

    预设库 添加DAMAGE_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_damage_type_kv(1, 1, "value")
```

---

## set_ability_key_harm_text_type_new_kv

method in GameAPI

- 描述

    预设库 添加HARM_TEXT_TYPE_NEW键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_harm_text_type_new_kv(1, 1, "value")
```

---

## set_ability_key_font_type_kv

method in GameAPI

- 描述

    预设库 添加FONT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_font_type_kv(1, 1, "value")
```

---

## set_ability_key_jump_word_track_kv

method in GameAPI

- 描述

    预设库 添加JUMP_WORD_TRACK键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_jump_word_track_kv(1, 1, "value")
```

---

## set_ability_key_new_timer_kv

method in GameAPI

- 描述

    预设库 添加NEW_TIMER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_new_timer_kv(1, 1, "value")
```

---

## set_ability_key_tech_key_kv

method in GameAPI

- 描述

    预设库 添加TECH_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_tech_key_kv(1, 1, "value")
```

---

## set_ability_key_store_key_kv

method in GameAPI

- 描述

    预设库 添加STORE_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_store_key_kv(1, 1, "value")
```

---

## set_ability_key_keyboard_key_kv

method in GameAPI

- 描述

    预设库 添加KEYBOARD_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_keyboard_key_kv(1, 1, "value")
```

---

## set_ability_key_func_keyboard_key_kv

method in GameAPI

- 描述

    预设库 添加FUNC_KEYBOARD_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_func_keyboard_key_kv(1, 1, "value")
```

---

## set_ability_key_mouse_key_kv

method in GameAPI

- 描述

    预设库 添加MOUSE_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_mouse_key_kv(1, 1, "value")
```

---

## set_ability_key_mouse_wheel_kv

method in GameAPI

- 描述

    预设库 添加MOUSE_WHEEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_mouse_wheel_kv(1, 1, "value")
```

---

## set_ability_key_post_effect_kv

method in GameAPI

- 描述

    预设库 添加POST_EFFECT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_post_effect_kv(1, 1, "value")
```

---

## set_ability_key_unit_type_kv

method in GameAPI

- 描述

    预设库 添加UNIT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_unit_type_kv(1, 1, "value")
```

---

## set_ability_key_unit_command_type_kv

method in GameAPI

- 描述

    预设库 添加UNIT_COMMAND_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_unit_command_type_kv(1, 1, "value")
```

---

## set_ability_key_mini_map_color_type_kv

method in GameAPI

- 描述

    预设库 添加MINI_MAP_COLOR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_mini_map_color_type_kv(1, 1, "value")
```

---

## set_ability_key_unit_behavior_kv

method in GameAPI

- 描述

    预设库 添加UNIT_BEHAVIOR键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_unit_behavior_kv(1, 1, "value")
```

---

## set_ability_key_curved_path_kv

method in GameAPI

- 描述

    预设库 添加CURVED_PATH键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_curved_path_kv(1, 1, "value")
```

---

## set_ability_key_curved_path_3d_kv

method in GameAPI

- 描述

    预设库 添加CURVED_PATH_3D键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_curved_path_3d_kv(1, 1, "value")
```

---

## is_modifier_id

method in GameAPI

- 描述

    判断BUFF是否是目标BUFFID的实例

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier1 | py.ModifierEntity | BUFF实例 |
    | modifier_key | py.ModifierKey | BUFFID |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否是目标buff的实例 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)
local modifier_key = 134274569

local result = GameAPI.is_modifier_id(modifier.handle, modifier_key)
```

---

## is_modifier_instance

method in GameAPI

- 描述

    判断BUFF是否是目标BUFF实例

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier1 | py.ModifierEntity | BUFF实例 |
    | modifier2 | py.ModifierEntity | BUFF实例 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否是目标实例 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

local result = GameAPI.is_modifier_instance(modifier.handle, modifier.handle)
```

---

## judge_modifier_effect_type

method in GameAPI

- 描述

    判断BUFF是否是为目标类型的buff(正面负面等)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier1 | py.ModifierEntity | BUFF实例 |
    | modifier_type | py.ModifierEffectType | BUFF效果类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否是目标效果类型 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

local result = GameAPI.judge_modifier_effect_type(modifier.handle, 1)
```

---

## get_type_of_modifier_entity

method in GameAPI

- 描述

    获取目标效果(BUFF)的效果类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier1 | py.ModifierEntity | BUFF实例 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierKey | 效果编号 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

local result = GameAPI.get_type_of_modifier_entity(modifier.handle)
```

---

## transfer_num_into_modifier_key

method in GameAPI

- 描述

    转换目标数字ID到效果类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | integer | 数字编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierKey | 效果编号 |

- 示例

```lua
local result = GameAPI.transfer_num_into_modifier_key(1)
```

---

## api_get_name_of_modifier_key

method in GameAPI

- 描述

    获取魔法效果类型的名称

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 名称 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.api_get_name_of_modifier_key(modifier_key)
```

---

## create_modifier_editor_data

method in GameAPI

- 描述

    创建新魔法效果物编

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | old_entity_no | py.ModifierKey | 魔法效果物编 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierKey | 魔法效果物编 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.create_modifier_editor_data(modifier_key)
```

---

## get_last_compose_unit

method in GameAPI

- 描述

    最近合成物品的单位

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 单位实体 |

- 示例

```lua
local result = GameAPI.get_last_compose_unit()
```

---

## get_last_add_item

method in GameAPI

- 描述

    最近添加物品

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Item | 物品实体 |

- 示例

```lua
local result = GameAPI.get_last_add_item()
```

---

## get_last_remove_item

method in GameAPI

- 描述

    最近移除物品

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Item | 物品实体 |

- 示例

```lua
local result = GameAPI.get_last_remove_item()
```

---

## get_last_use_item

method in GameAPI

- 描述

    最近使用物品

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Item | 物品实体 |

- 示例

```lua
local result = GameAPI.get_last_use_item()
```

---

## get_last_stack_changed_item

method in GameAPI

- 描述

    最近堆叠变化物品

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Item | 物品实体 |

- 示例

```lua
local result = GameAPI.get_last_stack_changed_item()
```

---

## get_last_charge_changed_item

method in GameAPI

- 描述

    最近充能变化物品

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Item | 物品实体 |

- 示例

```lua
local result = GameAPI.get_last_charge_changed_item()
```

---

## get_last_add_item_unit

method in GameAPI

- 描述

    最近添加物品单位

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 单位实体 |

- 示例

```lua
local result = GameAPI.get_last_add_item_unit()
```

---

## get_last_remove_item_unit

method in GameAPI

- 描述

    最近移除物品单位

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 单位实体 |

- 示例

```lua
local result = GameAPI.get_last_remove_item_unit()
```

---

## get_last_use_item_unit

method in GameAPI

- 描述

    最近使用物品单位

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 单位实体 |

- 示例

```lua
local result = GameAPI.get_last_use_item_unit()
```

---

## get_last_change_item_stack_unit

method in GameAPI

- 描述

    最近物品层数变化单位

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 单位实体 |

- 示例

```lua
local result = GameAPI.get_last_change_item_stack_unit()
```

---

## api_get_attr_of_item_key

method in GameAPI

- 描述

    获取物品类型附加属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品类型编号 |
    | attr_element_field | string | 属性名 |
    | attr_key | string | 属性成分名 |

- 返回值

    无

- 示例

```lua
local item_key = 134274569

GameAPI.api_get_attr_of_item_key(item_key, "attr_element_field", "attr_key")
```

---

## api_get_item_type_model

method in GameAPI

- 描述

    获取物品类型的模型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品类型编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModelKey | 模型编号 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.api_get_item_type_model(item_key)
```

---

## api_get_value_of_item_name_comp_mat

method in GameAPI

- 描述

    遍历物品类型合成所需的物品类型数量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品类型编号 |
    | comp_item_key | py.ItemKey | 物品类型编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 个数 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.api_get_value_of_item_name_comp_mat(item_key, item_key)
```

---

## api_get_value_of_item_name_comp_res

method in GameAPI

- 描述

    遍历物品类型合成所需的玩家属性数量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品类型编号 |
    | role_res_key | py.RoleResKey | 玩家属性 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 取值 |

- 示例

```lua
local item_key = 134274569
local role_res_key = "res_key"

local result = GameAPI.api_get_value_of_item_name_comp_res(item_key, role_res_key)
```

---

## create_item_editor_data

method in GameAPI

- 描述

    创建新物品物编

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | old_entity_no | py.ItemKey | 物品物编 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemKey | 物品物编 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.create_item_editor_data(item_key)
```

---

## api_get_item_key_res_cnt

method in GameAPI

- 描述

    获取物品类型的购买所需资源

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_no | py.ItemKey | 物品物编 |
    | role_res_key | py.RoleResKey | 玩家属性 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 资源数量 |

- 示例

```lua
local item_key = 134274569
local role_res_key = "res_key"

local result = GameAPI.api_get_item_key_res_cnt(item_key, role_res_key)
```

---

## api_get_item_type_float_attr

method in GameAPI

- 描述

    获取物品类型的实数属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_no | py.ItemKey | 物编编号 |
    | attr_key | string | 物品类型实数属性key |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 实数属性值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.api_get_item_type_float_attr(item_key, "attr_key")
```

---

## api_get_item_type_int_attr

method in GameAPI

- 描述

    获取物品类型的整数属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_no | py.ItemKey | 物编编号 |
    | attr_key | string | 物品整数属性key |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 整数属性值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.api_get_item_type_int_attr(item_key, "attr_key")
```

---

## api_add_item_to_group

method in GameAPI

- 描述

    添加物品到物品组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_group | py.Item | 物品 |
    | item | py.ItemGroup | 物品组 |

- 返回值

    无

- 示例

```lua
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)
local item_group = y3.item_group.create()

GameAPI.api_add_item_to_group(item.handle, item_group.handle)
```

---

## api_remove_item_in_group

method in GameAPI

- 描述

    删除物品组中某个物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_group | py.ItemGroup | 物品组 |
    | item | py.Item | 物品 |

- 返回值

    无

- 示例

```lua
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)
local item_group = y3.item_group.create()

GameAPI.api_remove_item_in_group(item_group.handle, item.handle)
```

---

## api_judge_item_in_group

method in GameAPI

- 描述

    判断物品是否在物品组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item | py.Item | 物品 |
    | item_group | py.ItemGroup | 物品组 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否在物品组 |

- 示例

```lua
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)
local item_group = y3.item_group.create()

local result = GameAPI.api_judge_item_in_group(item.handle, item_group.handle)
```

---

## api_get_random_item_in_item_group

method in GameAPI

- 描述

    物品组内随机一个单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_group | py.ItemGroup | 物品组 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Item | 物品 |

- 示例

```lua
local item_group = y3.item_group.create()

local result = GameAPI.api_get_random_item_in_item_group(item_group.handle)
```

---

## get_last_buy_shop_item

method in GameAPI

- 描述

    最近被购买物品

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Item | 物品实体 |

- 示例

```lua
local result = GameAPI.get_last_buy_shop_item()
```

---

## get_last_sell_shop_item

method in GameAPI

- 描述

    最近被出售物品

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Item | 物品实体 |

- 示例

```lua
local result = GameAPI.get_last_sell_shop_item()
```

---

## get_last_buyer_unit

method in GameAPI

- 描述

    最近购买者

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 单位实体 |

- 示例

```lua
local result = GameAPI.get_last_buyer_unit()
```

---

## get_last_seller_unit

method in GameAPI

- 描述

    最近出售者

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 单位实体 |

- 示例

```lua
local result = GameAPI.get_last_seller_unit()
```

---

## get_last_buy_shop_unit

method in GameAPI

- 描述

    最近被购买单位

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 单位实体 |

- 示例

```lua
local result = GameAPI.get_last_buy_shop_unit()
```

---

## get_last_upgraded_tech

method in GameAPI

- 描述

    最近升级科技

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.TechKey | 科技编号 |

- 示例

```lua
local result = GameAPI.get_last_upgraded_tech()
```

---

## get_last_operated_tech

method in GameAPI

- 描述

    最近升降科技

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.TechKey | 科技编号 |

- 示例

```lua
local result = GameAPI.get_last_operated_tech()
```

---

## get_last_changed_tech

method in GameAPI

- 描述

    最近变化科技

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.TechKey | 科技编号 |

- 示例

```lua
local result = GameAPI.get_last_changed_tech()
```

---

## get_last_changed_tech_level

method in GameAPI

- 描述

    最近变化科技等级

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 科技变化等级 |

- 示例

```lua
local result = GameAPI.get_last_changed_tech_level()
```

---

## get_last_added_tech

method in GameAPI

- 描述

    最近获得科技

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.TechKey | 科技编号 |

- 示例

```lua
local result = GameAPI.get_last_added_tech()
```

---

## get_last_removed_tech

method in GameAPI

- 描述

    最近失去科技

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.TechKey | 科技编号 |

- 示例

```lua
local result = GameAPI.get_last_removed_tech()
```

---

## get_last_upgrade_tech_unit

method in GameAPI

- 描述

    最近研究科技单位

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 研究科技单位 |

- 示例

```lua
local result = GameAPI.get_last_upgrade_tech_unit()
```

---

## get_last_add_tech_unit

method in GameAPI

- 描述

    最近获得科技单位

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 获得科技单位 |

- 示例

```lua
local result = GameAPI.get_last_add_tech_unit()
```

---

## get_last_remove_tech_unit

method in GameAPI

- 描述

    最近失去科技单位

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 失去科技单位 |

- 示例

```lua
local result = GameAPI.get_last_remove_tech_unit()
```

---

## get_tech_name

method in GameAPI

- 描述

    获取科技对应等级名字

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_no | py.TechKey | 科技编号 |
    | level | integer | 等级 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 名字 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_name(tech_key, 1)
```

---

## get_tech_icon

method in GameAPI

- 描述

    获取科技对应等级icon

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_no | py.TechKey | 科技编号 |
    | level | integer | 等级 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 图片id |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_icon(tech_key, 1)
```

---

## get_tech_cost

method in GameAPI

- 描述

    获取科技对应等级的花费

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_no | py.TechKey | 科技编号 |
    | level | integer | 等级 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 图片id |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_cost(tech_key, 1)
```

---

## get_tech_max_level

method in GameAPI

- 描述

    获取科技最大等级

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_no | py.TechKey | 科技编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 科技最大等级 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_max_level(tech_key)
```

---

## create_technology_editor_data

method in GameAPI

- 描述

    创建新科技物编

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | old_entity_no | py.TechKey | 科技物编 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.TechKey | 科技物编 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.create_technology_editor_data(tech_key)
```

---

## get_last_use_store_item_role

method in GameAPI

- 描述

    最近成功使用收费道具玩家

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Role | 玩家 |

- 示例

```lua
local result = GameAPI.get_last_use_store_item_role()
```

---

## set_function_return

method in GameAPI

- 描述

    设置函数返回值

- 参数

    无

- 返回值

    无

- 示例

```lua
GameAPI.set_function_return()
```

---

## get_function_return_value

method in GameAPI

- 描述

    获取函数返回值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | func_id | string | 函数ID |
    | actor | py.Actor | 调用者 |
    | context | py.Dict | 上下文 |
    | params_expr | py.List | 参数列表 |
    | call_rt_idx | integer | 返回值Index |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DynamicTypeMeta | 某一返回值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local dict = pydict()
local list = {}

local result = GameAPI.get_function_return_value("func_id", actor, dict, list, 1)
```

---

## send_event_custom

method in GameAPI

- 描述

    发送自定义事件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | event_id | integer | 事件ID |
    | params_dict | py.Dict | 参数字典 |

- 返回值

    无

- 示例

```lua
local dict = pydict()

GameAPI.send_event_custom(1, dict)
```

---

## gen_param_dict

method in GameAPI

- 描述

    生成字典

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ori_dict | py.Dict | 字典 |
    | key | string | 参数key |
    | param | string | 参数value |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Dict | 字典返回值 |

- 示例

```lua
local dict = pydict()

local result = GameAPI.gen_param_dict(dict, "key", "param")
```

---

## get_custom_param

method in GameAPI

- 描述

    获取字典中的值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | params_dict | py.Dict | 字典 |
    | key | string | 参数key |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DynamicTypeMeta | 字典中的值 |

- 示例

```lua
local dict = pydict()

local result = GameAPI.get_custom_param(dict, "key")
```

---

## eval_lua_code

method in GameAPI

- 描述

    执行Lua代码

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | code | string | 字符串 |
    | arg1? | string | 参数1 |
    | arg2? | string | 参数2 |
    | arg3? | string | 参数3 |
    | arg4? | string | 参数4 |
    | arg5? | string | 参数5 |

- 返回值

    无

- 示例

```lua
GameAPI.eval_lua_code("code", "arg1", "arg2", "arg3", "arg4", "arg5")
```

---

## remove_unit_mover

method in GameAPI

- 描述

    删除单位运动器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.remove_unit_mover(unit.handle)
```

---

## break_unit_mover

method in GameAPI

- 描述

    打断单位运动器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.break_unit_mover(unit.handle)
```

---

## get_mover_collide_unit

method in GameAPI

- 描述

    运动器碰撞单位

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 单位实体 |

- 示例

```lua
local result = GameAPI.get_mover_collide_unit()
```

---

## create_chasing_mover

method in GameAPI

- 描述

    创建追踪运动器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | target_unit | py.Unit | 目标单位 |
    | stop_distance_to_target | number | 停止距离 |
    | init_velocity | number | 初始速度 |
    | acceleration | number | 加速度 |
    | max_velocity? | number | 最大速度 |
    | min_velocity? | number | 最小速度 |
    | init_height? | number | 起始高度 |
    | parabola_height? | number | 抛物线高度 |
    | bind_point? | string | 附着点 |
    | collision_type? | integer | 碰撞类型 |
    | collision_radius? | number | 碰撞范围 |
    | is_face_angle? | boolean | 是否始终面向运动方向 |
    | is_multi_collision? | boolean | 是否能多次碰撞同一个物体 |
    | terrain_block? | boolean | 地形阻挡 |
    | priority? | integer | 优先级数 |
    | is_absolute_height? | boolean | 使用绝对高度 |
    | f_mover_finish? | function | 运动完成事件 |
    | f_mover_interrupt? | function | 运动打断事件 |
    | f_mover_removed? | function | 运动移除事件 |
    | f_terrain_collide? | function | 地形碰撞事件 |
    | f_unit_collide? | function | 单位碰撞事件 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Mover | 运动器ID |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = GameAPI.create_chasing_mover(unit.handle, unit.handle, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, "bind_point", 1, 1.0, true, true, true, 1, true, function() end, function() end, function() end, function() end, function() end)
```

---

## create_straight_mover

method in GameAPI

- 描述

    创建直线运动器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | angle | number | 运动方向 |
    | max_dist | number | 最大距离 |
    | init_velocity | number | 初始速度 |
    | acceleration | number | 加速度 |
    | max_velocity? | number | 最大速度 |
    | min_velocity? | number | 最小速度 |
    | init_height? | number | 起始高度 |
    | fin_height? | number | 终点高度 |
    | parabola_height? | number | 抛物线高度 |
    | collision_type? | integer | 碰撞类型 |
    | collision_radius? | number | 碰撞范围 |
    | is_face_angle? | boolean | 是否始终面向运动方向 |
    | is_multi_collision? | boolean | 是否能多次碰撞同一个物体 |
    | terrain_block? | boolean | 地形阻挡 |
    | priority? | integer | 优先级数 |
    | is_absolute_height? | boolean | 使用绝对高度 |
    | f_mover_finish? | function | 运动完成事件 |
    | f_mover_interrupt? | function | 运动打断事件 |
    | f_mover_removed? | function | 运动移除事件 |
    | f_terrain_collide? | function | 地形碰撞事件 |
    | f_unit_collide? | function | 单位碰撞事件 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Mover | 运动器ID |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = GameAPI.create_straight_mover(unit.handle, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1, 1.0, true, true, true, 1, true, function() end, function() end, function() end, function() end, function() end)
```

---

## create_round_mover

method in GameAPI

- 描述

    创建环绕运动器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | target_unit | py.Unit | 目标单位 |
    | circle_radius | number | 圆周半径 |
    | angle_velocity | number | 角速度 |
    | init_angle? | number | 初始角度 |
    | counterclockwise? | number | 方向 |
    | round_time? | number | 环绕时间 |
    | centrifugal_velocity? | number | 离心速度 |
    | lifting_velocity? | number | 提升速度 |
    | init_height? | number | 环绕高度 |
    | collision_type? | integer | 碰撞类型 |
    | collision_radius? | number | 碰撞范围 |
    | is_face_angle? | boolean | 是否始终面向运动方向 |
    | is_multi_collision? | boolean | 是否能多次碰撞同一个物体 |
    | terrain_block? | boolean | 地形阻挡 |
    | priority? | integer | 优先级数 |
    | is_absolute_height? | boolean | 使用绝对高度 |
    | target_pos? | py.Vector3 | 目标坐标 |
    | f_mover_finish? | function | 运动完成事件 |
    | f_mover_interrupt? | function | 运动打断事件 |
    | f_mover_removed? | function | 运动移除事件 |
    | f_terrain_collide? | function | 地形碰撞事件 |
    | f_unit_collide? | function | 单位碰撞事件 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Mover | 运动器ID |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local vector3 = Fix32Vec3(0, 0, 0)

local result = GameAPI.create_round_mover(unit.handle, unit.handle, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1, 1.0, true, true, true, 1, true, nil, function() end, function() end, function() end, function() end, function() end)
```

---

## create_curved_mover

method in GameAPI

- 描述

    创建曲线运动器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | angle | number | 运动方向 |
    | max_dist | number | 最大距离 |
    | init_velocity | number | 初始速度 |
    | acceleration | number | 加速度 |
    | max_velocity? | number | 最大速度 |
    | min_velocity? | number | 最小速度 |
    | init_height? | number | 起始高度 |
    | fin_height? | number | 终点高度 |
    | collision_type? | integer | 碰撞类型 |
    | collision_radius? | number | 碰撞范围 |
    | is_face_angle? | boolean | 是否始终面向运动方向 |
    | is_multi_collision? | boolean | 是否能多次碰撞同一个物体 |
    | terrain_block? | boolean | 地形阻挡 |
    | priority? | integer | 优先级数 |
    | is_absolute_height? | boolean | 使用绝对高度 |
    | path? | py.CurvedPath | 路径 |
    | f_mover_finish? | function | 运动完成事件 |
    | f_mover_interrupt? | function | 运动打断事件 |
    | f_mover_removed? | function | 运动移除事件 |
    | f_terrain_collide? | function | 地形碰撞事件 |
    | f_unit_collide? | function | 单位碰撞事件 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Mover | 运动器ID |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local path = {}

local result = GameAPI.create_curved_mover(unit.handle, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1, 1.0, true, true, true, 1, true, nil, function() end, function() end, function() end, function() end, function() end)
```

---

## get_mover_type

method in GameAPI

- 描述

    获得运动器类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | mover_id | py.Mover | 运动器 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 运动器类型 |

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })
local mover = GameAPI.get_projectile_mover(projectile.handle)

local result = GameAPI.get_mover_type(mover)
```

---

## remove_mover

method in GameAPI

- 描述

    删除运动器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | mover_id | py.Mover | 运动器 |

- 返回值

    无

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })
local mover = GameAPI.get_projectile_mover(projectile.handle)

GameAPI.remove_mover(mover)
```

---

## break_mover

method in GameAPI

- 描述

    打断运动器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | mover_id | py.Mover | 运动器 |

- 返回值

    无

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })
local mover = GameAPI.get_projectile_mover(projectile.handle)

GameAPI.break_mover(mover)
```

---

## get_unit_mover

method in GameAPI

- 描述

    获得单位的运动器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Mover | 运动器 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = GameAPI.get_unit_mover(unit.handle)
```

---

## get_mover_priority

method in GameAPI

- 描述

    获取运动器的优先级

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | mover_id | py.Mover | 运动器 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 优先级 |

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })
local mover = GameAPI.get_projectile_mover(projectile.handle)

local result = GameAPI.get_mover_priority(mover)
```

---

## set_mover_priority

method in GameAPI

- 描述

    设置运动器的优先级

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | mover_id | py.Mover | 运动器 |
    | priority | integer | 优先级 |

- 返回值

    无

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })
local mover = GameAPI.get_projectile_mover(projectile.handle)

GameAPI.set_mover_priority(mover, 1)
```

---

## set_mover_property

method in GameAPI

- 描述

    设置运动器的属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | mover_id | py.Mover | 运动器 |
    | key | integer | 属性名 |
    | value | py.Fixed | 属性值 |

- 返回值

    无

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })
local mover = GameAPI.get_projectile_mover(projectile.handle)

GameAPI.set_mover_property(mover, 1, Fix32(1))
```

---

## get_mover_property

method in GameAPI

- 描述

    获取运动器的属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | mover_id | py.Mover | 运动器 |
    | key | integer | 属性名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 属性值 |

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })
local mover = GameAPI.get_projectile_mover(projectile.handle)

local result = GameAPI.get_mover_property(mover, 1)
```

---

## get_mover_angle

method in GameAPI

- 描述

    获得运动器的运动方向

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | mover_id | py.Mover | 运动器 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 角度 |

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })
local mover = GameAPI.get_projectile_mover(projectile.handle)

local result = GameAPI.get_mover_angle(mover)
```

---

## set_mover_angle

method in GameAPI

- 描述

    设置运动器的运动方向

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | mover_id | py.Mover | 运动器 |
    | angle | py.Fixed | 方向 |

- 返回值

    无

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })
local mover = GameAPI.get_projectile_mover(projectile.handle)

GameAPI.set_mover_angle(mover, Fix32(1))
```

---

## set_mover_collision_radius

method in GameAPI

- 描述

    设置运动器的碰撞范围

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | mover_id | py.Mover | 运动器 |
    | radius | py.Fixed | 碰撞范围 |

- 返回值

    无

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })
local mover = GameAPI.get_projectile_mover(projectile.handle)

GameAPI.set_mover_collision_radius(mover, Fix32(1))
```

---

## get_mover_collision_radius

method in GameAPI

- 描述

    获得运动器的碰撞范围

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | mover_id | py.Mover | 运动器 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 碰撞范围 |

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })
local mover = GameAPI.get_projectile_mover(projectile.handle)

local result = GameAPI.get_mover_collision_radius(mover)
```

---

## set_mover_relate_unit

method in GameAPI

- 描述

    设置运动器的关联单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | mover_id | py.Mover | 运动器 |
    | unit | py.Unit | 关联单位 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })
local mover = GameAPI.get_projectile_mover(projectile.handle)

GameAPI.set_mover_relate_unit(mover, unit.handle)
```

---

## get_mover_relate_unit

method in GameAPI

- 描述

    获得运动器的关联单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | mover_id | py.Mover | 运动器 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 关联单位 |

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })
local mover = GameAPI.get_projectile_mover(projectile.handle)

local result = GameAPI.get_mover_relate_unit(mover)
```

---

## set_mover_relate_ability

method in GameAPI

- 描述

    设置运动器的关联技能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | mover_id | py.Mover | 运动器 |
    | ability | py.Ability | 关联技能 |

- 返回值

    无

- 示例

```lua
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })
local mover = GameAPI.get_projectile_mover(projectile.handle)

GameAPI.set_mover_relate_ability(mover, ability.handle)
```

---

## get_mover_relate_ability

method in GameAPI

- 描述

    获得运动器的关联技能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | mover_id | py.Mover | 运动器 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Ability | 关联技能 |

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })
local mover = GameAPI.get_projectile_mover(projectile.handle)

local result = GameAPI.get_mover_relate_ability(mover)
```

---

## create_unit_command_move_to_pos

method in GameAPI

- 描述

    移动

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | pos | py.FVector3 | 位置 |
    | nav_range? | py.Fixed | 寻路范围 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommand | 单位命令 |

- 示例

```lua
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

local result = GameAPI.create_unit_command_move_to_pos(fvector3, Fix32(1))
```

---

## create_unit_command_stop

method in GameAPI

- 描述

    停止

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommand | 单位命令 |

- 示例

```lua
local result = GameAPI.create_unit_command_stop()
```

---

## create_unit_command_empty

method in GameAPI

- 描述

    空状态

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommand | 单位命令 |

- 示例

```lua
local result = GameAPI.create_unit_command_empty()
```

---

## create_unit_command_hold

method in GameAPI

- 描述

    驻守

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | pos | py.FVector3 | 位置 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommand | 单位命令 |

- 示例

```lua
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

local result = GameAPI.create_unit_command_hold(fvector3)
```

---

## create_unit_command_attack_move

method in GameAPI

- 描述

    攻击移动

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | pos | py.FVector3 | 位置 |
    | nav_range? | py.Fixed | 寻路范围 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommand | 单位命令 |

- 示例

```lua
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

local result = GameAPI.create_unit_command_attack_move(fvector3, Fix32(1))
```

---

## create_unit_command_attack_target

method in GameAPI

- 描述

    攻击

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | target | py.Actor | 目标 |
    | nav_range? | py.Fixed | 寻路范围 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommand | 单位命令 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.create_unit_command_attack_target(actor, Fix32(1))
```

---

## create_unit_command_move_along_road

method in GameAPI

- 描述

    沿路径移动

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | road | py.Road | 路径 |
    | patrol_mode | integer | 移动方式 |
    | can_attack | boolean | 是否主动攻击 |
    | start_from_nearest? | boolean | 是否就近开始 |
    | back_to_nearest? | boolean | 是否就近返回 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommand | 单位命令 |

- 示例

```lua
local road = y3.road.get_road_by_res_id(1)

local result = GameAPI.create_unit_command_move_along_road(road.handle, 1, true, true, true)
```

---

## create_unit_command_use_skill

method in GameAPI

- 描述

    释放技能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability | py.Ability | 技能 |
    | tar_point_1? | py.Point | 释放点1 |
    | tar_point_2? | py.Point | 释放点2 |
    | tar_unit? | py.Unit | 释放目标单位 |
    | tar_item? | py.Item | 释放目标物品 |
    | tar_dest? | py.Destructible | 目标可破坏物 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommand | 单位命令 |

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)
local destructible = y3.destructible.get_by_id(1)
if destructible then

local result = GameAPI.create_unit_command_use_skill(ability.handle)
end
```

---

## create_unit_command_use_item

method in GameAPI

- 描述

    使用物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item | py.Item | 物品 |
    | tar_point_1? | py.Point | 释放点1 |
    | tar_point_2? | py.Point | 释放点2 |
    | tar_unit? | py.Unit | 目标单位 |
    | tar_item? | py.Item | 目标物品 |
    | tar_dest? | py.Destructible | 目标可破坏物 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommand | 单位命令 |

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)
local destructible = y3.destructible.get_by_id(1)
if destructible then

local result = GameAPI.create_unit_command_use_item(item.handle)
end
```

---

## create_unit_command_pick_item

method in GameAPI

- 描述

    拾取物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item | py.Item | 物品 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommand | 单位命令 |

- 示例

```lua
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = GameAPI.create_unit_command_pick_item(item.handle)
```

---

## create_unit_command_drop_item

method in GameAPI

- 描述

    丢弃物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item | py.Item | 物品 |
    | pos | py.FVector3 | 位置 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommand | 单位命令 |

- 示例

```lua
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

local result = GameAPI.create_unit_command_drop_item(item.handle, fvector3)
```

---

## create_unit_command_transfer_item

method in GameAPI

- 描述

    转移物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item | py.Item | 物品 |
    | target | py.Unit | 对象 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommand | 单位命令 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = GameAPI.create_unit_command_transfer_item(item.handle, unit.handle)
```

---

## create_unit_command_follow

method in GameAPI

- 描述

    跟随

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | target | py.Unit | 目标 |
    | refresh_interval? | py.Fixed | 间隔 |
    | near_offset? | py.Fixed | 跟随距离 |
    | far_offset? | py.Fixed | 重新跟随距离 |
    | follow_angle? | py.Fixed | 跟随角度 |
    | follow_dead_target? | boolean | 跟随死亡目标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommand | 单位命令 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = GameAPI.create_unit_command_follow(unit.handle, Fix32(1), Fix32(1), Fix32(1), Fix32(1), true)
```

---

## get_modifier_key_ui_anim_play_mode_kv

method in GameAPI

- 描述

    获取魔法效果特效编号UI_ANIM_PLAY_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_ui_anim_play_mode_kv(modifier_key, "key")
```

---

## get_projectile_key_ui_anim_play_mode_kv

method in GameAPI

- 描述

    获取特效编号UI_ANIM_PLAY_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_ui_anim_play_mode_kv(projectile_key, "key")
```

---

## get_destructible_key_ui_anim_play_mode_kv

method in GameAPI

- 描述

    获取可破坏物编号UI_ANIM_PLAY_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_ui_anim_play_mode_kv(destructible_key, "key")
```

---

## get_tech_key_ui_anim_play_mode_kv

method in GameAPI

- 描述

    获取科技编号UI_ANIM_PLAY_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_ui_anim_play_mode_kv(tech_key, "key")
```

---

## get_icon_id_ui_anim_play_mode_kv

method in GameAPI

- 描述

    获取图片UI_ANIM_PLAY_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_ui_anim_play_mode_kv(1, "key")
```

---

## get_physics_entity_key_ui_anim_play_mode_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型UI_ANIM_PLAY_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_ui_anim_play_mode_kv(1, "key")
```

---

## get_kv_pair_value_ui_anim_play_mode

method in GameAPI

- 描述

    获取UI_ANIM_PLAY_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_ui_anim_play_mode(kvbase, "key")
```

---

## get_unit_key_ui_text_font_name_kv

method in GameAPI

- 描述

    获取单位编号UI_TEXT_FONT_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_ui_text_font_name_kv(unit_key, "key")
```

---

## get_item_key_ui_text_font_name_kv

method in GameAPI

- 描述

    获取物品编号UI_TEXT_FONT_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_ui_text_font_name_kv(item_key, "key")
```

---

## get_ability_key_ui_text_font_name_kv

method in GameAPI

- 描述

    获取技能编号UI_TEXT_FONT_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_ui_text_font_name_kv(ability_key, "key")
```

---

## get_modifier_key_ui_text_font_name_kv

method in GameAPI

- 描述

    获取魔法效果特效编号UI_TEXT_FONT_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_ui_text_font_name_kv(modifier_key, "key")
```

---

## get_projectile_key_ui_text_font_name_kv

method in GameAPI

- 描述

    获取特效编号UI_TEXT_FONT_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_ui_text_font_name_kv(projectile_key, "key")
```

---

## get_destructible_key_ui_text_font_name_kv

method in GameAPI

- 描述

    获取可破坏物编号UI_TEXT_FONT_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_ui_text_font_name_kv(destructible_key, "key")
```

---

## get_tech_key_ui_text_font_name_kv

method in GameAPI

- 描述

    获取科技编号UI_TEXT_FONT_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_ui_text_font_name_kv(tech_key, "key")
```

---

## get_icon_id_ui_text_font_name_kv

method in GameAPI

- 描述

    获取图片UI_TEXT_FONT_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_ui_text_font_name_kv(1, "key")
```

---

## get_physics_entity_key_ui_text_font_name_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型UI_TEXT_FONT_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_ui_text_font_name_kv(1, "key")
```

---

## get_kv_pair_value_ui_text_font_name

method in GameAPI

- 描述

    获取UI_TEXT_FONT_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_ui_text_font_name(kvbase, "key")
```

---

## get_unit_key_ui_eca_anim_type_kv

method in GameAPI

- 描述

    获取单位编号UI_ECA_ANIM_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_ui_eca_anim_type_kv(unit_key, "key")
```

---

## get_item_key_ui_eca_anim_type_kv

method in GameAPI

- 描述

    获取物品编号UI_ECA_ANIM_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_ui_eca_anim_type_kv(item_key, "key")
```

---

## get_ability_key_ui_eca_anim_type_kv

method in GameAPI

- 描述

    获取技能编号UI_ECA_ANIM_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_ui_eca_anim_type_kv(ability_key, "key")
```

---

## get_modifier_key_ui_eca_anim_type_kv

method in GameAPI

- 描述

    获取魔法效果特效编号UI_ECA_ANIM_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_ui_eca_anim_type_kv(modifier_key, "key")
```

---

## get_projectile_key_ui_eca_anim_type_kv

method in GameAPI

- 描述

    获取特效编号UI_ECA_ANIM_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_ui_eca_anim_type_kv(projectile_key, "key")
```

---

## get_destructible_key_ui_eca_anim_type_kv

method in GameAPI

- 描述

    获取可破坏物编号UI_ECA_ANIM_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_ui_eca_anim_type_kv(destructible_key, "key")
```

---

## get_tech_key_ui_eca_anim_type_kv

method in GameAPI

- 描述

    获取科技编号UI_ECA_ANIM_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_ui_eca_anim_type_kv(tech_key, "key")
```

---

## get_icon_id_ui_eca_anim_type_kv

method in GameAPI

- 描述

    获取图片UI_ECA_ANIM_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_ui_eca_anim_type_kv(1, "key")
```

---

## get_physics_entity_key_ui_eca_anim_type_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型UI_ECA_ANIM_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_ui_eca_anim_type_kv(1, "key")
```

---

## get_kv_pair_value_ui_eca_anim_type

method in GameAPI

- 描述

    获取UI_ECA_ANIM_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_ui_eca_anim_type(kvbase, "key")
```

---

## get_unit_key_local_unit_group_kv

method in GameAPI

- 描述

    获取单位编号LOCAL_UNIT_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LocalUnitGroup | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_local_unit_group_kv(unit_key, "key")
```

---

## get_item_key_local_unit_group_kv

method in GameAPI

- 描述

    获取物品编号LOCAL_UNIT_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LocalUnitGroup | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_local_unit_group_kv(item_key, "key")
```

---

## get_ability_key_local_unit_group_kv

method in GameAPI

- 描述

    获取技能编号LOCAL_UNIT_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LocalUnitGroup | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_local_unit_group_kv(ability_key, "key")
```

---

## get_modifier_key_local_unit_group_kv

method in GameAPI

- 描述

    获取魔法效果特效编号LOCAL_UNIT_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LocalUnitGroup | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_local_unit_group_kv(modifier_key, "key")
```

---

## get_projectile_key_local_unit_group_kv

method in GameAPI

- 描述

    获取特效编号LOCAL_UNIT_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LocalUnitGroup | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_local_unit_group_kv(projectile_key, "key")
```

---

## get_destructible_key_local_unit_group_kv

method in GameAPI

- 描述

    获取可破坏物编号LOCAL_UNIT_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LocalUnitGroup | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_local_unit_group_kv(destructible_key, "key")
```

---

## get_tech_key_local_unit_group_kv

method in GameAPI

- 描述

    获取科技编号LOCAL_UNIT_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LocalUnitGroup | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_local_unit_group_kv(tech_key, "key")
```

---

## get_icon_id_local_unit_group_kv

method in GameAPI

- 描述

    获取图片LOCAL_UNIT_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LocalUnitGroup | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_local_unit_group_kv(1, "key")
```

---

## get_physics_entity_key_local_unit_group_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型LOCAL_UNIT_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LocalUnitGroup | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_local_unit_group_kv(1, "key")
```

---

## get_kv_pair_value_local_unit_group

method in GameAPI

- 描述

    获取LOCAL_UNIT_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LocalUnitGroup | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_local_unit_group(kvbase, "key")
```

---

## get_unit_key_damage_attack_type_kv

method in GameAPI

- 描述

    获取单位编号DAMAGE_ATTACK_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_damage_attack_type_kv(unit_key, "key")
```

---

## get_item_key_damage_attack_type_kv

method in GameAPI

- 描述

    获取物品编号DAMAGE_ATTACK_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_damage_attack_type_kv(item_key, "key")
```

---

## get_ability_key_damage_attack_type_kv

method in GameAPI

- 描述

    获取技能编号DAMAGE_ATTACK_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_damage_attack_type_kv(ability_key, "key")
```

---

## get_modifier_key_damage_attack_type_kv

method in GameAPI

- 描述

    获取魔法效果特效编号DAMAGE_ATTACK_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_damage_attack_type_kv(modifier_key, "key")
```

---

## get_projectile_key_damage_attack_type_kv

method in GameAPI

- 描述

    获取特效编号DAMAGE_ATTACK_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_damage_attack_type_kv(projectile_key, "key")
```

---

## get_destructible_key_damage_attack_type_kv

method in GameAPI

- 描述

    获取可破坏物编号DAMAGE_ATTACK_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_damage_attack_type_kv(destructible_key, "key")
```

---

## get_tech_key_damage_attack_type_kv

method in GameAPI

- 描述

    获取科技编号DAMAGE_ATTACK_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_damage_attack_type_kv(tech_key, "key")
```

---

## get_icon_id_damage_attack_type_kv

method in GameAPI

- 描述

    获取图片DAMAGE_ATTACK_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_damage_attack_type_kv(1, "key")
```

---

## get_physics_entity_key_damage_attack_type_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型DAMAGE_ATTACK_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_damage_attack_type_kv(1, "key")
```

---

## get_kv_pair_value_damage_attack_type

method in GameAPI

- 描述

    获取DAMAGE_ATTACK_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_damage_attack_type(kvbase, "key")
```

---

## get_unit_key_damage_armor_type_kv

method in GameAPI

- 描述

    获取单位编号DAMAGE_ARMOR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_damage_armor_type_kv(unit_key, "key")
```

---

## get_item_key_damage_armor_type_kv

method in GameAPI

- 描述

    获取物品编号DAMAGE_ARMOR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_damage_armor_type_kv(item_key, "key")
```

---

## get_ability_key_damage_armor_type_kv

method in GameAPI

- 描述

    获取技能编号DAMAGE_ARMOR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_damage_armor_type_kv(ability_key, "key")
```

---

## get_modifier_key_damage_armor_type_kv

method in GameAPI

- 描述

    获取魔法效果特效编号DAMAGE_ARMOR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_damage_armor_type_kv(modifier_key, "key")
```

---

## get_projectile_key_damage_armor_type_kv

method in GameAPI

- 描述

    获取特效编号DAMAGE_ARMOR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_damage_armor_type_kv(projectile_key, "key")
```

---

## get_destructible_key_damage_armor_type_kv

method in GameAPI

- 描述

    获取可破坏物编号DAMAGE_ARMOR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_damage_armor_type_kv(destructible_key, "key")
```

---

## get_tech_key_damage_armor_type_kv

method in GameAPI

- 描述

    获取科技编号DAMAGE_ARMOR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_damage_armor_type_kv(tech_key, "key")
```

---

## get_icon_id_damage_armor_type_kv

method in GameAPI

- 描述

    获取图片DAMAGE_ARMOR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_damage_armor_type_kv(1, "key")
```

---

## get_physics_entity_key_damage_armor_type_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型DAMAGE_ARMOR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_damage_armor_type_kv(1, "key")
```

---

## get_kv_pair_value_damage_armor_type

method in GameAPI

- 描述

    获取DAMAGE_ARMOR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_damage_armor_type(kvbase, "key")
```

---

## get_unit_key_item_stack_type_kv

method in GameAPI

- 描述

    获取单位编号ITEM_STACK_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemStackType | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_item_stack_type_kv(unit_key, "key")
```

---

## get_item_key_item_stack_type_kv

method in GameAPI

- 描述

    获取物品编号ITEM_STACK_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemStackType | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_item_stack_type_kv(item_key, "key")
```

---

## get_ability_key_item_stack_type_kv

method in GameAPI

- 描述

    获取技能编号ITEM_STACK_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemStackType | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_item_stack_type_kv(ability_key, "key")
```

---

## get_modifier_key_item_stack_type_kv

method in GameAPI

- 描述

    获取魔法效果特效编号ITEM_STACK_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemStackType | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_item_stack_type_kv(modifier_key, "key")
```

---

## get_projectile_key_item_stack_type_kv

method in GameAPI

- 描述

    获取特效编号ITEM_STACK_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemStackType | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_item_stack_type_kv(projectile_key, "key")
```

---

## get_destructible_key_item_stack_type_kv

method in GameAPI

- 描述

    获取可破坏物编号ITEM_STACK_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemStackType | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_item_stack_type_kv(destructible_key, "key")
```

---

## get_tech_key_item_stack_type_kv

method in GameAPI

- 描述

    获取科技编号ITEM_STACK_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemStackType | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_item_stack_type_kv(tech_key, "key")
```

---

## get_icon_id_item_stack_type_kv

method in GameAPI

- 描述

    获取图片ITEM_STACK_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemStackType | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_item_stack_type_kv(1, "key")
```

---

## get_physics_entity_key_item_stack_type_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型ITEM_STACK_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemStackType | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_item_stack_type_kv(1, "key")
```

---

## get_kv_pair_value_item_stack_type

method in GameAPI

- 描述

    获取ITEM_STACK_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemStackType | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_item_stack_type(kvbase, "key")
```

---

## get_unit_key_ability_release_id_kv

method in GameAPI

- 描述

    获取单位编号ABILITY_RELEASE_ID键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityReleaseId | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_ability_release_id_kv(unit_key, "key")
```

---

## get_item_key_ability_release_id_kv

method in GameAPI

- 描述

    获取物品编号ABILITY_RELEASE_ID键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityReleaseId | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_ability_release_id_kv(item_key, "key")
```

---

## get_ability_key_ability_release_id_kv

method in GameAPI

- 描述

    获取技能编号ABILITY_RELEASE_ID键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityReleaseId | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_ability_release_id_kv(ability_key, "key")
```

---

## get_modifier_key_ability_release_id_kv

method in GameAPI

- 描述

    获取魔法效果特效编号ABILITY_RELEASE_ID键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityReleaseId | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_ability_release_id_kv(modifier_key, "key")
```

---

## get_projectile_key_ability_release_id_kv

method in GameAPI

- 描述

    获取特效编号ABILITY_RELEASE_ID键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityReleaseId | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_ability_release_id_kv(projectile_key, "key")
```

---

## get_destructible_key_ability_release_id_kv

method in GameAPI

- 描述

    获取可破坏物编号ABILITY_RELEASE_ID键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityReleaseId | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_ability_release_id_kv(destructible_key, "key")
```

---

## get_tech_key_ability_release_id_kv

method in GameAPI

- 描述

    获取科技编号ABILITY_RELEASE_ID键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityReleaseId | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_ability_release_id_kv(tech_key, "key")
```

---

## get_icon_id_ability_release_id_kv

method in GameAPI

- 描述

    获取图片ABILITY_RELEASE_ID键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityReleaseId | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_ability_release_id_kv(1, "key")
```

---

## get_physics_entity_key_ability_release_id_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型ABILITY_RELEASE_ID键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityReleaseId | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_ability_release_id_kv(1, "key")
```

---

## get_kv_pair_value_ability_release_id

method in GameAPI

- 描述

    获取ABILITY_RELEASE_ID键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityReleaseId | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_ability_release_id(kvbase, "key")
```

---

## get_unit_key_slot_type_kv

method in GameAPI

- 描述

    获取单位编号SLOT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SlotType | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_slot_type_kv(unit_key, "key")
```

---

## get_item_key_slot_type_kv

method in GameAPI

- 描述

    获取物品编号SLOT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SlotType | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_slot_type_kv(item_key, "key")
```

---

## get_ability_key_slot_type_kv

method in GameAPI

- 描述

    获取技能编号SLOT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SlotType | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_slot_type_kv(ability_key, "key")
```

---

## get_modifier_key_slot_type_kv

method in GameAPI

- 描述

    获取魔法效果特效编号SLOT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SlotType | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_slot_type_kv(modifier_key, "key")
```

---

## get_projectile_key_slot_type_kv

method in GameAPI

- 描述

    获取特效编号SLOT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SlotType | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_slot_type_kv(projectile_key, "key")
```

---

## get_destructible_key_slot_type_kv

method in GameAPI

- 描述

    获取可破坏物编号SLOT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SlotType | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_slot_type_kv(destructible_key, "key")
```

---

## get_tech_key_slot_type_kv

method in GameAPI

- 描述

    获取科技编号SLOT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SlotType | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_slot_type_kv(tech_key, "key")
```

---

## get_icon_id_slot_type_kv

method in GameAPI

- 描述

    获取图片SLOT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SlotType | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_slot_type_kv(1, "key")
```

---

## get_physics_entity_key_slot_type_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型SLOT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SlotType | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_slot_type_kv(1, "key")
```

---

## get_kv_pair_value_slot_type

method in GameAPI

- 描述

    获取SLOT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SlotType | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_slot_type(kvbase, "key")
```

---

## get_unit_key_ui_point_kv

method in GameAPI

- 描述

    获取单位编号UI_POINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FUIPoint | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_ui_point_kv(unit_key, "key")
```

---

## get_item_key_ui_point_kv

method in GameAPI

- 描述

    获取物品编号UI_POINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FUIPoint | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_ui_point_kv(item_key, "key")
```

---

## get_ability_key_ui_point_kv

method in GameAPI

- 描述

    获取技能编号UI_POINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FUIPoint | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_ui_point_kv(ability_key, "key")
```

---

## get_modifier_key_ui_point_kv

method in GameAPI

- 描述

    获取魔法效果特效编号UI_POINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FUIPoint | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_ui_point_kv(modifier_key, "key")
```

---

## get_projectile_key_ui_point_kv

method in GameAPI

- 描述

    获取特效编号UI_POINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FUIPoint | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_ui_point_kv(projectile_key, "key")
```

---

## get_destructible_key_ui_point_kv

method in GameAPI

- 描述

    获取可破坏物编号UI_POINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FUIPoint | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_ui_point_kv(destructible_key, "key")
```

---

## get_tech_key_ui_point_kv

method in GameAPI

- 描述

    获取科技编号UI_POINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FUIPoint | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_ui_point_kv(tech_key, "key")
```

---

## get_icon_id_ui_point_kv

method in GameAPI

- 描述

    获取图片UI_POINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FUIPoint | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_ui_point_kv(1, "key")
```

---

## get_physics_entity_key_ui_point_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型UI_POINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FUIPoint | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_ui_point_kv(1, "key")
```

---

## get_kv_pair_value_ui_point

method in GameAPI

- 描述

    获取UI_POINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FUIPoint | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_ui_point(kvbase, "key")
```

---

## get_unit_key_attach_model_entity_kv

method in GameAPI

- 描述

    获取单位编号ATTACH_MODEL_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AttachModelEntity | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_attach_model_entity_kv(unit_key, "key")
```

---

## get_item_key_attach_model_entity_kv

method in GameAPI

- 描述

    获取物品编号ATTACH_MODEL_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AttachModelEntity | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_attach_model_entity_kv(item_key, "key")
```

---

## get_ability_key_attach_model_entity_kv

method in GameAPI

- 描述

    获取技能编号ATTACH_MODEL_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AttachModelEntity | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_attach_model_entity_kv(ability_key, "key")
```

---

## get_modifier_key_attach_model_entity_kv

method in GameAPI

- 描述

    获取魔法效果特效编号ATTACH_MODEL_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AttachModelEntity | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_attach_model_entity_kv(modifier_key, "key")
```

---

## get_projectile_key_attach_model_entity_kv

method in GameAPI

- 描述

    获取特效编号ATTACH_MODEL_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AttachModelEntity | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_attach_model_entity_kv(projectile_key, "key")
```

---

## get_destructible_key_attach_model_entity_kv

method in GameAPI

- 描述

    获取可破坏物编号ATTACH_MODEL_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AttachModelEntity | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_attach_model_entity_kv(destructible_key, "key")
```

---

## get_tech_key_attach_model_entity_kv

method in GameAPI

- 描述

    获取科技编号ATTACH_MODEL_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AttachModelEntity | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_attach_model_entity_kv(tech_key, "key")
```

---

## get_icon_id_attach_model_entity_kv

method in GameAPI

- 描述

    获取图片ATTACH_MODEL_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AttachModelEntity | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_attach_model_entity_kv(1, "key")
```

---

## get_physics_entity_key_attach_model_entity_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型ATTACH_MODEL_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AttachModelEntity | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_attach_model_entity_kv(1, "key")
```

---

## get_kv_pair_value_attach_model_entity

method in GameAPI

- 描述

    获取ATTACH_MODEL_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AttachModelEntity | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_attach_model_entity(kvbase, "key")
```

---

## get_unit_key_live2d_kv

method in GameAPI

- 描述

    获取单位编号LIVE2D键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Live2dKey | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_live2d_kv(unit_key, "key")
```

---

## get_item_key_live2d_kv

method in GameAPI

- 描述

    获取物品编号LIVE2D键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Live2dKey | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_live2d_kv(item_key, "key")
```

---

## get_ability_key_live2d_kv

method in GameAPI

- 描述

    获取技能编号LIVE2D键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Live2dKey | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_live2d_kv(ability_key, "key")
```

---

## get_modifier_key_live2d_kv

method in GameAPI

- 描述

    获取魔法效果特效编号LIVE2D键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Live2dKey | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_live2d_kv(modifier_key, "key")
```

---

## get_projectile_key_live2d_kv

method in GameAPI

- 描述

    获取特效编号LIVE2D键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Live2dKey | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_live2d_kv(projectile_key, "key")
```

---

## get_destructible_key_live2d_kv

method in GameAPI

- 描述

    获取可破坏物编号LIVE2D键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Live2dKey | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_live2d_kv(destructible_key, "key")
```

---

## get_tech_key_live2d_kv

method in GameAPI

- 描述

    获取科技编号LIVE2D键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Live2dKey | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_live2d_kv(tech_key, "key")
```

---

## get_icon_id_live2d_kv

method in GameAPI

- 描述

    获取图片LIVE2D键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Live2dKey | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_live2d_kv(1, "key")
```

---

## get_physics_entity_key_live2d_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型LIVE2D键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Live2dKey | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_live2d_kv(1, "key")
```

---

## get_kv_pair_value_live2d

method in GameAPI

- 描述

    获取LIVE2D键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Live2dKey | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_live2d(kvbase, "key")
```

---

## get_unit_key_spine_kv

method in GameAPI

- 描述

    获取单位编号SPINE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Spine | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_spine_kv(unit_key, "key")
```

---

## get_item_key_spine_kv

method in GameAPI

- 描述

    获取物品编号SPINE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Spine | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_spine_kv(item_key, "key")
```

---

## get_ability_key_spine_kv

method in GameAPI

- 描述

    获取技能编号SPINE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Spine | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_spine_kv(ability_key, "key")
```

---

## get_modifier_key_spine_kv

method in GameAPI

- 描述

    获取魔法效果特效编号SPINE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Spine | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_spine_kv(modifier_key, "key")
```

---

## get_projectile_key_spine_kv

method in GameAPI

- 描述

    获取特效编号SPINE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Spine | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_spine_kv(projectile_key, "key")
```

---

## get_destructible_key_spine_kv

method in GameAPI

- 描述

    获取可破坏物编号SPINE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Spine | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_spine_kv(destructible_key, "key")
```

---

## get_tech_key_spine_kv

method in GameAPI

- 描述

    获取科技编号SPINE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Spine | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_spine_kv(tech_key, "key")
```

---

## get_icon_id_spine_kv

method in GameAPI

- 描述

    获取图片SPINE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Spine | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_spine_kv(1, "key")
```

---

## get_physics_entity_key_spine_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型SPINE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Spine | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_spine_kv(1, "key")
```

---

## get_kv_pair_value_spine

method in GameAPI

- 描述

    获取SPINE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Spine | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_spine(kvbase, "key")
```

---

## get_unit_key_force_entity_kv

method in GameAPI

- 描述

    获取单位编号FORCE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Force | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_force_entity_kv(unit_key, "key")
```

---

## get_item_key_force_entity_kv

method in GameAPI

- 描述

    获取物品编号FORCE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Force | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_force_entity_kv(item_key, "key")
```

---

## get_ability_key_force_entity_kv

method in GameAPI

- 描述

    获取技能编号FORCE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Force | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_force_entity_kv(ability_key, "key")
```

---

## get_modifier_key_force_entity_kv

method in GameAPI

- 描述

    获取魔法效果特效编号FORCE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Force | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_force_entity_kv(modifier_key, "key")
```

---

## get_projectile_key_force_entity_kv

method in GameAPI

- 描述

    获取特效编号FORCE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Force | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_force_entity_kv(projectile_key, "key")
```

---

## get_destructible_key_force_entity_kv

method in GameAPI

- 描述

    获取可破坏物编号FORCE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Force | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_force_entity_kv(destructible_key, "key")
```

---

## get_tech_key_force_entity_kv

method in GameAPI

- 描述

    获取科技编号FORCE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Force | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_force_entity_kv(tech_key, "key")
```

---

## get_icon_id_force_entity_kv

method in GameAPI

- 描述

    获取图片FORCE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Force | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_force_entity_kv(1, "key")
```

---

## get_physics_entity_key_force_entity_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型FORCE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Force | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_force_entity_kv(1, "key")
```

---

## get_kv_pair_value_force_entity

method in GameAPI

- 描述

    获取FORCE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Force | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_force_entity(kvbase, "key")
```

---

## get_unit_key_goods_key_kv

method in GameAPI

- 描述

    获取单位编号GOODS_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.GoodsKey | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_goods_key_kv(unit_key, "key")
```

---

## get_item_key_goods_key_kv

method in GameAPI

- 描述

    获取物品编号GOODS_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.GoodsKey | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_goods_key_kv(item_key, "key")
```

---

## get_ability_key_goods_key_kv

method in GameAPI

- 描述

    获取技能编号GOODS_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.GoodsKey | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_goods_key_kv(ability_key, "key")
```

---

## get_modifier_key_goods_key_kv

method in GameAPI

- 描述

    获取魔法效果特效编号GOODS_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.GoodsKey | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_goods_key_kv(modifier_key, "key")
```

---

## get_projectile_key_goods_key_kv

method in GameAPI

- 描述

    获取特效编号GOODS_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.GoodsKey | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_goods_key_kv(projectile_key, "key")
```

---

## get_destructible_key_goods_key_kv

method in GameAPI

- 描述

    获取可破坏物编号GOODS_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.GoodsKey | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_goods_key_kv(destructible_key, "key")
```

---

## get_tech_key_goods_key_kv

method in GameAPI

- 描述

    获取科技编号GOODS_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.GoodsKey | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_goods_key_kv(tech_key, "key")
```

---

## get_icon_id_goods_key_kv

method in GameAPI

- 描述

    获取图片GOODS_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.GoodsKey | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_goods_key_kv(1, "key")
```

---

## get_physics_entity_key_goods_key_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型GOODS_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.GoodsKey | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_goods_key_kv(1, "key")
```

---

## get_kv_pair_value_goods_key

method in GameAPI

- 描述

    获取GOODS_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.GoodsKey | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_goods_key(kvbase, "key")
```

---

## get_unit_key_mouse_key_without_middle_kv

method in GameAPI

- 描述

    获取单位编号MOUSE_KEY_WITHOUT_MIDDLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MouseKeyWithoutMiddle | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_mouse_key_without_middle_kv(unit_key, "key")
```

---

## get_item_key_mouse_key_without_middle_kv

method in GameAPI

- 描述

    获取物品编号MOUSE_KEY_WITHOUT_MIDDLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MouseKeyWithoutMiddle | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_mouse_key_without_middle_kv(item_key, "key")
```

---

## get_ability_key_mouse_key_without_middle_kv

method in GameAPI

- 描述

    获取技能编号MOUSE_KEY_WITHOUT_MIDDLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MouseKeyWithoutMiddle | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_mouse_key_without_middle_kv(ability_key, "key")
```

---

## get_modifier_key_mouse_key_without_middle_kv

method in GameAPI

- 描述

    获取魔法效果特效编号MOUSE_KEY_WITHOUT_MIDDLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MouseKeyWithoutMiddle | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_mouse_key_without_middle_kv(modifier_key, "key")
```

---

## get_projectile_key_mouse_key_without_middle_kv

method in GameAPI

- 描述

    获取特效编号MOUSE_KEY_WITHOUT_MIDDLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MouseKeyWithoutMiddle | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_mouse_key_without_middle_kv(projectile_key, "key")
```

---

## get_destructible_key_mouse_key_without_middle_kv

method in GameAPI

- 描述

    获取可破坏物编号MOUSE_KEY_WITHOUT_MIDDLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MouseKeyWithoutMiddle | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_mouse_key_without_middle_kv(destructible_key, "key")
```

---

## get_tech_key_mouse_key_without_middle_kv

method in GameAPI

- 描述

    获取科技编号MOUSE_KEY_WITHOUT_MIDDLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MouseKeyWithoutMiddle | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_mouse_key_without_middle_kv(tech_key, "key")
```

---

## get_icon_id_mouse_key_without_middle_kv

method in GameAPI

- 描述

    获取图片MOUSE_KEY_WITHOUT_MIDDLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MouseKeyWithoutMiddle | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_mouse_key_without_middle_kv(1, "key")
```

---

## get_physics_entity_key_mouse_key_without_middle_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型MOUSE_KEY_WITHOUT_MIDDLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MouseKeyWithoutMiddle | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_mouse_key_without_middle_kv(1, "key")
```

---

## get_kv_pair_value_mouse_key_without_middle

method in GameAPI

- 描述

    获取MOUSE_KEY_WITHOUT_MIDDLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MouseKeyWithoutMiddle | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_mouse_key_without_middle(kvbase, "key")
```

---

## get_unit_key_map_kv

method in GameAPI

- 描述

    获取单位编号MAP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Map | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_map_kv(unit_key, "key")
```

---

## get_item_key_map_kv

method in GameAPI

- 描述

    获取物品编号MAP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Map | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_map_kv(item_key, "key")
```

---

## get_ability_key_map_kv

method in GameAPI

- 描述

    获取技能编号MAP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Map | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_map_kv(ability_key, "key")
```

---

## get_modifier_key_map_kv

method in GameAPI

- 描述

    获取魔法效果特效编号MAP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Map | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_map_kv(modifier_key, "key")
```

---

## get_projectile_key_map_kv

method in GameAPI

- 描述

    获取特效编号MAP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Map | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_map_kv(projectile_key, "key")
```

---

## get_destructible_key_map_kv

method in GameAPI

- 描述

    获取可破坏物编号MAP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Map | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_map_kv(destructible_key, "key")
```

---

## get_tech_key_map_kv

method in GameAPI

- 描述

    获取科技编号MAP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Map | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_map_kv(tech_key, "key")
```

---

## get_icon_id_map_kv

method in GameAPI

- 描述

    获取图片MAP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Map | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_map_kv(1, "key")
```

---

## get_physics_entity_key_map_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型MAP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Map | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_map_kv(1, "key")
```

---

## get_kv_pair_value_map

method in GameAPI

- 描述

    获取MAP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Map | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_map(kvbase, "key")
```

---

## get_unit_key_unit_group_command_type_kv

method in GameAPI

- 描述

    获取单位编号UNIT_GROUP_COMMAND_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitGroupCommandType | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_unit_group_command_type_kv(unit_key, "key")
```

---
