# 2022年架构SIG例会会议纪要

## 2022-1-11 会议纪要(Notes)

**议题1、全局资源调度子系统resourceschedule准出评审**  
汇报人：徐宽、唐城开  
会议结论：  
1、README、仓简介相关问题整改  
——四个仓均已整改完成。  

2、社区需要机遇RK3568测试  
——基于RK3568已经完成相关用例测试。  

3、用例需要自动化  
——与高涵一对齐后结论如下。  
a) 用例均为重启相关用例，暂时无法自动化，  
330之后系统能力ready再做。  
b) 后续插件加入框架需要内存、处理性能相关的看护。  
c) 后续需要加入更多插件异常的打点日志。  

4、架构相关的修改  
——与强波对齐后结论如下。  
         a) MarkDown表格相关问题整改。  
         b) background_task_mgr目录结构整改。  
该两点均已整改完成。  

**议题2：openharmony-sig/third_party_pyyaml准出评审**  
汇报人：许勇  
会议结论：  
1、问题遗留，需要拉革林及相关专家线下对齐最终引入结论。  

**议题3：openharmony-sig/third_party_benchmark孵化毕业评审**  
汇报人：王俊涛  
会议结论：  
1、未评估，下次过审  

**议题4：useriam_faceauth孵化毕业评审**  
汇报人：刘天石、王旭  
会议结论：  
1、测试：测试情况和测试对齐  
已和高涵一对齐，可以合入主干  
2、UX：完成UX验收  
已和邢文华沟通，因平台原因无法完成UX验收，不影响SIG毕业（Hi3516平台无模拟器、不支持截屏、录屏、无法远程验收；计划给UX同学协调开发版）  
3、UX：与UX确认图片是否开源  
已确认可以开源  
4、文档：README 删除构建信息，按模板修改格式  
文档类问题，已修改，资料同意上master  
5、文档：不要链接到Harmony OS，引导API参考  
同上  
6、文档：doc仓contribute README 模板，按模板修改  
同上  
7、测试：发送xts PR给（高涵一）  
已发送  
8、发送reviewBot扫描结果（邢文华）  
已发送  
9、对齐架构评审遗留问题（强波）  
已对齐架构评审遗留问题  

**议题5：access_tokne孵化毕业评审**  
汇报人：蒋晓峰、陈念  
会议结论：  
1、readme的issue问题闭环  
2、readme的名称修改  
3、仓的简介修改  
4、accesstoken_lib目录名称修改  
5、copy_right的时间以上码云的时间为准  

**议题6：minimp3/minimp4孵化毕业评审**  
汇报人：陈国栋  
会议结论：  
1、三方组件内部加.c文件，独立编译.a，再给其它模块链接。  
2、三方组件内部加BUILD.gn文件，独立编译，并加上三方软件使用的声名。  

**议题7：drivers_interface孵化毕业评审**  
汇报人：袁博  
会议结论：  
1、readme文档约定部分和HDF编程规范统一，不需要重复，链接到HDF编程规范即可；  
2、修改readme中关于hdi-gen工具的描述，对于开发者不需要的概念、工具不需要体现  

**议题8、third_party_libnl孵化毕业评审**  
汇报人：徐赛  
会议结论：  
1、README直接连接到官网  
2、确认源码都没有兼容问题  
3、保留commiter信息  

**议题9、foundation/communication/netmanager_base孵化评审**  
汇报人：张海丰  
会议结论：  
1、网络管理分为网络管理base和网络管理ext仓，无遗留问题。  

**议题10、foundation/communication/netmanager_ext孵化评审**  
汇报人：张海丰  
会议结论：  
1、网络管理分为网络管理base和网络管理ext仓，无遗留问题。  

## 2022-1-18 会议纪要(Notes)

**议题1：openharmony-sig/useriam_coauth,openharmony-sig/useriam_pinauth,openharmony-sig/useriam_userauth,openharmony-sig/useriam_useridm孵化毕业评审**  
汇报人：刘天石  
会议结论：  
1、确认协同认证模块命名是否合理  
已和任革林闭环  
2、执行FOSSBOT扫描，与余甜、邢文华、陈雅旬、董金光对齐  
已和余甜、陈雅旬对齐，发送内部邮件纪要  
3、完善资料图片配色，资料描述  
已完善  

**议题2：security_devicesecuritylevel孵化仓毕业，申请合入OpenHarmony主干**  
汇报人：徐知仁  
会议结论：  
1、签名的的格式建议考虑简化处理，方便oem接入。  
后续在生态推广的签名相关策略上统一考虑。  
2、fossbot在内网重新扫描一次。  
3、知识产权排查联系系刘霖确认  
4、遗留问题闭环后，评审通过。  

**议题3：accessibility申请孵化毕业**  
汇报人：赖癸仲  
遗留问题：  
1、合规风险：联系余甜，从多方面关注合规问题  
架构功能的差异，例如分布式投屏反控等场景；  
功能实现的差异，例如API差异、流程差异；  
可考虑参考业界差异的比例，对比我们与其他的差异比例。  
2、专利风险分析：联系刘霖，关注华为特有特性是否申请专利；特性是否侵犯它人专利  

