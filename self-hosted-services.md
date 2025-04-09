## s01服务器上部署的自托管服务

目前在s01服务器上用docker部署了以下服务，后续考虑升级为容器编排，例如docker-compose。

名称|简介
---|---
Alist|支持多种存储的文件列表程序
calibre-web|calibre电子书的web app
Firefly III|免费、开源的个人财务管理软件
Home Assistant|智能家居平台，可接入多个平台的智能设备，例如小米、德业等。
Jellyfin|多媒体应用程序
qBittorent|BT下载软件
tinyMediaManager|一款媒体管理工具，为Kodi媒体中心（原XBMC）、MediaPortal 和 Plex 媒体服务器提供元数据。
v2fly|代理工具
windows|在容器中运行windows系统

后续可能考虑部署的服务有：
名称|简介
---|---
迅雷|BT下载，国内还是迅雷快
gitlab|当github不满足需求时，则考虑用本地部署的gitlab替换
