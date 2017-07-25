ThinkCMF 5.0 高考版
===============
> 致我们正在消逝的青春！

### 最新讲座
https://segmentfault.com/l/1500000010288611
![](http://www.thinkcmf.com/themes/simplecmf/Public/getup/sf0810.jpeg)

### 赞助者招募
[查看招募令http://www.thinkcmf.com/supportcmf/goldsponsor.html](http://www.thinkcmf.com/supportcmf/goldsponsor.html)

### ThinkCMF5主要特性
* 基于全新 ThinkPHP5.0开发
* 更规范的代码,遵循PSR-2命名规范和PSR-4自动加载规范
* 更规范的数据库设计
* 前后台完全基于bootstrap3
* 增加 api 模块（需单独下载）
* 支持 composer 管理第三方库
* 核心化：独立核心代码包
* 应用化：开发者以应用的形式增加项目模模块
* 插件化：更强的插件机制，开发者以插件形式扩展功能
* 模板化：模板完全傻瓜式，用户无须改动任何代码即可在后台完成模板设计和配置
* 增加 URL美化功能，支持别名设置，更简单
* 独立的回收站功能，可以管理所有应用临时删除的数据
* 统一的资源管理，相同文件只保存一份
* 注解式的后台菜单管理功能，方便开发者代码管理后台菜单
* 文件存储插件化，默认支持七牛文件存储插件
* 模板制作标签化，内置多个cmf标签，方便小白用户
* 更人性化的导航标签，可以随意定制 html 结构
* 后台首页插件化，用户可以定制的网站后台首页

### 环境推荐
> php5.5+

> mysql 5.6+

> 打开rewrite


### 最低环境要求
> php5.4+

> mysql 5.5+ (mysql5.1稍后兼容)

> 打开rewrite

### 演示站点
http://demo5.thinkcmf.com/admin/   
用户名/密码:demo/thinkcmf

### 自动安装
> 之前安装过 cmf5的同学,请手动创建`data/install.lock`文件

代码已经加入自动安装程序,如果你在安装中有任何问题请提交 issue!

1. public目录做为网站根目录,入口文件在 public/index.php
2. 配置好网站，请访问http://你的域名

enjoy your cmf~!

### 系统更新
如果您是已经安装过 cmf5的用户,请查看 update 目录下的 sql 升级文件,根据自己的下载的程序版本进行更新

### API开发 (支持app,小程序,web)
如果你需要 `api` 开发请下载:  
ThinkCMF5 API :https://github.com/thinkcmf/thinkcmfapi

### 完整版目录结构
```
thinkcmf  根目录
├─api                   api目录(核心版不带)
├─app                   应用目录
│  ├─portal             门户应用目录
│  │  ├─config.php      应用配置文件
│  │  ├─common.php      模块函数文件
│  │  ├─controller      控制器目录
│  │  ├─model           模型目录
│  │  └─ ...            更多类库目录
│  ├─ ...               更多应用
│  ├─command.php        命令行工具配置文件
│  ├─common.php         应用公共(函数)文件
│  ├─config.php         应用(公共)配置文件
│  ├─database.php       数据库配置文件
│  ├─tags.php           应用行为扩展定义文件
│  └─route.php          路由配置文件
├─data                  数据目录
│  ├─conf               动态配置目录
│  ├─runtime            应用的运行时目录（可写）
│  └─ ...               更多
├─public                WEB 部署目录（对外访问目录）
│  ├─api                api入口目录(核心版不带)
│  ├─plugins            插件目录
│  ├─static             静态资源存放目录(css,js,image)
│  ├─themes             前后台主题目录
│  │  ├─admin_simpleboot3  后台默认主题
│  │  └─simpleboot3            前台默认主题
│  ├─upload             文件上传目录
│  ├─index.php          入口文件
│  ├─robots.txt         爬虫协议文件
│  ├─router.php         快速测试文件
│  └─.htaccess          apache重写文件
├─simplewind         
│  ├─cmf                CMF核心库目录
│  ├─extend             扩展类库目录
│  ├─thinkphp           thinkphp目录
│  └─vendor             第三方类库目录（Composer）
├─composer.json         composer 定义文件
├─LICENSE.txt           授权说明文件
├─README.md             README 文件
├─think                 命令行入口文件
```

### 开发手册
http://www.kancloud.cn/thinkcmf/doc

### QQ群:
`ThinkCMF 官方交流群`:316669417  
   
`ThinkCMF 高级交流群`:100828313 (付费)  
高级群专属权益:  
第一波:两个后台风格(ThinkCMF官网风格后台主题,蓝色风格后台主题)

`ThinkCMF 铲屎官交流群`:415136742 (生活娱乐，为有喵的猿人准备)

### 话题专区
http://www.thinkcmf.com/topic/index/index/cat/11.html

### 反馈问题
https://github.com/thinkcmf/thinkcmf/issues

### 更新日志
#### 5.0.170607
[核心]
* 删除 app/common.php
* 规范 admin.js frontend.js函数名
* 更改后台模板设计的模板文件列表排序规则为从小到大排序
* 增加模板切换钩子，方便开发者实现复杂的模板切换功能
* 增加插件作者和演示信息
* 增加数字验证码模板编辑功能
* 增加模板变量编辑控件color
* 增加插件配置组件时间，图片，地理位置，颜色
* 优化模板配置更新
* 优化文件上传，检查已经上传文件是否存在，不存在重新上传
* 修复插件增加新配置时报错
* 修复模板变量 rule 规则存在，但没有规则时模板设计保存会报错
* 修复后台清除缓存后url生成不美化
* 修复模板设计一个页面有多个数组编辑问题
* 修复cdn设置不生效
* 修复后台菜单添加子菜单不选择上级问题
* 修复后台可能多个滚动条
* 修复后台添加、编辑角色一处文字错误
* 修复插件更新时不更新新增的钩子

[门户应用]
* 完善前台模板钩子
* 完善文章标签功能
* 增加前台模板手机注册关闭开关
* 优化文章后台文章分类链接生成
* 修复ff下文章相册图片替换和删除问题
* 修复文章分类排序功能

#### 5.0.170520
[核心]
* 完善插件后台管理
* 后台登录插件化
* 后台首页插件化
* 文件存储插件化
* 增加 URL 美化功能
* 增加后台加密码功能
* 增加用户修改头像
* 增加插件设置表单验证
* 增加前台后台通用语言包
* 增加编辑器里上传文件链接替换
* 增加应用 command.php 配置文件
* 增加后台管理员添加编辑用户名，邮箱惟一性验证
* 优化安装程序
* 优化上传文件
* 优化后台首页
* 优化回收站
* 优化插件启用禁用
* 优化小屏下后台首页不兼容问题
* 优化后台图片查看
* 修复后台菜单编辑不生效
* 修复幻灯片添加不显示问题
* 修复导航数据源数据返回为空时报错
* 修复 pathinfo 模式下后台本站用户默认头像不显示问题
* 修复后台 cdn 不能设置
* 合并asset应用到 user

[门户应用]
* 增加文章收藏功能
* 增加文章点赞限制,一个用户只能点赞一次
* 增加文章分类缩略图
* 优化文章分类管理删除
* 优化文章页和页面页内容图片样式问题
* 修复文章添加编辑默认图片错误
* 修复分类下没有文章时报错
* 修复页面模板设置无效
* 修复页面删除后仍可以访问

#### 5.0.170505
[核心]
* 完善用户注册流程
* 完善插件功能
* 增加手机验证码发送钩子
* 增加手机验证码发送演示插件
* 增加用户邮箱绑定
* 增加用户手机绑定
* 增加常用模板钩子
* 增加模板设计图片上传
* 增加用户密码修改
* 增加用户收藏功能
* 增加导航标签,子导航标签增加 `max-level` 设置
* 修复邮箱验证码发送
* 修复windows下获取模板数据时模板文件路径问题
* 修复单文件,多文件上传
* 修复后台首页用户昵称一直显示admin
* 修复 `navigation`,`subNavigation` 标签两个以上不能同时使用问题
* 修复 console 模式报错
* 取消前台有错误时界面刷新

[门户应用]
* 增加文章附件功能
* 优化文章相册

#### 5.0.170422
[核心]
* 完善幻灯片
* 完善后台控制器方法注释
* 增加调试模式下实时更新模板配置
* 增加友情链接图片上传
* 增加应用公共语言包功能
* 增加资源管理
* 增加模板设计数据源层级关系
* 更新jQuery Form版本
* 增加后台菜单类型是否有界面区分
* 增加权限验证时权限规则里没有的规则不用验证
* 增加前台网站信息获取
* 优化后台菜单导入
* 统一排序规则,按从小到大排序
* 修复后台模板管理点更新提示卸载
* 修复标签`NavigationMenu`
* 修复菜单导入时未添加权限规则
* 修复`navigationFolder`设置多个子菜单后会多循环数据
* 修复部分代码php5.4下不兼容
* 修复后台菜单不能添加编辑

[门户应用]
* 完全独立门户应用
* 完善后台页面管理
* 完善面包屑标签`breadcrumb`
* 完善文章分类管理
* 完善文章管理
* 修复文章分类`path`更新
* 优化文章列表标签`articles`
* 优化后台文章分类选择
* 增加前台文章点赞功能
* 增加前台文章搜索功能
* 增加文章列表分页总数获取

#### 5.0.170401
* 完善文件上传
* 增加回收站功能
* 完善友情链接
* 优化网站设置
* 增加后台登陆验证码
* 修复后台用户密码修改
* 修复用户管理-本站用户头像不显示
* 完善前台用户登录注册
* 增加后台菜单导入
* 修复后台菜单列表排序
* 完善导航
* 增加插件钩子管理
* 完善前台模板


