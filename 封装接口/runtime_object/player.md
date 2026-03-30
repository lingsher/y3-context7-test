---
sidebarDepth: 1
---
# Player (运行时对象)

# 索引

Y3 编辑器 Player 封装接口，提供高级方法操作 Player 对象。

---

| 接口 | 描述 |
| --- | --- |
| [get_by_id](#get_by_id) | 转换玩家ID为玩家 |
| [get_by_string](#get_by_string) | 根据字符串获取玩家，字符串是通过 `tostring(Player)` |
| [get_by_handle](#get_by_handle) |  |
| [get_camp](#get_camp) |  |
| [is_middle_join](#is_middle_join) | 玩家是否中途加入 |
| [is_enemy](#is_enemy) | 玩家间是否是敌对关系 |
| [set_name](#set_name) | 设置名字 |
| [set_team](#set_team) | 设置队伍ID |
| [set](#set) | 设置属性值 |
| [add](#add) | 增加属性值 |
| [get](#get) | 获取玩家属性 |
| [get_attr](#get_attr) | 获取玩家属性 |
| [set_exp_rate](#set_exp_rate) | 设置经验获得率 |
| [set_hostility](#set_hostility) | 设置敌对关系 |
| [set_strict_group_navigation](#set_strict_group_navigation) | 设置群体寻路严格模式 |
| [select_unit](#select_unit) | 选中单位/单位组 |
| [set_follow_distance](#set_follow_distance) | 设置跟随距离 |
| [set_mouse_click_selection](#set_mouse_click_selection) | 为玩家开/关鼠标点选 |
| [set_mouse_drag_selection](#set_mouse_drag_selection) | 为玩家开/关鼠标框选 |
| [set_mouse_wheel](#set_mouse_wheel) | 为玩家开/关鼠标滚轮 |
| [is_operation_key_occupied](#is_operation_key_occupied) | 玩家基础操作快捷键是否被占用 |
| [set_operation_key](#set_operation_key) | 设置玩家的基础操作快捷键（过滤掉禁止设置的） |
| [set_all_operation_key](#set_all_operation_key) | 设置玩家的基础操作开关（包含所有基础操作） |
| [get_operation_key](#get_operation_key) | 获取玩家响应键盘按键的基础操作（过滤掉禁止设置的） |
| [set_tech_level](#set_tech_level) | 设置科技等级 |
| [add_tech_level](#add_tech_level) | 增加科技等级 |
| [share_vision_with_player](#share_vision_with_player) | 对玩家开放视野 |
| [share_vision_of_unit](#share_vision_of_unit) | 获取单位的视野 |
| [upload_save_data](#upload_save_data) | 上传存档 |
| [add_global_save_data](#add_global_save_data) | 增加全局存档 |
| [use_store_item](#use_store_item) | 消耗玩家平台道具 |
| [open_platform_shop](#open_platform_shop) | 请求购买平台道具 |
| [is_visible](#is_visible) | 玩家是否可以看到某个位置 |
| [is_in_fog](#is_in_fog) | 某个位置是否处于玩家的迷雾中 |
| [is_in_shadow](#is_in_shadow) | 某个位置是否处于玩家的黑色阴影中 |
| [get_id](#get_id) | 获取玩家ID |
| [get_color](#get_color) | 获取玩家颜色 |
| [get_state](#get_state) | 获取玩家游戏状态 |
| [get_controller](#get_controller) | 获取玩家控制者类型 |
| [is_alive](#is_alive) | 是否是存活的玩家（正在游戏中的真实玩家） |
| [need_sync](#need_sync) | 是否是需要同步数据的玩家（在线、掉线（可以重连）、观看中的玩家与观看者） |
| [get_name](#get_name) | 获取玩家名字 |
| [get_exp_rate](#get_exp_rate) | 获取经验获得率 |
| [get_team_id](#get_team_id) | 获取队伍ID |
| [get_rank_num](#get_rank_num) | 获取整数存档玩家排名 |
| [get_tech_level](#get_tech_level) | 获取科技等级 |
| [get_platform_icon](#get_platform_icon) | 获取玩家平台头像 |
| [get_platform_icon_url](#get_platform_icon_url) | 获取玩家平台头像下载地址 |
| [get_platform_id](#get_platform_id) | 获取玩家平台唯一ID |
| [get_map_level](#get_map_level) | 获取玩家的此地图平台等级 |
| [get_map_level_rank](#get_map_level_rank) | 获取玩家在本地图的平台等级排名 |
| [get_played_times](#get_played_times) | 获取玩家在本地图的累计局数 |
| [get_achieve_point](#get_achieve_point) | 获取玩家当前地图的成就点数 |
| [is_achieve_unlock](#is_achieve_unlock) | 判断指定成就是否解锁 |
| [get_store_item_number](#get_store_item_number) | 玩家平台道具数量 |
| [get_store_item_end_time](#get_store_item_end_time) | 玩家平台道具到期时间戳 |
| [get_platform_level](#get_platform_level) | 获取玩家平台等级 |
| [is_in_group](#is_in_group) | 玩家在玩家组中 |
| [get_all_units](#get_all_units) | 属于某玩家的所有单位 |
| [create_unit](#create_unit) | 创建单位 |
| [kick](#kick) | 强制踢出 |
| [get_platform_model](#get_platform_model) | 获取玩家平台外观模型 |
| [get_mouse_pos](#get_mouse_pos) | 获取鼠标在游戏内的所在点。 |
| [get_mouse_ui_x_percent](#get_mouse_ui_x_percent) | 获取玩家鼠标屏幕坐标X的占比。 |
| [get_mouse_ui_y_percent](#get_mouse_ui_y_percent) | 获取玩家鼠标屏幕坐标y的占比。 |
| [get_mouse_pos_x](#get_mouse_pos_x) | 获取鼠标在屏幕上的X坐标 |
| [get_mouse_pos_y](#get_mouse_pos_y) | 获取鼠标在屏幕上的y坐标 |
| [is_key_pressed](#is_key_pressed) | 玩家的按键是否被按下 |
| [get_platform_name](#get_platform_name) | 获取玩家唯一名称 |
| [get_platform_uuid](#get_platform_uuid) | 获取玩家加密UUID |
| [display_info](#display_info) | 向玩家发送提示 |
| [get_res_icon](#get_res_icon) | 获取玩家属性的货币图标 |
| [get_res_name](#get_res_name) | 获取玩家属性名称 |
| [set_color_grading](#set_color_grading) | 设置滤镜 |
| [set_local_terrain_visible](#set_local_terrain_visible) | 显示/隐藏玩家地表纹理 |
| [enable_vignetting](#enable_vignetting) | 设置暗角开关 |
| [set_vignetting_size](#set_vignetting_size) | 设置暗角大小 |
| [set_role_vignetting_breath_rate](#set_role_vignetting_breath_rate) | 设置暗角呼吸周期 |
| [set_vignetting_change_range](#set_vignetting_change_range) | 设置暗角变化幅度 |
| [set_vignetting_color](#set_vignetting_color) | 设置暗角颜色 |
| [exit_game](#exit_game) | 退出游戏 |
| [get_res_keys](#get_res_keys) | 获取所有玩家属性的属性名 |
| [display_message](#display_message) | 对玩家显示文本消息 |
| [upload_tracking_data](#upload_tracking_data) | 上传埋点数据 |
| [get_community_value](#get_community_value) | 获取玩家在社区的互动数据 |
| [get_sign_in_days](#get_sign_in_days) | 获取玩家当前地图的签到天数 |
| [is_bookmark_current_map](#is_bookmark_current_map) | 玩家是否收藏当前地图 |
| [request_random_pool](#request_random_pool) | 请求执行随机池掉落 |
| [request_use_item](#request_use_item) | 请求使用商城道具 |
| [request_buy_mall_coin](#request_buy_mall_coin) | 请求购买商城货币 |
| [request_mall_goods_info](#request_mall_goods_info) | 获取某个玩家的商城物品信息 |
| [request_mall_purchase_goods](#request_mall_purchase_goods) | 请求购买商城道具 |
| [request_random_number](#request_random_number) | 请求生成随机数 |
| [request_open_archive](#request_open_archive) | 请求玩家的开放存档数据 |
| [update_save_rank](#update_save_rank) | 更新存档排行榜 |

---

## get_by_id

method in Player

- 描述

    转换玩家ID为玩家

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | id | integer | 玩家ID |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Player | 玩家 |

- 示例

```lua
local result = y3.player.get_by_id(1)
```

---

## get_by_string

method in Player

- 描述

    根据字符串获取玩家，字符串是通过 `tostring(Player)`

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | str | string |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Player? |  |

- 示例

```lua
local result = y3.player.get_by_string("str")
```

---

## get_by_handle

method in Player

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | py_player | py.Role |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Player |  |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = y3.player.get_by_handle(player.handle)
```

---

## get_camp

method in Player

- 描述

    

- 参数

    无

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

player:get_camp()
```

---

## is_middle_join

method in Player

- 描述

    玩家是否中途加入

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否中途加入 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = player:is_middle_join()
```

---

## is_enemy

method in Player

- 描述

    玩家间是否是敌对关系

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否是敌对关系 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = player:is_enemy(player)
```

---

## set_name

method in Player

- 描述

    设置名字

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | name | string | 名字 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

player:set_name("name")
```

---

## set_team

method in Player

- 描述

    设置队伍ID

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | id | py.Camp |  |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local camp = GameAPI.get_camp_by_camp_id(1)

player:set_team(camp)
```

---

## set

method in Player

- 描述

    设置属性值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | y3.Const.PlayerAttr \| string | 属性名 |
    | value | number | 值 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

player:set("key", 1.0)
```

---

## add

method in Player

- 描述

    增加属性值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | y3.Const.PlayerAttr \| string | 属性名 |
    | value | number | 值 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

player:add("key", 1.0)
```

---

## get

method in Player

- 描述

    获取玩家属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | y3.Const.PlayerAttr \| string | 属性名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 玩家属性 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = player:get("key")
```

---

## get_attr

method in Player

- 描述

    获取玩家属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | y3.Const.PlayerAttr \| string | 属性名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 玩家属性 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = player:get_attr("key")
```

---

## set_exp_rate

method in Player

- 描述

    设置经验获得率

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | rate | number | 经验获得率 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

player:set_exp_rate(1.0)
```

---

## set_hostility

method in Player

- 描述

    设置敌对关系

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | is_hostile | boolean | 是否敌视 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

player:set_hostility(player, true)
```

---

## set_strict_group_navigation

method in Player

- 描述

    设置群体寻路严格模式

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_strict | boolean | 是否严格 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

player:set_strict_group_navigation(true)
```

---

## select_unit

method in Player

- 描述

    选中单位/单位组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_or_group | Unit\|UnitGroup | 单位/单位组 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local unit = y3.player.get_by_id(1):get_all_units()[1]

player:select_unit(unit_or_group)
```

---

## set_follow_distance

method in Player

- 描述

    设置跟随距离

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | distance | number | 距离 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

player:set_follow_distance(1.0)
```

---

## set_mouse_click_selection

method in Player

- 描述

    为玩家开/关鼠标点选

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_enable | boolean | 是否开鼠标点选 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

player:set_mouse_click_selection(true)
```

---

## set_mouse_drag_selection

method in Player

- 描述

    为玩家开/关鼠标框选

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_enable | boolean | 是否开鼠标框选 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

player:set_mouse_drag_selection(true)
```

---

## set_mouse_wheel

method in Player

- 描述

    为玩家开/关鼠标滚轮

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_enable | boolean | 是否开鼠标滚轮 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

player:set_mouse_wheel(true)
```

---

## is_operation_key_occupied

method in Player

- 描述

    玩家基础操作快捷键是否被占用

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | py.NormalKey | 键名 |
    | assist_key | py.RecordKey | 辅助键名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否被占用 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local key = "KEY_A"
local assist_key = "KEY_NONE"

local result = player:is_operation_key_occupied(key, assist_key)
```

---

## set_operation_key

method in Player

- 描述

    设置玩家的基础操作快捷键（过滤掉禁止设置的）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | operation | py.EditableGameFunc | 可编辑操作 |
    | key | py.NormalKey | 功能按键 |
    | assist_key | py.RecordKey | 辅助按键 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local operation = 1
local key = "KEY_A"
local assist_key = "KEY_NONE"

player:set_operation_key(operation, key, assist_key)
```

---

## set_all_operation_key

method in Player

- 描述

    设置玩家的基础操作开关（包含所有基础操作）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | operation | py.AllGameFunc | 可编辑操作 |
    | is_enable | boolean | 是否开 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local operation = 1

player:set_all_operation_key(operation, true)
```

---

## get_operation_key

method in Player

- 描述

    获取玩家响应键盘按键的基础操作（过滤掉禁止设置的）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | py.NormalKey | 键名 |
    | assist_key | py.RecordKey | 键盘按键 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.EditableGameFunc | 基础操作 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local key = "KEY_A"
local assist_key = "KEY_NONE"

local result = player:get_operation_key(key, assist_key)
```

---

## set_tech_level

method in Player

- 描述

    设置科技等级

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_type | py.TechKey | 科技等级 |
    | level | integer | 等级 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local tech_key = 134274569

player:set_tech_level(tech_key, 1)
```

---

## add_tech_level

method in Player

- 描述

    增加科技等级

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_type | py.TechKey | 科技等级 |
    | level | integer | 等级 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local tech_key = 134274569

player:add_tech_level(tech_key, 1)
```

---

## share_vision_with_player

method in Player

- 描述

    对玩家开放视野

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | target_player | Player | 玩家 |
    | share | boolean |  |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

player:share_vision_with_player(player, true)
```

---

## share_vision_of_unit

method in Player

- 描述

    获取单位的视野

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 单位 |
    | share | boolean |  |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local unit = y3.player.get_by_id(1):get_all_units()[1]

player:share_vision_of_unit(unit, true)
```

---

## upload_save_data

method in Player

- 描述

    上传存档

- 参数

    无

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

player:upload_save_data()
```

---

## add_global_save_data

method in Player

- 描述

    增加全局存档

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 键 |
    | value | integer | 值 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

player:add_global_save_data("key", 1)
```

---

## use_store_item

method in Player

- 描述

    消耗玩家平台道具

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | count | integer | 个数 |
    | item_id | py.StoreKey | 平台道具id |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local store_key = 1

player:use_store_item(1, store_key)
```

---

## open_platform_shop

method in Player

- 描述

    请求购买平台道具

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | id | py.StoreKey | 平台道具id |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local store_key = 1

player:open_platform_shop(store_key)
```

---

## is_visible

method in Player

- 描述

    玩家是否可以看到某个位置

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | Point | 点 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 点对于玩家可见 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local point = y3.point(0, 0)

local result = player:is_visible(point)
```

---

## is_in_fog

method in Player

- 描述

    某个位置是否处于玩家的迷雾中

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | Point | 点 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 点在迷雾中 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local point = y3.point(0, 0)

local result = player:is_in_fog(point)
```

---

## is_in_shadow

method in Player

- 描述

    某个位置是否处于玩家的黑色阴影中

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | Point | 点 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 点在黑色阴影中 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local point = y3.point(0, 0)

local result = player:is_in_shadow(point)
```

---

## get_id

method in Player

- 描述

    获取玩家ID

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 玩家ID |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = player:get_id()
```

---

## get_color

method in Player

- 描述

    获取玩家颜色

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string |  |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = player:get_color()
```

---

## get_state

method in Player

- 描述

    获取玩家游戏状态

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | y3.Const.RoleStatus | 玩家游戏状态 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = player:get_state()
```

---

## get_controller

method in Player

- 描述

    获取玩家控制者类型

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | y3.Const.RoleType | 玩家控制者类型 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = player:get_controller()
```

---

## is_alive

method in Player

- 描述

    是否是存活的玩家（正在游戏中的真实玩家）

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean |  |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = player:is_alive()
```

---

## need_sync

method in Player

- 描述

    是否是需要同步数据的玩家（在线、掉线（可以重连）、观看中的玩家与观看者）

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean |  |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = player:need_sync()
```

---

## get_name

method in Player

- 描述

    获取玩家名字

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 玩家名字 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = player:get_name()
```

---

## get_exp_rate

method in Player

- 描述

    获取经验获得率

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 经验获得率 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = player:get_exp_rate()
```

---

## get_team_id

method in Player

- 描述

    获取队伍ID

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 队伍ID |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = player:get_team_id()
```

---

## get_rank_num

method in Player

- 描述

    获取整数存档玩家排名

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | integer | 存档key |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 整数存档玩家排名 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = player:get_rank_num(1)
```

---

## get_tech_level

method in Player

- 描述

    获取科技等级

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_id | py.TechKey | 科技id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 科技等级 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local tech_key = 134274569

local result = player:get_tech_level(tech_key)
```

---

## get_platform_icon

method in Player

- 描述

    获取玩家平台头像

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 平台头像 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = player:get_platform_icon()
```

---

## get_platform_icon_url

method in Player

- 描述

    获取玩家平台头像下载地址

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 平台头像下载地址 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = player:get_platform_icon_url()
```

---

## get_platform_id

method in Player

- 描述

    获取玩家平台唯一ID

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 平台唯一ID |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = player:get_platform_id()
```

---

## get_map_level

method in Player

- 描述

    获取玩家的此地图平台等级

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer |  |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = player:get_map_level()
```

---

## get_map_level_rank

method in Player

- 描述

    获取玩家在本地图的平台等级排名

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer |  |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = player:get_map_level_rank()
```

---

## get_played_times

method in Player

- 描述

    获取玩家在本地图的累计局数

- 参数

    无

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

player:get_played_times()
```

---

## get_achieve_point

method in Player

- 描述

    获取玩家当前地图的成就点数

- 参数

    无

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

player:get_achieve_point()
```

---

## is_achieve_unlock

method in Player

- 描述

    判断指定成就是否解锁

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | id | string |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean |  |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = player:is_achieve_unlock("id")
```

---

## get_store_item_number

method in Player

- 描述

    玩家平台道具数量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | id | py.StoreKey | 平台道具id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 平台道具数量 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local store_key = 1

local result = player:get_store_item_number(store_key)
```

---

## get_store_item_end_time

method in Player

- 描述

    玩家平台道具到期时间戳

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | id | py.StoreKey | 平台道具id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 平台道具到期时间戳 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local store_key = 1

local result = player:get_store_item_end_time(store_key)
```

---

## get_platform_level

method in Player

- 描述

    获取玩家平台等级

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 平台等级 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = player:get_platform_level()
```

---

## is_in_group

method in Player

- 描述

    玩家在玩家组中

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player_group | PlayerGroup | 玩家组 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 玩家在玩家组中 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local player_group = y3.player_group.create()

local result = player:is_in_group(player_group)
```

---

## get_all_units

method in Player

- 描述

    属于某玩家的所有单位

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | UnitGroup | 单位组 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = player:get_all_units()
```

---

## create_unit

method in Player

- 描述

    创建单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_id | py.UnitKey | 单位类型 |
    | point? | Point | 单位 |
    | facing? | number | 朝向 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Unit |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local unit_key = 134274569

local result = player:create_unit(unit_key, point, 1.0)
```

---

## kick

method in Player

- 描述

    强制踢出

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | reason | string | 踢出原因 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

player:kick("reason")
```

---

## get_platform_model

method in Player

- 描述

    获取玩家平台外观模型

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModelKey | 模型id |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = player:get_platform_model()
```

---

## get_mouse_pos

method in Player

- 描述

    获取鼠标在游戏内的所在点。

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Point | 点 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = player:get_mouse_pos()
```

---

## get_mouse_ui_x_percent

method in Player

- 描述

    获取玩家鼠标屏幕坐标X的占比。

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | X的占比 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = player:get_mouse_ui_x_percent()
```

---

## get_mouse_ui_y_percent

method in Player

- 描述

    获取玩家鼠标屏幕坐标y的占比。

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | Y的占比 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = player:get_mouse_ui_y_percent()
```

---

## get_mouse_pos_x

method in Player

- 描述

    获取鼠标在屏幕上的X坐标

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | X坐标 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = player:get_mouse_pos_x()
```

---

## get_mouse_pos_y

method in Player

- 描述

    获取鼠标在屏幕上的y坐标

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | Y坐标 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = player:get_mouse_pos_y()
```

---

## is_key_pressed

method in Player

- 描述

    玩家的按键是否被按下

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | y3.Const.KeyboardKey \| y3.Const.MouseKey \| integer | 按键 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean |  |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = player:is_key_pressed(134274569)
```

---

## get_platform_name

method in Player

- 描述

    获取玩家唯一名称

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 属性名称 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = player:get_platform_name()
```

---

## get_platform_uuid

method in Player

- 描述

    获取玩家加密UUID

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string |  |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = player:get_platform_uuid()
```

---

## display_info

method in Player

- 描述

    向玩家发送提示

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | msg | string | 消息 |
    | localize? | boolean | 是否支持语言环境 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

player:display_info("msg", true)
```

---

## get_res_icon

method in Player

- 描述

    获取玩家属性的货币图标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | py.RoleResKey | 属性名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 图标id |

- 示例

```lua
local role_res_key = "res_key"

local result = y3.player.get_res_icon(role_res_key)
```

---

## get_res_name

method in Player

- 描述

    获取玩家属性名称

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | py.RoleResKey | 属性名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 属性名称 |

- 示例

```lua
local role_res_key = "res_key"

local result = y3.player.get_res_name(role_res_key)
```

---

## set_color_grading

method in Player

- 描述

    设置滤镜

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | integer | 滤镜 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

player:set_color_grading(1)
```

---

## set_local_terrain_visible

method in Player

- 描述

    显示/隐藏玩家地表纹理

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_visible | boolean | 显示/隐藏 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

player:set_local_terrain_visible(true)
```

---

## enable_vignetting

method in Player

- 描述

    设置暗角开关

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | is_enable | boolean | 开关 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

y3.player.enable_vignetting(player, true)
```

---

## set_vignetting_size

method in Player

- 描述

    设置暗角大小

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | size | number | 大小 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

player:set_vignetting_size(1.0)
```

---

## set_role_vignetting_breath_rate

method in Player

- 描述

    设置暗角呼吸周期

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | circle_time | number | 呼吸周期 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

player:set_role_vignetting_breath_rate(1.0)
```

---

## set_vignetting_change_range

method in Player

- 描述

    设置暗角变化幅度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | range | number | 幅度 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

player:set_vignetting_change_range(1.0)
```

---

## set_vignetting_color

method in Player

- 描述

    设置暗角颜色

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | red | number | 颜色r |
    | green | number | 颜色g |
    | blue | number | 颜色b |
    | time | number | 过渡时间 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

player:set_vignetting_color(1.0, 1.0, 1.0, 1.0)
```

---

## exit_game

method in Player

- 描述

    退出游戏

- 参数

    无

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

player:exit_game()
```

---

## get_res_keys

method in Player

- 描述

    获取所有玩家属性的属性名

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | only_coin | boolean | 只获取货币类型的玩家属性 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleResKey[] |  |

- 示例

```lua
local result = y3.player.get_res_keys(true)
```

---

## display_message

method in Player

- 描述

    对玩家显示文本消息

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | message | string | 消息 |
    | localize? | boolean | 是否支持语言环境 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

player:display_message("message", true)
```

---

## upload_tracking_data

method in Player

- 描述

    上传埋点数据

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string |  |
    | cnt | integer |  |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

player:upload_tracking_data("key", 1)
```

---

## get_community_value

method in Player

- 描述

    获取玩家在社区的互动数据

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | community_type | y3.Const.PlatFormRoleCommunityType |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local community_type = '发帖累计获赞'

local result = player:get_community_value(community_type)
```

---

## get_sign_in_days

method in Player

- 描述

    获取玩家当前地图的签到天数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | sign_type? | y3.Const.SignInDaysType |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer |  |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = player:get_sign_in_days()
```

---

## is_bookmark_current_map

method in Player

- 描述

    玩家是否收藏当前地图

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean |  |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = player:is_bookmark_current_map()
```

---

## request_random_pool

method in Player

- 描述

    请求执行随机池掉落

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | id | integer | 随机池的编号 |
    | callback | fun(code: | 0|1|2|999, result: { [integer]: integer }) # 执行完毕后的回调函数 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

player:request_random_pool(1, function() end)
```

---

## request_use_item

method in Player

- 描述

    请求使用商城道具

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | count | integer | 使用数量 |
    | item_id | py.StoreKey | 商城道具id |
    | callback | fun(suc: | boolean) # 执行完毕后的回调函数 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local store_key = 1

player:request_use_item(1, store_key, function() end)
```

---

## request_buy_mall_coin

method in Player

- 描述

    请求购买商城货币

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | goods_id | string |  |
    | callback? | fun(suc: | boolean, sn?: string, error_code?: integer) |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

player:request_buy_mall_coin("goods_id")
```

---

## request_mall_goods_info

method in Player

- 描述

    获取某个玩家的商城物品信息

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | goods_id | string |  |
    | callback | fun(info: | MallGoodsInfo) |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

player:request_mall_goods_info("goods_id", function() end)
```

---

## request_mall_purchase_goods

method in Player

- 描述

    请求购买商城道具

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | count | integer | 数量 |
    | goods_id | integer | 商城道具id |
    | callback? | fun(suc: | boolean, error_code: integer) # 执行完毕后的回调函数 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

player:request_mall_purchase_goods(1, 1)
```

---

## request_random_number

method in Player

- 描述

    请求生成随机数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | group_id | integer | 随机只读存档组id |
    | key | string | 随机数的key |
    | callback | fun(value: | integer) # 执行完毕后的回调函数 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

player:request_random_number(1, "key", function() end)
```

---

## request_open_archive

method in Player

- 描述

    请求玩家的开放存档数据

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | callback | fun(archive: | any) # 执行完毕后的回调函数 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

player:request_open_archive(function() end)
```

---

## update_save_rank

method in Player

- 描述

    更新存档排行榜

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | save_index | integer | 存档栏位 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

player:update_save_rank(1)
```

---
