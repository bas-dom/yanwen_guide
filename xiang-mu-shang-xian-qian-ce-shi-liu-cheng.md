# 测试流程 #

## 服务器 ##
windows远程登录机房仿真服务器：
内网使用：192.168.1.3
windows用户名：Administrator
windows密码：润物细无声

或者使用本机(windows系统,且部署core和python 3.4环境)


## 环境部署，适用于第一次测试 ##
* 建立机房仿真目录，如果已有则跳过 C:\simPlant\项目工程标识\
*下载core至该目录中
*将项目s3db文件拷贝至core目录
*将机房仿真策略后台（python程序包）从FTP项目测试目录中下载拷贝至core目录中
*使用Factory调试工具将模式设置为仿真



## 运行仿真 ##
*运行gatewaycore.exe
*运行logicEngine.exe
*运行仿真策略后台：在策略包文件夹空白处shift+右键，选择“在此处打开命令行”，然后运行：
```
python dataSimulation.py
```
* 验证是否联通，方法：使用调试工具修改ChOnOffSetting01为1或0，意味着发出开关机指令，观察ChOnOff01这个反馈点是否跟随变化，若变化则表示仿真后台成功运行

* 使用调试工具打开本地S3db文件调试策略，调试策略时可以控制某策略启用或禁用，以达到调试效果。