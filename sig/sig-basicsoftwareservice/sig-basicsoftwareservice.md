# SIG_BasicSoftwareService 
English | [简体中文](./sig-basicsoftwareservice_cn.md)

Note: The content of this SIG follows the convention described in OpenHarmony's PMC Management Charter [README](/zh/pmc.md).

## SIG group work objectives and scope

### Work Goals
Provide simple and effective Basic Software Services for Open Harmony Operating System; By modular design, Basic Software Services can support various kinds of devices, scaling from Level 0 to Level 5.

### Work Scope
Basic Software Services includes the following sub-systems:
| Name|Explanation|
| :----- | :----- |
|Startup System|Booting OpenHarmony, and provide init process manager and system parameters for the whole system|
|Upgrade System|Provide Operating System upgrade capability|
|DFX System|Design-for-Test, Design-for-Reliability and Design-for-Manufacturing|
|Event Notification System|Manage system and application notifications|
|Resource Management System|Manage system resources, including CPU, IO and memory，Background task manager，Workscheduler|
|Distributed Scheduling System|Scheduing Abilities in Open Harmony distributed network|
|Account Management System|Manage user accounts for Open Harmony|
|Barrier Free System|Provide barrier free common capabilities for Open Harmony|
|Miscellaneous Software System|Provide some miscellaneous services for Open Harmony|

## The repositories

