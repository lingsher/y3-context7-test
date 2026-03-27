---
sidebarDepth: 1
---
# Point (场景对象)

# 索引

Y3 编辑器 Point 封装接口，提供高级方法操作 Point 对象。

---

| 接口 | 描述 |
| --- | --- |
| [get_point_by_res_id](#get_point_by_res_id) |  |
| [get_by_handle](#get_by_handle) | 根据py对象创建点 |
| [get_x](#get_x) | 点的x坐标 |
| [get_y](#get_y) | 点的y坐标 |
| [get_z](#get_z) | 点的z坐标 |
| [get_point](#get_point) |  |
| [move](#move) | 移动点 |
| [create](#create) | 坐标转化为点 |
| [get_point_offset_vector](#get_point_offset_vector) | 点向方向偏移 |
| [get_point_in_path](#get_point_in_path) | 路径中的点 |
| [get_angle_with](#get_angle_with) | 获取与另一个点的方向 |
| [get_distance_with](#get_distance_with) | 获取与另一个点的距离 |
| [get_random_point](#get_random_point) | 获取圆形范围内的随机点 |

---

## get_point_by_res_id

method in Point

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | res_id | integer |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Point |  |

- 示例

```lua
local result = y3.point.get_point_by_res_id(1)
```

---

## get_by_handle

method in Point

- 描述

    根据py对象创建点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | py_point | Point.HandleType |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Point |  |

- 示例

```lua
local result = y3.point.get_by_handle(py_point)
```

---

## get_x

method in Point

- 描述

    点的x坐标

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number |  |

- 示例

```lua
local point = y3.point(100, 200)

local result = point:get_x()
```

---

## get_y

method in Point

- 描述

    点的y坐标

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number |  |

- 示例

```lua
local point = y3.point(100, 200)

local result = point:get_y()
```

---

## get_z

method in Point

- 描述

    点的z坐标

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number |  |

- 示例

```lua
local point = y3.point(100, 200)

local result = point:get_z()
```

---

## get_point

method in Point

- 描述

    

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Point |  |

- 示例

```lua
local point = y3.point(100, 200)

local result = point:get_point()
```

---

## move

method in Point

- 描述

    移动点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | x | number? |  |
    | y | number? |  |
    | z | number? |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Point |  |

- 示例

```lua
local point = y3.point(100, 200)

local result = point:move(nil, nil, nil)
```

---

## create

method in Point

- 描述

    坐标转化为点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | x | number | 点X坐标 |
    | y | number | 点Y坐标 |
    | z? | number | 点Z坐标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Point |  |

- 示例

```lua
local result = y3.point.create(1.0, 1.0, 1.0)
```

---

## get_point_offset_vector

method in Point

- 描述

    点向方向偏移

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | Point | 点 |
    | direction | number | 偏移方向点 |
    | offset | number | 偏移量 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Point |  |

- 示例

```lua
local point = y3.point(0, 0)

local result = y3.point.get_point_offset_vector(point, 1.0, 1.0)
```

---

## get_point_in_path

method in Point

- 描述

    路径中的点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | path | table | 目标路径 |
    | index | integer | 索引 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Point |  |

- 示例

```lua
local result = y3.point.get_point_in_path({}, 1)
```

---

## get_angle_with

method in Point

- 描述

    获取与另一个点的方向

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | other | Point |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number |  |

- 示例

```lua
local point = y3.point(100, 200)

local result = point:get_angle_with(point)
```

---

## get_distance_with

method in Point

- 描述

    获取与另一个点的距离

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | other | Point |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number |  |

- 示例

```lua
local point = y3.point(100, 200)

local result = point:get_distance_with(point)
```

---

## get_random_point

method in Point

- 描述

    获取圆形范围内的随机点

- 参数

    无

- 返回值

    无

- 示例

```lua
local point = y3.point(100, 200)

point:get_random_point()
```

---
