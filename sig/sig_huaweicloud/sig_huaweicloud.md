# sig_HuaweiCloud
English | [简体中文](./sig_huaweicloud_cn.md)

Note: The content of this SIG follows the convention described in OpenHarmony's PMC Management Charter [README](/zh/pmc.md).

## SIG group work objectives and scope

### work goals

Provide cloud collaboration components for OpenHarmony, hoping that HUAWEI CLOUD can drive OpenHarmony's breakthroughs in more frontier solutions and facilitate the development of its ecology.

### work scope
- Open source software hosting platform for Huawei Cloud components
-  Design, review, and make decisions on the architecture of software modules related to the HUAWEI CLOUD related open source projects. 
- Be responsible for reviewing and merging the code of software modules in the HUAWEI CLOUD domain software, prohibit low-quality code from being merged into the master branch, and maintain the test code. 
- Actively and effectively participate in code review and comment, share programming experience, communicate with developers, transfer software development skills, and effectively coach open source community developers to write good code. 
- Handle requirements, issues and mailing lists.
- Provide feedback and guidance on code quality based on review and development activities to improve code quality in the OpenHarmony community. 

##  Code Repository

| Component<img width=100/> | Function<img width=200/>                                     | Code Repository<img width=100/>           |
| ------------------------- | ------------------------------------------------------------ | ----------------------------------------- |
| IoT                       | Help OpenHarmony mini system, small system, and standard system devices quickly connect to the IoT platform. The devices that support the TCP/IP protocol stack can communicate directly with the IoT platform after integrating the IoT Device SDK, devices that do not support the TCP/IP protocol stack, such as Bluetooth, ZigBee and other devices, can forward device data to the IoT platform through the gateway integrated with the IoT Device SDK to communicate with the cloud platform. The main functions of device-cloud collaboration are as follows:<br>Cloud platform communication capabilities: establish and break links with the cloud platform, report messages, attributes, events, etc., and receive commands, send messages, upload and download files, and a series of communication functions.<br>Device-cloud secure communication: The cloud sends security PIN code information, sends device groups through the Huawei cloud platform, and devices realize the interconnection of things through the OpenHarmony softbus.<br>Device rule engine: Device-side rules provide capabilities similar to cloud rules. After setting the rules, the device will judge whether the rule triggering conditions are met. When the conditions are met, the device will execute the actions preset by the user. Unlike cloud rules, device-side rules can continue to run on the device side even when the network is interrupted or the device cannot interact with the cloud.<br/>Remote SSH login: You can remotely log in to your own online devices through the HUAWEI CLOUD IoTDA platform.<br/>Anomaly detection: Based on device-cloud collaboration, the device can detect abnormalities such as memory, storage space, abnormal ports, battery power, and CPU usage.<br>M2M function: currently supports to use the SDK to connect to the edge IoTEdge, and the edge node completes the transfer of the message to the target device. | iot_device_sdk_c<br>iot_device_sdk_c_tiny |

### The repository 

- project name:
  - iot_device_sdk_c: https://gitee.com/openharmony/iot_device_sdk_c
  - iot_device_sdk_c_tiny: https://gitee.com/openharmony/iot_device_sdk_c_tiny


## SIG Members

### Leader
- @one_two_zero(https://gitee.com/one_two_zero)

### Committers
- @one_two_zero(https://gitee.com/one_two_zero)
- @liteos2021(https://gitee.com/liteos2021)
- @xinglichen(https://gitee.com/xinglichen）
- @jojo_cjw(https://gitee.com/jojo_cjw)
- @Aiminabb(https://gitee.com/Aiminabb)

### Meetings
 - Meeting time: Bi-weekly meeting, Thursday 14:30-16:00 pm, UTC+8 
 - Meeting Proposal: [OpenHarmony sig_HuaweiCloud Meeting Proposal](https://shimo.im/sheets/zdkyBwNxgzCP8nA6/MODOC)
 - Meeting link: Welink or others
 - Meeting notification: [Subscribe to](https://lists.openatom.io/postorius/lists/dev.openharmony.io) mailing list dev@openharmony.io for the meeting link
 - Meeting Summary:To view the minutes of past meetings, please click this [Meeting minutes](https://gitee.com/openharmony-sig/sig-content/tree/master/huaweicloud/meetings)

### Contact
| Address                                 | Introduction | Usage Description                                                  |
| ---------------------------------------|---------- | ------------------------------------------------------------ |
| dev@openharmony.io  <img width=120/>| Mailing list <img width=100/> | OpenHarmony community development discussion mailing list, any community development related topics can be discussed in the mailing list. Any developer can [subscribe](https://lists.openatom.io/postorius/lists/dev.openharmony.io)。<img width=200/>|
