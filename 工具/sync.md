---
sidebarDepth: 1
---
# Sync (数据同步)

# 索引

数据同步模块，用于将本地数据广播给所有玩家。适用于需要在多人游戏中同步客户端数据的场景。

---

## 方法

| 接口 | 描述 |
| --- | --- |
| [send](#send) | 发送本地数据 |
| [onSync](#onsync) | 注册同步回调 |

---

## send

function in y3.sync

`y3.sync.send(id: string, data?: T, done?: fun(data: T))`

- 描述

    发送本地的信息给所有玩家。需要配合 `onSync` 来接收数据。
    
    **注意**：请在本地环境中使用此函数。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | id | string | 同步标识（以 `$` 开头的保留为内部使用） |
    | data? | T | 要同步的数据（支持序列化的类型） |
    | done? | fun(data: T) | 同步完成后的本地回调 |

- 示例

```lua
-- 发送简单数据
y3.sync.send('player_ready', { player_id = 1, ready = true })
```

```lua
-- 发送数据并等待同步完成
y3.sync.send('chat_message', '你好，世界！', function(data)
    print('消息已同步:', data)
end)
```

```lua
-- 在本地环境中发送玩家选择
y3.player.with_local(function(local_player)
    local selection = {
        hero_id = 134274912,
        skin_id = 1,
    }
    y3.sync.send('hero_selection', selection)
end)
```

---

## onSync

function in y3.sync

`y3.sync.onSync(id: string, callback: fun(data: any, source: Player))`

- 描述

    注册同步接收回调。当收到指定 id 的同步数据时执行回调。
    
    **注意**：同一个 id 只能注册一个回调函数，后注册的会覆盖前面的。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | id | string | 同步标识 |
    | callback | fun(data: any, source: Player) | 回调函数，data 为同步数据，source 为发送者 |

- 示例

```lua
-- 注册同步回调
y3.sync.onSync('player_ready', function(data, source)
    if not data then return end
    print(source:get_name(), '已准备就绪')
    print('英雄选择:', data.hero_id)
end)
```

```lua
-- 处理聊天消息
y3.sync.onSync('chat_message', function(message, sender)
    local name = sender:get_name()
    print(string.format('[%s]: %s', name, message))
end)
```
