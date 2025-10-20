# SIG_DriverFramework

[简体中文](./sig_driver_cn.md) | English

> **NOTE**
>
> The content of this special interest group (SIG) follows the conventions described in OpenHarmony's [PMC Management Charter](../../zh/pmc.md).

## Objectives and Scope

### Objectives

The driver SIG is responsible for building a unified Hardware Driver Foundation (HDF) for OpenHarmony to deploy driver software on devices of different sizes and continuously improve the development efficiency of drivers. The HDF provides a hardware driver platform with kernel decoupling, elastic framework, component-based device model, and unified configuration interface.

### Work Scope

- Define and design the device driver framework and guard its development and evolution.
- Review the Hardware Device Interface (HDI) APIs.
- Organize regular meetings on device drivers, and plan technical communication, Q&A, and sharing.
- Actively work with developers to promote the device ecosystem construction and expansion for device drivers in OpenHarmony projects.

Device driver technology stack
![OpenHarmony Document Overview](figures/driver_overview_en.png)

> **NOTE**
>
> The code of the HDF driver management framework components and driver components can be built on a mini-, small-, or standard-system device. In a standard-system device, you can also specify the user mode or kernel mode for the build.

## Code Repository

- **drivers_hdf_core repository**

| **Component**             | Function                                                                | Path          |
| ----------------- | ---------------------------------------------------------------------- | ---------------- |
| HDF (**hdf_core**)| Provides device service management, device driver management, configuration file compilation tool, dynamic configuration file parsing, device power management, location and debugging capabilities, hot swap management, access permission control, and platform driver model.| drivers/hdf_core |

- **drivers_peripheral repository**

