### 树莓派安装失败经验

硬件材料：

- 树莓派3B+
- 5V1A适配器
- HDMI转VGA头
- 8G class4 金士顿内存卡
- 键盘，显示器
- 网线一条

安装失败判断：1、SD卡的速度大小不够 2、官方系统问题 3、

额外知识：

- 红灯常亮表示电源稳定，给HDMI转VGA插头供电减少树莓派负担
- 绿灯闪表示系统正在工作
- 通过网线可以共享网络给树莓派，并可通过Putty，VNC控制树莓派([Ubuntu](https://www.embbnux.com/2014/03/24/on_ubuntu_use_vnc_connect_raspberry/)、[Windows](http://blog.csdn.net/github_38111866/article/details/76038665))

软件材料：

- [Win32DiskImager](https://sourceforge.net/projects/win32diskimager/)
- [系统镜像](https://www.raspberrypi.org/downloads/)
- [Putty](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html)
- [SDFormatter](https://www.sdcard.org/downloads/formatter_4/)

安装方式(NOOBS):

- 第一次： 安装时间1小时，赋值NOOBS下的文件到SD卡中，安装中途报错卡死
- 第二次： 安装结束后文件显示不完整报错
- 第三次： 安装成功，进入系统后卡死在初始化

安装方式(2017-11-29-raspbian-stretch):

- 第一次：利用Win32DiskImager安装镜像到SD卡大概20分钟，树莓派初始化报错,自动登陆用户pi，没有修改用户的权限，修改root密码失败，不能安装软件，无法切入界面，df命令查看找不到/boot系统引导分区。
- 第二次：相同
- 第三次：相同

安装方式(ubuntu-mate-16.04.2-desktop-armhf-raspberry-pi)

- 第一次：利用Win32DiskImager安装镜像到SD卡大概20分钟，安装过程就像安装Ubuntu一样，安装成功，只是系统运行有点卡。


NOOBS初始化报错：

![initError](/install/bug3.jpg)

Boot分区未挂载：

![BootError](/install/bug2.jpg)

raspbian初始化报错：

![initErrot](/install/bug1.jpg)
