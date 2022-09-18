# 虚拟机安装

如果你仍在学习过程中，建议使用虚拟机的方式安装，虚拟机方式的安装与实体机安装大同小异
建议参考如下文章进行安装
http://www.autolabor.com.cn/book/ROSTutorials/chapter1/12-roskai-fa-gong-ju-an-zhuang.html

# 实体机安装

一个真正的机器人运行时需要在实体机安装。
可以参考如下文字
https://blog.csdn.net/m0_60190682/article/details/118723468
也可以使用搜索引擎搜索"u盘安装 ubuntu20.04"



# 安装建议

安装界面大概如下图所示，

![](Ubuntu%2020.04的安装与配置/2022-09-18-03-23-50-image.png)





1. 建议安装之前先断网，否则安装过程可能会自动更新，而未换源之前更新将直接连接国外服务器，会导致安装进度巨慢无比。建议断网安装结束后，进系统后手动换源后手动更新。

2. 建议安装使用英文界面，不过Linux下中文不会像Windows那样轻易出现乱码情况（统一UTF-8编码），但是在纯终端界面下将会出现中文方块的情况。



# 虚拟机增强工具

> PS: 该内容仅虚拟机安装的用户需要关注。

当我们安装完虚拟机后，通过安装虚拟机增强工具可以使得虚拟机与物理机进行方便地交互。

如果我们使用的是VMware虚拟机，那么我们可进行如下操作，

![](Ubuntu%2020.04的安装与配置/2022-09-18-03-37-06-image.png)

然后我们发现出现了一个光盘设备，在此处打开终端

![](Ubuntu%2020.04的安装与配置/2022-09-18-03-38-23-image.png)

[在 Linux 虚拟机中手动安装 VMware Tools](https://docs.vmware.com/cn/VMware-Workstation-Pro/16.0/com.vmware.ws.using.doc/GUID-08BB9465-D40A-4E16-9E15-8C016CC8166F.html)

![](Ubuntu%2020.04的安装与配置/2022-09-18-03-46-22-image.png)

当提示上述信息时，增强工具便安装成功，然后可以输入`reboot`命令重启电脑。

重启之后你会发现虚拟机的分辨率将会随着虚拟机窗口而进行缩放，剪切板也可相互共享，大大提高的虚拟机的便捷性。

# 系统更新

断网安装完系统之后，就可以联网了。

> 由于现在Ubuntu 22.04已发布，可能会弹窗提示升级Ubuntu 22.04，请不要升级，因为后面我们需要安装的ROS1 的noetic发行版是需要绑定Ubuntu 20.04的发行版的。

需要先更换国内源，可以参考以下清华源或科大源的文档。

[ubuntu | 镜像站使用帮助 | 清华大学开源软件镜像站 | Tsinghua Open Source Mirror](https://mirrors.tuna.tsinghua.edu.cn/help/ubuntu/)

[Ubuntu 源使用帮助 &mdash; USTC Mirror Help 文档](https://mirrors.ustc.edu.cn/help/ubuntu.html)



更换国内源后便可通过以下命令更新apt源

```shell
sudo apt update
```

再运行以下命令执行系统软件包更新

```shell
sudo apt upgrade -y
```

![](Ubuntu%2020.04的安装与配置/2022-09-18-03-55-00-image.png)

更新完毕

# 中文输入法

中文输入法很有用，不管是写代码注释还是上网搜索均需要使用到中午输入。

如果你安装的是中文ubuntu，则已经会自带一个中文输入法；如果你安装的是英文ubuntu，则不会自带中文输入法。

不过，系统自带的中文输入法个人感觉较为难用。在此推荐安装使用搜狗输入法。

[搜狗输入法linux-首页](https://shurufa.sogou.com/linux)

官网已有详细的安装说明，再次不展开赘述。(需要严格执行官方帮助中的每一条命令，如果输入法还是无法正常使用，请再次重复执行)

将搜狗输入法加入输入法列表中。

![](Ubuntu%2020.04的安装与配置/2022-09-18-04-05-49-image.png)

此时已经能够输入中文了

![](Ubuntu%2020.04的安装与配置/2022-09-18-04-14-18-image.png)