# sig-dengluyi
简体中文 | [English](./sig-dengluyi.md)

说明：本SIG的内容遵循OpenHarmony的PMC管理章程 [README](/zh/pmc.md)中描述的约定。

## SIG组工作目标和范围

### 工作目标

为了满足OpenHarmony以及整个物联网行业对数据安全的迫切需求，我们希望基于目前成熟的登录易系统为每个用户和每个设备创建一个自己可以单点管控的全场景物联网设备数据安全管理终端/平台，为每个用户和设备都提供通用的账号管理功能，为企业提供优质安全的物联网设备数据保护，保障万物互联时代下的信息安全,希望通过创新的服务模式与安全成熟的技术为华为等杰出国产品牌智能设备提供数据安全保护屏障，助力国产品牌数据安全，保障国家数据安全，开创万物安全互联的新时代。

### 工作范围

#### 针对 OpenHarmony 账号系统的缺位——建立 OpenHarmony 用户生态 

通过在 OpenHarmony 环境嵌入一个通用标准的多账号管理模块，与手机登录易App通信互操作，实现新用户（包括人类用户和其他设备用户）的自动注册，老用户的自动登录，自动修改密码等功能，建立“登录易+OpenHarmony”生态账号系统，搭建 OpenHarmony 账号安全生态社区。用户除了可以使用专属的原有华为账号体系，还可以通过OpenHarmony开源环境中增加的登录易账号系统与其他 OpenHarmony 用户（和设备）进行安全验证和授权后的资源分享，也可通过账号划定个人私域空间，建立个人云端数据库。通过这种方式提升用户粘性，构建具有完整安全功能的 OpenHarmony 生态社区。

<img src="./images/4.png" style="zoom:48%;" />

#### 针对物联网设备弱密码造成的数据泄露问题——为每个用户建立集中、统一、单点管控的信息与设备管理终端，实施个人用户对多个设备的统一认证管理

用户在自己的登录易App中可以集中、统一、单点管控自己的所有已搭载 OpenHarmony 系统的智能设备，登录易自动为用户在每个设备设置专属的强密码，并可（人工设定或定期）自动修改，用户使用时只需通过装有登录易App的手机等智能设备进行“刷卡”（或同一局域网内的通信）即可完成认证，在免去用户人脑记忆负担的同时，解决产品的数据安全问题。

![](./images/2.png)

#### 针对物联网数据安全保护体系的缺位——实施权限管理/审计记录

用户每次使用搭载“登录易+ OpenHarmony”系统的智能物联网设备时，需要通过 登录易App进行信息认证与记录。通过该账号管理系统限制用户在该设备的使用权限并上传使用记录至日志系统，没有该设备使用权限的用户可通过登录易提交使用请求，没有权限的用户也可通过登录易提交针对部分核心权限功能的使用请求，所有提交使用设备请求的用户的账号信息都会记录在日志系统，存储在日志数据库，便于管理者随时进行调用审计。![](./images/3.png)



## 应用场景案例

日常生活中我们常常会涉及设备的权限问题，如每个人进入家门时都需要有对门锁的权限。这时候如果户主想要给保姆门锁的临时权限（按一段时间内有效或者按次数），便可以让保姆限时限次使用该基于登录易的OpenHarmony用户账号管理系统。保姆进门前需要通过载有OpenHarmony系统的门锁向户主发送请求来申请授权。户主收到请求后，可以同意/拒绝请求。此外，户主可以管理家中其他智能家居的权限，发放部分智能家居的权限给保姆等。

## 代码仓库地址

- openharmony-denlgu1-sig：https://gitee.com/youngp7/openharmony-competition

## SIG组成员

### Leader
- [@YoungP7 (吴宇鹏)](https://gitee.com/YoungP7)
- [@csliuwy(刘文印)](https://gitee.com/csliuwy)

### Committers列表
- [@qqsummer(邱棋锋)](https://gitee.com/qqsummer)
- [@wizardk(欧智昕)](https://gitee.com/wizardk)
- [@Pacific_D(何楷聪)](https://gitee.com/Pacific_D)
- [@ez-yang(伊辙)](https://gitee.com/ez-yang)
- [@yan-wensheng(颜文圣)](https://gitee.com/yan-wensheng)
- [@zeke(吴泽楷)](https://gitee.com/zekeGitee_admin)


### 会议
 - 会议时间：每双周周三 14:00-16:00
 - 会议链接：Welink或其他会议

### 联系方式

- 邮件列表：liuwy@gdut.edu.cn; dengluyi@openharmony.io
- Zulip群组：https://zulip.openharmony.cn/#narrow/stream/18-dengluyi
- 微信群：sig-dengluyi(登录易)
