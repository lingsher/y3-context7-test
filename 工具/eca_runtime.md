---
sidebarDepth: 1
---
# ECARuntime (ECA运行时)

# 索引

ECA 运行时支持库，用于 ECA 转 Lua 时支持 ECA 的特殊写法。如果是直接使用 Lua 开发，可以使用更好的写法。

> ⚠️ **注意**：此库主要用于 ECA 转 Lua 的兼容层，直接使用 Lua 开发时不建议使用。

---

## 方法

| 接口 | 描述 |
| --- | --- |
| [evaluate](#evaluate) | 动态执行代码字符串 |
| [array](#array) | 创建带默认值的数组 |
| [variable](#variable) | 创建变量空间 |
| [tointeger](#tointeger) | 转换为整数 |
| [string](#string) | 拼接字符串 |

---

## evaluate

function in ECARuntime

- 描述

    动态执行代码字符串，支持参数传递。结果会被缓存以提高性能。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | code | string | 要执行的 Lua 代码字符串 |
    | ... | any | 传递给代码的参数（可通过 `args` 表访问） |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | any | 代码执行的返回值 |

- 示例

```lua
-- 执行简单表达式
local result = y3.rt.evaluate('return 1 + 2')
print(result)  -- 3
```

```lua
-- 使用参数
local result = y3.rt.evaluate('return args[1] + args[2]', 10, 20)
print(result)  -- 30
```

```lua
-- 执行复杂逻辑
local code = [[
    local a, b = args[1], args[2]
    if a > b then
        return a
    else
        return b
    end
]]
local max_value = y3.rt.evaluate(code, 5, 10)
print(max_value)  -- 10
```

---

## array

function in ECARuntime

- 描述

    创建一个带默认值的数组。当访问不存在的索引时，会自动返回并存储默认值。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | default | any | 默认值（可以是值或代码字符串） |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | table | 带默认值的数组 |

- 示例

```lua
-- 创建默认值为 0 的数组
local scores = y3.rt.array(0)
print(scores[1])  -- 0（自动填充默认值）
scores[1] = 100
print(scores[1])  -- 100
```

```lua
-- 创建默认值为空字符串的数组
local names = y3.rt.array('')
print(names[1])  -- ""
names[1] = '玩家1'
```

```lua
-- 使用代码字符串创建默认值为新表的数组
local players = y3.rt.array('{}')
players[1].name = '玩家1'
players[1].score = 100
players[2].name = '玩家2'  -- 自动创建新表
```

---

## variable

function in ECARuntime

- 描述

    创建变量空间，用于管理 ECA 变量的作用域和默认值。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | variables | table<string, any> | 变量定义表 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | ECARuntime.VariableSpace | 变量空间实例 |

- 示例

```lua
-- 创建变量空间
local var_space = y3.rt.variable({
    hp = 100,
    mp = 50,
    name = '英雄',
    items = y3.rt.array('{}'),
})

-- 创建新的变量实例
local vars = var_space:new()
print(vars.hp)    -- 100
print(vars.name)  -- 英雄

vars.hp = 80
print(vars.hp)    -- 80
```

---

## tointeger

function in ECARuntime

- 描述

    将值转换为整数，无法转换时返回 0。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | v | any | 要转换的值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 转换后的整数 |

- 示例

```lua
print(y3.rt.tointeger(3.7))    -- 3
print(y3.rt.tointeger('10'))   -- 10
print(y3.rt.tointeger(nil))    -- 0
print(y3.rt.tointeger('abc'))  -- 0
```

---

## string

function in ECARuntime

- 描述

    拼接多个值为字符串，自动处理 nil 值。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ... | any | 要拼接的值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 拼接后的字符串 |

- 示例

```lua
print(y3.rt.string('Hello', ' ', 'World'))  -- Hello World
print(y3.rt.string('Value:', nil, 100))      -- Value:100
print(y3.rt.string())                        -- ""
```
