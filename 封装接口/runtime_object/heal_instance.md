---
sidebarDepth: 1
---
# HealInstance (运行时对象)

# 索引

Y3 编辑器 HealInstance 封装接口，提供高级方法操作 HealInstance 对象。

---

| 接口 | 描述 |
| --- | --- |
| [get_ability](#get_ability) | 获取关联技能 |
| [get_heal](#get_heal) | 获取当前治疗 |
| [set_heal](#set_heal) | 修改当前治疗 |

---

## get_ability

method in HealInstance

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
-- 在治疗事件中获取
-- local heal = event.heal

local result = heal:get_ability()
```

---

## get_heal

method in HealInstance

- 描述

    获取当前治疗

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number |  |

- 示例

```lua
-- 在治疗事件中获取
-- local heal = event.heal

local result = heal:get_heal()
```

---

## set_heal

method in HealInstance

- 描述

    修改当前治疗

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | number |  |

- 返回值

    无

- 示例

```lua
-- 在治疗事件中获取
-- local heal = event.heal

heal:set_heal(1.0)
```

---
