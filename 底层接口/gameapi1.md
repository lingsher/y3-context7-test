---
sidebarDepth: 1
---
# GameAPI (Part 1)

# 索引

Y3 编辑器 GameAPI 接口集合（第 1 部分），包含游戏核心功能。

---

| 接口 | 描述 |
| --- | --- |
| [del_unit_key_kv](#del_unit_key_kv) | 预设库单位删除键值对 |
| [del_ability_key_kv](#del_ability_key_kv) | 预设库技能删除键值对 |
| [del_item_key_kv](#del_item_key_kv) | 预设库物品删除键值对 |
| [del_prefab_key_kv](#del_prefab_key_kv) | 预设库物品删除键值对 |
| [add_boolean_kv](#add_boolean_kv) | 添加BOOLEAN键值对 |
| [add_integer_kv](#add_integer_kv) | 添加INTEGER键值对 |
| [add_float_kv](#add_float_kv) | 添加FLOAT键值对 |
| [add_string_kv](#add_string_kv) | 添加STRING键值对 |
| [add_ui_comp_kv](#add_ui_comp_kv) | 添加UI_COMP键值对 |
| [add_ui_comp_type_kv](#add_ui_comp_type_kv) | 添加UI_COMP_TYPE键值对 |
| [add_ui_comp_event_type_kv](#add_ui_comp_event_type_kv) | 添加UI_COMP_EVENT_TYPE键值对 |
| [add_ui_comp_attr_kv](#add_ui_comp_attr_kv) | 添加UI_COMP_ATTR键值对 |
| [add_ui_comp_align_type_kv](#add_ui_comp_align_type_kv) | 添加UI_COMP_ALIGN_TYPE键值对 |
| [add_ui_prefab_kv](#add_ui_prefab_kv) | 添加UI_PREFAB键值对 |
| [add_ui_prefab_instance_kv](#add_ui_prefab_instance_kv) | 添加UI_PREFAB_INSTANCE键值对 |
| [add_ui_prefab_ins_uid_kv](#add_ui_prefab_ins_uid_kv) | 添加UI_PREFAB_INS_UID键值对 |
| [add_ui_direction_kv](#add_ui_direction_kv) | 添加UI_DIRECTION键值对 |
| [add_ui_model_camera_mod_kv](#add_ui_model_camera_mod_kv) | 添加UI_MODEL_CAMERA_MOD键值对 |
| [add_ui_btn_status_kv](#add_ui_btn_status_kv) | 添加UI_BTN_STATUS键值对 |
| [add_ui_scrollview_type_kv](#add_ui_scrollview_type_kv) | 添加UI_SCROLLVIEW_TYPE键值对 |
| [add_ui_anim_kv](#add_ui_anim_kv) | 添加UI_ANIM键值对 |
| [add_ui_anim_curve_kv](#add_ui_anim_curve_kv) | 添加UI_ANIM_CURVE键值对 |
| [add_audio_channel_kv](#add_audio_channel_kv) | 添加AUDIO_CHANNEL键值对 |
| [add_unit_entity_kv](#add_unit_entity_kv) | 添加UNIT_ENTITY键值对 |
| [add_unit_group_kv](#add_unit_group_kv) | 添加UNIT_GROUP键值对 |
| [add_unit_name_kv](#add_unit_name_kv) | 添加UNIT_NAME键值对 |
| [add_unit_name_pool_kv](#add_unit_name_pool_kv) | 添加UNIT_NAME_POOL键值对 |
| [add_unit_write_attribute_kv](#add_unit_write_attribute_kv) | 添加UNIT_WRITE_ATTRIBUTE键值对 |
| [add_attr_element_kv](#add_attr_element_kv) | 添加ATTR_ELEMENT键值对 |
| [add_attr_element_read_kv](#add_attr_element_read_kv) | 添加ATTR_ELEMENT_READ键值对 |
| [add_mover_entity_kv](#add_mover_entity_kv) | 添加MOVER_ENTITY键值对 |
| [add_image_quality_kv](#add_image_quality_kv) | 添加IMAGE_QUALITY键值对 |
| [add_window_type_setting_kv](#add_window_type_setting_kv) | 添加WINDOW_TYPE_SETTING键值对 |
| [add_item_entity_kv](#add_item_entity_kv) | 添加ITEM_ENTITY键值对 |
| [add_item_group_kv](#add_item_group_kv) | 添加ITEM_GROUP键值对 |
| [add_item_name_kv](#add_item_name_kv) | 添加ITEM_NAME键值对 |
| [add_ability_kv](#add_ability_kv) | 添加ABILITY键值对 |
| [add_ability_type_kv](#add_ability_type_kv) | 添加ABILITY_TYPE键值对 |
| [add_ability_cast_type_kv](#add_ability_cast_type_kv) | 添加ABILITY_CAST_TYPE键值对 |
| [add_ability_name_kv](#add_ability_name_kv) | 添加ABILITY_NAME键值对 |
| [add_skill_pointer_type_kv](#add_skill_pointer_type_kv) | 添加SKILL_POINTER_TYPE键值对 |
| [add_modifier_entity_kv](#add_modifier_entity_kv) | 添加MODIFIER_ENTITY键值对 |
| [add_modifier_type_kv](#add_modifier_type_kv) | 添加MODIFIER_TYPE键值对 |
| [add_modifier_effect_type_kv](#add_modifier_effect_type_kv) | 添加MODIFIER_EFFECT_TYPE键值对 |
| [add_modifier_kv](#add_modifier_kv) | 添加MODIFIER键值对 |
| [add_projectile_kv](#add_projectile_kv) | 添加PROJECTILE键值对 |
| [add_projectile_entity_kv](#add_projectile_entity_kv) | 添加PROJECTILE_ENTITY键值对 |
| [add_projectile_group_kv](#add_projectile_group_kv) | 添加PROJECTILE_GROUP键值对 |
| [add_destructible_entity_kv](#add_destructible_entity_kv) | 添加DESTRUCTIBLE_ENTITY键值对 |
| [add_destructible_name_kv](#add_destructible_name_kv) | 添加DESTRUCTIBLE_NAME键值对 |
| [add_sound_entity_kv](#add_sound_entity_kv) | 添加SOUND_ENTITY键值对 |
| [add_audio_key_kv](#add_audio_key_kv) | 添加AUDIO_KEY键值对 |
| [add_game_mode_kv](#add_game_mode_kv) | 添加GAME_MODE键值对 |
| [add_player_kv](#add_player_kv) | 添加PLAYER键值对 |
| [add_player_group_kv](#add_player_group_kv) | 添加PLAYER_GROUP键值对 |
| [add_role_res_key_kv](#add_role_res_key_kv) | 添加ROLE_RES_KEY键值对 |
| [add_role_status_kv](#add_role_status_kv) | 添加ROLE_STATUS键值对 |
| [add_role_type_kv](#add_role_type_kv) | 添加ROLE_TYPE键值对 |
| [add_role_relation_kv](#add_role_relation_kv) | 添加ROLE_RELATION键值对 |
| [add_team_kv](#add_team_kv) | 添加TEAM键值对 |
| [add_point_kv](#add_point_kv) | 添加POINT键值对 |
| [add_vector3_kv](#add_vector3_kv) | 添加VECTOR3键值对 |
| [add_rotation_kv](#add_rotation_kv) | 添加ROTATION键值对 |
| [add_point_list_kv](#add_point_list_kv) | 添加POINT_LIST键值对 |
| [add_rectangle_kv](#add_rectangle_kv) | 添加RECTANGLE键值对 |
| [add_round_area_kv](#add_round_area_kv) | 添加ROUND_AREA键值对 |
| [add_polygon_kv](#add_polygon_kv) | 添加POLYGON键值对 |
| [add_camera_kv](#add_camera_kv) | 添加CAMERA键值对 |
| [add_camline_kv](#add_camline_kv) | 添加CAMLINE键值对 |
| [add_point_light_kv](#add_point_light_kv) | 添加POINT_LIGHT键值对 |
| [add_spot_light_kv](#add_spot_light_kv) | 添加SPOT_LIGHT键值对 |
| [add_fog_kv](#add_fog_kv) | 添加FOG键值对 |
| [add_scene_sound_kv](#add_scene_sound_kv) | 添加SCENE_SOUND键值对 |
| [add_model_kv](#add_model_kv) | 添加MODEL键值对 |
| [add_sfx_entity_kv](#add_sfx_entity_kv) | 添加SFX_ENTITY键值对 |
| [add_sfx_key_kv](#add_sfx_key_kv) | 添加SFX_KEY键值对 |
| [add_link_sfx_entity_kv](#add_link_sfx_entity_kv) | 添加LINK_SFX_ENTITY键值对 |
| [add_link_sfx_key_kv](#add_link_sfx_key_kv) | 添加LINK_SFX_KEY键值对 |
| [add_cursor_key_kv](#add_cursor_key_kv) | 添加CURSOR_KEY键值对 |
| [add_angle_kv](#add_angle_kv) | 添加ANGLE键值对 |
| [add_texture_kv](#add_texture_kv) | 添加TEXTURE键值对 |
| [add_sequence_kv](#add_sequence_kv) | 添加SEQUENCE键值对 |
| [add_physics_object_kv](#add_physics_object_kv) | 添加PHYSICS_OBJECT键值对 |
| [add_physics_entity_kv](#add_physics_entity_kv) | 添加PHYSICS_ENTITY键值对 |
| [add_physics_object_key_kv](#add_physics_object_key_kv) | 添加PHYSICS_OBJECT_KEY键值对 |
| [add_physics_entity_key_kv](#add_physics_entity_key_kv) | 添加PHYSICS_ENTITY_KEY键值对 |
| [add_rigid_body_kv](#add_rigid_body_kv) | 添加RIGID_BODY键值对 |
| [add_rigid_body_group_kv](#add_rigid_body_group_kv) | 添加RIGID_BODY_GROUP键值对 |
| [add_collider_kv](#add_collider_kv) | 添加COLLIDER键值对 |
| [add_joint_kv](#add_joint_kv) | 添加JOINT键值对 |
| [add_reaction_kv](#add_reaction_kv) | 添加REACTION键值对 |
| [add_reaction_group_kv](#add_reaction_group_kv) | 添加REACTION_GROUP键值对 |
| [add_dynamic_trigger_instance_kv](#add_dynamic_trigger_instance_kv) | 添加DYNAMIC_TRIGGER_INSTANCE键值对 |
| [add_table_kv](#add_table_kv) | 添加TABLE键值对 |
| [add_random_pool_kv](#add_random_pool_kv) | 添加RANDOM_POOL键值对 |
| [add_scene_ui_kv](#add_scene_ui_kv) | 添加SCENE_UI键值对 |
| [add_damage_type_kv](#add_damage_type_kv) | 添加DAMAGE_TYPE键值对 |
| [add_harm_text_type_new_kv](#add_harm_text_type_new_kv) | 添加HARM_TEXT_TYPE_NEW键值对 |
| [add_font_type_kv](#add_font_type_kv) | 添加FONT_TYPE键值对 |
| [add_jump_word_track_kv](#add_jump_word_track_kv) | 添加JUMP_WORD_TRACK键值对 |
| [add_new_timer_kv](#add_new_timer_kv) | 添加NEW_TIMER键值对 |
| [add_tech_key_kv](#add_tech_key_kv) | 添加TECH_KEY键值对 |
| [add_store_key_kv](#add_store_key_kv) | 添加STORE_KEY键值对 |
| [add_keyboard_key_kv](#add_keyboard_key_kv) | 添加KEYBOARD_KEY键值对 |
| [add_func_keyboard_key_kv](#add_func_keyboard_key_kv) | 添加FUNC_KEYBOARD_KEY键值对 |
| [add_mouse_key_kv](#add_mouse_key_kv) | 添加MOUSE_KEY键值对 |
| [add_mouse_wheel_kv](#add_mouse_wheel_kv) | 添加MOUSE_WHEEL键值对 |
| [add_post_effect_kv](#add_post_effect_kv) | 添加POST_EFFECT键值对 |
| [add_unit_type_kv](#add_unit_type_kv) | 添加UNIT_TYPE键值对 |
| [add_unit_command_type_kv](#add_unit_command_type_kv) | 添加UNIT_COMMAND_TYPE键值对 |
| [add_mini_map_color_type_kv](#add_mini_map_color_type_kv) | 添加MINI_MAP_COLOR_TYPE键值对 |
| [add_unit_behavior_kv](#add_unit_behavior_kv) | 添加UNIT_BEHAVIOR键值对 |
| [add_curved_path_kv](#add_curved_path_kv) | 添加CURVED_PATH键值对 |
| [add_curved_path_3d_kv](#add_curved_path_3d_kv) | 添加CURVED_PATH_3D键值对 |
| [has_kv_pair](#has_kv_pair) | 判断是否存在键值对(忽略类型) |
| [has_prefab_kv_any](#has_prefab_kv_any) | 判断预设类型是否存在键值对(忽略类型) |
| [has_kv_pair_boolean](#has_kv_pair_boolean) | 判断是否存在BOOLEAN键值对 |
| [has_unit_key_boolean_kv](#has_unit_key_boolean_kv) | 判断单位编号是否存在BOOLEAN键值对 |
| [has_item_key_boolean_kv](#has_item_key_boolean_kv) | 判断物品编号是否存在BOOLEAN键值对 |
| [has_ability_key_boolean_kv](#has_ability_key_boolean_kv) | 判断技能编号是否存在BOOLEAN键值对 |
| [has_kv_pair_integer](#has_kv_pair_integer) | 判断是否存在INTEGER键值对 |
| [has_unit_key_integer_kv](#has_unit_key_integer_kv) | 判断单位编号是否存在INTEGER键值对 |
| [has_item_key_integer_kv](#has_item_key_integer_kv) | 判断物品编号是否存在INTEGER键值对 |
| [has_ability_key_integer_kv](#has_ability_key_integer_kv) | 判断技能编号是否存在INTEGER键值对 |
| [has_kv_pair_float](#has_kv_pair_float) | 判断是否存在FLOAT键值对 |
| [has_unit_key_float_kv](#has_unit_key_float_kv) | 判断单位编号是否存在FLOAT键值对 |
| [has_item_key_float_kv](#has_item_key_float_kv) | 判断物品编号是否存在FLOAT键值对 |
| [has_ability_key_float_kv](#has_ability_key_float_kv) | 判断技能编号是否存在FLOAT键值对 |
| [has_kv_pair_string](#has_kv_pair_string) | 判断是否存在STRING键值对 |
| [has_unit_key_string_kv](#has_unit_key_string_kv) | 判断单位编号是否存在STRING键值对 |
| [has_item_key_string_kv](#has_item_key_string_kv) | 判断物品编号是否存在STRING键值对 |
| [has_ability_key_string_kv](#has_ability_key_string_kv) | 判断技能编号是否存在STRING键值对 |
| [has_kv_pair_ui_comp](#has_kv_pair_ui_comp) | 判断是否存在UI_COMP键值对 |
| [has_unit_key_ui_comp_kv](#has_unit_key_ui_comp_kv) | 判断单位编号是否存在UI_COMP键值对 |
| [has_item_key_ui_comp_kv](#has_item_key_ui_comp_kv) | 判断物品编号是否存在UI_COMP键值对 |
| [has_ability_key_ui_comp_kv](#has_ability_key_ui_comp_kv) | 判断技能编号是否存在UI_COMP键值对 |
| [has_kv_pair_ui_comp_type](#has_kv_pair_ui_comp_type) | 判断是否存在UI_COMP_TYPE键值对 |
| [has_unit_key_ui_comp_type_kv](#has_unit_key_ui_comp_type_kv) | 判断单位编号是否存在UI_COMP_TYPE键值对 |
| [has_item_key_ui_comp_type_kv](#has_item_key_ui_comp_type_kv) | 判断物品编号是否存在UI_COMP_TYPE键值对 |
| [has_ability_key_ui_comp_type_kv](#has_ability_key_ui_comp_type_kv) | 判断技能编号是否存在UI_COMP_TYPE键值对 |
| [has_kv_pair_ui_comp_event_type](#has_kv_pair_ui_comp_event_type) | 判断是否存在UI_COMP_EVENT_TYPE键值对 |
| [has_unit_key_ui_comp_event_type_kv](#has_unit_key_ui_comp_event_type_kv) | 判断单位编号是否存在UI_COMP_EVENT_TYPE键值对 |
| [has_item_key_ui_comp_event_type_kv](#has_item_key_ui_comp_event_type_kv) | 判断物品编号是否存在UI_COMP_EVENT_TYPE键值对 |
| [has_ability_key_ui_comp_event_type_kv](#has_ability_key_ui_comp_event_type_kv) | 判断技能编号是否存在UI_COMP_EVENT_TYPE键值对 |
| [has_kv_pair_ui_comp_attr](#has_kv_pair_ui_comp_attr) | 判断是否存在UI_COMP_ATTR键值对 |
| [has_unit_key_ui_comp_attr_kv](#has_unit_key_ui_comp_attr_kv) | 判断单位编号是否存在UI_COMP_ATTR键值对 |
| [has_item_key_ui_comp_attr_kv](#has_item_key_ui_comp_attr_kv) | 判断物品编号是否存在UI_COMP_ATTR键值对 |
| [has_ability_key_ui_comp_attr_kv](#has_ability_key_ui_comp_attr_kv) | 判断技能编号是否存在UI_COMP_ATTR键值对 |
| [has_kv_pair_ui_comp_align_type](#has_kv_pair_ui_comp_align_type) | 判断是否存在UI_COMP_ALIGN_TYPE键值对 |
| [has_unit_key_ui_comp_align_type_kv](#has_unit_key_ui_comp_align_type_kv) | 判断单位编号是否存在UI_COMP_ALIGN_TYPE键值对 |
| [has_item_key_ui_comp_align_type_kv](#has_item_key_ui_comp_align_type_kv) | 判断物品编号是否存在UI_COMP_ALIGN_TYPE键值对 |
| [has_ability_key_ui_comp_align_type_kv](#has_ability_key_ui_comp_align_type_kv) | 判断技能编号是否存在UI_COMP_ALIGN_TYPE键值对 |
| [has_kv_pair_ui_prefab](#has_kv_pair_ui_prefab) | 判断是否存在UI_PREFAB键值对 |
| [has_unit_key_ui_prefab_kv](#has_unit_key_ui_prefab_kv) | 判断单位编号是否存在UI_PREFAB键值对 |
| [has_item_key_ui_prefab_kv](#has_item_key_ui_prefab_kv) | 判断物品编号是否存在UI_PREFAB键值对 |
| [has_ability_key_ui_prefab_kv](#has_ability_key_ui_prefab_kv) | 判断技能编号是否存在UI_PREFAB键值对 |
| [has_kv_pair_ui_prefab_instance](#has_kv_pair_ui_prefab_instance) | 判断是否存在UI_PREFAB_INSTANCE键值对 |
| [has_unit_key_ui_prefab_instance_kv](#has_unit_key_ui_prefab_instance_kv) | 判断单位编号是否存在UI_PREFAB_INSTANCE键值对 |
| [has_item_key_ui_prefab_instance_kv](#has_item_key_ui_prefab_instance_kv) | 判断物品编号是否存在UI_PREFAB_INSTANCE键值对 |
| [has_ability_key_ui_prefab_instance_kv](#has_ability_key_ui_prefab_instance_kv) | 判断技能编号是否存在UI_PREFAB_INSTANCE键值对 |
| [has_kv_pair_ui_prefab_ins_uid](#has_kv_pair_ui_prefab_ins_uid) | 判断是否存在UI_PREFAB_INS_UID键值对 |
| [has_unit_key_ui_prefab_ins_uid_kv](#has_unit_key_ui_prefab_ins_uid_kv) | 判断单位编号是否存在UI_PREFAB_INS_UID键值对 |
| [has_item_key_ui_prefab_ins_uid_kv](#has_item_key_ui_prefab_ins_uid_kv) | 判断物品编号是否存在UI_PREFAB_INS_UID键值对 |
| [has_ability_key_ui_prefab_ins_uid_kv](#has_ability_key_ui_prefab_ins_uid_kv) | 判断技能编号是否存在UI_PREFAB_INS_UID键值对 |
| [has_kv_pair_ui_direction](#has_kv_pair_ui_direction) | 判断是否存在UI_DIRECTION键值对 |
| [has_unit_key_ui_direction_kv](#has_unit_key_ui_direction_kv) | 判断单位编号是否存在UI_DIRECTION键值对 |
| [has_item_key_ui_direction_kv](#has_item_key_ui_direction_kv) | 判断物品编号是否存在UI_DIRECTION键值对 |
| [has_ability_key_ui_direction_kv](#has_ability_key_ui_direction_kv) | 判断技能编号是否存在UI_DIRECTION键值对 |
| [has_kv_pair_ui_model_camera_mod](#has_kv_pair_ui_model_camera_mod) | 判断是否存在UI_MODEL_CAMERA_MOD键值对 |
| [has_unit_key_ui_model_camera_mod_kv](#has_unit_key_ui_model_camera_mod_kv) | 判断单位编号是否存在UI_MODEL_CAMERA_MOD键值对 |
| [has_item_key_ui_model_camera_mod_kv](#has_item_key_ui_model_camera_mod_kv) | 判断物品编号是否存在UI_MODEL_CAMERA_MOD键值对 |
| [has_ability_key_ui_model_camera_mod_kv](#has_ability_key_ui_model_camera_mod_kv) | 判断技能编号是否存在UI_MODEL_CAMERA_MOD键值对 |
| [has_kv_pair_ui_btn_status](#has_kv_pair_ui_btn_status) | 判断是否存在UI_BTN_STATUS键值对 |
| [has_unit_key_ui_btn_status_kv](#has_unit_key_ui_btn_status_kv) | 判断单位编号是否存在UI_BTN_STATUS键值对 |
| [has_item_key_ui_btn_status_kv](#has_item_key_ui_btn_status_kv) | 判断物品编号是否存在UI_BTN_STATUS键值对 |
| [has_ability_key_ui_btn_status_kv](#has_ability_key_ui_btn_status_kv) | 判断技能编号是否存在UI_BTN_STATUS键值对 |
| [has_kv_pair_ui_scrollview_type](#has_kv_pair_ui_scrollview_type) | 判断是否存在UI_SCROLLVIEW_TYPE键值对 |
| [has_unit_key_ui_scrollview_type_kv](#has_unit_key_ui_scrollview_type_kv) | 判断单位编号是否存在UI_SCROLLVIEW_TYPE键值对 |
| [has_item_key_ui_scrollview_type_kv](#has_item_key_ui_scrollview_type_kv) | 判断物品编号是否存在UI_SCROLLVIEW_TYPE键值对 |
| [has_ability_key_ui_scrollview_type_kv](#has_ability_key_ui_scrollview_type_kv) | 判断技能编号是否存在UI_SCROLLVIEW_TYPE键值对 |
| [has_kv_pair_ui_anim](#has_kv_pair_ui_anim) | 判断是否存在UI_ANIM键值对 |
| [has_unit_key_ui_anim_kv](#has_unit_key_ui_anim_kv) | 判断单位编号是否存在UI_ANIM键值对 |
| [has_item_key_ui_anim_kv](#has_item_key_ui_anim_kv) | 判断物品编号是否存在UI_ANIM键值对 |
| [has_ability_key_ui_anim_kv](#has_ability_key_ui_anim_kv) | 判断技能编号是否存在UI_ANIM键值对 |
| [has_kv_pair_ui_anim_curve](#has_kv_pair_ui_anim_curve) | 判断是否存在UI_ANIM_CURVE键值对 |
| [has_unit_key_ui_anim_curve_kv](#has_unit_key_ui_anim_curve_kv) | 判断单位编号是否存在UI_ANIM_CURVE键值对 |
| [has_item_key_ui_anim_curve_kv](#has_item_key_ui_anim_curve_kv) | 判断物品编号是否存在UI_ANIM_CURVE键值对 |
| [has_ability_key_ui_anim_curve_kv](#has_ability_key_ui_anim_curve_kv) | 判断技能编号是否存在UI_ANIM_CURVE键值对 |
| [has_kv_pair_audio_channel](#has_kv_pair_audio_channel) | 判断是否存在AUDIO_CHANNEL键值对 |
| [has_unit_key_audio_channel_kv](#has_unit_key_audio_channel_kv) | 判断单位编号是否存在AUDIO_CHANNEL键值对 |
| [has_item_key_audio_channel_kv](#has_item_key_audio_channel_kv) | 判断物品编号是否存在AUDIO_CHANNEL键值对 |
| [has_ability_key_audio_channel_kv](#has_ability_key_audio_channel_kv) | 判断技能编号是否存在AUDIO_CHANNEL键值对 |
| [has_kv_pair_unit_entity](#has_kv_pair_unit_entity) | 判断是否存在UNIT_ENTITY键值对 |
| [has_unit_key_unit_entity_kv](#has_unit_key_unit_entity_kv) | 判断单位编号是否存在UNIT_ENTITY键值对 |
| [has_item_key_unit_entity_kv](#has_item_key_unit_entity_kv) | 判断物品编号是否存在UNIT_ENTITY键值对 |
| [has_ability_key_unit_entity_kv](#has_ability_key_unit_entity_kv) | 判断技能编号是否存在UNIT_ENTITY键值对 |
| [has_kv_pair_unit_group](#has_kv_pair_unit_group) | 判断是否存在UNIT_GROUP键值对 |
| [has_unit_key_unit_group_kv](#has_unit_key_unit_group_kv) | 判断单位编号是否存在UNIT_GROUP键值对 |
| [has_item_key_unit_group_kv](#has_item_key_unit_group_kv) | 判断物品编号是否存在UNIT_GROUP键值对 |
| [has_ability_key_unit_group_kv](#has_ability_key_unit_group_kv) | 判断技能编号是否存在UNIT_GROUP键值对 |
| [has_kv_pair_unit_name](#has_kv_pair_unit_name) | 判断是否存在UNIT_NAME键值对 |
| [has_unit_key_unit_name_kv](#has_unit_key_unit_name_kv) | 判断单位编号是否存在UNIT_NAME键值对 |
| [has_item_key_unit_name_kv](#has_item_key_unit_name_kv) | 判断物品编号是否存在UNIT_NAME键值对 |
| [has_ability_key_unit_name_kv](#has_ability_key_unit_name_kv) | 判断技能编号是否存在UNIT_NAME键值对 |
| [has_kv_pair_unit_name_pool](#has_kv_pair_unit_name_pool) | 判断是否存在UNIT_NAME_POOL键值对 |
| [has_unit_key_unit_name_pool_kv](#has_unit_key_unit_name_pool_kv) | 判断单位编号是否存在UNIT_NAME_POOL键值对 |
| [has_item_key_unit_name_pool_kv](#has_item_key_unit_name_pool_kv) | 判断物品编号是否存在UNIT_NAME_POOL键值对 |
| [has_ability_key_unit_name_pool_kv](#has_ability_key_unit_name_pool_kv) | 判断技能编号是否存在UNIT_NAME_POOL键值对 |
| [has_kv_pair_unit_write_attribute](#has_kv_pair_unit_write_attribute) | 判断是否存在UNIT_WRITE_ATTRIBUTE键值对 |
| [has_unit_key_unit_write_attribute_kv](#has_unit_key_unit_write_attribute_kv) | 判断单位编号是否存在UNIT_WRITE_ATTRIBUTE键值对 |
| [has_item_key_unit_write_attribute_kv](#has_item_key_unit_write_attribute_kv) | 判断物品编号是否存在UNIT_WRITE_ATTRIBUTE键值对 |
| [has_ability_key_unit_write_attribute_kv](#has_ability_key_unit_write_attribute_kv) | 判断技能编号是否存在UNIT_WRITE_ATTRIBUTE键值对 |
| [has_kv_pair_attr_element](#has_kv_pair_attr_element) | 判断是否存在ATTR_ELEMENT键值对 |
| [has_unit_key_attr_element_kv](#has_unit_key_attr_element_kv) | 判断单位编号是否存在ATTR_ELEMENT键值对 |
| [has_item_key_attr_element_kv](#has_item_key_attr_element_kv) | 判断物品编号是否存在ATTR_ELEMENT键值对 |
| [has_ability_key_attr_element_kv](#has_ability_key_attr_element_kv) | 判断技能编号是否存在ATTR_ELEMENT键值对 |
| [has_kv_pair_attr_element_read](#has_kv_pair_attr_element_read) | 判断是否存在ATTR_ELEMENT_READ键值对 |
| [has_unit_key_attr_element_read_kv](#has_unit_key_attr_element_read_kv) | 判断单位编号是否存在ATTR_ELEMENT_READ键值对 |
| [has_item_key_attr_element_read_kv](#has_item_key_attr_element_read_kv) | 判断物品编号是否存在ATTR_ELEMENT_READ键值对 |
| [has_ability_key_attr_element_read_kv](#has_ability_key_attr_element_read_kv) | 判断技能编号是否存在ATTR_ELEMENT_READ键值对 |
| [has_kv_pair_mover_entity](#has_kv_pair_mover_entity) | 判断是否存在MOVER_ENTITY键值对 |
| [has_unit_key_mover_entity_kv](#has_unit_key_mover_entity_kv) | 判断单位编号是否存在MOVER_ENTITY键值对 |
| [has_item_key_mover_entity_kv](#has_item_key_mover_entity_kv) | 判断物品编号是否存在MOVER_ENTITY键值对 |
| [has_ability_key_mover_entity_kv](#has_ability_key_mover_entity_kv) | 判断技能编号是否存在MOVER_ENTITY键值对 |
| [has_kv_pair_image_quality](#has_kv_pair_image_quality) | 判断是否存在IMAGE_QUALITY键值对 |
| [has_unit_key_image_quality_kv](#has_unit_key_image_quality_kv) | 判断单位编号是否存在IMAGE_QUALITY键值对 |
| [has_item_key_image_quality_kv](#has_item_key_image_quality_kv) | 判断物品编号是否存在IMAGE_QUALITY键值对 |
| [has_ability_key_image_quality_kv](#has_ability_key_image_quality_kv) | 判断技能编号是否存在IMAGE_QUALITY键值对 |
| [has_kv_pair_window_type_setting](#has_kv_pair_window_type_setting) | 判断是否存在WINDOW_TYPE_SETTING键值对 |
| [has_unit_key_window_type_setting_kv](#has_unit_key_window_type_setting_kv) | 判断单位编号是否存在WINDOW_TYPE_SETTING键值对 |
| [has_item_key_window_type_setting_kv](#has_item_key_window_type_setting_kv) | 判断物品编号是否存在WINDOW_TYPE_SETTING键值对 |
| [has_ability_key_window_type_setting_kv](#has_ability_key_window_type_setting_kv) | 判断技能编号是否存在WINDOW_TYPE_SETTING键值对 |
| [has_kv_pair_item_entity](#has_kv_pair_item_entity) | 判断是否存在ITEM_ENTITY键值对 |
| [has_unit_key_item_entity_kv](#has_unit_key_item_entity_kv) | 判断单位编号是否存在ITEM_ENTITY键值对 |
| [has_item_key_item_entity_kv](#has_item_key_item_entity_kv) | 判断物品编号是否存在ITEM_ENTITY键值对 |
| [has_ability_key_item_entity_kv](#has_ability_key_item_entity_kv) | 判断技能编号是否存在ITEM_ENTITY键值对 |
| [has_kv_pair_item_group](#has_kv_pair_item_group) | 判断是否存在ITEM_GROUP键值对 |
| [has_unit_key_item_group_kv](#has_unit_key_item_group_kv) | 判断单位编号是否存在ITEM_GROUP键值对 |
| [has_item_key_item_group_kv](#has_item_key_item_group_kv) | 判断物品编号是否存在ITEM_GROUP键值对 |
| [has_ability_key_item_group_kv](#has_ability_key_item_group_kv) | 判断技能编号是否存在ITEM_GROUP键值对 |
| [has_kv_pair_item_name](#has_kv_pair_item_name) | 判断是否存在ITEM_NAME键值对 |
| [has_unit_key_item_name_kv](#has_unit_key_item_name_kv) | 判断单位编号是否存在ITEM_NAME键值对 |
| [has_item_key_item_name_kv](#has_item_key_item_name_kv) | 判断物品编号是否存在ITEM_NAME键值对 |
| [has_ability_key_item_name_kv](#has_ability_key_item_name_kv) | 判断技能编号是否存在ITEM_NAME键值对 |
| [has_kv_pair_ability](#has_kv_pair_ability) | 判断是否存在ABILITY键值对 |
| [has_unit_key_ability_kv](#has_unit_key_ability_kv) | 判断单位编号是否存在ABILITY键值对 |
| [has_item_key_ability_kv](#has_item_key_ability_kv) | 判断物品编号是否存在ABILITY键值对 |
| [has_ability_key_ability_kv](#has_ability_key_ability_kv) | 判断技能编号是否存在ABILITY键值对 |
| [has_kv_pair_ability_type](#has_kv_pair_ability_type) | 判断是否存在ABILITY_TYPE键值对 |
| [has_unit_key_ability_type_kv](#has_unit_key_ability_type_kv) | 判断单位编号是否存在ABILITY_TYPE键值对 |
| [has_item_key_ability_type_kv](#has_item_key_ability_type_kv) | 判断物品编号是否存在ABILITY_TYPE键值对 |
| [has_ability_key_ability_type_kv](#has_ability_key_ability_type_kv) | 判断技能编号是否存在ABILITY_TYPE键值对 |
| [has_kv_pair_ability_cast_type](#has_kv_pair_ability_cast_type) | 判断是否存在ABILITY_CAST_TYPE键值对 |
| [has_unit_key_ability_cast_type_kv](#has_unit_key_ability_cast_type_kv) | 判断单位编号是否存在ABILITY_CAST_TYPE键值对 |
| [has_item_key_ability_cast_type_kv](#has_item_key_ability_cast_type_kv) | 判断物品编号是否存在ABILITY_CAST_TYPE键值对 |
| [has_ability_key_ability_cast_type_kv](#has_ability_key_ability_cast_type_kv) | 判断技能编号是否存在ABILITY_CAST_TYPE键值对 |
| [has_kv_pair_ability_name](#has_kv_pair_ability_name) | 判断是否存在ABILITY_NAME键值对 |
| [has_unit_key_ability_name_kv](#has_unit_key_ability_name_kv) | 判断单位编号是否存在ABILITY_NAME键值对 |
| [has_item_key_ability_name_kv](#has_item_key_ability_name_kv) | 判断物品编号是否存在ABILITY_NAME键值对 |
| [has_ability_key_ability_name_kv](#has_ability_key_ability_name_kv) | 判断技能编号是否存在ABILITY_NAME键值对 |
| [has_kv_pair_skill_pointer_type](#has_kv_pair_skill_pointer_type) | 判断是否存在SKILL_POINTER_TYPE键值对 |
| [has_unit_key_skill_pointer_type_kv](#has_unit_key_skill_pointer_type_kv) | 判断单位编号是否存在SKILL_POINTER_TYPE键值对 |
| [has_item_key_skill_pointer_type_kv](#has_item_key_skill_pointer_type_kv) | 判断物品编号是否存在SKILL_POINTER_TYPE键值对 |
| [has_ability_key_skill_pointer_type_kv](#has_ability_key_skill_pointer_type_kv) | 判断技能编号是否存在SKILL_POINTER_TYPE键值对 |
| [has_kv_pair_modifier_entity](#has_kv_pair_modifier_entity) | 判断是否存在MODIFIER_ENTITY键值对 |
| [has_unit_key_modifier_entity_kv](#has_unit_key_modifier_entity_kv) | 判断单位编号是否存在MODIFIER_ENTITY键值对 |
| [has_item_key_modifier_entity_kv](#has_item_key_modifier_entity_kv) | 判断物品编号是否存在MODIFIER_ENTITY键值对 |
| [has_ability_key_modifier_entity_kv](#has_ability_key_modifier_entity_kv) | 判断技能编号是否存在MODIFIER_ENTITY键值对 |
| [has_kv_pair_modifier_type](#has_kv_pair_modifier_type) | 判断是否存在MODIFIER_TYPE键值对 |
| [has_unit_key_modifier_type_kv](#has_unit_key_modifier_type_kv) | 判断单位编号是否存在MODIFIER_TYPE键值对 |
| [has_item_key_modifier_type_kv](#has_item_key_modifier_type_kv) | 判断物品编号是否存在MODIFIER_TYPE键值对 |
| [has_ability_key_modifier_type_kv](#has_ability_key_modifier_type_kv) | 判断技能编号是否存在MODIFIER_TYPE键值对 |
| [has_kv_pair_modifier_effect_type](#has_kv_pair_modifier_effect_type) | 判断是否存在MODIFIER_EFFECT_TYPE键值对 |
| [has_unit_key_modifier_effect_type_kv](#has_unit_key_modifier_effect_type_kv) | 判断单位编号是否存在MODIFIER_EFFECT_TYPE键值对 |
| [has_item_key_modifier_effect_type_kv](#has_item_key_modifier_effect_type_kv) | 判断物品编号是否存在MODIFIER_EFFECT_TYPE键值对 |
| [has_ability_key_modifier_effect_type_kv](#has_ability_key_modifier_effect_type_kv) | 判断技能编号是否存在MODIFIER_EFFECT_TYPE键值对 |
| [has_kv_pair_modifier](#has_kv_pair_modifier) | 判断是否存在MODIFIER键值对 |
| [has_unit_key_modifier_kv](#has_unit_key_modifier_kv) | 判断单位编号是否存在MODIFIER键值对 |
| [has_item_key_modifier_kv](#has_item_key_modifier_kv) | 判断物品编号是否存在MODIFIER键值对 |
| [has_ability_key_modifier_kv](#has_ability_key_modifier_kv) | 判断技能编号是否存在MODIFIER键值对 |
| [has_kv_pair_projectile](#has_kv_pair_projectile) | 判断是否存在PROJECTILE键值对 |
| [has_unit_key_projectile_kv](#has_unit_key_projectile_kv) | 判断单位编号是否存在PROJECTILE键值对 |
| [has_item_key_projectile_kv](#has_item_key_projectile_kv) | 判断物品编号是否存在PROJECTILE键值对 |
| [has_ability_key_projectile_kv](#has_ability_key_projectile_kv) | 判断技能编号是否存在PROJECTILE键值对 |
| [has_kv_pair_projectile_entity](#has_kv_pair_projectile_entity) | 判断是否存在PROJECTILE_ENTITY键值对 |
| [has_unit_key_projectile_entity_kv](#has_unit_key_projectile_entity_kv) | 判断单位编号是否存在PROJECTILE_ENTITY键值对 |
| [has_item_key_projectile_entity_kv](#has_item_key_projectile_entity_kv) | 判断物品编号是否存在PROJECTILE_ENTITY键值对 |
| [has_ability_key_projectile_entity_kv](#has_ability_key_projectile_entity_kv) | 判断技能编号是否存在PROJECTILE_ENTITY键值对 |
| [has_kv_pair_projectile_group](#has_kv_pair_projectile_group) | 判断是否存在PROJECTILE_GROUP键值对 |
| [has_unit_key_projectile_group_kv](#has_unit_key_projectile_group_kv) | 判断单位编号是否存在PROJECTILE_GROUP键值对 |
| [has_item_key_projectile_group_kv](#has_item_key_projectile_group_kv) | 判断物品编号是否存在PROJECTILE_GROUP键值对 |
| [has_ability_key_projectile_group_kv](#has_ability_key_projectile_group_kv) | 判断技能编号是否存在PROJECTILE_GROUP键值对 |
| [has_kv_pair_destructible_entity](#has_kv_pair_destructible_entity) | 判断是否存在DESTRUCTIBLE_ENTITY键值对 |
| [has_unit_key_destructible_entity_kv](#has_unit_key_destructible_entity_kv) | 判断单位编号是否存在DESTRUCTIBLE_ENTITY键值对 |
| [has_item_key_destructible_entity_kv](#has_item_key_destructible_entity_kv) | 判断物品编号是否存在DESTRUCTIBLE_ENTITY键值对 |
| [has_ability_key_destructible_entity_kv](#has_ability_key_destructible_entity_kv) | 判断技能编号是否存在DESTRUCTIBLE_ENTITY键值对 |
| [has_kv_pair_destructible_name](#has_kv_pair_destructible_name) | 判断是否存在DESTRUCTIBLE_NAME键值对 |
| [has_unit_key_destructible_name_kv](#has_unit_key_destructible_name_kv) | 判断单位编号是否存在DESTRUCTIBLE_NAME键值对 |
| [has_item_key_destructible_name_kv](#has_item_key_destructible_name_kv) | 判断物品编号是否存在DESTRUCTIBLE_NAME键值对 |
| [has_ability_key_destructible_name_kv](#has_ability_key_destructible_name_kv) | 判断技能编号是否存在DESTRUCTIBLE_NAME键值对 |
| [has_kv_pair_sound_entity](#has_kv_pair_sound_entity) | 判断是否存在SOUND_ENTITY键值对 |
| [has_unit_key_sound_entity_kv](#has_unit_key_sound_entity_kv) | 判断单位编号是否存在SOUND_ENTITY键值对 |
| [has_item_key_sound_entity_kv](#has_item_key_sound_entity_kv) | 判断物品编号是否存在SOUND_ENTITY键值对 |
| [has_ability_key_sound_entity_kv](#has_ability_key_sound_entity_kv) | 判断技能编号是否存在SOUND_ENTITY键值对 |
| [has_kv_pair_audio_key](#has_kv_pair_audio_key) | 判断是否存在AUDIO_KEY键值对 |
| [has_unit_key_audio_key_kv](#has_unit_key_audio_key_kv) | 判断单位编号是否存在AUDIO_KEY键值对 |
| [has_item_key_audio_key_kv](#has_item_key_audio_key_kv) | 判断物品编号是否存在AUDIO_KEY键值对 |
| [has_ability_key_audio_key_kv](#has_ability_key_audio_key_kv) | 判断技能编号是否存在AUDIO_KEY键值对 |
| [has_kv_pair_game_mode](#has_kv_pair_game_mode) | 判断是否存在GAME_MODE键值对 |
| [has_unit_key_game_mode_kv](#has_unit_key_game_mode_kv) | 判断单位编号是否存在GAME_MODE键值对 |
| [has_item_key_game_mode_kv](#has_item_key_game_mode_kv) | 判断物品编号是否存在GAME_MODE键值对 |
| [has_ability_key_game_mode_kv](#has_ability_key_game_mode_kv) | 判断技能编号是否存在GAME_MODE键值对 |
| [has_kv_pair_player](#has_kv_pair_player) | 判断是否存在PLAYER键值对 |
| [has_unit_key_player_kv](#has_unit_key_player_kv) | 判断单位编号是否存在PLAYER键值对 |
| [has_item_key_player_kv](#has_item_key_player_kv) | 判断物品编号是否存在PLAYER键值对 |
| [has_ability_key_player_kv](#has_ability_key_player_kv) | 判断技能编号是否存在PLAYER键值对 |
| [has_kv_pair_player_group](#has_kv_pair_player_group) | 判断是否存在PLAYER_GROUP键值对 |
| [has_unit_key_player_group_kv](#has_unit_key_player_group_kv) | 判断单位编号是否存在PLAYER_GROUP键值对 |
| [has_item_key_player_group_kv](#has_item_key_player_group_kv) | 判断物品编号是否存在PLAYER_GROUP键值对 |
| [has_ability_key_player_group_kv](#has_ability_key_player_group_kv) | 判断技能编号是否存在PLAYER_GROUP键值对 |
| [has_kv_pair_role_res_key](#has_kv_pair_role_res_key) | 判断是否存在ROLE_RES_KEY键值对 |
| [has_unit_key_role_res_key_kv](#has_unit_key_role_res_key_kv) | 判断单位编号是否存在ROLE_RES_KEY键值对 |
| [has_item_key_role_res_key_kv](#has_item_key_role_res_key_kv) | 判断物品编号是否存在ROLE_RES_KEY键值对 |
| [has_ability_key_role_res_key_kv](#has_ability_key_role_res_key_kv) | 判断技能编号是否存在ROLE_RES_KEY键值对 |
| [has_kv_pair_role_status](#has_kv_pair_role_status) | 判断是否存在ROLE_STATUS键值对 |
| [has_unit_key_role_status_kv](#has_unit_key_role_status_kv) | 判断单位编号是否存在ROLE_STATUS键值对 |
| [has_item_key_role_status_kv](#has_item_key_role_status_kv) | 判断物品编号是否存在ROLE_STATUS键值对 |
| [has_ability_key_role_status_kv](#has_ability_key_role_status_kv) | 判断技能编号是否存在ROLE_STATUS键值对 |
| [has_kv_pair_role_type](#has_kv_pair_role_type) | 判断是否存在ROLE_TYPE键值对 |
| [has_unit_key_role_type_kv](#has_unit_key_role_type_kv) | 判断单位编号是否存在ROLE_TYPE键值对 |
| [has_item_key_role_type_kv](#has_item_key_role_type_kv) | 判断物品编号是否存在ROLE_TYPE键值对 |
| [has_ability_key_role_type_kv](#has_ability_key_role_type_kv) | 判断技能编号是否存在ROLE_TYPE键值对 |
| [has_kv_pair_role_relation](#has_kv_pair_role_relation) | 判断是否存在ROLE_RELATION键值对 |
| [has_unit_key_role_relation_kv](#has_unit_key_role_relation_kv) | 判断单位编号是否存在ROLE_RELATION键值对 |
| [has_item_key_role_relation_kv](#has_item_key_role_relation_kv) | 判断物品编号是否存在ROLE_RELATION键值对 |
| [has_ability_key_role_relation_kv](#has_ability_key_role_relation_kv) | 判断技能编号是否存在ROLE_RELATION键值对 |
| [has_kv_pair_team](#has_kv_pair_team) | 判断是否存在TEAM键值对 |
| [has_unit_key_team_kv](#has_unit_key_team_kv) | 判断单位编号是否存在TEAM键值对 |
| [has_item_key_team_kv](#has_item_key_team_kv) | 判断物品编号是否存在TEAM键值对 |
| [has_ability_key_team_kv](#has_ability_key_team_kv) | 判断技能编号是否存在TEAM键值对 |
| [has_kv_pair_point](#has_kv_pair_point) | 判断是否存在POINT键值对 |
| [has_unit_key_point_kv](#has_unit_key_point_kv) | 判断单位编号是否存在POINT键值对 |
| [has_item_key_point_kv](#has_item_key_point_kv) | 判断物品编号是否存在POINT键值对 |
| [has_ability_key_point_kv](#has_ability_key_point_kv) | 判断技能编号是否存在POINT键值对 |
| [has_kv_pair_vector3](#has_kv_pair_vector3) | 判断是否存在VECTOR3键值对 |
| [has_unit_key_vector3_kv](#has_unit_key_vector3_kv) | 判断单位编号是否存在VECTOR3键值对 |
| [has_item_key_vector3_kv](#has_item_key_vector3_kv) | 判断物品编号是否存在VECTOR3键值对 |
| [has_ability_key_vector3_kv](#has_ability_key_vector3_kv) | 判断技能编号是否存在VECTOR3键值对 |
| [has_kv_pair_rotation](#has_kv_pair_rotation) | 判断是否存在ROTATION键值对 |
| [has_unit_key_rotation_kv](#has_unit_key_rotation_kv) | 判断单位编号是否存在ROTATION键值对 |
| [has_item_key_rotation_kv](#has_item_key_rotation_kv) | 判断物品编号是否存在ROTATION键值对 |
| [has_ability_key_rotation_kv](#has_ability_key_rotation_kv) | 判断技能编号是否存在ROTATION键值对 |
| [has_kv_pair_point_list](#has_kv_pair_point_list) | 判断是否存在POINT_LIST键值对 |
| [has_unit_key_point_list_kv](#has_unit_key_point_list_kv) | 判断单位编号是否存在POINT_LIST键值对 |
| [has_item_key_point_list_kv](#has_item_key_point_list_kv) | 判断物品编号是否存在POINT_LIST键值对 |
| [has_ability_key_point_list_kv](#has_ability_key_point_list_kv) | 判断技能编号是否存在POINT_LIST键值对 |
| [has_kv_pair_rectangle](#has_kv_pair_rectangle) | 判断是否存在RECTANGLE键值对 |
| [has_unit_key_rectangle_kv](#has_unit_key_rectangle_kv) | 判断单位编号是否存在RECTANGLE键值对 |
| [has_item_key_rectangle_kv](#has_item_key_rectangle_kv) | 判断物品编号是否存在RECTANGLE键值对 |
| [has_ability_key_rectangle_kv](#has_ability_key_rectangle_kv) | 判断技能编号是否存在RECTANGLE键值对 |
| [has_kv_pair_round_area](#has_kv_pair_round_area) | 判断是否存在ROUND_AREA键值对 |
| [has_unit_key_round_area_kv](#has_unit_key_round_area_kv) | 判断单位编号是否存在ROUND_AREA键值对 |
| [has_item_key_round_area_kv](#has_item_key_round_area_kv) | 判断物品编号是否存在ROUND_AREA键值对 |
| [has_ability_key_round_area_kv](#has_ability_key_round_area_kv) | 判断技能编号是否存在ROUND_AREA键值对 |
| [has_kv_pair_polygon](#has_kv_pair_polygon) | 判断是否存在POLYGON键值对 |
| [has_unit_key_polygon_kv](#has_unit_key_polygon_kv) | 判断单位编号是否存在POLYGON键值对 |
| [has_item_key_polygon_kv](#has_item_key_polygon_kv) | 判断物品编号是否存在POLYGON键值对 |
| [has_ability_key_polygon_kv](#has_ability_key_polygon_kv) | 判断技能编号是否存在POLYGON键值对 |
| [has_kv_pair_camera](#has_kv_pair_camera) | 判断是否存在CAMERA键值对 |
| [has_unit_key_camera_kv](#has_unit_key_camera_kv) | 判断单位编号是否存在CAMERA键值对 |
| [has_item_key_camera_kv](#has_item_key_camera_kv) | 判断物品编号是否存在CAMERA键值对 |
| [has_ability_key_camera_kv](#has_ability_key_camera_kv) | 判断技能编号是否存在CAMERA键值对 |
| [has_kv_pair_camline](#has_kv_pair_camline) | 判断是否存在CAMLINE键值对 |
| [has_unit_key_camline_kv](#has_unit_key_camline_kv) | 判断单位编号是否存在CAMLINE键值对 |
| [has_item_key_camline_kv](#has_item_key_camline_kv) | 判断物品编号是否存在CAMLINE键值对 |
| [has_ability_key_camline_kv](#has_ability_key_camline_kv) | 判断技能编号是否存在CAMLINE键值对 |
| [has_kv_pair_point_light](#has_kv_pair_point_light) | 判断是否存在POINT_LIGHT键值对 |
| [has_unit_key_point_light_kv](#has_unit_key_point_light_kv) | 判断单位编号是否存在POINT_LIGHT键值对 |
| [has_item_key_point_light_kv](#has_item_key_point_light_kv) | 判断物品编号是否存在POINT_LIGHT键值对 |
| [has_ability_key_point_light_kv](#has_ability_key_point_light_kv) | 判断技能编号是否存在POINT_LIGHT键值对 |
| [has_kv_pair_spot_light](#has_kv_pair_spot_light) | 判断是否存在SPOT_LIGHT键值对 |
| [has_unit_key_spot_light_kv](#has_unit_key_spot_light_kv) | 判断单位编号是否存在SPOT_LIGHT键值对 |
| [has_item_key_spot_light_kv](#has_item_key_spot_light_kv) | 判断物品编号是否存在SPOT_LIGHT键值对 |
| [has_ability_key_spot_light_kv](#has_ability_key_spot_light_kv) | 判断技能编号是否存在SPOT_LIGHT键值对 |
| [has_kv_pair_fog](#has_kv_pair_fog) | 判断是否存在FOG键值对 |
| [has_unit_key_fog_kv](#has_unit_key_fog_kv) | 判断单位编号是否存在FOG键值对 |
| [has_item_key_fog_kv](#has_item_key_fog_kv) | 判断物品编号是否存在FOG键值对 |
| [has_ability_key_fog_kv](#has_ability_key_fog_kv) | 判断技能编号是否存在FOG键值对 |
| [has_kv_pair_scene_sound](#has_kv_pair_scene_sound) | 判断是否存在SCENE_SOUND键值对 |
| [has_unit_key_scene_sound_kv](#has_unit_key_scene_sound_kv) | 判断单位编号是否存在SCENE_SOUND键值对 |
| [has_item_key_scene_sound_kv](#has_item_key_scene_sound_kv) | 判断物品编号是否存在SCENE_SOUND键值对 |
| [has_ability_key_scene_sound_kv](#has_ability_key_scene_sound_kv) | 判断技能编号是否存在SCENE_SOUND键值对 |
| [has_kv_pair_model](#has_kv_pair_model) | 判断是否存在MODEL键值对 |
| [has_unit_key_model_kv](#has_unit_key_model_kv) | 判断单位编号是否存在MODEL键值对 |
| [has_item_key_model_kv](#has_item_key_model_kv) | 判断物品编号是否存在MODEL键值对 |
| [has_ability_key_model_kv](#has_ability_key_model_kv) | 判断技能编号是否存在MODEL键值对 |
| [has_kv_pair_sfx_entity](#has_kv_pair_sfx_entity) | 判断是否存在SFX_ENTITY键值对 |
| [has_unit_key_sfx_entity_kv](#has_unit_key_sfx_entity_kv) | 判断单位编号是否存在SFX_ENTITY键值对 |
| [has_item_key_sfx_entity_kv](#has_item_key_sfx_entity_kv) | 判断物品编号是否存在SFX_ENTITY键值对 |
| [has_ability_key_sfx_entity_kv](#has_ability_key_sfx_entity_kv) | 判断技能编号是否存在SFX_ENTITY键值对 |
| [has_kv_pair_sfx_key](#has_kv_pair_sfx_key) | 判断是否存在SFX_KEY键值对 |
| [has_unit_key_sfx_key_kv](#has_unit_key_sfx_key_kv) | 判断单位编号是否存在SFX_KEY键值对 |
| [has_item_key_sfx_key_kv](#has_item_key_sfx_key_kv) | 判断物品编号是否存在SFX_KEY键值对 |
| [has_ability_key_sfx_key_kv](#has_ability_key_sfx_key_kv) | 判断技能编号是否存在SFX_KEY键值对 |
| [has_kv_pair_link_sfx_entity](#has_kv_pair_link_sfx_entity) | 判断是否存在LINK_SFX_ENTITY键值对 |
| [has_unit_key_link_sfx_entity_kv](#has_unit_key_link_sfx_entity_kv) | 判断单位编号是否存在LINK_SFX_ENTITY键值对 |
| [has_item_key_link_sfx_entity_kv](#has_item_key_link_sfx_entity_kv) | 判断物品编号是否存在LINK_SFX_ENTITY键值对 |
| [has_ability_key_link_sfx_entity_kv](#has_ability_key_link_sfx_entity_kv) | 判断技能编号是否存在LINK_SFX_ENTITY键值对 |
| [has_kv_pair_link_sfx_key](#has_kv_pair_link_sfx_key) | 判断是否存在LINK_SFX_KEY键值对 |
| [has_unit_key_link_sfx_key_kv](#has_unit_key_link_sfx_key_kv) | 判断单位编号是否存在LINK_SFX_KEY键值对 |
| [has_item_key_link_sfx_key_kv](#has_item_key_link_sfx_key_kv) | 判断物品编号是否存在LINK_SFX_KEY键值对 |
| [has_ability_key_link_sfx_key_kv](#has_ability_key_link_sfx_key_kv) | 判断技能编号是否存在LINK_SFX_KEY键值对 |
| [has_kv_pair_cursor_key](#has_kv_pair_cursor_key) | 判断是否存在CURSOR_KEY键值对 |
| [has_unit_key_cursor_key_kv](#has_unit_key_cursor_key_kv) | 判断单位编号是否存在CURSOR_KEY键值对 |
| [has_item_key_cursor_key_kv](#has_item_key_cursor_key_kv) | 判断物品编号是否存在CURSOR_KEY键值对 |
| [has_ability_key_cursor_key_kv](#has_ability_key_cursor_key_kv) | 判断技能编号是否存在CURSOR_KEY键值对 |
| [has_kv_pair_angle](#has_kv_pair_angle) | 判断是否存在ANGLE键值对 |
| [has_unit_key_angle_kv](#has_unit_key_angle_kv) | 判断单位编号是否存在ANGLE键值对 |
| [has_item_key_angle_kv](#has_item_key_angle_kv) | 判断物品编号是否存在ANGLE键值对 |
| [has_ability_key_angle_kv](#has_ability_key_angle_kv) | 判断技能编号是否存在ANGLE键值对 |
| [has_kv_pair_texture](#has_kv_pair_texture) | 判断是否存在TEXTURE键值对 |
| [has_unit_key_texture_kv](#has_unit_key_texture_kv) | 判断单位编号是否存在TEXTURE键值对 |
| [has_item_key_texture_kv](#has_item_key_texture_kv) | 判断物品编号是否存在TEXTURE键值对 |
| [has_ability_key_texture_kv](#has_ability_key_texture_kv) | 判断技能编号是否存在TEXTURE键值对 |
| [has_kv_pair_sequence](#has_kv_pair_sequence) | 判断是否存在SEQUENCE键值对 |
| [has_unit_key_sequence_kv](#has_unit_key_sequence_kv) | 判断单位编号是否存在SEQUENCE键值对 |
| [has_item_key_sequence_kv](#has_item_key_sequence_kv) | 判断物品编号是否存在SEQUENCE键值对 |
| [has_ability_key_sequence_kv](#has_ability_key_sequence_kv) | 判断技能编号是否存在SEQUENCE键值对 |
| [has_kv_pair_physics_object](#has_kv_pair_physics_object) | 判断是否存在PHYSICS_OBJECT键值对 |
| [has_unit_key_physics_object_kv](#has_unit_key_physics_object_kv) | 判断单位编号是否存在PHYSICS_OBJECT键值对 |
| [has_item_key_physics_object_kv](#has_item_key_physics_object_kv) | 判断物品编号是否存在PHYSICS_OBJECT键值对 |
| [has_ability_key_physics_object_kv](#has_ability_key_physics_object_kv) | 判断技能编号是否存在PHYSICS_OBJECT键值对 |
| [has_kv_pair_physics_entity](#has_kv_pair_physics_entity) | 判断是否存在PHYSICS_ENTITY键值对 |
| [has_unit_key_physics_entity_kv](#has_unit_key_physics_entity_kv) | 判断单位编号是否存在PHYSICS_ENTITY键值对 |
| [has_item_key_physics_entity_kv](#has_item_key_physics_entity_kv) | 判断物品编号是否存在PHYSICS_ENTITY键值对 |
| [has_ability_key_physics_entity_kv](#has_ability_key_physics_entity_kv) | 判断技能编号是否存在PHYSICS_ENTITY键值对 |
| [has_kv_pair_physics_object_key](#has_kv_pair_physics_object_key) | 判断是否存在PHYSICS_OBJECT_KEY键值对 |
| [has_unit_key_physics_object_key_kv](#has_unit_key_physics_object_key_kv) | 判断单位编号是否存在PHYSICS_OBJECT_KEY键值对 |
| [has_item_key_physics_object_key_kv](#has_item_key_physics_object_key_kv) | 判断物品编号是否存在PHYSICS_OBJECT_KEY键值对 |
| [has_ability_key_physics_object_key_kv](#has_ability_key_physics_object_key_kv) | 判断技能编号是否存在PHYSICS_OBJECT_KEY键值对 |
| [has_kv_pair_physics_entity_key](#has_kv_pair_physics_entity_key) | 判断是否存在PHYSICS_ENTITY_KEY键值对 |
| [has_unit_key_physics_entity_key_kv](#has_unit_key_physics_entity_key_kv) | 判断单位编号是否存在PHYSICS_ENTITY_KEY键值对 |
| [has_item_key_physics_entity_key_kv](#has_item_key_physics_entity_key_kv) | 判断物品编号是否存在PHYSICS_ENTITY_KEY键值对 |
| [has_ability_key_physics_entity_key_kv](#has_ability_key_physics_entity_key_kv) | 判断技能编号是否存在PHYSICS_ENTITY_KEY键值对 |
| [has_kv_pair_rigid_body](#has_kv_pair_rigid_body) | 判断是否存在RIGID_BODY键值对 |
| [has_unit_key_rigid_body_kv](#has_unit_key_rigid_body_kv) | 判断单位编号是否存在RIGID_BODY键值对 |
| [has_item_key_rigid_body_kv](#has_item_key_rigid_body_kv) | 判断物品编号是否存在RIGID_BODY键值对 |
| [has_ability_key_rigid_body_kv](#has_ability_key_rigid_body_kv) | 判断技能编号是否存在RIGID_BODY键值对 |
| [has_kv_pair_rigid_body_group](#has_kv_pair_rigid_body_group) | 判断是否存在RIGID_BODY_GROUP键值对 |
| [has_unit_key_rigid_body_group_kv](#has_unit_key_rigid_body_group_kv) | 判断单位编号是否存在RIGID_BODY_GROUP键值对 |
| [has_item_key_rigid_body_group_kv](#has_item_key_rigid_body_group_kv) | 判断物品编号是否存在RIGID_BODY_GROUP键值对 |
| [has_ability_key_rigid_body_group_kv](#has_ability_key_rigid_body_group_kv) | 判断技能编号是否存在RIGID_BODY_GROUP键值对 |
| [has_kv_pair_collider](#has_kv_pair_collider) | 判断是否存在COLLIDER键值对 |
| [has_unit_key_collider_kv](#has_unit_key_collider_kv) | 判断单位编号是否存在COLLIDER键值对 |
| [has_item_key_collider_kv](#has_item_key_collider_kv) | 判断物品编号是否存在COLLIDER键值对 |
| [has_ability_key_collider_kv](#has_ability_key_collider_kv) | 判断技能编号是否存在COLLIDER键值对 |
| [has_kv_pair_joint](#has_kv_pair_joint) | 判断是否存在JOINT键值对 |
| [has_unit_key_joint_kv](#has_unit_key_joint_kv) | 判断单位编号是否存在JOINT键值对 |
| [has_item_key_joint_kv](#has_item_key_joint_kv) | 判断物品编号是否存在JOINT键值对 |
| [has_ability_key_joint_kv](#has_ability_key_joint_kv) | 判断技能编号是否存在JOINT键值对 |
| [has_kv_pair_reaction](#has_kv_pair_reaction) | 判断是否存在REACTION键值对 |
| [has_unit_key_reaction_kv](#has_unit_key_reaction_kv) | 判断单位编号是否存在REACTION键值对 |
| [has_item_key_reaction_kv](#has_item_key_reaction_kv) | 判断物品编号是否存在REACTION键值对 |
| [has_ability_key_reaction_kv](#has_ability_key_reaction_kv) | 判断技能编号是否存在REACTION键值对 |
| [has_kv_pair_reaction_group](#has_kv_pair_reaction_group) | 判断是否存在REACTION_GROUP键值对 |
| [has_unit_key_reaction_group_kv](#has_unit_key_reaction_group_kv) | 判断单位编号是否存在REACTION_GROUP键值对 |
| [has_item_key_reaction_group_kv](#has_item_key_reaction_group_kv) | 判断物品编号是否存在REACTION_GROUP键值对 |
| [has_ability_key_reaction_group_kv](#has_ability_key_reaction_group_kv) | 判断技能编号是否存在REACTION_GROUP键值对 |
| [has_kv_pair_dynamic_trigger_instance](#has_kv_pair_dynamic_trigger_instance) | 判断是否存在DYNAMIC_TRIGGER_INSTANCE键值对 |
| [has_unit_key_dynamic_trigger_instance_kv](#has_unit_key_dynamic_trigger_instance_kv) | 判断单位编号是否存在DYNAMIC_TRIGGER_INSTANCE键值对 |
| [has_item_key_dynamic_trigger_instance_kv](#has_item_key_dynamic_trigger_instance_kv) | 判断物品编号是否存在DYNAMIC_TRIGGER_INSTANCE键值对 |
| [has_ability_key_dynamic_trigger_instance_kv](#has_ability_key_dynamic_trigger_instance_kv) | 判断技能编号是否存在DYNAMIC_TRIGGER_INSTANCE键值对 |
| [has_kv_pair_table](#has_kv_pair_table) | 判断是否存在TABLE键值对 |
| [has_unit_key_table_kv](#has_unit_key_table_kv) | 判断单位编号是否存在TABLE键值对 |
| [has_item_key_table_kv](#has_item_key_table_kv) | 判断物品编号是否存在TABLE键值对 |
| [has_ability_key_table_kv](#has_ability_key_table_kv) | 判断技能编号是否存在TABLE键值对 |
| [has_kv_pair_random_pool](#has_kv_pair_random_pool) | 判断是否存在RANDOM_POOL键值对 |
| [has_unit_key_random_pool_kv](#has_unit_key_random_pool_kv) | 判断单位编号是否存在RANDOM_POOL键值对 |
| [has_item_key_random_pool_kv](#has_item_key_random_pool_kv) | 判断物品编号是否存在RANDOM_POOL键值对 |
| [has_ability_key_random_pool_kv](#has_ability_key_random_pool_kv) | 判断技能编号是否存在RANDOM_POOL键值对 |
| [has_kv_pair_scene_ui](#has_kv_pair_scene_ui) | 判断是否存在SCENE_UI键值对 |
| [has_unit_key_scene_ui_kv](#has_unit_key_scene_ui_kv) | 判断单位编号是否存在SCENE_UI键值对 |
| [has_item_key_scene_ui_kv](#has_item_key_scene_ui_kv) | 判断物品编号是否存在SCENE_UI键值对 |
| [has_ability_key_scene_ui_kv](#has_ability_key_scene_ui_kv) | 判断技能编号是否存在SCENE_UI键值对 |
| [has_kv_pair_damage_type](#has_kv_pair_damage_type) | 判断是否存在DAMAGE_TYPE键值对 |
| [has_unit_key_damage_type_kv](#has_unit_key_damage_type_kv) | 判断单位编号是否存在DAMAGE_TYPE键值对 |
| [has_item_key_damage_type_kv](#has_item_key_damage_type_kv) | 判断物品编号是否存在DAMAGE_TYPE键值对 |
| [has_ability_key_damage_type_kv](#has_ability_key_damage_type_kv) | 判断技能编号是否存在DAMAGE_TYPE键值对 |
| [has_kv_pair_harm_text_type_new](#has_kv_pair_harm_text_type_new) | 判断是否存在HARM_TEXT_TYPE_NEW键值对 |
| [has_unit_key_harm_text_type_new_kv](#has_unit_key_harm_text_type_new_kv) | 判断单位编号是否存在HARM_TEXT_TYPE_NEW键值对 |
| [has_item_key_harm_text_type_new_kv](#has_item_key_harm_text_type_new_kv) | 判断物品编号是否存在HARM_TEXT_TYPE_NEW键值对 |
| [has_ability_key_harm_text_type_new_kv](#has_ability_key_harm_text_type_new_kv) | 判断技能编号是否存在HARM_TEXT_TYPE_NEW键值对 |
| [has_kv_pair_font_type](#has_kv_pair_font_type) | 判断是否存在FONT_TYPE键值对 |
| [has_unit_key_font_type_kv](#has_unit_key_font_type_kv) | 判断单位编号是否存在FONT_TYPE键值对 |
| [has_item_key_font_type_kv](#has_item_key_font_type_kv) | 判断物品编号是否存在FONT_TYPE键值对 |
| [has_ability_key_font_type_kv](#has_ability_key_font_type_kv) | 判断技能编号是否存在FONT_TYPE键值对 |
| [has_kv_pair_jump_word_track](#has_kv_pair_jump_word_track) | 判断是否存在JUMP_WORD_TRACK键值对 |
| [has_unit_key_jump_word_track_kv](#has_unit_key_jump_word_track_kv) | 判断单位编号是否存在JUMP_WORD_TRACK键值对 |
| [has_item_key_jump_word_track_kv](#has_item_key_jump_word_track_kv) | 判断物品编号是否存在JUMP_WORD_TRACK键值对 |
| [has_ability_key_jump_word_track_kv](#has_ability_key_jump_word_track_kv) | 判断技能编号是否存在JUMP_WORD_TRACK键值对 |
| [has_kv_pair_new_timer](#has_kv_pair_new_timer) | 判断是否存在NEW_TIMER键值对 |
| [has_unit_key_new_timer_kv](#has_unit_key_new_timer_kv) | 判断单位编号是否存在NEW_TIMER键值对 |
| [has_item_key_new_timer_kv](#has_item_key_new_timer_kv) | 判断物品编号是否存在NEW_TIMER键值对 |
| [has_ability_key_new_timer_kv](#has_ability_key_new_timer_kv) | 判断技能编号是否存在NEW_TIMER键值对 |
| [has_kv_pair_tech_key](#has_kv_pair_tech_key) | 判断是否存在TECH_KEY键值对 |
| [has_unit_key_tech_key_kv](#has_unit_key_tech_key_kv) | 判断单位编号是否存在TECH_KEY键值对 |
| [has_item_key_tech_key_kv](#has_item_key_tech_key_kv) | 判断物品编号是否存在TECH_KEY键值对 |
| [has_ability_key_tech_key_kv](#has_ability_key_tech_key_kv) | 判断技能编号是否存在TECH_KEY键值对 |
| [has_kv_pair_store_key](#has_kv_pair_store_key) | 判断是否存在STORE_KEY键值对 |
| [has_unit_key_store_key_kv](#has_unit_key_store_key_kv) | 判断单位编号是否存在STORE_KEY键值对 |
| [has_item_key_store_key_kv](#has_item_key_store_key_kv) | 判断物品编号是否存在STORE_KEY键值对 |
| [has_ability_key_store_key_kv](#has_ability_key_store_key_kv) | 判断技能编号是否存在STORE_KEY键值对 |
| [has_kv_pair_keyboard_key](#has_kv_pair_keyboard_key) | 判断是否存在KEYBOARD_KEY键值对 |
| [has_unit_key_keyboard_key_kv](#has_unit_key_keyboard_key_kv) | 判断单位编号是否存在KEYBOARD_KEY键值对 |
| [has_item_key_keyboard_key_kv](#has_item_key_keyboard_key_kv) | 判断物品编号是否存在KEYBOARD_KEY键值对 |
| [has_ability_key_keyboard_key_kv](#has_ability_key_keyboard_key_kv) | 判断技能编号是否存在KEYBOARD_KEY键值对 |
| [has_kv_pair_func_keyboard_key](#has_kv_pair_func_keyboard_key) | 判断是否存在FUNC_KEYBOARD_KEY键值对 |
| [has_unit_key_func_keyboard_key_kv](#has_unit_key_func_keyboard_key_kv) | 判断单位编号是否存在FUNC_KEYBOARD_KEY键值对 |
| [has_item_key_func_keyboard_key_kv](#has_item_key_func_keyboard_key_kv) | 判断物品编号是否存在FUNC_KEYBOARD_KEY键值对 |
| [has_ability_key_func_keyboard_key_kv](#has_ability_key_func_keyboard_key_kv) | 判断技能编号是否存在FUNC_KEYBOARD_KEY键值对 |
| [has_kv_pair_mouse_key](#has_kv_pair_mouse_key) | 判断是否存在MOUSE_KEY键值对 |
| [has_unit_key_mouse_key_kv](#has_unit_key_mouse_key_kv) | 判断单位编号是否存在MOUSE_KEY键值对 |
| [has_item_key_mouse_key_kv](#has_item_key_mouse_key_kv) | 判断物品编号是否存在MOUSE_KEY键值对 |
| [has_ability_key_mouse_key_kv](#has_ability_key_mouse_key_kv) | 判断技能编号是否存在MOUSE_KEY键值对 |
| [has_kv_pair_mouse_wheel](#has_kv_pair_mouse_wheel) | 判断是否存在MOUSE_WHEEL键值对 |
| [has_unit_key_mouse_wheel_kv](#has_unit_key_mouse_wheel_kv) | 判断单位编号是否存在MOUSE_WHEEL键值对 |
| [has_item_key_mouse_wheel_kv](#has_item_key_mouse_wheel_kv) | 判断物品编号是否存在MOUSE_WHEEL键值对 |
| [has_ability_key_mouse_wheel_kv](#has_ability_key_mouse_wheel_kv) | 判断技能编号是否存在MOUSE_WHEEL键值对 |
| [has_kv_pair_post_effect](#has_kv_pair_post_effect) | 判断是否存在POST_EFFECT键值对 |
| [has_unit_key_post_effect_kv](#has_unit_key_post_effect_kv) | 判断单位编号是否存在POST_EFFECT键值对 |
| [has_item_key_post_effect_kv](#has_item_key_post_effect_kv) | 判断物品编号是否存在POST_EFFECT键值对 |
| [has_ability_key_post_effect_kv](#has_ability_key_post_effect_kv) | 判断技能编号是否存在POST_EFFECT键值对 |
| [has_kv_pair_unit_type](#has_kv_pair_unit_type) | 判断是否存在UNIT_TYPE键值对 |
| [has_unit_key_unit_type_kv](#has_unit_key_unit_type_kv) | 判断单位编号是否存在UNIT_TYPE键值对 |
| [has_item_key_unit_type_kv](#has_item_key_unit_type_kv) | 判断物品编号是否存在UNIT_TYPE键值对 |
| [has_ability_key_unit_type_kv](#has_ability_key_unit_type_kv) | 判断技能编号是否存在UNIT_TYPE键值对 |
| [has_kv_pair_unit_command_type](#has_kv_pair_unit_command_type) | 判断是否存在UNIT_COMMAND_TYPE键值对 |
| [has_unit_key_unit_command_type_kv](#has_unit_key_unit_command_type_kv) | 判断单位编号是否存在UNIT_COMMAND_TYPE键值对 |
| [has_item_key_unit_command_type_kv](#has_item_key_unit_command_type_kv) | 判断物品编号是否存在UNIT_COMMAND_TYPE键值对 |
| [has_ability_key_unit_command_type_kv](#has_ability_key_unit_command_type_kv) | 判断技能编号是否存在UNIT_COMMAND_TYPE键值对 |
| [has_kv_pair_mini_map_color_type](#has_kv_pair_mini_map_color_type) | 判断是否存在MINI_MAP_COLOR_TYPE键值对 |
| [has_unit_key_mini_map_color_type_kv](#has_unit_key_mini_map_color_type_kv) | 判断单位编号是否存在MINI_MAP_COLOR_TYPE键值对 |
| [has_item_key_mini_map_color_type_kv](#has_item_key_mini_map_color_type_kv) | 判断物品编号是否存在MINI_MAP_COLOR_TYPE键值对 |
| [has_ability_key_mini_map_color_type_kv](#has_ability_key_mini_map_color_type_kv) | 判断技能编号是否存在MINI_MAP_COLOR_TYPE键值对 |
| [has_kv_pair_unit_behavior](#has_kv_pair_unit_behavior) | 判断是否存在UNIT_BEHAVIOR键值对 |
| [has_unit_key_unit_behavior_kv](#has_unit_key_unit_behavior_kv) | 判断单位编号是否存在UNIT_BEHAVIOR键值对 |
| [has_item_key_unit_behavior_kv](#has_item_key_unit_behavior_kv) | 判断物品编号是否存在UNIT_BEHAVIOR键值对 |
| [has_ability_key_unit_behavior_kv](#has_ability_key_unit_behavior_kv) | 判断技能编号是否存在UNIT_BEHAVIOR键值对 |
| [has_kv_pair_curved_path](#has_kv_pair_curved_path) | 判断是否存在CURVED_PATH键值对 |
| [has_unit_key_curved_path_kv](#has_unit_key_curved_path_kv) | 判断单位编号是否存在CURVED_PATH键值对 |
| [has_item_key_curved_path_kv](#has_item_key_curved_path_kv) | 判断物品编号是否存在CURVED_PATH键值对 |
| [has_ability_key_curved_path_kv](#has_ability_key_curved_path_kv) | 判断技能编号是否存在CURVED_PATH键值对 |
| [has_kv_pair_curved_path_3d](#has_kv_pair_curved_path_3d) | 判断是否存在CURVED_PATH_3D键值对 |
| [has_unit_key_curved_path_3d_kv](#has_unit_key_curved_path_3d_kv) | 判断单位编号是否存在CURVED_PATH_3D键值对 |
| [has_item_key_curved_path_3d_kv](#has_item_key_curved_path_3d_kv) | 判断物品编号是否存在CURVED_PATH_3D键值对 |
| [has_ability_key_curved_path_3d_kv](#has_ability_key_curved_path_3d_kv) | 判断技能编号是否存在CURVED_PATH_3D键值对 |
| [get_kv_pair_value_boolean](#get_kv_pair_value_boolean) | 获取BOOLEAN键值对 |
| [get_kv_pair_value_integer](#get_kv_pair_value_integer) | 获取INTEGER键值对 |
| [get_kv_pair_value_float](#get_kv_pair_value_float) | 获取FLOAT键值对 |
| [get_kv_pair_value_string](#get_kv_pair_value_string) | 获取STRING键值对 |
| [get_kv_pair_value_ui_comp](#get_kv_pair_value_ui_comp) | 获取UI_COMP键值对 |
| [get_kv_pair_value_ui_comp_type](#get_kv_pair_value_ui_comp_type) | 获取UI_COMP_TYPE键值对 |
| [get_kv_pair_value_ui_comp_event_type](#get_kv_pair_value_ui_comp_event_type) | 获取UI_COMP_EVENT_TYPE键值对 |
| [get_kv_pair_value_ui_comp_attr](#get_kv_pair_value_ui_comp_attr) | 获取UI_COMP_ATTR键值对 |
| [get_kv_pair_value_ui_comp_align_type](#get_kv_pair_value_ui_comp_align_type) | 获取UI_COMP_ALIGN_TYPE键值对 |
| [get_kv_pair_value_ui_prefab](#get_kv_pair_value_ui_prefab) | 获取UI_PREFAB键值对 |
| [get_kv_pair_value_ui_prefab_instance](#get_kv_pair_value_ui_prefab_instance) | 获取UI_PREFAB_INSTANCE键值对 |
| [get_kv_pair_value_ui_prefab_ins_uid](#get_kv_pair_value_ui_prefab_ins_uid) | 获取UI_PREFAB_INS_UID键值对 |
| [get_kv_pair_value_ui_direction](#get_kv_pair_value_ui_direction) | 获取UI_DIRECTION键值对 |
| [get_kv_pair_value_ui_model_camera_mod](#get_kv_pair_value_ui_model_camera_mod) | 获取UI_MODEL_CAMERA_MOD键值对 |
| [get_kv_pair_value_ui_btn_status](#get_kv_pair_value_ui_btn_status) | 获取UI_BTN_STATUS键值对 |
| [get_kv_pair_value_ui_scrollview_type](#get_kv_pair_value_ui_scrollview_type) | 获取UI_SCROLLVIEW_TYPE键值对 |
| [get_kv_pair_value_ui_anim](#get_kv_pair_value_ui_anim) | 获取UI_ANIM键值对 |
| [get_kv_pair_value_ui_anim_curve](#get_kv_pair_value_ui_anim_curve) | 获取UI_ANIM_CURVE键值对 |
| [get_kv_pair_value_audio_channel](#get_kv_pair_value_audio_channel) | 获取AUDIO_CHANNEL键值对 |
| [get_kv_pair_value_unit_entity](#get_kv_pair_value_unit_entity) | 获取UNIT_ENTITY键值对 |
| [get_kv_pair_value_unit_group](#get_kv_pair_value_unit_group) | 获取UNIT_GROUP键值对 |
| [get_kv_pair_value_unit_name](#get_kv_pair_value_unit_name) | 获取UNIT_NAME键值对 |
| [get_kv_pair_value_unit_name_pool](#get_kv_pair_value_unit_name_pool) | 获取UNIT_NAME_POOL键值对 |
| [get_kv_pair_value_unit_write_attribute](#get_kv_pair_value_unit_write_attribute) | 获取UNIT_WRITE_ATTRIBUTE键值对 |
| [get_kv_pair_value_attr_element](#get_kv_pair_value_attr_element) | 获取ATTR_ELEMENT键值对 |
| [get_kv_pair_value_attr_element_read](#get_kv_pair_value_attr_element_read) | 获取ATTR_ELEMENT_READ键值对 |
| [get_kv_pair_value_mover_entity](#get_kv_pair_value_mover_entity) | 获取MOVER_ENTITY键值对 |
| [get_kv_pair_value_image_quality](#get_kv_pair_value_image_quality) | 获取IMAGE_QUALITY键值对 |
| [get_kv_pair_value_window_type_setting](#get_kv_pair_value_window_type_setting) | 获取WINDOW_TYPE_SETTING键值对 |
| [get_kv_pair_value_item_entity](#get_kv_pair_value_item_entity) | 获取ITEM_ENTITY键值对 |
| [get_kv_pair_value_item_group](#get_kv_pair_value_item_group) | 获取ITEM_GROUP键值对 |
| [get_kv_pair_value_item_name](#get_kv_pair_value_item_name) | 获取ITEM_NAME键值对 |
| [get_kv_pair_value_ability](#get_kv_pair_value_ability) | 获取ABILITY键值对 |
| [get_kv_pair_value_ability_type](#get_kv_pair_value_ability_type) | 获取ABILITY_TYPE键值对 |
| [get_kv_pair_value_ability_cast_type](#get_kv_pair_value_ability_cast_type) | 获取ABILITY_CAST_TYPE键值对 |
| [get_kv_pair_value_ability_name](#get_kv_pair_value_ability_name) | 获取ABILITY_NAME键值对 |
| [get_kv_pair_value_skill_pointer_type](#get_kv_pair_value_skill_pointer_type) | 获取SKILL_POINTER_TYPE键值对 |
| [get_kv_pair_value_modifier_entity](#get_kv_pair_value_modifier_entity) | 获取MODIFIER_ENTITY键值对 |
| [get_kv_pair_value_modifier_type](#get_kv_pair_value_modifier_type) | 获取MODIFIER_TYPE键值对 |
| [get_kv_pair_value_modifier_effect_type](#get_kv_pair_value_modifier_effect_type) | 获取MODIFIER_EFFECT_TYPE键值对 |
| [get_kv_pair_value_modifier](#get_kv_pair_value_modifier) | 获取MODIFIER键值对 |
| [get_kv_pair_value_projectile](#get_kv_pair_value_projectile) | 获取PROJECTILE键值对 |
| [get_kv_pair_value_projectile_entity](#get_kv_pair_value_projectile_entity) | 获取PROJECTILE_ENTITY键值对 |
| [get_kv_pair_value_projectile_group](#get_kv_pair_value_projectile_group) | 获取PROJECTILE_GROUP键值对 |
| [get_kv_pair_value_destructible_entity](#get_kv_pair_value_destructible_entity) | 获取DESTRUCTIBLE_ENTITY键值对 |
| [get_kv_pair_value_destructible_name](#get_kv_pair_value_destructible_name) | 获取DESTRUCTIBLE_NAME键值对 |
| [get_kv_pair_value_sound_entity](#get_kv_pair_value_sound_entity) | 获取SOUND_ENTITY键值对 |
| [get_kv_pair_value_audio_key](#get_kv_pair_value_audio_key) | 获取AUDIO_KEY键值对 |
| [get_kv_pair_value_game_mode](#get_kv_pair_value_game_mode) | 获取GAME_MODE键值对 |
| [get_kv_pair_value_player](#get_kv_pair_value_player) | 获取PLAYER键值对 |
| [get_kv_pair_value_player_group](#get_kv_pair_value_player_group) | 获取PLAYER_GROUP键值对 |
| [get_kv_pair_value_role_res_key](#get_kv_pair_value_role_res_key) | 获取ROLE_RES_KEY键值对 |
| [get_kv_pair_value_role_status](#get_kv_pair_value_role_status) | 获取ROLE_STATUS键值对 |
| [get_kv_pair_value_role_type](#get_kv_pair_value_role_type) | 获取ROLE_TYPE键值对 |
| [get_kv_pair_value_role_relation](#get_kv_pair_value_role_relation) | 获取ROLE_RELATION键值对 |
| [get_kv_pair_value_team](#get_kv_pair_value_team) | 获取TEAM键值对 |
| [get_kv_pair_value_point](#get_kv_pair_value_point) | 获取POINT键值对 |
| [get_kv_pair_value_vector3](#get_kv_pair_value_vector3) | 获取VECTOR3键值对 |
| [get_kv_pair_value_rotation](#get_kv_pair_value_rotation) | 获取ROTATION键值对 |
| [get_kv_pair_value_point_list](#get_kv_pair_value_point_list) | 获取POINT_LIST键值对 |
| [get_kv_pair_value_rectangle](#get_kv_pair_value_rectangle) | 获取RECTANGLE键值对 |
| [get_kv_pair_value_round_area](#get_kv_pair_value_round_area) | 获取ROUND_AREA键值对 |
| [get_kv_pair_value_polygon](#get_kv_pair_value_polygon) | 获取POLYGON键值对 |
| [get_kv_pair_value_camera](#get_kv_pair_value_camera) | 获取CAMERA键值对 |
| [get_kv_pair_value_camline](#get_kv_pair_value_camline) | 获取CAMLINE键值对 |
| [get_kv_pair_value_point_light](#get_kv_pair_value_point_light) | 获取POINT_LIGHT键值对 |
| [get_kv_pair_value_spot_light](#get_kv_pair_value_spot_light) | 获取SPOT_LIGHT键值对 |
| [get_kv_pair_value_fog](#get_kv_pair_value_fog) | 获取FOG键值对 |
| [get_kv_pair_value_scene_sound](#get_kv_pair_value_scene_sound) | 获取SCENE_SOUND键值对 |
| [get_kv_pair_value_model](#get_kv_pair_value_model) | 获取MODEL键值对 |
| [get_kv_pair_value_sfx_entity](#get_kv_pair_value_sfx_entity) | 获取SFX_ENTITY键值对 |
| [get_kv_pair_value_sfx_key](#get_kv_pair_value_sfx_key) | 获取SFX_KEY键值对 |
| [get_kv_pair_value_link_sfx_entity](#get_kv_pair_value_link_sfx_entity) | 获取LINK_SFX_ENTITY键值对 |
| [get_kv_pair_value_link_sfx_key](#get_kv_pair_value_link_sfx_key) | 获取LINK_SFX_KEY键值对 |
| [get_kv_pair_value_cursor_key](#get_kv_pair_value_cursor_key) | 获取CURSOR_KEY键值对 |
| [get_kv_pair_value_angle](#get_kv_pair_value_angle) | 获取ANGLE键值对 |
| [get_kv_pair_value_texture](#get_kv_pair_value_texture) | 获取TEXTURE键值对 |
| [get_kv_pair_value_sequence](#get_kv_pair_value_sequence) | 获取SEQUENCE键值对 |
| [get_kv_pair_value_physics_object](#get_kv_pair_value_physics_object) | 获取PHYSICS_OBJECT键值对 |
| [get_kv_pair_value_physics_entity](#get_kv_pair_value_physics_entity) | 获取PHYSICS_ENTITY键值对 |
| [get_kv_pair_value_physics_object_key](#get_kv_pair_value_physics_object_key) | 获取PHYSICS_OBJECT_KEY键值对 |
| [get_kv_pair_value_physics_entity_key](#get_kv_pair_value_physics_entity_key) | 获取PHYSICS_ENTITY_KEY键值对 |
| [get_kv_pair_value_rigid_body](#get_kv_pair_value_rigid_body) | 获取RIGID_BODY键值对 |
| [get_kv_pair_value_rigid_body_group](#get_kv_pair_value_rigid_body_group) | 获取RIGID_BODY_GROUP键值对 |
| [get_kv_pair_value_collider](#get_kv_pair_value_collider) | 获取COLLIDER键值对 |
| [get_kv_pair_value_joint](#get_kv_pair_value_joint) | 获取JOINT键值对 |
| [get_kv_pair_value_reaction](#get_kv_pair_value_reaction) | 获取REACTION键值对 |
| [get_kv_pair_value_reaction_group](#get_kv_pair_value_reaction_group) | 获取REACTION_GROUP键值对 |
| [get_kv_pair_value_dynamic_trigger_instance](#get_kv_pair_value_dynamic_trigger_instance) | 获取DYNAMIC_TRIGGER_INSTANCE键值对 |
| [get_kv_pair_value_table](#get_kv_pair_value_table) | 获取TABLE键值对 |
| [get_kv_pair_value_random_pool](#get_kv_pair_value_random_pool) | 获取RANDOM_POOL键值对 |
| [get_kv_pair_value_scene_ui](#get_kv_pair_value_scene_ui) | 获取SCENE_UI键值对 |
| [get_kv_pair_value_damage_type](#get_kv_pair_value_damage_type) | 获取DAMAGE_TYPE键值对 |
| [get_kv_pair_value_harm_text_type_new](#get_kv_pair_value_harm_text_type_new) | 获取HARM_TEXT_TYPE_NEW键值对 |
| [get_kv_pair_value_font_type](#get_kv_pair_value_font_type) | 获取FONT_TYPE键值对 |
| [get_kv_pair_value_jump_word_track](#get_kv_pair_value_jump_word_track) | 获取JUMP_WORD_TRACK键值对 |
| [get_kv_pair_value_new_timer](#get_kv_pair_value_new_timer) | 获取NEW_TIMER键值对 |
| [get_kv_pair_value_tech_key](#get_kv_pair_value_tech_key) | 获取TECH_KEY键值对 |
| [get_kv_pair_value_store_key](#get_kv_pair_value_store_key) | 获取STORE_KEY键值对 |
| [get_kv_pair_value_keyboard_key](#get_kv_pair_value_keyboard_key) | 获取KEYBOARD_KEY键值对 |
| [get_kv_pair_value_func_keyboard_key](#get_kv_pair_value_func_keyboard_key) | 获取FUNC_KEYBOARD_KEY键值对 |
| [get_kv_pair_value_mouse_key](#get_kv_pair_value_mouse_key) | 获取MOUSE_KEY键值对 |
| [get_kv_pair_value_mouse_wheel](#get_kv_pair_value_mouse_wheel) | 获取MOUSE_WHEEL键值对 |
| [get_kv_pair_value_post_effect](#get_kv_pair_value_post_effect) | 获取POST_EFFECT键值对 |
| [get_kv_pair_value_unit_type](#get_kv_pair_value_unit_type) | 获取UNIT_TYPE键值对 |
| [get_kv_pair_value_unit_command_type](#get_kv_pair_value_unit_command_type) | 获取UNIT_COMMAND_TYPE键值对 |
| [get_kv_pair_value_mini_map_color_type](#get_kv_pair_value_mini_map_color_type) | 获取MINI_MAP_COLOR_TYPE键值对 |
| [get_kv_pair_value_unit_behavior](#get_kv_pair_value_unit_behavior) | 获取UNIT_BEHAVIOR键值对 |
| [get_kv_pair_value_curved_path](#get_kv_pair_value_curved_path) | 获取CURVED_PATH键值对 |
| [get_kv_pair_value_curved_path_3d](#get_kv_pair_value_curved_path_3d) | 获取CURVED_PATH_3D键值对 |
| [get_trigger_variable_by_type](#get_trigger_variable_by_type) | 获取全局触发器非数组变量（指定类型） |
| [get_trigger_list_variable_by_type](#get_trigger_list_variable_by_type) | 获取全局触发器数组变量子项（指定类型） |
| [get_trigger_variable_boolean](#get_trigger_variable_boolean) | 获取全局触发器BOOLEAN非数组变量 |
| [get_trigger_actor_variable_boolean](#get_trigger_actor_variable_boolean) | 获取触发器BOOLEAN非数组 组变量 |
| [get_trigger_list_variable_boolean](#get_trigger_list_variable_boolean) | 获取全局触发器BOOLEAN数组变量子项 |
| [get_trigger_list_actor_variable_boolean](#get_trigger_list_actor_variable_boolean) | 获取触发器BOOLEAN数组 组变量子项 |
| [get_trigger_list_variable_all_boolean](#get_trigger_list_variable_all_boolean) | 获取全局触发器BOOLEAN数组变量 |
| [get_trigger_list_actor_variable_all_boolean](#get_trigger_list_actor_variable_all_boolean) | 获取触发器BOOLEAN 组变量数组 |
| [get_trigger_variable_integer](#get_trigger_variable_integer) | 获取全局触发器INTEGER非数组变量 |
| [get_trigger_actor_variable_integer](#get_trigger_actor_variable_integer) | 获取触发器INTEGER非数组 组变量 |
| [get_trigger_list_variable_integer](#get_trigger_list_variable_integer) | 获取全局触发器INTEGER数组变量子项 |
| [get_trigger_list_actor_variable_integer](#get_trigger_list_actor_variable_integer) | 获取触发器INTEGER数组 组变量子项 |
| [get_trigger_list_variable_all_integer](#get_trigger_list_variable_all_integer) | 获取全局触发器INTEGER数组变量 |
| [get_trigger_list_actor_variable_all_integer](#get_trigger_list_actor_variable_all_integer) | 获取触发器INTEGER 组变量数组 |
| [get_trigger_variable_float](#get_trigger_variable_float) | 获取全局触发器FLOAT非数组变量 |
| [get_trigger_actor_variable_float](#get_trigger_actor_variable_float) | 获取触发器FLOAT非数组 组变量 |
| [get_trigger_list_variable_float](#get_trigger_list_variable_float) | 获取全局触发器FLOAT数组变量子项 |
| [get_trigger_list_actor_variable_float](#get_trigger_list_actor_variable_float) | 获取触发器FLOAT数组 组变量子项 |
| [get_trigger_list_variable_all_float](#get_trigger_list_variable_all_float) | 获取全局触发器FLOAT数组变量 |
| [get_trigger_list_actor_variable_all_float](#get_trigger_list_actor_variable_all_float) | 获取触发器FLOAT 组变量数组 |
| [get_trigger_variable_string](#get_trigger_variable_string) | 获取全局触发器STRING非数组变量 |
| [get_trigger_actor_variable_string](#get_trigger_actor_variable_string) | 获取触发器STRING非数组 组变量 |
| [get_trigger_list_variable_string](#get_trigger_list_variable_string) | 获取全局触发器STRING数组变量子项 |
| [get_trigger_list_actor_variable_string](#get_trigger_list_actor_variable_string) | 获取触发器STRING数组 组变量子项 |
| [get_trigger_list_variable_all_string](#get_trigger_list_variable_all_string) | 获取全局触发器STRING数组变量 |
| [get_trigger_list_actor_variable_all_string](#get_trigger_list_actor_variable_all_string) | 获取触发器STRING 组变量数组 |
| [get_trigger_variable_ui_comp](#get_trigger_variable_ui_comp) | 获取全局触发器UI_COMP非数组变量 |
| [get_trigger_actor_variable_ui_comp](#get_trigger_actor_variable_ui_comp) | 获取触发器UI_COMP非数组 组变量 |
| [get_trigger_list_variable_ui_comp](#get_trigger_list_variable_ui_comp) | 获取全局触发器UI_COMP数组变量子项 |
| [get_trigger_list_actor_variable_ui_comp](#get_trigger_list_actor_variable_ui_comp) | 获取触发器UI_COMP数组 组变量子项 |
| [get_trigger_list_variable_all_ui_comp](#get_trigger_list_variable_all_ui_comp) | 获取全局触发器UI_COMP数组变量 |
| [get_trigger_list_actor_variable_all_ui_comp](#get_trigger_list_actor_variable_all_ui_comp) | 获取触发器UI_COMP 组变量数组 |
| [get_trigger_variable_ui_comp_type](#get_trigger_variable_ui_comp_type) | 获取全局触发器UI_COMP_TYPE非数组变量 |
| [get_trigger_actor_variable_ui_comp_type](#get_trigger_actor_variable_ui_comp_type) | 获取触发器UI_COMP_TYPE非数组 组变量 |
| [get_trigger_list_variable_ui_comp_type](#get_trigger_list_variable_ui_comp_type) | 获取全局触发器UI_COMP_TYPE数组变量子项 |
| [get_trigger_list_actor_variable_ui_comp_type](#get_trigger_list_actor_variable_ui_comp_type) | 获取触发器UI_COMP_TYPE数组 组变量子项 |
| [get_trigger_list_variable_all_ui_comp_type](#get_trigger_list_variable_all_ui_comp_type) | 获取全局触发器UI_COMP_TYPE数组变量 |
| [get_trigger_list_actor_variable_all_ui_comp_type](#get_trigger_list_actor_variable_all_ui_comp_type) | 获取触发器UI_COMP_TYPE 组变量数组 |
| [get_trigger_variable_ui_comp_event_type](#get_trigger_variable_ui_comp_event_type) | 获取全局触发器UI_COMP_EVENT_TYPE非数组变量 |
| [get_trigger_actor_variable_ui_comp_event_type](#get_trigger_actor_variable_ui_comp_event_type) | 获取触发器UI_COMP_EVENT_TYPE非数组 组变量 |
| [get_trigger_list_variable_ui_comp_event_type](#get_trigger_list_variable_ui_comp_event_type) | 获取全局触发器UI_COMP_EVENT_TYPE数组变量子项 |
| [get_trigger_list_actor_variable_ui_comp_event_type](#get_trigger_list_actor_variable_ui_comp_event_type) | 获取触发器UI_COMP_EVENT_TYPE数组 组变量子项 |
| [get_trigger_list_variable_all_ui_comp_event_type](#get_trigger_list_variable_all_ui_comp_event_type) | 获取全局触发器UI_COMP_EVENT_TYPE数组变量 |
| [get_trigger_list_actor_variable_all_ui_comp_event_type](#get_trigger_list_actor_variable_all_ui_comp_event_type) | 获取触发器UI_COMP_EVENT_TYPE 组变量数组 |
| [get_trigger_variable_ui_comp_align_type](#get_trigger_variable_ui_comp_align_type) | 获取全局触发器UI_COMP_ALIGN_TYPE非数组变量 |
| [get_trigger_actor_variable_ui_comp_align_type](#get_trigger_actor_variable_ui_comp_align_type) | 获取触发器UI_COMP_ALIGN_TYPE非数组 组变量 |
| [get_trigger_list_variable_ui_comp_align_type](#get_trigger_list_variable_ui_comp_align_type) | 获取全局触发器UI_COMP_ALIGN_TYPE数组变量子项 |
| [get_trigger_list_actor_variable_ui_comp_align_type](#get_trigger_list_actor_variable_ui_comp_align_type) | 获取触发器UI_COMP_ALIGN_TYPE数组 组变量子项 |
| [get_trigger_list_variable_all_ui_comp_align_type](#get_trigger_list_variable_all_ui_comp_align_type) | 获取全局触发器UI_COMP_ALIGN_TYPE数组变量 |
| [get_trigger_list_actor_variable_all_ui_comp_align_type](#get_trigger_list_actor_variable_all_ui_comp_align_type) | 获取触发器UI_COMP_ALIGN_TYPE 组变量数组 |
| [get_trigger_variable_ui_prefab](#get_trigger_variable_ui_prefab) | 获取全局触发器UI_PREFAB非数组变量 |
| [get_trigger_actor_variable_ui_prefab](#get_trigger_actor_variable_ui_prefab) | 获取触发器UI_PREFAB非数组 组变量 |
| [get_trigger_list_variable_ui_prefab](#get_trigger_list_variable_ui_prefab) | 获取全局触发器UI_PREFAB数组变量子项 |
| [get_trigger_list_actor_variable_ui_prefab](#get_trigger_list_actor_variable_ui_prefab) | 获取触发器UI_PREFAB数组 组变量子项 |
| [get_trigger_list_variable_all_ui_prefab](#get_trigger_list_variable_all_ui_prefab) | 获取全局触发器UI_PREFAB数组变量 |
| [get_trigger_list_actor_variable_all_ui_prefab](#get_trigger_list_actor_variable_all_ui_prefab) | 获取触发器UI_PREFAB 组变量数组 |
| [get_trigger_variable_ui_prefab_instance](#get_trigger_variable_ui_prefab_instance) | 获取全局触发器UI_PREFAB_INSTANCE非数组变量 |
| [get_trigger_actor_variable_ui_prefab_instance](#get_trigger_actor_variable_ui_prefab_instance) | 获取触发器UI_PREFAB_INSTANCE非数组 组变量 |
| [get_trigger_list_variable_ui_prefab_instance](#get_trigger_list_variable_ui_prefab_instance) | 获取全局触发器UI_PREFAB_INSTANCE数组变量子项 |
| [get_trigger_list_actor_variable_ui_prefab_instance](#get_trigger_list_actor_variable_ui_prefab_instance) | 获取触发器UI_PREFAB_INSTANCE数组 组变量子项 |
| [get_trigger_list_variable_all_ui_prefab_instance](#get_trigger_list_variable_all_ui_prefab_instance) | 获取全局触发器UI_PREFAB_INSTANCE数组变量 |
| [get_trigger_list_actor_variable_all_ui_prefab_instance](#get_trigger_list_actor_variable_all_ui_prefab_instance) | 获取触发器UI_PREFAB_INSTANCE 组变量数组 |
| [get_trigger_variable_ui_prefab_ins_uid](#get_trigger_variable_ui_prefab_ins_uid) | 获取全局触发器UI_PREFAB_INS_UID非数组变量 |
| [get_trigger_actor_variable_ui_prefab_ins_uid](#get_trigger_actor_variable_ui_prefab_ins_uid) | 获取触发器UI_PREFAB_INS_UID非数组 组变量 |
| [get_trigger_list_variable_ui_prefab_ins_uid](#get_trigger_list_variable_ui_prefab_ins_uid) | 获取全局触发器UI_PREFAB_INS_UID数组变量子项 |
| [get_trigger_list_actor_variable_ui_prefab_ins_uid](#get_trigger_list_actor_variable_ui_prefab_ins_uid) | 获取触发器UI_PREFAB_INS_UID数组 组变量子项 |
| [get_trigger_list_variable_all_ui_prefab_ins_uid](#get_trigger_list_variable_all_ui_prefab_ins_uid) | 获取全局触发器UI_PREFAB_INS_UID数组变量 |
| [get_trigger_list_actor_variable_all_ui_prefab_ins_uid](#get_trigger_list_actor_variable_all_ui_prefab_ins_uid) | 获取触发器UI_PREFAB_INS_UID 组变量数组 |
| [get_trigger_variable_ui_direction](#get_trigger_variable_ui_direction) | 获取全局触发器UI_DIRECTION非数组变量 |
| [get_trigger_actor_variable_ui_direction](#get_trigger_actor_variable_ui_direction) | 获取触发器UI_DIRECTION非数组 组变量 |
| [get_trigger_list_variable_ui_direction](#get_trigger_list_variable_ui_direction) | 获取全局触发器UI_DIRECTION数组变量子项 |
| [get_trigger_list_actor_variable_ui_direction](#get_trigger_list_actor_variable_ui_direction) | 获取触发器UI_DIRECTION数组 组变量子项 |
| [get_trigger_list_variable_all_ui_direction](#get_trigger_list_variable_all_ui_direction) | 获取全局触发器UI_DIRECTION数组变量 |
| [get_trigger_list_actor_variable_all_ui_direction](#get_trigger_list_actor_variable_all_ui_direction) | 获取触发器UI_DIRECTION 组变量数组 |
| [get_trigger_variable_ui_model_camera_mod](#get_trigger_variable_ui_model_camera_mod) | 获取全局触发器UI_MODEL_CAMERA_MOD非数组变量 |
| [get_trigger_actor_variable_ui_model_camera_mod](#get_trigger_actor_variable_ui_model_camera_mod) | 获取触发器UI_MODEL_CAMERA_MOD非数组 组变量 |
| [get_trigger_list_variable_ui_model_camera_mod](#get_trigger_list_variable_ui_model_camera_mod) | 获取全局触发器UI_MODEL_CAMERA_MOD数组变量子项 |
| [get_trigger_list_actor_variable_ui_model_camera_mod](#get_trigger_list_actor_variable_ui_model_camera_mod) | 获取触发器UI_MODEL_CAMERA_MOD数组 组变量子项 |
| [get_trigger_list_variable_all_ui_model_camera_mod](#get_trigger_list_variable_all_ui_model_camera_mod) | 获取全局触发器UI_MODEL_CAMERA_MOD数组变量 |
| [get_trigger_list_actor_variable_all_ui_model_camera_mod](#get_trigger_list_actor_variable_all_ui_model_camera_mod) | 获取触发器UI_MODEL_CAMERA_MOD 组变量数组 |
| [get_trigger_variable_ui_btn_status](#get_trigger_variable_ui_btn_status) | 获取全局触发器UI_BTN_STATUS非数组变量 |
| [get_trigger_actor_variable_ui_btn_status](#get_trigger_actor_variable_ui_btn_status) | 获取触发器UI_BTN_STATUS非数组 组变量 |
| [get_trigger_list_variable_ui_btn_status](#get_trigger_list_variable_ui_btn_status) | 获取全局触发器UI_BTN_STATUS数组变量子项 |
| [get_trigger_list_actor_variable_ui_btn_status](#get_trigger_list_actor_variable_ui_btn_status) | 获取触发器UI_BTN_STATUS数组 组变量子项 |
| [get_trigger_list_variable_all_ui_btn_status](#get_trigger_list_variable_all_ui_btn_status) | 获取全局触发器UI_BTN_STATUS数组变量 |
| [get_trigger_list_actor_variable_all_ui_btn_status](#get_trigger_list_actor_variable_all_ui_btn_status) | 获取触发器UI_BTN_STATUS 组变量数组 |
| [get_trigger_variable_ui_scrollview_type](#get_trigger_variable_ui_scrollview_type) | 获取全局触发器UI_SCROLLVIEW_TYPE非数组变量 |
| [get_trigger_actor_variable_ui_scrollview_type](#get_trigger_actor_variable_ui_scrollview_type) | 获取触发器UI_SCROLLVIEW_TYPE非数组 组变量 |
| [get_trigger_list_variable_ui_scrollview_type](#get_trigger_list_variable_ui_scrollview_type) | 获取全局触发器UI_SCROLLVIEW_TYPE数组变量子项 |
| [get_trigger_list_actor_variable_ui_scrollview_type](#get_trigger_list_actor_variable_ui_scrollview_type) | 获取触发器UI_SCROLLVIEW_TYPE数组 组变量子项 |
| [get_trigger_list_variable_all_ui_scrollview_type](#get_trigger_list_variable_all_ui_scrollview_type) | 获取全局触发器UI_SCROLLVIEW_TYPE数组变量 |
| [get_trigger_list_actor_variable_all_ui_scrollview_type](#get_trigger_list_actor_variable_all_ui_scrollview_type) | 获取触发器UI_SCROLLVIEW_TYPE 组变量数组 |
| [get_trigger_variable_ui_anim](#get_trigger_variable_ui_anim) | 获取全局触发器UI_ANIM非数组变量 |
| [get_trigger_actor_variable_ui_anim](#get_trigger_actor_variable_ui_anim) | 获取触发器UI_ANIM非数组 组变量 |
| [get_trigger_list_variable_ui_anim](#get_trigger_list_variable_ui_anim) | 获取全局触发器UI_ANIM数组变量子项 |
| [get_trigger_list_actor_variable_ui_anim](#get_trigger_list_actor_variable_ui_anim) | 获取触发器UI_ANIM数组 组变量子项 |
| [get_trigger_list_variable_all_ui_anim](#get_trigger_list_variable_all_ui_anim) | 获取全局触发器UI_ANIM数组变量 |
| [get_trigger_list_actor_variable_all_ui_anim](#get_trigger_list_actor_variable_all_ui_anim) | 获取触发器UI_ANIM 组变量数组 |
| [get_trigger_variable_ui_anim_curve](#get_trigger_variable_ui_anim_curve) | 获取全局触发器UI_ANIM_CURVE非数组变量 |
| [get_trigger_actor_variable_ui_anim_curve](#get_trigger_actor_variable_ui_anim_curve) | 获取触发器UI_ANIM_CURVE非数组 组变量 |
| [get_trigger_list_variable_ui_anim_curve](#get_trigger_list_variable_ui_anim_curve) | 获取全局触发器UI_ANIM_CURVE数组变量子项 |
| [get_trigger_list_actor_variable_ui_anim_curve](#get_trigger_list_actor_variable_ui_anim_curve) | 获取触发器UI_ANIM_CURVE数组 组变量子项 |
| [get_trigger_list_variable_all_ui_anim_curve](#get_trigger_list_variable_all_ui_anim_curve) | 获取全局触发器UI_ANIM_CURVE数组变量 |
| [get_trigger_list_actor_variable_all_ui_anim_curve](#get_trigger_list_actor_variable_all_ui_anim_curve) | 获取触发器UI_ANIM_CURVE 组变量数组 |
| [get_trigger_variable_audio_channel](#get_trigger_variable_audio_channel) | 获取全局触发器AUDIO_CHANNEL非数组变量 |
| [get_trigger_actor_variable_audio_channel](#get_trigger_actor_variable_audio_channel) | 获取触发器AUDIO_CHANNEL非数组 组变量 |
| [get_trigger_list_variable_audio_channel](#get_trigger_list_variable_audio_channel) | 获取全局触发器AUDIO_CHANNEL数组变量子项 |
| [get_trigger_list_actor_variable_audio_channel](#get_trigger_list_actor_variable_audio_channel) | 获取触发器AUDIO_CHANNEL数组 组变量子项 |
| [get_trigger_list_variable_all_audio_channel](#get_trigger_list_variable_all_audio_channel) | 获取全局触发器AUDIO_CHANNEL数组变量 |
| [get_trigger_list_actor_variable_all_audio_channel](#get_trigger_list_actor_variable_all_audio_channel) | 获取触发器AUDIO_CHANNEL 组变量数组 |
| [get_trigger_variable_unit_entity](#get_trigger_variable_unit_entity) | 获取全局触发器UNIT_ENTITY非数组变量 |
| [api_add_quick_tag](#api_add_quick_tag) | 添加快速标签 |
| [api_remove_quick_tag](#api_remove_quick_tag) | 移除快速标签 |
| [api_has_quick_tag](#api_has_quick_tag) | 检查是否有快速标签 |
| [set_prefab_key_xxx_kv](#set_prefab_key_xxx_kv) | 预设库 添加kv键值对 |
| [add_unit_xxx_kv](#add_unit_xxx_kv) | unit添加kv键值对 |
| [add_item_xxx_kv](#add_item_xxx_kv) | item添加kv键值对 |
| [add_destructible_xxx_kv](#add_destructible_xxx_kv) | destructible添加kv键值对 |
| [add_ability_xxx_kv](#add_ability_xxx_kv) | ability添加kv键值对 |
| [add_modifier_xxx_kv](#add_modifier_xxx_kv) | modifier添加kv键值对 |
| [set_prefab_key_ui_gridview_type_kv](#set_prefab_key_ui_gridview_type_kv) | 预设库 添加UI_GRIDVIEW_TYPE键值对 |
| [set_prefab_key_ui_gridview_bar_type_kv](#set_prefab_key_ui_gridview_bar_type_kv) | 预设库 添加UI_GRIDVIEW_BAR_TYPE键值对 |
| [set_prefab_key_ui_effect_camera_mode_kv](#set_prefab_key_ui_effect_camera_mode_kv) | 预设库 添加UI_EFFECT_CAMERA_MODE键值对 |
| [set_prefab_key_ui_equip_slot_use_type_kv](#set_prefab_key_ui_equip_slot_use_type_kv) | 预设库 添加UI_EQUIP_SLOT_USE_TYPE键值对 |
| [set_prefab_key_ui_equip_slot_drag_type_kv](#set_prefab_key_ui_equip_slot_drag_type_kv) | 预设库 添加UI_EQUIP_SLOT_DRAG_TYPE键值对 |
| [set_prefab_key_ui_layout_clipping_type_kv](#set_prefab_key_ui_layout_clipping_type_kv) | 预设库 添加UI_LAYOUT_CLIPPING_TYPE键值对 |
| [set_prefab_key_ui_text_over_length_handling_type_kv](#set_prefab_key_ui_text_over_length_handling_type_kv) | 预设库 添加UI_TEXT_OVER_LENGTH_HANDLING_TYPE键值对 |
| [set_prefab_key_ui_pos_adapt_mode_kv](#set_prefab_key_ui_pos_adapt_mode_kv) | 预设库 添加UI_POS_ADAPT_MODE键值对 |
| [set_prefab_key_ui_chat_send_channel_kv](#set_prefab_key_ui_chat_send_channel_kv) | 预设库 添加UI_CHAT_SEND_CHANNEL键值对 |
| [set_prefab_key_ui_chat_recv_channel_kv](#set_prefab_key_ui_chat_recv_channel_kv) | 预设库 添加UI_CHAT_RECV_CHANNEL键值对 |
| [set_prefab_key_ui_anim_play_mode_kv](#set_prefab_key_ui_anim_play_mode_kv) | 预设库 添加UI_ANIM_PLAY_MODE键值对 |
| [set_prefab_key_ui_text_font_name_kv](#set_prefab_key_ui_text_font_name_kv) | 预设库 添加UI_TEXT_FONT_NAME键值对 |
| [set_prefab_key_ui_eca_anim_type_kv](#set_prefab_key_ui_eca_anim_type_kv) | 预设库 添加UI_ECA_ANIM_TYPE键值对 |
| [set_prefab_key_local_unit_group_kv](#set_prefab_key_local_unit_group_kv) | 预设库 添加LOCAL_UNIT_GROUP键值对 |
| [set_prefab_key_damage_attack_type_kv](#set_prefab_key_damage_attack_type_kv) | 预设库 添加DAMAGE_ATTACK_TYPE键值对 |
| [set_prefab_key_damage_armor_type_kv](#set_prefab_key_damage_armor_type_kv) | 预设库 添加DAMAGE_ARMOR_TYPE键值对 |
| [set_prefab_key_item_stack_type_kv](#set_prefab_key_item_stack_type_kv) | 预设库 添加ITEM_STACK_TYPE键值对 |
| [set_prefab_key_ability_release_id_kv](#set_prefab_key_ability_release_id_kv) | 预设库 添加ABILITY_RELEASE_ID键值对 |
| [set_prefab_key_slot_type_kv](#set_prefab_key_slot_type_kv) | 预设库 添加SLOT_TYPE键值对 |
| [set_prefab_key_ui_point_kv](#set_prefab_key_ui_point_kv) | 预设库 添加UI_POINT键值对 |
| [set_prefab_key_attach_model_entity_kv](#set_prefab_key_attach_model_entity_kv) | 预设库 添加ATTACH_MODEL_ENTITY键值对 |
| [set_prefab_key_live2d_kv](#set_prefab_key_live2d_kv) | 预设库 添加LIVE2D键值对 |
| [set_prefab_key_spine_kv](#set_prefab_key_spine_kv) | 预设库 添加SPINE键值对 |
| [set_prefab_key_force_entity_kv](#set_prefab_key_force_entity_kv) | 预设库 添加FORCE_ENTITY键值对 |
| [set_prefab_key_goods_key_kv](#set_prefab_key_goods_key_kv) | 预设库 添加GOODS_KEY键值对 |
| [set_prefab_key_mouse_key_without_middle_kv](#set_prefab_key_mouse_key_without_middle_kv) | 预设库 添加MOUSE_KEY_WITHOUT_MIDDLE键值对 |
| [set_prefab_key_map_kv](#set_prefab_key_map_kv) | 预设库 添加MAP键值对 |
| [set_prefab_key_unit_group_command_type_kv](#set_prefab_key_unit_group_command_type_kv) | 预设库 添加UNIT_GROUP_COMMAND_TYPE键值对 |
| [set_prefab_key_rescue_seeker_type_kv](#set_prefab_key_rescue_seeker_type_kv) | 预设库 添加RESCUE_SEEKER_TYPE键值对 |
| [set_prefab_key_rescuer_type_kv](#set_prefab_key_rescuer_type_kv) | 预设库 添加RESCUER_TYPE键值对 |
| [set_prefab_key_store_item_type_kv](#set_prefab_key_store_item_type_kv) | 预设库 添加STORE_ITEM_TYPE键值对 |
| [set_prefab_key_site_state_kv](#set_prefab_key_site_state_kv) | 预设库 添加SITE_STATE键值对 |
| [set_prefab_key_coin_currency_kv](#set_prefab_key_coin_currency_kv) | 预设库 添加COIN_CURRENCY键值对 |
| [add_ui_gridview_type_kv](#add_ui_gridview_type_kv) | 添加UI_GRIDVIEW_TYPE键值对 |
| [add_ui_gridview_bar_type_kv](#add_ui_gridview_bar_type_kv) | 添加UI_GRIDVIEW_BAR_TYPE键值对 |
| [add_ui_effect_camera_mode_kv](#add_ui_effect_camera_mode_kv) | 添加UI_EFFECT_CAMERA_MODE键值对 |
| [add_ui_equip_slot_use_type_kv](#add_ui_equip_slot_use_type_kv) | 添加UI_EQUIP_SLOT_USE_TYPE键值对 |
| [add_ui_equip_slot_drag_type_kv](#add_ui_equip_slot_drag_type_kv) | 添加UI_EQUIP_SLOT_DRAG_TYPE键值对 |
| [add_ui_layout_clipping_type_kv](#add_ui_layout_clipping_type_kv) | 添加UI_LAYOUT_CLIPPING_TYPE键值对 |
| [add_ui_text_over_length_handling_type_kv](#add_ui_text_over_length_handling_type_kv) | 添加UI_TEXT_OVER_LENGTH_HANDLING_TYPE键值对 |
| [add_ui_pos_adapt_mode_kv](#add_ui_pos_adapt_mode_kv) | 添加UI_POS_ADAPT_MODE键值对 |
| [add_ui_chat_send_channel_kv](#add_ui_chat_send_channel_kv) | 添加UI_CHAT_SEND_CHANNEL键值对 |
| [add_ui_chat_recv_channel_kv](#add_ui_chat_recv_channel_kv) | 添加UI_CHAT_RECV_CHANNEL键值对 |
| [add_ui_anim_play_mode_kv](#add_ui_anim_play_mode_kv) | 添加UI_ANIM_PLAY_MODE键值对 |
| [add_ui_text_font_name_kv](#add_ui_text_font_name_kv) | 添加UI_TEXT_FONT_NAME键值对 |
| [add_ui_eca_anim_type_kv](#add_ui_eca_anim_type_kv) | 添加UI_ECA_ANIM_TYPE键值对 |
| [add_local_unit_group_kv](#add_local_unit_group_kv) | 添加LOCAL_UNIT_GROUP键值对 |
| [add_damage_attack_type_kv](#add_damage_attack_type_kv) | 添加DAMAGE_ATTACK_TYPE键值对 |
| [add_damage_armor_type_kv](#add_damage_armor_type_kv) | 添加DAMAGE_ARMOR_TYPE键值对 |
| [add_item_stack_type_kv](#add_item_stack_type_kv) | 添加ITEM_STACK_TYPE键值对 |
| [add_ability_release_id_kv](#add_ability_release_id_kv) | 添加ABILITY_RELEASE_ID键值对 |
| [add_slot_type_kv](#add_slot_type_kv) | 添加SLOT_TYPE键值对 |
| [add_ui_point_kv](#add_ui_point_kv) | 添加UI_POINT键值对 |
| [add_attach_model_entity_kv](#add_attach_model_entity_kv) | 添加ATTACH_MODEL_ENTITY键值对 |
| [add_live2d_kv](#add_live2d_kv) | 添加LIVE2D键值对 |
| [add_spine_kv](#add_spine_kv) | 添加SPINE键值对 |
| [add_force_entity_kv](#add_force_entity_kv) | 添加FORCE_ENTITY键值对 |
| [add_goods_key_kv](#add_goods_key_kv) | 添加GOODS_KEY键值对 |
| [add_mouse_key_without_middle_kv](#add_mouse_key_without_middle_kv) | 添加MOUSE_KEY_WITHOUT_MIDDLE键值对 |
| [add_map_kv](#add_map_kv) | 添加MAP键值对 |
| [add_unit_group_command_type_kv](#add_unit_group_command_type_kv) | 添加UNIT_GROUP_COMMAND_TYPE键值对 |
| [add_rescue_seeker_type_kv](#add_rescue_seeker_type_kv) | 添加RESCUE_SEEKER_TYPE键值对 |
| [add_rescuer_type_kv](#add_rescuer_type_kv) | 添加RESCUER_TYPE键值对 |
| [add_store_item_type_kv](#add_store_item_type_kv) | 添加STORE_ITEM_TYPE键值对 |
| [add_site_state_kv](#add_site_state_kv) | 添加SITE_STATE键值对 |
| [add_coin_currency_kv](#add_coin_currency_kv) | 添加COIN_CURRENCY键值对 |
| [has_prefab_xxx_kv](#has_prefab_xxx_kv) | 判断预设是否存在%s键值对 |
| [has_entity_ckv_pair_value_xxx](#has_entity_ckv_pair_value_xxx) | 获取值对 |
| [has_ability_ckv_pair_value_xxx](#has_ability_ckv_pair_value_xxx) | 获取值对 |
| [has_modifier_ckv_pair_value_xxx](#has_modifier_ckv_pair_value_xxx) | 获取值对 |
| [has_kv_pair_ui_gridview_type](#has_kv_pair_ui_gridview_type) | 判断是否存在UI_GRIDVIEW_TYPE键值对 |
| [has_prefab_ui_gridview_type_kv](#has_prefab_ui_gridview_type_kv) | 判断预设是否存在UI_GRIDVIEW_TYPE键值对 |
| [has_unit_key_ui_gridview_type_kv](#has_unit_key_ui_gridview_type_kv) | 判断单位编号是否存在UI_GRIDVIEW_TYPE键值对 |
| [has_item_key_ui_gridview_type_kv](#has_item_key_ui_gridview_type_kv) | 判断物品编号是否存在UI_GRIDVIEW_TYPE键值对 |
| [has_ability_key_ui_gridview_type_kv](#has_ability_key_ui_gridview_type_kv) | 判断技能编号是否存在UI_GRIDVIEW_TYPE键值对 |
| [has_kv_pair_ui_gridview_bar_type](#has_kv_pair_ui_gridview_bar_type) | 判断是否存在UI_GRIDVIEW_BAR_TYPE键值对 |
| [has_prefab_ui_gridview_bar_type_kv](#has_prefab_ui_gridview_bar_type_kv) | 判断预设是否存在UI_GRIDVIEW_BAR_TYPE键值对 |
| [has_unit_key_ui_gridview_bar_type_kv](#has_unit_key_ui_gridview_bar_type_kv) | 判断单位编号是否存在UI_GRIDVIEW_BAR_TYPE键值对 |
| [has_item_key_ui_gridview_bar_type_kv](#has_item_key_ui_gridview_bar_type_kv) | 判断物品编号是否存在UI_GRIDVIEW_BAR_TYPE键值对 |
| [has_ability_key_ui_gridview_bar_type_kv](#has_ability_key_ui_gridview_bar_type_kv) | 判断技能编号是否存在UI_GRIDVIEW_BAR_TYPE键值对 |
| [has_kv_pair_ui_effect_camera_mode](#has_kv_pair_ui_effect_camera_mode) | 判断是否存在UI_EFFECT_CAMERA_MODE键值对 |
| [has_prefab_ui_effect_camera_mode_kv](#has_prefab_ui_effect_camera_mode_kv) | 判断预设是否存在UI_EFFECT_CAMERA_MODE键值对 |
| [has_unit_key_ui_effect_camera_mode_kv](#has_unit_key_ui_effect_camera_mode_kv) | 判断单位编号是否存在UI_EFFECT_CAMERA_MODE键值对 |
| [has_item_key_ui_effect_camera_mode_kv](#has_item_key_ui_effect_camera_mode_kv) | 判断物品编号是否存在UI_EFFECT_CAMERA_MODE键值对 |
| [has_ability_key_ui_effect_camera_mode_kv](#has_ability_key_ui_effect_camera_mode_kv) | 判断技能编号是否存在UI_EFFECT_CAMERA_MODE键值对 |
| [has_kv_pair_ui_equip_slot_use_type](#has_kv_pair_ui_equip_slot_use_type) | 判断是否存在UI_EQUIP_SLOT_USE_TYPE键值对 |
| [has_prefab_ui_equip_slot_use_type_kv](#has_prefab_ui_equip_slot_use_type_kv) | 判断预设是否存在UI_EQUIP_SLOT_USE_TYPE键值对 |
| [has_unit_key_ui_equip_slot_use_type_kv](#has_unit_key_ui_equip_slot_use_type_kv) | 判断单位编号是否存在UI_EQUIP_SLOT_USE_TYPE键值对 |
| [has_item_key_ui_equip_slot_use_type_kv](#has_item_key_ui_equip_slot_use_type_kv) | 判断物品编号是否存在UI_EQUIP_SLOT_USE_TYPE键值对 |
| [has_ability_key_ui_equip_slot_use_type_kv](#has_ability_key_ui_equip_slot_use_type_kv) | 判断技能编号是否存在UI_EQUIP_SLOT_USE_TYPE键值对 |
| [has_kv_pair_ui_equip_slot_drag_type](#has_kv_pair_ui_equip_slot_drag_type) | 判断是否存在UI_EQUIP_SLOT_DRAG_TYPE键值对 |
| [has_prefab_ui_equip_slot_drag_type_kv](#has_prefab_ui_equip_slot_drag_type_kv) | 判断预设是否存在UI_EQUIP_SLOT_DRAG_TYPE键值对 |
| [has_unit_key_ui_equip_slot_drag_type_kv](#has_unit_key_ui_equip_slot_drag_type_kv) | 判断单位编号是否存在UI_EQUIP_SLOT_DRAG_TYPE键值对 |
| [has_item_key_ui_equip_slot_drag_type_kv](#has_item_key_ui_equip_slot_drag_type_kv) | 判断物品编号是否存在UI_EQUIP_SLOT_DRAG_TYPE键值对 |
| [has_ability_key_ui_equip_slot_drag_type_kv](#has_ability_key_ui_equip_slot_drag_type_kv) | 判断技能编号是否存在UI_EQUIP_SLOT_DRAG_TYPE键值对 |
| [has_kv_pair_ui_layout_clipping_type](#has_kv_pair_ui_layout_clipping_type) | 判断是否存在UI_LAYOUT_CLIPPING_TYPE键值对 |
| [has_prefab_ui_layout_clipping_type_kv](#has_prefab_ui_layout_clipping_type_kv) | 判断预设是否存在UI_LAYOUT_CLIPPING_TYPE键值对 |
| [has_unit_key_ui_layout_clipping_type_kv](#has_unit_key_ui_layout_clipping_type_kv) | 判断单位编号是否存在UI_LAYOUT_CLIPPING_TYPE键值对 |
| [has_item_key_ui_layout_clipping_type_kv](#has_item_key_ui_layout_clipping_type_kv) | 判断物品编号是否存在UI_LAYOUT_CLIPPING_TYPE键值对 |
| [has_ability_key_ui_layout_clipping_type_kv](#has_ability_key_ui_layout_clipping_type_kv) | 判断技能编号是否存在UI_LAYOUT_CLIPPING_TYPE键值对 |
| [has_kv_pair_ui_text_over_length_handling_type](#has_kv_pair_ui_text_over_length_handling_type) | 判断是否存在UI_TEXT_OVER_LENGTH_HANDLING_TYPE键值对 |
| [has_prefab_ui_text_over_length_handling_type_kv](#has_prefab_ui_text_over_length_handling_type_kv) | 判断预设是否存在UI_TEXT_OVER_LENGTH_HANDLING_TYPE键值对 |
| [has_unit_key_ui_text_over_length_handling_type_kv](#has_unit_key_ui_text_over_length_handling_type_kv) | 判断单位编号是否存在UI_TEXT_OVER_LENGTH_HANDLING_TYPE键值对 |
| [has_item_key_ui_text_over_length_handling_type_kv](#has_item_key_ui_text_over_length_handling_type_kv) | 判断物品编号是否存在UI_TEXT_OVER_LENGTH_HANDLING_TYPE键值对 |
| [has_ability_key_ui_text_over_length_handling_type_kv](#has_ability_key_ui_text_over_length_handling_type_kv) | 判断技能编号是否存在UI_TEXT_OVER_LENGTH_HANDLING_TYPE键值对 |
| [has_kv_pair_ui_pos_adapt_mode](#has_kv_pair_ui_pos_adapt_mode) | 判断是否存在UI_POS_ADAPT_MODE键值对 |
| [has_prefab_ui_pos_adapt_mode_kv](#has_prefab_ui_pos_adapt_mode_kv) | 判断预设是否存在UI_POS_ADAPT_MODE键值对 |
| [has_unit_key_ui_pos_adapt_mode_kv](#has_unit_key_ui_pos_adapt_mode_kv) | 判断单位编号是否存在UI_POS_ADAPT_MODE键值对 |
| [has_item_key_ui_pos_adapt_mode_kv](#has_item_key_ui_pos_adapt_mode_kv) | 判断物品编号是否存在UI_POS_ADAPT_MODE键值对 |
| [has_ability_key_ui_pos_adapt_mode_kv](#has_ability_key_ui_pos_adapt_mode_kv) | 判断技能编号是否存在UI_POS_ADAPT_MODE键值对 |
| [has_kv_pair_ui_chat_send_channel](#has_kv_pair_ui_chat_send_channel) | 判断是否存在UI_CHAT_SEND_CHANNEL键值对 |
| [has_prefab_ui_chat_send_channel_kv](#has_prefab_ui_chat_send_channel_kv) | 判断预设是否存在UI_CHAT_SEND_CHANNEL键值对 |
| [has_unit_key_ui_chat_send_channel_kv](#has_unit_key_ui_chat_send_channel_kv) | 判断单位编号是否存在UI_CHAT_SEND_CHANNEL键值对 |
| [has_item_key_ui_chat_send_channel_kv](#has_item_key_ui_chat_send_channel_kv) | 判断物品编号是否存在UI_CHAT_SEND_CHANNEL键值对 |
| [has_ability_key_ui_chat_send_channel_kv](#has_ability_key_ui_chat_send_channel_kv) | 判断技能编号是否存在UI_CHAT_SEND_CHANNEL键值对 |
| [has_kv_pair_ui_chat_recv_channel](#has_kv_pair_ui_chat_recv_channel) | 判断是否存在UI_CHAT_RECV_CHANNEL键值对 |
| [has_prefab_ui_chat_recv_channel_kv](#has_prefab_ui_chat_recv_channel_kv) | 判断预设是否存在UI_CHAT_RECV_CHANNEL键值对 |
| [has_unit_key_ui_chat_recv_channel_kv](#has_unit_key_ui_chat_recv_channel_kv) | 判断单位编号是否存在UI_CHAT_RECV_CHANNEL键值对 |
| [has_item_key_ui_chat_recv_channel_kv](#has_item_key_ui_chat_recv_channel_kv) | 判断物品编号是否存在UI_CHAT_RECV_CHANNEL键值对 |
| [has_ability_key_ui_chat_recv_channel_kv](#has_ability_key_ui_chat_recv_channel_kv) | 判断技能编号是否存在UI_CHAT_RECV_CHANNEL键值对 |
| [has_kv_pair_ui_anim_play_mode](#has_kv_pair_ui_anim_play_mode) | 判断是否存在UI_ANIM_PLAY_MODE键值对 |
| [has_prefab_ui_anim_play_mode_kv](#has_prefab_ui_anim_play_mode_kv) | 判断预设是否存在UI_ANIM_PLAY_MODE键值对 |
| [has_unit_key_ui_anim_play_mode_kv](#has_unit_key_ui_anim_play_mode_kv) | 判断单位编号是否存在UI_ANIM_PLAY_MODE键值对 |
| [has_item_key_ui_anim_play_mode_kv](#has_item_key_ui_anim_play_mode_kv) | 判断物品编号是否存在UI_ANIM_PLAY_MODE键值对 |
| [has_ability_key_ui_anim_play_mode_kv](#has_ability_key_ui_anim_play_mode_kv) | 判断技能编号是否存在UI_ANIM_PLAY_MODE键值对 |
| [has_kv_pair_ui_text_font_name](#has_kv_pair_ui_text_font_name) | 判断是否存在UI_TEXT_FONT_NAME键值对 |
| [has_prefab_ui_text_font_name_kv](#has_prefab_ui_text_font_name_kv) | 判断预设是否存在UI_TEXT_FONT_NAME键值对 |
| [has_unit_key_ui_text_font_name_kv](#has_unit_key_ui_text_font_name_kv) | 判断单位编号是否存在UI_TEXT_FONT_NAME键值对 |
| [has_item_key_ui_text_font_name_kv](#has_item_key_ui_text_font_name_kv) | 判断物品编号是否存在UI_TEXT_FONT_NAME键值对 |
| [has_ability_key_ui_text_font_name_kv](#has_ability_key_ui_text_font_name_kv) | 判断技能编号是否存在UI_TEXT_FONT_NAME键值对 |
| [has_kv_pair_ui_eca_anim_type](#has_kv_pair_ui_eca_anim_type) | 判断是否存在UI_ECA_ANIM_TYPE键值对 |
| [has_prefab_ui_eca_anim_type_kv](#has_prefab_ui_eca_anim_type_kv) | 判断预设是否存在UI_ECA_ANIM_TYPE键值对 |
| [has_unit_key_ui_eca_anim_type_kv](#has_unit_key_ui_eca_anim_type_kv) | 判断单位编号是否存在UI_ECA_ANIM_TYPE键值对 |
| [has_item_key_ui_eca_anim_type_kv](#has_item_key_ui_eca_anim_type_kv) | 判断物品编号是否存在UI_ECA_ANIM_TYPE键值对 |
| [has_ability_key_ui_eca_anim_type_kv](#has_ability_key_ui_eca_anim_type_kv) | 判断技能编号是否存在UI_ECA_ANIM_TYPE键值对 |
| [has_kv_pair_local_unit_group](#has_kv_pair_local_unit_group) | 判断是否存在LOCAL_UNIT_GROUP键值对 |
| [has_prefab_local_unit_group_kv](#has_prefab_local_unit_group_kv) | 判断预设是否存在LOCAL_UNIT_GROUP键值对 |
| [has_unit_key_local_unit_group_kv](#has_unit_key_local_unit_group_kv) | 判断单位编号是否存在LOCAL_UNIT_GROUP键值对 |
| [has_item_key_local_unit_group_kv](#has_item_key_local_unit_group_kv) | 判断物品编号是否存在LOCAL_UNIT_GROUP键值对 |
| [has_ability_key_local_unit_group_kv](#has_ability_key_local_unit_group_kv) | 判断技能编号是否存在LOCAL_UNIT_GROUP键值对 |
| [has_kv_pair_damage_attack_type](#has_kv_pair_damage_attack_type) | 判断是否存在DAMAGE_ATTACK_TYPE键值对 |
| [has_prefab_damage_attack_type_kv](#has_prefab_damage_attack_type_kv) | 判断预设是否存在DAMAGE_ATTACK_TYPE键值对 |
| [has_unit_key_damage_attack_type_kv](#has_unit_key_damage_attack_type_kv) | 判断单位编号是否存在DAMAGE_ATTACK_TYPE键值对 |
| [has_item_key_damage_attack_type_kv](#has_item_key_damage_attack_type_kv) | 判断物品编号是否存在DAMAGE_ATTACK_TYPE键值对 |
| [has_ability_key_damage_attack_type_kv](#has_ability_key_damage_attack_type_kv) | 判断技能编号是否存在DAMAGE_ATTACK_TYPE键值对 |
| [has_kv_pair_damage_armor_type](#has_kv_pair_damage_armor_type) | 判断是否存在DAMAGE_ARMOR_TYPE键值对 |
| [has_prefab_damage_armor_type_kv](#has_prefab_damage_armor_type_kv) | 判断预设是否存在DAMAGE_ARMOR_TYPE键值对 |
| [has_unit_key_damage_armor_type_kv](#has_unit_key_damage_armor_type_kv) | 判断单位编号是否存在DAMAGE_ARMOR_TYPE键值对 |
| [has_item_key_damage_armor_type_kv](#has_item_key_damage_armor_type_kv) | 判断物品编号是否存在DAMAGE_ARMOR_TYPE键值对 |
| [has_ability_key_damage_armor_type_kv](#has_ability_key_damage_armor_type_kv) | 判断技能编号是否存在DAMAGE_ARMOR_TYPE键值对 |
| [has_kv_pair_item_stack_type](#has_kv_pair_item_stack_type) | 判断是否存在ITEM_STACK_TYPE键值对 |
| [has_prefab_item_stack_type_kv](#has_prefab_item_stack_type_kv) | 判断预设是否存在ITEM_STACK_TYPE键值对 |
| [has_unit_key_item_stack_type_kv](#has_unit_key_item_stack_type_kv) | 判断单位编号是否存在ITEM_STACK_TYPE键值对 |
| [has_item_key_item_stack_type_kv](#has_item_key_item_stack_type_kv) | 判断物品编号是否存在ITEM_STACK_TYPE键值对 |
| [has_ability_key_item_stack_type_kv](#has_ability_key_item_stack_type_kv) | 判断技能编号是否存在ITEM_STACK_TYPE键值对 |
| [has_kv_pair_ability_release_id](#has_kv_pair_ability_release_id) | 判断是否存在ABILITY_RELEASE_ID键值对 |
| [has_prefab_ability_release_id_kv](#has_prefab_ability_release_id_kv) | 判断预设是否存在ABILITY_RELEASE_ID键值对 |
| [has_unit_key_ability_release_id_kv](#has_unit_key_ability_release_id_kv) | 判断单位编号是否存在ABILITY_RELEASE_ID键值对 |
| [has_item_key_ability_release_id_kv](#has_item_key_ability_release_id_kv) | 判断物品编号是否存在ABILITY_RELEASE_ID键值对 |
| [has_ability_key_ability_release_id_kv](#has_ability_key_ability_release_id_kv) | 判断技能编号是否存在ABILITY_RELEASE_ID键值对 |
| [has_kv_pair_slot_type](#has_kv_pair_slot_type) | 判断是否存在SLOT_TYPE键值对 |
| [has_prefab_slot_type_kv](#has_prefab_slot_type_kv) | 判断预设是否存在SLOT_TYPE键值对 |
| [has_unit_key_slot_type_kv](#has_unit_key_slot_type_kv) | 判断单位编号是否存在SLOT_TYPE键值对 |
| [has_item_key_slot_type_kv](#has_item_key_slot_type_kv) | 判断物品编号是否存在SLOT_TYPE键值对 |
| [has_ability_key_slot_type_kv](#has_ability_key_slot_type_kv) | 判断技能编号是否存在SLOT_TYPE键值对 |
| [has_kv_pair_ui_point](#has_kv_pair_ui_point) | 判断是否存在UI_POINT键值对 |
| [has_prefab_ui_point_kv](#has_prefab_ui_point_kv) | 判断预设是否存在UI_POINT键值对 |
| [has_unit_key_ui_point_kv](#has_unit_key_ui_point_kv) | 判断单位编号是否存在UI_POINT键值对 |
| [has_item_key_ui_point_kv](#has_item_key_ui_point_kv) | 判断物品编号是否存在UI_POINT键值对 |
| [has_ability_key_ui_point_kv](#has_ability_key_ui_point_kv) | 判断技能编号是否存在UI_POINT键值对 |
| [has_kv_pair_attach_model_entity](#has_kv_pair_attach_model_entity) | 判断是否存在ATTACH_MODEL_ENTITY键值对 |
| [has_prefab_attach_model_entity_kv](#has_prefab_attach_model_entity_kv) | 判断预设是否存在ATTACH_MODEL_ENTITY键值对 |
| [has_unit_key_attach_model_entity_kv](#has_unit_key_attach_model_entity_kv) | 判断单位编号是否存在ATTACH_MODEL_ENTITY键值对 |
| [has_item_key_attach_model_entity_kv](#has_item_key_attach_model_entity_kv) | 判断物品编号是否存在ATTACH_MODEL_ENTITY键值对 |
| [has_ability_key_attach_model_entity_kv](#has_ability_key_attach_model_entity_kv) | 判断技能编号是否存在ATTACH_MODEL_ENTITY键值对 |
| [has_kv_pair_live2d](#has_kv_pair_live2d) | 判断是否存在LIVE2D键值对 |
| [has_prefab_live2d_kv](#has_prefab_live2d_kv) | 判断预设是否存在LIVE2D键值对 |
| [has_unit_key_live2d_kv](#has_unit_key_live2d_kv) | 判断单位编号是否存在LIVE2D键值对 |
| [has_item_key_live2d_kv](#has_item_key_live2d_kv) | 判断物品编号是否存在LIVE2D键值对 |
| [has_ability_key_live2d_kv](#has_ability_key_live2d_kv) | 判断技能编号是否存在LIVE2D键值对 |
| [has_kv_pair_spine](#has_kv_pair_spine) | 判断是否存在SPINE键值对 |
| [has_prefab_spine_kv](#has_prefab_spine_kv) | 判断预设是否存在SPINE键值对 |
| [has_unit_key_spine_kv](#has_unit_key_spine_kv) | 判断单位编号是否存在SPINE键值对 |
| [has_item_key_spine_kv](#has_item_key_spine_kv) | 判断物品编号是否存在SPINE键值对 |
| [has_ability_key_spine_kv](#has_ability_key_spine_kv) | 判断技能编号是否存在SPINE键值对 |
| [has_kv_pair_force_entity](#has_kv_pair_force_entity) | 判断是否存在FORCE_ENTITY键值对 |
| [has_prefab_force_entity_kv](#has_prefab_force_entity_kv) | 判断预设是否存在FORCE_ENTITY键值对 |
| [has_unit_key_force_entity_kv](#has_unit_key_force_entity_kv) | 判断单位编号是否存在FORCE_ENTITY键值对 |
| [has_item_key_force_entity_kv](#has_item_key_force_entity_kv) | 判断物品编号是否存在FORCE_ENTITY键值对 |
| [has_ability_key_force_entity_kv](#has_ability_key_force_entity_kv) | 判断技能编号是否存在FORCE_ENTITY键值对 |
| [has_kv_pair_goods_key](#has_kv_pair_goods_key) | 判断是否存在GOODS_KEY键值对 |
| [has_prefab_goods_key_kv](#has_prefab_goods_key_kv) | 判断预设是否存在GOODS_KEY键值对 |
| [has_unit_key_goods_key_kv](#has_unit_key_goods_key_kv) | 判断单位编号是否存在GOODS_KEY键值对 |
| [has_item_key_goods_key_kv](#has_item_key_goods_key_kv) | 判断物品编号是否存在GOODS_KEY键值对 |
| [has_ability_key_goods_key_kv](#has_ability_key_goods_key_kv) | 判断技能编号是否存在GOODS_KEY键值对 |
| [has_kv_pair_mouse_key_without_middle](#has_kv_pair_mouse_key_without_middle) | 判断是否存在MOUSE_KEY_WITHOUT_MIDDLE键值对 |
| [has_prefab_mouse_key_without_middle_kv](#has_prefab_mouse_key_without_middle_kv) | 判断预设是否存在MOUSE_KEY_WITHOUT_MIDDLE键值对 |
| [has_unit_key_mouse_key_without_middle_kv](#has_unit_key_mouse_key_without_middle_kv) | 判断单位编号是否存在MOUSE_KEY_WITHOUT_MIDDLE键值对 |
| [has_item_key_mouse_key_without_middle_kv](#has_item_key_mouse_key_without_middle_kv) | 判断物品编号是否存在MOUSE_KEY_WITHOUT_MIDDLE键值对 |
| [has_ability_key_mouse_key_without_middle_kv](#has_ability_key_mouse_key_without_middle_kv) | 判断技能编号是否存在MOUSE_KEY_WITHOUT_MIDDLE键值对 |
| [has_kv_pair_map](#has_kv_pair_map) | 判断是否存在MAP键值对 |
| [has_prefab_map_kv](#has_prefab_map_kv) | 判断预设是否存在MAP键值对 |
| [has_unit_key_map_kv](#has_unit_key_map_kv) | 判断单位编号是否存在MAP键值对 |
| [has_item_key_map_kv](#has_item_key_map_kv) | 判断物品编号是否存在MAP键值对 |
| [has_ability_key_map_kv](#has_ability_key_map_kv) | 判断技能编号是否存在MAP键值对 |
| [has_kv_pair_unit_group_command_type](#has_kv_pair_unit_group_command_type) | 判断是否存在UNIT_GROUP_COMMAND_TYPE键值对 |
| [has_prefab_unit_group_command_type_kv](#has_prefab_unit_group_command_type_kv) | 判断预设是否存在UNIT_GROUP_COMMAND_TYPE键值对 |
| [has_unit_key_unit_group_command_type_kv](#has_unit_key_unit_group_command_type_kv) | 判断单位编号是否存在UNIT_GROUP_COMMAND_TYPE键值对 |
| [has_item_key_unit_group_command_type_kv](#has_item_key_unit_group_command_type_kv) | 判断物品编号是否存在UNIT_GROUP_COMMAND_TYPE键值对 |
| [has_ability_key_unit_group_command_type_kv](#has_ability_key_unit_group_command_type_kv) | 判断技能编号是否存在UNIT_GROUP_COMMAND_TYPE键值对 |
| [has_kv_pair_rescue_seeker_type](#has_kv_pair_rescue_seeker_type) | 判断是否存在RESCUE_SEEKER_TYPE键值对 |
| [has_prefab_rescue_seeker_type_kv](#has_prefab_rescue_seeker_type_kv) | 判断预设是否存在RESCUE_SEEKER_TYPE键值对 |
| [has_unit_key_rescue_seeker_type_kv](#has_unit_key_rescue_seeker_type_kv) | 判断单位编号是否存在RESCUE_SEEKER_TYPE键值对 |
| [has_item_key_rescue_seeker_type_kv](#has_item_key_rescue_seeker_type_kv) | 判断物品编号是否存在RESCUE_SEEKER_TYPE键值对 |

---

## del_unit_key_kv

method in GameAPI

- 描述

    预设库单位删除键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键值名称 |

- 返回值

    无

- 示例

```lua
local unit_key = 134274569

GameAPI.del_unit_key_kv(unit_key, "key")
```

---

## del_ability_key_kv

method in GameAPI

- 描述

    预设库技能删除键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键值名称 |

- 返回值

    无

- 示例

```lua
local ability_key = 134274569

GameAPI.del_ability_key_kv(ability_key, "key")
```

---

## del_item_key_kv

method in GameAPI

- 描述

    预设库物品删除键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键值名称 |

- 返回值

    无

- 示例

```lua
local item_key = 134274569

GameAPI.del_item_key_kv(item_key, "key")
```

---

## del_prefab_key_kv

method in GameAPI

- 描述

    预设库物品删除键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | 物品编号 |
    | key | string | 键值名称 |
    | prefab_conf_key | integer | prefab库ID |

- 返回值

    无

- 示例

```lua
GameAPI.del_prefab_key_kv(1, "key", 1)
```

---

## add_boolean_kv

method in GameAPI

- 描述

    添加BOOLEAN键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | boolean | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_boolean_kv(kvbase, "key", true)
```

---

## add_integer_kv

method in GameAPI

- 描述

    添加INTEGER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | integer | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_integer_kv(kvbase, "key", 1)
```

---

## add_float_kv

method in GameAPI

- 描述

    添加FLOAT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.Fixed | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_float_kv(kvbase, "key", Fix32(1))
```

---

## add_string_kv

method in GameAPI

- 描述

    添加STRING键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | string | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_string_kv(kvbase, "key", "item")
```

---

## add_ui_comp_kv

method in GameAPI

- 描述

    添加UI_COMP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | string | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_ui_comp_kv(kvbase, "key", "item")
```

---

## add_ui_comp_type_kv

method in GameAPI

- 描述

    添加UI_COMP_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | integer | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_ui_comp_type_kv(kvbase, "key", 1)
```

---

## add_ui_comp_event_type_kv

method in GameAPI

- 描述

    添加UI_COMP_EVENT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | integer | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_ui_comp_event_type_kv(kvbase, "key", 1)
```

---

## add_ui_comp_attr_kv

method in GameAPI

- 描述

    添加UI_COMP_ATTR键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | string | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_ui_comp_attr_kv(kvbase, "key", "item")
```

---

## add_ui_comp_align_type_kv

method in GameAPI

- 描述

    添加UI_COMP_ALIGN_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | integer | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_ui_comp_align_type_kv(kvbase, "key", 1)
```

---

## add_ui_prefab_kv

method in GameAPI

- 描述

    添加UI_PREFAB键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | string | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_ui_prefab_kv(kvbase, "key", "item")
```

---

## add_ui_prefab_instance_kv

method in GameAPI

- 描述

    添加UI_PREFAB_INSTANCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.UIPrefabIns | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local player = y3.player.get_by_id(1)
local ui_prefab_ins = GameAPI.get_ui_prefab_ins(player.handle, "prefab_uid")

GameAPI.add_ui_prefab_instance_kv(kvbase, "key")
```

---

## add_ui_prefab_ins_uid_kv

method in GameAPI

- 描述

    添加UI_PREFAB_INS_UID键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | string | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_ui_prefab_ins_uid_kv(kvbase, "key", "item")
```

---

## add_ui_direction_kv

method in GameAPI

- 描述

    添加UI_DIRECTION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | integer | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_ui_direction_kv(kvbase, "key", 1)
```

---

## add_ui_model_camera_mod_kv

method in GameAPI

- 描述

    添加UI_MODEL_CAMERA_MOD键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | integer | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_ui_model_camera_mod_kv(kvbase, "key", 1)
```

---

## add_ui_btn_status_kv

method in GameAPI

- 描述

    添加UI_BTN_STATUS键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | integer | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_ui_btn_status_kv(kvbase, "key", 1)
```

---

## add_ui_scrollview_type_kv

method in GameAPI

- 描述

    添加UI_SCROLLVIEW_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | integer | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_ui_scrollview_type_kv(kvbase, "key", 1)
```

---

## add_ui_anim_kv

method in GameAPI

- 描述

    添加UI_ANIM键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.UIAnimKey | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local ui_anim_key = GameAPI.get_unit_key_ui_anim_kv(1, "key")

GameAPI.add_ui_anim_kv(kvbase, "key")
```

---

## add_ui_anim_curve_kv

method in GameAPI

- 描述

    添加UI_ANIM_CURVE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | integer | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_ui_anim_curve_kv(kvbase, "key", 1)
```

---

## add_audio_channel_kv

method in GameAPI

- 描述

    添加AUDIO_CHANNEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | integer | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_audio_channel_kv(kvbase, "key", 1)
```

---

## add_unit_entity_kv

method in GameAPI

- 描述

    添加UNIT_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.Unit | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_unit_entity_kv(kvbase, "key")
```

---

## add_unit_group_kv

method in GameAPI

- 描述

    添加UNIT_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.UnitGroup | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local unit_group = y3.unit_group.create()

GameAPI.add_unit_group_kv(kvbase, "key")
```

---

## add_unit_name_kv

method in GameAPI

- 描述

    添加UNIT_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.UnitKey | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local unit_key = 134274569

GameAPI.add_unit_name_kv(kvbase, "key")
```

---

## add_unit_name_pool_kv

method in GameAPI

- 描述

    添加UNIT_NAME_POOL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.UnitKeyPool | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local unit_key_pool = GlobalAPI.get_empty_unit_key_pool()

GameAPI.add_unit_name_pool_kv(kvbase, "key")
```

---

## add_unit_write_attribute_kv

method in GameAPI

- 描述

    添加UNIT_WRITE_ATTRIBUTE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | string | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_unit_write_attribute_kv(kvbase, "key", "item")
```

---

## add_attr_element_kv

method in GameAPI

- 描述

    添加ATTR_ELEMENT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | string | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_attr_element_kv(kvbase, "key", "item")
```

---

## add_attr_element_read_kv

method in GameAPI

- 描述

    添加ATTR_ELEMENT_READ键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | string | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_attr_element_read_kv(kvbase, "key", "item")
```

---

## add_mover_entity_kv

method in GameAPI

- 描述

    添加MOVER_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.Mover | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })
local mover = GameAPI.get_projectile_mover(projectile.handle)

GameAPI.add_mover_entity_kv(kvbase, "key")
```

---

## add_image_quality_kv

method in GameAPI

- 描述

    添加IMAGE_QUALITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | string | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_image_quality_kv(kvbase, "key", "item")
```

---

## add_window_type_setting_kv

method in GameAPI

- 描述

    添加WINDOW_TYPE_SETTING键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | string | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_window_type_setting_kv(kvbase, "key", "item")
```

---

## add_item_entity_kv

method in GameAPI

- 描述

    添加ITEM_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.Item | value |

- 返回值

    无

- 示例

```lua
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_item_entity_kv(kvbase, "key")
```

---

## add_item_group_kv

method in GameAPI

- 描述

    添加ITEM_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.ItemGroup | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local item_group = y3.item_group.create()

GameAPI.add_item_group_kv(kvbase, "key")
```

---

## add_item_name_kv

method in GameAPI

- 描述

    添加ITEM_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.ItemKey | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local item_key = 134274569

GameAPI.add_item_name_kv(kvbase, "key")
```

---

## add_ability_kv

method in GameAPI

- 描述

    添加ABILITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.Ability | value |

- 返回值

    无

- 示例

```lua
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_ability_kv(kvbase, "key")
```

---

## add_ability_type_kv

method in GameAPI

- 描述

    添加ABILITY_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | integer | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_ability_type_kv(kvbase, "key", 1)
```

---

## add_ability_cast_type_kv

method in GameAPI

- 描述

    添加ABILITY_CAST_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | integer | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_ability_cast_type_kv(kvbase, "key", 1)
```

---

## add_ability_name_kv

method in GameAPI

- 描述

    添加ABILITY_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.AbilityKey | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local ability_key = 134274569

GameAPI.add_ability_name_kv(kvbase, "key")
```

---

## add_skill_pointer_type_kv

method in GameAPI

- 描述

    添加SKILL_POINTER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | integer | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_skill_pointer_type_kv(kvbase, "key", 1)
```

---

## add_modifier_entity_kv

method in GameAPI

- 描述

    添加MODIFIER_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.ModifierEntity | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)
local kvbase = unit.handle

GameAPI.add_modifier_entity_kv(kvbase, "key")
```

---

## add_modifier_type_kv

method in GameAPI

- 描述

    添加MODIFIER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.ModifierType | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_modifier_type_kv(kvbase, "key", 1)
```

---

## add_modifier_effect_type_kv

method in GameAPI

- 描述

    添加MODIFIER_EFFECT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.ModifierEffectType | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_modifier_effect_type_kv(kvbase, "key", 1)
```

---

## add_modifier_kv

method in GameAPI

- 描述

    添加MODIFIER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.ModifierKey | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local modifier_key = 134274569

GameAPI.add_modifier_kv(kvbase, "key")
```

---

## add_projectile_kv

method in GameAPI

- 描述

    添加PROJECTILE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.ProjectileKey | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local projectile_key = 134274569

GameAPI.add_projectile_kv(kvbase, "key")
```

---

## add_projectile_entity_kv

method in GameAPI

- 描述

    添加PROJECTILE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.ProjectileEntity | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local target_point = unit:get_point()
local projectile = y3.projectile.create({ key = 134274569, target = target_point })

GameAPI.add_projectile_entity_kv(kvbase, "key")
```

---

## add_projectile_group_kv

method in GameAPI

- 描述

    添加PROJECTILE_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.ProjectileGroup | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local projectile_group = y3.projectile_group.create_lua_projectile_group_from_py(GameAPI.create_projectile_group())

GameAPI.add_projectile_group_kv(kvbase, "key")
```

---

## add_destructible_entity_kv

method in GameAPI

- 描述

    添加DESTRUCTIBLE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.Destructible | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local destructible = y3.destructible.get_by_id(1)
if destructible then

GameAPI.add_destructible_entity_kv(kvbase, "key")
end
```

---

## add_destructible_name_kv

method in GameAPI

- 描述

    添加DESTRUCTIBLE_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.DestructibleKey | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local destructible_key = 1

GameAPI.add_destructible_name_kv(kvbase, "key")
```

---

## add_sound_entity_kv

method in GameAPI

- 描述

    添加SOUND_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.SoundEntity | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local player = y3.player.get_by_id(1)
local sound_entity = GameAPI.play_sound_for_player(player.handle, 134274569, false)

GameAPI.add_sound_entity_kv(kvbase, "key")
```

---

## add_audio_key_kv

method in GameAPI

- 描述

    添加AUDIO_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.AudioKey | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local audio_key = 134274569

GameAPI.add_audio_key_kv(kvbase, "key")
```

---

## add_game_mode_kv

method in GameAPI

- 描述

    添加GAME_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.GameMode | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_game_mode_kv(kvbase, "key", 1)
```

---

## add_player_kv

method in GameAPI

- 描述

    添加PLAYER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.Role | value |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_player_kv(kvbase, "key")
```

---

## add_player_group_kv

method in GameAPI

- 描述

    添加PLAYER_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.RoleGroup | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local player_group = y3.player_group.create()

GameAPI.add_player_group_kv(kvbase, "key")
```

---

## add_role_res_key_kv

method in GameAPI

- 描述

    添加ROLE_RES_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.RoleResKey | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local role_res_key = "res_key"

GameAPI.add_role_res_key_kv(kvbase, "key")
```

---

## add_role_status_kv

method in GameAPI

- 描述

    添加ROLE_STATUS键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.RoleStatus | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_role_status_kv(kvbase, "key", 1)
```

---

## add_role_type_kv

method in GameAPI

- 描述

    添加ROLE_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.RoleType | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_role_type_kv(kvbase, "key", 1)
```

---

## add_role_relation_kv

method in GameAPI

- 描述

    添加ROLE_RELATION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.RoleRelation | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local relation = 1

GameAPI.add_role_relation_kv(kvbase, "key")
```

---

## add_team_kv

method in GameAPI

- 描述

    添加TEAM键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.Camp | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local camp = GameAPI.get_camp_by_camp_id(1)

GameAPI.add_team_kv(kvbase, "key")
```

---

## add_point_kv

method in GameAPI

- 描述

    添加POINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.FPoint | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local fpoint = GameAPI.get_point_by_res_id(1)

GameAPI.add_point_kv(kvbase, "key")
```

---

## add_vector3_kv

method in GameAPI

- 描述

    添加VECTOR3键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.FVector3 | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

GameAPI.add_vector3_kv(kvbase, "key")
```

---

## add_rotation_kv

method in GameAPI

- 描述

    添加ROTATION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.FRotation | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_rotation_kv(kvbase, "key")
```

---

## add_point_list_kv

method in GameAPI

- 描述

    添加POINT_LIST键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.Road | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local road = y3.road.get_road_by_res_id(1)

GameAPI.add_point_list_kv(kvbase, "key")
```

---

## add_rectangle_kv

method in GameAPI

- 描述

    添加RECTANGLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.RecArea | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local rec_area = GameAPI.create_rec_area_from_two_points(Fix32Vec3(0, 0, 0), Fix32Vec3(100, 100, 0))

GameAPI.add_rectangle_kv(kvbase, "key")
```

---

## add_round_area_kv

method in GameAPI

- 描述

    添加ROUND_AREA键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.CirArea | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local cir_area = GameAPI.create_new_cir_area(GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0)), Fix32(100))

GameAPI.add_round_area_kv(kvbase, "key")
```

---

## add_polygon_kv

method in GameAPI

- 描述

    添加POLYGON键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.PolyArea | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local poly_area = GameAPI.create_polygon_area(Fix32Vec3(0, 0, 0), Fix32Vec3(100, 0, 0), Fix32Vec3(100, 100, 0))

GameAPI.add_polygon_kv(kvbase, "key")
```

---

## add_camera_kv

method in GameAPI

- 描述

    添加CAMERA键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.Camera | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local camera = y3.camera.create_camera(y3.point(0, 0), 1000, 500, 0, 45, 3000)

GameAPI.add_camera_kv(kvbase, "key")
```

---

## add_camline_kv

method in GameAPI

- 描述

    添加CAMLINE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.CamlineID | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_camline_kv(kvbase, "key", 1)
```

---

## add_point_light_kv

method in GameAPI

- 描述

    添加POINT_LIGHT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.PointLight | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local point_light = GameAPI.get_point_light_res_by_res_id(1)

GameAPI.add_point_light_kv(kvbase, "key")
```

---

## add_spot_light_kv

method in GameAPI

- 描述

    添加SPOT_LIGHT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.SpotLight | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local spot_light = GameAPI.get_spot_light_res_by_res_id(1)

GameAPI.add_spot_light_kv(kvbase, "key")
```

---

## add_fog_kv

method in GameAPI

- 描述

    添加FOG键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.Fog | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local fog = GameAPI.get_fog_res_by_res_id(1)

GameAPI.add_fog_kv(kvbase, "key")
```

---

## add_scene_sound_kv

method in GameAPI

- 描述

    添加SCENE_SOUND键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.SceneSound | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local scene_sound = GameAPI.get_scene_sound_by_res_id(1)

GameAPI.add_scene_sound_kv(kvbase, "key")
```

---

## add_model_kv

method in GameAPI

- 描述

    添加MODEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.ModelKey | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local model_key = 1

GameAPI.add_model_kv(kvbase, "key")
```

---

## add_sfx_entity_kv

method in GameAPI

- 描述

    添加SFX_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.Sfx | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local sfx = y3.particle.create({ type = 134274569, target = y3.point(0, 0) }).handle

GameAPI.add_sfx_entity_kv(kvbase, "key")
```

---

## add_sfx_key_kv

method in GameAPI

- 描述

    添加SFX_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.SfxKey | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local sfx_key = 134274569

GameAPI.add_sfx_key_kv(kvbase, "key")
```

---

## add_link_sfx_entity_kv

method in GameAPI

- 描述

    添加LINK_SFX_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.LinkSfx | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local link_sfx = GameAPI.create_link_sfx_from_unit_to_point(134274569, unit.handle, "origin", GlobalAPI.coord_to_point(Fix32(100), Fix32(100), Fix32(0)), Fix32(0))

GameAPI.add_link_sfx_entity_kv(kvbase, "key")
```

---

## add_link_sfx_key_kv

method in GameAPI

- 描述

    添加LINK_SFX_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.LinkSfxKey | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_link_sfx_key_kv(kvbase, "key", 1)
```

---

## add_cursor_key_kv

method in GameAPI

- 描述

    添加CURSOR_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.CursorKey | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_cursor_key_kv(kvbase, "key", 1)
```

---

## add_angle_kv

method in GameAPI

- 描述

    添加ANGLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.Fixed | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_angle_kv(kvbase, "key", Fix32(1))
```

---

## add_texture_kv

method in GameAPI

- 描述

    添加TEXTURE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.Texture | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_texture_kv(kvbase, "key", 1)
```

---

## add_sequence_kv

method in GameAPI

- 描述

    添加SEQUENCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.Sequence | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_sequence_kv(kvbase, "key", 1)
```

---

## add_physics_object_kv

method in GameAPI

- 描述

    添加PHYSICS_OBJECT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.PhysicsObject | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local physics_object = GameAPI.get_unit_key_physics_object_kv(1, "key")

GameAPI.add_physics_object_kv(kvbase, "key")
```

---

## add_physics_entity_kv

method in GameAPI

- 描述

    添加PHYSICS_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.PhysicsEntity | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local physics_entity = GameAPI.get_unit_key_physics_entity_kv(1, "key")

GameAPI.add_physics_entity_kv(kvbase, "key")
```

---

## add_physics_object_key_kv

method in GameAPI

- 描述

    添加PHYSICS_OBJECT_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.PhysicsObjectKey | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_physics_object_key_kv(kvbase, "key", 1)
```

---

## add_physics_entity_key_kv

method in GameAPI

- 描述

    添加PHYSICS_ENTITY_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.PhysicsEntityKey | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_physics_entity_key_kv(kvbase, "key", 1)
```

---

## add_rigid_body_kv

method in GameAPI

- 描述

    添加RIGID_BODY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.RigidBody | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local rigid_body = GameAPI.get_unit_key_rigid_body_kv(1, "key")

GameAPI.add_rigid_body_kv(kvbase, "key")
```

---

## add_rigid_body_group_kv

method in GameAPI

- 描述

    添加RIGID_BODY_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.RigidBodyGroup | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local rigid_body_group = GameAPI.get_unit_key_rigid_body_group_kv(1, "key")

GameAPI.add_rigid_body_group_kv(kvbase, "key")
```

---

## add_collider_kv

method in GameAPI

- 描述

    添加COLLIDER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.Collider | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local collider = GameAPI.get_unit_key_collider_kv(1, "key")

GameAPI.add_collider_kv(kvbase, "key")
```

---

## add_joint_kv

method in GameAPI

- 描述

    添加JOINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.Joint | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local joint = GameAPI.get_unit_key_joint_kv(1, "key")

GameAPI.add_joint_kv(kvbase, "key")
```

---

## add_reaction_kv

method in GameAPI

- 描述

    添加REACTION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.Reaction | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local physics_entity = GameAPI.get_unit_key_physics_entity_kv(1, "key")
local reaction = GameAPI.api_add_uniform_gravitation_field_to_rigid_body(physics_entity, Fix32(10), Fix32Vec3(0, 0, 0))

GameAPI.add_reaction_kv(kvbase, "key")
```

---

## add_reaction_group_kv

method in GameAPI

- 描述

    添加REACTION_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.ReactionGroup | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local reaction_group = GameAPI.get_trigger_variable_reaction_group("key")

GameAPI.add_reaction_group_kv(kvbase, "key")
```

---

## add_dynamic_trigger_instance_kv

method in GameAPI

- 描述

    添加DYNAMIC_TRIGGER_INSTANCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.DynamicTriggerInstance | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local trigger_instance = GameAPI.get_last_created_trigger()

GameAPI.add_dynamic_trigger_instance_kv(kvbase, "key")
```

---

## add_table_kv

method in GameAPI

- 描述

    添加TABLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.Table | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local tbl = {}

GameAPI.add_table_kv(kvbase, "key")
```

---

## add_random_pool_kv

method in GameAPI

- 描述

    添加RANDOM_POOL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.RandomPool | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local random_pool = GameAPI.create_random_pool()

GameAPI.add_random_pool_kv(kvbase, "key")
```

---

## add_scene_ui_kv

method in GameAPI

- 描述

    添加SCENE_UI键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.SceneNode | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local player = y3.player.get_by_id(1)
local scene_node = GameAPI.create_scene_node_on_unit_ex("comp_name", player.handle, unit.handle, "origin", false)

GameAPI.add_scene_ui_kv(kvbase, "key")
```

---

## add_damage_type_kv

method in GameAPI

- 描述

    添加DAMAGE_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | integer | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_damage_type_kv(kvbase, "key", 1)
```

---

## add_harm_text_type_new_kv

method in GameAPI

- 描述

    添加HARM_TEXT_TYPE_NEW键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | string | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_harm_text_type_new_kv(kvbase, "key", "item")
```

---

## add_font_type_kv

method in GameAPI

- 描述

    添加FONT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | string | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_font_type_kv(kvbase, "key", "item")
```

---

## add_jump_word_track_kv

method in GameAPI

- 描述

    添加JUMP_WORD_TRACK键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | integer | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_jump_word_track_kv(kvbase, "key", 1)
```

---

## add_new_timer_kv

method in GameAPI

- 描述

    添加NEW_TIMER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.Timer | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local timer = y3.timer.loop(1, function() end)

GameAPI.add_new_timer_kv(kvbase, "key")
```

---

## add_tech_key_kv

method in GameAPI

- 描述

    添加TECH_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.TechKey | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local tech_key = 134274569

GameAPI.add_tech_key_kv(kvbase, "key")
```

---

## add_store_key_kv

method in GameAPI

- 描述

    添加STORE_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.StoreKey | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local store_key = 134274569

GameAPI.add_store_key_kv(kvbase, "key")
```

---

## add_keyboard_key_kv

method in GameAPI

- 描述

    添加KEYBOARD_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.KeyboardKey | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_keyboard_key_kv(kvbase, "key", 1)
```

---

## add_func_keyboard_key_kv

method in GameAPI

- 描述

    添加FUNC_KEYBOARD_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.FuncKeyboardKey | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_func_keyboard_key_kv(kvbase, "key", 1)
```

---

## add_mouse_key_kv

method in GameAPI

- 描述

    添加MOUSE_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.MouseKey | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_mouse_key_kv(kvbase, "key", 1)
```

---

## add_mouse_wheel_kv

method in GameAPI

- 描述

    添加MOUSE_WHEEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.MouseWheel | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_mouse_wheel_kv(kvbase, "key", 1)
```

---

## add_post_effect_kv

method in GameAPI

- 描述

    添加POST_EFFECT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.PostEffect | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_post_effect_kv(kvbase, "key", 1)
```

---

## add_unit_type_kv

method in GameAPI

- 描述

    添加UNIT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.UnitType | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_unit_type_kv(kvbase, "key", 1)
```

---

## add_unit_command_type_kv

method in GameAPI

- 描述

    添加UNIT_COMMAND_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.UnitCommandType | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_unit_command_type_kv(kvbase, "key", 1)
```

---

## add_mini_map_color_type_kv

method in GameAPI

- 描述

    添加MINI_MAP_COLOR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.MiniMapColorType | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_mini_map_color_type_kv(kvbase, "key", 1)
```

---

## add_unit_behavior_kv

method in GameAPI

- 描述

    添加UNIT_BEHAVIOR键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.UnitBehavior | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local unit_behavior = "unit_behavior"

GameAPI.add_unit_behavior_kv(kvbase, "key")
```

---

## add_curved_path_kv

method in GameAPI

- 描述

    添加CURVED_PATH键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.CurvedPath | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local path = {}

GameAPI.add_curved_path_kv(kvbase, "key")
```

---

## add_curved_path_3d_kv

method in GameAPI

- 描述

    添加CURVED_PATH_3D键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.CurvedPath3D | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local curved_path_3d = {}

GameAPI.add_curved_path_3d_kv(kvbase, "key")
```

---

## has_kv_pair

method in GameAPI

- 描述

    判断是否存在键值对(忽略类型)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 布尔值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair(kvbase, "key")
```

---

## has_prefab_kv_any

method in GameAPI

- 描述

    判断预设类型是否存在键值对(忽略类型)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_type | string | 预设种类表 |
    | prefab_key | integer | 预设编号 |
    | key | string | 键名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 布尔值 |

- 示例

```lua
local result = GameAPI.has_prefab_kv_any("prefab_type", 1, "key")
```

---

## has_kv_pair_boolean

method in GameAPI

- 描述

    判断是否存在BOOLEAN键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_boolean(kvbase, "key")
```

---

## has_unit_key_boolean_kv

method in GameAPI

- 描述

    判断单位编号是否存在BOOLEAN键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_boolean_kv(unit_key, "key")
```

---

## has_item_key_boolean_kv

method in GameAPI

- 描述

    判断物品编号是否存在BOOLEAN键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_boolean_kv(item_key, "key")
```

---

## has_ability_key_boolean_kv

method in GameAPI

- 描述

    判断技能编号是否存在BOOLEAN键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_boolean_kv(ability_key, "key")
```

---

## has_kv_pair_integer

method in GameAPI

- 描述

    判断是否存在INTEGER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_integer(kvbase, "key")
```

---

## has_unit_key_integer_kv

method in GameAPI

- 描述

    判断单位编号是否存在INTEGER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_integer_kv(unit_key, "key")
```

---

## has_item_key_integer_kv

method in GameAPI

- 描述

    判断物品编号是否存在INTEGER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_integer_kv(item_key, "key")
```

---

## has_ability_key_integer_kv

method in GameAPI

- 描述

    判断技能编号是否存在INTEGER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_integer_kv(ability_key, "key")
```

---

## has_kv_pair_float

method in GameAPI

- 描述

    判断是否存在FLOAT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_float(kvbase, "key")
```

---

## has_unit_key_float_kv

method in GameAPI

- 描述

    判断单位编号是否存在FLOAT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_float_kv(unit_key, "key")
```

---

## has_item_key_float_kv

method in GameAPI

- 描述

    判断物品编号是否存在FLOAT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_float_kv(item_key, "key")
```

---

## has_ability_key_float_kv

method in GameAPI

- 描述

    判断技能编号是否存在FLOAT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_float_kv(ability_key, "key")
```

---

## has_kv_pair_string

method in GameAPI

- 描述

    判断是否存在STRING键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_string(kvbase, "key")
```

---

## has_unit_key_string_kv

method in GameAPI

- 描述

    判断单位编号是否存在STRING键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_string_kv(unit_key, "key")
```

---

## has_item_key_string_kv

method in GameAPI

- 描述

    判断物品编号是否存在STRING键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_string_kv(item_key, "key")
```

---

## has_ability_key_string_kv

method in GameAPI

- 描述

    判断技能编号是否存在STRING键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_string_kv(ability_key, "key")
```

---

## has_kv_pair_ui_comp

method in GameAPI

- 描述

    判断是否存在UI_COMP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_ui_comp(kvbase, "key")
```

---

## has_unit_key_ui_comp_kv

method in GameAPI

- 描述

    判断单位编号是否存在UI_COMP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_ui_comp_kv(unit_key, "key")
```

---

## has_item_key_ui_comp_kv

method in GameAPI

- 描述

    判断物品编号是否存在UI_COMP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_ui_comp_kv(item_key, "key")
```

---

## has_ability_key_ui_comp_kv

method in GameAPI

- 描述

    判断技能编号是否存在UI_COMP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_ui_comp_kv(ability_key, "key")
```

---

## has_kv_pair_ui_comp_type

method in GameAPI

- 描述

    判断是否存在UI_COMP_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_ui_comp_type(kvbase, "key")
```

---

## has_unit_key_ui_comp_type_kv

method in GameAPI

- 描述

    判断单位编号是否存在UI_COMP_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_ui_comp_type_kv(unit_key, "key")
```

---

## has_item_key_ui_comp_type_kv

method in GameAPI

- 描述

    判断物品编号是否存在UI_COMP_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_ui_comp_type_kv(item_key, "key")
```

---

## has_ability_key_ui_comp_type_kv

method in GameAPI

- 描述

    判断技能编号是否存在UI_COMP_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_ui_comp_type_kv(ability_key, "key")
```

---

## has_kv_pair_ui_comp_event_type

method in GameAPI

- 描述

    判断是否存在UI_COMP_EVENT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_ui_comp_event_type(kvbase, "key")
```

---

## has_unit_key_ui_comp_event_type_kv

method in GameAPI

- 描述

    判断单位编号是否存在UI_COMP_EVENT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_ui_comp_event_type_kv(unit_key, "key")
```

---

## has_item_key_ui_comp_event_type_kv

method in GameAPI

- 描述

    判断物品编号是否存在UI_COMP_EVENT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_ui_comp_event_type_kv(item_key, "key")
```

---

## has_ability_key_ui_comp_event_type_kv

method in GameAPI

- 描述

    判断技能编号是否存在UI_COMP_EVENT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_ui_comp_event_type_kv(ability_key, "key")
```

---

## has_kv_pair_ui_comp_attr

method in GameAPI

- 描述

    判断是否存在UI_COMP_ATTR键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_ui_comp_attr(kvbase, "key")
```

---

## has_unit_key_ui_comp_attr_kv

method in GameAPI

- 描述

    判断单位编号是否存在UI_COMP_ATTR键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_ui_comp_attr_kv(unit_key, "key")
```

---

## has_item_key_ui_comp_attr_kv

method in GameAPI

- 描述

    判断物品编号是否存在UI_COMP_ATTR键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_ui_comp_attr_kv(item_key, "key")
```

---

## has_ability_key_ui_comp_attr_kv

method in GameAPI

- 描述

    判断技能编号是否存在UI_COMP_ATTR键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_ui_comp_attr_kv(ability_key, "key")
```

---

## has_kv_pair_ui_comp_align_type

method in GameAPI

- 描述

    判断是否存在UI_COMP_ALIGN_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_ui_comp_align_type(kvbase, "key")
```

---

## has_unit_key_ui_comp_align_type_kv

method in GameAPI

- 描述

    判断单位编号是否存在UI_COMP_ALIGN_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_ui_comp_align_type_kv(unit_key, "key")
```

---

## has_item_key_ui_comp_align_type_kv

method in GameAPI

- 描述

    判断物品编号是否存在UI_COMP_ALIGN_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_ui_comp_align_type_kv(item_key, "key")
```

---

## has_ability_key_ui_comp_align_type_kv

method in GameAPI

- 描述

    判断技能编号是否存在UI_COMP_ALIGN_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_ui_comp_align_type_kv(ability_key, "key")
```

---

## has_kv_pair_ui_prefab

method in GameAPI

- 描述

    判断是否存在UI_PREFAB键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_ui_prefab(kvbase, "key")
```

---

## has_unit_key_ui_prefab_kv

method in GameAPI

- 描述

    判断单位编号是否存在UI_PREFAB键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_ui_prefab_kv(unit_key, "key")
```

---

## has_item_key_ui_prefab_kv

method in GameAPI

- 描述

    判断物品编号是否存在UI_PREFAB键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_ui_prefab_kv(item_key, "key")
```

---

## has_ability_key_ui_prefab_kv

method in GameAPI

- 描述

    判断技能编号是否存在UI_PREFAB键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_ui_prefab_kv(ability_key, "key")
```

---

## has_kv_pair_ui_prefab_instance

method in GameAPI

- 描述

    判断是否存在UI_PREFAB_INSTANCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_ui_prefab_instance(kvbase, "key")
```

---

## has_unit_key_ui_prefab_instance_kv

method in GameAPI

- 描述

    判断单位编号是否存在UI_PREFAB_INSTANCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_ui_prefab_instance_kv(unit_key, "key")
```

---

## has_item_key_ui_prefab_instance_kv

method in GameAPI

- 描述

    判断物品编号是否存在UI_PREFAB_INSTANCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_ui_prefab_instance_kv(item_key, "key")
```

---

## has_ability_key_ui_prefab_instance_kv

method in GameAPI

- 描述

    判断技能编号是否存在UI_PREFAB_INSTANCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_ui_prefab_instance_kv(ability_key, "key")
```

---

## has_kv_pair_ui_prefab_ins_uid

method in GameAPI

- 描述

    判断是否存在UI_PREFAB_INS_UID键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_ui_prefab_ins_uid(kvbase, "key")
```

---

## has_unit_key_ui_prefab_ins_uid_kv

method in GameAPI

- 描述

    判断单位编号是否存在UI_PREFAB_INS_UID键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_ui_prefab_ins_uid_kv(unit_key, "key")
```

---

## has_item_key_ui_prefab_ins_uid_kv

method in GameAPI

- 描述

    判断物品编号是否存在UI_PREFAB_INS_UID键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_ui_prefab_ins_uid_kv(item_key, "key")
```

---

## has_ability_key_ui_prefab_ins_uid_kv

method in GameAPI

- 描述

    判断技能编号是否存在UI_PREFAB_INS_UID键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_ui_prefab_ins_uid_kv(ability_key, "key")
```

---

## has_kv_pair_ui_direction

method in GameAPI

- 描述

    判断是否存在UI_DIRECTION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_ui_direction(kvbase, "key")
```

---

## has_unit_key_ui_direction_kv

method in GameAPI

- 描述

    判断单位编号是否存在UI_DIRECTION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_ui_direction_kv(unit_key, "key")
```

---

## has_item_key_ui_direction_kv

method in GameAPI

- 描述

    判断物品编号是否存在UI_DIRECTION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_ui_direction_kv(item_key, "key")
```

---

## has_ability_key_ui_direction_kv

method in GameAPI

- 描述

    判断技能编号是否存在UI_DIRECTION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_ui_direction_kv(ability_key, "key")
```

---

## has_kv_pair_ui_model_camera_mod

method in GameAPI

- 描述

    判断是否存在UI_MODEL_CAMERA_MOD键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_ui_model_camera_mod(kvbase, "key")
```

---

## has_unit_key_ui_model_camera_mod_kv

method in GameAPI

- 描述

    判断单位编号是否存在UI_MODEL_CAMERA_MOD键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_ui_model_camera_mod_kv(unit_key, "key")
```

---

## has_item_key_ui_model_camera_mod_kv

method in GameAPI

- 描述

    判断物品编号是否存在UI_MODEL_CAMERA_MOD键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_ui_model_camera_mod_kv(item_key, "key")
```

---

## has_ability_key_ui_model_camera_mod_kv

method in GameAPI

- 描述

    判断技能编号是否存在UI_MODEL_CAMERA_MOD键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_ui_model_camera_mod_kv(ability_key, "key")
```

---

## has_kv_pair_ui_btn_status

method in GameAPI

- 描述

    判断是否存在UI_BTN_STATUS键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_ui_btn_status(kvbase, "key")
```

---

## has_unit_key_ui_btn_status_kv

method in GameAPI

- 描述

    判断单位编号是否存在UI_BTN_STATUS键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_ui_btn_status_kv(unit_key, "key")
```

---

## has_item_key_ui_btn_status_kv

method in GameAPI

- 描述

    判断物品编号是否存在UI_BTN_STATUS键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_ui_btn_status_kv(item_key, "key")
```

---

## has_ability_key_ui_btn_status_kv

method in GameAPI

- 描述

    判断技能编号是否存在UI_BTN_STATUS键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_ui_btn_status_kv(ability_key, "key")
```

---

## has_kv_pair_ui_scrollview_type

method in GameAPI

- 描述

    判断是否存在UI_SCROLLVIEW_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_ui_scrollview_type(kvbase, "key")
```

---

## has_unit_key_ui_scrollview_type_kv

method in GameAPI

- 描述

    判断单位编号是否存在UI_SCROLLVIEW_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_ui_scrollview_type_kv(unit_key, "key")
```

---

## has_item_key_ui_scrollview_type_kv

method in GameAPI

- 描述

    判断物品编号是否存在UI_SCROLLVIEW_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_ui_scrollview_type_kv(item_key, "key")
```

---

## has_ability_key_ui_scrollview_type_kv

method in GameAPI

- 描述

    判断技能编号是否存在UI_SCROLLVIEW_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_ui_scrollview_type_kv(ability_key, "key")
```

---

## has_kv_pair_ui_anim

method in GameAPI

- 描述

    判断是否存在UI_ANIM键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_ui_anim(kvbase, "key")
```

---

## has_unit_key_ui_anim_kv

method in GameAPI

- 描述

    判断单位编号是否存在UI_ANIM键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_ui_anim_kv(unit_key, "key")
```

---

## has_item_key_ui_anim_kv

method in GameAPI

- 描述

    判断物品编号是否存在UI_ANIM键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_ui_anim_kv(item_key, "key")
```

---

## has_ability_key_ui_anim_kv

method in GameAPI

- 描述

    判断技能编号是否存在UI_ANIM键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_ui_anim_kv(ability_key, "key")
```

---

## has_kv_pair_ui_anim_curve

method in GameAPI

- 描述

    判断是否存在UI_ANIM_CURVE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_ui_anim_curve(kvbase, "key")
```

---

## has_unit_key_ui_anim_curve_kv

method in GameAPI

- 描述

    判断单位编号是否存在UI_ANIM_CURVE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_ui_anim_curve_kv(unit_key, "key")
```

---

## has_item_key_ui_anim_curve_kv

method in GameAPI

- 描述

    判断物品编号是否存在UI_ANIM_CURVE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_ui_anim_curve_kv(item_key, "key")
```

---

## has_ability_key_ui_anim_curve_kv

method in GameAPI

- 描述

    判断技能编号是否存在UI_ANIM_CURVE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_ui_anim_curve_kv(ability_key, "key")
```

---

## has_kv_pair_audio_channel

method in GameAPI

- 描述

    判断是否存在AUDIO_CHANNEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_audio_channel(kvbase, "key")
```

---

## has_unit_key_audio_channel_kv

method in GameAPI

- 描述

    判断单位编号是否存在AUDIO_CHANNEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_audio_channel_kv(unit_key, "key")
```

---

## has_item_key_audio_channel_kv

method in GameAPI

- 描述

    判断物品编号是否存在AUDIO_CHANNEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_audio_channel_kv(item_key, "key")
```

---

## has_ability_key_audio_channel_kv

method in GameAPI

- 描述

    判断技能编号是否存在AUDIO_CHANNEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_audio_channel_kv(ability_key, "key")
```

---

## has_kv_pair_unit_entity

method in GameAPI

- 描述

    判断是否存在UNIT_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_unit_entity(kvbase, "key")
```

---

## has_unit_key_unit_entity_kv

method in GameAPI

- 描述

    判断单位编号是否存在UNIT_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_unit_entity_kv(unit_key, "key")
```

---

## has_item_key_unit_entity_kv

method in GameAPI

- 描述

    判断物品编号是否存在UNIT_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_unit_entity_kv(item_key, "key")
```

---

## has_ability_key_unit_entity_kv

method in GameAPI

- 描述

    判断技能编号是否存在UNIT_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_unit_entity_kv(ability_key, "key")
```

---

## has_kv_pair_unit_group

method in GameAPI

- 描述

    判断是否存在UNIT_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_unit_group(kvbase, "key")
```

---

## has_unit_key_unit_group_kv

method in GameAPI

- 描述

    判断单位编号是否存在UNIT_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_unit_group_kv(unit_key, "key")
```

---

## has_item_key_unit_group_kv

method in GameAPI

- 描述

    判断物品编号是否存在UNIT_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_unit_group_kv(item_key, "key")
```

---

## has_ability_key_unit_group_kv

method in GameAPI

- 描述

    判断技能编号是否存在UNIT_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_unit_group_kv(ability_key, "key")
```

---

## has_kv_pair_unit_name

method in GameAPI

- 描述

    判断是否存在UNIT_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_unit_name(kvbase, "key")
```

---

## has_unit_key_unit_name_kv

method in GameAPI

- 描述

    判断单位编号是否存在UNIT_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_unit_name_kv(unit_key, "key")
```

---

## has_item_key_unit_name_kv

method in GameAPI

- 描述

    判断物品编号是否存在UNIT_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_unit_name_kv(item_key, "key")
```

---

## has_ability_key_unit_name_kv

method in GameAPI

- 描述

    判断技能编号是否存在UNIT_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_unit_name_kv(ability_key, "key")
```

---

## has_kv_pair_unit_name_pool

method in GameAPI

- 描述

    判断是否存在UNIT_NAME_POOL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_unit_name_pool(kvbase, "key")
```

---

## has_unit_key_unit_name_pool_kv

method in GameAPI

- 描述

    判断单位编号是否存在UNIT_NAME_POOL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_unit_name_pool_kv(unit_key, "key")
```

---

## has_item_key_unit_name_pool_kv

method in GameAPI

- 描述

    判断物品编号是否存在UNIT_NAME_POOL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_unit_name_pool_kv(item_key, "key")
```

---

## has_ability_key_unit_name_pool_kv

method in GameAPI

- 描述

    判断技能编号是否存在UNIT_NAME_POOL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_unit_name_pool_kv(ability_key, "key")
```

---

## has_kv_pair_unit_write_attribute

method in GameAPI

- 描述

    判断是否存在UNIT_WRITE_ATTRIBUTE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_unit_write_attribute(kvbase, "key")
```

---

## has_unit_key_unit_write_attribute_kv

method in GameAPI

- 描述

    判断单位编号是否存在UNIT_WRITE_ATTRIBUTE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_unit_write_attribute_kv(unit_key, "key")
```

---

## has_item_key_unit_write_attribute_kv

method in GameAPI

- 描述

    判断物品编号是否存在UNIT_WRITE_ATTRIBUTE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_unit_write_attribute_kv(item_key, "key")
```

---

## has_ability_key_unit_write_attribute_kv

method in GameAPI

- 描述

    判断技能编号是否存在UNIT_WRITE_ATTRIBUTE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_unit_write_attribute_kv(ability_key, "key")
```

---

## has_kv_pair_attr_element

method in GameAPI

- 描述

    判断是否存在ATTR_ELEMENT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_attr_element(kvbase, "key")
```

---

## has_unit_key_attr_element_kv

method in GameAPI

- 描述

    判断单位编号是否存在ATTR_ELEMENT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_attr_element_kv(unit_key, "key")
```

---

## has_item_key_attr_element_kv

method in GameAPI

- 描述

    判断物品编号是否存在ATTR_ELEMENT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_attr_element_kv(item_key, "key")
```

---

## has_ability_key_attr_element_kv

method in GameAPI

- 描述

    判断技能编号是否存在ATTR_ELEMENT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_attr_element_kv(ability_key, "key")
```

---

## has_kv_pair_attr_element_read

method in GameAPI

- 描述

    判断是否存在ATTR_ELEMENT_READ键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_attr_element_read(kvbase, "key")
```

---

## has_unit_key_attr_element_read_kv

method in GameAPI

- 描述

    判断单位编号是否存在ATTR_ELEMENT_READ键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_attr_element_read_kv(unit_key, "key")
```

---

## has_item_key_attr_element_read_kv

method in GameAPI

- 描述

    判断物品编号是否存在ATTR_ELEMENT_READ键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_attr_element_read_kv(item_key, "key")
```

---

## has_ability_key_attr_element_read_kv

method in GameAPI

- 描述

    判断技能编号是否存在ATTR_ELEMENT_READ键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_attr_element_read_kv(ability_key, "key")
```

---

## has_kv_pair_mover_entity

method in GameAPI

- 描述

    判断是否存在MOVER_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_mover_entity(kvbase, "key")
```

---

## has_unit_key_mover_entity_kv

method in GameAPI

- 描述

    判断单位编号是否存在MOVER_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_mover_entity_kv(unit_key, "key")
```

---

## has_item_key_mover_entity_kv

method in GameAPI

- 描述

    判断物品编号是否存在MOVER_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_mover_entity_kv(item_key, "key")
```

---

## has_ability_key_mover_entity_kv

method in GameAPI

- 描述

    判断技能编号是否存在MOVER_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_mover_entity_kv(ability_key, "key")
```

---

## has_kv_pair_image_quality

method in GameAPI

- 描述

    判断是否存在IMAGE_QUALITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_image_quality(kvbase, "key")
```

---

## has_unit_key_image_quality_kv

method in GameAPI

- 描述

    判断单位编号是否存在IMAGE_QUALITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_image_quality_kv(unit_key, "key")
```

---

## has_item_key_image_quality_kv

method in GameAPI

- 描述

    判断物品编号是否存在IMAGE_QUALITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_image_quality_kv(item_key, "key")
```

---

## has_ability_key_image_quality_kv

method in GameAPI

- 描述

    判断技能编号是否存在IMAGE_QUALITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_image_quality_kv(ability_key, "key")
```

---

## has_kv_pair_window_type_setting

method in GameAPI

- 描述

    判断是否存在WINDOW_TYPE_SETTING键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_window_type_setting(kvbase, "key")
```

---

## has_unit_key_window_type_setting_kv

method in GameAPI

- 描述

    判断单位编号是否存在WINDOW_TYPE_SETTING键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_window_type_setting_kv(unit_key, "key")
```

---

## has_item_key_window_type_setting_kv

method in GameAPI

- 描述

    判断物品编号是否存在WINDOW_TYPE_SETTING键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_window_type_setting_kv(item_key, "key")
```

---

## has_ability_key_window_type_setting_kv

method in GameAPI

- 描述

    判断技能编号是否存在WINDOW_TYPE_SETTING键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_window_type_setting_kv(ability_key, "key")
```

---

## has_kv_pair_item_entity

method in GameAPI

- 描述

    判断是否存在ITEM_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_item_entity(kvbase, "key")
```

---

## has_unit_key_item_entity_kv

method in GameAPI

- 描述

    判断单位编号是否存在ITEM_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_item_entity_kv(unit_key, "key")
```

---

## has_item_key_item_entity_kv

method in GameAPI

- 描述

    判断物品编号是否存在ITEM_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_item_entity_kv(item_key, "key")
```

---

## has_ability_key_item_entity_kv

method in GameAPI

- 描述

    判断技能编号是否存在ITEM_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_item_entity_kv(ability_key, "key")
```

---

## has_kv_pair_item_group

method in GameAPI

- 描述

    判断是否存在ITEM_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_item_group(kvbase, "key")
```

---

## has_unit_key_item_group_kv

method in GameAPI

- 描述

    判断单位编号是否存在ITEM_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_item_group_kv(unit_key, "key")
```

---

## has_item_key_item_group_kv

method in GameAPI

- 描述

    判断物品编号是否存在ITEM_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_item_group_kv(item_key, "key")
```

---

## has_ability_key_item_group_kv

method in GameAPI

- 描述

    判断技能编号是否存在ITEM_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_item_group_kv(ability_key, "key")
```

---

## has_kv_pair_item_name

method in GameAPI

- 描述

    判断是否存在ITEM_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_item_name(kvbase, "key")
```

---

## has_unit_key_item_name_kv

method in GameAPI

- 描述

    判断单位编号是否存在ITEM_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_item_name_kv(unit_key, "key")
```

---

## has_item_key_item_name_kv

method in GameAPI

- 描述

    判断物品编号是否存在ITEM_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_item_name_kv(item_key, "key")
```

---

## has_ability_key_item_name_kv

method in GameAPI

- 描述

    判断技能编号是否存在ITEM_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_item_name_kv(ability_key, "key")
```

---

## has_kv_pair_ability

method in GameAPI

- 描述

    判断是否存在ABILITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_ability(kvbase, "key")
```

---

## has_unit_key_ability_kv

method in GameAPI

- 描述

    判断单位编号是否存在ABILITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_ability_kv(unit_key, "key")
```

---

## has_item_key_ability_kv

method in GameAPI

- 描述

    判断物品编号是否存在ABILITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_ability_kv(item_key, "key")
```

---

## has_ability_key_ability_kv

method in GameAPI

- 描述

    判断技能编号是否存在ABILITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_ability_kv(ability_key, "key")
```

---

## has_kv_pair_ability_type

method in GameAPI

- 描述

    判断是否存在ABILITY_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_ability_type(kvbase, "key")
```

---

## has_unit_key_ability_type_kv

method in GameAPI

- 描述

    判断单位编号是否存在ABILITY_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_ability_type_kv(unit_key, "key")
```

---

## has_item_key_ability_type_kv

method in GameAPI

- 描述

    判断物品编号是否存在ABILITY_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_ability_type_kv(item_key, "key")
```

---

## has_ability_key_ability_type_kv

method in GameAPI

- 描述

    判断技能编号是否存在ABILITY_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_ability_type_kv(ability_key, "key")
```

---

## has_kv_pair_ability_cast_type

method in GameAPI

- 描述

    判断是否存在ABILITY_CAST_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_ability_cast_type(kvbase, "key")
```

---

## has_unit_key_ability_cast_type_kv

method in GameAPI

- 描述

    判断单位编号是否存在ABILITY_CAST_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_ability_cast_type_kv(unit_key, "key")
```

---

## has_item_key_ability_cast_type_kv

method in GameAPI

- 描述

    判断物品编号是否存在ABILITY_CAST_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_ability_cast_type_kv(item_key, "key")
```

---

## has_ability_key_ability_cast_type_kv

method in GameAPI

- 描述

    判断技能编号是否存在ABILITY_CAST_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_ability_cast_type_kv(ability_key, "key")
```

---

## has_kv_pair_ability_name

method in GameAPI

- 描述

    判断是否存在ABILITY_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_ability_name(kvbase, "key")
```

---

## has_unit_key_ability_name_kv

method in GameAPI

- 描述

    判断单位编号是否存在ABILITY_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_ability_name_kv(unit_key, "key")
```

---

## has_item_key_ability_name_kv

method in GameAPI

- 描述

    判断物品编号是否存在ABILITY_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_ability_name_kv(item_key, "key")
```

---

## has_ability_key_ability_name_kv

method in GameAPI

- 描述

    判断技能编号是否存在ABILITY_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_ability_name_kv(ability_key, "key")
```

---

## has_kv_pair_skill_pointer_type

method in GameAPI

- 描述

    判断是否存在SKILL_POINTER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_skill_pointer_type(kvbase, "key")
```

---

## has_unit_key_skill_pointer_type_kv

method in GameAPI

- 描述

    判断单位编号是否存在SKILL_POINTER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_skill_pointer_type_kv(unit_key, "key")
```

---

## has_item_key_skill_pointer_type_kv

method in GameAPI

- 描述

    判断物品编号是否存在SKILL_POINTER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_skill_pointer_type_kv(item_key, "key")
```

---

## has_ability_key_skill_pointer_type_kv

method in GameAPI

- 描述

    判断技能编号是否存在SKILL_POINTER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_skill_pointer_type_kv(ability_key, "key")
```

---

## has_kv_pair_modifier_entity

method in GameAPI

- 描述

    判断是否存在MODIFIER_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_modifier_entity(kvbase, "key")
```

---

## has_unit_key_modifier_entity_kv

method in GameAPI

- 描述

    判断单位编号是否存在MODIFIER_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_modifier_entity_kv(unit_key, "key")
```

---

## has_item_key_modifier_entity_kv

method in GameAPI

- 描述

    判断物品编号是否存在MODIFIER_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_modifier_entity_kv(item_key, "key")
```

---

## has_ability_key_modifier_entity_kv

method in GameAPI

- 描述

    判断技能编号是否存在MODIFIER_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_modifier_entity_kv(ability_key, "key")
```

---

## has_kv_pair_modifier_type

method in GameAPI

- 描述

    判断是否存在MODIFIER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_modifier_type(kvbase, "key")
```

---

## has_unit_key_modifier_type_kv

method in GameAPI

- 描述

    判断单位编号是否存在MODIFIER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_modifier_type_kv(unit_key, "key")
```

---

## has_item_key_modifier_type_kv

method in GameAPI

- 描述

    判断物品编号是否存在MODIFIER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_modifier_type_kv(item_key, "key")
```

---

## has_ability_key_modifier_type_kv

method in GameAPI

- 描述

    判断技能编号是否存在MODIFIER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_modifier_type_kv(ability_key, "key")
```

---

## has_kv_pair_modifier_effect_type

method in GameAPI

- 描述

    判断是否存在MODIFIER_EFFECT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_modifier_effect_type(kvbase, "key")
```

---

## has_unit_key_modifier_effect_type_kv

method in GameAPI

- 描述

    判断单位编号是否存在MODIFIER_EFFECT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_modifier_effect_type_kv(unit_key, "key")
```

---

## has_item_key_modifier_effect_type_kv

method in GameAPI

- 描述

    判断物品编号是否存在MODIFIER_EFFECT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_modifier_effect_type_kv(item_key, "key")
```

---

## has_ability_key_modifier_effect_type_kv

method in GameAPI

- 描述

    判断技能编号是否存在MODIFIER_EFFECT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_modifier_effect_type_kv(ability_key, "key")
```

---

## has_kv_pair_modifier

method in GameAPI

- 描述

    判断是否存在MODIFIER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_modifier(kvbase, "key")
```

---

## has_unit_key_modifier_kv

method in GameAPI

- 描述

    判断单位编号是否存在MODIFIER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_modifier_kv(unit_key, "key")
```

---

## has_item_key_modifier_kv

method in GameAPI

- 描述

    判断物品编号是否存在MODIFIER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_modifier_kv(item_key, "key")
```

---

## has_ability_key_modifier_kv

method in GameAPI

- 描述

    判断技能编号是否存在MODIFIER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_modifier_kv(ability_key, "key")
```

---

## has_kv_pair_projectile

method in GameAPI

- 描述

    判断是否存在PROJECTILE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_projectile(kvbase, "key")
```

---

## has_unit_key_projectile_kv

method in GameAPI

- 描述

    判断单位编号是否存在PROJECTILE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_projectile_kv(unit_key, "key")
```

---

## has_item_key_projectile_kv

method in GameAPI

- 描述

    判断物品编号是否存在PROJECTILE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_projectile_kv(item_key, "key")
```

---

## has_ability_key_projectile_kv

method in GameAPI

- 描述

    判断技能编号是否存在PROJECTILE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_projectile_kv(ability_key, "key")
```

---

## has_kv_pair_projectile_entity

method in GameAPI

- 描述

    判断是否存在PROJECTILE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_projectile_entity(kvbase, "key")
```

---

## has_unit_key_projectile_entity_kv

method in GameAPI

- 描述

    判断单位编号是否存在PROJECTILE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_projectile_entity_kv(unit_key, "key")
```

---

## has_item_key_projectile_entity_kv

method in GameAPI

- 描述

    判断物品编号是否存在PROJECTILE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_projectile_entity_kv(item_key, "key")
```

---

## has_ability_key_projectile_entity_kv

method in GameAPI

- 描述

    判断技能编号是否存在PROJECTILE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_projectile_entity_kv(ability_key, "key")
```

---

## has_kv_pair_projectile_group

method in GameAPI

- 描述

    判断是否存在PROJECTILE_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_projectile_group(kvbase, "key")
```

---

## has_unit_key_projectile_group_kv

method in GameAPI

- 描述

    判断单位编号是否存在PROJECTILE_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_projectile_group_kv(unit_key, "key")
```

---

## has_item_key_projectile_group_kv

method in GameAPI

- 描述

    判断物品编号是否存在PROJECTILE_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_projectile_group_kv(item_key, "key")
```

---

## has_ability_key_projectile_group_kv

method in GameAPI

- 描述

    判断技能编号是否存在PROJECTILE_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_projectile_group_kv(ability_key, "key")
```

---

## has_kv_pair_destructible_entity

method in GameAPI

- 描述

    判断是否存在DESTRUCTIBLE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_destructible_entity(kvbase, "key")
```

---

## has_unit_key_destructible_entity_kv

method in GameAPI

- 描述

    判断单位编号是否存在DESTRUCTIBLE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_destructible_entity_kv(unit_key, "key")
```

---

## has_item_key_destructible_entity_kv

method in GameAPI

- 描述

    判断物品编号是否存在DESTRUCTIBLE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_destructible_entity_kv(item_key, "key")
```

---

## has_ability_key_destructible_entity_kv

method in GameAPI

- 描述

    判断技能编号是否存在DESTRUCTIBLE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_destructible_entity_kv(ability_key, "key")
```

---

## has_kv_pair_destructible_name

method in GameAPI

- 描述

    判断是否存在DESTRUCTIBLE_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_destructible_name(kvbase, "key")
```

---

## has_unit_key_destructible_name_kv

method in GameAPI

- 描述

    判断单位编号是否存在DESTRUCTIBLE_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_destructible_name_kv(unit_key, "key")
```

---

## has_item_key_destructible_name_kv

method in GameAPI

- 描述

    判断物品编号是否存在DESTRUCTIBLE_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_destructible_name_kv(item_key, "key")
```

---

## has_ability_key_destructible_name_kv

method in GameAPI

- 描述

    判断技能编号是否存在DESTRUCTIBLE_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_destructible_name_kv(ability_key, "key")
```

---

## has_kv_pair_sound_entity

method in GameAPI

- 描述

    判断是否存在SOUND_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_sound_entity(kvbase, "key")
```

---

## has_unit_key_sound_entity_kv

method in GameAPI

- 描述

    判断单位编号是否存在SOUND_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_sound_entity_kv(unit_key, "key")
```

---

## has_item_key_sound_entity_kv

method in GameAPI

- 描述

    判断物品编号是否存在SOUND_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_sound_entity_kv(item_key, "key")
```

---

## has_ability_key_sound_entity_kv

method in GameAPI

- 描述

    判断技能编号是否存在SOUND_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_sound_entity_kv(ability_key, "key")
```

---

## has_kv_pair_audio_key

method in GameAPI

- 描述

    判断是否存在AUDIO_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_audio_key(kvbase, "key")
```

---

## has_unit_key_audio_key_kv

method in GameAPI

- 描述

    判断单位编号是否存在AUDIO_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_audio_key_kv(unit_key, "key")
```

---

## has_item_key_audio_key_kv

method in GameAPI

- 描述

    判断物品编号是否存在AUDIO_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_audio_key_kv(item_key, "key")
```

---

## has_ability_key_audio_key_kv

method in GameAPI

- 描述

    判断技能编号是否存在AUDIO_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_audio_key_kv(ability_key, "key")
```

---

## has_kv_pair_game_mode

method in GameAPI

- 描述

    判断是否存在GAME_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_game_mode(kvbase, "key")
```

---

## has_unit_key_game_mode_kv

method in GameAPI

- 描述

    判断单位编号是否存在GAME_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_game_mode_kv(unit_key, "key")
```

---

## has_item_key_game_mode_kv

method in GameAPI

- 描述

    判断物品编号是否存在GAME_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_game_mode_kv(item_key, "key")
```

---

## has_ability_key_game_mode_kv

method in GameAPI

- 描述

    判断技能编号是否存在GAME_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_game_mode_kv(ability_key, "key")
```

---

## has_kv_pair_player

method in GameAPI

- 描述

    判断是否存在PLAYER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_player(kvbase, "key")
```

---

## has_unit_key_player_kv

method in GameAPI

- 描述

    判断单位编号是否存在PLAYER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_player_kv(unit_key, "key")
```

---

## has_item_key_player_kv

method in GameAPI

- 描述

    判断物品编号是否存在PLAYER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_player_kv(item_key, "key")
```

---

## has_ability_key_player_kv

method in GameAPI

- 描述

    判断技能编号是否存在PLAYER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_player_kv(ability_key, "key")
```

---

## has_kv_pair_player_group

method in GameAPI

- 描述

    判断是否存在PLAYER_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_player_group(kvbase, "key")
```

---

## has_unit_key_player_group_kv

method in GameAPI

- 描述

    判断单位编号是否存在PLAYER_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_player_group_kv(unit_key, "key")
```

---

## has_item_key_player_group_kv

method in GameAPI

- 描述

    判断物品编号是否存在PLAYER_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_player_group_kv(item_key, "key")
```

---

## has_ability_key_player_group_kv

method in GameAPI

- 描述

    判断技能编号是否存在PLAYER_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_player_group_kv(ability_key, "key")
```

---

## has_kv_pair_role_res_key

method in GameAPI

- 描述

    判断是否存在ROLE_RES_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_role_res_key(kvbase, "key")
```

---

## has_unit_key_role_res_key_kv

method in GameAPI

- 描述

    判断单位编号是否存在ROLE_RES_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_role_res_key_kv(unit_key, "key")
```

---

## has_item_key_role_res_key_kv

method in GameAPI

- 描述

    判断物品编号是否存在ROLE_RES_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_role_res_key_kv(item_key, "key")
```

---

## has_ability_key_role_res_key_kv

method in GameAPI

- 描述

    判断技能编号是否存在ROLE_RES_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_role_res_key_kv(ability_key, "key")
```

---

## has_kv_pair_role_status

method in GameAPI

- 描述

    判断是否存在ROLE_STATUS键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_role_status(kvbase, "key")
```

---

## has_unit_key_role_status_kv

method in GameAPI

- 描述

    判断单位编号是否存在ROLE_STATUS键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_role_status_kv(unit_key, "key")
```

---

## has_item_key_role_status_kv

method in GameAPI

- 描述

    判断物品编号是否存在ROLE_STATUS键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_role_status_kv(item_key, "key")
```

---

## has_ability_key_role_status_kv

method in GameAPI

- 描述

    判断技能编号是否存在ROLE_STATUS键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_role_status_kv(ability_key, "key")
```

---

## has_kv_pair_role_type

method in GameAPI

- 描述

    判断是否存在ROLE_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_role_type(kvbase, "key")
```

---

## has_unit_key_role_type_kv

method in GameAPI

- 描述

    判断单位编号是否存在ROLE_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_role_type_kv(unit_key, "key")
```

---

## has_item_key_role_type_kv

method in GameAPI

- 描述

    判断物品编号是否存在ROLE_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_role_type_kv(item_key, "key")
```

---

## has_ability_key_role_type_kv

method in GameAPI

- 描述

    判断技能编号是否存在ROLE_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_role_type_kv(ability_key, "key")
```

---

## has_kv_pair_role_relation

method in GameAPI

- 描述

    判断是否存在ROLE_RELATION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_role_relation(kvbase, "key")
```

---

## has_unit_key_role_relation_kv

method in GameAPI

- 描述

    判断单位编号是否存在ROLE_RELATION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_role_relation_kv(unit_key, "key")
```

---

## has_item_key_role_relation_kv

method in GameAPI

- 描述

    判断物品编号是否存在ROLE_RELATION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_role_relation_kv(item_key, "key")
```

---

## has_ability_key_role_relation_kv

method in GameAPI

- 描述

    判断技能编号是否存在ROLE_RELATION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_role_relation_kv(ability_key, "key")
```

---

## has_kv_pair_team

method in GameAPI

- 描述

    判断是否存在TEAM键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_team(kvbase, "key")
```

---

## has_unit_key_team_kv

method in GameAPI

- 描述

    判断单位编号是否存在TEAM键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_team_kv(unit_key, "key")
```

---

## has_item_key_team_kv

method in GameAPI

- 描述

    判断物品编号是否存在TEAM键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_team_kv(item_key, "key")
```

---

## has_ability_key_team_kv

method in GameAPI

- 描述

    判断技能编号是否存在TEAM键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_team_kv(ability_key, "key")
```

---

## has_kv_pair_point

method in GameAPI

- 描述

    判断是否存在POINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_point(kvbase, "key")
```

---

## has_unit_key_point_kv

method in GameAPI

- 描述

    判断单位编号是否存在POINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_point_kv(unit_key, "key")
```

---

## has_item_key_point_kv

method in GameAPI

- 描述

    判断物品编号是否存在POINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_point_kv(item_key, "key")
```

---

## has_ability_key_point_kv

method in GameAPI

- 描述

    判断技能编号是否存在POINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_point_kv(ability_key, "key")
```

---

## has_kv_pair_vector3

method in GameAPI

- 描述

    判断是否存在VECTOR3键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_vector3(kvbase, "key")
```

---

## has_unit_key_vector3_kv

method in GameAPI

- 描述

    判断单位编号是否存在VECTOR3键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_vector3_kv(unit_key, "key")
```

---

## has_item_key_vector3_kv

method in GameAPI

- 描述

    判断物品编号是否存在VECTOR3键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_vector3_kv(item_key, "key")
```

---

## has_ability_key_vector3_kv

method in GameAPI

- 描述

    判断技能编号是否存在VECTOR3键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_vector3_kv(ability_key, "key")
```

---

## has_kv_pair_rotation

method in GameAPI

- 描述

    判断是否存在ROTATION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_rotation(kvbase, "key")
```

---

## has_unit_key_rotation_kv

method in GameAPI

- 描述

    判断单位编号是否存在ROTATION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_rotation_kv(unit_key, "key")
```

---

## has_item_key_rotation_kv

method in GameAPI

- 描述

    判断物品编号是否存在ROTATION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_rotation_kv(item_key, "key")
```

---

## has_ability_key_rotation_kv

method in GameAPI

- 描述

    判断技能编号是否存在ROTATION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_rotation_kv(ability_key, "key")
```

---

## has_kv_pair_point_list

method in GameAPI

- 描述

    判断是否存在POINT_LIST键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_point_list(kvbase, "key")
```

---

## has_unit_key_point_list_kv

method in GameAPI

- 描述

    判断单位编号是否存在POINT_LIST键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_point_list_kv(unit_key, "key")
```

---

## has_item_key_point_list_kv

method in GameAPI

- 描述

    判断物品编号是否存在POINT_LIST键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_point_list_kv(item_key, "key")
```

---

## has_ability_key_point_list_kv

method in GameAPI

- 描述

    判断技能编号是否存在POINT_LIST键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_point_list_kv(ability_key, "key")
```

---

## has_kv_pair_rectangle

method in GameAPI

- 描述

    判断是否存在RECTANGLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_rectangle(kvbase, "key")
```

---

## has_unit_key_rectangle_kv

method in GameAPI

- 描述

    判断单位编号是否存在RECTANGLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_rectangle_kv(unit_key, "key")
```

---

## has_item_key_rectangle_kv

method in GameAPI

- 描述

    判断物品编号是否存在RECTANGLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_rectangle_kv(item_key, "key")
```

---

## has_ability_key_rectangle_kv

method in GameAPI

- 描述

    判断技能编号是否存在RECTANGLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_rectangle_kv(ability_key, "key")
```

---

## has_kv_pair_round_area

method in GameAPI

- 描述

    判断是否存在ROUND_AREA键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_round_area(kvbase, "key")
```

---

## has_unit_key_round_area_kv

method in GameAPI

- 描述

    判断单位编号是否存在ROUND_AREA键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_round_area_kv(unit_key, "key")
```

---

## has_item_key_round_area_kv

method in GameAPI

- 描述

    判断物品编号是否存在ROUND_AREA键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_round_area_kv(item_key, "key")
```

---

## has_ability_key_round_area_kv

method in GameAPI

- 描述

    判断技能编号是否存在ROUND_AREA键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_round_area_kv(ability_key, "key")
```

---

## has_kv_pair_polygon

method in GameAPI

- 描述

    判断是否存在POLYGON键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_polygon(kvbase, "key")
```

---

## has_unit_key_polygon_kv

method in GameAPI

- 描述

    判断单位编号是否存在POLYGON键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_polygon_kv(unit_key, "key")
```

---

## has_item_key_polygon_kv

method in GameAPI

- 描述

    判断物品编号是否存在POLYGON键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_polygon_kv(item_key, "key")
```

---

## has_ability_key_polygon_kv

method in GameAPI

- 描述

    判断技能编号是否存在POLYGON键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_polygon_kv(ability_key, "key")
```

---

## has_kv_pair_camera

method in GameAPI

- 描述

    判断是否存在CAMERA键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_camera(kvbase, "key")
```

---

## has_unit_key_camera_kv

method in GameAPI

- 描述

    判断单位编号是否存在CAMERA键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_camera_kv(unit_key, "key")
```

---

## has_item_key_camera_kv

method in GameAPI

- 描述

    判断物品编号是否存在CAMERA键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_camera_kv(item_key, "key")
```

---

## has_ability_key_camera_kv

method in GameAPI

- 描述

    判断技能编号是否存在CAMERA键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_camera_kv(ability_key, "key")
```

---

## has_kv_pair_camline

method in GameAPI

- 描述

    判断是否存在CAMLINE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_camline(kvbase, "key")
```

---

## has_unit_key_camline_kv

method in GameAPI

- 描述

    判断单位编号是否存在CAMLINE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_camline_kv(unit_key, "key")
```

---

## has_item_key_camline_kv

method in GameAPI

- 描述

    判断物品编号是否存在CAMLINE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_camline_kv(item_key, "key")
```

---

## has_ability_key_camline_kv

method in GameAPI

- 描述

    判断技能编号是否存在CAMLINE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_camline_kv(ability_key, "key")
```

---

## has_kv_pair_point_light

method in GameAPI

- 描述

    判断是否存在POINT_LIGHT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_point_light(kvbase, "key")
```

---

## has_unit_key_point_light_kv

method in GameAPI

- 描述

    判断单位编号是否存在POINT_LIGHT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_point_light_kv(unit_key, "key")
```

---

## has_item_key_point_light_kv

method in GameAPI

- 描述

    判断物品编号是否存在POINT_LIGHT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_point_light_kv(item_key, "key")
```

---

## has_ability_key_point_light_kv

method in GameAPI

- 描述

    判断技能编号是否存在POINT_LIGHT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_point_light_kv(ability_key, "key")
```

---

## has_kv_pair_spot_light

method in GameAPI

- 描述

    判断是否存在SPOT_LIGHT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_spot_light(kvbase, "key")
```

---

## has_unit_key_spot_light_kv

method in GameAPI

- 描述

    判断单位编号是否存在SPOT_LIGHT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_spot_light_kv(unit_key, "key")
```

---

## has_item_key_spot_light_kv

method in GameAPI

- 描述

    判断物品编号是否存在SPOT_LIGHT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_spot_light_kv(item_key, "key")
```

---

## has_ability_key_spot_light_kv

method in GameAPI

- 描述

    判断技能编号是否存在SPOT_LIGHT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_spot_light_kv(ability_key, "key")
```

---

## has_kv_pair_fog

method in GameAPI

- 描述

    判断是否存在FOG键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_fog(kvbase, "key")
```

---

## has_unit_key_fog_kv

method in GameAPI

- 描述

    判断单位编号是否存在FOG键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_fog_kv(unit_key, "key")
```

---

## has_item_key_fog_kv

method in GameAPI

- 描述

    判断物品编号是否存在FOG键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_fog_kv(item_key, "key")
```

---

## has_ability_key_fog_kv

method in GameAPI

- 描述

    判断技能编号是否存在FOG键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_fog_kv(ability_key, "key")
```

---

## has_kv_pair_scene_sound

method in GameAPI

- 描述

    判断是否存在SCENE_SOUND键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_scene_sound(kvbase, "key")
```

---

## has_unit_key_scene_sound_kv

method in GameAPI

- 描述

    判断单位编号是否存在SCENE_SOUND键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_scene_sound_kv(unit_key, "key")
```

---

## has_item_key_scene_sound_kv

method in GameAPI

- 描述

    判断物品编号是否存在SCENE_SOUND键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_scene_sound_kv(item_key, "key")
```

---

## has_ability_key_scene_sound_kv

method in GameAPI

- 描述

    判断技能编号是否存在SCENE_SOUND键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_scene_sound_kv(ability_key, "key")
```

---

## has_kv_pair_model

method in GameAPI

- 描述

    判断是否存在MODEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_model(kvbase, "key")
```

---

## has_unit_key_model_kv

method in GameAPI

- 描述

    判断单位编号是否存在MODEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_model_kv(unit_key, "key")
```

---

## has_item_key_model_kv

method in GameAPI

- 描述

    判断物品编号是否存在MODEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_model_kv(item_key, "key")
```

---

## has_ability_key_model_kv

method in GameAPI

- 描述

    判断技能编号是否存在MODEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_model_kv(ability_key, "key")
```

---

## has_kv_pair_sfx_entity

method in GameAPI

- 描述

    判断是否存在SFX_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_sfx_entity(kvbase, "key")
```

---

## has_unit_key_sfx_entity_kv

method in GameAPI

- 描述

    判断单位编号是否存在SFX_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_sfx_entity_kv(unit_key, "key")
```

---

## has_item_key_sfx_entity_kv

method in GameAPI

- 描述

    判断物品编号是否存在SFX_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_sfx_entity_kv(item_key, "key")
```

---

## has_ability_key_sfx_entity_kv

method in GameAPI

- 描述

    判断技能编号是否存在SFX_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_sfx_entity_kv(ability_key, "key")
```

---

## has_kv_pair_sfx_key

method in GameAPI

- 描述

    判断是否存在SFX_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_sfx_key(kvbase, "key")
```

---

## has_unit_key_sfx_key_kv

method in GameAPI

- 描述

    判断单位编号是否存在SFX_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_sfx_key_kv(unit_key, "key")
```

---

## has_item_key_sfx_key_kv

method in GameAPI

- 描述

    判断物品编号是否存在SFX_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_sfx_key_kv(item_key, "key")
```

---

## has_ability_key_sfx_key_kv

method in GameAPI

- 描述

    判断技能编号是否存在SFX_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_sfx_key_kv(ability_key, "key")
```

---

## has_kv_pair_link_sfx_entity

method in GameAPI

- 描述

    判断是否存在LINK_SFX_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_link_sfx_entity(kvbase, "key")
```

---

## has_unit_key_link_sfx_entity_kv

method in GameAPI

- 描述

    判断单位编号是否存在LINK_SFX_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_link_sfx_entity_kv(unit_key, "key")
```

---

## has_item_key_link_sfx_entity_kv

method in GameAPI

- 描述

    判断物品编号是否存在LINK_SFX_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_link_sfx_entity_kv(item_key, "key")
```

---

## has_ability_key_link_sfx_entity_kv

method in GameAPI

- 描述

    判断技能编号是否存在LINK_SFX_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_link_sfx_entity_kv(ability_key, "key")
```

---

## has_kv_pair_link_sfx_key

method in GameAPI

- 描述

    判断是否存在LINK_SFX_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_link_sfx_key(kvbase, "key")
```

---

## has_unit_key_link_sfx_key_kv

method in GameAPI

- 描述

    判断单位编号是否存在LINK_SFX_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_link_sfx_key_kv(unit_key, "key")
```

---

## has_item_key_link_sfx_key_kv

method in GameAPI

- 描述

    判断物品编号是否存在LINK_SFX_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_link_sfx_key_kv(item_key, "key")
```

---

## has_ability_key_link_sfx_key_kv

method in GameAPI

- 描述

    判断技能编号是否存在LINK_SFX_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_link_sfx_key_kv(ability_key, "key")
```

---

## has_kv_pair_cursor_key

method in GameAPI

- 描述

    判断是否存在CURSOR_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_cursor_key(kvbase, "key")
```

---

## has_unit_key_cursor_key_kv

method in GameAPI

- 描述

    判断单位编号是否存在CURSOR_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_cursor_key_kv(unit_key, "key")
```

---

## has_item_key_cursor_key_kv

method in GameAPI

- 描述

    判断物品编号是否存在CURSOR_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_cursor_key_kv(item_key, "key")
```

---

## has_ability_key_cursor_key_kv

method in GameAPI

- 描述

    判断技能编号是否存在CURSOR_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_cursor_key_kv(ability_key, "key")
```

---

## has_kv_pair_angle

method in GameAPI

- 描述

    判断是否存在ANGLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_angle(kvbase, "key")
```

---

## has_unit_key_angle_kv

method in GameAPI

- 描述

    判断单位编号是否存在ANGLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_angle_kv(unit_key, "key")
```

---

## has_item_key_angle_kv

method in GameAPI

- 描述

    判断物品编号是否存在ANGLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_angle_kv(item_key, "key")
```

---

## has_ability_key_angle_kv

method in GameAPI

- 描述

    判断技能编号是否存在ANGLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_angle_kv(ability_key, "key")
```

---

## has_kv_pair_texture

method in GameAPI

- 描述

    判断是否存在TEXTURE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_texture(kvbase, "key")
```

---

## has_unit_key_texture_kv

method in GameAPI

- 描述

    判断单位编号是否存在TEXTURE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_texture_kv(unit_key, "key")
```

---

## has_item_key_texture_kv

method in GameAPI

- 描述

    判断物品编号是否存在TEXTURE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_texture_kv(item_key, "key")
```

---

## has_ability_key_texture_kv

method in GameAPI

- 描述

    判断技能编号是否存在TEXTURE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_texture_kv(ability_key, "key")
```

---

## has_kv_pair_sequence

method in GameAPI

- 描述

    判断是否存在SEQUENCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_sequence(kvbase, "key")
```

---

## has_unit_key_sequence_kv

method in GameAPI

- 描述

    判断单位编号是否存在SEQUENCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_sequence_kv(unit_key, "key")
```

---

## has_item_key_sequence_kv

method in GameAPI

- 描述

    判断物品编号是否存在SEQUENCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_sequence_kv(item_key, "key")
```

---

## has_ability_key_sequence_kv

method in GameAPI

- 描述

    判断技能编号是否存在SEQUENCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_sequence_kv(ability_key, "key")
```

---

## has_kv_pair_physics_object

method in GameAPI

- 描述

    判断是否存在PHYSICS_OBJECT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_physics_object(kvbase, "key")
```

---

## has_unit_key_physics_object_kv

method in GameAPI

- 描述

    判断单位编号是否存在PHYSICS_OBJECT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_physics_object_kv(unit_key, "key")
```

---

## has_item_key_physics_object_kv

method in GameAPI

- 描述

    判断物品编号是否存在PHYSICS_OBJECT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_physics_object_kv(item_key, "key")
```

---

## has_ability_key_physics_object_kv

method in GameAPI

- 描述

    判断技能编号是否存在PHYSICS_OBJECT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_physics_object_kv(ability_key, "key")
```

---

## has_kv_pair_physics_entity

method in GameAPI

- 描述

    判断是否存在PHYSICS_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_physics_entity(kvbase, "key")
```

---

## has_unit_key_physics_entity_kv

method in GameAPI

- 描述

    判断单位编号是否存在PHYSICS_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_physics_entity_kv(unit_key, "key")
```

---

## has_item_key_physics_entity_kv

method in GameAPI

- 描述

    判断物品编号是否存在PHYSICS_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_physics_entity_kv(item_key, "key")
```

---

## has_ability_key_physics_entity_kv

method in GameAPI

- 描述

    判断技能编号是否存在PHYSICS_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_physics_entity_kv(ability_key, "key")
```

---

## has_kv_pair_physics_object_key

method in GameAPI

- 描述

    判断是否存在PHYSICS_OBJECT_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_physics_object_key(kvbase, "key")
```

---

## has_unit_key_physics_object_key_kv

method in GameAPI

- 描述

    判断单位编号是否存在PHYSICS_OBJECT_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_physics_object_key_kv(unit_key, "key")
```

---

## has_item_key_physics_object_key_kv

method in GameAPI

- 描述

    判断物品编号是否存在PHYSICS_OBJECT_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_physics_object_key_kv(item_key, "key")
```

---

## has_ability_key_physics_object_key_kv

method in GameAPI

- 描述

    判断技能编号是否存在PHYSICS_OBJECT_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_physics_object_key_kv(ability_key, "key")
```

---

## has_kv_pair_physics_entity_key

method in GameAPI

- 描述

    判断是否存在PHYSICS_ENTITY_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_physics_entity_key(kvbase, "key")
```

---

## has_unit_key_physics_entity_key_kv

method in GameAPI

- 描述

    判断单位编号是否存在PHYSICS_ENTITY_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_physics_entity_key_kv(unit_key, "key")
```

---

## has_item_key_physics_entity_key_kv

method in GameAPI

- 描述

    判断物品编号是否存在PHYSICS_ENTITY_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_physics_entity_key_kv(item_key, "key")
```

---

## has_ability_key_physics_entity_key_kv

method in GameAPI

- 描述

    判断技能编号是否存在PHYSICS_ENTITY_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_physics_entity_key_kv(ability_key, "key")
```

---

## has_kv_pair_rigid_body

method in GameAPI

- 描述

    判断是否存在RIGID_BODY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_rigid_body(kvbase, "key")
```

---

## has_unit_key_rigid_body_kv

method in GameAPI

- 描述

    判断单位编号是否存在RIGID_BODY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_rigid_body_kv(unit_key, "key")
```

---

## has_item_key_rigid_body_kv

method in GameAPI

- 描述

    判断物品编号是否存在RIGID_BODY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_rigid_body_kv(item_key, "key")
```

---

## has_ability_key_rigid_body_kv

method in GameAPI

- 描述

    判断技能编号是否存在RIGID_BODY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_rigid_body_kv(ability_key, "key")
```

---

## has_kv_pair_rigid_body_group

method in GameAPI

- 描述

    判断是否存在RIGID_BODY_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_rigid_body_group(kvbase, "key")
```

---

## has_unit_key_rigid_body_group_kv

method in GameAPI

- 描述

    判断单位编号是否存在RIGID_BODY_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_rigid_body_group_kv(unit_key, "key")
```

---

## has_item_key_rigid_body_group_kv

method in GameAPI

- 描述

    判断物品编号是否存在RIGID_BODY_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_rigid_body_group_kv(item_key, "key")
```

---

## has_ability_key_rigid_body_group_kv

method in GameAPI

- 描述

    判断技能编号是否存在RIGID_BODY_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_rigid_body_group_kv(ability_key, "key")
```

---

## has_kv_pair_collider

method in GameAPI

- 描述

    判断是否存在COLLIDER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_collider(kvbase, "key")
```

---

## has_unit_key_collider_kv

method in GameAPI

- 描述

    判断单位编号是否存在COLLIDER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_collider_kv(unit_key, "key")
```

---

## has_item_key_collider_kv

method in GameAPI

- 描述

    判断物品编号是否存在COLLIDER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_collider_kv(item_key, "key")
```

---

## has_ability_key_collider_kv

method in GameAPI

- 描述

    判断技能编号是否存在COLLIDER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_collider_kv(ability_key, "key")
```

---

## has_kv_pair_joint

method in GameAPI

- 描述

    判断是否存在JOINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_joint(kvbase, "key")
```

---

## has_unit_key_joint_kv

method in GameAPI

- 描述

    判断单位编号是否存在JOINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_joint_kv(unit_key, "key")
```

---

## has_item_key_joint_kv

method in GameAPI

- 描述

    判断物品编号是否存在JOINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_joint_kv(item_key, "key")
```

---

## has_ability_key_joint_kv

method in GameAPI

- 描述

    判断技能编号是否存在JOINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_joint_kv(ability_key, "key")
```

---

## has_kv_pair_reaction

method in GameAPI

- 描述

    判断是否存在REACTION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_reaction(kvbase, "key")
```

---

## has_unit_key_reaction_kv

method in GameAPI

- 描述

    判断单位编号是否存在REACTION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_reaction_kv(unit_key, "key")
```

---

## has_item_key_reaction_kv

method in GameAPI

- 描述

    判断物品编号是否存在REACTION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_reaction_kv(item_key, "key")
```

---

## has_ability_key_reaction_kv

method in GameAPI

- 描述

    判断技能编号是否存在REACTION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_reaction_kv(ability_key, "key")
```

---

## has_kv_pair_reaction_group

method in GameAPI

- 描述

    判断是否存在REACTION_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_reaction_group(kvbase, "key")
```

---

## has_unit_key_reaction_group_kv

method in GameAPI

- 描述

    判断单位编号是否存在REACTION_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_reaction_group_kv(unit_key, "key")
```

---

## has_item_key_reaction_group_kv

method in GameAPI

- 描述

    判断物品编号是否存在REACTION_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_reaction_group_kv(item_key, "key")
```

---

## has_ability_key_reaction_group_kv

method in GameAPI

- 描述

    判断技能编号是否存在REACTION_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_reaction_group_kv(ability_key, "key")
```

---

## has_kv_pair_dynamic_trigger_instance

method in GameAPI

- 描述

    判断是否存在DYNAMIC_TRIGGER_INSTANCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_dynamic_trigger_instance(kvbase, "key")
```

---

## has_unit_key_dynamic_trigger_instance_kv

method in GameAPI

- 描述

    判断单位编号是否存在DYNAMIC_TRIGGER_INSTANCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_dynamic_trigger_instance_kv(unit_key, "key")
```

---

## has_item_key_dynamic_trigger_instance_kv

method in GameAPI

- 描述

    判断物品编号是否存在DYNAMIC_TRIGGER_INSTANCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_dynamic_trigger_instance_kv(item_key, "key")
```

---

## has_ability_key_dynamic_trigger_instance_kv

method in GameAPI

- 描述

    判断技能编号是否存在DYNAMIC_TRIGGER_INSTANCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_dynamic_trigger_instance_kv(ability_key, "key")
```

---

## has_kv_pair_table

method in GameAPI

- 描述

    判断是否存在TABLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_table(kvbase, "key")
```

---

## has_unit_key_table_kv

method in GameAPI

- 描述

    判断单位编号是否存在TABLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_table_kv(unit_key, "key")
```

---

## has_item_key_table_kv

method in GameAPI

- 描述

    判断物品编号是否存在TABLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_table_kv(item_key, "key")
```

---

## has_ability_key_table_kv

method in GameAPI

- 描述

    判断技能编号是否存在TABLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_table_kv(ability_key, "key")
```

---

## has_kv_pair_random_pool

method in GameAPI

- 描述

    判断是否存在RANDOM_POOL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_random_pool(kvbase, "key")
```

---

## has_unit_key_random_pool_kv

method in GameAPI

- 描述

    判断单位编号是否存在RANDOM_POOL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_random_pool_kv(unit_key, "key")
```

---

## has_item_key_random_pool_kv

method in GameAPI

- 描述

    判断物品编号是否存在RANDOM_POOL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_random_pool_kv(item_key, "key")
```

---

## has_ability_key_random_pool_kv

method in GameAPI

- 描述

    判断技能编号是否存在RANDOM_POOL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_random_pool_kv(ability_key, "key")
```

---

## has_kv_pair_scene_ui

method in GameAPI

- 描述

    判断是否存在SCENE_UI键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_scene_ui(kvbase, "key")
```

---

## has_unit_key_scene_ui_kv

method in GameAPI

- 描述

    判断单位编号是否存在SCENE_UI键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_scene_ui_kv(unit_key, "key")
```

---

## has_item_key_scene_ui_kv

method in GameAPI

- 描述

    判断物品编号是否存在SCENE_UI键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_scene_ui_kv(item_key, "key")
```

---

## has_ability_key_scene_ui_kv

method in GameAPI

- 描述

    判断技能编号是否存在SCENE_UI键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_scene_ui_kv(ability_key, "key")
```

---

## has_kv_pair_damage_type

method in GameAPI

- 描述

    判断是否存在DAMAGE_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_damage_type(kvbase, "key")
```

---

## has_unit_key_damage_type_kv

method in GameAPI

- 描述

    判断单位编号是否存在DAMAGE_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_damage_type_kv(unit_key, "key")
```

---

## has_item_key_damage_type_kv

method in GameAPI

- 描述

    判断物品编号是否存在DAMAGE_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_damage_type_kv(item_key, "key")
```

---

## has_ability_key_damage_type_kv

method in GameAPI

- 描述

    判断技能编号是否存在DAMAGE_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_damage_type_kv(ability_key, "key")
```

---

## has_kv_pair_harm_text_type_new

method in GameAPI

- 描述

    判断是否存在HARM_TEXT_TYPE_NEW键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_harm_text_type_new(kvbase, "key")
```

---

## has_unit_key_harm_text_type_new_kv

method in GameAPI

- 描述

    判断单位编号是否存在HARM_TEXT_TYPE_NEW键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_harm_text_type_new_kv(unit_key, "key")
```

---

## has_item_key_harm_text_type_new_kv

method in GameAPI

- 描述

    判断物品编号是否存在HARM_TEXT_TYPE_NEW键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_harm_text_type_new_kv(item_key, "key")
```

---

## has_ability_key_harm_text_type_new_kv

method in GameAPI

- 描述

    判断技能编号是否存在HARM_TEXT_TYPE_NEW键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_harm_text_type_new_kv(ability_key, "key")
```

---

## has_kv_pair_font_type

method in GameAPI

- 描述

    判断是否存在FONT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_font_type(kvbase, "key")
```

---

## has_unit_key_font_type_kv

method in GameAPI

- 描述

    判断单位编号是否存在FONT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_font_type_kv(unit_key, "key")
```

---

## has_item_key_font_type_kv

method in GameAPI

- 描述

    判断物品编号是否存在FONT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_font_type_kv(item_key, "key")
```

---

## has_ability_key_font_type_kv

method in GameAPI

- 描述

    判断技能编号是否存在FONT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_font_type_kv(ability_key, "key")
```

---

## has_kv_pair_jump_word_track

method in GameAPI

- 描述

    判断是否存在JUMP_WORD_TRACK键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_jump_word_track(kvbase, "key")
```

---

## has_unit_key_jump_word_track_kv

method in GameAPI

- 描述

    判断单位编号是否存在JUMP_WORD_TRACK键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_jump_word_track_kv(unit_key, "key")
```

---

## has_item_key_jump_word_track_kv

method in GameAPI

- 描述

    判断物品编号是否存在JUMP_WORD_TRACK键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_jump_word_track_kv(item_key, "key")
```

---

## has_ability_key_jump_word_track_kv

method in GameAPI

- 描述

    判断技能编号是否存在JUMP_WORD_TRACK键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_jump_word_track_kv(ability_key, "key")
```

---

## has_kv_pair_new_timer

method in GameAPI

- 描述

    判断是否存在NEW_TIMER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_new_timer(kvbase, "key")
```

---

## has_unit_key_new_timer_kv

method in GameAPI

- 描述

    判断单位编号是否存在NEW_TIMER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_new_timer_kv(unit_key, "key")
```

---

## has_item_key_new_timer_kv

method in GameAPI

- 描述

    判断物品编号是否存在NEW_TIMER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_new_timer_kv(item_key, "key")
```

---

## has_ability_key_new_timer_kv

method in GameAPI

- 描述

    判断技能编号是否存在NEW_TIMER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_new_timer_kv(ability_key, "key")
```

---

## has_kv_pair_tech_key

method in GameAPI

- 描述

    判断是否存在TECH_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_tech_key(kvbase, "key")
```

---

## has_unit_key_tech_key_kv

method in GameAPI

- 描述

    判断单位编号是否存在TECH_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_tech_key_kv(unit_key, "key")
```

---

## has_item_key_tech_key_kv

method in GameAPI

- 描述

    判断物品编号是否存在TECH_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_tech_key_kv(item_key, "key")
```

---

## has_ability_key_tech_key_kv

method in GameAPI

- 描述

    判断技能编号是否存在TECH_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_tech_key_kv(ability_key, "key")
```

---

## has_kv_pair_store_key

method in GameAPI

- 描述

    判断是否存在STORE_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_store_key(kvbase, "key")
```

---

## has_unit_key_store_key_kv

method in GameAPI

- 描述

    判断单位编号是否存在STORE_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_store_key_kv(unit_key, "key")
```

---

## has_item_key_store_key_kv

method in GameAPI

- 描述

    判断物品编号是否存在STORE_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_store_key_kv(item_key, "key")
```

---

## has_ability_key_store_key_kv

method in GameAPI

- 描述

    判断技能编号是否存在STORE_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_store_key_kv(ability_key, "key")
```

---

## has_kv_pair_keyboard_key

method in GameAPI

- 描述

    判断是否存在KEYBOARD_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_keyboard_key(kvbase, "key")
```

---

## has_unit_key_keyboard_key_kv

method in GameAPI

- 描述

    判断单位编号是否存在KEYBOARD_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_keyboard_key_kv(unit_key, "key")
```

---

## has_item_key_keyboard_key_kv

method in GameAPI

- 描述

    判断物品编号是否存在KEYBOARD_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_keyboard_key_kv(item_key, "key")
```

---

## has_ability_key_keyboard_key_kv

method in GameAPI

- 描述

    判断技能编号是否存在KEYBOARD_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_keyboard_key_kv(ability_key, "key")
```

---

## has_kv_pair_func_keyboard_key

method in GameAPI

- 描述

    判断是否存在FUNC_KEYBOARD_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_func_keyboard_key(kvbase, "key")
```

---

## has_unit_key_func_keyboard_key_kv

method in GameAPI

- 描述

    判断单位编号是否存在FUNC_KEYBOARD_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_func_keyboard_key_kv(unit_key, "key")
```

---

## has_item_key_func_keyboard_key_kv

method in GameAPI

- 描述

    判断物品编号是否存在FUNC_KEYBOARD_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_func_keyboard_key_kv(item_key, "key")
```

---

## has_ability_key_func_keyboard_key_kv

method in GameAPI

- 描述

    判断技能编号是否存在FUNC_KEYBOARD_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_func_keyboard_key_kv(ability_key, "key")
```

---

## has_kv_pair_mouse_key

method in GameAPI

- 描述

    判断是否存在MOUSE_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_mouse_key(kvbase, "key")
```

---

## has_unit_key_mouse_key_kv

method in GameAPI

- 描述

    判断单位编号是否存在MOUSE_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_mouse_key_kv(unit_key, "key")
```

---

## has_item_key_mouse_key_kv

method in GameAPI

- 描述

    判断物品编号是否存在MOUSE_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_mouse_key_kv(item_key, "key")
```

---

## has_ability_key_mouse_key_kv

method in GameAPI

- 描述

    判断技能编号是否存在MOUSE_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_mouse_key_kv(ability_key, "key")
```

---

## has_kv_pair_mouse_wheel

method in GameAPI

- 描述

    判断是否存在MOUSE_WHEEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_mouse_wheel(kvbase, "key")
```

---

## has_unit_key_mouse_wheel_kv

method in GameAPI

- 描述

    判断单位编号是否存在MOUSE_WHEEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_mouse_wheel_kv(unit_key, "key")
```

---

## has_item_key_mouse_wheel_kv

method in GameAPI

- 描述

    判断物品编号是否存在MOUSE_WHEEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_mouse_wheel_kv(item_key, "key")
```

---

## has_ability_key_mouse_wheel_kv

method in GameAPI

- 描述

    判断技能编号是否存在MOUSE_WHEEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_mouse_wheel_kv(ability_key, "key")
```

---

## has_kv_pair_post_effect

method in GameAPI

- 描述

    判断是否存在POST_EFFECT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_post_effect(kvbase, "key")
```

---

## has_unit_key_post_effect_kv

method in GameAPI

- 描述

    判断单位编号是否存在POST_EFFECT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_post_effect_kv(unit_key, "key")
```

---

## has_item_key_post_effect_kv

method in GameAPI

- 描述

    判断物品编号是否存在POST_EFFECT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_post_effect_kv(item_key, "key")
```

---

## has_ability_key_post_effect_kv

method in GameAPI

- 描述

    判断技能编号是否存在POST_EFFECT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_post_effect_kv(ability_key, "key")
```

---

## has_kv_pair_unit_type

method in GameAPI

- 描述

    判断是否存在UNIT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_unit_type(kvbase, "key")
```

---

## has_unit_key_unit_type_kv

method in GameAPI

- 描述

    判断单位编号是否存在UNIT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_unit_type_kv(unit_key, "key")
```

---

## has_item_key_unit_type_kv

method in GameAPI

- 描述

    判断物品编号是否存在UNIT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_unit_type_kv(item_key, "key")
```

---

## has_ability_key_unit_type_kv

method in GameAPI

- 描述

    判断技能编号是否存在UNIT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_unit_type_kv(ability_key, "key")
```

---

## has_kv_pair_unit_command_type

method in GameAPI

- 描述

    判断是否存在UNIT_COMMAND_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_unit_command_type(kvbase, "key")
```

---

## has_unit_key_unit_command_type_kv

method in GameAPI

- 描述

    判断单位编号是否存在UNIT_COMMAND_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_unit_command_type_kv(unit_key, "key")
```

---

## has_item_key_unit_command_type_kv

method in GameAPI

- 描述

    判断物品编号是否存在UNIT_COMMAND_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_unit_command_type_kv(item_key, "key")
```

---

## has_ability_key_unit_command_type_kv

method in GameAPI

- 描述

    判断技能编号是否存在UNIT_COMMAND_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_unit_command_type_kv(ability_key, "key")
```

---

## has_kv_pair_mini_map_color_type

method in GameAPI

- 描述

    判断是否存在MINI_MAP_COLOR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_mini_map_color_type(kvbase, "key")
```

---

## has_unit_key_mini_map_color_type_kv

method in GameAPI

- 描述

    判断单位编号是否存在MINI_MAP_COLOR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_mini_map_color_type_kv(unit_key, "key")
```

---

## has_item_key_mini_map_color_type_kv

method in GameAPI

- 描述

    判断物品编号是否存在MINI_MAP_COLOR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_mini_map_color_type_kv(item_key, "key")
```

---

## has_ability_key_mini_map_color_type_kv

method in GameAPI

- 描述

    判断技能编号是否存在MINI_MAP_COLOR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_mini_map_color_type_kv(ability_key, "key")
```

---

## has_kv_pair_unit_behavior

method in GameAPI

- 描述

    判断是否存在UNIT_BEHAVIOR键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_unit_behavior(kvbase, "key")
```

---

## has_unit_key_unit_behavior_kv

method in GameAPI

- 描述

    判断单位编号是否存在UNIT_BEHAVIOR键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_unit_behavior_kv(unit_key, "key")
```

---

## has_item_key_unit_behavior_kv

method in GameAPI

- 描述

    判断物品编号是否存在UNIT_BEHAVIOR键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_unit_behavior_kv(item_key, "key")
```

---

## has_ability_key_unit_behavior_kv

method in GameAPI

- 描述

    判断技能编号是否存在UNIT_BEHAVIOR键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_unit_behavior_kv(ability_key, "key")
```

---

## has_kv_pair_curved_path

method in GameAPI

- 描述

    判断是否存在CURVED_PATH键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_curved_path(kvbase, "key")
```

---

## has_unit_key_curved_path_kv

method in GameAPI

- 描述

    判断单位编号是否存在CURVED_PATH键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_curved_path_kv(unit_key, "key")
```

---

## has_item_key_curved_path_kv

method in GameAPI

- 描述

    判断物品编号是否存在CURVED_PATH键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_curved_path_kv(item_key, "key")
```

---

## has_ability_key_curved_path_kv

method in GameAPI

- 描述

    判断技能编号是否存在CURVED_PATH键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_curved_path_kv(ability_key, "key")
```

---

## has_kv_pair_curved_path_3d

method in GameAPI

- 描述

    判断是否存在CURVED_PATH_3D键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_curved_path_3d(kvbase, "key")
```

---

## has_unit_key_curved_path_3d_kv

method in GameAPI

- 描述

    判断单位编号是否存在CURVED_PATH_3D键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_curved_path_3d_kv(unit_key, "key")
```

---

## has_item_key_curved_path_3d_kv

method in GameAPI

- 描述

    判断物品编号是否存在CURVED_PATH_3D键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_curved_path_3d_kv(item_key, "key")
```

---

## has_ability_key_curved_path_3d_kv

method in GameAPI

- 描述

    判断技能编号是否存在CURVED_PATH_3D键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_curved_path_3d_kv(ability_key, "key")
```

---

## get_kv_pair_value_boolean

method in GameAPI

- 描述

    获取BOOLEAN键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_boolean(kvbase, "key")
```

---

## get_kv_pair_value_integer

method in GameAPI

- 描述

    获取INTEGER键值对

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

local result = GameAPI.get_kv_pair_value_integer(kvbase, "key")
```

---

## get_kv_pair_value_float

method in GameAPI

- 描述

    获取FLOAT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_float(kvbase, "key")
```

---

## get_kv_pair_value_string

method in GameAPI

- 描述

    获取STRING键值对

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

local result = GameAPI.get_kv_pair_value_string(kvbase, "key")
```

---

## get_kv_pair_value_ui_comp

method in GameAPI

- 描述

    获取UI_COMP键值对

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

local result = GameAPI.get_kv_pair_value_ui_comp(kvbase, "key")
```

---

## get_kv_pair_value_ui_comp_type

method in GameAPI

- 描述

    获取UI_COMP_TYPE键值对

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

local result = GameAPI.get_kv_pair_value_ui_comp_type(kvbase, "key")
```

---

## get_kv_pair_value_ui_comp_event_type

method in GameAPI

- 描述

    获取UI_COMP_EVENT_TYPE键值对

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

local result = GameAPI.get_kv_pair_value_ui_comp_event_type(kvbase, "key")
```

---

## get_kv_pair_value_ui_comp_attr

method in GameAPI

- 描述

    获取UI_COMP_ATTR键值对

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

local result = GameAPI.get_kv_pair_value_ui_comp_attr(kvbase, "key")
```

---

## get_kv_pair_value_ui_comp_align_type

method in GameAPI

- 描述

    获取UI_COMP_ALIGN_TYPE键值对

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

local result = GameAPI.get_kv_pair_value_ui_comp_align_type(kvbase, "key")
```

---

## get_kv_pair_value_ui_prefab

method in GameAPI

- 描述

    获取UI_PREFAB键值对

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

local result = GameAPI.get_kv_pair_value_ui_prefab(kvbase, "key")
```

---

## get_kv_pair_value_ui_prefab_instance

method in GameAPI

- 描述

    获取UI_PREFAB_INSTANCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UIPrefabIns | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_ui_prefab_instance(kvbase, "key")
```

---

## get_kv_pair_value_ui_prefab_ins_uid

method in GameAPI

- 描述

    获取UI_PREFAB_INS_UID键值对

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

local result = GameAPI.get_kv_pair_value_ui_prefab_ins_uid(kvbase, "key")
```

---

## get_kv_pair_value_ui_direction

method in GameAPI

- 描述

    获取UI_DIRECTION键值对

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

local result = GameAPI.get_kv_pair_value_ui_direction(kvbase, "key")
```

---

## get_kv_pair_value_ui_model_camera_mod

method in GameAPI

- 描述

    获取UI_MODEL_CAMERA_MOD键值对

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

local result = GameAPI.get_kv_pair_value_ui_model_camera_mod(kvbase, "key")
```

---

## get_kv_pair_value_ui_btn_status

method in GameAPI

- 描述

    获取UI_BTN_STATUS键值对

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

local result = GameAPI.get_kv_pair_value_ui_btn_status(kvbase, "key")
```

---

## get_kv_pair_value_ui_scrollview_type

method in GameAPI

- 描述

    获取UI_SCROLLVIEW_TYPE键值对

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

local result = GameAPI.get_kv_pair_value_ui_scrollview_type(kvbase, "key")
```

---

## get_kv_pair_value_ui_anim

method in GameAPI

- 描述

    获取UI_ANIM键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UIAnimKey | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_ui_anim(kvbase, "key")
```

---

## get_kv_pair_value_ui_anim_curve

method in GameAPI

- 描述

    获取UI_ANIM_CURVE键值对

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

local result = GameAPI.get_kv_pair_value_ui_anim_curve(kvbase, "key")
```

---

## get_kv_pair_value_audio_channel

method in GameAPI

- 描述

    获取AUDIO_CHANNEL键值对

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

local result = GameAPI.get_kv_pair_value_audio_channel(kvbase, "key")
```

---

## get_kv_pair_value_unit_entity

method in GameAPI

- 描述

    获取UNIT_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_unit_entity(kvbase, "key")
```

---

## get_kv_pair_value_unit_group

method in GameAPI

- 描述

    获取UNIT_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitGroup | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_unit_group(kvbase, "key")
```

---

## get_kv_pair_value_unit_name

method in GameAPI

- 描述

    获取UNIT_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitKey | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_unit_name(kvbase, "key")
```

---

## get_kv_pair_value_unit_name_pool

method in GameAPI

- 描述

    获取UNIT_NAME_POOL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitKeyPool | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_unit_name_pool(kvbase, "key")
```

---

## get_kv_pair_value_unit_write_attribute

method in GameAPI

- 描述

    获取UNIT_WRITE_ATTRIBUTE键值对

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

local result = GameAPI.get_kv_pair_value_unit_write_attribute(kvbase, "key")
```

---

## get_kv_pair_value_attr_element

method in GameAPI

- 描述

    获取ATTR_ELEMENT键值对

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

local result = GameAPI.get_kv_pair_value_attr_element(kvbase, "key")
```

---

## get_kv_pair_value_attr_element_read

method in GameAPI

- 描述

    获取ATTR_ELEMENT_READ键值对

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

local result = GameAPI.get_kv_pair_value_attr_element_read(kvbase, "key")
```

---

## get_kv_pair_value_mover_entity

method in GameAPI

- 描述

    获取MOVER_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Mover | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_mover_entity(kvbase, "key")
```

---

## get_kv_pair_value_image_quality

method in GameAPI

- 描述

    获取IMAGE_QUALITY键值对

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

local result = GameAPI.get_kv_pair_value_image_quality(kvbase, "key")
```

---

## get_kv_pair_value_window_type_setting

method in GameAPI

- 描述

    获取WINDOW_TYPE_SETTING键值对

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

local result = GameAPI.get_kv_pair_value_window_type_setting(kvbase, "key")
```

---

## get_kv_pair_value_item_entity

method in GameAPI

- 描述

    获取ITEM_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Item | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_item_entity(kvbase, "key")
```

---

## get_kv_pair_value_item_group

method in GameAPI

- 描述

    获取ITEM_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemGroup | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_item_group(kvbase, "key")
```

---

## get_kv_pair_value_item_name

method in GameAPI

- 描述

    获取ITEM_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemKey | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_item_name(kvbase, "key")
```

---

## get_kv_pair_value_ability

method in GameAPI

- 描述

    获取ABILITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Ability | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_ability(kvbase, "key")
```

---

## get_kv_pair_value_ability_type

method in GameAPI

- 描述

    获取ABILITY_TYPE键值对

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

local result = GameAPI.get_kv_pair_value_ability_type(kvbase, "key")
```

---

## get_kv_pair_value_ability_cast_type

method in GameAPI

- 描述

    获取ABILITY_CAST_TYPE键值对

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

local result = GameAPI.get_kv_pair_value_ability_cast_type(kvbase, "key")
```

---

## get_kv_pair_value_ability_name

method in GameAPI

- 描述

    获取ABILITY_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityKey | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_ability_name(kvbase, "key")
```

---

## get_kv_pair_value_skill_pointer_type

method in GameAPI

- 描述

    获取SKILL_POINTER_TYPE键值对

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

local result = GameAPI.get_kv_pair_value_skill_pointer_type(kvbase, "key")
```

---

## get_kv_pair_value_modifier_entity

method in GameAPI

- 描述

    获取MODIFIER_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierEntity | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_modifier_entity(kvbase, "key")
```

---

## get_kv_pair_value_modifier_type

method in GameAPI

- 描述

    获取MODIFIER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierType | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_modifier_type(kvbase, "key")
```

---

## get_kv_pair_value_modifier_effect_type

method in GameAPI

- 描述

    获取MODIFIER_EFFECT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierEffectType | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_modifier_effect_type(kvbase, "key")
```

---

## get_kv_pair_value_modifier

method in GameAPI

- 描述

    获取MODIFIER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierKey | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_modifier(kvbase, "key")
```

---

## get_kv_pair_value_projectile

method in GameAPI

- 描述

    获取PROJECTILE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileKey | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_projectile(kvbase, "key")
```

---

## get_kv_pair_value_projectile_entity

method in GameAPI

- 描述

    获取PROJECTILE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileEntity | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_projectile_entity(kvbase, "key")
```

---

## get_kv_pair_value_projectile_group

method in GameAPI

- 描述

    获取PROJECTILE_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileGroup | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_projectile_group(kvbase, "key")
```

---

## get_kv_pair_value_destructible_entity

method in GameAPI

- 描述

    获取DESTRUCTIBLE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Destructible | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_destructible_entity(kvbase, "key")
```

---

## get_kv_pair_value_destructible_name

method in GameAPI

- 描述

    获取DESTRUCTIBLE_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DestructibleKey | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_destructible_name(kvbase, "key")
```

---

## get_kv_pair_value_sound_entity

method in GameAPI

- 描述

    获取SOUND_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SoundEntity | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_sound_entity(kvbase, "key")
```

---

## get_kv_pair_value_audio_key

method in GameAPI

- 描述

    获取AUDIO_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AudioKey | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_audio_key(kvbase, "key")
```

---

## get_kv_pair_value_game_mode

method in GameAPI

- 描述

    获取GAME_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.GameMode | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_game_mode(kvbase, "key")
```

---

## get_kv_pair_value_player

method in GameAPI

- 描述

    获取PLAYER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Role | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_player(kvbase, "key")
```

---

## get_kv_pair_value_player_group

method in GameAPI

- 描述

    获取PLAYER_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleGroup | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_player_group(kvbase, "key")
```

---

## get_kv_pair_value_role_res_key

method in GameAPI

- 描述

    获取ROLE_RES_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleResKey | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_role_res_key(kvbase, "key")
```

---

## get_kv_pair_value_role_status

method in GameAPI

- 描述

    获取ROLE_STATUS键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleStatus | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_role_status(kvbase, "key")
```

---

## get_kv_pair_value_role_type

method in GameAPI

- 描述

    获取ROLE_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleType | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_role_type(kvbase, "key")
```

---

## get_kv_pair_value_role_relation

method in GameAPI

- 描述

    获取ROLE_RELATION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleRelation | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_role_relation(kvbase, "key")
```

---

## get_kv_pair_value_team

method in GameAPI

- 描述

    获取TEAM键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Camp | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_team(kvbase, "key")
```

---

## get_kv_pair_value_point

method in GameAPI

- 描述

    获取POINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FPoint | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_point(kvbase, "key")
```

---

## get_kv_pair_value_vector3

method in GameAPI

- 描述

    获取VECTOR3键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3 | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_vector3(kvbase, "key")
```

---

## get_kv_pair_value_rotation

method in GameAPI

- 描述

    获取ROTATION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FRotation | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_rotation(kvbase, "key")
```

---

## get_kv_pair_value_point_list

method in GameAPI

- 描述

    获取POINT_LIST键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Road | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_point_list(kvbase, "key")
```

---

## get_kv_pair_value_rectangle

method in GameAPI

- 描述

    获取RECTANGLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RecArea | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_rectangle(kvbase, "key")
```

---

## get_kv_pair_value_round_area

method in GameAPI

- 描述

    获取ROUND_AREA键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CirArea | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_round_area(kvbase, "key")
```

---

## get_kv_pair_value_polygon

method in GameAPI

- 描述

    获取POLYGON键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PolyArea | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_polygon(kvbase, "key")
```

---

## get_kv_pair_value_camera

method in GameAPI

- 描述

    获取CAMERA键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Camera | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_camera(kvbase, "key")
```

---

## get_kv_pair_value_camline

method in GameAPI

- 描述

    获取CAMLINE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CamlineID | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_camline(kvbase, "key")
```

---

## get_kv_pair_value_point_light

method in GameAPI

- 描述

    获取POINT_LIGHT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PointLight | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_point_light(kvbase, "key")
```

---

## get_kv_pair_value_spot_light

method in GameAPI

- 描述

    获取SPOT_LIGHT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SpotLight | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_spot_light(kvbase, "key")
```

---

## get_kv_pair_value_fog

method in GameAPI

- 描述

    获取FOG键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fog | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_fog(kvbase, "key")
```

---

## get_kv_pair_value_scene_sound

method in GameAPI

- 描述

    获取SCENE_SOUND键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SceneSound | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_scene_sound(kvbase, "key")
```

---

## get_kv_pair_value_model

method in GameAPI

- 描述

    获取MODEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModelKey | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_model(kvbase, "key")
```

---

## get_kv_pair_value_sfx_entity

method in GameAPI

- 描述

    获取SFX_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sfx | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_sfx_entity(kvbase, "key")
```

---

## get_kv_pair_value_sfx_key

method in GameAPI

- 描述

    获取SFX_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SfxKey | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_sfx_key(kvbase, "key")
```

---

## get_kv_pair_value_link_sfx_entity

method in GameAPI

- 描述

    获取LINK_SFX_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LinkSfx | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_link_sfx_entity(kvbase, "key")
```

---

## get_kv_pair_value_link_sfx_key

method in GameAPI

- 描述

    获取LINK_SFX_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LinkSfxKey | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_link_sfx_key(kvbase, "key")
```

---

## get_kv_pair_value_cursor_key

method in GameAPI

- 描述

    获取CURSOR_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CursorKey | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_cursor_key(kvbase, "key")
```

---

## get_kv_pair_value_angle

method in GameAPI

- 描述

    获取ANGLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_angle(kvbase, "key")
```

---

## get_kv_pair_value_texture

method in GameAPI

- 描述

    获取TEXTURE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Texture | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_texture(kvbase, "key")
```

---

## get_kv_pair_value_sequence

method in GameAPI

- 描述

    获取SEQUENCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sequence | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_sequence(kvbase, "key")
```

---

## get_kv_pair_value_physics_object

method in GameAPI

- 描述

    获取PHYSICS_OBJECT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsObject | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_physics_object(kvbase, "key")
```

---

## get_kv_pair_value_physics_entity

method in GameAPI

- 描述

    获取PHYSICS_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsEntity | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_physics_entity(kvbase, "key")
```

---

## get_kv_pair_value_physics_object_key

method in GameAPI

- 描述

    获取PHYSICS_OBJECT_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsObjectKey | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_physics_object_key(kvbase, "key")
```

---

## get_kv_pair_value_physics_entity_key

method in GameAPI

- 描述

    获取PHYSICS_ENTITY_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsEntityKey | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_physics_entity_key(kvbase, "key")
```

---

## get_kv_pair_value_rigid_body

method in GameAPI

- 描述

    获取RIGID_BODY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RigidBody | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_rigid_body(kvbase, "key")
```

---

## get_kv_pair_value_rigid_body_group

method in GameAPI

- 描述

    获取RIGID_BODY_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RigidBodyGroup | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_rigid_body_group(kvbase, "key")
```

---

## get_kv_pair_value_collider

method in GameAPI

- 描述

    获取COLLIDER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Collider | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_collider(kvbase, "key")
```

---

## get_kv_pair_value_joint

method in GameAPI

- 描述

    获取JOINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Joint | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_joint(kvbase, "key")
```

---

## get_kv_pair_value_reaction

method in GameAPI

- 描述

    获取REACTION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Reaction | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_reaction(kvbase, "key")
```

---

## get_kv_pair_value_reaction_group

method in GameAPI

- 描述

    获取REACTION_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ReactionGroup | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_reaction_group(kvbase, "key")
```

---

## get_kv_pair_value_dynamic_trigger_instance

method in GameAPI

- 描述

    获取DYNAMIC_TRIGGER_INSTANCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DynamicTriggerInstance | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_dynamic_trigger_instance(kvbase, "key")
```

---

## get_kv_pair_value_table

method in GameAPI

- 描述

    获取TABLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Table | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_table(kvbase, "key")
```

---

## get_kv_pair_value_random_pool

method in GameAPI

- 描述

    获取RANDOM_POOL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RandomPool | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_random_pool(kvbase, "key")
```

---

## get_kv_pair_value_scene_ui

method in GameAPI

- 描述

    获取SCENE_UI键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SceneNode | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_scene_ui(kvbase, "key")
```

---

## get_kv_pair_value_damage_type

method in GameAPI

- 描述

    获取DAMAGE_TYPE键值对

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

local result = GameAPI.get_kv_pair_value_damage_type(kvbase, "key")
```

---

## get_kv_pair_value_harm_text_type_new

method in GameAPI

- 描述

    获取HARM_TEXT_TYPE_NEW键值对

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

local result = GameAPI.get_kv_pair_value_harm_text_type_new(kvbase, "key")
```

---

## get_kv_pair_value_font_type

method in GameAPI

- 描述

    获取FONT_TYPE键值对

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

local result = GameAPI.get_kv_pair_value_font_type(kvbase, "key")
```

---

## get_kv_pair_value_jump_word_track

method in GameAPI

- 描述

    获取JUMP_WORD_TRACK键值对

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

local result = GameAPI.get_kv_pair_value_jump_word_track(kvbase, "key")
```

---

## get_kv_pair_value_new_timer

method in GameAPI

- 描述

    获取NEW_TIMER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Timer | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_new_timer(kvbase, "key")
```

---

## get_kv_pair_value_tech_key

method in GameAPI

- 描述

    获取TECH_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.TechKey | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_tech_key(kvbase, "key")
```

---

## get_kv_pair_value_store_key

method in GameAPI

- 描述

    获取STORE_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.StoreKey | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_store_key(kvbase, "key")
```

---

## get_kv_pair_value_keyboard_key

method in GameAPI

- 描述

    获取KEYBOARD_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.KeyboardKey | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_keyboard_key(kvbase, "key")
```

---

## get_kv_pair_value_func_keyboard_key

method in GameAPI

- 描述

    获取FUNC_KEYBOARD_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FuncKeyboardKey | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_func_keyboard_key(kvbase, "key")
```

---

## get_kv_pair_value_mouse_key

method in GameAPI

- 描述

    获取MOUSE_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MouseKey | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_mouse_key(kvbase, "key")
```

---

## get_kv_pair_value_mouse_wheel

method in GameAPI

- 描述

    获取MOUSE_WHEEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MouseWheel | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_mouse_wheel(kvbase, "key")
```

---

## get_kv_pair_value_post_effect

method in GameAPI

- 描述

    获取POST_EFFECT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PostEffect | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_post_effect(kvbase, "key")
```

---

## get_kv_pair_value_unit_type

method in GameAPI

- 描述

    获取UNIT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitType | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_unit_type(kvbase, "key")
```

---

## get_kv_pair_value_unit_command_type

method in GameAPI

- 描述

    获取UNIT_COMMAND_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommandType | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_unit_command_type(kvbase, "key")
```

---

## get_kv_pair_value_mini_map_color_type

method in GameAPI

- 描述

    获取MINI_MAP_COLOR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MiniMapColorType | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_mini_map_color_type(kvbase, "key")
```

---

## get_kv_pair_value_unit_behavior

method in GameAPI

- 描述

    获取UNIT_BEHAVIOR键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitBehavior | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_unit_behavior(kvbase, "key")
```

---

## get_kv_pair_value_curved_path

method in GameAPI

- 描述

    获取CURVED_PATH键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CurvedPath | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_curved_path(kvbase, "key")
```

---

## get_kv_pair_value_curved_path_3d

method in GameAPI

- 描述

    获取CURVED_PATH_3D键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CurvedPath3D | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_curved_path_3d(kvbase, "key")
```

---

## get_trigger_variable_by_type

method in GameAPI

- 描述

    获取全局触发器非数组变量（指定类型）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | var_type | string | 变量类型 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Actor | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_by_type("var_type", "key")
```

---

## get_trigger_list_variable_by_type

method in GameAPI

- 描述

    获取全局触发器数组变量子项（指定类型）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | var_type | string | 变量类型 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Actor | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_by_type("var_type", "key", 1)
```

---

## get_trigger_variable_boolean

method in GameAPI

- 描述

    获取全局触发器BOOLEAN非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_boolean("key")
```

---

## get_trigger_actor_variable_boolean

method in GameAPI

- 描述

    获取触发器BOOLEAN非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_boolean(actor, "key")
```

---

## get_trigger_list_variable_boolean

method in GameAPI

- 描述

    获取全局触发器BOOLEAN数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_boolean("key", 1)
```

---

## get_trigger_list_actor_variable_boolean

method in GameAPI

- 描述

    获取触发器BOOLEAN数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_boolean(actor, "key", 1)
```

---

## get_trigger_list_variable_all_boolean

method in GameAPI

- 描述

    获取全局触发器BOOLEAN数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 数组型变量值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_all_boolean("key")
```

---

## get_trigger_list_actor_variable_all_boolean

method in GameAPI

- 描述

    获取触发器BOOLEAN 组变量数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 数组型变量值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_all_boolean(actor, "key")
```

---

## get_trigger_variable_integer

method in GameAPI

- 描述

    获取全局触发器INTEGER非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_integer("key")
```

---

## get_trigger_actor_variable_integer

method in GameAPI

- 描述

    获取触发器INTEGER非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_integer(actor, "key")
```

---

## get_trigger_list_variable_integer

method in GameAPI

- 描述

    获取全局触发器INTEGER数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_integer("key", 1)
```

---

## get_trigger_list_actor_variable_integer

method in GameAPI

- 描述

    获取触发器INTEGER数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_integer(actor, "key", 1)
```

---

## get_trigger_list_variable_all_integer

method in GameAPI

- 描述

    获取全局触发器INTEGER数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 数组型变量值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_all_integer("key")
```

---

## get_trigger_list_actor_variable_all_integer

method in GameAPI

- 描述

    获取触发器INTEGER 组变量数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 数组型变量值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_all_integer(actor, "key")
```

---

## get_trigger_variable_float

method in GameAPI

- 描述

    获取全局触发器FLOAT非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_float("key")
```

---

## get_trigger_actor_variable_float

method in GameAPI

- 描述

    获取触发器FLOAT非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_float(actor, "key")
```

---

## get_trigger_list_variable_float

method in GameAPI

- 描述

    获取全局触发器FLOAT数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_float("key", 1)
```

---

## get_trigger_list_actor_variable_float

method in GameAPI

- 描述

    获取触发器FLOAT数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_float(actor, "key", 1)
```

---

## get_trigger_list_variable_all_float

method in GameAPI

- 描述

    获取全局触发器FLOAT数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 数组型变量值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_all_float("key")
```

---

## get_trigger_list_actor_variable_all_float

method in GameAPI

- 描述

    获取触发器FLOAT 组变量数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 数组型变量值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_all_float(actor, "key")
```

---

## get_trigger_variable_string

method in GameAPI

- 描述

    获取全局触发器STRING非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_string("key")
```

---

## get_trigger_actor_variable_string

method in GameAPI

- 描述

    获取触发器STRING非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_string(actor, "key")
```

---

## get_trigger_list_variable_string

method in GameAPI

- 描述

    获取全局触发器STRING数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_string("key", 1)
```

---

## get_trigger_list_actor_variable_string

method in GameAPI

- 描述

    获取触发器STRING数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_string(actor, "key", 1)
```

---

## get_trigger_list_variable_all_string

method in GameAPI

- 描述

    获取全局触发器STRING数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 数组型变量值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_all_string("key")
```

---

## get_trigger_list_actor_variable_all_string

method in GameAPI

- 描述

    获取触发器STRING 组变量数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 数组型变量值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_all_string(actor, "key")
```

---

## get_trigger_variable_ui_comp

method in GameAPI

- 描述

    获取全局触发器UI_COMP非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_ui_comp("key")
```

---

## get_trigger_actor_variable_ui_comp

method in GameAPI

- 描述

    获取触发器UI_COMP非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_ui_comp(actor, "key")
```

---

## get_trigger_list_variable_ui_comp

method in GameAPI

- 描述

    获取全局触发器UI_COMP数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_ui_comp("key", 1)
```

---

## get_trigger_list_actor_variable_ui_comp

method in GameAPI

- 描述

    获取触发器UI_COMP数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_ui_comp(actor, "key", 1)
```

---

## get_trigger_list_variable_all_ui_comp

method in GameAPI

- 描述

    获取全局触发器UI_COMP数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 数组型变量值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_all_ui_comp("key")
```

---

## get_trigger_list_actor_variable_all_ui_comp

method in GameAPI

- 描述

    获取触发器UI_COMP 组变量数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 数组型变量值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_all_ui_comp(actor, "key")
```

---

## get_trigger_variable_ui_comp_type

method in GameAPI

- 描述

    获取全局触发器UI_COMP_TYPE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_ui_comp_type("key")
```

---

## get_trigger_actor_variable_ui_comp_type

method in GameAPI

- 描述

    获取触发器UI_COMP_TYPE非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_ui_comp_type(actor, "key")
```

---

## get_trigger_list_variable_ui_comp_type

method in GameAPI

- 描述

    获取全局触发器UI_COMP_TYPE数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_ui_comp_type("key", 1)
```

---

## get_trigger_list_actor_variable_ui_comp_type

method in GameAPI

- 描述

    获取触发器UI_COMP_TYPE数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_ui_comp_type(actor, "key", 1)
```

---

## get_trigger_list_variable_all_ui_comp_type

method in GameAPI

- 描述

    获取全局触发器UI_COMP_TYPE数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 数组型变量值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_all_ui_comp_type("key")
```

---

## get_trigger_list_actor_variable_all_ui_comp_type

method in GameAPI

- 描述

    获取触发器UI_COMP_TYPE 组变量数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 数组型变量值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_all_ui_comp_type(actor, "key")
```

---

## get_trigger_variable_ui_comp_event_type

method in GameAPI

- 描述

    获取全局触发器UI_COMP_EVENT_TYPE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_ui_comp_event_type("key")
```

---

## get_trigger_actor_variable_ui_comp_event_type

method in GameAPI

- 描述

    获取触发器UI_COMP_EVENT_TYPE非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_ui_comp_event_type(actor, "key")
```

---

## get_trigger_list_variable_ui_comp_event_type

method in GameAPI

- 描述

    获取全局触发器UI_COMP_EVENT_TYPE数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_ui_comp_event_type("key", 1)
```

---

## get_trigger_list_actor_variable_ui_comp_event_type

method in GameAPI

- 描述

    获取触发器UI_COMP_EVENT_TYPE数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_ui_comp_event_type(actor, "key", 1)
```

---

## get_trigger_list_variable_all_ui_comp_event_type

method in GameAPI

- 描述

    获取全局触发器UI_COMP_EVENT_TYPE数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 数组型变量值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_all_ui_comp_event_type("key")
```

---

## get_trigger_list_actor_variable_all_ui_comp_event_type

method in GameAPI

- 描述

    获取触发器UI_COMP_EVENT_TYPE 组变量数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 数组型变量值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_all_ui_comp_event_type(actor, "key")
```

---

## get_trigger_variable_ui_comp_align_type

method in GameAPI

- 描述

    获取全局触发器UI_COMP_ALIGN_TYPE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_ui_comp_align_type("key")
```

---

## get_trigger_actor_variable_ui_comp_align_type

method in GameAPI

- 描述

    获取触发器UI_COMP_ALIGN_TYPE非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_ui_comp_align_type(actor, "key")
```

---

## get_trigger_list_variable_ui_comp_align_type

method in GameAPI

- 描述

    获取全局触发器UI_COMP_ALIGN_TYPE数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_ui_comp_align_type("key", 1)
```

---

## get_trigger_list_actor_variable_ui_comp_align_type

method in GameAPI

- 描述

    获取触发器UI_COMP_ALIGN_TYPE数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_ui_comp_align_type(actor, "key", 1)
```

---

## get_trigger_list_variable_all_ui_comp_align_type

method in GameAPI

- 描述

    获取全局触发器UI_COMP_ALIGN_TYPE数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 数组型变量值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_all_ui_comp_align_type("key")
```

---

## get_trigger_list_actor_variable_all_ui_comp_align_type

method in GameAPI

- 描述

    获取触发器UI_COMP_ALIGN_TYPE 组变量数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 数组型变量值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_all_ui_comp_align_type(actor, "key")
```

---

## get_trigger_variable_ui_prefab

method in GameAPI

- 描述

    获取全局触发器UI_PREFAB非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_ui_prefab("key")
```

---

## get_trigger_actor_variable_ui_prefab

method in GameAPI

- 描述

    获取触发器UI_PREFAB非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_ui_prefab(actor, "key")
```

---

## get_trigger_list_variable_ui_prefab

method in GameAPI

- 描述

    获取全局触发器UI_PREFAB数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_ui_prefab("key", 1)
```

---

## get_trigger_list_actor_variable_ui_prefab

method in GameAPI

- 描述

    获取触发器UI_PREFAB数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_ui_prefab(actor, "key", 1)
```

---

## get_trigger_list_variable_all_ui_prefab

method in GameAPI

- 描述

    获取全局触发器UI_PREFAB数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 数组型变量值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_all_ui_prefab("key")
```

---

## get_trigger_list_actor_variable_all_ui_prefab

method in GameAPI

- 描述

    获取触发器UI_PREFAB 组变量数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 数组型变量值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_all_ui_prefab(actor, "key")
```

---

## get_trigger_variable_ui_prefab_instance

method in GameAPI

- 描述

    获取全局触发器UI_PREFAB_INSTANCE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UIPrefabIns | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_ui_prefab_instance("key")
```

---

## get_trigger_actor_variable_ui_prefab_instance

method in GameAPI

- 描述

    获取触发器UI_PREFAB_INSTANCE非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UIPrefabIns | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_ui_prefab_instance(actor, "key")
```

---

## get_trigger_list_variable_ui_prefab_instance

method in GameAPI

- 描述

    获取全局触发器UI_PREFAB_INSTANCE数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UIPrefabIns | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_ui_prefab_instance("key", 1)
```

---

## get_trigger_list_actor_variable_ui_prefab_instance

method in GameAPI

- 描述

    获取触发器UI_PREFAB_INSTANCE数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UIPrefabIns | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_ui_prefab_instance(actor, "key", 1)
```

---

## get_trigger_list_variable_all_ui_prefab_instance

method in GameAPI

- 描述

    获取全局触发器UI_PREFAB_INSTANCE数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 数组型变量值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_all_ui_prefab_instance("key")
```

---

## get_trigger_list_actor_variable_all_ui_prefab_instance

method in GameAPI

- 描述

    获取触发器UI_PREFAB_INSTANCE 组变量数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 数组型变量值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_all_ui_prefab_instance(actor, "key")
```

---

## get_trigger_variable_ui_prefab_ins_uid

method in GameAPI

- 描述

    获取全局触发器UI_PREFAB_INS_UID非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_ui_prefab_ins_uid("key")
```

---

## get_trigger_actor_variable_ui_prefab_ins_uid

method in GameAPI

- 描述

    获取触发器UI_PREFAB_INS_UID非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_ui_prefab_ins_uid(actor, "key")
```

---

## get_trigger_list_variable_ui_prefab_ins_uid

method in GameAPI

- 描述

    获取全局触发器UI_PREFAB_INS_UID数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_ui_prefab_ins_uid("key", 1)
```

---

## get_trigger_list_actor_variable_ui_prefab_ins_uid

method in GameAPI

- 描述

    获取触发器UI_PREFAB_INS_UID数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_ui_prefab_ins_uid(actor, "key", 1)
```

---

## get_trigger_list_variable_all_ui_prefab_ins_uid

method in GameAPI

- 描述

    获取全局触发器UI_PREFAB_INS_UID数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 数组型变量值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_all_ui_prefab_ins_uid("key")
```

---

## get_trigger_list_actor_variable_all_ui_prefab_ins_uid

method in GameAPI

- 描述

    获取触发器UI_PREFAB_INS_UID 组变量数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 数组型变量值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_all_ui_prefab_ins_uid(actor, "key")
```

---

## get_trigger_variable_ui_direction

method in GameAPI

- 描述

    获取全局触发器UI_DIRECTION非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_ui_direction("key")
```

---

## get_trigger_actor_variable_ui_direction

method in GameAPI

- 描述

    获取触发器UI_DIRECTION非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_ui_direction(actor, "key")
```

---

## get_trigger_list_variable_ui_direction

method in GameAPI

- 描述

    获取全局触发器UI_DIRECTION数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_ui_direction("key", 1)
```

---

## get_trigger_list_actor_variable_ui_direction

method in GameAPI

- 描述

    获取触发器UI_DIRECTION数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_ui_direction(actor, "key", 1)
```

---

## get_trigger_list_variable_all_ui_direction

method in GameAPI

- 描述

    获取全局触发器UI_DIRECTION数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 数组型变量值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_all_ui_direction("key")
```

---

## get_trigger_list_actor_variable_all_ui_direction

method in GameAPI

- 描述

    获取触发器UI_DIRECTION 组变量数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 数组型变量值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_all_ui_direction(actor, "key")
```

---

## get_trigger_variable_ui_model_camera_mod

method in GameAPI

- 描述

    获取全局触发器UI_MODEL_CAMERA_MOD非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_ui_model_camera_mod("key")
```

---

## get_trigger_actor_variable_ui_model_camera_mod

method in GameAPI

- 描述

    获取触发器UI_MODEL_CAMERA_MOD非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_ui_model_camera_mod(actor, "key")
```

---

## get_trigger_list_variable_ui_model_camera_mod

method in GameAPI

- 描述

    获取全局触发器UI_MODEL_CAMERA_MOD数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_ui_model_camera_mod("key", 1)
```

---

## get_trigger_list_actor_variable_ui_model_camera_mod

method in GameAPI

- 描述

    获取触发器UI_MODEL_CAMERA_MOD数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_ui_model_camera_mod(actor, "key", 1)
```

---

## get_trigger_list_variable_all_ui_model_camera_mod

method in GameAPI

- 描述

    获取全局触发器UI_MODEL_CAMERA_MOD数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 数组型变量值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_all_ui_model_camera_mod("key")
```

---

## get_trigger_list_actor_variable_all_ui_model_camera_mod

method in GameAPI

- 描述

    获取触发器UI_MODEL_CAMERA_MOD 组变量数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 数组型变量值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_all_ui_model_camera_mod(actor, "key")
```

---

## get_trigger_variable_ui_btn_status

method in GameAPI

- 描述

    获取全局触发器UI_BTN_STATUS非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_ui_btn_status("key")
```

---

## get_trigger_actor_variable_ui_btn_status

method in GameAPI

- 描述

    获取触发器UI_BTN_STATUS非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_ui_btn_status(actor, "key")
```

---

## get_trigger_list_variable_ui_btn_status

method in GameAPI

- 描述

    获取全局触发器UI_BTN_STATUS数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_ui_btn_status("key", 1)
```

---

## get_trigger_list_actor_variable_ui_btn_status

method in GameAPI

- 描述

    获取触发器UI_BTN_STATUS数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_ui_btn_status(actor, "key", 1)
```

---

## get_trigger_list_variable_all_ui_btn_status

method in GameAPI

- 描述

    获取全局触发器UI_BTN_STATUS数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 数组型变量值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_all_ui_btn_status("key")
```

---

## get_trigger_list_actor_variable_all_ui_btn_status

method in GameAPI

- 描述

    获取触发器UI_BTN_STATUS 组变量数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 数组型变量值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_all_ui_btn_status(actor, "key")
```

---

## get_trigger_variable_ui_scrollview_type

method in GameAPI

- 描述

    获取全局触发器UI_SCROLLVIEW_TYPE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_ui_scrollview_type("key")
```

---

## get_trigger_actor_variable_ui_scrollview_type

method in GameAPI

- 描述

    获取触发器UI_SCROLLVIEW_TYPE非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_ui_scrollview_type(actor, "key")
```

---

## get_trigger_list_variable_ui_scrollview_type

method in GameAPI

- 描述

    获取全局触发器UI_SCROLLVIEW_TYPE数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_ui_scrollview_type("key", 1)
```

---

## get_trigger_list_actor_variable_ui_scrollview_type

method in GameAPI

- 描述

    获取触发器UI_SCROLLVIEW_TYPE数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_ui_scrollview_type(actor, "key", 1)
```

---

## get_trigger_list_variable_all_ui_scrollview_type

method in GameAPI

- 描述

    获取全局触发器UI_SCROLLVIEW_TYPE数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 数组型变量值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_all_ui_scrollview_type("key")
```

---

## get_trigger_list_actor_variable_all_ui_scrollview_type

method in GameAPI

- 描述

    获取触发器UI_SCROLLVIEW_TYPE 组变量数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 数组型变量值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_all_ui_scrollview_type(actor, "key")
```

---

## get_trigger_variable_ui_anim

method in GameAPI

- 描述

    获取全局触发器UI_ANIM非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UIAnimKey | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_ui_anim("key")
```

---

## get_trigger_actor_variable_ui_anim

method in GameAPI

- 描述

    获取触发器UI_ANIM非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UIAnimKey | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_ui_anim(actor, "key")
```

---

## get_trigger_list_variable_ui_anim

method in GameAPI

- 描述

    获取全局触发器UI_ANIM数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UIAnimKey | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_ui_anim("key", 1)
```

---

## get_trigger_list_actor_variable_ui_anim

method in GameAPI

- 描述

    获取触发器UI_ANIM数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UIAnimKey | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_ui_anim(actor, "key", 1)
```

---

## get_trigger_list_variable_all_ui_anim

method in GameAPI

- 描述

    获取全局触发器UI_ANIM数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 数组型变量值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_all_ui_anim("key")
```

---

## get_trigger_list_actor_variable_all_ui_anim

method in GameAPI

- 描述

    获取触发器UI_ANIM 组变量数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 数组型变量值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_all_ui_anim(actor, "key")
```

---

## get_trigger_variable_ui_anim_curve

method in GameAPI

- 描述

    获取全局触发器UI_ANIM_CURVE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_ui_anim_curve("key")
```

---

## get_trigger_actor_variable_ui_anim_curve

method in GameAPI

- 描述

    获取触发器UI_ANIM_CURVE非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_ui_anim_curve(actor, "key")
```

---

## get_trigger_list_variable_ui_anim_curve

method in GameAPI

- 描述

    获取全局触发器UI_ANIM_CURVE数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_ui_anim_curve("key", 1)
```

---

## get_trigger_list_actor_variable_ui_anim_curve

method in GameAPI

- 描述

    获取触发器UI_ANIM_CURVE数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_ui_anim_curve(actor, "key", 1)
```

---

## get_trigger_list_variable_all_ui_anim_curve

method in GameAPI

- 描述

    获取全局触发器UI_ANIM_CURVE数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 数组型变量值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_all_ui_anim_curve("key")
```

---

## get_trigger_list_actor_variable_all_ui_anim_curve

method in GameAPI

- 描述

    获取触发器UI_ANIM_CURVE 组变量数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 数组型变量值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_all_ui_anim_curve(actor, "key")
```

---

## get_trigger_variable_audio_channel

method in GameAPI

- 描述

    获取全局触发器AUDIO_CHANNEL非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_audio_channel("key")
```

---

## get_trigger_actor_variable_audio_channel

method in GameAPI

- 描述

    获取触发器AUDIO_CHANNEL非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_audio_channel(actor, "key")
```

---

## get_trigger_list_variable_audio_channel

method in GameAPI

- 描述

    获取全局触发器AUDIO_CHANNEL数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_audio_channel("key", 1)
```

---

## get_trigger_list_actor_variable_audio_channel

method in GameAPI

- 描述

    获取触发器AUDIO_CHANNEL数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_audio_channel(actor, "key", 1)
```

---

## get_trigger_list_variable_all_audio_channel

method in GameAPI

- 描述

    获取全局触发器AUDIO_CHANNEL数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 数组型变量值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_all_audio_channel("key")
```

---

## get_trigger_list_actor_variable_all_audio_channel

method in GameAPI

- 描述

    获取触发器AUDIO_CHANNEL 组变量数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 数组型变量值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_all_audio_channel(actor, "key")
```

---

## get_trigger_variable_unit_entity

method in GameAPI

- 描述

    获取全局触发器UNIT_ENTITY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_unit_entity("key")
```

---

## api_add_quick_tag

method in GameAPI

- 描述

    添加快速标签

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag_idx | integer | 标签ID |

- 返回值

    无

- 示例

```lua
GameAPI.api_add_quick_tag(1)
```

---

## api_remove_quick_tag

method in GameAPI

- 描述

    移除快速标签

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag_idx | integer | 标签ID |

- 返回值

    无

- 示例

```lua
GameAPI.api_remove_quick_tag(1)
```

---

## api_has_quick_tag

method in GameAPI

- 描述

    检查是否有快速标签

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag_idx | integer | 标签ID |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否有该标签 |

- 示例

```lua
local result = GameAPI.api_has_quick_tag(1)
```

---

## set_prefab_key_xxx_kv

method in GameAPI

- 描述

    预设库 添加kv键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | string | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | string | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_xxx_kv("prefab_conf_key", 1, "key", "value")
```

---

## add_unit_xxx_kv

method in GameAPI

- 描述

    unit添加kv键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 单位 |
    | key | string | 键值名称 |
    | value | string | value |
    | etype | integer | kv_type |
    | prefab_conf_key | string | 属性名称 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_unit_xxx_kv(kvbase, "key", "value", 1, "prefab_conf_key")
```

---

## add_item_xxx_kv

method in GameAPI

- 描述

    item添加kv键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 物品 |
    | key | string | 键值名称 |
    | value | string | value |
    | etype | integer | kv_type |
    | prefab_conf_key | string | 属性名称 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_item_xxx_kv(kvbase, "key", "value", 1, "prefab_conf_key")
```

---

## add_destructible_xxx_kv

method in GameAPI

- 描述

    destructible添加kv键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 可破坏物 |
    | key | string | 键值名称 |
    | value | string | value |
    | etype | integer | kv_type |
    | prefab_conf_key | string | 属性名称 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_destructible_xxx_kv(kvbase, "key", "value", 1, "prefab_conf_key")
```

---

## add_ability_xxx_kv

method in GameAPI

- 描述

    ability添加kv键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 技能 |
    | key | string | 键值名称 |
    | value | string | value |
    | etype | integer | kv_type |
    | prefab_conf_key | string | 属性名称 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_ability_xxx_kv(kvbase, "key", "value", 1, "prefab_conf_key")
```

---

## add_modifier_xxx_kv

method in GameAPI

- 描述

    modifier添加kv键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 魔法效果 |
    | key | string | 键值名称 |
    | value | string | value |
    | etype | integer | kv_type |
    | prefab_conf_key | string | 属性名称 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_modifier_xxx_kv(kvbase, "key", "value", 1, "prefab_conf_key")
```

---

## set_prefab_key_ui_gridview_type_kv

method in GameAPI

- 描述

    预设库 添加UI_GRIDVIEW_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | integer | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_ui_gridview_type_kv(1, 1, "key", 1)
```

---

## set_prefab_key_ui_gridview_bar_type_kv

method in GameAPI

- 描述

    预设库 添加UI_GRIDVIEW_BAR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | integer | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_ui_gridview_bar_type_kv(1, 1, "key", 1)
```

---

## set_prefab_key_ui_effect_camera_mode_kv

method in GameAPI

- 描述

    预设库 添加UI_EFFECT_CAMERA_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | integer | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_ui_effect_camera_mode_kv(1, 1, "key", 1)
```

---

## set_prefab_key_ui_equip_slot_use_type_kv

method in GameAPI

- 描述

    预设库 添加UI_EQUIP_SLOT_USE_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | integer | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_ui_equip_slot_use_type_kv(1, 1, "key", 1)
```

---

## set_prefab_key_ui_equip_slot_drag_type_kv

method in GameAPI

- 描述

    预设库 添加UI_EQUIP_SLOT_DRAG_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | integer | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_ui_equip_slot_drag_type_kv(1, 1, "key", 1)
```

---

## set_prefab_key_ui_layout_clipping_type_kv

method in GameAPI

- 描述

    预设库 添加UI_LAYOUT_CLIPPING_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | integer | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_ui_layout_clipping_type_kv(1, 1, "key", 1)
```

---

## set_prefab_key_ui_text_over_length_handling_type_kv

method in GameAPI

- 描述

    预设库 添加UI_TEXT_OVER_LENGTH_HANDLING_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | integer | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_ui_text_over_length_handling_type_kv(1, 1, "key", 1)
```

---

## set_prefab_key_ui_pos_adapt_mode_kv

method in GameAPI

- 描述

    预设库 添加UI_POS_ADAPT_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | integer | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_ui_pos_adapt_mode_kv(1, 1, "key", 1)
```

---

## set_prefab_key_ui_chat_send_channel_kv

method in GameAPI

- 描述

    预设库 添加UI_CHAT_SEND_CHANNEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | integer | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_ui_chat_send_channel_kv(1, 1, "key", 1)
```

---

## set_prefab_key_ui_chat_recv_channel_kv

method in GameAPI

- 描述

    预设库 添加UI_CHAT_RECV_CHANNEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | integer | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_ui_chat_recv_channel_kv(1, 1, "key", 1)
```

---

## set_prefab_key_ui_anim_play_mode_kv

method in GameAPI

- 描述

    预设库 添加UI_ANIM_PLAY_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | integer | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_ui_anim_play_mode_kv(1, 1, "key", 1)
```

---

## set_prefab_key_ui_text_font_name_kv

method in GameAPI

- 描述

    预设库 添加UI_TEXT_FONT_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | string | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_ui_text_font_name_kv(1, 1, "key", "value")
```

---

## set_prefab_key_ui_eca_anim_type_kv

method in GameAPI

- 描述

    预设库 添加UI_ECA_ANIM_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | integer | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_ui_eca_anim_type_kv(1, 1, "key", 1)
```

---

## set_prefab_key_local_unit_group_kv

method in GameAPI

- 描述

    预设库 添加LOCAL_UNIT_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.LocalUnitGroup | value |

- 返回值

    无

- 示例

```lua
local local_unit_group = GameAPI.get_unit_key_local_unit_group_kv(1, "key")

GameAPI.set_prefab_key_local_unit_group_kv(1, 1, "key", local_unit_group)
```

---

## set_prefab_key_damage_attack_type_kv

method in GameAPI

- 描述

    预设库 添加DAMAGE_ATTACK_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | integer | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_damage_attack_type_kv(1, 1, "key", 1)
```

---

## set_prefab_key_damage_armor_type_kv

method in GameAPI

- 描述

    预设库 添加DAMAGE_ARMOR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | integer | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_damage_armor_type_kv(1, 1, "key", 1)
```

---

## set_prefab_key_item_stack_type_kv

method in GameAPI

- 描述

    预设库 添加ITEM_STACK_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.ItemStackType | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_item_stack_type_kv(1, 1, "key", 1)
```

---

## set_prefab_key_ability_release_id_kv

method in GameAPI

- 描述

    预设库 添加ABILITY_RELEASE_ID键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.AbilityReleaseId | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_ability_release_id_kv(1, 1, "key", 1)
```

---

## set_prefab_key_slot_type_kv

method in GameAPI

- 描述

    预设库 添加SLOT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.SlotType | value |

- 返回值

    无

- 示例

```lua
local slot_type = y3.const.SlotType.BAR

GameAPI.set_prefab_key_slot_type_kv(1, 1, "key", slot_type)
```

---

## set_prefab_key_ui_point_kv

method in GameAPI

- 描述

    预设库 添加UI_POINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.FUIPoint | value |

- 返回值

    无

- 示例

```lua
local fui_point = GameAPI.get_unit_key_ui_point_kv(1, "key")

GameAPI.set_prefab_key_ui_point_kv(1, 1, "key", fui_point)
```

---

## set_prefab_key_attach_model_entity_kv

method in GameAPI

- 描述

    预设库 添加ATTACH_MODEL_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.AttachModelEntity | value |

- 返回值

    无

- 示例

```lua
local attach_model = GameAPI.get_unit_key_attach_model_entity_kv(1, "key")

GameAPI.set_prefab_key_attach_model_entity_kv(1, 1, "key", attach_model)
```

---

## set_prefab_key_live2d_kv

method in GameAPI

- 描述

    预设库 添加LIVE2D键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.Live2dKey | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_live2d_kv(1, 1, "key", 1)
```

---

## set_prefab_key_spine_kv

method in GameAPI

- 描述

    预设库 添加SPINE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.Spine | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_spine_kv(1, 1, "key", 1)
```

---

## set_prefab_key_force_entity_kv

method in GameAPI

- 描述

    预设库 添加FORCE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.Force | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_force_entity_kv(1, 1, "key", 1)
```

---

## set_prefab_key_goods_key_kv

method in GameAPI

- 描述

    预设库 添加GOODS_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.GoodsKey | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_goods_key_kv(1, 1, "key", 1)
```

---

## set_prefab_key_mouse_key_without_middle_kv

method in GameAPI

- 描述

    预设库 添加MOUSE_KEY_WITHOUT_MIDDLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.MouseKeyWithoutMiddle | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_mouse_key_without_middle_kv(1, 1, "key", 1)
```

---

## set_prefab_key_map_kv

method in GameAPI

- 描述

    预设库 添加MAP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.Map | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_map_kv(1, 1, "key", 1)
```

---

## set_prefab_key_unit_group_command_type_kv

method in GameAPI

- 描述

    预设库 添加UNIT_GROUP_COMMAND_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.UnitGroupCommandType | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_unit_group_command_type_kv(1, 1, "key", 1)
```

---

## set_prefab_key_rescue_seeker_type_kv

method in GameAPI

- 描述

    预设库 添加RESCUE_SEEKER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.ERescueSeekerType | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_rescue_seeker_type_kv(1, 1, "key", 1)
```

---

## set_prefab_key_rescuer_type_kv

method in GameAPI

- 描述

    预设库 添加RESCUER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.ERescuerType | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_rescuer_type_kv(1, 1, "key", 1)
```

---

## set_prefab_key_store_item_type_kv

method in GameAPI

- 描述

    预设库 添加STORE_ITEM_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.StoreItemType | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_store_item_type_kv(1, 1, "key", 1)
```

---

## set_prefab_key_site_state_kv

method in GameAPI

- 描述

    预设库 添加SITE_STATE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.SITE_STATE | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_site_state_kv(1, 1, "key", 1)
```

---

## set_prefab_key_coin_currency_kv

method in GameAPI

- 描述

    预设库 添加COIN_CURRENCY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.COIN_CURRENCY | value |

- 返回值

    无

- 示例

```lua
local coin_currency = "RMB"

GameAPI.set_prefab_key_coin_currency_kv(1, 1, "key", coin_currency)
```

---

## add_ui_gridview_type_kv

method in GameAPI

- 描述

    添加UI_GRIDVIEW_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | integer | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_ui_gridview_type_kv(kvbase, "key", 1)
```

---

## add_ui_gridview_bar_type_kv

method in GameAPI

- 描述

    添加UI_GRIDVIEW_BAR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | integer | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_ui_gridview_bar_type_kv(kvbase, "key", 1)
```

---

## add_ui_effect_camera_mode_kv

method in GameAPI

- 描述

    添加UI_EFFECT_CAMERA_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | integer | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_ui_effect_camera_mode_kv(kvbase, "key", 1)
```

---

## add_ui_equip_slot_use_type_kv

method in GameAPI

- 描述

    添加UI_EQUIP_SLOT_USE_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | integer | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_ui_equip_slot_use_type_kv(kvbase, "key", 1)
```

---

## add_ui_equip_slot_drag_type_kv

method in GameAPI

- 描述

    添加UI_EQUIP_SLOT_DRAG_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | integer | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_ui_equip_slot_drag_type_kv(kvbase, "key", 1)
```

---

## add_ui_layout_clipping_type_kv

method in GameAPI

- 描述

    添加UI_LAYOUT_CLIPPING_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | integer | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_ui_layout_clipping_type_kv(kvbase, "key", 1)
```

---

## add_ui_text_over_length_handling_type_kv

method in GameAPI

- 描述

    添加UI_TEXT_OVER_LENGTH_HANDLING_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | integer | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_ui_text_over_length_handling_type_kv(kvbase, "key", 1)
```

---

## add_ui_pos_adapt_mode_kv

method in GameAPI

- 描述

    添加UI_POS_ADAPT_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | integer | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_ui_pos_adapt_mode_kv(kvbase, "key", 1)
```

---

## add_ui_chat_send_channel_kv

method in GameAPI

- 描述

    添加UI_CHAT_SEND_CHANNEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | integer | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_ui_chat_send_channel_kv(kvbase, "key", 1)
```

---

## add_ui_chat_recv_channel_kv

method in GameAPI

- 描述

    添加UI_CHAT_RECV_CHANNEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | integer | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_ui_chat_recv_channel_kv(kvbase, "key", 1)
```

---

## add_ui_anim_play_mode_kv

method in GameAPI

- 描述

    添加UI_ANIM_PLAY_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | integer | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_ui_anim_play_mode_kv(kvbase, "key", 1)
```

---

## add_ui_text_font_name_kv

method in GameAPI

- 描述

    添加UI_TEXT_FONT_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | string | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_ui_text_font_name_kv(kvbase, "key", "item")
```

---

## add_ui_eca_anim_type_kv

method in GameAPI

- 描述

    添加UI_ECA_ANIM_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | integer | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_ui_eca_anim_type_kv(kvbase, "key", 1)
```

---

## add_local_unit_group_kv

method in GameAPI

- 描述

    添加LOCAL_UNIT_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.LocalUnitGroup | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local local_unit_group = GameAPI.get_unit_key_local_unit_group_kv(1, "key")

GameAPI.add_local_unit_group_kv(kvbase, "key")
```

---

## add_damage_attack_type_kv

method in GameAPI

- 描述

    添加DAMAGE_ATTACK_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | integer | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_damage_attack_type_kv(kvbase, "key", 1)
```

---

## add_damage_armor_type_kv

method in GameAPI

- 描述

    添加DAMAGE_ARMOR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | integer | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_damage_armor_type_kv(kvbase, "key", 1)
```

---

## add_item_stack_type_kv

method in GameAPI

- 描述

    添加ITEM_STACK_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.ItemStackType | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_item_stack_type_kv(kvbase, "key", 1)
```

---

## add_ability_release_id_kv

method in GameAPI

- 描述

    添加ABILITY_RELEASE_ID键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.AbilityReleaseId | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_ability_release_id_kv(kvbase, "key", 1)
```

---

## add_slot_type_kv

method in GameAPI

- 描述

    添加SLOT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.SlotType | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local slot_type = y3.const.SlotType.BAR

GameAPI.add_slot_type_kv(kvbase, "key")
```

---

## add_ui_point_kv

method in GameAPI

- 描述

    添加UI_POINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.FUIPoint | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local fui_point = GameAPI.get_unit_key_ui_point_kv(1, "key")

GameAPI.add_ui_point_kv(kvbase, "key")
```

---

## add_attach_model_entity_kv

method in GameAPI

- 描述

    添加ATTACH_MODEL_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.AttachModelEntity | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local attach_model = GameAPI.get_unit_key_attach_model_entity_kv(1, "key")

GameAPI.add_attach_model_entity_kv(kvbase, "key")
```

---

## add_live2d_kv

method in GameAPI

- 描述

    添加LIVE2D键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.Live2dKey | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_live2d_kv(kvbase, "key", 1)
```

---

## add_spine_kv

method in GameAPI

- 描述

    添加SPINE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.Spine | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_spine_kv(kvbase, "key", 1)
```

---

## add_force_entity_kv

method in GameAPI

- 描述

    添加FORCE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.Force | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_force_entity_kv(kvbase, "key", 1)
```

---

## add_goods_key_kv

method in GameAPI

- 描述

    添加GOODS_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.GoodsKey | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_goods_key_kv(kvbase, "key", 1)
```

---

## add_mouse_key_without_middle_kv

method in GameAPI

- 描述

    添加MOUSE_KEY_WITHOUT_MIDDLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.MouseKeyWithoutMiddle | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_mouse_key_without_middle_kv(kvbase, "key", 1)
```

---

## add_map_kv

method in GameAPI

- 描述

    添加MAP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.Map | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_map_kv(kvbase, "key", 1)
```

---

## add_unit_group_command_type_kv

method in GameAPI

- 描述

    添加UNIT_GROUP_COMMAND_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.UnitGroupCommandType | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_unit_group_command_type_kv(kvbase, "key", 1)
```

---

## add_rescue_seeker_type_kv

method in GameAPI

- 描述

    添加RESCUE_SEEKER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.ERescueSeekerType | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_rescue_seeker_type_kv(kvbase, "key", 1)
```

---

## add_rescuer_type_kv

method in GameAPI

- 描述

    添加RESCUER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.ERescuerType | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_rescuer_type_kv(kvbase, "key", 1)
```

---

## add_store_item_type_kv

method in GameAPI

- 描述

    添加STORE_ITEM_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.StoreItemType | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_store_item_type_kv(kvbase, "key", 1)
```

---

## add_site_state_kv

method in GameAPI

- 描述

    添加SITE_STATE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.SITE_STATE | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.add_site_state_kv(kvbase, "key", 1)
```

---

## add_coin_currency_kv

method in GameAPI

- 描述

    添加COIN_CURRENCY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键值名称 |
    | item? | py.COIN_CURRENCY | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle
local coin_currency = "RMB"

GameAPI.add_coin_currency_kv(kvbase, "key")
```

---

## has_prefab_xxx_kv

method in GameAPI

- 描述

    判断预设是否存在%s键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_type | string | 预设类型 |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |
    | kv_type | integer | kv_type |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_prefab_xxx_kv("prefab_type", unit_key, "key", 1)
```

---

## has_entity_ckv_pair_value_xxx

method in GameAPI

- 描述

    获取值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_entity_ckv_pair_value_xxx(kvbase, "key")
```

---

## has_ability_ckv_pair_value_xxx

method in GameAPI

- 描述

    获取值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_ability_ckv_pair_value_xxx(kvbase, "key")
```

---

## has_modifier_ckv_pair_value_xxx

method in GameAPI

- 描述

    获取值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_modifier_ckv_pair_value_xxx(kvbase, "key")
```

---

## has_kv_pair_ui_gridview_type

method in GameAPI

- 描述

    判断是否存在UI_GRIDVIEW_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_ui_gridview_type(kvbase, "key")
```

---

## has_prefab_ui_gridview_type_kv

method in GameAPI

- 描述

    判断预设是否存在UI_GRIDVIEW_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_type | string | 预设类型 |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_prefab_ui_gridview_type_kv("prefab_type", unit_key, "key")
```

---

## has_unit_key_ui_gridview_type_kv

method in GameAPI

- 描述

    判断单位编号是否存在UI_GRIDVIEW_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_ui_gridview_type_kv(unit_key, "key")
```

---

## has_item_key_ui_gridview_type_kv

method in GameAPI

- 描述

    判断物品编号是否存在UI_GRIDVIEW_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_ui_gridview_type_kv(item_key, "key")
```

---

## has_ability_key_ui_gridview_type_kv

method in GameAPI

- 描述

    判断技能编号是否存在UI_GRIDVIEW_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_ui_gridview_type_kv(ability_key, "key")
```

---

## has_kv_pair_ui_gridview_bar_type

method in GameAPI

- 描述

    判断是否存在UI_GRIDVIEW_BAR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_ui_gridview_bar_type(kvbase, "key")
```

---

## has_prefab_ui_gridview_bar_type_kv

method in GameAPI

- 描述

    判断预设是否存在UI_GRIDVIEW_BAR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_type | string | 预设类型 |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_prefab_ui_gridview_bar_type_kv("prefab_type", unit_key, "key")
```

---

## has_unit_key_ui_gridview_bar_type_kv

method in GameAPI

- 描述

    判断单位编号是否存在UI_GRIDVIEW_BAR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_ui_gridview_bar_type_kv(unit_key, "key")
```

---

## has_item_key_ui_gridview_bar_type_kv

method in GameAPI

- 描述

    判断物品编号是否存在UI_GRIDVIEW_BAR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_ui_gridview_bar_type_kv(item_key, "key")
```

---

## has_ability_key_ui_gridview_bar_type_kv

method in GameAPI

- 描述

    判断技能编号是否存在UI_GRIDVIEW_BAR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_ui_gridview_bar_type_kv(ability_key, "key")
```

---

## has_kv_pair_ui_effect_camera_mode

method in GameAPI

- 描述

    判断是否存在UI_EFFECT_CAMERA_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_ui_effect_camera_mode(kvbase, "key")
```

---

## has_prefab_ui_effect_camera_mode_kv

method in GameAPI

- 描述

    判断预设是否存在UI_EFFECT_CAMERA_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_type | string | 预设类型 |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_prefab_ui_effect_camera_mode_kv("prefab_type", unit_key, "key")
```

---

## has_unit_key_ui_effect_camera_mode_kv

method in GameAPI

- 描述

    判断单位编号是否存在UI_EFFECT_CAMERA_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_ui_effect_camera_mode_kv(unit_key, "key")
```

---

## has_item_key_ui_effect_camera_mode_kv

method in GameAPI

- 描述

    判断物品编号是否存在UI_EFFECT_CAMERA_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_ui_effect_camera_mode_kv(item_key, "key")
```

---

## has_ability_key_ui_effect_camera_mode_kv

method in GameAPI

- 描述

    判断技能编号是否存在UI_EFFECT_CAMERA_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_ui_effect_camera_mode_kv(ability_key, "key")
```

---

## has_kv_pair_ui_equip_slot_use_type

method in GameAPI

- 描述

    判断是否存在UI_EQUIP_SLOT_USE_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_ui_equip_slot_use_type(kvbase, "key")
```

---

## has_prefab_ui_equip_slot_use_type_kv

method in GameAPI

- 描述

    判断预设是否存在UI_EQUIP_SLOT_USE_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_type | string | 预设类型 |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_prefab_ui_equip_slot_use_type_kv("prefab_type", unit_key, "key")
```

---

## has_unit_key_ui_equip_slot_use_type_kv

method in GameAPI

- 描述

    判断单位编号是否存在UI_EQUIP_SLOT_USE_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_ui_equip_slot_use_type_kv(unit_key, "key")
```

---

## has_item_key_ui_equip_slot_use_type_kv

method in GameAPI

- 描述

    判断物品编号是否存在UI_EQUIP_SLOT_USE_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_ui_equip_slot_use_type_kv(item_key, "key")
```

---

## has_ability_key_ui_equip_slot_use_type_kv

method in GameAPI

- 描述

    判断技能编号是否存在UI_EQUIP_SLOT_USE_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_ui_equip_slot_use_type_kv(ability_key, "key")
```

---

## has_kv_pair_ui_equip_slot_drag_type

method in GameAPI

- 描述

    判断是否存在UI_EQUIP_SLOT_DRAG_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_ui_equip_slot_drag_type(kvbase, "key")
```

---

## has_prefab_ui_equip_slot_drag_type_kv

method in GameAPI

- 描述

    判断预设是否存在UI_EQUIP_SLOT_DRAG_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_type | string | 预设类型 |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_prefab_ui_equip_slot_drag_type_kv("prefab_type", unit_key, "key")
```

---

## has_unit_key_ui_equip_slot_drag_type_kv

method in GameAPI

- 描述

    判断单位编号是否存在UI_EQUIP_SLOT_DRAG_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_ui_equip_slot_drag_type_kv(unit_key, "key")
```

---

## has_item_key_ui_equip_slot_drag_type_kv

method in GameAPI

- 描述

    判断物品编号是否存在UI_EQUIP_SLOT_DRAG_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_ui_equip_slot_drag_type_kv(item_key, "key")
```

---

## has_ability_key_ui_equip_slot_drag_type_kv

method in GameAPI

- 描述

    判断技能编号是否存在UI_EQUIP_SLOT_DRAG_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_ui_equip_slot_drag_type_kv(ability_key, "key")
```

---

## has_kv_pair_ui_layout_clipping_type

method in GameAPI

- 描述

    判断是否存在UI_LAYOUT_CLIPPING_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_ui_layout_clipping_type(kvbase, "key")
```

---

## has_prefab_ui_layout_clipping_type_kv

method in GameAPI

- 描述

    判断预设是否存在UI_LAYOUT_CLIPPING_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_type | string | 预设类型 |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_prefab_ui_layout_clipping_type_kv("prefab_type", unit_key, "key")
```

---

## has_unit_key_ui_layout_clipping_type_kv

method in GameAPI

- 描述

    判断单位编号是否存在UI_LAYOUT_CLIPPING_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_ui_layout_clipping_type_kv(unit_key, "key")
```

---

## has_item_key_ui_layout_clipping_type_kv

method in GameAPI

- 描述

    判断物品编号是否存在UI_LAYOUT_CLIPPING_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_ui_layout_clipping_type_kv(item_key, "key")
```

---

## has_ability_key_ui_layout_clipping_type_kv

method in GameAPI

- 描述

    判断技能编号是否存在UI_LAYOUT_CLIPPING_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_ui_layout_clipping_type_kv(ability_key, "key")
```

---

## has_kv_pair_ui_text_over_length_handling_type

method in GameAPI

- 描述

    判断是否存在UI_TEXT_OVER_LENGTH_HANDLING_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_ui_text_over_length_handling_type(kvbase, "key")
```

---

## has_prefab_ui_text_over_length_handling_type_kv

method in GameAPI

- 描述

    判断预设是否存在UI_TEXT_OVER_LENGTH_HANDLING_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_type | string | 预设类型 |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_prefab_ui_text_over_length_handling_type_kv("prefab_type", unit_key, "key")
```

---

## has_unit_key_ui_text_over_length_handling_type_kv

method in GameAPI

- 描述

    判断单位编号是否存在UI_TEXT_OVER_LENGTH_HANDLING_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_ui_text_over_length_handling_type_kv(unit_key, "key")
```

---

## has_item_key_ui_text_over_length_handling_type_kv

method in GameAPI

- 描述

    判断物品编号是否存在UI_TEXT_OVER_LENGTH_HANDLING_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_ui_text_over_length_handling_type_kv(item_key, "key")
```

---

## has_ability_key_ui_text_over_length_handling_type_kv

method in GameAPI

- 描述

    判断技能编号是否存在UI_TEXT_OVER_LENGTH_HANDLING_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_ui_text_over_length_handling_type_kv(ability_key, "key")
```

---

## has_kv_pair_ui_pos_adapt_mode

method in GameAPI

- 描述

    判断是否存在UI_POS_ADAPT_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_ui_pos_adapt_mode(kvbase, "key")
```

---

## has_prefab_ui_pos_adapt_mode_kv

method in GameAPI

- 描述

    判断预设是否存在UI_POS_ADAPT_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_type | string | 预设类型 |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_prefab_ui_pos_adapt_mode_kv("prefab_type", unit_key, "key")
```

---

## has_unit_key_ui_pos_adapt_mode_kv

method in GameAPI

- 描述

    判断单位编号是否存在UI_POS_ADAPT_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_ui_pos_adapt_mode_kv(unit_key, "key")
```

---

## has_item_key_ui_pos_adapt_mode_kv

method in GameAPI

- 描述

    判断物品编号是否存在UI_POS_ADAPT_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_ui_pos_adapt_mode_kv(item_key, "key")
```

---

## has_ability_key_ui_pos_adapt_mode_kv

method in GameAPI

- 描述

    判断技能编号是否存在UI_POS_ADAPT_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_ui_pos_adapt_mode_kv(ability_key, "key")
```

---

## has_kv_pair_ui_chat_send_channel

method in GameAPI

- 描述

    判断是否存在UI_CHAT_SEND_CHANNEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_ui_chat_send_channel(kvbase, "key")
```

---

## has_prefab_ui_chat_send_channel_kv

method in GameAPI

- 描述

    判断预设是否存在UI_CHAT_SEND_CHANNEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_type | string | 预设类型 |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_prefab_ui_chat_send_channel_kv("prefab_type", unit_key, "key")
```

---

## has_unit_key_ui_chat_send_channel_kv

method in GameAPI

- 描述

    判断单位编号是否存在UI_CHAT_SEND_CHANNEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_ui_chat_send_channel_kv(unit_key, "key")
```

---

## has_item_key_ui_chat_send_channel_kv

method in GameAPI

- 描述

    判断物品编号是否存在UI_CHAT_SEND_CHANNEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_ui_chat_send_channel_kv(item_key, "key")
```

---

## has_ability_key_ui_chat_send_channel_kv

method in GameAPI

- 描述

    判断技能编号是否存在UI_CHAT_SEND_CHANNEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_ui_chat_send_channel_kv(ability_key, "key")
```

---

## has_kv_pair_ui_chat_recv_channel

method in GameAPI

- 描述

    判断是否存在UI_CHAT_RECV_CHANNEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_ui_chat_recv_channel(kvbase, "key")
```

---

## has_prefab_ui_chat_recv_channel_kv

method in GameAPI

- 描述

    判断预设是否存在UI_CHAT_RECV_CHANNEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_type | string | 预设类型 |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_prefab_ui_chat_recv_channel_kv("prefab_type", unit_key, "key")
```

---

## has_unit_key_ui_chat_recv_channel_kv

method in GameAPI

- 描述

    判断单位编号是否存在UI_CHAT_RECV_CHANNEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_ui_chat_recv_channel_kv(unit_key, "key")
```

---

## has_item_key_ui_chat_recv_channel_kv

method in GameAPI

- 描述

    判断物品编号是否存在UI_CHAT_RECV_CHANNEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_ui_chat_recv_channel_kv(item_key, "key")
```

---

## has_ability_key_ui_chat_recv_channel_kv

method in GameAPI

- 描述

    判断技能编号是否存在UI_CHAT_RECV_CHANNEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_ui_chat_recv_channel_kv(ability_key, "key")
```

---

## has_kv_pair_ui_anim_play_mode

method in GameAPI

- 描述

    判断是否存在UI_ANIM_PLAY_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_ui_anim_play_mode(kvbase, "key")
```

---

## has_prefab_ui_anim_play_mode_kv

method in GameAPI

- 描述

    判断预设是否存在UI_ANIM_PLAY_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_type | string | 预设类型 |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_prefab_ui_anim_play_mode_kv("prefab_type", unit_key, "key")
```

---

## has_unit_key_ui_anim_play_mode_kv

method in GameAPI

- 描述

    判断单位编号是否存在UI_ANIM_PLAY_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_ui_anim_play_mode_kv(unit_key, "key")
```

---

## has_item_key_ui_anim_play_mode_kv

method in GameAPI

- 描述

    判断物品编号是否存在UI_ANIM_PLAY_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_ui_anim_play_mode_kv(item_key, "key")
```

---

## has_ability_key_ui_anim_play_mode_kv

method in GameAPI

- 描述

    判断技能编号是否存在UI_ANIM_PLAY_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_ui_anim_play_mode_kv(ability_key, "key")
```

---

## has_kv_pair_ui_text_font_name

method in GameAPI

- 描述

    判断是否存在UI_TEXT_FONT_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_ui_text_font_name(kvbase, "key")
```

---

## has_prefab_ui_text_font_name_kv

method in GameAPI

- 描述

    判断预设是否存在UI_TEXT_FONT_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_type | string | 预设类型 |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_prefab_ui_text_font_name_kv("prefab_type", unit_key, "key")
```

---

## has_unit_key_ui_text_font_name_kv

method in GameAPI

- 描述

    判断单位编号是否存在UI_TEXT_FONT_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_ui_text_font_name_kv(unit_key, "key")
```

---

## has_item_key_ui_text_font_name_kv

method in GameAPI

- 描述

    判断物品编号是否存在UI_TEXT_FONT_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_ui_text_font_name_kv(item_key, "key")
```

---

## has_ability_key_ui_text_font_name_kv

method in GameAPI

- 描述

    判断技能编号是否存在UI_TEXT_FONT_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_ui_text_font_name_kv(ability_key, "key")
```

---

## has_kv_pair_ui_eca_anim_type

method in GameAPI

- 描述

    判断是否存在UI_ECA_ANIM_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_ui_eca_anim_type(kvbase, "key")
```

---

## has_prefab_ui_eca_anim_type_kv

method in GameAPI

- 描述

    判断预设是否存在UI_ECA_ANIM_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_type | string | 预设类型 |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_prefab_ui_eca_anim_type_kv("prefab_type", unit_key, "key")
```

---

## has_unit_key_ui_eca_anim_type_kv

method in GameAPI

- 描述

    判断单位编号是否存在UI_ECA_ANIM_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_ui_eca_anim_type_kv(unit_key, "key")
```

---

## has_item_key_ui_eca_anim_type_kv

method in GameAPI

- 描述

    判断物品编号是否存在UI_ECA_ANIM_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_ui_eca_anim_type_kv(item_key, "key")
```

---

## has_ability_key_ui_eca_anim_type_kv

method in GameAPI

- 描述

    判断技能编号是否存在UI_ECA_ANIM_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_ui_eca_anim_type_kv(ability_key, "key")
```

---

## has_kv_pair_local_unit_group

method in GameAPI

- 描述

    判断是否存在LOCAL_UNIT_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_local_unit_group(kvbase, "key")
```

---

## has_prefab_local_unit_group_kv

method in GameAPI

- 描述

    判断预设是否存在LOCAL_UNIT_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_type | string | 预设类型 |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_prefab_local_unit_group_kv("prefab_type", unit_key, "key")
```

---

## has_unit_key_local_unit_group_kv

method in GameAPI

- 描述

    判断单位编号是否存在LOCAL_UNIT_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_local_unit_group_kv(unit_key, "key")
```

---

## has_item_key_local_unit_group_kv

method in GameAPI

- 描述

    判断物品编号是否存在LOCAL_UNIT_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_local_unit_group_kv(item_key, "key")
```

---

## has_ability_key_local_unit_group_kv

method in GameAPI

- 描述

    判断技能编号是否存在LOCAL_UNIT_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_local_unit_group_kv(ability_key, "key")
```

---

## has_kv_pair_damage_attack_type

method in GameAPI

- 描述

    判断是否存在DAMAGE_ATTACK_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_damage_attack_type(kvbase, "key")
```

---

## has_prefab_damage_attack_type_kv

method in GameAPI

- 描述

    判断预设是否存在DAMAGE_ATTACK_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_type | string | 预设类型 |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_prefab_damage_attack_type_kv("prefab_type", unit_key, "key")
```

---

## has_unit_key_damage_attack_type_kv

method in GameAPI

- 描述

    判断单位编号是否存在DAMAGE_ATTACK_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_damage_attack_type_kv(unit_key, "key")
```

---

## has_item_key_damage_attack_type_kv

method in GameAPI

- 描述

    判断物品编号是否存在DAMAGE_ATTACK_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_damage_attack_type_kv(item_key, "key")
```

---

## has_ability_key_damage_attack_type_kv

method in GameAPI

- 描述

    判断技能编号是否存在DAMAGE_ATTACK_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_damage_attack_type_kv(ability_key, "key")
```

---

## has_kv_pair_damage_armor_type

method in GameAPI

- 描述

    判断是否存在DAMAGE_ARMOR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_damage_armor_type(kvbase, "key")
```

---

## has_prefab_damage_armor_type_kv

method in GameAPI

- 描述

    判断预设是否存在DAMAGE_ARMOR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_type | string | 预设类型 |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_prefab_damage_armor_type_kv("prefab_type", unit_key, "key")
```

---

## has_unit_key_damage_armor_type_kv

method in GameAPI

- 描述

    判断单位编号是否存在DAMAGE_ARMOR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_damage_armor_type_kv(unit_key, "key")
```

---

## has_item_key_damage_armor_type_kv

method in GameAPI

- 描述

    判断物品编号是否存在DAMAGE_ARMOR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_damage_armor_type_kv(item_key, "key")
```

---

## has_ability_key_damage_armor_type_kv

method in GameAPI

- 描述

    判断技能编号是否存在DAMAGE_ARMOR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_damage_armor_type_kv(ability_key, "key")
```

---

## has_kv_pair_item_stack_type

method in GameAPI

- 描述

    判断是否存在ITEM_STACK_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_item_stack_type(kvbase, "key")
```

---

## has_prefab_item_stack_type_kv

method in GameAPI

- 描述

    判断预设是否存在ITEM_STACK_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_type | string | 预设类型 |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_prefab_item_stack_type_kv("prefab_type", unit_key, "key")
```

---

## has_unit_key_item_stack_type_kv

method in GameAPI

- 描述

    判断单位编号是否存在ITEM_STACK_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_item_stack_type_kv(unit_key, "key")
```

---

## has_item_key_item_stack_type_kv

method in GameAPI

- 描述

    判断物品编号是否存在ITEM_STACK_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_item_stack_type_kv(item_key, "key")
```

---

## has_ability_key_item_stack_type_kv

method in GameAPI

- 描述

    判断技能编号是否存在ITEM_STACK_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_item_stack_type_kv(ability_key, "key")
```

---

## has_kv_pair_ability_release_id

method in GameAPI

- 描述

    判断是否存在ABILITY_RELEASE_ID键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_ability_release_id(kvbase, "key")
```

---

## has_prefab_ability_release_id_kv

method in GameAPI

- 描述

    判断预设是否存在ABILITY_RELEASE_ID键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_type | string | 预设类型 |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_prefab_ability_release_id_kv("prefab_type", unit_key, "key")
```

---

## has_unit_key_ability_release_id_kv

method in GameAPI

- 描述

    判断单位编号是否存在ABILITY_RELEASE_ID键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_ability_release_id_kv(unit_key, "key")
```

---

## has_item_key_ability_release_id_kv

method in GameAPI

- 描述

    判断物品编号是否存在ABILITY_RELEASE_ID键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_ability_release_id_kv(item_key, "key")
```

---

## has_ability_key_ability_release_id_kv

method in GameAPI

- 描述

    判断技能编号是否存在ABILITY_RELEASE_ID键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_ability_release_id_kv(ability_key, "key")
```

---

## has_kv_pair_slot_type

method in GameAPI

- 描述

    判断是否存在SLOT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_slot_type(kvbase, "key")
```

---

## has_prefab_slot_type_kv

method in GameAPI

- 描述

    判断预设是否存在SLOT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_type | string | 预设类型 |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_prefab_slot_type_kv("prefab_type", unit_key, "key")
```

---

## has_unit_key_slot_type_kv

method in GameAPI

- 描述

    判断单位编号是否存在SLOT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_slot_type_kv(unit_key, "key")
```

---

## has_item_key_slot_type_kv

method in GameAPI

- 描述

    判断物品编号是否存在SLOT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_slot_type_kv(item_key, "key")
```

---

## has_ability_key_slot_type_kv

method in GameAPI

- 描述

    判断技能编号是否存在SLOT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_slot_type_kv(ability_key, "key")
```

---

## has_kv_pair_ui_point

method in GameAPI

- 描述

    判断是否存在UI_POINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_ui_point(kvbase, "key")
```

---

## has_prefab_ui_point_kv

method in GameAPI

- 描述

    判断预设是否存在UI_POINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_type | string | 预设类型 |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_prefab_ui_point_kv("prefab_type", unit_key, "key")
```

---

## has_unit_key_ui_point_kv

method in GameAPI

- 描述

    判断单位编号是否存在UI_POINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_ui_point_kv(unit_key, "key")
```

---

## has_item_key_ui_point_kv

method in GameAPI

- 描述

    判断物品编号是否存在UI_POINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_ui_point_kv(item_key, "key")
```

---

## has_ability_key_ui_point_kv

method in GameAPI

- 描述

    判断技能编号是否存在UI_POINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_ui_point_kv(ability_key, "key")
```

---

## has_kv_pair_attach_model_entity

method in GameAPI

- 描述

    判断是否存在ATTACH_MODEL_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_attach_model_entity(kvbase, "key")
```

---

## has_prefab_attach_model_entity_kv

method in GameAPI

- 描述

    判断预设是否存在ATTACH_MODEL_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_type | string | 预设类型 |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_prefab_attach_model_entity_kv("prefab_type", unit_key, "key")
```

---

## has_unit_key_attach_model_entity_kv

method in GameAPI

- 描述

    判断单位编号是否存在ATTACH_MODEL_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_attach_model_entity_kv(unit_key, "key")
```

---

## has_item_key_attach_model_entity_kv

method in GameAPI

- 描述

    判断物品编号是否存在ATTACH_MODEL_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_attach_model_entity_kv(item_key, "key")
```

---

## has_ability_key_attach_model_entity_kv

method in GameAPI

- 描述

    判断技能编号是否存在ATTACH_MODEL_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_attach_model_entity_kv(ability_key, "key")
```

---

## has_kv_pair_live2d

method in GameAPI

- 描述

    判断是否存在LIVE2D键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_live2d(kvbase, "key")
```

---

## has_prefab_live2d_kv

method in GameAPI

- 描述

    判断预设是否存在LIVE2D键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_type | string | 预设类型 |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_prefab_live2d_kv("prefab_type", unit_key, "key")
```

---

## has_unit_key_live2d_kv

method in GameAPI

- 描述

    判断单位编号是否存在LIVE2D键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_live2d_kv(unit_key, "key")
```

---

## has_item_key_live2d_kv

method in GameAPI

- 描述

    判断物品编号是否存在LIVE2D键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_live2d_kv(item_key, "key")
```

---

## has_ability_key_live2d_kv

method in GameAPI

- 描述

    判断技能编号是否存在LIVE2D键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_live2d_kv(ability_key, "key")
```

---

## has_kv_pair_spine

method in GameAPI

- 描述

    判断是否存在SPINE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_spine(kvbase, "key")
```

---

## has_prefab_spine_kv

method in GameAPI

- 描述

    判断预设是否存在SPINE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_type | string | 预设类型 |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_prefab_spine_kv("prefab_type", unit_key, "key")
```

---

## has_unit_key_spine_kv

method in GameAPI

- 描述

    判断单位编号是否存在SPINE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_spine_kv(unit_key, "key")
```

---

## has_item_key_spine_kv

method in GameAPI

- 描述

    判断物品编号是否存在SPINE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_spine_kv(item_key, "key")
```

---

## has_ability_key_spine_kv

method in GameAPI

- 描述

    判断技能编号是否存在SPINE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_spine_kv(ability_key, "key")
```

---

## has_kv_pair_force_entity

method in GameAPI

- 描述

    判断是否存在FORCE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_force_entity(kvbase, "key")
```

---

## has_prefab_force_entity_kv

method in GameAPI

- 描述

    判断预设是否存在FORCE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_type | string | 预设类型 |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_prefab_force_entity_kv("prefab_type", unit_key, "key")
```

---

## has_unit_key_force_entity_kv

method in GameAPI

- 描述

    判断单位编号是否存在FORCE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_force_entity_kv(unit_key, "key")
```

---

## has_item_key_force_entity_kv

method in GameAPI

- 描述

    判断物品编号是否存在FORCE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_force_entity_kv(item_key, "key")
```

---

## has_ability_key_force_entity_kv

method in GameAPI

- 描述

    判断技能编号是否存在FORCE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_force_entity_kv(ability_key, "key")
```

---

## has_kv_pair_goods_key

method in GameAPI

- 描述

    判断是否存在GOODS_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_goods_key(kvbase, "key")
```

---

## has_prefab_goods_key_kv

method in GameAPI

- 描述

    判断预设是否存在GOODS_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_type | string | 预设类型 |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_prefab_goods_key_kv("prefab_type", unit_key, "key")
```

---

## has_unit_key_goods_key_kv

method in GameAPI

- 描述

    判断单位编号是否存在GOODS_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_goods_key_kv(unit_key, "key")
```

---

## has_item_key_goods_key_kv

method in GameAPI

- 描述

    判断物品编号是否存在GOODS_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_goods_key_kv(item_key, "key")
```

---

## has_ability_key_goods_key_kv

method in GameAPI

- 描述

    判断技能编号是否存在GOODS_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_goods_key_kv(ability_key, "key")
```

---

## has_kv_pair_mouse_key_without_middle

method in GameAPI

- 描述

    判断是否存在MOUSE_KEY_WITHOUT_MIDDLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_mouse_key_without_middle(kvbase, "key")
```

---

## has_prefab_mouse_key_without_middle_kv

method in GameAPI

- 描述

    判断预设是否存在MOUSE_KEY_WITHOUT_MIDDLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_type | string | 预设类型 |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_prefab_mouse_key_without_middle_kv("prefab_type", unit_key, "key")
```

---

## has_unit_key_mouse_key_without_middle_kv

method in GameAPI

- 描述

    判断单位编号是否存在MOUSE_KEY_WITHOUT_MIDDLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_mouse_key_without_middle_kv(unit_key, "key")
```

---

## has_item_key_mouse_key_without_middle_kv

method in GameAPI

- 描述

    判断物品编号是否存在MOUSE_KEY_WITHOUT_MIDDLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_mouse_key_without_middle_kv(item_key, "key")
```

---

## has_ability_key_mouse_key_without_middle_kv

method in GameAPI

- 描述

    判断技能编号是否存在MOUSE_KEY_WITHOUT_MIDDLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_mouse_key_without_middle_kv(ability_key, "key")
```

---

## has_kv_pair_map

method in GameAPI

- 描述

    判断是否存在MAP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_map(kvbase, "key")
```

---

## has_prefab_map_kv

method in GameAPI

- 描述

    判断预设是否存在MAP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_type | string | 预设类型 |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_prefab_map_kv("prefab_type", unit_key, "key")
```

---

## has_unit_key_map_kv

method in GameAPI

- 描述

    判断单位编号是否存在MAP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_map_kv(unit_key, "key")
```

---

## has_item_key_map_kv

method in GameAPI

- 描述

    判断物品编号是否存在MAP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_map_kv(item_key, "key")
```

---

## has_ability_key_map_kv

method in GameAPI

- 描述

    判断技能编号是否存在MAP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_map_kv(ability_key, "key")
```

---

## has_kv_pair_unit_group_command_type

method in GameAPI

- 描述

    判断是否存在UNIT_GROUP_COMMAND_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_unit_group_command_type(kvbase, "key")
```

---

## has_prefab_unit_group_command_type_kv

method in GameAPI

- 描述

    判断预设是否存在UNIT_GROUP_COMMAND_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_type | string | 预设类型 |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_prefab_unit_group_command_type_kv("prefab_type", unit_key, "key")
```

---

## has_unit_key_unit_group_command_type_kv

method in GameAPI

- 描述

    判断单位编号是否存在UNIT_GROUP_COMMAND_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_unit_group_command_type_kv(unit_key, "key")
```

---

## has_item_key_unit_group_command_type_kv

method in GameAPI

- 描述

    判断物品编号是否存在UNIT_GROUP_COMMAND_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_unit_group_command_type_kv(item_key, "key")
```

---

## has_ability_key_unit_group_command_type_kv

method in GameAPI

- 描述

    判断技能编号是否存在UNIT_GROUP_COMMAND_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.AbilityKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.has_ability_key_unit_group_command_type_kv(ability_key, "key")
```

---

## has_kv_pair_rescue_seeker_type

method in GameAPI

- 描述

    判断是否存在RESCUE_SEEKER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.has_kv_pair_rescue_seeker_type(kvbase, "key")
```

---

## has_prefab_rescue_seeker_type_kv

method in GameAPI

- 描述

    判断预设是否存在RESCUE_SEEKER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_type | string | 预设类型 |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_prefab_rescue_seeker_type_kv("prefab_type", unit_key, "key")
```

---

## has_unit_key_rescue_seeker_type_kv

method in GameAPI

- 描述

    判断单位编号是否存在RESCUE_SEEKER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.UnitKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.has_unit_key_rescue_seeker_type_kv(unit_key, "key")
```

---

## has_item_key_rescue_seeker_type_kv

method in GameAPI

- 描述

    判断物品编号是否存在RESCUE_SEEKER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_key | py.ItemKey | 预设编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.has_item_key_rescue_seeker_type_kv(item_key, "key")
```

---
