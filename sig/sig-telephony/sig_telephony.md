# SIG-Telephony
English | [简体中文](./sig_telephony_cn.md)

Note: The content of this SIG follows the convention described in OpenHarmony's PMC Management Charter [README](/zh/pmc.md).

## SIG group work objectives and scope

### work goals
- Provide basic communication capabilities of cellular mobile networks such as SIM card, network search, cellular data, cellular call and short MMS, manage multi-type call and data network connection, and provide convenient and consistent communication API for application developers.

### work scope
- Telephony core service: initializes the RIL Manager, SIM card module, and network search module.
- Call Manager module: manages three types of calls – circuit switched (CS), IP multimedia subsystem (IMS), and over the top (OTT) calls. It is responsible for applying for the audio and video resources required for a call and resolving conflicts in a multi-channel call.
- Cellular call module: implements basic calls over carrier networks.
- SMS & MMS module: provides the capabilities of sending and receiving short message service (SMS) messages and encoding and decoding multimedia messaging service (MMS) messages.
- State registry module: provides APIs to register and deregister an observer that listens for various callback events of the telephony subsystem.

### The repository 
- project name:
  - core_service：https://gitee.com/openharmony/telephony_core_service
  - cellular_call：https://gitee.com/openharmony/telephony_cellular_call
  - call_manage：https://gitee.com/openharmony/telephony_call_manager
  - state_registry：https://gitee.com/openharmony/telephony_state_registry
  - sms_mms：https://gitee.com/openharmony/telephony_sms_mms
  - ril_adapter：https://gitee.com/openharmony/telephony_ril_adapter
  - cellular_data：https://gitee.com/openharmony/telephony_cellular_data
  - data_storage：https://gitee.com/openharmony/telephony_data_storage
  - netmanager_standard：https://gitee.com/openharmony/communication_netmanager_standard

## SIG Members

### Leader
- @zhang-hai-feng (https://gitee.com/zhang-hai-feng)

### Committers
- @zhang-hai-feng (https://gitee.com/zhang-hai-feng)
- @jyh926 (https://gitee.com/jyh926)
- @clevercong (https://gitee.com/clevercong)
- @ohos-lsw (https://gitee.com/ohos-lsw)
- @xautosoft (https://gitee.com/xautosoft)
- @hwlitao (https://gitee.com/hwlitao)

### Meetings
 - Meeting time：Biweekly regular meeting 16:00-17:00 on Thursday afternoon
 - Meeting application:  [SIG-Telephony Meeting Proposal](https://shimo.im/sheets/wgwGRwc9KCYH6Txv/MODOC)
 - Meeting link: Welink Meeting or Others
 - Meeting notification: [Subscribe to] (https://lists.openatom.io/postorius/lists/dev.openharmony.io) mailing list dev@openharmony.io for the meeting link
 - Meeting-Minutes: [Archive link address](https://gitee.com/openharmony-sig/sig-content)

### Contact (optional)

- Mailing list：dev@openharmony.io
- Slack group：https://zulip.openharmony.cn/
- Wechat group：NA
