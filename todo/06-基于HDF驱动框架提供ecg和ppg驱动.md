### No.06 - 基于HDF驱动框架提供ECG和pPPG驱动能力 - 【团体任务】

### 描述
- 目前市场可供开发者选择的传感器越来越多，比如：加速度传感器，陀螺仪传感器，ECG/PPG传感器，温度传感器等类型。每种传感器厂家都有各自的传感器驱动，在产品开发时就需要对不同厂家或者同一厂家的不同型号进行适配开发，就会增加开发者的开发难度。为了快速开发或者移植传感器驱动，基于HDF（Hardware Driver Foundation）驱动框架开发了Sensor（传感器）驱动模型。Sensor驱动模型主要为上层提供稳定接口能力，对驱动开发者提供开放的接口实现和抽象的配置接口能力。
- 本项目的目标是基于HDF驱动框架开发的Sensor（传感器）驱动模型，实现ECG/PPG传感器使能，去使能，采样率配置，数据上报等功能，支撑上层服务使用ECG/PPG驱动能力。
- 本任务为团体项目，参与人数 2 - 3 人，奖金 x 万元人民币。

### 难度
- 中

### 导师
- @liufeihu(https://gitee.com/Kevin-Lau)
- @houxuanze(https://gitee.com/zianed)

### 联系方式
- liufeihu@huawei.com
- houxuanzhe@huawei.com

### 产出标准

- 实现ECG传感器抽象驱动，提供差异化驱动接口和差异化HCS配置，支持不同厂家的ECG传感器件。
- 实现PPG传感器抽象驱动，提供差异化驱动接口和差异化HCS配置，支持不同厂家的PPG传感器件。
- 按照数据改变模式上报ECG感器事情数据。
- 按照数据改变模式上报PPG传感器事情数据。
- 需求分析、架构设计、详细设计、测试用例、开发指南、维护手册等文档

### 技术要求

- 熟悉掌握HDF驱动框架、sensor驱动模型，sensor传感器等知识
- 熟悉掌握 Linux 内核及硬件驱动等知识
- 熟悉 Git 等代码版本管理工具

### 相关项目

- OpenHarmony 快速指导：https://gitee.com/openharmony/docs/blob/master/zh-cn/readme.md
- OpenHarmony 驱动开发指导 https://gitee.com/openharmony/docs/tree/master/zh-cn/device-dev/driver
- OpenHarmony 驱动技术系列文章 https://gitee.com/openharmony/drivers_framework/issues/I482K0
