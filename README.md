# v2ray 一键安装脚本 支持多种模式
*有问题请发 [issue](https://github.com/hacking001/v2ray-installers/issues)*

## 总览
- [已测试通过的系统](#已测试通过的系统)
- [注意事项](#注意事项)
- [常用命令](#常用命令)
- [安装](#安装)
    - [mKCP + WebSockets for Debian、Ubuntu](#mkcp--websockets-for-debainubuntu)
    - [mKCP + WebSockets for CentOS](#mkcp--websockets-for-centos)
    - [WebSockets for Debian、Ubuntu](#websockets-for-debianubuntu)
    - [WebSockets for CentOS](#websockets-for-centos)
    - [mKCP for Debian、Ubuntu](#mkcp-for-debianubuntu)
    - [mKCP for CentOS](#mkcp-for-centos)
- [安装 mKCP 的伪装版本](#安装-mkcp-的伪装版本)
    - [mKCP for Debian、Ubuntu with wechat-vedio mask](#mkcp-for-debianubuntu-with-wechat-vedio-mask)
    - [mKCP for CentOS with wechat-vedio mask](#mkcp-for-centos-with-wechat-vedio-mask)
    - [mKCP for Debian、Ubuntu with DTLS mask](#mkcp-for-debianubuntu-with-dtls-mask)
    - [mKCP for CentOS with DTLS mask](#mkcp-for-centos-with-dtls-mask)
- [安装附带 BBRLKL 的版本](#安装附带-bbrlkl-的版本)
    - [WebSockets for OpenVZ Debian、Ubuntu with BBRLKL](#websockets-for-openvz-debianubuntu-with-bbrlkl)
    - [WebSockets for OpenVZ CentOS](#websockets-for-openvz-centos-with-bbrlkl)
- [内核更新](#内核更新)
- [更新日志](#更新日志)

## 已通过测试的系统
- Ubuntu 18.04
- Ubuntu 16.04
- CentOS 7

理论上 v2ray 官方脚本能成功安装的系统，这里的都能安装成功

## 注意事项
- 请在干净的系统下安装
- v2ray 依赖系统时间，请确保系统 UTC 时间误差在三分钟以内，时区无关
- 与 Cloudflare 搭配的话请不要随便修改您的域名在 Cloudflare 上的设置（如果您不懂的话）
- WebSockets 模式支持 Cloudflare 前置，默认端口安装即可（懂的请随意）

## 常用命令
检查 v2ray 状态
```bash
service v2ray status
```
启动 v2ray 服务
```bash
service v2ray start
```
关闭 v2ray 服务
```bash
service v2ray stop
```
重启 v2ray 服务
```bash
service v2ray restart
```

## 安装
### mKCP + WebSockets for Debain、Ubuntu
```bash
wget -O mKCP-WebSockets.sh https://raw.githubusercontent.com/hacking001/v2ray-installers/master/mKCP-WebSockets.sh && bash mKCP-WebSockets.sh
```
### mKCP + WebSockets for CentOS
```bash
wget -O mKCP-WebSockets.sh https://raw.githubusercontent.com/hacking001/v2ray-installers/master/mKCP-WebSockets_CentOS.sh && bash mKCP-WebSockets.sh
```
### WebSockets for Debian、Ubuntu
```bash
wget -O WebSockets.sh https://raw.githubusercontent.com/hacking001/v2ray-installers/master/WebSockets.sh && bash WebSockets.sh
```
### WebSockets for CentOS
```bash
wget -O WebSockets.sh https://raw.githubusercontent.com/hacking001/v2ray-installers/master/WebSockets_CentOS.sh && bash WebSockets.sh
```
### mKCP for Debian、Ubuntu
```bash
wget -O mKCP.sh https://raw.githubusercontent.com/hacking001/v2ray-installers/master/mKCP.sh && bash mKCP.sh
```
### mKCP for CentOS
```bash
wget -O mKCP.sh https://raw.githubusercontent.com/hacking001/v2ray-installers/master/mKCP_CentOS.sh && bash mKCP.sh
```

## 安装 mKCP 的伪装版本
### mKCP for Debian、Ubuntu with wechat-vedio mask
```bash
wget -O mKCP-Wx.sh https://raw.githubusercontent.com/hacking001/v2ray-installers/master/mKCP-Wx.sh && bash mKCP-Wx.sh
```
### mKCP for CentOS with wechat-vedio mask
```bash
wget -O mKCP-Wx.sh https://raw.githubusercontent.com/hacking001/v2ray-installers/master/mKCP-WeChatVedio_CentOS.sh && mKCP-Wx.sh
```
### mKCP for Debian、Ubuntu with DTLS mask
```bash
wget -O mKCP-DTLS.sh https://raw.githubusercontent.com/hacking001/v2ray-installers/master/mKCP-DTLS.sh && bash mKCP-DTLS.sh
```
### mKCP for CentOS with DTLS mask
```bash
wget -O mKCP-DTLS.sh https://raw.githubusercontent.com/hacking001/v2ray-installers/master/mKCP-DTLS_CentOS.sh && mKCP-DTLS.sh
```

## 安装附带 BBRLKL 的版本
### WebSockets for OpenVZ Debian、Ubuntu with BBRLKL
```bash
wget -O WebSockets-BBRLKL.sh https://raw.githubusercontent.com/hacking001/v2ray-installers/master/WebSockets-BBRLKL.sh && bash WebSockets-BBRLKL.sh
```
### WebSockets for OpenVZ CentOS with BBRLKL
```bash
wget -O WebSockets-BBRLKL.sh https://raw.githubusercontent.com/hacking001/v2ray-installers/master/WebSockets-BBRLKL_CentOS.sh && bash WebSockets-BBRLKL.sh
```

## 内核更新
```bash
wget -O v2ray-installer.sh https://install.direct/go.sh && bash v2ray-installer.sh && rm -f v2ray-installer.sh
```
来源：[下载安装 · Project V 官方网站](https://www.v2ray.com/chapter_00/install.html)

## 更新日志
### 2018 年 11 月 13 日
- 增加 mKCP 的 DTLS 伪装模式
### 2018 年 11 月 2 日
- 更新配置文件格式，采用新版的配置格式
### 2018 年 8 月 6 日
- 项目初始化