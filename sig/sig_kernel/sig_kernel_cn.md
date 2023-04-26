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

技术栈范围全景图如下图所示：
![OpenHarmony文档概览](figures/kernel_overview.png)

## LiteOS代码仓
|部件名称|部件功能描述|部件仓名称|
| ------------ | ------------ |------------ |
|LiteOS-A内核|基于Huawei LiteOS上演进发展的新一代内核。适用于资源较丰富嵌入式设备的LiteOS内核	|kernel_liteos_a|
|LiteOS-M内核|基于Huawei LiteOS上演进发展的新一代内核。适用于MCU等各种资源极小设备的LiteOS内核|kernel_liteos_m|
|LiteOS-Littlefs|适用于LiteOS-M上的一个轻量级文件系统|third_party_littlefs|
|LiteOS模拟器|用于模拟LiteOS运行，解除对物理开发板的依赖|device_qemu|
|FatFs|适用于LiteOS上的EMMC等介质的文件系统|third_party_FatFs|
|cmsis|LiteOS-M支持的CMSIS标准接口|third_party_cmsis|

- 代码仓地址：
  - kernel_liteos_a名称：https://gitee.com/openharmony/kernel_liteos_a
  - kernel_liteos_m名称：https://gitee.com/openharmony/kernel_liteos_m
  - third_party_littlefs名称：https://gitee.com/openharmony/third_party_littlefs
  - device_qemu名称：https://gitee.com/openharmony/device_qemu
  - third_party_FatFs名称：https://gitee.com/openharmony/third_party_FatFs
  - third_party_cmsis名称：https://gitee.com/openharmony/third_party_cmsis

## Linux及其他代码仓
|部件名称|部件功能描述|部件仓名称|
| ------------ | ------------ |------------ |
|文件访问接口|提供目录和文件的基础访问操作接口|filemanagement_file_api|
|多窗口感知调度|通过帧感知调度机制，更新进程分组状态，调整内核调度参数，保障系统进程的调度供给|frame_aware_sched|
|增强内存管理|基于应用生命周期状态，更新进程的回收优先级，通过Kill、回收机制来保障系统空闲内存供给|resourceschedule_memmgr|
|分布式文件系统用户态服务|分布式文件系统的用户态守护进程，用来管理链接、挂载、用户管理相关服务状态和信息|filemanagement_dfs_service|
|公共文件管理|提供系统基于用户的公共文件的管理能力|filemanagement_user_file_service|
|应用文件管理|提供应用私有文件的管理能力，提供了系统框架机制，如：分享、克隆。|filemanagement_app_file_service|
|存储管理部件|提供多用户管理、磁盘挂卸载、加解密，磁盘卷状态管理和查询，为系统提供基础的存储管理能力|filemanagement_storage_service|
|内存基础库|提供基础内存操作的系统库|ComonLibary_memory|
|Linux内核部件|基于LTS内核基线，合入上述调度、内存、存储、安全相关的增强能力特性|kernel_linux_config<br>kernel_linux_build<br>kernel_linux_5.10<br>kernel_common_modules<br>kernel_linux_common_modules|
|镜像制作工具|用于生成Host镜像拍包工具|third_party_gptfdisk<br>filemanagement_fs_tools|
|文件系统拍包工具|用于生成指定文件系统格式的拍包工具|third_party_f2fs-tools<br>third_party_ntfs-3g<br>third_party_fsck_msdos<br>third_party_newfs_msdos<br>third_party_exfat-utils<br>third_party_exfatprogs<br>third_party_e2fsprogs|
|native内存分配器|用于替换musl默认内存分配器|third_party_mimalloc|

