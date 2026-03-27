---
sidebarDepth: 1
---
# 类型定义 (PyType)

Y3 编辑器类型定义，包含所有游戏对象的类型声明。

---

| 类型 | 继承自 | 描述 |
| --- | --- | --- |
| `py.ETypeMeta` |  |  |
| `py.DynamicTypeMeta` | py.ETypeMeta |  |
| `py.IntBase` | py.ETypeMeta | 整型 |
| `py.Fixed` | py.ETypeMeta | 定点数 |
| `py.FVector2` | py.ETypeMeta | 定点数Vector2 |
| `py.FVector3` | py.ETypeMeta | 定点数Vector3 |
| `py.FPoint` | py.FVector3 | 点 |
| `py.FUIPoint` | py.FVector2 | UI点 |
| `py.FRotation` | py.FVector3 | Rotation |
| `py.Vector2` | py.ETypeMeta | 浮点数Vector2 |
| `py.Vector3` | py.ETypeMeta | Vector3 |
| `py.Point` | py.Vector3 | 点 |
| `py.RoleID` | integer | 玩家ID |
| `py.RoleRelation` | integer | 玩家关系 |
| `py.CampID` | integer | 阵营ID |
| `py.UnitID` | integer | 单位ID |
| `py.LocalUnitID` | integer | 本地单位ID |
| `py.DecoID` | integer | 装饰物ID |
| `py.HighLightUnitID` | integer | 主控单位ID |
| `py.ProjectileID` | integer | 投射物ID |
| `py.AbilitySeq` | integer | 技能序号 |
| `py.UnitKey` | integer | 单位编号 |
| `py.UnitType` | integer | 单位类型 |
| `py.AbilityKey` | integer | 技能编号 |
| `py.WeatherType` | integer | 天气类型 |
| `py.ModifierKey` | integer | 效果编号 |
| `py.SortType` | integer |  |
| `py.ProjectileKey` | integer | 投射物编号 |
| `py.AbilityIndex` | integer | 技能槽位 |
| `py.AbilityReleaseId` | integer | 单次技能释放索引编号 |
| `py.AbilityType` | integer | 技能类型 |
| `py.AbilityCastType` | integer | 技能释放类型 |
| `py.AbilityStrAttr` | integer | 技能字符串类型属性 |
| `py.SfxVisibleType` | integer | 可见性规则 |
| `py.LinkSfxPointType` | integer | 起点或终点 |
| `py.MovementObstacleProcessType` | integer | 碰撞处理 |
| `py.AttackTargetHitType` | integer | 攻击目标类别 |
| `py.ItemID` | integer | 物品ID |
| `py.ItemStackType` | integer | 物品堆叠类型 |
| `py.ItemKey` | integer | 物品编号 |
| `py.Dict` | py.DynamicTypeMeta | 字典 |
| `py.RandomPool` | py.DynamicTypeMeta |  |
| `py.SceneNode` | py.DynamicTypeMeta |  |
| `py.TechKey` | integer | 科技编号 |
| `py.UIAnimKey` | py.DynamicTypeMeta | UI动画ID |
| `py.RoleStatus` | integer |  |
| `py.RoleType` | integer |  |
| `py.AudioKey` | integer | 音效编号 |
| `py.SfxKey` | integer | 特效编号 |
| `py.LinkSfxKey` | integer | 链接特效编号 |
| `py.ModelKey` | integer | 模型编号 |
| `py.Live2dKey` | integer | live2d模型编号 |
| `py.TriggerID` | integer | 触发器ID |
| `py.DynamicTriggerInstance` | py.DynamicTypeMeta | 动态触发器实例 |
| `py.AreaID` | integer | 区域ID |
| `py.SceneSoundID` | integer | 场景声音ID |
| `py.CamlineID` | integer | 镜头timelineID |
| `py.SlotType` | integer | 背包槽位类型 |
| `py.RoleResKey` | string |  |
| `py.GoodsKey` | integer | 平台商品编号 |
| `py.StoreKey` | integer | 平台道具编号 |
| `py.StoreItemType` | integer | 平台道具类型 |
| `py.TabName` | string |  |
| `py.TabIdx` | integer | 商店页签ID |
| `py.Texture` | integer | 图片 |
| `py.Sequence` | integer | 序列帧 |
| `py.Spine` | integer | Spine |
| `py.MiniMapColorType` | integer | 小地图颜色显示模式 |
| `py.UnitBehavior` | string | 单位行为 |
| `py.ERescueSeekerType` | integer | 求救类型 |
| `py.ERescuerType` | integer | 救援类型 |
| `py.Shape` | py.ETypeMeta | 形状 |
| `py.List` | py.DynamicTypeMeta |  |
| `py.ExprList` | py.List |  |
| `py.UIntList` | py.List |  |
| `py.IntList` | py.List |  |
| `py.Iterator` | py.DynamicTypeMeta | 迭代器 |
| `py.Int32Iterator` | py.Iterator |  |
| `py.KVBase` | py.DynamicTypeMeta | KVBase |
| `py.Actor` | py.KVBase |  |
| `py.WorldUINode` | py.KVBase | Widget |
| `py.UIPreset` | integer | UIPreset |
| `py.ActorContainer` | py.DynamicTypeMeta | Actor容器 |
| `py.Unit` | py.Actor | 单位 |
| `py.LocalUnit` | py.DynamicTypeMeta | 本地单位 |
| `py.UnitGroup` | py.UIntList | 单位组 |
| `py.LocalUnitGroup` | py.UIntList | 本地单位组 |
| `py.UnitKeyPool` | py.DynamicTypeMeta | 单位编号池 |
| `py.Camera` | py.DynamicTypeMeta | 镜头配置 |
| `py.RoleGroup` | py.UIntList | 玩家组 |
| `py.Item` | py.DynamicTypeMeta | 物品对象 |
| `py.ScenePreset` | integer | 地形预设 |
| `py.SoundEntity` | py.DynamicTypeMeta | 声音对象 |
| `py.ItemGroup` | py.UIntList | 物品组 |
| `py.Destructible` | py.DynamicTypeMeta | 可破坏物对象 |
| `py.DestructibleID` | integer | 可破坏物ID |
| `py.DestructibleKey` | integer | 可破坏物编号 |
| `py.DecoKey` | integer | 装饰物编号 |
| `py.GameAPI` | py.DynamicTypeMeta | GameAPI对象 |
| `py.Role` | py.DynamicTypeMeta | 玩家 |
| `py.Camp` | py.DynamicTypeMeta | 阵营对象 |
| `py.Area` | py.DynamicTypeMeta | 区域 |
| `py.RecArea` | py.Area | 矩形区域 |
| `py.CirArea` | py.Area | 圆形区域 |
| `py.PolyArea` | py.Area | 多边形区域 |
| `py.RoadGroup` | py.List |  |
| `py.LightID` | integer | 光源ID |
| `py.Light` | py.DynamicTypeMeta | 光源 |
| `py.PointLight` | py.Light | 点光源 |
| `py.SpotLight` | py.Light | 方向光源 |
| `py.Fog` | py.DynamicTypeMeta | 局部雾 |
| `py.SceneSound` | py.DynamicTypeMeta | 场景声音 |
| `py.FogID` | integer | 雾ID |
| `py.CcActionID` | integer | 主控角色预定义行为ID |
| `py.CcAsmState` | integer | 主控角色动画状态机状态 |
| `py.CcHandID` | integer | 主控角色 |
| `py.CcAnimationMachineStatus` | string | 动画机状态 |
| `py.CcEmo` | integer | 角色表情 |
| `py.Ability` | py.Actor | 技能对象 |
| `py.ModifierEntity` | py.Actor | 效果对象 |
| `py.ModifierEffectType` | integer | 效果类型 |
| `py.ModifierType` | integer | 魔法效果类别 |
| `py.ModifierStyle` | integer | 效果类别 |
| `py.ProjectileEntity` | py.Actor | 投掷物对象 |
| `py.ProjectileGroup` | py.UIntList | 投射物组 |
| `py.ActorList` | py.List |  |
| `py.UnitList` | py.ActorList |  |
| `py.UnitModel` | py.DynamicTypeMeta | 单位展示模型 |
| `py.Grid` | py.DynamicTypeMeta | 格子阵列 |
| `py.BinUnitPanel` | string | 绑定单位界面 |
| `py.AttachModelEntity` | py.Actor | 挂接模型实体 |
| `py.AttachModelEntityGroup` | py.ActorList | 挂接模型实体组 |
| `py.ModelEntity` | integer |  |
| `py.RoleRes` | string |  |
| `py.CameraPreset` | py.DynamicTypeMeta | 镜头预设 |
| `py.Road` | py.List | 路径 |
| `py.Model` | integer |  |
| `py.Live2d` | integer |  |
| `py.Sfx` | py.DynamicTypeMeta | 特效 |
| `py.LinkSfx` | py.DynamicTypeMeta | 链接特效 |
| `py.UnitCommand` | py.DynamicTypeMeta | 单位命令 |
| `py.UnitCommandType` | integer |  |
| `py.UnitGroupCommand` | py.DynamicTypeMeta | 单位组命令 |
| `py.UnitGroupCommandType` | integer |  |
| `py.Color` | string | 颜色 |
| `py.Timer` | integer | 计时器 |
| `py.Formula` | integer | 公式 |
| `py.KeyboardKey` | integer | 键盘按键 |
| `py.FuncKeyboardKey` | integer | 键盘辅助按键 |
| `py.MouseKey` | integer | 鼠标按键 |
| `py.MouseWheel` | integer | 鼠标滚轮 |
| `py.MouseKeyWithoutMiddle` | integer | 鼠标按键（仅包含左右键） |
| `py.GameMode` | integer |  |
| `py.MapId` | string |  |
| `py.StartMode` | integer |  |
| `py.UppassEnv` | string |  |
| `py.EditableGameFunc` | integer |  |
| `py.AllGameFunc` | integer |  |
| `py.NormalKey` | string |  |
| `py.RecordKey` | string |  |
| `py.CameraRotate` | integer |  |
| `py.LanguageType` | string |  |
| `py.HitPointKey` | integer |  |
| `py.CurvedPath` | py.List | 曲线运动器路径 |
| `py.CurvedPath3D` | py.List | 3D曲线运动器路径 |
| `py.Table` | py.DynamicTypeMeta | 表 |
| `py.PostEffect` | integer | 画风 |
| `py.UIPrefabIns` | py.DynamicTypeMeta |  |
| `py.SkillPointerType` | integer | 技能指示器类型 |
| `py.MoverType` | integer | 运动器类型 |
| `py.Mover` | py.DynamicTypeMeta | 运动器类型 |
| `py.SignalType` | integer | 信号类型 |
| `py.SignalVisibleType` | integer | 信号可见类型 |
| `py.CursorKey` | integer | 鼠标编号 |
| `py.CursorState` | string | 鼠标状态 |
| `py.PlatformDecoType` | integer | 平台装饰类型 |
| `py.PlatformSigninType` | integer | 签到天数类型 |
| `py.PlatformCommunityType` | integer | 玩家社区互动类型 |
| `py.PhysicsObject` | py.Actor | 物理组件 |
| `py.PhysicsEntity` | py.Actor | 逻辑物理组件 |
| `py.PhysicsFilter` | py.Actor | 物理过滤器 |
| `py.PhysicsObjectKey` | integer | 物理组件类型 |
| `py.PhysicsEntityKey` | integer | 逻辑物理组件类型 |
| `py.RigidBody` | py.Actor | 刚体 |
| `py.RigidBodyGroup` | py.UIntList | 刚体组 |
| `py.Collider` | py.Actor | 碰撞体 |
| `py.Joint` | py.Actor | 关节 |
| `py.Reaction` | py.Actor | 物理Reaction |
| `py.ReactionGroup` | py.DynamicTypeMeta | 物理Reaction Group |
| `py.TableOrder` | integer | 表排序顺序 |
| `py.CameraMode` | integer | 镜头模式 |
| `py.CameraRayDirection` | integer | 相机射线方向 |
| `py.PhysicsEntityState` | integer | 逻辑物理组件状态 |
| `py.Map` | integer | 关卡 |
| `py.MoveDirection` | integer | 移动方向 |
| `py.ImageQuality` | integer | 画质 |
| `py.WatchingModeStatus` | integer | 观战模式状态 |
| `py.Force` | integer | 牵引力 |
| `py.SITE_STATE` | integer | steam位置状态 |
| `py.COIN_CURRENCY` | string | steam币种 |
