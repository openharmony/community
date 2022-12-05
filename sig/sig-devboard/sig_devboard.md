# SIG_DevBoard
English | [简体中文](./sig_devboard_cn.md)

Note: The content of this SIG follows the convention described in OpenHarmony's PMC Management Charter [README](/zh/pmc.md).

## SIG group work objectives and scope

### work goals
- Solve the adaptation of OHOS chip and board card

- Solve the fragmentation of OHOS motherboards and accessories

- Provide one-stop service platform for OHOS boards

- Provide an exchange platform for OHOS board business opportunities

- Assist OHOS board card vendors to upload code to the library

### work scope

- Provide OHOS chip adaptation and planning
  - Statistics on the current situation and progress of the chips that have been adapted, are being adapted, and are planned to be adapted

- Provide hardware specifications for OHOS boards

  -  In order to facilitate the versatility of the development board, a hardware interface specification is proposed. It is recommended that development board manufacturers develop, produce and sell under this specification

- Easy Porting Requirements

  - Put forward portability requirements, all OpenHarmony projects need to be supported, not only the kernel and compiled projects

- Porting and Contributing Guidelines

  - Guides board manufacturers to contribute their codes and documents to the community.

- Demo Projects

  - Creates demo projects, hi3516/hi3518/hi3861, for others to follow.

- Expanding Ecosystems

  - Actively cooperates with board manufacturers.

### The repository 
- project name:
  - device_st: https://gitee.com/openharmony-sig/device_st
  - vendor_st: https://gitee.com/openharmony-sig/vendor_st
  - device_soc_allwinner: https://gitee.com/openharmony/device_soc_allwinner
  - device_board_seed: https://gitee.com/openharmony/device_board_isoftstone
  - vendor_seed: https://gitee.com/openharmony/vendor_isoftstone
  - device_mediatek: https://gitee.com/openharmony-sig/device_mediatek
  - vendor_mediatek: https://gitee.com/openharmony-sig/vendor_mediatek
  - device_nordic: https://gitee.com/openharmony-sig/device_nordic
  - vendor_nordic: https://gitee.com/openharmony-sig/vendor_nordic
  - device_nxp: https://gitee.com/openharmony-sig/device_nxp
  - vendor_nxp: https://gitee.com/openharmony-sig/vendor_nxp
  - device_fudanmicro: https://gitee.com/openharmony-sig/device_fudanmicro
  - vendor_fudanmicro: https://gitee.com/openharmony-sig/vendor_fudanmicro
  - device_soc_bestechnic: https://gitee.com/openharmony/device_soc_bestechnic
  - vendor_bestechnic: https://gitee.com/openharmony/vendor_bestechnic
  - device_board_fnlink: https://gitee.com/openharmony/device_board_fnlink
  - device_board_ingenic: https://gitee.com/openharmony-sig/device_board_ingenic
  - device_soc_ingenic: https://gitee.com/openharmony-sig/device_soc_ingenic
  - vendor_ingenic: https://gitee.com/openharmony-sig/vendor_ingenic
  - device_espressif: https://gitee.com/openharmony-sig/device_soc_espressif
  - device_espressif: https://gitee.com/openharmony-sig/device_board_espressif
  - vendor_espressif: https://gitee.com/openharmony-sig/vendor_espressif
  - device_winnermicro: https://gitee.com/openharmony-sig/device_winnermicro
  - vendor_winnermicro: https://gitee.com/openharmony-sig/vendor_winnermicro
  - device_rockchip: https://gitee.com/openharmony-sig/device_rockchip
  - vendor_rockchip: https://gitee.com/openharmony-sig/vendor_rockchip
  - device_unisoc: https://gitee.com/openharmony-sig/device_unisoc
  - vendor_unisoc: https://gitee.com/openharmony-sig/vendor_unisoc
  - device_broadcom: https://gitee.com/openharmony-sig/device_broadcom
  - vendor_broadcom: https://gitee.com/openharmony-sig/vendor_broadcom
  - device_realtek: https://gitee.com/openharmony-sig/device_realtek
  - vendor_realtek: https://gitee.com/openharmony-sig/vendor_realtek
  - device_bouffalolab: https://gitee.com/openharmony-sig/device_bouffalolab
  - vendor_bouffalolab: https://gitee.com/openharmony-sig/vendor_bouffalolab
  - device_soc_beken: https://gitee.com/openharmony/device_soc_beken
  - device_board_beken: https://gitee.com/openharmony/device_board_beken
  - vendor_beken: https://gitee.com/openharmony/vendor_beken
  - device_board_lango: https://gitee.com/openharmony/device_board_lango
  - vendor_asrmicro: https://gitee.com/openharmony/vendor_asrmicro
  - device_soc_asrmicro: https://gitee.com/openharmony/device_soc_asrmicro
  - device_qemu: https://gitee.com/openharmony/device_qemu
  - vendor_ohemu: https://gitee.com/openharmony/vendor_ohemu
  - device_hoperun:https://gitee.com/openharmony-sig/devboard_device_hihope_build
  - device_hoperun:https://gitee.com/openharmony-sig/devboard_device_hihope_dayu
  - device_hoperun:https://gitee.com/openharmony-sig/devboard_vendor_hihope
  - device_board_hihope:https://gitee.com/openharmony/device_board_hihope
  - vendor_hihope:https://gitee.com/openharmony/vendor_hihope
  - device_soc_rockchip:https://gitee.com/openharmony/device_soc_rockchip
  - device_soc_winnermicro:https://gitee.com/openharmony/device_soc_winnermicro
  - device_board_bearpi: https://gitee.com/openharmony/device_board_bearpi
  - device_bearpi:https://gitee.com/openharmony-sig/applications_sample_bearpi_hm_nano
  - device_bearpi:https://gitee.com/openharmony/vendor_bearpi
  - vendor_huawei_ipcamera_v3s: https://gitee.com/openharmony-sig/vendor_huawei_ipcamera_v3s
  - vendor_oh_fun: https://gitee.com/openharmony-sig/vendor_oh_fun
  - vendor_huawei_minidisplay_demo: https://gitee.com/openharmony-sig/vendor_huawei_minidisplay_demo
  - device_board_talkweb: https://gitee.com/openharmony/device_board_talkweb
  - vendor_talkweb: https://gitee.com/openharmony/vendor_talkweb
  - raspberrypi : https://gitee.com/openharmony-sig/devboard_vendor_rpi3b
  - Unionman: https://gitee.com/openharmony-sig/device_unionpi
  - Unionman: https://gitee.com/openharmony-sig/vendor_unionpi
  - itcast: https://gitee.com/openharmony-sig/devboard_device_itcast_genkipi
  - itcast: https://gitee.com/openharmony-sig/devboard_vendor_itcast_genkipi
  - waffle: https://gitee.com/openharmony-sig/devboard_waffle_nano
  - device_board_goodix: https://gitee.com/openharmony/device_board_goodix
  - vendor_goodix: https://gitee.com/openharmony/vendor_goodix
  - device_soc_goodix: https://gitee.com/openharmony/device_soc_goodix
  - device_soc_hisilicon: https://gitee.com/openharmony/device_soc_hisilicon
  - device_board_hisilicon: https://gitee.com/openharmony/device_board_hisilicon
  - device_board_fnlink: https://gitee.com/openharmony/device_board_fnlink
  - device_t-head: https://gitee.com/openharmony-sig/device_soc_t-head
  - device_t-head: https://gitee.com/openharmony-sig/device_board_t-head
  - vendor_t-head: https://gitee.com/openharmony-sig/vendor_t-head
  - device_soc_chipsea: https://gitee.com/openharmony/device_soc_chipsea
  - device_board_chipsea: https://gitee.com/openharmony/device_board_chipsea
  - vendor_chipsea: https://gitee.com/openharmony/vendor_chipsea
  - device_soc_st: https://gitee.com/openharmony/device_soc_st
  - device_board_isoftstone: https://gitee.com/openharmony/device_board_isoftstone
  - vendor_isoftstone: https://gitee.com/openharmony/vendor_isoftstone
  - device_board_hpmicro: https://gitee.com/openharmony/device_board_hpmicro
  - vendor_hpmicro: https://gitee.com/openharmony/vendor_hpmicro
  - device_soc_hpmicro: https://gitee.com/openharmony/device_soc_hpmicro
  - device_board_kaihong: https://gitee.com/openharmony/device_board_kaihong
  - vendor_kaihong: https://gitee.com/openharmony/vendor_kaihong
  - vendor_ubtech: https://gitee.com/openharmony-sig/vendor_ubtech
  - device_board_ubtech: https://gitee.com/openharmony-sig/device_board_ubtech
  - device_soc_xinsheng: https://gitee.com/openharmony-sig/device_soc_xinsheng
  - device_board_unionman: https://gitee.com/openharmony-sig/device_board_unionman
  - vendor_unionman: https://gitee.com/openharmony-sig/vendor_unionman
  - device_soc_eeasytech: https://gitee.com/openharmony-sig/device_soc_eeasytech
  - device_soc_asrmicro: https://gitee.com/openharmony-sig/device_soc_asrmicro

