---
sidebarDepth: 1
---
# BASE64 (Base64编码解码)

# 索引

Base64 编码解码工具，用于将字符串与 Base64 格式互相转换。

---

## 方法

| 接口 | 描述 |
| --- | --- |
| [encode](#encode) | 将字符串编码为 Base64 |
| [decode](#decode) | 将 Base64 解码为字符串 |

---

## encode

function in BASE64

- 描述

    将字符串编码为 Base64 格式

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | str | string | 要编码的字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | Base64 编码后的字符串 |

- 示例

```lua
local text = "Hello, World!"
local encoded = y3.base64.encode(text)
print("编码后:", encoded)  -- SGVsbG8sIFdvcmxkIQ==
```

---

## decode

function in BASE64

- 描述

    将 Base64 格式解码为原始字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | base64 | string | Base64 编码的字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 解码后的原始字符串 |

- 示例

```lua
local encoded = "SGVsbG8sIFdvcmxkIQ=="
local decoded = y3.base64.decode(encoded)
print("解码后:", decoded)  -- Hello, World!
```
