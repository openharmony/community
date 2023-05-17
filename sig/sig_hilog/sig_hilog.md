# sig_HILOG
English | [简体中文](./sig_hilog_cn.md)

Note: The content of this SIG follows the convention described in OpenHarmony's PMC Management Charter [README](../../zh/pmc.md).

## SIG group work objectives and scope
- To solve the problems such as lack of functionality, low performance and high resource consumption existing in the current log system, we establish this sig to design a new log system HiLog for OpenHarmony. HiLog stores and manages various types of logs, including kernel logs, system logs and third-party logs. It provides rich and convenient log access functions for system developers and application developers. At the same time, HiLog has good performance in log reliability, interface delay and resource overhead. This SIG is a sub SIG of [SIG_BasicSoftwareService](https://gitee.com/openharmony/community/tree/master/sig/sig_basicsoftwareservice).
### work goals
- Solve the common problems in log system:

  * No privacy control

  * No flow control

  * Logs cannot be managed by Domain

  * High IO overhead for log writing

  * Low drop performance, no direct drop mechanism

- Flexible deployment: the log system feature can be tailored according to the needs of the OS.

- Compatibility: the log system is isomorphic on mini system, small system and standard system.

- High performance & thin & reliable: interface delay, resource overhead, and log loss rate are lower than similar systems.

- Output technical documents.

### work scope


## SIG Members

### Leader
- [v11985](https://gitee.com/v11985)

### Committers
- [yaomanhai](https://gitee.com/yaomanhai)
- [stesen](https://gitee.com/stesen)
- [shenchenkai](https://gitee.com/shenchenkai)
- [aajwy](https://gitee.com/aajwy)
- [youyouyuai](https://gitee.com/youyouyuai)
- [heartofrainbow](https://gitee.com/heartofrainbow)
- [henglab](https://gitee.com/henglab)
- [cair_linux_cuda](https://gitee.com/cair_linux_cuda)
- [pan_qing_lin](https://gitee.com/pan_qing_lin)
- [landwind](https://gitee.com/landwind)

### Meetings
 - Meeting time：xxx
 - Meeting application: Refer to the method of [PMC meeting](https://gitee.com/dongjinguang/community/blob/master/zh/pmc.md#pmc%E4%BC%9A%E8%AE%AE%E9%93%BE%E6%8E%A5) to provide the shimo sharing document weblink, convenient for sig_related people to apply for the topic.
 - Meeting link: Welink Meeting or Others
 - Meeting notification: [Subscribe to] (https://lists.openatom.io/postorius/lists/dev.openharmony.io) mailing list dev@openharmony.io for the meeting link
 - Meeting-Minutes: [Archive link address](https://gitee.com/openharmony-sig/sig-content/tree/master/hilog/meetings)

### Contact (optional)

- Mailing list：dev@openharmony.io
- Wechat group：xxx
