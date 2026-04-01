---
sidebarDepth: 1
---
# AES (AES加密解密)

# 索引

AES 加密解密工具，提供字符串的加密和解密功能。

---

## 方法

| 接口 | 描述 |
| --- | --- |
| [encrypt](#encrypt) | 加密字符串 |
| [decrypt](#decrypt) | 解密字符串 |

---

## encrypt

function in AES

- 描述

    使用 AES 算法加密字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 密钥，长度必须是 16/24/32 |
    | iv | string | 初始化向量，长度必须是 16 |
    | source_text | string | 要加密的文本 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 加密后的文本 |

- 示例

```lua
-- 16位密钥（AES-128）
local key = "1234567890123456"
-- 16位初始化向量
local iv = "abcdefghijklmnop"
-- 原文
local text = "Hello, World!"

-- 加密
local encrypted = y3.aes.encrypt(key, iv, text)
print("加密后:", encrypted)
```

---

## decrypt

function in AES

- 描述

    使用 AES 算法解密字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 密钥，长度必须是 16/24/32 |
    | iv | string | 初始化向量，长度必须是 16 |
    | crypted_text | string | 要解密的文本 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 解密后的原文 |

- 示例

```lua
-- 16位密钥（AES-128）
local key = "1234567890123456"
-- 16位初始化向量
local iv = "abcdefghijklmnop"

-- 假设 encrypted 是之前加密得到的文本
local encrypted = "..."

-- 解密
local decrypted = y3.aes.decrypt(key, iv, encrypted)
print("解密后:", decrypted)
```