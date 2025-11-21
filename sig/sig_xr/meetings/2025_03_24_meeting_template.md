# XR SIG 重点工作拆分 2025年03月24日 9:30-12：00（北京时间）

## 议题(Agenda)
- OH For XR开发进展
- 技术诉求方案对齐
- 后续计划

## 与会人(Attendees)
- [@zhao_mengjiao](https://gitee.com/zhao_mengjiao)
- [@xie_yujuan](https://gitee.com/xie_yujuan_hw)

## 会议纪要(Notes)
### 一、OH For XR开发进展：
#### 1、适配现状：已基于OH4.0+RK3588适配蓝牙、WiFi及DP1.4相关驱动、适配IMU下行数据解析，可实现基于视野中心及第三方手柄（1款）的VR场景的3DoF呈现与交互及悬停视频播放能力 <br>

#### 2、技术诉求方案对齐：<br>
##### （1）Frontbuffer机制，解决送显时延问题：初步确定引入SingleBuffer机制解决。关注运作包括：纹理提交由RS完成；用RS纹理实现single buffer；vsync时序严格控制读写；超出vsync周期使用ATW解决撕裂问题。<br>依赖点包括：（i）OH+RK3588需要支持singlebuffer（shareBufferMode+autoRefresh）； <br>
##### （2）多应用纹理获取：建议使用图形子系统提供的虚拟屏能力获取应用纹理，再进行双目成像+纹理合成，提交眼镜屏buffer送显 <br>

#### 3、后续计划：430：明确代码仓管理及运作、技术诉求方案确定；531：多应用纹理获取开发与验证； <br>

#### 4、遗留点：
（1）OH For XR代码仓管理与运作方案，责任人：周才发、谢玉娟、卫丁，完成时间2025.4.20；<br>
（2）RK3588的OH适配节奏及singlebuffer送显依赖，责任人：周才发、谢玉娟、卫丁，完成时间2025.4.20；<br>
（3）OH For XR的对外宣传方式与OH开发者大会，责任人：周才发、谢玉娟、卫丁，完成时间2025.4.20；<br>
（4）Open XR华为内部对齐后，再将任务分解到XR SIG，责任人：张浩、洪汉德，完成时间2025.4.20 <br>
