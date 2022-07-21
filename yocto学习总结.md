# yocto

## 什么是Yocto Project	

​	有各种各样的distribution和build系统可以用来开发嵌入式Linux系统。许多桌面distributions能够做到比较精简以便在有限的资源环境和系统中使用，比如Ubuntu就有专门针对物联网设备的品类（specifically targeted at IoT devices）。 Raspberry Pi平台使用定制的Debian镜像作为其主要目标OS镜像。另外，有一些交叉编译全Linux系统的方法，最主要的有Yocto，OpenWRTl和Buildroot。这些系统通常托管在（hosted on）一个标准桌面Linux发行版并能够为选定的目标设备交叉构建（cross-build）一个Linux操作系统。

​	Yocto Project是一个能够帮助开发者创造基于Linux定做的系统的开源协作项目，定做的系统被设计用于嵌入式产品，且不受产品硬件架构的约束。Yocto Project提供了灵活的工具集和一个开发环境，该环境允许嵌入式设备开发者能够在世界任何位置通过共享技术，软件栈，配置和过去被用来创造这些定制化Linux images的一些最佳实践来进行协同工作。我的一句话总结就是给IoT（Internet of Things）项目开发用的东西。

​	以上官方的定义过于简便，说的类似于桌面linux distributions。其实Yocto更像是一个meta-distribution（http://wiki.c2.com/?MetaDistribution），一种旨在建立Linux发行版的软件系统；一个相当于一种适应性系统的项目，该项目能够根据用户规范build它本身。它是集方法，配置值和独立性于一身的东西，被用来创造根据你的特定需求自定义的Linux运行环境镜像。

## 面向IoT的嵌入式Linux设计

嵌入式和IoT里的项目用到了很广泛的芯片架构和开发板。Linux内核已经被移植到（ported to ）商用的大部分里，并在将来极有可能支持自选的芯片集（chipset）。大多数半导体厂商为了支持他们自己的产品而直接去开发内核代码和驱动，使客户在设计的时候更能适应Linux。 并非所有厂商的产品在stock kernels（from http://kernel.org/）里都适用，所以需要自己做研究、综合工作将选定的平台所必需的软件组件集合起来。

​	stock kernel:Linus本人说这是基本内核版本(base kernel release)。大多数发行版会使用stock kernel作为基本（base），并在这个kernel的最顶端添加这些发行版自己的patches和drivers（比如ndiswrapper,supermount等）。最终所有这些厂商提供的patches中的一部分会趋近于base kernel，但也有一些patches由于许可冲突不会达到base kernel（比如nvidia的驱动）。——LinuxQeustions.org

​	JTAG支持是嵌入式Linux中使用的方法并且在low-level的内核调试中广泛使用。它取决于半导体厂商以及JTAG器件制作者的支持。用诸如GDB这种的广泛可用且移植性好的工具可以更好的调试应用程序和用户态代码（user-space code）。

* 嵌入式软件开发和普通桌面软件开发的区别：

  嵌入式开发在宿主机上编辑、编译程序，在目标机运行测试程序，称为交叉开发；普通桌面软件开发在本机开发和调试；嵌入式开发需要根据目标机选择合适编辑器，嵌入式程序的调试需要专用软硬件的支持；嵌入式软件对体积、成本、可靠性方面都有较高要求。

  **q:**系统软件和应用软件的开发都算桌面软件开发么？
  
  **a:**

* 嵌入式Linux和普通嵌入式开发的区别：

  开发人员和嵌入式目标开发板的连接通常是通过串行端口和以太网，幸运的是嵌入式Linux对这些设备有广泛支持，并且不会对设计团队造成任何困难。Windows和MacOS主机系统中的驱动支持可能会出现问题，因为设备驱动可能不包括在默认的OS中并且可能需要安装第三方驱动程序。

### 和Linux的比较

​	Linux适用于更关注数据处理和网络连接的系统，但是在关注点在于使用简单控制逻辑的基础电子机械系统里，Linux的设计可能会过于夸张，此时使用一个实时操作系统（RTOS）或者控制循环可能会更合适。

### 交叉工具链

​	建立一个交叉编译环境很棘手，选择合适的工具链和库的组合是一个比较麻烦的事情，cross-ng(https://crosstool-ng.github.io/)是一个build system，可供选择。它是一个交叉工具链生成器，支持很多架构和组件并且界面简洁功能强大。

## 参考资料

https://docs.yoctoproject.org/

https://www.embedded.com/why-the-yocto-project-for-my-iot-project/	








