# OM工作站软件打包为win安装包的方法 #

  Win公用工控机上， 在直接在 d:\OM 目录下运行
  32位：npm run package-win
  64位：npm run package-win-x64
  （期间报错可以忽略掉，NSIS 安装包环境未配）
  完成后 OM 目录下 release 文件夹下会生成一个文件夹，那个就是绿色版的
  封包前，先更新最新代码

# OM后台的重启方法 #
  Win公用工控机上，远程桌面连接 139.196.243.32
  关掉已有的一个 python runEngine.py窗口
  在C:\dom\code\beopws目录下右键svn update更新文件后，开启命令行，敲：python runEngine.py
