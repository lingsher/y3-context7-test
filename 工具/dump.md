---
sidebarDepth: 1
---
# Dump (数据序列化)

# 索引

数据序列化工具，用于将 Lua 数据结构序列化为二进制字符串，以及将二进制字符串反序列化为 Lua 数据。支持自定义类的序列化。

---

## 方法

| 接口 | 描述 |
| --- | --- |
| [encode](#encode) | 序列化数据 |
| [decode](#decode) | 反序列化数据 |

---

## encode

function in Dump

- 描述

    将 Lua 数据序列化为二进制字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | data | Serialization.SupportTypes | 要序列化的数据 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 序列化后的二进制字符串 |

- 示例

```lua
-- 序列化基础数据类型
local data = {
    name = "玩家1",
    level = 10,
    hp = 100.5,
    skills = {"火球术", "冰霜新星"},
    position = {x = 100, y = 200}
}

local bin = y3.dump.encode(data)
print("序列化后长度:", #bin)
```

---

## decode

function in Dump

- 描述

    将二进制字符串反序列化为 Lua 数据

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | bin | string | 序列化的二进制字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | any | 反序列化后的数据 |

- 示例

```lua
-- 反序列化数据
local bin = y3.dump.encode({name = "测试", value = 123})
local data = y3.dump.decode(bin)

print("名称:", data.name)   -- 测试
print("值:", data.value)    -- 123
```
