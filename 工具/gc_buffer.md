---
sidebarDepth: 1
---
# GCBuffer (垃圾回收缓冲)

# 索引

垃圾回收缓冲工具，用于延迟删除对象。当对象需要被删除但希望延迟一段时间后再真正移除时使用。

---

## 构造

| 接口 | 描述 |
| --- | --- |
| [GCBuffer](#gcbuffer-构造) | 创建 GC 缓冲对象 |

---

## GCBuffer 构造

`GCBuffer(atLeast: number, gcObject: Class.Base) -> GCBuffer`

- 描述

    创建一个 GC 缓冲对象。当 GCBuffer 被销毁时，会等待指定时间后再移除关联的对象。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | atLeast | number | 至少等待的秒数（整数） |
    | gcObject | Class.Base | 要延迟移除的对象（必须有 remove 方法） |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | GCBuffer | GC 缓冲对象 |

- 示例

```lua
-- 创建一个 GC 缓冲，5秒后移除单位
local unit = y3.unit.create_unit(player, 134274912, point, 0)
local gc_buffer = New 'GCBuffer' (5, unit)

-- 当 gc_buffer 被销毁（如局部变量离开作用域或被设为 nil）时
-- unit 会在 5 秒后被移除
```
