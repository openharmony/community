# sig_Gaming
简体中文 | [English](./sig_gaming.md)

说明：本SIG的内容遵循OpenHarmony的PMC管理章程 [README](../../zh/pmc.md)中描述的约定。

## SIG组工作目标和范围

### 工作目标
构建基于OHOS上的游戏应用程序迁移及开发能力。在OH上端到端拉通游戏相关技术，让游戏类应用高效，方便的在OH上运行。同时结合OH分布式能力，打造和提升游戏的分布式体验。


### 工作范围
- 从游戏业务逻辑、游戏引擎、OpenHarmony系统进行端到端拉通游戏相关技术，让游戏类应用高效，方便的在OH上运行。
- Cocos2d-x部件的演进和看护。
- GameController部件的演进和看护以及GameControllerAPI的评审。

技术栈范围全景图![OpenHarmony文档概览](figures/gaming_overview.png)


## 代码仓

| 部件名称          | 部件功能描述                                                                                                                                   | 部件路径名称                                                                                                       |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| Cocos2d-x     | Cocos2d-x 是一个用于构建2D游戏、互动书籍、演示程序及其他图形应用的多平台框架。它基于 cocos2d-iphone，但与后者不同，它使用的是C++而非Objective-C。该框架支持iOS、Android、OS X、Windows、Linux以及Web平台。 | [cocos2d-x](https://gitcode.com/openharmony-sig/cocos2dx/tree/cocos2d-x-3.17.2-ohos)                         |
| GameController| 给游戏开发者提供游戏外设接入能力的API，实现对游戏外设上下线监听和外设输入事件监听；<br/>提供InnerAPI给终端设备厂商，让终端设备厂商可以实现对游戏外设设备信息的管理以及对输入转触控的配置管理。                                  | [domains/game/game_controller_framework](https://gitcode.com/openharmony-sig/game_game_controller_framework) |

## SIG组成员

### Leader
- @zleoyu(https://gitee.com/zleoyu)

### Committers列表
- @honglianglin(https://gitee.com/honglianglin)
- @lz-230(https://gitee.com/lz-230)
- @He_r(https://gitee.com/He_r)
- @niu2x(https://gitee.com/niu2x)

### 会议
- 会议时间：双周周五14:30-15:15
- 会议申报：[OpenHarmony sig_Gaming Meeting Proposal](https://shimo.im/file-invite/6LUJkovmJuABaTcW8v8a9TpZAl9d6/)
- 会议链接: Welink
