# sig_RISCV
English | [简体中文](./sig_riscv_cn.md)

Note: The content of this SIG follows the convention described in OpenHarmony's PMC Management Charter [README](../../zh/pmc.md).

## SIG group work objectives and scope


### Objectives of SIG

- RISC-V SIG aims to build a RISC-V ecosystem for OpenHarmony, provide instructions to build software, maintain supports for RISC-V devices, and enable security capabilities like TEE on RISC-V.
- RISC-V SIG will promote more developers to involve in developing OpenHarmony on RISC-V.

### Scope of SIG

- Support of OpenHarmony Subsystems for the RISC-V Architecture

	The SIG is responsible for the porting and adaptation of system components and third-party libraries that are strongly architecture-dependent — including musl, multimedia, graphics, LLVM, and the Ark eTS Runtime — as well as their continuous upgrades across OpenHarmony releases.

- Maintain supported RISC-V devices for OpenHarmony

	The SIG will continuously port and maintain OpenHarmony to support different RISC-V devices.

- RISC-V Security

	The SIG will enable TEE capability for OpenHarmony on RISC-V based on Penglai Enclave.

- Build Ecosystems

	The SIG will actively cooperate with schools and end-users to promote the usage of OpenHarmony on RISC-V devices.
## The repository
- Source Code Co-development Repository([link](https://gitee.com/riscv-sig))

	Since the current OpenHarmony RISC-V adaptation involves changes across a large number of repositories (around 70+), it has not yet been merged into the mainline. To facilitate collaborative development among SIG members, a full fork of the OpenHarmony community repositories has been created under the riscv-sig organization.

- SIG Documentation and Progress Tracking Repository([link](https://gitcode.com/openharmony-sig/riscv))

## SIG Members

### Leader

- [Jiageng Yu](https://gitee.com/yu_jia_geng)

### Committers

- [Dong Du](https://gitee.com/dongduResearcher)
- [Denny](https://gitee.com/DennyShen)- Zulip group: https://zulip.openharmony.cn
- [hplinux](https://gitee.com/hplinux)
- [Tai Yang](https://gitcode.com/taylor_young)
- [xzmu](https://gitee.com/xzmu)
- [clmngu](https://gitee.com/clmngu)
- [linzewentin](https://gitee.com/linzewentin)
- [Fredlou](https://gitee.com/Fredlou)

### Meetings
 - Meeting time：Monthly meeting, on the first Tuesday at 14:00, UTC+8
 - Meeting Proposal: [OpenHarmony RISC-V SIG Meeting Proposal](https://docs.qq.com/sheet/DR21vdXdsVE96c2tk?tab=45wxzh_t=1708586199631)
 - Meeting link：Tencent Meeting
 - Meeting Summary:To view the minutes of past meetings, please click this [Meeting minutes](https://gitcode.com/openharmony-sig/sig-content/tree/master/riscv/meetings)

### Contact (optional)

- Mailing list：dev@openharmony.io
- Wechat：Xin Ding(Sternstunde-00)
