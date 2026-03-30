---
sidebarDepth: 1
---
# Light (场景对象)

# 索引

Y3 编辑器 Light 封装接口，提供高级方法操作 Light 对象。

---

| 接口 | 描述 |
| --- | --- |
| [get_point_light_by_res_id](#get_point_light_by_res_id) | 根据场景id获得点光源 |
| [get_spot_light_by_res_id](#get_spot_light_by_res_id) | 根据场景id获得聚光灯 |
| [create_lua_light_by_py](#create_lua_light_by_py) |  |
| [get_light_attribute](#get_light_attribute) | 获取光源属性 |
| [get_light_cast_shadow_state](#get_light_cast_shadow_state) | 获取光源是否产生阴影 |
| [create_point_light_at_point](#create_point_light_at_point) | 创建点光源到点 |
| [create_point_light_at_unit_socket](#create_point_light_at_unit_socket) | 创建点光源到单位挂接点 |
| [create_spot_light_to_point](#create_spot_light_to_point) | 创建方向光源到点 |
| [create_spot_light_at_unit_socket](#create_spot_light_at_unit_socket) | 创建方向光源到单位挂接点 |
| [remove_light](#remove_light) | 删除光源 |
| [set_shadow_casting_status](#set_shadow_casting_status) | 设置光源是否产生阴影 |
| [set_point_light_attribute](#set_point_light_attribute) | 设置点光源属性 |
| [set_directional_light_attribute](#set_directional_light_attribute) | 设置方向光源属性 |

---

## get_point_light_by_res_id

method in Light

- 描述

    根据场景id获得点光源

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | res_id | py.LightID | 编辑场景中的id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Light |  |

- 示例

```lua
local result = y3.light.get_point_light_by_res_id(134274569)
```

---

## get_spot_light_by_res_id

method in Light

- 描述

    根据场景id获得聚光灯

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | res_id | py.LightID | 编辑场景中的id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Light |  |

- 示例

```lua
local result = y3.light.get_spot_light_by_res_id(134274569)
```

---

## create_lua_light_by_py

method in Light

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | py_light | py.Light |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Light |  |

- 示例

```lua
local result = y3.light.create_lua_light_by_py(light)
```

---

## get_light_attribute

method in Light

- 描述

    获取光源属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 属性名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number |  |

- 示例

```lua
local light = y3.light.get_point_light_by_res_id(1)

local result = light:get_light_attribute("key")
```

---

## get_light_cast_shadow_state

method in Light

- 描述

    获取光源是否产生阴影

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean |  |

- 示例

```lua
local light = y3.light.get_point_light_by_res_id(1)

local result = light:get_light_cast_shadow_state()
```

---

## create_point_light_at_point

method in Light

- 描述

    创建点光源到点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | Point | 目标点 |
    | deviation_height | number | 偏移高度 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Light |  |

- 示例

```lua
local point = y3.point(0, 0)

local result = y3.light.create_point_light_at_point(point, 1.0)
```

---

## create_point_light_at_unit_socket

method in Light

- 描述

    创建点光源到单位挂接点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 目标单位 |
    | socket_name | string | 挂接点 |
    | deviation_height | number | 偏移高度 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Light |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = y3.light.create_point_light_at_unit_socket(unit, "socket_name", 1.0)
```

---

## create_spot_light_to_point

method in Light

- 描述

    创建方向光源到点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | Point | 目标点 |
    | pos_offset_y? | number | 偏移高度 |
    | unit_point_projectile? | Unit\|Point\|Projectile | 目标 |
    | target_offset_y? | number | 目标点偏移高度 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Light |  |

- 示例

```lua
local point = y3.point(0, 0)

local result = y3.light.create_spot_light_to_point(point, 1.0, unit, 1.0)
```

---

## create_spot_light_at_unit_socket

method in Light

- 描述

    创建方向光源到单位挂接点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 目标单位 |
    | socket_name | string | 挂接点 |
    | pos_offset_y? | number | 偏移高度 |
    | target_unit? | Unit | 目标单位 |
    | target_offset_y? | number | 目标点偏移高度 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Light |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = y3.light.create_spot_light_at_unit_socket(unit, "socket_name", 1.0, unit, 1.0)
```

---

## remove_light

method in Light

- 描述

    删除光源

- 参数

    无

- 返回值

    无

- 示例

```lua
local light = y3.light.get_point_light_by_res_id(1)

light:remove_light()
```

---

## set_shadow_casting_status

method in Light

- 描述

    设置光源是否产生阴影

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | boolean | 是否产生阴影 |

- 返回值

    无

- 示例

```lua
local light = y3.light.get_point_light_by_res_id(1)

light:set_shadow_casting_status(true)
```

---

## set_point_light_attribute

method in Light

- 描述

    设置点光源属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | light_attr_type | string \| y3.Const.PointLightAttribute | 属性名 |
    | value | number | 属性值 |

- 返回值

    无

- 示例

```lua
local light = y3.light.get_point_light_by_res_id(1)

light:set_point_light_attribute("light_attr_type", 1.0)
```

---

## set_directional_light_attribute

method in Light

- 描述

    设置方向光源属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | light_attr_type | string \| y3.Const.DirectionalLightAttribute | 属性名 |
    | value | number | 属性值 |

- 返回值

    无

- 示例

```lua
local light = y3.light.get_point_light_by_res_id(1)

light:set_directional_light_attribute("light_attr_type", 1.0)
```

---
