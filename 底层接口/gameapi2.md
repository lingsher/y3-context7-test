---
sidebarDepth: 1
---
# GameAPI (Part 2)

# 索引

Y3 编辑器 GameAPI 接口集合（第 2 部分），包含游戏核心功能。

---

| 接口 | 描述 |
| --- | --- |
| [get_trigger_actor_variable_unit_entity](#get_trigger_actor_variable_unit_entity) | 获取触发器UNIT_ENTITY非数组 组变量 |
| [get_trigger_list_variable_unit_entity](#get_trigger_list_variable_unit_entity) | 获取全局触发器UNIT_ENTITY数组变量子项 |
| [get_trigger_list_actor_variable_unit_entity](#get_trigger_list_actor_variable_unit_entity) | 获取触发器UNIT_ENTITY数组 组变量子项 |
| [get_trigger_list_variable_all_unit_entity](#get_trigger_list_variable_all_unit_entity) | 获取全局触发器UNIT_ENTITY数组变量 |
| [get_trigger_list_actor_variable_all_unit_entity](#get_trigger_list_actor_variable_all_unit_entity) | 获取触发器UNIT_ENTITY 组变量数组 |
| [get_trigger_variable_unit_group](#get_trigger_variable_unit_group) | 获取全局触发器UNIT_GROUP非数组变量 |
| [get_trigger_actor_variable_unit_group](#get_trigger_actor_variable_unit_group) | 获取触发器UNIT_GROUP非数组 组变量 |
| [get_trigger_list_variable_unit_group](#get_trigger_list_variable_unit_group) | 获取全局触发器UNIT_GROUP数组变量子项 |
| [get_trigger_list_actor_variable_unit_group](#get_trigger_list_actor_variable_unit_group) | 获取触发器UNIT_GROUP数组 组变量子项 |
| [get_trigger_list_variable_all_unit_group](#get_trigger_list_variable_all_unit_group) | 获取全局触发器UNIT_GROUP数组变量 |
| [get_trigger_list_actor_variable_all_unit_group](#get_trigger_list_actor_variable_all_unit_group) | 获取触发器UNIT_GROUP 组变量数组 |
| [get_trigger_variable_unit_name](#get_trigger_variable_unit_name) | 获取全局触发器UNIT_NAME非数组变量 |
| [get_trigger_actor_variable_unit_name](#get_trigger_actor_variable_unit_name) | 获取触发器UNIT_NAME非数组 组变量 |
| [get_trigger_list_variable_unit_name](#get_trigger_list_variable_unit_name) | 获取全局触发器UNIT_NAME数组变量子项 |
| [get_trigger_list_actor_variable_unit_name](#get_trigger_list_actor_variable_unit_name) | 获取触发器UNIT_NAME数组 组变量子项 |
| [get_trigger_list_variable_all_unit_name](#get_trigger_list_variable_all_unit_name) | 获取全局触发器UNIT_NAME数组变量 |
| [get_trigger_list_actor_variable_all_unit_name](#get_trigger_list_actor_variable_all_unit_name) | 获取触发器UNIT_NAME 组变量数组 |
| [get_trigger_variable_unit_name_pool](#get_trigger_variable_unit_name_pool) | 获取全局触发器UNIT_NAME_POOL非数组变量 |
| [get_trigger_actor_variable_unit_name_pool](#get_trigger_actor_variable_unit_name_pool) | 获取触发器UNIT_NAME_POOL非数组 组变量 |
| [get_trigger_list_variable_unit_name_pool](#get_trigger_list_variable_unit_name_pool) | 获取全局触发器UNIT_NAME_POOL数组变量子项 |
| [get_trigger_list_actor_variable_unit_name_pool](#get_trigger_list_actor_variable_unit_name_pool) | 获取触发器UNIT_NAME_POOL数组 组变量子项 |
| [get_trigger_list_variable_all_unit_name_pool](#get_trigger_list_variable_all_unit_name_pool) | 获取全局触发器UNIT_NAME_POOL数组变量 |
| [get_trigger_list_actor_variable_all_unit_name_pool](#get_trigger_list_actor_variable_all_unit_name_pool) | 获取触发器UNIT_NAME_POOL 组变量数组 |
| [get_trigger_variable_unit_write_attribute](#get_trigger_variable_unit_write_attribute) | 获取全局触发器UNIT_WRITE_ATTRIBUTE非数组变量 |
| [get_trigger_actor_variable_unit_write_attribute](#get_trigger_actor_variable_unit_write_attribute) | 获取触发器UNIT_WRITE_ATTRIBUTE非数组 组变量 |
| [get_trigger_list_variable_unit_write_attribute](#get_trigger_list_variable_unit_write_attribute) | 获取全局触发器UNIT_WRITE_ATTRIBUTE数组变量子项 |
| [get_trigger_list_actor_variable_unit_write_attribute](#get_trigger_list_actor_variable_unit_write_attribute) | 获取触发器UNIT_WRITE_ATTRIBUTE数组 组变量子项 |
| [get_trigger_list_variable_all_unit_write_attribute](#get_trigger_list_variable_all_unit_write_attribute) | 获取全局触发器UNIT_WRITE_ATTRIBUTE数组变量 |
| [get_trigger_list_actor_variable_all_unit_write_attribute](#get_trigger_list_actor_variable_all_unit_write_attribute) | 获取触发器UNIT_WRITE_ATTRIBUTE 组变量数组 |
| [get_trigger_variable_attr_element](#get_trigger_variable_attr_element) | 获取全局触发器ATTR_ELEMENT非数组变量 |
| [get_trigger_actor_variable_attr_element](#get_trigger_actor_variable_attr_element) | 获取触发器ATTR_ELEMENT非数组 组变量 |
| [get_trigger_list_variable_attr_element](#get_trigger_list_variable_attr_element) | 获取全局触发器ATTR_ELEMENT数组变量子项 |
| [get_trigger_list_actor_variable_attr_element](#get_trigger_list_actor_variable_attr_element) | 获取触发器ATTR_ELEMENT数组 组变量子项 |
| [get_trigger_list_variable_all_attr_element](#get_trigger_list_variable_all_attr_element) | 获取全局触发器ATTR_ELEMENT数组变量 |
| [get_trigger_list_actor_variable_all_attr_element](#get_trigger_list_actor_variable_all_attr_element) | 获取触发器ATTR_ELEMENT 组变量数组 |
| [get_trigger_variable_attr_element_read](#get_trigger_variable_attr_element_read) | 获取全局触发器ATTR_ELEMENT_READ非数组变量 |
| [get_trigger_actor_variable_attr_element_read](#get_trigger_actor_variable_attr_element_read) | 获取触发器ATTR_ELEMENT_READ非数组 组变量 |
| [get_trigger_list_variable_attr_element_read](#get_trigger_list_variable_attr_element_read) | 获取全局触发器ATTR_ELEMENT_READ数组变量子项 |
| [get_trigger_list_actor_variable_attr_element_read](#get_trigger_list_actor_variable_attr_element_read) | 获取触发器ATTR_ELEMENT_READ数组 组变量子项 |
| [get_trigger_list_variable_all_attr_element_read](#get_trigger_list_variable_all_attr_element_read) | 获取全局触发器ATTR_ELEMENT_READ数组变量 |
| [get_trigger_list_actor_variable_all_attr_element_read](#get_trigger_list_actor_variable_all_attr_element_read) | 获取触发器ATTR_ELEMENT_READ 组变量数组 |
| [get_trigger_variable_mover_entity](#get_trigger_variable_mover_entity) | 获取全局触发器MOVER_ENTITY非数组变量 |
| [get_trigger_actor_variable_mover_entity](#get_trigger_actor_variable_mover_entity) | 获取触发器MOVER_ENTITY非数组 组变量 |
| [get_trigger_list_variable_mover_entity](#get_trigger_list_variable_mover_entity) | 获取全局触发器MOVER_ENTITY数组变量子项 |
| [get_trigger_list_actor_variable_mover_entity](#get_trigger_list_actor_variable_mover_entity) | 获取触发器MOVER_ENTITY数组 组变量子项 |
| [get_trigger_list_variable_all_mover_entity](#get_trigger_list_variable_all_mover_entity) | 获取全局触发器MOVER_ENTITY数组变量 |
| [get_trigger_list_actor_variable_all_mover_entity](#get_trigger_list_actor_variable_all_mover_entity) | 获取触发器MOVER_ENTITY 组变量数组 |
| [get_trigger_variable_image_quality](#get_trigger_variable_image_quality) | 获取全局触发器IMAGE_QUALITY非数组变量 |
| [get_trigger_actor_variable_image_quality](#get_trigger_actor_variable_image_quality) | 获取触发器IMAGE_QUALITY非数组 组变量 |
| [get_trigger_list_variable_image_quality](#get_trigger_list_variable_image_quality) | 获取全局触发器IMAGE_QUALITY数组变量子项 |
| [get_trigger_list_actor_variable_image_quality](#get_trigger_list_actor_variable_image_quality) | 获取触发器IMAGE_QUALITY数组 组变量子项 |
| [get_trigger_list_variable_all_image_quality](#get_trigger_list_variable_all_image_quality) | 获取全局触发器IMAGE_QUALITY数组变量 |
| [get_trigger_list_actor_variable_all_image_quality](#get_trigger_list_actor_variable_all_image_quality) | 获取触发器IMAGE_QUALITY 组变量数组 |
| [get_trigger_variable_window_type_setting](#get_trigger_variable_window_type_setting) | 获取全局触发器WINDOW_TYPE_SETTING非数组变量 |
| [get_trigger_actor_variable_window_type_setting](#get_trigger_actor_variable_window_type_setting) | 获取触发器WINDOW_TYPE_SETTING非数组 组变量 |
| [get_trigger_list_variable_window_type_setting](#get_trigger_list_variable_window_type_setting) | 获取全局触发器WINDOW_TYPE_SETTING数组变量子项 |
| [get_trigger_list_actor_variable_window_type_setting](#get_trigger_list_actor_variable_window_type_setting) | 获取触发器WINDOW_TYPE_SETTING数组 组变量子项 |
| [get_trigger_list_variable_all_window_type_setting](#get_trigger_list_variable_all_window_type_setting) | 获取全局触发器WINDOW_TYPE_SETTING数组变量 |
| [get_trigger_list_actor_variable_all_window_type_setting](#get_trigger_list_actor_variable_all_window_type_setting) | 获取触发器WINDOW_TYPE_SETTING 组变量数组 |
| [get_trigger_variable_damage_attack_type](#get_trigger_variable_damage_attack_type) | 获取全局触发器DAMAGE_ATTACK_TYPE非数组变量 |
| [get_trigger_actor_variable_damage_attack_type](#get_trigger_actor_variable_damage_attack_type) | 获取触发器DAMAGE_ATTACK_TYPE非数组 组变量 |
| [get_trigger_list_variable_damage_attack_type](#get_trigger_list_variable_damage_attack_type) | 获取全局触发器DAMAGE_ATTACK_TYPE数组变量子项 |
| [get_trigger_list_actor_variable_damage_attack_type](#get_trigger_list_actor_variable_damage_attack_type) | 获取触发器DAMAGE_ATTACK_TYPE数组 组变量子项 |
| [get_trigger_list_variable_all_damage_attack_type](#get_trigger_list_variable_all_damage_attack_type) | 获取全局触发器DAMAGE_ATTACK_TYPE数组变量 |
| [get_trigger_list_actor_variable_all_damage_attack_type](#get_trigger_list_actor_variable_all_damage_attack_type) | 获取触发器DAMAGE_ATTACK_TYPE 组变量数组 |
| [get_trigger_variable_damage_armor_type](#get_trigger_variable_damage_armor_type) | 获取全局触发器DAMAGE_ARMOR_TYPE非数组变量 |
| [get_trigger_actor_variable_damage_armor_type](#get_trigger_actor_variable_damage_armor_type) | 获取触发器DAMAGE_ARMOR_TYPE非数组 组变量 |
| [get_trigger_list_variable_damage_armor_type](#get_trigger_list_variable_damage_armor_type) | 获取全局触发器DAMAGE_ARMOR_TYPE数组变量子项 |
| [get_trigger_list_actor_variable_damage_armor_type](#get_trigger_list_actor_variable_damage_armor_type) | 获取触发器DAMAGE_ARMOR_TYPE数组 组变量子项 |
| [get_trigger_list_variable_all_damage_armor_type](#get_trigger_list_variable_all_damage_armor_type) | 获取全局触发器DAMAGE_ARMOR_TYPE数组变量 |
| [get_trigger_list_actor_variable_all_damage_armor_type](#get_trigger_list_actor_variable_all_damage_armor_type) | 获取触发器DAMAGE_ARMOR_TYPE 组变量数组 |
| [get_trigger_variable_item_entity](#get_trigger_variable_item_entity) | 获取全局触发器ITEM_ENTITY非数组变量 |
| [get_trigger_actor_variable_item_entity](#get_trigger_actor_variable_item_entity) | 获取触发器ITEM_ENTITY非数组 组变量 |
| [get_trigger_list_variable_item_entity](#get_trigger_list_variable_item_entity) | 获取全局触发器ITEM_ENTITY数组变量子项 |
| [get_trigger_list_actor_variable_item_entity](#get_trigger_list_actor_variable_item_entity) | 获取触发器ITEM_ENTITY数组 组变量子项 |
| [get_trigger_list_variable_all_item_entity](#get_trigger_list_variable_all_item_entity) | 获取全局触发器ITEM_ENTITY数组变量 |
| [get_trigger_list_actor_variable_all_item_entity](#get_trigger_list_actor_variable_all_item_entity) | 获取触发器ITEM_ENTITY 组变量数组 |
| [get_trigger_variable_item_group](#get_trigger_variable_item_group) | 获取全局触发器ITEM_GROUP非数组变量 |
| [get_trigger_actor_variable_item_group](#get_trigger_actor_variable_item_group) | 获取触发器ITEM_GROUP非数组 组变量 |
| [get_trigger_list_variable_item_group](#get_trigger_list_variable_item_group) | 获取全局触发器ITEM_GROUP数组变量子项 |
| [get_trigger_list_actor_variable_item_group](#get_trigger_list_actor_variable_item_group) | 获取触发器ITEM_GROUP数组 组变量子项 |
| [get_trigger_list_variable_all_item_group](#get_trigger_list_variable_all_item_group) | 获取全局触发器ITEM_GROUP数组变量 |
| [get_trigger_list_actor_variable_all_item_group](#get_trigger_list_actor_variable_all_item_group) | 获取触发器ITEM_GROUP 组变量数组 |
| [get_trigger_variable_item_name](#get_trigger_variable_item_name) | 获取全局触发器ITEM_NAME非数组变量 |
| [get_trigger_actor_variable_item_name](#get_trigger_actor_variable_item_name) | 获取触发器ITEM_NAME非数组 组变量 |
| [get_trigger_list_variable_item_name](#get_trigger_list_variable_item_name) | 获取全局触发器ITEM_NAME数组变量子项 |
| [get_trigger_list_actor_variable_item_name](#get_trigger_list_actor_variable_item_name) | 获取触发器ITEM_NAME数组 组变量子项 |
| [get_trigger_list_variable_all_item_name](#get_trigger_list_variable_all_item_name) | 获取全局触发器ITEM_NAME数组变量 |
| [get_trigger_list_actor_variable_all_item_name](#get_trigger_list_actor_variable_all_item_name) | 获取触发器ITEM_NAME 组变量数组 |
| [get_trigger_variable_ability](#get_trigger_variable_ability) | 获取全局触发器ABILITY非数组变量 |
| [get_trigger_actor_variable_ability](#get_trigger_actor_variable_ability) | 获取触发器ABILITY非数组 组变量 |
| [get_trigger_list_variable_ability](#get_trigger_list_variable_ability) | 获取全局触发器ABILITY数组变量子项 |
| [get_trigger_list_actor_variable_ability](#get_trigger_list_actor_variable_ability) | 获取触发器ABILITY数组 组变量子项 |
| [get_trigger_list_variable_all_ability](#get_trigger_list_variable_all_ability) | 获取全局触发器ABILITY数组变量 |
| [get_trigger_list_actor_variable_all_ability](#get_trigger_list_actor_variable_all_ability) | 获取触发器ABILITY 组变量数组 |
| [get_trigger_variable_ability_type](#get_trigger_variable_ability_type) | 获取全局触发器ABILITY_TYPE非数组变量 |
| [get_trigger_actor_variable_ability_type](#get_trigger_actor_variable_ability_type) | 获取触发器ABILITY_TYPE非数组 组变量 |
| [get_trigger_list_variable_ability_type](#get_trigger_list_variable_ability_type) | 获取全局触发器ABILITY_TYPE数组变量子项 |
| [get_trigger_list_actor_variable_ability_type](#get_trigger_list_actor_variable_ability_type) | 获取触发器ABILITY_TYPE数组 组变量子项 |
| [get_trigger_list_variable_all_ability_type](#get_trigger_list_variable_all_ability_type) | 获取全局触发器ABILITY_TYPE数组变量 |
| [get_trigger_list_actor_variable_all_ability_type](#get_trigger_list_actor_variable_all_ability_type) | 获取触发器ABILITY_TYPE 组变量数组 |
| [get_trigger_variable_ability_cast_type](#get_trigger_variable_ability_cast_type) | 获取全局触发器ABILITY_CAST_TYPE非数组变量 |
| [get_trigger_actor_variable_ability_cast_type](#get_trigger_actor_variable_ability_cast_type) | 获取触发器ABILITY_CAST_TYPE非数组 组变量 |
| [get_trigger_list_variable_ability_cast_type](#get_trigger_list_variable_ability_cast_type) | 获取全局触发器ABILITY_CAST_TYPE数组变量子项 |
| [get_trigger_list_actor_variable_ability_cast_type](#get_trigger_list_actor_variable_ability_cast_type) | 获取触发器ABILITY_CAST_TYPE数组 组变量子项 |
| [get_trigger_list_variable_all_ability_cast_type](#get_trigger_list_variable_all_ability_cast_type) | 获取全局触发器ABILITY_CAST_TYPE数组变量 |
| [get_trigger_list_actor_variable_all_ability_cast_type](#get_trigger_list_actor_variable_all_ability_cast_type) | 获取触发器ABILITY_CAST_TYPE 组变量数组 |
| [get_trigger_variable_ability_name](#get_trigger_variable_ability_name) | 获取全局触发器ABILITY_NAME非数组变量 |
| [get_trigger_actor_variable_ability_name](#get_trigger_actor_variable_ability_name) | 获取触发器ABILITY_NAME非数组 组变量 |
| [get_trigger_list_variable_ability_name](#get_trigger_list_variable_ability_name) | 获取全局触发器ABILITY_NAME数组变量子项 |
| [get_trigger_list_actor_variable_ability_name](#get_trigger_list_actor_variable_ability_name) | 获取触发器ABILITY_NAME数组 组变量子项 |
| [get_trigger_list_variable_all_ability_name](#get_trigger_list_variable_all_ability_name) | 获取全局触发器ABILITY_NAME数组变量 |
| [get_trigger_list_actor_variable_all_ability_name](#get_trigger_list_actor_variable_all_ability_name) | 获取触发器ABILITY_NAME 组变量数组 |
| [get_trigger_variable_modifier_entity](#get_trigger_variable_modifier_entity) | 获取全局触发器MODIFIER_ENTITY非数组变量 |
| [get_trigger_actor_variable_modifier_entity](#get_trigger_actor_variable_modifier_entity) | 获取触发器MODIFIER_ENTITY非数组 组变量 |
| [get_trigger_list_variable_modifier_entity](#get_trigger_list_variable_modifier_entity) | 获取全局触发器MODIFIER_ENTITY数组变量子项 |
| [get_trigger_list_actor_variable_modifier_entity](#get_trigger_list_actor_variable_modifier_entity) | 获取触发器MODIFIER_ENTITY数组 组变量子项 |
| [get_trigger_list_variable_all_modifier_entity](#get_trigger_list_variable_all_modifier_entity) | 获取全局触发器MODIFIER_ENTITY数组变量 |
| [get_trigger_list_actor_variable_all_modifier_entity](#get_trigger_list_actor_variable_all_modifier_entity) | 获取触发器MODIFIER_ENTITY 组变量数组 |
| [get_trigger_variable_modifier](#get_trigger_variable_modifier) | 获取全局触发器MODIFIER非数组变量 |
| [get_trigger_actor_variable_modifier](#get_trigger_actor_variable_modifier) | 获取触发器MODIFIER非数组 组变量 |
| [get_trigger_list_variable_modifier](#get_trigger_list_variable_modifier) | 获取全局触发器MODIFIER数组变量子项 |
| [get_trigger_list_actor_variable_modifier](#get_trigger_list_actor_variable_modifier) | 获取触发器MODIFIER数组 组变量子项 |
| [get_trigger_list_variable_all_modifier](#get_trigger_list_variable_all_modifier) | 获取全局触发器MODIFIER数组变量 |
| [get_trigger_list_actor_variable_all_modifier](#get_trigger_list_actor_variable_all_modifier) | 获取触发器MODIFIER 组变量数组 |
| [get_trigger_variable_projectile](#get_trigger_variable_projectile) | 获取全局触发器PROJECTILE非数组变量 |
| [get_trigger_actor_variable_projectile](#get_trigger_actor_variable_projectile) | 获取触发器PROJECTILE非数组 组变量 |
| [get_trigger_list_variable_projectile](#get_trigger_list_variable_projectile) | 获取全局触发器PROJECTILE数组变量子项 |
| [get_trigger_list_actor_variable_projectile](#get_trigger_list_actor_variable_projectile) | 获取触发器PROJECTILE数组 组变量子项 |
| [get_trigger_list_variable_all_projectile](#get_trigger_list_variable_all_projectile) | 获取全局触发器PROJECTILE数组变量 |
| [get_trigger_list_actor_variable_all_projectile](#get_trigger_list_actor_variable_all_projectile) | 获取触发器PROJECTILE 组变量数组 |
| [get_trigger_variable_projectile_entity](#get_trigger_variable_projectile_entity) | 获取全局触发器PROJECTILE_ENTITY非数组变量 |
| [get_trigger_actor_variable_projectile_entity](#get_trigger_actor_variable_projectile_entity) | 获取触发器PROJECTILE_ENTITY非数组 组变量 |
| [get_trigger_list_variable_projectile_entity](#get_trigger_list_variable_projectile_entity) | 获取全局触发器PROJECTILE_ENTITY数组变量子项 |
| [get_trigger_list_actor_variable_projectile_entity](#get_trigger_list_actor_variable_projectile_entity) | 获取触发器PROJECTILE_ENTITY数组 组变量子项 |
| [get_trigger_list_variable_all_projectile_entity](#get_trigger_list_variable_all_projectile_entity) | 获取全局触发器PROJECTILE_ENTITY数组变量 |
| [get_trigger_list_actor_variable_all_projectile_entity](#get_trigger_list_actor_variable_all_projectile_entity) | 获取触发器PROJECTILE_ENTITY 组变量数组 |
| [get_trigger_variable_projectile_group](#get_trigger_variable_projectile_group) | 获取全局触发器PROJECTILE_GROUP非数组变量 |
| [get_trigger_actor_variable_projectile_group](#get_trigger_actor_variable_projectile_group) | 获取触发器PROJECTILE_GROUP非数组 组变量 |
| [get_trigger_list_variable_projectile_group](#get_trigger_list_variable_projectile_group) | 获取全局触发器PROJECTILE_GROUP数组变量子项 |
| [get_trigger_list_actor_variable_projectile_group](#get_trigger_list_actor_variable_projectile_group) | 获取触发器PROJECTILE_GROUP数组 组变量子项 |
| [get_trigger_list_variable_all_projectile_group](#get_trigger_list_variable_all_projectile_group) | 获取全局触发器PROJECTILE_GROUP数组变量 |
| [get_trigger_list_actor_variable_all_projectile_group](#get_trigger_list_actor_variable_all_projectile_group) | 获取触发器PROJECTILE_GROUP 组变量数组 |
| [get_trigger_variable_destructible_entity](#get_trigger_variable_destructible_entity) | 获取全局触发器DESTRUCTIBLE_ENTITY非数组变量 |
| [get_trigger_actor_variable_destructible_entity](#get_trigger_actor_variable_destructible_entity) | 获取触发器DESTRUCTIBLE_ENTITY非数组 组变量 |
| [get_trigger_list_variable_destructible_entity](#get_trigger_list_variable_destructible_entity) | 获取全局触发器DESTRUCTIBLE_ENTITY数组变量子项 |
| [get_trigger_list_actor_variable_destructible_entity](#get_trigger_list_actor_variable_destructible_entity) | 获取触发器DESTRUCTIBLE_ENTITY数组 组变量子项 |
| [get_trigger_list_variable_all_destructible_entity](#get_trigger_list_variable_all_destructible_entity) | 获取全局触发器DESTRUCTIBLE_ENTITY数组变量 |
| [get_trigger_list_actor_variable_all_destructible_entity](#get_trigger_list_actor_variable_all_destructible_entity) | 获取触发器DESTRUCTIBLE_ENTITY 组变量数组 |
| [get_trigger_variable_destructible_name](#get_trigger_variable_destructible_name) | 获取全局触发器DESTRUCTIBLE_NAME非数组变量 |
| [get_trigger_actor_variable_destructible_name](#get_trigger_actor_variable_destructible_name) | 获取触发器DESTRUCTIBLE_NAME非数组 组变量 |
| [get_trigger_list_variable_destructible_name](#get_trigger_list_variable_destructible_name) | 获取全局触发器DESTRUCTIBLE_NAME数组变量子项 |
| [get_trigger_list_actor_variable_destructible_name](#get_trigger_list_actor_variable_destructible_name) | 获取触发器DESTRUCTIBLE_NAME数组 组变量子项 |
| [get_trigger_list_variable_all_destructible_name](#get_trigger_list_variable_all_destructible_name) | 获取全局触发器DESTRUCTIBLE_NAME数组变量 |
| [get_trigger_list_actor_variable_all_destructible_name](#get_trigger_list_actor_variable_all_destructible_name) | 获取触发器DESTRUCTIBLE_NAME 组变量数组 |
| [get_trigger_variable_sound_entity](#get_trigger_variable_sound_entity) | 获取全局触发器SOUND_ENTITY非数组变量 |
| [get_trigger_actor_variable_sound_entity](#get_trigger_actor_variable_sound_entity) | 获取触发器SOUND_ENTITY非数组 组变量 |
| [get_trigger_list_variable_sound_entity](#get_trigger_list_variable_sound_entity) | 获取全局触发器SOUND_ENTITY数组变量子项 |
| [get_trigger_list_actor_variable_sound_entity](#get_trigger_list_actor_variable_sound_entity) | 获取触发器SOUND_ENTITY数组 组变量子项 |
| [get_trigger_list_variable_all_sound_entity](#get_trigger_list_variable_all_sound_entity) | 获取全局触发器SOUND_ENTITY数组变量 |
| [get_trigger_list_actor_variable_all_sound_entity](#get_trigger_list_actor_variable_all_sound_entity) | 获取触发器SOUND_ENTITY 组变量数组 |
| [get_trigger_variable_audio_key](#get_trigger_variable_audio_key) | 获取全局触发器AUDIO_KEY非数组变量 |
| [get_trigger_actor_variable_audio_key](#get_trigger_actor_variable_audio_key) | 获取触发器AUDIO_KEY非数组 组变量 |
| [get_trigger_list_variable_audio_key](#get_trigger_list_variable_audio_key) | 获取全局触发器AUDIO_KEY数组变量子项 |
| [get_trigger_list_actor_variable_audio_key](#get_trigger_list_actor_variable_audio_key) | 获取触发器AUDIO_KEY数组 组变量子项 |
| [get_trigger_list_variable_all_audio_key](#get_trigger_list_variable_all_audio_key) | 获取全局触发器AUDIO_KEY数组变量 |
| [get_trigger_list_actor_variable_all_audio_key](#get_trigger_list_actor_variable_all_audio_key) | 获取触发器AUDIO_KEY 组变量数组 |
| [get_trigger_variable_game_mode](#get_trigger_variable_game_mode) | 获取全局触发器GAME_MODE非数组变量 |
| [get_trigger_actor_variable_game_mode](#get_trigger_actor_variable_game_mode) | 获取触发器GAME_MODE非数组 组变量 |
| [get_trigger_list_variable_game_mode](#get_trigger_list_variable_game_mode) | 获取全局触发器GAME_MODE数组变量子项 |
| [get_trigger_list_actor_variable_game_mode](#get_trigger_list_actor_variable_game_mode) | 获取触发器GAME_MODE数组 组变量子项 |
| [get_trigger_list_variable_all_game_mode](#get_trigger_list_variable_all_game_mode) | 获取全局触发器GAME_MODE数组变量 |
| [get_trigger_list_actor_variable_all_game_mode](#get_trigger_list_actor_variable_all_game_mode) | 获取触发器GAME_MODE 组变量数组 |
| [get_trigger_variable_player](#get_trigger_variable_player) | 获取全局触发器PLAYER非数组变量 |
| [get_trigger_actor_variable_player](#get_trigger_actor_variable_player) | 获取触发器PLAYER非数组 组变量 |
| [get_trigger_list_variable_player](#get_trigger_list_variable_player) | 获取全局触发器PLAYER数组变量子项 |
| [get_trigger_list_actor_variable_player](#get_trigger_list_actor_variable_player) | 获取触发器PLAYER数组 组变量子项 |
| [get_trigger_list_variable_all_player](#get_trigger_list_variable_all_player) | 获取全局触发器PLAYER数组变量 |
| [get_trigger_list_actor_variable_all_player](#get_trigger_list_actor_variable_all_player) | 获取触发器PLAYER 组变量数组 |
| [get_trigger_variable_player_group](#get_trigger_variable_player_group) | 获取全局触发器PLAYER_GROUP非数组变量 |
| [get_trigger_actor_variable_player_group](#get_trigger_actor_variable_player_group) | 获取触发器PLAYER_GROUP非数组 组变量 |
| [get_trigger_list_variable_player_group](#get_trigger_list_variable_player_group) | 获取全局触发器PLAYER_GROUP数组变量子项 |
| [get_trigger_list_actor_variable_player_group](#get_trigger_list_actor_variable_player_group) | 获取触发器PLAYER_GROUP数组 组变量子项 |
| [get_trigger_list_variable_all_player_group](#get_trigger_list_variable_all_player_group) | 获取全局触发器PLAYER_GROUP数组变量 |
| [get_trigger_list_actor_variable_all_player_group](#get_trigger_list_actor_variable_all_player_group) | 获取触发器PLAYER_GROUP 组变量数组 |
| [get_trigger_variable_role_res_key](#get_trigger_variable_role_res_key) | 获取全局触发器ROLE_RES_KEY非数组变量 |
| [get_trigger_actor_variable_role_res_key](#get_trigger_actor_variable_role_res_key) | 获取触发器ROLE_RES_KEY非数组 组变量 |
| [get_trigger_list_variable_role_res_key](#get_trigger_list_variable_role_res_key) | 获取全局触发器ROLE_RES_KEY数组变量子项 |
| [get_trigger_list_actor_variable_role_res_key](#get_trigger_list_actor_variable_role_res_key) | 获取触发器ROLE_RES_KEY数组 组变量子项 |
| [get_trigger_list_variable_all_role_res_key](#get_trigger_list_variable_all_role_res_key) | 获取全局触发器ROLE_RES_KEY数组变量 |
| [get_trigger_list_actor_variable_all_role_res_key](#get_trigger_list_actor_variable_all_role_res_key) | 获取触发器ROLE_RES_KEY 组变量数组 |
| [get_trigger_variable_role_status](#get_trigger_variable_role_status) | 获取全局触发器ROLE_STATUS非数组变量 |
| [get_trigger_actor_variable_role_status](#get_trigger_actor_variable_role_status) | 获取触发器ROLE_STATUS非数组 组变量 |
| [get_trigger_list_variable_role_status](#get_trigger_list_variable_role_status) | 获取全局触发器ROLE_STATUS数组变量子项 |
| [get_trigger_list_actor_variable_role_status](#get_trigger_list_actor_variable_role_status) | 获取触发器ROLE_STATUS数组 组变量子项 |
| [get_trigger_list_variable_all_role_status](#get_trigger_list_variable_all_role_status) | 获取全局触发器ROLE_STATUS数组变量 |
| [get_trigger_list_actor_variable_all_role_status](#get_trigger_list_actor_variable_all_role_status) | 获取触发器ROLE_STATUS 组变量数组 |
| [get_trigger_variable_role_type](#get_trigger_variable_role_type) | 获取全局触发器ROLE_TYPE非数组变量 |
| [get_trigger_actor_variable_role_type](#get_trigger_actor_variable_role_type) | 获取触发器ROLE_TYPE非数组 组变量 |
| [get_trigger_list_variable_role_type](#get_trigger_list_variable_role_type) | 获取全局触发器ROLE_TYPE数组变量子项 |
| [get_trigger_list_actor_variable_role_type](#get_trigger_list_actor_variable_role_type) | 获取触发器ROLE_TYPE数组 组变量子项 |
| [get_trigger_list_variable_all_role_type](#get_trigger_list_variable_all_role_type) | 获取全局触发器ROLE_TYPE数组变量 |
| [get_trigger_list_actor_variable_all_role_type](#get_trigger_list_actor_variable_all_role_type) | 获取触发器ROLE_TYPE 组变量数组 |
| [get_trigger_variable_team](#get_trigger_variable_team) | 获取全局触发器TEAM非数组变量 |
| [get_trigger_actor_variable_team](#get_trigger_actor_variable_team) | 获取触发器TEAM非数组 组变量 |
| [get_trigger_list_variable_team](#get_trigger_list_variable_team) | 获取全局触发器TEAM数组变量子项 |
| [get_trigger_list_actor_variable_team](#get_trigger_list_actor_variable_team) | 获取触发器TEAM数组 组变量子项 |
| [get_trigger_list_variable_all_team](#get_trigger_list_variable_all_team) | 获取全局触发器TEAM数组变量 |
| [get_trigger_list_actor_variable_all_team](#get_trigger_list_actor_variable_all_team) | 获取触发器TEAM 组变量数组 |
| [get_trigger_variable_point](#get_trigger_variable_point) | 获取全局触发器POINT非数组变量 |
| [get_trigger_actor_variable_point](#get_trigger_actor_variable_point) | 获取触发器POINT非数组 组变量 |
| [get_trigger_list_variable_point](#get_trigger_list_variable_point) | 获取全局触发器POINT数组变量子项 |
| [get_trigger_list_actor_variable_point](#get_trigger_list_actor_variable_point) | 获取触发器POINT数组 组变量子项 |
| [get_trigger_list_variable_all_point](#get_trigger_list_variable_all_point) | 获取全局触发器POINT数组变量 |
| [get_trigger_list_actor_variable_all_point](#get_trigger_list_actor_variable_all_point) | 获取触发器POINT 组变量数组 |
| [get_trigger_variable_vector3](#get_trigger_variable_vector3) | 获取全局触发器VECTOR3非数组变量 |
| [get_trigger_actor_variable_vector3](#get_trigger_actor_variable_vector3) | 获取触发器VECTOR3非数组 组变量 |
| [get_trigger_list_variable_vector3](#get_trigger_list_variable_vector3) | 获取全局触发器VECTOR3数组变量子项 |
| [get_trigger_list_actor_variable_vector3](#get_trigger_list_actor_variable_vector3) | 获取触发器VECTOR3数组 组变量子项 |
| [get_trigger_list_variable_all_vector3](#get_trigger_list_variable_all_vector3) | 获取全局触发器VECTOR3数组变量 |
| [get_trigger_list_actor_variable_all_vector3](#get_trigger_list_actor_variable_all_vector3) | 获取触发器VECTOR3 组变量数组 |
| [get_trigger_variable_rotation](#get_trigger_variable_rotation) | 获取全局触发器ROTATION非数组变量 |
| [get_trigger_actor_variable_rotation](#get_trigger_actor_variable_rotation) | 获取触发器ROTATION非数组 组变量 |
| [get_trigger_list_variable_rotation](#get_trigger_list_variable_rotation) | 获取全局触发器ROTATION数组变量子项 |
| [get_trigger_list_actor_variable_rotation](#get_trigger_list_actor_variable_rotation) | 获取触发器ROTATION数组 组变量子项 |
| [get_trigger_list_variable_all_rotation](#get_trigger_list_variable_all_rotation) | 获取全局触发器ROTATION数组变量 |
| [get_trigger_list_actor_variable_all_rotation](#get_trigger_list_actor_variable_all_rotation) | 获取触发器ROTATION 组变量数组 |
| [get_trigger_variable_point_list](#get_trigger_variable_point_list) | 获取全局触发器POINT_LIST非数组变量 |
| [get_trigger_actor_variable_point_list](#get_trigger_actor_variable_point_list) | 获取触发器POINT_LIST非数组 组变量 |
| [get_trigger_list_variable_point_list](#get_trigger_list_variable_point_list) | 获取全局触发器POINT_LIST数组变量子项 |
| [get_trigger_list_actor_variable_point_list](#get_trigger_list_actor_variable_point_list) | 获取触发器POINT_LIST数组 组变量子项 |
| [get_trigger_list_variable_all_point_list](#get_trigger_list_variable_all_point_list) | 获取全局触发器POINT_LIST数组变量 |
| [get_trigger_list_actor_variable_all_point_list](#get_trigger_list_actor_variable_all_point_list) | 获取触发器POINT_LIST 组变量数组 |
| [get_trigger_variable_road_group](#get_trigger_variable_road_group) | 获取全局触发器ROAD_GROUP非数组变量 |
| [get_trigger_actor_variable_road_group](#get_trigger_actor_variable_road_group) | 获取触发器ROAD_GROUP非数组 组变量 |
| [get_trigger_list_variable_road_group](#get_trigger_list_variable_road_group) | 获取全局触发器ROAD_GROUP数组变量子项 |
| [get_trigger_list_actor_variable_road_group](#get_trigger_list_actor_variable_road_group) | 获取触发器ROAD_GROUP数组 组变量子项 |
| [get_trigger_list_variable_all_road_group](#get_trigger_list_variable_all_road_group) | 获取全局触发器ROAD_GROUP数组变量 |
| [get_trigger_list_actor_variable_all_road_group](#get_trigger_list_actor_variable_all_road_group) | 获取触发器ROAD_GROUP 组变量数组 |
| [get_trigger_variable_rectangle](#get_trigger_variable_rectangle) | 获取全局触发器RECTANGLE非数组变量 |
| [get_trigger_actor_variable_rectangle](#get_trigger_actor_variable_rectangle) | 获取触发器RECTANGLE非数组 组变量 |
| [get_trigger_list_variable_rectangle](#get_trigger_list_variable_rectangle) | 获取全局触发器RECTANGLE数组变量子项 |
| [get_trigger_list_actor_variable_rectangle](#get_trigger_list_actor_variable_rectangle) | 获取触发器RECTANGLE数组 组变量子项 |
| [get_trigger_list_variable_all_rectangle](#get_trigger_list_variable_all_rectangle) | 获取全局触发器RECTANGLE数组变量 |
| [get_trigger_list_actor_variable_all_rectangle](#get_trigger_list_actor_variable_all_rectangle) | 获取触发器RECTANGLE 组变量数组 |
| [get_trigger_variable_round_area](#get_trigger_variable_round_area) | 获取全局触发器ROUND_AREA非数组变量 |
| [get_trigger_actor_variable_round_area](#get_trigger_actor_variable_round_area) | 获取触发器ROUND_AREA非数组 组变量 |
| [get_trigger_list_variable_round_area](#get_trigger_list_variable_round_area) | 获取全局触发器ROUND_AREA数组变量子项 |
| [get_trigger_list_actor_variable_round_area](#get_trigger_list_actor_variable_round_area) | 获取触发器ROUND_AREA数组 组变量子项 |
| [get_trigger_list_variable_all_round_area](#get_trigger_list_variable_all_round_area) | 获取全局触发器ROUND_AREA数组变量 |
| [get_trigger_list_actor_variable_all_round_area](#get_trigger_list_actor_variable_all_round_area) | 获取触发器ROUND_AREA 组变量数组 |
| [get_trigger_variable_polygon](#get_trigger_variable_polygon) | 获取全局触发器POLYGON非数组变量 |
| [get_trigger_actor_variable_polygon](#get_trigger_actor_variable_polygon) | 获取触发器POLYGON非数组 组变量 |
| [get_trigger_list_variable_polygon](#get_trigger_list_variable_polygon) | 获取全局触发器POLYGON数组变量子项 |
| [get_trigger_list_actor_variable_polygon](#get_trigger_list_actor_variable_polygon) | 获取触发器POLYGON数组 组变量子项 |
| [get_trigger_list_variable_all_polygon](#get_trigger_list_variable_all_polygon) | 获取全局触发器POLYGON数组变量 |
| [get_trigger_list_actor_variable_all_polygon](#get_trigger_list_actor_variable_all_polygon) | 获取触发器POLYGON 组变量数组 |
| [get_trigger_variable_camera](#get_trigger_variable_camera) | 获取全局触发器CAMERA非数组变量 |
| [get_trigger_actor_variable_camera](#get_trigger_actor_variable_camera) | 获取触发器CAMERA非数组 组变量 |
| [get_trigger_list_variable_camera](#get_trigger_list_variable_camera) | 获取全局触发器CAMERA数组变量子项 |
| [get_trigger_list_actor_variable_camera](#get_trigger_list_actor_variable_camera) | 获取触发器CAMERA数组 组变量子项 |
| [get_trigger_list_variable_all_camera](#get_trigger_list_variable_all_camera) | 获取全局触发器CAMERA数组变量 |
| [get_trigger_list_actor_variable_all_camera](#get_trigger_list_actor_variable_all_camera) | 获取触发器CAMERA 组变量数组 |
| [get_trigger_variable_camline](#get_trigger_variable_camline) | 获取全局触发器CAMLINE非数组变量 |
| [get_trigger_actor_variable_camline](#get_trigger_actor_variable_camline) | 获取触发器CAMLINE非数组 组变量 |
| [get_trigger_list_variable_camline](#get_trigger_list_variable_camline) | 获取全局触发器CAMLINE数组变量子项 |
| [get_trigger_list_actor_variable_camline](#get_trigger_list_actor_variable_camline) | 获取触发器CAMLINE数组 组变量子项 |
| [get_trigger_list_variable_all_camline](#get_trigger_list_variable_all_camline) | 获取全局触发器CAMLINE数组变量 |
| [get_trigger_list_actor_variable_all_camline](#get_trigger_list_actor_variable_all_camline) | 获取触发器CAMLINE 组变量数组 |
| [get_trigger_variable_point_light](#get_trigger_variable_point_light) | 获取全局触发器POINT_LIGHT非数组变量 |
| [get_trigger_actor_variable_point_light](#get_trigger_actor_variable_point_light) | 获取触发器POINT_LIGHT非数组 组变量 |
| [get_trigger_list_variable_point_light](#get_trigger_list_variable_point_light) | 获取全局触发器POINT_LIGHT数组变量子项 |
| [get_trigger_list_actor_variable_point_light](#get_trigger_list_actor_variable_point_light) | 获取触发器POINT_LIGHT数组 组变量子项 |
| [get_trigger_list_variable_all_point_light](#get_trigger_list_variable_all_point_light) | 获取全局触发器POINT_LIGHT数组变量 |
| [get_trigger_list_actor_variable_all_point_light](#get_trigger_list_actor_variable_all_point_light) | 获取触发器POINT_LIGHT 组变量数组 |
| [get_trigger_variable_spot_light](#get_trigger_variable_spot_light) | 获取全局触发器SPOT_LIGHT非数组变量 |
| [get_trigger_actor_variable_spot_light](#get_trigger_actor_variable_spot_light) | 获取触发器SPOT_LIGHT非数组 组变量 |
| [get_trigger_list_variable_spot_light](#get_trigger_list_variable_spot_light) | 获取全局触发器SPOT_LIGHT数组变量子项 |
| [get_trigger_list_actor_variable_spot_light](#get_trigger_list_actor_variable_spot_light) | 获取触发器SPOT_LIGHT数组 组变量子项 |
| [get_trigger_list_variable_all_spot_light](#get_trigger_list_variable_all_spot_light) | 获取全局触发器SPOT_LIGHT数组变量 |
| [get_trigger_list_actor_variable_all_spot_light](#get_trigger_list_actor_variable_all_spot_light) | 获取触发器SPOT_LIGHT 组变量数组 |
| [get_trigger_variable_fog](#get_trigger_variable_fog) | 获取全局触发器FOG非数组变量 |
| [get_trigger_actor_variable_fog](#get_trigger_actor_variable_fog) | 获取触发器FOG非数组 组变量 |
| [get_trigger_list_variable_fog](#get_trigger_list_variable_fog) | 获取全局触发器FOG数组变量子项 |
| [get_trigger_list_actor_variable_fog](#get_trigger_list_actor_variable_fog) | 获取触发器FOG数组 组变量子项 |
| [get_trigger_list_variable_all_fog](#get_trigger_list_variable_all_fog) | 获取全局触发器FOG数组变量 |
| [get_trigger_list_actor_variable_all_fog](#get_trigger_list_actor_variable_all_fog) | 获取触发器FOG 组变量数组 |
| [get_trigger_variable_model](#get_trigger_variable_model) | 获取全局触发器MODEL非数组变量 |
| [get_trigger_actor_variable_model](#get_trigger_actor_variable_model) | 获取触发器MODEL非数组 组变量 |
| [get_trigger_list_variable_model](#get_trigger_list_variable_model) | 获取全局触发器MODEL数组变量子项 |
| [get_trigger_list_actor_variable_model](#get_trigger_list_actor_variable_model) | 获取触发器MODEL数组 组变量子项 |
| [get_trigger_list_variable_all_model](#get_trigger_list_variable_all_model) | 获取全局触发器MODEL数组变量 |
| [get_trigger_list_actor_variable_all_model](#get_trigger_list_actor_variable_all_model) | 获取触发器MODEL 组变量数组 |
| [get_trigger_variable_sfx_entity](#get_trigger_variable_sfx_entity) | 获取全局触发器SFX_ENTITY非数组变量 |
| [get_trigger_actor_variable_sfx_entity](#get_trigger_actor_variable_sfx_entity) | 获取触发器SFX_ENTITY非数组 组变量 |
| [get_trigger_list_variable_sfx_entity](#get_trigger_list_variable_sfx_entity) | 获取全局触发器SFX_ENTITY数组变量子项 |
| [get_trigger_list_actor_variable_sfx_entity](#get_trigger_list_actor_variable_sfx_entity) | 获取触发器SFX_ENTITY数组 组变量子项 |
| [get_trigger_list_variable_all_sfx_entity](#get_trigger_list_variable_all_sfx_entity) | 获取全局触发器SFX_ENTITY数组变量 |
| [get_trigger_list_actor_variable_all_sfx_entity](#get_trigger_list_actor_variable_all_sfx_entity) | 获取触发器SFX_ENTITY 组变量数组 |
| [get_trigger_variable_sfx_key](#get_trigger_variable_sfx_key) | 获取全局触发器SFX_KEY非数组变量 |
| [get_trigger_actor_variable_sfx_key](#get_trigger_actor_variable_sfx_key) | 获取触发器SFX_KEY非数组 组变量 |
| [get_trigger_list_variable_sfx_key](#get_trigger_list_variable_sfx_key) | 获取全局触发器SFX_KEY数组变量子项 |
| [get_trigger_list_actor_variable_sfx_key](#get_trigger_list_actor_variable_sfx_key) | 获取触发器SFX_KEY数组 组变量子项 |
| [get_trigger_list_variable_all_sfx_key](#get_trigger_list_variable_all_sfx_key) | 获取全局触发器SFX_KEY数组变量 |
| [get_trigger_list_actor_variable_all_sfx_key](#get_trigger_list_actor_variable_all_sfx_key) | 获取触发器SFX_KEY 组变量数组 |
| [get_trigger_variable_link_sfx_entity](#get_trigger_variable_link_sfx_entity) | 获取全局触发器LINK_SFX_ENTITY非数组变量 |
| [get_trigger_actor_variable_link_sfx_entity](#get_trigger_actor_variable_link_sfx_entity) | 获取触发器LINK_SFX_ENTITY非数组 组变量 |
| [get_trigger_list_variable_link_sfx_entity](#get_trigger_list_variable_link_sfx_entity) | 获取全局触发器LINK_SFX_ENTITY数组变量子项 |
| [get_trigger_list_actor_variable_link_sfx_entity](#get_trigger_list_actor_variable_link_sfx_entity) | 获取触发器LINK_SFX_ENTITY数组 组变量子项 |
| [get_trigger_list_variable_all_link_sfx_entity](#get_trigger_list_variable_all_link_sfx_entity) | 获取全局触发器LINK_SFX_ENTITY数组变量 |
| [get_trigger_list_actor_variable_all_link_sfx_entity](#get_trigger_list_actor_variable_all_link_sfx_entity) | 获取触发器LINK_SFX_ENTITY 组变量数组 |
| [get_trigger_variable_link_sfx_key](#get_trigger_variable_link_sfx_key) | 获取全局触发器LINK_SFX_KEY非数组变量 |
| [get_trigger_actor_variable_link_sfx_key](#get_trigger_actor_variable_link_sfx_key) | 获取触发器LINK_SFX_KEY非数组 组变量 |
| [get_trigger_list_variable_link_sfx_key](#get_trigger_list_variable_link_sfx_key) | 获取全局触发器LINK_SFX_KEY数组变量子项 |
| [get_trigger_list_actor_variable_link_sfx_key](#get_trigger_list_actor_variable_link_sfx_key) | 获取触发器LINK_SFX_KEY数组 组变量子项 |
| [get_trigger_list_variable_all_link_sfx_key](#get_trigger_list_variable_all_link_sfx_key) | 获取全局触发器LINK_SFX_KEY数组变量 |
| [get_trigger_list_actor_variable_all_link_sfx_key](#get_trigger_list_actor_variable_all_link_sfx_key) | 获取触发器LINK_SFX_KEY 组变量数组 |
| [get_trigger_variable_cursor_key](#get_trigger_variable_cursor_key) | 获取全局触发器CURSOR_KEY非数组变量 |
| [get_trigger_actor_variable_cursor_key](#get_trigger_actor_variable_cursor_key) | 获取触发器CURSOR_KEY非数组 组变量 |
| [get_trigger_list_variable_cursor_key](#get_trigger_list_variable_cursor_key) | 获取全局触发器CURSOR_KEY数组变量子项 |
| [get_trigger_list_actor_variable_cursor_key](#get_trigger_list_actor_variable_cursor_key) | 获取触发器CURSOR_KEY数组 组变量子项 |
| [get_trigger_list_variable_all_cursor_key](#get_trigger_list_variable_all_cursor_key) | 获取全局触发器CURSOR_KEY数组变量 |
| [get_trigger_list_actor_variable_all_cursor_key](#get_trigger_list_actor_variable_all_cursor_key) | 获取触发器CURSOR_KEY 组变量数组 |
| [get_trigger_variable_image_key](#get_trigger_variable_image_key) | 获取全局触发器IMAGE_KEY非数组变量 |
| [get_trigger_actor_variable_image_key](#get_trigger_actor_variable_image_key) | 获取触发器IMAGE_KEY非数组 组变量 |
| [get_trigger_list_variable_image_key](#get_trigger_list_variable_image_key) | 获取全局触发器IMAGE_KEY数组变量子项 |
| [get_trigger_list_actor_variable_image_key](#get_trigger_list_actor_variable_image_key) | 获取触发器IMAGE_KEY数组 组变量子项 |
| [get_trigger_list_variable_all_image_key](#get_trigger_list_variable_all_image_key) | 获取全局触发器IMAGE_KEY数组变量 |
| [get_trigger_list_actor_variable_all_image_key](#get_trigger_list_actor_variable_all_image_key) | 获取触发器IMAGE_KEY 组变量数组 |
| [get_trigger_variable_angle](#get_trigger_variable_angle) | 获取全局触发器ANGLE非数组变量 |
| [get_trigger_actor_variable_angle](#get_trigger_actor_variable_angle) | 获取触发器ANGLE非数组 组变量 |
| [get_trigger_list_variable_angle](#get_trigger_list_variable_angle) | 获取全局触发器ANGLE数组变量子项 |
| [get_trigger_list_actor_variable_angle](#get_trigger_list_actor_variable_angle) | 获取触发器ANGLE数组 组变量子项 |
| [get_trigger_list_variable_all_angle](#get_trigger_list_variable_all_angle) | 获取全局触发器ANGLE数组变量 |
| [get_trigger_list_actor_variable_all_angle](#get_trigger_list_actor_variable_all_angle) | 获取触发器ANGLE 组变量数组 |
| [get_trigger_variable_texture](#get_trigger_variable_texture) | 获取全局触发器TEXTURE非数组变量 |
| [get_trigger_actor_variable_texture](#get_trigger_actor_variable_texture) | 获取触发器TEXTURE非数组 组变量 |
| [get_trigger_list_variable_texture](#get_trigger_list_variable_texture) | 获取全局触发器TEXTURE数组变量子项 |
| [get_trigger_list_actor_variable_texture](#get_trigger_list_actor_variable_texture) | 获取触发器TEXTURE数组 组变量子项 |
| [get_trigger_list_variable_all_texture](#get_trigger_list_variable_all_texture) | 获取全局触发器TEXTURE数组变量 |
| [get_trigger_list_actor_variable_all_texture](#get_trigger_list_actor_variable_all_texture) | 获取触发器TEXTURE 组变量数组 |
| [get_trigger_variable_sequence](#get_trigger_variable_sequence) | 获取全局触发器SEQUENCE非数组变量 |
| [get_trigger_actor_variable_sequence](#get_trigger_actor_variable_sequence) | 获取触发器SEQUENCE非数组 组变量 |
| [get_trigger_list_variable_sequence](#get_trigger_list_variable_sequence) | 获取全局触发器SEQUENCE数组变量子项 |
| [get_trigger_list_actor_variable_sequence](#get_trigger_list_actor_variable_sequence) | 获取触发器SEQUENCE数组 组变量子项 |
| [get_trigger_list_variable_all_sequence](#get_trigger_list_variable_all_sequence) | 获取全局触发器SEQUENCE数组变量 |
| [get_trigger_list_actor_variable_all_sequence](#get_trigger_list_actor_variable_all_sequence) | 获取触发器SEQUENCE 组变量数组 |
| [get_trigger_variable_physics_object](#get_trigger_variable_physics_object) | 获取全局触发器PHYSICS_OBJECT非数组变量 |
| [get_trigger_actor_variable_physics_object](#get_trigger_actor_variable_physics_object) | 获取触发器PHYSICS_OBJECT非数组 组变量 |
| [get_trigger_list_variable_physics_object](#get_trigger_list_variable_physics_object) | 获取全局触发器PHYSICS_OBJECT数组变量子项 |
| [get_trigger_list_actor_variable_physics_object](#get_trigger_list_actor_variable_physics_object) | 获取触发器PHYSICS_OBJECT数组 组变量子项 |
| [get_trigger_list_variable_all_physics_object](#get_trigger_list_variable_all_physics_object) | 获取全局触发器PHYSICS_OBJECT数组变量 |
| [get_trigger_list_actor_variable_all_physics_object](#get_trigger_list_actor_variable_all_physics_object) | 获取触发器PHYSICS_OBJECT 组变量数组 |
| [get_trigger_variable_physics_entity](#get_trigger_variable_physics_entity) | 获取全局触发器PHYSICS_ENTITY非数组变量 |
| [get_trigger_actor_variable_physics_entity](#get_trigger_actor_variable_physics_entity) | 获取触发器PHYSICS_ENTITY非数组 组变量 |
| [get_trigger_list_variable_physics_entity](#get_trigger_list_variable_physics_entity) | 获取全局触发器PHYSICS_ENTITY数组变量子项 |
| [get_trigger_list_actor_variable_physics_entity](#get_trigger_list_actor_variable_physics_entity) | 获取触发器PHYSICS_ENTITY数组 组变量子项 |
| [get_trigger_list_variable_all_physics_entity](#get_trigger_list_variable_all_physics_entity) | 获取全局触发器PHYSICS_ENTITY数组变量 |
| [get_trigger_list_actor_variable_all_physics_entity](#get_trigger_list_actor_variable_all_physics_entity) | 获取触发器PHYSICS_ENTITY 组变量数组 |
| [get_trigger_variable_physics_object_key](#get_trigger_variable_physics_object_key) | 获取全局触发器PHYSICS_OBJECT_KEY非数组变量 |
| [get_trigger_actor_variable_physics_object_key](#get_trigger_actor_variable_physics_object_key) | 获取触发器PHYSICS_OBJECT_KEY非数组 组变量 |
| [get_trigger_list_variable_physics_object_key](#get_trigger_list_variable_physics_object_key) | 获取全局触发器PHYSICS_OBJECT_KEY数组变量子项 |
| [get_trigger_list_actor_variable_physics_object_key](#get_trigger_list_actor_variable_physics_object_key) | 获取触发器PHYSICS_OBJECT_KEY数组 组变量子项 |
| [get_trigger_list_variable_all_physics_object_key](#get_trigger_list_variable_all_physics_object_key) | 获取全局触发器PHYSICS_OBJECT_KEY数组变量 |
| [get_trigger_list_actor_variable_all_physics_object_key](#get_trigger_list_actor_variable_all_physics_object_key) | 获取触发器PHYSICS_OBJECT_KEY 组变量数组 |
| [get_trigger_variable_physics_entity_key](#get_trigger_variable_physics_entity_key) | 获取全局触发器PHYSICS_ENTITY_KEY非数组变量 |
| [get_trigger_actor_variable_physics_entity_key](#get_trigger_actor_variable_physics_entity_key) | 获取触发器PHYSICS_ENTITY_KEY非数组 组变量 |
| [get_trigger_list_variable_physics_entity_key](#get_trigger_list_variable_physics_entity_key) | 获取全局触发器PHYSICS_ENTITY_KEY数组变量子项 |
| [get_trigger_list_actor_variable_physics_entity_key](#get_trigger_list_actor_variable_physics_entity_key) | 获取触发器PHYSICS_ENTITY_KEY数组 组变量子项 |
| [get_trigger_list_variable_all_physics_entity_key](#get_trigger_list_variable_all_physics_entity_key) | 获取全局触发器PHYSICS_ENTITY_KEY数组变量 |
| [get_trigger_list_actor_variable_all_physics_entity_key](#get_trigger_list_actor_variable_all_physics_entity_key) | 获取触发器PHYSICS_ENTITY_KEY 组变量数组 |
| [get_trigger_variable_rigid_body](#get_trigger_variable_rigid_body) | 获取全局触发器RIGID_BODY非数组变量 |
| [get_trigger_actor_variable_rigid_body](#get_trigger_actor_variable_rigid_body) | 获取触发器RIGID_BODY非数组 组变量 |
| [get_trigger_list_variable_rigid_body](#get_trigger_list_variable_rigid_body) | 获取全局触发器RIGID_BODY数组变量子项 |
| [get_trigger_list_actor_variable_rigid_body](#get_trigger_list_actor_variable_rigid_body) | 获取触发器RIGID_BODY数组 组变量子项 |
| [get_trigger_list_variable_all_rigid_body](#get_trigger_list_variable_all_rigid_body) | 获取全局触发器RIGID_BODY数组变量 |
| [get_trigger_list_actor_variable_all_rigid_body](#get_trigger_list_actor_variable_all_rigid_body) | 获取触发器RIGID_BODY 组变量数组 |
| [get_trigger_variable_rigid_body_group](#get_trigger_variable_rigid_body_group) | 获取全局触发器RIGID_BODY_GROUP非数组变量 |
| [get_trigger_actor_variable_rigid_body_group](#get_trigger_actor_variable_rigid_body_group) | 获取触发器RIGID_BODY_GROUP非数组 组变量 |
| [get_trigger_list_variable_rigid_body_group](#get_trigger_list_variable_rigid_body_group) | 获取全局触发器RIGID_BODY_GROUP数组变量子项 |
| [get_trigger_list_actor_variable_rigid_body_group](#get_trigger_list_actor_variable_rigid_body_group) | 获取触发器RIGID_BODY_GROUP数组 组变量子项 |
| [get_trigger_list_variable_all_rigid_body_group](#get_trigger_list_variable_all_rigid_body_group) | 获取全局触发器RIGID_BODY_GROUP数组变量 |
| [get_trigger_list_actor_variable_all_rigid_body_group](#get_trigger_list_actor_variable_all_rigid_body_group) | 获取触发器RIGID_BODY_GROUP 组变量数组 |
| [get_trigger_variable_collider](#get_trigger_variable_collider) | 获取全局触发器COLLIDER非数组变量 |
| [get_trigger_actor_variable_collider](#get_trigger_actor_variable_collider) | 获取触发器COLLIDER非数组 组变量 |
| [get_trigger_list_variable_collider](#get_trigger_list_variable_collider) | 获取全局触发器COLLIDER数组变量子项 |
| [get_trigger_list_actor_variable_collider](#get_trigger_list_actor_variable_collider) | 获取触发器COLLIDER数组 组变量子项 |
| [get_trigger_list_variable_all_collider](#get_trigger_list_variable_all_collider) | 获取全局触发器COLLIDER数组变量 |
| [get_trigger_list_actor_variable_all_collider](#get_trigger_list_actor_variable_all_collider) | 获取触发器COLLIDER 组变量数组 |
| [get_trigger_variable_joint](#get_trigger_variable_joint) | 获取全局触发器JOINT非数组变量 |
| [get_trigger_actor_variable_joint](#get_trigger_actor_variable_joint) | 获取触发器JOINT非数组 组变量 |
| [get_trigger_list_variable_joint](#get_trigger_list_variable_joint) | 获取全局触发器JOINT数组变量子项 |
| [get_trigger_list_actor_variable_joint](#get_trigger_list_actor_variable_joint) | 获取触发器JOINT数组 组变量子项 |
| [get_trigger_list_variable_all_joint](#get_trigger_list_variable_all_joint) | 获取全局触发器JOINT数组变量 |
| [get_trigger_list_actor_variable_all_joint](#get_trigger_list_actor_variable_all_joint) | 获取触发器JOINT 组变量数组 |
| [get_trigger_variable_reaction](#get_trigger_variable_reaction) | 获取全局触发器REACTION非数组变量 |
| [get_trigger_actor_variable_reaction](#get_trigger_actor_variable_reaction) | 获取触发器REACTION非数组 组变量 |
| [get_trigger_list_variable_reaction](#get_trigger_list_variable_reaction) | 获取全局触发器REACTION数组变量子项 |
| [get_trigger_list_actor_variable_reaction](#get_trigger_list_actor_variable_reaction) | 获取触发器REACTION数组 组变量子项 |
| [get_trigger_list_variable_all_reaction](#get_trigger_list_variable_all_reaction) | 获取全局触发器REACTION数组变量 |
| [get_trigger_list_actor_variable_all_reaction](#get_trigger_list_actor_variable_all_reaction) | 获取触发器REACTION 组变量数组 |
| [get_trigger_variable_reaction_group](#get_trigger_variable_reaction_group) | 获取全局触发器REACTION_GROUP非数组变量 |
| [get_trigger_actor_variable_reaction_group](#get_trigger_actor_variable_reaction_group) | 获取触发器REACTION_GROUP非数组 组变量 |
| [get_trigger_list_variable_reaction_group](#get_trigger_list_variable_reaction_group) | 获取全局触发器REACTION_GROUP数组变量子项 |
| [get_trigger_list_actor_variable_reaction_group](#get_trigger_list_actor_variable_reaction_group) | 获取触发器REACTION_GROUP数组 组变量子项 |
| [get_trigger_list_variable_all_reaction_group](#get_trigger_list_variable_all_reaction_group) | 获取全局触发器REACTION_GROUP数组变量 |
| [get_trigger_list_actor_variable_all_reaction_group](#get_trigger_list_actor_variable_all_reaction_group) | 获取触发器REACTION_GROUP 组变量数组 |
| [get_trigger_variable_physics_filter](#get_trigger_variable_physics_filter) | 获取全局触发器PHYSICS_FILTER非数组变量 |
| [get_trigger_actor_variable_physics_filter](#get_trigger_actor_variable_physics_filter) | 获取触发器PHYSICS_FILTER非数组 组变量 |
| [get_trigger_list_variable_physics_filter](#get_trigger_list_variable_physics_filter) | 获取全局触发器PHYSICS_FILTER数组变量子项 |
| [get_trigger_list_actor_variable_physics_filter](#get_trigger_list_actor_variable_physics_filter) | 获取触发器PHYSICS_FILTER数组 组变量子项 |
| [get_trigger_list_variable_all_physics_filter](#get_trigger_list_variable_all_physics_filter) | 获取全局触发器PHYSICS_FILTER数组变量 |
| [get_trigger_list_actor_variable_all_physics_filter](#get_trigger_list_actor_variable_all_physics_filter) | 获取触发器PHYSICS_FILTER 组变量数组 |
| [get_trigger_variable_int_save](#get_trigger_variable_int_save) | 获取全局触发器INT_SAVE非数组变量 |
| [get_trigger_actor_variable_int_save](#get_trigger_actor_variable_int_save) | 获取触发器INT_SAVE非数组 组变量 |
| [get_trigger_list_variable_int_save](#get_trigger_list_variable_int_save) | 获取全局触发器INT_SAVE数组变量子项 |
| [get_trigger_list_actor_variable_int_save](#get_trigger_list_actor_variable_int_save) | 获取触发器INT_SAVE数组 组变量子项 |
| [get_trigger_list_variable_all_int_save](#get_trigger_list_variable_all_int_save) | 获取全局触发器INT_SAVE数组变量 |
| [get_trigger_list_actor_variable_all_int_save](#get_trigger_list_actor_variable_all_int_save) | 获取触发器INT_SAVE 组变量数组 |
| [get_trigger_variable_str_save](#get_trigger_variable_str_save) | 获取全局触发器STR_SAVE非数组变量 |
| [get_trigger_actor_variable_str_save](#get_trigger_actor_variable_str_save) | 获取触发器STR_SAVE非数组 组变量 |
| [get_trigger_list_variable_str_save](#get_trigger_list_variable_str_save) | 获取全局触发器STR_SAVE数组变量子项 |
| [get_trigger_list_actor_variable_str_save](#get_trigger_list_actor_variable_str_save) | 获取触发器STR_SAVE数组 组变量子项 |
| [get_trigger_list_variable_all_str_save](#get_trigger_list_variable_all_str_save) | 获取全局触发器STR_SAVE数组变量 |
| [get_trigger_list_actor_variable_all_str_save](#get_trigger_list_actor_variable_all_str_save) | 获取触发器STR_SAVE 组变量数组 |
| [get_trigger_variable_float_save](#get_trigger_variable_float_save) | 获取全局触发器FLOAT_SAVE非数组变量 |
| [get_trigger_actor_variable_float_save](#get_trigger_actor_variable_float_save) | 获取触发器FLOAT_SAVE非数组 组变量 |
| [get_trigger_list_variable_float_save](#get_trigger_list_variable_float_save) | 获取全局触发器FLOAT_SAVE数组变量子项 |
| [get_trigger_list_actor_variable_float_save](#get_trigger_list_actor_variable_float_save) | 获取触发器FLOAT_SAVE数组 组变量子项 |
| [get_trigger_list_variable_all_float_save](#get_trigger_list_variable_all_float_save) | 获取全局触发器FLOAT_SAVE数组变量 |
| [get_trigger_list_actor_variable_all_float_save](#get_trigger_list_actor_variable_all_float_save) | 获取触发器FLOAT_SAVE 组变量数组 |
| [get_trigger_variable_bool_save](#get_trigger_variable_bool_save) | 获取全局触发器BOOL_SAVE非数组变量 |
| [get_trigger_actor_variable_bool_save](#get_trigger_actor_variable_bool_save) | 获取触发器BOOL_SAVE非数组 组变量 |
| [get_trigger_list_variable_bool_save](#get_trigger_list_variable_bool_save) | 获取全局触发器BOOL_SAVE数组变量子项 |
| [get_trigger_list_actor_variable_bool_save](#get_trigger_list_actor_variable_bool_save) | 获取触发器BOOL_SAVE数组 组变量子项 |
| [get_trigger_list_variable_all_bool_save](#get_trigger_list_variable_all_bool_save) | 获取全局触发器BOOL_SAVE数组变量 |
| [get_trigger_list_actor_variable_all_bool_save](#get_trigger_list_actor_variable_all_bool_save) | 获取触发器BOOL_SAVE 组变量数组 |
| [get_trigger_variable_table_save](#get_trigger_variable_table_save) | 获取全局触发器TABLE_SAVE非数组变量 |
| [get_trigger_actor_variable_table_save](#get_trigger_actor_variable_table_save) | 获取触发器TABLE_SAVE非数组 组变量 |
| [get_trigger_list_variable_table_save](#get_trigger_list_variable_table_save) | 获取全局触发器TABLE_SAVE数组变量子项 |
| [get_trigger_list_actor_variable_table_save](#get_trigger_list_actor_variable_table_save) | 获取触发器TABLE_SAVE数组 组变量子项 |
| [get_trigger_list_variable_all_table_save](#get_trigger_list_variable_all_table_save) | 获取全局触发器TABLE_SAVE数组变量 |
| [get_trigger_list_actor_variable_all_table_save](#get_trigger_list_actor_variable_all_table_save) | 获取触发器TABLE_SAVE 组变量数组 |
| [get_trigger_variable_global_archive_slot](#get_trigger_variable_global_archive_slot) | 获取全局触发器GLOBAL_ARCHIVE_SLOT非数组变量 |
| [get_trigger_actor_variable_global_archive_slot](#get_trigger_actor_variable_global_archive_slot) | 获取触发器GLOBAL_ARCHIVE_SLOT非数组 组变量 |
| [get_trigger_list_variable_global_archive_slot](#get_trigger_list_variable_global_archive_slot) | 获取全局触发器GLOBAL_ARCHIVE_SLOT数组变量子项 |
| [get_trigger_list_actor_variable_global_archive_slot](#get_trigger_list_actor_variable_global_archive_slot) | 获取触发器GLOBAL_ARCHIVE_SLOT数组 组变量子项 |
| [get_trigger_list_variable_all_global_archive_slot](#get_trigger_list_variable_all_global_archive_slot) | 获取全局触发器GLOBAL_ARCHIVE_SLOT数组变量 |
| [get_trigger_list_actor_variable_all_global_archive_slot](#get_trigger_list_actor_variable_all_global_archive_slot) | 获取触发器GLOBAL_ARCHIVE_SLOT 组变量数组 |
| [get_trigger_variable_random_pool_drop](#get_trigger_variable_random_pool_drop) | 获取全局触发器RANDOM_POOL_DROP非数组变量 |
| [get_trigger_actor_variable_random_pool_drop](#get_trigger_actor_variable_random_pool_drop) | 获取触发器RANDOM_POOL_DROP非数组 组变量 |
| [get_trigger_list_variable_random_pool_drop](#get_trigger_list_variable_random_pool_drop) | 获取全局触发器RANDOM_POOL_DROP数组变量子项 |
| [get_trigger_list_actor_variable_random_pool_drop](#get_trigger_list_actor_variable_random_pool_drop) | 获取触发器RANDOM_POOL_DROP数组 组变量子项 |
| [get_trigger_list_variable_all_random_pool_drop](#get_trigger_list_variable_all_random_pool_drop) | 获取全局触发器RANDOM_POOL_DROP数组变量 |
| [get_trigger_list_actor_variable_all_random_pool_drop](#get_trigger_list_actor_variable_all_random_pool_drop) | 获取触发器RANDOM_POOL_DROP 组变量数组 |
| [get_trigger_variable_dynamic_trigger_instance](#get_trigger_variable_dynamic_trigger_instance) | 获取全局触发器DYNAMIC_TRIGGER_INSTANCE非数组变量 |
| [get_trigger_actor_variable_dynamic_trigger_instance](#get_trigger_actor_variable_dynamic_trigger_instance) | 获取触发器DYNAMIC_TRIGGER_INSTANCE非数组 组变量 |
| [get_trigger_list_variable_dynamic_trigger_instance](#get_trigger_list_variable_dynamic_trigger_instance) | 获取全局触发器DYNAMIC_TRIGGER_INSTANCE数组变量子项 |
| [get_trigger_list_actor_variable_dynamic_trigger_instance](#get_trigger_list_actor_variable_dynamic_trigger_instance) | 获取触发器DYNAMIC_TRIGGER_INSTANCE数组 组变量子项 |
| [get_trigger_list_variable_all_dynamic_trigger_instance](#get_trigger_list_variable_all_dynamic_trigger_instance) | 获取全局触发器DYNAMIC_TRIGGER_INSTANCE数组变量 |
| [get_trigger_list_actor_variable_all_dynamic_trigger_instance](#get_trigger_list_actor_variable_all_dynamic_trigger_instance) | 获取触发器DYNAMIC_TRIGGER_INSTANCE 组变量数组 |
| [get_trigger_variable_table](#get_trigger_variable_table) | 获取全局触发器TABLE非数组变量 |
| [get_trigger_actor_variable_table](#get_trigger_actor_variable_table) | 获取触发器TABLE非数组 组变量 |
| [get_trigger_list_variable_table](#get_trigger_list_variable_table) | 获取全局触发器TABLE数组变量子项 |
| [get_trigger_list_actor_variable_table](#get_trigger_list_actor_variable_table) | 获取触发器TABLE数组 组变量子项 |
| [get_trigger_list_variable_all_table](#get_trigger_list_variable_all_table) | 获取全局触发器TABLE数组变量 |
| [get_trigger_list_actor_variable_all_table](#get_trigger_list_actor_variable_all_table) | 获取触发器TABLE 组变量数组 |
| [get_trigger_variable_random_pool](#get_trigger_variable_random_pool) | 获取全局触发器RANDOM_POOL非数组变量 |
| [get_trigger_actor_variable_random_pool](#get_trigger_actor_variable_random_pool) | 获取触发器RANDOM_POOL非数组 组变量 |
| [get_trigger_list_variable_random_pool](#get_trigger_list_variable_random_pool) | 获取全局触发器RANDOM_POOL数组变量子项 |
| [get_trigger_list_actor_variable_random_pool](#get_trigger_list_actor_variable_random_pool) | 获取触发器RANDOM_POOL数组 组变量子项 |
| [get_trigger_list_variable_all_random_pool](#get_trigger_list_variable_all_random_pool) | 获取全局触发器RANDOM_POOL数组变量 |
| [get_trigger_list_actor_variable_all_random_pool](#get_trigger_list_actor_variable_all_random_pool) | 获取触发器RANDOM_POOL 组变量数组 |
| [get_trigger_variable_scene_ui](#get_trigger_variable_scene_ui) | 获取全局触发器SCENE_UI非数组变量 |
| [get_trigger_actor_variable_scene_ui](#get_trigger_actor_variable_scene_ui) | 获取触发器SCENE_UI非数组 组变量 |
| [get_trigger_list_variable_scene_ui](#get_trigger_list_variable_scene_ui) | 获取全局触发器SCENE_UI数组变量子项 |
| [get_trigger_list_actor_variable_scene_ui](#get_trigger_list_actor_variable_scene_ui) | 获取触发器SCENE_UI数组 组变量子项 |
| [get_trigger_list_variable_all_scene_ui](#get_trigger_list_variable_all_scene_ui) | 获取全局触发器SCENE_UI数组变量 |
| [get_trigger_list_actor_variable_all_scene_ui](#get_trigger_list_actor_variable_all_scene_ui) | 获取触发器SCENE_UI 组变量数组 |
| [get_trigger_variable_damage_type](#get_trigger_variable_damage_type) | 获取全局触发器DAMAGE_TYPE非数组变量 |
| [get_trigger_actor_variable_damage_type](#get_trigger_actor_variable_damage_type) | 获取触发器DAMAGE_TYPE非数组 组变量 |
| [get_trigger_list_variable_damage_type](#get_trigger_list_variable_damage_type) | 获取全局触发器DAMAGE_TYPE数组变量子项 |
| [get_trigger_list_actor_variable_damage_type](#get_trigger_list_actor_variable_damage_type) | 获取触发器DAMAGE_TYPE数组 组变量子项 |
| [get_trigger_list_variable_all_damage_type](#get_trigger_list_variable_all_damage_type) | 获取全局触发器DAMAGE_TYPE数组变量 |
| [get_trigger_list_actor_variable_all_damage_type](#get_trigger_list_actor_variable_all_damage_type) | 获取触发器DAMAGE_TYPE 组变量数组 |
| [get_trigger_variable_new_timer](#get_trigger_variable_new_timer) | 获取全局触发器NEW_TIMER非数组变量 |
| [get_trigger_actor_variable_new_timer](#get_trigger_actor_variable_new_timer) | 获取触发器NEW_TIMER非数组 组变量 |
| [get_trigger_list_variable_new_timer](#get_trigger_list_variable_new_timer) | 获取全局触发器NEW_TIMER数组变量子项 |
| [get_trigger_list_actor_variable_new_timer](#get_trigger_list_actor_variable_new_timer) | 获取触发器NEW_TIMER数组 组变量子项 |
| [get_trigger_list_variable_all_new_timer](#get_trigger_list_variable_all_new_timer) | 获取全局触发器NEW_TIMER数组变量 |
| [get_trigger_list_actor_variable_all_new_timer](#get_trigger_list_actor_variable_all_new_timer) | 获取触发器NEW_TIMER 组变量数组 |
| [get_trigger_variable_tech_key](#get_trigger_variable_tech_key) | 获取全局触发器TECH_KEY非数组变量 |
| [get_trigger_actor_variable_tech_key](#get_trigger_actor_variable_tech_key) | 获取触发器TECH_KEY非数组 组变量 |
| [get_trigger_list_variable_tech_key](#get_trigger_list_variable_tech_key) | 获取全局触发器TECH_KEY数组变量子项 |
| [get_trigger_list_actor_variable_tech_key](#get_trigger_list_actor_variable_tech_key) | 获取触发器TECH_KEY数组 组变量子项 |
| [get_trigger_list_variable_all_tech_key](#get_trigger_list_variable_all_tech_key) | 获取全局触发器TECH_KEY数组变量 |
| [get_trigger_list_actor_variable_all_tech_key](#get_trigger_list_actor_variable_all_tech_key) | 获取触发器TECH_KEY 组变量数组 |
| [get_trigger_variable_store_key](#get_trigger_variable_store_key) | 获取全局触发器STORE_KEY非数组变量 |
| [get_trigger_actor_variable_store_key](#get_trigger_actor_variable_store_key) | 获取触发器STORE_KEY非数组 组变量 |
| [get_trigger_list_variable_store_key](#get_trigger_list_variable_store_key) | 获取全局触发器STORE_KEY数组变量子项 |
| [get_trigger_list_actor_variable_store_key](#get_trigger_list_actor_variable_store_key) | 获取触发器STORE_KEY数组 组变量子项 |
| [get_trigger_list_variable_all_store_key](#get_trigger_list_variable_all_store_key) | 获取全局触发器STORE_KEY数组变量 |
| [get_trigger_list_actor_variable_all_store_key](#get_trigger_list_actor_variable_all_store_key) | 获取触发器STORE_KEY 组变量数组 |
| [get_trigger_variable_keyboard_key](#get_trigger_variable_keyboard_key) | 获取全局触发器KEYBOARD_KEY非数组变量 |
| [get_trigger_actor_variable_keyboard_key](#get_trigger_actor_variable_keyboard_key) | 获取触发器KEYBOARD_KEY非数组 组变量 |
| [get_trigger_list_variable_keyboard_key](#get_trigger_list_variable_keyboard_key) | 获取全局触发器KEYBOARD_KEY数组变量子项 |
| [get_trigger_list_actor_variable_keyboard_key](#get_trigger_list_actor_variable_keyboard_key) | 获取触发器KEYBOARD_KEY数组 组变量子项 |
| [get_trigger_list_variable_all_keyboard_key](#get_trigger_list_variable_all_keyboard_key) | 获取全局触发器KEYBOARD_KEY数组变量 |
| [get_trigger_list_actor_variable_all_keyboard_key](#get_trigger_list_actor_variable_all_keyboard_key) | 获取触发器KEYBOARD_KEY 组变量数组 |
| [get_trigger_variable_unit_type](#get_trigger_variable_unit_type) | 获取全局触发器UNIT_TYPE非数组变量 |
| [get_trigger_actor_variable_unit_type](#get_trigger_actor_variable_unit_type) | 获取触发器UNIT_TYPE非数组 组变量 |
| [get_trigger_list_variable_unit_type](#get_trigger_list_variable_unit_type) | 获取全局触发器UNIT_TYPE数组变量子项 |
| [get_trigger_list_actor_variable_unit_type](#get_trigger_list_actor_variable_unit_type) | 获取触发器UNIT_TYPE数组 组变量子项 |
| [get_trigger_list_variable_all_unit_type](#get_trigger_list_variable_all_unit_type) | 获取全局触发器UNIT_TYPE数组变量 |
| [get_trigger_list_actor_variable_all_unit_type](#get_trigger_list_actor_variable_all_unit_type) | 获取触发器UNIT_TYPE 组变量数组 |
| [get_trigger_variable_curved_path](#get_trigger_variable_curved_path) | 获取全局触发器CURVED_PATH非数组变量 |
| [get_trigger_actor_variable_curved_path](#get_trigger_actor_variable_curved_path) | 获取触发器CURVED_PATH非数组 组变量 |
| [get_trigger_list_variable_curved_path](#get_trigger_list_variable_curved_path) | 获取全局触发器CURVED_PATH数组变量子项 |
| [get_trigger_list_actor_variable_curved_path](#get_trigger_list_actor_variable_curved_path) | 获取触发器CURVED_PATH数组 组变量子项 |
| [get_trigger_list_variable_all_curved_path](#get_trigger_list_variable_all_curved_path) | 获取全局触发器CURVED_PATH数组变量 |
| [get_trigger_list_actor_variable_all_curved_path](#get_trigger_list_actor_variable_all_curved_path) | 获取触发器CURVED_PATH 组变量数组 |
| [get_trigger_variable_curved_path_3d](#get_trigger_variable_curved_path_3d) | 获取全局触发器CURVED_PATH_3D非数组变量 |
| [get_trigger_actor_variable_curved_path_3d](#get_trigger_actor_variable_curved_path_3d) | 获取触发器CURVED_PATH_3D非数组 组变量 |
| [get_trigger_list_variable_curved_path_3d](#get_trigger_list_variable_curved_path_3d) | 获取全局触发器CURVED_PATH_3D数组变量子项 |
| [get_trigger_list_actor_variable_curved_path_3d](#get_trigger_list_actor_variable_curved_path_3d) | 获取触发器CURVED_PATH_3D数组 组变量子项 |
| [get_trigger_list_variable_all_curved_path_3d](#get_trigger_list_variable_all_curved_path_3d) | 获取全局触发器CURVED_PATH_3D数组变量 |
| [get_trigger_list_actor_variable_all_curved_path_3d](#get_trigger_list_actor_variable_all_curved_path_3d) | 获取触发器CURVED_PATH_3D 组变量数组 |
| [set_trigger_variable_by_type](#set_trigger_variable_by_type) | 设置全局触发器非数组变量（指定类型） |
| [set_trigger_list_variable_by_type](#set_trigger_list_variable_by_type) | 设置全局触发器数组变量子项（指定类型） |
| [set_trigger_list_variable_boolean](#set_trigger_list_variable_boolean) | 设置全局触发器BOOLEAN数组变量子项 |
| [set_trigger_list_actor_variable_boolean](#set_trigger_list_actor_variable_boolean) | 设置全局触发器BOOLEAN数组 组变量子项 |
| [set_trigger_variable_boolean](#set_trigger_variable_boolean) | 设置全局触发器BOOLEAN非数组变量 |
| [set_trigger_actor_variable_boolean](#set_trigger_actor_variable_boolean) | 设置全局触发器BOOLEAN非数组 组变量 |
| [set_trigger_list_variable_integer](#set_trigger_list_variable_integer) | 设置全局触发器INTEGER数组变量子项 |
| [set_trigger_list_actor_variable_integer](#set_trigger_list_actor_variable_integer) | 设置全局触发器INTEGER数组 组变量子项 |
| [set_trigger_variable_integer](#set_trigger_variable_integer) | 设置全局触发器INTEGER非数组变量 |
| [set_trigger_actor_variable_integer](#set_trigger_actor_variable_integer) | 设置全局触发器INTEGER非数组 组变量 |
| [set_trigger_list_variable_float](#set_trigger_list_variable_float) | 设置全局触发器FLOAT数组变量子项 |
| [set_trigger_list_actor_variable_float](#set_trigger_list_actor_variable_float) | 设置全局触发器FLOAT数组 组变量子项 |
| [set_trigger_variable_float](#set_trigger_variable_float) | 设置全局触发器FLOAT非数组变量 |
| [set_trigger_actor_variable_float](#set_trigger_actor_variable_float) | 设置全局触发器FLOAT非数组 组变量 |
| [set_trigger_list_variable_string](#set_trigger_list_variable_string) | 设置全局触发器STRING数组变量子项 |
| [set_trigger_list_actor_variable_string](#set_trigger_list_actor_variable_string) | 设置全局触发器STRING数组 组变量子项 |
| [set_trigger_variable_string](#set_trigger_variable_string) | 设置全局触发器STRING非数组变量 |
| [set_trigger_actor_variable_string](#set_trigger_actor_variable_string) | 设置全局触发器STRING非数组 组变量 |
| [set_trigger_list_variable_ui_comp](#set_trigger_list_variable_ui_comp) | 设置全局触发器UI_COMP数组变量子项 |
| [set_trigger_list_actor_variable_ui_comp](#set_trigger_list_actor_variable_ui_comp) | 设置全局触发器UI_COMP数组 组变量子项 |
| [set_trigger_variable_ui_comp](#set_trigger_variable_ui_comp) | 设置全局触发器UI_COMP非数组变量 |
| [set_trigger_actor_variable_ui_comp](#set_trigger_actor_variable_ui_comp) | 设置全局触发器UI_COMP非数组 组变量 |
| [set_trigger_list_variable_ui_comp_type](#set_trigger_list_variable_ui_comp_type) | 设置全局触发器UI_COMP_TYPE数组变量子项 |
| [set_trigger_list_actor_variable_ui_comp_type](#set_trigger_list_actor_variable_ui_comp_type) | 设置全局触发器UI_COMP_TYPE数组 组变量子项 |
| [set_trigger_variable_ui_comp_type](#set_trigger_variable_ui_comp_type) | 设置全局触发器UI_COMP_TYPE非数组变量 |
| [set_trigger_actor_variable_ui_comp_type](#set_trigger_actor_variable_ui_comp_type) | 设置全局触发器UI_COMP_TYPE非数组 组变量 |
| [set_trigger_list_variable_ui_comp_event_type](#set_trigger_list_variable_ui_comp_event_type) | 设置全局触发器UI_COMP_EVENT_TYPE数组变量子项 |
| [set_trigger_list_actor_variable_ui_comp_event_type](#set_trigger_list_actor_variable_ui_comp_event_type) | 设置全局触发器UI_COMP_EVENT_TYPE数组 组变量子项 |
| [set_trigger_variable_ui_comp_event_type](#set_trigger_variable_ui_comp_event_type) | 设置全局触发器UI_COMP_EVENT_TYPE非数组变量 |
| [set_trigger_actor_variable_ui_comp_event_type](#set_trigger_actor_variable_ui_comp_event_type) | 设置全局触发器UI_COMP_EVENT_TYPE非数组 组变量 |
| [set_trigger_list_variable_ui_comp_align_type](#set_trigger_list_variable_ui_comp_align_type) | 设置全局触发器UI_COMP_ALIGN_TYPE数组变量子项 |
| [set_trigger_list_actor_variable_ui_comp_align_type](#set_trigger_list_actor_variable_ui_comp_align_type) | 设置全局触发器UI_COMP_ALIGN_TYPE数组 组变量子项 |
| [set_trigger_variable_ui_comp_align_type](#set_trigger_variable_ui_comp_align_type) | 设置全局触发器UI_COMP_ALIGN_TYPE非数组变量 |
| [set_trigger_actor_variable_ui_comp_align_type](#set_trigger_actor_variable_ui_comp_align_type) | 设置全局触发器UI_COMP_ALIGN_TYPE非数组 组变量 |
| [set_trigger_list_variable_ui_prefab](#set_trigger_list_variable_ui_prefab) | 设置全局触发器UI_PREFAB数组变量子项 |
| [set_trigger_list_actor_variable_ui_prefab](#set_trigger_list_actor_variable_ui_prefab) | 设置全局触发器UI_PREFAB数组 组变量子项 |
| [set_trigger_variable_ui_prefab](#set_trigger_variable_ui_prefab) | 设置全局触发器UI_PREFAB非数组变量 |
| [set_trigger_actor_variable_ui_prefab](#set_trigger_actor_variable_ui_prefab) | 设置全局触发器UI_PREFAB非数组 组变量 |
| [set_trigger_list_variable_ui_prefab_instance](#set_trigger_list_variable_ui_prefab_instance) | 设置全局触发器UI_PREFAB_INSTANCE数组变量子项 |
| [set_trigger_list_actor_variable_ui_prefab_instance](#set_trigger_list_actor_variable_ui_prefab_instance) | 设置全局触发器UI_PREFAB_INSTANCE数组 组变量子项 |
| [set_trigger_variable_ui_prefab_instance](#set_trigger_variable_ui_prefab_instance) | 设置全局触发器UI_PREFAB_INSTANCE非数组变量 |
| [set_trigger_actor_variable_ui_prefab_instance](#set_trigger_actor_variable_ui_prefab_instance) | 设置全局触发器UI_PREFAB_INSTANCE非数组 组变量 |
| [set_trigger_list_variable_ui_prefab_ins_uid](#set_trigger_list_variable_ui_prefab_ins_uid) | 设置全局触发器UI_PREFAB_INS_UID数组变量子项 |
| [set_trigger_list_actor_variable_ui_prefab_ins_uid](#set_trigger_list_actor_variable_ui_prefab_ins_uid) | 设置全局触发器UI_PREFAB_INS_UID数组 组变量子项 |
| [set_trigger_variable_ui_prefab_ins_uid](#set_trigger_variable_ui_prefab_ins_uid) | 设置全局触发器UI_PREFAB_INS_UID非数组变量 |
| [set_trigger_actor_variable_ui_prefab_ins_uid](#set_trigger_actor_variable_ui_prefab_ins_uid) | 设置全局触发器UI_PREFAB_INS_UID非数组 组变量 |
| [set_trigger_list_variable_ui_direction](#set_trigger_list_variable_ui_direction) | 设置全局触发器UI_DIRECTION数组变量子项 |
| [set_trigger_list_actor_variable_ui_direction](#set_trigger_list_actor_variable_ui_direction) | 设置全局触发器UI_DIRECTION数组 组变量子项 |
| [set_trigger_variable_ui_direction](#set_trigger_variable_ui_direction) | 设置全局触发器UI_DIRECTION非数组变量 |
| [set_trigger_actor_variable_ui_direction](#set_trigger_actor_variable_ui_direction) | 设置全局触发器UI_DIRECTION非数组 组变量 |
| [set_trigger_list_variable_ui_model_camera_mod](#set_trigger_list_variable_ui_model_camera_mod) | 设置全局触发器UI_MODEL_CAMERA_MOD数组变量子项 |
| [set_trigger_list_actor_variable_ui_model_camera_mod](#set_trigger_list_actor_variable_ui_model_camera_mod) | 设置全局触发器UI_MODEL_CAMERA_MOD数组 组变量子项 |
| [set_trigger_variable_ui_model_camera_mod](#set_trigger_variable_ui_model_camera_mod) | 设置全局触发器UI_MODEL_CAMERA_MOD非数组变量 |
| [set_trigger_actor_variable_ui_model_camera_mod](#set_trigger_actor_variable_ui_model_camera_mod) | 设置全局触发器UI_MODEL_CAMERA_MOD非数组 组变量 |
| [set_trigger_list_variable_ui_btn_status](#set_trigger_list_variable_ui_btn_status) | 设置全局触发器UI_BTN_STATUS数组变量子项 |
| [set_trigger_list_actor_variable_ui_btn_status](#set_trigger_list_actor_variable_ui_btn_status) | 设置全局触发器UI_BTN_STATUS数组 组变量子项 |
| [set_trigger_variable_ui_btn_status](#set_trigger_variable_ui_btn_status) | 设置全局触发器UI_BTN_STATUS非数组变量 |
| [set_trigger_actor_variable_ui_btn_status](#set_trigger_actor_variable_ui_btn_status) | 设置全局触发器UI_BTN_STATUS非数组 组变量 |
| [set_trigger_list_variable_ui_scrollview_type](#set_trigger_list_variable_ui_scrollview_type) | 设置全局触发器UI_SCROLLVIEW_TYPE数组变量子项 |
| [set_trigger_list_actor_variable_ui_scrollview_type](#set_trigger_list_actor_variable_ui_scrollview_type) | 设置全局触发器UI_SCROLLVIEW_TYPE数组 组变量子项 |
| [set_trigger_variable_ui_scrollview_type](#set_trigger_variable_ui_scrollview_type) | 设置全局触发器UI_SCROLLVIEW_TYPE非数组变量 |
| [set_trigger_actor_variable_ui_scrollview_type](#set_trigger_actor_variable_ui_scrollview_type) | 设置全局触发器UI_SCROLLVIEW_TYPE非数组 组变量 |
| [set_trigger_list_variable_ui_anim](#set_trigger_list_variable_ui_anim) | 设置全局触发器UI_ANIM数组变量子项 |
| [set_trigger_list_actor_variable_ui_anim](#set_trigger_list_actor_variable_ui_anim) | 设置全局触发器UI_ANIM数组 组变量子项 |
| [set_trigger_variable_ui_anim](#set_trigger_variable_ui_anim) | 设置全局触发器UI_ANIM非数组变量 |
| [set_trigger_actor_variable_ui_anim](#set_trigger_actor_variable_ui_anim) | 设置全局触发器UI_ANIM非数组 组变量 |
| [set_trigger_list_variable_ui_anim_curve](#set_trigger_list_variable_ui_anim_curve) | 设置全局触发器UI_ANIM_CURVE数组变量子项 |
| [set_trigger_list_actor_variable_ui_anim_curve](#set_trigger_list_actor_variable_ui_anim_curve) | 设置全局触发器UI_ANIM_CURVE数组 组变量子项 |
| [set_trigger_variable_ui_anim_curve](#set_trigger_variable_ui_anim_curve) | 设置全局触发器UI_ANIM_CURVE非数组变量 |
| [set_trigger_actor_variable_ui_anim_curve](#set_trigger_actor_variable_ui_anim_curve) | 设置全局触发器UI_ANIM_CURVE非数组 组变量 |
| [set_trigger_list_variable_audio_channel](#set_trigger_list_variable_audio_channel) | 设置全局触发器AUDIO_CHANNEL数组变量子项 |
| [set_trigger_list_actor_variable_audio_channel](#set_trigger_list_actor_variable_audio_channel) | 设置全局触发器AUDIO_CHANNEL数组 组变量子项 |
| [set_trigger_variable_audio_channel](#set_trigger_variable_audio_channel) | 设置全局触发器AUDIO_CHANNEL非数组变量 |
| [set_trigger_actor_variable_audio_channel](#set_trigger_actor_variable_audio_channel) | 设置全局触发器AUDIO_CHANNEL非数组 组变量 |
| [set_trigger_list_variable_unit_entity](#set_trigger_list_variable_unit_entity) | 设置全局触发器UNIT_ENTITY数组变量子项 |
| [set_trigger_list_actor_variable_unit_entity](#set_trigger_list_actor_variable_unit_entity) | 设置全局触发器UNIT_ENTITY数组 组变量子项 |
| [set_trigger_variable_unit_entity](#set_trigger_variable_unit_entity) | 设置全局触发器UNIT_ENTITY非数组变量 |
| [set_trigger_actor_variable_unit_entity](#set_trigger_actor_variable_unit_entity) | 设置全局触发器UNIT_ENTITY非数组 组变量 |
| [set_trigger_list_variable_unit_group](#set_trigger_list_variable_unit_group) | 设置全局触发器UNIT_GROUP数组变量子项 |
| [set_trigger_list_actor_variable_unit_group](#set_trigger_list_actor_variable_unit_group) | 设置全局触发器UNIT_GROUP数组 组变量子项 |
| [set_trigger_variable_unit_group](#set_trigger_variable_unit_group) | 设置全局触发器UNIT_GROUP非数组变量 |
| [set_trigger_actor_variable_unit_group](#set_trigger_actor_variable_unit_group) | 设置全局触发器UNIT_GROUP非数组 组变量 |
| [set_trigger_list_variable_unit_name](#set_trigger_list_variable_unit_name) | 设置全局触发器UNIT_NAME数组变量子项 |
| [set_trigger_list_actor_variable_unit_name](#set_trigger_list_actor_variable_unit_name) | 设置全局触发器UNIT_NAME数组 组变量子项 |
| [set_trigger_variable_unit_name](#set_trigger_variable_unit_name) | 设置全局触发器UNIT_NAME非数组变量 |
| [set_trigger_actor_variable_unit_name](#set_trigger_actor_variable_unit_name) | 设置全局触发器UNIT_NAME非数组 组变量 |
| [set_trigger_list_variable_unit_name_pool](#set_trigger_list_variable_unit_name_pool) | 设置全局触发器UNIT_NAME_POOL数组变量子项 |
| [set_trigger_list_actor_variable_unit_name_pool](#set_trigger_list_actor_variable_unit_name_pool) | 设置全局触发器UNIT_NAME_POOL数组 组变量子项 |
| [set_trigger_variable_unit_name_pool](#set_trigger_variable_unit_name_pool) | 设置全局触发器UNIT_NAME_POOL非数组变量 |
| [set_trigger_actor_variable_unit_name_pool](#set_trigger_actor_variable_unit_name_pool) | 设置全局触发器UNIT_NAME_POOL非数组 组变量 |
| [set_trigger_list_variable_unit_write_attribute](#set_trigger_list_variable_unit_write_attribute) | 设置全局触发器UNIT_WRITE_ATTRIBUTE数组变量子项 |
| [set_trigger_list_actor_variable_unit_write_attribute](#set_trigger_list_actor_variable_unit_write_attribute) | 设置全局触发器UNIT_WRITE_ATTRIBUTE数组 组变量子项 |
| [set_trigger_variable_unit_write_attribute](#set_trigger_variable_unit_write_attribute) | 设置全局触发器UNIT_WRITE_ATTRIBUTE非数组变量 |
| [set_trigger_actor_variable_unit_write_attribute](#set_trigger_actor_variable_unit_write_attribute) | 设置全局触发器UNIT_WRITE_ATTRIBUTE非数组 组变量 |
| [set_trigger_list_variable_attr_element](#set_trigger_list_variable_attr_element) | 设置全局触发器ATTR_ELEMENT数组变量子项 |
| [set_trigger_list_actor_variable_attr_element](#set_trigger_list_actor_variable_attr_element) | 设置全局触发器ATTR_ELEMENT数组 组变量子项 |
| [set_trigger_variable_attr_element](#set_trigger_variable_attr_element) | 设置全局触发器ATTR_ELEMENT非数组变量 |
| [set_trigger_actor_variable_attr_element](#set_trigger_actor_variable_attr_element) | 设置全局触发器ATTR_ELEMENT非数组 组变量 |
| [set_trigger_list_variable_attr_element_read](#set_trigger_list_variable_attr_element_read) | 设置全局触发器ATTR_ELEMENT_READ数组变量子项 |
| [set_trigger_list_actor_variable_attr_element_read](#set_trigger_list_actor_variable_attr_element_read) | 设置全局触发器ATTR_ELEMENT_READ数组 组变量子项 |
| [set_trigger_variable_attr_element_read](#set_trigger_variable_attr_element_read) | 设置全局触发器ATTR_ELEMENT_READ非数组变量 |
| [set_trigger_actor_variable_attr_element_read](#set_trigger_actor_variable_attr_element_read) | 设置全局触发器ATTR_ELEMENT_READ非数组 组变量 |
| [set_trigger_list_variable_mover_entity](#set_trigger_list_variable_mover_entity) | 设置全局触发器MOVER_ENTITY数组变量子项 |
| [set_trigger_list_actor_variable_mover_entity](#set_trigger_list_actor_variable_mover_entity) | 设置全局触发器MOVER_ENTITY数组 组变量子项 |
| [set_trigger_variable_mover_entity](#set_trigger_variable_mover_entity) | 设置全局触发器MOVER_ENTITY非数组变量 |
| [set_trigger_actor_variable_mover_entity](#set_trigger_actor_variable_mover_entity) | 设置全局触发器MOVER_ENTITY非数组 组变量 |
| [set_trigger_list_variable_image_quality](#set_trigger_list_variable_image_quality) | 设置全局触发器IMAGE_QUALITY数组变量子项 |
| [set_trigger_list_actor_variable_image_quality](#set_trigger_list_actor_variable_image_quality) | 设置全局触发器IMAGE_QUALITY数组 组变量子项 |
| [set_trigger_variable_image_quality](#set_trigger_variable_image_quality) | 设置全局触发器IMAGE_QUALITY非数组变量 |
| [set_trigger_actor_variable_image_quality](#set_trigger_actor_variable_image_quality) | 设置全局触发器IMAGE_QUALITY非数组 组变量 |
| [set_trigger_list_variable_window_type_setting](#set_trigger_list_variable_window_type_setting) | 设置全局触发器WINDOW_TYPE_SETTING数组变量子项 |
| [set_trigger_list_actor_variable_window_type_setting](#set_trigger_list_actor_variable_window_type_setting) | 设置全局触发器WINDOW_TYPE_SETTING数组 组变量子项 |
| [set_trigger_variable_window_type_setting](#set_trigger_variable_window_type_setting) | 设置全局触发器WINDOW_TYPE_SETTING非数组变量 |
| [set_trigger_actor_variable_window_type_setting](#set_trigger_actor_variable_window_type_setting) | 设置全局触发器WINDOW_TYPE_SETTING非数组 组变量 |
| [set_trigger_list_variable_damage_attack_type](#set_trigger_list_variable_damage_attack_type) | 设置全局触发器DAMAGE_ATTACK_TYPE数组变量子项 |
| [set_trigger_list_actor_variable_damage_attack_type](#set_trigger_list_actor_variable_damage_attack_type) | 设置全局触发器DAMAGE_ATTACK_TYPE数组 组变量子项 |
| [set_trigger_variable_damage_attack_type](#set_trigger_variable_damage_attack_type) | 设置全局触发器DAMAGE_ATTACK_TYPE非数组变量 |
| [set_trigger_actor_variable_damage_attack_type](#set_trigger_actor_variable_damage_attack_type) | 设置全局触发器DAMAGE_ATTACK_TYPE非数组 组变量 |
| [set_trigger_list_variable_damage_armor_type](#set_trigger_list_variable_damage_armor_type) | 设置全局触发器DAMAGE_ARMOR_TYPE数组变量子项 |
| [set_trigger_list_actor_variable_damage_armor_type](#set_trigger_list_actor_variable_damage_armor_type) | 设置全局触发器DAMAGE_ARMOR_TYPE数组 组变量子项 |
| [set_trigger_variable_damage_armor_type](#set_trigger_variable_damage_armor_type) | 设置全局触发器DAMAGE_ARMOR_TYPE非数组变量 |
| [set_trigger_actor_variable_damage_armor_type](#set_trigger_actor_variable_damage_armor_type) | 设置全局触发器DAMAGE_ARMOR_TYPE非数组 组变量 |
| [set_trigger_list_variable_item_entity](#set_trigger_list_variable_item_entity) | 设置全局触发器ITEM_ENTITY数组变量子项 |
| [set_trigger_list_actor_variable_item_entity](#set_trigger_list_actor_variable_item_entity) | 设置全局触发器ITEM_ENTITY数组 组变量子项 |
| [set_trigger_variable_item_entity](#set_trigger_variable_item_entity) | 设置全局触发器ITEM_ENTITY非数组变量 |
| [set_trigger_actor_variable_item_entity](#set_trigger_actor_variable_item_entity) | 设置全局触发器ITEM_ENTITY非数组 组变量 |
| [set_trigger_list_variable_item_group](#set_trigger_list_variable_item_group) | 设置全局触发器ITEM_GROUP数组变量子项 |
| [set_trigger_list_actor_variable_item_group](#set_trigger_list_actor_variable_item_group) | 设置全局触发器ITEM_GROUP数组 组变量子项 |
| [set_trigger_variable_item_group](#set_trigger_variable_item_group) | 设置全局触发器ITEM_GROUP非数组变量 |
| [set_trigger_actor_variable_item_group](#set_trigger_actor_variable_item_group) | 设置全局触发器ITEM_GROUP非数组 组变量 |
| [set_trigger_list_variable_item_name](#set_trigger_list_variable_item_name) | 设置全局触发器ITEM_NAME数组变量子项 |
| [set_trigger_list_actor_variable_item_name](#set_trigger_list_actor_variable_item_name) | 设置全局触发器ITEM_NAME数组 组变量子项 |
| [set_trigger_variable_item_name](#set_trigger_variable_item_name) | 设置全局触发器ITEM_NAME非数组变量 |
| [set_trigger_actor_variable_item_name](#set_trigger_actor_variable_item_name) | 设置全局触发器ITEM_NAME非数组 组变量 |
| [set_trigger_list_variable_ability](#set_trigger_list_variable_ability) | 设置全局触发器ABILITY数组变量子项 |
| [set_trigger_list_actor_variable_ability](#set_trigger_list_actor_variable_ability) | 设置全局触发器ABILITY数组 组变量子项 |
| [set_trigger_variable_ability](#set_trigger_variable_ability) | 设置全局触发器ABILITY非数组变量 |
| [set_trigger_actor_variable_ability](#set_trigger_actor_variable_ability) | 设置全局触发器ABILITY非数组 组变量 |
| [set_trigger_list_variable_ability_type](#set_trigger_list_variable_ability_type) | 设置全局触发器ABILITY_TYPE数组变量子项 |
| [set_trigger_list_actor_variable_ability_type](#set_trigger_list_actor_variable_ability_type) | 设置全局触发器ABILITY_TYPE数组 组变量子项 |
| [set_trigger_variable_ability_type](#set_trigger_variable_ability_type) | 设置全局触发器ABILITY_TYPE非数组变量 |
| [set_trigger_actor_variable_ability_type](#set_trigger_actor_variable_ability_type) | 设置全局触发器ABILITY_TYPE非数组 组变量 |
| [set_trigger_list_variable_ability_cast_type](#set_trigger_list_variable_ability_cast_type) | 设置全局触发器ABILITY_CAST_TYPE数组变量子项 |
| [set_trigger_list_actor_variable_ability_cast_type](#set_trigger_list_actor_variable_ability_cast_type) | 设置全局触发器ABILITY_CAST_TYPE数组 组变量子项 |
| [set_trigger_variable_ability_cast_type](#set_trigger_variable_ability_cast_type) | 设置全局触发器ABILITY_CAST_TYPE非数组变量 |
| [set_trigger_actor_variable_ability_cast_type](#set_trigger_actor_variable_ability_cast_type) | 设置全局触发器ABILITY_CAST_TYPE非数组 组变量 |
| [set_trigger_list_variable_ability_name](#set_trigger_list_variable_ability_name) | 设置全局触发器ABILITY_NAME数组变量子项 |
| [set_trigger_list_actor_variable_ability_name](#set_trigger_list_actor_variable_ability_name) | 设置全局触发器ABILITY_NAME数组 组变量子项 |
| [set_trigger_variable_ability_name](#set_trigger_variable_ability_name) | 设置全局触发器ABILITY_NAME非数组变量 |
| [set_trigger_actor_variable_ability_name](#set_trigger_actor_variable_ability_name) | 设置全局触发器ABILITY_NAME非数组 组变量 |
| [set_trigger_list_variable_modifier_entity](#set_trigger_list_variable_modifier_entity) | 设置全局触发器MODIFIER_ENTITY数组变量子项 |
| [set_trigger_list_actor_variable_modifier_entity](#set_trigger_list_actor_variable_modifier_entity) | 设置全局触发器MODIFIER_ENTITY数组 组变量子项 |
| [set_trigger_variable_modifier_entity](#set_trigger_variable_modifier_entity) | 设置全局触发器MODIFIER_ENTITY非数组变量 |
| [set_trigger_actor_variable_modifier_entity](#set_trigger_actor_variable_modifier_entity) | 设置全局触发器MODIFIER_ENTITY非数组 组变量 |
| [set_trigger_list_variable_modifier](#set_trigger_list_variable_modifier) | 设置全局触发器MODIFIER数组变量子项 |
| [set_trigger_list_actor_variable_modifier](#set_trigger_list_actor_variable_modifier) | 设置全局触发器MODIFIER数组 组变量子项 |
| [set_trigger_variable_modifier](#set_trigger_variable_modifier) | 设置全局触发器MODIFIER非数组变量 |
| [set_trigger_actor_variable_modifier](#set_trigger_actor_variable_modifier) | 设置全局触发器MODIFIER非数组 组变量 |
| [set_trigger_list_variable_projectile](#set_trigger_list_variable_projectile) | 设置全局触发器PROJECTILE数组变量子项 |
| [set_trigger_list_actor_variable_projectile](#set_trigger_list_actor_variable_projectile) | 设置全局触发器PROJECTILE数组 组变量子项 |
| [set_trigger_variable_projectile](#set_trigger_variable_projectile) | 设置全局触发器PROJECTILE非数组变量 |
| [set_trigger_actor_variable_projectile](#set_trigger_actor_variable_projectile) | 设置全局触发器PROJECTILE非数组 组变量 |
| [set_trigger_list_variable_projectile_entity](#set_trigger_list_variable_projectile_entity) | 设置全局触发器PROJECTILE_ENTITY数组变量子项 |
| [set_trigger_list_actor_variable_projectile_entity](#set_trigger_list_actor_variable_projectile_entity) | 设置全局触发器PROJECTILE_ENTITY数组 组变量子项 |
| [set_trigger_variable_projectile_entity](#set_trigger_variable_projectile_entity) | 设置全局触发器PROJECTILE_ENTITY非数组变量 |
| [set_trigger_actor_variable_projectile_entity](#set_trigger_actor_variable_projectile_entity) | 设置全局触发器PROJECTILE_ENTITY非数组 组变量 |
| [set_trigger_list_variable_projectile_group](#set_trigger_list_variable_projectile_group) | 设置全局触发器PROJECTILE_GROUP数组变量子项 |
| [set_trigger_list_actor_variable_projectile_group](#set_trigger_list_actor_variable_projectile_group) | 设置全局触发器PROJECTILE_GROUP数组 组变量子项 |
| [set_trigger_variable_projectile_group](#set_trigger_variable_projectile_group) | 设置全局触发器PROJECTILE_GROUP非数组变量 |
| [set_trigger_actor_variable_projectile_group](#set_trigger_actor_variable_projectile_group) | 设置全局触发器PROJECTILE_GROUP非数组 组变量 |
| [set_trigger_list_variable_destructible_entity](#set_trigger_list_variable_destructible_entity) | 设置全局触发器DESTRUCTIBLE_ENTITY数组变量子项 |
| [set_trigger_list_actor_variable_destructible_entity](#set_trigger_list_actor_variable_destructible_entity) | 设置全局触发器DESTRUCTIBLE_ENTITY数组 组变量子项 |
| [set_trigger_variable_destructible_entity](#set_trigger_variable_destructible_entity) | 设置全局触发器DESTRUCTIBLE_ENTITY非数组变量 |
| [set_trigger_actor_variable_destructible_entity](#set_trigger_actor_variable_destructible_entity) | 设置全局触发器DESTRUCTIBLE_ENTITY非数组 组变量 |
| [set_trigger_list_variable_destructible_name](#set_trigger_list_variable_destructible_name) | 设置全局触发器DESTRUCTIBLE_NAME数组变量子项 |
| [set_trigger_list_actor_variable_destructible_name](#set_trigger_list_actor_variable_destructible_name) | 设置全局触发器DESTRUCTIBLE_NAME数组 组变量子项 |
| [set_trigger_variable_destructible_name](#set_trigger_variable_destructible_name) | 设置全局触发器DESTRUCTIBLE_NAME非数组变量 |
| [set_trigger_actor_variable_destructible_name](#set_trigger_actor_variable_destructible_name) | 设置全局触发器DESTRUCTIBLE_NAME非数组 组变量 |
| [set_trigger_list_variable_sound_entity](#set_trigger_list_variable_sound_entity) | 设置全局触发器SOUND_ENTITY数组变量子项 |
| [set_trigger_list_actor_variable_sound_entity](#set_trigger_list_actor_variable_sound_entity) | 设置全局触发器SOUND_ENTITY数组 组变量子项 |
| [set_trigger_variable_sound_entity](#set_trigger_variable_sound_entity) | 设置全局触发器SOUND_ENTITY非数组变量 |
| [set_trigger_actor_variable_sound_entity](#set_trigger_actor_variable_sound_entity) | 设置全局触发器SOUND_ENTITY非数组 组变量 |
| [set_trigger_list_variable_audio_key](#set_trigger_list_variable_audio_key) | 设置全局触发器AUDIO_KEY数组变量子项 |
| [set_trigger_list_actor_variable_audio_key](#set_trigger_list_actor_variable_audio_key) | 设置全局触发器AUDIO_KEY数组 组变量子项 |
| [set_trigger_variable_audio_key](#set_trigger_variable_audio_key) | 设置全局触发器AUDIO_KEY非数组变量 |
| [set_trigger_actor_variable_audio_key](#set_trigger_actor_variable_audio_key) | 设置全局触发器AUDIO_KEY非数组 组变量 |
| [set_trigger_list_variable_game_mode](#set_trigger_list_variable_game_mode) | 设置全局触发器GAME_MODE数组变量子项 |
| [set_trigger_list_actor_variable_game_mode](#set_trigger_list_actor_variable_game_mode) | 设置全局触发器GAME_MODE数组 组变量子项 |
| [set_trigger_variable_game_mode](#set_trigger_variable_game_mode) | 设置全局触发器GAME_MODE非数组变量 |
| [set_trigger_actor_variable_game_mode](#set_trigger_actor_variable_game_mode) | 设置全局触发器GAME_MODE非数组 组变量 |
| [set_trigger_list_variable_player](#set_trigger_list_variable_player) | 设置全局触发器PLAYER数组变量子项 |
| [set_trigger_list_actor_variable_player](#set_trigger_list_actor_variable_player) | 设置全局触发器PLAYER数组 组变量子项 |
| [set_trigger_variable_player](#set_trigger_variable_player) | 设置全局触发器PLAYER非数组变量 |
| [set_trigger_actor_variable_player](#set_trigger_actor_variable_player) | 设置全局触发器PLAYER非数组 组变量 |
| [set_trigger_list_variable_player_group](#set_trigger_list_variable_player_group) | 设置全局触发器PLAYER_GROUP数组变量子项 |
| [set_trigger_list_actor_variable_player_group](#set_trigger_list_actor_variable_player_group) | 设置全局触发器PLAYER_GROUP数组 组变量子项 |
| [set_trigger_variable_player_group](#set_trigger_variable_player_group) | 设置全局触发器PLAYER_GROUP非数组变量 |
| [set_trigger_actor_variable_player_group](#set_trigger_actor_variable_player_group) | 设置全局触发器PLAYER_GROUP非数组 组变量 |
| [set_trigger_list_variable_role_res_key](#set_trigger_list_variable_role_res_key) | 设置全局触发器ROLE_RES_KEY数组变量子项 |
| [set_trigger_list_actor_variable_role_res_key](#set_trigger_list_actor_variable_role_res_key) | 设置全局触发器ROLE_RES_KEY数组 组变量子项 |
| [set_trigger_variable_role_res_key](#set_trigger_variable_role_res_key) | 设置全局触发器ROLE_RES_KEY非数组变量 |
| [set_trigger_actor_variable_role_res_key](#set_trigger_actor_variable_role_res_key) | 设置全局触发器ROLE_RES_KEY非数组 组变量 |
| [set_trigger_list_variable_role_status](#set_trigger_list_variable_role_status) | 设置全局触发器ROLE_STATUS数组变量子项 |
| [set_trigger_list_actor_variable_role_status](#set_trigger_list_actor_variable_role_status) | 设置全局触发器ROLE_STATUS数组 组变量子项 |
| [set_trigger_variable_role_status](#set_trigger_variable_role_status) | 设置全局触发器ROLE_STATUS非数组变量 |
| [set_trigger_actor_variable_role_status](#set_trigger_actor_variable_role_status) | 设置全局触发器ROLE_STATUS非数组 组变量 |
| [set_trigger_list_variable_role_type](#set_trigger_list_variable_role_type) | 设置全局触发器ROLE_TYPE数组变量子项 |
| [set_trigger_list_actor_variable_role_type](#set_trigger_list_actor_variable_role_type) | 设置全局触发器ROLE_TYPE数组 组变量子项 |
| [set_trigger_variable_role_type](#set_trigger_variable_role_type) | 设置全局触发器ROLE_TYPE非数组变量 |
| [set_trigger_actor_variable_role_type](#set_trigger_actor_variable_role_type) | 设置全局触发器ROLE_TYPE非数组 组变量 |
| [set_trigger_list_variable_team](#set_trigger_list_variable_team) | 设置全局触发器TEAM数组变量子项 |
| [set_trigger_list_actor_variable_team](#set_trigger_list_actor_variable_team) | 设置全局触发器TEAM数组 组变量子项 |
| [set_trigger_variable_team](#set_trigger_variable_team) | 设置全局触发器TEAM非数组变量 |
| [set_trigger_actor_variable_team](#set_trigger_actor_variable_team) | 设置全局触发器TEAM非数组 组变量 |
| [set_trigger_list_variable_point](#set_trigger_list_variable_point) | 设置全局触发器POINT数组变量子项 |
| [set_trigger_list_actor_variable_point](#set_trigger_list_actor_variable_point) | 设置全局触发器POINT数组 组变量子项 |
| [set_trigger_variable_point](#set_trigger_variable_point) | 设置全局触发器POINT非数组变量 |
| [set_trigger_actor_variable_point](#set_trigger_actor_variable_point) | 设置全局触发器POINT非数组 组变量 |
| [set_trigger_list_variable_vector3](#set_trigger_list_variable_vector3) | 设置全局触发器VECTOR3数组变量子项 |
| [set_trigger_list_actor_variable_vector3](#set_trigger_list_actor_variable_vector3) | 设置全局触发器VECTOR3数组 组变量子项 |
| [set_trigger_variable_vector3](#set_trigger_variable_vector3) | 设置全局触发器VECTOR3非数组变量 |
| [set_trigger_actor_variable_vector3](#set_trigger_actor_variable_vector3) | 设置全局触发器VECTOR3非数组 组变量 |
| [set_trigger_list_variable_rotation](#set_trigger_list_variable_rotation) | 设置全局触发器ROTATION数组变量子项 |
| [set_trigger_list_actor_variable_rotation](#set_trigger_list_actor_variable_rotation) | 设置全局触发器ROTATION数组 组变量子项 |
| [set_trigger_variable_rotation](#set_trigger_variable_rotation) | 设置全局触发器ROTATION非数组变量 |
| [set_trigger_actor_variable_rotation](#set_trigger_actor_variable_rotation) | 设置全局触发器ROTATION非数组 组变量 |
| [set_trigger_list_variable_point_list](#set_trigger_list_variable_point_list) | 设置全局触发器POINT_LIST数组变量子项 |
| [set_trigger_list_actor_variable_point_list](#set_trigger_list_actor_variable_point_list) | 设置全局触发器POINT_LIST数组 组变量子项 |
| [set_trigger_variable_point_list](#set_trigger_variable_point_list) | 设置全局触发器POINT_LIST非数组变量 |
| [set_trigger_actor_variable_point_list](#set_trigger_actor_variable_point_list) | 设置全局触发器POINT_LIST非数组 组变量 |
| [set_trigger_list_variable_road_group](#set_trigger_list_variable_road_group) | 设置全局触发器ROAD_GROUP数组变量子项 |
| [set_trigger_list_actor_variable_road_group](#set_trigger_list_actor_variable_road_group) | 设置全局触发器ROAD_GROUP数组 组变量子项 |
| [set_trigger_variable_road_group](#set_trigger_variable_road_group) | 设置全局触发器ROAD_GROUP非数组变量 |
| [set_trigger_actor_variable_road_group](#set_trigger_actor_variable_road_group) | 设置全局触发器ROAD_GROUP非数组 组变量 |
| [set_trigger_list_variable_rectangle](#set_trigger_list_variable_rectangle) | 设置全局触发器RECTANGLE数组变量子项 |
| [set_trigger_list_actor_variable_rectangle](#set_trigger_list_actor_variable_rectangle) | 设置全局触发器RECTANGLE数组 组变量子项 |
| [set_trigger_variable_rectangle](#set_trigger_variable_rectangle) | 设置全局触发器RECTANGLE非数组变量 |
| [set_trigger_actor_variable_rectangle](#set_trigger_actor_variable_rectangle) | 设置全局触发器RECTANGLE非数组 组变量 |
| [set_trigger_list_variable_round_area](#set_trigger_list_variable_round_area) | 设置全局触发器ROUND_AREA数组变量子项 |
| [set_trigger_list_actor_variable_round_area](#set_trigger_list_actor_variable_round_area) | 设置全局触发器ROUND_AREA数组 组变量子项 |
| [set_trigger_variable_round_area](#set_trigger_variable_round_area) | 设置全局触发器ROUND_AREA非数组变量 |
| [set_trigger_actor_variable_round_area](#set_trigger_actor_variable_round_area) | 设置全局触发器ROUND_AREA非数组 组变量 |
| [set_trigger_list_variable_polygon](#set_trigger_list_variable_polygon) | 设置全局触发器POLYGON数组变量子项 |
| [set_trigger_list_actor_variable_polygon](#set_trigger_list_actor_variable_polygon) | 设置全局触发器POLYGON数组 组变量子项 |
| [set_trigger_variable_polygon](#set_trigger_variable_polygon) | 设置全局触发器POLYGON非数组变量 |
| [set_trigger_actor_variable_polygon](#set_trigger_actor_variable_polygon) | 设置全局触发器POLYGON非数组 组变量 |
| [set_trigger_list_variable_camera](#set_trigger_list_variable_camera) | 设置全局触发器CAMERA数组变量子项 |
| [set_trigger_list_actor_variable_camera](#set_trigger_list_actor_variable_camera) | 设置全局触发器CAMERA数组 组变量子项 |
| [set_trigger_variable_camera](#set_trigger_variable_camera) | 设置全局触发器CAMERA非数组变量 |
| [set_trigger_actor_variable_camera](#set_trigger_actor_variable_camera) | 设置全局触发器CAMERA非数组 组变量 |
| [set_trigger_list_variable_camline](#set_trigger_list_variable_camline) | 设置全局触发器CAMLINE数组变量子项 |
| [set_trigger_list_actor_variable_camline](#set_trigger_list_actor_variable_camline) | 设置全局触发器CAMLINE数组 组变量子项 |
| [set_trigger_variable_camline](#set_trigger_variable_camline) | 设置全局触发器CAMLINE非数组变量 |
| [set_trigger_actor_variable_camline](#set_trigger_actor_variable_camline) | 设置全局触发器CAMLINE非数组 组变量 |
| [set_trigger_list_variable_point_light](#set_trigger_list_variable_point_light) | 设置全局触发器POINT_LIGHT数组变量子项 |
| [set_trigger_list_actor_variable_point_light](#set_trigger_list_actor_variable_point_light) | 设置全局触发器POINT_LIGHT数组 组变量子项 |
| [set_trigger_variable_point_light](#set_trigger_variable_point_light) | 设置全局触发器POINT_LIGHT非数组变量 |
| [set_trigger_actor_variable_point_light](#set_trigger_actor_variable_point_light) | 设置全局触发器POINT_LIGHT非数组 组变量 |
| [set_trigger_list_variable_spot_light](#set_trigger_list_variable_spot_light) | 设置全局触发器SPOT_LIGHT数组变量子项 |
| [set_trigger_list_actor_variable_spot_light](#set_trigger_list_actor_variable_spot_light) | 设置全局触发器SPOT_LIGHT数组 组变量子项 |
| [set_trigger_variable_spot_light](#set_trigger_variable_spot_light) | 设置全局触发器SPOT_LIGHT非数组变量 |
| [set_trigger_actor_variable_spot_light](#set_trigger_actor_variable_spot_light) | 设置全局触发器SPOT_LIGHT非数组 组变量 |
| [set_trigger_list_variable_fog](#set_trigger_list_variable_fog) | 设置全局触发器FOG数组变量子项 |
| [set_trigger_list_actor_variable_fog](#set_trigger_list_actor_variable_fog) | 设置全局触发器FOG数组 组变量子项 |
| [set_trigger_variable_fog](#set_trigger_variable_fog) | 设置全局触发器FOG非数组变量 |
| [set_trigger_actor_variable_fog](#set_trigger_actor_variable_fog) | 设置全局触发器FOG非数组 组变量 |
| [set_trigger_list_variable_model](#set_trigger_list_variable_model) | 设置全局触发器MODEL数组变量子项 |
| [set_trigger_list_actor_variable_model](#set_trigger_list_actor_variable_model) | 设置全局触发器MODEL数组 组变量子项 |
| [set_trigger_variable_model](#set_trigger_variable_model) | 设置全局触发器MODEL非数组变量 |
| [set_trigger_actor_variable_model](#set_trigger_actor_variable_model) | 设置全局触发器MODEL非数组 组变量 |
| [set_trigger_list_variable_sfx_entity](#set_trigger_list_variable_sfx_entity) | 设置全局触发器SFX_ENTITY数组变量子项 |
| [set_trigger_list_actor_variable_sfx_entity](#set_trigger_list_actor_variable_sfx_entity) | 设置全局触发器SFX_ENTITY数组 组变量子项 |
| [set_trigger_variable_sfx_entity](#set_trigger_variable_sfx_entity) | 设置全局触发器SFX_ENTITY非数组变量 |
| [set_trigger_actor_variable_sfx_entity](#set_trigger_actor_variable_sfx_entity) | 设置全局触发器SFX_ENTITY非数组 组变量 |
| [set_trigger_list_variable_sfx_key](#set_trigger_list_variable_sfx_key) | 设置全局触发器SFX_KEY数组变量子项 |
| [set_trigger_list_actor_variable_sfx_key](#set_trigger_list_actor_variable_sfx_key) | 设置全局触发器SFX_KEY数组 组变量子项 |
| [set_trigger_variable_sfx_key](#set_trigger_variable_sfx_key) | 设置全局触发器SFX_KEY非数组变量 |
| [set_trigger_actor_variable_sfx_key](#set_trigger_actor_variable_sfx_key) | 设置全局触发器SFX_KEY非数组 组变量 |
| [set_trigger_list_variable_link_sfx_entity](#set_trigger_list_variable_link_sfx_entity) | 设置全局触发器LINK_SFX_ENTITY数组变量子项 |
| [set_trigger_list_actor_variable_link_sfx_entity](#set_trigger_list_actor_variable_link_sfx_entity) | 设置全局触发器LINK_SFX_ENTITY数组 组变量子项 |
| [set_trigger_variable_link_sfx_entity](#set_trigger_variable_link_sfx_entity) | 设置全局触发器LINK_SFX_ENTITY非数组变量 |
| [set_trigger_actor_variable_link_sfx_entity](#set_trigger_actor_variable_link_sfx_entity) | 设置全局触发器LINK_SFX_ENTITY非数组 组变量 |
| [set_trigger_list_variable_link_sfx_key](#set_trigger_list_variable_link_sfx_key) | 设置全局触发器LINK_SFX_KEY数组变量子项 |
| [set_trigger_list_actor_variable_link_sfx_key](#set_trigger_list_actor_variable_link_sfx_key) | 设置全局触发器LINK_SFX_KEY数组 组变量子项 |
| [set_trigger_variable_link_sfx_key](#set_trigger_variable_link_sfx_key) | 设置全局触发器LINK_SFX_KEY非数组变量 |
| [set_trigger_actor_variable_link_sfx_key](#set_trigger_actor_variable_link_sfx_key) | 设置全局触发器LINK_SFX_KEY非数组 组变量 |
| [set_trigger_list_variable_cursor_key](#set_trigger_list_variable_cursor_key) | 设置全局触发器CURSOR_KEY数组变量子项 |
| [set_trigger_list_actor_variable_cursor_key](#set_trigger_list_actor_variable_cursor_key) | 设置全局触发器CURSOR_KEY数组 组变量子项 |
| [set_trigger_variable_cursor_key](#set_trigger_variable_cursor_key) | 设置全局触发器CURSOR_KEY非数组变量 |
| [set_trigger_actor_variable_cursor_key](#set_trigger_actor_variable_cursor_key) | 设置全局触发器CURSOR_KEY非数组 组变量 |
| [set_trigger_list_variable_image_key](#set_trigger_list_variable_image_key) | 设置全局触发器IMAGE_KEY数组变量子项 |
| [set_trigger_list_actor_variable_image_key](#set_trigger_list_actor_variable_image_key) | 设置全局触发器IMAGE_KEY数组 组变量子项 |
| [set_trigger_variable_image_key](#set_trigger_variable_image_key) | 设置全局触发器IMAGE_KEY非数组变量 |
| [set_trigger_actor_variable_image_key](#set_trigger_actor_variable_image_key) | 设置全局触发器IMAGE_KEY非数组 组变量 |
| [set_trigger_list_variable_angle](#set_trigger_list_variable_angle) | 设置全局触发器ANGLE数组变量子项 |
| [set_trigger_list_actor_variable_angle](#set_trigger_list_actor_variable_angle) | 设置全局触发器ANGLE数组 组变量子项 |
| [set_trigger_variable_angle](#set_trigger_variable_angle) | 设置全局触发器ANGLE非数组变量 |
| [set_trigger_actor_variable_angle](#set_trigger_actor_variable_angle) | 设置全局触发器ANGLE非数组 组变量 |
| [set_trigger_list_variable_texture](#set_trigger_list_variable_texture) | 设置全局触发器TEXTURE数组变量子项 |
| [set_trigger_list_actor_variable_texture](#set_trigger_list_actor_variable_texture) | 设置全局触发器TEXTURE数组 组变量子项 |
| [set_trigger_variable_texture](#set_trigger_variable_texture) | 设置全局触发器TEXTURE非数组变量 |
| [set_trigger_actor_variable_texture](#set_trigger_actor_variable_texture) | 设置全局触发器TEXTURE非数组 组变量 |
| [set_trigger_list_variable_sequence](#set_trigger_list_variable_sequence) | 设置全局触发器SEQUENCE数组变量子项 |
| [set_trigger_list_actor_variable_sequence](#set_trigger_list_actor_variable_sequence) | 设置全局触发器SEQUENCE数组 组变量子项 |
| [set_trigger_variable_sequence](#set_trigger_variable_sequence) | 设置全局触发器SEQUENCE非数组变量 |
| [set_trigger_actor_variable_sequence](#set_trigger_actor_variable_sequence) | 设置全局触发器SEQUENCE非数组 组变量 |
| [set_trigger_list_variable_physics_object](#set_trigger_list_variable_physics_object) | 设置全局触发器PHYSICS_OBJECT数组变量子项 |
| [set_trigger_list_actor_variable_physics_object](#set_trigger_list_actor_variable_physics_object) | 设置全局触发器PHYSICS_OBJECT数组 组变量子项 |
| [set_trigger_variable_physics_object](#set_trigger_variable_physics_object) | 设置全局触发器PHYSICS_OBJECT非数组变量 |
| [set_trigger_actor_variable_physics_object](#set_trigger_actor_variable_physics_object) | 设置全局触发器PHYSICS_OBJECT非数组 组变量 |
| [set_trigger_list_variable_physics_entity](#set_trigger_list_variable_physics_entity) | 设置全局触发器PHYSICS_ENTITY数组变量子项 |
| [set_trigger_list_actor_variable_physics_entity](#set_trigger_list_actor_variable_physics_entity) | 设置全局触发器PHYSICS_ENTITY数组 组变量子项 |
| [set_trigger_variable_physics_entity](#set_trigger_variable_physics_entity) | 设置全局触发器PHYSICS_ENTITY非数组变量 |
| [set_trigger_actor_variable_physics_entity](#set_trigger_actor_variable_physics_entity) | 设置全局触发器PHYSICS_ENTITY非数组 组变量 |
| [set_trigger_list_variable_physics_object_key](#set_trigger_list_variable_physics_object_key) | 设置全局触发器PHYSICS_OBJECT_KEY数组变量子项 |
| [set_trigger_list_actor_variable_physics_object_key](#set_trigger_list_actor_variable_physics_object_key) | 设置全局触发器PHYSICS_OBJECT_KEY数组 组变量子项 |
| [set_trigger_variable_physics_object_key](#set_trigger_variable_physics_object_key) | 设置全局触发器PHYSICS_OBJECT_KEY非数组变量 |
| [set_trigger_actor_variable_physics_object_key](#set_trigger_actor_variable_physics_object_key) | 设置全局触发器PHYSICS_OBJECT_KEY非数组 组变量 |
| [set_trigger_list_variable_physics_entity_key](#set_trigger_list_variable_physics_entity_key) | 设置全局触发器PHYSICS_ENTITY_KEY数组变量子项 |
| [set_trigger_list_actor_variable_physics_entity_key](#set_trigger_list_actor_variable_physics_entity_key) | 设置全局触发器PHYSICS_ENTITY_KEY数组 组变量子项 |
| [set_trigger_variable_physics_entity_key](#set_trigger_variable_physics_entity_key) | 设置全局触发器PHYSICS_ENTITY_KEY非数组变量 |
| [set_trigger_actor_variable_physics_entity_key](#set_trigger_actor_variable_physics_entity_key) | 设置全局触发器PHYSICS_ENTITY_KEY非数组 组变量 |
| [set_trigger_list_variable_rigid_body](#set_trigger_list_variable_rigid_body) | 设置全局触发器RIGID_BODY数组变量子项 |
| [set_trigger_list_actor_variable_rigid_body](#set_trigger_list_actor_variable_rigid_body) | 设置全局触发器RIGID_BODY数组 组变量子项 |
| [set_trigger_variable_rigid_body](#set_trigger_variable_rigid_body) | 设置全局触发器RIGID_BODY非数组变量 |
| [set_trigger_actor_variable_rigid_body](#set_trigger_actor_variable_rigid_body) | 设置全局触发器RIGID_BODY非数组 组变量 |
| [set_trigger_list_variable_rigid_body_group](#set_trigger_list_variable_rigid_body_group) | 设置全局触发器RIGID_BODY_GROUP数组变量子项 |
| [set_trigger_list_actor_variable_rigid_body_group](#set_trigger_list_actor_variable_rigid_body_group) | 设置全局触发器RIGID_BODY_GROUP数组 组变量子项 |
| [set_trigger_variable_rigid_body_group](#set_trigger_variable_rigid_body_group) | 设置全局触发器RIGID_BODY_GROUP非数组变量 |
| [set_trigger_actor_variable_rigid_body_group](#set_trigger_actor_variable_rigid_body_group) | 设置全局触发器RIGID_BODY_GROUP非数组 组变量 |
| [set_trigger_list_variable_collider](#set_trigger_list_variable_collider) | 设置全局触发器COLLIDER数组变量子项 |
| [set_trigger_list_actor_variable_collider](#set_trigger_list_actor_variable_collider) | 设置全局触发器COLLIDER数组 组变量子项 |
| [set_trigger_variable_collider](#set_trigger_variable_collider) | 设置全局触发器COLLIDER非数组变量 |
| [set_trigger_actor_variable_collider](#set_trigger_actor_variable_collider) | 设置全局触发器COLLIDER非数组 组变量 |
| [set_trigger_list_variable_joint](#set_trigger_list_variable_joint) | 设置全局触发器JOINT数组变量子项 |
| [has_ability_key_rescue_seeker_type_kv](#has_ability_key_rescue_seeker_type_kv) | 判断技能编号是否存在RESCUE_SEEKER_TYPE键值对 |
| [has_kv_pair_rescuer_type](#has_kv_pair_rescuer_type) | 判断是否存在RESCUER_TYPE键值对 |
| [has_prefab_rescuer_type_kv](#has_prefab_rescuer_type_kv) | 判断预设是否存在RESCUER_TYPE键值对 |
| [has_unit_key_rescuer_type_kv](#has_unit_key_rescuer_type_kv) | 判断单位编号是否存在RESCUER_TYPE键值对 |
| [has_item_key_rescuer_type_kv](#has_item_key_rescuer_type_kv) | 判断物品编号是否存在RESCUER_TYPE键值对 |
| [has_ability_key_rescuer_type_kv](#has_ability_key_rescuer_type_kv) | 判断技能编号是否存在RESCUER_TYPE键值对 |
| [has_kv_pair_store_item_type](#has_kv_pair_store_item_type) | 判断是否存在STORE_ITEM_TYPE键值对 |
| [has_prefab_store_item_type_kv](#has_prefab_store_item_type_kv) | 判断预设是否存在STORE_ITEM_TYPE键值对 |
| [has_unit_key_store_item_type_kv](#has_unit_key_store_item_type_kv) | 判断单位编号是否存在STORE_ITEM_TYPE键值对 |
| [has_item_key_store_item_type_kv](#has_item_key_store_item_type_kv) | 判断物品编号是否存在STORE_ITEM_TYPE键值对 |
| [has_ability_key_store_item_type_kv](#has_ability_key_store_item_type_kv) | 判断技能编号是否存在STORE_ITEM_TYPE键值对 |
| [has_kv_pair_site_state](#has_kv_pair_site_state) | 判断是否存在SITE_STATE键值对 |
| [has_prefab_site_state_kv](#has_prefab_site_state_kv) | 判断预设是否存在SITE_STATE键值对 |
| [has_unit_key_site_state_kv](#has_unit_key_site_state_kv) | 判断单位编号是否存在SITE_STATE键值对 |
| [has_item_key_site_state_kv](#has_item_key_site_state_kv) | 判断物品编号是否存在SITE_STATE键值对 |
| [has_ability_key_site_state_kv](#has_ability_key_site_state_kv) | 判断技能编号是否存在SITE_STATE键值对 |
| [has_kv_pair_coin_currency](#has_kv_pair_coin_currency) | 判断是否存在COIN_CURRENCY键值对 |
| [has_prefab_coin_currency_kv](#has_prefab_coin_currency_kv) | 判断预设是否存在COIN_CURRENCY键值对 |
| [has_unit_key_coin_currency_kv](#has_unit_key_coin_currency_kv) | 判断单位编号是否存在COIN_CURRENCY键值对 |
| [has_item_key_coin_currency_kv](#has_item_key_coin_currency_kv) | 判断物品编号是否存在COIN_CURRENCY键值对 |
| [has_ability_key_coin_currency_kv](#has_ability_key_coin_currency_kv) | 判断技能编号是否存在COIN_CURRENCY键值对 |
| [api_serialize_kv](#api_serialize_kv) | 序列化KV |
| [api_deserialize_kv](#api_deserialize_kv) | 反序列化KV |
| [get_unit_key_xxx_kv](#get_unit_key_xxx_kv) | 获取单位编号键值对 |
| [get_item_key_xxx_kv](#get_item_key_xxx_kv) | 获取物品编号键值对 |
| [get_ability_key_xxx_kv](#get_ability_key_xxx_kv) | 获取技能编号键值对 |
| [get_modifier_key_xxx_kv](#get_modifier_key_xxx_kv) | 获取魔法效果特效编号键值对 |
| [get_projectile_key_xxx_kv](#get_projectile_key_xxx_kv) | 获取特效编号键值对 |
| [get_destructible_key_xxx_kv](#get_destructible_key_xxx_kv) | 获取可破坏物编号键值对 |
| [get_tech_key_xxx_kv](#get_tech_key_xxx_kv) | 获取科技编号键值对 |
| [get_icon_id_xxx_kv](#get_icon_id_xxx_kv) | 获取图片键值对 |
| [get_physics_entity_key_xxx_kv](#get_physics_entity_key_xxx_kv) | 获取逻辑物理组件类型键值对 |
| [get_entity_ckv_pair_value_xxx](#get_entity_ckv_pair_value_xxx) | 获取值对 |
| [get_ability_ckv_pair_value_xxx](#get_ability_ckv_pair_value_xxx) | 获取值对 |
| [get_modifier_ckv_pair_value_xxx](#get_modifier_ckv_pair_value_xxx) | 获取值对 |
| [get_unit_key_ui_gridview_type_kv](#get_unit_key_ui_gridview_type_kv) | 获取单位编号UI_GRIDVIEW_TYPE键值对 |
| [get_item_key_ui_gridview_type_kv](#get_item_key_ui_gridview_type_kv) | 获取物品编号UI_GRIDVIEW_TYPE键值对 |
| [get_ability_key_ui_gridview_type_kv](#get_ability_key_ui_gridview_type_kv) | 获取技能编号UI_GRIDVIEW_TYPE键值对 |
| [get_modifier_key_ui_gridview_type_kv](#get_modifier_key_ui_gridview_type_kv) | 获取魔法效果特效编号UI_GRIDVIEW_TYPE键值对 |
| [get_projectile_key_ui_gridview_type_kv](#get_projectile_key_ui_gridview_type_kv) | 获取特效编号UI_GRIDVIEW_TYPE键值对 |
| [get_destructible_key_ui_gridview_type_kv](#get_destructible_key_ui_gridview_type_kv) | 获取可破坏物编号UI_GRIDVIEW_TYPE键值对 |
| [get_tech_key_ui_gridview_type_kv](#get_tech_key_ui_gridview_type_kv) | 获取科技编号UI_GRIDVIEW_TYPE键值对 |
| [get_icon_id_ui_gridview_type_kv](#get_icon_id_ui_gridview_type_kv) | 获取图片UI_GRIDVIEW_TYPE键值对 |
| [get_physics_entity_key_ui_gridview_type_kv](#get_physics_entity_key_ui_gridview_type_kv) | 获取逻辑物理组件类型UI_GRIDVIEW_TYPE键值对 |
| [get_kv_pair_value_ui_gridview_type](#get_kv_pair_value_ui_gridview_type) | 获取UI_GRIDVIEW_TYPE键值对 |
| [get_unit_key_ui_gridview_bar_type_kv](#get_unit_key_ui_gridview_bar_type_kv) | 获取单位编号UI_GRIDVIEW_BAR_TYPE键值对 |
| [get_item_key_ui_gridview_bar_type_kv](#get_item_key_ui_gridview_bar_type_kv) | 获取物品编号UI_GRIDVIEW_BAR_TYPE键值对 |
| [get_ability_key_ui_gridview_bar_type_kv](#get_ability_key_ui_gridview_bar_type_kv) | 获取技能编号UI_GRIDVIEW_BAR_TYPE键值对 |
| [get_modifier_key_ui_gridview_bar_type_kv](#get_modifier_key_ui_gridview_bar_type_kv) | 获取魔法效果特效编号UI_GRIDVIEW_BAR_TYPE键值对 |
| [get_projectile_key_ui_gridview_bar_type_kv](#get_projectile_key_ui_gridview_bar_type_kv) | 获取特效编号UI_GRIDVIEW_BAR_TYPE键值对 |
| [get_destructible_key_ui_gridview_bar_type_kv](#get_destructible_key_ui_gridview_bar_type_kv) | 获取可破坏物编号UI_GRIDVIEW_BAR_TYPE键值对 |
| [get_tech_key_ui_gridview_bar_type_kv](#get_tech_key_ui_gridview_bar_type_kv) | 获取科技编号UI_GRIDVIEW_BAR_TYPE键值对 |
| [get_icon_id_ui_gridview_bar_type_kv](#get_icon_id_ui_gridview_bar_type_kv) | 获取图片UI_GRIDVIEW_BAR_TYPE键值对 |
| [get_physics_entity_key_ui_gridview_bar_type_kv](#get_physics_entity_key_ui_gridview_bar_type_kv) | 获取逻辑物理组件类型UI_GRIDVIEW_BAR_TYPE键值对 |
| [get_kv_pair_value_ui_gridview_bar_type](#get_kv_pair_value_ui_gridview_bar_type) | 获取UI_GRIDVIEW_BAR_TYPE键值对 |
| [get_unit_key_ui_effect_camera_mode_kv](#get_unit_key_ui_effect_camera_mode_kv) | 获取单位编号UI_EFFECT_CAMERA_MODE键值对 |
| [get_item_key_ui_effect_camera_mode_kv](#get_item_key_ui_effect_camera_mode_kv) | 获取物品编号UI_EFFECT_CAMERA_MODE键值对 |
| [get_ability_key_ui_effect_camera_mode_kv](#get_ability_key_ui_effect_camera_mode_kv) | 获取技能编号UI_EFFECT_CAMERA_MODE键值对 |
| [get_modifier_key_ui_effect_camera_mode_kv](#get_modifier_key_ui_effect_camera_mode_kv) | 获取魔法效果特效编号UI_EFFECT_CAMERA_MODE键值对 |
| [get_projectile_key_ui_effect_camera_mode_kv](#get_projectile_key_ui_effect_camera_mode_kv) | 获取特效编号UI_EFFECT_CAMERA_MODE键值对 |
| [get_destructible_key_ui_effect_camera_mode_kv](#get_destructible_key_ui_effect_camera_mode_kv) | 获取可破坏物编号UI_EFFECT_CAMERA_MODE键值对 |
| [get_tech_key_ui_effect_camera_mode_kv](#get_tech_key_ui_effect_camera_mode_kv) | 获取科技编号UI_EFFECT_CAMERA_MODE键值对 |
| [get_icon_id_ui_effect_camera_mode_kv](#get_icon_id_ui_effect_camera_mode_kv) | 获取图片UI_EFFECT_CAMERA_MODE键值对 |
| [get_physics_entity_key_ui_effect_camera_mode_kv](#get_physics_entity_key_ui_effect_camera_mode_kv) | 获取逻辑物理组件类型UI_EFFECT_CAMERA_MODE键值对 |
| [get_kv_pair_value_ui_effect_camera_mode](#get_kv_pair_value_ui_effect_camera_mode) | 获取UI_EFFECT_CAMERA_MODE键值对 |
| [get_unit_key_ui_equip_slot_use_type_kv](#get_unit_key_ui_equip_slot_use_type_kv) | 获取单位编号UI_EQUIP_SLOT_USE_TYPE键值对 |
| [get_item_key_ui_equip_slot_use_type_kv](#get_item_key_ui_equip_slot_use_type_kv) | 获取物品编号UI_EQUIP_SLOT_USE_TYPE键值对 |
| [get_ability_key_ui_equip_slot_use_type_kv](#get_ability_key_ui_equip_slot_use_type_kv) | 获取技能编号UI_EQUIP_SLOT_USE_TYPE键值对 |
| [get_modifier_key_ui_equip_slot_use_type_kv](#get_modifier_key_ui_equip_slot_use_type_kv) | 获取魔法效果特效编号UI_EQUIP_SLOT_USE_TYPE键值对 |
| [get_projectile_key_ui_equip_slot_use_type_kv](#get_projectile_key_ui_equip_slot_use_type_kv) | 获取特效编号UI_EQUIP_SLOT_USE_TYPE键值对 |
| [get_destructible_key_ui_equip_slot_use_type_kv](#get_destructible_key_ui_equip_slot_use_type_kv) | 获取可破坏物编号UI_EQUIP_SLOT_USE_TYPE键值对 |
| [get_tech_key_ui_equip_slot_use_type_kv](#get_tech_key_ui_equip_slot_use_type_kv) | 获取科技编号UI_EQUIP_SLOT_USE_TYPE键值对 |
| [get_icon_id_ui_equip_slot_use_type_kv](#get_icon_id_ui_equip_slot_use_type_kv) | 获取图片UI_EQUIP_SLOT_USE_TYPE键值对 |
| [get_physics_entity_key_ui_equip_slot_use_type_kv](#get_physics_entity_key_ui_equip_slot_use_type_kv) | 获取逻辑物理组件类型UI_EQUIP_SLOT_USE_TYPE键值对 |
| [get_kv_pair_value_ui_equip_slot_use_type](#get_kv_pair_value_ui_equip_slot_use_type) | 获取UI_EQUIP_SLOT_USE_TYPE键值对 |
| [get_unit_key_ui_equip_slot_drag_type_kv](#get_unit_key_ui_equip_slot_drag_type_kv) | 获取单位编号UI_EQUIP_SLOT_DRAG_TYPE键值对 |
| [get_item_key_ui_equip_slot_drag_type_kv](#get_item_key_ui_equip_slot_drag_type_kv) | 获取物品编号UI_EQUIP_SLOT_DRAG_TYPE键值对 |
| [get_ability_key_ui_equip_slot_drag_type_kv](#get_ability_key_ui_equip_slot_drag_type_kv) | 获取技能编号UI_EQUIP_SLOT_DRAG_TYPE键值对 |
| [get_modifier_key_ui_equip_slot_drag_type_kv](#get_modifier_key_ui_equip_slot_drag_type_kv) | 获取魔法效果特效编号UI_EQUIP_SLOT_DRAG_TYPE键值对 |
| [get_projectile_key_ui_equip_slot_drag_type_kv](#get_projectile_key_ui_equip_slot_drag_type_kv) | 获取特效编号UI_EQUIP_SLOT_DRAG_TYPE键值对 |
| [get_destructible_key_ui_equip_slot_drag_type_kv](#get_destructible_key_ui_equip_slot_drag_type_kv) | 获取可破坏物编号UI_EQUIP_SLOT_DRAG_TYPE键值对 |
| [get_tech_key_ui_equip_slot_drag_type_kv](#get_tech_key_ui_equip_slot_drag_type_kv) | 获取科技编号UI_EQUIP_SLOT_DRAG_TYPE键值对 |
| [get_icon_id_ui_equip_slot_drag_type_kv](#get_icon_id_ui_equip_slot_drag_type_kv) | 获取图片UI_EQUIP_SLOT_DRAG_TYPE键值对 |
| [get_physics_entity_key_ui_equip_slot_drag_type_kv](#get_physics_entity_key_ui_equip_slot_drag_type_kv) | 获取逻辑物理组件类型UI_EQUIP_SLOT_DRAG_TYPE键值对 |
| [get_kv_pair_value_ui_equip_slot_drag_type](#get_kv_pair_value_ui_equip_slot_drag_type) | 获取UI_EQUIP_SLOT_DRAG_TYPE键值对 |
| [get_unit_key_ui_layout_clipping_type_kv](#get_unit_key_ui_layout_clipping_type_kv) | 获取单位编号UI_LAYOUT_CLIPPING_TYPE键值对 |
| [get_item_key_ui_layout_clipping_type_kv](#get_item_key_ui_layout_clipping_type_kv) | 获取物品编号UI_LAYOUT_CLIPPING_TYPE键值对 |
| [get_ability_key_ui_layout_clipping_type_kv](#get_ability_key_ui_layout_clipping_type_kv) | 获取技能编号UI_LAYOUT_CLIPPING_TYPE键值对 |
| [get_modifier_key_ui_layout_clipping_type_kv](#get_modifier_key_ui_layout_clipping_type_kv) | 获取魔法效果特效编号UI_LAYOUT_CLIPPING_TYPE键值对 |
| [get_projectile_key_ui_layout_clipping_type_kv](#get_projectile_key_ui_layout_clipping_type_kv) | 获取特效编号UI_LAYOUT_CLIPPING_TYPE键值对 |
| [get_destructible_key_ui_layout_clipping_type_kv](#get_destructible_key_ui_layout_clipping_type_kv) | 获取可破坏物编号UI_LAYOUT_CLIPPING_TYPE键值对 |
| [get_tech_key_ui_layout_clipping_type_kv](#get_tech_key_ui_layout_clipping_type_kv) | 获取科技编号UI_LAYOUT_CLIPPING_TYPE键值对 |
| [get_icon_id_ui_layout_clipping_type_kv](#get_icon_id_ui_layout_clipping_type_kv) | 获取图片UI_LAYOUT_CLIPPING_TYPE键值对 |
| [get_physics_entity_key_ui_layout_clipping_type_kv](#get_physics_entity_key_ui_layout_clipping_type_kv) | 获取逻辑物理组件类型UI_LAYOUT_CLIPPING_TYPE键值对 |
| [get_kv_pair_value_ui_layout_clipping_type](#get_kv_pair_value_ui_layout_clipping_type) | 获取UI_LAYOUT_CLIPPING_TYPE键值对 |
| [get_unit_key_ui_text_over_length_handling_type_kv](#get_unit_key_ui_text_over_length_handling_type_kv) | 获取单位编号UI_TEXT_OVER_LENGTH_HANDLING_TYPE键值对 |
| [get_item_key_ui_text_over_length_handling_type_kv](#get_item_key_ui_text_over_length_handling_type_kv) | 获取物品编号UI_TEXT_OVER_LENGTH_HANDLING_TYPE键值对 |
| [get_ability_key_ui_text_over_length_handling_type_kv](#get_ability_key_ui_text_over_length_handling_type_kv) | 获取技能编号UI_TEXT_OVER_LENGTH_HANDLING_TYPE键值对 |
| [get_modifier_key_ui_text_over_length_handling_type_kv](#get_modifier_key_ui_text_over_length_handling_type_kv) | 获取魔法效果特效编号UI_TEXT_OVER_LENGTH_HANDLING_TYPE键值对 |
| [get_projectile_key_ui_text_over_length_handling_type_kv](#get_projectile_key_ui_text_over_length_handling_type_kv) | 获取特效编号UI_TEXT_OVER_LENGTH_HANDLING_TYPE键值对 |
| [get_destructible_key_ui_text_over_length_handling_type_kv](#get_destructible_key_ui_text_over_length_handling_type_kv) | 获取可破坏物编号UI_TEXT_OVER_LENGTH_HANDLING_TYPE键值对 |
| [get_tech_key_ui_text_over_length_handling_type_kv](#get_tech_key_ui_text_over_length_handling_type_kv) | 获取科技编号UI_TEXT_OVER_LENGTH_HANDLING_TYPE键值对 |
| [get_icon_id_ui_text_over_length_handling_type_kv](#get_icon_id_ui_text_over_length_handling_type_kv) | 获取图片UI_TEXT_OVER_LENGTH_HANDLING_TYPE键值对 |
| [get_physics_entity_key_ui_text_over_length_handling_type_kv](#get_physics_entity_key_ui_text_over_length_handling_type_kv) | 获取逻辑物理组件类型UI_TEXT_OVER_LENGTH_HANDLING_TYPE键值对 |
| [get_kv_pair_value_ui_text_over_length_handling_type](#get_kv_pair_value_ui_text_over_length_handling_type) | 获取UI_TEXT_OVER_LENGTH_HANDLING_TYPE键值对 |
| [get_unit_key_ui_pos_adapt_mode_kv](#get_unit_key_ui_pos_adapt_mode_kv) | 获取单位编号UI_POS_ADAPT_MODE键值对 |
| [get_item_key_ui_pos_adapt_mode_kv](#get_item_key_ui_pos_adapt_mode_kv) | 获取物品编号UI_POS_ADAPT_MODE键值对 |
| [get_ability_key_ui_pos_adapt_mode_kv](#get_ability_key_ui_pos_adapt_mode_kv) | 获取技能编号UI_POS_ADAPT_MODE键值对 |
| [get_modifier_key_ui_pos_adapt_mode_kv](#get_modifier_key_ui_pos_adapt_mode_kv) | 获取魔法效果特效编号UI_POS_ADAPT_MODE键值对 |
| [get_projectile_key_ui_pos_adapt_mode_kv](#get_projectile_key_ui_pos_adapt_mode_kv) | 获取特效编号UI_POS_ADAPT_MODE键值对 |
| [get_destructible_key_ui_pos_adapt_mode_kv](#get_destructible_key_ui_pos_adapt_mode_kv) | 获取可破坏物编号UI_POS_ADAPT_MODE键值对 |
| [get_tech_key_ui_pos_adapt_mode_kv](#get_tech_key_ui_pos_adapt_mode_kv) | 获取科技编号UI_POS_ADAPT_MODE键值对 |
| [get_icon_id_ui_pos_adapt_mode_kv](#get_icon_id_ui_pos_adapt_mode_kv) | 获取图片UI_POS_ADAPT_MODE键值对 |
| [get_physics_entity_key_ui_pos_adapt_mode_kv](#get_physics_entity_key_ui_pos_adapt_mode_kv) | 获取逻辑物理组件类型UI_POS_ADAPT_MODE键值对 |
| [get_kv_pair_value_ui_pos_adapt_mode](#get_kv_pair_value_ui_pos_adapt_mode) | 获取UI_POS_ADAPT_MODE键值对 |
| [get_unit_key_ui_chat_send_channel_kv](#get_unit_key_ui_chat_send_channel_kv) | 获取单位编号UI_CHAT_SEND_CHANNEL键值对 |
| [get_item_key_ui_chat_send_channel_kv](#get_item_key_ui_chat_send_channel_kv) | 获取物品编号UI_CHAT_SEND_CHANNEL键值对 |
| [get_ability_key_ui_chat_send_channel_kv](#get_ability_key_ui_chat_send_channel_kv) | 获取技能编号UI_CHAT_SEND_CHANNEL键值对 |
| [get_modifier_key_ui_chat_send_channel_kv](#get_modifier_key_ui_chat_send_channel_kv) | 获取魔法效果特效编号UI_CHAT_SEND_CHANNEL键值对 |
| [get_projectile_key_ui_chat_send_channel_kv](#get_projectile_key_ui_chat_send_channel_kv) | 获取特效编号UI_CHAT_SEND_CHANNEL键值对 |
| [get_destructible_key_ui_chat_send_channel_kv](#get_destructible_key_ui_chat_send_channel_kv) | 获取可破坏物编号UI_CHAT_SEND_CHANNEL键值对 |
| [get_tech_key_ui_chat_send_channel_kv](#get_tech_key_ui_chat_send_channel_kv) | 获取科技编号UI_CHAT_SEND_CHANNEL键值对 |
| [get_icon_id_ui_chat_send_channel_kv](#get_icon_id_ui_chat_send_channel_kv) | 获取图片UI_CHAT_SEND_CHANNEL键值对 |
| [get_physics_entity_key_ui_chat_send_channel_kv](#get_physics_entity_key_ui_chat_send_channel_kv) | 获取逻辑物理组件类型UI_CHAT_SEND_CHANNEL键值对 |
| [get_kv_pair_value_ui_chat_send_channel](#get_kv_pair_value_ui_chat_send_channel) | 获取UI_CHAT_SEND_CHANNEL键值对 |
| [get_unit_key_ui_chat_recv_channel_kv](#get_unit_key_ui_chat_recv_channel_kv) | 获取单位编号UI_CHAT_RECV_CHANNEL键值对 |
| [get_item_key_ui_chat_recv_channel_kv](#get_item_key_ui_chat_recv_channel_kv) | 获取物品编号UI_CHAT_RECV_CHANNEL键值对 |
| [get_ability_key_ui_chat_recv_channel_kv](#get_ability_key_ui_chat_recv_channel_kv) | 获取技能编号UI_CHAT_RECV_CHANNEL键值对 |
| [get_modifier_key_ui_chat_recv_channel_kv](#get_modifier_key_ui_chat_recv_channel_kv) | 获取魔法效果特效编号UI_CHAT_RECV_CHANNEL键值对 |
| [get_projectile_key_ui_chat_recv_channel_kv](#get_projectile_key_ui_chat_recv_channel_kv) | 获取特效编号UI_CHAT_RECV_CHANNEL键值对 |
| [get_destructible_key_ui_chat_recv_channel_kv](#get_destructible_key_ui_chat_recv_channel_kv) | 获取可破坏物编号UI_CHAT_RECV_CHANNEL键值对 |
| [get_tech_key_ui_chat_recv_channel_kv](#get_tech_key_ui_chat_recv_channel_kv) | 获取科技编号UI_CHAT_RECV_CHANNEL键值对 |
| [get_icon_id_ui_chat_recv_channel_kv](#get_icon_id_ui_chat_recv_channel_kv) | 获取图片UI_CHAT_RECV_CHANNEL键值对 |
| [get_physics_entity_key_ui_chat_recv_channel_kv](#get_physics_entity_key_ui_chat_recv_channel_kv) | 获取逻辑物理组件类型UI_CHAT_RECV_CHANNEL键值对 |
| [get_kv_pair_value_ui_chat_recv_channel](#get_kv_pair_value_ui_chat_recv_channel) | 获取UI_CHAT_RECV_CHANNEL键值对 |
| [get_unit_key_ui_anim_play_mode_kv](#get_unit_key_ui_anim_play_mode_kv) | 获取单位编号UI_ANIM_PLAY_MODE键值对 |
| [get_item_key_ui_anim_play_mode_kv](#get_item_key_ui_anim_play_mode_kv) | 获取物品编号UI_ANIM_PLAY_MODE键值对 |
| [get_ability_key_ui_anim_play_mode_kv](#get_ability_key_ui_anim_play_mode_kv) | 获取技能编号UI_ANIM_PLAY_MODE键值对 |

---

## get_trigger_actor_variable_unit_entity

method in GameAPI

- 描述

    获取触发器UNIT_ENTITY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_unit_entity(actor, "key")
```

---

## get_trigger_list_variable_unit_entity

method in GameAPI

- 描述

    获取全局触发器UNIT_ENTITY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_unit_entity("key", 1)
```

---

## get_trigger_list_actor_variable_unit_entity

method in GameAPI

- 描述

    获取触发器UNIT_ENTITY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_unit_entity(actor, "key", 1)
```

---

## get_trigger_list_variable_all_unit_entity

method in GameAPI

- 描述

    获取全局触发器UNIT_ENTITY数组变量

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
local result = GameAPI.get_trigger_list_variable_all_unit_entity("key")
```

---

## get_trigger_list_actor_variable_all_unit_entity

method in GameAPI

- 描述

    获取触发器UNIT_ENTITY 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_unit_entity(actor, "key")
```

---

## get_trigger_variable_unit_group

method in GameAPI

- 描述

    获取全局触发器UNIT_GROUP非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitGroup | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_unit_group("key")
```

---

## get_trigger_actor_variable_unit_group

method in GameAPI

- 描述

    获取触发器UNIT_GROUP非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitGroup | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_unit_group(actor, "key")
```

---

## get_trigger_list_variable_unit_group

method in GameAPI

- 描述

    获取全局触发器UNIT_GROUP数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitGroup | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_unit_group("key", 1)
```

---

## get_trigger_list_actor_variable_unit_group

method in GameAPI

- 描述

    获取触发器UNIT_GROUP数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitGroup | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_unit_group(actor, "key", 1)
```

---

## get_trigger_list_variable_all_unit_group

method in GameAPI

- 描述

    获取全局触发器UNIT_GROUP数组变量

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
local result = GameAPI.get_trigger_list_variable_all_unit_group("key")
```

---

## get_trigger_list_actor_variable_all_unit_group

method in GameAPI

- 描述

    获取触发器UNIT_GROUP 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_unit_group(actor, "key")
```

---

## get_trigger_variable_unit_name

method in GameAPI

- 描述

    获取全局触发器UNIT_NAME非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitKey | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_unit_name("key")
```

---

## get_trigger_actor_variable_unit_name

method in GameAPI

- 描述

    获取触发器UNIT_NAME非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitKey | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_unit_name(actor, "key")
```

---

## get_trigger_list_variable_unit_name

method in GameAPI

- 描述

    获取全局触发器UNIT_NAME数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitKey | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_unit_name("key", 1)
```

---

## get_trigger_list_actor_variable_unit_name

method in GameAPI

- 描述

    获取触发器UNIT_NAME数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitKey | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_unit_name(actor, "key", 1)
```

---

## get_trigger_list_variable_all_unit_name

method in GameAPI

- 描述

    获取全局触发器UNIT_NAME数组变量

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
local result = GameAPI.get_trigger_list_variable_all_unit_name("key")
```

---

## get_trigger_list_actor_variable_all_unit_name

method in GameAPI

- 描述

    获取触发器UNIT_NAME 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_unit_name(actor, "key")
```

---

## get_trigger_variable_unit_name_pool

method in GameAPI

- 描述

    获取全局触发器UNIT_NAME_POOL非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitKeyPool | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_unit_name_pool("key")
```

---

## get_trigger_actor_variable_unit_name_pool

method in GameAPI

- 描述

    获取触发器UNIT_NAME_POOL非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitKeyPool | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_unit_name_pool(actor, "key")
```

---

## get_trigger_list_variable_unit_name_pool

method in GameAPI

- 描述

    获取全局触发器UNIT_NAME_POOL数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitKeyPool | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_unit_name_pool("key", 1)
```

---

## get_trigger_list_actor_variable_unit_name_pool

method in GameAPI

- 描述

    获取触发器UNIT_NAME_POOL数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitKeyPool | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_unit_name_pool(actor, "key", 1)
```

---

## get_trigger_list_variable_all_unit_name_pool

method in GameAPI

- 描述

    获取全局触发器UNIT_NAME_POOL数组变量

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
local result = GameAPI.get_trigger_list_variable_all_unit_name_pool("key")
```

---

## get_trigger_list_actor_variable_all_unit_name_pool

method in GameAPI

- 描述

    获取触发器UNIT_NAME_POOL 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_unit_name_pool(actor, "key")
```

---

## get_trigger_variable_unit_write_attribute

method in GameAPI

- 描述

    获取全局触发器UNIT_WRITE_ATTRIBUTE非数组变量

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
local result = GameAPI.get_trigger_variable_unit_write_attribute("key")
```

---

## get_trigger_actor_variable_unit_write_attribute

method in GameAPI

- 描述

    获取触发器UNIT_WRITE_ATTRIBUTE非数组 组变量

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

local result = GameAPI.get_trigger_actor_variable_unit_write_attribute(actor, "key")
```

---

## get_trigger_list_variable_unit_write_attribute

method in GameAPI

- 描述

    获取全局触发器UNIT_WRITE_ATTRIBUTE数组变量子项

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
local result = GameAPI.get_trigger_list_variable_unit_write_attribute("key", 1)
```

---

## get_trigger_list_actor_variable_unit_write_attribute

method in GameAPI

- 描述

    获取触发器UNIT_WRITE_ATTRIBUTE数组 组变量子项

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

local result = GameAPI.get_trigger_list_actor_variable_unit_write_attribute(actor, "key", 1)
```

---

## get_trigger_list_variable_all_unit_write_attribute

method in GameAPI

- 描述

    获取全局触发器UNIT_WRITE_ATTRIBUTE数组变量

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
local result = GameAPI.get_trigger_list_variable_all_unit_write_attribute("key")
```

---

## get_trigger_list_actor_variable_all_unit_write_attribute

method in GameAPI

- 描述

    获取触发器UNIT_WRITE_ATTRIBUTE 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_unit_write_attribute(actor, "key")
```

---

## get_trigger_variable_attr_element

method in GameAPI

- 描述

    获取全局触发器ATTR_ELEMENT非数组变量

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
local result = GameAPI.get_trigger_variable_attr_element("key")
```

---

## get_trigger_actor_variable_attr_element

method in GameAPI

- 描述

    获取触发器ATTR_ELEMENT非数组 组变量

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

local result = GameAPI.get_trigger_actor_variable_attr_element(actor, "key")
```

---

## get_trigger_list_variable_attr_element

method in GameAPI

- 描述

    获取全局触发器ATTR_ELEMENT数组变量子项

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
local result = GameAPI.get_trigger_list_variable_attr_element("key", 1)
```

---

## get_trigger_list_actor_variable_attr_element

method in GameAPI

- 描述

    获取触发器ATTR_ELEMENT数组 组变量子项

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

local result = GameAPI.get_trigger_list_actor_variable_attr_element(actor, "key", 1)
```

---

## get_trigger_list_variable_all_attr_element

method in GameAPI

- 描述

    获取全局触发器ATTR_ELEMENT数组变量

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
local result = GameAPI.get_trigger_list_variable_all_attr_element("key")
```

---

## get_trigger_list_actor_variable_all_attr_element

method in GameAPI

- 描述

    获取触发器ATTR_ELEMENT 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_attr_element(actor, "key")
```

---

## get_trigger_variable_attr_element_read

method in GameAPI

- 描述

    获取全局触发器ATTR_ELEMENT_READ非数组变量

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
local result = GameAPI.get_trigger_variable_attr_element_read("key")
```

---

## get_trigger_actor_variable_attr_element_read

method in GameAPI

- 描述

    获取触发器ATTR_ELEMENT_READ非数组 组变量

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

local result = GameAPI.get_trigger_actor_variable_attr_element_read(actor, "key")
```

---

## get_trigger_list_variable_attr_element_read

method in GameAPI

- 描述

    获取全局触发器ATTR_ELEMENT_READ数组变量子项

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
local result = GameAPI.get_trigger_list_variable_attr_element_read("key", 1)
```

---

## get_trigger_list_actor_variable_attr_element_read

method in GameAPI

- 描述

    获取触发器ATTR_ELEMENT_READ数组 组变量子项

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

local result = GameAPI.get_trigger_list_actor_variable_attr_element_read(actor, "key", 1)
```

---

## get_trigger_list_variable_all_attr_element_read

method in GameAPI

- 描述

    获取全局触发器ATTR_ELEMENT_READ数组变量

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
local result = GameAPI.get_trigger_list_variable_all_attr_element_read("key")
```

---

## get_trigger_list_actor_variable_all_attr_element_read

method in GameAPI

- 描述

    获取触发器ATTR_ELEMENT_READ 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_attr_element_read(actor, "key")
```

---

## get_trigger_variable_mover_entity

method in GameAPI

- 描述

    获取全局触发器MOVER_ENTITY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Mover | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_mover_entity("key")
```

---

## get_trigger_actor_variable_mover_entity

method in GameAPI

- 描述

    获取触发器MOVER_ENTITY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Mover | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_mover_entity(actor, "key")
```

---

## get_trigger_list_variable_mover_entity

method in GameAPI

- 描述

    获取全局触发器MOVER_ENTITY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Mover | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_mover_entity("key", 1)
```

---

## get_trigger_list_actor_variable_mover_entity

method in GameAPI

- 描述

    获取触发器MOVER_ENTITY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Mover | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_mover_entity(actor, "key", 1)
```

---

## get_trigger_list_variable_all_mover_entity

method in GameAPI

- 描述

    获取全局触发器MOVER_ENTITY数组变量

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
local result = GameAPI.get_trigger_list_variable_all_mover_entity("key")
```

---

## get_trigger_list_actor_variable_all_mover_entity

method in GameAPI

- 描述

    获取触发器MOVER_ENTITY 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_mover_entity(actor, "key")
```

---

## get_trigger_variable_image_quality

method in GameAPI

- 描述

    获取全局触发器IMAGE_QUALITY非数组变量

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
local result = GameAPI.get_trigger_variable_image_quality("key")
```

---

## get_trigger_actor_variable_image_quality

method in GameAPI

- 描述

    获取触发器IMAGE_QUALITY非数组 组变量

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

local result = GameAPI.get_trigger_actor_variable_image_quality(actor, "key")
```

---

## get_trigger_list_variable_image_quality

method in GameAPI

- 描述

    获取全局触发器IMAGE_QUALITY数组变量子项

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
local result = GameAPI.get_trigger_list_variable_image_quality("key", 1)
```

---

## get_trigger_list_actor_variable_image_quality

method in GameAPI

- 描述

    获取触发器IMAGE_QUALITY数组 组变量子项

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

local result = GameAPI.get_trigger_list_actor_variable_image_quality(actor, "key", 1)
```

---

## get_trigger_list_variable_all_image_quality

method in GameAPI

- 描述

    获取全局触发器IMAGE_QUALITY数组变量

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
local result = GameAPI.get_trigger_list_variable_all_image_quality("key")
```

---

## get_trigger_list_actor_variable_all_image_quality

method in GameAPI

- 描述

    获取触发器IMAGE_QUALITY 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_image_quality(actor, "key")
```

---

## get_trigger_variable_window_type_setting

method in GameAPI

- 描述

    获取全局触发器WINDOW_TYPE_SETTING非数组变量

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
local result = GameAPI.get_trigger_variable_window_type_setting("key")
```

---

## get_trigger_actor_variable_window_type_setting

method in GameAPI

- 描述

    获取触发器WINDOW_TYPE_SETTING非数组 组变量

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

local result = GameAPI.get_trigger_actor_variable_window_type_setting(actor, "key")
```

---

## get_trigger_list_variable_window_type_setting

method in GameAPI

- 描述

    获取全局触发器WINDOW_TYPE_SETTING数组变量子项

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
local result = GameAPI.get_trigger_list_variable_window_type_setting("key", 1)
```

---

## get_trigger_list_actor_variable_window_type_setting

method in GameAPI

- 描述

    获取触发器WINDOW_TYPE_SETTING数组 组变量子项

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

local result = GameAPI.get_trigger_list_actor_variable_window_type_setting(actor, "key", 1)
```

---

## get_trigger_list_variable_all_window_type_setting

method in GameAPI

- 描述

    获取全局触发器WINDOW_TYPE_SETTING数组变量

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
local result = GameAPI.get_trigger_list_variable_all_window_type_setting("key")
```

---

## get_trigger_list_actor_variable_all_window_type_setting

method in GameAPI

- 描述

    获取触发器WINDOW_TYPE_SETTING 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_window_type_setting(actor, "key")
```

---

## get_trigger_variable_damage_attack_type

method in GameAPI

- 描述

    获取全局触发器DAMAGE_ATTACK_TYPE非数组变量

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
local result = GameAPI.get_trigger_variable_damage_attack_type("key")
```

---

## get_trigger_actor_variable_damage_attack_type

method in GameAPI

- 描述

    获取触发器DAMAGE_ATTACK_TYPE非数组 组变量

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

local result = GameAPI.get_trigger_actor_variable_damage_attack_type(actor, "key")
```

---

## get_trigger_list_variable_damage_attack_type

method in GameAPI

- 描述

    获取全局触发器DAMAGE_ATTACK_TYPE数组变量子项

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
local result = GameAPI.get_trigger_list_variable_damage_attack_type("key", 1)
```

---

## get_trigger_list_actor_variable_damage_attack_type

method in GameAPI

- 描述

    获取触发器DAMAGE_ATTACK_TYPE数组 组变量子项

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

local result = GameAPI.get_trigger_list_actor_variable_damage_attack_type(actor, "key", 1)
```

---

## get_trigger_list_variable_all_damage_attack_type

method in GameAPI

- 描述

    获取全局触发器DAMAGE_ATTACK_TYPE数组变量

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
local result = GameAPI.get_trigger_list_variable_all_damage_attack_type("key")
```

---

## get_trigger_list_actor_variable_all_damage_attack_type

method in GameAPI

- 描述

    获取触发器DAMAGE_ATTACK_TYPE 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_damage_attack_type(actor, "key")
```

---

## get_trigger_variable_damage_armor_type

method in GameAPI

- 描述

    获取全局触发器DAMAGE_ARMOR_TYPE非数组变量

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
local result = GameAPI.get_trigger_variable_damage_armor_type("key")
```

---

## get_trigger_actor_variable_damage_armor_type

method in GameAPI

- 描述

    获取触发器DAMAGE_ARMOR_TYPE非数组 组变量

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

local result = GameAPI.get_trigger_actor_variable_damage_armor_type(actor, "key")
```

---

## get_trigger_list_variable_damage_armor_type

method in GameAPI

- 描述

    获取全局触发器DAMAGE_ARMOR_TYPE数组变量子项

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
local result = GameAPI.get_trigger_list_variable_damage_armor_type("key", 1)
```

---

## get_trigger_list_actor_variable_damage_armor_type

method in GameAPI

- 描述

    获取触发器DAMAGE_ARMOR_TYPE数组 组变量子项

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

local result = GameAPI.get_trigger_list_actor_variable_damage_armor_type(actor, "key", 1)
```

---

## get_trigger_list_variable_all_damage_armor_type

method in GameAPI

- 描述

    获取全局触发器DAMAGE_ARMOR_TYPE数组变量

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
local result = GameAPI.get_trigger_list_variable_all_damage_armor_type("key")
```

---

## get_trigger_list_actor_variable_all_damage_armor_type

method in GameAPI

- 描述

    获取触发器DAMAGE_ARMOR_TYPE 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_damage_armor_type(actor, "key")
```

---

## get_trigger_variable_item_entity

method in GameAPI

- 描述

    获取全局触发器ITEM_ENTITY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Item | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_item_entity("key")
```

---

## get_trigger_actor_variable_item_entity

method in GameAPI

- 描述

    获取触发器ITEM_ENTITY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Item | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_item_entity(actor, "key")
```

---

## get_trigger_list_variable_item_entity

method in GameAPI

- 描述

    获取全局触发器ITEM_ENTITY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Item | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_item_entity("key", 1)
```

---

## get_trigger_list_actor_variable_item_entity

method in GameAPI

- 描述

    获取触发器ITEM_ENTITY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Item | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_item_entity(actor, "key", 1)
```

---

## get_trigger_list_variable_all_item_entity

method in GameAPI

- 描述

    获取全局触发器ITEM_ENTITY数组变量

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
local result = GameAPI.get_trigger_list_variable_all_item_entity("key")
```

---

## get_trigger_list_actor_variable_all_item_entity

method in GameAPI

- 描述

    获取触发器ITEM_ENTITY 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_item_entity(actor, "key")
```

---

## get_trigger_variable_item_group

method in GameAPI

- 描述

    获取全局触发器ITEM_GROUP非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemGroup | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_item_group("key")
```

---

## get_trigger_actor_variable_item_group

method in GameAPI

- 描述

    获取触发器ITEM_GROUP非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemGroup | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_item_group(actor, "key")
```

---

## get_trigger_list_variable_item_group

method in GameAPI

- 描述

    获取全局触发器ITEM_GROUP数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemGroup | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_item_group("key", 1)
```

---

## get_trigger_list_actor_variable_item_group

method in GameAPI

- 描述

    获取触发器ITEM_GROUP数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemGroup | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_item_group(actor, "key", 1)
```

---

## get_trigger_list_variable_all_item_group

method in GameAPI

- 描述

    获取全局触发器ITEM_GROUP数组变量

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
local result = GameAPI.get_trigger_list_variable_all_item_group("key")
```

---

## get_trigger_list_actor_variable_all_item_group

method in GameAPI

- 描述

    获取触发器ITEM_GROUP 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_item_group(actor, "key")
```

---

## get_trigger_variable_item_name

method in GameAPI

- 描述

    获取全局触发器ITEM_NAME非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemKey | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_item_name("key")
```

---

## get_trigger_actor_variable_item_name

method in GameAPI

- 描述

    获取触发器ITEM_NAME非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemKey | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_item_name(actor, "key")
```

---

## get_trigger_list_variable_item_name

method in GameAPI

- 描述

    获取全局触发器ITEM_NAME数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemKey | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_item_name("key", 1)
```

---

## get_trigger_list_actor_variable_item_name

method in GameAPI

- 描述

    获取触发器ITEM_NAME数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemKey | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_item_name(actor, "key", 1)
```

---

## get_trigger_list_variable_all_item_name

method in GameAPI

- 描述

    获取全局触发器ITEM_NAME数组变量

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
local result = GameAPI.get_trigger_list_variable_all_item_name("key")
```

---

## get_trigger_list_actor_variable_all_item_name

method in GameAPI

- 描述

    获取触发器ITEM_NAME 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_item_name(actor, "key")
```

---

## get_trigger_variable_ability

method in GameAPI

- 描述

    获取全局触发器ABILITY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Ability | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_ability("key")
```

---

## get_trigger_actor_variable_ability

method in GameAPI

- 描述

    获取触发器ABILITY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Ability | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_ability(actor, "key")
```

---

## get_trigger_list_variable_ability

method in GameAPI

- 描述

    获取全局触发器ABILITY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Ability | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_ability("key", 1)
```

---

## get_trigger_list_actor_variable_ability

method in GameAPI

- 描述

    获取触发器ABILITY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Ability | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_ability(actor, "key", 1)
```

---

## get_trigger_list_variable_all_ability

method in GameAPI

- 描述

    获取全局触发器ABILITY数组变量

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
local result = GameAPI.get_trigger_list_variable_all_ability("key")
```

---

## get_trigger_list_actor_variable_all_ability

method in GameAPI

- 描述

    获取触发器ABILITY 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_ability(actor, "key")
```

---

## get_trigger_variable_ability_type

method in GameAPI

- 描述

    获取全局触发器ABILITY_TYPE非数组变量

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
local result = GameAPI.get_trigger_variable_ability_type("key")
```

---

## get_trigger_actor_variable_ability_type

method in GameAPI

- 描述

    获取触发器ABILITY_TYPE非数组 组变量

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

local result = GameAPI.get_trigger_actor_variable_ability_type(actor, "key")
```

---

## get_trigger_list_variable_ability_type

method in GameAPI

- 描述

    获取全局触发器ABILITY_TYPE数组变量子项

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
local result = GameAPI.get_trigger_list_variable_ability_type("key", 1)
```

---

## get_trigger_list_actor_variable_ability_type

method in GameAPI

- 描述

    获取触发器ABILITY_TYPE数组 组变量子项

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

local result = GameAPI.get_trigger_list_actor_variable_ability_type(actor, "key", 1)
```

---

## get_trigger_list_variable_all_ability_type

method in GameAPI

- 描述

    获取全局触发器ABILITY_TYPE数组变量

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
local result = GameAPI.get_trigger_list_variable_all_ability_type("key")
```

---

## get_trigger_list_actor_variable_all_ability_type

method in GameAPI

- 描述

    获取触发器ABILITY_TYPE 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_ability_type(actor, "key")
```

---

## get_trigger_variable_ability_cast_type

method in GameAPI

- 描述

    获取全局触发器ABILITY_CAST_TYPE非数组变量

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
local result = GameAPI.get_trigger_variable_ability_cast_type("key")
```

---

## get_trigger_actor_variable_ability_cast_type

method in GameAPI

- 描述

    获取触发器ABILITY_CAST_TYPE非数组 组变量

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

local result = GameAPI.get_trigger_actor_variable_ability_cast_type(actor, "key")
```

---

## get_trigger_list_variable_ability_cast_type

method in GameAPI

- 描述

    获取全局触发器ABILITY_CAST_TYPE数组变量子项

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
local result = GameAPI.get_trigger_list_variable_ability_cast_type("key", 1)
```

---

## get_trigger_list_actor_variable_ability_cast_type

method in GameAPI

- 描述

    获取触发器ABILITY_CAST_TYPE数组 组变量子项

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

local result = GameAPI.get_trigger_list_actor_variable_ability_cast_type(actor, "key", 1)
```

---

## get_trigger_list_variable_all_ability_cast_type

method in GameAPI

- 描述

    获取全局触发器ABILITY_CAST_TYPE数组变量

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
local result = GameAPI.get_trigger_list_variable_all_ability_cast_type("key")
```

---

## get_trigger_list_actor_variable_all_ability_cast_type

method in GameAPI

- 描述

    获取触发器ABILITY_CAST_TYPE 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_ability_cast_type(actor, "key")
```

---

## get_trigger_variable_ability_name

method in GameAPI

- 描述

    获取全局触发器ABILITY_NAME非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityKey | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_ability_name("key")
```

---

## get_trigger_actor_variable_ability_name

method in GameAPI

- 描述

    获取触发器ABILITY_NAME非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityKey | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_ability_name(actor, "key")
```

---

## get_trigger_list_variable_ability_name

method in GameAPI

- 描述

    获取全局触发器ABILITY_NAME数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityKey | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_ability_name("key", 1)
```

---

## get_trigger_list_actor_variable_ability_name

method in GameAPI

- 描述

    获取触发器ABILITY_NAME数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityKey | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_ability_name(actor, "key", 1)
```

---

## get_trigger_list_variable_all_ability_name

method in GameAPI

- 描述

    获取全局触发器ABILITY_NAME数组变量

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
local result = GameAPI.get_trigger_list_variable_all_ability_name("key")
```

---

## get_trigger_list_actor_variable_all_ability_name

method in GameAPI

- 描述

    获取触发器ABILITY_NAME 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_ability_name(actor, "key")
```

---

## get_trigger_variable_modifier_entity

method in GameAPI

- 描述

    获取全局触发器MODIFIER_ENTITY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierEntity | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_modifier_entity("key")
```

---

## get_trigger_actor_variable_modifier_entity

method in GameAPI

- 描述

    获取触发器MODIFIER_ENTITY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierEntity | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_modifier_entity(actor, "key")
```

---

## get_trigger_list_variable_modifier_entity

method in GameAPI

- 描述

    获取全局触发器MODIFIER_ENTITY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierEntity | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_modifier_entity("key", 1)
```

---

## get_trigger_list_actor_variable_modifier_entity

method in GameAPI

- 描述

    获取触发器MODIFIER_ENTITY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierEntity | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_modifier_entity(actor, "key", 1)
```

---

## get_trigger_list_variable_all_modifier_entity

method in GameAPI

- 描述

    获取全局触发器MODIFIER_ENTITY数组变量

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
local result = GameAPI.get_trigger_list_variable_all_modifier_entity("key")
```

---

## get_trigger_list_actor_variable_all_modifier_entity

method in GameAPI

- 描述

    获取触发器MODIFIER_ENTITY 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_modifier_entity(actor, "key")
```

---

## get_trigger_variable_modifier

method in GameAPI

- 描述

    获取全局触发器MODIFIER非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierKey | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_modifier("key")
```

---

## get_trigger_actor_variable_modifier

method in GameAPI

- 描述

    获取触发器MODIFIER非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierKey | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_modifier(actor, "key")
```

---

## get_trigger_list_variable_modifier

method in GameAPI

- 描述

    获取全局触发器MODIFIER数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierKey | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_modifier("key", 1)
```

---

## get_trigger_list_actor_variable_modifier

method in GameAPI

- 描述

    获取触发器MODIFIER数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierKey | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_modifier(actor, "key", 1)
```

---

## get_trigger_list_variable_all_modifier

method in GameAPI

- 描述

    获取全局触发器MODIFIER数组变量

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
local result = GameAPI.get_trigger_list_variable_all_modifier("key")
```

---

## get_trigger_list_actor_variable_all_modifier

method in GameAPI

- 描述

    获取触发器MODIFIER 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_modifier(actor, "key")
```

---

## get_trigger_variable_projectile

method in GameAPI

- 描述

    获取全局触发器PROJECTILE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileKey | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_projectile("key")
```

---

## get_trigger_actor_variable_projectile

method in GameAPI

- 描述

    获取触发器PROJECTILE非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileKey | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_projectile(actor, "key")
```

---

## get_trigger_list_variable_projectile

method in GameAPI

- 描述

    获取全局触发器PROJECTILE数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileKey | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_projectile("key", 1)
```

---

## get_trigger_list_actor_variable_projectile

method in GameAPI

- 描述

    获取触发器PROJECTILE数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileKey | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_projectile(actor, "key", 1)
```

---

## get_trigger_list_variable_all_projectile

method in GameAPI

- 描述

    获取全局触发器PROJECTILE数组变量

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
local result = GameAPI.get_trigger_list_variable_all_projectile("key")
```

---

## get_trigger_list_actor_variable_all_projectile

method in GameAPI

- 描述

    获取触发器PROJECTILE 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_projectile(actor, "key")
```

---

## get_trigger_variable_projectile_entity

method in GameAPI

- 描述

    获取全局触发器PROJECTILE_ENTITY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileEntity | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_projectile_entity("key")
```

---

## get_trigger_actor_variable_projectile_entity

method in GameAPI

- 描述

    获取触发器PROJECTILE_ENTITY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileEntity | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_projectile_entity(actor, "key")
```

---

## get_trigger_list_variable_projectile_entity

method in GameAPI

- 描述

    获取全局触发器PROJECTILE_ENTITY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileEntity | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_projectile_entity("key", 1)
```

---

## get_trigger_list_actor_variable_projectile_entity

method in GameAPI

- 描述

    获取触发器PROJECTILE_ENTITY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileEntity | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_projectile_entity(actor, "key", 1)
```

---

## get_trigger_list_variable_all_projectile_entity

method in GameAPI

- 描述

    获取全局触发器PROJECTILE_ENTITY数组变量

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
local result = GameAPI.get_trigger_list_variable_all_projectile_entity("key")
```

---

## get_trigger_list_actor_variable_all_projectile_entity

method in GameAPI

- 描述

    获取触发器PROJECTILE_ENTITY 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_projectile_entity(actor, "key")
```

---

## get_trigger_variable_projectile_group

method in GameAPI

- 描述

    获取全局触发器PROJECTILE_GROUP非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileGroup | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_projectile_group("key")
```

---

## get_trigger_actor_variable_projectile_group

method in GameAPI

- 描述

    获取触发器PROJECTILE_GROUP非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileGroup | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_projectile_group(actor, "key")
```

---

## get_trigger_list_variable_projectile_group

method in GameAPI

- 描述

    获取全局触发器PROJECTILE_GROUP数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileGroup | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_projectile_group("key", 1)
```

---

## get_trigger_list_actor_variable_projectile_group

method in GameAPI

- 描述

    获取触发器PROJECTILE_GROUP数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileGroup | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_projectile_group(actor, "key", 1)
```

---

## get_trigger_list_variable_all_projectile_group

method in GameAPI

- 描述

    获取全局触发器PROJECTILE_GROUP数组变量

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
local result = GameAPI.get_trigger_list_variable_all_projectile_group("key")
```

---

## get_trigger_list_actor_variable_all_projectile_group

method in GameAPI

- 描述

    获取触发器PROJECTILE_GROUP 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_projectile_group(actor, "key")
```

---

## get_trigger_variable_destructible_entity

method in GameAPI

- 描述

    获取全局触发器DESTRUCTIBLE_ENTITY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Destructible | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_destructible_entity("key")
```

---

## get_trigger_actor_variable_destructible_entity

method in GameAPI

- 描述

    获取触发器DESTRUCTIBLE_ENTITY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Destructible | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_destructible_entity(actor, "key")
```

---

## get_trigger_list_variable_destructible_entity

method in GameAPI

- 描述

    获取全局触发器DESTRUCTIBLE_ENTITY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Destructible | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_destructible_entity("key", 1)
```

---

## get_trigger_list_actor_variable_destructible_entity

method in GameAPI

- 描述

    获取触发器DESTRUCTIBLE_ENTITY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Destructible | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_destructible_entity(actor, "key", 1)
```

---

## get_trigger_list_variable_all_destructible_entity

method in GameAPI

- 描述

    获取全局触发器DESTRUCTIBLE_ENTITY数组变量

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
local result = GameAPI.get_trigger_list_variable_all_destructible_entity("key")
```

---

## get_trigger_list_actor_variable_all_destructible_entity

method in GameAPI

- 描述

    获取触发器DESTRUCTIBLE_ENTITY 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_destructible_entity(actor, "key")
```

---

## get_trigger_variable_destructible_name

method in GameAPI

- 描述

    获取全局触发器DESTRUCTIBLE_NAME非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DestructibleKey | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_destructible_name("key")
```

---

## get_trigger_actor_variable_destructible_name

method in GameAPI

- 描述

    获取触发器DESTRUCTIBLE_NAME非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DestructibleKey | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_destructible_name(actor, "key")
```

---

## get_trigger_list_variable_destructible_name

method in GameAPI

- 描述

    获取全局触发器DESTRUCTIBLE_NAME数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DestructibleKey | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_destructible_name("key", 1)
```

---

## get_trigger_list_actor_variable_destructible_name

method in GameAPI

- 描述

    获取触发器DESTRUCTIBLE_NAME数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DestructibleKey | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_destructible_name(actor, "key", 1)
```

---

## get_trigger_list_variable_all_destructible_name

method in GameAPI

- 描述

    获取全局触发器DESTRUCTIBLE_NAME数组变量

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
local result = GameAPI.get_trigger_list_variable_all_destructible_name("key")
```

---

## get_trigger_list_actor_variable_all_destructible_name

method in GameAPI

- 描述

    获取触发器DESTRUCTIBLE_NAME 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_destructible_name(actor, "key")
```

---

## get_trigger_variable_sound_entity

method in GameAPI

- 描述

    获取全局触发器SOUND_ENTITY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SoundEntity | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_sound_entity("key")
```

---

## get_trigger_actor_variable_sound_entity

method in GameAPI

- 描述

    获取触发器SOUND_ENTITY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SoundEntity | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_sound_entity(actor, "key")
```

---

## get_trigger_list_variable_sound_entity

method in GameAPI

- 描述

    获取全局触发器SOUND_ENTITY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SoundEntity | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_sound_entity("key", 1)
```

---

## get_trigger_list_actor_variable_sound_entity

method in GameAPI

- 描述

    获取触发器SOUND_ENTITY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SoundEntity | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_sound_entity(actor, "key", 1)
```

---

## get_trigger_list_variable_all_sound_entity

method in GameAPI

- 描述

    获取全局触发器SOUND_ENTITY数组变量

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
local result = GameAPI.get_trigger_list_variable_all_sound_entity("key")
```

---

## get_trigger_list_actor_variable_all_sound_entity

method in GameAPI

- 描述

    获取触发器SOUND_ENTITY 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_sound_entity(actor, "key")
```

---

## get_trigger_variable_audio_key

method in GameAPI

- 描述

    获取全局触发器AUDIO_KEY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AudioKey | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_audio_key("key")
```

---

## get_trigger_actor_variable_audio_key

method in GameAPI

- 描述

    获取触发器AUDIO_KEY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AudioKey | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_audio_key(actor, "key")
```

---

## get_trigger_list_variable_audio_key

method in GameAPI

- 描述

    获取全局触发器AUDIO_KEY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AudioKey | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_audio_key("key", 1)
```

---

## get_trigger_list_actor_variable_audio_key

method in GameAPI

- 描述

    获取触发器AUDIO_KEY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AudioKey | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_audio_key(actor, "key", 1)
```

---

## get_trigger_list_variable_all_audio_key

method in GameAPI

- 描述

    获取全局触发器AUDIO_KEY数组变量

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
local result = GameAPI.get_trigger_list_variable_all_audio_key("key")
```

---

## get_trigger_list_actor_variable_all_audio_key

method in GameAPI

- 描述

    获取触发器AUDIO_KEY 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_audio_key(actor, "key")
```

---

## get_trigger_variable_game_mode

method in GameAPI

- 描述

    获取全局触发器GAME_MODE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.GameMode | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_game_mode("key")
```

---

## get_trigger_actor_variable_game_mode

method in GameAPI

- 描述

    获取触发器GAME_MODE非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.GameMode | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_game_mode(actor, "key")
```

---

## get_trigger_list_variable_game_mode

method in GameAPI

- 描述

    获取全局触发器GAME_MODE数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.GameMode | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_game_mode("key", 1)
```

---

## get_trigger_list_actor_variable_game_mode

method in GameAPI

- 描述

    获取触发器GAME_MODE数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.GameMode | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_game_mode(actor, "key", 1)
```

---

## get_trigger_list_variable_all_game_mode

method in GameAPI

- 描述

    获取全局触发器GAME_MODE数组变量

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
local result = GameAPI.get_trigger_list_variable_all_game_mode("key")
```

---

## get_trigger_list_actor_variable_all_game_mode

method in GameAPI

- 描述

    获取触发器GAME_MODE 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_game_mode(actor, "key")
```

---

## get_trigger_variable_player

method in GameAPI

- 描述

    获取全局触发器PLAYER非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Role | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_player("key")
```

---

## get_trigger_actor_variable_player

method in GameAPI

- 描述

    获取触发器PLAYER非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Role | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_player(actor, "key")
```

---

## get_trigger_list_variable_player

method in GameAPI

- 描述

    获取全局触发器PLAYER数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Role | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_player("key", 1)
```

---

## get_trigger_list_actor_variable_player

method in GameAPI

- 描述

    获取触发器PLAYER数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Role | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_player(actor, "key", 1)
```

---

## get_trigger_list_variable_all_player

method in GameAPI

- 描述

    获取全局触发器PLAYER数组变量

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
local result = GameAPI.get_trigger_list_variable_all_player("key")
```

---

## get_trigger_list_actor_variable_all_player

method in GameAPI

- 描述

    获取触发器PLAYER 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_player(actor, "key")
```

---

## get_trigger_variable_player_group

method in GameAPI

- 描述

    获取全局触发器PLAYER_GROUP非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleGroup | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_player_group("key")
```

---

## get_trigger_actor_variable_player_group

method in GameAPI

- 描述

    获取触发器PLAYER_GROUP非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleGroup | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_player_group(actor, "key")
```

---

## get_trigger_list_variable_player_group

method in GameAPI

- 描述

    获取全局触发器PLAYER_GROUP数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleGroup | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_player_group("key", 1)
```

---

## get_trigger_list_actor_variable_player_group

method in GameAPI

- 描述

    获取触发器PLAYER_GROUP数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleGroup | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_player_group(actor, "key", 1)
```

---

## get_trigger_list_variable_all_player_group

method in GameAPI

- 描述

    获取全局触发器PLAYER_GROUP数组变量

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
local result = GameAPI.get_trigger_list_variable_all_player_group("key")
```

---

## get_trigger_list_actor_variable_all_player_group

method in GameAPI

- 描述

    获取触发器PLAYER_GROUP 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_player_group(actor, "key")
```

---

## get_trigger_variable_role_res_key

method in GameAPI

- 描述

    获取全局触发器ROLE_RES_KEY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleResKey | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_role_res_key("key")
```

---

## get_trigger_actor_variable_role_res_key

method in GameAPI

- 描述

    获取触发器ROLE_RES_KEY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleResKey | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_role_res_key(actor, "key")
```

---

## get_trigger_list_variable_role_res_key

method in GameAPI

- 描述

    获取全局触发器ROLE_RES_KEY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleResKey | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_role_res_key("key", 1)
```

---

## get_trigger_list_actor_variable_role_res_key

method in GameAPI

- 描述

    获取触发器ROLE_RES_KEY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleResKey | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_role_res_key(actor, "key", 1)
```

---

## get_trigger_list_variable_all_role_res_key

method in GameAPI

- 描述

    获取全局触发器ROLE_RES_KEY数组变量

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
local result = GameAPI.get_trigger_list_variable_all_role_res_key("key")
```

---

## get_trigger_list_actor_variable_all_role_res_key

method in GameAPI

- 描述

    获取触发器ROLE_RES_KEY 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_role_res_key(actor, "key")
```

---

## get_trigger_variable_role_status

method in GameAPI

- 描述

    获取全局触发器ROLE_STATUS非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleStatus | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_role_status("key")
```

---

## get_trigger_actor_variable_role_status

method in GameAPI

- 描述

    获取触发器ROLE_STATUS非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleStatus | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_role_status(actor, "key")
```

---

## get_trigger_list_variable_role_status

method in GameAPI

- 描述

    获取全局触发器ROLE_STATUS数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleStatus | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_role_status("key", 1)
```

---

## get_trigger_list_actor_variable_role_status

method in GameAPI

- 描述

    获取触发器ROLE_STATUS数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleStatus | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_role_status(actor, "key", 1)
```

---

## get_trigger_list_variable_all_role_status

method in GameAPI

- 描述

    获取全局触发器ROLE_STATUS数组变量

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
local result = GameAPI.get_trigger_list_variable_all_role_status("key")
```

---

## get_trigger_list_actor_variable_all_role_status

method in GameAPI

- 描述

    获取触发器ROLE_STATUS 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_role_status(actor, "key")
```

---

## get_trigger_variable_role_type

method in GameAPI

- 描述

    获取全局触发器ROLE_TYPE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleType | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_role_type("key")
```

---

## get_trigger_actor_variable_role_type

method in GameAPI

- 描述

    获取触发器ROLE_TYPE非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleType | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_role_type(actor, "key")
```

---

## get_trigger_list_variable_role_type

method in GameAPI

- 描述

    获取全局触发器ROLE_TYPE数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleType | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_role_type("key", 1)
```

---

## get_trigger_list_actor_variable_role_type

method in GameAPI

- 描述

    获取触发器ROLE_TYPE数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleType | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_role_type(actor, "key", 1)
```

---

## get_trigger_list_variable_all_role_type

method in GameAPI

- 描述

    获取全局触发器ROLE_TYPE数组变量

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
local result = GameAPI.get_trigger_list_variable_all_role_type("key")
```

---

## get_trigger_list_actor_variable_all_role_type

method in GameAPI

- 描述

    获取触发器ROLE_TYPE 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_role_type(actor, "key")
```

---

## get_trigger_variable_team

method in GameAPI

- 描述

    获取全局触发器TEAM非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Camp | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_team("key")
```

---

## get_trigger_actor_variable_team

method in GameAPI

- 描述

    获取触发器TEAM非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Camp | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_team(actor, "key")
```

---

## get_trigger_list_variable_team

method in GameAPI

- 描述

    获取全局触发器TEAM数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Camp | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_team("key", 1)
```

---

## get_trigger_list_actor_variable_team

method in GameAPI

- 描述

    获取触发器TEAM数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Camp | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_team(actor, "key", 1)
```

---

## get_trigger_list_variable_all_team

method in GameAPI

- 描述

    获取全局触发器TEAM数组变量

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
local result = GameAPI.get_trigger_list_variable_all_team("key")
```

---

## get_trigger_list_actor_variable_all_team

method in GameAPI

- 描述

    获取触发器TEAM 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_team(actor, "key")
```

---

## get_trigger_variable_point

method in GameAPI

- 描述

    获取全局触发器POINT非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FPoint | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_point("key")
```

---

## get_trigger_actor_variable_point

method in GameAPI

- 描述

    获取触发器POINT非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FPoint | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_point(actor, "key")
```

---

## get_trigger_list_variable_point

method in GameAPI

- 描述

    获取全局触发器POINT数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FPoint | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_point("key", 1)
```

---

## get_trigger_list_actor_variable_point

method in GameAPI

- 描述

    获取触发器POINT数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FPoint | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_point(actor, "key", 1)
```

---

## get_trigger_list_variable_all_point

method in GameAPI

- 描述

    获取全局触发器POINT数组变量

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
local result = GameAPI.get_trigger_list_variable_all_point("key")
```

---

## get_trigger_list_actor_variable_all_point

method in GameAPI

- 描述

    获取触发器POINT 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_point(actor, "key")
```

---

## get_trigger_variable_vector3

method in GameAPI

- 描述

    获取全局触发器VECTOR3非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3 | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_vector3("key")
```

---

## get_trigger_actor_variable_vector3

method in GameAPI

- 描述

    获取触发器VECTOR3非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3 | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_vector3(actor, "key")
```

---

## get_trigger_list_variable_vector3

method in GameAPI

- 描述

    获取全局触发器VECTOR3数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3 | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_vector3("key", 1)
```

---

## get_trigger_list_actor_variable_vector3

method in GameAPI

- 描述

    获取触发器VECTOR3数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3 | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_vector3(actor, "key", 1)
```

---

## get_trigger_list_variable_all_vector3

method in GameAPI

- 描述

    获取全局触发器VECTOR3数组变量

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
local result = GameAPI.get_trigger_list_variable_all_vector3("key")
```

---

## get_trigger_list_actor_variable_all_vector3

method in GameAPI

- 描述

    获取触发器VECTOR3 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_vector3(actor, "key")
```

---

## get_trigger_variable_rotation

method in GameAPI

- 描述

    获取全局触发器ROTATION非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FRotation | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_rotation("key")
```

---

## get_trigger_actor_variable_rotation

method in GameAPI

- 描述

    获取触发器ROTATION非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FRotation | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_rotation(actor, "key")
```

---

## get_trigger_list_variable_rotation

method in GameAPI

- 描述

    获取全局触发器ROTATION数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FRotation | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_rotation("key", 1)
```

---

## get_trigger_list_actor_variable_rotation

method in GameAPI

- 描述

    获取触发器ROTATION数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FRotation | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_rotation(actor, "key", 1)
```

---

## get_trigger_list_variable_all_rotation

method in GameAPI

- 描述

    获取全局触发器ROTATION数组变量

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
local result = GameAPI.get_trigger_list_variable_all_rotation("key")
```

---

## get_trigger_list_actor_variable_all_rotation

method in GameAPI

- 描述

    获取触发器ROTATION 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_rotation(actor, "key")
```

---

## get_trigger_variable_point_list

method in GameAPI

- 描述

    获取全局触发器POINT_LIST非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Road | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_point_list("key")
```

---

## get_trigger_actor_variable_point_list

method in GameAPI

- 描述

    获取触发器POINT_LIST非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Road | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_point_list(actor, "key")
```

---

## get_trigger_list_variable_point_list

method in GameAPI

- 描述

    获取全局触发器POINT_LIST数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Road | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_point_list("key", 1)
```

---

## get_trigger_list_actor_variable_point_list

method in GameAPI

- 描述

    获取触发器POINT_LIST数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Road | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_point_list(actor, "key", 1)
```

---

## get_trigger_list_variable_all_point_list

method in GameAPI

- 描述

    获取全局触发器POINT_LIST数组变量

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
local result = GameAPI.get_trigger_list_variable_all_point_list("key")
```

---

## get_trigger_list_actor_variable_all_point_list

method in GameAPI

- 描述

    获取触发器POINT_LIST 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_point_list(actor, "key")
```

---

## get_trigger_variable_road_group

method in GameAPI

- 描述

    获取全局触发器ROAD_GROUP非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoadGroup | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_road_group("key")
```

---

## get_trigger_actor_variable_road_group

method in GameAPI

- 描述

    获取触发器ROAD_GROUP非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoadGroup | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_road_group(actor, "key")
```

---

## get_trigger_list_variable_road_group

method in GameAPI

- 描述

    获取全局触发器ROAD_GROUP数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoadGroup | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_road_group("key", 1)
```

---

## get_trigger_list_actor_variable_road_group

method in GameAPI

- 描述

    获取触发器ROAD_GROUP数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoadGroup | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_road_group(actor, "key", 1)
```

---

## get_trigger_list_variable_all_road_group

method in GameAPI

- 描述

    获取全局触发器ROAD_GROUP数组变量

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
local result = GameAPI.get_trigger_list_variable_all_road_group("key")
```

---

## get_trigger_list_actor_variable_all_road_group

method in GameAPI

- 描述

    获取触发器ROAD_GROUP 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_road_group(actor, "key")
```

---

## get_trigger_variable_rectangle

method in GameAPI

- 描述

    获取全局触发器RECTANGLE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RecArea | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_rectangle("key")
```

---

## get_trigger_actor_variable_rectangle

method in GameAPI

- 描述

    获取触发器RECTANGLE非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RecArea | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_rectangle(actor, "key")
```

---

## get_trigger_list_variable_rectangle

method in GameAPI

- 描述

    获取全局触发器RECTANGLE数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RecArea | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_rectangle("key", 1)
```

---

## get_trigger_list_actor_variable_rectangle

method in GameAPI

- 描述

    获取触发器RECTANGLE数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RecArea | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_rectangle(actor, "key", 1)
```

---

## get_trigger_list_variable_all_rectangle

method in GameAPI

- 描述

    获取全局触发器RECTANGLE数组变量

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
local result = GameAPI.get_trigger_list_variable_all_rectangle("key")
```

---

## get_trigger_list_actor_variable_all_rectangle

method in GameAPI

- 描述

    获取触发器RECTANGLE 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_rectangle(actor, "key")
```

---

## get_trigger_variable_round_area

method in GameAPI

- 描述

    获取全局触发器ROUND_AREA非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CirArea | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_round_area("key")
```

---

## get_trigger_actor_variable_round_area

method in GameAPI

- 描述

    获取触发器ROUND_AREA非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CirArea | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_round_area(actor, "key")
```

---

## get_trigger_list_variable_round_area

method in GameAPI

- 描述

    获取全局触发器ROUND_AREA数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CirArea | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_round_area("key", 1)
```

---

## get_trigger_list_actor_variable_round_area

method in GameAPI

- 描述

    获取触发器ROUND_AREA数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CirArea | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_round_area(actor, "key", 1)
```

---

## get_trigger_list_variable_all_round_area

method in GameAPI

- 描述

    获取全局触发器ROUND_AREA数组变量

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
local result = GameAPI.get_trigger_list_variable_all_round_area("key")
```

---

## get_trigger_list_actor_variable_all_round_area

method in GameAPI

- 描述

    获取触发器ROUND_AREA 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_round_area(actor, "key")
```

---

## get_trigger_variable_polygon

method in GameAPI

- 描述

    获取全局触发器POLYGON非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PolyArea | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_polygon("key")
```

---

## get_trigger_actor_variable_polygon

method in GameAPI

- 描述

    获取触发器POLYGON非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PolyArea | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_polygon(actor, "key")
```

---

## get_trigger_list_variable_polygon

method in GameAPI

- 描述

    获取全局触发器POLYGON数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PolyArea | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_polygon("key", 1)
```

---

## get_trigger_list_actor_variable_polygon

method in GameAPI

- 描述

    获取触发器POLYGON数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PolyArea | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_polygon(actor, "key", 1)
```

---

## get_trigger_list_variable_all_polygon

method in GameAPI

- 描述

    获取全局触发器POLYGON数组变量

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
local result = GameAPI.get_trigger_list_variable_all_polygon("key")
```

---

## get_trigger_list_actor_variable_all_polygon

method in GameAPI

- 描述

    获取触发器POLYGON 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_polygon(actor, "key")
```

---

## get_trigger_variable_camera

method in GameAPI

- 描述

    获取全局触发器CAMERA非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Camera | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_camera("key")
```

---

## get_trigger_actor_variable_camera

method in GameAPI

- 描述

    获取触发器CAMERA非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Camera | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_camera(actor, "key")
```

---

## get_trigger_list_variable_camera

method in GameAPI

- 描述

    获取全局触发器CAMERA数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Camera | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_camera("key", 1)
```

---

## get_trigger_list_actor_variable_camera

method in GameAPI

- 描述

    获取触发器CAMERA数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Camera | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_camera(actor, "key", 1)
```

---

## get_trigger_list_variable_all_camera

method in GameAPI

- 描述

    获取全局触发器CAMERA数组变量

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
local result = GameAPI.get_trigger_list_variable_all_camera("key")
```

---

## get_trigger_list_actor_variable_all_camera

method in GameAPI

- 描述

    获取触发器CAMERA 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_camera(actor, "key")
```

---

## get_trigger_variable_camline

method in GameAPI

- 描述

    获取全局触发器CAMLINE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CamlineID | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_camline("key")
```

---

## get_trigger_actor_variable_camline

method in GameAPI

- 描述

    获取触发器CAMLINE非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CamlineID | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_camline(actor, "key")
```

---

## get_trigger_list_variable_camline

method in GameAPI

- 描述

    获取全局触发器CAMLINE数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CamlineID | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_camline("key", 1)
```

---

## get_trigger_list_actor_variable_camline

method in GameAPI

- 描述

    获取触发器CAMLINE数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CamlineID | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_camline(actor, "key", 1)
```

---

## get_trigger_list_variable_all_camline

method in GameAPI

- 描述

    获取全局触发器CAMLINE数组变量

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
local result = GameAPI.get_trigger_list_variable_all_camline("key")
```

---

## get_trigger_list_actor_variable_all_camline

method in GameAPI

- 描述

    获取触发器CAMLINE 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_camline(actor, "key")
```

---

## get_trigger_variable_point_light

method in GameAPI

- 描述

    获取全局触发器POINT_LIGHT非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PointLight | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_point_light("key")
```

---

## get_trigger_actor_variable_point_light

method in GameAPI

- 描述

    获取触发器POINT_LIGHT非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PointLight | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_point_light(actor, "key")
```

---

## get_trigger_list_variable_point_light

method in GameAPI

- 描述

    获取全局触发器POINT_LIGHT数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PointLight | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_point_light("key", 1)
```

---

## get_trigger_list_actor_variable_point_light

method in GameAPI

- 描述

    获取触发器POINT_LIGHT数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PointLight | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_point_light(actor, "key", 1)
```

---

## get_trigger_list_variable_all_point_light

method in GameAPI

- 描述

    获取全局触发器POINT_LIGHT数组变量

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
local result = GameAPI.get_trigger_list_variable_all_point_light("key")
```

---

## get_trigger_list_actor_variable_all_point_light

method in GameAPI

- 描述

    获取触发器POINT_LIGHT 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_point_light(actor, "key")
```

---

## get_trigger_variable_spot_light

method in GameAPI

- 描述

    获取全局触发器SPOT_LIGHT非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SpotLight | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_spot_light("key")
```

---

## get_trigger_actor_variable_spot_light

method in GameAPI

- 描述

    获取触发器SPOT_LIGHT非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SpotLight | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_spot_light(actor, "key")
```

---

## get_trigger_list_variable_spot_light

method in GameAPI

- 描述

    获取全局触发器SPOT_LIGHT数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SpotLight | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_spot_light("key", 1)
```

---

## get_trigger_list_actor_variable_spot_light

method in GameAPI

- 描述

    获取触发器SPOT_LIGHT数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SpotLight | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_spot_light(actor, "key", 1)
```

---

## get_trigger_list_variable_all_spot_light

method in GameAPI

- 描述

    获取全局触发器SPOT_LIGHT数组变量

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
local result = GameAPI.get_trigger_list_variable_all_spot_light("key")
```

---

## get_trigger_list_actor_variable_all_spot_light

method in GameAPI

- 描述

    获取触发器SPOT_LIGHT 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_spot_light(actor, "key")
```

---

## get_trigger_variable_fog

method in GameAPI

- 描述

    获取全局触发器FOG非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fog | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_fog("key")
```

---

## get_trigger_actor_variable_fog

method in GameAPI

- 描述

    获取触发器FOG非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fog | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_fog(actor, "key")
```

---

## get_trigger_list_variable_fog

method in GameAPI

- 描述

    获取全局触发器FOG数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fog | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_fog("key", 1)
```

---

## get_trigger_list_actor_variable_fog

method in GameAPI

- 描述

    获取触发器FOG数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fog | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_fog(actor, "key", 1)
```

---

## get_trigger_list_variable_all_fog

method in GameAPI

- 描述

    获取全局触发器FOG数组变量

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
local result = GameAPI.get_trigger_list_variable_all_fog("key")
```

---

## get_trigger_list_actor_variable_all_fog

method in GameAPI

- 描述

    获取触发器FOG 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_fog(actor, "key")
```

---

## get_trigger_variable_model

method in GameAPI

- 描述

    获取全局触发器MODEL非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModelKey | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_model("key")
```

---

## get_trigger_actor_variable_model

method in GameAPI

- 描述

    获取触发器MODEL非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModelKey | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_model(actor, "key")
```

---

## get_trigger_list_variable_model

method in GameAPI

- 描述

    获取全局触发器MODEL数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModelKey | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_model("key", 1)
```

---

## get_trigger_list_actor_variable_model

method in GameAPI

- 描述

    获取触发器MODEL数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModelKey | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_model(actor, "key", 1)
```

---

## get_trigger_list_variable_all_model

method in GameAPI

- 描述

    获取全局触发器MODEL数组变量

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
local result = GameAPI.get_trigger_list_variable_all_model("key")
```

---

## get_trigger_list_actor_variable_all_model

method in GameAPI

- 描述

    获取触发器MODEL 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_model(actor, "key")
```

---

## get_trigger_variable_sfx_entity

method in GameAPI

- 描述

    获取全局触发器SFX_ENTITY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sfx | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_sfx_entity("key")
```

---

## get_trigger_actor_variable_sfx_entity

method in GameAPI

- 描述

    获取触发器SFX_ENTITY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sfx | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_sfx_entity(actor, "key")
```

---

## get_trigger_list_variable_sfx_entity

method in GameAPI

- 描述

    获取全局触发器SFX_ENTITY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sfx | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_sfx_entity("key", 1)
```

---

## get_trigger_list_actor_variable_sfx_entity

method in GameAPI

- 描述

    获取触发器SFX_ENTITY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sfx | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_sfx_entity(actor, "key", 1)
```

---

## get_trigger_list_variable_all_sfx_entity

method in GameAPI

- 描述

    获取全局触发器SFX_ENTITY数组变量

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
local result = GameAPI.get_trigger_list_variable_all_sfx_entity("key")
```

---

## get_trigger_list_actor_variable_all_sfx_entity

method in GameAPI

- 描述

    获取触发器SFX_ENTITY 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_sfx_entity(actor, "key")
```

---

## get_trigger_variable_sfx_key

method in GameAPI

- 描述

    获取全局触发器SFX_KEY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SfxKey | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_sfx_key("key")
```

---

## get_trigger_actor_variable_sfx_key

method in GameAPI

- 描述

    获取触发器SFX_KEY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SfxKey | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_sfx_key(actor, "key")
```

---

## get_trigger_list_variable_sfx_key

method in GameAPI

- 描述

    获取全局触发器SFX_KEY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SfxKey | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_sfx_key("key", 1)
```

---

## get_trigger_list_actor_variable_sfx_key

method in GameAPI

- 描述

    获取触发器SFX_KEY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SfxKey | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_sfx_key(actor, "key", 1)
```

---

## get_trigger_list_variable_all_sfx_key

method in GameAPI

- 描述

    获取全局触发器SFX_KEY数组变量

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
local result = GameAPI.get_trigger_list_variable_all_sfx_key("key")
```

---

## get_trigger_list_actor_variable_all_sfx_key

method in GameAPI

- 描述

    获取触发器SFX_KEY 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_sfx_key(actor, "key")
```

---

## get_trigger_variable_link_sfx_entity

method in GameAPI

- 描述

    获取全局触发器LINK_SFX_ENTITY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LinkSfx | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_link_sfx_entity("key")
```

---

## get_trigger_actor_variable_link_sfx_entity

method in GameAPI

- 描述

    获取触发器LINK_SFX_ENTITY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LinkSfx | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_link_sfx_entity(actor, "key")
```

---

## get_trigger_list_variable_link_sfx_entity

method in GameAPI

- 描述

    获取全局触发器LINK_SFX_ENTITY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LinkSfx | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_link_sfx_entity("key", 1)
```

---

## get_trigger_list_actor_variable_link_sfx_entity

method in GameAPI

- 描述

    获取触发器LINK_SFX_ENTITY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LinkSfx | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_link_sfx_entity(actor, "key", 1)
```

---

## get_trigger_list_variable_all_link_sfx_entity

method in GameAPI

- 描述

    获取全局触发器LINK_SFX_ENTITY数组变量

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
local result = GameAPI.get_trigger_list_variable_all_link_sfx_entity("key")
```

---

## get_trigger_list_actor_variable_all_link_sfx_entity

method in GameAPI

- 描述

    获取触发器LINK_SFX_ENTITY 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_link_sfx_entity(actor, "key")
```

---

## get_trigger_variable_link_sfx_key

method in GameAPI

- 描述

    获取全局触发器LINK_SFX_KEY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LinkSfxKey | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_link_sfx_key("key")
```

---

## get_trigger_actor_variable_link_sfx_key

method in GameAPI

- 描述

    获取触发器LINK_SFX_KEY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LinkSfxKey | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_link_sfx_key(actor, "key")
```

---

## get_trigger_list_variable_link_sfx_key

method in GameAPI

- 描述

    获取全局触发器LINK_SFX_KEY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LinkSfxKey | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_link_sfx_key("key", 1)
```

---

## get_trigger_list_actor_variable_link_sfx_key

method in GameAPI

- 描述

    获取触发器LINK_SFX_KEY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LinkSfxKey | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_link_sfx_key(actor, "key", 1)
```

---

## get_trigger_list_variable_all_link_sfx_key

method in GameAPI

- 描述

    获取全局触发器LINK_SFX_KEY数组变量

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
local result = GameAPI.get_trigger_list_variable_all_link_sfx_key("key")
```

---

## get_trigger_list_actor_variable_all_link_sfx_key

method in GameAPI

- 描述

    获取触发器LINK_SFX_KEY 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_link_sfx_key(actor, "key")
```

---

## get_trigger_variable_cursor_key

method in GameAPI

- 描述

    获取全局触发器CURSOR_KEY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CursorKey | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_cursor_key("key")
```

---

## get_trigger_actor_variable_cursor_key

method in GameAPI

- 描述

    获取触发器CURSOR_KEY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CursorKey | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_cursor_key(actor, "key")
```

---

## get_trigger_list_variable_cursor_key

method in GameAPI

- 描述

    获取全局触发器CURSOR_KEY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CursorKey | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_cursor_key("key", 1)
```

---

## get_trigger_list_actor_variable_cursor_key

method in GameAPI

- 描述

    获取触发器CURSOR_KEY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CursorKey | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_cursor_key(actor, "key", 1)
```

---

## get_trigger_list_variable_all_cursor_key

method in GameAPI

- 描述

    获取全局触发器CURSOR_KEY数组变量

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
local result = GameAPI.get_trigger_list_variable_all_cursor_key("key")
```

---

## get_trigger_list_actor_variable_all_cursor_key

method in GameAPI

- 描述

    获取触发器CURSOR_KEY 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_cursor_key(actor, "key")
```

---

## get_trigger_variable_image_key

method in GameAPI

- 描述

    获取全局触发器IMAGE_KEY非数组变量

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
local result = GameAPI.get_trigger_variable_image_key("key")
```

---

## get_trigger_actor_variable_image_key

method in GameAPI

- 描述

    获取触发器IMAGE_KEY非数组 组变量

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

local result = GameAPI.get_trigger_actor_variable_image_key(actor, "key")
```

---

## get_trigger_list_variable_image_key

method in GameAPI

- 描述

    获取全局触发器IMAGE_KEY数组变量子项

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
local result = GameAPI.get_trigger_list_variable_image_key("key", 1)
```

---

## get_trigger_list_actor_variable_image_key

method in GameAPI

- 描述

    获取触发器IMAGE_KEY数组 组变量子项

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

local result = GameAPI.get_trigger_list_actor_variable_image_key(actor, "key", 1)
```

---

## get_trigger_list_variable_all_image_key

method in GameAPI

- 描述

    获取全局触发器IMAGE_KEY数组变量

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
local result = GameAPI.get_trigger_list_variable_all_image_key("key")
```

---

## get_trigger_list_actor_variable_all_image_key

method in GameAPI

- 描述

    获取触发器IMAGE_KEY 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_image_key(actor, "key")
```

---

## get_trigger_variable_angle

method in GameAPI

- 描述

    获取全局触发器ANGLE非数组变量

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
local result = GameAPI.get_trigger_variable_angle("key")
```

---

## get_trigger_actor_variable_angle

method in GameAPI

- 描述

    获取触发器ANGLE非数组 组变量

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

local result = GameAPI.get_trigger_actor_variable_angle(actor, "key")
```

---

## get_trigger_list_variable_angle

method in GameAPI

- 描述

    获取全局触发器ANGLE数组变量子项

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
local result = GameAPI.get_trigger_list_variable_angle("key", 1)
```

---

## get_trigger_list_actor_variable_angle

method in GameAPI

- 描述

    获取触发器ANGLE数组 组变量子项

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

local result = GameAPI.get_trigger_list_actor_variable_angle(actor, "key", 1)
```

---

## get_trigger_list_variable_all_angle

method in GameAPI

- 描述

    获取全局触发器ANGLE数组变量

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
local result = GameAPI.get_trigger_list_variable_all_angle("key")
```

---

## get_trigger_list_actor_variable_all_angle

method in GameAPI

- 描述

    获取触发器ANGLE 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_angle(actor, "key")
```

---

## get_trigger_variable_texture

method in GameAPI

- 描述

    获取全局触发器TEXTURE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Texture | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_texture("key")
```

---

## get_trigger_actor_variable_texture

method in GameAPI

- 描述

    获取触发器TEXTURE非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Texture | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_texture(actor, "key")
```

---

## get_trigger_list_variable_texture

method in GameAPI

- 描述

    获取全局触发器TEXTURE数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Texture | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_texture("key", 1)
```

---

## get_trigger_list_actor_variable_texture

method in GameAPI

- 描述

    获取触发器TEXTURE数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Texture | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_texture(actor, "key", 1)
```

---

## get_trigger_list_variable_all_texture

method in GameAPI

- 描述

    获取全局触发器TEXTURE数组变量

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
local result = GameAPI.get_trigger_list_variable_all_texture("key")
```

---

## get_trigger_list_actor_variable_all_texture

method in GameAPI

- 描述

    获取触发器TEXTURE 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_texture(actor, "key")
```

---

## get_trigger_variable_sequence

method in GameAPI

- 描述

    获取全局触发器SEQUENCE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sequence | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_sequence("key")
```

---

## get_trigger_actor_variable_sequence

method in GameAPI

- 描述

    获取触发器SEQUENCE非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sequence | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_sequence(actor, "key")
```

---

## get_trigger_list_variable_sequence

method in GameAPI

- 描述

    获取全局触发器SEQUENCE数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sequence | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_sequence("key", 1)
```

---

## get_trigger_list_actor_variable_sequence

method in GameAPI

- 描述

    获取触发器SEQUENCE数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sequence | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_sequence(actor, "key", 1)
```

---

## get_trigger_list_variable_all_sequence

method in GameAPI

- 描述

    获取全局触发器SEQUENCE数组变量

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
local result = GameAPI.get_trigger_list_variable_all_sequence("key")
```

---

## get_trigger_list_actor_variable_all_sequence

method in GameAPI

- 描述

    获取触发器SEQUENCE 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_sequence(actor, "key")
```

---

## get_trigger_variable_physics_object

method in GameAPI

- 描述

    获取全局触发器PHYSICS_OBJECT非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsObject | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_physics_object("key")
```

---

## get_trigger_actor_variable_physics_object

method in GameAPI

- 描述

    获取触发器PHYSICS_OBJECT非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsObject | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_physics_object(actor, "key")
```

---

## get_trigger_list_variable_physics_object

method in GameAPI

- 描述

    获取全局触发器PHYSICS_OBJECT数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsObject | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_physics_object("key", 1)
```

---

## get_trigger_list_actor_variable_physics_object

method in GameAPI

- 描述

    获取触发器PHYSICS_OBJECT数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsObject | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_physics_object(actor, "key", 1)
```

---

## get_trigger_list_variable_all_physics_object

method in GameAPI

- 描述

    获取全局触发器PHYSICS_OBJECT数组变量

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
local result = GameAPI.get_trigger_list_variable_all_physics_object("key")
```

---

## get_trigger_list_actor_variable_all_physics_object

method in GameAPI

- 描述

    获取触发器PHYSICS_OBJECT 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_physics_object(actor, "key")
```

---

## get_trigger_variable_physics_entity

method in GameAPI

- 描述

    获取全局触发器PHYSICS_ENTITY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsEntity | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_physics_entity("key")
```

---

## get_trigger_actor_variable_physics_entity

method in GameAPI

- 描述

    获取触发器PHYSICS_ENTITY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsEntity | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_physics_entity(actor, "key")
```

---

## get_trigger_list_variable_physics_entity

method in GameAPI

- 描述

    获取全局触发器PHYSICS_ENTITY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsEntity | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_physics_entity("key", 1)
```

---

## get_trigger_list_actor_variable_physics_entity

method in GameAPI

- 描述

    获取触发器PHYSICS_ENTITY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsEntity | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_physics_entity(actor, "key", 1)
```

---

## get_trigger_list_variable_all_physics_entity

method in GameAPI

- 描述

    获取全局触发器PHYSICS_ENTITY数组变量

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
local result = GameAPI.get_trigger_list_variable_all_physics_entity("key")
```

---

## get_trigger_list_actor_variable_all_physics_entity

method in GameAPI

- 描述

    获取触发器PHYSICS_ENTITY 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_physics_entity(actor, "key")
```

---

## get_trigger_variable_physics_object_key

method in GameAPI

- 描述

    获取全局触发器PHYSICS_OBJECT_KEY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsObjectKey | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_physics_object_key("key")
```

---

## get_trigger_actor_variable_physics_object_key

method in GameAPI

- 描述

    获取触发器PHYSICS_OBJECT_KEY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsObjectKey | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_physics_object_key(actor, "key")
```

---

## get_trigger_list_variable_physics_object_key

method in GameAPI

- 描述

    获取全局触发器PHYSICS_OBJECT_KEY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsObjectKey | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_physics_object_key("key", 1)
```

---

## get_trigger_list_actor_variable_physics_object_key

method in GameAPI

- 描述

    获取触发器PHYSICS_OBJECT_KEY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsObjectKey | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_physics_object_key(actor, "key", 1)
```

---

## get_trigger_list_variable_all_physics_object_key

method in GameAPI

- 描述

    获取全局触发器PHYSICS_OBJECT_KEY数组变量

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
local result = GameAPI.get_trigger_list_variable_all_physics_object_key("key")
```

---

## get_trigger_list_actor_variable_all_physics_object_key

method in GameAPI

- 描述

    获取触发器PHYSICS_OBJECT_KEY 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_physics_object_key(actor, "key")
```

---

## get_trigger_variable_physics_entity_key

method in GameAPI

- 描述

    获取全局触发器PHYSICS_ENTITY_KEY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsEntityKey | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_physics_entity_key("key")
```

---

## get_trigger_actor_variable_physics_entity_key

method in GameAPI

- 描述

    获取触发器PHYSICS_ENTITY_KEY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsEntityKey | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_physics_entity_key(actor, "key")
```

---

## get_trigger_list_variable_physics_entity_key

method in GameAPI

- 描述

    获取全局触发器PHYSICS_ENTITY_KEY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsEntityKey | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_physics_entity_key("key", 1)
```

---

## get_trigger_list_actor_variable_physics_entity_key

method in GameAPI

- 描述

    获取触发器PHYSICS_ENTITY_KEY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsEntityKey | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_physics_entity_key(actor, "key", 1)
```

---

## get_trigger_list_variable_all_physics_entity_key

method in GameAPI

- 描述

    获取全局触发器PHYSICS_ENTITY_KEY数组变量

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
local result = GameAPI.get_trigger_list_variable_all_physics_entity_key("key")
```

---

## get_trigger_list_actor_variable_all_physics_entity_key

method in GameAPI

- 描述

    获取触发器PHYSICS_ENTITY_KEY 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_physics_entity_key(actor, "key")
```

---

## get_trigger_variable_rigid_body

method in GameAPI

- 描述

    获取全局触发器RIGID_BODY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RigidBody | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_rigid_body("key")
```

---

## get_trigger_actor_variable_rigid_body

method in GameAPI

- 描述

    获取触发器RIGID_BODY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RigidBody | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_rigid_body(actor, "key")
```

---

## get_trigger_list_variable_rigid_body

method in GameAPI

- 描述

    获取全局触发器RIGID_BODY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RigidBody | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_rigid_body("key", 1)
```

---

## get_trigger_list_actor_variable_rigid_body

method in GameAPI

- 描述

    获取触发器RIGID_BODY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RigidBody | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_rigid_body(actor, "key", 1)
```

---

## get_trigger_list_variable_all_rigid_body

method in GameAPI

- 描述

    获取全局触发器RIGID_BODY数组变量

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
local result = GameAPI.get_trigger_list_variable_all_rigid_body("key")
```

---

## get_trigger_list_actor_variable_all_rigid_body

method in GameAPI

- 描述

    获取触发器RIGID_BODY 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_rigid_body(actor, "key")
```

---

## get_trigger_variable_rigid_body_group

method in GameAPI

- 描述

    获取全局触发器RIGID_BODY_GROUP非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RigidBodyGroup | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_rigid_body_group("key")
```

---

## get_trigger_actor_variable_rigid_body_group

method in GameAPI

- 描述

    获取触发器RIGID_BODY_GROUP非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RigidBodyGroup | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_rigid_body_group(actor, "key")
```

---

## get_trigger_list_variable_rigid_body_group

method in GameAPI

- 描述

    获取全局触发器RIGID_BODY_GROUP数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RigidBodyGroup | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_rigid_body_group("key", 1)
```

---

## get_trigger_list_actor_variable_rigid_body_group

method in GameAPI

- 描述

    获取触发器RIGID_BODY_GROUP数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RigidBodyGroup | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_rigid_body_group(actor, "key", 1)
```

---

## get_trigger_list_variable_all_rigid_body_group

method in GameAPI

- 描述

    获取全局触发器RIGID_BODY_GROUP数组变量

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
local result = GameAPI.get_trigger_list_variable_all_rigid_body_group("key")
```

---

## get_trigger_list_actor_variable_all_rigid_body_group

method in GameAPI

- 描述

    获取触发器RIGID_BODY_GROUP 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_rigid_body_group(actor, "key")
```

---

## get_trigger_variable_collider

method in GameAPI

- 描述

    获取全局触发器COLLIDER非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Collider | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_collider("key")
```

---

## get_trigger_actor_variable_collider

method in GameAPI

- 描述

    获取触发器COLLIDER非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Collider | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_collider(actor, "key")
```

---

## get_trigger_list_variable_collider

method in GameAPI

- 描述

    获取全局触发器COLLIDER数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Collider | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_collider("key", 1)
```

---

## get_trigger_list_actor_variable_collider

method in GameAPI

- 描述

    获取触发器COLLIDER数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Collider | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_collider(actor, "key", 1)
```

---

## get_trigger_list_variable_all_collider

method in GameAPI

- 描述

    获取全局触发器COLLIDER数组变量

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
local result = GameAPI.get_trigger_list_variable_all_collider("key")
```

---

## get_trigger_list_actor_variable_all_collider

method in GameAPI

- 描述

    获取触发器COLLIDER 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_collider(actor, "key")
```

---

## get_trigger_variable_joint

method in GameAPI

- 描述

    获取全局触发器JOINT非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Joint | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_joint("key")
```

---

## get_trigger_actor_variable_joint

method in GameAPI

- 描述

    获取触发器JOINT非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Joint | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_joint(actor, "key")
```

---

## get_trigger_list_variable_joint

method in GameAPI

- 描述

    获取全局触发器JOINT数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Joint | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_joint("key", 1)
```

---

## get_trigger_list_actor_variable_joint

method in GameAPI

- 描述

    获取触发器JOINT数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Joint | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_joint(actor, "key", 1)
```

---

## get_trigger_list_variable_all_joint

method in GameAPI

- 描述

    获取全局触发器JOINT数组变量

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
local result = GameAPI.get_trigger_list_variable_all_joint("key")
```

---

## get_trigger_list_actor_variable_all_joint

method in GameAPI

- 描述

    获取触发器JOINT 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_joint(actor, "key")
```

---

## get_trigger_variable_reaction

method in GameAPI

- 描述

    获取全局触发器REACTION非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Reaction | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_reaction("key")
```

---

## get_trigger_actor_variable_reaction

method in GameAPI

- 描述

    获取触发器REACTION非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Reaction | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_reaction(actor, "key")
```

---

## get_trigger_list_variable_reaction

method in GameAPI

- 描述

    获取全局触发器REACTION数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Reaction | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_reaction("key", 1)
```

---

## get_trigger_list_actor_variable_reaction

method in GameAPI

- 描述

    获取触发器REACTION数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Reaction | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_reaction(actor, "key", 1)
```

---

## get_trigger_list_variable_all_reaction

method in GameAPI

- 描述

    获取全局触发器REACTION数组变量

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
local result = GameAPI.get_trigger_list_variable_all_reaction("key")
```

---

## get_trigger_list_actor_variable_all_reaction

method in GameAPI

- 描述

    获取触发器REACTION 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_reaction(actor, "key")
```

---

## get_trigger_variable_reaction_group

method in GameAPI

- 描述

    获取全局触发器REACTION_GROUP非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ReactionGroup | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_reaction_group("key")
```

---

## get_trigger_actor_variable_reaction_group

method in GameAPI

- 描述

    获取触发器REACTION_GROUP非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ReactionGroup | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_reaction_group(actor, "key")
```

---

## get_trigger_list_variable_reaction_group

method in GameAPI

- 描述

    获取全局触发器REACTION_GROUP数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ReactionGroup | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_reaction_group("key", 1)
```

---

## get_trigger_list_actor_variable_reaction_group

method in GameAPI

- 描述

    获取触发器REACTION_GROUP数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ReactionGroup | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_reaction_group(actor, "key", 1)
```

---

## get_trigger_list_variable_all_reaction_group

method in GameAPI

- 描述

    获取全局触发器REACTION_GROUP数组变量

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
local result = GameAPI.get_trigger_list_variable_all_reaction_group("key")
```

---

## get_trigger_list_actor_variable_all_reaction_group

method in GameAPI

- 描述

    获取触发器REACTION_GROUP 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_reaction_group(actor, "key")
```

---

## get_trigger_variable_physics_filter

method in GameAPI

- 描述

    获取全局触发器PHYSICS_FILTER非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsFilter | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_physics_filter("key")
```

---

## get_trigger_actor_variable_physics_filter

method in GameAPI

- 描述

    获取触发器PHYSICS_FILTER非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsFilter | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_physics_filter(actor, "key")
```

---

## get_trigger_list_variable_physics_filter

method in GameAPI

- 描述

    获取全局触发器PHYSICS_FILTER数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsFilter | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_physics_filter("key", 1)
```

---

## get_trigger_list_actor_variable_physics_filter

method in GameAPI

- 描述

    获取触发器PHYSICS_FILTER数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsFilter | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_physics_filter(actor, "key", 1)
```

---

## get_trigger_list_variable_all_physics_filter

method in GameAPI

- 描述

    获取全局触发器PHYSICS_FILTER数组变量

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
local result = GameAPI.get_trigger_list_variable_all_physics_filter("key")
```

---

## get_trigger_list_actor_variable_all_physics_filter

method in GameAPI

- 描述

    获取触发器PHYSICS_FILTER 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_physics_filter(actor, "key")
```

---

## get_trigger_variable_int_save

method in GameAPI

- 描述

    获取全局触发器INT_SAVE非数组变量

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
local result = GameAPI.get_trigger_variable_int_save("key")
```

---

## get_trigger_actor_variable_int_save

method in GameAPI

- 描述

    获取触发器INT_SAVE非数组 组变量

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

local result = GameAPI.get_trigger_actor_variable_int_save(actor, "key")
```

---

## get_trigger_list_variable_int_save

method in GameAPI

- 描述

    获取全局触发器INT_SAVE数组变量子项

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
local result = GameAPI.get_trigger_list_variable_int_save("key", 1)
```

---

## get_trigger_list_actor_variable_int_save

method in GameAPI

- 描述

    获取触发器INT_SAVE数组 组变量子项

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

local result = GameAPI.get_trigger_list_actor_variable_int_save(actor, "key", 1)
```

---

## get_trigger_list_variable_all_int_save

method in GameAPI

- 描述

    获取全局触发器INT_SAVE数组变量

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
local result = GameAPI.get_trigger_list_variable_all_int_save("key")
```

---

## get_trigger_list_actor_variable_all_int_save

method in GameAPI

- 描述

    获取触发器INT_SAVE 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_int_save(actor, "key")
```

---

## get_trigger_variable_str_save

method in GameAPI

- 描述

    获取全局触发器STR_SAVE非数组变量

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
local result = GameAPI.get_trigger_variable_str_save("key")
```

---

## get_trigger_actor_variable_str_save

method in GameAPI

- 描述

    获取触发器STR_SAVE非数组 组变量

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

local result = GameAPI.get_trigger_actor_variable_str_save(actor, "key")
```

---

## get_trigger_list_variable_str_save

method in GameAPI

- 描述

    获取全局触发器STR_SAVE数组变量子项

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
local result = GameAPI.get_trigger_list_variable_str_save("key", 1)
```

---

## get_trigger_list_actor_variable_str_save

method in GameAPI

- 描述

    获取触发器STR_SAVE数组 组变量子项

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

local result = GameAPI.get_trigger_list_actor_variable_str_save(actor, "key", 1)
```

---

## get_trigger_list_variable_all_str_save

method in GameAPI

- 描述

    获取全局触发器STR_SAVE数组变量

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
local result = GameAPI.get_trigger_list_variable_all_str_save("key")
```

---

## get_trigger_list_actor_variable_all_str_save

method in GameAPI

- 描述

    获取触发器STR_SAVE 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_str_save(actor, "key")
```

---

## get_trigger_variable_float_save

method in GameAPI

- 描述

    获取全局触发器FLOAT_SAVE非数组变量

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
local result = GameAPI.get_trigger_variable_float_save("key")
```

---

## get_trigger_actor_variable_float_save

method in GameAPI

- 描述

    获取触发器FLOAT_SAVE非数组 组变量

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

local result = GameAPI.get_trigger_actor_variable_float_save(actor, "key")
```

---

## get_trigger_list_variable_float_save

method in GameAPI

- 描述

    获取全局触发器FLOAT_SAVE数组变量子项

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
local result = GameAPI.get_trigger_list_variable_float_save("key", 1)
```

---

## get_trigger_list_actor_variable_float_save

method in GameAPI

- 描述

    获取触发器FLOAT_SAVE数组 组变量子项

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

local result = GameAPI.get_trigger_list_actor_variable_float_save(actor, "key", 1)
```

---

## get_trigger_list_variable_all_float_save

method in GameAPI

- 描述

    获取全局触发器FLOAT_SAVE数组变量

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
local result = GameAPI.get_trigger_list_variable_all_float_save("key")
```

---

## get_trigger_list_actor_variable_all_float_save

method in GameAPI

- 描述

    获取触发器FLOAT_SAVE 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_float_save(actor, "key")
```

---

## get_trigger_variable_bool_save

method in GameAPI

- 描述

    获取全局触发器BOOL_SAVE非数组变量

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
local result = GameAPI.get_trigger_variable_bool_save("key")
```

---

## get_trigger_actor_variable_bool_save

method in GameAPI

- 描述

    获取触发器BOOL_SAVE非数组 组变量

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

local result = GameAPI.get_trigger_actor_variable_bool_save(actor, "key")
```

---

## get_trigger_list_variable_bool_save

method in GameAPI

- 描述

    获取全局触发器BOOL_SAVE数组变量子项

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
local result = GameAPI.get_trigger_list_variable_bool_save("key", 1)
```

---

## get_trigger_list_actor_variable_bool_save

method in GameAPI

- 描述

    获取触发器BOOL_SAVE数组 组变量子项

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

local result = GameAPI.get_trigger_list_actor_variable_bool_save(actor, "key", 1)
```

---

## get_trigger_list_variable_all_bool_save

method in GameAPI

- 描述

    获取全局触发器BOOL_SAVE数组变量

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
local result = GameAPI.get_trigger_list_variable_all_bool_save("key")
```

---

## get_trigger_list_actor_variable_all_bool_save

method in GameAPI

- 描述

    获取触发器BOOL_SAVE 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_bool_save(actor, "key")
```

---

## get_trigger_variable_table_save

method in GameAPI

- 描述

    获取全局触发器TABLE_SAVE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Table | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_table_save("key")
```

---

## get_trigger_actor_variable_table_save

method in GameAPI

- 描述

    获取触发器TABLE_SAVE非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Table | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_table_save(actor, "key")
```

---

## get_trigger_list_variable_table_save

method in GameAPI

- 描述

    获取全局触发器TABLE_SAVE数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Table | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_table_save("key", 1)
```

---

## get_trigger_list_actor_variable_table_save

method in GameAPI

- 描述

    获取触发器TABLE_SAVE数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Table | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_table_save(actor, "key", 1)
```

---

## get_trigger_list_variable_all_table_save

method in GameAPI

- 描述

    获取全局触发器TABLE_SAVE数组变量

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
local result = GameAPI.get_trigger_list_variable_all_table_save("key")
```

---

## get_trigger_list_actor_variable_all_table_save

method in GameAPI

- 描述

    获取触发器TABLE_SAVE 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_table_save(actor, "key")
```

---

## get_trigger_variable_global_archive_slot

method in GameAPI

- 描述

    获取全局触发器GLOBAL_ARCHIVE_SLOT非数组变量

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
local result = GameAPI.get_trigger_variable_global_archive_slot("key")
```

---

## get_trigger_actor_variable_global_archive_slot

method in GameAPI

- 描述

    获取触发器GLOBAL_ARCHIVE_SLOT非数组 组变量

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

local result = GameAPI.get_trigger_actor_variable_global_archive_slot(actor, "key")
```

---

## get_trigger_list_variable_global_archive_slot

method in GameAPI

- 描述

    获取全局触发器GLOBAL_ARCHIVE_SLOT数组变量子项

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
local result = GameAPI.get_trigger_list_variable_global_archive_slot("key", 1)
```

---

## get_trigger_list_actor_variable_global_archive_slot

method in GameAPI

- 描述

    获取触发器GLOBAL_ARCHIVE_SLOT数组 组变量子项

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

local result = GameAPI.get_trigger_list_actor_variable_global_archive_slot(actor, "key", 1)
```

---

## get_trigger_list_variable_all_global_archive_slot

method in GameAPI

- 描述

    获取全局触发器GLOBAL_ARCHIVE_SLOT数组变量

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
local result = GameAPI.get_trigger_list_variable_all_global_archive_slot("key")
```

---

## get_trigger_list_actor_variable_all_global_archive_slot

method in GameAPI

- 描述

    获取触发器GLOBAL_ARCHIVE_SLOT 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_global_archive_slot(actor, "key")
```

---

## get_trigger_variable_random_pool_drop

method in GameAPI

- 描述

    获取全局触发器RANDOM_POOL_DROP非数组变量

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
local result = GameAPI.get_trigger_variable_random_pool_drop("key")
```

---

## get_trigger_actor_variable_random_pool_drop

method in GameAPI

- 描述

    获取触发器RANDOM_POOL_DROP非数组 组变量

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

local result = GameAPI.get_trigger_actor_variable_random_pool_drop(actor, "key")
```

---

## get_trigger_list_variable_random_pool_drop

method in GameAPI

- 描述

    获取全局触发器RANDOM_POOL_DROP数组变量子项

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
local result = GameAPI.get_trigger_list_variable_random_pool_drop("key", 1)
```

---

## get_trigger_list_actor_variable_random_pool_drop

method in GameAPI

- 描述

    获取触发器RANDOM_POOL_DROP数组 组变量子项

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

local result = GameAPI.get_trigger_list_actor_variable_random_pool_drop(actor, "key", 1)
```

---

## get_trigger_list_variable_all_random_pool_drop

method in GameAPI

- 描述

    获取全局触发器RANDOM_POOL_DROP数组变量

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
local result = GameAPI.get_trigger_list_variable_all_random_pool_drop("key")
```

---

## get_trigger_list_actor_variable_all_random_pool_drop

method in GameAPI

- 描述

    获取触发器RANDOM_POOL_DROP 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_random_pool_drop(actor, "key")
```

---

## get_trigger_variable_dynamic_trigger_instance

method in GameAPI

- 描述

    获取全局触发器DYNAMIC_TRIGGER_INSTANCE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DynamicTriggerInstance | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_dynamic_trigger_instance("key")
```

---

## get_trigger_actor_variable_dynamic_trigger_instance

method in GameAPI

- 描述

    获取触发器DYNAMIC_TRIGGER_INSTANCE非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DynamicTriggerInstance | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_dynamic_trigger_instance(actor, "key")
```

---

## get_trigger_list_variable_dynamic_trigger_instance

method in GameAPI

- 描述

    获取全局触发器DYNAMIC_TRIGGER_INSTANCE数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DynamicTriggerInstance | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_dynamic_trigger_instance("key", 1)
```

---

## get_trigger_list_actor_variable_dynamic_trigger_instance

method in GameAPI

- 描述

    获取触发器DYNAMIC_TRIGGER_INSTANCE数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DynamicTriggerInstance | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_dynamic_trigger_instance(actor, "key", 1)
```

---

## get_trigger_list_variable_all_dynamic_trigger_instance

method in GameAPI

- 描述

    获取全局触发器DYNAMIC_TRIGGER_INSTANCE数组变量

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
local result = GameAPI.get_trigger_list_variable_all_dynamic_trigger_instance("key")
```

---

## get_trigger_list_actor_variable_all_dynamic_trigger_instance

method in GameAPI

- 描述

    获取触发器DYNAMIC_TRIGGER_INSTANCE 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_dynamic_trigger_instance(actor, "key")
```

---

## get_trigger_variable_table

method in GameAPI

- 描述

    获取全局触发器TABLE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Table | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_table("key")
```

---

## get_trigger_actor_variable_table

method in GameAPI

- 描述

    获取触发器TABLE非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Table | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_table(actor, "key")
```

---

## get_trigger_list_variable_table

method in GameAPI

- 描述

    获取全局触发器TABLE数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Table | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_table("key", 1)
```

---

## get_trigger_list_actor_variable_table

method in GameAPI

- 描述

    获取触发器TABLE数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Table | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_table(actor, "key", 1)
```

---

## get_trigger_list_variable_all_table

method in GameAPI

- 描述

    获取全局触发器TABLE数组变量

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
local result = GameAPI.get_trigger_list_variable_all_table("key")
```

---

## get_trigger_list_actor_variable_all_table

method in GameAPI

- 描述

    获取触发器TABLE 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_table(actor, "key")
```

---

## get_trigger_variable_random_pool

method in GameAPI

- 描述

    获取全局触发器RANDOM_POOL非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RandomPool | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_random_pool("key")
```

---

## get_trigger_actor_variable_random_pool

method in GameAPI

- 描述

    获取触发器RANDOM_POOL非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RandomPool | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_random_pool(actor, "key")
```

---

## get_trigger_list_variable_random_pool

method in GameAPI

- 描述

    获取全局触发器RANDOM_POOL数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RandomPool | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_random_pool("key", 1)
```

---

## get_trigger_list_actor_variable_random_pool

method in GameAPI

- 描述

    获取触发器RANDOM_POOL数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RandomPool | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_random_pool(actor, "key", 1)
```

---

## get_trigger_list_variable_all_random_pool

method in GameAPI

- 描述

    获取全局触发器RANDOM_POOL数组变量

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
local result = GameAPI.get_trigger_list_variable_all_random_pool("key")
```

---

## get_trigger_list_actor_variable_all_random_pool

method in GameAPI

- 描述

    获取触发器RANDOM_POOL 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_random_pool(actor, "key")
```

---

## get_trigger_variable_scene_ui

method in GameAPI

- 描述

    获取全局触发器SCENE_UI非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SceneNode | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_scene_ui("key")
```

---

## get_trigger_actor_variable_scene_ui

method in GameAPI

- 描述

    获取触发器SCENE_UI非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SceneNode | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_scene_ui(actor, "key")
```

---

## get_trigger_list_variable_scene_ui

method in GameAPI

- 描述

    获取全局触发器SCENE_UI数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SceneNode | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_scene_ui("key", 1)
```

---

## get_trigger_list_actor_variable_scene_ui

method in GameAPI

- 描述

    获取触发器SCENE_UI数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SceneNode | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_scene_ui(actor, "key", 1)
```

---

## get_trigger_list_variable_all_scene_ui

method in GameAPI

- 描述

    获取全局触发器SCENE_UI数组变量

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
local result = GameAPI.get_trigger_list_variable_all_scene_ui("key")
```

---

## get_trigger_list_actor_variable_all_scene_ui

method in GameAPI

- 描述

    获取触发器SCENE_UI 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_scene_ui(actor, "key")
```

---

## get_trigger_variable_damage_type

method in GameAPI

- 描述

    获取全局触发器DAMAGE_TYPE非数组变量

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
local result = GameAPI.get_trigger_variable_damage_type("key")
```

---

## get_trigger_actor_variable_damage_type

method in GameAPI

- 描述

    获取触发器DAMAGE_TYPE非数组 组变量

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

local result = GameAPI.get_trigger_actor_variable_damage_type(actor, "key")
```

---

## get_trigger_list_variable_damage_type

method in GameAPI

- 描述

    获取全局触发器DAMAGE_TYPE数组变量子项

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
local result = GameAPI.get_trigger_list_variable_damage_type("key", 1)
```

---

## get_trigger_list_actor_variable_damage_type

method in GameAPI

- 描述

    获取触发器DAMAGE_TYPE数组 组变量子项

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

local result = GameAPI.get_trigger_list_actor_variable_damage_type(actor, "key", 1)
```

---

## get_trigger_list_variable_all_damage_type

method in GameAPI

- 描述

    获取全局触发器DAMAGE_TYPE数组变量

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
local result = GameAPI.get_trigger_list_variable_all_damage_type("key")
```

---

## get_trigger_list_actor_variable_all_damage_type

method in GameAPI

- 描述

    获取触发器DAMAGE_TYPE 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_damage_type(actor, "key")
```

---

## get_trigger_variable_new_timer

method in GameAPI

- 描述

    获取全局触发器NEW_TIMER非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Timer | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_new_timer("key")
```

---

## get_trigger_actor_variable_new_timer

method in GameAPI

- 描述

    获取触发器NEW_TIMER非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Timer | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_new_timer(actor, "key")
```

---

## get_trigger_list_variable_new_timer

method in GameAPI

- 描述

    获取全局触发器NEW_TIMER数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Timer | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_new_timer("key", 1)
```

---

## get_trigger_list_actor_variable_new_timer

method in GameAPI

- 描述

    获取触发器NEW_TIMER数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Timer | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_new_timer(actor, "key", 1)
```

---

## get_trigger_list_variable_all_new_timer

method in GameAPI

- 描述

    获取全局触发器NEW_TIMER数组变量

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
local result = GameAPI.get_trigger_list_variable_all_new_timer("key")
```

---

## get_trigger_list_actor_variable_all_new_timer

method in GameAPI

- 描述

    获取触发器NEW_TIMER 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_new_timer(actor, "key")
```

---

## get_trigger_variable_tech_key

method in GameAPI

- 描述

    获取全局触发器TECH_KEY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.TechKey | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_tech_key("key")
```

---

## get_trigger_actor_variable_tech_key

method in GameAPI

- 描述

    获取触发器TECH_KEY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.TechKey | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_tech_key(actor, "key")
```

---

## get_trigger_list_variable_tech_key

method in GameAPI

- 描述

    获取全局触发器TECH_KEY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.TechKey | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_tech_key("key", 1)
```

---

## get_trigger_list_actor_variable_tech_key

method in GameAPI

- 描述

    获取触发器TECH_KEY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.TechKey | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_tech_key(actor, "key", 1)
```

---

## get_trigger_list_variable_all_tech_key

method in GameAPI

- 描述

    获取全局触发器TECH_KEY数组变量

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
local result = GameAPI.get_trigger_list_variable_all_tech_key("key")
```

---

## get_trigger_list_actor_variable_all_tech_key

method in GameAPI

- 描述

    获取触发器TECH_KEY 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_tech_key(actor, "key")
```

---

## get_trigger_variable_store_key

method in GameAPI

- 描述

    获取全局触发器STORE_KEY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.StoreKey | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_store_key("key")
```

---

## get_trigger_actor_variable_store_key

method in GameAPI

- 描述

    获取触发器STORE_KEY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.StoreKey | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_store_key(actor, "key")
```

---

## get_trigger_list_variable_store_key

method in GameAPI

- 描述

    获取全局触发器STORE_KEY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.StoreKey | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_store_key("key", 1)
```

---

## get_trigger_list_actor_variable_store_key

method in GameAPI

- 描述

    获取触发器STORE_KEY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.StoreKey | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_store_key(actor, "key", 1)
```

---

## get_trigger_list_variable_all_store_key

method in GameAPI

- 描述

    获取全局触发器STORE_KEY数组变量

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
local result = GameAPI.get_trigger_list_variable_all_store_key("key")
```

---

## get_trigger_list_actor_variable_all_store_key

method in GameAPI

- 描述

    获取触发器STORE_KEY 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_store_key(actor, "key")
```

---

## get_trigger_variable_keyboard_key

method in GameAPI

- 描述

    获取全局触发器KEYBOARD_KEY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.KeyboardKey | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_keyboard_key("key")
```

---

## get_trigger_actor_variable_keyboard_key

method in GameAPI

- 描述

    获取触发器KEYBOARD_KEY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.KeyboardKey | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_keyboard_key(actor, "key")
```

---

## get_trigger_list_variable_keyboard_key

method in GameAPI

- 描述

    获取全局触发器KEYBOARD_KEY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.KeyboardKey | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_keyboard_key("key", 1)
```

---

## get_trigger_list_actor_variable_keyboard_key

method in GameAPI

- 描述

    获取触发器KEYBOARD_KEY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.KeyboardKey | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_keyboard_key(actor, "key", 1)
```

---

## get_trigger_list_variable_all_keyboard_key

method in GameAPI

- 描述

    获取全局触发器KEYBOARD_KEY数组变量

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
local result = GameAPI.get_trigger_list_variable_all_keyboard_key("key")
```

---

## get_trigger_list_actor_variable_all_keyboard_key

method in GameAPI

- 描述

    获取触发器KEYBOARD_KEY 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_keyboard_key(actor, "key")
```

---

## get_trigger_variable_unit_type

method in GameAPI

- 描述

    获取全局触发器UNIT_TYPE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitType | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_unit_type("key")
```

---

## get_trigger_actor_variable_unit_type

method in GameAPI

- 描述

    获取触发器UNIT_TYPE非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitType | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_unit_type(actor, "key")
```

---

## get_trigger_list_variable_unit_type

method in GameAPI

- 描述

    获取全局触发器UNIT_TYPE数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitType | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_unit_type("key", 1)
```

---

## get_trigger_list_actor_variable_unit_type

method in GameAPI

- 描述

    获取触发器UNIT_TYPE数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitType | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_unit_type(actor, "key", 1)
```

---

## get_trigger_list_variable_all_unit_type

method in GameAPI

- 描述

    获取全局触发器UNIT_TYPE数组变量

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
local result = GameAPI.get_trigger_list_variable_all_unit_type("key")
```

---

## get_trigger_list_actor_variable_all_unit_type

method in GameAPI

- 描述

    获取触发器UNIT_TYPE 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_unit_type(actor, "key")
```

---

## get_trigger_variable_curved_path

method in GameAPI

- 描述

    获取全局触发器CURVED_PATH非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CurvedPath | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_curved_path("key")
```

---

## get_trigger_actor_variable_curved_path

method in GameAPI

- 描述

    获取触发器CURVED_PATH非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CurvedPath | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_curved_path(actor, "key")
```

---

## get_trigger_list_variable_curved_path

method in GameAPI

- 描述

    获取全局触发器CURVED_PATH数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CurvedPath | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_curved_path("key", 1)
```

---

## get_trigger_list_actor_variable_curved_path

method in GameAPI

- 描述

    获取触发器CURVED_PATH数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CurvedPath | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_curved_path(actor, "key", 1)
```

---

## get_trigger_list_variable_all_curved_path

method in GameAPI

- 描述

    获取全局触发器CURVED_PATH数组变量

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
local result = GameAPI.get_trigger_list_variable_all_curved_path("key")
```

---

## get_trigger_list_actor_variable_all_curved_path

method in GameAPI

- 描述

    获取触发器CURVED_PATH 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_curved_path(actor, "key")
```

---

## get_trigger_variable_curved_path_3d

method in GameAPI

- 描述

    获取全局触发器CURVED_PATH_3D非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CurvedPath3D | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_curved_path_3d("key")
```

---

## get_trigger_actor_variable_curved_path_3d

method in GameAPI

- 描述

    获取触发器CURVED_PATH_3D非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CurvedPath3D | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_curved_path_3d(actor, "key")
```

---

## get_trigger_list_variable_curved_path_3d

method in GameAPI

- 描述

    获取全局触发器CURVED_PATH_3D数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CurvedPath3D | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_curved_path_3d("key", 1)
```

---

## get_trigger_list_actor_variable_curved_path_3d

method in GameAPI

- 描述

    获取触发器CURVED_PATH_3D数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CurvedPath3D | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_curved_path_3d(actor, "key", 1)
```

---

## get_trigger_list_variable_all_curved_path_3d

method in GameAPI

- 描述

    获取全局触发器CURVED_PATH_3D数组变量

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
local result = GameAPI.get_trigger_list_variable_all_curved_path_3d("key")
```

---

## get_trigger_list_actor_variable_all_curved_path_3d

method in GameAPI

- 描述

    获取触发器CURVED_PATH_3D 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_curved_path_3d(actor, "key")
```

---

## set_trigger_variable_by_type

method in GameAPI

- 描述

    设置全局触发器非数组变量（指定类型）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value | py.Actor | 值 |
    | var_type | string | 类型 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_variable_by_type("key", actor, "var_type")
```

---

## set_trigger_list_variable_by_type

method in GameAPI

- 描述

    设置全局触发器数组变量子项（指定类型）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value | py.Actor | 值 |
    | var_type | string | 类型 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_list_variable_by_type("key", 1, actor, "var_type")
```

---

## set_trigger_list_variable_boolean

method in GameAPI

- 描述

    设置全局触发器BOOLEAN数组变量子项

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
GameAPI.set_trigger_list_variable_boolean("key", 1, true)
```

---

## set_trigger_list_actor_variable_boolean

method in GameAPI

- 描述

    设置全局触发器BOOLEAN数组 组变量子项

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

GameAPI.set_trigger_list_actor_variable_boolean(actor, "key", 1, true)
```

---

## set_trigger_variable_boolean

method in GameAPI

- 描述

    设置全局触发器BOOLEAN非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | boolean | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_boolean("key", true)
```

---

## set_trigger_actor_variable_boolean

method in GameAPI

- 描述

    设置全局触发器BOOLEAN非数组 组变量

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

GameAPI.set_trigger_actor_variable_boolean(actor, "key", true)
```

---

## set_trigger_list_variable_integer

method in GameAPI

- 描述

    设置全局触发器INTEGER数组变量子项

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
GameAPI.set_trigger_list_variable_integer("key", 1, 1)
```

---

## set_trigger_list_actor_variable_integer

method in GameAPI

- 描述

    设置全局触发器INTEGER数组 组变量子项

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

GameAPI.set_trigger_list_actor_variable_integer(actor, "key", 1, 1)
```

---

## set_trigger_variable_integer

method in GameAPI

- 描述

    设置全局触发器INTEGER非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | integer | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_integer("key", 1)
```

---

## set_trigger_actor_variable_integer

method in GameAPI

- 描述

    设置全局触发器INTEGER非数组 组变量

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

GameAPI.set_trigger_actor_variable_integer(actor, "key", 1)
```

---

## set_trigger_list_variable_float

method in GameAPI

- 描述

    设置全局触发器FLOAT数组变量子项

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
GameAPI.set_trigger_list_variable_float("key", 1, Fix32(1))
```

---

## set_trigger_list_actor_variable_float

method in GameAPI

- 描述

    设置全局触发器FLOAT数组 组变量子项

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

GameAPI.set_trigger_list_actor_variable_float(actor, "key", 1, Fix32(1))
```

---

## set_trigger_variable_float

method in GameAPI

- 描述

    设置全局触发器FLOAT非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.Fixed | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_float("key", Fix32(1))
```

---

## set_trigger_actor_variable_float

method in GameAPI

- 描述

    设置全局触发器FLOAT非数组 组变量

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

GameAPI.set_trigger_actor_variable_float(actor, "key", Fix32(1))
```

---

## set_trigger_list_variable_string

method in GameAPI

- 描述

    设置全局触发器STRING数组变量子项

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
GameAPI.set_trigger_list_variable_string("key", 1, "value")
```

---

## set_trigger_list_actor_variable_string

method in GameAPI

- 描述

    设置全局触发器STRING数组 组变量子项

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

GameAPI.set_trigger_list_actor_variable_string(actor, "key", 1, "value")
```

---

## set_trigger_variable_string

method in GameAPI

- 描述

    设置全局触发器STRING非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | string | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_string("key", "value")
```

---

## set_trigger_actor_variable_string

method in GameAPI

- 描述

    设置全局触发器STRING非数组 组变量

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

GameAPI.set_trigger_actor_variable_string(actor, "key", "value")
```

---

## set_trigger_list_variable_ui_comp

method in GameAPI

- 描述

    设置全局触发器UI_COMP数组变量子项

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
GameAPI.set_trigger_list_variable_ui_comp("key", 1, "value")
```

---

## set_trigger_list_actor_variable_ui_comp

method in GameAPI

- 描述

    设置全局触发器UI_COMP数组 组变量子项

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

GameAPI.set_trigger_list_actor_variable_ui_comp(actor, "key", 1, "value")
```

---

## set_trigger_variable_ui_comp

method in GameAPI

- 描述

    设置全局触发器UI_COMP非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | string | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_ui_comp("key", "value")
```

---

## set_trigger_actor_variable_ui_comp

method in GameAPI

- 描述

    设置全局触发器UI_COMP非数组 组变量

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

GameAPI.set_trigger_actor_variable_ui_comp(actor, "key", "value")
```

---

## set_trigger_list_variable_ui_comp_type

method in GameAPI

- 描述

    设置全局触发器UI_COMP_TYPE数组变量子项

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
GameAPI.set_trigger_list_variable_ui_comp_type("key", 1, 1)
```

---

## set_trigger_list_actor_variable_ui_comp_type

method in GameAPI

- 描述

    设置全局触发器UI_COMP_TYPE数组 组变量子项

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

GameAPI.set_trigger_list_actor_variable_ui_comp_type(actor, "key", 1, 1)
```

---

## set_trigger_variable_ui_comp_type

method in GameAPI

- 描述

    设置全局触发器UI_COMP_TYPE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | integer | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_ui_comp_type("key", 1)
```

---

## set_trigger_actor_variable_ui_comp_type

method in GameAPI

- 描述

    设置全局触发器UI_COMP_TYPE非数组 组变量

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

GameAPI.set_trigger_actor_variable_ui_comp_type(actor, "key", 1)
```

---

## set_trigger_list_variable_ui_comp_event_type

method in GameAPI

- 描述

    设置全局触发器UI_COMP_EVENT_TYPE数组变量子项

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
GameAPI.set_trigger_list_variable_ui_comp_event_type("key", 1, 1)
```

---

## set_trigger_list_actor_variable_ui_comp_event_type

method in GameAPI

- 描述

    设置全局触发器UI_COMP_EVENT_TYPE数组 组变量子项

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

GameAPI.set_trigger_list_actor_variable_ui_comp_event_type(actor, "key", 1, 1)
```

---

## set_trigger_variable_ui_comp_event_type

method in GameAPI

- 描述

    设置全局触发器UI_COMP_EVENT_TYPE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | integer | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_ui_comp_event_type("key", 1)
```

---

## set_trigger_actor_variable_ui_comp_event_type

method in GameAPI

- 描述

    设置全局触发器UI_COMP_EVENT_TYPE非数组 组变量

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

GameAPI.set_trigger_actor_variable_ui_comp_event_type(actor, "key", 1)
```

---

## set_trigger_list_variable_ui_comp_align_type

method in GameAPI

- 描述

    设置全局触发器UI_COMP_ALIGN_TYPE数组变量子项

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
GameAPI.set_trigger_list_variable_ui_comp_align_type("key", 1, 1)
```

---

## set_trigger_list_actor_variable_ui_comp_align_type

method in GameAPI

- 描述

    设置全局触发器UI_COMP_ALIGN_TYPE数组 组变量子项

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

GameAPI.set_trigger_list_actor_variable_ui_comp_align_type(actor, "key", 1, 1)
```

---

## set_trigger_variable_ui_comp_align_type

method in GameAPI

- 描述

    设置全局触发器UI_COMP_ALIGN_TYPE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | integer | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_ui_comp_align_type("key", 1)
```

---

## set_trigger_actor_variable_ui_comp_align_type

method in GameAPI

- 描述

    设置全局触发器UI_COMP_ALIGN_TYPE非数组 组变量

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

GameAPI.set_trigger_actor_variable_ui_comp_align_type(actor, "key", 1)
```

---

## set_trigger_list_variable_ui_prefab

method in GameAPI

- 描述

    设置全局触发器UI_PREFAB数组变量子项

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
GameAPI.set_trigger_list_variable_ui_prefab("key", 1, "value")
```

---

## set_trigger_list_actor_variable_ui_prefab

method in GameAPI

- 描述

    设置全局触发器UI_PREFAB数组 组变量子项

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

GameAPI.set_trigger_list_actor_variable_ui_prefab(actor, "key", 1, "value")
```

---

## set_trigger_variable_ui_prefab

method in GameAPI

- 描述

    设置全局触发器UI_PREFAB非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | string | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_ui_prefab("key", "value")
```

---

## set_trigger_actor_variable_ui_prefab

method in GameAPI

- 描述

    设置全局触发器UI_PREFAB非数组 组变量

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

GameAPI.set_trigger_actor_variable_ui_prefab(actor, "key", "value")
```

---

## set_trigger_list_variable_ui_prefab_instance

method in GameAPI

- 描述

    设置全局触发器UI_PREFAB_INSTANCE数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.UIPrefabIns | 值 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui_prefab_ins = GameAPI.get_ui_prefab_ins(player.handle, "prefab_uid")

GameAPI.set_trigger_list_variable_ui_prefab_instance("key", 1)
```

---

## set_trigger_list_actor_variable_ui_prefab_instance

method in GameAPI

- 描述

    设置全局触发器UI_PREFAB_INSTANCE数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.UIPrefabIns | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local player = y3.player.get_by_id(1)
local ui_prefab_ins = GameAPI.get_ui_prefab_ins(player.handle, "prefab_uid")

GameAPI.set_trigger_list_actor_variable_ui_prefab_instance(actor, "key", 1)
```

---

## set_trigger_variable_ui_prefab_instance

method in GameAPI

- 描述

    设置全局触发器UI_PREFAB_INSTANCE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.UIPrefabIns | 值 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui_prefab_ins = GameAPI.get_ui_prefab_ins(player.handle, "prefab_uid")

GameAPI.set_trigger_variable_ui_prefab_instance("key")
```

---

## set_trigger_actor_variable_ui_prefab_instance

method in GameAPI

- 描述

    设置全局触发器UI_PREFAB_INSTANCE非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.UIPrefabIns | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local player = y3.player.get_by_id(1)
local ui_prefab_ins = GameAPI.get_ui_prefab_ins(player.handle, "prefab_uid")

GameAPI.set_trigger_actor_variable_ui_prefab_instance(actor, "key")
```

---

## set_trigger_list_variable_ui_prefab_ins_uid

method in GameAPI

- 描述

    设置全局触发器UI_PREFAB_INS_UID数组变量子项

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
GameAPI.set_trigger_list_variable_ui_prefab_ins_uid("key", 1, "value")
```

---

## set_trigger_list_actor_variable_ui_prefab_ins_uid

method in GameAPI

- 描述

    设置全局触发器UI_PREFAB_INS_UID数组 组变量子项

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

GameAPI.set_trigger_list_actor_variable_ui_prefab_ins_uid(actor, "key", 1, "value")
```

---

## set_trigger_variable_ui_prefab_ins_uid

method in GameAPI

- 描述

    设置全局触发器UI_PREFAB_INS_UID非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | string | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_ui_prefab_ins_uid("key", "value")
```

---

## set_trigger_actor_variable_ui_prefab_ins_uid

method in GameAPI

- 描述

    设置全局触发器UI_PREFAB_INS_UID非数组 组变量

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

GameAPI.set_trigger_actor_variable_ui_prefab_ins_uid(actor, "key", "value")
```

---

## set_trigger_list_variable_ui_direction

method in GameAPI

- 描述

    设置全局触发器UI_DIRECTION数组变量子项

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
GameAPI.set_trigger_list_variable_ui_direction("key", 1, 1)
```

---

## set_trigger_list_actor_variable_ui_direction

method in GameAPI

- 描述

    设置全局触发器UI_DIRECTION数组 组变量子项

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

GameAPI.set_trigger_list_actor_variable_ui_direction(actor, "key", 1, 1)
```

---

## set_trigger_variable_ui_direction

method in GameAPI

- 描述

    设置全局触发器UI_DIRECTION非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | integer | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_ui_direction("key", 1)
```

---

## set_trigger_actor_variable_ui_direction

method in GameAPI

- 描述

    设置全局触发器UI_DIRECTION非数组 组变量

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

GameAPI.set_trigger_actor_variable_ui_direction(actor, "key", 1)
```

---

## set_trigger_list_variable_ui_model_camera_mod

method in GameAPI

- 描述

    设置全局触发器UI_MODEL_CAMERA_MOD数组变量子项

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
GameAPI.set_trigger_list_variable_ui_model_camera_mod("key", 1, 1)
```

---

## set_trigger_list_actor_variable_ui_model_camera_mod

method in GameAPI

- 描述

    设置全局触发器UI_MODEL_CAMERA_MOD数组 组变量子项

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

GameAPI.set_trigger_list_actor_variable_ui_model_camera_mod(actor, "key", 1, 1)
```

---

## set_trigger_variable_ui_model_camera_mod

method in GameAPI

- 描述

    设置全局触发器UI_MODEL_CAMERA_MOD非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | integer | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_ui_model_camera_mod("key", 1)
```

---

## set_trigger_actor_variable_ui_model_camera_mod

method in GameAPI

- 描述

    设置全局触发器UI_MODEL_CAMERA_MOD非数组 组变量

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

GameAPI.set_trigger_actor_variable_ui_model_camera_mod(actor, "key", 1)
```

---

## set_trigger_list_variable_ui_btn_status

method in GameAPI

- 描述

    设置全局触发器UI_BTN_STATUS数组变量子项

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
GameAPI.set_trigger_list_variable_ui_btn_status("key", 1, 1)
```

---

## set_trigger_list_actor_variable_ui_btn_status

method in GameAPI

- 描述

    设置全局触发器UI_BTN_STATUS数组 组变量子项

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

GameAPI.set_trigger_list_actor_variable_ui_btn_status(actor, "key", 1, 1)
```

---

## set_trigger_variable_ui_btn_status

method in GameAPI

- 描述

    设置全局触发器UI_BTN_STATUS非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | integer | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_ui_btn_status("key", 1)
```

---

## set_trigger_actor_variable_ui_btn_status

method in GameAPI

- 描述

    设置全局触发器UI_BTN_STATUS非数组 组变量

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

GameAPI.set_trigger_actor_variable_ui_btn_status(actor, "key", 1)
```

---

## set_trigger_list_variable_ui_scrollview_type

method in GameAPI

- 描述

    设置全局触发器UI_SCROLLVIEW_TYPE数组变量子项

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
GameAPI.set_trigger_list_variable_ui_scrollview_type("key", 1, 1)
```

---

## set_trigger_list_actor_variable_ui_scrollview_type

method in GameAPI

- 描述

    设置全局触发器UI_SCROLLVIEW_TYPE数组 组变量子项

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

GameAPI.set_trigger_list_actor_variable_ui_scrollview_type(actor, "key", 1, 1)
```

---

## set_trigger_variable_ui_scrollview_type

method in GameAPI

- 描述

    设置全局触发器UI_SCROLLVIEW_TYPE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | integer | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_ui_scrollview_type("key", 1)
```

---

## set_trigger_actor_variable_ui_scrollview_type

method in GameAPI

- 描述

    设置全局触发器UI_SCROLLVIEW_TYPE非数组 组变量

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

GameAPI.set_trigger_actor_variable_ui_scrollview_type(actor, "key", 1)
```

---

## set_trigger_list_variable_ui_anim

method in GameAPI

- 描述

    设置全局触发器UI_ANIM数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.UIAnimKey | 值 |

- 返回值

    无

- 示例

```lua
local ui_anim_key = GameAPI.get_unit_key_ui_anim_kv(1, "key")

GameAPI.set_trigger_list_variable_ui_anim("key", 1)
```

---

## set_trigger_list_actor_variable_ui_anim

method in GameAPI

- 描述

    设置全局触发器UI_ANIM数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.UIAnimKey | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local ui_anim_key = GameAPI.get_unit_key_ui_anim_kv(1, "key")

GameAPI.set_trigger_list_actor_variable_ui_anim(actor, "key", 1)
```

---

## set_trigger_variable_ui_anim

method in GameAPI

- 描述

    设置全局触发器UI_ANIM非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.UIAnimKey | 值 |

- 返回值

    无

- 示例

```lua
local ui_anim_key = GameAPI.get_unit_key_ui_anim_kv(1, "key")

GameAPI.set_trigger_variable_ui_anim("key")
```

---

## set_trigger_actor_variable_ui_anim

method in GameAPI

- 描述

    设置全局触发器UI_ANIM非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.UIAnimKey | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local ui_anim_key = GameAPI.get_unit_key_ui_anim_kv(1, "key")

GameAPI.set_trigger_actor_variable_ui_anim(actor, "key")
```

---

## set_trigger_list_variable_ui_anim_curve

method in GameAPI

- 描述

    设置全局触发器UI_ANIM_CURVE数组变量子项

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
GameAPI.set_trigger_list_variable_ui_anim_curve("key", 1, 1)
```

---

## set_trigger_list_actor_variable_ui_anim_curve

method in GameAPI

- 描述

    设置全局触发器UI_ANIM_CURVE数组 组变量子项

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

GameAPI.set_trigger_list_actor_variable_ui_anim_curve(actor, "key", 1, 1)
```

---

## set_trigger_variable_ui_anim_curve

method in GameAPI

- 描述

    设置全局触发器UI_ANIM_CURVE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | integer | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_ui_anim_curve("key", 1)
```

---

## set_trigger_actor_variable_ui_anim_curve

method in GameAPI

- 描述

    设置全局触发器UI_ANIM_CURVE非数组 组变量

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

GameAPI.set_trigger_actor_variable_ui_anim_curve(actor, "key", 1)
```

---

## set_trigger_list_variable_audio_channel

method in GameAPI

- 描述

    设置全局触发器AUDIO_CHANNEL数组变量子项

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
GameAPI.set_trigger_list_variable_audio_channel("key", 1, 1)
```

---

## set_trigger_list_actor_variable_audio_channel

method in GameAPI

- 描述

    设置全局触发器AUDIO_CHANNEL数组 组变量子项

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

GameAPI.set_trigger_list_actor_variable_audio_channel(actor, "key", 1, 1)
```

---

## set_trigger_variable_audio_channel

method in GameAPI

- 描述

    设置全局触发器AUDIO_CHANNEL非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | integer | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_audio_channel("key", 1)
```

---

## set_trigger_actor_variable_audio_channel

method in GameAPI

- 描述

    设置全局触发器AUDIO_CHANNEL非数组 组变量

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

GameAPI.set_trigger_actor_variable_audio_channel(actor, "key", 1)
```

---

## set_trigger_list_variable_unit_entity

method in GameAPI

- 描述

    设置全局触发器UNIT_ENTITY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Unit | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.set_trigger_list_variable_unit_entity("key", 1)
```

---

## set_trigger_list_actor_variable_unit_entity

method in GameAPI

- 描述

    设置全局触发器UNIT_ENTITY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Unit | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_list_actor_variable_unit_entity(actor, "key", 1)
```

---

## set_trigger_variable_unit_entity

method in GameAPI

- 描述

    设置全局触发器UNIT_ENTITY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.Unit | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.set_trigger_variable_unit_entity("key")
```

---

## set_trigger_actor_variable_unit_entity

method in GameAPI

- 描述

    设置全局触发器UNIT_ENTITY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.Unit | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_actor_variable_unit_entity(actor, "key")
```

---

## set_trigger_list_variable_unit_group

method in GameAPI

- 描述

    设置全局触发器UNIT_GROUP数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.UnitGroup | 值 |

- 返回值

    无

- 示例

```lua
local unit_group = y3.unit_group.create()

GameAPI.set_trigger_list_variable_unit_group("key", 1)
```

---

## set_trigger_list_actor_variable_unit_group

method in GameAPI

- 描述

    设置全局触发器UNIT_GROUP数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.UnitGroup | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local unit_group = y3.unit_group.create()

GameAPI.set_trigger_list_actor_variable_unit_group(actor, "key", 1)
```

---

## set_trigger_variable_unit_group

method in GameAPI

- 描述

    设置全局触发器UNIT_GROUP非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.UnitGroup | 值 |

- 返回值

    无

- 示例

```lua
local unit_group = y3.unit_group.create()

GameAPI.set_trigger_variable_unit_group("key")
```

---

## set_trigger_actor_variable_unit_group

method in GameAPI

- 描述

    设置全局触发器UNIT_GROUP非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.UnitGroup | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local unit_group = y3.unit_group.create()

GameAPI.set_trigger_actor_variable_unit_group(actor, "key")
```

---

## set_trigger_list_variable_unit_name

method in GameAPI

- 描述

    设置全局触发器UNIT_NAME数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.UnitKey | 值 |

- 返回值

    无

- 示例

```lua
local unit_key = 134274569

GameAPI.set_trigger_list_variable_unit_name("key", 1)
```

---

## set_trigger_list_actor_variable_unit_name

method in GameAPI

- 描述

    设置全局触发器UNIT_NAME数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.UnitKey | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local unit_key = 134274569

GameAPI.set_trigger_list_actor_variable_unit_name(actor, "key", 1)
```

---

## set_trigger_variable_unit_name

method in GameAPI

- 描述

    设置全局触发器UNIT_NAME非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.UnitKey | 值 |

- 返回值

    无

- 示例

```lua
local unit_key = 134274569

GameAPI.set_trigger_variable_unit_name("key")
```

---

## set_trigger_actor_variable_unit_name

method in GameAPI

- 描述

    设置全局触发器UNIT_NAME非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.UnitKey | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local unit_key = 134274569

GameAPI.set_trigger_actor_variable_unit_name(actor, "key")
```

---

## set_trigger_list_variable_unit_name_pool

method in GameAPI

- 描述

    设置全局触发器UNIT_NAME_POOL数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.UnitKeyPool | 值 |

- 返回值

    无

- 示例

```lua
local unit_key_pool = GlobalAPI.get_empty_unit_key_pool()

GameAPI.set_trigger_list_variable_unit_name_pool("key", 1)
```

---

## set_trigger_list_actor_variable_unit_name_pool

method in GameAPI

- 描述

    设置全局触发器UNIT_NAME_POOL数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.UnitKeyPool | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local unit_key_pool = GlobalAPI.get_empty_unit_key_pool()

GameAPI.set_trigger_list_actor_variable_unit_name_pool(actor, "key", 1)
```

---

## set_trigger_variable_unit_name_pool

method in GameAPI

- 描述

    设置全局触发器UNIT_NAME_POOL非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.UnitKeyPool | 值 |

- 返回值

    无

- 示例

```lua
local unit_key_pool = GlobalAPI.get_empty_unit_key_pool()

GameAPI.set_trigger_variable_unit_name_pool("key")
```

---

## set_trigger_actor_variable_unit_name_pool

method in GameAPI

- 描述

    设置全局触发器UNIT_NAME_POOL非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.UnitKeyPool | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local unit_key_pool = GlobalAPI.get_empty_unit_key_pool()

GameAPI.set_trigger_actor_variable_unit_name_pool(actor, "key")
```

---

## set_trigger_list_variable_unit_write_attribute

method in GameAPI

- 描述

    设置全局触发器UNIT_WRITE_ATTRIBUTE数组变量子项

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
GameAPI.set_trigger_list_variable_unit_write_attribute("key", 1, "value")
```

---

## set_trigger_list_actor_variable_unit_write_attribute

method in GameAPI

- 描述

    设置全局触发器UNIT_WRITE_ATTRIBUTE数组 组变量子项

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

GameAPI.set_trigger_list_actor_variable_unit_write_attribute(actor, "key", 1, "value")
```

---

## set_trigger_variable_unit_write_attribute

method in GameAPI

- 描述

    设置全局触发器UNIT_WRITE_ATTRIBUTE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | string | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_unit_write_attribute("key", "value")
```

---

## set_trigger_actor_variable_unit_write_attribute

method in GameAPI

- 描述

    设置全局触发器UNIT_WRITE_ATTRIBUTE非数组 组变量

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

GameAPI.set_trigger_actor_variable_unit_write_attribute(actor, "key", "value")
```

---

## set_trigger_list_variable_attr_element

method in GameAPI

- 描述

    设置全局触发器ATTR_ELEMENT数组变量子项

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
GameAPI.set_trigger_list_variable_attr_element("key", 1, "value")
```

---

## set_trigger_list_actor_variable_attr_element

method in GameAPI

- 描述

    设置全局触发器ATTR_ELEMENT数组 组变量子项

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

GameAPI.set_trigger_list_actor_variable_attr_element(actor, "key", 1, "value")
```

---

## set_trigger_variable_attr_element

method in GameAPI

- 描述

    设置全局触发器ATTR_ELEMENT非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | string | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_attr_element("key", "value")
```

---

## set_trigger_actor_variable_attr_element

method in GameAPI

- 描述

    设置全局触发器ATTR_ELEMENT非数组 组变量

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

GameAPI.set_trigger_actor_variable_attr_element(actor, "key", "value")
```

---

## set_trigger_list_variable_attr_element_read

method in GameAPI

- 描述

    设置全局触发器ATTR_ELEMENT_READ数组变量子项

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
GameAPI.set_trigger_list_variable_attr_element_read("key", 1, "value")
```

---

## set_trigger_list_actor_variable_attr_element_read

method in GameAPI

- 描述

    设置全局触发器ATTR_ELEMENT_READ数组 组变量子项

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

GameAPI.set_trigger_list_actor_variable_attr_element_read(actor, "key", 1, "value")
```

---

## set_trigger_variable_attr_element_read

method in GameAPI

- 描述

    设置全局触发器ATTR_ELEMENT_READ非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | string | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_attr_element_read("key", "value")
```

---

## set_trigger_actor_variable_attr_element_read

method in GameAPI

- 描述

    设置全局触发器ATTR_ELEMENT_READ非数组 组变量

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

GameAPI.set_trigger_actor_variable_attr_element_read(actor, "key", "value")
```

---

## set_trigger_list_variable_mover_entity

method in GameAPI

- 描述

    设置全局触发器MOVER_ENTITY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Mover | 值 |

- 返回值

    无

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })
local mover = GameAPI.get_projectile_mover(projectile.handle)

GameAPI.set_trigger_list_variable_mover_entity("key", 1)
```

---

## set_trigger_list_actor_variable_mover_entity

method in GameAPI

- 描述

    设置全局触发器MOVER_ENTITY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Mover | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })
local mover = GameAPI.get_projectile_mover(projectile.handle)

GameAPI.set_trigger_list_actor_variable_mover_entity(actor, "key", 1)
```

---

## set_trigger_variable_mover_entity

method in GameAPI

- 描述

    设置全局触发器MOVER_ENTITY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.Mover | 值 |

- 返回值

    无

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })
local mover = GameAPI.get_projectile_mover(projectile.handle)

GameAPI.set_trigger_variable_mover_entity("key")
```

---

## set_trigger_actor_variable_mover_entity

method in GameAPI

- 描述

    设置全局触发器MOVER_ENTITY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.Mover | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })
local mover = GameAPI.get_projectile_mover(projectile.handle)

GameAPI.set_trigger_actor_variable_mover_entity(actor, "key")
```

---

## set_trigger_list_variable_image_quality

method in GameAPI

- 描述

    设置全局触发器IMAGE_QUALITY数组变量子项

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
GameAPI.set_trigger_list_variable_image_quality("key", 1, "value")
```

---

## set_trigger_list_actor_variable_image_quality

method in GameAPI

- 描述

    设置全局触发器IMAGE_QUALITY数组 组变量子项

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

GameAPI.set_trigger_list_actor_variable_image_quality(actor, "key", 1, "value")
```

---

## set_trigger_variable_image_quality

method in GameAPI

- 描述

    设置全局触发器IMAGE_QUALITY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | string | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_image_quality("key", "value")
```

---

## set_trigger_actor_variable_image_quality

method in GameAPI

- 描述

    设置全局触发器IMAGE_QUALITY非数组 组变量

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

GameAPI.set_trigger_actor_variable_image_quality(actor, "key", "value")
```

---

## set_trigger_list_variable_window_type_setting

method in GameAPI

- 描述

    设置全局触发器WINDOW_TYPE_SETTING数组变量子项

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
GameAPI.set_trigger_list_variable_window_type_setting("key", 1, "value")
```

---

## set_trigger_list_actor_variable_window_type_setting

method in GameAPI

- 描述

    设置全局触发器WINDOW_TYPE_SETTING数组 组变量子项

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

GameAPI.set_trigger_list_actor_variable_window_type_setting(actor, "key", 1, "value")
```

---

## set_trigger_variable_window_type_setting

method in GameAPI

- 描述

    设置全局触发器WINDOW_TYPE_SETTING非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | string | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_window_type_setting("key", "value")
```

---

## set_trigger_actor_variable_window_type_setting

method in GameAPI

- 描述

    设置全局触发器WINDOW_TYPE_SETTING非数组 组变量

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

GameAPI.set_trigger_actor_variable_window_type_setting(actor, "key", "value")
```

---

## set_trigger_list_variable_damage_attack_type

method in GameAPI

- 描述

    设置全局触发器DAMAGE_ATTACK_TYPE数组变量子项

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
GameAPI.set_trigger_list_variable_damage_attack_type("key", 1, 1)
```

---

## set_trigger_list_actor_variable_damage_attack_type

method in GameAPI

- 描述

    设置全局触发器DAMAGE_ATTACK_TYPE数组 组变量子项

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

GameAPI.set_trigger_list_actor_variable_damage_attack_type(actor, "key", 1, 1)
```

---

## set_trigger_variable_damage_attack_type

method in GameAPI

- 描述

    设置全局触发器DAMAGE_ATTACK_TYPE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | integer | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_damage_attack_type("key", 1)
```

---

## set_trigger_actor_variable_damage_attack_type

method in GameAPI

- 描述

    设置全局触发器DAMAGE_ATTACK_TYPE非数组 组变量

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

GameAPI.set_trigger_actor_variable_damage_attack_type(actor, "key", 1)
```

---

## set_trigger_list_variable_damage_armor_type

method in GameAPI

- 描述

    设置全局触发器DAMAGE_ARMOR_TYPE数组变量子项

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
GameAPI.set_trigger_list_variable_damage_armor_type("key", 1, 1)
```

---

## set_trigger_list_actor_variable_damage_armor_type

method in GameAPI

- 描述

    设置全局触发器DAMAGE_ARMOR_TYPE数组 组变量子项

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

GameAPI.set_trigger_list_actor_variable_damage_armor_type(actor, "key", 1, 1)
```

---

## set_trigger_variable_damage_armor_type

method in GameAPI

- 描述

    设置全局触发器DAMAGE_ARMOR_TYPE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | integer | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_damage_armor_type("key", 1)
```

---

## set_trigger_actor_variable_damage_armor_type

method in GameAPI

- 描述

    设置全局触发器DAMAGE_ARMOR_TYPE非数组 组变量

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

GameAPI.set_trigger_actor_variable_damage_armor_type(actor, "key", 1)
```

---

## set_trigger_list_variable_item_entity

method in GameAPI

- 描述

    设置全局触发器ITEM_ENTITY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Item | 值 |

- 返回值

    无

- 示例

```lua
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

GameAPI.set_trigger_list_variable_item_entity("key", 1)
```

---

## set_trigger_list_actor_variable_item_entity

method in GameAPI

- 描述

    设置全局触发器ITEM_ENTITY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Item | 值 |

- 返回值

    无

- 示例

```lua
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_list_actor_variable_item_entity(actor, "key", 1)
```

---

## set_trigger_variable_item_entity

method in GameAPI

- 描述

    设置全局触发器ITEM_ENTITY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.Item | 值 |

- 返回值

    无

- 示例

```lua
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

GameAPI.set_trigger_variable_item_entity("key")
```

---

## set_trigger_actor_variable_item_entity

method in GameAPI

- 描述

    设置全局触发器ITEM_ENTITY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.Item | 值 |

- 返回值

    无

- 示例

```lua
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_actor_variable_item_entity(actor, "key")
```

---

## set_trigger_list_variable_item_group

method in GameAPI

- 描述

    设置全局触发器ITEM_GROUP数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.ItemGroup | 值 |

- 返回值

    无

- 示例

```lua
local item_group = y3.item_group.create()

GameAPI.set_trigger_list_variable_item_group("key", 1)
```

---

## set_trigger_list_actor_variable_item_group

method in GameAPI

- 描述

    设置全局触发器ITEM_GROUP数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.ItemGroup | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local item_group = y3.item_group.create()

GameAPI.set_trigger_list_actor_variable_item_group(actor, "key", 1)
```

---

## set_trigger_variable_item_group

method in GameAPI

- 描述

    设置全局触发器ITEM_GROUP非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.ItemGroup | 值 |

- 返回值

    无

- 示例

```lua
local item_group = y3.item_group.create()

GameAPI.set_trigger_variable_item_group("key")
```

---

## set_trigger_actor_variable_item_group

method in GameAPI

- 描述

    设置全局触发器ITEM_GROUP非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.ItemGroup | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local item_group = y3.item_group.create()

GameAPI.set_trigger_actor_variable_item_group(actor, "key")
```

---

## set_trigger_list_variable_item_name

method in GameAPI

- 描述

    设置全局触发器ITEM_NAME数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.ItemKey | 值 |

- 返回值

    无

- 示例

```lua
local item_key = 134274569

GameAPI.set_trigger_list_variable_item_name("key", 1)
```

---

## set_trigger_list_actor_variable_item_name

method in GameAPI

- 描述

    设置全局触发器ITEM_NAME数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.ItemKey | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local item_key = 134274569

GameAPI.set_trigger_list_actor_variable_item_name(actor, "key", 1)
```

---

## set_trigger_variable_item_name

method in GameAPI

- 描述

    设置全局触发器ITEM_NAME非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.ItemKey | 值 |

- 返回值

    无

- 示例

```lua
local item_key = 134274569

GameAPI.set_trigger_variable_item_name("key")
```

---

## set_trigger_actor_variable_item_name

method in GameAPI

- 描述

    设置全局触发器ITEM_NAME非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.ItemKey | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local item_key = 134274569

GameAPI.set_trigger_actor_variable_item_name(actor, "key")
```

---

## set_trigger_list_variable_ability

method in GameAPI

- 描述

    设置全局触发器ABILITY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Ability | 值 |

- 返回值

    无

- 示例

```lua
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

GameAPI.set_trigger_list_variable_ability("key", 1)
```

---

## set_trigger_list_actor_variable_ability

method in GameAPI

- 描述

    设置全局触发器ABILITY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Ability | 值 |

- 返回值

    无

- 示例

```lua
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_list_actor_variable_ability(actor, "key", 1)
```

---

## set_trigger_variable_ability

method in GameAPI

- 描述

    设置全局触发器ABILITY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.Ability | 值 |

- 返回值

    无

- 示例

```lua
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

GameAPI.set_trigger_variable_ability("key")
```

---

## set_trigger_actor_variable_ability

method in GameAPI

- 描述

    设置全局触发器ABILITY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.Ability | 值 |

- 返回值

    无

- 示例

```lua
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_actor_variable_ability(actor, "key")
```

---

## set_trigger_list_variable_ability_type

method in GameAPI

- 描述

    设置全局触发器ABILITY_TYPE数组变量子项

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
GameAPI.set_trigger_list_variable_ability_type("key", 1, 1)
```

---

## set_trigger_list_actor_variable_ability_type

method in GameAPI

- 描述

    设置全局触发器ABILITY_TYPE数组 组变量子项

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

GameAPI.set_trigger_list_actor_variable_ability_type(actor, "key", 1, 1)
```

---

## set_trigger_variable_ability_type

method in GameAPI

- 描述

    设置全局触发器ABILITY_TYPE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | integer | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_ability_type("key", 1)
```

---

## set_trigger_actor_variable_ability_type

method in GameAPI

- 描述

    设置全局触发器ABILITY_TYPE非数组 组变量

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

GameAPI.set_trigger_actor_variable_ability_type(actor, "key", 1)
```

---

## set_trigger_list_variable_ability_cast_type

method in GameAPI

- 描述

    设置全局触发器ABILITY_CAST_TYPE数组变量子项

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
GameAPI.set_trigger_list_variable_ability_cast_type("key", 1, 1)
```

---

## set_trigger_list_actor_variable_ability_cast_type

method in GameAPI

- 描述

    设置全局触发器ABILITY_CAST_TYPE数组 组变量子项

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

GameAPI.set_trigger_list_actor_variable_ability_cast_type(actor, "key", 1, 1)
```

---

## set_trigger_variable_ability_cast_type

method in GameAPI

- 描述

    设置全局触发器ABILITY_CAST_TYPE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | integer | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_ability_cast_type("key", 1)
```

---

## set_trigger_actor_variable_ability_cast_type

method in GameAPI

- 描述

    设置全局触发器ABILITY_CAST_TYPE非数组 组变量

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

GameAPI.set_trigger_actor_variable_ability_cast_type(actor, "key", 1)
```

---

## set_trigger_list_variable_ability_name

method in GameAPI

- 描述

    设置全局触发器ABILITY_NAME数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.AbilityKey | 值 |

- 返回值

    无

- 示例

```lua
local ability_key = 134274569

GameAPI.set_trigger_list_variable_ability_name("key", 1)
```

---

## set_trigger_list_actor_variable_ability_name

method in GameAPI

- 描述

    设置全局触发器ABILITY_NAME数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.AbilityKey | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local ability_key = 134274569

GameAPI.set_trigger_list_actor_variable_ability_name(actor, "key", 1)
```

---

## set_trigger_variable_ability_name

method in GameAPI

- 描述

    设置全局触发器ABILITY_NAME非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.AbilityKey | 值 |

- 返回值

    无

- 示例

```lua
local ability_key = 134274569

GameAPI.set_trigger_variable_ability_name("key")
```

---

## set_trigger_actor_variable_ability_name

method in GameAPI

- 描述

    设置全局触发器ABILITY_NAME非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.AbilityKey | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local ability_key = 134274569

GameAPI.set_trigger_actor_variable_ability_name(actor, "key")
```

---

## set_trigger_list_variable_modifier_entity

method in GameAPI

- 描述

    设置全局触发器MODIFIER_ENTITY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.ModifierEntity | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

GameAPI.set_trigger_list_variable_modifier_entity("key", 1)
```

---

## set_trigger_list_actor_variable_modifier_entity

method in GameAPI

- 描述

    设置全局触发器MODIFIER_ENTITY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.ModifierEntity | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)
local actor = unit.handle

GameAPI.set_trigger_list_actor_variable_modifier_entity(actor, "key", 1)
```

---

## set_trigger_variable_modifier_entity

method in GameAPI

- 描述

    设置全局触发器MODIFIER_ENTITY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.ModifierEntity | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

GameAPI.set_trigger_variable_modifier_entity("key")
```

---

## set_trigger_actor_variable_modifier_entity

method in GameAPI

- 描述

    设置全局触发器MODIFIER_ENTITY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.ModifierEntity | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)
local actor = unit.handle

GameAPI.set_trigger_actor_variable_modifier_entity(actor, "key")
```

---

## set_trigger_list_variable_modifier

method in GameAPI

- 描述

    设置全局触发器MODIFIER数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.ModifierKey | 值 |

- 返回值

    无

- 示例

```lua
local modifier_key = 134274569

GameAPI.set_trigger_list_variable_modifier("key", 1)
```

---

## set_trigger_list_actor_variable_modifier

method in GameAPI

- 描述

    设置全局触发器MODIFIER数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.ModifierKey | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local modifier_key = 134274569

GameAPI.set_trigger_list_actor_variable_modifier(actor, "key", 1)
```

---

## set_trigger_variable_modifier

method in GameAPI

- 描述

    设置全局触发器MODIFIER非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.ModifierKey | 值 |

- 返回值

    无

- 示例

```lua
local modifier_key = 134274569

GameAPI.set_trigger_variable_modifier("key")
```

---

## set_trigger_actor_variable_modifier

method in GameAPI

- 描述

    设置全局触发器MODIFIER非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.ModifierKey | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local modifier_key = 134274569

GameAPI.set_trigger_actor_variable_modifier(actor, "key")
```

---

## set_trigger_list_variable_projectile

method in GameAPI

- 描述

    设置全局触发器PROJECTILE数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.ProjectileKey | 值 |

- 返回值

    无

- 示例

```lua
local projectile_key = 134274569

GameAPI.set_trigger_list_variable_projectile("key", 1)
```

---

## set_trigger_list_actor_variable_projectile

method in GameAPI

- 描述

    设置全局触发器PROJECTILE数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.ProjectileKey | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local projectile_key = 134274569

GameAPI.set_trigger_list_actor_variable_projectile(actor, "key", 1)
```

---

## set_trigger_variable_projectile

method in GameAPI

- 描述

    设置全局触发器PROJECTILE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.ProjectileKey | 值 |

- 返回值

    无

- 示例

```lua
local projectile_key = 134274569

GameAPI.set_trigger_variable_projectile("key")
```

---

## set_trigger_actor_variable_projectile

method in GameAPI

- 描述

    设置全局触发器PROJECTILE非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.ProjectileKey | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local projectile_key = 134274569

GameAPI.set_trigger_actor_variable_projectile(actor, "key")
```

---

## set_trigger_list_variable_projectile_entity

method in GameAPI

- 描述

    设置全局触发器PROJECTILE_ENTITY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.ProjectileEntity | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local target_point = unit:get_point()
local projectile = y3.projectile.create({ key = 134274569, target = target_point })

GameAPI.set_trigger_list_variable_projectile_entity("key", 1)
```

---

## set_trigger_list_actor_variable_projectile_entity

method in GameAPI

- 描述

    设置全局触发器PROJECTILE_ENTITY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.ProjectileEntity | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local target_point = unit:get_point()
local projectile = y3.projectile.create({ key = 134274569, target = target_point })

GameAPI.set_trigger_list_actor_variable_projectile_entity(actor, "key", 1)
```

---

## set_trigger_variable_projectile_entity

method in GameAPI

- 描述

    设置全局触发器PROJECTILE_ENTITY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.ProjectileEntity | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local target_point = unit:get_point()
local projectile = y3.projectile.create({ key = 134274569, target = target_point })

GameAPI.set_trigger_variable_projectile_entity("key")
```

---

## set_trigger_actor_variable_projectile_entity

method in GameAPI

- 描述

    设置全局触发器PROJECTILE_ENTITY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.ProjectileEntity | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local target_point = unit:get_point()
local projectile = y3.projectile.create({ key = 134274569, target = target_point })

GameAPI.set_trigger_actor_variable_projectile_entity(actor, "key")
```

---

## set_trigger_list_variable_projectile_group

method in GameAPI

- 描述

    设置全局触发器PROJECTILE_GROUP数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.ProjectileGroup | 值 |

- 返回值

    无

- 示例

```lua
local projectile_group = y3.projectile_group.create_lua_projectile_group_from_py(GameAPI.create_projectile_group())

GameAPI.set_trigger_list_variable_projectile_group("key", 1)
```

---

## set_trigger_list_actor_variable_projectile_group

method in GameAPI

- 描述

    设置全局触发器PROJECTILE_GROUP数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.ProjectileGroup | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local projectile_group = y3.projectile_group.create_lua_projectile_group_from_py(GameAPI.create_projectile_group())

GameAPI.set_trigger_list_actor_variable_projectile_group(actor, "key", 1)
```

---

## set_trigger_variable_projectile_group

method in GameAPI

- 描述

    设置全局触发器PROJECTILE_GROUP非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.ProjectileGroup | 值 |

- 返回值

    无

- 示例

```lua
local projectile_group = y3.projectile_group.create_lua_projectile_group_from_py(GameAPI.create_projectile_group())

GameAPI.set_trigger_variable_projectile_group("key")
```

---

## set_trigger_actor_variable_projectile_group

method in GameAPI

- 描述

    设置全局触发器PROJECTILE_GROUP非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.ProjectileGroup | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local projectile_group = y3.projectile_group.create_lua_projectile_group_from_py(GameAPI.create_projectile_group())

GameAPI.set_trigger_actor_variable_projectile_group(actor, "key")
```

---

## set_trigger_list_variable_destructible_entity

method in GameAPI

- 描述

    设置全局触发器DESTRUCTIBLE_ENTITY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Destructible | 值 |

- 返回值

    无

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

GameAPI.set_trigger_list_variable_destructible_entity("key", 1)
end
```

---

## set_trigger_list_actor_variable_destructible_entity

method in GameAPI

- 描述

    设置全局触发器DESTRUCTIBLE_ENTITY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Destructible | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local destructible = y3.destructible.get_by_id(1)
if destructible then

GameAPI.set_trigger_list_actor_variable_destructible_entity(actor, "key", 1)
end
```

---

## set_trigger_variable_destructible_entity

method in GameAPI

- 描述

    设置全局触发器DESTRUCTIBLE_ENTITY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.Destructible | 值 |

- 返回值

    无

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

GameAPI.set_trigger_variable_destructible_entity("key")
end
```

---

## set_trigger_actor_variable_destructible_entity

method in GameAPI

- 描述

    设置全局触发器DESTRUCTIBLE_ENTITY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.Destructible | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local destructible = y3.destructible.get_by_id(1)
if destructible then

GameAPI.set_trigger_actor_variable_destructible_entity(actor, "key")
end
```

---

## set_trigger_list_variable_destructible_name

method in GameAPI

- 描述

    设置全局触发器DESTRUCTIBLE_NAME数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.DestructibleKey | 值 |

- 返回值

    无

- 示例

```lua
local destructible_key = 1

GameAPI.set_trigger_list_variable_destructible_name("key", 1)
```

---

## set_trigger_list_actor_variable_destructible_name

method in GameAPI

- 描述

    设置全局触发器DESTRUCTIBLE_NAME数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.DestructibleKey | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local destructible_key = 1

GameAPI.set_trigger_list_actor_variable_destructible_name(actor, "key", 1)
```

---

## set_trigger_variable_destructible_name

method in GameAPI

- 描述

    设置全局触发器DESTRUCTIBLE_NAME非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.DestructibleKey | 值 |

- 返回值

    无

- 示例

```lua
local destructible_key = 1

GameAPI.set_trigger_variable_destructible_name("key")
```

---

## set_trigger_actor_variable_destructible_name

method in GameAPI

- 描述

    设置全局触发器DESTRUCTIBLE_NAME非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.DestructibleKey | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local destructible_key = 1

GameAPI.set_trigger_actor_variable_destructible_name(actor, "key")
```

---

## set_trigger_list_variable_sound_entity

method in GameAPI

- 描述

    设置全局触发器SOUND_ENTITY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.SoundEntity | 值 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local sound_entity = GameAPI.play_sound_for_player(player.handle, 134274569, false)

GameAPI.set_trigger_list_variable_sound_entity("key", 1)
```

---

## set_trigger_list_actor_variable_sound_entity

method in GameAPI

- 描述

    设置全局触发器SOUND_ENTITY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.SoundEntity | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local player = y3.player.get_by_id(1)
local sound_entity = GameAPI.play_sound_for_player(player.handle, 134274569, false)

GameAPI.set_trigger_list_actor_variable_sound_entity(actor, "key", 1)
```

---

## set_trigger_variable_sound_entity

method in GameAPI

- 描述

    设置全局触发器SOUND_ENTITY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.SoundEntity | 值 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local sound_entity = GameAPI.play_sound_for_player(player.handle, 134274569, false)

GameAPI.set_trigger_variable_sound_entity("key")
```

---

## set_trigger_actor_variable_sound_entity

method in GameAPI

- 描述

    设置全局触发器SOUND_ENTITY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.SoundEntity | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local player = y3.player.get_by_id(1)
local sound_entity = GameAPI.play_sound_for_player(player.handle, 134274569, false)

GameAPI.set_trigger_actor_variable_sound_entity(actor, "key")
```

---

## set_trigger_list_variable_audio_key

method in GameAPI

- 描述

    设置全局触发器AUDIO_KEY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.AudioKey | 值 |

- 返回值

    无

- 示例

```lua
local audio_key = 134274569

GameAPI.set_trigger_list_variable_audio_key("key", 1)
```

---

## set_trigger_list_actor_variable_audio_key

method in GameAPI

- 描述

    设置全局触发器AUDIO_KEY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.AudioKey | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local audio_key = 134274569

GameAPI.set_trigger_list_actor_variable_audio_key(actor, "key", 1)
```

---

## set_trigger_variable_audio_key

method in GameAPI

- 描述

    设置全局触发器AUDIO_KEY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.AudioKey | 值 |

- 返回值

    无

- 示例

```lua
local audio_key = 134274569

GameAPI.set_trigger_variable_audio_key("key")
```

---

## set_trigger_actor_variable_audio_key

method in GameAPI

- 描述

    设置全局触发器AUDIO_KEY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.AudioKey | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local audio_key = 134274569

GameAPI.set_trigger_actor_variable_audio_key(actor, "key")
```

---

## set_trigger_list_variable_game_mode

method in GameAPI

- 描述

    设置全局触发器GAME_MODE数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.GameMode | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_list_variable_game_mode("key", 1, 1)
```

---

## set_trigger_list_actor_variable_game_mode

method in GameAPI

- 描述

    设置全局触发器GAME_MODE数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.GameMode | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_list_actor_variable_game_mode(actor, "key", 1, 1)
```

---

## set_trigger_variable_game_mode

method in GameAPI

- 描述

    设置全局触发器GAME_MODE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.GameMode | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_game_mode("key", 1)
```

---

## set_trigger_actor_variable_game_mode

method in GameAPI

- 描述

    设置全局触发器GAME_MODE非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.GameMode | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_actor_variable_game_mode(actor, "key", 1)
```

---

## set_trigger_list_variable_player

method in GameAPI

- 描述

    设置全局触发器PLAYER数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Role | 值 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_trigger_list_variable_player("key", 1)
```

---

## set_trigger_list_actor_variable_player

method in GameAPI

- 描述

    设置全局触发器PLAYER数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Role | 值 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_list_actor_variable_player(actor, "key", 1)
```

---

## set_trigger_variable_player

method in GameAPI

- 描述

    设置全局触发器PLAYER非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.Role | 值 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_trigger_variable_player("key")
```

---

## set_trigger_actor_variable_player

method in GameAPI

- 描述

    设置全局触发器PLAYER非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.Role | 值 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_actor_variable_player(actor, "key")
```

---

## set_trigger_list_variable_player_group

method in GameAPI

- 描述

    设置全局触发器PLAYER_GROUP数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.RoleGroup | 值 |

- 返回值

    无

- 示例

```lua
local player_group = y3.player_group.create()

GameAPI.set_trigger_list_variable_player_group("key", 1)
```

---

## set_trigger_list_actor_variable_player_group

method in GameAPI

- 描述

    设置全局触发器PLAYER_GROUP数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.RoleGroup | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local player_group = y3.player_group.create()

GameAPI.set_trigger_list_actor_variable_player_group(actor, "key", 1)
```

---

## set_trigger_variable_player_group

method in GameAPI

- 描述

    设置全局触发器PLAYER_GROUP非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.RoleGroup | 值 |

- 返回值

    无

- 示例

```lua
local player_group = y3.player_group.create()

GameAPI.set_trigger_variable_player_group("key")
```

---

## set_trigger_actor_variable_player_group

method in GameAPI

- 描述

    设置全局触发器PLAYER_GROUP非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.RoleGroup | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local player_group = y3.player_group.create()

GameAPI.set_trigger_actor_variable_player_group(actor, "key")
```

---

## set_trigger_list_variable_role_res_key

method in GameAPI

- 描述

    设置全局触发器ROLE_RES_KEY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.RoleResKey | 值 |

- 返回值

    无

- 示例

```lua
local role_res_key = "res_key"

GameAPI.set_trigger_list_variable_role_res_key("key", 1)
```

---

## set_trigger_list_actor_variable_role_res_key

method in GameAPI

- 描述

    设置全局触发器ROLE_RES_KEY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.RoleResKey | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local role_res_key = "res_key"

GameAPI.set_trigger_list_actor_variable_role_res_key(actor, "key", 1)
```

---

## set_trigger_variable_role_res_key

method in GameAPI

- 描述

    设置全局触发器ROLE_RES_KEY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.RoleResKey | 值 |

- 返回值

    无

- 示例

```lua
local role_res_key = "res_key"

GameAPI.set_trigger_variable_role_res_key("key")
```

---

## set_trigger_actor_variable_role_res_key

method in GameAPI

- 描述

    设置全局触发器ROLE_RES_KEY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.RoleResKey | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local role_res_key = "res_key"

GameAPI.set_trigger_actor_variable_role_res_key(actor, "key")
```

---

## set_trigger_list_variable_role_status

method in GameAPI

- 描述

    设置全局触发器ROLE_STATUS数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.RoleStatus | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_list_variable_role_status("key", 1, 1)
```

---

## set_trigger_list_actor_variable_role_status

method in GameAPI

- 描述

    设置全局触发器ROLE_STATUS数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.RoleStatus | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_list_actor_variable_role_status(actor, "key", 1, 1)
```

---

## set_trigger_variable_role_status

method in GameAPI

- 描述

    设置全局触发器ROLE_STATUS非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.RoleStatus | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_role_status("key", 1)
```

---

## set_trigger_actor_variable_role_status

method in GameAPI

- 描述

    设置全局触发器ROLE_STATUS非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.RoleStatus | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_actor_variable_role_status(actor, "key", 1)
```

---

## set_trigger_list_variable_role_type

method in GameAPI

- 描述

    设置全局触发器ROLE_TYPE数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.RoleType | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_list_variable_role_type("key", 1, 1)
```

---

## set_trigger_list_actor_variable_role_type

method in GameAPI

- 描述

    设置全局触发器ROLE_TYPE数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.RoleType | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_list_actor_variable_role_type(actor, "key", 1, 1)
```

---

## set_trigger_variable_role_type

method in GameAPI

- 描述

    设置全局触发器ROLE_TYPE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.RoleType | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_role_type("key", 1)
```

---

## set_trigger_actor_variable_role_type

method in GameAPI

- 描述

    设置全局触发器ROLE_TYPE非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.RoleType | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_actor_variable_role_type(actor, "key", 1)
```

---

## set_trigger_list_variable_team

method in GameAPI

- 描述

    设置全局触发器TEAM数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Camp | 值 |

- 返回值

    无

- 示例

```lua
local camp = GameAPI.get_camp_by_camp_id(1)

GameAPI.set_trigger_list_variable_team("key", 1)
```

---

## set_trigger_list_actor_variable_team

method in GameAPI

- 描述

    设置全局触发器TEAM数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Camp | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local camp = GameAPI.get_camp_by_camp_id(1)

GameAPI.set_trigger_list_actor_variable_team(actor, "key", 1)
```

---

## set_trigger_variable_team

method in GameAPI

- 描述

    设置全局触发器TEAM非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.Camp | 值 |

- 返回值

    无

- 示例

```lua
local camp = GameAPI.get_camp_by_camp_id(1)

GameAPI.set_trigger_variable_team("key")
```

---

## set_trigger_actor_variable_team

method in GameAPI

- 描述

    设置全局触发器TEAM非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.Camp | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local camp = GameAPI.get_camp_by_camp_id(1)

GameAPI.set_trigger_actor_variable_team(actor, "key")
```

---

## set_trigger_list_variable_point

method in GameAPI

- 描述

    设置全局触发器POINT数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.FPoint | 值 |

- 返回值

    无

- 示例

```lua
local fpoint = GameAPI.get_point_by_res_id(1)

GameAPI.set_trigger_list_variable_point("key", 1)
```

---

## set_trigger_list_actor_variable_point

method in GameAPI

- 描述

    设置全局触发器POINT数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.FPoint | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local fpoint = GameAPI.get_point_by_res_id(1)

GameAPI.set_trigger_list_actor_variable_point(actor, "key", 1)
```

---

## set_trigger_variable_point

method in GameAPI

- 描述

    设置全局触发器POINT非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.FPoint | 值 |

- 返回值

    无

- 示例

```lua
local fpoint = GameAPI.get_point_by_res_id(1)

GameAPI.set_trigger_variable_point("key")
```

---

## set_trigger_actor_variable_point

method in GameAPI

- 描述

    设置全局触发器POINT非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.FPoint | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local fpoint = GameAPI.get_point_by_res_id(1)

GameAPI.set_trigger_actor_variable_point(actor, "key")
```

---

## set_trigger_list_variable_vector3

method in GameAPI

- 描述

    设置全局触发器VECTOR3数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.FVector3 | 值 |

- 返回值

    无

- 示例

```lua
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

GameAPI.set_trigger_list_variable_vector3("key", 1)
```

---

## set_trigger_list_actor_variable_vector3

method in GameAPI

- 描述

    设置全局触发器VECTOR3数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.FVector3 | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

GameAPI.set_trigger_list_actor_variable_vector3(actor, "key", 1)
```

---

## set_trigger_variable_vector3

method in GameAPI

- 描述

    设置全局触发器VECTOR3非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.FVector3 | 值 |

- 返回值

    无

- 示例

```lua
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

GameAPI.set_trigger_variable_vector3("key")
```

---

## set_trigger_actor_variable_vector3

method in GameAPI

- 描述

    设置全局触发器VECTOR3非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.FVector3 | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

GameAPI.set_trigger_actor_variable_vector3(actor, "key")
```

---

## set_trigger_list_variable_rotation

method in GameAPI

- 描述

    设置全局触发器ROTATION数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.FRotation | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_list_variable_rotation("key", 1)
```

---

## set_trigger_list_actor_variable_rotation

method in GameAPI

- 描述

    设置全局触发器ROTATION数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.FRotation | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_list_actor_variable_rotation(actor, "key", 1)
```

---

## set_trigger_variable_rotation

method in GameAPI

- 描述

    设置全局触发器ROTATION非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.FRotation | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_rotation("key")
```

---

## set_trigger_actor_variable_rotation

method in GameAPI

- 描述

    设置全局触发器ROTATION非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.FRotation | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_actor_variable_rotation(actor, "key")
```

---

## set_trigger_list_variable_point_list

method in GameAPI

- 描述

    设置全局触发器POINT_LIST数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Road | 值 |

- 返回值

    无

- 示例

```lua
local road = y3.road.get_road_by_res_id(1)

GameAPI.set_trigger_list_variable_point_list("key", 1)
```

---

## set_trigger_list_actor_variable_point_list

method in GameAPI

- 描述

    设置全局触发器POINT_LIST数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Road | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local road = y3.road.get_road_by_res_id(1)

GameAPI.set_trigger_list_actor_variable_point_list(actor, "key", 1)
```

---

## set_trigger_variable_point_list

method in GameAPI

- 描述

    设置全局触发器POINT_LIST非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.Road | 值 |

- 返回值

    无

- 示例

```lua
local road = y3.road.get_road_by_res_id(1)

GameAPI.set_trigger_variable_point_list("key")
```

---

## set_trigger_actor_variable_point_list

method in GameAPI

- 描述

    设置全局触发器POINT_LIST非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.Road | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local road = y3.road.get_road_by_res_id(1)

GameAPI.set_trigger_actor_variable_point_list(actor, "key")
```

---

## set_trigger_list_variable_road_group

method in GameAPI

- 描述

    设置全局触发器ROAD_GROUP数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.RoadGroup | 值 |

- 返回值

    无

- 示例

```lua
local road_group = GameAPI.get_trigger_variable_road_group("key")

GameAPI.set_trigger_list_variable_road_group("key", 1)
```

---

## set_trigger_list_actor_variable_road_group

method in GameAPI

- 描述

    设置全局触发器ROAD_GROUP数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.RoadGroup | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local road_group = GameAPI.get_trigger_variable_road_group("key")

GameAPI.set_trigger_list_actor_variable_road_group(actor, "key", 1)
```

---

## set_trigger_variable_road_group

method in GameAPI

- 描述

    设置全局触发器ROAD_GROUP非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.RoadGroup | 值 |

- 返回值

    无

- 示例

```lua
local road_group = GameAPI.get_trigger_variable_road_group("key")

GameAPI.set_trigger_variable_road_group("key")
```

---

## set_trigger_actor_variable_road_group

method in GameAPI

- 描述

    设置全局触发器ROAD_GROUP非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.RoadGroup | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local road_group = GameAPI.get_trigger_variable_road_group("key")

GameAPI.set_trigger_actor_variable_road_group(actor, "key")
```

---

## set_trigger_list_variable_rectangle

method in GameAPI

- 描述

    设置全局触发器RECTANGLE数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.RecArea | 值 |

- 返回值

    无

- 示例

```lua
local rec_area = GameAPI.create_rec_area_from_two_points(Fix32Vec3(0, 0, 0), Fix32Vec3(100, 100, 0))

GameAPI.set_trigger_list_variable_rectangle("key", 1)
```

---

## set_trigger_list_actor_variable_rectangle

method in GameAPI

- 描述

    设置全局触发器RECTANGLE数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.RecArea | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local rec_area = GameAPI.create_rec_area_from_two_points(Fix32Vec3(0, 0, 0), Fix32Vec3(100, 100, 0))

GameAPI.set_trigger_list_actor_variable_rectangle(actor, "key", 1)
```

---

## set_trigger_variable_rectangle

method in GameAPI

- 描述

    设置全局触发器RECTANGLE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.RecArea | 值 |

- 返回值

    无

- 示例

```lua
local rec_area = GameAPI.create_rec_area_from_two_points(Fix32Vec3(0, 0, 0), Fix32Vec3(100, 100, 0))

GameAPI.set_trigger_variable_rectangle("key")
```

---

## set_trigger_actor_variable_rectangle

method in GameAPI

- 描述

    设置全局触发器RECTANGLE非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.RecArea | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local rec_area = GameAPI.create_rec_area_from_two_points(Fix32Vec3(0, 0, 0), Fix32Vec3(100, 100, 0))

GameAPI.set_trigger_actor_variable_rectangle(actor, "key")
```

---

## set_trigger_list_variable_round_area

method in GameAPI

- 描述

    设置全局触发器ROUND_AREA数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.CirArea | 值 |

- 返回值

    无

- 示例

```lua
local cir_area = GameAPI.create_new_cir_area(GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0)), Fix32(100))

GameAPI.set_trigger_list_variable_round_area("key", 1)
```

---

## set_trigger_list_actor_variable_round_area

method in GameAPI

- 描述

    设置全局触发器ROUND_AREA数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.CirArea | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local cir_area = GameAPI.create_new_cir_area(GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0)), Fix32(100))

GameAPI.set_trigger_list_actor_variable_round_area(actor, "key", 1)
```

---

## set_trigger_variable_round_area

method in GameAPI

- 描述

    设置全局触发器ROUND_AREA非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.CirArea | 值 |

- 返回值

    无

- 示例

```lua
local cir_area = GameAPI.create_new_cir_area(GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0)), Fix32(100))

GameAPI.set_trigger_variable_round_area("key")
```

---

## set_trigger_actor_variable_round_area

method in GameAPI

- 描述

    设置全局触发器ROUND_AREA非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.CirArea | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local cir_area = GameAPI.create_new_cir_area(GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0)), Fix32(100))

GameAPI.set_trigger_actor_variable_round_area(actor, "key")
```

---

## set_trigger_list_variable_polygon

method in GameAPI

- 描述

    设置全局触发器POLYGON数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.PolyArea | 值 |

- 返回值

    无

- 示例

```lua
local poly_area = GameAPI.create_polygon_area(Fix32Vec3(0, 0, 0), Fix32Vec3(100, 0, 0), Fix32Vec3(100, 100, 0))

GameAPI.set_trigger_list_variable_polygon("key", 1)
```

---

## set_trigger_list_actor_variable_polygon

method in GameAPI

- 描述

    设置全局触发器POLYGON数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.PolyArea | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local poly_area = GameAPI.create_polygon_area(Fix32Vec3(0, 0, 0), Fix32Vec3(100, 0, 0), Fix32Vec3(100, 100, 0))

GameAPI.set_trigger_list_actor_variable_polygon(actor, "key", 1)
```

---

## set_trigger_variable_polygon

method in GameAPI

- 描述

    设置全局触发器POLYGON非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.PolyArea | 值 |

- 返回值

    无

- 示例

```lua
local poly_area = GameAPI.create_polygon_area(Fix32Vec3(0, 0, 0), Fix32Vec3(100, 0, 0), Fix32Vec3(100, 100, 0))

GameAPI.set_trigger_variable_polygon("key")
```

---

## set_trigger_actor_variable_polygon

method in GameAPI

- 描述

    设置全局触发器POLYGON非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.PolyArea | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local poly_area = GameAPI.create_polygon_area(Fix32Vec3(0, 0, 0), Fix32Vec3(100, 0, 0), Fix32Vec3(100, 100, 0))

GameAPI.set_trigger_actor_variable_polygon(actor, "key")
```

---

## set_trigger_list_variable_camera

method in GameAPI

- 描述

    设置全局触发器CAMERA数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Camera | 值 |

- 返回值

    无

- 示例

```lua
local camera = y3.camera.create_camera(y3.point(0, 0), 1000, 500, 0, 45, 3000)

GameAPI.set_trigger_list_variable_camera("key", 1)
```

---

## set_trigger_list_actor_variable_camera

method in GameAPI

- 描述

    设置全局触发器CAMERA数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Camera | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local camera = y3.camera.create_camera(y3.point(0, 0), 1000, 500, 0, 45, 3000)

GameAPI.set_trigger_list_actor_variable_camera(actor, "key", 1)
```

---

## set_trigger_variable_camera

method in GameAPI

- 描述

    设置全局触发器CAMERA非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.Camera | 值 |

- 返回值

    无

- 示例

```lua
local camera = y3.camera.create_camera(y3.point(0, 0), 1000, 500, 0, 45, 3000)

GameAPI.set_trigger_variable_camera("key")
```

---

## set_trigger_actor_variable_camera

method in GameAPI

- 描述

    设置全局触发器CAMERA非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.Camera | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local camera = y3.camera.create_camera(y3.point(0, 0), 1000, 500, 0, 45, 3000)

GameAPI.set_trigger_actor_variable_camera(actor, "key")
```

---

## set_trigger_list_variable_camline

method in GameAPI

- 描述

    设置全局触发器CAMLINE数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.CamlineID | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_list_variable_camline("key", 1, 1)
```

---

## set_trigger_list_actor_variable_camline

method in GameAPI

- 描述

    设置全局触发器CAMLINE数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.CamlineID | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_list_actor_variable_camline(actor, "key", 1, 1)
```

---

## set_trigger_variable_camline

method in GameAPI

- 描述

    设置全局触发器CAMLINE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.CamlineID | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_camline("key", 1)
```

---

## set_trigger_actor_variable_camline

method in GameAPI

- 描述

    设置全局触发器CAMLINE非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.CamlineID | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_actor_variable_camline(actor, "key", 1)
```

---

## set_trigger_list_variable_point_light

method in GameAPI

- 描述

    设置全局触发器POINT_LIGHT数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.PointLight | 值 |

- 返回值

    无

- 示例

```lua
local point_light = GameAPI.get_point_light_res_by_res_id(1)

GameAPI.set_trigger_list_variable_point_light("key", 1)
```

---

## set_trigger_list_actor_variable_point_light

method in GameAPI

- 描述

    设置全局触发器POINT_LIGHT数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.PointLight | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local point_light = GameAPI.get_point_light_res_by_res_id(1)

GameAPI.set_trigger_list_actor_variable_point_light(actor, "key", 1)
```

---

## set_trigger_variable_point_light

method in GameAPI

- 描述

    设置全局触发器POINT_LIGHT非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.PointLight | 值 |

- 返回值

    无

- 示例

```lua
local point_light = GameAPI.get_point_light_res_by_res_id(1)

GameAPI.set_trigger_variable_point_light("key")
```

---

## set_trigger_actor_variable_point_light

method in GameAPI

- 描述

    设置全局触发器POINT_LIGHT非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.PointLight | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local point_light = GameAPI.get_point_light_res_by_res_id(1)

GameAPI.set_trigger_actor_variable_point_light(actor, "key")
```

---

## set_trigger_list_variable_spot_light

method in GameAPI

- 描述

    设置全局触发器SPOT_LIGHT数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.SpotLight | 值 |

- 返回值

    无

- 示例

```lua
local spot_light = GameAPI.get_spot_light_res_by_res_id(1)

GameAPI.set_trigger_list_variable_spot_light("key", 1)
```

---

## set_trigger_list_actor_variable_spot_light

method in GameAPI

- 描述

    设置全局触发器SPOT_LIGHT数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.SpotLight | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local spot_light = GameAPI.get_spot_light_res_by_res_id(1)

GameAPI.set_trigger_list_actor_variable_spot_light(actor, "key", 1)
```

---

## set_trigger_variable_spot_light

method in GameAPI

- 描述

    设置全局触发器SPOT_LIGHT非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.SpotLight | 值 |

- 返回值

    无

- 示例

```lua
local spot_light = GameAPI.get_spot_light_res_by_res_id(1)

GameAPI.set_trigger_variable_spot_light("key")
```

---

## set_trigger_actor_variable_spot_light

method in GameAPI

- 描述

    设置全局触发器SPOT_LIGHT非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.SpotLight | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local spot_light = GameAPI.get_spot_light_res_by_res_id(1)

GameAPI.set_trigger_actor_variable_spot_light(actor, "key")
```

---

## set_trigger_list_variable_fog

method in GameAPI

- 描述

    设置全局触发器FOG数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Fog | 值 |

- 返回值

    无

- 示例

```lua
local fog = GameAPI.get_fog_res_by_res_id(1)

GameAPI.set_trigger_list_variable_fog("key", 1)
```

---

## set_trigger_list_actor_variable_fog

method in GameAPI

- 描述

    设置全局触发器FOG数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Fog | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local fog = GameAPI.get_fog_res_by_res_id(1)

GameAPI.set_trigger_list_actor_variable_fog(actor, "key", 1)
```

---

## set_trigger_variable_fog

method in GameAPI

- 描述

    设置全局触发器FOG非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.Fog | 值 |

- 返回值

    无

- 示例

```lua
local fog = GameAPI.get_fog_res_by_res_id(1)

GameAPI.set_trigger_variable_fog("key")
```

---

## set_trigger_actor_variable_fog

method in GameAPI

- 描述

    设置全局触发器FOG非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.Fog | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local fog = GameAPI.get_fog_res_by_res_id(1)

GameAPI.set_trigger_actor_variable_fog(actor, "key")
```

---

## set_trigger_list_variable_model

method in GameAPI

- 描述

    设置全局触发器MODEL数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.ModelKey | 值 |

- 返回值

    无

- 示例

```lua
local model_key = 1

GameAPI.set_trigger_list_variable_model("key", 1)
```

---

## set_trigger_list_actor_variable_model

method in GameAPI

- 描述

    设置全局触发器MODEL数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.ModelKey | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local model_key = 1

GameAPI.set_trigger_list_actor_variable_model(actor, "key", 1)
```

---

## set_trigger_variable_model

method in GameAPI

- 描述

    设置全局触发器MODEL非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.ModelKey | 值 |

- 返回值

    无

- 示例

```lua
local model_key = 1

GameAPI.set_trigger_variable_model("key")
```

---

## set_trigger_actor_variable_model

method in GameAPI

- 描述

    设置全局触发器MODEL非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.ModelKey | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local model_key = 1

GameAPI.set_trigger_actor_variable_model(actor, "key")
```

---

## set_trigger_list_variable_sfx_entity

method in GameAPI

- 描述

    设置全局触发器SFX_ENTITY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Sfx | 值 |

- 返回值

    无

- 示例

```lua
local sfx = y3.particle.create({ type = 134274569, target = y3.point(0, 0) }).handle

GameAPI.set_trigger_list_variable_sfx_entity("key", 1)
```

---

## set_trigger_list_actor_variable_sfx_entity

method in GameAPI

- 描述

    设置全局触发器SFX_ENTITY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Sfx | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local sfx = y3.particle.create({ type = 134274569, target = y3.point(0, 0) }).handle

GameAPI.set_trigger_list_actor_variable_sfx_entity(actor, "key", 1)
```

---

## set_trigger_variable_sfx_entity

method in GameAPI

- 描述

    设置全局触发器SFX_ENTITY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.Sfx | 值 |

- 返回值

    无

- 示例

```lua
local sfx = y3.particle.create({ type = 134274569, target = y3.point(0, 0) }).handle

GameAPI.set_trigger_variable_sfx_entity("key")
```

---

## set_trigger_actor_variable_sfx_entity

method in GameAPI

- 描述

    设置全局触发器SFX_ENTITY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.Sfx | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local sfx = y3.particle.create({ type = 134274569, target = y3.point(0, 0) }).handle

GameAPI.set_trigger_actor_variable_sfx_entity(actor, "key")
```

---

## set_trigger_list_variable_sfx_key

method in GameAPI

- 描述

    设置全局触发器SFX_KEY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.SfxKey | 值 |

- 返回值

    无

- 示例

```lua
local sfx_key = 134274569

GameAPI.set_trigger_list_variable_sfx_key("key", 1)
```

---

## set_trigger_list_actor_variable_sfx_key

method in GameAPI

- 描述

    设置全局触发器SFX_KEY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.SfxKey | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local sfx_key = 134274569

GameAPI.set_trigger_list_actor_variable_sfx_key(actor, "key", 1)
```

---

## set_trigger_variable_sfx_key

method in GameAPI

- 描述

    设置全局触发器SFX_KEY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.SfxKey | 值 |

- 返回值

    无

- 示例

```lua
local sfx_key = 134274569

GameAPI.set_trigger_variable_sfx_key("key")
```

---

## set_trigger_actor_variable_sfx_key

method in GameAPI

- 描述

    设置全局触发器SFX_KEY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.SfxKey | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local sfx_key = 134274569

GameAPI.set_trigger_actor_variable_sfx_key(actor, "key")
```

---

## set_trigger_list_variable_link_sfx_entity

method in GameAPI

- 描述

    设置全局触发器LINK_SFX_ENTITY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.LinkSfx | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local link_sfx = GameAPI.create_link_sfx_from_unit_to_point(134274569, unit.handle, "origin", GlobalAPI.coord_to_point(Fix32(100), Fix32(100), Fix32(0)), Fix32(0))

GameAPI.set_trigger_list_variable_link_sfx_entity("key", 1)
```

---

## set_trigger_list_actor_variable_link_sfx_entity

method in GameAPI

- 描述

    设置全局触发器LINK_SFX_ENTITY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.LinkSfx | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local link_sfx = GameAPI.create_link_sfx_from_unit_to_point(134274569, unit.handle, "origin", GlobalAPI.coord_to_point(Fix32(100), Fix32(100), Fix32(0)), Fix32(0))

GameAPI.set_trigger_list_actor_variable_link_sfx_entity(actor, "key", 1)
```

---

## set_trigger_variable_link_sfx_entity

method in GameAPI

- 描述

    设置全局触发器LINK_SFX_ENTITY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.LinkSfx | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local link_sfx = GameAPI.create_link_sfx_from_unit_to_point(134274569, unit.handle, "origin", GlobalAPI.coord_to_point(Fix32(100), Fix32(100), Fix32(0)), Fix32(0))

GameAPI.set_trigger_variable_link_sfx_entity("key")
```

---

## set_trigger_actor_variable_link_sfx_entity

method in GameAPI

- 描述

    设置全局触发器LINK_SFX_ENTITY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.LinkSfx | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local link_sfx = GameAPI.create_link_sfx_from_unit_to_point(134274569, unit.handle, "origin", GlobalAPI.coord_to_point(Fix32(100), Fix32(100), Fix32(0)), Fix32(0))

GameAPI.set_trigger_actor_variable_link_sfx_entity(actor, "key")
```

---

## set_trigger_list_variable_link_sfx_key

method in GameAPI

- 描述

    设置全局触发器LINK_SFX_KEY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.LinkSfxKey | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_list_variable_link_sfx_key("key", 1, 1)
```

---

## set_trigger_list_actor_variable_link_sfx_key

method in GameAPI

- 描述

    设置全局触发器LINK_SFX_KEY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.LinkSfxKey | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_list_actor_variable_link_sfx_key(actor, "key", 1, 1)
```

---

## set_trigger_variable_link_sfx_key

method in GameAPI

- 描述

    设置全局触发器LINK_SFX_KEY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.LinkSfxKey | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_link_sfx_key("key", 1)
```

---

## set_trigger_actor_variable_link_sfx_key

method in GameAPI

- 描述

    设置全局触发器LINK_SFX_KEY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.LinkSfxKey | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_actor_variable_link_sfx_key(actor, "key", 1)
```

---

## set_trigger_list_variable_cursor_key

method in GameAPI

- 描述

    设置全局触发器CURSOR_KEY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.CursorKey | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_list_variable_cursor_key("key", 1, 1)
```

---

## set_trigger_list_actor_variable_cursor_key

method in GameAPI

- 描述

    设置全局触发器CURSOR_KEY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.CursorKey | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_list_actor_variable_cursor_key(actor, "key", 1, 1)
```

---

## set_trigger_variable_cursor_key

method in GameAPI

- 描述

    设置全局触发器CURSOR_KEY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.CursorKey | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_cursor_key("key", 1)
```

---

## set_trigger_actor_variable_cursor_key

method in GameAPI

- 描述

    设置全局触发器CURSOR_KEY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.CursorKey | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_actor_variable_cursor_key(actor, "key", 1)
```

---

## set_trigger_list_variable_image_key

method in GameAPI

- 描述

    设置全局触发器IMAGE_KEY数组变量子项

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
GameAPI.set_trigger_list_variable_image_key("key", 1, 1)
```

---

## set_trigger_list_actor_variable_image_key

method in GameAPI

- 描述

    设置全局触发器IMAGE_KEY数组 组变量子项

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

GameAPI.set_trigger_list_actor_variable_image_key(actor, "key", 1, 1)
```

---

## set_trigger_variable_image_key

method in GameAPI

- 描述

    设置全局触发器IMAGE_KEY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | integer | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_image_key("key", 1)
```

---

## set_trigger_actor_variable_image_key

method in GameAPI

- 描述

    设置全局触发器IMAGE_KEY非数组 组变量

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

GameAPI.set_trigger_actor_variable_image_key(actor, "key", 1)
```

---

## set_trigger_list_variable_angle

method in GameAPI

- 描述

    设置全局触发器ANGLE数组变量子项

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
GameAPI.set_trigger_list_variable_angle("key", 1, Fix32(1))
```

---

## set_trigger_list_actor_variable_angle

method in GameAPI

- 描述

    设置全局触发器ANGLE数组 组变量子项

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

GameAPI.set_trigger_list_actor_variable_angle(actor, "key", 1, Fix32(1))
```

---

## set_trigger_variable_angle

method in GameAPI

- 描述

    设置全局触发器ANGLE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.Fixed | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_angle("key", Fix32(1))
```

---

## set_trigger_actor_variable_angle

method in GameAPI

- 描述

    设置全局触发器ANGLE非数组 组变量

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

GameAPI.set_trigger_actor_variable_angle(actor, "key", Fix32(1))
```

---

## set_trigger_list_variable_texture

method in GameAPI

- 描述

    设置全局触发器TEXTURE数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Texture | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_list_variable_texture("key", 1, 1)
```

---

## set_trigger_list_actor_variable_texture

method in GameAPI

- 描述

    设置全局触发器TEXTURE数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Texture | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_list_actor_variable_texture(actor, "key", 1, 1)
```

---

## set_trigger_variable_texture

method in GameAPI

- 描述

    设置全局触发器TEXTURE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.Texture | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_texture("key", 1)
```

---

## set_trigger_actor_variable_texture

method in GameAPI

- 描述

    设置全局触发器TEXTURE非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.Texture | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_actor_variable_texture(actor, "key", 1)
```

---

## set_trigger_list_variable_sequence

method in GameAPI

- 描述

    设置全局触发器SEQUENCE数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Sequence | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_list_variable_sequence("key", 1, 1)
```

---

## set_trigger_list_actor_variable_sequence

method in GameAPI

- 描述

    设置全局触发器SEQUENCE数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Sequence | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_list_actor_variable_sequence(actor, "key", 1, 1)
```

---

## set_trigger_variable_sequence

method in GameAPI

- 描述

    设置全局触发器SEQUENCE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.Sequence | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_sequence("key", 1)
```

---

## set_trigger_actor_variable_sequence

method in GameAPI

- 描述

    设置全局触发器SEQUENCE非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.Sequence | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_actor_variable_sequence(actor, "key", 1)
```

---

## set_trigger_list_variable_physics_object

method in GameAPI

- 描述

    设置全局触发器PHYSICS_OBJECT数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.PhysicsObject | 值 |

- 返回值

    无

- 示例

```lua
local physics_object = GameAPI.get_unit_key_physics_object_kv(1, "key")

GameAPI.set_trigger_list_variable_physics_object("key", 1)
```

---

## set_trigger_list_actor_variable_physics_object

method in GameAPI

- 描述

    设置全局触发器PHYSICS_OBJECT数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.PhysicsObject | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local physics_object = GameAPI.get_unit_key_physics_object_kv(1, "key")

GameAPI.set_trigger_list_actor_variable_physics_object(actor, "key", 1)
```

---

## set_trigger_variable_physics_object

method in GameAPI

- 描述

    设置全局触发器PHYSICS_OBJECT非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.PhysicsObject | 值 |

- 返回值

    无

- 示例

```lua
local physics_object = GameAPI.get_unit_key_physics_object_kv(1, "key")

GameAPI.set_trigger_variable_physics_object("key")
```

---

## set_trigger_actor_variable_physics_object

method in GameAPI

- 描述

    设置全局触发器PHYSICS_OBJECT非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.PhysicsObject | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local physics_object = GameAPI.get_unit_key_physics_object_kv(1, "key")

GameAPI.set_trigger_actor_variable_physics_object(actor, "key")
```

---

## set_trigger_list_variable_physics_entity

method in GameAPI

- 描述

    设置全局触发器PHYSICS_ENTITY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.PhysicsEntity | 值 |

- 返回值

    无

- 示例

```lua
local physics_entity = GameAPI.get_unit_key_physics_entity_kv(1, "key")

GameAPI.set_trigger_list_variable_physics_entity("key", 1)
```

---

## set_trigger_list_actor_variable_physics_entity

method in GameAPI

- 描述

    设置全局触发器PHYSICS_ENTITY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.PhysicsEntity | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local physics_entity = GameAPI.get_unit_key_physics_entity_kv(1, "key")

GameAPI.set_trigger_list_actor_variable_physics_entity(actor, "key", 1)
```

---

## set_trigger_variable_physics_entity

method in GameAPI

- 描述

    设置全局触发器PHYSICS_ENTITY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.PhysicsEntity | 值 |

- 返回值

    无

- 示例

```lua
local physics_entity = GameAPI.get_unit_key_physics_entity_kv(1, "key")

GameAPI.set_trigger_variable_physics_entity("key")
```

---

## set_trigger_actor_variable_physics_entity

method in GameAPI

- 描述

    设置全局触发器PHYSICS_ENTITY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.PhysicsEntity | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local physics_entity = GameAPI.get_unit_key_physics_entity_kv(1, "key")

GameAPI.set_trigger_actor_variable_physics_entity(actor, "key")
```

---

## set_trigger_list_variable_physics_object_key

method in GameAPI

- 描述

    设置全局触发器PHYSICS_OBJECT_KEY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.PhysicsObjectKey | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_list_variable_physics_object_key("key", 1, 1)
```

---

## set_trigger_list_actor_variable_physics_object_key

method in GameAPI

- 描述

    设置全局触发器PHYSICS_OBJECT_KEY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.PhysicsObjectKey | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_list_actor_variable_physics_object_key(actor, "key", 1, 1)
```

---

## set_trigger_variable_physics_object_key

method in GameAPI

- 描述

    设置全局触发器PHYSICS_OBJECT_KEY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.PhysicsObjectKey | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_physics_object_key("key", 1)
```

---

## set_trigger_actor_variable_physics_object_key

method in GameAPI

- 描述

    设置全局触发器PHYSICS_OBJECT_KEY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.PhysicsObjectKey | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_actor_variable_physics_object_key(actor, "key", 1)
```

---

## set_trigger_list_variable_physics_entity_key

method in GameAPI

- 描述

    设置全局触发器PHYSICS_ENTITY_KEY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.PhysicsEntityKey | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_list_variable_physics_entity_key("key", 1, 1)
```

---

## set_trigger_list_actor_variable_physics_entity_key

method in GameAPI

- 描述

    设置全局触发器PHYSICS_ENTITY_KEY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.PhysicsEntityKey | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_list_actor_variable_physics_entity_key(actor, "key", 1, 1)
```

---

## set_trigger_variable_physics_entity_key

method in GameAPI

- 描述

    设置全局触发器PHYSICS_ENTITY_KEY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.PhysicsEntityKey | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_physics_entity_key("key", 1)
```

---

## set_trigger_actor_variable_physics_entity_key

method in GameAPI

- 描述

    设置全局触发器PHYSICS_ENTITY_KEY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.PhysicsEntityKey | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_actor_variable_physics_entity_key(actor, "key", 1)
```

---

## set_trigger_list_variable_rigid_body

method in GameAPI

- 描述

    设置全局触发器RIGID_BODY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.RigidBody | 值 |

- 返回值

    无

- 示例

```lua
local rigid_body = GameAPI.get_unit_key_rigid_body_kv(1, "key")

GameAPI.set_trigger_list_variable_rigid_body("key", 1)
```

---

## set_trigger_list_actor_variable_rigid_body

method in GameAPI

- 描述

    设置全局触发器RIGID_BODY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.RigidBody | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local rigid_body = GameAPI.get_unit_key_rigid_body_kv(1, "key")

GameAPI.set_trigger_list_actor_variable_rigid_body(actor, "key", 1)
```

---

## set_trigger_variable_rigid_body

method in GameAPI

- 描述

    设置全局触发器RIGID_BODY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.RigidBody | 值 |

- 返回值

    无

- 示例

```lua
local rigid_body = GameAPI.get_unit_key_rigid_body_kv(1, "key")

GameAPI.set_trigger_variable_rigid_body("key")
```

---

## set_trigger_actor_variable_rigid_body

method in GameAPI

- 描述

    设置全局触发器RIGID_BODY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.RigidBody | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local rigid_body = GameAPI.get_unit_key_rigid_body_kv(1, "key")

GameAPI.set_trigger_actor_variable_rigid_body(actor, "key")
```

---

## set_trigger_list_variable_rigid_body_group

method in GameAPI

- 描述

    设置全局触发器RIGID_BODY_GROUP数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.RigidBodyGroup | 值 |

- 返回值

    无

- 示例

```lua
local rigid_body_group = GameAPI.get_unit_key_rigid_body_group_kv(1, "key")

GameAPI.set_trigger_list_variable_rigid_body_group("key", 1)
```

---

## set_trigger_list_actor_variable_rigid_body_group

method in GameAPI

- 描述

    设置全局触发器RIGID_BODY_GROUP数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.RigidBodyGroup | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local rigid_body_group = GameAPI.get_unit_key_rigid_body_group_kv(1, "key")

GameAPI.set_trigger_list_actor_variable_rigid_body_group(actor, "key", 1)
```

---

## set_trigger_variable_rigid_body_group

method in GameAPI

- 描述

    设置全局触发器RIGID_BODY_GROUP非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.RigidBodyGroup | 值 |

- 返回值

    无

- 示例

```lua
local rigid_body_group = GameAPI.get_unit_key_rigid_body_group_kv(1, "key")

GameAPI.set_trigger_variable_rigid_body_group("key")
```

---

## set_trigger_actor_variable_rigid_body_group

method in GameAPI

- 描述

    设置全局触发器RIGID_BODY_GROUP非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.RigidBodyGroup | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local rigid_body_group = GameAPI.get_unit_key_rigid_body_group_kv(1, "key")

GameAPI.set_trigger_actor_variable_rigid_body_group(actor, "key")
```

---

## set_trigger_list_variable_collider

method in GameAPI

- 描述

    设置全局触发器COLLIDER数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Collider | 值 |

- 返回值

    无

- 示例

```lua
local collider = GameAPI.get_unit_key_collider_kv(1, "key")

GameAPI.set_trigger_list_variable_collider("key", 1)
```

---

## set_trigger_list_actor_variable_collider

method in GameAPI

- 描述

    设置全局触发器COLLIDER数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Collider | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local collider = GameAPI.get_unit_key_collider_kv(1, "key")

GameAPI.set_trigger_list_actor_variable_collider(actor, "key", 1)
```

---

## set_trigger_variable_collider

method in GameAPI

- 描述

    设置全局触发器COLLIDER非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.Collider | 值 |

- 返回值

    无

- 示例

```lua
local collider = GameAPI.get_unit_key_collider_kv(1, "key")

GameAPI.set_trigger_variable_collider("key")
```

---

## set_trigger_actor_variable_collider

method in GameAPI

- 描述

    设置全局触发器COLLIDER非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.Collider | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local collider = GameAPI.get_unit_key_collider_kv(1, "key")

GameAPI.set_trigger_actor_variable_collider(actor, "key")
```

---

## set_trigger_list_variable_joint

method in GameAPI

- 描述

    设置全局触发器JOINT数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Joint | 值 |

- 返回值

    无

- 示例

```lua
local joint = GameAPI.get_unit_key_joint_kv(1, "key")

GameAPI.set_trigger_list_variable_joint("key", 1)
```

---

## has_ability_key_rescue_seeker_type_kv

method in GameAPI

- 描述

    判断技能编号是否存在RESCUE_SEEKER_TYPE键值对

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

local result = GameAPI.has_ability_key_rescue_seeker_type_kv(ability_key, "key")
```

---

## has_kv_pair_rescuer_type

method in GameAPI

- 描述

    判断是否存在RESCUER_TYPE键值对

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

local result = GameAPI.has_kv_pair_rescuer_type(kvbase, "key")
```

---

## has_prefab_rescuer_type_kv

method in GameAPI

- 描述

    判断预设是否存在RESCUER_TYPE键值对

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

local result = GameAPI.has_prefab_rescuer_type_kv("prefab_type", unit_key, "key")
```

---

## has_unit_key_rescuer_type_kv

method in GameAPI

- 描述

    判断单位编号是否存在RESCUER_TYPE键值对

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

local result = GameAPI.has_unit_key_rescuer_type_kv(unit_key, "key")
```

---

## has_item_key_rescuer_type_kv

method in GameAPI

- 描述

    判断物品编号是否存在RESCUER_TYPE键值对

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

local result = GameAPI.has_item_key_rescuer_type_kv(item_key, "key")
```

---

## has_ability_key_rescuer_type_kv

method in GameAPI

- 描述

    判断技能编号是否存在RESCUER_TYPE键值对

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

local result = GameAPI.has_ability_key_rescuer_type_kv(ability_key, "key")
```

---

## has_kv_pair_store_item_type

method in GameAPI

- 描述

    判断是否存在STORE_ITEM_TYPE键值对

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

local result = GameAPI.has_kv_pair_store_item_type(kvbase, "key")
```

---

## has_prefab_store_item_type_kv

method in GameAPI

- 描述

    判断预设是否存在STORE_ITEM_TYPE键值对

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

local result = GameAPI.has_prefab_store_item_type_kv("prefab_type", unit_key, "key")
```

---

## has_unit_key_store_item_type_kv

method in GameAPI

- 描述

    判断单位编号是否存在STORE_ITEM_TYPE键值对

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

local result = GameAPI.has_unit_key_store_item_type_kv(unit_key, "key")
```

---

## has_item_key_store_item_type_kv

method in GameAPI

- 描述

    判断物品编号是否存在STORE_ITEM_TYPE键值对

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

local result = GameAPI.has_item_key_store_item_type_kv(item_key, "key")
```

---

## has_ability_key_store_item_type_kv

method in GameAPI

- 描述

    判断技能编号是否存在STORE_ITEM_TYPE键值对

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

local result = GameAPI.has_ability_key_store_item_type_kv(ability_key, "key")
```

---

## has_kv_pair_site_state

method in GameAPI

- 描述

    判断是否存在SITE_STATE键值对

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

local result = GameAPI.has_kv_pair_site_state(kvbase, "key")
```

---

## has_prefab_site_state_kv

method in GameAPI

- 描述

    判断预设是否存在SITE_STATE键值对

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

local result = GameAPI.has_prefab_site_state_kv("prefab_type", unit_key, "key")
```

---

## has_unit_key_site_state_kv

method in GameAPI

- 描述

    判断单位编号是否存在SITE_STATE键值对

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

local result = GameAPI.has_unit_key_site_state_kv(unit_key, "key")
```

---

## has_item_key_site_state_kv

method in GameAPI

- 描述

    判断物品编号是否存在SITE_STATE键值对

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

local result = GameAPI.has_item_key_site_state_kv(item_key, "key")
```

---

## has_ability_key_site_state_kv

method in GameAPI

- 描述

    判断技能编号是否存在SITE_STATE键值对

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

local result = GameAPI.has_ability_key_site_state_kv(ability_key, "key")
```

---

## has_kv_pair_coin_currency

method in GameAPI

- 描述

    判断是否存在COIN_CURRENCY键值对

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

local result = GameAPI.has_kv_pair_coin_currency(kvbase, "key")
```

---

## has_prefab_coin_currency_kv

method in GameAPI

- 描述

    判断预设是否存在COIN_CURRENCY键值对

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

local result = GameAPI.has_prefab_coin_currency_kv("prefab_type", unit_key, "key")
```

---

## has_unit_key_coin_currency_kv

method in GameAPI

- 描述

    判断单位编号是否存在COIN_CURRENCY键值对

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

local result = GameAPI.has_unit_key_coin_currency_kv(unit_key, "key")
```

---

## has_item_key_coin_currency_kv

method in GameAPI

- 描述

    判断物品编号是否存在COIN_CURRENCY键值对

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

local result = GameAPI.has_item_key_coin_currency_kv(item_key, "key")
```

---

## has_ability_key_coin_currency_kv

method in GameAPI

- 描述

    判断技能编号是否存在COIN_CURRENCY键值对

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

local result = GameAPI.has_ability_key_coin_currency_kv(ability_key, "key")
```

---

## api_serialize_kv

method in GameAPI

- 描述

    序列化KV

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.Actor | Actor |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 序列化结果 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.api_serialize_kv(actor)
```

---

## api_deserialize_kv

method in GameAPI

- 描述

    反序列化KV

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.Actor | Actor |
    | json_str | string | kv |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.api_deserialize_kv(actor, "json_str")
```

---

## get_unit_key_xxx_kv

method in GameAPI

- 描述

    获取单位编号键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    无

- 示例

```lua
local unit_key = 134274569

GameAPI.get_unit_key_xxx_kv(unit_key, "key")
```

---

## get_item_key_xxx_kv

method in GameAPI

- 描述

    获取物品编号键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    无

- 示例

```lua
local item_key = 134274569

GameAPI.get_item_key_xxx_kv(item_key, "key")
```

---

## get_ability_key_xxx_kv

method in GameAPI

- 描述

    获取技能编号键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    无

- 示例

```lua
local ability_key = 134274569

GameAPI.get_ability_key_xxx_kv(ability_key, "key")
```

---

## get_modifier_key_xxx_kv

method in GameAPI

- 描述

    获取魔法效果特效编号键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    无

- 示例

```lua
local modifier_key = 134274569

GameAPI.get_modifier_key_xxx_kv(modifier_key, "key")
```

---

## get_projectile_key_xxx_kv

method in GameAPI

- 描述

    获取特效编号键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    无

- 示例

```lua
local projectile_key = 134274569

GameAPI.get_projectile_key_xxx_kv(projectile_key, "key")
```

---

## get_destructible_key_xxx_kv

method in GameAPI

- 描述

    获取可破坏物编号键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    无

- 示例

```lua
local destructible_key = 1

GameAPI.get_destructible_key_xxx_kv(destructible_key, "key")
```

---

## get_tech_key_xxx_kv

method in GameAPI

- 描述

    获取科技编号键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    无

- 示例

```lua
local tech_key = 134274569

GameAPI.get_tech_key_xxx_kv(tech_key, "key")
```

---

## get_icon_id_xxx_kv

method in GameAPI

- 描述

    获取图片键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    无

- 示例

```lua
GameAPI.get_icon_id_xxx_kv(1, "key")
```

---

## get_physics_entity_key_xxx_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    无

- 示例

```lua
GameAPI.get_physics_entity_key_xxx_kv(1, "key")
```

---

## get_entity_ckv_pair_value_xxx

method in GameAPI

- 描述

    获取值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.get_entity_ckv_pair_value_xxx(kvbase, "key")
```

---

## get_ability_ckv_pair_value_xxx

method in GameAPI

- 描述

    获取值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.get_ability_ckv_pair_value_xxx(kvbase, "key")
```

---

## get_modifier_ckv_pair_value_xxx

method in GameAPI

- 描述

    获取值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GameAPI.get_modifier_ckv_pair_value_xxx(kvbase, "key")
```

---

## get_unit_key_ui_gridview_type_kv

method in GameAPI

- 描述

    获取单位编号UI_GRIDVIEW_TYPE键值对

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

local result = GameAPI.get_unit_key_ui_gridview_type_kv(unit_key, "key")
```

---

## get_item_key_ui_gridview_type_kv

method in GameAPI

- 描述

    获取物品编号UI_GRIDVIEW_TYPE键值对

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

local result = GameAPI.get_item_key_ui_gridview_type_kv(item_key, "key")
```

---

## get_ability_key_ui_gridview_type_kv

method in GameAPI

- 描述

    获取技能编号UI_GRIDVIEW_TYPE键值对

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

local result = GameAPI.get_ability_key_ui_gridview_type_kv(ability_key, "key")
```

---

## get_modifier_key_ui_gridview_type_kv

method in GameAPI

- 描述

    获取魔法效果特效编号UI_GRIDVIEW_TYPE键值对

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

local result = GameAPI.get_modifier_key_ui_gridview_type_kv(modifier_key, "key")
```

---

## get_projectile_key_ui_gridview_type_kv

method in GameAPI

- 描述

    获取特效编号UI_GRIDVIEW_TYPE键值对

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

local result = GameAPI.get_projectile_key_ui_gridview_type_kv(projectile_key, "key")
```

---

## get_destructible_key_ui_gridview_type_kv

method in GameAPI

- 描述

    获取可破坏物编号UI_GRIDVIEW_TYPE键值对

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

local result = GameAPI.get_destructible_key_ui_gridview_type_kv(destructible_key, "key")
```

---

## get_tech_key_ui_gridview_type_kv

method in GameAPI

- 描述

    获取科技编号UI_GRIDVIEW_TYPE键值对

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

local result = GameAPI.get_tech_key_ui_gridview_type_kv(tech_key, "key")
```

---

## get_icon_id_ui_gridview_type_kv

method in GameAPI

- 描述

    获取图片UI_GRIDVIEW_TYPE键值对

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
local result = GameAPI.get_icon_id_ui_gridview_type_kv(1, "key")
```

---

## get_physics_entity_key_ui_gridview_type_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型UI_GRIDVIEW_TYPE键值对

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
local result = GameAPI.get_physics_entity_key_ui_gridview_type_kv(1, "key")
```

---

## get_kv_pair_value_ui_gridview_type

method in GameAPI

- 描述

    获取UI_GRIDVIEW_TYPE键值对

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

local result = GameAPI.get_kv_pair_value_ui_gridview_type(kvbase, "key")
```

---

## get_unit_key_ui_gridview_bar_type_kv

method in GameAPI

- 描述

    获取单位编号UI_GRIDVIEW_BAR_TYPE键值对

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

local result = GameAPI.get_unit_key_ui_gridview_bar_type_kv(unit_key, "key")
```

---

## get_item_key_ui_gridview_bar_type_kv

method in GameAPI

- 描述

    获取物品编号UI_GRIDVIEW_BAR_TYPE键值对

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

local result = GameAPI.get_item_key_ui_gridview_bar_type_kv(item_key, "key")
```

---

## get_ability_key_ui_gridview_bar_type_kv

method in GameAPI

- 描述

    获取技能编号UI_GRIDVIEW_BAR_TYPE键值对

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

local result = GameAPI.get_ability_key_ui_gridview_bar_type_kv(ability_key, "key")
```

---

## get_modifier_key_ui_gridview_bar_type_kv

method in GameAPI

- 描述

    获取魔法效果特效编号UI_GRIDVIEW_BAR_TYPE键值对

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

local result = GameAPI.get_modifier_key_ui_gridview_bar_type_kv(modifier_key, "key")
```

---

## get_projectile_key_ui_gridview_bar_type_kv

method in GameAPI

- 描述

    获取特效编号UI_GRIDVIEW_BAR_TYPE键值对

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

local result = GameAPI.get_projectile_key_ui_gridview_bar_type_kv(projectile_key, "key")
```

---

## get_destructible_key_ui_gridview_bar_type_kv

method in GameAPI

- 描述

    获取可破坏物编号UI_GRIDVIEW_BAR_TYPE键值对

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

local result = GameAPI.get_destructible_key_ui_gridview_bar_type_kv(destructible_key, "key")
```

---

## get_tech_key_ui_gridview_bar_type_kv

method in GameAPI

- 描述

    获取科技编号UI_GRIDVIEW_BAR_TYPE键值对

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

local result = GameAPI.get_tech_key_ui_gridview_bar_type_kv(tech_key, "key")
```

---

## get_icon_id_ui_gridview_bar_type_kv

method in GameAPI

- 描述

    获取图片UI_GRIDVIEW_BAR_TYPE键值对

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
local result = GameAPI.get_icon_id_ui_gridview_bar_type_kv(1, "key")
```

---

## get_physics_entity_key_ui_gridview_bar_type_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型UI_GRIDVIEW_BAR_TYPE键值对

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
local result = GameAPI.get_physics_entity_key_ui_gridview_bar_type_kv(1, "key")
```

---

## get_kv_pair_value_ui_gridview_bar_type

method in GameAPI

- 描述

    获取UI_GRIDVIEW_BAR_TYPE键值对

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

local result = GameAPI.get_kv_pair_value_ui_gridview_bar_type(kvbase, "key")
```

---

## get_unit_key_ui_effect_camera_mode_kv

method in GameAPI

- 描述

    获取单位编号UI_EFFECT_CAMERA_MODE键值对

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

local result = GameAPI.get_unit_key_ui_effect_camera_mode_kv(unit_key, "key")
```

---

## get_item_key_ui_effect_camera_mode_kv

method in GameAPI

- 描述

    获取物品编号UI_EFFECT_CAMERA_MODE键值对

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

local result = GameAPI.get_item_key_ui_effect_camera_mode_kv(item_key, "key")
```

---

## get_ability_key_ui_effect_camera_mode_kv

method in GameAPI

- 描述

    获取技能编号UI_EFFECT_CAMERA_MODE键值对

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

local result = GameAPI.get_ability_key_ui_effect_camera_mode_kv(ability_key, "key")
```

---

## get_modifier_key_ui_effect_camera_mode_kv

method in GameAPI

- 描述

    获取魔法效果特效编号UI_EFFECT_CAMERA_MODE键值对

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

local result = GameAPI.get_modifier_key_ui_effect_camera_mode_kv(modifier_key, "key")
```

---

## get_projectile_key_ui_effect_camera_mode_kv

method in GameAPI

- 描述

    获取特效编号UI_EFFECT_CAMERA_MODE键值对

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

local result = GameAPI.get_projectile_key_ui_effect_camera_mode_kv(projectile_key, "key")
```

---

## get_destructible_key_ui_effect_camera_mode_kv

method in GameAPI

- 描述

    获取可破坏物编号UI_EFFECT_CAMERA_MODE键值对

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

local result = GameAPI.get_destructible_key_ui_effect_camera_mode_kv(destructible_key, "key")
```

---

## get_tech_key_ui_effect_camera_mode_kv

method in GameAPI

- 描述

    获取科技编号UI_EFFECT_CAMERA_MODE键值对

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

local result = GameAPI.get_tech_key_ui_effect_camera_mode_kv(tech_key, "key")
```

---

## get_icon_id_ui_effect_camera_mode_kv

method in GameAPI

- 描述

    获取图片UI_EFFECT_CAMERA_MODE键值对

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
local result = GameAPI.get_icon_id_ui_effect_camera_mode_kv(1, "key")
```

---

## get_physics_entity_key_ui_effect_camera_mode_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型UI_EFFECT_CAMERA_MODE键值对

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
local result = GameAPI.get_physics_entity_key_ui_effect_camera_mode_kv(1, "key")
```

---

## get_kv_pair_value_ui_effect_camera_mode

method in GameAPI

- 描述

    获取UI_EFFECT_CAMERA_MODE键值对

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

local result = GameAPI.get_kv_pair_value_ui_effect_camera_mode(kvbase, "key")
```

---

## get_unit_key_ui_equip_slot_use_type_kv

method in GameAPI

- 描述

    获取单位编号UI_EQUIP_SLOT_USE_TYPE键值对

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

local result = GameAPI.get_unit_key_ui_equip_slot_use_type_kv(unit_key, "key")
```

---

## get_item_key_ui_equip_slot_use_type_kv

method in GameAPI

- 描述

    获取物品编号UI_EQUIP_SLOT_USE_TYPE键值对

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

local result = GameAPI.get_item_key_ui_equip_slot_use_type_kv(item_key, "key")
```

---

## get_ability_key_ui_equip_slot_use_type_kv

method in GameAPI

- 描述

    获取技能编号UI_EQUIP_SLOT_USE_TYPE键值对

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

local result = GameAPI.get_ability_key_ui_equip_slot_use_type_kv(ability_key, "key")
```

---

## get_modifier_key_ui_equip_slot_use_type_kv

method in GameAPI

- 描述

    获取魔法效果特效编号UI_EQUIP_SLOT_USE_TYPE键值对

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

local result = GameAPI.get_modifier_key_ui_equip_slot_use_type_kv(modifier_key, "key")
```

---

## get_projectile_key_ui_equip_slot_use_type_kv

method in GameAPI

- 描述

    获取特效编号UI_EQUIP_SLOT_USE_TYPE键值对

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

local result = GameAPI.get_projectile_key_ui_equip_slot_use_type_kv(projectile_key, "key")
```

---

## get_destructible_key_ui_equip_slot_use_type_kv

method in GameAPI

- 描述

    获取可破坏物编号UI_EQUIP_SLOT_USE_TYPE键值对

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

local result = GameAPI.get_destructible_key_ui_equip_slot_use_type_kv(destructible_key, "key")
```

---

## get_tech_key_ui_equip_slot_use_type_kv

method in GameAPI

- 描述

    获取科技编号UI_EQUIP_SLOT_USE_TYPE键值对

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

local result = GameAPI.get_tech_key_ui_equip_slot_use_type_kv(tech_key, "key")
```

---

## get_icon_id_ui_equip_slot_use_type_kv

method in GameAPI

- 描述

    获取图片UI_EQUIP_SLOT_USE_TYPE键值对

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
local result = GameAPI.get_icon_id_ui_equip_slot_use_type_kv(1, "key")
```

---

## get_physics_entity_key_ui_equip_slot_use_type_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型UI_EQUIP_SLOT_USE_TYPE键值对

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
local result = GameAPI.get_physics_entity_key_ui_equip_slot_use_type_kv(1, "key")
```

---

## get_kv_pair_value_ui_equip_slot_use_type

method in GameAPI

- 描述

    获取UI_EQUIP_SLOT_USE_TYPE键值对

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

local result = GameAPI.get_kv_pair_value_ui_equip_slot_use_type(kvbase, "key")
```

---

## get_unit_key_ui_equip_slot_drag_type_kv

method in GameAPI

- 描述

    获取单位编号UI_EQUIP_SLOT_DRAG_TYPE键值对

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

local result = GameAPI.get_unit_key_ui_equip_slot_drag_type_kv(unit_key, "key")
```

---

## get_item_key_ui_equip_slot_drag_type_kv

method in GameAPI

- 描述

    获取物品编号UI_EQUIP_SLOT_DRAG_TYPE键值对

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

local result = GameAPI.get_item_key_ui_equip_slot_drag_type_kv(item_key, "key")
```

---

## get_ability_key_ui_equip_slot_drag_type_kv

method in GameAPI

- 描述

    获取技能编号UI_EQUIP_SLOT_DRAG_TYPE键值对

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

local result = GameAPI.get_ability_key_ui_equip_slot_drag_type_kv(ability_key, "key")
```

---

## get_modifier_key_ui_equip_slot_drag_type_kv

method in GameAPI

- 描述

    获取魔法效果特效编号UI_EQUIP_SLOT_DRAG_TYPE键值对

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

local result = GameAPI.get_modifier_key_ui_equip_slot_drag_type_kv(modifier_key, "key")
```

---

## get_projectile_key_ui_equip_slot_drag_type_kv

method in GameAPI

- 描述

    获取特效编号UI_EQUIP_SLOT_DRAG_TYPE键值对

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

local result = GameAPI.get_projectile_key_ui_equip_slot_drag_type_kv(projectile_key, "key")
```

---

## get_destructible_key_ui_equip_slot_drag_type_kv

method in GameAPI

- 描述

    获取可破坏物编号UI_EQUIP_SLOT_DRAG_TYPE键值对

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

local result = GameAPI.get_destructible_key_ui_equip_slot_drag_type_kv(destructible_key, "key")
```

---

## get_tech_key_ui_equip_slot_drag_type_kv

method in GameAPI

- 描述

    获取科技编号UI_EQUIP_SLOT_DRAG_TYPE键值对

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

local result = GameAPI.get_tech_key_ui_equip_slot_drag_type_kv(tech_key, "key")
```

---

## get_icon_id_ui_equip_slot_drag_type_kv

method in GameAPI

- 描述

    获取图片UI_EQUIP_SLOT_DRAG_TYPE键值对

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
local result = GameAPI.get_icon_id_ui_equip_slot_drag_type_kv(1, "key")
```

---

## get_physics_entity_key_ui_equip_slot_drag_type_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型UI_EQUIP_SLOT_DRAG_TYPE键值对

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
local result = GameAPI.get_physics_entity_key_ui_equip_slot_drag_type_kv(1, "key")
```

---

## get_kv_pair_value_ui_equip_slot_drag_type

method in GameAPI

- 描述

    获取UI_EQUIP_SLOT_DRAG_TYPE键值对

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

local result = GameAPI.get_kv_pair_value_ui_equip_slot_drag_type(kvbase, "key")
```

---

## get_unit_key_ui_layout_clipping_type_kv

method in GameAPI

- 描述

    获取单位编号UI_LAYOUT_CLIPPING_TYPE键值对

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

local result = GameAPI.get_unit_key_ui_layout_clipping_type_kv(unit_key, "key")
```

---

## get_item_key_ui_layout_clipping_type_kv

method in GameAPI

- 描述

    获取物品编号UI_LAYOUT_CLIPPING_TYPE键值对

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

local result = GameAPI.get_item_key_ui_layout_clipping_type_kv(item_key, "key")
```

---

## get_ability_key_ui_layout_clipping_type_kv

method in GameAPI

- 描述

    获取技能编号UI_LAYOUT_CLIPPING_TYPE键值对

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

local result = GameAPI.get_ability_key_ui_layout_clipping_type_kv(ability_key, "key")
```

---

## get_modifier_key_ui_layout_clipping_type_kv

method in GameAPI

- 描述

    获取魔法效果特效编号UI_LAYOUT_CLIPPING_TYPE键值对

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

local result = GameAPI.get_modifier_key_ui_layout_clipping_type_kv(modifier_key, "key")
```

---

## get_projectile_key_ui_layout_clipping_type_kv

method in GameAPI

- 描述

    获取特效编号UI_LAYOUT_CLIPPING_TYPE键值对

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

local result = GameAPI.get_projectile_key_ui_layout_clipping_type_kv(projectile_key, "key")
```

---

## get_destructible_key_ui_layout_clipping_type_kv

method in GameAPI

- 描述

    获取可破坏物编号UI_LAYOUT_CLIPPING_TYPE键值对

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

local result = GameAPI.get_destructible_key_ui_layout_clipping_type_kv(destructible_key, "key")
```

---

## get_tech_key_ui_layout_clipping_type_kv

method in GameAPI

- 描述

    获取科技编号UI_LAYOUT_CLIPPING_TYPE键值对

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

local result = GameAPI.get_tech_key_ui_layout_clipping_type_kv(tech_key, "key")
```

---

## get_icon_id_ui_layout_clipping_type_kv

method in GameAPI

- 描述

    获取图片UI_LAYOUT_CLIPPING_TYPE键值对

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
local result = GameAPI.get_icon_id_ui_layout_clipping_type_kv(1, "key")
```

---

## get_physics_entity_key_ui_layout_clipping_type_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型UI_LAYOUT_CLIPPING_TYPE键值对

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
local result = GameAPI.get_physics_entity_key_ui_layout_clipping_type_kv(1, "key")
```

---

## get_kv_pair_value_ui_layout_clipping_type

method in GameAPI

- 描述

    获取UI_LAYOUT_CLIPPING_TYPE键值对

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

local result = GameAPI.get_kv_pair_value_ui_layout_clipping_type(kvbase, "key")
```

---

## get_unit_key_ui_text_over_length_handling_type_kv

method in GameAPI

- 描述

    获取单位编号UI_TEXT_OVER_LENGTH_HANDLING_TYPE键值对

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

local result = GameAPI.get_unit_key_ui_text_over_length_handling_type_kv(unit_key, "key")
```

---

## get_item_key_ui_text_over_length_handling_type_kv

method in GameAPI

- 描述

    获取物品编号UI_TEXT_OVER_LENGTH_HANDLING_TYPE键值对

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

local result = GameAPI.get_item_key_ui_text_over_length_handling_type_kv(item_key, "key")
```

---

## get_ability_key_ui_text_over_length_handling_type_kv

method in GameAPI

- 描述

    获取技能编号UI_TEXT_OVER_LENGTH_HANDLING_TYPE键值对

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

local result = GameAPI.get_ability_key_ui_text_over_length_handling_type_kv(ability_key, "key")
```

---

## get_modifier_key_ui_text_over_length_handling_type_kv

method in GameAPI

- 描述

    获取魔法效果特效编号UI_TEXT_OVER_LENGTH_HANDLING_TYPE键值对

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

local result = GameAPI.get_modifier_key_ui_text_over_length_handling_type_kv(modifier_key, "key")
```

---

## get_projectile_key_ui_text_over_length_handling_type_kv

method in GameAPI

- 描述

    获取特效编号UI_TEXT_OVER_LENGTH_HANDLING_TYPE键值对

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

local result = GameAPI.get_projectile_key_ui_text_over_length_handling_type_kv(projectile_key, "key")
```

---

## get_destructible_key_ui_text_over_length_handling_type_kv

method in GameAPI

- 描述

    获取可破坏物编号UI_TEXT_OVER_LENGTH_HANDLING_TYPE键值对

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

local result = GameAPI.get_destructible_key_ui_text_over_length_handling_type_kv(destructible_key, "key")
```

---

## get_tech_key_ui_text_over_length_handling_type_kv

method in GameAPI

- 描述

    获取科技编号UI_TEXT_OVER_LENGTH_HANDLING_TYPE键值对

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

local result = GameAPI.get_tech_key_ui_text_over_length_handling_type_kv(tech_key, "key")
```

---

## get_icon_id_ui_text_over_length_handling_type_kv

method in GameAPI

- 描述

    获取图片UI_TEXT_OVER_LENGTH_HANDLING_TYPE键值对

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
local result = GameAPI.get_icon_id_ui_text_over_length_handling_type_kv(1, "key")
```

---

## get_physics_entity_key_ui_text_over_length_handling_type_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型UI_TEXT_OVER_LENGTH_HANDLING_TYPE键值对

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
local result = GameAPI.get_physics_entity_key_ui_text_over_length_handling_type_kv(1, "key")
```

---

## get_kv_pair_value_ui_text_over_length_handling_type

method in GameAPI

- 描述

    获取UI_TEXT_OVER_LENGTH_HANDLING_TYPE键值对

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

local result = GameAPI.get_kv_pair_value_ui_text_over_length_handling_type(kvbase, "key")
```

---

## get_unit_key_ui_pos_adapt_mode_kv

method in GameAPI

- 描述

    获取单位编号UI_POS_ADAPT_MODE键值对

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

local result = GameAPI.get_unit_key_ui_pos_adapt_mode_kv(unit_key, "key")
```

---

## get_item_key_ui_pos_adapt_mode_kv

method in GameAPI

- 描述

    获取物品编号UI_POS_ADAPT_MODE键值对

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

local result = GameAPI.get_item_key_ui_pos_adapt_mode_kv(item_key, "key")
```

---

## get_ability_key_ui_pos_adapt_mode_kv

method in GameAPI

- 描述

    获取技能编号UI_POS_ADAPT_MODE键值对

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

local result = GameAPI.get_ability_key_ui_pos_adapt_mode_kv(ability_key, "key")
```

---

## get_modifier_key_ui_pos_adapt_mode_kv

method in GameAPI

- 描述

    获取魔法效果特效编号UI_POS_ADAPT_MODE键值对

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

local result = GameAPI.get_modifier_key_ui_pos_adapt_mode_kv(modifier_key, "key")
```

---

## get_projectile_key_ui_pos_adapt_mode_kv

method in GameAPI

- 描述

    获取特效编号UI_POS_ADAPT_MODE键值对

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

local result = GameAPI.get_projectile_key_ui_pos_adapt_mode_kv(projectile_key, "key")
```

---

## get_destructible_key_ui_pos_adapt_mode_kv

method in GameAPI

- 描述

    获取可破坏物编号UI_POS_ADAPT_MODE键值对

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

local result = GameAPI.get_destructible_key_ui_pos_adapt_mode_kv(destructible_key, "key")
```

---

## get_tech_key_ui_pos_adapt_mode_kv

method in GameAPI

- 描述

    获取科技编号UI_POS_ADAPT_MODE键值对

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

local result = GameAPI.get_tech_key_ui_pos_adapt_mode_kv(tech_key, "key")
```

---

## get_icon_id_ui_pos_adapt_mode_kv

method in GameAPI

- 描述

    获取图片UI_POS_ADAPT_MODE键值对

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
local result = GameAPI.get_icon_id_ui_pos_adapt_mode_kv(1, "key")
```

---

## get_physics_entity_key_ui_pos_adapt_mode_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型UI_POS_ADAPT_MODE键值对

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
local result = GameAPI.get_physics_entity_key_ui_pos_adapt_mode_kv(1, "key")
```

---

## get_kv_pair_value_ui_pos_adapt_mode

method in GameAPI

- 描述

    获取UI_POS_ADAPT_MODE键值对

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

local result = GameAPI.get_kv_pair_value_ui_pos_adapt_mode(kvbase, "key")
```

---

## get_unit_key_ui_chat_send_channel_kv

method in GameAPI

- 描述

    获取单位编号UI_CHAT_SEND_CHANNEL键值对

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

local result = GameAPI.get_unit_key_ui_chat_send_channel_kv(unit_key, "key")
```

---

## get_item_key_ui_chat_send_channel_kv

method in GameAPI

- 描述

    获取物品编号UI_CHAT_SEND_CHANNEL键值对

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

local result = GameAPI.get_item_key_ui_chat_send_channel_kv(item_key, "key")
```

---

## get_ability_key_ui_chat_send_channel_kv

method in GameAPI

- 描述

    获取技能编号UI_CHAT_SEND_CHANNEL键值对

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

local result = GameAPI.get_ability_key_ui_chat_send_channel_kv(ability_key, "key")
```

---

## get_modifier_key_ui_chat_send_channel_kv

method in GameAPI

- 描述

    获取魔法效果特效编号UI_CHAT_SEND_CHANNEL键值对

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

local result = GameAPI.get_modifier_key_ui_chat_send_channel_kv(modifier_key, "key")
```

---

## get_projectile_key_ui_chat_send_channel_kv

method in GameAPI

- 描述

    获取特效编号UI_CHAT_SEND_CHANNEL键值对

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

local result = GameAPI.get_projectile_key_ui_chat_send_channel_kv(projectile_key, "key")
```

---

## get_destructible_key_ui_chat_send_channel_kv

method in GameAPI

- 描述

    获取可破坏物编号UI_CHAT_SEND_CHANNEL键值对

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

local result = GameAPI.get_destructible_key_ui_chat_send_channel_kv(destructible_key, "key")
```

---

## get_tech_key_ui_chat_send_channel_kv

method in GameAPI

- 描述

    获取科技编号UI_CHAT_SEND_CHANNEL键值对

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

local result = GameAPI.get_tech_key_ui_chat_send_channel_kv(tech_key, "key")
```

---

## get_icon_id_ui_chat_send_channel_kv

method in GameAPI

- 描述

    获取图片UI_CHAT_SEND_CHANNEL键值对

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
local result = GameAPI.get_icon_id_ui_chat_send_channel_kv(1, "key")
```

---

## get_physics_entity_key_ui_chat_send_channel_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型UI_CHAT_SEND_CHANNEL键值对

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
local result = GameAPI.get_physics_entity_key_ui_chat_send_channel_kv(1, "key")
```

---

## get_kv_pair_value_ui_chat_send_channel

method in GameAPI

- 描述

    获取UI_CHAT_SEND_CHANNEL键值对

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

local result = GameAPI.get_kv_pair_value_ui_chat_send_channel(kvbase, "key")
```

---

## get_unit_key_ui_chat_recv_channel_kv

method in GameAPI

- 描述

    获取单位编号UI_CHAT_RECV_CHANNEL键值对

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

local result = GameAPI.get_unit_key_ui_chat_recv_channel_kv(unit_key, "key")
```

---

## get_item_key_ui_chat_recv_channel_kv

method in GameAPI

- 描述

    获取物品编号UI_CHAT_RECV_CHANNEL键值对

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

local result = GameAPI.get_item_key_ui_chat_recv_channel_kv(item_key, "key")
```

---

## get_ability_key_ui_chat_recv_channel_kv

method in GameAPI

- 描述

    获取技能编号UI_CHAT_RECV_CHANNEL键值对

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

local result = GameAPI.get_ability_key_ui_chat_recv_channel_kv(ability_key, "key")
```

---

## get_modifier_key_ui_chat_recv_channel_kv

method in GameAPI

- 描述

    获取魔法效果特效编号UI_CHAT_RECV_CHANNEL键值对

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

local result = GameAPI.get_modifier_key_ui_chat_recv_channel_kv(modifier_key, "key")
```

---

## get_projectile_key_ui_chat_recv_channel_kv

method in GameAPI

- 描述

    获取特效编号UI_CHAT_RECV_CHANNEL键值对

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

local result = GameAPI.get_projectile_key_ui_chat_recv_channel_kv(projectile_key, "key")
```

---

## get_destructible_key_ui_chat_recv_channel_kv

method in GameAPI

- 描述

    获取可破坏物编号UI_CHAT_RECV_CHANNEL键值对

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

local result = GameAPI.get_destructible_key_ui_chat_recv_channel_kv(destructible_key, "key")
```

---

## get_tech_key_ui_chat_recv_channel_kv

method in GameAPI

- 描述

    获取科技编号UI_CHAT_RECV_CHANNEL键值对

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

local result = GameAPI.get_tech_key_ui_chat_recv_channel_kv(tech_key, "key")
```

---

## get_icon_id_ui_chat_recv_channel_kv

method in GameAPI

- 描述

    获取图片UI_CHAT_RECV_CHANNEL键值对

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
local result = GameAPI.get_icon_id_ui_chat_recv_channel_kv(1, "key")
```

---

## get_physics_entity_key_ui_chat_recv_channel_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型UI_CHAT_RECV_CHANNEL键值对

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
local result = GameAPI.get_physics_entity_key_ui_chat_recv_channel_kv(1, "key")
```

---

## get_kv_pair_value_ui_chat_recv_channel

method in GameAPI

- 描述

    获取UI_CHAT_RECV_CHANNEL键值对

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

local result = GameAPI.get_kv_pair_value_ui_chat_recv_channel(kvbase, "key")
```

---

## get_unit_key_ui_anim_play_mode_kv

method in GameAPI

- 描述

    获取单位编号UI_ANIM_PLAY_MODE键值对

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

local result = GameAPI.get_unit_key_ui_anim_play_mode_kv(unit_key, "key")
```

---

## get_item_key_ui_anim_play_mode_kv

method in GameAPI

- 描述

    获取物品编号UI_ANIM_PLAY_MODE键值对

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

local result = GameAPI.get_item_key_ui_anim_play_mode_kv(item_key, "key")
```

---

## get_ability_key_ui_anim_play_mode_kv

method in GameAPI

- 描述

    获取技能编号UI_ANIM_PLAY_MODE键值对

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

local result = GameAPI.get_ability_key_ui_anim_play_mode_kv(ability_key, "key")
```

---
