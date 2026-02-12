# 架构SIG例会 2025-09-28 16:30-18:00(UTC+08:00)Beijing

## 议题(Agenda)

议题1、SIG仓申请孵化毕业：location_location_cangjie_wrapper  
议题2、SIG仓申请孵化毕业：notification_notification_cangjie_wrapper  
议题3、SIG仓申请孵化毕业：applications_applications_cangjie_wrapper  
议题4、SIG仓申请孵化毕业：telephony_telephony_cangjie_wrapper  
议题5、SIG仓申请孵化毕业：netmanager_netmanager_cangjie_wrapper  
议题6、SIG仓申请孵化毕业：time_time_cangjie_wrapper  
议题7、SIG仓申请孵化毕业：startup_startup_cangjie_wrapper  
议题8、SIG仓申请孵化毕业：third_party_cangjie_stdx  
议题9、SIG仓申请孵化毕业：third_party_cangjie_runtime遗留问题闭环  
议题10、SIG仓申请孵化毕业：third_party_cangjie_tools遗留问题闭环  

## 与会人(Attendees)

任革林 [@im-off-this-week](https://gitcode.com/im-off-this-week)  
董金光 [@dong_jinguang](https://gitcode.com/dong_jinguang)  

## 会议纪要(Notes)

**议题1、SIG仓申请孵化毕业：location_location_cangjie_wrapper**  
汇报人：刘涵  
会议结论：  
1、同意location_location_cangjie_wrapper仓孵化毕业，可申请QA SIG评审。孵化仓地址为:https://gitcode.com/openharmony-sig/location_location_cangjie_wrapper 。  
遗留问题：  
无。  

**议题2、SIG仓申请孵化毕业：notification_notification_cangjie_wrapper**  
汇报人：焦阳  
会议结论：  
1、同意notification_notification_cangjie_wrapper仓孵化毕业，可申请QA SIG评审。孵化仓地址为:https://gitcode.com/openharmony-sig/notification_notification_cangjie_wrapper 。  
遗留问题：  
无。  

**议题3、SIG仓申请孵化毕业：applications_applications_cangjie_wrapper**  
汇报人：邵一帆  
会议结论：  
1、同意applications_applications_cangjie_wrapper仓孵化毕业，可申请QA SIG评审，允许线下闭环剩余遗留问题。孵化仓地址为:https://gitcode.com/openharmony-sig/applications_applications_cangjie_wrapper 。  
遗留问题：  
1、建议针对异常场景添加DFX维测能力以及对hiviewdfx的部件依赖。  

**议题4、SIG仓申请孵化毕业：telephony_telephony_cangjie_wrapper**  
汇报人：焦阳  
会议结论：  
1、同意telephony_telephony_cangjie_wrapper仓孵化毕业，可申请QA SIG评审。孵化仓地址为:https://gitcode.com/openharmony-sig/telephony_telephony_cangjie_wrapper 。  
遗留问题：  
无。  

**议题5、SIG仓申请孵化毕业：netmanager_netmanager_cangjie_wrapper**  
汇报人：罗明  
会议结论：  
1、遗留问题闭环后同意netmanager_netmanager_cangjie_wrapper仓孵化毕业，可申请QA SIG评审，允许线下闭环剩余遗留问题。孵化仓地址为:https://gitcode.com/openharmony-sig/netmanager_netmanager_cangjie_wrapper 。  
遗留问题：  
1、readme中使用说明部分需要补充NetManager以及NetStack具体功能，使开发者易于理解。  

**议题6、SIG仓申请孵化毕业：time_time_cangjie_wrapper**  
汇报人：邵一帆  
会议结论：  
1、同意time_time_cangjie_wrapper仓孵化毕业，可申请QA SIG评审。孵化仓地址为:https://gitcode.com/openharmony-sig/time_time_cangjie_wrapper 。  
遗留问题：  
无。  

**议题7、SIG仓申请孵化毕业：startup_startup_cangjie_wrapper**  
汇报人：焦阳  
会议结论：  
1、同意startup_startup_cangjie_wrapper仓孵化毕业，可申请QA SIG评审。孵化仓地址为:https://gitcode.com/openharmony-sig/startup_startup_cangjie_wrapper 。  
遗留问题：  
无。  

**议题8、SIG仓申请孵化毕业：third_party_cangjie_stdx**  
汇报人：虞家豪  
会议结论：  
1、同意startup_startup_cangjie_wrapper仓孵化毕业，可申请QA SIG评审。孵化仓地址为:https://gitcode.com/openharmony-sig/startup_startup_cangjie_wrapper 。  
遗留问题：  
1、stdx定位属于应用级三方库，需要与TPC的owner 于洋沟通，明确归属策略；  
2、readme的架构图中标准库和运行时属于同一部件，需要合并，且不需要体现对三方依赖的箭头；  
3、明确src目录下子目录后续的规划；  
4、仓的目录中删除third_party目录，同步修改readme；  
5、构建步骤里配置Cangjie SDK要改成OpenHarmony SDK；  
6、构建命令删除OpenSSL的--target-lib参数。  

**议题9、SIG仓申请孵化毕业：third_party_cangjie_runtime遗留问题闭环**  
汇报人：李果  
会议结论：  
1、遗留问题闭环后同意third_party_cangjie_runtime仓孵化毕业，可申请QA SIG评审。孵化仓地址为:https://gitcode.com/openharmony-sig/third_party_cangjie_runtime 。  
遗留问题：  
1、删除flatbufferPatch文件，该patch需要打到上游；  
2、平台支持计划，针对ARM32明确在25 Q4支持反射、动态加载高阶功能。  
3、仓库中的大写命名建议修改，给出整改计划。（不阻塞本次毕业）  
4、针对社区运行时与标准库必须随源码构建的基本要求，请着手优化标准库（std）的构建效率，并提交一份包含工作量评估与具体落地计划的方案。  

**议题10、SIG仓申请孵化毕业：third_party_cangjie_tools遗留问题闭环**  
汇报人：张俊  
会议结论：  
1、同意third_party_cangjie_tools仓遗留问题闭环，同意孵化毕业，可申请QA SIG评审。孵化仓地址为:https://gitcode.com/openharmony-sig/third_party_cangjie_tools  
遗留问题：  
无。  
