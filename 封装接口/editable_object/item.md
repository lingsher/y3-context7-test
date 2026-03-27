---
sidebarDepth: 1
---
# Item (物编对象)

# 索引

Y3 编辑器 Item 封装接口，提供高级方法操作 Item 对象。

---

| 接口 | 描述 |
| --- | --- |
| [get_by_handle](#get_by_handle) | 通过py层的技能实例获取lua层的道具实例 |
| [get_by_id](#get_by_id) | 通过id获取lua层的道具实例 |
| [is_exist](#is_exist) | 是否存在 |
| [get_id](#get_id) | 获取唯一ID |
| [has_tag](#has_tag) | 存在标签 |
| [is_in_scene](#is_in_scene) | 是否在场景中 |
| [is_in_bar](#is_in_bar) | 物品在物品栏 |
| [is_in_bag](#is_in_bag) | 物品在背包栏 |
| [attr_pick](#attr_pick) | 遍历物品的单位属性 |
| [attr_pick_by_key](#attr_pick_by_key) | 遍历物品类型的单位属性 |
| [remove](#remove) | 删除物品 |
| [drop](#drop) | 丢弃物品到点 |
| [set_point](#set_point) | 移动到点 |
| [set_name](#set_name) | 设置物品的名称 |
| [set_name_show_type](#set_name_show_type) | 设置名称显示方式 |
| [set_description](#set_description) | 设置物品的描述 |
| [set_icon](#set_icon) | 设置物品的图标 |
| [get_icon](#get_icon) | 获取物品的图标 |
| [set_owner_player](#set_owner_player) | 设置所属玩家 |
| [set_level](#set_level) | 设置等级 |
| [set_charge](#set_charge) | 设置充能数 |
| [add_charge](#add_charge) | 增加充能数 |
| [set_max_charge](#set_max_charge) | 设置最大充能数 |
| [set_stack](#set_stack) | 设置堆叠数 |
| [add_stack](#add_stack) | 增加堆叠数 |
| [set_attr](#set_attr) | 设置属性 |
| [set_attribute](#set_attribute) | 设置基础属性 |
| [add_attribute](#add_attribute) | 增加基础属性 |
| [get_attribute](#get_attribute) | 获取物品的基础属性 |
| [set_bonus_attribute](#set_bonus_attribute) | 设置增益属性 |
| [add_bonus_attribute](#add_bonus_attribute) | 增加增益属性 |
| [get_bonus_attribute](#get_bonus_attribute) | 获取物品的增益属性 |
| [set_hp](#set_hp) | 设置生命值 |
| [add_passive_ability](#add_passive_ability) | 给物品添加被动技能 |
| [set_droppable](#set_droppable) | 设置丢弃状态 |
| [add_tag](#add_tag) | 添加标签 |
| [remove_tag](#remove_tag) |  |
| [set_sale_state](#set_sale_state) | 设置物品可否出售 |
| [set_scale](#set_scale) | 设置物品缩放 |
| [set_visible](#set_visible) | 设置物品可见性 |
| [set_facing](#set_facing) | 设置物品朝向 |
| [get_key](#get_key) | 获取物品类型id |
| [set_shop_price](#set_shop_price) | 设置物品商品售价 |
| [get_owner](#get_owner) | 物品持有者 |
| [get_point](#get_point) | 物品所在点 |
| [get_stack](#get_stack) | 物品堆叠数 |
| [get_stack_type](#get_stack_type) | 获取堆叠类型 |
| [get_charge](#get_charge) | 物品充能数 |
| [get_max_charge](#get_max_charge) | 获取最大充能数 |
| [get_level](#get_level) | 获取物品等级 |
| [get_hp](#get_hp) | 获取物品的生命值 |
| [get_name](#get_name) | 获取物品名 |
| [get_description](#get_description) | 获取物品描述 |
| [get_scale](#get_scale) | 获取物品缩放 |
| [get_facing](#get_facing) | 获取物品的朝向 |
| [get_ability](#get_ability) | 获取物品的主动技能 |
| [get_passive_ability](#get_passive_ability) | 获取物品的被动技能 |
| [get_slot](#get_slot) | 获取物品在单位身上的格子位置 |
| [get_owner_player](#get_owner_player) | 获取物品的拥有玩家 |
| [get_slot_type](#get_slot_type) | 获取物品在单位身上的背包槽类型 |
| [check_precondition_by_key](#check_precondition_by_key) | 检查物品类型前置条件 |
| [create_item](#create_item) | 创建物品到点 |
| [get_item_buy_price_by_key](#get_item_buy_price_by_key) | 获取物品购买售价 |
| [get_item_sell_price_by_key](#get_item_sell_price_by_key) | 获取物品出售售价 |
| [get_item_group_in_area](#get_item_group_in_area) | 获得区域内所有物品 |
| [get_name_by_key](#get_name_by_key) | 获取物品类型名 |
| [get_icon_id_by_key](#get_icon_id_by_key) | 获取物品类型的icon的图片id |
| [get_description_by_key](#get_description_by_key) | 获取物品类型的描述 |
| [get_model](#get_model) | 获取物品模型 |
| [get_model_by_key](#get_model_by_key) | 获取物品类型的模型 |
| [get_num_of_item_mat](#get_num_of_item_mat) | 物品类型合成所需的物品类型数量 |
| [get_num_of_player_attr](#get_num_of_player_attr) | 物品类型合成所需的玩家属性数量 |
| [get_attribute_by_key](#get_attribute_by_key) | 获取物品类型的基础属性 |
| [has_tag_by_key](#has_tag_by_key) | 物品类型是否存在标签 |
| [get_tags_by_key](#get_tags_by_key) | 获取物品的所有标签 |
| [is_destroyed](#is_destroyed) |  |
| [set_name_bar_type](#set_name_bar_type) | 设置物品名称显示样式 |

---

## get_by_handle

method in Item

- 描述

    通过py层的技能实例获取lua层的道具实例

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | py_item | py.Item | py层的道具实例 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Item? | 返回在lua层初始化后的lua层道具实例 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = y3.item.get_by_handle(item.handle)
```

---

## get_by_id

method in Item

- 描述

    通过id获取lua层的道具实例

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | id | py.ItemID |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Item | 返回在lua层初始化后的lua层道具实例 |

- 示例

```lua
local item_id = 1

local result = y3.item.get_by_id(item_id)
```

---

## is_exist

method in Item

- 描述

    是否存在

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存在 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item:is_exist()
```

---

## get_id

method in Item

- 描述

    获取唯一ID

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item:get_id()
```

---

## has_tag

method in Item

- 描述

    存在标签

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | 删除标签 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否有标签 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item:has_tag("tag")
```

---

## is_in_scene

method in Item

- 描述

    是否在场景中

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否在场景中 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item:is_in_scene()
```

---

## is_in_bar

method in Item

- 描述

    物品在物品栏

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否在物品栏 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item:is_in_bar()
```

---

## is_in_bag

method in Item

- 描述

    物品在背包栏

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否在背包栏 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item:is_in_bag()
```

---

## attr_pick

method in Item

- 描述

    遍历物品的单位属性

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string[] | 属性key |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item:attr_pick()
```

---

## attr_pick_by_key

method in Item

- 描述

    遍历物品类型的单位属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string[] | 属性key |

- 示例

```lua
local item_key = 134274569

local result = y3.item.attr_pick_by_key(item_key)
```

---

## remove

method in Item

- 描述

    删除物品

- 参数

    无

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item:remove()
```

---

## drop

method in Item

- 描述

    丢弃物品到点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | Point | 目标点 |
    | count | integer | 丢弃数量 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)
local point = y3.point(0, 0)

item:drop(point, 1)
```

---

## set_point

method in Item

- 描述

    移动到点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | Point | 点 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)
local point = y3.point(0, 0)

item:set_point(point)
```

---

## set_name

method in Item

- 描述

    设置物品的名称

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | name | string | 名字 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item:set_name("name")
```

---

## set_name_show_type

method in Item

- 描述

    设置名称显示方式

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | show_type | y3.Const.BarNameShowType | 名称显示方式 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item:set_name_show_type("show_type")
```

---

## set_description

method in Item

- 描述

    设置物品的描述

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | description | string | 描述 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item:set_description("description")
```

---

## set_icon

method in Item

- 描述

    设置物品的图标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | picture_id | py.Texture | 图片id |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)
local texture = 1

item:set_icon(texture)
```

---

## get_icon

method in Item

- 描述

    获取物品的图标

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Texture |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item:get_icon()
```

---

## set_owner_player

method in Item

- 描述

    设置所属玩家

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 所属玩家 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)
local player = y3.player.get_by_id(1)

item:set_owner_player(player)
```

---

## set_level

method in Item

- 描述

    设置等级

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | level | integer | 等级 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item:set_level(1)
```

---

## set_charge

method in Item

- 描述

    设置充能数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | charge | integer | 充能数 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item:set_charge(1)
```

---

## add_charge

method in Item

- 描述

    增加充能数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | charge | integer | 充能数 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item:add_charge(1)
```

---

## set_max_charge

method in Item

- 描述

    设置最大充能数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | charge | integer | 最大充能数 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item:set_max_charge(1)
```

---

## set_stack

method in Item

- 描述

    设置堆叠数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | stack | integer | 堆叠数 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item:set_stack(1)
```

---

## add_stack

method in Item

- 描述

    增加堆叠数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | stack | integer | 堆叠数 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item:add_stack(1)
```

---

## set_attr

method in Item

- 描述

    设置属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr_name | string | 属性名 |
    | value | number | 属性值 |
    | attr_type | string | 属性类型 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item:set_attr("attr_name", 1.0, "attr_type")
```

---

## set_attribute

method in Item

- 描述

    设置基础属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 属性key |
    | value | number | 属性值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item:set_attribute("key", 1.0)
```

---

## add_attribute

method in Item

- 描述

    增加基础属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 属性key |
    | value | number | 属性值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item:add_attribute("key", 1.0)
```

---

## get_attribute

method in Item

- 描述

    获取物品的基础属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 属性key |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item:get_attribute("key")
```

---

## set_bonus_attribute

method in Item

- 描述

    设置增益属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 属性key |
    | value | number | 属性值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item:set_bonus_attribute("key", 1.0)
```

---

## add_bonus_attribute

method in Item

- 描述

    增加增益属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 属性key |
    | value | number | 属性值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item:add_bonus_attribute("key", 1.0)
```

---

## get_bonus_attribute

method in Item

- 描述

    获取物品的增益属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 属性key |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item:get_bonus_attribute("key")
```

---

## set_hp

method in Item

- 描述

    设置生命值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | number | 生命值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item:set_hp(1.0)
```

---

## add_passive_ability

method in Item

- 描述

    给物品添加被动技能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_id | py.AbilityKey | 技能id |
    | level | integer | 等级 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)
local ability_key = 134274569

item:add_passive_ability(ability_key, 1)
```

---

## set_droppable

method in Item

- 描述

    设置丢弃状态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | dropable | boolean | 状态 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item:set_droppable(true)
```

---

## add_tag

method in Item

- 描述

    添加标签

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | 标签 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item:add_tag("tag")
```

---

## remove_tag

method in Item

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | 标签 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item:remove_tag("tag")
```

---

## set_sale_state

method in Item

- 描述

    设置物品可否出售

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | state | boolean | 是否可出售 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item:set_sale_state(true)
```

---

## set_scale

method in Item

- 描述

    设置物品缩放

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | scale | number | 缩放 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item:set_scale(1.0)
```

---

## set_visible

method in Item

- 描述

    设置物品可见性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_visible | boolean | 是否可见 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item:set_visible(true)
```

---

## set_facing

method in Item

- 描述

    设置物品朝向

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | facing | number | 朝向 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item:set_facing(1.0)
```

---

## get_key

method in Item

- 描述

    获取物品类型id

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemKey | 类型 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item:get_key()
```

---

## set_shop_price

method in Item

- 描述

    设置物品商品售价

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | id | py.ItemKey | 物品id |
    | player_attr_name | py.RoleResKey | 玩家属性 |
    | price | number | 价格 |

- 返回值

    无

- 示例

```lua
local item_key = 134274569
local role_res_key = "res_key"

y3.item.set_shop_price(item_key, role_res_key, 1.0)
```

---

## get_owner

method in Item

- 描述

    物品持有者

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Unit? | 持有者 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item:get_owner()
```

---

## get_point

method in Item

- 描述

    物品所在点

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Point | 物品所在点 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item:get_point()
```

---

## get_stack

method in Item

- 描述

    物品堆叠数

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 堆叠数 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item:get_stack()
```

---

## get_stack_type

method in Item

- 描述

    获取堆叠类型

- 参数

    无

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item:get_stack_type()
```

---

## get_charge

method in Item

- 描述

    物品充能数

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 充能数 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item:get_charge()
```

---

## get_max_charge

method in Item

- 描述

    获取最大充能数

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 最大充能数 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item:get_max_charge()
```

---

## get_level

method in Item

- 描述

    获取物品等级

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 物品等级 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item:get_level()
```

---

## get_hp

method in Item

- 描述

    获取物品的生命值

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 物品的生命值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item:get_hp()
```

---

## get_name

method in Item

- 描述

    获取物品名

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 物品名字 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item:get_name()
```

---

## get_description

method in Item

- 描述

    获取物品描述

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 物品描述 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item:get_description()
```

---

## get_scale

method in Item

- 描述

    获取物品缩放

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 物品缩放 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item:get_scale()
```

---

## get_facing

method in Item

- 描述

    获取物品的朝向

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 朝向 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item:get_facing()
```

---

## get_ability

method in Item

- 描述

    获取物品的主动技能

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Ability? | 主动技能 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item:get_ability()
```

---

## get_passive_ability

method in Item

- 描述

    获取物品的被动技能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | index | integer |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Ability? | 被动技能 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item:get_passive_ability(1)
```

---

## get_slot

method in Item

- 描述

    获取物品在单位身上的格子位置

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 格子位置 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item:get_slot()
```

---

## get_owner_player

method in Item

- 描述

    获取物品的拥有玩家

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Player? | 玩家 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item:get_owner_player()
```

---

## get_slot_type

method in Item

- 描述

    获取物品在单位身上的背包槽类型

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SlotType |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item:get_slot_type()
```

---

## check_precondition_by_key

method in Item

- 描述

    检查物品类型前置条件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | item_key | py.ItemKey | 物品类型ID |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local item_key = 134274569

local result = y3.item.check_precondition_by_key(player, item_key)
```

---

## create_item

method in Item

- 描述

    创建物品到点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | Point | 点 |
    | item_key | py.ItemKey | 道具类型 |
    | player? | Player | 玩家 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Item |  |

- 示例

```lua
local point = y3.point(0, 0)
local item_key = 134274569

local result = y3.item.create_item(point, item_key)
```

---

## get_item_buy_price_by_key

method in Item

- 描述

    获取物品购买售价

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 类型 |
    | key | y3.Const.PlayerAttr \| string | 玩家属性 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 价格 |

- 示例

```lua
local item_key = 134274569

local result = y3.item.get_item_buy_price_by_key(item_key, "key")
```

---

## get_item_sell_price_by_key

method in Item

- 描述

    获取物品出售售价

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 类型 |
    | key | y3.Const.PlayerAttr \| string | 玩家属性 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 价格 |

- 示例

```lua
local item_key = 134274569

local result = y3.item.get_item_sell_price_by_key(item_key, "key")
```

---

## get_item_group_in_area

method in Item

- 描述

    获得区域内所有物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | Area | 区域 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | ItemGroup |  |

- 示例

```lua
local area = y3.area.create_circle_area(y3.point(0, 0), 500)

local result = y3.item.get_item_group_in_area(area)
```

---

## get_name_by_key

method in Item

- 描述

    获取物品类型名

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string |  |

- 示例

```lua
local item_key = 134274569

local result = y3.item.get_name_by_key(item_key)
```

---

## get_icon_id_by_key

method in Item

- 描述

    获取物品类型的icon的图片id

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Texture |  |

- 示例

```lua
local item_key = 134274569

local result = y3.item.get_icon_id_by_key(item_key)
```

---

## get_description_by_key

method in Item

- 描述

    获取物品类型的描述

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string |  |

- 示例

```lua
local item_key = 134274569

local result = y3.item.get_description_by_key(item_key)
```

---

## get_model

method in Item

- 描述

    获取物品模型

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModelKey | 模型类型 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item:get_model()
```

---

## get_model_by_key

method in Item

- 描述

    获取物品类型的模型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModelKey | 模型类型 |

- 示例

```lua
local item_key = 134274569

local result = y3.item.get_model_by_key(item_key)
```

---

## get_num_of_item_mat

method in Item

- 描述

    物品类型合成所需的物品类型数量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey |  |
    | comp_item_key | py.ItemKey |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer |  |

- 示例

```lua
local item_key = 134274569

local result = y3.item.get_num_of_item_mat(item_key, item_key)
```

---

## get_num_of_player_attr

method in Item

- 描述

    物品类型合成所需的玩家属性数量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey |  |
    | role_res_key | py.RoleResKey |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number |  |

- 示例

```lua
local item_key = 134274569
local role_res_key = "res_key"

local result = y3.item.get_num_of_player_attr(item_key, role_res_key)
```

---

## get_attribute_by_key

method in Item

- 描述

    获取物品类型的基础属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey | 物品类型 |
    | key | string | 属性key |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number |  |

- 示例

```lua
local item_key = 134274569

local result = y3.item.get_attribute_by_key(item_key, "key")
```

---

## has_tag_by_key

method in Item

- 描述

    物品类型是否存在标签

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | 标签 |
    | item_key | py.ItemKey | 物品类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否有标签 |

- 示例

```lua
local item_key = 134274569

local result = y3.item.has_tag_by_key("tag", item_key)
```

---

## get_tags_by_key

method in Item

- 描述

    获取物品的所有标签

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_key | py.ItemKey |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string[] |  |

- 示例

```lua
local item_key = 134274569

local result = y3.item.get_tags_by_key(item_key)
```

---

## is_destroyed

method in Item

- 描述

    

- 参数

    无

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item:is_destroyed()
```

---

## set_name_bar_type

method in Item

- 描述

    设置物品名称显示样式

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | name_bar_type | integer | 名字显示样式 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item:set_name_bar_type(1)
```

---
