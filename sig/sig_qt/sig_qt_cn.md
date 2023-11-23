# sig_Qt
简体中文 | [English](./sig_qt.md)

说明：本SIG的内容遵循OpenHarmony的PMC管理章程 [README](../../zh/pmc.md)中描述的约定。

## SIG组工作目标和范围

### 工作目标

Qt SIG负责完成在OpenHarmony的[Qt](https://qt.io)软件开发框架的移植及适配，实现基于Qt研发的应用迁移及OpenHarmony的研发生态补充，将适配OpenHarmony平台的Qt代码提交到Qt社区。

### 工作范围

Qt框架移植与适配计划贡献提供Qt版本为Qt5.12.12及Qt5.15.11。

Qt5.12.12版本适配贡献规划如下所示：
| 模块                     | 描述                                                         | 是否支持 |
| ------------------------ | ------------------------------------------------------------ | -------- |
| Qt Core                  | 非图形核心类，供其他模块使用。                               | 是       |
| Qt GUI                   | 提供图形用户界面（GUI）的基础类，包含OpenGL。                | 是       |
| Qt Multimedia            | 提供音频、视频、广播和摄像头功能。                           | 是       |
| Qt Multimedia Widgets    | 提供基于控件窗口的多媒体功能。                               | 是       |
| Qt Network               | 提供简化和便携的网络编程类。                                 | 是       |
| Qt QML                   | 用于处理QML和JavaScript的类。                                | 是       |
| Qt Quick                 | 声明性框架，用于构建动态的自定义用户界面。                   | 是       |
| Qt Quick Controls        | 提供轻量级QML类型，用于创建高性能用户界面。采用简单样式，效率高。 | 是       |
| Qt Quick Dialogs         | 提供从Qt Quick应用创建和交互的系统对话框类型。               | 是       |
| Qt Quick Layouts         | 用于在用户界面中排列基于Qt Quick 2的项目。                   | 是       |
| Qt Quick Test            | QML应用的单元测试框架，测试用例为JavaScript函数。            | 是       |
| Qt SQL                   | 提供数据库集成和使用SQL的类。                                | 是       |
| Qt Test                  | 提供对Qt应用和库的单元测试功能。                             | 是       |
| Qt Widgets               | 扩展Qt GUI的C++控件类。                                      | 是       |
| Active Qt                | 用于支持ActiveX和COM的应用程序。                             | 否       |
| Qt 3D                    | 支持2D和3D渲染的近实时仿真系统功能。                         | 是       |
| Qt Android Extras        | 提供Android特定的API。                                       | 否       |
| Qt Bluetooth             | 提供对蓝牙硬件的访问。                                       | 是       |
| Qt Canvas 3D             | 使Qt Quick应用使用JavaScript进行OpenGL样式的3D绘图。         | 否       |
| Qt Concurrent            | 提供编写多线程程序的类，无需使用低级线程原语。               | 是       |
| Qt D-Bus                 | 提供通过D-Bus协议进行进程间通信的类。                        | 否       |
| Qt Gamepad               | 支持使用游戏手柄硬件的Qt应用。                               | 否       |
| Qt Graphical Effects     | 提供与Qt Quick 2一起使用的图形效果。                         | 是       |
| Qt Help                  | 用于将文档集成到与Qt Assistant类似的应用中。                 | 是       |
| Qt Image Formats         | 提供其他图像格式的插件：TIFF、MNG、TGA、WBMP。               | 是       |
| Qt Location              | 在QML应用中显示地图、导航和地点内容。                        | 是       |
| Qt Mac Extras            | 提供macOS特定的API。                                         | 否       |
| Qt NFC                   | 提供对近场通信（NFC）硬件的访问。                            | 是       |
| Qt OpenGL                | 提供OpenGL支持类。                                           | 否       |
| Qt Platform Headers      | 提供与给定平台插件相关的特定信息的类。                       | 否       |
| Qt Positioning           | 提供位置、卫星和区域监控类的访问。                           | 是       |
| Qt Print Support         | 提供简化和便携的打印功能。                                   | 是       |
| Qt Purchasing            | 使Qt应用能够购买产品的功能。                                 | 否       |
| Qt Quick Controls 1      | 提供用于创建经典桌面风格UI的Qt Quick UI控件。                | 否       |
| Qt Quick Extras          | 提供一组专用控件，用于在Qt Quick中构建界面。                 | 是       |
| Qt Quick Widgets         | 提供一个C++控件窗口类，用于显示Qt Quick UI。                 | 是       |
| Qt Remote Objects        | 提供在进程或设备间共享QObject API的机制。                    | 是       |
| Qt Script                | 使Qt应用可脚本化的类。                                       | 否       |
| Qt SCXML                 | 提供从SCXML文件创建状态机并嵌入应用的类和工具。              | 是       |
| Qt Script Tools          | 提供用于调试Qt Script代码的类。                              | 否       |
| Qt Sensors               | 提供对硬件传感器的访问。                                     | 是       |
| Qt Serial Bus            | 提供对串行总线的访问。                                       | 是       |
| Qt Serial Port           | 提供对串行端口的访问。                                       | 是       |
| Qt Speech                | 提供支持文本转语音的功能。                                   | 否       |
| Qt SVG                   | 提供显示SVG文件的类。                                        | 是       |
| Qt UI Tools              | 提供处理UI文件的类。                                         | 是       |
| Qt WebChannel            | 提供从Web内容到Qt应用的双向通信。                            | 否       |
| Qt WebEngine             | 提供嵌入Web内容到Qt应用的类。                                | 否       |
| Qt WebSockets            | 提供创建WebSocket服务器和客户端的类。                        | 否       |
| Qt WebView               | 无需使用完整的Web堆栈将Web内容显示在QML应用程序中            | 否       |
| Qt Windows Extras        | 提供Windows特定的API。                                       | 否       |
| Qt X11 Extras            | 提供X11特定的API。                                           | 否       |
| Qt XML                   | 提供SAX和DOM风格API，用于读写XML文件。                       | 是       |
| Qt XML Patterns          | 提供查询和转换XML数据的类。                                  | 是       |
| Qt Wayland Compositor    | 提供构建Wayland合成器的类。                                  | 否       |
| Qt Charts                | 提供图表界面控件的类。                                       | 是       |
| Qt Data Visualization    | 创建3D数据可视化界面控件的类。                               | 是       |
| Qt Network Authorization | 提供支持基于OAuth的在线服务授权。                            | 否       |
| Qt Virtual Keyboard      | 提供Qt应用的虚拟键盘。                                       | 否       |
| Qt Quick WebGL           | 提供一个平台插件，允许使用WebGL™通过网络流式传输Qt Quick用户界面。 | 否       |

Qt5.15.11版本适配贡献规划如下所示（字体加粗模块为与5.12.12版本有差异模块）：
| 模块                     | 描述                                                         | 是否支持 |
| ------------------------ | ------------------------------------------------------------ | -------- |
| Qt Core                  | 非图形核心类，供其他模块使用。                               | 是       |
| Qt GUI                   | 提供图形用户界面（GUI）的基础类，包含OpenGL。                | 是       |
| Qt Multimedia            | 提供音频、视频、广播和摄像头功能。                           | 是       |
| Qt Multimedia Widgets    | 提供基于控件窗口的多媒体功能。                               | 是       |
| Qt Network               | 提供简化和便携的网络编程类。                                 | 是       |
| Qt QML                   | 用于处理QML和JavaScript的类。                                | 是       |
| Qt Quick                 | 声明性框架，用于构建动态的自定义用户界面。                   | 是       |
| Qt Quick Controls        | 提供轻量级QML类型，用于创建高性能用户界面。采用简单样式，效率高。 | 是       |
| Qt Quick Dialogs         | 提供从Qt Quick应用创建和交互的系统对话框类型。               | 是       |
| Qt Quick Layouts         | 用于在用户界面中排列基于Qt Quick 2的项目。                   | 是       |
| Qt Quick Test            | QML应用的单元测试框架，测试用例为JavaScript函数。            | 是       |
| Qt SQL                   | 提供数据库集成和使用SQL的类。                                | 是       |
| Qt Test                  | 提供对Qt应用和库的单元测试功能。                             | 是       |
| Qt Widgets               | 扩展Qt GUI的C++控件类。                                      | 是       |
| Active Qt                | 用于支持ActiveX和COM的应用程序。                             | 否       |
| Qt 3D                    | 支持2D和3D渲染的近实时仿真系统功能。                         | 是       |
| Qt Android Extras        | 提供Android特定的API。                                       | 否       |
| Qt Bluetooth             | 提供对蓝牙硬件的访问。                                       | 是       |
| Qt Canvas 3D             | 使Qt Quick应用使用JavaScript进行OpenGL样式的3D绘图。         | 否       |
| Qt Concurrent            | 提供编写多线程程序的类，无需使用低级线程原语。               | 是       |
| Qt D-Bus                 | 提供通过D-Bus协议进行进程间通信的类。                        | 否       |
| Qt Gamepad               | 支持使用游戏手柄硬件的Qt应用。                               | 否       |
| Qt Graphical Effects     | 提供与Qt Quick 2一起使用的图形效果。                         | 是       |
| Qt Help                  | 用于将文档集成到与Qt Assistant类似的应用中。                 | 是       |
| Qt Image Formats         | 提供其他图像格式的插件：TIFF、MNG、TGA、WBMP。               | 是       |
| Qt Location              | 在QML应用中显示地图、导航和地点内容。                        | 是       |
| Qt Mac Extras            | 提供macOS特定的API。                                         | 否       |
| Qt NFC                   | 提供对近场通信（NFC）硬件的访问。                            | 是       |
| Qt OpenGL                | 提供OpenGL支持类。                                           | 否       |
| **Qt PDF**               | **提供PDF显示及读取类。**                                    | **是**   |
| Qt Platform Headers      | 提供与给定平台插件相关的特定信息的类。                       | 否       |
| Qt Positioning           | 提供位置、卫星和区域监控类的访问。                           | 是       |
| Qt Print Support         | 提供简化和便携的打印功能。                                   | 是       |
| Qt Purchasing            | 使Qt应用能够购买产品的功能。                                 | 否       |
| Qt Quick Controls 1      | 提供用于创建经典桌面风格UI的Qt Quick UI控件。                | 否       |
| Qt Quick Extras          | 提供一组专用控件，用于在Qt Quick中构建界面。                 | 是       |
| Qt Quick Widgets         | 提供一个C++控件窗口类，用于显示Qt Quick UI。                 | 是       |
| Qt Remote Objects        | 提供在进程或设备间共享QObject API的机制。                    | 是       |
| Qt Script                | 使Qt应用可脚本化的类。                                       | 否       |
| Qt SCXML                 | 提供从SCXML文件创建状态机并嵌入应用的类和工具。              | 是       |
| Qt Script Tools          | 提供用于调试Qt Script代码的类。                              | 否       |
| Qt Sensors               | 提供对硬件传感器的访问。                                     | 是       |
| Qt Serial Bus            | 提供对串行总线的访问。                                       | 是       |
| Qt Serial Port           | 提供对串行端口的访问。                                       | 是       |
| Qt Speech                | 提供支持文本转语音的功能。                                   | 否       |
| Qt SVG                   | 提供显示SVG文件的类。                                        | 是       |
| Qt UI Tools              | 提供处理UI文件的类。                                         | 是       |
| Qt WebChannel            | 提供从Web内容到Qt应用的双向通信。                            | 否       |
| Qt WebEngine             | 提供嵌入Web内容到Qt应用的类。                                | 否       |
| Qt WebSockets            | 提供创建WebSocket服务器和客户端的类。                        | 否       |
| Qt WebView               | 无需使用完整的Web堆栈将Web内容显示在QML应用程序中            | 否       |
| Qt Windows Extras        | 提供Windows特定的API。                                       | 否       |
| Qt X11 Extras            | 提供X11特定的API。                                           | 否       |
| Qt XML                   | 提供SAX和DOM风格API，用于读写XML文件。                       | 是       |
| **Qt XML Patterns**      | **提供查询和转换XML数据的类。**                              | **否**   |
| Qt Wayland Compositor    | 提供构建Wayland合成器的类。                                  | 否       |
| Qt Charts                | 提供图表界面控件的类。                                       | 是       |
| Qt Data Visualization    | 创建3D数据可视化界面控件的类。                               | 是       |
| **Qt Lottie Animation**  | **提供Lottie动画格式支持。**                                 | **是**   |
| Qt Network Authorization | 提供支持基于OAuth的在线服务授权。                            | 否       |
| Qt Virtual Keyboard      | 提供Qt应用的虚拟键盘。                                       | 否       |
| Qt Quick WebGL           | 提供一个平台插件，允许使用WebGL™通过网络流式传输Qt Quick用户界面。 | 否       |

### 工作交付件及工作计划
- 2022年10月~2022年12月：完成Qt Core、Qt GUI、Qt QML等核心模块移植适配
- 2022年12月~2023年3月：移植Qt相关的工具，匹配Qt相关的项目工程;完成Qt附加模块移植
- 2023年3月~2023年6月：Qt示例及Demo移植适配验证;
- 2023年7月~2023年9月：完成Qt5.12.12版本规划内模块适配及二进制SDK包发布;Qt单元测试移植适配验证
- 2023年10月~2023年12月：完成Qt5.15.11版本规划内模块适配及二进制SDK包发布;发布基于DevEco的Qt应用实例工程；
- 2024年1月~2024年6月：完成Qt6.5.x版本适配及二进制SDK包发布

## SIG组成员

### Leader
- @cwc1987(https://gitee.com/cwc1987)

### Committers列表
- @zhu.wei(https://gitee.com/zhuwei12345678)
- @xiecy(https://gitee.com/xiecyong)
- @wanglz(https://gitee.com/wanglz1988)
- @wangh(https://gitee.com/CplusCplus)
- @honglianglin(https://gitee.com/honglianglin)


### 会议
 - 会议时间：双周例会，周五 10:00-10:30
 - 会议申报：[Qt SIG议题申报](https://shimo.im/sheets/vVqRVBewOBUx7oqy/MODOC)
 - 会议链接：WeLink
 - 会议纪要：[归档链接地址](https://gitee.com/openharmony-sig/sig-content/tree/master/qt/meetings)
 - 会议通知：请[订阅](https://lists.openatom.io/postorius/lists/dev.openharmony.io)邮件列表 dev@openharmony.io 获取会议链接