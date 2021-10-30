# Synology DSM Connect

通过群晖自带的 nginx 反向代理来解决群晖的外部访问问题

### 功能说明

此方法适用于使用 IPv6 地址通过外网访问内网群晖。

手机访问会处于 Loading 状态，电脑访问正常。DSM会判断客户端，但是为何无法打开DSM移动端尚不清楚。

PPPOE 上网动态 IP 需要依赖 [dnspod-ipv6-ddns](https://github.com/thxplus/dnspod-ipv6-ddns)

### 安装方法

文件拷贝或创建在 /etc/nginx/conf.d 中

然后执行 `sudo nginx -s stop` 群晖会自动重启 nginx

或者 `sudo synoservicecfg --restart nginx` 

刷新或重新访问地址。
