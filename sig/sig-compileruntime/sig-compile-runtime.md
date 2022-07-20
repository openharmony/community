# SIG_COMPILERUNTIME
 English | [简体中文](./sig-compile-runtime_cn.md)
 
 Note: The content of this SIG follows the convention described in OpenHarmony's PMC Management Charter [README](/zh/pmc.md).

## SIG group work objectives and scope

### objectives

- Support JS/TS language compilation and execution, and create high-performance JS/TS virtual machines.
- Provide basic JSAPI capabilities, including concurrency, string encoding and decoding, and URL parsing capabilities, etc..
- Support C/C++ compilation, debugging based on Clang/LLVM.
- Provide basic library support such as musl and evolution of related abilities.
- Provide new programming language design and implementation based on OpenHarmony's requirements.

### work scope
- Programming language, compiler and runtime architecture design and review.
- Programming language, compiler and runtime implementation and review.
- Community requirements, issues and mailing lists processing.

### overview
- Compiler
![figures/compileruntime-overview-compiler-en.png](figures/compileruntime-overview-compiler-en.png)
- Runtime
![figures/compileruntime-overview-runtime-en.png](figures/compileruntime-overview-runtime-en.png)

### repositories
  - arkcompiler_runtime_core: https://gitee.com/openharmony/arkcompiler_runtime_core
  - arkcompiler_ets_runtime: https://gitee.com/openharmony/arkcompiler_ets_runtime
  - arkcompiler_ets_frontend: https://gitee.com/openharmony/arkcompiler_ets_frontend
  - arkcompiler_toolchain: https://gitee.com/openharmony/arkcompiler_toolchain

  - ets_utils: https://gitee.com/openharmony-sig/commonlibrary_ets_utils

  - third_party_jerryscript: https://gitee.com/openharmony/third_party_jerryscript
  - third_party_quickjs: https://gitee.com/openharmony/third_party_quickjs

  - third_party_llvm-project: https://gitee.com/openharmony-sig/third_party_llvm-project
  - third_party_lldb-mi: https://gitee.com/openharmony-sig/third_party_lldb-mi
  - third_party_mingw-w64: https://gitee.com/openharmony/third_party_mingw-w64
  - third_party_musl: https://gitee.com/openharmony/third_party_musl
  - third_party_mimalloc: https://gitee.com/openharmony-sig/third_party_mimalloc

  - commonlibrary_c_utils: https://gitee.com/openharmony/commonlibrary_c_utils
  - commonlibrary_utils_lite: https://gitee.com/openharmony/commonlibrary_utils_lite

  - utils_memory: https://gitee.com/openharmony/utils_memory

  - third_party_miniz: https://gitee.com/openharmony/third_party_miniz

## SIG Members

### Leader
- @klooer (https://gitee.com/klooer)

### Committers
- @huanghuijin (https://gitee.com/huanghuijin)
- @wuzhefengh (https://gitee.com/wuzhefengh)
- @gongjunsong (https://gitee.com/gongjunsong)
- @sunzhe23 (https://gitee.com/sunzhe23)
- @weng-changcheng (https://gitee.com/weng-changcheng)
- @yingguofeng (https://gitee.com/yingguofeng)
- @xliu-huanwei (https://gitee.com/xliu-huanwei)
- @flyingwolf (https://gitee.com/flyingwolf)
- @godmiaozi (https://gitee.com/godmiaozi)
- @dhy308 (https://gitee.com/dhy308)
- @pengzhuoli (https://gitee.com/zhuoli72)
- @JerryH1011 (https://gitee.com/JerryH1011)
- @dongduResearcher (https://gitee.com/dongduResearcher)

 ### Meetings
 - Meeting time: Bi-weekly meeting, Monday 19:00 pm, UTC+8
 - Meeting application: [SIG-COMPILERUNTIME Meeting Proposal](https://shimo.im/sheets/cHkjRvDJQtt638y3/MODOC)
 - Meeting link: Welink Meeting or Others
 - Meeting notification: [Subscribe to](https://lists.openatom.io/postorius/lists/dev.openharmony.io) mailing list dev@openharmony.io for the meeting link
 - Meeting-Minutes: [Archive link address](https://gitee.com/openharmony-sig/sig-content)
 
 ### Contact
 
 - Mailing list: dev@openharmony.io
 - Zulip group: https://zulip.openharmony.cn
 - Wechat group: NA
