---
sidebarDepth: 1
---
# 物品 (Item)

# 索引

Y3 编辑器物品对象相关接口，用于操作物品的属性、堆叠、使用等。

---

| 接口 | 描述 |
| --- | --- |
| [api_get_key](#api_get_key) | 获取物品编号 |
| [set_name](#set_name) | 设置物品名称 |
| [get_name](#get_name) | 获取物品名称 |
| [api_get_conf_name](#api_get_conf_name) | 获取物品配置名称 |
| [api_set_desc](#api_set_desc) | 设置物品描述 |
| [api_get_desc](#api_get_desc) | 获取物品描述 |
| [api_get_conf_desc](#api_get_conf_desc) | 获取物品配置描述 |
| [api_get_type](#api_get_type) | 获取物品类型 |
| [api_get_level](#api_get_level) | 获取物品等级 |
| [api_set_level](#api_set_level) | 设置物品等级 |
| [api_drop_self](#api_drop_self) | 丢弃物品 |
| [api_remove](#api_remove) | 从单位身上移除物品 |
| [api_set_sale_state](#api_set_sale_state) | 设置物品出售 |
| [api_set_stack_cnt](#api_set_stack_cnt) | 设置物品堆叠数 |
| [api_set_charge_cnt](#api_set_charge_cnt) | 设置物品充能数 |
| [api_set_max_charge](#api_set_max_charge) | 设置物品最大充能数 |
| [api_get_position](#api_get_position) | 物品实体所在位置(若在玩家身上返回玩家位置) |
| [api_is_in_scene](#api_is_in_scene) | 物品是否在场景中 |
| [api_get_stack_cnt](#api_get_stack_cnt) | 获取物品堆叠数 |
| [api_get_stack_type](#api_get_stack_type) | 获取物品堆叠类型 |
| [api_get_charge_cnt](#api_get_charge_cnt) | 获取物品充能数 |
| [api_get_max_charge](#api_get_max_charge) | 获取物品充能数 |
| [api_set_droppable](#api_set_droppable) | 设置物品丢弃 |
| [api_set_sellable](#api_set_sellable) | 设置物品出售 |
| [api_set_hp](#api_set_hp) | 设置物品生命值 |
| [api_get_droppable](#api_get_droppable) | 获取物品丢弃 |
| [api_get_sellable](#api_get_sellable) | 获取物品出售 |
| [api_get_hp](#api_get_hp) | 获取物品生命值 |
| [api_set_attr](#api_set_attr) | 设置物品附加属性 |
| [api_change_attr](#api_change_attr) | 增加物品附加属性 |
| [api_get_attr](#api_get_attr) | 获取物品附加属性 |
| [api_set_creator](#api_set_creator) | 设置物品所有玩家 |
| [api_get_creator](#api_get_creator) | 获得物品所有玩家 |
| [api_get_owner](#api_get_owner) | 获得物品拥有者 |
| [api_add_stack](#api_add_stack) | 添加物品堆叠数 |
| [api_add_charge](#api_add_charge) | 添加物品充能数 |
| [api_get_scale](#api_get_scale) | 获取物品缩放 |
| [api_get_face_angle](#api_get_face_angle) | 获取物品朝向 |
| [api_set_scale](#api_set_scale) | 设置物品缩放 |
| [api_set_position](#api_set_position) | 设置物品位置 |
| [api_set_face_angle](#api_set_face_angle) | 设置物品朝向 |
| [api_is_in_area](#api_is_in_area) | 是否在区域内 |
| [api_transmit](#api_transmit) | 移动物品到点 |
| [api_add_tag](#api_add_tag) | 物品添加标签 |
| [api_remove_tag](#api_remove_tag) | 物品删除标签 |
| [api_has_tag](#api_has_tag) | 物品是否拥有标签 |
| [api_remove_kv](#api_remove_kv) | 物品移除键值对 |
| [api_get_item_unit](#api_get_item_unit) | 获取物品在场景中的对应实体 |
| [api_get_id](#api_get_id) | 获取物品id |
| [api_is_in_bar](#api_is_in_bar) | 物品是否在物品栏 |
| [api_is_in_pkg](#api_is_in_pkg) | 物品是否在背包栏中 |
| [api_play_sound_by_item_for_role_relation](#api_play_sound_by_item_for_role_relation) | 对物品所属单位的所属玩家关系播放音乐 |
| [api_get_positive_ability](#api_get_positive_ability) | 获取物品的主动技能 |
| [api_get_passive_ability](#api_get_passive_ability) | 获取物品的被动技能 |
| [api_set_item_icon](#api_set_item_icon) | 设置物品的图标为图片 |
| [api_get_item_icon](#api_get_item_icon) | 获取物品的图标 |
| [api_get_item_slot_type](#api_get_item_slot_type) | 物品所在背包槽位类型 |
| [api_get_item_slot_idx](#api_get_item_slot_idx) | 物品所在的格子位置索引 |
| [api_item_add_passive_ability](#api_item_add_passive_ability) | 物品实例添加被动技能 |
| [api_get_item_model](#api_get_item_model) | 获取物品的模型 |
| [api_set_item_visible](#api_set_item_visible) | 设置物品可见性 |
| [api_is_item_visible](#api_is_item_visible) | 物品是否可见 |
| [api_change_model](#api_change_model) | 物品替换模型 |
| [api_cancel_replace_model](#api_cancel_replace_model) | 取消物品替换模型 |
| [api_get_item_res_cnt](#api_get_item_res_cnt) | 获取物品购买所需资源 |
| [api_get_item_float_attr](#api_get_item_float_attr) | 获取物品的实数属性 |
| [api_get_item_int_attr](#api_get_item_int_attr) | 获取物品的整数属性 |
| [api_is_item_auto_use](#api_is_item_auto_use) | 物品是否自动使用 |
| [api_item_delete_passive_ability](#api_item_delete_passive_ability) | 物品实例删除被动技能 |
| [api_change_texture](#api_change_texture) | 物品替换贴图 |
| [api_set_name_bar_type](#api_set_name_bar_type) | 设置物品名称显示样式 |

---

## api_get_key

method in Item

- 描述

    获取物品编号

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemKey? | 物品编号 |

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item.handle:api_get_key()
```

---

## set_name

method in Item

- 描述

    设置物品名称

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | name | string | 物品名称 |

- 返回值

    无

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item.handle:set_name("name")
```

---

## get_name

method in Item

- 描述

    获取物品名称

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string? | 物品名称 |

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item.handle:get_name()
```

---

## api_get_conf_name

method in Item

- 描述

    获取物品配置名称

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string? | 物品名称 |

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item.handle:api_get_conf_name()
```

---

## api_set_desc

method in Item

- 描述

    设置物品描述

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | desc | string | 物品描述 |

- 返回值

    无

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item.handle:api_set_desc("desc")
```

---

## api_get_desc

method in Item

- 描述

    获取物品描述

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string? | 物品描述 |

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item.handle:api_get_desc()
```

---

## api_get_conf_desc

method in Item

- 描述

    获取物品配置描述

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string? | 物品描述 |

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item.handle:api_get_conf_desc()
```

---

## api_get_type

method in Item

- 描述

    获取物品类型

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 物品类型 |

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item.handle:api_get_type()
```

---

## api_get_level

method in Item

- 描述

    获取物品等级

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 物品等级 |

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item.handle:api_get_level()
```

---

## api_set_level

method in Item

- 描述

    设置物品等级

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | level | integer | 等级 |

- 返回值

    无

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item.handle:api_set_level(1)
```

---

## api_drop_self

method in Item

- 描述

    丢弃物品

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | pos | py.FPoint | 点 |
    | stack_cnt? | integer | 数量 |

- 返回值

    无

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)
local fpoint = GameAPI.get_point_by_res_id(1)

item.handle:api_drop_self(fpoint, 1)
```

---

## api_remove

method in Item

- 描述

    从单位身上移除物品

- 参数

    无

- 返回值

    无

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item.handle:api_remove()
```

---

## api_set_sale_state

method in Item

- 描述

    设置物品出售

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | sale_state | boolean | 可否出售 |

- 返回值

    无

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item.handle:api_set_sale_state(true)
```

---

## api_set_stack_cnt

method in Item

- 描述

    设置物品堆叠数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | stack_cnt | integer | 堆叠数 |

- 返回值

    无

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item.handle:api_set_stack_cnt(1)
```

---

## api_set_charge_cnt

method in Item

- 描述

    设置物品充能数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | charge_cnt | integer | 充能数 |

- 返回值

    无

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item.handle:api_set_charge_cnt(1)
```

---

## api_set_max_charge

method in Item

- 描述

    设置物品最大充能数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | max_charge | integer | 最大充能数 |

- 返回值

    无

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item.handle:api_set_max_charge(1)
```

---

## api_get_position

method in Item

- 描述

    物品实体所在位置(若在玩家身上返回玩家位置)

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3? | 物品位置 |

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item.handle:api_get_position()
```

---

## api_is_in_scene

method in Item

- 描述

    物品是否在场景中

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 是否在场景中 |

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item.handle:api_is_in_scene()
```

---

## api_get_stack_cnt

method in Item

- 描述

    获取物品堆叠数

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 堆叠数 |

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item.handle:api_get_stack_cnt()
```

---

## api_get_stack_type

method in Item

- 描述

    获取物品堆叠类型

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 堆叠类型 |

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item.handle:api_get_stack_type()
```

---

## api_get_charge_cnt

method in Item

- 描述

    获取物品充能数

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 充能数 |

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item.handle:api_get_charge_cnt()
```

---

## api_get_max_charge

method in Item

- 描述

    获取物品充能数

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 最大充能数 |

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item.handle:api_get_max_charge()
```

---

## api_set_droppable

method in Item

- 描述

    设置物品丢弃

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | can_drop | boolean | 可否丢弃 |

- 返回值

    无

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item.handle:api_set_droppable(true)
```

---

## api_set_sellable

method in Item

- 描述

    设置物品出售

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | can_sell | boolean | 可否丢弃 |

- 返回值

    无

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item.handle:api_set_sellable(true)
```

---

## api_set_hp

method in Item

- 描述

    设置物品生命值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | hp | number | 生命值 |

- 返回值

    无

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item.handle:api_set_hp(1.0)
```

---

## api_get_droppable

method in Item

- 描述

    获取物品丢弃

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 可否丢弃 |

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item.handle:api_get_droppable()
```

---

## api_get_sellable

method in Item

- 描述

    获取物品出售

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 可否出售 |

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item.handle:api_get_sellable()
```

---

## api_get_hp

method in Item

- 描述

    获取物品生命值

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 生命值 |

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item.handle:api_get_hp()
```

---

## api_set_attr

method in Item

- 描述

    设置物品附加属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr_element_field | string | 属性名 |
    | attr_key | string | 属性成分名 |
    | val | number | 属性值 |

- 返回值

    无

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item.handle:api_set_attr("attr_element_field", "attr_key", 1.0)
```

---

## api_change_attr

method in Item

- 描述

    增加物品附加属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr_element_field | string | 属性名 |
    | attr_key | string | 属性成分名 |
    | delta | number | 属性值 |

- 返回值

    无

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item.handle:api_change_attr("attr_element_field", "attr_key", 1.0)
```

---

## api_get_attr

method in Item

- 描述

    获取物品附加属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr_element_field | string | 属性成分名 |
    | attr_key | string | 属性名 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 属性值 |

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item.handle:api_get_attr("attr_element_field", "attr_key")
```

---

## api_set_creator

method in Item

- 描述

    设置物品所有玩家

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | creator | py.Role | 所有者 |

- 返回值

    无

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)
local player = y3.player.get_by_id(1)

item.handle:api_set_creator(player.handle)
```

---

## api_get_creator

method in Item

- 描述

    获得物品所有玩家

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Role? | 所有者 |

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item.handle:api_get_creator()
```

---

## api_get_owner

method in Item

- 描述

    获得物品拥有者

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit? | 拥有者 |

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item.handle:api_get_owner()
```

---

## api_add_stack

method in Item

- 描述

    添加物品堆叠数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | cnt | integer | 堆叠数 |

- 返回值

    无

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item.handle:api_add_stack(1)
```

---

## api_add_charge

method in Item

- 描述

    添加物品充能数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | cnt | integer | 充能数 |

- 返回值

    无

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item.handle:api_add_charge(1)
```

---

## api_get_scale

method in Item

- 描述

    获取物品缩放

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 缩放 |

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item.handle:api_get_scale()
```

---

## api_get_face_angle

method in Item

- 描述

    获取物品朝向

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 朝向角度 |

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item.handle:api_get_face_angle()
```

---

## api_set_scale

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
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item.handle:api_set_scale(1.0)
```

---

## api_set_position

method in Item

- 描述

    设置物品位置

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.Point | 物品位置 |

- 返回值

    无

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)
local point = Fix32Vec3(0, 0, 0)

item.handle:api_set_position(point)
```

---

## api_set_face_angle

method in Item

- 描述

    设置物品朝向

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | face_angle | number | 物品朝向 |

- 返回值

    无

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item.handle:api_set_face_angle(1.0)
```

---

## api_is_in_area

method in Item

- 描述

    是否在区域内

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | py.Area | 区域 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 是否在区域 |

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)
local area = y3.area.create_circle_area(y3.point.create(0, 0, 0), 500)

local result = item.handle:api_is_in_area(area.handle)
```

---

## api_transmit

method in Item

- 描述

    移动物品到点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.Point | 点 |

- 返回值

    无

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)
local point = Fix32Vec3(0, 0, 0)

item.handle:api_transmit(point)
```

---

## api_add_tag

method in Item

- 描述

    物品添加标签

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | 标签 |

- 返回值

    无

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item.handle:api_add_tag("tag")
```

---

## api_remove_tag

method in Item

- 描述

    物品删除标签

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | 标签 |

- 返回值

    无

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item.handle:api_remove_tag("tag")
```

---

## api_has_tag

method in Item

- 描述

    物品是否拥有标签

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | 标签 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 物品是否拥有标签 |

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item.handle:api_has_tag("tag")
```

---

## api_remove_kv

method in Item

- 描述

    物品移除键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | k | string | 要移除的键 |

- 返回值

    无

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item.handle:api_remove_kv("k")
```

---

## api_get_item_unit

method in Item

- 描述

    获取物品在场景中的对应实体

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit? | 场景中的实体 |

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item.handle:api_get_item_unit()
```

---

## api_get_id

method in Item

- 描述

    获取物品id

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemID? | 物品id |

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item.handle:api_get_id()
```

---

## api_is_in_bar

method in Item

- 描述

    物品是否在物品栏

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 是否在物品栏中 |

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item.handle:api_is_in_bar()
```

---

## api_is_in_pkg

method in Item

- 描述

    物品是否在背包栏中

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 是否在背包栏中 |

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item.handle:api_is_in_pkg()
```

---

## api_play_sound_by_item_for_role_relation

method in Item

- 描述

    对物品所属单位的所属玩家关系播放音乐

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | camp_target | py.RoleRelation | 玩家关系 |
    | sid | py.AudioKey | 乐曲编号 |
    | loop | boolean | 是否循环 |

- 返回值

    无

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)
local relation = 1
local audio_key = 134274569

item.handle:api_play_sound_by_item_for_role_relation(relation, audio_key, true)
```

---

## api_get_positive_ability

method in Item

- 描述

    获取物品的主动技能

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Ability? | 技能对象 |

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item.handle:api_get_positive_ability()
```

---

## api_get_passive_ability

method in Item

- 描述

    获取物品的被动技能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | index? | integer | 索引 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Ability? | 技能对象 |

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item.handle:api_get_passive_ability(1)
```

---

## api_set_item_icon

method in Item

- 描述

    设置物品的图标为图片

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon_id | py.Texture | 图标 |

- 返回值

    无

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item.handle:api_set_item_icon(1)
```

---

## api_get_item_icon

method in Item

- 描述

    获取物品的图标

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Texture? | 图标 |

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item.handle:api_get_item_icon()
```

---

## api_get_item_slot_type

method in Item

- 描述

    物品所在背包槽位类型

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.SlotType? | 槽位类型 |

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item.handle:api_get_item_slot_type()
```

---

## api_get_item_slot_idx

method in Item

- 描述

    物品所在的格子位置索引

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 格子位置 |

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item.handle:api_get_item_slot_idx()
```

---

## api_item_add_passive_ability

method in Item

- 描述

    物品实例添加被动技能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_id | py.AbilityKey | 技能id |
    | ability_level | integer | 技能等级 |

- 返回值

    无

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)
local ability_key = 134274569

item.handle:api_item_add_passive_ability(ability_key, 1)
```

---

## api_get_item_model

method in Item

- 描述

    获取物品的模型

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModelKey? | 模型编号 |

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item.handle:api_get_item_model()
```

---

## api_set_item_visible

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
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item.handle:api_set_item_visible(true)
```

---

## api_is_item_visible

method in Item

- 描述

    物品是否可见

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 是否可见 |

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item.handle:api_is_item_visible()
```

---

## api_change_model

method in Item

- 描述

    物品替换模型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | source_model | py.ModelKey | 原模型编号 |

- 返回值

    无

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)
local model_key = 1

item.handle:api_change_model(model_key)
```

---

## api_cancel_replace_model

method in Item

- 描述

    取消物品替换模型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | target_model | py.ModelKey | 目标模型名字 |

- 返回值

    无

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)
local model_key = 1

item.handle:api_cancel_replace_model(model_key)
```

---

## api_get_item_res_cnt

method in Item

- 描述

    获取物品购买所需资源

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role_res_key | py.RoleResKey | 玩家属性key |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 所需资源数量 |

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)
local role_res_key = "res_key"

local result = item.handle:api_get_item_res_cnt(role_res_key)
```

---

## api_get_item_float_attr

method in Item

- 描述

    获取物品的实数属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | att_key | string | 物品实数属性key |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 实数属性值 |

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item.handle:api_get_item_float_attr("att_key")
```

---

## api_get_item_int_attr

method in Item

- 描述

    获取物品的整数属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | att_key | string | 物品整数属性key |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 整数属性值 |

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item.handle:api_get_item_int_attr("att_key")
```

---

## api_is_item_auto_use

method in Item

- 描述

    物品是否自动使用

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 是否自动使用 |

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = item.handle:api_is_item_auto_use()
```

---

## api_item_delete_passive_ability

method in Item

- 描述

    物品实例删除被动技能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_id | py.AbilityKey | 技能id |

- 返回值

    无

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)
local ability_key = 134274569

item.handle:api_item_delete_passive_ability(ability_key)
```

---

## api_change_texture

method in Item

- 描述

    物品替换贴图

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | material_id | integer | 材质 id |
    | layer_id | integer | layer id |
    | texture | py.Texture | 贴图 |

- 返回值

    无

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item.handle:api_change_texture(1, 1, 1)
```

---

## api_set_name_bar_type

method in Item

- 描述

    设置物品名称显示样式

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | name_bar_type | integer | 姓名样式 |

- 返回值

    无

- 示例

```lua
-- 获取单位和物品对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item.handle:api_set_name_bar_type(1)
```

---
