---
sidebarDepth: 1
---
# Force (运行时对象)

# 索引

Y3 编辑器 Force 封装接口，提供高级方法操作 Force 对象。

---

| 接口 | 描述 |
| --- | --- |
| [remove](#remove) |  |
| [create](#create) |  |

---

## remove

method in Force

- 描述

    

- 参数

    无

- 返回值

    无

- 示例

```lua
local force = y3.force.create()

force:remove()
```

---

## create

method in Force

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 被牵引的单位 |
    | options | Force.Options | 牵引选项 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Force |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = y3.force.create(unit, "options")
```

---
