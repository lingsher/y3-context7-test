---
sidebarDepth: 1
---
# Buff (物编对象)

# 索引

Y3 编辑器 Buff 封装接口，提供高级方法操作 Buff 对象。

---

| 接口 | 描述 |
| --- | --- |
| [get_by_handle](#get_by_handle) | 通过py层的魔法效果实例获取lua层的魔法效果实例 |
| [get_by_id](#get_by_id) |  |
| [has_tag](#has_tag) | 是否具有标签 |
| [is_icon_visible](#is_icon_visible) | 魔法效果的图标是否可见 |
| [remove](#remove) | 移除 |
| [is_exist](#is_exist) | 是否存在 |
| [set_name](#set_name) | 设置魔法效果的名称 |
| [set_description](#set_description) | 设置魔法效果对象的描述 |
| [set_time](#set_time) | 设置剩余持续时间 |
| [add_time](#add_time) | 增加剩余持续时间 |
| [set_stack](#set_stack) | 设置堆叠层数 |
| [add_stack](#add_stack) | 增加堆叠层数 |
| [set_shield](#set_shield) | 设置护盾值 |
| [add_shield](#add_shield) | 增加护盾值 |
| [get_stack](#get_stack) | 获取魔法效果的堆叠层数 |
| [get_time](#get_time) | 获取魔法效果的剩余持续时间 |
| [get_buff_type](#get_buff_type) | 获取魔法效果类型 |
| [get_buff_effect_type](#get_buff_effect_type) | 获取魔法效果影响类型 |
| [get_max_stack](#get_max_stack) | 获取魔法效果的最大堆叠层数 |
| [get_shield](#get_shield) | 获取魔法效果的护盾 |
| [get_aura](#get_aura) | 获取所属光环 |
| [get_cycle_time](#get_cycle_time) | 获取魔法效果循环周期 |
| [get_passed_time](#get_passed_time) | 魔法效果的已持续时间 |
| [get_buff_aura_effect_key](#get_buff_aura_effect_key) | 获取魔法效果的光环效果类型ID |
| [get_buff_aura_range](#get_buff_aura_range) | 获取魔法效果的光环范围 |
| [get_name_by_key](#get_name_by_key) | 获取魔法效果类型的名称 |
| [get_source](#get_source) | 获取魔法效果的施加者 |
| [get_owner](#get_owner) | 获取魔法效果的携带者 |
| [get_name](#get_name) | 获取魔法效果对象的名称 |
| [get_description](#get_description) | 获取魔法效果对象的描述 |
| [get_level](#get_level) | 获取等级 |
| [is_icon_visible_by_key](#is_icon_visible_by_key) | 魔法效果类型的图标是否可见 |
| [get_key](#get_key) | 获得魔法效果的类别 |
| [get_description_by_key](#get_description_by_key) | 获取魔法效果类型的描述 |
| [get_icon_by_key](#get_icon_by_key) | 获取魔法效果类型的icon图标的图片 |
| [get_ability](#get_ability) | 获得关联技能 |
| [add_aura_range](#add_aura_range) | 增加魔法效果光环影响范围 |
| [set_aura_range](#set_aura_range) | 设置魔法效果光环影响范围 |
| [add_cycle_time](#add_cycle_time) | 增加魔法效果循环周期 |
| [set_cycle_time](#set_cycle_time) | 设置魔法效果循环周期 |
| [set_icon](#set_icon) | 设置魔法效果的图标 |
| [set_data](#set_data) | 设置自定义数据，可使用 `Buff.data` 访问 |
| [is_destroyed](#is_destroyed) |  |

---

## get_by_handle

method in Buff

- 描述

    通过py层的魔法效果实例获取lua层的魔法效果实例

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | py_buff | py.ModifierEntity | py层的魔法效果实例 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Buff? | 返回在lua层初始化后的lua层魔法效果实例 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

local result = y3.buff.get_by_handle(modifier.handle)
```

---

## get_by_id

method in Buff

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | id | integer |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Buff |  |

- 示例

```lua
local result = y3.buff.get_by_id(1)
```

---

## has_tag

method in Buff

- 描述

    是否具有标签

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | 标签 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local buff = unit:find_buff(134274569)

local result = buff:has_tag("tag")
```

---

## is_icon_visible

method in Buff

- 描述

    魔法效果的图标是否可见

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否可见 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local buff = unit:find_buff(134274569)

local result = buff:is_icon_visible()
```

---

## remove

method in Buff

- 描述

    移除

- 参数

    无

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local buff = unit:find_buff(134274569)

buff:remove()
```

---

## is_exist

method in Buff

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
local buff = unit:find_buff(134274569)

local result = buff:is_exist()
```

---

## set_name

method in Buff

- 描述

    设置魔法效果的名称

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | name | string | 名字 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local buff = unit:find_buff(134274569)

buff:set_name("name")
```

---

## set_description

method in Buff

- 描述

    设置魔法效果对象的描述

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | description | string | 描述 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local buff = unit:find_buff(134274569)

buff:set_description("description")
```

---

## set_time

method in Buff

- 描述

    设置剩余持续时间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | time | number | 剩余持续时间 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local buff = unit:find_buff(134274569)

buff:set_time(1.0)
```

---

## add_time

method in Buff

- 描述

    增加剩余持续时间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | time | number | 剩余持续时间 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local buff = unit:find_buff(134274569)

buff:add_time(1.0)
```

---

## set_stack

method in Buff

- 描述

    设置堆叠层数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | stack | integer | 层数 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local buff = unit:find_buff(134274569)

buff:set_stack(1)
```

---

## add_stack

method in Buff

- 描述

    增加堆叠层数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | stack | integer | 层数 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local buff = unit:find_buff(134274569)

buff:add_stack(1)
```

---

## set_shield

method in Buff

- 描述

    设置护盾值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | number | 护盾值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local buff = unit:find_buff(134274569)

buff:set_shield(1.0)
```

---

## add_shield

method in Buff

- 描述

    增加护盾值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | number | 护盾值 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local buff = unit:find_buff(134274569)

buff:add_shield(1.0)
```

---

## get_stack

method in Buff

- 描述

    获取魔法效果的堆叠层数

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 层数 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local buff = unit:find_buff(134274569)

local result = buff:get_stack()
```

---

## get_time

method in Buff

- 描述

    获取魔法效果的剩余持续时间

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 剩余持续时间 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local buff = unit:find_buff(134274569)

local result = buff:get_time()
```

---

## get_buff_type

method in Buff

- 描述

    获取魔法效果类型

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | y3.Const.ModifierType | 魔法效果类型 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local buff = unit:find_buff(134274569)

local result = buff:get_buff_type()
```

---

## get_buff_effect_type

method in Buff

- 描述

    获取魔法效果影响类型

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | y3.Const.EffectType | 魔法效果影响类型 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local buff = unit:find_buff(134274569)

local result = buff:get_buff_effect_type()
```

---

## get_max_stack

method in Buff

- 描述

    获取魔法效果的最大堆叠层数

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 层数 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local buff = unit:find_buff(134274569)

local result = buff:get_max_stack()
```

---

## get_shield

method in Buff

- 描述

    获取魔法效果的护盾

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 护盾值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local buff = unit:find_buff(134274569)

local result = buff:get_shield()
```

---

## get_aura

method in Buff

- 描述

    获取所属光环

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Buff? | 所属光环 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local buff = unit:find_buff(134274569)

local result = buff:get_aura()
```

---

## get_cycle_time

method in Buff

- 描述

    获取魔法效果循环周期

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 循环周期 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local buff = unit:find_buff(134274569)

local result = buff:get_cycle_time()
```

---

## get_passed_time

method in Buff

- 描述

    魔法效果的已持续时间

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 持续时间 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local buff = unit:find_buff(134274569)

local result = buff:get_passed_time()
```

---

## get_buff_aura_effect_key

method in Buff

- 描述

    获取魔法效果的光环效果类型ID

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierKey | 光环效果类型ID |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local buff = unit:find_buff(134274569)

local result = buff:get_buff_aura_effect_key()
```

---

## get_buff_aura_range

method in Buff

- 描述

    获取魔法效果的光环范围

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 光环范围 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local buff = unit:find_buff(134274569)

local result = buff:get_buff_aura_range()
```

---

## get_name_by_key

method in Buff

- 描述

    获取魔法效果类型的名称

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | buff_key | py.ModifierKey | 类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 名字 |

- 示例

```lua
local modifier_key = 134274569

local result = y3.buff.get_name_by_key(modifier_key)
```

---

## get_source

method in Buff

- 描述

    获取魔法效果的施加者

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Unit? | 施加者 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local buff = unit:find_buff(134274569)

local result = buff:get_source()
```

---

## get_owner

method in Buff

- 描述

    获取魔法效果的携带者

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Unit? | 携带者 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local buff = unit:find_buff(134274569)

local result = buff:get_owner()
```

---

## get_name

method in Buff

- 描述

    获取魔法效果对象的名称

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 名字 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local buff = unit:find_buff(134274569)

local result = buff:get_name()
```

---

## get_description

method in Buff

- 描述

    获取魔法效果对象的描述

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 描述 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local buff = unit:find_buff(134274569)

local result = buff:get_description()
```

---

## get_level

method in Buff

- 描述

    获取等级

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 等级 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local buff = unit:find_buff(134274569)

local result = buff:get_level()
```

---

## is_icon_visible_by_key

method in Buff

- 描述

    魔法效果类型的图标是否可见

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | buff_key | py.ModifierKey | 类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否可见 |

- 示例

```lua
local modifier_key = 134274569

local result = y3.buff.is_icon_visible_by_key(modifier_key)
```

---

## get_key

method in Buff

- 描述

    获得魔法效果的类别

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierKey | 类别 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local buff = unit:find_buff(134274569)

local result = buff:get_key()
```

---

## get_description_by_key

method in Buff

- 描述

    获取魔法效果类型的描述

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | buff_key | py.ModifierKey | 类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 描述 |

- 示例

```lua
local modifier_key = 134274569

local result = y3.buff.get_description_by_key(modifier_key)
```

---

## get_icon_by_key

method in Buff

- 描述

    获取魔法效果类型的icon图标的图片

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | buff_key | py.ModifierKey | 类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Texture | 图片id |

- 示例

```lua
local modifier_key = 134274569

local result = y3.buff.get_icon_by_key(modifier_key)
```

---

## get_ability

method in Buff

- 描述

    获得关联技能

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Ability|nil | 投射物或魔法效果的关联技能 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local buff = unit:find_buff(134274569)

local result = buff:get_ability()
```

---

## add_aura_range

method in Buff

- 描述

    增加魔法效果光环影响范围

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | range | number | 影响范围 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local buff = unit:find_buff(134274569)

buff:add_aura_range(1.0)
```

---

## set_aura_range

method in Buff

- 描述

    设置魔法效果光环影响范围

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | range | number | 影响范围 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local buff = unit:find_buff(134274569)

buff:set_aura_range(1.0)
```

---

## add_cycle_time

method in Buff

- 描述

    增加魔法效果循环周期

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | time | number | 变化时间 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local buff = unit:find_buff(134274569)

buff:add_cycle_time(1.0)
```

---

## set_cycle_time

method in Buff

- 描述

    设置魔法效果循环周期

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | time | number | 循环周期 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local buff = unit:find_buff(134274569)

buff:set_cycle_time(1.0)
```

---

## set_icon

method in Buff

- 描述

    设置魔法效果的图标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | icon | integer | 图标 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local buff = unit:find_buff(134274569)

buff:set_icon(1)
```

---

## set_data

method in Buff

- 描述

    设置自定义数据，可使用 `Buff.data` 访问

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | data | any |  |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local buff = unit:find_buff(134274569)

buff:set_data("data")
```

---

## is_destroyed

method in Buff

- 描述

    

- 参数

    无

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local buff = unit:find_buff(134274569)

buff:is_destroyed()
```

---
