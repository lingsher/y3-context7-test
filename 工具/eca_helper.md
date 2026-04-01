---
sidebarDepth: 1
---
# ECAHelper (ECA辅助工具)

# 索引

ECA 辅助工具，提供快速定义 ECA 函数和调用 ECA 自定义事件的功能。

---

## 方法

| 接口 | 描述 |
| --- | --- |
| [def](#def) | 注册 ECA 函数（快捷方式） |
| [call](#call) | 调用 ECA 中定义的自定义事件 |
| [resolve](#resolve) | 解析 ECA 消息数据 |

---

## def

function in ECAHelper

- 描述

    注册 ECA 函数，是 `New 'ECAFunction' (name)` 的快捷方式。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | name | string | 函数名称 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | ECAFunction | ECA 函数实例 |

- 示例

```lua
-- 使用 def 快速定义 ECA 函数
y3.eca.def('计算伤害')
    :with_param('攻击者', 'Unit')
    :with_param('目标', 'Unit')
    :with_param('伤害值', 'number')
    :call(function(attacker, target, damage)
        attacker:damage({
            target = target,
            damage = damage,
        })
    end)
```

```lua
-- 带返回值的 ECA 函数
y3.eca.def('获取单位距离')
    :with_param('单位A', 'Unit')
    :with_param('单位B', 'Unit')
    :with_return('距离', 'number')
    :call(function(unit_a, unit_b)
        local point_a = unit_a:get_point()
        local point_b = unit_b:get_point()
        return point_a:get_distance(point_b)
    end)
```

---

## call

function in ECAHelper

- 描述

    调用 ECA 中定义的自定义事件。如果事件不存在，会抛出错误。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ... | any | 事件名称和参数 |

- 返回值

    无

- 示例

```lua
-- 在游戏逻辑中触发 ECA 事件
y3.game:event('单位-死亡', function(trg, data)
    local unit = data.unit
    local source = data.source_unit
    
    -- 调用 ECA 中定义的"处理单位死亡"事件
    y3.eca.call('处理单位死亡', unit, source)
end)
```

---

## resolve

function in ECAHelper

- 描述

    解析 ECA 消息数据，将原始事件参数转换为更易用的格式。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | data | EventParam.游戏-消息 | 消息事件数据 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | table | 解析后的数据（包含 name 和 data 字段） |

- 示例

```lua
-- 解析 ECA 消息
y3.game:event('游戏-消息', function(trg, data)
    local resolved = y3.eca.resolve(data)
    
    print('消息名称:', resolved.name)
    print('消息数据:', resolved.data)
end)
```
