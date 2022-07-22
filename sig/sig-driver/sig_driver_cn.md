# SIG_DriverFramework

简体中文 | [English](./sig_driver.md)

说明：本SIG的内容遵循OpenHarmony的PMC管理章程 [README](/zh/pmc.md)中描述的约定。

## SIG组工作目标和范围

### 工作目标

Driver sig负责构建OpenHarmony的统一硬件驱动平台HDF（Hardware Driver Foundation），以不断提升设备驱动开发效率，实现驱动软件在不同大小设备的部署目标；构建具备内核解耦，弹性化框架，组件化设备模型，及统一配置界面的硬件驱动平台。

### 工作范围

- 设备驱动架构定义、设计、演进和看护。
- HDI（Hardware Device Interface）接口评审。
- 组织社区设备驱动例会，策划技术解答分享，问题交流互动。
- 积极与开发者推动设备驱动在OpenHarmony项目的南向生态建设和拓展。

设备驱动技术栈范围全景图
![OpenHarmony文档概览](figures/driver-overview.png)

说明：HDF驱动管理框架部件及各设备驱动部件代码可以根据编译制定，构建在轻量系统设备，小型系统设备或者标准系统设备中；在标准系统设备中，可以编译指定构建在用户态还是内核态。

## 代码仓

- **drivers_hdf_core代码仓部件**

| 部件名称              | 部件功能描述                                                                 | 部件路径名称           |
| ----------------- | ---------------------------------------------------------------------- | ---------------- |
| HDF驱动框架【hdf_core】 | 支持设备服务管理、设备驱动管理、配置文件编译工具、配置文件动态解析、器件设备电源管理、定位调试能力、热插拔管理、访问权限控制、平台驱动模型。 | drivers/hdf_core |

- **drivers_peripheral代码仓部件**

