---
sidebarDepth: 1
---
# SceneUI (场景对象)

# 索引

Y3 编辑器 SceneUI 封装接口，提供高级方法操作 SceneUI 对象。

---

| 接口 | 描述 |
| --- | --- |
| [get_by_handle](#get_by_handle) | 通过py层的界面实例获取lua层的界面实例 |
| [create_scene_ui_at_point](#create_scene_ui_at_point) | 创建场景界面到场景点 |
| [get_ui_comp_in_scene_ui](#get_ui_comp_in_scene_ui) | 获取指定玩家场景ui中的控件 |
| [create_scene_ui_at_player_unit_socket](#create_scene_ui_at_player_unit_socket) | 创建场景界面到玩家单位挂点 |
| [remove_scene_ui](#remove_scene_ui) | 删除场景界面 |
| [set_scene_ui_visible_distance](#set_scene_ui_visible_distance) | 设置场景界面对玩家的可见距离 |

---

## get_by_handle

method in SceneUI

- 描述

    通过py层的界面实例获取lua层的界面实例

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | py_scene_node | py.SceneNode |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | SceneUI |  |

- 示例

```lua
local result = y3.scene_ui.get_by_handle(scene_node)
```

---

## create_scene_ui_at_point

method in SceneUI

- 描述

    创建场景界面到场景点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | sceneui | string \| y3.Const.SceneUI | 控件 |
    | point | Point | 点 |
    | range? | number | 可见距离 |
    | height? | number | 离地高度 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | SceneUI | 场景ui |

- 示例

```lua
local point = y3.point(0, 0)

local result = y3.scene_ui.create_scene_ui_at_point("sceneui", point, 1.0, 1.0)
```

---

## get_ui_comp_in_scene_ui

method in SceneUI

- 描述

    获取指定玩家场景ui中的控件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | comp_path | string | 控件路径 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | UI | UI控件 |

- 示例

```lua
local scene_ui = y3.scene_ui.create_scene_ui_at_point("sceneui", y3.point(0, 0))
local player = y3.player.get_by_id(1)

local result = scene_ui:get_ui_comp_in_scene_ui(player, "comp_path")
```

---

## create_scene_ui_at_player_unit_socket

method in SceneUI

- 描述

    创建场景界面到玩家单位挂点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | scene_ui_type | string \| y3.Const.SceneUI | 场景ui类型 |
    | player | Player | 玩家 |
    | unit | Unit | 单位 |
    | socket_name | string | 挂接点名称 |
    | distance? | number | 可见距离 |
    | follow_scale? | boolean | 是否跟随缩放 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | SceneUI | 场景ui |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

local result = y3.scene_ui.create_scene_ui_at_player_unit_socket("scene_ui_type", player, unit, "socket_name", 1.0, true)
```

---

## remove_scene_ui

method in SceneUI

- 描述

    删除场景界面

- 参数

    无

- 返回值

    无

- 示例

```lua
local scene_ui = y3.scene_ui.create_scene_ui_at_point("sceneui", y3.point(0, 0))

scene_ui:remove_scene_ui()
```

---

## set_scene_ui_visible_distance

method in SceneUI

- 描述

    设置场景界面对玩家的可见距离

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | dis | number | 可见距离 |

- 返回值

    无

- 示例

```lua
local scene_ui = y3.scene_ui.create_scene_ui_at_point("sceneui", y3.point(0, 0))
local player = y3.player.get_by_id(1)

scene_ui:set_scene_ui_visible_distance(player, 1.0)
```

---
