---
sidebarDepth: 1
---
# 可破坏物 (Destructible)

# 索引

Y3 编辑器可破坏物对象相关接口，用于操作可破坏物的位置、属性、生命值等。

---

| 接口 | 描述 |
| --- | --- |
| [api_transmit](#api_transmit) | 移动可破坏物到点 |
| [api_kill](#api_kill) | 杀死可破坏物 |
| [api_set_dest_dry](#api_set_dest_dry) | 使可破坏物枯竭 |
| [api_delete](#api_delete) | 删除可破坏物 |
| [api_revivie](#api_revivie) | 复活可破坏物 |
| [api_show_hide](#api_show_hide) | 显示隐藏可破坏物 |
| [api_set_hp](#api_set_hp) | 设置可破坏物生命值 |
| [api_set_max_hp](#api_set_max_hp) | 设置可破坏物最大生命值 |
| [api_set_name](#api_set_name) | 设置可破坏物的名称 |
| [api_set_source_num](#api_set_source_num) | 设置可破坏物的资源数量 |
| [api_set_scale](#api_set_scale) | 设置可破坏物的大小 |
| [api_set_face_angle](#api_set_face_angle) | 设置可破坏物的角度 |
| [api_get_int_attr](#api_get_int_attr) | 获取可破坏物的整型属性 |
| [api_get_key](#api_get_key) | 获取可破坏物的编号 |
| [api_get_str_attr](#api_get_str_attr) | 获取可破坏物的字符串属性 |
| [api_set_str_attr](#api_set_str_attr) | 设置可破坏物的字符串属性 |
| [api_get_bool_attr](#api_get_bool_attr) | 获取可破坏物的布尔值属性 |
| [api_get_float_attr](#api_get_float_attr) | 获取可破坏物的浮点数属性 |
| [api_get_camp_id](#api_get_camp_id) | 获取可破坏物所属阵营id |
| [api_get_position](#api_get_position) | 获取可破坏物位置 |
| [api_get_id](#api_get_id) | 获取可破坏物的id |
| [api_get_x_scale](#api_get_x_scale) | 获取可破坏物的x轴缩放 |
| [api_get_y_scale](#api_get_y_scale) | 获取可破坏物的y轴缩放 |
| [api_get_z_scale](#api_get_z_scale) | 获取可破坏物的z轴缩放 |
| [api_get_angle](#api_get_angle) | 获取可破坏物的旋转角度 |
| [api_get_dest_model](#api_get_dest_model) | 获取可破坏物模型 |
| [api_is_ability_target](#api_is_ability_target) | 可破坏物能否被技能指示器选中 |
| [api_is_attacked](#api_is_attacked) | 可破坏物能否被普通攻击 |
| [api_is_selected](#api_is_selected) | 可破坏物能否被选中 |
| [api_is_collected](#api_is_collected) | 可破坏物能否被采集 |
| [api_is_visible](#api_is_visible) | 可破坏物是否可见 |
| [api_is_alive](#api_is_alive) | 可破坏物是否存活 |
| [api_get_dest_cur_source_nums](#api_get_dest_cur_source_nums) | 获取可破坏物的当前资源 |
| [api_get_dest_max_source_nums](#api_get_dest_max_source_nums) | 获取可破坏物的最大资源 |
| [api_get_role_res_of_dest](#api_get_role_res_of_dest) | 获取可破坏物的玩家属性 |
| [api_get_item_type_of_dest](#api_get_item_type_of_dest) | 获取可破坏物的物品类型 |
| [api_get_dest_face_angle](#api_get_dest_face_angle) | 获取可破坏物的面向角度 |
| [api_get_dest_height_offset](#api_get_dest_height_offset) | 获取可破坏物的高度 |
| [api_revivie_new](#api_revivie_new) | 复活可破坏物 |
| [api_set_dest_is_ability_target](#api_set_dest_is_ability_target) | 设置可破坏物能否被技能指示器选中 |
| [api_set_dest_is_attacked](#api_set_dest_is_attacked) | 设置可破坏物能否被普通攻击 |
| [api_set_dest_is_selected](#api_set_dest_is_selected) | 设置可破坏物能否被选中 |
| [api_set_dest_is_collected](#api_set_dest_is_collected) | 设置可破坏物能否被采集 |
| [api_add_tag](#api_add_tag) | 可破坏物添加标签 |
| [api_remove_tag](#api_remove_tag) | 可破坏物移除标签 |
| [api_set_cur_source_nums](#api_set_cur_source_nums) | 设置可破坏物能的当前资源个数 |
| [api_set_max_source_nums](#api_set_max_source_nums) | 设置可破坏物能的最大资源个数 |
| [api_add_hp_cur_value](#api_add_hp_cur_value) | 增加可破坏物能的当前生命值 |
| [api_add_hp_max_value](#api_add_hp_max_value) | 增加可破坏物能的最大生命值 |
| [api_add_sp_cur_value](#api_add_sp_cur_value) | 增加可破坏物能的当前资源个数 |
| [api_add_sp_max_value](#api_add_sp_max_value) | 增加可破坏物能的最大资源个数 |
| [api_play_animation](#api_play_animation) | 可破坏物播放动画 |
| [api_stop_animation](#api_stop_animation) | 可破坏物停止播放动画 |
| [api_replace_model](#api_replace_model) | 可破坏物替换模型 |
| [api_cancel_replace_model](#api_cancel_replace_model) | 取消可破坏物替换模型 |
| [api_set_height_offset](#api_set_height_offset) | 设置可破坏物的高度 |
| [api_add_height_offset](#api_add_height_offset) | 增加可破坏物的高度 |
| [api_replace_texture](#api_replace_texture) | 可破坏物替换贴图 |

---

## api_transmit

method in Destructible

- 描述

    移动可破坏物到点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.Point | 点 |

- 返回值

    无

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then
    local point = Fix32Vec3(0, 0, 0)

    destructible.handle:api_transmit(point)
end
```

---

## api_kill

method in Destructible

- 描述

    杀死可破坏物

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 凶手单位 |

- 返回值

    无

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then
    local unit = y3.player.get_by_id(1):get_all_units()[1]

    destructible.handle:api_kill(unit.handle)
end
```

---

## api_set_dest_dry

method in Destructible

- 描述

    使可破坏物枯竭

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | py.Unit | 采集单位 |

- 返回值

    无

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then
    local unit = y3.player.get_by_id(1):get_all_units()[1]

    destructible.handle:api_set_dest_dry(unit.handle)
end
```

---

## api_delete

method in Destructible

- 描述

    删除可破坏物

- 参数

    无

- 返回值

    无

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible.handle:api_delete()
end
```

---

## api_revivie

method in Destructible

- 描述

    复活可破坏物

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.Point | 复活点 |

- 返回值

    无

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then
    local point = Fix32Vec3(0, 0, 0)

    destructible.handle:api_revivie(point)
end
```

---

## api_show_hide

method in Destructible

- 描述

    显示隐藏可破坏物

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_show | boolean | 是否显示 |

- 返回值

    无

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible.handle:api_show_hide(true)
end
```

---

## api_set_hp

method in Destructible

- 描述

    设置可破坏物生命值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | hp_value | py.Fixed | 生命值 |

- 返回值

    无

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible.handle:api_set_hp(Fix32(1))
end
```

---

## api_set_max_hp

method in Destructible

- 描述

    设置可破坏物最大生命值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | hp_value | py.Fixed | 最大生命值 |

- 返回值

    无

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible.handle:api_set_max_hp(Fix32(1))
end
```

---

## api_set_name

method in Destructible

- 描述

    设置可破坏物的名称

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | name | string | 名称 |

- 返回值

    无

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible.handle:api_set_name("name")
end
```

---

## api_set_source_num

method in Destructible

- 描述

    设置可破坏物的资源数量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | num | integer | 资源数量 |

- 返回值

    无

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible.handle:api_set_source_num(1)
end
```

---

## api_set_scale

method in Destructible

- 描述

    设置可破坏物的大小

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | x | py.Fixed | x大小 |
    | y | py.Fixed | y大小 |
    | z | py.Fixed | z大小 |

- 返回值

    无

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible.handle:api_set_scale(Fix32(1), Fix32(1), Fix32(1))
end
```

---

## api_set_face_angle

method in Destructible

- 描述

    设置可破坏物的角度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | angle | py.Fixed | 角度 |

- 返回值

    无

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible.handle:api_set_face_angle(Fix32(1))
end
```

---

## api_get_int_attr

method in Destructible

- 描述

    获取可破坏物的整型属性

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
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

local result =     destructible.handle:api_get_int_attr("attr_name")
end
```

---

## api_get_key

method in Destructible

- 描述

    获取可破坏物的编号

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DestructibleKey? | 可破坏物编号 |

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

local result =     destructible.handle:api_get_key()
end
```

---

## api_get_str_attr

method in Destructible

- 描述

    获取可破坏物的字符串属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr_name | string | 属性名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string? | 字符串类型返回值 |

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

local result =     destructible.handle:api_get_str_attr("attr_name")
end
```

---

## api_set_str_attr

method in Destructible

- 描述

    设置可破坏物的字符串属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr_name | string | 属性名称 |
    | value | string | 属性取值 |

- 返回值

    无

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible.handle:api_set_str_attr("attr_name", "value")
end
```

---

## api_get_bool_attr

method in Destructible

- 描述

    获取可破坏物的布尔值属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr_name | string | 属性名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 布尔类型返回值 |

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

local result =     destructible.handle:api_get_bool_attr("attr_name")
end
```

---

## api_get_float_attr

method in Destructible

- 描述

    获取可破坏物的浮点数属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | attr_name | string | 属性名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 浮点类型返回值 |

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

local result =     destructible.handle:api_get_float_attr("attr_name")
end
```

---

## api_get_camp_id

method in Destructible

- 描述

    获取可破坏物所属阵营id

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.CampID? | 阵营ID |

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

local result =     destructible.handle:api_get_camp_id()
end
```

---

## api_get_position

method in Destructible

- 描述

    获取可破坏物位置

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3? | 单位位置 |

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

local result =     destructible.handle:api_get_position()
end
```

---

## api_get_id

method in Destructible

- 描述

    获取可破坏物的id

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DestructibleID? | 可破坏物id |

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

local result =     destructible.handle:api_get_id()
end
```

---

## api_get_x_scale

method in Destructible

- 描述

    获取可破坏物的x轴缩放

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number? | 缩放的值 |

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

local result =     destructible.handle:api_get_x_scale()
end
```

---

## api_get_y_scale

method in Destructible

- 描述

    获取可破坏物的y轴缩放

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number? | 缩放的值 |

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

local result =     destructible.handle:api_get_y_scale()
end
```

---

## api_get_z_scale

method in Destructible

- 描述

    获取可破坏物的z轴缩放

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number? | 缩放的值 |

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

local result =     destructible.handle:api_get_z_scale()
end
```

---

## api_get_angle

method in Destructible

- 描述

    获取可破坏物的旋转角度

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number? | 角度值 |

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

local result =     destructible.handle:api_get_angle()
end
```

---

## api_get_dest_model

method in Destructible

- 描述

    获取可破坏物模型

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModelKey? | 模型编号 |

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

local result =     destructible.handle:api_get_dest_model()
end
```

---

## api_is_ability_target

method in Destructible

- 描述

    可破坏物能否被技能指示器选中

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 布尔值 |

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

local result =     destructible.handle:api_is_ability_target()
end
```

---

## api_is_attacked

method in Destructible

- 描述

    可破坏物能否被普通攻击

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 布尔值 |

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

local result =     destructible.handle:api_is_attacked()
end
```

---

## api_is_selected

method in Destructible

- 描述

    可破坏物能否被选中

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 布尔值 |

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

local result =     destructible.handle:api_is_selected()
end
```

---

## api_is_collected

method in Destructible

- 描述

    可破坏物能否被采集

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 布尔值 |

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

local result =     destructible.handle:api_is_collected()
end
```

---

## api_is_visible

method in Destructible

- 描述

    可破坏物是否可见

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 布尔值 |

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

local result =     destructible.handle:api_is_visible()
end
```

---

## api_is_alive

method in Destructible

- 描述

    可破坏物是否存活

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean? | 布尔值 |

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

local result =     destructible.handle:api_is_alive()
end
```

---

## api_get_dest_cur_source_nums

method in Destructible

- 描述

    获取可破坏物的当前资源

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 布尔值 |

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

local result =     destructible.handle:api_get_dest_cur_source_nums()
end
```

---

## api_get_dest_max_source_nums

method in Destructible

- 描述

    获取可破坏物的最大资源

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer? | 布尔值 |

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

local result =     destructible.handle:api_get_dest_max_source_nums()
end
```

---

## api_get_role_res_of_dest

method in Destructible

- 描述

    获取可破坏物的玩家属性

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleResKey? | 玩家属性 |

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

local result =     destructible.handle:api_get_role_res_of_dest()
end
```

---

## api_get_item_type_of_dest

method in Destructible

- 描述

    获取可破坏物的物品类型

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemKey? | 物品类型 |

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

local result =     destructible.handle:api_get_item_type_of_dest()
end
```

---

## api_get_dest_face_angle

method in Destructible

- 描述

    获取可破坏物的面向角度

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 可破坏物的面向角度 |

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

local result =     destructible.handle:api_get_dest_face_angle()
end
```

---

## api_get_dest_height_offset

method in Destructible

- 描述

    获取可破坏物的高度

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed? | 可破坏物的高度 |

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

local result =     destructible.handle:api_get_dest_height_offset()
end
```

---

## api_revivie_new

method in Destructible

- 描述

    复活可破坏物

- 参数

    无

- 返回值

    无

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible.handle:api_revivie_new()
end
```

---

## api_set_dest_is_ability_target

method in Destructible

- 描述

    设置可破坏物能否被技能指示器选中

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | bool_value | boolean | 布尔值 |

- 返回值

    无

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible.handle:api_set_dest_is_ability_target(true)
end
```

---

## api_set_dest_is_attacked

method in Destructible

- 描述

    设置可破坏物能否被普通攻击

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | bool_value | boolean | 布尔值 |

- 返回值

    无

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible.handle:api_set_dest_is_attacked(true)
end
```

---

## api_set_dest_is_selected

method in Destructible

- 描述

    设置可破坏物能否被选中

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | bool_value | boolean | 布尔值 |

- 返回值

    无

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible.handle:api_set_dest_is_selected(true)
end
```

---

## api_set_dest_is_collected

method in Destructible

- 描述

    设置可破坏物能否被采集

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | bool_value | boolean | 布尔值 |

- 返回值

    无

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible.handle:api_set_dest_is_collected(true)
end
```

---

## api_add_tag

method in Destructible

- 描述

    可破坏物添加标签

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | TAG |

- 返回值

    无

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible.handle:api_add_tag("tag")
end
```

---

## api_remove_tag

method in Destructible

- 描述

    可破坏物移除标签

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | TAG |

- 返回值

    无

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible.handle:api_remove_tag("tag")
end
```

---

## api_set_cur_source_nums

method in Destructible

- 描述

    设置可破坏物能的当前资源个数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | sp_value | py.Fixed | 资源数 |

- 返回值

    无

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible.handle:api_set_cur_source_nums(Fix32(1))
end
```

---

## api_set_max_source_nums

method in Destructible

- 描述

    设置可破坏物能的最大资源个数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | sp_value | py.Fixed | 资源数 |

- 返回值

    无

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible.handle:api_set_max_source_nums(Fix32(1))
end
```

---

## api_add_hp_cur_value

method in Destructible

- 描述

    增加可破坏物能的当前生命值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | delta | py.Fixed | 当前生命值 |

- 返回值

    无

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible.handle:api_add_hp_cur_value(Fix32(1))
end
```

---

## api_add_hp_max_value

method in Destructible

- 描述

    增加可破坏物能的最大生命值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | delta | py.Fixed | 最大生命值 |

- 返回值

    无

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible.handle:api_add_hp_max_value(Fix32(1))
end
```

---

## api_add_sp_cur_value

method in Destructible

- 描述

    增加可破坏物能的当前资源个数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | delta | py.Fixed | 当前资源数 |

- 返回值

    无

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible.handle:api_add_sp_cur_value(Fix32(1))
end
```

---

## api_add_sp_max_value

method in Destructible

- 描述

    增加可破坏物能的最大资源个数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | delta | py.Fixed | 最大资源数 |

- 返回值

    无

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible.handle:api_add_sp_max_value(Fix32(1))
end
```

---

## api_play_animation

method in Destructible

- 描述

    可破坏物播放动画

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | name | string | 动画名称 |
    | init_time? | number | 开始时间(s) |
    | end_time? | number | 结束时间(s)，正数 -1 表示不结束 |
    | loop? | boolean | 是否循环 |
    | rate? | number | 播放倍率 |

- 返回值

    无

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible.handle:api_play_animation("name", 1.0, 1.0, true, 1.0)
end
```

---

## api_stop_animation

method in Destructible

- 描述

    可破坏物停止播放动画

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | name | string | 动画名称 |

- 返回值

    无

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible.handle:api_stop_animation("name")
end
```

---

## api_replace_model

method in Destructible

- 描述

    可破坏物替换模型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | target_model | py.ModelKey | 目标模型编号 |

- 返回值

    无

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then
    local model_key = 1

    destructible.handle:api_replace_model(model_key)
end
```

---

## api_cancel_replace_model

method in Destructible

- 描述

    取消可破坏物替换模型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | target_model | py.ModelKey | 目标模型名字 |

- 返回值

    无

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then
    local model_key = 1

    destructible.handle:api_cancel_replace_model(model_key)
end
```

---

## api_set_height_offset

method in Destructible

- 描述

    设置可破坏物的高度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | height_value | py.Fixed | 高度值 |

- 返回值

    无

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible.handle:api_set_height_offset(Fix32(1))
end
```

---

## api_add_height_offset

method in Destructible

- 描述

    增加可破坏物的高度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | delta | py.Fixed | 高度变化值 |

- 返回值

    无

- 示例

```lua
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible.handle:api_add_height_offset(Fix32(1))
end
```

---

## api_replace_texture

method in Destructible

- 描述

    可破坏物替换贴图

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
-- 获取可破坏物对象
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible.handle:api_replace_texture(1, 1, 1)
end
```

---
