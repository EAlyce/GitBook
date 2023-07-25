# 第三方工具

**一、Boxjs**\
\
BoxJs 是一款运行在 Surge、Quantumult X、Loon、Shadowrocket、Stash 环境下的脚本！\
\
相关文档：[https://docs.boxjs.app/](https://docs.boxjs.app/)

安装链接：[https://raw.githubusercontent.com/chavyleung/scripts/master/box/rewrite/boxjs.rewrite.surge.sgmodule](https://raw.githubusercontent.com/chavyleung/scripts/master/box/rewrite/boxjs.rewrite.surge.sgmodule)

安装完成后，打开重写，脚本，Mitm三个开关

访问 [http://boxjs.com](http://boxjs.com)

**二、Sub-Store**\
\
适用于 Loon 、 Surge 和 Quantumult X 的高级订阅管理工具。完全本地解析，无订阅泄露的风险。

模块安装链接：[https://raw.githubusercontent.com/sub-store-org/Sub-Store/master/config/Surge.sgmodule](https://raw.githubusercontent.com/sub-store-org/Sub-Store/master/config/Surge.sgmodule)\
\
安装完成后

1. 确认安装substore模块，并且安装证书和信任证书。
2. 开启全局代理更新外部资源，确认全部资源更新成功。
3. 将模块生效顺序放到最底部。
4. 开启Mitm,脚本,重写这三个开关。
5. 代理规则添加「DOMAIN-SUFFIX」→「vercel.app」走代理节点\
   \
   访问：[https://sub.store/](https://sub.store/)

**三、Geoip**\
\
&#x20;      \[首页]->\[更多设置]->\[Geoip数据库]\
\
&#x20;      第三方Geoip数据库推荐：\
\
&#x20;      **1、**[https://raw.githubusercontent.com/NobyDa/geoip/release/Private-GeoIP-CN.mmdb](https://raw.githubusercontent.com/NobyDa/geoip/release/Private-GeoIP-CN.mmdb)\
\
&#x20;      **2、**[https://raw.githubusercontent.com/Hackl0us/GeoIP2-CN/release/Country.mmdb](https://raw.githubusercontent.com/Hackl0us/GeoIP2-CN/release/Country.mmdb)\
\
&#x20;   **3、**[https://raw.githubusercontent.com/Loyalsoldier/geoip/release/Country-only-cn-private.mmdb](https://raw.githubusercontent.com/Loyalsoldier/geoip/release/Country-only-cn-private.mmdb)\


**四、Script Hub**

• 支持将 QX 重写解析至 Surge Shadowrocket Loon Stash

• 支持将 Surge 模块解析至 Loon Stash

• 支持将 Loon 插件解析至 Surge Shadowrocket Stash

• 支持 QX & Surge & Loon & Shadowrocket & Clash 规则集解析，适用 app: Surge Shadowrocket Stash Loon (注：不支持 域名集 IP-CIDR 集)

• 支持 将 QX 脚本转换成 Surge 脚本(兼容)

• 支持一键导入 Shadowrocket / Loon

• 相关生态: [Surge 模块工具](https://github.com/Script-Hub-Org/Script-Hub/wiki/%E7%9B%B8%E5%85%B3%E7%94%9F%E6%80%81:-Surge-%E6%A8%A1%E5%9D%97%E5%B7%A5%E5%85%B7) 支持一键导入 Surge

原仓库：[https://github.com/Script-Hub-Org/Script-Hub](https://github.com/Script-Hub-Org/Script-Hub)

安装模块：[https://raw.githubusercontent.com/Script-Hub-Org/Script-Hub/main/modules/script-hub.surge.sgmodule](https://raw.githubusercontent.com/Script-Hub-Org/Script-Hub/main/modules/script-hub.surge.sgmodule)

在安装完成, 并且更新全部外部资源之后:

如果你已经完成了信任证书 开启 MitM 等常规操作

应该可以正常访问 [https://script.hub](https://script.hub)

如果你实在搞不定什么是信任证书 开启 MitM

访问[http://script.hub](http://script.hub) 也可以, 不保证功能完整性

可在 Safari 的共享中选择 "添加到主屏幕"，Script Hub 将以全屏模式运行

使用文档：[https://github.com/Script-Hub-Org/Script-Hub/wiki](https://github.com/Script-Hub-Org/Script-Hub/wiki)

返回导航页面：[mu-lu-dao-hang.md](mu-lu-dao-hang.md "mention")
