---
sidebarDepth: 1
---
# ECAFunction (ECA函数绑定)

# 索引

ECA 函数绑定工具，用于将 Lua 函数注册到 ECA 系统中，使其可以在编辑器的 ECA（事件-条件-动作）系统中被调用。

---

## 方法

| 接口 | 描述 |
| --- | --- |
| [new](#new) | 创建 ECA 函数 |
| [with_param](#with_param) | 添加参数 |
| [with_return](#with_return) | 添加返回值 |
| [call](#call) | 设置执行的函数 |

---

## new

constructor in ECAFunction

- 描述

    创建一个新的 ECA 函数绑定

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | name | string | 函数名称（在 ECA 中调用时使用） |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | ECAFunction | ECA 函数实例 |

- 示例

```lua
-- 创建一个 ECA 函数
local eca_func = New 'ECAFunction' ('我的函数')
```

---

## with_param

method in ECAFunction

- 描述

    添加一个参数。参数类型名后面加 `?` 表示可选参数。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 参数名称 |
    | type_name | string | 参数类型（如 "number", "string", "Unit" 等） |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self | 支持链式调用 |

- 示例

```lua
-- 添加必选参数
New 'ECAFunction' ('计算伤害')
    :with_param('攻击者', 'Unit')
    :with_param('目标', 'Unit')
    :with_param('基础伤害', 'number')
    :call(function(attacker, target, damage)
        -- 处理逻辑
    end)
```

```lua
-- 添加可选参数（类型名后加 ?）
New 'ECAFunction' ('显示消息')
    :with_param('消息内容', 'string')
    :with_param('持续时间', 'number?')  -- 可选参数
    :call(function(message, duration)
        duration = duration or 3  -- 默认值
        print(message)
    end)
```

---

## with_return

method in ECAFunction

- 描述

    添加一个返回值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 返回值名称 |
    | type_name | string | 返回值类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self | 支持链式调用 |

- 示例

```lua
-- 添加返回值
New 'ECAFunction' ('获取单位血量')
    :with_param('单位', 'Unit')
    :with_return('当前血量', 'number')
    :call(function(unit)
        return unit:get_hp()
    end)
```

---

## call

method in ECAFunction

- 描述

    设置执行的函数。函数会接收 `with_param` 定义的参数，并返回 `with_return` 定义的返回值。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | func | function | 要执行的函数 |

- 返回值

    无

- 示例

```lua
-- 完整的 ECA 函数定义
New 'ECAFunction' ('创建单位并返回')
    :with_param('玩家', 'Player')
    :with_param('单位类型', 'py.UnitKey')
    :with_param('位置', 'Point')
    :with_return('创建的单位', 'Unit')
    :call(function(player, unit_key, point)
        local unit = player:create_unit(unit_key, point, 0)
        return unit
    end)
```
