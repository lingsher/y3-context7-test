---
sidebarDepth: 1
---
# Steam (Game)

# 索引

Y3 编辑器 Steam 游戏接口，提供游戏相关功能。

---

| 接口 | 描述 |
| --- | --- |
| [get_team_id](#get_team_id) | 【异步】获取本地玩家在组队系统中的队伍id。如果不在队伍中则返回 `0`。 |
| [get_player_aid](#get_player_aid) | 【异步】获取本地玩家的玩家aid。 |
| [get_avatar_url](#get_avatar_url) | 【异步】获取本地玩家的头像资源url |
| [start_match](#start_match) | 【异步】请求开始匹配 |
| [cancel_match](#cancel_match) | 【异步】请求取消匹配 |
| [get_team_state](#get_team_state) | 【异步】获取当前队伍的状态 |
| [get_player_state](#get_player_state) | 【异步】获取本地玩家的状态 |
| [get_nickname](#get_nickname) | 【异步】获取本地玩家的昵称 |
| [get_player_store_items](#get_player_store_items) | 获取玩家的商店物品 |
| [set_global_archive_data](#set_global_archive_data) | 【异步】设置全局存档值 |
| [add_global_archive_data](#add_global_archive_data) | 【异步】增加全局存档值 |
| [request_friends](#request_friends) | 【异步】请求自己的好友列表 |
| [request_add_friend](#request_add_friend) | 【异步】请求添加好友 |
| [request_delete_friend](#request_delete_friend) | 【异步】请求删除好友 |
| [reply_friend_add](#reply_friend_add) | 【异步】回复好友请求 |
| [request_start_game](#request_start_game) | 【异步】请求开始游戏（不匹配），只有队长可以调用 |
| [request_join_team](#request_join_team) | 【异步】请求加入队伍 |
| [request_join_team_by_name](#request_join_team_by_name) | 【异步】请求加入队伍 |
| [request_invite_join_team](#request_invite_join_team) | 【异步】邀请玩家加入队伍 |
| [reply_team_invite](#reply_team_invite) | 【异步】回复队伍邀请 |
| [request_quit_team](#request_quit_team) | 【异步】请求退出队伍 |
| [request_team_info](#request_team_info) | 【异步】请求指定玩家的队伍信息 |
| [request_transfer_captain](#request_transfer_captain) | 【异步】转交队长，只有队长可以调用 |
| [request_kick_member](#request_kick_member) | 【异步】请求从队伍中踢出玩家，只有队长可以调用 |
| [request_aid_by_nickname](#request_aid_by_nickname) | 【异步】根据玩家昵称查询玩家的aid |
| [request_create_team](#request_create_team) | 【异步】请求创建队伍 |
| [request_start_match](#request_start_match) | 【异步】请求开始匹配 |
| [request_cancel_match](#request_cancel_match) | 【异步】请求取消匹配 |
| [request_global_archive_datas](#request_global_archive_datas) | 【异步】请求全局存档数据 |
| [request_icon](#request_icon) | 【异步】请求头像的文件路径 |
| [request_roll_settle_ladder_score](#request_roll_settle_ladder_score) | 【异步】请求结算天梯分 |
| [request_create_room](#request_create_room) | 【异步】请求创建房间 |
| [request_room_list](#request_room_list) | 【异步】请求房间列表 |
| [request_join_room](#request_join_room) | 【异步】请求加入房间 |
| [request_room_info](#request_room_info) | 【异步】请求指定用户所在的房间信息 |
| [request_room_start_game](#request_room_start_game) | 【异步】请求房间开始游戏 |
| [request_invite_join_room](#request_invite_join_room) | 【异步】邀请玩家加入房间 |
| [reply_accpet_room_invite](#reply_accpet_room_invite) | 【异步】接受房间邀请 |
| [request_change_room_slot](#request_change_room_slot) | 【异步】请求交换房间槽位 |
| [request_change_owner](#request_change_owner) | 【异步】请求将房主转交给其他用户 |
| [request_exit_room](#request_exit_room) | 【异步】请求退出自己所在的房间 |
| [request_kick_from_room](#request_kick_from_room) | 【异步】请求从房间中踢出用户 |
| [request_change_slot_state](#request_change_slot_state) | 【异步】请求修改房间中某个槽位的状态 |
| [request_change_room_password](#request_change_room_password) | 【异步】请求修改房间密码 |
| [request_change_room_name](#request_change_room_name) | 【异步】请求修改房间名字 |
| [get_steam_currency](#get_steam_currency) | 【异步】获取本地玩家在steam上使用的币种 |
| [get_steam_goods_price](#get_steam_goods_price) | 【异步】获取指定steam商品在本地玩家当前币种下的价格 |

---

## get_team_id

method in Steam

- 描述

    【异步】获取本地玩家在组队系统中的队伍id。如果不在队伍中则返回 `0`。

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer |  |

- 示例

```lua
local result = y3.steam.get_team_id()
```

---

## get_player_aid

method in Steam

- 描述

    【异步】获取本地玩家的玩家aid。

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer |  |

- 示例

```lua
local result = y3.steam.get_player_aid()
```

---

## get_avatar_url

method in Steam

- 描述

    【异步】获取本地玩家的头像资源url

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string |  |

- 示例

```lua
local result = y3.steam.get_avatar_url()
```

---

## start_match

method in Steam

- 描述

    【异步】请求开始匹配

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | score | integer | 匹配分数 |
    | level_id | string | 目标地图id |
    | game_mode? | integer | 目标地图模式 |

- 返回值

    无

- 示例

```lua
y3.steam.start_match(1, "level_id", 1)
```

---

## cancel_match

method in Steam

- 描述

    【异步】请求取消匹配

- 参数

    无

- 返回值

    无

- 示例

```lua
y3.steam.cancel_match()
```

---

## get_team_state

method in Steam

- 描述

    【异步】获取当前队伍的状态

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Steam.TeamState |  |

- 示例

```lua
local result = y3.steam.get_team_state()
```

---

## get_player_state

method in Steam

- 描述

    【异步】获取本地玩家的状态

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | y3.Const.SteamOnlineState |  |

- 示例

```lua
local result = y3.steam.get_player_state()
```

---

## get_nickname

method in Steam

- 描述

    【异步】获取本地玩家的昵称

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string |  |

- 示例

```lua
local result = y3.steam.get_nickname()
```

---

## get_player_store_items

method in Steam

- 描述

    获取玩家的商店物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | { |  |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = y3.steam.get_player_store_items(player)
```

---

## set_global_archive_data

method in Steam

- 描述

    【异步】设置全局存档值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string |  |
    | value | string\|integer |  |

- 返回值

    无

- 示例

```lua
y3.steam.set_global_archive_data("key", "value")
```

---

## add_global_archive_data

method in Steam

- 描述

    【异步】增加全局存档值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string |  |
    | value | integer |  |

- 返回值

    无

- 示例

```lua
y3.steam.add_global_archive_data("key", 1)
```

---

## request_friends

method in Steam

- 描述

    【异步】请求自己的好友列表

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | callback | fun(friends: | Steam.FriendState[]) |

- 返回值

    无

- 示例

```lua
y3.steam.request_friends(function() end)
```

---

## request_add_friend

method in Steam

- 描述

    【异步】请求添加好友

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | aid | integer | 对方的aid |
    | callback? | fun(success: | boolean, error_code?: integer) |

- 返回值

    无

- 示例

```lua
y3.steam.request_add_friend(1)
```

---

## request_delete_friend

method in Steam

- 描述

    【异步】请求删除好友

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | aid | integer | 对方的aid |
    | callback? | fun(success: | boolean, error_code?: integer) |

- 返回值

    无

- 示例

```lua
y3.steam.request_delete_friend(1)
```

---

## reply_friend_add

method in Steam

- 描述

    【异步】回复好友请求

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | aid | integer | 对方的aid |
    | accept | boolean | 是否接受 |
    | callback? | fun(success: | boolean, error_code?: integer) |

- 返回值

    无

- 示例

```lua
y3.steam.reply_friend_add(1, true)
```

---

## request_start_game

method in Steam

- 描述

    【异步】请求开始游戏（不匹配），只有队长可以调用

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | level_id? | string | 目标地图id |
    | game_mode? | integer | 目标地图模式 |
    | callback? | fun(success?: | boolean, error_code?: integer) |

- 返回值

    无

- 示例

```lua
y3.steam.request_start_game("level_id", 1)
```

---

## request_join_team

method in Steam

- 描述

    【异步】请求加入队伍

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | team_id | integer | 队伍id |
    | callback? | fun(success: | boolean, error_code?: integer) |

- 返回值

    无

- 示例

```lua
y3.steam.request_join_team(1)
```

---

## request_join_team_by_name

method in Steam

- 描述

    【异步】请求加入队伍

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | name | string | 对方的玩家名字 |
    | callback? | fun(success: | boolean, error_code?: integer) |

- 返回值

    无

- 示例

```lua
y3.steam.request_join_team_by_name("name")
```

---

## request_invite_join_team

method in Steam

- 描述

    【异步】邀请玩家加入队伍

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | aid | integer | 对方的aid |
    | callback? | fun(success: | boolean, error_code?: integer) |

- 返回值

    无

- 示例

```lua
y3.steam.request_invite_join_team(1)
```

---

## reply_team_invite

method in Steam

- 描述

    【异步】回复队伍邀请

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | aid | integer | 对方的aid |
    | team_id | integer | 队伍id |
    | accept | boolean | 是否接受 |
    | callback? | fun(success: | boolean, error_code?: integer) |

- 返回值

    无

- 示例

```lua
y3.steam.reply_team_invite(1, 1, true)
```

---

## request_quit_team

method in Steam

- 描述

    【异步】请求退出队伍

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | callback? | fun(success: | boolean, error_code?: integer) |

- 返回值

    无

- 示例

```lua
y3.steam.request_quit_team()
```

---

## request_team_info

method in Steam

- 描述

    【异步】请求指定玩家的队伍信息

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | aid | integer | 对方的aid |
    | callback | fun(team_info?: | Steam.MemberInfo[], error_code?: integer) |

- 返回值

    无

- 示例

```lua
y3.steam.request_team_info(1, function() end)
```

---

## request_transfer_captain

method in Steam

- 描述

    【异步】转交队长，只有队长可以调用

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | aid | integer | 对方的aid |
    | callback? | fun(success: | boolean, error_code?: integer) |

- 返回值

    无

- 示例

```lua
y3.steam.request_transfer_captain(1)
```

---

## request_kick_member

method in Steam

- 描述

    【异步】请求从队伍中踢出玩家，只有队长可以调用

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | aid | integer | 对方的aid |
    | callback? | fun(success: | boolean, error_code?: integer) |

- 返回值

    无

- 示例

```lua
y3.steam.request_kick_member(1)
```

---

## request_aid_by_nickname

method in Steam

- 描述

    【异步】根据玩家昵称查询玩家的aid

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | nickname | string | 玩家昵称 |
    | callback | fun(aid?: | integer, error_code?: integer) |

- 返回值

    无

- 示例

```lua
y3.steam.request_aid_by_nickname("nickname", function() end)
```

---

## request_create_team

method in Steam

- 描述

    【异步】请求创建队伍

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | team_num | integer | 人数上限 |
    | callback? | fun(success: | boolean, error_code?: integer) |

- 返回值

    无

- 示例

```lua
y3.steam.request_create_team(1)
```

---

## request_start_match

method in Steam

- 描述

    【异步】请求开始匹配

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | score | integer | 匹配分数 |
    | level_id? | string | 目标地图id |
    | game_mode? | integer | 目标地图模式 |
    | callback? | fun(success?: | boolean, error_code?: integer) |

- 返回值

    无

- 示例

```lua
y3.steam.request_start_match(1, "level_id", 1)
```

---

## request_cancel_match

method in Steam

- 描述

    【异步】请求取消匹配

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | callback? | fun(success: | boolean, error_code?: integer) |

- 返回值

    无

- 示例

```lua
y3.steam.request_cancel_match()
```

---

## request_global_archive_datas

method in Steam

- 描述

    【异步】请求全局存档数据

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | callback | fun(data: | (string | integer)[], error_code?: integer) |

- 返回值

    无

- 示例

```lua
y3.steam.request_global_archive_datas(function() end)
```

---

## request_icon

method in Steam

- 描述

    【异步】请求头像的文件路径

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | url | string | 头像的网络地址 |
    | callback | fun(path: | string) # 图像下载完毕后回调，参数为下载后的文件路径 |

- 返回值

    无

- 示例

```lua
y3.steam.request_icon("url", function() end)
```

---

## request_roll_settle_ladder_score

method in Steam

- 描述

    【异步】请求结算天梯分

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player |  |
    | params | table<string, | any> # 结算参数 |
    | callback? | fun(result: | { |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

y3.steam.request_roll_settle_ladder_score(player, {params1 = 1})
```

---

## request_create_room

method in Steam

- 描述

    【异步】请求创建房间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | room_name | string | 房间名称 |
    | callback | fun(room_info?: | Steam.FullRoomInfo, error_code?: integer) # 创建成功后回调，参数为房间id |
    | mode_id? | integer | 模式id，默认为 `1002` |
    | password? | string | 房间密码，`nil` 或空字符串等表示无需密码 |

- 返回值

    无

- 示例

```lua
y3.steam.request_create_room("room_name", function() end, 1, "password")
```

---

## request_room_list

method in Steam

- 描述

    【异步】请求房间列表

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | page | integer | 第几页，每页会有最多100个结果 |
    | callback | fun(rooms?: | Steam.SimpleRoomInfo[], error_code?: integer) |

- 返回值

    无

- 示例

```lua
y3.steam.request_room_list(1, function() end)
```

---

## request_join_room

method in Steam

- 描述

    【异步】请求加入房间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | room_id | integer |  |
    | callback | fun(room_info?: | Steam.FullRoomInfo, error_code?: integer) |
    | password? | string |  |

- 返回值

    无

- 示例

```lua
y3.steam.request_join_room(1, function() end, "password")
```

---

## request_room_info

method in Steam

- 描述

    【异步】请求指定用户所在的房间信息

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | aid | integer |  |
    | callback | fun(info?: | Steam.FullRoomInfo, error_code?: integer) |

- 返回值

    无

- 示例

```lua
y3.steam.request_room_info(1, function() end)
```

---

## request_room_start_game

method in Steam

- 描述

    【异步】请求房间开始游戏

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | callback | fun(success: | boolean, error_code?: integer) |

- 返回值

    无

- 示例

```lua
y3.steam.request_room_start_game(function() end)
```

---

## request_invite_join_room

method in Steam

- 描述

    【异步】邀请玩家加入房间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | aid | integer |  |
    | callback | fun(success: | boolean, error_code?: integer) |

- 返回值

    无

- 示例

```lua
y3.steam.request_invite_join_room(1, function() end)
```

---

## reply_accpet_room_invite

method in Steam

- 描述

    【异步】接受房间邀请

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | aid | integer |  |
    | room_id | integer |  |
    | callback | fun(success: | boolean, error_code?: integer) |

- 返回值

    无

- 示例

```lua
y3.steam.reply_accpet_room_invite(1, 1, function() end)
```

---

## request_change_room_slot

method in Steam

- 描述

    【异步】请求交换房间槽位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | slot | integer | 目标槽位 |
    | callback | fun(success: | boolean, error_code?: integer) |

- 返回值

    无

- 示例

```lua
y3.steam.request_change_room_slot(1, function() end)
```

---

## request_change_owner

method in Steam

- 描述

    【异步】请求将房主转交给其他用户

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | aid | integer | 目标用户的aid |
    | callback | fun(success: | boolean, error_code?: integer) |

- 返回值

    无

- 示例

```lua
y3.steam.request_change_owner(1, function() end)
```

---

## request_exit_room

method in Steam

- 描述

    【异步】请求退出自己所在的房间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | callback | fun(success: | boolean, error_code?: integer) |

- 返回值

    无

- 示例

```lua
y3.steam.request_exit_room(function() end)
```

---

## request_kick_from_room

method in Steam

- 描述

    【异步】请求从房间中踢出用户

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | aid | integer | 目标用户的aid |
    | callback | fun(success: | boolean, error_code?: integer) |

- 返回值

    无

- 示例

```lua
y3.steam.request_kick_from_room(1, function() end)
```

---

## request_change_slot_state

method in Steam

- 描述

    【异步】请求修改房间中某个槽位的状态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | slot | integer | 目标槽位 |
    | state | y3.Const.SteamRoomSlotState | 目标状态 |
    | callback | fun(success: | boolean, error_code?: integer) |

- 返回值

    无

- 示例

```lua
y3.steam.request_change_slot_state(1, y3.const.SteamRoomSlotState['打开'], function() end)
```

---

## request_change_room_password

method in Steam

- 描述

    【异步】请求修改房间密码

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | password? | string | 房间密码，`nil` 或空字符串等表示无需密码 |
    | callback? | fun(success: | boolean, error_code?: integer) |

- 返回值

    无

- 示例

```lua
y3.steam.request_change_room_password("password")
```

---

## request_change_room_name

method in Steam

- 描述

    【异步】请求修改房间名字

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | name | string | 房间名字 |
    | callback? | fun(success: | boolean, error_code?: integer) |

- 返回值

    无

- 示例

```lua
y3.steam.request_change_room_name("name")
```

---

## get_steam_currency

method in Steam

- 描述

    【异步】获取本地玩家在steam上使用的币种

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | | 'CNY' |

- 示例

```lua
local result = y3.steam.get_steam_currency()
```

---

## get_steam_goods_price

method in Steam

- 描述

    【异步】获取指定steam商品在本地玩家当前币种下的价格

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | goods_id | integer \| string |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number? |  |

- 示例

```lua
local result = y3.steam.get_steam_goods_price("goods_id")
```

---
