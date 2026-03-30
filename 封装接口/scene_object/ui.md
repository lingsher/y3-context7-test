---
sidebarDepth: 1
---
# UI (场景对象)

# 索引

Y3 编辑器 UI 封装接口，提供高级方法操作 UI 对象。

---

| 接口 | 描述 |
| --- | --- |
| [get_by_handle](#get_by_handle) | 通过py层的界面实例获取lua层的界面实例 |
| [create_ui](#create_ui) | 创建界面控件 |
| [get_ui](#get_ui) |  |
| [create_child](#create_child) |  |
| [add_event](#add_event) | 创建界面事件 |
| [add_fast_event](#add_fast_event) | 创建快速界面事件 |
| [add_local_event](#add_local_event) | 创建本地界面事件 |
| [set_relative_parent_pos](#set_relative_parent_pos) | 设置相对父级位置. 目前不建议使用, 引擎层存在 bug, 建议手动计算位置赋值. |
| [send_event](#send_event) | 对玩家触发UI事件 |
| [set_visible](#set_visible) | 设置UI控件显隐 |
| [set_image](#set_image) | 设置图片 |
| [set_image_url](#set_image_url) | 设置来自网络的图片 |
| [set_image_color](#set_image_color) | 设置图片颜色 |
| [set_image_color_hex](#set_image_color_hex) | 设置图片颜色(hex) |
| [set_text](#set_text) | 设置文本 |
| [set_alpha](#set_alpha) | 设置控件透明度 |
| [set_anim_opacity](#set_anim_opacity) | 播放UI透明度动画 |
| [set_is_draggable](#set_is_draggable) | 设置控件是否可拖动 |
| [set_intercepts_operations](#set_intercepts_operations) | 设置控件是否拦截操作 |
| [set_z_order](#set_z_order) | 设置控件深度 |
| [set_max_progress_bar_value](#set_max_progress_bar_value) | 设置进度条最大值 |
| [set_current_progress_bar_value](#set_current_progress_bar_value) | 设置进度条当前值 |
| [set_button_enable](#set_button_enable) | 启用/禁用按钮 |
| [set_ui_size](#set_ui_size) | 设置控件尺寸 |
| [set_ui_9](#set_ui_9) | 设置控件9宫格 |
| [set_ui_9_enable](#set_ui_9_enable) | 设置控件9宫格启用 |
| [set_font_size](#set_font_size) | 设置文本字体大小 |
| [set_input_field_focus](#set_input_field_focus) | 让输入框获取焦点 |
| [set_input_field_not_focus](#set_input_field_not_focus) | 让输入框失去焦点 |
| [set_list_view_percent](#set_list_view_percent) | 设置列表视图百分比 |
| [set_skill_on_ui_comp](#set_skill_on_ui_comp) | 绑定技能对象到控件 |
| [bind_ability](#bind_ability) | 绑定技能 |
| [set_buff_on_ui](#set_buff_on_ui) | 绑定单位到魔法效果显示栏组件 |
| [set_item_on_ui](#set_item_on_ui) | 绑定物品对象到物品组件 |
| [set_prefab_ui_visible](#set_prefab_ui_visible) | 设置默认游戏界面的开关 |
| [set_ui_model_id](#set_ui_model_id) | 设置模型控件的模型 |
| [set_ui_model_unit](#set_ui_model_unit) | 设置UI模型控件的单位 |
| [change_mini_map_img](#change_mini_map_img) | 改变小地图图片 |
| [set_minimap_show_area](#set_minimap_show_area) | 设置小地图显示区域 |
| [set_ui_unit_slot](#set_ui_unit_slot) | 设置物品组件绑定单位 |
| [set_button_shortcut](#set_button_shortcut) | 设置按钮快捷键 |
| [set_btn_meta_key](#set_btn_meta_key) | 设置按钮组合快捷键 |
| [set_btn_status_string](#set_btn_status_string) | 设置按钮不同状态下的文本 |
| [set_btn_status_image](#set_btn_status_image) | 设置按钮不同状态下的图片 |
| [set_skill_btn_smart_cast_key](#set_skill_btn_smart_cast_key) | 设置智能施法快捷键 |
| [set_skill_btn_func_meta_key](#set_skill_btn_func_meta_key) | 设置智能施法组合快捷键 |
| [set_skill_btn_action_effect](#set_skill_btn_action_effect) | 播放/停止技能按钮激活动效 |
| [set_text_color](#set_text_color) | 设置文本颜色 |
| [set_text_color_hex](#set_text_color_hex) | 设置文本颜色(HEX) |
| [change_showroom_fov](#change_showroom_fov) | 设置模型控件的镜头视野 |
| [change_showroom_cposition](#change_showroom_cposition) | 设置模型控件的镜头坐标 |
| [change_showroom_crotation](#change_showroom_crotation) | 设置模型控件的镜头旋转 |
| [display_message](#display_message) | 系统消息提示 |
| [set_show_room_background_color](#set_show_room_background_color) | 设置界面模型控件背景色 |
| [set_widget_relative_rotation](#set_widget_relative_rotation) | 设置控件相对旋转 |
| [set_widget_absolute_coordinates](#set_widget_absolute_coordinates) | 设置控件绝对坐标 |
| [set_widget_absolute_rotation](#set_widget_absolute_rotation) | 设置控件绝对旋转 |
| [set_widget_absolute_scale](#set_widget_absolute_scale) | 设置控件绝对缩放 |
| [set_widget_relative_scale](#set_widget_relative_scale) | 设置控件相对缩放 |
| [change_minimap_display_mode](#change_minimap_display_mode) | 设置小地图显示模式 |
| [set_slider_value](#set_slider_value) | 设置滑动条的进度 |
| [unbind_widget](#unbind_widget) | 解绑控件 |
| [get_ui_comp_children](#get_ui_comp_children) | 遍历某个界面控件的子节点 |
| [get_childs](#get_childs) | 遍历某个界面控件的子节点 |
| [play_timeline_animation](#play_timeline_animation) | 播放时间轴动画 |
| [set_anim_pos](#set_anim_pos) | 播放动画移动 |
| [set_anim_scale](#set_anim_scale) | 播放UI缩放动画 |
| [set_ui_model_focus_pos](#set_ui_model_focus_pos) | 设置模型控件观察点 |
| [bind_unit_attr](#bind_unit_attr) | 绑定单位属性到玩家界面控件的属性 |
| [bind_player_prop](#bind_player_prop) | 绑定玩家属性到玩家界面控件的属性 |
| [bind_global_variable](#bind_global_variable) | 绑定全局变量到玩家界面控件的属性 |
| [set_text_format](#set_text_format) | 设置文本格式，如 `%.2f` 表示保留两位小数 |
| [unbind](#unbind) | 解绑界面控件属性绑定 |
| [bind_unit](#bind_unit) | 界面控件属性绑定指定单位 |
| [set_disable_image_type](#set_disable_image_type) | 设置禁用图片(图片类型) |
| [set_hover_image_type](#set_hover_image_type) | 设置悬浮图片(图片类型) |
| [set_press_image_type](#set_press_image_type) | 设置按下图片(图片类型) |
| [set_text_alignment](#set_text_alignment) | 设置文本的对齐方式 |
| [enable_drawing_unit_path](#enable_drawing_unit_path) | 开启绘制单位路径线 |
| [disable_drawing_unit_path](#disable_drawing_unit_path) | 关闭绘制单位路径线 |
| [remove](#remove) | 删除界面控件 |
| [is_removed](#is_removed) | 是否被删除 |
| [bind_ability_cd](#bind_ability_cd) | 绑定技能冷却时间到玩家界面控件的属性 |
| [bind_buff_time](#bind_buff_time) | 绑定魔法效果剩余时间到玩家界面控件的属性 |
| [enable_chat](#enable_chat) | 开启/禁用发送聊天功能 |
| [show_chat](#show_chat) | 显示/隐藏聊天框 |
| [clear_chat](#clear_chat) | 清空聊天信息 |
| [send_chat](#send_chat) | 发送私聊信息 |
| [get_checkbox_selected](#get_checkbox_selected) | 获取复选框当前选中状态 |
| [create_floating_text2](#create_floating_text2) | 创建悬浮文字 |
| [set_window_mode](#set_window_mode) | 设置窗口类型 |
| [set_graphics_quality](#set_graphics_quality) | 设置画质 |
| [set_screen_resolution](#set_screen_resolution) | 屏幕分辨率 |
| [get_relative_x](#get_relative_x) | 获取本地控件相对坐标的X |
| [get_relative_y](#get_relative_y) | 获取本地控件相对坐标的Y |
| [get_absolute_x](#get_absolute_x) | 获取本地控件绝对坐标的X |
| [get_absolute_y](#get_absolute_y) | 获取本地控件绝对坐标的Y |
| [get_relative_rotation](#get_relative_rotation) | 获取本地控件相对旋转 |
| [get_absolute_rotation](#get_absolute_rotation) | 获取本地控件绝对旋转 |
| [get_relative_scale_x](#get_relative_scale_x) | 获取本地控件相对缩放的X |
| [get_relative_scale_y](#get_relative_scale_y) | 获取本地控件相对缩放的Y |
| [get_absolute_scale_x](#get_absolute_scale_x) | 获取本地控件绝对缩放的X |
| [get_absolute_scale_y](#get_absolute_scale_y) | 获取本地控件绝对缩放的Y |
| [set_anim_rotate](#set_anim_rotate) | 设置动画旋转 |
| [to_string](#to_string) | 界面控件转化为字符串 |
| [get_slider_current_value](#get_slider_current_value) | 获取滑动条当前值 |
| [get_name](#get_name) | 获得界面控件名 |
| [get_child](#get_child) | 获取指定命名的子控件 |
| [get_width](#get_width) | 获得控件宽度 |
| [get_height](#get_height) | 获得控件高度 |
| [get_real_width](#get_real_width) | 获得控件真实宽度 |
| [get_real_height](#get_real_height) | 获得控件真实高度 |
| [get_parent](#get_parent) | 获得界面控件的父控件 |
| [get_input_field_content](#get_input_field_content) | 获得玩家输入框文本内容 |
| [is_visible](#is_visible) | 获得控件可见性 |
| [is_real_visible](#is_real_visible) | 获得控件真实可见性 |
| [set_pos](#set_pos) | 设置控件相对坐标 |
| [set_absolute_pos](#set_absolute_pos) | 设置控件绝对坐标 |
| [set_anchor](#set_anchor) | 设置界面控件的锚点 |
| [set_nearby_micro_switch](#set_nearby_micro_switch) | 设置聊天频道 |
| [get_screen_width](#get_screen_width) | 获取屏幕横向分辨率 |
| [get_screen_height](#get_screen_height) | 获取屏幕纵向分辨率 |
| [get_window_width](#get_window_width) | 获取窗口宽度 |
| [get_window_height](#get_window_height) | 获取窗口高度 |
| [set_follow_mouse](#set_follow_mouse) | 设置控件跟随鼠标 |
| [set_cursor](#set_cursor) | 设置鼠标样式 |
| [set_sequence_image](#set_sequence_image) | 设置序列帧图片 |
| [play_ui_sequence](#play_ui_sequence) | 播放序列帧 |
| [stop_ui_sequence](#stop_ui_sequence) | 停止播放序列帧 |
| [set_equip_slot_use_operation](#set_equip_slot_use_operation) | 设置使用物品操作方式 |
| [set_equip_slot_drag_operation](#set_equip_slot_drag_operation) | 设置拖拽物品操作方式 |
| [insert_ui_gridview_comp](#insert_ui_gridview_comp) | 添加UI到网格列表 |
| [set_ui_gridview_type](#set_ui_gridview_type) | 设置网格列表布局方式 |
| [set_ui_gridview_count](#set_ui_gridview_count) | 设置网格列表行数列数 |
| [set_ui_gridview_size](#set_ui_gridview_size) | 设置网格列表单元格宽高 |
| [set_ui_gridview_margin](#set_ui_gridview_margin) | 设置网格列表边距 |
| [set_ui_gridview_space](#set_ui_gridview_space) | 设置网格列表单元格间距 |
| [set_ui_gridview_align](#set_ui_gridview_align) | 设置网格列表对齐方式 |
| [set_ui_gridview_scroll](#set_ui_gridview_scroll) | 设置网格列表启用/禁止滚动 |
| [set_ui_gridview_size_adaptive](#set_ui_gridview_size_adaptive) | 设置网格列表启用/禁止尺寸随内容变化 |
| [set_ui_gridview_bar_percent](#set_ui_gridview_bar_percent) | 设置网格列表横向/纵向跳转百分比 |
| [set_ui_comp_parent](#set_ui_comp_parent) | 设置界面控件的父控件 |
| [clear_ui_comp_image](#clear_ui_comp_image) | 清空UI控件图片 |
| [set_scrollview_scroll](#set_scrollview_scroll) | 设置列表允许/禁止滚动 |
| [play_ui_effect](#play_ui_effect) | 特效控件播放特效 |
| [set_effect_background_color](#set_effect_background_color) | 设置特效控件的背景颜色 |
| [set_effect_camera_fov](#set_effect_camera_fov) | 设置特效控件的镜头视口 |
| [set_effect_camera_pos](#set_effect_camera_pos) | 设置特效控件的镜头坐标 |
| [set_effect_camera_rotation](#set_effect_camera_rotation) | 设置特效控件的镜头旋转 |
| [set_effect_camera_mode](#set_effect_camera_mode) | 设置模型控件的镜头模式 |
| [set_effect_focus_pos](#set_effect_focus_pos) | 设置特效控件的镜头焦点 |
| [set_effect_play_speed](#set_effect_play_speed) | 设置特效控件的播放速度 |

---

## get_by_handle

method in UI

- 描述

    通过py层的界面实例获取lua层的界面实例

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player |  |
    | handle | string |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | UI |  |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = y3.ui.get_by_handle(player, "handle")
```

---

## create_ui

method in UI

- 描述

    创建界面控件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | parent_ui | UI | ui控件 |
    | comp_type | y3.Const.UIComponentType | ui控件 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | UI |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local parent_ui = y3.ui.get_ui(y3.player.get_by_id(1), "ui_path")
local component_type = '物品'

local result = y3.ui.create_ui(player, parent_ui, component_type)
```

---

## get_ui

method in UI

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | ui_path | string | ui对象路径，自画板一级开始，父节点与子节点使用“.”链接 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | UI |  |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = y3.ui.get_ui(player, "ui_path")
```

---

## create_child

method in UI

- 描述

    

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | comp_type | y3.Const.UIComponentType | ui控件 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | UI |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")
local component_type = '物品'

local result = ui:create_child(component_type)
```

---

## add_event

method in UI

- 描述

    创建界面事件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | event | y3.Const.UIEvent | 界面事件类型 |
    | name | string | 事件名 |
    | data? | Serialization.SupportTypes | 自定义数据，在事件中通过 `data` 字段获取 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")
local ui_event = '左键-按下'

local result = ui:add_event(ui_event, "name")
```

---

## add_fast_event

method in UI

- 描述

    创建快速界面事件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | event | y3.Const.UIEvent | 界面事件类型 |
    | callback | fun(trg: | Trigger) |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | Trigger |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")
local ui_event = '左键-按下'

local result = ui:add_fast_event(ui_event, function() end)
```

---

## add_local_event

method in UI

- 描述

    创建本地界面事件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | event | y3.Const.UIEvent | 界面事件类型 |
    | callback | fun(local_player: | Player) # 回调函数 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")
local ui_event = '左键-按下'

ui:add_local_event(ui_event, function() end)
```

---

## set_relative_parent_pos

method in UI

- 描述

    设置相对父级位置. 目前不建议使用, 引擎层存在 bug, 建议手动计算位置赋值.

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | direction | y3.Const.UIRelativeParentPosType |  |
    | offset | number | 相对父级位置 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | UI |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")
local pos_type = '顶部'

local result = ui:set_relative_parent_pos(pos_type, 1.0)
```

---

## send_event

method in UI

- 描述

    对玩家触发UI事件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | event_name | string |  |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

ui:send_event("event_name")
```

---

## set_visible

method in UI

- 描述

    设置UI控件显隐

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | visible | boolean | 显示/隐藏 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_visible(true)
```

---

## set_image

method in UI

- 描述

    设置图片

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | img | py.Texture \| string | 图片id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")
local texture = 1

local result = ui:set_image("img")
```

---

## set_image_url

method in UI

- 描述

    设置来自网络的图片

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | url | string | 图片url |
    | aid? | string | 图片的唯一id，如果不指定会从url中提取。如果本地已经有该aid的图片，会直接使用本地图片。必须是操作系统可用的文件名。 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_image_url("url", "aid")
```

---

## set_image_color

method in UI

- 描述

    设置图片颜色

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | r | number | 红色 |
    | g | number | 绿色 |
    | b | number | 蓝色 |
    | a | number | 透明度 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_image_color(1.0, 1.0, 1.0, 1.0)
```

---

## set_image_color_hex

method in UI

- 描述

    设置图片颜色(hex)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | color | string | hex |
    | a | number | 透明度 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_image_color_hex("color", 1.0)
```

---

## set_text

method in UI

- 描述

    设置文本

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | str | string | 文本 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_text("str")
```

---

## set_alpha

method in UI

- 描述

    设置控件透明度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | value | number | 透明度 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_alpha(1.0)
```

---

## set_anim_opacity

method in UI

- 描述

    播放UI透明度动画

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | start_alpha | number | 开始alpha |
    | end_alpha | number | 结束alpha |
    | duration | number | 持续时间 |
    | ease_type? | y3.Const.EaseType | 曲线类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_anim_opacity(1.0, 1.0, 1.0)
```

---

## set_is_draggable

method in UI

- 描述

    设置控件是否可拖动

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | isdrag | boolean | 是否可拖动 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_is_draggable(true)
```

---

## set_intercepts_operations

method in UI

- 描述

    设置控件是否拦截操作

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | intercepts | boolean | 是否拦截操作 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_intercepts_operations(true)
```

---

## set_z_order

method in UI

- 描述

    设置控件深度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | deep | integer | 深度 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_z_order(1)
```

---

## set_max_progress_bar_value

method in UI

- 描述

    设置进度条最大值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | progress | number | 进度条最大值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_max_progress_bar_value(1.0)
```

---

## set_current_progress_bar_value

method in UI

- 描述

    设置进度条当前值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | progress | number | 进度条当前值 |
    | time | number? | 渐变时间 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_current_progress_bar_value(1.0, nil)
```

---

## set_button_enable

method in UI

- 描述

    启用/禁用按钮

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | enable | boolean | 启用/禁用按钮 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_button_enable(true)
```

---

## set_ui_size

method in UI

- 描述

    设置控件尺寸

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | width | number | 宽度 |
    | height | number | 高度 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_ui_size(1.0, 1.0)
```

---

## set_ui_9

method in UI

- 描述

    设置控件9宫格

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | x_left | integer | x |
    | x_right | integer | y |
    | y_top | integer | width |
    | y_bottom | integer | height |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_ui_9(1, 1, 1, 1)
```

---

## set_ui_9_enable

method in UI

- 描述

    设置控件9宫格启用

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | switch | boolean | 启用/禁用 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_ui_9_enable(true)
```

---

## set_font_size

method in UI

- 描述

    设置文本字体大小

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | size | integer | 字体大小 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_font_size(1)
```

---

## set_input_field_focus

method in UI

- 描述

    让输入框获取焦点

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_input_field_focus()
```

---

## set_input_field_not_focus

method in UI

- 描述

    让输入框失去焦点

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_input_field_not_focus()
```

---

## set_list_view_percent

method in UI

- 描述

    设置列表视图百分比

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | percent | number | 百分比 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

ui:set_list_view_percent(1.0)
```

---

## set_skill_on_ui_comp

method in UI

- 描述

    绑定技能对象到控件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | skill? | Ability | 技能对象 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_skill_on_ui_comp()
```

---

## bind_ability

method in UI

- 描述

    绑定技能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability? | Ability | 技能对象 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:bind_ability()
```

---

## set_buff_on_ui

method in UI

- 描述

    绑定单位到魔法效果显示栏组件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 单位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = ui:set_buff_on_ui(unit)
```

---

## set_item_on_ui

method in UI

- 描述

    绑定物品对象到物品组件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item | Item | 物品对象 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = ui:set_item_on_ui(item)
```

---

## set_prefab_ui_visible

method in UI

- 描述

    设置默认游戏界面的开关

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | visible | boolean | 游戏界面的开关 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

y3.ui.set_prefab_ui_visible(player, true)
```

---

## set_ui_model_id

method in UI

- 描述

    设置模型控件的模型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | modelid | py.ModelKey | 模型id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")
local model_key = 1

local result = ui:set_ui_model_id(model_key)
```

---

## set_ui_model_unit

method in UI

- 描述

    设置UI模型控件的单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | model_unit | Unit | 单位 |
    | clone_effect? | boolean | 继承特效 |
    | clone_attach? | boolean | 继承挂接模型 |
    | clone_material? | boolean | 继承材质变化 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")
local unit = y3.player.get_by_id(1):get_all_units()[1]

ui:set_ui_model_unit(unit, true, true, true)
```

---

## change_mini_map_img

method in UI

- 描述

    改变小地图图片

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | img | py.Texture | 图片id |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local texture = 1

y3.ui.change_mini_map_img(player, texture)
```

---

## set_minimap_show_area

method in UI

- 描述

    设置小地图显示区域

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | rect_area | Area | 矩形区域 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local area = y3.area.create_circle_area(y3.point(0, 0), 500)

y3.ui.set_minimap_show_area(player, area)
```

---

## set_ui_unit_slot

method in UI

- 描述

    设置物品组件绑定单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit |  |
    | field | y3.Const.SlotType | 背包槽位类型名 |
    | index | integer | 格子位置 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")
local unit = y3.player.get_by_id(1):get_all_units()[1]
local slot_type = y3.const.SlotType['NOT_IN_BAG']

local result = ui:set_ui_unit_slot(unit, slot_type, 1)
```

---

## set_button_shortcut

method in UI

- 描述

    设置按钮快捷键

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | integer | 快捷键 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_button_shortcut(1)
```

---

## set_btn_meta_key

method in UI

- 描述

    设置按钮组合快捷键

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | integer | 辅助按键 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_btn_meta_key(1)
```

---

## set_btn_status_string

method in UI

- 描述

    设置按钮不同状态下的文本

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | status | y3.Const.UIButtonStatus | 状态 |
    | text | string | 文本 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")
local status = y3.const.UIButtonStatus['常态']

local result = ui:set_btn_status_string(status, "text")
```

---

## set_btn_status_image

method in UI

- 描述

    设置按钮不同状态下的图片

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | status | y3.Const.UIButtonStatus | 状态 |
    | img | integer | 图片id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")
local status = y3.const.UIButtonStatus['常态']

local result = ui:set_btn_status_image(status, 1)
```

---

## set_skill_btn_smart_cast_key

method in UI

- 描述

    设置智能施法快捷键

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | integer | 快捷键 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_skill_btn_smart_cast_key(1)
```

---

## set_skill_btn_func_meta_key

method in UI

- 描述

    设置智能施法组合快捷键

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | integer | 辅助按键 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_skill_btn_func_meta_key(1)
```

---

## set_skill_btn_action_effect

method in UI

- 描述

    播放/停止技能按钮激活动效

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | isopen | boolean | 播放/停止技能按钮激活动效 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_skill_btn_action_effect(true)
```

---

## set_text_color

method in UI

- 描述

    设置文本颜色

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | r | number | 红色(0-255) |
    | g | number | 绿色(0-255) |
    | b | number | 蓝色(0-255) |
    | a? | number | 不透明度(0-255) |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_text_color(1.0, 1.0, 1.0, 1.0)
```

---

## set_text_color_hex

method in UI

- 描述

    设置文本颜色(HEX)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | color | string | 如 `ffcc00` |
    | a? | number | 不透明度，0为完全透明，100为完全不透明 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_text_color_hex("color", 1.0)
```

---

## change_showroom_fov

method in UI

- 描述

    设置模型控件的镜头视野

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | fov | number | 视野范围 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:change_showroom_fov(1.0)
```

---

## change_showroom_cposition

method in UI

- 描述

    设置模型控件的镜头坐标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | x | number | x轴 |
    | y | number | y轴 |
    | z | number | z轴 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:change_showroom_cposition(1.0, 1.0, 1.0)
```

---

## change_showroom_crotation

method in UI

- 描述

    设置模型控件的镜头旋转

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | x | number | x轴 |
    | y | number | y轴 |
    | z | number | z轴 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:change_showroom_crotation(1.0, 1.0, 1.0)
```

---

## display_message

method in UI

- 描述

    系统消息提示

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | msg | string | 消息 |
    | time | number | 持续时间 |
    | isSupportLanguage? | boolean | 是否支持语言环境 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

y3.ui.display_message(player, "msg", 1.0, true)
```

---

## set_show_room_background_color

method in UI

- 描述

    设置界面模型控件背景色

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | r | number | 红色 |
    | g | number | 绿色 |
    | b | number | 蓝色 |
    | a | number | 透明度 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_show_room_background_color(1.0, 1.0, 1.0, 1.0)
```

---

## set_widget_relative_rotation

method in UI

- 描述

    设置控件相对旋转

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | rot | number | 角度 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_widget_relative_rotation(1.0)
```

---

## set_widget_absolute_coordinates

method in UI

- 描述

    设置控件绝对坐标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | x | number | x轴 |
    | y | number | y轴 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_widget_absolute_coordinates(1.0, 1.0)
```

---

## set_widget_absolute_rotation

method in UI

- 描述

    设置控件绝对旋转

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | rot | number | 角度 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_widget_absolute_rotation(1.0)
```

---

## set_widget_absolute_scale

method in UI

- 描述

    设置控件绝对缩放

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | x | number | x轴 |
    | y | number | y轴 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_widget_absolute_scale(1.0, 1.0)
```

---

## set_widget_relative_scale

method in UI

- 描述

    设置控件相对缩放

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | x | number | x轴 |
    | y | number | y轴 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_widget_relative_scale(1.0, 1.0)
```

---

## change_minimap_display_mode

method in UI

- 描述

    设置小地图显示模式

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | type | integer | 小地图显示模式 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

y3.ui.change_minimap_display_mode(player, 1)
```

---

## set_slider_value

method in UI

- 描述

    设置滑动条的进度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | percent | number | 滑动条的进度 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_slider_value(1.0)
```

---

## unbind_widget

method in UI

- 描述

    解绑控件

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:unbind_widget()
```

---

## get_ui_comp_children

method in UI

- 描述

    遍历某个界面控件的子节点

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | UI[] |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:get_ui_comp_children()
```

---

## get_childs

method in UI

- 描述

    遍历某个界面控件的子节点

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | UI[] |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:get_childs()
```

---

## play_timeline_animation

method in UI

- 描述

    播放时间轴动画

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | anim | string \| y3.Const.UIAnimKey | 动画 |
    | speed? | number | 播放速度 |
    | mode? | boolean \| '保持' \| '常规' \| '往复' \| '循环' | 播放模式 |
    | start? | integer | 开始帧 |
    | finish? | integer | 结束帧 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

y3.ui.play_timeline_animation(player, "anim", 1.0, '保持', 1, 1)
```

---

## set_anim_pos

method in UI

- 描述

    播放动画移动

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | start_x | number | 开始x |
    | start_y | number | 开始y |
    | end_x | number | 结束x |
    | end_y | number | 结束y |
    | duration | number | 持续时间 |
    | ease_type? | integer | 曲线类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | UI |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_anim_pos(1.0, 1.0, 1.0, 1.0, 1.0, 1)
```

---

## set_anim_scale

method in UI

- 描述

    播放UI缩放动画

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | start_x | number | 开始x |
    | start_y | number | 开始y |
    | end_x | number | 结束x |
    | end_y | number | 结束y |
    | duration | number | 持续时间 |
    | ease_type? | integer | 曲线类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_anim_scale(1.0, 1.0, 1.0, 1.0, 1.0, 1)
```

---

## set_ui_model_focus_pos

method in UI

- 描述

    设置模型控件观察点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | x | number | x轴 |
    | y | number | y轴 |
    | z | number | z轴 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_ui_model_focus_pos(1.0, 1.0, 1.0)
```

---

## bind_unit_attr

method in UI

- 描述

    绑定单位属性到玩家界面控件的属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | uiAttr | y3.Const.UIAttr | 界面控件属性 |
    | attr_name | y3.Const.UnitAttr | 单位属性 |
    | accuracy? | integer | 小数精度，默认为0 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")
local ui_attr = "文本"

local result = ui:bind_unit_attr(ui_attr, "attr_name", 1)
```

---

## bind_player_prop

method in UI

- 描述

    绑定玩家属性到玩家界面控件的属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | uiAttr | y3.Const.UIAttr | 界面控件属性 |
    | player | Player | 玩家 |
    | attr_or_var | y3.Const.PlayerAttr | 玩家属性key |
    | accuracy? | integer | 小数精度，默认为0 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")
local ui_attr = "文本"

local result = ui:bind_player_prop(ui_attr, player, "attr_or_var", 1)
```

---

## bind_global_variable

method in UI

- 描述

    绑定全局变量到玩家界面控件的属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | uiAttr | y3.Const.UIAttr \| string | 界面控件属性 |
    | globalVar | string | 全局属性 |
    | accuracy? | integer | 小数精度 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")
local ui_attr = "文本"

local result = ui:bind_global_variable("uiAttr", "globalVar", 1)
```

---

## set_text_format

method in UI

- 描述

    设置文本格式，如 `%.2f` 表示保留两位小数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | format_str | string |  |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

ui:set_text_format("format_str")
```

---

## unbind

method in UI

- 描述

    解绑界面控件属性绑定

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | uiAttr | string | 界面控件属性 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:unbind("uiAttr")
```

---

## bind_unit

method in UI

- 描述

    界面控件属性绑定指定单位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 单位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = ui:bind_unit(unit)
```

---

## set_disable_image_type

method in UI

- 描述

    设置禁用图片(图片类型)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | img | integer | 图片id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_disable_image_type(1)
```

---

## set_hover_image_type

method in UI

- 描述

    设置悬浮图片(图片类型)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | img | integer | 图片id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_hover_image_type(1)
```

---

## set_press_image_type

method in UI

- 描述

    设置按下图片(图片类型)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | img | integer | 图片id |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_press_image_type(1)
```

---

## set_text_alignment

method in UI

- 描述

    设置文本的对齐方式

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | h? | y3.Const.UIHAlignmentType | 横向对齐方式 |
    | v? | y3.Const.UIVAlignmentType | 纵向对齐方式 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_text_alignment()
```

---

## enable_drawing_unit_path

method in UI

- 描述

    开启绘制单位路径线

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | unit | Unit | 单位 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

y3.ui.enable_drawing_unit_path(player, unit)
```

---

## disable_drawing_unit_path

method in UI

- 描述

    关闭绘制单位路径线

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | unit | Unit | 单位 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local player = y3.player.get_by_id(1)

y3.ui.disable_drawing_unit_path(player, unit)
```

---

## remove

method in UI

- 描述

    删除界面控件

- 参数

    无

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

ui:remove()
```

---

## is_removed

method in UI

- 描述

    是否被删除

- 参数

    无

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

ui:is_removed()
```

---

## bind_ability_cd

method in UI

- 描述

    绑定技能冷却时间到玩家界面控件的属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | uiAttr | string | 界面控件属性 |
    | skill | Ability | 技能 |
    | isSmooth? | boolean | 是否平滑 |
    | digits? | integer | 小数位数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = ui:bind_ability_cd("uiAttr", ability, true, 1)
```

---

## bind_buff_time

method in UI

- 描述

    绑定魔法效果剩余时间到玩家界面控件的属性

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | uiAttr | string | 界面控件属性 |
    | buff | Buff | 魔法效果 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")
local unit = y3.player.get_by_id(1):get_all_units()[1]
local buff = unit:find_buff(134274569)

local result = ui:bind_buff_time("uiAttr", buff)
```

---

## enable_chat

method in UI

- 描述

    开启/禁用发送聊天功能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | enable | boolean | 开启/禁用发送聊天功能 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:enable_chat(true)
```

---

## show_chat

method in UI

- 描述

    显示/隐藏聊天框

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 目标玩家 |
    | enable | boolean | 显示/隐藏聊天框 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:show_chat(player, true)
```

---

## clear_chat

method in UI

- 描述

    清空聊天信息

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:clear_chat()
```

---

## send_chat

method in UI

- 描述

    发送私聊信息

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | msg | string | 信息 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:send_chat(player, "msg")
```

---

## get_checkbox_selected

method in UI

- 描述

    获取复选框当前选中状态

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 当前选中状态 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:get_checkbox_selected()
```

---

## create_floating_text2

method in UI

- 描述

    创建悬浮文字

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | Point | 点 |
    | text_type | y3.Const.FloatTextType \| string \| integer | 跳字类型 |
    | str | string | 文字 |
    | jump_word_track? | y3.Const.FloatTextJumpType | 跳字轨迹类型，如果不传会使用随机轨迹 |
    | player_group? | PlayerGroup | 可见的玩家组。传入 `nil` 表示所有玩家都可见 |

- 返回值

    无

- 示例

```lua
local point = y3.point(0, 0)

y3.ui.create_floating_text2(point, "text_type", "str")
```

---

## set_window_mode

method in UI

- 描述

    设置窗口类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | window_mode | Game.WindowMode | 窗口类型 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

y3.ui.set_window_mode(player, "window_mode")
```

---

## set_graphics_quality

method in UI

- 描述

    设置画质

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | quality | string | 画质 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

y3.ui.set_graphics_quality(player, "quality")
```

---

## set_screen_resolution

method in UI

- 描述

    屏幕分辨率

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | x | number | x轴 |
    | y | number | y轴 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

y3.ui.set_screen_resolution(player, 1.0, 1.0)
```

---

## get_relative_x

method in UI

- 描述

    获取本地控件相对坐标的X

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | x相对坐标 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:get_relative_x()
```

---

## get_relative_y

method in UI

- 描述

    获取本地控件相对坐标的Y

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | y坐标 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:get_relative_y()
```

---

## get_absolute_x

method in UI

- 描述

    获取本地控件绝对坐标的X

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | x绝对坐标 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:get_absolute_x()
```

---

## get_absolute_y

method in UI

- 描述

    获取本地控件绝对坐标的Y

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | y绝对坐标 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:get_absolute_y()
```

---

## get_relative_rotation

method in UI

- 描述

    获取本地控件相对旋转

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 相对旋转 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:get_relative_rotation()
```

---

## get_absolute_rotation

method in UI

- 描述

    获取本地控件绝对旋转

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 绝对旋转 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:get_absolute_rotation()
```

---

## get_relative_scale_x

method in UI

- 描述

    获取本地控件相对缩放的X

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | x相对缩放 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:get_relative_scale_x()
```

---

## get_relative_scale_y

method in UI

- 描述

    获取本地控件相对缩放的Y

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | y绝对缩放 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:get_relative_scale_y()
```

---

## get_absolute_scale_x

method in UI

- 描述

    获取本地控件绝对缩放的X

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | x绝对缩放 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:get_absolute_scale_x()
```

---

## get_absolute_scale_y

method in UI

- 描述

    获取本地控件绝对缩放的Y

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | y绝对缩放 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:get_absolute_scale_y()
```

---

## set_anim_rotate

method in UI

- 描述

    设置动画旋转

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | start_rotation | number | 开始旋转 |
    | end_rotation | number | 结束旋转 |
    | duration | number | 持续时间 |
    | ease_type? | integer | 曲线类型 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

ui:set_anim_rotate(1.0, 1.0, 1.0, 1)
```

---

## to_string

method in UI

- 描述

    界面控件转化为字符串

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:to_string()
```

---

## get_slider_current_value

method in UI

- 描述

    获取滑动条当前值

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 滑动条当前值 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:get_slider_current_value()
```

---

## get_name

method in UI

- 描述

    获得界面控件名

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 控件名 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:get_name()
```

---

## get_child

method in UI

- 描述

    获取指定命名的子控件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | name | string |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | UI | ui控件 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:get_child("name")
```

---

## get_width

method in UI

- 描述

    获得控件宽度

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 控件宽度 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:get_width()
```

---

## get_height

method in UI

- 描述

    获得控件高度

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 控件高度 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:get_height()
```

---

## get_real_width

method in UI

- 描述

    获得控件真实宽度

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 控件真实宽度 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:get_real_width()
```

---

## get_real_height

method in UI

- 描述

    获得控件真实高度

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | number | 控件真实高度 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:get_real_height()
```

---

## get_parent

method in UI

- 描述

    获得界面控件的父控件

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | UI? | ui控件 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:get_parent()
```

---

## get_input_field_content

method in UI

- 描述

    获得玩家输入框文本内容

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 文本内容 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:get_input_field_content()
```

---

## is_visible

method in UI

- 描述

    获得控件可见性

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 控件可见性 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:is_visible()
```

---

## is_real_visible

method in UI

- 描述

    获得控件真实可见性

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:is_real_visible()
```

---

## set_pos

method in UI

- 描述

    设置控件相对坐标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | x | number | x轴 |
    | y | number | y轴 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_pos(1.0, 1.0)
```

---

## set_absolute_pos

method in UI

- 描述

    设置控件绝对坐标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | x | number | x轴 |
    | y | number | y轴 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_absolute_pos(1.0, 1.0)
```

---

## set_anchor

method in UI

- 描述

    设置界面控件的锚点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | x | number | x轴 |
    | y | number | y轴 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_anchor(1.0, 1.0)
```

---

## set_nearby_micro_switch

method in UI

- 描述

    设置聊天频道

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | switch | boolean | 开关 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_nearby_micro_switch(true)
```

---

## get_screen_width

method in UI

- 描述

    获取屏幕横向分辨率

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 横向分辨率 |

- 示例

```lua
local result = y3.ui.get_screen_width()
```

---

## get_screen_height

method in UI

- 描述

    获取屏幕纵向分辨率

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 纵向分辨率 |

- 示例

```lua
local result = y3.ui.get_screen_height()
```

---

## get_window_width

method in UI

- 描述

    获取窗口宽度

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer |  |

- 示例

```lua
local result = y3.ui.get_window_width()
```

---

## get_window_height

method in UI

- 描述

    获取窗口高度

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer |  |

- 示例

```lua
local result = y3.ui.get_window_height()
```

---

## set_follow_mouse

method in UI

- 描述

    设置控件跟随鼠标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | follow_mouse | boolean |  |
    | offset_x? | number | 偏移x轴 |
    | offset_y? | number | 偏移y轴 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:set_follow_mouse(true, 1.0, 1.0)
```

---

## set_cursor

method in UI

- 描述

    设置鼠标样式

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player |  |
    | state | y3.Const.CursorState |  |
    | key | py.CursorKey |  |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")
local cursor_state = '常态悬浮'

local result = ui:set_cursor(player, cursor_state, 134274569)
```

---

## set_sequence_image

method in UI

- 描述

    设置序列帧图片

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | image_id | integer | 序列帧图片ID |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

ui:set_sequence_image(1)
```

---

## play_ui_sequence

method in UI

- 描述

    播放序列帧

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | loop? | boolean | 是否循环 |
    | space? | number | 间隔帧数 |
    | start_frame? | integer | 起始帧 |
    | end_frame? | integer | 结束帧 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | self |  |

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

local result = ui:play_ui_sequence(true, 1.0, 1, 1)
```

---

## stop_ui_sequence

method in UI

- 描述

    停止播放序列帧

- 参数

    无

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

ui:stop_ui_sequence()
```

---

## set_equip_slot_use_operation

method in UI

- 描述

    设置使用物品操作方式

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | use_operation | Item.UseOperation | 操作方式 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")
local use_operation = '无'

ui:set_equip_slot_use_operation(use_operation)
```

---

## set_equip_slot_drag_operation

method in UI

- 描述

    设置拖拽物品操作方式

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | drag_operation | Item.DrapOperation | 操作方式 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")
local drop_operation = '无'

ui:set_equip_slot_drag_operation(drop_operation)
```

---

## insert_ui_gridview_comp

method in UI

- 描述

    添加UI到网格列表

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | child | UI |  |
    | child_index? | integer | 默认是最后一个, 如果位置大于当前最大位置, 也是默认最后一个 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")
local parent_ui = y3.ui.get_ui(y3.player.get_by_id(1), "ui_path")

ui:insert_ui_gridview_comp(parent_ui, 1)
```

---

## set_ui_gridview_type

method in UI

- 描述

    设置网格列表布局方式

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | layout_type | integer | 布局方式 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

ui:set_ui_gridview_type(1)
```

---

## set_ui_gridview_count

method in UI

- 描述

    设置网格列表行数列数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | row_count | integer | 行数 |
    | column_count | integer | 列数 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

ui:set_ui_gridview_count(1, 1)
```

---

## set_ui_gridview_size

method in UI

- 描述

    设置网格列表单元格宽高

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | width | number | 宽 |
    | height | number | 高 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

ui:set_ui_gridview_size(1.0, 1.0)
```

---

## set_ui_gridview_margin

method in UI

- 描述

    设置网格列表边距

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | top | number | 上 |
    | bottom | number | 下 |
    | left | number | 左 |
    | right | number | 右 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

ui:set_ui_gridview_margin(1.0, 1.0, 1.0, 1.0)
```

---

## set_ui_gridview_space

method in UI

- 描述

    设置网格列表单元格间距

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | row | number | 行间距（纵向） |
    | col | number | 列间距（横向） |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

ui:set_ui_gridview_space(1.0, 1.0)
```

---

## set_ui_gridview_align

method in UI

- 描述

    设置网格列表对齐方式

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | align_type | integer | 对齐方式 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

ui:set_ui_gridview_align(1)
```

---

## set_ui_gridview_scroll

method in UI

- 描述

    设置网格列表启用/禁止滚动

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | enable | boolean | 是否启用 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

ui:set_ui_gridview_scroll(true)
```

---

## set_ui_gridview_size_adaptive

method in UI

- 描述

    设置网格列表启用/禁止尺寸随内容变化

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | enable | boolean | 是否启用 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

ui:set_ui_gridview_size_adaptive(true)
```

---

## set_ui_gridview_bar_percent

method in UI

- 描述

    设置网格列表横向/纵向跳转百分比

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | direction | integer | 横向/纵向 |
    | ratio | number | 百分比 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

ui:set_ui_gridview_bar_percent(1, 1.0)
```

---

## set_ui_comp_parent

method in UI

- 描述

    设置界面控件的父控件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | parent_uid | string | 父控件uid |
    | keep_pos? | boolean | 保持位置 |
    | keep_rotation? | boolean | 保持旋转 |
    | keep_scale? | boolean | 保持缩放 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

ui:set_ui_comp_parent("parent_uid", true, true, true)
```

---

## clear_ui_comp_image

method in UI

- 描述

    清空UI控件图片

- 参数

    无

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

ui:clear_ui_comp_image()
```

---

## set_scrollview_scroll

method in UI

- 描述

    设置列表允许/禁止滚动

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | enable | boolean | 是否允许滚动 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

ui:set_scrollview_scroll(true)
```

---

## play_ui_effect

method in UI

- 描述

    特效控件播放特效

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | effect_id | integer | 特效id |
    | is_loop? | boolean | 是否循环 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

ui:play_ui_effect(1, true)
```

---

## set_effect_background_color

method in UI

- 描述

    设置特效控件的背景颜色

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | r | number | R |
    | g | number | G |
    | b | number | B |
    | a | number | A |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

ui:set_effect_background_color(1.0, 1.0, 1.0, 1.0)
```

---

## set_effect_camera_fov

method in UI

- 描述

    设置特效控件的镜头视口

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | fov | number | fov |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

ui:set_effect_camera_fov(1.0)
```

---

## set_effect_camera_pos

method in UI

- 描述

    设置特效控件的镜头坐标

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | x | number | x |
    | y | number | y |
    | z | number | z |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

ui:set_effect_camera_pos(1.0, 1.0, 1.0)
```

---

## set_effect_camera_rotation

method in UI

- 描述

    设置特效控件的镜头旋转

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | pitch | number | pitch |
    | roll | number | roll |
    | yaw | number | yaw |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

ui:set_effect_camera_rotation(1.0, 1.0, 1.0)
```

---

## set_effect_camera_mode

method in UI

- 描述

    设置模型控件的镜头模式

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | camera_mod | y3.Const.UIEffectCameraMode | 镜头模式 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")
local camera_mode = '自定义模式'

ui:set_effect_camera_mode(camera_mode)
```

---

## set_effect_focus_pos

method in UI

- 描述

    设置特效控件的镜头焦点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | x | number | x |
    | y | number | y |
    | z | number | z |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

ui:set_effect_focus_pos(1.0, 1.0, 1.0)
```

---

## set_effect_play_speed

method in UI

- 描述

    设置特效控件的播放速度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | play_speed | number | 播放速度 |

- 返回值

    无

- 示例

```lua
local player = y3.player.get_by_id(1)
local ui = y3.ui.get_ui(player, "ui_path")

ui:set_effect_play_speed(1.0)
```

---
