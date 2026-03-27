---
sidebarDepth: 1
---
# Beam (运行时对象)

# 索引

Y3 编辑器 Beam 封装接口，提供高级方法操作 Beam 对象。

---

| 接口 | 描述 |
| --- | --- |
| [create_lua_beam_by_py](#create_lua_beam_by_py) |  |
| [create](#create) |  |
| [remove](#remove) | 链接特效 - 销毁 |
| [set_speed](#set_speed) | 设置播放速度 |
| [show](#show) | 链接特效 - 显示/隐藏 |
| [set](#set) | 链接特效 - 设置位置 |

---

## create_lua_beam_by_py

method in Beam

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | py_beam | py.LinkSfx |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Beam |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local link_sfx = GameAPI.create_link_sfx_from_unit_to_point(134274569, unit.handle, "origin", GlobalAPI.coord_to_point(Fix32(100), Fix32(100), Fix32(0)), Fix32(0))

local result = y3.beam.create_lua_beam_by_py(link_sfx)
```

---

## create

method in Beam

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | data | Beam.CreateData |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Beam |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local data = { key = 134274569, source = unit, target = y3.point(0, 0) }

local result = y3.beam.create(data)
```

---

## remove

method in Beam

- 描述

    链接特效 - 销毁

- 参数

    无

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local beam = y3.beam.create({ key = 134274569, source = unit, target = y3.point(0, 0) })

beam:remove()
```

---

## set_speed

method in Beam

- 描述

    设置播放速度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | speed | number | 播放速度 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local beam = y3.beam.create({ key = 134274569, source = unit, target = y3.point(0, 0) })

beam:set_speed(1.0)
```

---

## show

method in Beam

- 描述

    链接特效 - 显示/隐藏

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_show | boolean | 是否显示 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local beam = y3.beam.create({ key = 134274569, source = unit, target = y3.point(0, 0) })

beam:show(true)
```

---

## set

method in Beam

- 描述

    链接特效 - 设置位置

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | data | Beam.LinkData |  |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local beam = y3.beam.create({ key = 134274569, source = unit, target = y3.point(0, 0) })
local data = { point_type = y3.const.LinkSfxPointType.START, target = y3.point(0, 0) }

beam:set(data)
```

---