**议题4：skia申请孵化毕业**  
汇报人：杨光宇  
遗留问题：  
1、AOSP版权需要与法务线下沟通并确认合规问题
2、fossbot内网重新扫描并输出报告结果
3、遗留问题闭环后评审通过

**议题5：杂散子系统打印、下载等部件仓申请孵化毕业**  
汇报人：方忠灿、赵超  
会议结论：  
无。  

**议题6：SIG毕业评审三方开源引入openh264**  
汇报人：朱明亮、黄小龙  
会议结论：  
1、允许OpenH264 孵化毕业。  
遗留问题：  
1、此开源代码使用的License 是否与 BSD 2.0的描述一致，若一致可精简OAT.xml。  

## 2022-1-25 会议纪要(Notes)

**议题1：resourceschedule_memmgr申请孵化毕业**  
汇报人：孙采、陈杰  
会议结论：  
1、oat.xml中删掉代码不涉及的部分--已完成  
2、进行内部FossBot扫描--已完成  
3、readme按issue要求整改--已完成  
4、遗留问题闭环后评审通过  

**议题2：hiviewdfx_hichecker申请孵化毕业**  
汇报人：夏中林、蒋为正  
会议结论：  
1、ohos.build整改--已完成  
2、README_zh字母大写 已完成  
3、仓简介、描述补充  已完成  
4、与测试对齐测试用例 已对齐、补充  
5、新增JS接口评审、补充xts用例  与任革林确认后本次准出不包含js接口相关代码  
6、遗留问题闭环后评审通过  

**议题3： developtools_hapsigner孵化仓毕业，申请合入OpenHarmony主干**  
汇报人：刘志伟、詹泽怡  
会议结论：  
1、oat.xml中删掉不涉及的部分  
2、内部FossBot扫描  
3、架构问题闭环  
4、仓描述刷新  
5、提供测试报告  
6、闭环文档issue  
7、删除readme.md文件（无英文文档）  

**议题4：opensles孵化仓毕业，申请合入OpenHarmony主干**  
汇报人：杨帅  
会议结论：  
1、新增build.gn文件-已完成  
2、notice文件生成-已完成  
3、使用fossboot扫描-已完成  
遗留问题闭环后评审通过  

**议题5、filemanagement_app_file_service仓孵化毕业评审**  
汇报人：潘钦旭  
会议结论：  
1、内部FossBot扫描结果  
2、README_zh字母大写  
3、ohos.build整改  
4、英文readme文件删除  
5、增加oat.xml文件  
6、补充简介  

## 2022-2-8 会议纪要(Notes)

**议题1、MindSpore仓孵化毕业评审**  
汇报人：孙锁东  
会议结论：  
1、仓名mindspore改成third_party_mindspore  
2、保留commit记录  
3、增加Gn编译工程  
4、增加XTS兼容测试用例  

**议题2、frame_aware_sched 仓孵化毕业评审**  
汇报人：师荣堃  
会议结论：  
1、fossboot、静态检查扫描  
2、README_ZH的依赖仓内容补充，设备系统系统开发者是否需要使用评估  
3、测试用例的和tse对齐，同时出具测试报告  
4、OAT通过的扫描结果展示  

**议题3、sig仓developtools_ets_lint_rules，third_party_typescript和third_party_typescript_eslint申请孵化毕业**  
汇报人：李洪、陈功平、刘源、肖义文  
会议结论：  
1、代码补齐  
2、gn文件修改，测试验证  
3、notice文件  
4、专利评估  

**议题4、third_party_openmax仓孵化毕业评审**  
汇报人：孙赫赫  
会议结论：  
1、确认License   ---已确认  
2、确认是否需要增加XTS测试用例 ---不涉及  
3、专利评估   ---只使用头文件，不涉及专利  
4、notice文件   ---仓不参与编译，只有头文件  

**议题5、SIG仓assist_tools-napi_tool申请孵化毕业**  
汇报人：赵军霞  
会议结论：  
1、【assist_tools仓 改为 napi_generator】：上移一层napi_tool目录 --黄明龙、赵军霞 330前合入  
2、修改命令行名为napi_generator，命令行格式增加-h帮助说明（例如版本信息） --赵军霞 330前合入  
3、【修改readme排版】：--赵军霞 330前合入  
1)按优先级排序  
2)增加最低支持的node js api 的版本信息  
3）修改开发说明：改为链接方式、细化开发环境说明（是linux or windows，例如Windows环境无sudo）  
4）删除截图，改为markdown格式  
4、【整改code目录】：参考其他仓 赵军霞 330前合入  
5、【增加prebuilt目录】，存放可执行文件、插件文件 --赵军霞 330前合入  
6、【增加自动化测试用例】--赵军霞、hanyi 330前合入  
7、工具介绍说明集成--黄明龙 330前合入  
8、同步修改community的sig目录信息 --赵军霞 330前合入  
9、命令行 输出格式不光是console,还需要支持xml和json--- 赵军霞 330以后  

