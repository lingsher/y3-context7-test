---
sidebarDepth: 1
---
# GameAPI (Part 6)

# 索引

Y3 编辑器 GameAPI 接口集合（第 6 部分），包含游戏核心功能。

---

| 接口 | 描述 |
| --- | --- |
| [get_destructible_key_modifier_entity_kv](#get_destructible_key_modifier_entity_kv) | 获取可破坏物编号MODIFIER_ENTITY键值对 |
| [get_tech_key_modifier_entity_kv](#get_tech_key_modifier_entity_kv) | 获取科技编号MODIFIER_ENTITY键值对 |
| [get_icon_id_modifier_entity_kv](#get_icon_id_modifier_entity_kv) | 获取图片MODIFIER_ENTITY键值对 |
| [get_physics_entity_key_modifier_entity_kv](#get_physics_entity_key_modifier_entity_kv) | 获取逻辑物理组件类型MODIFIER_ENTITY键值对 |
| [get_unit_key_modifier_type_kv](#get_unit_key_modifier_type_kv) | 获取单位编号MODIFIER_TYPE键值对 |
| [get_item_key_modifier_type_kv](#get_item_key_modifier_type_kv) | 获取物品编号MODIFIER_TYPE键值对 |
| [get_ability_key_modifier_type_kv](#get_ability_key_modifier_type_kv) | 获取技能编号MODIFIER_TYPE键值对 |
| [get_modifier_key_modifier_type_kv](#get_modifier_key_modifier_type_kv) | 获取魔法效果特效编号MODIFIER_TYPE键值对 |
| [get_projectile_key_modifier_type_kv](#get_projectile_key_modifier_type_kv) | 获取特效编号MODIFIER_TYPE键值对 |
| [get_destructible_key_modifier_type_kv](#get_destructible_key_modifier_type_kv) | 获取可破坏物编号MODIFIER_TYPE键值对 |
| [get_tech_key_modifier_type_kv](#get_tech_key_modifier_type_kv) | 获取科技编号MODIFIER_TYPE键值对 |
| [get_icon_id_modifier_type_kv](#get_icon_id_modifier_type_kv) | 获取图片MODIFIER_TYPE键值对 |
| [get_physics_entity_key_modifier_type_kv](#get_physics_entity_key_modifier_type_kv) | 获取逻辑物理组件类型MODIFIER_TYPE键值对 |
| [get_unit_key_modifier_effect_type_kv](#get_unit_key_modifier_effect_type_kv) | 获取单位编号MODIFIER_EFFECT_TYPE键值对 |
| [get_item_key_modifier_effect_type_kv](#get_item_key_modifier_effect_type_kv) | 获取物品编号MODIFIER_EFFECT_TYPE键值对 |
| [get_ability_key_modifier_effect_type_kv](#get_ability_key_modifier_effect_type_kv) | 获取技能编号MODIFIER_EFFECT_TYPE键值对 |
| [get_modifier_key_modifier_effect_type_kv](#get_modifier_key_modifier_effect_type_kv) | 获取魔法效果特效编号MODIFIER_EFFECT_TYPE键值对 |
| [get_projectile_key_modifier_effect_type_kv](#get_projectile_key_modifier_effect_type_kv) | 获取特效编号MODIFIER_EFFECT_TYPE键值对 |
| [get_destructible_key_modifier_effect_type_kv](#get_destructible_key_modifier_effect_type_kv) | 获取可破坏物编号MODIFIER_EFFECT_TYPE键值对 |
| [get_tech_key_modifier_effect_type_kv](#get_tech_key_modifier_effect_type_kv) | 获取科技编号MODIFIER_EFFECT_TYPE键值对 |
| [get_icon_id_modifier_effect_type_kv](#get_icon_id_modifier_effect_type_kv) | 获取图片MODIFIER_EFFECT_TYPE键值对 |
| [get_physics_entity_key_modifier_effect_type_kv](#get_physics_entity_key_modifier_effect_type_kv) | 获取逻辑物理组件类型MODIFIER_EFFECT_TYPE键值对 |
| [get_unit_key_modifier_kv](#get_unit_key_modifier_kv) | 获取单位编号MODIFIER键值对 |
| [get_item_key_modifier_kv](#get_item_key_modifier_kv) | 获取物品编号MODIFIER键值对 |
| [get_ability_key_modifier_kv](#get_ability_key_modifier_kv) | 获取技能编号MODIFIER键值对 |
| [get_modifier_key_modifier_kv](#get_modifier_key_modifier_kv) | 获取魔法效果特效编号MODIFIER键值对 |
| [get_projectile_key_modifier_kv](#get_projectile_key_modifier_kv) | 获取特效编号MODIFIER键值对 |
| [get_destructible_key_modifier_kv](#get_destructible_key_modifier_kv) | 获取可破坏物编号MODIFIER键值对 |
| [get_tech_key_modifier_kv](#get_tech_key_modifier_kv) | 获取科技编号MODIFIER键值对 |
| [get_icon_id_modifier_kv](#get_icon_id_modifier_kv) | 获取图片MODIFIER键值对 |
| [get_physics_entity_key_modifier_kv](#get_physics_entity_key_modifier_kv) | 获取逻辑物理组件类型MODIFIER键值对 |
| [get_unit_key_projectile_kv](#get_unit_key_projectile_kv) | 获取单位编号PROJECTILE键值对 |
| [get_item_key_projectile_kv](#get_item_key_projectile_kv) | 获取物品编号PROJECTILE键值对 |
| [get_ability_key_projectile_kv](#get_ability_key_projectile_kv) | 获取技能编号PROJECTILE键值对 |
| [get_modifier_key_projectile_kv](#get_modifier_key_projectile_kv) | 获取魔法效果特效编号PROJECTILE键值对 |
| [get_projectile_key_projectile_kv](#get_projectile_key_projectile_kv) | 获取特效编号PROJECTILE键值对 |
| [get_destructible_key_projectile_kv](#get_destructible_key_projectile_kv) | 获取可破坏物编号PROJECTILE键值对 |
| [get_tech_key_projectile_kv](#get_tech_key_projectile_kv) | 获取科技编号PROJECTILE键值对 |
| [get_icon_id_projectile_kv](#get_icon_id_projectile_kv) | 获取图片PROJECTILE键值对 |
| [get_physics_entity_key_projectile_kv](#get_physics_entity_key_projectile_kv) | 获取逻辑物理组件类型PROJECTILE键值对 |
| [get_unit_key_projectile_entity_kv](#get_unit_key_projectile_entity_kv) | 获取单位编号PROJECTILE_ENTITY键值对 |
| [get_item_key_projectile_entity_kv](#get_item_key_projectile_entity_kv) | 获取物品编号PROJECTILE_ENTITY键值对 |
| [get_ability_key_projectile_entity_kv](#get_ability_key_projectile_entity_kv) | 获取技能编号PROJECTILE_ENTITY键值对 |
| [get_modifier_key_projectile_entity_kv](#get_modifier_key_projectile_entity_kv) | 获取魔法效果特效编号PROJECTILE_ENTITY键值对 |
| [get_projectile_key_projectile_entity_kv](#get_projectile_key_projectile_entity_kv) | 获取特效编号PROJECTILE_ENTITY键值对 |
| [get_destructible_key_projectile_entity_kv](#get_destructible_key_projectile_entity_kv) | 获取可破坏物编号PROJECTILE_ENTITY键值对 |
| [get_tech_key_projectile_entity_kv](#get_tech_key_projectile_entity_kv) | 获取科技编号PROJECTILE_ENTITY键值对 |
| [get_icon_id_projectile_entity_kv](#get_icon_id_projectile_entity_kv) | 获取图片PROJECTILE_ENTITY键值对 |
| [get_physics_entity_key_projectile_entity_kv](#get_physics_entity_key_projectile_entity_kv) | 获取逻辑物理组件类型PROJECTILE_ENTITY键值对 |
| [get_unit_key_projectile_group_kv](#get_unit_key_projectile_group_kv) | 获取单位编号PROJECTILE_GROUP键值对 |
| [get_item_key_projectile_group_kv](#get_item_key_projectile_group_kv) | 获取物品编号PROJECTILE_GROUP键值对 |
| [get_ability_key_projectile_group_kv](#get_ability_key_projectile_group_kv) | 获取技能编号PROJECTILE_GROUP键值对 |
| [get_modifier_key_projectile_group_kv](#get_modifier_key_projectile_group_kv) | 获取魔法效果特效编号PROJECTILE_GROUP键值对 |
| [get_projectile_key_projectile_group_kv](#get_projectile_key_projectile_group_kv) | 获取特效编号PROJECTILE_GROUP键值对 |
| [get_destructible_key_projectile_group_kv](#get_destructible_key_projectile_group_kv) | 获取可破坏物编号PROJECTILE_GROUP键值对 |
| [get_tech_key_projectile_group_kv](#get_tech_key_projectile_group_kv) | 获取科技编号PROJECTILE_GROUP键值对 |
| [get_icon_id_projectile_group_kv](#get_icon_id_projectile_group_kv) | 获取图片PROJECTILE_GROUP键值对 |
| [get_physics_entity_key_projectile_group_kv](#get_physics_entity_key_projectile_group_kv) | 获取逻辑物理组件类型PROJECTILE_GROUP键值对 |
| [get_unit_key_destructible_entity_kv](#get_unit_key_destructible_entity_kv) | 获取单位编号DESTRUCTIBLE_ENTITY键值对 |
| [get_item_key_destructible_entity_kv](#get_item_key_destructible_entity_kv) | 获取物品编号DESTRUCTIBLE_ENTITY键值对 |
| [get_ability_key_destructible_entity_kv](#get_ability_key_destructible_entity_kv) | 获取技能编号DESTRUCTIBLE_ENTITY键值对 |
| [get_modifier_key_destructible_entity_kv](#get_modifier_key_destructible_entity_kv) | 获取魔法效果特效编号DESTRUCTIBLE_ENTITY键值对 |
| [get_projectile_key_destructible_entity_kv](#get_projectile_key_destructible_entity_kv) | 获取特效编号DESTRUCTIBLE_ENTITY键值对 |
| [get_destructible_key_destructible_entity_kv](#get_destructible_key_destructible_entity_kv) | 获取可破坏物编号DESTRUCTIBLE_ENTITY键值对 |
| [get_tech_key_destructible_entity_kv](#get_tech_key_destructible_entity_kv) | 获取科技编号DESTRUCTIBLE_ENTITY键值对 |
| [get_icon_id_destructible_entity_kv](#get_icon_id_destructible_entity_kv) | 获取图片DESTRUCTIBLE_ENTITY键值对 |
| [get_physics_entity_key_destructible_entity_kv](#get_physics_entity_key_destructible_entity_kv) | 获取逻辑物理组件类型DESTRUCTIBLE_ENTITY键值对 |
| [get_unit_key_destructible_name_kv](#get_unit_key_destructible_name_kv) | 获取单位编号DESTRUCTIBLE_NAME键值对 |
| [get_item_key_destructible_name_kv](#get_item_key_destructible_name_kv) | 获取物品编号DESTRUCTIBLE_NAME键值对 |
| [get_ability_key_destructible_name_kv](#get_ability_key_destructible_name_kv) | 获取技能编号DESTRUCTIBLE_NAME键值对 |
| [get_modifier_key_destructible_name_kv](#get_modifier_key_destructible_name_kv) | 获取魔法效果特效编号DESTRUCTIBLE_NAME键值对 |
| [get_projectile_key_destructible_name_kv](#get_projectile_key_destructible_name_kv) | 获取特效编号DESTRUCTIBLE_NAME键值对 |
| [get_destructible_key_destructible_name_kv](#get_destructible_key_destructible_name_kv) | 获取可破坏物编号DESTRUCTIBLE_NAME键值对 |
| [get_tech_key_destructible_name_kv](#get_tech_key_destructible_name_kv) | 获取科技编号DESTRUCTIBLE_NAME键值对 |
| [get_icon_id_destructible_name_kv](#get_icon_id_destructible_name_kv) | 获取图片DESTRUCTIBLE_NAME键值对 |
| [get_physics_entity_key_destructible_name_kv](#get_physics_entity_key_destructible_name_kv) | 获取逻辑物理组件类型DESTRUCTIBLE_NAME键值对 |
| [get_unit_key_sound_entity_kv](#get_unit_key_sound_entity_kv) | 获取单位编号SOUND_ENTITY键值对 |
| [get_item_key_sound_entity_kv](#get_item_key_sound_entity_kv) | 获取物品编号SOUND_ENTITY键值对 |
| [get_ability_key_sound_entity_kv](#get_ability_key_sound_entity_kv) | 获取技能编号SOUND_ENTITY键值对 |
| [get_modifier_key_sound_entity_kv](#get_modifier_key_sound_entity_kv) | 获取魔法效果特效编号SOUND_ENTITY键值对 |
| [get_projectile_key_sound_entity_kv](#get_projectile_key_sound_entity_kv) | 获取特效编号SOUND_ENTITY键值对 |
| [get_destructible_key_sound_entity_kv](#get_destructible_key_sound_entity_kv) | 获取可破坏物编号SOUND_ENTITY键值对 |
| [get_tech_key_sound_entity_kv](#get_tech_key_sound_entity_kv) | 获取科技编号SOUND_ENTITY键值对 |
| [get_icon_id_sound_entity_kv](#get_icon_id_sound_entity_kv) | 获取图片SOUND_ENTITY键值对 |
| [get_physics_entity_key_sound_entity_kv](#get_physics_entity_key_sound_entity_kv) | 获取逻辑物理组件类型SOUND_ENTITY键值对 |
| [get_unit_key_audio_key_kv](#get_unit_key_audio_key_kv) | 获取单位编号AUDIO_KEY键值对 |
| [get_item_key_audio_key_kv](#get_item_key_audio_key_kv) | 获取物品编号AUDIO_KEY键值对 |
| [get_ability_key_audio_key_kv](#get_ability_key_audio_key_kv) | 获取技能编号AUDIO_KEY键值对 |
| [get_modifier_key_audio_key_kv](#get_modifier_key_audio_key_kv) | 获取魔法效果特效编号AUDIO_KEY键值对 |
| [get_projectile_key_audio_key_kv](#get_projectile_key_audio_key_kv) | 获取特效编号AUDIO_KEY键值对 |
| [get_destructible_key_audio_key_kv](#get_destructible_key_audio_key_kv) | 获取可破坏物编号AUDIO_KEY键值对 |
| [get_tech_key_audio_key_kv](#get_tech_key_audio_key_kv) | 获取科技编号AUDIO_KEY键值对 |
| [get_icon_id_audio_key_kv](#get_icon_id_audio_key_kv) | 获取图片AUDIO_KEY键值对 |
| [get_physics_entity_key_audio_key_kv](#get_physics_entity_key_audio_key_kv) | 获取逻辑物理组件类型AUDIO_KEY键值对 |
| [get_unit_key_game_mode_kv](#get_unit_key_game_mode_kv) | 获取单位编号GAME_MODE键值对 |
| [get_item_key_game_mode_kv](#get_item_key_game_mode_kv) | 获取物品编号GAME_MODE键值对 |
| [get_ability_key_game_mode_kv](#get_ability_key_game_mode_kv) | 获取技能编号GAME_MODE键值对 |
| [get_modifier_key_game_mode_kv](#get_modifier_key_game_mode_kv) | 获取魔法效果特效编号GAME_MODE键值对 |
| [get_projectile_key_game_mode_kv](#get_projectile_key_game_mode_kv) | 获取特效编号GAME_MODE键值对 |
| [get_destructible_key_game_mode_kv](#get_destructible_key_game_mode_kv) | 获取可破坏物编号GAME_MODE键值对 |
| [get_tech_key_game_mode_kv](#get_tech_key_game_mode_kv) | 获取科技编号GAME_MODE键值对 |
| [get_icon_id_game_mode_kv](#get_icon_id_game_mode_kv) | 获取图片GAME_MODE键值对 |
| [get_physics_entity_key_game_mode_kv](#get_physics_entity_key_game_mode_kv) | 获取逻辑物理组件类型GAME_MODE键值对 |
| [get_unit_key_player_kv](#get_unit_key_player_kv) | 获取单位编号PLAYER键值对 |
| [get_item_key_player_kv](#get_item_key_player_kv) | 获取物品编号PLAYER键值对 |
| [get_ability_key_player_kv](#get_ability_key_player_kv) | 获取技能编号PLAYER键值对 |
| [get_modifier_key_player_kv](#get_modifier_key_player_kv) | 获取魔法效果特效编号PLAYER键值对 |
| [get_projectile_key_player_kv](#get_projectile_key_player_kv) | 获取特效编号PLAYER键值对 |
| [get_destructible_key_player_kv](#get_destructible_key_player_kv) | 获取可破坏物编号PLAYER键值对 |
| [get_tech_key_player_kv](#get_tech_key_player_kv) | 获取科技编号PLAYER键值对 |
| [get_icon_id_player_kv](#get_icon_id_player_kv) | 获取图片PLAYER键值对 |
| [get_physics_entity_key_player_kv](#get_physics_entity_key_player_kv) | 获取逻辑物理组件类型PLAYER键值对 |
| [get_unit_key_player_group_kv](#get_unit_key_player_group_kv) | 获取单位编号PLAYER_GROUP键值对 |
| [get_item_key_player_group_kv](#get_item_key_player_group_kv) | 获取物品编号PLAYER_GROUP键值对 |
| [get_ability_key_player_group_kv](#get_ability_key_player_group_kv) | 获取技能编号PLAYER_GROUP键值对 |
| [get_modifier_key_player_group_kv](#get_modifier_key_player_group_kv) | 获取魔法效果特效编号PLAYER_GROUP键值对 |
| [get_projectile_key_player_group_kv](#get_projectile_key_player_group_kv) | 获取特效编号PLAYER_GROUP键值对 |
| [get_destructible_key_player_group_kv](#get_destructible_key_player_group_kv) | 获取可破坏物编号PLAYER_GROUP键值对 |
| [get_tech_key_player_group_kv](#get_tech_key_player_group_kv) | 获取科技编号PLAYER_GROUP键值对 |
| [get_icon_id_player_group_kv](#get_icon_id_player_group_kv) | 获取图片PLAYER_GROUP键值对 |
| [get_physics_entity_key_player_group_kv](#get_physics_entity_key_player_group_kv) | 获取逻辑物理组件类型PLAYER_GROUP键值对 |
| [get_unit_key_role_res_key_kv](#get_unit_key_role_res_key_kv) | 获取单位编号ROLE_RES_KEY键值对 |
| [get_item_key_role_res_key_kv](#get_item_key_role_res_key_kv) | 获取物品编号ROLE_RES_KEY键值对 |
| [get_ability_key_role_res_key_kv](#get_ability_key_role_res_key_kv) | 获取技能编号ROLE_RES_KEY键值对 |
| [get_modifier_key_role_res_key_kv](#get_modifier_key_role_res_key_kv) | 获取魔法效果特效编号ROLE_RES_KEY键值对 |
| [get_projectile_key_role_res_key_kv](#get_projectile_key_role_res_key_kv) | 获取特效编号ROLE_RES_KEY键值对 |
| [get_destructible_key_role_res_key_kv](#get_destructible_key_role_res_key_kv) | 获取可破坏物编号ROLE_RES_KEY键值对 |
| [get_tech_key_role_res_key_kv](#get_tech_key_role_res_key_kv) | 获取科技编号ROLE_RES_KEY键值对 |
| [get_icon_id_role_res_key_kv](#get_icon_id_role_res_key_kv) | 获取图片ROLE_RES_KEY键值对 |
| [get_physics_entity_key_role_res_key_kv](#get_physics_entity_key_role_res_key_kv) | 获取逻辑物理组件类型ROLE_RES_KEY键值对 |
| [get_unit_key_role_status_kv](#get_unit_key_role_status_kv) | 获取单位编号ROLE_STATUS键值对 |
| [get_item_key_role_status_kv](#get_item_key_role_status_kv) | 获取物品编号ROLE_STATUS键值对 |
| [get_ability_key_role_status_kv](#get_ability_key_role_status_kv) | 获取技能编号ROLE_STATUS键值对 |
| [get_modifier_key_role_status_kv](#get_modifier_key_role_status_kv) | 获取魔法效果特效编号ROLE_STATUS键值对 |
| [get_projectile_key_role_status_kv](#get_projectile_key_role_status_kv) | 获取特效编号ROLE_STATUS键值对 |
| [get_destructible_key_role_status_kv](#get_destructible_key_role_status_kv) | 获取可破坏物编号ROLE_STATUS键值对 |
| [get_tech_key_role_status_kv](#get_tech_key_role_status_kv) | 获取科技编号ROLE_STATUS键值对 |
| [get_icon_id_role_status_kv](#get_icon_id_role_status_kv) | 获取图片ROLE_STATUS键值对 |
| [get_physics_entity_key_role_status_kv](#get_physics_entity_key_role_status_kv) | 获取逻辑物理组件类型ROLE_STATUS键值对 |
| [get_unit_key_role_type_kv](#get_unit_key_role_type_kv) | 获取单位编号ROLE_TYPE键值对 |
| [get_item_key_role_type_kv](#get_item_key_role_type_kv) | 获取物品编号ROLE_TYPE键值对 |
| [get_ability_key_role_type_kv](#get_ability_key_role_type_kv) | 获取技能编号ROLE_TYPE键值对 |
| [get_modifier_key_role_type_kv](#get_modifier_key_role_type_kv) | 获取魔法效果特效编号ROLE_TYPE键值对 |
| [get_projectile_key_role_type_kv](#get_projectile_key_role_type_kv) | 获取特效编号ROLE_TYPE键值对 |
| [get_destructible_key_role_type_kv](#get_destructible_key_role_type_kv) | 获取可破坏物编号ROLE_TYPE键值对 |
| [get_tech_key_role_type_kv](#get_tech_key_role_type_kv) | 获取科技编号ROLE_TYPE键值对 |
| [get_icon_id_role_type_kv](#get_icon_id_role_type_kv) | 获取图片ROLE_TYPE键值对 |
| [get_physics_entity_key_role_type_kv](#get_physics_entity_key_role_type_kv) | 获取逻辑物理组件类型ROLE_TYPE键值对 |
| [get_unit_key_role_relation_kv](#get_unit_key_role_relation_kv) | 获取单位编号ROLE_RELATION键值对 |
| [get_item_key_role_relation_kv](#get_item_key_role_relation_kv) | 获取物品编号ROLE_RELATION键值对 |
| [get_ability_key_role_relation_kv](#get_ability_key_role_relation_kv) | 获取技能编号ROLE_RELATION键值对 |
| [get_modifier_key_role_relation_kv](#get_modifier_key_role_relation_kv) | 获取魔法效果特效编号ROLE_RELATION键值对 |
| [get_projectile_key_role_relation_kv](#get_projectile_key_role_relation_kv) | 获取特效编号ROLE_RELATION键值对 |
| [get_destructible_key_role_relation_kv](#get_destructible_key_role_relation_kv) | 获取可破坏物编号ROLE_RELATION键值对 |
| [get_tech_key_role_relation_kv](#get_tech_key_role_relation_kv) | 获取科技编号ROLE_RELATION键值对 |
| [get_icon_id_role_relation_kv](#get_icon_id_role_relation_kv) | 获取图片ROLE_RELATION键值对 |
| [get_physics_entity_key_role_relation_kv](#get_physics_entity_key_role_relation_kv) | 获取逻辑物理组件类型ROLE_RELATION键值对 |
| [get_unit_key_team_kv](#get_unit_key_team_kv) | 获取单位编号TEAM键值对 |
| [get_item_key_team_kv](#get_item_key_team_kv) | 获取物品编号TEAM键值对 |
| [get_ability_key_team_kv](#get_ability_key_team_kv) | 获取技能编号TEAM键值对 |
| [get_modifier_key_team_kv](#get_modifier_key_team_kv) | 获取魔法效果特效编号TEAM键值对 |
| [get_projectile_key_team_kv](#get_projectile_key_team_kv) | 获取特效编号TEAM键值对 |
| [get_destructible_key_team_kv](#get_destructible_key_team_kv) | 获取可破坏物编号TEAM键值对 |
| [get_tech_key_team_kv](#get_tech_key_team_kv) | 获取科技编号TEAM键值对 |
| [get_icon_id_team_kv](#get_icon_id_team_kv) | 获取图片TEAM键值对 |
| [get_physics_entity_key_team_kv](#get_physics_entity_key_team_kv) | 获取逻辑物理组件类型TEAM键值对 |
| [get_unit_key_point_kv](#get_unit_key_point_kv) | 获取单位编号POINT键值对 |
| [get_item_key_point_kv](#get_item_key_point_kv) | 获取物品编号POINT键值对 |
| [get_ability_key_point_kv](#get_ability_key_point_kv) | 获取技能编号POINT键值对 |
| [get_modifier_key_point_kv](#get_modifier_key_point_kv) | 获取魔法效果特效编号POINT键值对 |
| [get_projectile_key_point_kv](#get_projectile_key_point_kv) | 获取特效编号POINT键值对 |
| [get_destructible_key_point_kv](#get_destructible_key_point_kv) | 获取可破坏物编号POINT键值对 |
| [get_tech_key_point_kv](#get_tech_key_point_kv) | 获取科技编号POINT键值对 |
| [get_icon_id_point_kv](#get_icon_id_point_kv) | 获取图片POINT键值对 |
| [get_physics_entity_key_point_kv](#get_physics_entity_key_point_kv) | 获取逻辑物理组件类型POINT键值对 |
| [get_unit_key_vector3_kv](#get_unit_key_vector3_kv) | 获取单位编号VECTOR3键值对 |
| [get_item_key_vector3_kv](#get_item_key_vector3_kv) | 获取物品编号VECTOR3键值对 |
| [get_ability_key_vector3_kv](#get_ability_key_vector3_kv) | 获取技能编号VECTOR3键值对 |
| [get_modifier_key_vector3_kv](#get_modifier_key_vector3_kv) | 获取魔法效果特效编号VECTOR3键值对 |
| [get_projectile_key_vector3_kv](#get_projectile_key_vector3_kv) | 获取特效编号VECTOR3键值对 |
| [get_destructible_key_vector3_kv](#get_destructible_key_vector3_kv) | 获取可破坏物编号VECTOR3键值对 |
| [get_tech_key_vector3_kv](#get_tech_key_vector3_kv) | 获取科技编号VECTOR3键值对 |
| [get_icon_id_vector3_kv](#get_icon_id_vector3_kv) | 获取图片VECTOR3键值对 |
| [get_physics_entity_key_vector3_kv](#get_physics_entity_key_vector3_kv) | 获取逻辑物理组件类型VECTOR3键值对 |
| [get_unit_key_rotation_kv](#get_unit_key_rotation_kv) | 获取单位编号ROTATION键值对 |
| [get_item_key_rotation_kv](#get_item_key_rotation_kv) | 获取物品编号ROTATION键值对 |
| [get_ability_key_rotation_kv](#get_ability_key_rotation_kv) | 获取技能编号ROTATION键值对 |
| [get_modifier_key_rotation_kv](#get_modifier_key_rotation_kv) | 获取魔法效果特效编号ROTATION键值对 |
| [get_projectile_key_rotation_kv](#get_projectile_key_rotation_kv) | 获取特效编号ROTATION键值对 |
| [get_destructible_key_rotation_kv](#get_destructible_key_rotation_kv) | 获取可破坏物编号ROTATION键值对 |
| [get_tech_key_rotation_kv](#get_tech_key_rotation_kv) | 获取科技编号ROTATION键值对 |
| [get_icon_id_rotation_kv](#get_icon_id_rotation_kv) | 获取图片ROTATION键值对 |
| [get_physics_entity_key_rotation_kv](#get_physics_entity_key_rotation_kv) | 获取逻辑物理组件类型ROTATION键值对 |
| [get_unit_key_point_list_kv](#get_unit_key_point_list_kv) | 获取单位编号POINT_LIST键值对 |
| [get_item_key_point_list_kv](#get_item_key_point_list_kv) | 获取物品编号POINT_LIST键值对 |
| [get_ability_key_point_list_kv](#get_ability_key_point_list_kv) | 获取技能编号POINT_LIST键值对 |
| [get_modifier_key_point_list_kv](#get_modifier_key_point_list_kv) | 获取魔法效果特效编号POINT_LIST键值对 |
| [get_projectile_key_point_list_kv](#get_projectile_key_point_list_kv) | 获取特效编号POINT_LIST键值对 |
| [get_destructible_key_point_list_kv](#get_destructible_key_point_list_kv) | 获取可破坏物编号POINT_LIST键值对 |
| [get_tech_key_point_list_kv](#get_tech_key_point_list_kv) | 获取科技编号POINT_LIST键值对 |
| [get_icon_id_point_list_kv](#get_icon_id_point_list_kv) | 获取图片POINT_LIST键值对 |
| [get_physics_entity_key_point_list_kv](#get_physics_entity_key_point_list_kv) | 获取逻辑物理组件类型POINT_LIST键值对 |
| [get_unit_key_rectangle_kv](#get_unit_key_rectangle_kv) | 获取单位编号RECTANGLE键值对 |
| [get_item_key_rectangle_kv](#get_item_key_rectangle_kv) | 获取物品编号RECTANGLE键值对 |
| [get_ability_key_rectangle_kv](#get_ability_key_rectangle_kv) | 获取技能编号RECTANGLE键值对 |
| [get_modifier_key_rectangle_kv](#get_modifier_key_rectangle_kv) | 获取魔法效果特效编号RECTANGLE键值对 |
| [get_projectile_key_rectangle_kv](#get_projectile_key_rectangle_kv) | 获取特效编号RECTANGLE键值对 |
| [get_destructible_key_rectangle_kv](#get_destructible_key_rectangle_kv) | 获取可破坏物编号RECTANGLE键值对 |
| [get_tech_key_rectangle_kv](#get_tech_key_rectangle_kv) | 获取科技编号RECTANGLE键值对 |
| [get_icon_id_rectangle_kv](#get_icon_id_rectangle_kv) | 获取图片RECTANGLE键值对 |
| [get_physics_entity_key_rectangle_kv](#get_physics_entity_key_rectangle_kv) | 获取逻辑物理组件类型RECTANGLE键值对 |
| [get_unit_key_round_area_kv](#get_unit_key_round_area_kv) | 获取单位编号ROUND_AREA键值对 |
| [get_item_key_round_area_kv](#get_item_key_round_area_kv) | 获取物品编号ROUND_AREA键值对 |
| [get_ability_key_round_area_kv](#get_ability_key_round_area_kv) | 获取技能编号ROUND_AREA键值对 |
| [get_modifier_key_round_area_kv](#get_modifier_key_round_area_kv) | 获取魔法效果特效编号ROUND_AREA键值对 |
| [get_projectile_key_round_area_kv](#get_projectile_key_round_area_kv) | 获取特效编号ROUND_AREA键值对 |
| [get_destructible_key_round_area_kv](#get_destructible_key_round_area_kv) | 获取可破坏物编号ROUND_AREA键值对 |
| [get_tech_key_round_area_kv](#get_tech_key_round_area_kv) | 获取科技编号ROUND_AREA键值对 |
| [get_icon_id_round_area_kv](#get_icon_id_round_area_kv) | 获取图片ROUND_AREA键值对 |
| [get_physics_entity_key_round_area_kv](#get_physics_entity_key_round_area_kv) | 获取逻辑物理组件类型ROUND_AREA键值对 |
| [get_unit_key_polygon_kv](#get_unit_key_polygon_kv) | 获取单位编号POLYGON键值对 |
| [get_item_key_polygon_kv](#get_item_key_polygon_kv) | 获取物品编号POLYGON键值对 |
| [get_ability_key_polygon_kv](#get_ability_key_polygon_kv) | 获取技能编号POLYGON键值对 |
| [get_modifier_key_polygon_kv](#get_modifier_key_polygon_kv) | 获取魔法效果特效编号POLYGON键值对 |
| [get_projectile_key_polygon_kv](#get_projectile_key_polygon_kv) | 获取特效编号POLYGON键值对 |
| [get_destructible_key_polygon_kv](#get_destructible_key_polygon_kv) | 获取可破坏物编号POLYGON键值对 |
| [get_tech_key_polygon_kv](#get_tech_key_polygon_kv) | 获取科技编号POLYGON键值对 |
| [get_icon_id_polygon_kv](#get_icon_id_polygon_kv) | 获取图片POLYGON键值对 |
| [get_physics_entity_key_polygon_kv](#get_physics_entity_key_polygon_kv) | 获取逻辑物理组件类型POLYGON键值对 |
| [get_unit_key_camera_kv](#get_unit_key_camera_kv) | 获取单位编号CAMERA键值对 |
| [get_item_key_camera_kv](#get_item_key_camera_kv) | 获取物品编号CAMERA键值对 |
| [get_ability_key_camera_kv](#get_ability_key_camera_kv) | 获取技能编号CAMERA键值对 |
| [get_modifier_key_camera_kv](#get_modifier_key_camera_kv) | 获取魔法效果特效编号CAMERA键值对 |
| [get_projectile_key_camera_kv](#get_projectile_key_camera_kv) | 获取特效编号CAMERA键值对 |
| [get_destructible_key_camera_kv](#get_destructible_key_camera_kv) | 获取可破坏物编号CAMERA键值对 |
| [get_tech_key_camera_kv](#get_tech_key_camera_kv) | 获取科技编号CAMERA键值对 |
| [get_icon_id_camera_kv](#get_icon_id_camera_kv) | 获取图片CAMERA键值对 |
| [get_physics_entity_key_camera_kv](#get_physics_entity_key_camera_kv) | 获取逻辑物理组件类型CAMERA键值对 |
| [get_unit_key_camline_kv](#get_unit_key_camline_kv) | 获取单位编号CAMLINE键值对 |
| [get_item_key_camline_kv](#get_item_key_camline_kv) | 获取物品编号CAMLINE键值对 |
| [get_ability_key_camline_kv](#get_ability_key_camline_kv) | 获取技能编号CAMLINE键值对 |
| [get_modifier_key_camline_kv](#get_modifier_key_camline_kv) | 获取魔法效果特效编号CAMLINE键值对 |
| [get_projectile_key_camline_kv](#get_projectile_key_camline_kv) | 获取特效编号CAMLINE键值对 |
| [get_destructible_key_camline_kv](#get_destructible_key_camline_kv) | 获取可破坏物编号CAMLINE键值对 |
| [get_tech_key_camline_kv](#get_tech_key_camline_kv) | 获取科技编号CAMLINE键值对 |
| [get_icon_id_camline_kv](#get_icon_id_camline_kv) | 获取图片CAMLINE键值对 |
| [get_physics_entity_key_camline_kv](#get_physics_entity_key_camline_kv) | 获取逻辑物理组件类型CAMLINE键值对 |
| [get_unit_key_point_light_kv](#get_unit_key_point_light_kv) | 获取单位编号POINT_LIGHT键值对 |
| [get_item_key_point_light_kv](#get_item_key_point_light_kv) | 获取物品编号POINT_LIGHT键值对 |
| [get_ability_key_point_light_kv](#get_ability_key_point_light_kv) | 获取技能编号POINT_LIGHT键值对 |
| [get_modifier_key_point_light_kv](#get_modifier_key_point_light_kv) | 获取魔法效果特效编号POINT_LIGHT键值对 |
| [get_projectile_key_point_light_kv](#get_projectile_key_point_light_kv) | 获取特效编号POINT_LIGHT键值对 |
| [get_destructible_key_point_light_kv](#get_destructible_key_point_light_kv) | 获取可破坏物编号POINT_LIGHT键值对 |
| [get_tech_key_point_light_kv](#get_tech_key_point_light_kv) | 获取科技编号POINT_LIGHT键值对 |
| [get_icon_id_point_light_kv](#get_icon_id_point_light_kv) | 获取图片POINT_LIGHT键值对 |
| [get_physics_entity_key_point_light_kv](#get_physics_entity_key_point_light_kv) | 获取逻辑物理组件类型POINT_LIGHT键值对 |
| [get_unit_key_spot_light_kv](#get_unit_key_spot_light_kv) | 获取单位编号SPOT_LIGHT键值对 |
| [get_item_key_spot_light_kv](#get_item_key_spot_light_kv) | 获取物品编号SPOT_LIGHT键值对 |
| [get_ability_key_spot_light_kv](#get_ability_key_spot_light_kv) | 获取技能编号SPOT_LIGHT键值对 |
| [get_modifier_key_spot_light_kv](#get_modifier_key_spot_light_kv) | 获取魔法效果特效编号SPOT_LIGHT键值对 |
| [get_projectile_key_spot_light_kv](#get_projectile_key_spot_light_kv) | 获取特效编号SPOT_LIGHT键值对 |
| [get_destructible_key_spot_light_kv](#get_destructible_key_spot_light_kv) | 获取可破坏物编号SPOT_LIGHT键值对 |
| [get_tech_key_spot_light_kv](#get_tech_key_spot_light_kv) | 获取科技编号SPOT_LIGHT键值对 |
| [get_icon_id_spot_light_kv](#get_icon_id_spot_light_kv) | 获取图片SPOT_LIGHT键值对 |
| [get_physics_entity_key_spot_light_kv](#get_physics_entity_key_spot_light_kv) | 获取逻辑物理组件类型SPOT_LIGHT键值对 |
| [get_unit_key_fog_kv](#get_unit_key_fog_kv) | 获取单位编号FOG键值对 |
| [get_item_key_fog_kv](#get_item_key_fog_kv) | 获取物品编号FOG键值对 |
| [get_ability_key_fog_kv](#get_ability_key_fog_kv) | 获取技能编号FOG键值对 |
| [get_modifier_key_fog_kv](#get_modifier_key_fog_kv) | 获取魔法效果特效编号FOG键值对 |
| [get_projectile_key_fog_kv](#get_projectile_key_fog_kv) | 获取特效编号FOG键值对 |
| [get_destructible_key_fog_kv](#get_destructible_key_fog_kv) | 获取可破坏物编号FOG键值对 |
| [get_tech_key_fog_kv](#get_tech_key_fog_kv) | 获取科技编号FOG键值对 |
| [get_icon_id_fog_kv](#get_icon_id_fog_kv) | 获取图片FOG键值对 |
| [get_physics_entity_key_fog_kv](#get_physics_entity_key_fog_kv) | 获取逻辑物理组件类型FOG键值对 |
| [get_unit_key_scene_sound_kv](#get_unit_key_scene_sound_kv) | 获取单位编号SCENE_SOUND键值对 |
| [get_item_key_scene_sound_kv](#get_item_key_scene_sound_kv) | 获取物品编号SCENE_SOUND键值对 |
| [get_ability_key_scene_sound_kv](#get_ability_key_scene_sound_kv) | 获取技能编号SCENE_SOUND键值对 |
| [get_modifier_key_scene_sound_kv](#get_modifier_key_scene_sound_kv) | 获取魔法效果特效编号SCENE_SOUND键值对 |
| [get_projectile_key_scene_sound_kv](#get_projectile_key_scene_sound_kv) | 获取特效编号SCENE_SOUND键值对 |
| [get_destructible_key_scene_sound_kv](#get_destructible_key_scene_sound_kv) | 获取可破坏物编号SCENE_SOUND键值对 |
| [get_tech_key_scene_sound_kv](#get_tech_key_scene_sound_kv) | 获取科技编号SCENE_SOUND键值对 |
| [get_icon_id_scene_sound_kv](#get_icon_id_scene_sound_kv) | 获取图片SCENE_SOUND键值对 |
| [get_physics_entity_key_scene_sound_kv](#get_physics_entity_key_scene_sound_kv) | 获取逻辑物理组件类型SCENE_SOUND键值对 |
| [get_unit_key_model_kv](#get_unit_key_model_kv) | 获取单位编号MODEL键值对 |
| [get_item_key_model_kv](#get_item_key_model_kv) | 获取物品编号MODEL键值对 |
| [get_ability_key_model_kv](#get_ability_key_model_kv) | 获取技能编号MODEL键值对 |
| [get_modifier_key_model_kv](#get_modifier_key_model_kv) | 获取魔法效果特效编号MODEL键值对 |
| [get_projectile_key_model_kv](#get_projectile_key_model_kv) | 获取特效编号MODEL键值对 |
| [get_destructible_key_model_kv](#get_destructible_key_model_kv) | 获取可破坏物编号MODEL键值对 |
| [get_tech_key_model_kv](#get_tech_key_model_kv) | 获取科技编号MODEL键值对 |
| [get_icon_id_model_kv](#get_icon_id_model_kv) | 获取图片MODEL键值对 |
| [get_physics_entity_key_model_kv](#get_physics_entity_key_model_kv) | 获取逻辑物理组件类型MODEL键值对 |
| [get_unit_key_sfx_entity_kv](#get_unit_key_sfx_entity_kv) | 获取单位编号SFX_ENTITY键值对 |
| [get_item_key_sfx_entity_kv](#get_item_key_sfx_entity_kv) | 获取物品编号SFX_ENTITY键值对 |
| [get_ability_key_sfx_entity_kv](#get_ability_key_sfx_entity_kv) | 获取技能编号SFX_ENTITY键值对 |
| [get_modifier_key_sfx_entity_kv](#get_modifier_key_sfx_entity_kv) | 获取魔法效果特效编号SFX_ENTITY键值对 |
| [get_projectile_key_sfx_entity_kv](#get_projectile_key_sfx_entity_kv) | 获取特效编号SFX_ENTITY键值对 |
| [get_destructible_key_sfx_entity_kv](#get_destructible_key_sfx_entity_kv) | 获取可破坏物编号SFX_ENTITY键值对 |
| [get_tech_key_sfx_entity_kv](#get_tech_key_sfx_entity_kv) | 获取科技编号SFX_ENTITY键值对 |
| [get_icon_id_sfx_entity_kv](#get_icon_id_sfx_entity_kv) | 获取图片SFX_ENTITY键值对 |
| [get_physics_entity_key_sfx_entity_kv](#get_physics_entity_key_sfx_entity_kv) | 获取逻辑物理组件类型SFX_ENTITY键值对 |
| [get_unit_key_sfx_key_kv](#get_unit_key_sfx_key_kv) | 获取单位编号SFX_KEY键值对 |
| [get_item_key_sfx_key_kv](#get_item_key_sfx_key_kv) | 获取物品编号SFX_KEY键值对 |
| [get_ability_key_sfx_key_kv](#get_ability_key_sfx_key_kv) | 获取技能编号SFX_KEY键值对 |
| [get_modifier_key_sfx_key_kv](#get_modifier_key_sfx_key_kv) | 获取魔法效果特效编号SFX_KEY键值对 |
| [get_projectile_key_sfx_key_kv](#get_projectile_key_sfx_key_kv) | 获取特效编号SFX_KEY键值对 |
| [get_destructible_key_sfx_key_kv](#get_destructible_key_sfx_key_kv) | 获取可破坏物编号SFX_KEY键值对 |
| [get_tech_key_sfx_key_kv](#get_tech_key_sfx_key_kv) | 获取科技编号SFX_KEY键值对 |
| [get_icon_id_sfx_key_kv](#get_icon_id_sfx_key_kv) | 获取图片SFX_KEY键值对 |
| [get_physics_entity_key_sfx_key_kv](#get_physics_entity_key_sfx_key_kv) | 获取逻辑物理组件类型SFX_KEY键值对 |
| [get_unit_key_link_sfx_entity_kv](#get_unit_key_link_sfx_entity_kv) | 获取单位编号LINK_SFX_ENTITY键值对 |
| [get_item_key_link_sfx_entity_kv](#get_item_key_link_sfx_entity_kv) | 获取物品编号LINK_SFX_ENTITY键值对 |
| [get_ability_key_link_sfx_entity_kv](#get_ability_key_link_sfx_entity_kv) | 获取技能编号LINK_SFX_ENTITY键值对 |
| [get_modifier_key_link_sfx_entity_kv](#get_modifier_key_link_sfx_entity_kv) | 获取魔法效果特效编号LINK_SFX_ENTITY键值对 |
| [get_projectile_key_link_sfx_entity_kv](#get_projectile_key_link_sfx_entity_kv) | 获取特效编号LINK_SFX_ENTITY键值对 |
| [get_destructible_key_link_sfx_entity_kv](#get_destructible_key_link_sfx_entity_kv) | 获取可破坏物编号LINK_SFX_ENTITY键值对 |
| [get_tech_key_link_sfx_entity_kv](#get_tech_key_link_sfx_entity_kv) | 获取科技编号LINK_SFX_ENTITY键值对 |
| [get_icon_id_link_sfx_entity_kv](#get_icon_id_link_sfx_entity_kv) | 获取图片LINK_SFX_ENTITY键值对 |
| [get_physics_entity_key_link_sfx_entity_kv](#get_physics_entity_key_link_sfx_entity_kv) | 获取逻辑物理组件类型LINK_SFX_ENTITY键值对 |
| [get_unit_key_link_sfx_key_kv](#get_unit_key_link_sfx_key_kv) | 获取单位编号LINK_SFX_KEY键值对 |
| [get_item_key_link_sfx_key_kv](#get_item_key_link_sfx_key_kv) | 获取物品编号LINK_SFX_KEY键值对 |
| [get_ability_key_link_sfx_key_kv](#get_ability_key_link_sfx_key_kv) | 获取技能编号LINK_SFX_KEY键值对 |
| [get_modifier_key_link_sfx_key_kv](#get_modifier_key_link_sfx_key_kv) | 获取魔法效果特效编号LINK_SFX_KEY键值对 |
| [get_projectile_key_link_sfx_key_kv](#get_projectile_key_link_sfx_key_kv) | 获取特效编号LINK_SFX_KEY键值对 |
| [get_destructible_key_link_sfx_key_kv](#get_destructible_key_link_sfx_key_kv) | 获取可破坏物编号LINK_SFX_KEY键值对 |
| [get_tech_key_link_sfx_key_kv](#get_tech_key_link_sfx_key_kv) | 获取科技编号LINK_SFX_KEY键值对 |
| [get_icon_id_link_sfx_key_kv](#get_icon_id_link_sfx_key_kv) | 获取图片LINK_SFX_KEY键值对 |
| [get_physics_entity_key_link_sfx_key_kv](#get_physics_entity_key_link_sfx_key_kv) | 获取逻辑物理组件类型LINK_SFX_KEY键值对 |
| [get_unit_key_cursor_key_kv](#get_unit_key_cursor_key_kv) | 获取单位编号CURSOR_KEY键值对 |
| [get_item_key_cursor_key_kv](#get_item_key_cursor_key_kv) | 获取物品编号CURSOR_KEY键值对 |
| [get_ability_key_cursor_key_kv](#get_ability_key_cursor_key_kv) | 获取技能编号CURSOR_KEY键值对 |
| [get_modifier_key_cursor_key_kv](#get_modifier_key_cursor_key_kv) | 获取魔法效果特效编号CURSOR_KEY键值对 |
| [get_projectile_key_cursor_key_kv](#get_projectile_key_cursor_key_kv) | 获取特效编号CURSOR_KEY键值对 |
| [get_destructible_key_cursor_key_kv](#get_destructible_key_cursor_key_kv) | 获取可破坏物编号CURSOR_KEY键值对 |
| [get_tech_key_cursor_key_kv](#get_tech_key_cursor_key_kv) | 获取科技编号CURSOR_KEY键值对 |
| [get_icon_id_cursor_key_kv](#get_icon_id_cursor_key_kv) | 获取图片CURSOR_KEY键值对 |
| [get_physics_entity_key_cursor_key_kv](#get_physics_entity_key_cursor_key_kv) | 获取逻辑物理组件类型CURSOR_KEY键值对 |
| [get_unit_key_angle_kv](#get_unit_key_angle_kv) | 获取单位编号ANGLE键值对 |
| [get_item_key_angle_kv](#get_item_key_angle_kv) | 获取物品编号ANGLE键值对 |
| [get_ability_key_angle_kv](#get_ability_key_angle_kv) | 获取技能编号ANGLE键值对 |
| [get_modifier_key_angle_kv](#get_modifier_key_angle_kv) | 获取魔法效果特效编号ANGLE键值对 |
| [get_projectile_key_angle_kv](#get_projectile_key_angle_kv) | 获取特效编号ANGLE键值对 |
| [get_destructible_key_angle_kv](#get_destructible_key_angle_kv) | 获取可破坏物编号ANGLE键值对 |
| [get_tech_key_angle_kv](#get_tech_key_angle_kv) | 获取科技编号ANGLE键值对 |
| [get_icon_id_angle_kv](#get_icon_id_angle_kv) | 获取图片ANGLE键值对 |
| [get_physics_entity_key_angle_kv](#get_physics_entity_key_angle_kv) | 获取逻辑物理组件类型ANGLE键值对 |
| [get_unit_key_texture_kv](#get_unit_key_texture_kv) | 获取单位编号TEXTURE键值对 |
| [get_item_key_texture_kv](#get_item_key_texture_kv) | 获取物品编号TEXTURE键值对 |
| [get_ability_key_texture_kv](#get_ability_key_texture_kv) | 获取技能编号TEXTURE键值对 |
| [get_modifier_key_texture_kv](#get_modifier_key_texture_kv) | 获取魔法效果特效编号TEXTURE键值对 |
| [get_projectile_key_texture_kv](#get_projectile_key_texture_kv) | 获取特效编号TEXTURE键值对 |
| [get_destructible_key_texture_kv](#get_destructible_key_texture_kv) | 获取可破坏物编号TEXTURE键值对 |
| [get_tech_key_texture_kv](#get_tech_key_texture_kv) | 获取科技编号TEXTURE键值对 |
| [get_icon_id_texture_kv](#get_icon_id_texture_kv) | 获取图片TEXTURE键值对 |
| [get_physics_entity_key_texture_kv](#get_physics_entity_key_texture_kv) | 获取逻辑物理组件类型TEXTURE键值对 |
| [get_unit_key_sequence_kv](#get_unit_key_sequence_kv) | 获取单位编号SEQUENCE键值对 |
| [get_item_key_sequence_kv](#get_item_key_sequence_kv) | 获取物品编号SEQUENCE键值对 |
| [get_ability_key_sequence_kv](#get_ability_key_sequence_kv) | 获取技能编号SEQUENCE键值对 |
| [get_modifier_key_sequence_kv](#get_modifier_key_sequence_kv) | 获取魔法效果特效编号SEQUENCE键值对 |
| [get_projectile_key_sequence_kv](#get_projectile_key_sequence_kv) | 获取特效编号SEQUENCE键值对 |
| [get_destructible_key_sequence_kv](#get_destructible_key_sequence_kv) | 获取可破坏物编号SEQUENCE键值对 |
| [get_tech_key_sequence_kv](#get_tech_key_sequence_kv) | 获取科技编号SEQUENCE键值对 |
| [get_icon_id_sequence_kv](#get_icon_id_sequence_kv) | 获取图片SEQUENCE键值对 |
| [get_physics_entity_key_sequence_kv](#get_physics_entity_key_sequence_kv) | 获取逻辑物理组件类型SEQUENCE键值对 |
| [get_unit_key_physics_object_kv](#get_unit_key_physics_object_kv) | 获取单位编号PHYSICS_OBJECT键值对 |
| [get_item_key_physics_object_kv](#get_item_key_physics_object_kv) | 获取物品编号PHYSICS_OBJECT键值对 |
| [get_ability_key_physics_object_kv](#get_ability_key_physics_object_kv) | 获取技能编号PHYSICS_OBJECT键值对 |
| [get_modifier_key_physics_object_kv](#get_modifier_key_physics_object_kv) | 获取魔法效果特效编号PHYSICS_OBJECT键值对 |
| [get_projectile_key_physics_object_kv](#get_projectile_key_physics_object_kv) | 获取特效编号PHYSICS_OBJECT键值对 |
| [get_destructible_key_physics_object_kv](#get_destructible_key_physics_object_kv) | 获取可破坏物编号PHYSICS_OBJECT键值对 |
| [get_tech_key_physics_object_kv](#get_tech_key_physics_object_kv) | 获取科技编号PHYSICS_OBJECT键值对 |
| [get_icon_id_physics_object_kv](#get_icon_id_physics_object_kv) | 获取图片PHYSICS_OBJECT键值对 |
| [get_physics_entity_key_physics_object_kv](#get_physics_entity_key_physics_object_kv) | 获取逻辑物理组件类型PHYSICS_OBJECT键值对 |
| [get_unit_key_physics_entity_kv](#get_unit_key_physics_entity_kv) | 获取单位编号PHYSICS_ENTITY键值对 |
| [get_item_key_physics_entity_kv](#get_item_key_physics_entity_kv) | 获取物品编号PHYSICS_ENTITY键值对 |
| [get_ability_key_physics_entity_kv](#get_ability_key_physics_entity_kv) | 获取技能编号PHYSICS_ENTITY键值对 |
| [get_modifier_key_physics_entity_kv](#get_modifier_key_physics_entity_kv) | 获取魔法效果特效编号PHYSICS_ENTITY键值对 |
| [get_projectile_key_physics_entity_kv](#get_projectile_key_physics_entity_kv) | 获取特效编号PHYSICS_ENTITY键值对 |
| [get_destructible_key_physics_entity_kv](#get_destructible_key_physics_entity_kv) | 获取可破坏物编号PHYSICS_ENTITY键值对 |
| [get_tech_key_physics_entity_kv](#get_tech_key_physics_entity_kv) | 获取科技编号PHYSICS_ENTITY键值对 |
| [get_icon_id_physics_entity_kv](#get_icon_id_physics_entity_kv) | 获取图片PHYSICS_ENTITY键值对 |
| [get_physics_entity_key_physics_entity_kv](#get_physics_entity_key_physics_entity_kv) | 获取逻辑物理组件类型PHYSICS_ENTITY键值对 |
| [get_unit_key_physics_object_key_kv](#get_unit_key_physics_object_key_kv) | 获取单位编号PHYSICS_OBJECT_KEY键值对 |
| [get_item_key_physics_object_key_kv](#get_item_key_physics_object_key_kv) | 获取物品编号PHYSICS_OBJECT_KEY键值对 |
| [get_ability_key_physics_object_key_kv](#get_ability_key_physics_object_key_kv) | 获取技能编号PHYSICS_OBJECT_KEY键值对 |
| [get_modifier_key_physics_object_key_kv](#get_modifier_key_physics_object_key_kv) | 获取魔法效果特效编号PHYSICS_OBJECT_KEY键值对 |
| [get_projectile_key_physics_object_key_kv](#get_projectile_key_physics_object_key_kv) | 获取特效编号PHYSICS_OBJECT_KEY键值对 |
| [get_destructible_key_physics_object_key_kv](#get_destructible_key_physics_object_key_kv) | 获取可破坏物编号PHYSICS_OBJECT_KEY键值对 |
| [get_tech_key_physics_object_key_kv](#get_tech_key_physics_object_key_kv) | 获取科技编号PHYSICS_OBJECT_KEY键值对 |
| [get_icon_id_physics_object_key_kv](#get_icon_id_physics_object_key_kv) | 获取图片PHYSICS_OBJECT_KEY键值对 |
| [get_physics_entity_key_physics_object_key_kv](#get_physics_entity_key_physics_object_key_kv) | 获取逻辑物理组件类型PHYSICS_OBJECT_KEY键值对 |
| [get_unit_key_physics_entity_key_kv](#get_unit_key_physics_entity_key_kv) | 获取单位编号PHYSICS_ENTITY_KEY键值对 |
| [get_item_key_physics_entity_key_kv](#get_item_key_physics_entity_key_kv) | 获取物品编号PHYSICS_ENTITY_KEY键值对 |
| [get_ability_key_physics_entity_key_kv](#get_ability_key_physics_entity_key_kv) | 获取技能编号PHYSICS_ENTITY_KEY键值对 |
| [get_modifier_key_physics_entity_key_kv](#get_modifier_key_physics_entity_key_kv) | 获取魔法效果特效编号PHYSICS_ENTITY_KEY键值对 |
| [get_projectile_key_physics_entity_key_kv](#get_projectile_key_physics_entity_key_kv) | 获取特效编号PHYSICS_ENTITY_KEY键值对 |
| [get_destructible_key_physics_entity_key_kv](#get_destructible_key_physics_entity_key_kv) | 获取可破坏物编号PHYSICS_ENTITY_KEY键值对 |
| [get_tech_key_physics_entity_key_kv](#get_tech_key_physics_entity_key_kv) | 获取科技编号PHYSICS_ENTITY_KEY键值对 |
| [get_icon_id_physics_entity_key_kv](#get_icon_id_physics_entity_key_kv) | 获取图片PHYSICS_ENTITY_KEY键值对 |
| [get_physics_entity_key_physics_entity_key_kv](#get_physics_entity_key_physics_entity_key_kv) | 获取逻辑物理组件类型PHYSICS_ENTITY_KEY键值对 |
| [get_unit_key_rigid_body_kv](#get_unit_key_rigid_body_kv) | 获取单位编号RIGID_BODY键值对 |
| [get_item_key_rigid_body_kv](#get_item_key_rigid_body_kv) | 获取物品编号RIGID_BODY键值对 |
| [get_ability_key_rigid_body_kv](#get_ability_key_rigid_body_kv) | 获取技能编号RIGID_BODY键值对 |
| [get_modifier_key_rigid_body_kv](#get_modifier_key_rigid_body_kv) | 获取魔法效果特效编号RIGID_BODY键值对 |
| [get_projectile_key_rigid_body_kv](#get_projectile_key_rigid_body_kv) | 获取特效编号RIGID_BODY键值对 |
| [get_destructible_key_rigid_body_kv](#get_destructible_key_rigid_body_kv) | 获取可破坏物编号RIGID_BODY键值对 |
| [get_tech_key_rigid_body_kv](#get_tech_key_rigid_body_kv) | 获取科技编号RIGID_BODY键值对 |
| [get_icon_id_rigid_body_kv](#get_icon_id_rigid_body_kv) | 获取图片RIGID_BODY键值对 |
| [get_physics_entity_key_rigid_body_kv](#get_physics_entity_key_rigid_body_kv) | 获取逻辑物理组件类型RIGID_BODY键值对 |
| [get_unit_key_rigid_body_group_kv](#get_unit_key_rigid_body_group_kv) | 获取单位编号RIGID_BODY_GROUP键值对 |
| [get_item_key_rigid_body_group_kv](#get_item_key_rigid_body_group_kv) | 获取物品编号RIGID_BODY_GROUP键值对 |
| [get_ability_key_rigid_body_group_kv](#get_ability_key_rigid_body_group_kv) | 获取技能编号RIGID_BODY_GROUP键值对 |
| [get_modifier_key_rigid_body_group_kv](#get_modifier_key_rigid_body_group_kv) | 获取魔法效果特效编号RIGID_BODY_GROUP键值对 |
| [get_projectile_key_rigid_body_group_kv](#get_projectile_key_rigid_body_group_kv) | 获取特效编号RIGID_BODY_GROUP键值对 |
| [get_destructible_key_rigid_body_group_kv](#get_destructible_key_rigid_body_group_kv) | 获取可破坏物编号RIGID_BODY_GROUP键值对 |
| [get_tech_key_rigid_body_group_kv](#get_tech_key_rigid_body_group_kv) | 获取科技编号RIGID_BODY_GROUP键值对 |
| [get_icon_id_rigid_body_group_kv](#get_icon_id_rigid_body_group_kv) | 获取图片RIGID_BODY_GROUP键值对 |
| [get_physics_entity_key_rigid_body_group_kv](#get_physics_entity_key_rigid_body_group_kv) | 获取逻辑物理组件类型RIGID_BODY_GROUP键值对 |
| [get_unit_key_collider_kv](#get_unit_key_collider_kv) | 获取单位编号COLLIDER键值对 |
| [get_item_key_collider_kv](#get_item_key_collider_kv) | 获取物品编号COLLIDER键值对 |
| [get_ability_key_collider_kv](#get_ability_key_collider_kv) | 获取技能编号COLLIDER键值对 |
| [get_modifier_key_collider_kv](#get_modifier_key_collider_kv) | 获取魔法效果特效编号COLLIDER键值对 |
| [get_projectile_key_collider_kv](#get_projectile_key_collider_kv) | 获取特效编号COLLIDER键值对 |
| [get_destructible_key_collider_kv](#get_destructible_key_collider_kv) | 获取可破坏物编号COLLIDER键值对 |
| [get_tech_key_collider_kv](#get_tech_key_collider_kv) | 获取科技编号COLLIDER键值对 |
| [get_icon_id_collider_kv](#get_icon_id_collider_kv) | 获取图片COLLIDER键值对 |
| [get_physics_entity_key_collider_kv](#get_physics_entity_key_collider_kv) | 获取逻辑物理组件类型COLLIDER键值对 |
| [get_unit_key_joint_kv](#get_unit_key_joint_kv) | 获取单位编号JOINT键值对 |
| [get_item_key_joint_kv](#get_item_key_joint_kv) | 获取物品编号JOINT键值对 |
| [get_ability_key_joint_kv](#get_ability_key_joint_kv) | 获取技能编号JOINT键值对 |
| [get_modifier_key_joint_kv](#get_modifier_key_joint_kv) | 获取魔法效果特效编号JOINT键值对 |
| [get_projectile_key_joint_kv](#get_projectile_key_joint_kv) | 获取特效编号JOINT键值对 |
| [get_destructible_key_joint_kv](#get_destructible_key_joint_kv) | 获取可破坏物编号JOINT键值对 |
| [get_tech_key_joint_kv](#get_tech_key_joint_kv) | 获取科技编号JOINT键值对 |
| [get_icon_id_joint_kv](#get_icon_id_joint_kv) | 获取图片JOINT键值对 |
| [get_physics_entity_key_joint_kv](#get_physics_entity_key_joint_kv) | 获取逻辑物理组件类型JOINT键值对 |
| [get_unit_key_reaction_kv](#get_unit_key_reaction_kv) | 获取单位编号REACTION键值对 |
| [get_item_key_reaction_kv](#get_item_key_reaction_kv) | 获取物品编号REACTION键值对 |
| [get_ability_key_reaction_kv](#get_ability_key_reaction_kv) | 获取技能编号REACTION键值对 |
| [get_modifier_key_reaction_kv](#get_modifier_key_reaction_kv) | 获取魔法效果特效编号REACTION键值对 |
| [get_projectile_key_reaction_kv](#get_projectile_key_reaction_kv) | 获取特效编号REACTION键值对 |
| [get_destructible_key_reaction_kv](#get_destructible_key_reaction_kv) | 获取可破坏物编号REACTION键值对 |
| [get_tech_key_reaction_kv](#get_tech_key_reaction_kv) | 获取科技编号REACTION键值对 |
| [get_icon_id_reaction_kv](#get_icon_id_reaction_kv) | 获取图片REACTION键值对 |
| [get_physics_entity_key_reaction_kv](#get_physics_entity_key_reaction_kv) | 获取逻辑物理组件类型REACTION键值对 |
| [get_unit_key_reaction_group_kv](#get_unit_key_reaction_group_kv) | 获取单位编号REACTION_GROUP键值对 |
| [get_item_key_reaction_group_kv](#get_item_key_reaction_group_kv) | 获取物品编号REACTION_GROUP键值对 |
| [get_ability_key_reaction_group_kv](#get_ability_key_reaction_group_kv) | 获取技能编号REACTION_GROUP键值对 |
| [get_modifier_key_reaction_group_kv](#get_modifier_key_reaction_group_kv) | 获取魔法效果特效编号REACTION_GROUP键值对 |
| [get_projectile_key_reaction_group_kv](#get_projectile_key_reaction_group_kv) | 获取特效编号REACTION_GROUP键值对 |
| [get_destructible_key_reaction_group_kv](#get_destructible_key_reaction_group_kv) | 获取可破坏物编号REACTION_GROUP键值对 |
| [get_tech_key_reaction_group_kv](#get_tech_key_reaction_group_kv) | 获取科技编号REACTION_GROUP键值对 |
| [get_icon_id_reaction_group_kv](#get_icon_id_reaction_group_kv) | 获取图片REACTION_GROUP键值对 |
| [get_physics_entity_key_reaction_group_kv](#get_physics_entity_key_reaction_group_kv) | 获取逻辑物理组件类型REACTION_GROUP键值对 |
| [get_unit_key_dynamic_trigger_instance_kv](#get_unit_key_dynamic_trigger_instance_kv) | 获取单位编号DYNAMIC_TRIGGER_INSTANCE键值对 |
| [get_item_key_dynamic_trigger_instance_kv](#get_item_key_dynamic_trigger_instance_kv) | 获取物品编号DYNAMIC_TRIGGER_INSTANCE键值对 |
| [get_ability_key_dynamic_trigger_instance_kv](#get_ability_key_dynamic_trigger_instance_kv) | 获取技能编号DYNAMIC_TRIGGER_INSTANCE键值对 |
| [get_modifier_key_dynamic_trigger_instance_kv](#get_modifier_key_dynamic_trigger_instance_kv) | 获取魔法效果特效编号DYNAMIC_TRIGGER_INSTANCE键值对 |
| [get_projectile_key_dynamic_trigger_instance_kv](#get_projectile_key_dynamic_trigger_instance_kv) | 获取特效编号DYNAMIC_TRIGGER_INSTANCE键值对 |
| [get_destructible_key_dynamic_trigger_instance_kv](#get_destructible_key_dynamic_trigger_instance_kv) | 获取可破坏物编号DYNAMIC_TRIGGER_INSTANCE键值对 |
| [get_tech_key_dynamic_trigger_instance_kv](#get_tech_key_dynamic_trigger_instance_kv) | 获取科技编号DYNAMIC_TRIGGER_INSTANCE键值对 |
| [get_icon_id_dynamic_trigger_instance_kv](#get_icon_id_dynamic_trigger_instance_kv) | 获取图片DYNAMIC_TRIGGER_INSTANCE键值对 |
| [get_physics_entity_key_dynamic_trigger_instance_kv](#get_physics_entity_key_dynamic_trigger_instance_kv) | 获取逻辑物理组件类型DYNAMIC_TRIGGER_INSTANCE键值对 |
| [get_unit_key_table_kv](#get_unit_key_table_kv) | 获取单位编号TABLE键值对 |
| [get_item_key_table_kv](#get_item_key_table_kv) | 获取物品编号TABLE键值对 |
| [get_ability_key_table_kv](#get_ability_key_table_kv) | 获取技能编号TABLE键值对 |
| [get_modifier_key_table_kv](#get_modifier_key_table_kv) | 获取魔法效果特效编号TABLE键值对 |
| [get_projectile_key_table_kv](#get_projectile_key_table_kv) | 获取特效编号TABLE键值对 |
| [get_destructible_key_table_kv](#get_destructible_key_table_kv) | 获取可破坏物编号TABLE键值对 |
| [get_tech_key_table_kv](#get_tech_key_table_kv) | 获取科技编号TABLE键值对 |
| [get_icon_id_table_kv](#get_icon_id_table_kv) | 获取图片TABLE键值对 |
| [get_physics_entity_key_table_kv](#get_physics_entity_key_table_kv) | 获取逻辑物理组件类型TABLE键值对 |
| [get_unit_key_random_pool_kv](#get_unit_key_random_pool_kv) | 获取单位编号RANDOM_POOL键值对 |
| [get_item_key_random_pool_kv](#get_item_key_random_pool_kv) | 获取物品编号RANDOM_POOL键值对 |
| [get_ability_key_random_pool_kv](#get_ability_key_random_pool_kv) | 获取技能编号RANDOM_POOL键值对 |
| [get_modifier_key_random_pool_kv](#get_modifier_key_random_pool_kv) | 获取魔法效果特效编号RANDOM_POOL键值对 |
| [get_projectile_key_random_pool_kv](#get_projectile_key_random_pool_kv) | 获取特效编号RANDOM_POOL键值对 |
| [get_destructible_key_random_pool_kv](#get_destructible_key_random_pool_kv) | 获取可破坏物编号RANDOM_POOL键值对 |
| [get_tech_key_random_pool_kv](#get_tech_key_random_pool_kv) | 获取科技编号RANDOM_POOL键值对 |
| [get_icon_id_random_pool_kv](#get_icon_id_random_pool_kv) | 获取图片RANDOM_POOL键值对 |
| [get_physics_entity_key_random_pool_kv](#get_physics_entity_key_random_pool_kv) | 获取逻辑物理组件类型RANDOM_POOL键值对 |
| [get_unit_key_scene_ui_kv](#get_unit_key_scene_ui_kv) | 获取单位编号SCENE_UI键值对 |
| [get_item_key_scene_ui_kv](#get_item_key_scene_ui_kv) | 获取物品编号SCENE_UI键值对 |
| [get_ability_key_scene_ui_kv](#get_ability_key_scene_ui_kv) | 获取技能编号SCENE_UI键值对 |
| [get_modifier_key_scene_ui_kv](#get_modifier_key_scene_ui_kv) | 获取魔法效果特效编号SCENE_UI键值对 |
| [get_projectile_key_scene_ui_kv](#get_projectile_key_scene_ui_kv) | 获取特效编号SCENE_UI键值对 |
| [get_destructible_key_scene_ui_kv](#get_destructible_key_scene_ui_kv) | 获取可破坏物编号SCENE_UI键值对 |
| [get_tech_key_scene_ui_kv](#get_tech_key_scene_ui_kv) | 获取科技编号SCENE_UI键值对 |
| [get_icon_id_scene_ui_kv](#get_icon_id_scene_ui_kv) | 获取图片SCENE_UI键值对 |
| [get_physics_entity_key_scene_ui_kv](#get_physics_entity_key_scene_ui_kv) | 获取逻辑物理组件类型SCENE_UI键值对 |
| [get_unit_key_damage_type_kv](#get_unit_key_damage_type_kv) | 获取单位编号DAMAGE_TYPE键值对 |
| [get_item_key_damage_type_kv](#get_item_key_damage_type_kv) | 获取物品编号DAMAGE_TYPE键值对 |
| [get_ability_key_damage_type_kv](#get_ability_key_damage_type_kv) | 获取技能编号DAMAGE_TYPE键值对 |
| [get_modifier_key_damage_type_kv](#get_modifier_key_damage_type_kv) | 获取魔法效果特效编号DAMAGE_TYPE键值对 |
| [get_projectile_key_damage_type_kv](#get_projectile_key_damage_type_kv) | 获取特效编号DAMAGE_TYPE键值对 |
| [get_destructible_key_damage_type_kv](#get_destructible_key_damage_type_kv) | 获取可破坏物编号DAMAGE_TYPE键值对 |
| [get_tech_key_damage_type_kv](#get_tech_key_damage_type_kv) | 获取科技编号DAMAGE_TYPE键值对 |
| [get_icon_id_damage_type_kv](#get_icon_id_damage_type_kv) | 获取图片DAMAGE_TYPE键值对 |
| [get_physics_entity_key_damage_type_kv](#get_physics_entity_key_damage_type_kv) | 获取逻辑物理组件类型DAMAGE_TYPE键值对 |
| [get_unit_key_harm_text_type_new_kv](#get_unit_key_harm_text_type_new_kv) | 获取单位编号HARM_TEXT_TYPE_NEW键值对 |
| [get_item_key_harm_text_type_new_kv](#get_item_key_harm_text_type_new_kv) | 获取物品编号HARM_TEXT_TYPE_NEW键值对 |
| [get_ability_key_harm_text_type_new_kv](#get_ability_key_harm_text_type_new_kv) | 获取技能编号HARM_TEXT_TYPE_NEW键值对 |
| [get_modifier_key_harm_text_type_new_kv](#get_modifier_key_harm_text_type_new_kv) | 获取魔法效果特效编号HARM_TEXT_TYPE_NEW键值对 |
| [get_projectile_key_harm_text_type_new_kv](#get_projectile_key_harm_text_type_new_kv) | 获取特效编号HARM_TEXT_TYPE_NEW键值对 |
| [get_destructible_key_harm_text_type_new_kv](#get_destructible_key_harm_text_type_new_kv) | 获取可破坏物编号HARM_TEXT_TYPE_NEW键值对 |
| [get_tech_key_harm_text_type_new_kv](#get_tech_key_harm_text_type_new_kv) | 获取科技编号HARM_TEXT_TYPE_NEW键值对 |
| [get_icon_id_harm_text_type_new_kv](#get_icon_id_harm_text_type_new_kv) | 获取图片HARM_TEXT_TYPE_NEW键值对 |
| [get_physics_entity_key_harm_text_type_new_kv](#get_physics_entity_key_harm_text_type_new_kv) | 获取逻辑物理组件类型HARM_TEXT_TYPE_NEW键值对 |
| [get_unit_key_font_type_kv](#get_unit_key_font_type_kv) | 获取单位编号FONT_TYPE键值对 |
| [get_item_key_font_type_kv](#get_item_key_font_type_kv) | 获取物品编号FONT_TYPE键值对 |
| [get_ability_key_font_type_kv](#get_ability_key_font_type_kv) | 获取技能编号FONT_TYPE键值对 |
| [get_modifier_key_font_type_kv](#get_modifier_key_font_type_kv) | 获取魔法效果特效编号FONT_TYPE键值对 |
| [get_projectile_key_font_type_kv](#get_projectile_key_font_type_kv) | 获取特效编号FONT_TYPE键值对 |
| [get_destructible_key_font_type_kv](#get_destructible_key_font_type_kv) | 获取可破坏物编号FONT_TYPE键值对 |
| [get_tech_key_font_type_kv](#get_tech_key_font_type_kv) | 获取科技编号FONT_TYPE键值对 |
| [get_icon_id_font_type_kv](#get_icon_id_font_type_kv) | 获取图片FONT_TYPE键值对 |
| [get_physics_entity_key_font_type_kv](#get_physics_entity_key_font_type_kv) | 获取逻辑物理组件类型FONT_TYPE键值对 |
| [get_unit_key_jump_word_track_kv](#get_unit_key_jump_word_track_kv) | 获取单位编号JUMP_WORD_TRACK键值对 |
| [get_item_key_jump_word_track_kv](#get_item_key_jump_word_track_kv) | 获取物品编号JUMP_WORD_TRACK键值对 |
| [get_ability_key_jump_word_track_kv](#get_ability_key_jump_word_track_kv) | 获取技能编号JUMP_WORD_TRACK键值对 |
| [get_modifier_key_jump_word_track_kv](#get_modifier_key_jump_word_track_kv) | 获取魔法效果特效编号JUMP_WORD_TRACK键值对 |
| [get_projectile_key_jump_word_track_kv](#get_projectile_key_jump_word_track_kv) | 获取特效编号JUMP_WORD_TRACK键值对 |
| [get_destructible_key_jump_word_track_kv](#get_destructible_key_jump_word_track_kv) | 获取可破坏物编号JUMP_WORD_TRACK键值对 |
| [get_tech_key_jump_word_track_kv](#get_tech_key_jump_word_track_kv) | 获取科技编号JUMP_WORD_TRACK键值对 |
| [get_icon_id_jump_word_track_kv](#get_icon_id_jump_word_track_kv) | 获取图片JUMP_WORD_TRACK键值对 |
| [get_physics_entity_key_jump_word_track_kv](#get_physics_entity_key_jump_word_track_kv) | 获取逻辑物理组件类型JUMP_WORD_TRACK键值对 |
| [get_unit_key_new_timer_kv](#get_unit_key_new_timer_kv) | 获取单位编号NEW_TIMER键值对 |
| [get_item_key_new_timer_kv](#get_item_key_new_timer_kv) | 获取物品编号NEW_TIMER键值对 |
| [get_ability_key_new_timer_kv](#get_ability_key_new_timer_kv) | 获取技能编号NEW_TIMER键值对 |
| [get_modifier_key_new_timer_kv](#get_modifier_key_new_timer_kv) | 获取魔法效果特效编号NEW_TIMER键值对 |
| [get_projectile_key_new_timer_kv](#get_projectile_key_new_timer_kv) | 获取特效编号NEW_TIMER键值对 |
| [get_destructible_key_new_timer_kv](#get_destructible_key_new_timer_kv) | 获取可破坏物编号NEW_TIMER键值对 |
| [get_tech_key_new_timer_kv](#get_tech_key_new_timer_kv) | 获取科技编号NEW_TIMER键值对 |
| [get_icon_id_new_timer_kv](#get_icon_id_new_timer_kv) | 获取图片NEW_TIMER键值对 |
| [get_physics_entity_key_new_timer_kv](#get_physics_entity_key_new_timer_kv) | 获取逻辑物理组件类型NEW_TIMER键值对 |
| [get_unit_key_tech_key_kv](#get_unit_key_tech_key_kv) | 获取单位编号TECH_KEY键值对 |
| [get_item_key_tech_key_kv](#get_item_key_tech_key_kv) | 获取物品编号TECH_KEY键值对 |
| [get_ability_key_tech_key_kv](#get_ability_key_tech_key_kv) | 获取技能编号TECH_KEY键值对 |
| [get_modifier_key_tech_key_kv](#get_modifier_key_tech_key_kv) | 获取魔法效果特效编号TECH_KEY键值对 |
| [get_projectile_key_tech_key_kv](#get_projectile_key_tech_key_kv) | 获取特效编号TECH_KEY键值对 |
| [get_destructible_key_tech_key_kv](#get_destructible_key_tech_key_kv) | 获取可破坏物编号TECH_KEY键值对 |
| [get_tech_key_tech_key_kv](#get_tech_key_tech_key_kv) | 获取科技编号TECH_KEY键值对 |
| [get_icon_id_tech_key_kv](#get_icon_id_tech_key_kv) | 获取图片TECH_KEY键值对 |
| [get_physics_entity_key_tech_key_kv](#get_physics_entity_key_tech_key_kv) | 获取逻辑物理组件类型TECH_KEY键值对 |
| [get_unit_key_store_key_kv](#get_unit_key_store_key_kv) | 获取单位编号STORE_KEY键值对 |
| [get_item_key_store_key_kv](#get_item_key_store_key_kv) | 获取物品编号STORE_KEY键值对 |
| [get_ability_key_store_key_kv](#get_ability_key_store_key_kv) | 获取技能编号STORE_KEY键值对 |
| [get_modifier_key_store_key_kv](#get_modifier_key_store_key_kv) | 获取魔法效果特效编号STORE_KEY键值对 |
| [get_projectile_key_store_key_kv](#get_projectile_key_store_key_kv) | 获取特效编号STORE_KEY键值对 |
| [get_destructible_key_store_key_kv](#get_destructible_key_store_key_kv) | 获取可破坏物编号STORE_KEY键值对 |
| [get_tech_key_store_key_kv](#get_tech_key_store_key_kv) | 获取科技编号STORE_KEY键值对 |
| [get_icon_id_store_key_kv](#get_icon_id_store_key_kv) | 获取图片STORE_KEY键值对 |
| [get_physics_entity_key_store_key_kv](#get_physics_entity_key_store_key_kv) | 获取逻辑物理组件类型STORE_KEY键值对 |
| [get_unit_key_keyboard_key_kv](#get_unit_key_keyboard_key_kv) | 获取单位编号KEYBOARD_KEY键值对 |
| [get_item_key_keyboard_key_kv](#get_item_key_keyboard_key_kv) | 获取物品编号KEYBOARD_KEY键值对 |
| [get_ability_key_keyboard_key_kv](#get_ability_key_keyboard_key_kv) | 获取技能编号KEYBOARD_KEY键值对 |
| [get_modifier_key_keyboard_key_kv](#get_modifier_key_keyboard_key_kv) | 获取魔法效果特效编号KEYBOARD_KEY键值对 |
| [get_projectile_key_keyboard_key_kv](#get_projectile_key_keyboard_key_kv) | 获取特效编号KEYBOARD_KEY键值对 |
| [get_destructible_key_keyboard_key_kv](#get_destructible_key_keyboard_key_kv) | 获取可破坏物编号KEYBOARD_KEY键值对 |
| [get_tech_key_keyboard_key_kv](#get_tech_key_keyboard_key_kv) | 获取科技编号KEYBOARD_KEY键值对 |
| [get_icon_id_keyboard_key_kv](#get_icon_id_keyboard_key_kv) | 获取图片KEYBOARD_KEY键值对 |
| [get_physics_entity_key_keyboard_key_kv](#get_physics_entity_key_keyboard_key_kv) | 获取逻辑物理组件类型KEYBOARD_KEY键值对 |
| [get_unit_key_func_keyboard_key_kv](#get_unit_key_func_keyboard_key_kv) | 获取单位编号FUNC_KEYBOARD_KEY键值对 |
| [get_item_key_func_keyboard_key_kv](#get_item_key_func_keyboard_key_kv) | 获取物品编号FUNC_KEYBOARD_KEY键值对 |
| [get_ability_key_func_keyboard_key_kv](#get_ability_key_func_keyboard_key_kv) | 获取技能编号FUNC_KEYBOARD_KEY键值对 |
| [get_modifier_key_func_keyboard_key_kv](#get_modifier_key_func_keyboard_key_kv) | 获取魔法效果特效编号FUNC_KEYBOARD_KEY键值对 |
| [get_projectile_key_func_keyboard_key_kv](#get_projectile_key_func_keyboard_key_kv) | 获取特效编号FUNC_KEYBOARD_KEY键值对 |
| [get_destructible_key_func_keyboard_key_kv](#get_destructible_key_func_keyboard_key_kv) | 获取可破坏物编号FUNC_KEYBOARD_KEY键值对 |
| [get_tech_key_func_keyboard_key_kv](#get_tech_key_func_keyboard_key_kv) | 获取科技编号FUNC_KEYBOARD_KEY键值对 |
| [get_icon_id_func_keyboard_key_kv](#get_icon_id_func_keyboard_key_kv) | 获取图片FUNC_KEYBOARD_KEY键值对 |
| [get_physics_entity_key_func_keyboard_key_kv](#get_physics_entity_key_func_keyboard_key_kv) | 获取逻辑物理组件类型FUNC_KEYBOARD_KEY键值对 |
| [get_unit_key_mouse_key_kv](#get_unit_key_mouse_key_kv) | 获取单位编号MOUSE_KEY键值对 |
| [get_item_key_mouse_key_kv](#get_item_key_mouse_key_kv) | 获取物品编号MOUSE_KEY键值对 |
| [get_ability_key_mouse_key_kv](#get_ability_key_mouse_key_kv) | 获取技能编号MOUSE_KEY键值对 |
| [get_modifier_key_mouse_key_kv](#get_modifier_key_mouse_key_kv) | 获取魔法效果特效编号MOUSE_KEY键值对 |
| [get_projectile_key_mouse_key_kv](#get_projectile_key_mouse_key_kv) | 获取特效编号MOUSE_KEY键值对 |
| [get_destructible_key_mouse_key_kv](#get_destructible_key_mouse_key_kv) | 获取可破坏物编号MOUSE_KEY键值对 |
| [get_tech_key_mouse_key_kv](#get_tech_key_mouse_key_kv) | 获取科技编号MOUSE_KEY键值对 |
| [get_icon_id_mouse_key_kv](#get_icon_id_mouse_key_kv) | 获取图片MOUSE_KEY键值对 |
| [get_physics_entity_key_mouse_key_kv](#get_physics_entity_key_mouse_key_kv) | 获取逻辑物理组件类型MOUSE_KEY键值对 |
| [get_unit_key_mouse_wheel_kv](#get_unit_key_mouse_wheel_kv) | 获取单位编号MOUSE_WHEEL键值对 |
| [get_item_key_mouse_wheel_kv](#get_item_key_mouse_wheel_kv) | 获取物品编号MOUSE_WHEEL键值对 |
| [get_ability_key_mouse_wheel_kv](#get_ability_key_mouse_wheel_kv) | 获取技能编号MOUSE_WHEEL键值对 |
| [get_modifier_key_mouse_wheel_kv](#get_modifier_key_mouse_wheel_kv) | 获取魔法效果特效编号MOUSE_WHEEL键值对 |
| [get_projectile_key_mouse_wheel_kv](#get_projectile_key_mouse_wheel_kv) | 获取特效编号MOUSE_WHEEL键值对 |
| [get_destructible_key_mouse_wheel_kv](#get_destructible_key_mouse_wheel_kv) | 获取可破坏物编号MOUSE_WHEEL键值对 |
| [get_tech_key_mouse_wheel_kv](#get_tech_key_mouse_wheel_kv) | 获取科技编号MOUSE_WHEEL键值对 |
| [get_icon_id_mouse_wheel_kv](#get_icon_id_mouse_wheel_kv) | 获取图片MOUSE_WHEEL键值对 |
| [get_physics_entity_key_mouse_wheel_kv](#get_physics_entity_key_mouse_wheel_kv) | 获取逻辑物理组件类型MOUSE_WHEEL键值对 |
| [get_unit_key_post_effect_kv](#get_unit_key_post_effect_kv) | 获取单位编号POST_EFFECT键值对 |
| [get_item_key_post_effect_kv](#get_item_key_post_effect_kv) | 获取物品编号POST_EFFECT键值对 |
| [get_ability_key_post_effect_kv](#get_ability_key_post_effect_kv) | 获取技能编号POST_EFFECT键值对 |
| [get_modifier_key_post_effect_kv](#get_modifier_key_post_effect_kv) | 获取魔法效果特效编号POST_EFFECT键值对 |
| [get_projectile_key_post_effect_kv](#get_projectile_key_post_effect_kv) | 获取特效编号POST_EFFECT键值对 |
| [get_destructible_key_post_effect_kv](#get_destructible_key_post_effect_kv) | 获取可破坏物编号POST_EFFECT键值对 |
| [get_tech_key_post_effect_kv](#get_tech_key_post_effect_kv) | 获取科技编号POST_EFFECT键值对 |
| [get_icon_id_post_effect_kv](#get_icon_id_post_effect_kv) | 获取图片POST_EFFECT键值对 |
| [get_physics_entity_key_post_effect_kv](#get_physics_entity_key_post_effect_kv) | 获取逻辑物理组件类型POST_EFFECT键值对 |
| [get_unit_key_unit_type_kv](#get_unit_key_unit_type_kv) | 获取单位编号UNIT_TYPE键值对 |
| [get_item_key_unit_type_kv](#get_item_key_unit_type_kv) | 获取物品编号UNIT_TYPE键值对 |
| [get_ability_key_unit_type_kv](#get_ability_key_unit_type_kv) | 获取技能编号UNIT_TYPE键值对 |
| [get_modifier_key_unit_type_kv](#get_modifier_key_unit_type_kv) | 获取魔法效果特效编号UNIT_TYPE键值对 |
| [get_projectile_key_unit_type_kv](#get_projectile_key_unit_type_kv) | 获取特效编号UNIT_TYPE键值对 |
| [get_destructible_key_unit_type_kv](#get_destructible_key_unit_type_kv) | 获取可破坏物编号UNIT_TYPE键值对 |
| [get_tech_key_unit_type_kv](#get_tech_key_unit_type_kv) | 获取科技编号UNIT_TYPE键值对 |
| [get_icon_id_unit_type_kv](#get_icon_id_unit_type_kv) | 获取图片UNIT_TYPE键值对 |
| [get_physics_entity_key_unit_type_kv](#get_physics_entity_key_unit_type_kv) | 获取逻辑物理组件类型UNIT_TYPE键值对 |
| [get_unit_key_unit_command_type_kv](#get_unit_key_unit_command_type_kv) | 获取单位编号UNIT_COMMAND_TYPE键值对 |
| [get_item_key_unit_command_type_kv](#get_item_key_unit_command_type_kv) | 获取物品编号UNIT_COMMAND_TYPE键值对 |
| [get_ability_key_unit_command_type_kv](#get_ability_key_unit_command_type_kv) | 获取技能编号UNIT_COMMAND_TYPE键值对 |
| [get_modifier_key_unit_command_type_kv](#get_modifier_key_unit_command_type_kv) | 获取魔法效果特效编号UNIT_COMMAND_TYPE键值对 |
| [get_projectile_key_unit_command_type_kv](#get_projectile_key_unit_command_type_kv) | 获取特效编号UNIT_COMMAND_TYPE键值对 |
| [get_destructible_key_unit_command_type_kv](#get_destructible_key_unit_command_type_kv) | 获取可破坏物编号UNIT_COMMAND_TYPE键值对 |
| [get_tech_key_unit_command_type_kv](#get_tech_key_unit_command_type_kv) | 获取科技编号UNIT_COMMAND_TYPE键值对 |
| [get_icon_id_unit_command_type_kv](#get_icon_id_unit_command_type_kv) | 获取图片UNIT_COMMAND_TYPE键值对 |
| [get_physics_entity_key_unit_command_type_kv](#get_physics_entity_key_unit_command_type_kv) | 获取逻辑物理组件类型UNIT_COMMAND_TYPE键值对 |
| [get_unit_key_mini_map_color_type_kv](#get_unit_key_mini_map_color_type_kv) | 获取单位编号MINI_MAP_COLOR_TYPE键值对 |
| [get_item_key_mini_map_color_type_kv](#get_item_key_mini_map_color_type_kv) | 获取物品编号MINI_MAP_COLOR_TYPE键值对 |
| [get_ability_key_mini_map_color_type_kv](#get_ability_key_mini_map_color_type_kv) | 获取技能编号MINI_MAP_COLOR_TYPE键值对 |
| [get_modifier_key_mini_map_color_type_kv](#get_modifier_key_mini_map_color_type_kv) | 获取魔法效果特效编号MINI_MAP_COLOR_TYPE键值对 |
| [get_projectile_key_mini_map_color_type_kv](#get_projectile_key_mini_map_color_type_kv) | 获取特效编号MINI_MAP_COLOR_TYPE键值对 |
| [get_destructible_key_mini_map_color_type_kv](#get_destructible_key_mini_map_color_type_kv) | 获取可破坏物编号MINI_MAP_COLOR_TYPE键值对 |
| [get_tech_key_mini_map_color_type_kv](#get_tech_key_mini_map_color_type_kv) | 获取科技编号MINI_MAP_COLOR_TYPE键值对 |
| [get_icon_id_mini_map_color_type_kv](#get_icon_id_mini_map_color_type_kv) | 获取图片MINI_MAP_COLOR_TYPE键值对 |
| [get_physics_entity_key_mini_map_color_type_kv](#get_physics_entity_key_mini_map_color_type_kv) | 获取逻辑物理组件类型MINI_MAP_COLOR_TYPE键值对 |
| [get_unit_key_unit_behavior_kv](#get_unit_key_unit_behavior_kv) | 获取单位编号UNIT_BEHAVIOR键值对 |
| [get_item_key_unit_behavior_kv](#get_item_key_unit_behavior_kv) | 获取物品编号UNIT_BEHAVIOR键值对 |
| [get_ability_key_unit_behavior_kv](#get_ability_key_unit_behavior_kv) | 获取技能编号UNIT_BEHAVIOR键值对 |
| [get_modifier_key_unit_behavior_kv](#get_modifier_key_unit_behavior_kv) | 获取魔法效果特效编号UNIT_BEHAVIOR键值对 |
| [get_projectile_key_unit_behavior_kv](#get_projectile_key_unit_behavior_kv) | 获取特效编号UNIT_BEHAVIOR键值对 |
| [get_destructible_key_unit_behavior_kv](#get_destructible_key_unit_behavior_kv) | 获取可破坏物编号UNIT_BEHAVIOR键值对 |
| [get_tech_key_unit_behavior_kv](#get_tech_key_unit_behavior_kv) | 获取科技编号UNIT_BEHAVIOR键值对 |
| [get_icon_id_unit_behavior_kv](#get_icon_id_unit_behavior_kv) | 获取图片UNIT_BEHAVIOR键值对 |
| [get_physics_entity_key_unit_behavior_kv](#get_physics_entity_key_unit_behavior_kv) | 获取逻辑物理组件类型UNIT_BEHAVIOR键值对 |
| [get_unit_key_curved_path_kv](#get_unit_key_curved_path_kv) | 获取单位编号CURVED_PATH键值对 |
| [get_item_key_curved_path_kv](#get_item_key_curved_path_kv) | 获取物品编号CURVED_PATH键值对 |
| [get_ability_key_curved_path_kv](#get_ability_key_curved_path_kv) | 获取技能编号CURVED_PATH键值对 |
| [get_modifier_key_curved_path_kv](#get_modifier_key_curved_path_kv) | 获取魔法效果特效编号CURVED_PATH键值对 |
| [get_projectile_key_curved_path_kv](#get_projectile_key_curved_path_kv) | 获取特效编号CURVED_PATH键值对 |
| [get_destructible_key_curved_path_kv](#get_destructible_key_curved_path_kv) | 获取可破坏物编号CURVED_PATH键值对 |
| [get_tech_key_curved_path_kv](#get_tech_key_curved_path_kv) | 获取科技编号CURVED_PATH键值对 |
| [get_icon_id_curved_path_kv](#get_icon_id_curved_path_kv) | 获取图片CURVED_PATH键值对 |
| [get_physics_entity_key_curved_path_kv](#get_physics_entity_key_curved_path_kv) | 获取逻辑物理组件类型CURVED_PATH键值对 |
| [get_unit_key_curved_path_3d_kv](#get_unit_key_curved_path_3d_kv) | 获取单位编号CURVED_PATH_3D键值对 |
| [get_item_key_curved_path_3d_kv](#get_item_key_curved_path_3d_kv) | 获取物品编号CURVED_PATH_3D键值对 |
| [get_ability_key_curved_path_3d_kv](#get_ability_key_curved_path_3d_kv) | 获取技能编号CURVED_PATH_3D键值对 |
| [get_modifier_key_curved_path_3d_kv](#get_modifier_key_curved_path_3d_kv) | 获取魔法效果特效编号CURVED_PATH_3D键值对 |
| [get_projectile_key_curved_path_3d_kv](#get_projectile_key_curved_path_3d_kv) | 获取特效编号CURVED_PATH_3D键值对 |
| [get_destructible_key_curved_path_3d_kv](#get_destructible_key_curved_path_3d_kv) | 获取可破坏物编号CURVED_PATH_3D键值对 |
| [get_tech_key_curved_path_3d_kv](#get_tech_key_curved_path_3d_kv) | 获取科技编号CURVED_PATH_3D键值对 |
| [get_icon_id_curved_path_3d_kv](#get_icon_id_curved_path_3d_kv) | 获取图片CURVED_PATH_3D键值对 |
| [get_physics_entity_key_curved_path_3d_kv](#get_physics_entity_key_curved_path_3d_kv) | 获取逻辑物理组件类型CURVED_PATH_3D键值对 |
| [set_coin_currency_list_value](#set_coin_currency_list_value) | 设置COIN_CURRENCY数组中某项 |
| [get_coin_currency_n_list](#get_coin_currency_n_list) | 生成n个值为v的COIN_CURRENCY数组 |
| [get_map_list_value](#get_map_list_value) | 获取MAP数组中某项 |
| [set_map_list_value](#set_map_list_value) | 设置MAP数组中某项 |
| [get_map_n_list](#get_map_n_list) | 生成n个值为v的MAP数组 |
| [get_ui_equip_slot_use_type_list_value](#get_ui_equip_slot_use_type_list_value) | 获取UI_EQUIP_SLOT_USE_TYPE数组中某项 |
| [set_ui_equip_slot_use_type_list_value](#set_ui_equip_slot_use_type_list_value) | 设置UI_EQUIP_SLOT_USE_TYPE数组中某项 |
| [get_ui_equip_slot_use_type_n_list](#get_ui_equip_slot_use_type_n_list) | 生成n个值为v的UI_EQUIP_SLOT_USE_TYPE数组 |
| [get_ui_equip_slot_drag_type_list_value](#get_ui_equip_slot_drag_type_list_value) | 获取UI_EQUIP_SLOT_DRAG_TYPE数组中某项 |
| [set_ui_equip_slot_drag_type_list_value](#set_ui_equip_slot_drag_type_list_value) | 设置UI_EQUIP_SLOT_DRAG_TYPE数组中某项 |
| [get_ui_equip_slot_drag_type_n_list](#get_ui_equip_slot_drag_type_n_list) | 生成n个值为v的UI_EQUIP_SLOT_DRAG_TYPE数组 |
| [get_live2d_list_value](#get_live2d_list_value) | 获取LIVE2D数组中某项 |
| [set_live2d_list_value](#set_live2d_list_value) | 设置LIVE2D数组中某项 |
| [get_live2d_n_list](#get_live2d_n_list) | 生成n个值为v的LIVE2D数组 |
| [get_ui_text_over_length_handling_type_list_value](#get_ui_text_over_length_handling_type_list_value) | 获取UI_TEXT_OVER_LENGTH_HANDLING_TYPE数组中某项 |
| [set_ui_text_over_length_handling_type_list_value](#set_ui_text_over_length_handling_type_list_value) | 设置UI_TEXT_OVER_LENGTH_HANDLING_TYPE数组中某项 |
| [get_ui_text_over_length_handling_type_n_list](#get_ui_text_over_length_handling_type_n_list) | 生成n个值为v的UI_TEXT_OVER_LENGTH_HANDLING_TYPE数组 |
| [get_ui_layout_clipping_type_list_value](#get_ui_layout_clipping_type_list_value) | 获取UI_LAYOUT_CLIPPING_TYPE数组中某项 |
| [set_ui_layout_clipping_type_list_value](#set_ui_layout_clipping_type_list_value) | 设置UI_LAYOUT_CLIPPING_TYPE数组中某项 |
| [get_ui_layout_clipping_type_n_list](#get_ui_layout_clipping_type_n_list) | 生成n个值为v的UI_LAYOUT_CLIPPING_TYPE数组 |
| [get_ui_gridview_type_list_value](#get_ui_gridview_type_list_value) | 获取UI_GRIDVIEW_TYPE数组中某项 |
| [set_ui_gridview_type_list_value](#set_ui_gridview_type_list_value) | 设置UI_GRIDVIEW_TYPE数组中某项 |
| [get_ui_gridview_type_n_list](#get_ui_gridview_type_n_list) | 生成n个值为v的UI_GRIDVIEW_TYPE数组 |
| [get_ui_gridview_bar_type_list_value](#get_ui_gridview_bar_type_list_value) | 获取UI_GRIDVIEW_BAR_TYPE数组中某项 |
| [set_ui_gridview_bar_type_list_value](#set_ui_gridview_bar_type_list_value) | 设置UI_GRIDVIEW_BAR_TYPE数组中某项 |
| [get_ui_gridview_bar_type_n_list](#get_ui_gridview_bar_type_n_list) | 生成n个值为v的UI_GRIDVIEW_BAR_TYPE数组 |
| [get_ui_effect_camera_mode_list_value](#get_ui_effect_camera_mode_list_value) | 获取UI_EFFECT_CAMERA_MODE数组中某项 |
| [set_ui_effect_camera_mode_list_value](#set_ui_effect_camera_mode_list_value) | 设置UI_EFFECT_CAMERA_MODE数组中某项 |
| [get_ui_effect_camera_mode_n_list](#get_ui_effect_camera_mode_n_list) | 生成n个值为v的UI_EFFECT_CAMERA_MODE数组 |
| [get_ui_pos_adapt_mode_list_value](#get_ui_pos_adapt_mode_list_value) | 获取UI_POS_ADAPT_MODE数组中某项 |
| [set_ui_pos_adapt_mode_list_value](#set_ui_pos_adapt_mode_list_value) | 设置UI_POS_ADAPT_MODE数组中某项 |
| [get_ui_pos_adapt_mode_n_list](#get_ui_pos_adapt_mode_n_list) | 生成n个值为v的UI_POS_ADAPT_MODE数组 |
| [get_goods_key_list_value](#get_goods_key_list_value) | 获取GOODS_KEY数组中某项 |
| [set_goods_key_list_value](#set_goods_key_list_value) | 设置GOODS_KEY数组中某项 |
| [get_goods_key_n_list](#get_goods_key_n_list) | 生成n个值为v的GOODS_KEY数组 |
| [get_ui_chat_send_channel_list_value](#get_ui_chat_send_channel_list_value) | 获取UI_CHAT_SEND_CHANNEL数组中某项 |
| [set_ui_chat_send_channel_list_value](#set_ui_chat_send_channel_list_value) | 设置UI_CHAT_SEND_CHANNEL数组中某项 |
| [get_ui_chat_send_channel_n_list](#get_ui_chat_send_channel_n_list) | 生成n个值为v的UI_CHAT_SEND_CHANNEL数组 |
| [get_ui_chat_recv_channel_list_value](#get_ui_chat_recv_channel_list_value) | 获取UI_CHAT_RECV_CHANNEL数组中某项 |
| [set_ui_chat_recv_channel_list_value](#set_ui_chat_recv_channel_list_value) | 设置UI_CHAT_RECV_CHANNEL数组中某项 |
| [get_ui_chat_recv_channel_n_list](#get_ui_chat_recv_channel_n_list) | 生成n个值为v的UI_CHAT_RECV_CHANNEL数组 |
| [get_attach_model_entity_list_value](#get_attach_model_entity_list_value) | 获取ATTACH_MODEL_ENTITY数组中某项 |
| [set_attach_model_entity_list_value](#set_attach_model_entity_list_value) | 设置ATTACH_MODEL_ENTITY数组中某项 |
| [get_attach_model_entity_n_list](#get_attach_model_entity_n_list) | 生成n个值为v的ATTACH_MODEL_ENTITY数组 |
| [set_unit_key_ui_gridview_type_kv](#set_unit_key_ui_gridview_type_kv) | 预设库 添加UI_GRIDVIEW_TYPE键值对 |
| [set_unit_key_ui_gridview_bar_type_kv](#set_unit_key_ui_gridview_bar_type_kv) | 预设库 添加UI_GRIDVIEW_BAR_TYPE键值对 |
| [set_unit_key_ui_effect_camera_mode_kv](#set_unit_key_ui_effect_camera_mode_kv) | 预设库 添加UI_EFFECT_CAMERA_MODE键值对 |
| [set_unit_key_ui_equip_slot_use_type_kv](#set_unit_key_ui_equip_slot_use_type_kv) | 预设库 添加UI_EQUIP_SLOT_USE_TYPE键值对 |
| [set_unit_key_ui_equip_slot_drag_type_kv](#set_unit_key_ui_equip_slot_drag_type_kv) | 预设库 添加UI_EQUIP_SLOT_DRAG_TYPE键值对 |
| [set_unit_key_ui_layout_clipping_type_kv](#set_unit_key_ui_layout_clipping_type_kv) | 预设库 添加UI_LAYOUT_CLIPPING_TYPE键值对 |
| [set_unit_key_ui_text_over_length_handling_type_kv](#set_unit_key_ui_text_over_length_handling_type_kv) | 预设库 添加UI_TEXT_OVER_LENGTH_HANDLING_TYPE键值对 |
| [set_unit_key_ui_pos_adapt_mode_kv](#set_unit_key_ui_pos_adapt_mode_kv) | 预设库 添加UI_POS_ADAPT_MODE键值对 |
| [set_unit_key_ui_chat_send_channel_kv](#set_unit_key_ui_chat_send_channel_kv) | 预设库 添加UI_CHAT_SEND_CHANNEL键值对 |
| [set_unit_key_ui_chat_recv_channel_kv](#set_unit_key_ui_chat_recv_channel_kv) | 预设库 添加UI_CHAT_RECV_CHANNEL键值对 |
| [set_unit_key_ui_anim_play_mode_kv](#set_unit_key_ui_anim_play_mode_kv) | 预设库 添加UI_ANIM_PLAY_MODE键值对 |
| [set_unit_key_ui_text_font_name_kv](#set_unit_key_ui_text_font_name_kv) | 预设库 添加UI_TEXT_FONT_NAME键值对 |
| [set_unit_key_ui_eca_anim_type_kv](#set_unit_key_ui_eca_anim_type_kv) | 预设库 添加UI_ECA_ANIM_TYPE键值对 |
| [set_unit_key_local_unit_group_kv](#set_unit_key_local_unit_group_kv) | 预设库 添加LOCAL_UNIT_GROUP键值对 |
| [set_unit_key_damage_attack_type_kv](#set_unit_key_damage_attack_type_kv) | 预设库 添加DAMAGE_ATTACK_TYPE键值对 |
| [set_unit_key_damage_armor_type_kv](#set_unit_key_damage_armor_type_kv) | 预设库 添加DAMAGE_ARMOR_TYPE键值对 |
| [set_unit_key_item_stack_type_kv](#set_unit_key_item_stack_type_kv) | 预设库 添加ITEM_STACK_TYPE键值对 |
| [set_unit_key_ability_release_id_kv](#set_unit_key_ability_release_id_kv) | 预设库 添加ABILITY_RELEASE_ID键值对 |
| [set_unit_key_slot_type_kv](#set_unit_key_slot_type_kv) | 预设库 添加SLOT_TYPE键值对 |
| [set_unit_key_ui_point_kv](#set_unit_key_ui_point_kv) | 预设库 添加UI_POINT键值对 |
| [set_unit_key_attach_model_entity_kv](#set_unit_key_attach_model_entity_kv) | 预设库 添加ATTACH_MODEL_ENTITY键值对 |
| [set_unit_key_live2d_kv](#set_unit_key_live2d_kv) | 预设库 添加LIVE2D键值对 |
| [set_unit_key_spine_kv](#set_unit_key_spine_kv) | 预设库 添加SPINE键值对 |
| [set_unit_key_force_entity_kv](#set_unit_key_force_entity_kv) | 预设库 添加FORCE_ENTITY键值对 |
| [set_unit_key_goods_key_kv](#set_unit_key_goods_key_kv) | 预设库 添加GOODS_KEY键值对 |
| [set_unit_key_mouse_key_without_middle_kv](#set_unit_key_mouse_key_without_middle_kv) | 预设库 添加MOUSE_KEY_WITHOUT_MIDDLE键值对 |
| [set_unit_key_map_kv](#set_unit_key_map_kv) | 预设库 添加MAP键值对 |
| [set_unit_key_unit_group_command_type_kv](#set_unit_key_unit_group_command_type_kv) | 预设库 添加UNIT_GROUP_COMMAND_TYPE键值对 |
| [set_unit_key_rescue_seeker_type_kv](#set_unit_key_rescue_seeker_type_kv) | 预设库 添加RESCUE_SEEKER_TYPE键值对 |
| [set_unit_key_rescuer_type_kv](#set_unit_key_rescuer_type_kv) | 预设库 添加RESCUER_TYPE键值对 |
| [set_unit_key_store_item_type_kv](#set_unit_key_store_item_type_kv) | 预设库 添加STORE_ITEM_TYPE键值对 |
| [set_unit_key_site_state_kv](#set_unit_key_site_state_kv) | 预设库 添加SITE_STATE键值对 |
| [set_unit_key_coin_currency_kv](#set_unit_key_coin_currency_kv) | 预设库 添加COIN_CURRENCY键值对 |
| [set_item_key_ui_gridview_type_kv](#set_item_key_ui_gridview_type_kv) | 预设库 添加UI_GRIDVIEW_TYPE键值对 |
| [set_item_key_ui_gridview_bar_type_kv](#set_item_key_ui_gridview_bar_type_kv) | 预设库 添加UI_GRIDVIEW_BAR_TYPE键值对 |
| [set_item_key_ui_effect_camera_mode_kv](#set_item_key_ui_effect_camera_mode_kv) | 预设库 添加UI_EFFECT_CAMERA_MODE键值对 |
| [set_item_key_ui_equip_slot_use_type_kv](#set_item_key_ui_equip_slot_use_type_kv) | 预设库 添加UI_EQUIP_SLOT_USE_TYPE键值对 |
| [set_item_key_ui_equip_slot_drag_type_kv](#set_item_key_ui_equip_slot_drag_type_kv) | 预设库 添加UI_EQUIP_SLOT_DRAG_TYPE键值对 |
| [set_item_key_ui_layout_clipping_type_kv](#set_item_key_ui_layout_clipping_type_kv) | 预设库 添加UI_LAYOUT_CLIPPING_TYPE键值对 |
| [set_item_key_ui_text_over_length_handling_type_kv](#set_item_key_ui_text_over_length_handling_type_kv) | 预设库 添加UI_TEXT_OVER_LENGTH_HANDLING_TYPE键值对 |
| [set_item_key_ui_pos_adapt_mode_kv](#set_item_key_ui_pos_adapt_mode_kv) | 预设库 添加UI_POS_ADAPT_MODE键值对 |
| [set_item_key_ui_chat_send_channel_kv](#set_item_key_ui_chat_send_channel_kv) | 预设库 添加UI_CHAT_SEND_CHANNEL键值对 |
| [set_item_key_ui_chat_recv_channel_kv](#set_item_key_ui_chat_recv_channel_kv) | 预设库 添加UI_CHAT_RECV_CHANNEL键值对 |
| [set_item_key_ui_anim_play_mode_kv](#set_item_key_ui_anim_play_mode_kv) | 预设库 添加UI_ANIM_PLAY_MODE键值对 |
| [set_item_key_ui_text_font_name_kv](#set_item_key_ui_text_font_name_kv) | 预设库 添加UI_TEXT_FONT_NAME键值对 |
| [set_item_key_ui_eca_anim_type_kv](#set_item_key_ui_eca_anim_type_kv) | 预设库 添加UI_ECA_ANIM_TYPE键值对 |
| [set_item_key_local_unit_group_kv](#set_item_key_local_unit_group_kv) | 预设库 添加LOCAL_UNIT_GROUP键值对 |
| [set_item_key_damage_attack_type_kv](#set_item_key_damage_attack_type_kv) | 预设库 添加DAMAGE_ATTACK_TYPE键值对 |
| [set_item_key_damage_armor_type_kv](#set_item_key_damage_armor_type_kv) | 预设库 添加DAMAGE_ARMOR_TYPE键值对 |
| [set_item_key_item_stack_type_kv](#set_item_key_item_stack_type_kv) | 预设库 添加ITEM_STACK_TYPE键值对 |
| [set_item_key_ability_release_id_kv](#set_item_key_ability_release_id_kv) | 预设库 添加ABILITY_RELEASE_ID键值对 |
| [set_item_key_slot_type_kv](#set_item_key_slot_type_kv) | 预设库 添加SLOT_TYPE键值对 |
| [set_item_key_ui_point_kv](#set_item_key_ui_point_kv) | 预设库 添加UI_POINT键值对 |
| [set_item_key_attach_model_entity_kv](#set_item_key_attach_model_entity_kv) | 预设库 添加ATTACH_MODEL_ENTITY键值对 |
| [set_item_key_live2d_kv](#set_item_key_live2d_kv) | 预设库 添加LIVE2D键值对 |
| [set_item_key_spine_kv](#set_item_key_spine_kv) | 预设库 添加SPINE键值对 |
| [set_item_key_force_entity_kv](#set_item_key_force_entity_kv) | 预设库 添加FORCE_ENTITY键值对 |
| [set_item_key_goods_key_kv](#set_item_key_goods_key_kv) | 预设库 添加GOODS_KEY键值对 |
| [set_item_key_mouse_key_without_middle_kv](#set_item_key_mouse_key_without_middle_kv) | 预设库 添加MOUSE_KEY_WITHOUT_MIDDLE键值对 |
| [set_item_key_map_kv](#set_item_key_map_kv) | 预设库 添加MAP键值对 |
| [set_item_key_unit_group_command_type_kv](#set_item_key_unit_group_command_type_kv) | 预设库 添加UNIT_GROUP_COMMAND_TYPE键值对 |
| [set_item_key_rescue_seeker_type_kv](#set_item_key_rescue_seeker_type_kv) | 预设库 添加RESCUE_SEEKER_TYPE键值对 |
| [set_item_key_rescuer_type_kv](#set_item_key_rescuer_type_kv) | 预设库 添加RESCUER_TYPE键值对 |
| [set_item_key_store_item_type_kv](#set_item_key_store_item_type_kv) | 预设库 添加STORE_ITEM_TYPE键值对 |
| [set_item_key_site_state_kv](#set_item_key_site_state_kv) | 预设库 添加SITE_STATE键值对 |
| [set_item_key_coin_currency_kv](#set_item_key_coin_currency_kv) | 预设库 添加COIN_CURRENCY键值对 |
| [set_ability_key_ui_gridview_type_kv](#set_ability_key_ui_gridview_type_kv) | 预设库 添加UI_GRIDVIEW_TYPE键值对 |
| [set_ability_key_ui_gridview_bar_type_kv](#set_ability_key_ui_gridview_bar_type_kv) | 预设库 添加UI_GRIDVIEW_BAR_TYPE键值对 |
| [set_ability_key_ui_effect_camera_mode_kv](#set_ability_key_ui_effect_camera_mode_kv) | 预设库 添加UI_EFFECT_CAMERA_MODE键值对 |
| [set_ability_key_ui_equip_slot_use_type_kv](#set_ability_key_ui_equip_slot_use_type_kv) | 预设库 添加UI_EQUIP_SLOT_USE_TYPE键值对 |
| [set_ability_key_ui_equip_slot_drag_type_kv](#set_ability_key_ui_equip_slot_drag_type_kv) | 预设库 添加UI_EQUIP_SLOT_DRAG_TYPE键值对 |
| [set_ability_key_ui_layout_clipping_type_kv](#set_ability_key_ui_layout_clipping_type_kv) | 预设库 添加UI_LAYOUT_CLIPPING_TYPE键值对 |
| [set_ability_key_ui_text_over_length_handling_type_kv](#set_ability_key_ui_text_over_length_handling_type_kv) | 预设库 添加UI_TEXT_OVER_LENGTH_HANDLING_TYPE键值对 |
| [set_ability_key_ui_pos_adapt_mode_kv](#set_ability_key_ui_pos_adapt_mode_kv) | 预设库 添加UI_POS_ADAPT_MODE键值对 |
| [set_ability_key_ui_chat_send_channel_kv](#set_ability_key_ui_chat_send_channel_kv) | 预设库 添加UI_CHAT_SEND_CHANNEL键值对 |
| [set_ability_key_ui_chat_recv_channel_kv](#set_ability_key_ui_chat_recv_channel_kv) | 预设库 添加UI_CHAT_RECV_CHANNEL键值对 |
| [set_ability_key_ui_anim_play_mode_kv](#set_ability_key_ui_anim_play_mode_kv) | 预设库 添加UI_ANIM_PLAY_MODE键值对 |
| [set_ability_key_ui_text_font_name_kv](#set_ability_key_ui_text_font_name_kv) | 预设库 添加UI_TEXT_FONT_NAME键值对 |
| [set_ability_key_ui_eca_anim_type_kv](#set_ability_key_ui_eca_anim_type_kv) | 预设库 添加UI_ECA_ANIM_TYPE键值对 |
| [set_ability_key_local_unit_group_kv](#set_ability_key_local_unit_group_kv) | 预设库 添加LOCAL_UNIT_GROUP键值对 |
| [set_ability_key_damage_attack_type_kv](#set_ability_key_damage_attack_type_kv) | 预设库 添加DAMAGE_ATTACK_TYPE键值对 |
| [set_ability_key_damage_armor_type_kv](#set_ability_key_damage_armor_type_kv) | 预设库 添加DAMAGE_ARMOR_TYPE键值对 |
| [set_ability_key_item_stack_type_kv](#set_ability_key_item_stack_type_kv) | 预设库 添加ITEM_STACK_TYPE键值对 |
| [set_ability_key_ability_release_id_kv](#set_ability_key_ability_release_id_kv) | 预设库 添加ABILITY_RELEASE_ID键值对 |
| [set_ability_key_slot_type_kv](#set_ability_key_slot_type_kv) | 预设库 添加SLOT_TYPE键值对 |
| [set_ability_key_ui_point_kv](#set_ability_key_ui_point_kv) | 预设库 添加UI_POINT键值对 |
| [set_ability_key_attach_model_entity_kv](#set_ability_key_attach_model_entity_kv) | 预设库 添加ATTACH_MODEL_ENTITY键值对 |
| [set_ability_key_live2d_kv](#set_ability_key_live2d_kv) | 预设库 添加LIVE2D键值对 |
| [set_ability_key_spine_kv](#set_ability_key_spine_kv) | 预设库 添加SPINE键值对 |
| [set_ability_key_force_entity_kv](#set_ability_key_force_entity_kv) | 预设库 添加FORCE_ENTITY键值对 |
| [set_ability_key_goods_key_kv](#set_ability_key_goods_key_kv) | 预设库 添加GOODS_KEY键值对 |
| [set_ability_key_mouse_key_without_middle_kv](#set_ability_key_mouse_key_without_middle_kv) | 预设库 添加MOUSE_KEY_WITHOUT_MIDDLE键值对 |
| [set_ability_key_map_kv](#set_ability_key_map_kv) | 预设库 添加MAP键值对 |
| [set_ability_key_unit_group_command_type_kv](#set_ability_key_unit_group_command_type_kv) | 预设库 添加UNIT_GROUP_COMMAND_TYPE键值对 |
| [set_ability_key_rescue_seeker_type_kv](#set_ability_key_rescue_seeker_type_kv) | 预设库 添加RESCUE_SEEKER_TYPE键值对 |
| [set_ability_key_rescuer_type_kv](#set_ability_key_rescuer_type_kv) | 预设库 添加RESCUER_TYPE键值对 |
| [set_ability_key_store_item_type_kv](#set_ability_key_store_item_type_kv) | 预设库 添加STORE_ITEM_TYPE键值对 |
| [set_ability_key_site_state_kv](#set_ability_key_site_state_kv) | 预设库 添加SITE_STATE键值对 |
| [set_ability_key_coin_currency_kv](#set_ability_key_coin_currency_kv) | 预设库 添加COIN_CURRENCY键值对 |
| [set_attach_model_fresnel](#set_attach_model_fresnel) | 遍历魔法效果的挂接模型 |
| [api_get_item_group_length](#api_get_item_group_length) | 获取物品组的数量 |
| [api_get_item_type_id](#api_get_item_type_id) | 获取物品类型编号 |
| [api_get_item_stack_type_id](#api_get_item_stack_type_id) | 获取物品类型的堆叠类型 |
| [api_get_item_group_intersection](#api_get_item_group_intersection) | 物品组取交集 |
| [api_get_item_group_diff](#api_get_item_group_diff) | 物品组取差集 |
| [api_switch_unit_item_slot_by_slot_id](#api_switch_unit_item_slot_by_slot_id) | 根据槽位交换物品 |
| [api_switch_item_slot](#api_switch_item_slot) | 交换物品 |
| [set_item_name_permanent_show_config](#set_item_name_permanent_show_config) | 设置游戏内物品名称是否常驻显示 |
| [set_touch_type_of_picking_up_item_by_item_name](#set_touch_type_of_picking_up_item_by_item_name) | 设置物品姓名版点击拾取的操作方式 |
| [api_get_store_item_type](#api_get_store_item_type) | 获取平台道具类别 |
| [screenshot_func_for_lua](#screenshot_func_for_lua) | 在Lua中调用截图功能 |
| [disable_all_eca_triggers](#disable_all_eca_triggers) | 禁用所有的ECA全局触发器 |
| [mover_miss_target](#mover_miss_target) | 运动器丢失追踪目标 |
| [get_projectile_mover](#get_projectile_mover) | 获得投射物的运动器 |
| [get_mover_relate_projectile](#get_mover_relate_projectile) | 获取运动器关联投射物 |
| [create_unit_command_customized_move_to_pos](#create_unit_command_customized_move_to_pos) | 定制移动 |
| [create_unit_command_move_to_pos_3D](#create_unit_command_move_to_pos_3D) | 移动至三维坐标 |
| [create_unit_command_hold_3D](#create_unit_command_hold_3D) | 驻守至三维坐标 |
| [create_unit_command_attack_point](#create_unit_command_attack_point) | 攻击目标点 |
| [create_unit_command_patrol](#create_unit_command_patrol) | 巡逻 |
| [api_release_group_command](#api_release_group_command) | 发布命令 |
| [create_unit_group_command_move_to_pos](#create_unit_group_command_move_to_pos) | 移动 |
| [create_unit_group_command_stop](#create_unit_group_command_stop) | 停止 |
| [create_unit_group_command_empty](#create_unit_group_command_empty) | 空状态 |
| [create_unit_group_command_hold](#create_unit_group_command_hold) | 驻守 |
| [create_unit_group_command_attack_move](#create_unit_group_command_attack_move) | 攻击移动 |
| [create_unit_group_command_attack_target](#create_unit_group_command_attack_target) | 攻击 |
| [create_unit_group_command_move_along_road](#create_unit_group_command_move_along_road) | 沿路径移动 |
| [create_unit_group_command_follow](#create_unit_group_command_follow) | 跟随 |
| [create_unit_group_command_move_to_random_pos](#create_unit_group_command_move_to_random_pos) | 移动到随机位置 |
| [create_unit_group_command_attack_move_random_pos](#create_unit_group_command_attack_move_random_pos) | 攻击移动到随机位置 |
| [create_unit_group_command_attack_point](#create_unit_group_command_attack_point) | 攻击目标点 |
| [create_unit_group_command_patrol](#create_unit_group_command_patrol) | 巡逻 |
| [set_player_sfx_switch_by_tag](#set_player_sfx_switch_by_tag) | 特效播放开关 |
| [create_link_sfx_from_unit_to_point1](#create_link_sfx_from_unit_to_point1) | 创建单位到点闪电特效 |
| [create_link_sfx_from_unit_to_unit1](#create_link_sfx_from_unit_to_unit1) | 创建单位到单位闪电特效 |
| [create_link_sfx_from_point_to_unit1](#create_link_sfx_from_point_to_unit1) | 创建点到单位闪电特效 |
| [create_link_sfx_from_point_to_point1](#create_link_sfx_from_point_to_point1) | 创建点到点闪电特效 |
| [create_sfx_on_point_new](#create_sfx_on_point_new) | 创建特效到点 |
| [create_sfx_on_unit_new_new](#create_sfx_on_unit_new_new) | 创建特效到单位附加点（跟随旋转使用枚举） |
| [create_sfx_on_unit_3](#create_sfx_on_unit_3) | 创建特效到单位附加点（跟随旋转使用枚举） |
| [create_sfx_on_modifier_attach_model](#create_sfx_on_modifier_attach_model) | 创建特效到魔法效果挂接模型（跟随旋转使用枚举） |
| [set_sfx_color_hex](#set_sfx_color_hex) | 设置特效颜色(HEX) |
| [set_link_sfx_scale](#set_link_sfx_scale) | 设置闪电特效缩放 |
| [set_link_sfx_animation_speed](#set_link_sfx_animation_speed) | 设置闪电特效动画速度 |
| [add_point_tag](#add_point_tag) | 给点添加tag |
| [remove_point_tag](#remove_point_tag) | 给点移除tag |
| [get_points_by_tag](#get_points_by_tag) | 根据tag获取对应的点 |
| [if_area_has_tag](#if_area_has_tag) | 区域是否拥有某tags |
| [api_reset_cir_area](#api_reset_cir_area) | 重设圆形区域中心点和半径 |
| [api_reset_rect_two_point](#api_reset_rect_two_point) | 重设矩形区域起点和终点 |
| [get_map_id](#get_map_id) | 获取当前地图版本id |
| [get_uppass_env](#get_uppass_env) | 获取当前uppass env |
| [api_collect_garbage](#api_collect_garbage) | 进行一次内存垃圾回收以释放内存。会导致游戏短暂卡顿，建议在切场景等能够接收卡顿的时机调用 |
| [get_current_level](#get_current_level) | 获取当前关卡 |
| [get_client_mode](#get_client_mode) | 获取当前运行环境 |
| [load_sub_scene](#load_sub_scene) | 创建地形预设 |
| [get_global_map_str_archive](#get_global_map_str_archive) | 获取当前地图的指定key的字符串型存档值 |
| [get_archive_rank_player_tag](#get_archive_rank_player_tag) | 获取玩家指定的个人存档栏位的第n名玩家昵称的后缀id |
| [get_aid_by_rank_info](#get_aid_by_rank_info) | 获取排行榜指定排名玩家的aid |
| [get_local_engine_version](#get_local_engine_version) | 获取本地引擎版本号 |
| [get_latest_engine_version](#get_latest_engine_version) | 获取最新引擎版本号 |
| [get_local_map_id](#get_local_map_id) | 获取本地地图版本号 |
| [get_latest_map_id](#get_latest_map_id) | 获取最新地图版本号 |
| [api_get_logic_fps](#api_get_logic_fps) | 获取逻辑帧率 |
| [api_upload_user_tracking_data](#api_upload_user_tracking_data) | 上传埋点数据 |
| [add_detail_log](#add_detail_log) | 记录自定义日志，用于定位不同步 |
| [api_set_enable_detail_snapshot](#api_set_enable_detail_snapshot) | 开启/关闭不同步详细日志。默认关闭。这个是总开关，关了这个之后别的设置接口都不生效了了，但性能最好。 |
| [api_set_snapshot_traceback_level](#api_set_snapshot_traceback_level) | 设置某些日志的堆栈记录详细等级。 |
| [api_set_enable_timer_snapshot](#api_set_enable_timer_snapshot) | 开启/关闭timer不同步检测日志。默认关闭。开启后可以检测出哪里多创建了ECA计时器，但计时器不一致并不一定代表着实际游戏内容不同步（比如计时器回调里只做表现层修改就是安全的） |
| [api_set_enable_ui_snapshot](#api_set_enable_ui_snapshot) | 开启/关闭UI界面不同步检测日志。默认关闭。开启后会统计所有UI的创建。UI创建不一致会导致UI的序号不一致，进而导致UI组件/元件转字符串的结果不一致，以及UI相关事件中的【触发事件的控件】不一致，如果游戏中将相关值用于玩法逻辑中，则会导致逻辑不同步。如果确定不会引起不同步，可以选择关闭这个开关 |
| [api_set_enable_eca_snapshot](#api_set_enable_eca_snapshot) | 开启/关闭ECA不同步检测日志。默认关闭，开销较高。可通过参数过滤掉一些安全的API以防止误报，例如创建特效、UI操作等 |
| [api_set_detail_snapshot_enable_tag](#api_set_detail_snapshot_enable_tag) | 设置不同步详细日志级别。越详细越利于定位不同步产生点,但性能消耗会增高 |
| [api_set_time_scale](#api_set_time_scale) | 设置播放速率 |
| [set_joystick_target](#set_joystick_target) | 绑定摇杆单位 |
| [api_set_player_select_unit_priority](#api_set_player_select_unit_priority) | 设置玩家点选单位优先级 |
| [set_local_camera_focus_position](#set_local_camera_focus_position) | 设置本地相机聚焦位置 |
| [api_set_rule_mgr_value](#api_set_rule_mgr_value) | 局内修改游戏规则开关（布尔值） |
| [api_set_shortcut_enable](#api_set_shortcut_enable) | 局内修改游戏按键功能开关（布尔值） |
| [api_set_obj_twinkle_parameters](#api_set_obj_twinkle_parameters) | 设置对象的闪烁效果 |
| [api_get_obj_fresnel_exp](#api_get_obj_fresnel_exp) | 获取对象的菲涅尔指数 |
| [api_get_obj_fresnel_color_strength](#api_get_obj_fresnel_color_strength) | 获取对象的菲涅尔强度 |
| [enable_player_mini_map_fog_img](#enable_player_mini_map_fog_img) | 开启小地图迷雾显示 |
| [set_mini_map_show_area_by_two_points](#set_mini_map_show_area_by_two_points) | 设置小地图显示区域(两点) |
| [only_show_local_player_jump_word](#only_show_local_player_jump_word) | 仅显示本地玩家跳字 |
| [set_global_visibility_of_billboard](#set_global_visibility_of_billboard) | 设置血条的全局可见性 |
| [get_point_texture](#get_point_texture) | 获取指定点的纹理类型 |
| [set_obj_material_param](#set_obj_material_param) | 修改对象材质 |
| [set_mouse_cursor_visible](#set_mouse_cursor_visible) | 设置鼠标是否可见 |
| [set_mini_map_alpha](#set_mini_map_alpha) | 小地图遮罩透明度 |
| [set_mini_map_color_int](#set_mini_map_color_int) | 小地图遮罩颜色 |
| [set_mini_map_color_str](#set_mini_map_color_str) | 小地图遮罩颜色 |
| [api_set_hero_mini_map_frame](#api_set_hero_mini_map_frame) | 小地图 - 设置英雄小地图头像底框 |
| [int_transform_unit_type](#int_transform_unit_type) | 整数转单位类型 |
| [int_transform_projectile_type](#int_transform_projectile_type) | 整数转投射物类型 |
| [int_transform_item_type](#int_transform_item_type) | 整数转物品类型 |
| [int_transform_modifier_type](#int_transform_modifier_type) | 整数转魔法效果类型 |
| [int_transform_ability_type](#int_transform_ability_type) | 整数转技能类型 |
| [int_transform_tech_type](#int_transform_tech_type) | 整数转科技类型 |
| [int_transform_destruct_type](#int_transform_destruct_type) | 整数转可破坏物类型 |
| [int_transform_sound_type](#int_transform_sound_type) | 整数转声音类型 |
| [steam_get_team_id](#steam_get_team_id) | 获取队伍id |
| [steam_get_player_id](#steam_get_player_id) | 获取玩家id |
| [steam_get_player_head_icon_url](#steam_get_player_head_icon_url) | 获取本地玩家头像url |
| [steam_get_team_state](#steam_get_team_state) | 获取队伍状态 |
| [get_is_steam_lobby](#get_is_steam_lobby) | 获取是否是大厅关卡 |
| [steam_get_player_state](#steam_get_player_state) | 获取玩家状态 |
| [steam_get_player_nickname](#steam_get_player_nickname) | 获取本地玩家的名称 |
| [steam_get_player_storm_items](#steam_get_player_storm_items) | 获取本地玩家背包内的道具 |
| [set_ui_comp_image_with_icon_steam](#set_ui_comp_image_with_icon_steam) | 设置ui组件图片(图片类型) |
| [get_steam_player_currency](#get_steam_player_currency) | 获取玩家steam国区 |
| [get_steam_goods_price](#get_steam_goods_price) | 获取玩家商品对应国区价格 |
| [set_steam_global_archive_data](#set_steam_global_archive_data) | 设置steam大厅的指定key的全局存档值 |
| [add_steam_global_archive_data](#add_steam_global_archive_data) | 增加steam大厅的指定key的全局存档值 |
| [request_buy_mall_coin](#request_buy_mall_coin) | 请求购买 |
| [set_draw_ui](#set_draw_ui) | 设置是否渲染场景 |
| [get_local_game_version](#get_local_game_version) | 获取本地游戏版本号 |
| [get_latest_game_version](#get_latest_game_version) | 获取最新游戏版本号 |
| [get_settle_ladder_role](#get_settle_ladder_role) | 获取进行结算的玩家 |
| [get_settle_ladder_new_score](#get_settle_ladder_new_score) | 获取进行结算的玩家新分数 |
| [get_settle_ladder_diff_value](#get_settle_ladder_diff_value) | 获取进行结算的玩家匹配分修正值 |
| [lua_request_change_room_name](#lua_request_change_room_name) | 请求更改房间名称 |
| [lua_request_message_from_server](#lua_request_message_from_server) | 请求服务器时间 |
| [lua_request_get_map_rank](#lua_request_get_map_rank) | 请求获取最新排行榜的值 |
| [lua_request_server_time](#lua_request_server_time) | 请求服务器时间 |
| [lua_request_server_role_use_item](#lua_request_server_role_use_item) | 请求服务器获取玩家使用道具 |
| [lua_request_server_random_pool_result](#lua_request_server_random_pool_result) | 执行服务器随机池掉落策略 |
| [lua_request_server_mall_goods_info](#lua_request_server_mall_goods_info) | 请求服务器获取商品信息 |
| [lua_request_server_consume_mall_coin](#lua_request_server_consume_mall_coin) | 请求服务器获取商城消耗货币 |
| [lua_request_server_mall_purchase_goods](#lua_request_server_mall_purchase_goods) | 请求服务器购买商品 |
| [lua_request_server_mall_dlc_status](#lua_request_server_mall_dlc_status) | 请求服务器获取商城dlc状态 |
| [lua_request_server_create_room](#lua_request_server_create_room) | steam创建房间 |
| [lua_request_server_room_list_info](#lua_request_server_room_list_info) | steam请求房间列表 |
| [lua_request_server_join_room](#lua_request_server_join_room) | steam请求加入房间 |
| [lua_request_server_room_info](#lua_request_server_room_info) | steam请求房间信息 |
| [lua_request_server_room_strat_game](#lua_request_server_room_strat_game) | steam请求房间开始游戏 |
| [lua_request_server_invite_player_join_room](#lua_request_server_invite_player_join_room) | steam邀请玩家加入房间 |
| [lua_request_server_reply_room_invite](#lua_request_server_reply_room_invite) | steam接受房间邀请 |
| [lua_request_server_change_room_slot](#lua_request_server_change_room_slot) | steam交换房间槽位 |
| [lua_request_server_change_owner](#lua_request_server_change_owner) | steam交换房主 |
| [lua_request_server_exit_room](#lua_request_server_exit_room) | steam退出房间 |
| [lua_request_server_kick_from_room](#lua_request_server_kick_from_room) | steam踢出房间 |
| [lua_request_server_set_site_state](#lua_request_server_set_site_state) | steam改变位置状态 |
| [lua_request_server_change_room_password](#lua_request_server_change_room_password) | steam更改房间密码 |
| [lua_request_server_change_room_level_limit](#lua_request_server_change_room_level_limit) | steam更改房间等级 |
| [lua_request_my_team_info](#lua_request_my_team_info) | steam查询自己的队伍信息 |
| [api_destroy_force](#api_destroy_force) | 删除牵引力 |
| [create_force_direction](#create_force_direction) | 创建牵引力方向 |
| [create_force_point](#create_force_point) | 创建牵引力点 |
| [create_force_target](#create_force_target) | 创建牵引力目标 |
| [set_ui_image_color_hex](#set_ui_image_color_hex) | 设置图片颜色(hex) |
| [get_ui_image_color](#get_ui_image_color) | 【异步】获取图片颜色 |
| [ui_comp_role_exist](#ui_comp_role_exist) | 界面组件是否存在 |
| [set_ui_comp_pos_percent](#set_ui_comp_pos_percent) | 设置ui组件坐标百分比 |
| [set_ui_comp_pos_mode](#set_ui_comp_pos_mode) | 设置ui组件坐标适配模式 |
| [set_ui_comp_font_color_norm](#set_ui_comp_font_color_norm) | 设置ui文本颜色 |
| [set_ui_comp_font_color_hex](#set_ui_comp_font_color_hex) | 设置ui文本颜色(HEX) |
| [get_ui_comp_font_color](#get_ui_comp_font_color) | 【异步】获取ui文本颜色 |
| [set_ui_comp_text_multilingual](#set_ui_comp_text_multilingual) | 设置ui文本多语言 |
| [play_ui_comp_anim_new](#play_ui_comp_anim_new) | 新播放UI控件时间轴动画 |
| [api_set_ability_release_timing](#api_set_ability_release_timing) | 设置技能按钮施法的时机 |
| [api_set_ability_mouse_control_key](#api_set_ability_mouse_control_key) | 设置技能按钮鼠标操控快捷键 |
| [get_ui_comp_opacity](#get_ui_comp_opacity) | 【异步】获取控件透明度 |
| [set_ui_comp_unit_slot_new](#set_ui_comp_unit_slot_new) | 设置道具栏控件类型和槽位号 |
| [set_ui_model_id_from_object_editor](#set_ui_model_id_from_object_editor) | 设置模型控件的物编模型 |
| [set_ui_model_from_scene_unit_with_tag_model](#set_ui_model_from_scene_unit_with_tag_model) | 设置模型控件的模型为场景中设定了指定标签的模型 |
| [set_ui_model_model_scale](#set_ui_model_model_scale) | 设置模型控件模型缩放 |
| [set_ui_model_unit](#set_ui_model_unit) | 设置UI模型控件单位 |
| [set_modifier_on_ui_model](#set_modifier_on_ui_model) | 播放魔法效果表现到模型控件 |
| [play_ui_spine](#play_ui_spine) | 播放spine动画 |
| [get_slider_cur_percent_safe](#get_slider_cur_percent_safe) | 【同步】获取滑动条当前值 |
| [set_ui_comp_bind_modifier_cycle](#set_ui_comp_bind_modifier_cycle) | 绑定魔法效果剩余循环周期到玩家界面控件的属性 |
| [get_list_view_percent](#get_list_view_percent) | 【异步】获取列表当前百分比位置 |
| [set_list_view_layout_reverse](#set_list_view_layout_reverse) | 设置列表反向排布 |
| [get_ui_comp_by_prefab_ins](#get_ui_comp_by_prefab_ins) | 通过预制实例获得ui控件 |
| [stop_eca_anim](#stop_eca_anim) | 停止播放控件动画 |
| [set_equip_slot_use_operation](#set_equip_slot_use_operation) | 设置使用物品操作方式 |
| [set_equip_slot_drag_operation](#set_equip_slot_drag_operation) | 设置拖拽物品操作方式 |
| [get_page_view_current_index](#get_page_view_current_index) | 【异步】获取轮播图当前图片索引 |
| [get_page_view_click_index](#get_page_view_click_index) | 【异步】获取轮播图点击图片索引 |
| [get_checkbox_selected](#get_checkbox_selected) | 获取复选框当前选中状态 |
| [set_checkbox_selected](#set_checkbox_selected) | 设置复选框当前选中状态 |
| [get_tab_widget_current_index](#get_tab_widget_current_index) | 【异步】界面-获取标签页控件当前选中页索引 |
| [set_tab_widget_current_index](#set_tab_widget_current_index) | 界面-设置标签页控件当前选中页索引 |
| [get_ui_comp_path](#get_ui_comp_path) | 【异步】界面-获取控件路径 |
| [play_live2d_anim](#play_live2d_anim) | live2d控件播放动画 |
| [stop_live2d_anim](#stop_live2d_anim) | live2d控件停止播放动画 |
| [set_live2d_model_id](#set_live2d_model_id) | live2d设置模型 |
| [set_live2d_expression](#set_live2d_expression) | live2d设置表情 |
| [set_live2d_background_color](#set_live2d_background_color) | live2d设置背景色 |
| [del_ui_comp_event](#del_ui_comp_event) | 界面-删除界面事件 |
| [set_layout_clipping_enable](#set_layout_clipping_enable) | 设置layout是否裁剪 |
| [set_input_field_enable](#set_input_field_enable) | 设置输入框是否可用 |
| [set_layout_clipping_type](#set_layout_clipping_type) | 设置layout裁剪模式 |
| [set_text_over_length_handling_type](#set_text_over_length_handling_type) | 设置文本超框处理方式 |
| [set_ui_gridview_type](#set_ui_gridview_type) | 设置网格列表布局方式 |
| [set_ui_gridview_count](#set_ui_gridview_count) | 设置网格列表行数列数 |
| [set_ui_gridview_size](#set_ui_gridview_size) | 设置网格列表单元格宽高 |
| [set_ui_gridview_margin](#set_ui_gridview_margin) | 设置网格列表边距 |
| [set_ui_gridview_space](#set_ui_gridview_space) | 设置网格列表单元格间距 |
| [set_ui_gridview_align](#set_ui_gridview_align) | 设置网格列表对齐方式 |
| [insert_ui_gridview_comp](#insert_ui_gridview_comp) | 添加控件到网格列表指定位置 |
| [set_ui_gridview_scroll](#set_ui_gridview_scroll) | 设置网格列表启用/禁止滚动 |
| [set_ui_gridview_size_adaptive](#set_ui_gridview_size_adaptive) | 设置网格列表启用/禁止尺寸随内容变化 |

---

## get_destructible_key_modifier_entity_kv

method in GameAPI

- 描述

    获取可破坏物编号MODIFIER_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierEntity | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_modifier_entity_kv(destructible_key, "key")
```

---

## get_tech_key_modifier_entity_kv

method in GameAPI

- 描述

    获取科技编号MODIFIER_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierEntity | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_modifier_entity_kv(tech_key, "key")
```

---

## get_icon_id_modifier_entity_kv

method in GameAPI

- 描述

    获取图片MODIFIER_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierEntity | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_modifier_entity_kv(1, "key")
```

---

## get_physics_entity_key_modifier_entity_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型MODIFIER_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierEntity | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_modifier_entity_kv(1, "key")
```

---

## get_unit_key_modifier_type_kv

method in GameAPI

- 描述

    获取单位编号MODIFIER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierType | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_modifier_type_kv(unit_key, "key")
```

---

## get_item_key_modifier_type_kv

method in GameAPI

- 描述

    获取物品编号MODIFIER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierType | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_modifier_type_kv(item_key, "key")
```

---

## get_ability_key_modifier_type_kv

method in GameAPI

- 描述

    获取技能编号MODIFIER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierType | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_modifier_type_kv(ability_key, "key")
```

---

## get_modifier_key_modifier_type_kv

method in GameAPI

- 描述

    获取魔法效果特效编号MODIFIER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierType | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_modifier_type_kv(modifier_key, "key")
```

---

## get_projectile_key_modifier_type_kv

method in GameAPI

- 描述

    获取特效编号MODIFIER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierType | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_modifier_type_kv(projectile_key, "key")
```

---

## get_destructible_key_modifier_type_kv

method in GameAPI

- 描述

    获取可破坏物编号MODIFIER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierType | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_modifier_type_kv(destructible_key, "key")
```

---

## get_tech_key_modifier_type_kv

method in GameAPI

- 描述

    获取科技编号MODIFIER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierType | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_modifier_type_kv(tech_key, "key")
```

---

## get_icon_id_modifier_type_kv

method in GameAPI

- 描述

    获取图片MODIFIER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierType | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_modifier_type_kv(1, "key")
```

---

## get_physics_entity_key_modifier_type_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型MODIFIER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierType | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_modifier_type_kv(1, "key")
```

---

## get_unit_key_modifier_effect_type_kv

method in GameAPI

- 描述

    获取单位编号MODIFIER_EFFECT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierEffectType | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_modifier_effect_type_kv(unit_key, "key")
```

---

## get_item_key_modifier_effect_type_kv

method in GameAPI

- 描述

    获取物品编号MODIFIER_EFFECT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierEffectType | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_modifier_effect_type_kv(item_key, "key")
```

---

## get_ability_key_modifier_effect_type_kv

method in GameAPI

- 描述

    获取技能编号MODIFIER_EFFECT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierEffectType | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_modifier_effect_type_kv(ability_key, "key")
```

---

## get_modifier_key_modifier_effect_type_kv

method in GameAPI

- 描述

    获取魔法效果特效编号MODIFIER_EFFECT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierEffectType | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_modifier_effect_type_kv(modifier_key, "key")
```

---

## get_projectile_key_modifier_effect_type_kv

method in GameAPI

- 描述

    获取特效编号MODIFIER_EFFECT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierEffectType | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_modifier_effect_type_kv(projectile_key, "key")
```

---

## get_destructible_key_modifier_effect_type_kv

method in GameAPI

- 描述

    获取可破坏物编号MODIFIER_EFFECT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierEffectType | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_modifier_effect_type_kv(destructible_key, "key")
```

---

## get_tech_key_modifier_effect_type_kv

method in GameAPI

- 描述

    获取科技编号MODIFIER_EFFECT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierEffectType | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_modifier_effect_type_kv(tech_key, "key")
```

---

## get_icon_id_modifier_effect_type_kv

method in GameAPI

- 描述

    获取图片MODIFIER_EFFECT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierEffectType | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_modifier_effect_type_kv(1, "key")
```

---

## get_physics_entity_key_modifier_effect_type_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型MODIFIER_EFFECT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierEffectType | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_modifier_effect_type_kv(1, "key")
```

---

## get_unit_key_modifier_kv

method in GameAPI

- 描述

    获取单位编号MODIFIER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierKey | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_modifier_kv(unit_key, "key")
```

---

## get_item_key_modifier_kv

method in GameAPI

- 描述

    获取物品编号MODIFIER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierKey | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_modifier_kv(item_key, "key")
```

---

## get_ability_key_modifier_kv

method in GameAPI

- 描述

    获取技能编号MODIFIER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierKey | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_modifier_kv(ability_key, "key")
```

---

## get_modifier_key_modifier_kv

method in GameAPI

- 描述

    获取魔法效果特效编号MODIFIER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierKey | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_modifier_kv(modifier_key, "key")
```

---

## get_projectile_key_modifier_kv

method in GameAPI

- 描述

    获取特效编号MODIFIER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierKey | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_modifier_kv(projectile_key, "key")
```

---

## get_destructible_key_modifier_kv

method in GameAPI

- 描述

    获取可破坏物编号MODIFIER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierKey | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_modifier_kv(destructible_key, "key")
```

---

## get_tech_key_modifier_kv

method in GameAPI

- 描述

    获取科技编号MODIFIER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierKey | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_modifier_kv(tech_key, "key")
```

---

## get_icon_id_modifier_kv

method in GameAPI

- 描述

    获取图片MODIFIER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierKey | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_modifier_kv(1, "key")
```

---

## get_physics_entity_key_modifier_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型MODIFIER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierKey | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_modifier_kv(1, "key")
```

---

## get_unit_key_projectile_kv

method in GameAPI

- 描述

    获取单位编号PROJECTILE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileKey | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_projectile_kv(unit_key, "key")
```

---

## get_item_key_projectile_kv

method in GameAPI

- 描述

    获取物品编号PROJECTILE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileKey | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_projectile_kv(item_key, "key")
```

---

## get_ability_key_projectile_kv

method in GameAPI

- 描述

    获取技能编号PROJECTILE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileKey | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_projectile_kv(ability_key, "key")
```

---

## get_modifier_key_projectile_kv

method in GameAPI

- 描述

    获取魔法效果特效编号PROJECTILE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileKey | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_projectile_kv(modifier_key, "key")
```

---

## get_projectile_key_projectile_kv

method in GameAPI

- 描述

    获取特效编号PROJECTILE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileKey | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_projectile_kv(projectile_key, "key")
```

---

## get_destructible_key_projectile_kv

method in GameAPI

- 描述

    获取可破坏物编号PROJECTILE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileKey | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_projectile_kv(destructible_key, "key")
```

---

## get_tech_key_projectile_kv

method in GameAPI

- 描述

    获取科技编号PROJECTILE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileKey | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_projectile_kv(tech_key, "key")
```

---

## get_icon_id_projectile_kv

method in GameAPI

- 描述

    获取图片PROJECTILE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileKey | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_projectile_kv(1, "key")
```

---

## get_physics_entity_key_projectile_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型PROJECTILE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileKey | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_projectile_kv(1, "key")
```

---

## get_unit_key_projectile_entity_kv

method in GameAPI

- 描述

    获取单位编号PROJECTILE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileEntity | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_projectile_entity_kv(unit_key, "key")
```

---

## get_item_key_projectile_entity_kv

method in GameAPI

- 描述

    获取物品编号PROJECTILE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileEntity | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_projectile_entity_kv(item_key, "key")
```

---

## get_ability_key_projectile_entity_kv

method in GameAPI

- 描述

    获取技能编号PROJECTILE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileEntity | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_projectile_entity_kv(ability_key, "key")
```

---

## get_modifier_key_projectile_entity_kv

method in GameAPI

- 描述

    获取魔法效果特效编号PROJECTILE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileEntity | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_projectile_entity_kv(modifier_key, "key")
```

---

## get_projectile_key_projectile_entity_kv

method in GameAPI

- 描述

    获取特效编号PROJECTILE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileEntity | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_projectile_entity_kv(projectile_key, "key")
```

---

## get_destructible_key_projectile_entity_kv

method in GameAPI

- 描述

    获取可破坏物编号PROJECTILE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileEntity | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_projectile_entity_kv(destructible_key, "key")
```

---

## get_tech_key_projectile_entity_kv

method in GameAPI

- 描述

    获取科技编号PROJECTILE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileEntity | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_projectile_entity_kv(tech_key, "key")
```

---

## get_icon_id_projectile_entity_kv

method in GameAPI

- 描述

    获取图片PROJECTILE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileEntity | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_projectile_entity_kv(1, "key")
```

---

## get_physics_entity_key_projectile_entity_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型PROJECTILE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileEntity | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_projectile_entity_kv(1, "key")
```

---

## get_unit_key_projectile_group_kv

method in GameAPI

- 描述

    获取单位编号PROJECTILE_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileGroup | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_projectile_group_kv(unit_key, "key")
```

---

## get_item_key_projectile_group_kv

method in GameAPI

- 描述

    获取物品编号PROJECTILE_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileGroup | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_projectile_group_kv(item_key, "key")
```

---

## get_ability_key_projectile_group_kv

method in GameAPI

- 描述

    获取技能编号PROJECTILE_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileGroup | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_projectile_group_kv(ability_key, "key")
```

---

## get_modifier_key_projectile_group_kv

method in GameAPI

- 描述

    获取魔法效果特效编号PROJECTILE_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileGroup | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_projectile_group_kv(modifier_key, "key")
```

---

## get_projectile_key_projectile_group_kv

method in GameAPI

- 描述

    获取特效编号PROJECTILE_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileGroup | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_projectile_group_kv(projectile_key, "key")
```

---

## get_destructible_key_projectile_group_kv

method in GameAPI

- 描述

    获取可破坏物编号PROJECTILE_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileGroup | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_projectile_group_kv(destructible_key, "key")
```

---

## get_tech_key_projectile_group_kv

method in GameAPI

- 描述

    获取科技编号PROJECTILE_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileGroup | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_projectile_group_kv(tech_key, "key")
```

---

## get_icon_id_projectile_group_kv

method in GameAPI

- 描述

    获取图片PROJECTILE_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileGroup | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_projectile_group_kv(1, "key")
```

---

## get_physics_entity_key_projectile_group_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型PROJECTILE_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileGroup | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_projectile_group_kv(1, "key")
```

---

## get_unit_key_destructible_entity_kv

method in GameAPI

- 描述

    获取单位编号DESTRUCTIBLE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Destructible | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_destructible_entity_kv(unit_key, "key")
```

---

## get_item_key_destructible_entity_kv

method in GameAPI

- 描述

    获取物品编号DESTRUCTIBLE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Destructible | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_destructible_entity_kv(item_key, "key")
```

---

## get_ability_key_destructible_entity_kv

method in GameAPI

- 描述

    获取技能编号DESTRUCTIBLE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Destructible | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_destructible_entity_kv(ability_key, "key")
```

---

## get_modifier_key_destructible_entity_kv

method in GameAPI

- 描述

    获取魔法效果特效编号DESTRUCTIBLE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Destructible | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_destructible_entity_kv(modifier_key, "key")
```

---

## get_projectile_key_destructible_entity_kv

method in GameAPI

- 描述

    获取特效编号DESTRUCTIBLE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Destructible | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_destructible_entity_kv(projectile_key, "key")
```

---

## get_destructible_key_destructible_entity_kv

method in GameAPI

- 描述

    获取可破坏物编号DESTRUCTIBLE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Destructible | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_destructible_entity_kv(destructible_key, "key")
```

---

## get_tech_key_destructible_entity_kv

method in GameAPI

- 描述

    获取科技编号DESTRUCTIBLE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Destructible | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_destructible_entity_kv(tech_key, "key")
```

---

## get_icon_id_destructible_entity_kv

method in GameAPI

- 描述

    获取图片DESTRUCTIBLE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Destructible | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_destructible_entity_kv(1, "key")
```

---

## get_physics_entity_key_destructible_entity_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型DESTRUCTIBLE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Destructible | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_destructible_entity_kv(1, "key")
```

---

## get_unit_key_destructible_name_kv

method in GameAPI

- 描述

    获取单位编号DESTRUCTIBLE_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DestructibleKey | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_destructible_name_kv(unit_key, "key")
```

---

## get_item_key_destructible_name_kv

method in GameAPI

- 描述

    获取物品编号DESTRUCTIBLE_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DestructibleKey | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_destructible_name_kv(item_key, "key")
```

---

## get_ability_key_destructible_name_kv

method in GameAPI

- 描述

    获取技能编号DESTRUCTIBLE_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DestructibleKey | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_destructible_name_kv(ability_key, "key")
```

---

## get_modifier_key_destructible_name_kv

method in GameAPI

- 描述

    获取魔法效果特效编号DESTRUCTIBLE_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DestructibleKey | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_destructible_name_kv(modifier_key, "key")
```

---

## get_projectile_key_destructible_name_kv

method in GameAPI

- 描述

    获取特效编号DESTRUCTIBLE_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DestructibleKey | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_destructible_name_kv(projectile_key, "key")
```

---

## get_destructible_key_destructible_name_kv

method in GameAPI

- 描述

    获取可破坏物编号DESTRUCTIBLE_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DestructibleKey | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_destructible_name_kv(destructible_key, "key")
```

---

## get_tech_key_destructible_name_kv

method in GameAPI

- 描述

    获取科技编号DESTRUCTIBLE_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DestructibleKey | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_destructible_name_kv(tech_key, "key")
```

---

## get_icon_id_destructible_name_kv

method in GameAPI

- 描述

    获取图片DESTRUCTIBLE_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DestructibleKey | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_destructible_name_kv(1, "key")
```

---

## get_physics_entity_key_destructible_name_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型DESTRUCTIBLE_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DestructibleKey | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_destructible_name_kv(1, "key")
```

---

## get_unit_key_sound_entity_kv

method in GameAPI

- 描述

    获取单位编号SOUND_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SoundEntity | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_sound_entity_kv(unit_key, "key")
```

---

## get_item_key_sound_entity_kv

method in GameAPI

- 描述

    获取物品编号SOUND_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SoundEntity | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_sound_entity_kv(item_key, "key")
```

---

## get_ability_key_sound_entity_kv

method in GameAPI

- 描述

    获取技能编号SOUND_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SoundEntity | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_sound_entity_kv(ability_key, "key")
```

---

## get_modifier_key_sound_entity_kv

method in GameAPI

- 描述

    获取魔法效果特效编号SOUND_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SoundEntity | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_sound_entity_kv(modifier_key, "key")
```

---

## get_projectile_key_sound_entity_kv

method in GameAPI

- 描述

    获取特效编号SOUND_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SoundEntity | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_sound_entity_kv(projectile_key, "key")
```

---

## get_destructible_key_sound_entity_kv

method in GameAPI

- 描述

    获取可破坏物编号SOUND_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SoundEntity | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_sound_entity_kv(destructible_key, "key")
```

---

## get_tech_key_sound_entity_kv

method in GameAPI

- 描述

    获取科技编号SOUND_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SoundEntity | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_sound_entity_kv(tech_key, "key")
```

---

## get_icon_id_sound_entity_kv

method in GameAPI

- 描述

    获取图片SOUND_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SoundEntity | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_sound_entity_kv(1, "key")
```

---

## get_physics_entity_key_sound_entity_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型SOUND_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SoundEntity | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_sound_entity_kv(1, "key")
```

---

## get_unit_key_audio_key_kv

method in GameAPI

- 描述

    获取单位编号AUDIO_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AudioKey | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_audio_key_kv(unit_key, "key")
```

---

## get_item_key_audio_key_kv

method in GameAPI

- 描述

    获取物品编号AUDIO_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AudioKey | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_audio_key_kv(item_key, "key")
```

---

## get_ability_key_audio_key_kv

method in GameAPI

- 描述

    获取技能编号AUDIO_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AudioKey | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_audio_key_kv(ability_key, "key")
```

---

## get_modifier_key_audio_key_kv

method in GameAPI

- 描述

    获取魔法效果特效编号AUDIO_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AudioKey | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_audio_key_kv(modifier_key, "key")
```

---

## get_projectile_key_audio_key_kv

method in GameAPI

- 描述

    获取特效编号AUDIO_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AudioKey | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_audio_key_kv(projectile_key, "key")
```

---

## get_destructible_key_audio_key_kv

method in GameAPI

- 描述

    获取可破坏物编号AUDIO_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AudioKey | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_audio_key_kv(destructible_key, "key")
```

---

## get_tech_key_audio_key_kv

method in GameAPI

- 描述

    获取科技编号AUDIO_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AudioKey | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_audio_key_kv(tech_key, "key")
```

---

## get_icon_id_audio_key_kv

method in GameAPI

- 描述

    获取图片AUDIO_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AudioKey | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_audio_key_kv(1, "key")
```

---

## get_physics_entity_key_audio_key_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型AUDIO_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AudioKey | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_audio_key_kv(1, "key")
```

---

## get_unit_key_game_mode_kv

method in GameAPI

- 描述

    获取单位编号GAME_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.GameMode | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_game_mode_kv(unit_key, "key")
```

---

## get_item_key_game_mode_kv

method in GameAPI

- 描述

    获取物品编号GAME_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.GameMode | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_game_mode_kv(item_key, "key")
```

---

## get_ability_key_game_mode_kv

method in GameAPI

- 描述

    获取技能编号GAME_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.GameMode | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_game_mode_kv(ability_key, "key")
```

---

## get_modifier_key_game_mode_kv

method in GameAPI

- 描述

    获取魔法效果特效编号GAME_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.GameMode | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_game_mode_kv(modifier_key, "key")
```

---

## get_projectile_key_game_mode_kv

method in GameAPI

- 描述

    获取特效编号GAME_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.GameMode | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_game_mode_kv(projectile_key, "key")
```

---

## get_destructible_key_game_mode_kv

method in GameAPI

- 描述

    获取可破坏物编号GAME_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.GameMode | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_game_mode_kv(destructible_key, "key")
```

---

## get_tech_key_game_mode_kv

method in GameAPI

- 描述

    获取科技编号GAME_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.GameMode | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_game_mode_kv(tech_key, "key")
```

---

## get_icon_id_game_mode_kv

method in GameAPI

- 描述

    获取图片GAME_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.GameMode | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_game_mode_kv(1, "key")
```

---

## get_physics_entity_key_game_mode_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型GAME_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.GameMode | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_game_mode_kv(1, "key")
```

---

## get_unit_key_player_kv

method in GameAPI

- 描述

    获取单位编号PLAYER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Role | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_player_kv(unit_key, "key")
```

---

## get_item_key_player_kv

method in GameAPI

- 描述

    获取物品编号PLAYER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Role | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_player_kv(item_key, "key")
```

---

## get_ability_key_player_kv

method in GameAPI

- 描述

    获取技能编号PLAYER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Role | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_player_kv(ability_key, "key")
```

---

## get_modifier_key_player_kv

method in GameAPI

- 描述

    获取魔法效果特效编号PLAYER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Role | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_player_kv(modifier_key, "key")
```

---

## get_projectile_key_player_kv

method in GameAPI

- 描述

    获取特效编号PLAYER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Role | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_player_kv(projectile_key, "key")
```

---

## get_destructible_key_player_kv

method in GameAPI

- 描述

    获取可破坏物编号PLAYER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Role | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_player_kv(destructible_key, "key")
```

---

## get_tech_key_player_kv

method in GameAPI

- 描述

    获取科技编号PLAYER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Role | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_player_kv(tech_key, "key")
```

---

## get_icon_id_player_kv

method in GameAPI

- 描述

    获取图片PLAYER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Role | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_player_kv(1, "key")
```

---

## get_physics_entity_key_player_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型PLAYER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Role | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_player_kv(1, "key")
```

---

## get_unit_key_player_group_kv

method in GameAPI

- 描述

    获取单位编号PLAYER_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleGroup | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_player_group_kv(unit_key, "key")
```

---

## get_item_key_player_group_kv

method in GameAPI

- 描述

    获取物品编号PLAYER_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleGroup | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_player_group_kv(item_key, "key")
```

---

## get_ability_key_player_group_kv

method in GameAPI

- 描述

    获取技能编号PLAYER_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleGroup | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_player_group_kv(ability_key, "key")
```

---

## get_modifier_key_player_group_kv

method in GameAPI

- 描述

    获取魔法效果特效编号PLAYER_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleGroup | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_player_group_kv(modifier_key, "key")
```

---

## get_projectile_key_player_group_kv

method in GameAPI

- 描述

    获取特效编号PLAYER_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleGroup | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_player_group_kv(projectile_key, "key")
```

---

## get_destructible_key_player_group_kv

method in GameAPI

- 描述

    获取可破坏物编号PLAYER_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleGroup | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_player_group_kv(destructible_key, "key")
```

---

## get_tech_key_player_group_kv

method in GameAPI

- 描述

    获取科技编号PLAYER_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleGroup | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_player_group_kv(tech_key, "key")
```

---

## get_icon_id_player_group_kv

method in GameAPI

- 描述

    获取图片PLAYER_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleGroup | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_player_group_kv(1, "key")
```

---

## get_physics_entity_key_player_group_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型PLAYER_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleGroup | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_player_group_kv(1, "key")
```

---

## get_unit_key_role_res_key_kv

method in GameAPI

- 描述

    获取单位编号ROLE_RES_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleResKey | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_role_res_key_kv(unit_key, "key")
```

---

## get_item_key_role_res_key_kv

method in GameAPI

- 描述

    获取物品编号ROLE_RES_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleResKey | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_role_res_key_kv(item_key, "key")
```

---

## get_ability_key_role_res_key_kv

method in GameAPI

- 描述

    获取技能编号ROLE_RES_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleResKey | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_role_res_key_kv(ability_key, "key")
```

---

## get_modifier_key_role_res_key_kv

method in GameAPI

- 描述

    获取魔法效果特效编号ROLE_RES_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleResKey | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_role_res_key_kv(modifier_key, "key")
```

---

## get_projectile_key_role_res_key_kv

method in GameAPI

- 描述

    获取特效编号ROLE_RES_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleResKey | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_role_res_key_kv(projectile_key, "key")
```

---

## get_destructible_key_role_res_key_kv

method in GameAPI

- 描述

    获取可破坏物编号ROLE_RES_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleResKey | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_role_res_key_kv(destructible_key, "key")
```

---

## get_tech_key_role_res_key_kv

method in GameAPI

- 描述

    获取科技编号ROLE_RES_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleResKey | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_role_res_key_kv(tech_key, "key")
```

---

## get_icon_id_role_res_key_kv

method in GameAPI

- 描述

    获取图片ROLE_RES_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleResKey | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_role_res_key_kv(1, "key")
```

---

## get_physics_entity_key_role_res_key_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型ROLE_RES_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleResKey | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_role_res_key_kv(1, "key")
```

---

## get_unit_key_role_status_kv

method in GameAPI

- 描述

    获取单位编号ROLE_STATUS键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleStatus | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_role_status_kv(unit_key, "key")
```

---

## get_item_key_role_status_kv

method in GameAPI

- 描述

    获取物品编号ROLE_STATUS键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleStatus | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_role_status_kv(item_key, "key")
```

---

## get_ability_key_role_status_kv

method in GameAPI

- 描述

    获取技能编号ROLE_STATUS键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleStatus | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_role_status_kv(ability_key, "key")
```

---

## get_modifier_key_role_status_kv

method in GameAPI

- 描述

    获取魔法效果特效编号ROLE_STATUS键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleStatus | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_role_status_kv(modifier_key, "key")
```

---

## get_projectile_key_role_status_kv

method in GameAPI

- 描述

    获取特效编号ROLE_STATUS键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleStatus | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_role_status_kv(projectile_key, "key")
```

---

## get_destructible_key_role_status_kv

method in GameAPI

- 描述

    获取可破坏物编号ROLE_STATUS键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleStatus | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_role_status_kv(destructible_key, "key")
```

---

## get_tech_key_role_status_kv

method in GameAPI

- 描述

    获取科技编号ROLE_STATUS键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleStatus | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_role_status_kv(tech_key, "key")
```

---

## get_icon_id_role_status_kv

method in GameAPI

- 描述

    获取图片ROLE_STATUS键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleStatus | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_role_status_kv(1, "key")
```

---

## get_physics_entity_key_role_status_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型ROLE_STATUS键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleStatus | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_role_status_kv(1, "key")
```

---

## get_unit_key_role_type_kv

method in GameAPI

- 描述

    获取单位编号ROLE_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleType | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_role_type_kv(unit_key, "key")
```

---

## get_item_key_role_type_kv

method in GameAPI

- 描述

    获取物品编号ROLE_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleType | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_role_type_kv(item_key, "key")
```

---

## get_ability_key_role_type_kv

method in GameAPI

- 描述

    获取技能编号ROLE_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleType | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_role_type_kv(ability_key, "key")
```

---

## get_modifier_key_role_type_kv

method in GameAPI

- 描述

    获取魔法效果特效编号ROLE_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleType | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_role_type_kv(modifier_key, "key")
```

---

## get_projectile_key_role_type_kv

method in GameAPI

- 描述

    获取特效编号ROLE_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleType | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_role_type_kv(projectile_key, "key")
```

---

## get_destructible_key_role_type_kv

method in GameAPI

- 描述

    获取可破坏物编号ROLE_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleType | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_role_type_kv(destructible_key, "key")
```

---

## get_tech_key_role_type_kv

method in GameAPI

- 描述

    获取科技编号ROLE_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleType | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_role_type_kv(tech_key, "key")
```

---

## get_icon_id_role_type_kv

method in GameAPI

- 描述

    获取图片ROLE_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleType | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_role_type_kv(1, "key")
```

---

## get_physics_entity_key_role_type_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型ROLE_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleType | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_role_type_kv(1, "key")
```

---

## get_unit_key_role_relation_kv

method in GameAPI

- 描述

    获取单位编号ROLE_RELATION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleRelation | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_role_relation_kv(unit_key, "key")
```

---

## get_item_key_role_relation_kv

method in GameAPI

- 描述

    获取物品编号ROLE_RELATION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleRelation | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_role_relation_kv(item_key, "key")
```

---

## get_ability_key_role_relation_kv

method in GameAPI

- 描述

    获取技能编号ROLE_RELATION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleRelation | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_role_relation_kv(ability_key, "key")
```

---

## get_modifier_key_role_relation_kv

method in GameAPI

- 描述

    获取魔法效果特效编号ROLE_RELATION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleRelation | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_role_relation_kv(modifier_key, "key")
```

---

## get_projectile_key_role_relation_kv

method in GameAPI

- 描述

    获取特效编号ROLE_RELATION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleRelation | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_role_relation_kv(projectile_key, "key")
```

---

## get_destructible_key_role_relation_kv

method in GameAPI

- 描述

    获取可破坏物编号ROLE_RELATION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleRelation | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_role_relation_kv(destructible_key, "key")
```

---

## get_tech_key_role_relation_kv

method in GameAPI

- 描述

    获取科技编号ROLE_RELATION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleRelation | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_role_relation_kv(tech_key, "key")
```

---

## get_icon_id_role_relation_kv

method in GameAPI

- 描述

    获取图片ROLE_RELATION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleRelation | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_role_relation_kv(1, "key")
```

---

## get_physics_entity_key_role_relation_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型ROLE_RELATION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleRelation | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_role_relation_kv(1, "key")
```

---

## get_unit_key_team_kv

method in GameAPI

- 描述

    获取单位编号TEAM键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Camp | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_team_kv(unit_key, "key")
```

---

## get_item_key_team_kv

method in GameAPI

- 描述

    获取物品编号TEAM键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Camp | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_team_kv(item_key, "key")
```

---

## get_ability_key_team_kv

method in GameAPI

- 描述

    获取技能编号TEAM键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Camp | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_team_kv(ability_key, "key")
```

---

## get_modifier_key_team_kv

method in GameAPI

- 描述

    获取魔法效果特效编号TEAM键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Camp | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_team_kv(modifier_key, "key")
```

---

## get_projectile_key_team_kv

method in GameAPI

- 描述

    获取特效编号TEAM键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Camp | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_team_kv(projectile_key, "key")
```

---

## get_destructible_key_team_kv

method in GameAPI

- 描述

    获取可破坏物编号TEAM键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Camp | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_team_kv(destructible_key, "key")
```

---

## get_tech_key_team_kv

method in GameAPI

- 描述

    获取科技编号TEAM键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Camp | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_team_kv(tech_key, "key")
```

---

## get_icon_id_team_kv

method in GameAPI

- 描述

    获取图片TEAM键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Camp | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_team_kv(1, "key")
```

---

## get_physics_entity_key_team_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型TEAM键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Camp | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_team_kv(1, "key")
```

---

## get_unit_key_point_kv

method in GameAPI

- 描述

    获取单位编号POINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FPoint | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_point_kv(unit_key, "key")
```

---

## get_item_key_point_kv

method in GameAPI

- 描述

    获取物品编号POINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FPoint | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_point_kv(item_key, "key")
```

---

## get_ability_key_point_kv

method in GameAPI

- 描述

    获取技能编号POINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FPoint | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_point_kv(ability_key, "key")
```

---

## get_modifier_key_point_kv

method in GameAPI

- 描述

    获取魔法效果特效编号POINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FPoint | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_point_kv(modifier_key, "key")
```

---

## get_projectile_key_point_kv

method in GameAPI

- 描述

    获取特效编号POINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FPoint | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_point_kv(projectile_key, "key")
```

---

## get_destructible_key_point_kv

method in GameAPI

- 描述

    获取可破坏物编号POINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FPoint | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_point_kv(destructible_key, "key")
```

---

## get_tech_key_point_kv

method in GameAPI

- 描述

    获取科技编号POINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FPoint | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_point_kv(tech_key, "key")
```

---

## get_icon_id_point_kv

method in GameAPI

- 描述

    获取图片POINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FPoint | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_point_kv(1, "key")
```

---

## get_physics_entity_key_point_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型POINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FPoint | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_point_kv(1, "key")
```

---

## get_unit_key_vector3_kv

method in GameAPI

- 描述

    获取单位编号VECTOR3键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3 | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_vector3_kv(unit_key, "key")
```

---

## get_item_key_vector3_kv

method in GameAPI

- 描述

    获取物品编号VECTOR3键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3 | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_vector3_kv(item_key, "key")
```

---

## get_ability_key_vector3_kv

method in GameAPI

- 描述

    获取技能编号VECTOR3键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3 | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_vector3_kv(ability_key, "key")
```

---

## get_modifier_key_vector3_kv

method in GameAPI

- 描述

    获取魔法效果特效编号VECTOR3键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3 | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_vector3_kv(modifier_key, "key")
```

---

## get_projectile_key_vector3_kv

method in GameAPI

- 描述

    获取特效编号VECTOR3键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3 | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_vector3_kv(projectile_key, "key")
```

---

## get_destructible_key_vector3_kv

method in GameAPI

- 描述

    获取可破坏物编号VECTOR3键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3 | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_vector3_kv(destructible_key, "key")
```

---

## get_tech_key_vector3_kv

method in GameAPI

- 描述

    获取科技编号VECTOR3键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3 | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_vector3_kv(tech_key, "key")
```

---

## get_icon_id_vector3_kv

method in GameAPI

- 描述

    获取图片VECTOR3键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3 | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_vector3_kv(1, "key")
```

---

## get_physics_entity_key_vector3_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型VECTOR3键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3 | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_vector3_kv(1, "key")
```

---

## get_unit_key_rotation_kv

method in GameAPI

- 描述

    获取单位编号ROTATION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FRotation | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_rotation_kv(unit_key, "key")
```

---

## get_item_key_rotation_kv

method in GameAPI

- 描述

    获取物品编号ROTATION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FRotation | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_rotation_kv(item_key, "key")
```

---

## get_ability_key_rotation_kv

method in GameAPI

- 描述

    获取技能编号ROTATION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FRotation | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_rotation_kv(ability_key, "key")
```

---

## get_modifier_key_rotation_kv

method in GameAPI

- 描述

    获取魔法效果特效编号ROTATION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FRotation | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_rotation_kv(modifier_key, "key")
```

---

## get_projectile_key_rotation_kv

method in GameAPI

- 描述

    获取特效编号ROTATION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FRotation | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_rotation_kv(projectile_key, "key")
```

---

## get_destructible_key_rotation_kv

method in GameAPI

- 描述

    获取可破坏物编号ROTATION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FRotation | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_rotation_kv(destructible_key, "key")
```

---

## get_tech_key_rotation_kv

method in GameAPI

- 描述

    获取科技编号ROTATION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FRotation | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_rotation_kv(tech_key, "key")
```

---

## get_icon_id_rotation_kv

method in GameAPI

- 描述

    获取图片ROTATION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FRotation | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_rotation_kv(1, "key")
```

---

## get_physics_entity_key_rotation_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型ROTATION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FRotation | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_rotation_kv(1, "key")
```

---

## get_unit_key_point_list_kv

method in GameAPI

- 描述

    获取单位编号POINT_LIST键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Road | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_point_list_kv(unit_key, "key")
```

---

## get_item_key_point_list_kv

method in GameAPI

- 描述

    获取物品编号POINT_LIST键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Road | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_point_list_kv(item_key, "key")
```

---

## get_ability_key_point_list_kv

method in GameAPI

- 描述

    获取技能编号POINT_LIST键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Road | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_point_list_kv(ability_key, "key")
```

---

## get_modifier_key_point_list_kv

method in GameAPI

- 描述

    获取魔法效果特效编号POINT_LIST键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Road | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_point_list_kv(modifier_key, "key")
```

---

## get_projectile_key_point_list_kv

method in GameAPI

- 描述

    获取特效编号POINT_LIST键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Road | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_point_list_kv(projectile_key, "key")
```

---

## get_destructible_key_point_list_kv

method in GameAPI

- 描述

    获取可破坏物编号POINT_LIST键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Road | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_point_list_kv(destructible_key, "key")
```

---

## get_tech_key_point_list_kv

method in GameAPI

- 描述

    获取科技编号POINT_LIST键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Road | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_point_list_kv(tech_key, "key")
```

---

## get_icon_id_point_list_kv

method in GameAPI

- 描述

    获取图片POINT_LIST键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Road | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_point_list_kv(1, "key")
```

---

## get_physics_entity_key_point_list_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型POINT_LIST键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Road | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_point_list_kv(1, "key")
```

---

## get_unit_key_rectangle_kv

method in GameAPI

- 描述

    获取单位编号RECTANGLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RecArea | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_rectangle_kv(unit_key, "key")
```

---

## get_item_key_rectangle_kv

method in GameAPI

- 描述

    获取物品编号RECTANGLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RecArea | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_rectangle_kv(item_key, "key")
```

---

## get_ability_key_rectangle_kv

method in GameAPI

- 描述

    获取技能编号RECTANGLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RecArea | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_rectangle_kv(ability_key, "key")
```

---

## get_modifier_key_rectangle_kv

method in GameAPI

- 描述

    获取魔法效果特效编号RECTANGLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RecArea | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_rectangle_kv(modifier_key, "key")
```

---

## get_projectile_key_rectangle_kv

method in GameAPI

- 描述

    获取特效编号RECTANGLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RecArea | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_rectangle_kv(projectile_key, "key")
```

---

## get_destructible_key_rectangle_kv

method in GameAPI

- 描述

    获取可破坏物编号RECTANGLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RecArea | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_rectangle_kv(destructible_key, "key")
```

---

## get_tech_key_rectangle_kv

method in GameAPI

- 描述

    获取科技编号RECTANGLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RecArea | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_rectangle_kv(tech_key, "key")
```

---

## get_icon_id_rectangle_kv

method in GameAPI

- 描述

    获取图片RECTANGLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RecArea | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_rectangle_kv(1, "key")
```

---

## get_physics_entity_key_rectangle_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型RECTANGLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RecArea | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_rectangle_kv(1, "key")
```

---

## get_unit_key_round_area_kv

method in GameAPI

- 描述

    获取单位编号ROUND_AREA键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CirArea | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_round_area_kv(unit_key, "key")
```

---

## get_item_key_round_area_kv

method in GameAPI

- 描述

    获取物品编号ROUND_AREA键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CirArea | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_round_area_kv(item_key, "key")
```

---

## get_ability_key_round_area_kv

method in GameAPI

- 描述

    获取技能编号ROUND_AREA键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CirArea | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_round_area_kv(ability_key, "key")
```

---

## get_modifier_key_round_area_kv

method in GameAPI

- 描述

    获取魔法效果特效编号ROUND_AREA键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CirArea | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_round_area_kv(modifier_key, "key")
```

---

## get_projectile_key_round_area_kv

method in GameAPI

- 描述

    获取特效编号ROUND_AREA键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CirArea | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_round_area_kv(projectile_key, "key")
```

---

## get_destructible_key_round_area_kv

method in GameAPI

- 描述

    获取可破坏物编号ROUND_AREA键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CirArea | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_round_area_kv(destructible_key, "key")
```

---

## get_tech_key_round_area_kv

method in GameAPI

- 描述

    获取科技编号ROUND_AREA键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CirArea | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_round_area_kv(tech_key, "key")
```

---

## get_icon_id_round_area_kv

method in GameAPI

- 描述

    获取图片ROUND_AREA键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CirArea | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_round_area_kv(1, "key")
```

---

## get_physics_entity_key_round_area_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型ROUND_AREA键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CirArea | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_round_area_kv(1, "key")
```

---

## get_unit_key_polygon_kv

method in GameAPI

- 描述

    获取单位编号POLYGON键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PolyArea | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_polygon_kv(unit_key, "key")
```

---

## get_item_key_polygon_kv

method in GameAPI

- 描述

    获取物品编号POLYGON键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PolyArea | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_polygon_kv(item_key, "key")
```

---

## get_ability_key_polygon_kv

method in GameAPI

- 描述

    获取技能编号POLYGON键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PolyArea | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_polygon_kv(ability_key, "key")
```

---

## get_modifier_key_polygon_kv

method in GameAPI

- 描述

    获取魔法效果特效编号POLYGON键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PolyArea | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_polygon_kv(modifier_key, "key")
```

---

## get_projectile_key_polygon_kv

method in GameAPI

- 描述

    获取特效编号POLYGON键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PolyArea | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_polygon_kv(projectile_key, "key")
```

---

## get_destructible_key_polygon_kv

method in GameAPI

- 描述

    获取可破坏物编号POLYGON键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PolyArea | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_polygon_kv(destructible_key, "key")
```

---

## get_tech_key_polygon_kv

method in GameAPI

- 描述

    获取科技编号POLYGON键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PolyArea | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_polygon_kv(tech_key, "key")
```

---

## get_icon_id_polygon_kv

method in GameAPI

- 描述

    获取图片POLYGON键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PolyArea | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_polygon_kv(1, "key")
```

---

## get_physics_entity_key_polygon_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型POLYGON键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PolyArea | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_polygon_kv(1, "key")
```

---

## get_unit_key_camera_kv

method in GameAPI

- 描述

    获取单位编号CAMERA键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Camera | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_camera_kv(unit_key, "key")
```

---

## get_item_key_camera_kv

method in GameAPI

- 描述

    获取物品编号CAMERA键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Camera | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_camera_kv(item_key, "key")
```

---

## get_ability_key_camera_kv

method in GameAPI

- 描述

    获取技能编号CAMERA键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Camera | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_camera_kv(ability_key, "key")
```

---

## get_modifier_key_camera_kv

method in GameAPI

- 描述

    获取魔法效果特效编号CAMERA键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Camera | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_camera_kv(modifier_key, "key")
```

---

## get_projectile_key_camera_kv

method in GameAPI

- 描述

    获取特效编号CAMERA键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Camera | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_camera_kv(projectile_key, "key")
```

---

## get_destructible_key_camera_kv

method in GameAPI

- 描述

    获取可破坏物编号CAMERA键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Camera | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_camera_kv(destructible_key, "key")
```

---

## get_tech_key_camera_kv

method in GameAPI

- 描述

    获取科技编号CAMERA键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Camera | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_camera_kv(tech_key, "key")
```

---

## get_icon_id_camera_kv

method in GameAPI

- 描述

    获取图片CAMERA键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Camera | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_camera_kv(1, "key")
```

---

## get_physics_entity_key_camera_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型CAMERA键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Camera | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_camera_kv(1, "key")
```

---

## get_unit_key_camline_kv

method in GameAPI

- 描述

    获取单位编号CAMLINE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CamlineID | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_camline_kv(unit_key, "key")
```

---

## get_item_key_camline_kv

method in GameAPI

- 描述

    获取物品编号CAMLINE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CamlineID | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_camline_kv(item_key, "key")
```

---

## get_ability_key_camline_kv

method in GameAPI

- 描述

    获取技能编号CAMLINE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CamlineID | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_camline_kv(ability_key, "key")
```

---

## get_modifier_key_camline_kv

method in GameAPI

- 描述

    获取魔法效果特效编号CAMLINE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CamlineID | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_camline_kv(modifier_key, "key")
```

---

## get_projectile_key_camline_kv

method in GameAPI

- 描述

    获取特效编号CAMLINE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CamlineID | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_camline_kv(projectile_key, "key")
```

---

## get_destructible_key_camline_kv

method in GameAPI

- 描述

    获取可破坏物编号CAMLINE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CamlineID | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_camline_kv(destructible_key, "key")
```

---

## get_tech_key_camline_kv

method in GameAPI

- 描述

    获取科技编号CAMLINE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CamlineID | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_camline_kv(tech_key, "key")
```

---

## get_icon_id_camline_kv

method in GameAPI

- 描述

    获取图片CAMLINE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CamlineID | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_camline_kv(1, "key")
```

---

## get_physics_entity_key_camline_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型CAMLINE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CamlineID | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_camline_kv(1, "key")
```

---

## get_unit_key_point_light_kv

method in GameAPI

- 描述

    获取单位编号POINT_LIGHT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PointLight | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_point_light_kv(unit_key, "key")
```

---

## get_item_key_point_light_kv

method in GameAPI

- 描述

    获取物品编号POINT_LIGHT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PointLight | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_point_light_kv(item_key, "key")
```

---

## get_ability_key_point_light_kv

method in GameAPI

- 描述

    获取技能编号POINT_LIGHT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PointLight | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_point_light_kv(ability_key, "key")
```

---

## get_modifier_key_point_light_kv

method in GameAPI

- 描述

    获取魔法效果特效编号POINT_LIGHT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PointLight | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_point_light_kv(modifier_key, "key")
```

---

## get_projectile_key_point_light_kv

method in GameAPI

- 描述

    获取特效编号POINT_LIGHT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PointLight | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_point_light_kv(projectile_key, "key")
```

---

## get_destructible_key_point_light_kv

method in GameAPI

- 描述

    获取可破坏物编号POINT_LIGHT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PointLight | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_point_light_kv(destructible_key, "key")
```

---

## get_tech_key_point_light_kv

method in GameAPI

- 描述

    获取科技编号POINT_LIGHT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PointLight | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_point_light_kv(tech_key, "key")
```

---

## get_icon_id_point_light_kv

method in GameAPI

- 描述

    获取图片POINT_LIGHT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PointLight | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_point_light_kv(1, "key")
```

---

## get_physics_entity_key_point_light_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型POINT_LIGHT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PointLight | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_point_light_kv(1, "key")
```

---

## get_unit_key_spot_light_kv

method in GameAPI

- 描述

    获取单位编号SPOT_LIGHT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SpotLight | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_spot_light_kv(unit_key, "key")
```

---

## get_item_key_spot_light_kv

method in GameAPI

- 描述

    获取物品编号SPOT_LIGHT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SpotLight | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_spot_light_kv(item_key, "key")
```

---

## get_ability_key_spot_light_kv

method in GameAPI

- 描述

    获取技能编号SPOT_LIGHT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SpotLight | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_spot_light_kv(ability_key, "key")
```

---

## get_modifier_key_spot_light_kv

method in GameAPI

- 描述

    获取魔法效果特效编号SPOT_LIGHT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SpotLight | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_spot_light_kv(modifier_key, "key")
```

---

## get_projectile_key_spot_light_kv

method in GameAPI

- 描述

    获取特效编号SPOT_LIGHT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SpotLight | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_spot_light_kv(projectile_key, "key")
```

---

## get_destructible_key_spot_light_kv

method in GameAPI

- 描述

    获取可破坏物编号SPOT_LIGHT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SpotLight | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_spot_light_kv(destructible_key, "key")
```

---

## get_tech_key_spot_light_kv

method in GameAPI

- 描述

    获取科技编号SPOT_LIGHT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SpotLight | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_spot_light_kv(tech_key, "key")
```

---

## get_icon_id_spot_light_kv

method in GameAPI

- 描述

    获取图片SPOT_LIGHT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SpotLight | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_spot_light_kv(1, "key")
```

---

## get_physics_entity_key_spot_light_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型SPOT_LIGHT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SpotLight | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_spot_light_kv(1, "key")
```

---

## get_unit_key_fog_kv

method in GameAPI

- 描述

    获取单位编号FOG键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fog | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_fog_kv(unit_key, "key")
```

---

## get_item_key_fog_kv

method in GameAPI

- 描述

    获取物品编号FOG键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fog | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_fog_kv(item_key, "key")
```

---

## get_ability_key_fog_kv

method in GameAPI

- 描述

    获取技能编号FOG键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fog | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_fog_kv(ability_key, "key")
```

---

## get_modifier_key_fog_kv

method in GameAPI

- 描述

    获取魔法效果特效编号FOG键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fog | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_fog_kv(modifier_key, "key")
```

---

## get_projectile_key_fog_kv

method in GameAPI

- 描述

    获取特效编号FOG键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fog | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_fog_kv(projectile_key, "key")
```

---

## get_destructible_key_fog_kv

method in GameAPI

- 描述

    获取可破坏物编号FOG键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fog | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_fog_kv(destructible_key, "key")
```

---

## get_tech_key_fog_kv

method in GameAPI

- 描述

    获取科技编号FOG键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fog | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_fog_kv(tech_key, "key")
```

---

## get_icon_id_fog_kv

method in GameAPI

- 描述

    获取图片FOG键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fog | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_fog_kv(1, "key")
```

---

## get_physics_entity_key_fog_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型FOG键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fog | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_fog_kv(1, "key")
```

---

## get_unit_key_scene_sound_kv

method in GameAPI

- 描述

    获取单位编号SCENE_SOUND键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SceneSound | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_scene_sound_kv(unit_key, "key")
```

---

## get_item_key_scene_sound_kv

method in GameAPI

- 描述

    获取物品编号SCENE_SOUND键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SceneSound | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_scene_sound_kv(item_key, "key")
```

---

## get_ability_key_scene_sound_kv

method in GameAPI

- 描述

    获取技能编号SCENE_SOUND键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SceneSound | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_scene_sound_kv(ability_key, "key")
```

---

## get_modifier_key_scene_sound_kv

method in GameAPI

- 描述

    获取魔法效果特效编号SCENE_SOUND键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SceneSound | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_scene_sound_kv(modifier_key, "key")
```

---

## get_projectile_key_scene_sound_kv

method in GameAPI

- 描述

    获取特效编号SCENE_SOUND键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SceneSound | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_scene_sound_kv(projectile_key, "key")
```

---

## get_destructible_key_scene_sound_kv

method in GameAPI

- 描述

    获取可破坏物编号SCENE_SOUND键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SceneSound | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_scene_sound_kv(destructible_key, "key")
```

---

## get_tech_key_scene_sound_kv

method in GameAPI

- 描述

    获取科技编号SCENE_SOUND键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SceneSound | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_scene_sound_kv(tech_key, "key")
```

---

## get_icon_id_scene_sound_kv

method in GameAPI

- 描述

    获取图片SCENE_SOUND键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SceneSound | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_scene_sound_kv(1, "key")
```

---

## get_physics_entity_key_scene_sound_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型SCENE_SOUND键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SceneSound | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_scene_sound_kv(1, "key")
```

---

## get_unit_key_model_kv

method in GameAPI

- 描述

    获取单位编号MODEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModelKey | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_model_kv(unit_key, "key")
```

---

## get_item_key_model_kv

method in GameAPI

- 描述

    获取物品编号MODEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModelKey | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_model_kv(item_key, "key")
```

---

## get_ability_key_model_kv

method in GameAPI

- 描述

    获取技能编号MODEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModelKey | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_model_kv(ability_key, "key")
```

---

## get_modifier_key_model_kv

method in GameAPI

- 描述

    获取魔法效果特效编号MODEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModelKey | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_model_kv(modifier_key, "key")
```

---

## get_projectile_key_model_kv

method in GameAPI

- 描述

    获取特效编号MODEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModelKey | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_model_kv(projectile_key, "key")
```

---

## get_destructible_key_model_kv

method in GameAPI

- 描述

    获取可破坏物编号MODEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModelKey | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_model_kv(destructible_key, "key")
```

---

## get_tech_key_model_kv

method in GameAPI

- 描述

    获取科技编号MODEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModelKey | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_model_kv(tech_key, "key")
```

---

## get_icon_id_model_kv

method in GameAPI

- 描述

    获取图片MODEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModelKey | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_model_kv(1, "key")
```

---

## get_physics_entity_key_model_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型MODEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModelKey | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_model_kv(1, "key")
```

---

## get_unit_key_sfx_entity_kv

method in GameAPI

- 描述

    获取单位编号SFX_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sfx | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_sfx_entity_kv(unit_key, "key")
```

---

## get_item_key_sfx_entity_kv

method in GameAPI

- 描述

    获取物品编号SFX_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sfx | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_sfx_entity_kv(item_key, "key")
```

---

## get_ability_key_sfx_entity_kv

method in GameAPI

- 描述

    获取技能编号SFX_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sfx | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_sfx_entity_kv(ability_key, "key")
```

---

## get_modifier_key_sfx_entity_kv

method in GameAPI

- 描述

    获取魔法效果特效编号SFX_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sfx | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_sfx_entity_kv(modifier_key, "key")
```

---

## get_projectile_key_sfx_entity_kv

method in GameAPI

- 描述

    获取特效编号SFX_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sfx | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_sfx_entity_kv(projectile_key, "key")
```

---

## get_destructible_key_sfx_entity_kv

method in GameAPI

- 描述

    获取可破坏物编号SFX_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sfx | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_sfx_entity_kv(destructible_key, "key")
```

---

## get_tech_key_sfx_entity_kv

method in GameAPI

- 描述

    获取科技编号SFX_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sfx | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_sfx_entity_kv(tech_key, "key")
```

---

## get_icon_id_sfx_entity_kv

method in GameAPI

- 描述

    获取图片SFX_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sfx | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_sfx_entity_kv(1, "key")
```

---

## get_physics_entity_key_sfx_entity_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型SFX_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sfx | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_sfx_entity_kv(1, "key")
```

---

## get_unit_key_sfx_key_kv

method in GameAPI

- 描述

    获取单位编号SFX_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SfxKey | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_sfx_key_kv(unit_key, "key")
```

---

## get_item_key_sfx_key_kv

method in GameAPI

- 描述

    获取物品编号SFX_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SfxKey | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_sfx_key_kv(item_key, "key")
```

---

## get_ability_key_sfx_key_kv

method in GameAPI

- 描述

    获取技能编号SFX_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SfxKey | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_sfx_key_kv(ability_key, "key")
```

---

## get_modifier_key_sfx_key_kv

method in GameAPI

- 描述

    获取魔法效果特效编号SFX_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SfxKey | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_sfx_key_kv(modifier_key, "key")
```

---

## get_projectile_key_sfx_key_kv

method in GameAPI

- 描述

    获取特效编号SFX_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SfxKey | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_sfx_key_kv(projectile_key, "key")
```

---

## get_destructible_key_sfx_key_kv

method in GameAPI

- 描述

    获取可破坏物编号SFX_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SfxKey | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_sfx_key_kv(destructible_key, "key")
```

---

## get_tech_key_sfx_key_kv

method in GameAPI

- 描述

    获取科技编号SFX_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SfxKey | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_sfx_key_kv(tech_key, "key")
```

---

## get_icon_id_sfx_key_kv

method in GameAPI

- 描述

    获取图片SFX_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SfxKey | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_sfx_key_kv(1, "key")
```

---

## get_physics_entity_key_sfx_key_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型SFX_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SfxKey | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_sfx_key_kv(1, "key")
```

---

## get_unit_key_link_sfx_entity_kv

method in GameAPI

- 描述

    获取单位编号LINK_SFX_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LinkSfx | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_link_sfx_entity_kv(unit_key, "key")
```

---

## get_item_key_link_sfx_entity_kv

method in GameAPI

- 描述

    获取物品编号LINK_SFX_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LinkSfx | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_link_sfx_entity_kv(item_key, "key")
```

---

## get_ability_key_link_sfx_entity_kv

method in GameAPI

- 描述

    获取技能编号LINK_SFX_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LinkSfx | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_link_sfx_entity_kv(ability_key, "key")
```

---

## get_modifier_key_link_sfx_entity_kv

method in GameAPI

- 描述

    获取魔法效果特效编号LINK_SFX_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LinkSfx | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_link_sfx_entity_kv(modifier_key, "key")
```

---

## get_projectile_key_link_sfx_entity_kv

method in GameAPI

- 描述

    获取特效编号LINK_SFX_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LinkSfx | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_link_sfx_entity_kv(projectile_key, "key")
```

---

## get_destructible_key_link_sfx_entity_kv

method in GameAPI

- 描述

    获取可破坏物编号LINK_SFX_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LinkSfx | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_link_sfx_entity_kv(destructible_key, "key")
```

---

## get_tech_key_link_sfx_entity_kv

method in GameAPI

- 描述

    获取科技编号LINK_SFX_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LinkSfx | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_link_sfx_entity_kv(tech_key, "key")
```

---

## get_icon_id_link_sfx_entity_kv

method in GameAPI

- 描述

    获取图片LINK_SFX_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LinkSfx | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_link_sfx_entity_kv(1, "key")
```

---

## get_physics_entity_key_link_sfx_entity_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型LINK_SFX_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LinkSfx | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_link_sfx_entity_kv(1, "key")
```

---

## get_unit_key_link_sfx_key_kv

method in GameAPI

- 描述

    获取单位编号LINK_SFX_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LinkSfxKey | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_link_sfx_key_kv(unit_key, "key")
```

---

## get_item_key_link_sfx_key_kv

method in GameAPI

- 描述

    获取物品编号LINK_SFX_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LinkSfxKey | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_link_sfx_key_kv(item_key, "key")
```

---

## get_ability_key_link_sfx_key_kv

method in GameAPI

- 描述

    获取技能编号LINK_SFX_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LinkSfxKey | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_link_sfx_key_kv(ability_key, "key")
```

---

## get_modifier_key_link_sfx_key_kv

method in GameAPI

- 描述

    获取魔法效果特效编号LINK_SFX_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LinkSfxKey | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_link_sfx_key_kv(modifier_key, "key")
```

---

## get_projectile_key_link_sfx_key_kv

method in GameAPI

- 描述

    获取特效编号LINK_SFX_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LinkSfxKey | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_link_sfx_key_kv(projectile_key, "key")
```

---

## get_destructible_key_link_sfx_key_kv

method in GameAPI

- 描述

    获取可破坏物编号LINK_SFX_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LinkSfxKey | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_link_sfx_key_kv(destructible_key, "key")
```

---

## get_tech_key_link_sfx_key_kv

method in GameAPI

- 描述

    获取科技编号LINK_SFX_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LinkSfxKey | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_link_sfx_key_kv(tech_key, "key")
```

---

## get_icon_id_link_sfx_key_kv

method in GameAPI

- 描述

    获取图片LINK_SFX_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LinkSfxKey | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_link_sfx_key_kv(1, "key")
```

---

## get_physics_entity_key_link_sfx_key_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型LINK_SFX_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LinkSfxKey | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_link_sfx_key_kv(1, "key")
```

---

## get_unit_key_cursor_key_kv

method in GameAPI

- 描述

    获取单位编号CURSOR_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CursorKey | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_cursor_key_kv(unit_key, "key")
```

---

## get_item_key_cursor_key_kv

method in GameAPI

- 描述

    获取物品编号CURSOR_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CursorKey | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_cursor_key_kv(item_key, "key")
```

---

## get_ability_key_cursor_key_kv

method in GameAPI

- 描述

    获取技能编号CURSOR_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CursorKey | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_cursor_key_kv(ability_key, "key")
```

---

## get_modifier_key_cursor_key_kv

method in GameAPI

- 描述

    获取魔法效果特效编号CURSOR_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CursorKey | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_cursor_key_kv(modifier_key, "key")
```

---

## get_projectile_key_cursor_key_kv

method in GameAPI

- 描述

    获取特效编号CURSOR_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CursorKey | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_cursor_key_kv(projectile_key, "key")
```

---

## get_destructible_key_cursor_key_kv

method in GameAPI

- 描述

    获取可破坏物编号CURSOR_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CursorKey | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_cursor_key_kv(destructible_key, "key")
```

---

## get_tech_key_cursor_key_kv

method in GameAPI

- 描述

    获取科技编号CURSOR_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CursorKey | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_cursor_key_kv(tech_key, "key")
```

---

## get_icon_id_cursor_key_kv

method in GameAPI

- 描述

    获取图片CURSOR_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CursorKey | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_cursor_key_kv(1, "key")
```

---

## get_physics_entity_key_cursor_key_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型CURSOR_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CursorKey | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_cursor_key_kv(1, "key")
```

---

## get_unit_key_angle_kv

method in GameAPI

- 描述

    获取单位编号ANGLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_angle_kv(unit_key, "key")
```

---

## get_item_key_angle_kv

method in GameAPI

- 描述

    获取物品编号ANGLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_angle_kv(item_key, "key")
```

---

## get_ability_key_angle_kv

method in GameAPI

- 描述

    获取技能编号ANGLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_angle_kv(ability_key, "key")
```

---

## get_modifier_key_angle_kv

method in GameAPI

- 描述

    获取魔法效果特效编号ANGLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_angle_kv(modifier_key, "key")
```

---

## get_projectile_key_angle_kv

method in GameAPI

- 描述

    获取特效编号ANGLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_angle_kv(projectile_key, "key")
```

---

## get_destructible_key_angle_kv

method in GameAPI

- 描述

    获取可破坏物编号ANGLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_angle_kv(destructible_key, "key")
```

---

## get_tech_key_angle_kv

method in GameAPI

- 描述

    获取科技编号ANGLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_angle_kv(tech_key, "key")
```

---

## get_icon_id_angle_kv

method in GameAPI

- 描述

    获取图片ANGLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_angle_kv(1, "key")
```

---

## get_physics_entity_key_angle_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型ANGLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_angle_kv(1, "key")
```

---

## get_unit_key_texture_kv

method in GameAPI

- 描述

    获取单位编号TEXTURE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Texture | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_texture_kv(unit_key, "key")
```

---

## get_item_key_texture_kv

method in GameAPI

- 描述

    获取物品编号TEXTURE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Texture | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_texture_kv(item_key, "key")
```

---

## get_ability_key_texture_kv

method in GameAPI

- 描述

    获取技能编号TEXTURE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Texture | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_texture_kv(ability_key, "key")
```

---

## get_modifier_key_texture_kv

method in GameAPI

- 描述

    获取魔法效果特效编号TEXTURE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Texture | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_texture_kv(modifier_key, "key")
```

---

## get_projectile_key_texture_kv

method in GameAPI

- 描述

    获取特效编号TEXTURE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Texture | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_texture_kv(projectile_key, "key")
```

---

## get_destructible_key_texture_kv

method in GameAPI

- 描述

    获取可破坏物编号TEXTURE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Texture | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_texture_kv(destructible_key, "key")
```

---

## get_tech_key_texture_kv

method in GameAPI

- 描述

    获取科技编号TEXTURE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Texture | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_texture_kv(tech_key, "key")
```

---

## get_icon_id_texture_kv

method in GameAPI

- 描述

    获取图片TEXTURE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Texture | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_texture_kv(1, "key")
```

---

## get_physics_entity_key_texture_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型TEXTURE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Texture | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_texture_kv(1, "key")
```

---

## get_unit_key_sequence_kv

method in GameAPI

- 描述

    获取单位编号SEQUENCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sequence | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_sequence_kv(unit_key, "key")
```

---

## get_item_key_sequence_kv

method in GameAPI

- 描述

    获取物品编号SEQUENCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sequence | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_sequence_kv(item_key, "key")
```

---

## get_ability_key_sequence_kv

method in GameAPI

- 描述

    获取技能编号SEQUENCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sequence | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_sequence_kv(ability_key, "key")
```

---

## get_modifier_key_sequence_kv

method in GameAPI

- 描述

    获取魔法效果特效编号SEQUENCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sequence | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_sequence_kv(modifier_key, "key")
```

---

## get_projectile_key_sequence_kv

method in GameAPI

- 描述

    获取特效编号SEQUENCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sequence | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_sequence_kv(projectile_key, "key")
```

---

## get_destructible_key_sequence_kv

method in GameAPI

- 描述

    获取可破坏物编号SEQUENCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sequence | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_sequence_kv(destructible_key, "key")
```

---

## get_tech_key_sequence_kv

method in GameAPI

- 描述

    获取科技编号SEQUENCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sequence | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_sequence_kv(tech_key, "key")
```

---

## get_icon_id_sequence_kv

method in GameAPI

- 描述

    获取图片SEQUENCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sequence | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_sequence_kv(1, "key")
```

---

## get_physics_entity_key_sequence_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型SEQUENCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sequence | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_sequence_kv(1, "key")
```

---

## get_unit_key_physics_object_kv

method in GameAPI

- 描述

    获取单位编号PHYSICS_OBJECT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsObject | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_physics_object_kv(unit_key, "key")
```

---

## get_item_key_physics_object_kv

method in GameAPI

- 描述

    获取物品编号PHYSICS_OBJECT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsObject | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_physics_object_kv(item_key, "key")
```

---

## get_ability_key_physics_object_kv

method in GameAPI

- 描述

    获取技能编号PHYSICS_OBJECT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsObject | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_physics_object_kv(ability_key, "key")
```

---

## get_modifier_key_physics_object_kv

method in GameAPI

- 描述

    获取魔法效果特效编号PHYSICS_OBJECT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsObject | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_physics_object_kv(modifier_key, "key")
```

---

## get_projectile_key_physics_object_kv

method in GameAPI

- 描述

    获取特效编号PHYSICS_OBJECT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsObject | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_physics_object_kv(projectile_key, "key")
```

---

## get_destructible_key_physics_object_kv

method in GameAPI

- 描述

    获取可破坏物编号PHYSICS_OBJECT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsObject | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_physics_object_kv(destructible_key, "key")
```

---

## get_tech_key_physics_object_kv

method in GameAPI

- 描述

    获取科技编号PHYSICS_OBJECT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsObject | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_physics_object_kv(tech_key, "key")
```

---

## get_icon_id_physics_object_kv

method in GameAPI

- 描述

    获取图片PHYSICS_OBJECT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsObject | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_physics_object_kv(1, "key")
```

---

## get_physics_entity_key_physics_object_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型PHYSICS_OBJECT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsObject | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_physics_object_kv(1, "key")
```

---

## get_unit_key_physics_entity_kv

method in GameAPI

- 描述

    获取单位编号PHYSICS_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsEntity | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_physics_entity_kv(unit_key, "key")
```

---

## get_item_key_physics_entity_kv

method in GameAPI

- 描述

    获取物品编号PHYSICS_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsEntity | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_physics_entity_kv(item_key, "key")
```

---

## get_ability_key_physics_entity_kv

method in GameAPI

- 描述

    获取技能编号PHYSICS_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsEntity | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_physics_entity_kv(ability_key, "key")
```

---

## get_modifier_key_physics_entity_kv

method in GameAPI

- 描述

    获取魔法效果特效编号PHYSICS_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsEntity | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_physics_entity_kv(modifier_key, "key")
```

---

## get_projectile_key_physics_entity_kv

method in GameAPI

- 描述

    获取特效编号PHYSICS_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsEntity | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_physics_entity_kv(projectile_key, "key")
```

---

## get_destructible_key_physics_entity_kv

method in GameAPI

- 描述

    获取可破坏物编号PHYSICS_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsEntity | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_physics_entity_kv(destructible_key, "key")
```

---

## get_tech_key_physics_entity_kv

method in GameAPI

- 描述

    获取科技编号PHYSICS_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsEntity | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_physics_entity_kv(tech_key, "key")
```

---

## get_icon_id_physics_entity_kv

method in GameAPI

- 描述

    获取图片PHYSICS_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsEntity | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_physics_entity_kv(1, "key")
```

---

## get_physics_entity_key_physics_entity_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型PHYSICS_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsEntity | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_physics_entity_kv(1, "key")
```

---

## get_unit_key_physics_object_key_kv

method in GameAPI

- 描述

    获取单位编号PHYSICS_OBJECT_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsObjectKey | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_physics_object_key_kv(unit_key, "key")
```

---

## get_item_key_physics_object_key_kv

method in GameAPI

- 描述

    获取物品编号PHYSICS_OBJECT_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsObjectKey | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_physics_object_key_kv(item_key, "key")
```

---

## get_ability_key_physics_object_key_kv

method in GameAPI

- 描述

    获取技能编号PHYSICS_OBJECT_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsObjectKey | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_physics_object_key_kv(ability_key, "key")
```

---

## get_modifier_key_physics_object_key_kv

method in GameAPI

- 描述

    获取魔法效果特效编号PHYSICS_OBJECT_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsObjectKey | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_physics_object_key_kv(modifier_key, "key")
```

---

## get_projectile_key_physics_object_key_kv

method in GameAPI

- 描述

    获取特效编号PHYSICS_OBJECT_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsObjectKey | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_physics_object_key_kv(projectile_key, "key")
```

---

## get_destructible_key_physics_object_key_kv

method in GameAPI

- 描述

    获取可破坏物编号PHYSICS_OBJECT_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsObjectKey | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_physics_object_key_kv(destructible_key, "key")
```

---

## get_tech_key_physics_object_key_kv

method in GameAPI

- 描述

    获取科技编号PHYSICS_OBJECT_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsObjectKey | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_physics_object_key_kv(tech_key, "key")
```

---

## get_icon_id_physics_object_key_kv

method in GameAPI

- 描述

    获取图片PHYSICS_OBJECT_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsObjectKey | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_physics_object_key_kv(1, "key")
```

---

## get_physics_entity_key_physics_object_key_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型PHYSICS_OBJECT_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsObjectKey | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_physics_object_key_kv(1, "key")
```

---

## get_unit_key_physics_entity_key_kv

method in GameAPI

- 描述

    获取单位编号PHYSICS_ENTITY_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsEntityKey | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_physics_entity_key_kv(unit_key, "key")
```

---

## get_item_key_physics_entity_key_kv

method in GameAPI

- 描述

    获取物品编号PHYSICS_ENTITY_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsEntityKey | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_physics_entity_key_kv(item_key, "key")
```

---

## get_ability_key_physics_entity_key_kv

method in GameAPI

- 描述

    获取技能编号PHYSICS_ENTITY_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsEntityKey | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_physics_entity_key_kv(ability_key, "key")
```

---

## get_modifier_key_physics_entity_key_kv

method in GameAPI

- 描述

    获取魔法效果特效编号PHYSICS_ENTITY_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsEntityKey | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_physics_entity_key_kv(modifier_key, "key")
```

---

## get_projectile_key_physics_entity_key_kv

method in GameAPI

- 描述

    获取特效编号PHYSICS_ENTITY_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsEntityKey | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_physics_entity_key_kv(projectile_key, "key")
```

---

## get_destructible_key_physics_entity_key_kv

method in GameAPI

- 描述

    获取可破坏物编号PHYSICS_ENTITY_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsEntityKey | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_physics_entity_key_kv(destructible_key, "key")
```

---

## get_tech_key_physics_entity_key_kv

method in GameAPI

- 描述

    获取科技编号PHYSICS_ENTITY_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsEntityKey | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_physics_entity_key_kv(tech_key, "key")
```

---

## get_icon_id_physics_entity_key_kv

method in GameAPI

- 描述

    获取图片PHYSICS_ENTITY_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsEntityKey | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_physics_entity_key_kv(1, "key")
```

---

## get_physics_entity_key_physics_entity_key_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型PHYSICS_ENTITY_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsEntityKey | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_physics_entity_key_kv(1, "key")
```

---

## get_unit_key_rigid_body_kv

method in GameAPI

- 描述

    获取单位编号RIGID_BODY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RigidBody | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_rigid_body_kv(unit_key, "key")
```

---

## get_item_key_rigid_body_kv

method in GameAPI

- 描述

    获取物品编号RIGID_BODY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RigidBody | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_rigid_body_kv(item_key, "key")
```

---

## get_ability_key_rigid_body_kv

method in GameAPI

- 描述

    获取技能编号RIGID_BODY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RigidBody | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_rigid_body_kv(ability_key, "key")
```

---

## get_modifier_key_rigid_body_kv

method in GameAPI

- 描述

    获取魔法效果特效编号RIGID_BODY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RigidBody | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_rigid_body_kv(modifier_key, "key")
```

---

## get_projectile_key_rigid_body_kv

method in GameAPI

- 描述

    获取特效编号RIGID_BODY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RigidBody | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_rigid_body_kv(projectile_key, "key")
```

---

## get_destructible_key_rigid_body_kv

method in GameAPI

- 描述

    获取可破坏物编号RIGID_BODY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RigidBody | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_rigid_body_kv(destructible_key, "key")
```

---

## get_tech_key_rigid_body_kv

method in GameAPI

- 描述

    获取科技编号RIGID_BODY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RigidBody | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_rigid_body_kv(tech_key, "key")
```

---

## get_icon_id_rigid_body_kv

method in GameAPI

- 描述

    获取图片RIGID_BODY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RigidBody | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_rigid_body_kv(1, "key")
```

---

## get_physics_entity_key_rigid_body_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型RIGID_BODY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RigidBody | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_rigid_body_kv(1, "key")
```

---

## get_unit_key_rigid_body_group_kv

method in GameAPI

- 描述

    获取单位编号RIGID_BODY_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RigidBodyGroup | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_rigid_body_group_kv(unit_key, "key")
```

---

## get_item_key_rigid_body_group_kv

method in GameAPI

- 描述

    获取物品编号RIGID_BODY_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RigidBodyGroup | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_rigid_body_group_kv(item_key, "key")
```

---

## get_ability_key_rigid_body_group_kv

method in GameAPI

- 描述

    获取技能编号RIGID_BODY_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RigidBodyGroup | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_rigid_body_group_kv(ability_key, "key")
```

---

## get_modifier_key_rigid_body_group_kv

method in GameAPI

- 描述

    获取魔法效果特效编号RIGID_BODY_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RigidBodyGroup | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_rigid_body_group_kv(modifier_key, "key")
```

---

## get_projectile_key_rigid_body_group_kv

method in GameAPI

- 描述

    获取特效编号RIGID_BODY_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RigidBodyGroup | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_rigid_body_group_kv(projectile_key, "key")
```

---

## get_destructible_key_rigid_body_group_kv

method in GameAPI

- 描述

    获取可破坏物编号RIGID_BODY_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RigidBodyGroup | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_rigid_body_group_kv(destructible_key, "key")
```

---

## get_tech_key_rigid_body_group_kv

method in GameAPI

- 描述

    获取科技编号RIGID_BODY_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RigidBodyGroup | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_rigid_body_group_kv(tech_key, "key")
```

---

## get_icon_id_rigid_body_group_kv

method in GameAPI

- 描述

    获取图片RIGID_BODY_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RigidBodyGroup | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_rigid_body_group_kv(1, "key")
```

---

## get_physics_entity_key_rigid_body_group_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型RIGID_BODY_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RigidBodyGroup | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_rigid_body_group_kv(1, "key")
```

---

## get_unit_key_collider_kv

method in GameAPI

- 描述

    获取单位编号COLLIDER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Collider | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_collider_kv(unit_key, "key")
```

---

## get_item_key_collider_kv

method in GameAPI

- 描述

    获取物品编号COLLIDER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Collider | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_collider_kv(item_key, "key")
```

---

## get_ability_key_collider_kv

method in GameAPI

- 描述

    获取技能编号COLLIDER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Collider | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_collider_kv(ability_key, "key")
```

---

## get_modifier_key_collider_kv

method in GameAPI

- 描述

    获取魔法效果特效编号COLLIDER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Collider | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_collider_kv(modifier_key, "key")
```

---

## get_projectile_key_collider_kv

method in GameAPI

- 描述

    获取特效编号COLLIDER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Collider | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_collider_kv(projectile_key, "key")
```

---

## get_destructible_key_collider_kv

method in GameAPI

- 描述

    获取可破坏物编号COLLIDER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Collider | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_collider_kv(destructible_key, "key")
```

---

## get_tech_key_collider_kv

method in GameAPI

- 描述

    获取科技编号COLLIDER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Collider | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_collider_kv(tech_key, "key")
```

---

## get_icon_id_collider_kv

method in GameAPI

- 描述

    获取图片COLLIDER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Collider | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_collider_kv(1, "key")
```

---

## get_physics_entity_key_collider_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型COLLIDER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Collider | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_collider_kv(1, "key")
```

---

## get_unit_key_joint_kv

method in GameAPI

- 描述

    获取单位编号JOINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Joint | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_joint_kv(unit_key, "key")
```

---

## get_item_key_joint_kv

method in GameAPI

- 描述

    获取物品编号JOINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Joint | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_joint_kv(item_key, "key")
```

---

## get_ability_key_joint_kv

method in GameAPI

- 描述

    获取技能编号JOINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Joint | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_joint_kv(ability_key, "key")
```

---

## get_modifier_key_joint_kv

method in GameAPI

- 描述

    获取魔法效果特效编号JOINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Joint | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_joint_kv(modifier_key, "key")
```

---

## get_projectile_key_joint_kv

method in GameAPI

- 描述

    获取特效编号JOINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Joint | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_joint_kv(projectile_key, "key")
```

---

## get_destructible_key_joint_kv

method in GameAPI

- 描述

    获取可破坏物编号JOINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Joint | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_joint_kv(destructible_key, "key")
```

---

## get_tech_key_joint_kv

method in GameAPI

- 描述

    获取科技编号JOINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Joint | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_joint_kv(tech_key, "key")
```

---

## get_icon_id_joint_kv

method in GameAPI

- 描述

    获取图片JOINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Joint | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_joint_kv(1, "key")
```

---

## get_physics_entity_key_joint_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型JOINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Joint | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_joint_kv(1, "key")
```

---

## get_unit_key_reaction_kv

method in GameAPI

- 描述

    获取单位编号REACTION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Reaction | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_reaction_kv(unit_key, "key")
```

---

## get_item_key_reaction_kv

method in GameAPI

- 描述

    获取物品编号REACTION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Reaction | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_reaction_kv(item_key, "key")
```

---

## get_ability_key_reaction_kv

method in GameAPI

- 描述

    获取技能编号REACTION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Reaction | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_reaction_kv(ability_key, "key")
```

---

## get_modifier_key_reaction_kv

method in GameAPI

- 描述

    获取魔法效果特效编号REACTION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Reaction | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_reaction_kv(modifier_key, "key")
```

---

## get_projectile_key_reaction_kv

method in GameAPI

- 描述

    获取特效编号REACTION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Reaction | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_reaction_kv(projectile_key, "key")
```

---

## get_destructible_key_reaction_kv

method in GameAPI

- 描述

    获取可破坏物编号REACTION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Reaction | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_reaction_kv(destructible_key, "key")
```

---

## get_tech_key_reaction_kv

method in GameAPI

- 描述

    获取科技编号REACTION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Reaction | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_reaction_kv(tech_key, "key")
```

---

## get_icon_id_reaction_kv

method in GameAPI

- 描述

    获取图片REACTION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Reaction | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_reaction_kv(1, "key")
```

---

## get_physics_entity_key_reaction_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型REACTION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Reaction | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_reaction_kv(1, "key")
```

---

## get_unit_key_reaction_group_kv

method in GameAPI

- 描述

    获取单位编号REACTION_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ReactionGroup | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_reaction_group_kv(unit_key, "key")
```

---

## get_item_key_reaction_group_kv

method in GameAPI

- 描述

    获取物品编号REACTION_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ReactionGroup | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_reaction_group_kv(item_key, "key")
```

---

## get_ability_key_reaction_group_kv

method in GameAPI

- 描述

    获取技能编号REACTION_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ReactionGroup | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_reaction_group_kv(ability_key, "key")
```

---

## get_modifier_key_reaction_group_kv

method in GameAPI

- 描述

    获取魔法效果特效编号REACTION_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ReactionGroup | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_reaction_group_kv(modifier_key, "key")
```

---

## get_projectile_key_reaction_group_kv

method in GameAPI

- 描述

    获取特效编号REACTION_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ReactionGroup | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_reaction_group_kv(projectile_key, "key")
```

---

## get_destructible_key_reaction_group_kv

method in GameAPI

- 描述

    获取可破坏物编号REACTION_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ReactionGroup | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_reaction_group_kv(destructible_key, "key")
```

---

## get_tech_key_reaction_group_kv

method in GameAPI

- 描述

    获取科技编号REACTION_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ReactionGroup | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_reaction_group_kv(tech_key, "key")
```

---

## get_icon_id_reaction_group_kv

method in GameAPI

- 描述

    获取图片REACTION_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ReactionGroup | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_reaction_group_kv(1, "key")
```

---

## get_physics_entity_key_reaction_group_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型REACTION_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ReactionGroup | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_reaction_group_kv(1, "key")
```

---

## get_unit_key_dynamic_trigger_instance_kv

method in GameAPI

- 描述

    获取单位编号DYNAMIC_TRIGGER_INSTANCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DynamicTriggerInstance | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_dynamic_trigger_instance_kv(unit_key, "key")
```

---

## get_item_key_dynamic_trigger_instance_kv

method in GameAPI

- 描述

    获取物品编号DYNAMIC_TRIGGER_INSTANCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DynamicTriggerInstance | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_dynamic_trigger_instance_kv(item_key, "key")
```

---

## get_ability_key_dynamic_trigger_instance_kv

method in GameAPI

- 描述

    获取技能编号DYNAMIC_TRIGGER_INSTANCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DynamicTriggerInstance | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_dynamic_trigger_instance_kv(ability_key, "key")
```

---

## get_modifier_key_dynamic_trigger_instance_kv

method in GameAPI

- 描述

    获取魔法效果特效编号DYNAMIC_TRIGGER_INSTANCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DynamicTriggerInstance | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_dynamic_trigger_instance_kv(modifier_key, "key")
```

---

## get_projectile_key_dynamic_trigger_instance_kv

method in GameAPI

- 描述

    获取特效编号DYNAMIC_TRIGGER_INSTANCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DynamicTriggerInstance | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_dynamic_trigger_instance_kv(projectile_key, "key")
```

---

## get_destructible_key_dynamic_trigger_instance_kv

method in GameAPI

- 描述

    获取可破坏物编号DYNAMIC_TRIGGER_INSTANCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DynamicTriggerInstance | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_dynamic_trigger_instance_kv(destructible_key, "key")
```

---

## get_tech_key_dynamic_trigger_instance_kv

method in GameAPI

- 描述

    获取科技编号DYNAMIC_TRIGGER_INSTANCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DynamicTriggerInstance | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_dynamic_trigger_instance_kv(tech_key, "key")
```

---

## get_icon_id_dynamic_trigger_instance_kv

method in GameAPI

- 描述

    获取图片DYNAMIC_TRIGGER_INSTANCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DynamicTriggerInstance | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_dynamic_trigger_instance_kv(1, "key")
```

---

## get_physics_entity_key_dynamic_trigger_instance_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型DYNAMIC_TRIGGER_INSTANCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DynamicTriggerInstance | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_dynamic_trigger_instance_kv(1, "key")
```

---

## get_unit_key_table_kv

method in GameAPI

- 描述

    获取单位编号TABLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Table | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_table_kv(unit_key, "key")
```

---

## get_item_key_table_kv

method in GameAPI

- 描述

    获取物品编号TABLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Table | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_table_kv(item_key, "key")
```

---

## get_ability_key_table_kv

method in GameAPI

- 描述

    获取技能编号TABLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Table | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_table_kv(ability_key, "key")
```

---

## get_modifier_key_table_kv

method in GameAPI

- 描述

    获取魔法效果特效编号TABLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Table | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_table_kv(modifier_key, "key")
```

---

## get_projectile_key_table_kv

method in GameAPI

- 描述

    获取特效编号TABLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Table | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_table_kv(projectile_key, "key")
```

---

## get_destructible_key_table_kv

method in GameAPI

- 描述

    获取可破坏物编号TABLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Table | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_table_kv(destructible_key, "key")
```

---

## get_tech_key_table_kv

method in GameAPI

- 描述

    获取科技编号TABLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Table | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_table_kv(tech_key, "key")
```

---

## get_icon_id_table_kv

method in GameAPI

- 描述

    获取图片TABLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Table | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_table_kv(1, "key")
```

---

## get_physics_entity_key_table_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型TABLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Table | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_table_kv(1, "key")
```

---

## get_unit_key_random_pool_kv

method in GameAPI

- 描述

    获取单位编号RANDOM_POOL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RandomPool | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_random_pool_kv(unit_key, "key")
```

---

## get_item_key_random_pool_kv

method in GameAPI

- 描述

    获取物品编号RANDOM_POOL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RandomPool | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_random_pool_kv(item_key, "key")
```

---

## get_ability_key_random_pool_kv

method in GameAPI

- 描述

    获取技能编号RANDOM_POOL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RandomPool | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_random_pool_kv(ability_key, "key")
```

---

## get_modifier_key_random_pool_kv

method in GameAPI

- 描述

    获取魔法效果特效编号RANDOM_POOL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RandomPool | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_random_pool_kv(modifier_key, "key")
```

---

## get_projectile_key_random_pool_kv

method in GameAPI

- 描述

    获取特效编号RANDOM_POOL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RandomPool | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_random_pool_kv(projectile_key, "key")
```

---

## get_destructible_key_random_pool_kv

method in GameAPI

- 描述

    获取可破坏物编号RANDOM_POOL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RandomPool | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_random_pool_kv(destructible_key, "key")
```

---

## get_tech_key_random_pool_kv

method in GameAPI

- 描述

    获取科技编号RANDOM_POOL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RandomPool | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_random_pool_kv(tech_key, "key")
```

---

## get_icon_id_random_pool_kv

method in GameAPI

- 描述

    获取图片RANDOM_POOL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RandomPool | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_random_pool_kv(1, "key")
```

---

## get_physics_entity_key_random_pool_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型RANDOM_POOL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RandomPool | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_random_pool_kv(1, "key")
```

---

## get_unit_key_scene_ui_kv

method in GameAPI

- 描述

    获取单位编号SCENE_UI键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SceneNode | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_scene_ui_kv(unit_key, "key")
```

---

## get_item_key_scene_ui_kv

method in GameAPI

- 描述

    获取物品编号SCENE_UI键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SceneNode | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_scene_ui_kv(item_key, "key")
```

---

## get_ability_key_scene_ui_kv

method in GameAPI

- 描述

    获取技能编号SCENE_UI键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SceneNode | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_scene_ui_kv(ability_key, "key")
```

---

## get_modifier_key_scene_ui_kv

method in GameAPI

- 描述

    获取魔法效果特效编号SCENE_UI键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SceneNode | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_scene_ui_kv(modifier_key, "key")
```

---

## get_projectile_key_scene_ui_kv

method in GameAPI

- 描述

    获取特效编号SCENE_UI键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SceneNode | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_scene_ui_kv(projectile_key, "key")
```

---

## get_destructible_key_scene_ui_kv

method in GameAPI

- 描述

    获取可破坏物编号SCENE_UI键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SceneNode | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_scene_ui_kv(destructible_key, "key")
```

---

## get_tech_key_scene_ui_kv

method in GameAPI

- 描述

    获取科技编号SCENE_UI键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SceneNode | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_scene_ui_kv(tech_key, "key")
```

---

## get_icon_id_scene_ui_kv

method in GameAPI

- 描述

    获取图片SCENE_UI键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SceneNode | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_scene_ui_kv(1, "key")
```

---

## get_physics_entity_key_scene_ui_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型SCENE_UI键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SceneNode | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_scene_ui_kv(1, "key")
```

---

## get_unit_key_damage_type_kv

method in GameAPI

- 描述

    获取单位编号DAMAGE_TYPE键值对

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

local result = GameAPI.get_unit_key_damage_type_kv(unit_key, "key")
```

---

## get_item_key_damage_type_kv

method in GameAPI

- 描述

    获取物品编号DAMAGE_TYPE键值对

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

local result = GameAPI.get_item_key_damage_type_kv(item_key, "key")
```

---

## get_ability_key_damage_type_kv

method in GameAPI

- 描述

    获取技能编号DAMAGE_TYPE键值对

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

local result = GameAPI.get_ability_key_damage_type_kv(ability_key, "key")
```

---

## get_modifier_key_damage_type_kv

method in GameAPI

- 描述

    获取魔法效果特效编号DAMAGE_TYPE键值对

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

local result = GameAPI.get_modifier_key_damage_type_kv(modifier_key, "key")
```

---

## get_projectile_key_damage_type_kv

method in GameAPI

- 描述

    获取特效编号DAMAGE_TYPE键值对

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

local result = GameAPI.get_projectile_key_damage_type_kv(projectile_key, "key")
```

---

## get_destructible_key_damage_type_kv

method in GameAPI

- 描述

    获取可破坏物编号DAMAGE_TYPE键值对

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

local result = GameAPI.get_destructible_key_damage_type_kv(destructible_key, "key")
```

---

## get_tech_key_damage_type_kv

method in GameAPI

- 描述

    获取科技编号DAMAGE_TYPE键值对

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

local result = GameAPI.get_tech_key_damage_type_kv(tech_key, "key")
```

---

## get_icon_id_damage_type_kv

method in GameAPI

- 描述

    获取图片DAMAGE_TYPE键值对

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
local result = GameAPI.get_icon_id_damage_type_kv(1, "key")
```

---

## get_physics_entity_key_damage_type_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型DAMAGE_TYPE键值对

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
local result = GameAPI.get_physics_entity_key_damage_type_kv(1, "key")
```

---

## get_unit_key_harm_text_type_new_kv

method in GameAPI

- 描述

    获取单位编号HARM_TEXT_TYPE_NEW键值对

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

local result = GameAPI.get_unit_key_harm_text_type_new_kv(unit_key, "key")
```

---

## get_item_key_harm_text_type_new_kv

method in GameAPI

- 描述

    获取物品编号HARM_TEXT_TYPE_NEW键值对

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

local result = GameAPI.get_item_key_harm_text_type_new_kv(item_key, "key")
```

---

## get_ability_key_harm_text_type_new_kv

method in GameAPI

- 描述

    获取技能编号HARM_TEXT_TYPE_NEW键值对

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

local result = GameAPI.get_ability_key_harm_text_type_new_kv(ability_key, "key")
```

---

## get_modifier_key_harm_text_type_new_kv

method in GameAPI

- 描述

    获取魔法效果特效编号HARM_TEXT_TYPE_NEW键值对

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

local result = GameAPI.get_modifier_key_harm_text_type_new_kv(modifier_key, "key")
```

---

## get_projectile_key_harm_text_type_new_kv

method in GameAPI

- 描述

    获取特效编号HARM_TEXT_TYPE_NEW键值对

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

local result = GameAPI.get_projectile_key_harm_text_type_new_kv(projectile_key, "key")
```

---

## get_destructible_key_harm_text_type_new_kv

method in GameAPI

- 描述

    获取可破坏物编号HARM_TEXT_TYPE_NEW键值对

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

local result = GameAPI.get_destructible_key_harm_text_type_new_kv(destructible_key, "key")
```

---

## get_tech_key_harm_text_type_new_kv

method in GameAPI

- 描述

    获取科技编号HARM_TEXT_TYPE_NEW键值对

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

local result = GameAPI.get_tech_key_harm_text_type_new_kv(tech_key, "key")
```

---

## get_icon_id_harm_text_type_new_kv

method in GameAPI

- 描述

    获取图片HARM_TEXT_TYPE_NEW键值对

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
local result = GameAPI.get_icon_id_harm_text_type_new_kv(1, "key")
```

---

## get_physics_entity_key_harm_text_type_new_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型HARM_TEXT_TYPE_NEW键值对

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
local result = GameAPI.get_physics_entity_key_harm_text_type_new_kv(1, "key")
```

---

## get_unit_key_font_type_kv

method in GameAPI

- 描述

    获取单位编号FONT_TYPE键值对

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

local result = GameAPI.get_unit_key_font_type_kv(unit_key, "key")
```

---

## get_item_key_font_type_kv

method in GameAPI

- 描述

    获取物品编号FONT_TYPE键值对

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

local result = GameAPI.get_item_key_font_type_kv(item_key, "key")
```

---

## get_ability_key_font_type_kv

method in GameAPI

- 描述

    获取技能编号FONT_TYPE键值对

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

local result = GameAPI.get_ability_key_font_type_kv(ability_key, "key")
```

---

## get_modifier_key_font_type_kv

method in GameAPI

- 描述

    获取魔法效果特效编号FONT_TYPE键值对

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

local result = GameAPI.get_modifier_key_font_type_kv(modifier_key, "key")
```

---

## get_projectile_key_font_type_kv

method in GameAPI

- 描述

    获取特效编号FONT_TYPE键值对

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

local result = GameAPI.get_projectile_key_font_type_kv(projectile_key, "key")
```

---

## get_destructible_key_font_type_kv

method in GameAPI

- 描述

    获取可破坏物编号FONT_TYPE键值对

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

local result = GameAPI.get_destructible_key_font_type_kv(destructible_key, "key")
```

---

## get_tech_key_font_type_kv

method in GameAPI

- 描述

    获取科技编号FONT_TYPE键值对

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

local result = GameAPI.get_tech_key_font_type_kv(tech_key, "key")
```

---

## get_icon_id_font_type_kv

method in GameAPI

- 描述

    获取图片FONT_TYPE键值对

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
local result = GameAPI.get_icon_id_font_type_kv(1, "key")
```

---

## get_physics_entity_key_font_type_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型FONT_TYPE键值对

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
local result = GameAPI.get_physics_entity_key_font_type_kv(1, "key")
```

---

## get_unit_key_jump_word_track_kv

method in GameAPI

- 描述

    获取单位编号JUMP_WORD_TRACK键值对

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

local result = GameAPI.get_unit_key_jump_word_track_kv(unit_key, "key")
```

---

## get_item_key_jump_word_track_kv

method in GameAPI

- 描述

    获取物品编号JUMP_WORD_TRACK键值对

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

local result = GameAPI.get_item_key_jump_word_track_kv(item_key, "key")
```

---

## get_ability_key_jump_word_track_kv

method in GameAPI

- 描述

    获取技能编号JUMP_WORD_TRACK键值对

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

local result = GameAPI.get_ability_key_jump_word_track_kv(ability_key, "key")
```

---

## get_modifier_key_jump_word_track_kv

method in GameAPI

- 描述

    获取魔法效果特效编号JUMP_WORD_TRACK键值对

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

local result = GameAPI.get_modifier_key_jump_word_track_kv(modifier_key, "key")
```

---

## get_projectile_key_jump_word_track_kv

method in GameAPI

- 描述

    获取特效编号JUMP_WORD_TRACK键值对

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

local result = GameAPI.get_projectile_key_jump_word_track_kv(projectile_key, "key")
```

---

## get_destructible_key_jump_word_track_kv

method in GameAPI

- 描述

    获取可破坏物编号JUMP_WORD_TRACK键值对

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

local result = GameAPI.get_destructible_key_jump_word_track_kv(destructible_key, "key")
```

---

## get_tech_key_jump_word_track_kv

method in GameAPI

- 描述

    获取科技编号JUMP_WORD_TRACK键值对

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

local result = GameAPI.get_tech_key_jump_word_track_kv(tech_key, "key")
```

---

## get_icon_id_jump_word_track_kv

method in GameAPI

- 描述

    获取图片JUMP_WORD_TRACK键值对

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
local result = GameAPI.get_icon_id_jump_word_track_kv(1, "key")
```

---

## get_physics_entity_key_jump_word_track_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型JUMP_WORD_TRACK键值对

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
local result = GameAPI.get_physics_entity_key_jump_word_track_kv(1, "key")
```

---

## get_unit_key_new_timer_kv

method in GameAPI

- 描述

    获取单位编号NEW_TIMER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Timer | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_new_timer_kv(unit_key, "key")
```

---

## get_item_key_new_timer_kv

method in GameAPI

- 描述

    获取物品编号NEW_TIMER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Timer | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_new_timer_kv(item_key, "key")
```

---

## get_ability_key_new_timer_kv

method in GameAPI

- 描述

    获取技能编号NEW_TIMER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Timer | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_new_timer_kv(ability_key, "key")
```

---

## get_modifier_key_new_timer_kv

method in GameAPI

- 描述

    获取魔法效果特效编号NEW_TIMER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Timer | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_new_timer_kv(modifier_key, "key")
```

---

## get_projectile_key_new_timer_kv

method in GameAPI

- 描述

    获取特效编号NEW_TIMER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Timer | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_new_timer_kv(projectile_key, "key")
```

---

## get_destructible_key_new_timer_kv

method in GameAPI

- 描述

    获取可破坏物编号NEW_TIMER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Timer | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_new_timer_kv(destructible_key, "key")
```

---

## get_tech_key_new_timer_kv

method in GameAPI

- 描述

    获取科技编号NEW_TIMER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Timer | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_new_timer_kv(tech_key, "key")
```

---

## get_icon_id_new_timer_kv

method in GameAPI

- 描述

    获取图片NEW_TIMER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Timer | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_new_timer_kv(1, "key")
```

---

## get_physics_entity_key_new_timer_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型NEW_TIMER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Timer | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_new_timer_kv(1, "key")
```

---

## get_unit_key_tech_key_kv

method in GameAPI

- 描述

    获取单位编号TECH_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.TechKey | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_tech_key_kv(unit_key, "key")
```

---

## get_item_key_tech_key_kv

method in GameAPI

- 描述

    获取物品编号TECH_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.TechKey | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_tech_key_kv(item_key, "key")
```

---

## get_ability_key_tech_key_kv

method in GameAPI

- 描述

    获取技能编号TECH_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.TechKey | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_tech_key_kv(ability_key, "key")
```

---

## get_modifier_key_tech_key_kv

method in GameAPI

- 描述

    获取魔法效果特效编号TECH_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.TechKey | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_tech_key_kv(modifier_key, "key")
```

---

## get_projectile_key_tech_key_kv

method in GameAPI

- 描述

    获取特效编号TECH_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.TechKey | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_tech_key_kv(projectile_key, "key")
```

---

## get_destructible_key_tech_key_kv

method in GameAPI

- 描述

    获取可破坏物编号TECH_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.TechKey | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_tech_key_kv(destructible_key, "key")
```

---

## get_tech_key_tech_key_kv

method in GameAPI

- 描述

    获取科技编号TECH_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.TechKey | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_tech_key_kv(tech_key, "key")
```

---

## get_icon_id_tech_key_kv

method in GameAPI

- 描述

    获取图片TECH_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.TechKey | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_tech_key_kv(1, "key")
```

---

## get_physics_entity_key_tech_key_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型TECH_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.TechKey | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_tech_key_kv(1, "key")
```

---

## get_unit_key_store_key_kv

method in GameAPI

- 描述

    获取单位编号STORE_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.StoreKey | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_store_key_kv(unit_key, "key")
```

---

## get_item_key_store_key_kv

method in GameAPI

- 描述

    获取物品编号STORE_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.StoreKey | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_store_key_kv(item_key, "key")
```

---

## get_ability_key_store_key_kv

method in GameAPI

- 描述

    获取技能编号STORE_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.StoreKey | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_store_key_kv(ability_key, "key")
```

---

## get_modifier_key_store_key_kv

method in GameAPI

- 描述

    获取魔法效果特效编号STORE_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.StoreKey | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_store_key_kv(modifier_key, "key")
```

---

## get_projectile_key_store_key_kv

method in GameAPI

- 描述

    获取特效编号STORE_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.StoreKey | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_store_key_kv(projectile_key, "key")
```

---

## get_destructible_key_store_key_kv

method in GameAPI

- 描述

    获取可破坏物编号STORE_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.StoreKey | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_store_key_kv(destructible_key, "key")
```

---

## get_tech_key_store_key_kv

method in GameAPI

- 描述

    获取科技编号STORE_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.StoreKey | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_store_key_kv(tech_key, "key")
```

---

## get_icon_id_store_key_kv

method in GameAPI

- 描述

    获取图片STORE_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.StoreKey | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_store_key_kv(1, "key")
```

---

## get_physics_entity_key_store_key_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型STORE_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.StoreKey | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_store_key_kv(1, "key")
```

---

## get_unit_key_keyboard_key_kv

method in GameAPI

- 描述

    获取单位编号KEYBOARD_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.KeyboardKey | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_keyboard_key_kv(unit_key, "key")
```

---

## get_item_key_keyboard_key_kv

method in GameAPI

- 描述

    获取物品编号KEYBOARD_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.KeyboardKey | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_keyboard_key_kv(item_key, "key")
```

---

## get_ability_key_keyboard_key_kv

method in GameAPI

- 描述

    获取技能编号KEYBOARD_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.KeyboardKey | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_keyboard_key_kv(ability_key, "key")
```

---

## get_modifier_key_keyboard_key_kv

method in GameAPI

- 描述

    获取魔法效果特效编号KEYBOARD_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.KeyboardKey | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_keyboard_key_kv(modifier_key, "key")
```

---

## get_projectile_key_keyboard_key_kv

method in GameAPI

- 描述

    获取特效编号KEYBOARD_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.KeyboardKey | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_keyboard_key_kv(projectile_key, "key")
```

---

## get_destructible_key_keyboard_key_kv

method in GameAPI

- 描述

    获取可破坏物编号KEYBOARD_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.KeyboardKey | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_keyboard_key_kv(destructible_key, "key")
```

---

## get_tech_key_keyboard_key_kv

method in GameAPI

- 描述

    获取科技编号KEYBOARD_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.KeyboardKey | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_keyboard_key_kv(tech_key, "key")
```

---

## get_icon_id_keyboard_key_kv

method in GameAPI

- 描述

    获取图片KEYBOARD_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.KeyboardKey | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_keyboard_key_kv(1, "key")
```

---

## get_physics_entity_key_keyboard_key_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型KEYBOARD_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.KeyboardKey | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_keyboard_key_kv(1, "key")
```

---

## get_unit_key_func_keyboard_key_kv

method in GameAPI

- 描述

    获取单位编号FUNC_KEYBOARD_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FuncKeyboardKey | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_func_keyboard_key_kv(unit_key, "key")
```

---

## get_item_key_func_keyboard_key_kv

method in GameAPI

- 描述

    获取物品编号FUNC_KEYBOARD_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FuncKeyboardKey | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_func_keyboard_key_kv(item_key, "key")
```

---

## get_ability_key_func_keyboard_key_kv

method in GameAPI

- 描述

    获取技能编号FUNC_KEYBOARD_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FuncKeyboardKey | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_func_keyboard_key_kv(ability_key, "key")
```

---

## get_modifier_key_func_keyboard_key_kv

method in GameAPI

- 描述

    获取魔法效果特效编号FUNC_KEYBOARD_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FuncKeyboardKey | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_func_keyboard_key_kv(modifier_key, "key")
```

---

## get_projectile_key_func_keyboard_key_kv

method in GameAPI

- 描述

    获取特效编号FUNC_KEYBOARD_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FuncKeyboardKey | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_func_keyboard_key_kv(projectile_key, "key")
```

---

## get_destructible_key_func_keyboard_key_kv

method in GameAPI

- 描述

    获取可破坏物编号FUNC_KEYBOARD_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FuncKeyboardKey | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_func_keyboard_key_kv(destructible_key, "key")
```

---

## get_tech_key_func_keyboard_key_kv

method in GameAPI

- 描述

    获取科技编号FUNC_KEYBOARD_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FuncKeyboardKey | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_func_keyboard_key_kv(tech_key, "key")
```

---

## get_icon_id_func_keyboard_key_kv

method in GameAPI

- 描述

    获取图片FUNC_KEYBOARD_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FuncKeyboardKey | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_func_keyboard_key_kv(1, "key")
```

---

## get_physics_entity_key_func_keyboard_key_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型FUNC_KEYBOARD_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FuncKeyboardKey | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_func_keyboard_key_kv(1, "key")
```

---

## get_unit_key_mouse_key_kv

method in GameAPI

- 描述

    获取单位编号MOUSE_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MouseKey | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_mouse_key_kv(unit_key, "key")
```

---

## get_item_key_mouse_key_kv

method in GameAPI

- 描述

    获取物品编号MOUSE_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MouseKey | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_mouse_key_kv(item_key, "key")
```

---

## get_ability_key_mouse_key_kv

method in GameAPI

- 描述

    获取技能编号MOUSE_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MouseKey | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_mouse_key_kv(ability_key, "key")
```

---

## get_modifier_key_mouse_key_kv

method in GameAPI

- 描述

    获取魔法效果特效编号MOUSE_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MouseKey | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_mouse_key_kv(modifier_key, "key")
```

---

## get_projectile_key_mouse_key_kv

method in GameAPI

- 描述

    获取特效编号MOUSE_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MouseKey | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_mouse_key_kv(projectile_key, "key")
```

---

## get_destructible_key_mouse_key_kv

method in GameAPI

- 描述

    获取可破坏物编号MOUSE_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MouseKey | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_mouse_key_kv(destructible_key, "key")
```

---

## get_tech_key_mouse_key_kv

method in GameAPI

- 描述

    获取科技编号MOUSE_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MouseKey | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_mouse_key_kv(tech_key, "key")
```

---

## get_icon_id_mouse_key_kv

method in GameAPI

- 描述

    获取图片MOUSE_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MouseKey | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_mouse_key_kv(1, "key")
```

---

## get_physics_entity_key_mouse_key_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型MOUSE_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MouseKey | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_mouse_key_kv(1, "key")
```

---

## get_unit_key_mouse_wheel_kv

method in GameAPI

- 描述

    获取单位编号MOUSE_WHEEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MouseWheel | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_mouse_wheel_kv(unit_key, "key")
```

---

## get_item_key_mouse_wheel_kv

method in GameAPI

- 描述

    获取物品编号MOUSE_WHEEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MouseWheel | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_mouse_wheel_kv(item_key, "key")
```

---

## get_ability_key_mouse_wheel_kv

method in GameAPI

- 描述

    获取技能编号MOUSE_WHEEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MouseWheel | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_mouse_wheel_kv(ability_key, "key")
```

---

## get_modifier_key_mouse_wheel_kv

method in GameAPI

- 描述

    获取魔法效果特效编号MOUSE_WHEEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MouseWheel | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_mouse_wheel_kv(modifier_key, "key")
```

---

## get_projectile_key_mouse_wheel_kv

method in GameAPI

- 描述

    获取特效编号MOUSE_WHEEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MouseWheel | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_mouse_wheel_kv(projectile_key, "key")
```

---

## get_destructible_key_mouse_wheel_kv

method in GameAPI

- 描述

    获取可破坏物编号MOUSE_WHEEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MouseWheel | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_mouse_wheel_kv(destructible_key, "key")
```

---

## get_tech_key_mouse_wheel_kv

method in GameAPI

- 描述

    获取科技编号MOUSE_WHEEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MouseWheel | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_mouse_wheel_kv(tech_key, "key")
```

---

## get_icon_id_mouse_wheel_kv

method in GameAPI

- 描述

    获取图片MOUSE_WHEEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MouseWheel | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_mouse_wheel_kv(1, "key")
```

---

## get_physics_entity_key_mouse_wheel_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型MOUSE_WHEEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MouseWheel | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_mouse_wheel_kv(1, "key")
```

---

## get_unit_key_post_effect_kv

method in GameAPI

- 描述

    获取单位编号POST_EFFECT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PostEffect | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_post_effect_kv(unit_key, "key")
```

---

## get_item_key_post_effect_kv

method in GameAPI

- 描述

    获取物品编号POST_EFFECT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PostEffect | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_post_effect_kv(item_key, "key")
```

---

## get_ability_key_post_effect_kv

method in GameAPI

- 描述

    获取技能编号POST_EFFECT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PostEffect | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_post_effect_kv(ability_key, "key")
```

---

## get_modifier_key_post_effect_kv

method in GameAPI

- 描述

    获取魔法效果特效编号POST_EFFECT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PostEffect | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_post_effect_kv(modifier_key, "key")
```

---

## get_projectile_key_post_effect_kv

method in GameAPI

- 描述

    获取特效编号POST_EFFECT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PostEffect | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_post_effect_kv(projectile_key, "key")
```

---

## get_destructible_key_post_effect_kv

method in GameAPI

- 描述

    获取可破坏物编号POST_EFFECT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PostEffect | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_post_effect_kv(destructible_key, "key")
```

---

## get_tech_key_post_effect_kv

method in GameAPI

- 描述

    获取科技编号POST_EFFECT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PostEffect | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_post_effect_kv(tech_key, "key")
```

---

## get_icon_id_post_effect_kv

method in GameAPI

- 描述

    获取图片POST_EFFECT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PostEffect | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_post_effect_kv(1, "key")
```

---

## get_physics_entity_key_post_effect_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型POST_EFFECT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PostEffect | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_post_effect_kv(1, "key")
```

---

## get_unit_key_unit_type_kv

method in GameAPI

- 描述

    获取单位编号UNIT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitType | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_unit_type_kv(unit_key, "key")
```

---

## get_item_key_unit_type_kv

method in GameAPI

- 描述

    获取物品编号UNIT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitType | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_unit_type_kv(item_key, "key")
```

---

## get_ability_key_unit_type_kv

method in GameAPI

- 描述

    获取技能编号UNIT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitType | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_unit_type_kv(ability_key, "key")
```

---

## get_modifier_key_unit_type_kv

method in GameAPI

- 描述

    获取魔法效果特效编号UNIT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitType | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_unit_type_kv(modifier_key, "key")
```

---

## get_projectile_key_unit_type_kv

method in GameAPI

- 描述

    获取特效编号UNIT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitType | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_unit_type_kv(projectile_key, "key")
```

---

## get_destructible_key_unit_type_kv

method in GameAPI

- 描述

    获取可破坏物编号UNIT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitType | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_unit_type_kv(destructible_key, "key")
```

---

## get_tech_key_unit_type_kv

method in GameAPI

- 描述

    获取科技编号UNIT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitType | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_unit_type_kv(tech_key, "key")
```

---

## get_icon_id_unit_type_kv

method in GameAPI

- 描述

    获取图片UNIT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitType | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_unit_type_kv(1, "key")
```

---

## get_physics_entity_key_unit_type_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型UNIT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitType | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_unit_type_kv(1, "key")
```

---

## get_unit_key_unit_command_type_kv

method in GameAPI

- 描述

    获取单位编号UNIT_COMMAND_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommandType | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_unit_command_type_kv(unit_key, "key")
```

---

## get_item_key_unit_command_type_kv

method in GameAPI

- 描述

    获取物品编号UNIT_COMMAND_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommandType | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_unit_command_type_kv(item_key, "key")
```

---

## get_ability_key_unit_command_type_kv

method in GameAPI

- 描述

    获取技能编号UNIT_COMMAND_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommandType | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_unit_command_type_kv(ability_key, "key")
```

---

## get_modifier_key_unit_command_type_kv

method in GameAPI

- 描述

    获取魔法效果特效编号UNIT_COMMAND_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommandType | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_unit_command_type_kv(modifier_key, "key")
```

---

## get_projectile_key_unit_command_type_kv

method in GameAPI

- 描述

    获取特效编号UNIT_COMMAND_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommandType | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_unit_command_type_kv(projectile_key, "key")
```

---

## get_destructible_key_unit_command_type_kv

method in GameAPI

- 描述

    获取可破坏物编号UNIT_COMMAND_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommandType | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_unit_command_type_kv(destructible_key, "key")
```

---

## get_tech_key_unit_command_type_kv

method in GameAPI

- 描述

    获取科技编号UNIT_COMMAND_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommandType | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_unit_command_type_kv(tech_key, "key")
```

---

## get_icon_id_unit_command_type_kv

method in GameAPI

- 描述

    获取图片UNIT_COMMAND_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommandType | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_unit_command_type_kv(1, "key")
```

---

## get_physics_entity_key_unit_command_type_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型UNIT_COMMAND_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommandType | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_unit_command_type_kv(1, "key")
```

---

## get_unit_key_mini_map_color_type_kv

method in GameAPI

- 描述

    获取单位编号MINI_MAP_COLOR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MiniMapColorType | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_mini_map_color_type_kv(unit_key, "key")
```

---

## get_item_key_mini_map_color_type_kv

method in GameAPI

- 描述

    获取物品编号MINI_MAP_COLOR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MiniMapColorType | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_mini_map_color_type_kv(item_key, "key")
```

---

## get_ability_key_mini_map_color_type_kv

method in GameAPI

- 描述

    获取技能编号MINI_MAP_COLOR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MiniMapColorType | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_mini_map_color_type_kv(ability_key, "key")
```

---

## get_modifier_key_mini_map_color_type_kv

method in GameAPI

- 描述

    获取魔法效果特效编号MINI_MAP_COLOR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MiniMapColorType | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_mini_map_color_type_kv(modifier_key, "key")
```

---

## get_projectile_key_mini_map_color_type_kv

method in GameAPI

- 描述

    获取特效编号MINI_MAP_COLOR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MiniMapColorType | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_mini_map_color_type_kv(projectile_key, "key")
```

---

## get_destructible_key_mini_map_color_type_kv

method in GameAPI

- 描述

    获取可破坏物编号MINI_MAP_COLOR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MiniMapColorType | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_mini_map_color_type_kv(destructible_key, "key")
```

---

## get_tech_key_mini_map_color_type_kv

method in GameAPI

- 描述

    获取科技编号MINI_MAP_COLOR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MiniMapColorType | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_mini_map_color_type_kv(tech_key, "key")
```

---

## get_icon_id_mini_map_color_type_kv

method in GameAPI

- 描述

    获取图片MINI_MAP_COLOR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MiniMapColorType | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_mini_map_color_type_kv(1, "key")
```

---

## get_physics_entity_key_mini_map_color_type_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型MINI_MAP_COLOR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MiniMapColorType | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_mini_map_color_type_kv(1, "key")
```

---

## get_unit_key_unit_behavior_kv

method in GameAPI

- 描述

    获取单位编号UNIT_BEHAVIOR键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitBehavior | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_unit_behavior_kv(unit_key, "key")
```

---

## get_item_key_unit_behavior_kv

method in GameAPI

- 描述

    获取物品编号UNIT_BEHAVIOR键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitBehavior | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_unit_behavior_kv(item_key, "key")
```

---

## get_ability_key_unit_behavior_kv

method in GameAPI

- 描述

    获取技能编号UNIT_BEHAVIOR键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitBehavior | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_unit_behavior_kv(ability_key, "key")
```

---

## get_modifier_key_unit_behavior_kv

method in GameAPI

- 描述

    获取魔法效果特效编号UNIT_BEHAVIOR键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitBehavior | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_unit_behavior_kv(modifier_key, "key")
```

---

## get_projectile_key_unit_behavior_kv

method in GameAPI

- 描述

    获取特效编号UNIT_BEHAVIOR键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitBehavior | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_unit_behavior_kv(projectile_key, "key")
```

---

## get_destructible_key_unit_behavior_kv

method in GameAPI

- 描述

    获取可破坏物编号UNIT_BEHAVIOR键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitBehavior | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_unit_behavior_kv(destructible_key, "key")
```

---

## get_tech_key_unit_behavior_kv

method in GameAPI

- 描述

    获取科技编号UNIT_BEHAVIOR键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitBehavior | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_unit_behavior_kv(tech_key, "key")
```

---

## get_icon_id_unit_behavior_kv

method in GameAPI

- 描述

    获取图片UNIT_BEHAVIOR键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitBehavior | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_unit_behavior_kv(1, "key")
```

---

## get_physics_entity_key_unit_behavior_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型UNIT_BEHAVIOR键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitBehavior | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_unit_behavior_kv(1, "key")
```

---

## get_unit_key_curved_path_kv

method in GameAPI

- 描述

    获取单位编号CURVED_PATH键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CurvedPath | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_curved_path_kv(unit_key, "key")
```

---

## get_item_key_curved_path_kv

method in GameAPI

- 描述

    获取物品编号CURVED_PATH键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CurvedPath | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_curved_path_kv(item_key, "key")
```

---

## get_ability_key_curved_path_kv

method in GameAPI

- 描述

    获取技能编号CURVED_PATH键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CurvedPath | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_curved_path_kv(ability_key, "key")
```

---

## get_modifier_key_curved_path_kv

method in GameAPI

- 描述

    获取魔法效果特效编号CURVED_PATH键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CurvedPath | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_curved_path_kv(modifier_key, "key")
```

---

## get_projectile_key_curved_path_kv

method in GameAPI

- 描述

    获取特效编号CURVED_PATH键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CurvedPath | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_curved_path_kv(projectile_key, "key")
```

---

## get_destructible_key_curved_path_kv

method in GameAPI

- 描述

    获取可破坏物编号CURVED_PATH键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CurvedPath | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_curved_path_kv(destructible_key, "key")
```

---

## get_tech_key_curved_path_kv

method in GameAPI

- 描述

    获取科技编号CURVED_PATH键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CurvedPath | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_curved_path_kv(tech_key, "key")
```

---

## get_icon_id_curved_path_kv

method in GameAPI

- 描述

    获取图片CURVED_PATH键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CurvedPath | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_curved_path_kv(1, "key")
```

---

## get_physics_entity_key_curved_path_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型CURVED_PATH键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CurvedPath | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_curved_path_kv(1, "key")
```

---

## get_unit_key_curved_path_3d_kv

method in GameAPI

- 描述

    获取单位编号CURVED_PATH_3D键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CurvedPath3D | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_curved_path_3d_kv(unit_key, "key")
```

---

## get_item_key_curved_path_3d_kv

method in GameAPI

- 描述

    获取物品编号CURVED_PATH_3D键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CurvedPath3D | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_curved_path_3d_kv(item_key, "key")
```

---

## get_ability_key_curved_path_3d_kv

method in GameAPI

- 描述

    获取技能编号CURVED_PATH_3D键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CurvedPath3D | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_curved_path_3d_kv(ability_key, "key")
```

---

## get_modifier_key_curved_path_3d_kv

method in GameAPI

- 描述

    获取魔法效果特效编号CURVED_PATH_3D键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CurvedPath3D | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_curved_path_3d_kv(modifier_key, "key")
```

---

## get_projectile_key_curved_path_3d_kv

method in GameAPI

- 描述

    获取特效编号CURVED_PATH_3D键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CurvedPath3D | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_curved_path_3d_kv(projectile_key, "key")
```

---

## get_destructible_key_curved_path_3d_kv

method in GameAPI

- 描述

    获取可破坏物编号CURVED_PATH_3D键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CurvedPath3D | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_curved_path_3d_kv(destructible_key, "key")
```

---

## get_tech_key_curved_path_3d_kv

method in GameAPI

- 描述

    获取科技编号CURVED_PATH_3D键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CurvedPath3D | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_curved_path_3d_kv(tech_key, "key")
```

---

## get_icon_id_curved_path_3d_kv

method in GameAPI

- 描述

    获取图片CURVED_PATH_3D键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CurvedPath3D | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_curved_path_3d_kv(1, "key")
```

---

## get_physics_entity_key_curved_path_3d_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型CURVED_PATH_3D键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CurvedPath3D | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_curved_path_3d_kv(1, "key")
```

---

## set_coin_currency_list_value

method in GameAPI

- 描述

    设置COIN_CURRENCY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.COIN_CURRENCY | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local coin_currency = "RMB"

GameAPI.set_coin_currency_list_value(list, 1, coin_currency)
```

---

## get_coin_currency_n_list

method in GameAPI

- 描述

    生成n个值为v的COIN_CURRENCY数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.COIN_CURRENCY | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local coin_currency = "RMB"

local result = GameAPI.get_coin_currency_n_list(1)
```

---

## get_map_list_value

method in GameAPI

- 描述

    获取MAP数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Map | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_map_list_value(list, 1)
```

---

## set_map_list_value

method in GameAPI

- 描述

    设置MAP数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.Map | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_map_list_value(list, 1, 1)
```

---

## get_map_n_list

method in GameAPI

- 描述

    生成n个值为v的MAP数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.Map | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_map_n_list(1, 1)
```

---

## get_ui_equip_slot_use_type_list_value

method in GameAPI

- 描述

    获取UI_EQUIP_SLOT_USE_TYPE数组中某项

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

local result = GameAPI.get_ui_equip_slot_use_type_list_value(list, 1)
```

---

## set_ui_equip_slot_use_type_list_value

method in GameAPI

- 描述

    设置UI_EQUIP_SLOT_USE_TYPE数组中某项

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

GameAPI.set_ui_equip_slot_use_type_list_value(list, 1, 1)
```

---

## get_ui_equip_slot_use_type_n_list

method in GameAPI

- 描述

    生成n个值为v的UI_EQUIP_SLOT_USE_TYPE数组

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
local result = GameAPI.get_ui_equip_slot_use_type_n_list(1, 1)
```

---

## get_ui_equip_slot_drag_type_list_value

method in GameAPI

- 描述

    获取UI_EQUIP_SLOT_DRAG_TYPE数组中某项

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

local result = GameAPI.get_ui_equip_slot_drag_type_list_value(list, 1)
```

---

## set_ui_equip_slot_drag_type_list_value

method in GameAPI

- 描述

    设置UI_EQUIP_SLOT_DRAG_TYPE数组中某项

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

GameAPI.set_ui_equip_slot_drag_type_list_value(list, 1, 1)
```

---

## get_ui_equip_slot_drag_type_n_list

method in GameAPI

- 描述

    生成n个值为v的UI_EQUIP_SLOT_DRAG_TYPE数组

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
local result = GameAPI.get_ui_equip_slot_drag_type_n_list(1, 1)
```

---

## get_live2d_list_value

method in GameAPI

- 描述

    获取LIVE2D数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Live2dKey | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_live2d_list_value(list, 1)
```

---

## set_live2d_list_value

method in GameAPI

- 描述

    设置LIVE2D数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.Live2dKey | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_live2d_list_value(list, 1, 1)
```

---

## get_live2d_n_list

method in GameAPI

- 描述

    生成n个值为v的LIVE2D数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.Live2dKey | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_live2d_n_list(1, 1)
```

---

## get_ui_text_over_length_handling_type_list_value

method in GameAPI

- 描述

    获取UI_TEXT_OVER_LENGTH_HANDLING_TYPE数组中某项

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

local result = GameAPI.get_ui_text_over_length_handling_type_list_value(list, 1)
```

---

## set_ui_text_over_length_handling_type_list_value

method in GameAPI

- 描述

    设置UI_TEXT_OVER_LENGTH_HANDLING_TYPE数组中某项

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

GameAPI.set_ui_text_over_length_handling_type_list_value(list, 1, 1)
```

---

## get_ui_text_over_length_handling_type_n_list

method in GameAPI

- 描述

    生成n个值为v的UI_TEXT_OVER_LENGTH_HANDLING_TYPE数组

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
local result = GameAPI.get_ui_text_over_length_handling_type_n_list(1, 1)
```

---

## get_ui_layout_clipping_type_list_value

method in GameAPI

- 描述

    获取UI_LAYOUT_CLIPPING_TYPE数组中某项

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

local result = GameAPI.get_ui_layout_clipping_type_list_value(list, 1)
```

---

## set_ui_layout_clipping_type_list_value

method in GameAPI

- 描述

    设置UI_LAYOUT_CLIPPING_TYPE数组中某项

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

GameAPI.set_ui_layout_clipping_type_list_value(list, 1, 1)
```

---

## get_ui_layout_clipping_type_n_list

method in GameAPI

- 描述

    生成n个值为v的UI_LAYOUT_CLIPPING_TYPE数组

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
local result = GameAPI.get_ui_layout_clipping_type_n_list(1, 1)
```

---

## get_ui_gridview_type_list_value

method in GameAPI

- 描述

    获取UI_GRIDVIEW_TYPE数组中某项

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

local result = GameAPI.get_ui_gridview_type_list_value(list, 1)
```

---

## set_ui_gridview_type_list_value

method in GameAPI

- 描述

    设置UI_GRIDVIEW_TYPE数组中某项

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

GameAPI.set_ui_gridview_type_list_value(list, 1, 1)
```

---

## get_ui_gridview_type_n_list

method in GameAPI

- 描述

    生成n个值为v的UI_GRIDVIEW_TYPE数组

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
local result = GameAPI.get_ui_gridview_type_n_list(1, 1)
```

---

## get_ui_gridview_bar_type_list_value

method in GameAPI

- 描述

    获取UI_GRIDVIEW_BAR_TYPE数组中某项

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

local result = GameAPI.get_ui_gridview_bar_type_list_value(list, 1)
```

---

## set_ui_gridview_bar_type_list_value

method in GameAPI

- 描述

    设置UI_GRIDVIEW_BAR_TYPE数组中某项

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

GameAPI.set_ui_gridview_bar_type_list_value(list, 1, 1)
```

---

## get_ui_gridview_bar_type_n_list

method in GameAPI

- 描述

    生成n个值为v的UI_GRIDVIEW_BAR_TYPE数组

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
local result = GameAPI.get_ui_gridview_bar_type_n_list(1, 1)
```

---

## get_ui_effect_camera_mode_list_value

method in GameAPI

- 描述

    获取UI_EFFECT_CAMERA_MODE数组中某项

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

local result = GameAPI.get_ui_effect_camera_mode_list_value(list, 1)
```

---

## set_ui_effect_camera_mode_list_value

method in GameAPI

- 描述

    设置UI_EFFECT_CAMERA_MODE数组中某项

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

GameAPI.set_ui_effect_camera_mode_list_value(list, 1, 1)
```

---

## get_ui_effect_camera_mode_n_list

method in GameAPI

- 描述

    生成n个值为v的UI_EFFECT_CAMERA_MODE数组

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
local result = GameAPI.get_ui_effect_camera_mode_n_list(1, 1)
```

---

## get_ui_pos_adapt_mode_list_value

method in GameAPI

- 描述

    获取UI_POS_ADAPT_MODE数组中某项

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

local result = GameAPI.get_ui_pos_adapt_mode_list_value(list, 1)
```

---

## set_ui_pos_adapt_mode_list_value

method in GameAPI

- 描述

    设置UI_POS_ADAPT_MODE数组中某项

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

GameAPI.set_ui_pos_adapt_mode_list_value(list, 1, 1)
```

---

## get_ui_pos_adapt_mode_n_list

method in GameAPI

- 描述

    生成n个值为v的UI_POS_ADAPT_MODE数组

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
local result = GameAPI.get_ui_pos_adapt_mode_n_list(1, 1)
```

---

## get_goods_key_list_value

method in GameAPI

- 描述

    获取GOODS_KEY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.GoodsKey | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_goods_key_list_value(list, 1)
```

---

## set_goods_key_list_value

method in GameAPI

- 描述

    设置GOODS_KEY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.GoodsKey | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_goods_key_list_value(list, 1, 1)
```

---

## get_goods_key_n_list

method in GameAPI

- 描述

    生成n个值为v的GOODS_KEY数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.GoodsKey | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_goods_key_n_list(1, 1)
```

---

## get_ui_chat_send_channel_list_value

method in GameAPI

- 描述

    获取UI_CHAT_SEND_CHANNEL数组中某项

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

local result = GameAPI.get_ui_chat_send_channel_list_value(list, 1)
```

---

## set_ui_chat_send_channel_list_value

method in GameAPI

- 描述

    设置UI_CHAT_SEND_CHANNEL数组中某项

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

GameAPI.set_ui_chat_send_channel_list_value(list, 1, 1)
```

---

## get_ui_chat_send_channel_n_list

method in GameAPI

- 描述

    生成n个值为v的UI_CHAT_SEND_CHANNEL数组

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
local result = GameAPI.get_ui_chat_send_channel_n_list(1, 1)
```

---

## get_ui_chat_recv_channel_list_value

method in GameAPI

- 描述

    获取UI_CHAT_RECV_CHANNEL数组中某项

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

local result = GameAPI.get_ui_chat_recv_channel_list_value(list, 1)
```

---

## set_ui_chat_recv_channel_list_value

method in GameAPI

- 描述

    设置UI_CHAT_RECV_CHANNEL数组中某项

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

GameAPI.set_ui_chat_recv_channel_list_value(list, 1, 1)
```

---

## get_ui_chat_recv_channel_n_list

method in GameAPI

- 描述

    生成n个值为v的UI_CHAT_RECV_CHANNEL数组

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
local result = GameAPI.get_ui_chat_recv_channel_n_list(1, 1)
```

---

## get_attach_model_entity_list_value

method in GameAPI

- 描述

    获取ATTACH_MODEL_ENTITY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AttachModelEntity | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_attach_model_entity_list_value(list, 1)
```

---

## set_attach_model_entity_list_value

method in GameAPI

- 描述

    设置ATTACH_MODEL_ENTITY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.AttachModelEntity | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local attach_model = GameAPI.get_unit_key_attach_model_entity_kv(1, "key")

GameAPI.set_attach_model_entity_list_value(list, 1, attach_model)
```

---

## get_attach_model_entity_n_list

method in GameAPI

- 描述

    生成n个值为v的ATTACH_MODEL_ENTITY数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.AttachModelEntity | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local attach_model = GameAPI.get_unit_key_attach_model_entity_kv(1, "key")

local result = GameAPI.get_attach_model_entity_n_list(1)
```

---

## set_unit_key_ui_gridview_type_kv

method in GameAPI

- 描述

    预设库 添加UI_GRIDVIEW_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_ui_gridview_type_kv(1, 1, "value")
```

---

## set_unit_key_ui_gridview_bar_type_kv

method in GameAPI

- 描述

    预设库 添加UI_GRIDVIEW_BAR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_ui_gridview_bar_type_kv(1, 1, "value")
```

---

## set_unit_key_ui_effect_camera_mode_kv

method in GameAPI

- 描述

    预设库 添加UI_EFFECT_CAMERA_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_ui_effect_camera_mode_kv(1, 1, "value")
```

---

## set_unit_key_ui_equip_slot_use_type_kv

method in GameAPI

- 描述

    预设库 添加UI_EQUIP_SLOT_USE_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_ui_equip_slot_use_type_kv(1, 1, "value")
```

---

## set_unit_key_ui_equip_slot_drag_type_kv

method in GameAPI

- 描述

    预设库 添加UI_EQUIP_SLOT_DRAG_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_ui_equip_slot_drag_type_kv(1, 1, "value")
```

---

## set_unit_key_ui_layout_clipping_type_kv

method in GameAPI

- 描述

    预设库 添加UI_LAYOUT_CLIPPING_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_ui_layout_clipping_type_kv(1, 1, "value")
```

---

## set_unit_key_ui_text_over_length_handling_type_kv

method in GameAPI

- 描述

    预设库 添加UI_TEXT_OVER_LENGTH_HANDLING_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_ui_text_over_length_handling_type_kv(1, 1, "value")
```

---

## set_unit_key_ui_pos_adapt_mode_kv

method in GameAPI

- 描述

    预设库 添加UI_POS_ADAPT_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_ui_pos_adapt_mode_kv(1, 1, "value")
```

---

## set_unit_key_ui_chat_send_channel_kv

method in GameAPI

- 描述

    预设库 添加UI_CHAT_SEND_CHANNEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_ui_chat_send_channel_kv(1, 1, "value")
```

---

## set_unit_key_ui_chat_recv_channel_kv

method in GameAPI

- 描述

    预设库 添加UI_CHAT_RECV_CHANNEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_ui_chat_recv_channel_kv(1, 1, "value")
```

---

## set_unit_key_ui_anim_play_mode_kv

method in GameAPI

- 描述

    预设库 添加UI_ANIM_PLAY_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_ui_anim_play_mode_kv(1, 1, "value")
```

---

## set_unit_key_ui_text_font_name_kv

method in GameAPI

- 描述

    预设库 添加UI_TEXT_FONT_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_ui_text_font_name_kv(1, 1, "value")
```

---

## set_unit_key_ui_eca_anim_type_kv

method in GameAPI

- 描述

    预设库 添加UI_ECA_ANIM_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_ui_eca_anim_type_kv(1, 1, "value")
```

---

## set_unit_key_local_unit_group_kv

method in GameAPI

- 描述

    预设库 添加LOCAL_UNIT_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_local_unit_group_kv(1, 1, "value")
```

---

## set_unit_key_damage_attack_type_kv

method in GameAPI

- 描述

    预设库 添加DAMAGE_ATTACK_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_damage_attack_type_kv(1, 1, "value")
```

---

## set_unit_key_damage_armor_type_kv

method in GameAPI

- 描述

    预设库 添加DAMAGE_ARMOR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_damage_armor_type_kv(1, 1, "value")
```

---

## set_unit_key_item_stack_type_kv

method in GameAPI

- 描述

    预设库 添加ITEM_STACK_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_item_stack_type_kv(1, 1, "value")
```

---

## set_unit_key_ability_release_id_kv

method in GameAPI

- 描述

    预设库 添加ABILITY_RELEASE_ID键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_ability_release_id_kv(1, 1, "value")
```

---

## set_unit_key_slot_type_kv

method in GameAPI

- 描述

    预设库 添加SLOT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_slot_type_kv(1, 1, "value")
```

---

## set_unit_key_ui_point_kv

method in GameAPI

- 描述

    预设库 添加UI_POINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_ui_point_kv(1, 1, "value")
```

---

## set_unit_key_attach_model_entity_kv

method in GameAPI

- 描述

    预设库 添加ATTACH_MODEL_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_attach_model_entity_kv(1, 1, "value")
```

---

## set_unit_key_live2d_kv

method in GameAPI

- 描述

    预设库 添加LIVE2D键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_live2d_kv(1, 1, "value")
```

---

## set_unit_key_spine_kv

method in GameAPI

- 描述

    预设库 添加SPINE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_spine_kv(1, 1, "value")
```

---

## set_unit_key_force_entity_kv

method in GameAPI

- 描述

    预设库 添加FORCE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_force_entity_kv(1, 1, "value")
```

---

## set_unit_key_goods_key_kv

method in GameAPI

- 描述

    预设库 添加GOODS_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_goods_key_kv(1, 1, "value")
```

---

## set_unit_key_mouse_key_without_middle_kv

method in GameAPI

- 描述

    预设库 添加MOUSE_KEY_WITHOUT_MIDDLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_mouse_key_without_middle_kv(1, 1, "value")
```

---

## set_unit_key_map_kv

method in GameAPI

- 描述

    预设库 添加MAP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_map_kv(1, 1, "value")
```

---

## set_unit_key_unit_group_command_type_kv

method in GameAPI

- 描述

    预设库 添加UNIT_GROUP_COMMAND_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_unit_group_command_type_kv(1, 1, "value")
```

---

## set_unit_key_rescue_seeker_type_kv

method in GameAPI

- 描述

    预设库 添加RESCUE_SEEKER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_rescue_seeker_type_kv(1, 1, "value")
```

---

## set_unit_key_rescuer_type_kv

method in GameAPI

- 描述

    预设库 添加RESCUER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_rescuer_type_kv(1, 1, "value")
```

---

## set_unit_key_store_item_type_kv

method in GameAPI

- 描述

    预设库 添加STORE_ITEM_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_store_item_type_kv(1, 1, "value")
```

---

## set_unit_key_site_state_kv

method in GameAPI

- 描述

    预设库 添加SITE_STATE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_site_state_kv(1, 1, "value")
```

---

## set_unit_key_coin_currency_kv

method in GameAPI

- 描述

    预设库 添加COIN_CURRENCY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_unit_key_coin_currency_kv(1, 1, "value")
```

---

## set_item_key_ui_gridview_type_kv

method in GameAPI

- 描述

    预设库 添加UI_GRIDVIEW_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_ui_gridview_type_kv(1, 1, "value")
```

---

## set_item_key_ui_gridview_bar_type_kv

method in GameAPI

- 描述

    预设库 添加UI_GRIDVIEW_BAR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_ui_gridview_bar_type_kv(1, 1, "value")
```

---

## set_item_key_ui_effect_camera_mode_kv

method in GameAPI

- 描述

    预设库 添加UI_EFFECT_CAMERA_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_ui_effect_camera_mode_kv(1, 1, "value")
```

---

## set_item_key_ui_equip_slot_use_type_kv

method in GameAPI

- 描述

    预设库 添加UI_EQUIP_SLOT_USE_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_ui_equip_slot_use_type_kv(1, 1, "value")
```

---

## set_item_key_ui_equip_slot_drag_type_kv

method in GameAPI

- 描述

    预设库 添加UI_EQUIP_SLOT_DRAG_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_ui_equip_slot_drag_type_kv(1, 1, "value")
```

---

## set_item_key_ui_layout_clipping_type_kv

method in GameAPI

- 描述

    预设库 添加UI_LAYOUT_CLIPPING_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_ui_layout_clipping_type_kv(1, 1, "value")
```

---

## set_item_key_ui_text_over_length_handling_type_kv

method in GameAPI

- 描述

    预设库 添加UI_TEXT_OVER_LENGTH_HANDLING_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_ui_text_over_length_handling_type_kv(1, 1, "value")
```

---

## set_item_key_ui_pos_adapt_mode_kv

method in GameAPI

- 描述

    预设库 添加UI_POS_ADAPT_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_ui_pos_adapt_mode_kv(1, 1, "value")
```

---

## set_item_key_ui_chat_send_channel_kv

method in GameAPI

- 描述

    预设库 添加UI_CHAT_SEND_CHANNEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_ui_chat_send_channel_kv(1, 1, "value")
```

---

## set_item_key_ui_chat_recv_channel_kv

method in GameAPI

- 描述

    预设库 添加UI_CHAT_RECV_CHANNEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_ui_chat_recv_channel_kv(1, 1, "value")
```

---

## set_item_key_ui_anim_play_mode_kv

method in GameAPI

- 描述

    预设库 添加UI_ANIM_PLAY_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_ui_anim_play_mode_kv(1, 1, "value")
```

---

## set_item_key_ui_text_font_name_kv

method in GameAPI

- 描述

    预设库 添加UI_TEXT_FONT_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_ui_text_font_name_kv(1, 1, "value")
```

---

## set_item_key_ui_eca_anim_type_kv

method in GameAPI

- 描述

    预设库 添加UI_ECA_ANIM_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_ui_eca_anim_type_kv(1, 1, "value")
```

---

## set_item_key_local_unit_group_kv

method in GameAPI

- 描述

    预设库 添加LOCAL_UNIT_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_local_unit_group_kv(1, 1, "value")
```

---

## set_item_key_damage_attack_type_kv

method in GameAPI

- 描述

    预设库 添加DAMAGE_ATTACK_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_damage_attack_type_kv(1, 1, "value")
```

---

## set_item_key_damage_armor_type_kv

method in GameAPI

- 描述

    预设库 添加DAMAGE_ARMOR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_damage_armor_type_kv(1, 1, "value")
```

---

## set_item_key_item_stack_type_kv

method in GameAPI

- 描述

    预设库 添加ITEM_STACK_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_item_stack_type_kv(1, 1, "value")
```

---

## set_item_key_ability_release_id_kv

method in GameAPI

- 描述

    预设库 添加ABILITY_RELEASE_ID键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_ability_release_id_kv(1, 1, "value")
```

---

## set_item_key_slot_type_kv

method in GameAPI

- 描述

    预设库 添加SLOT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_slot_type_kv(1, 1, "value")
```

---

## set_item_key_ui_point_kv

method in GameAPI

- 描述

    预设库 添加UI_POINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_ui_point_kv(1, 1, "value")
```

---

## set_item_key_attach_model_entity_kv

method in GameAPI

- 描述

    预设库 添加ATTACH_MODEL_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_attach_model_entity_kv(1, 1, "value")
```

---

## set_item_key_live2d_kv

method in GameAPI

- 描述

    预设库 添加LIVE2D键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_live2d_kv(1, 1, "value")
```

---

## set_item_key_spine_kv

method in GameAPI

- 描述

    预设库 添加SPINE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_spine_kv(1, 1, "value")
```

---

## set_item_key_force_entity_kv

method in GameAPI

- 描述

    预设库 添加FORCE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_force_entity_kv(1, 1, "value")
```

---

## set_item_key_goods_key_kv

method in GameAPI

- 描述

    预设库 添加GOODS_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_goods_key_kv(1, 1, "value")
```

---

## set_item_key_mouse_key_without_middle_kv

method in GameAPI

- 描述

    预设库 添加MOUSE_KEY_WITHOUT_MIDDLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_mouse_key_without_middle_kv(1, 1, "value")
```

---

## set_item_key_map_kv

method in GameAPI

- 描述

    预设库 添加MAP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_map_kv(1, 1, "value")
```

---

## set_item_key_unit_group_command_type_kv

method in GameAPI

- 描述

    预设库 添加UNIT_GROUP_COMMAND_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_unit_group_command_type_kv(1, 1, "value")
```

---

## set_item_key_rescue_seeker_type_kv

method in GameAPI

- 描述

    预设库 添加RESCUE_SEEKER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_rescue_seeker_type_kv(1, 1, "value")
```

---

## set_item_key_rescuer_type_kv

method in GameAPI

- 描述

    预设库 添加RESCUER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_rescuer_type_kv(1, 1, "value")
```

---

## set_item_key_store_item_type_kv

method in GameAPI

- 描述

    预设库 添加STORE_ITEM_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_store_item_type_kv(1, 1, "value")
```

---

## set_item_key_site_state_kv

method in GameAPI

- 描述

    预设库 添加SITE_STATE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_site_state_kv(1, 1, "value")
```

---

## set_item_key_coin_currency_kv

method in GameAPI

- 描述

    预设库 添加COIN_CURRENCY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_key_coin_currency_kv(1, 1, "value")
```

---

## set_ability_key_ui_gridview_type_kv

method in GameAPI

- 描述

    预设库 添加UI_GRIDVIEW_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_ui_gridview_type_kv(1, 1, "value")
```

---

## set_ability_key_ui_gridview_bar_type_kv

method in GameAPI

- 描述

    预设库 添加UI_GRIDVIEW_BAR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_ui_gridview_bar_type_kv(1, 1, "value")
```

---

## set_ability_key_ui_effect_camera_mode_kv

method in GameAPI

- 描述

    预设库 添加UI_EFFECT_CAMERA_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_ui_effect_camera_mode_kv(1, 1, "value")
```

---

## set_ability_key_ui_equip_slot_use_type_kv

method in GameAPI

- 描述

    预设库 添加UI_EQUIP_SLOT_USE_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_ui_equip_slot_use_type_kv(1, 1, "value")
```

---

## set_ability_key_ui_equip_slot_drag_type_kv

method in GameAPI

- 描述

    预设库 添加UI_EQUIP_SLOT_DRAG_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_ui_equip_slot_drag_type_kv(1, 1, "value")
```

---

## set_ability_key_ui_layout_clipping_type_kv

method in GameAPI

- 描述

    预设库 添加UI_LAYOUT_CLIPPING_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_ui_layout_clipping_type_kv(1, 1, "value")
```

---

## set_ability_key_ui_text_over_length_handling_type_kv

method in GameAPI

- 描述

    预设库 添加UI_TEXT_OVER_LENGTH_HANDLING_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_ui_text_over_length_handling_type_kv(1, 1, "value")
```

---

## set_ability_key_ui_pos_adapt_mode_kv

method in GameAPI

- 描述

    预设库 添加UI_POS_ADAPT_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_ui_pos_adapt_mode_kv(1, 1, "value")
```

---

## set_ability_key_ui_chat_send_channel_kv

method in GameAPI

- 描述

    预设库 添加UI_CHAT_SEND_CHANNEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_ui_chat_send_channel_kv(1, 1, "value")
```

---

## set_ability_key_ui_chat_recv_channel_kv

method in GameAPI

- 描述

    预设库 添加UI_CHAT_RECV_CHANNEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_ui_chat_recv_channel_kv(1, 1, "value")
```

---

## set_ability_key_ui_anim_play_mode_kv

method in GameAPI

- 描述

    预设库 添加UI_ANIM_PLAY_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_ui_anim_play_mode_kv(1, 1, "value")
```

---

## set_ability_key_ui_text_font_name_kv

method in GameAPI

- 描述

    预设库 添加UI_TEXT_FONT_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_ui_text_font_name_kv(1, 1, "value")
```

---

## set_ability_key_ui_eca_anim_type_kv

method in GameAPI

- 描述

    预设库 添加UI_ECA_ANIM_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_ui_eca_anim_type_kv(1, 1, "value")
```

---

## set_ability_key_local_unit_group_kv

method in GameAPI

- 描述

    预设库 添加LOCAL_UNIT_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_local_unit_group_kv(1, 1, "value")
```

---

## set_ability_key_damage_attack_type_kv

method in GameAPI

- 描述

    预设库 添加DAMAGE_ATTACK_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_damage_attack_type_kv(1, 1, "value")
```

---

## set_ability_key_damage_armor_type_kv

method in GameAPI

- 描述

    预设库 添加DAMAGE_ARMOR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_damage_armor_type_kv(1, 1, "value")
```

---

## set_ability_key_item_stack_type_kv

method in GameAPI

- 描述

    预设库 添加ITEM_STACK_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_item_stack_type_kv(1, 1, "value")
```

---

## set_ability_key_ability_release_id_kv

method in GameAPI

- 描述

    预设库 添加ABILITY_RELEASE_ID键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_ability_release_id_kv(1, 1, "value")
```

---

## set_ability_key_slot_type_kv

method in GameAPI

- 描述

    预设库 添加SLOT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_slot_type_kv(1, 1, "value")
```

---

## set_ability_key_ui_point_kv

method in GameAPI

- 描述

    预设库 添加UI_POINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_ui_point_kv(1, 1, "value")
```

---

## set_ability_key_attach_model_entity_kv

method in GameAPI

- 描述

    预设库 添加ATTACH_MODEL_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_attach_model_entity_kv(1, 1, "value")
```

---

## set_ability_key_live2d_kv

method in GameAPI

- 描述

    预设库 添加LIVE2D键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_live2d_kv(1, 1, "value")
```

---

## set_ability_key_spine_kv

method in GameAPI

- 描述

    预设库 添加SPINE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_spine_kv(1, 1, "value")
```

---

## set_ability_key_force_entity_kv

method in GameAPI

- 描述

    预设库 添加FORCE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_force_entity_kv(1, 1, "value")
```

---

## set_ability_key_goods_key_kv

method in GameAPI

- 描述

    预设库 添加GOODS_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_goods_key_kv(1, 1, "value")
```

---

## set_ability_key_mouse_key_without_middle_kv

method in GameAPI

- 描述

    预设库 添加MOUSE_KEY_WITHOUT_MIDDLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_mouse_key_without_middle_kv(1, 1, "value")
```

---

## set_ability_key_map_kv

method in GameAPI

- 描述

    预设库 添加MAP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_map_kv(1, 1, "value")
```

---

## set_ability_key_unit_group_command_type_kv

method in GameAPI

- 描述

    预设库 添加UNIT_GROUP_COMMAND_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_unit_group_command_type_kv(1, 1, "value")
```

---

## set_ability_key_rescue_seeker_type_kv

method in GameAPI

- 描述

    预设库 添加RESCUE_SEEKER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_rescue_seeker_type_kv(1, 1, "value")
```

---

## set_ability_key_rescuer_type_kv

method in GameAPI

- 描述

    预设库 添加RESCUER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_rescuer_type_kv(1, 1, "value")
```

---

## set_ability_key_store_item_type_kv

method in GameAPI

- 描述

    预设库 添加STORE_ITEM_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_store_item_type_kv(1, 1, "value")
```

---

## set_ability_key_site_state_kv

method in GameAPI

- 描述

    预设库 添加SITE_STATE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_site_state_kv(1, 1, "value")
```

---

## set_ability_key_coin_currency_kv

method in GameAPI

- 描述

    预设库 添加COIN_CURRENCY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | integer | prefab库ID |
    | key | integer | 编号 |
    | value | string | 键值名称 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ability_key_coin_currency_kv(1, 1, "value")
```

---

## set_attach_model_fresnel

method in GameAPI

- 描述

    遍历魔法效果的挂接模型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_entity | py.ModifierEntity | 魔法效果 |
    | model_key | py.ModelKey | 模型类型 |
    | color | string | 颜色 |
    | exp | number | 指数 |
    | strength | number | 强度 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)
local model_key = 1

GameAPI.set_attach_model_fresnel(modifier.handle, model_key, "color", 1.0, 1.0)
```

---

## api_get_item_group_length

method in GameAPI

- 描述

    获取物品组的数量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_group | py.ItemGroup | 物品组 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 物品组数量 |

- 示例

```lua
local item_group = y3.item_group.create()

local result = GameAPI.api_get_item_group_length(item_group.handle)
```

---

## api_get_item_type_id

method in GameAPI

- 描述

    获取物品类型编号

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemKey | 物品编号 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.api_get_item_type_id(item_key)
```

---

## api_get_item_stack_type_id

method in GameAPI

- 描述

    获取物品类型的堆叠类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemStackType | 物品编号 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.api_get_item_stack_type_id(item_key)
```

---

## api_get_item_group_intersection

method in GameAPI

- 描述

    物品组取交集

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | group1 | py.ItemGroup | 物品组1 |
    | group2 | py.ItemGroup | 物品组2 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemGroup | 物品组 |

- 示例

```lua
local item_group = y3.item_group.create()

local result = GameAPI.api_get_item_group_intersection(item_group.handle, item_group.handle)
```

---

## api_get_item_group_diff

method in GameAPI

- 描述

    物品组取差集

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | group1 | py.ItemGroup | 物品组1 |
    | group2 | py.ItemGroup | 物品组2 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemGroup | 物品组 |

- 示例

```lua
local item_group = y3.item_group.create()

local result = GameAPI.api_get_item_group_diff(item_group.handle, item_group.handle)
```

---

## api_switch_unit_item_slot_by_slot_id

method in GameAPI

- 描述

    根据槽位交换物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | slot_type_1 | py.SlotType | 物品槽位类型 |
    | slot_id_1 | integer | 槽位ID |
    | slot_type_2 | py.SlotType | 物品槽位类型 |
    | slot_id_2 | integer | 槽位ID |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local slot_type = y3.const.SlotType.BAR

GameAPI.api_switch_unit_item_slot_by_slot_id(unit.handle, slot_type, 1, slot_type, 1)
```

---

## api_switch_item_slot

method in GameAPI

- 描述

    交换物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item1 | py.Item | 物品 |
    | item2 | py.Item | 物品 |

- 返回值

    无

- 示例

```lua
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

GameAPI.api_switch_item_slot(item.handle, item.handle)
```

---

## set_item_name_permanent_show_config

method in GameAPI

- 描述

    设置游戏内物品名称是否常驻显示

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | permanent_show | boolean | 是否常驻显示 |

- 返回值

    无

- 示例

```lua
GameAPI.set_item_name_permanent_show_config(true)
```

---

## set_touch_type_of_picking_up_item_by_item_name

method in GameAPI

- 描述

    设置物品姓名版点击拾取的操作方式

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | pickup_touch_type | integer | 操作type |

- 返回值

    无

- 示例

```lua
GameAPI.set_touch_type_of_picking_up_item_by_item_name(1)
```

---

## api_get_store_item_type

method in GameAPI

- 描述

    获取平台道具类别

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | store_key | py.StoreKey | 平台道具编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.StoreItemType | 平台道具类型 |

- 示例

```lua
local store_key = 134274569

local result = GameAPI.api_get_store_item_type(store_key)
```

---

## screenshot_func_for_lua

method in GameAPI

- 描述

    在Lua中调用截图功能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | path | string | LocalData下的相对路径 |
    | file_name | string | 文件名 |
    | width? | integer | 图片宽 |
    | height? | integer | 图片高 |

- 返回值

    无

- 示例

```lua
GameAPI.screenshot_func_for_lua("path", "file_name", 1, 1)
```

---

## disable_all_eca_triggers

method in GameAPI

- 描述

    禁用所有的ECA全局触发器

- 参数

    无

- 返回值

    无

- 示例

```lua
GameAPI.disable_all_eca_triggers()
```

---

## mover_miss_target

method in GameAPI

- 描述

    运动器丢失追踪目标

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

GameAPI.mover_miss_target(mover)
```

---

## get_projectile_mover

method in GameAPI

- 描述

    获得投射物的运动器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile | py.ProjectileEntity | 投掷物对象 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Mover | 运动器 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local target_point = unit:get_point()
local projectile = y3.projectile.create({ key = 134274569, target = target_point })

local result = GameAPI.get_projectile_mover(projectile.handle)
```

---

## get_mover_relate_projectile

method in GameAPI

- 描述

    获取运动器关联投射物

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | mover_id | py.Mover | 运动器 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileEntity | 关联投射物 |

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })
local mover = GameAPI.get_projectile_mover(projectile.handle)

local result = GameAPI.get_mover_relate_projectile(mover)
```

---

## create_unit_command_customized_move_to_pos

method in GameAPI

- 描述

    定制移动

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | pos | py.FVector3 | 位置 |
    | take_static_collision | boolean | 考虑非地形静态阻挡 |
    | take_dynamic_collision | boolean | 考虑动态阻挡 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommand | 单位命令 |

- 示例

```lua
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

local result = GameAPI.create_unit_command_customized_move_to_pos(fvector3, true, true)
```

---

## create_unit_command_move_to_pos_3D

method in GameAPI

- 描述

    移动至三维坐标

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

local result = GameAPI.create_unit_command_move_to_pos_3D(fvector3, Fix32(1))
```

---

## create_unit_command_hold_3D

method in GameAPI

- 描述

    驻守至三维坐标

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

local result = GameAPI.create_unit_command_hold_3D(fvector3)
```

---

## create_unit_command_attack_point

method in GameAPI

- 描述

    攻击目标点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.Point | 释放点 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommand | 单位命令 |

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)

local result = GameAPI.create_unit_command_attack_point(point)
```

---

## create_unit_command_patrol

method in GameAPI

- 描述

    巡逻

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | pos | py.Unit | 目标点 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommand | 单位命令 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = GameAPI.create_unit_command_patrol(unit.handle)
```

---

## api_release_group_command

method in GameAPI

- 描述

    发布命令

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | group | py.UnitGroup | 单位组 |
    | command | py.UnitCommand | 命令 |

- 返回值

    无

- 示例

```lua
local unit_group = y3.unit_group.create()
local unit = y3.player.get_by_id(1):get_all_units()[1]
local unit_command = unit.handle:api_release_command_stop()

GameAPI.api_release_group_command(unit_group.handle, unit_command)
```

---

## create_unit_group_command_move_to_pos

method in GameAPI

- 描述

    移动

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | pos | py.FVector3 | 位置 |
    | nav_range? | py.Fixed | 寻路范围 |
    | organization? | boolean | 是否编队 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommand | 单位命令 |

- 示例

```lua
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

local result = GameAPI.create_unit_group_command_move_to_pos(fvector3, Fix32(1), true)
```

---

## create_unit_group_command_stop

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
local result = GameAPI.create_unit_group_command_stop()
```

---

## create_unit_group_command_empty

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
local result = GameAPI.create_unit_group_command_empty()
```

---

## create_unit_group_command_hold

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

local result = GameAPI.create_unit_group_command_hold(fvector3)
```

---

## create_unit_group_command_attack_move

method in GameAPI

- 描述

    攻击移动

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | pos | py.FVector3 | 位置 |
    | nav_range? | py.Fixed | 寻路范围 |
    | organization? | boolean | 是否编队 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommand | 单位命令 |

- 示例

```lua
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

local result = GameAPI.create_unit_group_command_attack_move(fvector3, Fix32(1), true)
```

---

## create_unit_group_command_attack_target

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

local result = GameAPI.create_unit_group_command_attack_target(actor, Fix32(1))
```

---

## create_unit_group_command_move_along_road

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

local result = GameAPI.create_unit_group_command_move_along_road(road.handle, 1, true, true, true)
```

---

## create_unit_group_command_follow

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

local result = GameAPI.create_unit_group_command_follow(unit.handle, Fix32(1), Fix32(1), Fix32(1), Fix32(1), true)
```

---

## create_unit_group_command_move_to_random_pos

method in GameAPI

- 描述

    移动到随机位置

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.Area | 区域 |
    | r? | py.Fixed | 寻路范围 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommand | 单位命令 |

- 示例

```lua
local area = y3.area.create_circle_area(y3.point.create(0, 0, 0), 500)

local result = GameAPI.create_unit_group_command_move_to_random_pos(area.handle, Fix32(1))
```

---

## create_unit_group_command_attack_move_random_pos

method in GameAPI

- 描述

    攻击移动到随机位置

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.Area | 区域 |
    | r? | py.Fixed | 寻路范围 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommand | 单位命令 |

- 示例

```lua
local area = y3.area.create_circle_area(y3.point.create(0, 0, 0), 500)

local result = GameAPI.create_unit_group_command_attack_move_random_pos(area.handle, Fix32(1))
```

---

## create_unit_group_command_attack_point

method in GameAPI

- 描述

    攻击目标点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.Point | 释放点 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommand | 单位命令 |

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)

local result = GameAPI.create_unit_group_command_attack_point(point)
```

---

## create_unit_group_command_patrol

method in GameAPI

- 描述

    巡逻

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.Point | 目标点 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommand | 单位命令 |

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)

local result = GameAPI.create_unit_group_command_patrol(point)
```

---

## set_player_sfx_switch_by_tag

method in GameAPI

- 描述

    特效播放开关

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | tag | integer | 特效标签 |
    | switch | boolean | 开关 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_player_sfx_switch_by_tag(player.handle, 1, true)
```

---

## create_link_sfx_from_unit_to_point1

method in GameAPI

- 描述

    创建单位到点闪电特效

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | sfx_res_id | py.SfxKey | 特效编号 |
    | source_unit | py.Unit | 起点单位 |
    | source_socket | string | 起点单位挂接点名称 |
    | target_point | py.FVector3 | 终点 |
    | target_height | py.Fixed | 终点高度 |
    | duration? | number | 持续时间 |
    | immediately? | boolean | 是否立即删除 |
    | use_sys_d_destroy_way? | boolean | 特效删除的方式是否读表 |
    | show_in_fog? | boolean | 迷雾中显示 |
    | blend_with_fog? | boolean | 迷雾混合 |
    | follow_change_position? | boolean | 跟随模型缩放改变位置 |
    | follow_change_size? | boolean | 跟随模型缩放改变尺寸 |
    | speed? | number | 播放速度 |
    | x_scale? | number | x轴缩放 |
    | y_scale? | number | y轴缩放 |
    | z_scale? | number | z轴缩放 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LinkSfx | 特效 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local sfx_key = 134274569
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

local result = GameAPI.create_link_sfx_from_unit_to_point1(sfx_key, unit.handle, "source_socket", fvector3, Fix32(1), 1.0, true, true, true, true, true, true, 1.0, 1.0, 1.0, 1.0)
```

---

## create_link_sfx_from_unit_to_unit1

method in GameAPI

- 描述

    创建单位到单位闪电特效

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | sfx_res_id | py.SfxKey | 特效编号 |
    | source_unit | py.Unit | 起点单位 |
    | source_socket | string | 起点单位挂接点名称 |
    | target_unit | py.Unit | 终点单位 |
    | target_socket | string | 起点单位挂接点名称 |
    | duration? | number | 持续时间 |
    | immediately? | boolean | 是否立即删除 |
    | use_sys_d_destroy_way? | boolean | 特效删除的方式是否读表 |
    | show_in_fog? | boolean | 迷雾中显示 |
    | blend_with_fog? | boolean | 迷雾混合 |
    | follow_change_position? | boolean | 跟随模型缩放改变位置 |
    | follow_change_size? | boolean | 跟随模型缩放改变尺寸 |
    | speed? | number | 播放速度 |
    | x_scale? | number | x轴缩放 |
    | y_scale? | number | y轴缩放 |
    | z_scale? | number | z轴缩放 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LinkSfx | 特效 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local sfx_key = 134274569

local result = GameAPI.create_link_sfx_from_unit_to_unit1(sfx_key, unit.handle, "source_socket", unit.handle, "target_socket", 1.0, true, true, true, true, true, true, 1.0, 1.0, 1.0, 1.0)
```

---

## create_link_sfx_from_point_to_unit1

method in GameAPI

- 描述

    创建点到单位闪电特效

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | sfx_res_id | py.SfxKey | 特效编号 |
    | source_point | py.FVector3 | 起点 |
    | source_height | py.Fixed | 起点高度 |
    | source_unit | py.Unit | 终点单位 |
    | source_socket | string | 起点单位挂接点名称 |
    | duration? | number | 持续时间 |
    | immediately? | boolean | 是否立即删除 |
    | use_sys_d_destroy_way? | boolean | 特效删除的方式是否读表 |
    | show_in_fog? | boolean | 迷雾中显示 |
    | blend_with_fog? | boolean | 迷雾混合 |
    | speed? | number | 播放速度 |
    | x_scale? | number | x轴缩放 |
    | y_scale? | number | y轴缩放 |
    | z_scale? | number | z轴缩放 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LinkSfx | 特效 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local sfx_key = 134274569
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

local result = GameAPI.create_link_sfx_from_point_to_unit1(sfx_key, fvector3, Fix32(1), unit.handle, "source_socket", 1.0, true, true, true, true, 1.0, 1.0, 1.0, 1.0)
```

---

## create_link_sfx_from_point_to_point1

method in GameAPI

- 描述

    创建点到点闪电特效

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | sfx_res_id | py.SfxKey | 特效编号 |
    | source_point | py.FVector3 | 起点 |
    | source_height | py.Fixed | 起点高度 |
    | target_point | py.FVector3 | 终点 |
    | target_height | py.Fixed | 终点高度 |
    | duration? | number | 持续时间 |
    | immediately? | boolean | 是否立即删除 |
    | use_sys_d_destroy_way? | boolean | 特效删除的方式是否读表 |
    | show_in_fog? | boolean | 迷雾中显示 |
    | blend_with_fog? | boolean | 迷雾混合 |
    | speed? | number | 播放速度 |
    | x_scale? | number | x轴缩放 |
    | y_scale? | number | y轴缩放 |
    | z_scale? | number | z轴缩放 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LinkSfx | 特效 |

- 示例

```lua
local sfx_key = 134274569
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

local result = GameAPI.create_link_sfx_from_point_to_point1(sfx_key, fvector3, Fix32(1), fvector3, Fix32(1), 1.0, true, true, true, true, 1.0, 1.0, 1.0, 1.0)
```

---

## create_sfx_on_point_new

method in GameAPI

- 描述

    创建特效到点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | sfx_id | py.SfxKey | 特效编号 |
    | point | py.Point | 点 |
    | face_angle | number | 面向角度 |
    | speed | number | 播放速度 |
    | height | number | 高度 |
    | duration | number | 持续时间 |
    | immediately? | boolean | 是否立即删除 |
    | use_sys_d_destroy_way? | boolean | 特效删除的方式是否读表 |
    | show_in_fog? | boolean | 迷雾里显示 |
    | blend_with_fog? | boolean | 迷雾混合 |
    | scale_x? | number | x轴缩放 |
    | scale_y? | number | y轴缩放 |
    | scale_z? | number | z轴缩放 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sfx | 特效 |

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)
local sfx_key = 134274569

local result = GameAPI.create_sfx_on_point_new(sfx_key, point, 1.0, 1.0, 1.0, 1.0, true, true, true, true, 1.0, 1.0, 1.0)
```

---

## create_sfx_on_unit_new_new

method in GameAPI

- 描述

    创建特效到单位附加点（跟随旋转使用枚举）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | sfx_id | py.SfxKey | 特效编号 |
    | unit | py.Unit | 单位 |
    | socket | string | 单位挂接点 |
    | rotate_type | integer | 跟随旋转方式 |
    | b_follow_scale | boolean | 是否跟随单位缩放 |
    | speed? | number | 播放速度 |
    | duration? | number | 持续时间 |
    | angle? | number | 角度 |
    | immediately? | boolean | 是否立即删除 |
    | use_sys_d_destroy_way? | boolean | 特效删除的方式是否读表 |
    | detach? | boolean | 是否脱离单位 |
    | show_in_fog? | boolean | 迷雾里显示 |
    | blend_with_fog? | boolean | 迷雾混合 |
    | scale_x? | number | x轴缩放 |
    | scale_y? | number | y轴缩放 |
    | scale_z? | number | z轴缩放 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sfx | 特效 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local sfx_key = 134274569

local result = GameAPI.create_sfx_on_unit_new_new(sfx_key, unit.handle, "socket", 1, true, 1.0, 1.0, 1.0, true, true, true, true, true, 1.0, 1.0, 1.0)
```

---

## create_sfx_on_unit_3

method in GameAPI

- 描述

    创建特效到单位附加点（跟随旋转使用枚举）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | sfx_id | py.SfxKey | 特效编号 |
    | unit | py.Unit | 单位 |
    | socket | string | 单位挂接点 |
    | rotate_type | integer | 跟随旋转方式 |
    | speed? | number | 播放速度 |
    | duration? | number | 持续时间 |
    | angle? | number | 角度 |
    | immediately? | boolean | 是否立即删除 |
    | use_sys_d_destroy_way? | boolean | 特效删除的方式是否读表 |
    | detach? | boolean | 是否脱离单位 |
    | show_in_fog? | boolean | 迷雾里显示 |
    | blend_with_fog? | boolean | 迷雾混合 |
    | scale_x? | number | x轴缩放 |
    | scale_y? | number | y轴缩放 |
    | scale_z? | number | z轴缩放 |
    | follow_change_position? | boolean | 跟随模型缩放改变位置 |
    | follow_change_scale? | boolean | 跟随模型缩放改变尺寸 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sfx | 特效 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local sfx_key = 134274569

local result = GameAPI.create_sfx_on_unit_3(sfx_key, unit.handle, "socket", 1, 1.0, 1.0, 1.0, true, true, true, true, true, 1.0, 1.0, 1.0, true, true)
```

---

## create_sfx_on_modifier_attach_model

method in GameAPI

- 描述

    创建特效到魔法效果挂接模型（跟随旋转使用枚举）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | sfx_id | py.SfxKey | 特效编号 |
    | unit | py.ModifierEntity | 魔法效果 |
    | editor_model_id | py.ModelKey | 挂接模型id |
    | socket | string | 单位挂接点 |
    | rotate_type | integer | 跟随旋转方式 |
    | b_follow_scale | boolean | 是否跟随单位缩放 |
    | speed? | number | 播放速度 |
    | duration? | number | 持续时间 |
    | angle? | number | 角度 |
    | immediately? | boolean | 是否立即删除 |
    | use_sys_d_destroy_way? | boolean | 特效删除的方式是否读表 |
    | detach? | boolean | 是否脱离单位 |
    | show_in_fog? | boolean | 迷雾里显示 |
    | blend_with_fog? | boolean | 迷雾混合 |
    | scale_x? | number | x轴缩放 |
    | scale_y? | number | y轴缩放 |
    | scale_z? | number | z轴缩放 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sfx | 特效 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)
local sfx_key = 134274569
local model_key = 1

local result = GameAPI.create_sfx_on_modifier_attach_model(sfx_key, modifier.handle, model_key, "socket", 1, true, 1.0, 1.0, 1.0, true, true, true, true, true, 1.0, 1.0, 1.0)
```

---

## set_sfx_color_hex

method in GameAPI

- 描述

    设置特效颜色(HEX)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | sfx_entity | py.Sfx | 特效 |
    | color | string | hex |
    | w | number | w |

- 返回值

    无

- 示例

```lua
local sfx = y3.particle.create({ type = 134274569, target = y3.point(0, 0) }).handle

GameAPI.set_sfx_color_hex(sfx, "color", 1.0)
```

---

## set_link_sfx_scale

method in GameAPI

- 描述

    设置闪电特效缩放

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | sfx_entity | py.LinkSfx | 特效 |
    | scale_x | number | x轴缩放 |
    | scale_y | number | y轴缩放 |
    | scale_z | number | z轴缩放 |
    | duration? | number | 过渡时间 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local link_sfx = GameAPI.create_link_sfx_from_unit_to_point(134274569, unit.handle, "origin", GlobalAPI.coord_to_point(Fix32(100), Fix32(100), Fix32(0)), Fix32(0))

GameAPI.set_link_sfx_scale(link_sfx, 1.0, 1.0, 1.0, 1.0)
```

---

## set_link_sfx_animation_speed

method in GameAPI

- 描述

    设置闪电特效动画速度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | sfx_entity | py.LinkSfx | 特效 |
    | speed | number | 动画速度 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local link_sfx = GameAPI.create_link_sfx_from_unit_to_point(134274569, unit.handle, "origin", GlobalAPI.coord_to_point(Fix32(100), Fix32(100), Fix32(0)), Fix32(0))

GameAPI.set_link_sfx_animation_speed(link_sfx, 1.0)
```

---

## add_point_tag

method in GameAPI

- 描述

    给点添加tag

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | fixvec3 | py.Point | 点 |
    | tag | string | tag |

- 返回值

    无

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)

GameAPI.add_point_tag(point, "tag")
```

---

## remove_point_tag

method in GameAPI

- 描述

    给点移除tag

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | fixvec3 | py.Point | 点 |
    | tag | string | tag |

- 返回值

    无

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)

GameAPI.remove_point_tag(point, "tag")
```

---

## get_points_by_tag

method in GameAPI

- 描述

    根据tag获取对应的点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | tag |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_points_by_tag("tag")
```

---

## if_area_has_tag

method in GameAPI

- 描述

    区域是否拥有某tags

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.Area | 区域 |
    | tag | string | tag |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 布尔值 |

- 示例

```lua
local area = y3.area.create_circle_area(y3.point.create(0, 0, 0), 500)

local result = GameAPI.if_area_has_tag(area.handle, "tag")
```

---

## api_reset_cir_area

method in GameAPI

- 描述

    重设圆形区域中心点和半径

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.CirArea | 圆形区域 |
    | center_point | py.Point | 中心点 |
    | radius | py.Fixed | 半径 |

- 返回值

    无

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)
local cir_area = GameAPI.create_new_cir_area(GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0)), Fix32(100))

GameAPI.api_reset_cir_area(cir_area, point, Fix32(1))
```

---

## api_reset_rect_two_point

method in GameAPI

- 描述

    重设矩形区域起点和终点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.RecArea | 矩形区域 |
    | point_begin | py.Point | 起始点 |
    | point_end | py.Point | 终点 |

- 返回值

    无

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)
local rec_area = GameAPI.create_rec_area_from_two_points(Fix32Vec3(0, 0, 0), Fix32Vec3(100, 100, 0))

GameAPI.api_reset_rect_two_point(rec_area, point, point)
```

---

## get_map_id

method in GameAPI

- 描述

    获取当前地图版本id

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MapId | 地图版本id |

- 示例

```lua
local result = GameAPI.get_map_id()
```

---

## get_uppass_env

method in GameAPI

- 描述

    获取当前uppass env

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UppassEnv | uppass env |

- 示例

```lua
local result = GameAPI.get_uppass_env()
```

---

## api_collect_garbage

method in GameAPI

- 描述

    进行一次内存垃圾回收以释放内存。会导致游戏短暂卡顿，建议在切场景等能够接收卡顿的时机调用

- 参数

    无

- 返回值

    无

- 示例

```lua
GameAPI.api_collect_garbage()
```

---

## get_current_level

method in GameAPI

- 描述

    获取当前关卡

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Map | 当前关卡 |

- 示例

```lua
local result = GameAPI.get_current_level()
```

---

## get_client_mode

method in GameAPI

- 描述

    获取当前运行环境

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 当前运行环境 |

- 示例

```lua
local result = GameAPI.get_client_mode()
```

---

## load_sub_scene

method in GameAPI

- 描述

    创建地形预设

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.Point | 点 |
    | level_id_str | py.Map | 关卡ID |
    | has_light? | boolean | 是否携带灯光 |
    | has_decoration? | boolean | 是否携带装饰物 |
    | has_fog? | boolean | 是否携带雾效 |
    | has_projectile? | boolean | 是否携带投射物 |
    | has_item? | boolean | 是否携带物品 |
    | has_destructible? | boolean | 是否携带可破坏物 |
    | has_collision? | boolean | 是否携带碰撞 |
    | rotate? | integer | 旋转角度 |

- 返回值

    无

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)

GameAPI.load_sub_scene(point, 1, true, true, true, true, true, true, true, 1)
```

---

## get_global_map_str_archive

method in GameAPI

- 描述

    获取当前地图的指定key的字符串型存档值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 指定的全局存档key值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串型全局存档值 |

- 示例

```lua
local result = GameAPI.get_global_map_str_archive("key")
```

---

## get_archive_rank_player_tag

method in GameAPI

- 描述

    获取玩家指定的个人存档栏位的第n名玩家昵称的后缀id

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | archive_key | integer | 玩家存档栏位 |
    | num | integer | 第n名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 后缀id |

- 示例

```lua
local result = GameAPI.get_archive_rank_player_tag(1, 1)
```

---

## get_aid_by_rank_info

method in GameAPI

- 描述

    获取排行榜指定排名玩家的aid

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | archive_key | integer | 整数存档 |
    | num | integer | 排名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 玩家aid |

- 示例

```lua
local result = GameAPI.get_aid_by_rank_info(1, 1)
```

---

## get_local_engine_version

method in GameAPI

- 描述

    获取本地引擎版本号

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 本地引擎版本号 |

- 示例

```lua
local result = GameAPI.get_local_engine_version()
```

---

## get_latest_engine_version

method in GameAPI

- 描述

    获取最新引擎版本号

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | http_data | string | http data |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 最新引擎版本号 |

- 示例

```lua
local result = GameAPI.get_latest_engine_version("http_data")
```

---

## get_local_map_id

method in GameAPI

- 描述

    获取本地地图版本号

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 本地地图版本号 |

- 示例

```lua
local result = GameAPI.get_local_map_id()
```

---

## get_latest_map_id

method in GameAPI

- 描述

    获取最新地图版本号

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | http_data | string | http data |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 最新地图版本号 |

- 示例

```lua
local result = GameAPI.get_latest_map_id("http_data")
```

---

## api_get_logic_fps

method in GameAPI

- 描述

    获取逻辑帧率

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 逻辑帧率 |

- 示例

```lua
local result = GameAPI.api_get_logic_fps()
```

---

## api_upload_user_tracking_data

method in GameAPI

- 描述

    上传埋点数据

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | op_key | string | 埋点Key |
    | op_cnt | integer | 次数 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.api_upload_user_tracking_data(player.handle, "op_key", 1)
```

---

## add_detail_log

method in GameAPI

- 描述

    记录自定义日志，用于定位不同步

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | log | string | 日志内容 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 返回值恒定为True |

- 示例

```lua
local result = GameAPI.add_detail_log("log")
```

---

## api_set_enable_detail_snapshot

method in GameAPI

- 描述

    开启/关闭不同步详细日志。默认关闭。这个是总开关，关了这个之后别的设置接口都不生效了了，但性能最好。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | enable? | boolean | 是否开启 |

- 返回值

    无

- 示例

```lua
GameAPI.api_set_enable_detail_snapshot(true)
```

---

## api_set_snapshot_traceback_level

method in GameAPI

- 描述

    设置某些日志的堆栈记录详细等级。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | level? | integer | 等级 |

- 返回值

    无

- 示例

```lua
GameAPI.api_set_snapshot_traceback_level(1)
```

---

## api_set_enable_timer_snapshot

method in GameAPI

- 描述

    开启/关闭timer不同步检测日志。默认关闭。开启后可以检测出哪里多创建了ECA计时器，但计时器不一致并不一定代表着实际游戏内容不同步（比如计时器回调里只做表现层修改就是安全的）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | enable? | boolean | 是否开启 |

- 返回值

    无

- 示例

```lua
GameAPI.api_set_enable_timer_snapshot(true)
```

---

## api_set_enable_ui_snapshot

method in GameAPI

- 描述

    开启/关闭UI界面不同步检测日志。默认关闭。开启后会统计所有UI的创建。UI创建不一致会导致UI的序号不一致，进而导致UI组件/元件转字符串的结果不一致，以及UI相关事件中的【触发事件的控件】不一致，如果游戏中将相关值用于玩法逻辑中，则会导致逻辑不同步。如果确定不会引起不同步，可以选择关闭这个开关

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | enable? | boolean | 是否开启 |

- 返回值

    无

- 示例

```lua
GameAPI.api_set_enable_ui_snapshot(true)
```

---

## api_set_enable_eca_snapshot

method in GameAPI

- 描述

    开启/关闭ECA不同步检测日志。默认关闭，开销较高。可通过参数过滤掉一些安全的API以防止误报，例如创建特效、UI操作等

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | enable | boolean | 是否开启 |
    | filter_mode? | integer | 过滤模式,默认1 剔除模式（不记录filter_set中指定的api）或者0 包含模式（仅记录filter_set中指定的api） |
    | filter_set? | py.Table | 过滤集合，默认为{"client_only", "client_possible"}。可传入想要剔除/包含的API（取决于上个参数），如{"client_only", "client_possible", "GameAPI:print_to_dialog, "GameAPI:get_function_return_value"}。client_only和client_possible为官方确认安全/较安全的API集合，即在{使用得当的情况下}即使调用次数不一致也不会影响游戏核心逻辑，通常可以将其加入剔除集合中以避免误报 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 开启结果 |

- 示例

```lua
local tbl = {}

local result = GameAPI.api_set_enable_eca_snapshot(true, 1)
```

---

## api_set_detail_snapshot_enable_tag

method in GameAPI

- 描述

    设置不同步详细日志级别。越详细越利于定位不同步产生点,但性能消耗会增高

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | integer | mask用于控制开启哪些日志，0xFFFFFFFF全部开启，默认开启16+32。各bit含义>> 1：运动器tick，2：运动器碰撞检测，4：寻路回调，8：寻路坐标更新，16：血量变化，32：坐标瞬变 |

- 返回值

    无

- 示例

```lua
GameAPI.api_set_detail_snapshot_enable_tag(1)
```

---

## api_set_time_scale

method in GameAPI

- 描述

    设置播放速率

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | scale | number | 播放速率 |

- 返回值

    无

- 示例

```lua
GameAPI.api_set_time_scale(1.0)
```

---

## set_joystick_target

method in GameAPI

- 描述

    绑定摇杆单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 摇杆控件ID |
    | unit | py.Unit | 绑定单位 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

GameAPI.set_joystick_target(player.handle, "comp_name", unit.handle)
```

---

## api_set_player_select_unit_priority

method in GameAPI

- 描述

    设置玩家点选单位优先级

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | unit_type | integer | 单位类型 |
    | priority | integer | 优先级 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.api_set_player_select_unit_priority(player.handle, 1, 1)
```

---

## set_local_camera_focus_position

method in GameAPI

- 描述

    设置本地相机聚焦位置

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | position | py.Vector3 | 位置 |

- 返回值

    无

- 示例

```lua
local vector3 = Fix32Vec3(0, 0, 0)

GameAPI.set_local_camera_focus_position(vector3)
```

---

## api_set_rule_mgr_value

method in GameAPI

- 描述

    局内修改游戏规则开关（布尔值）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | integer | 规则枚举值 |
    | value | boolean | 是否开启 |

- 返回值

    无

- 示例

```lua
GameAPI.api_set_rule_mgr_value(1, true)
```

---

## api_set_shortcut_enable

method in GameAPI

- 描述

    局内修改游戏按键功能开关（布尔值）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | integer | 按键规则枚举值 |
    | value | boolean | 是否开启 |

- 返回值

    无

- 示例

```lua
GameAPI.api_set_shortcut_enable(1, true)
```

---

## api_set_obj_twinkle_parameters

method in GameAPI

- 描述

    设置对象的闪烁效果

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | log_obj | py.Actor | 对象 |
    | interval? | number | interval |
    | time? | number | time |
    | color_r? | integer | R |
    | color_g? | integer | G |
    | color_b? | integer | B |
    | alpha? | number | alpha |
    | exp? | number | exp |
    | exp2? | number | exp2 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.api_set_obj_twinkle_parameters(actor, 1.0, 1.0, 1, 1, 1, 1.0, 1.0, 1.0)
```

---

## api_get_obj_fresnel_exp

method in GameAPI

- 描述

    获取对象的菲涅尔指数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | log_obj | py.Actor | 对象 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 指数 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.api_get_obj_fresnel_exp(actor)
```

---

## api_get_obj_fresnel_color_strength

method in GameAPI

- 描述

    获取对象的菲涅尔强度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | log_obj | py.Actor | 对象 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 强度 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.api_get_obj_fresnel_color_strength(actor)
```

---

## enable_player_mini_map_fog_img

method in GameAPI

- 描述

    开启小地图迷雾显示

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | enable | integer | 显示模式 |
    | specify_mini_map? | string | 指定的小地图 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.enable_player_mini_map_fog_img(player.handle, 1, "specify_mini_map")
```

---

## set_mini_map_show_area_by_two_points

method in GameAPI

- 描述

    设置小地图显示区域(两点)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | position1 | py.Point | 点1 |
    | position2 | py.Point | 点2 |

- 返回值

    无

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)
local player = y3.player.get_by_id(1)

GameAPI.set_mini_map_show_area_by_two_points(player.handle, point, point)
```

---

## only_show_local_player_jump_word

method in GameAPI

- 描述

    仅显示本地玩家跳字

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_show | boolean | 是否开启 |

- 返回值

    无

- 示例

```lua
GameAPI.only_show_local_player_jump_word(true)
```

---

## set_global_visibility_of_billboard

method in GameAPI

- 描述

    设置血条的全局可见性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | enable | boolean | 是否开启 |

- 返回值

    无

- 示例

```lua
GameAPI.set_global_visibility_of_billboard(true)
```

---

## get_point_texture

method in GameAPI

- 描述

    获取指定点的纹理类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | position | py.Point | 点 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 纹理类型 |

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)

local result = GameAPI.get_point_texture(point)
```

---

## set_obj_material_param

method in GameAPI

- 描述

    修改对象材质

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | py.Actor | 对象 |
    | material_id | integer | 材质id |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_obj_material_param(actor, 1)
```

---

## set_mouse_cursor_visible

method in GameAPI

- 描述

    设置鼠标是否可见

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | visible | boolean | 是否可见 |

- 返回值

    无

- 示例

```lua
GameAPI.set_mouse_cursor_visible(true)
```

---

## set_mini_map_alpha

method in GameAPI

- 描述

    小地图遮罩透明度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | alpha | number | 透明度 |
    | specify_mini_map? | string | 指定的小地图 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_mini_map_alpha(player.handle, 1.0, "specify_mini_map")
```

---

## set_mini_map_color_int

method in GameAPI

- 描述

    小地图遮罩颜色

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | colorR | integer | R |
    | colorG | integer | G |
    | colorB | integer | B |
    | colorA | integer | A |
    | specify_mini_map? | string | 指定的小地图 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_mini_map_color_int(player.handle, 1, 1, 1, 1, "specify_mini_map")
```

---

## set_mini_map_color_str

method in GameAPI

- 描述

    小地图遮罩颜色

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | rgb_hex | string | rgb |
    | alpha | number | a |
    | specify_mini_map? | string | 指定的小地图 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_mini_map_color_str(player.handle, "rgb_hex", 1.0, "specify_mini_map")
```

---

## api_set_hero_mini_map_frame

method in GameAPI

- 描述

    小地图 - 设置英雄小地图头像底框

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | unit | py.Unit | 单位 |
    | image_id | py.Texture | 图片id |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

GameAPI.api_set_hero_mini_map_frame(player.handle, unit.handle, 1)
```

---

## int_transform_unit_type

method in GameAPI

- 描述

    整数转单位类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | int_num | integer | 整数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitType | 单位类型 |

- 示例

```lua
local result = GameAPI.int_transform_unit_type(1)
```

---

## int_transform_projectile_type

method in GameAPI

- 描述

    整数转投射物类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | int_num | integer | 整数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileKey | 投射物类型 |

- 示例

```lua
local result = GameAPI.int_transform_projectile_type(1)
```

---

## int_transform_item_type

method in GameAPI

- 描述

    整数转物品类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | int_num | integer | 整数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemKey | 物品类型 |

- 示例

```lua
local result = GameAPI.int_transform_item_type(1)
```

---

## int_transform_modifier_type

method in GameAPI

- 描述

    整数转魔法效果类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | int_num | integer | 整数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierType | 魔法效果类型 |

- 示例

```lua
local result = GameAPI.int_transform_modifier_type(1)
```

---

## int_transform_ability_type

method in GameAPI

- 描述

    整数转技能类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | int_num | integer | 整数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityKey | 技能类型 |

- 示例

```lua
local result = GameAPI.int_transform_ability_type(1)
```

---

## int_transform_tech_type

method in GameAPI

- 描述

    整数转科技类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | int_num | integer | 整数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.TechKey | 科技类型 |

- 示例

```lua
local result = GameAPI.int_transform_tech_type(1)
```

---

## int_transform_destruct_type

method in GameAPI

- 描述

    整数转可破坏物类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | int_num | integer | 整数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DestructibleKey | 可破坏物类型 |

- 示例

```lua
local result = GameAPI.int_transform_destruct_type(1)
```

---

## int_transform_sound_type

method in GameAPI

- 描述

    整数转声音类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | int_num | integer | 整数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AudioKey | 声音类型 |

- 示例

```lua
local result = GameAPI.int_transform_sound_type(1)
```

---

## steam_get_team_id

method in GameAPI

- 描述

    获取队伍id

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 队伍id |

- 示例

```lua
local result = GameAPI.steam_get_team_id()
```

---

## steam_get_player_id

method in GameAPI

- 描述

    获取玩家id

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 玩家id |

- 示例

```lua
local result = GameAPI.steam_get_player_id()
```

---

## steam_get_player_head_icon_url

method in GameAPI

- 描述

    获取本地玩家头像url

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 头像url |

- 示例

```lua
local result = GameAPI.steam_get_player_head_icon_url()
```

---

## steam_get_team_state

method in GameAPI

- 描述

    获取队伍状态

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 队伍状态 |

- 示例

```lua
local result = GameAPI.steam_get_team_state()
```

---

## get_is_steam_lobby

method in GameAPI

- 描述

    获取是否是大厅关卡

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | bool |

- 示例

```lua
local result = GameAPI.get_is_steam_lobby()
```

---

## steam_get_player_state

method in GameAPI

- 描述

    获取玩家状态

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 玩家状态 |

- 示例

```lua
local result = GameAPI.steam_get_player_state()
```

---

## steam_get_player_nickname

method in GameAPI

- 描述

    获取本地玩家的名称

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 玩家名称 |

- 示例

```lua
local result = GameAPI.steam_get_player_nickname()
```

---

## steam_get_player_storm_items

method in GameAPI

- 描述

    获取本地玩家背包内的道具

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Table | 物品表 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.steam_get_player_storm_items(player.handle)
```

---

## set_ui_comp_image_with_icon_steam

method in GameAPI

- 描述

    设置ui组件图片(图片类型)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | image_id | py.Texture | 图片 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_image_with_icon_steam(player.handle, "comp_name", 1)
```

---

## get_steam_player_currency

method in GameAPI

- 描述

    获取玩家steam国区

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.COIN_CURRENCY | steam币种 |

- 示例

```lua
local result = GameAPI.get_steam_player_currency()
```

---

## get_steam_goods_price

method in GameAPI

- 描述

    获取玩家商品对应国区价格

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | goods_id | string | 商品ID |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 价格 |

- 示例

```lua
local result = GameAPI.get_steam_goods_price("goods_id")
```

---

## set_steam_global_archive_data

method in GameAPI

- 描述

    设置steam大厅的指定key的全局存档值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 全局存档key值 |
    | value | py.Actor | 设置的数值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_steam_global_archive_data("key", actor)
```

---

## add_steam_global_archive_data

method in GameAPI

- 描述

    增加steam大厅的指定key的全局存档值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 全局存档key值 |
    | value | integer | 增加的数值 |

- 返回值

    无

- 示例

```lua
GameAPI.add_steam_global_archive_data("key", 1)
```

---

## request_buy_mall_coin

method in GameAPI

- 描述

    请求购买

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | py.Role | 玩家 |
    | goods_id | string | 物品ID |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.request_buy_mall_coin(player.handle, "goods_id")
```

---

## set_draw_ui

method in GameAPI

- 描述

    设置是否渲染场景

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_open | boolean | bool |

- 返回值

    无

- 示例

```lua
GameAPI.set_draw_ui(true)
```

---

## get_local_game_version

method in GameAPI

- 描述

    获取本地游戏版本号

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 本地游戏版本号 |

- 示例

```lua
local result = GameAPI.get_local_game_version()
```

---

## get_latest_game_version

method in GameAPI

- 描述

    获取最新游戏版本号

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | http_data | string | http data |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 最新游戏版本号 |

- 示例

```lua
local result = GameAPI.get_latest_game_version("http_data")
```

---

## get_settle_ladder_role

method in GameAPI

- 描述

    获取进行结算的玩家

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | v | py.RoleID | 玩家 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Role | 玩家 |

- 示例

```lua
local role_id = 1

local result = GameAPI.get_settle_ladder_role(role_id)
```

---

## get_settle_ladder_new_score

method in GameAPI

- 描述

    获取进行结算的玩家新分数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | v | integer | 玩家新分数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 玩家新分数 |

- 示例

```lua
local result = GameAPI.get_settle_ladder_new_score(1)
```

---

## get_settle_ladder_diff_value

method in GameAPI

- 描述

    获取进行结算的玩家匹配分修正值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | v | integer | 玩家分差值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 玩家分差值 |

- 示例

```lua
local result = GameAPI.get_settle_ladder_diff_value(1)
```

---

## lua_request_change_room_name

method in GameAPI

- 描述

    请求更改房间名称

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | room_name | string | 房间名称 |
    | lua_func | function | 回调函数 |
    | context | py.Dict | 回调传参 |

- 返回值

    无

- 示例

```lua
local dict = pydict()

GameAPI.lua_request_change_room_name("room_name", function() end, dict)
```

---

## lua_request_message_from_server

method in GameAPI

- 描述

    请求服务器时间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | lua_func | function | 回调函数 |
    | context | py.Dict | 回调传参 |

- 返回值

    无

- 示例

```lua
local dict = pydict()

GameAPI.lua_request_message_from_server(function() end, dict)
```

---

## lua_request_get_map_rank

method in GameAPI

- 描述

    请求获取最新排行榜的值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | archive_key | integer | 玩家存档栏位 |
    | lua_func | function | 回调函数 |

- 返回值

    无

- 示例

```lua
GameAPI.lua_request_get_map_rank(1, function() end)
```

---

## lua_request_server_time

method in GameAPI

- 描述

    请求服务器时间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | lua_func | function | 回调函数 |
    | context | py.Dict | 回调传参 |

- 返回值

    无

- 示例

```lua
local dict = pydict()

GameAPI.lua_request_server_time(function() end, dict)
```

---

## lua_request_server_role_use_item

method in GameAPI

- 描述

    请求服务器获取玩家使用道具

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | count | integer | 数量 |
    | no | integer | 道具ID |
    | lua_func | function | 回调函数 |
    | context | py.Dict | 回调传参 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local dict = pydict()

GameAPI.lua_request_server_role_use_item(player.handle, 1, 1, function() end, dict)
```

---

## lua_request_server_random_pool_result

method in GameAPI

- 描述

    执行服务器随机池掉落策略

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | pool_id | integer | 随机池ID |
    | lua_func | function | 回调函数 |
    | context | py.Dict | 回调传参 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local dict = pydict()

GameAPI.lua_request_server_random_pool_result(player.handle, 1, function() end, dict)
```

---

## lua_request_server_mall_goods_info

method in GameAPI

- 描述

    请求服务器获取商品信息

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | goods_id | string | 商品ID |
    | lua_func | function | 回调函数 |
    | context | py.Dict | 回调传参 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local dict = pydict()

GameAPI.lua_request_server_mall_goods_info(player.handle, "goods_id", function() end, dict)
```

---

## lua_request_server_consume_mall_coin

method in GameAPI

- 描述

    请求服务器获取商城消耗货币

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | amount | integer | 数量 |
    | lua_func | function | 回调函数 |
    | context | py.Dict | 回调传参 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local dict = pydict()

GameAPI.lua_request_server_consume_mall_coin(player.handle, 1, function() end, dict)
```

---

## lua_request_server_mall_purchase_goods

method in GameAPI

- 描述

    请求服务器购买商品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | count | integer | 商品数量 |
    | no | string | 商品ID |
    | lua_func | function | 回调函数 |
    | context | py.Dict | 回调传参 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local dict = pydict()

GameAPI.lua_request_server_mall_purchase_goods(player.handle, 1, "no", function() end, dict)
```

---

## lua_request_server_mall_dlc_status

method in GameAPI

- 描述

    请求服务器获取商城dlc状态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | goods_id | string | 商品ID |
    | lua_func | function | 回调函数 |
    | context | py.Dict | 回调传参 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local dict = pydict()

GameAPI.lua_request_server_mall_dlc_status(player.handle, "goods_id", function() end, dict)
```

---

## lua_request_server_create_room

method in GameAPI

- 描述

    steam创建房间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | room_name | string | 房间名称 |
    | lua_func | function | 回调函数 |
    | context | py.Dict | 回调传参 |
    | mode_id? | integer | 游戏模式 |
    | password? | string | 房间密码 |

- 返回值

    无

- 示例

```lua
local dict = pydict()

GameAPI.lua_request_server_create_room("room_name", function() end, dict, 1, "password")
```

---

## lua_request_server_room_list_info

method in GameAPI

- 描述

    steam请求房间列表

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | lua_func | function | 回调函数 |
    | context | py.Dict | 回调传参 |
    | page_index | string | 房间页数 |

- 返回值

    无

- 示例

```lua
local dict = pydict()

GameAPI.lua_request_server_room_list_info(function() end, dict, "page_index")
```

---

## lua_request_server_join_room

method in GameAPI

- 描述

    steam请求加入房间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | room_id | integer | 房间id |
    | lua_func | function | 回调函数 |
    | context | py.Dict | 回调传参 |
    | password | string | 房间密码 |

- 返回值

    无

- 示例

```lua
local dict = pydict()

GameAPI.lua_request_server_join_room(1, function() end, dict, "password")
```

---

## lua_request_server_room_info

method in GameAPI

- 描述

    steam请求房间信息

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | aid | integer | 玩家id |
    | lua_func | function | 回调函数 |
    | context | py.Dict | 回调传参 |

- 返回值

    无

- 示例

```lua
local dict = pydict()

GameAPI.lua_request_server_room_info(1, function() end, dict)
```

---

## lua_request_server_room_strat_game

method in GameAPI

- 描述

    steam请求房间开始游戏

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | lua_func | function | 回调函数 |
    | context | py.Dict | 回调传参 |

- 返回值

    无

- 示例

```lua
local dict = pydict()

GameAPI.lua_request_server_room_strat_game(function() end, dict)
```

---

## lua_request_server_invite_player_join_room

method in GameAPI

- 描述

    steam邀请玩家加入房间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | aid | integer | 玩家id |
    | lua_func | function | 回调函数 |
    | context | py.Dict | 回调传参 |

- 返回值

    无

- 示例

```lua
local dict = pydict()

GameAPI.lua_request_server_invite_player_join_room(1, function() end, dict)
```

---

## lua_request_server_reply_room_invite

method in GameAPI

- 描述

    steam接受房间邀请

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | aid | integer | 玩家id |
    | room_id | integer | 房间id |
    | lua_func | function | 回调函数 |
    | context | py.Dict | 回调传参 |

- 返回值

    无

- 示例

```lua
local dict = pydict()

GameAPI.lua_request_server_reply_room_invite(1, 1, function() end, dict)
```

---

## lua_request_server_change_room_slot

method in GameAPI

- 描述

    steam交换房间槽位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | slot_index | integer | 槽位 |
    | lua_func | function | 回调函数 |
    | context | py.Dict | 回调传参 |

- 返回值

    无

- 示例

```lua
local dict = pydict()

GameAPI.lua_request_server_change_room_slot(1, function() end, dict)
```

---

## lua_request_server_change_owner

method in GameAPI

- 描述

    steam交换房主

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | aid | integer | 玩家id |
    | lua_func | function | 回调函数 |
    | context | py.Dict | 回调传参 |

- 返回值

    无

- 示例

```lua
local dict = pydict()

GameAPI.lua_request_server_change_owner(1, function() end, dict)
```

---

## lua_request_server_exit_room

method in GameAPI

- 描述

    steam退出房间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | aid | integer | 玩家id |
    | lua_func | function | 回调函数 |
    | context | py.Dict | 回调传参 |

- 返回值

    无

- 示例

```lua
local dict = pydict()

GameAPI.lua_request_server_exit_room(1, function() end, dict)
```

---

## lua_request_server_kick_from_room

method in GameAPI

- 描述

    steam踢出房间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | aid | integer | 玩家id |
    | lua_func | function | 回调函数 |
    | context | py.Dict | 回调传参 |

- 返回值

    无

- 示例

```lua
local dict = pydict()

GameAPI.lua_request_server_kick_from_room(1, function() end, dict)
```

---

## lua_request_server_set_site_state

method in GameAPI

- 描述

    steam改变位置状态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | slot_index | integer | 槽位 |
    | state | integer | 槽位 |
    | lua_func | function | 回调函数 |
    | context | py.Dict | 回调传参 |

- 返回值

    无

- 示例

```lua
local dict = pydict()

GameAPI.lua_request_server_set_site_state(1, 1, function() end, dict)
```

---

## lua_request_server_change_room_password

method in GameAPI

- 描述

    steam更改房间密码

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | pass_word | string | 密码 |
    | lua_func | function | 回调函数 |
    | context | py.Dict | 回调传参 |

- 返回值

    无

- 示例

```lua
local dict = pydict()

GameAPI.lua_request_server_change_room_password("pass_word", function() end, dict)
```

---

## lua_request_server_change_room_level_limit

method in GameAPI

- 描述

    steam更改房间等级

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | level_min | string | 最小等级 |
    | level_max | string | 最大等级 |
    | lua_func | function | 回调函数 |
    | context | py.Dict | 回调传参 |

- 返回值

    无

- 示例

```lua
local dict = pydict()

GameAPI.lua_request_server_change_room_level_limit("level_min", "level_max", function() end, dict)
```

---

## lua_request_my_team_info

method in GameAPI

- 描述

    steam查询自己的队伍信息

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | lua_func | function | 回调函数 |
    | context | py.Dict | 回调传参 |

- 返回值

    无

- 示例

```lua
local dict = pydict()

GameAPI.lua_request_my_team_info(function() end, dict)
```

---

## api_destroy_force

method in GameAPI

- 描述

    删除牵引力

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | force_id | py.Force | 牵引力 |

- 返回值

    无

- 示例

```lua
GameAPI.api_destroy_force(1)
```

---

## create_force_direction

method in GameAPI

- 描述

    创建牵引力方向

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | target_unit | py.Unit | 目标单位 |
    | force_angle | py.Fixed | 方向角度 |
    | speed | py.Fixed | 速度 |
    | max_speed | py.Fixed | 最大速度 |
    | min_speed | py.Fixed | 最小速度 |
    | acc | py.Fixed | 加速度 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 牵引力对象 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = GameAPI.create_force_direction(unit.handle, Fix32(1), Fix32(1), Fix32(1), Fix32(1), Fix32(1))
```

---

## create_force_point

method in GameAPI

- 描述

    创建牵引力点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | target_unit | py.Unit | 目标单位 |
    | force_point | py.Point | 中心点 |
    | speed | py.Fixed | 速度 |
    | max_speed | py.Fixed | 最大速度 |
    | min_speed | py.Fixed | 最小速度 |
    | acc | py.Fixed | 加速度 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 牵引力对象 |

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = GameAPI.create_force_point(unit.handle, point, Fix32(1), Fix32(1), Fix32(1), Fix32(1))
```

---

## create_force_target

method in GameAPI

- 描述

    创建牵引力目标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | target_unit | py.Unit | 目标单位 |
    | force_unit | py.Unit | 牵引力单位 |
    | speed | py.Fixed | 速度 |
    | max_speed | py.Fixed | 最大速度 |
    | min_speed | py.Fixed | 最小速度 |
    | acc | py.Fixed | 加速度 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 牵引力对象 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = GameAPI.create_force_target(unit.handle, unit.handle, Fix32(1), Fix32(1), Fix32(1), Fix32(1))
```

---

## set_ui_image_color_hex

method in GameAPI

- 描述

    设置图片颜色(hex)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件名 |
    | color | string | hex |
    | a | number | A |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_image_color_hex(player.handle, "comp_uid", "color", 1.0)
```

---

## get_ui_image_color

method in GameAPI

- 描述

    【异步】获取图片颜色

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | comp_uid | string | 控件名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 图片颜色hex值 |

- 示例

```lua
local result = GameAPI.get_ui_image_color("comp_uid")
```

---

## ui_comp_role_exist

method in GameAPI

- 描述

    界面组件是否存在

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | ui_comp | string | 界面组件名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.ui_comp_role_exist(player.handle, "ui_comp")
```

---

## set_ui_comp_pos_percent

method in GameAPI

- 描述

    设置ui组件坐标百分比

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | x | number | x |
    | y | number | y |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_pos_percent(player.handle, "comp_name", 1.0, 1.0)
```

---

## set_ui_comp_pos_mode

method in GameAPI

- 描述

    设置ui组件坐标适配模式

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | x_mode | integer | x_mode |
    | y_mode | integer | y_mode |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_pos_mode(player.handle, "comp_name", 1, 1)
```

---

## set_ui_comp_font_color_norm

method in GameAPI

- 描述

    设置ui文本颜色

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | r | number | R |
    | g | number | G |
    | b | number | B |
    | a | number | A |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_font_color_norm(player.handle, "comp_name", 1.0, 1.0, 1.0, 1.0)
```

---

## set_ui_comp_font_color_hex

method in GameAPI

- 描述

    设置ui文本颜色(HEX)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | color | string | hex |
    | a | number | A |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_font_color_hex(player.handle, "comp_name", "color", 1.0)
```

---

## get_ui_comp_font_color

method in GameAPI

- 描述

    【异步】获取ui文本颜色

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | comp_uid | string | 控件名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 颜色hex值 |

- 示例

```lua
local result = GameAPI.get_ui_comp_font_color("comp_uid")
```

---

## set_ui_comp_text_multilingual

method in GameAPI

- 描述

    设置ui文本多语言

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | text0 | string | 文本 |
    | text1? | string | 拼接文本1 |
    | text2? | string | 拼接文本2 |
    | text3? | string | 拼接文本3 |
    | text4? | string | 拼接文本4 |
    | text5? | string | 拼接文本5 |
    | text6? | string | 拼接文本6 |
    | text7? | string | 拼接文本7 |
    | text8? | string | 拼接文本8 |
    | text9? | string | 拼接文本9 |
    | text10? | string | 拼接文本10 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_text_multilingual(player.handle, "comp_name", "text0", "text1", "text2", "text3", "text4", "text5", "text6", "text7", "text8", "text9", "text10")
```

---

## play_ui_comp_anim_new

method in GameAPI

- 描述

    新播放UI控件时间轴动画

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | anim_id | py.UIAnimKey | UI动画 |
    | start_frame? | integer | 起始帧 |
    | end_frame? | integer | 结束帧 |
    | speed? | number | 播放速度 |
    | play_mode? | integer | 播放模式 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui_anim_key = GameAPI.get_unit_key_ui_anim_kv(1, "key")

GameAPI.play_ui_comp_anim_new(player.handle, ui_anim_key, 1, 1, 1.0, 1)
```

---

## api_set_ability_release_timing

method in GameAPI

- 描述

    设置技能按钮施法的时机

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | release_timing | integer | 施法时机 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.api_set_ability_release_timing(player.handle, "comp_name", 1)
```

---

## api_set_ability_mouse_control_key

method in GameAPI

- 描述

    设置技能按钮鼠标操控快捷键

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | key | integer | 快捷键 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.api_set_ability_mouse_control_key(player.handle, "comp_name", 1)
```

---

## get_ui_comp_opacity

method in GameAPI

- 描述

    【异步】获取控件透明度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | comp_name | string | 控件名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 透明度 |

- 示例

```lua
local result = GameAPI.get_ui_comp_opacity("comp_name")
```

---

## set_ui_comp_unit_slot_new

method in GameAPI

- 描述

    设置道具栏控件类型和槽位号

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | unit | py.Unit | 单位 |
    | slot_type | py.SlotType | 类型 |
    | slot_index | integer | 槽位id |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)
local slot_type = y3.const.SlotType.BAR

GameAPI.set_ui_comp_unit_slot_new(player.handle, "comp_name", unit.handle, slot_type, 1)
```

---

## set_ui_model_id_from_object_editor

method in GameAPI

- 描述

    设置模型控件的物编模型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | unit_id | py.UnitID | 模型id |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local unit_id = 134274569

GameAPI.set_ui_model_id_from_object_editor(player.handle, "comp_name", unit_id)
```

---

## set_ui_model_from_scene_unit_with_tag_model

method in GameAPI

- 描述

    设置模型控件的模型为场景中设定了指定标签的模型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | unit | py.Unit | 单位对象 |
    | clone_effect? | boolean | 继承特效 |
    | clone_attach? | boolean | 继承挂接模型 |
    | clone_material? | boolean | 继承材质变化 |
    | is_show_mount? | boolean | 是否显示坐骑 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

GameAPI.set_ui_model_from_scene_unit_with_tag_model(player.handle, "comp_name", unit.handle, true, true, true, true)
```

---

## set_ui_model_model_scale

method in GameAPI

- 描述

    设置模型控件模型缩放

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | scale | number | 模型缩放 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_model_model_scale(player.handle, "comp_name", 1.0)
```

---

## set_ui_model_unit

method in GameAPI

- 描述

    设置UI模型控件单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | model_unit | py.Unit | 单位 |
    | clone_effect? | boolean | 继承特效 |
    | clone_attach? | boolean | 继承挂接模型 |
    | clone_material? | boolean | 继承材质变化 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

GameAPI.set_ui_model_unit(player.handle, "comp_name", unit.handle, true, true, true)
```

---

## set_modifier_on_ui_model

method in GameAPI

- 描述

    播放魔法效果表现到模型控件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果类型 |
    | modifier_state | integer | 播放枚举 |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local modifier_key = 134274569

GameAPI.set_modifier_on_ui_model(modifier_key, 1, player.handle, "comp_name")
```

---

## play_ui_spine

method in GameAPI

- 描述

    播放spine动画

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | uid | string | 控件uid |
    | fx_id | py.Spine | 控件动效工程id |
    | ani_name | string | 动效名 |
    | loop? | boolean | 循环 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.play_ui_spine(player.handle, "uid", 1, "ani_name", true)
```

---

## get_slider_cur_percent_safe

method in GameAPI

- 描述

    【同步】获取滑动条当前值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_id | string | 滑动条 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | value |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_slider_cur_percent_safe(player.handle, "comp_id")
```

---

## set_ui_comp_bind_modifier_cycle

method in GameAPI

- 描述

    绑定魔法效果剩余循环周期到玩家界面控件的属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | ui_comp | string | 控件uid |
    | ui_comp_attr | string | 控件属性字段 |
    | modifier | py.ModifierEntity | 技能实体对象 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_bind_modifier_cycle(player.handle, "ui_comp", "ui_comp_attr", modifier.handle)
```

---

## get_list_view_percent

method in GameAPI

- 描述

    【异步】获取列表当前百分比位置

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件uid |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 百分比 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_list_view_percent(player.handle, "comp_name")
```

---

## set_list_view_layout_reverse

method in GameAPI

- 描述

    设置列表反向排布

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件uid |
    | enable | boolean | 开启/关闭反向排布 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_list_view_layout_reverse(player.handle, "comp_name", true)
```

---

## get_ui_comp_by_prefab_ins

method in GameAPI

- 描述

    通过预制实例获得ui控件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_ins | py.UIPrefabIns | 预制 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 控件uid |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui_prefab_ins = GameAPI.get_ui_prefab_ins(player.handle, "prefab_uid")

local result = GameAPI.get_ui_comp_by_prefab_ins(ui_prefab_ins)
```

---

## stop_eca_anim

method in GameAPI

- 描述

    停止播放控件动画

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件uid |
    | anim_type | integer | 动画类型 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.stop_eca_anim(player.handle, "comp_name", 1)
```

---

## set_equip_slot_use_operation

method in GameAPI

- 描述

    设置使用物品操作方式

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | use_operation | integer | 操作方式 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_equip_slot_use_operation(player.handle, "comp_uid", 1)
```

---

## set_equip_slot_drag_operation

method in GameAPI

- 描述

    设置拖拽物品操作方式

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | drag_operation | integer | 操作方式 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_equip_slot_drag_operation(player.handle, "comp_uid", 1)
```

---

## get_page_view_current_index

method in GameAPI

- 描述

    【异步】获取轮播图当前图片索引

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 索引值 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_page_view_current_index(player.handle, "comp_uid")
```

---

## get_page_view_click_index

method in GameAPI

- 描述

    【异步】获取轮播图点击图片索引

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 索引值 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_page_view_click_index(player.handle, "comp_uid")
```

---

## get_checkbox_selected

method in GameAPI

- 描述

    获取复选框当前选中状态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件uid |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 当前选中状态 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_checkbox_selected(player.handle, "comp_name")
```

---

## set_checkbox_selected

method in GameAPI

- 描述

    设置复选框当前选中状态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件uid |
    | is_selected | boolean | 选中状态 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_checkbox_selected(player.handle, "comp_name", true)
```

---

## get_tab_widget_current_index

method in GameAPI

- 描述

    【异步】界面-获取标签页控件当前选中页索引

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 索引 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_tab_widget_current_index(player.handle, "comp_uid")
```

---

## set_tab_widget_current_index

method in GameAPI

- 描述

    界面-设置标签页控件当前选中页索引

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | index | integer | 索引 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_tab_widget_current_index(player.handle, "comp_uid", 1)
```

---

## get_ui_comp_path

method in GameAPI

- 描述

    【异步】界面-获取控件路径

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 路径 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_ui_comp_path(player.handle, "comp_uid")
```

---

## play_live2d_anim

method in GameAPI

- 描述

    live2d控件播放动画

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | motion_name | string | 动画名称 |
    | ith? | integer | 序号 |
    | priority? | integer | 优先级 |
    | loop? | boolean | 是否延续之前的播放 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.play_live2d_anim(player.handle, "comp_uid", "motion_name", 1, 1, true)
```

---

## stop_live2d_anim

method in GameAPI

- 描述

    live2d控件停止播放动画

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | motion_name | string | 动画名称 |
    | ith | integer | 序号 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.stop_live2d_anim(player.handle, "comp_uid", "motion_name", 1)
```

---

## set_live2d_model_id

method in GameAPI

- 描述

    live2d设置模型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | model_id | py.Live2d | live2d资源 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_live2d_model_id(player.handle, "comp_uid", 1)
```

---

## set_live2d_expression

method in GameAPI

- 描述

    live2d设置表情

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | expression | string | 表情名称 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_live2d_expression(player.handle, "comp_uid", "expression")
```

---

## set_live2d_background_color

method in GameAPI

- 描述

    live2d设置背景色

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | r | number | R |
    | g | number | G |
    | b | number | B |
    | a | number | A |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_live2d_background_color(player.handle, "comp_name", 1.0, 1.0, 1.0, 1.0)
```

---

## del_ui_comp_event

method in GameAPI

- 描述

    界面-删除界面事件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | comp_uid | string | 控件uid |
    | event_type | integer | 控件事件类型 |
    | name | string | 自定义事件名 |

- 返回值

    无

- 示例

```lua
GameAPI.del_ui_comp_event("comp_uid", 1, "name")
```

---

## set_layout_clipping_enable

method in GameAPI

- 描述

    设置layout是否裁剪

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | clip_enabled | boolean | 是否裁剪 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_layout_clipping_enable(player.handle, "comp_uid", true)
```

---

## set_input_field_enable

method in GameAPI

- 描述

    设置输入框是否可用

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | enable | boolean | 是否可用 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_input_field_enable(player.handle, "comp_uid", true)
```

---

## set_layout_clipping_type

method in GameAPI

- 描述

    设置layout裁剪模式

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | clipping_type | integer | 裁剪模式 |
    | image_id? | integer | 图片id |
    | color? | string | 颜色 |
    | alpha? | integer | 不透明度 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_layout_clipping_type(player.handle, "comp_uid", 1, 1, "color", 1)
```

---

## set_text_over_length_handling_type

method in GameAPI

- 描述

    设置文本超框处理方式

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | over_pattern | py.DynamicTypeMeta | 超框处理类型 |
    | font_min_size? | integer | 最小字号 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local dynamic_type = GameAPI.get_function_return_value("func_id", y3.player.get_by_id(1):get_all_units()[1].handle, pydict(), {}, 1)

GameAPI.set_text_over_length_handling_type(player.handle, "comp_uid", dynamic_type, 1)
```

---

## set_ui_gridview_type

method in GameAPI

- 描述

    设置网格列表布局方式

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | layout_type | integer | 布局方式 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_gridview_type(player.handle, "comp_uid", 1)
```

---

## set_ui_gridview_count

method in GameAPI

- 描述

    设置网格列表行数列数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | row_count | integer | 行数 |
    | column_count | integer | 列数 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_gridview_count(player.handle, "comp_uid", 1, 1)
```

---

## set_ui_gridview_size

method in GameAPI

- 描述

    设置网格列表单元格宽高

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | width | number | 宽 |
    | height | number | 高 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_gridview_size(player.handle, "comp_uid", 1.0, 1.0)
```

---

## set_ui_gridview_margin

method in GameAPI

- 描述

    设置网格列表边距

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | top | number | 上 |
    | bottom | number | 下 |
    | left | number | 左 |
    | right | number | 右 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_gridview_margin(player.handle, "comp_uid", 1.0, 1.0, 1.0, 1.0)
```

---

## set_ui_gridview_space

method in GameAPI

- 描述

    设置网格列表单元格间距

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | width | number | 横向 |
    | height | number | 纵向 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_gridview_space(player.handle, "comp_uid", 1.0, 1.0)
```

---

## set_ui_gridview_align

method in GameAPI

- 描述

    设置网格列表对齐方式

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | align_type | integer | 对齐方式 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_gridview_align(player.handle, "comp_uid", 1)
```

---

## insert_ui_gridview_comp

method in GameAPI

- 描述

    添加控件到网格列表指定位置

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | grid_uid | string | 网格列表uid |
    | child_index | integer | 位置索引 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.insert_ui_gridview_comp(player.handle, "comp_uid", "grid_uid", 1)
```

---

## set_ui_gridview_scroll

method in GameAPI

- 描述

    设置网格列表启用/禁止滚动

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | enable | boolean | 是否启用 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_gridview_scroll(player.handle, "comp_uid", true)
```

---

## set_ui_gridview_size_adaptive

method in GameAPI

- 描述

    设置网格列表启用/禁止尺寸随内容变化

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | enable | boolean | 是否启用 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_gridview_size_adaptive(player.handle, "comp_uid", true)
```

---
