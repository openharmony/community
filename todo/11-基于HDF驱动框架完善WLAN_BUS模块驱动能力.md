### No.11 - 基于HDF驱动框架完善WLAN BUS驱动能力 - 【团体任务】

### 描述
- BUS 驱动模块向上提供统一的总线抽象接口。通过向下调用Platform层提供的sdio接口和封装适配 usb、pcie 接口，屏蔽不同操作系统的差异；
  通过对不同类型的总线操作进行统一封装，屏蔽不同芯片差异，能够对不同芯片厂商提供完备的总线驱动功能，不同厂商共用此模块接口，
  从而使厂商的开发更为便捷和统一。
- 本项目的目标是实现usb和pcie的总线接口适配。
- 本任务为团体项目，参与人数 2 - 3 人，奖金 x 万元人民币。

### 难度
- 中

### 导师
- @xusai(https://gitee.com/michael4096)
- @houxuanzhe(https://gitee.com/zidane)

### 联系方式
- xusai4@huawei.com
- houxuanzhe@huawei.com

### 产出标准

- 完成BUS模块usb和pcie的接口适配完整功能，能够对接BUS模块的业务统一接口。
- 用一款usb总线的wifi芯片进行调试在框架上运行，wifi功能正常。
- 用一款pcie总线的wifi芯片进行调试在框架上运行，wifi功能正常。
- 需求分析、架构设计、详细设计、测试用例、开发指南、维护手册等文档。

### 技术要求

- 熟悉掌握HDF驱动框架、WLAN驱动、usb和pcie总线等知识
- 熟悉掌握 Linux 内核及硬件驱动等知识
- 熟悉 Git 等代码版本管理工具

### 相关项目

- OpenHarmony 快速指导：https://gitee.com/openharmony/docs/blob/master/zh-cn/readme.md
- OpenHarmony 驱动开发指导 https://gitee.com/openharmony/docs/tree/master/zh-cn/device-dev/driver
- OpenHarmony 驱动技术系列文章 https://gitee.com/openharmony/drivers_framework/issues/I482K0
