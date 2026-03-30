---
sidebarDepth: 1
---
# Mover (运行时对象)

# 索引

Y3 编辑器 Mover 封装接口，提供高级方法操作 Mover 对象。

---

| 接口 | 描述 |
| --- | --- |
| [get_by_handle](#get_by_handle) |  |
| [stop](#stop) | 打断运动器 |
| [remove](#remove) | 移除运动器 |
| [mover_line](#mover_line) |  |
| [mover_target](#mover_target) |  |
| [mover_curve](#mover_curve) |  |
| [mover_round](#mover_round) |  |

---

## get_by_handle

method in Mover

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | py_mover | py.Mover |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Mover |  |

- 示例

```lua
local result = y3.mover.get_by_handle(mover)
```

---

## stop

method in Mover

- 描述

    打断运动器

- 参数

    无

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local mover = unit:create_mover_line(500, 0)

mover:stop()
```

---

## remove

method in Mover

- 描述

    移除运动器

- 参数

    无

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local mover = unit:create_mover_line(500, 0)

mover:remove()
```

---

## mover_line

method in Mover

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | mover_unit | Unit\|Projectile\|Particle |  |
    | mover_data | Mover.CreateData.Line |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Mover |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local mover_data = { angle = 0, distance = 500, speed = 300 }

local result = y3.mover.mover_line(mover_unit, mover_data)
```

---

## mover_target

method in Mover

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | mover_unit | Unit\|Projectile\|Particle |  |
    | mover_data | Mover.CreateData.Target |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Mover |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local target_unit = y3.player.get_by_id(1):get_all_units()[1]
local mover_data = { target = target_unit, speed = 300, target_distance = 50 }

local result = y3.mover.mover_target(mover_unit, mover_data)
```

---

## mover_curve

method in Mover

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | mover_unit | Unit\|Projectile\|Particle |  |
    | mover_data | Mover.CreateData.Curve |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Mover |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local mover_data = { angle = 0, distance = 500, speed = 300, path = { y3.point(100, 100) } }

local result = y3.mover.mover_curve(mover_unit, mover_data)
```

---

## mover_round

method in Mover

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | mover_unit | Unit\|Projectile\|Particle |  |
    | mover_data | Mover.CreateData.Round |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Mover |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local mover_data = { angle = 0, radius = 300, speed = 300, clock_wise = true }

local result = y3.mover.mover_round(mover_unit, mover_data)
```

---
