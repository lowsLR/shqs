# 生活糗事
生活糗事是仿百科糗事，一个笑话分享社区。是用uniapp开发的，目前兼容app、微信小程序、支付宝小程序。目前实现的功能有：发布和分享图文，搜索图文文章，个人空间，第三方登录（微信，支付宝账号），查询添加好友，聊天（目前聊天只能发文字）。为何会仿这项目，事由的从一只蝙蝠说起。。。
## 开发所用的框架工具或语言
* 前端-主要是uniapp框架开发，调式工具有Android真机、微信、支付宝小程序
* 后端-基于thinkphp框架开发，编写工具VisualStudioCode
* 聊天功能用的GatewayWorker框架
* 数据库工具-Navicat for MySQL
* 本地服务器调式工具-UPUPW ANK
* 接口测试工具-Postman
* 证书生成-app端用uni的云打包生成，支付宝小程序用支付宝开放平台开发助手
### 预览效果
* 由于带有分享、发布文章和聊天功能，个人用户无法申请到小程序，目前浏览方式可以下载img.zip里面有截图，或者下载app端浏览，[apk下载](https://www.vfor.top/apk/shqs.apk)
## 前端主要目录结构
~~~
┌─common                引用外部资源的公共区
│  └─animate.css        css3动画库
│  └─icon.css           阿里巴巴矢量图标库
│  └─chat.js            聊天界面逻辑处理
│  └─config.js          api请求前缀和websocket地址
│  └─lib.js             网络监听和热更新
│  └─time.js            时间格式
│  └─user.js            用户操作权限
│  └─request.js         验证用户权限
│  └─...                其他的是hello-uni插件的样式
├─components            uni-app组件目录
│   ├─common            多次重复用到的组件
│   ├─mpvue-citypicker  三级联动省份组件
│   ├─uni-xxxx          uni开头的是hello-uni插件的组件
│   └─...   
├─pages                 业务页面文件存放的目录
│  ├─index
│  │  └─index.vue       首页
│  ├─news
│  │  └─news.vue        动态页面
│  ├─paper
│  │  └─paper.vue       聊天列表
│  ├─home
│  │  └─home.vue        设置页面
│  └─...
├─static                存放应用引用静态资源
├─main.js               Vue初始化入口文件
├─App.vue               应用配置，用来配置App全局样式以及监听 应用生命周期
├─manifest.json         配置应用名称、appid、logo、版本等打包信息
└─pages.json            配置页面路由、导航条、选项卡等页面类信息
~~~
