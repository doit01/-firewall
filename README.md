# -firewall
https://blog.csdn.net/Javastudying_/article/details/111949723
关闭防火墙： systemctl stop firewalld
开机自关闭： systemctl disable firewalld
打开防火墙： systemctl start firewalld
开机自打开： systemctl enable firewalld
配置 firewalld-cmd

查看防火墙状态： firewall-cmd --state
查看所有打开的端口： firewall-cmd --zone=public --list-ports
使配置生效： firewall-cmd --reload 

firewall-cmd --permanent --zone=public --add-port=81/tcp
firewall-cmd --reload