|Subsystem|Repository|Code Path|Owner|
| :----- | :----- | :----- | :----- |
|HiviewDFX|[hiviewdfx_hievent_lite](https://gitee.com/openharmony/hiviewdfx_hievent_lite)|base/hiviewdfx/hievent_lite|[stesen](https://gitee.com/stesen)|
|HiviewDFX|[hiviewdfx_hilog_lite](https://gitee.com/openharmony/hiviewdfx_hilog_lite)|base/hiviewdfx/hilog_lite|[stesen](https://gitee.com/stesen)|
|HiviewDFX|[hiviewdfx_hiview_lite](https://gitee.com/openharmony/hiviewdfx_hiview_lite)|base/hiviewdfx/hiview_lite|[stesen](https://gitee.com/stesen)|
|HiviewDFX|[third_party_curl](https://gitee.com/openharmony/third_party_curl)|third_party/curl|[stesen](https://gitee.com/stesen)|
|HiviewDFX|[third_party_nghttp2](https://gitee.com/openharmony/third_party_nghttp2)|third_party/nghttp2|[zhuwenchao](https://gitee.com/xautosoft)|
|netmanager|[third_party_libwebsockets](https://gitee.com/openharmony-sig/third_party_libwebsockets)|third_party/libwebsockets|[zhuwenchao](https://gitee.com/xautosoft)|
|netmanager|[third_party_iptables](https://gitee.com/openharmony-sig/third_party_iptables)|third_party/iptables|[zhuwenchao](https://gitee.com/xautosoft)|
|netmanager|[third_party_libmnl](https://gitee.com/openharmony-sig/third_party_libmnl)|third_party/libmnl|[zhuwenchao](https://gitee.com/xautosoft)|
|netmanager|[third_party_libnetfilter_conntrack](https://gitee.com/openharmony-sig/third_party_libnetfilter_conntrack)|third_party/libnetfilter/conntrack|[zhuwenchao](https://gitee.com/xautosoft)|
|netmanager|[third_party_libnfnetlink](https://gitee.com/openharmony-sig/third_party_libnfnetlink)|third_party/libnfnetlink|[zhuwenchao](https://gitee.com/xautosoft)|
|netmanager|[third_party_libnftnl](https://gitee.com/openharmony-sig/third_party_libnftnl)|third_party/libnftnl|[zhuwenchao](https://gitee.com/xautosoft)|
|HiviewDFX|[hiviewdfx_faultloggerd](https://gitee.com/openharmony/hiviewdfx_faultloggerd)|base/hiviewdfx/faultloggerd|[maplestorys](https://gitee.com/maplestorys)|
|HiviewDFX|[hiviewdfx_hiappevent](https://gitee.com/openharmony/hiviewdfx_hiappevent)|base/hiviewdfx/hiappevent|[stesen](https://gitee.com/stesen)|
|HiviewDFX|[hiviewdfx_hilog](https://gitee.com/openharmony/hiviewdfx_hilog)|base/hiviewdfx/hilog|[stesen](https://gitee.com/stesen)|
|HiviewDFX|[hiviewdfx_hisysevent](https://gitee.com/openharmony/hiviewdfx_hisysevent)|base/hiviewdfx/hisysevent|[yaomanhai](https://gitee.com/yaomanhai)|
|HiviewDFX|[hiviewdfx_hiview](https://gitee.com/openharmony/hiviewdfx_hiview)|base/hiviewdfx/hiview|[maplestorys](https://gitee.com/maplestorys)|
|HiviewDFX|[third_party_libunwind](https://gitee.com/openharmony/third_party_libunwind)|third_party/libunwind|[maplestorys](https://gitee.com/maplestorys)|
| HiviewDFX           | [hiviewdfx_blackbox](https://gitee.com/openharmony/hiviewdfx_blackbox) | base/hiviewdfx/blackbox                           |[stesen](https://gitee.com/stesen)|
| HiviewDFX           | [hiviewdfx_hidumper_lite](https://gitee.com/openharmony/hiviewdfx_hidumper_lite) | base/hiviewdfx/hidumper_lite                      | [stesen](https://gitee.com/stesen)           |
| HiviewDFX           | [hiviewdfx_hitrace](https://gitee.com/openharmony/hiviewdfx_hitrace) | base/hiviewdfx/hitrace                            | [yaomanhai](https://gitee.com/yaomanhai)     |
| HiviewDFX           | [hiviewdfx_hicollie](https://gitee.com/openharmony/hiviewdfx_hicollie) | base/hiviewdfx/hicollie                           | [ericlee](https://gitee.com/ericlee)         |
| HiviewDFX           | [third_party_ejdb](https://gitee.com/openharmony/third_party_ejdb) | third_party/ejdb                                  | [ericlee](https://gitee.com/ericlee)         |
| HiviewDFX           | [third_party_iowow](https://gitee.com/openharmony/third_party_iowow) | third_party/iowow                                 | [ericlee](https://gitee.com/ericlee)         |
|DistributedSchedule|[distributedschedule_dms_fwk_lite](https://gitee.com/openharmony/distributedschedule_dms_fwk_lite)|foundation/distributedschedule/dmsfwk_lite|[lijiarun](https://gitee.com/lijiarun)|
|DistributedSchedule|[distributedschedule_safwk_lite](https://gitee.com/openharmony/distributedschedule_safwk_lite)|foundation/distributedschedule/safwk_lite|[lijiarun](https://gitee.com/lijiarun)|
|DistributedSchedule|[distributedschedule_samgr_lite](https://gitee.com/openharmony/distributedschedule_samgr_lite)|foundation/distributedschedule/samgr_lite|[lijiarun](https://gitee.com/lijiarun)|
|StartUp|[startup_appspawn_lite](https://gitee.com/openharmony/startup_appspawn_lite)|base/startup/appspawn_lite|[handyohos](https://gitee.com/handyohos)|
|StartUp|[startup_bootstrap_lite](https://gitee.com/openharmony/startup_bootstrap_lite)|base/startup/bootstrap_lite|[handyohos](https://gitee.com/handyohos)|
|StartUp|[startup_init_lite](https://gitee.com/openharmony/startup_init_lite)|base/startup/init_lite|[handyohos](https://gitee.com/handyohos)|
|StartUp|[startup_syspara_lite](https://gitee.com/openharmony/startup_syspara_lite)|base/startup/syspara_lite|[handyohos](https://gitee.com/handyohos)|
|StartUp|[startup_appspawn](https://gitee.com/openharmony/startup_appspawn)|base/startup/appspawn_standard|[handyohos](https://gitee.com/handyohos)|
|Update|[update_ota_lite](https://gitee.com/openharmony/update_ota_lite)|base/update/ota_lite|[ailorna](https://gitee.com/ailorna)|
|Update|[update_app](https://gitee.com/openharmony/update_app)|base/update/app|[ailorna](https://gitee.com/ailorna)|
|Update|[update_packaging_tools](https://gitee.com/openharmony/update_packaging_tools)|base/update/packaging_tools|[ailorna](https://gitee.com/ailorna)|
|Update|[update_updater](https://gitee.com/openharmony/update_updater)|base/update/updater|[ailorna](https://gitee.com/ailorna)|
|Update|[update_updateservice](https://gitee.com/openharmony/update_updateservice)|base/update/updateservice|[ailorna](https://gitee.com/ailorna)|
|Update|[third_party_bzip2](https://gitee.com/openharmony/third_party_bzip2)|third_party/bzip2|[ailorna](https://gitee.com/ailorna)|
|Update|[third_party_lz4](https://gitee.com/openharmony/third_party_lz4)|third_party/lz4|[ailorna](https://gitee.com/ailorna)|
|MiscServices|[miscservices_time](https://gitee.com/openharmony/miscservices_time)|base/miscservices/time|[litao33](https://gitee.com/litao33)|
|MiscServices|[miscservices_inputmethod](https://gitee.com/openharmony/miscservices_inputmethod)|base/miscservices/inputmethod|[demon](https://gitee.com/zhouyongfei)|
|MiscServices|[miscservices_wallpaper](https://gitee.com/openharmony-sig/miscservices_wallpaper)|base/miscservices/wallpaper|[litao33](https://gitee.com/litao33)|
|MiscServices|[miscservices_screensaver](https://gitee.com/openharmony-sig/miscservices_screensaver)|base/miscservices/screensaver|[litao33](https://gitee.com/litao33)|
|MiscServices|[miscservices_screenlock](https://gitee.com/openharmony-sig/miscservices_screenlock)|base/miscservices/screenlock|[litao33](https://gitee.com/litao33)|
|MiscServices|[miscservices_print](https://gitee.com/openharmony-sig/miscservices_print)|base/miscservices/print|[litao33](https://gitee.com/litao33)|
|MiscServices|[miscservices_pasteboard](https://gitee.com/openharmony-sig/miscservices_pasteboard)|base/miscservices/pasteboard|[litao33](https://gitee.com/litao33)|
|MiscServices|[miscservices_download](https://gitee.com/openharmony-sig/miscservices_download)|base/miscservices/download|[litao33](https://gitee.com/litao33)|
|Notification|[notification_ces_standard](https://gitee.com/openharmony/notification_ces_standard)|base/notification/ces_standard|[autumn330](https://gitee.com/autumn330)|
|Notification|[notification_ans_standard](https://gitee.com/openharmony/notification_ans_standard)|base/notification/ans_standard|[autumn330](https://gitee.com/autumn330)|
|Account|[account_os_account](https://gitee.com/openharmony/account_os_account)|base/account/os_account|[verystone](https://gitee.com/verystone)|
|Account|[account_app_account](https://gitee.com/openharmony-sig/account_app_account)|base/account/app_account|[verystone](https://gitee.com/verystone)|
|accessibility|[accessibility](https://gitee.com/openharmony-sig/accessibility)|base/accessibility|[xueyulong](https://gitee.com/ylsnow)|
|DeviceProfile|[device_profile_core](https://gitee.com/openharmony/device_profile_core)|foundation/deviceprofile/device_profile_core|[lijiarun](https://gitee.com/lijiarun)|
|DeviceProfile|[device_profile_core](https://gitee.com/openharmony/device_profile_core)|foundation/deviceprofile/device_profile_core|[jiacan](https://gitee.com/cangegegege)|
|ResourceSchedule|[resourceschedule_work_scheduler](https://gitee.com/openharmony-sig/resourceschedule_work_scheduler)|foundation/resourceschedule/work_scheduler|[chenmingJay](https://gitee.com/chenmingJay)|
|ResourceSchedule|[resourceschedule_background_task_mgr](https://gitee.com/openharmony-sig/resourceschedule_background_task_mgr)|foundation/resourceschedule/background_task_mgr|[wanglai-yao](https://gitee.com/wanglai-yao)|
|ResourceSchedule|[resourceschedule_device_usage_statistics](https://gitee.com/openharmony-sig/resourceschedule_device_usage_statistics)|foundation/resourceschedule/device_usage_statistics|[tangtiantian2021](https://gitee.com/tangtiantian2021)|
|ResourceSchedule|[resourceschedule_resource_schedule_service](https://gitee.com/openharmony-sig/resourceschedule_resource_schedule_service)|foundation/resourceschedule/resource_schedule_service|[shire-yao](https://gitee.com/shire-yao)|

## SIG Members

### Leader
- @handyohos(https://gitee.com/handyohos)
- @ericlee(https://gitee.com/ericlee)

### Committers
|SubSystem|Committer|Mail|
| :----- | :----- |:----- |
|HiviewDFX|[stesen](https://gitee.com/stesen)|[mail](stesen.ma@huawei.com)|
|HiviewDFX|[ericlee](https://gitee.com/ericlee)|[mail](liyu1@huawei.com)|
|HiviewDFX|[maplestorys](https://gitee.com/maplestorys)|[mail](zengzhi5@huawei.com)|
|HiviewDFX|[yaomanhai](https://gitee.com/yaomanhai)|[mail](yaomanhai@huawei.com)|
|HiviewDFX|[shenchenkai](https://gitee.com/shenchenkai)|[mail](shenchenkai@huawei.com)|
|HiviewDFX|[guochuanqi](https://gitee.com/guochuanqi)|[mail](guochuanqi@huawei.com)|
|HiviewDFX|[qidechun](https://gitee.com/pcwlno1)|[mail](qidechun@huawei.com)|
|MiscServices|[litao3](https://gitee.com/litao33)|[mail](litao33@huawei.com)|
|DistributedSchedule|[lijiarun](https://gitee.com/lijiarun)|[mail](lijiarun@huawei.com)|
|StartUp|[handyohos](https://gitee.com/handyohos)|[mail](zhangxiaotian@huawei.com)|
|StartUp|[derek520](https://gitee.com/derek520)|[mail](wtweitao.wei@huawei.com)|
|StartUp|[mytide](https://gitee.com/mytide)|[mail](max.liuwei@huawei.com)|
|Update|[ailorna](https://gitee.com/ailorna)|[mail](hehuan1@huawei.com)|
|Notification|[autumn330](https://gitee.com/autumn330)|[mail](hw.liuwei@huawei.com)|
|Account|[verystone](https://gitee.com/verystone)|[mail](xudaqing@huawei.com)|
|accessibility|[xueyulong](https://gitee.com/ylsnow)|[mail](xueyulong@huawei.com)|
|accessibility|[yaoruijiang](https://gitee.com/ydmgr)|[mail](yaoruijiang1@huawei.com)|
|DeviceProfile|[lijiarun](https://gitee.com/lijiarun)|[mail](lijiarun@huawei.com)|
|DeviceProfile|[jiacan](https://gitee.com/cangegegege)|[mail](jiacan@huawei.com)|
|ResourceSchedule|[chenmingJay](https://gitee.com/chenmingJay)|[mail](chenming48@huawei.com)|
|ResourceSchedule|[wanglai-yao](https://gitee.com/wanglai-yao)|[mail](yaowanglai@huawei.com)|
|ResourceSchedule|[tangtiantian2021](https://gitee.com/tangtiantian2021)|[mail](tangchengkai@huawei.com)|
|ResourceSchedule|[shire-yao](https://gitee.com/shire-yao)|[mail](yaoyanxia1@huawei.com)|

### Meetings
 - Meeting time: Wednesday at 14:00 o'clock, biweekly
 - Meeting link: Welink

### Contact (optional)

- Mailing list：stesen.ma@huawei.com;liyu1@huawei.com;zengzhi5@huawei.com;yaomanhai@huawei.com;shenchenkai@huawei.com;guochuanqi@huawei.com;litao33@huawei.com;lijiarun@huawei.com;zhangxiaotian@huawei.com;wtweitao.wei@huawei.com;max.liuwei@huawei.com;hehuan1@huawei.com;hw.liuwei@huawei.com;xudaqing@huawei.com;qidechun@huawei.com
- Zulip group: https://zulip.openharmony.cn
- Wechat group：NA
