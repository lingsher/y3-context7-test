---
sidebarDepth: 1
---
# 投射物 (Projectile)

# 索引

Y3 编辑器投射物对象相关接口，用于操作投射物的位置、速度、方向等。

---

| 接口 | 描述 |
| --- | --- |
| [api_get_self](#api_get_self) | 投射物本身对象 |
| [api_get_id](#api_get_id) | 获取单位ID |
| [api_get_key](#api_get_key) | 投射物编号 |
| [api_get_owner](#api_get_owner) | 投射物产生者 |
| [api_delete](#api_delete) | 销毁投射物对象 |
| [api_set_position](#api_set_position) | 设置投射物位置 |
| [api_set_face_angle](#api_set_face_angle) | 设置投射物朝向 |
| [api_set_rotation](#api_set_rotation) | 设置投射物旋转 |
| [api_set_scale](#api_set_scale) | 设置投射物缩放 |
| [api_set_animation_speed](#api_set_animation_speed) | 设置投射物特效播放速度 |
| [api_set_duration](#api_set_duration) | 设置投射物持续时间 |
| [api_add_duration](#api_add_duration) | 增加投射物持续时间 |
| [api_get_left_time](#api_get_left_time) | 获取投射物剩余持续时间 |
| [api_get_height](#api_get_height) | 获取投射物高度 |
| [api_get_face_angle](#api_get_face_angle) | 获取投射物角度 |
| [api_get_position](#api_get_position) | 获取投射物位置 |
| [api_get_face_dir](#api_get_face_dir) | 获取投射物朝向 |
| [api_raise_height](#api_raise_height) | 投射物抬高 |
| [api_get_str_attr](#api_get_str_attr) | 获取投射物的字符串属性 |
| [api_set_str_attr](#api_set_str_attr) | 设置投射物的字符串属性 |
| [api_add_tag](#api_add_tag) | 投射物添加键值对 |
| [api_remove_tag](#api_remove_tag) | 投射物移除键值对 |
| [api_play_sound_by_proj_for_role_relation](#api_play_sound_by_proj_for_role_relation) | 对投射物所属单位的所属玩家关系播放音乐 |
| [get_projectile_role](#get_projectile_role) | 获取投射物的玩家 |
| [api_set_projectile_visible](#api_set_projectile_visible) | 设置投射物对玩家的可见性 |

---

## api_get_self

method in ProjectileEntity

- 描述

    投射物本身对象

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit? | 投射物本身对象 |

- 示例

```lua
-- 创建投射物对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local target_point = unit:get_point()
local projectile = y3.projectile.create({ key = 134274569, target = target_point })

local result = projectile.handle:api_get_self()
```

---

## api_get_id

method in ProjectileEntity

- 描述

    获取单位ID

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitID? | 单位ID |

- 示例

```lua
-- 创建投射物对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local target_point = unit:get_point()
local projectile = y3.projectile.create({ key = 134274569, target = target_point })

local result = projectile.handle:api_get_id()
```

---

## api_get_key

method in ProjectileEntity

- 描述

    投射物编号

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileKey? | 投射物的key |

- 示例

```lua
-- 创建投射物对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local target_point = unit:get_point()
local projectile = y3.projectile.create({ key = 134274569, target = target_point })

local result = projectile.handle:api_get_key()
```

---

## api_get_owner

method in ProjectileEntity

- 描述

    投射物产生者

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit? | 投射物产生者 |

- 示例

```lua
-- 创建投射物对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local target_point = unit:get_point()
local projectile = y3.projectile.create({ key = 134274569, target = target_point })

local result = projectile.handle:api_get_owner()
```

---

## api_delete

method in ProjectileEntity

- 描述

    销毁投射物对象

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit? | py.Unit | 销毁的投射物对象 |
    | immediately? | boolean | 立即移除表现 |

- 返回值

    无

- 示例

```lua
-- 创建投射物对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local target_point = unit:get_point()
local projectile = y3.projectile.create({ key = 134274569, target = target_point })

projectile.handle:api_delete(nil, true)
```

---

## api_set_position

method in ProjectileEntity

- 描述

    设置投射物位置

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.Point | 投射物位置 |
    | interpolation? | boolean | 是否平滑 |

- 返回值

    无

- 示例

```lua
-- 创建投射物对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local target_point = unit:get_point()
local projectile = y3.projectile.create({ key = 134274569, target = target_point })
local point = Fix32Vec3(0, 0, 0)

projectile.handle:api_set_position(point, true)
```

---

## api_set_face_angle

method in ProjectileEntity

- 描述

    设置投射物朝向

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | face_angle | number | 投射物朝向 |

- 返回值

    无

- 示例

```lua
-- 创建投射物对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local target_point = unit:get_point()
local projectile = y3.projectile.create({ key = 134274569, target = target_point })

projectile.handle:api_set_face_angle(1.0)
```

---

## api_set_rotation

method in ProjectileEntity

- 描述

    设置投射物旋转

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | x | number | x轴旋转 |
    | z | number | y轴旋转 |
    | y | number | z轴旋转 |

- 返回值

    无

- 示例

```lua
-- 创建投射物对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local target_point = unit:get_point()
local projectile = y3.projectile.create({ key = 134274569, target = target_point })

projectile.handle:api_set_rotation(1.0, 1.0, 1.0)
```

---

## api_set_scale

method in ProjectileEntity

- 描述

    设置投射物缩放

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | x | number | x轴缩放 |
    | z | number | y轴缩放 |
    | y | number | z轴缩放 |
    | duration? | number | 过渡时间 |

- 返回值

    无

- 示例

```lua
-- 创建投射物对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local target_point = unit:get_point()
local projectile = y3.projectile.create({ key = 134274569, target = target_point })

projectile.handle:api_set_scale(1.0, 1.0, 1.0, 1.0)
```

---

## api_set_animation_speed

method in ProjectileEntity

- 描述

    设置投射物特效播放速度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | rate | number | 播放速度 |

- 返回值

    无

- 示例

```lua
-- 创建投射物对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local target_point = unit:get_point()
local projectile = y3.projectile.create({ key = 134274569, target = target_point })

projectile.handle:api_set_animation_speed(1.0)
```

---

## api_set_duration

method in ProjectileEntity

- 描述

    设置投射物持续时间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | duration | number | 持续时间 |

- 返回值

    无

- 示例

```lua
-- 创建投射物对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local target_point = unit:get_point()
local projectile = y3.projectile.create({ key = 134274569, target = target_point })

projectile.handle:api_set_duration(1.0)
```

---

## api_add_duration

method in ProjectileEntity

- 描述

    增加投射物持续时间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | extra_time | number | 持续时间变化值 |

- 返回值

    无

- 示例

```lua
-- 创建投射物对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local target_point = unit:get_point()
local projectile = y3.projectile.create({ key = 134274569, target = target_point })

projectile.handle:api_add_duration(1.0)
```

---

## api_get_left_time

method in ProjectileEntity

- 描述

    获取投射物剩余持续时间

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number? | 投射物剩余持续时间 |

- 示例

```lua
-- 创建投射物对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local target_point = unit:get_point()
local projectile = y3.projectile.create({ key = 134274569, target = target_point })

local result = projectile.handle:api_get_left_time()
```

---

## api_get_height

method in ProjectileEntity

- 描述

    获取投射物高度

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number? | 投射物高度 |

- 示例

```lua
-- 创建投射物对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local target_point = unit:get_point()
local projectile = y3.projectile.create({ key = 134274569, target = target_point })

local result = projectile.handle:api_get_height()
```

---

## api_get_face_angle

method in ProjectileEntity

- 描述

    获取投射物角度

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number? | 投射物的角度 |

- 示例

```lua
-- 创建投射物对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local target_point = unit:get_point()
local projectile = y3.projectile.create({ key = 134274569, target = target_point })

local result = projectile.handle:api_get_face_angle()
```

---

## api_get_position

method in ProjectileEntity

- 描述

    获取投射物位置

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3? | 投射物位置 |

- 示例

```lua
-- 创建投射物对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local target_point = unit:get_point()
local projectile = y3.projectile.create({ key = 134274569, target = target_point })

local result = projectile.handle:api_get_position()
```

---

## api_get_face_dir

method in ProjectileEntity

- 描述

    获取投射物朝向

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3? | 投射物朝向 |

- 示例

```lua
-- 创建投射物对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local target_point = unit:get_point()
local projectile = y3.projectile.create({ key = 134274569, target = target_point })

local result = projectile.handle:api_get_face_dir()
```

---

## api_raise_height

method in ProjectileEntity

- 描述

    投射物抬高

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | y | py.Fixed | 定点数 |

- 返回值

    无

- 示例

```lua
-- 创建投射物对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local target_point = unit:get_point()
local projectile = y3.projectile.create({ key = 134274569, target = target_point })

projectile.handle:api_raise_height(Fix32(1))
```

---

## api_get_str_attr

method in ProjectileEntity

- 描述

    获取投射物的字符串属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr_name | string | 属性名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string? | 字符串类型返回值 |

- 示例

```lua
-- 创建投射物对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local target_point = unit:get_point()
local projectile = y3.projectile.create({ key = 134274569, target = target_point })

local result = projectile.handle:api_get_str_attr("attr_name")
```

---

## api_set_str_attr

method in ProjectileEntity

- 描述

    设置投射物的字符串属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr_name | string | 属性名称 |
    | value | string | 属性取值 |

- 返回值

    无

- 示例

```lua
-- 创建投射物对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local target_point = unit:get_point()
local projectile = y3.projectile.create({ key = 134274569, target = target_point })

projectile.handle:api_set_str_attr("attr_name", "value")
```

---

## api_add_tag

method in ProjectileEntity

- 描述

    投射物添加键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | TAG |

- 返回值

    无

- 示例

```lua
-- 创建投射物对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local target_point = unit:get_point()
local projectile = y3.projectile.create({ key = 134274569, target = target_point })

projectile.handle:api_add_tag("tag")
```

---

## api_remove_tag

method in ProjectileEntity

- 描述

    投射物移除键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | TAG |

- 返回值

    无

- 示例

```lua
-- 创建投射物对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local target_point = unit:get_point()
local projectile = y3.projectile.create({ key = 134274569, target = target_point })

projectile.handle:api_remove_tag("tag")
```

---

## api_play_sound_by_proj_for_role_relation

method in ProjectileEntity

- 描述

    对投射物所属单位的所属玩家关系播放音乐

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | camp_target | py.RoleRelation | 玩家关系 |
    | sid | py.AudioKey | 乐曲编号 |
    | loop | boolean | 是否循环 |

- 返回值

    无

- 示例

```lua
-- 创建投射物对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local target_point = unit:get_point()
local projectile = y3.projectile.create({ key = 134274569, target = target_point })
local relation = 1
local audio_key = 134274569

projectile.handle:api_play_sound_by_proj_for_role_relation(relation, audio_key, true)
```

---

## get_projectile_role

method in ProjectileEntity

- 描述

    获取投射物的玩家

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Role? | 玩家 |

- 示例

```lua
-- 创建投射物对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local target_point = unit:get_point()
local projectile = y3.projectile.create({ key = 134274569, target = target_point })

local result = projectile.handle:get_projectile_role()
```

---

## api_set_projectile_visible

method in ProjectileEntity

- 描述

    设置投射物对玩家的可见性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家/玩家组 |
    | is_visible | boolean | 是否可见 |

- 返回值

    无

- 示例

```lua
-- 创建投射物对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local target_point = unit:get_point()
local projectile = y3.projectile.create({ key = 134274569, target = target_point })
local player = y3.player.get_by_id(1)

projectile.handle:api_set_projectile_visible(player.handle, true)
```

---
