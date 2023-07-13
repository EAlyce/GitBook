# 机场订阅

\
**1、**从机场个人订阅管理界面一键导入Surge\
\
**2、**本地配置，直接分享到Surge即可\
\
**3、**在[dao-ru-pei-zhi.md](dao-ru-pei-zhi.md "mention")后，进入文本编辑模式，找到\[Proxy Group],找到**policy-path=，填写 机场订阅链接** 即可\
\
**4、**若已有机场托管配置，只需[dao-ru-pei-zhi.md](dao-ru-pei-zhi.md "mention")即可\
\
如果没有Surge托管配置，但节点协议支持Surge使用，可以在[ding-yue-zhuan-huan.md](ding-yue-zhuan-huan.md "mention")，进行转换后[dao-ru-pei-zhi.md](dao-ru-pei-zhi.md "mention")使用。

\
亦可直接引用其他配置中的节点或策略组：[https://kb.nssurge.com/surge-knowledge-base/v/zh/guidelines/detached-profile](https://kb.nssurge.com/surge-knowledge-base/v/zh/guidelines/detached-profile)

```
示例：

[Proxy]
#!include Proxy1.dconf, Proxy2.dconf

[Proxy Group]
#!include Group.dconf
```

\
**注意事项：Surge 5 目前支持以下协议：HTTP、HTTPS、SOCKS5、SOCKS5 via TLS、Snell、Shadowsocks、VMess、Trojan、SSH、WireGuard、TUIC**\
\


返回导航页面：[mu-lu-dao-hang.md](../mu-lu-dao-hang.md "mention")
