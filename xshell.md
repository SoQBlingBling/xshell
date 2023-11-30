配置静态ip：



vi /etc/ssh/sshd_congfig

UseDMS no   修改

> 重启sshd

systemctl restart sshd

> 修改ip

cd /etc/sysconfig/network-script/

vi ifcfg-ems33

BOOTPROTO = 'static'  修改

IPADDR = 192.168.xxx.xx  //任意  添加ip

GATEWAY = 192.168.xx.xx//设置网关

NETMASK = xxx.xxx.xxx.xxxx

DMS1 = xxx.xxx.xxx.x

配置访问公网：

允许其他网络用户通过此计算机的internet连接来连接

cd /etc/sysconfig/network-script/

vi ifcfg-ems33

改为对应适配上的ip

wmware  将网关和ip设置为对应的ip值