## SIG Members

### Leader
- [liuyang198591](https://gitee.com/liuyang198591)

### Committers
- [li-gaopeng0312](https://gitee.com/li-gaopeng0312)
- [zianed](https://gitee.com/zianed)
- [DennyShen](https://gitee.com/DennyShen)
- [borne](https://gitee.com/borne)
- [jady3356](https://gitee.com/taiyipei)
- [zeeman_wang](https://gitee.com/zeeman_wang)
- [dxbedu](https://gitee.com/dxbedu)
- [SimonLi](https://gitee.com/kkup180)
- [kefeixiong](https://gitee.com/addyke)
- [cijliu](https://gitee.com/cijliu)
- [Laowang-BearPi](https://gitee.com/laowangiotclub)
- [weidongshan](https://gitee.com/weidongshan)
- [Leon](https://gitee.com/jahyeon)
- [zhao_xiuxiu](https://gitee.com/zhao_xiuxiu)
- [firefly_team](https://gitee.com/firefly_team)

### Meetings
 - Meeting time: BiWeek Thursday 10:00
 - Meeting application: [SIG-DevBoardMeeting application](https://shimo.im/sheets/UZBk8yBk0y4NE4SZ)
 - meeting link:Tencent meeting or other meeting
 - Meeting notification: [Subscribe to](https://lists.openatom.io/postorius/lists/sig_devboard.openharmony.io/) mailing list for the 
 - Meeting Summary:To view the minutes of past meetings, please click this [link](https://gitee.com/openharmony-sig/sig-content/tree/master/devboard/meetings)

### Contact (optional)

- Mailing list: [sig_devboard@openharmony.io](https://lists.openatom.io/postorius/lists/sig_devboard.openharmony.io/)
- Zulip group: https://zulip.openharmony.cn
- Wechat group: xxx

