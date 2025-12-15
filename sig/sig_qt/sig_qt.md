# sig_Qt
English | [简体中文](./sig_qt_cn.md)

Note: The content of this SIG follows the conventions described in the OpenHarmony's PMC management charter [README](../../zh/pmc.md).

## SIG Group Work Objectives and Scope

### Work Goals

Qt is a cross-platform C++ application framework used for developing graphical user interface applications, supporting mainstream operating systems such as Windows, Linux, MacOS, etc. The Qt SIG has extended the Qt framework to support OpenHarmony, assisting applications developed with Qt in quickly migrating and supplementing the software ecosystem for OpenHarmony.


### Work Scope

The Qt framework porting and adaptation plan contributes to versions Qt5.12.12 and Qt5.15.12.

The adaptation contribution plan for version Qt5.12.12 is as follows:
| Module                   | Description                                                  | Supported |
| ------------------------ | ------------------------------------------------------------ | --------- |
| Qt Core                  | Core non-graphical classes used by other modules.            | Yes       |
| Qt GUI                   | Base classes for graphical user interface (GUI) components. Includes OpenGL. | Yes       |
| Qt Multimedia            | Classes for audio, video, radio and camera functionality.    | Yes       |
| Qt Multimedia Widgets    | Widget-based classes for implementing multimedia functionality. | Yes       |
| Qt Network               | Classes to make network programming easier and more portable. | Yes       |
| Qt QML                   | Classes for QML and JavaScript languages.                    | Yes       |
| Qt Quick                 | A declarative framework for building highly dynamic applications with custom user interfaces. | Yes       |
| Qt Quick Controls        | Provides lightweight QML types for creating performant user interfaces for desktop, embedded, and mobile devices. These types employ a simple styling architecture and are very efficient. | Yes       |
| Qt Quick Dialogs         | Types for creating and interacting with system dialogs from a Qt Quick application. | Yes       |
| Qt Quick Layouts         | Layouts are items that are used to arrange Qt Quick 2 based items in the user interface. | Yes       |
| Qt Quick Test            | A unit test framework for QML applications, where the test cases are written as JavaScript functions. | Yes       |
| Qt SQL                   | Classes for database integration using SQL.                  | Yes       |
| Qt Test                  | Classes for unit testing Qt applications and libraries.      | Yes       |
| Qt Widgets               | Classes to extend Qt GUI with C++ widgets.                   | Yes       |
| Active Qt                | Classes for applications which use ActiveX and COM           | No        |
| Qt 3D                    | Functionality for near-realtime simulation systems with support for 2D and 3D rendering. | Yes       |
| Qt Android Extras        | Provides platform-specific APIs for Android.                 | No        |
| Qt Bluetooth             | Provides access to Bluetooth hardware.                       | Yes       |
| Qt Canvas 3D             | Enables OpenGL-like 3D drawing calls from Qt Quick applications using JavaScript. | No        |
| Qt Concurrent            | Classes for writing multi-threaded programs without using low-level threading primitives. | Yes       |
| Qt D-Bus                 | Classes for inter-process communication over the D-Bus protocol. | No        |
| Qt Gamepad               | Enables Qt applications to support the use of gamepad hardware. | No        |
| Qt Graphical Effects     | Graphical effects for use with Qt Quick 2.                   | Yes       |
| Qt Help                  | Classes for integrating documentation into applications, similar to Qt Assistant. | Yes       |
| Qt Image Formats         | Plugins for additional image formats: TIFF, MNG, TGA, WBMP.  | Yes       |
| Qt Location              | Displays map, navigation, and place content in a QML application. | Yes       |
| Qt Mac Extras            | Provides platform-specific APIs for macOS.                   | No        |
| Qt NFC                   | Provides access to Near-Field communication (NFC) hardware.  | Yes       |
| Qt OpenGL                | OpenGL support classes. Deprecated in favor of the `QOpenGL*` classes in the Qt GUImodule. | No        |
| Qt Platform Headers      | Provides classes that encapsulate platform-specific information, tied to a given runtime configuration of a platform plugin | No        |
| Qt Positioning           | Provides access to position, satellite and area monitoring classes. | Yes       |
| Qt Print Support         | Classes to make printing easier and more portable.           | Yes       |
| Qt Purchasing            | Enables in-app purchase of products in Qt applications.      | No        |
| Qt Quick Controls 1      | Reusable Qt Quick based UI controls to create classic desktop-style user interfaces. Deprecated in favor of Qt Quick Controls 2, which are better and easier to use. | No        |
| Qt Quick Extras          | Provides a specialized set of controls that can be used to build interfaces in Qt Quick. | Yes       |
| Qt Quick Widgets         | Provides a C++ widget class for displaying a Qt Quick user interface. | Yes       |
| Qt Remote Objects        | Provides an easy to use mechanism for sharing a QObjects API (Properties/Signals/Slots) between processes or devices. | Yes       |
| Qt Script                | Classes for making Qt applications scriptable. Deprecated in favor of the `QJS*` classes in the Qt QML module. | No        |
| Qt SCXML                 | Provides classes and tools for creating state machines from SCXML files and embedding them in applications. | Yes       |
| Qt Script Tools          | Additional components for applications that use Qt Script.   | No        |
| Qt Sensors               | Provides access to sensor hardware and motion gesture recognition. | Yes       |
| Qt Serial Bus            | Provides access to serial industrial bus interface. Currently the module supports the CAN bus and Modbus protocols. | Yes       |
| Qt Serial Port           | Provides access to hardware and virtual serial ports.        | Yes       |
| Qt Speech                | Provides support for accessibility features such as text-to-speech. | No        |
| Qt SVG                   | Classes for displaying the contents of SVG files. Supports a subset of the SVG 1.2 Tinystandard. | Yes       |
| Qt UI Tools              | Classes for loading QWidget based forms created in *Qt Designer* dynamically, at runtime. | Yes       |
| Qt WebChannel            | Provides access to QObject or QML objects from HTML clients for seamless integration of Qt applications with HTML/JavaScript clients. | No        |
| Qt WebEngine             | Classes and functions for embedding web content in applications using the Chromium browser project. | No        |
| Qt WebSockets            | Provides WebSocket communication compliant with RFC 6455.    | No        |
| Qt WebView               | Displays web content in a QML application by using APIs native to the platform, without the need to include a full web browser stack. | No        |
| Qt Windows Extras        | Provides platform-specific APIs for Windows.                 | No        |
| Qt X11 Extras            | Provides platform-specific APIs for X11.                     | No        |
| Qt XML                   | C++ implementations of SAX and DOM.                          | Yes       |
| Qt XML Patterns          | Support for XPath, XQuery, XSLT and XML schema validation.   | Yes       |
| Qt Wayland Compositor    | Provides a framework to develop a Wayland compositor.        | No        |
| Qt Charts                | UI Components for displaying visually pleasing charts, driven by static or dynamic data models. | Yes       |
| Qt Data Visualization    | UI Components for creating stunning 3D data visualizations.  | Yes       |
| Qt Network Authorization | Provides support for OAuth-based authorization to online services. | No        |
| Qt Virtual Keyboard      | A framework for implementing different input methods as well as a QML virtual keyboard. Supports localized keyboard layouts and custom visual themes. | No        |
| Qt Quick WebGL           | Provides a platform plugin that allows streaming Qt Quick user interfaces over the network using WebGL™. | No        |

