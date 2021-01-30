yum install bind bind-utils  -y



修改文件

/etc/named.conf

/etc/named.github.zones

/var/named/amazonaws.com.zone
/var/named/fastly.net.zone
/var/named/github.com.zone
/var/named/github.community.zone
/var/named/github.io.zone
/var/named/githubassets.com.zone
/var/named/githubstatus.com.zone
/var/named/githubusercontent.com.zone



启动服务

systemctl statr named

设为开机启动

systemctl enable named



然后将服务，在防火墙上放行：

firewall-cmd *--add-service=dns --permanent* 

firewall-cmd *--reload*