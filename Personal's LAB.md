# Configuration
inGoosey's Surge Configuration.

# Surge Configuration
[General]
# 日志级别
loglevel = notify
# IPv6 相关
ipv6 = false
ipv6-vif = disabled
# 游戏优化
udp-priority = true
# Web 管理界面
http-api-web-dashboard = true
# 允许 Wi-Fi 访问 (仅 iOS，若允许远程访问将 false 改为 true )
allow-wifi-access = false
wifi-access-http-port = 6152
wifi-access-socks5-port = 6153
# 允许 Wi-Fi 访问 (仅 macOS，若允许远程访问将 127.0.0.1 改为 0.0.0.0 )
http-listen = 127.0.0.1:6152
socks5-listen = 127.0.0.1:6153
# 跳过代理
skip-proxy = 127.0.0.1, 192.168.0.0/16, 10.0.0.0/8, 172.16.0.0/12, 100.64.0.0/10, localhost, *.local
# 域名系统服务器
dns-server = 119.29.29.29, 223.5.5.5
# encrypted-dns-server = https://doh.pub/dns-query
# 排除简单主机名
exclude-simple-hostnames = true
# 测试超时（秒）
test-timeout = 3
# 网络测试 URL
internet-test-url = http://connectivitycheck.platform.hicloud.com/generate_204
# 代理测试 URL
proxy-test-url = http://cp.cloudflare.com/generate_204
# 自定义 GeoIP 数据库
geoip-maxmind-url = https://github.com/Hackl0us/GeoIP2-CN/raw/release/Country.mmdb

[Proxy]
# 香港 台湾 日本 狮城 美国 边缘

[Rule]
# inGoosey 用户自定义设置分流规则
# 抖音分流规则
# RULE-SET,https://raw.githubusercontent.com/ingoosey/Configuration/main/Ruleset/RULE-SET/DouYin.list,边缘
# 游戏分流规则
RULE-SET,https://raw.githubusercontent.com/ingoosey/Configuration/main/Ruleset/RULE-SET/Games.list,香港
# Open AI 分流规则
RULE-SET,https://raw.githubusercontent.com/ingoosey/Configuration/main/Ruleset/RULE-SET/ChatGPT.list,美国
# PayPal 分流规则
RULE-SET,https://raw.githubusercontent.com/ingoosey/Configuration/main/Ruleset/RULE-SET/PayPal.list,美国
# Ultra Mobile 分流规则
RULE-SET,https://raw.githubusercontent.com/ingoosey/Configuration/main/Ruleset/RULE-SET/Ultra.list,美国
# Telegram 分流规则
RULE-SET,https://raw.githubusercontent.com/ingoosey/Configuration/main/Ruleset/RULE-SET/Telegram.list,代理
# macOS的词典和维基百科搜索集成的分流规则 需要开启Surge的增强模式
RULE-SET,https://raw.githubusercontent.com/ingoosey/Configuration/main/Ruleset/RULE-SET/Siri.list,代理
# Google 分流规则
RULE-SET,https://raw.githubusercontent.com/ingoosey/Configuration/main/Ruleset/RULE-SET/Google.list,代理
# 流媒体域名列表
RULE-SET,https://raw.githubusercontent.com/ingoosey/Configuration/main/Ruleset/RULE-SET/Streaming.list,媒体
# 来自 Apple 和 iCloud 可直接连接的域名合集
DOMAIN-SET,https://raw.githubusercontent.com/ingoosey/Configuration/main/Ruleset/DOMAIN-SET/Apple.list,DIRECT
DOMAIN-SET,https://raw.githubusercontent.com/ingoosey/Configuration/main/Ruleset/DOMAIN-SET/iCloud.list,DIRECT
# 局域网的相关请求
RULE-SET,LAN,DIRECT
# 中国大陆 GeoIP2 数据库的请求
GEOIP,CN,DIRECT
# 为匹配的最终请求
FINAL,代理,dns-failed
