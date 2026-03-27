---
sidebarDepth: 1
---
# Road (场景对象)

# 索引

Y3 编辑器 Road 封装接口，提供高级方法操作 Road 对象。

---

| 接口 | 描述 |
| --- | --- |
| [get_road_by_res_id](#get_road_by_res_id) |  |
| [get_by_handle](#get_by_handle) |  |
| [has_tag](#has_tag) | 路径是否有tag |
| [remove_path](#remove_path) | 删除路径 |
| [add_point](#add_point) | 给路径添加点 |
| [remove_point](#remove_point) | 给路径移除点 |
| [add_tag](#add_tag) | 给路径添加标签 |
| [remove_tag](#remove_tag) | 给路径移除标签 |
| [get_point_count](#get_point_count) | 获取路径中点的个数 |
| [create_path](#create_path) | 以点为起点创建路径 |
| [get_path_areas_by_tag](#get_path_areas_by_tag) | 按标签获取所有的路径 |

---

## get_road_by_res_id

method in Road

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | res_id | integer |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Road |  |

- 示例

```lua
local result = y3.road.get_road_by_res_id(1)
```

---

## get_by_handle

method in Road

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | py_road | py.Road |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Road |  |

- 示例

```lua
local result = y3.road.get_by_handle(road)
```

---

## has_tag

method in Road

- 描述

    路径是否有tag

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
local road = y3.road.get_road_by_res_id(1)

local result = road:has_tag("tag")
```

---

## remove_path

method in Road

- 描述

    删除路径

- 参数

    无

- 返回值

    无

- 示例

```lua
local road = y3.road.get_road_by_res_id(1)

road:remove_path()
```

---

## add_point

method in Road

- 描述

    给路径添加点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | index | integer | 序号 |
    | point | Point | 点 |

- 返回值

    无

- 示例

```lua
local road = y3.road.get_road_by_res_id(1)
local point = y3.point(0, 0)

road:add_point(1, point)
```

---

## remove_point

method in Road

- 描述

    给路径移除点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | index | integer | 序号 |

- 返回值

    无

- 示例

```lua
local road = y3.road.get_road_by_res_id(1)

road:remove_point(1)
```

---

## add_tag

method in Road

- 描述

    给路径添加标签

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | 序号 |

- 返回值

    无

- 示例

```lua
local road = y3.road.get_road_by_res_id(1)

road:add_tag("tag")
```

---

## remove_tag

method in Road

- 描述

    给路径移除标签

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | 序号 |

- 返回值

    无

- 示例

```lua
local road = y3.road.get_road_by_res_id(1)

road:remove_tag("tag")
```

---

## get_point_count

method in Road

- 描述

    获取路径中点的个数

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer |  |

- 示例

```lua
local road = y3.road.get_road_by_res_id(1)

local result = road:get_point_count()
```

---

## create_path

method in Road

- 描述

    以点为起点创建路径

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | start_point | Point | 起点 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Road |  |

- 示例

```lua
local point = y3.point(0, 0)

local result = y3.road.create_path(point)
```

---

## get_path_areas_by_tag

method in Road

- 描述

    按标签获取所有的路径

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | 标签 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Road[] |  |

- 示例

```lua
local result = y3.road.get_path_areas_by_tag("tag")
```

---
