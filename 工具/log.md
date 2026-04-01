---
sidebarDepth: 1
---
# log (日志系统)

# 索引

Y3 框架的日志系统，提供多级别日志输出。支持输出到控制台、游戏窗口、编辑器助手和文件。

---

## 全局对象

| 对象 | 描述 |
| --- | --- |
| [log](#log-对象) | 全局日志对象 |
| [print](#print-函数) | 重载的 print 函数 |

## 日志级别

| 级别 | 方法 | 说明 |
| --- | --- | --- |
| trace | `log.trace()` | 最详细的跟踪信息 |
| debug | `log.debug()` | 调试信息 |
| info | `log.info()` | 一般信息 |
| warn | `log.warn()` | 警告信息 |
| error | `log.error()` | 错误信息（会上报） |
| fatal | `log.fatal()` | 致命错误（会上报） |

---

## log 对象

全局日志对象，使用 `Log` 类创建。

### log.trace

`log.trace(...)`

- 描述

    输出跟踪级别日志

- 示例

```lua
-- 跟踪级别日志
log.trace('进入函数', 'calculate_damage')
```

### log.debug

`log.debug(...)`

- 描述

    输出调试级别日志

- 示例

```lua
-- 调试级别日志
log.debug('变量值:', damage, target_hp)
```

### log.info

`log.info(...)`

- 描述

    输出信息级别日志

- 示例

```lua
-- 信息级别日志
log.info('玩家进入游戏:', player:get_name())
```

### log.warn

`log.warn(...)`

- 描述

    输出警告级别日志

- 示例

```lua
-- 警告级别日志
log.warn('配置文件缺失，使用默认值')
```

### log.error

`log.error(...)`

- 描述

    输出错误级别日志。错误信息会自动上报。

- 示例

```lua
-- 错误级别日志
log.error('技能释放失败:', skill_id)
```

### log.fatal

`log.fatal(...)`

- 描述

    输出致命错误级别日志。错误信息会自动上报。

- 示例

```lua
-- 致命错误日志
log.fatal('无法初始化游戏:', err_msg)
```

---

## print 函数

`print(...)`

- 描述

    重载的全局 print 函数。等价于 `log.debug`，但在开发模式中还会确保打印到游戏窗口。

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ... | any | 要打印的值（自动转为字符串） |

- 示例

```lua
-- 使用 print 输出调试信息
print('当前帧:', frame_count)
print('伤害计算:', damage, '目标:', target)
```

