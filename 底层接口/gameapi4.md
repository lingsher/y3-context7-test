---
sidebarDepth: 1
---
# GameAPI (Part 4)

# 索引

Y3 编辑器 GameAPI 接口集合（第 4 部分），包含游戏核心功能。

---

| 接口 | 描述 |
| --- | --- |
| [set_player_sfx_switch](#set_player_sfx_switch) | 特效播放开关 |
| [play_sfx_on_point](#play_sfx_on_point) | 在某点播放特效 |
| [create_link_sfx_from_unit_to_point](#create_link_sfx_from_unit_to_point) | 创建单位到点闪电特效 |
| [create_link_sfx_from_unit_to_unit](#create_link_sfx_from_unit_to_unit) | 创建单位到单位闪电特效 |
| [create_link_sfx_from_point_to_unit](#create_link_sfx_from_point_to_unit) | 创建点到单位闪电特效 |
| [create_link_sfx_from_point_to_point](#create_link_sfx_from_point_to_point) | 创建点到点闪电特效 |
| [set_link_sfx_point](#set_link_sfx_point) | 设置闪电特效的位置点 |
| [set_link_sfx_unit_socket](#set_link_sfx_unit_socket) | 设置闪电特效单位附加点 |
| [remove_link_sfx](#remove_link_sfx) | 移除特效 |
| [enable_link_sfx_show](#enable_link_sfx_show) | 设置特效是否显示 |
| [enable_link_sfx_visible](#enable_link_sfx_visible) | 设置链接特效 |
| [enable_sfx_visible](#enable_sfx_visible) | 设置特效 |
| [create_sfx_on_point](#create_sfx_on_point) | 创建特效到点 |
| [create_sfx_on_unit](#create_sfx_on_unit) | 创建特效到单位附加点 |
| [create_sfx_on_unit_new](#create_sfx_on_unit_new) | 创建特效到单位附加点（跟随旋转使用枚举） |
| [delete_sfx](#delete_sfx) | 删除特效 |
| [set_sfx_rotate](#set_sfx_rotate) | 设置特效旋转 |
| [set_sfx_angle](#set_sfx_angle) | 设置特效朝向 |
| [set_sfx_color](#set_sfx_color) | 设置特效颜色 |
| [set_sfx_scale](#set_sfx_scale) | 设置特效缩放 |
| [set_sfx_height](#set_sfx_height) | 设置特效高度 |
| [set_sfx_position](#set_sfx_position) | 设置特效到点 |
| [set_sfx_animation_speed](#set_sfx_animation_speed) | 设置特效动画速度 |
| [set_sfx_duration](#set_sfx_duration) | 设置特效持续时间 |
| [add_sfx_to_camera](#add_sfx_to_camera) | 播放屏幕特效 |
| [add_sfx_to_camera_with_return](#add_sfx_to_camera_with_return) | 播放屏幕特效并返回特效实体 |
| [start_shake](#start_shake) | 震动屏幕 |
| [link_sfx_key_to_str](#link_sfx_key_to_str) | 链接特效路径转字符串 |
| [str_to_link_sfx_key](#str_to_link_sfx_key) | 字符串转链接特效路径 |
| [sfx_to_str](#sfx_to_str) | 特效转字符串 |
| [particle_sfx_key_to_str](#particle_sfx_key_to_str) | 粒子特效路径转字符串 |
| [str_to_particle_sfx_key](#str_to_particle_sfx_key) | 字符串转粒子特效路径 |
| [link_sfx_to_str](#link_sfx_to_str) | 链接特效转字符串 |
| [get_table](#get_table) | get_table |
| [set_table_value](#set_table_value) | set_table_value |
| [table_has_key](#table_has_key) | table_has_key |
| [get_table_var](#get_table_var) | get_table_var |
| [remove_table_value](#remove_table_value) | remove_table_value |
| [remove_table_value_n](#remove_table_value_n) | remove_table_value_n |
| [insert_table_value](#insert_table_value) | insert_table_value |
| [get_new_table](#get_new_table) | get_new_table |
| [clear_table](#clear_table) | clear_table |
| [encrypt_table](#encrypt_table) | encrypt_table |
| [get_copy_of_table](#get_copy_of_table) | get_copy_of_table |
| [dump_table](#dump_table) | dump_table |
| [get_table_length](#get_table_length) | get_table_length |
| [is_table_empty](#is_table_empty) | 表 - 是否为空表 |
| [get_iter_table_value](#get_iter_table_value) | get_iter_table_value_by_type |
| [table_iterator](#table_iterator) | table迭代器 |
| [ordered_table_iterator](#ordered_table_iterator) | table迭代器（保序） |
| [table_iterator_new](#table_iterator_new) | table迭代器 |
| [unserialize_by_string](#unserialize_by_string) | unserialize_by_string |
| [sort_table_by](#sort_table_by) | sort_table_by |
| [dbg_dialog_print_frame_timer_info](#dbg_dialog_print_frame_timer_info) | 调试-Dialog窗口输出帧计时器信息 |
| [get_last_created_timer](#get_last_created_timer) | 获取最近创建的计时器 |
| [start_timer](#start_timer) | 开启计时器 |
| [stop_timer](#stop_timer) | 关闭计时器 |
| [run_lua_timer](#run_lua_timer) | 开启计时器（新） |
| [is_timer_valid](#is_timer_valid) | 计时器是否正在运行 |
| [delete_timer](#delete_timer) | 删除计时器 |
| [pause_timer](#pause_timer) | 暂停计时器 |
| [resume_timer](#resume_timer) | 恢复计时器 |
| [timer_set_left_count](#timer_set_left_count) | 设置计时器剩余次数 |
| [timer_set_left_time](#timer_set_left_time) | 设置计时器剩余时间 |
| [timer_set_interval_time](#timer_set_interval_time) | 设置计时器间隔时间 |
| [timer_set_interval_frame](#timer_set_interval_frame) | 设置帧计时器间隔帧数 |
| [get_timer_time_out_time](#get_timer_time_out_time) | 获取计时器设置的时间 |
| [get_timer_elapsed_time](#get_timer_elapsed_time) | 获取计时器经过的时间 |
| [get_timer_remaining_time](#get_timer_remaining_time) | 获取计时器剩余时间 |
| [get_timer_init_count](#get_timer_init_count) | 获取计时器初始计数 |
| [get_timer_remaining_count](#get_timer_remaining_count) | 获取计时器剩余计数 |
| [get_actor_timer_run_time](#get_actor_timer_run_time) | 获取独立计时器当前计时秒数 |
| [get_current_expired_timer](#get_current_expired_timer) | 获取当前到期的计时器 |
| [timer_is_exist](#timer_is_exist) | 计时器是否存在 |
| [add_timer](#add_timer) | 添加定时回调 |
| [cancel_timer](#cancel_timer) | 取消定时回调 |
| [get_cur_day_and_night_time](#get_cur_day_and_night_time) | 游戏当前昼夜时间 |
| [set_day_and_night_time](#set_day_and_night_time) | 设置昼夜游戏时间 |
| [set_day_and_night_time_speed](#set_day_and_night_time_speed) | 设置昼夜游戏时间的流逝速度（倍数） |
| [set_day_and_night_time_speed_per](#set_day_and_night_time_speed_per) | 设置昼夜游戏时间的流逝速度（百分比） |
| [open_or_close_time_speed](#open_or_close_time_speed) | 打开/关闭时间流逝 |
| [create_day_and_night_human_time](#create_day_and_night_human_time) | 创建人造时间，并持续一段时间 |
| [get_points_angle](#get_points_angle) | 点与点的角度 |
| [get_points_dis](#get_points_dis) | 点与点的距离 |
| [get_point_ground_height](#get_point_ground_height) | 获取当前点的地面高度 |
| [get_point_ground_collision](#get_point_ground_collision) | 获取当前点的碰撞类型 |
| [get_point_view_block_type](#get_point_view_block_type) | 获取当前点的视野隔断类型 |
| [judge_point_in_area](#judge_point_in_area) | 判断点是否在区域内 |
| [judge_point_in_rec](#judge_point_in_rec) | 判断点是否在正方形内 |
| [add_area_tag](#add_area_tag) | 给区域添加tag |
| [remove_area_tag](#remove_area_tag) | 给区域移除tag |
| [add_road_tag](#add_road_tag) | 给路径添加tag |
| [remove_road_tag](#remove_road_tag) | 给路径移除tag |
| [if_cir_area_has_tag](#if_cir_area_has_tag) | 圆形区域是否拥有某tags |
| [if_rect_area_has_tag](#if_rect_area_has_tag) | 矩形区域是否拥有某tags |
| [if_road_has_tag](#if_road_has_tag) | 路径是否拥有某tags |
| [get_cir_areas_by_tag](#get_cir_areas_by_tag) | 根据tag获取对应的圆形区域 |
| [get_rect_areas_by_tag](#get_rect_areas_by_tag) | 根据tag获取对应的矩形区域 |
| [get_polygon_areas_by_tag](#get_polygon_areas_by_tag) | 根据tag获取对应的不规则区域 |
| [get_roads_by_tag](#get_roads_by_tag) | 根据tag获取对应的路径 |
| [get_poly_area_point_list](#get_poly_area_point_list) | 获取不规则区域顶点列表 |
| [get_point_by_road_point](#get_point_by_road_point) | 通过路点返回点 |
| [create_new_rec_area](#create_new_rec_area) | 创建矩形区域 |
| [create_rect_area_by_center](#create_rect_area_by_center) | 创建矩形区域 |
| [create_rec_area_from_two_points](#create_rec_area_from_two_points) | 创建矩形区域 |
| [create_new_cir_area](#create_new_cir_area) | 创建圆形区域 |
| [create_polygon_area](#create_polygon_area) | 创建多边形区域 |
| [create_polygon_area_new](#create_polygon_area_new) | 创建多边形区域(新) |
| [set_cir_area_radius](#set_cir_area_radius) | 设置圆形区域大小 |
| [get_circle_area_radius](#get_circle_area_radius) | 获取圆形区域半径 |
| [get_circle_area_min_x](#get_circle_area_min_x) | 获取圆形区域内最小X坐标 |
| [get_circle_area_min_y](#get_circle_area_min_y) | 获取圆形区域内最小y坐标 |
| [get_circle_area_max_x](#get_circle_area_max_x) | 获取圆形区域内最大X坐标 |
| [get_circle_area_max_y](#get_circle_area_max_y) | 获取圆形区域内最大y坐标 |
| [set_rect_area_radius](#set_rect_area_radius) | 设置矩形区域大小 |
| [get_rect_area_min_x](#get_rect_area_min_x) | 获取矩形区域内最小X坐标 |
| [get_rect_area_min_y](#get_rect_area_min_y) | 获取矩形区域内最小Y坐标 |
| [get_rect_area_max_x](#get_rect_area_max_x) | 获取矩形区域内最大X坐标 |
| [get_rect_area_max_y](#get_rect_area_max_y) | 获取矩形区域内最大Y坐标 |
| [get_usable_map_range](#get_usable_map_range) | 获取可用地图范围 |
| [get_rec_area_by_res_id](#get_rec_area_by_res_id) | 通过区域ID返回矩形区域 |
| [get_circle_area_by_res_id](#get_circle_area_by_res_id) | 通过区域ID返回圆形区域 |
| [get_polygon_area_by_res_id](#get_polygon_area_by_res_id) | 通过区域ID返回自定义多边形区域 |
| [get_rec_area_last_created](#get_rec_area_last_created) | 最近创建的矩形区域 |
| [judge_point_in_rec_area](#judge_point_in_rec_area) | 点是否在矩形区域内 |
| [judge_point_in_cir_area](#judge_point_in_cir_area) | 点是否在圆形区域内 |
| [judge_point_in_polygon_area](#judge_point_in_polygon_area) | 点是否在不规则区域内 |
| [get_point_by_res_id](#get_point_by_res_id) | 通过资源id返回点 |
| [get_unit_num_in_area](#get_unit_num_in_area) | 获取区域内单位数量 |
| [get_unit_num_in_rec_area](#get_unit_num_in_rec_area) | 矩形区域内单位数量 |
| [get_unit_num_in_cir_area](#get_unit_num_in_cir_area) | 圆形区域内单位数量 |
| [get_unit_num_in_poly_area](#get_unit_num_in_poly_area) | 不规则区域内单位数量 |
| [get_unit_group_in_rec_area](#get_unit_group_in_rec_area) | 矩形区域内所有未销毁单位单位 |
| [get_unit_group_in_cir_area](#get_unit_group_in_cir_area) | 圆形区域内所有未销毁单位 |
| [get_unit_group_in_poly_area](#get_unit_group_in_poly_area) | 不规则区域内所有未销毁单位 |
| [get_item_group_in_rec_area](#get_item_group_in_rec_area) | 矩形区域内所有物品 |
| [get_item_group_in_cir_area](#get_item_group_in_cir_area) | 圆形区域内所有物品 |
| [get_item_group_in_poly_area](#get_item_group_in_poly_area) | 不规则区域内所有物品 |
| [remove_area](#remove_area) | 删除区域 |
| [get_area_weather](#get_area_weather) | 获得区域天气 |
| [update_area_weather](#update_area_weather) | 设置区域天气 |
| [set_point_collision](#set_point_collision) | 设置点碰撞 |
| [set_area_collision](#set_area_collision) | 设置区域碰撞 |
| [edit_area_collision](#edit_area_collision) | 编辑区域碰撞 |
| [edit_area_fov_block](#edit_area_fov_block) | 编辑区域视野阻挡 |
| [get_area_resource_id](#get_area_resource_id) | 获取区域的场景ID |
| [get_road_resource_id](#get_road_resource_id) | 获取路径的场景ID |
| [sound_entity_to_str](#sound_entity_to_str) | 声音转字符串 |
| [audio_key_to_str](#audio_key_to_str) | 声音类型转字符串 |
| [str_to_audio_key](#str_to_audio_key) | 字符串转声音类型 |
| [reg_sound_area](#reg_sound_area) | 注册区域的附近语音频道 |
| [unreg_sound_area](#unreg_sound_area) | 反注册区域的附近语音频道 |
| [set_nearby_voice_mode](#set_nearby_voice_mode) | 设置附近语音的区域模式开关 |
| [set_audio_chat_channel](#set_audio_chat_channel) | 设置玩家发言频道 |
| [play_sound_for_player](#play_sound_for_player) | 播放音乐 |
| [play_sound_for_role_relation](#play_sound_for_role_relation) | 对目标播放音乐 |
| [play_3d_sound_for_player](#play_3d_sound_for_player) | 播放3d音乐 |
| [follow_object_play_3d_sound_for_player](#follow_object_play_3d_sound_for_player) | 跟随单位播放3d音乐 |
| [stop_sound](#stop_sound) | 停止播放音乐 |
| [sound_play_controller](#sound_play_controller) | 播放控制 |
| [set_player_listener_to_follow_intersection_of_camera_ray_and_ground](#set_player_listener_to_follow_intersection_of_camera_ray_and_ground) | 设置玩家的声音接收器跟随镜头射线与地面焦点 |
| [set_player_listener_to_follow_unit](#set_player_listener_to_follow_unit) | 设置玩家的声音接收器跟随单位 |
| [open_background_music](#open_background_music) | 设置背景音乐开关 |
| [open_battle_music](#open_battle_music) | 设置战斗音乐开关 |
| [set_background_music_volume](#set_background_music_volume) | 设置背景音乐音量 |
| [set_battle_music_volume](#set_battle_music_volume) | 设置战斗音效音量 |
| [set_sound_volume](#set_sound_volume) | 设置声音音量 |
| [get_scene_sound_by_res_id](#get_scene_sound_by_res_id) | 通过场景声音ID返回场景声音 |
| [play_scene_sound](#play_scene_sound) | 播放场景声音 |
| [stop_scene_sound](#stop_scene_sound) | 停止场景声音 |
| [set_scene_sound_loop](#set_scene_sound_loop) | 设置场景声音是否循环 |
| [set_scene_sound_min_dist](#set_scene_sound_min_dist) | 设置场景声音衰减距离 |
| [set_scene_sound_max_dist](#set_scene_sound_max_dist) | 设置场景声音静音距离 |
| [set_scene_sound_pause](#set_scene_sound_pause) | 设置场景声音是否暂停 |
| [get_bgm_state](#get_bgm_state) | 获取初始化背景音乐开关状态 |
| [get_battle_bgm_state](#get_battle_bgm_state) | 获取初始化战斗音效开关状态 |
| [get_bgm_volume](#get_bgm_volume) | 获取初始化背景音乐音量 |
| [get_battle_volume](#get_battle_volume) | 获取初始化战斗音效音量 |
| [get_game_mode](#get_game_mode) | 获取当前游戏模式 |
| [pause_game](#pause_game) | 暂停游戏 |
| [set_melee_result_by_role](#set_melee_result_by_role) | 为玩家结束游戏 |
| [set_melee_result_by_role_2](#set_melee_result_by_role_2) | 结束玩家游戏 |
| [upload_role_billboard_score](#upload_role_billboard_score) | 上传玩家排行榜分数 |
| [game_end](#game_end) | 结束游戏 |
| [request_new_round](#request_new_round) | 申请开始下一轮 |
| [request_switch_level](#request_switch_level) | 切换至关卡 |
| [get_global_map_archive](#get_global_map_archive) | 获取当前地图的指定key的存档值 |
| [get_rank_player_nickname](#get_rank_player_nickname) | 获取地图全局指定key存档的第n名玩家的昵称 |
| [get_rank_player_global_archive_value](#get_rank_player_global_archive_value) | 获取地图全局指定key存档的第n名玩家的存档值 |
| [get_archive_rank_player_nickname](#get_archive_rank_player_nickname) | 获取玩家指定的个人存档栏位的第n名玩家的昵称 |
| [get_archive_rank_player_archive_value](#get_archive_rank_player_archive_value) | 获取玩家指定的个人存档栏位的第n名玩家的存档值 |
| [api_change_logic_fps](#api_change_logic_fps) | 调整逻辑帧率 |
| [api_soft_pause_game](#api_soft_pause_game) | 开启软暂停 |
| [api_soft_resume_game](#api_soft_resume_game) | 关闭软暂停 |
| [get_owner_role_id](#get_owner_role_id) | 本地玩家编号 |
| [get_local_player_pointing_pos](#get_local_player_pointing_pos) | 本地玩家鼠标位置 |
| [get_local_player_ui_pos_x](#get_local_player_ui_pos_x) | 本地玩家鼠标屏幕位置X |
| [get_local_player_ui_pos_y](#get_local_player_ui_pos_y) | 本地玩家鼠标屏幕位置Y |
| [get_local_role_ui_x_per](#get_local_role_ui_x_per) | 本地玩家鼠标屏幕位置X的窗口占比 |
| [get_local_role_ui_y_per](#get_local_role_ui_y_per) | 本地玩家鼠标屏幕位置y的窗口占比 |
| [get_local_player_camera_direction](#get_local_player_camera_direction) | 本地玩家摄像机朝向 |
| [get_local_player_camera_center_raycast](#get_local_player_camera_center_raycast) | 本地玩家摄像机中心射线检测 |
| [get_game_init_time_stamp](#get_game_init_time_stamp) | 获取游戏开始时间戳 |
| [get_local_time_stamp](#get_local_time_stamp) | 获取本地时间戳 |
| [add_local_timer](#add_local_timer) | 添加本地计时器 |
| [add_local_repeat_timer](#add_local_repeat_timer) | 添加本地循环计时器 |
| [cancel_local_timer](#cancel_local_timer) | 取消本地计时器 |
| [force_enable_mouse_sync](#force_enable_mouse_sync) | 强制开启/关闭鼠标同步 |
| [force_enable_keyboard_sync](#force_enable_keyboard_sync) | 强制开启/关闭按键同步 |
| [force_enable_camera_sync](#force_enable_camera_sync) | 强制开启/关闭镜头同步 |
| [init_bind_nim](#init_bind_nim) | 启动云信并绑定对象 |
| [api_set_v_sync](#api_set_v_sync) | 启用/禁用垂直同步 |
| [api_set_local_mapping_key](#api_set_local_mapping_key) | 设置本地改键 |
| [api_cancel_local_mapping_key](#api_cancel_local_mapping_key) | 取消本地改键 |
| [api_clear_local_mapping_key](#api_clear_local_mapping_key) | 清空本地改键 |
| [api_set_builtin_key_control_enable](#api_set_builtin_key_control_enable) | 设置是否使用内置本地改键方案 |
| [api_is_builtin_key_control_enable](#api_is_builtin_key_control_enable) | 判断是否使用内置键盘控制 |
| [api_set_role_camera_mode](#api_set_role_camera_mode) | 设置玩家镜头模式 |
| [is_cameraIS_playing_timeline](#is_cameraIS_playing_timeline) | 玩家镜头是否正在播放动画 |
| [play_camera_timeline](#play_camera_timeline) | 播放镜头动画 |
| [stop_camera_timeline](#stop_camera_timeline) | 停止播放镜头动画 |
| [api_set_obj_fresnel_visible](#api_set_obj_fresnel_visible) | 设置对象的菲涅尔效果开关 |
| [api_set_obj_fresnel_parameters](#api_set_obj_fresnel_parameters) | 设置对象的菲涅尔效果 |
| [set_focus_distance](#set_focus_distance) | 设置模型加载范围 |
| [set_image_quality](#set_image_quality) | 设置画质 |
| [get_graphics_quality](#get_graphics_quality) | 获取初始化游戏画质 |
| [set_post_effect](#set_post_effect) | 设置画风 |
| [set_cascaded_shadow_enable](#set_cascaded_shadow_enable) | 级联阴影开关 |
| [set_dynamic_shadow_cascades](#set_dynamic_shadow_cascades) | 级联阴影层数 |
| [set_dynamic_shadow_distance_movable_light](#set_dynamic_shadow_distance_movable_light) | 级联阴影距离 |
| [set_cascaded_shadow_distance](#set_cascaded_shadow_distance) | 阴影距离 |
| [get_cascaded_shadow_enable](#get_cascaded_shadow_enable) | 获取级联阴影状态 |
| [get_dynamic_shadow_cascades](#get_dynamic_shadow_cascades) | 获取级联阴影层数 |
| [get_dynamic_shadow_distance_movable_light](#get_dynamic_shadow_distance_movable_light) | 获取级联阴影距离 |
| [get_cascaded_shadow_distance](#get_cascaded_shadow_distance) | 获取阴影距离 |
| [get_light_float_attr_value](#get_light_float_attr_value) | 获取光源Float属性 |
| [set_light_cast_shadow_attr_value](#set_light_cast_shadow_attr_value) | 设置光源是否产生阴影 |
| [get_light_cast_shadow_attr_value](#get_light_cast_shadow_attr_value) | 获取光源是否产生阴影 |
| [get_fog_res_by_res_id](#get_fog_res_by_res_id) | 根据局部雾ID返回局部雾 |
| [set_fog_attr](#set_fog_attr) | 修改雾效属性 |
| [set_fog_attr_new](#set_fog_attr_new) | 修改雾效属性新 |
| [enable_fow_for_player](#enable_fow_for_player) | 为玩家开关全局视野 |
| [change_mini_map_img](#change_mini_map_img) | 设置小地图替代图片 |
| [change_mini_map_img_with_icon](#change_mini_map_img_with_icon) | 设置小地图替代图片(图片类型) |
| [change_mini_map_color_type](#change_mini_map_color_type) | 设置小地图颜色显示模式 |
| [enable_unit_path_drawing](#enable_unit_path_drawing) | 开启绘制单位路径线 |
| [disable_unit_path_drawing](#disable_unit_path_drawing) | 关闭绘制单位路径线 |
| [set_min_map_show_area](#set_min_map_show_area) | 设置小地图显示区域 |
| [set_local_player_jump_word_close](#set_local_player_jump_word_close) | 关闭localplayer的表现层跳字 |
| [api_change_obj_base_color](#api_change_obj_base_color) | 设置对象的基础材质属性 |
| [set_camera_floating_with_terrain](#set_camera_floating_with_terrain) | 设置镜头是否跟随地形高度浮动 |
| [modify_point_texture](#modify_point_texture) | 修改某点的地形纹理 |
| [modify_point_height](#modify_point_height) | 修改某点的地形高度 |
| [replace_point_texture](#replace_point_texture) | 替换区域中的指定地形纹理 |
| [get_texture_type](#get_texture_type) | 获取纹理类型 |
| [set_local_terrain_visible](#set_local_terrain_visible) | 修改玩家的地表纹理 |
| [set_material_param](#set_material_param) | 修改材质属性 |
| [set_role_color_grading](#set_role_color_grading) | 为玩家设置滤镜效果 |
| [set_screen_resolution](#set_screen_resolution) | 设置分辨率 |
| [set_window_type](#set_window_type) | 设置窗口 |
| [set_grass_enable_by_pos](#set_grass_enable_by_pos) | 开关目标点的草丛 |
| [get_window_mode](#get_window_mode) | 获取初始化窗口类别 |
| [get_game_x_resolution](#get_game_x_resolution) | 获取初始化横向分辨率 |
| [get_game_y_resolution](#get_game_y_resolution) | 获取初始化纵向分辨率 |
| [get_window_real_x_size](#get_window_real_x_size) | 当前窗体横向尺寸 |
| [get_window_real_y_size](#get_window_real_y_size) | 当前窗体纵向尺寸 |
| [get_screen_x_resolution](#get_screen_x_resolution) | 获取屏幕横向分辨率 |
| [get_screen_y_resolution](#get_screen_y_resolution) | 获取屏幕纵向分辨率 |
| [check_unit_key_precondition](#check_unit_key_precondition) | 判断玩家单位类型前置条件满足需求 |
| [check_item_key_precondition](#check_item_key_precondition) | 判断玩家物品类型前置条件满足需求 |
| [check_tech_key_precondition](#check_tech_key_precondition) | 判断玩家科技类型前置条件满足需求 |
| [check_ability_key_precondition](#check_ability_key_precondition) | 判断玩家技能类型前置条件满足需求 |
| [get_ability_key_precondition_list](#get_ability_key_precondition_list) | 获取技能类型的前置条件列表 |
| [get_unit_key_precondition_list](#get_unit_key_precondition_list) | 获取单位类型的前置条件列表 |
| [get_item_key_precondition_list](#get_item_key_precondition_list) | 获取物品类型的前置条件列表 |
| [get_pre_condition_iter_unit_key](#get_pre_condition_iter_unit_key) | 获取前置条件遍历到的单位类型 |
| [get_pre_condition_iter_tech_key](#get_pre_condition_iter_tech_key) | 获取前置条件遍历到的科技类型 |
| [get_pre_condition_iter_unit_tag](#get_pre_condition_iter_unit_tag) | 获取前置条件遍历到的单位标签 |
| [get_pre_condition_iter_tech_tag](#get_pre_condition_iter_tech_tag) | 获取前置条件遍历到的科技标签 |
| [get_unit_type_unit_key_pre_condition_require_count](#get_unit_type_unit_key_pre_condition_require_count) | 获取单位单位类型前置条件的需求值 |
| [get_unit_type_unit_tag_pre_condition_require_count](#get_unit_type_unit_tag_pre_condition_require_count) | 获取单位单位标签前置条件的需求值 |
| [get_unit_type_tech_key_pre_condition_require_count](#get_unit_type_tech_key_pre_condition_require_count) | 获取单位科技类型前置条件的需求值 |
| [get_unit_type_tech_tag_pre_condition_require_count](#get_unit_type_tech_tag_pre_condition_require_count) | 获取单位科技标签前置条件的需求值 |
| [get_ability_type_unit_key_pre_condition_require_count](#get_ability_type_unit_key_pre_condition_require_count) | 获取技能单位类型前置条件的需求值 |
| [get_ability_type_unit_tag_pre_condition_require_count](#get_ability_type_unit_tag_pre_condition_require_count) | 获取技能单位标签前置条件的需求值 |
| [get_ability_type_tech_key_pre_condition_require_count](#get_ability_type_tech_key_pre_condition_require_count) | 获取技能科技类型前置条件的需求值 |
| [get_ability_type_tech_tag_pre_condition_require_count](#get_ability_type_tech_tag_pre_condition_require_count) | 获取技能科技标签前置条件的需求值 |
| [get_item_type_unit_key_pre_condition_require_count](#get_item_type_unit_key_pre_condition_require_count) | 获取物品单位类型前置条件的需求值 |
| [get_item_type_unit_tag_pre_condition_require_count](#get_item_type_unit_tag_pre_condition_require_count) | 获取物品单位标签前置条件的需求值 |
| [get_item_type_tech_key_pre_condition_require_count](#get_item_type_tech_key_pre_condition_require_count) | 获取物品科技类型前置条件的需求值 |
| [get_item_type_tech_tag_pre_condition_require_count](#get_item_type_tech_tag_pre_condition_require_count) | 获取物品科技标签前置条件的需求值 |
| [set_ui_comp_adapt_option](#set_ui_comp_adapt_option) | 设置控件适配 |
| [trigger_ui_event](#trigger_ui_event) | 使玩家触发界面事件 |
| [set_ui_comp_follow_mouse](#set_ui_comp_follow_mouse) | 控制控件跟随鼠标 |
| [pos_in_comp_box](#pos_in_comp_box) | 【异步】获得坐标是否在控件内 |
| [set_model_comp_camera_mod](#set_model_comp_camera_mod) | 设置模型控件的镜头模式 |
| [set_ui_btn_status_string](#set_ui_btn_status_string) | 设置不同状态下的按钮文本 |
| [set_ui_btn_status_image](#set_ui_btn_status_image) | 设置不同状态下的按钮图片 |
| [set_ui_scrollview_type](#set_ui_scrollview_type) | 设置列表控件的布局方式 |
| [set_ui_scrollview_size_change_according_children](#set_ui_scrollview_size_change_according_children) | 设置列表控件的尺寸是否跟随子控件变化 |
| [set_ui_image_color](#set_ui_image_color) | 设置图片颜色 |
| [get_role_ui_comp_real_width](#get_role_ui_comp_real_width) | 【异步】界面-获取控件的真实宽度 |
| [get_role_ui_comp_real_height](#get_role_ui_comp_real_height) | 【异步】界面-获取控件的真实高度 |
| [get_role_real_mouse_x](#get_role_real_mouse_x) | 【异步】界面-获取玩家鼠标真实x坐标 |
| [get_role_real_mouse_y](#get_role_real_mouse_y) | 【异步】界面-获取玩家鼠标真实y坐标 |
| [set_cur_chatbox](#set_cur_chatbox) | 设置当前聊天框控件 |
| [ui_comp_is_exist](#ui_comp_is_exist) | 界面组件是否存在 |
| [show_ui_comp_animation](#show_ui_comp_animation) | 显示ui组件并播放动画 |
| [hide_ui_comp_animation](#hide_ui_comp_animation) | 隐藏ui组件并播放动画 |
| [set_ui_comp_pos](#set_ui_comp_pos) | 设置ui组件坐标 |
| [set_ui_comp_pos_no_trans](#set_ui_comp_pos_no_trans) | 设置ui组件坐标没有转化 |
| [set_ui_comp_scale](#set_ui_comp_scale) | 设置ui组件缩放 |
| [set_ui_comp_size](#set_ui_comp_size) | 设置ui组件尺寸 |
| [set_ui_comp_z_order](#set_ui_comp_z_order) | 设置ui组件深度 |
| [set_ui_comp_image](#set_ui_comp_image) | 设置ui组件图片 |
| [set_ui_comp_margin](#set_ui_comp_margin) | 设置ui列表组件间距 |
| [set_ui_comp_image_with_icon](#set_ui_comp_image_with_icon) | 设置ui组件图片(图片类型) |
| [set_ui_comp_sequence](#set_ui_comp_sequence) | 设置ui组件序列帧 |
| [play_ui_comp_sequence](#play_ui_comp_sequence) | 播放序列帧 |
| [stop_ui_comp_sequence](#stop_ui_comp_sequence) | 停止播放序列帧 |
| [set_progress_bar_max_value](#set_progress_bar_max_value) | 设置进度条最大值 |
| [set_progress_bar_current_value](#set_progress_bar_current_value) | 设置进度条当前值 |
| [set_ui_comp_enable](#set_ui_comp_enable) | 设置ui开启/关闭 |
| [set_ui_comp_visible](#set_ui_comp_visible) | 设置ui显示/隐藏 |
| [set_ui_comp_font_color](#set_ui_comp_font_color) | 设置ui文本颜色 |
| [set_ui_comp_text](#set_ui_comp_text) | 设置ui文本 |
| [set_ui_comp_font_size](#set_ui_comp_font_size) | 设置ui文本大小 |
| [set_input_field_focus](#set_input_field_focus) | 设置输入框获得焦点 |
| [set_input_field_not_focus](#set_input_field_not_focus) | 设置输入框失去焦点 |
| [play_ui_comp_anim](#play_ui_comp_anim) | 播放UI控件时间轴动画 |
| [stop_ui_comp_anim](#stop_ui_comp_anim) | 停止UI控件时间轴动画 |
| [set_skill_on_ui_comp](#set_skill_on_ui_comp) | 绑定技能实体到控件 |
| [unbind_skill_on_ui_comp](#unbind_skill_on_ui_comp) | 解绑技能实体到控件 |
| [set_ui_comp_opacity](#set_ui_comp_opacity) | 设置控件透明度 |
| [set_buff_on_ui_comp](#set_buff_on_ui_comp) | 绑定对象到BUFF控件 |
| [set_item_on_ui_comp](#set_item_on_ui_comp) | 绑定物品实体到道具栏控件 |
| [set_ui_comp_slot](#set_ui_comp_slot) | 设置道具栏控件类型和槽位号 |
| [set_ui_comp_unit_slot](#set_ui_comp_unit_slot) | 设置道具栏控件类型和槽位号 |
| [set_prefab_ui_visible](#set_prefab_ui_visible) | 设置预设主界面UI显隐 |
| [set_skill_btn_action_effect](#set_skill_btn_action_effect) | 播放/停止技能按钮激活动效 |
| [set_btn_short_cut](#set_btn_short_cut) | 设置按钮快捷键 |
| [set_btn_func_short_cut](#set_btn_func_short_cut) | 设置按钮辅助键 |
| [set_skill_btn_smart_cast_key](#set_skill_btn_smart_cast_key) | 设置技能按钮智能施法快捷键 |
| [set_skill_btn_func_smart_cast_key](#set_skill_btn_func_smart_cast_key) | 设置技能按钮智能施法辅助键 |
| [set_ui_model_id](#set_ui_model_id) | 设置UI模型控件ID |
| [set_shop_comp_bind_shop_unit](#set_shop_comp_bind_shop_unit) | 设置玩家的商店控件的目标商店单位 |
| [set_compose_comp_refresh](#set_compose_comp_refresh) | 设置玩家的合成控件的参数并刷新 |
| [set_show_room_background_color](#set_show_room_background_color) | 设置ui模型控件背景色 |
| [change_showroom_fov](#change_showroom_fov) | 设置Showroom的fov |
| [change_showroom_cposition](#change_showroom_cposition) | 设置Showroom的camera pos |
| [change_showroom_crotation](#change_showroom_crotation) | 设置Showroom的camera rotation |
| [set_ui_comp_rotation](#set_ui_comp_rotation) | 设置控件旋转 |
| [set_ui_comp_swallow](#set_ui_comp_swallow) | 设置控件是否拦截 |
| [set_ui_comp_drag](#set_ui_comp_drag) | 设置控件是否可拖动 |
| [set_ui_comp_world_pos](#set_ui_comp_world_pos) | 设置控件世界坐标 |
| [set_ui_comp_world_rotation](#set_ui_comp_world_rotation) | 设置控件世界旋转 |
| [set_ui_comp_world_scale](#set_ui_comp_world_scale) | 设置控件世界缩放 |
| [get_ui_comp_pos_x](#get_ui_comp_pos_x) | 【异步】获取当前玩家控件相对位置x |
| [get_ui_comp_pos_y](#get_ui_comp_pos_y) | 【异步】获取当前玩家控件相对位置y |
| [get_ui_comp_world_pos_x](#get_ui_comp_world_pos_x) | 【异步】获取当前玩家控件绝对位置x |
| [get_ui_comp_world_pos_y](#get_ui_comp_world_pos_y) | 【异步】获取当前玩家控件绝对位置y |
| [get_ui_comp_rotation](#get_ui_comp_rotation) | 【异步】获取当前玩家控件相对旋转 |
| [get_ui_comp_world_rotation](#get_ui_comp_world_rotation) | 【异步】获取当前玩家控件绝对旋转 |
| [get_ui_comp_scale_x](#get_ui_comp_scale_x) | 【异步】获取当前玩家控件相对缩放x |
| [get_ui_comp_scale_y](#get_ui_comp_scale_y) | 【异步】获取当前玩家控件相对缩放y |
| [get_ui_comp_world_scale_x](#get_ui_comp_world_scale_x) | 【异步】获取当前玩家控件绝对缩放x |
| [get_ui_comp_world_scale_y](#get_ui_comp_world_scale_y) | 【异步】获取当前玩家控件绝对缩放y |
| [create_ui_comp](#create_ui_comp) | 创建ui控件 |
| [get_ui_comp_id_by_name](#get_ui_comp_id_by_name) | 查找指定名字的UI控件 |
| [create_ui_comp_event](#create_ui_comp_event) | 创建并绑定ui控件事件 |
| [create_ui_comp_event_ex](#create_ui_comp_event_ex) | 创建并绑定ui控件事件(指定事件名) |
| [create_ui_comp_event_ex_ex](#create_ui_comp_event_ex_ex) | 新版创建并绑定ui控件事件(指定事件名),不再传入玩家，同时支持普通控件和动态创建控件 |
| [create_ui_comp_event_ex_no_check](#create_ui_comp_event_ex_no_check) | 创建并绑定ui控件事件(指定事件名) |
| [get_ui_comp_in_scene_ui](#get_ui_comp_in_scene_ui) | 获取场景ui中的控件 |
| [get_ui_comp_in_scene_ui_ex](#get_ui_comp_in_scene_ui_ex) | 获取场景ui中的控件 |
| [get_comp_by_path](#get_comp_by_path) | 通过控件+路径获得ui控件 |
| [get_comp_by_absolute_path](#get_comp_by_absolute_path) | 通过绝对路径获得ui控件 |
| [play_ui_comp_fx](#play_ui_comp_fx) | 播放ui动效 |
| [play_ui_model_anim](#play_ui_model_anim) | ui模型控件播放动画 |
| [set_ui_comp_suspend_image](#set_ui_comp_suspend_image) | 设置ui组件悬浮态图片 |
| [set_ui_comp_press_image](#set_ui_comp_press_image) | 设置ui组件按下态图片 |
| [set_ui_comp_disabled_image](#set_ui_comp_disabled_image) | 设置ui组件禁用态图片 |
| [clear_combo_box](#clear_combo_box) | 清空下拉框 |
| [add_combo_item](#add_combo_item) | 添加下拉框选项 |
| [set_combo_text](#set_combo_text) | 设置下拉框默认文本 |
| [get_combo_box_cur_value](#get_combo_box_cur_value) | 【异步】获取下拉框当前值 |
| [get_slider_cur_percent](#get_slider_cur_percent) | 【异步】获取滑动条当前值 |
| [set_slider_cur_percent](#set_slider_cur_percent) | 设置滑动条当前值 |
| [get_ui_comp_width](#get_ui_comp_width) | 【异步】获得控件宽度 |
| [get_ui_comp_height](#get_ui_comp_height) | 【异步】获得控件高度 |
| [set_ui_comp_bar_status](#set_ui_comp_bar_status) | 设置ui按钮是否开启多态 |
| [set_ui_model_focus_pos](#set_ui_model_focus_pos) | 设置UI控件模型焦点 |
| [get_ui_comp_children](#get_ui_comp_children) | 获取ui控件的子控件 |
| [get_ui_comp_children_no_check](#get_ui_comp_children_no_check) | 获取ui控件的子控件 |
| [get_ui_comp_name](#get_ui_comp_name) | 获取ui控件的名称 |
| [unbind_ui_comp](#unbind_ui_comp) | 解绑绑定控件 |
| [set_ui_comp_bind_attr](#set_ui_comp_bind_attr) | 绑定单位属性或者全局变量到玩家界面控件的属性 |
| [set_ui_comp_bind_var](#set_ui_comp_bind_var) | 绑定单位属性或者全局变量到玩家界面控件的属性 |
| [ui_comp_unbind](#ui_comp_unbind) | 解绑界面控件属性绑定 |
| [ui_comp_bind_unit](#ui_comp_bind_unit) | 界面控件属性绑定指定单位 |
| [ui_comp_bind_ctrl_unit](#ui_comp_bind_ctrl_unit) | 界面控件属性动态绑定主控单位 |
| [get_ui_comp_parent](#get_ui_comp_parent) | 获取界面控件的父控件 |
| [set_ui_comp_bind_player_prop](#set_ui_comp_bind_player_prop) | 绑定玩家属性到玩家界面控件的属性 |
| [set_ui_comp_align](#set_ui_comp_align) | 设置控件文本对齐方式 |
| [register_ui_comp_fx_cb](#register_ui_comp_fx_cb) | 注册界面控件播放指定动效回调 |
| [create_ui_prefab_instance](#create_ui_prefab_instance) | 创建界面模块 |
| [del_ui_comp](#del_ui_comp) | 删除界面控件 |
| [set_ui_comp_text_adaptive](#set_ui_comp_text_adaptive) | 开启字体大小跟随内容自适应 |
| [set_ui_comp_bind_ability_cd](#set_ui_comp_bind_ability_cd) | 绑定技能cd到玩家界面控件的属性 |
| [set_ui_comp_bind_modifier_cd](#set_ui_comp_bind_modifier_cd) | 绑定魔法效果cd到玩家界面控件的属性 |
| [set_chat_send_enabled](#set_chat_send_enabled) | 开启/禁用发送聊天功能 |
| [set_player_chat_show](#set_player_chat_show) | 显示/不显示玩家聊天 |
| [clear_player_chat_panel](#clear_player_chat_panel) | 清理聊天 |
| [send_chat_to_role](#send_chat_to_role) | 发送聊天给玩家 |
| [del_ui_prefab](#del_ui_prefab) | 删除界面预制实例 |
| [get_ui_comp_visible](#get_ui_comp_visible) | 【异步】获得玩家控件显隐性 |
| [set_role_micro_unit](#set_role_micro_unit) | 设置玩家的声音主单位 |
| [close_role_micro_unit](#close_role_micro_unit) | 关闭【玩家】的附近语音聊天 |
| [set_role_camp_sound_switch](#set_role_camp_sound_switch) | 设置【玩家】的同阵营语音聊天收听开关为【布尔】 |
| [set_role_camp_micro_switch](#set_role_camp_micro_switch) | 设置【玩家】的同阵营语音聊天发言开关为【布尔】 |
| [set_nearby_micro_switch](#set_nearby_micro_switch) | 设置【玩家】的附近语音聊天发言开关为【布尔】 |
| [set_nearby_sound_switch](#set_nearby_sound_switch) | 设置【玩家】的附近语音聊天收听开关为【布尔】 |
| [set_role_all_sound_switch](#set_role_all_sound_switch) | 设置【玩家】的所有人语音聊天收听开关为【布尔】 |
| [set_role_all_micro_switch](#set_role_all_micro_switch) | 设置【玩家】的所有人语音聊天发言开关为【布尔】 |
| [set_ui_comp_chat_channel](#set_ui_comp_chat_channel) | 设置聊天控件的频道为同盟或者所有人 |
| [set_ui_comp_anchor](#set_ui_comp_anchor) | 设置界面控件锚点 |
| [set_ui_comp_scale_9_enable](#set_ui_comp_scale_9_enable) | 设置界面控件九宫开关 |
| [set_ui_comp_cap_insets](#set_ui_comp_cap_insets) | 设置界面控件九宫值 |
| [set_ui_comp_bind_format](#set_ui_comp_bind_format) | 设置ui控件绑定公式 |
| [set_list_view_percent](#set_list_view_percent) | 设置列表滚动到百分比位置 |
| [get_ui_prefab_ins](#get_ui_prefab_ins) | 获得玩家的界面模块实例 |
| [get_ui_comp_prefab](#get_ui_comp_prefab) | 获得界面控件所属的界面模块实例(如果是的话) |
| [set_ui_comp_text_adaptive_min_size](#set_ui_comp_text_adaptive_min_size) | 设置字体大小跟随内容自适应最小值(需要重新设置文本生效) |
| [get_ui_prefab_child_by_path](#get_ui_prefab_child_by_path) | 通过预制实例+路径获得ui控件 |
| [get_input_field_content](#get_input_field_content) | 获得玩家输入框文本内容 |
| [set_ui_comp_anim_pos](#set_ui_comp_anim_pos) | 设置动画移动 |
| [set_ui_comp_anim_opacity](#set_ui_comp_anim_opacity) | 设置动画透明度 |
| [set_ui_comp_anim_scale](#set_ui_comp_anim_scale) | 设置动画缩放 |
| [set_ui_comp_anim_rotate](#set_ui_comp_anim_rotate) | 设置动画旋转 |
| [create_unit_editor_data](#create_unit_editor_data) | 创建新单位物编 |
| [set_camera_perspective_ray_unit](#set_camera_perspective_ray_unit) | 设置相机透视射线的焦点单位 |
| [create_spine](#create_spine) | create_spine |
| [convert_unit_attr_m2cm](#convert_unit_attr_m2cm) | 单位属性m转cm |
| [create_ability_editor_data](#create_ability_editor_data) | 创建新技能物编 |
| [create_projectile_editor_data](#create_projectile_editor_data) | 创建新投射物物编 |
| [create_destructible_editor_data](#create_destructible_editor_data) | 创建新可破坏物物编 |
| [api_get_editor_type_data](#api_get_editor_type_data) | 获取指定对象类型的物编数据 |
| [api_set_editor_type_data](#api_set_editor_type_data) | 设置指定对象类型的物编数据 |
| [api_get_collider_body](#api_get_collider_body) | 获取COLLIDER所属的刚体 |
| [api_set_collider_bool_attr](#api_set_collider_bool_attr) | 设置碰撞体的布尔类型属性 |
| [api_get_collider_bool_attr](#api_get_collider_bool_attr) | 获取碰撞体的布尔类型属性 |
| [api_set_collider_float_attr](#api_set_collider_float_attr) | 设置碰撞体的实数类型属性 |
| [api_is_collider_collision_category](#api_is_collider_collision_category) | 碰撞器的自身碰撞类别是否有指定类型 |
| [api_is_collider_collide_with_mask](#api_is_collider_collide_with_mask) | 碰撞器的目标碰撞类别是否有指定类型 |
| [api_is_collider_collision_category_player](#api_is_collider_collision_category_player) | 碰撞器的自身碰撞类别是否有玩家 |
| [api_is_collider_collision_category_floor](#api_is_collider_collision_category_floor) | 碰撞器的自身碰撞类别是否有地面 |
| [api_get_collider_collision_category](#api_get_collider_collision_category) | 获得碰撞器的自身碰撞类别 |
| [api_get_collider_collide_with_mask](#api_get_collider_collide_with_mask) | 获得碰撞器的目标碰撞类别 |
| [api_set_collider_collision_category](#api_set_collider_collision_category) | 设置碰撞器的自身碰撞类别 |
| [api_set_collider_collide_with_mask](#api_set_collider_collide_with_mask) | 获得碰撞器的目标碰撞类别 |
| [api_get_joint_by_bid](#api_get_joint_by_bid) | 根据jid获取joint |
| [api_create_fixed_joint](#api_create_fixed_joint) | 创建固定关节 |
| [api_destroy_joint](#api_destroy_joint) | 销毁关节 |
| [api_get_physics_entity_by_id](#api_get_physics_entity_by_id) | 根据id获取逻辑物理组件 |
| [api_get_physics_object_by_id](#api_get_physics_object_by_id) | 根据id获取物理组件 |
| [api_get_rigid_body_in_physics_entity](#api_get_rigid_body_in_physics_entity) | 根据名称获取逻辑物理组件中的rigidbody |
| [api_get_unit_or_physics_entity_pos](#api_get_unit_or_physics_entity_pos) | 获取单位或者物理组件的位置 |
| [api_physics_raycast](#api_physics_raycast) | 射线检测 |
| [api_get_physics_raycast_first_point](#api_get_physics_raycast_first_point) | 获得射线检测首次碰撞点 |
| [api_set_physics_object_activated_and_visible](#api_set_physics_object_activated_and_visible) | 设置物理组件可见性(以及是否为生效状态) |
| [api_set_physics_entity_activated_and_visible](#api_set_physics_entity_activated_and_visible) | 设置逻辑物理组件可见性(以及是否为生效状态) |
| [api_check_physics_is_overlapping](#api_check_physics_is_overlapping) | 单位/逻辑物理组件之间是否有重叠 |
| [api_check_physics_is_contacting](#api_check_physics_is_contacting) | 单位/逻辑物理组件之间是否有碰撞 |
| [api_create_physics_object](#api_create_physics_object) | 创建物理组件 |
| [api_create_physics_entity](#api_create_physics_entity) | 创建逻辑物理组件 |
| [api_del_physics_object](#api_del_physics_object) | 删除物理组件 |
| [api_del_physics_entity](#api_del_physics_entity) | 删除逻辑物理组件 |
| [api_physics_entity_is_exist](#api_physics_entity_is_exist) | 逻辑物理组件是否存在 |
| [api_physics_play_animation](#api_physics_play_animation) | 逻辑物理组件中指定刚体的模型播放动画 |
| [api_get_physics_entity_state](#api_get_physics_entity_state) | 获得逻辑物理组件的状态 |
| [api_set_entity_state](#api_set_entity_state) | 设置逻辑物理组件状态 |
| [api_set_entity_active](#api_set_entity_active) | 设置逻辑物理组件的激活状态 |
| [api_is_physics_entity_active](#api_is_physics_entity_active) | 判断逻辑物理组件是激活状态 |
| [api_is_physics_entity_deactive](#api_is_physics_entity_deactive) | 判断逻辑物理组件是关闭状态 |
| [api_get_physics_entity](#api_get_physics_entity) | 根据id获得逻辑物理组件 |
| [api_set_gravity](#api_set_gravity) | 设置重力加速度 |
| [api_create_sfx_on_rigid](#api_create_sfx_on_rigid) | 创建特效到逻辑物理组件 |
| [api_get_physics_entity_type](#api_get_physics_entity_type) | 获取逻辑物理组件类型 |
| [api_destroy_physics_entity](#api_destroy_physics_entity) | 销毁逻辑物理组件 |
| [api_physics_entity_set_orientation](#api_physics_entity_set_orientation) | 设置逻辑物理组件旋转（欧拉角） |
| [api_physics_entity_has_tag](#api_physics_entity_has_tag) | 逻辑物理组件是否有指定tag |
| [api_physics_entity_add_tag](#api_physics_entity_add_tag) | 逻辑物理组件添加tag |
| [api_physics_entity_remove_tag](#api_physics_entity_remove_tag) | 逻辑物理组件删除tag |
| [api_world_pos_to_camera_pos](#api_world_pos_to_camera_pos) | 世界坐标转换屏幕坐标 |
| [api_world_pos_to_screen_edge_pos](#api_world_pos_to_screen_edge_pos) | 世界坐标转换屏幕边缘坐标 |
| [api_create_physics_filter](#api_create_physics_filter) | 创建物理过滤器 |
| [api_get_rigid_body_in_unit](#api_get_rigid_body_in_unit) | 获取单位的rigidBody |
| [set_physics_ctrl_unit](#set_physics_ctrl_unit) | 设置物理主控单位 |
| [get_physics_ctrl_unit](#get_physics_ctrl_unit) | 获取物理主控单位 |
| [api_set_cc_visibility](#api_set_cc_visibility) | 设置主控单位可见性visual |
| [create_unit_at_vector3](#create_unit_at_vector3) | 创建单位 |
| [api_unit_transmit_3d](#api_unit_transmit_3d) | 单位传送到指定坐标 |
| [api_revive_unit_3d](#api_revive_unit_3d) | 复活单位 |
| [api_get_character_state_name](#api_get_character_state_name) | 获取角色所处状态机节点名称 |
| [cc_look_at_camera](#cc_look_at_camera) | 让单位lookat镜头 |
| [cc_look_at_other_unit](#cc_look_at_other_unit) | 让单位lookat目标单位 |
| [cc_cancel_look_at](#cc_cancel_look_at) | 取消单位lookat |
| [cc_get_random_unit_around](#cc_get_random_unit_around) | 获取单位周围的随机单位 |
| [api_check_asm_state](#api_check_asm_state) | 动画状态机状态判断 |
| [api_get_grab_character](#api_get_grab_character) | 获取单位碰撞盒里最近的抓取单位（测试用） |
| [api_grab](#api_grab) | 抓取技能 |
| [check_catch_other_character](#check_catch_other_character) | 判断 - 是否可以施放暴揍技能 |
| [api_physics_catch](#api_physics_catch) | 暴揍技能 |
| [api_disconnect_hand](#api_disconnect_hand) | 移除手部黏连状态 |
| [api_disconnect_both_hands](#api_disconnect_both_hands) | 移除双手的黏连状态 |
| [api_check_hand_connection](#api_check_hand_connection) | 检查手部是否处于黏连状态 |
| [cc_do_predefined_action](#cc_do_predefined_action) | 主控角色做预定义行为 |
| [api_override_anim_status](#api_override_anim_status) | 重载角色动画状态 |
| [is_upper_body_limited](#is_upper_body_limited) | 判断单位上半身行动受限 |
| [api_physics_throw](#api_physics_throw) | 投掷技能 |
| [api_physics_pick_up](#api_physics_pick_up) | 拾取物品 |
| [api_physics_pick_up_item](#api_physics_pick_up_item) | 拾取指定物品 |
| [api_physics_drop](#api_physics_drop) | 单位丢弃物理道具 |
| [api_physics_hit_down_unit](#api_physics_hit_down_unit) | 施加倒地状态 |
| [api_get_grab_unit](#api_get_grab_unit) | 获取抓举单位 |
| [api_check_grab_state](#api_check_grab_state) | 检查是否处于抓举状态 |
| [api_get_pick_item](#api_get_pick_item) | 获取手持物品 |
| [api_check_physics_unit_pick_item_exist](#api_check_physics_unit_pick_item_exist) | 检查是否手持物品 |
| [api_add_unit_down_value](#api_add_unit_down_value) | 增加击倒值 |
| [api_character_try_begin_use](#api_character_try_begin_use) | 开始使用手持道具 |
| [api_character_try_end_use](#api_character_try_end_use) | 结束使用手持道具 |
| [api_set_entity_anim_state_machine_physics](#api_set_entity_anim_state_machine_physics) | 设置动画状态机为物理状态 |
| [api_physics_unit_get_move_speed](#api_physics_unit_get_move_speed) | 获取角色移动速度 |
| [api_physics_unit_set_orientation](#api_physics_unit_set_orientation) | 设置单位旋转（欧拉角） |
| [cc_change_emo](#cc_change_emo) | 主控角色做预定义表情 |
| [api_asm_jump_to_state](#api_asm_jump_to_state) | 单位切换状态机 |
| [api_set_unit_squash](#api_set_unit_squash) | 设置角色squash |
| [api_set_unit_move](#api_set_unit_move) | 设置单位移动 |
| [api_set_unit_stop_move](#api_set_unit_stop_move) | 设置单位停止移动 |
| [api_notify_custom_key](#api_notify_custom_key) | 通知改键 |
| [api_set_unit_jump](#api_set_unit_jump) | 设置单位跳跃 |
| [api_set_unit_run](#api_set_unit_run) | 设置单位跑(角色配置的跑步速度) |
| [api_set_unit_walk](#api_set_unit_walk) | 设置单位走(角色配置的走路速度) |
| [api_set_unit_speed](#api_set_unit_speed) | 设置单位速度 |
| [api_set_audio_cc](#api_set_audio_cc) | 设置语音指令 |
| [api_get_rigid_body_by_bid](#api_get_rigid_body_by_bid) | 根据bid获取rigidBody |
| [api_add_sphere_collider](#api_add_sphere_collider) | 刚体添加球形碰撞器 |
| [api_get_rigid_body_in_physics_object](#api_get_rigid_body_in_physics_object) | 根据名称获取物理组件中的rigidbody |
| [api_get_rigid_body_owner_unit](#api_get_rigid_body_owner_unit) | 获取刚体所属的单位 |
| [api_get_rigid_body_owner_physics_entity](#api_get_rigid_body_owner_physics_entity) | 获取刚体所属的逻辑物理组件 |
| [api_add_force_to_rigid_body](#api_add_force_to_rigid_body) | 向刚体施加力 |
| [api_add_velocity_to_rigid_body](#api_add_velocity_to_rigid_body) | 给刚体叠加速度 |
| [api_get_rigid_body_pos](#api_get_rigid_body_pos) | 获取刚体的位置 |
| [api_set_rigid_body_pos](#api_set_rigid_body_pos) | 设置刚体的位置 |
| [api_set_rigid_body_direction](#api_set_rigid_body_direction) | 设置刚体的朝向 |
| [api_set_rigid_body_type](#api_set_rigid_body_type) | 设置刚体的刚体类型 |
| [api_set_rigid_body_bool_attr](#api_set_rigid_body_bool_attr) | 设置刚体的布尔类型属性 |
| [api_set_rigidbody_active](#api_set_rigidbody_active) | 设置刚体有效性 |
| [api_set_rigidbody_visible](#api_set_rigidbody_visible) | 设置刚体模型可见性 |
| [api_get_rigidbody_active](#api_get_rigidbody_active) | 获取刚体有效性 |
| [api_set_rigidbody_velocity](#api_set_rigidbody_velocity) | 设置刚体速度 |
| [api_get_rigidbody_velocity](#api_get_rigidbody_velocity) | 获得刚体速度 |
| [api_set_rigidbody_angular_velocity](#api_set_rigidbody_angular_velocity) | 设置刚体角速度 |
| [api_get_rigidbody_angular_velocity](#api_get_rigidbody_angular_velocity) | 设置刚体角速度 |
| [api_get_rigidbody_forward](#api_get_rigidbody_forward) | 获得刚体朝向 |
| [api_get_rigid_body_group_in_range](#api_get_rigid_body_group_in_range) | 获得范围内的刚体组 |
| [api_replace_rigid_body_model](#api_replace_rigid_body_model) | 替换刚体模型 |
| [api_restore_rigid_body_last_model](#api_restore_rigid_body_last_model) | 还原刚体上一个模型 |
| [api_get_rigid_body_collider](#api_get_rigid_body_collider) | 获得刚体中指定名字的碰撞器 |
| [api_is_rigid_has_tag](#api_is_rigid_has_tag) | 刚体是否有指定tag |
| [api_rigid_body_get_mass](#api_rigid_body_get_mass) | 获取刚体质量 |
| [api_rigid_body_set_scale](#api_rigid_body_set_scale) | 设置刚体模型缩放 |
| [api_rigid_body_angle_axis](#api_rigid_body_angle_axis) | 刚体按照指定轴旋转 |
| [api_throw_rigid_body](#api_throw_rigid_body) | 扔出刚体 |
| [api_set_rigid_body_reference_frame_velocity](#api_set_rigid_body_reference_frame_velocity) | 设置刚体的相对坐标系的速度 |
| [api_set_rigid_body_add_reference_frame](#api_set_rigid_body_add_reference_frame) | 设置刚体绑定目标刚体的相对坐标系 |
| [api_set_rigid_body_remove_reference_frame](#api_set_rigid_body_remove_reference_frame) | 设置刚体移除目标刚体的相对坐标系 |
| [api_transform_local_to_global_coords](#api_transform_local_to_global_coords) | 把刚体的本地坐标转到全局坐标 |
| [api_add_rigid_body_to_group](#api_add_rigid_body_to_group) | 添加刚体到刚体组 |
| [api_remove_rigid_body_in_group](#api_remove_rigid_body_in_group) | 从刚体组中移除刚体 |
| [api_delete_reaction](#api_delete_reaction) | 删除REACTION |
| [api_delete_reaction_group](#api_delete_reaction_group) | 删除REACTION Group |
| [api_add_uniform_gravitation_field_to_rigid_body](#api_add_uniform_gravitation_field_to_rigid_body) | 刚体增加均匀引力场 |
| [api_add_wind_force_field_to_rigid_body](#api_add_wind_force_field_to_rigid_body) | 刚体增加风场 |
| [throw_physics_item](#throw_physics_item) | 物理物品抛出 |
| [get_physics_item_body_object](#get_physics_item_body_object) | 获取物理物品的刚体 |
| [api_remove_physics_item](#api_remove_physics_item) | 删除逻辑物理物品 |
| [api_physics_item_viewer_detach](#api_physics_item_viewer_detach) | 逻辑物理物品模型解绑持有者 |
| [api_physics_item_get_ability](#api_physics_item_get_ability) | 获取逻辑物理物品绑定技能 |
| [api_physics_item_create_sfx](#api_physics_item_create_sfx) | 逻辑物理物品创建特效 |
| [api_physics_item_play_animation](#api_physics_item_play_animation) | 逻辑物理物品播放动画 |
| [throw_physics_entity](#throw_physics_entity) | 单位扔出物理组件 |
| [api_detach_physics_entity_viewer](#api_detach_physics_entity_viewer) | 持有者解绑逻辑物理组件模型 |
| [api_get_physics_entity_owner](#api_get_physics_entity_owner) | 获得逻辑物理组件的持有者 |
| [create_sfx_on_point_3d](#create_sfx_on_point_3d) | 创建特效到三维坐标 |
| [report_info](#report_info) | 埋点 |
| [api_debug_pause](#api_debug_pause) | 调试暂停 |
| [init_lua_var](#init_lua_var) | LUA层初始化参数 |
| [set_lua_var](#set_lua_var) | 从lua设置变量 |
| [get_lua_var](#get_lua_var) | 从lua读取变量 |
| [set_random_seed](#set_random_seed) | 设置随机数种子 |
| [get_random_seed](#get_random_seed) | 获取随机数种子 |
| [create_unit](#create_unit) | 创建单位 |
| [change_unit_role](#change_unit_role) | 改变单位所属玩家 |
| [change_projectile_owner](#change_projectile_owner) | 改变投射物所属单位 |
| [change_projectile_ability](#change_projectile_ability) | 改变投射物所属技能 |
| [change_role_res_icon](#change_role_res_icon) | 修改玩家资源图标 |
| [change_role_res_icon_with_icon](#change_role_res_icon_with_icon) | 修改玩家资源图标(图片类型) |
| [remove_control_unit](#remove_control_unit) | 移除控制列表中的某个单位 |
| [get_unit_ids_in_team](#get_unit_ids_in_team) | 获取队伍内单位列表 |
| [add_unit_to_team](#add_unit_to_team) | 给队伍添加单位 |
| [remove_unit_from_team](#remove_unit_from_team) | 从队伍中去除单位 |
| [create_illusion](#create_illusion) | 创建幻象 |
| [is_unit_illusion](#is_unit_illusion) | 判断单位是否是幻象单位 |
| [get_illusion_caller_unit](#get_illusion_caller_unit) | 获取幻象召唤者 |
| [create_projectile_on_socket](#create_projectile_on_socket) | 在单位的挂接点创建一个投掷物 |
| [create_projectile_in_scene](#create_projectile_in_scene) | 创建一个投掷物 |
| [create_projectile_in_scene_new](#create_projectile_in_scene_new) | 创建一个投掷物 |
| [add_role_to_group](#add_role_to_group) | 将玩家添加到玩家组 |
| [rem_role_from_group](#rem_role_from_group) | 玩家组中删除玩家 |
| [get_unit_by_id](#get_unit_by_id) | 根据单位ID获取单位 |
| [get_projectile_by_id](#get_projectile_by_id) | 根据特效ID获取特效 |
| [judge_unit_in_group](#judge_unit_in_group) | 判断单位是否在单位组 |
| [api_get_tech_icon](#api_get_tech_icon) | 获取科技图标 |
| [update_global_weather](#update_global_weather) | 设置全局天气 |
| [get_global_weather](#get_global_weather) | 获得全局天气 |
| [start_skill_pointer](#start_skill_pointer) | 打开技能指示器 |
| [stop_skill_pointer](#stop_skill_pointer) | 关闭技能指示器 |
| [create_preview_skill_pointer](#create_preview_skill_pointer) | 打开技能指示器 |
| [clear_preview_skill_pointer](#clear_preview_skill_pointer) | 关闭技能指示器 |
| [get_ability_key_skill_pointer](#get_ability_key_skill_pointer) | 技能类型指示器 |
| [send_signal](#send_signal) | 发送信号 |
| [get_point_light_res_by_res_id](#get_point_light_res_by_res_id) | 根据点光源ID返回点光源 |
| [get_spot_light_res_by_res_id](#get_spot_light_res_by_res_id) | 根据方向光源ID返回方向光源 |
| [create_point_light_to_point](#create_point_light_to_point) | 创建点光源到点 |
| [create_point_light_to_unit_socket](#create_point_light_to_unit_socket) | 创建点光源到单位绑点 |
| [create_spot_light_to_point](#create_spot_light_to_point) | 创建方向光源到点 |
| [create_spot_light_to_unit_socket](#create_spot_light_to_unit_socket) | 创建方向光源到单位绑点 |
| [remove_light](#remove_light) | 删除光源 |
| [set_light_float_attr_value](#set_light_float_attr_value) | 设置光源Float属性 |
| [get_units_by_key](#get_units_by_key) | 获取固定单位编号的单位组 |
| [get_random_n_unit_in_group](#get_random_n_unit_in_group) | 单位组内随机整数个单位 |
| [get_first_unit_in_group](#get_first_unit_in_group) | 单位组内第一个单位 |
| [get_last_unit_in_group](#get_last_unit_in_group) | 单位组内最后一个单位 |
| [get_unit_sort_by_attr](#get_unit_sort_by_attr) | 根据属性值从单位组中取整数个单位 |
| [get_unit_sort_by_position](#get_unit_sort_by_position) | 根据距离从单位组中取整数个单位 |
| [get_random_unit_in_unit_group](#get_random_unit_in_unit_group) | 单位组内随机一个单位 |
| [api_get_influenced_by_cd_reduce](#api_get_influenced_by_cd_reduce) | 技能类型是否受冷却缩减影响 |
| [get_ability_conf_str_attr](#get_ability_conf_str_attr) | 技能类型的字符串属性 |
| [get_ability_conf_bool_attr](#get_ability_conf_bool_attr) | 技能类型的布尔属性 |
| [get_ability_conf_float_attr](#get_ability_conf_float_attr) | 技能类型的实数属性 |
| [get_ability_conf_int_attr](#get_ability_conf_int_attr) | 技能类型的整数属性 |
| [get_ability_conf_formula_attr](#get_ability_conf_formula_attr) | 技能类型的公式属性 |
| [get_ability_conf_formula_attr_with_unit](#get_ability_conf_formula_attr_with_unit) | 技能类型的公式属性 |
| [get_target_unit_in_ability](#get_target_unit_in_ability) | 技能选取的目标单位 |
| [get_target_item_in_ability](#get_target_item_in_ability) | 技能选取的目标物品 |
| [get_target_dest_in_ability](#get_target_dest_in_ability) | 技能选取的目标可破坏物 |
| [filter_unit_id_list_in_area](#filter_unit_id_list_in_area) | 筛选范围内单位(废弃) |
| [filter_unit_id_list_in_area_v2](#filter_unit_id_list_in_area_v2) | 筛选范围内单位 |
| [filter_projectile_id_list_in_area](#filter_projectile_id_list_in_area) | 筛选范围内投射物 |
| [get_all_projectiles_with_tag](#get_all_projectiles_with_tag) | 筛选带有tag的投射物 |
| [get_camp_by_camp_id](#get_camp_by_camp_id) | 按阵营编号获取阵营对象 |
| [get_camp_id_by_role_id](#get_camp_id_by_role_id) | 按玩家编号获取阵营编号 |
| [get_role_by_role_id](#get_role_by_role_id) | 按玩家编号获取玩家对象 |
| [get_role_by_int](#get_role_by_int) | 按整型获取玩家对象 |
| [get_alive_unit_num_by_camp_id](#get_alive_unit_num_by_camp_id) | 获取阵营存活单位数量 |
| [get_all_role_ids](#get_all_role_ids) | 所有玩家 |
| [get_role_ids_by_camp](#get_role_ids_by_camp) | 阵营所有玩家 |
| [get_role_ids_by_type](#get_role_ids_by_type) | 特定类型玩家 |
| [get_ally_ids_by_role](#get_ally_ids_by_role) | 同盟玩家 |
| [get_enemy_ids_by_role](#get_enemy_ids_by_role) | 获取某玩家敌对玩家组 |
| [get_victorious_role_ids](#get_victorious_role_ids) | 获取获胜玩家组 |
| [get_defeated_role_ids](#get_defeated_role_ids) | 获取失利玩家组 |
| [api_if_pri_attr_state_open](#api_if_pri_attr_state_open) | 三维属性是否开启 |
| [is_enemy](#is_enemy) | 判断单位敌对关系 |
| [is_ally](#is_ally) | 判断单位友军关系 |
| [get_visibility_of_unit](#get_visibility_of_unit) | 玩家或单位是否拥有单位的可见性 |
| [role_in_game](#role_in_game) | 玩家是否加入游戏 |
| [role_has_store_item](#role_has_store_item) | 玩家是否拥有收费道具 |
| [has_download_save_data_callback](#has_download_save_data_callback) | 玩家下载存档是否回调 |
| [get_last_created_item](#get_last_created_item) | 获取最近创建的物品 |
| [create_items](#create_items) | 创建物品 |
| [get_item](#get_item) | 根据id获取物品 |
| [get_item_by_unit_id](#get_item_by_unit_id) | 根据物品id获取物品 |
| [get_item_conf_name](#get_item_conf_name) | 获取物品配置名称 |
| [create_item_by_id](#create_item_by_id) | 创建单个物品 |
| [get_texture_by_icon_id](#get_texture_by_icon_id) | 根据ID获取图片 |
| [get_icon_id_by_texture](#get_icon_id_by_texture) | 根据图片获取ID |
| [refresh_triggers](#refresh_triggers) | 刷新触发器 |
| [enable_global_lua_trigger](#enable_global_lua_trigger) | 激活Lua动态触发器 |
| [get_dest_by_id](#get_dest_by_id) | 根据预设id获取可破坏物 |
| [get_dest_type](#get_dest_type) | 获取可破坏物类型 |
| [is_dest_in_area](#is_dest_in_area) | 判断可破坏物是否在区域中 |
| [create_destructible](#create_destructible) | 创建可破坏物 |
| [create_destructible_new](#create_destructible_new) | 创建可破坏物 |
| [get_all_dest_in_area](#get_all_dest_in_area) | 获取区域内的可破坏物列表 |
| [get_all_dest_in_point_rng](#get_all_dest_in_point_rng) | 获取点范围内的可破坏物列表 |
| [get_all_dest_in_shapes](#get_all_dest_in_shapes) | 获取不同形状范围内的可破坏物列表 |
| [add_camera_conf](#add_camera_conf) | 创建镜头 |
| [apply_camera_conf](#apply_camera_conf) | 应用镜头配置 |
| [camera_linear_move_duration](#camera_linear_move_duration) | 线性移动镜头(时间) |
| [camera_linear_move_speed](#camera_linear_move_speed) | 线性移动镜头(初速度) |
| [camera_look_at](#camera_look_at) | 让镜头看向某点（镜头位置不变） |
| [camera_set_param_roll](#camera_set_param_roll) | 设置镜头参数roll |
| [camera_set_param_pitch](#camera_set_param_pitch) | 设置镜头参数pitch |
| [camera_set_param_yaw](#camera_set_param_yaw) | 设置镜头参数yaw |
| [camera_set_param_rotate](#camera_set_param_rotate) | 设置镜头角度参数 |
| [camera_set_param_distance](#camera_set_param_distance) | 设置镜头参数distance |
| [camera_rotate_pitch_angle_duration](#camera_rotate_pitch_angle_duration) | 旋转镜头俯仰角（角度，时间） |
| [camera_rotate_pitch_speed_duration](#camera_rotate_pitch_speed_duration) | 旋转镜头俯仰角（角速度，时间） |
| [camera_rotate_pitch_speed_angle](#camera_rotate_pitch_speed_angle) | 旋转镜头俯仰角（角速度，角度） |
| [camera_rotate_yaw_angle_duration](#camera_rotate_yaw_angle_duration) | 旋转镜头导航角（角度，时间） |
| [camera_rotate_yaw_speed_duration](#camera_rotate_yaw_speed_duration) | 旋转镜头导航角（角速度，时间） |
| [camera_rotate_yaw_speed_angle](#camera_rotate_yaw_speed_angle) | 旋转镜头导航角（角速度，角度） |
| [camera_rotate_roll_angle_duration](#camera_rotate_roll_angle_duration) | 旋转镜头滚角（角度，时间） |
| [camera_rotate_roll_speed_duration](#camera_rotate_roll_speed_duration) | 旋转镜头滚角（角速度，时间） |
| [camera_rotate_roll_speed_angle](#camera_rotate_roll_speed_angle) | 旋转镜头滚角（角速度，角度） |
| [camera_shake_xy](#camera_shake_xy) | 镜头摇晃xy |
| [camera_shake_z](#camera_shake_z) | 镜头摇晃z |
| [camera_shake](#camera_shake) | 镜头摇晃xy |
| [camera_shake_with_decay](#camera_shake_with_decay) | 镜头带衰减震动 |
| [camera_limit_area](#camera_limit_area) | 镜头限制移动区域 |
| [camera_limit_area_close](#camera_limit_area_close) | 镜头限制移动区域 |
| [camera_set_follow_unit](#camera_set_follow_unit) | 镜头跟随某个单位 |
| [camera_set_tps_follow_unit](#camera_set_tps_follow_unit) | 镜头tps跟随某个单位 |
| [camera_cancel_tps_follow_unit](#camera_cancel_tps_follow_unit) | 取消镜头tps跟随单位 |
| [camera_cancel_follow_unit](#camera_cancel_follow_unit) | 将玩家相机解除绑定 |
| [camera_is_following_target](#camera_is_following_target) | 本地镜头在跟随状态 |
| [camera_set_focus_y](#camera_set_focus_y) | 设置玩家镜头焦点高度 |
| [camera_set_move_enable](#camera_set_move_enable) | 设置玩家相机允许移动 |
| [camera_set_move_not_enable](#camera_set_move_not_enable) | 设置玩家相机禁止移动 |
| [set_tps_mode_ctrl](#set_tps_mode_ctrl) | 设置第三人称跟随镜头鼠标控制开关 |
| [get_camera_attr_real_num](#get_camera_attr_real_num) | 获取本地玩家镜头的实数属性 |
| [get_camera_attr_integer](#get_camera_attr_integer) | 获取本地玩家镜头的整数属性 |
| [api_show_text](#api_show_text) | 向玩家正上方显示提示信息 |
| [show_tips_text](#show_tips_text) | 向玩家显示多语言信息 |
| [api_test_log_msg](#api_test_log_msg) | API测试记录日志并可选显示 |
| [api_test_show_msg_tip](#api_test_show_msg_tip) | API测试显示UI信息 |
| [api_test_add_log_assert_result](#api_test_add_log_assert_result) | API测试-向Log添加Assert结果 |
| [print_to_dialog](#print_to_dialog) | Dialog窗口输出信息 |
| [show_unit_text_to_role](#show_unit_text_to_role) | 向玩家显示单位对话 |
| [show_msg_to_role](#show_msg_to_role) | 向玩家左下角显示信息 |
| [show_game_end_ui_by_camp_id](#show_game_end_ui_by_camp_id) | 按阵营显示游戏结束信息 |
| [get_random_int](#get_random_int) | 范围内随机整数 |
| [get_random_fixed](#get_random_fixed) | 范围内随机定点数 |
| [get_random_angle](#get_random_angle) | 随机角度 |
| [api_calc_formula_kv](#api_calc_formula_kv) | 计算公式类型KV |
| [get_unit_group_num](#get_unit_group_num) | 单位组内所有状态的单位数量 |
| [refresh_unit_group](#refresh_unit_group) | 遍历时过滤单位组 |
| [refresh_projectile_group](#refresh_projectile_group) | 遍历时过滤投射物组 |
| [get_state_unit_num_in_group](#get_state_unit_num_in_group) | 单位组某状态的单位数量 |
| [get_num_of_unit_key_in_group](#get_num_of_unit_key_in_group) | 单位组中特定单位编号的单位数量 |
| [remove_unit_in_group_by_key](#remove_unit_in_group_by_key) | 删除单位组中某种单位 |
| [remove_unit_in_group](#remove_unit_in_group) | 删除单位组中某个单位 |
| [set_unit_group_selected](#set_unit_group_selected) | 设置单位组中单位选中 |
| [unit_key_pool_add_key](#unit_key_pool_add_key) | 单位编号池添加单位编号 |
| [unit_key_pool_rem_key](#unit_key_pool_rem_key) | 单位编号池删除单位编号 |
| [get_unit_key_from_pool](#get_unit_key_from_pool) | 单位编号池返回单位编号 |
| [get_unit_key_icon](#get_unit_key_icon) | 获取单位预设库配置的图标路径 |
| [get_item_key_icon](#get_item_key_icon) | 获取物品预设库配置的图标路径 |
| [get_unit_key_pic](#get_unit_key_pic) | 获取单位预设库配置的图片路径 |
| [get_unit_key_str](#get_unit_key_str) | 获取单位预设库配置的类型为字符串的属性 |
| [get_unit_key_fixed](#get_unit_key_fixed) | 获取单位预设库配置的类型为实数的属性 |
| [get_icon_by_uid](#get_icon_by_uid) | 根据UID获取预设库配置的图标路径 |
| [get_ability_key_icon](#get_ability_key_icon) | 获取技能预设库配置的图标路径 |
| [len_of_var](#len_of_var) | 变量长度 |
| [get_slave_coeff](#get_slave_coeff) | 获取三维属性的slave系数 |
| [set_slave_coeff](#set_slave_coeff) | 设置三维属性的slave系数 |
| [get_damage_ratio](#get_damage_ratio) | 攻击类型和防御类型对应的伤害系数 |
| [set_damage_ratio](#set_damage_ratio) | 设置攻击类型和防御类型对应的伤害系数 |
| [apply_damage](#apply_damage) | 应用伤害 |
| [get_hurt_damage](#get_hurt_damage) | 攻击伤害绝对值 |
| [set_cur_damage](#set_cur_damage) | 设置当前攻击伤害的数值 |
| [get_cur_damage_is_miss](#get_cur_damage_is_miss) | 获取当次攻击是否闪避 |
| [get_item_key_unit_group_command_type_kv](#get_item_key_unit_group_command_type_kv) | 获取物品编号UNIT_GROUP_COMMAND_TYPE键值对 |
| [get_ability_key_unit_group_command_type_kv](#get_ability_key_unit_group_command_type_kv) | 获取技能编号UNIT_GROUP_COMMAND_TYPE键值对 |
| [get_modifier_key_unit_group_command_type_kv](#get_modifier_key_unit_group_command_type_kv) | 获取魔法效果特效编号UNIT_GROUP_COMMAND_TYPE键值对 |
| [get_projectile_key_unit_group_command_type_kv](#get_projectile_key_unit_group_command_type_kv) | 获取特效编号UNIT_GROUP_COMMAND_TYPE键值对 |
| [get_destructible_key_unit_group_command_type_kv](#get_destructible_key_unit_group_command_type_kv) | 获取可破坏物编号UNIT_GROUP_COMMAND_TYPE键值对 |
| [get_tech_key_unit_group_command_type_kv](#get_tech_key_unit_group_command_type_kv) | 获取科技编号UNIT_GROUP_COMMAND_TYPE键值对 |
| [get_icon_id_unit_group_command_type_kv](#get_icon_id_unit_group_command_type_kv) | 获取图片UNIT_GROUP_COMMAND_TYPE键值对 |
| [get_physics_entity_key_unit_group_command_type_kv](#get_physics_entity_key_unit_group_command_type_kv) | 获取逻辑物理组件类型UNIT_GROUP_COMMAND_TYPE键值对 |
| [get_kv_pair_value_unit_group_command_type](#get_kv_pair_value_unit_group_command_type) | 获取UNIT_GROUP_COMMAND_TYPE键值对 |
| [get_unit_key_rescue_seeker_type_kv](#get_unit_key_rescue_seeker_type_kv) | 获取单位编号RESCUE_SEEKER_TYPE键值对 |
| [get_item_key_rescue_seeker_type_kv](#get_item_key_rescue_seeker_type_kv) | 获取物品编号RESCUE_SEEKER_TYPE键值对 |
| [get_ability_key_rescue_seeker_type_kv](#get_ability_key_rescue_seeker_type_kv) | 获取技能编号RESCUE_SEEKER_TYPE键值对 |
| [get_modifier_key_rescue_seeker_type_kv](#get_modifier_key_rescue_seeker_type_kv) | 获取魔法效果特效编号RESCUE_SEEKER_TYPE键值对 |
| [get_projectile_key_rescue_seeker_type_kv](#get_projectile_key_rescue_seeker_type_kv) | 获取特效编号RESCUE_SEEKER_TYPE键值对 |
| [get_destructible_key_rescue_seeker_type_kv](#get_destructible_key_rescue_seeker_type_kv) | 获取可破坏物编号RESCUE_SEEKER_TYPE键值对 |
| [get_tech_key_rescue_seeker_type_kv](#get_tech_key_rescue_seeker_type_kv) | 获取科技编号RESCUE_SEEKER_TYPE键值对 |
| [get_icon_id_rescue_seeker_type_kv](#get_icon_id_rescue_seeker_type_kv) | 获取图片RESCUE_SEEKER_TYPE键值对 |
| [get_physics_entity_key_rescue_seeker_type_kv](#get_physics_entity_key_rescue_seeker_type_kv) | 获取逻辑物理组件类型RESCUE_SEEKER_TYPE键值对 |
| [get_kv_pair_value_rescue_seeker_type](#get_kv_pair_value_rescue_seeker_type) | 获取RESCUE_SEEKER_TYPE键值对 |
| [get_unit_key_rescuer_type_kv](#get_unit_key_rescuer_type_kv) | 获取单位编号RESCUER_TYPE键值对 |
| [get_item_key_rescuer_type_kv](#get_item_key_rescuer_type_kv) | 获取物品编号RESCUER_TYPE键值对 |
| [get_ability_key_rescuer_type_kv](#get_ability_key_rescuer_type_kv) | 获取技能编号RESCUER_TYPE键值对 |
| [get_modifier_key_rescuer_type_kv](#get_modifier_key_rescuer_type_kv) | 获取魔法效果特效编号RESCUER_TYPE键值对 |
| [get_projectile_key_rescuer_type_kv](#get_projectile_key_rescuer_type_kv) | 获取特效编号RESCUER_TYPE键值对 |
| [get_destructible_key_rescuer_type_kv](#get_destructible_key_rescuer_type_kv) | 获取可破坏物编号RESCUER_TYPE键值对 |
| [get_tech_key_rescuer_type_kv](#get_tech_key_rescuer_type_kv) | 获取科技编号RESCUER_TYPE键值对 |
| [get_icon_id_rescuer_type_kv](#get_icon_id_rescuer_type_kv) | 获取图片RESCUER_TYPE键值对 |
| [get_physics_entity_key_rescuer_type_kv](#get_physics_entity_key_rescuer_type_kv) | 获取逻辑物理组件类型RESCUER_TYPE键值对 |
| [get_kv_pair_value_rescuer_type](#get_kv_pair_value_rescuer_type) | 获取RESCUER_TYPE键值对 |
| [get_unit_key_store_item_type_kv](#get_unit_key_store_item_type_kv) | 获取单位编号STORE_ITEM_TYPE键值对 |
| [get_item_key_store_item_type_kv](#get_item_key_store_item_type_kv) | 获取物品编号STORE_ITEM_TYPE键值对 |
| [get_ability_key_store_item_type_kv](#get_ability_key_store_item_type_kv) | 获取技能编号STORE_ITEM_TYPE键值对 |
| [get_modifier_key_store_item_type_kv](#get_modifier_key_store_item_type_kv) | 获取魔法效果特效编号STORE_ITEM_TYPE键值对 |
| [get_projectile_key_store_item_type_kv](#get_projectile_key_store_item_type_kv) | 获取特效编号STORE_ITEM_TYPE键值对 |
| [get_destructible_key_store_item_type_kv](#get_destructible_key_store_item_type_kv) | 获取可破坏物编号STORE_ITEM_TYPE键值对 |
| [get_tech_key_store_item_type_kv](#get_tech_key_store_item_type_kv) | 获取科技编号STORE_ITEM_TYPE键值对 |
| [get_icon_id_store_item_type_kv](#get_icon_id_store_item_type_kv) | 获取图片STORE_ITEM_TYPE键值对 |
| [get_physics_entity_key_store_item_type_kv](#get_physics_entity_key_store_item_type_kv) | 获取逻辑物理组件类型STORE_ITEM_TYPE键值对 |
| [get_kv_pair_value_store_item_type](#get_kv_pair_value_store_item_type) | 获取STORE_ITEM_TYPE键值对 |
| [get_unit_key_site_state_kv](#get_unit_key_site_state_kv) | 获取单位编号SITE_STATE键值对 |
| [get_item_key_site_state_kv](#get_item_key_site_state_kv) | 获取物品编号SITE_STATE键值对 |
| [get_ability_key_site_state_kv](#get_ability_key_site_state_kv) | 获取技能编号SITE_STATE键值对 |
| [get_modifier_key_site_state_kv](#get_modifier_key_site_state_kv) | 获取魔法效果特效编号SITE_STATE键值对 |
| [get_projectile_key_site_state_kv](#get_projectile_key_site_state_kv) | 获取特效编号SITE_STATE键值对 |
| [get_destructible_key_site_state_kv](#get_destructible_key_site_state_kv) | 获取可破坏物编号SITE_STATE键值对 |
| [get_tech_key_site_state_kv](#get_tech_key_site_state_kv) | 获取科技编号SITE_STATE键值对 |
| [get_icon_id_site_state_kv](#get_icon_id_site_state_kv) | 获取图片SITE_STATE键值对 |
| [get_physics_entity_key_site_state_kv](#get_physics_entity_key_site_state_kv) | 获取逻辑物理组件类型SITE_STATE键值对 |
| [get_kv_pair_value_site_state](#get_kv_pair_value_site_state) | 获取SITE_STATE键值对 |
| [get_unit_key_coin_currency_kv](#get_unit_key_coin_currency_kv) | 获取单位编号COIN_CURRENCY键值对 |
| [get_item_key_coin_currency_kv](#get_item_key_coin_currency_kv) | 获取物品编号COIN_CURRENCY键值对 |
| [get_ability_key_coin_currency_kv](#get_ability_key_coin_currency_kv) | 获取技能编号COIN_CURRENCY键值对 |
| [get_modifier_key_coin_currency_kv](#get_modifier_key_coin_currency_kv) | 获取魔法效果特效编号COIN_CURRENCY键值对 |
| [get_projectile_key_coin_currency_kv](#get_projectile_key_coin_currency_kv) | 获取特效编号COIN_CURRENCY键值对 |
| [get_destructible_key_coin_currency_kv](#get_destructible_key_coin_currency_kv) | 获取可破坏物编号COIN_CURRENCY键值对 |
| [get_tech_key_coin_currency_kv](#get_tech_key_coin_currency_kv) | 获取科技编号COIN_CURRENCY键值对 |
| [get_icon_id_coin_currency_kv](#get_icon_id_coin_currency_kv) | 获取图片COIN_CURRENCY键值对 |
| [get_physics_entity_key_coin_currency_kv](#get_physics_entity_key_coin_currency_kv) | 获取逻辑物理组件类型COIN_CURRENCY键值对 |
| [get_kv_pair_value_coin_currency](#get_kv_pair_value_coin_currency) | 获取COIN_CURRENCY键值对 |
| [get_trigger_variable_ui_gridview_type](#get_trigger_variable_ui_gridview_type) | 获取全局触发器UI_GRIDVIEW_TYPE非数组变量 |
| [get_trigger_actor_variable_ui_gridview_type](#get_trigger_actor_variable_ui_gridview_type) | 获取触发器UI_GRIDVIEW_TYPE非数组 组变量 |
| [get_trigger_list_variable_ui_gridview_type](#get_trigger_list_variable_ui_gridview_type) | 获取全局触发器UI_GRIDVIEW_TYPE数组变量子项 |
| [get_trigger_list_actor_variable_ui_gridview_type](#get_trigger_list_actor_variable_ui_gridview_type) | 获取触发器UI_GRIDVIEW_TYPE数组 组变量子项 |
| [get_trigger_list_variable_all_ui_gridview_type](#get_trigger_list_variable_all_ui_gridview_type) | 获取全局触发器UI_GRIDVIEW_TYPE数组变量 |
| [get_trigger_list_actor_variable_all_ui_gridview_type](#get_trigger_list_actor_variable_all_ui_gridview_type) | 获取触发器UI_GRIDVIEW_TYPE 组变量数组 |
| [get_trigger_variable_ui_gridview_bar_type](#get_trigger_variable_ui_gridview_bar_type) | 获取全局触发器UI_GRIDVIEW_BAR_TYPE非数组变量 |
| [get_trigger_actor_variable_ui_gridview_bar_type](#get_trigger_actor_variable_ui_gridview_bar_type) | 获取触发器UI_GRIDVIEW_BAR_TYPE非数组 组变量 |
| [get_trigger_list_variable_ui_gridview_bar_type](#get_trigger_list_variable_ui_gridview_bar_type) | 获取全局触发器UI_GRIDVIEW_BAR_TYPE数组变量子项 |
| [get_trigger_list_actor_variable_ui_gridview_bar_type](#get_trigger_list_actor_variable_ui_gridview_bar_type) | 获取触发器UI_GRIDVIEW_BAR_TYPE数组 组变量子项 |
| [get_trigger_list_variable_all_ui_gridview_bar_type](#get_trigger_list_variable_all_ui_gridview_bar_type) | 获取全局触发器UI_GRIDVIEW_BAR_TYPE数组变量 |
| [get_trigger_list_actor_variable_all_ui_gridview_bar_type](#get_trigger_list_actor_variable_all_ui_gridview_bar_type) | 获取触发器UI_GRIDVIEW_BAR_TYPE 组变量数组 |
| [get_trigger_variable_ui_effect_camera_mode](#get_trigger_variable_ui_effect_camera_mode) | 获取全局触发器UI_EFFECT_CAMERA_MODE非数组变量 |
| [get_trigger_actor_variable_ui_effect_camera_mode](#get_trigger_actor_variable_ui_effect_camera_mode) | 获取触发器UI_EFFECT_CAMERA_MODE非数组 组变量 |
| [get_trigger_list_variable_ui_effect_camera_mode](#get_trigger_list_variable_ui_effect_camera_mode) | 获取全局触发器UI_EFFECT_CAMERA_MODE数组变量子项 |
| [get_trigger_list_actor_variable_ui_effect_camera_mode](#get_trigger_list_actor_variable_ui_effect_camera_mode) | 获取触发器UI_EFFECT_CAMERA_MODE数组 组变量子项 |
| [get_trigger_list_variable_all_ui_effect_camera_mode](#get_trigger_list_variable_all_ui_effect_camera_mode) | 获取全局触发器UI_EFFECT_CAMERA_MODE数组变量 |
| [get_trigger_list_actor_variable_all_ui_effect_camera_mode](#get_trigger_list_actor_variable_all_ui_effect_camera_mode) | 获取触发器UI_EFFECT_CAMERA_MODE 组变量数组 |
| [get_trigger_variable_ui_equip_slot_use_type](#get_trigger_variable_ui_equip_slot_use_type) | 获取全局触发器UI_EQUIP_SLOT_USE_TYPE非数组变量 |
| [get_trigger_actor_variable_ui_equip_slot_use_type](#get_trigger_actor_variable_ui_equip_slot_use_type) | 获取触发器UI_EQUIP_SLOT_USE_TYPE非数组 组变量 |
| [get_trigger_list_variable_ui_equip_slot_use_type](#get_trigger_list_variable_ui_equip_slot_use_type) | 获取全局触发器UI_EQUIP_SLOT_USE_TYPE数组变量子项 |
| [get_trigger_list_actor_variable_ui_equip_slot_use_type](#get_trigger_list_actor_variable_ui_equip_slot_use_type) | 获取触发器UI_EQUIP_SLOT_USE_TYPE数组 组变量子项 |
| [get_trigger_list_variable_all_ui_equip_slot_use_type](#get_trigger_list_variable_all_ui_equip_slot_use_type) | 获取全局触发器UI_EQUIP_SLOT_USE_TYPE数组变量 |
| [get_trigger_list_actor_variable_all_ui_equip_slot_use_type](#get_trigger_list_actor_variable_all_ui_equip_slot_use_type) | 获取触发器UI_EQUIP_SLOT_USE_TYPE 组变量数组 |
| [get_trigger_variable_ui_equip_slot_drag_type](#get_trigger_variable_ui_equip_slot_drag_type) | 获取全局触发器UI_EQUIP_SLOT_DRAG_TYPE非数组变量 |
| [get_trigger_actor_variable_ui_equip_slot_drag_type](#get_trigger_actor_variable_ui_equip_slot_drag_type) | 获取触发器UI_EQUIP_SLOT_DRAG_TYPE非数组 组变量 |
| [get_trigger_list_variable_ui_equip_slot_drag_type](#get_trigger_list_variable_ui_equip_slot_drag_type) | 获取全局触发器UI_EQUIP_SLOT_DRAG_TYPE数组变量子项 |
| [get_trigger_list_actor_variable_ui_equip_slot_drag_type](#get_trigger_list_actor_variable_ui_equip_slot_drag_type) | 获取触发器UI_EQUIP_SLOT_DRAG_TYPE数组 组变量子项 |
| [get_trigger_list_variable_all_ui_equip_slot_drag_type](#get_trigger_list_variable_all_ui_equip_slot_drag_type) | 获取全局触发器UI_EQUIP_SLOT_DRAG_TYPE数组变量 |
| [get_trigger_list_actor_variable_all_ui_equip_slot_drag_type](#get_trigger_list_actor_variable_all_ui_equip_slot_drag_type) | 获取触发器UI_EQUIP_SLOT_DRAG_TYPE 组变量数组 |
| [get_trigger_variable_ui_layout_clipping_type](#get_trigger_variable_ui_layout_clipping_type) | 获取全局触发器UI_LAYOUT_CLIPPING_TYPE非数组变量 |
| [get_trigger_actor_variable_ui_layout_clipping_type](#get_trigger_actor_variable_ui_layout_clipping_type) | 获取触发器UI_LAYOUT_CLIPPING_TYPE非数组 组变量 |
| [get_trigger_list_variable_ui_layout_clipping_type](#get_trigger_list_variable_ui_layout_clipping_type) | 获取全局触发器UI_LAYOUT_CLIPPING_TYPE数组变量子项 |
| [get_trigger_list_actor_variable_ui_layout_clipping_type](#get_trigger_list_actor_variable_ui_layout_clipping_type) | 获取触发器UI_LAYOUT_CLIPPING_TYPE数组 组变量子项 |
| [get_trigger_list_variable_all_ui_layout_clipping_type](#get_trigger_list_variable_all_ui_layout_clipping_type) | 获取全局触发器UI_LAYOUT_CLIPPING_TYPE数组变量 |
| [get_trigger_list_actor_variable_all_ui_layout_clipping_type](#get_trigger_list_actor_variable_all_ui_layout_clipping_type) | 获取触发器UI_LAYOUT_CLIPPING_TYPE 组变量数组 |
| [get_trigger_variable_ui_text_over_length_handling_type](#get_trigger_variable_ui_text_over_length_handling_type) | 获取全局触发器UI_TEXT_OVER_LENGTH_HANDLING_TYPE非数组变量 |
| [get_trigger_actor_variable_ui_text_over_length_handling_type](#get_trigger_actor_variable_ui_text_over_length_handling_type) | 获取触发器UI_TEXT_OVER_LENGTH_HANDLING_TYPE非数组 组变量 |
| [get_trigger_list_variable_ui_text_over_length_handling_type](#get_trigger_list_variable_ui_text_over_length_handling_type) | 获取全局触发器UI_TEXT_OVER_LENGTH_HANDLING_TYPE数组变量子项 |
| [get_trigger_list_actor_variable_ui_text_over_length_handling_type](#get_trigger_list_actor_variable_ui_text_over_length_handling_type) | 获取触发器UI_TEXT_OVER_LENGTH_HANDLING_TYPE数组 组变量子项 |
| [get_trigger_list_variable_all_ui_text_over_length_handling_type](#get_trigger_list_variable_all_ui_text_over_length_handling_type) | 获取全局触发器UI_TEXT_OVER_LENGTH_HANDLING_TYPE数组变量 |
| [get_trigger_list_actor_variable_all_ui_text_over_length_handling_type](#get_trigger_list_actor_variable_all_ui_text_over_length_handling_type) | 获取触发器UI_TEXT_OVER_LENGTH_HANDLING_TYPE 组变量数组 |
| [get_trigger_variable_ui_pos_adapt_mode](#get_trigger_variable_ui_pos_adapt_mode) | 获取全局触发器UI_POS_ADAPT_MODE非数组变量 |
| [get_trigger_actor_variable_ui_pos_adapt_mode](#get_trigger_actor_variable_ui_pos_adapt_mode) | 获取触发器UI_POS_ADAPT_MODE非数组 组变量 |
| [get_trigger_list_variable_ui_pos_adapt_mode](#get_trigger_list_variable_ui_pos_adapt_mode) | 获取全局触发器UI_POS_ADAPT_MODE数组变量子项 |
| [get_trigger_list_actor_variable_ui_pos_adapt_mode](#get_trigger_list_actor_variable_ui_pos_adapt_mode) | 获取触发器UI_POS_ADAPT_MODE数组 组变量子项 |
| [get_trigger_list_variable_all_ui_pos_adapt_mode](#get_trigger_list_variable_all_ui_pos_adapt_mode) | 获取全局触发器UI_POS_ADAPT_MODE数组变量 |
| [get_trigger_list_actor_variable_all_ui_pos_adapt_mode](#get_trigger_list_actor_variable_all_ui_pos_adapt_mode) | 获取触发器UI_POS_ADAPT_MODE 组变量数组 |
| [get_trigger_variable_ui_chat_send_channel](#get_trigger_variable_ui_chat_send_channel) | 获取全局触发器UI_CHAT_SEND_CHANNEL非数组变量 |
| [get_trigger_actor_variable_ui_chat_send_channel](#get_trigger_actor_variable_ui_chat_send_channel) | 获取触发器UI_CHAT_SEND_CHANNEL非数组 组变量 |
| [get_trigger_list_variable_ui_chat_send_channel](#get_trigger_list_variable_ui_chat_send_channel) | 获取全局触发器UI_CHAT_SEND_CHANNEL数组变量子项 |
| [get_trigger_list_actor_variable_ui_chat_send_channel](#get_trigger_list_actor_variable_ui_chat_send_channel) | 获取触发器UI_CHAT_SEND_CHANNEL数组 组变量子项 |
| [get_trigger_list_variable_all_ui_chat_send_channel](#get_trigger_list_variable_all_ui_chat_send_channel) | 获取全局触发器UI_CHAT_SEND_CHANNEL数组变量 |
| [get_trigger_list_actor_variable_all_ui_chat_send_channel](#get_trigger_list_actor_variable_all_ui_chat_send_channel) | 获取触发器UI_CHAT_SEND_CHANNEL 组变量数组 |
| [get_trigger_variable_ui_chat_recv_channel](#get_trigger_variable_ui_chat_recv_channel) | 获取全局触发器UI_CHAT_RECV_CHANNEL非数组变量 |
| [get_trigger_actor_variable_ui_chat_recv_channel](#get_trigger_actor_variable_ui_chat_recv_channel) | 获取触发器UI_CHAT_RECV_CHANNEL非数组 组变量 |
| [get_trigger_list_variable_ui_chat_recv_channel](#get_trigger_list_variable_ui_chat_recv_channel) | 获取全局触发器UI_CHAT_RECV_CHANNEL数组变量子项 |
| [get_trigger_list_actor_variable_ui_chat_recv_channel](#get_trigger_list_actor_variable_ui_chat_recv_channel) | 获取触发器UI_CHAT_RECV_CHANNEL数组 组变量子项 |
| [get_trigger_list_variable_all_ui_chat_recv_channel](#get_trigger_list_variable_all_ui_chat_recv_channel) | 获取全局触发器UI_CHAT_RECV_CHANNEL数组变量 |
| [get_trigger_list_actor_variable_all_ui_chat_recv_channel](#get_trigger_list_actor_variable_all_ui_chat_recv_channel) | 获取触发器UI_CHAT_RECV_CHANNEL 组变量数组 |
| [get_trigger_variable_ui_anim_play_mode](#get_trigger_variable_ui_anim_play_mode) | 获取全局触发器UI_ANIM_PLAY_MODE非数组变量 |
| [get_trigger_actor_variable_ui_anim_play_mode](#get_trigger_actor_variable_ui_anim_play_mode) | 获取触发器UI_ANIM_PLAY_MODE非数组 组变量 |
| [get_trigger_list_variable_ui_anim_play_mode](#get_trigger_list_variable_ui_anim_play_mode) | 获取全局触发器UI_ANIM_PLAY_MODE数组变量子项 |
| [get_trigger_list_actor_variable_ui_anim_play_mode](#get_trigger_list_actor_variable_ui_anim_play_mode) | 获取触发器UI_ANIM_PLAY_MODE数组 组变量子项 |
| [get_trigger_list_variable_all_ui_anim_play_mode](#get_trigger_list_variable_all_ui_anim_play_mode) | 获取全局触发器UI_ANIM_PLAY_MODE数组变量 |
| [get_trigger_list_actor_variable_all_ui_anim_play_mode](#get_trigger_list_actor_variable_all_ui_anim_play_mode) | 获取触发器UI_ANIM_PLAY_MODE 组变量数组 |
| [get_trigger_variable_ui_text_font_name](#get_trigger_variable_ui_text_font_name) | 获取全局触发器UI_TEXT_FONT_NAME非数组变量 |
| [get_trigger_actor_variable_ui_text_font_name](#get_trigger_actor_variable_ui_text_font_name) | 获取触发器UI_TEXT_FONT_NAME非数组 组变量 |
| [get_trigger_list_variable_ui_text_font_name](#get_trigger_list_variable_ui_text_font_name) | 获取全局触发器UI_TEXT_FONT_NAME数组变量子项 |
| [get_trigger_list_actor_variable_ui_text_font_name](#get_trigger_list_actor_variable_ui_text_font_name) | 获取触发器UI_TEXT_FONT_NAME数组 组变量子项 |
| [get_trigger_list_variable_all_ui_text_font_name](#get_trigger_list_variable_all_ui_text_font_name) | 获取全局触发器UI_TEXT_FONT_NAME数组变量 |
| [get_trigger_list_actor_variable_all_ui_text_font_name](#get_trigger_list_actor_variable_all_ui_text_font_name) | 获取触发器UI_TEXT_FONT_NAME 组变量数组 |
| [get_trigger_variable_ui_eca_anim_type](#get_trigger_variable_ui_eca_anim_type) | 获取全局触发器UI_ECA_ANIM_TYPE非数组变量 |
| [get_trigger_actor_variable_ui_eca_anim_type](#get_trigger_actor_variable_ui_eca_anim_type) | 获取触发器UI_ECA_ANIM_TYPE非数组 组变量 |
| [get_trigger_list_variable_ui_eca_anim_type](#get_trigger_list_variable_ui_eca_anim_type) | 获取全局触发器UI_ECA_ANIM_TYPE数组变量子项 |
| [get_trigger_list_actor_variable_ui_eca_anim_type](#get_trigger_list_actor_variable_ui_eca_anim_type) | 获取触发器UI_ECA_ANIM_TYPE数组 组变量子项 |
| [get_trigger_list_variable_all_ui_eca_anim_type](#get_trigger_list_variable_all_ui_eca_anim_type) | 获取全局触发器UI_ECA_ANIM_TYPE数组变量 |
| [get_trigger_list_actor_variable_all_ui_eca_anim_type](#get_trigger_list_actor_variable_all_ui_eca_anim_type) | 获取触发器UI_ECA_ANIM_TYPE 组变量数组 |
| [get_trigger_variable_local_unit_entity](#get_trigger_variable_local_unit_entity) | 获取全局触发器LOCAL_UNIT_ENTITY非数组变量 |
| [get_trigger_actor_variable_local_unit_entity](#get_trigger_actor_variable_local_unit_entity) | 获取触发器LOCAL_UNIT_ENTITY非数组 组变量 |
| [get_trigger_list_variable_local_unit_entity](#get_trigger_list_variable_local_unit_entity) | 获取全局触发器LOCAL_UNIT_ENTITY数组变量子项 |
| [get_trigger_list_actor_variable_local_unit_entity](#get_trigger_list_actor_variable_local_unit_entity) | 获取触发器LOCAL_UNIT_ENTITY数组 组变量子项 |
| [get_trigger_list_variable_all_local_unit_entity](#get_trigger_list_variable_all_local_unit_entity) | 获取全局触发器LOCAL_UNIT_ENTITY数组变量 |
| [get_trigger_list_actor_variable_all_local_unit_entity](#get_trigger_list_actor_variable_all_local_unit_entity) | 获取触发器LOCAL_UNIT_ENTITY 组变量数组 |
| [get_trigger_variable_local_unit_group](#get_trigger_variable_local_unit_group) | 获取全局触发器LOCAL_UNIT_GROUP非数组变量 |
| [get_trigger_actor_variable_local_unit_group](#get_trigger_actor_variable_local_unit_group) | 获取触发器LOCAL_UNIT_GROUP非数组 组变量 |
| [get_trigger_list_variable_local_unit_group](#get_trigger_list_variable_local_unit_group) | 获取全局触发器LOCAL_UNIT_GROUP数组变量子项 |
| [get_trigger_list_actor_variable_local_unit_group](#get_trigger_list_actor_variable_local_unit_group) | 获取触发器LOCAL_UNIT_GROUP数组 组变量子项 |
| [get_trigger_list_variable_all_local_unit_group](#get_trigger_list_variable_all_local_unit_group) | 获取全局触发器LOCAL_UNIT_GROUP数组变量 |
| [get_trigger_list_actor_variable_all_local_unit_group](#get_trigger_list_actor_variable_all_local_unit_group) | 获取触发器LOCAL_UNIT_GROUP 组变量数组 |
| [get_trigger_variable_deco_entity](#get_trigger_variable_deco_entity) | 获取全局触发器DECO_ENTITY非数组变量 |
| [get_trigger_actor_variable_deco_entity](#get_trigger_actor_variable_deco_entity) | 获取触发器DECO_ENTITY非数组 组变量 |
| [get_trigger_list_variable_deco_entity](#get_trigger_list_variable_deco_entity) | 获取全局触发器DECO_ENTITY数组变量子项 |
| [get_trigger_list_actor_variable_deco_entity](#get_trigger_list_actor_variable_deco_entity) | 获取触发器DECO_ENTITY数组 组变量子项 |
| [get_trigger_list_variable_all_deco_entity](#get_trigger_list_variable_all_deco_entity) | 获取全局触发器DECO_ENTITY数组变量 |
| [get_trigger_list_actor_variable_all_deco_entity](#get_trigger_list_actor_variable_all_deco_entity) | 获取触发器DECO_ENTITY 组变量数组 |
| [get_trigger_variable_scene_preset](#get_trigger_variable_scene_preset) | 获取全局触发器SCENE_PRESET非数组变量 |
| [get_trigger_actor_variable_scene_preset](#get_trigger_actor_variable_scene_preset) | 获取触发器SCENE_PRESET非数组 组变量 |
| [get_trigger_list_variable_scene_preset](#get_trigger_list_variable_scene_preset) | 获取全局触发器SCENE_PRESET数组变量子项 |
| [get_trigger_list_actor_variable_scene_preset](#get_trigger_list_actor_variable_scene_preset) | 获取触发器SCENE_PRESET数组 组变量子项 |
| [get_trigger_list_variable_all_scene_preset](#get_trigger_list_variable_all_scene_preset) | 获取全局触发器SCENE_PRESET数组变量 |
| [get_trigger_list_actor_variable_all_scene_preset](#get_trigger_list_actor_variable_all_scene_preset) | 获取触发器SCENE_PRESET 组变量数组 |
| [get_trigger_variable_item_stack_type](#get_trigger_variable_item_stack_type) | 获取全局触发器ITEM_STACK_TYPE非数组变量 |
| [get_trigger_actor_variable_item_stack_type](#get_trigger_actor_variable_item_stack_type) | 获取触发器ITEM_STACK_TYPE非数组 组变量 |
| [get_trigger_list_variable_item_stack_type](#get_trigger_list_variable_item_stack_type) | 获取全局触发器ITEM_STACK_TYPE数组变量子项 |
| [get_trigger_list_actor_variable_item_stack_type](#get_trigger_list_actor_variable_item_stack_type) | 获取触发器ITEM_STACK_TYPE数组 组变量子项 |
| [get_trigger_list_variable_all_item_stack_type](#get_trigger_list_variable_all_item_stack_type) | 获取全局触发器ITEM_STACK_TYPE数组变量 |
| [get_trigger_list_actor_variable_all_item_stack_type](#get_trigger_list_actor_variable_all_item_stack_type) | 获取触发器ITEM_STACK_TYPE 组变量数组 |
| [get_trigger_variable_ability_release_id](#get_trigger_variable_ability_release_id) | 获取全局触发器ABILITY_RELEASE_ID非数组变量 |
| [get_trigger_actor_variable_ability_release_id](#get_trigger_actor_variable_ability_release_id) | 获取触发器ABILITY_RELEASE_ID非数组 组变量 |
| [get_trigger_list_variable_ability_release_id](#get_trigger_list_variable_ability_release_id) | 获取全局触发器ABILITY_RELEASE_ID数组变量子项 |
| [get_trigger_list_actor_variable_ability_release_id](#get_trigger_list_actor_variable_ability_release_id) | 获取触发器ABILITY_RELEASE_ID数组 组变量子项 |
| [get_trigger_list_variable_all_ability_release_id](#get_trigger_list_variable_all_ability_release_id) | 获取全局触发器ABILITY_RELEASE_ID数组变量 |
| [get_trigger_list_actor_variable_all_ability_release_id](#get_trigger_list_actor_variable_all_ability_release_id) | 获取触发器ABILITY_RELEASE_ID 组变量数组 |
| [get_trigger_variable_deco_name](#get_trigger_variable_deco_name) | 获取全局触发器DECO_NAME非数组变量 |
| [get_trigger_actor_variable_deco_name](#get_trigger_actor_variable_deco_name) | 获取触发器DECO_NAME非数组 组变量 |
| [get_trigger_list_variable_deco_name](#get_trigger_list_variable_deco_name) | 获取全局触发器DECO_NAME数组变量子项 |
| [get_trigger_list_actor_variable_deco_name](#get_trigger_list_actor_variable_deco_name) | 获取触发器DECO_NAME数组 组变量子项 |
| [get_trigger_list_variable_all_deco_name](#get_trigger_list_variable_all_deco_name) | 获取全局触发器DECO_NAME数组变量 |
| [get_trigger_list_actor_variable_all_deco_name](#get_trigger_list_actor_variable_all_deco_name) | 获取触发器DECO_NAME 组变量数组 |
| [get_trigger_variable_ui_point](#get_trigger_variable_ui_point) | 获取全局触发器UI_POINT非数组变量 |
| [get_trigger_actor_variable_ui_point](#get_trigger_actor_variable_ui_point) | 获取触发器UI_POINT非数组 组变量 |
| [get_trigger_list_variable_ui_point](#get_trigger_list_variable_ui_point) | 获取全局触发器UI_POINT数组变量子项 |
| [get_trigger_list_actor_variable_ui_point](#get_trigger_list_actor_variable_ui_point) | 获取触发器UI_POINT数组 组变量子项 |
| [get_trigger_list_variable_all_ui_point](#get_trigger_list_variable_all_ui_point) | 获取全局触发器UI_POINT数组变量 |
| [get_trigger_list_actor_variable_all_ui_point](#get_trigger_list_actor_variable_all_ui_point) | 获取触发器UI_POINT 组变量数组 |
| [get_trigger_variable_attach_model_entity](#get_trigger_variable_attach_model_entity) | 获取全局触发器ATTACH_MODEL_ENTITY非数组变量 |
| [get_trigger_actor_variable_attach_model_entity](#get_trigger_actor_variable_attach_model_entity) | 获取触发器ATTACH_MODEL_ENTITY非数组 组变量 |
| [get_trigger_list_variable_attach_model_entity](#get_trigger_list_variable_attach_model_entity) | 获取全局触发器ATTACH_MODEL_ENTITY数组变量子项 |
| [get_trigger_list_actor_variable_attach_model_entity](#get_trigger_list_actor_variable_attach_model_entity) | 获取触发器ATTACH_MODEL_ENTITY数组 组变量子项 |
| [get_trigger_list_variable_all_attach_model_entity](#get_trigger_list_variable_all_attach_model_entity) | 获取全局触发器ATTACH_MODEL_ENTITY数组变量 |
| [get_trigger_list_actor_variable_all_attach_model_entity](#get_trigger_list_actor_variable_all_attach_model_entity) | 获取触发器ATTACH_MODEL_ENTITY 组变量数组 |
| [get_trigger_variable_live2d](#get_trigger_variable_live2d) | 获取全局触发器LIVE2D非数组变量 |
| [get_trigger_actor_variable_live2d](#get_trigger_actor_variable_live2d) | 获取触发器LIVE2D非数组 组变量 |
| [get_trigger_list_variable_live2d](#get_trigger_list_variable_live2d) | 获取全局触发器LIVE2D数组变量子项 |
| [get_trigger_list_actor_variable_live2d](#get_trigger_list_actor_variable_live2d) | 获取触发器LIVE2D数组 组变量子项 |
| [get_trigger_list_variable_all_live2d](#get_trigger_list_variable_all_live2d) | 获取全局触发器LIVE2D数组变量 |
| [get_trigger_list_actor_variable_all_live2d](#get_trigger_list_actor_variable_all_live2d) | 获取触发器LIVE2D 组变量数组 |
| [get_trigger_variable_spine](#get_trigger_variable_spine) | 获取全局触发器SPINE非数组变量 |
| [get_trigger_actor_variable_spine](#get_trigger_actor_variable_spine) | 获取触发器SPINE非数组 组变量 |
| [get_trigger_list_variable_spine](#get_trigger_list_variable_spine) | 获取全局触发器SPINE数组变量子项 |
| [get_trigger_list_actor_variable_spine](#get_trigger_list_actor_variable_spine) | 获取触发器SPINE数组 组变量子项 |
| [get_trigger_list_variable_all_spine](#get_trigger_list_variable_all_spine) | 获取全局触发器SPINE数组变量 |
| [get_trigger_list_actor_variable_all_spine](#get_trigger_list_actor_variable_all_spine) | 获取触发器SPINE 组变量数组 |
| [get_trigger_variable_debug_shape](#get_trigger_variable_debug_shape) | 获取全局触发器DEBUG_SHAPE非数组变量 |
| [get_trigger_actor_variable_debug_shape](#get_trigger_actor_variable_debug_shape) | 获取触发器DEBUG_SHAPE非数组 组变量 |
| [get_trigger_list_variable_debug_shape](#get_trigger_list_variable_debug_shape) | 获取全局触发器DEBUG_SHAPE数组变量子项 |
| [get_trigger_list_actor_variable_debug_shape](#get_trigger_list_actor_variable_debug_shape) | 获取触发器DEBUG_SHAPE数组 组变量子项 |
| [get_trigger_list_variable_all_debug_shape](#get_trigger_list_variable_all_debug_shape) | 获取全局触发器DEBUG_SHAPE数组变量 |
| [get_trigger_list_actor_variable_all_debug_shape](#get_trigger_list_actor_variable_all_debug_shape) | 获取触发器DEBUG_SHAPE 组变量数组 |
| [get_trigger_variable_watching_mode_status](#get_trigger_variable_watching_mode_status) | 获取全局触发器WATCHING_MODE_STATUS非数组变量 |
| [get_trigger_actor_variable_watching_mode_status](#get_trigger_actor_variable_watching_mode_status) | 获取触发器WATCHING_MODE_STATUS非数组 组变量 |
| [get_trigger_list_variable_watching_mode_status](#get_trigger_list_variable_watching_mode_status) | 获取全局触发器WATCHING_MODE_STATUS数组变量子项 |
| [get_trigger_list_actor_variable_watching_mode_status](#get_trigger_list_actor_variable_watching_mode_status) | 获取触发器WATCHING_MODE_STATUS数组 组变量子项 |
| [get_trigger_list_variable_all_watching_mode_status](#get_trigger_list_variable_all_watching_mode_status) | 获取全局触发器WATCHING_MODE_STATUS数组变量 |
| [get_trigger_list_actor_variable_all_watching_mode_status](#get_trigger_list_actor_variable_all_watching_mode_status) | 获取触发器WATCHING_MODE_STATUS 组变量数组 |
| [get_trigger_variable_force_entity](#get_trigger_variable_force_entity) | 获取全局触发器FORCE_ENTITY非数组变量 |
| [get_trigger_actor_variable_force_entity](#get_trigger_actor_variable_force_entity) | 获取触发器FORCE_ENTITY非数组 组变量 |
| [get_trigger_list_variable_force_entity](#get_trigger_list_variable_force_entity) | 获取全局触发器FORCE_ENTITY数组变量子项 |
| [get_trigger_list_actor_variable_force_entity](#get_trigger_list_actor_variable_force_entity) | 获取触发器FORCE_ENTITY数组 组变量子项 |
| [get_trigger_list_variable_all_force_entity](#get_trigger_list_variable_all_force_entity) | 获取全局触发器FORCE_ENTITY数组变量 |
| [get_trigger_list_actor_variable_all_force_entity](#get_trigger_list_actor_variable_all_force_entity) | 获取触发器FORCE_ENTITY 组变量数组 |
| [get_trigger_variable_goods_key](#get_trigger_variable_goods_key) | 获取全局触发器GOODS_KEY非数组变量 |
| [get_trigger_actor_variable_goods_key](#get_trigger_actor_variable_goods_key) | 获取触发器GOODS_KEY非数组 组变量 |
| [get_trigger_list_variable_goods_key](#get_trigger_list_variable_goods_key) | 获取全局触发器GOODS_KEY数组变量子项 |
| [get_trigger_list_actor_variable_goods_key](#get_trigger_list_actor_variable_goods_key) | 获取触发器GOODS_KEY数组 组变量子项 |
| [get_trigger_list_variable_all_goods_key](#get_trigger_list_variable_all_goods_key) | 获取全局触发器GOODS_KEY数组变量 |

---

## set_player_sfx_switch

method in GameAPI

- 描述

    特效播放开关

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | switch | boolean | 开关 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_player_sfx_switch(player.handle, true)
```

---

## play_sfx_on_point

method in GameAPI

- 描述

    在某点播放特效

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.FVector3 | 点 |
    | sfx | py.SfxKey | 特效编号 |
    | scale | py.Fixed | 缩放 |
    | duratime | py.Fixed | 持续时间 |
    | offset | py.Fixed | 竖直方向偏移 |
    | role? | py.Role | 玩家 |
    | visible_type? | integer | 显示类型（1：全体，2：自己 3：仅自己和友方 4：非自己和友方 |
    | rotation? | py.Fixed | 初始旋转角度 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sfx | 特效 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))
local sfx_key = 134274569

local result = GameAPI.play_sfx_on_point(fvector3, sfx_key, Fix32(1), Fix32(1), Fix32(1), nil, 1, Fix32(1))
```

---

## create_link_sfx_from_unit_to_point

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
    | follow_scale? | boolean | 是否跟随单位缩放 |
    | show_in_fog? | boolean | 迷雾中显示 |
    | blend_with_fog? | boolean | 迷雾混合 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LinkSfx | 特效 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local sfx_key = 134274569
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

local result = GameAPI.create_link_sfx_from_unit_to_point(sfx_key, unit.handle, "source_socket", fvector3, Fix32(1), 1.0, true, true, true, true, true)
```

---

## create_link_sfx_from_unit_to_unit

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
    | follow_scale? | boolean | 是否跟随单位缩放 |
    | show_in_fog? | boolean | 迷雾中显示 |
    | blend_with_fog? | boolean | 迷雾混合 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LinkSfx | 特效 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local sfx_key = 134274569

local result = GameAPI.create_link_sfx_from_unit_to_unit(sfx_key, unit.handle, "source_socket", unit.handle, "target_socket", 1.0, true, true, true, true, true)
```

---

## create_link_sfx_from_point_to_unit

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

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LinkSfx | 特效 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local sfx_key = 134274569
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

local result = GameAPI.create_link_sfx_from_point_to_unit(sfx_key, fvector3, Fix32(1), unit.handle, "source_socket", 1.0, true, true, true, true)
```

---

## create_link_sfx_from_point_to_point

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

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LinkSfx | 特效 |

- 示例

```lua
local sfx_key = 134274569
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

local result = GameAPI.create_link_sfx_from_point_to_point(sfx_key, fvector3, Fix32(1), fvector3, Fix32(1), 1.0, true, true, true, true)
```

---

## set_link_sfx_point

method in GameAPI

- 描述

    设置闪电特效的位置点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | sfx_entity | py.LinkSfx | 特效 |
    | source_or_target | py.LinkSfxPointType | 起点/终点 |
    | point | py.Point | 点 |
    | height | number | 高度 |

- 返回值

    无

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)
local unit = y3.player.get_by_id(1):get_all_units()[1]
local link_sfx = GameAPI.create_link_sfx_from_unit_to_point(134274569, unit.handle, "origin", GlobalAPI.coord_to_point(Fix32(100), Fix32(100), Fix32(0)), Fix32(0))

GameAPI.set_link_sfx_point(link_sfx, 1, point, 1.0)
```

---

## set_link_sfx_unit_socket

method in GameAPI

- 描述

    设置闪电特效单位附加点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | sfx_entity | py.LinkSfx | 特效 |
    | source_or_target | py.LinkSfxPointType | 起点/终点 |
    | unit | py.Unit | 单位 |
    | socket | string | 单位挂接点 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local link_sfx = GameAPI.create_link_sfx_from_unit_to_point(134274569, unit.handle, "origin", GlobalAPI.coord_to_point(Fix32(100), Fix32(100), Fix32(0)), Fix32(0))

GameAPI.set_link_sfx_unit_socket(link_sfx, 1, unit.handle, "socket")
```

---

## remove_link_sfx

method in GameAPI

- 描述

    移除特效

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | sfx_entity | py.LinkSfx | 特效 |
    | immediately? | boolean | 立即移除表现 |
    | use_sys_d_destroy_way? | boolean | 特效删除的方式是否读表 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local link_sfx = GameAPI.create_link_sfx_from_unit_to_point(134274569, unit.handle, "origin", GlobalAPI.coord_to_point(Fix32(100), Fix32(100), Fix32(0)), Fix32(0))

GameAPI.remove_link_sfx(link_sfx, true, true)
```

---

## enable_link_sfx_show

method in GameAPI

- 描述

    设置特效是否显示

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | sfx_entity | py.LinkSfx | 特效 |
    | b_show | boolean | 是否显示 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local link_sfx = GameAPI.create_link_sfx_from_unit_to_point(134274569, unit.handle, "origin", GlobalAPI.coord_to_point(Fix32(100), Fix32(100), Fix32(0)), Fix32(0))

GameAPI.enable_link_sfx_show(link_sfx, true)
```

---

## enable_link_sfx_visible

method in GameAPI

- 描述

    设置链接特效

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | sfx_entity | py.LinkSfx | 特效 |
    | role | py.Role | 玩家 |
    | b_visible | boolean | 开关 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local unit = y3.player.get_by_id(1):get_all_units()[1]
local link_sfx = GameAPI.create_link_sfx_from_unit_to_point(134274569, unit.handle, "origin", GlobalAPI.coord_to_point(Fix32(100), Fix32(100), Fix32(0)), Fix32(0))

GameAPI.enable_link_sfx_visible(link_sfx, player.handle, true)
```

---

## enable_sfx_visible

method in GameAPI

- 描述

    设置特效

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | sfx_entity | py.Sfx | 特效 |
    | role | py.Role | 玩家 |
    | b_visible | boolean | 开关 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local sfx = y3.particle.create({ type = 134274569, target = y3.point(0, 0) }).handle

GameAPI.enable_sfx_visible(sfx, player.handle, true)
```

---

## create_sfx_on_point

method in GameAPI

- 描述

    创建特效到点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | sfx_id | py.SfxKey | 特效编号 |
    | point | py.Point | 点 |
    | face_angle | number | 面向角度 |
    | scale | number | 缩放比例 |
    | height | number | 高度 |
    | duration | number | 持续时间 |
    | immediately? | boolean | 是否立即删除 |
    | use_sys_d_destroy_way? | boolean | 特效删除的方式是否读表 |
    | show_in_fog? | boolean | 迷雾里显示 |
    | blend_with_fog? | boolean | 迷雾混合 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sfx | 特效 |

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)
local sfx_key = 134274569

local result = GameAPI.create_sfx_on_point(sfx_key, point, 1.0, 1.0, 1.0, 1.0, true, true, true, true)
```

---

## create_sfx_on_unit

method in GameAPI

- 描述

    创建特效到单位附加点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | sfx_id | py.SfxKey | 特效编号 |
    | unit | py.Unit | 单位 |
    | socket | string | 单位挂接点 |
    | b_follow_rotate | boolean | 是否跟随单位旋转 |
    | b_follow_scale | boolean | 是否跟随单位缩放 |
    | scale? | number | 缩放比例 |
    | duration? | number | 持续时间 |
    | angle? | number | 角度 |
    | immediately? | boolean | 是否立即删除 |
    | use_sys_d_destroy_way? | boolean | 特效删除的方式是否读表 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sfx | 特效 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local sfx_key = 134274569

local result = GameAPI.create_sfx_on_unit(sfx_key, unit.handle, "socket", true, true, 1.0, 1.0, 1.0, true, true)
```

---

## create_sfx_on_unit_new

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
    | scale? | number | 缩放比例 |
    | duration? | number | 持续时间 |
    | angle? | number | 角度 |
    | immediately? | boolean | 是否立即删除 |
    | use_sys_d_destroy_way? | boolean | 特效删除的方式是否读表 |
    | detach? | boolean | 是否脱离单位 |
    | show_in_fog? | boolean | 迷雾里显示 |
    | blend_with_fog? | boolean | 迷雾混合 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sfx | 特效 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local sfx_key = 134274569

local result = GameAPI.create_sfx_on_unit_new(sfx_key, unit.handle, "socket", 1, true, 1.0, 1.0, 1.0, true, true, true, true, true)
```

---

## delete_sfx

method in GameAPI

- 描述

    删除特效

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | sfx_entity? | py.Sfx | 特效 |
    | immediately? | boolean | 立即移除表现 |
    | use_sys_d? | boolean | 删除时是否读取系统默认特效 |

- 返回值

    无

- 示例

```lua
local sfx = y3.particle.create({ type = 134274569, target = y3.point(0, 0) }).handle

GameAPI.delete_sfx(nil, true, true)
```

---

## set_sfx_rotate

method in GameAPI

- 描述

    设置特效旋转

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | sfx_entity | py.Sfx | 特效 |
    | rotate_x | number | x轴旋转 |
    | rotate_y | number | y轴旋转 |
    | rotate_z | number | z轴旋转 |

- 返回值

    无

- 示例

```lua
local sfx = y3.particle.create({ type = 134274569, target = y3.point(0, 0) }).handle

GameAPI.set_sfx_rotate(sfx, 1.0, 1.0, 1.0)
```

---

## set_sfx_angle

method in GameAPI

- 描述

    设置特效朝向

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | sfx_entity | py.Sfx | 特效 |
    | face_angle | number | 朝向 |

- 返回值

    无

- 示例

```lua
local sfx = y3.particle.create({ type = 134274569, target = y3.point(0, 0) }).handle

GameAPI.set_sfx_angle(sfx, 1.0)
```

---

## set_sfx_color

method in GameAPI

- 描述

    设置特效颜色

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | sfx_entity | py.Sfx | 特效 |
    | x | number | x |
    | y | number | y |
    | z | number | z |
    | w | number | w |

- 返回值

    无

- 示例

```lua
local sfx = y3.particle.create({ type = 134274569, target = y3.point(0, 0) }).handle

GameAPI.set_sfx_color(sfx, 1.0, 1.0, 1.0, 1.0)
```

---

## set_sfx_scale

method in GameAPI

- 描述

    设置特效缩放

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | sfx_entity | py.Sfx | 特效 |
    | scale_x | number | x轴缩放 |
    | scale_y | number | y轴缩放 |
    | scale_z | number | z轴缩放 |
    | duration? | number | 过渡时间 |

- 返回值

    无

- 示例

```lua
local sfx = y3.particle.create({ type = 134274569, target = y3.point(0, 0) }).handle

GameAPI.set_sfx_scale(sfx, 1.0, 1.0, 1.0, 1.0)
```

---

## set_sfx_height

method in GameAPI

- 描述

    设置特效高度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | sfx_entity | py.Sfx | 特效 |
    | height | number | 高度 |

- 返回值

    无

- 示例

```lua
local sfx = y3.particle.create({ type = 134274569, target = y3.point(0, 0) }).handle

GameAPI.set_sfx_height(sfx, 1.0)
```

---

## set_sfx_position

method in GameAPI

- 描述

    设置特效到点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | sfx_entity | py.Sfx | 特效 |
    | point | py.Point | 点 |
    | fluent_move? | boolean | 平滑移动 |

- 返回值

    无

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)
local sfx = y3.particle.create({ type = 134274569, target = y3.point(0, 0) }).handle

GameAPI.set_sfx_position(sfx, point, true)
```

---

## set_sfx_animation_speed

method in GameAPI

- 描述

    设置特效动画速度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | sfx_entity | py.Sfx | 特效 |
    | speed | number | 动画速度 |

- 返回值

    无

- 示例

```lua
local sfx = y3.particle.create({ type = 134274569, target = y3.point(0, 0) }).handle

GameAPI.set_sfx_animation_speed(sfx, 1.0)
```

---

## set_sfx_duration

method in GameAPI

- 描述

    设置特效持续时间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | sfx_entity | py.Sfx | 特效 |
    | duration | number | 持续时间 |

- 返回值

    无

- 示例

```lua
local sfx = y3.particle.create({ type = 134274569, target = y3.point(0, 0) }).handle

GameAPI.set_sfx_duration(sfx, 1.0)
```

---

## add_sfx_to_camera

method in GameAPI

- 描述

    播放屏幕特效

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | sfx_key | py.SfxKey | 特效编号 |
    | keep_time | number | 持续时间 |
    | role? | py.Role | 玩家 |
    | render_after_post? | boolean | 是否后处理之后渲染 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local sfx_key = 134274569

GameAPI.add_sfx_to_camera(sfx_key, 1.0, nil, true)
```

---

## add_sfx_to_camera_with_return

method in GameAPI

- 描述

    播放屏幕特效并返回特效实体

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | sfx_key | py.SfxKey | 特效编号 |
    | keep_time | number | 持续时间 |
    | role? | py.Role | 玩家 |
    | render_after_post? | boolean | 是否后处理之后渲染 |
    | immediately? | boolean | 是否立即删除 |
    | use_sys_d_destroy_way? | boolean | 特效删除的方式是否读表 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sfx | 特效 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local sfx_key = 134274569

local result = GameAPI.add_sfx_to_camera_with_return(sfx_key, 1.0, nil, true, true, true)
```

---

## start_shake

method in GameAPI

- 描述

    震动屏幕

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | period | number | 震动周期 |
    | amplitude_vector | py.FVector3 | 振幅大小 |
    | increase_vector | py.FVector3 | 增幅值 |
    | keep_time | number | 震动持续时间 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

GameAPI.start_shake(player.handle, 1.0, fvector3, fvector3, 1.0)
```

---

## link_sfx_key_to_str

method in GameAPI

- 描述

    链接特效路径转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | val | py.SfxKey | 特效编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local sfx_key = 134274569

local result = GameAPI.link_sfx_key_to_str(sfx_key)
```

---

## str_to_link_sfx_key

method in GameAPI

- 描述

    字符串转链接特效路径

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | val | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SfxKey | 特效编号 |

- 示例

```lua
local result = GameAPI.str_to_link_sfx_key("val")
```

---

## sfx_to_str

method in GameAPI

- 描述

    特效转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | py.Sfx | 特效 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local sfx = y3.particle.create({ type = 134274569, target = y3.point(0, 0) }).handle

local result = GameAPI.sfx_to_str(sfx)
```

---

## particle_sfx_key_to_str

method in GameAPI

- 描述

    粒子特效路径转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | val | py.SfxKey | 特效编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local sfx_key = 134274569

local result = GameAPI.particle_sfx_key_to_str(sfx_key)
```

---

## str_to_particle_sfx_key

method in GameAPI

- 描述

    字符串转粒子特效路径

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | val | string | 特效编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SfxKey | 特效编号 |

- 示例

```lua
local result = GameAPI.str_to_particle_sfx_key("val")
```

---

## link_sfx_to_str

method in GameAPI

- 描述

    链接特效转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | py.LinkSfx | 链接特效 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local link_sfx = GameAPI.create_link_sfx_from_unit_to_point(134274569, unit.handle, "origin", GlobalAPI.coord_to_point(Fix32(100), Fix32(100), Fix32(0)), Fix32(0))

local result = GameAPI.link_sfx_to_str(link_sfx)
```

---

## get_table

method in GameAPI

- 描述

    get_table

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | table_name | string | table_name |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Table | table |

- 示例

```lua
local result = GameAPI.get_table("table_name")
```

---

## set_table_value

method in GameAPI

- 描述

    set_table_value

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | table | py.Table | table |
    | value | py.Actor | value |
    | key1 | string | key1 |
    | key2 | string | key2 |
    | key3 | string | key3 |
    | key4 | string | key4 |
    | key5 | string | key5 |
    | value_convert_func | string | value_convert_func |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local tbl = {}

GameAPI.set_table_value(tbl, actor, "key1", "key2", "key3", "key4", "key5", "value_convert_func")
```

---

## table_has_key

method in GameAPI

- 描述

    table_has_key

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | table | py.Table | table |
    | key | string | key |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | bool |

- 示例

```lua
local tbl = {}

local result = GameAPI.table_has_key(tbl, "key")
```

---

## get_table_var

method in GameAPI

- 描述

    get_table_var

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | table | py.Table | table |
    | key1 | string | key1 |
    | key2 | string | key2 |
    | key3 | string | key3 |
    | key4 | string | key4 |
    | key5 | string | key5 |
    | default_value | py.Actor | default |
    | value_convert_func | string | value_convert_func |
    | extra_info? | py.Dict | extra_info(for debug) |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Actor | value |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local tbl = {}
local dict = pydict()

local result = GameAPI.get_table_var(tbl, "key1", "key2", "key3", "key4", "key5", actor, "value_convert_func")
```

---

## remove_table_value

method in GameAPI

- 描述

    remove_table_value

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | table | py.Table | table |
    | key1 | string | key1 |
    | key2 | string | key2 |
    | key3 | string | key3 |
    | key4 | string | key4 |
    | key5 | string | key5 |

- 返回值

    无

- 示例

```lua
local tbl = {}

GameAPI.remove_table_value(tbl, "key1", "key2", "key3", "key4", "key5")
```

---

## remove_table_value_n

method in GameAPI

- 描述

    remove_table_value_n

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | table | py.Table | table |
    | n | integer | N |

- 返回值

    无

- 示例

```lua
local tbl = {}

GameAPI.remove_table_value_n(tbl, 1)
```

---

## insert_table_value

method in GameAPI

- 描述

    insert_table_value

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | table | py.Table | table |
    | value | py.Actor | value |
    | value_convert_func | string | value_convert_func |
    | pos | integer | pos |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local tbl = {}

GameAPI.insert_table_value(tbl, actor, "value_convert_func", 1)
```

---

## get_new_table

method in GameAPI

- 描述

    get_new_table

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Table | table |

- 示例

```lua
local result = GameAPI.get_new_table()
```

---

## clear_table

method in GameAPI

- 描述

    clear_table

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | table | py.Table | table |

- 返回值

    无

- 示例

```lua
local tbl = {}

GameAPI.clear_table(tbl)
```

---

## encrypt_table

method in GameAPI

- 描述

    encrypt_table

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | table | py.Table | table |

- 返回值

    无

- 示例

```lua
local tbl = {}

GameAPI.encrypt_table(tbl)
```

---

## get_copy_of_table

method in GameAPI

- 描述

    get_copy_of_table

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | table | py.Table | table |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Table | table |

- 示例

```lua
local tbl = {}

local result = GameAPI.get_copy_of_table(tbl)
```

---

## dump_table

method in GameAPI

- 描述

    dump_table

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | table | py.Table | table |
    | extra_info? | py.DynamicTypeMeta | extra_info |

- 返回值

    无

- 示例

```lua
local tbl = {}
local dynamic_type = GameAPI.get_function_return_value("func_id", y3.player.get_by_id(1):get_all_units()[1].handle, pydict(), {}, 1)

GameAPI.dump_table(tbl)
```

---

## get_table_length

method in GameAPI

- 描述

    get_table_length

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | table | py.Table | table |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | length |

- 示例

```lua
local tbl = {}

local result = GameAPI.get_table_length(tbl)
```

---

## is_table_empty

method in GameAPI

- 描述

    表 - 是否为空表

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | table | py.Table | table |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否为空 |

- 示例

```lua
local tbl = {}

local result = GameAPI.is_table_empty(tbl)
```

---

## get_iter_table_value

method in GameAPI

- 描述

    get_iter_table_value_by_type

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item | py.List | table iter item |
    | default_value | py.Actor | default |
    | value_convert_func | string | value_convert_func |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Actor | value |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local list = {}

local result = GameAPI.get_iter_table_value(list, actor, "value_convert_func")
```

---

## table_iterator

method in GameAPI

- 描述

    table迭代器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | t | py.Table | TAB |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Iterator | Python迭代器 |

- 示例

```lua
local tbl = {}

local result = GameAPI.table_iterator(tbl)
```

---

## ordered_table_iterator

method in GameAPI

- 描述

    table迭代器（保序）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | t | py.Table | TAB |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Iterator | Python迭代器 |

- 示例

```lua
local tbl = {}

local result = GameAPI.ordered_table_iterator(tbl)
```

---

## table_iterator_new

method in GameAPI

- 描述

    table迭代器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | t | py.Table | TAB |
    | ordered? | boolean | 是否仅遍历数组部分（保序） |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Iterator | Python迭代器 |

- 示例

```lua
local tbl = {}

local result = GameAPI.table_iterator_new(tbl, true)
```

---

## unserialize_by_string

method in GameAPI

- 描述

    unserialize_by_string

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | archive_table_str | string | archive_table_str |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Table | table |

- 示例

```lua
local result = GameAPI.unserialize_by_string("archive_table_str")
```

---

## sort_table_by

method in GameAPI

- 描述

    sort_table_by

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | table | py.Table | table |
    | key | string | key |
    | order | py.TableOrder | order |
    | save_as? | py.Table | save_as |

- 返回值

    无

- 示例

```lua
local tbl = {}

GameAPI.sort_table_by(tbl, "key", 1)
```

---

## dbg_dialog_print_frame_timer_info

method in GameAPI

- 描述

    调试-Dialog窗口输出帧计时器信息

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | show_tasks | boolean | 显示任务 |

- 返回值

    无

- 示例

```lua
GameAPI.dbg_dialog_print_frame_timer_info(true)
```

---

## get_last_created_timer

method in GameAPI

- 描述

    获取最近创建的计时器

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Timer | 计时器 |

- 示例

```lua
local result = GameAPI.get_last_created_timer()
```

---

## start_timer

method in GameAPI

- 描述

    开启计时器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | name | string | 计时器名称 |
    | once | boolean | 是否单次 |
    | interval | py.Fixed | 时间 |
    | context | py.Dict | 上下文 |
    | desc | string | 描述 |

- 返回值

    无

- 示例

```lua
local dict = pydict()

GameAPI.start_timer("name", true, Fix32(1), dict, "desc")
```

---

## stop_timer

method in GameAPI

- 描述

    关闭计时器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | name | string | 计时器名称 |

- 返回值

    无

- 示例

```lua
GameAPI.stop_timer("name")
```

---

## run_lua_timer

method in GameAPI

- 描述

    开启计时器（新）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | time_delay | py.Fixed | 延迟时间 |
    | repeat_count | integer | 循环次数 |
    | run_at_start | boolean | 启动时立即运行 |
    | timer_callback | function | 回调函数 |
    | context | py.Dict | 上下文 |
    | desc | string | 描述 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Timer | 计时器编号 |

- 示例

```lua
local dict = pydict()

local result = GameAPI.run_lua_timer(Fix32(1), 1, true, function() end, dict, "desc")
```

---

## is_timer_valid

method in GameAPI

- 描述

    计时器是否正在运行

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | timer_id | py.Timer | 计时器编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否合法 |

- 示例

```lua
local timer = y3.timer.loop(1, function() end)

local result = GameAPI.is_timer_valid(timer.handle)
```

---

## delete_timer

method in GameAPI

- 描述

    删除计时器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | timer_id | py.Timer | 计时器编号 |

- 返回值

    无

- 示例

```lua
local timer = y3.timer.loop(1, function() end)

GameAPI.delete_timer(timer.handle)
```

---

## pause_timer

method in GameAPI

- 描述

    暂停计时器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | timer_id | py.Timer | 计时器编号 |

- 返回值

    无

- 示例

```lua
local timer = y3.timer.loop(1, function() end)

GameAPI.pause_timer(timer.handle)
```

---

## resume_timer

method in GameAPI

- 描述

    恢复计时器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | timer_id | py.Timer | 计时器编号 |

- 返回值

    无

- 示例

```lua
local timer = y3.timer.loop(1, function() end)

GameAPI.resume_timer(timer.handle)
```

---

## timer_set_left_count

method in GameAPI

- 描述

    设置计时器剩余次数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | timer_id | py.Timer | 计时器编号 |
    | count | integer | 剩余次数 |

- 返回值

    无

- 示例

```lua
local timer = y3.timer.loop(1, function() end)

GameAPI.timer_set_left_count(timer.handle, 1)
```

---

## timer_set_left_time

method in GameAPI

- 描述

    设置计时器剩余时间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | timer_id | py.Timer | 计时器编号 |
    | time | py.Fixed | 剩余时间 |

- 返回值

    无

- 示例

```lua
local timer = y3.timer.loop(1, function() end)

GameAPI.timer_set_left_time(timer.handle, Fix32(1))
```

---

## timer_set_interval_time

method in GameAPI

- 描述

    设置计时器间隔时间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | timer_id | py.Timer | 计时器编号 |
    | time | py.Fixed | 间隔时间 |

- 返回值

    无

- 示例

```lua
local timer = y3.timer.loop(1, function() end)

GameAPI.timer_set_interval_time(timer.handle, Fix32(1))
```

---

## timer_set_interval_frame

method in GameAPI

- 描述

    设置帧计时器间隔帧数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | timer_id | py.Timer | 计时器编号 |
    | frame | integer | 间隔帧数 |

- 返回值

    无

- 示例

```lua
local timer = y3.timer.loop(1, function() end)

GameAPI.timer_set_interval_frame(timer.handle, 1)
```

---

## get_timer_time_out_time

method in GameAPI

- 描述

    获取计时器设置的时间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | timer_id | py.Timer | 计时器 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 时间 |

- 示例

```lua
local timer = y3.timer.loop(1, function() end)

local result = GameAPI.get_timer_time_out_time(timer.handle)
```

---

## get_timer_elapsed_time

method in GameAPI

- 描述

    获取计时器经过的时间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | timer_id | py.Timer | 计时器 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 时间 |

- 示例

```lua
local timer = y3.timer.loop(1, function() end)

local result = GameAPI.get_timer_elapsed_time(timer.handle)
```

---

## get_timer_remaining_time

method in GameAPI

- 描述

    获取计时器剩余时间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | timer_id | py.Timer | 计时器 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 时间 |

- 示例

```lua
local timer = y3.timer.loop(1, function() end)

local result = GameAPI.get_timer_remaining_time(timer.handle)
```

---

## get_timer_init_count

method in GameAPI

- 描述

    获取计时器初始计数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | timer_id | py.Timer | 计时器 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 次数 |

- 示例

```lua
local timer = y3.timer.loop(1, function() end)

local result = GameAPI.get_timer_init_count(timer.handle)
```

---

## get_timer_remaining_count

method in GameAPI

- 描述

    获取计时器剩余计数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | timer_id | py.Timer | 计时器 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 次数 |

- 示例

```lua
local timer = y3.timer.loop(1, function() end)

local result = GameAPI.get_timer_remaining_count(timer.handle)
```

---

## get_actor_timer_run_time

method in GameAPI

- 描述

    获取独立计时器当前计时秒数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | name | string | 倒计时名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 计时秒数 |

- 示例

```lua
local result = GameAPI.get_actor_timer_run_time("name")
```

---

## get_current_expired_timer

method in GameAPI

- 描述

    获取当前到期的计时器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | timer_id | py.Timer | 计时器 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Timer | 计时器 |

- 示例

```lua
local timer = y3.timer.loop(1, function() end)

local result = GameAPI.get_current_expired_timer(timer.handle)
```

---

## timer_is_exist

method in GameAPI

- 描述

    计时器是否存在

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | timer_id | py.Timer | 计时器编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否合法 |

- 示例

```lua
local timer = y3.timer.loop(1, function() end)

local result = GameAPI.timer_is_exist(timer.handle)
```

---

## add_timer

method in GameAPI

- 描述

    添加定时回调

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | interval | py.Fixed | 间隔时间 |
    | is_repeat | boolean | 是否重复 |
    | func | function | 回调 |
    | desc? | string | 描述 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | timer_id |

- 示例

```lua
local result = GameAPI.add_timer(Fix32(1), true, function() end, "desc")
```

---

## cancel_timer

method in GameAPI

- 描述

    取消定时回调

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | timer_id | integer | timer_id |

- 返回值

    无

- 示例

```lua
GameAPI.cancel_timer(1)
```

---

## get_cur_day_and_night_time

method in GameAPI

- 描述

    游戏当前昼夜时间

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 时间 |

- 示例

```lua
local result = GameAPI.get_cur_day_and_night_time()
```

---

## set_day_and_night_time

method in GameAPI

- 描述

    设置昼夜游戏时间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | time | py.Fixed | 时间（0-24） |

- 返回值

    无

- 示例

```lua
GameAPI.set_day_and_night_time(Fix32(1))
```

---

## set_day_and_night_time_speed

method in GameAPI

- 描述

    设置昼夜游戏时间的流逝速度（倍数）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | time_multiple | py.Fixed | 倍数，非负数 |

- 返回值

    无

- 示例

```lua
GameAPI.set_day_and_night_time_speed(Fix32(1))
```

---

## set_day_and_night_time_speed_per

method in GameAPI

- 描述

    设置昼夜游戏时间的流逝速度（百分比）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | time_per | py.Fixed | 百分比，非负数 |

- 返回值

    无

- 示例

```lua
GameAPI.set_day_and_night_time_speed_per(Fix32(1))
```

---

## open_or_close_time_speed

method in GameAPI

- 描述

    打开/关闭时间流逝

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | flag | boolean | 布尔值 |

- 返回值

    无

- 示例

```lua
GameAPI.open_or_close_time_speed(true)
```

---

## create_day_and_night_human_time

method in GameAPI

- 描述

    创建人造时间，并持续一段时间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | create_time | py.Fixed | 创建的时间 |
    | time_delay | py.Fixed | 持续的时间 |

- 返回值

    无

- 示例

```lua
GameAPI.create_day_and_night_human_time(Fix32(1), Fix32(1))
```

---

## get_points_angle

method in GameAPI

- 描述

    点与点的角度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | p1 | py.Point | 点 |
    | p2 | py.Point | 目标点 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 角度 |

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)

local result = GameAPI.get_points_angle(point, point)
```

---

## get_points_dis

method in GameAPI

- 描述

    点与点的距离

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | p1 | py.Point | 点 |
    | p2 | py.Point | 目标点 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 距离 |

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)

local result = GameAPI.get_points_dis(point, point)
```

---

## get_point_ground_height

method in GameAPI

- 描述

    获取当前点的地面高度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.Point | 点 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 地面高度 |

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)

local result = GameAPI.get_point_ground_height(point)
```

---

## get_point_ground_collision

method in GameAPI

- 描述

    获取当前点的碰撞类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.Point | 点 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 碰撞类型 |

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)

local result = GameAPI.get_point_ground_collision(point)
```

---

## get_point_view_block_type

method in GameAPI

- 描述

    获取当前点的视野隔断类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.Point | 点 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 隔断类型 |

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)

local result = GameAPI.get_point_view_block_type(point)
```

---

## judge_point_in_area

method in GameAPI

- 描述

    判断点是否在区域内

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.FVector3 | 点 |
    | area | py.Area | 区域 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 点是否在区域中 |

- 示例

```lua
local area = y3.area.create_circle_area(y3.point.create(0, 0, 0), 500)
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

local result = GameAPI.judge_point_in_area(fvector3, area.handle)
```

---

## judge_point_in_rec

method in GameAPI

- 描述

    判断点是否在正方形内

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.FVector3 | 点 |
    | center | py.FVector3 | 中心点 |
    | width | py.Fixed | 正方形边长 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 点是否在正方形中 |

- 示例

```lua
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

local result = GameAPI.judge_point_in_rec(fvector3, fvector3, Fix32(1))
```

---

## add_area_tag

method in GameAPI

- 描述

    给区域添加tag

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.Area | 区域 |
    | tag | string | tag |

- 返回值

    无

- 示例

```lua
local area = y3.area.create_circle_area(y3.point.create(0, 0, 0), 500)

GameAPI.add_area_tag(area.handle, "tag")
```

---

## remove_area_tag

method in GameAPI

- 描述

    给区域移除tag

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.Area | 区域 |
    | tag | string | tag |

- 返回值

    无

- 示例

```lua
local area = y3.area.create_circle_area(y3.point.create(0, 0, 0), 500)

GameAPI.remove_area_tag(area.handle, "tag")
```

---

## add_road_tag

method in GameAPI

- 描述

    给路径添加tag

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | road | py.Road | 路径 |
    | tag | string | tag |

- 返回值

    无

- 示例

```lua
local road = y3.road.get_road_by_res_id(1)

GameAPI.add_road_tag(road.handle, "tag")
```

---

## remove_road_tag

method in GameAPI

- 描述

    给路径移除tag

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | road | py.Road | 路径 |
    | tag | string | tag |

- 返回值

    无

- 示例

```lua
local road = y3.road.get_road_by_res_id(1)

GameAPI.remove_road_tag(road.handle, "tag")
```

---

## if_cir_area_has_tag

method in GameAPI

- 描述

    圆形区域是否拥有某tags

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

local result = GameAPI.if_cir_area_has_tag(area.handle, "tag")
```

---

## if_rect_area_has_tag

method in GameAPI

- 描述

    矩形区域是否拥有某tags

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

local result = GameAPI.if_rect_area_has_tag(area.handle, "tag")
```

---

## if_road_has_tag

method in GameAPI

- 描述

    路径是否拥有某tags

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | road | py.Road | 路径 |
    | tag | string | tag |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 布尔值 |

- 示例

```lua
local road = y3.road.get_road_by_res_id(1)

local result = GameAPI.if_road_has_tag(road.handle, "tag")
```

---

## get_cir_areas_by_tag

method in GameAPI

- 描述

    根据tag获取对应的圆形区域

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
local result = GameAPI.get_cir_areas_by_tag("tag")
```

---

## get_rect_areas_by_tag

method in GameAPI

- 描述

    根据tag获取对应的矩形区域

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
local result = GameAPI.get_rect_areas_by_tag("tag")
```

---

## get_polygon_areas_by_tag

method in GameAPI

- 描述

    根据tag获取对应的不规则区域

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
local result = GameAPI.get_polygon_areas_by_tag("tag")
```

---

## get_roads_by_tag

method in GameAPI

- 描述

    根据tag获取对应的路径

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
local result = GameAPI.get_roads_by_tag("tag")
```

---

## get_poly_area_point_list

method in GameAPI

- 描述

    获取不规则区域顶点列表

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | poly_area | py.PolyArea | 不规则区域 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 顶点列表 |

- 示例

```lua
local poly_area = GameAPI.create_polygon_area(Fix32Vec3(0, 0, 0), Fix32Vec3(100, 0, 0), Fix32Vec3(100, 100, 0))

local result = GameAPI.get_poly_area_point_list(poly_area)
```

---

## get_point_by_road_point

method in GameAPI

- 描述

    通过路点返回点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | road_point | py.DynamicTypeMeta | 路点 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3 | 点 |

- 示例

```lua
local dynamic_type = GameAPI.get_function_return_value("func_id", y3.player.get_by_id(1):get_all_units()[1].handle, pydict(), {}, 1)

local result = GameAPI.get_point_by_road_point(dynamic_type)
```

---

## create_new_rec_area

method in GameAPI

- 描述

    创建矩形区域

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.FVector3 | 左下方起始点 |
    | width | py.Fixed | 宽 |
    | height | py.Fixed | 高 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RecArea | 矩形区域 |

- 示例

```lua
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

local result = GameAPI.create_new_rec_area(fvector3, Fix32(1), Fix32(1))
```

---

## create_rect_area_by_center

method in GameAPI

- 描述

    创建矩形区域

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | center | py.FVector3 | 中心点 |
    | width | py.Fixed | 宽 |
    | height | py.Fixed | 高 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RecArea | 矩形区域 |

- 示例

```lua
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

local result = GameAPI.create_rect_area_by_center(fvector3, Fix32(1), Fix32(1))
```

---

## create_rec_area_from_two_points

method in GameAPI

- 描述

    创建矩形区域

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point_begin | py.Point | 起始点 |
    | point_end | py.Point | 终点 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RecArea | 矩形区域 |

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)

local result = GameAPI.create_rec_area_from_two_points(point, point)
```

---

## create_new_cir_area

method in GameAPI

- 描述

    创建圆形区域

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.FVector3 | 中心点 |
    | radius | py.Fixed | 半径 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CirArea | 圆形区域 |

- 示例

```lua
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

local result = GameAPI.create_new_cir_area(fvector3, Fix32(1))
```

---

## create_polygon_area

method in GameAPI

- 描述

    创建多边形区域

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point0 | py.Point | 点 |
    | point1 | py.Point | 点 |
    | point2 | py.Point | 点 |
    | point3? | py.Point | 点 |
    | point4? | py.Point | 点 |
    | point5? | py.Point | 点 |
    | point6? | py.Point | 点 |
    | point7? | py.Point | 点 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PolyArea | 多边形区域 |

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)

local result = GameAPI.create_polygon_area(point, point, point)
```

---

## create_polygon_area_new

method in GameAPI

- 描述

    创建多边形区域(新)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point0 | py.Point | 点 |
    | point1 | py.Point | 点 |
    | point2 | py.Point | 点 |
    | point3? | py.Point | 点 |
    | point4? | py.Point | 点 |
    | point5? | py.Point | 点 |
    | point6? | py.Point | 点 |
    | point7? | py.Point | 点 |
    | point8? | py.Point | 点 |
    | point9? | py.Point | 点 |
    | point10? | py.Point | 点 |
    | point11? | py.Point | 点 |
    | point12? | py.Point | 点 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PolyArea | 多边形区域 |

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)

local result = GameAPI.create_polygon_area_new(point, point, point)
```

---

## set_cir_area_radius

method in GameAPI

- 描述

    设置圆形区域大小

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.CirArea | 圆形区域 |
    | radius | py.Fixed | 半径 |

- 返回值

    无

- 示例

```lua
local cir_area = GameAPI.create_new_cir_area(GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0)), Fix32(100))

GameAPI.set_cir_area_radius(cir_area, Fix32(1))
```

---

## get_circle_area_radius

method in GameAPI

- 描述

    获取圆形区域半径

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.CirArea | 圆形区域 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 半径 |

- 示例

```lua
local cir_area = GameAPI.create_new_cir_area(GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0)), Fix32(100))

local result = GameAPI.get_circle_area_radius(cir_area)
```

---

## get_circle_area_min_x

method in GameAPI

- 描述

    获取圆形区域内最小X坐标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.CirArea | 圆形区域 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 最小的X坐标 |

- 示例

```lua
local cir_area = GameAPI.create_new_cir_area(GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0)), Fix32(100))

local result = GameAPI.get_circle_area_min_x(cir_area)
```

---

## get_circle_area_min_y

method in GameAPI

- 描述

    获取圆形区域内最小y坐标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.CirArea | 圆形区域 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 最小的Y坐标 |

- 示例

```lua
local cir_area = GameAPI.create_new_cir_area(GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0)), Fix32(100))

local result = GameAPI.get_circle_area_min_y(cir_area)
```

---

## get_circle_area_max_x

method in GameAPI

- 描述

    获取圆形区域内最大X坐标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.CirArea | 圆形区域 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 最大的X坐标 |

- 示例

```lua
local cir_area = GameAPI.create_new_cir_area(GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0)), Fix32(100))

local result = GameAPI.get_circle_area_max_x(cir_area)
```

---

## get_circle_area_max_y

method in GameAPI

- 描述

    获取圆形区域内最大y坐标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.CirArea | 圆形区域 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 最大的Y坐标 |

- 示例

```lua
local cir_area = GameAPI.create_new_cir_area(GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0)), Fix32(100))

local result = GameAPI.get_circle_area_max_y(cir_area)
```

---

## set_rect_area_radius

method in GameAPI

- 描述

    设置矩形区域大小

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.RecArea | 矩形区域 |
    | length | py.Fixed | 长 |
    | width | py.Fixed | 宽 |

- 返回值

    无

- 示例

```lua
local rec_area = GameAPI.create_rec_area_from_two_points(Fix32Vec3(0, 0, 0), Fix32Vec3(100, 100, 0))

GameAPI.set_rect_area_radius(rec_area, Fix32(1), Fix32(1))
```

---

## get_rect_area_min_x

method in GameAPI

- 描述

    获取矩形区域内最小X坐标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.RecArea | 矩形区域 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 最小的X坐标 |

- 示例

```lua
local rec_area = GameAPI.create_rec_area_from_two_points(Fix32Vec3(0, 0, 0), Fix32Vec3(100, 100, 0))

local result = GameAPI.get_rect_area_min_x(rec_area)
```

---

## get_rect_area_min_y

method in GameAPI

- 描述

    获取矩形区域内最小Y坐标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.RecArea | 矩形区域 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 最小的Y坐标 |

- 示例

```lua
local rec_area = GameAPI.create_rec_area_from_two_points(Fix32Vec3(0, 0, 0), Fix32Vec3(100, 100, 0))

local result = GameAPI.get_rect_area_min_y(rec_area)
```

---

## get_rect_area_max_x

method in GameAPI

- 描述

    获取矩形区域内最大X坐标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.RecArea | 矩形区域 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 最大的X坐标 |

- 示例

```lua
local rec_area = GameAPI.create_rec_area_from_two_points(Fix32Vec3(0, 0, 0), Fix32Vec3(100, 100, 0))

local result = GameAPI.get_rect_area_max_x(rec_area)
```

---

## get_rect_area_max_y

method in GameAPI

- 描述

    获取矩形区域内最大Y坐标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.RecArea | 矩形区域 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 最大的Y坐标 |

- 示例

```lua
local rec_area = GameAPI.create_rec_area_from_two_points(Fix32Vec3(0, 0, 0), Fix32Vec3(100, 100, 0))

local result = GameAPI.get_rect_area_max_y(rec_area)
```

---

## get_usable_map_range

method in GameAPI

- 描述

    获取可用地图范围

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RecArea | 区域 |

- 示例

```lua
local result = GameAPI.get_usable_map_range()
```

---

## get_rec_area_by_res_id

method in GameAPI

- 描述

    通过区域ID返回矩形区域

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | res_id | py.AreaID | 区域ID |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RecArea | 矩形区域 |

- 示例

```lua
local area_id = 1

local result = GameAPI.get_rec_area_by_res_id(area_id)
```

---

## get_circle_area_by_res_id

method in GameAPI

- 描述

    通过区域ID返回圆形区域

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | res_id | py.AreaID | 区域ID |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CirArea | 圆形区域 |

- 示例

```lua
local area_id = 1

local result = GameAPI.get_circle_area_by_res_id(area_id)
```

---

## get_polygon_area_by_res_id

method in GameAPI

- 描述

    通过区域ID返回自定义多边形区域

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | res_id | py.AreaID | 区域ID |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PolyArea | 多边形区域 |

- 示例

```lua
local area_id = 1

local result = GameAPI.get_polygon_area_by_res_id(area_id)
```

---

## get_rec_area_last_created

method in GameAPI

- 描述

    最近创建的矩形区域

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RecArea | 矩形区域 |

- 示例

```lua
local result = GameAPI.get_rec_area_last_created()
```

---

## judge_point_in_rec_area

method in GameAPI

- 描述

    点是否在矩形区域内

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.FPoint | 点 |
    | area | py.RecArea | 矩形区域 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 点是否在矩形区域内 |

- 示例

```lua
local fpoint = GameAPI.get_point_by_res_id(1)
local rec_area = GameAPI.create_rec_area_from_two_points(Fix32Vec3(0, 0, 0), Fix32Vec3(100, 100, 0))

local result = GameAPI.judge_point_in_rec_area(fpoint, rec_area)
```

---

## judge_point_in_cir_area

method in GameAPI

- 描述

    点是否在圆形区域内

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.FPoint | 点 |
    | area | py.CirArea | 圆形区域 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 点是否在圆形区域内 |

- 示例

```lua
local fpoint = GameAPI.get_point_by_res_id(1)
local cir_area = GameAPI.create_new_cir_area(GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0)), Fix32(100))

local result = GameAPI.judge_point_in_cir_area(fpoint, cir_area)
```

---

## judge_point_in_polygon_area

method in GameAPI

- 描述

    点是否在不规则区域内

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.FPoint | 点 |
    | area | py.CirArea | 不规则区域 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 点是否在不规则区域内 |

- 示例

```lua
local fpoint = GameAPI.get_point_by_res_id(1)
local cir_area = GameAPI.create_new_cir_area(GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0)), Fix32(100))

local result = GameAPI.judge_point_in_polygon_area(fpoint, cir_area)
```

---

## get_point_by_res_id

method in GameAPI

- 描述

    通过资源id返回点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | res_id | integer | 资源ID |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FPoint | 点 |

- 示例

```lua
local result = GameAPI.get_point_by_res_id(1)
```

---

## get_unit_num_in_area

method in GameAPI

- 描述

    获取区域内单位数量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.Area | 区域 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 单位数量 |

- 示例

```lua
local area = y3.area.create_circle_area(y3.point.create(0, 0, 0), 500)

local result = GameAPI.get_unit_num_in_area(area.handle)
```

---

## get_unit_num_in_rec_area

method in GameAPI

- 描述

    矩形区域内单位数量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.RecArea | 矩形区域 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 单位数量 |

- 示例

```lua
local rec_area = GameAPI.create_rec_area_from_two_points(Fix32Vec3(0, 0, 0), Fix32Vec3(100, 100, 0))

local result = GameAPI.get_unit_num_in_rec_area(rec_area)
```

---

## get_unit_num_in_cir_area

method in GameAPI

- 描述

    圆形区域内单位数量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.CirArea | 圆形区域 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 单位数量 |

- 示例

```lua
local cir_area = GameAPI.create_new_cir_area(GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0)), Fix32(100))

local result = GameAPI.get_unit_num_in_cir_area(cir_area)
```

---

## get_unit_num_in_poly_area

method in GameAPI

- 描述

    不规则区域内单位数量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.PolyArea | 不规则区域 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 单位数量 |

- 示例

```lua
local poly_area = GameAPI.create_polygon_area(Fix32Vec3(0, 0, 0), Fix32Vec3(100, 0, 0), Fix32Vec3(100, 100, 0))

local result = GameAPI.get_unit_num_in_poly_area(poly_area)
```

---

## get_unit_group_in_rec_area

method in GameAPI

- 描述

    矩形区域内所有未销毁单位单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.RecArea | 矩形区域 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitGroup | 单位组 |

- 示例

```lua
local rec_area = GameAPI.create_rec_area_from_two_points(Fix32Vec3(0, 0, 0), Fix32Vec3(100, 100, 0))

local result = GameAPI.get_unit_group_in_rec_area(rec_area)
```

---

## get_unit_group_in_cir_area

method in GameAPI

- 描述

    圆形区域内所有未销毁单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.CirArea | 圆形区域 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitGroup | 单位组 |

- 示例

```lua
local cir_area = GameAPI.create_new_cir_area(GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0)), Fix32(100))

local result = GameAPI.get_unit_group_in_cir_area(cir_area)
```

---

## get_unit_group_in_poly_area

method in GameAPI

- 描述

    不规则区域内所有未销毁单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.CirArea | 不规则区域 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitGroup | 单位组 |

- 示例

```lua
local cir_area = GameAPI.create_new_cir_area(GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0)), Fix32(100))

local result = GameAPI.get_unit_group_in_poly_area(cir_area)
```

---

## get_item_group_in_rec_area

method in GameAPI

- 描述

    矩形区域内所有物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.RecArea | 矩形区域 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemGroup | 物品组 |

- 示例

```lua
local rec_area = GameAPI.create_rec_area_from_two_points(Fix32Vec3(0, 0, 0), Fix32Vec3(100, 100, 0))

local result = GameAPI.get_item_group_in_rec_area(rec_area)
```

---

## get_item_group_in_cir_area

method in GameAPI

- 描述

    圆形区域内所有物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.CirArea | 圆形区域 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemGroup | 物品组 |

- 示例

```lua
local cir_area = GameAPI.create_new_cir_area(GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0)), Fix32(100))

local result = GameAPI.get_item_group_in_cir_area(cir_area)
```

---

## get_item_group_in_poly_area

method in GameAPI

- 描述

    不规则区域内所有物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.PolyArea | 不规则区域 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemGroup | 物品组 |

- 示例

```lua
local poly_area = GameAPI.create_polygon_area(Fix32Vec3(0, 0, 0), Fix32Vec3(100, 0, 0), Fix32Vec3(100, 100, 0))

local result = GameAPI.get_item_group_in_poly_area(poly_area)
```

---

## remove_area

method in GameAPI

- 描述

    删除区域

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.Area | 区域 |

- 返回值

    无

- 示例

```lua
local area = y3.area.create_circle_area(y3.point.create(0, 0, 0), 500)

GameAPI.remove_area(area.handle)
```

---

## get_area_weather

method in GameAPI

- 描述

    获得区域天气

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.Area | 区域 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 天气类型 |

- 示例

```lua
local area = y3.area.create_circle_area(y3.point.create(0, 0, 0), 500)

local result = GameAPI.get_area_weather(area.handle)
```

---

## update_area_weather

method in GameAPI

- 描述

    设置区域天气

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.Area | 区域 |
    | weather_type | integer | 天气类型 |

- 返回值

    无

- 示例

```lua
local area = y3.area.create_circle_area(y3.point.create(0, 0, 0), 500)

GameAPI.update_area_weather(area.handle, 1)
```

---

## set_point_collision

method in GameAPI

- 描述

    设置点碰撞

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.Point | 点 |
    | is_add | boolean | 添加/去除 |
    | ground_channel | boolean | 地面碰撞 |
    | air_channel | boolean | 飞行碰撞 |

- 返回值

    无

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)

GameAPI.set_point_collision(point, true, true, true)
```

---

## set_area_collision

method in GameAPI

- 描述

    设置区域碰撞

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.Area | 区域 |
    | is_add | boolean | 添加/去除 |
    | ground_channel | boolean | 地面碰撞 |
    | air_channel | boolean | 飞行碰撞 |

- 返回值

    无

- 示例

```lua
local area = y3.area.create_circle_area(y3.point.create(0, 0, 0), 500)

GameAPI.set_area_collision(area.handle, true, true, true)
```

---

## edit_area_collision

method in GameAPI

- 描述

    编辑区域碰撞

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.Area | 区域 |
    | collision_layer | integer | 碰撞类型 |
    | is_add | boolean | 添加/去除 |

- 返回值

    无

- 示例

```lua
local area = y3.area.create_circle_area(y3.point.create(0, 0, 0), 500)

GameAPI.edit_area_collision(area.handle, 1, true)
```

---

## edit_area_fov_block

method in GameAPI

- 描述

    编辑区域视野阻挡

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.Area | 区域 |
    | fov_block_type | integer | 视野阻挡类型 |
    | is_add | boolean | 添加/去除 |

- 返回值

    无

- 示例

```lua
local area = y3.area.create_circle_area(y3.point.create(0, 0, 0), 500)

GameAPI.edit_area_fov_block(area.handle, 1, true)
```

---

## get_area_resource_id

method in GameAPI

- 描述

    获取区域的场景ID

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.Area | 区域 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 场景ID |

- 示例

```lua
local area = y3.area.create_circle_area(y3.point.create(0, 0, 0), 500)

local result = GameAPI.get_area_resource_id(area.handle)
```

---

## get_road_resource_id

method in GameAPI

- 描述

    获取路径的场景ID

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | road | py.Road | 路径 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 场景ID |

- 示例

```lua
local road = y3.road.get_road_by_res_id(1)

local result = GameAPI.get_road_resource_id(road.handle)
```

---

## sound_entity_to_str

method in GameAPI

- 描述

    声音转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | py.SoundEntity | 声音对象 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local sound_entity = GameAPI.play_sound_for_player(player.handle, 134274569, false)

local result = GameAPI.sound_entity_to_str(sound_entity)
```

---

## audio_key_to_str

method in GameAPI

- 描述

    声音类型转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | py.AudioKey | 音效编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local audio_key = 134274569

local result = GameAPI.audio_key_to_str(audio_key)
```

---

## str_to_audio_key

method in GameAPI

- 描述

    字符串转声音类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AudioKey | 音效编号 |

- 示例

```lua
local result = GameAPI.str_to_audio_key("obj")
```

---

## reg_sound_area

method in GameAPI

- 描述

    注册区域的附近语音频道

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.Area | 区域 |

- 返回值

    无

- 示例

```lua
local area = y3.area.create_circle_area(y3.point.create(0, 0, 0), 500)

GameAPI.reg_sound_area(area.handle)
```

---

## unreg_sound_area

method in GameAPI

- 描述

    反注册区域的附近语音频道

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.Area | 区域 |

- 返回值

    无

- 示例

```lua
local area = y3.area.create_circle_area(y3.point.create(0, 0, 0), 500)

GameAPI.unreg_sound_area(area.handle)
```

---

## set_nearby_voice_mode

method in GameAPI

- 描述

    设置附近语音的区域模式开关

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | b | boolean | 区域模式开关 |

- 返回值

    无

- 示例

```lua
GameAPI.set_nearby_voice_mode(true)
```

---

## set_audio_chat_channel

method in GameAPI

- 描述

    设置玩家发言频道

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | channel | integer | 频道 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_audio_chat_channel(player.handle, 1)
```

---

## play_sound_for_player

method in GameAPI

- 描述

    播放音乐

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | sid | py.AudioKey | 乐曲编号 |
    | loop | boolean | 是否循环 |
    | fade_in_time? | number | 淡入时间 |
    | fade_out_time? | number | 淡出时间 |
    | volume? | integer | 音量 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SoundEntity | 声音对象 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local audio_key = 134274569

local result = GameAPI.play_sound_for_player(player.handle, audio_key, true, 1.0, 1.0, 1)
```

---

## play_sound_for_role_relation

method in GameAPI

- 描述

    对目标播放音乐

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | camp_target | py.RoleRelation | 玩家关系 |
    | sid | py.AudioKey | 乐曲编号 |
    | loop | boolean | 是否循环 |

- 返回值

    无

- 示例

```lua
local unit_key = 134274569
local relation = 1
local audio_key = 134274569

GameAPI.play_sound_for_role_relation(unit_key, relation, audio_key, true)
```

---

## play_3d_sound_for_player

method in GameAPI

- 描述

    播放3d音乐

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | sid | py.AudioKey | 乐曲编号 |
    | position | py.Point | 播放位置 |
    | height | number | 高度 |
    | fade_in_time? | number | 淡入时间 |
    | fade_out_time? | number | 淡出时间 |
    | ensure_play? | boolean | 确保播放 |
    | loop? | boolean | 是否循环 |
    | volume? | integer | 音量 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SoundEntity | 声音对象 |

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)
local player = y3.player.get_by_id(1)
local audio_key = 134274569

local result = GameAPI.play_3d_sound_for_player(player.handle, audio_key, point, 1.0, 1.0, 1.0, true, true, 1)
```

---

## follow_object_play_3d_sound_for_player

method in GameAPI

- 描述

    跟随单位播放3d音乐

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | sid | py.AudioKey | 乐曲编号 |
    | unit | py.Unit | 单位 |
    | fade_in_time? | number | 淡入时间 |
    | fade_out_time? | number | 淡出时间 |
    | ensure_play? | boolean | 确保播放 |
    | loop? | boolean | 是否循环 |
    | offset_x? | number | 偏移x |
    | offset_y? | number | 偏移y |
    | offset_z? | number | 偏移z |
    | volume? | integer | 音量 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SoundEntity | 声音对象 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)
local audio_key = 134274569

local result = GameAPI.follow_object_play_3d_sound_for_player(player.handle, audio_key, unit.handle, 1.0, 1.0, true, true, 1.0, 1.0, 1.0, 1)
```

---

## stop_sound

method in GameAPI

- 描述

    停止播放音乐

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | sound | py.SoundEntity | 声音 |
    | immediately_stop? | boolean | 是否立即停止 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local sound_entity = GameAPI.play_sound_for_player(player.handle, 134274569, false)

GameAPI.stop_sound(player.handle, sound_entity, true)
```

---

## sound_play_controller

method in GameAPI

- 描述

    播放控制

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | sound | py.SoundEntity | 声音 |
    | play_operation | integer | 播放操作 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local sound_entity = GameAPI.play_sound_for_player(player.handle, 134274569, false)

GameAPI.sound_play_controller(player.handle, sound_entity, 1)
```

---

## set_player_listener_to_follow_intersection_of_camera_ray_and_ground

method in GameAPI

- 描述

    设置玩家的声音接收器跟随镜头射线与地面焦点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | camera_ray_direction | py.CameraRayDirection | 相机射线方向 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_player_listener_to_follow_intersection_of_camera_ray_and_ground(player.handle, 1)
```

---

## set_player_listener_to_follow_unit

method in GameAPI

- 描述

    设置玩家的声音接收器跟随单位

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

GameAPI.set_player_listener_to_follow_unit(player.handle, unit.handle)
```

---

## open_background_music

method in GameAPI

- 描述

    设置背景音乐开关

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | value | boolean | 打开/关闭 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.open_background_music(player.handle, true)
```

---

## open_battle_music

method in GameAPI

- 描述

    设置战斗音乐开关

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | value | boolean | 打开/关闭 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.open_battle_music(player.handle, true)
```

---

## set_background_music_volume

method in GameAPI

- 描述

    设置背景音乐音量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | value | integer | 音量 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_background_music_volume(player.handle, 1)
```

---

## set_battle_music_volume

method in GameAPI

- 描述

    设置战斗音效音量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | value | integer | 音量 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_battle_music_volume(player.handle, 1)
```

---

## set_sound_volume

method in GameAPI

- 描述

    设置声音音量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | py.Role | 玩家 |
    | sound | py.SoundEntity | 声音 |
    | volume | integer | 音量 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local sound_entity = GameAPI.play_sound_for_player(player.handle, 134274569, false)

GameAPI.set_sound_volume(player.handle, sound_entity, 1)
```

---

## get_scene_sound_by_res_id

method in GameAPI

- 描述

    通过场景声音ID返回场景声音

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | res_id | py.SceneSoundID | 场景声音ID |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SceneSound | 场景声音 |

- 示例

```lua
local result = GameAPI.get_scene_sound_by_res_id(1)
```

---

## play_scene_sound

method in GameAPI

- 描述

    播放场景声音

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | scene_sound | py.SceneSound | 场景声音 |

- 返回值

    无

- 示例

```lua
local scene_sound = GameAPI.get_scene_sound_by_res_id(1)

GameAPI.play_scene_sound(scene_sound)
```

---

## stop_scene_sound

method in GameAPI

- 描述

    停止场景声音

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | scene_sound | py.SceneSound | 场景声音 |

- 返回值

    无

- 示例

```lua
local scene_sound = GameAPI.get_scene_sound_by_res_id(1)

GameAPI.stop_scene_sound(scene_sound)
```

---

## set_scene_sound_loop

method in GameAPI

- 描述

    设置场景声音是否循环

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | scene_sound | py.SceneSound | 场景声音 |
    | loop | boolean | 是否循环 |

- 返回值

    无

- 示例

```lua
local scene_sound = GameAPI.get_scene_sound_by_res_id(1)

GameAPI.set_scene_sound_loop(scene_sound, true)
```

---

## set_scene_sound_min_dist

method in GameAPI

- 描述

    设置场景声音衰减距离

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | scene_sound | py.SceneSound | 场景声音 |
    | min_dist | number | 衰减距离 |

- 返回值

    无

- 示例

```lua
local scene_sound = GameAPI.get_scene_sound_by_res_id(1)

GameAPI.set_scene_sound_min_dist(scene_sound, 1.0)
```

---

## set_scene_sound_max_dist

method in GameAPI

- 描述

    设置场景声音静音距离

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | scene_sound | py.SceneSound | 场景声音 |
    | max_dist | number | 静音距离 |

- 返回值

    无

- 示例

```lua
local scene_sound = GameAPI.get_scene_sound_by_res_id(1)

GameAPI.set_scene_sound_max_dist(scene_sound, 1.0)
```

---

## set_scene_sound_pause

method in GameAPI

- 描述

    设置场景声音是否暂停

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | scene_sound | py.SceneSound | 场景声音 |
    | paused | boolean | 是否暂停 |

- 返回值

    无

- 示例

```lua
local scene_sound = GameAPI.get_scene_sound_by_res_id(1)

GameAPI.set_scene_sound_pause(scene_sound, true)
```

---

## get_bgm_state

method in GameAPI

- 描述

    获取初始化背景音乐开关状态

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | value |

- 示例

```lua
local result = GameAPI.get_bgm_state()
```

---

## get_battle_bgm_state

method in GameAPI

- 描述

    获取初始化战斗音效开关状态

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | value |

- 示例

```lua
local result = GameAPI.get_battle_bgm_state()
```

---

## get_bgm_volume

method in GameAPI

- 描述

    获取初始化背景音乐音量

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | value |

- 示例

```lua
local result = GameAPI.get_bgm_volume()
```

---

## get_battle_volume

method in GameAPI

- 描述

    获取初始化战斗音效音量

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | value |

- 示例

```lua
local result = GameAPI.get_battle_volume()
```

---

## get_game_mode

method in GameAPI

- 描述

    获取当前游戏模式

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.GameMode | 游戏模式 |

- 示例

```lua
local result = GameAPI.get_game_mode()
```

---

## pause_game

method in GameAPI

- 描述

    暂停游戏

- 参数

    无

- 返回值

    无

- 示例

```lua
GameAPI.pause_game()
```

---

## set_melee_result_by_role

method in GameAPI

- 描述

    为玩家结束游戏

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | result | string | 战斗结果 |
    | show | boolean | 显示结束面板 |
    | send? | boolean | 是否上传玩家排行榜分数 |
    | score? | integer | 排行榜分数 |
    | accumulate? | boolean | 是否累积计算分数 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_melee_result_by_role(player.handle, "result", true, true, 1, true)
```

---

## set_melee_result_by_role_2

method in GameAPI

- 描述

    结束玩家游戏

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | result | string | 战斗结果 |
    | comp_uid | string | 控件uid |
    | send? | boolean | 是否上传玩家排行榜分数 |
    | score? | integer | 排行榜分数 |
    | accumulate? | boolean | 是否累积计算分数 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_melee_result_by_role_2(player.handle, "result", "comp_uid", true, 1, true)
```

---

## upload_role_billboard_score

method in GameAPI

- 描述

    上传玩家排行榜分数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | score | integer | 排行榜分数 |
    | accumulate? | boolean | 是否累积计算分数 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.upload_role_billboard_score(player.handle, 1, true)
```

---

## game_end

method in GameAPI

- 描述

    结束游戏

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player_results? | py.Dict | 玩家结算信息 |

- 返回值

    无

- 示例

```lua
local dict = pydict()

GameAPI.game_end()
```

---

## request_new_round

method in GameAPI

- 描述

    申请开始下一轮

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | fast_restart? | boolean | 是否快速重置 |

- 返回值

    无

- 示例

```lua
GameAPI.request_new_round(true)
```

---

## request_switch_level

method in GameAPI

- 描述

    切换至关卡

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | level_id_str | py.Map | 关卡ID |
    | load_same_world? | boolean | 是否跳过场景加载 |
    | skip_loading_ui? | boolean | 是否跳过UI加载 |

- 返回值

    无

- 示例

```lua
GameAPI.request_switch_level(1, true, true)
```

---

## get_global_map_archive

method in GameAPI

- 描述

    获取当前地图的指定key的存档值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 指定的全局存档key值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 全局存档值 |

- 示例

```lua
local result = GameAPI.get_global_map_archive("key")
```

---

## get_rank_player_nickname

method in GameAPI

- 描述

    获取地图全局指定key存档的第n名玩家的昵称

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | rank_key | string | key值 |
    | num | integer | 第n名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 昵称 |

- 示例

```lua
local result = GameAPI.get_rank_player_nickname("rank_key", 1)
```

---

## get_rank_player_global_archive_value

method in GameAPI

- 描述

    获取地图全局指定key存档的第n名玩家的存档值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | rank_key | string | key值 |
    | num | integer | 第n名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 存档值 |

- 示例

```lua
local result = GameAPI.get_rank_player_global_archive_value("rank_key", 1)
```

---

## get_archive_rank_player_nickname

method in GameAPI

- 描述

    获取玩家指定的个人存档栏位的第n名玩家的昵称

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | archive_key | integer | 玩家存档栏位 |
    | num | integer | 第n名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 昵称 |

- 示例

```lua
local result = GameAPI.get_archive_rank_player_nickname(1, 1)
```

---

## get_archive_rank_player_archive_value

method in GameAPI

- 描述

    获取玩家指定的个人存档栏位的第n名玩家的存档值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | archive_key | integer | 玩家存档栏位 |
    | num | integer | 第n名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 存档值 |

- 示例

```lua
local result = GameAPI.get_archive_rank_player_archive_value(1, 1)
```

---

## api_change_logic_fps

method in GameAPI

- 描述

    调整逻辑帧率

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | fps | integer | 目标帧率 |

- 返回值

    无

- 示例

```lua
GameAPI.api_change_logic_fps(1)
```

---

## api_soft_pause_game

method in GameAPI

- 描述

    开启软暂停

- 参数

    无

- 返回值

    无

- 示例

```lua
GameAPI.api_soft_pause_game()
```

---

## api_soft_resume_game

method in GameAPI

- 描述

    关闭软暂停

- 参数

    无

- 返回值

    无

- 示例

```lua
GameAPI.api_soft_resume_game()
```

---

## get_owner_role_id

method in GameAPI

- 描述

    本地玩家编号

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleID | 玩家编号 |

- 示例

```lua
local result = GameAPI.get_owner_role_id()
```

---

## get_local_player_pointing_pos

method in GameAPI

- 描述

    本地玩家鼠标位置

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Point | 鼠标位置 |

- 示例

```lua
local result = GameAPI.get_local_player_pointing_pos()
```

---

## get_local_player_ui_pos_x

method in GameAPI

- 描述

    本地玩家鼠标屏幕位置X

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 鼠标屏幕位置X |

- 示例

```lua
local result = GameAPI.get_local_player_ui_pos_x()
```

---

## get_local_player_ui_pos_y

method in GameAPI

- 描述

    本地玩家鼠标屏幕位置Y

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 鼠标屏幕位置Y |

- 示例

```lua
local result = GameAPI.get_local_player_ui_pos_y()
```

---

## get_local_role_ui_x_per

method in GameAPI

- 描述

    本地玩家鼠标屏幕位置X的窗口占比

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 占比值 |

- 示例

```lua
local result = GameAPI.get_local_role_ui_x_per()
```

---

## get_local_role_ui_y_per

method in GameAPI

- 描述

    本地玩家鼠标屏幕位置y的窗口占比

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 占比值 |

- 示例

```lua
local result = GameAPI.get_local_role_ui_y_per()
```

---

## get_local_player_camera_direction

method in GameAPI

- 描述

    本地玩家摄像机朝向

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Point | 摄像机朝向 |

- 示例

```lua
local result = GameAPI.get_local_player_camera_direction()
```

---

## get_local_player_camera_center_raycast

method in GameAPI

- 描述

    本地玩家摄像机中心射线检测

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Point | 交点 |

- 示例

```lua
local result = GameAPI.get_local_player_camera_center_raycast()
```

---

## get_game_init_time_stamp

method in GameAPI

- 描述

    获取游戏开始时间戳

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 游戏开始时间戳 |

- 示例

```lua
local result = GameAPI.get_game_init_time_stamp()
```

---

## get_local_time_stamp

method in GameAPI

- 描述

    获取本地时间戳

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 本地时间戳 |

- 示例

```lua
local result = GameAPI.get_local_time_stamp()
```

---

## add_local_timer

method in GameAPI

- 描述

    添加本地计时器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | delay | number | 延迟 |
    | callback | function | 回调 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 计时器编号 |

- 示例

```lua
local result = GameAPI.add_local_timer(1.0, function() end)
```

---

## add_local_repeat_timer

method in GameAPI

- 描述

    添加本地循环计时器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | interval | number | 间隔 |
    | callback | function | 回调 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 计时器编号 |

- 示例

```lua
local result = GameAPI.add_local_repeat_timer(1.0, function() end)
```

---

## cancel_local_timer

method in GameAPI

- 描述

    取消本地计时器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | timer_id | integer | 计时器编号 |

- 返回值

    无

- 示例

```lua
GameAPI.cancel_local_timer(1)
```

---

## force_enable_mouse_sync

method in GameAPI

- 描述

    强制开启/关闭鼠标同步

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | enable | boolean | 开关 |

- 返回值

    无

- 示例

```lua
GameAPI.force_enable_mouse_sync(true)
```

---

## force_enable_keyboard_sync

method in GameAPI

- 描述

    强制开启/关闭按键同步

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | enable | boolean | 开关 |

- 返回值

    无

- 示例

```lua
GameAPI.force_enable_keyboard_sync(true)
```

---

## force_enable_camera_sync

method in GameAPI

- 描述

    强制开启/关闭镜头同步

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | enable | boolean | 开关 |

- 返回值

    无

- 示例

```lua
GameAPI.force_enable_camera_sync(true)
```

---

## init_bind_nim

method in GameAPI

- 描述

    启动云信并绑定对象

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | entity | py.Unit | 单位 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

GameAPI.init_bind_nim(player.handle, unit.handle)
```

---

## api_set_v_sync

method in GameAPI

- 描述

    启用/禁用垂直同步

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | enable | boolean | 开启 |

- 返回值

    无

- 示例

```lua
GameAPI.api_set_v_sync(true)
```

---

## api_set_local_mapping_key

method in GameAPI

- 描述

    设置本地改键

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | py.KeyboardKey | 原始按键 |
    | target_key | py.KeyboardKey | 目标按键 |

- 返回值

    无

- 示例

```lua
GameAPI.api_set_local_mapping_key(1, 1)
```

---

## api_cancel_local_mapping_key

method in GameAPI

- 描述

    取消本地改键

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | py.KeyboardKey | 原始按键 |

- 返回值

    无

- 示例

```lua
GameAPI.api_cancel_local_mapping_key(1)
```

---

## api_clear_local_mapping_key

method in GameAPI

- 描述

    清空本地改键

- 参数

    无

- 返回值

    无

- 示例

```lua
GameAPI.api_clear_local_mapping_key()
```

---

## api_set_builtin_key_control_enable

method in GameAPI

- 描述

    设置是否使用内置本地改键方案

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | enable | boolean | 是否使用 |

- 返回值

    无

- 示例

```lua
GameAPI.api_set_builtin_key_control_enable(true)
```

---

## api_is_builtin_key_control_enable

method in GameAPI

- 描述

    判断是否使用内置键盘控制

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 布尔值 |

- 示例

```lua
local result = GameAPI.api_is_builtin_key_control_enable()
```

---

## api_set_role_camera_mode

method in GameAPI

- 描述

    设置玩家镜头模式

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | cam_mod | py.CameraMode | 镜头模式 |
    | ortho_scale? | number | 正交缩放 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.api_set_role_camera_mode(player.handle, 1, 1.0)
```

---

## is_cameraIS_playing_timeline

method in GameAPI

- 描述

    玩家镜头是否正在播放动画

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否播放动画 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.is_cameraIS_playing_timeline(player.handle)
```

---

## play_camera_timeline

method in GameAPI

- 描述

    播放镜头动画

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | camline_id | py.CamlineID | 镜头TimelineID |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.play_camera_timeline(player.handle, 1)
```

---

## stop_camera_timeline

method in GameAPI

- 描述

    停止播放镜头动画

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.stop_camera_timeline(player.handle)
```

---

## api_set_obj_fresnel_visible

method in GameAPI

- 描述

    设置对象的菲涅尔效果开关

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | log_obj | py.Actor | 对象 |
    | visible | boolean | 开关 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.api_set_obj_fresnel_visible(actor, true)
```

---

## api_set_obj_fresnel_parameters

method in GameAPI

- 描述

    设置对象的菲涅尔效果

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | log_obj | py.Actor | 对象 |
    | color_r? | integer | R |
    | color_g? | integer | G |
    | color_b? | integer | B |
    | alpha? | number | alpha |
    | exp? | number | exp |
    | strength? | number | strength |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.api_set_obj_fresnel_parameters(actor, 1, 1, 1, 1.0, 1.0, 1.0)
```

---

## set_focus_distance

method in GameAPI

- 描述

    设置模型加载范围

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | focus_distance | number | 范围 |

- 返回值

    无

- 示例

```lua
GameAPI.set_focus_distance(1.0)
```

---

## set_image_quality

method in GameAPI

- 描述

    设置画质

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | quality | string | 画质 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_image_quality(player.handle, "quality")
```

---

## get_graphics_quality

method in GameAPI

- 描述

    获取初始化游戏画质

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | value |

- 示例

```lua
local result = GameAPI.get_graphics_quality()
```

---

## set_post_effect

method in GameAPI

- 描述

    设置画风

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | post_style_type | py.PostEffect | 画风 |
    | color_r? | integer | R |
    | color_g? | integer | R |
    | color_b? | integer | R |
    | depth_scale? | number | 描边 |
    | intensity? | number | 强度 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_post_effect(player.handle, 1, 1, 1, 1, 1.0, 1.0)
```

---

## set_cascaded_shadow_enable

method in GameAPI

- 描述

    级联阴影开关

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_enable | boolean | 开关 |

- 返回值

    无

- 示例

```lua
GameAPI.set_cascaded_shadow_enable(true)
```

---

## set_dynamic_shadow_cascades

method in GameAPI

- 描述

    级联阴影层数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | levels | integer | 层数 |

- 返回值

    无

- 示例

```lua
GameAPI.set_dynamic_shadow_cascades(1)
```

---

## set_dynamic_shadow_distance_movable_light

method in GameAPI

- 描述

    级联阴影距离

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | distance | number | 距离 |

- 返回值

    无

- 示例

```lua
GameAPI.set_dynamic_shadow_distance_movable_light(1.0)
```

---

## set_cascaded_shadow_distance

method in GameAPI

- 描述

    阴影距离

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | distance | number | 距离 |

- 返回值

    无

- 示例

```lua
GameAPI.set_cascaded_shadow_distance(1.0)
```

---

## get_cascaded_shadow_enable

method in GameAPI

- 描述

    获取级联阴影状态

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 状态 |

- 示例

```lua
local result = GameAPI.get_cascaded_shadow_enable()
```

---

## get_dynamic_shadow_cascades

method in GameAPI

- 描述

    获取级联阴影层数

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 层数 |

- 示例

```lua
local result = GameAPI.get_dynamic_shadow_cascades()
```

---

## get_dynamic_shadow_distance_movable_light

method in GameAPI

- 描述

    获取级联阴影距离

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 距离 |

- 示例

```lua
local result = GameAPI.get_dynamic_shadow_distance_movable_light()
```

---

## get_cascaded_shadow_distance

method in GameAPI

- 描述

    获取阴影距离

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 距离 |

- 示例

```lua
local result = GameAPI.get_cascaded_shadow_distance()
```

---

## get_light_float_attr_value

method in GameAPI

- 描述

    获取光源Float属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | light | py.Light | 光源 |
    | attr_name | string | 属性名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 值 |

- 示例

```lua
local light = GameAPI.get_point_light_res_by_res_id(1)

local result = GameAPI.get_light_float_attr_value(light, "attr_name")
```

---

## set_light_cast_shadow_attr_value

method in GameAPI

- 描述

    设置光源是否产生阴影

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | light | py.Light | 光源 |
    | value | boolean | 值 |

- 返回值

    无

- 示例

```lua
local light = GameAPI.get_point_light_res_by_res_id(1)

GameAPI.set_light_cast_shadow_attr_value(light, true)
```

---

## get_light_cast_shadow_attr_value

method in GameAPI

- 描述

    获取光源是否产生阴影

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | light | py.Light | 光源 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 值 |

- 示例

```lua
local light = GameAPI.get_point_light_res_by_res_id(1)

local result = GameAPI.get_light_cast_shadow_attr_value(light)
```

---

## get_fog_res_by_res_id

method in GameAPI

- 描述

    根据局部雾ID返回局部雾

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | res_id | py.FogID | 雾ID |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fog | 雾 |

- 示例

```lua
local result = GameAPI.get_fog_res_by_res_id(1)
```

---

## set_fog_attr

method in GameAPI

- 描述

    修改雾效属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | fog | py.Fog | 雾 |
    | op_flag | integer | 默认参数 |
    | yaw? | number | 朝向 |
    | pos_x? | number | 位置x |
    | pos_y? | number | 位置y |
    | pos_z? | number | 位置z |
    | scale_x? | number | 缩放x |
    | scale_y? | number | 缩放y |
    | scale_z? | number | 缩放z |
    | color_r? | number | 颜色r |
    | color_g? | number | 颜色g |
    | color_b? | number | 颜色b |
    | density? | number | 浓度 |
    | flow_speed? | number | 流速 |

- 返回值

    无

- 示例

```lua
local fog = GameAPI.get_fog_res_by_res_id(1)

GameAPI.set_fog_attr(fog, 1, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0)
```

---

## set_fog_attr_new

method in GameAPI

- 描述

    修改雾效属性新

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | fog | py.Fog | 雾 |
    | fog_attr | string | 雾效属性 |
    | value | number | 值 |

- 返回值

    无

- 示例

```lua
local fog = GameAPI.get_fog_res_by_res_id(1)

GameAPI.set_fog_attr_new(fog, "fog_attr", 1.0)
```

---

## enable_fow_for_player

method in GameAPI

- 描述

    为玩家开关全局视野

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | enable | boolean | 开关 |

- 返回值

    无

- 示例

```lua
GameAPI.enable_fow_for_player(true)
```

---

## change_mini_map_img

method in GameAPI

- 描述

    设置小地图替代图片

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | image_id | integer | 图片id |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.change_mini_map_img(player.handle, 1)
```

---

## change_mini_map_img_with_icon

method in GameAPI

- 描述

    设置小地图替代图片(图片类型)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | image_id | py.Texture | 图片 |
    | specify_mini_map? | string | 指定的小地图 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.change_mini_map_img_with_icon(player.handle, 1, "specify_mini_map")
```

---

## change_mini_map_color_type

method in GameAPI

- 描述

    设置小地图颜色显示模式

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | color_type | integer | 显示模式 |
    | specify_mini_map? | string | 指定的小地图 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.change_mini_map_color_type(player.handle, 1, "specify_mini_map")
```

---

## enable_unit_path_drawing

method in GameAPI

- 描述

    开启绘制单位路径线

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | unit | py.Unit | 单位 |
    | specify_mini_map? | string | 指定的小地图 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

GameAPI.enable_unit_path_drawing(player.handle, unit.handle, "specify_mini_map")
```

---

## disable_unit_path_drawing

method in GameAPI

- 描述

    关闭绘制单位路径线

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | unit | py.Unit | 单位 |
    | specify_mini_map? | string | 指定的小地图 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

GameAPI.disable_unit_path_drawing(player.handle, unit.handle, "specify_mini_map")
```

---

## set_min_map_show_area

method in GameAPI

- 描述

    设置小地图显示区域

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | rect_area | py.RecArea | 矩形区域 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local rec_area = GameAPI.create_rec_area_from_two_points(Fix32Vec3(0, 0, 0), Fix32Vec3(100, 100, 0))

GameAPI.set_min_map_show_area(player.handle, rec_area)
```

---

## set_local_player_jump_word_close

method in GameAPI

- 描述

    关闭localplayer的表现层跳字

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_close | boolean | 是否关闭 |

- 返回值

    无

- 示例

```lua
GameAPI.set_local_player_jump_word_close(true)
```

---

## api_change_obj_base_color

method in GameAPI

- 描述

    设置对象的基础材质属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | logic_obj | py.Actor | 逻辑对象 |
    | color_r? | integer | R |
    | color_g? | integer | G |
    | color_b? | integer | B |
    | color_a? | integer | A |
    | base_model_opacity? | integer | model_opacity |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.api_change_obj_base_color(actor, 1, 1, 1, 1, 1)
```

---

## set_camera_floating_with_terrain

method in GameAPI

- 描述

    设置镜头是否跟随地形高度浮动

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | enable | boolean | 开关 |
    | detect_range? | integer | 检测范围 |

- 返回值

    无

- 示例

```lua
GameAPI.set_camera_floating_with_terrain(true, 1)
```

---

## modify_point_texture

method in GameAPI

- 描述

    修改某点的地形纹理

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | position | py.Point | 指定点 |
    | texture_type | integer | 纹理类型 |
    | radius | integer | 范围 |
    | area_shape | integer | 区域类型 |

- 返回值

    无

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)

GameAPI.modify_point_texture(point, 1, 1, 1)
```

---

## modify_point_height

method in GameAPI

- 描述

    修改某点的地形高度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | position | py.Point | 指定点 |
    | terrain_height | integer | 高度 |
    | radius | integer | 范围 |
    | area_shape | integer | 区域类型 |

- 返回值

    无

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)

GameAPI.modify_point_height(point, 1, 1, 1)
```

---

## replace_point_texture

method in GameAPI

- 描述

    替换区域中的指定地形纹理

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.Area | 区域 |
    | texture_type | integer | 纹理类型 |
    | new_texture_type | integer | 新纹理类型 |

- 返回值

    无

- 示例

```lua
local area = y3.area.create_circle_area(y3.point.create(0, 0, 0), 500)

GameAPI.replace_point_texture(area.handle, 1, 1)
```

---

## get_texture_type

method in GameAPI

- 描述

    获取纹理类型

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

local result = GameAPI.get_texture_type(point)
```

---

## set_local_terrain_visible

method in GameAPI

- 描述

    修改玩家的地表纹理

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | bool_value | boolean | 布尔值 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_local_terrain_visible(player.handle, true)
```

---

## set_material_param

method in GameAPI

- 描述

    修改材质属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | py.Actor | 对象 |
    | material_id | integer | 材质id |
    | r_value | number | R |
    | g_value | number | G |
    | b_value | number | B |
    | intensity? | number | 强度 |
    | alpha? | number | 透明度 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_material_param(actor, 1, 1.0, 1.0, 1.0, 1.0, 1.0)
```

---

## set_role_color_grading

method in GameAPI

- 描述

    为玩家设置滤镜效果

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | value | integer | id |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_role_color_grading(player.handle, 1)
```

---

## set_screen_resolution

method in GameAPI

- 描述

    设置分辨率

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | x_resolution | number | 横向分辨率 |
    | y_resolution | number | 纵向分辨率 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_screen_resolution(player.handle, 1.0, 1.0)
```

---

## set_window_type

method in GameAPI

- 描述

    设置窗口

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | window_type | string | 样式 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_window_type(player.handle, "window_type")
```

---

## set_grass_enable_by_pos

method in GameAPI

- 描述

    开关目标点的草丛

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | enable | boolean | 开关 |
    | point | py.Point | 点 |

- 返回值

    无

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)

GameAPI.set_grass_enable_by_pos(true, point)
```

---

## get_window_mode

method in GameAPI

- 描述

    获取初始化窗口类别

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | value |

- 示例

```lua
local result = GameAPI.get_window_mode()
```

---

## get_game_x_resolution

method in GameAPI

- 描述

    获取初始化横向分辨率

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | value |

- 示例

```lua
local result = GameAPI.get_game_x_resolution()
```

---

## get_game_y_resolution

method in GameAPI

- 描述

    获取初始化纵向分辨率

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | value |

- 示例

```lua
local result = GameAPI.get_game_y_resolution()
```

---

## get_window_real_x_size

method in GameAPI

- 描述

    当前窗体横向尺寸

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | value |

- 示例

```lua
local result = GameAPI.get_window_real_x_size()
```

---

## get_window_real_y_size

method in GameAPI

- 描述

    当前窗体纵向尺寸

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | value |

- 示例

```lua
local result = GameAPI.get_window_real_y_size()
```

---

## get_screen_x_resolution

method in GameAPI

- 描述

    获取屏幕横向分辨率

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | value |

- 示例

```lua
local result = GameAPI.get_screen_x_resolution()
```

---

## get_screen_y_resolution

method in GameAPI

- 描述

    获取屏幕纵向分辨率

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | value |

- 示例

```lua
local result = GameAPI.get_screen_y_resolution()
```

---

## check_unit_key_precondition

method in GameAPI

- 描述

    判断玩家单位类型前置条件满足需求

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | py.Role | 玩家 |
    | unity_key | py.UnitKey | 单位类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否满足 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local unit_key = 134274569

local result = GameAPI.check_unit_key_precondition(player.handle, unit_key)
```

---

## check_item_key_precondition

method in GameAPI

- 描述

    判断玩家物品类型前置条件满足需求

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | py.Role | 玩家 |
    | item_key | py.ItemKey | 物品类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否满足 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local item_key = 134274569

local result = GameAPI.check_item_key_precondition(player.handle, item_key)
```

---

## check_tech_key_precondition

method in GameAPI

- 描述

    判断玩家科技类型前置条件满足需求

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | py.Role | 玩家 |
    | tech_key | py.TechKey | 科技类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否满足 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local tech_key = 134274569

local result = GameAPI.check_tech_key_precondition(player.handle, tech_key)
```

---

## check_ability_key_precondition

method in GameAPI

- 描述

    判断玩家技能类型前置条件满足需求

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | py.Role | 玩家 |
    | ability_key | py.AbilityKey | 技能类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否满足 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ability_key = 134274569

local result = GameAPI.check_ability_key_precondition(player.handle, ability_key)
```

---

## get_ability_key_precondition_list

method in GameAPI

- 描述

    获取技能类型的前置条件列表

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 前置条件列表 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_precondition_list(ability_key)
```

---

## get_unit_key_precondition_list

method in GameAPI

- 描述

    获取单位类型的前置条件列表

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 前置条件列表 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_precondition_list(unit_key)
```

---

## get_item_key_precondition_list

method in GameAPI

- 描述

    获取物品类型的前置条件列表

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 前置条件列表 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_precondition_list(item_key)
```

---

## get_pre_condition_iter_unit_key

method in GameAPI

- 描述

    获取前置条件遍历到的单位类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | iter_data | py.Actor | 数据 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitKey | 单位类型 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_pre_condition_iter_unit_key(actor)
```

---

## get_pre_condition_iter_tech_key

method in GameAPI

- 描述

    获取前置条件遍历到的科技类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | iter_data | py.Actor | 数据 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.TechKey | 科技类型 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_pre_condition_iter_tech_key(actor)
```

---

## get_pre_condition_iter_unit_tag

method in GameAPI

- 描述

    获取前置条件遍历到的单位标签

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | iter_data | py.Actor | 数据 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 单位标签 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_pre_condition_iter_unit_tag(actor)
```

---

## get_pre_condition_iter_tech_tag

method in GameAPI

- 描述

    获取前置条件遍历到的科技标签

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | iter_data | py.Actor | 数据 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 科技标签 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_pre_condition_iter_tech_tag(actor)
```

---

## get_unit_type_unit_key_pre_condition_require_count

method in GameAPI

- 描述

    获取单位单位类型前置条件的需求值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | source_item_key | py.UnitKey | 检测的单位 |
    | target_item_key | py.UnitKey | 查询的单位类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 需求值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_type_unit_key_pre_condition_require_count(unit_key, unit_key)
```

---

## get_unit_type_unit_tag_pre_condition_require_count

method in GameAPI

- 描述

    获取单位单位标签前置条件的需求值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | source_item_key | py.UnitKey | 检测的单位 |
    | target_item_key | string | 查询的单位标签 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 需求值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_type_unit_tag_pre_condition_require_count(unit_key, "target_item_key")
```

---

## get_unit_type_tech_key_pre_condition_require_count

method in GameAPI

- 描述

    获取单位科技类型前置条件的需求值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | source_item_key | py.UnitKey | 检测的单位 |
    | target_item_key | py.TechKey | 查询的科技类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 需求值 |

- 示例

```lua
local unit_key = 134274569
local tech_key = 134274569

local result = GameAPI.get_unit_type_tech_key_pre_condition_require_count(unit_key, tech_key)
```

---

## get_unit_type_tech_tag_pre_condition_require_count

method in GameAPI

- 描述

    获取单位科技标签前置条件的需求值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | source_item_key | py.UnitKey | 检测的单位 |
    | target_item_key | string | 查询的科技标签 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 需求值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_type_tech_tag_pre_condition_require_count(unit_key, "target_item_key")
```

---

## get_ability_type_unit_key_pre_condition_require_count

method in GameAPI

- 描述

    获取技能单位类型前置条件的需求值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | source_item_key | py.AbilityKey | 检测的技能 |
    | target_item_key | py.UnitKey | 查询的单位类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 需求值 |

- 示例

```lua
local ability_key = 134274569
local unit_key = 134274569

local result = GameAPI.get_ability_type_unit_key_pre_condition_require_count(ability_key, unit_key)
```

---

## get_ability_type_unit_tag_pre_condition_require_count

method in GameAPI

- 描述

    获取技能单位标签前置条件的需求值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | source_item_key | py.AbilityKey | 检测的技能 |
    | target_item_key | string | 查询的单位标签 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 需求值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_type_unit_tag_pre_condition_require_count(ability_key, "target_item_key")
```

---

## get_ability_type_tech_key_pre_condition_require_count

method in GameAPI

- 描述

    获取技能科技类型前置条件的需求值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | source_item_key | py.AbilityKey | 检测的技能 |
    | target_item_key | py.TechKey | 查询的科技类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 需求值 |

- 示例

```lua
local ability_key = 134274569
local tech_key = 134274569

local result = GameAPI.get_ability_type_tech_key_pre_condition_require_count(ability_key, tech_key)
```

---

## get_ability_type_tech_tag_pre_condition_require_count

method in GameAPI

- 描述

    获取技能科技标签前置条件的需求值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | source_item_key | py.AbilityKey | 检测的技能 |
    | target_item_key | string | 查询的科技标签 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 需求值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_type_tech_tag_pre_condition_require_count(ability_key, "target_item_key")
```

---

## get_item_type_unit_key_pre_condition_require_count

method in GameAPI

- 描述

    获取物品单位类型前置条件的需求值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | source_item_key | py.ItemKey | 检测的物品 |
    | target_item_key | py.UnitKey | 查询的单位类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 需求值 |

- 示例

```lua
local item_key = 134274569
local unit_key = 134274569

local result = GameAPI.get_item_type_unit_key_pre_condition_require_count(item_key, unit_key)
```

---

## get_item_type_unit_tag_pre_condition_require_count

method in GameAPI

- 描述

    获取物品单位标签前置条件的需求值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | source_item_key | py.ItemKey | 检测的物品 |
    | target_item_key | string | 查询的单位标签 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 需求值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_type_unit_tag_pre_condition_require_count(item_key, "target_item_key")
```

---

## get_item_type_tech_key_pre_condition_require_count

method in GameAPI

- 描述

    获取物品科技类型前置条件的需求值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | source_item_key | py.ItemKey | 检测的物品 |
    | target_item_key | py.TechKey | 查询的科技类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 需求值 |

- 示例

```lua
local item_key = 134274569
local tech_key = 134274569

local result = GameAPI.get_item_type_tech_key_pre_condition_require_count(item_key, tech_key)
```

---

## get_item_type_tech_tag_pre_condition_require_count

method in GameAPI

- 描述

    获取物品科技标签前置条件的需求值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | source_item_key | py.ItemKey | 检测的物品 |
    | target_item_key | string | 查询的科技标签 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 需求值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_type_tech_tag_pre_condition_require_count(item_key, "target_item_key")
```

---

## set_ui_comp_adapt_option

method in GameAPI

- 描述

    设置控件适配

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件uid |
    | direction | integer | 方向 |
    | offset | number | offset |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_adapt_option(player.handle, "comp_name", 1, 1.0)
```

---

## trigger_ui_event

method in GameAPI

- 描述

    使玩家触发界面事件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件uid |
    | event_name | string | 事件名 |
    | not_wait_network? | boolean | 不等待网络返回 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.trigger_ui_event(player.handle, "comp_name", "event_name", true)
```

---

## set_ui_comp_follow_mouse

method in GameAPI

- 描述

    控制控件跟随鼠标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件uid |
    | is_follow | boolean | 是否跟随 |
    | offset_x? | number | 偏移x |
    | offset_y? | number | 偏移y |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_follow_mouse(player.handle, "comp_name", true, 1.0, 1.0)
```

---

## pos_in_comp_box

method in GameAPI

- 描述

    【异步】获得坐标是否在控件内

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | x | number | x |
    | y | number | y |
    | comp_name | string | 控件uid |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否在其中 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.pos_in_comp_box(player.handle, 1.0, 1.0, "comp_name")
```

---

## set_model_comp_camera_mod

method in GameAPI

- 描述

    设置模型控件的镜头模式

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | camera_mod | integer | 镜头模式 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_model_comp_camera_mod(player.handle, "comp_uid", 1)
```

---

## set_ui_btn_status_string

method in GameAPI

- 描述

    设置不同状态下的按钮文本

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | btn_status | integer | 按钮状态 |
    | btn_text | string | 文本 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_btn_status_string(player.handle, "comp_uid", 1, "btn_text")
```

---

## set_ui_btn_status_image

method in GameAPI

- 描述

    设置不同状态下的按钮图片

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | btn_status | integer | 按钮状态 |
    | btn_image | integer | 图片 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_btn_status_image(player.handle, "comp_uid", 1, 1)
```

---

## set_ui_scrollview_type

method in GameAPI

- 描述

    设置列表控件的布局方式

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | scrollview_type | integer | 布局方式 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_scrollview_type(player.handle, "comp_uid", 1)
```

---

## set_ui_scrollview_size_change_according_children

method in GameAPI

- 描述

    设置列表控件的尺寸是否跟随子控件变化

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | flag | boolean | 布尔值 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_scrollview_size_change_according_children(player.handle, "comp_uid", true)
```

---

## set_ui_image_color

method in GameAPI

- 描述

    设置图片颜色

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件名 |
    | r | number | R |
    | g | number | G |
    | b | number | B |
    | a | number | A |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_image_color(player.handle, "comp_uid", 1.0, 1.0, 1.0, 1.0)
```

---

## get_role_ui_comp_real_width

method in GameAPI

- 描述

    【异步】界面-获取控件的真实宽度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件名 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.get_role_ui_comp_real_width(player.handle, "comp_uid")
```

---

## get_role_ui_comp_real_height

method in GameAPI

- 描述

    【异步】界面-获取控件的真实高度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件名 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.get_role_ui_comp_real_height(player.handle, "comp_uid")
```

---

## get_role_real_mouse_x

method in GameAPI

- 描述

    【异步】界面-获取玩家鼠标真实x坐标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.get_role_real_mouse_x(player.handle)
```

---

## get_role_real_mouse_y

method in GameAPI

- 描述

    【异步】界面-获取玩家鼠标真实y坐标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.get_role_real_mouse_y(player.handle)
```

---

## set_cur_chatbox

method in GameAPI

- 描述

    设置当前聊天框控件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 聊天框id |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_cur_chatbox(player.handle, "comp_uid")
```

---

## ui_comp_is_exist

method in GameAPI

- 描述

    界面组件是否存在

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ui_comp | string | 界面组件名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local result = GameAPI.ui_comp_is_exist("ui_comp")
```

---

## show_ui_comp_animation

method in GameAPI

- 描述

    显示ui组件并播放动画

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | anim_name? | string | 动画名 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.show_ui_comp_animation(player.handle, "comp_name", "anim_name")
```

---

## hide_ui_comp_animation

method in GameAPI

- 描述

    隐藏ui组件并播放动画

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | anim_name? | string | 动画名 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.hide_ui_comp_animation(player.handle, "comp_name", "anim_name")
```

---

## set_ui_comp_pos

method in GameAPI

- 描述

    设置ui组件坐标

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

GameAPI.set_ui_comp_pos(player.handle, "comp_name", 1.0, 1.0)
```

---

## set_ui_comp_pos_no_trans

method in GameAPI

- 描述

    设置ui组件坐标没有转化

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

GameAPI.set_ui_comp_pos_no_trans(player.handle, "comp_name", 1.0, 1.0)
```

---

## set_ui_comp_scale

method in GameAPI

- 描述

    设置ui组件缩放

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | width | number | width |
    | height | number | height |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_scale(player.handle, "comp_name", 1.0, 1.0)
```

---

## set_ui_comp_size

method in GameAPI

- 描述

    设置ui组件尺寸

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | width | number | width |
    | height | number | height |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_size(player.handle, "comp_name", 1.0, 1.0)
```

---

## set_ui_comp_z_order

method in GameAPI

- 描述

    设置ui组件深度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | z_order | integer | z_order |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_z_order(player.handle, "comp_name", 1)
```

---

## set_ui_comp_image

method in GameAPI

- 描述

    设置ui组件图片

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | image_id | integer | 图片id |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_image(player.handle, "comp_name", 1)
```

---

## set_ui_comp_margin

method in GameAPI

- 描述

    设置ui列表组件间距

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | margin | integer | 间距 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_margin(player.handle, "comp_name", 1)
```

---

## set_ui_comp_image_with_icon

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

GameAPI.set_ui_comp_image_with_icon(player.handle, "comp_name", 1)
```

---

## set_ui_comp_sequence

method in GameAPI

- 描述

    设置ui组件序列帧

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | image_id | py.Sequence | 图片 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_sequence(player.handle, "comp_name", 1)
```

---

## play_ui_comp_sequence

method in GameAPI

- 描述

    播放序列帧

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | loop? | boolean | 循环 |
    | space? | number | 间隔 |
    | start_frame? | integer | 开始帧 |
    | end_frame? | integer | 结束帧 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.play_ui_comp_sequence(player.handle, "comp_name", true, 1.0, 1, 1)
```

---

## stop_ui_comp_sequence

method in GameAPI

- 描述

    停止播放序列帧

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.stop_ui_comp_sequence(player.handle, "comp_name")
```

---

## set_progress_bar_max_value

method in GameAPI

- 描述

    设置进度条最大值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | max_value | number | 最大值 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_progress_bar_max_value(player.handle, "comp_name", 1.0)
```

---

## set_progress_bar_current_value

method in GameAPI

- 描述

    设置进度条当前值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | current_value | number | 当前值 |
    | time? | number | 渐变时间 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_progress_bar_current_value(player.handle, "comp_name", 1.0, 1.0)
```

---

## set_ui_comp_enable

method in GameAPI

- 描述

    设置ui开启/关闭

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | current_value | boolean | 是否开启 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_enable(player.handle, "comp_name", true)
```

---

## set_ui_comp_visible

method in GameAPI

- 描述

    设置ui显示/隐藏

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | visible | boolean | 显/隐 |
    | comp_name | string | 控件名 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_visible(player.handle, true, "comp_name")
```

---

## set_ui_comp_font_color

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

GameAPI.set_ui_comp_font_color(player.handle, "comp_name", 1.0, 1.0, 1.0, 1.0)
```

---

## set_ui_comp_text

method in GameAPI

- 描述

    设置ui文本

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | content | string | 文本 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_text(player.handle, "comp_name", "content")
```

---

## set_ui_comp_font_size

method in GameAPI

- 描述

    设置ui文本大小

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | size | integer | 文本大小 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_font_size(player.handle, "comp_name", 1)
```

---

## set_input_field_focus

method in GameAPI

- 描述

    设置输入框获得焦点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_input_field_focus(player.handle, "comp_name")
```

---

## set_input_field_not_focus

method in GameAPI

- 描述

    设置输入框失去焦点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_input_field_not_focus(player.handle, "comp_name")
```

---

## play_ui_comp_anim

method in GameAPI

- 描述

    播放UI控件时间轴动画

- 参数

    无

- 返回值

    无

- 示例

```lua
GameAPI.play_ui_comp_anim()
```

---

## stop_ui_comp_anim

method in GameAPI

- 描述

    停止UI控件时间轴动画

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | anim_id | py.UIAnimKey | UI动画 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui_anim_key = GameAPI.get_unit_key_ui_anim_kv(1, "key")

GameAPI.stop_ui_comp_anim(player.handle, ui_anim_key)
```

---

## set_skill_on_ui_comp

method in GameAPI

- 描述

    绑定技能实体到控件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | ability | py.Ability | 技能对象 |
    | comp_name | string | 控件名 |

- 返回值

    无

- 示例

```lua
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)
local player = y3.player.get_by_id(1)

GameAPI.set_skill_on_ui_comp(player.handle, ability.handle, "comp_name")
```

---

## unbind_skill_on_ui_comp

method in GameAPI

- 描述

    解绑技能实体到控件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | ability | py.Ability | 技能对象 |
    | comp_name | string | 控件名 |

- 返回值

    无

- 示例

```lua
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)
local player = y3.player.get_by_id(1)

GameAPI.unbind_skill_on_ui_comp(player.handle, ability.handle, "comp_name")
```

---

## set_ui_comp_opacity

method in GameAPI

- 描述

    设置控件透明度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | opacity | number | 透明度 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_opacity(player.handle, "comp_name", 1.0)
```

---

## set_buff_on_ui_comp

method in GameAPI

- 描述

    绑定对象到BUFF控件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | unit | py.Unit | 单位对象 |
    | comp_name | string | 控件名 |
    | effect? | integer | BUFF效果类型 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

GameAPI.set_buff_on_ui_comp(player.handle, unit.handle, "comp_name", 1)
```

---

## set_item_on_ui_comp

method in GameAPI

- 描述

    绑定物品实体到道具栏控件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | item | py.Item | 物品对象 |
    | comp_name | string | 控件名 |

- 返回值

    无

- 示例

```lua
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)
local player = y3.player.get_by_id(1)

GameAPI.set_item_on_ui_comp(player.handle, item.handle, "comp_name")
```

---

## set_ui_comp_slot

method in GameAPI

- 描述

    设置道具栏控件类型和槽位号

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | slot_type | py.SlotType | 类型 |
    | slot_index | integer | 槽位id |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local slot_type = y3.const.SlotType.BAR

GameAPI.set_ui_comp_slot(player.handle, "comp_name", slot_type, 1)
```

---

## set_ui_comp_unit_slot

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

GameAPI.set_ui_comp_unit_slot(player.handle, "comp_name", unit.handle, slot_type, 1)
```

---

## set_prefab_ui_visible

method in GameAPI

- 描述

    设置预设主界面UI显隐

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | visible | boolean | 显隐 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_prefab_ui_visible(player.handle, true)
```

---

## set_skill_btn_action_effect

method in GameAPI

- 描述

    播放/停止技能按钮激活动效

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | play | boolean | 播放/停止 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_skill_btn_action_effect(player.handle, "comp_name", true)
```

---

## set_btn_short_cut

method in GameAPI

- 描述

    设置按钮快捷键

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | btn | integer | 按键ID |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_btn_short_cut(player.handle, "comp_name", 1)
```

---

## set_btn_func_short_cut

method in GameAPI

- 描述

    设置按钮辅助键

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | btn | integer | 按键ID |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_btn_func_short_cut(player.handle, "comp_name", 1)
```

---

## set_skill_btn_smart_cast_key

method in GameAPI

- 描述

    设置技能按钮智能施法快捷键

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | btn | integer | 按键ID |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_skill_btn_smart_cast_key(player.handle, "comp_name", 1)
```

---

## set_skill_btn_func_smart_cast_key

method in GameAPI

- 描述

    设置技能按钮智能施法辅助键

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | btn | integer | 按键ID |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_skill_btn_func_smart_cast_key(player.handle, "comp_name", 1)
```

---

## set_ui_model_id

method in GameAPI

- 描述

    设置UI模型控件ID

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | model_id | py.Model | 模型id |
    | idle_anim | string | 常态动画 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_model_id(player.handle, "comp_name", 1, "idle_anim")
```

---

## set_shop_comp_bind_shop_unit

method in GameAPI

- 描述

    设置玩家的商店控件的目标商店单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | shop_unit | py.Unit | 商店单位 |
    | index | py.Unit | 页签索引 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

GameAPI.set_shop_comp_bind_shop_unit(player.handle, "comp_name", unit.handle, unit.handle)
```

---

## set_compose_comp_refresh

method in GameAPI

- 描述

    设置玩家的合成控件的参数并刷新

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | item_id | py.ItemID | 合成目标物品id |
    | shop_unit | py.Unit | 商店单位 |
    | buy_unit | py.Unit | 购买单位 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)
local item_id = 134274569

GameAPI.set_compose_comp_refresh(player.handle, "comp_name", item_id, unit.handle, unit.handle)
```

---

## set_show_room_background_color

method in GameAPI

- 描述

    设置ui模型控件背景色

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

GameAPI.set_show_room_background_color(player.handle, "comp_name", 1.0, 1.0, 1.0, 1.0)
```

---

## change_showroom_fov

method in GameAPI

- 描述

    设置Showroom的fov

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | fov | number | fov |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.change_showroom_fov(player.handle, "comp_name", 1.0)
```

---

## change_showroom_cposition

method in GameAPI

- 描述

    设置Showroom的camera pos

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | x | number | x |
    | y | number | y |
    | z | number | z |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.change_showroom_cposition(player.handle, "comp_name", 1.0, 1.0, 1.0)
```

---

## change_showroom_crotation

method in GameAPI

- 描述

    设置Showroom的camera rotation

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | pitch | number | pitch |
    | roll | number | roll |
    | yaw | number | yaw |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.change_showroom_crotation(player.handle, "comp_name", 1.0, 1.0, 1.0)
```

---

## set_ui_comp_rotation

method in GameAPI

- 描述

    设置控件旋转

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | rotation | number | 角度 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_rotation(player.handle, "comp_name", 1.0)
```

---

## set_ui_comp_swallow

method in GameAPI

- 描述

    设置控件是否拦截

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | swallow | boolean | 是否拦截点击 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_swallow(player.handle, "comp_name", true)
```

---

## set_ui_comp_drag

method in GameAPI

- 描述

    设置控件是否可拖动

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | can_drag | boolean | 是否可拖动 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_drag(player.handle, "comp_name", true)
```

---

## set_ui_comp_world_pos

method in GameAPI

- 描述

    设置控件世界坐标

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

GameAPI.set_ui_comp_world_pos(player.handle, "comp_name", 1.0, 1.0)
```

---

## set_ui_comp_world_rotation

method in GameAPI

- 描述

    设置控件世界旋转

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | rotation | number | rotation |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_world_rotation(player.handle, "comp_name", 1.0)
```

---

## set_ui_comp_world_scale

method in GameAPI

- 描述

    设置控件世界缩放

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | scale_x | number | scale_x |
    | scale_y | number | scale_y |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_world_scale(player.handle, "comp_name", 1.0, 1.0)
```

---

## get_ui_comp_pos_x

method in GameAPI

- 描述

    【异步】获取当前玩家控件相对位置x

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | comp_name | string | 控件名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | x |

- 示例

```lua
local result = GameAPI.get_ui_comp_pos_x("comp_name")
```

---

## get_ui_comp_pos_y

method in GameAPI

- 描述

    【异步】获取当前玩家控件相对位置y

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | comp_name | string | 控件名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | y |

- 示例

```lua
local result = GameAPI.get_ui_comp_pos_y("comp_name")
```

---

## get_ui_comp_world_pos_x

method in GameAPI

- 描述

    【异步】获取当前玩家控件绝对位置x

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | comp_name | string | 控件名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | x |

- 示例

```lua
local result = GameAPI.get_ui_comp_world_pos_x("comp_name")
```

---

## get_ui_comp_world_pos_y

method in GameAPI

- 描述

    【异步】获取当前玩家控件绝对位置y

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | comp_name | string | 控件名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | y |

- 示例

```lua
local result = GameAPI.get_ui_comp_world_pos_y("comp_name")
```

---

## get_ui_comp_rotation

method in GameAPI

- 描述

    【异步】获取当前玩家控件相对旋转

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | comp_name | string | 控件名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | rotation |

- 示例

```lua
local result = GameAPI.get_ui_comp_rotation("comp_name")
```

---

## get_ui_comp_world_rotation

method in GameAPI

- 描述

    【异步】获取当前玩家控件绝对旋转

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | comp_name | string | 控件名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | rotation |

- 示例

```lua
local result = GameAPI.get_ui_comp_world_rotation("comp_name")
```

---

## get_ui_comp_scale_x

method in GameAPI

- 描述

    【异步】获取当前玩家控件相对缩放x

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | comp_name | string | 控件名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | scale_x |

- 示例

```lua
local result = GameAPI.get_ui_comp_scale_x("comp_name")
```

---

## get_ui_comp_scale_y

method in GameAPI

- 描述

    【异步】获取当前玩家控件相对缩放y

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | comp_name | string | 控件名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | scale_y |

- 示例

```lua
local result = GameAPI.get_ui_comp_scale_y("comp_name")
```

---

## get_ui_comp_world_scale_x

method in GameAPI

- 描述

    【异步】获取当前玩家控件绝对缩放x

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | comp_name | string | 控件名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | scale_x |

- 示例

```lua
local result = GameAPI.get_ui_comp_world_scale_x("comp_name")
```

---

## get_ui_comp_world_scale_y

method in GameAPI

- 描述

    【异步】获取当前玩家控件绝对缩放y

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | comp_name | string | 控件名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | scale_y |

- 示例

```lua
local result = GameAPI.get_ui_comp_world_scale_y("comp_name")
```

---

## create_ui_comp

method in GameAPI

- 描述

    创建ui控件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 父节点 |
    | comp_type | integer | 控件类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 控件uid |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.create_ui_comp(player.handle, "comp_name", 1)
```

---

## get_ui_comp_id_by_name

method in GameAPI

- 描述

    查找指定名字的UI控件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 节点名字 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 控件uid |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_ui_comp_id_by_name(player.handle, "comp_name")
```

---

## create_ui_comp_event

method in GameAPI

- 描述

    创建并绑定ui控件事件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | event_type | integer | 控件事件类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 事件名 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.create_ui_comp_event(player.handle, "comp_uid", 1)
```

---

## create_ui_comp_event_ex

method in GameAPI

- 描述

    创建并绑定ui控件事件(指定事件名)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | event_type | integer | 控件事件类型 |
    | name | string | 自定义事件名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 事件名 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.create_ui_comp_event_ex(player.handle, "comp_uid", 1, "name")
```

---

## create_ui_comp_event_ex_ex

method in GameAPI

- 描述

    新版创建并绑定ui控件事件(指定事件名),不再传入玩家，同时支持普通控件和动态创建控件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | comp_uid | string | 控件uid |
    | event_type | integer | 控件事件类型 |
    | name | string | 自定义事件名 |
    | user_data | string | 自定义数据 |
    | not_wait_network? | boolean | 不等待网络返回 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 事件名 |

- 示例

```lua
local result = GameAPI.create_ui_comp_event_ex_ex("comp_uid", 1, "name", "user_data", true)
```

---

## create_ui_comp_event_ex_no_check

method in GameAPI

- 描述

    创建并绑定ui控件事件(指定事件名)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | event_type | integer | 控件事件类型 |
    | name | string | 自定义事件名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 事件名 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.create_ui_comp_event_ex_no_check(player.handle, "comp_uid", 1, "name")
```

---

## get_ui_comp_in_scene_ui

method in GameAPI

- 描述

    获取场景ui中的控件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | scene_node_entity | py.SceneNode | 场景点 |
    | comp_path | string | 控件路径 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 控件名 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local unit = player:get_all_units()[1]
local scene_node = GameAPI.create_scene_node_on_unit_ex("comp_name", player.handle, unit.handle, "origin", false)

local result = GameAPI.get_ui_comp_in_scene_ui(scene_node, "comp_path")
```

---

## get_ui_comp_in_scene_ui_ex

method in GameAPI

- 描述

    获取场景ui中的控件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | scene_node_entity | py.SceneNode | 场景点 |
    | comp_uid | string | 模板控件uid |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | uid |

- 示例

```lua
local player = y3.player.get_by_id(1)
local unit = player:get_all_units()[1]
local scene_node = GameAPI.create_scene_node_on_unit_ex("comp_name", player.handle, unit.handle, "origin", false)

local result = GameAPI.get_ui_comp_in_scene_ui_ex(scene_node, "comp_uid")
```

---

## get_comp_by_path

method in GameAPI

- 描述

    通过控件+路径获得ui控件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 父节点 |
    | path | string | 路径 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 控件uid |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_comp_by_path(player.handle, "comp_name", "path")
```

---

## get_comp_by_absolute_path

method in GameAPI

- 描述

    通过绝对路径获得ui控件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | path | string | 路径 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 控件uid |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_comp_by_absolute_path(player.handle, "path")
```

---

## play_ui_comp_fx

method in GameAPI

- 描述

    播放ui动效

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | uid | string | 控件uid |
    | fx_id | integer | 控件动效工程id |
    | ani_name | string | 动效名 |
    | loop? | boolean | 循环 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.play_ui_comp_fx(player.handle, "uid", 1, "ani_name", true)
```

---

## play_ui_model_anim

method in GameAPI

- 描述

    ui模型控件播放动画

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | uid | string | 控件uid |
    | anim | string | 动画名 |
    | play_speed? | number | 动画速率 |
    | begin_t? | number | 开始时间 |
    | end_t? | number | 结束时间 |
    | loop? | boolean | 是否循环 |
    | return_idle? | boolean | 是否回到默认动画 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.play_ui_model_anim(player.handle, "uid", "anim", 1.0, 1.0, 1.0, true, true)
```

---

## set_ui_comp_suspend_image

method in GameAPI

- 描述

    设置ui组件悬浮态图片

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | image_id | integer | 图片id |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_suspend_image(player.handle, "comp_name", 1)
```

---

## set_ui_comp_press_image

method in GameAPI

- 描述

    设置ui组件按下态图片

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | image_id | integer | 图片id |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_press_image(player.handle, "comp_name", 1)
```

---

## set_ui_comp_disabled_image

method in GameAPI

- 描述

    设置ui组件禁用态图片

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | image_id | integer | 图片id |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_disabled_image(player.handle, "comp_name", 1)
```

---

## clear_combo_box

method in GameAPI

- 描述

    清空下拉框

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_id | string | 下拉框 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.clear_combo_box(player.handle, "comp_id")
```

---

## add_combo_item

method in GameAPI

- 描述

    添加下拉框选项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_id | string | 下拉框 |
    | text | string | 名称 |
    | value | string | 值 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.add_combo_item(player.handle, "comp_id", "text", "value")
```

---

## set_combo_text

method in GameAPI

- 描述

    设置下拉框默认文本

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_id | string | 下拉框 |
    | text | string | 默认文本 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_combo_text(player.handle, "comp_id", "text")
```

---

## get_combo_box_cur_value

method in GameAPI

- 描述

    【异步】获取下拉框当前值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | comp_id | string | 下拉框 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | value |

- 示例

```lua
local result = GameAPI.get_combo_box_cur_value("comp_id")
```

---

## get_slider_cur_percent

method in GameAPI

- 描述

    【异步】获取滑动条当前值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | comp_id | string | 滑动条 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | value |

- 示例

```lua
local result = GameAPI.get_slider_cur_percent("comp_id")
```

---

## set_slider_cur_percent

method in GameAPI

- 描述

    设置滑动条当前值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_id | string | 滑动条 |
    | value | number | value |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_slider_cur_percent(player.handle, "comp_id", 1.0)
```

---

## get_ui_comp_width

method in GameAPI

- 描述

    【异步】获得控件宽度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | comp_id | string | UI控件 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | width |

- 示例

```lua
local result = GameAPI.get_ui_comp_width("comp_id")
```

---

## get_ui_comp_height

method in GameAPI

- 描述

    【异步】获得控件高度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | comp_id | string | UI控件 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | height |

- 示例

```lua
local result = GameAPI.get_ui_comp_height("comp_id")
```

---

## set_ui_comp_bar_status

method in GameAPI

- 描述

    设置ui按钮是否开启多态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | is_open | boolean | 是否开启 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_bar_status(player.handle, "comp_name", true)
```

---

## set_ui_model_focus_pos

method in GameAPI

- 描述

    设置UI控件模型焦点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | py.Role | 玩家 |
    | comp_name | string | UI控件 |
    | x | number | x |
    | y | number | y |
    | z | number | z |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_model_focus_pos(player.handle, "comp_name", 1.0, 1.0, 1.0)
```

---

## get_ui_comp_children

method in GameAPI

- 描述

    获取ui控件的子控件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | uid | string | 控件uid |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 子控件uid |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_ui_comp_children(player.handle, "uid")
```

---

## get_ui_comp_children_no_check

method in GameAPI

- 描述

    获取ui控件的子控件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | uid | string | 控件uid |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 子控件uid |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_ui_comp_children_no_check(player.handle, "uid")
```

---

## get_ui_comp_name

method in GameAPI

- 描述

    获取ui控件的名称

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件uid |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 控件名 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_ui_comp_name(player.handle, "comp_name")
```

---

## unbind_ui_comp

method in GameAPI

- 描述

    解绑绑定控件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件uid |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.unbind_ui_comp(player.handle, "comp_name")
```

---

## set_ui_comp_bind_attr

method in GameAPI

- 描述

    绑定单位属性或者全局变量到玩家界面控件的属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | ui_comp | string | 控件uid |
    | ui_comp_attr | string | 控件属性字段 |
    | attr_or_var | string | 属性名 |
    | precision? | integer | 保留小数精度 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_bind_attr(player.handle, "ui_comp", "ui_comp_attr", "attr_or_var", 1)
```

---

## set_ui_comp_bind_var

method in GameAPI

- 描述

    绑定单位属性或者全局变量到玩家界面控件的属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | ui_comp | string | 控件uid |
    | ui_comp_attr | string | 控件属性字段 |
    | attr_or_var | string | 属性名 |
    | precision? | integer | 保留小数精度 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_bind_var(player.handle, "ui_comp", "ui_comp_attr", "attr_or_var", 1)
```

---

## ui_comp_unbind

method in GameAPI

- 描述

    解绑界面控件属性绑定

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | ui_comp | string | 控件uid |
    | ui_comp_attr | string | 控件属性字段 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.ui_comp_unbind(player.handle, "ui_comp", "ui_comp_attr")
```

---

## ui_comp_bind_unit

method in GameAPI

- 描述

    界面控件属性绑定指定单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | ui_comp | string | 控件uid |
    | unit | py.Unit | 单位 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

GameAPI.ui_comp_bind_unit(player.handle, "ui_comp", unit.handle)
```

---

## ui_comp_bind_ctrl_unit

method in GameAPI

- 描述

    界面控件属性动态绑定主控单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | ui_comp | string | 控件uid |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.ui_comp_bind_ctrl_unit(player.handle, "ui_comp")
```

---

## get_ui_comp_parent

method in GameAPI

- 描述

    获取界面控件的父控件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 界面控件 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 父控件 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_ui_comp_parent(player.handle, "comp_uid")
```

---

## set_ui_comp_bind_player_prop

method in GameAPI

- 描述

    绑定玩家属性到玩家界面控件的属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | ui_comp | string | 控件uid |
    | ui_comp_attr | string | 控件属性字段 |
    | bind_role | py.Role | 玩家 |
    | attr_or_var | string | 玩家属性key |
    | precision? | integer | 保留小数精度 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_bind_player_prop(player.handle, "ui_comp", "ui_comp_attr", player.handle, "attr_or_var", 1)
```

---

## set_ui_comp_align

method in GameAPI

- 描述

    设置控件文本对齐方式

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | align_type | integer | 对齐方式 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_align(player.handle, "comp_name", 1)
```

---

## register_ui_comp_fx_cb

method in GameAPI

- 描述

    注册界面控件播放指定动效回调

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | uid | string | 控件uid |
    | fx_id | integer | 控件动效工程id |
    | ani_name | string | 动效名 |
    | frame | integer | 播放动效回调帧数 |
    | handler | string | 回调句柄 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.register_ui_comp_fx_cb(player.handle, "uid", 1, "ani_name", 1, "handler")
```

---

## create_ui_prefab_instance

method in GameAPI

- 描述

    创建界面模块

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | prefab_id | string | 预设uid |
    | comp_name | string | 父控件 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 控件uid |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.create_ui_prefab_instance(player.handle, "prefab_id", "comp_name")
```

---

## del_ui_comp

method in GameAPI

- 描述

    删除界面控件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件uid |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.del_ui_comp(player.handle, "comp_name")
```

---

## set_ui_comp_text_adaptive

method in GameAPI

- 描述

    开启字体大小跟随内容自适应

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件uid |
    | is_open | boolean | 开启/关闭 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_text_adaptive(player.handle, "comp_name", true)
```

---

## set_ui_comp_bind_ability_cd

method in GameAPI

- 描述

    绑定技能cd到玩家界面控件的属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | ui_comp | string | 控件uid |
    | ui_comp_attr | string | 控件属性字段 |
    | ability | py.Ability | 技能实体对象 |
    | is_smooth? | boolean | 是否平滑 |
    | decimal_digits? | integer | 小数位数 |

- 返回值

    无

- 示例

```lua
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_bind_ability_cd(player.handle, "ui_comp", "ui_comp_attr", ability.handle, true, 1)
```

---

## set_ui_comp_bind_modifier_cd

method in GameAPI

- 描述

    绑定魔法效果cd到玩家界面控件的属性

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

GameAPI.set_ui_comp_bind_modifier_cd(player.handle, "ui_comp", "ui_comp_attr", modifier.handle)
```

---

## set_chat_send_enabled

method in GameAPI

- 描述

    开启/禁用发送聊天功能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | ui_comp | string | 控件uid |
    | enabled | boolean | 开关 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_chat_send_enabled(player.handle, "ui_comp", true)
```

---

## set_player_chat_show

method in GameAPI

- 描述

    显示/不显示玩家聊天

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | ui_comp | string | 控件uid |
    | chat_role | py.Role | 玩家 |
    | is_show | boolean | 开关 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_player_chat_show(player.handle, "ui_comp", player.handle, true)
```

---

## clear_player_chat_panel

method in GameAPI

- 描述

    清理聊天

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | ui_comp | string | 控件uid |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.clear_player_chat_panel(player.handle, "ui_comp")
```

---

## send_chat_to_role

method in GameAPI

- 描述

    发送聊天给玩家

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | ui_comp | string | 控件uid |
    | target_role | py.Role | 玩家 |
    | context | string | 内容 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.send_chat_to_role(player.handle, "ui_comp", player.handle, "context")
```

---

## del_ui_prefab

method in GameAPI

- 描述

    删除界面预制实例

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ui_prefab_ins | string | 控件名 |

- 返回值

    无

- 示例

```lua
GameAPI.del_ui_prefab("ui_prefab_ins")
```

---

## get_ui_comp_visible

method in GameAPI

- 描述

    【异步】获得玩家控件显隐性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件uid |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否显示 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_ui_comp_visible(player.handle, "comp_name")
```

---

## set_role_micro_unit

method in GameAPI

- 描述

    设置玩家的声音主单位

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

GameAPI.set_role_micro_unit(player.handle, unit.handle)
```

---

## close_role_micro_unit

method in GameAPI

- 描述

    关闭【玩家】的附近语音聊天

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.close_role_micro_unit(player.handle)
```

---

## set_role_camp_sound_switch

method in GameAPI

- 描述

    设置【玩家】的同阵营语音聊天收听开关为【布尔】

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | is_open | boolean | 开关 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_role_camp_sound_switch(player.handle, true)
```

---

## set_role_camp_micro_switch

method in GameAPI

- 描述

    设置【玩家】的同阵营语音聊天发言开关为【布尔】

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | is_open | boolean | 开关 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_role_camp_micro_switch(player.handle, true)
```

---

## set_nearby_micro_switch

method in GameAPI

- 描述

    设置【玩家】的附近语音聊天发言开关为【布尔】

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | is_open | boolean | 开关 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_nearby_micro_switch(player.handle, true)
```

---

## set_nearby_sound_switch

method in GameAPI

- 描述

    设置【玩家】的附近语音聊天收听开关为【布尔】

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | is_open | boolean | 开关 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_nearby_sound_switch(player.handle, true)
```

---

## set_role_all_sound_switch

method in GameAPI

- 描述

    设置【玩家】的所有人语音聊天收听开关为【布尔】

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | is_open | boolean | 开关 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_role_all_sound_switch(player.handle, true)
```

---

## set_role_all_micro_switch

method in GameAPI

- 描述

    设置【玩家】的所有人语音聊天发言开关为【布尔】

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | is_open | boolean | 开关 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_role_all_micro_switch(player.handle, true)
```

---

## set_ui_comp_chat_channel

method in GameAPI

- 描述

    设置聊天控件的频道为同盟或者所有人

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件uid |
    | is_ally | boolean | 是否为同盟 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_chat_channel(player.handle, "comp_name", true)
```

---

## set_ui_comp_anchor

method in GameAPI

- 描述

    设置界面控件锚点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件uid |
    | x | number | x |
    | y | number | y |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_anchor(player.handle, "comp_name", 1.0, 1.0)
```

---

## set_ui_comp_scale_9_enable

method in GameAPI

- 描述

    设置界面控件九宫开关

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件uid |
    | switch | boolean | 开关 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_scale_9_enable(player.handle, "comp_name", true)
```

---

## set_ui_comp_cap_insets

method in GameAPI

- 描述

    设置界面控件九宫值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件uid |
    | x_left | integer | x |
    | x_right | integer | y |
    | y_top | integer | width |
    | y_bottom | integer | height |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_cap_insets(player.handle, "comp_name", 1, 1, 1, 1)
```

---

## set_ui_comp_bind_format

method in GameAPI

- 描述

    设置ui控件绑定公式

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件名 |
    | format_str | string | 公式 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_bind_format(player.handle, "comp_name", "format_str")
```

---

## set_list_view_percent

method in GameAPI

- 描述

    设置列表滚动到百分比位置

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件uid |
    | percent | number | 百分比 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_list_view_percent(player.handle, "comp_name", 1.0)
```

---

## get_ui_prefab_ins

method in GameAPI

- 描述

    获得玩家的界面模块实例

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | uid | string | 界面模块实例uid |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UIPrefabIns | 界面模块实例 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_ui_prefab_ins(player.handle, "uid")
```

---

## get_ui_comp_prefab

method in GameAPI

- 描述

    获得界面控件所属的界面模块实例(如果是的话)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件uid |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UIPrefabIns | 界面预制体实例 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_ui_comp_prefab(player.handle, "comp_name")
```

---

## set_ui_comp_text_adaptive_min_size

method in GameAPI

- 描述

    设置字体大小跟随内容自适应最小值(需要重新设置文本生效)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | min_value | integer | 最小值 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_text_adaptive_min_size(player.handle, 1)
```

---

## get_ui_prefab_child_by_path

method in GameAPI

- 描述

    通过预制实例+路径获得ui控件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_ins | py.UIPrefabIns | 预制 |
    | path | string | 路径 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 控件uid |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui_prefab_ins = GameAPI.get_ui_prefab_ins(player.handle, "prefab_uid")

local result = GameAPI.get_ui_prefab_child_by_path(ui_prefab_ins, "path")
```

---

## get_input_field_content

method in GameAPI

- 描述

    获得玩家输入框文本内容

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件uid |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 文本内容 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_input_field_content(player.handle, "comp_name")
```

---

## set_ui_comp_anim_pos

method in GameAPI

- 描述

    设置动画移动

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件uid |
    | start_x | number | 开始x |
    | start_y | number | 开始y |
    | end_x | number | 结束x |
    | end_y | number | 结束y |
    | duration | number | 持续时间 |
    | ease_type? | integer | 曲线类型 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_anim_pos(player.handle, "comp_name", 1.0, 1.0, 1.0, 1.0, 1.0, 1)
```

---

## set_ui_comp_anim_opacity

method in GameAPI

- 描述

    设置动画透明度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件uid |
    | start_alpha | number | 开始alpha |
    | end_alpha | number | 结束alpha |
    | duration | number | 持续时间 |
    | ease_type? | integer | 曲线类型 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_anim_opacity(player.handle, "comp_name", 1.0, 1.0, 1.0, 1)
```

---

## set_ui_comp_anim_scale

method in GameAPI

- 描述

    设置动画缩放

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件uid |
    | start_x | number | 开始x |
    | start_y | number | 开始y |
    | end_x | number | 结束x |
    | end_y | number | 结束y |
    | duration | number | 持续时间 |
    | ease_type? | integer | 曲线类型 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_anim_scale(player.handle, "comp_name", 1.0, 1.0, 1.0, 1.0, 1.0, 1)
```

---

## set_ui_comp_anim_rotate

method in GameAPI

- 描述

    设置动画旋转

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件uid |
    | start_rotation | number | 开始旋转 |
    | end_rotation | number | 结束旋转 |
    | duration | number | 持续时间 |
    | ease_type? | integer | 曲线类型 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_anim_rotate(player.handle, "comp_name", 1.0, 1.0, 1.0, 1)
```

---

## create_unit_editor_data

method in GameAPI

- 描述

    创建新单位物编

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | old_entity_no | py.UnitKey | 单位物编 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitKey | 单位物编key |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.create_unit_editor_data(unit_key)
```

---

## set_camera_perspective_ray_unit

method in GameAPI

- 描述

    设置相机透视射线的焦点单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 所属玩家 |
    | unit | py.Unit | 单位 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

GameAPI.set_camera_perspective_ray_unit(player.handle, unit.handle)
```

---

## create_spine

method in GameAPI

- 描述

    create_spine

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ientity | py.Unit | ientity |
    | spine | string | spine |
    | vertical? | boolean | vertical |
    | rate? | number | rate |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.create_spine(unit.handle, "spine", true, 1.0)
```

---

## convert_unit_attr_m2cm

method in GameAPI

- 描述

    单位属性m转cm

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr | string | 属性名 |
    | value | py.Fixed | 属性值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 属性值 |

- 示例

```lua
local result = GameAPI.convert_unit_attr_m2cm("attr", Fix32(1))
```

---

## create_ability_editor_data

method in GameAPI

- 描述

    创建新技能物编

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | old_entity_no | py.AbilityKey | 技能物编 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityKey | 技能物编 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.create_ability_editor_data(ability_key)
```

---

## create_projectile_editor_data

method in GameAPI

- 描述

    创建新投射物物编

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | old_entity_no | py.ProjectileKey | 投射物物编 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileKey | 投射物物编 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.create_projectile_editor_data(projectile_key)
```

---

## create_destructible_editor_data

method in GameAPI

- 描述

    创建新可破坏物物编

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | old_entity_no | py.DestructibleKey | 可破坏物物编 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DestructibleKey | 可破坏物物编 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.create_destructible_editor_data(destructible_key)
```

---

## api_get_editor_type_data

method in GameAPI

- 描述

    获取指定对象类型的物编数据

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | data_type | string | 对象类型 |
    | key | integer | 物编key |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Dict | 物编数据 |

- 示例

```lua
local result = GameAPI.api_get_editor_type_data("data_type", 1)
```

---

## api_set_editor_type_data

method in GameAPI

- 描述

    设置指定对象类型的物编数据

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | data_type | string | 对象类型 |
    | key | integer | 物编key |
    | data | py.Dict | 物编数据 |

- 返回值

    无

- 示例

```lua
local dict = pydict()

GameAPI.api_set_editor_type_data("data_type", 1, dict)
```

---

## api_get_collider_body

method in GameAPI

- 描述

    获取COLLIDER所属的刚体

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | collider | py.Collider | Collider |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RigidBody | Body |

- 示例

```lua
local collider = GameAPI.get_unit_key_collider_kv(1, "key")

local result = GameAPI.api_get_collider_body(collider)
```

---

## api_set_collider_bool_attr

method in GameAPI

- 描述

    设置碰撞体的布尔类型属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | collider | py.RigidBody | 刚体 |
    | attr_name | string | 布尔类型属性 |
    | value | py.Fixed | 值 |

- 返回值

    无

- 示例

```lua
local rigid_body = GameAPI.get_unit_key_rigid_body_kv(1, "key")

GameAPI.api_set_collider_bool_attr(rigid_body, "attr_name", Fix32(1))
```

---

## api_get_collider_bool_attr

method in GameAPI

- 描述

    获取碰撞体的布尔类型属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | collider | py.RigidBody | 刚体 |
    | attr_name | string | 布尔类型属性 |

- 返回值

    无

- 示例

```lua
local rigid_body = GameAPI.get_unit_key_rigid_body_kv(1, "key")

GameAPI.api_get_collider_bool_attr(rigid_body, "attr_name")
```

---

## api_set_collider_float_attr

method in GameAPI

- 描述

    设置碰撞体的实数类型属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | collider | py.RigidBody | 刚体 |
    | attr_name | string | 实数类型属性 |
    | value | boolean | 值 |

- 返回值

    无

- 示例

```lua
local rigid_body = GameAPI.get_unit_key_rigid_body_kv(1, "key")

GameAPI.api_set_collider_float_attr(rigid_body, "attr_name", true)
```

---

## api_is_collider_collision_category

method in GameAPI

- 描述

    碰撞器的自身碰撞类别是否有指定类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | collider | py.Collider | 碰撞器 |
    | mask | py.Fixed | mask |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 布尔值 |

- 示例

```lua
local collider = GameAPI.get_unit_key_collider_kv(1, "key")

local result = GameAPI.api_is_collider_collision_category(collider, Fix32(1))
```

---

## api_is_collider_collide_with_mask

method in GameAPI

- 描述

    碰撞器的目标碰撞类别是否有指定类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | collider | py.Collider | 碰撞器 |
    | mask | py.Fixed | mask |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 布尔值 |

- 示例

```lua
local collider = GameAPI.get_unit_key_collider_kv(1, "key")

local result = GameAPI.api_is_collider_collide_with_mask(collider, Fix32(1))
```

---

## api_is_collider_collision_category_player

method in GameAPI

- 描述

    碰撞器的自身碰撞类别是否有玩家

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | collider | py.Collider | 碰撞器 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 布尔值 |

- 示例

```lua
local collider = GameAPI.get_unit_key_collider_kv(1, "key")

local result = GameAPI.api_is_collider_collision_category_player(collider)
```

---

## api_is_collider_collision_category_floor

method in GameAPI

- 描述

    碰撞器的自身碰撞类别是否有地面

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | collider | py.Collider | 碰撞器 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 布尔值 |

- 示例

```lua
local collider = GameAPI.get_unit_key_collider_kv(1, "key")

local result = GameAPI.api_is_collider_collision_category_floor(collider)
```

---

## api_get_collider_collision_category

method in GameAPI

- 描述

    获得碰撞器的自身碰撞类别

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | collider | py.Collider | 碰撞器 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | mask |

- 示例

```lua
local collider = GameAPI.get_unit_key_collider_kv(1, "key")

local result = GameAPI.api_get_collider_collision_category(collider)
```

---

## api_get_collider_collide_with_mask

method in GameAPI

- 描述

    获得碰撞器的目标碰撞类别

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | collider | py.Collider | 碰撞器 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | mask |

- 示例

```lua
local collider = GameAPI.get_unit_key_collider_kv(1, "key")

local result = GameAPI.api_get_collider_collide_with_mask(collider)
```

---

## api_set_collider_collision_category

method in GameAPI

- 描述

    设置碰撞器的自身碰撞类别

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | collider | py.Collider | 碰撞器 |
    | mask | integer | mask |

- 返回值

    无

- 示例

```lua
local collider = GameAPI.get_unit_key_collider_kv(1, "key")

GameAPI.api_set_collider_collision_category(collider, 1)
```

---

## api_set_collider_collide_with_mask

method in GameAPI

- 描述

    获得碰撞器的目标碰撞类别

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | collider | py.Collider | 碰撞器 |
    | mask | integer | mask |

- 返回值

    无

- 示例

```lua
local collider = GameAPI.get_unit_key_collider_kv(1, "key")

GameAPI.api_set_collider_collide_with_mask(collider, 1)
```

---

## api_get_joint_by_bid

method in GameAPI

- 描述

    根据jid获取joint

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | jid | integer | joint ID |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Joint | Joint |

- 示例

```lua
local result = GameAPI.api_get_joint_by_bid(1)
```

---

## api_create_fixed_joint

method in GameAPI

- 描述

    创建固定关节

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | pos | py.FVector3 | 创建位置 |
    | body_1 | py.RigidBody | 刚体 |
    | body_2 | py.RigidBody | 刚体 |
    | enable_collision? | boolean | 检测碰撞 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RigidBody | Body |

- 示例

```lua
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))
local rigid_body = GameAPI.get_unit_key_rigid_body_kv(1, "key")

local result = GameAPI.api_create_fixed_joint(fvector3, rigid_body, rigid_body, true)
```

---

## api_destroy_joint

method in GameAPI

- 描述

    销毁关节

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | joint | py.Joint | 关节 |

- 返回值

    无

- 示例

```lua
local joint = GameAPI.get_unit_key_joint_kv(1, "key")

GameAPI.api_destroy_joint(joint)
```

---

## api_get_physics_entity_by_id

method in GameAPI

- 描述

    根据id获取逻辑物理组件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | id | integer | 物理组件id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsEntity | PhysicsEntity |

- 示例

```lua
local result = GameAPI.api_get_physics_entity_by_id(1)
```

---

## api_get_physics_object_by_id

method in GameAPI

- 描述

    根据id获取物理组件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | comp_id | integer | joint ID |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsObject | PhysicsObject |

- 示例

```lua
local result = GameAPI.api_get_physics_object_by_id(1)
```

---

## api_get_rigid_body_in_physics_entity

method in GameAPI

- 描述

    根据名称获取逻辑物理组件中的rigidbody

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | entity | py.PhysicsEntity | 物理组件 |
    | name | string | 名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RigidBody | RigidBody |

- 示例

```lua
local physics_entity = GameAPI.get_unit_key_physics_entity_kv(1, "key")

local result = GameAPI.api_get_rigid_body_in_physics_entity(physics_entity, "name")
```

---

## api_get_unit_or_physics_entity_pos

method in GameAPI

- 描述

    获取单位或者物理组件的位置

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Actor | 单位或物理组件 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3 | Position |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.api_get_unit_or_physics_entity_pos(actor)
```

---

## api_physics_raycast

method in GameAPI

- 描述

    射线检测

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | start_point | py.FVector3 | 起点 |
    | end_point | py.FVector3 | 终点 |
    | query_filter? | py.PhysicsFilter | 过滤器 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RigidBodyGroup | 是否有重叠 |

- 示例

```lua
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))
local physics_filter = GameAPI.api_create_physics_filter(1, 1, false, false, false, false, false)

local result = GameAPI.api_physics_raycast(fvector3, fvector3)
```

---

## api_get_physics_raycast_first_point

method in GameAPI

- 描述

    获得射线检测首次碰撞点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | start_point | py.FVector3 | 起点 |
    | end_point | py.FVector3 | 终点 |
    | query_filter? | py.PhysicsFilter | 过滤器 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3 | 碰撞点 |

- 示例

```lua
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))
local physics_filter = GameAPI.api_create_physics_filter(1, 1, false, false, false, false, false)

local result = GameAPI.api_get_physics_raycast_first_point(fvector3, fvector3)
```

---

## api_set_physics_object_activated_and_visible

method in GameAPI

- 描述

    设置物理组件可见性(以及是否为生效状态)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_object_id | py.Actor | 物理组件 |
    | is_visible | boolean | 是否可见 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.api_set_physics_object_activated_and_visible(actor, true)
```

---

## api_set_physics_entity_activated_and_visible

method in GameAPI

- 描述

    设置逻辑物理组件可见性(以及是否为生效状态)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | entity | py.Actor | 物理组件 |
    | is_visible | boolean | 是否可见 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.api_set_physics_entity_activated_and_visible(actor, true)
```

---

## api_check_physics_is_overlapping

method in GameAPI

- 描述

    单位/逻辑物理组件之间是否有重叠

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | entity_1 | py.Actor | 单位/逻辑物理组件 |
    | entity_2 | py.Actor | 单位/逻辑物理组件 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否有重叠 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.api_check_physics_is_overlapping(actor, actor)
```

---

## api_check_physics_is_contacting

method in GameAPI

- 描述

    单位/逻辑物理组件之间是否有碰撞

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | entity_1 | py.Actor | 单位/逻辑物理组件 |
    | entity_2 | py.Actor | 单位/逻辑物理组件 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否有重叠 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.api_check_physics_is_contacting(actor, actor)
```

---

## api_create_physics_object

method in GameAPI

- 描述

    创建物理组件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_object_id | py.PhysicsObjectKey | 物理组件类型 |
    | translation | py.FVector3 | 位置 |
    | direction | py.FVector3 | 朝向 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsObject | 物理组件 |

- 示例

```lua
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

local result = GameAPI.api_create_physics_object(1, fvector3, fvector3)
```

---

## api_create_physics_entity

method in GameAPI

- 描述

    创建逻辑物理组件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_id | py.PhysicsObjectKey | 物理组件类型 |
    | translation | py.FVector3 | 位置 |
    | direction | py.FVector3 | 朝向 |
    | scale? | py.Fixed | 缩放 |

- 返回值

    无

- 示例

```lua
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

GameAPI.api_create_physics_entity(1, fvector3, fvector3, Fix32(1))
```

---

## api_del_physics_object

method in GameAPI

- 描述

    删除物理组件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_object_id | py.Actor | 逻辑物理组件 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.api_del_physics_object(actor)
```

---

## api_del_physics_entity

method in GameAPI

- 描述

    删除逻辑物理组件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity | py.Actor | 逻辑物理组件 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.api_del_physics_entity(actor)
```

---

## api_physics_entity_is_exist

method in GameAPI

- 描述

    逻辑物理组件是否存在

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | entity? | py.PhysicsEntity | 逻辑物理组件 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 布尔值 |

- 示例

```lua
local physics_entity = GameAPI.get_unit_key_physics_entity_kv(1, "key")

local result = GameAPI.api_physics_entity_is_exist()
```

---

## api_physics_play_animation

method in GameAPI

- 描述

    逻辑物理组件中指定刚体的模型播放动画

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | entity | py.PhysicsEntity | 物理组件 |
    | body | py.RigidBody | 刚体 |
    | anim_name | string | 动画名称 |
    | loop? | boolean | 是否循环 |
    | play_speed? | py.Fixed | 速度 |

- 返回值

    无

- 示例

```lua
local physics_entity = GameAPI.get_unit_key_physics_entity_kv(1, "key")
local rigid_body = GameAPI.get_unit_key_rigid_body_kv(1, "key")

GameAPI.api_physics_play_animation(physics_entity, rigid_body, "anim_name", true, Fix32(1))
```

---

## api_get_physics_entity_state

method in GameAPI

- 描述

    获得逻辑物理组件的状态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | entity | py.PhysicsEntity | 物理组件 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsEntityState | 状态 |

- 示例

```lua
local physics_entity = GameAPI.get_unit_key_physics_entity_kv(1, "key")

local result = GameAPI.api_get_physics_entity_state(physics_entity)
```

---

## api_set_entity_state

method in GameAPI

- 描述

    设置逻辑物理组件状态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | entity | py.PhysicsEntity | 物理组件 |
    | state | py.PhysicsEntityState | 状态 |

- 返回值

    无

- 示例

```lua
local physics_entity = GameAPI.get_unit_key_physics_entity_kv(1, "key")

GameAPI.api_set_entity_state(physics_entity, 1)
```

---

## api_set_entity_active

method in GameAPI

- 描述

    设置逻辑物理组件的激活状态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | entity | py.PhysicsEntity | 物理组件 |
    | is_active | boolean | 激活状态 |
    | visible? | boolean | 可见性 |

- 返回值

    无

- 示例

```lua
local physics_entity = GameAPI.get_unit_key_physics_entity_kv(1, "key")

GameAPI.api_set_entity_active(physics_entity, true, true)
```

---

## api_is_physics_entity_active

method in GameAPI

- 描述

    判断逻辑物理组件是激活状态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | entity | py.PhysicsEntity | 物理组件 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 激活状态 |

- 示例

```lua
local physics_entity = GameAPI.get_unit_key_physics_entity_kv(1, "key")

local result = GameAPI.api_is_physics_entity_active(physics_entity)
```

---

## api_is_physics_entity_deactive

method in GameAPI

- 描述

    判断逻辑物理组件是关闭状态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | entity | py.PhysicsEntity | 物理组件 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 关闭状态 |

- 示例

```lua
local physics_entity = GameAPI.get_unit_key_physics_entity_kv(1, "key")

local result = GameAPI.api_is_physics_entity_deactive(physics_entity)
```

---

## api_get_physics_entity

method in GameAPI

- 描述

    根据id获得逻辑物理组件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | entity_id | py.Fixed | id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsEntity | 逻辑物理组件 |

- 示例

```lua
local result = GameAPI.api_get_physics_entity(Fix32(1))
```

---

## api_set_gravity

method in GameAPI

- 描述

    设置重力加速度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | gravity | py.FVector3 | 重力加速度 |

- 返回值

    无

- 示例

```lua
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

GameAPI.api_set_gravity(fvector3)
```

---

## api_create_sfx_on_rigid

method in GameAPI

- 描述

    创建特效到逻辑物理组件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | entity | py.PhysicsEntity | 逻辑物理组件 |
    | body_name | string | 刚体名称 |
    | sfx_id | py.Fixed | 特效ID |
    | b_follow_rotate? | boolean | 是否跟随旋转 |
    | b_follow_scale? | boolean | 是否跟随缩放 |
    | position? | py.Vector3 | 偏移 |
    | scale? | py.Fixed | 缩放 |
    | rotation? | py.Vector3 | 旋转 |
    | duration? | py.Fixed | 持续时间 |
    | immediately? | boolean | 是否播放完移除 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sfx | 特效 |

- 示例

```lua
local physics_entity = GameAPI.get_unit_key_physics_entity_kv(1, "key")
local vector3 = Fix32Vec3(0, 0, 0)

local result = GameAPI.api_create_sfx_on_rigid(physics_entity, "body_name", Fix32(1), true, true, nil, Fix32(1), nil, Fix32(1), true)
```

---

## api_get_physics_entity_type

method in GameAPI

- 描述

    获取逻辑物理组件类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | entity | py.PhysicsEntity | 逻辑物理组件 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 类型 |

- 示例

```lua
local physics_entity = GameAPI.get_unit_key_physics_entity_kv(1, "key")

local result = GameAPI.api_get_physics_entity_type(physics_entity)
```

---

## api_destroy_physics_entity

method in GameAPI

- 描述

    销毁逻辑物理组件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | entity | py.PhysicsEntity | 逻辑物理组件 |

- 返回值

    无

- 示例

```lua
local physics_entity = GameAPI.get_unit_key_physics_entity_kv(1, "key")

GameAPI.api_destroy_physics_entity(physics_entity)
```

---

## api_physics_entity_set_orientation

method in GameAPI

- 描述

    设置逻辑物理组件旋转（欧拉角）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | entity | py.PhysicsEntity | 逻辑物理组件 |
    | rotation | py.FRotation | 欧拉角 |

- 返回值

    无

- 示例

```lua
local physics_entity = GameAPI.get_unit_key_physics_entity_kv(1, "key")

GameAPI.api_physics_entity_set_orientation(physics_entity, GlobalAPI.vector3_to_euler(Fix32Vec3(0, 0, 0)))
```

---

## api_physics_entity_has_tag

method in GameAPI

- 描述

    逻辑物理组件是否有指定tag

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | entity | py.PhysicsEntity | 逻辑物理组件 |
    | tag | string | tag |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 布尔值 |

- 示例

```lua
local physics_entity = GameAPI.get_unit_key_physics_entity_kv(1, "key")

local result = GameAPI.api_physics_entity_has_tag(physics_entity, "tag")
```

---

## api_physics_entity_add_tag

method in GameAPI

- 描述

    逻辑物理组件添加tag

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | entity | py.PhysicsEntity | 逻辑物理组件 |
    | tag | string | tag |

- 返回值

    无

- 示例

```lua
local physics_entity = GameAPI.get_unit_key_physics_entity_kv(1, "key")

GameAPI.api_physics_entity_add_tag(physics_entity, "tag")
```

---

## api_physics_entity_remove_tag

method in GameAPI

- 描述

    逻辑物理组件删除tag

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | entity | py.PhysicsEntity | 逻辑物理组件 |
    | tag | string | tag |

- 返回值

    无

- 示例

```lua
local physics_entity = GameAPI.get_unit_key_physics_entity_kv(1, "key")

GameAPI.api_physics_entity_remove_tag(physics_entity, "tag")
```

---

## api_world_pos_to_camera_pos

method in GameAPI

- 描述

    世界坐标转换屏幕坐标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | world_pos | py.Vector3 | 世界坐标 |

- 返回值

    无

- 示例

```lua
local vector3 = Fix32Vec3(0, 0, 0)

GameAPI.api_world_pos_to_camera_pos(vector3)
```

---

## api_world_pos_to_screen_edge_pos

method in GameAPI

- 描述

    世界坐标转换屏幕边缘坐标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | world_pos | py.Vector3 | 世界坐标 |
    | delta_dis | py.Fixed | 定点数 |

- 返回值

    无

- 示例

```lua
local vector3 = Fix32Vec3(0, 0, 0)

GameAPI.api_world_pos_to_screen_edge_pos(vector3, Fix32(1))
```

---

## api_create_physics_filter

method in GameAPI

- 描述

    创建物理过滤器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | collision_category | integer | 自身碰撞标签 |
    | collide_with_mask | integer | 目标碰撞标签 |
    | ignore_trigger | boolean | 是否忽略触发器 |
    | ignore_non_trigger | boolean | 是否忽略非触发器 |
    | ignore_static_rb | boolean | 是否忽略静态刚体 |
    | ignore_dynamic_rb | boolean | 是否忽略动态刚体 |
    | ignore_kinematic_rb | boolean | 是否忽略运动学刚体 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsFilter | 过滤器 |

- 示例

```lua
local result = GameAPI.api_create_physics_filter(1, 1, true, true, true, true, true)
```

---

## api_get_rigid_body_in_unit

method in GameAPI

- 描述

    获取单位的rigidBody

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RigidBody | RigidBody |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = GameAPI.api_get_rigid_body_in_unit(unit.handle)
```

---

## set_physics_ctrl_unit

method in GameAPI

- 描述

    设置物理主控单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | ragdoll_collide? | boolean | Ragdoll是否碰撞 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.set_physics_ctrl_unit(unit.handle, true)
```

---

## get_physics_ctrl_unit

method in GameAPI

- 描述

    获取物理主控单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 单位 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_physics_ctrl_unit(player.handle)
```

---

## api_set_cc_visibility

method in GameAPI

- 描述

    设置主控单位可见性visual

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | is_visible | boolean | 可见性 |
    | only_self? | boolean | 仅自己生效 |
    | only_self_friend? | boolean | 仅自己和友军生效 |
    | only_enemy? | boolean | 仅对敌军生效 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.api_set_cc_visibility(unit.handle, true, true, true, true)
```

---

## create_unit_at_vector3

method in GameAPI

- 描述

    创建单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | py.UnitKey | 单位编号 |
    | location | py.FVector3 | 位置 |
    | direction | py.FVector3 | 朝向 |
    | role_or_unit | py.Role | 所属玩家 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 创建出的单位 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local unit_key = 134274569
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

local result = GameAPI.create_unit_at_vector3(unit_key, fvector3, fvector3, player.handle)
```

---

## api_unit_transmit_3d

method in GameAPI

- 描述

    单位传送到指定坐标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | position | py.FVector3 | 目标坐标 |
    | clear_speed | boolean | 是否清除速度 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

GameAPI.api_unit_transmit_3d(unit.handle, fvector3, true)
```

---

## api_revive_unit_3d

method in GameAPI

- 描述

    复活单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | position | py.FVector3 | 复活位置 |
    | clear_speed | boolean | 清除速度 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

GameAPI.api_revive_unit_3d(unit.handle, fvector3, true)
```

---

## api_get_character_state_name

method in GameAPI

- 描述

    获取角色所处状态机节点名称

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 状态机节点名称 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = GameAPI.api_get_character_state_name(unit.handle)
```

---

## cc_look_at_camera

method in GameAPI

- 描述

    让单位lookat镜头

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.cc_look_at_camera(unit.handle)
```

---

## cc_look_at_other_unit

method in GameAPI

- 描述

    让单位lookat目标单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | other_unit | py.Unit | 单位 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.cc_look_at_other_unit(unit.handle, unit.handle)
```

---

## cc_cancel_look_at

method in GameAPI

- 描述

    取消单位lookat

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.cc_cancel_look_at(unit.handle)
```

---

## cc_get_random_unit_around

method in GameAPI

- 描述

    获取单位周围的随机单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | radius | py.Fixed | 距离 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 随机单位 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = GameAPI.cc_get_random_unit_around(unit.handle, Fix32(1))
```

---

## api_check_asm_state

method in GameAPI

- 描述

    动画状态机状态判断

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | state1 | py.CcAsmState | 动画机状态 |
    | state2 | py.CcAsmState | 动画机状态 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否相等 |

- 示例

```lua
local result = GameAPI.api_check_asm_state(1, 1)
```

---

## api_get_grab_character

method in GameAPI

- 描述

    获取单位碰撞盒里最近的抓取单位（测试用）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 距离最近的单位 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = GameAPI.api_get_grab_character(unit.handle)
```

---

## api_grab

method in GameAPI

- 描述

    抓取技能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | source | py.Unit | 施法单位 |
    | target | py.Unit | 目标单位 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.api_grab(unit.handle, unit.handle)
```

---

## check_catch_other_character

method in GameAPI

- 描述

    判断 - 是否可以施放暴揍技能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | source | py.Unit | 施法单位 |
    | target | py.Unit | 目标单位 |
    | bind | string | 绑点名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否可以施放 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = GameAPI.check_catch_other_character(unit.handle, unit.handle, "bind")
```

---

## api_physics_catch

method in GameAPI

- 描述

    暴揍技能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | source | py.Unit | 施法单位 |
    | target | py.Unit | 目标单位 |
    | state | integer | 暴揍动作 |
    | duration | py.Fixed | 持续时间 |
    | bind | string | 绑点名称 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.api_physics_catch(unit.handle, unit.handle, 1, Fix32(1), "bind")
```

---

## api_disconnect_hand

method in GameAPI

- 描述

    移除手部黏连状态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | handtype | py.CcHandID | 左手/右手 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.api_disconnect_hand(unit.handle, 1)
```

---

## api_disconnect_both_hands

method in GameAPI

- 描述

    移除双手的黏连状态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.api_disconnect_both_hands(unit.handle)
```

---

## api_check_hand_connection

method in GameAPI

- 描述

    检查手部是否处于黏连状态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | handtype | py.CcHandID | 左手/右手 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否黏连 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = GameAPI.api_check_hand_connection(unit.handle, 1)
```

---

## cc_do_predefined_action

method in GameAPI

- 描述

    主控角色做预定义行为

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 角色 |
    | cc_action | py.CcActionID | 预定义行为ID |
    | cc_hand? | py.CcHandID | 左手/右手 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.cc_do_predefined_action(unit.handle, 1, 1)
```

---

## api_override_anim_status

method in GameAPI

- 描述

    重载角色动画状态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 角色 |
    | anim_status | py.CcAnimationMachineStatus | 动画机节点名字 |
    | anim_name | string | 动画名 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local cc_anim_status = "anim"

GameAPI.api_override_anim_status(unit.handle, cc_anim_status, "anim_name")
```

---

## is_upper_body_limited

method in GameAPI

- 描述

    判断单位上半身行动受限

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否受限 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = GameAPI.is_upper_body_limited(unit.handle)
```

---

## api_physics_throw

method in GameAPI

- 描述

    投掷技能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 施法单位 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.api_physics_throw(unit.handle)
```

---

## api_physics_pick_up

method in GameAPI

- 描述

    拾取物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 施法单位 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.api_physics_pick_up(unit.handle)
```

---

## api_physics_pick_up_item

method in GameAPI

- 描述

    拾取指定物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | item | py.Unit | 物品 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.api_physics_pick_up_item(unit.handle, unit.handle)
```

---

## api_physics_drop

method in GameAPI

- 描述

    单位丢弃物理道具

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.api_physics_drop(unit.handle)
```

---

## api_physics_hit_down_unit

method in GameAPI

- 描述

    施加倒地状态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 施加目标 |
    | duration | py.Fixed | 持续时间 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.api_physics_hit_down_unit(unit.handle, Fix32(1))
```

---

## api_get_grab_unit

method in GameAPI

- 描述

    获取抓举单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.api_get_grab_unit(unit.handle)
```

---

## api_check_grab_state

method in GameAPI

- 描述

    检查是否处于抓举状态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否处于抓举状态 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = GameAPI.api_check_grab_state(unit.handle)
```

---

## api_get_pick_item

method in GameAPI

- 描述

    获取手持物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.api_get_pick_item(unit.handle)
```

---

## api_check_physics_unit_pick_item_exist

method in GameAPI

- 描述

    检查是否手持物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否手持物品 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = GameAPI.api_check_physics_unit_pick_item_exist(unit.handle)
```

---

## api_add_unit_down_value

method in GameAPI

- 描述

    增加击倒值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | down_value | py.Fixed | 击倒值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.api_add_unit_down_value(unit.handle, Fix32(1))
```

---

## api_character_try_begin_use

method in GameAPI

- 描述

    开始使用手持道具

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.api_character_try_begin_use(unit.handle)
```

---

## api_character_try_end_use

method in GameAPI

- 描述

    结束使用手持道具

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.api_character_try_end_use(unit.handle)
```

---

## api_set_entity_anim_state_machine_physics

method in GameAPI

- 描述

    设置动画状态机为物理状态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | duration | py.Fixed | 持续时间 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.api_set_entity_anim_state_machine_physics(unit.handle, Fix32(1))
```

---

## api_physics_unit_get_move_speed

method in GameAPI

- 描述

    获取角色移动速度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3 | 速度 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = GameAPI.api_physics_unit_get_move_speed(unit.handle)
```

---

## api_physics_unit_set_orientation

method in GameAPI

- 描述

    设置单位旋转（欧拉角）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | rotation | py.FRotation | X |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.api_physics_unit_set_orientation(unit.handle, GlobalAPI.vector3_to_euler(Fix32Vec3(0, 0, 0)))
```

---

## cc_change_emo

method in GameAPI

- 描述

    主控角色做预定义表情

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 角色 |
    | cc_emo | py.CcEmo | 预定义表情ID |
    | duration | py.Fixed | 表情播放时长 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.cc_change_emo(unit.handle, 1, Fix32(1))
```

---

## api_asm_jump_to_state

method in GameAPI

- 描述

    单位切换状态机

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | state_name | string | 状态机名称 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.api_asm_jump_to_state(unit.handle, "state_name")
```

---

## api_set_unit_squash

method in GameAPI

- 描述

    设置角色squash

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 角色 |
    | squash | py.Fixed | squash |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.api_set_unit_squash(unit.handle, Fix32(1))
```

---

## api_set_unit_move

method in GameAPI

- 描述

    设置单位移动

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | move_direction | py.MoveDirection | 方向 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.api_set_unit_move(unit.handle, 1)
```

---

## api_set_unit_stop_move

method in GameAPI

- 描述

    设置单位停止移动

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | move_direction | py.MoveDirection | 方向 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.api_set_unit_stop_move(unit.handle, 1)
```

---

## api_notify_custom_key

method in GameAPI

- 描述

    通知改键

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | enable | boolean | 是否使用 |

- 返回值

    无

- 示例

```lua
GameAPI.api_notify_custom_key(true)
```

---

## api_set_unit_jump

method in GameAPI

- 描述

    设置单位跳跃

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.api_set_unit_jump(unit.handle)
```

---

## api_set_unit_run

method in GameAPI

- 描述

    设置单位跑(角色配置的跑步速度)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.api_set_unit_run(unit.handle)
```

---

## api_set_unit_walk

method in GameAPI

- 描述

    设置单位走(角色配置的走路速度)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.api_set_unit_walk(unit.handle)
```

---

## api_set_unit_speed

method in GameAPI

- 描述

    设置单位速度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | speed | py.Fixed | 速度 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.api_set_unit_speed(unit.handle, Fix32(1))
```

---

## api_set_audio_cc

method in GameAPI

- 描述

    设置语音指令

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_on | boolean | 是否开启 |

- 返回值

    无

- 示例

```lua
GameAPI.api_set_audio_cc(true)
```

---

## api_get_rigid_body_by_bid

method in GameAPI

- 描述

    根据bid获取rigidBody

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | bid | integer | body ID |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RigidBody | RigidBody |

- 示例

```lua
local result = GameAPI.api_get_rigid_body_by_bid(1)
```

---

## api_add_sphere_collider

method in GameAPI

- 描述

    刚体添加球形碰撞器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | body | py.RigidBody | 刚体 |
    | pos | py.FVector3 | pos |
    | radius | py.Fixed | radius |
    | euler_angle? | py.FVector3 | euler_angle |
    | is_trigger? | boolean | is_trigger |

- 返回值

    无

- 示例

```lua
local rigid_body = GameAPI.get_unit_key_rigid_body_kv(1, "key")
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

GameAPI.api_add_sphere_collider(rigid_body, fvector3, Fix32(1), nil, true)
```

---

## api_get_rigid_body_in_physics_object

method in GameAPI

- 描述

    根据名称获取物理组件中的rigidbody

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_object | py.PhysicsEntity | 物理组件 |
    | name | string | 名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RigidBody | RigidBody |

- 示例

```lua
local physics_entity = GameAPI.get_unit_key_physics_entity_kv(1, "key")

local result = GameAPI.api_get_rigid_body_in_physics_object(physics_entity, "name")
```

---

## api_get_rigid_body_owner_unit

method in GameAPI

- 描述

    获取刚体所属的单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | body | py.RigidBody | 刚体 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | Owner |

- 示例

```lua
local rigid_body = GameAPI.get_unit_key_rigid_body_kv(1, "key")

local result = GameAPI.api_get_rigid_body_owner_unit(rigid_body)
```

---

## api_get_rigid_body_owner_physics_entity

method in GameAPI

- 描述

    获取刚体所属的逻辑物理组件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | body | py.RigidBody | 刚体 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PhysicsEntity | Owner |

- 示例

```lua
local rigid_body = GameAPI.get_unit_key_rigid_body_kv(1, "key")

local result = GameAPI.api_get_rigid_body_owner_physics_entity(rigid_body)
```

---

## api_add_force_to_rigid_body

method in GameAPI

- 描述

    向刚体施加力

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | body | py.RigidBody | 刚体 |
    | force | py.Fixed | 力度 |
    | direction | py.FVector3 | 方向 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RigidBody | RigidBody |

- 示例

```lua
local rigid_body = GameAPI.get_unit_key_rigid_body_kv(1, "key")
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

local result = GameAPI.api_add_force_to_rigid_body(rigid_body, Fix32(1), fvector3)
```

---

## api_add_velocity_to_rigid_body

method in GameAPI

- 描述

    给刚体叠加速度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | body | py.RigidBody | 刚体 |
    | speed | py.Fixed | 速度的大小 |
    | direction | py.FVector3 | 速度的方向 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RigidBody | RigidBody |

- 示例

```lua
local rigid_body = GameAPI.get_unit_key_rigid_body_kv(1, "key")
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

local result = GameAPI.api_add_velocity_to_rigid_body(rigid_body, Fix32(1), fvector3)
```

---

## api_get_rigid_body_pos

method in GameAPI

- 描述

    获取刚体的位置

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | body | py.RigidBody | 刚体 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3 | Position |

- 示例

```lua
local rigid_body = GameAPI.get_unit_key_rigid_body_kv(1, "key")

local result = GameAPI.api_get_rigid_body_pos(rigid_body)
```

---

## api_set_rigid_body_pos

method in GameAPI

- 描述

    设置刚体的位置

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | body | py.RigidBody | 刚体 |
    | pos | py.FVector3 | pos |

- 返回值

    无

- 示例

```lua
local rigid_body = GameAPI.get_unit_key_rigid_body_kv(1, "key")
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

GameAPI.api_set_rigid_body_pos(rigid_body, fvector3)
```

---

## api_set_rigid_body_direction

method in GameAPI

- 描述

    设置刚体的朝向

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | body | py.RigidBody | 刚体 |
    | direction | py.FRotation | direction |

- 返回值

    无

- 示例

```lua
local rigid_body = GameAPI.get_unit_key_rigid_body_kv(1, "key")

GameAPI.api_set_rigid_body_direction(rigid_body, GlobalAPI.vector3_to_euler(Fix32Vec3(0, 0, 0)))
```

---

## api_set_rigid_body_type

method in GameAPI

- 描述

    设置刚体的刚体类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | body | py.RigidBody | 刚体 |
    | body_type | string | 刚体类型 |

- 返回值

    无

- 示例

```lua
local rigid_body = GameAPI.get_unit_key_rigid_body_kv(1, "key")

GameAPI.api_set_rigid_body_type(rigid_body, "body_type")
```

---

## api_set_rigid_body_bool_attr

method in GameAPI

- 描述

    设置刚体的布尔类型属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | body | py.RigidBody | 刚体 |
    | attr_name | string | 布尔类型属性 |
    | value | boolean | 值 |

- 返回值

    无

- 示例

```lua
local rigid_body = GameAPI.get_unit_key_rigid_body_kv(1, "key")

GameAPI.api_set_rigid_body_bool_attr(rigid_body, "attr_name", true)
```

---

## api_set_rigidbody_active

method in GameAPI

- 描述

    设置刚体有效性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | body | py.RigidBody | 刚体 |
    | is_active | boolean | 是否有效 |

- 返回值

    无

- 示例

```lua
local rigid_body = GameAPI.get_unit_key_rigid_body_kv(1, "key")

GameAPI.api_set_rigidbody_active(rigid_body, true)
```

---

## api_set_rigidbody_visible

method in GameAPI

- 描述

    设置刚体模型可见性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | body | py.PhysicsEntity | 物理组件 |
    | visible | py.RigidBody | 刚体 |

- 返回值

    无

- 示例

```lua
local physics_entity = GameAPI.get_unit_key_physics_entity_kv(1, "key")
local rigid_body = GameAPI.get_unit_key_rigid_body_kv(1, "key")

GameAPI.api_set_rigidbody_visible(physics_entity, rigid_body)
```

---

## api_get_rigidbody_active

method in GameAPI

- 描述

    获取刚体有效性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | body | py.RigidBody | 刚体 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否有效 |

- 示例

```lua
local rigid_body = GameAPI.get_unit_key_rigid_body_kv(1, "key")

local result = GameAPI.api_get_rigidbody_active(rigid_body)
```

---

## api_set_rigidbody_velocity

method in GameAPI

- 描述

    设置刚体速度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | body | py.RigidBody | 刚体 |
    | speed | py.Fixed | 速度大小 |
    | direction | py.FVector3 | 速度方向 |

- 返回值

    无

- 示例

```lua
local rigid_body = GameAPI.get_unit_key_rigid_body_kv(1, "key")
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

GameAPI.api_set_rigidbody_velocity(rigid_body, Fix32(1), fvector3)
```

---

## api_get_rigidbody_velocity

method in GameAPI

- 描述

    获得刚体速度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | body | py.RigidBody | 刚体 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3 | 速度 |

- 示例

```lua
local rigid_body = GameAPI.get_unit_key_rigid_body_kv(1, "key")

local result = GameAPI.api_get_rigidbody_velocity(rigid_body)
```

---

## api_set_rigidbody_angular_velocity

method in GameAPI

- 描述

    设置刚体角速度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | body | py.RigidBody | 刚体 |
    | angular_velocity | py.FVector3 | 角速度 |

- 返回值

    无

- 示例

```lua
local rigid_body = GameAPI.get_unit_key_rigid_body_kv(1, "key")
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

GameAPI.api_set_rigidbody_angular_velocity(rigid_body, fvector3)
```

---

## api_get_rigidbody_angular_velocity

method in GameAPI

- 描述

    设置刚体角速度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | body | py.RigidBody | 刚体 |

- 返回值

    无

- 示例

```lua
local rigid_body = GameAPI.get_unit_key_rigid_body_kv(1, "key")

GameAPI.api_get_rigidbody_angular_velocity(rigid_body)
```

---

## api_get_rigidbody_forward

method in GameAPI

- 描述

    获得刚体朝向

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | body | py.RigidBody | 刚体 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3 | 朝向 |

- 示例

```lua
local rigid_body = GameAPI.get_unit_key_rigid_body_kv(1, "key")

local result = GameAPI.api_get_rigidbody_forward(rigid_body)
```

---

## api_get_rigid_body_group_in_range

method in GameAPI

- 描述

    获得范围内的刚体组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | position | py.FVector3 | 位置 |
    | radius | number | 半径 |
    | collision_category? | integer | 自身碰撞类别 |
    | collide_with_mask? | integer | 目标碰撞类别 |
    | ignore_trigger? | boolean | 忽略触发器 |
    | ignore_non_trigger? | boolean | 忽略非触发器 |
    | ignore_non_rigid? | boolean | 忽略非刚体 |
    | ignore_dynamic? | boolean | 忽略动态物体 |
    | ignore_kinematic? | boolean | 忽略运动学物体 |
    | ignore_static? | boolean | 忽略静态物体 |
    | ignore_logic_body? | boolean | 忽略逻辑物体 |
    | ignore_non_logic_body? | boolean | 忽略非逻辑物体 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RigidBodyGroup | 刚体组 |

- 示例

```lua
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

local result = GameAPI.api_get_rigid_body_group_in_range(fvector3, 1.0, 1, 1, true, true, true, true, true, true, true, true)
```

---

## api_replace_rigid_body_model

method in GameAPI

- 描述

    替换刚体模型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | body | py.RigidBody | 刚体 |
    | id | py.ModelKey | 模型id |

- 返回值

    无

- 示例

```lua
local rigid_body = GameAPI.get_unit_key_rigid_body_kv(1, "key")
local model_key = 1

GameAPI.api_replace_rigid_body_model(rigid_body, model_key)
```

---

## api_restore_rigid_body_last_model

method in GameAPI

- 描述

    还原刚体上一个模型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | body | py.RigidBody | 刚体 |

- 返回值

    无

- 示例

```lua
local rigid_body = GameAPI.get_unit_key_rigid_body_kv(1, "key")

GameAPI.api_restore_rigid_body_last_model(rigid_body)
```

---

## api_get_rigid_body_collider

method in GameAPI

- 描述

    获得刚体中指定名字的碰撞器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | body | py.RigidBody | 刚体 |
    | name | string | 碰撞器名字 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Collider | Collider |

- 示例

```lua
local rigid_body = GameAPI.get_unit_key_rigid_body_kv(1, "key")

local result = GameAPI.api_get_rigid_body_collider(rigid_body, "name")
```

---

## api_is_rigid_has_tag

method in GameAPI

- 描述

    刚体是否有指定tag

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | body | py.RigidBody | 刚体 |
    | tag | string | tag |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 布尔值 |

- 示例

```lua
local rigid_body = GameAPI.get_unit_key_rigid_body_kv(1, "key")

local result = GameAPI.api_is_rigid_has_tag(rigid_body, "tag")
```

---

## api_rigid_body_get_mass

method in GameAPI

- 描述

    获取刚体质量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | body | py.RigidBody | 刚体 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 质量 |

- 示例

```lua
local rigid_body = GameAPI.get_unit_key_rigid_body_kv(1, "key")

local result = GameAPI.api_rigid_body_get_mass(rigid_body)
```

---

## api_rigid_body_set_scale

method in GameAPI

- 描述

    设置刚体模型缩放

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | body | py.RigidBody | 刚体 |
    | scale_x | number | x缩放 |
    | scale_y | number | y缩放 |
    | scale_z | number | z缩放 |

- 返回值

    无

- 示例

```lua
local rigid_body = GameAPI.get_unit_key_rigid_body_kv(1, "key")

GameAPI.api_rigid_body_set_scale(rigid_body, 1.0, 1.0, 1.0)
```

---

## api_rigid_body_angle_axis

method in GameAPI

- 描述

    刚体按照指定轴旋转

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | body | py.RigidBody | 刚体 |
    | axis | py.Vector3 | 轴 |
    | angle | py.Fixed | 角度 |

- 返回值

    无

- 示例

```lua
local rigid_body = GameAPI.get_unit_key_rigid_body_kv(1, "key")
local vector3 = Fix32Vec3(0, 0, 0)

GameAPI.api_rigid_body_angle_axis(rigid_body, vector3, Fix32(1))
```

---

## api_throw_rigid_body

method in GameAPI

- 描述

    扔出刚体

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | body | py.PhysicsEntity | 刚体 |
    | start | py.Vector3 | 抛出点 |
    | forward | py.Vector3 | 抛出方向 |
    | length | py.Fixed | 抛出距离 |
    | speed | py.Fixed | 水平速度 |

- 返回值

    无

- 示例

```lua
local physics_entity = GameAPI.get_unit_key_physics_entity_kv(1, "key")
local vector3 = Fix32Vec3(0, 0, 0)

GameAPI.api_throw_rigid_body(physics_entity, vector3, vector3, Fix32(1), Fix32(1))
```

---

## api_set_rigid_body_reference_frame_velocity

method in GameAPI

- 描述

    设置刚体的相对坐标系的速度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | body | py.RigidBody | 刚体 |
    | speed | py.Fixed | 速度大小 |
    | direction | py.FVector3 | 速度方向 |

- 返回值

    无

- 示例

```lua
local rigid_body = GameAPI.get_unit_key_rigid_body_kv(1, "key")
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

GameAPI.api_set_rigid_body_reference_frame_velocity(rigid_body, Fix32(1), fvector3)
```

---

## api_set_rigid_body_add_reference_frame

method in GameAPI

- 描述

    设置刚体绑定目标刚体的相对坐标系

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | body | py.RigidBody | 刚体 |
    | target | py.RigidBody | 目标刚体 |

- 返回值

    无

- 示例

```lua
local rigid_body = GameAPI.get_unit_key_rigid_body_kv(1, "key")

GameAPI.api_set_rigid_body_add_reference_frame(rigid_body, rigid_body)
```

---

## api_set_rigid_body_remove_reference_frame

method in GameAPI

- 描述

    设置刚体移除目标刚体的相对坐标系

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | body | py.RigidBody | 刚体 |
    | target | py.RigidBody | 目标刚体 |

- 返回值

    无

- 示例

```lua
local rigid_body = GameAPI.get_unit_key_rigid_body_kv(1, "key")

GameAPI.api_set_rigid_body_remove_reference_frame(rigid_body, rigid_body)
```

---

## api_transform_local_to_global_coords

method in GameAPI

- 描述

    把刚体的本地坐标转到全局坐标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | body | py.RigidBody | 刚体 |
    | local_pos | py.FVector3 | local_pos |

- 返回值

    无

- 示例

```lua
local rigid_body = GameAPI.get_unit_key_rigid_body_kv(1, "key")
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

GameAPI.api_transform_local_to_global_coords(rigid_body, fvector3)
```

---

## api_add_rigid_body_to_group

method in GameAPI

- 描述

    添加刚体到刚体组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | body | py.Unit | 刚体 |
    | group | py.RigidBodyGroup | 刚体组 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local rigid_body_group = GameAPI.get_unit_key_rigid_body_group_kv(1, "key")

GameAPI.api_add_rigid_body_to_group(unit.handle, rigid_body_group)
```

---

## api_remove_rigid_body_in_group

method in GameAPI

- 描述

    从刚体组中移除刚体

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | group | py.UnitGroup | 刚体组 |
    | body | py.Unit | 刚体 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local unit_group = y3.unit_group.create()

GameAPI.api_remove_rigid_body_in_group(unit_group.handle, unit.handle)
```

---

## api_delete_reaction

method in GameAPI

- 描述

    删除REACTION

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | reaction | py.Reaction | Reaction |

- 返回值

    无

- 示例

```lua
local physics_entity = GameAPI.get_unit_key_physics_entity_kv(1, "key")
local reaction = GameAPI.api_add_uniform_gravitation_field_to_rigid_body(physics_entity, Fix32(10), Fix32Vec3(0, 0, 0))

GameAPI.api_delete_reaction(reaction)
```

---

## api_delete_reaction_group

method in GameAPI

- 描述

    删除REACTION Group

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | reactions | py.ReactionGroup | ReactionGroup |

- 返回值

    无

- 示例

```lua
local reaction_group = GameAPI.get_trigger_variable_reaction_group("key")

GameAPI.api_delete_reaction_group(reaction_group)
```

---

## api_add_uniform_gravitation_field_to_rigid_body

method in GameAPI

- 描述

    刚体增加均匀引力场

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | body | py.PhysicsEntity | 刚体 |
    | speed | py.Fixed | 速度大小 |
    | position | py.Vector3 | 力场源点 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Reaction | 物理Reaction |

- 示例

```lua
local physics_entity = GameAPI.get_unit_key_physics_entity_kv(1, "key")
local vector3 = Fix32Vec3(0, 0, 0)

local result = GameAPI.api_add_uniform_gravitation_field_to_rigid_body(physics_entity, Fix32(1), vector3)
```

---

## api_add_wind_force_field_to_rigid_body

method in GameAPI

- 描述

    刚体增加风场

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | body | py.PhysicsEntity | 刚体 |
    | speed | py.Fixed | 速度大小 |
    | direction | py.FVector3 | 速度方向 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RigidBody | RigidBody |

- 示例

```lua
local physics_entity = GameAPI.get_unit_key_physics_entity_kv(1, "key")
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

local result = GameAPI.api_add_wind_force_field_to_rigid_body(physics_entity, Fix32(1), fvector3)
```

---

## throw_physics_item

method in GameAPI

- 描述

    物理物品抛出

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_item | py.Unit | 物品单位 |
    | length | py.Fixed | 抛出距离 |
    | vel | py.Fixed | 水平速度 |
    | socket_name | string | 出手绑点 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.throw_physics_item(unit.handle, Fix32(1), Fix32(1), "socket_name")
```

---

## get_physics_item_body_object

method in GameAPI

- 描述

    获取物理物品的刚体

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_item | py.Unit | 物品单位 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.get_physics_item_body_object(unit.handle)
```

---

## api_remove_physics_item

method in GameAPI

- 描述

    删除逻辑物理物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_item | py.Unit | 物品单位 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.api_remove_physics_item(unit.handle)
```

---

## api_physics_item_viewer_detach

method in GameAPI

- 描述

    逻辑物理物品模型解绑持有者

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_item | py.Unit | 物品单位 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.api_physics_item_viewer_detach(unit.handle)
```

---

## api_physics_item_get_ability

method in GameAPI

- 描述

    获取逻辑物理物品绑定技能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_item | py.Unit | 物品单位 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.api_physics_item_get_ability(unit.handle)
```

---

## api_physics_item_create_sfx

method in GameAPI

- 描述

    逻辑物理物品创建特效

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_item | py.PhysicsEntity | 物理组件 |
    | sfx_id | py.Fixed | 特效ID |
    | position | py.FVector3 | 位置 |
    | duration? | py.Fixed | 持续时间 |

- 返回值

    无

- 示例

```lua
local physics_entity = GameAPI.get_unit_key_physics_entity_kv(1, "key")
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

GameAPI.api_physics_item_create_sfx(physics_entity, Fix32(1), fvector3, Fix32(1))
```

---

## api_physics_item_play_animation

method in GameAPI

- 描述

    逻辑物理物品播放动画

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_item | py.Unit | 物理组件 |
    | anim | string | 动画名称 |
    | play_speed | number | 播放倍率 |
    | begin_t | number | 开始时间(s) |
    | end_t | number | 结束时间(s)，正数 -1 表示不结束 |
    | loop | boolean | 是否循环 |
    | return_idle | boolean | 播放结束后是否恢复idle |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.api_physics_item_play_animation(unit.handle, "anim", 1.0, 1.0, 1.0, true, true)
```

---

## throw_physics_entity

method in GameAPI

- 描述

    单位扔出物理组件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | entity | py.PhysicsEntity | 物理组件 |
    | length | py.Fixed | 抛出距离 |
    | vel | py.Fixed | 水平速度 |
    | socket_name | string | 出手绑点 |

- 返回值

    无

- 示例

```lua
local physics_entity = GameAPI.get_unit_key_physics_entity_kv(1, "key")

GameAPI.throw_physics_entity(physics_entity, Fix32(1), Fix32(1), "socket_name")
```

---

## api_detach_physics_entity_viewer

method in GameAPI

- 描述

    持有者解绑逻辑物理组件模型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | entity | py.Unit | 逻辑物理组件 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.api_detach_physics_entity_viewer(unit.handle)
```

---

## api_get_physics_entity_owner

method in GameAPI

- 描述

    获得逻辑物理组件的持有者

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | entity | py.PhysicsEntity | 逻辑物理组件 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 持有者 |

- 示例

```lua
local physics_entity = GameAPI.get_unit_key_physics_entity_kv(1, "key")

local result = GameAPI.api_get_physics_entity_owner(physics_entity)
```

---

## create_sfx_on_point_3d

method in GameAPI

- 描述

    创建特效到三维坐标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | sfx_id | py.SfxKey | 特效编号 |
    | position | py.FVector3 | 位置 |
    | direction? | py.FVector3 | 朝向 |
    | scale? | number | 缩放比例 |
    | duration? | number | 持续时间 |
    | immediately? | boolean | 是否立即删除 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sfx | 特效 |

- 示例

```lua
local sfx_key = 134274569
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

local result = GameAPI.create_sfx_on_point_3d(sfx_key, fvector3, nil, 1.0, 1.0, true)
```

---

## report_info

method in GameAPI

- 描述

    埋点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | key |
    | value | string | value |
    | str1 | string | 额外参数1 |
    | str2 | string | 额外参数2 |
    | str3 | string | 额外参数3 |
    | str4 | string | 额外参数4 |
    | str5 | string | 额外参数5 |

- 返回值

    无

- 示例

```lua
GameAPI.report_info("key", "value", "str1", "str2", "str3", "str4", "str5")
```

---

## api_debug_pause

method in GameAPI

- 描述

    调试暂停

- 参数

    无

- 返回值

    无

- 示例

```lua
GameAPI.api_debug_pause()
```

---

## init_lua_var

method in GameAPI

- 描述

    LUA层初始化参数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | name | string | name |
    | value | string | value |
    | if_list | boolean | 是否数组 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Actor | 变量 |

- 示例

```lua
local result = GameAPI.init_lua_var("name", "value", true)
```

---

## set_lua_var

method in GameAPI

- 描述

    从lua设置变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | func_name | string | 函数名称 |
    | actor | py.Actor | actor |
    | key | integer | index |
    | index | string | key |
    | value | string | value |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.set_lua_var("func_name", actor, 1, "index", "value")
```

---

## get_lua_var

method in GameAPI

- 描述

    从lua读取变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | func_name | string | 函数名称 |
    | actor | py.Actor | actor |
    | key | string | key |
    | index? | integer | index |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GameAPI.get_lua_var("func_name", actor, "key", 1)
```

---

## set_random_seed

method in GameAPI

- 描述

    设置随机数种子

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | v | integer | 随机数种子 |

- 返回值

    无

- 示例

```lua
GameAPI.set_random_seed(1)
```

---

## get_random_seed

method in GameAPI

- 描述

    获取随机数种子

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 随机数种子 |

- 示例

```lua
local result = GameAPI.get_random_seed()
```

---

## create_unit

method in GameAPI

- 描述

    创建单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | py.UnitKey | 单位编号 |
    | pos | py.FVector3 | 位置 |
    | angle | py.Fixed | 朝向 |
    | role_or_unit | py.Role | 所属玩家 |
    | lua_table? | py.Table | 用户自定义配置表 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 创建出的单位 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local unit_key = 134274569
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))
local tbl = {}

local result = GameAPI.create_unit(unit_key, fvector3, Fix32(1), player.handle)
```

---

## change_unit_role

method in GameAPI

- 描述

    改变单位所属玩家

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | role | py.Role | 所属玩家 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

GameAPI.change_unit_role(unit.handle, player.handle)
```

---

## change_projectile_owner

method in GameAPI

- 描述

    改变投射物所属单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile | py.ProjectileEntity | 投射物 |
    | unit | py.Unit | 单位 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local target_point = unit:get_point()
local projectile = y3.projectile.create({ key = 134274569, target = target_point })

GameAPI.change_projectile_owner(projectile.handle, unit.handle)
```

---

## change_projectile_ability

method in GameAPI

- 描述

    改变投射物所属技能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile | py.ProjectileEntity | 投射物 |
    | related_ability | py.Ability | 单位 |

- 返回值

    无

- 示例

```lua
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)
local unit = y3.player.get_by_id(1):get_all_units()[1]
local target_point = unit:get_point()
local projectile = y3.projectile.create({ key = 134274569, target = target_point })

GameAPI.change_projectile_ability(projectile.handle, ability.handle)
```

---

## change_role_res_icon

method in GameAPI

- 描述

    修改玩家资源图标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | res_key | py.RoleResKey | 资源名称 |
    | icon_id | integer | 图标编号 |

- 返回值

    无

- 示例

```lua
local role_res_key = "res_key"

GameAPI.change_role_res_icon(role_res_key, 1)
```

---

## change_role_res_icon_with_icon

method in GameAPI

- 描述

    修改玩家资源图标(图片类型)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | res_key | py.RoleResKey | 资源名称 |
    | icon_id | py.Texture | 图标 |

- 返回值

    无

- 示例

```lua
local role_res_key = "res_key"

GameAPI.change_role_res_icon_with_icon(role_res_key, 1)
```

---

## remove_control_unit

method in GameAPI

- 描述

    移除控制列表中的某个单位

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

GameAPI.remove_control_unit(player.handle, unit.handle)
```

---

## get_unit_ids_in_team

method in GameAPI

- 描述

    获取队伍内单位列表

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | team_id | integer | 队伍编号 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.get_unit_ids_in_team(player.handle, 1)
```

---

## add_unit_to_team

method in GameAPI

- 描述

    给队伍添加单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | team_id | integer | 队伍编号 |
    | unit | py.Unit | 单位 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

GameAPI.add_unit_to_team(player.handle, 1, unit.handle)
```

---

## remove_unit_from_team

method in GameAPI

- 描述

    从队伍中去除单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | team_id | integer | 队伍编号 |
    | unit | py.Unit | 单位 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

GameAPI.remove_unit_from_team(player.handle, 1, unit.handle)
```

---

## create_illusion

method in GameAPI

- 描述

    创建幻象

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | clone_unit | py.Unit | 复制目标 |
    | caller_unit | py.Unit | 召唤者 |
    | role | py.Role | 玩家 |
    | pos | py.FVector3 | 位置 |
    | angle | py.Fixed | 朝向 |
    | clone_hp_mp? | boolean | 是否继承生命与魔法 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

GameAPI.create_illusion(unit.handle, unit.handle, player.handle, fvector3, Fix32(1), true)
```

---

## is_unit_illusion

method in GameAPI

- 描述

    判断单位是否是幻象单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否是幻象 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = GameAPI.is_unit_illusion(unit.handle)
```

---

## get_illusion_caller_unit

method in GameAPI

- 描述

    获取幻象召唤者

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | illusion_unit | py.Unit | 幻象单位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 召唤单位 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = GameAPI.get_illusion_caller_unit(unit.handle)
```

---

## create_projectile_on_socket

method in GameAPI

- 描述

    在单位的挂接点创建一个投掷物

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | p_key | py.ProjectileKey | 投掷物编号 |
    | socket_unit | py.Unit | 挂节点所属单位 |
    | socket_name | string | 挂接点名称 |
    | face | py.Fixed | 朝向 |
    | owner_unit_or_player? | py.Actor | 所属单位或玩家 |
    | related_ability? | py.Ability | 关联技能 |
    | visibility? | integer | 粒子特效可见性规则 |
    | duration? | py.Fixed | 持续时间 |
    | is_open_duration? | boolean | 是否启用持续时间 |
    | immediately? | boolean | 立即移除表现 |
    | use_sys_d_destroy_way? | boolean | 特效删除的方式是否读表 |
    | show_in_fog? | boolean | 迷雾中是否可见 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileEntity | 创建出的投掷物 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)
local actor = unit.handle
local projectile_key = 134274569

local result = GameAPI.create_projectile_on_socket(projectile_key, unit.handle, "socket_name", Fix32(1), nil, nil, 1, Fix32(1), true, true, true, true)
```

---

## create_projectile_in_scene

method in GameAPI

- 描述

    创建一个投掷物

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | p_key | py.ProjectileKey | 投掷物编号 |
    | location | py.FVector3 | 位置 |
    | face? | py.Fixed | 朝向 |
    | owner_unit_or_player? | py.Unit | 所属单位 |
    | related_ability? | py.Ability | 关联技能 |
    | duration? | py.Fixed | 持续时间 |
    | is_open_duration? | boolean | 是否启用持续时间 |
    | height? | py.Fixed | 高度 |
    | visibility? | integer | 粒子特效可见性规则 |
    | immediately? | boolean | 立即移除表现 |
    | use_sys_d_destroy_way? | boolean | 特效删除的方式是否读表 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileEntity | 创建出的投掷物 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)
local projectile_key = 134274569
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

local result = GameAPI.create_projectile_in_scene(projectile_key, fvector3, Fix32(1), nil, nil, Fix32(1), true, Fix32(1), 1, true, true)
```

---

## create_projectile_in_scene_new

method in GameAPI

- 描述

    创建一个投掷物

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | p_key | py.ProjectileKey | 投掷物编号 |
    | location | py.FVector3 | 位置 |
    | owner_unit_or_player | py.Actor | 所属单位或玩家 |
    | face? | py.Fixed | 朝向 |
    | related_ability? | py.Ability | 关联技能 |
    | duration? | py.Fixed | 持续时间 |
    | is_open_duration? | boolean | 是否启用持续时间 |
    | height? | py.Fixed | 高度 |
    | visibility? | integer | 粒子特效可见性规则 |
    | immediately? | boolean | 立即移除表现 |
    | use_sys_d_destroy_way? | boolean | 特效删除的方式是否读表 |
    | show_in_fog? | boolean | 迷雾中是否可见 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileEntity | 创建出的投掷物 |

- 示例

```lua
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local projectile_key = 134274569
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

local result = GameAPI.create_projectile_in_scene_new(projectile_key, fvector3, actor, Fix32(1), nil, Fix32(1), true, Fix32(1), 1, true, true, true)
```

---

## add_role_to_group

method in GameAPI

- 描述

    将玩家添加到玩家组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | group | py.RoleGroup | 玩家组 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local player_group = y3.player_group.create()

GameAPI.add_role_to_group(player.handle, player_group.handle)
```

---

## rem_role_from_group

method in GameAPI

- 描述

    玩家组中删除玩家

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | group | py.RoleGroup | 玩家组 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local player_group = y3.player_group.create()

GameAPI.rem_role_from_group(player.handle, player_group.handle)
```

---

## get_unit_by_id

method in GameAPI

- 描述

    根据单位ID获取单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_id | py.UnitID | 单位id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 单位 |

- 示例

```lua
local unit_id = 134274569

local result = GameAPI.get_unit_by_id(unit_id)
```

---

## get_projectile_by_id

method in GameAPI

- 描述

    根据特效ID获取特效

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_id | py.ProjectileID | 特效id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileEntity | 特效 |

- 示例

```lua
local result = GameAPI.get_projectile_by_id(1)
```

---

## judge_unit_in_group

method in GameAPI

- 描述

    判断单位是否在单位组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | group | py.UnitGroup | 单位组 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否在单位组 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local unit_group = y3.unit_group.create()

local result = GameAPI.judge_unit_in_group(unit.handle, unit_group.handle)
```

---

## api_get_tech_icon

method in GameAPI

- 描述

    获取科技图标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | target_level | integer | 等级 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Texture | 图片 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.api_get_tech_icon(tech_key, 1)
```

---

## update_global_weather

method in GameAPI

- 描述

    设置全局天气

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | weather_type | integer | 天气类型 |

- 返回值

    无

- 示例

```lua
GameAPI.update_global_weather(1)
```

---

## get_global_weather

method in GameAPI

- 描述

    获得全局天气

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 天气类型 |

- 示例

```lua
local result = GameAPI.get_global_weather()
```

---

## start_skill_pointer

method in GameAPI

- 描述

    打开技能指示器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | ability | py.Ability | 技能 |
    | dry_run? | boolean | 是否仅模拟不施法 |
    | ignore_unit_ids? | py.UnitGroup | 忽略单位的id列表 |

- 返回值

    无

- 示例

```lua
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)
local player = y3.player.get_by_id(1)
local unit_group = y3.unit_group.create()

GameAPI.start_skill_pointer(player.handle, ability.handle, true)
```

---

## stop_skill_pointer

method in GameAPI

- 描述

    关闭技能指示器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | ability | py.Ability | 技能 |

- 返回值

    无

- 示例

```lua
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)
local player = y3.player.get_by_id(1)

GameAPI.stop_skill_pointer(player.handle, ability.handle)
```

---

## create_preview_skill_pointer

method in GameAPI

- 描述

    打开技能指示器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | ability | py.Ability | 技能 |

- 返回值

    无

- 示例

```lua
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)
local player = y3.player.get_by_id(1)

GameAPI.create_preview_skill_pointer(player.handle, ability.handle)
```

---

## clear_preview_skill_pointer

method in GameAPI

- 描述

    关闭技能指示器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.clear_preview_skill_pointer(player.handle)
```

---

## get_ability_key_skill_pointer

method in GameAPI

- 描述

    技能类型指示器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_id | py.AbilityKey | 技能ID |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 指示器类型 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_skill_pointer(ability_key)
```

---

## send_signal

method in GameAPI

- 描述

    发送信号

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role_or_role_id | py.RoleID | 玩家ID |
    | signal_type | py.SignalType | 信号类型 |
    | world_pos | py.Point | 位置 |
    | visible_type | py.SignalVisibleType | 显示类型 |

- 返回值

    无

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)
local role_id = 1

GameAPI.send_signal(role_id, 1, point, 1)
```

---

## get_point_light_res_by_res_id

method in GameAPI

- 描述

    根据点光源ID返回点光源

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | res_id | py.LightID | 光源ID |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PointLight | 点光源 |

- 示例

```lua
local result = GameAPI.get_point_light_res_by_res_id(1)
```

---

## get_spot_light_res_by_res_id

method in GameAPI

- 描述

    根据方向光源ID返回方向光源

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | res_id | py.LightID | 光源ID |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SpotLight | 方向光源 |

- 示例

```lua
local result = GameAPI.get_spot_light_res_by_res_id(1)
```

---

## create_point_light_to_point

method in GameAPI

- 描述

    创建点光源到点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.Point | 点 |
    | offset_y? | py.Fixed | 偏移高度 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PointLight | 点光源 |

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)

local result = GameAPI.create_point_light_to_point(point, Fix32(1))
```

---

## create_point_light_to_unit_socket

method in GameAPI

- 描述

    创建点光源到单位绑点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | socket_name | string | 挂节点 |
    | offset_y? | py.Fixed | 偏移高度 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.PointLight | 点光源 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = GameAPI.create_point_light_to_unit_socket(unit.handle, "socket_name", Fix32(1))
```

---

## create_spot_light_to_point

method in GameAPI

- 描述

    创建方向光源到点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.Point | 点 |
    | pos_offset_y? | py.Fixed | 起点偏移高度 |
    | target? | py.Actor | 朝向目标 |
    | target_offset_y? | py.Fixed | 朝向目标偏移高度 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SpotLight | 方向光源 |

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.create_spot_light_to_point(point, Fix32(1), nil, Fix32(1))
```

---

## create_spot_light_to_unit_socket

method in GameAPI

- 描述

    创建方向光源到单位绑点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | socket_name | string | 挂节点 |
    | pos_offset_y? | py.Fixed | 起点偏移高度 |
    | target? | py.Actor | 朝向目标 |
    | target_offset_y? | py.Fixed | 朝向目标偏移高度 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SpotLight | 方向光源 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.create_spot_light_to_unit_socket(unit.handle, "socket_name", Fix32(1), nil, Fix32(1))
```

---

## remove_light

method in GameAPI

- 描述

    删除光源

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | light | py.Light | 光源 |

- 返回值

    无

- 示例

```lua
local light = GameAPI.get_point_light_res_by_res_id(1)

GameAPI.remove_light(light)
```

---

## set_light_float_attr_value

method in GameAPI

- 描述

    设置光源Float属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | light | py.Light | 光源 |
    | attr_name | string | 属性名 |
    | value | py.Fixed | 值 |

- 返回值

    无

- 示例

```lua
local light = GameAPI.get_point_light_res_by_res_id(1)

GameAPI.set_light_float_attr_value(light, "attr_name", Fix32(1))
```

---

## get_units_by_key

method in GameAPI

- 描述

    获取固定单位编号的单位组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitGroup | 单位组 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_units_by_key(unit_key)
```

---

## get_random_n_unit_in_group

method in GameAPI

- 描述

    单位组内随机整数个单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | units | py.UnitGroup | 单位组 |
    | n | integer | 随机个数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitGroup | 随机的单位组 |

- 示例

```lua
local unit_group = y3.unit_group.create()

local result = GameAPI.get_random_n_unit_in_group(unit_group.handle, 1)
```

---

## get_first_unit_in_group

method in GameAPI

- 描述

    单位组内第一个单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | units | py.UnitGroup | 单位组 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 第一个单位 |

- 示例

```lua
local unit_group = y3.unit_group.create()

local result = GameAPI.get_first_unit_in_group(unit_group.handle)
```

---

## get_last_unit_in_group

method in GameAPI

- 描述

    单位组内最后一个单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | units | py.UnitGroup | 单位组 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 最后一个单位 |

- 示例

```lua
local unit_group = y3.unit_group.create()

local result = GameAPI.get_last_unit_in_group(unit_group.handle)
```

---

## get_unit_sort_by_attr

method in GameAPI

- 描述

    根据属性值从单位组中取整数个单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | units | py.UnitGroup | 单位组 |
    | attr | string | 属性 |
    | rise | boolean | 是否升序排列 |
    | num | integer | 单位个数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitGroup | 单位组 |

- 示例

```lua
local unit_group = y3.unit_group.create()

local result = GameAPI.get_unit_sort_by_attr(unit_group.handle, "attr", true, 1)
```

---

## get_unit_sort_by_position

method in GameAPI

- 描述

    根据距离从单位组中取整数个单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | units | py.UnitGroup | 单位组 |
    | point | py.FPoint | 点 |
    | rise | boolean | 是否升序排列 |
    | num | integer | 单位个数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitGroup | 单位组 |

- 示例

```lua
local unit_group = y3.unit_group.create()
local fpoint = GameAPI.get_point_by_res_id(1)

local result = GameAPI.get_unit_sort_by_position(unit_group.handle, fpoint, true, 1)
```

---

## get_random_unit_in_unit_group

method in GameAPI

- 描述

    单位组内随机一个单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | units | py.UnitGroup | 单位组 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 单位 |

- 示例

```lua
local unit_group = y3.unit_group.create()

local result = GameAPI.get_random_unit_in_unit_group(unit_group.handle)
```

---

## api_get_influenced_by_cd_reduce

method in GameAPI

- 描述

    技能类型是否受冷却缩减影响

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_id | py.AbilityKey | 技能类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 布尔值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.api_get_influenced_by_cd_reduce(ability_key)
```

---

## get_ability_conf_str_attr

method in GameAPI

- 描述

    技能类型的字符串属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_id | py.AbilityKey | 技能类型 |
    | attr_name | py.AbilityStrAttr | 字符串属性 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_conf_str_attr(ability_key, 1)
```

---

## get_ability_conf_bool_attr

method in GameAPI

- 描述

    技能类型的布尔属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_id | py.AbilityKey | 技能类型 |
    | attr_name | string | 布尔属性 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 布尔属性 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_conf_bool_attr(ability_key, "attr_name")
```

---

## get_ability_conf_float_attr

method in GameAPI

- 描述

    技能类型的实数属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_id | py.AbilityKey | 技能类型 |
    | attr_name | string | 实数属性 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 实数 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_conf_float_attr(ability_key, "attr_name")
```

---

## get_ability_conf_int_attr

method in GameAPI

- 描述

    技能类型的整数属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_id | py.AbilityKey | 技能类型 |
    | attr_name | string | 整数属性 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 实数 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_conf_int_attr(ability_key, "attr_name")
```

---

## get_ability_conf_formula_attr

method in GameAPI

- 描述

    技能类型的公式属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_id | py.AbilityKey | 技能类型 |
    | attr_name | string | 公式属性 |
    | level | integer | 当前等级 |
    | stack_count | integer | 当前充能层数 |
    | unit_hp_max? | py.Fixed | 施法者最大生命值 |
    | unit_hp_cur? | py.Fixed | 施法者当前生命值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 实数 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_conf_formula_attr(ability_key, "attr_name", 1, 1, Fix32(1), Fix32(1))
```

---

## get_ability_conf_formula_attr_with_unit

method in GameAPI

- 描述

    技能类型的公式属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_id | py.AbilityKey | 技能类型 |
    | attr_name | string | 公式属性 |
    | level | integer | 当前等级 |
    | stack_count | integer | 当前充能层数 |
    | unit? | py.Unit | 施法计算单位 |
    | return_cm? | boolean | 是否返回cm |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 实数 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability_key = 134274569

local result = GameAPI.get_ability_conf_formula_attr_with_unit(ability_key, "attr_name", 1, 1, nil, true)
```

---

## get_target_unit_in_ability

method in GameAPI

- 描述

    技能选取的目标单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability | py.Ability | 技能 |
    | runtime_id? | integer | runtime_id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit | 单位 |

- 示例

```lua
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = GameAPI.get_target_unit_in_ability(ability.handle, 1)
```

---

## get_target_item_in_ability

method in GameAPI

- 描述

    技能选取的目标物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability | py.Ability | 技能 |
    | runtime_id? | integer | runtime_id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Item | 物品 |

- 示例

```lua
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = GameAPI.get_target_item_in_ability(ability.handle, 1)
```

---

## get_target_dest_in_ability

method in GameAPI

- 描述

    技能选取的目标可破坏物

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability | py.Ability | 技能 |
    | runtime_id? | integer | runtime_id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Destructible | 可破坏物 |

- 示例

```lua
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = GameAPI.get_target_dest_in_ability(ability.handle, 1)
```

---

## filter_unit_id_list_in_area

method in GameAPI

- 描述

    筛选范围内单位(废弃)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | pos | py.Vector3 | 坐标 |
    | shape | py.Shape | 形状 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitGroup | 单位组 |

- 示例

```lua
local vector3 = Fix32Vec3(0, 0, 0)
local shape = GlobalAPI.create_circular_shape(Fix32(500))

local result = GameAPI.filter_unit_id_list_in_area(vector3, shape)
```

---

## filter_unit_id_list_in_area_v2

method in GameAPI

- 描述

    筛选范围内单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | pos | py.Vector3 | 坐标 |
    | shape | py.Shape | 形状 |
    | belong_role_group? | py.Role | 属于玩家或玩家组 |
    | visible_role? | py.Role | 对玩家可见 |
    | invisible_role? | py.Role | 对玩家不可见 |
    | exclude_unit_group? | py.UnitGroup | 不在单位组内 |
    | with_tag? | string | 具有标签 |
    | without_tag? | string | 不具有标签 |
    | entity_no? | py.UnitKey | 单位名称 |
    | exclude_unit? | py.Unit | 排除单位 |
    | unit_type? | py.UnitType | 单位种类 |
    | in_state? | integer | 具有状态 |
    | not_in_state? | integer | 不具有状态 |
    | include_dead? | boolean | 是否包括死亡单位 |
    | max_count? | integer | 数量上限 |
    | sort_type? | py.SortType | 排序类型 |
    | filter_ability? | py.Ability | 筛选技能 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitGroup | 单位组 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)
local player = y3.player.get_by_id(1)
local vector3 = Fix32Vec3(0, 0, 0)
local shape = GlobalAPI.create_circular_shape(Fix32(500))
local unit_group = y3.unit_group.create()
local unit_key = 134274569

local result = GameAPI.filter_unit_id_list_in_area_v2(vector3, shape, nil, nil, nil, nil, "with_tag", "without_tag", nil, nil, 1, 1, 1, true, 1, 1)
```

---

## filter_projectile_id_list_in_area

method in GameAPI

- 描述

    筛选范围内投射物

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | pos | py.Vector3 | 坐标 |
    | shape | py.Shape | 形状 |
    | sort_type? | py.SortType | 排序类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileGroup | 投射物组 |

- 示例

```lua
local vector3 = Fix32Vec3(0, 0, 0)
local shape = GlobalAPI.create_circular_shape(Fix32(500))

local result = GameAPI.filter_projectile_id_list_in_area(vector3, shape, 1)
```

---

## get_all_projectiles_with_tag

method in GameAPI

- 描述

    筛选带有tag的投射物

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | tag |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileGroup | 投射物组 |

- 示例

```lua
local result = GameAPI.get_all_projectiles_with_tag("tag")
```

---

## get_camp_by_camp_id

method in GameAPI

- 描述

    按阵营编号获取阵营对象

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | camp_id | py.CampID | 阵营编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Camp | 阵营对象 |

- 示例

```lua
local result = GameAPI.get_camp_by_camp_id(1)
```

---

## get_camp_id_by_role_id

method in GameAPI

- 描述

    按玩家编号获取阵营编号

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role_id | py.RoleID | 玩家编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Camp | 阵营编号 |

- 示例

```lua
local role_id = 1

local result = GameAPI.get_camp_id_by_role_id(role_id)
```

---

## get_role_by_role_id

method in GameAPI

- 描述

    按玩家编号获取玩家对象

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role_id | py.RoleID | 玩家编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Role | 玩家 |

- 示例

```lua
local role_id = 1

local result = GameAPI.get_role_by_role_id(role_id)
```

---

## get_role_by_int

method in GameAPI

- 描述

    按整型获取玩家对象

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role_id | integer | 玩家编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Role | 玩家 |

- 示例

```lua
local result = GameAPI.get_role_by_int(1)
```

---

## get_alive_unit_num_by_camp_id

method in GameAPI

- 描述

    获取阵营存活单位数量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | camp_id | py.CampID | 阵营编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 单位数量 |

- 示例

```lua
local result = GameAPI.get_alive_unit_num_by_camp_id(1)
```

---

## get_all_role_ids

method in GameAPI

- 描述

    所有玩家

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleGroup | 玩家组 |

- 示例

```lua
local result = GameAPI.get_all_role_ids()
```

---

## get_role_ids_by_camp

method in GameAPI

- 描述

    阵营所有玩家

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | camp | py.Camp | 阵营对象 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleGroup | 玩家组 |

- 示例

```lua
local camp = GameAPI.get_camp_by_camp_id(1)

local result = GameAPI.get_role_ids_by_camp(camp)
```

---

## get_role_ids_by_type

method in GameAPI

- 描述

    特定类型玩家

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role_type | integer | 玩家类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleGroup | 玩家组 |

- 示例

```lua
local result = GameAPI.get_role_ids_by_type(1)
```

---

## get_ally_ids_by_role

method in GameAPI

- 描述

    同盟玩家

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleGroup | 玩家组 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_ally_ids_by_role(player.handle)
```

---

## get_enemy_ids_by_role

method in GameAPI

- 描述

    获取某玩家敌对玩家组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleGroup | 玩家组 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_enemy_ids_by_role(player.handle)
```

---

## get_victorious_role_ids

method in GameAPI

- 描述

    获取获胜玩家组

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleGroup | 玩家组 |

- 示例

```lua
local result = GameAPI.get_victorious_role_ids()
```

---

## get_defeated_role_ids

method in GameAPI

- 描述

    获取失利玩家组

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleGroup | 玩家组 |

- 示例

```lua
local result = GameAPI.get_defeated_role_ids()
```

---

## api_if_pri_attr_state_open

method in GameAPI

- 描述

    三维属性是否开启

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否开启 |

- 示例

```lua
local result = GameAPI.api_if_pri_attr_state_open()
```

---

## is_enemy

method in GameAPI

- 描述

    判断单位敌对关系

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit1 | py.Unit | 单位 |
    | unit2 | py.Unit | 单位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否敌对 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = GameAPI.is_enemy(unit.handle, unit.handle)
```

---

## is_ally

method in GameAPI

- 描述

    判断单位友军关系

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit1 | py.Unit | 单位 |
    | unit2 | py.Unit | 单位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否友军 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = GameAPI.is_ally(unit.handle, unit.handle)
```

---

## get_visibility_of_unit

method in GameAPI

- 描述

    玩家或单位是否拥有单位的可见性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role_or_unit | py.Role | 玩家 |
    | unit | py.Unit | 单位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否可见 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

local result = GameAPI.get_visibility_of_unit(player.handle, unit.handle)
```

---

## role_in_game

method in GameAPI

- 描述

    玩家是否加入游戏

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 玩家是否加入游戏 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.role_in_game(player.handle)
```

---

## role_has_store_item

method in GameAPI

- 描述

    玩家是否拥有收费道具

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | no | py.StoreKey | 收费道具key |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 玩家是否拥有收费道具 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local store_key = 134274569

local result = GameAPI.role_has_store_item(player.handle, store_key)
```

---

## has_download_save_data_callback

method in GameAPI

- 描述

    玩家下载存档是否回调

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 玩家下载存档是否回调 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.has_download_save_data_callback(player.handle)
```

---

## get_last_created_item

method in GameAPI

- 描述

    获取最近创建的物品

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Item | 物品对象 |

- 示例

```lua
local result = GameAPI.get_last_created_item()
```

---

## create_items

method in GameAPI

- 描述

    创建物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | position | py.FVector3 | 位置 |
    | num | integer | 数量 |
    | eid | py.ItemKey | 物品编号 |
    | player | py.Role | 所属玩家 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))
local item_key = 134274569

GameAPI.create_items(fvector3, 1, item_key, player.handle)
```

---

## get_item

method in GameAPI

- 描述

    根据id获取物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | id | py.ItemID | 物品ID |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Item | 物品 |

- 示例

```lua
local item_id = 134274569

local result = GameAPI.get_item(item_id)
```

---

## get_item_by_unit_id

method in GameAPI

- 描述

    根据物品id获取物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_unit_id | integer | unit_id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Item | 物品 |

- 示例

```lua
local result = GameAPI.get_item_by_unit_id(1)
```

---

## get_item_conf_name

method in GameAPI

- 描述

    获取物品配置名称

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | py.ItemKey | item_id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 物品名称 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_conf_name(item_key)
```

---

## create_item_by_id

method in GameAPI

- 描述

    创建单个物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | position | py.FVector3 | 位置 |
    | item_key | py.ItemKey | 物品编号 |
    | player | py.Role | 所属玩家 |
    | lua_table? | py.Table | 用户自定义配置表 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Item | 创建出的物品 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))
local item_key = 134274569
local tbl = {}

local result = GameAPI.create_item_by_id(fvector3, item_key, player.handle)
```

---

## get_texture_by_icon_id

method in GameAPI

- 描述

    根据ID获取图片

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | integer | 图片ID |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Texture | 图片 |

- 示例

```lua
local result = GameAPI.get_texture_by_icon_id(1)
```

---

## get_icon_id_by_texture

method in GameAPI

- 描述

    根据图片获取ID

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | texture | py.Texture | 图片 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 图片ID |

- 示例

```lua
local result = GameAPI.get_icon_id_by_texture(1)
```

---

## refresh_triggers

method in GameAPI

- 描述

    刷新触发器

- 参数

    无

- 返回值

    无

- 示例

```lua
GameAPI.refresh_triggers()
```

---

## enable_global_lua_trigger

method in GameAPI

- 描述

    激活Lua动态触发器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | lua_conf | py.Dict | Lua触发器 |

- 返回值

    无

- 示例

```lua
local dict = pydict()

GameAPI.enable_global_lua_trigger(dict)
```

---

## get_dest_by_id

method in GameAPI

- 描述

    根据预设id获取可破坏物

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | dest_unit_id | py.DestructibleID | 预设可破坏物unit_id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Destructible | 可破坏物 |

- 示例

```lua
local dest_id = 1

local result = GameAPI.get_dest_by_id(dest_id)
```

---

## get_dest_type

method in GameAPI

- 描述

    获取可破坏物类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | dest | py.Destructible | 可破坏物 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DestructibleKey | 可破坏物类型 |

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

local result = GameAPI.get_dest_type(destructible.handle)
end
```

---

## is_dest_in_area

method in GameAPI

- 描述

    判断可破坏物是否在区域中

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | dest_id | py.Destructible | 可破坏物 |
    | area | py.Area | 区域 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 布尔值 |

- 示例

```lua
local area = y3.area.create_circle_area(y3.point.create(0, 0, 0), 500)
local destructible = y3.destructible.get_by_id(1)
if destructible then

local result = GameAPI.is_dest_in_area(destructible.handle, area.handle)
end
```

---

## create_destructible

method in GameAPI

- 描述

    创建可破坏物

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | location | py.FVector3 | 位置 |
    | dest_key | py.DestructibleKey | 物品编号 |
    | angle | py.Fixed | 面向角度 |
    | size | number | 大小 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Destructible | 创建出的可破坏物 |

- 示例

```lua
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))
local destructible_key = 1

local result = GameAPI.create_destructible(fvector3, destructible_key, Fix32(1), 1.0)
```

---

## create_destructible_new

method in GameAPI

- 描述

    创建可破坏物

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | dest_key | py.DestructibleKey | 物品编号 |
    | location | py.FVector3 | 位置 |
    | angle | py.Fixed | 面向角度 |
    | scale_x? | py.Fixed | 缩放x |
    | scale_y? | py.Fixed | 缩放y |
    | scale_z? | py.Fixed | 缩放z |
    | height_offset? | py.Fixed | 高度 |
    | lua_table? | py.Table | 用户自定义配置表 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Destructible | 创建出的可破坏物 |

- 示例

```lua
local destructible_key = 1
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))
local tbl = {}

local result = GameAPI.create_destructible_new(destructible_key, fvector3, Fix32(1), Fix32(1), Fix32(1), Fix32(1), Fix32(1))
```

---

## get_all_dest_in_area

method in GameAPI

- 描述

    获取区域内的可破坏物列表

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.Area | 区域对象 |
    | sort_type? | py.SortType | 筛选规则 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 可破坏物列表 |

- 示例

```lua
local area = y3.area.create_circle_area(y3.point.create(0, 0, 0), 500)

local result = GameAPI.get_all_dest_in_area(area.handle, 1)
```

---

## get_all_dest_in_point_rng

method in GameAPI

- 描述

    获取点范围内的可破坏物列表

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.Point | 区域对象 |
    | rng | number | 半径 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 可破坏物列表 |

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)

local result = GameAPI.get_all_dest_in_point_rng(point, 1.0)
```

---

## get_all_dest_in_shapes

method in GameAPI

- 描述

    获取不同形状范围内的可破坏物列表

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.Point | 区域对象 |
    | shape | py.Shape | 形状 |
    | sort_type? | py.SortType | 筛选规则 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 可破坏物列表 |

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)
local shape = GlobalAPI.create_circular_shape(Fix32(500))

local result = GameAPI.get_all_dest_in_shapes(point, shape, 1)
```

---

## add_camera_conf

method in GameAPI

- 描述

    创建镜头

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | focus_point | py.FVector3 | 点 |
    | dis | number | 焦距 |
    | focus_y? | number | 焦点高度 |
    | yaw? | number | yaw |
    | pitch? | number | pitch |
    | fov? | number | fov |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 镜头ID |

- 示例

```lua
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

local result = GameAPI.add_camera_conf(fvector3, 1.0, 1.0, 1.0, 1.0, 1.0)
```

---

## apply_camera_conf

method in GameAPI

- 描述

    应用镜头配置

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | conf_id | py.Camera | 镜头配置 |
    | duration | number | 过渡时间 |
    | slope_mode? | integer | 镜头移动类型 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local camera = y3.camera.create_camera(y3.point(0, 0), 1000, 500, 0, 45, 3000)

GameAPI.apply_camera_conf(player.handle, camera.handle, 1.0, 1)
```

---

## camera_linear_move_duration

method in GameAPI

- 描述

    线性移动镜头(时间)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | point | py.FVector3 | 点 |
    | duration | py.Fixed | 持续时间 |
    | acc | integer | 加速度 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

GameAPI.camera_linear_move_duration(player.handle, fvector3, Fix32(1), 1)
```

---

## camera_linear_move_speed

method in GameAPI

- 描述

    线性移动镜头(初速度)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | point | py.FVector3 | 点 |
    | speed | py.Fixed | 初速度 |
    | acc | integer | 加速度 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

GameAPI.camera_linear_move_speed(player.handle, fvector3, Fix32(1), 1)
```

---

## camera_look_at

method in GameAPI

- 描述

    让镜头看向某点（镜头位置不变）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | point | py.FVector3 | 点 |
    | move_time? | py.Fixed | 时间 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

GameAPI.camera_look_at(player.handle, fvector3, Fix32(1))
```

---

## camera_set_param_roll

method in GameAPI

- 描述

    设置镜头参数roll

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | roll | py.Fixed | 滚动角 |
    | move_time? | py.Fixed | 时间 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.camera_set_param_roll(player.handle, Fix32(1), Fix32(1))
```

---

## camera_set_param_pitch

method in GameAPI

- 描述

    设置镜头参数pitch

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | pitch | py.Fixed | 俯仰角 |
    | move_time? | py.Fixed | 时间 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.camera_set_param_pitch(player.handle, Fix32(1), Fix32(1))
```

---

## camera_set_param_yaw

method in GameAPI

- 描述

    设置镜头参数yaw

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | yaw | py.Fixed | 导航角 |
    | move_time? | py.Fixed | 时间 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.camera_set_param_yaw(player.handle, Fix32(1), Fix32(1))
```

---

## camera_set_param_rotate

method in GameAPI

- 描述

    设置镜头角度参数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | rotate_type | py.CameraRotate | 角度类型 |
    | angle | py.Fixed | 角度值 |
    | move_time? | py.Fixed | 时间 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.camera_set_param_rotate(player.handle, 1, Fix32(1), Fix32(1))
```

---

## camera_set_param_distance

method in GameAPI

- 描述

    设置镜头参数distance

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | distance | py.Fixed | 焦点距离 |
    | move_time? | py.Fixed | 时间 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.camera_set_param_distance(player.handle, Fix32(1), Fix32(1))
```

---

## camera_rotate_pitch_angle_duration

method in GameAPI

- 描述

    旋转镜头俯仰角（角度，时间）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | angle | py.Fixed | 角度 |
    | duration | py.Fixed | 时间 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.camera_rotate_pitch_angle_duration(player.handle, Fix32(1), Fix32(1))
```

---

## camera_rotate_pitch_speed_duration

method in GameAPI

- 描述

    旋转镜头俯仰角（角速度，时间）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | angle_speed | py.Fixed | 角速度 |
    | duration | py.Fixed | 时间 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.camera_rotate_pitch_speed_duration(player.handle, Fix32(1), Fix32(1))
```

---

## camera_rotate_pitch_speed_angle

method in GameAPI

- 描述

    旋转镜头俯仰角（角速度，角度）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | angle_speed | py.Fixed | 角速度 |
    | angle | py.Fixed | 角度 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.camera_rotate_pitch_speed_angle(player.handle, Fix32(1), Fix32(1))
```

---

## camera_rotate_yaw_angle_duration

method in GameAPI

- 描述

    旋转镜头导航角（角度，时间）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | angle | py.Fixed | 角度 |
    | duration | py.Fixed | 时间 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.camera_rotate_yaw_angle_duration(player.handle, Fix32(1), Fix32(1))
```

---

## camera_rotate_yaw_speed_duration

method in GameAPI

- 描述

    旋转镜头导航角（角速度，时间）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | angle_speed | py.Fixed | 角速度 |
    | duration | py.Fixed | 时间 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.camera_rotate_yaw_speed_duration(player.handle, Fix32(1), Fix32(1))
```

---

## camera_rotate_yaw_speed_angle

method in GameAPI

- 描述

    旋转镜头导航角（角速度，角度）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | angle_speed | py.Fixed | 角速度 |
    | angle | py.Fixed | 角度 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.camera_rotate_yaw_speed_angle(player.handle, Fix32(1), Fix32(1))
```

---

## camera_rotate_roll_angle_duration

method in GameAPI

- 描述

    旋转镜头滚角（角度，时间）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | angle | py.Fixed | 角度 |
    | duration | py.Fixed | 时间 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.camera_rotate_roll_angle_duration(player.handle, Fix32(1), Fix32(1))
```

---

## camera_rotate_roll_speed_duration

method in GameAPI

- 描述

    旋转镜头滚角（角速度，时间）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | angle_speed | py.Fixed | 角速度 |
    | duration | py.Fixed | 时间 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.camera_rotate_roll_speed_duration(player.handle, Fix32(1), Fix32(1))
```

---

## camera_rotate_roll_speed_angle

method in GameAPI

- 描述

    旋转镜头滚角（角速度，角度）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | angle_speed | py.Fixed | 角速度 |
    | angle | py.Fixed | 角度 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.camera_rotate_roll_speed_angle(player.handle, Fix32(1), Fix32(1))
```

---

## camera_shake_xy

method in GameAPI

- 描述

    镜头摇晃xy

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | amplitude | py.Fixed | 摇晃幅度 |
    | speed | py.Fixed | 摇晃速率 |
    | duration | py.Fixed | 持续时间 |
    | t | integer | 摇晃方式 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.camera_shake_xy(player.handle, Fix32(1), Fix32(1), Fix32(1), 1)
```

---

## camera_shake_z

method in GameAPI

- 描述

    镜头摇晃z

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | amplitude | py.Fixed | 摇晃幅度 |
    | speed | py.Fixed | 摇晃速率 |
    | duration | py.Fixed | 持续时间 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.camera_shake_z(player.handle, Fix32(1), Fix32(1), Fix32(1))
```

---

## camera_shake

method in GameAPI

- 描述

    镜头摇晃xy

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | amplitude | py.Fixed | 摇晃幅度 |
    | speed | py.Fixed | 摇晃速率 |
    | duration | py.Fixed | 持续时间 |
    | shake_mode | integer | 摇晃方式 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.camera_shake(player.handle, Fix32(1), Fix32(1), Fix32(1), 1)
```

---

## camera_shake_with_decay

method in GameAPI

- 描述

    镜头带衰减震动

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | amplitude | py.Fixed | 震动幅度 |
    | decay | py.Fixed | 衰减速率 |
    | frequency | py.Fixed | 频率 |
    | duration | py.Fixed | 持续时间 |
    | shake_type | integer | 震动方式 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.camera_shake_with_decay(player.handle, Fix32(1), Fix32(1), Fix32(1), Fix32(1), 1)
```

---

## camera_limit_area

method in GameAPI

- 描述

    镜头限制移动区域

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | area | py.Area | 限制区域 |
    | clear_mover? | boolean | 超出区域是否停止mover |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local area = y3.area.create_circle_area(y3.point.create(0, 0, 0), 500)

GameAPI.camera_limit_area(player.handle, area.handle, true)
```

---

## camera_limit_area_close

method in GameAPI

- 描述

    镜头限制移动区域

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.camera_limit_area_close(player.handle)
```

---

## camera_set_follow_unit

method in GameAPI

- 描述

    镜头跟随某个单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | unit | py.Unit | 跟随单位 |
    | offset_x? | number | 偏移距离x |
    | offset_y? | number | 偏移距离y |
    | offset_height? | number | 偏移高度 |
    | socket? | string | 挂接点 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

GameAPI.camera_set_follow_unit(player.handle, unit.handle, 1.0, 1.0, 1.0, "socket")
```

---

## camera_set_tps_follow_unit

method in GameAPI

- 描述

    镜头tps跟随某个单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | unit | py.Unit | 跟随单位 |
    | sensitive? | number | 灵敏度 |
    | pitch? | number | 俯仰角 |
    | yaw? | number | 偏航角 |
    | offset_x? | number | 偏移距离x |
    | offset_y? | number | 偏移距离y |
    | offset_z? | number | 偏移高度 |
    | distance? | number | 摄像机距离 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

GameAPI.camera_set_tps_follow_unit(player.handle, unit.handle, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0)
```

---

## camera_cancel_tps_follow_unit

method in GameAPI

- 描述

    取消镜头tps跟随单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.camera_cancel_tps_follow_unit(player.handle)
```

---

## camera_cancel_follow_unit

method in GameAPI

- 描述

    将玩家相机解除绑定

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.camera_cancel_follow_unit(player.handle)
```

---

## camera_is_following_target

method in GameAPI

- 描述

    本地镜头在跟随状态

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否跟随 |

- 示例

```lua
local result = GameAPI.camera_is_following_target()
```

---

## camera_set_focus_y

method in GameAPI

- 描述

    设置玩家镜头焦点高度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | y | py.Fixed | 高度 |
    | move_time? | py.Fixed | 时间 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.camera_set_focus_y(player.handle, Fix32(1), Fix32(1))
```

---

## camera_set_move_enable

method in GameAPI

- 描述

    设置玩家相机允许移动

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.camera_set_move_enable(player.handle)
```

---

## camera_set_move_not_enable

method in GameAPI

- 描述

    设置玩家相机禁止移动

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.camera_set_move_not_enable(player.handle)
```

---

## set_tps_mode_ctrl

method in GameAPI

- 描述

    设置第三人称跟随镜头鼠标控制开关

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | enable | boolean | 开关 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_tps_mode_ctrl(player.handle, true)
```

---

## get_camera_attr_real_num

method in GameAPI

- 描述

    获取本地玩家镜头的实数属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr_name | string | 属性名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 属性值 |

- 示例

```lua
local result = GameAPI.get_camera_attr_real_num("attr_name")
```

---

## get_camera_attr_integer

method in GameAPI

- 描述

    获取本地玩家镜头的整数属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr_name | string | 属性名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 属性值 |

- 示例

```lua
local result = GameAPI.get_camera_attr_integer("attr_name")
```

---

## api_show_text

method in GameAPI

- 描述

    向玩家正上方显示提示信息

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | seconds? | number | 持续时间 |
    | text? | string | 信息 |
    | localize? | boolean | 多语言转化 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.api_show_text(player.handle, 1.0, "text", true)
```

---

## show_tips_text

method in GameAPI

- 描述

    向玩家显示多语言信息

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | text | string | 显示信息 |
    | second | py.Fixed | 持续时间, 单位秒 |
    | localize? | boolean | 多语言转化 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.show_tips_text(player.handle, "text", Fix32(1), true)
```

---

## api_test_log_msg

method in GameAPI

- 描述

    API测试记录日志并可选显示

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | text | string | 信息 |
    | seconds | py.Fixed | 持续时间, 单位秒 |
    | show | boolean | 是否在屏幕显示 |

- 返回值

    无

- 示例

```lua
GameAPI.api_test_log_msg("text", Fix32(1), true)
```

---

## api_test_show_msg_tip

method in GameAPI

- 描述

    API测试显示UI信息

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | text | string | 信息 |
    | seconds | py.Fixed | 持续时间, 单位秒 |

- 返回值

    无

- 示例

```lua
GameAPI.api_test_show_msg_tip("text", Fix32(1))
```

---

## api_test_add_log_assert_result

method in GameAPI

- 描述

    API测试-向Log添加Assert结果

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_pass | boolean | 是否通过 |
    | info_str | string | 信息 |

- 返回值

    无

- 示例

```lua
GameAPI.api_test_add_log_assert_result(true, "info_str")
```

---

## print_to_dialog

method in GameAPI

- 描述

    Dialog窗口输出信息

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | type | integer | 窗口等级 |
    | text | string | 打印信息 |
    | trigger_info? | py.Dict | 字典 |

- 返回值

    无

- 示例

```lua
local dict = pydict()

GameAPI.print_to_dialog(1, "text")
```

---

## show_unit_text_to_role

method in GameAPI

- 描述

    向玩家显示单位对话

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | role | py.Role | 玩家 |
    | text | string | 信息 |
    | second | py.Fixed | 持续时间 |
    | localize? | boolean | 多语言转化 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

GameAPI.show_unit_text_to_role(unit.handle, player.handle, "text", Fix32(1), true)
```

---

## show_msg_to_role

method in GameAPI

- 描述

    向玩家左下角显示信息

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | text | string | 信息 |
    | localize? | boolean | 多语言转化 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.show_msg_to_role(player.handle, "text", true)
```

---

## show_game_end_ui_by_camp_id

method in GameAPI

- 描述

    按阵营显示游戏结束信息

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | camp_id | py.CampID | 阵营编号 |
    | result | string | 结束信息 |

- 返回值

    无

- 示例

```lua
GameAPI.show_game_end_ui_by_camp_id(1, "result")
```

---

## get_random_int

method in GameAPI

- 描述

    范围内随机整数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | min_num | integer | 最小值 |
    | max_num | integer | 最大值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 随机整数 |

- 示例

```lua
local result = GameAPI.get_random_int(1, 1)
```

---

## get_random_fixed

method in GameAPI

- 描述

    范围内随机定点数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | min_num | py.Fixed | 最小值 |
    | max_num | py.Fixed | 最大值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 随机定点数 |

- 示例

```lua
local result = GameAPI.get_random_fixed(Fix32(1), Fix32(1))
```

---

## get_random_angle

method in GameAPI

- 描述

    随机角度

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 随机定点数 |

- 示例

```lua
local result = GameAPI.get_random_angle()
```

---

## api_calc_formula_kv

method in GameAPI

- 描述

    计算公式类型KV

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 公式所属对象 |
    | k | string | key |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.api_calc_formula_kv(actor, "k")
```

---

## get_unit_group_num

method in GameAPI

- 描述

    单位组内所有状态的单位数量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_group | py.UnitGroup | 单位组 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 单位数量 |

- 示例

```lua
local unit_group = y3.unit_group.create()

local result = GameAPI.get_unit_group_num(unit_group.handle)
```

---

## refresh_unit_group

method in GameAPI

- 描述

    遍历时过滤单位组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_group | py.UnitGroup | 单位组 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitGroup | 单位组 |

- 示例

```lua
local unit_group = y3.unit_group.create()

local result = GameAPI.refresh_unit_group(unit_group.handle)
```

---

## refresh_projectile_group

method in GameAPI

- 描述

    遍历时过滤投射物组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | proj_group | py.UnitGroup | 投射物组 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitGroup | 投射物组 |

- 示例

```lua
local unit_group = y3.unit_group.create()

local result = GameAPI.refresh_projectile_group(unit_group.handle)
```

---

## get_state_unit_num_in_group

method in GameAPI

- 描述

    单位组某状态的单位数量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_group | py.UnitGroup | 单位组 |
    | status | string | 状态名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 单位数量 |

- 示例

```lua
local unit_group = y3.unit_group.create()

local result = GameAPI.get_state_unit_num_in_group(unit_group.handle, "status")
```

---

## get_num_of_unit_key_in_group

method in GameAPI

- 描述

    单位组中特定单位编号的单位数量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_group | py.UnitGroup | 单位组 |
    | unit_key | py.UnitKey | 单位编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 无符号整型 |

- 示例

```lua
local unit_group = y3.unit_group.create()
local unit_key = 134274569

local result = GameAPI.get_num_of_unit_key_in_group(unit_group.handle, unit_key)
```

---

## remove_unit_in_group_by_key

method in GameAPI

- 描述

    删除单位组中某种单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_group | py.UnitGroup | 单位组 |
    | unit_key | py.UnitKey | 单位编号 |

- 返回值

    无

- 示例

```lua
local unit_group = y3.unit_group.create()
local unit_key = 134274569

GameAPI.remove_unit_in_group_by_key(unit_group.handle, unit_key)
```

---

## remove_unit_in_group

method in GameAPI

- 描述

    删除单位组中某个单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_group | py.UnitGroup | 单位组 |
    | unit | py.Unit | 单位 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local unit_group = y3.unit_group.create()

GameAPI.remove_unit_in_group(unit_group.handle, unit.handle)
```

---

## set_unit_group_selected

method in GameAPI

- 描述

    设置单位组中单位选中

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_group_id | py.UnitGroup | 单位组 |

- 返回值

    无

- 示例

```lua
local unit_group = y3.unit_group.create()

GameAPI.set_unit_group_selected(unit_group.handle)
```

---

## unit_key_pool_add_key

method in GameAPI

- 描述

    单位编号池添加单位编号

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | pool | py.UnitKeyPool | 单位编号池 |
    | key | py.UnitKey | 单位编号 |
    | pro | py.Fixed | 定点数 |

- 返回值

    无

- 示例

```lua
local unit_key_pool = GlobalAPI.get_empty_unit_key_pool()
local unit_key = 134274569

GameAPI.unit_key_pool_add_key(unit_key_pool, unit_key, Fix32(1))
```

---

## unit_key_pool_rem_key

method in GameAPI

- 描述

    单位编号池删除单位编号

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | pool | py.UnitKeyPool | 单位编号池 |
    | key | py.UnitKey | 单位编号 |

- 返回值

    无

- 示例

```lua
local unit_key_pool = GlobalAPI.get_empty_unit_key_pool()
local unit_key = 134274569

GameAPI.unit_key_pool_rem_key(unit_key_pool, unit_key)
```

---

## get_unit_key_from_pool

method in GameAPI

- 描述

    单位编号池返回单位编号

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | pool | py.UnitKeyPool | 单位编号池 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitKey | 单位编号 |

- 示例

```lua
local unit_key_pool = GlobalAPI.get_empty_unit_key_pool()

local result = GameAPI.get_unit_key_from_pool(unit_key_pool)
```

---

## get_unit_key_icon

method in GameAPI

- 描述

    获取单位预设库配置的图标路径

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | py.UnitKey | 单位编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 图标 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_icon(unit_key)
```

---

## get_item_key_icon

method in GameAPI

- 描述

    获取物品预设库配置的图标路径

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | py.ItemKey | 物品编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 图标 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_icon(item_key)
```

---

## get_unit_key_pic

method in GameAPI

- 描述

    获取单位预设库配置的图片路径

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | py.UnitKey | 单位编号 |
    | pic_type | string | 图片类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 图片 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_pic(unit_key, "pic_type")
```

---

## get_unit_key_str

method in GameAPI

- 描述

    获取单位预设库配置的类型为字符串的属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | attr | string | 属性名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串属性值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_str(unit_key, "attr")
```

---

## get_unit_key_fixed

method in GameAPI

- 描述

    获取单位预设库配置的类型为实数的属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | attr | string | 属性名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 实数属性值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_fixed(unit_key, "attr")
```

---

## get_icon_by_uid

method in GameAPI

- 描述

    根据UID获取预设库配置的图标路径

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_uid | string | 图标唯一ID |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 图标 |

- 示例

```lua
local result = GameAPI.get_icon_by_uid("icon_uid")
```

---

## get_ability_key_icon

method in GameAPI

- 描述

    获取技能预设库配置的图标路径

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | py.AbilityKey | 技能编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 图标 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_icon(ability_key)
```

---

## len_of_var

method in GameAPI

- 描述

    变量长度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | var | py.List | 变量 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 变量长度 |

- 示例

```lua
local list = {}

local result = GameAPI.len_of_var(list)
```

---

## get_slave_coeff

method in GameAPI

- 描述

    获取三维属性的slave系数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | pri | string | 三维属性 |
    | slave | string | slave属性 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | slave系数 |

- 示例

```lua
local result = GameAPI.get_slave_coeff("pri", "slave")
```

---

## set_slave_coeff

method in GameAPI

- 描述

    设置三维属性的slave系数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | pri | string | 三维属性 |
    | slave | string | slave属性 |
    | coeff | py.Fixed | slave系数 |

- 返回值

    无

- 示例

```lua
GameAPI.set_slave_coeff("pri", "slave", Fix32(1))
```

---

## get_damage_ratio

method in GameAPI

- 描述

    攻击类型和防御类型对应的伤害系数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attack_idx | integer | 攻击类型 |
    | armor_idx | integer | 防御类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 伤害系数 |

- 示例

```lua
local result = GameAPI.get_damage_ratio(1, 1)
```

---

## set_damage_ratio

method in GameAPI

- 描述

    设置攻击类型和防御类型对应的伤害系数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attack_idx | integer | 攻击类型 |
    | armor_idx | integer | 防御类型 |
    | damage_ratio | py.Fixed | 伤害系数 |

- 返回值

    无

- 示例

```lua
GameAPI.set_damage_ratio(1, 1, Fix32(1))
```

---

## apply_damage

method in GameAPI

- 描述

    应用伤害

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | source_unit? | py.Unit | 伤害者 |
    | ability? | py.Ability | 来源关联技能 |
    | target_unit? | py.Unit | 单位或者物品 |
    | damage_type? | integer | 伤害类型 |
    | damage? | py.Fixed | 伤害值 |
    | jump_word? | boolean | 是否跳字 |
    | extra_context? | py.Actor | extra_data |
    | as_normal_hit? | boolean | 视为普攻 |
    | critical? | boolean | 必定暴击 |
    | no_miss? | boolean | 无视闪避 |
    | hit_sfx? | py.SfxKey | 受击特效 |
    | hit_socket? | string | 挂接点 |
    | harm_text_enum? | string | 跳字枚举 |
    | jump_word_track? | integer | 跳字轨迹 |
    | attack_type? | integer | 攻击类型 |
    | pos_socket? | string | 跳字起始位置挂节点 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)
local actor = unit.handle
local sfx_key = 134274569

GameAPI.apply_damage(nil, nil, nil, 1, Fix32(1), true, nil, true, true, true, nil, "hit_socket", "harm_text_enum", 1, 1, "pos_socket")
```

---

## get_hurt_damage

method in GameAPI

- 描述

    攻击伤害绝对值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | damage | py.Fixed | 伤害值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 伤害绝对值 |

- 示例

```lua
local result = GameAPI.get_hurt_damage(Fix32(1))
```

---

## set_cur_damage

method in GameAPI

- 描述

    设置当前攻击伤害的数值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | damage | py.Fixed | 伤害值 |

- 返回值

    无

- 示例

```lua
GameAPI.set_cur_damage(Fix32(1))
```

---

## get_cur_damage_is_miss

method in GameAPI

- 描述

    获取当次攻击是否闪避

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | damage_result_state | integer | damage_result_state |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 伤害绝对值 |

- 示例

```lua
local result = GameAPI.get_cur_damage_is_miss(1)
```

---

## get_item_key_unit_group_command_type_kv

method in GameAPI

- 描述

    获取物品编号UNIT_GROUP_COMMAND_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitGroupCommandType | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_unit_group_command_type_kv(item_key, "key")
```

---

## get_ability_key_unit_group_command_type_kv

method in GameAPI

- 描述

    获取技能编号UNIT_GROUP_COMMAND_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitGroupCommandType | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_unit_group_command_type_kv(ability_key, "key")
```

---

## get_modifier_key_unit_group_command_type_kv

method in GameAPI

- 描述

    获取魔法效果特效编号UNIT_GROUP_COMMAND_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitGroupCommandType | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_unit_group_command_type_kv(modifier_key, "key")
```

---

## get_projectile_key_unit_group_command_type_kv

method in GameAPI

- 描述

    获取特效编号UNIT_GROUP_COMMAND_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitGroupCommandType | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_unit_group_command_type_kv(projectile_key, "key")
```

---

## get_destructible_key_unit_group_command_type_kv

method in GameAPI

- 描述

    获取可破坏物编号UNIT_GROUP_COMMAND_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitGroupCommandType | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_unit_group_command_type_kv(destructible_key, "key")
```

---

## get_tech_key_unit_group_command_type_kv

method in GameAPI

- 描述

    获取科技编号UNIT_GROUP_COMMAND_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitGroupCommandType | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_unit_group_command_type_kv(tech_key, "key")
```

---

## get_icon_id_unit_group_command_type_kv

method in GameAPI

- 描述

    获取图片UNIT_GROUP_COMMAND_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitGroupCommandType | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_unit_group_command_type_kv(1, "key")
```

---

## get_physics_entity_key_unit_group_command_type_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型UNIT_GROUP_COMMAND_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitGroupCommandType | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_unit_group_command_type_kv(1, "key")
```

---

## get_kv_pair_value_unit_group_command_type

method in GameAPI

- 描述

    获取UNIT_GROUP_COMMAND_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitGroupCommandType | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_unit_group_command_type(kvbase, "key")
```

---

## get_unit_key_rescue_seeker_type_kv

method in GameAPI

- 描述

    获取单位编号RESCUE_SEEKER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ERescueSeekerType | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_rescue_seeker_type_kv(unit_key, "key")
```

---

## get_item_key_rescue_seeker_type_kv

method in GameAPI

- 描述

    获取物品编号RESCUE_SEEKER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ERescueSeekerType | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_rescue_seeker_type_kv(item_key, "key")
```

---

## get_ability_key_rescue_seeker_type_kv

method in GameAPI

- 描述

    获取技能编号RESCUE_SEEKER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ERescueSeekerType | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_rescue_seeker_type_kv(ability_key, "key")
```

---

## get_modifier_key_rescue_seeker_type_kv

method in GameAPI

- 描述

    获取魔法效果特效编号RESCUE_SEEKER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ERescueSeekerType | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_rescue_seeker_type_kv(modifier_key, "key")
```

---

## get_projectile_key_rescue_seeker_type_kv

method in GameAPI

- 描述

    获取特效编号RESCUE_SEEKER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ERescueSeekerType | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_rescue_seeker_type_kv(projectile_key, "key")
```

---

## get_destructible_key_rescue_seeker_type_kv

method in GameAPI

- 描述

    获取可破坏物编号RESCUE_SEEKER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ERescueSeekerType | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_rescue_seeker_type_kv(destructible_key, "key")
```

---

## get_tech_key_rescue_seeker_type_kv

method in GameAPI

- 描述

    获取科技编号RESCUE_SEEKER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ERescueSeekerType | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_rescue_seeker_type_kv(tech_key, "key")
```

---

## get_icon_id_rescue_seeker_type_kv

method in GameAPI

- 描述

    获取图片RESCUE_SEEKER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ERescueSeekerType | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_rescue_seeker_type_kv(1, "key")
```

---

## get_physics_entity_key_rescue_seeker_type_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型RESCUE_SEEKER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ERescueSeekerType | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_rescue_seeker_type_kv(1, "key")
```

---

## get_kv_pair_value_rescue_seeker_type

method in GameAPI

- 描述

    获取RESCUE_SEEKER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ERescueSeekerType | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_rescue_seeker_type(kvbase, "key")
```

---

## get_unit_key_rescuer_type_kv

method in GameAPI

- 描述

    获取单位编号RESCUER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ERescuerType | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_rescuer_type_kv(unit_key, "key")
```

---

## get_item_key_rescuer_type_kv

method in GameAPI

- 描述

    获取物品编号RESCUER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ERescuerType | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_rescuer_type_kv(item_key, "key")
```

---

## get_ability_key_rescuer_type_kv

method in GameAPI

- 描述

    获取技能编号RESCUER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ERescuerType | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_rescuer_type_kv(ability_key, "key")
```

---

## get_modifier_key_rescuer_type_kv

method in GameAPI

- 描述

    获取魔法效果特效编号RESCUER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ERescuerType | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_rescuer_type_kv(modifier_key, "key")
```

---

## get_projectile_key_rescuer_type_kv

method in GameAPI

- 描述

    获取特效编号RESCUER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ERescuerType | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_rescuer_type_kv(projectile_key, "key")
```

---

## get_destructible_key_rescuer_type_kv

method in GameAPI

- 描述

    获取可破坏物编号RESCUER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ERescuerType | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_rescuer_type_kv(destructible_key, "key")
```

---

## get_tech_key_rescuer_type_kv

method in GameAPI

- 描述

    获取科技编号RESCUER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ERescuerType | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_rescuer_type_kv(tech_key, "key")
```

---

## get_icon_id_rescuer_type_kv

method in GameAPI

- 描述

    获取图片RESCUER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ERescuerType | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_rescuer_type_kv(1, "key")
```

---

## get_physics_entity_key_rescuer_type_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型RESCUER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ERescuerType | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_rescuer_type_kv(1, "key")
```

---

## get_kv_pair_value_rescuer_type

method in GameAPI

- 描述

    获取RESCUER_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ERescuerType | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_rescuer_type(kvbase, "key")
```

---

## get_unit_key_store_item_type_kv

method in GameAPI

- 描述

    获取单位编号STORE_ITEM_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.StoreItemType | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_store_item_type_kv(unit_key, "key")
```

---

## get_item_key_store_item_type_kv

method in GameAPI

- 描述

    获取物品编号STORE_ITEM_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.StoreItemType | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_store_item_type_kv(item_key, "key")
```

---

## get_ability_key_store_item_type_kv

method in GameAPI

- 描述

    获取技能编号STORE_ITEM_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.StoreItemType | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_store_item_type_kv(ability_key, "key")
```

---

## get_modifier_key_store_item_type_kv

method in GameAPI

- 描述

    获取魔法效果特效编号STORE_ITEM_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.StoreItemType | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_store_item_type_kv(modifier_key, "key")
```

---

## get_projectile_key_store_item_type_kv

method in GameAPI

- 描述

    获取特效编号STORE_ITEM_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.StoreItemType | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_store_item_type_kv(projectile_key, "key")
```

---

## get_destructible_key_store_item_type_kv

method in GameAPI

- 描述

    获取可破坏物编号STORE_ITEM_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.StoreItemType | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_store_item_type_kv(destructible_key, "key")
```

---

## get_tech_key_store_item_type_kv

method in GameAPI

- 描述

    获取科技编号STORE_ITEM_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.StoreItemType | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_store_item_type_kv(tech_key, "key")
```

---

## get_icon_id_store_item_type_kv

method in GameAPI

- 描述

    获取图片STORE_ITEM_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.StoreItemType | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_store_item_type_kv(1, "key")
```

---

## get_physics_entity_key_store_item_type_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型STORE_ITEM_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.StoreItemType | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_store_item_type_kv(1, "key")
```

---

## get_kv_pair_value_store_item_type

method in GameAPI

- 描述

    获取STORE_ITEM_TYPE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.StoreItemType | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_store_item_type(kvbase, "key")
```

---

## get_unit_key_site_state_kv

method in GameAPI

- 描述

    获取单位编号SITE_STATE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SITE_STATE | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_site_state_kv(unit_key, "key")
```

---

## get_item_key_site_state_kv

method in GameAPI

- 描述

    获取物品编号SITE_STATE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SITE_STATE | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_site_state_kv(item_key, "key")
```

---

## get_ability_key_site_state_kv

method in GameAPI

- 描述

    获取技能编号SITE_STATE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SITE_STATE | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_site_state_kv(ability_key, "key")
```

---

## get_modifier_key_site_state_kv

method in GameAPI

- 描述

    获取魔法效果特效编号SITE_STATE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SITE_STATE | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_site_state_kv(modifier_key, "key")
```

---

## get_projectile_key_site_state_kv

method in GameAPI

- 描述

    获取特效编号SITE_STATE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SITE_STATE | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_site_state_kv(projectile_key, "key")
```

---

## get_destructible_key_site_state_kv

method in GameAPI

- 描述

    获取可破坏物编号SITE_STATE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SITE_STATE | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_site_state_kv(destructible_key, "key")
```

---

## get_tech_key_site_state_kv

method in GameAPI

- 描述

    获取科技编号SITE_STATE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SITE_STATE | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_site_state_kv(tech_key, "key")
```

---

## get_icon_id_site_state_kv

method in GameAPI

- 描述

    获取图片SITE_STATE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SITE_STATE | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_site_state_kv(1, "key")
```

---

## get_physics_entity_key_site_state_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型SITE_STATE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SITE_STATE | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_site_state_kv(1, "key")
```

---

## get_kv_pair_value_site_state

method in GameAPI

- 描述

    获取SITE_STATE键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SITE_STATE | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_site_state(kvbase, "key")
```

---

## get_unit_key_coin_currency_kv

method in GameAPI

- 描述

    获取单位编号COIN_CURRENCY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.COIN_CURRENCY | 键值 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_unit_key_coin_currency_kv(unit_key, "key")
```

---

## get_item_key_coin_currency_kv

method in GameAPI

- 描述

    获取物品编号COIN_CURRENCY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.COIN_CURRENCY | 键值 |

- 示例

```lua
local item_key = 134274569

local result = GameAPI.get_item_key_coin_currency_kv(item_key, "key")
```

---

## get_ability_key_coin_currency_kv

method in GameAPI

- 描述

    获取技能编号COIN_CURRENCY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.COIN_CURRENCY | 键值 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.get_ability_key_coin_currency_kv(ability_key, "key")
```

---

## get_modifier_key_coin_currency_kv

method in GameAPI

- 描述

    获取魔法效果特效编号COIN_CURRENCY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_key | py.ModifierKey | 魔法效果编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.COIN_CURRENCY | 键值 |

- 示例

```lua
local modifier_key = 134274569

local result = GameAPI.get_modifier_key_coin_currency_kv(modifier_key, "key")
```

---

## get_projectile_key_coin_currency_kv

method in GameAPI

- 描述

    获取特效编号COIN_CURRENCY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_key | py.ProjectileKey | 特效编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.COIN_CURRENCY | 键值 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_key_coin_currency_kv(projectile_key, "key")
```

---

## get_destructible_key_coin_currency_kv

method in GameAPI

- 描述

    获取可破坏物编号COIN_CURRENCY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible_key | py.DestructibleKey | 可破坏物编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.COIN_CURRENCY | 键值 |

- 示例

```lua
local destructible_key = 1

local result = GameAPI.get_destructible_key_coin_currency_kv(destructible_key, "key")
```

---

## get_tech_key_coin_currency_kv

method in GameAPI

- 描述

    获取科技编号COIN_CURRENCY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_key | py.TechKey | 科技编号 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.COIN_CURRENCY | 键值 |

- 示例

```lua
local tech_key = 134274569

local result = GameAPI.get_tech_key_coin_currency_kv(tech_key, "key")
```

---

## get_icon_id_coin_currency_kv

method in GameAPI

- 描述

    获取图片COIN_CURRENCY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图片 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.COIN_CURRENCY | 键值 |

- 示例

```lua
local result = GameAPI.get_icon_id_coin_currency_kv(1, "key")
```

---

## get_physics_entity_key_coin_currency_kv

method in GameAPI

- 描述

    获取逻辑物理组件类型COIN_CURRENCY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | physics_entity_key | py.PhysicsEntityKey | 逻辑物理组件类型 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.COIN_CURRENCY | 键值 |

- 示例

```lua
local result = GameAPI.get_physics_entity_key_coin_currency_kv(1, "key")
```

---

## get_kv_pair_value_coin_currency

method in GameAPI

- 描述

    获取COIN_CURRENCY键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 自定义键值载体 |
    | key | string | 键名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.COIN_CURRENCY | 键值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

local result = GameAPI.get_kv_pair_value_coin_currency(kvbase, "key")
```

---

## get_trigger_variable_ui_gridview_type

method in GameAPI

- 描述

    获取全局触发器UI_GRIDVIEW_TYPE非数组变量

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
local result = GameAPI.get_trigger_variable_ui_gridview_type("key")
```

---

## get_trigger_actor_variable_ui_gridview_type

method in GameAPI

- 描述

    获取触发器UI_GRIDVIEW_TYPE非数组 组变量

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

local result = GameAPI.get_trigger_actor_variable_ui_gridview_type(actor, "key")
```

---

## get_trigger_list_variable_ui_gridview_type

method in GameAPI

- 描述

    获取全局触发器UI_GRIDVIEW_TYPE数组变量子项

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
local result = GameAPI.get_trigger_list_variable_ui_gridview_type("key", 1)
```

---

## get_trigger_list_actor_variable_ui_gridview_type

method in GameAPI

- 描述

    获取触发器UI_GRIDVIEW_TYPE数组 组变量子项

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

local result = GameAPI.get_trigger_list_actor_variable_ui_gridview_type(actor, "key", 1)
```

---

## get_trigger_list_variable_all_ui_gridview_type

method in GameAPI

- 描述

    获取全局触发器UI_GRIDVIEW_TYPE数组变量

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
local result = GameAPI.get_trigger_list_variable_all_ui_gridview_type("key")
```

---

## get_trigger_list_actor_variable_all_ui_gridview_type

method in GameAPI

- 描述

    获取触发器UI_GRIDVIEW_TYPE 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_ui_gridview_type(actor, "key")
```

---

## get_trigger_variable_ui_gridview_bar_type

method in GameAPI

- 描述

    获取全局触发器UI_GRIDVIEW_BAR_TYPE非数组变量

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
local result = GameAPI.get_trigger_variable_ui_gridview_bar_type("key")
```

---

## get_trigger_actor_variable_ui_gridview_bar_type

method in GameAPI

- 描述

    获取触发器UI_GRIDVIEW_BAR_TYPE非数组 组变量

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

local result = GameAPI.get_trigger_actor_variable_ui_gridview_bar_type(actor, "key")
```

---

## get_trigger_list_variable_ui_gridview_bar_type

method in GameAPI

- 描述

    获取全局触发器UI_GRIDVIEW_BAR_TYPE数组变量子项

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
local result = GameAPI.get_trigger_list_variable_ui_gridview_bar_type("key", 1)
```

---

## get_trigger_list_actor_variable_ui_gridview_bar_type

method in GameAPI

- 描述

    获取触发器UI_GRIDVIEW_BAR_TYPE数组 组变量子项

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

local result = GameAPI.get_trigger_list_actor_variable_ui_gridview_bar_type(actor, "key", 1)
```

---

## get_trigger_list_variable_all_ui_gridview_bar_type

method in GameAPI

- 描述

    获取全局触发器UI_GRIDVIEW_BAR_TYPE数组变量

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
local result = GameAPI.get_trigger_list_variable_all_ui_gridview_bar_type("key")
```

---

## get_trigger_list_actor_variable_all_ui_gridview_bar_type

method in GameAPI

- 描述

    获取触发器UI_GRIDVIEW_BAR_TYPE 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_ui_gridview_bar_type(actor, "key")
```

---

## get_trigger_variable_ui_effect_camera_mode

method in GameAPI

- 描述

    获取全局触发器UI_EFFECT_CAMERA_MODE非数组变量

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
local result = GameAPI.get_trigger_variable_ui_effect_camera_mode("key")
```

---

## get_trigger_actor_variable_ui_effect_camera_mode

method in GameAPI

- 描述

    获取触发器UI_EFFECT_CAMERA_MODE非数组 组变量

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

local result = GameAPI.get_trigger_actor_variable_ui_effect_camera_mode(actor, "key")
```

---

## get_trigger_list_variable_ui_effect_camera_mode

method in GameAPI

- 描述

    获取全局触发器UI_EFFECT_CAMERA_MODE数组变量子项

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
local result = GameAPI.get_trigger_list_variable_ui_effect_camera_mode("key", 1)
```

---

## get_trigger_list_actor_variable_ui_effect_camera_mode

method in GameAPI

- 描述

    获取触发器UI_EFFECT_CAMERA_MODE数组 组变量子项

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

local result = GameAPI.get_trigger_list_actor_variable_ui_effect_camera_mode(actor, "key", 1)
```

---

## get_trigger_list_variable_all_ui_effect_camera_mode

method in GameAPI

- 描述

    获取全局触发器UI_EFFECT_CAMERA_MODE数组变量

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
local result = GameAPI.get_trigger_list_variable_all_ui_effect_camera_mode("key")
```

---

## get_trigger_list_actor_variable_all_ui_effect_camera_mode

method in GameAPI

- 描述

    获取触发器UI_EFFECT_CAMERA_MODE 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_ui_effect_camera_mode(actor, "key")
```

---

## get_trigger_variable_ui_equip_slot_use_type

method in GameAPI

- 描述

    获取全局触发器UI_EQUIP_SLOT_USE_TYPE非数组变量

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
local result = GameAPI.get_trigger_variable_ui_equip_slot_use_type("key")
```

---

## get_trigger_actor_variable_ui_equip_slot_use_type

method in GameAPI

- 描述

    获取触发器UI_EQUIP_SLOT_USE_TYPE非数组 组变量

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

local result = GameAPI.get_trigger_actor_variable_ui_equip_slot_use_type(actor, "key")
```

---

## get_trigger_list_variable_ui_equip_slot_use_type

method in GameAPI

- 描述

    获取全局触发器UI_EQUIP_SLOT_USE_TYPE数组变量子项

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
local result = GameAPI.get_trigger_list_variable_ui_equip_slot_use_type("key", 1)
```

---

## get_trigger_list_actor_variable_ui_equip_slot_use_type

method in GameAPI

- 描述

    获取触发器UI_EQUIP_SLOT_USE_TYPE数组 组变量子项

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

local result = GameAPI.get_trigger_list_actor_variable_ui_equip_slot_use_type(actor, "key", 1)
```

---

## get_trigger_list_variable_all_ui_equip_slot_use_type

method in GameAPI

- 描述

    获取全局触发器UI_EQUIP_SLOT_USE_TYPE数组变量

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
local result = GameAPI.get_trigger_list_variable_all_ui_equip_slot_use_type("key")
```

---

## get_trigger_list_actor_variable_all_ui_equip_slot_use_type

method in GameAPI

- 描述

    获取触发器UI_EQUIP_SLOT_USE_TYPE 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_ui_equip_slot_use_type(actor, "key")
```

---

## get_trigger_variable_ui_equip_slot_drag_type

method in GameAPI

- 描述

    获取全局触发器UI_EQUIP_SLOT_DRAG_TYPE非数组变量

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
local result = GameAPI.get_trigger_variable_ui_equip_slot_drag_type("key")
```

---

## get_trigger_actor_variable_ui_equip_slot_drag_type

method in GameAPI

- 描述

    获取触发器UI_EQUIP_SLOT_DRAG_TYPE非数组 组变量

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

local result = GameAPI.get_trigger_actor_variable_ui_equip_slot_drag_type(actor, "key")
```

---

## get_trigger_list_variable_ui_equip_slot_drag_type

method in GameAPI

- 描述

    获取全局触发器UI_EQUIP_SLOT_DRAG_TYPE数组变量子项

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
local result = GameAPI.get_trigger_list_variable_ui_equip_slot_drag_type("key", 1)
```

---

## get_trigger_list_actor_variable_ui_equip_slot_drag_type

method in GameAPI

- 描述

    获取触发器UI_EQUIP_SLOT_DRAG_TYPE数组 组变量子项

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

local result = GameAPI.get_trigger_list_actor_variable_ui_equip_slot_drag_type(actor, "key", 1)
```

---

## get_trigger_list_variable_all_ui_equip_slot_drag_type

method in GameAPI

- 描述

    获取全局触发器UI_EQUIP_SLOT_DRAG_TYPE数组变量

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
local result = GameAPI.get_trigger_list_variable_all_ui_equip_slot_drag_type("key")
```

---

## get_trigger_list_actor_variable_all_ui_equip_slot_drag_type

method in GameAPI

- 描述

    获取触发器UI_EQUIP_SLOT_DRAG_TYPE 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_ui_equip_slot_drag_type(actor, "key")
```

---

## get_trigger_variable_ui_layout_clipping_type

method in GameAPI

- 描述

    获取全局触发器UI_LAYOUT_CLIPPING_TYPE非数组变量

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
local result = GameAPI.get_trigger_variable_ui_layout_clipping_type("key")
```

---

## get_trigger_actor_variable_ui_layout_clipping_type

method in GameAPI

- 描述

    获取触发器UI_LAYOUT_CLIPPING_TYPE非数组 组变量

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

local result = GameAPI.get_trigger_actor_variable_ui_layout_clipping_type(actor, "key")
```

---

## get_trigger_list_variable_ui_layout_clipping_type

method in GameAPI

- 描述

    获取全局触发器UI_LAYOUT_CLIPPING_TYPE数组变量子项

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
local result = GameAPI.get_trigger_list_variable_ui_layout_clipping_type("key", 1)
```

---

## get_trigger_list_actor_variable_ui_layout_clipping_type

method in GameAPI

- 描述

    获取触发器UI_LAYOUT_CLIPPING_TYPE数组 组变量子项

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

local result = GameAPI.get_trigger_list_actor_variable_ui_layout_clipping_type(actor, "key", 1)
```

---

## get_trigger_list_variable_all_ui_layout_clipping_type

method in GameAPI

- 描述

    获取全局触发器UI_LAYOUT_CLIPPING_TYPE数组变量

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
local result = GameAPI.get_trigger_list_variable_all_ui_layout_clipping_type("key")
```

---

## get_trigger_list_actor_variable_all_ui_layout_clipping_type

method in GameAPI

- 描述

    获取触发器UI_LAYOUT_CLIPPING_TYPE 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_ui_layout_clipping_type(actor, "key")
```

---

## get_trigger_variable_ui_text_over_length_handling_type

method in GameAPI

- 描述

    获取全局触发器UI_TEXT_OVER_LENGTH_HANDLING_TYPE非数组变量

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
local result = GameAPI.get_trigger_variable_ui_text_over_length_handling_type("key")
```

---

## get_trigger_actor_variable_ui_text_over_length_handling_type

method in GameAPI

- 描述

    获取触发器UI_TEXT_OVER_LENGTH_HANDLING_TYPE非数组 组变量

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

local result = GameAPI.get_trigger_actor_variable_ui_text_over_length_handling_type(actor, "key")
```

---

## get_trigger_list_variable_ui_text_over_length_handling_type

method in GameAPI

- 描述

    获取全局触发器UI_TEXT_OVER_LENGTH_HANDLING_TYPE数组变量子项

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
local result = GameAPI.get_trigger_list_variable_ui_text_over_length_handling_type("key", 1)
```

---

## get_trigger_list_actor_variable_ui_text_over_length_handling_type

method in GameAPI

- 描述

    获取触发器UI_TEXT_OVER_LENGTH_HANDLING_TYPE数组 组变量子项

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

local result = GameAPI.get_trigger_list_actor_variable_ui_text_over_length_handling_type(actor, "key", 1)
```

---

## get_trigger_list_variable_all_ui_text_over_length_handling_type

method in GameAPI

- 描述

    获取全局触发器UI_TEXT_OVER_LENGTH_HANDLING_TYPE数组变量

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
local result = GameAPI.get_trigger_list_variable_all_ui_text_over_length_handling_type("key")
```

---

## get_trigger_list_actor_variable_all_ui_text_over_length_handling_type

method in GameAPI

- 描述

    获取触发器UI_TEXT_OVER_LENGTH_HANDLING_TYPE 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_ui_text_over_length_handling_type(actor, "key")
```

---

## get_trigger_variable_ui_pos_adapt_mode

method in GameAPI

- 描述

    获取全局触发器UI_POS_ADAPT_MODE非数组变量

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
local result = GameAPI.get_trigger_variable_ui_pos_adapt_mode("key")
```

---

## get_trigger_actor_variable_ui_pos_adapt_mode

method in GameAPI

- 描述

    获取触发器UI_POS_ADAPT_MODE非数组 组变量

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

local result = GameAPI.get_trigger_actor_variable_ui_pos_adapt_mode(actor, "key")
```

---

## get_trigger_list_variable_ui_pos_adapt_mode

method in GameAPI

- 描述

    获取全局触发器UI_POS_ADAPT_MODE数组变量子项

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
local result = GameAPI.get_trigger_list_variable_ui_pos_adapt_mode("key", 1)
```

---

## get_trigger_list_actor_variable_ui_pos_adapt_mode

method in GameAPI

- 描述

    获取触发器UI_POS_ADAPT_MODE数组 组变量子项

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

local result = GameAPI.get_trigger_list_actor_variable_ui_pos_adapt_mode(actor, "key", 1)
```

---

## get_trigger_list_variable_all_ui_pos_adapt_mode

method in GameAPI

- 描述

    获取全局触发器UI_POS_ADAPT_MODE数组变量

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
local result = GameAPI.get_trigger_list_variable_all_ui_pos_adapt_mode("key")
```

---

## get_trigger_list_actor_variable_all_ui_pos_adapt_mode

method in GameAPI

- 描述

    获取触发器UI_POS_ADAPT_MODE 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_ui_pos_adapt_mode(actor, "key")
```

---

## get_trigger_variable_ui_chat_send_channel

method in GameAPI

- 描述

    获取全局触发器UI_CHAT_SEND_CHANNEL非数组变量

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
local result = GameAPI.get_trigger_variable_ui_chat_send_channel("key")
```

---

## get_trigger_actor_variable_ui_chat_send_channel

method in GameAPI

- 描述

    获取触发器UI_CHAT_SEND_CHANNEL非数组 组变量

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

local result = GameAPI.get_trigger_actor_variable_ui_chat_send_channel(actor, "key")
```

---

## get_trigger_list_variable_ui_chat_send_channel

method in GameAPI

- 描述

    获取全局触发器UI_CHAT_SEND_CHANNEL数组变量子项

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
local result = GameAPI.get_trigger_list_variable_ui_chat_send_channel("key", 1)
```

---

## get_trigger_list_actor_variable_ui_chat_send_channel

method in GameAPI

- 描述

    获取触发器UI_CHAT_SEND_CHANNEL数组 组变量子项

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

local result = GameAPI.get_trigger_list_actor_variable_ui_chat_send_channel(actor, "key", 1)
```

---

## get_trigger_list_variable_all_ui_chat_send_channel

method in GameAPI

- 描述

    获取全局触发器UI_CHAT_SEND_CHANNEL数组变量

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
local result = GameAPI.get_trigger_list_variable_all_ui_chat_send_channel("key")
```

---

## get_trigger_list_actor_variable_all_ui_chat_send_channel

method in GameAPI

- 描述

    获取触发器UI_CHAT_SEND_CHANNEL 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_ui_chat_send_channel(actor, "key")
```

---

## get_trigger_variable_ui_chat_recv_channel

method in GameAPI

- 描述

    获取全局触发器UI_CHAT_RECV_CHANNEL非数组变量

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
local result = GameAPI.get_trigger_variable_ui_chat_recv_channel("key")
```

---

## get_trigger_actor_variable_ui_chat_recv_channel

method in GameAPI

- 描述

    获取触发器UI_CHAT_RECV_CHANNEL非数组 组变量

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

local result = GameAPI.get_trigger_actor_variable_ui_chat_recv_channel(actor, "key")
```

---

## get_trigger_list_variable_ui_chat_recv_channel

method in GameAPI

- 描述

    获取全局触发器UI_CHAT_RECV_CHANNEL数组变量子项

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
local result = GameAPI.get_trigger_list_variable_ui_chat_recv_channel("key", 1)
```

---

## get_trigger_list_actor_variable_ui_chat_recv_channel

method in GameAPI

- 描述

    获取触发器UI_CHAT_RECV_CHANNEL数组 组变量子项

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

local result = GameAPI.get_trigger_list_actor_variable_ui_chat_recv_channel(actor, "key", 1)
```

---

## get_trigger_list_variable_all_ui_chat_recv_channel

method in GameAPI

- 描述

    获取全局触发器UI_CHAT_RECV_CHANNEL数组变量

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
local result = GameAPI.get_trigger_list_variable_all_ui_chat_recv_channel("key")
```

---

## get_trigger_list_actor_variable_all_ui_chat_recv_channel

method in GameAPI

- 描述

    获取触发器UI_CHAT_RECV_CHANNEL 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_ui_chat_recv_channel(actor, "key")
```

---

## get_trigger_variable_ui_anim_play_mode

method in GameAPI

- 描述

    获取全局触发器UI_ANIM_PLAY_MODE非数组变量

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
local result = GameAPI.get_trigger_variable_ui_anim_play_mode("key")
```

---

## get_trigger_actor_variable_ui_anim_play_mode

method in GameAPI

- 描述

    获取触发器UI_ANIM_PLAY_MODE非数组 组变量

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

local result = GameAPI.get_trigger_actor_variable_ui_anim_play_mode(actor, "key")
```

---

## get_trigger_list_variable_ui_anim_play_mode

method in GameAPI

- 描述

    获取全局触发器UI_ANIM_PLAY_MODE数组变量子项

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
local result = GameAPI.get_trigger_list_variable_ui_anim_play_mode("key", 1)
```

---

## get_trigger_list_actor_variable_ui_anim_play_mode

method in GameAPI

- 描述

    获取触发器UI_ANIM_PLAY_MODE数组 组变量子项

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

local result = GameAPI.get_trigger_list_actor_variable_ui_anim_play_mode(actor, "key", 1)
```

---

## get_trigger_list_variable_all_ui_anim_play_mode

method in GameAPI

- 描述

    获取全局触发器UI_ANIM_PLAY_MODE数组变量

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
local result = GameAPI.get_trigger_list_variable_all_ui_anim_play_mode("key")
```

---

## get_trigger_list_actor_variable_all_ui_anim_play_mode

method in GameAPI

- 描述

    获取触发器UI_ANIM_PLAY_MODE 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_ui_anim_play_mode(actor, "key")
```

---

## get_trigger_variable_ui_text_font_name

method in GameAPI

- 描述

    获取全局触发器UI_TEXT_FONT_NAME非数组变量

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
local result = GameAPI.get_trigger_variable_ui_text_font_name("key")
```

---

## get_trigger_actor_variable_ui_text_font_name

method in GameAPI

- 描述

    获取触发器UI_TEXT_FONT_NAME非数组 组变量

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

local result = GameAPI.get_trigger_actor_variable_ui_text_font_name(actor, "key")
```

---

## get_trigger_list_variable_ui_text_font_name

method in GameAPI

- 描述

    获取全局触发器UI_TEXT_FONT_NAME数组变量子项

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
local result = GameAPI.get_trigger_list_variable_ui_text_font_name("key", 1)
```

---

## get_trigger_list_actor_variable_ui_text_font_name

method in GameAPI

- 描述

    获取触发器UI_TEXT_FONT_NAME数组 组变量子项

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

local result = GameAPI.get_trigger_list_actor_variable_ui_text_font_name(actor, "key", 1)
```

---

## get_trigger_list_variable_all_ui_text_font_name

method in GameAPI

- 描述

    获取全局触发器UI_TEXT_FONT_NAME数组变量

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
local result = GameAPI.get_trigger_list_variable_all_ui_text_font_name("key")
```

---

## get_trigger_list_actor_variable_all_ui_text_font_name

method in GameAPI

- 描述

    获取触发器UI_TEXT_FONT_NAME 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_ui_text_font_name(actor, "key")
```

---

## get_trigger_variable_ui_eca_anim_type

method in GameAPI

- 描述

    获取全局触发器UI_ECA_ANIM_TYPE非数组变量

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
local result = GameAPI.get_trigger_variable_ui_eca_anim_type("key")
```

---

## get_trigger_actor_variable_ui_eca_anim_type

method in GameAPI

- 描述

    获取触发器UI_ECA_ANIM_TYPE非数组 组变量

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

local result = GameAPI.get_trigger_actor_variable_ui_eca_anim_type(actor, "key")
```

---

## get_trigger_list_variable_ui_eca_anim_type

method in GameAPI

- 描述

    获取全局触发器UI_ECA_ANIM_TYPE数组变量子项

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
local result = GameAPI.get_trigger_list_variable_ui_eca_anim_type("key", 1)
```

---

## get_trigger_list_actor_variable_ui_eca_anim_type

method in GameAPI

- 描述

    获取触发器UI_ECA_ANIM_TYPE数组 组变量子项

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

local result = GameAPI.get_trigger_list_actor_variable_ui_eca_anim_type(actor, "key", 1)
```

---

## get_trigger_list_variable_all_ui_eca_anim_type

method in GameAPI

- 描述

    获取全局触发器UI_ECA_ANIM_TYPE数组变量

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
local result = GameAPI.get_trigger_list_variable_all_ui_eca_anim_type("key")
```

---

## get_trigger_list_actor_variable_all_ui_eca_anim_type

method in GameAPI

- 描述

    获取触发器UI_ECA_ANIM_TYPE 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_ui_eca_anim_type(actor, "key")
```

---

## get_trigger_variable_local_unit_entity

method in GameAPI

- 描述

    获取全局触发器LOCAL_UNIT_ENTITY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LocalUnit | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_local_unit_entity("key")
```

---

## get_trigger_actor_variable_local_unit_entity

method in GameAPI

- 描述

    获取触发器LOCAL_UNIT_ENTITY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LocalUnit | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_local_unit_entity(actor, "key")
```

---

## get_trigger_list_variable_local_unit_entity

method in GameAPI

- 描述

    获取全局触发器LOCAL_UNIT_ENTITY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LocalUnit | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_local_unit_entity("key", 1)
```

---

## get_trigger_list_actor_variable_local_unit_entity

method in GameAPI

- 描述

    获取触发器LOCAL_UNIT_ENTITY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LocalUnit | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_local_unit_entity(actor, "key", 1)
```

---

## get_trigger_list_variable_all_local_unit_entity

method in GameAPI

- 描述

    获取全局触发器LOCAL_UNIT_ENTITY数组变量

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
local result = GameAPI.get_trigger_list_variable_all_local_unit_entity("key")
```

---

## get_trigger_list_actor_variable_all_local_unit_entity

method in GameAPI

- 描述

    获取触发器LOCAL_UNIT_ENTITY 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_local_unit_entity(actor, "key")
```

---

## get_trigger_variable_local_unit_group

method in GameAPI

- 描述

    获取全局触发器LOCAL_UNIT_GROUP非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LocalUnitGroup | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_local_unit_group("key")
```

---

## get_trigger_actor_variable_local_unit_group

method in GameAPI

- 描述

    获取触发器LOCAL_UNIT_GROUP非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LocalUnitGroup | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_local_unit_group(actor, "key")
```

---

## get_trigger_list_variable_local_unit_group

method in GameAPI

- 描述

    获取全局触发器LOCAL_UNIT_GROUP数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LocalUnitGroup | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_local_unit_group("key", 1)
```

---

## get_trigger_list_actor_variable_local_unit_group

method in GameAPI

- 描述

    获取触发器LOCAL_UNIT_GROUP数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LocalUnitGroup | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_local_unit_group(actor, "key", 1)
```

---

## get_trigger_list_variable_all_local_unit_group

method in GameAPI

- 描述

    获取全局触发器LOCAL_UNIT_GROUP数组变量

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
local result = GameAPI.get_trigger_list_variable_all_local_unit_group("key")
```

---

## get_trigger_list_actor_variable_all_local_unit_group

method in GameAPI

- 描述

    获取触发器LOCAL_UNIT_GROUP 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_local_unit_group(actor, "key")
```

---

## get_trigger_variable_deco_entity

method in GameAPI

- 描述

    获取全局触发器DECO_ENTITY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DecoID | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_deco_entity("key")
```

---

## get_trigger_actor_variable_deco_entity

method in GameAPI

- 描述

    获取触发器DECO_ENTITY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DecoID | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_deco_entity(actor, "key")
```

---

## get_trigger_list_variable_deco_entity

method in GameAPI

- 描述

    获取全局触发器DECO_ENTITY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DecoID | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_deco_entity("key", 1)
```

---

## get_trigger_list_actor_variable_deco_entity

method in GameAPI

- 描述

    获取触发器DECO_ENTITY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DecoID | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_deco_entity(actor, "key", 1)
```

---

## get_trigger_list_variable_all_deco_entity

method in GameAPI

- 描述

    获取全局触发器DECO_ENTITY数组变量

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
local result = GameAPI.get_trigger_list_variable_all_deco_entity("key")
```

---

## get_trigger_list_actor_variable_all_deco_entity

method in GameAPI

- 描述

    获取触发器DECO_ENTITY 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_deco_entity(actor, "key")
```

---

## get_trigger_variable_scene_preset

method in GameAPI

- 描述

    获取全局触发器SCENE_PRESET非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ScenePreset | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_scene_preset("key")
```

---

## get_trigger_actor_variable_scene_preset

method in GameAPI

- 描述

    获取触发器SCENE_PRESET非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ScenePreset | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_scene_preset(actor, "key")
```

---

## get_trigger_list_variable_scene_preset

method in GameAPI

- 描述

    获取全局触发器SCENE_PRESET数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ScenePreset | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_scene_preset("key", 1)
```

---

## get_trigger_list_actor_variable_scene_preset

method in GameAPI

- 描述

    获取触发器SCENE_PRESET数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ScenePreset | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_scene_preset(actor, "key", 1)
```

---

## get_trigger_list_variable_all_scene_preset

method in GameAPI

- 描述

    获取全局触发器SCENE_PRESET数组变量

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
local result = GameAPI.get_trigger_list_variable_all_scene_preset("key")
```

---

## get_trigger_list_actor_variable_all_scene_preset

method in GameAPI

- 描述

    获取触发器SCENE_PRESET 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_scene_preset(actor, "key")
```

---

## get_trigger_variable_item_stack_type

method in GameAPI

- 描述

    获取全局触发器ITEM_STACK_TYPE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemStackType | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_item_stack_type("key")
```

---

## get_trigger_actor_variable_item_stack_type

method in GameAPI

- 描述

    获取触发器ITEM_STACK_TYPE非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemStackType | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_item_stack_type(actor, "key")
```

---

## get_trigger_list_variable_item_stack_type

method in GameAPI

- 描述

    获取全局触发器ITEM_STACK_TYPE数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemStackType | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_item_stack_type("key", 1)
```

---

## get_trigger_list_actor_variable_item_stack_type

method in GameAPI

- 描述

    获取触发器ITEM_STACK_TYPE数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemStackType | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_item_stack_type(actor, "key", 1)
```

---

## get_trigger_list_variable_all_item_stack_type

method in GameAPI

- 描述

    获取全局触发器ITEM_STACK_TYPE数组变量

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
local result = GameAPI.get_trigger_list_variable_all_item_stack_type("key")
```

---

## get_trigger_list_actor_variable_all_item_stack_type

method in GameAPI

- 描述

    获取触发器ITEM_STACK_TYPE 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_item_stack_type(actor, "key")
```

---

## get_trigger_variable_ability_release_id

method in GameAPI

- 描述

    获取全局触发器ABILITY_RELEASE_ID非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityReleaseId | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_ability_release_id("key")
```

---

## get_trigger_actor_variable_ability_release_id

method in GameAPI

- 描述

    获取触发器ABILITY_RELEASE_ID非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityReleaseId | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_ability_release_id(actor, "key")
```

---

## get_trigger_list_variable_ability_release_id

method in GameAPI

- 描述

    获取全局触发器ABILITY_RELEASE_ID数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityReleaseId | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_ability_release_id("key", 1)
```

---

## get_trigger_list_actor_variable_ability_release_id

method in GameAPI

- 描述

    获取触发器ABILITY_RELEASE_ID数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityReleaseId | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_ability_release_id(actor, "key", 1)
```

---

## get_trigger_list_variable_all_ability_release_id

method in GameAPI

- 描述

    获取全局触发器ABILITY_RELEASE_ID数组变量

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
local result = GameAPI.get_trigger_list_variable_all_ability_release_id("key")
```

---

## get_trigger_list_actor_variable_all_ability_release_id

method in GameAPI

- 描述

    获取触发器ABILITY_RELEASE_ID 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_ability_release_id(actor, "key")
```

---

## get_trigger_variable_deco_name

method in GameAPI

- 描述

    获取全局触发器DECO_NAME非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DecoKey | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_deco_name("key")
```

---

## get_trigger_actor_variable_deco_name

method in GameAPI

- 描述

    获取触发器DECO_NAME非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DecoKey | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_deco_name(actor, "key")
```

---

## get_trigger_list_variable_deco_name

method in GameAPI

- 描述

    获取全局触发器DECO_NAME数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DecoKey | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_deco_name("key", 1)
```

---

## get_trigger_list_actor_variable_deco_name

method in GameAPI

- 描述

    获取触发器DECO_NAME数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DecoKey | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_deco_name(actor, "key", 1)
```

---

## get_trigger_list_variable_all_deco_name

method in GameAPI

- 描述

    获取全局触发器DECO_NAME数组变量

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
local result = GameAPI.get_trigger_list_variable_all_deco_name("key")
```

---

## get_trigger_list_actor_variable_all_deco_name

method in GameAPI

- 描述

    获取触发器DECO_NAME 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_deco_name(actor, "key")
```

---

## get_trigger_variable_ui_point

method in GameAPI

- 描述

    获取全局触发器UI_POINT非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FUIPoint | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_ui_point("key")
```

---

## get_trigger_actor_variable_ui_point

method in GameAPI

- 描述

    获取触发器UI_POINT非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FUIPoint | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_ui_point(actor, "key")
```

---

## get_trigger_list_variable_ui_point

method in GameAPI

- 描述

    获取全局触发器UI_POINT数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FUIPoint | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_ui_point("key", 1)
```

---

## get_trigger_list_actor_variable_ui_point

method in GameAPI

- 描述

    获取触发器UI_POINT数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FUIPoint | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_ui_point(actor, "key", 1)
```

---

## get_trigger_list_variable_all_ui_point

method in GameAPI

- 描述

    获取全局触发器UI_POINT数组变量

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
local result = GameAPI.get_trigger_list_variable_all_ui_point("key")
```

---

## get_trigger_list_actor_variable_all_ui_point

method in GameAPI

- 描述

    获取触发器UI_POINT 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_ui_point(actor, "key")
```

---

## get_trigger_variable_attach_model_entity

method in GameAPI

- 描述

    获取全局触发器ATTACH_MODEL_ENTITY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AttachModelEntity | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_attach_model_entity("key")
```

---

## get_trigger_actor_variable_attach_model_entity

method in GameAPI

- 描述

    获取触发器ATTACH_MODEL_ENTITY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AttachModelEntity | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_attach_model_entity(actor, "key")
```

---

## get_trigger_list_variable_attach_model_entity

method in GameAPI

- 描述

    获取全局触发器ATTACH_MODEL_ENTITY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AttachModelEntity | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_attach_model_entity("key", 1)
```

---

## get_trigger_list_actor_variable_attach_model_entity

method in GameAPI

- 描述

    获取触发器ATTACH_MODEL_ENTITY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AttachModelEntity | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_attach_model_entity(actor, "key", 1)
```

---

## get_trigger_list_variable_all_attach_model_entity

method in GameAPI

- 描述

    获取全局触发器ATTACH_MODEL_ENTITY数组变量

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
local result = GameAPI.get_trigger_list_variable_all_attach_model_entity("key")
```

---

## get_trigger_list_actor_variable_all_attach_model_entity

method in GameAPI

- 描述

    获取触发器ATTACH_MODEL_ENTITY 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_attach_model_entity(actor, "key")
```

---

## get_trigger_variable_live2d

method in GameAPI

- 描述

    获取全局触发器LIVE2D非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Live2dKey | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_live2d("key")
```

---

## get_trigger_actor_variable_live2d

method in GameAPI

- 描述

    获取触发器LIVE2D非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Live2dKey | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_live2d(actor, "key")
```

---

## get_trigger_list_variable_live2d

method in GameAPI

- 描述

    获取全局触发器LIVE2D数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Live2dKey | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_live2d("key", 1)
```

---

## get_trigger_list_actor_variable_live2d

method in GameAPI

- 描述

    获取触发器LIVE2D数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Live2dKey | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_live2d(actor, "key", 1)
```

---

## get_trigger_list_variable_all_live2d

method in GameAPI

- 描述

    获取全局触发器LIVE2D数组变量

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
local result = GameAPI.get_trigger_list_variable_all_live2d("key")
```

---

## get_trigger_list_actor_variable_all_live2d

method in GameAPI

- 描述

    获取触发器LIVE2D 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_live2d(actor, "key")
```

---

## get_trigger_variable_spine

method in GameAPI

- 描述

    获取全局触发器SPINE非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Spine | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_spine("key")
```

---

## get_trigger_actor_variable_spine

method in GameAPI

- 描述

    获取触发器SPINE非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Spine | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_spine(actor, "key")
```

---

## get_trigger_list_variable_spine

method in GameAPI

- 描述

    获取全局触发器SPINE数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Spine | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_spine("key", 1)
```

---

## get_trigger_list_actor_variable_spine

method in GameAPI

- 描述

    获取触发器SPINE数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Spine | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_spine(actor, "key", 1)
```

---

## get_trigger_list_variable_all_spine

method in GameAPI

- 描述

    获取全局触发器SPINE数组变量

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
local result = GameAPI.get_trigger_list_variable_all_spine("key")
```

---

## get_trigger_list_actor_variable_all_spine

method in GameAPI

- 描述

    获取触发器SPINE 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_spine(actor, "key")
```

---

## get_trigger_variable_debug_shape

method in GameAPI

- 描述

    获取全局触发器DEBUG_SHAPE非数组变量

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
local result = GameAPI.get_trigger_variable_debug_shape("key")
```

---

## get_trigger_actor_variable_debug_shape

method in GameAPI

- 描述

    获取触发器DEBUG_SHAPE非数组 组变量

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

local result = GameAPI.get_trigger_actor_variable_debug_shape(actor, "key")
```

---

## get_trigger_list_variable_debug_shape

method in GameAPI

- 描述

    获取全局触发器DEBUG_SHAPE数组变量子项

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
local result = GameAPI.get_trigger_list_variable_debug_shape("key", 1)
```

---

## get_trigger_list_actor_variable_debug_shape

method in GameAPI

- 描述

    获取触发器DEBUG_SHAPE数组 组变量子项

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

local result = GameAPI.get_trigger_list_actor_variable_debug_shape(actor, "key", 1)
```

---

## get_trigger_list_variable_all_debug_shape

method in GameAPI

- 描述

    获取全局触发器DEBUG_SHAPE数组变量

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
local result = GameAPI.get_trigger_list_variable_all_debug_shape("key")
```

---

## get_trigger_list_actor_variable_all_debug_shape

method in GameAPI

- 描述

    获取触发器DEBUG_SHAPE 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_debug_shape(actor, "key")
```

---

## get_trigger_variable_watching_mode_status

method in GameAPI

- 描述

    获取全局触发器WATCHING_MODE_STATUS非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.WatchingModeStatus | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_watching_mode_status("key")
```

---

## get_trigger_actor_variable_watching_mode_status

method in GameAPI

- 描述

    获取触发器WATCHING_MODE_STATUS非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.WatchingModeStatus | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_watching_mode_status(actor, "key")
```

---

## get_trigger_list_variable_watching_mode_status

method in GameAPI

- 描述

    获取全局触发器WATCHING_MODE_STATUS数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.WatchingModeStatus | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_watching_mode_status("key", 1)
```

---

## get_trigger_list_actor_variable_watching_mode_status

method in GameAPI

- 描述

    获取触发器WATCHING_MODE_STATUS数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.WatchingModeStatus | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_watching_mode_status(actor, "key", 1)
```

---

## get_trigger_list_variable_all_watching_mode_status

method in GameAPI

- 描述

    获取全局触发器WATCHING_MODE_STATUS数组变量

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
local result = GameAPI.get_trigger_list_variable_all_watching_mode_status("key")
```

---

## get_trigger_list_actor_variable_all_watching_mode_status

method in GameAPI

- 描述

    获取触发器WATCHING_MODE_STATUS 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_watching_mode_status(actor, "key")
```

---

## get_trigger_variable_force_entity

method in GameAPI

- 描述

    获取全局触发器FORCE_ENTITY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Force | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_force_entity("key")
```

---

## get_trigger_actor_variable_force_entity

method in GameAPI

- 描述

    获取触发器FORCE_ENTITY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Force | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_force_entity(actor, "key")
```

---

## get_trigger_list_variable_force_entity

method in GameAPI

- 描述

    获取全局触发器FORCE_ENTITY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Force | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_force_entity("key", 1)
```

---

## get_trigger_list_actor_variable_force_entity

method in GameAPI

- 描述

    获取触发器FORCE_ENTITY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Force | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_force_entity(actor, "key", 1)
```

---

## get_trigger_list_variable_all_force_entity

method in GameAPI

- 描述

    获取全局触发器FORCE_ENTITY数组变量

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
local result = GameAPI.get_trigger_list_variable_all_force_entity("key")
```

---

## get_trigger_list_actor_variable_all_force_entity

method in GameAPI

- 描述

    获取触发器FORCE_ENTITY 组变量数组

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

local result = GameAPI.get_trigger_list_actor_variable_all_force_entity(actor, "key")
```

---

## get_trigger_variable_goods_key

method in GameAPI

- 描述

    获取全局触发器GOODS_KEY非数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.GoodsKey | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_variable_goods_key("key")
```

---

## get_trigger_actor_variable_goods_key

method in GameAPI

- 描述

    获取触发器GOODS_KEY非数组 组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.GoodsKey | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_actor_variable_goods_key(actor, "key")
```

---

## get_trigger_list_variable_goods_key

method in GameAPI

- 描述

    获取全局触发器GOODS_KEY数组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.GoodsKey | 值 |

- 示例

```lua
local result = GameAPI.get_trigger_list_variable_goods_key("key", 1)
```

---

## get_trigger_list_actor_variable_goods_key

method in GameAPI

- 描述

    获取触发器GOODS_KEY数组 组变量子项

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | 单位实体 |
    | key | string | 变量名称 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.GoodsKey | 值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.get_trigger_list_actor_variable_goods_key(actor, "key", 1)
```

---

## get_trigger_list_variable_all_goods_key

method in GameAPI

- 描述

    获取全局触发器GOODS_KEY数组变量

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
local result = GameAPI.get_trigger_list_variable_all_goods_key("key")
```

---
