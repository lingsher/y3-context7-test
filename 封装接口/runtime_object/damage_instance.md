---
sidebarDepth: 1
---
# DamageInstance (运行时对象)

# 索引

Y3 编辑器 DamageInstance 封装接口，提供高级方法操作 DamageInstance 对象。

---

| 接口 | 描述 |
| --- | --- |
| [get_ability](#get_ability) | 获取关联技能 |
| [get_damage](#get_damage) | 获取当前伤害 |
| [set_damage](#set_damage) | 修改当前伤害 |
| [is_missed](#is_missed) | 获取当前伤害是否闪避 |
| [set_missed](#set_missed) | 设置当前伤害是否闪避 |
| [is_critical](#is_critical) | 获取当前伤害是否暴击 |
| [set_critical](#set_critical) | 设置当前伤害是否暴击 |
| [get_attack_type](#get_attack_type) |  |
| [get_damage_type](#get_damage_type) |  |

---

## get_ability

method in DamageInstance

- 描述

    获取关联技能

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Ability? |  |

- 示例

```lua
-- 在伤害事件中获取
-- local damage = event.damage

local result = damage:get_ability()
```

---

## get_damage

method in DamageInstance

- 描述

    获取当前伤害

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number |  |

- 示例

```lua
-- 在伤害事件中获取
-- local damage = event.damage

local result = damage:get_damage()
```

---

## set_damage

method in DamageInstance

- 描述

    修改当前伤害

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | damage | number |  |

- 返回值

    无

- 示例

```lua
-- 在伤害事件中获取
-- local damage = event.damage

damage:set_damage(1.0)
```

---

## is_missed

method in DamageInstance

- 描述

    获取当前伤害是否闪避

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean |  |

- 示例

```lua
-- 在伤害事件中获取
-- local damage = event.damage

local result = damage:is_missed()
```

---

## set_missed

method in DamageInstance

- 描述

    设置当前伤害是否闪避

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | missed | boolean |  |

- 返回值

    无

- 示例

```lua
-- 在伤害事件中获取
-- local damage = event.damage

damage:set_missed(true)
```

---

## is_critical

method in DamageInstance

- 描述

    获取当前伤害是否暴击

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean |  |

- 示例

```lua
-- 在伤害事件中获取
-- local damage = event.damage

local result = damage:is_critical()
```

---

## set_critical

method in DamageInstance

- 描述

    设置当前伤害是否暴击

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | critical | boolean |  |

- 返回值

    无

- 示例

```lua
-- 在伤害事件中获取
-- local damage = event.damage

damage:set_critical(true)
```

---

## get_attack_type

method in DamageInstance

- 描述

    

- 参数

    无

- 返回值

    无

- 示例

```lua
-- 在伤害事件中获取
-- local damage = event.damage

damage:get_attack_type()
```

---

## get_damage_type

method in DamageInstance

- 描述

    

- 参数

    无

- 返回值

    无

- 示例

```lua
-- 在伤害事件中获取
-- local damage = event.damage

damage:get_damage_type()
```

---
