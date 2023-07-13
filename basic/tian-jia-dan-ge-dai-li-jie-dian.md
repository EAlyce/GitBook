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


```

\
官方手册：[https://manual.nssurge.com/policy/proxy.html](https://manual.nssurge.com/policy/proxy.html)\
\
如需更详细教学请查看[qi-ta-jiao-cheng.md](../qi-ta-jiao-cheng.md "mention")

返回导航页面：[mu-lu-dao-hang.md](../mu-lu-dao-hang.md "mention")