| **Component**                                            | Function                                                                                                                                             | Path                               |
| ------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------- |
| Audio driver (**drivers_peripheral_audio**)               | Provides PCM software parameter configuration, PCM stream operations, audio playback control, audio recording control, audio framework adaptation, and audio effect control.                                                                                             | drivers/peripheral/audio              |
| Camera driver (**drivers_peripheral_camera**)               | Provides photo preview and photographing, video preview and recording, camera device management, camera pipeline management, camera sensor device management, configuration of camera sensor control parameters, camera sensor data flow management, and camera sensor model.                         | drivers/peripheral/camera             |
| Display driver (**drivers_peripheral_display**)              | Provides display hardware control, display hardware composition, display memory management, display device management, and display driver model.                                                                                                                | drivers/peripheral/display            |
| WLAN driver (**drivers_peripheral_wlan**)              | Enables or disables Wi-Fi (STA mode, AP mode, or P2P direct connection), and supports the following: network scanning in STA mode, device dormancy configuration for power saving (low power consumption), network connection or disconnection, iPerf for data transmission testing, anti-interference mode for WLAN, WLAN power mode, WLAN P2P compatibility, and WLAN compatibility architecture.| drivers/peripheral/wlan               |
| Input driver (**drivers_peripheral_input**)                | Opens or closes an input device, reads input events, provides device registration, deregistration, and hot swap mechanisms, obtains input device information, and sets and executes commands for extending the input device.                                                                            | drivers/peripheral/input              |
| Sensor driver (**drivers_peripheral_sensor**)              | Provides traditional sensor driver models (accelerometer, gyroscope, ambient light sensor, proximity sensor, Hall effect sensor, barometer, and thermometer), and medical sensor driver models, and offers capabilities for sensor driver management and data subscription.                                                                           | drivers/peripheral/sensor             |
| USB driver (**drivers_peripheral_usb**)                | Supports the USB device mode and USB host mode.                                                                                                                               | drivers/peripheral/usb                |
| Bluetooth driver (**drivers_peripheral_bluetooth**)            | Enables Bluetooth, disables Bluetooth, and listens for the Bluetooth connection status, to implement the mechanism for Bluetooth sleep and wakeup.                                                                                                                   | drivers/peripheral/Bluetooth          |
| Vibrator driver (**driver_peripheral_vibrator**)             | Provides capabilities for vibrating the vibrator, stopping the vibration, and configuring the vibration effect.                                                                                                                                | drivers/periphera/vibrator            |
| Codec driver (**drivers_peripheral_codec**)              | Provides capabilities related to the codec Hardware Device Interface (HDI) service, codec configuration, codec buffer queue management, and codec adaptation layer.                                                                                                     | drivers/peripheral/codec              |
| Light driver (**drivers_peripheral_light**)               | Provides capabilities for light control and light effect configuration.                                                                                                                                       | drivers/peripheral/light              |
| Thermal driver (**drivers_peripheral_thermal**)               | Polls and checks the heat status of the system hardware, and reports the status to the thermal manager.                                                                                                                  | drivers/peripheral/thermal            |
| Battery driver (**drivers_peripheral_battery**)             | Queries and reports battery status information.                                                                                                                                       | drivers/peripheral/powermgr/battery   |
| Power driver (**drivers_peripheral_power**)                | Processes the hibernation status or wakeup status, as well as the running lock.                                                                                                                               | drivers/peripheral/power              |
| Motion driver (**drivers_peripheral_motion**)             | Provides the motion recognition model to implement capabilities such as enabling or disabling motion recognition, and subscribing to or unsubscribing from motion recognition data.                                                                                                                      | drivers/peripheral/motion             |
| NFC driver (**drivers_peripheral_nfc**)                | Provides capabilities to implement NFC enabling or disabling, tag reading and writing, host card emulation (HCE), and enhanced security element (eSE) emulation.                                                                                                        | drivers/peripheral/nfc                |
| NFC tag driver (**drivers_peripheral_connected_tag**)  | Provides the NFC tag read and write capabilities to allow for writing some device information into the tag chip.                                                                                                                     | drivers/peripheral/nfc/connected_tag  |
| Distributed camera driver (**drivers_peripheral_distributed_camera**)| Provides the implementation of the HDI of the local camera and the extended HDI of the distributed camera, and interacts with the camera framework and the distributed camera SA to complete the operations of the distributed camera.                                                                                       | drivers/peripheral/distributed_camera |
| Memory tracker driver (**drivers_peripheral_memorytracker**)     | Obtains the memory usage of the device driver.                                                                                                                                    | drivers/peripheral/memorytracker      |
| User_auth driver (**drivers_peripheral_user_auth**)         | Provides identity authentication capabilities, including identity authentication with or without a specified user ID, which internally implements the authentication scheme generation and result evaluation to ensure that user identity authentication meets the target security level requirements.                                                                 | drivers/peripheral/user_auth          |
| Face_auth driver (**drivers_peripheral_face_auth**)          | Provides capabilities for face image enrolling and deletion, as well as anti-brute force cracking, functioning as an executor to connect to the unified authentication framework based on the mode defined in the resource pool.                                                                                                     | drivers/peripheral/face_auth          |
| Pin_auth driver (**drivers_peripheral_pin_auth**)          | Provides capabilities for Personal Identification Number (PIN) enrolling and deletion, as well as anti-brute force cracking, functioning as an executor to connect to the unified authentication framework based on the mode defined in the resource pool.                                                                                                     | drivers/peripheral/pin_auth           |
| Fingerprint_auth driver (**drivers_peripheral_fingerprint_auth**)   | Provides capabilities for fingerprint enrolling, deletion, and identification or recognition.                                                                                                                                | drivers/peripheral/fingerprint_auth   |

- **drivers_interface repository**

