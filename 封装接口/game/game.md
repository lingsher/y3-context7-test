---
sidebarDepth: 1
---
# Game (Game)

# 索引

Y3 编辑器 Game 游戏接口，提供游戏相关功能。

---

| 接口 | 描述 |
| --- | --- |
| [remove_unit_kv](#remove_unit_kv) | 清除单位类型键值 |
| [remove_item_kv](#remove_item_kv) | 清除物品类型键值 |
| [remove_ability_kv](#remove_ability_kv) | 清除技能类型键值 |
| [get_camp_by_id](#get_camp_by_id) | 获得阵营 |
| [set_cascaded_shadow_distance](#set_cascaded_shadow_distance) | 设置阴影距离 |
| [str_to_unit_command_type](#str_to_unit_command_type) | 字符串转单位命令类型 |
| [str_to_ability_cast_type](#str_to_ability_cast_type) | 字符串转技能释放类型 |
| [str_to_link_sfx_key](#str_to_link_sfx_key) | 字符串转链接特效 |
| [str_to_role_relation](#str_to_role_relation) | 字符串转玩家关系 |
| [str_to_unit_type](#str_to_unit_type) | 字符串转单位分类 |
| [str_to_unit_key](#str_to_unit_key) | 字符串转单位类型 |
| [str_to_unit_name](#str_to_unit_name) | 字符串转单位属性 |
| [str_to_item_key](#str_to_item_key) | 字符串转物品类型 |
| [str_to_role_res](#str_to_role_res) | 字符串转玩家属性 |
| [str_to_role_status](#str_to_role_status) | 字玩家状态转字符串 |
| [str_to_role_type](#str_to_role_type) | 字符串转玩家控制状态 |
| [str_to_ability_key](#str_to_ability_key) | 字符串转技能类型 |
| [str_to_ability_type](#str_to_ability_type) | 字符串转技能槽位类型 |
| [str_to_dest_key](#str_to_dest_key) | 字符串转可破坏物类型 |
| [str_to_project_key](#str_to_project_key) | 字符串转投射物类型 |
| [str_to_particle_sfx_key](#str_to_particle_sfx_key) | 字符串转特效 |
| [str_to_tech_key](#str_to_tech_key) | 字符串转科技类型 |
| [str_to_model_key](#str_to_model_key) | 字符串转模型类型 |
| [str_to_modifier_key](#str_to_modifier_key) | 字符串转魔法效果类型 |
| [str_to_modifier_effect_type](#str_to_modifier_effect_type) | 字符串转魔法效果影响类型 |
| [str_to_modifier_type](#str_to_modifier_type) | 字符串转魔法效果类别 |
| [str_to_camp](#str_to_camp) | 字符串转阵营 |
| [str_to_keyboard_key](#str_to_keyboard_key) | 字符串转键盘按键 |
| [str_to_mouse_key](#str_to_mouse_key) | 字符串转鼠标按键 |
| [str_to_mouse_wheel](#str_to_mouse_wheel) | 字符串转鼠标滚轮 |
| [str_to_store_key](#str_to_store_key) | 字符串转平台道具类型 |
| [str_to_damage_type](#str_to_damage_type) | 字符串转伤害类型 |
| [str_to_unit_attr_type](#str_to_unit_attr_type) | 字符串转单位属性类型 |
| [str_to_audio_key](#str_to_audio_key) | 字符串转声音类型 |
| [get_obj_icon](#get_obj_icon) | 获取任意对象图片 |
| [modify_point_texture](#modify_point_texture) | 设置某点的地形纹理 |
| [get_point_texture](#get_point_texture) | 获取地形纹理 |
| [replace_area_texture](#replace_area_texture) | 替换地形纹理 |
| [set_area_weather](#set_area_weather) | 设置区域天气 |
| [set_global_weather](#set_global_weather) | 设置全局天气 |
| [set_fog_attribute](#set_fog_attribute) | 设置雾效属性 |
| [set_fog_attr](#set_fog_attr) | 设置雾效属性(新) |
| [set_cascaded_shadow_distanc](#set_cascaded_shadow_distanc) | 设置阴影距离 |
| [set_cascaded_shadow_enable](#set_cascaded_shadow_enable) | 开关级联阴影 |
| [set_post_effect](#set_post_effect) | 为玩家切换画风 |
| [get_tech_max_level](#get_tech_max_level) | 获取科技最大等级 |
| [get_tech_icon](#get_tech_icon) | 获取科技图标 |
| [get_tech_description](#get_tech_description) | 获取科技类型的描述 |
| [get_tech_name](#get_tech_name) | 获取科技类型的名称 |
| [end_player_game](#end_player_game) | 结束玩家游戏 |
| [pause_game](#pause_game) | 暂停游戏 |
| [restart_game](#restart_game) | 开始新一轮游戏 |
| [set_game_speed](#set_game_speed) | 设置游戏运行速率 |
| [enable_soft_pause](#enable_soft_pause) | 开启软暂停 |
| [resume_soft_pause](#resume_soft_pause) | 恢复软暂停 |
| [switch_level](#switch_level) | 切换至关卡 |
| [get_level](#get_level) | 获取当前关卡 |
| [set_damage_factor](#set_damage_factor) | 设置伤害系数 |
| [set_compound_attributes](#set_compound_attributes) | 设置复合属性 |
| [get_compound_attributes](#get_compound_attributes) | 获取三维属性的影响系数 |
| [is_compound_attributes_enabled](#is_compound_attributes_enabled) | 是否开启三维属性 |
| [set_day_night_speed](#set_day_night_speed) | 设置游戏时间的流逝速度 |
| [set_day_night_time](#set_day_night_time) | 设置游戏时间 |
| [create_day_night_human_time](#create_day_night_human_time) | 创建人造时间 |
| [set_random_seed](#set_random_seed) | 设置随机数种子 |
| [toggle_day_night_time](#toggle_day_night_time) | 开关时间流逝 |
| [enable_grass_by_pos](#enable_grass_by_pos) | 开关目标点的草丛 |
| [get_current_game_mode](#get_current_game_mode) | 获取当前游戏模式 |
| [current_game_run_time](#current_game_run_time) | 游戏已运行的时间 |
| [get_day_night_time](#get_day_night_time) | 获取游戏当前昼夜时间 |
| [get_damage_ratio](#get_damage_ratio) | 获取伤害系数 |
| [get_start_mode](#get_start_mode) | 获取本局游戏环境 |
| [is_debug_mode](#is_debug_mode) | 是否是调试模式 |
| [get_global_archive](#get_global_archive) | 获取全局存档 |
| [get_archive_rank_player_archive_value](#get_archive_rank_player_archive_value) | 获取整数存档排行榜玩家存档值 |
| [get_global_weather](#get_global_weather) | 获取全局天气 |
| [locale](#locale) | 获取多语言内容 |
| [get_game_init_time_stamp](#get_game_init_time_stamp) | 获取游戏开始时间戳 |
| [get_current_server_time](#get_current_server_time) | 获取当前的服务器时间。为了保证结果的一致性需要你自己指定时区。 |
| [request_time](#request_time) | 请求真实时间。为了保证结果的一致性需要你自己指定时区。 |
| [get_game_x_resolution](#get_game_x_resolution) | 获取初始化横向分辨率 |
| [get_game_y_resolution](#get_game_y_resolution) | 获取初始化纵向分辨率 |
| [get_graphics_quality](#get_graphics_quality) | 获取初始化游戏画质 |
| [get_window_mode](#get_window_mode) | 获取窗口化类别 |
| [send_signal](#send_signal) | 发送信号 |
| [send_custom_event](#send_custom_event) | 发送自定义事件给ECA |
| [str_to_ui_event](#str_to_ui_event) | 字符串转界面事件 |
| [get_table](#get_table) | 获取表 |
| [table_has_key](#table_has_key) | 表是否存在字段 |
| [clear_table](#clear_table) | 清空表 |
| [set_globale_view](#set_globale_view) | 启用全图视野（总是可见的） |
| [set_object_color](#set_object_color) | 设置对象基础材质颜色 |
| [set_object_fresnel_visible](#set_object_fresnel_visible) | 设置对象的菲涅尔效果 |
| [set_object_fresnel](#set_object_fresnel) | 设置对象的菲涅尔效果 |
| [set_logic_fps](#set_logic_fps) | 设置逻辑帧率 |
| [encrypt_table](#encrypt_table) | 加密表 |
| [set_jump_word](#set_jump_word) | 关闭localplayer的表现层跳字 |
| [sfx_switch](#sfx_switch) | 特效播放开关 |
| [reg_sound_area](#reg_sound_area) | 注册区域的附近语音频道 |
| [unreg_sound_area](#unreg_sound_area) | 注销区域的附近语音频道 |
| [set_nearby_voice_mode](#set_nearby_voice_mode) | 设置附近语音的区域模式开关 |
| [set_nearby_sound_switch](#set_nearby_sound_switch) | 设置玩家的附近语音聊天收听开关 |
| [set_nearby_micro_switch](#set_nearby_micro_switch) | 设置玩家的附近语音聊天发言开关 |
| [set_role_micro_unit](#set_role_micro_unit) | 设置玩家的声音主单位 |
| [close_role_micro_unit](#close_role_micro_unit) | 关闭玩家的附近语音聊天 |
| [set_role_camp_sound_switch](#set_role_camp_sound_switch) | 设置玩家的同阵营语音聊天收听开关 |
| [set_role_camp_micro_switch](#set_role_camp_micro_switch) | 设置玩家的同阵营语音聊天发言开关 |
| [set_role_all_sound_switch](#set_role_all_sound_switch) | 设置玩家的所有人语音聊天收听开关 |
| [set_role_all_micro_switch](#set_role_all_micro_switch) | 设置玩家的所有人语音聊天发言开关 |
| [world_pos_to_camera_pos](#world_pos_to_camera_pos) | 世界坐标转换屏幕坐标 |
| [world_pos_to_screen_edge_pos](#world_pos_to_screen_edge_pos) | 世界坐标转换屏幕边缘坐标 |
| [load_sub_scene](#load_sub_scene) | 创建地形预设 |
| [on_client_tick](#on_client_tick) | 本地客户端每帧回调此函数 |
| [request_url](#request_url) | 发送 http 请求，成功或失败都会触发回调， |
| [download_platform_icon](#download_platform_icon) | 下载玩家平台头像，下载完毕后调用回调函数 |
| [is_lobby](#is_lobby) | 当前是否是大厅关卡 |
| [set_draw_scene](#set_draw_scene) | 设置是否渲染场景 |
| [get_local_game_version](#get_local_game_version) | 【异步】获取本地的游戏客户端版本号 |
| [get_latest_game_version](#get_latest_game_version) | 【异步】获取最新的游戏客户端版本号。获取成功后会通过回调函数返回版本号 |
| [request_map_rank](#request_map_rank) | 【异步】请求最新的存档排行榜数据。 |
| [md5](#md5) |  |
| [get_booked_number](#get_booked_number) | 获取当前地图预约人数 |

---

## remove_unit_kv

method in Game

- 描述

    清除单位类型键值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位id |
    | key | string | 键 |

- 返回值

    无

- 示例

```lua
local unit_key = 134274569

y3.game.remove_unit_kv(unit_key, "key")
```

---

## remove_item_kv

method in Game

- 描述

    清除物品类型键值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品id |
    | key | string | 键 |

- 返回值

    无

- 示例

```lua
local item_key = 134274569

y3.game.remove_item_kv(item_key, "key")
```

---

## remove_ability_kv

method in Game

- 描述

    清除技能类型键值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_key | py.AbilityKey | 技能id |
    | key | string | 键 |

- 返回值

    无

- 示例

```lua
local ability_key = 134274569

y3.game.remove_ability_kv(ability_key, "key")
```

---

## get_camp_by_id

method in Game

- 描述

    获得阵营

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | id | py.CampID | 阵营id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Camp |  |

- 示例

```lua
local result = y3.game.get_camp_by_id(134274569)
```

---

## set_cascaded_shadow_distance

method in Game

- 描述

    设置阴影距离

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | dis | number | 距离 |

- 返回值

    无

- 示例

```lua
y3.game.set_cascaded_shadow_distance(1.0)
```

---

## str_to_unit_command_type

method in Game

- 描述

    字符串转单位命令类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | str | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommandType | 单位命令类型 |

- 示例

```lua
local result = y3.game.str_to_unit_command_type("str")
```

---

## str_to_ability_cast_type

method in Game

- 描述

    字符串转技能释放类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | str | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityCastType | 技能释放类型 |

- 示例

```lua
local result = y3.game.str_to_ability_cast_type("str")
```

---

## str_to_link_sfx_key

method in Game

- 描述

    字符串转链接特效

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | str | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SfxKey | 链接特效 |

- 示例

```lua
local result = y3.game.str_to_link_sfx_key("str")
```

---

## str_to_role_relation

method in Game

- 描述

    字符串转玩家关系

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | str | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleRelation | 玩家关系 |

- 示例

```lua
local result = y3.game.str_to_role_relation("str")
```

---

## str_to_unit_type

method in Game

- 描述

    字符串转单位分类

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | str | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitType | 单位分类 |

- 示例

```lua
local result = y3.game.str_to_unit_type("str")
```

---

## str_to_unit_key

method in Game

- 描述

    字符串转单位类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | str | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitKey | 单位类型 |

- 示例

```lua
local result = y3.game.str_to_unit_key("str")
```

---

## str_to_unit_name

method in Game

- 描述

    字符串转单位属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | str | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 单位属性 |

- 示例

```lua
local result = y3.game.str_to_unit_name("str")
```

---

## str_to_item_key

method in Game

- 描述

    字符串转物品类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | str | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemKey | 物品类型 |

- 示例

```lua
local result = y3.game.str_to_item_key("str")
```

---

## str_to_role_res

method in Game

- 描述

    字符串转玩家属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | str | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleResKey | 玩家属性 |

- 示例

```lua
local result = y3.game.str_to_role_res("str")
```

---

## str_to_role_status

method in Game

- 描述

    字玩家状态转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | status | py.RoleStatus |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string |  |

- 示例

```lua
local role_status = 1

local result = y3.game.str_to_role_status(role_status)
```

---

## str_to_role_type

method in Game

- 描述

    字符串转玩家控制状态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | str | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleType | 玩家控制状态 |

- 示例

```lua
local result = y3.game.str_to_role_type("str")
```

---

## str_to_ability_key

method in Game

- 描述

    字符串转技能类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | str | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityKey | 技能类型 |

- 示例

```lua
local result = y3.game.str_to_ability_key("str")
```

---

## str_to_ability_type

method in Game

- 描述

    字符串转技能槽位类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | str | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityType | 技能槽位类型 |

- 示例

```lua
local result = y3.game.str_to_ability_type("str")
```

---

## str_to_dest_key

method in Game

- 描述

    字符串转可破坏物类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | str | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DestructibleKey | 可破坏物类型 |

- 示例

```lua
local result = y3.game.str_to_dest_key("str")
```

---

## str_to_project_key

method in Game

- 描述

    字符串转投射物类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | str | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileKey | 投射物类型 |

- 示例

```lua
local result = y3.game.str_to_project_key("str")
```

---

## str_to_particle_sfx_key

method in Game

- 描述

    字符串转特效

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | str | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SfxKey | 特效 |

- 示例

```lua
local result = y3.game.str_to_particle_sfx_key("str")
```

---

## str_to_tech_key

method in Game

- 描述

    字符串转科技类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | str | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.TechKey | 科技类型 |

- 示例

```lua
local result = y3.game.str_to_tech_key("str")
```

---

## str_to_model_key

method in Game

- 描述

    字符串转模型类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | str | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModelKey | 模型类型 |

- 示例

```lua
local result = y3.game.str_to_model_key("str")
```

---

## str_to_modifier_key

method in Game

- 描述

    字符串转魔法效果类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | str | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierKey | 魔法效果类型 |

- 示例

```lua
local result = y3.game.str_to_modifier_key("str")
```

---

## str_to_modifier_effect_type

method in Game

- 描述

    字符串转魔法效果影响类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | str | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierEffectType | 魔法效果影响类型 |

- 示例

```lua
local result = y3.game.str_to_modifier_effect_type("str")
```

---

## str_to_modifier_type

method in Game

- 描述

    字符串转魔法效果类别

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | str | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierType | 魔法效果类别 |

- 示例

```lua
local result = y3.game.str_to_modifier_type("str")
```

---

## str_to_camp

method in Game

- 描述

    字符串转阵营

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | str | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Camp | 阵营 |

- 示例

```lua
local result = y3.game.str_to_camp("str")
```

---

## str_to_keyboard_key

method in Game

- 描述

    字符串转键盘按键

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | str | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.KeyboardKey | 键盘按键 |

- 示例

```lua
local result = y3.game.str_to_keyboard_key("str")
```

---

## str_to_mouse_key

method in Game

- 描述

    字符串转鼠标按键

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | str | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MouseKey | 鼠标按键 |

- 示例

```lua
local result = y3.game.str_to_mouse_key("str")
```

---

## str_to_mouse_wheel

method in Game

- 描述

    字符串转鼠标滚轮

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | str | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MouseWheel | 鼠标滚轮 |

- 示例

```lua
local result = y3.game.str_to_mouse_wheel("str")
```

---

## str_to_store_key

method in Game

- 描述

    字符串转平台道具类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | str | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.StoreKey | 平台道具类型 |

- 示例

```lua
local result = y3.game.str_to_store_key("str")
```

---

## str_to_damage_type

method in Game

- 描述

    字符串转伤害类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | str | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 伤害类型 |

- 示例

```lua
local result = y3.game.str_to_damage_type("str")
```

---

## str_to_unit_attr_type

method in Game

- 描述

    字符串转单位属性类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | str | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 单位属性类型 |

- 示例

```lua
local result = y3.game.str_to_unit_attr_type("str")
```

---

## str_to_audio_key

method in Game

- 描述

    字符串转声音类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | str | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AudioKey | 声音类型 |

- 示例

```lua
local result = y3.game.str_to_audio_key("str")
```

---

## get_obj_icon

method in Game

- 描述

    获取任意对象图片

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | ?Unit\|Item\|Ability\|Buff | 单位|物品|技能|魔法效果 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Texture |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = y3.game.get_obj_icon(unit)
```

---

## modify_point_texture

method in Game

- 描述

    设置某点的地形纹理

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | Point | 点 |
    | terrain_type | integer | 纹理类型 |
    | range | integer | 范围 |
    | area_type | integer | 形状 |

- 返回值

    无

- 示例

```lua
local point = y3.point(0, 0)

y3.game.modify_point_texture(point, 1, 1, 1)
```

---

## get_point_texture

method in Game

- 描述

    获取地形纹理

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | Point | 点 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer |  |

- 示例

```lua
local point = y3.point(0, 0)

local result = y3.game.get_point_texture(point)
```

---

## replace_area_texture

method in Game

- 描述

    替换地形纹理

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | Area | 区域 |
    | old_texture | integer | 纹理类型 |
    | new_texture | integer | 纹理类型 |

- 返回值

    无

- 示例

```lua
local area = y3.area.create_circle_area(y3.point(0, 0), 500)

y3.game.replace_area_texture(area, 1, 1)
```

---

## set_area_weather

method in Game

- 描述

    设置区域天气

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | Area | 区域 |
    | weather | integer \| y3.Const.WeatherType | 天气 |

- 返回值

    无

- 示例

```lua
local area = y3.area.create_circle_area(y3.point(0, 0), 500)

y3.game.set_area_weather(area, 1)
```

---

## set_global_weather

method in Game

- 描述

    设置全局天气

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | weather | integer \| y3.Const.WeatherType | 天气 |

- 返回值

    无

- 示例

```lua
y3.game.set_global_weather(1)
```

---

## set_fog_attribute

method in Game

- 描述

    设置雾效属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | fog | table | 局部雾 |
    | direction | number | 朝向 |
    | pos_x | number | 位置x |
    | pos_y | number | 位置y |
    | pos_z | number | 位置z |
    | scale_x | number | 缩放x |
    | scale_y | number | 缩放y |
    | scale_z | number | 缩放z |
    | red | number | 颜色r |
    | green | number | 颜色g |
    | blue | number | 颜色b |
    | concentration | number | 浓度 |
    | speed | number | 流速 |

- 返回值

    无

- 示例

```lua
y3.game.set_fog_attribute({}, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0)
```

---

## set_fog_attr

method in Game

- 描述

    设置雾效属性(新)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | fog | table | 局部雾 |
    | attr | string | 朝向 |
    | value | number | 位置x |

- 返回值

    无

- 示例

```lua
y3.game.set_fog_attr({}, "attr", 1.0)
```

---

## set_cascaded_shadow_distanc

method in Game

- 描述

    设置阴影距离

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | distance | number | 距离 |

- 返回值

    无

- 示例

```lua
y3.game.set_cascaded_shadow_distanc(1.0)
```

---

## set_cascaded_shadow_enable

method in Game

- 描述

    开关级联阴影

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_enable | boolean | 开关 |

- 返回值

    无

- 示例

```lua
y3.game.set_cascaded_shadow_enable(true)
```

---

## set_post_effect

method in Game

- 描述

    为玩家切换画风

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | processing | py.PostEffect | 画风 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local post_effect = 1

y3.game.set_post_effect(player, post_effect)
```

---

## get_tech_max_level

method in Game

- 描述

    获取科技最大等级

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_id | py.TechKey | 科技id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 最大等级 |

- 示例

```lua
local tech_key = 134274569

local result = y3.game.get_tech_max_level(tech_key)
```

---

## get_tech_icon

method in Game

- 描述

    获取科技图标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_id | py.TechKey | 科技 |
    | index | integer | 等级 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Texture | 图标id |

- 示例

```lua
local tech_key = 134274569

local result = y3.game.get_tech_icon(tech_key, 1)
```

---

## get_tech_description

method in Game

- 描述

    获取科技类型的描述

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_id | py.TechKey | 科技类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 描述 |

- 示例

```lua
local tech_key = 134274569

local result = y3.game.get_tech_description(tech_key)
```

---

## get_tech_name

method in Game

- 描述

    获取科技类型的名称

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_id | py.TechKey | 科技类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 名称 |

- 示例

```lua
local tech_key = 134274569

local result = y3.game.get_tech_name(tech_key)
```

---

## end_player_game

method in Game

- 描述

    结束玩家游戏

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | result | string | 结果 |
    | is_show | boolean | 是否展示界面 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

y3.game.end_player_game(player, "result", true)
```

---

## pause_game

method in Game

- 描述

    暂停游戏

- 参数

    无

- 返回值

    无

- 示例

```lua
y3.game.pause_game()
```

---

## restart_game

method in Game

- 描述

    开始新一轮游戏

- 参数

    无

- 返回值

    无

- 示例

```lua
y3.game.restart_game()
```

---

## set_game_speed

method in Game

- 描述

    设置游戏运行速率

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | speed | number | 速率 |

- 返回值

    无

- 示例

```lua
y3.game.set_game_speed(1.0)
```

---

## enable_soft_pause

method in Game

- 描述

    开启软暂停

- 参数

    无

- 返回值

    无

- 示例

```lua
y3.game.enable_soft_pause()
```

---

## resume_soft_pause

method in Game

- 描述

    恢复软暂停

- 参数

    无

- 返回值

    无

- 示例

```lua
y3.game.resume_soft_pause()
```

---

## switch_level

method in Game

- 描述

    切换至关卡

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | level_id_str | py.Map \| string | 关卡ID |

- 返回值

    无

- 示例

```lua
y3.game.switch_level("level_id_str")
```

---

## get_level

method in Game

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
local result = y3.game.get_level()
```

---

## set_damage_factor

method in Game

- 描述

    设置伤害系数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attack_type | integer | 攻击类型 |
    | armor_type | integer | 护甲类型 |
    | ratio | number | 系数 |

- 返回值

    无

- 示例

```lua
y3.game.set_damage_factor(1, 1, 1.0)
```

---

## set_compound_attributes

method in Game

- 描述

    设置复合属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | primary_attribute | string | 一级属性 |
    | secondary_attr | string | 二级属性 |
    | value | number | 属性值 |

- 返回值

    无

- 示例

```lua
y3.game.set_compound_attributes("primary_attribute", "secondary_attr", 1.0)
```

---

## get_compound_attributes

method in Game

- 描述

    获取三维属性的影响系数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | primary_attribute | string | 一级属性 |
    | secondary_attr | string | 二级属性 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 系数 |

- 示例

```lua
local result = y3.game.get_compound_attributes("primary_attribute", "secondary_attr")
```

---

## is_compound_attributes_enabled

method in Game

- 描述

    是否开启三维属性

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否开启 |

- 示例

```lua
local result = y3.game.is_compound_attributes_enabled()
```

---

## set_day_night_speed

method in Game

- 描述

    设置游戏时间的流逝速度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | speed | number | 速度 |

- 返回值

    无

- 示例

```lua
y3.game.set_day_night_speed(1.0)
```

---

## set_day_night_time

method in Game

- 描述

    设置游戏时间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | time | number | 时间 |

- 返回值

    无

- 示例

```lua
y3.game.set_day_night_time(1.0)
```

---

## create_day_night_human_time

method in Game

- 描述

    创建人造时间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | time | number | 时间 |
    | dur | number | 持续时间 |

- 返回值

    无

- 示例

```lua
y3.game.create_day_night_human_time(1.0, 1.0)
```

---

## set_random_seed

method in Game

- 描述

    设置随机数种子

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | seed | integer | 随机种子 |

- 返回值

    无

- 示例

```lua
y3.game.set_random_seed(1)
```

---

## toggle_day_night_time

method in Game

- 描述

    开关时间流逝

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_on | boolean | 开关 |

- 返回值

    无

- 示例

```lua
y3.game.toggle_day_night_time(true)
```

---

## enable_grass_by_pos

method in Game

- 描述

    开关目标点的草丛

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_on | boolean | 开关 |
    | point | Point | 点 |

- 返回值

    无

- 示例

```lua
local point = y3.point(0, 0)

y3.game.enable_grass_by_pos(true, point)
```

---

## get_current_game_mode

method in Game

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
local result = y3.game.get_current_game_mode()
```

---

## current_game_run_time

method in Game

- 描述

    游戏已运行的时间

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 时间 |

- 示例

```lua
local result = y3.game.current_game_run_time()
```

---

## get_day_night_time

method in Game

- 描述

    获取游戏当前昼夜时间

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 时间 |

- 示例

```lua
local result = y3.game.get_day_night_time()
```

---

## get_damage_ratio

method in Game

- 描述

    获取伤害系数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attack_type | integer | 攻击类型 |
    | area_type | integer | 护甲类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 伤害系数 |

- 示例

```lua
local result = y3.game.get_damage_ratio(1, 1)
```

---

## get_start_mode

method in Game

- 描述

    获取本局游戏环境

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 游戏环境，1是编辑器，2是平台 |

- 示例

```lua
local result = y3.game.get_start_mode()
```

---

## is_debug_mode

method in Game

- 描述

    是否是调试模式

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ignore_config? | boolean | 是否忽略用户的设置 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean |  |

- 示例

```lua
local result = y3.game.is_debug_mode(true)
```

---

## get_global_archive

method in Game

- 描述

    获取全局存档

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | name | string | 存档名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 存档 |

- 示例

```lua
local result = y3.game.get_global_archive("name")
```

---

## get_archive_rank_player_archive_value

method in Game

- 描述

    获取整数存档排行榜玩家存档值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | file | integer | 存档 |
    | index | integer | 序号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 存档值 |

- 示例

```lua
local result = y3.game.get_archive_rank_player_archive_value(1, 1)
```

---

## get_global_weather

method in Game

- 描述

    获取全局天气

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 天气 |

- 示例

```lua
local result = y3.game.get_global_weather()
```

---

## locale

method in Game

- 描述

    获取多语言内容

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | integer\|string | 多语言key |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string |  |

- 示例

```lua
local result = y3.game.locale("key")
```

---

## get_game_init_time_stamp

method in Game

- 描述

    获取游戏开始时间戳

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 时间戳 |

- 示例

```lua
local result = y3.game.get_game_init_time_stamp()
```

---

## get_current_server_time

method in Game

- 描述

    获取当前的服务器时间。为了保证结果的一致性需要你自己指定时区。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | time_zone? | integer | 时区，默认为0。获取中国的时间请传入8。 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | ServerTime |  |

- 示例

```lua
local result = y3.game.get_current_server_time(1)
```

---

## request_time

method in Game

- 描述

    请求真实时间。为了保证结果的一致性需要你自己指定时区。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | time_zone | integer | 时区，默认为0。获取中国的时间请传入8。 |
    | callback | fun(time: | ServerTime) |

- 返回值

    无

- 示例

```lua
y3.game.request_time(1, function() end)
```

---

## get_game_x_resolution

method in Game

- 描述

    获取初始化横向分辨率

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 横向分辨率 |

- 示例

```lua
local result = y3.game.get_game_x_resolution()
```

---

## get_game_y_resolution

method in Game

- 描述

    获取初始化纵向分辨率

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 纵向分辨率 |

- 示例

```lua
local result = y3.game.get_game_y_resolution()
```

---

## get_graphics_quality

method in Game

- 描述

    获取初始化游戏画质

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | 'low' | | 'medium' | 'high' quality 画质 |

- 示例

```lua
local result = y3.game.get_graphics_quality()
```

---

## get_window_mode

method in Game

- 描述

    获取窗口化类别

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Game.WindowMode | 窗口化类别 |

- 示例

```lua
local result = y3.game.get_window_mode()
```

---

## send_signal

method in Game

- 描述

    发送信号

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | signal_enum | y3.Const.SignalType | 信号枚举值 |
    | point | Point | 点 |
    | visible_enum | y3.Const.VisibleType | 可见性枚举值 |

- 返回值

    无

- 示例

```lua
local point = y3.point(0, 0)
local player = y3.player.get_by_id(1)
local signal_type = '普通'
local visible_type = '全体'

y3.game.send_signal(player, signal_type, point, visible_type)
```

---

## send_custom_event

method in Game

- 描述

    发送自定义事件给ECA

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | id | integer | 事件id |
    | table | table | 事件数据 |

- 返回值

    无

- 示例

```lua
y3.game.send_custom_event(1, {})
```

---

## str_to_ui_event

method in Game

- 描述

    字符串转界面事件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | str | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string |  |

- 示例

```lua
local result = y3.game.str_to_ui_event("str")
```

---

## get_table

method in Game

- 描述

    获取表

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | name | string | 表名 |
    | as_lua? | boolean | 是否将表中的数据转换为Lua的数据类型，例如Fix32转number |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | table | 表 |

- 示例

```lua
local result = y3.game.get_table("name", true)
```

---

## table_has_key

method in Game

- 描述

    表是否存在字段

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | table | table |  |
    | key | string |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean |  |

- 示例

```lua
local result = y3.game.table_has_key({}, "key")
```

---

## clear_table

method in Game

- 描述

    清空表

- 参数

    无

- 返回值

    无

- 示例

```lua
y3.game.clear_table()
```

---

## set_globale_view

method in Game

- 描述

    启用全图视野（总是可见的）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | enable | boolean |  |

- 返回值

    无

- 示例

```lua
y3.game.set_globale_view(true)
```

---

## set_object_color

method in Game

- 描述

    设置对象基础材质颜色

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | Unit\|Item\|Destructible |  |
    | r | integer | 红色（0~255） |
    | g | integer | 绿色（0~255） |
    | b | integer | 蓝色（0~255） |
    | a? | integer | 强度（0~100） |
    | o? | number | 不透明度（0~1） |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

y3.game.set_object_color(unit, 1, 1, 1, 1, 1.0)
```

---

## set_object_fresnel_visible

method in Game

- 描述

    设置对象的菲涅尔效果

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | Unit\|Item\|Destructible |  |
    | b | boolean |  |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

y3.game.set_object_fresnel_visible(unit, true)
```

---

## set_object_fresnel

method in Game

- 描述

    设置对象的菲涅尔效果

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | Unit\|Item\|Destructible |  |
    | r? | integer | R |
    | g? | integer | G |
    | b? | integer | B |
    | alpha? | number | alpha |
    | exp? | number | exp |
    | strength? | number | strength |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

y3.game.set_object_fresnel(unit, 1, 1, 1, 1.0, 1.0, 1.0)
```

---

## set_logic_fps

method in Game

- 描述

    设置逻辑帧率

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | fps | integer | 帧率 |

- 返回值

    无

- 示例

```lua
y3.game.set_logic_fps(1)
```

---

## encrypt_table

method in Game

- 描述

    加密表

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tab | table | 表 |

- 返回值

    无

- 示例

```lua
y3.game.encrypt_table({})
```

---

## set_jump_word

method in Game

- 描述

    关闭localplayer的表现层跳字

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | enable | boolean | 是否关闭 |

- 返回值

    无

- 示例

```lua
y3.game.set_jump_word(true)
```

---

## sfx_switch

method in Game

- 描述

    特效播放开关

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | switch | boolean | 是否关闭 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

y3.game.sfx_switch(player, true)
```

---

## reg_sound_area

method in Game

- 描述

    注册区域的附近语音频道

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | Area | 区域 |

- 返回值

    无

- 示例

```lua
local area = y3.area.create_circle_area(y3.point(0, 0), 500)

y3.game.reg_sound_area(area)
```

---

## unreg_sound_area

method in Game

- 描述

    注销区域的附近语音频道

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | Area | 区域 |

- 返回值

    无

- 示例

```lua
local area = y3.area.create_circle_area(y3.point(0, 0), 500)

y3.game.unreg_sound_area(area)
```

---

## set_nearby_voice_mode

method in Game

- 描述

    设置附近语音的区域模式开关

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | switch | boolean | 是否关闭 |

- 返回值

    无

- 示例

```lua
y3.game.set_nearby_voice_mode(true)
```

---

## set_nearby_sound_switch

method in Game

- 描述

    设置玩家的附近语音聊天收听开关

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | switch | boolean | 是否关闭 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

y3.game.set_nearby_sound_switch(player, true)
```

---

## set_nearby_micro_switch

method in Game

- 描述

    设置玩家的附近语音聊天发言开关

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | switch | boolean | 是否关闭 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

y3.game.set_nearby_micro_switch(player, true)
```

---

## set_role_micro_unit

method in Game

- 描述

    设置玩家的声音主单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | unit | Unit | 是否关闭 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

y3.game.set_role_micro_unit(player, unit)
```

---

## close_role_micro_unit

method in Game

- 描述

    关闭玩家的附近语音聊天

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

y3.game.close_role_micro_unit(player)
```

---

## set_role_camp_sound_switch

method in Game

- 描述

    设置玩家的同阵营语音聊天收听开关

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | switch | boolean | 是否关闭 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

y3.game.set_role_camp_sound_switch(player, true)
```

---

## set_role_camp_micro_switch

method in Game

- 描述

    设置玩家的同阵营语音聊天发言开关

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | switch | boolean | 是否关闭 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

y3.game.set_role_camp_micro_switch(player, true)
```

---

## set_role_all_sound_switch

method in Game

- 描述

    设置玩家的所有人语音聊天收听开关

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | switch | boolean | 是否关闭 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

y3.game.set_role_all_sound_switch(player, true)
```

---

## set_role_all_micro_switch

method in Game

- 描述

    设置玩家的所有人语音聊天发言开关

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | switch | boolean | 是否关闭 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

y3.game.set_role_all_micro_switch(player, true)
```

---

## world_pos_to_camera_pos

method in Game

- 描述

    世界坐标转换屏幕坐标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | world_pos | Point | 世界坐标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | x, number y 屏幕坐标 |

- 示例

```lua
local point = y3.point(0, 0)

local result = y3.game.world_pos_to_camera_pos(point)
```

---

## world_pos_to_screen_edge_pos

method in Game

- 描述

    世界坐标转换屏幕边缘坐标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | world_pos | Point |  |
    | delta_dis | number |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | x, number y |

- 示例

```lua
local point = y3.point(0, 0)

local result = y3.game.world_pos_to_screen_edge_pos(point, 1.0)
```

---

## load_sub_scene

method in Game

- 描述

    创建地形预设

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | Point | 点 |
    | level_id | string | 关卡ID，通过 `y3.game.get_level()` 获取 |
    | rotate? | integer | 旋转角度 |
    | has_light? | boolean | 是否携带灯光 |
    | has_decoration? | boolean | 是否携带装饰物 |
    | has_fog? | boolean | 是否携带雾效 |
    | has_collision? | boolean | 是否携带碰撞 |
    | has_projectile? | boolean | 是否携带投射物 |
    | has_item? | boolean | 是否携带物品 |
    | has_destructible? | boolean | 是否携带可破坏物 |

- 返回值

    无

- 示例

```lua
local point = y3.point(0, 0)

y3.game.load_sub_scene(point, "level_id", 1, true, true, true, true, true, true, true)
```

---

## on_client_tick

method in Game

- 描述

    本地客户端每帧回调此函数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | callback | fun(local_player: | Player) |

- 返回值

    无

- 示例

```lua
y3.game.on_client_tick(function() end)
```

---

## request_url

method in Game

- 描述

    发送 http 请求，成功或失败都会触发回调，

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | url | string |  |
    | body? | string |  |
    | callback? | fun(body?: | string) |
    | options? | HttpRequestOptions |  |

- 返回值

    无

- 示例

```lua


y3.game:request_url("url", "body")
```

---

## download_platform_icon

method in Game

- 描述

    下载玩家平台头像，下载完毕后调用回调函数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | url | string | 头像下载地址 |
    | icon | string | 头像路径，如果本地已有头像则不会下载而是立即调用回调函数 |
    | callback | fun(real_path: | string) # 下载完毕后的回调函数 |

- 返回值

    无

- 示例

```lua
y3.game.download_platform_icon("url", "icon", function() end)
```

---

## is_lobby

method in Game

- 描述

    当前是否是大厅关卡

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean |  |

- 示例

```lua
local result = y3.game.is_lobby()
```

---

## set_draw_scene

method in Game

- 描述

    设置是否渲染场景

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | flag | boolean |  |

- 返回值

    无

- 示例

```lua
y3.game.set_draw_scene(true)
```

---

## get_local_game_version

method in Game

- 描述

    【异步】获取本地的游戏客户端版本号

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer |  |

- 示例

```lua
local result = y3.game.get_local_game_version()
```

---

## get_latest_game_version

method in Game

- 描述

    【异步】获取最新的游戏客户端版本号。获取成功后会通过回调函数返回版本号

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | callback | fun(version: | integer) |

- 返回值

    无

- 示例

```lua
y3.game.get_latest_game_version(function() end)
```

---

## request_map_rank

method in Game

- 描述

    【异步】请求最新的存档排行榜数据。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | save_index | integer | 存档栏位 |
    | callback? | fun() | 排行榜刷新完成后的回调函数 |

- 返回值

    无

- 示例

```lua
y3.game.request_map_rank(1)
```

---

## md5

method in Game

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | str | string |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string |  |

- 示例

```lua
local result = y3.game.md5("str")
```

---

## get_booked_number

method in Game

- 描述

    获取当前地图预约人数

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer |  |

- 示例

```lua
local result = y3.game.get_booked_number()
```

---
