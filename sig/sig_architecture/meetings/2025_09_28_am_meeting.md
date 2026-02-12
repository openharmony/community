# 架构SIG例会 2025-09-28 10:00-12:00(UTC+08:00)Beijing

## 议题(Agenda)

议题1：SIG仓申请孵化毕业：testfwk_testfwk_cangjie_wrapper  
议题2：SIG仓申请孵化毕业：arkweb_arkweb_cangjie_wrapper  
议题3：SIG仓申请孵化毕业：security_security_cangjie_wrapper  
议题4：SIG仓申请孵化毕业：sensors_sensors_cangjie_wrapper  
议题5：SIG仓申请孵化毕业：communication_communication_cangjie_wrapper  
议题6、SIG仓申请孵化毕业：distributeddatamgr_distributeddatamgr_cangjie_wrapper  

## 与会人(Attendees)

任革林 [@im-off-this-week](https://gitcode.com/im-off-this-week)  
董金光 [@dong_jinguang](https://gitcode.com/dong_jinguang)  

## 会议纪要(Notes)

**议题1、SIG仓申请孵化毕业：testfwk_testfwk_cangjie_wrapper**  
汇报人：焦阳  
会议结论：  
1、遗留问题闭环后同意testfwk_testfwk_cangjie_wrapper仓孵化毕业，孵化仓地址为：https://gitcode.com/openharmony-sig/testfwk_testfwk_cangjie_wrapper。  
遗留问题：  
1、架构图接口层改为“UI测试框架接口”。  
2、对依赖组件init组件的描述需要补充系统参数如何配置。  
3、确认是否支持键盘能力，并在接口层描述中补充。  
4、接口层描述中补充WindowFilter的常见属性。  
5、接口层描述中需要说明Driver和Component功能差异。  
6、补充findComponent相关信息。  

**议题2、SIG仓申请孵化毕业：arkweb_arkweb_cangjie_wrapper**  
汇报人：张睿鸣  
会议结论：  
1、遗留问题闭环后同意arkweb_arkweb_cangjie_wrapper仓孵化毕业，孵化仓地址为：https://gitcode.com/openharmony-sig/arkweb_arkweb_cangjie_wrapper。  
遗留问题：  
1、接口层描述需要对历史信息列表进一步补充包含具体的内容。  
2、接口层描述需要对Cookie管理进一步补充包含的具体内容。  

**议题3、SIG仓申请孵化毕业：security_security_cangjie_wrapper**  
汇报人：罗明  
会议结论：  
1、遗留问题闭环后同意security_security_cangjie_wrapper 仓孵化毕业，孵化仓地址为：https://gitcode.com/openharmony-sig/security_security_cangjie_wrapper。  
遗留问题：  
1、简介部分仓的功能描述需要进一步优化。  
2、readme中架构图说明部分加解密算法列清楚具体加解密算法，密钥管理功能介绍中，按照完整、统一、安全粒度介绍清楚。  
3、readme中使用说明部分将“加解密算法基础功能接口”改为“加解密算法库框架接口”，排查同类问题，资料和代码、API接口一致性。  
4、排查bundle.json中的syscap。  

**议题4、SIG仓申请孵化毕业：sensors_sensors_cangjie_wrapper**  
汇报人：邵一帆  
会议结论：  
1、遗留问题闭环后同意sensor_sensor_cangjie_wrapper仓孵化毕业，孵化仓地址为：https://gitcode.com/openharmony-sig/sensor_sensor_cangjie_wrapper。  
遗留问题：  
1、readme中接口层描述需要列举支持传感器列表。  
2、readme中补充获传感器的具体信息。  
3、readme中约束部分对地磁相关功能的约束描述需要统一。  

**议题5、SIG仓申请孵化毕业：communication_communication_cangjie_wrapper**  
汇报人：罗明  
会议结论：  
1、遗留问题闭环后同意communication_communication_cangjie_wrapper仓孵化毕业，孵化仓地址为：https://gitcode.com/openharmony-sig/communication_communication_cangjie_wrapper。  
遗留问题：  
1、仓库名不要叫“分布式软总线”，跟仓的具体功能相匹配。  
2、接口层描述中增加"fd"等数据类型，并对基础类型列举具体范围。  
3、约束部分“传输的数据量最大约为1MB”需要明确具体规格。  
4、按使用场景补充使用指南，包括具体的场景及示例。  
5、仓颉整体的架构设计在开发普适性方面需要进一步审视和优化。  

**议题6、SIG仓申请孵化毕业：distributeddatamgr_distributeddatamgr_cangjie_wrapper**  
汇报人：焦阳  
会议结论：  
1、遗留问题闭环后同意distributeddatamgr_distributeddatamgr_cangjie_wrapper仓孵化毕业，孵化仓地址为：https://gitcode.com/openharmony-sig/distributeddatamgr_distributeddatamgr_cangjie_wrapper。  
遗留问题：  
1、接口层描述补充数据共享谓词提供的作用，以及其特殊性。  
2、接口层描述补充数据集具体的结构和目的。  
3、接口层需要清晰的描述为开发者提供了哪些能力。  
4、bundle.json文件中删除重复的syscap。  
