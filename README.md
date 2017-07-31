服务器配置

##linux常用命令
uname -a   查看系统
ps -ef|grep  java  查看系统是否有java线程正在运行
ll 查看文件
rm -rf 递归删除
mkdir 创建文件夹
cd  读取目录
cd ~    cd /
./xxx    运行xxx程序
sudo   管理员模式
exit   退出


vim编辑器，来用编辑配置文件等等
vim  wenjian  文件
常用功能键使用
i   插入
u   撤销
dd  删除行
esc :  q 退出不保存
esc : wq! 退出保存

ubuntu 系统
apt-get 获取安装包
其他linux
yum
rpm 都是安装

从网络上下载文件命令
eg：从网络上下载tomcat
wget  http://mirror.bit.edu.cn/apache/tomcat/tomcat-8/v8.5.16/bin/apache-tomcat-8.5.16.tar.gz

有需要使用下载完成之后解压的
解压命令为  tar  
tar
-c: 建立压缩档案
-x：解压
-t：查看内容
-r：向压缩归档文件末尾追加文件
-u：更新原压缩包中的文件

这五个是独立的命令，压缩解压都要用到其中一个，可以和别的命令连用但只能用其中一个。下面的参数是根据需要在压缩或解压档案时可选的。

-z：有gzip属性的
-j：有bz2属性的
-Z：有compress属性的
-v：显示所有过程
-O：将文件解开到标准输出

下面的参数-f是必须的

-f: 使用档案名字，切记，这个参数是最后一个参数，后面只能接档案名。

## make
有文件在解压完成之后进入到解压文件夹下执行
make install


#问题
对于有问题不明确的需要看日志，tomcat有日志文件夹
tail命令
-f 是自动刷新
-n 是行数
使用tail -f -n 1000  xxx.log


nginx 启动
进入到nginx 目录下
nginx -t -c /path/to/nginx.conf 测试nginx配置文件是否正确
nginx -s reload   重启

tomcat启动  
进入到tomcat文件下

nginx反向代理到tomcat
http://www.linuxidc.com/Linux/2015-03/115208.htm

每次更改配置文件，相应的服务都应该重启。
eg：改变了nginx的配置文件，那么就应该重启nginx服务


#以下是公司服务器的路径
 文件的安装路径一般都是在 /var/lib/
 配置路径在 ect/

cd   /var/lib/tomcat7
是各种启动tomcat的
service tomcat7
force-reload  start         stop
restart       status        try-restart

##ningx配置路径
/etc/nginx/sites-enabled/
