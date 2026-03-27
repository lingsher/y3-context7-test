---
sidebarDepth: 1
---
# 全局API (GlobalAPI)

# 索引

Y3 编辑器全局API，包含数学运算、类型转换、形状创建等全局函数。

---

| 接口 | 描述 |
| --- | --- |
| [api_clear_tag](#api_clear_tag) | 清空标签 |
| [api_clear_kv](#api_clear_kv) | 清空自定义键值 |
| [has_tag](#has_tag) | 判断Actor是否有Tag |
| [api_has_kv_any](#api_has_kv_any) | 判断Actor是否有kv |
| [is_str_include_other](#is_str_include_other) | 字符串A是否包含字符串B |
| [set_actor_trigger_enabled](#set_actor_trigger_enabled) | 使能Actor身上的触发器 |
| [trigger_actor_trigger](#trigger_actor_trigger) | 触发Actor身上的触发器 |
| [reg_actor_trigger](#reg_actor_trigger) | 注册Actor上的触发器并生效 |
| [unreg_actor_trigger](#unreg_actor_trigger) | 注销Actor上的触发器 |
| [create_sector_shape](#create_sector_shape) | 创建一个扇形 |
| [create_circular_shape](#create_circular_shape) | 创建一个圆形 |
| [create_rectangle_shape](#create_rectangle_shape) | 创建一个矩形 |
| [create_annular_shape](#create_annular_shape) | 创建一个环形 |
| [coord_to_point](#coord_to_point) | 坐标值转化为FVector3 |
| [float_to_vector3](#float_to_vector3) | 三维坐标值转化为FVector3 |
| [get_vector3_x](#get_vector3_x) | 返回三维向量的X |
| [get_vector3_y](#get_vector3_y) | 返回三维向量的Y |
| [get_vector3_z](#get_vector3_z) | 返回三维向量的Z |
| [float_to_rotation](#float_to_rotation) | 三维坐标值转化为FRotation |
| [get_rotation_roll](#get_rotation_roll) | 返回旋转的Roll |
| [get_rotation_yaw](#get_rotation_yaw) | 返回旋转的YAW |
| [get_rotation_pitch](#get_rotation_pitch) | 返回旋转的PITCH |
| [int_iterator](#int_iterator) | 整数迭代器，最大迭代次数不超过2^20 |
| [int_iterator2](#int_iterator2) | 整数迭代器 |
| [list_index_iterator](#list_index_iterator) | 列表索引迭代器 |
| [table_iterator](#table_iterator) | table迭代器(废弃) |
| [get_iter_table_key_str](#get_iter_table_key_str) | get_iter_table_key_str |
| [get_iter_table_key_int](#get_iter_table_key_int) | get_iter_table_key_int |
| [int32_arithmetic_operation](#int32_arithmetic_operation) | Int32运算 |
| [int32_plus_one](#int32_plus_one) | Int32自增1 |
| [int32_min](#int32_min) | Int32取较小值 |
| [int32_max](#int32_max) | Int32取较大值 |
| [get_point_offset_vector](#get_point_offset_vector) | 点向方向偏移 |
| [int64_to_str](#int64_to_str) | int64转换字符串 |
| [to_str_default](#to_str_default) | to_str_default |
| [api_remove_kv](#api_remove_kv) | 删除键值对 |
| [get_unit_key_pool_num](#get_unit_key_pool_num) | 获取单位编号池内单位编号数量 |
| [plane_range_between_2_point](#plane_range_between_2_point) | 两点之间距离 |
| [int32_to_fixed](#int32_to_fixed) | 整数转定点数 |
| [fix32_equal_with_precision](#fix32_equal_with_precision) | 实数近似比较(4位小数) |
| [fixed_to_int32](#fixed_to_int32) | 定点数转整数 |
| [ability_index_to_int32](#ability_index_to_int32) | 技能槽位转整数 |
| [fixed_to_str](#fixed_to_str) | 定点数转字符串 |
| [fvector3_to_str](#fvector3_to_str) | 定点FVector3转字符串 |
| [fvector2_to_str](#fvector2_to_str) | 定点FVector2转字符串 |
| [float_to_str](#float_to_str) | 浮点数转字符串 |
| [vector3_to_str](#vector3_to_str) | 浮点Vector3转字符串 |
| [str_to_vector3](#str_to_vector3) | 字符串转Vector3 |
| [vector2_to_str](#vector2_to_str) | 浮点Vector2转字符串 |
| [shape_to_str](#shape_to_str) | Shape转字符串 |
| [dynamic_to_str](#dynamic_to_str) | 动态类型数转字符串 |
| [int32_to_str](#int32_to_str) | int32_to_str |
| [bool_to_str](#bool_to_str) | 布尔型转字符串 |
| [i2s](#i2s) | 整数转字符串 |
| [join_s](#join_s) | 字符串拼接 |
| [join_s_new](#join_s_new) | 字符串拼接 |
| [root](#root) | 开方 |
| [replace_str](#replace_str) | 字符串替换 |
| [fixed_arithmetic_operation](#fixed_arithmetic_operation) | 定点数运算 |
| [vector3_arithmetic_operation](#vector3_arithmetic_operation) | 三维向量运算 |
| [vector3_length](#vector3_length) | 三维向量的长度 |
| [vector3_normalize](#vector3_normalize) | 三维向量归一化 |
| [get_vector3_normalize](#get_vector3_normalize) | 三维向量的归一化向量 |
| [vector3_multiply_scalar](#vector3_multiply_scalar) | 三维向量乘以标量 |
| [vector3_to_euler](#vector3_to_euler) | 三维向量转欧拉角 |
| [vector3_angle_axis](#vector3_angle_axis) | 获得三维向量绕轴旋转后的向量 |
| [fixed_plus_one](#fixed_plus_one) | 定点数自增1 |
| [fixed_min](#fixed_min) | 取两个定点数最小值 |
| [fixed_max](#fixed_max) | 取两个定点数最小大值 |
| [angle_arithmetic_operation](#angle_arithmetic_operation) | 角度计算 |
| [degree_to_radian](#degree_to_radian) | 转换度到弧度 |
| [radian_sin](#radian_sin) | 正弦 |
| [radian_cos](#radian_cos) | 余弦 |
| [radian_tan](#radian_tan) | 正切 |
| [radian_asin](#radian_asin) | 反正弦 |
| [radian_acos](#radian_acos) | 反余弦 |
| [radian_atan](#radian_atan) | 反正切 |
| [radian_atan_x_y](#radian_atan_x_y) | 反正切(Y:X) |
| [sqrt](#sqrt) | 平方根 |
| [pow](#pow) | 求幂 |
| [abs](#abs) | 求绝对值 |
| [int_abs](#int_abs) | 求绝对值 |
| [interval](#interval) | 区间 |
| [nearest_quadratic_number](#nearest_quadratic_number) | 找最近的二次方数 |
| [ceil](#ceil) | 最小整数 |
| [floor](#floor) | 最大整数 |
| [interpolate](#interpolate) | 插值 |
| [invert_interpolate](#invert_interpolate) | 反插值 |
| [log10](#log10) | 对数10 |
| [log](#log) | 对数 |
| [get_max_in_list](#get_max_in_list) | 返回组内最大值 |
| [get_min_in_list](#get_min_in_list) | 返回组内最小值 |
| [round](#round) | 四舍五入 |
| [sign](#sign) | 返回正负符号 |
| [round_dec](#round_dec) | 保留X位小数 |
| [fixed_trigonometric_operation](#fixed_trigonometric_operation) | 定点数三角函数运算 |
| [get_player_group_num](#get_player_group_num) | 玩家组的玩家数量 |
| [get_related_ability](#get_related_ability) | 获取Actor关联技能 |
| [add_actor_timer](#add_actor_timer) | 为Actor添加定时器 |
| [stop_actor_timer](#stop_actor_timer) | 关闭Actor计时器 |
| [get_fixed_coord_index](#get_fixed_coord_index) | 获取FVector3的其中一个值 |
| [clear_group](#clear_group) | 清空组/数组变量 |
| [remove_list_var_item](#remove_list_var_item) | 数组 - 删除数组条目 |
| [set_list_with_length](#set_list_with_length) | 将第二个列表的值赋值给第一个列表 不改变第一个列表的长度 |
| [judge_role_in_group](#judge_role_in_group) | 判断玩家是否在玩家组 |
| [is_unit_alive](#is_unit_alive) | 判断单位是否活着 |
| [get_empty_unit_key_pool](#get_empty_unit_key_pool) | 获取空的单位编号池 |
| [get_point_in_route](#get_point_in_route) | 获取路径中某点 |
| [get_point_rotate_y](#get_point_rotate_y) | 点绕Y轴旋转(角度制) |
| [str_to_int](#str_to_int) | 字符串转整数 |
| [str_to_bool](#str_to_bool) | 字符串转布尔值 |
| [str_to_fixed](#str_to_fixed) | 字符串转定点数 |
| [delete_sub_str](#delete_sub_str) | 删除子字符串 |
| [extract_str](#extract_str) | 截取子字符串 |
| [length_of_str](#length_of_str) | 获取字符串长度 |
| [str_to_upper_lower](#str_to_upper_lower) | 字符串大小写统一 |
| [pos_in_str](#pos_in_str) | 子字符串位置 |
| [api_int_to_key](#api_int_to_key) | 整数转化为特效类型 |
| [api_key_to_int](#api_key_to_int) | 将投射物类型转化为整数 |
| [unit_command_type_to_str](#unit_command_type_to_str) | 单位命令类型转字符串 |
| [str_to_unit_command_type](#str_to_unit_command_type) | 字符串转单位命令类型 |
| [ability_cast_type_to_str](#ability_cast_type_to_str) | 技能释放类型转字符串 |
| [str_to_ability_cast_type](#str_to_ability_cast_type) | 字符串转技能释放类型 |
| [poly_area_to_str](#poly_area_to_str) | 多边形区域转字符串 |
| [projectile_group_to_str](#projectile_group_to_str) | 投射物组转字符串 |
| [role_relation_to_str](#role_relation_to_str) | 玩家关系转字符串 |
| [str_to_role_relation](#str_to_role_relation) | 字符串转玩家关系 |
| [unit_key_pool_to_str](#unit_key_pool_to_str) | 单位编号池转字符串 |
| [unit_type_to_str](#unit_type_to_str) | 单位分类转字符串 |
| [str_to_unit_type](#str_to_unit_type) | 字符串转单位分类 |
| [timer_to_str](#timer_to_str) | 计时器转字符串 |
| [unit_to_str](#unit_to_str) | 单位转字符串 |
| [unit_group_to_str](#unit_group_to_str) | 单位组转字符串 |
| [item_to_str](#item_to_str) | 物品转字符串 |
| [item_group_to_str](#item_group_to_str) | 物品组转字符串 |
| [mover_entity_to_str](#mover_entity_to_str) | 运动器转字符串 |
| [role_to_str](#role_to_str) | 玩家转字符串 |
| [role_group_to_str](#role_group_to_str) | 玩家组转字符串 |
| [role_status_to_str](#role_status_to_str) | 玩家状态转字符串 |
| [str_to_role_status](#str_to_role_status) | 字符串转玩家状态 |
| [role_type_to_str](#role_type_to_str) | 玩家控制者转字符串 |
| [str_to_role_type](#str_to_role_type) | 字符串转玩家控制者 |
| [ability_to_str](#ability_to_str) | 技能转字符串 |
| [ability_type_to_str](#ability_type_to_str) | 技能槽位类型转字符串 |
| [str_to_ability_type](#str_to_ability_type) | 字符串转技能槽位类型 |
| [rect_area_to_str](#rect_area_to_str) | 矩形区域转字符串 |
| [circle_area_to_str](#circle_area_to_str) | 圆形区域转字符串 |
| [road_to_str](#road_to_str) | 路径转字符串 |
| [dest_to_str](#dest_to_str) | 可破坏物转字符串 |
| [project_to_str](#project_to_str) | 投射物转字符串 |
| [modifier_entity_to_str](#modifier_entity_to_str) | 魔法效果转字符串 |
| [modifier_type_to_str](#modifier_type_to_str) | 魔法效果类别转字符串 |
| [str_to_modifier_type](#str_to_modifier_type) | 字符串转魔法效果类别 |
| [modifier_effect_type_to_str](#modifier_effect_type_to_str) | 魔法效果影响类型转字符串 |
| [str_to_modifier_effect_type](#str_to_modifier_effect_type) | 字符串转魔法效果影响类型 |
| [camp_to_str](#camp_to_str) | 阵营转字符串 |
| [random_pool_to_str](#random_pool_to_str) | 随机池转字符串 |
| [keyboard_key_to_str](#keyboard_key_to_str) | 键盘按键转字符串 |
| [str_to_keyboard_key](#str_to_keyboard_key) | 字符串转键盘按键 |
| [mouse_key_to_str](#mouse_key_to_str) | 鼠标按键转字符串 |
| [str_to_mouse_key](#str_to_mouse_key) | 字符串转鼠标按键 |
| [mouse_wheel_to_str](#mouse_wheel_to_str) | 鼠标滚轮转字符串 |
| [str_to_mouse_wheel](#str_to_mouse_wheel) | 字符串转鼠标滚轮 |
| [trigger_to_str](#trigger_to_str) | 触发器转字符串 |
| [table_to_str](#table_to_str) | 表转字符串 |
| [damage_type_to_str](#damage_type_to_str) | 伤害类型转字符串 |
| [str_to_damage_type](#str_to_damage_type) | 字符串转伤害类型 |
| [unit_attr_type_to_str](#unit_attr_type_to_str) | 单位属性类型转字符串 |
| [str_to_unit_attr_type](#str_to_unit_attr_type) | 字符串转单位属性类型 |
| [str_to_ui_event](#str_to_ui_event) | 字符串转UI事件 |
| [comp_to_str](#comp_to_str) | 控件转字符串 |
| [get_client_language_type](#get_client_language_type) | 获取本地语言环境 |
| [string_slice](#string_slice) | 截取 |
| [bool_not](#bool_not) | 取反 |
| [get_year_of_server_timestamp](#get_year_of_server_timestamp) | 获取返回的服务器时间(年) |
| [get_month_of_server_timestamp](#get_month_of_server_timestamp) | 获取返回的服务器时间(月) |
| [get_day_of_server_timestamp](#get_day_of_server_timestamp) | 获取返回的服务器时间(日) |
| [get_hour_of_server_timestamp](#get_hour_of_server_timestamp) | 获取返回的服务器时间(小时) |
| [iter_random_pool_result](#iter_random_pool_result) | 随机池结果迭代器 |
| [get_random_pool_ret_code](#get_random_pool_ret_code) | 获取服务器随机池执行结果 |
| [get_iter_random_pool_archive_key](#get_iter_random_pool_archive_key) | 获取服务器随机池掉落影响存档槽位 |
| [get_iter_random_pool_archive_increment](#get_iter_random_pool_archive_increment) | 获取服务器随机池掉落影响存档值 |
| [api_do_nothing](#api_do_nothing) | 空api |
| [int_iterator3](#int_iterator3) | 整数迭代器 |
| [int_to_string](#int_to_string) | 整数转换为字符串 |
| [int_to_model_key](#int_to_model_key) | 整数转换为模型类型 |
| [float_to_str_new](#float_to_str_new) | 定点数转字符串 |
| [remove_list_var_item_2](#remove_list_var_item_2) | 数组 - 删除数组条目 |
| [dict_has_key](#dict_has_key) | 数组 - 是否具有索引 |
| [dict_has_value](#dict_has_value) | 数组 - 是否存在元素 |
| [dict_has_value_special](#dict_has_value_special) | 数组 - 是否存在元素 |
| [api_stop_luagc_control](#api_stop_luagc_control) | 停止对lua gc的控制 |
| [map_to_str](#map_to_str) | 关卡转字符串 |
| [get_role_open_archive](#get_role_open_archive) | 获取玩家离线存档 |
| [get_random_number_err_code](#get_random_number_err_code) | 获取生成随机数错误码 |
| [lua_get_python_empty_dict](#lua_get_python_empty_dict) | 还给lua一个空python table |
| [timestamp_to_str](#timestamp_to_str) | 时间戳转化为日期 |
| [str_to_timestamp](#str_to_timestamp) | 字符串转时间戳 |
| [api_get_booked_number](#api_get_booked_number) | 获取当前地图预约人数 |
| [api_timestamp_to_week](#api_timestamp_to_week) | 时间戳转星期 |
| [floor_or_ceil](#floor_or_ceil) | 取整 |

---

## api_clear_tag

method in GlobalAPI

- 描述

    清空标签

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | Actor |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GlobalAPI.api_clear_tag(actor)
```

---

## api_clear_kv

method in GlobalAPI

- 描述

    清空自定义键值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | Actor |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GlobalAPI.api_clear_kv(actor)
```

---

## has_tag

method in GlobalAPI

- 描述

    判断Actor是否有Tag

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | Actor |
    | tag | string | Tag标签 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否有tag |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GlobalAPI.has_tag(actor, "tag")
```

---

## api_has_kv_any

method in GlobalAPI

- 描述

    判断Actor是否有kv

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.Actor | Actor |
    | key | string | kv |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否有tag |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GlobalAPI.api_has_kv_any(actor, "key")
```

---

## is_str_include_other

method in GlobalAPI

- 描述

    字符串A是否包含字符串B

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | str_a | string | str |
    | str_b | string | str |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 是否包含 |

- 示例

```lua
local result = GlobalAPI.is_str_include_other("str_a", "str_b")
```

---

## set_actor_trigger_enabled

method in GlobalAPI

- 描述

    使能Actor身上的触发器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | Actor |
    | trigger_id | py.TriggerID | 触发器id |
    | enabled | boolean | 使能 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GlobalAPI.set_actor_trigger_enabled(actor, 1, true)
```

---

## trigger_actor_trigger

method in GlobalAPI

- 描述

    触发Actor身上的触发器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | actor |
    | trigger_id | py.TriggerID | 触发器id |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GlobalAPI.trigger_actor_trigger(actor, 1)
```

---

## reg_actor_trigger

method in GlobalAPI

- 描述

    注册Actor上的触发器并生效

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | actor |
    | conf_id | py.TriggerID | 触发器配置id |
    | context | py.Dict | 上下文 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.DynamicTriggerInstance | 动态触发器实例 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local dict = pydict()

local result = GlobalAPI.reg_actor_trigger(actor, 1, dict)
```

---

## unreg_actor_trigger

method in GlobalAPI

- 描述

    注销Actor上的触发器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | actor |
    | trigger_id | py.DynamicTriggerInstance | 动态触发器实例 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local trigger_instance = GameAPI.get_last_created_trigger()

GlobalAPI.unreg_actor_trigger(actor, trigger_instance)
```

---

## create_sector_shape

method in GlobalAPI

- 描述

    创建一个扇形

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | radius | py.Fixed | 半径 |
    | angle | py.Fixed | 角度 |
    | yaw | number | 朝向 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Shape | 扇形对象 |

- 示例

```lua
local result = GlobalAPI.create_sector_shape(Fix32(1), Fix32(1), 1.0)
```

---

## create_circular_shape

method in GlobalAPI

- 描述

    创建一个圆形

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | radius | py.Fixed | 半径 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Shape | 圆形对象 |

- 示例

```lua
local result = GlobalAPI.create_circular_shape(Fix32(1))
```

---

## create_rectangle_shape

method in GlobalAPI

- 描述

    创建一个矩形

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | width | py.Fixed | 长 |
    | length | py.Fixed | 宽 |
    | yaw | number | 朝向 |
    | offset_x_ratio? | py.Fixed | 偏移x |
    | offset_y_ratio? | py.Fixed | 偏移y |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Shape | 矩形对象 |

- 示例

```lua
local result = GlobalAPI.create_rectangle_shape(Fix32(1), Fix32(1), 1.0, Fix32(1), Fix32(1))
```

---

## create_annular_shape

method in GlobalAPI

- 描述

    创建一个环形

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | small_r | py.Fixed | 小圆半径 |
    | big_r | py.Fixed | 大圆半径 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Shape | 环形对象 |

- 示例

```lua
local result = GlobalAPI.create_annular_shape(Fix32(1), Fix32(1))
```

---

## coord_to_point

method in GlobalAPI

- 描述

    坐标值转化为FVector3

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | x | py.Fixed | x |
    | z | py.Fixed | y |
    | y? | py.Fixed | z |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3 | FVector3 |

- 示例

```lua
local result = GlobalAPI.coord_to_point(Fix32(1), Fix32(1), Fix32(1))
```

---

## float_to_vector3

method in GlobalAPI

- 描述

    三维坐标值转化为FVector3

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | x | py.Fixed | x |
    | y | py.Fixed | y |
    | z | py.Fixed | z |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3 | FVector3 |

- 示例

```lua
local result = GlobalAPI.float_to_vector3(Fix32(1), Fix32(1), Fix32(1))
```

---

## get_vector3_x

method in GlobalAPI

- 描述

    返回三维向量的X

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | vector | py.FVector3 | 三维向量 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | X |

- 示例

```lua
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

local result = GlobalAPI.get_vector3_x(fvector3)
```

---

## get_vector3_y

method in GlobalAPI

- 描述

    返回三维向量的Y

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | vector | py.FVector3 | 三维向量 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | Y |

- 示例

```lua
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

local result = GlobalAPI.get_vector3_y(fvector3)
```

---

## get_vector3_z

method in GlobalAPI

- 描述

    返回三维向量的Z

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | vector | py.FVector3 | 三维向量 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | Z |

- 示例

```lua
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

local result = GlobalAPI.get_vector3_z(fvector3)
```

---

## float_to_rotation

method in GlobalAPI

- 描述

    三维坐标值转化为FRotation

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | x | py.Fixed | x |
    | y | py.Fixed | y |
    | z | py.Fixed | z |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3 | FVector3 |

- 示例

```lua
local result = GlobalAPI.float_to_rotation(Fix32(1), Fix32(1), Fix32(1))
```

---

## get_rotation_roll

method in GlobalAPI

- 描述

    返回旋转的Roll

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | vector | py.FRotation | Rotation |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | X |

- 示例

```lua
local result = GlobalAPI.get_rotation_roll(GlobalAPI.vector3_to_euler(Fix32Vec3(0, 0, 0)))
```

---

## get_rotation_yaw

method in GlobalAPI

- 描述

    返回旋转的YAW

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | vector | py.FRotation | Rotation |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | Y |

- 示例

```lua
local result = GlobalAPI.get_rotation_yaw(GlobalAPI.vector3_to_euler(Fix32Vec3(0, 0, 0)))
```

---

## get_rotation_pitch

method in GlobalAPI

- 描述

    返回旋转的PITCH

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | vector | py.FRotation | Rotation |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | Z |

- 示例

```lua
local result = GlobalAPI.get_rotation_pitch(GlobalAPI.vector3_to_euler(Fix32Vec3(0, 0, 0)))
```

---

## int_iterator

method in GlobalAPI

- 描述

    整数迭代器，最大迭代次数不超过2^20

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | num | integer | 迭代次数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Int32Iterator | Python迭代器 |

- 示例

```lua
local result = GlobalAPI.int_iterator(1)
```

---

## int_iterator2

method in GlobalAPI

- 描述

    整数迭代器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | start | integer | 计数从start开始 |
    | stop | integer | 计数到stop结束 |
    | step? | integer | 步长 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Int32Iterator | Python迭代器 |

- 示例

```lua
local result = GlobalAPI.int_iterator2(1, 1, 1)
```

---

## list_index_iterator

method in GlobalAPI

- 描述

    列表索引迭代器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Iterator | Python迭代器 |

- 示例

```lua
local list = {}

local result = GlobalAPI.list_index_iterator(list)
```

---

## table_iterator

method in GlobalAPI

- 描述

    table迭代器(废弃)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.Table | TAB |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Iterator | Python迭代器 |

- 示例

```lua
local tbl = {}

local result = GlobalAPI.table_iterator(tbl)
```

---

## get_iter_table_key_str

method in GlobalAPI

- 描述

    get_iter_table_key_str

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item | py.List | table iter item |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | key str |

- 示例

```lua
local list = {}

local result = GlobalAPI.get_iter_table_key_str(list)
```

---

## get_iter_table_key_int

method in GlobalAPI

- 描述

    get_iter_table_key_int

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item | py.List | table iter item |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | key int |

- 示例

```lua
local list = {}

local result = GlobalAPI.get_iter_table_key_int(list)
```

---

## int32_arithmetic_operation

method in GlobalAPI

- 描述

    Int32运算

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | v1 | integer | x |
    | op | string | operator(+,-,*,/,%) |
    | v2 | integer | y |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 返回值 |

- 示例

```lua
local result = GlobalAPI.int32_arithmetic_operation(1, "op", 1)
```

---

## int32_plus_one

method in GlobalAPI

- 描述

    Int32自增1

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | int_value | integer | x |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 返回值 |

- 示例

```lua
local result = GlobalAPI.int32_plus_one(1)
```

---

## int32_min

method in GlobalAPI

- 描述

    Int32取较小值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | int_value1 | integer | x1 |
    | int_value2 | integer | x2 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 返回值 |

- 示例

```lua
local result = GlobalAPI.int32_min(1, 1)
```

---

## int32_max

method in GlobalAPI

- 描述

    Int32取较大值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | int_value1 | integer | x1 |
    | int_value2 | integer | x2 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 返回值 |

- 示例

```lua
local result = GlobalAPI.int32_max(1, 1)
```

---

## get_point_offset_vector

method in GlobalAPI

- 描述

    点向方向偏移

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.FVector3 | 起始点 |
    | angle | py.Fixed | 方向角度 |
    | dis | py.Fixed | 偏移距离 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3 | 返回值 |

- 示例

```lua
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

local result = GlobalAPI.get_point_offset_vector(fvector3, Fix32(1), Fix32(1))
```

---

## int64_to_str

method in GlobalAPI

- 描述

    int64转换字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | val | integer | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local result = GlobalAPI.int64_to_str(1)
```

---

## to_str_default

method in GlobalAPI

- 描述

    to_str_default

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | val | py.Actor | 值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GlobalAPI.to_str_default(actor)
```

---

## api_remove_kv

method in GlobalAPI

- 描述

    删除键值对

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | kvbase | py.KVBase | 键值对容器 |
    | key | string | 键名 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local kvbase = unit.handle

GlobalAPI.api_remove_kv(kvbase, "key")
```

---

## get_unit_key_pool_num

method in GlobalAPI

- 描述

    获取单位编号池内单位编号数量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | pool | py.UnitKeyPool | 单位编号池 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 单位编号数量 |

- 示例

```lua
local unit_key_pool = GlobalAPI.get_empty_unit_key_pool()

local result = GlobalAPI.get_unit_key_pool_num(unit_key_pool)
```

---

## plane_range_between_2_point

method in GlobalAPI

- 描述

    两点之间距离

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | p1 | py.FPoint | 目标点 |
    | p2 | py.FPoint | 起始点 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 距离 |

- 示例

```lua
local fpoint = GameAPI.get_point_by_res_id(1)

local result = GlobalAPI.plane_range_between_2_point(fpoint, fpoint)
```

---

## int32_to_fixed

method in GlobalAPI

- 描述

    整数转定点数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | i | integer | 整数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 定点数 |

- 示例

```lua
local result = GlobalAPI.int32_to_fixed(1)
```

---

## fix32_equal_with_precision

method in GlobalAPI

- 描述

    实数近似比较(4位小数)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | a | py.Fixed | 定点数1 |
    | op | string | 比较符 |
    | b | py.Fixed | 定点数2 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 结果 |

- 示例

```lua
local result = GlobalAPI.fix32_equal_with_precision(Fix32(1), "op", Fix32(1))
```

---

## fixed_to_int32

method in GlobalAPI

- 描述

    定点数转整数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | f | py.Fixed | 定点数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 整数 |

- 示例

```lua
local result = GlobalAPI.fixed_to_int32(Fix32(1))
```

---

## ability_index_to_int32

method in GlobalAPI

- 描述

    技能槽位转整数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_index | py.AbilityIndex | 技能槽位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 整数 |

- 示例

```lua
local ability_index = 0

local result = GlobalAPI.ability_index_to_int32(ability_index)
```

---

## fixed_to_str

method in GlobalAPI

- 描述

    定点数转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | f | py.Fixed | 定点数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local result = GlobalAPI.fixed_to_str(Fix32(1))
```

---

## fvector3_to_str

method in GlobalAPI

- 描述

    定点FVector3转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | f | py.FVector3 | FVector3 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

local result = GlobalAPI.fvector3_to_str(fvector3)
```

---

## fvector2_to_str

method in GlobalAPI

- 描述

    定点FVector2转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | f | py.FVector2 | FVector2 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local result = GlobalAPI.fvector2_to_str("f")
```

---

## float_to_str

method in GlobalAPI

- 描述

    浮点数转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | f | number | 浮点数 |
    | num? | integer | 保留位数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local result = GlobalAPI.float_to_str(1.0, 1)
```

---

## vector3_to_str

method in GlobalAPI

- 描述

    浮点Vector3转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | f | py.Vector3 | Vector3 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local vector3 = Fix32Vec3(0, 0, 0)

local result = GlobalAPI.vector3_to_str(vector3)
```

---

## str_to_vector3

method in GlobalAPI

- 描述

    字符串转Vector3

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | f | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Vector3 | Vector3 |

- 示例

```lua
local result = GlobalAPI.str_to_vector3("f")
```

---

## vector2_to_str

method in GlobalAPI

- 描述

    浮点Vector2转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | f | py.Vector2 | Vector2 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local result = GlobalAPI.vector2_to_str("f")
```

---

## shape_to_str

method in GlobalAPI

- 描述

    Shape转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | f | py.Shape | Shape |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local shape = GlobalAPI.create_circular_shape(Fix32(500))

local result = GlobalAPI.shape_to_str(shape)
```

---

## dynamic_to_str

method in GlobalAPI

- 描述

    动态类型数转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | f | py.DynamicTypeMeta | 动态类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local dynamic_type = GameAPI.get_function_return_value("func_id", y3.player.get_by_id(1):get_all_units()[1].handle, pydict(), {}, 1)

local result = GlobalAPI.dynamic_to_str(dynamic_type)
```

---

## int32_to_str

method in GlobalAPI

- 描述

    int32_to_str

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | f | integer | int32 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local result = GlobalAPI.int32_to_str(1)
```

---

## bool_to_str

method in GlobalAPI

- 描述

    布尔型转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | f | boolean | 布尔值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local result = GlobalAPI.bool_to_str(true)
```

---

## i2s

method in GlobalAPI

- 描述

    整数转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | i | integer | 整数值 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local result = GlobalAPI.i2s(1)
```

---

## join_s

method in GlobalAPI

- 描述

    字符串拼接

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | s1 | string | 字符串 |
    | s2 | string | 字符串 |
    | s3 | string | 字符串 |
    | s4 | string | 字符串 |
    | s5 | string | 字符串 |
    | s6 | string | 字符串 |
    | s7 | string | 字符串 |
    | s8 | string | 字符串 |
    | s9 | string | 字符串 |
    | s10 | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local result = GlobalAPI.join_s("s1", "s2", "s3", "s4", "s5", "s6", "s7", "s8", "s9", "s10")
```

---

## join_s_new

method in GlobalAPI

- 描述

    字符串拼接

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | s1 | string | 字符串 |
    | s2 | string | 字符串 |
    | s3 | string | 字符串 |
    | s4 | string | 字符串 |
    | s5 | string | 字符串 |
    | s6 | string | 字符串 |
    | s7 | string | 字符串 |
    | s8 | string | 字符串 |
    | s9 | string | 字符串 |
    | s10 | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local result = GlobalAPI.join_s_new("s1", "s2", "s3", "s4", "s5", "s6", "s7", "s8", "s9", "s10")
```

---

## root

method in GlobalAPI

- 描述

    开方

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | base | py.Fixed | 开方底 |
    | num | py.Fixed | 开方次数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 计算结果 |

- 示例

```lua
local result = GlobalAPI.root(Fix32(1), Fix32(1))
```

---

## replace_str

method in GlobalAPI

- 描述

    字符串替换

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | s1 | string | 母字符串 |
    | old | string | 被替换的字符串 |
    | new | string | 替换目标字符串 |
    | num? | integer | 最大替换次数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local result = GlobalAPI.replace_str("s1", "old", "new", 1)
```

---

## fixed_arithmetic_operation

method in GlobalAPI

- 描述

    定点数运算

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | a | py.Fixed | x |
    | o | string | operator(+,-*,/) |
    | b | py.Fixed | y |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 定点数 |

- 示例

```lua
local result = GlobalAPI.fixed_arithmetic_operation(Fix32(1), "o", Fix32(1))
```

---

## vector3_arithmetic_operation

method in GlobalAPI

- 描述

    三维向量运算

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | a | py.FVector3 | x |
    | o | string | operator(+,-) |
    | b | py.FVector3 | y |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3 | 定点数Vector3 |

- 示例

```lua
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

local result = GlobalAPI.vector3_arithmetic_operation(fvector3, "o", fvector3)
```

---

## vector3_length

method in GlobalAPI

- 描述

    三维向量的长度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | vec3 | py.FVector3 | x |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 定点数 |

- 示例

```lua
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

local result = GlobalAPI.vector3_length(fvector3)
```

---

## vector3_normalize

method in GlobalAPI

- 描述

    三维向量归一化

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | vec3 | py.Vector3 | 三维向量 |

- 返回值

    无

- 示例

```lua
local vector3 = Fix32Vec3(0, 0, 0)

GlobalAPI.vector3_normalize(vector3)
```

---

## get_vector3_normalize

method in GlobalAPI

- 描述

    三维向量的归一化向量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | vec3 | py.Vector3 | 三维向量 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Vector3 | 三维向量 |

- 示例

```lua
local vector3 = Fix32Vec3(0, 0, 0)

local result = GlobalAPI.get_vector3_normalize(vector3)
```

---

## vector3_multiply_scalar

method in GlobalAPI

- 描述

    三维向量乘以标量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | vec3 | py.Vector3 | 三维向量 |
    | scalar | py.Vector3 | 标量 |

- 返回值

    无

- 示例

```lua
local vector3 = Fix32Vec3(0, 0, 0)

GlobalAPI.vector3_multiply_scalar(vector3, vector3)
```

---

## vector3_to_euler

method in GlobalAPI

- 描述

    三维向量转欧拉角

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | vec3 | py.Vector3 | 三维向量 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FRotation | 欧拉角 |

- 示例

```lua
local vector3 = Fix32Vec3(0, 0, 0)

local result = GlobalAPI.vector3_to_euler(vector3)
```

---

## vector3_angle_axis

method in GlobalAPI

- 描述

    获得三维向量绕轴旋转后的向量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | vec3 | py.FVector3 | 三维向量 |
    | axis | py.FVector3 | 旋转轴 |
    | angle | py.Fixed | 旋转角度 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FVector3 | 定点数Vector3 |

- 示例

```lua
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

local result = GlobalAPI.vector3_angle_axis(fvector3, fvector3, Fix32(1))
```

---

## fixed_plus_one

method in GlobalAPI

- 描述

    定点数自增1

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | fix_value | py.Fixed | x |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 定点数 |

- 示例

```lua
local result = GlobalAPI.fixed_plus_one(Fix32(1))
```

---

## fixed_min

method in GlobalAPI

- 描述

    取两个定点数最小值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | fix_value1 | py.Fixed | x1 |
    | fix_value2 | py.Fixed | x2 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 定点数 |

- 示例

```lua
local result = GlobalAPI.fixed_min(Fix32(1), Fix32(1))
```

---

## fixed_max

method in GlobalAPI

- 描述

    取两个定点数最小大值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | fix_value1 | py.Fixed | x1 |
    | fix_value2 | py.Fixed | x2 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 定点数 |

- 示例

```lua
local result = GlobalAPI.fixed_max(Fix32(1), Fix32(1))
```

---

## angle_arithmetic_operation

method in GlobalAPI

- 描述

    角度计算

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | a | py.Fixed | x |
    | o | string | operator(+,-*,/) |
    | b | py.Fixed | y |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 定点数 |

- 示例

```lua
local result = GlobalAPI.angle_arithmetic_operation(Fix32(1), "o", Fix32(1))
```

---

## degree_to_radian

method in GlobalAPI

- 描述

    转换度到弧度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | d | py.Fixed | 角度 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 弧度 |

- 示例

```lua
local result = GlobalAPI.degree_to_radian(Fix32(1))
```

---

## radian_sin

method in GlobalAPI

- 描述

    正弦

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | r | py.Fixed | 弧度 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 定点数 |

- 示例

```lua
local result = GlobalAPI.radian_sin(Fix32(1))
```

---

## radian_cos

method in GlobalAPI

- 描述

    余弦

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | r | py.Fixed | 弧度 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 定点数 |

- 示例

```lua
local result = GlobalAPI.radian_cos(Fix32(1))
```

---

## radian_tan

method in GlobalAPI

- 描述

    正切

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | r | py.Fixed | 弧度 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 定点数 |

- 示例

```lua
local result = GlobalAPI.radian_tan(Fix32(1))
```

---

## radian_asin

method in GlobalAPI

- 描述

    反正弦

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | r | py.Fixed | 定点数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 弧度 |

- 示例

```lua
local result = GlobalAPI.radian_asin(Fix32(1))
```

---

## radian_acos

method in GlobalAPI

- 描述

    反余弦

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | r | py.Fixed | 定点数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 弧度 |

- 示例

```lua
local result = GlobalAPI.radian_acos(Fix32(1))
```

---

## radian_atan

method in GlobalAPI

- 描述

    反正切

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | r | py.Fixed | 定点数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 弧度 |

- 示例

```lua
local result = GlobalAPI.radian_atan(Fix32(1))
```

---

## radian_atan_x_y

method in GlobalAPI

- 描述

    反正切(Y:X)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | y | py.Fixed | 定点数 |
    | x | py.Fixed | 定点数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 弧度 |

- 示例

```lua
local result = GlobalAPI.radian_atan_x_y(Fix32(1), Fix32(1))
```

---

## sqrt

method in GlobalAPI

- 描述

    平方根

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | x | py.Fixed | 定点数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 定点数 |

- 示例

```lua
local result = GlobalAPI.sqrt(Fix32(1))
```

---

## pow

method in GlobalAPI

- 描述

    求幂

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | f | py.Fixed | 定点数 |
    | n | integer | 整数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 定点数 |

- 示例

```lua
local result = GlobalAPI.pow(Fix32(1), 1)
```

---

## abs

method in GlobalAPI

- 描述

    求绝对值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | f | py.Fixed | 定点数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 定点数 |

- 示例

```lua
local result = GlobalAPI.abs(Fix32(1))
```

---

## int_abs

method in GlobalAPI

- 描述

    求绝对值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | number | integer | 整数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 整数 |

- 示例

```lua
local result = GlobalAPI.int_abs(1)
```

---

## interval

method in GlobalAPI

- 描述

    区间

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | x0 | py.Fixed | 定点数 |
    | x1 | py.Fixed | 定点数 |
    | x2 | py.Fixed | 定点数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 定点数 |

- 示例

```lua
local result = GlobalAPI.interval(Fix32(1), Fix32(1), Fix32(1))
```

---

## nearest_quadratic_number

method in GlobalAPI

- 描述

    找最近的二次方数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | x | py.Fixed | 定点数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 二次方数 |

- 示例

```lua
local result = GlobalAPI.nearest_quadratic_number(Fix32(1))
```

---

## ceil

method in GlobalAPI

- 描述

    最小整数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | f | py.Fixed | 定点数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 整数 |

- 示例

```lua
local result = GlobalAPI.ceil(Fix32(1))
```

---

## floor

method in GlobalAPI

- 描述

    最大整数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | f | py.Fixed | 定点数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 整数 |

- 示例

```lua
local result = GlobalAPI.floor(Fix32(1))
```

---

## interpolate

method in GlobalAPI

- 描述

    插值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | x_from | py.Fixed | 定点数 |
    | x_to | py.Fixed | 定点数 |
    | t | py.Fixed | 定点数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 定点数 |

- 示例

```lua
local result = GlobalAPI.interpolate(Fix32(1), Fix32(1), Fix32(1))
```

---

## invert_interpolate

method in GlobalAPI

- 描述

    反插值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | x_from | py.Fixed | 定点数 |
    | x_to | py.Fixed | 定点数 |
    | res_val | py.Fixed | 定点数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 定点数 |

- 示例

```lua
local result = GlobalAPI.invert_interpolate(Fix32(1), Fix32(1), Fix32(1))
```

---

## log10

method in GlobalAPI

- 描述

    对数10

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | x | py.Fixed | 定点数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 定点数 |

- 示例

```lua
local result = GlobalAPI.log10(Fix32(1))
```

---

## log

method in GlobalAPI

- 描述

    对数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | x1 | py.Fixed | 定点数 |
    | x2 | py.Fixed | 定点数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 定点数 |

- 示例

```lua
local result = GlobalAPI.log(Fix32(1), Fix32(1))
```

---

## get_max_in_list

method in GlobalAPI

- 描述

    返回组内最大值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 定点数 |

- 示例

```lua
local list = {}

local result = GlobalAPI.get_max_in_list(list)
```

---

## get_min_in_list

method in GlobalAPI

- 描述

    返回组内最小值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | l | py.List | 列表 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 定点数 |

- 示例

```lua
local list = {}

local result = GlobalAPI.get_min_in_list(list)
```

---

## round

method in GlobalAPI

- 描述

    四舍五入

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | x | py.Fixed | 定点数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 定点数 |

- 示例

```lua
local result = GlobalAPI.round(Fix32(1))
```

---

## sign

method in GlobalAPI

- 描述

    返回正负符号

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | f | py.Fixed | 定点数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 定点数 |

- 示例

```lua
local result = GlobalAPI.sign(Fix32(1))
```

---

## round_dec

method in GlobalAPI

- 描述

    保留X位小数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | x | py.Fixed | 定点数 |
    | num | integer | X位小数 |
    | b? | boolean | 是否四舍五入 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 定点数 |

- 示例

```lua
local result = GlobalAPI.round_dec(Fix32(1), 1, true)
```

---

## fixed_trigonometric_operation

method in GlobalAPI

- 描述

    定点数三角函数运算

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | o | string | method(sin,cos,tan) |
    | a | py.Fixed | 定点数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 定点数 |

- 示例

```lua
local result = GlobalAPI.fixed_trigonometric_operation("o", Fix32(1))
```

---

## get_player_group_num

method in GlobalAPI

- 描述

    玩家组的玩家数量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player_group | py.RoleGroup | 玩家组 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 玩家数量 |

- 示例

```lua
local player_group = y3.player_group.create()

local result = GlobalAPI.get_player_group_num(player_group.handle)
```

---

## get_related_ability

method in GlobalAPI

- 描述

    获取Actor关联技能

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | Actor |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Ability | 技能 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

local result = GlobalAPI.get_related_ability(actor)
```

---

## add_actor_timer

method in GlobalAPI

- 描述

    为Actor添加定时器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | actor |
    | name | string | 定时器名称 |
    | once | string | 字符串 |
    | interval | py.Fixed | 定点数 |
    | context | py.Dict | 字典 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle
local dict = pydict()

GlobalAPI.add_actor_timer(actor, "name", "once", Fix32(1), dict)
```

---

## stop_actor_timer

method in GlobalAPI

- 描述

    关闭Actor计时器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | actor | py.Actor | actor |
    | name | string | 字符串 |

- 返回值

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local actor = unit.handle

GlobalAPI.stop_actor_timer(actor, "name")
```

---

## get_fixed_coord_index

method in GlobalAPI

- 描述

    获取FVector3的其中一个值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.FVector3 | FVector3 |
    | index | integer | 序号(0-2) |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 定点数 |

- 示例

```lua
local fvector3 = GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0))

local result = GlobalAPI.get_fixed_coord_index(fvector3, 1)
```

---

## clear_group

method in GlobalAPI

- 描述

    清空组/数组变量

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | list1 | py.List | 列表 |

- 返回值

    无

- 示例

```lua
local list = {}

GlobalAPI.clear_group(list)
```

---

## remove_list_var_item

method in GlobalAPI

- 描述

    数组 - 删除数组条目

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | dict_var | py.List | list var |
    | index | integer | index |
    | index_forward? | boolean | 索引前移 |

- 返回值

    无

- 示例

```lua
local list = {}

GlobalAPI.remove_list_var_item(list, 1, true)
```

---

## set_list_with_length

method in GlobalAPI

- 描述

    将第二个列表的值赋值给第一个列表 不改变第一个列表的长度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | list1 | py.List | 列表 |
    | list2 | py.List | 列表 |

- 返回值

    无

- 示例

```lua
local list = {}

GlobalAPI.set_list_with_length(list, list)
```

---

## judge_role_in_group

method in GlobalAPI

- 描述

    判断玩家是否在玩家组

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | role | py.Role | 玩家 |
    | group | py.RoleGroup | 玩家组 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 布尔值 |

- 示例

```lua
local player = y3.player.get_by_id(1)
local player_group = y3.player_group.create()

local result = GlobalAPI.judge_role_in_group(player.handle, player_group.handle)
```

---

## is_unit_alive

method in GlobalAPI

- 描述

    判断单位是否活着

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit? | py.Unit | 单位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 布尔值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = GlobalAPI.is_unit_alive()
```

---

## get_empty_unit_key_pool

method in GlobalAPI

- 描述

    获取空的单位编号池

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitKeyPool | 单位编号池 |

- 示例

```lua
local result = GlobalAPI.get_empty_unit_key_pool()
```

---

## get_point_in_route

method in GlobalAPI

- 描述

    获取路径中某点

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | road_point_list | py.Road | 路径 |
    | index | integer | 下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FPoint | 点 |

- 示例

```lua
local road = y3.road.get_road_by_res_id(1)

local result = GlobalAPI.get_point_in_route(road.handle, 1)
```

---

## get_point_rotate_y

method in GlobalAPI

- 描述

    点绕Y轴旋转(角度制)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | point | py.FPoint | 点 |
    | angle | py.Fixed | 旋转 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.FPoint | 点 |

- 示例

```lua
local fpoint = GameAPI.get_point_by_res_id(1)

local result = GlobalAPI.get_point_rotate_y(fpoint, Fix32(1))
```

---

## str_to_int

method in GlobalAPI

- 描述

    字符串转整数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | s | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 返回值 |

- 示例

```lua
local result = GlobalAPI.str_to_int("s")
```

---

## str_to_bool

method in GlobalAPI

- 描述

    字符串转布尔值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | s | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 布尔值 |

- 示例

```lua
local result = GlobalAPI.str_to_bool("s")
```

---

## str_to_fixed

method in GlobalAPI

- 描述

    字符串转定点数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | s | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Fixed | 返回值 |

- 示例

```lua
local result = GlobalAPI.str_to_fixed("s")
```

---

## delete_sub_str

method in GlobalAPI

- 描述

    删除子字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | str1 | string | 原字符串 |
    | sub_str | string | 子字符串 |
    | only_one | boolean | 仅一次 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 原字符串 |

- 示例

```lua
local result = GlobalAPI.delete_sub_str("str1", "sub_str", true)
```

---

## extract_str

method in GlobalAPI

- 描述

    截取子字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | str1 | string | 原字符串 |
    | index1 | integer | 左下标 |
    | index2 | integer | 右下标 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 截取后字符串 |

- 示例

```lua
local result = GlobalAPI.extract_str("str1", 1, 1)
```

---

## length_of_str

method in GlobalAPI

- 描述

    获取字符串长度

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | str1 | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 字符串长度 |

- 示例

```lua
local result = GlobalAPI.length_of_str("str1")
```

---

## str_to_upper_lower

method in GlobalAPI

- 描述

    字符串大小写统一

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | str1 | string | 原字符串 |
    | is_upper | boolean | 是否大写 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 处理后字符串 |

- 示例

```lua
local result = GlobalAPI.str_to_upper_lower("str1", true)
```

---

## pos_in_str

method in GlobalAPI

- 描述

    子字符串位置

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | str1 | string | 原字符串 |
    | sub_str | string | 子字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 子字符串位置 |

- 示例

```lua
local result = GlobalAPI.pos_in_str("str1", "sub_str")
```

---

## api_int_to_key

method in GlobalAPI

- 描述

    整数转化为特效类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | integer | integer | 整数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ProjectileKey | 投射物类型 |

- 示例

```lua
local result = GlobalAPI.api_int_to_key(1)
```

---

## api_key_to_int

method in GlobalAPI

- 描述

    将投射物类型转化为整数

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | py.ProjectileKey | 投射物类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 整数 |

- 示例

```lua
local projectile_key = 134274569

local result = GlobalAPI.api_key_to_int(projectile_key)
```

---

## unit_command_type_to_str

method in GlobalAPI

- 描述

    单位命令类型转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | val | py.UnitCommandType | 单位命令类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local result = GlobalAPI.unit_command_type_to_str(1)
```

---

## str_to_unit_command_type

method in GlobalAPI

- 描述

    字符串转单位命令类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | val | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitCommandType | 单位命令类型 |

- 示例

```lua
local result = GlobalAPI.str_to_unit_command_type("val")
```

---

## ability_cast_type_to_str

method in GlobalAPI

- 描述

    技能释放类型转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | val | py.AbilityCastType | 技能释放类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local result = GlobalAPI.ability_cast_type_to_str(1)
```

---

## str_to_ability_cast_type

method in GlobalAPI

- 描述

    字符串转技能释放类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | val | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityCastType | 技能释放类型 |

- 示例

```lua
local result = GlobalAPI.str_to_ability_cast_type("val")
```

---

## poly_area_to_str

method in GlobalAPI

- 描述

    多边形区域转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | py.PolyArea | 多边形区域 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local poly_area = GameAPI.create_polygon_area(Fix32Vec3(0, 0, 0), Fix32Vec3(100, 0, 0), Fix32Vec3(100, 100, 0))

local result = GlobalAPI.poly_area_to_str(poly_area)
```

---

## projectile_group_to_str

method in GlobalAPI

- 描述

    投射物组转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | py.ProjectileGroup | 投射物组 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local projectile_group = y3.projectile_group.create_lua_projectile_group_from_py(GameAPI.create_projectile_group())

local result = GlobalAPI.projectile_group_to_str(projectile_group.handle)
```

---

## role_relation_to_str

method in GlobalAPI

- 描述

    玩家关系转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | val | py.RoleRelation | 玩家关系 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local relation = 1

local result = GlobalAPI.role_relation_to_str(relation)
```

---

## str_to_role_relation

method in GlobalAPI

- 描述

    字符串转玩家关系

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | val | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleRelation | 玩家关系 |

- 示例

```lua
local result = GlobalAPI.str_to_role_relation("val")
```

---

## unit_key_pool_to_str

method in GlobalAPI

- 描述

    单位编号池转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | py.UnitKeyPool | 单位编号池 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local unit_key_pool = GlobalAPI.get_empty_unit_key_pool()

local result = GlobalAPI.unit_key_pool_to_str(unit_key_pool)
```

---

## unit_type_to_str

method in GlobalAPI

- 描述

    单位分类转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | val | py.UnitType | 单位类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local result = GlobalAPI.unit_type_to_str(1)
```

---

## str_to_unit_type

method in GlobalAPI

- 描述

    字符串转单位分类

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | val | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.UnitType | 单位类型 |

- 示例

```lua
local result = GlobalAPI.str_to_unit_type("val")
```

---

## timer_to_str

method in GlobalAPI

- 描述

    计时器转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | val | py.Timer | 计时器 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local timer = y3.timer.loop(1, function() end)

local result = GlobalAPI.timer_to_str(timer.handle)
```

---

## unit_to_str

method in GlobalAPI

- 描述

    单位转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | py.Unit | 单位 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

local result = GlobalAPI.unit_to_str(unit.handle)
```

---

## unit_group_to_str

method in GlobalAPI

- 描述

    单位组转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | py.UnitGroup | 单位组 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local unit_group = y3.unit_group.create()

local result = GlobalAPI.unit_group_to_str(unit_group.handle)
```

---

## item_to_str

method in GlobalAPI

- 描述

    物品转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | py.Item | 物品对象 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

local result = GlobalAPI.item_to_str(item.handle)
```

---

## item_group_to_str

method in GlobalAPI

- 描述

    物品组转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | py.ItemGroup | 物品组 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local item_group = y3.item_group.create()

local result = GlobalAPI.item_group_to_str(item_group.handle)
```

---

## mover_entity_to_str

method in GlobalAPI

- 描述

    运动器转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj_id | py.Mover | 运动器 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local projectile = y3.projectile.create({ key = 134274569, target = y3.point(0, 0) })
local mover = GameAPI.get_projectile_mover(projectile.handle)

local result = GlobalAPI.mover_entity_to_str(mover)
```

---

## role_to_str

method in GlobalAPI

- 描述

    玩家转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | py.Role | 玩家 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local player = y3.player.get_by_id(1)

local result = GlobalAPI.role_to_str(player.handle)
```

---

## role_group_to_str

method in GlobalAPI

- 描述

    玩家组转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | py.RoleGroup | 玩家组 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local player_group = y3.player_group.create()

local result = GlobalAPI.role_group_to_str(player_group.handle)
```

---

## role_status_to_str

method in GlobalAPI

- 描述

    玩家状态转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | val | py.RoleStatus | 玩家状态 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local result = GlobalAPI.role_status_to_str(1)
```

---

## str_to_role_status

method in GlobalAPI

- 描述

    字符串转玩家状态

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | val | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleStatus | 玩家状态 |

- 示例

```lua
local result = GlobalAPI.str_to_role_status("val")
```

---

## role_type_to_str

method in GlobalAPI

- 描述

    玩家控制者转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | val | py.RoleType | 玩家控制者类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local result = GlobalAPI.role_type_to_str(1)
```

---

## str_to_role_type

method in GlobalAPI

- 描述

    字符串转玩家控制者

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | val | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.RoleType | 玩家控制者类型 |

- 示例

```lua
local result = GlobalAPI.str_to_role_type("val")
```

---

## ability_to_str

method in GlobalAPI

- 描述

    技能转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | py.Ability | 技能对象 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

local result = GlobalAPI.ability_to_str(ability.handle)
```

---

## ability_type_to_str

method in GlobalAPI

- 描述

    技能槽位类型转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | val | py.AbilityType | 技能类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local ability_type = y3.const.AbilityType.HERO

local result = GlobalAPI.ability_type_to_str(ability_type)
```

---

## str_to_ability_type

method in GlobalAPI

- 描述

    字符串转技能槽位类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | val | string | 技能类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.AbilityType | 技能类型 |

- 示例

```lua
local result = GlobalAPI.str_to_ability_type("val")
```

---

## rect_area_to_str

method in GlobalAPI

- 描述

    矩形区域转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | py.RecArea | 矩形区域 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local rec_area = GameAPI.create_rec_area_from_two_points(Fix32Vec3(0, 0, 0), Fix32Vec3(100, 100, 0))

local result = GlobalAPI.rect_area_to_str(rec_area)
```

---

## circle_area_to_str

method in GlobalAPI

- 描述

    圆形区域转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | py.CirArea | 圆形区域 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local cir_area = GameAPI.create_new_cir_area(GlobalAPI.float_to_vector3(Fix32(0), Fix32(0), Fix32(0)), Fix32(100))

local result = GlobalAPI.circle_area_to_str(cir_area)
```

---

## road_to_str

method in GlobalAPI

- 描述

    路径转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | py.Road | 路径 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local road = y3.road.get_road_by_res_id(1)

local result = GlobalAPI.road_to_str(road.handle)
```

---

## dest_to_str

method in GlobalAPI

- 描述

    可破坏物转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | py.Destructible | 可破坏物对象 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)
if destructible then

local result = GlobalAPI.dest_to_str(destructible.handle)
end
```

---

## project_to_str

method in GlobalAPI

- 描述

    投射物转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | py.ProjectileEntity | 投掷物对象 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local target_point = unit:get_point()
local projectile = y3.projectile.create({ key = 134274569, target = target_point })

local result = GlobalAPI.project_to_str(projectile.handle)
```

---

## modifier_entity_to_str

method in GlobalAPI

- 描述

    魔法效果转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | py.ModifierEntity | 魔法效果对象 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local modifier = unit:find_modifier(134274569)

local result = GlobalAPI.modifier_entity_to_str(modifier.handle)
```

---

## modifier_type_to_str

method in GlobalAPI

- 描述

    魔法效果类别转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | val | py.ModifierType | 魔法效果类别 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local result = GlobalAPI.modifier_type_to_str(1)
```

---

## str_to_modifier_type

method in GlobalAPI

- 描述

    字符串转魔法效果类别

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | val | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierType | 魔法效果类别 |

- 示例

```lua
local result = GlobalAPI.str_to_modifier_type("val")
```

---

## modifier_effect_type_to_str

method in GlobalAPI

- 描述

    魔法效果影响类型转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | val | py.ModifierEffectType | 魔法效果影响类别 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local result = GlobalAPI.modifier_effect_type_to_str(1)
```

---

## str_to_modifier_effect_type

method in GlobalAPI

- 描述

    字符串转魔法效果影响类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | val | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModifierEffectType | 魔法效果影响类别 |

- 示例

```lua
local result = GlobalAPI.str_to_modifier_effect_type("val")
```

---

## camp_to_str

method in GlobalAPI

- 描述

    阵营转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | py.Camp | 阵营对象 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local camp = GameAPI.get_camp_by_camp_id(1)

local result = GlobalAPI.camp_to_str(camp)
```

---

## random_pool_to_str

method in GlobalAPI

- 描述

    随机池转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | py.RandomPool | 随机池 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local random_pool = GameAPI.create_random_pool()

local result = GlobalAPI.random_pool_to_str(random_pool)
```

---

## keyboard_key_to_str

method in GlobalAPI

- 描述

    键盘按键转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | py.KeyboardKey | 键盘按键 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local result = GlobalAPI.keyboard_key_to_str(1)
```

---

## str_to_keyboard_key

method in GlobalAPI

- 描述

    字符串转键盘按键

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.KeyboardKey | 键盘按键 |

- 示例

```lua
local result = GlobalAPI.str_to_keyboard_key("obj")
```

---

## mouse_key_to_str

method in GlobalAPI

- 描述

    鼠标按键转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | py.MouseKey | 鼠标按键 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local result = GlobalAPI.mouse_key_to_str(1)
```

---

## str_to_mouse_key

method in GlobalAPI

- 描述

    字符串转鼠标按键

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MouseKey | 鼠标按键 |

- 示例

```lua
local result = GlobalAPI.str_to_mouse_key("obj")
```

---

## mouse_wheel_to_str

method in GlobalAPI

- 描述

    鼠标滚轮转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | py.MouseWheel | 鼠标滚轮 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local result = GlobalAPI.mouse_wheel_to_str(1)
```

---

## str_to_mouse_wheel

method in GlobalAPI

- 描述

    字符串转鼠标滚轮

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.MouseWheel | 鼠标滚轮 |

- 示例

```lua
local result = GlobalAPI.str_to_mouse_wheel("obj")
```

---

## trigger_to_str

method in GlobalAPI

- 描述

    触发器转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | py.DynamicTypeMeta | 触发器 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local dynamic_type = GameAPI.get_function_return_value("func_id", y3.player.get_by_id(1):get_all_units()[1].handle, pydict(), {}, 1)

local result = GlobalAPI.trigger_to_str(dynamic_type)
```

---

## table_to_str

method in GlobalAPI

- 描述

    表转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | py.Table | 表 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local tbl = {}

local result = GlobalAPI.table_to_str(tbl)
```

---

## damage_type_to_str

method in GlobalAPI

- 描述

    伤害类型转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | integer | 伤害类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local result = GlobalAPI.damage_type_to_str(1)
```

---

## str_to_damage_type

method in GlobalAPI

- 描述

    字符串转伤害类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 伤害类型 |

- 示例

```lua
local result = GlobalAPI.str_to_damage_type("obj")
```

---

## unit_attr_type_to_str

method in GlobalAPI

- 描述

    单位属性类型转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | string | 属性类型 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local result = GlobalAPI.unit_attr_type_to_str("obj")
```

---

## str_to_unit_attr_type

method in GlobalAPI

- 描述

    字符串转单位属性类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 属性类型 |

- 示例

```lua
local result = GlobalAPI.str_to_unit_attr_type("obj")
```

---

## str_to_ui_event

method in GlobalAPI

- 描述

    字符串转UI事件

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | string | 字符串 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | UI事件 |

- 示例

```lua
local result = GlobalAPI.str_to_ui_event("obj")
```

---

## comp_to_str

method in GlobalAPI

- 描述

    控件转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | string | 控件 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local result = GlobalAPI.comp_to_str("obj")
```

---

## get_client_language_type

method in GlobalAPI

- 描述

    获取本地语言环境

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.LanguageType | 语言环境 |

- 示例

```lua
local result = GlobalAPI.get_client_language_type()
```

---

## string_slice

method in GlobalAPI

- 描述

    截取

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | string | 字符串 |
    | start | integer | start |
    | end_ | integer | end |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | str |

- 示例

```lua
local result = GlobalAPI.string_slice("obj", 1, 1)
```

---

## bool_not

method in GlobalAPI

- 描述

    取反

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | v | boolean | bool |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | bool |

- 示例

```lua
local result = GlobalAPI.bool_not(true)
```

---

## get_year_of_server_timestamp

method in GlobalAPI

- 描述

    获取返回的服务器时间(年)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | v | number | float |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | int |

- 示例

```lua
local result = GlobalAPI.get_year_of_server_timestamp(1.0)
```

---

## get_month_of_server_timestamp

method in GlobalAPI

- 描述

    获取返回的服务器时间(月)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | v | number | float |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | int |

- 示例

```lua
local result = GlobalAPI.get_month_of_server_timestamp(1.0)
```

---

## get_day_of_server_timestamp

method in GlobalAPI

- 描述

    获取返回的服务器时间(日)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | v | number | float |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | int |

- 示例

```lua
local result = GlobalAPI.get_day_of_server_timestamp(1.0)
```

---

## get_hour_of_server_timestamp

method in GlobalAPI

- 描述

    获取返回的服务器时间(小时)

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | v | number | float |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | int |

- 示例

```lua
local result = GlobalAPI.get_hour_of_server_timestamp(1.0)
```

---

## iter_random_pool_result

method in GlobalAPI

- 描述

    随机池结果迭代器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | v | py.Dict | Result |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Iterator | Python迭代器 |

- 示例

```lua
local dict = pydict()

local result = GlobalAPI.iter_random_pool_result(dict)
```

---

## get_random_pool_ret_code

method in GlobalAPI

- 描述

    获取服务器随机池执行结果

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | v | integer | int |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | int |

- 示例

```lua
local result = GlobalAPI.get_random_pool_ret_code(1)
```

---

## get_iter_random_pool_archive_key

method in GlobalAPI

- 描述

    获取服务器随机池掉落影响存档槽位

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | v | integer | int |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | int |

- 示例

```lua
local result = GlobalAPI.get_iter_random_pool_archive_key(1)
```

---

## get_iter_random_pool_archive_increment

method in GlobalAPI

- 描述

    获取服务器随机池掉落影响存档值

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | v | integer | int |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | int |

- 示例

```lua
local result = GlobalAPI.get_iter_random_pool_archive_increment(1)
```

---

## api_do_nothing

method in GlobalAPI

- 描述

    空api

- 参数

    无

- 返回值

    无

- 示例

```lua
GlobalAPI.api_do_nothing()
```

---

## int_iterator3

method in GlobalAPI

- 描述

    整数迭代器

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | start | integer | 计数从start开始 |
    | stop | integer | 计数到stop结束 |
    | step? | integer | 步长 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Int32Iterator | Python迭代器 |

- 示例

```lua
local result = GlobalAPI.int_iterator3(1, 1, 1)
```

---

## int_to_string

method in GlobalAPI

- 描述

    整数转换为字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | i | integer | 整数 |
    | num? | integer | 保留位数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local result = GlobalAPI.int_to_string(1, 1)
```

---

## int_to_model_key

method in GlobalAPI

- 描述

    整数转换为模型类型

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | integer | 整数 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.ModelKey | 字符串 |

- 示例

```lua
local result = GlobalAPI.int_to_model_key(1)
```

---

## float_to_str_new

method in GlobalAPI

- 描述

    定点数转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | f | number | 浮点数 |
    | num | integer | 保留位数 |
    | rule? | integer | 保留规则 |

- 返回值

    无

- 示例

```lua
GlobalAPI.float_to_str_new(1.0, 1, 1)
```

---

## remove_list_var_item_2

method in GlobalAPI

- 描述

    数组 - 删除数组条目

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | dict_var | py.List | list var |
    | index | integer | index |
    | index_forward? | boolean | 索引前移 |

- 返回值

    无

- 示例

```lua
local list = {}

GlobalAPI.remove_list_var_item_2(list, 1, true)
```

---

## dict_has_key

method in GlobalAPI

- 描述

    数组 - 是否具有索引

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | dict_var | py.List | list var |
    | key | integer | key |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 结果 |

- 示例

```lua
local list = {}

local result = GlobalAPI.dict_has_key(list, 1)
```

---

## dict_has_value

method in GlobalAPI

- 描述

    数组 - 是否存在元素

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | dict_var | py.List | list var |
    | key | py.DynamicTypeMeta | value |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 结果 |

- 示例

```lua
local list = {}
local dynamic_type = GameAPI.get_function_return_value("func_id", y3.player.get_by_id(1):get_all_units()[1].handle, pydict(), {}, 1)

local result = GlobalAPI.dict_has_value(list, dynamic_type)
```

---

## dict_has_value_special

method in GlobalAPI

- 描述

    数组 - 是否存在元素

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | dict_var | py.List | list var |
    | key | py.DynamicTypeMeta | value |
    | name | string | name |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | boolean | 结果 |

- 示例

```lua
local list = {}
local dynamic_type = GameAPI.get_function_return_value("func_id", y3.player.get_by_id(1):get_all_units()[1].handle, pydict(), {}, 1)

local result = GlobalAPI.dict_has_value_special(list, dynamic_type, "name")
```

---

## api_stop_luagc_control

method in GlobalAPI

- 描述

    停止对lua gc的控制

- 参数

    无

- 返回值

    无

- 示例

```lua
GlobalAPI.api_stop_luagc_control()
```

---

## map_to_str

method in GlobalAPI

- 描述

    关卡转字符串

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | obj | py.Map | 关卡 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | 字符串 |

- 示例

```lua
local result = GlobalAPI.map_to_str(1)
```

---

## get_role_open_archive

method in GlobalAPI

- 描述

    获取玩家离线存档

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | v | string | str |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | str |

- 示例

```lua
local result = GlobalAPI.get_role_open_archive("v")
```

---

## get_random_number_err_code

method in GlobalAPI

- 描述

    获取生成随机数错误码

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | v | integer | int |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | int |

- 示例

```lua
local result = GlobalAPI.get_random_number_err_code(1)
```

---

## lua_get_python_empty_dict

method in GlobalAPI

- 描述

    还给lua一个空python table

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | py.Dict | Dict |

- 示例

```lua
local result = GlobalAPI.lua_get_python_empty_dict()
```

---

## timestamp_to_str

method in GlobalAPI

- 描述

    时间戳转化为日期

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | v | integer | int |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | string | str |

- 示例

```lua
local result = GlobalAPI.timestamp_to_str(1)
```

---

## str_to_timestamp

method in GlobalAPI

- 描述

    字符串转时间戳

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | v | string | str |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | int |

- 示例

```lua
local result = GlobalAPI.str_to_timestamp("v")
```

---

## api_get_booked_number

method in GlobalAPI

- 描述

    获取当前地图预约人数

- 参数

    无

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 预约人数 |

- 示例

```lua
local result = GlobalAPI.api_get_booked_number()
```

---

## api_timestamp_to_week

method in GlobalAPI

- 描述

    时间戳转星期

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | v | integer | 时间戳 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 星期 |

- 示例

```lua
local result = GlobalAPI.api_timestamp_to_week(1)
```

---

## floor_or_ceil

method in GlobalAPI

- 描述

    取整

- 参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | v | number | 实数 |
    | mode | integer | 取整方式 |

- 返回值

    | 数据类型 | 说明 |
    | :--- | :--- |
    | integer | 取整之后的值 |

- 示例

```lua
local result = GlobalAPI.floor_or_ceil(1.0, 1)
```

---