| 部件名称                                             | 部件功能描述                                                                                                                                              | 部件路径名称                                |
| ------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------- |
| 音频设备驱动 【drivers_peripheral_audio】                | PCM软件参数配置,PCM码流操作,音频播放控制,音频录制控制,音频框架Adaption,音频音效控制能力。                                                                                              | drivers/peripheral/audio              |
| 相机设备驱动【drivers_peripheral_camera】                | 拍照预览,拍照功能,录像预览,录制视频,Camera设备管理,Camera Pipeline管理,Camera Sensor设备管理,Camera Sensor控制参数配置,Camera Sensor数据流管理,Camera Sensor模型。                          | drivers/peripheral/camera             |
| 显示设备驱动【drivers_peripheral_display】               | 显示硬件控制,显示硬件合成,显示内存管理,显示设备管理,显示驱动模型。                                                                                                                 | drivers/peripheral/display            |
| WLAN设备驱动 【drivers_peripheral_wlan】               | 开关WIFI（STA 模式）,支持开关WIFI（AP模式）,支持开关WIFI（p2p直连）,支持STA模式下扫描网络,支持省电休眠设置（低功耗）,支持连接/断开网络,支持数据传输Iperf打流测试,支持WLAN抗干扰模式,支持WLAN功率模式,支持WLAN P2P兼容,支持WLAN兼容性架构。 | drivers/peripheral/wlan               |
| 输入设备驱动【drivers_peripheral_input】                 | 打开关闭input设备，读取input事件,提供设备注册、注销、热插拔机制,支持获取input设备信息,支持设置与执行拓展input设备命令。                                                                             | drivers/peripheral/input              |
| 传感器设备驱动【drivers_peripheral_sensor】               | 传统的传感器驱动模型(加速度计、陀螺仪、磁力计、环境光、接近光、霍尔传感器、气压计、温度计)，医学传感器驱动模型，传感器驱动管理和数据订阅能力。                                                                            | drivers/peripheral/sensor             |
| USB设备驱动 【drivers_peripheral_usb】                 | 支持USB设备模式、支持USB主机模式。                                                                                                                                | drivers/peripheral/usb                |
| 蓝牙设备驱动【drivers_peripheral_bluetooth】             | 支持打开蓝牙、关闭蓝牙、监听蓝牙连接状态，实现BT睡眠唤醒机制。                                                                                                                    | drivers/peripheral/Bluetooth          |
| drivers/peripheral/Bluetooth 振动设备驱动              | 马达振动，马达停止，马达效果调制能力。                                                                                                                                 | drivers/periphera/vibrator            |
| 编解码设备驱动 【drivers_peripheral_codec】               | Codec HDI服务、Codec配置能力、Codec buffer 队列管理、Codec 适配层。                                                                                                      | drivers/peripheral/codec              |
| 灯光设备驱动 【drivers_peripheral_light】                | 灯的控制，灯的效果配置。                                                                                                                                        | drivers/peripheral/light              |
| 热设备驱动【drivers_peripheral_thermal】                | 轮询和感知系统硬件发热状态，并将期间的热状态信息上报给热管理服务。                                                                                                                   | drivers/peripheral/thermal            |
| 电池设备驱动 【drivers_peripheral_battery】              | 电池状态信息的查询和上报                                                                                                                                        | drivers/peripheral/powermgr/battery   |
| 电源设备驱动【drivers_peripheral_power】                 | 电源休眠/唤醒状态的处理，运行锁的处理。                                                                                                                                | drivers/peripheral/power              |
| 手势识别设备驱动【drivers_peripheral_motion】              | 手势识别设备模型，具有使能，去使能手势识别，数据订阅能力。                                                                                                                       | drivers/peripheral/motion             |
| NFC设备驱动 【drivers_peripheral_nfc】                 | NFC开关能力、提供Tag标签读写卡能力、提供HCE卡模拟能力、提供eSE卡模拟能力。                                                                                                         | drivers/peripheral/nfc                |
| NFC有源标签设备驱动 【drivers_peripheral_connected_tag】   | 提供的“有源标签”读写能力，把一些设备信息，写入到标签芯片。                                                                                                                      | drivers/peripheral/nfc/connected_tag  |
| 分布式相机设备驱动【drivers_peripheral_distributed_camera】 | 提供本地相机HDI接口和分布式相机扩展HDI接口的实现，和相机框架以及分布式相机SA之间进行交互，完成分布式相机的操作。                                                                                        | drivers/peripheral/distributed_camera |
| 内存跟踪设备驱动 【drivers_peripheral_memorytracker】      | 获取设备驱动相关内存占用信息。                                                                                                                                     | drivers/peripheral/memorytracker      |
| 用户认证设备驱动 【drivers_peripheral_user_auth】          | 提供用户身份认证功能，包含指定用户id的用户身份认证和不指定用户id的用户身份识别功能，内部实现用户身份认证方案生成和结果评估，使用户身份认证达到目标安全等级要求。                                                                  | drivers/peripheral/user_auth          |
| 人脸认证设备驱动【drivers_peripheral_face_auth】           | 提供用户人脸的录入/删除/防暴力破解等能力，按资源池定义方式，作为执行器对接到统一认证框架。                                                                                                      | drivers/peripheral/face_auth          |
| 口令认证设备驱动 【drivers_peripheral_pin_auth】           | 提供用户口令的录入/删除/防暴力破解等能力，按资源池定义方式，作为执行器对接到统一认证框架。                                                                                                      | drivers/peripheral/pin_auth           |
| 指纹认证设备驱动【drivers_peripheral_fingerprint_auth】    | 提供指纹的录入，删除和认证/识别功能。                                                                                                                                 | drivers/peripheral/fingerprint_auth   |

- **drivers_interface代码仓部件**

