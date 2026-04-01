---
sidebarDepth: 1
---
# Network (网络)

# 索引

网络模块，提供 Socket 客户端功能，用于连接外部服务器进行数据通信。

---

## 构造

| 接口 | 描述 |
| --- | --- |
| [y3.network.connect](#connect) | 建立 Socket 连接 |

## 方法

| 接口 | 描述 |
| --- | --- |
| [on_connected](#on_connected) | 连接成功回调 |
| [on_data](#on_data) | 收到数据回调 |
| [on_disconnected](#on_disconnected) | 断开连接回调 |
| [on_error](#on_error) | 发生错误回调 |
| [data_reader](#data_reader) | 阻塞式数据读取器 |
| [send](#send) | 发送数据 |
| [is_connecting](#is_connecting) | 检查连接状态 |
| [remove](#remove) | 关闭连接 |

---

## connect

function in y3.network

`y3.network.connect(ip: string, port: integer, options?: Network.Options) -> Network`

- 描述

    建立一个 Socket 客户端，连接到目标服务器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ip | string | 服务器 IP 地址 |
    | port | integer | 端口号 |
    | options? | Network.Options | 配置选项 |

- 配置选项 (Network.Options)

    | 字段 | 类型 | 默认值 | 说明 |
    |------|------|--------|------|
    | buffer_size | integer | 2MB | 网络缓冲区大小（字节） |
    | timeout | number | 无限 | 连接超时时间（秒） |
    | update_interval | number | 0.2 | 网络更新间隔（秒） |
    | retry_interval | number | 5 | 重连间隔（秒） |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Network | 网络连接对象 |

- 示例

```lua
-- 连接到服务器
local network = y3.network.connect('127.0.0.1', 8080)

network:on_connected(function(self)
    print('连接成功')
end)
```

```lua
-- 带配置的连接
local network = y3.network.connect('192.168.1.100', 9000, {
    buffer_size = 1024 * 1024,  -- 1MB 缓冲
    timeout = 10,               -- 10秒超时
    update_interval = 0.1,      -- 0.1秒更新
    retry_interval = 3,         -- 3秒重试
})
```

---

## on_connected

method in Network

- 描述

    设置连接成功后的回调函数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | callback | fun(self: Network) | 回调函数 |

- 示例

```lua
local network = y3.network.connect('127.0.0.1', 8080)

network:on_connected(function(self)
    print('已连接到服务器')
    self:send('Hello Server!')
end)
```

---

## on_data

method in Network

- 描述

    设置收到数据后的回调函数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | callback | fun(self: Network, data: string) | 回调函数 |

- 示例

```lua
local network = y3.network.connect('127.0.0.1', 8080)

network:on_data(function(self, data)
    print('收到数据:', data)
    -- 处理接收到的数据
end)
```

---

## on_disconnected

method in Network

- 描述

    设置断开连接后的回调函数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | callback | fun(self: Network) | 回调函数 |

- 示例

```lua
local network = y3.network.connect('127.0.0.1', 8080)

network:on_disconnected(function(self)
    print('与服务器断开连接')
end)
```

---

## on_error

method in Network

- 描述

    设置发生错误后的回调函数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | callback | fun(self: Network, error: string) | 回调函数 |

- 示例

```lua
local network = y3.network.connect('127.0.0.1', 8080)

network:on_error(function(self, error)
    print('网络错误:', error)
end)
```

---

## data_reader

method in Network

- 描述

    创建一个"阻塞"式的数据读取器。与 `on_data` 互斥。
    
    读取规则：
    - `read()` - 读取所有已收到的数据
    - `read(n)` - 读取指定字节数
    - `read('l')` - 读取一行（不含换行符）
    - `read('L')` - 读取一行（含换行符）

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | callback | fun(read: fun(len?): string) | 读取器回调 |

- 示例

```lua
local network = y3.network.connect('127.0.0.1', 8080)

network:data_reader(function(read)
    -- 读取一行数据
    local line = read('l')
    print('收到一行:', line)
end)
```

```lua
-- 读取固定长度的协议包
local network = y3.network.connect('127.0.0.1', 8080)

network:data_reader(function(read)
    -- 先读取 4 字节的包头（长度）
    local header = read(4)
    local length = string.unpack('>I4', header)
    
    -- 再读取指定长度的包体
    local body = read(length)
    print('收到包体:', body)
end)
```

---

## send

method in Network

- 描述

    发送数据到服务器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | data | string | 要发送的数据 |

- 示例

```lua
local network = y3.network.connect('127.0.0.1', 8080)

network:on_connected(function(self)
    -- 发送文本数据
    self:send('Hello')
    
    -- 发送二进制数据
    local packet = string.pack('>I4', 12345)
    self:send(packet)
end)
```

---

## is_connecting

method in Network

- 描述

    检查是否已连接

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否已连接 |

- 示例

```lua
local network = y3.network.connect('127.0.0.1', 8080)

y3.ltimer.loop(1, function()
    if network:is_connecting() then
        print('网络已连接')
    else
        print('网络未连接')
    end
end)
```

---

## remove

method in Network

- 描述

    关闭并销毁网络连接

- 示例

```lua
local network = y3.network.connect('127.0.0.1', 8080)

-- 某些条件下关闭连接
network:remove()
```
