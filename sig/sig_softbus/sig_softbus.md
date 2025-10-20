# sig_SoftBus
English | [简体中文](./sig_softbus_cn.md)

Note: The content of this SIG follows the convention described in OpenHarmony's PMC Management Charter [README](../../zh/pmc.md).

## SIG group work objectives and scope

### work goals

Continuously contributes to the softbus of the OpenHarmony community, implements unified distributed communication capability management between near-field devices, and provides device discovery, networking, and transmission capabilities regardless of the link type. 

### work scope
- Design, review, and make decisions on the architecture of software modules related to the distributed softbus. 
- Review and incorporate the code of software modules in the distributed softbus domain, prohibit low-quality code from being incorporated into the master branch, and maintain the test code. 
- Actively and effectively participate in code review and comment, share programming experience, communicate with developers, transfer software development skills, and effectively coach open source community developers to write good code. 
- Handle requirements, issues and mailing lists, and ensure that the closure period meets the SLA requirements of the OpenHarmony community. 
- Provide feedback and guidance on code quality based on review and development activities to improve code quality in the OpenHarmony community. 

### The repository 
- project name:
  - communication_dsoftbus: https://gitcode.com/openharmony/communication_dsoftbus
  - communication_ipc: https://gitcode.com/openharmony/communication_ipc
  - communication_ipc_lite: https://gitcode.com/openharmony/communication_ipc_lite
  - communication_bluetooth: https://gitcode.com/openharmony/communication_bluetooth
  - communication_nfc: https://gitcode.com/openharmony/communication_nfc
  - communication_connected_nfc_tag: https://gitcode.com/openharmony/communication_connected_nfc_tag
  - communication_wifi: https://gitcode.com/openharmony/communication_wifi
  - communication_wifi_lite: https://gitcode.com/openharmony/communication_wifi_lite
  - communication_wifi_aware: https://gitcode.com/openharmony/communication_wifi_aware
  - communication_dhcp: https://gitcode.com/openharmony/communication_dhcp
  - kernel_linux_common_modules: https://gitcode.com/openharmony/kernel_linux_common_modules/tree/master/newip
  - base_location：https://gitcode.com/openharmony/base_location
  - telephony_call_manager: https://gitcode.com/openharmony/telephony_call_manager
  - telephony_cellular_call: https://gitcode.com/openharmony/telephony_cellular_call
  - telephony_core_service: https://gitcode.com/openharmony/telephony_core_service
  - telephony_sms_mms: https://gitcode.com/openharmony/telephony_sms_mms
  - telephony_state_registry: https://gitcode.com/openharmony/telephony_state_registry
  - applications_camera_sample_communication: https://gitcode.com/openharmony/applications_camera_sample_communication
  - applications_sample_wifi_iot: https://gitcode.com/openharmony/applications_sample_wifi_iot
  - iothardware_peripheral: https://gitcode.com/openharmony/iothardware_peripheral
  - iot_link: https://gitcode.com/openharmony/iot_link
  - third_party_lwip: https://gitcode.com/openharmony/third_party_lwip
  - third_party_nfc-nci：https://gitcode.com/openharmony-sig/third_party_nfc-nci
  - third_party_wpa_supplicant: https://gitcode.com/openharmony/third_party_wpa_supplicant
  - third_party_libcoap: https://gitcode.com/openharmony/third_party_libcoap


## SIG Members

### Leader
- @MaErlii(https://gitee.com/maerlii)

### Committers
- @xuyongpan(https://gitee.com/xuyongpan)
- @yinyouzhan(https://gitee.com/yinyouzhan)
- @rain_myf(https://gitee.com/rain_myf)
- @bigpumpkin(https://gitee.com/bigpumpkin)
- @jiayanhong-hw(https://gitee.com/jiayanhong-hw)
- @life-liu(https://gitee.com/life-liu)
- @knpingan(https://gitee.com/knpingan)
- @hwlitao(https://gitee.com/hwlitao)
- @defeng2020(https://gitee.com/defeng2020)
- @brickhz(https://gitee.com/brickhz)
- @clevercong(https://gitee.com/clevercong)
- @ohos-lsw(https://gitee.com/ohos-lsw)
- @xautosoft(https://gitee.com/xautosoft)
- @li-jet(https://gitee.com/li-jet)
- @MaErlii(https://gitee.com/maerlii)

### Meetings
 - Meeting time: Bi-weekly meeting, Monday 16:00 pm, UTC+8 
 - Meeting Proposal: [OpenHarmony sig_SoftBus Meeting Proposal](https://shimo.im/sheets/iDp1dGmnk3sVjJoE/MODOC)
 - Meeting link: Welink
 - Meeting notification: [Subscribe to](https://lists.openatom.io/postorius/lists/sig_dsoftbus.openharmony.io) mailing list sig_dsoftbus@openharmony.io for the meeting link
 - Meeting Summary:To view the minutes of past meetings, please click this [Meeting minutes](https://gitcode.com/openharmony-sig/sig-content/blob/master/softbus/meetings)


### Contact (optional)
- Mailing list：sig_dsoftbus@openharmony.io
- Wechat group：NA