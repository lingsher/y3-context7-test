---
sidebarDepth: 1
---
# GameAPI (Part 7)

# 索引

Y3 编辑器 GameAPI 接口集合（第 7 部分），包含游戏核心功能。

---

| 接口 | 描述 |
| --- | --- |
| [clear_ui_comp_image](#clear_ui_comp_image) | 清空UI控件图片 |
| [set_ui_gridview_bar_enable](#set_ui_gridview_bar_enable) | 设置网格列表启用/禁止滚动条 |
| [set_ui_gridview_bar_percent](#set_ui_gridview_bar_percent) | 设置网格列表横向/纵向跳转百分比 |
| [set_ui_gridview_bar_thick](#set_ui_gridview_bar_thick) | 设置网格列表横向/纵向滚动条粗细 |
| [set_ui_gridview_bar_margin](#set_ui_gridview_bar_margin) | 设置网格列表横向/纵向滚动条边距 |
| [set_ui_gridview_bar_image](#set_ui_gridview_bar_image) | 设置网格列表横向/纵向滚动条图片 |
| [set_ui_gridview_bar_color](#set_ui_gridview_bar_color) | 设置网格列表横向/纵向滚动条图片颜色 |
| [set_ui_gridview_bar_color_norm](#set_ui_gridview_bar_color_norm) | 设置网格列表横向/纵向滚动条图片颜色 |
| [set_ui_gridview_bar_scale_9_enable](#set_ui_gridview_bar_scale_9_enable) | 设置网格列表横向/纵向滚动条九宫开关 |
| [set_ui_gridview_bar_cap_insets](#set_ui_gridview_bar_cap_insets) | 设置网格列表横向/纵向滚动条九宫值 |
| [set_ui_gridview_horizontal_reverse_enable](#set_ui_gridview_horizontal_reverse_enable) | 设置网格列表启用/禁止左右反向排布 |
| [set_ui_gridview_vertical_reverse_enable](#set_ui_gridview_vertical_reverse_enable) | 设置网格列表启用/禁止上下反向排布 |
| [set_ui_gridview_skip_invisible_enable](#set_ui_gridview_skip_invisible_enable) | 设置网格列表开启/禁用跳过隐藏控件 |
| [set_ui_gridview_bounce_enabled](#set_ui_gridview_bounce_enabled) | 设置网格列表启用/禁止下拉回弹 |
| [get_grid_view_percent](#get_grid_view_percent) | 【异步】获取本地玩家网格列表当前百分比位置 |
| [set_ui_comp_parent](#set_ui_comp_parent) | 设置界面控件的父控件 |
| [set_ui_scrollview_scroll](#set_ui_scrollview_scroll) | 设置列表启用/禁止滚动 |
| [play_ui_video](#play_ui_video) | 视频控件开始播放视频 |
| [play_ui_video_comp](#play_ui_video_comp) | 视频控件开始播放视频 |
| [stop_ui_video](#stop_ui_video) | 视频控件停止播放视频 |
| [set_ui_video_volume](#set_ui_video_volume) | 视频控件设置音量 |
| [set_ui_effect_id](#set_ui_effect_id) | UI播放特效 |
| [set_ui_effect_background_color](#set_ui_effect_background_color) | 设置特效控件的背景颜色 |
| [set_ui_effect_background_color_norm](#set_ui_effect_background_color_norm) | 设置特效控件的背景颜色 |
| [set_ui_effect_camera_fov](#set_ui_effect_camera_fov) | 设置特效控件的镜头视野 |
| [set_ui_effect_camera_pos](#set_ui_effect_camera_pos) | 设置特效控件的镜头坐标 |
| [set_ui_effect_camera_rotation](#set_ui_effect_camera_rotation) | 设置特效控件的镜头旋转 |
| [set_ui_effect_camera_mode](#set_ui_effect_camera_mode) | 设置模型控件的镜头模式 |
| [set_ui_effect_focus_pos](#set_ui_effect_focus_pos) | 设置特效控件的镜头焦点 |
| [set_ui_effect_play_speed](#set_ui_effect_play_speed) | 设置特效控件的播放速度 |
| [get_ui_comp_modifier](#get_ui_comp_modifier) | 【异步】获取魔法效果控件绑定的魔法效果 |
| [set_ui_text_font_name](#set_ui_text_font_name) | 设置文本字体 |
| [get_is_cursor_blocked_by_ui](#get_is_cursor_blocked_by_ui) | 获取鼠标是否悬浮在UI上 |
| [get_minimap_node_pos_from_world_pos](#get_minimap_node_pos_from_world_pos) | 世界坐标转小地图坐标 |
| [get_ui_point_x](#get_ui_point_x) | 获取ui坐标的x坐标 |
| [get_ui_point_y](#get_ui_point_y) | 获取ui坐标的y坐标 |
| [get_mini_map_node_pos_point_from_world_pos](#get_mini_map_node_pos_point_from_world_pos) | 世界坐标转小地图坐标 |
| [set_mini_map_follow_unit](#set_mini_map_follow_unit) | 设置小地图跟随单位 |
| [set_mini_map_move_enabled](#set_mini_map_move_enabled) | 设置小地图右键寻路可用性 |
| [api_enable_mini_map_alpha_click_range](#api_enable_mini_map_alpha_click_range) | 根据图片的透明区域设置小地图点击范围 |
| [api_disable_mini_map_alpha_click_range](#api_disable_mini_map_alpha_click_range) | 关闭根据图片的透明区域设置小地图点击范围 |
| [create_frame_sequence_on_mini_map](#create_frame_sequence_on_mini_map) | 在小地图上播放序列帧 |
| [create_sequence_on_unit_mini_map_icon](#create_sequence_on_unit_mini_map_icon) | 在单位的小地图头像上创建序列帧动画 |
| [set_unit_mini_map_sequence_icon](#set_unit_mini_map_sequence_icon) | 设置单位的序列帧类型的小地图头像 |
| [set_unit_enemy_mini_map_sequence_icon](#set_unit_enemy_mini_map_sequence_icon) | 设置单位的序列帧类型的敌方小地图头像 |
| [set_mini_map_icon_rotation](#set_mini_map_icon_rotation) | 设置小地图头像的旋转 |
| [set_ui_fog_table_size](#set_ui_fog_table_size) | 设置UI迷雾控件遮罩大小 |
| [set_ui_fog_by_table](#set_ui_fog_by_table) | 设置UI迷雾控件遮罩表格 |
| [set_ui_fog_vision_radius](#set_ui_fog_vision_radius) | 设置UI迷雾控件视野半径 |
| [set_ui_fog_blur_radius](#set_ui_fog_blur_radius) | 设置UI迷雾控件模糊度 |
| [get_local_player_language](#get_local_player_language) | 获取本地玩家语言 |
| [set_ui_model_sun_color](#set_ui_model_sun_color) | 设置UI模型控件光照颜色 |
| [set_ui_model_sun_direction](#set_ui_model_sun_direction) | 设置UI模型控件光照方向 |
| [api_get_joystick_move_state](#api_get_joystick_move_state) | 获取玩家摇杆的激活状态 |
| [api_get_joystick_move_direction](#api_get_joystick_move_direction) | 获取摇杆移动方向 |
| [api_get_joystick_move_percent](#api_get_joystick_move_percent) | 获取摇杆移动的力度 |
| [set_ui_world_chat_box_send_channel](#set_ui_world_chat_box_send_channel) | 设置UI世界聊天发送频道 |
| [set_ui_world_chat_box_recv_channel](#set_ui_world_chat_box_recv_channel) | 设置UI世界聊天接收频道 |
| [ban_ui_world_chat_box_send_channel](#ban_ui_world_chat_box_send_channel) | 屏蔽世界聊天发送频道 |
| [ban_ui_world_chat_box_recv_channel](#ban_ui_world_chat_box_recv_channel) | 屏蔽世界聊天接收频道 |
| [set_ui_image_size_adaptive](#set_ui_image_size_adaptive) | 设置图片保持原尺寸 |
| [set_ui_btn_status_cap_insets](#set_ui_btn_status_cap_insets) | 设置不同状态下的按钮九宫值 |
| [set_ui_text_gradient_color](#set_ui_text_gradient_color) | 设置文本渐变色 |
| [add_rich_text_text_to_chat_box](#add_rich_text_text_to_chat_box) | 添加富文本文字到输入框 |
| [add_rich_text_pic_to_chat_box](#add_rich_text_pic_to_chat_box) | 添加富文本图片到输入框 |
| [get_ui_resolution_x](#get_ui_resolution_x) | 获取UI横向分辨率 |
| [get_ui_resolution_y](#get_ui_resolution_y) | 获取UI纵向分辨率 |
| [set_ui_camera_binding](#set_ui_camera_binding) | 镜头控件-设置镜头控件绑定镜头 |
| [set_ui_camera_mask_texture](#set_ui_camera_mask_texture) | 镜头控件-设置遮罩贴图 |
| [copy_ui_text_to_clipboard](#copy_ui_text_to_clipboard) | 复制控件文本到剪贴板 |
| [set_clipping_node_stencil_texture](#set_clipping_node_stencil_texture) | 裁切节点-设置裁切节点的图片蒙版 |
| [set_clipping_node_inverted](#set_clipping_node_inverted) | 裁切节点-设置裁切节点开启反向裁切 |
| [create_layer](#create_layer) | 界面-创建画布 |
| [del_layer](#del_layer) | 界面-删除画布 |
| [set_ui_fog_pos_and_radius](#set_ui_fog_pos_and_radius) | 设置UI迷雾控件迷雾坐标和半径 |
| [set_ui_fog_clicked_comp_and_radius](#set_ui_fog_clicked_comp_and_radius) | 设置UI迷雾控件被点击的控件和半径 |
| [set_ui_text_strike_through](#set_ui_text_strike_through) | 设置文本删除线 |
| [set_ui_text_under_line](#set_ui_text_under_line) | 设置文本下划线 |
| [set_ui_text_italics](#set_ui_text_italics) | 设置文本斜体 |
| [set_scroll_view_scroll_by_touch_move_enabled](#set_scroll_view_scroll_by_touch_move_enabled) | 设置列表是否允许拖拽滚动 |
| [set_scroll_view_scroll_by_mouse_wheel_enabled](#set_scroll_view_scroll_by_mouse_wheel_enabled) | 设置列表是否允许鼠标滚轮滚动 |
| [api_get_attr_name](#api_get_attr_name) | 获取属性名 |
| [get_build_res_cost](#get_build_res_cost) | 获取建造消耗 |
| [set_build_res_cost](#set_build_res_cost) | 设置建造消耗 |
| [get_build_time](#get_build_time) | 获取建造时间 |
| [set_build_time](#set_build_time) | 设置建造时间 |
| [get_construction_progress](#get_construction_progress) | 获取建造进度 |
| [set_construction_progress](#set_construction_progress) | 设置建造进度 |
| [get_construction_factor](#get_construction_factor) | 获取建造速率 |
| [set_construction_factor](#set_construction_factor) | 设置建造速率 |
| [cancel_construction](#cancel_construction) | 取消单位建造 |
| [cancel_build_upgrade](#cancel_build_upgrade) | 取消建筑升级 |
| [start_build_upgrade](#start_build_upgrade) | 开始建筑升级 |
| [get_build_upgrade_list](#get_build_upgrade_list) | 获取建筑升级列表 |
| [set_build_upgrade_list](#set_build_upgrade_list) | 设置建筑升级列表 |
| [get_build_upgrade_progress](#get_build_upgrade_progress) | 获取建筑升级进度 |
| [set_build_upgrade_progress](#set_build_upgrade_progress) | 设置建筑升级进度 |
| [get_build_upgrade_factor](#get_build_upgrade_factor) | 获取建筑升级速率 |
| [set_build_upgrade_factor](#set_build_upgrade_factor) | 设置建筑升级速率 |
| [set_enable_war3_threat_group](#set_enable_war3_threat_group) | 开启WAR3仇恨系统：反击、救援行为过程中不再产生新的指令，其索敌通过扩展索敌范围实现 |
| [set_enable_war3_caution_force_return](#set_enable_war3_caution_force_return) | 开启WAR3中警戒强制返回特性：处于警戒状态下追逐敌人超过一定时间没有攻击到后强制移动回初始点（返回期间不攻击） |
| [set_enable_war3_ai_features](#set_enable_war3_ai_features) | 开启仿WAR3的AI特性，详见set_enable_war3_threat_group、set_enable_war3_caution_force_return |
| [set_cur_ai_target](#set_cur_ai_target) | 设置索敌目标。在【即将尝试索敌】或【发现目标】事件中修改索敌目标。在【即将尝试索敌】中指定目标可以跳过后续内置索敌从而节省一定性能，而在【发现目标】中修改索敌目标则不能 |
| [set_target_search_limit](#set_target_search_limit) | [性能]限制单次索敌遍历数量上限，对性能有提升。开启后索敌不再完整遍历检查警戒范围内的所有目标，而是在找到最多该数量个单位后直接退出遍历，以当前最优目标作为最终目标。可能导致索敌到的单位不是实际最优的（有其他单位距离更近、仇恨等级更高的没有被遍历到）。如果玩法对索敌准确性要求不高且性能压力较大，则建议开启。（多人游戏时需要保持同步） |
| [set_search_target_keep_frame](#set_search_target_keep_frame) | [性能]限制最小索敌间隔帧数，对性能有提升。开启后，单位的每两次完整索敌之间需要间隔一定时间，期间单位会尽可能保持上个目标（除非上个目标无效了）。可能导致单位索敌更新不及时，如果玩法对索敌准确性要求不高/微操比重不高且性能压力较大，则建议开启。（多人游戏时需要保持同步） |
| [set_enable_simple_attack_sensor](#set_enable_simple_attack_sensor) | [性能]简化警戒范围检测，对性能有提升。开启后会导致特定场景下索敌准确性降低（敌方单位之间移速差距较大且进出警戒范围频繁），大部分情况下副作用不明显，建议视情况开启。（多人游戏时需要保持同步） |
| [set_enable_new_sensor_rule](#set_enable_new_sensor_rule) | [性能]统一范围检测判定方式为碰撞半径检测，对性能有提升。由于历史原因，光环和商店的范围判定是不考虑单位自身碰撞半径的，而警戒和攻击范围的判定是考虑单位碰撞半径的，同时存在两套判定规则在一定程度上增加了性能消耗。开启此开关后会使上述的范围判定全都考虑自身碰撞半径，这样可以简化Y3内部的实现，使得游戏性能得到提升。出于兼容性考虑，此开关默认关闭。如果判断此改动无副作用的话，建议开启。（多人游戏时需要保持同步） |
| [set_enable_dynamic_sensor_tick_gap](#set_enable_dynamic_sensor_tick_gap) | [性能]启用动态范围检测刷新频率，对性能有提升。开启后游戏会动态根据当前场上单位数量等因素调整范围检测刷新频率，避免因为计算量过大/频率过高而导致游戏卡顿。副作用为单位的警戒响应、魔法效果光环进出判定的即时性会略微降低，但如果游戏性能问题相比起来更严重，则建议开启。（多人游戏时需要保持同步） |
| [set_alarm_range_limit](#set_alarm_range_limit) | [性能]一键设置警戒范围上限。警戒范围默认无上限，但是过大的警戒范围会增加性能消耗，尤其当这样的单位数量较多时，性能会以n^2的速度下降。这个接口可以用于一键设置警戒范围上限，游戏内的实际值会采用该值和物编配置中的较小值。一般来说警戒范围不宜超过5000。（多人游戏时需要保持同步） |
| [set_ai_tick_limit](#set_ai_tick_limit) | [性能]限制单位AI tick量。该数值用于在单位数量较多时限制每帧tick的单位数量，避免游戏卡顿。数值越低，允许每帧tick的单位数量越少，越利于减轻游戏卡顿，但是副作用是单位的响应灵敏性会降低/攻击间隔增大。默认初始值为6000，一般来说在单位量级小于1000时副作用体感不会很明显。如果游戏卡顿可以尝试调低该值。（多人游戏时需要保持同步） |
| [set_ai_ignore_threat_priority](#set_ai_ignore_threat_priority) | [性能]设置索敌时是否忽略威胁优先级。默认关闭，开启后索敌时的目标优先级排序将仅考虑距离，不再考虑目标的威胁程度。开启后对于警戒范围内有大量潜在目标时的索敌性能会有极大性能提升，如果地图玩法对于威胁优先级没有严格需求则建议开启 |
| [stop_unit_pick_item](#stop_unit_pick_item) | 阻止单位拾取物品 |
| [get_pick_item_slot](#get_pick_item_slot) | 返回拾取物品的目标栏位 |
| [api_get_abilityKey_by_unitkey](#api_get_abilityKey_by_unitkey) | 获取单位某个技能位的技能类型 |
| [set_enable_auto_lua_gc](#set_enable_auto_lua_gc) | [性能] 设置是否开启空闲时lua自动gc逻辑，默认关闭lua-gc，帧率空闲时进行LUA_GCSTEP; 设置为False后可以自行控制lua-gc |
| [get_unit_group_intersect](#get_unit_group_intersect) | 单位组取交集 |
| [get_unit_group_diff](#get_unit_group_diff) | 单位组取差集 |
| [api_get_ability_type_cast_type](#api_get_ability_type_cast_type) | 获取技能类型的释放技能 |
| [set_use_skill_dry_run_state](#set_use_skill_dry_run_state) | 设置单次建造的模拟状态 |
| [get_ability_type_by_int](#get_ability_type_by_int) | 整数转技能类型 |
| [get_ability_by_ability_global_id](#get_ability_by_ability_global_id) | 根据技能唯一ID获取技能实例 |
| [get_projectile_group_in_area](#get_projectile_group_in_area) | 得到区域内的投射物id列表 |
| [get_projectile_group_by_key](#get_projectile_group_by_key) | 得到投射物类型对应的投射物组 |
| [add_projectile_to_group](#add_projectile_to_group) | 添加投射物到投射物组 |
| [get_role_of_projectile](#get_role_of_projectile) | 获取投射物的所属玩家 |
| [change_projectile_owner_player](#change_projectile_owner_player) | 改变投射物所属玩家 |
| [create_projectile_group](#create_projectile_group) | 创建空投射物组 |
| [get_projectile_group_nums](#get_projectile_group_nums) | 获取投射物组数量 |
| [get_projectile_group_intersection](#get_projectile_group_intersection) | 投射物组取交集 |
| [get_projectile_group_diff](#get_projectile_group_diff) | 投射物组取差集 |
| [set_deco_visible](#set_deco_visible) | 设置装饰物显隐 |
| [set_deco_visible_new](#set_deco_visible_new) | 设置装饰物对玩家显隐 |
| [set_deco_texture](#set_deco_texture) | 装饰物替换模型贴图 |
| [create_deco](#create_deco) | 创建装饰物 |
| [delete_deco](#delete_deco) | 删除装饰物 |
| [set_mouse_follower](#set_mouse_follower) | 设置鼠标挂接物 |
| [cancel_mouse_follower](#cancel_mouse_follower) | 取消鼠标挂接物 |
| [set_mouse_follower_offset](#set_mouse_follower_offset) | 设置鼠标挂接物的偏移 |
| [set_mouse_follower_rotation](#set_mouse_follower_rotation) | 设置鼠标挂接物的旋转角度 |
| [set_mouse_follower_scale](#set_mouse_follower_scale) | 设置鼠标挂接物的缩放比列 |
| [set_mouse_follower_anim_speed](#set_mouse_follower_anim_speed) | 设置鼠标挂接物的动画速度 |
| [set_mouse_follower_model_anim](#set_mouse_follower_model_anim) | 设置鼠标挂接物模型播放动画 |
| [set_build_pointer_move_grids](#set_build_pointer_move_grids) | 设置建造指示器移动格子数 |
| [set_build_pointer_move_grids_offset](#set_build_pointer_move_grids_offset) | 设置建造指示器移动格子数偏移 |
| [is_in_watch_mode](#is_in_watch_mode) | 当前是否为观战模式 |
| [get_cur_watching_player](#get_cur_watching_player) | 获取当前被观战的玩家 |
| [get_watching_mode_status](#get_watching_mode_status) | 获取观战状态 |
| [set_watcher_simulate_player](#set_watcher_simulate_player) | 模拟指定玩家 |
| [enable_switch_watch_player_shortcut](#enable_switch_watch_player_shortcut) | 禁用/启用切换被观战玩家按键 |
| [api_get_select_unit_single](#api_get_select_unit_single) | 获取玩家选中的单个单位 |
| [api_get_select_unit_first](#api_get_select_unit_first) | 获取玩家选中的第一个单位 |
| [api_get_select_unit_group](#api_get_select_unit_group) | 获取玩家选中单位组(单位ID列表) |
| [is_command_queue_key_down](#is_command_queue_key_down) | 获取玩家是否按下命令队列按键 |
| [is_command_queue_enabled](#is_command_queue_enabled) | 获取命令队列功能是否开启 |
| [api_get_role_group_intersection](#api_get_role_group_intersection) | 玩家组取交集 |
| [api_get_role_group_diff](#api_get_role_group_diff) | 玩家组取差集 |
| [get_dungeon_info](#get_dungeon_info) | 查询副本信息 |
| [get_h_nearest_unit_with_quick_tag](#get_h_nearest_unit_with_quick_tag) | 距离最近的带标签单位 |
| [get_unit_ids_with_quick_tag](#get_unit_ids_with_quick_tag) | 获取带标签的单位id列表 |
| [get_external_info](#get_external_info) | 获取外部验证信息 |
| [init_external_http_config](#init_external_http_config) | 平台外部服务器设置接口 |
| [platform_http_login](#platform_http_login) | 平台外部连接登录 |
| [platform_http_request](#platform_http_request) | 平台外部http请求 |
| [get_random_archive_value](#get_random_archive_value) | 读取服务器随机数的值 |
| [get_random_archive_timestamp](#get_random_archive_timestamp) | 读取服务器随机数的时间戳 |
| [get_random_archive_group_id](#get_random_archive_group_id) | 读取服务器随机数的组id |
| [get_random_archive_daily_remain](#get_random_archive_daily_remain) | 获取指定只读随机存档的每日剩余次数 |
| [get_random_archive_game_remain](#get_random_archive_game_remain) | 获取指定只读随机存档的每局剩余次数 |
| [get_role_map_archive_limit](#get_role_map_archive_limit) | 获取存档剩余次数 |
| [api_get_ai_random_seed](#api_get_ai_random_seed) | 获取当前地图AI随机种子 |
| [api_set_preload_cam](#api_set_preload_cam) | 设置下个场景的初始化镜头 |
| [set_follow_placer_enable_inertia](#set_follow_placer_enable_inertia) | 设置镜头跟随单位缓动 |
| [camera_set_param_collide](#camera_set_param_collide) | 设置镜头碰撞参数 |
| [camera_set_param_collide_radius](#camera_set_param_collide_radius) | 设置镜头碰撞参数 |
| [set_tps_camera_pitch_max](#set_tps_camera_pitch_max) | 设置tps镜头pitch上限 |
| [set_tps_camera_pitch_min](#set_tps_camera_pitch_min) | 设置tps镜头pitch下限 |
| [set_tps_camera_fov](#set_tps_camera_fov) | 设置tps镜头fov |
| [set_camera_dof](#set_camera_dof) | 镜头景深功能 |
| [api_world_pos_to_camera_pos_2d](#api_world_pos_to_camera_pos_2d) | 世界坐标转换屏幕坐标 |
| [api_world_pos_to_screen_edge_pos_2d](#api_world_pos_to_screen_edge_pos_2d) | 世界坐标转换屏幕边缘坐标 |
| [get_local_player_camera_focus](#get_local_player_camera_focus) | 获取本地玩家镜头焦点 |
| [api_get_string_md5](#api_get_string_md5) | 获取字符串的md5值 |
| [generate_rsa_keys](#generate_rsa_keys) | 生成RSA密钥对 |
| [rsa_encrypt_message](#rsa_encrypt_message) | 使用公钥加密消息 |
| [rsa_decrypt_message](#rsa_decrypt_message) | 使用私钥解密消息 |
| [debug_draw_sphere](#debug_draw_sphere) | 调试-绘制球形 |
| [debug_draw_cylinder](#debug_draw_cylinder) | 调试-绘制圆柱 |
| [debug_draw_box](#debug_draw_box) | 调试-绘制立方体 |
| [debug_draw_polyline](#debug_draw_polyline) | 调试-绘制线段 |
| [delete_debug_draw](#delete_debug_draw) | 调试-删除绘制 |
| [debug_draw_filter_area_circular](#debug_draw_filter_area_circular) | 调试-绘制区域-圆形 |
| [debug_draw_filter_area_sector](#debug_draw_filter_area_sector) | 调试-绘制区域-扇形 |
| [debug_draw_filter_area_annular](#debug_draw_filter_area_annular) | 调试-绘制区域-环形 |
| [debug_draw_filter_area_rect](#debug_draw_filter_area_rect) | 调试-绘制区域-矩形 |
| [set_pb_isolated](#set_pb_isolated) | 设置pickbound是否受动态碰撞半径影响 |
| [open_ui_module_panel](#open_ui_module_panel) | 打开uimodule |
| [init_user_card_panel](#init_user_card_panel) | 初始化玩家图鉴 |
| [filter_user_card_panel](#filter_user_card_panel) | 初始化玩家图鉴 |
| [set_sfx_position_3d](#set_sfx_position_3d) | 设置特效到三维坐标 |
| [api_change_time_scale](#api_change_time_scale) | 修改游戏速度 |
| [api_enable_profile](#api_enable_profile) | 开关profile功能 |
| [create_unit_new](#create_unit_new) | 创建单位 |
| [create_local_unit](#create_local_unit) | 创建本地单位 |
| [create_illusion_new](#create_illusion_new) | 创建幻象 |
| [create_role_group](#create_role_group) | 新建空玩家组 |
| [get_local_unit_by_id](#get_local_unit_by_id) | 根据单位ID获取本地单位 |
| [get_deco_by_id](#get_deco_by_id) | 直接返回装饰物id |
| [create_character_top_light_to_unit_socket](#create_character_top_light_to_unit_socket) | 创建角色顶光到单位挂接点 |
| [get_first_unit_in_local_group](#get_first_unit_in_local_group) | 本地单位组内第一个单位 |
| [get_last_unit_in_local_group](#get_last_unit_in_local_group) | 本地单位组内最后一个单位 |
| [create_item_by_id_ex](#create_item_by_id_ex) | 创建单个物品 |
| [get_local_unit_group_num](#get_local_unit_group_num) | 本地单位组内单位数量 |
| [refresh_item_group](#refresh_item_group) | 遍历时过滤物品组 |
| [remove_unit_in_local_group](#remove_unit_in_local_group) | 删除本地单位组中某个单位 |
| [get_random_point_in_circular](#get_random_point_in_circular) | 返回圆形范围内随机点 |
| [get_all_items_in_shapes_new](#get_all_items_in_shapes_new) | 获取指定形状内的所有物品新 |
| [create_unit_group](#create_unit_group) | 新建空单位组 |
| [add_unit_to_local_group](#add_unit_to_local_group) | 添加单位到本地单位组 |
| [local_unit_group_is_exist](#local_unit_group_is_exist) | 本地单位组是否存在 |
| [trigger_is_exist](#trigger_is_exist) | 触发器是否存在 |
| [mover_is_exist](#mover_is_exist) | 运动器是否存在 |
| [common_is_exist](#common_is_exist) | 对象是否存在 |
| [create_harm_text_ex](#create_harm_text_ex) | 生成漂浮文字 |
| [set_scene_node_to_point](#set_scene_node_to_point) | 设置场景ui的位置到场景点 |
| [create_scene_node_on_unit_ex](#create_scene_node_on_unit_ex) | 创建场景点并绑定UI到单位 |
| [create_scene_node_on_unit_new](#create_scene_node_on_unit_new) | 创建场景点并绑定UI到单位 |
| [get_client_role_id](#get_client_role_id) | 获取本地玩家id |
| [is_returning_player](#is_returning_player) | 玩家是否回流 |
| [get_player_last_recommend_time](#get_player_last_recommend_time) | 获取玩家上次安利墙的时间 |
| [get_role_platform_url](#get_role_platform_url) | 获取玩家平台头像URL |
| [set_billboard_overall_visibility](#set_billboard_overall_visibility) | 设置血条整体可见性 |
| [reset_billboard_overall_visibility](#reset_billboard_overall_visibility) | 重置血条的整体可见性 |
| [set_billboard_picture_group](#set_billboard_picture_group) | 设置血条中进度条控件的进度条图片 |
| [open_platform_shop](#open_platform_shop) | 请求购买平台道具 |
| [api_compare_store_key](#api_compare_store_key) | 平台道具是否相等 |
| [save_anticheat_data](#save_anticheat_data) | 上传反作弊数值统计 |
| [get_plain_text_from_rich_text](#get_plain_text_from_rich_text) | 剔除字符串内富文本信息 |
| [api_is_point_in_shape](#api_is_point_in_shape) | 点是否在范围内 |
| [api_get_pseudo_random](#api_get_pseudo_random) | 保底伪随机数Roll点 |
| [api_broadcast_msg](#api_broadcast_msg) | 广播本地消息 |
| [refresh_get_effect_on_modifier](#refresh_get_effect_on_modifier) | 遍历魔法效果的得到特效 |
| [refresh_loss_effect_on_modifier](#refresh_loss_effect_on_modifier) | 遍历魔法效果的失去特效 |
| [get_effect_on_modifier](#get_effect_on_modifier) | 获得遍历到的特效 |
| [refresh_attach_model_on_modifier](#refresh_attach_model_on_modifier) | 遍历魔法效果的挂接模型 |
| [get_attach_model_on_modifier](#get_attach_model_on_modifier) | 获得遍历到的模型 |
| [slot_type_to_str](#slot_type_to_str) | 背包类型转字符串 |
| [attach_model_entity_to_str](#attach_model_entity_to_str) | 挂接模型实体转字符串 |
| [play_attach_model_animation](#play_attach_model_animation) | 播放动画 |
| [stop_attach_model_animation](#stop_attach_model_animation) | 停止播放动画 |
| [api_get_autorec_interval](#api_get_autorec_interval) | 获取属性自动恢复间隔 |
| [get_object_multilingual_key](#get_object_multilingual_key) | 获取物编名称/描述多语言key |
| [set_common_atk_quick_cast](#set_common_atk_quick_cast) | 设置快捷施法 |

---

## clear_ui_comp_image

method in GameAPI

- 描述

    清空UI控件图片

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

GameAPI.clear_ui_comp_image(player.handle, "comp_name")
```

---

## set_ui_gridview_bar_enable

method in GameAPI

- 描述

    设置网格列表启用/禁止滚动条

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

GameAPI.set_ui_gridview_bar_enable(player.handle, "comp_uid", true)
```

---

## set_ui_gridview_bar_percent

method in GameAPI

- 描述

    设置网格列表横向/纵向跳转百分比

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | direction | integer | 横向/纵向 |
    | ratio | number | 百分比 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_gridview_bar_percent(player.handle, "comp_uid", 1, 1.0)
```

---

## set_ui_gridview_bar_thick

method in GameAPI

- 描述

    设置网格列表横向/纵向滚动条粗细

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | direction | integer | 横向/纵向 |
    | thick | number | 粗细 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_gridview_bar_thick(player.handle, "comp_uid", 1, 1.0)
```

---

## set_ui_gridview_bar_margin

method in GameAPI

- 描述

    设置网格列表横向/纵向滚动条边距

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件名 |
    | direction | integer | 横向/纵向 |
    | top | number | 上 |
    | bottom | number | 下 |
    | left | number | 左 |
    | right | number | 右 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_gridview_bar_margin(player.handle, "comp_uid", 1, 1.0, 1.0, 1.0, 1.0)
```

---

## set_ui_gridview_bar_image

method in GameAPI

- 描述

    设置网格列表横向/纵向滚动条图片

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件名 |
    | direction | integer | 横向/纵向 |
    | image | integer | 图片 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_gridview_bar_image(player.handle, "comp_uid", 1, 1)
```

---

## set_ui_gridview_bar_color

method in GameAPI

- 描述

    设置网格列表横向/纵向滚动条图片颜色

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件名 |
    | direction | integer | 横向/纵向 |
    | r | number | R |
    | g | number | G |
    | b | number | B |
    | a | number | A |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_gridview_bar_color(player.handle, "comp_uid", 1, 1.0, 1.0, 1.0, 1.0)
```

---

## set_ui_gridview_bar_color_norm

method in GameAPI

- 描述

    设置网格列表横向/纵向滚动条图片颜色

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件名 |
    | direction | integer | 横向/纵向 |
    | r | number | R |
    | g | number | G |
    | b | number | B |
    | a | number | A |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_gridview_bar_color_norm(player.handle, "comp_uid", 1, 1.0, 1.0, 1.0, 1.0)
```

---

## set_ui_gridview_bar_scale_9_enable

method in GameAPI

- 描述

    设置网格列表横向/纵向滚动条九宫开关

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件名 |
    | direction | integer | 横向/纵向 |
    | enable | boolean | 是否启用 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_gridview_bar_scale_9_enable(player.handle, "comp_uid", 1, true)
```

---

## set_ui_gridview_bar_cap_insets

method in GameAPI

- 描述

    设置网格列表横向/纵向滚动条九宫值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件uid |
    | direction | integer | 横向/纵向 |
    | x_left | integer | x |
    | x_right | integer | y |
    | y_top | integer | width |
    | y_bottom | integer | height |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_gridview_bar_cap_insets(player.handle, "comp_name", 1, 1, 1, 1, 1)
```

---

## set_ui_gridview_horizontal_reverse_enable

method in GameAPI

- 描述

    设置网格列表启用/禁止左右反向排布

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件名 |
    | enable | boolean | 是否启用 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_gridview_horizontal_reverse_enable(player.handle, "comp_uid", true)
```

---

## set_ui_gridview_vertical_reverse_enable

method in GameAPI

- 描述

    设置网格列表启用/禁止上下反向排布

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件名 |
    | enable | boolean | 是否启用 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_gridview_vertical_reverse_enable(player.handle, "comp_uid", true)
```

---

## set_ui_gridview_skip_invisible_enable

method in GameAPI

- 描述

    设置网格列表开启/禁用跳过隐藏控件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件名 |
    | enable | boolean | 是否启用 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_gridview_skip_invisible_enable(player.handle, "comp_uid", true)
```

---

## set_ui_gridview_bounce_enabled

method in GameAPI

- 描述

    设置网格列表启用/禁止下拉回弹

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件名 |
    | enable | boolean | 是否启用 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_gridview_bounce_enabled(player.handle, "comp_uid", true)
```

---

## get_grid_view_percent

method in GameAPI

- 描述

    【异步】获取本地玩家网格列表当前百分比位置

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | comp_name | string | 控件uid |
    | direction | integer | 横向/纵向 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 百分比 |

- 示例

```lua
local result = GameAPI.get_grid_view_percent("comp_name", 1)
```

---

## set_ui_comp_parent

method in GameAPI

- 描述

    设置界面控件的父控件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | parent_uid | string | 父控件uid |
    | keep_pos? | boolean | 保持位置 |
    | keep_rotation? | boolean | 保持旋转 |
    | keep_scale? | boolean | 保持缩放 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_comp_parent(player.handle, "comp_uid", "parent_uid", true, true, true)
```

---

## set_ui_scrollview_scroll

method in GameAPI

- 描述

    设置列表启用/禁止滚动

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

GameAPI.set_ui_scrollview_scroll(player.handle, "comp_uid", true)
```

---

## play_ui_video

method in GameAPI

- 描述

    视频控件开始播放视频

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | url | string | url |
    | ease_in_time? | number | 淡入时长 |
    | ease_out_time? | number | 淡出时长 |
    | ease_type? | integer | 曲线类型 |
    | is_loop? | boolean | 循环播放 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.play_ui_video(player.handle, "url", 1.0, 1.0, 1, true)
```

---

## play_ui_video_comp

method in GameAPI

- 描述

    视频控件开始播放视频

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | url | string | url |
    | ease_in_time? | number | 淡入时长 |
    | ease_out_time? | number | 淡出时长 |
    | ease_type? | integer | 曲线类型 |
    | is_loop? | boolean | 循环播放 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.play_ui_video_comp(player.handle, "comp_uid", "url", 1.0, 1.0, 1, true)
```

---

## stop_ui_video

method in GameAPI

- 描述

    视频控件停止播放视频

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.stop_ui_video(player.handle)
```

---

## set_ui_video_volume

method in GameAPI

- 描述

    视频控件设置音量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | volume | number | 音量 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_video_volume(player.handle, 1.0)
```

---

## set_ui_effect_id

method in GameAPI

- 描述

    UI播放特效

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件uid |
    | effect_id | string | 特效id |
    | is_loop? | boolean | 是否循环 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_effect_id(player.handle, "comp_name", "effect_id", true)
```

---

## set_ui_effect_background_color

method in GameAPI

- 描述

    设置特效控件的背景颜色

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

GameAPI.set_ui_effect_background_color(player.handle, "comp_name", 1.0, 1.0, 1.0, 1.0)
```

---

## set_ui_effect_background_color_norm

method in GameAPI

- 描述

    设置特效控件的背景颜色

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

GameAPI.set_ui_effect_background_color_norm(player.handle, "comp_name", 1.0, 1.0, 1.0, 1.0)
```

---

## set_ui_effect_camera_fov

method in GameAPI

- 描述

    设置特效控件的镜头视野

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

GameAPI.set_ui_effect_camera_fov(player.handle, "comp_name", 1.0)
```

---

## set_ui_effect_camera_pos

method in GameAPI

- 描述

    设置特效控件的镜头坐标

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

GameAPI.set_ui_effect_camera_pos(player.handle, "comp_name", 1.0, 1.0, 1.0)
```

---

## set_ui_effect_camera_rotation

method in GameAPI

- 描述

    设置特效控件的镜头旋转

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

GameAPI.set_ui_effect_camera_rotation(player.handle, "comp_name", 1.0, 1.0, 1.0)
```

---

## set_ui_effect_camera_mode

method in GameAPI

- 描述

    设置模型控件的镜头模式

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件uid |
    | camera_mod | integer | 镜头模式 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_effect_camera_mode(player.handle, "comp_name", 1)
```

---

## set_ui_effect_focus_pos

method in GameAPI

- 描述

    设置特效控件的镜头焦点

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

GameAPI.set_ui_effect_focus_pos(player.handle, "comp_name", 1.0, 1.0, 1.0)
```

---

## set_ui_effect_play_speed

method in GameAPI

- 描述

    设置特效控件的播放速度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件uid |
    | play_speed | number | 播放速度 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_effect_play_speed(player.handle, "comp_name", 1.0)
```

---

## get_ui_comp_modifier

method in GameAPI

- 描述

    【异步】获取魔法效果控件绑定的魔法效果

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | comp_id | string | 控件uid |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierEntity | 魔法效果 |

- 示例

```lua
local result = GameAPI.get_ui_comp_modifier("comp_id")
```

---

## set_ui_text_font_name

method in GameAPI

- 描述

    设置文本字体

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件uid |
    | font_name | string | 字体 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_text_font_name(player.handle, "comp_name", "font_name")
```

---

## get_is_cursor_blocked_by_ui

method in GameAPI

- 描述

    获取鼠标是否悬浮在UI上

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.get_is_cursor_blocked_by_ui(player.handle)
```

---

## get_minimap_node_pos_from_world_pos

method in GameAPI

- 描述

    世界坐标转小地图坐标

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

GameAPI.get_minimap_node_pos_from_world_pos(player.handle, "comp_name", 1.0, 1.0)
```

---

## get_ui_point_x

method in GameAPI

- 描述

    获取ui坐标的x坐标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.FUIPoint | 坐标 |

- 返回值

    无

- 示例

```lua
local fui_point = GameAPI.get_unit_key_ui_point_kv(1, "key")

GameAPI.get_ui_point_x(fui_point)
```

---

## get_ui_point_y

method in GameAPI

- 描述

    获取ui坐标的y坐标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.FUIPoint | 坐标 |

- 返回值

    无

- 示例

```lua
local fui_point = GameAPI.get_unit_key_ui_point_kv(1, "key")

GameAPI.get_ui_point_y(fui_point)
```

---

## get_mini_map_node_pos_point_from_world_pos

method in GameAPI

- 描述

    世界坐标转小地图坐标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | pos | py.Point | point |
    | comp_name | string | 控件uid |

- 返回值

    无

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)

GameAPI.get_mini_map_node_pos_point_from_world_pos(point, "comp_name")
```

---

## set_mini_map_follow_unit

method in GameAPI

- 描述

    设置小地图跟随单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | player |
    | unit | py.Unit | 跟随单位 |
    | view_range | number | 视野范围 |
    | follow_range_limit_in_valid_area? | boolean | 是否将视野限制在合理地图范围内 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

GameAPI.set_mini_map_follow_unit(player.handle, unit.handle, 1.0, true)
```

---

## set_mini_map_move_enabled

method in GameAPI

- 描述

    设置小地图右键寻路可用性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | comp_name | string | 控件uid |
    | enabled | boolean | enabled |

- 返回值

    无

- 示例

```lua
GameAPI.set_mini_map_move_enabled("comp_name", true)
```

---

## api_enable_mini_map_alpha_click_range

method in GameAPI

- 描述

    根据图片的透明区域设置小地图点击范围

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件uid |
    | texture | py.Texture | 图片 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.api_enable_mini_map_alpha_click_range(player.handle, "comp_name", 1)
```

---

## api_disable_mini_map_alpha_click_range

method in GameAPI

- 描述

    关闭根据图片的透明区域设置小地图点击范围

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

GameAPI.api_disable_mini_map_alpha_click_range(player.handle, "comp_name")
```

---

## create_frame_sequence_on_mini_map

method in GameAPI

- 描述

    在小地图上播放序列帧

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | world_pos | py.Point | 世界坐标 |
    | sequence_resource | py.Sequence | 序列帧资源 |
    | source_player | py.Role | 发送信号的玩家 |
    | visible_type | py.SignalVisibleType | 可见类型 |
    | scale? | py.Fixed | 缩放 |
    | offset_percent_x? | py.Fixed | X方向偏移百分比 |
    | offset_percent_y? | py.Fixed | Y方向偏移百分比 |

- 返回值

    无

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)
local player = y3.player.get_by_id(1)

GameAPI.create_frame_sequence_on_mini_map(point, 1, player.handle, 1, Fix32(1), Fix32(1), Fix32(1))
```

---

## create_sequence_on_unit_mini_map_icon

method in GameAPI

- 描述

    在单位的小地图头像上创建序列帧动画

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | sequence_resource | py.Sequence | 序列帧资源 |
    | is_loop | boolean | 是否循环播放 |
    | duration | py.Fixed | 持续时间 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.create_sequence_on_unit_mini_map_icon(unit.handle, 1, true, Fix32(1))
```

---

## set_unit_mini_map_sequence_icon

method in GameAPI

- 描述

    设置单位的序列帧类型的小地图头像

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | sequence_resource | py.Sequence | 序列帧资源 |
    | is_loop | boolean | 是否循环播放 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.set_unit_mini_map_sequence_icon(unit.handle, 1, true)
```

---

## set_unit_enemy_mini_map_sequence_icon

method in GameAPI

- 描述

    设置单位的序列帧类型的敌方小地图头像

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | sequence_resource | py.Sequence | 序列帧资源 |
    | is_loop | boolean | 是否循环播放 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.set_unit_enemy_mini_map_sequence_icon(unit.handle, 1, true)
```

---

## set_mini_map_icon_rotation

method in GameAPI

- 描述

    设置小地图头像的旋转

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | py.Unit | 单位 |
    | rotation | py.Fixed | Rotation |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

GameAPI.set_mini_map_icon_rotation(player.handle, unit.handle, Fix32(1))
```

---

## set_ui_fog_table_size

method in GameAPI

- 描述

    设置UI迷雾控件遮罩大小

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | m | integer | M |
    | n | integer | N |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_fog_table_size(player.handle, "comp_uid", 1, 1)
```

---

## set_ui_fog_by_table

method in GameAPI

- 描述

    设置UI迷雾控件遮罩表格

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | table | py.Table | 遮罩表格 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local tbl = {}

GameAPI.set_ui_fog_by_table(player.handle, "comp_uid", tbl)
```

---

## set_ui_fog_vision_radius

method in GameAPI

- 描述

    设置UI迷雾控件视野半径

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | radius | integer | 视野半径 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_fog_vision_radius(player.handle, "comp_uid", 1)
```

---

## set_ui_fog_blur_radius

method in GameAPI

- 描述

    设置UI迷雾控件模糊度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | blur | integer | 模糊度 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_fog_blur_radius(player.handle, "comp_uid", 1)
```

---

## get_local_player_language

method in GameAPI

- 描述

    获取本地玩家语言

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | language |

- 示例

```lua
local result = GameAPI.get_local_player_language()
```

---

## set_ui_model_sun_color

method in GameAPI

- 描述

    设置UI模型控件光照颜色

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | py.Role | 玩家 |
    | comp_name | string | UI控件 |
    | r | number | R |
    | g | number | G |
    | b | number | B |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_model_sun_color(player.handle, "comp_name", 1.0, 1.0, 1.0)
```

---

## set_ui_model_sun_direction

method in GameAPI

- 描述

    设置UI模型控件光照方向

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | py.Role | 玩家 |
    | comp_name | string | UI控件 |
    | rotation | number | 纬度 |
    | longitude | number | 经度 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_model_sun_direction(player.handle, "comp_name", 1.0, 1.0)
```

---

## api_get_joystick_move_state

method in GameAPI

- 描述

    获取玩家摇杆的激活状态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | UI控件 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否激活 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.api_get_joystick_move_state(player.handle, "comp_name")
```

---

## api_get_joystick_move_direction

method in GameAPI

- 描述

    获取摇杆移动方向

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | UI控件 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | language |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.api_get_joystick_move_direction(player.handle, "comp_name")
```

---

## api_get_joystick_move_percent

method in GameAPI

- 描述

    获取摇杆移动的力度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | UI控件 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | language |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.api_get_joystick_move_percent(player.handle, "comp_name")
```

---

## set_ui_world_chat_box_send_channel

method in GameAPI

- 描述

    设置UI世界聊天发送频道

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | py.Role | 玩家 |
    | comp_name | string | UI控件 |
    | channel | integer | 频道 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_world_chat_box_send_channel(player.handle, "comp_name", 1)
```

---

## set_ui_world_chat_box_recv_channel

method in GameAPI

- 描述

    设置UI世界聊天接收频道

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | py.Role | 玩家 |
    | comp_name | string | UI控件 |
    | channel | integer | 频道 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_world_chat_box_recv_channel(player.handle, "comp_name", 1)
```

---

## ban_ui_world_chat_box_send_channel

method in GameAPI

- 描述

    屏蔽世界聊天发送频道

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | py.Role | 玩家 |
    | comp_name | string | UI控件 |
    | channel | integer | 频道 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.ban_ui_world_chat_box_send_channel(player.handle, "comp_name", 1)
```

---

## ban_ui_world_chat_box_recv_channel

method in GameAPI

- 描述

    屏蔽世界聊天接收频道

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | py.Role | 玩家 |
    | comp_name | string | UI控件 |
    | channel | integer | 频道 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.ban_ui_world_chat_box_recv_channel(player.handle, "comp_name", 1)
```

---

## set_ui_image_size_adaptive

method in GameAPI

- 描述

    设置图片保持原尺寸

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | size_adaptive | boolean | 保持原尺寸 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_image_size_adaptive(player.handle, "comp_uid", true)
```

---

## set_ui_btn_status_cap_insets

method in GameAPI

- 描述

    设置不同状态下的按钮九宫值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件uid |
    | btn_status | integer | 按钮状态 |
    | x_left | integer | x |
    | x_right | integer | y |
    | y_top | integer | width |
    | y_bottom | integer | height |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_btn_status_cap_insets(player.handle, "comp_name", 1, 1, 1, 1, 1)
```

---

## set_ui_text_gradient_color

method in GameAPI

- 描述

    设置文本渐变色

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件名 |
    | hex1? | string | hex |
    | a1? | number | A |
    | hex2? | string | hex |
    | a2? | number | A |
    | hex3? | string | hex |
    | a3? | number | A |
    | hex4? | string | hex |
    | a4? | number | A |
    | enable? | boolean | enable |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_text_gradient_color(player.handle, "comp_uid", "hex1", 1.0, "hex2", 1.0, "hex3", 1.0, "hex4", 1.0, true)
```

---

## add_rich_text_text_to_chat_box

method in GameAPI

- 描述

    添加富文本文字到输入框

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | text | string | 文字 |
    | color | string | 颜色 |
    | is_bold? | boolean | 是否加粗 |
    | is_underline? | boolean | 是否下划线 |
    | data? | string | 回调数据 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.add_rich_text_text_to_chat_box(player.handle, "comp_uid", "text", "color", true, true, "data")
```

---

## add_rich_text_pic_to_chat_box

method in GameAPI

- 描述

    添加富文本图片到输入框

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | image_id | py.Texture | 图片 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.add_rich_text_pic_to_chat_box(player.handle, "comp_uid", 1)
```

---

## get_ui_resolution_x

method in GameAPI

- 描述

    获取UI横向分辨率

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 分辨率 |

- 示例

```lua
local result = GameAPI.get_ui_resolution_x()
```

---

## get_ui_resolution_y

method in GameAPI

- 描述

    获取UI纵向分辨率

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 分辨率 |

- 示例

```lua
local result = GameAPI.get_ui_resolution_y()
```

---

## set_ui_camera_binding

method in GameAPI

- 描述

    镜头控件-设置镜头控件绑定镜头

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | camera_id | py.Camera | 镜头 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local camera = y3.camera.create_camera(y3.point(0, 0), 1000, 500, 0, 45, 3000)

GameAPI.set_ui_camera_binding(player.handle, "comp_uid", camera.handle)
```

---

## set_ui_camera_mask_texture

method in GameAPI

- 描述

    镜头控件-设置遮罩贴图

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | mask_texture | integer | 图片id |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_camera_mask_texture(player.handle, "comp_uid", 1)
```

---

## copy_ui_text_to_clipboard

method in GameAPI

- 描述

    复制控件文本到剪贴板

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | index1? | integer | 起始索引 |
    | index2? | integer | 结束索引 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.copy_ui_text_to_clipboard(player.handle, "comp_uid", 1, 1)
```

---

## set_clipping_node_stencil_texture

method in GameAPI

- 描述

    裁切节点-设置裁切节点的图片蒙版

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | stencil_texture | integer | 图片id |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_clipping_node_stencil_texture(player.handle, "comp_uid", 1)
```

---

## set_clipping_node_inverted

method in GameAPI

- 描述

    裁切节点-设置裁切节点开启反向裁切

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | is_inverted | boolean | 是否反向裁切 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_clipping_node_inverted(player.handle, "comp_uid", true)
```

---

## create_layer

method in GameAPI

- 描述

    界面-创建画布

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.create_layer(player.handle, "comp_uid")
```

---

## del_layer

method in GameAPI

- 描述

    界面-删除画布

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.del_layer(player.handle, "comp_uid")
```

---

## set_ui_fog_pos_and_radius

method in GameAPI

- 描述

    设置UI迷雾控件迷雾坐标和半径

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | pos_x | number | 坐标X |
    | pos_y | number | 坐标Y |
    | radius | integer | 视野半径 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_fog_pos_and_radius(player.handle, "comp_uid", 1.0, 1.0, 1)
```

---

## set_ui_fog_clicked_comp_and_radius

method in GameAPI

- 描述

    设置UI迷雾控件被点击的控件和半径

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | clicked_comp_uid | string | 被点击控件uid |
    | radius | integer | 视野半径 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_fog_clicked_comp_and_radius(player.handle, "comp_uid", "clicked_comp_uid", 1)
```

---

## set_ui_text_strike_through

method in GameAPI

- 描述

    设置文本删除线

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件uid |
    | enable | boolean | 开关 |
    | width? | integer | 粗细 |
    | color? | string | hex |
    | alpha? | number | A |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_text_strike_through(player.handle, "comp_name", true, 1, "color", 1.0)
```

---

## set_ui_text_under_line

method in GameAPI

- 描述

    设置文本下划线

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件uid |
    | enable | boolean | 开关 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_text_under_line(player.handle, "comp_name", true)
```

---

## set_ui_text_italics

method in GameAPI

- 描述

    设置文本斜体

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_name | string | 控件uid |
    | enable | boolean | 开关 |
    | radius? | number | 倾斜程度 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_ui_text_italics(player.handle, "comp_name", true, 1.0)
```

---

## set_scroll_view_scroll_by_touch_move_enabled

method in GameAPI

- 描述

    设置列表是否允许拖拽滚动

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | enable | boolean | 开关 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_scroll_view_scroll_by_touch_move_enabled(player.handle, "comp_uid", true)
```

---

## set_scroll_view_scroll_by_mouse_wheel_enabled

method in GameAPI

- 描述

    设置列表是否允许鼠标滚轮滚动

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | comp_uid | string | 控件uid |
    | enable | boolean | 开关 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_scroll_view_scroll_by_mouse_wheel_enabled(player.handle, "comp_uid", true)
```

---

## api_get_attr_name

method in GameAPI

- 描述

    获取属性名

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr_key | string | 属性key |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 属性名 |

- 示例

```lua
local result = GameAPI.api_get_attr_name("attr_key")
```

---

## get_build_res_cost

method in GameAPI

- 描述

    获取建造消耗

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | entity_no | py.UnitKey | 单位物编ID |
    | res_key | py.RoleResKey | 玩家属性 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 消耗数值 |

- 示例

```lua
local unit_key = 134274569
local role_res_key = "res_key"

local result = GameAPI.get_build_res_cost(unit_key, role_res_key)
```

---

## set_build_res_cost

method in GameAPI

- 描述

    设置建造消耗

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | entity_no | py.UnitKey | 单位物编ID |
    | res_key | py.RoleResKey | 玩家属性 |
    | val | py.Fixed | 消耗数值 |

- 返回值

    无

- 示例

```lua
local unit_key = 134274569
local role_res_key = "res_key"

GameAPI.set_build_res_cost(unit_key, role_res_key, Fix32(1))
```

---

## get_build_time

method in GameAPI

- 描述

    获取建造时间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | entity_no | py.UnitKey | 单位物编ID |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 建造时间 |

- 示例

```lua
local unit_key = 134274569

local result = GameAPI.get_build_time(unit_key)
```

---

## set_build_time

method in GameAPI

- 描述

    设置建造时间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | entity_no | py.UnitKey | 单位物编ID |
    | build_time | py.Fixed | 建造时间 |

- 返回值

    无

- 示例

```lua
local unit_key = 134274569

GameAPI.set_build_time(unit_key, Fix32(1))
```

---

## get_construction_progress

method in GameAPI

- 描述

    获取建造进度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 建造进度 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = GameAPI.get_construction_progress(unit.handle)
```

---

## set_construction_progress

method in GameAPI

- 描述

    设置建造进度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | progress | py.Fixed | 建造进度 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.set_construction_progress(unit.handle, Fix32(1))
```

---

## get_construction_factor

method in GameAPI

- 描述

    获取建造速率

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 建造速率 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = GameAPI.get_construction_factor(unit.handle)
```

---

## set_construction_factor

method in GameAPI

- 描述

    设置建造速率

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | factor | py.Fixed | 建造速率 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.set_construction_factor(unit.handle, Fix32(1))
```

---

## cancel_construction

method in GameAPI

- 描述

    取消单位建造

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | return_res? | boolean | 是否返还资源 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.cancel_construction(unit.handle, true)
```

---

## cancel_build_upgrade

method in GameAPI

- 描述

    取消建筑升级

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | return_res? | boolean | 是否返还资源 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.cancel_build_upgrade(unit.handle, true)
```

---

## start_build_upgrade

method in GameAPI

- 描述

    开始建筑升级

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | upgrade_entity_no | py.UnitKey | 目标单位物编ID |
    | keep_custom_kv_tag? | boolean | 是否保留自定义kv |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local unit_key = 134274569

GameAPI.start_build_upgrade(unit.handle, unit_key, true)
```

---

## get_build_upgrade_list

method in GameAPI

- 描述

    获取建筑升级列表

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Table | 可升级的单位编号一维表 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = GameAPI.get_build_upgrade_list(unit.handle)
```

---

## set_build_upgrade_list

method in GameAPI

- 描述

    设置建筑升级列表

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | lua_table | py.Table | 单位编号一维表 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local tbl = {}

GameAPI.set_build_upgrade_list(unit.handle, tbl)
```

---

## get_build_upgrade_progress

method in GameAPI

- 描述

    获取建筑升级进度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 进度 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = GameAPI.get_build_upgrade_progress(unit.handle)
```

---

## set_build_upgrade_progress

method in GameAPI

- 描述

    设置建筑升级进度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | progress | py.Fixed | 进度 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.set_build_upgrade_progress(unit.handle, Fix32(1))
```

---

## get_build_upgrade_factor

method in GameAPI

- 描述

    获取建筑升级速率

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 速率 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = GameAPI.get_build_upgrade_factor(unit.handle)
```

---

## set_build_upgrade_factor

method in GameAPI

- 描述

    设置建筑升级速率

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | factor | py.Fixed | 速率 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.set_build_upgrade_factor(unit.handle, Fix32(1))
```

---

## set_enable_war3_threat_group

method in GameAPI

- 描述

    开启WAR3仇恨系统：反击、救援行为过程中不再产生新的指令，其索敌通过扩展索敌范围实现

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | b | boolean | 开关 |

- 返回值

    无

- 示例

```lua
GameAPI.set_enable_war3_threat_group(true)
```

---

## set_enable_war3_caution_force_return

method in GameAPI

- 描述

    开启WAR3中警戒强制返回特性：处于警戒状态下追逐敌人超过一定时间没有攻击到后强制移动回初始点（返回期间不攻击）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | b | boolean | 开关 |

- 返回值

    无

- 示例

```lua
GameAPI.set_enable_war3_caution_force_return(true)
```

---

## set_enable_war3_ai_features

method in GameAPI

- 描述

    开启仿WAR3的AI特性，详见set_enable_war3_threat_group、set_enable_war3_caution_force_return

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | b | boolean | 开关 |

- 返回值

    无

- 示例

```lua
GameAPI.set_enable_war3_ai_features(true)
```

---

## set_cur_ai_target

method in GameAPI

- 描述

    设置索敌目标。在【即将尝试索敌】或【发现目标】事件中修改索敌目标。在【即将尝试索敌】中指定目标可以跳过后续内置索敌从而节省一定性能，而在【发现目标】中修改索敌目标则不能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | target | py.Unit | 目标 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

GameAPI.set_cur_ai_target(unit.handle)
```

---

## set_target_search_limit

method in GameAPI

- 描述

    [性能]限制单次索敌遍历数量上限，对性能有提升。开启后索敌不再完整遍历检查警戒范围内的所有目标，而是在找到最多该数量个单位后直接退出遍历，以当前最优目标作为最终目标。可能导致索敌到的单位不是实际最优的（有其他单位距离更近、仇恨等级更高的没有被遍历到）。如果玩法对索敌准确性要求不高且性能压力较大，则建议开启。（多人游戏时需要保持同步）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | limit | integer | 上限。小于等于0则不开启 |

- 返回值

    无

- 示例

```lua
GameAPI.set_target_search_limit(1)
```

---

## set_search_target_keep_frame

method in GameAPI

- 描述

    [性能]限制最小索敌间隔帧数，对性能有提升。开启后，单位的每两次完整索敌之间需要间隔一定时间，期间单位会尽可能保持上个目标（除非上个目标无效了）。可能导致单位索敌更新不及时，如果玩法对索敌准确性要求不高/微操比重不高且性能压力较大，则建议开启。（多人游戏时需要保持同步）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | interval | integer | 间隔帧数。小于等于0则不开启。（游戏默认30帧为1秒） |

- 返回值

    无

- 示例

```lua
GameAPI.set_search_target_keep_frame(1)
```

---

## set_enable_simple_attack_sensor

method in GameAPI

- 描述

    [性能]简化警戒范围检测，对性能有提升。开启后会导致特定场景下索敌准确性降低（敌方单位之间移速差距较大且进出警戒范围频繁），大部分情况下副作用不明显，建议视情况开启。（多人游戏时需要保持同步）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | enable | boolean | 是否开启 |

- 返回值

    无

- 示例

```lua
GameAPI.set_enable_simple_attack_sensor(true)
```

---

## set_enable_new_sensor_rule

method in GameAPI

- 描述

    [性能]统一范围检测判定方式为碰撞半径检测，对性能有提升。由于历史原因，光环和商店的范围判定是不考虑单位自身碰撞半径的，而警戒和攻击范围的判定是考虑单位碰撞半径的，同时存在两套判定规则在一定程度上增加了性能消耗。开启此开关后会使上述的范围判定全都考虑自身碰撞半径，这样可以简化Y3内部的实现，使得游戏性能得到提升。出于兼容性考虑，此开关默认关闭。如果判断此改动无副作用的话，建议开启。（多人游戏时需要保持同步）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | enable | boolean | 是否开启 |

- 返回值

    无

- 示例

```lua
GameAPI.set_enable_new_sensor_rule(true)
```

---

## set_enable_dynamic_sensor_tick_gap

method in GameAPI

- 描述

    [性能]启用动态范围检测刷新频率，对性能有提升。开启后游戏会动态根据当前场上单位数量等因素调整范围检测刷新频率，避免因为计算量过大/频率过高而导致游戏卡顿。副作用为单位的警戒响应、魔法效果光环进出判定的即时性会略微降低，但如果游戏性能问题相比起来更严重，则建议开启。（多人游戏时需要保持同步）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | enable | boolean | 是否开启 |

- 返回值

    无

- 示例

```lua
GameAPI.set_enable_dynamic_sensor_tick_gap(true)
```

---

## set_alarm_range_limit

method in GameAPI

- 描述

    [性能]一键设置警戒范围上限。警戒范围默认无上限，但是过大的警戒范围会增加性能消耗，尤其当这样的单位数量较多时，性能会以n^2的速度下降。这个接口可以用于一键设置警戒范围上限，游戏内的实际值会采用该值和物编配置中的较小值。一般来说警戒范围不宜超过5000。（多人游戏时需要保持同步）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | limit | py.Fixed | 值(厘米) |

- 返回值

    无

- 示例

```lua
GameAPI.set_alarm_range_limit(Fix32(1))
```

---

## set_ai_tick_limit

method in GameAPI

- 描述

    [性能]限制单位AI tick量。该数值用于在单位数量较多时限制每帧tick的单位数量，避免游戏卡顿。数值越低，允许每帧tick的单位数量越少，越利于减轻游戏卡顿，但是副作用是单位的响应灵敏性会降低/攻击间隔增大。默认初始值为6000，一般来说在单位量级小于1000时副作用体感不会很明显。如果游戏卡顿可以尝试调低该值。（多人游戏时需要保持同步）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | limit | integer | 值（初始默认值为6000） |

- 返回值

    无

- 示例

```lua
GameAPI.set_ai_tick_limit(1)
```

---

## set_ai_ignore_threat_priority

method in GameAPI

- 描述

    [性能]设置索敌时是否忽略威胁优先级。默认关闭，开启后索敌时的目标优先级排序将仅考虑距离，不再考虑目标的威胁程度。开启后对于警戒范围内有大量潜在目标时的索敌性能会有极大性能提升，如果地图玩法对于威胁优先级没有严格需求则建议开启

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | enable | boolean | 是否开启 |

- 返回值

    无

- 示例

```lua
GameAPI.set_ai_ignore_threat_priority(true)
```

---

## stop_unit_pick_item

method in GameAPI

- 描述

    阻止单位拾取物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_id | py.UnitID | UnitID |
    | slot_type | py.SlotType | SlotType |

- 返回值

    无

- 示例

```lua
local unit_id = 134274569
local slot_type = y3.const.SlotType.BAR

GameAPI.stop_unit_pick_item(unit_id, slot_type)
```

---

## get_pick_item_slot

method in GameAPI

- 描述

    返回拾取物品的目标栏位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_id | py.ItemID | ItemID |
    | slot_type | py.SlotType | SlotType |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SlotType | 目标栏位 |

- 示例

```lua
local item_id = 134274569
local slot_type = y3.const.SlotType.BAR

local result = GameAPI.get_pick_item_slot(item_id, slot_type)
```

---

## api_get_abilityKey_by_unitkey

method in GameAPI

- 描述

    获取单位某个技能位的技能类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位类型 |
    | abilityType | py.AbilityType | 技能类型 |
    | abilityIndex | py.AbilityIndex | 技能槽位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityKey | 技能类型 |

- 示例

```lua
local unit_key = 134274569
local ability_type = y3.const.AbilityType.HERO
local ability_index = 0

local result = GameAPI.api_get_abilityKey_by_unitkey(unit_key, ability_type, ability_index)
```

---

## set_enable_auto_lua_gc

method in GameAPI

- 描述

    [性能] 设置是否开启空闲时lua自动gc逻辑，默认关闭lua-gc，帧率空闲时进行LUA_GCSTEP; 设置为False后可以自行控制lua-gc

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | enable | boolean | 是否开启 |

- 返回值

    无

- 示例

```lua
GameAPI.set_enable_auto_lua_gc(true)
```

---

## get_unit_group_intersect

method in GameAPI

- 描述

    单位组取交集

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_group1 | py.UnitGroup | 单位组1 |
    | unit_group2 | py.UnitGroup | 单位组2 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitGroup | 单位组 |

- 示例

```lua
local unit_group = y3.unit_group.create()

local result = GameAPI.get_unit_group_intersect(unit_group.handle, unit_group.handle)
```

---

## get_unit_group_diff

method in GameAPI

- 描述

    单位组取差集

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_group1 | py.UnitGroup | 单位组1 |
    | unit_group2 | py.UnitGroup | 单位组2 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitGroup | 单位组 |

- 示例

```lua
local unit_group = y3.unit_group.create()

local result = GameAPI.get_unit_group_diff(unit_group.handle, unit_group.handle)
```

---

## api_get_ability_type_cast_type

method in GameAPI

- 描述

    获取技能类型的释放技能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能物编 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityCastType | 技能释放类型 |

- 示例

```lua
local ability_key = 134274569

local result = GameAPI.api_get_ability_type_cast_type(ability_key)
```

---

## set_use_skill_dry_run_state

method in GameAPI

- 描述

    设置单次建造的模拟状态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | idx | py.AbilityReleaseId | 整数索引值 |
    | is_dry_run | boolean | 是否仅模拟 |

- 返回值

    无

- 示例

```lua
GameAPI.set_use_skill_dry_run_state(1, true)
```

---

## get_ability_type_by_int

method in GameAPI

- 描述

    整数转技能类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | num | integer | 整数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityKey | 技能物编 |

- 示例

```lua
local result = GameAPI.get_ability_type_by_int(1)
```

---

## get_ability_by_ability_global_id

method in GameAPI

- 描述

    根据技能唯一ID获取技能实例

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_global_id | integer | ID |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Ability | 技能 |

- 示例

```lua
local result = GameAPI.get_ability_by_ability_global_id(1)
```

---

## get_projectile_group_in_area

method in GameAPI

- 描述

    得到区域内的投射物id列表

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.Area | 区域对象 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileGroup | 物品组 |

- 示例

```lua
local area = y3.area.create_circle_area(y3.point.create(0, 0, 0), 500)

local result = GameAPI.get_projectile_group_in_area(area.handle)
```

---

## get_projectile_group_by_key

method in GameAPI

- 描述

    得到投射物类型对应的投射物组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | py.ProjectileKey | 投射物类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileGroup | 物品组 |

- 示例

```lua
local projectile_key = 134274569

local result = GameAPI.get_projectile_group_by_key(projectile_key)
```

---

## add_projectile_to_group

method in GameAPI

- 描述

    添加投射物到投射物组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | Projectile | py.ProjectileEntity | 投射物 |
    | Projectile_group | py.ProjectileGroup | 投射物组 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local target_point = unit:get_point()
local projectile = y3.projectile.create({ key = 134274569, target = target_point })
local projectile_group = y3.projectile_group.create_lua_projectile_group_from_py(GameAPI.create_projectile_group())

GameAPI.add_projectile_to_group(projectile.handle, projectile_group.handle)
```

---

## get_role_of_projectile

method in GameAPI

- 描述

    获取投射物的所属玩家

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | project | py.ProjectileEntity | 投射物 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Role | 玩家 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local target_point = unit:get_point()
local projectile = y3.projectile.create({ key = 134274569, target = target_point })

local result = GameAPI.get_role_of_projectile(projectile.handle)
```

---

## change_projectile_owner_player

method in GameAPI

- 描述

    改变投射物所属玩家

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile | py.ProjectileEntity | 投射物 |
    | player | py.Actor | 玩家 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local target_point = unit:get_point()
local projectile = y3.projectile.create({ key = 134274569, target = target_point })

GameAPI.change_projectile_owner_player(projectile.handle, actor)
```

---

## create_projectile_group

method in GameAPI

- 描述

    创建空投射物组

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileGroup | 投射物组 |

- 示例

```lua
local result = GameAPI.create_projectile_group()
```

---

## get_projectile_group_nums

method in GameAPI

- 描述

    获取投射物组数量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile_group | py.ProjectileGroup | 投射物组 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 数量 |

- 示例

```lua
local projectile_group = y3.projectile_group.create_lua_projectile_group_from_py(GameAPI.create_projectile_group())

local result = GameAPI.get_projectile_group_nums(projectile_group.handle)
```

---

## get_projectile_group_intersection

method in GameAPI

- 描述

    投射物组取交集

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | group1 | py.ProjectileGroup | 投射物组1 |
    | group2 | py.ProjectileGroup | 投射物组2 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileGroup | 投射物组 |

- 示例

```lua
local projectile_group = y3.projectile_group.create_lua_projectile_group_from_py(GameAPI.create_projectile_group())

local result = GameAPI.get_projectile_group_intersection(projectile_group.handle, projectile_group.handle)
```

---

## get_projectile_group_diff

method in GameAPI

- 描述

    投射物组取差集

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | group1 | py.ProjectileGroup | 投射物组1 |
    | group2 | py.ProjectileGroup | 投射物组2 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileGroup | 投射物组 |

- 示例

```lua
local projectile_group = y3.projectile_group.create_lua_projectile_group_from_py(GameAPI.create_projectile_group())

local result = GameAPI.get_projectile_group_diff(projectile_group.handle, projectile_group.handle)
```

---

## set_deco_visible

method in GameAPI

- 描述

    设置装饰物显隐

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | deco_id | py.DecoID | 装饰物ID |
    | visible | boolean | 是否显隐 |

- 返回值

    无

- 示例

```lua
GameAPI.set_deco_visible(1, true)
```

---

## set_deco_visible_new

method in GameAPI

- 描述

    设置装饰物对玩家显隐

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | deco_id | py.DecoID | 装饰物ID |
    | player | py.Role | 玩家 |
    | visible | boolean | 是否显隐 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_deco_visible_new(1, player.handle, true)
```

---

## set_deco_texture

method in GameAPI

- 描述

    装饰物替换模型贴图

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | deco_id | py.DecoID | 装饰物ID |
    | material_id | integer | 材质 id |
    | layer_id | integer | layer id |
    | texture | py.Texture | 贴图 |

- 返回值

    无

- 示例

```lua
GameAPI.set_deco_texture(1, 1, 1, 1)
```

---

## create_deco

method in GameAPI

- 描述

    创建装饰物

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.FVector3 | 位置 |
    | deco_type | py.DecoKey | 装饰物类型 |
    | angle | py.Fixed | 角度 |
    | height_offset? | py.Fixed | 高度 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DecoID | 创建出的装饰物id |

- 示例

```lua
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

local result = GameAPI.create_deco(fvector3, 1, Fix32(1), Fix32(1))
```

---

## delete_deco

method in GameAPI

- 描述

    删除装饰物

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | deco_id | py.DecoID | 装饰物id |

- 返回值

    无

- 示例

```lua
GameAPI.delete_deco(1)
```

---

## set_mouse_follower

method in GameAPI

- 描述

    设置鼠标挂接物

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | _type | integer | 类型 |
    | entity_no | integer | 模型/特效id |
    | role | py.Role | 玩家 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_mouse_follower(1, 1, player.handle)
```

---

## cancel_mouse_follower

method in GameAPI

- 描述

    取消鼠标挂接物

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.cancel_mouse_follower(player.handle)
```

---

## set_mouse_follower_offset

method in GameAPI

- 描述

    设置鼠标挂接物的偏移

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | offset_x | number | 偏移X |
    | offset_y | number | 偏移Y |
    | offset_z | number | 偏移Z |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_mouse_follower_offset(player.handle, 1.0, 1.0, 1.0)
```

---

## set_mouse_follower_rotation

method in GameAPI

- 描述

    设置鼠标挂接物的旋转角度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | rotation_x | number | X |
    | rotation_y | number | Y |
    | rotation_z | number | Z |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_mouse_follower_rotation(player.handle, 1.0, 1.0, 1.0)
```

---

## set_mouse_follower_scale

method in GameAPI

- 描述

    设置鼠标挂接物的缩放比列

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | scale_x | number | X |
    | scale_y | number | Y |
    | scale_z | number | Z |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_mouse_follower_scale(player.handle, 1.0, 1.0, 1.0)
```

---

## set_mouse_follower_anim_speed

method in GameAPI

- 描述

    设置鼠标挂接物的动画速度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | anim_speed | number | 速度 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_mouse_follower_anim_speed(player.handle, 1.0)
```

---

## set_mouse_follower_model_anim

method in GameAPI

- 描述

    设置鼠标挂接物模型播放动画

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | anim_name | string | 动画名 |
    | anim_speed? | number | 动画速率 |
    | start_time? | number | 开始时间 |
    | end_time? | number | 结束时间 |
    | is_loop? | boolean | 是否循环播放 |
    | is_back_to_default? | boolean | 是否回到默认动画 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_mouse_follower_model_anim(player.handle, "anim_name", 1.0, 1.0, 1.0, true, true)
```

---

## set_build_pointer_move_grids

method in GameAPI

- 描述

    设置建造指示器移动格子数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | x | py.RoleID | 玩家ID |
    | y | py.UnitGroup | 单位组 |

- 返回值

    无

- 示例

```lua
local role_id = 1
local unit_group = y3.unit_group.create()

GameAPI.set_build_pointer_move_grids(role_id, unit_group.handle)
```

---

## set_build_pointer_move_grids_offset

method in GameAPI

- 描述

    设置建造指示器移动格子数偏移

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | x | integer | X偏移 |
    | y | integer | Y偏移 |

- 返回值

    无

- 示例

```lua
GameAPI.set_build_pointer_move_grids_offset(1, 1)
```

---

## is_in_watch_mode

method in GameAPI

- 描述

    当前是否为观战模式

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否为观战模式 |

- 示例

```lua
local result = GameAPI.is_in_watch_mode()
```

---

## get_cur_watching_player

method in GameAPI

- 描述

    获取当前被观战的玩家

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleID | 被观战玩家 |

- 示例

```lua
local result = GameAPI.get_cur_watching_player()
```

---

## get_watching_mode_status

method in GameAPI

- 描述

    获取观战状态

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.WatchingModeStatus | 观战模式状态 |

- 示例

```lua
local result = GameAPI.get_watching_mode_status()
```

---

## set_watcher_simulate_player

method in GameAPI

- 描述

    模拟指定玩家

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 模拟的玩家 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_watcher_simulate_player(player.handle)
```

---

## enable_switch_watch_player_shortcut

method in GameAPI

- 描述

    禁用/启用切换被观战玩家按键

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | enable | boolean | 是否可以切换被观战玩家 |

- 返回值

    无

- 示例

```lua
GameAPI.enable_switch_watch_player_shortcut(true)
```

---

## api_get_select_unit_single

method in GameAPI

- 描述

    获取玩家选中的单个单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role_id | py.RoleID | 玩家ID |

- 返回值

    无

- 示例

```lua
local role_id = 1

GameAPI.api_get_select_unit_single(role_id)
```

---

## api_get_select_unit_first

method in GameAPI

- 描述

    获取玩家选中的第一个单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role_id | py.RoleID | 玩家ID |

- 返回值

    无

- 示例

```lua
local role_id = 1

GameAPI.api_get_select_unit_first(role_id)
```

---

## api_get_select_unit_group

method in GameAPI

- 描述

    获取玩家选中单位组(单位ID列表)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role_id | py.RoleID | 玩家ID |

- 返回值

    无

- 示例

```lua
local role_id = 1

GameAPI.api_get_select_unit_group(role_id)
```

---

## is_command_queue_key_down

method in GameAPI

- 描述

    获取玩家是否按下命令队列按键

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.RoleID | 玩家ID |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否按下 |

- 示例

```lua
local role_id = 1

local result = GameAPI.is_command_queue_key_down(role_id)
```

---

## is_command_queue_enabled

method in GameAPI

- 描述

    获取命令队列功能是否开启

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否开启 |

- 示例

```lua
local result = GameAPI.is_command_queue_enabled()
```

---

## api_get_role_group_intersection

method in GameAPI

- 描述

    玩家组取交集

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | group1 | py.RoleGroup | 玩家组1 |
    | group2 | py.RoleGroup | 玩家组2 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleGroup | 玩家组 |

- 示例

```lua
local player_group = y3.player_group.create()

local result = GameAPI.api_get_role_group_intersection(player_group.handle, player_group.handle)
```

---

## api_get_role_group_diff

method in GameAPI

- 描述

    玩家组取差集

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | group1 | py.RoleGroup | 玩家组1 |
    | group2 | py.RoleGroup | 玩家组2 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleGroup | 玩家组 |

- 示例

```lua
local player_group = y3.player_group.create()

local result = GameAPI.api_get_role_group_diff(player_group.handle, player_group.handle)
```

---

## get_dungeon_info

method in GameAPI

- 描述

    查询副本信息

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Table | 副本信息 |

- 示例

```lua
local result = GameAPI.get_dungeon_info()
```

---

## get_h_nearest_unit_with_quick_tag

method in GameAPI

- 描述

    距离最近的带标签单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | position | py.Point | 位置 |
    | tag_idx | integer | 标签ID |
    | check_alive | boolean | 检查存活 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitID | 单位ID |

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)

local result = GameAPI.get_h_nearest_unit_with_quick_tag(point, 1, true)
```

---

## get_unit_ids_with_quick_tag

method in GameAPI

- 描述

    获取带标签的单位id列表

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag_idx | integer | 标签ID |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitGroup | 单位组 |

- 示例

```lua
local result = GameAPI.get_unit_ids_with_quick_tag(1)
```

---

## get_external_info

method in GameAPI

- 描述

    获取外部验证信息

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Table | 外部验证信息 |

- 示例

```lua
local result = GameAPI.get_external_info()
```

---

## init_external_http_config

method in GameAPI

- 描述

    平台外部服务器设置接口

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | aes_key | string | AESKey |
    | public_key | string | PublicKey |
    | external_url | string | ExternalUrl |

- 返回值

    无

- 示例

```lua
GameAPI.init_external_http_config("aes_key", "public_key", "external_url")
```

---

## platform_http_login

method in GameAPI

- 描述

    平台外部连接登录

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | api_path | string | 外部API路径 |
    | external_data | string | 自定义数据 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 调用结果 |

- 示例

```lua
local result = GameAPI.platform_http_login("api_path", "external_data")
```

---

## platform_http_request

method in GameAPI

- 描述

    平台外部http请求

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | api | string | 外部API路径 |
    | is_post | boolean | 是否是post请求 |
    | data | string | body数据 |
    | disable_in_connect? | boolean | 是否禁用在connect中 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 调用结果 |

- 示例

```lua
local result = GameAPI.platform_http_request("api", true, "data", true)
```

---

## get_random_archive_value

method in GameAPI

- 描述

    读取服务器随机数的值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | archive_id | string | 随机存档id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 随机数的值 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_random_archive_value(player.handle, "archive_id")
```

---

## get_random_archive_timestamp

method in GameAPI

- 描述

    读取服务器随机数的时间戳

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | archive_id | string | 随机存档id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 时间戳 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_random_archive_timestamp(player.handle, "archive_id")
```

---

## get_random_archive_group_id

method in GameAPI

- 描述

    读取服务器随机数的组id

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | archive_id | string | 随机存档id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 组id |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_random_archive_group_id(player.handle, "archive_id")
```

---

## get_random_archive_daily_remain

method in GameAPI

- 描述

    获取指定只读随机存档的每日剩余次数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | group_id | integer | 组id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 剩余次数 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_random_archive_daily_remain(player.handle, 1)
```

---

## get_random_archive_game_remain

method in GameAPI

- 描述

    获取指定只读随机存档的每局剩余次数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | group_id | integer | 组id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 剩余次数 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_random_archive_game_remain(player.handle, 1)
```

---

## get_role_map_archive_limit

method in GameAPI

- 描述

    获取存档剩余次数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | archive_key | integer | 整数存档 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 存档剩余值 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_role_map_archive_limit(player.handle, 1)
```

---

## api_get_ai_random_seed

method in GameAPI

- 描述

    获取当前地图AI随机种子

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 随机种子 |

- 示例

```lua
local result = GameAPI.api_get_ai_random_seed()
```

---

## api_set_preload_cam

method in GameAPI

- 描述

    设置下个场景的初始化镜头

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | camera | py.Camera | 镜头配置 |

- 返回值

    无

- 示例

```lua
local camera = y3.camera.create_camera(y3.point(0, 0), 1000, 500, 0, 45, 3000)

GameAPI.api_set_preload_cam(camera.handle)
```

---

## set_follow_placer_enable_inertia

method in GameAPI

- 描述

    设置镜头跟随单位缓动

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | enable | boolean | 缓动开关 |
    | inertia_coeff? | py.Fixed | 缓动速率 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_follow_placer_enable_inertia(player.handle, true, Fix32(1))
```

---

## camera_set_param_collide

method in GameAPI

- 描述

    设置镜头碰撞参数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | enable_collider | boolean | 碰撞开关 |
    | MinDist | number | 最小焦距 |
    | SmoothRatio? | number | 过度速率 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.camera_set_param_collide(player.handle, true, 1.0, 1.0)
```

---

## camera_set_param_collide_radius

method in GameAPI

- 描述

    设置镜头碰撞参数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | radius | number | 最小焦距 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.camera_set_param_collide_radius(player.handle, 1.0)
```

---

## set_tps_camera_pitch_max

method in GameAPI

- 描述

    设置tps镜头pitch上限

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | pitch | number | tps pitch上限 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_tps_camera_pitch_max(player.handle, 1.0)
```

---

## set_tps_camera_pitch_min

method in GameAPI

- 描述

    设置tps镜头pitch下限

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | pitch | number | tps pitch下限 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_tps_camera_pitch_min(player.handle, 1.0)
```

---

## set_tps_camera_fov

method in GameAPI

- 描述

    设置tps镜头fov

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | fov | number | tps fov |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_tps_camera_fov(player.handle, 1.0)
```

---

## set_camera_dof

method in GameAPI

- 描述

    镜头景深功能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | enable | boolean | 景深开关 |
    | dist | number | 景深开始距离 |
    | region | number | 景深大小 |
    | near_trans_region | number | 近处过渡距离 |
    | far_trans_region | number | 远处过渡距离 |

- 返回值

    无

- 示例

```lua
GameAPI.set_camera_dof(true, 1.0, 1.0, 1.0, 1.0)
```

---

## api_world_pos_to_camera_pos_2d

method in GameAPI

- 描述

    世界坐标转换屏幕坐标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | world_pos | py.Point | 世界坐标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Point | 屏幕坐标 |

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)

local result = GameAPI.api_world_pos_to_camera_pos_2d(point)
```

---

## api_world_pos_to_screen_edge_pos_2d

method in GameAPI

- 描述

    世界坐标转换屏幕边缘坐标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | world_pos | py.Point | 世界坐标 |
    | delta_dis | py.Fixed | 定点数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Point | 屏幕坐标 |

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)

local result = GameAPI.api_world_pos_to_screen_edge_pos_2d(point, Fix32(1))
```

---

## get_local_player_camera_focus

method in GameAPI

- 描述

    获取本地玩家镜头焦点

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3 | 镜头焦点 |

- 示例

```lua
local result = GameAPI.get_local_player_camera_focus()
```

---

## api_get_string_md5

method in GameAPI

- 描述

    获取字符串的md5值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | original_str | string | 原始字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | md5值 |

- 示例

```lua
local result = GameAPI.api_get_string_md5("original_str")
```

---

## generate_rsa_keys

method in GameAPI

- 描述

    生成RSA密钥对

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 公钥和私钥 |

- 示例

```lua
local result = GameAPI.generate_rsa_keys()
```

---

## rsa_encrypt_message

method in GameAPI

- 描述

    使用公钥加密消息

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | public_key | string | 公钥 |
    | message | string | 原始消息 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 加密后的消息 |

- 示例

```lua
local result = GameAPI.rsa_encrypt_message("public_key", "message")
```

---

## rsa_decrypt_message

method in GameAPI

- 描述

    使用私钥解密消息

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | private_key | string | 私钥 |
    | encrypted_message | string | 加密后的消息 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 解密后的消息 |

- 示例

```lua
local result = GameAPI.rsa_decrypt_message("private_key", "encrypted_message")
```

---

## debug_draw_sphere

method in GameAPI

- 描述

    调试-绘制球形

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | x | py.Fixed | x坐标 |
    | y | py.Fixed | y坐标 |
    | z | py.Fixed | z坐标 |
    | radius | py.Fixed | 半径 |
    | duration? | py.Fixed | 持续时间 |
    | color? | string | 绘制颜色 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 绘制id |

- 示例

```lua
local result = GameAPI.debug_draw_sphere(Fix32(1), Fix32(1), Fix32(1), Fix32(1), Fix32(1), "color")
```

---

## debug_draw_cylinder

method in GameAPI

- 描述

    调试-绘制圆柱

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.Point | 底部中心点 |
    | radius | py.Fixed | 半径 |
    | height | py.Fixed | 高度 |
    | duration? | py.Fixed | 持续时间 |
    | color? | string | 绘制颜色 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 绘制id |

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)

local result = GameAPI.debug_draw_cylinder(point, Fix32(1), Fix32(1), Fix32(1), "color")
```

---

## debug_draw_box

method in GameAPI

- 描述

    调试-绘制立方体

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | rect | py.RecArea | 矩形区域 |
    | height | py.Fixed | 高度 |
    | duration? | py.Fixed | 持续时间 |
    | color? | string | 绘制颜色 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 绘制id |

- 示例

```lua
local rec_area = GameAPI.create_rec_area_from_two_points(Fix32Vec3(0, 0, 0), Fix32Vec3(100, 100, 0))

local result = GameAPI.debug_draw_box(rec_area, Fix32(1), Fix32(1), "color")
```

---

## debug_draw_polyline

method in GameAPI

- 描述

    调试-绘制线段

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point1_x | py.Fixed | x1坐标 |
    | point1_y | py.Fixed | y1坐标 |
    | point1_z | py.Fixed | z1坐标 |
    | point2_x | py.Fixed | x2坐标 |
    | point2_y | py.Fixed | y2坐标 |
    | point2_z | py.Fixed | z2坐标 |
    | duration? | py.Fixed | 持续时间 |
    | color? | string | 绘制颜色 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 绘制id |

- 示例

```lua
local result = GameAPI.debug_draw_polyline(Fix32(1), Fix32(1), Fix32(1), Fix32(1), Fix32(1), Fix32(1), Fix32(1), "color")
```

---

## delete_debug_draw

method in GameAPI

- 描述

    调试-删除绘制

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | shape_id | integer | 绘制id |

- 返回值

    无

- 示例

```lua
GameAPI.delete_debug_draw(1)
```

---

## debug_draw_filter_area_circular

method in GameAPI

- 描述

    调试-绘制区域-圆形

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | pos | py.Vector3 | 坐标 |
    | shape | py.Shape | 圆形 |
    | duration? | py.Fixed | 持续时间 |
    | color? | string | 绘制颜色 |
    | attach_unit? | py.Unit | 挂接单位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 绘制id |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local vector3 = Fix32Vec3(0, 0, 0)
local shape = GlobalAPI.create_circular_shape(Fix32(500))

local result = GameAPI.debug_draw_filter_area_circular(vector3, shape, Fix32(1), "color")
```

---

## debug_draw_filter_area_sector

method in GameAPI

- 描述

    调试-绘制区域-扇形

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | pos | py.Vector3 | 坐标 |
    | shape | py.Shape | 扇形 |
    | duration? | py.Fixed | 持续时间 |
    | color? | string | 绘制颜色 |
    | attach_unit? | py.Unit | 挂接单位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 绘制id |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local vector3 = Fix32Vec3(0, 0, 0)
local shape = GlobalAPI.create_circular_shape(Fix32(500))

local result = GameAPI.debug_draw_filter_area_sector(vector3, shape, Fix32(1), "color")
```

---

## debug_draw_filter_area_annular

method in GameAPI

- 描述

    调试-绘制区域-环形

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | pos | py.Vector3 | 坐标 |
    | shape | py.Shape | 环形 |
    | duration? | py.Fixed | 持续时间 |
    | color? | string | 绘制颜色 |
    | attach_unit? | py.Unit | 挂接单位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 绘制id |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local vector3 = Fix32Vec3(0, 0, 0)
local shape = GlobalAPI.create_circular_shape(Fix32(500))

local result = GameAPI.debug_draw_filter_area_annular(vector3, shape, Fix32(1), "color")
```

---

## debug_draw_filter_area_rect

method in GameAPI

- 描述

    调试-绘制区域-矩形

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | pos | py.Vector3 | 坐标 |
    | shape | py.Shape | 矩形 |
    | duration? | py.Fixed | 持续时间 |
    | color? | string | 绘制颜色 |
    | attach_unit? | py.Unit | 挂接单位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 绘制id |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local vector3 = Fix32Vec3(0, 0, 0)
local shape = GlobalAPI.create_circular_shape(Fix32(500))

local result = GameAPI.debug_draw_filter_area_rect(vector3, shape, Fix32(1), "color")
```

---

## set_pb_isolated

method in GameAPI

- 描述

    设置pickbound是否受动态碰撞半径影响

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | isolated | boolean | 布尔 |

- 返回值

    无

- 示例

```lua
GameAPI.set_pb_isolated(true)
```

---

## open_ui_module_panel

method in GameAPI

- 描述

    打开uimodule

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | model_id | integer | modelid |

- 返回值

    无

- 示例

```lua
GameAPI.open_ui_module_panel(1)
```

---

## init_user_card_panel

method in GameAPI

- 描述

    初始化玩家图鉴

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | table | py.Table | 图鉴表 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local tbl = {}

GameAPI.init_user_card_panel(player.handle, tbl)
```

---

## filter_user_card_panel

method in GameAPI

- 描述

    初始化玩家图鉴

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | filter_type | string | 類型 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.filter_user_card_panel(player.handle, "filter_type")
```

---

## set_sfx_position_3d

method in GameAPI

- 描述

    设置特效到三维坐标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | sfx_entity | py.Sfx | 特效 |
    | point | py.FVector3 | 位置 |
    | fluent_move? | boolean | 平滑移动 |

- 返回值

    无

- 示例

```lua
local sfx = y3.particle.create({ type = 134274569, target = y3.point(0, 0) }).handle
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

GameAPI.set_sfx_position_3d(sfx, fvector3, true)
```

---

## api_change_time_scale

method in GameAPI

- 描述

    修改游戏速度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | time_scale | py.Fixed | name |

- 返回值

    无

- 示例

```lua
GameAPI.api_change_time_scale(Fix32(1))
```

---

## api_enable_profile

method in GameAPI

- 描述

    开关profile功能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | enable | boolean | enable |

- 返回值

    无

- 示例

```lua
GameAPI.api_enable_profile(true)
```

---

## create_unit_new

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

local result = GameAPI.create_unit_new(unit_key, fvector3, Fix32(1), player.handle)
```

---

## create_local_unit

method in GameAPI

- 描述

    创建本地单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | py.UnitKey | 单位编号 |
    | pos | py.FVector3 | 位置 |
    | face | py.Fixed | 朝向 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LocalUnit | 创建出的单位 |

- 示例

```lua
local unit_key = 134274569
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

local result = GameAPI.create_local_unit(unit_key, fvector3, Fix32(1))
```

---

## create_illusion_new

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
    | clone_items? | boolean | 是否继承物品 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

GameAPI.create_illusion_new(unit.handle, unit.handle, player.handle, fvector3, Fix32(1), true, true)
```

---

## create_role_group

method in GameAPI

- 描述

    新建空玩家组

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleGroup | 玩家组 |

- 示例

```lua
local result = GameAPI.create_role_group()
```

---

## get_local_unit_by_id

method in GameAPI

- 描述

    根据单位ID获取本地单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_id | py.LocalUnitID | 单位id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LocalUnit | 本地单位 |

- 示例

```lua
local result = GameAPI.get_local_unit_by_id(1)
```

---

## get_deco_by_id

method in GameAPI

- 描述

    直接返回装饰物id

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | deco_id | py.DecoID | 装饰物id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DecoID | 装饰物id |

- 示例

```lua
local result = GameAPI.get_deco_by_id(1)
```

---

## create_character_top_light_to_unit_socket

method in GameAPI

- 描述

    创建角色顶光到单位挂接点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | socket_name | string | 挂节点 |
    | pos_offset_y? | py.Fixed | 起点偏移高度 |
    | target? | py.Actor | 朝向目标 |
    | target_offset_y? | py.Fixed | 朝向目标偏移高度 |
    | need_shadow? | boolean | 是否产生阴影 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SpotLight | 方向光源 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GameAPI.create_character_top_light_to_unit_socket(unit.handle, "socket_name", Fix32(1), nil, Fix32(1), true)
```

---

## get_first_unit_in_local_group

method in GameAPI

- 描述

    本地单位组内第一个单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | units | py.LocalUnitGroup | 单位组 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LocalUnit | 第一个单位 |

- 示例

```lua
local local_unit_group = GameAPI.get_unit_key_local_unit_group_kv(1, "key")

local result = GameAPI.get_first_unit_in_local_group(local_unit_group)
```

---

## get_last_unit_in_local_group

method in GameAPI

- 描述

    本地单位组内最后一个单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | units | py.LocalUnitGroup | 单位组 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LocalUnit | 最后一个单位 |

- 示例

```lua
local local_unit_group = GameAPI.get_unit_key_local_unit_group_kv(1, "key")

local result = GameAPI.get_last_unit_in_local_group(local_unit_group)
```

---

## create_item_by_id_ex

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

local result = GameAPI.create_item_by_id_ex(fvector3, item_key, player.handle)
```

---

## get_local_unit_group_num

method in GameAPI

- 描述

    本地单位组内单位数量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_group | py.LocalUnitGroup | 单位组 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 单位数量 |

- 示例

```lua
local local_unit_group = GameAPI.get_unit_key_local_unit_group_kv(1, "key")

local result = GameAPI.get_local_unit_group_num(local_unit_group)
```

---

## refresh_item_group

method in GameAPI

- 描述

    遍历时过滤物品组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_group | py.ItemGroup | 物品组 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemGroup | 物品组 |

- 示例

```lua
local item_group = y3.item_group.create()

local result = GameAPI.refresh_item_group(item_group.handle)
```

---

## remove_unit_in_local_group

method in GameAPI

- 描述

    删除本地单位组中某个单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_group | py.LocalUnitGroup | 单位组 |
    | unit | py.LocalUnit | 单位 |

- 返回值

    无

- 示例

```lua
local local_unit_group = GameAPI.get_unit_key_local_unit_group_kv(1, "key")
local local_unit = GameAPI.create_local_unit(134274569, GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0)), Fix32(1))

GameAPI.remove_unit_in_local_group(local_unit_group, local_unit)
```

---

## get_random_point_in_circular

method in GameAPI

- 描述

    返回圆形范围内随机点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.FVector3 | 圆心 |
    | radius | py.Fixed | 半径 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3 | 随机点 |

- 示例

```lua
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

local result = GameAPI.get_random_point_in_circular(fvector3, Fix32(1))
```

---

## get_all_items_in_shapes_new

method in GameAPI

- 描述

    获取指定形状内的所有物品新

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

local result = GameAPI.get_all_items_in_shapes_new(point, shape, 1)
```

---

## create_unit_group

method in GameAPI

- 描述

    新建空单位组

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitGroup | 单位组 |

- 示例

```lua
local result = GameAPI.create_unit_group()
```

---

## add_unit_to_local_group

method in GameAPI

- 描述

    添加单位到本地单位组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.LocalUnit | 单位 |
    | unit_group | py.LocalUnitGroup | 本地单位组 |

- 返回值

    无

- 示例

```lua
local local_unit = GameAPI.create_local_unit(134274569, GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0)), Fix32(1))
local local_unit_group = GameAPI.get_unit_key_local_unit_group_kv(1, "key")

GameAPI.add_unit_to_local_group(local_unit, local_unit_group)
```

---

## local_unit_group_is_exist

method in GameAPI

- 描述

    本地单位组是否存在

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_group | py.LocalUnitGroup | 本地单位组 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local local_unit_group = GameAPI.get_unit_key_local_unit_group_kv(1, "key")

local result = GameAPI.local_unit_group_is_exist(local_unit_group)
```

---

## trigger_is_exist

method in GameAPI

- 描述

    触发器是否存在

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | trigger_id | py.DynamicTriggerInstance | 动态触发器实例 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local trigger_instance = GameAPI.get_last_created_trigger()

local result = GameAPI.trigger_is_exist(trigger_instance)
```

---

## mover_is_exist

method in GameAPI

- 描述

    运动器是否存在

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | mover_id | py.Mover | 运动器实例 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })
local mover = GameAPI.get_projectile_mover(projectile.handle)

local result = GameAPI.mover_is_exist(mover)
```

---

## common_is_exist

method in GameAPI

- 描述

    对象是否存在

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | py.DynamicTypeMeta | 对象 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local dynamic_type = GameAPI.get_function_return_value("func_id", y3.player.get_by_id(1):get_all_units()[1].handle, pydict(), {}, 1)

local result = GameAPI.common_is_exist(dynamic_type)
```

---

## create_harm_text_ex

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

GameAPI.create_harm_text_ex(point, "text_type", "value", player_group.handle, 1)
```

---

## set_scene_node_to_point

method in GameAPI

- 描述

    设置场景ui的位置到场景点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | scene_node | py.SceneNode | 场景点 |
    | point | py.Point | 点 |
    | visible_dis? | number | 可见距离 |
    | height_offset? | number | 离地高度 |

- 返回值

    无

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)
local player = y3.player.get_by_id(1)
local unit = player:get_all_units()[1]
local scene_node = GameAPI.create_scene_node_on_unit_ex("comp_name", player.handle, unit.handle, "origin", false)

GameAPI.set_scene_node_to_point(scene_node, point, 1.0, 1.0)
```

---

## create_scene_node_on_unit_ex

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
    | socket_offset_follow_model_scale | boolean | 挂接点偏移跟随模型缩放 |
    | visible_dis? | number | 可见距离 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SceneNode | 场景点 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

local result = GameAPI.create_scene_node_on_unit_ex("comp_name", player.handle, unit.handle, "socket_name", true, 1.0)
```

---

## create_scene_node_on_unit_new

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
    | socket_offset_follow_model_scale | boolean | 挂接点偏移跟随模型缩放 |
    | visible_dis? | number | 可见距离 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SceneNode | 场景点 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

local result = GameAPI.create_scene_node_on_unit_new("comp_name", player.handle, unit.handle, "socket_name", true, 1.0)
```

---

## get_client_role_id

method in GameAPI

- 描述

    获取本地玩家id

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 玩家id |

- 示例

```lua
local result = GameAPI.get_client_role_id()
```

---

## is_returning_player

method in GameAPI

- 描述

    玩家是否回流

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否为回流玩家 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.is_returning_player(player.handle)
```

---

## get_player_last_recommend_time

method in GameAPI

- 描述

    获取玩家上次安利墙的时间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 玩家上次安利墙的时间 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GameAPI.get_player_last_recommend_time(player.handle)
```

---

## get_role_platform_url

method in GameAPI

- 描述

    获取玩家平台头像URL

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

local result = GameAPI.get_role_platform_url(player.handle)
```

---

## set_billboard_overall_visibility

method in GameAPI

- 描述

    设置血条整体可见性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | visibility | boolean | 可见性 |
    | role? | py.Role | 玩家 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

GameAPI.set_billboard_overall_visibility(unit.handle, true)
```

---

## reset_billboard_overall_visibility

method in GameAPI

- 描述

    重置血条的整体可见性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | role? | py.Role | 玩家 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

GameAPI.reset_billboard_overall_visibility(unit.handle)
```

---

## set_billboard_picture_group

method in GameAPI

- 描述

    设置血条中进度条控件的进度条图片

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |
    | node_name | string | 血条命名 |
    | icon_id | py.Texture | 图片 |
    | role? | py.Role | 玩家 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

GameAPI.set_billboard_picture_group(unit.handle, "node_name", 1)
```

---

## open_platform_shop

method in GameAPI

- 描述

    请求购买平台道具

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | store_key | py.StoreKey | 平台道具类型 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local store_key = 134274569

GameAPI.open_platform_shop(player.handle, store_key)
```

---

## api_compare_store_key

method in GameAPI

- 描述

    平台道具是否相等

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | store_key1 | py.StoreKey | 平台道具 |
    | store_key2 | py.StoreKey | 平台道具 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否相等 |

- 示例

```lua
local store_key = 134274569

local result = GameAPI.api_compare_store_key(store_key, store_key)
```

---

## save_anticheat_data

method in GameAPI

- 描述

    上传反作弊数值统计

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | args | py.List | 自定义参数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 玩家全量昵称 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local list = {}

local result = GameAPI.save_anticheat_data(player.handle, list)
```

---

## get_plain_text_from_rich_text

method in GameAPI

- 描述

    剔除字符串内富文本信息

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | rich_text | string | 富文本 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 普通文本 |

- 示例

```lua
local result = GameAPI.get_plain_text_from_rich_text("rich_text")
```

---

## api_is_point_in_shape

method in GameAPI

- 描述

    点是否在范围内

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | check_point | py.Point | 待检查的点 |
    | center_point | py.Point | 中心点 |
    | shape | py.Shape | 范围 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 布尔值 |

- 示例

```lua
local point = Fix32Vec3(0, 0, 0)
local shape = GlobalAPI.create_circular_shape(Fix32(500))

local result = GameAPI.api_is_point_in_shape(point, point, shape)
```

---

## api_get_pseudo_random

method in GameAPI

- 描述

    保底伪随机数Roll点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | event_name | string | 事件名 |
    | event_odds | number | 期望概率(百分数) |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 布尔值 |

- 示例

```lua
local result = GameAPI.api_get_pseudo_random("event_name", 1.0)
```

---

## api_broadcast_msg

method in GameAPI

- 描述

    广播本地消息

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | msg_id | string | msg_id |
    | msg_content | string | msg_content |

- 返回值

    无

- 示例

```lua
GameAPI.api_broadcast_msg("msg_id", "msg_content")
```

---

## refresh_get_effect_on_modifier

method in GameAPI

- 描述

    遍历魔法效果的得到特效

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_entity | py.ModifierEntity | 魔法效果 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 特效idList |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

local result = GameAPI.refresh_get_effect_on_modifier(modifier.handle)
```

---

## refresh_loss_effect_on_modifier

method in GameAPI

- 描述

    遍历魔法效果的失去特效

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_entity | py.ModifierEntity | 魔法效果 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 特效idList |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

local result = GameAPI.refresh_loss_effect_on_modifier(modifier.handle)
```

---

## get_effect_on_modifier

method in GameAPI

- 描述

    获得遍历到的特效

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | effect_id | string | 特效ID拼接Str |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sfx | 特效实体 |

- 示例

```lua
local result = GameAPI.get_effect_on_modifier("effect_id")
```

---

## refresh_attach_model_on_modifier

method in GameAPI

- 描述

    遍历魔法效果的挂接模型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modifier_entity | py.ModifierEntity | 魔法效果 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.List | 挂接模型idList |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

local result = GameAPI.refresh_attach_model_on_modifier(modifier.handle)
```

---

## get_attach_model_on_modifier

method in GameAPI

- 描述

    获得遍历到的模型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attach_model_id | string | 模型ID拼接Str |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 模型ID拼接Str |

- 示例

```lua
local result = GameAPI.get_attach_model_on_modifier("attach_model_id")
```

---

## slot_type_to_str

method in GameAPI

- 描述

    背包类型转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | slot_type | py.SlotType | 背包类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local slot_type = y3.const.SlotType.BAR

local result = GameAPI.slot_type_to_str(slot_type)
```

---

## attach_model_entity_to_str

method in GameAPI

- 描述

    挂接模型实体转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attach_model_id | string | 模型ID拼接Str |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local result = GameAPI.attach_model_entity_to_str("attach_model_id")
```

---

## play_attach_model_animation

method in GameAPI

- 描述

    播放动画

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attach_model_id | string | 模型ID拼接Str |
    | name | string | 动画名称 |
    | rate? | number | 播放倍率 |
    | init_time? | number | 开始时间(s) |
    | end_time? | number | 结束时间(s)，正数 -1 表示不结束 |
    | loop? | boolean | 是否循环 |
    | return_idle? | boolean | 播放结束后是否恢复idle |

- 返回值

    无

- 示例

```lua
GameAPI.play_attach_model_animation("attach_model_id", "name", 1.0, 1.0, 1.0, true, true)
```

---

## stop_attach_model_animation

method in GameAPI

- 描述

    停止播放动画

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attach_model_id | string | 模型ID拼接Str |
    | name | string | 动画名称 |

- 返回值

    无

- 示例

```lua
GameAPI.stop_attach_model_animation("attach_model_id", "name")
```

---

## api_get_autorec_interval

method in GameAPI

- 描述

    获取属性自动恢复间隔

- 参数

    无

- 返回值

    无

- 示例

```lua
GameAPI.api_get_autorec_interval()
```

---

## get_object_multilingual_key

method in GameAPI

- 描述

    获取物编名称/描述多语言key

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | data_key | string | 物编类型 |
    | entity_id | integer | 物编对象 |
    | name_or_desc | string | 名称/描述 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 多语言key |

- 示例

```lua
local result = GameAPI.get_object_multilingual_key("data_key", 1, "name_or_desc")
```

---

## set_common_atk_quick_cast

method in GameAPI

- 描述

    设置快捷施法

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | is_on | boolean | 是否开启 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

GameAPI.set_common_atk_quick_cast(player.handle, true)
```

---
