##  树莓派配置（无显示屏）
关于树莓派3B+(2018.6.7)： 经测试树莓派不能安装ubuntu mate系统，这个系统只针对3B;

- 系统下载：[RASPBIAN](https://www.raspberrypi.org/downloads/raspbian/) 系统分为完整型和网络安装型，这里选完整型；

- 使用[Win32DiskImager](https://sourceforge.net/projects/win32diskimager/) 软件安装系统；

- 在SD卡里添加 SSH 文件 ( 默认系统不开启SSH )，或者树莓派命令行敲 sudo raspi-config 开启ssh服务；

- 使用网线连接树莓派，设置电脑的 WLAN 网络共享给本地连接；

- 打开电脑 cmd 输入 arp-a 获取IP地址 例如：192.168.139.126；

- 电脑端使用 putty 连接树莓派；

## 电脑端使用xrdp、vnc远程连接树莓派

    sudo apt-get install xrdp
    sudo  /etc/initd/xrdp defaults
    sudo apt-get install tightvnserver

    sudo apt-get install Vnc4server
    // 设置分辨率 只有VNC需要设置
    sudo vim /boot/config.txt

## 安装scim-pinyin 配置中文环境

    sudo raspi-config
    >> change locale
    >> zh_CN.UTF-8 UTF-8

    sudo apt-get install scim-pinyin
    scim // 激活输入法

## 使用 winScp 管理树莓派文件系统

  - 下载winScp [winScp](https://winscp.net/eng/download.php)

## 安装 cheese 拍照

    sudo apt-get install cheese
