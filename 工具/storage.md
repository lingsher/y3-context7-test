---
sidebarDepth: 1
---
# Storage (存储)

# 索引

存储类（Mixin），为对象提供键值存储能力。可以通过 `Extends` 混入到其他类中使用。

---

## 方法

| 接口 | 描述 |
| --- | --- |
| [storage_set](#storage_set) | 存储值 |
| [storage_get](#storage_get) | 获取值 |
| [storage_all](#storage_all) | 获取所有存储数据 |

---

## storage_set

method in Storage

`obj:storage_set(key: any, value: any) -> any`

- 描述

    存储任意值到对象中

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | any | 存储键 |
    | value | any | 存储值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | any | 存储的值 |

- 示例

```lua
-- 假设 unit 混入了 Storage
local unit = y3.unit.get_by_id(123456)

if unit then
    -- 存储数据
    unit:storage_set('last_damage', 100)
    unit:storage_set('combo_count', 5)
    unit:storage_set('custom_data', { name = '特殊数据' })
end
```

---

## storage_get

method in Storage

`obj:storage_get(key: any) -> any`

- 描述

    获取存储的值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | any | 存储键 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | any | 存储的值，不存在返回 nil |

- 示例

```lua
-- 获取存储的数据
local unit = y3.unit.get_by_id(123456)

if unit then
    local last_damage = unit:storage_get('last_damage')
    print('上次伤害:', last_damage or 0)

    local combo = unit:storage_get('combo_count')
    if combo and combo > 3 then
        print('连击数较高!')
    end
end 
```

---

## storage_all

method in Storage

`obj:storage_all() -> table`

- 描述

    获取存储数据的容器表

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | table | 存储容器 |

- 示例

```lua
-- 获取所有存储数据
local unit = y3.unit.get_by_id(123456)

if unit then
    unit:storage_set('hp_bonus', 100)
    unit:storage_set('mp_bonus', 50)

    local all_data = unit:storage_all()
    for key, value in pairs(all_data) do
        print(key, '=', value)
    end
end 
```
