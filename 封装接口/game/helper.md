---
sidebarDepth: 1
---
# Helper (Game)

# 索引

Y3 编辑器 Helper 游戏接口，提供游戏相关功能。

---

| 接口 | 描述 |
| --- | --- |
| [unpack_list](#unpack_list) |  |
| [pack_list](#pack_list) |  |
| [tonumber](#tonumber) |  |
| [number_type](#number_type) |  |
| [as_lua](#as_lua) |  |
| [as_py](#as_py) |  |
| [py_dict](#py_dict) |  |
| [py_tuple](#py_tuple) |  |
| [dict_to_table](#dict_to_table) | 将py.Dict转换为table |
| [tuple_to_table](#tuple_to_table) |  |
| [py_to_table](#py_to_table) |  |
| [table_to_py](#table_to_py) |  |

---

## unpack_list

method in Helper

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | py_list | py.List |  |
    | wrapper? | fun(py_object: | any): any |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | any[] |  |

- 示例

```lua
local list = {}
    
local result = y3.helper.unpack_list(list)
```

---

## pack_list

method in Helper

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | lua_list | any[] |  |
    | unwrapper? | fun(lua_object: | any): any |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DynamicTypeMeta[] |  |

- 示例

```lua
local result = y3.helper.pack_list({"str1", "str2"})
```

---

## tonumber

method in Helper

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n? | y3.Number |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number? |  |

- 示例

```lua
local result = y3.helper.tonumber()
```

---

## number_type

method in Helper

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | n? | y3.Number \| any |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | 'number' | | 'Fix32' | 'XDouble' | nil |

- 示例

```lua
local result = y3.helper.number_type()
```

---

## as_lua

method in Helper

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | v | any |  |
    | recursive? | boolean |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | any |  |

- 示例

```lua
local result = y3.helper.as_lua("v", true)
```

---

## as_py

method in Helper

- 描述

    

- 参数

    无

- 返回值

    无

- 示例

```lua
y3.game.as_py()
```

---

## py_dict

method in Helper

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | t? | table |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Dict |  |

- 示例

```lua
local result = y3.helper.py_dict({})
```

---

## py_tuple

method in Helper

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | t? | any[] |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Tuple |  |

- 示例

```lua
local result = y3.helper.py_tuple({1, 2, 3})
```

---

## dict_to_table

method in Helper

- 描述

    将py.Dict转换为table

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | dict | py.Dict |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | table |  |

- 示例

```lua
local dict = y3.helper.py_dict({key1 = 1})

local result = y3.helper.dict_to_table(dict)
```

---

## tuple_to_table

method in Helper

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tuple | py.Tuple |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | table |  |

- 示例

```lua
local tuple = y3.helper.py_tuple({1, 2, 3})

local result = y3.helper.tuple_to_table(tuple)
```

---

## py_to_table

method in Helper

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | py_object | any |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | table |  |

- 示例

```lua
local result = y3.helper.py_to_table("py_object")
```

---

## table_to_py

method in Helper

- 描述

    

- 参数

    无

- 返回值

    无

- 示例

```lua
y3.helper.table_to_py()
```

---
