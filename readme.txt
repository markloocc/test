huifukejian commented on Aug 8, 2020
可以看下我的，日常用起来还可以， 没什么问题

force-AAAA-SOA yes
conf-file /etc/smartdns/smartdns-domains.china.conf
speed-check-mode tcp:443,tcp:80,ping
bind: 6053 -group china
bind: 5335 -group gfwlist

server-https https://doh.pub/dns-query -group china -exclude-default-group
server-https https://223.5.5.5/dns-query -group china -exclude-default-group

server-tls 1.0.0.1:853 -group gfwlist
server-tls 8.8.4.4:853 -group gfwlist

/etc/smartdns/smartdns-domains.china.conf 加载中国域名文件，生成的脚本代码
https://github.com/huifukejian/test/blob/master/update-china-list.sh
弄个定时脚本每天执行一次就可以了
