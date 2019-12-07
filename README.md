# 查看到进程占用的端口号
2、	netstat -anp | grep pid
	
	
2、查看8000端口的使用情况
lsof -i:8000

3、netstat命令各个参数说明如下：

　　-t : 指明显示TCP端口

　　-u : 指明显示UDP端口

　　-l : 仅显示监听套接字(所谓套接字就是使应用程序能够读写与收发通讯协议(protocol)与资料的程序)

　　-p : 显示进程标识符和程序名称，每一个套接字/端口都属于一个程序。

　　-n : 不进行DNS轮询，显示IP(可以加速操作)

4、查看当前所有tcp端口·

netstat -ntlp  

查看所有80端口使用情况

netstat -ntulp |grep 80  


# 安装php
1、rpm -Uvh https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
2、yum provides php 升级
3、yum install php72w php72w-fpm php72w-cli php72w-common php72w-devel php72w-gd php72w-pdo php72w-mysql php72w-mbstring php72w-bcmath 
4、systemctl start php-fpm