## 2022-3-1 会议纪要(Notes)

**议题1、sig仓device_soc_asrmicro、device_board_lango、vendor_asrmicro 申请孵化毕业**  
汇报人：姚少鹏  
会议结论：  
1、提供二进制文件许可 EULA  
2、Soc仓 license 闭环 重新扫描  
3、指导文档 杨妮 重新扫描检查  
4、闭环架构相关问题，由李开龙审核，目前软总线主干代码还没有全部合入，需要等330新版本合入后进行整改，其他代码架构问题全部闭环  

**议题2、sig仓global_timezone、third_party_tzdata申请孵化毕业**  
汇报人：孙耀祖  
会议结论：  
1、参加代码评审  
2、更新oat.xml屏蔽二进制文件  
3、修改脚本文件头部注释中的版权信息  

**议题3、sig仓utils_memory申请孵化毕业**  
汇报人：宋远征  
会议结论：  
1、闭环遗留问题，准出  
遗留问题：  
1、OAT整改：删除不需要的部分  
2、提供测试验证报告结果，邮件发送相关责任人  

**议题4、sig仓msdp_start、msdp_device_status申请孵化毕业**  
汇报人：刘东淼  
会议结论：  
1、闭环遗留问题，准出  
遗留问题：  
1、Readme删除掉 相关仓 一章，当前只有一个仓  
2、测试用例会后和高涵一确认下  

**议题5、sensors_medical_sensor申请孵化毕业**  
汇报人：武和波  
会议结论：  
1、文档有专人在检视，有问题会提issue，直接按issue修改  
2、待上库到master分支之后，会全量跑XTS，覆盖率如果有问题会单独提issue再增加XTS用例即可，此条不影响准出  
3、闭环架构例会遗留问题及其他遗留问题后，同意准出  

**议题6、applications_admin_provisioning申请孵化毕业**  
汇报人：李恒  
会议结论：  
1、闭环遗留问题，准出  
遗留问题：
1、readme资料相关仓和资料对齐修改  
2、设备管理方案和架构对齐，已经内部邮件对齐  
3、UX同意准出的结论，已经内部邮件对齐  
4、测试同意准出的结论，已经内部邮件对齐  

**议题7、third_party_libexif申请孵化毕业**  
汇报人：张晓波  
会议结论：  
1、闭环遗留问题后准出  
遗留问题：
1、加入版本火车 （完成） 
   确认当前的开源的版本火车中包含有libexif  
2、対齐项目许可证LGPL-2.1是否有风险。（完成）  
   与陈雅旬已対齐，并完成OAT.xml整改  
3、参与下周架构sig例会评审。(完成)  
   已通过架构评审。  
4、试内容対齐，提交功能测试结果。（完成）  
   与高涵一対齐测试措施，已提供测试结果。  
5.build.gn 文件声明整改 （完成）  
   已修改上库：https://gitee.com/openharmony-sig/third_party_libexif/pulls/2  

**议题8、global_resource_tool 申请孵化毕业**  
汇报人：陈程  
会议结论：  
1、暂时不准出  
遗留问题：  
1、readme 需求修改。  
2、架构sig评审，需要整改编译使用的工具链。  

**议题9、distributed_hardware_fwk申请孵化毕业**  
汇报人：张创  
会议结论：  
1、准出材料无问题，闭环遗留问题，准出  
遗留问题：  
1、需要在PMC架构sig例会评审  

## 2022-3-7 会议纪要(Notes)

**议题1、hiviewdfx_hidumper申请孵化毕业**  
汇报人：夏中林、蒋为正  
会议结论：  
1、闭环遗留问题后准出  
遗留问题：  
1、专利评审通过  
2、法务评审通过(比较功能差异) --已与法务对齐，无风险  
3、xts用例对齐 --已对齐，xts用例不用上，后续补充本模块下用例即可  
4、readme按需求修改  

**议题2、enterprise_device_management申请孵化毕业**  
汇报人：蔡明港  
会议结论：  
遗留问题闭环后准出  
准出后XTS的合入规则和纪永下来对齐  

**议题3、developtools_syscap_codec申请请孵化毕业**  
汇报人：裴太乙  
会议结论：  
1、遗留问题闭环后准出  
遗留问题：  
1、解决README相关的ISSUE， 并删除当前未实现的文件说明  
2、与测试对齐测试结果和测试方法  

**议题4、distributed_camera、distributed_screen仓申请孵化毕业**  
汇报人：张创  
会议结论：  
1、不同意准出，待内部遗留问题解决，代码发布到sig仓后再次评审  

**议题5、global_resource_tool 申请孵化毕业**  
汇报人：陈程  
会议结论：  
1、解决遗留问题后可以准出。  
遗留问题：  
1、添加测试用例  
2、修改readme  
3、third_party 目录名字与架构讨论是否适合叫这个名字  

