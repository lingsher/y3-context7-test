---
sidebarDepth: 1
---
# Sound (运行时对象)

# 索引

Y3 编辑器 Sound 封装接口，提供高级方法操作 Sound 对象。

---

| 接口 | 描述 |
| --- | --- |
| [get_by_handle](#get_by_handle) |  |
| [play](#play) | 播放声音 |
| [play_3d](#play_3d) | 播放3D声音 |
| [play_with_object](#play_with_object) | 跟随单位播放声音 |
| [stop](#stop) | 停止播放声音 |
| [set_volume](#set_volume) | 设置音量 |

---

## get_by_handle

method in Sound

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | py_sound | py.SoundEntity |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Sound |  |

- 示例

```lua
local result = y3.sound.get_by_handle(sound_entity)
```

---

## play

method in Sound

- 描述

    播放声音

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | sound | py.AudioKey | 声音 |
    | options | Sound.PlayOptions? | 播放选项 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Sound? |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local audio_key = 1

local result = y3.sound.play(player, audio_key)
```

---

## play_3d

method in Sound

- 描述

    播放3D声音

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | sound | py.AudioKey | 声音 |
    | point | Point | 目标点 |
    | options | Sound.Play3DOptions? | 播放选项 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Sound? |  |

- 示例

```lua
local point = y3.point(0, 0)
local player = y3.player.get_by_id(1)
local audio_key = 1

local result = y3.sound.play_3d(player, audio_key, point)
```

---

## play_with_object

method in Sound

- 描述

    跟随单位播放声音

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | sound | py.AudioKey | 声音 |
    | unit | Unit | 跟随的单位 |
    | options | Sound.PlayUnitOptions? | 播放选项 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Sound? |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)
local audio_key = 1

local result = y3.sound.play_with_object(player, audio_key, unit)
```

---

## stop

method in Sound

- 描述

    停止播放声音

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | is_immediately? | boolean | 是否立即停止 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local sound = y3.sound.play(player, 1)
if sound then

    sound:stop(player, true)
end
```

---

## set_volume

method in Sound

- 描述

    设置音量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | volume | integer | 音量(0-100) |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local sound = y3.sound.play(player, 1)
if sound then

    sound:set_volume(player, 1)
end
```

---
