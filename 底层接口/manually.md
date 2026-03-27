---
sidebarDepth: 1
---
# 手动定义 (Manually)

Y3 编辑器手动定义的类型和全局函数，包含定点数、运动器、触发器等。

---

| 接口 | 描述 |
| --- | --- |
| [Fix32](#Fix32) | 创建定点数 |
| [Fix32Vec2](#Fix32Vec2) | 创建二维定点数向量 |
| [Fix32Vec3](#Fix32Vec3) | 创建三维定点数向量/点 |
| [new_global_trigger](#new_global_trigger) | 创建全局触发器 |
| [python_len](#python_len) | 获取容器大小 |
| [python_index](#python_index) | 获取容器元素 |
| [set_python_index](#set_python_index) | 设置容器元素 |
| [python.debug_ns_timestamp](#python.debug_ns_timestamp) | 获取调试用纳秒时间戳 |
| [pydict](#pydict) | 创建Python字典对象 |
| [pytuple](#pytuple) | 创建Python元组对象 |
| [StraightMoverArgs](#StraightMoverArgs) | 直线运动参数生成器 |
| [ChasingMoverArgs](#ChasingMoverArgs) | 追踪运动参数生成器 |
| [CurvedMoverArgs](#CurvedMoverArgs) | 曲线运动参数生成器 |
| [RoundMoverArgs](#RoundMoverArgs) | 环绕运动参数生成器 |
| [Unit:create_mover_trigger](#Unit:create_mover_trigger) | 为单位创建运动器触发器 |
| [Projectile:create_mover_trigger](#Projectile:create_mover_trigger) | 为投射物创建运动器触发器 |
| [consoleprint](#consoleprint) | 控制台打印（调试用） |
| [upload_traceback](#upload_traceback) | 上传错误堆栈信息 |
| [enable_lua_profile](#enable_lua_profile) | 启用/禁用 tracy 性能分析（对运行性能有较大影响） |
| [GameAPI.bind_local_listener](#GameAPI.bind_local_listener) | 绑定本地UI事件监听器 |
| [GameAPI.get_prefab_ins_id_by_name](#GameAPI.get_prefab_ins_id_by_name) | 根据预制体名称获取实例ID |
| [GameAPI.lua_get_start_args](#GameAPI.lua_get_start_args) | 获取游戏启动参数 |
| [broadcast_lua_msg](#broadcast_lua_msg) | 广播Lua消息给所有玩家 |
| [request_url](#request_url) | HTTP请求 |
| [os.clock_banned](#os.clock_banned) | 获取本地时钟（每个玩家返回结果不同，不可用于同步逻辑） |
| [math.random_banned](#math.random_banned) | 获取本地随机数（每个玩家返回结果不同，不可用于同步逻辑） |
| [Unit:api_add_multi_state](#Unit:api_add_multi_state) | 为单位添加多重状态 |
| [Unit:api_remove_multi_state](#Unit:api_remove_multi_state) | 移除单位的多重状态 |
| [regist_object_event](#regist_object_event) | 注册对象事件回调 |
| [unregist_object_event](#unregist_object_event) | 取消注册对象事件 |
| [start_danmaku](#start_danmaku) | 开始读取弹幕 |
| [stop_danmaku](#stop_danmaku) | 停止读取弹幕 |
| [get_danmaku_comments](#get_danmaku_comments) | 获取新增弹幕列表 |

---

## Fix32

全局函数

- 描述

    创建定点数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | luaNumber | number|string | Lua数字或字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 定点数 |

- 示例

```lua
local fixed = Fix32(100)
local fixed2 = Fix32(3.14)
local fixed3 = Fix32("200.5")
```

---

## Fix32Vec2

全局函数

- 描述

    创建二维定点数向量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | x | number | X坐标 |
    | y | number | Y坐标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FixedVec2 | 二维定点数向量 |

- 示例

```lua
local vec2 = Fix32Vec2(100, 200)

-- 用于环绕运动器的目标位置
local mover_args = RoundMoverArgs()
mover_args.set_target_pos(Fix32Vec2(500, 500))
```

---

## Fix32Vec3

全局函数

- 描述

    创建三维定点数向量/点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | x | number | X坐标 |
    | y | number | Y坐标 |
    | z | number | Z坐标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Point | 三维点 |

- 示例

```lua
local point = Fix32Vec3(1000, 1000, 0)

-- 用于单位传送
local unit = y3.player.get_by_id(1):get_all_units()[1]
unit.handle:api_transmit(point)
```

---

## new_global_trigger

全局函数

- 描述

    创建全局触发器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | id | integer | 触发器ID |
    | name | string | 触发器名称 |
    | event | y3.Const.EventType | 事件类型（字符串，如 "ET_GAME_INIT"） |
    | init_enabled | boolean | 初始是否启用 |
    | addition | any | 附加参数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | table | 触发器对象，包含on_event回调 |

- 示例

```lua
local trigger = new_global_trigger(1, "test", "ET_GAME_INIT", true, nil)
trigger.on_event = function(trigger, event, actor, data)
    print("触发器执行")
end
```

---

## python_len

全局函数

- 描述

    获取容器大小

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | py.DynamicTypeMeta|py.Tuple | 容器对象 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 容器大小 |

- 示例

```lua
local dict = pydict()
local size = python_len(dict)
```

---

## python_index

全局函数

- 描述

    获取容器元素

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | py.DynamicTypeMeta|py.Tuple | 容器对象 |
    | index | integer | 索引 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | any | 元素值 |

- 示例

```lua
local tuple = pytuple({[1] = true})
local value = python_index(tuple, 0)
```

---

## set_python_index

全局函数

- 描述

    设置容器元素

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | py.DynamicTypeMeta | 容器对象 |
    | index | integer | 索引 |
    | value | any | 要设置的值 |

- 返回值

    无

- 示例

```lua
local dict = pydict()
set_python_index(dict, 0, "value")
```

---

## python.debug_ns_timestamp

全局函数

- 描述

    获取调试用纳秒时间戳

- 参数

    无

- 返回值

    无

- 示例

```lua
local timestamp = python.debug_ns_timestamp()
```

---

## pydict

全局函数

- 描述

    创建Python字典对象

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Dict | Python字典 |

- 示例

```lua
local dict = pydict()
```

---

## pytuple

全局函数

- 描述

    创建Python元组对象

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | list? | table<integer, true> | 可选的初始列表 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Tuple | Python元组 |

- 示例

```lua
local tuple = pytuple()
local tuple2 = pytuple({[1] = true, [2] = true})
```

---

## StraightMoverArgs

全局函数

- 描述

    直线运动参数生成器

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MoverLineBuilder | 直线运动参数构建器 |

- 示例

```lua
local args = StraightMoverArgs()
args.set_angle(Fix32(45))
args.set_max_dist(Fix32(1000))
args.set_init_velocity(Fix32(500))
args.set_acceleration(Fix32(100))
```

---

## ChasingMoverArgs

全局函数

- 描述

    追踪运动参数生成器

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MoverTargetBuilder | 追踪运动参数构建器 |

- 示例

```lua
local args = ChasingMoverArgs()
args.set_init_velocity(Fix32(500))
args.set_stop_distance_to_target(Fix32(100))
```

---

## CurvedMoverArgs

全局函数

- 描述

    曲线运动参数生成器

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MoverCurveBuilder | 曲线运动参数构建器 |

- 示例

```lua
local args = CurvedMoverArgs()
args.set_angle(Fix32(0))
args.set_max_dist(Fix32(1000))
args.set_init_velocity(Fix32(300))
```

---

## RoundMoverArgs

全局函数

- 描述

    环绕运动参数生成器

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MoverRoundBuilder | 环绕运动参数构建器 |

- 示例

```lua
local args = RoundMoverArgs()
args.set_is_to_unit(false)
args.set_target_pos(Fix32Vec2(1000, 1000))
args.set_circle_radius(Fix32(200))
args.set_angle_velocity(Fix32(120))
```

---

## Unit:create_mover_trigger

全局函数

- 描述

    为单位创建运动器触发器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | mover_data | table | 运动器参数（由xxxMoverArgs()创建） |
    | mode | string | 运动模式：'StraightMover'|'ChasingMover'|'CurvedMover'|'RoundMover' |
    | unit_collide | function | 单位碰撞回调 fun(mover, unit) |
    | mover_finish | function | 运动完成回调 fun(mover) |
    | terrain_collide | function | 地形碰撞回调 fun(mover) |
    | mover_interrupt | function | 运动中断回调 fun(mover) |
    | mover_removed | function | 运动器移除回调 fun(mover) |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Mover | 运动器对象 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local args = StraightMoverArgs()
args.set_angle(Fix32(0))
args.set_max_dist(Fix32(500))
args.set_init_velocity(Fix32(300))

local mover = unit.handle:create_mover_trigger(
    args.dict,
    'StraightMover',
    function(mover, hit_unit) print("碰撞单位") end,
    function(mover) print("运动完成") end,
    function(mover) print("碰撞地形") end,
    function(mover) print("运动中断") end,
    function(mover) print("运动器移除") end
)
```

---

## Projectile:create_mover_trigger

全局函数

- 描述

    为投射物创建运动器触发器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | mover_data | table | 运动器参数（由xxxMoverArgs()创建） |
    | mode | string | 运动模式：'StraightMover'|'ChasingMover'|'CurvedMover'|'RoundMover' |
    | unit_collide | function | 单位碰撞回调 fun(mover, unit) |
    | mover_finish | function | 运动完成回调 fun(mover) |
    | terrain_collide | function | 地形碰撞回调 fun(mover) |
    | mover_interrupt | function | 运动中断回调 fun(mover) |
    | mover_removed | function | 运动器移除回调 fun(mover) |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Mover | 运动器对象 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local target_point = unit:get_point()
local projectile = y3.projectile.create({ key = 134274569, target = target_point })

local args = ChasingMoverArgs()
args.set_init_velocity(Fix32(500))

local mover = projectile.handle:create_mover_trigger(
    args.dict,
    'ChasingMover',
    function(mover, hit_unit) print("碰撞单位") end,
    function(mover) print("运动完成") end,
    function(mover) print("碰撞地形") end,
    function(mover) print("运动中断") end,
    function(mover) print("运动器移除") end
)
```

---

## consoleprint

全局函数

- 描述

    控制台打印（调试用）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ... | any | 任意数量的参数 |

- 返回值

    无

- 示例

```lua
consoleprint("调试信息", 123, true)
```

---

## upload_traceback

全局函数

- 描述

    上传错误堆栈信息

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | message | string | 错误消息 |

- 返回值

    无

- 示例

```lua
upload_traceback("发生了一个错误")
```

---

## enable_lua_profile

全局函数

- 描述

    启用/禁用 tracy 性能分析（对运行性能有较大影响）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | enable | boolean | 是否启用 |

- 返回值

    无

- 示例

```lua
-- 开始性能分析
enable_lua_profile(true)
-- 执行需要分析的代码...
-- 结束性能分析
enable_lua_profile(false)
```

---

## GameAPI.bind_local_listener

全局函数

- 描述

    绑定本地UI事件监听器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | comp_uid | string | UI组件UID |
    | event_type | integer | 事件类型 |
    | callback | function | 回调函数 |

- 返回值

    无

- 示例

```lua
GameAPI.bind_local_listener("btn_start", 1, function()
    print("按钮被点击")
end)
```

---

## GameAPI.get_prefab_ins_id_by_name

全局函数

- 描述

    根据预制体名称获取实例ID

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_name | string | 预制体名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 实例ID |

- 示例

```lua
local ins_id = GameAPI.get_prefab_ins_id_by_name("my_prefab")
```

---

## GameAPI.lua_get_start_args

全局函数

- 描述

    获取游戏启动参数

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Dict | 启动参数字典 |

- 示例

```lua
local args = GameAPI.lua_get_start_args()
```

---

## broadcast_lua_msg

全局函数

- 描述

    广播Lua消息给所有玩家

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | id | string | 消息ID |
    | data | string | 消息数据 |

- 返回值

    无

- 示例

```lua
broadcast_lua_msg("sync_data", '{"score": 100}')
```

---

## request_url

全局函数

- 描述

    HTTP请求

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | url | string | 请求URL |
    | post? | boolean | 是否POST请求 |
    | body? | string | 请求体 |
    | port? | integer | 端口号 |
    | timeout? | number | 超时时间（秒） |
    | headers? | table | 请求头 |
    | callback? | function | 回调函数 fun(body?) |

- 返回值

    无

- 示例

```lua
-- GET请求
request_url("https://api.example.com/data", false, nil, nil, 10, nil, function(body)
    if body then
        print("响应:", body)
    end
end)

-- POST请求
request_url("https://api.example.com/submit", true, '{"key":"value"}', nil, 10, 
    {["Content-Type"] = "application/json"}, 
    function(body) print("响应:", body) end
)
```

---

## os.clock_banned

全局函数

- 描述

    获取本地时钟（每个玩家返回结果不同，不可用于同步逻辑）

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 时钟值 |

- 示例

```lua
-- 注意：仅用于本地效果，不可用于游戏逻辑同步
local clock = os.clock_banned()
```

---

## math.random_banned

全局函数

- 描述

    获取本地随机数（每个玩家返回结果不同，不可用于同步逻辑）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | m? | integer | 范围下限或上限 |
    | n? | integer | 范围上限 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number|integer | 随机数 |

- 示例

```lua
-- 注意：仅用于本地效果，不可用于游戏逻辑同步
local r1 = math.random_banned()        -- 0-1之间的小数
local r2 = math.random_banned(10)      -- 1-10之间的整数
local r3 = math.random_banned(5, 15)   -- 5-15之间的整数
```

---

## Unit:api_add_multi_state

全局函数

- 描述

    为单位添加多重状态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | state_enum | integer | 状态枚举值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
unit.handle:api_add_multi_state(1)
```

---

## Unit:api_remove_multi_state

全局函数

- 描述

    移除单位的多重状态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | state_enum | integer | 状态枚举值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
unit.handle:api_remove_multi_state(1)
```

---

## regist_object_event

全局函数

- 描述

    注册对象事件回调

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | handle | any | 对象句柄 |
    | py_event_name | string | Python事件名称 |
    | callback | function | 回调函数 fun(data) |
    | ... | any | 额外参数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 事件序列号，用于取消注册 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local seq = regist_object_event(unit.handle, "ET_UNIT_DEAD", function(data)
    print("单位死亡")
end)
```

---

## unregist_object_event

全局函数

- 描述

    取消注册对象事件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | seq | integer | 事件序列号 |

- 返回值

    无

- 示例

```lua
-- 使用 regist_object_event 返回的序列号
unregist_object_event(seq)
```

---

## start_danmaku

全局函数

- 描述

    开始读取弹幕

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | port | integer | 端口号 |

- 返回值

    无

- 示例

```lua
start_danmaku(8080)
```

---

## stop_danmaku

全局函数

- 描述

    停止读取弹幕

- 参数

    无

- 返回值

    无

- 示例

```lua
stop_danmaku()
```

---

## get_danmaku_comments

全局函数

- 描述

    获取新增弹幕列表

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | any[] | 弹幕列表 |

- 示例

```lua
local comments = get_danmaku_comments()
for _, comment in ipairs(comments) do
    print(comment)
end
```

---
