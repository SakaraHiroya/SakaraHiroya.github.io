---
title: React.js折腾小计
date: 2017-02-08 15:57:00
---

我不会告诉你这篇文章是折腾了ng1，vue，react三大框架之后才写的QvQ

好了废话不多说了，为什么我会跳入这个坑，最早是因为在express框架中，注册表单在用户填写后得通过post请求传回到后端再写入数据库，然而又不想碰jQuery这个东西，所以想到了用目前流行想这些框架。

一开始是用ng1，然后根据phonecat的教程构建出了应用，然而也用了原始的方法，一个angular.js一个angular-router.js再加一个app.js实现的。
当然这样被 [锐神](http://blog.zhangrgk.ninja)等dalao吐槽了，于是乎尝试锐神他们较为推荐的vue来构建，但是vue虽然轻量，但是在模板实现上，以及子父绑定上并不友好，并且vue的社区支持并不友好，对于新手来学习上手并不友好，没有手把手的案例来教你做应用，即使，vue推出了vue-cli这个东西，然而，由于太多报错不知道如何解决，故放弃，最后采用了react实现了项目，并熟悉了webpack打包模式。

这个项目呢，是一个不依托后端程序的单页应用，（导航站），为什么不直接写死html呢，废话！当然是为了便于维护(╯‵□′)╯︵┻━┻，同时也是为了后期升级做打算，因为，未来打算做成一个综合门户，页眉页脚直接写死html，到content里在调用react形成app，content目前只是通过几个路由，每个路由下get一个json，列出导航条目，后期的话，把菜单导航升级成二级的，就可以调用比如论坛等的api实现一个综合门户。

react的hash路由系统默认会抛出一个 "? k=xxxxx"的东西，google一圈，so上有大佬解释说这是为了方便判断什么时候点的某个链接，也有相应的隐藏的解决方案。
但是窝不打算隐藏，url嘛，总要带些 &?_ 什么的才有逼格嘛2333333。

webpack打包模式非常赞，尽管他给我打包出个32k行的js...，但webpack用得不是特别熟悉的情况下，不要乱import进css。（包括我_(:з」∠)_ ）

react目前才学习了冰山一角，开学后继续学习，该应用也很快将会上线，下一篇博文会写一下该应用的实现ovo。

PS：jsx的写法实在太赞了！另外webpack -p后不要在编辑器里乱点编译好的js（。别问我为什么Orz）

<!--more-->