---
sidebarDepth: 1
---
# Projectile (物编对象)

# 索引

Y3 编辑器 Projectile 封装接口，提供高级方法操作 Projectile 对象。

---

| 接口 | 描述 |
| --- | --- |
| [get_by_handle](#get_by_handle) |  |
| [get_by_id](#get_by_id) |  |
| [get_key](#get_key) | 获取投射物的类型ID |
| [is_exist](#is_exist) | 是否存在 |
| [get_id](#get_id) | 获取唯一ID |
| [get_height](#get_height) | 获取投射物高度 |
| [get_left_time](#get_left_time) | 获取投射物剩余持续时间 |
| [get_owner](#get_owner) | 获取投射物的拥有者 |
| [get_facing](#get_facing) | 获取投射物朝向 |
| [get_point](#get_point) | 获取投射物所在点 |
| [has_tag](#has_tag) | 是否拥有标签 |
| [add_tag](#add_tag) | 投射物添加标签 |
| [remove_tag](#remove_tag) | 投射物移除标签 |
| [create](#create) | 创建投射物 |
| [set_owner](#set_owner) | 设置所属单位 |
| [set_ability](#set_ability) | 设置关联技能 |
| [remove](#remove) | 销毁 |
| [set_height](#set_height) | 设置高度 |
| [set_point](#set_point) | 设置坐标 |
| [set_facing](#set_facing) | 设置朝向 |
| [set_rotation](#set_rotation) | 设置旋转 |
| [set_scale](#set_scale) | 设置缩放 |
| [set_animation_speed](#set_animation_speed) | 设置动画速度 |
| [set_time](#set_time) | 设置持续时间 |
| [add_time](#add_time) | 增加持续时间 |
| [get_ability](#get_ability) | 获得关联技能 |
| [set_visible](#set_visible) | 设置投射物的可见性 |
| [is_destroyed](#is_destroyed) |  |
| [get_type](#get_type) |  |

---

## get_by_handle

method in Projectile

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | py_projectile | py.ProjectileEntity |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Projectile? |  |

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })

local result = y3.projectile.get_by_handle(projectile.handle)
```

---

## get_by_id

method in Projectile

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | id | py.ProjectileID |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Projectile |  |

- 示例

```lua
local result = y3.projectile.get_by_id(134274569)
```

---

## get_key

method in Projectile

- 描述

    获取投射物的类型ID

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileKey |  |

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })

local result = projectile:get_key()
```

---

## is_exist

method in Projectile

- 描述

    是否存在

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })

local result = projectile:is_exist()
```

---

## get_id

method in Projectile

- 描述

    获取唯一ID

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer |  |

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })

local result = projectile:get_id()
```

---

## get_height

method in Projectile

- 描述

    获取投射物高度

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 高度 |

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })

local result = projectile:get_height()
```

---

## get_left_time

method in Projectile

- 描述

    获取投射物剩余持续时间

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 投射物剩余持续时间 |

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })

local result = projectile:get_left_time()
```

---

## get_owner

method in Projectile

- 描述

    获取投射物的拥有者

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Unit? | 投射物的拥有者 |

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })

local result = projectile:get_owner()
```

---

## get_facing

method in Projectile

- 描述

    获取投射物朝向

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 投射物朝向 |

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })

local result = projectile:get_facing()
```

---

## get_point

method in Projectile

- 描述

    获取投射物所在点

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Point | 投射物所在点 |

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })

local result = projectile:get_point()
```

---

## has_tag

method in Projectile

- 描述

    是否拥有标签

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | 标签 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否拥有标签 |

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })

local result = projectile:has_tag("tag")
```

---

## add_tag

method in Projectile

- 描述

    投射物添加标签

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | 标签 |

- 返回值

    无

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })

projectile:add_tag("tag")
```

---

## remove_tag

method in Projectile

- 描述

    投射物移除标签

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | 标签 |

- 返回值

    无

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })

projectile:remove_tag("tag")
```

---

## create

method in Projectile

- 描述

    创建投射物

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | data | Projectile.CreateData | 投射物创建数据 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Projectile |  |

- 示例

```lua
local data = { key = 134274569, target = y3.point(0, 0) }

local result = y3.projectile.create(data)
```

---

## set_owner

method in Projectile

- 描述

    设置所属单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 所属单位 |

- 返回值

    无

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })
local unit = y3.player.get_by_id(1):get_all_units()[1]

projectile:set_owner(unit)
```

---

## set_ability

method in Projectile

- 描述

    设置关联技能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability | Ability | 关联技能 |

- 返回值

    无

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

projectile:set_ability(ability)
```

---

## remove

method in Projectile

- 描述

    销毁

- 参数

    无

- 返回值

    无

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })

projectile:remove()
```

---

## set_height

method in Projectile

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
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })

projectile:set_height(1.0)
```

---

## set_point

method in Projectile

- 描述

    设置坐标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | Point | 点坐标 |

- 返回值

    无

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })
local point = y3.point(0, 0)

projectile:set_point(point)
```

---

## set_facing

method in Projectile

- 描述

    设置朝向

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | direction | number | 朝向 |

- 返回值

    无

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })

projectile:set_facing(1.0)
```

---

## set_rotation

method in Projectile

- 描述

    设置旋转

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | x | number | x轴 |
    | y | number | y轴 |
    | z | number | z轴 |

- 返回值

    无

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })

projectile:set_rotation(1.0, 1.0, 1.0)
```

---

## set_scale

method in Projectile

- 描述

    设置缩放

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | x | number | x轴 |
    | y | number | y轴 |
    | z | number | z轴 |

- 返回值

    无

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })

projectile:set_scale(1.0, 1.0, 1.0)
```

---

## set_animation_speed

method in Projectile

- 描述

    设置动画速度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | speed | number |  |

- 返回值

    无

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })

projectile:set_animation_speed(1.0)
```

---

## set_time

method in Projectile

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
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })

projectile:set_time(1.0)
```

---

## add_time

method in Projectile

- 描述

    增加持续时间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | duration | number | 持续时间 |

- 返回值

    无

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })

projectile:add_time(1.0)
```

---

## get_ability

method in Projectile

- 描述

    获得关联技能

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Ability? | 投射物或魔法效果的关联技能 |

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })

local result = projectile:get_ability()
```

---

## set_visible

method in Projectile

- 描述

    设置投射物的可见性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | visible | boolean | 是否可见 |
    | player_or_group? | Player \| PlayerGroup | 应用于哪些玩家，默认为所有玩家 |

- 返回值

    无

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })

projectile:set_visible(true)
```

---

## is_destroyed

method in Projectile

- 描述

    

- 参数

    无

- 返回值

    无

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })

projectile:is_destroyed()
```

---

## get_type

method in Projectile

- 描述

    

- 参数

    无

- 返回值

    无

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })

projectile:get_type()
```

---
