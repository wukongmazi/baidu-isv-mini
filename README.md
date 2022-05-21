# 百度小程序第三方平台开发，一整套流程

https://mp.weixin.qq.com/s/HCsh1J5fP57AW4iMbtNdWA

![Image text](https://img-blog.csdnimg.cn/33d71210ef32403c9a3a6fddfa26d2d9.png)

#### 介绍
百度智能小程序第三方平台开发着力于解决百度生态体系内的小程序管理问题，一套模板，随处部署。能尽可能地减少系统服务商的开发成本，系统服务商只用开发一套小程序代码作为模板就可以快速批量的孵化出大量的商家小程序。

第三方平台是第三方服务商帮助小程序开发者进行开发、管理、运营等工作的综合平台。小程序开发者可一键授权给第三方平台，通过第三方平台完成业务。

![Image text](https://img-blog.csdnimg.cn/bca84214438c4d95ae02436f2a388d8d.png)

比如餐饮类、社区团购类的小程序，大部分功能都相同，这时候第三方平台只要通过模板开发，得到商家授权后，即可快速根据模板代码给商家快速实例化小程序。无需关心各个商家的小程序资料信息，繁琐操作那些开发配置信息。多个前端只需对应一个服务端后台。时间少，成本低。

#### 业务特点：

模板开发。先开发小程序模板，再用模板给授权小程序上传代码。

使用绑定开发小程序的管理员或成员账号登录百度小程序开发者工具（IDE）。

开发者工具中按照正常的小程序开发流程进行代码开发和调试。

开发完成后，点击发布，完成草稿上传。

#### 1、添加商户基本信息

![Image text](https://img-blog.csdnimg.cn/d2b4abd2000e467abafdc3f83ce143f2.png)

#### 2、引导商户授权获取授权信息

![Image text](https://img-blog.csdnimg.cn/0d0e44f98cc54893a7041615dbb2cd56.png)

![Image text](https://img-blog.csdnimg.cn/f70663c432f44505a7a2ee8e3043adef.png)

#### 3、修改小程序基本资料

在这里可以直接修改小程序资料，而无需跑到各个小程序后台去修改。包括小程序头像、小程序名称、简介内容、服务状态。这四个是独立接口，放在一起，所以修改的时候需要选择要修改哪个属性。

![Image text](https://img-blog.csdnimg.cn/fc90a0deb1314cd4b868e4ea4f603140.png)

#### 4、服务类目管理

支持类目的覆盖修改，主体下类目资质已经审核通过的不会再次审核，小程序类目上限为5个

![Image text](https://img-blog.csdnimg.cn/f8e7695f03834ac7abfdc1f8b8ce9348.png)

![Image text](https://img-blog.csdnimg.cn/3a4992b149224063ba0bc81d420d7819.png)

![Image text](https://img-blog.csdnimg.cn/96bbe26550964612b77b077c367a6aa7.png)

删除类目

![Image text](https://img-blog.csdnimg.cn/41e7a63b1b854d8ea410376d858f2509.png)

新增和修改类目，如果需要资质的话要上传资质文件

![Image text](https://img-blog.csdnimg.cn/64101f1f792f419887182994e3b66b72.png)

#### 5、设置服务器域名

授权给第三方的小程序，其服务器域名只可以为第三方的服务器，当小程序通过第三方发布代码送审后，小程序原先自己配置的服务器域名将被删除，只保留第三方平台的域名，所以第三方平台在代替小程序送审之前，需要调用接口为小程序添加服务器域名。

需要先将域名登记到第三方平台的小程序服务器域名中，才可以调用接口进行配置。

为授权的小程序配置域名时支持配置子域名，例如第三方登记的服务器域名如为baidu.com，则可以直接将baidu.com及其子域名（如xxx.baidu.com）也配置到授权的小程序中。

![Image text](https://img-blog.csdnimg.cn/eb04888da77549279065ff997b7ded97.png)

支持添加、覆盖、删除操作

![Image text](https://img-blog.csdnimg.cn/f50e408099464d1283583e29ead071f0.png)

#### 6、设置业务域名

授权给第三方的小程序，其业务域名只可以为第三方的服务器，当小程序通过第三方发布代码送审后，小程序原先自己配置的业务域名将被删除，只保留第三方平台的域名，所以第三方平台在代替小程序送审之前，需要调用接口为小程序添加业务域名。

需要先将域名登记到第三方平台的业务域名中，才可以调用接口进行配置。

为授权的小程序配置域名时支持配置子域名，例如第三方登记的业务域名如为 baidu.com，则可以直接将 baidu.com 及其子域名（如 xxx.baidu.com）也配置到授权的小程序中。

![Image text](https://img-blog.csdnimg.cn/0e2fbeced84a48b5b032c68a91d36e86.png)

支持添加、覆盖、删除操作

![Image text](https://img-blog.csdnimg.cn/840f935f81094901a318d1316330dd23.png)

#### 7、申请手机号权限

小程序想要集成获取用户授权手机号功能，则需第三方平台代为申请。

![Image text](https://img-blog.csdnimg.cn/7e5c1e30b5934851a7850bde72c6a24f.png)

#### 8、取消手机号权限

小程序不想要集成获取用户授权手机号功能时，可以发起取消手机号权限操作。

![Image text](https://img-blog.csdnimg.cn/3d802b1a5ed0426b8dd7f5e0e74a4da8.png)

最重要的就是代小程序上传代码包、提交审核、撤回审核、发布小程序、版本回退的功能。

小程序提包上线流程详解

![Image text](https://img-blog.csdnimg.cn/8900cc9236e34b37b805626cc6faa5bd.png)

#### 9、上传代码

![Image text](https://img-blog.csdnimg.cn/1e6cb326761349f28f3cc2a555231890.png)

#### 10、查看版本

可以在这里查看版本状态。

![Image text](https://img-blog.csdnimg.cn/c76ea4dfd0044d689409e6e216dbc36b.png)

#### 11、提交审核

当上传代码成后，在这里提交审核。

![Image text](https://img-blog.csdnimg.cn/7810e22512f04797b453927729926910.png)

#### 12、审核撤回

![Image text](https://img-blog.csdnimg.cn/b0ac8dbf96ab4104a1e8dba714fce98c.png)

#### 13、生成体验二维码

在审核发布之前可以生成体验二维码进行体验。

![Image text](https://img-blog.csdnimg.cn/b8959e6fcf954c02a2c0811149563cad.png)

#### 14、发布小程序

审核通过之后，可以将版本发布。

![Image text](https://img-blog.csdnimg.cn/ae0c42b4b63e49b28fa8276c9f9608fd.png)

#### 15、版本回退

如果已发布的版本有问题，还可以将版本回退。

![Image text](https://img-blog.csdnimg.cn/5a9e15c2fb2a4f78a314055113460de4.png)

#### 16、流量下线

在小程序无法正常提供服务（如服务到期等），可以通过该功能主动对流量进行下线。

![Image text](https://img-blog.csdnimg.cn/517bd995f2f94e44af216adb505eb7c6.png)

#### 17、流量开启

当主动对流量进行下线后，可以通过该功能主动自助恢复流量。

![Image text](https://img-blog.csdnimg.cn/337c687be5cb4e4791e5c8337dd986d7.png)

以上就是百度小程序第三方平台开发的整个流程。

公众号后台回复【百度模板开发】获取账号密码。

![Image text](https://img-blog.csdnimg.cn/101a73ed0228494786544af811382ace.png)

山水有相逢，来日皆可期，谢谢阅读，我们再会

我手中的金箍棒，上能通天，下能探海