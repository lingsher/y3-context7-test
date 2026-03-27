---
sidebarDepth: 1
---
# GameAPI (Part 5)

# 索引

Y3 编辑器 GameAPI 接口集合（第 5 部分），包含游戏核心功能。

---

| 接口 | 描述 |
| --- | --- |
| [set_cur_damage_is_miss](#set_cur_damage_is_miss) | 设置当前是否闪避 |
| [set_cur_cure_value](#set_cur_cure_value) | 设置当前治疗的数值 |
| [get_cur_damage_is_critical](#get_cur_damage_is_critical) | 获取当次攻击是否暴击 |
| [set_cur_damage_is_critical](#set_cur_damage_is_critical) | 设置当前是否暴击 |
| [assign_behavior_tree](#assign_behavior_tree) | 启动行为树 |
| [stop_behavior_tree](#stop_behavior_tree) | 停止一棵行为树 |
| [stop_all_behavior_tree](#stop_all_behavior_tree) | 停止所有行为树 |
| [run_behavior_tree_once](#run_behavior_tree_once) | 运行一次行为树 |
| [unit_key_del_kv](#unit_key_del_kv) | 预设库单位删除键值对 |
| [ability_key_del_kv](#ability_key_del_kv) | 预设库技能删除键值对 |
| [item_key_del_kv](#item_key_del_kv) | 预设库物品删除键值对 |
| [set_item_buy_price](#set_item_buy_price) | 设置物品商品售价 |
| [set_item_sell_price](#set_item_sell_price) | 设置物品商品出售资源获得 |
| [set_unit_buy_price](#set_unit_buy_price) | 设置单位商品售价 |
| [set_unit_sell_price](#set_unit_sell_price) | 设置单位商品出售资源获得 |
| [get_item_buy_price](#get_item_buy_price) | 获取物品商品售价 |
| [get_item_sell_price](#get_item_sell_price) | 获取物品商品出售资源获得 |
| [get_unit_buy_price](#get_unit_buy_price) | 获取单位商品售价 |
| [get_unit_sell_price](#get_unit_sell_price) | 获取单位商品出售资源获得 |
| [get_rec_center_point](#get_rec_center_point) | 返回矩形区域中心点 |
| [get_circle_center_point](#get_circle_center_point) | 返回圆形区域中心点 |
| [get_random_point_in_rec_area](#get_random_point_in_rec_area) | 返回矩形区域内随机点 |
| [get_random_point_in_circular_area](#get_random_point_in_circular_area) | 返回圆形区域内随机点 |
| [get_random_point_in_poly_area](#get_random_point_in_poly_area) | 返回多边形区域内随机点 |
| [get_cir_area_last_created](#get_cir_area_last_created) | 最近创建的圆型区域 |
| [get_road_point_list_by_res_id](#get_road_point_list_by_res_id) | 通过资源id返回路径 |
| [create_road_point_list](#create_road_point_list) | 在某点创建一条路径 |
| [remove_road_point_list](#remove_road_point_list) | 移除路径 |
| [add_road_point](#add_road_point) | 给路径添加点 |
| [remove_road_point](#remove_road_point) | 移除路径点 |
| [get_road_point_start_point](#get_road_point_start_point) | 获取路径的【起点】 |
| [get_road_point_end_point](#get_road_point_end_point) | 获取路径的【终点】 |
| [get_road_point_random_point](#get_road_point_random_point) | 获取路径的【随机点】 |
| [get_nearest_road_point_list_by_pos](#get_nearest_road_point_list_by_pos) | 获取某点的最近路径 |
| [get_road_point_list_by_offset](#get_road_point_list_by_offset) | 获取某路径偏移后的路径 |
| [get_road_point_list_loop](#get_road_point_list_loop) | 获取某路径循环n次后的路径 |
| [get_road_point_list_join](#get_road_point_list_join) | 获取两路径拼接后的路径 |
| [get_road_point_list_inversion](#get_road_point_list_inversion) | 获取某路径反转后的路径 |
| [get_road_point_num](#get_road_point_num) | 获取路径中点的数量 |
| [get_last_created_unit](#get_last_created_unit) | 最近创建单位实体 |
| [get_last_created_trigger](#get_last_created_trigger) | 最近创建子触发器 |
| [get_last_created_projectile](#get_last_created_projectile) | 最近创建投射物 |
| [get_unit_group_in_area](#get_unit_group_in_area) | 得到区域内的单位id列表 |
| [get_unit_group_belong_to_player_in_area](#get_unit_group_belong_to_player_in_area) | 获取区域内玩家所有单位id列表 |
| [get_item_group_in_area](#get_item_group_in_area) | 得到区域内的物品对象id列表 |
| [get_all_items_in_shapes](#get_all_items_in_shapes) | 获取指定形状内的所有物品 |
| [send_ui_global_event_with_info_dict](#send_ui_global_event_with_info_dict) | 向ui发送附带dict的事件 |
| [add_unit_to_group](#add_unit_to_group) | 添加单位到单位组 |
| [set_trigger_table_list_variable](#set_trigger_table_list_variable) | 批量设置全局触发器数组变量 |
| [set_trigger_str_list_by_split](#set_trigger_str_list_by_split) | 通过分割字符串设置字符串数组 |
| [create_trigger_list_variable](#create_trigger_list_variable) | 创建全局触发器数组变量 |
| [unit_key_has_tag](#unit_key_has_tag) | 单位编号是否拥有tag |
| [item_key_has_tag](#item_key_has_tag) | 物品编号是否拥有tag |
| [ability_key_has_tag](#ability_key_has_tag) | 技能编号是否拥有tag |
| [modifier_key_has_tag](#modifier_key_has_tag) | 效果编号是否拥有tag |
| [projectile_key_has_tag](#projectile_key_has_tag) | 投射物编号是否拥有tag |
| [dest_key_has_tag](#dest_key_has_tag) | 可破坏物编号是否拥有tag |
| [unit_is_exist](#unit_is_exist) | 单位实体是否存在 |
| [modifier_is_exist](#modifier_is_exist) | 效果实体是否存在 |
| [projectile_is_exist](#projectile_is_exist) | 投射物实体是否存在 |
| [ability_is_exist](#ability_is_exist) | 技能实体是否存在 |
| [destructible_is_exist](#destructible_is_exist) | 可破坏物是否存在 |
| [item_is_exist](#item_is_exist) | 图片是否存在 |
| [unit_group_is_exist](#unit_group_is_exist) | 单位组是否存在 |
| [role_group_is_exist](#role_group_is_exist) | 玩家组是否存在 |
| [sfx_is_exist](#sfx_is_exist) | 特效是否存在 |
| [point_is_exist](#point_is_exist) | 点是否存在 |
| [point_list_is_exist](#point_list_is_exist) | 路径是否存在 |
| [circle_area_is_exist](#circle_area_is_exist) | 圆形区域是否存在 |
| [rect_area_is_exist](#rect_area_is_exist) | 矩形区域是否存在 |
| [camera_is_exist](#camera_is_exist) | 镜头是否存在 |
| [get_ability_max_level](#get_ability_max_level) | 获取技能最大等级 |
| [random_list_from_list](#random_list_from_list) | 列表中返回随机整数个元素组成的列表 |
| [shake_phone](#shake_phone) | 震动设备 |
| [set_role_rank_score](#set_role_rank_score) | 为<玩家>输入排行榜<分数> |
| [unit_send_global_event_with_info](#unit_send_global_event_with_info) | 单位触发器向全局触发器发送事件, 附带信息 |
| [ability_send_global_event_with_info](#ability_send_global_event_with_info) | 技能触发器向全局触发器发送事件, 附带信息 |
| [modifier_send_global_event_with_info](#modifier_send_global_event_with_info) | 效果触发器向全局触发器发送事件, 附带信息 |
| [projectile_send_global_event_with_info](#projectile_send_global_event_with_info) | 投射物触发器向全局触发器发送事件, 附带信息 |
| [item_send_global_event_with_info](#item_send_global_event_with_info) | 物品触发器向全局触发器发送事件, 附带信息 |
| [get_player_nick_name](#get_player_nick_name) | 获取[玩家]的玩家昵称 |
| [get_player_full_nick_name](#get_player_full_nick_name) | 获取[玩家]的玩家全量昵称 |
| [get_player_plat_aid](#get_player_plat_aid) | 获取[玩家]的玩家aid |
| [get_player_icon](#get_player_icon) | 获取[玩家]的玩家图像 |
| [filter_unit_status](#filter_unit_status) | 筛选单位删除状态 |
| [open_charge_item_store_for_role](#open_charge_item_store_for_role) | 为玩家打开收费道具商店 |
| [get_cur_game_time](#get_cur_game_time) | 当前游戏运行时间 |
| [can_point_reach_point](#can_point_reach_point) | 检查点到点是否联通 |
| [unit_can_collide_with_point](#unit_can_collide_with_point) | 检测点是否和单位碰撞 |
| [api_get_ability_by_seq](#api_get_ability_by_seq) | 通过技能序列号获取技能 |
| [api_get_ability_by_unit_and_seq](#api_get_ability_by_unit_and_seq) | 通过单位编号+技能序列号获取技能 |
| [get_damage_statistic_rank_unit](#get_damage_statistic_rank_unit) | 获取【单位组】中伤害排名【整数】的单位实体 |
| [get_select_circle_scale](#get_select_circle_scale) | 获取选择圈缩放 |
| [delete_model_entity](#delete_model_entity) | 删除模型 |
| [create_model_on_point](#create_model_on_point) | 创建展示模型，面向点，朝向实数 |
| [create_model_in_scene](#create_model_in_scene) | 创建模型 |
| [destroy_model_in_scene](#destroy_model_in_scene) | 销毁模型 |
| [get_item_key_str_attr](#get_item_key_str_attr) | 返回指定物品名字的字符串属性值 |
| [role_force_quit](#role_force_quit) | 强制踢出玩家 |
| [set_rect_vision_visibility](#set_rect_vision_visibility) | 设置矩形区域内视野情况 |
| [set_fog_state](#set_fog_state) | 设置区域内视野情况 |
| [set_circle_vision_visibility](#set_circle_vision_visibility) | 设置圆形区域内视野情况 |
| [set_poly_vision_visibility](#set_poly_vision_visibility) | 设置多边形区域内视野情况 |
| [create_random_pool](#create_random_pool) | 创建随机池 |
| [set_random_pool_value](#set_random_pool_value) | 设置随机池指定整数权重 |
| [increase_random_pool_value](#increase_random_pool_value) | 随机池增加指定整数权重 |
| [remove_random_pool_value](#remove_random_pool_value) | 随机池移除指定整数 |
| [get_bitrary_random_pool_value](#get_bitrary_random_pool_value) | 从随机池中获取一个随机整数 |
| [get_random_pool_probability](#get_random_pool_probability) | 获取随机池中指定整数的权重概率 |
| [get_random_pool_all_weight](#get_random_pool_all_weight) | 获取随机池中指定整数的权重概率 |
| [get_random_pool_size](#get_random_pool_size) | 获取随机池中的整数数量 |
| [copy_random_pool](#copy_random_pool) | 复制随机池 |
| [api_get_attr_growth](#api_get_attr_growth) | 成长属性 |
| [api_set_attr_growth](#api_set_attr_growth) | 设置成长属性 |
| [get_all_random_pool_value](#get_all_random_pool_value) | 获取某个随机池的列表 |
| [get_random_pool_pointed_weight](#get_random_pool_pointed_weight) | 获取某个随机池中指定整数的权重 |
| [get_text_config](#get_text_config) | 翻译字符串 |
| [send_custom_event](#send_custom_event) | 发送触发器自定义事件 |
| [get_icon_id](#get_icon_id) | 获取icon图标的图片id |
| [get_icon_id_by_ability_type](#get_icon_id_by_ability_type) | 获取技能icon图标的图片id |
| [get_icon_id_by_item_type](#get_icon_id_by_item_type) | 获取物品icon图标的图片id |
| [get_icon_id_by_unit_type](#get_icon_id_by_unit_type) | 获取单位icon图标的图片id |
| [get_icon_id_by_buff_type](#get_icon_id_by_buff_type) | 获取魔法效果icon图标的图片id |
| [is_show_on_ui_by_buff_type](#is_show_on_ui_by_buff_type) | 获取魔法效果类型图标的可见性 |
| [create_harm_text](#create_harm_text) | 生成漂浮文字 |
| [player_key_is_pressed](#player_key_is_pressed) | 玩家是否按下按键 |
| [get_player_pointing_pos](#get_player_pointing_pos) | 玩家鼠标位置 |
| [get_player_ui_pos_x](#get_player_ui_pos_x) | 玩家鼠标屏幕位置X |
| [get_player_ui_pos_y](#get_player_ui_pos_y) | 玩家鼠标屏幕位置Y |
| [get_player_camera_direction](#get_player_camera_direction) | 玩家摄像机朝向 |
| [get_camera_center_raycast](#get_camera_center_raycast) | 玩家摄像机中心射线检测 |
| [get_role_ui_x_per](#get_role_ui_x_per) | 玩家鼠标屏幕位置X的窗口占比 |
| [get_role_ui_y_per](#get_role_ui_y_per) | 玩家鼠标屏幕位置Y的窗口占比 |
| [get_unit_name_by_type](#get_unit_name_by_type) | 返回指定单位类型的名称 |
| [get_unit_desc_by_type](#get_unit_desc_by_type) | 返回指定单位类型的描述 |
| [get_role_attr_by_unit_type](#get_role_attr_by_unit_type) | 获取单位类型建造资源消耗属性(玩家属性) |
| [get_dest_name_by_type](#get_dest_name_by_type) | 返回指定可破坏物类型的名称 |
| [get_dest_desc_by_type](#get_dest_desc_by_type) | 返回指定可破坏物类型的描述 |
| [get_projectile_name_by_type](#get_projectile_name_by_type) | 返回指定投射物类型的名称 |
| [get_projectile_desc_by_type](#get_projectile_desc_by_type) | 返回指定投射物类型的描述 |
| [get_item_desc_by_type](#get_item_desc_by_type) | 返回指定物品类型的描述 |
| [get_ability_desc_by_type](#get_ability_desc_by_type) | 返回指定技能类型的描述 |
| [get_ability_name_by_type](#get_ability_name_by_type) | 返回指定技能类型的名称 |
| [get_tech_name_by_type](#get_tech_name_by_type) | 返回指定科技类型的名称 |
| [get_tech_desc_by_type](#get_tech_desc_by_type) | 返回指定科技类型的描述 |
| [get_modifier_name_by_type](#get_modifier_name_by_type) | 返回指定魔法效果类型的名称 |
| [get_modifier_desc_by_type](#get_modifier_desc_by_type) | 返回指定魔法效果类型的描述 |
| [get_item_name_by_type](#get_item_name_by_type) | 返回指定物品类型的名字 |
| [block_global_key_event](#block_global_key_event) | 屏蔽全局键盘事件 |
| [block_global_mouse_event](#block_global_mouse_event) | 屏蔽全局鼠标事件 |
| [block_trigger_key_event](#block_trigger_key_event) | 屏蔽触发器键盘事件 |
| [block_trigger_mouse_event](#block_trigger_mouse_event) | 屏蔽触发器鼠标事件 |
| [get_role_res_icon](#get_role_res_icon) | 获取玩家属性Icon |
| [get_role_res_name](#get_role_res_name) | 获取玩家属性名称 |
| [draw_grid_polyline](#draw_grid_polyline) | (调试)绘制网格线 |
| [draw_polyline](#draw_polyline) | (调试)绘线 |
| [draw_box](#draw_box) | (调试)绘制矩形 |
| [hide_all_rect](#hide_all_rect) | (调试)隐藏所有矩形 |
| [clear_grid_polyline](#clear_grid_polyline) | (调试)清除调试绘线 |
| [set_billboard_font_size](#set_billboard_font_size) | (调试)设置billboard字体大小 |
| [set_mouse_click_control_move](#set_mouse_click_control_move) | 设置鼠标关闭右键点击移动 |
| [iter_role_res](#iter_role_res) | 遍历所有玩家的资源属性 |
| [create_scene_node_on_point](#create_scene_node_on_point) | 创建场景点并绑定UI到点 |
| [create_scene_node_on_unit](#create_scene_node_on_unit) | 创建场景点并绑定UI到单位 |
| [create_scene_node_on_3d](#create_scene_node_on_3d) | 创建场景点并绑定UI到三维坐标 |
| [create_scene_node_on_rigid_body](#create_scene_node_on_rigid_body) | 创建场景界面到刚体 |
| [set_scene_node_visible_distance](#set_scene_node_visible_distance) | 设置场景点对玩家的可见距离 |
| [delete_scene_node](#delete_scene_node) | 删除场景点 |
| [unit_key_to_str](#unit_key_to_str) | 单位类型转字符串 |
| [str_to_unit_key](#str_to_unit_key) | 字符串转单位类型 |
| [item_key_to_str](#item_key_to_str) | 物品类型转字符串 |
| [str_to_item_key](#str_to_item_key) | 字符串转物品类型 |
| [ability_key_to_str](#ability_key_to_str) | 技能类型转字符串 |
| [str_to_ability_key](#str_to_ability_key) | 字符串转技能类型 |
| [dest_key_to_str](#dest_key_to_str) | 可破坏物类型转字符串 |
| [str_to_dest_key](#str_to_dest_key) | 字符串转可破坏物类型 |
| [project_key_to_str](#project_key_to_str) | 投射物类型转字符串 |
| [str_to_project_key](#str_to_project_key) | 字符串转投射物类型 |
| [tech_key_to_str](#tech_key_to_str) | 科技类型转字符串 |
| [str_to_tech_key](#str_to_tech_key) | 字符串转科技类型 |
| [model_entity_to_str](#model_entity_to_str) | 模型实体转字符串 |
| [model_key_to_str](#model_key_to_str) | 模型类型转字符串 |
| [str_to_model_key](#str_to_model_key) | 字符串转模型类型 |
| [modifier_key_to_str](#modifier_key_to_str) | 魔法效果类型转字符串 |
| [str_to_modifier_key](#str_to_modifier_key) | 字符串转魔法效果类型 |
| [store_key_to_str](#store_key_to_str) | 平台道具类型转字符串 |
| [str_to_store_key](#str_to_store_key) | 字符串转平台道具类型 |
| [camera_to_str](#camera_to_str) | 镜头转字符串 |
| [ui_comp_to_str](#ui_comp_to_str) | 界面组件转字符串 |
| [role_res_to_str](#role_res_to_str) | 玩家属性转字符串 |
| [str_to_role_res](#str_to_role_res) | 字符串转玩家属性 |
| [unit_attr_to_str](#unit_attr_to_str) | 单位属性转字符串 |
| [str_to_unit_attr](#str_to_unit_attr) | 字符串转单位属性 |
| [str_to_camp](#str_to_camp) | 字符串转阵营对象 |
| [get_model_key_of_dest_key](#get_model_key_of_dest_key) | 获取可破坏物类型的模型 |
| [set_smart_cast_ability](#set_smart_cast_ability) | 打开/关闭自动施法 |
| [set_preview_common_atk_range](#set_preview_common_atk_range) | 设置{玩家}的普攻预览状态为{开启/关闭} |
| [set_smart_cast_with_pointer](#set_smart_cast_with_pointer) | 是否让{玩家}的智能施法使用指示器 |
| [set_shortcut](#set_shortcut) | 设置快捷键 |
| [get_shortcut](#get_shortcut) | 获取快捷键 |
| [set_simple_cast](#set_simple_cast) | 设置智能施法 |
| [get_simple_cast](#get_simple_cast) | 获取智能施法 |
| [get_client_simple_cast](#get_client_simple_cast) | 获取客户端智能施法 |
| [save_client_setting](#save_client_setting) | 保存编辑器局内设置 |
| [save_game_setting](#save_game_setting) | 保存玩家设置 |
| [get_client_role](#get_client_role) | 获取本地玩家 |
| [set_mouse_move_camera_mode](#set_mouse_move_camera_mode) | 设置鼠标移动镜头模式 |
| [set_mouse_move_camera_speed](#set_mouse_move_camera_speed) | 设置鼠标移动镜头速度 |
| [set_key_move_camera_speed](#set_key_move_camera_speed) | 设置键盘移动镜头速度 |
| [change_highlight_unit_of_role](#change_highlight_unit_of_role) | 修改玩家主控单位 |
| [set_highlight_unit_of_role](#set_highlight_unit_of_role) | 玩家主控单位 |
| [get_highlight_unit_of_role](#get_highlight_unit_of_role) | 获取玩家主控单位 |
| [api_get_start_mode](#api_get_start_mode) | 获取本局游戏环境 |
| [api_check_attack_type](#api_check_attack_type) | 攻击类型判断 |
| [api_check_armor_type](#api_check_armor_type) | 护甲类型判断 |
| [set_weahter_enable](#set_weahter_enable) | 天气系统开关 |
| [get_role_platform_icon](#get_role_platform_icon) | 获取玩家平台头像 |
| [get_role_platform_model](#get_role_platform_model) | 获取玩家平台模型 |
| [set_camera_distance_max](#set_camera_distance_max) | 设置相机最大视距 |
| [exit_game](#exit_game) | 退出游戏 |
| [create_physics_projectile_in_scene](#create_physics_projectile_in_scene) | 创建一个物理投射物 |
| [api_get_unit_type_model](#api_get_unit_type_model) | 获取单位类型的模型 |
| [api_get_unit_type_category](#api_get_unit_type_category) | 获取单位类型的分类 |
| [api_get_role_name_of_rank](#api_get_role_name_of_rank) | 玩家本地图平台等级排行榜玩家名称 |
| [api_get_role_level_of_rank](#api_get_role_level_of_rank) | 玩家本地图平台等级排行榜玩家等级 |
| [iter_compose_item_res_of_item_name](#iter_compose_item_res_of_item_name) | 遍历物品类型的物品合成材料 |
| [iter_compose_role_attr_of_item_name](#iter_compose_role_attr_of_item_name) | 遍历物品类型的玩家合成材料 |
| [get_random_role_in_role_group](#get_random_role_in_role_group) | 玩家组内随机一个玩家 |
| [get_first_role_in_group](#get_first_role_in_group) | 玩家组内第一个玩家 |
| [get_last_role_in_group](#get_last_role_in_group) | 玩家组内最后一个玩家 |
| [iter_unit_attr_of_item_name](#iter_unit_attr_of_item_name) | 遍历物品类型的单位属性 |
| [iter_unit_attr_of_item](#iter_unit_attr_of_item) | 遍历物品的单位属性 |
| [set_billboard_picture](#set_billboard_picture) | 设置血条图片 |
| [set_billboard_text](#set_billboard_text) | 设置血条文本 |
| [set_billboard_visible](#set_billboard_visible) | 设置血条可见性 |
| [set_billboard_progress](#set_billboard_progress) | 设置血条进度 |
| [lobby_exit_game](#lobby_exit_game) | 玩家完全退出游戏（大厅完全退出游戏） |
| [set_prefab_key_boolean_kv](#set_prefab_key_boolean_kv) | 预设库 添加BOOLEAN键值对 |
| [set_prefab_key_integer_kv](#set_prefab_key_integer_kv) | 预设库 添加INTEGER键值对 |
| [set_prefab_key_float_kv](#set_prefab_key_float_kv) | 预设库 添加FLOAT键值对 |
| [set_prefab_key_string_kv](#set_prefab_key_string_kv) | 预设库 添加STRING键值对 |
| [set_prefab_key_ui_comp_kv](#set_prefab_key_ui_comp_kv) | 预设库 添加UI_COMP键值对 |
| [set_prefab_key_ui_comp_type_kv](#set_prefab_key_ui_comp_type_kv) | 预设库 添加UI_COMP_TYPE键值对 |
| [set_prefab_key_ui_comp_event_type_kv](#set_prefab_key_ui_comp_event_type_kv) | 预设库 添加UI_COMP_EVENT_TYPE键值对 |
| [set_prefab_key_ui_comp_attr_kv](#set_prefab_key_ui_comp_attr_kv) | 预设库 添加UI_COMP_ATTR键值对 |
| [set_prefab_key_ui_comp_align_type_kv](#set_prefab_key_ui_comp_align_type_kv) | 预设库 添加UI_COMP_ALIGN_TYPE键值对 |
| [set_prefab_key_ui_prefab_kv](#set_prefab_key_ui_prefab_kv) | 预设库 添加UI_PREFAB键值对 |
| [set_prefab_key_ui_prefab_instance_kv](#set_prefab_key_ui_prefab_instance_kv) | 预设库 添加UI_PREFAB_INSTANCE键值对 |
| [set_prefab_key_ui_prefab_ins_uid_kv](#set_prefab_key_ui_prefab_ins_uid_kv) | 预设库 添加UI_PREFAB_INS_UID键值对 |
| [set_prefab_key_ui_direction_kv](#set_prefab_key_ui_direction_kv) | 预设库 添加UI_DIRECTION键值对 |
| [set_prefab_key_ui_model_camera_mod_kv](#set_prefab_key_ui_model_camera_mod_kv) | 预设库 添加UI_MODEL_CAMERA_MOD键值对 |
| [set_prefab_key_ui_btn_status_kv](#set_prefab_key_ui_btn_status_kv) | 预设库 添加UI_BTN_STATUS键值对 |
| [set_prefab_key_ui_scrollview_type_kv](#set_prefab_key_ui_scrollview_type_kv) | 预设库 添加UI_SCROLLVIEW_TYPE键值对 |
| [set_prefab_key_ui_anim_kv](#set_prefab_key_ui_anim_kv) | 预设库 添加UI_ANIM键值对 |
| [set_prefab_key_ui_anim_curve_kv](#set_prefab_key_ui_anim_curve_kv) | 预设库 添加UI_ANIM_CURVE键值对 |
| [set_prefab_key_audio_channel_kv](#set_prefab_key_audio_channel_kv) | 预设库 添加AUDIO_CHANNEL键值对 |
| [set_prefab_key_unit_entity_kv](#set_prefab_key_unit_entity_kv) | 预设库 添加UNIT_ENTITY键值对 |
| [set_prefab_key_unit_group_kv](#set_prefab_key_unit_group_kv) | 预设库 添加UNIT_GROUP键值对 |
| [set_prefab_key_unit_name_kv](#set_prefab_key_unit_name_kv) | 预设库 添加UNIT_NAME键值对 |
| [set_prefab_key_unit_name_pool_kv](#set_prefab_key_unit_name_pool_kv) | 预设库 添加UNIT_NAME_POOL键值对 |
| [set_prefab_key_unit_write_attribute_kv](#set_prefab_key_unit_write_attribute_kv) | 预设库 添加UNIT_WRITE_ATTRIBUTE键值对 |
| [set_prefab_key_attr_element_kv](#set_prefab_key_attr_element_kv) | 预设库 添加ATTR_ELEMENT键值对 |
| [set_prefab_key_attr_element_read_kv](#set_prefab_key_attr_element_read_kv) | 预设库 添加ATTR_ELEMENT_READ键值对 |
| [set_prefab_key_mover_entity_kv](#set_prefab_key_mover_entity_kv) | 预设库 添加MOVER_ENTITY键值对 |
| [set_prefab_key_image_quality_kv](#set_prefab_key_image_quality_kv) | 预设库 添加IMAGE_QUALITY键值对 |
| [set_prefab_key_window_type_setting_kv](#set_prefab_key_window_type_setting_kv) | 预设库 添加WINDOW_TYPE_SETTING键值对 |
| [set_prefab_key_item_entity_kv](#set_prefab_key_item_entity_kv) | 预设库 添加ITEM_ENTITY键值对 |
| [set_prefab_key_item_group_kv](#set_prefab_key_item_group_kv) | 预设库 添加ITEM_GROUP键值对 |
| [set_prefab_key_item_name_kv](#set_prefab_key_item_name_kv) | 预设库 添加ITEM_NAME键值对 |
| [set_prefab_key_ability_kv](#set_prefab_key_ability_kv) | 预设库 添加ABILITY键值对 |
| [set_prefab_key_ability_type_kv](#set_prefab_key_ability_type_kv) | 预设库 添加ABILITY_TYPE键值对 |
| [set_prefab_key_ability_cast_type_kv](#set_prefab_key_ability_cast_type_kv) | 预设库 添加ABILITY_CAST_TYPE键值对 |
| [set_prefab_key_ability_name_kv](#set_prefab_key_ability_name_kv) | 预设库 添加ABILITY_NAME键值对 |
| [set_prefab_key_skill_pointer_type_kv](#set_prefab_key_skill_pointer_type_kv) | 预设库 添加SKILL_POINTER_TYPE键值对 |
| [set_prefab_key_modifier_entity_kv](#set_prefab_key_modifier_entity_kv) | 预设库 添加MODIFIER_ENTITY键值对 |
| [set_prefab_key_modifier_type_kv](#set_prefab_key_modifier_type_kv) | 预设库 添加MODIFIER_TYPE键值对 |
| [set_prefab_key_modifier_effect_type_kv](#set_prefab_key_modifier_effect_type_kv) | 预设库 添加MODIFIER_EFFECT_TYPE键值对 |
| [set_prefab_key_modifier_kv](#set_prefab_key_modifier_kv) | 预设库 添加MODIFIER键值对 |
| [set_prefab_key_projectile_kv](#set_prefab_key_projectile_kv) | 预设库 添加PROJECTILE键值对 |
| [set_prefab_key_projectile_entity_kv](#set_prefab_key_projectile_entity_kv) | 预设库 添加PROJECTILE_ENTITY键值对 |
| [set_prefab_key_projectile_group_kv](#set_prefab_key_projectile_group_kv) | 预设库 添加PROJECTILE_GROUP键值对 |
| [set_prefab_key_destructible_entity_kv](#set_prefab_key_destructible_entity_kv) | 预设库 添加DESTRUCTIBLE_ENTITY键值对 |
| [set_prefab_key_destructible_name_kv](#set_prefab_key_destructible_name_kv) | 预设库 添加DESTRUCTIBLE_NAME键值对 |
| [set_prefab_key_sound_entity_kv](#set_prefab_key_sound_entity_kv) | 预设库 添加SOUND_ENTITY键值对 |
| [set_prefab_key_audio_key_kv](#set_prefab_key_audio_key_kv) | 预设库 添加AUDIO_KEY键值对 |
| [set_prefab_key_game_mode_kv](#set_prefab_key_game_mode_kv) | 预设库 添加GAME_MODE键值对 |
| [set_prefab_key_player_kv](#set_prefab_key_player_kv) | 预设库 添加PLAYER键值对 |
| [set_prefab_key_player_group_kv](#set_prefab_key_player_group_kv) | 预设库 添加PLAYER_GROUP键值对 |
| [set_prefab_key_role_res_key_kv](#set_prefab_key_role_res_key_kv) | 预设库 添加ROLE_RES_KEY键值对 |
| [set_prefab_key_role_status_kv](#set_prefab_key_role_status_kv) | 预设库 添加ROLE_STATUS键值对 |
| [set_prefab_key_role_type_kv](#set_prefab_key_role_type_kv) | 预设库 添加ROLE_TYPE键值对 |
| [set_prefab_key_role_relation_kv](#set_prefab_key_role_relation_kv) | 预设库 添加ROLE_RELATION键值对 |
| [set_prefab_key_team_kv](#set_prefab_key_team_kv) | 预设库 添加TEAM键值对 |
| [set_prefab_key_point_kv](#set_prefab_key_point_kv) | 预设库 添加POINT键值对 |
| [set_prefab_key_vector3_kv](#set_prefab_key_vector3_kv) | 预设库 添加VECTOR3键值对 |
| [set_prefab_key_rotation_kv](#set_prefab_key_rotation_kv) | 预设库 添加ROTATION键值对 |
| [set_prefab_key_point_list_kv](#set_prefab_key_point_list_kv) | 预设库 添加POINT_LIST键值对 |
| [set_prefab_key_rectangle_kv](#set_prefab_key_rectangle_kv) | 预设库 添加RECTANGLE键值对 |
| [set_prefab_key_round_area_kv](#set_prefab_key_round_area_kv) | 预设库 添加ROUND_AREA键值对 |
| [set_prefab_key_polygon_kv](#set_prefab_key_polygon_kv) | 预设库 添加POLYGON键值对 |
| [set_prefab_key_camera_kv](#set_prefab_key_camera_kv) | 预设库 添加CAMERA键值对 |
| [set_prefab_key_camline_kv](#set_prefab_key_camline_kv) | 预设库 添加CAMLINE键值对 |
| [set_prefab_key_point_light_kv](#set_prefab_key_point_light_kv) | 预设库 添加POINT_LIGHT键值对 |
| [set_prefab_key_spot_light_kv](#set_prefab_key_spot_light_kv) | 预设库 添加SPOT_LIGHT键值对 |
| [set_prefab_key_fog_kv](#set_prefab_key_fog_kv) | 预设库 添加FOG键值对 |
| [set_prefab_key_scene_sound_kv](#set_prefab_key_scene_sound_kv) | 预设库 添加SCENE_SOUND键值对 |
| [set_prefab_key_model_kv](#set_prefab_key_model_kv) | 预设库 添加MODEL键值对 |
| [set_prefab_key_sfx_entity_kv](#set_prefab_key_sfx_entity_kv) | 预设库 添加SFX_ENTITY键值对 |
| [set_prefab_key_sfx_key_kv](#set_prefab_key_sfx_key_kv) | 预设库 添加SFX_KEY键值对 |
| [set_prefab_key_link_sfx_entity_kv](#set_prefab_key_link_sfx_entity_kv) | 预设库 添加LINK_SFX_ENTITY键值对 |
| [set_prefab_key_link_sfx_key_kv](#set_prefab_key_link_sfx_key_kv) | 预设库 添加LINK_SFX_KEY键值对 |
| [set_prefab_key_cursor_key_kv](#set_prefab_key_cursor_key_kv) | 预设库 添加CURSOR_KEY键值对 |
| [set_prefab_key_angle_kv](#set_prefab_key_angle_kv) | 预设库 添加ANGLE键值对 |
| [set_prefab_key_texture_kv](#set_prefab_key_texture_kv) | 预设库 添加TEXTURE键值对 |
| [set_prefab_key_sequence_kv](#set_prefab_key_sequence_kv) | 预设库 添加SEQUENCE键值对 |
| [set_prefab_key_physics_object_kv](#set_prefab_key_physics_object_kv) | 预设库 添加PHYSICS_OBJECT键值对 |
| [set_prefab_key_physics_entity_kv](#set_prefab_key_physics_entity_kv) | 预设库 添加PHYSICS_ENTITY键值对 |
| [set_prefab_key_physics_object_key_kv](#set_prefab_key_physics_object_key_kv) | 预设库 添加PHYSICS_OBJECT_KEY键值对 |
| [set_prefab_key_physics_entity_key_kv](#set_prefab_key_physics_entity_key_kv) | 预设库 添加PHYSICS_ENTITY_KEY键值对 |
| [set_prefab_key_rigid_body_kv](#set_prefab_key_rigid_body_kv) | 预设库 添加RIGID_BODY键值对 |
| [set_prefab_key_rigid_body_group_kv](#set_prefab_key_rigid_body_group_kv) | 预设库 添加RIGID_BODY_GROUP键值对 |
| [set_prefab_key_collider_kv](#set_prefab_key_collider_kv) | 预设库 添加COLLIDER键值对 |
| [set_prefab_key_joint_kv](#set_prefab_key_joint_kv) | 预设库 添加JOINT键值对 |
| [set_prefab_key_reaction_kv](#set_prefab_key_reaction_kv) | 预设库 添加REACTION键值对 |
| [set_prefab_key_reaction_group_kv](#set_prefab_key_reaction_group_kv) | 预设库 添加REACTION_GROUP键值对 |
| [set_prefab_key_dynamic_trigger_instance_kv](#set_prefab_key_dynamic_trigger_instance_kv) | 预设库 添加DYNAMIC_TRIGGER_INSTANCE键值对 |
| [set_prefab_key_table_kv](#set_prefab_key_table_kv) | 预设库 添加TABLE键值对 |
| [set_prefab_key_random_pool_kv](#set_prefab_key_random_pool_kv) | 预设库 添加RANDOM_POOL键值对 |
| [set_prefab_key_scene_ui_kv](#set_prefab_key_scene_ui_kv) | 预设库 添加SCENE_UI键值对 |
| [set_prefab_key_damage_type_kv](#set_prefab_key_damage_type_kv) | 预设库 添加DAMAGE_TYPE键值对 |
| [set_prefab_key_harm_text_type_new_kv](#set_prefab_key_harm_text_type_new_kv) | 预设库 添加HARM_TEXT_TYPE_NEW键值对 |
| [set_prefab_key_font_type_kv](#set_prefab_key_font_type_kv) | 预设库 添加FONT_TYPE键值对 |
| [set_prefab_key_jump_word_track_kv](#set_prefab_key_jump_word_track_kv) | 预设库 添加JUMP_WORD_TRACK键值对 |
| [set_prefab_key_new_timer_kv](#set_prefab_key_new_timer_kv) | 预设库 添加NEW_TIMER键值对 |
| [set_prefab_key_tech_key_kv](#set_prefab_key_tech_key_kv) | 预设库 添加TECH_KEY键值对 |
| [set_prefab_key_store_key_kv](#set_prefab_key_store_key_kv) | 预设库 添加STORE_KEY键值对 |
| [set_prefab_key_keyboard_key_kv](#set_prefab_key_keyboard_key_kv) | 预设库 添加KEYBOARD_KEY键值对 |
| [set_prefab_key_func_keyboard_key_kv](#set_prefab_key_func_keyboard_key_kv) | 预设库 添加FUNC_KEYBOARD_KEY键值对 |
| [set_prefab_key_mouse_key_kv](#set_prefab_key_mouse_key_kv) | 预设库 添加MOUSE_KEY键值对 |
| [set_prefab_key_mouse_wheel_kv](#set_prefab_key_mouse_wheel_kv) | 预设库 添加MOUSE_WHEEL键值对 |
| [set_prefab_key_post_effect_kv](#set_prefab_key_post_effect_kv) | 预设库 添加POST_EFFECT键值对 |
| [set_prefab_key_unit_type_kv](#set_prefab_key_unit_type_kv) | 预设库 添加UNIT_TYPE键值对 |
| [set_prefab_key_unit_command_type_kv](#set_prefab_key_unit_command_type_kv) | 预设库 添加UNIT_COMMAND_TYPE键值对 |
| [set_prefab_key_mini_map_color_type_kv](#set_prefab_key_mini_map_color_type_kv) | 预设库 添加MINI_MAP_COLOR_TYPE键值对 |
| [set_prefab_key_unit_behavior_kv](#set_prefab_key_unit_behavior_kv) | 预设库 添加UNIT_BEHAVIOR键值对 |
| [set_prefab_key_curved_path_kv](#set_prefab_key_curved_path_kv) | 预设库 添加CURVED_PATH键值对 |
| [set_prefab_key_curved_path_3d_kv](#set_prefab_key_curved_path_3d_kv) | 预设库 添加CURVED_PATH_3D键值对 |
| [has_prefab_boolean_kv](#has_prefab_boolean_kv) | 判断预设是否存在BOOLEAN键值对 |
| [has_prefab_integer_kv](#has_prefab_integer_kv) | 判断预设是否存在INTEGER键值对 |
| [has_prefab_float_kv](#has_prefab_float_kv) | 判断预设是否存在FLOAT键值对 |
| [has_prefab_string_kv](#has_prefab_string_kv) | 判断预设是否存在STRING键值对 |
| [has_prefab_ui_comp_kv](#has_prefab_ui_comp_kv) | 判断预设是否存在UI_COMP键值对 |
| [has_prefab_ui_comp_type_kv](#has_prefab_ui_comp_type_kv) | 判断预设是否存在UI_COMP_TYPE键值对 |
| [has_prefab_ui_comp_event_type_kv](#has_prefab_ui_comp_event_type_kv) | 判断预设是否存在UI_COMP_EVENT_TYPE键值对 |
| [has_prefab_ui_comp_attr_kv](#has_prefab_ui_comp_attr_kv) | 判断预设是否存在UI_COMP_ATTR键值对 |
| [has_prefab_ui_comp_align_type_kv](#has_prefab_ui_comp_align_type_kv) | 判断预设是否存在UI_COMP_ALIGN_TYPE键值对 |
| [has_prefab_ui_prefab_kv](#has_prefab_ui_prefab_kv) | 判断预设是否存在UI_PREFAB键值对 |
| [has_prefab_ui_prefab_instance_kv](#has_prefab_ui_prefab_instance_kv) | 判断预设是否存在UI_PREFAB_INSTANCE键值对 |
| [has_prefab_ui_prefab_ins_uid_kv](#has_prefab_ui_prefab_ins_uid_kv) | 判断预设是否存在UI_PREFAB_INS_UID键值对 |
| [has_prefab_ui_direction_kv](#has_prefab_ui_direction_kv) | 判断预设是否存在UI_DIRECTION键值对 |
| [has_prefab_ui_model_camera_mod_kv](#has_prefab_ui_model_camera_mod_kv) | 判断预设是否存在UI_MODEL_CAMERA_MOD键值对 |
| [has_prefab_ui_btn_status_kv](#has_prefab_ui_btn_status_kv) | 判断预设是否存在UI_BTN_STATUS键值对 |
| [has_prefab_ui_scrollview_type_kv](#has_prefab_ui_scrollview_type_kv) | 判断预设是否存在UI_SCROLLVIEW_TYPE键值对 |
| [has_prefab_ui_anim_kv](#has_prefab_ui_anim_kv) | 判断预设是否存在UI_ANIM键值对 |
| [has_prefab_ui_anim_curve_kv](#has_prefab_ui_anim_curve_kv) | 判断预设是否存在UI_ANIM_CURVE键值对 |
| [has_prefab_audio_channel_kv](#has_prefab_audio_channel_kv) | 判断预设是否存在AUDIO_CHANNEL键值对 |
| [has_prefab_unit_entity_kv](#has_prefab_unit_entity_kv) | 判断预设是否存在UNIT_ENTITY键值对 |
| [has_prefab_unit_group_kv](#has_prefab_unit_group_kv) | 判断预设是否存在UNIT_GROUP键值对 |
| [has_prefab_unit_name_kv](#has_prefab_unit_name_kv) | 判断预设是否存在UNIT_NAME键值对 |
| [has_prefab_unit_name_pool_kv](#has_prefab_unit_name_pool_kv) | 判断预设是否存在UNIT_NAME_POOL键值对 |
| [has_prefab_unit_write_attribute_kv](#has_prefab_unit_write_attribute_kv) | 判断预设是否存在UNIT_WRITE_ATTRIBUTE键值对 |
| [has_prefab_attr_element_kv](#has_prefab_attr_element_kv) | 判断预设是否存在ATTR_ELEMENT键值对 |
| [has_prefab_attr_element_read_kv](#has_prefab_attr_element_read_kv) | 判断预设是否存在ATTR_ELEMENT_READ键值对 |
| [has_prefab_mover_entity_kv](#has_prefab_mover_entity_kv) | 判断预设是否存在MOVER_ENTITY键值对 |
| [has_prefab_image_quality_kv](#has_prefab_image_quality_kv) | 判断预设是否存在IMAGE_QUALITY键值对 |
| [has_prefab_window_type_setting_kv](#has_prefab_window_type_setting_kv) | 判断预设是否存在WINDOW_TYPE_SETTING键值对 |
| [has_prefab_item_entity_kv](#has_prefab_item_entity_kv) | 判断预设是否存在ITEM_ENTITY键值对 |
| [has_prefab_item_group_kv](#has_prefab_item_group_kv) | 判断预设是否存在ITEM_GROUP键值对 |
| [has_prefab_item_name_kv](#has_prefab_item_name_kv) | 判断预设是否存在ITEM_NAME键值对 |
| [has_prefab_ability_kv](#has_prefab_ability_kv) | 判断预设是否存在ABILITY键值对 |
| [has_prefab_ability_type_kv](#has_prefab_ability_type_kv) | 判断预设是否存在ABILITY_TYPE键值对 |
| [has_prefab_ability_cast_type_kv](#has_prefab_ability_cast_type_kv) | 判断预设是否存在ABILITY_CAST_TYPE键值对 |
| [has_prefab_ability_name_kv](#has_prefab_ability_name_kv) | 判断预设是否存在ABILITY_NAME键值对 |
| [has_prefab_skill_pointer_type_kv](#has_prefab_skill_pointer_type_kv) | 判断预设是否存在SKILL_POINTER_TYPE键值对 |
| [has_prefab_modifier_entity_kv](#has_prefab_modifier_entity_kv) | 判断预设是否存在MODIFIER_ENTITY键值对 |
| [has_prefab_modifier_type_kv](#has_prefab_modifier_type_kv) | 判断预设是否存在MODIFIER_TYPE键值对 |
| [has_prefab_modifier_effect_type_kv](#has_prefab_modifier_effect_type_kv) | 判断预设是否存在MODIFIER_EFFECT_TYPE键值对 |
| [has_prefab_modifier_kv](#has_prefab_modifier_kv) | 判断预设是否存在MODIFIER键值对 |
| [has_prefab_projectile_kv](#has_prefab_projectile_kv) | 判断预设是否存在PROJECTILE键值对 |
| [has_prefab_projectile_entity_kv](#has_prefab_projectile_entity_kv) | 判断预设是否存在PROJECTILE_ENTITY键值对 |
| [has_prefab_projectile_group_kv](#has_prefab_projectile_group_kv) | 判断预设是否存在PROJECTILE_GROUP键值对 |
| [has_prefab_destructible_entity_kv](#has_prefab_destructible_entity_kv) | 判断预设是否存在DESTRUCTIBLE_ENTITY键值对 |
| [has_prefab_destructible_name_kv](#has_prefab_destructible_name_kv) | 判断预设是否存在DESTRUCTIBLE_NAME键值对 |
| [has_prefab_sound_entity_kv](#has_prefab_sound_entity_kv) | 判断预设是否存在SOUND_ENTITY键值对 |
| [has_prefab_audio_key_kv](#has_prefab_audio_key_kv) | 判断预设是否存在AUDIO_KEY键值对 |
| [has_prefab_game_mode_kv](#has_prefab_game_mode_kv) | 判断预设是否存在GAME_MODE键值对 |
| [has_prefab_player_kv](#has_prefab_player_kv) | 判断预设是否存在PLAYER键值对 |
| [has_prefab_player_group_kv](#has_prefab_player_group_kv) | 判断预设是否存在PLAYER_GROUP键值对 |
| [has_prefab_role_res_key_kv](#has_prefab_role_res_key_kv) | 判断预设是否存在ROLE_RES_KEY键值对 |
| [has_prefab_role_status_kv](#has_prefab_role_status_kv) | 判断预设是否存在ROLE_STATUS键值对 |
| [has_prefab_role_type_kv](#has_prefab_role_type_kv) | 判断预设是否存在ROLE_TYPE键值对 |
| [has_prefab_role_relation_kv](#has_prefab_role_relation_kv) | 判断预设是否存在ROLE_RELATION键值对 |
| [has_prefab_team_kv](#has_prefab_team_kv) | 判断预设是否存在TEAM键值对 |
| [has_prefab_point_kv](#has_prefab_point_kv) | 判断预设是否存在POINT键值对 |
| [has_prefab_vector3_kv](#has_prefab_vector3_kv) | 判断预设是否存在VECTOR3键值对 |
| [has_prefab_rotation_kv](#has_prefab_rotation_kv) | 判断预设是否存在ROTATION键值对 |
| [has_prefab_point_list_kv](#has_prefab_point_list_kv) | 判断预设是否存在POINT_LIST键值对 |
| [has_prefab_rectangle_kv](#has_prefab_rectangle_kv) | 判断预设是否存在RECTANGLE键值对 |
| [has_prefab_round_area_kv](#has_prefab_round_area_kv) | 判断预设是否存在ROUND_AREA键值对 |
| [has_prefab_polygon_kv](#has_prefab_polygon_kv) | 判断预设是否存在POLYGON键值对 |
| [has_prefab_camera_kv](#has_prefab_camera_kv) | 判断预设是否存在CAMERA键值对 |
| [has_prefab_camline_kv](#has_prefab_camline_kv) | 判断预设是否存在CAMLINE键值对 |
| [has_prefab_point_light_kv](#has_prefab_point_light_kv) | 判断预设是否存在POINT_LIGHT键值对 |
| [has_prefab_spot_light_kv](#has_prefab_spot_light_kv) | 判断预设是否存在SPOT_LIGHT键值对 |
| [has_prefab_fog_kv](#has_prefab_fog_kv) | 判断预设是否存在FOG键值对 |
| [has_prefab_scene_sound_kv](#has_prefab_scene_sound_kv) | 判断预设是否存在SCENE_SOUND键值对 |
| [has_prefab_model_kv](#has_prefab_model_kv) | 判断预设是否存在MODEL键值对 |
| [has_prefab_sfx_entity_kv](#has_prefab_sfx_entity_kv) | 判断预设是否存在SFX_ENTITY键值对 |
| [has_prefab_sfx_key_kv](#has_prefab_sfx_key_kv) | 判断预设是否存在SFX_KEY键值对 |
| [has_prefab_link_sfx_entity_kv](#has_prefab_link_sfx_entity_kv) | 判断预设是否存在LINK_SFX_ENTITY键值对 |
| [has_prefab_link_sfx_key_kv](#has_prefab_link_sfx_key_kv) | 判断预设是否存在LINK_SFX_KEY键值对 |
| [has_prefab_cursor_key_kv](#has_prefab_cursor_key_kv) | 判断预设是否存在CURSOR_KEY键值对 |
| [has_prefab_angle_kv](#has_prefab_angle_kv) | 判断预设是否存在ANGLE键值对 |
| [has_prefab_texture_kv](#has_prefab_texture_kv) | 判断预设是否存在TEXTURE键值对 |
| [has_prefab_sequence_kv](#has_prefab_sequence_kv) | 判断预设是否存在SEQUENCE键值对 |
| [has_prefab_physics_object_kv](#has_prefab_physics_object_kv) | 判断预设是否存在PHYSICS_OBJECT键值对 |
| [has_prefab_physics_entity_kv](#has_prefab_physics_entity_kv) | 判断预设是否存在PHYSICS_ENTITY键值对 |
| [has_prefab_physics_object_key_kv](#has_prefab_physics_object_key_kv) | 判断预设是否存在PHYSICS_OBJECT_KEY键值对 |
| [has_prefab_physics_entity_key_kv](#has_prefab_physics_entity_key_kv) | 判断预设是否存在PHYSICS_ENTITY_KEY键值对 |
| [has_prefab_rigid_body_kv](#has_prefab_rigid_body_kv) | 判断预设是否存在RIGID_BODY键值对 |
| [has_prefab_rigid_body_group_kv](#has_prefab_rigid_body_group_kv) | 判断预设是否存在RIGID_BODY_GROUP键值对 |
| [has_prefab_collider_kv](#has_prefab_collider_kv) | 判断预设是否存在COLLIDER键值对 |
| [has_prefab_joint_kv](#has_prefab_joint_kv) | 判断预设是否存在JOINT键值对 |
| [has_prefab_reaction_kv](#has_prefab_reaction_kv) | 判断预设是否存在REACTION键值对 |
| [has_prefab_reaction_group_kv](#has_prefab_reaction_group_kv) | 判断预设是否存在REACTION_GROUP键值对 |
| [has_prefab_dynamic_trigger_instance_kv](#has_prefab_dynamic_trigger_instance_kv) | 判断预设是否存在DYNAMIC_TRIGGER_INSTANCE键值对 |
| [has_prefab_table_kv](#has_prefab_table_kv) | 判断预设是否存在TABLE键值对 |
| [has_prefab_random_pool_kv](#has_prefab_random_pool_kv) | 判断预设是否存在RANDOM_POOL键值对 |
| [has_prefab_scene_ui_kv](#has_prefab_scene_ui_kv) | 判断预设是否存在SCENE_UI键值对 |
| [has_prefab_damage_type_kv](#has_prefab_damage_type_kv) | 判断预设是否存在DAMAGE_TYPE键值对 |
| [has_prefab_harm_text_type_new_kv](#has_prefab_harm_text_type_new_kv) | 判断预设是否存在HARM_TEXT_TYPE_NEW键值对 |
| [has_prefab_font_type_kv](#has_prefab_font_type_kv) | 判断预设是否存在FONT_TYPE键值对 |
| [has_prefab_jump_word_track_kv](#has_prefab_jump_word_track_kv) | 判断预设是否存在JUMP_WORD_TRACK键值对 |
| [has_prefab_new_timer_kv](#has_prefab_new_timer_kv) | 判断预设是否存在NEW_TIMER键值对 |
| [has_prefab_tech_key_kv](#has_prefab_tech_key_kv) | 判断预设是否存在TECH_KEY键值对 |
| [has_prefab_store_key_kv](#has_prefab_store_key_kv) | 判断预设是否存在STORE_KEY键值对 |
| [has_prefab_keyboard_key_kv](#has_prefab_keyboard_key_kv) | 判断预设是否存在KEYBOARD_KEY键值对 |
| [has_prefab_func_keyboard_key_kv](#has_prefab_func_keyboard_key_kv) | 判断预设是否存在FUNC_KEYBOARD_KEY键值对 |
| [has_prefab_mouse_key_kv](#has_prefab_mouse_key_kv) | 判断预设是否存在MOUSE_KEY键值对 |
| [has_prefab_mouse_wheel_kv](#has_prefab_mouse_wheel_kv) | 判断预设是否存在MOUSE_WHEEL键值对 |
| [has_prefab_post_effect_kv](#has_prefab_post_effect_kv) | 判断预设是否存在POST_EFFECT键值对 |
| [has_prefab_unit_type_kv](#has_prefab_unit_type_kv) | 判断预设是否存在UNIT_TYPE键值对 |
| [has_prefab_unit_command_type_kv](#has_prefab_unit_command_type_kv) | 判断预设是否存在UNIT_COMMAND_TYPE键值对 |
| [has_prefab_mini_map_color_type_kv](#has_prefab_mini_map_color_type_kv) | 判断预设是否存在MINI_MAP_COLOR_TYPE键值对 |
| [has_prefab_unit_behavior_kv](#has_prefab_unit_behavior_kv) | 判断预设是否存在UNIT_BEHAVIOR键值对 |
| [has_prefab_curved_path_kv](#has_prefab_curved_path_kv) | 判断预设是否存在CURVED_PATH键值对 |
| [has_prefab_curved_path_3d_kv](#has_prefab_curved_path_3d_kv) | 判断预设是否存在CURVED_PATH_3D键值对 |
| [get_unit_key_boolean_kv](#get_unit_key_boolean_kv) | 获取单位编号BOOLEAN键值对 |
| [get_item_key_boolean_kv](#get_item_key_boolean_kv) | 获取物品编号BOOLEAN键值对 |
| [get_ability_key_boolean_kv](#get_ability_key_boolean_kv) | 获取技能编号BOOLEAN键值对 |
| [get_modifier_key_boolean_kv](#get_modifier_key_boolean_kv) | 获取魔法效果特效编号BOOLEAN键值对 |
| [get_projectile_key_boolean_kv](#get_projectile_key_boolean_kv) | 获取特效编号BOOLEAN键值对 |
| [get_destructible_key_boolean_kv](#get_destructible_key_boolean_kv) | 获取可破坏物编号BOOLEAN键值对 |
| [get_tech_key_boolean_kv](#get_tech_key_boolean_kv) | 获取科技编号BOOLEAN键值对 |
| [get_icon_id_boolean_kv](#get_icon_id_boolean_kv) | 获取图片BOOLEAN键值对 |
| [get_physics_entity_key_boolean_kv](#get_physics_entity_key_boolean_kv) | 获取逻辑物理组件类型BOOLEAN键值对 |
| [get_unit_key_integer_kv](#get_unit_key_integer_kv) | 获取单位编号INTEGER键值对 |
| [get_item_key_integer_kv](#get_item_key_integer_kv) | 获取物品编号INTEGER键值对 |
| [get_ability_key_integer_kv](#get_ability_key_integer_kv) | 获取技能编号INTEGER键值对 |
| [get_modifier_key_integer_kv](#get_modifier_key_integer_kv) | 获取魔法效果特效编号INTEGER键值对 |
| [get_projectile_key_integer_kv](#get_projectile_key_integer_kv) | 获取特效编号INTEGER键值对 |
| [get_destructible_key_integer_kv](#get_destructible_key_integer_kv) | 获取可破坏物编号INTEGER键值对 |
| [get_tech_key_integer_kv](#get_tech_key_integer_kv) | 获取科技编号INTEGER键值对 |
| [get_icon_id_integer_kv](#get_icon_id_integer_kv) | 获取图片INTEGER键值对 |
| [get_physics_entity_key_integer_kv](#get_physics_entity_key_integer_kv) | 获取逻辑物理组件类型INTEGER键值对 |
| [get_unit_key_float_kv](#get_unit_key_float_kv) | 获取单位编号FLOAT键值对 |
| [get_item_key_float_kv](#get_item_key_float_kv) | 获取物品编号FLOAT键值对 |
| [get_ability_key_float_kv](#get_ability_key_float_kv) | 获取技能编号FLOAT键值对 |
| [get_modifier_key_float_kv](#get_modifier_key_float_kv) | 获取魔法效果特效编号FLOAT键值对 |
| [get_projectile_key_float_kv](#get_projectile_key_float_kv) | 获取特效编号FLOAT键值对 |
| [get_destructible_key_float_kv](#get_destructible_key_float_kv) | 获取可破坏物编号FLOAT键值对 |
| [get_tech_key_float_kv](#get_tech_key_float_kv) | 获取科技编号FLOAT键值对 |
| [get_icon_id_float_kv](#get_icon_id_float_kv) | 获取图片FLOAT键值对 |
| [get_physics_entity_key_float_kv](#get_physics_entity_key_float_kv) | 获取逻辑物理组件类型FLOAT键值对 |
| [get_unit_key_string_kv](#get_unit_key_string_kv) | 获取单位编号STRING键值对 |
| [get_item_key_string_kv](#get_item_key_string_kv) | 获取物品编号STRING键值对 |
| [get_ability_key_string_kv](#get_ability_key_string_kv) | 获取技能编号STRING键值对 |
| [get_modifier_key_string_kv](#get_modifier_key_string_kv) | 获取魔法效果特效编号STRING键值对 |
| [get_projectile_key_string_kv](#get_projectile_key_string_kv) | 获取特效编号STRING键值对 |
| [get_destructible_key_string_kv](#get_destructible_key_string_kv) | 获取可破坏物编号STRING键值对 |
| [get_tech_key_string_kv](#get_tech_key_string_kv) | 获取科技编号STRING键值对 |
| [get_icon_id_string_kv](#get_icon_id_string_kv) | 获取图片STRING键值对 |
| [get_physics_entity_key_string_kv](#get_physics_entity_key_string_kv) | 获取逻辑物理组件类型STRING键值对 |
| [get_unit_key_ui_comp_kv](#get_unit_key_ui_comp_kv) | 获取单位编号UI_COMP键值对 |
| [get_item_key_ui_comp_kv](#get_item_key_ui_comp_kv) | 获取物品编号UI_COMP键值对 |
| [get_ability_key_ui_comp_kv](#get_ability_key_ui_comp_kv) | 获取技能编号UI_COMP键值对 |
| [get_modifier_key_ui_comp_kv](#get_modifier_key_ui_comp_kv) | 获取魔法效果特效编号UI_COMP键值对 |
| [get_projectile_key_ui_comp_kv](#get_projectile_key_ui_comp_kv) | 获取特效编号UI_COMP键值对 |
| [get_destructible_key_ui_comp_kv](#get_destructible_key_ui_comp_kv) | 获取可破坏物编号UI_COMP键值对 |
| [get_tech_key_ui_comp_kv](#get_tech_key_ui_comp_kv) | 获取科技编号UI_COMP键值对 |
| [get_icon_id_ui_comp_kv](#get_icon_id_ui_comp_kv) | 获取图片UI_COMP键值对 |
| [get_physics_entity_key_ui_comp_kv](#get_physics_entity_key_ui_comp_kv) | 获取逻辑物理组件类型UI_COMP键值对 |
| [get_unit_key_ui_comp_type_kv](#get_unit_key_ui_comp_type_kv) | 获取单位编号UI_COMP_TYPE键值对 |
| [get_item_key_ui_comp_type_kv](#get_item_key_ui_comp_type_kv) | 获取物品编号UI_COMP_TYPE键值对 |
| [get_ability_key_ui_comp_type_kv](#get_ability_key_ui_comp_type_kv) | 获取技能编号UI_COMP_TYPE键值对 |
| [get_modifier_key_ui_comp_type_kv](#get_modifier_key_ui_comp_type_kv) | 获取魔法效果特效编号UI_COMP_TYPE键值对 |
| [get_projectile_key_ui_comp_type_kv](#get_projectile_key_ui_comp_type_kv) | 获取特效编号UI_COMP_TYPE键值对 |
| [get_destructible_key_ui_comp_type_kv](#get_destructible_key_ui_comp_type_kv) | 获取可破坏物编号UI_COMP_TYPE键值对 |
| [get_tech_key_ui_comp_type_kv](#get_tech_key_ui_comp_type_kv) | 获取科技编号UI_COMP_TYPE键值对 |
| [get_icon_id_ui_comp_type_kv](#get_icon_id_ui_comp_type_kv) | 获取图片UI_COMP_TYPE键值对 |
| [get_physics_entity_key_ui_comp_type_kv](#get_physics_entity_key_ui_comp_type_kv) | 获取逻辑物理组件类型UI_COMP_TYPE键值对 |
| [get_unit_key_ui_comp_event_type_kv](#get_unit_key_ui_comp_event_type_kv) | 获取单位编号UI_COMP_EVENT_TYPE键值对 |
| [get_item_key_ui_comp_event_type_kv](#get_item_key_ui_comp_event_type_kv) | 获取物品编号UI_COMP_EVENT_TYPE键值对 |
| [get_ability_key_ui_comp_event_type_kv](#get_ability_key_ui_comp_event_type_kv) | 获取技能编号UI_COMP_EVENT_TYPE键值对 |
| [get_modifier_key_ui_comp_event_type_kv](#get_modifier_key_ui_comp_event_type_kv) | 获取魔法效果特效编号UI_COMP_EVENT_TYPE键值对 |
| [get_projectile_key_ui_comp_event_type_kv](#get_projectile_key_ui_comp_event_type_kv) | 获取特效编号UI_COMP_EVENT_TYPE键值对 |
| [get_destructible_key_ui_comp_event_type_kv](#get_destructible_key_ui_comp_event_type_kv) | 获取可破坏物编号UI_COMP_EVENT_TYPE键值对 |
| [get_tech_key_ui_comp_event_type_kv](#get_tech_key_ui_comp_event_type_kv) | 获取科技编号UI_COMP_EVENT_TYPE键值对 |
| [get_icon_id_ui_comp_event_type_kv](#get_icon_id_ui_comp_event_type_kv) | 获取图片UI_COMP_EVENT_TYPE键值对 |
| [get_physics_entity_key_ui_comp_event_type_kv](#get_physics_entity_key_ui_comp_event_type_kv) | 获取逻辑物理组件类型UI_COMP_EVENT_TYPE键值对 |
| [get_unit_key_ui_comp_attr_kv](#get_unit_key_ui_comp_attr_kv) | 获取单位编号UI_COMP_ATTR键值对 |
| [get_item_key_ui_comp_attr_kv](#get_item_key_ui_comp_attr_kv) | 获取物品编号UI_COMP_ATTR键值对 |
| [get_ability_key_ui_comp_attr_kv](#get_ability_key_ui_comp_attr_kv) | 获取技能编号UI_COMP_ATTR键值对 |
| [get_modifier_key_ui_comp_attr_kv](#get_modifier_key_ui_comp_attr_kv) | 获取魔法效果特效编号UI_COMP_ATTR键值对 |
| [get_projectile_key_ui_comp_attr_kv](#get_projectile_key_ui_comp_attr_kv) | 获取特效编号UI_COMP_ATTR键值对 |
| [get_destructible_key_ui_comp_attr_kv](#get_destructible_key_ui_comp_attr_kv) | 获取可破坏物编号UI_COMP_ATTR键值对 |
| [get_tech_key_ui_comp_attr_kv](#get_tech_key_ui_comp_attr_kv) | 获取科技编号UI_COMP_ATTR键值对 |
| [get_icon_id_ui_comp_attr_kv](#get_icon_id_ui_comp_attr_kv) | 获取图片UI_COMP_ATTR键值对 |
| [get_physics_entity_key_ui_comp_attr_kv](#get_physics_entity_key_ui_comp_attr_kv) | 获取逻辑物理组件类型UI_COMP_ATTR键值对 |
| [get_unit_key_ui_comp_align_type_kv](#get_unit_key_ui_comp_align_type_kv) | 获取单位编号UI_COMP_ALIGN_TYPE键值对 |
| [get_item_key_ui_comp_align_type_kv](#get_item_key_ui_comp_align_type_kv) | 获取物品编号UI_COMP_ALIGN_TYPE键值对 |
| [get_ability_key_ui_comp_align_type_kv](#get_ability_key_ui_comp_align_type_kv) | 获取技能编号UI_COMP_ALIGN_TYPE键值对 |
| [get_modifier_key_ui_comp_align_type_kv](#get_modifier_key_ui_comp_align_type_kv) | 获取魔法效果特效编号UI_COMP_ALIGN_TYPE键值对 |
| [get_projectile_key_ui_comp_align_type_kv](#get_projectile_key_ui_comp_align_type_kv) | 获取特效编号UI_COMP_ALIGN_TYPE键值对 |
| [get_destructible_key_ui_comp_align_type_kv](#get_destructible_key_ui_comp_align_type_kv) | 获取可破坏物编号UI_COMP_ALIGN_TYPE键值对 |
| [get_tech_key_ui_comp_align_type_kv](#get_tech_key_ui_comp_align_type_kv) | 获取科技编号UI_COMP_ALIGN_TYPE键值对 |
| [get_icon_id_ui_comp_align_type_kv](#get_icon_id_ui_comp_align_type_kv) | 获取图片UI_COMP_ALIGN_TYPE键值对 |
| [get_physics_entity_key_ui_comp_align_type_kv](#get_physics_entity_key_ui_comp_align_type_kv) | 获取逻辑物理组件类型UI_COMP_ALIGN_TYPE键值对 |
| [get_unit_key_ui_prefab_kv](#get_unit_key_ui_prefab_kv) | 获取单位编号UI_PREFAB键值对 |
| [get_item_key_ui_prefab_kv](#get_item_key_ui_prefab_kv) | 获取物品编号UI_PREFAB键值对 |
| [get_ability_key_ui_prefab_kv](#get_ability_key_ui_prefab_kv) | 获取技能编号UI_PREFAB键值对 |
| [get_modifier_key_ui_prefab_kv](#get_modifier_key_ui_prefab_kv) | 获取魔法效果特效编号UI_PREFAB键值对 |
| [get_projectile_key_ui_prefab_kv](#get_projectile_key_ui_prefab_kv) | 获取特效编号UI_PREFAB键值对 |
| [get_destructible_key_ui_prefab_kv](#get_destructible_key_ui_prefab_kv) | 获取可破坏物编号UI_PREFAB键值对 |
| [get_tech_key_ui_prefab_kv](#get_tech_key_ui_prefab_kv) | 获取科技编号UI_PREFAB键值对 |
| [get_icon_id_ui_prefab_kv](#get_icon_id_ui_prefab_kv) | 获取图片UI_PREFAB键值对 |
| [get_physics_entity_key_ui_prefab_kv](#get_physics_entity_key_ui_prefab_kv) | 获取逻辑物理组件类型UI_PREFAB键值对 |
| [get_unit_key_ui_prefab_instance_kv](#get_unit_key_ui_prefab_instance_kv) | 获取单位编号UI_PREFAB_INSTANCE键值对 |
| [get_item_key_ui_prefab_instance_kv](#get_item_key_ui_prefab_instance_kv) | 获取物品编号UI_PREFAB_INSTANCE键值对 |
| [get_ability_key_ui_prefab_instance_kv](#get_ability_key_ui_prefab_instance_kv) | 获取技能编号UI_PREFAB_INSTANCE键值对 |
| [get_modifier_key_ui_prefab_instance_kv](#get_modifier_key_ui_prefab_instance_kv) | 获取魔法效果特效编号UI_PREFAB_INSTANCE键值对 |
| [get_projectile_key_ui_prefab_instance_kv](#get_projectile_key_ui_prefab_instance_kv) | 获取特效编号UI_PREFAB_INSTANCE键值对 |
| [get_destructible_key_ui_prefab_instance_kv](#get_destructible_key_ui_prefab_instance_kv) | 获取可破坏物编号UI_PREFAB_INSTANCE键值对 |
| [get_tech_key_ui_prefab_instance_kv](#get_tech_key_ui_prefab_instance_kv) | 获取科技编号UI_PREFAB_INSTANCE键值对 |
| [get_icon_id_ui_prefab_instance_kv](#get_icon_id_ui_prefab_instance_kv) | 获取图片UI_PREFAB_INSTANCE键值对 |
| [get_physics_entity_key_ui_prefab_instance_kv](#get_physics_entity_key_ui_prefab_instance_kv) | 获取逻辑物理组件类型UI_PREFAB_INSTANCE键值对 |
| [get_unit_key_ui_prefab_ins_uid_kv](#get_unit_key_ui_prefab_ins_uid_kv) | 获取单位编号UI_PREFAB_INS_UID键值对 |
| [get_item_key_ui_prefab_ins_uid_kv](#get_item_key_ui_prefab_ins_uid_kv) | 获取物品编号UI_PREFAB_INS_UID键值对 |
| [get_ability_key_ui_prefab_ins_uid_kv](#get_ability_key_ui_prefab_ins_uid_kv) | 获取技能编号UI_PREFAB_INS_UID键值对 |
| [get_modifier_key_ui_prefab_ins_uid_kv](#get_modifier_key_ui_prefab_ins_uid_kv) | 获取魔法效果特效编号UI_PREFAB_INS_UID键值对 |
| [get_projectile_key_ui_prefab_ins_uid_kv](#get_projectile_key_ui_prefab_ins_uid_kv) | 获取特效编号UI_PREFAB_INS_UID键值对 |
| [get_destructible_key_ui_prefab_ins_uid_kv](#get_destructible_key_ui_prefab_ins_uid_kv) | 获取可破坏物编号UI_PREFAB_INS_UID键值对 |
| [get_tech_key_ui_prefab_ins_uid_kv](#get_tech_key_ui_prefab_ins_uid_kv) | 获取科技编号UI_PREFAB_INS_UID键值对 |
| [get_icon_id_ui_prefab_ins_uid_kv](#get_icon_id_ui_prefab_ins_uid_kv) | 获取图片UI_PREFAB_INS_UID键值对 |
| [get_physics_entity_key_ui_prefab_ins_uid_kv](#get_physics_entity_key_ui_prefab_ins_uid_kv) | 获取逻辑物理组件类型UI_PREFAB_INS_UID键值对 |
| [get_unit_key_ui_direction_kv](#get_unit_key_ui_direction_kv) | 获取单位编号UI_DIRECTION键值对 |
| [get_item_key_ui_direction_kv](#get_item_key_ui_direction_kv) | 获取物品编号UI_DIRECTION键值对 |
| [get_ability_key_ui_direction_kv](#get_ability_key_ui_direction_kv) | 获取技能编号UI_DIRECTION键值对 |
| [get_modifier_key_ui_direction_kv](#get_modifier_key_ui_direction_kv) | 获取魔法效果特效编号UI_DIRECTION键值对 |
| [get_projectile_key_ui_direction_kv](#get_projectile_key_ui_direction_kv) | 获取特效编号UI_DIRECTION键值对 |
| [get_destructible_key_ui_direction_kv](#get_destructible_key_ui_direction_kv) | 获取可破坏物编号UI_DIRECTION键值对 |
| [get_tech_key_ui_direction_kv](#get_tech_key_ui_direction_kv) | 获取科技编号UI_DIRECTION键值对 |
| [get_icon_id_ui_direction_kv](#get_icon_id_ui_direction_kv) | 获取图片UI_DIRECTION键值对 |
| [get_physics_entity_key_ui_direction_kv](#get_physics_entity_key_ui_direction_kv) | 获取逻辑物理组件类型UI_DIRECTION键值对 |
| [get_unit_key_ui_model_camera_mod_kv](#get_unit_key_ui_model_camera_mod_kv) | 获取单位编号UI_MODEL_CAMERA_MOD键值对 |
| [get_item_key_ui_model_camera_mod_kv](#get_item_key_ui_model_camera_mod_kv) | 获取物品编号UI_MODEL_CAMERA_MOD键值对 |
| [get_ability_key_ui_model_camera_mod_kv](#get_ability_key_ui_model_camera_mod_kv) | 获取技能编号UI_MODEL_CAMERA_MOD键值对 |
| [get_modifier_key_ui_model_camera_mod_kv](#get_modifier_key_ui_model_camera_mod_kv) | 获取魔法效果特效编号UI_MODEL_CAMERA_MOD键值对 |
| [get_projectile_key_ui_model_camera_mod_kv](#get_projectile_key_ui_model_camera_mod_kv) | 获取特效编号UI_MODEL_CAMERA_MOD键值对 |
| [get_destructible_key_ui_model_camera_mod_kv](#get_destructible_key_ui_model_camera_mod_kv) | 获取可破坏物编号UI_MODEL_CAMERA_MOD键值对 |
| [get_tech_key_ui_model_camera_mod_kv](#get_tech_key_ui_model_camera_mod_kv) | 获取科技编号UI_MODEL_CAMERA_MOD键值对 |
| [get_icon_id_ui_model_camera_mod_kv](#get_icon_id_ui_model_camera_mod_kv) | 获取图片UI_MODEL_CAMERA_MOD键值对 |
| [get_physics_entity_key_ui_model_camera_mod_kv](#get_physics_entity_key_ui_model_camera_mod_kv) | 获取逻辑物理组件类型UI_MODEL_CAMERA_MOD键值对 |
| [get_unit_key_ui_btn_status_kv](#get_unit_key_ui_btn_status_kv) | 获取单位编号UI_BTN_STATUS键值对 |
| [get_item_key_ui_btn_status_kv](#get_item_key_ui_btn_status_kv) | 获取物品编号UI_BTN_STATUS键值对 |
| [get_ability_key_ui_btn_status_kv](#get_ability_key_ui_btn_status_kv) | 获取技能编号UI_BTN_STATUS键值对 |
| [get_modifier_key_ui_btn_status_kv](#get_modifier_key_ui_btn_status_kv) | 获取魔法效果特效编号UI_BTN_STATUS键值对 |
| [get_projectile_key_ui_btn_status_kv](#get_projectile_key_ui_btn_status_kv) | 获取特效编号UI_BTN_STATUS键值对 |
| [get_destructible_key_ui_btn_status_kv](#get_destructible_key_ui_btn_status_kv) | 获取可破坏物编号UI_BTN_STATUS键值对 |
| [get_tech_key_ui_btn_status_kv](#get_tech_key_ui_btn_status_kv) | 获取科技编号UI_BTN_STATUS键值对 |
| [get_icon_id_ui_btn_status_kv](#get_icon_id_ui_btn_status_kv) | 获取图片UI_BTN_STATUS键值对 |
| [get_physics_entity_key_ui_btn_status_kv](#get_physics_entity_key_ui_btn_status_kv) | 获取逻辑物理组件类型UI_BTN_STATUS键值对 |
| [get_unit_key_ui_scrollview_type_kv](#get_unit_key_ui_scrollview_type_kv) | 获取单位编号UI_SCROLLVIEW_TYPE键值对 |
| [get_item_key_ui_scrollview_type_kv](#get_item_key_ui_scrollview_type_kv) | 获取物品编号UI_SCROLLVIEW_TYPE键值对 |
| [get_ability_key_ui_scrollview_type_kv](#get_ability_key_ui_scrollview_type_kv) | 获取技能编号UI_SCROLLVIEW_TYPE键值对 |
| [get_modifier_key_ui_scrollview_type_kv](#get_modifier_key_ui_scrollview_type_kv) | 获取魔法效果特效编号UI_SCROLLVIEW_TYPE键值对 |
| [get_projectile_key_ui_scrollview_type_kv](#get_projectile_key_ui_scrollview_type_kv) | 获取特效编号UI_SCROLLVIEW_TYPE键值对 |
| [get_destructible_key_ui_scrollview_type_kv](#get_destructible_key_ui_scrollview_type_kv) | 获取可破坏物编号UI_SCROLLVIEW_TYPE键值对 |
| [get_tech_key_ui_scrollview_type_kv](#get_tech_key_ui_scrollview_type_kv) | 获取科技编号UI_SCROLLVIEW_TYPE键值对 |
| [get_icon_id_ui_scrollview_type_kv](#get_icon_id_ui_scrollview_type_kv) | 获取图片UI_SCROLLVIEW_TYPE键值对 |
| [get_physics_entity_key_ui_scrollview_type_kv](#get_physics_entity_key_ui_scrollview_type_kv) | 获取逻辑物理组件类型UI_SCROLLVIEW_TYPE键值对 |
| [get_unit_key_ui_anim_kv](#get_unit_key_ui_anim_kv) | 获取单位编号UI_ANIM键值对 |
| [get_item_key_ui_anim_kv](#get_item_key_ui_anim_kv) | 获取物品编号UI_ANIM键值对 |
| [get_ability_key_ui_anim_kv](#get_ability_key_ui_anim_kv) | 获取技能编号UI_ANIM键值对 |
| [get_modifier_key_ui_anim_kv](#get_modifier_key_ui_anim_kv) | 获取魔法效果特效编号UI_ANIM键值对 |
| [get_projectile_key_ui_anim_kv](#get_projectile_key_ui_anim_kv) | 获取特效编号UI_ANIM键值对 |
| [get_destructible_key_ui_anim_kv](#get_destructible_key_ui_anim_kv) | 获取可破坏物编号UI_ANIM键值对 |
| [get_tech_key_ui_anim_kv](#get_tech_key_ui_anim_kv) | 获取科技编号UI_ANIM键值对 |
| [get_icon_id_ui_anim_kv](#get_icon_id_ui_anim_kv) | 获取图片UI_ANIM键值对 |
| [get_physics_entity_key_ui_anim_kv](#get_physics_entity_key_ui_anim_kv) | 获取逻辑物理组件类型UI_ANIM键值对 |
| [get_unit_key_ui_anim_curve_kv](#get_unit_key_ui_anim_curve_kv) | 获取单位编号UI_ANIM_CURVE键值对 |
| [get_item_key_ui_anim_curve_kv](#get_item_key_ui_anim_curve_kv) | 获取物品编号UI_ANIM_CURVE键值对 |
| [get_ability_key_ui_anim_curve_kv](#get_ability_key_ui_anim_curve_kv) | 获取技能编号UI_ANIM_CURVE键值对 |
| [get_modifier_key_ui_anim_curve_kv](#get_modifier_key_ui_anim_curve_kv) | 获取魔法效果特效编号UI_ANIM_CURVE键值对 |
| [get_projectile_key_ui_anim_curve_kv](#get_projectile_key_ui_anim_curve_kv) | 获取特效编号UI_ANIM_CURVE键值对 |
| [get_destructible_key_ui_anim_curve_kv](#get_destructible_key_ui_anim_curve_kv) | 获取可破坏物编号UI_ANIM_CURVE键值对 |
| [get_tech_key_ui_anim_curve_kv](#get_tech_key_ui_anim_curve_kv) | 获取科技编号UI_ANIM_CURVE键值对 |
| [get_icon_id_ui_anim_curve_kv](#get_icon_id_ui_anim_curve_kv) | 获取图片UI_ANIM_CURVE键值对 |
| [get_physics_entity_key_ui_anim_curve_kv](#get_physics_entity_key_ui_anim_curve_kv) | 获取逻辑物理组件类型UI_ANIM_CURVE键值对 |
| [get_unit_key_audio_channel_kv](#get_unit_key_audio_channel_kv) | 获取单位编号AUDIO_CHANNEL键值对 |
| [get_item_key_audio_channel_kv](#get_item_key_audio_channel_kv) | 获取物品编号AUDIO_CHANNEL键值对 |
| [get_ability_key_audio_channel_kv](#get_ability_key_audio_channel_kv) | 获取技能编号AUDIO_CHANNEL键值对 |
| [get_modifier_key_audio_channel_kv](#get_modifier_key_audio_channel_kv) | 获取魔法效果特效编号AUDIO_CHANNEL键值对 |
| [get_projectile_key_audio_channel_kv](#get_projectile_key_audio_channel_kv) | 获取特效编号AUDIO_CHANNEL键值对 |
| [get_destructible_key_audio_channel_kv](#get_destructible_key_audio_channel_kv) | 获取可破坏物编号AUDIO_CHANNEL键值对 |
| [get_tech_key_audio_channel_kv](#get_tech_key_audio_channel_kv) | 获取科技编号AUDIO_CHANNEL键值对 |
| [get_icon_id_audio_channel_kv](#get_icon_id_audio_channel_kv) | 获取图片AUDIO_CHANNEL键值对 |
| [get_physics_entity_key_audio_channel_kv](#get_physics_entity_key_audio_channel_kv) | 获取逻辑物理组件类型AUDIO_CHANNEL键值对 |
| [get_unit_key_unit_entity_kv](#get_unit_key_unit_entity_kv) | 获取单位编号UNIT_ENTITY键值对 |
| [get_item_key_unit_entity_kv](#get_item_key_unit_entity_kv) | 获取物品编号UNIT_ENTITY键值对 |
| [get_ability_key_unit_entity_kv](#get_ability_key_unit_entity_kv) | 获取技能编号UNIT_ENTITY键值对 |
| [get_modifier_key_unit_entity_kv](#get_modifier_key_unit_entity_kv) | 获取魔法效果特效编号UNIT_ENTITY键值对 |
| [get_projectile_key_unit_entity_kv](#get_projectile_key_unit_entity_kv) | 获取特效编号UNIT_ENTITY键值对 |
| [get_destructible_key_unit_entity_kv](#get_destructible_key_unit_entity_kv) | 获取可破坏物编号UNIT_ENTITY键值对 |
| [get_tech_key_unit_entity_kv](#get_tech_key_unit_entity_kv) | 获取科技编号UNIT_ENTITY键值对 |
| [get_icon_id_unit_entity_kv](#get_icon_id_unit_entity_kv) | 获取图片UNIT_ENTITY键值对 |
| [get_physics_entity_key_unit_entity_kv](#get_physics_entity_key_unit_entity_kv) | 获取逻辑物理组件类型UNIT_ENTITY键值对 |
| [get_unit_key_unit_group_kv](#get_unit_key_unit_group_kv) | 获取单位编号UNIT_GROUP键值对 |
| [get_item_key_unit_group_kv](#get_item_key_unit_group_kv) | 获取物品编号UNIT_GROUP键值对 |
| [get_ability_key_unit_group_kv](#get_ability_key_unit_group_kv) | 获取技能编号UNIT_GROUP键值对 |
| [get_modifier_key_unit_group_kv](#get_modifier_key_unit_group_kv) | 获取魔法效果特效编号UNIT_GROUP键值对 |
| [get_projectile_key_unit_group_kv](#get_projectile_key_unit_group_kv) | 获取特效编号UNIT_GROUP键值对 |
| [get_destructible_key_unit_group_kv](#get_destructible_key_unit_group_kv) | 获取可破坏物编号UNIT_GROUP键值对 |
| [get_tech_key_unit_group_kv](#get_tech_key_unit_group_kv) | 获取科技编号UNIT_GROUP键值对 |
| [get_icon_id_unit_group_kv](#get_icon_id_unit_group_kv) | 获取图片UNIT_GROUP键值对 |
| [get_physics_entity_key_unit_group_kv](#get_physics_entity_key_unit_group_kv) | 获取逻辑物理组件类型UNIT_GROUP键值对 |
| [get_unit_key_unit_name_kv](#get_unit_key_unit_name_kv) | 获取单位编号UNIT_NAME键值对 |
| [get_item_key_unit_name_kv](#get_item_key_unit_name_kv) | 获取物品编号UNIT_NAME键值对 |
| [get_ability_key_unit_name_kv](#get_ability_key_unit_name_kv) | 获取技能编号UNIT_NAME键值对 |
| [get_modifier_key_unit_name_kv](#get_modifier_key_unit_name_kv) | 获取魔法效果特效编号UNIT_NAME键值对 |
| [get_projectile_key_unit_name_kv](#get_projectile_key_unit_name_kv) | 获取特效编号UNIT_NAME键值对 |
| [get_destructible_key_unit_name_kv](#get_destructible_key_unit_name_kv) | 获取可破坏物编号UNIT_NAME键值对 |
| [get_tech_key_unit_name_kv](#get_tech_key_unit_name_kv) | 获取科技编号UNIT_NAME键值对 |
| [get_icon_id_unit_name_kv](#get_icon_id_unit_name_kv) | 获取图片UNIT_NAME键值对 |
| [get_physics_entity_key_unit_name_kv](#get_physics_entity_key_unit_name_kv) | 获取逻辑物理组件类型UNIT_NAME键值对 |
| [get_unit_key_unit_name_pool_kv](#get_unit_key_unit_name_pool_kv) | 获取单位编号UNIT_NAME_POOL键值对 |
| [get_item_key_unit_name_pool_kv](#get_item_key_unit_name_pool_kv) | 获取物品编号UNIT_NAME_POOL键值对 |
| [get_ability_key_unit_name_pool_kv](#get_ability_key_unit_name_pool_kv) | 获取技能编号UNIT_NAME_POOL键值对 |
| [get_modifier_key_unit_name_pool_kv](#get_modifier_key_unit_name_pool_kv) | 获取魔法效果特效编号UNIT_NAME_POOL键值对 |
| [get_projectile_key_unit_name_pool_kv](#get_projectile_key_unit_name_pool_kv) | 获取特效编号UNIT_NAME_POOL键值对 |
| [get_destructible_key_unit_name_pool_kv](#get_destructible_key_unit_name_pool_kv) | 获取可破坏物编号UNIT_NAME_POOL键值对 |
| [get_tech_key_unit_name_pool_kv](#get_tech_key_unit_name_pool_kv) | 获取科技编号UNIT_NAME_POOL键值对 |
| [get_icon_id_unit_name_pool_kv](#get_icon_id_unit_name_pool_kv) | 获取图片UNIT_NAME_POOL键值对 |
| [get_physics_entity_key_unit_name_pool_kv](#get_physics_entity_key_unit_name_pool_kv) | 获取逻辑物理组件类型UNIT_NAME_POOL键值对 |
| [get_unit_key_unit_write_attribute_kv](#get_unit_key_unit_write_attribute_kv) | 获取单位编号UNIT_WRITE_ATTRIBUTE键值对 |
| [get_item_key_unit_write_attribute_kv](#get_item_key_unit_write_attribute_kv) | 获取物品编号UNIT_WRITE_ATTRIBUTE键值对 |
| [get_ability_key_unit_write_attribute_kv](#get_ability_key_unit_write_attribute_kv) | 获取技能编号UNIT_WRITE_ATTRIBUTE键值对 |
| [get_modifier_key_unit_write_attribute_kv](#get_modifier_key_unit_write_attribute_kv) | 获取魔法效果特效编号UNIT_WRITE_ATTRIBUTE键值对 |
| [get_projectile_key_unit_write_attribute_kv](#get_projectile_key_unit_write_attribute_kv) | 获取特效编号UNIT_WRITE_ATTRIBUTE键值对 |
| [get_destructible_key_unit_write_attribute_kv](#get_destructible_key_unit_write_attribute_kv) | 获取可破坏物编号UNIT_WRITE_ATTRIBUTE键值对 |
| [get_tech_key_unit_write_attribute_kv](#get_tech_key_unit_write_attribute_kv) | 获取科技编号UNIT_WRITE_ATTRIBUTE键值对 |
| [get_icon_id_unit_write_attribute_kv](#get_icon_id_unit_write_attribute_kv) | 获取图片UNIT_WRITE_ATTRIBUTE键值对 |
| [get_physics_entity_key_unit_write_attribute_kv](#get_physics_entity_key_unit_write_attribute_kv) | 获取逻辑物理组件类型UNIT_WRITE_ATTRIBUTE键值对 |
| [get_unit_key_attr_element_kv](#get_unit_key_attr_element_kv) | 获取单位编号ATTR_ELEMENT键值对 |
| [get_item_key_attr_element_kv](#get_item_key_attr_element_kv) | 获取物品编号ATTR_ELEMENT键值对 |
| [get_ability_key_attr_element_kv](#get_ability_key_attr_element_kv) | 获取技能编号ATTR_ELEMENT键值对 |
| [get_modifier_key_attr_element_kv](#get_modifier_key_attr_element_kv) | 获取魔法效果特效编号ATTR_ELEMENT键值对 |
| [get_projectile_key_attr_element_kv](#get_projectile_key_attr_element_kv) | 获取特效编号ATTR_ELEMENT键值对 |
| [get_destructible_key_attr_element_kv](#get_destructible_key_attr_element_kv) | 获取可破坏物编号ATTR_ELEMENT键值对 |
| [get_tech_key_attr_element_kv](#get_tech_key_attr_element_kv) | 获取科技编号ATTR_ELEMENT键值对 |
| [get_icon_id_attr_element_kv](#get_icon_id_attr_element_kv) | 获取图片ATTR_ELEMENT键值对 |
| [get_physics_entity_key_attr_element_kv](#get_physics_entity_key_attr_element_kv) | 获取逻辑物理组件类型ATTR_ELEMENT键值对 |
| [get_unit_key_attr_element_read_kv](#get_unit_key_attr_element_read_kv) | 获取单位编号ATTR_ELEMENT_READ键值对 |
| [get_item_key_attr_element_read_kv](#get_item_key_attr_element_read_kv) | 获取物品编号ATTR_ELEMENT_READ键值对 |
| [get_ability_key_attr_element_read_kv](#get_ability_key_attr_element_read_kv) | 获取技能编号ATTR_ELEMENT_READ键值对 |
| [get_modifier_key_attr_element_read_kv](#get_modifier_key_attr_element_read_kv) | 获取魔法效果特效编号ATTR_ELEMENT_READ键值对 |
| [get_projectile_key_attr_element_read_kv](#get_projectile_key_attr_element_read_kv) | 获取特效编号ATTR_ELEMENT_READ键值对 |
| [get_destructible_key_attr_element_read_kv](#get_destructible_key_attr_element_read_kv) | 获取可破坏物编号ATTR_ELEMENT_READ键值对 |
| [get_tech_key_attr_element_read_kv](#get_tech_key_attr_element_read_kv) | 获取科技编号ATTR_ELEMENT_READ键值对 |
| [get_icon_id_attr_element_read_kv](#get_icon_id_attr_element_read_kv) | 获取图片ATTR_ELEMENT_READ键值对 |
| [get_physics_entity_key_attr_element_read_kv](#get_physics_entity_key_attr_element_read_kv) | 获取逻辑物理组件类型ATTR_ELEMENT_READ键值对 |
| [get_unit_key_mover_entity_kv](#get_unit_key_mover_entity_kv) | 获取单位编号MOVER_ENTITY键值对 |
| [get_item_key_mover_entity_kv](#get_item_key_mover_entity_kv) | 获取物品编号MOVER_ENTITY键值对 |
| [get_ability_key_mover_entity_kv](#get_ability_key_mover_entity_kv) | 获取技能编号MOVER_ENTITY键值对 |
| [get_modifier_key_mover_entity_kv](#get_modifier_key_mover_entity_kv) | 获取魔法效果特效编号MOVER_ENTITY键值对 |
| [get_projectile_key_mover_entity_kv](#get_projectile_key_mover_entity_kv) | 获取特效编号MOVER_ENTITY键值对 |
| [get_destructible_key_mover_entity_kv](#get_destructible_key_mover_entity_kv) | 获取可破坏物编号MOVER_ENTITY键值对 |
| [get_tech_key_mover_entity_kv](#get_tech_key_mover_entity_kv) | 获取科技编号MOVER_ENTITY键值对 |
| [get_icon_id_mover_entity_kv](#get_icon_id_mover_entity_kv) | 获取图片MOVER_ENTITY键值对 |
| [get_physics_entity_key_mover_entity_kv](#get_physics_entity_key_mover_entity_kv) | 获取逻辑物理组件类型MOVER_ENTITY键值对 |
| [get_unit_key_image_quality_kv](#get_unit_key_image_quality_kv) | 获取单位编号IMAGE_QUALITY键值对 |
| [get_item_key_image_quality_kv](#get_item_key_image_quality_kv) | 获取物品编号IMAGE_QUALITY键值对 |
| [get_ability_key_image_quality_kv](#get_ability_key_image_quality_kv) | 获取技能编号IMAGE_QUALITY键值对 |
| [get_modifier_key_image_quality_kv](#get_modifier_key_image_quality_kv) | 获取魔法效果特效编号IMAGE_QUALITY键值对 |
| [get_projectile_key_image_quality_kv](#get_projectile_key_image_quality_kv) | 获取特效编号IMAGE_QUALITY键值对 |
| [get_destructible_key_image_quality_kv](#get_destructible_key_image_quality_kv) | 获取可破坏物编号IMAGE_QUALITY键值对 |
| [get_tech_key_image_quality_kv](#get_tech_key_image_quality_kv) | 获取科技编号IMAGE_QUALITY键值对 |
| [get_icon_id_image_quality_kv](#get_icon_id_image_quality_kv) | 获取图片IMAGE_QUALITY键值对 |
| [get_physics_entity_key_image_quality_kv](#get_physics_entity_key_image_quality_kv) | 获取逻辑物理组件类型IMAGE_QUALITY键值对 |
| [get_unit_key_window_type_setting_kv](#get_unit_key_window_type_setting_kv) | 获取单位编号WINDOW_TYPE_SETTING键值对 |
| [get_item_key_window_type_setting_kv](#get_item_key_window_type_setting_kv) | 获取物品编号WINDOW_TYPE_SETTING键值对 |
| [get_ability_key_window_type_setting_kv](#get_ability_key_window_type_setting_kv) | 获取技能编号WINDOW_TYPE_SETTING键值对 |
| [get_modifier_key_window_type_setting_kv](#get_modifier_key_window_type_setting_kv) | 获取魔法效果特效编号WINDOW_TYPE_SETTING键值对 |
| [get_projectile_key_window_type_setting_kv](#get_projectile_key_window_type_setting_kv) | 获取特效编号WINDOW_TYPE_SETTING键值对 |
| [get_destructible_key_window_type_setting_kv](#get_destructible_key_window_type_setting_kv) | 获取可破坏物编号WINDOW_TYPE_SETTING键值对 |
| [get_tech_key_window_type_setting_kv](#get_tech_key_window_type_setting_kv) | 获取科技编号WINDOW_TYPE_SETTING键值对 |
| [get_icon_id_window_type_setting_kv](#get_icon_id_window_type_setting_kv) | 获取图片WINDOW_TYPE_SETTING键值对 |
| [get_physics_entity_key_window_type_setting_kv](#get_physics_entity_key_window_type_setting_kv) | 获取逻辑物理组件类型WINDOW_TYPE_SETTING键值对 |
| [get_unit_key_item_entity_kv](#get_unit_key_item_entity_kv) | 获取单位编号ITEM_ENTITY键值对 |
| [get_item_key_item_entity_kv](#get_item_key_item_entity_kv) | 获取物品编号ITEM_ENTITY键值对 |
| [get_ability_key_item_entity_kv](#get_ability_key_item_entity_kv) | 获取技能编号ITEM_ENTITY键值对 |
| [get_modifier_key_item_entity_kv](#get_modifier_key_item_entity_kv) | 获取魔法效果特效编号ITEM_ENTITY键值对 |
| [get_projectile_key_item_entity_kv](#get_projectile_key_item_entity_kv) | 获取特效编号ITEM_ENTITY键值对 |
| [get_destructible_key_item_entity_kv](#get_destructible_key_item_entity_kv) | 获取可破坏物编号ITEM_ENTITY键值对 |
| [get_tech_key_item_entity_kv](#get_tech_key_item_entity_kv) | 获取科技编号ITEM_ENTITY键值对 |
| [get_icon_id_item_entity_kv](#get_icon_id_item_entity_kv) | 获取图片ITEM_ENTITY键值对 |
| [get_physics_entity_key_item_entity_kv](#get_physics_entity_key_item_entity_kv) | 获取逻辑物理组件类型ITEM_ENTITY键值对 |
| [get_unit_key_item_group_kv](#get_unit_key_item_group_kv) | 获取单位编号ITEM_GROUP键值对 |
| [get_item_key_item_group_kv](#get_item_key_item_group_kv) | 获取物品编号ITEM_GROUP键值对 |
| [get_ability_key_item_group_kv](#get_ability_key_item_group_kv) | 获取技能编号ITEM_GROUP键值对 |
| [get_modifier_key_item_group_kv](#get_modifier_key_item_group_kv) | 获取魔法效果特效编号ITEM_GROUP键值对 |
| [get_projectile_key_item_group_kv](#get_projectile_key_item_group_kv) | 获取特效编号ITEM_GROUP键值对 |
| [get_destructible_key_item_group_kv](#get_destructible_key_item_group_kv) | 获取可破坏物编号ITEM_GROUP键值对 |
| [get_tech_key_item_group_kv](#get_tech_key_item_group_kv) | 获取科技编号ITEM_GROUP键值对 |
| [get_icon_id_item_group_kv](#get_icon_id_item_group_kv) | 获取图片ITEM_GROUP键值对 |
| [get_physics_entity_key_item_group_kv](#get_physics_entity_key_item_group_kv) | 获取逻辑物理组件类型ITEM_GROUP键值对 |
| [get_unit_key_item_name_kv](#get_unit_key_item_name_kv) | 获取单位编号ITEM_NAME键值对 |
| [get_item_key_item_name_kv](#get_item_key_item_name_kv) | 获取物品编号ITEM_NAME键值对 |
| [get_ability_key_item_name_kv](#get_ability_key_item_name_kv) | 获取技能编号ITEM_NAME键值对 |
| [get_modifier_key_item_name_kv](#get_modifier_key_item_name_kv) | 获取魔法效果特效编号ITEM_NAME键值对 |
| [get_projectile_key_item_name_kv](#get_projectile_key_item_name_kv) | 获取特效编号ITEM_NAME键值对 |
| [get_destructible_key_item_name_kv](#get_destructible_key_item_name_kv) | 获取可破坏物编号ITEM_NAME键值对 |
| [get_tech_key_item_name_kv](#get_tech_key_item_name_kv) | 获取科技编号ITEM_NAME键值对 |
| [get_icon_id_item_name_kv](#get_icon_id_item_name_kv) | 获取图片ITEM_NAME键值对 |
| [get_physics_entity_key_item_name_kv](#get_physics_entity_key_item_name_kv) | 获取逻辑物理组件类型ITEM_NAME键值对 |
| [get_unit_key_ability_kv](#get_unit_key_ability_kv) | 获取单位编号ABILITY键值对 |
| [get_item_key_ability_kv](#get_item_key_ability_kv) | 获取物品编号ABILITY键值对 |
| [get_ability_key_ability_kv](#get_ability_key_ability_kv) | 获取技能编号ABILITY键值对 |
| [get_modifier_key_ability_kv](#get_modifier_key_ability_kv) | 获取魔法效果特效编号ABILITY键值对 |
| [get_projectile_key_ability_kv](#get_projectile_key_ability_kv) | 获取特效编号ABILITY键值对 |
| [get_destructible_key_ability_kv](#get_destructible_key_ability_kv) | 获取可破坏物编号ABILITY键值对 |
| [get_tech_key_ability_kv](#get_tech_key_ability_kv) | 获取科技编号ABILITY键值对 |
| [get_icon_id_ability_kv](#get_icon_id_ability_kv) | 获取图片ABILITY键值对 |
| [get_physics_entity_key_ability_kv](#get_physics_entity_key_ability_kv) | 获取逻辑物理组件类型ABILITY键值对 |
| [get_unit_key_ability_type_kv](#get_unit_key_ability_type_kv) | 获取单位编号ABILITY_TYPE键值对 |
| [get_item_key_ability_type_kv](#get_item_key_ability_type_kv) | 获取物品编号ABILITY_TYPE键值对 |
| [get_ability_key_ability_type_kv](#get_ability_key_ability_type_kv) | 获取技能编号ABILITY_TYPE键值对 |
| [get_modifier_key_ability_type_kv](#get_modifier_key_ability_type_kv) | 获取魔法效果特效编号ABILITY_TYPE键值对 |
| [get_projectile_key_ability_type_kv](#get_projectile_key_ability_type_kv) | 获取特效编号ABILITY_TYPE键值对 |
| [get_destructible_key_ability_type_kv](#get_destructible_key_ability_type_kv) | 获取可破坏物编号ABILITY_TYPE键值对 |
| [get_tech_key_ability_type_kv](#get_tech_key_ability_type_kv) | 获取科技编号ABILITY_TYPE键值对 |
| [get_icon_id_ability_type_kv](#get_icon_id_ability_type_kv) | 获取图片ABILITY_TYPE键值对 |
| [get_physics_entity_key_ability_type_kv](#get_physics_entity_key_ability_type_kv) | 获取逻辑物理组件类型ABILITY_TYPE键值对 |
| [get_unit_key_ability_cast_type_kv](#get_unit_key_ability_cast_type_kv) | 获取单位编号ABILITY_CAST_TYPE键值对 |
| [get_item_key_ability_cast_type_kv](#get_item_key_ability_cast_type_kv) | 获取物品编号ABILITY_CAST_TYPE键值对 |
| [get_ability_key_ability_cast_type_kv](#get_ability_key_ability_cast_type_kv) | 获取技能编号ABILITY_CAST_TYPE键值对 |
| [get_modifier_key_ability_cast_type_kv](#get_modifier_key_ability_cast_type_kv) | 获取魔法效果特效编号ABILITY_CAST_TYPE键值对 |
| [get_projectile_key_ability_cast_type_kv](#get_projectile_key_ability_cast_type_kv) | 获取特效编号ABILITY_CAST_TYPE键值对 |
| [get_destructible_key_ability_cast_type_kv](#get_destructible_key_ability_cast_type_kv) | 获取可破坏物编号ABILITY_CAST_TYPE键值对 |
| [get_tech_key_ability_cast_type_kv](#get_tech_key_ability_cast_type_kv) | 获取科技编号ABILITY_CAST_TYPE键值对 |
| [get_icon_id_ability_cast_type_kv](#get_icon_id_ability_cast_type_kv) | 获取图片ABILITY_CAST_TYPE键值对 |
| [get_physics_entity_key_ability_cast_type_kv](#get_physics_entity_key_ability_cast_type_kv) | 获取逻辑物理组件类型ABILITY_CAST_TYPE键值对 |
| [get_unit_key_ability_name_kv](#get_unit_key_ability_name_kv) | 获取单位编号ABILITY_NAME键值对 |
| [get_item_key_ability_name_kv](#get_item_key_ability_name_kv) | 获取物品编号ABILITY_NAME键值对 |
| [get_ability_key_ability_name_kv](#get_ability_key_ability_name_kv) | 获取技能编号ABILITY_NAME键值对 |
| [get_modifier_key_ability_name_kv](#get_modifier_key_ability_name_kv) | 获取魔法效果特效编号ABILITY_NAME键值对 |
| [get_projectile_key_ability_name_kv](#get_projectile_key_ability_name_kv) | 获取特效编号ABILITY_NAME键值对 |
| [get_destructible_key_ability_name_kv](#get_destructible_key_ability_name_kv) | 获取可破坏物编号ABILITY_NAME键值对 |
| [get_tech_key_ability_name_kv](#get_tech_key_ability_name_kv) | 获取科技编号ABILITY_NAME键值对 |
| [get_icon_id_ability_name_kv](#get_icon_id_ability_name_kv) | 获取图片ABILITY_NAME键值对 |
| [get_physics_entity_key_ability_name_kv](#get_physics_entity_key_ability_name_kv) | 获取逻辑物理组件类型ABILITY_NAME键值对 |
| [get_unit_key_skill_pointer_type_kv](#get_unit_key_skill_pointer_type_kv) | 获取单位编号SKILL_POINTER_TYPE键值对 |
| [get_item_key_skill_pointer_type_kv](#get_item_key_skill_pointer_type_kv) | 获取物品编号SKILL_POINTER_TYPE键值对 |
| [get_ability_key_skill_pointer_type_kv](#get_ability_key_skill_pointer_type_kv) | 获取技能编号SKILL_POINTER_TYPE键值对 |
| [get_modifier_key_skill_pointer_type_kv](#get_modifier_key_skill_pointer_type_kv) | 获取魔法效果特效编号SKILL_POINTER_TYPE键值对 |
| [get_projectile_key_skill_pointer_type_kv](#get_projectile_key_skill_pointer_type_kv) | 获取特效编号SKILL_POINTER_TYPE键值对 |
| [get_destructible_key_skill_pointer_type_kv](#get_destructible_key_skill_pointer_type_kv) | 获取可破坏物编号SKILL_POINTER_TYPE键值对 |
| [get_tech_key_skill_pointer_type_kv](#get_tech_key_skill_pointer_type_kv) | 获取科技编号SKILL_POINTER_TYPE键值对 |
| [get_icon_id_skill_pointer_type_kv](#get_icon_id_skill_pointer_type_kv) | 获取图片SKILL_POINTER_TYPE键值对 |
| [get_physics_entity_key_skill_pointer_type_kv](#get_physics_entity_key_skill_pointer_type_kv) | 获取逻辑物理组件类型SKILL_POINTER_TYPE键值对 |
| [get_unit_key_modifier_entity_kv](#get_unit_key_modifier_entity_kv) | 获取单位编号MODIFIER_ENTITY键值对 |
| [get_item_key_modifier_entity_kv](#get_item_key_modifier_entity_kv) | 获取物品编号MODIFIER_ENTITY键值对 |
| [get_ability_key_modifier_entity_kv](#get_ability_key_modifier_entity_kv) | 获取技能编号MODIFIER_ENTITY键值对 |
| [get_modifier_key_modifier_entity_kv](#get_modifier_key_modifier_entity_kv) | 获取魔法效果特效编号MODIFIER_ENTITY键值对 |
| [get_projectile_key_modifier_entity_kv](#get_projectile_key_modifier_entity_kv) | 获取特效编号MODIFIER_ENTITY键值对 |
| [get_trigger_list_actor_variable_all_goods_key](#get_trigger_list_actor_variable_all_goods_key) | 获取触发器GOODS_KEY 组变量数组 |
| [get_trigger_variable_map](#get_trigger_variable_map) | 获取全局触发器MAP非数组变量 |
| [get_trigger_actor_variable_map](#get_trigger_actor_variable_map) | 获取触发器MAP非数组 组变量 |
| [get_trigger_list_variable_map](#get_trigger_list_variable_map) | 获取全局触发器MAP数组变量子项 |
| [get_trigger_list_actor_variable_map](#get_trigger_list_actor_variable_map) | 获取触发器MAP数组 组变量子项 |
| [get_trigger_list_variable_all_map](#get_trigger_list_variable_all_map) | 获取全局触发器MAP数组变量 |
| [get_trigger_list_actor_variable_all_map](#get_trigger_list_actor_variable_all_map) | 获取触发器MAP 组变量数组 |
| [get_trigger_variable_store_item_type](#get_trigger_variable_store_item_type) | 获取全局触发器STORE_ITEM_TYPE非数组变量 |
| [get_trigger_actor_variable_store_item_type](#get_trigger_actor_variable_store_item_type) | 获取触发器STORE_ITEM_TYPE非数组 组变量 |
| [get_trigger_list_variable_store_item_type](#get_trigger_list_variable_store_item_type) | 获取全局触发器STORE_ITEM_TYPE数组变量子项 |
| [get_trigger_list_actor_variable_store_item_type](#get_trigger_list_actor_variable_store_item_type) | 获取触发器STORE_ITEM_TYPE数组 组变量子项 |
| [get_trigger_list_variable_all_store_item_type](#get_trigger_list_variable_all_store_item_type) | 获取全局触发器STORE_ITEM_TYPE数组变量 |
| [get_trigger_list_actor_variable_all_store_item_type](#get_trigger_list_actor_variable_all_store_item_type) | 获取触发器STORE_ITEM_TYPE 组变量数组 |
| [get_trigger_variable_site_state](#get_trigger_variable_site_state) | 获取全局触发器SITE_STATE非数组变量 |
| [get_trigger_actor_variable_site_state](#get_trigger_actor_variable_site_state) | 获取触发器SITE_STATE非数组 组变量 |
| [get_trigger_list_variable_site_state](#get_trigger_list_variable_site_state) | 获取全局触发器SITE_STATE数组变量子项 |
| [get_trigger_list_actor_variable_site_state](#get_trigger_list_actor_variable_site_state) | 获取触发器SITE_STATE数组 组变量子项 |
| [get_trigger_list_variable_all_site_state](#get_trigger_list_variable_all_site_state) | 获取全局触发器SITE_STATE数组变量 |
| [get_trigger_list_actor_variable_all_site_state](#get_trigger_list_actor_variable_all_site_state) | 获取触发器SITE_STATE 组变量数组 |
| [get_trigger_variable_coin_currency](#get_trigger_variable_coin_currency) | 获取全局触发器COIN_CURRENCY非数组变量 |
| [get_trigger_actor_variable_coin_currency](#get_trigger_actor_variable_coin_currency) | 获取触发器COIN_CURRENCY非数组 组变量 |
| [get_trigger_list_variable_coin_currency](#get_trigger_list_variable_coin_currency) | 获取全局触发器COIN_CURRENCY数组变量子项 |
| [get_trigger_list_actor_variable_coin_currency](#get_trigger_list_actor_variable_coin_currency) | 获取触发器COIN_CURRENCY数组 组变量子项 |
| [get_trigger_list_variable_all_coin_currency](#get_trigger_list_variable_all_coin_currency) | 获取全局触发器COIN_CURRENCY数组变量 |
| [get_trigger_list_actor_variable_all_coin_currency](#get_trigger_list_actor_variable_all_coin_currency) | 获取触发器COIN_CURRENCY 组变量数组 |
| [set_trigger_list_variable_ui_gridview_type](#set_trigger_list_variable_ui_gridview_type) | 设置全局触发器UI_GRIDVIEW_TYPE数组变量子项 |
| [set_trigger_list_actor_variable_ui_gridview_type](#set_trigger_list_actor_variable_ui_gridview_type) | 设置全局触发器UI_GRIDVIEW_TYPE数组 组变量子项 |
| [set_trigger_variable_ui_gridview_type](#set_trigger_variable_ui_gridview_type) | 设置全局触发器UI_GRIDVIEW_TYPE非数组变量 |
| [set_trigger_actor_variable_ui_gridview_type](#set_trigger_actor_variable_ui_gridview_type) | 设置全局触发器UI_GRIDVIEW_TYPE非数组 组变量 |
| [set_trigger_list_variable_ui_gridview_bar_type](#set_trigger_list_variable_ui_gridview_bar_type) | 设置全局触发器UI_GRIDVIEW_BAR_TYPE数组变量子项 |
| [set_trigger_list_actor_variable_ui_gridview_bar_type](#set_trigger_list_actor_variable_ui_gridview_bar_type) | 设置全局触发器UI_GRIDVIEW_BAR_TYPE数组 组变量子项 |
| [set_trigger_variable_ui_gridview_bar_type](#set_trigger_variable_ui_gridview_bar_type) | 设置全局触发器UI_GRIDVIEW_BAR_TYPE非数组变量 |
| [set_trigger_actor_variable_ui_gridview_bar_type](#set_trigger_actor_variable_ui_gridview_bar_type) | 设置全局触发器UI_GRIDVIEW_BAR_TYPE非数组 组变量 |
| [set_trigger_list_variable_ui_effect_camera_mode](#set_trigger_list_variable_ui_effect_camera_mode) | 设置全局触发器UI_EFFECT_CAMERA_MODE数组变量子项 |
| [set_trigger_list_actor_variable_ui_effect_camera_mode](#set_trigger_list_actor_variable_ui_effect_camera_mode) | 设置全局触发器UI_EFFECT_CAMERA_MODE数组 组变量子项 |
| [set_trigger_variable_ui_effect_camera_mode](#set_trigger_variable_ui_effect_camera_mode) | 设置全局触发器UI_EFFECT_CAMERA_MODE非数组变量 |
| [set_trigger_actor_variable_ui_effect_camera_mode](#set_trigger_actor_variable_ui_effect_camera_mode) | 设置全局触发器UI_EFFECT_CAMERA_MODE非数组 组变量 |
| [set_trigger_list_variable_ui_equip_slot_use_type](#set_trigger_list_variable_ui_equip_slot_use_type) | 设置全局触发器UI_EQUIP_SLOT_USE_TYPE数组变量子项 |
| [set_trigger_list_actor_variable_ui_equip_slot_use_type](#set_trigger_list_actor_variable_ui_equip_slot_use_type) | 设置全局触发器UI_EQUIP_SLOT_USE_TYPE数组 组变量子项 |
| [set_trigger_variable_ui_equip_slot_use_type](#set_trigger_variable_ui_equip_slot_use_type) | 设置全局触发器UI_EQUIP_SLOT_USE_TYPE非数组变量 |
| [set_trigger_actor_variable_ui_equip_slot_use_type](#set_trigger_actor_variable_ui_equip_slot_use_type) | 设置全局触发器UI_EQUIP_SLOT_USE_TYPE非数组 组变量 |
| [set_trigger_list_variable_ui_equip_slot_drag_type](#set_trigger_list_variable_ui_equip_slot_drag_type) | 设置全局触发器UI_EQUIP_SLOT_DRAG_TYPE数组变量子项 |
| [set_trigger_list_actor_variable_ui_equip_slot_drag_type](#set_trigger_list_actor_variable_ui_equip_slot_drag_type) | 设置全局触发器UI_EQUIP_SLOT_DRAG_TYPE数组 组变量子项 |
| [set_trigger_variable_ui_equip_slot_drag_type](#set_trigger_variable_ui_equip_slot_drag_type) | 设置全局触发器UI_EQUIP_SLOT_DRAG_TYPE非数组变量 |
| [set_trigger_actor_variable_ui_equip_slot_drag_type](#set_trigger_actor_variable_ui_equip_slot_drag_type) | 设置全局触发器UI_EQUIP_SLOT_DRAG_TYPE非数组 组变量 |
| [set_trigger_list_variable_ui_layout_clipping_type](#set_trigger_list_variable_ui_layout_clipping_type) | 设置全局触发器UI_LAYOUT_CLIPPING_TYPE数组变量子项 |
| [set_trigger_list_actor_variable_ui_layout_clipping_type](#set_trigger_list_actor_variable_ui_layout_clipping_type) | 设置全局触发器UI_LAYOUT_CLIPPING_TYPE数组 组变量子项 |
| [set_trigger_variable_ui_layout_clipping_type](#set_trigger_variable_ui_layout_clipping_type) | 设置全局触发器UI_LAYOUT_CLIPPING_TYPE非数组变量 |
| [set_trigger_actor_variable_ui_layout_clipping_type](#set_trigger_actor_variable_ui_layout_clipping_type) | 设置全局触发器UI_LAYOUT_CLIPPING_TYPE非数组 组变量 |
| [set_trigger_list_variable_ui_text_over_length_handling_type](#set_trigger_list_variable_ui_text_over_length_handling_type) | 设置全局触发器UI_TEXT_OVER_LENGTH_HANDLING_TYPE数组变量子项 |
| [set_trigger_list_actor_variable_ui_text_over_length_handling_type](#set_trigger_list_actor_variable_ui_text_over_length_handling_type) | 设置全局触发器UI_TEXT_OVER_LENGTH_HANDLING_TYPE数组 组变量子项 |
| [set_trigger_variable_ui_text_over_length_handling_type](#set_trigger_variable_ui_text_over_length_handling_type) | 设置全局触发器UI_TEXT_OVER_LENGTH_HANDLING_TYPE非数组变量 |
| [set_trigger_actor_variable_ui_text_over_length_handling_type](#set_trigger_actor_variable_ui_text_over_length_handling_type) | 设置全局触发器UI_TEXT_OVER_LENGTH_HANDLING_TYPE非数组 组变量 |
| [set_trigger_list_variable_ui_pos_adapt_mode](#set_trigger_list_variable_ui_pos_adapt_mode) | 设置全局触发器UI_POS_ADAPT_MODE数组变量子项 |
| [set_trigger_list_actor_variable_ui_pos_adapt_mode](#set_trigger_list_actor_variable_ui_pos_adapt_mode) | 设置全局触发器UI_POS_ADAPT_MODE数组 组变量子项 |
| [set_trigger_variable_ui_pos_adapt_mode](#set_trigger_variable_ui_pos_adapt_mode) | 设置全局触发器UI_POS_ADAPT_MODE非数组变量 |
| [set_trigger_actor_variable_ui_pos_adapt_mode](#set_trigger_actor_variable_ui_pos_adapt_mode) | 设置全局触发器UI_POS_ADAPT_MODE非数组 组变量 |
| [set_trigger_list_variable_ui_chat_send_channel](#set_trigger_list_variable_ui_chat_send_channel) | 设置全局触发器UI_CHAT_SEND_CHANNEL数组变量子项 |
| [set_trigger_list_actor_variable_ui_chat_send_channel](#set_trigger_list_actor_variable_ui_chat_send_channel) | 设置全局触发器UI_CHAT_SEND_CHANNEL数组 组变量子项 |
| [set_trigger_variable_ui_chat_send_channel](#set_trigger_variable_ui_chat_send_channel) | 设置全局触发器UI_CHAT_SEND_CHANNEL非数组变量 |
| [set_trigger_actor_variable_ui_chat_send_channel](#set_trigger_actor_variable_ui_chat_send_channel) | 设置全局触发器UI_CHAT_SEND_CHANNEL非数组 组变量 |
| [set_trigger_list_variable_ui_chat_recv_channel](#set_trigger_list_variable_ui_chat_recv_channel) | 设置全局触发器UI_CHAT_RECV_CHANNEL数组变量子项 |
| [set_trigger_list_actor_variable_ui_chat_recv_channel](#set_trigger_list_actor_variable_ui_chat_recv_channel) | 设置全局触发器UI_CHAT_RECV_CHANNEL数组 组变量子项 |
| [set_trigger_variable_ui_chat_recv_channel](#set_trigger_variable_ui_chat_recv_channel) | 设置全局触发器UI_CHAT_RECV_CHANNEL非数组变量 |
| [set_trigger_actor_variable_ui_chat_recv_channel](#set_trigger_actor_variable_ui_chat_recv_channel) | 设置全局触发器UI_CHAT_RECV_CHANNEL非数组 组变量 |
| [set_trigger_list_variable_ui_anim_play_mode](#set_trigger_list_variable_ui_anim_play_mode) | 设置全局触发器UI_ANIM_PLAY_MODE数组变量子项 |
| [set_trigger_list_actor_variable_ui_anim_play_mode](#set_trigger_list_actor_variable_ui_anim_play_mode) | 设置全局触发器UI_ANIM_PLAY_MODE数组 组变量子项 |
| [set_trigger_variable_ui_anim_play_mode](#set_trigger_variable_ui_anim_play_mode) | 设置全局触发器UI_ANIM_PLAY_MODE非数组变量 |
| [set_trigger_actor_variable_ui_anim_play_mode](#set_trigger_actor_variable_ui_anim_play_mode) | 设置全局触发器UI_ANIM_PLAY_MODE非数组 组变量 |
| [set_trigger_list_variable_ui_text_font_name](#set_trigger_list_variable_ui_text_font_name) | 设置全局触发器UI_TEXT_FONT_NAME数组变量子项 |
| [set_trigger_list_actor_variable_ui_text_font_name](#set_trigger_list_actor_variable_ui_text_font_name) | 设置全局触发器UI_TEXT_FONT_NAME数组 组变量子项 |
| [set_trigger_variable_ui_text_font_name](#set_trigger_variable_ui_text_font_name) | 设置全局触发器UI_TEXT_FONT_NAME非数组变量 |
| [set_trigger_actor_variable_ui_text_font_name](#set_trigger_actor_variable_ui_text_font_name) | 设置全局触发器UI_TEXT_FONT_NAME非数组 组变量 |
| [set_trigger_list_variable_ui_eca_anim_type](#set_trigger_list_variable_ui_eca_anim_type) | 设置全局触发器UI_ECA_ANIM_TYPE数组变量子项 |
| [set_trigger_list_actor_variable_ui_eca_anim_type](#set_trigger_list_actor_variable_ui_eca_anim_type) | 设置全局触发器UI_ECA_ANIM_TYPE数组 组变量子项 |
| [set_trigger_variable_ui_eca_anim_type](#set_trigger_variable_ui_eca_anim_type) | 设置全局触发器UI_ECA_ANIM_TYPE非数组变量 |
| [set_trigger_actor_variable_ui_eca_anim_type](#set_trigger_actor_variable_ui_eca_anim_type) | 设置全局触发器UI_ECA_ANIM_TYPE非数组 组变量 |
| [set_trigger_list_variable_local_unit_entity](#set_trigger_list_variable_local_unit_entity) | 设置全局触发器LOCAL_UNIT_ENTITY数组变量子项 |
| [set_trigger_list_actor_variable_local_unit_entity](#set_trigger_list_actor_variable_local_unit_entity) | 设置全局触发器LOCAL_UNIT_ENTITY数组 组变量子项 |
| [set_trigger_variable_local_unit_entity](#set_trigger_variable_local_unit_entity) | 设置全局触发器LOCAL_UNIT_ENTITY非数组变量 |
| [set_trigger_actor_variable_local_unit_entity](#set_trigger_actor_variable_local_unit_entity) | 设置全局触发器LOCAL_UNIT_ENTITY非数组 组变量 |
| [set_trigger_list_variable_local_unit_group](#set_trigger_list_variable_local_unit_group) | 设置全局触发器LOCAL_UNIT_GROUP数组变量子项 |
| [set_trigger_list_actor_variable_local_unit_group](#set_trigger_list_actor_variable_local_unit_group) | 设置全局触发器LOCAL_UNIT_GROUP数组 组变量子项 |
| [set_trigger_variable_local_unit_group](#set_trigger_variable_local_unit_group) | 设置全局触发器LOCAL_UNIT_GROUP非数组变量 |
| [set_trigger_actor_variable_local_unit_group](#set_trigger_actor_variable_local_unit_group) | 设置全局触发器LOCAL_UNIT_GROUP非数组 组变量 |
| [set_trigger_list_variable_deco_entity](#set_trigger_list_variable_deco_entity) | 设置全局触发器DECO_ENTITY数组变量子项 |
| [set_trigger_list_actor_variable_deco_entity](#set_trigger_list_actor_variable_deco_entity) | 设置全局触发器DECO_ENTITY数组 组变量子项 |
| [set_trigger_variable_deco_entity](#set_trigger_variable_deco_entity) | 设置全局触发器DECO_ENTITY非数组变量 |
| [set_trigger_actor_variable_deco_entity](#set_trigger_actor_variable_deco_entity) | 设置全局触发器DECO_ENTITY非数组 组变量 |
| [set_trigger_list_variable_scene_preset](#set_trigger_list_variable_scene_preset) | 设置全局触发器SCENE_PRESET数组变量子项 |
| [set_trigger_list_actor_variable_scene_preset](#set_trigger_list_actor_variable_scene_preset) | 设置全局触发器SCENE_PRESET数组 组变量子项 |
| [set_trigger_variable_scene_preset](#set_trigger_variable_scene_preset) | 设置全局触发器SCENE_PRESET非数组变量 |
| [set_trigger_actor_variable_scene_preset](#set_trigger_actor_variable_scene_preset) | 设置全局触发器SCENE_PRESET非数组 组变量 |
| [set_trigger_list_variable_item_stack_type](#set_trigger_list_variable_item_stack_type) | 设置全局触发器ITEM_STACK_TYPE数组变量子项 |
| [set_trigger_list_actor_variable_item_stack_type](#set_trigger_list_actor_variable_item_stack_type) | 设置全局触发器ITEM_STACK_TYPE数组 组变量子项 |
| [set_trigger_variable_item_stack_type](#set_trigger_variable_item_stack_type) | 设置全局触发器ITEM_STACK_TYPE非数组变量 |
| [set_trigger_actor_variable_item_stack_type](#set_trigger_actor_variable_item_stack_type) | 设置全局触发器ITEM_STACK_TYPE非数组 组变量 |
| [set_trigger_list_variable_ability_release_id](#set_trigger_list_variable_ability_release_id) | 设置全局触发器ABILITY_RELEASE_ID数组变量子项 |
| [set_trigger_list_actor_variable_ability_release_id](#set_trigger_list_actor_variable_ability_release_id) | 设置全局触发器ABILITY_RELEASE_ID数组 组变量子项 |
| [set_trigger_variable_ability_release_id](#set_trigger_variable_ability_release_id) | 设置全局触发器ABILITY_RELEASE_ID非数组变量 |
| [set_trigger_actor_variable_ability_release_id](#set_trigger_actor_variable_ability_release_id) | 设置全局触发器ABILITY_RELEASE_ID非数组 组变量 |
| [set_trigger_list_variable_deco_name](#set_trigger_list_variable_deco_name) | 设置全局触发器DECO_NAME数组变量子项 |
| [set_trigger_list_actor_variable_deco_name](#set_trigger_list_actor_variable_deco_name) | 设置全局触发器DECO_NAME数组 组变量子项 |
| [set_trigger_variable_deco_name](#set_trigger_variable_deco_name) | 设置全局触发器DECO_NAME非数组变量 |
| [set_trigger_actor_variable_deco_name](#set_trigger_actor_variable_deco_name) | 设置全局触发器DECO_NAME非数组 组变量 |
| [set_trigger_list_variable_ui_point](#set_trigger_list_variable_ui_point) | 设置全局触发器UI_POINT数组变量子项 |
| [set_trigger_list_actor_variable_ui_point](#set_trigger_list_actor_variable_ui_point) | 设置全局触发器UI_POINT数组 组变量子项 |
| [set_trigger_variable_ui_point](#set_trigger_variable_ui_point) | 设置全局触发器UI_POINT非数组变量 |
| [set_trigger_actor_variable_ui_point](#set_trigger_actor_variable_ui_point) | 设置全局触发器UI_POINT非数组 组变量 |
| [set_trigger_list_variable_attach_model_entity](#set_trigger_list_variable_attach_model_entity) | 设置全局触发器ATTACH_MODEL_ENTITY数组变量子项 |
| [set_trigger_list_actor_variable_attach_model_entity](#set_trigger_list_actor_variable_attach_model_entity) | 设置全局触发器ATTACH_MODEL_ENTITY数组 组变量子项 |
| [set_trigger_variable_attach_model_entity](#set_trigger_variable_attach_model_entity) | 设置全局触发器ATTACH_MODEL_ENTITY非数组变量 |
| [set_trigger_actor_variable_attach_model_entity](#set_trigger_actor_variable_attach_model_entity) | 设置全局触发器ATTACH_MODEL_ENTITY非数组 组变量 |
| [set_trigger_list_variable_live2d](#set_trigger_list_variable_live2d) | 设置全局触发器LIVE2D数组变量子项 |
| [set_trigger_list_actor_variable_live2d](#set_trigger_list_actor_variable_live2d) | 设置全局触发器LIVE2D数组 组变量子项 |
| [set_trigger_variable_live2d](#set_trigger_variable_live2d) | 设置全局触发器LIVE2D非数组变量 |
| [set_trigger_actor_variable_live2d](#set_trigger_actor_variable_live2d) | 设置全局触发器LIVE2D非数组 组变量 |
| [set_trigger_list_variable_spine](#set_trigger_list_variable_spine) | 设置全局触发器SPINE数组变量子项 |
| [set_trigger_list_actor_variable_spine](#set_trigger_list_actor_variable_spine) | 设置全局触发器SPINE数组 组变量子项 |
| [set_trigger_variable_spine](#set_trigger_variable_spine) | 设置全局触发器SPINE非数组变量 |
| [set_trigger_actor_variable_spine](#set_trigger_actor_variable_spine) | 设置全局触发器SPINE非数组 组变量 |
| [set_trigger_list_variable_debug_shape](#set_trigger_list_variable_debug_shape) | 设置全局触发器DEBUG_SHAPE数组变量子项 |
| [set_trigger_list_actor_variable_debug_shape](#set_trigger_list_actor_variable_debug_shape) | 设置全局触发器DEBUG_SHAPE数组 组变量子项 |
| [set_trigger_variable_debug_shape](#set_trigger_variable_debug_shape) | 设置全局触发器DEBUG_SHAPE非数组变量 |
| [set_trigger_actor_variable_debug_shape](#set_trigger_actor_variable_debug_shape) | 设置全局触发器DEBUG_SHAPE非数组 组变量 |
| [set_trigger_list_variable_watching_mode_status](#set_trigger_list_variable_watching_mode_status) | 设置全局触发器WATCHING_MODE_STATUS数组变量子项 |
| [set_trigger_list_actor_variable_watching_mode_status](#set_trigger_list_actor_variable_watching_mode_status) | 设置全局触发器WATCHING_MODE_STATUS数组 组变量子项 |
| [set_trigger_variable_watching_mode_status](#set_trigger_variable_watching_mode_status) | 设置全局触发器WATCHING_MODE_STATUS非数组变量 |
| [set_trigger_actor_variable_watching_mode_status](#set_trigger_actor_variable_watching_mode_status) | 设置全局触发器WATCHING_MODE_STATUS非数组 组变量 |
| [set_trigger_list_variable_force_entity](#set_trigger_list_variable_force_entity) | 设置全局触发器FORCE_ENTITY数组变量子项 |
| [set_trigger_list_actor_variable_force_entity](#set_trigger_list_actor_variable_force_entity) | 设置全局触发器FORCE_ENTITY数组 组变量子项 |
| [set_trigger_variable_force_entity](#set_trigger_variable_force_entity) | 设置全局触发器FORCE_ENTITY非数组变量 |
| [set_trigger_actor_variable_force_entity](#set_trigger_actor_variable_force_entity) | 设置全局触发器FORCE_ENTITY非数组 组变量 |
| [set_trigger_list_variable_goods_key](#set_trigger_list_variable_goods_key) | 设置全局触发器GOODS_KEY数组变量子项 |
| [set_trigger_list_actor_variable_goods_key](#set_trigger_list_actor_variable_goods_key) | 设置全局触发器GOODS_KEY数组 组变量子项 |
| [set_trigger_variable_goods_key](#set_trigger_variable_goods_key) | 设置全局触发器GOODS_KEY非数组变量 |
| [set_trigger_actor_variable_goods_key](#set_trigger_actor_variable_goods_key) | 设置全局触发器GOODS_KEY非数组 组变量 |
| [set_trigger_list_variable_map](#set_trigger_list_variable_map) | 设置全局触发器MAP数组变量子项 |
| [set_trigger_list_actor_variable_map](#set_trigger_list_actor_variable_map) | 设置全局触发器MAP数组 组变量子项 |
| [set_trigger_variable_map](#set_trigger_variable_map) | 设置全局触发器MAP非数组变量 |
| [set_trigger_actor_variable_map](#set_trigger_actor_variable_map) | 设置全局触发器MAP非数组 组变量 |
| [set_trigger_list_variable_store_item_type](#set_trigger_list_variable_store_item_type) | 设置全局触发器STORE_ITEM_TYPE数组变量子项 |
| [set_trigger_list_actor_variable_store_item_type](#set_trigger_list_actor_variable_store_item_type) | 设置全局触发器STORE_ITEM_TYPE数组 组变量子项 |
| [set_trigger_variable_store_item_type](#set_trigger_variable_store_item_type) | 设置全局触发器STORE_ITEM_TYPE非数组变量 |
| [set_trigger_actor_variable_store_item_type](#set_trigger_actor_variable_store_item_type) | 设置全局触发器STORE_ITEM_TYPE非数组 组变量 |
| [set_trigger_list_variable_site_state](#set_trigger_list_variable_site_state) | 设置全局触发器SITE_STATE数组变量子项 |
| [set_trigger_list_actor_variable_site_state](#set_trigger_list_actor_variable_site_state) | 设置全局触发器SITE_STATE数组 组变量子项 |
| [set_trigger_variable_site_state](#set_trigger_variable_site_state) | 设置全局触发器SITE_STATE非数组变量 |
| [set_trigger_actor_variable_site_state](#set_trigger_actor_variable_site_state) | 设置全局触发器SITE_STATE非数组 组变量 |
| [set_trigger_list_variable_coin_currency](#set_trigger_list_variable_coin_currency) | 设置全局触发器COIN_CURRENCY数组变量子项 |
| [set_trigger_list_actor_variable_coin_currency](#set_trigger_list_actor_variable_coin_currency) | 设置全局触发器COIN_CURRENCY数组 组变量子项 |
| [set_trigger_variable_coin_currency](#set_trigger_variable_coin_currency) | 设置全局触发器COIN_CURRENCY非数组变量 |
| [set_trigger_actor_variable_coin_currency](#set_trigger_actor_variable_coin_currency) | 设置全局触发器COIN_CURRENCY非数组 组变量 |
| [get_deco_entity_list_value](#get_deco_entity_list_value) | 获取DECO_ENTITY数组中某项 |
| [set_deco_entity_list_value](#set_deco_entity_list_value) | 设置DECO_ENTITY数组中某项 |
| [get_deco_entity_n_list](#get_deco_entity_n_list) | 生成n个值为v的DECO_ENTITY数组 |
| [get_scene_preset_list_value](#get_scene_preset_list_value) | 获取SCENE_PRESET数组中某项 |
| [set_scene_preset_list_value](#set_scene_preset_list_value) | 设置SCENE_PRESET数组中某项 |
| [get_scene_preset_n_list](#get_scene_preset_n_list) | 生成n个值为v的SCENE_PRESET数组 |
| [get_spine_list_value](#get_spine_list_value) | 获取SPINE数组中某项 |
| [set_spine_list_value](#set_spine_list_value) | 设置SPINE数组中某项 |
| [get_spine_n_list](#get_spine_n_list) | 生成n个值为v的SPINE数组 |
| [get_ui_anim_play_mode_list_value](#get_ui_anim_play_mode_list_value) | 获取UI_ANIM_PLAY_MODE数组中某项 |
| [set_ui_anim_play_mode_list_value](#set_ui_anim_play_mode_list_value) | 设置UI_ANIM_PLAY_MODE数组中某项 |
| [get_ui_anim_play_mode_n_list](#get_ui_anim_play_mode_n_list) | 生成n个值为v的UI_ANIM_PLAY_MODE数组 |
| [get_debug_shape_list_value](#get_debug_shape_list_value) | 获取DEBUG_SHAPE数组中某项 |
| [set_debug_shape_list_value](#set_debug_shape_list_value) | 设置DEBUG_SHAPE数组中某项 |
| [get_debug_shape_n_list](#get_debug_shape_n_list) | 生成n个值为v的DEBUG_SHAPE数组 |
| [get_ui_text_font_name_list_value](#get_ui_text_font_name_list_value) | 获取UI_TEXT_FONT_NAME数组中某项 |
| [set_ui_text_font_name_list_value](#set_ui_text_font_name_list_value) | 设置UI_TEXT_FONT_NAME数组中某项 |
| [get_ui_text_font_name_n_list](#get_ui_text_font_name_n_list) | 生成n个值为v的UI_TEXT_FONT_NAME数组 |
| [get_ui_eca_anim_type_list_value](#get_ui_eca_anim_type_list_value) | 获取UI_ECA_ANIM_TYPE数组中某项 |
| [set_ui_eca_anim_type_list_value](#set_ui_eca_anim_type_list_value) | 设置UI_ECA_ANIM_TYPE数组中某项 |
| [get_ui_eca_anim_type_n_list](#get_ui_eca_anim_type_n_list) | 生成n个值为v的UI_ECA_ANIM_TYPE数组 |
| [get_local_unit_entity_list_value](#get_local_unit_entity_list_value) | 获取LOCAL_UNIT_ENTITY数组中某项 |
| [set_local_unit_entity_list_value](#set_local_unit_entity_list_value) | 设置LOCAL_UNIT_ENTITY数组中某项 |
| [get_local_unit_entity_n_list](#get_local_unit_entity_n_list) | 生成n个值为v的LOCAL_UNIT_ENTITY数组 |
| [get_local_unit_group_list_value](#get_local_unit_group_list_value) | 获取LOCAL_UNIT_GROUP数组中某项 |
| [set_local_unit_group_list_value](#set_local_unit_group_list_value) | 设置LOCAL_UNIT_GROUP数组中某项 |
| [get_local_unit_group_n_list](#get_local_unit_group_n_list) | 生成n个值为v的LOCAL_UNIT_GROUP数组 |
| [get_store_item_type_list_value](#get_store_item_type_list_value) | 获取STORE_ITEM_TYPE数组中某项 |
| [set_store_item_type_list_value](#set_store_item_type_list_value) | 设置STORE_ITEM_TYPE数组中某项 |
| [get_store_item_type_n_list](#get_store_item_type_n_list) | 生成n个值为v的STORE_ITEM_TYPE数组 |
| [get_watching_mode_status_list_value](#get_watching_mode_status_list_value) | 获取WATCHING_MODE_STATUS数组中某项 |
| [set_watching_mode_status_list_value](#set_watching_mode_status_list_value) | 设置WATCHING_MODE_STATUS数组中某项 |
| [get_watching_mode_status_n_list](#get_watching_mode_status_n_list) | 生成n个值为v的WATCHING_MODE_STATUS数组 |
| [get_item_stack_type_list_value](#get_item_stack_type_list_value) | 获取ITEM_STACK_TYPE数组中某项 |
| [set_item_stack_type_list_value](#set_item_stack_type_list_value) | 设置ITEM_STACK_TYPE数组中某项 |
| [get_item_stack_type_n_list](#get_item_stack_type_n_list) | 生成n个值为v的ITEM_STACK_TYPE数组 |
| [get_deco_name_list_value](#get_deco_name_list_value) | 获取DECO_NAME数组中某项 |
| [set_deco_name_list_value](#set_deco_name_list_value) | 设置DECO_NAME数组中某项 |
| [get_deco_name_n_list](#get_deco_name_n_list) | 生成n个值为v的DECO_NAME数组 |
| [get_ability_release_id_list_value](#get_ability_release_id_list_value) | 获取ABILITY_RELEASE_ID数组中某项 |
| [set_ability_release_id_list_value](#set_ability_release_id_list_value) | 设置ABILITY_RELEASE_ID数组中某项 |
| [get_ability_release_id_n_list](#get_ability_release_id_n_list) | 生成n个值为v的ABILITY_RELEASE_ID数组 |
| [get_ui_point_list_value](#get_ui_point_list_value) | 获取UI_POINT数组中某项 |
| [set_ui_point_list_value](#set_ui_point_list_value) | 设置UI_POINT数组中某项 |
| [get_ui_point_n_list](#get_ui_point_n_list) | 生成n个值为v的UI_POINT数组 |
| [get_force_entity_list_value](#get_force_entity_list_value) | 获取FORCE_ENTITY数组中某项 |
| [set_force_entity_list_value](#set_force_entity_list_value) | 设置FORCE_ENTITY数组中某项 |
| [get_force_entity_n_list](#get_force_entity_n_list) | 生成n个值为v的FORCE_ENTITY数组 |
| [get_site_state_list_value](#get_site_state_list_value) | 获取SITE_STATE数组中某项 |
| [set_site_state_list_value](#set_site_state_list_value) | 设置SITE_STATE数组中某项 |
| [get_site_state_n_list](#get_site_state_n_list) | 生成n个值为v的SITE_STATE数组 |
| [get_coin_currency_list_value](#get_coin_currency_list_value) | 获取COIN_CURRENCY数组中某项 |

---

## set_cur_damage_is_miss

method in GameAPI

- 描述

    设置当前是否闪避

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_miss | boolean | 是否闪避 |

- 返回值

    无

- 示例

```lua
GameAPI.set_cur_damage_is_miss(true)
```

---

## set_cur_cure_value

method in GameAPI

- 描述

    设置当前治疗的数值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | py.Fixed | 治疗值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_cur_cure_value(Fix32(1))
```

---

## get_cur_damage_is_critical

method in GameAPI

- 描述

    获取当次攻击是否暴击

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | damage_result_state | integer | damage_result_state |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否暴击 |

- 示例

```lua
local result = GameAPI.get_cur_damage_is_critical(1)
```

---

## set_cur_damage_is_critical

method in GameAPI

- 描述

    设置当前是否暴击

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_critical | boolean | 是否暴击 |

- 返回值

    无

- 示例

```lua
GameAPI.set_cur_damage_is_critical(true)
```

---

## assign_behavior_tree

method in GameAPI

- 描述

    启动行为树

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | tree_name | string | 行为树名称 |
    | tree_args | py.Dict | 行为树参数 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local dict = pydict()

GameAPI.assign_behavior_tree(unit.handle, "tree_name", dict)
```

---

## stop_behavior_tree

method in GameAPI

- 描述

    停止一棵行为树

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | tree_name | string | 行为树名称 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.stop_behavior_tree(unit.handle, "tree_name")
```

---

## stop_all_behavior_tree

method in GameAPI

- 描述

    停止所有行为树

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.stop_all_behavior_tree(unit.handle)
```

---

## run_behavior_tree_once

method in GameAPI

- 描述

    运行一次行为树

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | tree_name | string | 行为树名称 |
    | tree_args | py.Dict | 行为树参数 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local dict = pydict()

GameAPI.run_behavior_tree_once(unit.handle, "tree_name", dict)
```

---

## unit_key_del_kv

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

GameAPI.unit_key_del_kv(unit_key, "key")
```

---

## ability_key_del_kv

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

GameAPI.ability_key_del_kv(ability_key, "key")
```

---

## item_key_del_kv

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

GameAPI.item_key_del_kv(item_key, "key")
```

---

## set_item_buy_price

method in GameAPI

- 描述

    设置物品商品售价

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_no | py.ItemKey | 物品编号 |
    | res_type | py.RoleResKey | 资源类型 |
    | price | number | 售价 |

- 返回值

    无

- 示例

```lua
local item_key = 134274569
local role_res_key = "res_key"

GameAPI.set_item_buy_price(item_key, role_res_key, 1.0)
```

---

## set_item_sell_price

method in GameAPI

- 描述

    设置物品商品出售资源获得

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_no | py.ItemKey | 物品编号 |
    | res_type | py.RoleResKey | 资源类型 |
    | price | number | 出售资源获得 |

- 返回值

    无

- 示例

```lua
local item_key = 134274569
local role_res_key = "res_key"

GameAPI.set_item_sell_price(item_key, role_res_key, 1.0)
```

---

## set_unit_buy_price

method in GameAPI

- 描述

    设置单位商品售价

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | entity_no | py.UnitKey | 单位编号 |
    | res_type | py.RoleResKey | 资源类型 |
    | price | number | 售价 |

- 返回值

    无

- 示例

```lua
local unit_key = 134274569
local role_res_key = "res_key"

GameAPI.set_unit_buy_price(unit_key, role_res_key, 1.0)
```

---

## set_unit_sell_price

method in GameAPI

- 描述

    设置单位商品出售资源获得

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | entity_no | py.UnitKey | 单位编号 |
    | res_type | py.RoleResKey | 资源类型 |
    | price | number | 出售资源获得 |

- 返回值

    无

- 示例

```lua
local unit_key = 134274569
local role_res_key = "res_key"

GameAPI.set_unit_sell_price(unit_key, role_res_key, 1.0)
```

---

## get_item_buy_price

method in GameAPI

- 描述

    获取物品商品售价

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_no | py.ItemKey | 物品编号 |
    | res_type | py.RoleResKey | 资源类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 售价 |

- 示例

```lua
local item_key = 134274569
local role_res_key = "res_key"

local result = GameAPI.get_item_buy_price(item_key, role_res_key)
```

---

## get_item_sell_price

method in GameAPI

- 描述

    获取物品商品出售资源获得

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_no | py.ItemKey | 物品编号 |
    | res_type | py.RoleResKey | 资源类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 出售资源获得 |

- 示例

```lua
local item_key = 134274569
local role_res_key = "res_key"

local result = GameAPI.get_item_sell_price(item_key, role_res_key)
```

---

## get_unit_buy_price

method in GameAPI

- 描述

    获取单位商品售价

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | entity_no | py.UnitKey | 单位编号 |
    | res_type | py.RoleResKey | 资源类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 售价 |

- 示例

```lua
local unit_key = 134274569
local role_res_key = "res_key"

local result = GameAPI.get_unit_buy_price(unit_key, role_res_key)
```

---

## get_unit_sell_price

method in GameAPI

- 描述

    获取单位商品出售资源获得

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | entity_no | py.UnitKey | 单位编号 |
    | res_type | py.RoleResKey | 资源类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 出售资源获得 |

- 示例

```lua
local unit_key = 134274569
local role_res_key = "res_key"

local result = GameAPI.get_unit_sell_price(unit_key, role_res_key)
```

---

## get_rec_center_point

method in GameAPI

- 描述

    返回矩形区域中心点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | rec | py.RecArea | 矩形区域 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3 | 中心点 |

- 示例

```lua
local rec_area = GameAPI.create_rec_area_from_two_points(Fix32Vec3(0, 0, 0), Fix32Vec3(100, 100, 0))

local result = GameAPI.get_rec_center_point(rec_area)
```

---

## get_circle_center_point

method in GameAPI

- 描述

    返回圆形区域中心点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | cir | py.CirArea | 圆形区域 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3 | 中心点 |

- 示例

```lua
local cir_area = GameAPI.create_new_cir_area(GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0)), Fix32(100))

local result = GameAPI.get_circle_center_point(cir_area)
```

---

## get_random_point_in_rec_area

method in GameAPI

- 描述

    返回矩形区域内随机点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.RecArea | 矩形区域 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3 | 随机点 |

- 示例

```lua
local rec_area = GameAPI.create_rec_area_from_two_points(Fix32Vec3(0, 0, 0), Fix32Vec3(100, 100, 0))

local result = GameAPI.get_random_point_in_rec_area(rec_area)
```

---

## get_random_point_in_circular_area

method in GameAPI

- 描述

    返回圆形区域内随机点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.CirArea | 圆形区域 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3 | 随机点 |

- 示例

```lua
local cir_area = GameAPI.create_new_cir_area(GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0)), Fix32(100))

local result = GameAPI.get_random_point_in_circular_area(cir_area)
```

---

## get_random_point_in_poly_area

method in GameAPI

- 描述

    返回多边形区域内随机点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.PolyArea | 不规则区域 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3 | 随机点 |

- 示例

```lua
local poly_area = GameAPI.create_polygon_area(Fix32Vec3(0, 0, 0), Fix32Vec3(100, 0, 0), Fix32Vec3(100, 100, 0))

local result = GameAPI.get_random_point_in_poly_area(poly_area)
```

---

## get_cir_area_last_created

method in GameAPI

- 描述

    最近创建的圆型区域

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CirArea | 圆型区域 |

- 示例

```lua
local result = GameAPI.get_cir_area_last_created()
```

---

## get_road_point_list_by_res_id

method in GameAPI

- 描述

    通过资源id返回路径

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | res_id | integer | 资源ID |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Road | 路径 |

- 示例

```lua
local result = GameAPI.get_road_point_list_by_res_id(1)
```

---

## create_road_point_list

method in GameAPI

- 描述

    在某点创建一条路径

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.Point | 点 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Road | 路径 |

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)

local result = GameAPI.create_road_point_list(point)
```

---

## remove_road_point_list

method in GameAPI

- 描述

    移除路径

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | road | py.Road | 路径 |

- 返回值

    无

- 示例

```lua
local road = y3.road.get_road_by_res_id(1)

GameAPI.remove_road_point_list(road.handle)
```

---

## add_road_point

method in GameAPI

- 描述

    给路径添加点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | road | py.Road | 路径 |
    | num | integer | 序号 |
    | point | py.Point | 点 |

- 返回值

    无

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)
local road = y3.road.get_road_by_res_id(1)

GameAPI.add_road_point(road.handle, 1, point)
```

---

## remove_road_point

method in GameAPI

- 描述

    移除路径点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | road | py.Road | 路径 |
    | num | integer | 序号 |

- 返回值

    无

- 示例

```lua
local road = y3.road.get_road_by_res_id(1)

GameAPI.remove_road_point(road.handle, 1)
```

---

## get_road_point_start_point

method in GameAPI

- 描述

    获取路径的【起点】

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | road_point_list | py.Road | 路径 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3 | 起点 |

- 示例

```lua
local road = y3.road.get_road_by_res_id(1)

local result = GameAPI.get_road_point_start_point(road.handle)
```

---

## get_road_point_end_point

method in GameAPI

- 描述

    获取路径的【终点】

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | road_point_list | py.Road | 路径 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3 | 终点 |

- 示例

```lua
local road = y3.road.get_road_by_res_id(1)

local result = GameAPI.get_road_point_end_point(road.handle)
```

---

## get_road_point_random_point

method in GameAPI

- 描述

    获取路径的【随机点】

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | road_point_list | py.Road | 路径 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3 | 随机点 |

- 示例

```lua
local road = y3.road.get_road_by_res_id(1)

local result = GameAPI.get_road_point_random_point(road.handle)
```

---

## get_nearest_road_point_list_by_pos

method in GameAPI

- 描述

    获取某点的最近路径

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.Point | 位置 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Road | 路径 |

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)

local result = GameAPI.get_nearest_road_point_list_by_pos(point)
```

---

## get_road_point_list_by_offset

method in GameAPI

- 描述

    获取某路径偏移后的路径

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | origin_roads | py.Road | 原始路径 |
    | offset | py.Fixed | 偏移距离 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Road | 路径 |

- 示例

```lua
local road = y3.road.get_road_by_res_id(1)

local result = GameAPI.get_road_point_list_by_offset(road.handle, Fix32(1))
```

---

## get_road_point_list_loop

method in GameAPI

- 描述

    获取某路径循环n次后的路径

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point_list | py.Road | 原始路径 |
    | n | integer | 循环次数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Road | 路径 |

- 示例

```lua
local road = y3.road.get_road_by_res_id(1)

local result = GameAPI.get_road_point_list_loop(road.handle, 1)
```

---

## get_road_point_list_join

method in GameAPI

- 描述

    获取两路径拼接后的路径

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | pl1 | py.Road | 原始路径 |
    | pl2 | py.Road | 原始路径 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Road | 路径 |

- 示例

```lua
local road = y3.road.get_road_by_res_id(1)

local result = GameAPI.get_road_point_list_join(road.handle, road.handle)
```

---

## get_road_point_list_inversion

method in GameAPI

- 描述

    获取某路径反转后的路径

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point_list | py.Road | 原始路径 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Road | 路径 |

- 示例

```lua
local road = y3.road.get_road_by_res_id(1)

local result = GameAPI.get_road_point_list_inversion(road.handle)
```

---

## get_road_point_num

method in GameAPI

- 描述

    获取路径中点的数量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | road_point_list | py.Road | 路径 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 数量 |

- 示例

```lua
local road = y3.road.get_road_by_res_id(1)

local result = GameAPI.get_road_point_num(road.handle)
```

---

## get_last_created_unit

method in GameAPI

- 描述

    最近创建单位实体

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 单位实体 |

- 示例

```lua
local result = GameAPI.get_last_created_unit()
```

---

## get_last_created_trigger

method in GameAPI

- 描述

    最近创建子触发器

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DynamicTriggerInstance | 子触发器ID |

- 示例

```lua
local result = GameAPI.get_last_created_trigger()
```

---

## get_last_created_projectile

method in GameAPI

- 描述

    最近创建投射物

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 投射物 |

- 示例

```lua
local result = GameAPI.get_last_created_projectile()
```

---

## get_unit_group_in_area

method in GameAPI

- 描述

    得到区域内的单位id列表

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.Area | 区域对象 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 单位ID列表 |

- 示例

```lua
local area = y3.area.create_circle_area(y3.point.create(0, 0, 0), 500)

local result = GameAPI.get_unit_group_in_area(area.handle)
```

---

## get_unit_group_belong_to_player_in_area

method in GameAPI

- 描述

    获取区域内玩家所有单位id列表

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.Area | 区域对象 |
    | role | py.Role | 玩家 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitGroup | 单位id列表 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local area = y3.area.create_circle_area(y3.point.create(0, 0, 0), 500)

local result = GameAPI.get_unit_group_belong_to_player_in_area(area.handle, player.handle)
```

---

## get_item_group_in_area

method in GameAPI

- 描述

    得到区域内的物品对象id列表

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.Area | 区域对象 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemGroup | 物品组 |

- 示例

```lua
local area = y3.area.create_circle_area(y3.point.create(0, 0, 0), 500)

local result = GameAPI.get_item_group_in_area(area.handle)
```

---

## get_all_items_in_shapes

method in GameAPI

- 描述

    获取指定形状内的所有物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.Point | 区域对象 |
    | shape | py.Shape | 形状 |
    | sort_type? | py.SortType | 排序类型 |
    | filter_ability? | py.Ability | 筛选技能 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemGroup | 物品组 |

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)
local shape = GlobalAPI.create_circular_shape(Fix32(500))

local result = GameAPI.get_all_items_in_shapes(point, shape, 1)
```

---

## send_ui_global_event_with_info_dict

method in GameAPI

- 描述

    向ui发送附带dict的事件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | s | string | 事件名称 |
    | args | py.Dict | 参数 |

- 返回值

    无

- 示例

```lua
local dict = pydict()

GameAPI.send_ui_global_event_with_info_dict("s", dict)
```

---

## add_unit_to_group

method in GameAPI

- 描述

    添加单位到单位组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | unit_group | py.UnitGroup | 单位组 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local unit_group = y3.unit_group.create()

GameAPI.add_unit_to_group(unit.handle, unit_group.handle)
```

---

## set_trigger_table_list_variable

method in GameAPI

- 描述

    批量设置全局触发器数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | table | py.List | 组合列表，格式为[[数组变量名称，类型（'INTEGER', 'BOOLEAN', 'FLOAT', 'STRING'），列表值（[值，值，......]）],[.....]] |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_trigger_table_list_variable(list)
```

---

## set_trigger_str_list_by_split

method in GameAPI

- 描述

    通过分割字符串设置字符串数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | py.List | 字符串数组 |
    | actor | py.Actor | 类型提示 |
    | content | string | 分割内容 |
    | split | string | 分割符 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local list = {}

GameAPI.set_trigger_str_list_by_split(list, actor, "content", "split")
```

---

## create_trigger_list_variable

method in GameAPI

- 描述

    创建全局触发器数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 数组变量名称 |
    | var_type | string | 值类型 |
    | arr_val | py.List | 列表型值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.create_trigger_list_variable("key", "var_type", list)
```

---

## unit_key_has_tag

method in GameAPI

- 描述

    单位编号是否拥有tag

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | py.UnitKey | 单位编号 |
    | tag | string | tag |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 布尔值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.unit_key_has_tag(unit_key, "tag")
```

---

## item_key_has_tag

method in GameAPI

- 描述

    物品编号是否拥有tag

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | py.ItemKey | 物品编号 |
    | tag | string | tag |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 布尔值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.item_key_has_tag(item_key, "tag")
```

---

## ability_key_has_tag

method in GameAPI

- 描述

    技能编号是否拥有tag

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | py.AbilityKey | 技能编号 |
    | tag | string | tag |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 布尔值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.ability_key_has_tag(ability_key, "tag")
```

---

## modifier_key_has_tag

method in GameAPI

- 描述

    效果编号是否拥有tag

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | py.AbilityKey | 技能编号 |
    | tag | string | tag |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 布尔值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.modifier_key_has_tag(ability_key, "tag")
```

---

## projectile_key_has_tag

method in GameAPI

- 描述

    投射物编号是否拥有tag

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | py.AbilityKey | 投射物编号 |
    | tag | string | tag |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 布尔值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.projectile_key_has_tag(ability_key, "tag")
```

---

## dest_key_has_tag

method in GameAPI

- 描述

    可破坏物编号是否拥有tag

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | py.DestructibleKey | 可破坏物编号 |
    | tag | string | tag |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 布尔值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.dest_key_has_tag(destructible_key, "tag")
```

---

## unit_is_exist

method in GameAPI

- 描述

    单位实体是否存在

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit? | py.Unit | 单位实体 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 布尔值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = GameAPI.unit_is_exist()
```

---

## modifier_is_exist

method in GameAPI

- 描述

    效果实体是否存在

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier? | py.ModifierEntity | 效果实体 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 布尔值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

local result = GameAPI.modifier_is_exist()
```

---

## projectile_is_exist

method in GameAPI

- 描述

    投射物实体是否存在

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile? | py.ProjectileEntity | 投射物 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 布尔值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local target_point = unit:get_point()
local projectile = y3.projectile.create({ key = 134274569, target = target_point })

local result = GameAPI.projectile_is_exist()
```

---

## ability_is_exist

method in GameAPI

- 描述

    技能实体是否存在

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability? | py.Ability | 技能 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 布尔值 |

- 示例

```lua
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = GameAPI.ability_is_exist()
```

---

## destructible_is_exist

method in GameAPI

- 描述

    可破坏物是否存在

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible? | py.Destructible | 可破坏物 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 布尔值 |

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

local result = GameAPI.destructible_is_exist()
end
```

---

## item_is_exist

method in GameAPI

- 描述

    图片是否存在

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item? | py.Item | 图片key |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 布尔值 |

- 示例

```lua
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = GameAPI.item_is_exist()
```

---

## unit_group_is_exist

method in GameAPI

- 描述

    单位组是否存在

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_group | py.UnitGroup | 单位组 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit_group = y3.unit_group.create()

local result = GameAPI.unit_group_is_exist(unit_group.handle)
```

---

## role_group_is_exist

method in GameAPI

- 描述

    玩家组是否存在

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role_group | py.RoleGroup | 玩家组 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local player_group = y3.player_group.create()

local result = GameAPI.role_group_is_exist(player_group.handle)
```

---

## sfx_is_exist

method in GameAPI

- 描述

    特效是否存在

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | sfx | py.Sfx | 特效 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local sfx = y3.particle.create({ type = 134274569, target = y3.point(0, 0) }).handle

local result = GameAPI.sfx_is_exist(sfx)
```

---

## point_is_exist

method in GameAPI

- 描述

    点是否存在

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.Point | 点 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)

local result = GameAPI.point_is_exist(point)
```

---

## point_list_is_exist

method in GameAPI

- 描述

    路径是否存在

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point_list | py.Road | 路径 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local road = y3.road.get_road_by_res_id(1)

local result = GameAPI.point_list_is_exist(road.handle)
```

---

## circle_area_is_exist

method in GameAPI

- 描述

    圆形区域是否存在

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | circle_area | py.CirArea | 圆形区域 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local cir_area = GameAPI.create_new_cir_area(GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0)), Fix32(100))

local result = GameAPI.circle_area_is_exist(cir_area)
```

---

## rect_area_is_exist

method in GameAPI

- 描述

    矩形区域是否存在

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | rect_area | py.RecArea | 矩形区域 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local rec_area = GameAPI.create_rec_area_from_two_points(Fix32Vec3(0, 0, 0), Fix32Vec3(100, 100, 0))

local result = GameAPI.rect_area_is_exist(rec_area)
```

---

## camera_is_exist

method in GameAPI

- 描述

    镜头是否存在

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | camera | py.Camera | 镜头 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local camera = y3.camera.create_camera(y3.point(0, 0), 1000, 500, 0, 45, 3000)

local result = GameAPI.camera_is_exist(camera.handle)
```

---

## get_ability_max_level

method in GameAPI

- 描述

    获取技能最大等级

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability | py.Ability | 技能 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 最大等级 |

- 示例

```lua
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = GameAPI.get_ability_max_level(ability.handle)
```

---

## random_list_from_list

method in GameAPI

- 描述

    列表中返回随机整数个元素组成的列表

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | list1 | py.List | 列表 |
    | n | integer | 整数个 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 随机生成的列表 |

- 示例

```lua
local list = {}

local result = GameAPI.random_list_from_list(list, 1)
```

---

## shake_phone

method in GameAPI

- 描述

    震动设备

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | time | py.Fixed | 震动时间 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.shake_phone(player.handle, Fix32(1))
```

---

## set_role_rank_score

method in GameAPI

- 描述

    为<玩家>输入排行榜<分数>

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | score | integer | 战斗内排行榜分数 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_role_rank_score(player.handle, 1)
```

---

## unit_send_global_event_with_info

method in GameAPI

- 描述

    单位触发器向全局触发器发送事件, 附带信息

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | event_name | string | 事件名称 |
    | i | integer | 整型值 |
    | f | py.Fixed | 定点型值 |
    | b | boolean | 布尔型值 |
    | s | string | 字符串型值 |
    | p | py.Point | 浮点数点型值 |
    | u? | py.Unit | 单位对象 |

- 返回值

    无

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.unit_send_global_event_with_info("event_name", 1, Fix32(1), true, "s", point)
```

---

## ability_send_global_event_with_info

method in GameAPI

- 描述

    技能触发器向全局触发器发送事件, 附带信息

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | event_name | string | 事件名称 |
    | i | integer | 整型值 |
    | f | py.Fixed | 定点型值 |
    | b | boolean | 布尔型值 |
    | s | string | 字符串型值 |
    | p | py.Point | 浮点数点型值 |
    | u? | py.Unit | 单位对象 |

- 返回值

    无

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.ability_send_global_event_with_info("event_name", 1, Fix32(1), true, "s", point)
```

---

## modifier_send_global_event_with_info

method in GameAPI

- 描述

    效果触发器向全局触发器发送事件, 附带信息

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | event_name | string | 事件名称 |
    | i | integer | 整型值 |
    | f | py.Fixed | 定点型值 |
    | b | boolean | 布尔型值 |
    | s | string | 字符串型值 |
    | p | py.Point | 浮点数点型值 |
    | u? | py.Unit | 单位对象 |

- 返回值

    无

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.modifier_send_global_event_with_info("event_name", 1, Fix32(1), true, "s", point)
```

---

## projectile_send_global_event_with_info

method in GameAPI

- 描述

    投射物触发器向全局触发器发送事件, 附带信息

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | event_name | string | 事件名称 |
    | i | integer | 整型值 |
    | f | py.Fixed | 定点型值 |
    | b | boolean | 布尔型值 |
    | s | string | 字符串型值 |
    | p | py.Point | 浮点数点型值 |
    | u? | py.Unit | 单位对象 |

- 返回值

    无

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.projectile_send_global_event_with_info("event_name", 1, Fix32(1), true, "s", point)
```

---

## item_send_global_event_with_info

method in GameAPI

- 描述

    物品触发器向全局触发器发送事件, 附带信息

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | event_name | string | 事件名称 |
    | i | integer | 整型值 |
    | f | py.Fixed | 定点型值 |
    | b | boolean | 布尔型值 |
    | s | string | 字符串型值 |
    | p | py.Point | 浮点数点型值 |
    | u? | py.Unit | 单位对象 |

- 返回值

    无

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.item_send_global_event_with_info("event_name", 1, Fix32(1), true, "s", point)
```

---

## get_player_nick_name

method in GameAPI

- 描述

    获取[玩家]的玩家昵称

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 玩家昵称 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_player_nick_name(player.handle)
```

---

## get_player_full_nick_name

method in GameAPI

- 描述

    获取[玩家]的玩家全量昵称

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 玩家全量昵称 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_player_full_nick_name(player.handle)
```

---

## get_player_plat_aid

method in GameAPI

- 描述

    获取[玩家]的玩家aid

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 玩家aid |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_player_plat_aid(player.handle)
```

---

## get_player_icon

method in GameAPI

- 描述

    获取[玩家]的玩家图像

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 玩家图像 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_player_icon(player.handle)
```

---

## filter_unit_status

method in GameAPI

- 描述

    筛选单位删除状态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit? | py.Unit | 单位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 有效单位对象 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = GameAPI.filter_unit_status()
```

---

## open_charge_item_store_for_role

method in GameAPI

- 描述

    为玩家打开收费道具商店

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.open_charge_item_store_for_role(player.handle)
```

---

## get_cur_game_time

method in GameAPI

- 描述

    当前游戏运行时间

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 时间 |

- 示例

```lua
local result = GameAPI.get_cur_game_time()
```

---

## can_point_reach_point

method in GameAPI

- 描述

    检查点到点是否联通

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 寻路单位 |
    | pointa | py.Point | 起点 |
    | pointb | py.Point | 终点 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否联通 |

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = GameAPI.can_point_reach_point(unit.handle, point, point)
```

---

## unit_can_collide_with_point

method in GameAPI

- 描述

    检测点是否和单位碰撞

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | point | py.Point | 点 |
    | radius | number | 范围 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否碰撞 |

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = GameAPI.unit_can_collide_with_point(unit.handle, point, 1.0)
```

---

## api_get_ability_by_seq

method in GameAPI

- 描述

    通过技能序列号获取技能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | ability_seq | py.AbilitySeq | 技能序列号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Ability | 技能对象 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = GameAPI.api_get_ability_by_seq(unit.handle, 1)
```

---

## api_get_ability_by_unit_and_seq

method in GameAPI

- 描述

    通过单位编号+技能序列号获取技能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_id | py.UnitID | 单位ID |
    | ability_seq | py.AbilitySeq | 技能序列号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Ability | 技能对象 |

- 示例

```lua
local unit_id = 134274569

local result = GameAPI.api_get_ability_by_unit_and_seq(unit_id, 1)
```

---

## get_damage_statistic_rank_unit

method in GameAPI

- 描述

    获取【单位组】中伤害排名【整数】的单位实体

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_group | py.UnitGroup | 单位组 |
    | rank | integer | 排名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 单位 |

- 示例

```lua
local unit_group = y3.unit_group.create()

local result = GameAPI.get_damage_statistic_rank_unit(unit_group.handle, 1)
```

---

## get_select_circle_scale

method in GameAPI

- 描述

    获取选择圈缩放

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 缩放 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = GameAPI.get_select_circle_scale(unit.handle)
```

---

## delete_model_entity

method in GameAPI

- 描述

    删除模型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | model | py.Model | 模型 |

- 返回值

    无

- 示例

```lua
GameAPI.delete_model_entity(1)
```

---

## create_model_on_point

method in GameAPI

- 描述

    创建展示模型，面向点，朝向实数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | model_res_id | py.ModelKey | 模型名称 |
    | position | py.Point | 点 |
    | rotation | number | 朝向 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Model | 模型 |

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)
local model_key = 1

local result = GameAPI.create_model_on_point(model_key, point, 1.0)
```

---

## create_model_in_scene

method in GameAPI

- 描述

    创建模型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | model_key | py.ModelKey | 模型编号 |
    | pos | py.FPoint | 点 |
    | face | py.Fixed | 朝向 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Model | 模型 |

- 示例

```lua
local model_key = 1
local fpoint = GameAPI.get_point_by_res_id(1)

local result = GameAPI.create_model_in_scene(model_key, fpoint, Fix32(1))
```

---

## destroy_model_in_scene

method in GameAPI

- 描述

    销毁模型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | model? | py.Model | 模型 |

- 返回值

    无

- 示例

```lua
GameAPI.destroy_model_in_scene(1)
```

---

## get_item_key_str_attr

method in GameAPI

- 描述

    返回指定物品名字的字符串属性值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | py.ItemKey | 物品编号 |
    | name | string | 属性名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_str_attr(item_key, "name")
```

---

## role_force_quit

method in GameAPI

- 描述

    强制踢出玩家

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | reason | string | 踢出理由 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.role_force_quit(player.handle, "reason")
```

---

## set_rect_vision_visibility

method in GameAPI

- 描述

    设置矩形区域内视野情况

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | rect_area | py.RecArea | 矩形区域 |
    | player | py.Role | 玩家 |
    | is_vision | boolean | 布尔变量 |
    | is_vision_true | boolean | 布尔变量 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RecArea | 矩形区域 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local rec_area = GameAPI.create_rec_area_from_two_points(Fix32Vec3(0, 0, 0), Fix32Vec3(100, 100, 0))

local result = GameAPI.set_rect_vision_visibility(rec_area, player.handle, true, true)
```

---

## set_fog_state

method in GameAPI

- 描述

    设置区域内视野情况

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.Area | 区域 |
    | player | py.Role | 玩家 |
    | fog_state | integer | 迷雾状态 |
    | is_vision_true | boolean | 布尔变量 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local area = y3.area.create_circle_area(y3.point.create(0, 0, 0), 500)

GameAPI.set_fog_state(area.handle, player.handle, 1, true)
```

---

## set_circle_vision_visibility

method in GameAPI

- 描述

    设置圆形区域内视野情况

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | circle_area | py.CirArea | 圆形区域 |
    | player | py.Role | 玩家 |
    | is_vision | boolean | 布尔变量 |
    | is_vision_true | boolean | 布尔变量 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CirArea | 圆形区域 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local cir_area = GameAPI.create_new_cir_area(GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0)), Fix32(100))

local result = GameAPI.set_circle_vision_visibility(cir_area, player.handle, true, true)
```

---

## set_poly_vision_visibility

method in GameAPI

- 描述

    设置多边形区域内视野情况

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | poly_area | py.PolyArea | 多边形区域 |
    | player | py.Role | 玩家 |
    | is_vision | boolean | 布尔变量 |
    | is_vision_true | boolean | 布尔变量 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PolyArea | 多边形区域 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local poly_area = GameAPI.create_polygon_area(Fix32Vec3(0, 0, 0), Fix32Vec3(100, 0, 0), Fix32Vec3(100, 100, 0))

local result = GameAPI.set_poly_vision_visibility(poly_area, player.handle, true, true)
```

---

## create_random_pool

method in GameAPI

- 描述

    创建随机池

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RandomPool | 随机池 |

- 示例

```lua
local result = GameAPI.create_random_pool()
```

---

## set_random_pool_value

method in GameAPI

- 描述

    设置随机池指定整数权重

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | random_pool | py.RandomPool | 随机池 |
    | value | integer | 整型 |
    | weight | integer | 整型 |

- 返回值

    无

- 示例

```lua
local random_pool = GameAPI.create_random_pool()

GameAPI.set_random_pool_value(random_pool, 1, 1)
```

---

## increase_random_pool_value

method in GameAPI

- 描述

    随机池增加指定整数权重

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | random_pool | py.RandomPool | 随机池 |
    | value | integer | 整型 |
    | increment | integer | 整型 |

- 返回值

    无

- 示例

```lua
local random_pool = GameAPI.create_random_pool()

GameAPI.increase_random_pool_value(random_pool, 1, 1)
```

---

## remove_random_pool_value

method in GameAPI

- 描述

    随机池移除指定整数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | random_pool | py.RandomPool | 随机池 |
    | value | integer | 整型 |

- 返回值

    无

- 示例

```lua
local random_pool = GameAPI.create_random_pool()

GameAPI.remove_random_pool_value(random_pool, 1)
```

---

## get_bitrary_random_pool_value

method in GameAPI

- 描述

    从随机池中获取一个随机整数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | random_pool | py.RandomPool | 随机池 |
    | remain? | boolean | 布尔 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 整数 |

- 示例

```lua
local random_pool = GameAPI.create_random_pool()

local result = GameAPI.get_bitrary_random_pool_value(random_pool, true)
```

---

## get_random_pool_probability

method in GameAPI

- 描述

    获取随机池中指定整数的权重概率

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | random_pool | py.RandomPool | 随机池 |
    | value | integer | 整数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 权重概率 |

- 示例

```lua
local random_pool = GameAPI.create_random_pool()

local result = GameAPI.get_random_pool_probability(random_pool, 1)
```

---

## get_random_pool_all_weight

method in GameAPI

- 描述

    获取随机池中指定整数的权重概率

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | random_pool | py.RandomPool | 随机池 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 总权重 |

- 示例

```lua
local random_pool = GameAPI.create_random_pool()

local result = GameAPI.get_random_pool_all_weight(random_pool)
```

---

## get_random_pool_size

method in GameAPI

- 描述

    获取随机池中的整数数量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | random_pool | py.RandomPool | 随机池 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 整数数量 |

- 示例

```lua
local random_pool = GameAPI.create_random_pool()

local result = GameAPI.get_random_pool_size(random_pool)
```

---

## copy_random_pool

method in GameAPI

- 描述

    复制随机池

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | random_pool | py.RandomPool | 随机池 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RandomPool | 随机池 |

- 示例

```lua
local random_pool = GameAPI.create_random_pool()

local result = GameAPI.copy_random_pool(random_pool)
```

---

## api_get_attr_growth

method in GameAPI

- 描述

    成长属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | entity_no | py.UnitKey | 单位编号 |
    | attr | string | 属性名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 属性值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.api_get_attr_growth(unit_key, "attr")
```

---

## api_set_attr_growth

method in GameAPI

- 描述

    设置成长属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | entity_no | py.UnitKey | 单位编号 |
    | attr | string | 属性名 |
    | value | py.Fixed | 属性值 |

- 返回值

    无

- 示例

```lua
local unit_key = 134274569

GameAPI.api_set_attr_growth(unit_key, "attr", Fix32(1))
```

---

## get_all_random_pool_value

method in GameAPI

- 描述

    获取某个随机池的列表

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | random_pool | py.RandomPool | 随机池 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 整数 |

- 示例

```lua
local random_pool = GameAPI.create_random_pool()

local result = GameAPI.get_all_random_pool_value(random_pool)
```

---

## get_random_pool_pointed_weight

method in GameAPI

- 描述

    获取某个随机池中指定整数的权重

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | random_pool | py.RandomPool | 随机池 |
    | value | integer | 整数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 整数 |

- 示例

```lua
local random_pool = GameAPI.create_random_pool()

local result = GameAPI.get_random_pool_pointed_weight(random_pool, 1)
```

---

## get_text_config

method in GameAPI

- 描述

    翻译字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | string | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 翻译后的字符串 |

- 示例

```lua
local result = GameAPI.get_text_config("string")
```

---

## send_custom_event

method in GameAPI

- 描述

    发送触发器自定义事件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | event_name | string | 自定义事件名称 |
    | p1 | integer | 参数1 |
    | p2 | integer | 参数2 |
    | p3 | integer | 参数3 |
    | p4 | integer | 参数4 |
    | p5 | integer | 参数5 |

- 返回值

    无

- 示例

```lua
GameAPI.send_custom_event("event_name", 1, 1, 1, 1, 1)
```

---

## get_icon_id

method in GameAPI

- 描述

    获取icon图标的图片id

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | parameter | py.Actor | 对象 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 图片id |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_icon_id(actor)
```

---

## get_icon_id_by_ability_type

method in GameAPI

- 描述

    获取技能icon图标的图片id

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | py.AbilityKey | 技能编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 图片id |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_icon_id_by_ability_type(ability_key)
```

---

## get_icon_id_by_item_type

method in GameAPI

- 描述

    获取物品icon图标的图片id

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | py.ItemKey | 物品编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 图片id |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_icon_id_by_item_type(item_key)
```

---

## get_icon_id_by_unit_type

method in GameAPI

- 描述

    获取单位icon图标的图片id

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | py.UnitKey | 单位编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 图片id |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_icon_id_by_unit_type(unit_key)
```

---

## get_icon_id_by_buff_type

method in GameAPI

- 描述

    获取魔法效果icon图标的图片id

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | py.ModifierKey | 魔法效果编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 图片id |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_icon_id_by_buff_type(modifier_key)
```

---

## is_show_on_ui_by_buff_type

method in GameAPI

- 描述

    获取魔法效果类型图标的可见性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | py.ModifierKey | 魔法效果编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 布尔值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.is_show_on_ui_by_buff_type(modifier_key)
```

---

## create_harm_text

method in GameAPI

- 描述

    生成漂浮文字

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.Point | 点 |
    | text_type | string | 跳字枚举 |
    | value | string | 跳字内容 |
    | player_group | py.RoleGroup | 玩家组 |
    | jump_word_track? | integer | 跳字轨迹 |

- 返回值

    无

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)
local player_group = y3.player_group.create()

GameAPI.create_harm_text(point, "text_type", "value", player_group.handle, 1)
```

---

## player_key_is_pressed

method in GameAPI

- 描述

    玩家是否按下按键

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | key | py.KeyboardKey | 键盘按键 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 按下状态 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.player_key_is_pressed(player.handle, 1)
```

---

## get_player_pointing_pos

method in GameAPI

- 描述

    玩家鼠标位置

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Point | 鼠标位置 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_player_pointing_pos(player.handle)
```

---

## get_player_ui_pos_x

method in GameAPI

- 描述

    玩家鼠标屏幕位置X

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 鼠标屏幕位置X |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_player_ui_pos_x(player.handle)
```

---

## get_player_ui_pos_y

method in GameAPI

- 描述

    玩家鼠标屏幕位置Y

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 鼠标屏幕位置Y |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_player_ui_pos_y(player.handle)
```

---

## get_player_camera_direction

method in GameAPI

- 描述

    玩家摄像机朝向

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Point | 摄像机朝向 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_player_camera_direction(player.handle)
```

---

## get_camera_center_raycast

method in GameAPI

- 描述

    玩家摄像机中心射线检测

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Point | 交点 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_camera_center_raycast(player.handle)
```

---

## get_role_ui_x_per

method in GameAPI

- 描述

    玩家鼠标屏幕位置X的窗口占比

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 占比值 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_role_ui_x_per(player.handle)
```

---

## get_role_ui_y_per

method in GameAPI

- 描述

    玩家鼠标屏幕位置Y的窗口占比

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 占比值 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_role_ui_y_per(player.handle)
```

---

## get_unit_name_by_type

method in GameAPI

- 描述

    返回指定单位类型的名称

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 描述 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_name_by_type(unit_key)
```

---

## get_unit_desc_by_type

method in GameAPI

- 描述

    返回指定单位类型的描述

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 描述 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_desc_by_type(unit_key)
```

---

## get_role_attr_by_unit_type

method in GameAPI

- 描述

    获取单位类型建造资源消耗属性(玩家属性)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位类型 |
    | role_res_key | py.RoleResKey | 玩家属性 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 玩家属性值 |

- 示例

```lua
local unit_key = 134274569
local role_res_key = "res_key"

local result = GameAPI.get_role_attr_by_unit_type(unit_key, role_res_key)
```

---

## get_dest_name_by_type

method in GameAPI

- 描述

    返回指定可破坏物类型的名称

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | dest_key | py.DestructibleKey | 可破坏物ID |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 描述 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_dest_name_by_type(destructible_key)
```

---

## get_dest_desc_by_type

method in GameAPI

- 描述

    返回指定可破坏物类型的描述

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | dest_key | py.DestructibleKey | 可破坏物ID |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 描述 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_dest_desc_by_type(destructible_key)
```

---

## get_projectile_name_by_type

method in GameAPI

- 描述

    返回指定投射物类型的名称

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 投射物ID |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 描述 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_name_by_type(projectile_key)
```

---

## get_projectile_desc_by_type

method in GameAPI

- 描述

    返回指定投射物类型的描述

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 投射物ID |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 描述 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_desc_by_type(projectile_key)
```

---

## get_item_desc_by_type

method in GameAPI

- 描述

    返回指定物品类型的描述

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品ID |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 描述 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_desc_by_type(item_key)
```

---

## get_ability_desc_by_type

method in GameAPI

- 描述

    返回指定技能类型的描述

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能ID |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 描述 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_desc_by_type(ability_key)
```

---

## get_ability_name_by_type

method in GameAPI

- 描述

    返回指定技能类型的名称

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能ID |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 名称 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_name_by_type(ability_key)
```

---

## get_tech_name_by_type

method in GameAPI

- 描述

    返回指定科技类型的名称

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技ID |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 名称 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_name_by_type(tech_key)
```

---

## get_tech_desc_by_type

method in GameAPI

- 描述

    返回指定科技类型的描述

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技ID |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 描述 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_desc_by_type(tech_key)
```

---

## get_modifier_name_by_type

method in GameAPI

- 描述

    返回指定魔法效果类型的名称

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果ID |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 描述 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_name_by_type(modifier_key)
```

---

## get_modifier_desc_by_type

method in GameAPI

- 描述

    返回指定魔法效果类型的描述

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果ID |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 描述 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_desc_by_type(modifier_key)
```

---

## get_item_name_by_type

method in GameAPI

- 描述

    返回指定物品类型的名字

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品ID |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 名字 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_name_by_type(item_key)
```

---

## block_global_key_event

method in GameAPI

- 描述

    屏蔽全局键盘事件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | block | boolean | 是否屏蔽 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.block_global_key_event(player.handle, true)
```

---

## block_global_mouse_event

method in GameAPI

- 描述

    屏蔽全局鼠标事件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | block | boolean | 是否屏蔽 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.block_global_mouse_event(player.handle, true)
```

---

## block_trigger_key_event

method in GameAPI

- 描述

    屏蔽触发器键盘事件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | block | boolean | 是否屏蔽 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.block_trigger_key_event(player.handle, true)
```

---

## block_trigger_mouse_event

method in GameAPI

- 描述

    屏蔽触发器鼠标事件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | block | boolean | 是否屏蔽 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.block_trigger_mouse_event(player.handle, true)
```

---

## get_role_res_icon

method in GameAPI

- 描述

    获取玩家属性Icon

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | res_key | py.RoleResKey | 玩家属性 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 图片ID |

- 示例

```lua
local role_res_key = "res_key"

local result = GameAPI.get_role_res_icon(role_res_key)
```

---

## get_role_res_name

method in GameAPI

- 描述

    获取玩家属性名称

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | res_key | py.RoleResKey | 玩家属性 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 属性名称 |

- 示例

```lua
local role_res_key = "res_key"

local result = GameAPI.get_role_res_name(role_res_key)
```

---

## draw_grid_polyline

method in GameAPI

- 描述

    (调试)绘制网格线

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | start_x | number | 起点x |
    | start_y | number | 起点y |
    | height | number | 高度 |
    | space | number | 间距 |
    | line_count | integer | 线数 |
    | r | integer | r |
    | g | integer | g |
    | b | integer | b |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.draw_grid_polyline(player.handle, 1.0, 1.0, 1.0, 1.0, 1, 1, 1, 1)
```

---

## draw_polyline

method in GameAPI

- 描述

    (调试)绘线

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point_list | py.List | 点 |
    | height | number | 高度 |
    | r | integer | r |
    | g | integer | g |
    | b | integer | b |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 索引 |

- 示例

```lua
local list = {}

local result = GameAPI.draw_polyline(list, 1.0, 1, 1, 1)
```

---

## draw_box

method in GameAPI

- 描述

    (调试)绘制矩形

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point_list | py.List | 点 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.draw_box(list)
```

---

## hide_all_rect

method in GameAPI

- 描述

    (调试)隐藏所有矩形

- 参数

    无

- 返回值

    无

- 示例

```lua
GameAPI.hide_all_rect()
```

---

## clear_grid_polyline

method in GameAPI

- 描述

    (调试)清除调试绘线

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | index | integer | 索引 |

- 返回值

    无

- 示例

```lua
GameAPI.clear_grid_polyline(1)
```

---

## set_billboard_font_size

method in GameAPI

- 描述

    (调试)设置billboard字体大小

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | size | integer | 大小 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_billboard_font_size(player.handle, 1)
```

---

## set_mouse_click_control_move

method in GameAPI

- 描述

    设置鼠标关闭右键点击移动

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | b | boolean | 开关 |

- 返回值

    无

- 示例

```lua
GameAPI.set_mouse_click_control_move(true)
```

---

## iter_role_res

method in GameAPI

- 描述

    遍历所有玩家的资源属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_iter_coin_only | boolean | 是否遍历货币类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 资源属性列表 |

- 示例

```lua
local result = GameAPI.iter_role_res(true)
```

---

## create_scene_node_on_point

method in GameAPI

- 描述

    创建场景点并绑定UI到点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | comp_name | string | 控件名 |
    | point | py.Point | 点 |
    | visible_dis? | number | 可见距离 |
    | height_offset? | number | 离地高度 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SceneNode | 场景点 |

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)

local result = GameAPI.create_scene_node_on_point("comp_name", point, 1.0, 1.0)
```

---

## create_scene_node_on_unit

method in GameAPI

- 描述

    创建场景点并绑定UI到单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | comp_name | string | 控件名 |
    | player | py.Role | 玩家 |
    | unit | py.Unit | 单位 |
    | socket_name | string | 挂接点 |
    | visible_dis? | number | 可见距离 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SceneNode | 场景点 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

local result = GameAPI.create_scene_node_on_unit("comp_name", player.handle, unit.handle, "socket_name", 1.0)
```

---

## create_scene_node_on_3d

method in GameAPI

- 描述

    创建场景点并绑定UI到三维坐标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | comp_name | string | 控件名 |
    | position | py.Vector3 | 三维坐标 |
    | visible_dis? | number | 可见距离 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SceneNode | 场景点 |

- 示例

```lua
local vector3 = Fix32Vec3(0, 0, 0)

local result = GameAPI.create_scene_node_on_3d("comp_name", vector3, 1.0)
```

---

## create_scene_node_on_rigid_body

method in GameAPI

- 描述

    创建场景界面到刚体

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | comp_name | string | 控件名 |
    | body | py.RigidBody | 刚体 |
    | offset | py.Vector3 | 偏移量 |
    | visible_dis? | number | 可见距离 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SceneNode | 场景点 |

- 示例

```lua
local rigid_body = GameAPI.get_unit_key_rigid_body_kv(1, "key")
local vector3 = Fix32Vec3(0, 0, 0)

local result = GameAPI.create_scene_node_on_rigid_body("comp_name", rigid_body, vector3, 1.0)
```

---

## set_scene_node_visible_distance

method in GameAPI

- 描述

    设置场景点对玩家的可见距离

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | scene_node | py.SceneNode | 场景点 |
    | player | py.Role | 玩家 |
    | visible_dis | number | 可见距离 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local unit = player:get_all_units()[1]
local scene_node = GameAPI.create_scene_node_on_unit_ex("comp_name", player.handle, unit.handle, "origin", false)

GameAPI.set_scene_node_visible_distance(scene_node, player.handle, 1.0)
```

---

## delete_scene_node

method in GameAPI

- 描述

    删除场景点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | scene_node_entity | py.SceneNode | 场景点 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local unit = player:get_all_units()[1]
local scene_node = GameAPI.create_scene_node_on_unit_ex("comp_name", player.handle, unit.handle, "origin", false)

GameAPI.delete_scene_node(scene_node)
```

---

## unit_key_to_str

method in GameAPI

- 描述

    单位类型转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | val | py.UnitKey | 单位编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.unit_key_to_str(unit_key)
```

---

## str_to_unit_key

method in GameAPI

- 描述

    字符串转单位类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | val | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitKey | 单位编号 |

- 示例

```lua
local result = GameAPI.str_to_unit_key("val")
```

---

## item_key_to_str

method in GameAPI

- 描述

    物品类型转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | val | py.ItemKey | 物品编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.item_key_to_str(item_key)
```

---

## str_to_item_key

method in GameAPI

- 描述

    字符串转物品类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | val | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemKey | 物品编号 |

- 示例

```lua
local result = GameAPI.str_to_item_key("val")
```

---

## ability_key_to_str

method in GameAPI

- 描述

    技能类型转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | val | py.AbilityKey | 技能编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.ability_key_to_str(ability_key)
```

---

## str_to_ability_key

method in GameAPI

- 描述

    字符串转技能类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | val | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityKey | 技能编号 |

- 示例

```lua
local result = GameAPI.str_to_ability_key("val")
```

---

## dest_key_to_str

method in GameAPI

- 描述

    可破坏物类型转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | py.DestructibleKey | 可破坏物编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.dest_key_to_str(destructible_key)
```

---

## str_to_dest_key

method in GameAPI

- 描述

    字符串转可破坏物类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DestructibleKey | 可破坏物编号 |

- 示例

```lua
local result = GameAPI.str_to_dest_key("obj")
```

---

## project_key_to_str

method in GameAPI

- 描述

    投射物类型转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | py.ProjectileKey | 投射物编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.project_key_to_str(projectile_key)
```

---

## str_to_project_key

method in GameAPI

- 描述

    字符串转投射物类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileKey | 投射物编号 |

- 示例

```lua
local result = GameAPI.str_to_project_key("obj")
```

---

## tech_key_to_str

method in GameAPI

- 描述

    科技类型转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | val | py.TechKey | 科技编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.tech_key_to_str(tech_key)
```

---

## str_to_tech_key

method in GameAPI

- 描述

    字符串转科技类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | val | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.TechKey | 科技编号 |

- 示例

```lua
local result = GameAPI.str_to_tech_key("val")
```

---

## model_entity_to_str

method in GameAPI

- 描述

    模型实体转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | py.ModelEntity | 模型实体 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local result = GameAPI.model_entity_to_str(1)
```

---

## model_key_to_str

method in GameAPI

- 描述

    模型类型转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | val | py.ModelKey | 模型编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local model_key = 1

local result = GameAPI.model_key_to_str(model_key)
```

---

## str_to_model_key

method in GameAPI

- 描述

    字符串转模型类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | val | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModelKey | 模型编号 |

- 示例

```lua
local result = GameAPI.str_to_model_key("val")
```

---

## modifier_key_to_str

method in GameAPI

- 描述

    魔法效果类型转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | val | py.ModifierKey | 效果编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.modifier_key_to_str(modifier_key)
```

---

## str_to_modifier_key

method in GameAPI

- 描述

    字符串转魔法效果类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | val | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierKey | 效果编号 |

- 示例

```lua
local result = GameAPI.str_to_modifier_key("val")
```

---

## store_key_to_str

method in GameAPI

- 描述

    平台道具类型转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | py.StoreKey | 平台道具类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local store_key = 134274569

local result = GameAPI.store_key_to_str(store_key)
```

---

## str_to_store_key

method in GameAPI

- 描述

    字符串转平台道具类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.StoreKey | 平台道具类型 |

- 示例

```lua
local result = GameAPI.str_to_store_key("obj")
```

---

## camera_to_str

method in GameAPI

- 描述

    镜头转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | id_value | py.Camera | 镜头 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local camera = y3.camera.create_camera(y3.point(0, 0), 1000, 500, 0, 45, 3000)

local result = GameAPI.camera_to_str(camera.handle)
```

---

## ui_comp_to_str

method in GameAPI

- 描述

    界面组件转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | string | 组件名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local result = GameAPI.ui_comp_to_str("obj")
```

---

## role_res_to_str

method in GameAPI

- 描述

    玩家属性转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | val | py.RoleResKey | 资源类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local role_res_key = "res_key"

local result = GameAPI.role_res_to_str(role_res_key)
```

---

## str_to_role_res

method in GameAPI

- 描述

    字符串转玩家属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | val | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleResKey | 资源类型 |

- 示例

```lua
local result = GameAPI.str_to_role_res("val")
```

---

## unit_attr_to_str

method in GameAPI

- 描述

    单位属性转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | val | string | 属性名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local result = GameAPI.unit_attr_to_str("val")
```

---

## str_to_unit_attr

method in GameAPI

- 描述

    字符串转单位属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | val | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 单位属性 |

- 示例

```lua
local result = GameAPI.str_to_unit_attr("val")
```

---

## str_to_camp

method in GameAPI

- 描述

    字符串转阵营对象

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Camp | 阵营对象 |

- 示例

```lua
local result = GameAPI.str_to_camp("obj")
```

---

## get_model_key_of_dest_key

method in GameAPI

- 描述

    获取可破坏物类型的模型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | dest_key | py.DestructibleKey | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModelKey | 模型编号 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_model_key_of_dest_key(destructible_key)
```

---

## set_smart_cast_ability

method in GameAPI

- 描述

    打开/关闭自动施法

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | py.Role | 玩家 |
    | is_open | boolean | 是否打开 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_smart_cast_ability(player.handle, true)
```

---

## set_preview_common_atk_range

method in GameAPI

- 描述

    设置{玩家}的普攻预览状态为{开启/关闭}

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | py.Role | 玩家 |
    | is_open | boolean | 是否打开 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_preview_common_atk_range(player.handle, true)
```

---

## set_smart_cast_with_pointer

method in GameAPI

- 描述

    是否让{玩家}的智能施法使用指示器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | py.Role | 玩家 |
    | use_skill_pointer | boolean | 是否使用指示器 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_smart_cast_with_pointer(player.handle, true)
```

---

## set_shortcut

method in GameAPI

- 描述

    设置快捷键

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | plan | integer | 方案 |
    | key | string | 快捷键key |
    | value1 | integer | 键盘码1 |
    | value2 | integer | 键盘码2 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_shortcut(player.handle, 1, "key", 1, 1)
```

---

## get_shortcut

method in GameAPI

- 描述

    获取快捷键

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | plan | integer | 方案 |
    | key | string | 快捷键key |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.IntList | 键盘码 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_shortcut(player.handle, 1, "key")
```

---

## set_simple_cast

method in GameAPI

- 描述

    设置智能施法

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | value | boolean | 开启/关闭 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_simple_cast(player.handle, true)
```

---

## get_simple_cast

method in GameAPI

- 描述

    获取智能施法

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否智能施法 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_simple_cast(player.handle)
```

---

## get_client_simple_cast

method in GameAPI

- 描述

    获取客户端智能施法

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否智能施法 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_client_simple_cast(player.handle)
```

---

## save_client_setting

method in GameAPI

- 描述

    保存编辑器局内设置

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.save_client_setting(player.handle)
```

---

## save_game_setting

method in GameAPI

- 描述

    保存玩家设置

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.save_game_setting(player.handle)
```

---

## get_client_role

method in GameAPI

- 描述

    获取本地玩家

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Role | 玩家 |

- 示例

```lua
local result = GameAPI.get_client_role()
```

---

## set_mouse_move_camera_mode

method in GameAPI

- 描述

    设置鼠标移动镜头模式

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | value | boolean | 开启/关闭 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_mouse_move_camera_mode(player.handle, true)
```

---

## set_mouse_move_camera_speed

method in GameAPI

- 描述

    设置鼠标移动镜头速度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | value | number | 移动速度 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_mouse_move_camera_speed(player.handle, 1.0)
```

---

## set_key_move_camera_speed

method in GameAPI

- 描述

    设置键盘移动镜头速度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | value | number | 移动速度 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_key_move_camera_speed(player.handle, 1.0)
```

---

## change_highlight_unit_of_role

method in GameAPI

- 描述

    修改玩家主控单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | unit | py.Unit | 单位 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

GameAPI.change_highlight_unit_of_role(player.handle, unit.handle)
```

---

## set_highlight_unit_of_role

method in GameAPI

- 描述

    玩家主控单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | unit | py.Unit | 单位 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

GameAPI.set_highlight_unit_of_role(player.handle, unit.handle)
```

---

## get_highlight_unit_of_role

method in GameAPI

- 描述

    获取玩家主控单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.get_highlight_unit_of_role(player.handle)
```

---

## api_get_start_mode

method in GameAPI

- 描述

    获取本局游戏环境

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.StartMode | 游戏环境 |

- 示例

```lua
local result = GameAPI.api_get_start_mode()
```

---

## api_check_attack_type

method in GameAPI

- 描述

    攻击类型判断

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attack_type0 | integer | 攻击类型 |
    | attack_type1 | integer | 攻击类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 攻击类型判断 |

- 示例

```lua
local result = GameAPI.api_check_attack_type(1, 1)
```

---

## api_check_armor_type

method in GameAPI

- 描述

    护甲类型判断

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | armor_type0 | integer | 护甲类型 |
    | armor_type1 | integer | 护甲类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 护甲类型判断 |

- 示例

```lua
local result = GameAPI.api_check_armor_type(1, 1)
```

---

## set_weahter_enable

method in GameAPI

- 描述

    天气系统开关

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | weatherID | integer | 天气ID |
    | time | number | 时间 |
    | intensity | number | 强度 |

- 返回值

    无

- 示例

```lua
GameAPI.set_weahter_enable(1, 1.0, 1.0)
```

---

## get_role_platform_icon

method in GameAPI

- 描述

    获取玩家平台头像

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 图片ID |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_role_platform_icon(player.handle)
```

---

## get_role_platform_model

method in GameAPI

- 描述

    获取玩家平台模型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModelKey | 模型编号 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_role_platform_model(player.handle)
```

---

## set_camera_distance_max

method in GameAPI

- 描述

    设置相机最大视距

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | distance_max | number | 高度上限值 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_camera_distance_max(player.handle, 1.0)
```

---

## exit_game

method in GameAPI

- 描述

    退出游戏

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.exit_game(player.handle)
```

---

## create_physics_projectile_in_scene

method in GameAPI

- 描述

    创建一个物理投射物

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | p_key | py.ProjectileKey | 投射物编号 |
    | position | py.FVector3 | 位置 |
    | rotation? | py.FVector3 | 朝向 |
    | owner_unit_or_player? | py.Unit | 所属单位 |
    | duration? | py.Fixed | 持续时间 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileEntity | 创建出的投射物 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local projectile_key = 134274569
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

local result = GameAPI.create_physics_projectile_in_scene(projectile_key, fvector3, nil, nil, Fix32(1))
```

---

## api_get_unit_type_model

method in GameAPI

- 描述

    获取单位类型的模型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位类型编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModelKey | 模型编号 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.api_get_unit_type_model(unit_key)
```

---

## api_get_unit_type_category

method in GameAPI

- 描述

    获取单位类型的分类

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位类型编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 类型 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.api_get_unit_type_category(unit_key)
```

---

## api_get_role_name_of_rank

method in GameAPI

- 描述

    玩家本地图平台等级排行榜玩家名称

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | rank | integer | 排名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 玩家名称 |

- 示例

```lua
local result = GameAPI.api_get_role_name_of_rank(1)
```

---

## api_get_role_level_of_rank

method in GameAPI

- 描述

    玩家本地图平台等级排行榜玩家等级

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | rank | integer | 排名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 玩家等级 |

- 示例

```lua
local result = GameAPI.api_get_role_level_of_rank(1)
```

---

## iter_compose_item_res_of_item_name

method in GameAPI

- 描述

    遍历物品类型的物品合成材料

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品类型 |

- 返回值

    无

- 示例

```lua
local item_key = 134274569

GameAPI.iter_compose_item_res_of_item_name(item_key)
```

---

## iter_compose_role_attr_of_item_name

method in GameAPI

- 描述

    遍历物品类型的玩家合成材料

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品类型 |

- 返回值

    无

- 示例

```lua
local item_key = 134274569

GameAPI.iter_compose_role_attr_of_item_name(item_key)
```

---

## get_random_role_in_role_group

method in GameAPI

- 描述

    玩家组内随机一个玩家

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | roles | py.RoleGroup | 玩家组 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Role | 玩家 |

- 示例

```lua
local player_group = y3.player_group.create()

local result = GameAPI.get_random_role_in_role_group(player_group.handle)
```

---

## get_first_role_in_group

method in GameAPI

- 描述

    玩家组内第一个玩家

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | roles | py.RoleGroup | 玩家组 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Role | 第一个玩家 |

- 示例

```lua
local player_group = y3.player_group.create()

local result = GameAPI.get_first_role_in_group(player_group.handle)
```

---

## get_last_role_in_group

method in GameAPI

- 描述

    玩家组内最后一个玩家

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | roles | py.RoleGroup | 玩家组 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Role | 最后一个玩家 |

- 示例

```lua
local player_group = y3.player_group.create()

local result = GameAPI.get_last_role_in_group(player_group.handle)
```

---

## iter_unit_attr_of_item_name

method in GameAPI

- 描述

    遍历物品类型的单位属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品类型 |

- 返回值

    无

- 示例

```lua
local item_key = 134274569

GameAPI.iter_unit_attr_of_item_name(item_key)
```

---

## iter_unit_attr_of_item

method in GameAPI

- 描述

    遍历物品的单位属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item | py.Item | 物品 |

- 返回值

    无

- 示例

```lua
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

GameAPI.iter_unit_attr_of_item(item.handle)
```

---

## set_billboard_picture

method in GameAPI

- 描述

    设置血条图片

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | node_name | string | 血条命名 |
    | image_id | py.Texture | 图片 |
    | role? | py.Role | 玩家 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

GameAPI.set_billboard_picture(unit.handle, "node_name", 1)
```

---

## set_billboard_text

method in GameAPI

- 描述

    设置血条文本

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | node_name | string | 血条命名 |
    | text | string | 文本 |
    | role? | py.Role | 玩家 |
    | font? | string | 字体 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

GameAPI.set_billboard_text(unit.handle, "node_name", "text", nil, "font")
```

---

## set_billboard_visible

method in GameAPI

- 描述

    设置血条可见性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | node_name | string | 血条命名 |
    | visible | boolean | 可见性 |
    | role? | py.Role | 玩家 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

GameAPI.set_billboard_visible(unit.handle, "node_name", true)
```

---

## set_billboard_progress

method in GameAPI

- 描述

    设置血条进度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | node_name | string | 血条命名 |
    | progress | number | 进度 |
    | role? | py.Role | 玩家 |
    | transition_time? | number | 过渡时间 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

GameAPI.set_billboard_progress(unit.handle, "node_name", 1.0, nil, 1.0)
```

---

## lobby_exit_game

method in GameAPI

- 描述

    玩家完全退出游戏（大厅完全退出游戏）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.lobby_exit_game(player.handle)
```

---

## set_prefab_key_boolean_kv

method in GameAPI

- 描述

    预设库 添加BOOLEAN键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | boolean | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_boolean_kv(1, 1, "key", true)
```

---

## set_prefab_key_integer_kv

method in GameAPI

- 描述

    预设库 添加INTEGER键值对

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
GameAPI.set_prefab_key_integer_kv(1, 1, "key", 1)
```

---

## set_prefab_key_float_kv

method in GameAPI

- 描述

    预设库 添加FLOAT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.Fixed | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_float_kv(1, 1, "key", Fix32(1))
```

---

## set_prefab_key_string_kv

method in GameAPI

- 描述

    预设库 添加STRING键值对

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
GameAPI.set_prefab_key_string_kv(1, 1, "key", "value")
```

---

## set_prefab_key_ui_comp_kv

method in GameAPI

- 描述

    预设库 添加UI_COMP键值对

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
GameAPI.set_prefab_key_ui_comp_kv(1, 1, "key", "value")
```

---

## set_prefab_key_ui_comp_type_kv

method in GameAPI

- 描述

    预设库 添加UI_COMP_TYPE键值对

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
GameAPI.set_prefab_key_ui_comp_type_kv(1, 1, "key", 1)
```

---

## set_prefab_key_ui_comp_event_type_kv

method in GameAPI

- 描述

    预设库 添加UI_COMP_EVENT_TYPE键值对

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
GameAPI.set_prefab_key_ui_comp_event_type_kv(1, 1, "key", 1)
```

---

## set_prefab_key_ui_comp_attr_kv

method in GameAPI

- 描述

    预设库 添加UI_COMP_ATTR键值对

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
GameAPI.set_prefab_key_ui_comp_attr_kv(1, 1, "key", "value")
```

---

## set_prefab_key_ui_comp_align_type_kv

method in GameAPI

- 描述

    预设库 添加UI_COMP_ALIGN_TYPE键值对

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
GameAPI.set_prefab_key_ui_comp_align_type_kv(1, 1, "key", 1)
```

---

## set_prefab_key_ui_prefab_kv

method in GameAPI

- 描述

    预设库 添加UI_PREFAB键值对

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
GameAPI.set_prefab_key_ui_prefab_kv(1, 1, "key", "value")
```

---

## set_prefab_key_ui_prefab_instance_kv

method in GameAPI

- 描述

    预设库 添加UI_PREFAB_INSTANCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.UIPrefabIns | value |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui_prefab_ins = GameAPI.get_ui_prefab_ins(player.handle, "prefab_uid")

GameAPI.set_prefab_key_ui_prefab_instance_kv(1, 1, "key", ui_prefab_ins)
```

---

## set_prefab_key_ui_prefab_ins_uid_kv

method in GameAPI

- 描述

    预设库 添加UI_PREFAB_INS_UID键值对

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
GameAPI.set_prefab_key_ui_prefab_ins_uid_kv(1, 1, "key", "value")
```

---

## set_prefab_key_ui_direction_kv

method in GameAPI

- 描述

    预设库 添加UI_DIRECTION键值对

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
GameAPI.set_prefab_key_ui_direction_kv(1, 1, "key", 1)
```

---

## set_prefab_key_ui_model_camera_mod_kv

method in GameAPI

- 描述

    预设库 添加UI_MODEL_CAMERA_MOD键值对

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
GameAPI.set_prefab_key_ui_model_camera_mod_kv(1, 1, "key", 1)
```

---

## set_prefab_key_ui_btn_status_kv

method in GameAPI

- 描述

    预设库 添加UI_BTN_STATUS键值对

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
GameAPI.set_prefab_key_ui_btn_status_kv(1, 1, "key", 1)
```

---

## set_prefab_key_ui_scrollview_type_kv

method in GameAPI

- 描述

    预设库 添加UI_SCROLLVIEW_TYPE键值对

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
GameAPI.set_prefab_key_ui_scrollview_type_kv(1, 1, "key", 1)
```

---

## set_prefab_key_ui_anim_kv

method in GameAPI

- 描述

    预设库 添加UI_ANIM键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.UIAnimKey | value |

- 返回值

    无

- 示例

```lua
local ui_anim_key = GameAPI.get_unit_key_ui_anim_kv(1, "key")

GameAPI.set_prefab_key_ui_anim_kv(1, 1, "key", ui_anim_key)
```

---

## set_prefab_key_ui_anim_curve_kv

method in GameAPI

- 描述

    预设库 添加UI_ANIM_CURVE键值对

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
GameAPI.set_prefab_key_ui_anim_curve_kv(1, 1, "key", 1)
```

---

## set_prefab_key_audio_channel_kv

method in GameAPI

- 描述

    预设库 添加AUDIO_CHANNEL键值对

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
GameAPI.set_prefab_key_audio_channel_kv(1, 1, "key", 1)
```

---

## set_prefab_key_unit_entity_kv

method in GameAPI

- 描述

    预设库 添加UNIT_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.Unit | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.set_prefab_key_unit_entity_kv(1, 1, "key", unit.handle)
```

---

## set_prefab_key_unit_group_kv

method in GameAPI

- 描述

    预设库 添加UNIT_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.UnitGroup | value |

- 返回值

    无

- 示例

```lua
local unit_group = y3.unit_group.create()

GameAPI.set_prefab_key_unit_group_kv(1, 1, "key", unit_group.handle)
```

---

## set_prefab_key_unit_name_kv

method in GameAPI

- 描述

    预设库 添加UNIT_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.UnitKey | value |

- 返回值

    无

- 示例

```lua
local unit_key = 134274569

GameAPI.set_prefab_key_unit_name_kv(1, 1, "key", unit_key)
```

---

## set_prefab_key_unit_name_pool_kv

method in GameAPI

- 描述

    预设库 添加UNIT_NAME_POOL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.UnitKeyPool | value |

- 返回值

    无

- 示例

```lua
local unit_key_pool = GlobalAPI.get_empty_unit_key_pool()

GameAPI.set_prefab_key_unit_name_pool_kv(1, 1, "key", unit_key_pool)
```

---

## set_prefab_key_unit_write_attribute_kv

method in GameAPI

- 描述

    预设库 添加UNIT_WRITE_ATTRIBUTE键值对

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
GameAPI.set_prefab_key_unit_write_attribute_kv(1, 1, "key", "value")
```

---

## set_prefab_key_attr_element_kv

method in GameAPI

- 描述

    预设库 添加ATTR_ELEMENT键值对

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
GameAPI.set_prefab_key_attr_element_kv(1, 1, "key", "value")
```

---

## set_prefab_key_attr_element_read_kv

method in GameAPI

- 描述

    预设库 添加ATTR_ELEMENT_READ键值对

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
GameAPI.set_prefab_key_attr_element_read_kv(1, 1, "key", "value")
```

---

## set_prefab_key_mover_entity_kv

method in GameAPI

- 描述

    预设库 添加MOVER_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.Mover | value |

- 返回值

    无

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })
local mover = GameAPI.get_projectile_mover(projectile.handle)

GameAPI.set_prefab_key_mover_entity_kv(1, 1, "key", mover)
```

---

## set_prefab_key_image_quality_kv

method in GameAPI

- 描述

    预设库 添加IMAGE_QUALITY键值对

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
GameAPI.set_prefab_key_image_quality_kv(1, 1, "key", "value")
```

---

## set_prefab_key_window_type_setting_kv

method in GameAPI

- 描述

    预设库 添加WINDOW_TYPE_SETTING键值对

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
GameAPI.set_prefab_key_window_type_setting_kv(1, 1, "key", "value")
```

---

## set_prefab_key_item_entity_kv

method in GameAPI

- 描述

    预设库 添加ITEM_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.Item | value |

- 返回值

    无

- 示例

```lua
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

GameAPI.set_prefab_key_item_entity_kv(1, 1, "key", item.handle)
```

---

## set_prefab_key_item_group_kv

method in GameAPI

- 描述

    预设库 添加ITEM_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.ItemGroup | value |

- 返回值

    无

- 示例

```lua
local item_group = y3.item_group.create()

GameAPI.set_prefab_key_item_group_kv(1, 1, "key", item_group.handle)
```

---

## set_prefab_key_item_name_kv

method in GameAPI

- 描述

    预设库 添加ITEM_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.ItemKey | value |

- 返回值

    无

- 示例

```lua
local item_key = 134274569

GameAPI.set_prefab_key_item_name_kv(1, 1, "key", item_key)
```

---

## set_prefab_key_ability_kv

method in GameAPI

- 描述

    预设库 添加ABILITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.Ability | value |

- 返回值

    无

- 示例

```lua
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

GameAPI.set_prefab_key_ability_kv(1, 1, "key", ability.handle)
```

---

## set_prefab_key_ability_type_kv

method in GameAPI

- 描述

    预设库 添加ABILITY_TYPE键值对

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
GameAPI.set_prefab_key_ability_type_kv(1, 1, "key", 1)
```

---

## set_prefab_key_ability_cast_type_kv

method in GameAPI

- 描述

    预设库 添加ABILITY_CAST_TYPE键值对

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
GameAPI.set_prefab_key_ability_cast_type_kv(1, 1, "key", 1)
```

---

## set_prefab_key_ability_name_kv

method in GameAPI

- 描述

    预设库 添加ABILITY_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.AbilityKey | value |

- 返回值

    无

- 示例

```lua
local ability_key = 134274569

GameAPI.set_prefab_key_ability_name_kv(1, 1, "key", ability_key)
```

---

## set_prefab_key_skill_pointer_type_kv

method in GameAPI

- 描述

    预设库 添加SKILL_POINTER_TYPE键值对

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
GameAPI.set_prefab_key_skill_pointer_type_kv(1, 1, "key", 1)
```

---

## set_prefab_key_modifier_entity_kv

method in GameAPI

- 描述

    预设库 添加MODIFIER_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.ModifierEntity | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

GameAPI.set_prefab_key_modifier_entity_kv(1, 1, "key", modifier.handle)
```

---

## set_prefab_key_modifier_type_kv

method in GameAPI

- 描述

    预设库 添加MODIFIER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.ModifierType | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_modifier_type_kv(1, 1, "key", 1)
```

---

## set_prefab_key_modifier_effect_type_kv

method in GameAPI

- 描述

    预设库 添加MODIFIER_EFFECT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.ModifierEffectType | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_modifier_effect_type_kv(1, 1, "key", 1)
```

---

## set_prefab_key_modifier_kv

method in GameAPI

- 描述

    预设库 添加MODIFIER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.ModifierKey | value |

- 返回值

    无

- 示例

```lua
local modifier_key = 134274569

GameAPI.set_prefab_key_modifier_kv(1, 1, "key", modifier_key)
```

---

## set_prefab_key_projectile_kv

method in GameAPI

- 描述

    预设库 添加PROJECTILE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.ProjectileKey | value |

- 返回值

    无

- 示例

```lua
local projectile_key = 134274569

GameAPI.set_prefab_key_projectile_kv(1, 1, "key", projectile_key)
```

---

## set_prefab_key_projectile_entity_kv

method in GameAPI

- 描述

    预设库 添加PROJECTILE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.ProjectileEntity | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local target_point = unit:get_point()
local projectile = y3.projectile.create({ key = 134274569, target = target_point })

GameAPI.set_prefab_key_projectile_entity_kv(1, 1, "key", projectile.handle)
```

---

## set_prefab_key_projectile_group_kv

method in GameAPI

- 描述

    预设库 添加PROJECTILE_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.ProjectileGroup | value |

- 返回值

    无

- 示例

```lua
local projectile_group = y3.projectile_group.create_lua_projectile_group_from_py(GameAPI.create_projectile_group())

GameAPI.set_prefab_key_projectile_group_kv(1, 1, "key", projectile_group.handle)
```

---

## set_prefab_key_destructible_entity_kv

method in GameAPI

- 描述

    预设库 添加DESTRUCTIBLE_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.Destructible | value |

- 返回值

    无

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

GameAPI.set_prefab_key_destructible_entity_kv(1, 1, "key", destructible.handle)
end
```

---

## set_prefab_key_destructible_name_kv

method in GameAPI

- 描述

    预设库 添加DESTRUCTIBLE_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.DestructibleKey | value |

- 返回值

    无

- 示例

```lua
local destructible_key = 1

GameAPI.set_prefab_key_destructible_name_kv(1, 1, "key", destructible_key)
```

---

## set_prefab_key_sound_entity_kv

method in GameAPI

- 描述

    预设库 添加SOUND_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.SoundEntity | value |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local sound_entity = GameAPI.play_sound_for_player(player.handle, 134274569, false)

GameAPI.set_prefab_key_sound_entity_kv(1, 1, "key", sound_entity)
```

---

## set_prefab_key_audio_key_kv

method in GameAPI

- 描述

    预设库 添加AUDIO_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.AudioKey | value |

- 返回值

    无

- 示例

```lua
local audio_key = 134274569

GameAPI.set_prefab_key_audio_key_kv(1, 1, "key", audio_key)
```

---

## set_prefab_key_game_mode_kv

method in GameAPI

- 描述

    预设库 添加GAME_MODE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.GameMode | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_game_mode_kv(1, 1, "key", 1)
```

---

## set_prefab_key_player_kv

method in GameAPI

- 描述

    预设库 添加PLAYER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.Role | value |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_prefab_key_player_kv(1, 1, "key", player.handle)
```

---

## set_prefab_key_player_group_kv

method in GameAPI

- 描述

    预设库 添加PLAYER_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.RoleGroup | value |

- 返回值

    无

- 示例

```lua
local player_group = y3.player_group.create()

GameAPI.set_prefab_key_player_group_kv(1, 1, "key", player_group.handle)
```

---

## set_prefab_key_role_res_key_kv

method in GameAPI

- 描述

    预设库 添加ROLE_RES_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.RoleResKey | value |

- 返回值

    无

- 示例

```lua
local role_res_key = "res_key"

GameAPI.set_prefab_key_role_res_key_kv(1, 1, "key", role_res_key)
```

---

## set_prefab_key_role_status_kv

method in GameAPI

- 描述

    预设库 添加ROLE_STATUS键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.RoleStatus | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_role_status_kv(1, 1, "key", 1)
```

---

## set_prefab_key_role_type_kv

method in GameAPI

- 描述

    预设库 添加ROLE_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.RoleType | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_role_type_kv(1, 1, "key", 1)
```

---

## set_prefab_key_role_relation_kv

method in GameAPI

- 描述

    预设库 添加ROLE_RELATION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.RoleRelation | value |

- 返回值

    无

- 示例

```lua
local relation = 1

GameAPI.set_prefab_key_role_relation_kv(1, 1, "key", relation)
```

---

## set_prefab_key_team_kv

method in GameAPI

- 描述

    预设库 添加TEAM键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.Camp | value |

- 返回值

    无

- 示例

```lua
local camp = GameAPI.get_camp_by_camp_id(1)

GameAPI.set_prefab_key_team_kv(1, 1, "key", camp)
```

---

## set_prefab_key_point_kv

method in GameAPI

- 描述

    预设库 添加POINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.FPoint | value |

- 返回值

    无

- 示例

```lua
local fpoint = GameAPI.get_point_by_res_id(1)

GameAPI.set_prefab_key_point_kv(1, 1, "key", fpoint)
```

---

## set_prefab_key_vector3_kv

method in GameAPI

- 描述

    预设库 添加VECTOR3键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.FVector3 | value |

- 返回值

    无

- 示例

```lua
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

GameAPI.set_prefab_key_vector3_kv(1, 1, "key", fvector3)
```

---

## set_prefab_key_rotation_kv

method in GameAPI

- 描述

    预设库 添加ROTATION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.FRotation | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_rotation_kv(1, 1, "key", GlobalAPI.vector3_to_euler(Fix32Vec3(0, 0, 0)))
```

---

## set_prefab_key_point_list_kv

method in GameAPI

- 描述

    预设库 添加POINT_LIST键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.Road | value |

- 返回值

    无

- 示例

```lua
local road = y3.road.get_road_by_res_id(1)

GameAPI.set_prefab_key_point_list_kv(1, 1, "key", road.handle)
```

---

## set_prefab_key_rectangle_kv

method in GameAPI

- 描述

    预设库 添加RECTANGLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.RecArea | value |

- 返回值

    无

- 示例

```lua
local rec_area = GameAPI.create_rec_area_from_two_points(Fix32Vec3(0, 0, 0), Fix32Vec3(100, 100, 0))

GameAPI.set_prefab_key_rectangle_kv(1, 1, "key", rec_area)
```

---

## set_prefab_key_round_area_kv

method in GameAPI

- 描述

    预设库 添加ROUND_AREA键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.CirArea | value |

- 返回值

    无

- 示例

```lua
local cir_area = GameAPI.create_new_cir_area(GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0)), Fix32(100))

GameAPI.set_prefab_key_round_area_kv(1, 1, "key", cir_area)
```

---

## set_prefab_key_polygon_kv

method in GameAPI

- 描述

    预设库 添加POLYGON键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.PolyArea | value |

- 返回值

    无

- 示例

```lua
local poly_area = GameAPI.create_polygon_area(Fix32Vec3(0, 0, 0), Fix32Vec3(100, 0, 0), Fix32Vec3(100, 100, 0))

GameAPI.set_prefab_key_polygon_kv(1, 1, "key", poly_area)
```

---

## set_prefab_key_camera_kv

method in GameAPI

- 描述

    预设库 添加CAMERA键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.Camera | value |

- 返回值

    无

- 示例

```lua
local camera = y3.camera.create_camera(y3.point(0, 0), 1000, 500, 0, 45, 3000)

GameAPI.set_prefab_key_camera_kv(1, 1, "key", camera.handle)
```

---

## set_prefab_key_camline_kv

method in GameAPI

- 描述

    预设库 添加CAMLINE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.CamlineID | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_camline_kv(1, 1, "key", 1)
```

---

## set_prefab_key_point_light_kv

method in GameAPI

- 描述

    预设库 添加POINT_LIGHT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.PointLight | value |

- 返回值

    无

- 示例

```lua
local point_light = GameAPI.get_point_light_res_by_res_id(1)

GameAPI.set_prefab_key_point_light_kv(1, 1, "key", point_light)
```

---

## set_prefab_key_spot_light_kv

method in GameAPI

- 描述

    预设库 添加SPOT_LIGHT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.SpotLight | value |

- 返回值

    无

- 示例

```lua
local spot_light = GameAPI.get_spot_light_res_by_res_id(1)

GameAPI.set_prefab_key_spot_light_kv(1, 1, "key", spot_light)
```

---

## set_prefab_key_fog_kv

method in GameAPI

- 描述

    预设库 添加FOG键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.Fog | value |

- 返回值

    无

- 示例

```lua
local fog = GameAPI.get_fog_res_by_res_id(1)

GameAPI.set_prefab_key_fog_kv(1, 1, "key", fog)
```

---

## set_prefab_key_scene_sound_kv

method in GameAPI

- 描述

    预设库 添加SCENE_SOUND键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.SceneSound | value |

- 返回值

    无

- 示例

```lua
local scene_sound = GameAPI.get_scene_sound_by_res_id(1)

GameAPI.set_prefab_key_scene_sound_kv(1, 1, "key", scene_sound)
```

---

## set_prefab_key_model_kv

method in GameAPI

- 描述

    预设库 添加MODEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.ModelKey | value |

- 返回值

    无

- 示例

```lua
local model_key = 1

GameAPI.set_prefab_key_model_kv(1, 1, "key", model_key)
```

---

## set_prefab_key_sfx_entity_kv

method in GameAPI

- 描述

    预设库 添加SFX_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.Sfx | value |

- 返回值

    无

- 示例

```lua
local sfx = y3.particle.create({ type = 134274569, target = y3.point(0, 0) }).handle

GameAPI.set_prefab_key_sfx_entity_kv(1, 1, "key", sfx)
```

---

## set_prefab_key_sfx_key_kv

method in GameAPI

- 描述

    预设库 添加SFX_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.SfxKey | value |

- 返回值

    无

- 示例

```lua
local sfx_key = 134274569

GameAPI.set_prefab_key_sfx_key_kv(1, 1, "key", sfx_key)
```

---

## set_prefab_key_link_sfx_entity_kv

method in GameAPI

- 描述

    预设库 添加LINK_SFX_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.LinkSfx | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local link_sfx = GameAPI.create_link_sfx_from_unit_to_point(134274569, unit.handle, "origin", GlobalAPI.coord_to_point(Fix32(100), Fix32(100), Fix32(0)), Fix32(0))

GameAPI.set_prefab_key_link_sfx_entity_kv(1, 1, "key", link_sfx)
```

---

## set_prefab_key_link_sfx_key_kv

method in GameAPI

- 描述

    预设库 添加LINK_SFX_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.LinkSfxKey | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_link_sfx_key_kv(1, 1, "key", 1)
```

---

## set_prefab_key_cursor_key_kv

method in GameAPI

- 描述

    预设库 添加CURSOR_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.CursorKey | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_cursor_key_kv(1, 1, "key", 1)
```

---

## set_prefab_key_angle_kv

method in GameAPI

- 描述

    预设库 添加ANGLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.Fixed | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_angle_kv(1, 1, "key", Fix32(1))
```

---

## set_prefab_key_texture_kv

method in GameAPI

- 描述

    预设库 添加TEXTURE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.Texture | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_texture_kv(1, 1, "key", 1)
```

---

## set_prefab_key_sequence_kv

method in GameAPI

- 描述

    预设库 添加SEQUENCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.Sequence | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_sequence_kv(1, 1, "key", 1)
```

---

## set_prefab_key_physics_object_kv

method in GameAPI

- 描述

    预设库 添加PHYSICS_OBJECT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.PhysicsObject | value |

- 返回值

    无

- 示例

```lua
local physics_object = GameAPI.get_unit_key_physics_object_kv(1, "key")

GameAPI.set_prefab_key_physics_object_kv(1, 1, "key", physics_object)
```

---

## set_prefab_key_physics_entity_kv

method in GameAPI

- 描述

    预设库 添加PHYSICS_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.PhysicsEntity | value |

- 返回值

    无

- 示例

```lua
local physics_entity = GameAPI.get_unit_key_physics_entity_kv(1, "key")

GameAPI.set_prefab_key_physics_entity_kv(1, 1, "key", physics_entity)
```

---

## set_prefab_key_physics_object_key_kv

method in GameAPI

- 描述

    预设库 添加PHYSICS_OBJECT_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.PhysicsObjectKey | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_physics_object_key_kv(1, 1, "key", 1)
```

---

## set_prefab_key_physics_entity_key_kv

method in GameAPI

- 描述

    预设库 添加PHYSICS_ENTITY_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.PhysicsEntityKey | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_physics_entity_key_kv(1, 1, "key", 1)
```

---

## set_prefab_key_rigid_body_kv

method in GameAPI

- 描述

    预设库 添加RIGID_BODY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.RigidBody | value |

- 返回值

    无

- 示例

```lua
local rigid_body = GameAPI.get_unit_key_rigid_body_kv(1, "key")

GameAPI.set_prefab_key_rigid_body_kv(1, 1, "key", rigid_body)
```

---

## set_prefab_key_rigid_body_group_kv

method in GameAPI

- 描述

    预设库 添加RIGID_BODY_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.RigidBodyGroup | value |

- 返回值

    无

- 示例

```lua
local rigid_body_group = GameAPI.get_unit_key_rigid_body_group_kv(1, "key")

GameAPI.set_prefab_key_rigid_body_group_kv(1, 1, "key", rigid_body_group)
```

---

## set_prefab_key_collider_kv

method in GameAPI

- 描述

    预设库 添加COLLIDER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.Collider | value |

- 返回值

    无

- 示例

```lua
local collider = GameAPI.get_unit_key_collider_kv(1, "key")

GameAPI.set_prefab_key_collider_kv(1, 1, "key", collider)
```

---

## set_prefab_key_joint_kv

method in GameAPI

- 描述

    预设库 添加JOINT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.Joint | value |

- 返回值

    无

- 示例

```lua
local joint = GameAPI.get_unit_key_joint_kv(1, "key")

GameAPI.set_prefab_key_joint_kv(1, 1, "key", joint)
```

---

## set_prefab_key_reaction_kv

method in GameAPI

- 描述

    预设库 添加REACTION键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.Reaction | value |

- 返回值

    无

- 示例

```lua
local physics_entity = GameAPI.get_unit_key_physics_entity_kv(1, "key")
local reaction = GameAPI.api_add_uniform_gravitation_field_to_rigid_body(physics_entity, Fix32(10), Fix32Vec3(0, 0, 0))

GameAPI.set_prefab_key_reaction_kv(1, 1, "key", reaction)
```

---

## set_prefab_key_reaction_group_kv

method in GameAPI

- 描述

    预设库 添加REACTION_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.ReactionGroup | value |

- 返回值

    无

- 示例

```lua
local reaction_group = GameAPI.get_trigger_variable_reaction_group("key")

GameAPI.set_prefab_key_reaction_group_kv(1, 1, "key", reaction_group)
```

---

## set_prefab_key_dynamic_trigger_instance_kv

method in GameAPI

- 描述

    预设库 添加DYNAMIC_TRIGGER_INSTANCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.DynamicTriggerInstance | value |

- 返回值

    无

- 示例

```lua
local trigger_instance = GameAPI.get_last_created_trigger()

GameAPI.set_prefab_key_dynamic_trigger_instance_kv(1, 1, "key", trigger_instance)
```

---

## set_prefab_key_table_kv

method in GameAPI

- 描述

    预设库 添加TABLE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.Table | value |

- 返回值

    无

- 示例

```lua
local tbl = {}

GameAPI.set_prefab_key_table_kv(1, 1, "key", tbl)
```

---

## set_prefab_key_random_pool_kv

method in GameAPI

- 描述

    预设库 添加RANDOM_POOL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.RandomPool | value |

- 返回值

    无

- 示例

```lua
local random_pool = GameAPI.create_random_pool()

GameAPI.set_prefab_key_random_pool_kv(1, 1, "key", random_pool)
```

---

## set_prefab_key_scene_ui_kv

method in GameAPI

- 描述

    预设库 添加SCENE_UI键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.SceneNode | value |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local unit = player:get_all_units()[1]
local scene_node = GameAPI.create_scene_node_on_unit_ex("comp_name", player.handle, unit.handle, "origin", false)

GameAPI.set_prefab_key_scene_ui_kv(1, 1, "key", scene_node)
```

---

## set_prefab_key_damage_type_kv

method in GameAPI

- 描述

    预设库 添加DAMAGE_TYPE键值对

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
GameAPI.set_prefab_key_damage_type_kv(1, 1, "key", 1)
```

---

## set_prefab_key_harm_text_type_new_kv

method in GameAPI

- 描述

    预设库 添加HARM_TEXT_TYPE_NEW键值对

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
GameAPI.set_prefab_key_harm_text_type_new_kv(1, 1, "key", "value")
```

---

## set_prefab_key_font_type_kv

method in GameAPI

- 描述

    预设库 添加FONT_TYPE键值对

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
GameAPI.set_prefab_key_font_type_kv(1, 1, "key", "value")
```

---

## set_prefab_key_jump_word_track_kv

method in GameAPI

- 描述

    预设库 添加JUMP_WORD_TRACK键值对

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
GameAPI.set_prefab_key_jump_word_track_kv(1, 1, "key", 1)
```

---

## set_prefab_key_new_timer_kv

method in GameAPI

- 描述

    预设库 添加NEW_TIMER键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.Timer | value |

- 返回值

    无

- 示例

```lua
local timer = y3.timer.loop(1, function() end)

GameAPI.set_prefab_key_new_timer_kv(1, 1, "key", timer.handle)
```

---

## set_prefab_key_tech_key_kv

method in GameAPI

- 描述

    预设库 添加TECH_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.TechKey | value |

- 返回值

    无

- 示例

```lua
local tech_key = 134274569

GameAPI.set_prefab_key_tech_key_kv(1, 1, "key", tech_key)
```

---

## set_prefab_key_store_key_kv

method in GameAPI

- 描述

    预设库 添加STORE_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.StoreKey | value |

- 返回值

    无

- 示例

```lua
local store_key = 134274569

GameAPI.set_prefab_key_store_key_kv(1, 1, "key", store_key)
```

---

## set_prefab_key_keyboard_key_kv

method in GameAPI

- 描述

    预设库 添加KEYBOARD_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.KeyboardKey | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_keyboard_key_kv(1, 1, "key", 1)
```

---

## set_prefab_key_func_keyboard_key_kv

method in GameAPI

- 描述

    预设库 添加FUNC_KEYBOARD_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.FuncKeyboardKey | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_func_keyboard_key_kv(1, 1, "key", 1)
```

---

## set_prefab_key_mouse_key_kv

method in GameAPI

- 描述

    预设库 添加MOUSE_KEY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.MouseKey | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_mouse_key_kv(1, 1, "key", 1)
```

---

## set_prefab_key_mouse_wheel_kv

method in GameAPI

- 描述

    预设库 添加MOUSE_WHEEL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.MouseWheel | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_mouse_wheel_kv(1, 1, "key", 1)
```

---

## set_prefab_key_post_effect_kv

method in GameAPI

- 描述

    预设库 添加POST_EFFECT键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.PostEffect | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_post_effect_kv(1, 1, "key", 1)
```

---

## set_prefab_key_unit_type_kv

method in GameAPI

- 描述

    预设库 添加UNIT_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.UnitType | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_unit_type_kv(1, 1, "key", 1)
```

---

## set_prefab_key_unit_command_type_kv

method in GameAPI

- 描述

    预设库 添加UNIT_COMMAND_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.UnitCommandType | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_unit_command_type_kv(1, 1, "key", 1)
```

---

## set_prefab_key_mini_map_color_type_kv

method in GameAPI

- 描述

    预设库 添加MINI_MAP_COLOR_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.MiniMapColorType | value |

- 返回值

    无

- 示例

```lua
GameAPI.set_prefab_key_mini_map_color_type_kv(1, 1, "key", 1)
```

---

## set_prefab_key_unit_behavior_kv

method in GameAPI

- 描述

    预设库 添加UNIT_BEHAVIOR键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.UnitBehavior | value |

- 返回值

    无

- 示例

```lua
local unit_behavior = "unit_behavior"

GameAPI.set_prefab_key_unit_behavior_kv(1, 1, "key", unit_behavior)
```

---

## set_prefab_key_curved_path_kv

method in GameAPI

- 描述

    预设库 添加CURVED_PATH键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.CurvedPath | value |

- 返回值

    无

- 示例

```lua
local path = {}

GameAPI.set_prefab_key_curved_path_kv(1, 1, "key", path)
```

---

## set_prefab_key_curved_path_3d_kv

method in GameAPI

- 描述

    预设库 添加CURVED_PATH_3D键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_conf_key | integer | prefab库ID |
    | item_key | integer | 编号 |
    | key | string | 键值名称 |
    | value | py.CurvedPath3D | value |

- 返回值

    无

- 示例

```lua
local curved_path_3d = {}

GameAPI.set_prefab_key_curved_path_3d_kv(1, 1, "key", curved_path_3d)
```

---

## has_prefab_boolean_kv

method in GameAPI

- 描述

    判断预设是否存在BOOLEAN键值对

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

local result = GameAPI.has_prefab_boolean_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_integer_kv

method in GameAPI

- 描述

    判断预设是否存在INTEGER键值对

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

local result = GameAPI.has_prefab_integer_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_float_kv

method in GameAPI

- 描述

    判断预设是否存在FLOAT键值对

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

local result = GameAPI.has_prefab_float_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_string_kv

method in GameAPI

- 描述

    判断预设是否存在STRING键值对

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

local result = GameAPI.has_prefab_string_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_ui_comp_kv

method in GameAPI

- 描述

    判断预设是否存在UI_COMP键值对

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

local result = GameAPI.has_prefab_ui_comp_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_ui_comp_type_kv

method in GameAPI

- 描述

    判断预设是否存在UI_COMP_TYPE键值对

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

local result = GameAPI.has_prefab_ui_comp_type_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_ui_comp_event_type_kv

method in GameAPI

- 描述

    判断预设是否存在UI_COMP_EVENT_TYPE键值对

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

local result = GameAPI.has_prefab_ui_comp_event_type_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_ui_comp_attr_kv

method in GameAPI

- 描述

    判断预设是否存在UI_COMP_ATTR键值对

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

local result = GameAPI.has_prefab_ui_comp_attr_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_ui_comp_align_type_kv

method in GameAPI

- 描述

    判断预设是否存在UI_COMP_ALIGN_TYPE键值对

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

local result = GameAPI.has_prefab_ui_comp_align_type_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_ui_prefab_kv

method in GameAPI

- 描述

    判断预设是否存在UI_PREFAB键值对

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

local result = GameAPI.has_prefab_ui_prefab_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_ui_prefab_instance_kv

method in GameAPI

- 描述

    判断预设是否存在UI_PREFAB_INSTANCE键值对

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

local result = GameAPI.has_prefab_ui_prefab_instance_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_ui_prefab_ins_uid_kv

method in GameAPI

- 描述

    判断预设是否存在UI_PREFAB_INS_UID键值对

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

local result = GameAPI.has_prefab_ui_prefab_ins_uid_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_ui_direction_kv

method in GameAPI

- 描述

    判断预设是否存在UI_DIRECTION键值对

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

local result = GameAPI.has_prefab_ui_direction_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_ui_model_camera_mod_kv

method in GameAPI

- 描述

    判断预设是否存在UI_MODEL_CAMERA_MOD键值对

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

local result = GameAPI.has_prefab_ui_model_camera_mod_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_ui_btn_status_kv

method in GameAPI

- 描述

    判断预设是否存在UI_BTN_STATUS键值对

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

local result = GameAPI.has_prefab_ui_btn_status_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_ui_scrollview_type_kv

method in GameAPI

- 描述

    判断预设是否存在UI_SCROLLVIEW_TYPE键值对

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

local result = GameAPI.has_prefab_ui_scrollview_type_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_ui_anim_kv

method in GameAPI

- 描述

    判断预设是否存在UI_ANIM键值对

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

local result = GameAPI.has_prefab_ui_anim_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_ui_anim_curve_kv

method in GameAPI

- 描述

    判断预设是否存在UI_ANIM_CURVE键值对

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

local result = GameAPI.has_prefab_ui_anim_curve_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_audio_channel_kv

method in GameAPI

- 描述

    判断预设是否存在AUDIO_CHANNEL键值对

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

local result = GameAPI.has_prefab_audio_channel_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_unit_entity_kv

method in GameAPI

- 描述

    判断预设是否存在UNIT_ENTITY键值对

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

local result = GameAPI.has_prefab_unit_entity_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_unit_group_kv

method in GameAPI

- 描述

    判断预设是否存在UNIT_GROUP键值对

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

local result = GameAPI.has_prefab_unit_group_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_unit_name_kv

method in GameAPI

- 描述

    判断预设是否存在UNIT_NAME键值对

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

local result = GameAPI.has_prefab_unit_name_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_unit_name_pool_kv

method in GameAPI

- 描述

    判断预设是否存在UNIT_NAME_POOL键值对

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

local result = GameAPI.has_prefab_unit_name_pool_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_unit_write_attribute_kv

method in GameAPI

- 描述

    判断预设是否存在UNIT_WRITE_ATTRIBUTE键值对

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

local result = GameAPI.has_prefab_unit_write_attribute_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_attr_element_kv

method in GameAPI

- 描述

    判断预设是否存在ATTR_ELEMENT键值对

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

local result = GameAPI.has_prefab_attr_element_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_attr_element_read_kv

method in GameAPI

- 描述

    判断预设是否存在ATTR_ELEMENT_READ键值对

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

local result = GameAPI.has_prefab_attr_element_read_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_mover_entity_kv

method in GameAPI

- 描述

    判断预设是否存在MOVER_ENTITY键值对

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

local result = GameAPI.has_prefab_mover_entity_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_image_quality_kv

method in GameAPI

- 描述

    判断预设是否存在IMAGE_QUALITY键值对

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

local result = GameAPI.has_prefab_image_quality_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_window_type_setting_kv

method in GameAPI

- 描述

    判断预设是否存在WINDOW_TYPE_SETTING键值对

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

local result = GameAPI.has_prefab_window_type_setting_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_item_entity_kv

method in GameAPI

- 描述

    判断预设是否存在ITEM_ENTITY键值对

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

local result = GameAPI.has_prefab_item_entity_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_item_group_kv

method in GameAPI

- 描述

    判断预设是否存在ITEM_GROUP键值对

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

local result = GameAPI.has_prefab_item_group_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_item_name_kv

method in GameAPI

- 描述

    判断预设是否存在ITEM_NAME键值对

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

local result = GameAPI.has_prefab_item_name_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_ability_kv

method in GameAPI

- 描述

    判断预设是否存在ABILITY键值对

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

local result = GameAPI.has_prefab_ability_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_ability_type_kv

method in GameAPI

- 描述

    判断预设是否存在ABILITY_TYPE键值对

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

local result = GameAPI.has_prefab_ability_type_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_ability_cast_type_kv

method in GameAPI

- 描述

    判断预设是否存在ABILITY_CAST_TYPE键值对

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

local result = GameAPI.has_prefab_ability_cast_type_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_ability_name_kv

method in GameAPI

- 描述

    判断预设是否存在ABILITY_NAME键值对

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

local result = GameAPI.has_prefab_ability_name_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_skill_pointer_type_kv

method in GameAPI

- 描述

    判断预设是否存在SKILL_POINTER_TYPE键值对

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

local result = GameAPI.has_prefab_skill_pointer_type_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_modifier_entity_kv

method in GameAPI

- 描述

    判断预设是否存在MODIFIER_ENTITY键值对

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

local result = GameAPI.has_prefab_modifier_entity_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_modifier_type_kv

method in GameAPI

- 描述

    判断预设是否存在MODIFIER_TYPE键值对

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

local result = GameAPI.has_prefab_modifier_type_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_modifier_effect_type_kv

method in GameAPI

- 描述

    判断预设是否存在MODIFIER_EFFECT_TYPE键值对

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

local result = GameAPI.has_prefab_modifier_effect_type_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_modifier_kv

method in GameAPI

- 描述

    判断预设是否存在MODIFIER键值对

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

local result = GameAPI.has_prefab_modifier_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_projectile_kv

method in GameAPI

- 描述

    判断预设是否存在PROJECTILE键值对

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

local result = GameAPI.has_prefab_projectile_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_projectile_entity_kv

method in GameAPI

- 描述

    判断预设是否存在PROJECTILE_ENTITY键值对

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

local result = GameAPI.has_prefab_projectile_entity_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_projectile_group_kv

method in GameAPI

- 描述

    判断预设是否存在PROJECTILE_GROUP键值对

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

local result = GameAPI.has_prefab_projectile_group_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_destructible_entity_kv

method in GameAPI

- 描述

    判断预设是否存在DESTRUCTIBLE_ENTITY键值对

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

local result = GameAPI.has_prefab_destructible_entity_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_destructible_name_kv

method in GameAPI

- 描述

    判断预设是否存在DESTRUCTIBLE_NAME键值对

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

local result = GameAPI.has_prefab_destructible_name_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_sound_entity_kv

method in GameAPI

- 描述

    判断预设是否存在SOUND_ENTITY键值对

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

local result = GameAPI.has_prefab_sound_entity_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_audio_key_kv

method in GameAPI

- 描述

    判断预设是否存在AUDIO_KEY键值对

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

local result = GameAPI.has_prefab_audio_key_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_game_mode_kv

method in GameAPI

- 描述

    判断预设是否存在GAME_MODE键值对

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

local result = GameAPI.has_prefab_game_mode_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_player_kv

method in GameAPI

- 描述

    判断预设是否存在PLAYER键值对

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

local result = GameAPI.has_prefab_player_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_player_group_kv

method in GameAPI

- 描述

    判断预设是否存在PLAYER_GROUP键值对

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

local result = GameAPI.has_prefab_player_group_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_role_res_key_kv

method in GameAPI

- 描述

    判断预设是否存在ROLE_RES_KEY键值对

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

local result = GameAPI.has_prefab_role_res_key_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_role_status_kv

method in GameAPI

- 描述

    判断预设是否存在ROLE_STATUS键值对

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

local result = GameAPI.has_prefab_role_status_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_role_type_kv

method in GameAPI

- 描述

    判断预设是否存在ROLE_TYPE键值对

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

local result = GameAPI.has_prefab_role_type_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_role_relation_kv

method in GameAPI

- 描述

    判断预设是否存在ROLE_RELATION键值对

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

local result = GameAPI.has_prefab_role_relation_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_team_kv

method in GameAPI

- 描述

    判断预设是否存在TEAM键值对

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

local result = GameAPI.has_prefab_team_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_point_kv

method in GameAPI

- 描述

    判断预设是否存在POINT键值对

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

local result = GameAPI.has_prefab_point_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_vector3_kv

method in GameAPI

- 描述

    判断预设是否存在VECTOR3键值对

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

local result = GameAPI.has_prefab_vector3_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_rotation_kv

method in GameAPI

- 描述

    判断预设是否存在ROTATION键值对

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

local result = GameAPI.has_prefab_rotation_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_point_list_kv

method in GameAPI

- 描述

    判断预设是否存在POINT_LIST键值对

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

local result = GameAPI.has_prefab_point_list_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_rectangle_kv

method in GameAPI

- 描述

    判断预设是否存在RECTANGLE键值对

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

local result = GameAPI.has_prefab_rectangle_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_round_area_kv

method in GameAPI

- 描述

    判断预设是否存在ROUND_AREA键值对

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

local result = GameAPI.has_prefab_round_area_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_polygon_kv

method in GameAPI

- 描述

    判断预设是否存在POLYGON键值对

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

local result = GameAPI.has_prefab_polygon_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_camera_kv

method in GameAPI

- 描述

    判断预设是否存在CAMERA键值对

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

local result = GameAPI.has_prefab_camera_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_camline_kv

method in GameAPI

- 描述

    判断预设是否存在CAMLINE键值对

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

local result = GameAPI.has_prefab_camline_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_point_light_kv

method in GameAPI

- 描述

    判断预设是否存在POINT_LIGHT键值对

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

local result = GameAPI.has_prefab_point_light_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_spot_light_kv

method in GameAPI

- 描述

    判断预设是否存在SPOT_LIGHT键值对

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

local result = GameAPI.has_prefab_spot_light_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_fog_kv

method in GameAPI

- 描述

    判断预设是否存在FOG键值对

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

local result = GameAPI.has_prefab_fog_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_scene_sound_kv

method in GameAPI

- 描述

    判断预设是否存在SCENE_SOUND键值对

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

local result = GameAPI.has_prefab_scene_sound_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_model_kv

method in GameAPI

- 描述

    判断预设是否存在MODEL键值对

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

local result = GameAPI.has_prefab_model_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_sfx_entity_kv

method in GameAPI

- 描述

    判断预设是否存在SFX_ENTITY键值对

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

local result = GameAPI.has_prefab_sfx_entity_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_sfx_key_kv

method in GameAPI

- 描述

    判断预设是否存在SFX_KEY键值对

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

local result = GameAPI.has_prefab_sfx_key_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_link_sfx_entity_kv

method in GameAPI

- 描述

    判断预设是否存在LINK_SFX_ENTITY键值对

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

local result = GameAPI.has_prefab_link_sfx_entity_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_link_sfx_key_kv

method in GameAPI

- 描述

    判断预设是否存在LINK_SFX_KEY键值对

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

local result = GameAPI.has_prefab_link_sfx_key_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_cursor_key_kv

method in GameAPI

- 描述

    判断预设是否存在CURSOR_KEY键值对

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

local result = GameAPI.has_prefab_cursor_key_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_angle_kv

method in GameAPI

- 描述

    判断预设是否存在ANGLE键值对

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

local result = GameAPI.has_prefab_angle_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_texture_kv

method in GameAPI

- 描述

    判断预设是否存在TEXTURE键值对

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

local result = GameAPI.has_prefab_texture_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_sequence_kv

method in GameAPI

- 描述

    判断预设是否存在SEQUENCE键值对

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

local result = GameAPI.has_prefab_sequence_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_physics_object_kv

method in GameAPI

- 描述

    判断预设是否存在PHYSICS_OBJECT键值对

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

local result = GameAPI.has_prefab_physics_object_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_physics_entity_kv

method in GameAPI

- 描述

    判断预设是否存在PHYSICS_ENTITY键值对

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

local result = GameAPI.has_prefab_physics_entity_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_physics_object_key_kv

method in GameAPI

- 描述

    判断预设是否存在PHYSICS_OBJECT_KEY键值对

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

local result = GameAPI.has_prefab_physics_object_key_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_physics_entity_key_kv

method in GameAPI

- 描述

    判断预设是否存在PHYSICS_ENTITY_KEY键值对

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

local result = GameAPI.has_prefab_physics_entity_key_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_rigid_body_kv

method in GameAPI

- 描述

    判断预设是否存在RIGID_BODY键值对

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

local result = GameAPI.has_prefab_rigid_body_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_rigid_body_group_kv

method in GameAPI

- 描述

    判断预设是否存在RIGID_BODY_GROUP键值对

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

local result = GameAPI.has_prefab_rigid_body_group_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_collider_kv

method in GameAPI

- 描述

    判断预设是否存在COLLIDER键值对

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

local result = GameAPI.has_prefab_collider_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_joint_kv

method in GameAPI

- 描述

    判断预设是否存在JOINT键值对

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

local result = GameAPI.has_prefab_joint_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_reaction_kv

method in GameAPI

- 描述

    判断预设是否存在REACTION键值对

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

local result = GameAPI.has_prefab_reaction_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_reaction_group_kv

method in GameAPI

- 描述

    判断预设是否存在REACTION_GROUP键值对

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

local result = GameAPI.has_prefab_reaction_group_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_dynamic_trigger_instance_kv

method in GameAPI

- 描述

    判断预设是否存在DYNAMIC_TRIGGER_INSTANCE键值对

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

local result = GameAPI.has_prefab_dynamic_trigger_instance_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_table_kv

method in GameAPI

- 描述

    判断预设是否存在TABLE键值对

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

local result = GameAPI.has_prefab_table_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_random_pool_kv

method in GameAPI

- 描述

    判断预设是否存在RANDOM_POOL键值对

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

local result = GameAPI.has_prefab_random_pool_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_scene_ui_kv

method in GameAPI

- 描述

    判断预设是否存在SCENE_UI键值对

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

local result = GameAPI.has_prefab_scene_ui_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_damage_type_kv

method in GameAPI

- 描述

    判断预设是否存在DAMAGE_TYPE键值对

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

local result = GameAPI.has_prefab_damage_type_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_harm_text_type_new_kv

method in GameAPI

- 描述

    判断预设是否存在HARM_TEXT_TYPE_NEW键值对

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

local result = GameAPI.has_prefab_harm_text_type_new_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_font_type_kv

method in GameAPI

- 描述

    判断预设是否存在FONT_TYPE键值对

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

local result = GameAPI.has_prefab_font_type_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_jump_word_track_kv

method in GameAPI

- 描述

    判断预设是否存在JUMP_WORD_TRACK键值对

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

local result = GameAPI.has_prefab_jump_word_track_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_new_timer_kv

method in GameAPI

- 描述

    判断预设是否存在NEW_TIMER键值对

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

local result = GameAPI.has_prefab_new_timer_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_tech_key_kv

method in GameAPI

- 描述

    判断预设是否存在TECH_KEY键值对

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

local result = GameAPI.has_prefab_tech_key_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_store_key_kv

method in GameAPI

- 描述

    判断预设是否存在STORE_KEY键值对

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

local result = GameAPI.has_prefab_store_key_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_keyboard_key_kv

method in GameAPI

- 描述

    判断预设是否存在KEYBOARD_KEY键值对

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

local result = GameAPI.has_prefab_keyboard_key_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_func_keyboard_key_kv

method in GameAPI

- 描述

    判断预设是否存在FUNC_KEYBOARD_KEY键值对

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

local result = GameAPI.has_prefab_func_keyboard_key_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_mouse_key_kv

method in GameAPI

- 描述

    判断预设是否存在MOUSE_KEY键值对

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

local result = GameAPI.has_prefab_mouse_key_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_mouse_wheel_kv

method in GameAPI

- 描述

    判断预设是否存在MOUSE_WHEEL键值对

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

local result = GameAPI.has_prefab_mouse_wheel_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_post_effect_kv

method in GameAPI

- 描述

    判断预设是否存在POST_EFFECT键值对

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

local result = GameAPI.has_prefab_post_effect_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_unit_type_kv

method in GameAPI

- 描述

    判断预设是否存在UNIT_TYPE键值对

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

local result = GameAPI.has_prefab_unit_type_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_unit_command_type_kv

method in GameAPI

- 描述

    判断预设是否存在UNIT_COMMAND_TYPE键值对

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

local result = GameAPI.has_prefab_unit_command_type_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_mini_map_color_type_kv

method in GameAPI

- 描述

    判断预设是否存在MINI_MAP_COLOR_TYPE键值对

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

local result = GameAPI.has_prefab_mini_map_color_type_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_unit_behavior_kv

method in GameAPI

- 描述

    判断预设是否存在UNIT_BEHAVIOR键值对

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

local result = GameAPI.has_prefab_unit_behavior_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_curved_path_kv

method in GameAPI

- 描述

    判断预设是否存在CURVED_PATH键值对

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

local result = GameAPI.has_prefab_curved_path_kv("prefab_type", unit_key, "key")
```

---

## has_prefab_curved_path_3d_kv

method in GameAPI

- 描述

    判断预设是否存在CURVED_PATH_3D键值对

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

local result = GameAPI.has_prefab_curved_path_3d_kv("prefab_type", unit_key, "key")
```

---

## get_unit_key_boolean_kv

method in GameAPI

- 描述

    获取单位编号BOOLEAN键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_boolean_kv(unit_key, "key")
```

---

## get_item_key_boolean_kv

method in GameAPI

- 描述

    获取物品编号BOOLEAN键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_boolean_kv(item_key, "key")
```

---

## get_ability_key_boolean_kv

method in GameAPI

- 描述

    获取技能编号BOOLEAN键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_boolean_kv(ability_key, "key")
```

---

## get_modifier_key_boolean_kv

method in GameAPI

- 描述

    获取魔法效果特效编号BOOLEAN键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_boolean_kv(modifier_key, "key")
```

---

## get_projectile_key_boolean_kv

method in GameAPI

- 描述

    获取特效编号BOOLEAN键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_boolean_kv(projectile_key, "key")
```

---

## get_destructible_key_boolean_kv

method in GameAPI

- 描述

    获取可破坏物编号BOOLEAN键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_boolean_kv(destructible_key, "key")
```

---

## get_tech_key_boolean_kv

method in GameAPI

- 描述

    获取科技编号BOOLEAN键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_boolean_kv(tech_key, "key")
```

---

## get_icon_id_boolean_kv

method in GameAPI

- 描述

    获取图片BOOLEAN键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_boolean_kv(1, "key")
```

---

## get_physics_entity_key_boolean_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型BOOLEAN键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_boolean_kv(1, "key")
```

---

## get_unit_key_integer_kv

method in GameAPI

- 描述

    获取单位编号INTEGER键值对

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

local result = GameAPI.get_unit_key_integer_kv(unit_key, "key")
```

---

## get_item_key_integer_kv

method in GameAPI

- 描述

    获取物品编号INTEGER键值对

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

local result = GameAPI.get_item_key_integer_kv(item_key, "key")
```

---

## get_ability_key_integer_kv

method in GameAPI

- 描述

    获取技能编号INTEGER键值对

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

local result = GameAPI.get_ability_key_integer_kv(ability_key, "key")
```

---

## get_modifier_key_integer_kv

method in GameAPI

- 描述

    获取魔法效果特效编号INTEGER键值对

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

local result = GameAPI.get_modifier_key_integer_kv(modifier_key, "key")
```

---

## get_projectile_key_integer_kv

method in GameAPI

- 描述

    获取特效编号INTEGER键值对

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

local result = GameAPI.get_projectile_key_integer_kv(projectile_key, "key")
```

---

## get_destructible_key_integer_kv

method in GameAPI

- 描述

    获取可破坏物编号INTEGER键值对

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

local result = GameAPI.get_destructible_key_integer_kv(destructible_key, "key")
```

---

## get_tech_key_integer_kv

method in GameAPI

- 描述

    获取科技编号INTEGER键值对

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

local result = GameAPI.get_tech_key_integer_kv(tech_key, "key")
```

---

## get_icon_id_integer_kv

method in GameAPI

- 描述

    获取图片INTEGER键值对

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
local result = GameAPI.get_icon_id_integer_kv(1, "key")
```

---

## get_physics_entity_key_integer_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型INTEGER键值对

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
local result = GameAPI.get_physics_entity_key_integer_kv(1, "key")
```

---

## get_unit_key_float_kv

method in GameAPI

- 描述

    获取单位编号FLOAT键值对

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

local result = GameAPI.get_unit_key_float_kv(unit_key, "key")
```

---

## get_item_key_float_kv

method in GameAPI

- 描述

    获取物品编号FLOAT键值对

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

local result = GameAPI.get_item_key_float_kv(item_key, "key")
```

---

## get_ability_key_float_kv

method in GameAPI

- 描述

    获取技能编号FLOAT键值对

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

local result = GameAPI.get_ability_key_float_kv(ability_key, "key")
```

---

## get_modifier_key_float_kv

method in GameAPI

- 描述

    获取魔法效果特效编号FLOAT键值对

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

local result = GameAPI.get_modifier_key_float_kv(modifier_key, "key")
```

---

## get_projectile_key_float_kv

method in GameAPI

- 描述

    获取特效编号FLOAT键值对

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

local result = GameAPI.get_projectile_key_float_kv(projectile_key, "key")
```

---

## get_destructible_key_float_kv

method in GameAPI

- 描述

    获取可破坏物编号FLOAT键值对

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

local result = GameAPI.get_destructible_key_float_kv(destructible_key, "key")
```

---

## get_tech_key_float_kv

method in GameAPI

- 描述

    获取科技编号FLOAT键值对

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

local result = GameAPI.get_tech_key_float_kv(tech_key, "key")
```

---

## get_icon_id_float_kv

method in GameAPI

- 描述

    获取图片FLOAT键值对

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
local result = GameAPI.get_icon_id_float_kv(1, "key")
```

---

## get_physics_entity_key_float_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型FLOAT键值对

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
local result = GameAPI.get_physics_entity_key_float_kv(1, "key")
```

---

## get_unit_key_string_kv

method in GameAPI

- 描述

    获取单位编号STRING键值对

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

local result = GameAPI.get_unit_key_string_kv(unit_key, "key")
```

---

## get_item_key_string_kv

method in GameAPI

- 描述

    获取物品编号STRING键值对

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

local result = GameAPI.get_item_key_string_kv(item_key, "key")
```

---

## get_ability_key_string_kv

method in GameAPI

- 描述

    获取技能编号STRING键值对

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

local result = GameAPI.get_ability_key_string_kv(ability_key, "key")
```

---

## get_modifier_key_string_kv

method in GameAPI

- 描述

    获取魔法效果特效编号STRING键值对

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

local result = GameAPI.get_modifier_key_string_kv(modifier_key, "key")
```

---

## get_projectile_key_string_kv

method in GameAPI

- 描述

    获取特效编号STRING键值对

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

local result = GameAPI.get_projectile_key_string_kv(projectile_key, "key")
```

---

## get_destructible_key_string_kv

method in GameAPI

- 描述

    获取可破坏物编号STRING键值对

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

local result = GameAPI.get_destructible_key_string_kv(destructible_key, "key")
```

---

## get_tech_key_string_kv

method in GameAPI

- 描述

    获取科技编号STRING键值对

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

local result = GameAPI.get_tech_key_string_kv(tech_key, "key")
```

---

## get_icon_id_string_kv

method in GameAPI

- 描述

    获取图片STRING键值对

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
local result = GameAPI.get_icon_id_string_kv(1, "key")
```

---

## get_physics_entity_key_string_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型STRING键值对

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
local result = GameAPI.get_physics_entity_key_string_kv(1, "key")
```

---

## get_unit_key_ui_comp_kv

method in GameAPI

- 描述

    获取单位编号UI_COMP键值对

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

local result = GameAPI.get_unit_key_ui_comp_kv(unit_key, "key")
```

---

## get_item_key_ui_comp_kv

method in GameAPI

- 描述

    获取物品编号UI_COMP键值对

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

local result = GameAPI.get_item_key_ui_comp_kv(item_key, "key")
```

---

## get_ability_key_ui_comp_kv

method in GameAPI

- 描述

    获取技能编号UI_COMP键值对

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

local result = GameAPI.get_ability_key_ui_comp_kv(ability_key, "key")
```

---

## get_modifier_key_ui_comp_kv

method in GameAPI

- 描述

    获取魔法效果特效编号UI_COMP键值对

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

local result = GameAPI.get_modifier_key_ui_comp_kv(modifier_key, "key")
```

---

## get_projectile_key_ui_comp_kv

method in GameAPI

- 描述

    获取特效编号UI_COMP键值对

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

local result = GameAPI.get_projectile_key_ui_comp_kv(projectile_key, "key")
```

---

## get_destructible_key_ui_comp_kv

method in GameAPI

- 描述

    获取可破坏物编号UI_COMP键值对

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

local result = GameAPI.get_destructible_key_ui_comp_kv(destructible_key, "key")
```

---

## get_tech_key_ui_comp_kv

method in GameAPI

- 描述

    获取科技编号UI_COMP键值对

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

local result = GameAPI.get_tech_key_ui_comp_kv(tech_key, "key")
```

---

## get_icon_id_ui_comp_kv

method in GameAPI

- 描述

    获取图片UI_COMP键值对

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
local result = GameAPI.get_icon_id_ui_comp_kv(1, "key")
```

---

## get_physics_entity_key_ui_comp_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型UI_COMP键值对

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
local result = GameAPI.get_physics_entity_key_ui_comp_kv(1, "key")
```

---

## get_unit_key_ui_comp_type_kv

method in GameAPI

- 描述

    获取单位编号UI_COMP_TYPE键值对

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

local result = GameAPI.get_unit_key_ui_comp_type_kv(unit_key, "key")
```

---

## get_item_key_ui_comp_type_kv

method in GameAPI

- 描述

    获取物品编号UI_COMP_TYPE键值对

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

local result = GameAPI.get_item_key_ui_comp_type_kv(item_key, "key")
```

---

## get_ability_key_ui_comp_type_kv

method in GameAPI

- 描述

    获取技能编号UI_COMP_TYPE键值对

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

local result = GameAPI.get_ability_key_ui_comp_type_kv(ability_key, "key")
```

---

## get_modifier_key_ui_comp_type_kv

method in GameAPI

- 描述

    获取魔法效果特效编号UI_COMP_TYPE键值对

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

local result = GameAPI.get_modifier_key_ui_comp_type_kv(modifier_key, "key")
```

---

## get_projectile_key_ui_comp_type_kv

method in GameAPI

- 描述

    获取特效编号UI_COMP_TYPE键值对

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

local result = GameAPI.get_projectile_key_ui_comp_type_kv(projectile_key, "key")
```

---

## get_destructible_key_ui_comp_type_kv

method in GameAPI

- 描述

    获取可破坏物编号UI_COMP_TYPE键值对

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

local result = GameAPI.get_destructible_key_ui_comp_type_kv(destructible_key, "key")
```

---

## get_tech_key_ui_comp_type_kv

method in GameAPI

- 描述

    获取科技编号UI_COMP_TYPE键值对

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

local result = GameAPI.get_tech_key_ui_comp_type_kv(tech_key, "key")
```

---

## get_icon_id_ui_comp_type_kv

method in GameAPI

- 描述

    获取图片UI_COMP_TYPE键值对

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
local result = GameAPI.get_icon_id_ui_comp_type_kv(1, "key")
```

---

## get_physics_entity_key_ui_comp_type_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型UI_COMP_TYPE键值对

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
local result = GameAPI.get_physics_entity_key_ui_comp_type_kv(1, "key")
```

---

## get_unit_key_ui_comp_event_type_kv

method in GameAPI

- 描述

    获取单位编号UI_COMP_EVENT_TYPE键值对

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

local result = GameAPI.get_unit_key_ui_comp_event_type_kv(unit_key, "key")
```

---

## get_item_key_ui_comp_event_type_kv

method in GameAPI

- 描述

    获取物品编号UI_COMP_EVENT_TYPE键值对

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

local result = GameAPI.get_item_key_ui_comp_event_type_kv(item_key, "key")
```

---

## get_ability_key_ui_comp_event_type_kv

method in GameAPI

- 描述

    获取技能编号UI_COMP_EVENT_TYPE键值对

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

local result = GameAPI.get_ability_key_ui_comp_event_type_kv(ability_key, "key")
```

---

## get_modifier_key_ui_comp_event_type_kv

method in GameAPI

- 描述

    获取魔法效果特效编号UI_COMP_EVENT_TYPE键值对

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

local result = GameAPI.get_modifier_key_ui_comp_event_type_kv(modifier_key, "key")
```

---

## get_projectile_key_ui_comp_event_type_kv

method in GameAPI

- 描述

    获取特效编号UI_COMP_EVENT_TYPE键值对

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

local result = GameAPI.get_projectile_key_ui_comp_event_type_kv(projectile_key, "key")
```

---

## get_destructible_key_ui_comp_event_type_kv

method in GameAPI

- 描述

    获取可破坏物编号UI_COMP_EVENT_TYPE键值对

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

local result = GameAPI.get_destructible_key_ui_comp_event_type_kv(destructible_key, "key")
```

---

## get_tech_key_ui_comp_event_type_kv

method in GameAPI

- 描述

    获取科技编号UI_COMP_EVENT_TYPE键值对

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

local result = GameAPI.get_tech_key_ui_comp_event_type_kv(tech_key, "key")
```

---

## get_icon_id_ui_comp_event_type_kv

method in GameAPI

- 描述

    获取图片UI_COMP_EVENT_TYPE键值对

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
local result = GameAPI.get_icon_id_ui_comp_event_type_kv(1, "key")
```

---

## get_physics_entity_key_ui_comp_event_type_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型UI_COMP_EVENT_TYPE键值对

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
local result = GameAPI.get_physics_entity_key_ui_comp_event_type_kv(1, "key")
```

---

## get_unit_key_ui_comp_attr_kv

method in GameAPI

- 描述

    获取单位编号UI_COMP_ATTR键值对

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

local result = GameAPI.get_unit_key_ui_comp_attr_kv(unit_key, "key")
```

---

## get_item_key_ui_comp_attr_kv

method in GameAPI

- 描述

    获取物品编号UI_COMP_ATTR键值对

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

local result = GameAPI.get_item_key_ui_comp_attr_kv(item_key, "key")
```

---

## get_ability_key_ui_comp_attr_kv

method in GameAPI

- 描述

    获取技能编号UI_COMP_ATTR键值对

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

local result = GameAPI.get_ability_key_ui_comp_attr_kv(ability_key, "key")
```

---

## get_modifier_key_ui_comp_attr_kv

method in GameAPI

- 描述

    获取魔法效果特效编号UI_COMP_ATTR键值对

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

local result = GameAPI.get_modifier_key_ui_comp_attr_kv(modifier_key, "key")
```

---

## get_projectile_key_ui_comp_attr_kv

method in GameAPI

- 描述

    获取特效编号UI_COMP_ATTR键值对

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

local result = GameAPI.get_projectile_key_ui_comp_attr_kv(projectile_key, "key")
```

---

## get_destructible_key_ui_comp_attr_kv

method in GameAPI

- 描述

    获取可破坏物编号UI_COMP_ATTR键值对

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

local result = GameAPI.get_destructible_key_ui_comp_attr_kv(destructible_key, "key")
```

---

## get_tech_key_ui_comp_attr_kv

method in GameAPI

- 描述

    获取科技编号UI_COMP_ATTR键值对

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

local result = GameAPI.get_tech_key_ui_comp_attr_kv(tech_key, "key")
```

---

## get_icon_id_ui_comp_attr_kv

method in GameAPI

- 描述

    获取图片UI_COMP_ATTR键值对

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
local result = GameAPI.get_icon_id_ui_comp_attr_kv(1, "key")
```

---

## get_physics_entity_key_ui_comp_attr_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型UI_COMP_ATTR键值对

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
local result = GameAPI.get_physics_entity_key_ui_comp_attr_kv(1, "key")
```

---

## get_unit_key_ui_comp_align_type_kv

method in GameAPI

- 描述

    获取单位编号UI_COMP_ALIGN_TYPE键值对

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

local result = GameAPI.get_unit_key_ui_comp_align_type_kv(unit_key, "key")
```

---

## get_item_key_ui_comp_align_type_kv

method in GameAPI

- 描述

    获取物品编号UI_COMP_ALIGN_TYPE键值对

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

local result = GameAPI.get_item_key_ui_comp_align_type_kv(item_key, "key")
```

---

## get_ability_key_ui_comp_align_type_kv

method in GameAPI

- 描述

    获取技能编号UI_COMP_ALIGN_TYPE键值对

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

local result = GameAPI.get_ability_key_ui_comp_align_type_kv(ability_key, "key")
```

---

## get_modifier_key_ui_comp_align_type_kv

method in GameAPI

- 描述

    获取魔法效果特效编号UI_COMP_ALIGN_TYPE键值对

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

local result = GameAPI.get_modifier_key_ui_comp_align_type_kv(modifier_key, "key")
```

---

## get_projectile_key_ui_comp_align_type_kv

method in GameAPI

- 描述

    获取特效编号UI_COMP_ALIGN_TYPE键值对

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

local result = GameAPI.get_projectile_key_ui_comp_align_type_kv(projectile_key, "key")
```

---

## get_destructible_key_ui_comp_align_type_kv

method in GameAPI

- 描述

    获取可破坏物编号UI_COMP_ALIGN_TYPE键值对

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

local result = GameAPI.get_destructible_key_ui_comp_align_type_kv(destructible_key, "key")
```

---

## get_tech_key_ui_comp_align_type_kv

method in GameAPI

- 描述

    获取科技编号UI_COMP_ALIGN_TYPE键值对

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

local result = GameAPI.get_tech_key_ui_comp_align_type_kv(tech_key, "key")
```

---

## get_icon_id_ui_comp_align_type_kv

method in GameAPI

- 描述

    获取图片UI_COMP_ALIGN_TYPE键值对

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
local result = GameAPI.get_icon_id_ui_comp_align_type_kv(1, "key")
```

---

## get_physics_entity_key_ui_comp_align_type_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型UI_COMP_ALIGN_TYPE键值对

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
local result = GameAPI.get_physics_entity_key_ui_comp_align_type_kv(1, "key")
```

---

## get_unit_key_ui_prefab_kv

method in GameAPI

- 描述

    获取单位编号UI_PREFAB键值对

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

local result = GameAPI.get_unit_key_ui_prefab_kv(unit_key, "key")
```

---

## get_item_key_ui_prefab_kv

method in GameAPI

- 描述

    获取物品编号UI_PREFAB键值对

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

local result = GameAPI.get_item_key_ui_prefab_kv(item_key, "key")
```

---

## get_ability_key_ui_prefab_kv

method in GameAPI

- 描述

    获取技能编号UI_PREFAB键值对

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

local result = GameAPI.get_ability_key_ui_prefab_kv(ability_key, "key")
```

---

## get_modifier_key_ui_prefab_kv

method in GameAPI

- 描述

    获取魔法效果特效编号UI_PREFAB键值对

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

local result = GameAPI.get_modifier_key_ui_prefab_kv(modifier_key, "key")
```

---

## get_projectile_key_ui_prefab_kv

method in GameAPI

- 描述

    获取特效编号UI_PREFAB键值对

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

local result = GameAPI.get_projectile_key_ui_prefab_kv(projectile_key, "key")
```

---

## get_destructible_key_ui_prefab_kv

method in GameAPI

- 描述

    获取可破坏物编号UI_PREFAB键值对

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

local result = GameAPI.get_destructible_key_ui_prefab_kv(destructible_key, "key")
```

---

## get_tech_key_ui_prefab_kv

method in GameAPI

- 描述

    获取科技编号UI_PREFAB键值对

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

local result = GameAPI.get_tech_key_ui_prefab_kv(tech_key, "key")
```

---

## get_icon_id_ui_prefab_kv

method in GameAPI

- 描述

    获取图片UI_PREFAB键值对

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
local result = GameAPI.get_icon_id_ui_prefab_kv(1, "key")
```

---

## get_physics_entity_key_ui_prefab_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型UI_PREFAB键值对

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
local result = GameAPI.get_physics_entity_key_ui_prefab_kv(1, "key")
```

---

## get_unit_key_ui_prefab_instance_kv

method in GameAPI

- 描述

    获取单位编号UI_PREFAB_INSTANCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UIPrefabIns | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_ui_prefab_instance_kv(unit_key, "key")
```

---

## get_item_key_ui_prefab_instance_kv

method in GameAPI

- 描述

    获取物品编号UI_PREFAB_INSTANCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UIPrefabIns | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_ui_prefab_instance_kv(item_key, "key")
```

---

## get_ability_key_ui_prefab_instance_kv

method in GameAPI

- 描述

    获取技能编号UI_PREFAB_INSTANCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UIPrefabIns | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_ui_prefab_instance_kv(ability_key, "key")
```

---

## get_modifier_key_ui_prefab_instance_kv

method in GameAPI

- 描述

    获取魔法效果特效编号UI_PREFAB_INSTANCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UIPrefabIns | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_ui_prefab_instance_kv(modifier_key, "key")
```

---

## get_projectile_key_ui_prefab_instance_kv

method in GameAPI

- 描述

    获取特效编号UI_PREFAB_INSTANCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UIPrefabIns | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_ui_prefab_instance_kv(projectile_key, "key")
```

---

## get_destructible_key_ui_prefab_instance_kv

method in GameAPI

- 描述

    获取可破坏物编号UI_PREFAB_INSTANCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UIPrefabIns | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_ui_prefab_instance_kv(destructible_key, "key")
```

---

## get_tech_key_ui_prefab_instance_kv

method in GameAPI

- 描述

    获取科技编号UI_PREFAB_INSTANCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UIPrefabIns | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_ui_prefab_instance_kv(tech_key, "key")
```

---

## get_icon_id_ui_prefab_instance_kv

method in GameAPI

- 描述

    获取图片UI_PREFAB_INSTANCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UIPrefabIns | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_ui_prefab_instance_kv(1, "key")
```

---

## get_physics_entity_key_ui_prefab_instance_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型UI_PREFAB_INSTANCE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UIPrefabIns | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_ui_prefab_instance_kv(1, "key")
```

---

## get_unit_key_ui_prefab_ins_uid_kv

method in GameAPI

- 描述

    获取单位编号UI_PREFAB_INS_UID键值对

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

local result = GameAPI.get_unit_key_ui_prefab_ins_uid_kv(unit_key, "key")
```

---

## get_item_key_ui_prefab_ins_uid_kv

method in GameAPI

- 描述

    获取物品编号UI_PREFAB_INS_UID键值对

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

local result = GameAPI.get_item_key_ui_prefab_ins_uid_kv(item_key, "key")
```

---

## get_ability_key_ui_prefab_ins_uid_kv

method in GameAPI

- 描述

    获取技能编号UI_PREFAB_INS_UID键值对

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

local result = GameAPI.get_ability_key_ui_prefab_ins_uid_kv(ability_key, "key")
```

---

## get_modifier_key_ui_prefab_ins_uid_kv

method in GameAPI

- 描述

    获取魔法效果特效编号UI_PREFAB_INS_UID键值对

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

local result = GameAPI.get_modifier_key_ui_prefab_ins_uid_kv(modifier_key, "key")
```

---

## get_projectile_key_ui_prefab_ins_uid_kv

method in GameAPI

- 描述

    获取特效编号UI_PREFAB_INS_UID键值对

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

local result = GameAPI.get_projectile_key_ui_prefab_ins_uid_kv(projectile_key, "key")
```

---

## get_destructible_key_ui_prefab_ins_uid_kv

method in GameAPI

- 描述

    获取可破坏物编号UI_PREFAB_INS_UID键值对

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

local result = GameAPI.get_destructible_key_ui_prefab_ins_uid_kv(destructible_key, "key")
```

---

## get_tech_key_ui_prefab_ins_uid_kv

method in GameAPI

- 描述

    获取科技编号UI_PREFAB_INS_UID键值对

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

local result = GameAPI.get_tech_key_ui_prefab_ins_uid_kv(tech_key, "key")
```

---

## get_icon_id_ui_prefab_ins_uid_kv

method in GameAPI

- 描述

    获取图片UI_PREFAB_INS_UID键值对

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
local result = GameAPI.get_icon_id_ui_prefab_ins_uid_kv(1, "key")
```

---

## get_physics_entity_key_ui_prefab_ins_uid_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型UI_PREFAB_INS_UID键值对

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
local result = GameAPI.get_physics_entity_key_ui_prefab_ins_uid_kv(1, "key")
```

---

## get_unit_key_ui_direction_kv

method in GameAPI

- 描述

    获取单位编号UI_DIRECTION键值对

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

local result = GameAPI.get_unit_key_ui_direction_kv(unit_key, "key")
```

---

## get_item_key_ui_direction_kv

method in GameAPI

- 描述

    获取物品编号UI_DIRECTION键值对

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

local result = GameAPI.get_item_key_ui_direction_kv(item_key, "key")
```

---

## get_ability_key_ui_direction_kv

method in GameAPI

- 描述

    获取技能编号UI_DIRECTION键值对

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

local result = GameAPI.get_ability_key_ui_direction_kv(ability_key, "key")
```

---

## get_modifier_key_ui_direction_kv

method in GameAPI

- 描述

    获取魔法效果特效编号UI_DIRECTION键值对

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

local result = GameAPI.get_modifier_key_ui_direction_kv(modifier_key, "key")
```

---

## get_projectile_key_ui_direction_kv

method in GameAPI

- 描述

    获取特效编号UI_DIRECTION键值对

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

local result = GameAPI.get_projectile_key_ui_direction_kv(projectile_key, "key")
```

---

## get_destructible_key_ui_direction_kv

method in GameAPI

- 描述

    获取可破坏物编号UI_DIRECTION键值对

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

local result = GameAPI.get_destructible_key_ui_direction_kv(destructible_key, "key")
```

---

## get_tech_key_ui_direction_kv

method in GameAPI

- 描述

    获取科技编号UI_DIRECTION键值对

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

local result = GameAPI.get_tech_key_ui_direction_kv(tech_key, "key")
```

---

## get_icon_id_ui_direction_kv

method in GameAPI

- 描述

    获取图片UI_DIRECTION键值对

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
local result = GameAPI.get_icon_id_ui_direction_kv(1, "key")
```

---

## get_physics_entity_key_ui_direction_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型UI_DIRECTION键值对

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
local result = GameAPI.get_physics_entity_key_ui_direction_kv(1, "key")
```

---

## get_unit_key_ui_model_camera_mod_kv

method in GameAPI

- 描述

    获取单位编号UI_MODEL_CAMERA_MOD键值对

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

local result = GameAPI.get_unit_key_ui_model_camera_mod_kv(unit_key, "key")
```

---

## get_item_key_ui_model_camera_mod_kv

method in GameAPI

- 描述

    获取物品编号UI_MODEL_CAMERA_MOD键值对

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

local result = GameAPI.get_item_key_ui_model_camera_mod_kv(item_key, "key")
```

---

## get_ability_key_ui_model_camera_mod_kv

method in GameAPI

- 描述

    获取技能编号UI_MODEL_CAMERA_MOD键值对

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

local result = GameAPI.get_ability_key_ui_model_camera_mod_kv(ability_key, "key")
```

---

## get_modifier_key_ui_model_camera_mod_kv

method in GameAPI

- 描述

    获取魔法效果特效编号UI_MODEL_CAMERA_MOD键值对

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

local result = GameAPI.get_modifier_key_ui_model_camera_mod_kv(modifier_key, "key")
```

---

## get_projectile_key_ui_model_camera_mod_kv

method in GameAPI

- 描述

    获取特效编号UI_MODEL_CAMERA_MOD键值对

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

local result = GameAPI.get_projectile_key_ui_model_camera_mod_kv(projectile_key, "key")
```

---

## get_destructible_key_ui_model_camera_mod_kv

method in GameAPI

- 描述

    获取可破坏物编号UI_MODEL_CAMERA_MOD键值对

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

local result = GameAPI.get_destructible_key_ui_model_camera_mod_kv(destructible_key, "key")
```

---

## get_tech_key_ui_model_camera_mod_kv

method in GameAPI

- 描述

    获取科技编号UI_MODEL_CAMERA_MOD键值对

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

local result = GameAPI.get_tech_key_ui_model_camera_mod_kv(tech_key, "key")
```

---

## get_icon_id_ui_model_camera_mod_kv

method in GameAPI

- 描述

    获取图片UI_MODEL_CAMERA_MOD键值对

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
local result = GameAPI.get_icon_id_ui_model_camera_mod_kv(1, "key")
```

---

## get_physics_entity_key_ui_model_camera_mod_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型UI_MODEL_CAMERA_MOD键值对

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
local result = GameAPI.get_physics_entity_key_ui_model_camera_mod_kv(1, "key")
```

---

## get_unit_key_ui_btn_status_kv

method in GameAPI

- 描述

    获取单位编号UI_BTN_STATUS键值对

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

local result = GameAPI.get_unit_key_ui_btn_status_kv(unit_key, "key")
```

---

## get_item_key_ui_btn_status_kv

method in GameAPI

- 描述

    获取物品编号UI_BTN_STATUS键值对

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

local result = GameAPI.get_item_key_ui_btn_status_kv(item_key, "key")
```

---

## get_ability_key_ui_btn_status_kv

method in GameAPI

- 描述

    获取技能编号UI_BTN_STATUS键值对

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

local result = GameAPI.get_ability_key_ui_btn_status_kv(ability_key, "key")
```

---

## get_modifier_key_ui_btn_status_kv

method in GameAPI

- 描述

    获取魔法效果特效编号UI_BTN_STATUS键值对

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

local result = GameAPI.get_modifier_key_ui_btn_status_kv(modifier_key, "key")
```

---

## get_projectile_key_ui_btn_status_kv

method in GameAPI

- 描述

    获取特效编号UI_BTN_STATUS键值对

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

local result = GameAPI.get_projectile_key_ui_btn_status_kv(projectile_key, "key")
```

---

## get_destructible_key_ui_btn_status_kv

method in GameAPI

- 描述

    获取可破坏物编号UI_BTN_STATUS键值对

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

local result = GameAPI.get_destructible_key_ui_btn_status_kv(destructible_key, "key")
```

---

## get_tech_key_ui_btn_status_kv

method in GameAPI

- 描述

    获取科技编号UI_BTN_STATUS键值对

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

local result = GameAPI.get_tech_key_ui_btn_status_kv(tech_key, "key")
```

---

## get_icon_id_ui_btn_status_kv

method in GameAPI

- 描述

    获取图片UI_BTN_STATUS键值对

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
local result = GameAPI.get_icon_id_ui_btn_status_kv(1, "key")
```

---

## get_physics_entity_key_ui_btn_status_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型UI_BTN_STATUS键值对

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
local result = GameAPI.get_physics_entity_key_ui_btn_status_kv(1, "key")
```

---

## get_unit_key_ui_scrollview_type_kv

method in GameAPI

- 描述

    获取单位编号UI_SCROLLVIEW_TYPE键值对

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

local result = GameAPI.get_unit_key_ui_scrollview_type_kv(unit_key, "key")
```

---

## get_item_key_ui_scrollview_type_kv

method in GameAPI

- 描述

    获取物品编号UI_SCROLLVIEW_TYPE键值对

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

local result = GameAPI.get_item_key_ui_scrollview_type_kv(item_key, "key")
```

---

## get_ability_key_ui_scrollview_type_kv

method in GameAPI

- 描述

    获取技能编号UI_SCROLLVIEW_TYPE键值对

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

local result = GameAPI.get_ability_key_ui_scrollview_type_kv(ability_key, "key")
```

---

## get_modifier_key_ui_scrollview_type_kv

method in GameAPI

- 描述

    获取魔法效果特效编号UI_SCROLLVIEW_TYPE键值对

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

local result = GameAPI.get_modifier_key_ui_scrollview_type_kv(modifier_key, "key")
```

---

## get_projectile_key_ui_scrollview_type_kv

method in GameAPI

- 描述

    获取特效编号UI_SCROLLVIEW_TYPE键值对

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

local result = GameAPI.get_projectile_key_ui_scrollview_type_kv(projectile_key, "key")
```

---

## get_destructible_key_ui_scrollview_type_kv

method in GameAPI

- 描述

    获取可破坏物编号UI_SCROLLVIEW_TYPE键值对

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

local result = GameAPI.get_destructible_key_ui_scrollview_type_kv(destructible_key, "key")
```

---

## get_tech_key_ui_scrollview_type_kv

method in GameAPI

- 描述

    获取科技编号UI_SCROLLVIEW_TYPE键值对

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

local result = GameAPI.get_tech_key_ui_scrollview_type_kv(tech_key, "key")
```

---

## get_icon_id_ui_scrollview_type_kv

method in GameAPI

- 描述

    获取图片UI_SCROLLVIEW_TYPE键值对

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
local result = GameAPI.get_icon_id_ui_scrollview_type_kv(1, "key")
```

---

## get_physics_entity_key_ui_scrollview_type_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型UI_SCROLLVIEW_TYPE键值对

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
local result = GameAPI.get_physics_entity_key_ui_scrollview_type_kv(1, "key")
```

---

## get_unit_key_ui_anim_kv

method in GameAPI

- 描述

    获取单位编号UI_ANIM键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UIAnimKey | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_ui_anim_kv(unit_key, "key")
```

---

## get_item_key_ui_anim_kv

method in GameAPI

- 描述

    获取物品编号UI_ANIM键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UIAnimKey | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_ui_anim_kv(item_key, "key")
```

---

## get_ability_key_ui_anim_kv

method in GameAPI

- 描述

    获取技能编号UI_ANIM键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UIAnimKey | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_ui_anim_kv(ability_key, "key")
```

---

## get_modifier_key_ui_anim_kv

method in GameAPI

- 描述

    获取魔法效果特效编号UI_ANIM键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UIAnimKey | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_ui_anim_kv(modifier_key, "key")
```

---

## get_projectile_key_ui_anim_kv

method in GameAPI

- 描述

    获取特效编号UI_ANIM键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UIAnimKey | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_ui_anim_kv(projectile_key, "key")
```

---

## get_destructible_key_ui_anim_kv

method in GameAPI

- 描述

    获取可破坏物编号UI_ANIM键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UIAnimKey | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_ui_anim_kv(destructible_key, "key")
```

---

## get_tech_key_ui_anim_kv

method in GameAPI

- 描述

    获取科技编号UI_ANIM键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UIAnimKey | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_ui_anim_kv(tech_key, "key")
```

---

## get_icon_id_ui_anim_kv

method in GameAPI

- 描述

    获取图片UI_ANIM键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UIAnimKey | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_ui_anim_kv(1, "key")
```

---

## get_physics_entity_key_ui_anim_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型UI_ANIM键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UIAnimKey | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_ui_anim_kv(1, "key")
```

---

## get_unit_key_ui_anim_curve_kv

method in GameAPI

- 描述

    获取单位编号UI_ANIM_CURVE键值对

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

local result = GameAPI.get_unit_key_ui_anim_curve_kv(unit_key, "key")
```

---

## get_item_key_ui_anim_curve_kv

method in GameAPI

- 描述

    获取物品编号UI_ANIM_CURVE键值对

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

local result = GameAPI.get_item_key_ui_anim_curve_kv(item_key, "key")
```

---

## get_ability_key_ui_anim_curve_kv

method in GameAPI

- 描述

    获取技能编号UI_ANIM_CURVE键值对

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

local result = GameAPI.get_ability_key_ui_anim_curve_kv(ability_key, "key")
```

---

## get_modifier_key_ui_anim_curve_kv

method in GameAPI

- 描述

    获取魔法效果特效编号UI_ANIM_CURVE键值对

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

local result = GameAPI.get_modifier_key_ui_anim_curve_kv(modifier_key, "key")
```

---

## get_projectile_key_ui_anim_curve_kv

method in GameAPI

- 描述

    获取特效编号UI_ANIM_CURVE键值对

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

local result = GameAPI.get_projectile_key_ui_anim_curve_kv(projectile_key, "key")
```

---

## get_destructible_key_ui_anim_curve_kv

method in GameAPI

- 描述

    获取可破坏物编号UI_ANIM_CURVE键值对

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

local result = GameAPI.get_destructible_key_ui_anim_curve_kv(destructible_key, "key")
```

---

## get_tech_key_ui_anim_curve_kv

method in GameAPI

- 描述

    获取科技编号UI_ANIM_CURVE键值对

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

local result = GameAPI.get_tech_key_ui_anim_curve_kv(tech_key, "key")
```

---

## get_icon_id_ui_anim_curve_kv

method in GameAPI

- 描述

    获取图片UI_ANIM_CURVE键值对

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
local result = GameAPI.get_icon_id_ui_anim_curve_kv(1, "key")
```

---

## get_physics_entity_key_ui_anim_curve_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型UI_ANIM_CURVE键值对

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
local result = GameAPI.get_physics_entity_key_ui_anim_curve_kv(1, "key")
```

---

## get_unit_key_audio_channel_kv

method in GameAPI

- 描述

    获取单位编号AUDIO_CHANNEL键值对

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

local result = GameAPI.get_unit_key_audio_channel_kv(unit_key, "key")
```

---

## get_item_key_audio_channel_kv

method in GameAPI

- 描述

    获取物品编号AUDIO_CHANNEL键值对

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

local result = GameAPI.get_item_key_audio_channel_kv(item_key, "key")
```

---

## get_ability_key_audio_channel_kv

method in GameAPI

- 描述

    获取技能编号AUDIO_CHANNEL键值对

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

local result = GameAPI.get_ability_key_audio_channel_kv(ability_key, "key")
```

---

## get_modifier_key_audio_channel_kv

method in GameAPI

- 描述

    获取魔法效果特效编号AUDIO_CHANNEL键值对

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

local result = GameAPI.get_modifier_key_audio_channel_kv(modifier_key, "key")
```

---

## get_projectile_key_audio_channel_kv

method in GameAPI

- 描述

    获取特效编号AUDIO_CHANNEL键值对

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

local result = GameAPI.get_projectile_key_audio_channel_kv(projectile_key, "key")
```

---

## get_destructible_key_audio_channel_kv

method in GameAPI

- 描述

    获取可破坏物编号AUDIO_CHANNEL键值对

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

local result = GameAPI.get_destructible_key_audio_channel_kv(destructible_key, "key")
```

---

## get_tech_key_audio_channel_kv

method in GameAPI

- 描述

    获取科技编号AUDIO_CHANNEL键值对

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

local result = GameAPI.get_tech_key_audio_channel_kv(tech_key, "key")
```

---

## get_icon_id_audio_channel_kv

method in GameAPI

- 描述

    获取图片AUDIO_CHANNEL键值对

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
local result = GameAPI.get_icon_id_audio_channel_kv(1, "key")
```

---

## get_physics_entity_key_audio_channel_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型AUDIO_CHANNEL键值对

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
local result = GameAPI.get_physics_entity_key_audio_channel_kv(1, "key")
```

---

## get_unit_key_unit_entity_kv

method in GameAPI

- 描述

    获取单位编号UNIT_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_unit_entity_kv(unit_key, "key")
```

---

## get_item_key_unit_entity_kv

method in GameAPI

- 描述

    获取物品编号UNIT_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_unit_entity_kv(item_key, "key")
```

---

## get_ability_key_unit_entity_kv

method in GameAPI

- 描述

    获取技能编号UNIT_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_unit_entity_kv(ability_key, "key")
```

---

## get_modifier_key_unit_entity_kv

method in GameAPI

- 描述

    获取魔法效果特效编号UNIT_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_unit_entity_kv(modifier_key, "key")
```

---

## get_projectile_key_unit_entity_kv

method in GameAPI

- 描述

    获取特效编号UNIT_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_unit_entity_kv(projectile_key, "key")
```

---

## get_destructible_key_unit_entity_kv

method in GameAPI

- 描述

    获取可破坏物编号UNIT_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_unit_entity_kv(destructible_key, "key")
```

---

## get_tech_key_unit_entity_kv

method in GameAPI

- 描述

    获取科技编号UNIT_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_unit_entity_kv(tech_key, "key")
```

---

## get_icon_id_unit_entity_kv

method in GameAPI

- 描述

    获取图片UNIT_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_unit_entity_kv(1, "key")
```

---

## get_physics_entity_key_unit_entity_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型UNIT_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_unit_entity_kv(1, "key")
```

---

## get_unit_key_unit_group_kv

method in GameAPI

- 描述

    获取单位编号UNIT_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitGroup | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_unit_group_kv(unit_key, "key")
```

---

## get_item_key_unit_group_kv

method in GameAPI

- 描述

    获取物品编号UNIT_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitGroup | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_unit_group_kv(item_key, "key")
```

---

## get_ability_key_unit_group_kv

method in GameAPI

- 描述

    获取技能编号UNIT_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitGroup | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_unit_group_kv(ability_key, "key")
```

---

## get_modifier_key_unit_group_kv

method in GameAPI

- 描述

    获取魔法效果特效编号UNIT_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitGroup | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_unit_group_kv(modifier_key, "key")
```

---

## get_projectile_key_unit_group_kv

method in GameAPI

- 描述

    获取特效编号UNIT_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitGroup | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_unit_group_kv(projectile_key, "key")
```

---

## get_destructible_key_unit_group_kv

method in GameAPI

- 描述

    获取可破坏物编号UNIT_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitGroup | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_unit_group_kv(destructible_key, "key")
```

---

## get_tech_key_unit_group_kv

method in GameAPI

- 描述

    获取科技编号UNIT_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitGroup | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_unit_group_kv(tech_key, "key")
```

---

## get_icon_id_unit_group_kv

method in GameAPI

- 描述

    获取图片UNIT_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitGroup | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_unit_group_kv(1, "key")
```

---

## get_physics_entity_key_unit_group_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型UNIT_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitGroup | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_unit_group_kv(1, "key")
```

---

## get_unit_key_unit_name_kv

method in GameAPI

- 描述

    获取单位编号UNIT_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitKey | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_unit_name_kv(unit_key, "key")
```

---

## get_item_key_unit_name_kv

method in GameAPI

- 描述

    获取物品编号UNIT_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitKey | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_unit_name_kv(item_key, "key")
```

---

## get_ability_key_unit_name_kv

method in GameAPI

- 描述

    获取技能编号UNIT_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitKey | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_unit_name_kv(ability_key, "key")
```

---

## get_modifier_key_unit_name_kv

method in GameAPI

- 描述

    获取魔法效果特效编号UNIT_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitKey | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_unit_name_kv(modifier_key, "key")
```

---

## get_projectile_key_unit_name_kv

method in GameAPI

- 描述

    获取特效编号UNIT_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitKey | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_unit_name_kv(projectile_key, "key")
```

---

## get_destructible_key_unit_name_kv

method in GameAPI

- 描述

    获取可破坏物编号UNIT_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitKey | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_unit_name_kv(destructible_key, "key")
```

---

## get_tech_key_unit_name_kv

method in GameAPI

- 描述

    获取科技编号UNIT_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitKey | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_unit_name_kv(tech_key, "key")
```

---

## get_icon_id_unit_name_kv

method in GameAPI

- 描述

    获取图片UNIT_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitKey | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_unit_name_kv(1, "key")
```

---

## get_physics_entity_key_unit_name_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型UNIT_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitKey | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_unit_name_kv(1, "key")
```

---

## get_unit_key_unit_name_pool_kv

method in GameAPI

- 描述

    获取单位编号UNIT_NAME_POOL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitKeyPool | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_unit_name_pool_kv(unit_key, "key")
```

---

## get_item_key_unit_name_pool_kv

method in GameAPI

- 描述

    获取物品编号UNIT_NAME_POOL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitKeyPool | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_unit_name_pool_kv(item_key, "key")
```

---

## get_ability_key_unit_name_pool_kv

method in GameAPI

- 描述

    获取技能编号UNIT_NAME_POOL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitKeyPool | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_unit_name_pool_kv(ability_key, "key")
```

---

## get_modifier_key_unit_name_pool_kv

method in GameAPI

- 描述

    获取魔法效果特效编号UNIT_NAME_POOL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitKeyPool | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_unit_name_pool_kv(modifier_key, "key")
```

---

## get_projectile_key_unit_name_pool_kv

method in GameAPI

- 描述

    获取特效编号UNIT_NAME_POOL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitKeyPool | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_unit_name_pool_kv(projectile_key, "key")
```

---

## get_destructible_key_unit_name_pool_kv

method in GameAPI

- 描述

    获取可破坏物编号UNIT_NAME_POOL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitKeyPool | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_unit_name_pool_kv(destructible_key, "key")
```

---

## get_tech_key_unit_name_pool_kv

method in GameAPI

- 描述

    获取科技编号UNIT_NAME_POOL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitKeyPool | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_unit_name_pool_kv(tech_key, "key")
```

---

## get_icon_id_unit_name_pool_kv

method in GameAPI

- 描述

    获取图片UNIT_NAME_POOL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitKeyPool | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_unit_name_pool_kv(1, "key")
```

---

## get_physics_entity_key_unit_name_pool_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型UNIT_NAME_POOL键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitKeyPool | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_unit_name_pool_kv(1, "key")
```

---

## get_unit_key_unit_write_attribute_kv

method in GameAPI

- 描述

    获取单位编号UNIT_WRITE_ATTRIBUTE键值对

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

local result = GameAPI.get_unit_key_unit_write_attribute_kv(unit_key, "key")
```

---

## get_item_key_unit_write_attribute_kv

method in GameAPI

- 描述

    获取物品编号UNIT_WRITE_ATTRIBUTE键值对

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

local result = GameAPI.get_item_key_unit_write_attribute_kv(item_key, "key")
```

---

## get_ability_key_unit_write_attribute_kv

method in GameAPI

- 描述

    获取技能编号UNIT_WRITE_ATTRIBUTE键值对

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

local result = GameAPI.get_ability_key_unit_write_attribute_kv(ability_key, "key")
```

---

## get_modifier_key_unit_write_attribute_kv

method in GameAPI

- 描述

    获取魔法效果特效编号UNIT_WRITE_ATTRIBUTE键值对

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

local result = GameAPI.get_modifier_key_unit_write_attribute_kv(modifier_key, "key")
```

---

## get_projectile_key_unit_write_attribute_kv

method in GameAPI

- 描述

    获取特效编号UNIT_WRITE_ATTRIBUTE键值对

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

local result = GameAPI.get_projectile_key_unit_write_attribute_kv(projectile_key, "key")
```

---

## get_destructible_key_unit_write_attribute_kv

method in GameAPI

- 描述

    获取可破坏物编号UNIT_WRITE_ATTRIBUTE键值对

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

local result = GameAPI.get_destructible_key_unit_write_attribute_kv(destructible_key, "key")
```

---

## get_tech_key_unit_write_attribute_kv

method in GameAPI

- 描述

    获取科技编号UNIT_WRITE_ATTRIBUTE键值对

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

local result = GameAPI.get_tech_key_unit_write_attribute_kv(tech_key, "key")
```

---

## get_icon_id_unit_write_attribute_kv

method in GameAPI

- 描述

    获取图片UNIT_WRITE_ATTRIBUTE键值对

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
local result = GameAPI.get_icon_id_unit_write_attribute_kv(1, "key")
```

---

## get_physics_entity_key_unit_write_attribute_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型UNIT_WRITE_ATTRIBUTE键值对

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
local result = GameAPI.get_physics_entity_key_unit_write_attribute_kv(1, "key")
```

---

## get_unit_key_attr_element_kv

method in GameAPI

- 描述

    获取单位编号ATTR_ELEMENT键值对

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

local result = GameAPI.get_unit_key_attr_element_kv(unit_key, "key")
```

---

## get_item_key_attr_element_kv

method in GameAPI

- 描述

    获取物品编号ATTR_ELEMENT键值对

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

local result = GameAPI.get_item_key_attr_element_kv(item_key, "key")
```

---

## get_ability_key_attr_element_kv

method in GameAPI

- 描述

    获取技能编号ATTR_ELEMENT键值对

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

local result = GameAPI.get_ability_key_attr_element_kv(ability_key, "key")
```

---

## get_modifier_key_attr_element_kv

method in GameAPI

- 描述

    获取魔法效果特效编号ATTR_ELEMENT键值对

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

local result = GameAPI.get_modifier_key_attr_element_kv(modifier_key, "key")
```

---

## get_projectile_key_attr_element_kv

method in GameAPI

- 描述

    获取特效编号ATTR_ELEMENT键值对

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

local result = GameAPI.get_projectile_key_attr_element_kv(projectile_key, "key")
```

---

## get_destructible_key_attr_element_kv

method in GameAPI

- 描述

    获取可破坏物编号ATTR_ELEMENT键值对

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

local result = GameAPI.get_destructible_key_attr_element_kv(destructible_key, "key")
```

---

## get_tech_key_attr_element_kv

method in GameAPI

- 描述

    获取科技编号ATTR_ELEMENT键值对

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

local result = GameAPI.get_tech_key_attr_element_kv(tech_key, "key")
```

---

## get_icon_id_attr_element_kv

method in GameAPI

- 描述

    获取图片ATTR_ELEMENT键值对

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
local result = GameAPI.get_icon_id_attr_element_kv(1, "key")
```

---

## get_physics_entity_key_attr_element_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型ATTR_ELEMENT键值对

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
local result = GameAPI.get_physics_entity_key_attr_element_kv(1, "key")
```

---

## get_unit_key_attr_element_read_kv

method in GameAPI

- 描述

    获取单位编号ATTR_ELEMENT_READ键值对

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

local result = GameAPI.get_unit_key_attr_element_read_kv(unit_key, "key")
```

---

## get_item_key_attr_element_read_kv

method in GameAPI

- 描述

    获取物品编号ATTR_ELEMENT_READ键值对

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

local result = GameAPI.get_item_key_attr_element_read_kv(item_key, "key")
```

---

## get_ability_key_attr_element_read_kv

method in GameAPI

- 描述

    获取技能编号ATTR_ELEMENT_READ键值对

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

local result = GameAPI.get_ability_key_attr_element_read_kv(ability_key, "key")
```

---

## get_modifier_key_attr_element_read_kv

method in GameAPI

- 描述

    获取魔法效果特效编号ATTR_ELEMENT_READ键值对

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

local result = GameAPI.get_modifier_key_attr_element_read_kv(modifier_key, "key")
```

---

## get_projectile_key_attr_element_read_kv

method in GameAPI

- 描述

    获取特效编号ATTR_ELEMENT_READ键值对

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

local result = GameAPI.get_projectile_key_attr_element_read_kv(projectile_key, "key")
```

---

## get_destructible_key_attr_element_read_kv

method in GameAPI

- 描述

    获取可破坏物编号ATTR_ELEMENT_READ键值对

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

local result = GameAPI.get_destructible_key_attr_element_read_kv(destructible_key, "key")
```

---

## get_tech_key_attr_element_read_kv

method in GameAPI

- 描述

    获取科技编号ATTR_ELEMENT_READ键值对

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

local result = GameAPI.get_tech_key_attr_element_read_kv(tech_key, "key")
```

---

## get_icon_id_attr_element_read_kv

method in GameAPI

- 描述

    获取图片ATTR_ELEMENT_READ键值对

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
local result = GameAPI.get_icon_id_attr_element_read_kv(1, "key")
```

---

## get_physics_entity_key_attr_element_read_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型ATTR_ELEMENT_READ键值对

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
local result = GameAPI.get_physics_entity_key_attr_element_read_kv(1, "key")
```

---

## get_unit_key_mover_entity_kv

method in GameAPI

- 描述

    获取单位编号MOVER_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Mover | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_mover_entity_kv(unit_key, "key")
```

---

## get_item_key_mover_entity_kv

method in GameAPI

- 描述

    获取物品编号MOVER_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Mover | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_mover_entity_kv(item_key, "key")
```

---

## get_ability_key_mover_entity_kv

method in GameAPI

- 描述

    获取技能编号MOVER_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Mover | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_mover_entity_kv(ability_key, "key")
```

---

## get_modifier_key_mover_entity_kv

method in GameAPI

- 描述

    获取魔法效果特效编号MOVER_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Mover | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_mover_entity_kv(modifier_key, "key")
```

---

## get_projectile_key_mover_entity_kv

method in GameAPI

- 描述

    获取特效编号MOVER_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Mover | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_mover_entity_kv(projectile_key, "key")
```

---

## get_destructible_key_mover_entity_kv

method in GameAPI

- 描述

    获取可破坏物编号MOVER_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Mover | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_mover_entity_kv(destructible_key, "key")
```

---

## get_tech_key_mover_entity_kv

method in GameAPI

- 描述

    获取科技编号MOVER_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Mover | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_mover_entity_kv(tech_key, "key")
```

---

## get_icon_id_mover_entity_kv

method in GameAPI

- 描述

    获取图片MOVER_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Mover | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_mover_entity_kv(1, "key")
```

---

## get_physics_entity_key_mover_entity_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型MOVER_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Mover | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_mover_entity_kv(1, "key")
```

---

## get_unit_key_image_quality_kv

method in GameAPI

- 描述

    获取单位编号IMAGE_QUALITY键值对

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

local result = GameAPI.get_unit_key_image_quality_kv(unit_key, "key")
```

---

## get_item_key_image_quality_kv

method in GameAPI

- 描述

    获取物品编号IMAGE_QUALITY键值对

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

local result = GameAPI.get_item_key_image_quality_kv(item_key, "key")
```

---

## get_ability_key_image_quality_kv

method in GameAPI

- 描述

    获取技能编号IMAGE_QUALITY键值对

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

local result = GameAPI.get_ability_key_image_quality_kv(ability_key, "key")
```

---

## get_modifier_key_image_quality_kv

method in GameAPI

- 描述

    获取魔法效果特效编号IMAGE_QUALITY键值对

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

local result = GameAPI.get_modifier_key_image_quality_kv(modifier_key, "key")
```

---

## get_projectile_key_image_quality_kv

method in GameAPI

- 描述

    获取特效编号IMAGE_QUALITY键值对

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

local result = GameAPI.get_projectile_key_image_quality_kv(projectile_key, "key")
```

---

## get_destructible_key_image_quality_kv

method in GameAPI

- 描述

    获取可破坏物编号IMAGE_QUALITY键值对

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

local result = GameAPI.get_destructible_key_image_quality_kv(destructible_key, "key")
```

---

## get_tech_key_image_quality_kv

method in GameAPI

- 描述

    获取科技编号IMAGE_QUALITY键值对

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

local result = GameAPI.get_tech_key_image_quality_kv(tech_key, "key")
```

---

## get_icon_id_image_quality_kv

method in GameAPI

- 描述

    获取图片IMAGE_QUALITY键值对

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
local result = GameAPI.get_icon_id_image_quality_kv(1, "key")
```

---

## get_physics_entity_key_image_quality_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型IMAGE_QUALITY键值对

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
local result = GameAPI.get_physics_entity_key_image_quality_kv(1, "key")
```

---

## get_unit_key_window_type_setting_kv

method in GameAPI

- 描述

    获取单位编号WINDOW_TYPE_SETTING键值对

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

local result = GameAPI.get_unit_key_window_type_setting_kv(unit_key, "key")
```

---

## get_item_key_window_type_setting_kv

method in GameAPI

- 描述

    获取物品编号WINDOW_TYPE_SETTING键值对

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

local result = GameAPI.get_item_key_window_type_setting_kv(item_key, "key")
```

---

## get_ability_key_window_type_setting_kv

method in GameAPI

- 描述

    获取技能编号WINDOW_TYPE_SETTING键值对

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

local result = GameAPI.get_ability_key_window_type_setting_kv(ability_key, "key")
```

---

## get_modifier_key_window_type_setting_kv

method in GameAPI

- 描述

    获取魔法效果特效编号WINDOW_TYPE_SETTING键值对

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

local result = GameAPI.get_modifier_key_window_type_setting_kv(modifier_key, "key")
```

---

## get_projectile_key_window_type_setting_kv

method in GameAPI

- 描述

    获取特效编号WINDOW_TYPE_SETTING键值对

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

local result = GameAPI.get_projectile_key_window_type_setting_kv(projectile_key, "key")
```

---

## get_destructible_key_window_type_setting_kv

method in GameAPI

- 描述

    获取可破坏物编号WINDOW_TYPE_SETTING键值对

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

local result = GameAPI.get_destructible_key_window_type_setting_kv(destructible_key, "key")
```

---

## get_tech_key_window_type_setting_kv

method in GameAPI

- 描述

    获取科技编号WINDOW_TYPE_SETTING键值对

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

local result = GameAPI.get_tech_key_window_type_setting_kv(tech_key, "key")
```

---

## get_icon_id_window_type_setting_kv

method in GameAPI

- 描述

    获取图片WINDOW_TYPE_SETTING键值对

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
local result = GameAPI.get_icon_id_window_type_setting_kv(1, "key")
```

---

## get_physics_entity_key_window_type_setting_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型WINDOW_TYPE_SETTING键值对

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
local result = GameAPI.get_physics_entity_key_window_type_setting_kv(1, "key")
```

---

## get_unit_key_item_entity_kv

method in GameAPI

- 描述

    获取单位编号ITEM_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Item | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_item_entity_kv(unit_key, "key")
```

---

## get_item_key_item_entity_kv

method in GameAPI

- 描述

    获取物品编号ITEM_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Item | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_item_entity_kv(item_key, "key")
```

---

## get_ability_key_item_entity_kv

method in GameAPI

- 描述

    获取技能编号ITEM_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Item | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_item_entity_kv(ability_key, "key")
```

---

## get_modifier_key_item_entity_kv

method in GameAPI

- 描述

    获取魔法效果特效编号ITEM_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Item | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_item_entity_kv(modifier_key, "key")
```

---

## get_projectile_key_item_entity_kv

method in GameAPI

- 描述

    获取特效编号ITEM_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Item | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_item_entity_kv(projectile_key, "key")
```

---

## get_destructible_key_item_entity_kv

method in GameAPI

- 描述

    获取可破坏物编号ITEM_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Item | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_item_entity_kv(destructible_key, "key")
```

---

## get_tech_key_item_entity_kv

method in GameAPI

- 描述

    获取科技编号ITEM_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Item | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_item_entity_kv(tech_key, "key")
```

---

## get_icon_id_item_entity_kv

method in GameAPI

- 描述

    获取图片ITEM_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Item | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_item_entity_kv(1, "key")
```

---

## get_physics_entity_key_item_entity_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型ITEM_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Item | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_item_entity_kv(1, "key")
```

---

## get_unit_key_item_group_kv

method in GameAPI

- 描述

    获取单位编号ITEM_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemGroup | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_item_group_kv(unit_key, "key")
```

---

## get_item_key_item_group_kv

method in GameAPI

- 描述

    获取物品编号ITEM_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemGroup | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_item_group_kv(item_key, "key")
```

---

## get_ability_key_item_group_kv

method in GameAPI

- 描述

    获取技能编号ITEM_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemGroup | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_item_group_kv(ability_key, "key")
```

---

## get_modifier_key_item_group_kv

method in GameAPI

- 描述

    获取魔法效果特效编号ITEM_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemGroup | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_item_group_kv(modifier_key, "key")
```

---

## get_projectile_key_item_group_kv

method in GameAPI

- 描述

    获取特效编号ITEM_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemGroup | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_item_group_kv(projectile_key, "key")
```

---

## get_destructible_key_item_group_kv

method in GameAPI

- 描述

    获取可破坏物编号ITEM_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemGroup | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_item_group_kv(destructible_key, "key")
```

---

## get_tech_key_item_group_kv

method in GameAPI

- 描述

    获取科技编号ITEM_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemGroup | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_item_group_kv(tech_key, "key")
```

---

## get_icon_id_item_group_kv

method in GameAPI

- 描述

    获取图片ITEM_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemGroup | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_item_group_kv(1, "key")
```

---

## get_physics_entity_key_item_group_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型ITEM_GROUP键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemGroup | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_item_group_kv(1, "key")
```

---

## get_unit_key_item_name_kv

method in GameAPI

- 描述

    获取单位编号ITEM_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemKey | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_item_name_kv(unit_key, "key")
```

---

## get_item_key_item_name_kv

method in GameAPI

- 描述

    获取物品编号ITEM_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemKey | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_item_name_kv(item_key, "key")
```

---

## get_ability_key_item_name_kv

method in GameAPI

- 描述

    获取技能编号ITEM_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemKey | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_item_name_kv(ability_key, "key")
```

---

## get_modifier_key_item_name_kv

method in GameAPI

- 描述

    获取魔法效果特效编号ITEM_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemKey | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_item_name_kv(modifier_key, "key")
```

---

## get_projectile_key_item_name_kv

method in GameAPI

- 描述

    获取特效编号ITEM_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemKey | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_item_name_kv(projectile_key, "key")
```

---

## get_destructible_key_item_name_kv

method in GameAPI

- 描述

    获取可破坏物编号ITEM_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemKey | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_item_name_kv(destructible_key, "key")
```

---

## get_tech_key_item_name_kv

method in GameAPI

- 描述

    获取科技编号ITEM_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemKey | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_item_name_kv(tech_key, "key")
```

---

## get_icon_id_item_name_kv

method in GameAPI

- 描述

    获取图片ITEM_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemKey | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_item_name_kv(1, "key")
```

---

## get_physics_entity_key_item_name_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型ITEM_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemKey | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_item_name_kv(1, "key")
```

---

## get_unit_key_ability_kv

method in GameAPI

- 描述

    获取单位编号ABILITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Ability | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_ability_kv(unit_key, "key")
```

---

## get_item_key_ability_kv

method in GameAPI

- 描述

    获取物品编号ABILITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Ability | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_ability_kv(item_key, "key")
```

---

## get_ability_key_ability_kv

method in GameAPI

- 描述

    获取技能编号ABILITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Ability | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_ability_kv(ability_key, "key")
```

---

## get_modifier_key_ability_kv

method in GameAPI

- 描述

    获取魔法效果特效编号ABILITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Ability | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_ability_kv(modifier_key, "key")
```

---

## get_projectile_key_ability_kv

method in GameAPI

- 描述

    获取特效编号ABILITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Ability | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_ability_kv(projectile_key, "key")
```

---

## get_destructible_key_ability_kv

method in GameAPI

- 描述

    获取可破坏物编号ABILITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Ability | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_ability_kv(destructible_key, "key")
```

---

## get_tech_key_ability_kv

method in GameAPI

- 描述

    获取科技编号ABILITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Ability | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_ability_kv(tech_key, "key")
```

---

## get_icon_id_ability_kv

method in GameAPI

- 描述

    获取图片ABILITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Ability | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_ability_kv(1, "key")
```

---

## get_physics_entity_key_ability_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型ABILITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Ability | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_ability_kv(1, "key")
```

---

## get_unit_key_ability_type_kv

method in GameAPI

- 描述

    获取单位编号ABILITY_TYPE键值对

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

local result = GameAPI.get_unit_key_ability_type_kv(unit_key, "key")
```

---

## get_item_key_ability_type_kv

method in GameAPI

- 描述

    获取物品编号ABILITY_TYPE键值对

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

local result = GameAPI.get_item_key_ability_type_kv(item_key, "key")
```

---

## get_ability_key_ability_type_kv

method in GameAPI

- 描述

    获取技能编号ABILITY_TYPE键值对

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

local result = GameAPI.get_ability_key_ability_type_kv(ability_key, "key")
```

---

## get_modifier_key_ability_type_kv

method in GameAPI

- 描述

    获取魔法效果特效编号ABILITY_TYPE键值对

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

local result = GameAPI.get_modifier_key_ability_type_kv(modifier_key, "key")
```

---

## get_projectile_key_ability_type_kv

method in GameAPI

- 描述

    获取特效编号ABILITY_TYPE键值对

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

local result = GameAPI.get_projectile_key_ability_type_kv(projectile_key, "key")
```

---

## get_destructible_key_ability_type_kv

method in GameAPI

- 描述

    获取可破坏物编号ABILITY_TYPE键值对

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

local result = GameAPI.get_destructible_key_ability_type_kv(destructible_key, "key")
```

---

## get_tech_key_ability_type_kv

method in GameAPI

- 描述

    获取科技编号ABILITY_TYPE键值对

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

local result = GameAPI.get_tech_key_ability_type_kv(tech_key, "key")
```

---

## get_icon_id_ability_type_kv

method in GameAPI

- 描述

    获取图片ABILITY_TYPE键值对

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
local result = GameAPI.get_icon_id_ability_type_kv(1, "key")
```

---

## get_physics_entity_key_ability_type_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型ABILITY_TYPE键值对

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
local result = GameAPI.get_physics_entity_key_ability_type_kv(1, "key")
```

---

## get_unit_key_ability_cast_type_kv

method in GameAPI

- 描述

    获取单位编号ABILITY_CAST_TYPE键值对

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

local result = GameAPI.get_unit_key_ability_cast_type_kv(unit_key, "key")
```

---

## get_item_key_ability_cast_type_kv

method in GameAPI

- 描述

    获取物品编号ABILITY_CAST_TYPE键值对

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

local result = GameAPI.get_item_key_ability_cast_type_kv(item_key, "key")
```

---

## get_ability_key_ability_cast_type_kv

method in GameAPI

- 描述

    获取技能编号ABILITY_CAST_TYPE键值对

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

local result = GameAPI.get_ability_key_ability_cast_type_kv(ability_key, "key")
```

---

## get_modifier_key_ability_cast_type_kv

method in GameAPI

- 描述

    获取魔法效果特效编号ABILITY_CAST_TYPE键值对

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

local result = GameAPI.get_modifier_key_ability_cast_type_kv(modifier_key, "key")
```

---

## get_projectile_key_ability_cast_type_kv

method in GameAPI

- 描述

    获取特效编号ABILITY_CAST_TYPE键值对

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

local result = GameAPI.get_projectile_key_ability_cast_type_kv(projectile_key, "key")
```

---

## get_destructible_key_ability_cast_type_kv

method in GameAPI

- 描述

    获取可破坏物编号ABILITY_CAST_TYPE键值对

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

local result = GameAPI.get_destructible_key_ability_cast_type_kv(destructible_key, "key")
```

---

## get_tech_key_ability_cast_type_kv

method in GameAPI

- 描述

    获取科技编号ABILITY_CAST_TYPE键值对

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

local result = GameAPI.get_tech_key_ability_cast_type_kv(tech_key, "key")
```

---

## get_icon_id_ability_cast_type_kv

method in GameAPI

- 描述

    获取图片ABILITY_CAST_TYPE键值对

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
local result = GameAPI.get_icon_id_ability_cast_type_kv(1, "key")
```

---

## get_physics_entity_key_ability_cast_type_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型ABILITY_CAST_TYPE键值对

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
local result = GameAPI.get_physics_entity_key_ability_cast_type_kv(1, "key")
```

---

## get_unit_key_ability_name_kv

method in GameAPI

- 描述

    获取单位编号ABILITY_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityKey | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_ability_name_kv(unit_key, "key")
```

---

## get_item_key_ability_name_kv

method in GameAPI

- 描述

    获取物品编号ABILITY_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityKey | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_ability_name_kv(item_key, "key")
```

---

## get_ability_key_ability_name_kv

method in GameAPI

- 描述

    获取技能编号ABILITY_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityKey | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_ability_name_kv(ability_key, "key")
```

---

## get_modifier_key_ability_name_kv

method in GameAPI

- 描述

    获取魔法效果特效编号ABILITY_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityKey | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_ability_name_kv(modifier_key, "key")
```

---

## get_projectile_key_ability_name_kv

method in GameAPI

- 描述

    获取特效编号ABILITY_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityKey | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_ability_name_kv(projectile_key, "key")
```

---

## get_destructible_key_ability_name_kv

method in GameAPI

- 描述

    获取可破坏物编号ABILITY_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityKey | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_ability_name_kv(destructible_key, "key")
```

---

## get_tech_key_ability_name_kv

method in GameAPI

- 描述

    获取科技编号ABILITY_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityKey | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_ability_name_kv(tech_key, "key")
```

---

## get_icon_id_ability_name_kv

method in GameAPI

- 描述

    获取图片ABILITY_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityKey | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_ability_name_kv(1, "key")
```

---

## get_physics_entity_key_ability_name_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型ABILITY_NAME键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityKey | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_ability_name_kv(1, "key")
```

---

## get_unit_key_skill_pointer_type_kv

method in GameAPI

- 描述

    获取单位编号SKILL_POINTER_TYPE键值对

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

local result = GameAPI.get_unit_key_skill_pointer_type_kv(unit_key, "key")
```

---

## get_item_key_skill_pointer_type_kv

method in GameAPI

- 描述

    获取物品编号SKILL_POINTER_TYPE键值对

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

local result = GameAPI.get_item_key_skill_pointer_type_kv(item_key, "key")
```

---

## get_ability_key_skill_pointer_type_kv

method in GameAPI

- 描述

    获取技能编号SKILL_POINTER_TYPE键值对

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

local result = GameAPI.get_ability_key_skill_pointer_type_kv(ability_key, "key")
```

---

## get_modifier_key_skill_pointer_type_kv

method in GameAPI

- 描述

    获取魔法效果特效编号SKILL_POINTER_TYPE键值对

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

local result = GameAPI.get_modifier_key_skill_pointer_type_kv(modifier_key, "key")
```

---

## get_projectile_key_skill_pointer_type_kv

method in GameAPI

- 描述

    获取特效编号SKILL_POINTER_TYPE键值对

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

local result = GameAPI.get_projectile_key_skill_pointer_type_kv(projectile_key, "key")
```

---

## get_destructible_key_skill_pointer_type_kv

method in GameAPI

- 描述

    获取可破坏物编号SKILL_POINTER_TYPE键值对

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

local result = GameAPI.get_destructible_key_skill_pointer_type_kv(destructible_key, "key")
```

---

## get_tech_key_skill_pointer_type_kv

method in GameAPI

- 描述

    获取科技编号SKILL_POINTER_TYPE键值对

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

local result = GameAPI.get_tech_key_skill_pointer_type_kv(tech_key, "key")
```

---

## get_icon_id_skill_pointer_type_kv

method in GameAPI

- 描述

    获取图片SKILL_POINTER_TYPE键值对

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
local result = GameAPI.get_icon_id_skill_pointer_type_kv(1, "key")
```

---

## get_physics_entity_key_skill_pointer_type_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型SKILL_POINTER_TYPE键值对

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
local result = GameAPI.get_physics_entity_key_skill_pointer_type_kv(1, "key")
```

---

## get_unit_key_modifier_entity_kv

method in GameAPI

- 描述

    获取单位编号MODIFIER_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierEntity | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_modifier_entity_kv(unit_key, "key")
```

---

## get_item_key_modifier_entity_kv

method in GameAPI

- 描述

    获取物品编号MODIFIER_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierEntity | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_modifier_entity_kv(item_key, "key")
```

---

## get_ability_key_modifier_entity_kv

method in GameAPI

- 描述

    获取技能编号MODIFIER_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierEntity | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_modifier_entity_kv(ability_key, "key")
```

---

## get_modifier_key_modifier_entity_kv

method in GameAPI

- 描述

    获取魔法效果特效编号MODIFIER_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierEntity | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_modifier_entity_kv(modifier_key, "key")
```

---

## get_projectile_key_modifier_entity_kv

method in GameAPI

- 描述

    获取特效编号MODIFIER_ENTITY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierEntity | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_modifier_entity_kv(projectile_key, "key")
```

---

## get_trigger_list_actor_variable_all_goods_key

method in GameAPI

- 描述

    获取触发器GOODS_KEY 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_goods_key(actor, "key")
```

---

## get_trigger_variable_map

method in GameAPI

- 描述

    获取全局触发器MAP非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Map | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_map("key")
```

---

## get_trigger_actor_variable_map

method in GameAPI

- 描述

    获取触发器MAP非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Map | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_map(actor, "key")
```

---

## get_trigger_list_variable_map

method in GameAPI

- 描述

    获取全局触发器MAP数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Map | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_map("key", 1)
```

---

## get_trigger_list_actor_variable_map

method in GameAPI

- 描述

    获取触发器MAP数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Map | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_map(actor, "key", 1)
```

---

## get_trigger_list_variable_all_map

method in GameAPI

- 描述

    获取全局触发器MAP数组变量

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
local result = GameAPI.get_trigger_list_variable_all_map("key")
```

---

## get_trigger_list_actor_variable_all_map

method in GameAPI

- 描述

    获取触发器MAP 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_map(actor, "key")
```

---

## get_trigger_variable_store_item_type

method in GameAPI

- 描述

    获取全局触发器STORE_ITEM_TYPE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.StoreItemType | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_store_item_type("key")
```

---

## get_trigger_actor_variable_store_item_type

method in GameAPI

- 描述

    获取触发器STORE_ITEM_TYPE非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.StoreItemType | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_store_item_type(actor, "key")
```

---

## get_trigger_list_variable_store_item_type

method in GameAPI

- 描述

    获取全局触发器STORE_ITEM_TYPE数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.StoreItemType | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_store_item_type("key", 1)
```

---

## get_trigger_list_actor_variable_store_item_type

method in GameAPI

- 描述

    获取触发器STORE_ITEM_TYPE数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.StoreItemType | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_store_item_type(actor, "key", 1)
```

---

## get_trigger_list_variable_all_store_item_type

method in GameAPI

- 描述

    获取全局触发器STORE_ITEM_TYPE数组变量

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
local result = GameAPI.get_trigger_list_variable_all_store_item_type("key")
```

---

## get_trigger_list_actor_variable_all_store_item_type

method in GameAPI

- 描述

    获取触发器STORE_ITEM_TYPE 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_store_item_type(actor, "key")
```

---

## get_trigger_variable_site_state

method in GameAPI

- 描述

    获取全局触发器SITE_STATE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SITE_STATE | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_site_state("key")
```

---

## get_trigger_actor_variable_site_state

method in GameAPI

- 描述

    获取触发器SITE_STATE非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SITE_STATE | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_site_state(actor, "key")
```

---

## get_trigger_list_variable_site_state

method in GameAPI

- 描述

    获取全局触发器SITE_STATE数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SITE_STATE | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_site_state("key", 1)
```

---

## get_trigger_list_actor_variable_site_state

method in GameAPI

- 描述

    获取触发器SITE_STATE数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SITE_STATE | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_site_state(actor, "key", 1)
```

---

## get_trigger_list_variable_all_site_state

method in GameAPI

- 描述

    获取全局触发器SITE_STATE数组变量

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
local result = GameAPI.get_trigger_list_variable_all_site_state("key")
```

---

## get_trigger_list_actor_variable_all_site_state

method in GameAPI

- 描述

    获取触发器SITE_STATE 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_site_state(actor, "key")
```

---

## get_trigger_variable_coin_currency

method in GameAPI

- 描述

    获取全局触发器COIN_CURRENCY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.COIN_CURRENCY | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_coin_currency("key")
```

---

## get_trigger_actor_variable_coin_currency

method in GameAPI

- 描述

    获取触发器COIN_CURRENCY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.COIN_CURRENCY | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_coin_currency(actor, "key")
```

---

## get_trigger_list_variable_coin_currency

method in GameAPI

- 描述

    获取全局触发器COIN_CURRENCY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.COIN_CURRENCY | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_coin_currency("key", 1)
```

---

## get_trigger_list_actor_variable_coin_currency

method in GameAPI

- 描述

    获取触发器COIN_CURRENCY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.COIN_CURRENCY | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_coin_currency(actor, "key", 1)
```

---

## get_trigger_list_variable_all_coin_currency

method in GameAPI

- 描述

    获取全局触发器COIN_CURRENCY数组变量

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
local result = GameAPI.get_trigger_list_variable_all_coin_currency("key")
```

---

## get_trigger_list_actor_variable_all_coin_currency

method in GameAPI

- 描述

    获取触发器COIN_CURRENCY 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_coin_currency(actor, "key")
```

---

## set_trigger_list_variable_ui_gridview_type

method in GameAPI

- 描述

    设置全局触发器UI_GRIDVIEW_TYPE数组变量子项

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
GameAPI.set_trigger_list_variable_ui_gridview_type("key", 1, 1)
```

---

## set_trigger_list_actor_variable_ui_gridview_type

method in GameAPI

- 描述

    设置全局触发器UI_GRIDVIEW_TYPE数组 组变量子项

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

GameAPI.set_trigger_list_actor_variable_ui_gridview_type(actor, "key", 1, 1)
```

---

## set_trigger_variable_ui_gridview_type

method in GameAPI

- 描述

    设置全局触发器UI_GRIDVIEW_TYPE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | integer | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_ui_gridview_type("key", 1)
```

---

## set_trigger_actor_variable_ui_gridview_type

method in GameAPI

- 描述

    设置全局触发器UI_GRIDVIEW_TYPE非数组 组变量

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

GameAPI.set_trigger_actor_variable_ui_gridview_type(actor, "key", 1)
```

---

## set_trigger_list_variable_ui_gridview_bar_type

method in GameAPI

- 描述

    设置全局触发器UI_GRIDVIEW_BAR_TYPE数组变量子项

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
GameAPI.set_trigger_list_variable_ui_gridview_bar_type("key", 1, 1)
```

---

## set_trigger_list_actor_variable_ui_gridview_bar_type

method in GameAPI

- 描述

    设置全局触发器UI_GRIDVIEW_BAR_TYPE数组 组变量子项

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

GameAPI.set_trigger_list_actor_variable_ui_gridview_bar_type(actor, "key", 1, 1)
```

---

## set_trigger_variable_ui_gridview_bar_type

method in GameAPI

- 描述

    设置全局触发器UI_GRIDVIEW_BAR_TYPE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | integer | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_ui_gridview_bar_type("key", 1)
```

---

## set_trigger_actor_variable_ui_gridview_bar_type

method in GameAPI

- 描述

    设置全局触发器UI_GRIDVIEW_BAR_TYPE非数组 组变量

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

GameAPI.set_trigger_actor_variable_ui_gridview_bar_type(actor, "key", 1)
```

---

## set_trigger_list_variable_ui_effect_camera_mode

method in GameAPI

- 描述

    设置全局触发器UI_EFFECT_CAMERA_MODE数组变量子项

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
GameAPI.set_trigger_list_variable_ui_effect_camera_mode("key", 1, 1)
```

---

## set_trigger_list_actor_variable_ui_effect_camera_mode

method in GameAPI

- 描述

    设置全局触发器UI_EFFECT_CAMERA_MODE数组 组变量子项

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

GameAPI.set_trigger_list_actor_variable_ui_effect_camera_mode(actor, "key", 1, 1)
```

---

## set_trigger_variable_ui_effect_camera_mode

method in GameAPI

- 描述

    设置全局触发器UI_EFFECT_CAMERA_MODE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | integer | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_ui_effect_camera_mode("key", 1)
```

---

## set_trigger_actor_variable_ui_effect_camera_mode

method in GameAPI

- 描述

    设置全局触发器UI_EFFECT_CAMERA_MODE非数组 组变量

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

GameAPI.set_trigger_actor_variable_ui_effect_camera_mode(actor, "key", 1)
```

---

## set_trigger_list_variable_ui_equip_slot_use_type

method in GameAPI

- 描述

    设置全局触发器UI_EQUIP_SLOT_USE_TYPE数组变量子项

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
GameAPI.set_trigger_list_variable_ui_equip_slot_use_type("key", 1, 1)
```

---

## set_trigger_list_actor_variable_ui_equip_slot_use_type

method in GameAPI

- 描述

    设置全局触发器UI_EQUIP_SLOT_USE_TYPE数组 组变量子项

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

GameAPI.set_trigger_list_actor_variable_ui_equip_slot_use_type(actor, "key", 1, 1)
```

---

## set_trigger_variable_ui_equip_slot_use_type

method in GameAPI

- 描述

    设置全局触发器UI_EQUIP_SLOT_USE_TYPE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | integer | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_ui_equip_slot_use_type("key", 1)
```

---

## set_trigger_actor_variable_ui_equip_slot_use_type

method in GameAPI

- 描述

    设置全局触发器UI_EQUIP_SLOT_USE_TYPE非数组 组变量

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

GameAPI.set_trigger_actor_variable_ui_equip_slot_use_type(actor, "key", 1)
```

---

## set_trigger_list_variable_ui_equip_slot_drag_type

method in GameAPI

- 描述

    设置全局触发器UI_EQUIP_SLOT_DRAG_TYPE数组变量子项

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
GameAPI.set_trigger_list_variable_ui_equip_slot_drag_type("key", 1, 1)
```

---

## set_trigger_list_actor_variable_ui_equip_slot_drag_type

method in GameAPI

- 描述

    设置全局触发器UI_EQUIP_SLOT_DRAG_TYPE数组 组变量子项

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

GameAPI.set_trigger_list_actor_variable_ui_equip_slot_drag_type(actor, "key", 1, 1)
```

---

## set_trigger_variable_ui_equip_slot_drag_type

method in GameAPI

- 描述

    设置全局触发器UI_EQUIP_SLOT_DRAG_TYPE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | integer | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_ui_equip_slot_drag_type("key", 1)
```

---

## set_trigger_actor_variable_ui_equip_slot_drag_type

method in GameAPI

- 描述

    设置全局触发器UI_EQUIP_SLOT_DRAG_TYPE非数组 组变量

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

GameAPI.set_trigger_actor_variable_ui_equip_slot_drag_type(actor, "key", 1)
```

---

## set_trigger_list_variable_ui_layout_clipping_type

method in GameAPI

- 描述

    设置全局触发器UI_LAYOUT_CLIPPING_TYPE数组变量子项

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
GameAPI.set_trigger_list_variable_ui_layout_clipping_type("key", 1, 1)
```

---

## set_trigger_list_actor_variable_ui_layout_clipping_type

method in GameAPI

- 描述

    设置全局触发器UI_LAYOUT_CLIPPING_TYPE数组 组变量子项

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

GameAPI.set_trigger_list_actor_variable_ui_layout_clipping_type(actor, "key", 1, 1)
```

---

## set_trigger_variable_ui_layout_clipping_type

method in GameAPI

- 描述

    设置全局触发器UI_LAYOUT_CLIPPING_TYPE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | integer | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_ui_layout_clipping_type("key", 1)
```

---

## set_trigger_actor_variable_ui_layout_clipping_type

method in GameAPI

- 描述

    设置全局触发器UI_LAYOUT_CLIPPING_TYPE非数组 组变量

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

GameAPI.set_trigger_actor_variable_ui_layout_clipping_type(actor, "key", 1)
```

---

## set_trigger_list_variable_ui_text_over_length_handling_type

method in GameAPI

- 描述

    设置全局触发器UI_TEXT_OVER_LENGTH_HANDLING_TYPE数组变量子项

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
GameAPI.set_trigger_list_variable_ui_text_over_length_handling_type("key", 1, 1)
```

---

## set_trigger_list_actor_variable_ui_text_over_length_handling_type

method in GameAPI

- 描述

    设置全局触发器UI_TEXT_OVER_LENGTH_HANDLING_TYPE数组 组变量子项

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

GameAPI.set_trigger_list_actor_variable_ui_text_over_length_handling_type(actor, "key", 1, 1)
```

---

## set_trigger_variable_ui_text_over_length_handling_type

method in GameAPI

- 描述

    设置全局触发器UI_TEXT_OVER_LENGTH_HANDLING_TYPE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | integer | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_ui_text_over_length_handling_type("key", 1)
```

---

## set_trigger_actor_variable_ui_text_over_length_handling_type

method in GameAPI

- 描述

    设置全局触发器UI_TEXT_OVER_LENGTH_HANDLING_TYPE非数组 组变量

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

GameAPI.set_trigger_actor_variable_ui_text_over_length_handling_type(actor, "key", 1)
```

---

## set_trigger_list_variable_ui_pos_adapt_mode

method in GameAPI

- 描述

    设置全局触发器UI_POS_ADAPT_MODE数组变量子项

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
GameAPI.set_trigger_list_variable_ui_pos_adapt_mode("key", 1, 1)
```

---

## set_trigger_list_actor_variable_ui_pos_adapt_mode

method in GameAPI

- 描述

    设置全局触发器UI_POS_ADAPT_MODE数组 组变量子项

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

GameAPI.set_trigger_list_actor_variable_ui_pos_adapt_mode(actor, "key", 1, 1)
```

---

## set_trigger_variable_ui_pos_adapt_mode

method in GameAPI

- 描述

    设置全局触发器UI_POS_ADAPT_MODE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | integer | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_ui_pos_adapt_mode("key", 1)
```

---

## set_trigger_actor_variable_ui_pos_adapt_mode

method in GameAPI

- 描述

    设置全局触发器UI_POS_ADAPT_MODE非数组 组变量

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

GameAPI.set_trigger_actor_variable_ui_pos_adapt_mode(actor, "key", 1)
```

---

## set_trigger_list_variable_ui_chat_send_channel

method in GameAPI

- 描述

    设置全局触发器UI_CHAT_SEND_CHANNEL数组变量子项

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
GameAPI.set_trigger_list_variable_ui_chat_send_channel("key", 1, 1)
```

---

## set_trigger_list_actor_variable_ui_chat_send_channel

method in GameAPI

- 描述

    设置全局触发器UI_CHAT_SEND_CHANNEL数组 组变量子项

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

GameAPI.set_trigger_list_actor_variable_ui_chat_send_channel(actor, "key", 1, 1)
```

---

## set_trigger_variable_ui_chat_send_channel

method in GameAPI

- 描述

    设置全局触发器UI_CHAT_SEND_CHANNEL非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | integer | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_ui_chat_send_channel("key", 1)
```

---

## set_trigger_actor_variable_ui_chat_send_channel

method in GameAPI

- 描述

    设置全局触发器UI_CHAT_SEND_CHANNEL非数组 组变量

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

GameAPI.set_trigger_actor_variable_ui_chat_send_channel(actor, "key", 1)
```

---

## set_trigger_list_variable_ui_chat_recv_channel

method in GameAPI

- 描述

    设置全局触发器UI_CHAT_RECV_CHANNEL数组变量子项

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
GameAPI.set_trigger_list_variable_ui_chat_recv_channel("key", 1, 1)
```

---

## set_trigger_list_actor_variable_ui_chat_recv_channel

method in GameAPI

- 描述

    设置全局触发器UI_CHAT_RECV_CHANNEL数组 组变量子项

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

GameAPI.set_trigger_list_actor_variable_ui_chat_recv_channel(actor, "key", 1, 1)
```

---

## set_trigger_variable_ui_chat_recv_channel

method in GameAPI

- 描述

    设置全局触发器UI_CHAT_RECV_CHANNEL非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | integer | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_ui_chat_recv_channel("key", 1)
```

---

## set_trigger_actor_variable_ui_chat_recv_channel

method in GameAPI

- 描述

    设置全局触发器UI_CHAT_RECV_CHANNEL非数组 组变量

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

GameAPI.set_trigger_actor_variable_ui_chat_recv_channel(actor, "key", 1)
```

---

## set_trigger_list_variable_ui_anim_play_mode

method in GameAPI

- 描述

    设置全局触发器UI_ANIM_PLAY_MODE数组变量子项

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
GameAPI.set_trigger_list_variable_ui_anim_play_mode("key", 1, 1)
```

---

## set_trigger_list_actor_variable_ui_anim_play_mode

method in GameAPI

- 描述

    设置全局触发器UI_ANIM_PLAY_MODE数组 组变量子项

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

GameAPI.set_trigger_list_actor_variable_ui_anim_play_mode(actor, "key", 1, 1)
```

---

## set_trigger_variable_ui_anim_play_mode

method in GameAPI

- 描述

    设置全局触发器UI_ANIM_PLAY_MODE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | integer | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_ui_anim_play_mode("key", 1)
```

---

## set_trigger_actor_variable_ui_anim_play_mode

method in GameAPI

- 描述

    设置全局触发器UI_ANIM_PLAY_MODE非数组 组变量

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

GameAPI.set_trigger_actor_variable_ui_anim_play_mode(actor, "key", 1)
```

---

## set_trigger_list_variable_ui_text_font_name

method in GameAPI

- 描述

    设置全局触发器UI_TEXT_FONT_NAME数组变量子项

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
GameAPI.set_trigger_list_variable_ui_text_font_name("key", 1, "value")
```

---

## set_trigger_list_actor_variable_ui_text_font_name

method in GameAPI

- 描述

    设置全局触发器UI_TEXT_FONT_NAME数组 组变量子项

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

GameAPI.set_trigger_list_actor_variable_ui_text_font_name(actor, "key", 1, "value")
```

---

## set_trigger_variable_ui_text_font_name

method in GameAPI

- 描述

    设置全局触发器UI_TEXT_FONT_NAME非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | string | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_ui_text_font_name("key", "value")
```

---

## set_trigger_actor_variable_ui_text_font_name

method in GameAPI

- 描述

    设置全局触发器UI_TEXT_FONT_NAME非数组 组变量

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

GameAPI.set_trigger_actor_variable_ui_text_font_name(actor, "key", "value")
```

---

## set_trigger_list_variable_ui_eca_anim_type

method in GameAPI

- 描述

    设置全局触发器UI_ECA_ANIM_TYPE数组变量子项

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
GameAPI.set_trigger_list_variable_ui_eca_anim_type("key", 1, 1)
```

---

## set_trigger_list_actor_variable_ui_eca_anim_type

method in GameAPI

- 描述

    设置全局触发器UI_ECA_ANIM_TYPE数组 组变量子项

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

GameAPI.set_trigger_list_actor_variable_ui_eca_anim_type(actor, "key", 1, 1)
```

---

## set_trigger_variable_ui_eca_anim_type

method in GameAPI

- 描述

    设置全局触发器UI_ECA_ANIM_TYPE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | integer | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_ui_eca_anim_type("key", 1)
```

---

## set_trigger_actor_variable_ui_eca_anim_type

method in GameAPI

- 描述

    设置全局触发器UI_ECA_ANIM_TYPE非数组 组变量

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

GameAPI.set_trigger_actor_variable_ui_eca_anim_type(actor, "key", 1)
```

---

## set_trigger_list_variable_local_unit_entity

method in GameAPI

- 描述

    设置全局触发器LOCAL_UNIT_ENTITY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.LocalUnit | 值 |

- 返回值

    无

- 示例

```lua
local local_unit = GameAPI.create_local_unit(134274569, GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0)), Fix32(1))

GameAPI.set_trigger_list_variable_local_unit_entity("key", 1)
```

---

## set_trigger_list_actor_variable_local_unit_entity

method in GameAPI

- 描述

    设置全局触发器LOCAL_UNIT_ENTITY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.LocalUnit | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local local_unit = GameAPI.create_local_unit(134274569, GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0)), Fix32(1))

GameAPI.set_trigger_list_actor_variable_local_unit_entity(actor, "key", 1)
```

---

## set_trigger_variable_local_unit_entity

method in GameAPI

- 描述

    设置全局触发器LOCAL_UNIT_ENTITY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.LocalUnit | 值 |

- 返回值

    无

- 示例

```lua
local local_unit = GameAPI.create_local_unit(134274569, GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0)), Fix32(1))

GameAPI.set_trigger_variable_local_unit_entity("key")
```

---

## set_trigger_actor_variable_local_unit_entity

method in GameAPI

- 描述

    设置全局触发器LOCAL_UNIT_ENTITY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.LocalUnit | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local local_unit = GameAPI.create_local_unit(134274569, GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0)), Fix32(1))

GameAPI.set_trigger_actor_variable_local_unit_entity(actor, "key")
```

---

## set_trigger_list_variable_local_unit_group

method in GameAPI

- 描述

    设置全局触发器LOCAL_UNIT_GROUP数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.LocalUnitGroup | 值 |

- 返回值

    无

- 示例

```lua
local local_unit_group = GameAPI.get_unit_key_local_unit_group_kv(1, "key")

GameAPI.set_trigger_list_variable_local_unit_group("key", 1)
```

---

## set_trigger_list_actor_variable_local_unit_group

method in GameAPI

- 描述

    设置全局触发器LOCAL_UNIT_GROUP数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.LocalUnitGroup | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local local_unit_group = GameAPI.get_unit_key_local_unit_group_kv(1, "key")

GameAPI.set_trigger_list_actor_variable_local_unit_group(actor, "key", 1)
```

---

## set_trigger_variable_local_unit_group

method in GameAPI

- 描述

    设置全局触发器LOCAL_UNIT_GROUP非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.LocalUnitGroup | 值 |

- 返回值

    无

- 示例

```lua
local local_unit_group = GameAPI.get_unit_key_local_unit_group_kv(1, "key")

GameAPI.set_trigger_variable_local_unit_group("key")
```

---

## set_trigger_actor_variable_local_unit_group

method in GameAPI

- 描述

    设置全局触发器LOCAL_UNIT_GROUP非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.LocalUnitGroup | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local local_unit_group = GameAPI.get_unit_key_local_unit_group_kv(1, "key")

GameAPI.set_trigger_actor_variable_local_unit_group(actor, "key")
```

---

## set_trigger_list_variable_deco_entity

method in GameAPI

- 描述

    设置全局触发器DECO_ENTITY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.DecoID | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_list_variable_deco_entity("key", 1, 1)
```

---

## set_trigger_list_actor_variable_deco_entity

method in GameAPI

- 描述

    设置全局触发器DECO_ENTITY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.DecoID | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_list_actor_variable_deco_entity(actor, "key", 1, 1)
```

---

## set_trigger_variable_deco_entity

method in GameAPI

- 描述

    设置全局触发器DECO_ENTITY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.DecoID | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_deco_entity("key", 1)
```

---

## set_trigger_actor_variable_deco_entity

method in GameAPI

- 描述

    设置全局触发器DECO_ENTITY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.DecoID | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_actor_variable_deco_entity(actor, "key", 1)
```

---

## set_trigger_list_variable_scene_preset

method in GameAPI

- 描述

    设置全局触发器SCENE_PRESET数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.ScenePreset | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_list_variable_scene_preset("key", 1, 1)
```

---

## set_trigger_list_actor_variable_scene_preset

method in GameAPI

- 描述

    设置全局触发器SCENE_PRESET数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.ScenePreset | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_list_actor_variable_scene_preset(actor, "key", 1, 1)
```

---

## set_trigger_variable_scene_preset

method in GameAPI

- 描述

    设置全局触发器SCENE_PRESET非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.ScenePreset | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_scene_preset("key", 1)
```

---

## set_trigger_actor_variable_scene_preset

method in GameAPI

- 描述

    设置全局触发器SCENE_PRESET非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.ScenePreset | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_actor_variable_scene_preset(actor, "key", 1)
```

---

## set_trigger_list_variable_item_stack_type

method in GameAPI

- 描述

    设置全局触发器ITEM_STACK_TYPE数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.ItemStackType | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_list_variable_item_stack_type("key", 1, 1)
```

---

## set_trigger_list_actor_variable_item_stack_type

method in GameAPI

- 描述

    设置全局触发器ITEM_STACK_TYPE数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.ItemStackType | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_list_actor_variable_item_stack_type(actor, "key", 1, 1)
```

---

## set_trigger_variable_item_stack_type

method in GameAPI

- 描述

    设置全局触发器ITEM_STACK_TYPE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.ItemStackType | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_item_stack_type("key", 1)
```

---

## set_trigger_actor_variable_item_stack_type

method in GameAPI

- 描述

    设置全局触发器ITEM_STACK_TYPE非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.ItemStackType | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_actor_variable_item_stack_type(actor, "key", 1)
```

---

## set_trigger_list_variable_ability_release_id

method in GameAPI

- 描述

    设置全局触发器ABILITY_RELEASE_ID数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.AbilityReleaseId | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_list_variable_ability_release_id("key", 1, 1)
```

---

## set_trigger_list_actor_variable_ability_release_id

method in GameAPI

- 描述

    设置全局触发器ABILITY_RELEASE_ID数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.AbilityReleaseId | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_list_actor_variable_ability_release_id(actor, "key", 1, 1)
```

---

## set_trigger_variable_ability_release_id

method in GameAPI

- 描述

    设置全局触发器ABILITY_RELEASE_ID非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.AbilityReleaseId | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_ability_release_id("key", 1)
```

---

## set_trigger_actor_variable_ability_release_id

method in GameAPI

- 描述

    设置全局触发器ABILITY_RELEASE_ID非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.AbilityReleaseId | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_actor_variable_ability_release_id(actor, "key", 1)
```

---

## set_trigger_list_variable_deco_name

method in GameAPI

- 描述

    设置全局触发器DECO_NAME数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.DecoKey | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_list_variable_deco_name("key", 1, 1)
```

---

## set_trigger_list_actor_variable_deco_name

method in GameAPI

- 描述

    设置全局触发器DECO_NAME数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.DecoKey | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_list_actor_variable_deco_name(actor, "key", 1, 1)
```

---

## set_trigger_variable_deco_name

method in GameAPI

- 描述

    设置全局触发器DECO_NAME非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.DecoKey | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_deco_name("key", 1)
```

---

## set_trigger_actor_variable_deco_name

method in GameAPI

- 描述

    设置全局触发器DECO_NAME非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.DecoKey | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_actor_variable_deco_name(actor, "key", 1)
```

---

## set_trigger_list_variable_ui_point

method in GameAPI

- 描述

    设置全局触发器UI_POINT数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.FUIPoint | 值 |

- 返回值

    无

- 示例

```lua
local fui_point = GameAPI.get_unit_key_ui_point_kv(1, "key")

GameAPI.set_trigger_list_variable_ui_point("key", 1)
```

---

## set_trigger_list_actor_variable_ui_point

method in GameAPI

- 描述

    设置全局触发器UI_POINT数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.FUIPoint | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local fui_point = GameAPI.get_unit_key_ui_point_kv(1, "key")

GameAPI.set_trigger_list_actor_variable_ui_point(actor, "key", 1)
```

---

## set_trigger_variable_ui_point

method in GameAPI

- 描述

    设置全局触发器UI_POINT非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.FUIPoint | 值 |

- 返回值

    无

- 示例

```lua
local fui_point = GameAPI.get_unit_key_ui_point_kv(1, "key")

GameAPI.set_trigger_variable_ui_point("key")
```

---

## set_trigger_actor_variable_ui_point

method in GameAPI

- 描述

    设置全局触发器UI_POINT非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.FUIPoint | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local fui_point = GameAPI.get_unit_key_ui_point_kv(1, "key")

GameAPI.set_trigger_actor_variable_ui_point(actor, "key")
```

---

## set_trigger_list_variable_attach_model_entity

method in GameAPI

- 描述

    设置全局触发器ATTACH_MODEL_ENTITY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.AttachModelEntity | 值 |

- 返回值

    无

- 示例

```lua
local attach_model = GameAPI.get_unit_key_attach_model_entity_kv(1, "key")

GameAPI.set_trigger_list_variable_attach_model_entity("key", 1)
```

---

## set_trigger_list_actor_variable_attach_model_entity

method in GameAPI

- 描述

    设置全局触发器ATTACH_MODEL_ENTITY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.AttachModelEntity | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local attach_model = GameAPI.get_unit_key_attach_model_entity_kv(1, "key")

GameAPI.set_trigger_list_actor_variable_attach_model_entity(actor, "key", 1)
```

---

## set_trigger_variable_attach_model_entity

method in GameAPI

- 描述

    设置全局触发器ATTACH_MODEL_ENTITY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.AttachModelEntity | 值 |

- 返回值

    无

- 示例

```lua
local attach_model = GameAPI.get_unit_key_attach_model_entity_kv(1, "key")

GameAPI.set_trigger_variable_attach_model_entity("key")
```

---

## set_trigger_actor_variable_attach_model_entity

method in GameAPI

- 描述

    设置全局触发器ATTACH_MODEL_ENTITY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.AttachModelEntity | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local attach_model = GameAPI.get_unit_key_attach_model_entity_kv(1, "key")

GameAPI.set_trigger_actor_variable_attach_model_entity(actor, "key")
```

---

## set_trigger_list_variable_live2d

method in GameAPI

- 描述

    设置全局触发器LIVE2D数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Live2dKey | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_list_variable_live2d("key", 1, 1)
```

---

## set_trigger_list_actor_variable_live2d

method in GameAPI

- 描述

    设置全局触发器LIVE2D数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Live2dKey | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_list_actor_variable_live2d(actor, "key", 1, 1)
```

---

## set_trigger_variable_live2d

method in GameAPI

- 描述

    设置全局触发器LIVE2D非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.Live2dKey | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_live2d("key", 1)
```

---

## set_trigger_actor_variable_live2d

method in GameAPI

- 描述

    设置全局触发器LIVE2D非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.Live2dKey | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_actor_variable_live2d(actor, "key", 1)
```

---

## set_trigger_list_variable_spine

method in GameAPI

- 描述

    设置全局触发器SPINE数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Spine | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_list_variable_spine("key", 1, 1)
```

---

## set_trigger_list_actor_variable_spine

method in GameAPI

- 描述

    设置全局触发器SPINE数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Spine | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_list_actor_variable_spine(actor, "key", 1, 1)
```

---

## set_trigger_variable_spine

method in GameAPI

- 描述

    设置全局触发器SPINE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.Spine | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_spine("key", 1)
```

---

## set_trigger_actor_variable_spine

method in GameAPI

- 描述

    设置全局触发器SPINE非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.Spine | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_actor_variable_spine(actor, "key", 1)
```

---

## set_trigger_list_variable_debug_shape

method in GameAPI

- 描述

    设置全局触发器DEBUG_SHAPE数组变量子项

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
GameAPI.set_trigger_list_variable_debug_shape("key", 1, 1)
```

---

## set_trigger_list_actor_variable_debug_shape

method in GameAPI

- 描述

    设置全局触发器DEBUG_SHAPE数组 组变量子项

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

GameAPI.set_trigger_list_actor_variable_debug_shape(actor, "key", 1, 1)
```

---

## set_trigger_variable_debug_shape

method in GameAPI

- 描述

    设置全局触发器DEBUG_SHAPE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | integer | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_debug_shape("key", 1)
```

---

## set_trigger_actor_variable_debug_shape

method in GameAPI

- 描述

    设置全局触发器DEBUG_SHAPE非数组 组变量

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

GameAPI.set_trigger_actor_variable_debug_shape(actor, "key", 1)
```

---

## set_trigger_list_variable_watching_mode_status

method in GameAPI

- 描述

    设置全局触发器WATCHING_MODE_STATUS数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.WatchingModeStatus | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_list_variable_watching_mode_status("key", 1, 1)
```

---

## set_trigger_list_actor_variable_watching_mode_status

method in GameAPI

- 描述

    设置全局触发器WATCHING_MODE_STATUS数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.WatchingModeStatus | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_list_actor_variable_watching_mode_status(actor, "key", 1, 1)
```

---

## set_trigger_variable_watching_mode_status

method in GameAPI

- 描述

    设置全局触发器WATCHING_MODE_STATUS非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.WatchingModeStatus | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_watching_mode_status("key", 1)
```

---

## set_trigger_actor_variable_watching_mode_status

method in GameAPI

- 描述

    设置全局触发器WATCHING_MODE_STATUS非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.WatchingModeStatus | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_actor_variable_watching_mode_status(actor, "key", 1)
```

---

## set_trigger_list_variable_force_entity

method in GameAPI

- 描述

    设置全局触发器FORCE_ENTITY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Force | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_list_variable_force_entity("key", 1, 1)
```

---

## set_trigger_list_actor_variable_force_entity

method in GameAPI

- 描述

    设置全局触发器FORCE_ENTITY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Force | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_list_actor_variable_force_entity(actor, "key", 1, 1)
```

---

## set_trigger_variable_force_entity

method in GameAPI

- 描述

    设置全局触发器FORCE_ENTITY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.Force | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_force_entity("key", 1)
```

---

## set_trigger_actor_variable_force_entity

method in GameAPI

- 描述

    设置全局触发器FORCE_ENTITY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.Force | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_actor_variable_force_entity(actor, "key", 1)
```

---

## set_trigger_list_variable_goods_key

method in GameAPI

- 描述

    设置全局触发器GOODS_KEY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.GoodsKey | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_list_variable_goods_key("key", 1, 1)
```

---

## set_trigger_list_actor_variable_goods_key

method in GameAPI

- 描述

    设置全局触发器GOODS_KEY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.GoodsKey | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_list_actor_variable_goods_key(actor, "key", 1, 1)
```

---

## set_trigger_variable_goods_key

method in GameAPI

- 描述

    设置全局触发器GOODS_KEY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.GoodsKey | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_goods_key("key", 1)
```

---

## set_trigger_actor_variable_goods_key

method in GameAPI

- 描述

    设置全局触发器GOODS_KEY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.GoodsKey | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_actor_variable_goods_key(actor, "key", 1)
```

---

## set_trigger_list_variable_map

method in GameAPI

- 描述

    设置全局触发器MAP数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Map | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_list_variable_map("key", 1, 1)
```

---

## set_trigger_list_actor_variable_map

method in GameAPI

- 描述

    设置全局触发器MAP数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.Map | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_list_actor_variable_map(actor, "key", 1, 1)
```

---

## set_trigger_variable_map

method in GameAPI

- 描述

    设置全局触发器MAP非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.Map | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_map("key", 1)
```

---

## set_trigger_actor_variable_map

method in GameAPI

- 描述

    设置全局触发器MAP非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.Map | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_actor_variable_map(actor, "key", 1)
```

---

## set_trigger_list_variable_store_item_type

method in GameAPI

- 描述

    设置全局触发器STORE_ITEM_TYPE数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.StoreItemType | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_list_variable_store_item_type("key", 1, 1)
```

---

## set_trigger_list_actor_variable_store_item_type

method in GameAPI

- 描述

    设置全局触发器STORE_ITEM_TYPE数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.StoreItemType | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_list_actor_variable_store_item_type(actor, "key", 1, 1)
```

---

## set_trigger_variable_store_item_type

method in GameAPI

- 描述

    设置全局触发器STORE_ITEM_TYPE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.StoreItemType | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_store_item_type("key", 1)
```

---

## set_trigger_actor_variable_store_item_type

method in GameAPI

- 描述

    设置全局触发器STORE_ITEM_TYPE非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.StoreItemType | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_actor_variable_store_item_type(actor, "key", 1)
```

---

## set_trigger_list_variable_site_state

method in GameAPI

- 描述

    设置全局触发器SITE_STATE数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.SITE_STATE | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_list_variable_site_state("key", 1, 1)
```

---

## set_trigger_list_actor_variable_site_state

method in GameAPI

- 描述

    设置全局触发器SITE_STATE数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.SITE_STATE | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_list_actor_variable_site_state(actor, "key", 1, 1)
```

---

## set_trigger_variable_site_state

method in GameAPI

- 描述

    设置全局触发器SITE_STATE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.SITE_STATE | 值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_trigger_variable_site_state("key", 1)
```

---

## set_trigger_actor_variable_site_state

method in GameAPI

- 描述

    设置全局触发器SITE_STATE非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.SITE_STATE | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_trigger_actor_variable_site_state(actor, "key", 1)
```

---

## set_trigger_list_variable_coin_currency

method in GameAPI

- 描述

    设置全局触发器COIN_CURRENCY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.COIN_CURRENCY | 值 |

- 返回值

    无

- 示例

```lua
local coin_currency = "RMB"

GameAPI.set_trigger_list_variable_coin_currency("key", 1)
```

---

## set_trigger_list_actor_variable_coin_currency

method in GameAPI

- 描述

    设置全局触发器COIN_CURRENCY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |
    | value? | py.COIN_CURRENCY | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local coin_currency = "RMB"

GameAPI.set_trigger_list_actor_variable_coin_currency(actor, "key", 1)
```

---

## set_trigger_variable_coin_currency

method in GameAPI

- 描述

    设置全局触发器COIN_CURRENCY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | value? | py.COIN_CURRENCY | 值 |

- 返回值

    无

- 示例

```lua
local coin_currency = "RMB"

GameAPI.set_trigger_variable_coin_currency("key")
```

---

## set_trigger_actor_variable_coin_currency

method in GameAPI

- 描述

    设置全局触发器COIN_CURRENCY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | value? | py.COIN_CURRENCY | 值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local coin_currency = "RMB"

GameAPI.set_trigger_actor_variable_coin_currency(actor, "key")
```

---

## get_deco_entity_list_value

method in GameAPI

- 描述

    获取DECO_ENTITY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DecoID | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_deco_entity_list_value(list, 1)
```

---

## set_deco_entity_list_value

method in GameAPI

- 描述

    设置DECO_ENTITY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.DecoID | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_deco_entity_list_value(list, 1, 1)
```

---

## get_deco_entity_n_list

method in GameAPI

- 描述

    生成n个值为v的DECO_ENTITY数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.DecoID | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_deco_entity_n_list(1, 1)
```

---

## get_scene_preset_list_value

method in GameAPI

- 描述

    获取SCENE_PRESET数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ScenePreset | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_scene_preset_list_value(list, 1)
```

---

## set_scene_preset_list_value

method in GameAPI

- 描述

    设置SCENE_PRESET数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.ScenePreset | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_scene_preset_list_value(list, 1, 1)
```

---

## get_scene_preset_n_list

method in GameAPI

- 描述

    生成n个值为v的SCENE_PRESET数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.ScenePreset | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_scene_preset_n_list(1, 1)
```

---

## get_spine_list_value

method in GameAPI

- 描述

    获取SPINE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Spine | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_spine_list_value(list, 1)
```

---

## set_spine_list_value

method in GameAPI

- 描述

    设置SPINE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.Spine | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_spine_list_value(list, 1, 1)
```

---

## get_spine_n_list

method in GameAPI

- 描述

    生成n个值为v的SPINE数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.Spine | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_spine_n_list(1, 1)
```

---

## get_ui_anim_play_mode_list_value

method in GameAPI

- 描述

    获取UI_ANIM_PLAY_MODE数组中某项

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

local result = GameAPI.get_ui_anim_play_mode_list_value(list, 1)
```

---

## set_ui_anim_play_mode_list_value

method in GameAPI

- 描述

    设置UI_ANIM_PLAY_MODE数组中某项

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

GameAPI.set_ui_anim_play_mode_list_value(list, 1, 1)
```

---

## get_ui_anim_play_mode_n_list

method in GameAPI

- 描述

    生成n个值为v的UI_ANIM_PLAY_MODE数组

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
local result = GameAPI.get_ui_anim_play_mode_n_list(1, 1)
```

---

## get_debug_shape_list_value

method in GameAPI

- 描述

    获取DEBUG_SHAPE数组中某项

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

local result = GameAPI.get_debug_shape_list_value(list, 1)
```

---

## set_debug_shape_list_value

method in GameAPI

- 描述

    设置DEBUG_SHAPE数组中某项

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

GameAPI.set_debug_shape_list_value(list, 1, 1)
```

---

## get_debug_shape_n_list

method in GameAPI

- 描述

    生成n个值为v的DEBUG_SHAPE数组

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
local result = GameAPI.get_debug_shape_n_list(1, 1)
```

---

## get_ui_text_font_name_list_value

method in GameAPI

- 描述

    获取UI_TEXT_FONT_NAME数组中某项

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

local result = GameAPI.get_ui_text_font_name_list_value(list, 1)
```

---

## set_ui_text_font_name_list_value

method in GameAPI

- 描述

    设置UI_TEXT_FONT_NAME数组中某项

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

GameAPI.set_ui_text_font_name_list_value(list, 1, "v")
```

---

## get_ui_text_font_name_n_list

method in GameAPI

- 描述

    生成n个值为v的UI_TEXT_FONT_NAME数组

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
local result = GameAPI.get_ui_text_font_name_n_list(1, "v")
```

---

## get_ui_eca_anim_type_list_value

method in GameAPI

- 描述

    获取UI_ECA_ANIM_TYPE数组中某项

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

local result = GameAPI.get_ui_eca_anim_type_list_value(list, 1)
```

---

## set_ui_eca_anim_type_list_value

method in GameAPI

- 描述

    设置UI_ECA_ANIM_TYPE数组中某项

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

GameAPI.set_ui_eca_anim_type_list_value(list, 1, 1)
```

---

## get_ui_eca_anim_type_n_list

method in GameAPI

- 描述

    生成n个值为v的UI_ECA_ANIM_TYPE数组

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
local result = GameAPI.get_ui_eca_anim_type_n_list(1, 1)
```

---

## get_local_unit_entity_list_value

method in GameAPI

- 描述

    获取LOCAL_UNIT_ENTITY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LocalUnit | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_local_unit_entity_list_value(list, 1)
```

---

## set_local_unit_entity_list_value

method in GameAPI

- 描述

    设置LOCAL_UNIT_ENTITY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.LocalUnit | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local local_unit = GameAPI.create_local_unit(134274569, GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0)), Fix32(1))

GameAPI.set_local_unit_entity_list_value(list, 1, local_unit)
```

---

## get_local_unit_entity_n_list

method in GameAPI

- 描述

    生成n个值为v的LOCAL_UNIT_ENTITY数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.LocalUnit | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local local_unit = GameAPI.create_local_unit(134274569, GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0)), Fix32(1))

local result = GameAPI.get_local_unit_entity_n_list(1)
```

---

## get_local_unit_group_list_value

method in GameAPI

- 描述

    获取LOCAL_UNIT_GROUP数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LocalUnitGroup | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_local_unit_group_list_value(list, 1)
```

---

## set_local_unit_group_list_value

method in GameAPI

- 描述

    设置LOCAL_UNIT_GROUP数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.LocalUnitGroup | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local local_unit_group = GameAPI.get_unit_key_local_unit_group_kv(1, "key")

GameAPI.set_local_unit_group_list_value(list, 1, local_unit_group)
```

---

## get_local_unit_group_n_list

method in GameAPI

- 描述

    生成n个值为v的LOCAL_UNIT_GROUP数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.LocalUnitGroup | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local local_unit_group = GameAPI.get_unit_key_local_unit_group_kv(1, "key")

local result = GameAPI.get_local_unit_group_n_list(1)
```

---

## get_store_item_type_list_value

method in GameAPI

- 描述

    获取STORE_ITEM_TYPE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.StoreItemType | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_store_item_type_list_value(list, 1)
```

---

## set_store_item_type_list_value

method in GameAPI

- 描述

    设置STORE_ITEM_TYPE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.StoreItemType | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_store_item_type_list_value(list, 1, 1)
```

---

## get_store_item_type_n_list

method in GameAPI

- 描述

    生成n个值为v的STORE_ITEM_TYPE数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.StoreItemType | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_store_item_type_n_list(1, 1)
```

---

## get_watching_mode_status_list_value

method in GameAPI

- 描述

    获取WATCHING_MODE_STATUS数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.WatchingModeStatus | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_watching_mode_status_list_value(list, 1)
```

---

## set_watching_mode_status_list_value

method in GameAPI

- 描述

    设置WATCHING_MODE_STATUS数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.WatchingModeStatus | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_watching_mode_status_list_value(list, 1, 1)
```

---

## get_watching_mode_status_n_list

method in GameAPI

- 描述

    生成n个值为v的WATCHING_MODE_STATUS数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.WatchingModeStatus | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_watching_mode_status_n_list(1, 1)
```

---

## get_item_stack_type_list_value

method in GameAPI

- 描述

    获取ITEM_STACK_TYPE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemStackType | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_item_stack_type_list_value(list, 1)
```

---

## set_item_stack_type_list_value

method in GameAPI

- 描述

    设置ITEM_STACK_TYPE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.ItemStackType | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_item_stack_type_list_value(list, 1, 1)
```

---

## get_item_stack_type_n_list

method in GameAPI

- 描述

    生成n个值为v的ITEM_STACK_TYPE数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.ItemStackType | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_item_stack_type_n_list(1, 1)
```

---

## get_deco_name_list_value

method in GameAPI

- 描述

    获取DECO_NAME数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DecoKey | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_deco_name_list_value(list, 1)
```

---

## set_deco_name_list_value

method in GameAPI

- 描述

    设置DECO_NAME数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.DecoKey | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_deco_name_list_value(list, 1, 1)
```

---

## get_deco_name_n_list

method in GameAPI

- 描述

    生成n个值为v的DECO_NAME数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.DecoKey | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_deco_name_n_list(1, 1)
```

---

## get_ability_release_id_list_value

method in GameAPI

- 描述

    获取ABILITY_RELEASE_ID数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityReleaseId | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_ability_release_id_list_value(list, 1)
```

---

## set_ability_release_id_list_value

method in GameAPI

- 描述

    设置ABILITY_RELEASE_ID数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.AbilityReleaseId | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_ability_release_id_list_value(list, 1, 1)
```

---

## get_ability_release_id_n_list

method in GameAPI

- 描述

    生成n个值为v的ABILITY_RELEASE_ID数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.AbilityReleaseId | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_ability_release_id_n_list(1, 1)
```

---

## get_ui_point_list_value

method in GameAPI

- 描述

    获取UI_POINT数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FUIPoint | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_ui_point_list_value(list, 1)
```

---

## set_ui_point_list_value

method in GameAPI

- 描述

    设置UI_POINT数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.FUIPoint | 值 |

- 返回值

    无

- 示例

```lua
local list = {}
local fui_point = GameAPI.get_unit_key_ui_point_kv(1, "key")

GameAPI.set_ui_point_list_value(list, 1, fui_point)
```

---

## get_ui_point_n_list

method in GameAPI

- 描述

    生成n个值为v的UI_POINT数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.FUIPoint | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local fui_point = GameAPI.get_unit_key_ui_point_kv(1, "key")

local result = GameAPI.get_ui_point_n_list(1)
```

---

## get_force_entity_list_value

method in GameAPI

- 描述

    获取FORCE_ENTITY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Force | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_force_entity_list_value(list, 1)
```

---

## set_force_entity_list_value

method in GameAPI

- 描述

    设置FORCE_ENTITY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.Force | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_force_entity_list_value(list, 1, 1)
```

---

## get_force_entity_n_list

method in GameAPI

- 描述

    生成n个值为v的FORCE_ENTITY数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.Force | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_force_entity_n_list(1, 1)
```

---

## get_site_state_list_value

method in GameAPI

- 描述

    获取SITE_STATE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SITE_STATE | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_site_state_list_value(list, 1)
```

---

## set_site_state_list_value

method in GameAPI

- 描述

    设置SITE_STATE数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |
    | v | py.SITE_STATE | 值 |

- 返回值

    无

- 示例

```lua
local list = {}

GameAPI.set_site_state_list_value(list, 1, 1)
```

---

## get_site_state_n_list

method in GameAPI

- 描述

    生成n个值为v的SITE_STATE数组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n | integer | 长度 |
    | v? | py.SITE_STATE | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 列表 |

- 示例

```lua
local result = GameAPI.get_site_state_n_list(1, 1)
```

---

## get_coin_currency_list_value

method in GameAPI

- 描述

    获取COIN_CURRENCY数组中某项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |
    | i | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.COIN_CURRENCY | 值 |

- 示例

```lua
local list = {}

local result = GameAPI.get_coin_currency_list_value(list, 1)
```

---
