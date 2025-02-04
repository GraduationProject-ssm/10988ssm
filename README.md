# [首页查询更多项目](https://github.com/GraduationProject-ssm) 包安装运行


# 10988ssm美好生活日志网

![picture](https://raw.githubusercontent.com/GraduationProject-springboot/.github/main/img/wx.png)

### 点击播放视频 ▼
[![Watch the video](https://i.sstatic.net/Vp2cE.png)](https://www.bilibili.com/video/BV1Sh44eDEx6?p=84)


# 系统概述
进过系统的分析后，就开始记性系统的设计，系统设计包含总体设计和详细设计。总体设计只是一个大体的设计，经过了总体设计，我们能够划分出系统的一些东西，例如文件、文档、数据等。而且我们通过总体设计，大致可以划分出了程序的模块，以及功能。但是只是一个初步的分类，并没有真正的实现。

整体设计，只是一个初步设计，而且，对于一个项目，我们可以进行多个整体设计，通过对比，包括性能的对比、成本的对比、效益的对比，来最终确定一个最优的设计方案，选择优秀的整体设计可以降低开发成本，增加公司效益，从这一点来讲，整体设计还是非常重要的。

九宫格日志网站工作原理图如图4-1所示：

![](/md/blog.012.png)

图4-1 系统工作原理图
## 4.2 系统结构设计
系统架构图属于系统设计阶段，系统架构图只是这个阶段一个产物，系统的总体架构决定了整个系统的模式，是系统的基础。九宫格日志网站的整体结构设计如图4-2所示。

![](/md/blog.013.png)

图4-2 系统结构图
## 4.3数据库设计
数据库是计算机信息系统的基础。目前，电脑系统的关键与核心部分就是数据库。数据库开发的优劣对整个系统的质量和速度有着直接影响。
### 4.3.1 数据库设计原则
数据库的概念结构设计采用实体—联系（E-R）模型设计方法。E-R模型法的组成元素有：实体、属性、联系，E-R模型用E-R图表示，是提示用户工作环境中所涉及的事物，属性则是对实体特性的描述。在系统设计当中数据库起着决定性的因素。下面设计出这几个关键实体的实体—关系图。
### 4.3.2 数据库实体
数据模型中的实体（Entity），也称为实例，对应现实世界中可区别于其他对象的“事件”或“事物”。例如，公司中的每个员工，家里中的每个家具。

本系统的E-R图如下图所示：

1、日记信息管理实体图如图4-3所示：

![](/md/blog.014.png)

图4-3日记信息管理实体图

2、美食信息管理实体图如图4-4所示：

![](/md/blog.015.png)

`  `图4-4美食信息管理实体图

3、新闻推荐管理实体图如图4-5所示：

![](/md/blog.016.png)

图4-5新闻推荐管理实体图

#########

### 4.3.3 数据库表设计
数据库的表信息属于设计的一部分，下面介绍数据库中的各个表的详细信息。

表4-1 allusers表

|列名|数据类型|长度|约束|
| :-: | :-: | :-: | :-: |
|id|int|11|NOT NULL|
|username|varchar|50|` `default NULL|
|pwd|varchar|50|` `default NULL|
|cx|varchar|50|` `default NULL|


表4-2 jingdianxinxi表

|列名|数据类型|长度|约束|
| :-: | :-: | :-: | :-: |
|id|int|11|NOT NULL|
|addtime|varchar|50|default NULL|
|jingdianbianhao|varchar|50|default NULL|
|jingdianmingcheng|varchar|50|default NULL|
|jingdianneirong|varchar|50|default NULL|
|jingdianweizhi|varchar|50|default NULL|
|xiangguantupian|varchar|50|default NULL|
|zhanghao|varchar|50|default NULL|
|xingming|varchar|50|default NULL|
|riqi|varchar|50|default NULL|
|sfsh|varchar|50|default NULL|
|shhf|varchar|50|default NULL|

表4-3：meishixinxi表

|列名|数据类型|长度|约束|
| :-: | :-: | :-: | :-: |
|id|` `int|11|NOT NULL |
|addtime|varchar|50|default NULL|
|meishibianhao|varchar|50|default NULL|
|neirong|varchar|50|default NULL|
|meishimingcheng|varchar|50|default NULL|
|meishitupian|varchar|50|default NULL|
|zhanghao|varchar|50|default NULL|
|xingming|varchar|50|default NULL|
|riqi|varchar|50|default NULL|
|sfsh|varchar|50|default NULL|
|`	   `shhf|varchar|50|default NULL|


表4-4：rijixinxi表

|列名|数据类型|长度|约束|
| :-: | :-: | :-: | :-: |
|id|` `int|11|NOT NULL |
|addtime|varchar|50|default NULL|
|rijibianhao|varchar|50|default NULL|
|rijibiaoti|varchar|50|default NULL|
|rijineirong|varchar|50|default NULL|
|xiangguantupian|varchar|50|default NULL|
|zhanghao|varchar|50|default NULL|
|xingming|varchar|50|default NULL|
|riqi|varchar|50|default NULL|
|sfsh|varchar|50|default NULL|
|shhf|varchar|50|default NULL|

表4-5：rijizhanshi表

|列名|数据类型|长度|约束|
| :-: | :-: | :-: | :-: |
|id|` `int|11|NOT NULL |
|addtime|varchar|50|default NULL|
|rijibianhao|varchar|50|default NULL|
|rijibiaoti|varchar|50|default NULL|
|rijineirong|varchar|50|default NULL|
|xiangguantupian|varchar|50|default NULL|
|zhanghao|varchar|50|default NULL|
|xingming|varchar|50|default NULL|
|riqi|varchar|50|default NULL|
|tuijianyuanyin|varchar|50|default NULL|





# 5统详细设计
## 5.1前台首页功能模块
九宫格日志网站，在系统首页可以查看首页、日记信息、美食信息、景点信息、新闻推荐、日志展示、论坛信息、新闻资讯、留言反馈、我的、跳转到后台等内容，如图5-1所示。

![](/md/blog.017.png)

图5-1前台首页功能界面图



`    `用户注册，在用户注册页面可以填写账号、密码、姓名、身份证号码、手机号码、邮箱等信息进行注册，如图5-2所示。

![](/md/blog.018.png)

图5-2用户注册界面图

用户登录，在用户登录页面通过填写账号、密码等信息完成登录，如图5-3所示。在日记信息页面通过填写日记编号、日记标题、日记内容、相关图片、审核回复等信息进行转载操作，如图5-4所示。

![](/md/blog.019.png)

图5-3用户登录界面图

![](/md/blog.020.png)

图5-4日记信息界面图

## 5.2管理员功能模块
管理员登录，通过填写注册时输入的用户名、密码进行登录，如图5-5所示。

![](/md/blog.021.png)

图5-5管理员登录界面图

管理员登录进入九宫格日志网站可以查看个人中心、用户管理、日记信息管理、美食信息管理、景点信息管理、新闻推荐管理、日志展示管理、论坛管理、我的收藏管理、管理员管理、留言板管理、系统管理等信息。

用户管理，在用户管理页面中可以通过填写账号、密码、姓名、性别、身份证号码、手机号码、邮箱、照片等内容进行修改、删除，如图5-6所示。还可以根据需要对日记信息管理进行详情，修改等详细操作，如图5-7所示。

![](/md/blog.022.png)

图5-6用户管理界面图

![](/md/blog.023.png)

图5-7日记信息管理界面图

美食信息管理，在美食信息管理页面中可以查看美食编号、内容、美食名称、美食图片、账号、姓名、日期、是否审核、审核回复等信息，并可根据需要对已有美食信息管理进行修改或删除等操作，如图5-8所示。

![](/md/blog.024.png)

图5-8美食信息管理界面图

景点信息管理，在景点信息管理页面中可以查看景点编号、景点名称、景点内容、景点位置、相关图片、账号、姓名、日期、是否审核、审核回复等信息，并可根据需要对已有景点信息管理进行修改或删除等详细操作，如图5-9所示。

![](/md/blog.025.png)

图5-9景点信息管理界面图

新闻推荐管理，在新闻推荐管理页面中可以查看新闻编号、新闻内容、新闻标题、新闻图片、账号、姓名、日期、是否审核、审核回复等内容，并且根据需要对已有新闻推荐管理进行详情，修改或删除等详细操作，如图5-10所示。

![](/md/blog.026.png)

图5-10新闻推荐管理界面图

日志展示管理，在日志展示管理页面中可以查看日志编号、日志标题、日志内容、相关图片、账号、姓名、日期、推荐原因等内容，并且根据需要对已有日志展示管理进行详情，修改或删除等详细操作，如图5-11所示。

![](/md/blog.027.png)

图5-11日志展示管理界面图

论坛管理，在论坛管理页面中可以查看帖子标题、帖子内容、父节点ID、用户ID、用户名、状态等内容，并且根据需要对已有论坛管理进行修改或删除等详细操作，如图5-12所示。

![](/md/blog.028.png)

图5-12论坛管理界面图


## 5.3用户功能模块
用户登录进入九宫格日志网站可以查看个人中心、日记信息管理、美食信息管理、景点信息管理、新闻推荐管理、日志展示管理、留言板管理、论坛管理、我的收藏管理、系统管理等内容。

日记信息管理，在日记信息管理页面中通过填写日记编号、日记标题、日记内容、相关图片、账号、姓名、日期、是否审核、审核回复等信息，还可以根据需要对日记信息管理进行修改，如图5-13所示。

![](/md/blog.029.png)

图5-13日记信息管理界面图

美食信息管理，在美食信息管理页面中可以查看美食编号、内容、美食名称、美食图片、账号、姓名、日期、是否审核、审核回复等信息，并且根据需要对已有美食信息管理进行查看删除等其他详细操作，如图5-14所示。

![](/md/blog.030.png)

图5-14美食信息管理界面图

景点信息管理，在景点信息管理页面中通过填写景点编号、景点名称、景点内容、景点位置、相关图片、账号、姓名、日期、是否审核、审核回复等内容进行查看、修改、删除，如图5-15所示。

![](/md/blog.031.png)

图5-15景点信息管理界面图

新闻推荐管理，在新闻推荐管理页面中通过填写新闻编号、新闻内容、新闻标题、新闻图片、账号、姓名、日期、是否审核、审核回复等内容进行查看、删除，如图5-16所示。

![](/md/blog.032.png)

图5-16新闻推荐管理界面图

论坛管理，在论坛管理页面中通过填写帖子标题、帖子内容、父节点ID、用户ID、用户名、状态等内容进行查看、删除，如图5-17所示。

![](/md/blog.033.png)

图5-17论坛管理界面图

我的收藏管理，在我的收藏管理页面中通过填写用户ID、收藏ID、表名、收藏名称、收藏图片等内容进行查看、删除，如图5-18所示。

![](/md/blog.034.png)

图5-18我的收藏管理界面图














