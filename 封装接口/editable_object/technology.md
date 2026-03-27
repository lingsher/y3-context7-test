---
sidebarDepth: 1
---
# Technology (物编对象)

# 索引

Y3 编辑器 Technology 封装接口，提供高级方法操作 Technology 对象。

---

| 接口 | 描述 |
| --- | --- |
| [check_precondition_by_key](#check_precondition_by_key) | 检查科技类型前置条件 |

---

## check_precondition_by_key

method in Technology

- 描述

    检查科技类型前置条件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | tech_key | py.TechKey | 技能类型id (物编id) |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 技能类型前置条件是否满足 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local tech_key = 134274569

local result = y3.technology.check_precondition_by_key(player, tech_key)
```

---
