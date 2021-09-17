### No.01 - 基于HDF驱动框架提供codec驱动能力 - 【团体任务】

### 描述
- 图像、音频等媒体信息经采集后生成的原始视频数据量非常庞大，不利于存储和传输，而编码处理之后会显著减小视频的大小，所以无论是为了存储或者为了传输，亦或是为了加密、修改都必须对视频进行编码。编码之后的视频通过解码还原视频的原貌，解码过程中能够得到码流片段，可以通过码流片段对视频流进行处理。
- 本项目的目标是基于HDF驱动框架提供codec驱动框架，实现音视频编码和解码基本功能，支撑上层服务使用codec驱动能力。
- 本任务为团体项目，参与人数 3 - 4 人，奖金 x 万元人民币。

### 难度
- 中

### 导师
- @sunhehe(https://gitee.com/crescenthe)
- @zhangyunhu(https://gitee.com/vb6174)

### 联系方式
- sunhehe@huawei.com
- zhangyunhu@huawei.com

### 产出标准

- 实现 Codec 驱动编解码基本功能
- 兼容当前的Codec HDI IPC服务化模块
- 提供一套通用的接口，让OEM厂商通过适配这些接口来接入Codec编解码模块
- 提供OpenMAX兼容适配层，可以对接OpenMAX框架
- 需求分析、架构设计、详细设计、测试用例、开发指南、维护手册等文档

### 技术要求

- 熟悉掌握HDF驱动框架、Codec编解码等知识
- 熟悉掌握 Linux 内核及硬件驱动等知识
- 熟悉 Git 等代码版本管理工具

### 相关项目

- OpenHarmony 快速指导：https://gitee.com/openharmony/docs/blob/master/zh-cn/readme.md
- OpenHarmony 驱动开发指导 https://gitee.com/openharmony/docs/tree/master/zh-cn/device-dev/driver
- OpenHarmony 驱动技术系列文章 https://gitee.com/openharmony/drivers_framework/issues/I482K0
