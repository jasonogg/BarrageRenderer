## BarrageRenderer
一个 iOS 上的开源弹幕渲染库.

##发起原因:
弹幕实质是多个精灵的时间上的渲染方式. PC/Web上已经有很成熟的解决方案了; Android上比较有名的是BiliBili开源的DanmakuFlameMaster, 但是开源社区尚没有比较好的iOS弹幕渲染器.觉得在二次元文化逐渐渗透的今天,视频弹幕已经是很重要的一种情绪表达方式了.没必要重复造轮子,所以我把自己写的一份弹幕渲染引擎开源了.还有一些需要后续完善的地方,但基本功能已经有了.祝大家玩得开心.

## Features
*  提供过场弹幕(4种方向)与悬浮弹幕(2种方向)支持; 支持图片弹幕与文字弹幕.
*  提供图文弹幕接口attributedText, 可按照demo中的指示生成图文混排弹幕.
*  弹幕字体可定义: 颜色,边框,圆角,背景,字体等皆可定制.
*  自动轨道搜寻算法,新发弹幕会根据相同方向的同种弹幕获取最佳运动轨道.
*  支持延时弹幕,为反复播放弹幕提供可能；支持与外界的时间同步.
*  独立的动画时间系统, 可以统一调整动画速度.
*  特制的动画引擎,播放弹幕更流畅,可承接持续的10条/s的弹幕流速.
*  丰富的扩展接口, 实现了父类的接口就可以自定义弹幕动画.
*  概念较清晰,可以为任意UIView绑定弹幕,当然弹幕内容需要创建控件输入.
*  因为作者记性比较差,所以在很多紧要处添加了注释,理解代码更容易.
*  效果动画如下图所示:
	![效果动画](./BarrageRendererDemo.gif)
	
	视频演示地址: http://v.youku.com/v_show/id_XMTI5NDM4ODk3Ng==.html

## 使用方式
1. 下载版本库,进入BarrageRendererDemo目录. 运行pod update拉取相关库, 即可以运行BarrageRendererDemo.xcworkspace
2. 也可以在您工程的podfile中添加一条引用: *pod 'BarrageRenderer', '1.6.0'*  并在工程目录下的命令行中运行 pod update
3. 或者将代码下载下来, 将BarrageRenderer/目录添加到您的工程当中
4. 在需要使用弹幕渲染功能的地方 #import "BarrageHeader.h".
5. 创建BarrageRenderer,添加BarrageRenderer.view, 执行start方法, 通过receive方法输入弹幕描述符descriptor, 即可以显示弹幕. 详见demo
6. 相关的一篇博文: http://blog.exbye.com/2015/07/an-open-source-ios-barrage-renderer/

## 改进方向
* 引入UIView重用机制,以减少创建弹幕view的cpu消耗.
* 完善批量加载弹幕,XML文件格式制定，弹幕持久化支持;或支持其他格式xml文件.
* 支持设定一屏显示的弹幕的最大长度,支持控制弹幕的流速.

## 支持与联系
* 可以在github上提出相关的issue;
* 也可以通过unash@exbye.com邮件我;
* 或加入qq群:325298378(但消息不一定能及时回复);
* 或关注我的博客: http://blog.exbye.com.