**议题6、dcts申请孵化毕业**  
汇报人：李昊、宋大伟  
会议结论：  
1、同意准出。  

## 2022-3-9 会议纪要(Notes)

**议题1：SIG Communication-NFC**  
汇报人：张秀平  
会议结论：  
1、解决遗留问题后准出。  
遗留问题：  
1、readme文档、仓描述更新、增加简介、新增OAT.xml  
2、部件架构评审任革林的评审会议上遗留问题，和革林闭环。  
3、敏感词扫描扫描列表为空，会后找邢文华再确认下。  

**议题2：base_location仓申请孵化毕业，申请在master建仓**  
汇报人：刘彬俊  
会议结论：  
1、解决遗留问题后可以准出。  
遗留问题：  
1、oat xml提交PR合入  
2、架构图修改下，让yangni评审下  
3、oat扫描问题闭环  
4、需要确认下XTS用例代码是否有上库到蓝区。  

**议题3：applications_filepicker仓申请孵化毕业**  
汇报人：陈佳乐  
会议结论：  
1、遗留问题解决后准出。  
遗留问题：  
1、png图片文件找UX同事看看是否有版权问题 -- 已和UX确认没问题
2、OAT扫面的问题闭环，并将OAT.xml文件合入到代码仓；README的文档需要闭环 --OAT文件，README文件已闭环  
3、专利问题找刘霖对齐  
4、测试用例找高涵一对齐 -- 已和高涵一对齐无问题  
5、代码仓中的gradle/wrapper删除 -- 已删除  

**议题4：applications_notes仓申请孵化毕业**  
汇报人：朱鸿  
会议结论：  
1、解决遗留问题后准出。  
遗留问题：  
1、readme文档、仓描述更新  
2、更新OAT.xml  
3、代码完成合规扫描  
4、内部拉架构评审会议  

**议题5：distributed_camera、distributed_screen仓申请孵化毕业**  
汇报人：张创  
会议结论：  
1、解决遗留问题后准出。  
遗留问题：  
1、门禁问题处理完毕  
2、提供测试报告  
3、代码合入sig仓后完成合规扫描  

**议题6：sig仓applications_settings_data，applications_screenlock，applications_screenshota，applications_theme申请孵化毕业**  
汇报人：苏鹏  
会议结论：  
1、解决遗留问题后准出。  
遗留问题：
1、README文档issue闭环  
2、仓描述更新  
3、内部拉架构评审会议  

## 2022-3-11 会议纪要(Notes)

**议题1：miscservices_wallpaper、miscservices_screenlock、miscservices_download、miscservices_pasteboard申请孵化毕业**  
汇报人：方忠灿  
会议结论：  
1、遗留问题闭环后准出。  
遗留问题：  
1、需补齐XTS用例，保障兼容性接口正常  
2、跟踪完成架构SIG评审  

**议题2：sig仓third_party_cef、web_webview、third_party_chromium申请孵化毕业**  
汇报人：李征、陈震南  
会议结论：  
1、遗留问题闭环后，同意准出。  
遗留问题：  
1、webview代码仓中的头文件目录整改。   --责任人： 李征 闭环时间：2022.3.11  
2、webview代码仓文件的copyright和license整改。 --责任人： 李征 闭环时间：2022.3.11  

## 2022-3-17 会议纪要(Notes)

**议题1：sig仓 filemanagement_fs_tools申请孵化毕业**  
汇报人：张文迪  
会议结论：  
1、暂不准出。  

**议题2：sig仓vendor_chipsea,device_board_chipsea,device_soc_chipsea申请孵化毕业**  
汇报人：郝波  
会议结论：  
1、在readme中把xts测试和正常产品的编译说清楚。  
2、hdf适配合入到公共仓。等准出后找OWNER合入到主仓。  
3、授权合规问题。   
4、二进制开源问题要先有结论。  

**议题3：SIG 仓hypium、wukong申请孵化毕业**  
汇报人：任熠、戴伟琦  
会议结论：  
1、遗留问题闭环后准出。  
遗留问题：  
1、资料均需修改，考虑先从开发者使用视角和贡献视角触发，说明工具或框架如何被开发者使用--已同杨妮评审通过，同意闭环  
2、测试框架需补充oat.xml--已提交闭环  

**议题4：sig仓device_soc_st、device_board_bearpi、vendor_bearpi申请孵化毕业**  
汇报人：王城  
会议结论：  
1、二进制文件需要尽量开源  
2、合规问题确认，问题一闭环后再整体扫描  
3、开发板由于疫情未投递，待投递及闭环门禁流水线搭建  
4、xts测试报告邮件抄送给纪永和邢文华同步  
5、等问题一闭环后，再上QA例会进行说明  
6、文档由杨妮审核，无问题后相关问题闭环  

**议题5：SIG仓三方代码仓tizen申请作为正式仓**  
汇报人：张海丰、李洪进  
会议结论：  
1、不需要新建三方仓，在sms_mms仓内自研化整改  

