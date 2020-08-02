WINDOWS CMD 使用SSH登录LINUX云服务器
ssh -p 端口（22） 用户名@IP
例：
ssh -p 22 root@106.13.49.201
默认端口为22
经试验，Linux云已经默认装了SSH，不知道是自带的时候不小心装了。。

Linux查看端口是否开启,8000为例，如果没反馈则没有开启
lsof -i:8000



ps -ef | grep 命令查看指定服务是否启动
ps -e| grep 服务名

ps -e |grep ntp命令 详解
ps：进程查看命令
-A 显示所有程序
-e 此参数的效果与指定"A"参数相同
-f 显示UID，PPIP，C与STIME栏位
服务名可以采用启动命令中的关键词

OPENSSH——需确认FRP是否用到（目前是用PUTTY)

FRP


问题1：
如何直接在Linux终端中下载GitHub中的如下资源（release）

下载方式纠正，类似这种release文件夹下面的资源，直接点右键复制下载链接，然后在Linux上面wget
wget下载包太慢，采用Windows下载，然后宝塔上传到需要的Linux目录