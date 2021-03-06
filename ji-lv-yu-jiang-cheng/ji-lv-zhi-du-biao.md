# 纪律制度表

团队协作中，严明的纪律是战斗力的基本要素，制定的纪律必须严格执行。

大部分低效团队原因都是“沟通”的低效， 因此纪律规范中对沟通明确了要求。

| 条目 | 纪律规范 | 每月允许犯错 | 备注 |
| :--- | :--- | :--- | :--- |
| 1 | 9:30前在QQ群发出今日计划（无论是否有晨会），模版参考备注1 | 1次 | 漏发、晚发、格式不符均算违纪 |
| 2 | 每日工作结束时在QQ群发出工作总结，模版参考备注2 | 1次 | 漏发或格式不符算违纪 |
| 3 | 团队协作中排查后通知前端bug请求协助的规范，模版参考备注3 | 1次 | 发出的协助请求漏内容，算违纪 |
| 4 | 团队协作中排查后通知后台人员接口或服务器问题请求协助的规范，参考备注4 | 1次 | 发出的协助请求漏内容，算违纪 |
| 5 | 所有代码提交必须有明确、清晰、他人能看懂的log，杜绝没内容的流水账（比如说“我修了个bug”） | 0次 | 明显的不合理log算违纪 |
| 6 | 所有发出的redmine任务必须有明确、清晰、他人能看懂的问题内容、描述，杜绝没内容的流水账（比如说“要修几个bug”） | 0次 | 明显的不合理标题或内容算违纪 |
| 7 | 每人每周必须为他们做不少于2次有效的code review, review时必须理解代码基本逻辑 | 0次 | 潦草、遗漏明显问题的code review算违纪 |

# 模版，请严格抄写

备注1：计划模版

```
【今日任务】
1. 实现历史曲线在退出后的不刷新问题(http://192.168.1.3/issues/103)
```

备注2：总结模版

```
【今日任务总结】
1. 实现历史曲线在退出后的不刷新问题(http://192.168.1.3/issues/103)  未完成，原因：临时调配工作。

临时变动：
1. 增加了一个历史报警的bug修复任务（(http://192.168.1.3/issues/103)） 已完成
```

备注3：前端问题

```
【请求前端协助】
eic用户提出诊断页面看不了，经浏览器工具调试定位为前端问题，问题页面：http://59.110.162.38/diagnosisPage, 后台请求暂时无异常。
```

备注4：后台接口问题

必须包含接口、body文本（非截图，超长字符用文本文件）、目前结果、期望结果四个要素

```
【请求后台协助】
eic用户提出诊断页面看不了，经浏览器工具调试定位为后台问题：http://59.110.162.38/api/v2/diagnosis/get/moduleStatus/173
该 接口（get）返回为404，期望返回200。
```



