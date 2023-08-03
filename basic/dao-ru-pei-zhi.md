# 导入配置

打开 Surge，在「**首页**」左上角点击配置名 - 「**从 URL 下载配置**」，**将输入框清除干净后**，粘贴懒人配置链接。\
\
若无法下载请新建空白配置，将内容复制粘贴即可。\
常用配置（排名不分先后）：

**深巷有喵**: [https://raw.githubusercontent.com/Rabbit-Spec/Surge/Master/Conf/Spec/Surge-Mini.conf](https://raw.githubusercontent.com/Rabbit-Spec/Surge/Master/Conf/Spec/Surge-Mini.conf)

全参数配置(仅作示例，不可使用）：[https://raw.githubusercontent.com/getsomecat/GetSomeCats/Surge/SurgePro.conf](https://raw.githubusercontent.com/getsomecat/GetSomeCats/Surge/SurgePro.conf)

**Surge开发者推荐的中国区用户最小配置**: [https://community.nssurge.com/d/1214](https://community.nssurge.com/d/1214)

最小配置远程引用版（第三方仓库）：[https://gist.githubusercontent.com/Zeaphyou/864aebea248ca1bb8000e0e5623b65f3/raw/c36413c715f43f22772d3c2353358e1ff936b2e6/Surge.conf](https://gist.githubusercontent.com/Zeaphyou/864aebea248ca1bb8000e0e5623b65f3/raw/c36413c715f43f22772d3c2353358e1ff936b2e6/Surge.conf)

**注意Surge配置写法严格区分大小写**

```
[General]
skip-proxy = 192.168.0.0/24, 10.0.0.0/8, 172.16.0.0/12, 127.0.0.1, localhost, *.local
exclude-simple-hostnames = true
internet-test-url = http://taobao.com/
proxy-test-url = http://www.apple.com/
test-timeout = 2
dns-server = 223.5.5.5, 114.114.114.114
# encrypted-dns-server = https://223.5.5.5/ // 除非当地 ISP 有严重的 DNS 污染问题，否则没必要开启 DoH，传统 DNS 的性能最优，网络异常后恢复速度最快
wifi-assist = true
ipv6 = false // 如无特殊需求不应开启 IPv6，目前网络环境下 IPv6 只会带来问题。

[Proxy Group]
Proxy = select, policy-path=机场订阅链接, update-interval=36000, no-alert=0, hidden=0, include-all-proxies=0, persistent=1

[Rule]
RULE-SET,https://github.com/Blankwonder/surge-list/raw/master/blocked.list,Proxy
RULE-SET,https://github.com/Blankwonder/surge-list/raw/master/cn.list,DIRECT
DOMAIN,apps.apple.com,Proxy
DOMAIN-SUFFIX,ls.apple.com,DIRECT // Apple Maps
DOMAIN-SUFFIX,store.apple.com,DIRECT // Apple Store Online
RULE-SET,SYSTEM,Proxy
RULE-SET,https://github.com/Blankwonder/surge-list/raw/master/apple.list,Proxy
# 以下规则将触发本地 DNS 解析
RULE-SET,LAN,DIRECT
GEOIP,CN,DIRECT
FINAL,Proxy,dns-failed

图片示例教程：
1、打开 Surge，在「首页」左上角点击配置名
```

![](../.gitbook/assets/photo\_3\_2022-11-16\_09-33-46.jpg)\
\
2、从 URL 下载配置\
![](../.gitbook/assets/photo\_1\_2022-11-16\_09-33-46.jpg)\
\
3、将输入框清除干净后，粘贴懒人配置链接。\
![](../.gitbook/assets/photo\_2\_2022-11-16\_09-33-46.jpg)\
\
4、点击完成\
![](../.gitbook/assets/photo\_8\_2022-11-16\_09-33-46.jpg)\
\
5、打开配置列表，选择在文本模式中编辑\
![](../.gitbook/assets/photo\_4\_2022-11-16\_09-33-46.jpg)\
\
6、找到 **\[Proxy Group]**,在该模块下 所有 的<mark style="color:red;">**policy-path=**</mark>后填写你的机场订阅\
![](../.gitbook/assets/photo\_5\_2022-11-16\_09-33-46.jpg)\
\
7、保存配置，返回首页\
![](../.gitbook/assets/photo\_6\_2022-11-16\_09-33-46.jpg)\
\
8、长按更新外部资源\
![](../.gitbook/assets/photo\_7\_2022-11-16\_09-33-46.jpg)\
\
\
\
\


返回导航页面：[mu-lu-dao-hang.md](../mu-lu-dao-hang.md "mention")
