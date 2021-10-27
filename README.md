# Synology-Connect
通过群晖自带的 nginx 反向代理来解决群晖的外部访问问题
# 说明
大部分童鞋的 IPv4 的 80 和 443 端口都被关闭了。但是 IPv6 仍然是全端口开放。
此方法仅限于使用 IPv6 地址通过外网访问内网群晖。
PPPOE 上网动态 IP 需要依赖 dnspod-ipv6-ddns
# 安装方法
文件拷贝或创建在 /etc/nginx/conf.d 中 
然后执行 nginx -s stop 群晖会自动重启 nginx
