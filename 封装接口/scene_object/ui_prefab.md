---
sidebarDepth: 1
---
# UIPrefab (场景对象)

# 索引

Y3 编辑器 UIPrefab 封装接口，提供高级方法操作 UIPrefab 对象。

---

| 接口 | 描述 |
| --- | --- |
| [get_by_handle](#get_by_handle) | 通过py层的界面实例获取lua层的界面实例 |
| [create](#create) | 创建界面模块实例 |
| [remove](#remove) | 删除界面模块实例 |
| [get_child](#get_child) | 获取 UIPrefab 的 UI 实例 |

---

## get_by_handle

method in UIPrefab

- 描述

    通过py层的界面实例获取lua层的界面实例

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | prefab_name | string |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | UIPrefab | 返回在lua层初始化后的lua层技能实例 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = y3.ui_prefab.get_by_handle(player, "prefab_name")
```

---

## create

method in UIPrefab

- 描述

    创建界面模块实例

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | prefab_name | string | 界面模块id |
    | parent_ui | UI | 父控件 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | UIPrefab |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local parent_ui = y3.ui.get_ui(y3.player.get_by_id(1), "ui_path")

local result = y3.ui_prefab.create(player, "prefab_name", parent_ui)
```

---

## remove

method in UIPrefab

- 描述

    删除界面模块实例

- 参数

    无

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui_prefab = y3.ui_prefab.create(player, "prefab_name", y3.ui.get_ui(player, "ui_path"))

ui_prefab:remove()
```

---

## get_child

method in UIPrefab

- 描述

    获取 UIPrefab 的 UI 实例

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | child_path? | string | 路径，默认为根节点。 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | UI? |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui_prefab = y3.ui_prefab.create(player, "prefab_name", y3.ui.get_ui(player, "ui_path"))

local result = ui_prefab:get_child("child_path")
```

---
