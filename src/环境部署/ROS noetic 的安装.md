# 参考文章

ROS的安装参考如下文章，

ROS官方wiki

[noetic/Installation/Ubuntu - ROS Wiki](http://wiki.ros.org/noetic/Installation/Ubuntu)

奥特学园

[1.2.4 安装 ROS · Autolabor-ROS机器人入门课程《ROS理论与实践》零基础教程](http://www.autolabor.com.cn/book/ROSTutorials/chapter1/12-roskai-fa-gong-ju-an-zhuang/124-an-zhuang-ros.html)

# ROS安装

配置完ROS源之后，使用

```shell
sudo apt install ros-noetic-desktop-full
```

即可开始漫长的安装过程。

> PS: Linux 绝大多数命令行输入都可以按键盘上的Tab键来自动补全，擅于使用补全有利于提高工作效率。

如下图将开始漫长的ROS安装过程（此时你可以把电脑放一边去吃个饭什么的），

![](ROS%20noetic%20的安装/2022-09-18-04-22-17-image.png)

下图便是下载完毕开始安装的步骤

![](ROS%20noetic%20的安装/2022-09-18-12-31-50-image.png)

# ROS配置

最终ROS将会被安装到/opt/ros/noetic目录下，此时还无法运行ros相关命令，我们可以在ros安装目录下发现setup.bash文件，该文件为ros环境的初始化文件。

使用命令

```shell
source /opt/ros/noetic/setup.bash
```

即可完成当前终端下的ros环境变量的配置。

此时运行`roscore`便可以启动ros master节点

![](ROS%20noetic%20的安装/2022-09-18-12-47-11-image.png)

为了方便使用不用每次启动终端都需要source，可将环境变量配置到.bashrc文件中

![](ROS%20noetic%20的安装/2022-09-18-12-49-31-image.png)

# ROS测试

开三个终端，每个终端分别运行如下命令

`roscore`

`rosrun turtlesim turtlesim_node`

`rosrun turtlesim turtle_teleop_key`

即可在第三个终端窗口下通过方向键操作第二个终端打开的小海龟窗口中的海龟了。

![](ROS%20noetic%20的安装/2022-09-18-12-54-16-image.png)


