# SIG_COMPILERUNTIME
 English | [简体中文](./sig_compileruntime_cn.md)
 
 Note: The content of this SIG follows the convention described in OpenHarmony's PMC Management Charter [README](/zh/pmc.md).

## SIG group work objectives and scope

### work goals

- The development and maintenance of compilation framework and its efficiency improvement. Supporting compilation of multiple products and components.
- Support JS/TS language compilation and runtime, and create high-performance JS/TS virtual machines. Provide basic JSAPI capabilities, including multi-threading capabilities, encoding and decoding string capabilities, and URL parsing capabilities.
- Support C/C++ compilation, debugging based on Clang/LLVM.
- Provide basic library support such as musl and evolution of related abilities.

### work scope
- Design, review, and make decisions on the architecture of the language compilation and runtime.
- Review and incorporate the code of the language compilation and runtime, prohibit low-quality code from being incorporated into the master branch.
- Actively and effectively participate in code review and comment, share programming experience, communicate with developers, transfer software development skills, and effectively coach open source community developers to write good code.
- Handle requirements, issues and mailing lists, and ensure that the closure period meets the SLA requirements of the OpenHarmony community.
- Provide feedback and guidance on code quality based on review and development activities to improve code quality in the OpenHarmony community.

### The repository 
- project name:
  - build_lite: https://gitee.com/openharmony/build_lite
  - build: https://gitee.com/openharmony/build
  - js_api_module: https://gitee.com/openharmony/js_api_module
  - js_sys_module: https://gitee.com/openharmony/js_sys_module
  - js_util_module: https://gitee.com/openharmony/js_util_module
  - js_worker_module: https://gitee.com/openharmony/js_worker_module
  - productdefine_common: https://gitee.com/openharmony/productdefine_common
  - prebuilts_aosp_libs: https://gitee.com/openharmony/prebuilts_aosp_libs
  - third_party_gn: https://gitee.com/openharmony/third_party_gn
  - third_party_jinja2: https://gitee.com/openharmony/third_party_jinja2
  - third_party_jerryscript: https://gitee.com/openharmony/third_party_jerryscript
  - third_party_markupsafe: https://gitee.com/openharmony/third_party_markupsafe
  - third_party_mingw-w64: https://gitee.com/openharmony/third_party_mingw-w64
  - third_party_musl: https://gitee.com/openharmony/third_party_musl
  - third_party_mimalloc: https://gitee.com/openharmony-sig/third_party_mimalloc
  - third_party_ninja: https://gitee.com/openharmony/third_party_ninja
  - third_party_python: https://gitee.com/openharmony/third_party_python
  - third_party_quickjs: https://gitee.com/openharmony/third_party_quickjs
  - utils: https://gitee.com/openharmony/utils
  - utils_memory: https://gitee.com/openharmony/utils_memory
  - utils_native: https://gitee.com/openharmony/utils_native
  - utils_native_lite: https://gitee.com/openharmony/utils_native_lite

  - third_party_llvm-project: https://gitee.com/openharmony-sig/third_party_llvm-project
  - third_party_lldb-mi: https://gitee.com/openharmony-sig/third_party_lldb-mi

  - ark_runtime_core: https://gitee.com/openharmony/ark_runtime_core
  - ark_js_runtime: https://gitee.com/openharmony/ark_js_runtime
  - ark_ts2abc: https://gitee.com/openharmony/ark_ts2abc
  - third_party_miniz: https://gitee.com/openharmony/third_party_miniz

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