| **Component**                                               | Function                                                                            | Path                              |
| --------------------------------------------------- | ---------------------------------------------------------------------------------- | ------------------------------------ |
| Display HDI (**drivers_interface_display**)              | Provides the display HDI.                                                                      | drivers/interface/display            |
| WLAN HDI (**drivers_interface_wlan**)               | Provides the WLAN HDI.                                                                    | drivers/interface/wlan               |
| Input HDI (**drivers_interface_input**)                | Provides the input HDI.                                                                   | drivers/interface/input              |
| Sensor HDI (**drivers_interface_sensor**)              | Provides the sensor HDI.                                                                     | drivers/interface/sensor             |
| Vibrator HDI (**drivers_interface_vibrator**)             | Provides the vibrator HDI.                                                                      | drivers/interface/vibrator           |
| Light HDI (**drivers_interface_light**)                | Provides the light HDI.                                                                       | drivers/interface/light              |
| Motion HDI (**drivers_interface_motion**)             | Provides the motion HDI.                                                                      | drivers/interface/motion             |
| USB HDI (**drivers_interface_usb**)                 | Provides the USB HDI.                                                                     | drivers/interface/usb                |
| Thermal HDI (**drivers_interface_thermal**)               | Provides the thermal HDI.                                                                       | drivers/interface/thermal            |
| Power HDI (**drivers_interface_power**)                | Provides the power HDI.                                                                      | drivers/interface/power              |
| Battery HDI (**drivers_interface_battery**)              | Provides the battery HDI.                                                                      | drivers/interface/battery            |
| NFC HDI (**drivers_interface_nfc**)                  | Provides capabilities to implement NFC enabling or disabling, tag reading and writing, host card emulation (HCE), and enhanced security element (eSE) emulation.                                     | drivers/interface/nfc                |
| Distributed camera HDI (**drivers_interface_distributed_camera**)| Provides definition for the extended HDI of the distributed camera.                                                                | drivers/interface/distributed_camera |
| Memory tracker HDI (**drivers_interface_memorytracker**)      | Obtains the memory usage of the device driver.                                                                   | drivers/interface/memorytracker      |
| User authentication HDI (**drivers_interface_user_auth**)          | Provides identity authentication capabilities, including identity authentication with or without a specified user ID, which internally implements the authentication scheme generation and result evaluation to ensure that user identity authentication meets the target security level requirements.| drivers/interface/user_auth          |
| Face_auth HDI (**drivers_interface_face_auth**)           | Provides capabilities for face image enrolling and deletion, as well as anti-brute force cracking, functioning as an executor to connect to the unified authentication framework based on the mode defined in the resource pool.                                    | drivers/interface/face_auth          |
| Pin_auth HDI (**drivers_interface_pin_auth**)            | Provides capabilities for Personal Identification Number (PIN) enrolling and deletion, as well as anti-brute force cracking, functioning as an executor to connect to the unified authentication framework based on the mode defined in the resource pool.                                    | drivers/interface/pin_auth           |
| Fingerprint_auth HDI (**drivers_interface_fingerprint_auth**)   | Provides capabilities for fingerprint enrolling, deletion, and identification or recognition.                                                               | drivers/interface/fingerprint_auth   |


## SIG Members

### Leader

- @zhaowenhua(https://gitee.com/shidi_snow)

### Committers

- @zianed(https://gitee.com/zianed)

- @Kevin-Lau(https://gitee.com/Kevin-Lau)

- @yuanbo(https://gitee.com/yuanbogit)

- @zhuangchunxin(https://gitee.com/aqxyjay)
  
  ### Meetings
  
  - Meeting time: bi-weekly meeting, at 16:00 Wednesday
  - Meeting application: [sig_Driver meetings](https://shimo.im/sheets/36GKhpvrXd8TcQHY)
  - Meeting link: Tencent or other meetings
  - Meeting notice: [Subscribe to](https://lists.openatom.io/postorius/lists/sig_driver@openharmony.io/) the email address to obtain the meeting link.
  - Meeting minutes: Click [here](https://gitcode.com/openharmony-sig/sig-content/tree/master/driver/meetings) to view previous meeting minutes.

### (Optional) Contact

- Email list: [sig_driver@openharmony.io](https://lists.openatom.io/postorius/lists/sig_driver@openharmony.io/)
- WeChat group: xxx
