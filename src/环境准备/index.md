## 运行环境
操作系统: Ubuntu20.04

ROS版本: 使用与 Ubuntu 20.04 配套的 ROS 的 Noetic 版本。

ROS Noetic与之前的版本最大的一个不同就是其Python环境的变更，在ROS melodic,kinetic 及更早的版本，使用的是 Python2.7 的运行环境，而 Noetic 原生完美支持 Python3.8 的运行环境，给我们的机器人开发带来了非常先进的 Python 开发体验。而 C++ 层面的变更到不大，基本可以兼容以前的代码。


> 考古: 曾经19年之前，本社团机器人运行环境为更古老的 Ubuntu14.04 下的 ROS Indigo，远古代码的备份已存放至github。[https://github.com/SIT-Robot/achieved2019](https://github.com/SIT-Robot/achieved2019)。后来，本人使用melodic环境重写了机器人的ros代码，经过数次迭代更新，最终迁移到noetic环境，代码即如今现有的代码。

## 推荐工具

推荐开发工具VSCode，安装ROS插件后即可愉快地开发。插件市场搜索相应插件，还可补全launch,urdf,xacro等ros下基于xml的描述配置的语言。

ROS的 C++ 功能包本质就是一个 cmake 工程，可以直接通过 CLion/VSCode 这样的支持 cmake 工程的 ide 打开，这在调试 c++ 功能包时是及其有用的。

ROS的 Python 功能包与一般的 Python 项目无异，可以直接通过 Pycharm/VSCode 打开，不过如果你电脑上安装有 Anaconda 一类的Python环境，一定要注意切换使用 System Python 即可索引到相关依赖，开启智能补全。

当然 Anaconda 这样的工具也是很有用的，但是不能直接在 conda 的虚拟环境中使用 ros 的功能包，需要单独配置。

尽量熟悉 Git工具的使用，使代码能够保留传承下去。
善于利用 Github 上一些诸如 Github Action(CI工具) 这样提高效率的工具。

推荐一些其他提高开发效率的工具
+ fish
+ zsh

## 学习资源推荐

### 文章资料

**[【奥特学园--赵虚左】《ROS理论与实践》零基础教程](http://www.autolabor.com.cn/book/ROSTutorials/)**


**【古月居】《ROS 机器人开发实践》**

这是一个实体书籍，大家可以去学校图书馆免费借阅到。

**[【古月居】ROS入门21讲 视频补充资料](https://www.bilibili.com/read/cv12059277)**

### 视频学习

**[【奥特学园--赵虚左】ROS机器人入门课程《ROS理论与实践》零基础教程（ROS基础与仿真环境下的导航实现）](https://www.bilibili.com/video/BV1Ci4y1L7ZZ)**

这个视频是本人在2021年初发现的关于ROS的视频学习资料，可以说是相当完美的学习资源。总共361集，可以说是相当详细的一部视频教程了。这个教程只要你肯花时间慢慢去学，一定能够学会ROS机器人开发入门。

**[【奥特学园--赵虚左】《ROS理论与实践》第8、9章--ROS机器人操作系统（实体机器人的软硬件开发与导航实现）](https://www.bilibili.com/video/BV1Ub4y1a7PH)**

这个视频是针对上一个361集视频资源的补充，原视频教程只包含了ROS的理论部分和仿真环境下的实践部分。本视频共91集，包含了上一个视频残缺的实体机器人的开发。其中涵盖了Arduino单片机开发，PID控制理论与实践，电机控制，串口协议开发，ROS实体机器人导航等知识点。

**[【古月居】ROS入门21讲](https://www.bilibili.com/video/BV1zt411G7Vn)**

这个视频是本人2020年底第一次学习机器人时看的第一个入门视频，当时在国内ROS的资料很少，尤其是视频教程。这个教程适合快速入门，快速了解上手机器人开发，但是讲的不够深入，不够细节，也不太适合零基础的小白。