The adaptation contribution plan for version Qt5.15.12 is as follows（The module with bold font indicates differences from the 5.12.12 version）:
| Module                   | Description                                                  | Supported |
| ------------------------ | ------------------------------------------------------------ | --------- |
| Qt Core                  | Core non-graphical classes used by other modules.            | Yes       |
| Qt GUI                   | Base classes for graphical user interface (GUI) components. Includes OpenGL. | Yes       |
| Qt Multimedia            | Classes for audio, video, radio and camera functionality.    | Yes       |
| Qt Multimedia Widgets    | Widget-based classes for implementing multimedia functionality. | Yes       |
| Qt Network               | Classes to make network programming easier and more portable. | Yes       |
| Qt QML                   | Classes for QML and JavaScript languages.                    | Yes       |
| Qt Quick                 | A declarative framework for building highly dynamic applications with custom user interfaces. | Yes       |
| Qt Quick Controls        | Provides lightweight QML types for creating performant user interfaces for desktop, embedded, and mobile devices. These types employ a simple styling architecture and are very efficient. | Yes       |
| Qt Quick Dialogs         | Types for creating and interacting with system dialogs from a Qt Quick application. | Yes       |
| Qt Quick Layouts         | Layouts are items that are used to arrange Qt Quick 2 based items in the user interface. | Yes       |
| Qt Quick Test            | A unit test framework for QML applications, where the test cases are written as JavaScript functions. | Yes       |
| Qt SQL                   | Classes for database integration using SQL.                  | Yes       |
| Qt Test                  | Classes for unit testing Qt applications and libraries.      | Yes       |
| Qt Widgets               | Classes to extend Qt GUI with C++ widgets.                   | Yes       |
| Active Qt                | Classes for applications which use ActiveX and COM           | No        |
| Qt 3D                    | Functionality for near-realtime simulation systems with support for 2D and 3D rendering. | Yes       |
| Qt Android Extras        | Provides platform-specific APIs for Android.                 | No        |
| Qt Bluetooth             | Provides access to Bluetooth hardware.                       | Yes       |
| Qt Canvas 3D             | Enables OpenGL-like 3D drawing calls from Qt Quick applications using JavaScript. | No        |
| Qt Concurrent            | Classes for writing multi-threaded programs without using low-level threading primitives. | Yes       |
| Qt D-Bus                 | Classes for inter-process communication over the D-Bus protocol. | No        |
| Qt Gamepad               | Enables Qt applications to support the use of gamepad hardware. | No        |
| Qt Graphical Effects     | Graphical effects for use with Qt Quick 2.                   | Yes       |
| Qt Help                  | Classes for integrating documentation into applications, similar to Qt Assistant. | Yes       |
| Qt Image Formats         | Plugins for additional image formats: TIFF, MNG, TGA, WBMP.  | Yes       |
| Qt Location              | Displays map, navigation, and place content in a QML application. | Yes       |
| Qt Mac Extras            | Provides platform-specific APIs for macOS.                   | No        |
| Qt NFC                   | Provides access to Near-Field communication (NFC) hardware.  | Yes       |
| Qt OpenGL                | OpenGL support classes. Deprecated in favor of the `QOpenGL*` classes in the Qt GUImodule. | No        |
| **Qt PDF**               | **Classes and functions for rendering PDF documents.**       | **Yes**   |
| Qt Platform Headers      | Provides classes that encapsulate platform-specific information, tied to a given runtime configuration of a platform plugin | No        |
| Qt Positioning           | Provides access to position, satellite and area monitoring classes. | Yes       |
| Qt Print Support         | Classes to make printing easier and more portable.           | Yes       |
| Qt Purchasing            | Enables in-app purchase of products in Qt applications.      | No        |
| Qt Quick Controls 1      | Reusable Qt Quick based UI controls to create classic desktop-style user interfaces. Deprecated in favor of Qt Quick Controls 2, which are better and easier to use. | No        |
| Qt Quick Extras          | Provides a specialized set of controls that can be used to build interfaces in Qt Quick. | Yes       |
| Qt Quick Widgets         | Provides a C++ widget class for displaying a Qt Quick user interface. | Yes       |
| Qt Remote Objects        | Provides an easy to use mechanism for sharing a QObjects API (Properties/Signals/Slots) between processes or devices. | Yes       |
| Qt Script                | Classes for making Qt applications scriptable. Deprecated in favor of the `QJS*` classes in the Qt QML module. | No        |
| Qt SCXML                 | Provides classes and tools for creating state machines from SCXML files and embedding them in applications. | Yes       |
| Qt Script Tools          | Additional components for applications that use Qt Script.   | No        |
| Qt Sensors               | Provides access to sensor hardware and motion gesture recognition. | Yes       |
| Qt Serial Bus            | Provides access to serial industrial bus interface. Currently the module supports the CAN bus and Modbus protocols. | Yes       |
| Qt Serial Port           | Provides access to hardware and virtual serial ports.        | Yes       |
| Qt Speech                | Provides support for accessibility features such as text-to-speech. | No        |
| Qt SVG                   | Classes for displaying the contents of SVG files. Supports a subset of the SVG 1.2 Tinystandard. | Yes       |
| Qt UI Tools              | Classes for loading QWidget based forms created in *Qt Designer* dynamically, at runtime. | Yes       |
| Qt WebChannel            | Provides access to QObject or QML objects from HTML clients for seamless integration of Qt applications with HTML/JavaScript clients. | No        |
| Qt WebEngine             | Classes and functions for embedding web content in applications using the Chromium browser project. | No        |
| Qt WebSockets            | Provides WebSocket communication compliant with RFC 6455.    | No        |
| Qt WebView               | Displays web content in a QML application by using APIs native to the platform, without the need to include a full web browser stack. | No        |
| Qt Windows Extras        | Provides platform-specific APIs for Windows.                 | No        |
| Qt X11 Extras            | Provides platform-specific APIs for X11.                     | No        |
| Qt XML                   | C++ implementations of SAX and DOM.                          | Yes       |
| **Qt XML Patterns**      | **Support for XPath, XQuery, XSLT and XML schema validation.** | **No**    |
| Qt Wayland Compositor    | Provides a framework to develop a Wayland compositor.        | No        |
| Qt Charts                | UI Components for displaying visually pleasing charts, driven by static or dynamic data models. | Yes       |
| Qt Data Visualization    | UI Components for creating stunning 3D data visualizations.  | Yes       |
| **Qt Lottie Animation**  | **A QML API for rendering graphics and animations in JSON format, exported by the Bodymovin plugin for Adobe® After Effects.** | **Yes**   |
| Qt Network Authorization | Provides support for OAuth-based authorization to online services. | No        |
| Qt Virtual Keyboard      | A framework for implementing different input methods as well as a QML virtual keyboard. Supports localized keyboard layouts and custom visual themes. | No        |
| Qt Quick WebGL           | Provides a platform plugin that allows streaming Qt Quick user interfaces over the network using WebGL™. | No        |

