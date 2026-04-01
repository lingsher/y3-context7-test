---
sidebarDepth: 1
---
# fs (文件系统)

# 索引

文件系统工具，用于读取和保存脚本目录下的文件。路径不区分大小写，只能使用相对路径。

---

## 方法

| 接口 | 描述 |
| --- | --- |
| [load](#load) | 加载文件内容 |
| [save](#save) | 保存文件内容 |

---

## load

function in y3.fs

`y3.fs.load(fileName: string) -> string?, string?`

- 描述

    加载 `script` 目录下的文件。文件名不区分大小写，只能使用相对路径。路径中不能包含 `.` 开头的目录。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | fileName | string | 相对于 script 目录的文件路径 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string? | 文件内容，读取失败返回 nil |
    | string? | 错误信息 |

- 示例

```lua
-- 读取配置文件
local content, err = y3.fs.load('config/settings.lua')
if content then
    print('文件内容:', content)
else
    print('读取失败:', err)
end
```

```lua
-- 读取 JSON 配置并解析
local json_content, err = y3.fs.load('data/items.json')
if json_content then
    local data = y3.json.decode(json_content)
    print('物品数量:', #data)
end
```

```lua
-- 使用相对路径（支持 .. 回退）
local content = y3.fs.load('game/../shared/utils.lua')
-- 等效于 y3.fs.load('shared/utils.lua')
```

---

## save

function in y3.fs

`y3.fs.save(fileName: string, content: string) -> boolean, string?`

- 描述

    保存文件。
    - 编辑器/助手启动时：保存在 `script` 目录下
    - 平台启动时：保存在 `custom` 目录下
    
    注意：目录必须存在，否则保存失败。文件名不区分大小写。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | fileName | string | 相对路径 |
    | content | string | 文件内容（必须是字符串） |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否保存成功 |
    | string? | 错误信息 |

- 示例

```lua
-- 保存文本文件
local success, err = y3.fs.save('logs/game.log', '游戏开始')
if success then
    print('保存成功')
else
    print('保存失败:', err)
end
```

```lua
-- 保存 JSON 数据
local data = {
    player_count = 4,
    map_name = '测试地图',
}
local json_str = y3.json.encode(data)
y3.fs.save('data/save.json', json_str)
```

```lua
-- 追加日志（先读取再写入）
local function append_log(message)
    local old_content = y3.fs.load('logs/debug.log') or ''
    local new_content = old_content .. '\n' .. os.date() .. ': ' .. message
    y3.fs.save('logs/debug.log', new_content)
end

append_log('玩家进入游戏')
```