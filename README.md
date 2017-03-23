Game Base Framework
===

### 基本设计理念
1. 所有模块相互独立，都应该能作为插件导入
2. 保持轻量级，提供高扩展性，减少上层逻辑
3. 易用性强，上手速度快
4. 简化配置，开箱即用

###  模块划分

#### UI框架
1. UI基础框架
- 包含UI基类
- UI管理器
- 自动层级控制
- UI动画接口
- UI遮罩
- 对话框，Loading，Tips
- Loading界面集成
- UI热更新接口
- 场景切换动画
- 框架内消息系统
2. 编辑器工具：
- UI prefab生成编辑器工具，代码框架自动生成，枚举自动构建工具
- 排版布局工具
- 图片导入自动转换sprite
- 图集工具
- UI资源库，保存常用字体配置，颜色配置，按钮
- UI prefab管理工具
3. 通用UI空间
- 列表工具

#### 版本控制 & 资源管理
1. 资源加载
2. 版本管理
3. 资源热更新
4. 资源缓存
5. Assbundle打包工具
6. 资源服务器

#### 教程系统 & 剧情系统
1. 基础框架
 - 抽象段落，步骤，事件；
 - 事件触发
 - 触摸屏蔽，按钮绑定代码触发
 - 延时，步骤等待，防止网络通信异常
 - 阻塞处理
 - 支持全局的事件监听（即非步骤式的，而是达到某种状态之后触发，可能在游戏过程中任意状态）
 - 预留步骤保存接口，支持从固定段落开始
 - 脚本支持
 - 支持镜头动画；场景触发器接口；场景物体控制接口；
2. 编辑器
 - 段落，步骤，对话编辑器
3. 基本逻辑
- 创建数据流，指定每个步骤事件类型，UI类型，下一个步骤ID
- 绑定步骤完成回调
- 通过完成回调触发下一个步骤
- 附加：教程由多段组成，每段由多个步骤组成，保存只保存大段，未完成则从一段开始；

#### 通用功能
1. 音频音效管理器
2. 时间管理器
3. 全局管理器

