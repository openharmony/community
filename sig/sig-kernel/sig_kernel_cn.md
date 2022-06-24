 # SIG_Kernel
 简体中文 | [English](./sig_kernel.md)

说明：本SIG的内容遵循OpenHarmony的PMC管理章程 [README](/zh/pmc.md)中描述的约定。

## SIG组工作目标和范围

### 工作目标
- 使能OpenHarmony内核能力： 孵化内核（存储、内存、调度、安全等）增强能力，支撑框架子系统能力；看护内核Linux架构，保证能够持续跟进Linux LTS主线；看护多内核架构，保证OpenHarmony能够同时支持多个内核，方便厂商适配，方便生态发展。
### 工作范围
- 孵化内核（存储、内存、调度、安全等）增强能力，支撑框架子系统能力，提升OpenHarmony平台竞争力；
- 维护内核Linux架构，跟踪Linux LTS主线及安全补丁，提供稳定、安全的内核基线；
- 维护多内核架构，支持轻量化设备选择LiteOS内核，维护生态发展。

## 代码仓
- 代码仓地址：
  - repository1名称：https://gitee.com/openharmony/third_party_littlefs
  - repository2名称：https://gitee.com/openharmony/third_party_e2fsprogs
  - repository3名称：https://gitee.com/openharmony/kernel_linux_build
  - repository4名称：https://gitee.com/openharmony/kernel_linux_4.19
  - repository5名称：https://gitee.com/openharmony/kernel_linux_5.10
  - repository6名称：https://gitee.com/openharmony/filemanagement_user_file_service
  - repository7名称：https://gitee.com/openharmony/filemanagement_file_api
  - repository8名称：https://gitee.com/openharmony/filemanagement_app_file_service
  - repository9名称：https://gitee.com/openharmony/filemanagement_storage_service
  - repository10名称：https://gitee.com/openharmony/filemanagement_dfs_service
  - repository11名称：https://gitee.com/openharmony-sig/filemanagement_fs_tools
  - repository12名称：https://gitee.com/openharmony/third_party_f2fs-tools
  - repository13名称：https://gitee.com/openharmony/third_party_ntfs-3g
  - repository14名称：https://gitee.com/openharmony/third_party_fsck_msdos
  - repository15名称：https://gitee.com/openharmony/third_party_gptfdisk
  - repository16名称：https://gitee.com/openharmony/third_party_newfs_msdos
  - repository17名称：https://gitee.com/openharmony/third_party_exfat-utils
  - repository18名称：https://gitee.com/openharmony/third_party_exfatprogs

## SIG组成员

### Leader
- [@easy-to-see](https://gitee.com/easy-to-see)

### Committers列表
- [@liuyoufang](https://gitee.com/liuyoufang)
- [@kkup180](https://gitee.com/kkup180)
- [@zhangzhiwi](https://gitee.com/zhangzhiwi)
- [@bubble_mao](https://gitee.com/bubble_mao)
- [@linux_anio](https://gitee.com/linux_anio)
- [@vincent_qianjing](https://gitee.com/vincent_qianjing)
- [@weiyj_lk](https://gitee.com/weiyj_lk)

### 会议
 - 会议时间：周二上午9:30
 - 会议申报：请填写[石墨文档](https://shimo.im/sheets/VgQV6VjCJ9cXtY8G/MODOC)，SIG相关申报人自行申请议题
 - 会议链接: Welink或其他会议
 - 会议通知: 请[订阅](https://lists.openatom.io/hyperkitty/list/dev@openharmony.io/)邮件列表 dev@openharmony.io 获取会议链接
 - 会议纪要: [归档链接地址](https://gitee.com/openharmony-sig/sig-content)

### 联系方式(可选)

- 邮件列表：kernel@openharmony.io
- Zulip群组：https://zulip.openharmony.cn
