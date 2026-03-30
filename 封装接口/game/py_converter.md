---
sidebarDepth: 1
---
# PYConverter (Game)

# 索引

Y3 编辑器 PYConverter 游戏接口，提供游戏相关功能。

---

| 接口 | 描述 |
| --- | --- |
| [py_to_lua](#py_to_lua) |  |
| [py_to_lua_by_lua_type](#py_to_lua_by_lua_type) |  |
| [lua_to_py](#lua_to_py) |  |
| [lua_to_py_by_lua_type](#lua_to_py_by_lua_type) |  |
| [lua_to_py_factory](#lua_to_py_factory) |  |
| [py_to_lua_factory](#py_to_lua_factory) |  |
| [register_py_to_lua](#register_py_to_lua) |  |
| [register_lua_to_py](#register_lua_to_py) |  |
| [get_py_type](#get_py_type) |  |
| [register_type_alias](#register_type_alias) |  |

---

## py_to_lua

method in PYConverter

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | py_type | string |  |
    | py_value | any |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | any |  |

- 示例

```lua
local result = y3.py_converter.py_to_lua("py_type", "py_value")
```

---

## py_to_lua_by_lua_type

method in PYConverter

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | lua_type | string |  |
    | py_value | any |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | any |  |

- 示例

```lua
local result = y3.py_converter.py_to_lua_by_lua_type("lua_type", "py_value")
```

---

## lua_to_py

method in PYConverter

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | py_type | string |  |
    | lua_value | any |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | any |  |

- 示例

```lua
local result = y3.py_converter.lua_to_py("py_type", "lua_value")
```

---

## lua_to_py_by_lua_type

method in PYConverter

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | lua_type | string |  |
    | lua_value | any |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | any |  |

- 示例

```lua
local result = y3.py_converter.lua_to_py_by_lua_type("lua_type", "lua_value")
```

---

## lua_to_py_factory

method in PYConverter

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | py_type | string |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | fun(py_value:any):any |  |

- 示例

```lua
local result = y3.py_converter.lua_to_py_factory("py_type")
```

---

## py_to_lua_factory

method in PYConverter

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | py_type | string |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | fun(lua_value:any):any |  |

- 示例

```lua
local result = y3.py_converter.py_to_lua_factory("py_type")
```

---

## register_py_to_lua

method in PYConverter

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | py_type | string |  |
    | converter | fun(py_value:any):any |  |

- 返回值

    无

- 示例

```lua
local result = y3.py_converter.register_py_to_lua("py_type", function() end)
```

---

## register_lua_to_py

method in PYConverter

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | py_type | string |  |
    | converter | fun(lua_value:any):any |  |

- 返回值

    无

- 示例

```lua
local result = y3.py_converter.register_lua_to_py("py_type", function() end)
```

---

## get_py_type

method in PYConverter

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | type_name | string |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string |  |

- 示例

```lua
local result = y3.py_converter.get_py_type("type_name")
```

---

## register_type_alias

method in PYConverter

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | py_type_name | string |  |
    | lua_type_name | string |  |

- 返回值

    无

- 示例

```lua
local result = y3.py_converter.register_type_alias("py_type_name", "lua_type_name")
```

---
