---
sidebarDepth: 1
---
# RSA (RSA 加密)

# 索引

RSA 非对称加密模块，提供密钥生成、加密和解密功能。适用于安全数据传输、数字签名等场景。

---

## 方法

| 接口 | 描述 |
| --- | --- |
| [generate_keys](#generate_keys) | 生成 RSA 密钥对 |
| [encrypt](#encrypt) | 使用公钥加密 |
| [decrypt](#decrypt) | 使用私钥解密 |

---

## generate_keys

function in y3.rsa

`y3.rsa.generate_keys() -> string, string`

- 描述

    生成一对 RSA 密钥（公钥和私钥）

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 公钥 |
    | string | 私钥 |

- 示例

```lua
-- 生成 RSA 密钥对
local public_key, private_key = y3.rsa.generate_keys()
print('公钥:', public_key)
print('私钥:', private_key)
```

---

## encrypt

function in y3.rsa

`y3.rsa.encrypt(public_key: string, data: string) -> string`

- 描述

    使用公钥加密数据

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | public_key | string | 公钥 |
    | data | string | 要加密的内容 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 加密后的内容 |

- 示例

```lua
-- 使用公钥加密
local public_key, private_key = y3.rsa.generate_keys()

local message = '这是秘密消息'
local encrypted = y3.rsa.encrypt(public_key, message)
print('加密后:', encrypted)
```

---

## decrypt

function in y3.rsa

`y3.rsa.decrypt(private_key: string, data: string) -> string`

- 描述

    使用私钥解密数据

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | private_key | string | 私钥 |
    | data | string | 要解密的内容 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 解密后的内容 |

- 示例

```lua
-- 使用私钥解密
local public_key, private_key = y3.rsa.generate_keys()

local message = '这是秘密消息'
local encrypted = y3.rsa.encrypt(public_key, message)
local decrypted = y3.rsa.decrypt(private_key, encrypted)

print('原始消息:', message)
print('解密后:', decrypted)
-- 输出: 原始消息: 这是秘密消息
-- 输出: 解密后: 这是秘密消息
```
