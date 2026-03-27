---
sidebarDepth: 1
---
# 事件 (Event)

# 索引

Y3 编辑器事件系统，用于注册和处理游戏中的各种事件。

---

| 事件 | 描述 | 所属对象 |
| --- | --- | --- |
| [游戏-初始化](#游戏-初始化) | 游戏初始化时触发。 | Game |
| [游戏-追帧完成](#游戏-追帧完成) | 游戏-追帧完成 | Game |
| [游戏-逻辑不同步](#游戏-逻辑不同步) | 游戏-逻辑不同步 | Game |
| [游戏-地形预设加载完成](#游戏-地形预设加载完成) | 游戏-地形预设加载完成 | Game |
| [游戏-结束](#游戏-结束) | 游戏结束时触发 | Game |
| [游戏-暂停](#游戏-暂停) | 游戏暂停时触发 | Game |
| [游戏-恢复](#游戏-恢复) | 游戏恢复时触发 | Game |
| [游戏-昼夜变化](#游戏-昼夜变化) | 通过参数判断进入白天还是进入夜晚 | Game |
| [区域-进入](#区域-进入) | 任意单位进入区域时触发 | Area |
| [区域-离开](#区域-离开) | 任意单位离开区域时触发 | Area |
| [游戏-http返回](#游戏-http返回) | 游戏-http返回 | Game |
| [游戏-接收广播信息](#游戏-接收广播信息) | 游戏-接收广播信息 | Game |
| [玩家-加入游戏](#玩家-加入游戏) | 玩家加入游戏时触发 | Player |
| [玩家-离开游戏](#玩家-离开游戏) | 玩家离开游戏时触发 | Player |
| [玩家-掉线](#玩家-掉线) | 玩家掉线时触发 | Player |
| [玩家-使用平台道具](#玩家-使用平台道具) | 玩家使用平台道具时触发 | Player |
| [玩家-持有平台道具](#玩家-持有平台道具) | 玩家进入游戏时如果持有指定平台道具会触发 | Player |
| [玩家-属性变化](#玩家-属性变化) | 玩家属性变化时触发 | Player |
| [玩家-发送指定消息](#玩家-发送指定消息) | 玩家发送指定消息时触发 | Game / Player |
| [玩家-科技提升](#玩家-科技提升) | 玩家科技每提升一级都会触发一次 | Player |
| [玩家-科技降低](#玩家-科技降低) | 玩家科技每降低一级都会触发一次 | Player |
| [玩家-科技变化](#玩家-科技变化) | 玩家科技变化时触发，一次变化多个等级也只会触发一次 | Player |
| [单位-研发科技](#单位-研发科技) | 单位研发科技时触发 | Unit |
| [单位-获得科技](#单位-获得科技) | 单位获得科技时触发 | Unit |
| [单位-失去科技](#单位-失去科技) | 单位失去科技时触发 | Unit |
| [玩家-关系变化](#玩家-关系变化) | 玩家之间的关系改变时触发 | Player |
| [玩家-重连](#玩家-重连) | 玩家重连时触发 | Player |
| [单位-建筑升级开始](#单位-建筑升级开始) | 单位-建筑升级开始 | Unit |
| [单位-建筑升级取消](#单位-建筑升级取消) | 单位-建筑升级取消 | Unit |
| [单位-建筑升级完成](#单位-建筑升级完成) | 单位-建筑升级完成 | Unit |
| [单位-建造开始](#单位-建造开始) | 单位-建造开始 | Unit |
| [单位-建造取消](#单位-建造取消) | 单位-建造取消 | Unit |
| [单位-建造完成](#单位-建造完成) | 单位-建造完成 | Unit |
| [技能-建造完成](#技能-建造完成) | 通过建造类技能建造完成时触发，可以获取到被建造出来的单位 | Ability |
| [技能-学习](#技能-学习) | 学习技能后触发 | Ability |
| [技能-可用状态变化](#技能-可用状态变化) | 技能-可用状态变化 | Ability |
| [技能-沉默状态变化](#技能-沉默状态变化) | 技能-沉默状态变化 | Ability |
| [技能-图标变化](#技能-图标变化) | 技能-图标变化 | Game |
| [单位-名称变化](#单位-名称变化) | 单位-名称变化 | Unit |
| [单位-小地图图标变化](#单位-小地图图标变化) | 单位-小地图图标变化 | Unit |
| [单位-头像变化](#单位-头像变化) | 单位-头像变化 | Unit |
| [单位-移除](#单位-移除) | 单位被移除后触发 | Unit |
| [单位-移除后](#单位-移除后) | 单位-移除后 | Unit |
| [单位-传送结束](#单位-传送结束) | 单位-传送结束 | Unit |
| [单位-属性变化](#单位-属性变化) | 指定单位的指定属性变化后触发 | Unit |
| [单位-即将死亡](#单位-即将死亡) | 单位死亡前触发 | Unit |
| [单位-死亡](#单位-死亡) | 单位死亡后触发 | Unit |
| [单位-受到伤害前](#单位-受到伤害前) | 在其他计算前触发，可以修改闪避 | Unit |
| [单位-造成伤害前](#单位-造成伤害前) | 在其他计算前触发，可以修改闪避 | Unit |
| [单位-受到伤害时](#单位-受到伤害时) | 可以修改伤害值 | Unit |
| [单位-造成伤害时](#单位-造成伤害时) | 可以修改伤害值 | Unit |
| [单位-造成伤害后](#单位-造成伤害后) | 伤害已结算，只能获取伤害值 | Unit |
| [单位-受到伤害后](#单位-受到伤害后) | 伤害已结算，只能获取伤害值 | Unit |
| [单位-受到治疗前](#单位-受到治疗前) | 可在其他计算前触发，可以修改有效性 | Unit |
| [单位-受到治疗后](#单位-受到治疗后) | 治疗已结算，只能获取治疗值 | Unit |
| [单位-受到治疗时](#单位-受到治疗时) | 可以修改治疗值 | Unit |
| [玩家-属性图标变化](#玩家-属性图标变化) | 玩家-属性图标变化 | Game |
| [单位-施放技能](#单位-施放技能) | 单位施放技能时触发 | Unit |
| [单位-获得经验前](#单位-获得经验前) | 单位获得经验前触发 | Unit |
| [单位-获得经验后](#单位-获得经验后) | 单位获得经验后触发 | Unit |
| [单位-接收命令](#单位-接收命令) | 接收到命令时触发，如果命令有目标会根据目标类型存到不同的字段里 | Unit |
| [单位-击杀](#单位-击杀) | 单位击杀其他单位时触发 | Unit |
| [单位-创建](#单位-创建) | 单位被创建后触发 | Unit |
| [单位-进入战斗](#单位-进入战斗) | 单位进入战斗时触发 | Unit |
| [单位-脱离战斗](#单位-脱离战斗) | 单位离开战斗时触发 | Unit |
| [单位-即将拾取物品](#单位-即将拾取物品) | 单位-即将拾取物品 | Unit |
| [单位-切换默认行为](#单位-切换默认行为) | 单位-切换默认行为 | Unit |
| [单位-即将索敌](#单位-即将索敌) | 单位-即将索敌 | Unit |
| [单位-发现目标](#单位-发现目标) | 单位-发现目标 | Unit |
| [本地-骨骼碰撞](#本地-骨骼碰撞) | 骨骼碰撞时触发 | Game |
| [物理-骨骼碰撞](#物理-骨骼碰撞) | 骨骼碰撞时触发 | Game |
| [单位-购买物品](#单位-购买物品) | 购买物品时触发 | Unit |
| [单位-购买单位](#单位-购买单位) | 购买单位时触发 | Unit |
| [单位-出售物品](#单位-出售物品) | 出售物品时触发 | Unit |
| [商店-商品变化](#商店-商品变化) | 商店-商品变化 | Game |
| [商店-库存变化](#商店-库存变化) | 商店-库存变化 | Game |
| [商店-售价变化](#商店-售价变化) | 商店-售价变化 | Game |
| [单位-物品合成](#单位-物品合成) | 物品合成时触发 | Unit |
| [单位-购买物品合成](#单位-购买物品合成) | 购买物品合成时触发 | Unit |
| [单位-复活](#单位-复活) | 单位复活后触发 | Unit |
| [单位-升级](#单位-升级) | 单位升级后触发 | Unit |
| [单位-进入草丛](#单位-进入草丛) | 单位进入草丛时触发 | Unit |
| [单位-离开草丛](#单位-离开草丛) | 单位离开草丛时触发 | Unit |
| [单位-改变所属](#单位-改变所属) | 单位的所有者玩家发生变化时触发 | Unit |
| [单位类型-前置条件成立](#单位类型-前置条件成立) | 前置条件由不成立变为成立时触发 | Game |
| [单位类型-前置条件不成立](#单位类型-前置条件不成立) | 前置条件由成立变为不成立时触发 | Game |
| [物品类型-前置条件成立](#物品类型-前置条件成立) | 前置条件由不成立变为成立时触发 | Game |
| [物品类型-前置条件不成立](#物品类型-前置条件不成立) | 前置条件由成立变为不成立时触发 | Game |
| [技能类型-前置条件成立](#技能类型-前置条件成立) | 前置条件由不成立变为成立时触发 | Game |
| [技能类型-前置条件不成立](#技能类型-前置条件不成立) | 前置条件由成立变为不成立时触发 | Game |
| [科技类型-前置条件成立](#科技类型-前置条件成立) | 前置条件由不成立变为成立时触发 | Game |
| [科技类型-前置条件不成立](#科技类型-前置条件不成立) | 前置条件由成立变为不成立时触发 | Game |
| [技能-升级](#技能-升级) | 技能升级后触发 | Ability |
| [施法-即将开始](#施法-即将开始) | 即将施法时触发 | Ability |
| [施法-开始](#施法-开始) | 施法开始后，前摇开始前触发 | Ability |
| [施法-引导](#施法-引导) | 前摇完成后，持续引导前触发 | Ability |
| [施法-出手](#施法-出手) | 持续引导后，后摇开始前触发 | Ability |
| [施法-完成](#施法-完成) | 后摇结束后触发。只有施法正常完成才会触发。 | Ability |
| [施法-结束](#施法-结束) | 整个施法的表现结束后触发 | Ability |
| [施法-打断开始](#施法-打断开始) | 在“开始”到“引导”之间被打断 | Ability |
| [施法-打断引导](#施法-打断引导) | 在“引导”到“出手”之间被打断 | Ability |
| [施法-打断出手](#施法-打断出手) | 在“出手”到“完成”之间被打断 | Ability |
| [施法-停止](#施法-停止) | 施法停止后触发，是施法流程的最后一个事件。 | Ability |
| [技能-获得](#技能-获得) | 获得技能后触发 | Ability |
| [技能-失去](#技能-失去) | 失去技能后触发 | Ability |
| [技能-交换](#技能-交换) | 技能交换后触发 | Ability |
| [技能-禁用](#技能-禁用) | 技能-禁用 | Ability |
| [技能-启用](#技能-启用) | 技能-启用 | Ability |
| [技能-冷却结束](#技能-冷却结束) | 技能冷却结束后触发 | Ability |
| [技能-自定义动画轴](#技能-自定义动画轴) | 技能-自定义动画轴 | Ability |
| [效果-获得](#效果-获得) | 获得魔法效果后触发 | Buff |
| [效果-失去](#效果-失去) | 失去魔法效果后触发 | Buff |
| [效果-心跳](#效果-心跳) | 魔法效果的周期性触发 | Buff |
| [效果-叠加](#效果-叠加) | 魔法效果叠加时触发 | Buff |
| [效果-层数变化](#效果-层数变化) | 魔法效果层数变化时触发 | Buff |
| [效果-即将获得](#效果-即将获得) | 魔法效果获得前触发 | Buff |
| [效果-覆盖](#效果-覆盖) | 魔法效果覆盖时触发 | Buff |
| [可破坏物-创建](#可破坏物-创建) | 可破坏物创建后触发 | Destructible |
| [可破坏物-死亡](#可破坏物-死亡) | 可破坏物死亡后触发 | Destructible |
| [可破坏物-复活](#可破坏物-复活) | 可破坏物复活后触发 | Destructible |
| [可破坏物-资源变化](#可破坏物-资源变化) | 可破坏物存储的资源变化后触发 | Destructible |
| [可破坏物-采集](#可破坏物-采集) | 可破坏物被采集后触发 | Destructible |
| [可破坏物-受到伤害](#可破坏物-受到伤害) | 可破坏物受到伤害后触发 | Destructible |
| [选中-可破坏物](#选中-可破坏物) | 玩家选中可破坏物被后触发 | Player |
| [本地-选中-可破坏物](#本地-选中-可破坏物) | 本地玩家选中可破坏物被后触发 | Player |
| [可破坏物-移除](#可破坏物-移除) | 可破坏物被移除后触发 | Destructible |
| [投射物-创建](#投射物-创建) | 投射物创建后触发 | Projectile |
| [投射物-死亡](#投射物-死亡) | 投射物死亡后触发 | Projectile |
| [界面-消息](#界面-消息) | 触发界面上标记的自定义事件后触发 | Game / Player |
| [玩家-点击小地图](#玩家-点击小地图) | 点击小地图时触发 | Game / Player |
| [界面-滑动条变化](#界面-滑动条变化) | 滑动条变化时触发 | Game / Player |
| [界面-聊天框可见性变化](#界面-聊天框可见性变化) | 聊天框可见性变化时触发 | Game / Player |
| [界面-装备拖拽](#界面-装备拖拽) | 界面-装备拖拽 | Game / Player |
| [界面-复选框变化](#界面-复选框变化) | 复选框变化时触发 | Game / Player |
| [界面-视频播放完成](#界面-视频播放完成) | 界面-视频播放完成 | Game / Player |
| [本地-界面-输入框获取焦点](#本地-界面-输入框获取焦点) | 本地-界面-输入框获取焦点 | Game / Player |
| [本地-界面-输入框失去焦点](#本地-界面-输入框失去焦点) | 本地-界面-输入框失去焦点 | Game / Player |
| [本地-界面-输入框内容改变](#本地-界面-输入框内容改变) | 本地-界面-输入框内容改变 | Game / Player |
| [键盘-按下](#键盘-按下) | 键盘上的某个键按下时触发 | Game / Player |
| [键盘-抬起](#键盘-抬起) | 键盘上的某个键抬起时触发 | Game / Player |
| [本地-键盘-按下](#本地-键盘-按下) | 键盘上的某个键按下时触发 | Game / Player |
| [本地-键盘-抬起](#本地-键盘-抬起) | 键盘上的某个键抬起时触发 | Game / Player |
| [鼠标-按下](#鼠标-按下) | 鼠标上的某个键按下时触发 | Game / Player |
| [鼠标-抬起](#鼠标-抬起) | 鼠标上的某个键抬起时触发 | Game / Player |
| [鼠标-双击](#鼠标-双击) | 鼠标上的某个键双击时触发 | Game / Player |
| [本地-鼠标-按下](#本地-鼠标-按下) | 鼠标上的某个键按下时触发 | Game / Player |
| [本地-鼠标-抬起](#本地-鼠标-抬起) | 鼠标上的某个键抬起时触发 | Game / Player |
| [本地-鼠标-双击](#本地-鼠标-双击) | 鼠标上的某个键双击时触发 | Game / Player |
| [鼠标-按下单位](#鼠标-按下单位) | 鼠标上的某个键对着单位按下时触发 | Game / Player |
| [鼠标-抬起单位](#鼠标-抬起单位) | 鼠标上的某个键对着单位抬起时触发 | Game / Player |
| [鼠标-双击单位](#鼠标-双击单位) | 鼠标上的某个键对着单位双击时触发 | Game / Player |
| [本地-鼠标-按下单位](#本地-鼠标-按下单位) | 鼠标上的某个键对着单位按下时触发 | Game / Player |
| [本地-鼠标-抬起单位](#本地-鼠标-抬起单位) | 鼠标上的某个键对着单位抬起时触发 | Game / Player |
| [本地-鼠标-双击单位](#本地-鼠标-双击单位) | 鼠标上的某个键对着单位双击时触发 | Game / Player |
| [鼠标-移动](#鼠标-移动) | 鼠标移动时触发 | Game / Player |
| [本地-鼠标-移动](#本地-鼠标-移动) | 鼠标移动时触发 | Game / Player |
| [鼠标-滚轮](#鼠标-滚轮) | 鼠标滚轮滚动时触发 | Game / Player |
| [本地-鼠标-滚轮](#本地-鼠标-滚轮) | 鼠标滚轮滚动时触发 | Game / Player |
| [选中-单位](#选中-单位) | 玩家选中单位时触发 | Player |
| [本地-选中-单位](#本地-选中-单位) | 本地玩家选中单位时触发 | Player |
| [选中-取消](#选中-取消) | 玩家主动取消选中时触发 | Player |
| [本地-选中-取消](#本地-选中-取消) | 玩家的选中状态被取消时触发 | Player |
| [选中-失去单位](#选中-失去单位) | 玩家被动失去对单位的选中状态时触发 | Player |
| [本地-选中-失去单位](#本地-选中-失去单位) | 本地玩家被动失去对单位的选中状态时触发 | Player |
| [选中-物品](#选中-物品) | 物品被选中时触发 | Player |
| [本地-选中-物品](#本地-选中-物品) | 本地玩家选中物品时触发 | Player |
| [玩家-检测到作弊](#玩家-检测到作弊) | 玩家-检测到作弊 | Player |
| [鼠标-双击物品](#鼠标-双击物品) | 鼠标上左键双击物品时触发 | Game / Player |
| [鼠标-双击可破坏物](#鼠标-双击可破坏物) | 鼠标上左键双击可破坏物时触发 | Game / Player |
| [选中-单位组](#选中-单位组) | 玩家选中单位组时触发 | Player |
| [本地-选中-单位组](#本地-选中-单位组) | 本地玩家选中单位组时触发 | Player |
| [技能-打开指示器](#技能-打开指示器) | 技能的瞄准指示器显示时触发 | Ability |
| [技能-建造技能释放前](#技能-建造技能释放前) | 建造技能的命令将要发布时 | Ability |
| [技能-关闭指示器](#技能-关闭指示器) | 技能的瞄准指示器消失时触发 | Ability |
| [物品-获得](#物品-获得) | 单位获得物品时触发 | Item |
| [物品-进入物品栏](#物品-进入物品栏) | 物品进入单位的物品栏时触发 | Item |
| [物品-进入背包](#物品-进入背包) | 物品进入单位的背包时触发 | Item |
| [物品-失去](#物品-失去) | 单位失去物品时触发 | Item |
| [物品-离开物品栏](#物品-离开物品栏) | 物品离开单位的物品栏时触发 | Item |
| [物品-离开背包](#物品-离开背包) | 物品离开单位的背包时触发 | Item |
| [物品-使用](#物品-使用) | 单位使用物品时触发 | Item |
| [单位-寻路开始](#单位-寻路开始) | 攻击、移动、施法等行为均可能导致寻路 | Unit |
| [单位-寻路结束](#单位-寻路结束) | 寻路到达目标位置或失败3次后触发 | Unit |
| [物品-堆叠变化](#物品-堆叠变化) | 物品堆叠数变化时触发 | Item |
| [物品-充能变化](#物品-充能变化) | 物品充能层数变化时触发 | Item |
| [物品-创建](#物品-创建) | 物品创建时触发 | Item |
| [物品-移除](#物品-移除) | 物品移除时触发 | Item |
| [物品-出售](#物品-出售) | 将物品出售给商店时触发 | Item |
| [物品-死亡](#物品-死亡) | 物品被破坏时触发 | Item |
| [物品-采集创建](#物品-采集创建) | 物品通过采集被创建时会触发该事件。采集功能来自可破坏物。 | Item |
| [命令-攻击移动](#命令-攻击移动) | 命令-攻击移动 | Unit |
| [命令-出售物品](#命令-出售物品) | 命令-出售物品 | Unit |
| [命令-施放技能](#命令-施放技能) | 命令-施放技能 | Unit |
| [命令-巡逻](#命令-巡逻) | 命令-巡逻 | Unit |
| [命令-移动](#命令-移动) | 命令-移动 | Unit |
| [鼠标-悬停](#鼠标-悬停) | 悬停进入或离开都会触发 | Game / Player |
| [本地-鼠标-悬停](#本地-鼠标-悬停) | 悬停进入或离开都会触发 | Game / Player |
| [玩家-发送消息](#玩家-发送消息) | 玩家发送任意消息时触发 | Game / Player |
| [游戏-消息](#游戏-消息) | 在事件管理处定义的事件通过这个方法进行触发 | Game |
| [玩家-语音发言](#玩家-语音发言) | 玩家开始语音和结束语音都会触发 | Game / Player |
| [玩家-平台道具变化](#玩家-平台道具变化) | 玩家平台道具变化时触发 | Player |
| [玩家-平台商城窗口变化](#玩家-平台商城窗口变化) | 平台商城窗口变化事件 | Game / Player |
| [控制台-输入](#控制台-输入) | 控制台-输入 | Game |
| [控制台-请求补全](#控制台-请求补全) | 控制台-请求补全 | Game |
| [steam-收到好友申请](#steam-收到好友申请) | steam-收到好友申请 | Game |
| [steam-收到被好友删除](#steam-收到被好友删除) | steam-收到被好友删除 | Game |
| [steam-好友在线状态变化](#steam-好友在线状态变化) | steam-好友在线状态变化 | Game |
| [steam-本地玩家队伍变化](#steam-本地玩家队伍变化) | steam-本地玩家队伍变化 | Game |
| [steam-收到队伍邀请](#steam-收到队伍邀请) | steam-收到队伍邀请 | Game |
| [steam-进入大厅](#steam-进入大厅) | steam-进入大厅 | Game |
| [steam-开始匹配](#steam-开始匹配) | steam-开始匹配 | Game |
| [steam-取消匹配](#steam-取消匹配) | steam-取消匹配 | Game |
| [steam-本地房间信息变化](#steam-本地房间信息变化) | steam-本地房间信息变化 | Game |
| [steam-被邀请加入房间](#steam-被邀请加入房间) | steam-被邀请加入房间 | Game |
| [steam-被踢出房间](#steam-被踢出房间) | steam-被踢出房间 | Game |
| [steam-创建房间成功](#steam-创建房间成功) | steam-创建房间成功 | Game |

---

## 游戏-初始化

event in Game

- 描述

    游戏初始化时触发。

- 注册参数

    无

- 事件参数 (data)

    无

- 示例

```lua
y3.game:event('游戏-初始化', function(trg, data)
    -- 无事件参数
end)
```

---

## 游戏-追帧完成

event in Game

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    无

- 示例

```lua
y3.game:event('游戏-追帧完成', function(trg, data)
    -- 无事件参数
end)
```

---

## 游戏-逻辑不同步

event in Game

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | int1 | integer | 不同步帧号 |

- 示例

```lua
y3.game:event('游戏-逻辑不同步', function(trg, data)
    local int1 = data.int1  -- 不同步帧号
end)
```

---

## 游戏-地形预设加载完成

event in Game

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | scene_preset | py.ScenePreset | 场景预设hash |

- 示例

```lua
y3.game:event('游戏-地形预设加载完成', function(trg, data)
    local scene_preset = data.scene_preset  -- 场景预设hash
end)
```

---

## 游戏-结束

event in Game

- 描述

    游戏结束时触发

- 注册参数

    无

- 事件参数 (data)

    无

- 示例

```lua
y3.game:event('游戏-结束', function(trg, data)
    -- 无事件参数
end)
```

---

## 游戏-暂停

event in Game

- 描述

    游戏暂停时触发

- 注册参数

    无

- 事件参数 (data)

    无

- 示例

```lua
y3.game:event('游戏-暂停', function(trg, data)
    -- 无事件参数
end)
```

---

## 游戏-恢复

event in Game

- 描述

    游戏恢复时触发

- 注册参数

    无

- 事件参数 (data)

    无

- 示例

```lua
y3.game:event('游戏-恢复', function(trg, data)
    -- 无事件参数
end)
```

---

## 游戏-昼夜变化

event in Game

- 描述

    通过参数判断进入白天还是进入夜晚

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_day_to_night | boolean | 是否是白天转到黑夜 |

- 示例

```lua
y3.game:event('游戏-昼夜变化', function(trg, data)
    local is_day_to_night = data.is_day_to_night  -- 是否是白天转到黑夜
end)
```

---

## 区域-进入

event in Area

- 描述

    任意单位进入区域时触发

- 注册参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | Area | 区域 |

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 单位 |
    | area | Area | 区域 |
    | trigger_id | py.TriggerID | 触发器ID |

- 示例

```lua
local area = y3.area.get_by_id(1)

area:event('区域-进入', area, function(trg, data)
    local unit = data.unit  -- 单位
    local area = data.area  -- 区域
    local trigger_id = data.trigger_id  -- 触发器ID
end)
```

---

## 区域-离开

event in Area

- 描述

    任意单位离开区域时触发

- 注册参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | area | Area | 区域 |

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 单位 |
    | area | Area | 区域 |
    | trigger_id | py.TriggerID | 触发器ID |

- 示例

```lua
local area = y3.area.get_by_id(1)

area:event('区域-离开', area, function(trg, data)
    local unit = data.unit  -- 单位
    local area = data.area  -- 区域
    local trigger_id = data.trigger_id  -- 触发器ID
end)
```

---

## 游戏-http返回

event in Game

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | http_req | string | http请求 |
    | http_resp_body | string | 响应内容 |
    | http_resp_status | string | 响应状态 |

- 示例

```lua
y3.game:event('游戏-http返回', function(trg, data)
    local http_req = data.http_req  -- http请求
    local http_resp_body = data.http_resp_body  -- 响应内容
    local http_resp_status = data.http_resp_status  -- 响应状态
end)
```

---

## 游戏-接收广播信息

event in Game

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | broadcast_lua_msg_id | string | 消息id |
    | broadcast_lua_msg_content | string | 消息内容 |
    | player | Player | 玩家 |

- 示例

```lua
y3.game:event('游戏-接收广播信息', function(trg, data)
    local broadcast_lua_msg_id = data.broadcast_lua_msg_id  -- 消息id
    local broadcast_lua_msg_content = data.broadcast_lua_msg_content  -- 消息内容
    local player = data.player  -- 玩家
end)
```

---

## 玩家-加入游戏

event in Player

- 描述

    玩家加入游戏时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | is_middle_join | boolean | 是否中途加入 |

- 示例

```lua
local player = y3.player.get_by_id(1)

player:event('玩家-加入游戏', function(trg, data)
    local player = data.player  -- 玩家
    local is_middle_join = data.is_middle_join  -- 是否中途加入
end)
```

---

## 玩家-离开游戏

event in Player

- 描述

    玩家离开游戏时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |

- 示例

```lua
local player = y3.player.get_by_id(1)

player:event('玩家-离开游戏', function(trg, data)
    local player = data.player  -- 玩家
end)
```

---

## 玩家-掉线

event in Player

- 描述

    玩家掉线时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |

- 示例

```lua
local player = y3.player.get_by_id(1)

player:event('玩家-掉线', function(trg, data)
    local player = data.player  -- 玩家
end)
```

---

## 玩家-使用平台道具

event in Player

- 描述

    玩家使用平台道具时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | store_key | py.StoreKey | 收费道具编号 |
    | use_cnt | integer | 使用次数 |

- 示例

```lua
local player = y3.player.get_by_id(1)

player:event('玩家-使用平台道具', function(trg, data)
    local player = data.player  -- 玩家
    local store_key = data.store_key  -- 收费道具编号
    local use_cnt = data.use_cnt  -- 使用次数
end)
```

---

## 玩家-持有平台道具

event in Player

- 描述

    玩家进入游戏时如果持有指定平台道具会触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | store_key | py.StoreKey | 收费道具编号 |

- 示例

```lua
local player = y3.player.get_by_id(1)

player:event('玩家-持有平台道具', function(trg, data)
    local player = data.player  -- 玩家
    local store_key = data.store_key  -- 收费道具编号
end)
```

---

## 玩家-属性变化

event in Player

- 描述

    玩家属性变化时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | res_key | py.RoleResKey | 玩家资源类型 |
    | res_value | integer | 玩家资源值 |
    | res_value_delta | number | 玩家资源变量值 |

- 示例

```lua
local player = y3.player.get_by_id(1)

player:event('玩家-属性变化', function(trg, data)
    local player = data.player  -- 玩家
    local res_key = data.res_key  -- 玩家资源类型
    local res_value = data.res_value  -- 玩家资源值
    local res_value_delta = data.res_value_delta  -- 玩家资源变量值
end)
```

---

## 玩家-发送指定消息

event in Game / Player

- 描述

    玩家发送指定消息时触发

- 注册参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | msg | string | 消息内容 |

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | msg | string | 字符串 |

- 示例

```lua
-- 方式1: 通过 y3.game 注册（监听所有玩家）
y3.game:event('玩家-发送指定消息', "msg", function(trg, data)
    local player = data.player  -- 玩家
    local msg = data.msg  -- 字符串
end)

-- 方式2: 通过 Player 对象注册（监听特定对象）
local player = y3.player.get_by_id(1)

player:event('玩家-发送指定消息', "msg", function(trg, data)
    local player = data.player  -- 玩家
    local msg = data.msg  -- 字符串
end)
```

---

## 玩家-科技提升

event in Player

- 描述

    玩家科技每提升一级都会触发一次

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | tech_no | py.TechKey | 科技编号 |
    | curr_lv | integer | 当前科技等级 |

- 示例

```lua
local player = y3.player.get_by_id(1)

player:event('玩家-科技提升', function(trg, data)
    local player = data.player  -- 玩家
    local tech_no = data.tech_no  -- 科技编号
    local curr_lv = data.curr_lv  -- 当前科技等级
end)
```

---

## 玩家-科技降低

event in Player

- 描述

    玩家科技每降低一级都会触发一次

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | tech_no | py.TechKey | 科技编号 |
    | curr_lv | integer | 当前科技等级 |

- 示例

```lua
local player = y3.player.get_by_id(1)

player:event('玩家-科技降低', function(trg, data)
    local player = data.player  -- 玩家
    local tech_no = data.tech_no  -- 科技编号
    local curr_lv = data.curr_lv  -- 当前科技等级
end)
```

---

## 玩家-科技变化

event in Player

- 描述

    玩家科技变化时触发，一次变化多个等级也只会触发一次

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | tech_no | py.TechKey | 科技编号 |
    | curr_lv | integer | 当前科技等级 |
    | delta_lv | integer | 科技变化等级 |

- 示例

```lua
local player = y3.player.get_by_id(1)

player:event('玩家-科技变化', function(trg, data)
    local player = data.player  -- 玩家
    local tech_no = data.tech_no  -- 科技编号
    local curr_lv = data.curr_lv  -- 当前科技等级
    local delta_lv = data.delta_lv  -- 科技变化等级
end)
```

---

## 单位-研发科技

event in Unit

- 描述

    单位研发科技时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 单位 |
    | player | Player | 单位所属玩家 |
    | tech_no | py.TechKey | 科技编号 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-研发科技', function(trg, data)
    local unit = data.unit  -- 单位
    local player = data.player  -- 单位所属玩家
    local tech_no = data.tech_no  -- 科技编号
end)
```

---

## 单位-获得科技

event in Unit

- 描述

    单位获得科技时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 单位 |
    | player | Player | 单位所属玩家 |
    | tech_no | py.TechKey | 科技编号 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-获得科技', function(trg, data)
    local unit = data.unit  -- 单位
    local player = data.player  -- 单位所属玩家
    local tech_no = data.tech_no  -- 科技编号
end)
```

---

## 单位-失去科技

event in Unit

- 描述

    单位失去科技时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 单位 |
    | player | Player | 单位所属玩家 |
    | tech_no | py.TechKey | 科技编号 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-失去科技', function(trg, data)
    local unit = data.unit  -- 单位
    local player = data.player  -- 单位所属玩家
    local tech_no = data.tech_no  -- 科技编号
end)
```

---

## 玩家-关系变化

event in Player

- 描述

    玩家之间的关系改变时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | src_player | Player | 源玩家 |
    | dst_player | Player | 目标玩家 |
    | relation | py.RoleRelation | 关系 |

- 示例

```lua
local player = y3.player.get_by_id(1)

player:event('玩家-关系变化', function(trg, data)
    local src_player = data.src_player  -- 源玩家
    local dst_player = data.dst_player  -- 目标玩家
    local relation = data.relation  -- 关系
end)
```

---

## 玩家-重连

event in Player

- 描述

    玩家重连时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |

- 示例

```lua
local player = y3.player.get_by_id(1)

player:event('玩家-重连', function(trg, data)
    local player = data.player  -- 玩家
end)
```

---

## 单位-建筑升级开始

event in Unit

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 开始升级的建筑单位 |
    | old_unit_key | py.UnitKey | 老的单位物编 |
    | new_unit_key | py.UnitKey | 新的单位物编 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-建筑升级开始', function(trg, data)
    local unit = data.unit  -- 开始升级的建筑单位
    local old_unit_key = data.old_unit_key  -- 老的单位物编
    local new_unit_key = data.new_unit_key  -- 新的单位物编
end)
```

---

## 单位-建筑升级取消

event in Unit

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 取消升级的建筑单位 |
    | old_unit_key | py.UnitKey | 老的单位物编 |
    | new_unit_key | py.UnitKey | 新的单位物编 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-建筑升级取消', function(trg, data)
    local unit = data.unit  -- 取消升级的建筑单位
    local old_unit_key = data.old_unit_key  -- 老的单位物编
    local new_unit_key = data.new_unit_key  -- 新的单位物编
end)
```

---

## 单位-建筑升级完成

event in Unit

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 升级完成的建筑单位 |
    | old_unit_key | py.UnitKey | 老的单位物编 |
    | new_unit_key | py.UnitKey | 新的单位物编 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-建筑升级完成', function(trg, data)
    local unit = data.unit  -- 升级完成的建筑单位
    local old_unit_key = data.old_unit_key  -- 老的单位物编
    local new_unit_key = data.new_unit_key  -- 新的单位物编
end)
```

---

## 单位-建造开始

event in Unit

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 开始建造的单位 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-建造开始', function(trg, data)
    local unit = data.unit  -- 开始建造的单位
end)
```

---

## 单位-建造取消

event in Unit

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 取消建造的单位 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-建造取消', function(trg, data)
    local unit = data.unit  -- 取消建造的单位
end)
```

---

## 单位-建造完成

event in Unit

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 建造完成的单位 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-建造完成', function(trg, data)
    local unit = data.unit  -- 建造完成的单位
end)
```

---

## 技能-建造完成

event in Ability

- 描述

    通过建造类技能建造完成时触发，可以获取到被建造出来的单位

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability | Ability | 技能 |
    | ability_type | py.AbilityType | 技能类型 |
    | ability_index | py.AbilityIndex | 技能ID |
    | ability_seq | py.AbilitySeq | 技能Seq |
    | unit | Unit | 主人 |
    | build_unit | Unit | 建造出来的单位 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:event('技能-建造完成', function(trg, data)
    local ability = data.ability  -- 技能
    local ability_type = data.ability_type  -- 技能类型
    local ability_index = data.ability_index  -- 技能ID
    local ability_seq = data.ability_seq  -- 技能Seq
    local unit = data.unit  -- 主人
    local build_unit = data.build_unit  -- 建造出来的单位
end)
```

---

## 技能-学习

event in Ability

- 描述

    学习技能后触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_index | py.AbilityIndex | 技能坑位 |
    | ability | Ability | 技能对象 |
    | unit | Unit | 单位 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:event('技能-学习', function(trg, data)
    local ability_index = data.ability_index  -- 技能坑位
    local ability = data.ability  -- 技能对象
    local unit = data.unit  -- 单位
end)
```

---

## 技能-可用状态变化

event in Ability

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_index | py.AbilityIndex | 技能坑位 |
    | is_forbidden | boolean | 是否禁用 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:event('技能-可用状态变化', function(trg, data)
    local ability_index = data.ability_index  -- 技能坑位
    local is_forbidden = data.is_forbidden  -- 是否禁用
end)
```

---

## 技能-沉默状态变化

event in Ability

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_silent | boolean | 是否禁用 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:event('技能-沉默状态变化', function(trg, data)
    local is_silent = data.is_silent  -- 是否禁用
end)
```

---

## 技能-图标变化

event in Game

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    无

- 示例

```lua
y3.game:event('技能-图标变化', function(trg, data)
    -- 无事件参数
end)
```

---

## 单位-名称变化

event in Unit

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-名称变化', function(trg, data)
    -- 无事件参数
end)
```

---

## 单位-小地图图标变化

event in Unit

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-小地图图标变化', function(trg, data)
    -- 无事件参数
end)
```

---

## 单位-头像变化

event in Unit

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-头像变化', function(trg, data)
    local unit = data.unit
end)
```

---

## 单位-移除

event in Unit

- 描述

    单位被移除后触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-移除', function(trg, data)
    local unit = data.unit
end)
```

---

## 单位-移除后

event in Unit

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-移除后', function(trg, data)
    local unit = data.unit
end)
```

---

## 单位-传送结束

event in Unit

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-传送结束', function(trg, data)
    local unit = data.unit
end)
```

---

## 单位-属性变化

event in Unit

- 描述

    指定单位的指定属性变化后触发

- 注册参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 单位 |
    | attr | string | 属性名 |

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit |  |
    | attr | string |  |
    | old_float_attr_value | number |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-属性变化', unit, "attr", function(trg, data)
    local unit = data.unit
    local attr = data.attr
    local old_float_attr_value = data.old_float_attr_value
end)
```

---

## 单位-即将死亡

event in Unit

- 描述

    单位死亡前触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | damage | number | 受到的伤害值 |
    | source_unit | Unit | 施加伤害的单位 |
    | target_unit | Unit | 承受伤害的单位 |
    | ability | Ability | 当前伤害所属技能 |
    | damage_type | integer | 伤害类型 |
    | unit | Unit |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-即将死亡', function(trg, data)
    local damage = data.damage  -- 受到的伤害值
    local source_unit = data.source_unit  -- 施加伤害的单位
    local target_unit = data.target_unit  -- 承受伤害的单位
    local ability = data.ability  -- 当前伤害所属技能
    local damage_type = data.damage_type  -- 伤害类型
    local unit = data.unit
end)
```

---

## 单位-死亡

event in Unit

- 描述

    单位死亡后触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | damage | number | 受到的伤害值 |
    | source_unit | Unit | 施加伤害的单位 |
    | target_unit | Unit | 承受伤害的单位 |
    | ability | Ability | 当前伤害所属技能 |
    | damage_type | integer | 伤害类型 |
    | unit | Unit |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-死亡', function(trg, data)
    local damage = data.damage  -- 受到的伤害值
    local source_unit = data.source_unit  -- 施加伤害的单位
    local target_unit = data.target_unit  -- 承受伤害的单位
    local ability = data.ability  -- 当前伤害所属技能
    local damage_type = data.damage_type  -- 伤害类型
    local unit = data.unit
end)
```

---

## 单位-受到伤害前

event in Unit

- 描述

    在其他计算前触发，可以修改闪避

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_normal_hit | boolean | 是否是普通攻击 |
    | damage | number | 受到的伤害值 |
    | source_unit | Unit | 施加伤害的单位 |
    | target_unit | Unit | 承受伤害的单位 |
    | ability | Ability | 当前伤害所属技能 |
    | damage_type | integer | 伤害类型 |
    | unit | Unit |  |
    | damage_instance | DamageInstance | 伤害实例 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-受到伤害前', function(trg, data)
    local is_normal_hit = data.is_normal_hit  -- 是否是普通攻击
    local damage = data.damage  -- 受到的伤害值
    local source_unit = data.source_unit  -- 施加伤害的单位
    local target_unit = data.target_unit  -- 承受伤害的单位
    local ability = data.ability  -- 当前伤害所属技能
    local damage_type = data.damage_type  -- 伤害类型
    local unit = data.unit
    local damage_instance = data.damage_instance  -- 伤害实例
end)
```

---

## 单位-造成伤害前

event in Unit

- 描述

    在其他计算前触发，可以修改闪避

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_normal_hit | boolean | 是否是普通攻击 |
    | damage | number | 受到的伤害值 |
    | source_unit | Unit | 施加伤害的单位 |
    | target_unit | Unit | 承受伤害的单位 |
    | ability | Ability | 当前伤害所属技能 |
    | damage_type | integer | 伤害类型 |
    | unit | Unit |  |
    | damage_instance | DamageInstance | 伤害实例 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-造成伤害前', function(trg, data)
    local is_normal_hit = data.is_normal_hit  -- 是否是普通攻击
    local damage = data.damage  -- 受到的伤害值
    local source_unit = data.source_unit  -- 施加伤害的单位
    local target_unit = data.target_unit  -- 承受伤害的单位
    local ability = data.ability  -- 当前伤害所属技能
    local damage_type = data.damage_type  -- 伤害类型
    local unit = data.unit
    local damage_instance = data.damage_instance  -- 伤害实例
end)
```

---

## 单位-受到伤害时

event in Unit

- 描述

    可以修改伤害值

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_normal_hit | boolean | 是否是普通攻击 |
    | damage | number | 受到的伤害值 |
    | source_unit | Unit | 施加伤害的单位 |
    | target_unit | Unit | 承受伤害的单位 |
    | ability | Ability | 当前伤害所属技能 |
    | damage_type | integer | 伤害类型 |
    | unit | Unit |  |
    | damage_instance | DamageInstance | 伤害实例 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-受到伤害时', function(trg, data)
    local is_normal_hit = data.is_normal_hit  -- 是否是普通攻击
    local damage = data.damage  -- 受到的伤害值
    local source_unit = data.source_unit  -- 施加伤害的单位
    local target_unit = data.target_unit  -- 承受伤害的单位
    local ability = data.ability  -- 当前伤害所属技能
    local damage_type = data.damage_type  -- 伤害类型
    local unit = data.unit
    local damage_instance = data.damage_instance  -- 伤害实例
end)
```

---

## 单位-造成伤害时

event in Unit

- 描述

    可以修改伤害值

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_normal_hit | boolean | 是否是普通攻击 |
    | damage | number | 受到的伤害值 |
    | source_unit | Unit | 施加伤害的单位 |
    | target_unit | Unit | 承受伤害的单位 |
    | ability | Ability | 当前伤害所属技能 |
    | damage_type | integer | 伤害类型 |
    | unit | Unit |  |
    | damage_instance | DamageInstance | 伤害实例 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-造成伤害时', function(trg, data)
    local is_normal_hit = data.is_normal_hit  -- 是否是普通攻击
    local damage = data.damage  -- 受到的伤害值
    local source_unit = data.source_unit  -- 施加伤害的单位
    local target_unit = data.target_unit  -- 承受伤害的单位
    local ability = data.ability  -- 当前伤害所属技能
    local damage_type = data.damage_type  -- 伤害类型
    local unit = data.unit
    local damage_instance = data.damage_instance  -- 伤害实例
end)
```

---

## 单位-造成伤害后

event in Unit

- 描述

    伤害已结算，只能获取伤害值

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_critical_hit | boolean | 是否是暴击 |
    | is_normal_hit | boolean | 是否是普通攻击 |
    | damage | number | 受到的伤害值 |
    | source_unit | Unit | 施加伤害的单位 |
    | target_unit | Unit | 承受伤害的单位 |
    | ability | Ability | 当前伤害所属技能 |
    | damage_type | integer | 伤害类型 |
    | unit | Unit |  |
    | damage_instance | DamageInstance | 伤害实例 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-造成伤害后', function(trg, data)
    local is_critical_hit = data.is_critical_hit  -- 是否是暴击
    local is_normal_hit = data.is_normal_hit  -- 是否是普通攻击
    local damage = data.damage  -- 受到的伤害值
    local source_unit = data.source_unit  -- 施加伤害的单位
    local target_unit = data.target_unit  -- 承受伤害的单位
    local ability = data.ability  -- 当前伤害所属技能
    local damage_type = data.damage_type  -- 伤害类型
    local unit = data.unit
    local damage_instance = data.damage_instance  -- 伤害实例
end)
```

---

## 单位-受到伤害后

event in Unit

- 描述

    伤害已结算，只能获取伤害值

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | is_critical_hit | boolean | 是否是暴击 |
    | is_normal_hit | boolean | 是否是普通攻击 |
    | damage | number | 受到的伤害值 |
    | source_unit | Unit | 施加伤害的单位 |
    | target_unit | Unit | 承受伤害的单位 |
    | ability | Ability | 当前伤害所属技能 |
    | damage_type | integer | 伤害类型 |
    | unit | Unit |  |
    | damage_instance | DamageInstance | 伤害实例 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-受到伤害后', function(trg, data)
    local is_critical_hit = data.is_critical_hit  -- 是否是暴击
    local is_normal_hit = data.is_normal_hit  -- 是否是普通攻击
    local damage = data.damage  -- 受到的伤害值
    local source_unit = data.source_unit  -- 施加伤害的单位
    local target_unit = data.target_unit  -- 承受伤害的单位
    local ability = data.ability  -- 当前伤害所属技能
    local damage_type = data.damage_type  -- 伤害类型
    local unit = data.unit
    local damage_instance = data.damage_instance  -- 伤害实例
end)
```

---

## 单位-受到治疗前

event in Unit

- 描述

    可在其他计算前触发，可以修改有效性

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | source_unit | Unit | 治疗来源单位 |
    | target_unit | Unit | 被治疗的单位 |
    | cured_value | number | 受到的治疗值 |
    | ability | Ability | 当前治疗所属技能 |
    | heal_instance | HealInstance | 治疗实例 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-受到治疗前', function(trg, data)
    local source_unit = data.source_unit  -- 治疗来源单位
    local target_unit = data.target_unit  -- 被治疗的单位
    local cured_value = data.cured_value  -- 受到的治疗值
    local ability = data.ability  -- 当前治疗所属技能
    local heal_instance = data.heal_instance  -- 治疗实例
end)
```

---

## 单位-受到治疗后

event in Unit

- 描述

    治疗已结算，只能获取治疗值

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | source_unit | Unit | 治疗来源单位 |
    | target_unit | Unit | 被治疗的单位 |
    | cured_value | number | 受到的治疗值 |
    | ability | Ability | 当前治疗所属技能 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-受到治疗后', function(trg, data)
    local source_unit = data.source_unit  -- 治疗来源单位
    local target_unit = data.target_unit  -- 被治疗的单位
    local cured_value = data.cured_value  -- 受到的治疗值
    local ability = data.ability  -- 当前治疗所属技能
end)
```

---

## 单位-受到治疗时

event in Unit

- 描述

    可以修改治疗值

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | source_unit | Unit | 治疗来源单位 |
    | target_unit | Unit | 被治疗的单位 |
    | cured_value | number | 受到的治疗值 |
    | ability | Ability | 当前治疗所属技能 |
    | heal_instance | HealInstance | 治疗实例 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-受到治疗时', function(trg, data)
    local source_unit = data.source_unit  -- 治疗来源单位
    local target_unit = data.target_unit  -- 被治疗的单位
    local cured_value = data.cured_value  -- 受到的治疗值
    local ability = data.ability  -- 当前治疗所属技能
    local heal_instance = data.heal_instance  -- 治疗实例
end)
```

---

## 玩家-属性图标变化

event in Game

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | res_key | py.RoleResKey | 资源 |
    | icon_id | integer | ICON ID |

- 示例

```lua
y3.game:event('玩家-属性图标变化', function(trg, data)
    local res_key = data.res_key  -- 资源
    local icon_id = data.icon_id  -- ICON ID
end)
```

---

## 单位-施放技能

event in Unit

- 描述

    单位施放技能时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability | Ability | 施放的技能对象 |
    | unit | Unit | 触发事件的单位unit_ |
    | ability_target_unit | Unit | 技能的目标单位 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-施放技能', function(trg, data)
    local ability = data.ability  -- 施放的技能对象
    local unit = data.unit  -- 触发事件的单位unit_
    local ability_target_unit = data.ability_target_unit  -- 技能的目标单位
end)
```

---

## 单位-获得经验前

event in Unit

- 描述

    单位获得经验前触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 获得经验的单位 |
    | add_exp | number | 增加的经验 |
    | set_exp | fun(exp: number) | 修改经验 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-获得经验前', function(trg, data)
    local unit = data.unit  -- 获得经验的单位
    local add_exp = data.add_exp  -- 增加的经验
    local set_exp = data.set_exp  -- 修改经验
end)
```

---

## 单位-获得经验后

event in Unit

- 描述

    单位获得经验后触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 获得经验的单位 |
    | add_exp | number | 增加的经验 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-获得经验后', function(trg, data)
    local unit = data.unit  -- 获得经验的单位
    local add_exp = data.add_exp  -- 增加的经验
end)
```

---

## 单位-接收命令

event in Unit

- 描述

    接收到命令时触发，如果命令有目标会根据目标类型存到不同的字段里

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 单位 |
    | cmd_type | py.UnitCommand | 接收的命令 |
    | target_unit | Unit | 目标单位 |
    | point | Point | 目标点 |
    | destructible | Destructible | 目标可破坏物 |
    | item | Item | 目标物品 |
    | ability | Ability | 释放的技能 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-接收命令', function(trg, data)
    local unit = data.unit  -- 单位
    local cmd_type = data.cmd_type  -- 接收的命令
    local target_unit = data.target_unit  -- 目标单位
    local point = data.point  -- 目标点
    local destructible = data.destructible  -- 目标可破坏物
    local item = data.item  -- 目标物品
    local ability = data.ability  -- 释放的技能
end)
```

---

## 单位-击杀

event in Unit

- 描述

    单位击杀其他单位时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | damage | number | 伤害值 |
    | source_unit | Unit | 杀手单位 |
    | target_unit | Unit | 死亡单位 |
    | ability | Ability | 致命伤害所属技能 |
    | damage_type | integer | 致命伤害类型 |
    | unit | Unit |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-击杀', function(trg, data)
    local damage = data.damage  -- 伤害值
    local source_unit = data.source_unit  -- 杀手单位
    local target_unit = data.target_unit  -- 死亡单位
    local ability = data.ability  -- 致命伤害所属技能
    local damage_type = data.damage_type  -- 致命伤害类型
    local unit = data.unit
end)
```

---

## 单位-创建

event in Unit

- 描述

    单位被创建后触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit |  |
    | lua_table | py.Table | 用户自定义配置表 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-创建', function(trg, data)
    local unit = data.unit
    local lua_table = data.lua_table  -- 用户自定义配置表
end)
```

---

## 单位-进入战斗

event in Unit

- 描述

    单位进入战斗时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 单位 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-进入战斗', function(trg, data)
    local unit = data.unit  -- 单位
end)
```

---

## 单位-脱离战斗

event in Unit

- 描述

    单位离开战斗时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 单位 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-脱离战斗', function(trg, data)
    local unit = data.unit  -- 单位
end)
```

---

## 单位-即将拾取物品

event in Unit

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 单位 |
    | equip_slot_type | py.SlotType | 背包类型 |
    | item | Item | 目标物品 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-即将拾取物品', function(trg, data)
    local unit = data.unit  -- 单位
    local equip_slot_type = data.equip_slot_type  -- 背包类型
    local item = data.item  -- 目标物品
end)
```

---

## 单位-切换默认行为

event in Unit

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    无

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-切换默认行为', function(trg, data)
    -- 无事件参数
end)
```

---

## 单位-即将索敌

event in Unit

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 单位 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-即将索敌', function(trg, data)
    local unit = data.unit  -- 单位
end)
```

---

## 单位-发现目标

event in Unit

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 单位 |
    | target_unit | Unit | 目标单位 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-发现目标', function(trg, data)
    local unit = data.unit  -- 单位
    local target_unit = data.target_unit  -- 目标单位
end)
```

---

## 本地-骨骼碰撞

event in Game

- 描述

    骨骼碰撞时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | source_unit | Unit |  |
    | target_unit | Unit |  |
    | src_bone | string |  |
    | target_bone | string |  |
    | hitPos | Point |  |
    | hitNormal | Point |  |

- 示例

```lua
y3.game:event('本地-骨骼碰撞', function(trg, data)
    local source_unit = data.source_unit
    local target_unit = data.target_unit
    local src_bone = data.src_bone
    local target_bone = data.target_bone
    local hitPos = data.hitPos
    local hitNormal = data.hitNormal
end)
```

---

## 物理-骨骼碰撞

event in Game

- 描述

    骨骼碰撞时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | source_unit | Unit |  |
    | target_unit | Unit |  |
    | src_bone | string |  |
    | target_bone | string |  |
    | hitPos | Point |  |
    | hitNormal | Point |  |

- 示例

```lua
y3.game:event('物理-骨骼碰撞', function(trg, data)
    local source_unit = data.source_unit
    local target_unit = data.target_unit
    local src_bone = data.src_bone
    local target_bone = data.target_bone
    local hitPos = data.hitPos
    local hitNormal = data.hitNormal
end)
```

---

## 单位-购买物品

event in Unit

- 描述

    购买物品时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 购买物品单位 |
    | shop_unit | Unit | 商店单位 |
    | tab_idx | integer | 商店分页 |
    | cnt | integer | 商品数量 |
    | item | Item | 商品物品 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-购买物品', function(trg, data)
    local unit = data.unit  -- 购买物品单位
    local shop_unit = data.shop_unit  -- 商店单位
    local tab_idx = data.tab_idx  -- 商店分页
    local cnt = data.cnt  -- 商品数量
    local item = data.item  -- 商品物品
end)
```

---

## 单位-购买单位

event in Unit

- 描述

    购买单位时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 购买物品单位 |
    | shop_unit | Unit | 商店单位 |
    | tab_idx | integer | 商店分页 |
    | cnt | integer | 商品数量 |
    | unit_stuff | Unit | 商品单位 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-购买单位', function(trg, data)
    local unit = data.unit  -- 购买物品单位
    local shop_unit = data.shop_unit  -- 商店单位
    local tab_idx = data.tab_idx  -- 商店分页
    local cnt = data.cnt  -- 商品数量
    local unit_stuff = data.unit_stuff  -- 商品单位
end)
```

---

## 单位-出售物品

event in Unit

- 描述

    出售物品时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 购买物品单位 |
    | shop_unit | Unit | 商店单位 |
    | item | Item | 道具 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-出售物品', function(trg, data)
    local unit = data.unit  -- 购买物品单位
    local shop_unit = data.shop_unit  -- 商店单位
    local item = data.item  -- 道具
end)
```

---

## 商店-商品变化

event in Game

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | shop_unit | Unit | 商店单位 |
    | tab_idx | integer | 商店分页 |
    | shop_key | string | 商品id |
    | curr_stock | integer | 当前库存 |

- 示例

```lua
y3.game:event('商店-商品变化', function(trg, data)
    local shop_unit = data.shop_unit  -- 商店单位
    local tab_idx = data.tab_idx  -- 商店分页
    local shop_key = data.shop_key  -- 商品id
    local curr_stock = data.curr_stock  -- 当前库存
end)
```

---

## 商店-库存变化

event in Game

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | shop_unit | Unit | 商店单位 |
    | tab_idx | integer | 商店分页 |
    | shop_key | string | 商品id |
    | curr_stock | integer | 当前库存 |

- 示例

```lua
y3.game:event('商店-库存变化', function(trg, data)
    local shop_unit = data.shop_unit  -- 商店单位
    local tab_idx = data.tab_idx  -- 商店分页
    local shop_key = data.shop_key  -- 商品id
    local curr_stock = data.curr_stock  -- 当前库存
end)
```

---

## 商店-售价变化

event in Game

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | shop_unit | Unit | 商店单位 |
    | tab_idx | integer | 商店分页 |
    | shop_key | string | 商品id |
    | res_type | py.RoleResKey | 资源编号 |
    | res_cost | integer | 当前售价 |

- 示例

```lua
y3.game:event('商店-售价变化', function(trg, data)
    local shop_unit = data.shop_unit  -- 商店单位
    local tab_idx = data.tab_idx  -- 商店分页
    local shop_key = data.shop_key  -- 商品id
    local res_type = data.res_type  -- 资源编号
    local res_cost = data.res_cost  -- 当前售价
end)
```

---

## 单位-物品合成

event in Unit

- 描述

    物品合成时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 单位 |
    | compose_id | py.ItemKey | 道具编号 |
    | item_prop | Item | 道具 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-物品合成', function(trg, data)
    local unit = data.unit  -- 单位
    local compose_id = data.compose_id  -- 道具编号
    local item_prop = data.item_prop  -- 道具
end)
```

---

## 单位-购买物品合成

event in Unit

- 描述

    购买物品合成时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 购买物品单位 |
    | shop_unit | Unit | 商店单位 |
    | item | Item | 物品编号 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-购买物品合成', function(trg, data)
    local unit = data.unit  -- 购买物品单位
    local shop_unit = data.shop_unit  -- 商店单位
    local item = data.item  -- 物品编号
end)
```

---

## 单位-复活

event in Unit

- 描述

    单位复活后触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-复活', function(trg, data)
    local unit = data.unit
end)
```

---

## 单位-升级

event in Unit

- 描述

    单位升级后触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit |  |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-升级', function(trg, data)
    local unit = data.unit
end)
```

---

## 单位-进入草丛

event in Unit

- 描述

    单位进入草丛时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 单位 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-进入草丛', function(trg, data)
    local unit = data.unit  -- 单位
end)
```

---

## 单位-离开草丛

event in Unit

- 描述

    单位离开草丛时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 单位 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-离开草丛', function(trg, data)
    local unit = data.unit  -- 单位
end)
```

---

## 单位-改变所属

event in Unit

- 描述

    单位的所有者玩家发生变化时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 触发事件的单位 |
    | old_player | Player | 单位原所属玩家 |
    | new_player | Player | 单位新所属玩家 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-改变所属', function(trg, data)
    local unit = data.unit  -- 触发事件的单位
    local old_player = data.old_player  -- 单位原所属玩家
    local new_player = data.new_player  -- 单位新所属玩家
end)
```

---

## 单位类型-前置条件成立

event in Game

- 描述

    前置条件由不成立变为成立时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位类型 |
    | player | Player | 玩家 |

- 示例

```lua
y3.game:event('单位类型-前置条件成立', function(trg, data)
    local unit_key = data.unit_key  -- 单位类型
    local player = data.player  -- 玩家
end)
```

---

## 单位类型-前置条件不成立

event in Game

- 描述

    前置条件由成立变为不成立时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit_key | py.UnitKey | 单位类型 |
    | player | Player | 玩家 |

- 示例

```lua
y3.game:event('单位类型-前置条件不成立', function(trg, data)
    local unit_key = data.unit_key  -- 单位类型
    local player = data.player  -- 玩家
end)
```

---

## 物品类型-前置条件成立

event in Game

- 描述

    前置条件由不成立变为成立时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_no | py.ItemKey | 物品类型 |
    | player | Player | 玩家 |

- 示例

```lua
y3.game:event('物品类型-前置条件成立', function(trg, data)
    local item_no = data.item_no  -- 物品类型
    local player = data.player  -- 玩家
end)
```

---

## 物品类型-前置条件不成立

event in Game

- 描述

    前置条件由成立变为不成立时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item_no | py.ItemKey | 物品类型 |
    | player | Player | 玩家 |

- 示例

```lua
y3.game:event('物品类型-前置条件不成立', function(trg, data)
    local item_no = data.item_no  -- 物品类型
    local player = data.player  -- 玩家
end)
```

---

## 技能类型-前置条件成立

event in Game

- 描述

    前置条件由不成立变为成立时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_id | py.AbilityKey | 技能类型 |
    | player | Player | 玩家 |

- 示例

```lua
y3.game:event('技能类型-前置条件成立', function(trg, data)
    local ability_id = data.ability_id  -- 技能类型
    local player = data.player  -- 玩家
end)
```

---

## 技能类型-前置条件不成立

event in Game

- 描述

    前置条件由成立变为不成立时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability_id | py.AbilityKey | 技能类型 |
    | player | Player | 玩家 |

- 示例

```lua
y3.game:event('技能类型-前置条件不成立', function(trg, data)
    local ability_id = data.ability_id  -- 技能类型
    local player = data.player  -- 玩家
end)
```

---

## 科技类型-前置条件成立

event in Game

- 描述

    前置条件由不成立变为成立时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_no | py.TechKey | 科技类型 |
    | player | Player | 玩家 |

- 示例

```lua
y3.game:event('科技类型-前置条件成立', function(trg, data)
    local tech_no = data.tech_no  -- 科技类型
    local player = data.player  -- 玩家
end)
```

---

## 科技类型-前置条件不成立

event in Game

- 描述

    前置条件由成立变为不成立时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | tech_no | py.TechKey | 科技类型 |
    | player | Player | 玩家 |

- 示例

```lua
y3.game:event('科技类型-前置条件不成立', function(trg, data)
    local tech_no = data.tech_no  -- 科技类型
    local player = data.player  -- 玩家
end)
```

---

## 技能-升级

event in Ability

- 描述

    技能升级后触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability | Ability | 技能对象 |
    | unit | Unit | 技能Owner |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:event('技能-升级', function(trg, data)
    local ability = data.ability  -- 技能对象
    local unit = data.unit  -- 技能Owner
end)
```

---

## 施法-即将开始

event in Ability

- 描述

    即将施法时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability | Ability | 技能对象 |
    | unit | Unit | 技能Owner |
    | ability_target_unit | Unit | 技能目标单位 |
    | cast | Cast | 施法 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:event('施法-即将开始', function(trg, data)
    local ability = data.ability  -- 技能对象
    local unit = data.unit  -- 技能Owner
    local ability_target_unit = data.ability_target_unit  -- 技能目标单位
    local cast = data.cast  -- 施法
end)
```

---

## 施法-开始

event in Ability

- 描述

    施法开始后，前摇开始前触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability | Ability | 技能对象 |
    | unit | Unit | 技能Owner |
    | ability_target_unit | Unit | 技能目标单位 |
    | cast | Cast | 施法 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:event('施法-开始', function(trg, data)
    local ability = data.ability  -- 技能对象
    local unit = data.unit  -- 技能Owner
    local ability_target_unit = data.ability_target_unit  -- 技能目标单位
    local cast = data.cast  -- 施法
end)
```

---

## 施法-引导

event in Ability

- 描述

    前摇完成后，持续引导前触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability | Ability | 技能对象 |
    | unit | Unit | 技能Owner |
    | ability_target_unit | Unit | 技能目标单位 |
    | cast | Cast | 施法 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:event('施法-引导', function(trg, data)
    local ability = data.ability  -- 技能对象
    local unit = data.unit  -- 技能Owner
    local ability_target_unit = data.ability_target_unit  -- 技能目标单位
    local cast = data.cast  -- 施法
end)
```

---

## 施法-出手

event in Ability

- 描述

    持续引导后，后摇开始前触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability | Ability | 技能对象 |
    | unit | Unit | 技能Owner |
    | ability_target_unit | Unit | 技能目标单位 |
    | cast | Cast | 施法 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:event('施法-出手', function(trg, data)
    local ability = data.ability  -- 技能对象
    local unit = data.unit  -- 技能Owner
    local ability_target_unit = data.ability_target_unit  -- 技能目标单位
    local cast = data.cast  -- 施法
end)
```

---

## 施法-完成

event in Ability

- 描述

    后摇结束后触发。只有施法正常完成才会触发。

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability | Ability | 技能对象 |
    | unit | Unit | 技能Owner |
    | ability_target_unit | Unit | 技能目标单位 |
    | cast | Cast | 施法 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:event('施法-完成', function(trg, data)
    local ability = data.ability  -- 技能对象
    local unit = data.unit  -- 技能Owner
    local ability_target_unit = data.ability_target_unit  -- 技能目标单位
    local cast = data.cast  -- 施法
end)
```

---

## 施法-结束

event in Ability

- 描述

    整个施法的表现结束后触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability | Ability | 技能对象 |
    | unit | Unit | 技能Owner |
    | ability_target_unit | Unit | 技能目标单位 |
    | cast | Cast | 施法 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:event('施法-结束', function(trg, data)
    local ability = data.ability  -- 技能对象
    local unit = data.unit  -- 技能Owner
    local ability_target_unit = data.ability_target_unit  -- 技能目标单位
    local cast = data.cast  -- 施法
end)
```

---

## 施法-打断开始

event in Ability

- 描述

    在“开始”到“引导”之间被打断

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability | Ability | 技能对象 |
    | unit | Unit | 技能Owner |
    | ability_target_unit | Unit | 技能目标单位 |
    | cast | Cast | 施法 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:event('施法-打断开始', function(trg, data)
    local ability = data.ability  -- 技能对象
    local unit = data.unit  -- 技能Owner
    local ability_target_unit = data.ability_target_unit  -- 技能目标单位
    local cast = data.cast  -- 施法
end)
```

---

## 施法-打断引导

event in Ability

- 描述

    在“引导”到“出手”之间被打断

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability | Ability | 技能对象 |
    | unit | Unit | 技能Owner |
    | ability_target_unit | Unit | 技能目标单位 |
    | cast | Cast | 施法 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:event('施法-打断引导', function(trg, data)
    local ability = data.ability  -- 技能对象
    local unit = data.unit  -- 技能Owner
    local ability_target_unit = data.ability_target_unit  -- 技能目标单位
    local cast = data.cast  -- 施法
end)
```

---

## 施法-打断出手

event in Ability

- 描述

    在“出手”到“完成”之间被打断

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability | Ability | 技能对象 |
    | unit | Unit | 技能Owner |
    | ability_target_unit | Unit | 技能目标单位 |
    | cast | Cast | 施法 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:event('施法-打断出手', function(trg, data)
    local ability = data.ability  -- 技能对象
    local unit = data.unit  -- 技能Owner
    local ability_target_unit = data.ability_target_unit  -- 技能目标单位
    local cast = data.cast  -- 施法
end)
```

---

## 施法-停止

event in Ability

- 描述

    施法停止后触发，是施法流程的最后一个事件。

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability | Ability | 技能对象 |
    | unit | Unit | 技能Owner |
    | ability_target_unit | Unit | 技能目标单位 |
    | cast | Cast | 施法 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:event('施法-停止', function(trg, data)
    local ability = data.ability  -- 技能对象
    local unit = data.unit  -- 技能Owner
    local ability_target_unit = data.ability_target_unit  -- 技能目标单位
    local cast = data.cast  -- 施法
end)
```

---

## 技能-获得

event in Ability

- 描述

    获得技能后触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability | Ability | 技能对象 |
    | unit | Unit | 单位 |
    | lua_table | py.Table | 用户自定义配置表 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:event('技能-获得', function(trg, data)
    local ability = data.ability  -- 技能对象
    local unit = data.unit  -- 单位
    local lua_table = data.lua_table  -- 用户自定义配置表
end)
```

---

## 技能-失去

event in Ability

- 描述

    失去技能后触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability | Ability | 技能对象 |
    | unit | Unit | 单位 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:event('技能-失去', function(trg, data)
    local ability = data.ability  -- 技能对象
    local unit = data.unit  -- 单位
end)
```

---

## 技能-交换

event in Ability

- 描述

    技能交换后触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability | Ability | 技能对象 |
    | unit | Unit | 技能Owner |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:event('技能-交换', function(trg, data)
    local ability = data.ability  -- 技能对象
    local unit = data.unit  -- 技能Owner
end)
```

---

## 技能-禁用

event in Ability

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability | Ability | 技能对象 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:event('技能-禁用', function(trg, data)
    local ability = data.ability  -- 技能对象
end)
```

---

## 技能-启用

event in Ability

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability | Ability | 技能对象 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:event('技能-启用', function(trg, data)
    local ability = data.ability  -- 技能对象
end)
```

---

## 技能-冷却结束

event in Ability

- 描述

    技能冷却结束后触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability | Ability | 技能对象 |
    | unit | Unit | 技能Owner |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:event('技能-冷却结束', function(trg, data)
    local ability = data.ability  -- 技能对象
    local unit = data.unit  -- 技能Owner
end)
```

---

## 技能-自定义动画轴

event in Ability

- 描述

    无

- 注册参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | string | string | CUE事件名 |

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ability | Ability | 技能对象 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:event('技能-自定义动画轴', "string", function(trg, data)
    local ability = data.ability  -- 技能对象
end)
```

---

## 效果-获得

event in Buff

- 描述

    获得魔法效果后触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | buff | Buff | 触发的魔法效果 |
    | owner_unit | Unit | 效果携带者 |
    | from_unit | Unit | 效果施加者 |
    | lua_table | py.Table | 用户自定义配置表 |

- 示例

```lua
y3.game:event('效果-获得', function(trg, data)
    local buff = data.buff  -- 触发的魔法效果
    local owner_unit = data.owner_unit  -- 效果携带者
    local from_unit = data.from_unit  -- 效果施加者
    local lua_table = data.lua_table  -- 用户自定义配置表
end)
```

---

## 效果-失去

event in Buff

- 描述

    失去魔法效果后触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | buff | Buff | 触发的魔法效果 |
    | owner_unit | Unit | 效果携带者 |
    | from_unit | Unit | 效果施加者 |
    | lua_table | py.Table | 用户自定义配置表 |

- 示例

```lua
y3.game:event('效果-失去', function(trg, data)
    local buff = data.buff  -- 触发的魔法效果
    local owner_unit = data.owner_unit  -- 效果携带者
    local from_unit = data.from_unit  -- 效果施加者
    local lua_table = data.lua_table  -- 用户自定义配置表
end)
```

---

## 效果-心跳

event in Buff

- 描述

    魔法效果的周期性触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | buff | Buff | 触发的魔法效果 |
    | owner_unit | Unit | 效果携带者 |
    | from_unit | Unit | 效果施加者 |
    | lua_table | py.Table | 用户自定义配置表 |

- 示例

```lua
y3.game:event('效果-心跳', function(trg, data)
    local buff = data.buff  -- 触发的魔法效果
    local owner_unit = data.owner_unit  -- 效果携带者
    local from_unit = data.from_unit  -- 效果施加者
    local lua_table = data.lua_table  -- 用户自定义配置表
end)
```

---

## 效果-叠加

event in Buff

- 描述

    魔法效果叠加时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | buff | Buff | 触发的魔法效果 |
    | owner_unit | Unit | 效果携带者 |
    | from_unit | Unit | 效果施加者 |
    | lua_table | py.Table | 用户自定义配置表 |

- 示例

```lua
y3.game:event('效果-叠加', function(trg, data)
    local buff = data.buff  -- 触发的魔法效果
    local owner_unit = data.owner_unit  -- 效果携带者
    local from_unit = data.from_unit  -- 效果施加者
    local lua_table = data.lua_table  -- 用户自定义配置表
end)
```

---

## 效果-层数变化

event in Buff

- 描述

    魔法效果层数变化时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | buff | Buff | 触发的魔法效果 |
    | owner_unit | Unit | 效果携带者 |
    | layer_change_values | integer | 层数变化值 |
    | from_unit | Unit | 效果施加者 |
    | lua_table | py.Table | 用户自定义配置表 |

- 示例

```lua
y3.game:event('效果-层数变化', function(trg, data)
    local buff = data.buff  -- 触发的魔法效果
    local owner_unit = data.owner_unit  -- 效果携带者
    local layer_change_values = data.layer_change_values  -- 层数变化值
    local from_unit = data.from_unit  -- 效果施加者
    local lua_table = data.lua_table  -- 用户自定义配置表
end)
```

---

## 效果-即将获得

event in Buff

- 描述

    魔法效果获得前触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | buff | Buff | 触发的魔法效果 |
    | owner_unit | Unit | 效果携带者 |
    | from_unit | Unit | 效果施加者 |
    | lua_table | py.Table | 用户自定义配置表 |

- 示例

```lua
y3.game:event('效果-即将获得', function(trg, data)
    local buff = data.buff  -- 触发的魔法效果
    local owner_unit = data.owner_unit  -- 效果携带者
    local from_unit = data.from_unit  -- 效果施加者
    local lua_table = data.lua_table  -- 用户自定义配置表
end)
```

---

## 效果-覆盖

event in Buff

- 描述

    魔法效果覆盖时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | owner_unit | Unit | 效果携带者 |
    | old_buff | Buff | 已有的魔法效果 |
    | new_buff | Buff | 新增的魔法效果 |
    | lua_table | py.Table | 用户自定义配置表 |

- 示例

```lua
y3.game:event('效果-覆盖', function(trg, data)
    local owner_unit = data.owner_unit  -- 效果携带者
    local old_buff = data.old_buff  -- 已有的魔法效果
    local new_buff = data.new_buff  -- 新增的魔法效果
    local lua_table = data.lua_table  -- 用户自定义配置表
end)
```

---

## 可破坏物-创建

event in Destructible

- 描述

    可破坏物创建后触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible | Destructible | 可破坏物 |
    | lua_table | py.Table | 用户自定义配置表 |

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)

destructible:event('可破坏物-创建', function(trg, data)
    local destructible = data.destructible  -- 可破坏物
    local lua_table = data.lua_table  -- 用户自定义配置表
end)
```

---

## 可破坏物-死亡

event in Destructible

- 描述

    可破坏物死亡后触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible | Destructible | 可破坏物 |
    | unit_id_of_dest_killer | Unit | 凶手单位ID |

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)

destructible:event('可破坏物-死亡', function(trg, data)
    local destructible = data.destructible  -- 可破坏物
    local unit_id_of_dest_killer = data.unit_id_of_dest_killer  -- 凶手单位ID
end)
```

---

## 可破坏物-复活

event in Destructible

- 描述

    可破坏物复活后触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible | Destructible | 可破坏物 |

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)

destructible:event('可破坏物-复活', function(trg, data)
    local destructible = data.destructible  -- 可破坏物
end)
```

---

## 可破坏物-资源变化

event in Destructible

- 描述

    可破坏物存储的资源变化后触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible | Destructible | 可破坏物 |
    | res_chg_cnt_in_dest_event | integer | 可破坏物资源变化量 |

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)

destructible:event('可破坏物-资源变化', function(trg, data)
    local destructible = data.destructible  -- 可破坏物
    local res_chg_cnt_in_dest_event = data.res_chg_cnt_in_dest_event  -- 可破坏物资源变化量
end)
```

---

## 可破坏物-采集

event in Destructible

- 描述

    可破坏物被采集后触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible | Destructible | 可破坏物 |
    | unit_id_in_dest_event | Unit | 事件中的单位 |
    | ability_in_dest_event | Ability | 事件中的技能对象 |
    | player_res_cnt_in_event | integer | 采集的玩家属性个数 |

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)

destructible:event('可破坏物-采集', function(trg, data)
    local destructible = data.destructible  -- 可破坏物
    local unit_id_in_dest_event = data.unit_id_in_dest_event  -- 事件中的单位
    local ability_in_dest_event = data.ability_in_dest_event  -- 事件中的技能对象
    local player_res_cnt_in_event = data.player_res_cnt_in_event  -- 采集的玩家属性个数
end)
```

---

## 可破坏物-受到伤害

event in Destructible

- 描述

    可破坏物受到伤害后触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible | Destructible | 可破坏物 |
    | unit_id_of_hurt_dest | Unit | 事件中的单位 |
    | damage_value_of_hurt_dest | number | 受到的伤害 |

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)

destructible:event('可破坏物-受到伤害', function(trg, data)
    local destructible = data.destructible  -- 可破坏物
    local unit_id_of_hurt_dest = data.unit_id_of_hurt_dest  -- 事件中的单位
    local damage_value_of_hurt_dest = data.damage_value_of_hurt_dest  -- 受到的伤害
end)
```

---

## 选中-可破坏物

event in Player

- 描述

    玩家选中可破坏物被后触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | destructible | Destructible | 点击到可破坏物 |

- 示例

```lua
local player = y3.player.get_by_id(1)

player:event('选中-可破坏物', function(trg, data)
    local player = data.player  -- 玩家
    local destructible = data.destructible  -- 点击到可破坏物
end)
```

---

## 本地-选中-可破坏物

event in Player

- 描述

    本地玩家选中可破坏物被后触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | destructible | Destructible | 点击到可破坏物 |

- 示例

```lua
local player = y3.player.get_by_id(1)

player:event('本地-选中-可破坏物', function(trg, data)
    local player = data.player  -- 玩家
    local destructible = data.destructible  -- 点击到可破坏物
end)
```

---

## 可破坏物-移除

event in Destructible

- 描述

    可破坏物被移除后触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | destructible | Destructible | 触发事件的可破坏物 |

- 示例

```lua
local destructible = y3.destructible.get_by_id(1)

destructible:event('可破坏物-移除', function(trg, data)
    local destructible = data.destructible  -- 触发事件的可破坏物
end)
```

---

## 投射物-创建

event in Projectile

- 描述

    投射物创建后触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile | Projectile | 投射物 |

- 示例

```lua
-- 需要先创建或获取投射物对象
projectile:event('投射物-创建', function(trg, data)
    local projectile = data.projectile  -- 投射物
end)
```

---

## 投射物-死亡

event in Projectile

- 描述

    投射物死亡后触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | projectile | Projectile | 投射物 |

- 示例

```lua
-- 需要先创建或获取投射物对象
projectile:event('投射物-死亡', function(trg, data)
    local projectile = data.projectile  -- 投射物
end)
```

---

## 界面-消息

event in Game / Player

- 描述

    触发界面上标记的自定义事件后触发

- 注册参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | event_name | string | 自定义事件名称 |

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | ui_event_name | string | ui事件变量名 |
    | comp_name | string | 触发事件控件名称 |
    | pos | py.Vector2 | 触碰坐标 |
    | touch_id | integer | 触碰ID |
    | str1 | string | 自定义信息 |
    | ui | UI | ui |
    | data | any | 自定义数据 |

- 示例

```lua
-- 方式1: 通过 y3.game 注册（监听所有玩家）
y3.game:event('界面-消息', "event_name", function(trg, data)
    local player = data.player  -- 玩家
    local ui_event_name = data.ui_event_name  -- ui事件变量名
    local comp_name = data.comp_name  -- 触发事件控件名称
    local pos = data.pos  -- 触碰坐标
    local touch_id = data.touch_id  -- 触碰ID
    local str1 = data.str1  -- 自定义信息
    local ui = data.ui  -- ui
    local data = data.data  -- 自定义数据
end)

-- 方式2: 通过 Player 对象注册（监听特定对象）
local player = y3.player.get_by_id(1)

player:event('界面-消息', "event_name", function(trg, data)
    local player = data.player  -- 玩家
    local ui_event_name = data.ui_event_name  -- ui事件变量名
    local comp_name = data.comp_name  -- 触发事件控件名称
    local pos = data.pos  -- 触碰坐标
    local touch_id = data.touch_id  -- 触碰ID
    local str1 = data.str1  -- 自定义信息
    local ui = data.ui  -- ui
    local data = data.data  -- 自定义数据
end)
```

---

## 玩家-点击小地图

event in Game / Player

- 描述

    点击小地图时触发

- 注册参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | y3.Const.ClickMiniMapKey|integer | 按下的键 |

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | mini_map_touched_world_pos | Point | 点击对应的世界坐标 |

- 示例

```lua
-- 方式1: 通过 y3.game 注册（监听所有玩家）
y3.game:event('玩家-点击小地图', 1, function(trg, data)
    local player = data.player  -- 玩家
    local mini_map_touched_world_pos = data.mini_map_touched_world_pos  -- 点击对应的世界坐标
end)

-- 方式2: 通过 Player 对象注册（监听特定对象）
local player = y3.player.get_by_id(1)

player:event('玩家-点击小地图', 1, function(trg, data)
    local player = data.player  -- 玩家
    local mini_map_touched_world_pos = data.mini_map_touched_world_pos  -- 点击对应的世界坐标
end)
```

---

## 界面-滑动条变化

event in Game / Player

- 描述

    滑动条变化时触发

- 注册参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ui | UI | 目标控件 |

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | ui_event_name | string | ui事件变量名 |
    | comp_name | string | 触发事件控件名称 |
    | float1 | number | 自定义信息 |
    | ui | UI | ui |

- 示例

```lua
-- 方式1: 通过 y3.game 注册（监听所有玩家）
y3.game:event('界面-滑动条变化', ui, function(trg, data)
    local player = data.player  -- 玩家
    local ui_event_name = data.ui_event_name  -- ui事件变量名
    local comp_name = data.comp_name  -- 触发事件控件名称
    local float1 = data.float1  -- 自定义信息
    local ui = data.ui  -- ui
end)

-- 方式2: 通过 Player 对象注册（监听特定对象）
local player = y3.player.get_by_id(1)

player:event('界面-滑动条变化', ui, function(trg, data)
    local player = data.player  -- 玩家
    local ui_event_name = data.ui_event_name  -- ui事件变量名
    local comp_name = data.comp_name  -- 触发事件控件名称
    local float1 = data.float1  -- 自定义信息
    local ui = data.ui  -- ui
end)
```

---

## 界面-聊天框可见性变化

event in Game / Player

- 描述

    聊天框可见性变化时触发

- 注册参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ui | UI | 目标控件 |

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | ui_event_name | string | ui事件变量名 |
    | comp_name | string | 触发事件控件名称 |
    | bool1 | boolean | 自定义信息 |
    | ui | UI | ui |

- 示例

```lua
-- 方式1: 通过 y3.game 注册（监听所有玩家）
y3.game:event('界面-聊天框可见性变化', ui, function(trg, data)
    local player = data.player  -- 玩家
    local ui_event_name = data.ui_event_name  -- ui事件变量名
    local comp_name = data.comp_name  -- 触发事件控件名称
    local bool1 = data.bool1  -- 自定义信息
    local ui = data.ui  -- ui
end)

-- 方式2: 通过 Player 对象注册（监听特定对象）
local player = y3.player.get_by_id(1)

player:event('界面-聊天框可见性变化', ui, function(trg, data)
    local player = data.player  -- 玩家
    local ui_event_name = data.ui_event_name  -- ui事件变量名
    local comp_name = data.comp_name  -- 触发事件控件名称
    local bool1 = data.bool1  -- 自定义信息
    local ui = data.ui  -- ui
end)
```

---

## 界面-装备拖拽

event in Game / Player

- 描述

    无

- 注册参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ui | UI | 目标控件 |

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ui_event_name | string | 事件名 |
    | player | Player | 玩家 |
    | equip_slot_id | integer | 槽位索引 |
    | equip_slot_type | integer | 物品栏类型 |
    | equip_slot_item | Item | 物品 |
    | equip_slot_unit | Unit | 单位 |
    | equip_slot_is_begin | boolean | 是否拖拽开始 |
    | ui | UI | ui |

- 示例

```lua
-- 方式1: 通过 y3.game 注册（监听所有玩家）
y3.game:event('界面-装备拖拽', ui, function(trg, data)
    local ui_event_name = data.ui_event_name  -- 事件名
    local player = data.player  -- 玩家
    local equip_slot_id = data.equip_slot_id  -- 槽位索引
    local equip_slot_type = data.equip_slot_type  -- 物品栏类型
    local equip_slot_item = data.equip_slot_item  -- 物品
    local equip_slot_unit = data.equip_slot_unit  -- 单位
    local equip_slot_is_begin = data.equip_slot_is_begin  -- 是否拖拽开始
    local ui = data.ui  -- ui
end)

-- 方式2: 通过 Player 对象注册（监听特定对象）
local player = y3.player.get_by_id(1)

player:event('界面-装备拖拽', ui, function(trg, data)
    local ui_event_name = data.ui_event_name  -- 事件名
    local player = data.player  -- 玩家
    local equip_slot_id = data.equip_slot_id  -- 槽位索引
    local equip_slot_type = data.equip_slot_type  -- 物品栏类型
    local equip_slot_item = data.equip_slot_item  -- 物品
    local equip_slot_unit = data.equip_slot_unit  -- 单位
    local equip_slot_is_begin = data.equip_slot_is_begin  -- 是否拖拽开始
    local ui = data.ui  -- ui
end)
```

---

## 界面-复选框变化

event in Game / Player

- 描述

    复选框变化时触发

- 注册参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ui | UI | 目标控件 |

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | ui_event_name | string | ui事件变量名 |
    | comp_name | string | 触发事件控件名称 |
    | bool1 | boolean | 自定义信息 |
    | ui | UI | ui |

- 示例

```lua
-- 方式1: 通过 y3.game 注册（监听所有玩家）
y3.game:event('界面-复选框变化', ui, function(trg, data)
    local player = data.player  -- 玩家
    local ui_event_name = data.ui_event_name  -- ui事件变量名
    local comp_name = data.comp_name  -- 触发事件控件名称
    local bool1 = data.bool1  -- 自定义信息
    local ui = data.ui  -- ui
end)

-- 方式2: 通过 Player 对象注册（监听特定对象）
local player = y3.player.get_by_id(1)

player:event('界面-复选框变化', ui, function(trg, data)
    local player = data.player  -- 玩家
    local ui_event_name = data.ui_event_name  -- ui事件变量名
    local comp_name = data.comp_name  -- 触发事件控件名称
    local bool1 = data.bool1  -- 自定义信息
    local ui = data.ui  -- ui
end)
```

---

## 界面-视频播放完成

event in Game / Player

- 描述

    无

- 注册参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ui | UI | 目标控件 |

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | ui_event_name | string | ui事件变量名 |
    | comp_name | string | 触发事件控件名称 |
    | str1 | string | 自定义信息 |
    | ui | UI | ui |

- 示例

```lua
-- 方式1: 通过 y3.game 注册（监听所有玩家）
y3.game:event('界面-视频播放完成', ui, function(trg, data)
    local player = data.player  -- 玩家
    local ui_event_name = data.ui_event_name  -- ui事件变量名
    local comp_name = data.comp_name  -- 触发事件控件名称
    local str1 = data.str1  -- 自定义信息
    local ui = data.ui  -- ui
end)

-- 方式2: 通过 Player 对象注册（监听特定对象）
local player = y3.player.get_by_id(1)

player:event('界面-视频播放完成', ui, function(trg, data)
    local player = data.player  -- 玩家
    local ui_event_name = data.ui_event_name  -- ui事件变量名
    local comp_name = data.comp_name  -- 触发事件控件名称
    local str1 = data.str1  -- 自定义信息
    local ui = data.ui  -- ui
end)
```

---

## 本地-界面-输入框获取焦点

event in Game / Player

- 描述

    无

- 注册参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ui | UI | 输入框控件 |

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | ui_event_name | string | ui事件变量名 |
    | comp_name | string | 触发事件控件名称 |
    | ui | UI | ui |

- 示例

```lua
-- 方式1: 通过 y3.game 注册（监听所有玩家）
y3.game:event('本地-界面-输入框获取焦点', ui, function(trg, data)
    local player = data.player  -- 玩家
    local ui_event_name = data.ui_event_name  -- ui事件变量名
    local comp_name = data.comp_name  -- 触发事件控件名称
    local ui = data.ui  -- ui
end)

-- 方式2: 通过 Player 对象注册（监听特定对象）
local player = y3.player.get_by_id(1)

player:event('本地-界面-输入框获取焦点', ui, function(trg, data)
    local player = data.player  -- 玩家
    local ui_event_name = data.ui_event_name  -- ui事件变量名
    local comp_name = data.comp_name  -- 触发事件控件名称
    local ui = data.ui  -- ui
end)
```

---

## 本地-界面-输入框失去焦点

event in Game / Player

- 描述

    无

- 注册参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ui | UI | 输入框控件 |

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | ui_event_name | string | ui事件变量名 |
    | comp_name | string | 触发事件控件名称 |
    | ui | UI | ui |

- 示例

```lua
-- 方式1: 通过 y3.game 注册（监听所有玩家）
y3.game:event('本地-界面-输入框失去焦点', ui, function(trg, data)
    local player = data.player  -- 玩家
    local ui_event_name = data.ui_event_name  -- ui事件变量名
    local comp_name = data.comp_name  -- 触发事件控件名称
    local ui = data.ui  -- ui
end)

-- 方式2: 通过 Player 对象注册（监听特定对象）
local player = y3.player.get_by_id(1)

player:event('本地-界面-输入框失去焦点', ui, function(trg, data)
    local player = data.player  -- 玩家
    local ui_event_name = data.ui_event_name  -- ui事件变量名
    local comp_name = data.comp_name  -- 触发事件控件名称
    local ui = data.ui  -- ui
end)
```

---

## 本地-界面-输入框内容改变

event in Game / Player

- 描述

    无

- 注册参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | ui | UI | 输入框控件 |

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | ui_event_name | string | ui事件变量名 |
    | comp_name | string | 触发事件控件名称 |
    | str1 | string | 文本内容 |
    | ui | UI | ui |

- 示例

```lua
-- 方式1: 通过 y3.game 注册（监听所有玩家）
y3.game:event('本地-界面-输入框内容改变', ui, function(trg, data)
    local player = data.player  -- 玩家
    local ui_event_name = data.ui_event_name  -- ui事件变量名
    local comp_name = data.comp_name  -- 触发事件控件名称
    local str1 = data.str1  -- 文本内容
    local ui = data.ui  -- ui
end)

-- 方式2: 通过 Player 对象注册（监听特定对象）
local player = y3.player.get_by_id(1)

player:event('本地-界面-输入框内容改变', ui, function(trg, data)
    local player = data.player  -- 玩家
    local ui_event_name = data.ui_event_name  -- ui事件变量名
    local comp_name = data.comp_name  -- 触发事件控件名称
    local str1 = data.str1  -- 文本内容
    local ui = data.ui  -- ui
end)
```

---

## 键盘-按下

event in Game / Player

- 描述

    键盘上的某个键按下时触发

- 注册参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | y3.Const.KeyboardKey|integer | 按下的键 |

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 触发按键的玩家 |
    | current_key | py.KeyboardKey | 当前键盘按键 |

- 示例

```lua
-- 方式1: 通过 y3.game 注册（监听所有玩家）
y3.game:event('键盘-按下', 'M', function(trg, data)
    local player = data.player  -- 触发按键的玩家
    local current_key = data.current_key  -- 当前键盘按键
end)

-- 方式2: 通过 Player 对象注册（监听特定对象）
local player = y3.player.get_by_id(1)

player:event('键盘-按下', 'M', function(trg, data)
    local player = data.player  -- 触发按键的玩家
    local current_key = data.current_key  -- 当前键盘按键
end)
```

---

## 键盘-抬起

event in Game / Player

- 描述

    键盘上的某个键抬起时触发

- 注册参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | y3.Const.KeyboardKey|integer | 抬起的键 |

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 触发按键的玩家 |
    | current_key | py.KeyboardKey | 当前键盘按键 |

- 示例

```lua
-- 方式1: 通过 y3.game 注册（监听所有玩家）
y3.game:event('键盘-抬起', 'M', function(trg, data)
    local player = data.player  -- 触发按键的玩家
    local current_key = data.current_key  -- 当前键盘按键
end)

-- 方式2: 通过 Player 对象注册（监听特定对象）
local player = y3.player.get_by_id(1)

player:event('键盘-抬起', 'M', function(trg, data)
    local player = data.player  -- 触发按键的玩家
    local current_key = data.current_key  -- 当前键盘按键
end)
```

---

## 本地-键盘-按下

event in Game / Player

- 描述

    键盘上的某个键按下时触发

- 注册参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | y3.Const.KeyboardKey|integer | 按下的键 |

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 触发按键的玩家 |
    | current_key | py.KeyboardKey | 当前键盘按键 |

- 示例

```lua
-- 方式1: 通过 y3.game 注册（监听所有玩家）
y3.game:event('本地-键盘-按下', 'M', function(trg, data)
    local player = data.player  -- 触发按键的玩家
    local current_key = data.current_key  -- 当前键盘按键
end)

-- 方式2: 通过 Player 对象注册（监听特定对象）
local player = y3.player.get_by_id(1)

player:event('本地-键盘-按下', 'M', function(trg, data)
    local player = data.player  -- 触发按键的玩家
    local current_key = data.current_key  -- 当前键盘按键
end)
```

---

## 本地-键盘-抬起

event in Game / Player

- 描述

    键盘上的某个键抬起时触发

- 注册参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | y3.Const.KeyboardKey|integer | 抬起的键 |

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 触发按键的玩家 |
    | current_key | py.KeyboardKey | 当前键盘按键 |

- 示例

```lua
-- 方式1: 通过 y3.game 注册（监听所有玩家）
y3.game:event('本地-键盘-抬起', 'M', function(trg, data)
    local player = data.player  -- 触发按键的玩家
    local current_key = data.current_key  -- 当前键盘按键
end)

-- 方式2: 通过 Player 对象注册（监听特定对象）
local player = y3.player.get_by_id(1)

player:event('本地-键盘-抬起', 'M', function(trg, data)
    local player = data.player  -- 触发按键的玩家
    local current_key = data.current_key  -- 当前键盘按键
end)
```

---

## 鼠标-按下

event in Game / Player

- 描述

    鼠标上的某个键按下时触发

- 注册参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | y3.Const.MouseKey|integer | 按下的键 |

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 触发按键的玩家 |
    | current_key | py.MouseKey | 当前鼠标按键 |
    | pointing_world_pos | Point | 鼠标指向的世界坐标 |
    | is_click_swallowed_by_ui | boolean | 点击事件是否被UI吞噬 |

- 示例

```lua
-- 方式1: 通过 y3.game 注册（监听所有玩家）
y3.game:event('鼠标-按下', 0, function(trg, data)
    local player = data.player  -- 触发按键的玩家
    local current_key = data.current_key  -- 当前鼠标按键
    local pointing_world_pos = data.pointing_world_pos  -- 鼠标指向的世界坐标
    local is_click_swallowed_by_ui = data.is_click_swallowed_by_ui  -- 点击事件是否被UI吞噬
end)

-- 方式2: 通过 Player 对象注册（监听特定对象）
local player = y3.player.get_by_id(1)

player:event('鼠标-按下', 0, function(trg, data)
    local player = data.player  -- 触发按键的玩家
    local current_key = data.current_key  -- 当前鼠标按键
    local pointing_world_pos = data.pointing_world_pos  -- 鼠标指向的世界坐标
    local is_click_swallowed_by_ui = data.is_click_swallowed_by_ui  -- 点击事件是否被UI吞噬
end)
```

---

## 鼠标-抬起

event in Game / Player

- 描述

    鼠标上的某个键抬起时触发

- 注册参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | y3.Const.MouseKey|integer | 抬起的键 |

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 触发按键的玩家 |
    | current_key | py.MouseKey | 当前鼠标按键 |
    | pointing_world_pos | Point | 鼠标指向的世界坐标 |

- 示例

```lua
-- 方式1: 通过 y3.game 注册（监听所有玩家）
y3.game:event('鼠标-抬起', 0, function(trg, data)
    local player = data.player  -- 触发按键的玩家
    local current_key = data.current_key  -- 当前鼠标按键
    local pointing_world_pos = data.pointing_world_pos  -- 鼠标指向的世界坐标
end)

-- 方式2: 通过 Player 对象注册（监听特定对象）
local player = y3.player.get_by_id(1)

player:event('鼠标-抬起', 0, function(trg, data)
    local player = data.player  -- 触发按键的玩家
    local current_key = data.current_key  -- 当前鼠标按键
    local pointing_world_pos = data.pointing_world_pos  -- 鼠标指向的世界坐标
end)
```

---

## 鼠标-双击

event in Game / Player

- 描述

    鼠标上的某个键双击时触发

- 注册参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | y3.Const.MouseKey|integer | 双击的键 |

- 事件参数 (data)

    无

- 示例

```lua
-- 方式1: 通过 y3.game 注册（监听所有玩家）
y3.game:event('鼠标-双击', 0, function(trg, data)
    -- 无事件参数
end)

-- 方式2: 通过 Player 对象注册（监听特定对象）
local player = y3.player.get_by_id(1)

player:event('鼠标-双击', 0, function(trg, data)
    -- 无事件参数
end)
```

---

## 本地-鼠标-按下

event in Game / Player

- 描述

    鼠标上的某个键按下时触发

- 注册参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | y3.Const.MouseKey|integer | 按下的键 |

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 触发按键的玩家 |
    | current_key | py.MouseKey | 当前鼠标按键 |
    | pointing_world_pos | Point | 鼠标指向的世界坐标 |
    | is_click_swallowed_by_ui | boolean | 点击事件是否被UI吞噬 |

- 示例

```lua
-- 方式1: 通过 y3.game 注册（监听所有玩家）
y3.game:event('本地-鼠标-按下', 0, function(trg, data)
    local player = data.player  -- 触发按键的玩家
    local current_key = data.current_key  -- 当前鼠标按键
    local pointing_world_pos = data.pointing_world_pos  -- 鼠标指向的世界坐标
    local is_click_swallowed_by_ui = data.is_click_swallowed_by_ui  -- 点击事件是否被UI吞噬
end)

-- 方式2: 通过 Player 对象注册（监听特定对象）
local player = y3.player.get_by_id(1)

player:event('本地-鼠标-按下', 0, function(trg, data)
    local player = data.player  -- 触发按键的玩家
    local current_key = data.current_key  -- 当前鼠标按键
    local pointing_world_pos = data.pointing_world_pos  -- 鼠标指向的世界坐标
    local is_click_swallowed_by_ui = data.is_click_swallowed_by_ui  -- 点击事件是否被UI吞噬
end)
```

---

## 本地-鼠标-抬起

event in Game / Player

- 描述

    鼠标上的某个键抬起时触发

- 注册参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | y3.Const.MouseKey|integer | 抬起的键 |

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 触发按键的玩家 |
    | current_key | py.MouseKey | 当前鼠标按键 |
    | pointing_world_pos | Point | 鼠标指向的世界坐标 |

- 示例

```lua
-- 方式1: 通过 y3.game 注册（监听所有玩家）
y3.game:event('本地-鼠标-抬起', 0, function(trg, data)
    local player = data.player  -- 触发按键的玩家
    local current_key = data.current_key  -- 当前鼠标按键
    local pointing_world_pos = data.pointing_world_pos  -- 鼠标指向的世界坐标
end)

-- 方式2: 通过 Player 对象注册（监听特定对象）
local player = y3.player.get_by_id(1)

player:event('本地-鼠标-抬起', 0, function(trg, data)
    local player = data.player  -- 触发按键的玩家
    local current_key = data.current_key  -- 当前鼠标按键
    local pointing_world_pos = data.pointing_world_pos  -- 鼠标指向的世界坐标
end)
```

---

## 本地-鼠标-双击

event in Game / Player

- 描述

    鼠标上的某个键双击时触发

- 注册参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | y3.Const.MouseKey|integer | 双击的键 |

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 触发按键的玩家 |
    | current_key | py.MouseKey | 当前鼠标按键 |
    | pointing_world_pos | Point | 鼠标指向的世界坐标 |

- 示例

```lua
-- 方式1: 通过 y3.game 注册（监听所有玩家）
y3.game:event('本地-鼠标-双击', 0, function(trg, data)
    local player = data.player  -- 触发按键的玩家
    local current_key = data.current_key  -- 当前鼠标按键
    local pointing_world_pos = data.pointing_world_pos  -- 鼠标指向的世界坐标
end)

-- 方式2: 通过 Player 对象注册（监听特定对象）
local player = y3.player.get_by_id(1)

player:event('本地-鼠标-双击', 0, function(trg, data)
    local player = data.player  -- 触发按键的玩家
    local current_key = data.current_key  -- 当前鼠标按键
    local pointing_world_pos = data.pointing_world_pos  -- 鼠标指向的世界坐标
end)
```

---

## 鼠标-按下单位

event in Game / Player

- 描述

    鼠标上的某个键对着单位按下时触发

- 注册参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | y3.Const.MouseKey|integer | 按下的键 |

- 事件参数 (data)

    无

- 示例

```lua
-- 方式1: 通过 y3.game 注册（监听所有玩家）
y3.game:event('鼠标-按下单位', 0, function(trg, data)
    -- 无事件参数
end)

-- 方式2: 通过 Player 对象注册（监听特定对象）
local player = y3.player.get_by_id(1)

player:event('鼠标-按下单位', 0, function(trg, data)
    -- 无事件参数
end)
```

---

## 鼠标-抬起单位

event in Game / Player

- 描述

    鼠标上的某个键对着单位抬起时触发

- 注册参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | y3.Const.MouseKey|integer | 抬起的键 |

- 事件参数 (data)

    无

- 示例

```lua
-- 方式1: 通过 y3.game 注册（监听所有玩家）
y3.game:event('鼠标-抬起单位', 0, function(trg, data)
    -- 无事件参数
end)

-- 方式2: 通过 Player 对象注册（监听特定对象）
local player = y3.player.get_by_id(1)

player:event('鼠标-抬起单位', 0, function(trg, data)
    -- 无事件参数
end)
```

---

## 鼠标-双击单位

event in Game / Player

- 描述

    鼠标上的某个键对着单位双击时触发

- 注册参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | y3.Const.MouseKey|integer | 双击的键 |

- 事件参数 (data)

    无

- 示例

```lua
-- 方式1: 通过 y3.game 注册（监听所有玩家）
y3.game:event('鼠标-双击单位', 0, function(trg, data)
    -- 无事件参数
end)

-- 方式2: 通过 Player 对象注册（监听特定对象）
local player = y3.player.get_by_id(1)

player:event('鼠标-双击单位', 0, function(trg, data)
    -- 无事件参数
end)
```

---

## 本地-鼠标-按下单位

event in Game / Player

- 描述

    鼠标上的某个键对着单位按下时触发

- 注册参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | y3.Const.MouseKey|integer | 按下的键 |

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 触发按键的玩家 |
    | current_key | py.MouseKey | 当前鼠标按键 |
    | unit | Unit | 当前操作的单位 |

- 示例

```lua
-- 方式1: 通过 y3.game 注册（监听所有玩家）
y3.game:event('本地-鼠标-按下单位', 0, function(trg, data)
    local player = data.player  -- 触发按键的玩家
    local current_key = data.current_key  -- 当前鼠标按键
    local unit = data.unit  -- 当前操作的单位
end)

-- 方式2: 通过 Player 对象注册（监听特定对象）
local player = y3.player.get_by_id(1)

player:event('本地-鼠标-按下单位', 0, function(trg, data)
    local player = data.player  -- 触发按键的玩家
    local current_key = data.current_key  -- 当前鼠标按键
    local unit = data.unit  -- 当前操作的单位
end)
```

---

## 本地-鼠标-抬起单位

event in Game / Player

- 描述

    鼠标上的某个键对着单位抬起时触发

- 注册参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | y3.Const.MouseKey|integer | 抬起的键 |

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 触发按键的玩家 |
    | current_key | py.MouseKey | 当前鼠标按键 |
    | unit | Unit | 当前操作的单位 |

- 示例

```lua
-- 方式1: 通过 y3.game 注册（监听所有玩家）
y3.game:event('本地-鼠标-抬起单位', 0, function(trg, data)
    local player = data.player  -- 触发按键的玩家
    local current_key = data.current_key  -- 当前鼠标按键
    local unit = data.unit  -- 当前操作的单位
end)

-- 方式2: 通过 Player 对象注册（监听特定对象）
local player = y3.player.get_by_id(1)

player:event('本地-鼠标-抬起单位', 0, function(trg, data)
    local player = data.player  -- 触发按键的玩家
    local current_key = data.current_key  -- 当前鼠标按键
    local unit = data.unit  -- 当前操作的单位
end)
```

---

## 本地-鼠标-双击单位

event in Game / Player

- 描述

    鼠标上的某个键对着单位双击时触发

- 注册参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | y3.Const.MouseKey|integer | 双击的键 |

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 触发按键的玩家 |
    | current_key | py.MouseKey | 当前鼠标按键 |
    | unit | Unit | 当前操作的单位 |

- 示例

```lua
-- 方式1: 通过 y3.game 注册（监听所有玩家）
y3.game:event('本地-鼠标-双击单位', 0, function(trg, data)
    local player = data.player  -- 触发按键的玩家
    local current_key = data.current_key  -- 当前鼠标按键
    local unit = data.unit  -- 当前操作的单位
end)

-- 方式2: 通过 Player 对象注册（监听特定对象）
local player = y3.player.get_by_id(1)

player:event('本地-鼠标-双击单位', 0, function(trg, data)
    local player = data.player  -- 触发按键的玩家
    local current_key = data.current_key  -- 当前鼠标按键
    local unit = data.unit  -- 当前操作的单位
end)
```

---

## 鼠标-移动

event in Game / Player

- 描述

    鼠标移动时触发

- 注册参数

    无

- 事件参数 (data)

    无

- 示例

```lua
-- 方式1: 通过 y3.game 注册（监听所有玩家）
y3.game:event('鼠标-移动', function(trg, data)
    -- 无事件参数
end)

-- 方式2: 通过 Player 对象注册（监听特定对象）
local player = y3.player.get_by_id(1)

player:event('鼠标-移动', function(trg, data)
    -- 无事件参数
end)
```

---

## 本地-鼠标-移动

event in Game / Player

- 描述

    鼠标移动时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 触发按键的玩家 |
    | pointing_world_pos | Point | 鼠标指向的世界坐标 |
    | tar_x | integer | 鼠标指向的屏幕坐标X |
    | tar_y | integer | 鼠标指向的屏幕坐标Y |

- 示例

```lua
-- 方式1: 通过 y3.game 注册（监听所有玩家）
y3.game:event('本地-鼠标-移动', function(trg, data)
    local player = data.player  -- 触发按键的玩家
    local pointing_world_pos = data.pointing_world_pos  -- 鼠标指向的世界坐标
    local tar_x = data.tar_x  -- 鼠标指向的屏幕坐标X
    local tar_y = data.tar_y  -- 鼠标指向的屏幕坐标Y
end)

-- 方式2: 通过 Player 对象注册（监听特定对象）
local player = y3.player.get_by_id(1)

player:event('本地-鼠标-移动', function(trg, data)
    local player = data.player  -- 触发按键的玩家
    local pointing_world_pos = data.pointing_world_pos  -- 鼠标指向的世界坐标
    local tar_x = data.tar_x  -- 鼠标指向的屏幕坐标X
    local tar_y = data.tar_y  -- 鼠标指向的屏幕坐标Y
end)
```

---

## 鼠标-滚轮

event in Game / Player

- 描述

    鼠标滚轮滚动时触发

- 注册参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | y3.Const.MouseKey|integer | 滚动方向 |

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 触发按键的玩家 |
    | mouse_wheel | py.MouseWheel | 当前鼠标滚轮 |

- 示例

```lua
-- 方式1: 通过 y3.game 注册（监听所有玩家）
y3.game:event('鼠标-滚轮', 0, function(trg, data)
    local player = data.player  -- 触发按键的玩家
    local mouse_wheel = data.mouse_wheel  -- 当前鼠标滚轮
end)

-- 方式2: 通过 Player 对象注册（监听特定对象）
local player = y3.player.get_by_id(1)

player:event('鼠标-滚轮', 0, function(trg, data)
    local player = data.player  -- 触发按键的玩家
    local mouse_wheel = data.mouse_wheel  -- 当前鼠标滚轮
end)
```

---

## 本地-鼠标-滚轮

event in Game / Player

- 描述

    鼠标滚轮滚动时触发

- 注册参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | key | y3.Const.MouseKey|integer | 滚动方向 |

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 触发按键的玩家 |
    | mouse_wheel | py.MouseWheel | 当前鼠标滚轮 |

- 示例

```lua
-- 方式1: 通过 y3.game 注册（监听所有玩家）
y3.game:event('本地-鼠标-滚轮', 0, function(trg, data)
    local player = data.player  -- 触发按键的玩家
    local mouse_wheel = data.mouse_wheel  -- 当前鼠标滚轮
end)

-- 方式2: 通过 Player 对象注册（监听特定对象）
local player = y3.player.get_by_id(1)

player:event('本地-鼠标-滚轮', 0, function(trg, data)
    local player = data.player  -- 触发按键的玩家
    local mouse_wheel = data.mouse_wheel  -- 当前鼠标滚轮
end)
```

---

## 选中-单位

event in Player

- 描述

    玩家选中单位时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | unit | Unit | 点击到单位 |

- 示例

```lua
local player = y3.player.get_by_id(1)

player:event('选中-单位', function(trg, data)
    local player = data.player  -- 玩家
    local unit = data.unit  -- 点击到单位
end)
```

---

## 本地-选中-单位

event in Player

- 描述

    本地玩家选中单位时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | unit | Unit | 点击的单位 |

- 示例

```lua
local player = y3.player.get_by_id(1)

player:event('本地-选中-单位', function(trg, data)
    local player = data.player  -- 玩家
    local unit = data.unit  -- 点击的单位
end)
```

---

## 选中-取消

event in Player

- 描述

    玩家主动取消选中时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |

- 示例

```lua
local player = y3.player.get_by_id(1)

player:event('选中-取消', function(trg, data)
    local player = data.player  -- 玩家
end)
```

---

## 本地-选中-取消

event in Player

- 描述

    玩家的选中状态被取消时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |

- 示例

```lua
local player = y3.player.get_by_id(1)

player:event('本地-选中-取消', function(trg, data)
    local player = data.player  -- 玩家
end)
```

---

## 选中-失去单位

event in Player

- 描述

    玩家被动失去对单位的选中状态时触发

- 注册参数

    无

- 事件参数 (data)

    无

- 示例

```lua
local player = y3.player.get_by_id(1)

player:event('选中-失去单位', function(trg, data)
    -- 无事件参数
end)
```

---

## 本地-选中-失去单位

event in Player

- 描述

    本地玩家被动失去对单位的选中状态时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | unit | Unit | 点击到单位 |

- 示例

```lua
local player = y3.player.get_by_id(1)

player:event('本地-选中-失去单位', function(trg, data)
    local player = data.player  -- 玩家
    local unit = data.unit  -- 点击到单位
end)
```

---

## 选中-物品

event in Player

- 描述

    物品被选中时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | item | Item | 点击到物品 |

- 示例

```lua
local player = y3.player.get_by_id(1)

player:event('选中-物品', function(trg, data)
    local player = data.player  -- 玩家
    local item = data.item  -- 点击到物品
end)
```

---

## 本地-选中-物品

event in Player

- 描述

    本地玩家选中物品时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | item | Item | 点击到物品 |

- 示例

```lua
local player = y3.player.get_by_id(1)

player:event('本地-选中-物品', function(trg, data)
    local player = data.player  -- 玩家
    local item = data.item  -- 点击到物品
end)
```

---

## 玩家-检测到作弊

event in Player

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 作弊玩家 |
    | unit | Unit | 作弊单位 |
    | attr_key | string | 作弊属性名 |
    | cheating_value | number | 作弊值 |
    | real_value | number | 真实值 |

- 示例

```lua
local player = y3.player.get_by_id(1)

player:event('玩家-检测到作弊', function(trg, data)
    local player = data.player  -- 作弊玩家
    local unit = data.unit  -- 作弊单位
    local attr_key = data.attr_key  -- 作弊属性名
    local cheating_value = data.cheating_value  -- 作弊值
    local real_value = data.real_value  -- 真实值
end)
```

---

## 鼠标-双击物品

event in Game / Player

- 描述

    鼠标上左键双击物品时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | item | Item | 双击到物品 |

- 示例

```lua
-- 方式1: 通过 y3.game 注册（监听所有玩家）
y3.game:event('鼠标-双击物品', function(trg, data)
    local player = data.player  -- 玩家
    local item = data.item  -- 双击到物品
end)

-- 方式2: 通过 Player 对象注册（监听特定对象）
local player = y3.player.get_by_id(1)

player:event('鼠标-双击物品', function(trg, data)
    local player = data.player  -- 玩家
    local item = data.item  -- 双击到物品
end)
```

---

## 鼠标-双击可破坏物

event in Game / Player

- 描述

    鼠标上左键双击可破坏物时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | destructible | Destructible | 双击到可破坏物 |

- 示例

```lua
-- 方式1: 通过 y3.game 注册（监听所有玩家）
y3.game:event('鼠标-双击可破坏物', function(trg, data)
    local player = data.player  -- 玩家
    local destructible = data.destructible  -- 双击到可破坏物
end)

-- 方式2: 通过 Player 对象注册（监听特定对象）
local player = y3.player.get_by_id(1)

player:event('鼠标-双击可破坏物', function(trg, data)
    local player = data.player  -- 玩家
    local destructible = data.destructible  -- 双击到可破坏物
end)
```

---

## 选中-单位组

event in Player

- 描述

    玩家选中单位组时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | unit_group_id_list | UnitGroup | 框选到单位组id列表 |
    | team_id | integer | 队伍编号 |

- 示例

```lua
local player = y3.player.get_by_id(1)

player:event('选中-单位组', function(trg, data)
    local player = data.player  -- 玩家
    local unit_group_id_list = data.unit_group_id_list  -- 框选到单位组id列表
    local team_id = data.team_id  -- 队伍编号
end)
```

---

## 本地-选中-单位组

event in Player

- 描述

    本地玩家选中单位组时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | unit_group_id_list | UnitGroup | 框选到单位组id列表 |
    | team_id | integer | 队伍编号 |

- 示例

```lua
local player = y3.player.get_by_id(1)

player:event('本地-选中-单位组', function(trg, data)
    local player = data.player  -- 玩家
    local unit_group_id_list = data.unit_group_id_list  -- 框选到单位组id列表
    local team_id = data.team_id  -- 队伍编号
end)
```

---

## 技能-打开指示器

event in Ability

- 描述

    技能的瞄准指示器显示时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | unit | Unit | 释放单位 |
    | ability_type | py.AbilityType | 技能类型 |
    | ability_index | py.AbilityIndex | 技能Index |
    | ability_seq | py.AbilitySeq | 技能Seq |
    | ability | Ability | 技能 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:event('技能-打开指示器', function(trg, data)
    local player = data.player  -- 玩家
    local unit = data.unit  -- 释放单位
    local ability_type = data.ability_type  -- 技能类型
    local ability_index = data.ability_index  -- 技能Index
    local ability_seq = data.ability_seq  -- 技能Seq
    local ability = data.ability  -- 技能
end)
```

---

## 技能-建造技能释放前

event in Ability

- 描述

    建造技能的命令将要发布时

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | unit | Unit | 释放单位 |
    | ability_seq | py.AbilitySeq | 技能Seq |
    | ability | Ability | 技能 |
    | new_unit_key | py.UnitKey | 要建造单位的物编ID |
    | ability_target_pos | Point | 施法目标位置 |
    | ability_release_id | py.AbilityReleaseId | 单次技能释放唯一ID |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:event('技能-建造技能释放前', function(trg, data)
    local player = data.player  -- 玩家
    local unit = data.unit  -- 释放单位
    local ability_seq = data.ability_seq  -- 技能Seq
    local ability = data.ability  -- 技能
    local new_unit_key = data.new_unit_key  -- 要建造单位的物编ID
    local ability_target_pos = data.ability_target_pos  -- 施法目标位置
    local ability_release_id = data.ability_release_id  -- 单次技能释放唯一ID
end)
```

---

## 技能-关闭指示器

event in Ability

- 描述

    技能的瞄准指示器消失时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | unit | Unit | 释放单位 |
    | ability_type | py.AbilityType | 技能类型 |
    | ability_index | py.AbilityIndex | 技能Index |
    | ability_seq | py.AbilitySeq | 技能Seq |
    | ability | Ability | 技能 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local ability = unit:get_ability_by_slot(y3.const.AbilityType.HERO, 0)

ability:event('技能-关闭指示器', function(trg, data)
    local player = data.player  -- 玩家
    local unit = data.unit  -- 释放单位
    local ability_type = data.ability_type  -- 技能类型
    local ability_index = data.ability_index  -- 技能Index
    local ability_seq = data.ability_seq  -- 技能Seq
    local ability = data.ability  -- 技能
end)
```

---

## 物品-获得

event in Item

- 描述

    单位获得物品时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 获得该物品的单位 |
    | item | Item | 物品 |
    | item_no | py.ItemKey | 物品编号 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item:event('物品-获得', function(trg, data)
    local unit = data.unit  -- 获得该物品的单位
    local item = data.item  -- 物品
    local item_no = data.item_no  -- 物品编号
end)
```

---

## 物品-进入物品栏

event in Item

- 描述

    物品进入单位的物品栏时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 获得该物品的单位 |
    | item | Item | 物品 |
    | item_no | py.ItemKey | 物品编号 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item:event('物品-进入物品栏', function(trg, data)
    local unit = data.unit  -- 获得该物品的单位
    local item = data.item  -- 物品
    local item_no = data.item_no  -- 物品编号
end)
```

---

## 物品-进入背包

event in Item

- 描述

    物品进入单位的背包时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 获得该物品的单位 |
    | item | Item | 物品 |
    | item_no | py.ItemKey | 物品编号 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item:event('物品-进入背包', function(trg, data)
    local unit = data.unit  -- 获得该物品的单位
    local item = data.item  -- 物品
    local item_no = data.item_no  -- 物品编号
end)
```

---

## 物品-失去

event in Item

- 描述

    单位失去物品时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 失去该物品的单位 |
    | item | Item | 物品 |
    | item_no | py.ItemKey | 物品编号 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item:event('物品-失去', function(trg, data)
    local unit = data.unit  -- 失去该物品的单位
    local item = data.item  -- 物品
    local item_no = data.item_no  -- 物品编号
end)
```

---

## 物品-离开物品栏

event in Item

- 描述

    物品离开单位的物品栏时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 失去该物品的单位 |
    | item | Item | 物品 |
    | item_no | py.ItemKey | 物品编号 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item:event('物品-离开物品栏', function(trg, data)
    local unit = data.unit  -- 失去该物品的单位
    local item = data.item  -- 物品
    local item_no = data.item_no  -- 物品编号
end)
```

---

## 物品-离开背包

event in Item

- 描述

    物品离开单位的背包时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 失去该物品的单位 |
    | item | Item | 物品 |
    | item_no | py.ItemKey | 物品编号 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item:event('物品-离开背包', function(trg, data)
    local unit = data.unit  -- 失去该物品的单位
    local item = data.item  -- 物品
    local item_no = data.item_no  -- 物品编号
end)
```

---

## 物品-使用

event in Item

- 描述

    单位使用物品时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 使用该物品的单位 |
    | item | Item | 物品 |
    | item_no | py.ItemKey | 物品编号 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item:event('物品-使用', function(trg, data)
    local unit = data.unit  -- 使用该物品的单位
    local item = data.item  -- 物品
    local item_no = data.item_no  -- 物品编号
end)
```

---

## 单位-寻路开始

event in Unit

- 描述

    攻击、移动、施法等行为均可能导致寻路

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 单位 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-寻路开始', function(trg, data)
    local unit = data.unit  -- 单位
end)
```

---

## 单位-寻路结束

event in Unit

- 描述

    寻路到达目标位置或失败3次后触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 单位 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('单位-寻路结束', function(trg, data)
    local unit = data.unit  -- 单位
end)
```

---

## 物品-堆叠变化

event in Item

- 描述

    物品堆叠数变化时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 单位 |
    | item | Item | 物品 |
    | item_no | py.ItemKey | 物品编号 |
    | delta_cnt | integer | 变化值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item:event('物品-堆叠变化', function(trg, data)
    local unit = data.unit  -- 单位
    local item = data.item  -- 物品
    local item_no = data.item_no  -- 物品编号
    local delta_cnt = data.delta_cnt  -- 变化值
end)
```

---

## 物品-充能变化

event in Item

- 描述

    物品充能层数变化时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 单位 |
    | item | Item | 物品 |
    | item_no | py.ItemKey | 物品编号 |
    | delta_cnt | integer | 变化值 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item:event('物品-充能变化', function(trg, data)
    local unit = data.unit  -- 单位
    local item = data.item  -- 物品
    local item_no = data.item_no  -- 物品编号
    local delta_cnt = data.delta_cnt  -- 变化值
end)
```

---

## 物品-创建

event in Item

- 描述

    物品创建时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item | Item | 被创建的物品 |
    | lua_table | py.Table | 用户自定义配置表 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item:event('物品-创建', function(trg, data)
    local item = data.item  -- 被创建的物品
    local lua_table = data.lua_table  -- 用户自定义配置表
end)
```

---

## 物品-移除

event in Item

- 描述

    物品移除时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item | Item | 销毁的物品 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item:event('物品-移除', function(trg, data)
    local item = data.item  -- 销毁的物品
end)
```

---

## 物品-出售

event in Item

- 描述

    将物品出售给商店时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 购买者 |
    | unit2 | Unit | 贩卖者 |
    | item | Item | 被售出的物品 |
    | buy_unit | Unit | 收购物品的单位 |
    | shop_unit | Unit | 出售物品的单位 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item:event('物品-出售', function(trg, data)
    local unit = data.unit  -- 购买者
    local unit2 = data.unit2  -- 贩卖者
    local item = data.item  -- 被售出的物品
    local buy_unit = data.buy_unit  -- 收购物品的单位
    local shop_unit = data.shop_unit  -- 出售物品的单位
end)
```

---

## 物品-死亡

event in Item

- 描述

    物品被破坏时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item | Item | 被破坏的物品 |
    | unit | Unit | 破坏物品的单位 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item:event('物品-死亡', function(trg, data)
    local item = data.item  -- 被破坏的物品
    local unit = data.unit  -- 破坏物品的单位
end)
```

---

## 物品-采集创建

event in Item

- 描述

    物品通过采集被创建时会触发该事件。采集功能来自可破坏物。

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | item | Item | 事件中的物品 |
    | destructible | Destructible | 事件中的可破坏物 |
    | unit | Unit | 采集可破坏物事件中的单位 |
    | ability | Ability | 采集可破坏物的捷能 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]
local item = unit:get_item_by_slot(y3.const.SlotType.BAR, 0)

item:event('物品-采集创建', function(trg, data)
    local item = data.item  -- 事件中的物品
    local destructible = data.destructible  -- 事件中的可破坏物
    local unit = data.unit  -- 采集可破坏物事件中的单位
    local ability = data.ability  -- 采集可破坏物的捷能
end)
```

---

## 命令-攻击移动

event in Unit

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 指定单位 |
    | tar_x | number | 点击位置X坐标 |
    | tar_y | number | 点击位置Y坐标 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('命令-攻击移动', function(trg, data)
    local unit = data.unit  -- 指定单位
    local tar_x = data.tar_x  -- 点击位置X坐标
    local tar_y = data.tar_y  -- 点击位置Y坐标
end)
```

---

## 命令-出售物品

event in Unit

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | shop_unit | Unit | 商店单位 |
    | item | Item | 商品 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('命令-出售物品', function(trg, data)
    local shop_unit = data.shop_unit  -- 商店单位
    local item = data.item  -- 商品
end)
```

---

## 命令-施放技能

event in Unit

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 指定单位 |
    | ability_type | py.AbilityType | 技能类型 |
    | ability_index | py.AbilityIndex | 技能Index |
    | ability_seq | py.AbilitySeq | 技能SEQ |
    | target_item | py.Dict | 释放技能参数 |
    | ability | Ability | 技能 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('命令-施放技能', function(trg, data)
    local unit = data.unit  -- 指定单位
    local ability_type = data.ability_type  -- 技能类型
    local ability_index = data.ability_index  -- 技能Index
    local ability_seq = data.ability_seq  -- 技能SEQ
    local target_item = data.target_item  -- 释放技能参数
    local ability = data.ability  -- 技能
end)
```

---

## 命令-巡逻

event in Unit

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 指定单位 |
    | tar_x | number | 点击位置X坐标 |
    | tar_y | number | 点击位置Y坐标 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('命令-巡逻', function(trg, data)
    local unit = data.unit  -- 指定单位
    local tar_x = data.tar_x  -- 点击位置X坐标
    local tar_y = data.tar_y  -- 点击位置Y坐标
end)
```

---

## 命令-移动

event in Unit

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | unit | Unit | 指定单位 |
    | tar_x | number | 点击位置X坐标 |
    | tar_y | number | 点击位置Y坐标 |

- 示例

```lua
local unit = y3.player.get_by_id(1):get_all_units()[1]

unit:event('命令-移动', function(trg, data)
    local unit = data.unit  -- 指定单位
    local tar_x = data.tar_x  -- 点击位置X坐标
    local tar_y = data.tar_y  -- 点击位置Y坐标
end)
```

---

## 鼠标-悬停

event in Game / Player

- 描述

    悬停进入或离开都会触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | unit | Unit | 悬浮单位 |
    | item | Item | 悬浮物品 |
    | destructible | Destructible | 悬浮可破坏物 |

- 示例

```lua
-- 方式1: 通过 y3.game 注册（监听所有玩家）
y3.game:event('鼠标-悬停', function(trg, data)
    local player = data.player  -- 玩家
    local unit = data.unit  -- 悬浮单位
    local item = data.item  -- 悬浮物品
    local destructible = data.destructible  -- 悬浮可破坏物
end)

-- 方式2: 通过 Player 对象注册（监听特定对象）
local player = y3.player.get_by_id(1)

player:event('鼠标-悬停', function(trg, data)
    local player = data.player  -- 玩家
    local unit = data.unit  -- 悬浮单位
    local item = data.item  -- 悬浮物品
    local destructible = data.destructible  -- 悬浮可破坏物
end)
```

---

## 本地-鼠标-悬停

event in Game / Player

- 描述

    悬停进入或离开都会触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | unit | Unit | 悬浮单位 |
    | item | Item | 悬浮物品 |
    | destructible | Destructible | 悬浮可破坏物 |

- 示例

```lua
-- 方式1: 通过 y3.game 注册（监听所有玩家）
y3.game:event('本地-鼠标-悬停', function(trg, data)
    local player = data.player  -- 玩家
    local unit = data.unit  -- 悬浮单位
    local item = data.item  -- 悬浮物品
    local destructible = data.destructible  -- 悬浮可破坏物
end)

-- 方式2: 通过 Player 对象注册（监听特定对象）
local player = y3.player.get_by_id(1)

player:event('本地-鼠标-悬停', function(trg, data)
    local player = data.player  -- 玩家
    local unit = data.unit  -- 悬浮单位
    local item = data.item  -- 悬浮物品
    local destructible = data.destructible  -- 悬浮可破坏物
end)
```

---

## 玩家-发送消息

event in Game / Player

- 描述

    玩家发送任意消息时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | str1 | string | 指令字符串 |
    | player | Player | 玩家 |

- 示例

```lua
-- 方式1: 通过 y3.game 注册（监听所有玩家）
y3.game:event('玩家-发送消息', function(trg, data)
    local str1 = data.str1  -- 指令字符串
    local player = data.player  -- 玩家
end)

-- 方式2: 通过 Player 对象注册（监听特定对象）
local player = y3.player.get_by_id(1)

player:event('玩家-发送消息', function(trg, data)
    local str1 = data.str1  -- 指令字符串
    local player = data.player  -- 玩家
end)
```

---

## 游戏-消息

event in Game

- 描述

    在事件管理处定义的事件通过这个方法进行触发

- 注册参数

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | event_id | integer | 事件ID |

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | c_param_1 | integer | 事件参数 |
    | c_param_dict | py.Dict | 自定义参数列表 |
    | data | table |  |
    | event | string |  |

- 示例

```lua
y3.game:event('游戏-消息', 1, function(trg, data)
    local c_param_1 = data.c_param_1  -- 事件参数
    local c_param_dict = data.c_param_dict  -- 自定义参数列表
    local data = data.data
    local event = data.event
end)
```

---

## 玩家-语音发言

event in Game / Player

- 描述

    玩家开始语音和结束语音都会触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | audio_channel | integer | 频道 |
    | audio_bool | boolean | 是否发言 |

- 示例

```lua
-- 方式1: 通过 y3.game 注册（监听所有玩家）
y3.game:event('玩家-语音发言', function(trg, data)
    local player = data.player  -- 玩家
    local audio_channel = data.audio_channel  -- 频道
    local audio_bool = data.audio_bool  -- 是否发言
end)

-- 方式2: 通过 Player 对象注册（监听特定对象）
local player = y3.player.get_by_id(1)

player:event('玩家-语音发言', function(trg, data)
    local player = data.player  -- 玩家
    local audio_channel = data.audio_channel  -- 频道
    local audio_bool = data.audio_bool  -- 是否发言
end)
```

---

## 玩家-平台道具变化

event in Player

- 描述

    玩家平台道具变化时触发

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | store_key | py.StoreKey | 道具编号 |
    | store_item_type | py.StoreItemType | 道具类型 |
    | store_item_change_count | integer | 平台道具变化数 |
    | store_item_expire_date | integer | 平台道具到期时间戳 |
    | player | Player | 玩家 |

- 示例

```lua
local player = y3.player.get_by_id(1)

player:event('玩家-平台道具变化', function(trg, data)
    local store_key = data.store_key  -- 道具编号
    local store_item_type = data.store_item_type  -- 道具类型
    local store_item_change_count = data.store_item_change_count  -- 平台道具变化数
    local store_item_expire_date = data.store_item_expire_date  -- 平台道具到期时间戳
    local player = data.player  -- 玩家
end)
```

---

## 玩家-平台商城窗口变化

event in Game / Player

- 描述

    平台商城窗口变化事件

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player | Player | 玩家 |
    | store_page_state | boolean | 商城界面状态 |

- 示例

```lua
-- 方式1: 通过 y3.game 注册（监听所有玩家）
y3.game:event('玩家-平台商城窗口变化', function(trg, data)
    local player = data.player  -- 玩家
    local store_page_state = data.store_page_state  -- 商城界面状态
end)

-- 方式2: 通过 Player 对象注册（监听特定对象）
local player = y3.player.get_by_id(1)

player:event('玩家-平台商城窗口变化', function(trg, data)
    local player = data.player  -- 玩家
    local store_page_state = data.store_page_state  -- 商城界面状态
end)
```

---

## 控制台-输入

event in Game

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | str1 | string | 指令字符串 |

- 示例

```lua
y3.game:event('控制台-输入', function(trg, data)
    local str1 = data.str1  -- 指令字符串
end)
```

---

## 控制台-请求补全

event in Game

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | str1 | string | 指令前缀 |

- 示例

```lua
y3.game:event('控制台-请求补全', function(trg, data)
    local str1 = data.str1  -- 指令前缀
end)
```

---

## steam-收到好友申请

event in Game

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | nick_name | string | 申请者名称 |

- 示例

```lua
y3.game:event('steam-收到好友申请', function(trg, data)
    local nick_name = data.nick_name  -- 申请者名称
end)
```

---

## steam-收到被好友删除

event in Game

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player_aid | integer | 删除者ID |

- 示例

```lua
y3.game:event('steam-收到被好友删除', function(trg, data)
    local player_aid = data.player_aid  -- 删除者ID
end)
```

---

## steam-好友在线状态变化

event in Game

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | online_state | y3.Const.SteamOnlineState | 好友在线状态 |
    | player_aid | integer | 好友ID |

- 示例

```lua
y3.game:event('steam-好友在线状态变化', function(trg, data)
    local online_state = data.online_state  -- 好友在线状态
    local player_aid = data.player_aid  -- 好友ID
end)
```

---

## steam-本地玩家队伍变化

event in Game

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    无

- 示例

```lua
y3.game:event('steam-本地玩家队伍变化', function(trg, data)
    -- 无事件参数
end)
```

---

## steam-收到队伍邀请

event in Game

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | player_aid | integer | 发送方ID |
    | nick_name | string | 发送方名称 |
    | team_id | integer | 队伍ID |

- 示例

```lua
y3.game:event('steam-收到队伍邀请', function(trg, data)
    local player_aid = data.player_aid  -- 发送方ID
    local nick_name = data.nick_name  -- 发送方名称
    local team_id = data.team_id  -- 队伍ID
end)
```

---

## steam-进入大厅

event in Game

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    无

- 示例

```lua
y3.game:event('steam-进入大厅', function(trg, data)
    -- 无事件参数
end)
```

---

## steam-开始匹配

event in Game

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    无

- 示例

```lua
y3.game:event('steam-开始匹配', function(trg, data)
    -- 无事件参数
end)
```

---

## steam-取消匹配

event in Game

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    无

- 示例

```lua
y3.game:event('steam-取消匹配', function(trg, data)
    -- 无事件参数
end)
```

---

## steam-本地房间信息变化

event in Game

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    无

- 示例

```lua
y3.game:event('steam-本地房间信息变化', function(trg, data)
    -- 无事件参数
end)
```

---

## steam-被邀请加入房间

event in Game

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    | 参数名 | 数据类型 | 说明 |
    | :--- | :--- | :--- |
    | room_id | integer | 房间号 |
    | player_aid | integer | 邀请人ID |
    | nick_name | string | 邀请人名称 |

- 示例

```lua
y3.game:event('steam-被邀请加入房间', function(trg, data)
    local room_id = data.room_id  -- 房间号
    local player_aid = data.player_aid  -- 邀请人ID
    local nick_name = data.nick_name  -- 邀请人名称
end)
```

---

## steam-被踢出房间

event in Game

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    无

- 示例

```lua
y3.game:event('steam-被踢出房间', function(trg, data)
    -- 无事件参数
end)
```

---

## steam-创建房间成功

event in Game

- 描述

    无

- 注册参数

    无

- 事件参数 (data)

    无

- 示例

```lua
y3.game:event('steam-创建房间成功', function(trg, data)
    -- 无事件参数
end)
```

---
