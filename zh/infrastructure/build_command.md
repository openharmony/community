# OpenHarmony社区PR评论支持命令清单

| 评论输入命令 | 是否必选 | 使用场景                                                     | 命令触发角色 |
| ------------ | -------- | ------------------------------------------------------------ | ------------ |
| start build  | **必选** | 触发编译构建测试                                             | PR创建人<br>committer     |
| stop build   | 可选     | 停止编译构建测试                                             | PR创建人     |
| submit       | 可选     | 自动合入异常时,手工触发合入,检查通过后自动合并PR<br>检查通过条件:openharmony_ci测试通过+PR允许合入 | 任何人     |
| check dco    | 可选     | DCO检查失败时, 更新DCO信息后,人工触发检查DCO<br>检查通过条件:已签署DCO+PR所有提交均包含Signed-off-by信息检查通过,可参考[DCO FAQ](https://gitee.com/openharmony/docs/blob/master/zh-cn/contribute/FAQ.md)处理 | PR创建人     |
| static-check | 可选     | 静态检查失败时,手工触发静态检查,仅用于单独验证,不影响最终构建结果                   | PR创建人     |