| 部件名称                                                | 部件功能描述                                                                             | 部件路径名称                               |
| --------------------------------------------------- | ---------------------------------------------------------------------------------- | ------------------------------------ |
| 显示设备HDI接口 【drivers_interface_display】               | 提供显示设备HDI接口。                                                                       | drivers/interface/display            |
| WLAN设备HDI接口 【drivers_interface_wlan】                | 提供WLAN设备HDI接口。                                                                     | drivers/interface/wlan               |
| 输入设备HDI接口 【drivers_interface_input】                 | 提供Input设备HDI接口。                                                                    | drivers/interface/input              |
| 传感器设备HDI接口 【drivers_interface_sensor】               | 提供传感器设备HDI接口。                                                                      | drivers/interface/sensor             |
| 振动设备HDI接口 【drivers_interface_vibrator】              | 提供马达设备HDI接口。                                                                       | drivers/interface/vibrator           |
| 灯光设备HDI接口 【drivers_interface_light】                 | 提供灯设备HDI接口。                                                                        | drivers/interface/light              |
| 手势识别设备HDI接口 【drivers_interface_motion】              | 提供手势识别HDI接口。                                                                       | drivers/interface/motion             |
| USB设备HDI接口 【drivers_interface_usb】                  | 提供USB设备HDI接口。                                                                      | drivers/interface/usb                |
| 热设备HDI接口 【drivers_interface_thermal】                | 提供热设备HDI接口。                                                                        | drivers/interface/thermal            |
| 电源设备HDI接口 【drivers_interface_power】                 | 提供电源设备HDI接口。                                                                       | drivers/interface/power              |
| 电池设备HDI接口 【drivers_interface_battery】               | 提供电池设备HDI接口。                                                                       | drivers/interface/battery            |
| NFC设备HDI接口【drivers_interface_nfc】                   | 提供NFC开关能力、提供Tag标签读写卡能力、提供HCE卡模拟能力、提供eSE卡模拟能力。                                      | drivers/interface/nfc                |
| 分布式相机设备HDI接口 【drivers_interface_distributed_camera】 | 提供分布式相机扩展HDI接口的定义。                                                                 | drivers/interface/distributed_camera |
| 内存跟踪设备HDI接口 【drivers_interface_memorytracker】       | 获取设备驱动相关内存占用信息。                                                                    | drivers/interface/memorytracker      |
| 用户认证设备HDI接口 【drivers_interface_user_auth】           | 提供用户身份认证功能，包含指定用户id的用户身份认证和不指定用户id的用户身份识别功能，内部实现用户身份认证方案生成和结果评估，使用户身份认证达到目标安全等级要求。 | drivers/interface/user_auth          |
| 人脸认证设备HDI接口【drivers_interface_face_auth】            | 提供用户人脸的录入/删除/防暴力破解等能力，按资源池定义方式，作为执行器对接到统一认证框架。                                     | drivers/interface/face_auth          |
| 口令认证设备HDI接口【drivers_interface_pin_auth】             | 提供用户口令的录入/删除/防暴力破解等能力，按资源池定义方式，作为执行器对接到统一认证框架。                                     | drivers/interface/pin_auth           |
| 指纹认证设备HDI接口 【drivers_interface_fingerprint_auth】    | 提供指纹的录入，删除和认证/识别功能。                                                                | drivers/interface/fingerprint_auth   |

- **代码仓地址：**
  - drivers_hdf_core：https://gitee.com/openharmony/drivers_hdf_core
  - drivers_peripheral：https://gitee.com/openharmony/drivers_peripheral
  - drivers_interface：https://gitee.com/openharmony/drivers_interface
  - third_party_libnl：https://gitee.com/openharmony/third_party_libnl
  - third_party_openmax：https://gitee.com/openharmony/third_party_openmax

## SIG组成员

### Leader

- @zhaowenhua(https://gitee.com/shidi_snow)

### Committers列表

- @zianed(https://gitee.com/zianed)

- @Kevin-Lau(https://gitee.com/Kevin-Lau)

- @yuanbo(https://gitee.com/yuanbogit)

- @zhuangchunxin(https://gitee.com/aqxyjay)
  
  ### 会议
  
  - 会议时间：双周例会，周三下午16:00
  - 会议申报：[SIG-Driver会议议题收集](https://shimo.im/sheets/36GKhpvrXd8TcQHY)
  - 会议链接：腾讯会议或其他会议
  - 会议通知: 请[订阅](https://lists.openatom.io/postorius/lists/sig_driver.openharmony.io/)邮件列表获取会议链接
  - 会议纪要：查看往期会议纪要，请点此[链接](https://gitee.com/openharmony-sig/sig-content/tree/master/driver/meetings)

### 联系方式(可选)

- 邮件列表：[sig_driver@openharmony.io](https://lists.openatom.io/postorius/lists/sig_driver.openharmony.io/)
- Zulip群组：https://zulip.openharmony.cn
- 微信群：xxx