- 代码仓地址：
  - filemanagement_file_api名称：https://gitee.com/openharmony/filemanagement_file_api
  - frame_aware_sched名称：https://gitee.com/openharmony/frame_aware_sched
  - resourceschedule_memmgr名称：https://gitee.com/openharmony/resourceschedule_memmgr
  - filemanagement_dfs_service名称：https://gitee.com/openharmony/filemanagement_dfs_service
  - filemanagement_user_file_service名称：https://gitee.com/openharmony/filemanagement_user_file_service
  - filemanagement_app_file_service名称：https://gitee.com/openharmony/filemanagement_app_file_service
  - filemanagement_storage_service名称：https://gitee.com/openharmony/filemanagement_storage_service
  - ComonLibary_memory名称：https://gitee.com/openharmony/ComonLibary_memory
  - kernel_linux_build名称：https://gitee.com/openharmony/kernel_linux_config
  - kernel_linux_build名称：https://gitee.com/openharmony/kernel_linux_build
  - kernel_linux_5.10名称：https://gitee.com/openharmony/kernel_linux_5.10
  - third_party_gptfdisk名称：https://gitee.com/openharmony/third_party_gptfdisk
  - filemanagement_fs_tools名称：https://gitee.com/openharmony-sig/filemanagement_fs_tools
  - third_party_f2fs-tools名称：https://gitee.com/openharmony/third_party_f2fs-tools
  - third_party_ntfs-3g名称：https://gitee.com/openharmony/third_party_ntfs-3g
  - third_party_fsck_msdos名称：https://gitee.com/openharmony/third_party_fsck_msdos
  - third_party_newfs_msdos名称：https://gitee.com/openharmony/third_party_newfs_msdos
  - third_party_exfat-utils名称：https://gitee.com/openharmony/third_party_exfat-utils
  - third_party_exfatprogs名称：https://gitee.com/openharmony/third_party_exfatprogs
  - third_party_e2fsprogs名称：https://gitee.com/openharmony/third_party_e2fsprogs
  - third_party_mimalloc名称: https://gitee.com/openharmony/third_party_mimalloc
  - resourceschedule-ffrt-core名称:https://gitee.com/openharmony-sig/resourceschedule_ffrt_core
  - resourceschedule-ffrt-sched名称:https://gitee.com/openharmony-sig/resourceschedule_ffrt_sched
  - kernel_uniproton名称：https://gitee.com/openharmony/kernel_uniproton
  - vendor_alientek名称：https://gitee.com/openharmony/vendor_alientek
  - third_party_libfuse名称: https://gitee.com/openharmony/third_party_libfuse
  - kernel_common_modules名称：https://gitee.com/openharmony-sig/kernel_common_modules
  - kernel_linux_common_modules名称：https://gitee.com/openharmony/kernel_linux_common_modules

## SIG组成员

### Leader
- [@easy-to-see](https://gitee.com/easy-to-see)
- [@weiyj_lk](https://gitee.com/weiyj_lk)

### Committers列表
- [@liuyoufang](https://gitee.com/liuyoufang)
- [@JerryH1011](https://gitee.com/JerryH1011)
- [@zhangzhiwi](https://gitee.com/zhangzhiwi)
- [@bubble_mao](https://gitee.com/bubble_mao)
- [@linux_anio](https://gitee.com/linux_anio)
- [@z-jax](https://gitee.com/z-jax)
- [@leonchan5](https://gitee.com/leonchan5)
- [@gatieme](https://gitee.com/gatieme)

### 会议
 - 会议时间：按需召开 (例行召开时间：周二上午9:30，紧急请联系[@z-jax](https://gitee.com/z-jax) )
 - 会议申报：请填写[石墨文档](https://shimo.im/sheets/8Nk6MM2zmnfj5lqL/MODOC)，SIG相关申报人自行申请议题
 - 会议链接：Welink或其他会议
 - 会议通知：请[订阅](https://lists.openatom.io/hyperkitty/list/kernel@openharmony.io/)邮件列表 kernel@openharmony.io 获取会议链接
 - 会议纪要：[归档链接地址](https://gitee.com/openharmony-sig/sig-content)

### 联系方式(可选)

- 邮件列表：kernel@openharmony.io
- Zulip群组：https://zulip.openharmony.cn
