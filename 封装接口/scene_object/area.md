---
sidebarDepth: 1
---
# Area (场景对象)

# 索引

Y3 编辑器 Area 封装接口，提供高级方法操作 Area 对象。

---

| 接口 | 描述 |
| --- | --- |
| [get_by_handle](#get_by_handle) | 根据py对象创建区域 |
| [get_by_res_id](#get_by_res_id) |  |
| [get_circle_by_res_id](#get_circle_by_res_id) | 根据场景id获得圆形区域 |
| [get_rectangle_by_res_id](#get_rectangle_by_res_id) | 根据场景id获得矩形区域 |
| [get_polygon_by_res_id](#get_polygon_by_res_id) | 根据场景id获得多边形区域 |
| [remove](#remove) | 删除区域 |
| [set_collision](#set_collision) | 设置区域碰撞 |
| [add_tag](#add_tag) | 给区域添加标签 |
| [remove_tag](#remove_tag) | 给区域移除标签 |
| [has_tag](#has_tag) | 区域是否有tag |
| [set_visible](#set_visible) | 设置多边形区域对玩家可见性 |
| [set_radius](#set_radius) | 设置圆形区域半径 |
| [set_size](#set_size) | 设置矩形区域半径 |
| [get_radius](#get_radius) | 获得圆形区域半径 |
| [get_min_x](#get_min_x) | 获取区域内最小X坐标 |
| [get_min_y](#get_min_y) | 获取区域内最小Y坐标 |
| [get_max_x](#get_max_x) | 获取区域内最大X坐标 |
| [get_max_y](#get_max_y) | 获取区域内最大Y坐标 |
| [get_center_point](#get_center_point) | 获取中心点 |
| [random_point](#random_point) | 获取随机点 |
| [get_weather](#get_weather) | 获得区域天气 |
| [get_all_unit_in_area](#get_all_unit_in_area) | 区域内的所有单位 |
| [get_unit_in_area_by_camp](#get_unit_in_area_by_camp) | 区域内阵营所有单位 |
| [get_unit_group_in_area](#get_unit_group_in_area) | 区域内玩家单位(单位组) |
| [get_unit_num_in_area](#get_unit_num_in_area) | 区域中单位的数量 |
| [edit_area_collision](#edit_area_collision) | 编辑区域碰撞 |
| [edit_area_fov_block](#edit_area_fov_block) | 编辑区域视野阻挡 |
| [is_point_in_area](#is_point_in_area) | 点是否在区域内 |
| [get_map_area](#get_map_area) | 获取完整地图区域 |
| [get_rectangle_area_last_created](#get_rectangle_area_last_created) | 获得最后创建的矩形区域 |
| [create_circle_area](#create_circle_area) | 创建圆形区域 |
| [create_rectangle_area](#create_rectangle_area) | 创建矩形区域 |
| [create_rectangle_area_from_two_points](#create_rectangle_area_from_two_points) | 以起点终点创建矩形区域 |
| [create_polygon_area_by_points](#create_polygon_area_by_points) | 沿点创建多边形 |
| [get_circle_areas_by_tag](#get_circle_areas_by_tag) | 按标签获取所有的圆形区域 |
| [get_rect_areas_by_tag](#get_rect_areas_by_tag) | 按标签获取所有的矩形区域 |
| [get_polygon_areas_by_tag](#get_polygon_areas_by_tag) | 按标签获取所有的多边形区域 |
| [get_polygon_areas_point_list](#get_polygon_areas_point_list) | 获取多边形的所有顶点 |

---

## get_by_handle

method in Area

- 描述

    根据py对象创建区域

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | py_area | py.Area | py层对象 |
    | shape? | Area.Shape | 见area.enum |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Area |  |

- 示例

```lua
local area = y3.area.create_circle_area(y3.point(0, 0), 500)

local result = y3.area.get_by_handle(area.handle)
```

---

## get_by_res_id

method in Area

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | res_id | py.AreaID | 编辑场景中的id |
    | shape? | Area.Shape | 见area.enum |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Area |  |

- 示例

```lua
local area_id = 1

local result = y3.area.get_by_res_id(area_id)
```

---

## get_circle_by_res_id

method in Area

- 描述

    根据场景id获得圆形区域

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | res_id | py.AreaID | 编辑场景中的id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Area |  |

- 示例

```lua
local area_id = 1

local result = y3.area.get_circle_by_res_id(area_id)
```

---

## get_rectangle_by_res_id

method in Area

- 描述

    根据场景id获得矩形区域

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | res_id | py.AreaID | 编辑场景中的id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Area |  |

- 示例

```lua
local area_id = 1

local result = y3.area.get_rectangle_by_res_id(area_id)
```

---

## get_polygon_by_res_id

method in Area

- 描述

    根据场景id获得多边形区域

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | res_id | py.AreaID | 编辑场景中的id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Area |  |

- 示例

```lua
local area_id = 1

local result = y3.area.get_polygon_by_res_id(area_id)
```

---

## remove

method in Area

- 描述

    删除区域

- 参数

    无

- 返回值

    无

- 示例

```lua
local area = y3.area.create_circle_area(y3.point(0, 0), 500)

area:remove()
```

---

## set_collision

method in Area

- 描述

    设置区域碰撞

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_collision_effect | boolean | 碰撞是否生效 |
    | is_land_effect | boolean | 地面碰撞开关 |
    | is_air_effect | boolean | 空中碰撞开关 |

- 返回值

    无

- 示例

```lua
local area = y3.area.create_circle_area(y3.point(0, 0), 500)

area:set_collision(true, true, true)
```

---

## add_tag

method in Area

- 描述

    给区域添加标签

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | tag |

- 返回值

    无

- 示例

```lua
local area = y3.area.create_circle_area(y3.point(0, 0), 500)

area:add_tag("tag")
```

---

## remove_tag

method in Area

- 描述

    给区域移除标签

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | tag |

- 返回值

    无

- 示例

```lua
local area = y3.area.create_circle_area(y3.point(0, 0), 500)

area:remove_tag("tag")
```

---

## has_tag

method in Area

- 描述

    区域是否有tag

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | tag |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean |  |

- 示例

```lua
local area = y3.area.create_circle_area(y3.point(0, 0), 500)

local result = area:has_tag("tag")
```

---

## set_visible

method in Area

- 描述

    设置多边形区域对玩家可见性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | is_visibility | boolean | 是否开启视野 |
    | is_real_visibility | boolean | 是否开启真实视野 |

- 返回值

    无

- 示例

```lua
local area = y3.area.create_circle_area(y3.point(0, 0), 500)
local player = y3.player.get_by_id(1)

area:set_visible(player, true, true)
```

---

## set_radius

method in Area

- 描述

    设置圆形区域半径

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | radius | number | 半径 |

- 返回值

    无

- 示例

```lua
local area = y3.area.create_circle_area(y3.point(0, 0), 500)

area:set_radius(1.0)
```

---

## set_size

method in Area

- 描述

    设置矩形区域半径

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | horizontal_length | number | 长度 |
    | vertical_length | number | 宽度 |

- 返回值

    无

- 示例

```lua
local area = y3.area.create_circle_area(y3.point(0, 0), 500)

area:set_size(1.0, 1.0)
```

---

## get_radius

method in Area

- 描述

    获得圆形区域半径

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number |  |

- 示例

```lua
local area = y3.area.create_circle_area(y3.point(0, 0), 500)

local result = area:get_radius()
```

---

## get_min_x

method in Area

- 描述

    获取区域内最小X坐标

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number |  |

- 示例

```lua
local area = y3.area.create_circle_area(y3.point(0, 0), 500)

local result = area:get_min_x()
```

---

## get_min_y

method in Area

- 描述

    获取区域内最小Y坐标

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number |  |

- 示例

```lua
local area = y3.area.create_circle_area(y3.point(0, 0), 500)

local result = area:get_min_y()
```

---

## get_max_x

method in Area

- 描述

    获取区域内最大X坐标

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number |  |

- 示例

```lua
local area = y3.area.create_circle_area(y3.point(0, 0), 500)

local result = area:get_max_x()
```

---

## get_max_y

method in Area

- 描述

    获取区域内最大Y坐标

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number |  |

- 示例

```lua
local area = y3.area.create_circle_area(y3.point(0, 0), 500)

local result = area:get_max_y()
```

---

## get_center_point

method in Area

- 描述

    获取中心点

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Point |  |

- 示例

```lua
local area = y3.area.create_circle_area(y3.point(0, 0), 500)

local result = area:get_center_point()
```

---

## random_point

method in Area

- 描述

    获取随机点

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Point |  |

- 示例

```lua
local area = y3.area.create_circle_area(y3.point(0, 0), 500)

local result = area:random_point()
```

---

## get_weather

method in Area

- 描述

    获得区域天气

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer |  |

- 示例

```lua
local area = y3.area.create_circle_area(y3.point(0, 0), 500)

local result = area:get_weather()
```

---

## get_all_unit_in_area

method in Area

- 描述

    区域内的所有单位

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Unit[] |  |

- 示例

```lua
local area = y3.area.create_circle_area(y3.point(0, 0), 500)

local result = area:get_all_unit_in_area()
```

---

## get_unit_in_area_by_camp

method in Area

- 描述

    区域内阵营所有单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | camp | py.Camp |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Unit[] |  |

- 示例

```lua
local area = y3.area.create_circle_area(y3.point(0, 0), 500)
local camp = GameAPI.get_camp_by_camp_id(1)

local result = area:get_unit_in_area_by_camp(camp)
```

---

## get_unit_group_in_area

method in Area

- 描述

    区域内玩家单位(单位组)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | UnitGroup |  |

- 示例

```lua
local area = y3.area.create_circle_area(y3.point(0, 0), 500)
local player = y3.player.get_by_id(1)

local result = area:get_unit_group_in_area(player)
```

---

## get_unit_num_in_area

method in Area

- 描述

    区域中单位的数量

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer |  |

- 示例

```lua
local area = y3.area.create_circle_area(y3.point(0, 0), 500)

local result = area:get_unit_num_in_area()
```

---

## edit_area_collision

method in Area

- 描述

    编辑区域碰撞

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | collision_layer | integer | 碰撞类型 |
    | is_add | boolean | 添加/去除 |

- 返回值

    无

- 示例

```lua
local area = y3.area.create_circle_area(y3.point(0, 0), 500)

area:edit_area_collision(1, true)
```

---

## edit_area_fov_block

method in Area

- 描述

    编辑区域视野阻挡

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | fov_block_type | integer | 视野阻挡类型 |
    | is_add | boolean | 添加/去除 |

- 返回值

    无

- 示例

```lua
local area = y3.area.create_circle_area(y3.point(0, 0), 500)

area:edit_area_fov_block(1, true)
```

---

## is_point_in_area

method in Area

- 描述

    点是否在区域内

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | Point | 点 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean |  |

- 示例

```lua
local area = y3.area.create_circle_area(y3.point(0, 0), 500)
local point = y3.point(0, 0)

local result = area:is_point_in_area(point)
```

---

## get_map_area

method in Area

- 描述

    获取完整地图区域

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Area |  |

- 示例

```lua
local result = y3.area.get_map_area()
```

---

## get_rectangle_area_last_created

method in Area

- 描述

    获得最后创建的矩形区域

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Area |  |

- 示例

```lua
local result = y3.area.get_rectangle_area_last_created()
```

---

## create_circle_area

method in Area

- 描述

    创建圆形区域

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | Point | 点 |
    | radius | number | 半径 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Area |  |

- 示例

```lua
local point = y3.point(0, 0)

local result = y3.area.create_circle_area(point, 1.0)
```

---

## create_rectangle_area

method in Area

- 描述

    创建矩形区域

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | Point | 点 |
    | horizontal_length | number | 长度 |
    | vertical_length | number | 宽度 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Area | 矩形区域 |

- 示例

```lua
local point = y3.point(0, 0)

local result = y3.area.create_rectangle_area(point, 1.0, 1.0)
```

---

## create_rectangle_area_from_two_points

method in Area

- 描述

    以起点终点创建矩形区域

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point_one | Point | 点1 |
    | point_two | Point | 点2 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Area | 矩形区域 |

- 示例

```lua
local point = y3.point(0, 0)

local result = y3.area.create_rectangle_area_from_two_points(point, point)
```

---

## create_polygon_area_by_points

method in Area

- 描述

    沿点创建多边形

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Area | 多边形区域 |

- 示例

```lua
local result = y3.area.create_polygon_area_by_points()
```

---

## get_circle_areas_by_tag

method in Area

- 描述

    按标签获取所有的圆形区域

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | 标签 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Area[] | 矩形区域 |

- 示例

```lua
local result = y3.area.get_circle_areas_by_tag("tag")
```

---

## get_rect_areas_by_tag

method in Area

- 描述

    按标签获取所有的矩形区域

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | 标签 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Area[] | 矩形区域表 |

- 示例

```lua
local result = y3.area.get_rect_areas_by_tag("tag")
```

---

## get_polygon_areas_by_tag

method in Area

- 描述

    按标签获取所有的多边形区域

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | 标签 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Area[] | 多边形区域表 |

- 示例

```lua
local result = y3.area.get_polygon_areas_by_tag("tag")
```

---

## get_polygon_areas_point_list

method in Area

- 描述

    获取多边形的所有顶点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | polygon | Area | 多边形区域 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | table | 多边形顶点表 |

- 示例

```lua
local area = y3.area.create_circle_area(y3.point(0, 0), 500)

local result = y3.area.get_polygon_areas_point_list(area)
```

---
