---
sidebarDepth: 1
---
# 网络 (KKNetwork)

# 索引

Y3 编辑器网络通信相关接口。

---

| 接口 | 描述 |
| --- | --- |
| [init](#init) | 初始化网络环境 |
| [start](#start) | 启动网络连接 |
| [is_connecting](#is_connecting) | 返回网络连接的在状态 |
| [stop](#stop) | 断开网络连接，停止接受网络消息事件 |
| [run_once](#run_once) | 主循环，需要在用户主循环中调用 |
| [destroy](#destroy) | 释放网络类资源，如果还没断开连接，这里会断开网络连接 |
| [send](#send) | 发送网络消息 |
| [recv](#recv) | 接受网络消息 |
| [peek](#peek) | 探测网络消息，不会从消息队列移除，多用于判断消息头是否足够 |
| [reset](#reset) |  |

---

## init

method in KKNetwork

- 描述

    初始化网络环境

- 参数

    无

- 返回值

    无

- 示例

```lua

network:init()
```

---

## start

method in KKNetwork

- 描述

    启动网络连接

- 参数

    无

- 返回值

    无

- 示例

```lua

network:start()
```

---

## is_connecting

method in KKNetwork

- 描述

    返回网络连接的在状态

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean |  |

- 示例

```lua

local result = network:is_connecting()
```

---

## stop

method in KKNetwork

- 描述

    断开网络连接，停止接受网络消息事件

- 参数

    无

- 返回值

    无

- 示例

```lua

network:stop()
```

---

## run_once

method in KKNetwork

- 描述

    主循环，需要在用户主循环中调用

- 参数

    无

- 返回值

    无

- 示例

```lua

network:run_once()
```

---

## destroy

method in KKNetwork

- 描述

    释放网络类资源，如果还没断开连接，这里会断开网络连接

- 参数

    无

- 返回值

    无

- 示例

```lua

network:destroy()
```

---

## send

method in KKNetwork

- 描述

    发送网络消息

- 参数

    无

- 返回值

    无

- 示例

```lua

network:send()
```

---

## recv

method in KKNetwork

- 描述

    接受网络消息

- 参数

    无

- 返回值

    无

- 示例

```lua

network:recv()
```

---

## peek

method in KKNetwork

- 描述

    探测网络消息，不会从消息队列移除，多用于判断消息头是否足够

- 参数

    无

- 返回值

    无

- 示例

```lua

network:peek()
```

---

## reset

method in KKNetwork

- 描述

    

- 参数

    无

- 返回值

    无

- 示例

```lua

network:reset()
```

---
