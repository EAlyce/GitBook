# 配置同步

iOS端与Mac端标准配置基本通用，可以多设备同步使用

iOS端：在Surge中，更多—配置同步—选择iCloud云盘或者Dropbox（需代理环境）。

Mac端：在更多—配置—配置文件路径中修改，找到与iOS端云文件相同路径点击选择即可同步。

注意，配置同步速度受网络质量影响，以及个别参数仅限iOS或者Mac

```
compatibility-mode (iOS Only)
allow-wifi-access (iOS Only)
Allow Surge proxy services access from other devices in the LAN.

wifi-access-http-port (iOS Only)
The port number of Surge HTTP proxy service.

wifi-access-socks5-port (iOS Only)
The port number of Surge SOCKS5 proxy service.

wifi-access-http-auth (iOS Only)
Require authentication for Surge HTTP proxy service. E.g.: username:password

include-all-networks (iOS Only)
By default, some requests might not be taken over by Surge. For example, apps can bind to the physical network interface to bypass Surge VIF. Enabling the Include All Networks option to make sure all requests are handled by Surge without leaking. This option is useful when you use Surge as a firewall. (Requires iOS 14.0 or above)

Enabling this option may cause AirDrop and Xcode debugging issues, Surge Dashboard via USB not working, and other unexpected side effects. Use with caution.

include-local-networks (iOS Only)
Enable this option to make Surge VIF handle requests sent to LAN. (Requires iOS 14.2 or above)

Enabling this option may cause AirDrop and Xcode debugging issues, Surge Dashboard via USB not working, and other unexpected side effects. Use with caution.

wifi-assist (iOS Only)
Enable Wi-Fi assist.

hide-vpn-icon (iOS Only)
Hide the VPN icon in the status bar.

all-hybrid (iOS Only)
allow-hotspot-access (iOS Only)
Allow Surge proxy services access from other devices while Personal Hotspot is on.

use-default-policy-if-wifi-not-primary (macOS Only)
If disabled, SSID/BSSID patterns can still match even when Wi-Fi is not the primary network interface.

read-etc-hosts (macOS Only)
Follow local DNS mapping items in /etc/hosts.

http-listen (macOS Only)
The HTTP proxy service listen parameter. E.g.: 0.0.0.0:6152

socks5-listen (macOS Only)
The SOCKS5 proxy service listen parameter. E.g.: 0.0.0.0:6153
```
