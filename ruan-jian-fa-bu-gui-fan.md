# 发布流程 #

  所有软件发布均在本地打包或者自动构建后，上传至公网FTP的dom_release目录相应的产品下；
  
  如果是Release版本，并需要开放给用户下载，请同时将一份拷贝放置在public_for_web 目录中；
  
  所有产品必须有版本号。
  
  Release版本必须提供安装包和绿色安装两个文件，其他版本可以使用绿色安装。
 
# 发布时版本号文件命名 #
 
  软件版本号有四部分组成，第一部分为主版本号，第二部分为次版本号，第三部分为修订版
本号，第四部分为日期版本号加希腊字母版本号，希腊字母版本号共有四种，分别为alpha、beta 、RC 、 release
软件版本命名规范
![](http://ww1.sinaimg.cn/large/006R5gQQgy1fh7l8t0jnaj30dd06774h.jpg)

## 软件版本阶段说明##

###Alpha
软件的初级版本，表示该软件在此阶段以实现软件功能为主，通常只在软件开发者    内部交流，一般而言，该版本软件的Bug较多，需要继续修改，是测试版本。测试    人员提交Bug经开发人员修改确认之后，发布到测试网址让测试人员测试，此时可将软件版本标注为alpha版。

###Beta

该版本相对于Alpha 版已经有了很大的进步，消除了严重错误，但还需要经过多次    测试来进一步消除，此版本主要的修改对象是软件的UI。修改的的Bug 经测试人    员测试确认后可发布到外网上，此时可将软件版本标注为 beta版。
###RC
该版本已经相当成熟了，基本上不存在导致错误的Bug，与即将发行的正式版本相差   无几。

###Release
该版本意味“最终版本”，在前面版本的一系列测试版之后，终归会有一个正式的      版本，是最终交付用户使用的一个版本。该版本有时也称标准版。


## 版本号修改规则##
（1）主版本号：当功能模块有较大的变动，比如增加模块或是整体架构发生变化。此版本      号由项目决定是否修改。
（2）次版本号：相对于主版本号而言，次版本号的升级对应的只是局部的变动，但该局部      的变动造成程序和以前版本不能兼容，或者对该程序以前的协作关系产生      了破坏，或者 是功能上有大的改进或增强。此版本号由项目决定是否修      改。
（3）修订版本号：一般是Bug 的修复或是一些小的变动或是一些功能的扩充，要经常发布    修订版，修复一个严重 Bug 即可发布一个修订版。此版本号由项目经理    决定是否修改。
（4）日期版本号：用于记录修改项目的当前日期，每天对项目的修改都需要更改日期版本     号。此版本号由开发人员决定是否修改。
（5）希腊字母版本号：此版本号用于标注当前版本的软件处于哪个开发阶段，当软件进入      到另一个阶段时需要修改此版本号。此版本号由项目决定是否修改。

##版本发布周期 ##
### 非紧急情况：
首先由测试人员测试并提交Bug，其次开发人员会尽量在当天修复Bug并在第二天发布该版本的alpha版，然后由测试人员测试验证关闭Bug之后在第三天会发布该版本的 beta 版。
###紧急情况
如果Bug比较紧急可跳过一般流程，由开发人员尽快修复Bug，测试确认之后直接发布该版本的 beta版。

# 版本号修改举例说明
如此时版本号为：1.0.0.0321_alpha ，此时为内部测试阶段
（1）开发人员修复了测试人员提交的bug并经测试人员测试验证关闭bug之后，发布到外网时，此时就进入了软件的下一个阶段，版本号可改为：1.0.0.0321_beta ，如当前日期跟上一个版本号的日期不一样，版本号可改为：1.0.0.0322_beta。
（2）如果修复了一些重大Bug 并按照流程发布到外网时就可发布一个修订版，如1.0.1.0322_beta，日期为发布的当前日期。
（3）如果对软件进行了一些功能上的改进或增强，进行了一些局部变动的时候要修改次版本号，如：1.1.0.0322_beta（上一级有变动时，下级要归零）。
（4）当功能模块有较大变动，增加模块或整体架构发生变化时要修改主版本号，如新增加了退款功能，则版本号要改为：2.0.0.0322_beta 。
  
  