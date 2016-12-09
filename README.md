# memcahed

安装memcahed  及配置


#安装
需要memcahe  及  libevent
 1.源码安装
 
 memcahe 依赖libevent
 安装  libevent   ./configure --prefix=/usr
 
 安装 memcahe  ./configure –with-libevent=/usr
 
 
 帮助信息   /usr/local/bin/memecached -h
 
 
 安装telnet   连接 memcahe
 yum intall telnet-server
 yum install telnet
 yum install xinetd
 
/usr/local/bin/memcached -d -m 10 -u root -l 192.168.192.134 -p 11211 -c 256 -P /tmp/memcached.pid
-d选项是启动一个守护进程，
-m是分配给Memcache使用的内存数量，单位是MB，这里是10MB，
-u是运行Memcache的用户，这里是root，
-l是监听的服务器IP地址，如果有多个地址的话，这里指定了服务器的IP地址192.168.0.200，
-p是设置Memcache监听的端口，这里设置了12000，最好是1024以上的端口，
-c选项是最大运行的并发连接数，默认是1024，这里设置了256，按照你服务器的负载量来设定，
-P是设置保存Memcache的pid文件，这里是保存在 /tmp/memcached.pid，

pstree |grep memcahe


telnet 192.168.192.134 11211



 
 
