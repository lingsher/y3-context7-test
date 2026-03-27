---
sidebarDepth: 1
---
# Particle (运行时对象)

# 索引

Y3 编辑器 Particle 封装接口，提供高级方法操作 Particle 对象。

---

| 接口 | 描述 |
| --- | --- |
| [get_by_handle](#get_by_handle) |  |
| [create_screen](#create_screen) | 创建屏幕特效 |
| [create](#create) | 创建特效到单位或点 |
| [get_handle](#get_handle) |  |
| [remove](#remove) | 删除粒子 |
| [set_rotate](#set_rotate) | 设置旋转角度 |
| [set_facing](#set_facing) | 设置朝向 |
| [set_scale](#set_scale) | 设置缩放比例 |
| [set_height](#set_height) | 设置高度 |
| [set_point](#set_point) | 设置坐标 |
| [set_animation_speed](#set_animation_speed) | 设置动画速度 |
| [set_time](#set_time) | 设置持续时间 |
| [set_color](#set_color) | 设置特效颜色 |
| [set_visible](#set_visible) | 设置特效显示 |
| [get_type](#get_type) |  |

---

## get_by_handle

method in Particle

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | py_sfx | py.Sfx |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Particle |  |

- 示例

```lua
local result = y3.particle.get_by_handle(sfx)
```

---

## create_screen

method in Particle

- 描述

    创建屏幕特效

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | data | Particle.Param.Screen |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Particle |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local data = { type = 134274569, time = 3.0, target = player, is_on_fog = false }

local result = y3.particle.create_screen(data)
```

---

## create

method in Particle

- 描述

    创建特效到单位或点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | data | Particle.Param.Create |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Particle |  |

- 示例

```lua
local data = { type = 134274569, target = y3.point(0, 0) }

local result = y3.particle.create(data)
```

---

## get_handle

method in Particle

- 描述

    

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Sfx |  |

- 示例

```lua
local particle = y3.particle.create({ type = 134274569, target = y3.point(0, 0) })

local result = particle:get_handle()
```

---

## remove

method in Particle

- 描述

    删除粒子

- 参数

    无

- 返回值

    无

- 示例

```lua
local particle = y3.particle.create({ type = 134274569, target = y3.point(0, 0) })

particle:remove()
```

---

## set_rotate

method in Particle

- 描述

    设置旋转角度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | x | number | X轴角度 |
    | y | number | Y轴角度 |
    | z | number | Z轴角度 |

- 返回值

    无

- 示例

```lua
local particle = y3.particle.create({ type = 134274569, target = y3.point(0, 0) })

particle:set_rotate(1.0, 1.0, 1.0)
```

---

## set_facing

method in Particle

- 描述

    设置朝向

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | direction | number | 方向 |

- 返回值

    无

- 示例

```lua
local particle = y3.particle.create({ type = 134274569, target = y3.point(0, 0) })

particle:set_facing(1.0)
```

---

## set_scale

method in Particle

- 描述

    设置缩放比例

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | x | number | X轴缩放 |
    | y | number | Y轴缩放 |
    | z | number | Z轴缩放 |

- 返回值

    无

- 示例

```lua
local particle = y3.particle.create({ type = 134274569, target = y3.point(0, 0) })

particle:set_scale(1.0, 1.0, 1.0)
```

---

## set_height

method in Particle

- 描述

    设置高度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | height | number | 高度 |

- 返回值

    无

- 示例

```lua
local particle = y3.particle.create({ type = 134274569, target = y3.point(0, 0) })

particle:set_height(1.0)
```

---

## set_point

method in Particle

- 描述

    设置坐标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | Point | 点 |

- 返回值

    无

- 示例

```lua
local particle = y3.particle.create({ type = 134274569, target = y3.point(0, 0) })
local point = y3.point(0, 0)

particle:set_point(point)
```

---

## set_animation_speed

method in Particle

- 描述

    设置动画速度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | speed | number | 速度 |

- 返回值

    无

- 示例

```lua
local particle = y3.particle.create({ type = 134274569, target = y3.point(0, 0) })

particle:set_animation_speed(1.0)
```

---

## set_time

method in Particle

- 描述

    设置持续时间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | duration | number | 持续时间 |

- 返回值

    无

- 示例

```lua
local particle = y3.particle.create({ type = 134274569, target = y3.point(0, 0) })

particle:set_time(1.0)
```

---

## set_color

method in Particle

- 描述

    设置特效颜色

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | x | number | x |
    | y | number | y |
    | z | number | z |
    | w | number | w |

- 返回值

    无

- 示例

```lua
local particle = y3.particle.create({ type = 134274569, target = y3.point(0, 0) })

particle:set_color(1.0, 1.0, 1.0, 1.0)
```

---

## set_visible

method in Particle

- 描述

    设置特效显示

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | visible | boolean | 开关 |

- 返回值

    无

- 示例

```lua
local particle = y3.particle.create({ type = 134274569, target = y3.point(0, 0) })

particle:set_visible(true)
```

---

## get_type

method in Particle

- 描述

    

- 参数

    无

- 返回值

    无

- 示例

```lua
local particle = y3.particle.create({ type = 134274569, target = y3.point(0, 0) })

particle:get_type()
```

---
