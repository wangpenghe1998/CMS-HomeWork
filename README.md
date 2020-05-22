# CMS-HomeWork
CMS模板作业库

## 第四章 实现最小框架

### 创建空目录之后，切换到新创建的此目录然后运行以下命令（运行之后空目录中会出现node_modules文件夹和package-lock.json文件）
<p> (1)npm init -y </p>
<p> (2)npm i titbit </p>
<p> (3)npm i titbit-loader </p>

### 在创建好的目录中创建ceshi1.js文件并在其中加入响应代码，并在此目录下运行以下命令，之后访问http://localhost:8008/
<p> 运行命令 </p>
<p> node ceshi1.js </p>
<p> 访问http://localhost:8008/</p>

## 第六章 重构设计并使用数据库

### Windows平台下载并安装好PostgreSQL

### Windows上如何管理数据库?
<p> 数据库软件部署后，可能需要先利用当前用户的身份登录，然后进行数据库和用户的管理。 </p>

## 第八章 使用TextLight
### 一、通过以下网址获取到TextLight文件夹，并下载到本地
<p> https://github.com/master-genius/textlight </p>

### 二、之后切换到textlight目录下

### 三、初始化
<p> (1)初始化之前需要先创建一个数据库，还需要创建一个普通数据库用户。 </p>
<p> 例如：你要创建tlt用户以及textcms数据库，并让tlt拥有textcms数据库，并且赋予tlt的登录属性 </p>
<p> 注意事项：需要打开SQL Shell进行执行命令，并需要输入正确的用户postgres的口令才可以进行命令输入与执行。 </p>
<p> 执行命令如下： </p>
<p> 1.create role tlt with password 'textcms'; </p>
<p> 2.create database textcms owner tlt; </p>
<p> 3.alter role tlt login; </p>

<p> (2)执行成功，之后可以在pgAdmin中看到数据库与用户名 </p>

<p> (3)Windows上的初始化，运行以下命令： </p>
<p> npm install </p>

<p> 之后创建config目录，然后将cfg-example中的文件都复制到config目录中 </p>

<p> 然后对config/dbconfig.js文件来配置自己的数据库信息</p>

<p> 之后对config/config.js中CMS需要的配置项，进行调整，比如更改host和port </p>

### 四、最后进行初始化root用户，运行以下命令
<p> node createuser.js </p>

### 五、初始化工作完成，启动服务运行一下命令
<p> node app.js </p>

### 六、默认端口在2022，然后在浏览器访问http://localhost:2022

### 七、登录后台，访问以下路径即可访问后台，默认要通过root用户以及初始的密码登录，你可以在登录后重新设置密码。
<p> http://localhost:2022/adminpage/home </p>

## CMS使用感受
<p>内容管理系统（content management system，CMS）是一种位于WEB 前端（Web 服务器）和后端办公系统或流程（内容创作、编辑）之间的软件系统。内容的创作人员、编辑人员、发布人员使用内容管理系统来提交、修改、审批、发布内容。这里指的“内容”可能包括文件、表格、图片、数据库中的数据甚至视频等一切你想要发布到Internet、Intranet以及Extranet网站的信息。</p>

<p>CMS具有许多基于模板的优秀设计，可以加快网站开发的速度和减少开发的成本。</p>

<p>CMS的功能并不只限于文本处理，它也可以处理图片、Flash动画、声像流、图像甚至电子邮件档案。</p>
