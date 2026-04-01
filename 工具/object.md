---
sidebarDepth: 1
---
# EditorObject (物编管理)

# 索引

物编管理模块，用于访问和动态创建物编数据（单位、物品、技能、魔法效果、投射物、可破坏物）。支持读取/修改物编属性、注册物编事件回调。

---

## 物编类型

| 类型 | 访问方式 | 说明 |
| --- | --- | --- |
| [unit](#unit-单位物编) | `y3.object.unit[key]` | 单位物编 |
| [item](#item-物品物编) | `y3.object.item[key]` | 物品物编 |
| [ability](#ability-技能物编) | `y3.object.ability[key]` | 技能物编 |
| [buff](#buff-魔法效果物编) | `y3.object.buff[key]` | 魔法效果物编 |
| [projectile](#projectile-投射物物编) | `y3.object.projectile[key]` | 投射物物编 |
| [destructible](#destructible-可破坏物物编) | `y3.object.destructible[key]` | 可破坏物物编 |

---

## unit (单位物编)

`y3.object.unit[key]`

- 描述

    获取单位物编对象

- 属性

    | 字段 | 类型 | 说明 |
    |------|------|------|
    | key | py.UnitKey | 物编 ID |
    | data | Object.Unit | 原始物编数据 |
    | lua_data | Object.Unit | 自动转换的 Lua 物编数据 |

- 回调钩子

    | 钩子 | 说明 |
    |------|------|
    | on_create | 单位创建后执行 |
    | on_remove | 单位移除后执行 |
    | on_dead | 单位死亡后执行 |

- 示例

```lua
-- 获取单位物编
local soldier_def = y3.object.unit[134274912]
print('单位名称:', soldier_def.data.name)
```

```lua
-- 设置单位创建回调
y3.object.unit[134274912].on_create = function(unit)
    print('士兵创建:', unit:get_name())
    unit:set_hp(1000)
end
```

```lua
-- 使用 lua_data 读取物编数据（自动类型转换）
local unit_def = y3.object.unit[134274912]
local hp = unit_def.lua_data.hp_max
local name = unit_def.lua_data.name
print('最大生命:', hp, '名称:', name)
```

### unit:new

`unit_def:new(new_key?, data?) -> EditorObject.Unit`

- 描述

    以此单位为模板创建新的单位物编

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | new_key? | py.UnitKey | 新物编的 ID（可选，自动生成） |
    | data? | Object.UnitOptions | 要修改的数据 |

- 示例

```lua
-- 创建新单位物编
local base_unit = y3.object.unit[134274912]
local new_unit = base_unit:new(nil, {
    name = '强化士兵',
    hp_max = 2000,
    attack = 100,
})
print('新单位 key:', new_unit.key)
```

---

## item (物品物编)

`y3.object.item[key]`

- 描述

    获取物品物编对象

- 回调钩子

    | 钩子 | 说明 |
    |------|------|
    | on_create | 物品创建后执行 |
    | on_remove | 物品移除后执行 |
    | on_add | 物品获得后执行 |
    | on_lose | 物品失去后执行 |
    | on_add_to_pkg | 物品进入背包后执行 |
    | on_add_to_bar | 物品进入装备栏后执行 |
    | on_use | 物品使用时执行 |

- 示例

```lua
-- 获取物品物编
local sword_def = y3.object.item[134274912]

-- 设置物品使用回调
sword_def.on_use = function(item)
    print('使用了物品:', item:get_name())
end
```

```lua
-- 创建新物品物编
local base_item = y3.object.item[134274912]
local new_item = base_item:new()
print('新物品 key:', new_item.key)
```

---

## ability (技能物编)

`y3.object.ability[key]`

- 描述

    获取技能物编对象

- 回调钩子

    | 钩子 | 说明 |
    |------|------|
    | on_add | 技能获得后执行 |
    | on_lose | 技能失去后执行 |
    | on_cooldown | 技能冷却结束后执行 |
    | on_upgrade | 技能升级后执行 |
    | on_can_cast | 技能即将施法时执行 |
    | on_cast_start | 技能开始施法时执行 |
    | on_cast_channel | 技能引导施法时执行 |
    | on_cast_shot | 技能出手施法时执行 |
    | on_cast_finish | 技能完成施法时执行 |
    | on_cast_stop | 技能停止施法时执行 |

- 示例

```lua
-- 设置技能施法回调
local skill_def = y3.object.ability[134274912]

skill_def.on_cast_shot = function(ability, cast)
    print('技能出手:', ability:get_name())
    -- 创建伤害效果
    local caster = ability:get_owner()
    local target = cast:get_target_unit()
end
```

```lua
-- 创建新技能物编
local base_skill = y3.object.ability[134274912]
local new_skill = base_skill:new(nil, {
    name = '强化火球',
    ability_damage = {"200", "300"},
})
```

---

## buff (魔法效果物编)

`y3.object.buff[key]`

- 描述

    获取魔法效果物编对象

- 回调钩子

    | 钩子 | 说明 |
    |------|------|
    | on_can_add | 效果即将获得时执行 |
    | on_add | 效果获得后执行 |
    | on_lose | 效果失去后执行 |
    | on_pulse | 效果心跳后执行 |
    | on_stack_change | 效果层数变化后执行 |

- 示例

```lua
-- 设置 Buff 心跳回调
local poison_def = y3.object.buff[134274912]

poison_def.on_pulse = function(buff)
    local owner = buff:get_owner()
    -- 每次心跳造成 10 点伤害
end
```

```lua
-- 创建新 Buff 物编
local base_buff = y3.object.buff[134274912]
local new_buff = base_buff:new()
print('新 Buff key:', new_buff.key)
```

---

## projectile (投射物物编)

`y3.object.projectile[key]`

- 描述

    获取投射物物编对象

- 回调钩子

    | 钩子 | 说明 |
    |------|------|
    | on_create | 投射物创建时执行 |
    | on_remove | 投射物销毁时执行 |

- 示例

```lua
-- 设置投射物创建回调
local arrow_def = y3.object.projectile[134274912]

arrow_def.on_create = function(projectile)
    print('投射物创建:', projectile:get_key())
end
```

---

## destructible (可破坏物物编)

`y3.object.destructible[key]`

- 描述

    获取可破坏物物编对象

- 示例

```lua
-- 获取可破坏物物编
local tree_def = y3.object.destructible[134274912]
print('可破坏物数据:', tree_def.data)
```

---

# 物编事件

物编对象支持注册事件监听器：

```lua
-- 使用 event 方法注册事件（推荐）
local unit_def = y3.object.unit[134274912]

unit_def:event('单位-受到伤害后', function(trg, data)
    print('单位受到伤害:', data.damage)
end)
```
