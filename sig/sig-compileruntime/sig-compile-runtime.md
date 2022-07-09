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
- Provide development, maintenance and optimizations of the build framework, supporting the build for multiple products and configurable components.

### work scope
- Programming language, compiler and runtime architecture design and review.
- Programming language, compiler and runtime implementation and review.
- Community requirements, issues and mailing lists processing.

### repositories
  - arkcompiler_runtime_core: https://gitee.com/openharmony/arkcompiler_runtime_core
  - arkcompiler_ets_runtime: https://gitee.com/openharmony/arkcompiler_ets_runtime
  - arkcompiler_ets_frontend: https://gitee.com/openharmony/arkcompiler_ets_frontend

  - js_api_module: https://gitee.com/openharmony/js_api_module
  - js_sys_module: https://gitee.com/openharmony/js_sys_module
  - js_util_module: https://gitee.com/openharmony/js_util_module
  - js_worker_module: https://gitee.com/openharmony/js_worker_module

  - third_party_jerryscript: https://gitee.com/openharmony/third_party_jerryscript
  - third_party_quickjs: https://gitee.com/openharmony/third_party_quickjs

  - third_party_llvm-project: https://gitee.com/openharmony-sig/third_party_llvm-project
  - third_party_lldb-mi: https://gitee.com/openharmony-sig/third_party_lldb-mi
  - third_party_mingw-w64: https://gitee.com/openharmony/third_party_mingw-w64
  - third_party_musl: https://gitee.com/openharmony/third_party_musl
  - third_party_mimalloc: https://gitee.com/openharmony-sig/third_party_mimalloc

  - utils: https://gitee.com/openharmony/utils
  - utils_memory: https://gitee.com/openharmony/utils_memory
  - utils_native: https://gitee.com/openharmony/utils_native
  - utils_native_lite: https://gitee.com/openharmony/utils_native_lite
  - third_party_miniz: https://gitee.com/openharmony/third_party_miniz

  - build_lite: https://gitee.com/openharmony/build_lite
  - build: https://gitee.com/openharmony/build
  - third_party_gn: https://gitee.com/openharmony/third_party_gn
  - third_party_jinja2: https://gitee.com/openharmony/third_party_jinja2
  - third_party_ninja: https://gitee.com/openharmony/third_party_ninja
  - third_party_python: https://gitee.com/openharmony/third_party_python
  - productdefine_common: https://gitee.com/openharmony/productdefine_common
  - third_party_markupsafe: https://gitee.com/openharmony/third_party_markupsafe

## SIG Members

### Leader
- @Xingwa (https://gitee.com/wangxing-hw)
- @huanghuijin (https://gitee.com/huanghuijin)

### Committers
- @weichaox (https://gitee.com/weichaox)
- @jady3356 (https://gitee.com/taiyipei)
- @Han00000000 (https://gitee.com/Han00000000)
- @wuzhefengh (https://gitee.com/wuzhefengh)
- @gongjunsong (https://gitee.com/gongjunsong)
- @sunzhe23 (https://gitee.com/sunzhe23)
- @weng-changcheng (https://gitee.com/weng-changcheng)
- @yingguofeng (https://gitee.com/yingguofeng)
- @flyingwolf (https://gitee.com/flyingwolf)
- @godmiaozi (https://gitee.com/godmiaozi)
- @dhy308 (https://gitee.com/dhy308)
- @pengzhuoli (https://gitee.com/zhuoli72)
- @cbraham (https://gitee.com/cbraham)
- @wang2002xu (https://gitee.com/wang2002xu)
- @chen-wandun (https://gitee.com/chen-wandun)
- @eliotc (https://gitee.com/eliotc)

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
