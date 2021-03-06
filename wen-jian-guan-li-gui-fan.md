# 简要原则

项目分为实施和运维阶段，实施阶段所有文件使用`公网FTP`管理，运维阶段所有记录使用`GITBOOK`进行记录跟踪。

# 1. 实施阶段文件管理规则

每个项目一旦开始实施，就会有一个项目工程ID，目前命名规则为：

```
省拼音首字母连接-市首字母连接-项目俗称全拼音
```

注意：所有内容均为小写

FTP上项目所在目录路径为：

```
/project/项目工程ID/
```

| FTP项目目录下的子目录名 | 目录所包含的文件 |
| :--- | :--- |
| 00-图纸与现场情况 |  |
| 01-下位机 |  |
| 02-上位机 |  |
| 03-内外网环境 |  |
| 04-需求-设计-测试 |  |
| 05-projectdb |  |
| 06-调试 |  |
| 07-验收 |  |
| 08-交付与培训 |  |

# 2. 运维阶段文档记录规则

运维文档不通过FTP存储，主要原因是这个文档需多人协作和不断的更新。

何时需要记录运维文档？当发生以下情形之一时需要整理到运维文档中：

1. 用户提出需求或问题
2. 当项目发生问题或者运维人员主动巡检项目时发现的问题

每个项目的运维文档都由bas-dom用户（公司统一文档管理员）从GITHUB建立一个文档仓库，仓库名为：

```
pom_项目工程ID
```

bas-dom管理者用联名账号同步到GITBOOK，建立书籍，并后将该项目的运维人员GITBOOK账号均设置为colaborator便具备了在线协作编辑权限。

> 申请github及gitbook账号的说明可以参考[刚入职时我需要找谁申请哪些帐号](/tools_user.md "刚入职时我需要找谁申请哪些账号")

## 每个项目运维文档的主要必需内容

| 运维文档主要章节 | 描述 |
| :--- | :--- |
| 用户需求 |  |
| 数据问题 |  |
| 常规策略问题 |  |
| 优化策略问题 |  |
| 界面问题 |  |
| 不知道如何分类的问题 |  |

## 问题段落的主要必需内容

| 问题段落必须包含的内容 | 描述 |
| :--- | :--- |
| 问题提出或发现人 | 不要直接出现真实人名、项目名全称，可以用英文代号。 |
| 问题提出时间 |  |
| 问题描述 |  |
| 分析 |  |
| 解决过程和结果 | 如果没有解决，一定需要留关键字：@fix 表示等待解决 |



