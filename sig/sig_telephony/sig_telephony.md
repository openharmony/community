# sig_Telephony
English | [简体中文](./sig_telephony_cn.md)

Note: The content of this SIG follows the convention described in OpenHarmony's PMC Management Charter [README](../../zh/pmc.md).

## SIG group work objectives and scope

### work goals
- Provide basic communication capabilities of cellular mobile networks such as SIM card, network search, cellular data, cellular call and short MMS, manage multi-type call and data network connection, and provide convenient and consistent communication API for application developers.

### work scope
- Telephony core service: initializes the RIL Manager, SIM card module, and network search module.
- Call Manager module: manages three types of calls – circuit switched (CS), IP multimedia subsystem (IMS), and over the top (OTT) calls. It is responsible for applying for the audio and video resources required for a call and resolving conflicts in a multi-channel call.
- Cellular call module: implements basic calls over carrier networks.
- SMS & MMS module: provides the capabilities of sending and receiving short message service (SMS) messages and encoding and decoding multimedia messaging service (MMS) messages.
- State registry module: provides APIs to register and deregister an observer that listens for various callback events of the telephony subsystem.


## SIG Members

### Leader
- @zhang-hai-feng (https://gitee.com/zhang-hai-feng)

### Committers
- @zhang-hai-feng (https://gitee.com/zhang-hai-feng)
- @jiayanhong-hw (https://gitee.com/jiayanhong-hw)
- @clevercong (https://gitee.com/clevercong)
- @ohos-lsw (https://gitee.com/ohos-lsw)
- @xautosoft (https://gitee.com/xautosoft)
- @hwlitao (https://gitee.com/hwlitao)

### Meetings
 - Meeting time：Biweekly regular meeting 16:00-17:00 on Thursday afternoon
 - Meeting application:  [sig_Telephony Meeting Proposal](https://shimo.im/sheets/wgwGRwc9KCYH6Txv/MODOC)
 - Meeting link: Welink Meeting or Others
 - Meeting notification: [Subscribe to] (https://lists.openatom.io/postorius/lists/dev.openharmony.io) mailing list dev@openharmony.io for the meeting link
 - Meeting-Minutes: [Archive link address](https://gitee.com/openharmony-sig/sig-content)

### Contact (optional)

- Mailing list：dev@openharmony.io
- Wechat group：NA
