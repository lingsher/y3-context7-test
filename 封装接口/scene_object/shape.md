---
sidebarDepth: 1
---
# Shape (场景对象)

# 索引

Y3 编辑器 Shape 封装接口，提供高级方法操作 Shape 对象。

---

| 接口 | 描述 |
| --- | --- |
| [get_by_handle](#get_by_handle) |  |
| [create_annular_shape](#create_annular_shape) | 创建环形区域 |
| [create_circular_shape](#create_circular_shape) | 创建圆形区域 |
| [create_rectangle_shape](#create_rectangle_shape) | 创建矩形区域 |
| [create_sector_shape](#create_sector_shape) | 扇形 |

---

## get_by_handle

method in Shape

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | py_shape | py.Shape |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Shape |  |

- 示例

```lua
local result = y3.shape.get_by_handle(shape)
```

---

## create_annular_shape

method in Shape

- 描述

    创建环形区域

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | in_radius | number | 内半径 |
    | out_radius | number | 外半径 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Shape |  |

- 示例

```lua
local result = y3.shape.create_annular_shape(1.0, 1.0)
```

---

## create_circular_shape

method in Shape

- 描述

    创建圆形区域

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | radius | number | 半径 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Shape |  |

- 示例

```lua
local result = y3.shape.create_circular_shape(1.0)
```

---

## create_rectangle_shape

method in Shape

- 描述

    创建矩形区域

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | width | number | 宽度 |
    | length | number | 长度 |
    | angle | number | 角度 |
    | offset_x_ratio? | number | 偏移x |
    | offset_y_ratio? | number | 偏移y |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Shape |  |

- 示例

```lua
local result = y3.shape.create_rectangle_shape(1.0, 1.0, 1.0, 1.0, 1.0)
```

---

## create_sector_shape

method in Shape

- 描述

    扇形

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | radius | number | 半径 |
    | angle | number | 角度 |
    | direction | number | 方向 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Shape |  |

- 示例

```lua
local result = y3.shape.create_sector_shape(1.0, 1.0, 1.0)
```

---