## 2022-3-31 会议纪要(Notes)

**议题1、sig仓vendor_hihope、device_board_hihope、device_soc_winnermicro孵化毕业申请**  
汇报人：屈博  
会议结论：  
1、遗留问题闭环后转出  
遗留问题：  
1、SOC仓代码版权声明问题，和厂商沟通按照开源规范增加版权头和声明  
2、SOC仓二进制库提供许可  
3、二进制库需要评审专家统一审视提供意见决策并反馈  

**议题2、sig仓device_soc_st、device_board_bearpi、vendor_bearpi孵化毕业申请**  
汇报人：王城  
会议结论：  
1、遗留问题闭环后准出。  
遗留问题：  
1、开龙合并kernel_liteos_a的PR：https://gitee.com/openharmony/kernel_liteos_a/pulls/865  
2、基金会后期设立二进制延迟开源规则，不影响本次准出  
3、纪永确认NFS测试项是否通过  

**议题3、sig仓device_soc_allwinner、device_board_seed、vendor_seed孵化毕业申请**  
汇报人：刘召勤  
会议结论：  
1、遗留问题闭环后准出。  
遗留问题：  
1、二进制文件开源问题开会讨论  
2、Board仓代码版权修改  -- 已经整改完成  
3、显示/camera问题解决  

**议题4、sig仓vendor_chipsea, device_board_chipsea, device_soc_chipsea申请孵化毕业**  
汇报人：郭超胜、郝波  
遗留问题：  
1、三个库的issue闭环处理。  

**议题5、sig仓vendor_talkweb, device_board_talkweb, device_soc_st申请孵化毕业**  
汇报人：候鹏飞、方烨  
遗留问题：  
1、协商解决xts module_ActsSamgrTest测试套件栈溢出的问题。  
2、二进制承诺2个月内开源代码  
3、架构例会相关遗留事项闭环  

## 2022-4-12 会议纪要(Notes)

**议题1、sig仓third_party_libwebsockets申请孵化毕业**  
汇报人：毛思平  
会议结论：  
遗留问题：  
1、使用不到的文件涉及LGPL/GPL许可证，是删除还是加入OAT屏蔽，拉上法务再确认一次。  

遗留问题已闭环，未使用的文件不需要删除，无许可证风险。  

**议题2、sig仓申请孵化毕业msdp_spatial_awareness、msdp_motion、msdp_movement、msdp_timeline、msdp_geofence**  
汇报人：彭红星、侯朋飞、刘东淼  
会议结论：  
1、以下遗留问题闭环后准出。  
遗留问题：  
1、资料问题闭环：Readme的issue、代码仓简介  
2、拿到sig架构同意结论  
ps：发准出闭环邮件时，将测试报告作为附件贴上  

## 2022-5-10 会议纪要(Notes)

**议题1、sig仓申请孵化毕业device_cert_sdk**  
汇报人：高博、王纪睿  
会议结论：  
1、与架构SIG沟通具体孵化出仓具体要求，达标后再出仓  
2、闭环QA会议遗留问题  
1）编译脚本拆分frameworks和pals  
2）代码目录readme补充完善，找杨妮评审  

**议题2、sig仓申请孵化毕业third_party_mesa3d**  
汇报人：张雷宇、林洪亮  
会议结论：  
1、遗留问题闭环后准出。  
遗留问题：  
1、lisence问题和余甜再次确认  
2、编译时增加一个参数传递到GN，直接修改代码方式不友好  

**议题3、sig仓申请孵化毕业distributeddatamgr_data_share**  
汇报人：宋瑞瑞、徐大庆  
会议结论：  
1、遗留问题闭环后准出。  
遗留问题：  
1、readme与杨妮确认，问题闭环  
2、拿到sig架构同意结论  

**议题4、sig仓申请孵化毕业third_party_exfatprogs**  
汇报人：宁左斌、潘钦旭  
会议结论：  
1、遗留问题闭环后准出。  
遗留问题：  
1、支持修复exfat中的错误，linux-5.7内核更新疑问  
2、LTS3.1 Release版本 exfatEOM软件漏洞维护方法  
3、补充仓名描述  
2.拿到sig架构同意结论  

## 2022-6-1 会议纪要(Notes)

**议题1、sig仓申请孵化毕业，third_party_iptables**  
汇报人：毛思平  
会议结论：  
1、软件使用申请(OK)  
2、义务履行等checklist项补充(OK)  
3、SPDX单独下会后单独确认(2的补充)(没有使用带有SPDX协议的文件，不涉及)  
4、补充README  
5、补充bundle.json  

**议题2、sig仓申请孵化毕业device_soc_telink、device_board_telink、vendor_telink**  
汇报人：刘杰  
遗留问题：  
1、文件整理，二进制是否有必要存在  
2、文档内容闭环issue  
3、和少峰下面对一下，交叉编译工具的事情。  
托管到云端，赵鹏。安光林。  
需要进行放进去openharmony社区，并涉及到相关许可。  
4、XTS测试master，确认纪永  
5、测试用例确认-高涵一  
6、和少峰老师确认一下开发板的功能和结构，拿到结论  

