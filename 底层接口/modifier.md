---
sidebarDepth: 1
---
# 魔法效果 (Modifier)

# 索引

Y3 编辑器魔法效果对象相关接口，用于操作Buff的属性、层数、持续时间等。

---

| 接口 | 描述 |
| --- | --- |
| [api_add_buff_max_layer](#api_add_buff_max_layer) | 增加buff最大层数 |
| [api_add_buff_layer](#api_add_buff_layer) | 增加buff实例层数 |
| [api_add_buff_residue_time](#api_add_buff_residue_time) | 增加buff的剩余持续时间 |
| [api_add_float_shield](#api_add_float_shield) | 增加buff浮点属性效果 |
| [api_add_cycle_time](#api_add_cycle_time) | 增加循环周期事件的循环时间 |
| [api_prevent_will_modifier](#api_prevent_will_modifier) | 阻止即将获得的魔法效果 |
| [api_remove](#api_remove) | 删除魔法效果 |
| [api_add_modifier_halo_influence_rng](#api_add_modifier_halo_influence_rng) | 增加魔法效果光环影响范围 |
| [api_get_owner](#api_get_owner) | 获取效果携带者 |
| [api_get_releaser](#api_get_releaser) | 获取效果释放者 |
| [api_get_residue_time](#api_get_residue_time) | 获取剩余持续时间 |
| [api_get_passed_time](#api_get_passed_time) | 获取已经持续时间 |
| [api_get_from_ability_id](#api_get_from_ability_id) | 获取buff关联技能id |
| [api_get_layer_max](#api_get_layer_max) | 获取buff最大堆叠层数 |
| [api_get_modifier_type](#api_get_modifier_type) | 获取buff类别 |
| [api_get_modifier_effect_type](#api_get_modifier_effect_type) | 获取buff影响类型 |
| [api_get_float_attr](#api_get_float_attr) | 获取buff浮点属性效果 |
| [api_get_cycle_time](#api_get_cycle_time) | 获取buff循环周期 |
| [api_get_sub_halo_modifier_key](#api_get_sub_halo_modifier_key) | 获取光环魔法效果的子光环类型 |
| [api_get_halo_modifier_instance](#api_get_halo_modifier_instance) | 获取子光环的光环实体 |
| [api_get_halo_inf_rng](#api_get_halo_inf_rng) | 获取光环的范围 |
| [api_get_will_modifier_unit](#api_get_will_modifier_unit) | 获取即将获得魔法效果的单位 |
| [api_get_will_modifier_key](#api_get_will_modifier_key) | 获取即将获得魔法效果类型 |
| [api_get_modifier_unique_id](#api_get_modifier_unique_id) | 获取buff的唯一id |
| [api_get_modifier_key](#api_get_modifier_key) | 获取buff的类型key |
| [api_get_int_attr](#api_get_int_attr) | 获取buff整数属性效果 |
| [api_get_str_attr](#api_get_str_attr) | 获取buff字符属性效果 |
| [api_get_icon_is_visible](#api_get_icon_is_visible) | 获取buff图标是否可见 |
| [api_get_modifier_level](#api_get_modifier_level) | 获取魔法效果等级 |
| [api_get_modifier_layer](#api_get_modifier_layer) | 获取魔法效果的堆叠层数 |
| [api_set_buff_max_layer](#api_set_buff_max_layer) | 设置buff整数属性效果 |
| [api_set_buff_layer](#api_set_buff_layer) | 设置buff实例层数 |
| [api_set_buff_residue_time](#api_set_buff_residue_time) | 设置buff的剩余持续时间 |
| [api_set_float_shield](#api_set_float_shield) | 设置buff浮点属性效果 |
| [api_set_cycle_time](#api_set_cycle_time) | 设置循环周期事件 |
| [api_set_duration](#api_set_duration) | 设置魔法效果的持续时间 |
| [api_set_buff_str_attr](#api_set_buff_str_attr) | 设置buff的字符串属性 |
| [api_play_sound_by_mod_for_role_relation](#api_play_sound_by_mod_for_role_relation) | 对魔法效果所属单位的所属玩家关系播放音乐 |
| [api_set_modifier_halo_influence_rng](#api_set_modifier_halo_influence_rng) | 设置魔法效果光环影响范围 |
| [api_set_modifier_icon](#api_set_modifier_icon) | 设置魔法效果的图标 |
| [api_add_modifier_owner_attr_by_attr_element](#api_add_modifier_owner_attr_by_attr_element) | 增加魔法效果所属单位属性 |
| [api_get_modifier_owner_attr_by_attr_element](#api_get_modifier_owner_attr_by_attr_element) | 获取魔法效果所属单位属性 |
| [api_add_modifier_tag](#api_add_modifier_tag) | 魔法效果添加标签 |
| [api_remove_modifier_tag](#api_remove_modifier_tag) | 魔法效果去除标签 |
| [api_set_modifier_owner_attr_by_attr_element](#api_set_modifier_owner_attr_by_attr_element) | 设置魔法效果所属单位属性 |
| [api_clear_modifier_owner_attr](#api_clear_modifier_owner_attr) | 清空魔法效果所属单位属性 |

---

## api_add_buff_max_layer

method in ModifierEntity

- 描述

    增加buff最大层数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr_num | integer | 整数属性值 |

- 返回值

    无

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

modifier.handle:api_add_buff_max_layer(1)
```

---

## api_add_buff_layer

method in ModifierEntity

- 描述

    增加buff实例层数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | plus_layer | integer | 整数属性值 |

- 返回值

    无

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

modifier.handle:api_add_buff_layer(1)
```

---

## api_add_buff_residue_time

method in ModifierEntity

- 描述

    增加buff的剩余持续时间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | residue_time | py.Fixed | 浮点数剩余时间 |

- 返回值

    无

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

modifier.handle:api_add_buff_residue_time(Fix32(1))
```

---

## api_add_float_shield

method in ModifierEntity

- 描述

    增加buff浮点属性效果

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr_name | string | 属性名称 |
    | attr_num | py.Fixed | 浮点数属性值 |

- 返回值

    无

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

modifier.handle:api_add_float_shield("attr_name", Fix32(1))
```

---

## api_add_cycle_time

method in ModifierEntity

- 描述

    增加循环周期事件的循环时间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | add_cycle_time | py.Fixed | 浮点数属性值 |

- 返回值

    无

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

modifier.handle:api_add_cycle_time(Fix32(1))
```

---

## api_prevent_will_modifier

method in ModifierEntity

- 描述

    阻止即将获得的魔法效果

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 返回值 |

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

local result = modifier.handle:api_prevent_will_modifier()
```

---

## api_remove

method in ModifierEntity

- 描述

    删除魔法效果

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 返回值 |

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

local result = modifier.handle:api_remove()
```

---

## api_add_modifier_halo_influence_rng

method in ModifierEntity

- 描述

    增加魔法效果光环影响范围

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | add_value | py.Fixed | 浮点数属性值 |

- 返回值

    无

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

modifier.handle:api_add_modifier_halo_influence_rng(Fix32(1))
```

---

## api_get_owner

method in ModifierEntity

- 描述

    获取效果携带者

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit? | 效果携带者 |

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

local result = modifier.handle:api_get_owner()
```

---

## api_get_releaser

method in ModifierEntity

- 描述

    获取效果释放者

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit? | 效果释放者 |

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

local result = modifier.handle:api_get_releaser()
```

---

## api_get_residue_time

method in ModifierEntity

- 描述

    获取剩余持续时间

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 剩余持续时间 |

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

local result = modifier.handle:api_get_residue_time()
```

---

## api_get_passed_time

method in ModifierEntity

- 描述

    获取已经持续时间

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 已经持续时间 |

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

local result = modifier.handle:api_get_passed_time()
```

---

## api_get_from_ability_id

method in ModifierEntity

- 描述

    获取buff关联技能id

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 最大堆叠层数 |

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

local result = modifier.handle:api_get_from_ability_id()
```

---

## api_get_layer_max

method in ModifierEntity

- 描述

    获取buff最大堆叠层数

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 最大堆叠层数 |

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

local result = modifier.handle:api_get_layer_max()
```

---

## api_get_modifier_type

method in ModifierEntity

- 描述

    获取buff类别

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr_name | string | 属性名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierType? | 魔法效果类别 |

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

local result = modifier.handle:api_get_modifier_type("attr_name")
```

---

## api_get_modifier_effect_type

method in ModifierEntity

- 描述

    获取buff影响类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr_name | string | 属性名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierEffectType? | 魔法效果影响类别 |

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

local result = modifier.handle:api_get_modifier_effect_type("attr_name")
```

---

## api_get_float_attr

method in ModifierEntity

- 描述

    获取buff浮点属性效果

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr_name | string | 属性名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 浮点数返回类型 |

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

local result = modifier.handle:api_get_float_attr("attr_name")
```

---

## api_get_cycle_time

method in ModifierEntity

- 描述

    获取buff循环周期

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 浮点数返回类型 |

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

local result = modifier.handle:api_get_cycle_time()
```

---

## api_get_sub_halo_modifier_key

method in ModifierEntity

- 描述

    获取光环魔法效果的子光环类型

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierKey? | 魔法效果编号 |

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

local result = modifier.handle:api_get_sub_halo_modifier_key()
```

---

## api_get_halo_modifier_instance

method in ModifierEntity

- 描述

    获取子光环的光环实体

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierEntity? | 魔法效果对象 |

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

local result = modifier.handle:api_get_halo_modifier_instance()
```

---

## api_get_halo_inf_rng

method in ModifierEntity

- 描述

    获取光环的范围

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number? | 光环影响范围 |

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

local result = modifier.handle:api_get_halo_inf_rng()
```

---

## api_get_will_modifier_unit

method in ModifierEntity

- 描述

    获取即将获得魔法效果的单位

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Unit? | 单位 |

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

local result = modifier.handle:api_get_will_modifier_unit()
```

---

## api_get_will_modifier_key

method in ModifierEntity

- 描述

    获取即将获得魔法效果类型

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierKey? | 魔法效果编号 |

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

local result = modifier.handle:api_get_will_modifier_key()
```

---

## api_get_modifier_unique_id

method in ModifierEntity

- 描述

    获取buff的唯一id

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 魔法效果唯一ID |

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

local result = modifier.handle:api_get_modifier_unique_id()
```

---

## api_get_modifier_key

method in ModifierEntity

- 描述

    获取buff的类型key

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierKey? | 魔法效果key |

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

local result = modifier.handle:api_get_modifier_key()
```

---

## api_get_int_attr

method in ModifierEntity

- 描述

    获取buff整数属性效果

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr_name | string | 属性名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 整数类型返回值 |

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

local result = modifier.handle:api_get_int_attr("attr_name")
```

---

## api_get_str_attr

method in ModifierEntity

- 描述

    获取buff字符属性效果

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr_name | string | 属性名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string? | 字符类型返回值 |

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

local result = modifier.handle:api_get_str_attr("attr_name")
```

---

## api_get_icon_is_visible

method in ModifierEntity

- 描述

    获取buff图标是否可见

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 布尔值 |

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

local result = modifier.handle:api_get_icon_is_visible()
```

---

## api_get_modifier_level

method in ModifierEntity

- 描述

    获取魔法效果等级

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 等级 |

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

local result = modifier.handle:api_get_modifier_level()
```

---

## api_get_modifier_layer

method in ModifierEntity

- 描述

    获取魔法效果的堆叠层数

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 堆叠层数 |

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

local result = modifier.handle:api_get_modifier_layer()
```

---

## api_set_buff_max_layer

method in ModifierEntity

- 描述

    设置buff整数属性效果

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr_num | integer | 整数属性值 |

- 返回值

    无

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

modifier.handle:api_set_buff_max_layer(1)
```

---

## api_set_buff_layer

method in ModifierEntity

- 描述

    设置buff实例层数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr_num | integer | 整数属性值 |

- 返回值

    无

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

modifier.handle:api_set_buff_layer(1)
```

---

## api_set_buff_residue_time

method in ModifierEntity

- 描述

    设置buff的剩余持续时间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | residue_time | py.Fixed | 浮点数剩余时间 |

- 返回值

    无

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

modifier.handle:api_set_buff_residue_time(Fix32(1))
```

---

## api_set_float_shield

method in ModifierEntity

- 描述

    设置buff浮点属性效果

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr_name | string | 属性名称 |
    | attr_num | py.Fixed | 浮点数属性值 |

- 返回值

    无

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

modifier.handle:api_set_float_shield("attr_name", Fix32(1))
```

---

## api_set_cycle_time

method in ModifierEntity

- 描述

    设置循环周期事件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | new_cycle_time | py.Fixed | 浮点数属性值 |

- 返回值

    无

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

modifier.handle:api_set_cycle_time(Fix32(1))
```

---

## api_set_duration

method in ModifierEntity

- 描述

    设置魔法效果的持续时间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | residue_time | py.Fixed | 非负数实数值 |

- 返回值

    无

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

modifier.handle:api_set_duration(Fix32(1))
```

---

## api_set_buff_str_attr

method in ModifierEntity

- 描述

    设置buff的字符串属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | name | string | 属性名称 |
    | value | string | 属性值 |

- 返回值

    无

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

modifier.handle:api_set_buff_str_attr("name", "value")
```

---

## api_play_sound_by_mod_for_role_relation

method in ModifierEntity

- 描述

    对魔法效果所属单位的所属玩家关系播放音乐

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
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)
local relation = 1
local audio_key = 134274569

modifier.handle:api_play_sound_by_mod_for_role_relation(relation, audio_key, true)
```

---

## api_set_modifier_halo_influence_rng

method in ModifierEntity

- 描述

    设置魔法效果光环影响范围

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | py.Fixed | 浮点数属性值 |

- 返回值

    无

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

modifier.handle:api_set_modifier_halo_influence_rng(Fix32(1))
```

---

## api_set_modifier_icon

method in ModifierEntity

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
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

modifier.handle:api_set_modifier_icon(1)
```

---

## api_add_modifier_owner_attr_by_attr_element

method in ModifierEntity

- 描述

    增加魔法效果所属单位属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 属性名 |
    | attr_element | string | 属性分类 |
    | value | py.Fixed | 值 |

- 返回值

    无

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

modifier.handle:api_add_modifier_owner_attr_by_attr_element("key", "attr_element", Fix32(1))
```

---

## api_get_modifier_owner_attr_by_attr_element

method in ModifierEntity

- 描述

    获取魔法效果所属单位属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 属性名 |
    | attr_element | string | 属性分类 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 属性值 |

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

local result = modifier.handle:api_get_modifier_owner_attr_by_attr_element("key", "attr_element")
```

---

## api_add_modifier_tag

method in ModifierEntity

- 描述

    魔法效果添加标签

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | 标签 |

- 返回值

    无

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

modifier.handle:api_add_modifier_tag("tag")
```

---

## api_remove_modifier_tag

method in ModifierEntity

- 描述

    魔法效果去除标签

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | 标签 |

- 返回值

    无

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

modifier.handle:api_remove_modifier_tag("tag")
```

---

## api_set_modifier_owner_attr_by_attr_element

method in ModifierEntity

- 描述

    设置魔法效果所属单位属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | string | 属性名 |
    | attr_element | string | 属性分类 |
    | value | py.Fixed | 值 |

- 返回值

    无

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

modifier.handle:api_set_modifier_owner_attr_by_attr_element("key", "attr_element", Fix32(1))
```

---

## api_clear_modifier_owner_attr

method in ModifierEntity

- 描述

    清空魔法效果所属单位属性

- 参数

    无

- 返回值

    无

- 示例

```lua
-- 获取单位和魔法效果对象
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

modifier.handle:api_clear_modifier_owner_attr()
```

---
