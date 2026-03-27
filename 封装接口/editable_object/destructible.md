---
sidebarDepth: 1
---
# Destructible (物编对象)

# 索引

Y3 编辑器 Destructible 封装接口，提供高级方法操作 Destructible 对象。

---

| 接口 | 描述 |
| --- | --- |
| [get_by_handle](#get_by_handle) | 通过py层的可破坏物实例获取lua层的可破坏物对象 |
| [get_by_id](#get_by_id) | 通过可破坏物的唯一ID获取lua的可破坏物对象 |
| [is_exist](#is_exist) | 是否存在 |
| [get_id](#get_id) | 获取唯一ID |
| [can_be_ability_target](#can_be_ability_target) | 可破坏物能否被技能指示器选中 |
| [can_be_attacked](#can_be_attacked) | 可破坏物能否被攻击 |
| [can_be_selected](#can_be_selected) | 可破坏物能否被选中 |
| [can_be_collected](#can_be_collected) | 可破坏物能否被采集 |
| [is_visible](#is_visible) | 可破坏物是否可见 |
| [is_alive](#is_alive) | 可破坏物是否存活 |
| [kill](#kill) | 杀死可破坏物 |
| [remove](#remove) | 删除可破坏物 |
| [reborn](#reborn) | 复活可破坏物 |
| [set_point](#set_point) | 移动到点 |
| [set_hp](#set_hp) | 设置生命值 |
| [add_hp](#add_hp) | 增加当前生命值 |
| [set_max_hp](#set_max_hp) | 设置最大生命值 |
| [add_max_hp](#add_max_hp) | 增加最大生命值 |
| [set_resource](#set_resource) | 设置当前资源数 |
| [add_resource](#add_resource) | 增加当前资源数 |
| [set_max_resource](#set_max_resource) | 设置最大资源数 |
| [add_max_resource](#add_max_resource) | 增加最大资源数 |
| [set_name](#set_name) | 设置名称 |
| [set_description](#set_description) | 设置描述 |
| [set_scale](#set_scale) | 设置缩放 |
| [set_facing](#set_facing) | 设置朝向 |
| [set_height](#set_height) | 设置高度 |
| [add_height](#add_height) | 增加高度 |
| [set_can_be_ability_target](#set_can_be_ability_target) | 设置能否被技能指示器锁定 |
| [set_can_be_attacked](#set_can_be_attacked) | 设置能否被攻击 |
| [set_can_be_selected](#set_can_be_selected) | 设置能否被选中 |
| [set_can_be_collected](#set_can_be_collected) | 设置能否被采集 |
| [add_tag](#add_tag) | 增加标签 |
| [remove_tag](#remove_tag) | 移除标签 |
| [has_tag](#has_tag) | 是否具有标签 |
| [play_animation](#play_animation) | 播放动画 |
| [stop_animation](#stop_animation) | 停止动画 |
| [replace_model](#replace_model) | 替换模型 |
| [cancel_replace_model](#cancel_replace_model) | 取消替换模型 |
| [set_visible](#set_visible) | 显示/隐藏 |
| [get_key](#get_key) | 获取可破坏物类型 |
| [get_name](#get_name) | 获取可破坏物的名称 |
| [get_description](#get_description) | 获取可破坏物描述 |
| [get_hp](#get_hp) | 获取可破坏物的生命值 |
| [get_resource_name](#get_resource_name) | 获取可破坏物的资源名称 |
| [get_max_hp](#get_max_hp) | 获取可破坏物的生命值 |
| [get_resource](#get_resource) | 获取可破坏物的当前资源数 |
| [get_max_resource](#get_max_resource) | 获取可破坏物的最大资源数 |
| [get_resource_type](#get_resource_type) | 获取可破坏物的玩家属性名 |
| [get_item_type](#get_item_type) | 获取可破坏物的物品类型ID |
| [get_model](#get_model) | 获取可破坏物的模型 |
| [get_height](#get_height) | 获取可破坏物的高度 |
| [get_facing](#get_facing) | 获取可破坏物的面向角度 |
| [get_position](#get_position) | 获取可破坏物对象的位置 |
| [create_destructible](#create_destructible) | 创建可破坏物 |
| [get_name_by_key](#get_name_by_key) | 获取可破坏物类型的名称 |
| [get_description_by_key](#get_description_by_key) | 获取可破坏物类型的描述 |
| [get_model_by_type](#get_model_by_type) | 获取可破坏物类型的模型 |
| [pick](#pick) | 遍历区域中的所有可破坏物 |
| [pick_in_shape](#pick_in_shape) | 获取不同形状范围内的可破坏物列表 |
| [is_destroyed](#is_destroyed) |  |

---

## get_by_handle

method in Destructible

- 描述

    通过py层的可破坏物实例获取lua层的可破坏物对象

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | py_destructible | py.Destructible |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Destructible? |  |

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    local result = y3.destructible.get_by_handle(destructible.handle)
end
```

---

## get_by_id

method in Destructible

- 描述

    通过可破坏物的唯一ID获取lua的可破坏物对象

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | id | py.DestructibleID |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Destructible? |  |

- 示例

```lua
local destructible_id = 1

local result = y3.destructible.get_by_id(destructible_id)
```

---

## is_exist

method in Destructible

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
local destructible = y3.destructible.get_by_id(1)
if destructible then

    local result = destructible:is_exist()
end
```

---

## get_id

method in Destructible

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
local destructible = y3.destructible.get_by_id(1)
if destructible then

    local result = destructible:get_id()
end
```

---

## can_be_ability_target

method in Destructible

- 描述

    可破坏物能否被技能指示器选中

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 能否被选中 |

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    local result = destructible:can_be_ability_target()
end
```

---

## can_be_attacked

method in Destructible

- 描述

    可破坏物能否被攻击

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 能否被攻击 |

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    local result = destructible:can_be_attacked()
end
```

---

## can_be_selected

method in Destructible

- 描述

    可破坏物能否被选中

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 能否被选中 |

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    local result = destructible:can_be_selected()
end
```

---

## can_be_collected

method in Destructible

- 描述

    可破坏物能否被采集

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 能否被采集 |

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    local result = destructible:can_be_collected()
end
```

---

## is_visible

method in Destructible

- 描述

    可破坏物是否可见

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否可见 |

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    local result = destructible:is_visible()
end
```

---

## is_alive

method in Destructible

- 描述

    可破坏物是否存活

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否存活 |

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    local result = destructible:is_alive()
end
```

---

## kill

method in Destructible

- 描述

    杀死可破坏物

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | killer_unit | Unit | 凶手 |

- 返回值

    无

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then
local unit = y3.player.get_by_id(1):get_all_units()[1]

    destructible:kill(unit)
end
```

---

## remove

method in Destructible

- 描述

    删除可破坏物

- 参数

    无

- 返回值

    无

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible:remove()
end
```

---

## reborn

method in Destructible

- 描述

    复活可破坏物

- 参数

    无

- 返回值

    无

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible:reborn()
end
```

---

## set_point

method in Destructible

- 描述

    移动到点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | Point | 目标点 |

- 返回值

    无

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then
local point = y3.point(0, 0)

    destructible:set_point(point)
end
```

---

## set_hp

method in Destructible

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
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible:set_hp(1.0)
end
```

---

## add_hp

method in Destructible

- 描述

    增加当前生命值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | number | 生命值 |

- 返回值

    无

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible:add_hp(1.0)
end
```

---

## set_max_hp

method in Destructible

- 描述

    设置最大生命值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | number | 生命值 |

- 返回值

    无

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible:set_max_hp(1.0)
end
```

---

## add_max_hp

method in Destructible

- 描述

    增加最大生命值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | number | 生命值 |

- 返回值

    无

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible:add_max_hp(1.0)
end
```

---

## set_resource

method in Destructible

- 描述

    设置当前资源数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | number | 资源数 |

- 返回值

    无

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible:set_resource(1.0)
end
```

---

## add_resource

method in Destructible

- 描述

    增加当前资源数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | number | 资源数 |

- 返回值

    无

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible:add_resource(1.0)
end
```

---

## set_max_resource

method in Destructible

- 描述

    设置最大资源数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | number | 资源数 |

- 返回值

    无

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible:set_max_resource(1.0)
end
```

---

## add_max_resource

method in Destructible

- 描述

    增加最大资源数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | number | 资源数 |

- 返回值

    无

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible:add_max_resource(1.0)
end
```

---

## set_name

method in Destructible

- 描述

    设置名称

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | name | string | 名字 |

- 返回值

    无

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible:set_name("name")
end
```

---

## set_description

method in Destructible

- 描述

    设置描述

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | description | string | 描述 |

- 返回值

    无

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible:set_description("description")
end
```

---

## set_scale

method in Destructible

- 描述

    设置缩放

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | x | number | x轴缩放 |
    | y | number | y轴缩放 |
    | z | number | z轴缩放 |

- 返回值

    无

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible:set_scale(1.0, 1.0, 1.0)
end
```

---

## set_facing

method in Destructible

- 描述

    设置朝向

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | angle | number | 朝向角度 |

- 返回值

    无

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible:set_facing(1.0)
end
```

---

## set_height

method in Destructible

- 描述

    设置高度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | height | number | 高度 |

- 返回值

    无

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible:set_height(1.0)
end
```

---

## add_height

method in Destructible

- 描述

    增加高度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | height | number | 高度 |

- 返回值

    无

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible:add_height(1.0)
end
```

---

## set_can_be_ability_target

method in Destructible

- 描述

    设置能否被技能指示器锁定

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | can_be_ability_target | boolean | 能否被技能指示器锁定 |

- 返回值

    无

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible:set_can_be_ability_target(true)
end
```

---

## set_can_be_attacked

method in Destructible

- 描述

    设置能否被攻击

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_attackable | boolean | 能否被攻击 |

- 返回值

    无

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible:set_can_be_attacked(true)
end
```

---

## set_can_be_selected

method in Destructible

- 描述

    设置能否被选中

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_selectable | boolean | 能否被选中 |

- 返回值

    无

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible:set_can_be_selected(true)
end
```

---

## set_can_be_collected

method in Destructible

- 描述

    设置能否被采集

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_collectable | boolean | 能否被采集 |

- 返回值

    无

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible:set_can_be_collected(true)
end
```

---

## add_tag

method in Destructible

- 描述

    增加标签

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | 标签 |

- 返回值

    无

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible:add_tag("tag")
end
```

---

## remove_tag

method in Destructible

- 描述

    移除标签

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag | string | 标签 |

- 返回值

    无

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible:remove_tag("tag")
end
```

---

## has_tag

method in Destructible

- 描述

    是否具有标签

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tag_name | string | 标签 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 具有标签 |

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    local result = destructible:has_tag("tag_name")
end
```

---

## play_animation

method in Destructible

- 描述

    播放动画

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | anim_name | string | 动画名字 |
    | start_time? | number | 开始时间 |
    | end_time? | number | 结束时间(默认-1表示播放到最后) |
    | is_loop? | boolean | 是否循环 |
    | speed? | number | 速度 |

- 返回值

    无

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible:play_animation("anim_name", 1.0, 1.0, true, 1.0)
end
```

---

## stop_animation

method in Destructible

- 描述

    停止动画

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | anim_name | string | 动画名字 |

- 返回值

    无

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible:stop_animation("anim_name")
end
```

---

## replace_model

method in Destructible

- 描述

    替换模型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | model_id | py.ModelKey | 模型id |

- 返回值

    无

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then
local model_key = 1

    destructible:replace_model(model_key)
end
```

---

## cancel_replace_model

method in Destructible

- 描述

    取消替换模型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | model_id | py.ModelKey | 模型id |

- 返回值

    无

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then
local model_key = 1

    destructible:cancel_replace_model(model_key)
end
```

---

## set_visible

method in Destructible

- 描述

    显示/隐藏

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_visible | boolean | 是否显示 |

- 返回值

    无

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible:set_visible(true)
end
```

---

## get_key

method in Destructible

- 描述

    获取可破坏物类型

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DestructibleKey | 可破坏物类型 |

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    local result = destructible:get_key()
end
```

---

## get_name

method in Destructible

- 描述

    获取可破坏物的名称

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 可破坏物的名称 |

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    local result = destructible:get_name()
end
```

---

## get_description

method in Destructible

- 描述

    获取可破坏物描述

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 描述 |

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    local result = destructible:get_description()
end
```

---

## get_hp

method in Destructible

- 描述

    获取可破坏物的生命值

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 生命值 |

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    local result = destructible:get_hp()
end
```

---

## get_resource_name

method in Destructible

- 描述

    获取可破坏物的资源名称

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 资源名称 |

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    local result = destructible:get_resource_name()
end
```

---

## get_max_hp

method in Destructible

- 描述

    获取可破坏物的生命值

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 可破坏物的生命值 |

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    local result = destructible:get_max_hp()
end
```

---

## get_resource

method in Destructible

- 描述

    获取可破坏物的当前资源数

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 当前资源数 |

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    local result = destructible:get_resource()
end
```

---

## get_max_resource

method in Destructible

- 描述

    获取可破坏物的最大资源数

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 最大资源数 |

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    local result = destructible:get_max_resource()
end
```

---

## get_resource_type

method in Destructible

- 描述

    获取可破坏物的玩家属性名

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleResKey | 玩家属性 |

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    local result = destructible:get_resource_type()
end
```

---

## get_item_type

method in Destructible

- 描述

    获取可破坏物的物品类型ID

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ItemKey | 物品类型ID |

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    local result = destructible:get_item_type()
end
```

---

## get_model

method in Destructible

- 描述

    获取可破坏物的模型

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModelKey | 模型id |

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    local result = destructible:get_model()
end
```

---

## get_height

method in Destructible

- 描述

    获取可破坏物的高度

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 高度 |

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    local result = destructible:get_height()
end
```

---

## get_facing

method in Destructible

- 描述

    获取可破坏物的面向角度

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 面向角度 |

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    local result = destructible:get_facing()
end
```

---

## get_position

method in Destructible

- 描述

    获取可破坏物对象的位置

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Point | 可破坏物的位置 |

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    local result = destructible:get_position()
end
```

---

## create_destructible

method in Destructible

- 描述

    创建可破坏物

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | type_id | py.DestructibleKey | 可破坏物类型id |
    | point | Point | 创建到点 |
    | angle | number | 面向角度 |
    | scale_x? | number | 缩放x |
    | scale_y? | number | 缩放y |
    | scale_z? | number | 缩放z |
    | height? | number | 高度 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Destructible | 可破坏物 |

- 示例

```lua
local point = y3.point(0, 0)
local destructible_key = 1

local result = y3.destructible.create_destructible(destructible_key, point, 1.0, 1.0, 1.0, 1.0, 1.0)
```

---

## get_name_by_key

method in Destructible

- 描述

    获取可破坏物类型的名称

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | py.DestructibleKey | 类型id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 名称 |

- 示例

```lua
local destructible_key = 1

local result = y3.destructible.get_name_by_key(destructible_key)
```

---

## get_description_by_key

method in Destructible

- 描述

    获取可破坏物类型的描述

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | py.DestructibleKey | 类型id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 描述 |

- 示例

```lua
local destructible_key = 1

local result = y3.destructible.get_description_by_key(destructible_key)
```

---

## get_model_by_type

method in Destructible

- 描述

    获取可破坏物类型的模型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | py.DestructibleKey | 类型id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModelKey | 模型id |

- 示例

```lua
local destructible_key = 1

local result = y3.destructible.get_model_by_type(destructible_key)
```

---

## pick

method in Destructible

- 描述

    遍历区域中的所有可破坏物

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | Area | 区域对象 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Destructible[] |  |

- 示例

```lua
local area = y3.area.create_circle_area(y3.point(0, 0), 500)

local result = y3.destructible.pick(area)
```

---

## pick_in_shape

method in Destructible

- 描述

    获取不同形状范围内的可破坏物列表

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | Point | 点 |
    | shape | Shape | 区域 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | table | 可破坏物列表 |

- 示例

```lua
local point = y3.point(0, 0)
local shape = y3.shape.create_circular_shape(500)

local result = y3.destructible.pick_in_shape(point, shape)
```

---

## is_destroyed

method in Destructible

- 描述

    

- 参数

    无

- 返回值

    无

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

    destructible:is_destroyed()
end
```

---
