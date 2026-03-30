---
sidebarDepth: 1
---
# Math (Game)

# 索引

Y3 编辑器 Math 游戏接口，提供游戏相关功能。

---

| 接口 | 描述 |
| --- | --- |
| [get_random_angle](#get_random_angle) | 获取随机角度 |
| [random_float](#random_float) | 范围内随机实数 |
| [sin](#sin) | 正弦（角度制） |
| [cos](#cos) | 余弦（角度制） |
| [tan](#tan) | 正切（角度制） |
| [asin](#asin) | 反正弦（角度制） |
| [acos](#acos) | 反余弦（角度制） |
| [atan](#atan) | 反正切（角度制） |
| [includedAngle](#includedAngle) | 计算2个角度之间的夹角（角度制） |
| [isBetween](#isBetween) | 检查数字是否在[min, max]范围内 |
| [get_random_seed](#get_random_seed) | 获取随机种子 |

---

## get_random_angle

method in Math

- 描述

    获取随机角度

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number |  |

- 示例

```lua
local result = y3.math.get_random_angle()
```

---

## random_float

method in Math

- 描述

    范围内随机实数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | min | number | 范围内最小实数 |
    | max | number | 范围内最大实数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 随机实数 |

- 示例

```lua
local result = y3.math.random_float(1.0, 1.0)
```

---

## sin

method in Math

- 描述

    正弦（角度制）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | number | 实数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 实数 |

- 示例

```lua
local result = y3.math.sin(1.0)
```

---

## cos

method in Math

- 描述

    余弦（角度制）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | number | 实数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 实数 |

- 示例

```lua
local result = y3.math.cos(1.0)
```

---

## tan

method in Math

- 描述

    正切（角度制）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | number | 实数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 实数 |

- 示例

```lua
local result = y3.math.tan(1.0)
```

---

## asin

method in Math

- 描述

    反正弦（角度制）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | number | 实数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 实数 |

- 示例

```lua
local result = y3.math.asin(1.0)
```

---

## acos

method in Math

- 描述

    反余弦（角度制）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | number | 实数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 实数 |

- 示例

```lua
local result = y3.math.acos(1.0)
```

---

## atan

method in Math

- 描述

    反正切（角度制）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | y | number |  |
    | x | number |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 实数 |

- 示例

```lua
local result = y3.math.atan(1.0, 1.0)
```

---

## includedAngle

method in Math

- 描述

    计算2个角度之间的夹角（角度制）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | r1 | number |  |
    | r2 | number |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 夹角，取值范围[0, 180] |
    | number | 方向，1为顺时针，-1为逆时针 |

- 示例

```lua
local result = y3.math.includedAngle(1.0, 1.0)
```

---

## isBetween

method in Math

- 描述

    检查数字是否在[min, max]范围内

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | number | number |  |
    | min | number |  |
    | max | number |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean |  |

- 示例

```lua
local result = y3.math.isBetween(1.0, 1.0, 1.0)
```

---

## get_random_seed

method in Math

- 描述

    获取随机种子

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 随机种子 |

- 示例

```lua
local result = y3.math.get_random_seed()
```

---
