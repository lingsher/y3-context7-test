---
sidebarDepth: 1
---
# LocalUILogic (本地UI逻辑框架)

# 索引

本地UI逻辑框架，用于管理UI的本地刷新、事件绑定和元件系统。

---

## API 函数

| 接口 | 描述 |
| --- | --- |
| [create](#create) | 创建一个本地UI逻辑 |
| [prefab](#prefab) | 创建一个用于元件的本地UI逻辑 |

## 实例方法

| 接口 | 描述 |
| --- | --- |
| [remove](#remove) | 删除本地UI逻辑 |
| [attach](#attach) | 附着到一个UI上 |
| [detach](#detach) | 解除UI附着 |
| [bind_unit_attr](#bind_unit_attr) | 将子控件的属性绑定到单位的属性 |
| [on_refresh](#on_refresh) | 订阅控件刷新 |
| [on_event](#on_event) | 订阅控件的本地事件 |
| [on_init](#on_init) | 订阅控件的初始化事件 |
| [bind_prefab](#bind_prefab) | 绑定元件 |
| [refresh_prefab](#refresh_prefab) | 刷新元件 |
| [refresh](#refresh) | 刷新控件 |

---

# API 函数

## create

function in LocalUILogic.API

- 描述

    创建一个本地UI逻辑

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | path_or_ui | string \| UI | UI路径或UI对象 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | LocalUILogic | 本地UI逻辑实例 |

- 示例

```lua
local local_ui = y3.local_ui.create("main_panel")
```

---

## prefab

function in LocalUILogic.API

- 描述

    创建一个用于元件的本地UI逻辑

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_name | string | 元件名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | LocalUILogic | 用于元件的本地UI逻辑实例 |

- 示例

```lua
local prefab_logic = y3.local_ui.prefab("item_slot")
```

---

# 实例方法

## remove

method in LocalUILogic

- 描述

    删除本地UI逻辑

- 参数

    无

- 返回值

    无

- 示例

```lua
local local_ui = y3.local_ui.create("main_panel")

local_ui:remove()
```

---

## attach

method in LocalUILogic

- 描述

    附着到一个UI上

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ui | UI | 要附着的UI对象 |
    | kv? | table | 数据，使用 `instance:storage_get` 获取 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | LocalUILogic | 本地UI逻辑实例 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "main_panel")
local local_ui = y3.local_ui.create("main_panel")

local_ui:attach(ui, {name = "test", value = 100})
```

---

## detach

method in LocalUILogic

- 描述

    解除UI附着

- 参数

    无

- 返回值

    无

- 示例

```lua
local local_ui = y3.local_ui.create("main_panel")

local_ui:detach()
```

---

## bind_unit_attr

method in LocalUILogic

- 描述

    将子控件的属性绑定到单位的属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | child_name | string | 子控件名称 |
    | ui_attr | y3.Const.UIAttr | UI属性 |
    | unit_attr | y3.Const.UnitAttr \| string | 单位属性 |
    | accuracy? | integer | 小数精度 |

- 返回值

    无

- 示例

```lua
local local_ui = y3.local_ui.create("main_panel")

local_ui:bind_unit_attr("hp_bar", "当前值", "当前生命", 0)
local_ui:bind_unit_attr("mp_bar", "当前值", "当前魔法", 0)
```

---

## on_refresh

method in LocalUILogic

- 描述

    订阅控件刷新，回调函数在 *本地玩家* 环境中执行。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | child_name | string | 子控件名称，空字符串表示主控件 |
    | on_refresh | fun(ui: UI, local_player: Player, instance: LocalUILogic) | 刷新回调函数 |

- 返回值

    无

- 示例

```lua
local local_ui = y3.local_ui.create("main_panel")

local_ui:on_refresh("gold_text", function(ui, local_player, instance)
    local gold = instance:storage_get("gold") or 0
    ui:set_text(tostring(gold))
end)

local_ui:on_refresh("", function(ui, local_player, instance)
    -- 刷新主控件
    ui:set_visible(true)
end)
```

---

## on_event

method in LocalUILogic

- 描述

    订阅控件的本地事件，回调函数在 *本地玩家* 环境中执行。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | child_name | string | 子控件名称，空字符串表示主控件 |
    | event | y3.Const.UIEvent | UI事件类型 |
    | callback | fun(ui: UI, local_player: Player, instance: LocalUILogic) | 事件回调函数 |

- 返回值

    无

- 示例

```lua
local local_ui = y3.local_ui.create("main_panel")

local_ui:on_event("buy_btn", "左键-点击", function(ui, local_player, instance)
    print("购买按钮被点击了！")
end)

local_ui:on_event("close_btn", "左键-点击", function(ui, local_player, instance)
    instance:remove()
end)
```

---

## on_init

method in LocalUILogic

- 描述

    订阅控件的初始化事件，回调函数在 *本地玩家* 环境中执行。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | child_name | string | 子控件名称，空字符串表示主控件 |
    | on_init | fun(ui: UI, local_player: Player, instance: LocalUILogic) | 初始化回调函数 |

- 返回值

    无

- 示例

```lua
local local_ui = y3.local_ui.create("main_panel")

local_ui:on_init("", function(ui, local_player, instance)
    -- 初始化主控件
    instance:storage_set("gold", 1000)
    print("UI初始化完成！")
end)

local_ui:on_init("title", function(ui, local_player, instance)
    ui:set_text("欢迎来到游戏")
end)
```

---

## bind_prefab

method in LocalUILogic

- 描述

    绑定元件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | child_name | string | 子控件名称，空字符串表示主控件 |
    | prefab_logic | LocalUILogic | 使用 `y3.local_ui.prefab` 创建的元件逻辑 |
    | prefab_token? | any | 如果你在不同的控件下绑定了相同的元件且需要分开刷新，可以为它们设置不同的 token |

- 返回值

    无

- 示例

```lua
-- 创建元件逻辑
local item_prefab = y3.local_ui.prefab("item_slot")

item_prefab:on_refresh("", function(ui, local_player, instance)
    local index = instance:storage_get("index")
    local item_name = instance:storage_get("item_name") or "空"
    ui:get_child("name"):set_text(item_name)
end)

-- 主UI逻辑
local local_ui = y3.local_ui.create("inventory_panel")

-- 绑定元件到容器
local_ui:bind_prefab("item_container", item_prefab)
```

---

## refresh_prefab

method in LocalUILogic

- 描述

    刷新元件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | prefab_token | any | 要刷新的元件，默认为绑定时的元件逻辑 |
    | count? | integer | 修改元件数量 |
    | on_create? | fun(index: integer, kv: table) | 创建新的元件时回调，`kv` 中默认会将 `index` 设置为这是第几个元件 |
    | on_refresh? | fun(ui: UI, local_player: Player, instance: LocalUILogic) | 刷新元件前的回调，你可以趁机通过 `instance:storage_set` 设置元件的属性 |

- 返回值

    无

- 示例

```lua
local item_prefab = y3.local_ui.prefab("item_slot")
local local_ui = y3.local_ui.create("inventory_panel")

local_ui:bind_prefab("item_container", item_prefab)

local_ui:on_init("", function(ui, local_player, instance)
    -- 创建5个物品槽
    local items = {"剑", "盾", "药水", "弓箭", "头盔"}
    
    instance:refresh_prefab(item_prefab, 5,
        function(index, kv)
            -- 创建时设置数据
            kv.item_name = items[index]
        end,
        function(ui, local_player, prefab_instance)
            -- 刷新时更新显示
            local index = prefab_instance:storage_get("index")
            print("刷新第" .. index .. "个元件")
        end
    )
end)
```

---

## refresh

method in LocalUILogic

- 描述

    刷新控件，指定的控件以及其子控件都会收到刷新消息。参数为 `*` 时，刷新所有控件。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | name | string | 控件名称，`*` 表示刷新所有控件 |
    | player? | Player | 只刷新此玩家的UI |

- 返回值

    无

- 示例

```lua
local local_ui = y3.local_ui.create("main_panel")

-- 刷新所有控件
local_ui:refresh("*")

-- 刷新指定控件及其子控件
local_ui:refresh("gold_panel")

-- 只刷新指定玩家的UI
local player = y3.player.get_by_id(1)
local_ui:refresh("*", player)
```
