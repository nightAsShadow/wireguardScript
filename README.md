# wireguardScript
wireguard安装卸载脚本

# 使用方法
## 使用前修改参数
修改脚本中的
ipv4ServerAddress
ipv6ServerAddress
publicAddress
UDPListenPort
ClientAllowedIPs
几个字段,
其中publicAddress为必须修改字段 <br>
生成客户端配置文件，需要输入客户端的hostname，自动生成hostname+wg.conf <br>

## 脚本使用
### 服务端安装
su - <br>
chmod +x  wireguard.sh #给脚本执行权限<br>
./wireguard.sh <br>
选择1 <br>
PostUp/1PostDown启动停止VPN接口之后运行的命令，开启了转发 <br>
 默认自动开机启动 <br>
![image](https://github.com/nightAsShadow/wireguardScript/blob/main/img/install.png) <br>
### 启动
### 客户端安装
su - <br>
chmod +x  wireguard.sh #给脚本执行权限<br>
./wireguard.sh <br>
选择2 <br>
![image](https://github.com/nightAsShadow/wireguardScript/blob/main/img/clientinstall.png) <br>

### 客户端配置文件生成
./wireguard.sh  #在服务端运行<br>
选择3 <br>
client name 取客户端的hostname，生成的文件是hostname+wg.conf<br>
输入分配给该客户端的ipv4和ipv6地址
![image](https://github.com/nightAsShadow/wireguardScript/blob/main/img/createclientconf.png) <br>
![image](https://github.com/nightAsShadow/wireguardScript/blob/main/img/createclientconf1.png) <br>
<br>

./wireguard.sh  #在服务端运行<br>
从服务端获取客户端的配置文件<br>
![image](https://github.com/nightAsShadow/wireguardScript/blob/main/img/startclientconf.png) <br>
把配置写入到客户端中<br>
![image](https://github.com/nightAsShadow/wireguardScript/blob/main/img/startcreateclientconf.png) <br>
### 客户端和服务端启动
./wireguard.sh<br>
默认配置文件为hostname+wg.conf <br>
![image](https://github.com/nightAsShadow/wireguardScript/blob/main/img/startclient.png) <br>


### 卸载
./wireguard.sh <br>
选择5 <br>
![image](https://github.com/nightAsShadow/wireguardScript/blob/main/img/uninstall.png) <br>
<br>

# 问题
目前测试了debian11，ubuntu22.04。centos7，arch
使用过程中碰到问题请联系我，感谢!!!
