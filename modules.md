# 模块

**一、编写模块**

**模块从上至下依次覆盖配置**，模块编写和标准配置写法基本一致，目前**仅支持调整以下段**：

**1、\[General]、\[Replica]、\[MITM]、\[Panel]**

直接覆盖原始值：key = value \
在原始值的末尾进行追加：key = %APPEND% value \
在原始值的开始进行插入：key = %INSERT% value

你只能在 \[MITM] 段中操作 hostname 字段。

**2、\[Rule]、\[Script]、\[URL Rewrite]、\[Header Rewrite]、\[Host]**

新加入的定义将会追加在原始内容的顶部。 \
模块中的规则只可以使用 DIRECT、REJECT、REJECT-TINYGIF 三个内置策略。

**3、元数据**&#x20;

你可以在模块文件里添加元数据：

\#!name=Name Here \
\#!desc=Description Here \
\#（可选）你还可以限制模块的使用平台（可取值为 ios 和 mac）： \
\#!system=mac\
\
原文：[https://community.nssurge.com/d/225-module](https://community.nssurge.com/d/225-module)

模块示例：

```
#!name=模块名
#!desc=模块说明
#!system=ios OR Mac (可选)

[Script]
Scriptname1 = type=generic,timeout=5,script-path=脚本地址
Scriptname2 = type=generic,timeout=5,script-path=脚本地址

[Panel]
//面板
Panel1 = script-name=Scriptname1,update-interval=120 //更新间隔，单位s
Panel2 = script-name=Scriptname2,update-interval=120
```

**二、第三方模块**

来源于网络，不保证永久可用。



Key的模块仓库：[https://github.com/Keywos/rule/tree/main/module](https://github.com/Keywos/rule/tree/main/module)

Ping面板：[https://raw.githubusercontent.com/Keywos/rule/main/module/PingGif.sgmodule](https://raw.githubusercontent.com/Keywos/rule/main/module/PingGif.sgmodule)

迷你机型Ping面板：[https://raw.githubusercontent.com/Keywos/rule/main/module/PingGifMini.sgmodule](https://raw.githubusercontent.com/Keywos/rule/main/module/PingGifMini.sgmodule)

DoH : [https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Spec/DoH](https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Spec/DoH)

WARP+ : [https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Panel/WARP](https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Panel/WARP)

刷新DNS : [https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Panel/Flush-DNS](https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Panel/Flush-DNS)

节点切换 : [https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Panel/Group-Panel](https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Panel/Group-Panel)

节点iP信息 : [https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Panel/IP-Check](https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Panel/IP-Check)

网络信息 : [https://raw.githubusercontent.com/getsomecat/GetSomeCats/Surge/modules/Panel/Network-Info/Moore/Network-Info-CN.sgmodule](https://raw.githubusercontent.com/getsomecat/GetSomeCats/Surge/modules/Panel/Network-Info/Moore/Network-Info-CN.sgmodule)

流媒体解锁检测 : [https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Panel/Stream-All](https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Panel/Stream-All)

流媒体解锁检测Lite : [https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Panel/Stream-All-Lite](https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Panel/Stream-All-Lite)

Sub-Store : [https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Spec/Sub-Store](https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Spec/Sub-Store)

机场流量信息 : [https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Panel/Sub-info](https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Panel/Sub-info)

Surge启动时长 : [https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Panel/Surge-Pro](https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Panel/Surge-Pro)

节假日信息 : [https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Panel/Timecard](https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Panel/Timecard)

TestFlight下载修正/账户管理 : [https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Spec/TestFlight](https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Spec/TestFlight)

Safari 谷歌搜索重定向 : [https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Spec/GoogleRewrite](https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Spec/GoogleRewrite)

隐藏状态栏VPN图标 : [https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Spec/Hide-VPN-Icon](https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Spec/Hide-VPN-Icon)

京东历史价格展示 : [https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Spec/JD\_Price](https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Spec/JD\_Price)

通用设置增强 : [https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Spec/General](https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Spec/General)

跳过部分国内App的代理检测 : [https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Spec/Skip-Proxy](https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Spec/Skip-Proxy)

什么值得买「自动签到+去广告」 : [https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Spec/smzdm](https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Spec/smzdm)

B站净化 : [https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Spec/Bilibili](https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Spec/Bilibili)

B站签到 : [https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Spec/Bilibili-Login](https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Spec/Bilibili-Login)

微博净化 : [https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Spec/Weibo](https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Spec/Weibo)

知乎净化 : [https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Spec/Zhihu](https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Spec/Zhihu)

贴吧净化 : [https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Spec/Tieba](https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Spec/Tieba)

贴吧签到 : [https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Spec/Tieba\_Checkin](https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Spec/Tieba\_Checkin)

电信余量：[https://github.com/ChinaTelecomOperators/ChinaTelecom ](https://github.com/ChinaTelecomOperators/ChinaTelecom)

联通余量：[https://github.com/ChinaTelecomOperators/ChinaUnicom ](https://github.com/ChinaTelecomOperators/ChinaUnicom)

短信转发：[https://github.com/ChinaTelecomOperators/SMSForward](https://github.com/ChinaTelecomOperators/SMSForward)

TikTok解锁 : [https://github.com/Semporia/TikTok-Unlock](https://github.com/Semporia/TikTok-Unlock)

macOS翻译 : [https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Spec/macOS-Translate](https://github.com/Rabbit-Spec/Surge/tree/Master/Module/Spec/macOS-Translate)

去广告模块：[https://github.com/blackmatrix7/ios\_rule\_script/tree/master/rewrite/Surge](https://github.com/blackmatrix7/ios\_rule\_script/tree/master/rewrite/Surge)

阻止HTTPDNS：[https://github.com/VirgilClyne/GetSomeFries/wiki/🚫-HTTPDNS](https://github.com/VirgilClyne/GetSomeFries/wiki/%F0%9F%9A%AB-HTTPDNS)

网络测速模：[https://raw.githubusercontent.com/getsomecat/GetSomeCats/Surge/modules/Panel/Net\_Speed/Net\_Speed.sgmodule](https://raw.githubusercontent.com/getsomecat/GetSomeCats/Surge/modules/Panel/Net\_Speed/Net\_Speed.sgmodule)

B站增强模块仓库：[https://github.com/BiliUniverse/Universe](https://github.com/BiliUniverse/Universe)

ChatGPT可用性检测：[https://raw.githubusercontent.com/getsomecat/GetSomeCats/Surge/modules/Panel/CFGPT/CFGPT\_new.sgmodule](https://raw.githubusercontent.com/getsomecat/GetSomeCats/Surge/modules/Panel/CFGPT/CFGPT\_new.sgmodule)

ChatGPT可用性检测（不带warp）：[https://raw.githubusercontent.com/getsomecat/GetSomeCats/Surge/modules/Panel/CFGPT/CFGPT\_newnowarp.sgmodule](https://raw.githubusercontent.com/getsomecat/GetSomeCats/Surge/modules/Panel/CFGPT/CFGPT\_newnowarp.sgmodule)

中国电信 Cookie：[https://raw.githubusercontent.com/FoKit/Scripts/main/rewrite/get\_10000\_cookie.sgmodule](https://raw.githubusercontent.com/FoKit/Scripts/main/rewrite/get\_10000\_cookie.sgmodule)

流媒体解锁检测：[https://raw.githubusercontent.com/w164955/Config/main/Surge/Panel/Stream-All-1.sgmodule](https://raw.githubusercontent.com/w164955/Config/main/Surge/Panel/Stream-All-1.sgmodule)

网络连通性测试：[https://raw.githubusercontent.com/getsomecat/GetSomeCats/Surge/modules/Connectivity\_Test.sgmodule](https://raw.githubusercontent.com/getsomecat/GetSomeCats/Surge/modules/Connectivity\_Test.sgmodule)

Reddit 去广告，简单粗暴测试中：[https://raw.githubusercontent.com/chouchoui/QuanX/master/Scripts/reddit/reddit.ad.sgmodule](https://raw.githubusercontent.com/chouchoui/QuanX/master/Scripts/reddit/reddit.ad.sgmodule)

知乎去广告：[https://raw.githubusercontent.com/blackmatrix7/ios\_rule\_script/master/script/zheye/zheye.sgmodule](https://raw.githubusercontent.com/blackmatrix7/ios\_rule\_script/master/script/zheye/zheye.sgmodule)

机场流量信息：[https://raw.githubusercontent.com/getsomecat/GetSomeCats/Surge/modules/Panel/Sub-info/Moore/Sub-info.sgmodule](https://raw.githubusercontent.com/getsomecat/GetSomeCats/Surge/modules/Panel/Sub-info/Moore/Sub-info.sgmodule)

TestFlight账户管理：[https://raw.githubusercontent.com/NobyDa/Script/master/Surge/Module/TestFlightAccount.sgmodule](https://raw.githubusercontent.com/NobyDa/Script/master/Surge/Module/TestFlightAccount.sgmodule)

网络延迟：[https://raw.githubusercontent.com/TributePaulWalker/Profiles/main/Surge/Module/Surge\_ConnectivityTest.sgmodule](https://raw.githubusercontent.com/TributePaulWalker/Profiles/main/Surge/Module/Surge\_ConnectivityTest.sgmodule)

解除微信链接限制：[https://raw.githubusercontent.com/zZPiglet/Task/master/UnblockURLinWeChat.sgmodule](https://raw.githubusercontent.com/zZPiglet/Task/master/UnblockURLinWeChat.sgmodule)

京东比价：[https://raw.githubusercontent.com/githubdulong/Script/master/jd\_price2.sgmodule](https://raw.githubusercontent.com/githubdulong/Script/master/jd\_price2.sgmodule)

Skip Proxy Lists：[https://raw.githubusercontent.com/mieqq/mieqq/master/skip-proxy-lists.sgmodule](https://raw.githubusercontent.com/mieqq/mieqq/master/skip-proxy-lists.sgmodule)

Bing Edge UA：[https://block.royli.dev/bing-edge-ua.sgmodule](https://block.royli.dev/bing-edge-ua.sgmodule)

General Settings Enhanced：[https://raw.githubusercontent.com/VirgilClyne/GetSomeFries/main/sgmodule/General.sgmodule](https://raw.githubusercontent.com/VirgilClyne/GetSomeFries/main/sgmodule/General.sgmodule)

酷我音乐：[https://raw.githubusercontent.com/I-am-R-E/Functional-Store-Hub/Master/KuWoMusic/KuWoMusic.Surge.sgmodule](https://raw.githubusercontent.com/I-am-R-E/Functional-Store-Hub/Master/KuWoMusic/KuWoMusic.Surge.sgmodule)

QX重写&规则集转化：[https://raw.githubusercontent.com/chengkongyiban/Surge/main/modules/QX\_to\_Surge.sgmodule](https://raw.githubusercontent.com/chengkongyiban/Surge/main/modules/QX\_to\_Surge.sgmodule)

获取捷停车userId：[https://raw.githubusercontent.com/getsomecat/GetSomeCats/Surge/modules/jtcgetuserid.sgmodule](https://raw.githubusercontent.com/getsomecat/GetSomeCats/Surge/modules/jtcgetuserid.sgmodule)

捷停车签到：[https://raw.githubusercontent.com/getsomecat/GetSomeCats/Surge/modules/jtccheckin.sgmodule](https://raw.githubusercontent.com/getsomecat/GetSomeCats/Surge/modules/jtccheckin.sgmodule)

去除 Youtube 广告：[https://raw.githubusercontent.com/Maasea/sgmodule/master/YoutubeAds.sgmodule](https://raw.githubusercontent.com/Maasea/sgmodule/master/YoutubeAds.sgmodule)

流量统计 [https://raw.githubusercontent.com/w164955/Config/main/Surge/Panel/TrafficStatistics.sgmodule](https://raw.githubusercontent.com/w164955/Config/main/Surge/Panel/TrafficStatistics.sgmodule)

启动时长 [https://raw.githubusercontent.com/w164955/Config/main/Surge/Panel/Surge\_Pro.sgmodule](https://raw.githubusercontent.com/w164955/Config/main/Surge/Panel/Surge\_Pro.sgmodule)

网络入口面板：[https://raw.githubusercontent.com/Keywos/rule/main/module/NetIspmini.sgmodule](https://raw.githubusercontent.com/Keywos/rule/main/module/NetIspmini.sgmodule)

节点延迟：[https://raw.githubusercontent.com/getsomecat/keywos/main/module/NetIspmini.sgmodule](https://raw.githubusercontent.com/getsomecat/keywos/main/module/NetIspmini.sgmodule)

实时油价：[https://raw.githubusercontent.com/getsomecat/GetSomeCats/Surge/modules/Panel/youjia.sgmodule](https://raw.githubusercontent.com/getsomecat/GetSomeCats/Surge/modules/Panel/youjia.sgmodule)

VPS流量监控：[https://raw.githubusercontent.com/getsomecat/GetSomeCats/Surge/modules/serverinfo.sgmodule](https://raw.githubusercontent.com/getsomecat/GetSomeCats/Surge/modules/serverinfo.sgmodule)

Safari 使用New Bing ：[https://raw.githubusercontent.com/getsomecat/GetSomeCats/Surge/modules/newbing.sgmodule](https://raw.githubusercontent.com/getsomecat/GetSomeCats/Surge/modules/newbing.sgmodule)

网速测试：[https://raw.githubusercontent.com/getsomecat/GetSomeCats/Surge/modules/Panel/Net\_Speed/Net\_Speed.sgmodule](https://raw.githubusercontent.com/getsomecat/GetSomeCats/Surge/modules/Panel/Net\_Speed/Net\_Speed.sgmodule)

检测ChatGPT解锁：[https://raw.githubusercontent.com/getsomecat/GetSomeCats/Surge/modules/Panel/CFGPT/CFGPT\_new.sgmodule](https://raw.githubusercontent.com/getsomecat/GetSomeCats/Surge/modules/Panel/CFGPT/CFGPT\_new.sgmodule)





[mu-lu-dao-hang.md](mu-lu-dao-hang.md "mention")







