# 【置顶-通告】社区ToDoList

## 告所有OpenHarmony开发者

亲爱的OpenHarmony开发者，你们好，感谢你们前期的贡献，在大家的共同努力下，社区取得了长足的发展。

本社区ToDoList将持续更新， 欢迎感兴趣的同学一起参与OpenHarmony社区贡献



## **如何参与**

步骤一、**认领ToDo项**：在下面表格找到感兴趣的特性并[提交PR](https://gitee.com/openharmony/docs/blob/master/zh-cn/contribute/%E8%B4%A1%E7%8C%AE%E6%B5%81%E7%A8%8B.md)，更新本文TodoList表格中对应的认领单位/个人和计划完成时间两列；

步骤二、**加入子系统仓团队**：社区管理员审核通过后，仓committer会邀请步骤1中认领ToDo项的账号加入对应的团队，一般是通过发私信或者向账号对应的邮箱发送邮件来完成通知，此时注意查收信息并确认,通常1个工作日内会响应；

步骤三、**成为对应需求issue的负责人**：认领账号确认接受邀请后，子系统负责人会将对应的需求发布一个issue进行跟踪，并将认领账号设置为该issue的责任人；

步骤四、**需求澄清&方案确认**：issue责任人对需求有任何疑问，或者需要交流方案，建议在issue下方进行评论，并@committer，仓committer收到消息后会进行回复；

步骤五、**开发与提交代码**：责任人和社区通过跟踪[issue](https://gitee.com/openharmony/community/blob/master/sig/sig-QA/issue%EF%BC%88%E9%9C%80%E6%B1%82%E7%B1%BB%EF%BC%89%E5%A4%84%E7%90%86%E6%8C%87%E5%AF%BC.md)来进行互动，开发完成后，提交PR[上传代码](https://gitee.com/openharmony/docs/blob/master/zh-cn/contribute/%E8%B4%A1%E7%8C%AE%E6%B5%81%E7%A8%8B.md),并把PR和对应的任务issue进行关联。



## TodoList：

| 级别         | 子系统    | 特性     | 需求描述                                     | 产出标准                                     | 技术要求                              | 难度   | 认领单位/个人 | 计划完成时间 | gitee issue链接                            |
| ---------- | ------ | ------ | ---------------------------------------- | ---------------------------------------- | --------------------------------- | ---- | ------- | ------ | ---------------------------------------- |
| Mini/Small | kernel | Arch   | 支持中断嵌套，提高内核硬实时性                          | 1、实现中断嵌套基本功能：      （1）Cortex-M系列：NVIC（内嵌向量中断控制器）；      1）支持中断抢占优先级和子优先级设置；      2）高抢占优先级的中断可以抢占低抢占优先级的中断的执行（即中断嵌套）；      3）在抢占优先级相同的情况下，高子优先级的中断优先被响应；子优先级只能决定中断响应的先后顺序，不能抢占（即不支持中断嵌套）；      （2）Cortex-A/R系列：GIC中断控制器；      1）同一时间只能有一个中断可以被设成快速中断FIQ；      2）快速中断FIQ可以打断IRQ中断服务程序；      3）IRQ中断不能打断其他中断；      3、其他架构：可根据架构是否支持而定；      4、提供一套通用的对外接口，可以通过适配这些接口来提供中断嵌套的能力；      5、输出需求分析、架构分析、详细设计、测试用例、开发指南、维护手册等文档； | 1、熟悉各个架构中断控制器；      2、熟悉内核异常处理逻辑； | 高    |         |        | <https://gitee.com/openharmony/kernel_liteos_a/issues/I4T8NJ?from=project-issue> |
| Mini       | kernel | Kernel | 支持多核SMP                                  | 1、实现多核基础功能：      1）多核启动框架；      2）多核调度；      3）绑核操作；      2、支持多核功能裁剪，即单核运行或多核运行；      3、保证多核运行尽量独立，减少竞态，提高并行能力；      4、多核性能测试工具，输出多核性能提升数据；      5、支持spinlock死锁检测机制；      6、输出需求分析、架构分析、详细设计、测试用例、开发指南、维测手段等文档； | 1、熟悉内核调度模块；      2、熟悉架构多核启动流程；    | 高    | 拓维      | 930    | <https://gitee.com/openharmony/kernel_liteos_m/issues/I4T90H?from=project-issue> |
| Mini/Small | kernel | Kernel | 互斥锁优先级继承机制优化：当前内核互斥锁优先级继承在多任务多锁场景下，会出现优先级过早恢复或者没有逐级恢复（即违背优先级继承原则）或者优先级恢复错误等问题，需要提供一套覆盖全场景的优先级继承机制，确保优先级继承及恢复满足要求，并且对系统的性能影响降到最低 | 1、全场景优先级继承及恢复功能正常；         2、支持互斥锁死锁检测机制；      3、输出优化后性能影响评估，要求全场景下，性能影响为常量；      4、输出需求分析、详细设计、测试用例、性能分析、维测手段等文档； | 1、熟悉互斥锁逻辑；      2、熟悉优先级继承机制；      | 高    |         |        | <https://gitee.com/openharmony/kernel_liteos_a/issues/I4T8W2?from=project-issue> |
| Mini/Small | kernel | Kernel | 当前内核队列机制在创建队列时，就指定了队列的读写长度，读操作无法在小于该长度的情况下进行，无法满足一些长度变化的读写场景 | 1、支持队列可变长读写操作，读写操作可以在小于该长度的情况下进行；      2、对于超过该长度的读写操作，一律禁止；      3、输出需求分析、详细设计、测试用例等文档； | 1、熟悉内核队列模块；                       | 中    | 深开鸿     | 930    | <https://gitee.com/openharmony/kernel_liteos_a/issues/I4T8WQ?from=project-issue> |
| Mini/Small | kernel | Kernel | 支持Task/Queue/Mutex/sem/Swtmr资源静态方式创建     | 1、支持静态创建任务，需要的内存由程序员指定；      2、结合动态创建的方式，用户可以根据场景调用不同的接口创建任务，适用于内存受限、安全要求高等场景；      3、考虑能否基于现有接口通过添加任务参数（TSK_INIT_PARAM_S）的方式，扩展该功能；      4、如果可以，需要兼容现有调测功能；      5、输出需求分析、详细设计、测试用例等文档； | 1、熟悉各个资源创建流程及涉及的资源；               | 中    | 润和      | 930    | <https://gitee.com/openharmony/kernel_liteos_a/issues/I4T8X4?from=project-issue> |
| Mini       | kernel | Kernel | 任务notify机制                               | 1、适合父线程需要等待子线程运行结束等场景；      2、可以替代信号量、消息队列、时间等机制，使用任务通知的效率会更高；      3、通知量是TCB自带的资源，使用起来非常方便，而且可以点对点的精准唤醒任务；      4、尽量占用最小的资源实现该功能，并提供相关的调测手段；      5、输出需求分析、详细设计、测试用例、开发指南、维测手段等文档； | 1、熟悉任务机制；      2、熟悉任务notify机制；    | 中    | 润和      | 930    | <https://gitee.com/openharmony/kernel_liteos_m/issues/I4T90T?from=project-issue> |
| Mini       | kernel | Kernel | 支持内核queue读写操作，可以在中断中进行                   | 1、对标FreeRTOS，分析内核阻塞式接口在中断中操作的使用场景及好处；      2、以queue机制为例，提供在中断中支持读写操作的功能；      3、输出需求分析、详细设计、测试用例、补充开发指南等文档； | 1、熟悉中断上下文逻辑；                      | 中    | 拓维      | 930    | <https://gitee.com/openharmony/kernel_liteos_m/issues/I4T914?from=project-issue> |
| Mini       | kernel | Arch   | arch架构qemu补充                             | 1、支持arm926   qemu仿真demo；      2、支持Cortex-m33 qemu仿真demo；      3、支持Cortex-m7 qemu仿真demo；      4、demo功能包括基本内核正常运行，串口正常打印，中断、定时器正常运行，内核测试套全部passed； | 1、熟悉qemu仿真；                       | 高    |         |        | <https://gitee.com/openharmony/kernel_liteos_m/issues/I4T91G?from=project-issue> |
| Small      | kernel | Arch   | 支持A53/A72                                | 1、LiteOS-A适配支持A53/A72架构，支持启动、任务调度、MMU、异常、中断、定时器、原子操作等基础功能，满足内核态和用户态运行要求；      2、支持qemu仿真demo；      3、支持内核用例全量拉通；      4、输出需求分析、详细设计等文档； | 1、有Arch适配经验；                      | 高    |         |        | <https://gitee.com/openharmony/kernel_liteos_a/issues/I4T934?from=project-issue> |
| Mini/Small | kernel | 维测     | dump增强（配套解析工具）                           | 1、系统异常dump信息增强，协助全面的分析系统异常问题；      2、要求尽量通过dump信息即可较全面的分析异常问题，提高系统易用性；      3、dump信息配套工具，自动解析； | 1、异常流程；      2、各个模块调测功能；          | 中    |         |        | <https://gitee.com/openharmony/kernel_liteos_a/issues/I4T93F?from=project-issue> |
| Mini       | kernel | FS     | NandFlash文件系统 （基于littlefs增强：小体积、性能、开源）   |                                          |                                   |      |         |        |                                          |
| Small      | kernel | FS     | 面向fat32、jffs2持续性能优化，做到极致                 |                                          |                                   |      |         |        | <https://gitee.com/openharmony/kernel_liteos_a/issues/I4T93U?from=project-issue> |
| Small      | kernel | FS     | fat32支持fast   seek （现有fast seek限制文件扩展，需要改造） |                                          |                                   |      |         |        | <https://gitee.com/openharmony/kernel_liteos_a/issues/I4T948?from=project-issue> |
| Small      | kernel | FS     | FAT文件系统去大锁                               |                                          |                                   | 高    |         |        | <https://gitee.com/openharmony/kernel_liteos_a/issues/I4T94D?from=project-issue> |
| Small      | kernel | FS     | 接口层去nuttx                                |                                          |                                   | 高    |         |        | <https://gitee.com/openharmony/kernel_liteos_a/issues/I4T94V?from=project-issue> |
| Mini       | kernel | FS     | littlefs随机写性能优化                          |                                          |                                   |      |         |        | <https://gitee.com/openharmony/kernel_liteos_m/issues/I4T92J?from=project-issue> |
| Small      | kernel | FS     | rootfs降内存demo验证                          |                                          |                                   |      |         |        | <https://gitee.com/openharmony/kernel_liteos_a/issues/I4T95Q?from=project-issue> |
| Small      | kernel | C库     | 支持libc++引入                               |                                          |                                   |      |         |        | <https://gitee.com/openharmony/kernel_liteos_a/issues/I4T967?from=project-issue> |
| Small      | kernel | C库     | C库能力补全（epoll实现等）                         | 1、用户态musl   c库不支持接口补齐，其中不支持的接口一般会有unsupported_api标识；      2、不支持的接口一般由于内核机制或者系统调用接口不具备，需要补齐；      3、输出接口测试用例等； | 1、熟悉内核；      2、熟悉系统调用框架；          |      |         |        | <https://gitee.com/openharmony/kernel_liteos_a/issues/I4T96M?from=project-issue> |
| Small      | kernel | 三方库    | libuv、dlna、benchmark、pcap、gstreamer、iperf、perf、tcpdump   等等 | 主流三方库支持，丰富轻内核生态                          |                                   | 高    | 深开鸿     | 930    | <https://gitee.com/openharmony/kernel_liteos_a/issues/I4T96Z?from=project-issue> |
| Mini       | kernel | 探索性课题  | 基于rust重写liteos_m基础内核                     |                                          |                                   |      |         |        | <https://gitee.com/openharmony/kernel_liteos_m/issues/I4T92R?from=project-issue> |
| Small      | kernel | 探索性课题  | 用户态驱动（对比业界并增强）                           |                                          |                                   |      |         |        | <https://gitee.com/openharmony/kernel_liteos_a/issues/I4T97E?from=project-issue> |
| Small      | kernel | 探索性课题  | 用户态文件系统                                  |                                          |                                   |      |         |        | <https://gitee.com/openharmony/kernel_liteos_a/issues/I4T97L?from=project-issue> |