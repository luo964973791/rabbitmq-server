## 具体参考文档： https://github.com/rabbitmq/erlang-rpm  

-------------------------------------------------------------------------  
#centos 6 安装 方法  
yum install epel-release -y && yum install wget socat lrzsz -y  
wget https://github.com/rabbitmq/rabbitmq-server/releases/download/v3.7.11/rabbitmq-server-3.7.11-1.el6.noarch.rpm  
vi /etc/yum.repos.d/rabbitmq-erlang.repo  
[rabbitmq-erlang]  
name=rabbitmq-erlang  
baseurl=https://dl.bintray.com/rabbitmq-erlang/rpm/erlang/20/el/6  
gpgcheck=1  
gpgkey=https://dl.bintray.com/rabbitmq/Keys/rabbitmq-release-signing-key.asc  
repo_gpgcheck=0  
enabled=1  

#yum 安装 并且加入开机自启动   
yum install rabbitmq-server-3.7.11-1.el6.noarch.rpm -y && chkconfig rabbitmq-server on  

------------------------------------------------------------------------- 

#centos7 安装  
To use Erlang 20.3.x on CentOS 7:  
yum install epel-release -y && yum install wget socat lrzsz -y  
wget https://github.com/rabbitmq/rabbitmq-server/releases/download/v3.7.11/rabbitmq-server-3.7.11-1.el7.noarch.rpm  
vi /etc/yum.repos.d/rabbitmq-erlang.repo  
[rabbitmq-erlang]  
name=rabbitmq-erlang  
baseurl=https://dl.bintray.com/rabbitmq-erlang/rpm/erlang/20/el/7  
gpgcheck=1  
gpgkey=https://dl.bintray.com/rabbitmq/Keys/rabbitmq-release-signing-key.asc  
repo_gpgcheck=0  
enabled=1  

#yum 安装 并且加入开机自启动   
yum install rabbitmq-server-3.7.11-1.el7.noarch.rpm -y && systemctl enable rabbitmq-server  

-------------------------------------------------------------------------