**议题3、sig仓申请孵化毕业notification_eventhandler**  
汇报人：李强、陈理恩  
会议结论：  
无。

**议题4、sig仓申请孵化毕业，third_party_alsa-lib、third_party_alsa-utils**  
汇报人：张云虎  
会议结论：  
1、同意准出。  
遗留问题：  
1、有COPYING文件是否可以不添加LICENCE文件——已确认可以并添加，将COPYING文件在README.OpenSource中声明即可。  
2.、通过BUILD.gn生成Notice.txt——已添加  

## 2022-6-14 会议纪要(Notes)

**议题1、sig仓申请孵化毕业，ability_form_runtime、ability_ability_base、ability_idl**  
汇报人：徐承桦、丁瑶  
会议结论：  
1、同意准出。  
遗留问题：  
1、ability_form_fwk仓删除diff，init等多余文件，yaml文件整改；  
2、所有仓检查补充OTA.xml配置，并刷新仓描述；  
3、readme与杨妮确认，issue问题闭环；  
4、测试用例与高涵一确认；  
5、与测试TSE程星振确认分仓影响；  

**议题2、sig仓申请孵化毕业device_soc_nxp、device_board_osware、vendor_osware**  
汇报人：赵秀成  
会议结论：  
1、同意准出  
遗留问题：  
1、根据issue修改readme  
2、提uboot相关issue  

## 2022-6-28 会议纪要(Notes)

**议题1、sig仓申请孵化毕业device_soc_amlogic、device_board_unionman、vendor_unionman**  
汇报人：于敏杰  
会议结论：  
1、遗留问题闭环后准出。  
遗留问题：  
1、代码双协议问题处理，与少锋确认；  
2、readme相关issue问题闭环；  
3、master版本的XTS测试与纪勇确认；  

**议题2、sig仓申请孵化毕业device_soc_rockchip、device_board_lockzhiner、vendor_lockzhiner**  
汇报人：王小彬  
会议结论：  
1、遗留问题闭环后准出；  
遗留问题：  
1、board_lockzhiner有中等版权风险。  
已经解决。已经删除有风险的第三方库。  
2、二进制文件需和rockchip协商。  
二进制文件是瑞芯微的核心代码，非我方代码，瑞芯微不让公开。  
3、md说明文档要完善。  
已修改完成。截止2022年6月30日17:01，md说明文档没有新的问题。  

**议题3、扬帆sig仓申请孵化毕业device_soc_rockchip、device_board_isoftstone、vendor_isoftstone**  
汇报人：庞伟  
会议结论：  
1、遗留问题闭环后准出。  
遗留问题：  
1、board、Vendor、Soc仓整改，README的Issue需要闭环  
已经整改，Board、Vendor、Soc仓，Issue已闭环  
2、涉及GPL协议，修改为双协议头  
已经解决  
3、3399的显示需要解决  
已经解决  
4、XTS需要提供报告  
正在整理  
5、杨帆开发板需要投递  
正在安排投递  
6、EULA.txt文件名需要同步修改为EULA  
已经解决，上传到SIG仓  
7、编译问题  
已经解决，目录调整完成  

**议题4、致远sig仓申请孵化毕业device_soc_allwinner、device_board_isoftstone、vendor_isoftstone**  
汇报人：庞伟  
会议结论：  
1、遗留问题闭环后准出。  
遗留问题：  
1、Bluetooth/网卡硬件不支持，需要与少峰再确认一下是否可以上主干  
已闭环  
2、README的ISSUE问题需要修改  
已闭环  
3、XTS的需要提供纪永的反馈结果  
已闭环  
4、涉及GPL协议，修改为双协议头  
已闭环  
5、软通动力申报的议题需要分开，分为扬帆开发板QA评审和致远开发板QA评审  
已闭环  

## 2022-7-12 会议纪要(Notes)

