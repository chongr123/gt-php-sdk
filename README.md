gt-php-sdk
============

GtWeb Php Demo!

使用 Composer
=============

如果你的项目使用 composer 管理依赖, 可以通过以下方式使用 gt PHP Library.


1. 在 `composer.json` 中添加 gt 依赖

```
{
    "require":{
       "gee-team/gt-php-sdk": "dev-master"
    }
}
```
2. 执行 `php composer.phar install` 或 `php composer.phar update`

文件描述
===============================================
1. config/
    - ./config.php
        - captchaid和privatekey配置文件
2. lib/
    - ./class.geetestlib.php
        - 极验的PHP SDK库,提供只带拼图行为验证的功能
    - ./class.geetestmsg.php
        - 提供带短信功能打包的完整功能,继承于GeetestLib

3. static/
    - ./login.html
        - 行为验证的前端示范页面
    - ./msg_login.html
        - 短信+行为验证的前端示范页面

4. web/
    - ./StartCapthcaServlet.php
        - 用户判断极验服务器是否Down机的示例Servlet,页面生成前置处理
    - ./VerifyLoginServlet.php
        - 提交验证调用Sdk的示例Servlet

5. msg/
    - ./StartMsgCapthcaServlet.php
        - 用户判断极验服务器是否Down机的示例Servlet,页面生成前置处理
    - ./VerifyGeetestServlet.php
        - 获取短信前的一次验证逻辑控制
    - ./VerifyMsgServlet.php
        - 提交短信验证示例Servlet

发布日志（由新到旧）
======================
15.7.16.1
-------------------------------------------------------------
1. 向下兼容

15.7.6.1
-----------------------------------------------------------------------------------------------
1. 增加了在极验服务器down机情况下的failback方案的具体实现
2. 优化了前端逻辑，在down机状态下采用动态异步请求的方式，响应速度更快

15.6.29.1
---------------------------------------------------------------------------
1. 根据极验服务升级写的全新的SDK使用方法Demo

15.5.26.1
---------------------------------------------
1. 更改数据传输方式为curl传输

15.4.29.1
-----------------------------------------
1. 规范化SDK

15.4.2.1
-----------------------------------------
1. 增加GT_SDK_VERSION

15.4.1.2
-----------------------------------------
1. 更改数据传输方式

15.4.1.1
-----------------------------------------
1. 更新到 SDK2.0，优化 SDK 写法

15.3.11.1
-----------------------------------------
1.优化弹出式

15.3.10.1
-----------------------------------------
1.优化弹出式

15.3.4.1
-----------------------------------------
1.更改SDK类名，与文档保持一致性


15.2.2.3
-----------------------------------------
1. 一些小bug修复


15.2.2.2
-----------------------------------------
1. 注册chanllege的请求增加超时处理


15.2.2.1
-----------------------------------------
1. chanllege的生成函数转移到服务器端

15.1.28.1
-----------------------------------------
1. SDK加入了自主生成id的接口
2. 前端src引用有了加强版
3. SDK的版本编号规则发生变化

14.8.28
-----------------------------------------
1. login.php里面的`gt`替换成自己验证码的id 
     http://api.geetest.com/get.php?gt=a40fd3b0d712165c5d13e6f747e948d4" 
2. VerifyLogin.php里面的`$PRIVATE_KEY`替换成自己验证码的key值


联系作者：
Email:tanxu1993@gmail.com