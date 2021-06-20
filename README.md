N1里面的是2021年5月23日的快照完整备份，
里面的功能相对比较全面，就是界面特别丑。
采用的是一键安装的策略。


以下内容来自http://wp.jinxiart.com/post/65.html


hassio_install
hassio 一键安装脚本，实现以下功能。

自动更改系统源为中科大源。（目前支持 Debian Ubuntu Raspbian 三款系统）

自动安装 Docker，可以选择切换 Docker 源为国内源，提高容器下载速度。

避开 Hassio 因亚马逊连接超时导致无法拉取最新版本的 Homeassistant 容器。

目前支持的系统
Raspbian

Ubuntu 测试版本 18.04 LTS通过，但按道理 16 以上都可以。

Debian 测试版本 9.5 通过。

使用方法
以 root 身份运行以下命令。

curl -sL -o install.sh https://raw.githubusercontent.com/neroxps/hassio_install/master/install.sh
chmod a+x install.sh
./install.sh




设备类型选型说明
raspberrypi : 树莓派1代

raspberrypi2 : 树莓派2代

raspberrypi3 : 树莓派3代（或3B+）

raspberrypi3-64  : 树莓派3代（或3B+）

qemuarm : 其余未知的arm设备（例如斐讯N1)

qemuarm-64 : 其余未知的arm设备（例如斐讯N1)

qemux86-64 : X86-64位系统通用（普通的PC机电脑）

qemux86 : X86-64位系统通用（普通的PC机电脑）

intel-nuc : 英特尔的nuc小主机



问题：
如果提示 curl: command not found ，那是因为没装 Curl

ubuntu/debian 系统安装 Curl 方法: apt-get update -y && apt-get install curl -y
centos 系统安装 Curl 方法: yum update -y && yum install curl -y
安装好 curl 之后就能安装脚本了
————————————————
版权声明：本文为CSDN博主「宋峥清」的原创文章，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/pang_ping/article/details/111994897