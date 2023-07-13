# 添加单个代理节点

推荐使用UI操作：\[打开Surge]->\[首页]->\[代理服务器]->\[选择代理类型]->\[填入相应节点参数即可]\
\
创建完成后，可以打开首页->代理服务器->新建策略组->将节点拖放至包含的策略

\
文本模式编辑，示例

```
[Proxy]
ProxyHTTP = http, 1.2.3.4, 443, username, password
ProxyHTTPS = https, 1.2.3.4, 443, username, password
ProxySOCKS5 = socks5, 1.2.3.4, 443, username, password
ProxySOCKS5TLS = socks5-tls, 1.2.3.4, 443, username, password, skip-common-name-verify=true

# 写法是 策略名 = 代理类型,代理地址，端口号，用户名，密码
# 不同的类型填写的具体项目会有差异，建议在 UI 界面中填写
# 策略名不可重复，策略名须先定义才能在其它部分引用
# Proxy01 = https,adc-us.com,443,username = 用户名,password = 密码
# Proxy02 = ss, abc-kt.com, 443, encrypt-method = rc4-md5, password = 密码
# Proxy03 = socks5, abc-cn.com, 443, username = 用户名, password = 密码
# 代理链 Proxy chain：可以通过一个代理跳板使用另一个代理，可以无限嵌套使用。
# ProxyB = trojan, example.com, 443, password=password1, skip-cert-verify=true, underlying-proxy=ProxyA/Proxies
# 如上示例，在使用 ServerB 时是通过 ServerA 到 ServerB：
# Surge <--> ProxyA/Proxies <--> ProxyB <--> Internet
# Proxy = select, Auto, Proxy01 , Proxy02, Proxy03

# 内置策略
# DIRECT 表示将该请求直接发往目标服务器
# REJECT 表示拒绝该请求，当连接类型为 HTTP 时，会返回一个错误页面。（该行为可被 show-error-page-for-reject 参数控制）
# REJECT-TINYGIF 表示拒绝该请求，当连接类型为 HTTP 时，返回一个 1px 的 GIF 图片响应。若为其他类型连接则直接断开。该策略主要用于 Web 广告屏蔽。
# REJECT-DROP 表示拒绝该请求，与 REJECT 不同的是，该策略将静默抛弃请求。因为部分程序有着十分暴力的重试逻辑，连接失败后会立刻进行重试，导致请求风暴。如果发往某主机名的请求短时间内大量触发 REJECT/REJECT-TINYGIF 策略（当前版本的阈值为 30 秒内 10 次），为了避免产生大量资源浪费，Surge 将自动升级策略为 REJECT-DROP 策略。
# REJECT-NO-DROP 表示不使用默认的自动丢包逻辑，这样 Surge 每次都会返回 ICMP Port Unreachable，应用会立刻回退而不是等超时。
# CELLULAR 表示优先使用数据网络；
# CELLULAR-ONLY 表示仅使用数据网络；
# HYBRID 表示尝试并发使用 Wi-Fi 和数据网络建立连接，仅当混合网络开关未开启时有意义。
# NO-HYBRID 表示当 Wi-Fi可用时永不尝试数据网络，仅当混合网络或 i-Fi 助力选项开启时有意义。
# - 新增 IPv4 & IPv6 偏好参数，对于所有策略，可附带参数 ip-version=，可选参数有：
# * dual：默认行为，在双栈网络上将并发使用 v4 和 v6 地址并选取最快速的结果。
# * prefer-v4：若DNS解析获得了 A 与 AAAA 记录，优先使用 A 记录，否则使用 AAAA 记录。
# * prefer-v6：若DNS解析获得了 A 与 AAAA 记录，优先使用 AAAA 记录，否则使用 A 记录。
# * v4-only：仅使用 A 记录，若未获得A记录则失败。
# * v6-only：仅使用 AAAA 记录，若未获得 AAAA 记录则失败。
# 可配合 direct 类型策略使用，如：IPV6-ONLY = direct, ip-version=v6-only
# DIRECT = direct, ip-version=prefer-v4
# HYBRID = direct, hybrid=true, ip-version=dual

```

\
官方手册：[https://manual.nssurge.com/policy/proxy.html](https://manual.nssurge.com/policy/proxy.html)\
\
如需更详细教学请查看[qi-ta-jiao-cheng.md](../qi-ta-jiao-cheng.md "mention")

返回导航页面：[mu-lu-dao-hang.md](../mu-lu-dao-hang.md "mention")
