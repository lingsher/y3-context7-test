---
sidebarDepth: 1
---
# 玩家 (Role)

# 索引

Y3 编辑器玩家对象相关接口，用于操作玩家的属性、资源、单位等。

---

| 接口 | 描述 |
| --- | --- |
| [api_get_role_id](#api_get_role_id) | 玩家获取玩家ID |
| [api_get_camp_id](#api_get_camp_id) | 获取玩家所属阵营ID |
| [get_role_id_num](#get_role_id_num) | 获取玩家ID数值 |
| [get_camp_id_num](#get_camp_id_num) | 获取玩家所属阵营ID数值 |
| [get_role_name](#get_role_name) | 获取玩家名字 |
| [get_role__unique_name](#get_role__unique_name) | 获取玩家唯一名字 |
| [get_role_plat_map_level](#get_role_plat_map_level) | 获取玩家平台等级 |
| [get_role_type](#get_role_type) | 获取玩家控制者类型 |
| [is_middle_join](#is_middle_join) | 玩家是否中途加入 |
| [api_get_camp](#api_get_camp) | 获取玩家所属阵营对象 |
| [set_attr_val](#set_attr_val) | 玩家设置属性 |
| [get_all_unit_id](#get_all_unit_id) | 获取玩家所有单位对象 |
| [set_role_exp_rate](#set_role_exp_rate) | 设置玩家经验获得率 |
| [get_role_exp_rate](#get_role_exp_rate) | 获得玩家经验倍率 |
| [set_role_spawn_point](#set_role_spawn_point) | 设置玩家出生点 |
| [get_role_spawn_point](#get_role_spawn_point) | 获取玩家出生点 |
| [api_set_camp](#api_set_camp) | 设置玩家队伍ID |
| [set_role_name](#set_role_name) | 设置玩家名字 |
| [change_role_res](#change_role_res) | 修改玩家资源 |
| [set_role_res](#set_role_res) | 设置玩家资源 |
| [get_role_res](#get_role_res) | 获得玩家资源 |
| [set_group_navigate_mode](#set_group_navigate_mode) | 设置玩家群体寻路严格模式 |
| [set_save_data_int_value](#set_save_data_int_value) | 设置整数型参数到玩家存档栏位 |
| [add_save_data_int_value](#add_save_data_int_value) | 增加整数型参数到玩家存档栏位 |
| [mult_save_data_value](#mult_save_data_value) | 乘量实数型参数到玩家存档栏位 |
| [set_save_data_fixed_value](#set_save_data_fixed_value) | 设置实数型参数到玩家存档栏位 |
| [add_save_data_fixed_value](#add_save_data_fixed_value) | 增加实数型参数到玩家存档栏位 |
| [set_save_data_bool_value](#set_save_data_bool_value) | 设置布尔型参数到玩家存档栏位 |
| [set_save_data_str_value](#set_save_data_str_value) | 设置字符串型参数到玩家存档栏位 |
| [set_save_data_table_value](#set_save_data_table_value) | 设置表型参数到玩家存档栏位 |
| [set_save_table_key_value](#set_save_table_key_value) | set_save_table_key_value |
| [add_save_table_key_value](#add_save_table_key_value) | add_save_table_key_value |
| [multiply_save_table_key_value](#multiply_save_table_key_value) | multiply_save_table_key_value |
| [remove_save_table_key_value](#remove_save_table_key_value) | remove_save_table_key_value |
| [get_save_table_key_value](#get_save_table_key_value) | get_save_table_key_value |
| [upload_save_data](#upload_save_data) | 上传玩家存档数据 |
| [add_global_map_archive_data](#add_global_map_archive_data) | 增加当前地图的指定key的存档值 |
| [get_player_rank_num](#get_player_rank_num) | 获取玩家指定的全局存档key值对应排行榜的排名 |
| [get_player_archive_rank_num](#get_player_archive_rank_num) | 获取玩家指定的个人存档栏位对应排行榜的排名 |
| [download_save_data](#download_save_data) | 下载玩家存档数据 |
| [reset_download_save_data_callback](#reset_download_save_data_callback) | 重置下载档案数据回调 |
| [get_save_data_int_value](#get_save_data_int_value) | 读取整数型玩家存档数据 |
| [get_save_data_fixed_value](#get_save_data_fixed_value) | 读取实数型玩家存档数据 |
| [get_save_data_bool_value](#get_save_data_bool_value) | 读取布尔型玩家存档数据 |
| [get_save_data_str_value](#get_save_data_str_value) | 读取字符串型玩家存档数据 |
| [get_save_data_table_value](#get_save_data_table_value) | 读取表型玩家存档数据 |
| [get_encry_uuid](#get_encry_uuid) | 获取玩家加密uuid |
| [api_use_store_item](#api_use_store_item) | 玩家使用收费道具 |
| [get_store_item_cnt](#get_store_item_cnt) | 获取玩家收费道具数量 |
| [get_visibility_of_unit](#get_visibility_of_unit) | 玩家是否拥有单位的可见性 |
| [api_change_tech_level](#api_change_tech_level) | 修改玩家科技等级 |
| [api_set_tech_level](#api_set_tech_level) | 修改玩家科技等级 |
| [api_get_tech_level](#api_get_tech_level) | 获取玩家科技等级 |
| [is_point_visible_to_player](#is_point_visible_to_player) | 点对于玩家是否可见 |
| [is_point_in_fog](#is_point_in_fog) | 点是否在迷雾中 |
| [is_point_in_shadow](#is_point_in_shadow) | 点是否在黑色阴影中 |
| [get_role_status](#get_role_status) | 获取玩家状态 |
| [set_role_hostility](#set_role_hostility) | 设置玩家是否是敌对关系 |
| [players_is_alliance](#players_is_alliance) | 玩家是否是同盟关系 |
| [players_is_enemy](#players_is_enemy) | 玩家是否是敌对关系 |
| [share_source_player_vision_to_target](#share_source_player_vision_to_target) | 原始玩家对目标玩家开放视野 |
| [close_source_player_vision_to_target](#close_source_player_vision_to_target) | 原始玩家对目标玩家关闭视野 |
| [share_source_unit_vision_to_target](#share_source_unit_vision_to_target) | 原始单位对目标玩家开放视野 |
| [close_source_unit_vision_to_target](#close_source_unit_vision_to_target) | 原始单位对目标玩家关闭视野 |
| [role_select_unit](#role_select_unit) | 选中单位或单位组 |
| [set_role_mouse_left_click](#set_role_mouse_left_click) | 开/关玩家鼠标的点选 |
| [set_role_mouse_move_select](#set_role_mouse_move_select) | 开/关玩家的鼠标的框选 |
| [set_role_mouse_wheel](#set_role_mouse_wheel) | 开/关玩家的鼠标滚轮 |
| [set_role_vignetting_enable](#set_role_vignetting_enable) | 设置玩家暗角开关 |
| [set_role_vignetting_size](#set_role_vignetting_size) | 设置玩家暗角大小 |
| [set_role_vignetting_breath_rate](#set_role_vignetting_breath_rate) | 设置玩家暗角呼吸周期 |
| [set_role_vignetting_change_range](#set_role_vignetting_change_range) | 设置玩家暗角变化幅度 |
| [set_role_vignetting_color](#set_role_vignetting_color) | 设置玩家暗角颜色 |
| [api_set_role_editable_game_func](#api_set_role_editable_game_func) | 设置玩家的基础操作快捷键（过滤掉禁止修改的） |
| [api_set_role_all_game_func_enable](#api_set_role_all_game_func_enable) | 设置玩家的基础操作开关（包含所有基础操作） |
| [api_is_conf_of_editable_game_func](#api_is_conf_of_editable_game_func) | 基础操作响应的快捷键是否已被占用（过滤掉禁止修改的） |
| [api_get_editable_game_func_of_shortcut](#api_get_editable_game_func_of_shortcut) | 获取玩家响应键盘按键的基础操作（过滤掉禁止修改的） |
| [set_bool_hit_point_data](#set_bool_hit_point_data) | 设置玩家布尔埋点数据 |
| [set_int_hit_point_data](#set_int_hit_point_data) | 设置玩家整型埋点数据 |
| [api_set_follow_distance](#api_set_follow_distance) | 设置跟随距离 |
| [api_set_role_cursor](#api_set_role_cursor) | 设置玩家的鼠标样式 |
| [api_set_role_skill_indicator](#api_set_role_skill_indicator) | 设置玩家的技能指示器特效 |
| [api_get_role_color](#api_get_role_color) | 获取玩家颜色 |
| [api_is_honor_vip](#api_is_honor_vip) | 玩家是否为平台荣耀会员 |
| [api_is_cur_map_author](#api_is_cur_map_author) | 玩家是否为当前作者 |
| [api_get_equip_deco_id](#api_get_equip_deco_id) | 获取玩家装备装饰类型的ID |
| [api_get_map_level](#api_get_map_level) | 获取玩家在本地图的等级 |
| [api_get_played_times](#api_get_played_times) | 获取玩家在本地图的累计局数 |
| [api_get_map_level_rank](#api_get_map_level_rank) | 玩家在本地图的平台等级排名 |
| [api_get_sign_in_days_of_platform](#api_get_sign_in_days_of_platform) | 玩家签到天数 |
| [api_get_community_value](#api_get_community_value) | 玩家在社区的互动 |
| [api_is_returning_player](#api_is_returning_player) | 玩家是否是当前地图的回流用户 |
| [api_is_bookmark_current_map](#api_is_bookmark_current_map) | 玩家是否收藏当前地图 |
| [api_get_ladder_rank_points](#api_get_ladder_rank_points) | 获取玩家当前赛季天梯的排位积分 |
| [api_get_role_total_consume](#api_get_role_total_consume) | 获取玩家该地图累计充值 |
| [api_get_role_is_donated](#api_get_role_is_donated) | 获取玩家是否打赏该地图 |
| [set_archive_group_value](#set_archive_group_value) | 设置存档组数据 |
| [get_archive_group_value](#get_archive_group_value) | 读取字符串型玩家存档组数据 |
| [copy_save_data_table_value](#copy_save_data_table_value) | 复制表型存档到玩家存档栏位 |
| [force_upload_save_data](#force_upload_save_data) | 强制上传玩家非实时存档 |
| [get_store_item_expired_time](#get_store_item_expired_time) | 获取平台道具到期时间戳 |
| [set_role_vignetting_color_hex](#set_role_vignetting_color_hex) | 设置玩家暗角颜色(HEX) |
| [upload_player_game_rank](#upload_player_game_rank) | 上报玩家排名 |
| [api_get_role_select_units](#api_get_role_select_units) | 获取玩家当前选中单位组 |
| [update_player_save_rank](#update_player_save_rank) | 更新玩家存档排行榜 |
| [api_get_current_season_id](#api_get_current_season_id) | 获取玩家当前赛季天梯编号 |
| [api_get_current_season_standing](#api_get_current_season_standing) | 获取玩家当前赛季天梯排名 |
| [api_get_current_season_standing_number](#api_get_current_season_standing_number) | 获取玩家当前赛天梯排名次数 |
| [api_get_number_of_expeditions](#api_get_number_of_expeditions) | 获取玩家当前地图探险次数 |
| [api_get_time_of_expeditions](#api_get_time_of_expeditions) | 获取玩家当前地图探险时长 |
| [api_get_role_store_params](#api_get_role_store_params) | 获取玩家商城登录用token |
| [api_get_role_achieve_point](#api_get_role_achieve_point) | 获取玩家当前地图的成就点数 |
| [api_get_role_achieve_unlock](#api_get_role_achieve_unlock) | 获取玩家当前地图成就是否解锁 |
| [api_get_number_of_lottery](#api_get_number_of_lottery) | 获取玩家当前地图指定宝箱的抽取次数 |
| [api_get_number_of_all_lottery](#api_get_number_of_all_lottery) | 获取玩家当前地图抽取宝箱的总次数 |
| [api_get_guild_name](#api_get_guild_name) | 获取玩家所在公会名 |
| [api_get_guild_announcement](#api_get_guild_announcement) | 获取玩家所在公会公告 |
| [api_get_guild_member_count](#api_get_guild_member_count) | 获取玩家所在公会人数 |
| [api_get_guild_level](#api_get_guild_level) | 获取玩家所在公会等级 |
| [pet_http_request](#pet_http_request) | 宠物http请求调用 |
| [request_create_private_dungeon](#request_create_private_dungeon) | 请求创建私有副本 |
| [request_join_private_dungeon](#request_join_private_dungeon) | 请求加入私有副本 |
| [request_join_public_dungeon](#request_join_public_dungeon) | 请求加入公有副本 |
| [get_role_general_depot](#get_role_general_depot) | 获取玩家武将信息 |

---

## api_get_role_id

method in Role

- 描述

    玩家获取玩家ID

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleID? | 玩家ID |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:api_get_role_id()
```

---

## api_get_camp_id

method in Role

- 描述

    获取玩家所属阵营ID

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 玩家所属阵营ID |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:api_get_camp_id()
```

---

## get_role_id_num

method in Role

- 描述

    获取玩家ID数值

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 玩家ID数值 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:get_role_id_num()
```

---

## get_camp_id_num

method in Role

- 描述

    获取玩家所属阵营ID数值

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 玩家所属阵营ID数值 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:get_camp_id_num()
```

---

## get_role_name

method in Role

- 描述

    获取玩家名字

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string? | 玩家名字 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:get_role_name()
```

---

## get_role__unique_name

method in Role

- 描述

    获取玩家唯一名字

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string? | 玩家唯一名字 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:get_role__unique_name()
```

---

## get_role_plat_map_level

method in Role

- 描述

    获取玩家平台等级

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 玩家等级 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:get_role_plat_map_level()
```

---

## get_role_type

method in Role

- 描述

    获取玩家控制者类型

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleType? | 玩家控制者类型 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:get_role_type()
```

---

## is_middle_join

method in Role

- 描述

    玩家是否中途加入

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 是否中途加入 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:is_middle_join()
```

---

## api_get_camp

method in Role

- 描述

    获取玩家所属阵营对象

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Camp? | 阵营对象 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:api_get_camp()
```

---

## set_attr_val

method in Role

- 描述

    玩家设置属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | k | string | 属性名 |
    | value | integer | 属性值 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

role.handle:set_attr_val("k", 1)
```

---

## get_all_unit_id

method in Role

- 描述

    获取玩家所有单位对象

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitGroup? | 单位对象列表 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:get_all_unit_id()
```

---

## set_role_exp_rate

method in Role

- 描述

    设置玩家经验获得率

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | rate | number | 倍率 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

role.handle:set_role_exp_rate(1.0)
```

---

## get_role_exp_rate

method in Role

- 描述

    获得玩家经验倍率

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 返回倍率 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:get_role_exp_rate()
```

---

## set_role_spawn_point

method in Role

- 描述

    设置玩家出生点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.Point | 点 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)
local point = Fix32Vec3(0, 0, 0)

role.handle:set_role_spawn_point(point)
```

---

## get_role_spawn_point

method in Role

- 描述

    获取玩家出生点

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3? | 返回出生点位置 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:get_role_spawn_point()
```

---

## api_set_camp

method in Role

- 描述

    设置玩家队伍ID

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | new_camp | py.Camp | 队伍ID |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)
local camp = GameAPI.get_camp_by_camp_id(1)

role.handle:api_set_camp(camp)
```

---

## set_role_name

method in Role

- 描述

    设置玩家名字

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | name | string | 名字 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

role.handle:set_role_name("name")
```

---

## change_role_res

method in Role

- 描述

    修改玩家资源

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | res_key | py.RoleResKey | 资源名 |
    | res_cnt | py.Fixed | 资源值 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)
local role_res_key = "res_key"

role.handle:change_role_res(role_res_key, Fix32(1))
```

---

## set_role_res

method in Role

- 描述

    设置玩家资源

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | res_key | py.RoleResKey | 资源名 |
    | res_cnt | py.Fixed | 资源值 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)
local role_res_key = "res_key"

role.handle:set_role_res(role_res_key, Fix32(1))
```

---

## get_role_res

method in Role

- 描述

    获得玩家资源

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | res_key | py.RoleResKey | 资源名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 资源值 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)
local role_res_key = "res_key"

local result = role.handle:get_role_res(role_res_key)
```

---

## set_group_navigate_mode

method in Role

- 描述

    设置玩家群体寻路严格模式

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | group_navigate_mode | boolean | 开启群体寻路严格模式 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

role.handle:set_group_navigate_mode(true)
```

---

## set_save_data_int_value

method in Role

- 描述

    设置整数型参数到玩家存档栏位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | index | integer | 玩家存档栏位 |
    | value | integer | 整型参数 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

role.handle:set_save_data_int_value(1, 1)
```

---

## add_save_data_int_value

method in Role

- 描述

    增加整数型参数到玩家存档栏位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | index | integer | 玩家存档栏位 |
    | value | integer | 整型参数 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

role.handle:add_save_data_int_value(1, 1)
```

---

## mult_save_data_value

method in Role

- 描述

    乘量实数型参数到玩家存档栏位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | index | integer | 玩家存档栏位 |
    | value | py.Fixed | 实数型参数 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

role.handle:mult_save_data_value(1, Fix32(1))
```

---

## set_save_data_fixed_value

method in Role

- 描述

    设置实数型参数到玩家存档栏位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | index | integer | 玩家存档栏位 |
    | value | py.Fixed | 实数型参数 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

role.handle:set_save_data_fixed_value(1, Fix32(1))
```

---

## add_save_data_fixed_value

method in Role

- 描述

    增加实数型参数到玩家存档栏位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | index | integer | 玩家存档栏位 |
    | value | py.Fixed | 实数型参数 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

role.handle:add_save_data_fixed_value(1, Fix32(1))
```

---

## set_save_data_bool_value

method in Role

- 描述

    设置布尔型参数到玩家存档栏位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | index | integer | 玩家存档栏位 |
    | value | boolean | 布尔型参数 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

role.handle:set_save_data_bool_value(1, true)
```

---

## set_save_data_str_value

method in Role

- 描述

    设置字符串型参数到玩家存档栏位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | index | integer | 玩家存档栏位 |
    | value | string | 字符串型参数 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

role.handle:set_save_data_str_value(1, "value")
```

---

## set_save_data_table_value

method in Role

- 描述

    设置表型参数到玩家存档栏位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | index | integer | 玩家存档栏位 |
    | value | py.Table | 表型参数 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)
local tbl = {}

role.handle:set_save_data_table_value(1, tbl)
```

---

## set_save_table_key_value

method in Role

- 描述

    set_save_table_key_value

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | save_slot | integer | 玩家存档栏位 |
    | key1 | string | key1 |
    | value | py.Actor | value |
    | key2 | string | key2 |
    | key3 | string | key3 |
    | value_convert_func | string | value_convert_func |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

role.handle:set_save_table_key_value(1, "key1", actor, "key2", "key3", "value_convert_func")
```

---

## add_save_table_key_value

method in Role

- 描述

    add_save_table_key_value

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | save_slot | integer | 玩家存档栏位 |
    | key1 | string | key1 |
    | value | py.Actor | value |
    | key2 | string | key2 |
    | key3 | string | key3 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

role.handle:add_save_table_key_value(1, "key1", actor, "key2", "key3")
```

---

## multiply_save_table_key_value

method in Role

- 描述

    multiply_save_table_key_value

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | save_slot | integer | 玩家存档栏位 |
    | key1 | string | key1 |
    | value | py.Actor | value |
    | key2 | string | key2 |
    | key3 | string | key3 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

role.handle:multiply_save_table_key_value(1, "key1", actor, "key2", "key3")
```

---

## remove_save_table_key_value

method in Role

- 描述

    remove_save_table_key_value

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | save_slot | integer | 玩家存档栏位 |
    | key1 | string | key1 |
    | key2 | string | key2 |
    | key3 | string | key3 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

role.handle:remove_save_table_key_value(1, "key1", "key2", "key3")
```

---

## get_save_table_key_value

method in Role

- 描述

    get_save_table_key_value

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | save_slot | integer | 玩家存档栏位 |
    | key1 | string | key1 |
    | key2 | string | key2 |
    | key3 | string | key3 |
    | default_value | py.Actor | value |
    | value_convert_func | string | key2 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

role.handle:get_save_table_key_value(1, "key1", "key2", "key3", actor, "value_convert_func")
```

---

## upload_save_data

method in Role

- 描述

    上传玩家存档数据

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | use_proxy? | boolean | 进行代理上传 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

role.handle:upload_save_data(true)
```

---

## add_global_map_archive_data

method in Role

- 描述

    增加当前地图的指定key的存档值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 全局存档key值 |
    | value | integer | 增加的数值 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

role.handle:add_global_map_archive_data("key", 1)
```

---

## get_player_rank_num

method in Role

- 描述

    获取玩家指定的全局存档key值对应排行榜的排名

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | rank_key | string | 全局存档key值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 整型 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:get_player_rank_num("rank_key")
```

---

## get_player_archive_rank_num

method in Role

- 描述

    获取玩家指定的个人存档栏位对应排行榜的排名

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | archive_key | integer | 玩家存档栏位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 整型 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:get_player_archive_rank_num(1)
```

---

## download_save_data

method in Role

- 描述

    下载玩家存档数据

- 参数

    无

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

role.handle:download_save_data()
```

---

## reset_download_save_data_callback

method in Role

- 描述

    重置下载档案数据回调

- 参数

    无

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

role.handle:reset_download_save_data_callback()
```

---

## get_save_data_int_value

method in Role

- 描述

    读取整数型玩家存档数据

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | index | integer | 玩家存档栏位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 整型 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:get_save_data_int_value(1)
```

---

## get_save_data_fixed_value

method in Role

- 描述

    读取实数型玩家存档数据

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | index | integer | 玩家存档栏位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 定点数 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:get_save_data_fixed_value(1)
```

---

## get_save_data_bool_value

method in Role

- 描述

    读取布尔型玩家存档数据

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | index | integer | 玩家存档栏位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 布尔值 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:get_save_data_bool_value(1)
```

---

## get_save_data_str_value

method in Role

- 描述

    读取字符串型玩家存档数据

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | index | integer | 玩家存档栏位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string? | 字符串 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:get_save_data_str_value(1)
```

---

## get_save_data_table_value

method in Role

- 描述

    读取表型玩家存档数据

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | index | integer | 玩家存档栏位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Table? | 表 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:get_save_data_table_value(1)
```

---

## get_encry_uuid

method in Role

- 描述

    获取玩家加密uuid

- 参数

    无

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

role.handle:get_encry_uuid()
```

---

## api_use_store_item

method in Role

- 描述

    玩家使用收费道具

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | cnt | integer | 数量 |
    | no | py.StoreKey | 收费道具KEY |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)
local store_key = 134274569

role.handle:api_use_store_item(1, store_key)
```

---

## get_store_item_cnt

method in Role

- 描述

    获取玩家收费道具数量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | no | py.StoreKey | 收费道具key |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 收费道具数量 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)
local store_key = 134274569

local result = role.handle:get_store_item_cnt(store_key)
```

---

## get_visibility_of_unit

method in Role

- 描述

    玩家是否拥有单位的可见性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 是否可见 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = role.handle:get_visibility_of_unit(unit.handle)
```

---

## api_change_tech_level

method in Role

- 描述

    修改玩家科技等级

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_no | py.TechKey | 科技编号 |
    | delta_lv | integer | 变化等级 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)
local tech_key = 134274569

role.handle:api_change_tech_level(tech_key, 1)
```

---

## api_set_tech_level

method in Role

- 描述

    修改玩家科技等级

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_no | py.TechKey | 科技编号 |
    | lv | integer | 等级 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)
local tech_key = 134274569

role.handle:api_set_tech_level(tech_key, 1)
```

---

## api_get_tech_level

method in Role

- 描述

    获取玩家科技等级

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_no | py.TechKey | 科技编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 科技等级 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)
local tech_key = 134274569

local result = role.handle:api_get_tech_level(tech_key)
```

---

## is_point_visible_to_player

method in Role

- 描述

    点对于玩家是否可见

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.FPoint | 点 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 布尔值 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)
local fpoint = GameAPI.get_point_by_res_id(1)

local result = role.handle:is_point_visible_to_player(fpoint)
```

---

## is_point_in_fog

method in Role

- 描述

    点是否在迷雾中

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.FPoint | 点 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 布尔值 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)
local fpoint = GameAPI.get_point_by_res_id(1)

local result = role.handle:is_point_in_fog(fpoint)
```

---

## is_point_in_shadow

method in Role

- 描述

    点是否在黑色阴影中

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.FPoint | 点 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 布尔值 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)
local fpoint = GameAPI.get_point_by_res_id(1)

local result = role.handle:is_point_in_shadow(fpoint)
```

---

## get_role_status

method in Role

- 描述

    获取玩家状态

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleStatus? | 玩家状态 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:get_role_status()
```

---

## set_role_hostility

method in Role

- 描述

    设置玩家是否是敌对关系

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | is_enemy | boolean | 布尔变量 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)
local player = y3.player.get_by_id(1)

role.handle:set_role_hostility(player.handle, true)
```

---

## players_is_alliance

method in Role

- 描述

    玩家是否是同盟关系

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 返回值 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)
local player = y3.player.get_by_id(1)

local result = role.handle:players_is_alliance(player.handle)
```

---

## players_is_enemy

method in Role

- 描述

    玩家是否是敌对关系

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 返回值 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)
local player = y3.player.get_by_id(1)

local result = role.handle:players_is_enemy(player.handle)
```

---

## share_source_player_vision_to_target

method in Role

- 描述

    原始玩家对目标玩家开放视野

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role_2 | py.Role | 玩家 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 返回值 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)
local player = y3.player.get_by_id(1)

local result = role.handle:share_source_player_vision_to_target(player.handle)
```

---

## close_source_player_vision_to_target

method in Role

- 描述

    原始玩家对目标玩家关闭视野

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role_2 | py.Role | 玩家 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 返回值 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)
local player = y3.player.get_by_id(1)

local result = role.handle:close_source_player_vision_to_target(player.handle)
```

---

## share_source_unit_vision_to_target

method in Role

- 描述

    原始单位对目标玩家开放视野

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 返回值 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = role.handle:share_source_unit_vision_to_target(unit.handle)
```

---

## close_source_unit_vision_to_target

method in Role

- 描述

    原始单位对目标玩家关闭视野

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 单位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 返回值 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = role.handle:close_source_unit_vision_to_target(unit.handle)
```

---

## role_select_unit

method in Role

- 描述

    选中单位或单位组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_or_unit_groupd | py.DynamicTypeMeta | 单位或单位组 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)
local dynamic_type = GameAPI.get_function_return_value("func_id", y3.player.get_by_id(1):get_all_units()[1].handle, pydict(), {}, 1)

role.handle:role_select_unit(dynamic_type)
```

---

## set_role_mouse_left_click

method in Role

- 描述

    开/关玩家鼠标的点选

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | boolean | 开/关 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

role.handle:set_role_mouse_left_click(true)
```

---

## set_role_mouse_move_select

method in Role

- 描述

    开/关玩家的鼠标的框选

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | boolean | 开/关 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

role.handle:set_role_mouse_move_select(true)
```

---

## set_role_mouse_wheel

method in Role

- 描述

    开/关玩家的鼠标滚轮

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | boolean | 开/关 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

role.handle:set_role_mouse_wheel(true)
```

---

## set_role_vignetting_enable

method in Role

- 描述

    设置玩家暗角开关

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | boolean | 暗角开关 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

role.handle:set_role_vignetting_enable(true)
```

---

## set_role_vignetting_size

method in Role

- 描述

    设置玩家暗角大小

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | number | 暗角大小 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

role.handle:set_role_vignetting_size(1.0)
```

---

## set_role_vignetting_breath_rate

method in Role

- 描述

    设置玩家暗角呼吸周期

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | number | 呼吸周期 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

role.handle:set_role_vignetting_breath_rate(1.0)
```

---

## set_role_vignetting_change_range

method in Role

- 描述

    设置玩家暗角变化幅度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | number | 变化幅度 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

role.handle:set_role_vignetting_change_range(1.0)
```

---

## set_role_vignetting_color

method in Role

- 描述

    设置玩家暗角颜色

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | r | number | R |
    | g | number | G |
    | b | number | B |
    | interval? | number | Interval |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

role.handle:set_role_vignetting_color(1.0, 1.0, 1.0, 1.0)
```

---

## api_set_role_editable_game_func

method in Role

- 描述

    设置玩家的基础操作快捷键（过滤掉禁止修改的）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | game_func_id | py.EditableGameFunc | 可编辑操作 |
    | normal_key | py.NormalKey | 功能键 |
    | record_key | py.RecordKey | 辅助键 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

role.handle:api_set_role_editable_game_func(1, "normal_key", "record_key")
```

---

## api_set_role_all_game_func_enable

method in Role

- 描述

    设置玩家的基础操作开关（包含所有基础操作）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | game_func_id | py.AllGameFunc | 所有操作 |
    | is_enable | boolean | 开/关 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

role.handle:api_set_role_all_game_func_enable(1, true)
```

---

## api_is_conf_of_editable_game_func

method in Role

- 描述

    基础操作响应的快捷键是否已被占用（过滤掉禁止修改的）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | normal_key | py.NormalKey | 功能键 |
    | record_key | py.RecordKey | 辅助键 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 是否 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:api_is_conf_of_editable_game_func("normal_key", "record_key")
```

---

## api_get_editable_game_func_of_shortcut

method in Role

- 描述

    获取玩家响应键盘按键的基础操作（过滤掉禁止修改的）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | normal_key | py.NormalKey | 功能键 |
    | record_key | py.RecordKey | 辅助 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.EditableGameFunc? | 可修改基础操作 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:api_get_editable_game_func_of_shortcut("normal_key", "record_key")
```

---

## set_bool_hit_point_data

method in Role

- 描述

    设置玩家布尔埋点数据

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | integer | 布尔key |
    | value | boolean | 布尔值 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

role.handle:set_bool_hit_point_data(1, true)
```

---

## set_int_hit_point_data

method in Role

- 描述

    设置玩家整型埋点数据

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | integer | 整型key |
    | value | integer | 整数 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

role.handle:set_int_hit_point_data(1, 1)
```

---

## api_set_follow_distance

method in Role

- 描述

    设置跟随距离

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | follow_distance | py.Fixed | 跟随距离 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

role.handle:api_set_follow_distance(Fix32(1))
```

---

## api_set_role_cursor

method in Role

- 描述

    设置玩家的鼠标样式

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | cur_state_key | py.CursorState | 鼠标状态 |
    | cur_key | py.CursorKey | 鼠标key |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

role.handle:api_set_role_cursor("cur_state_key", 1)
```

---

## api_set_role_skill_indicator

method in Role

- 描述

    设置玩家的技能指示器特效

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | skill_indicator_key | integer | 指示器特效枚举 |
    | effect_key | py.SfxKey | 特效key |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)
local sfx_key = 134274569

role.handle:api_set_role_skill_indicator(1, sfx_key)
```

---

## api_get_role_color

method in Role

- 描述

    获取玩家颜色

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string? | 颜色 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:api_get_role_color()
```

---

## api_is_honor_vip

method in Role

- 描述

    玩家是否为平台荣耀会员

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 是否是会员 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:api_is_honor_vip()
```

---

## api_is_cur_map_author

method in Role

- 描述

    玩家是否为当前作者

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 是否是作者 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:api_is_cur_map_author()
```

---

## api_get_equip_deco_id

method in Role

- 描述

    获取玩家装备装饰类型的ID

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | plat_deco_type | py.PlatformDecoType | 平台装饰类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 装饰ID |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:api_get_equip_deco_id(1)
```

---

## api_get_map_level

method in Role

- 描述

    获取玩家在本地图的等级

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 地图等级 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:api_get_map_level()
```

---

## api_get_played_times

method in Role

- 描述

    获取玩家在本地图的累计局数

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 局数 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:api_get_played_times()
```

---

## api_get_map_level_rank

method in Role

- 描述

    玩家在本地图的平台等级排名

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 排名 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:api_get_map_level_rank()
```

---

## api_get_sign_in_days_of_platform

method in Role

- 描述

    玩家签到天数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | signin_type | py.PlatformSigninType | 签到天数类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 签到天数 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:api_get_sign_in_days_of_platform(1)
```

---

## api_get_community_value

method in Role

- 描述

    玩家在社区的互动

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | community_type | py.PlatformCommunityType | 平台社区类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 个数 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:api_get_community_value(1)
```

---

## api_is_returning_player

method in Role

- 描述

    玩家是否是当前地图的回流用户

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 是否回流用户 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:api_is_returning_player()
```

---

## api_is_bookmark_current_map

method in Role

- 描述

    玩家是否收藏当前地图

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 是否收藏当前地图 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:api_is_bookmark_current_map()
```

---

## api_get_ladder_rank_points

method in Role

- 描述

    获取玩家当前赛季天梯的排位积分

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ladder_key | string | 天梯key |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 积分 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:api_get_ladder_rank_points("ladder_key")
```

---

## api_get_role_total_consume

method in Role

- 描述

    获取玩家该地图累计充值

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 累计充值 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:api_get_role_total_consume()
```

---

## api_get_role_is_donated

method in Role

- 描述

    获取玩家是否打赏该地图

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 是否打赏该地图 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:api_get_role_is_donated()
```

---

## set_archive_group_value

method in Role

- 描述

    设置存档组数据

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 玩家存档组key |
    | value | string | 字符串值 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

role.handle:set_archive_group_value("key", "value")
```

---

## get_archive_group_value

method in Role

- 描述

    读取字符串型玩家存档组数据

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 玩家存档组key |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string? | 字符串 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:get_archive_group_value("key")
```

---

## copy_save_data_table_value

method in Role

- 描述

    复制表型存档到玩家存档栏位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | src_index | integer | 源玩家存档栏位 |
    | dst_index | integer | 目标玩家存档栏位 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

role.handle:copy_save_data_table_value(1, 1)
```

---

## force_upload_save_data

method in Role

- 描述

    强制上传玩家非实时存档

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | use_proxy? | boolean | 进行代理上传 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

role.handle:force_upload_save_data(true)
```

---

## get_store_item_expired_time

method in Role

- 描述

    获取平台道具到期时间戳

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | no | py.StoreKey | 收费道具key |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 收费道具数量 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)
local store_key = 134274569

local result = role.handle:get_store_item_expired_time(store_key)
```

---

## set_role_vignetting_color_hex

method in Role

- 描述

    设置玩家暗角颜色(HEX)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | color | string | hex |
    | interval? | number | Interval |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

role.handle:set_role_vignetting_color_hex("color", 1.0)
```

---

## upload_player_game_rank

method in Role

- 描述

    上报玩家排名

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | rank | integer | 本局游戏排名 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

role.handle:upload_player_game_rank(1)
```

---

## api_get_role_select_units

method in Role

- 描述

    获取玩家当前选中单位组

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitGroup? | 单位组 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:api_get_role_select_units()
```

---

## update_player_save_rank

method in Role

- 描述

    更新玩家存档排行榜

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | save_index | integer | 玩家存档栏位 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

role.handle:update_player_save_rank(1)
```

---

## api_get_current_season_id

method in Role

- 描述

    获取玩家当前赛季天梯编号

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ladder_key | string | 天梯key |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 赛季编号 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:api_get_current_season_id("ladder_key")
```

---

## api_get_current_season_standing

method in Role

- 描述

    获取玩家当前赛季天梯排名

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ladder_key | string | 天梯key |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 当前赛季排名 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:api_get_current_season_standing("ladder_key")
```

---

## api_get_current_season_standing_number

method in Role

- 描述

    获取玩家当前赛天梯排名次数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ladder_key | string | 天梯key |
    | rank_number | integer | 第几名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 排名次数 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:api_get_current_season_standing_number("ladder_key", 1)
```

---

## api_get_number_of_expeditions

method in Role

- 描述

    获取玩家当前地图探险次数

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 探险次数 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:api_get_number_of_expeditions()
```

---

## api_get_time_of_expeditions

method in Role

- 描述

    获取玩家当前地图探险时长

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 探险时长 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:api_get_time_of_expeditions()
```

---

## api_get_role_store_params

method in Role

- 描述

    获取玩家商城登录用token

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string? | 商城token |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:api_get_role_store_params()
```

---

## api_get_role_achieve_point

method in Role

- 描述

    获取玩家当前地图的成就点数

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 成就点数 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:api_get_role_achieve_point()
```

---

## api_get_role_achieve_unlock

method in Role

- 描述

    获取玩家当前地图成就是否解锁

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | achieve_id | string | 成就ID |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 是否解锁 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:api_get_role_achieve_unlock("achieve_id")
```

---

## api_get_number_of_lottery

method in Role

- 描述

    获取玩家当前地图指定宝箱的抽取次数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | lottery_number | integer | 地图宝箱编号 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 宝箱抽取次数 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:api_get_number_of_lottery(1)
```

---

## api_get_number_of_all_lottery

method in Role

- 描述

    获取玩家当前地图抽取宝箱的总次数

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 宝箱总次数 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:api_get_number_of_all_lottery()
```

---

## api_get_guild_name

method in Role

- 描述

    获取玩家所在公会名

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string? | 公会名 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:api_get_guild_name()
```

---

## api_get_guild_announcement

method in Role

- 描述

    获取玩家所在公会公告

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string? | 公会公告 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:api_get_guild_announcement()
```

---

## api_get_guild_member_count

method in Role

- 描述

    获取玩家所在公会人数

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 公会人数 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:api_get_guild_member_count()
```

---

## api_get_guild_level

method in Role

- 描述

    获取玩家所在公会等级

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 公会等级 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:api_get_guild_level()
```

---

## pet_http_request

method in Role

- 描述

    宠物http请求调用

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | api | string | 请求的api方法名 |
    | is_post | boolean | api是否为post方法 |
    | body | string | 请求的body |
    | timeout? | integer | 超时时间 |
    | callback? | function | 回调函数 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

role.handle:pet_http_request("api", true, "body", 1, function() end)
```

---

## request_create_private_dungeon

method in Role

- 描述

    请求创建私有副本

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | level_id | py.Map | 关卡id |
    | game_mode | py.GameMode | 游戏模式 |
    | max_player? | integer | 最大人数 |
    | custom_param? | string | 自定义参数 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

role.handle:request_create_private_dungeon(1, 1, 1, "custom_param")
```

---

## request_join_private_dungeon

method in Role

- 描述

    请求加入私有副本

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | token | string | 房间口令 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

role.handle:request_join_private_dungeon("token")
```

---

## request_join_public_dungeon

method in Role

- 描述

    请求加入公有副本

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | level_id | py.Map | 关卡id |
    | game_mode | py.GameMode | 游戏模式 |

- 返回值

    无

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

role.handle:request_join_public_dungeon(1, 1)
```

---

## get_role_general_depot

method in Role

- 描述

    获取玩家武将信息

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Table? | 玩家武将信息 |

- 示例

```lua
-- 获取玩家对象
local role = y3.player.get_by_id(1)

local result = role.handle:get_role_general_depot()
```

---
