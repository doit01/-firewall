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

firewall-cmd --permanent --add-rich-rule="rule family="ipv4" source address="10.128.29.194" accept"
firewall-cmd --permanent --add-rich-rule="rule family="ipv4" source address="10.128.29.161" accept"
firewall-cmd --permanent --add-rich-rule="rule family="ipv4" source address="10.128.29.195" accept"
firewall-cmd --permanent --add-rich-rule="rule family="ipv4" source address="10.28.140.2" accept"
firewall-cmd --permanent --add-rich-rule="rule family="ipv4" source address="10.28.140.3" accept"
firewall-cmd --permanent --add-rich-rule="rule family="ipv4" source address="10.28.140.4" accept"
firewall-cmd --permanent --add-rich-rule="rule family="ipv4" source address="10.31.94.189" accept"
firewall-cmd --permanent --add-rich-rule="rule family="ipv4" source address="10.31.95.209" accept"
firewall-cmd --permanent --add-rich-rule="rule family="ipv4" source address="10.31.95.187" accept"

firewall-cmd --permanent --add-rich-rule="rule family="ipv4" source address="10.31.94.29" accept"
firewall-cmd --permanent --add-rich-rule="rule family="ipv4" source address="10.31.95.21" accept"

firewall-cmd --permanent --zone=public --add-port=80/tcp
firewall-cmd --permanent --zone=public --add-port=81/tcp
firewall-cmd --permanent --zone=public --add-port=443/tcp
firewall-cmd --permanent --zone=public --add-port=20001/tcp
firewall-cmd --permanent --zone=public --add-port=5432/tcp



firewall-cmd --reload
