# sig_x86
English | [简体中文](./sig_x86_cn.md)

Note: The content of this SIG follows the convention described in OpenHarmony's PMC Management Charter [README](../../zh/pmc.md).

## SIG group work objectives and scope


### Objectives of SIG

The x86 instruction set is highly favored for its mature technology, strong scalability, and complete ecosystem. Combining x86 architecture with OpenHarmony system can bring multiple advantages such as compatibility, performance, development flexibility, ecological scalability, as well as security and stability. The x86 SIG group aims to build a software and hardware ecosystem around x86+OpenHarmony, providing guidance on adapting software packages and system construction, enabling security and other capabilities in x86 scenarios. The x86 SIG will encourage developers interested in x86+OpenHarmony to participate in open source system development activities.

- Enable OpenHarmony to support X86 architecture and X86 devices, providing guidance on X86 software packages and system construction.

- Maintain support for x86 architecture. Including x86 instruction set, compilation, toolchain QEMU、Clang、Musl、 Adaptation to media, graphics, drivers, TEE, AI, etc.

- Realize the adaptation of x86 chips (mainstream chip series such as Intel/AMD/Zhaoxin/Haiguang) to OpenHarmony standard system.

- Open source and publish the relevant code for x86 to support OpenHarmony on TPC, and continuously maintain the relevant adaptation chip code.

- Based on the OH community, attract 1-2 leading X86 chip manufacturers to jointly build the OpenHarmony chip adaptation under the X86 architecture.

- Attract 2 or more manufacturers of complete machines/boards, broaden the adaptability of OH, and enrich the supported device ecosystem.

- Absorb more than 50 X86 technical experts and jointly build X86+OH base technology in the community.

- Attract Top 100 software development companies from various industries and enrich the application ecosystem.

### Scope of SIG

- General capabilities: Build OpenHarmony's support for x86 architecture, continuously update and improve key capabilities, support x86 standard systems, provide installation images, and offer dynamic/online installation driver packages. Regarding x86 instruction set, compilation, toolchain QEMU、Clang、Musl、 Adaptation to media, graphics, drivers, TEE, AI, etc. Support Arkruntime and other applications, and connect the northbound application framework.

- Security Capability: Combining TEE solutions from top X86 manufacturers to enable OpenHarmony's security capabilities under X86.

- Device adaptation: Adapt to mainstream chips such as Intel Core 8/12th generation, Zhaoxin, etc. The chip adaptation code will be completed and integrated into the TPC warehouse by the end of 2024. Integrate adaptation codes for TOP manufacturers' chips/graphics cards/major peripheral drivers in 2025 and beyond. Support for more devices.

- Scenario extension: Added desktop types, provided unified suite library management, integrated common user graphical interface solutions, desktop 2D/3D libraries, and provided solutions for gaming, multimedia, software development functions, and more. Support virtualization and enterprise level application scenarios, combined with x86 technology, to promote OpenHarmony system virtualization, containerization, and application cloudification, allowing OpenHarmony applications to be used in different scenarios and platforms.

- Ecological Expansion: Actively cooperate with chip, board, system, whole machine manufacturers, and related X86 industry customers to promote the application ecosystem construction of OpenHarmony in X86 environment.

## SIG Members

### Leader

- [xbye](https://gitee.com/xbye)

### Committers

- [pengzhaon](https://gitee.com/pengzhaon)
- [lianzhian](https://gitee.com/lianzhian)
- [hiweil](https://gitee.com/hiweil)
- [paworcn](https://gitee.com/paworcn)
- [chn9528](https://gitee.com/chn9528)
- [diemit](https://gitee.com/diemit)

### Meetings
 - Meeting time：Monthly meeting, first Thursday of the month at 10:00 AM
 - Meeting link：Welink or other meeting
 - Meeting application: [sig_x86Meeting application](https://shimo.im/sheets/5bqndMnd6aiyVNAy)
 - Meeting Summary:To view the minutes of past meetings, please click this [link](https://gitee.com/openharmony-sig/sig-content/tree/master/x86/meetings)

### Contact (optional)

- Mailing list：dev@openharmony.io
- Wechat group：NA
