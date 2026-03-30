---
sidebarDepth: 1
---
# Camera (场景对象)

# 索引

Y3 编辑器 Camera 封装接口，提供高级方法操作 Camera 对象。

---

| 接口 | 描述 |
| --- | --- |
| [get_by_handle](#get_by_handle) |  |
| [get_by_res_id](#get_by_res_id) | 获取摆放在场景上的镜头 |
| [apply](#apply) | 引用镜头 |
| [is_camera_playing_timeline](#is_camera_playing_timeline) | 玩家镜头是否正在播放动画 |
| [create_camera](#create_camera) | 创建镜头 |
| [enable_camera_move](#enable_camera_move) | 允许玩家镜头移动 |
| [disable_camera_move](#disable_camera_move) | 禁止玩家镜头移动 |
| [play_camera_timeline](#play_camera_timeline) | 播放镜头动画 |
| [stop_camera_timeline](#stop_camera_timeline) | 停止镜头动画 |
| [camera_shake_with_decay](#camera_shake_with_decay) | 镜头带衰减震动 |
| [camera_shake](#camera_shake) | 镜头摇晃镜头 |
| [show_tps_mode_mouse](#show_tps_mode_mouse) | 设置TPS视角鼠标显示 |
| [linear_move_by_time](#linear_move_by_time) | 线性移动（时间） |
| [set_camera_follow_unit](#set_camera_follow_unit) | 设置镜头跟随单位 |
| [cancel_camera_follow_unit](#cancel_camera_follow_unit) | 设置镜头取消跟随 |
| [set_tps_follow_unit](#set_tps_follow_unit) | 设置镜头第三人称跟随单位 |
| [cancel_tps_follow_unit](#cancel_tps_follow_unit) | 取消镜头第三人称跟随单位 |
| [look_at_point](#look_at_point) | 设置镜头朝向点 |
| [set_max_distance](#set_max_distance) | 设置镜头高度上限 |
| [set_rotate](#set_rotate) | 设置镜头角度 |
| [set_distance](#set_distance) | 设置焦点距离 |
| [set_focus_height](#set_focus_height) | 设置镜头焦点高度 |
| [limit_in_rectangle_area](#limit_in_rectangle_area) | 限制镜头移动范围 |
| [cancel_area_limit](#cancel_area_limit) | 关闭镜头限制移动 |
| [set_moving_with_mouse](#set_moving_with_mouse) | 设置是否可以鼠标移动镜头 |
| [set_mouse_move_camera_speed](#set_mouse_move_camera_speed) | 设置镜头移动速度（鼠标） |
| [set_keyboard_move_camera_speed](#set_keyboard_move_camera_speed) | 设置镜头移动速度（键盘） |
| [get_player_camera_direction](#get_player_camera_direction) | 获取玩家摄像机朝向。 |
| [get_camera_center_raycast](#get_camera_center_raycast) | 获取玩家摄像机中心射线的碰撞点。 |
| [get_attr_real](#get_attr_real) | 获取（本地玩家）的镜头属性（实数） |
| [get_attr_integer](#get_attr_integer) | 获取（本地玩家）的镜头属性（整数） |

---

## get_by_handle

method in Camera

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | py_camera | integer |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Camera |  |

- 示例

```lua
local result = y3.camera.get_by_handle(1)
```

---

## get_by_res_id

method in Camera

- 描述

    获取摆放在场景上的镜头

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | res_id | integer |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Camera |  |

- 示例

```lua
local result = y3.camera.get_by_res_id(1)
```

---

## apply

method in Camera

- 描述

    引用镜头

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player_or_group? | Player \| PlayerGroup | 玩家或玩家组，默认为所有玩家 |
    | duration? | number | 过渡时间，默认为0 |
    | slope_mode? | y3.Const.CameraMoveMode | 过渡模式，默认为匀速 |

- 返回值

    无

- 示例

```lua
local camera = y3.camera.create_camera(y3.point(0, 0), 1000, 500, 0, 45, 3000)

camera:apply(player, 1.0)
```

---

## is_camera_playing_timeline

method in Camera

- 描述

    玩家镜头是否正在播放动画

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean |  |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = y3.camera.is_camera_playing_timeline(player)
```

---

## create_camera

method in Camera

- 描述

    创建镜头

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | Point | 镜头所在点 |
    | focal_length | number | 焦距 |
    | focal_height | number | 焦点高度 |
    | yaw | number | 镜头的yaw |
    | pitch | number | 镜头的pitch |
    | range_of_visibility | number | 远景裁切范围 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Camera |  |

- 示例

```lua
local point = y3.point(0, 0)

local result = y3.camera.create_camera(point, 1.0, 1.0, 1.0, 1.0, 1.0)
```

---

## enable_camera_move

method in Camera

- 描述

    允许玩家镜头移动

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

y3.camera.enable_camera_move(player)
```

---

## disable_camera_move

method in Camera

- 描述

    禁止玩家镜头移动

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

y3.camera.disable_camera_move(player)
```

---

## play_camera_timeline

method in Camera

- 描述

    播放镜头动画

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | camera_timeline_id | py.CamlineID | 镜头动画ID |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

y3.camera.play_camera_timeline(player, 134274569)
```

---

## stop_camera_timeline

method in Camera

- 描述

    停止镜头动画

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

y3.camera.stop_camera_timeline(player)
```

---

## camera_shake_with_decay

method in Camera

- 描述

    镜头带衰减震动

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | shake | number | 震动幅度 |
    | attenuation | number | 衰减 |
    | frequency | number | 频率 |
    | time | number | 持续时间 |
    | shake_type | integer | 震动模式 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

y3.camera.camera_shake_with_decay(player, 1.0, 1.0, 1.0, 1.0, 1)
```

---

## camera_shake

method in Camera

- 描述

    镜头摇晃镜头

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | strength | number | 晃动幅度 |
    | speed | number | 速率 |
    | time | number | 持续时间 |
    | shake_type | integer | 震动模式 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

y3.camera.camera_shake(player, 1.0, 1.0, 1.0, 1)
```

---

## show_tps_mode_mouse

method in Camera

- 描述

    设置TPS视角鼠标显示

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | switch | boolean | 是否显示鼠标 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

y3.camera.show_tps_mode_mouse(player, true)
```

---

## linear_move_by_time

method in Camera

- 描述

    线性移动（时间）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | point | Point | 目标点 |
    | time | number | 过渡时间 |
    | move_type | integer | 移动模式 |

- 返回值

    无

- 示例

```lua
local point = y3.point(0, 0)
local player = y3.player.get_by_id(1)

y3.camera.linear_move_by_time(player, point, 1.0, 1)
```

---

## set_camera_follow_unit

method in Camera

- 描述

    设置镜头跟随单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | unit | Unit | 目标单位 |
    | x? | number | 过渡时间 |
    | y? | number | 移动模式 |
    | height? | number | 高度 |
    | socket? | string | socket |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

y3.camera.set_camera_follow_unit(player, unit, 1.0, 1.0, 1.0, "socket")
```

---

## cancel_camera_follow_unit

method in Camera

- 描述

    设置镜头取消跟随

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

y3.camera.cancel_camera_follow_unit(player)
```

---

## set_tps_follow_unit

method in Camera

- 描述

    设置镜头第三人称跟随单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | unit | Unit | 目标单位 |
    | sensitivity? | number | 灵敏度 |
    | yaw? | number | yaw |
    | pitch? | number | pitch |
    | x_offset? | number | 偏移量X |
    | y_offset? | number | 偏移量Y |
    | z_offset? | number | 偏移高度 |
    | camera_distance? | number | 距离焦点距离 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

y3.camera.set_tps_follow_unit(player, unit, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0)
```

---

## cancel_tps_follow_unit

method in Camera

- 描述

    取消镜头第三人称跟随单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

y3.camera.cancel_tps_follow_unit(player)
```

---

## look_at_point

method in Camera

- 描述

    设置镜头朝向点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | point | Point | 目标点 |
    | time | number | 过渡时间 |

- 返回值

    无

- 示例

```lua
local point = y3.point(0, 0)
local player = y3.player.get_by_id(1)

y3.camera.look_at_point(player, point, 1.0)
```

---

## set_max_distance

method in Camera

- 描述

    设置镜头高度上限

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | value | number | 高度上限 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

y3.camera.set_max_distance(player, 1.0)
```

---

## set_rotate

method in Camera

- 描述

    设置镜头角度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | angle_type | py.CameraRotate | 角度类型 |
    | value | number | 值 |
    | time | number | 过渡时间 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local camera_rotate = 1

y3.camera.set_rotate(player, camera_rotate, 1.0, 1.0)
```

---

## set_distance

method in Camera

- 描述

    设置焦点距离

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | value | number | 值 |
    | time | number | 过渡时间 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

y3.camera.set_distance(player, 1.0, 1.0)
```

---

## set_focus_height

method in Camera

- 描述

    设置镜头焦点高度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | value | number | 值 |
    | time | number | 过渡时间 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

y3.camera.set_focus_height(player, 1.0, 1.0)
```

---

## limit_in_rectangle_area

method in Camera

- 描述

    限制镜头移动范围

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | area | Area | 移动范围区域 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local area = y3.area.create_circle_area(y3.point(0, 0), 500)

y3.camera.limit_in_rectangle_area(player, area)
```

---

## cancel_area_limit

method in Camera

- 描述

    关闭镜头限制移动

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

y3.camera.cancel_area_limit(player)
```

---

## set_moving_with_mouse

method in Camera

- 描述

    设置是否可以鼠标移动镜头

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | state | boolean | 开关 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

y3.camera.set_moving_with_mouse(player, true)
```

---

## set_mouse_move_camera_speed

method in Camera

- 描述

    设置镜头移动速度（鼠标）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | speed | number | 移动速度 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

y3.camera.set_mouse_move_camera_speed(player, 1.0)
```

---

## set_keyboard_move_camera_speed

method in Camera

- 描述

    设置镜头移动速度（键盘）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | speed | number | 移动速度 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

y3.camera.set_keyboard_move_camera_speed(player, 1.0)
```

---

## get_player_camera_direction

method in Camera

- 描述

    获取玩家摄像机朝向。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Point |  |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = y3.camera.get_player_camera_direction(player)
```

---

## get_camera_center_raycast

method in Camera

- 描述

    获取玩家摄像机中心射线的碰撞点。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Point |  |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = y3.camera.get_camera_center_raycast(player)
```

---

## get_attr_real

method in Camera

- 描述

    获取（本地玩家）的镜头属性（实数）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr | 'pitch' \| 'yaw' \| 'roll' \| 'fov' |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number |  |

- 示例

```lua
local attr = 'pitch'

local result = y3.camera.get_attr_real(attr)
```

---

## get_attr_integer

method in Camera

- 描述

    获取（本地玩家）的镜头属性（整数）

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer |  |

- 示例

```lua
local result = y3.camera.get_attr_integer()
```

---