### Work Deliverables and Work Plan
- October 2022 to December 2022: Complete the porting and adaptation of core modules such as Qt Core, Qt GUI, and Qt QML.
- December 2022 to March 2023: Port tools related to Qt, match Qt-related project engineering; complete the porting of additional Qt modules.
- March 2023 to June 2023: Validate the porting and adaptation of Qt samples and demos.
- July 2023 to September 2023: Complete the adaptation of modules planned for Qt5.12.12 version and release the binary SDK package; validate the porting and adaptation of Qt unit tests.
- October 2023 to December 2023: Complete the adaptation of modules planned for Qt5.15.12 version and release the binary SDK package; release a Qt application example project based on DevEco.
- January 2024 to June 2024: Complete the adaptation for Qt6.2.x version and release the binary SDK package.

## SIG Members

### Leader
- @cwc1987(https://gitee.com/cwc1987)

### Committers
- @zhu.wei(https://gitee.com/zhuwei12345678)
- @xiecy(https://gitee.com/xiecyong)
- @wanglz(https://gitee.com/wanglz1988)
- @wangh(https://gitee.com/CplusCplus)
- @honglianglin(https://gitee.com/honglianglin)

### Meeting
 - Meeting Time: Bi-weekly meeting, Friday 10:00-10:30
 - Meeting Proposal：[Qt SIG Metting Proposal](https://docs-pre.qingque.cn/s/home/eZQDMOq-T25IEhYtRTMYbqWUD?identityId=25cWu1jdmUt)
 - Meeting Link: WeLink
 - Meeting Summary：[Archive Link Address](https://gitcode.com/openharmony-sig/sig-content/tree/master/qt/meetings)
 - Meeting Notification: [Subscribe to](https://lists.openatom.io/postorius/lists/dev.openharmony.io) mailing list dev@openharmony.io for the meeting link