**议题1、sig仓申请孵化毕业third_party_llvm-project、third_party_lldb-mi**  
汇报人：李文韬  
会议结论：  
1、同意准出  
遗留问题(不阻塞准出）：
1、已确认build_musl.sh编译过程中对轻设备富设备已进行了区分  
2、确认官方NOTICE归档流程  

**议题2、sig仓申请孵化毕业third_party_mimalloc**  
汇报人：陈杰  
会议结论：  
1、架构SIG和QA SIG遗留问题闭环后，同意仓库third_party_mimalloc毕业。  
架构SIG遗留问题：  
1、会后按照选型模板整理材料后与董金光对齐选型流程  
QA SIG遗留问题：  
1、补全BUILD.gn文件  
2、提供稳定性压测报告  

## 2022-8-9 会议纪要(Notes)

**议题1、sig仓申请孵化毕业device_soc_esp、device_board_openvalley、vendor_openvalley**  
汇报人：方烨  
会议结论：  
无。

## 2022-8-16 会议纪要(Notes)

**议题1、sig仓申请孵化毕业arkcompiler_toolchain**  
汇报人：余美杰  
会议结论：  
1、同意准出。  
遗留问题：  
1、README需要更新一下，修改意见已提issue跟踪  

**议题2、sig仓申请孵化毕业third_party_elfio**  
汇报人：毛思平  
会议结论：  
1、遗留问题已闭环，允许准出  

## 2022-8-30 会议纪要(Notes)

**议题1、sig仓申请孵化毕业device_board_kaihong、device_soc_rockchip、vendor_kaihong**  
汇报人：王成  
会议结论：  
1、遗留问题闭环后准出。  
遗留问题：  
1、REAEME的ISSUE问题需要修改  
已修改  
2、XTS结果需要纪永确认  
已确认  

**议题2、sig仓申请孵化毕业third_party_vulkan**  
汇报人：张召  
会议结论：  
1、架构SIG遗留问题闭环后，同意仓库third_party_vulkan-headers准出。  

**议题3、sig仓申请孵化毕业opencl-headers**  
汇报人：陈旭  
会议结论：  
1、闭环遗留问题后准出  
遗留问题：  
1、README需要更新一下，修改意见已提issue跟踪  
---已更新中文指导  
2、wrapper.so的NOTICE自动生成  
---已经确认包含，构建的时候会自动扫描的LICENSE文件，然后合并到/system/etc/NOTICE.txt  
3、原有测试用例覆盖  
---添加BUILD.gn构建出原测试程序可以执行  

## 2022-9-9 会议纪要(Notes)

**议题1、sig仓申请孵化毕业 sys_installer**  
汇报人：胡振  
会议结论：  
1、同意准出  
遗留问题：
1、README需要更新一下，修改意见已提issue跟踪  

**议题2、sig仓申请孵化毕业 crypto_framework**  
汇报人：吕元民  
会议结论：  
1、同意准出  
遗留问题：
1、README需要更新一下，修改意见已提issue跟踪  

## 2022-9-14 会议纪要(Notes)

**议题1、sig仓申请孵化毕业kernel_uniproton、vendor_alientek**  
汇报人：陈炜  
遗留问题：  
1、UniProton 是否作为三方软件引入，对齐拿到结论？  
     已三方库的形式引入  
2、找明龙协助拿到每日构建扫描报告？  
     已拿到报告  
3、README中介绍一下和OH关系以及价值？  
4、基础内核 + hdf xts测试用例报告？  
5、kernel_uniproton 仓许可证决策？  
法律上三个license都没问题，选那个都可以先定社区策略(扩展内核放UniProton基础内核还是OpenHarmony社区)，再决定使用那个LICENSE  
6、不建立内核仓，编译时如何把内核结果拿过来？  
  推动UniProton 支持GN编译  
7、从liteos里面拿过来的代码使用什么许可证？  
   从liteos里面拿过来的代码是可以重新定义许可证的 -- relicense,可以从BSD许可证变成Apache，但需要做来源说明  
8、API文档 --- 对外接口文档 和 用户指南  
   没修改他们的直接使用他们的链接  

## 2022-9-27 会议纪要(Notes)

**议题1、sig仓申请孵化毕业av_session**  
汇报人：王俊涛  
会议结论：  
无。  

**议题2、sig仓申请孵化毕业security_privacy_center、security_certificate_manager**  
汇报人：刘志伟、詹泽怡  
会议结论：  
1、闭环遗留问题后准出  
遗留问题：  
1、自提issue跟踪 API延迟交付事项 - 已闭环，已在SIG仓自提issue跟踪  
2、readme刷新 -已闭环，已更新readme  
3、API演进兼容和C资料问题需要在周三会上评审 - 已闭环 不涉及C资料  

**议题3、sig仓申请孵化毕业kernel_uniproton、vendor_alientek**  
汇报人：陈炜  
会议结论：  
1、同意准出，闭环遗留问题  
遗留问题：  
1、README讲清楚和OpenEuler的关系，那些属于上游？怎么贡献？ --- 已提issue跟踪  
2、BUILD.gn里面能够生成NOTICE  --- 已闭环  
3、添加OpenSource                         --- 已闭环  
4、xts测试报告找高涵一确认            --- 已闭环  
5、专利找刘霖对齐                            --- 已闭环  

**议题4、sig仓申请孵化毕业communication_sfc_newip**  
汇报人：谭延营、樊晓宇、马尔利  
会议结论：  
1、闭环遗留问题后准出  
遗留问题：  
1、【已闭环】license文件以及代码文件头去掉“NewIP is dual licensed: you can use it under the terms of the GPL V2 and the BSD2 license”相关描述，只在项目仓根目录license文件中描述每个路径的license即可。  
2、【已闭环】只保留根目录license文件，去掉子目录license文件。  
3、【已闭环】NewIP是网络5.0联盟共同推出的新协议，属于公共，建议公共代码license使用BSD-3，不要使用BSD-2。liteOS是BSD-3，如果用BSD-2，属于反向使用。  
4、【已闭环】linux目录增加README.OpenSource，相当于NewIP引用Linux内核第三方软件的形式，参考鸿蒙社区Linux-5.10内核仓README.OpenSource。  
5、【已闭环】参考多个V4/V6文件(不同GPL license)新生成的newip文件license定义合规问题，发给余甜律师帮确认。  
6、【已闭环】社区后面建立好漏洞故障树后，将newip仓和故障树进行关联，新建issue长期跟踪。  
7、【已闭环】线下和测试对齐测试用例如何覆盖，参考V4/V6方法拉齐。与Test SIG负责人高涵一讨论同意提issue跟踪，持续构建，不阻塞sig转正。  
     裁决依据：NewIP内核协议栈首次落地，目前暂无第三方厂商使用，风险可控。  

## 2022-10-11 会议纪要(Notes)

**议题1、sig仓申请孵化毕业av_session**  
汇报人：张斌  
会议结论：  
无。  

**议题2、sig仓申请孵化毕业(2022.9.27遗留问题评审闭环)communication_sfc_newip**  
汇报人：谭延营、樊晓宇、马尔利  
会议结论：  
1、遗留问题都已闭环。  

## 2022-10-14 会议纪要(Notes)

**议题1、sig仓申请孵化毕业device_soc_hpmicro、device_board_hpmicro、vendor_hpmicro**  
汇报人：霍宏鹏、施灵峰  
遗留问题：  
1、先楫需要提供命令行下载工具，供鸿蒙实验室做自动化测试，整改期限一个月，不影响合主干。  
结果：开发中，计划11.14日开发完成  
2、先楫目前提供的图形化下载工具，提供给华为托管，供开发者下载使用，先楫需要相关签署协议。后续由华为的李兵跟踪。  
结果：  
下载工具可以在gitee 公开下载https://gitee.com/hpmicro/hpmprogrammmer/releases/download/v0.2.0/HPMProgrammmer_v0.2.0.zip  
在下载的工具包含有这份license。允许按照这份license 分发这工具，license见附件。  
3、目前先楫SDK的协议头有多种书写格式，合主干前需要进行统一。.OAT.xml许可扫描配置文件，删除掉无用的配置项。  
结果：  
已经将先楫SDK中所有源码统一为1种格式；  
OAT.xml无用的配置项已经删除；  

## 2022-10-25 会议纪要(Notes)

**议题1、sig仓申请孵化毕业smartperf**  
汇报人：高曦、戴松岭  
会议结论：  
1、同意新建device_soc_renesas sig孵化仓。  
遗留问题：  
无。  

**议题2、sig仓申请孵化毕业device_board_beken、device_soc_beken、vendor_beken**  
汇报人：涂文星、林万顷  
遗留问题及闭环  
1、统一许可证（包括MIT等修改）  
        https://gitee.com/openharmony-sig/device_soc_beken/pulls/17  
        https://gitee.com/openharmony-sig/device_board_beken/pulls/17  
        https://gitee.com/openharmony-sig/vendor_beken/pulls/15  
2、OAT.xml精简  
        https://gitee.com/openharmony-sig/device_soc_beken/pulls/18  
        https://gitee.com/openharmony-sig/device_board_beken/pulls/18  
        https://gitee.com/openharmony-sig/vendor_beken/pulls/16  
3、EULA  
我司法务同事，会审核我们提供的EULA。在此之前，我们提供的静态二进制文件，请放心使用，也不限制传播。  

**议题3、sig仓申请孵化毕业device_board_isoftstone、device_soc_loongson、vendor_isoftstone**  
汇报人：庞伟  
会议结论：  
1、遗留问题待闭环。  

## 2022-11-8 会议纪要(Notes)

**议题1、sig仓申请孵化毕业 neural_network_runtime**  
汇报人：杨永杰  
会议结论：  
1、刷新资料问题后同意准出。  

**议题2、sig仓申请孵化毕业third_party_VK-GL-CTS、third_party_SPIRV-Tools、third_party_spirv-headers、third_party_glslang**  
汇报人：张雷宇  
会议结论：  
1、补充合规扫描报告后补充评审意见。  

## 2022-11-22 会议纪要(Notes)

**议题1、sig仓申请孵化毕业third_party_libbpf**  
汇报人：夏中林  
会议结论：  
1、遗留问题闭环之后准出。  
遗留问题：  
1、bundle.json/README.OpenSource全部用 BSD license  
2、build.gn增加生成开源使用声明  
3、OAT.xml修改策略，去掉屏蔽项  

**议题2、sig仓申请孵化毕业print_print_fwk**  
汇报人：曾旻  
会议结论：  
1、问题闭环后同意准出。

**议题3、sig仓申请孵化毕业xts_device_attest、xts_device_attest_lite**  
汇报人：刘勋  
会议结论：  
1、README同步更新，同意准出。  
