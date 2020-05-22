# CMS-HomeWork
CMS模板作业库

## 第四章 实现最小框架
### 一、实现最小框架的结构示意图
<img src="./image/第四章结构示意图.png"/>

### 二、创建空目录之后，切换到新创建的此目录然后运行以下命令（运行之后空目录中会出现node_modules文件夹和package-lock.json文件）
<p> (1)npm init -y </p>
<p> (2)npm i titbit </p>
<p> (3)npm i titbit-loader </p>

### 三、在创建好的目录中创建ceshi1.js文件并在其中加入响应代码，并在此目录下运行以下命令，之后访问http://localhost:8008/
<p> (1)运行命令 </p>
<p> node ceshi1.js </p>
<p> (2)运行结果如下 </p>
<img src="./image/第四章测试结果.png"/>
<p> (3)访问http://localhost:8008/结果示意图 </p>
<img src="./image/第四章页面访问测试结果.png"/>
<p> (4)mdata文件示意图</p>
<img src="./image/第四章mdata示意图.png"/>

## 第五章 添加显示图片功能
### 一、第五章mdata文件示意图
<img src="./image/第五章mdata文件示意图.png"/>

### 二、第五章测试结果图
<img src="./image/第五章测试结果.png"/>

### 三、第五章访问测试结果图
<img src="./image/第五章访问测试结果图.png"/>

## 第六章 重构设计并使用数据库
### 一、加入数据库和后台管理的设计框架图
<img src="./image/第六章设计框架图.png"/>

### 二、Windows平台下载并安装好PostgreSQL
<img src="./image/pgAdmin示意图.png"/>

### 三、Windows上如何管理数据库?
<p> 数据库软件部署后，可能需要先利用当前用户的身份登录，然后进行数据库和用户的管理。 </p>

## 第七章 重新设计目录结构并开始开发
### 一、了解基本的目录结构
<p> (1)adminpages目录是后台页面。 </p>
<p> (2)pages是页面所在目录。 </p>
<p> (3)static是静态文件所在目录，包括js、css等文件。但是pages中同样包括这些文件。 </p>
<p> (4)page.js通过简单的模板机制来整合这些页面。这样可以提供灵活的，方便替换页面的方案。 </p>
<p> (5)controller是控制所在目录。 </p>
<p> (6)model目录的模块都是封装数据库的操作。 </p>
<p> (7)middleware用于集中管理中间件。 </p>
<p> (8)app.js是程序入口文件。 </p>
<p> (9)data目录存储了一些静态数据或者是需要自己编辑的数据。 </p>

## 第八章 使用TextLight
### 一、通过以下网址获取到TextLight文件夹，并下载到本地
<p> https://github.com/master-genius/textlight </p>

### 二、之后切换到textlight目录下，如图所示
<img src="./image/切换到textlight目录.png"/>

### 三、初始化
<p> (1)初始化之前需要先创建一个数据库，还需要创建一个普通数据库用户。 </p>
<p> 例如：你要创建liaobo用户以及textcms数据库，并让liaobo拥有textcms数据库，并且赋予liaobo的登录属性 </p>
<p> 注意事项：需要打开SQL Shell进行执行命令，并需要输入正确的用户postgres的口令才可以进行命令输入与执行。 </p>
<p> 执行命令如下： </p>
<p> 1.create role liaobo with password 'liaobo123'; </p>
<p> 2.create database textcms owner liaobo; </p>
<p> 3.alter role liaobo login; </p>
<p> 执行示意图如下: </p>
<img src="./image/第八章数据库命令执行示意图.png"/>

<p> (2)执行成功，之后可以在pgAdmin中看到数据库与用户名 </p>
<img src="./image/paAdmin执行后示意图.png"/>

<p> (3)Windows上的初始化，运行以下命令： </p>
<p> npm install </p>
<img src="./image/第八章Windows初始化完成示意图.png"/>

<p> 之后创建config目录，然后将cfg-example中的文件都复制到config目录中 </p>
<img src="./image/config目录示意图.png"/>
<p> 然后对config/dbconfig.js文件来配置自己的数据库信息，示意图如下 </p>
<img src="./image/dbconfig.js文件内容示意图.png"/>
<p> 之后对config/config.js中CMS需要的配置项，进行调整，比如更改host和port </p>
<img src="./image/config.js文件示意图.png"/>

### 四、最后进行初始化root用户，运行以下命令
<p> node createuser.js </p>

### 五、初始化工作完成，启动服务运行一下命令
<p> node app.js </p>

### 六、默认端口在2022，然后在浏览器访问http://localhost:2022

### 七、登录后台，访问以下路径即可访问后台，默认要通过root用户以及初始的密码登录，你可以在登录后重新设置密码。
<p> http://localhost:2022/adminpage/home </p>