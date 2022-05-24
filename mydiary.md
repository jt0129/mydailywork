ssh:Secure Shell（安全外壳协定，简称**SSH**）是一种加密的[网路传输协定](https://zh.wikipedia.org/wiki/网络传输协议)，可在不安全的网路中为网路服务提供安全的传输环境[[1\]](https://zh.wikipedia.org/zh-tw/Secure_Shell#cite_note-rfc4251-1)。SSH通过在网路中建立[安全隧道](https://zh.wikipedia.org/w/index.php?title=安全隧道&action=edit&redlink=1)来实现SSH客户端与伺服器之间的连接[[2\]](https://zh.wikipedia.org/zh-tw/Secure_Shell#cite_note-rfc4252-2)。SSH最常见的用途是远端登入系统，人们通常利用SSH来传输[命令列介面](https://zh.wikipedia.org/wiki/命令行界面)和远端执行命令。SSH使用频率最高的场合是[类Unix系统](https://zh.wikipedia.org/wiki/类Unix系统)，但是[Windows](https://zh.wikipedia.org/wiki/Windows)作业系统也能有限度地使用SSH。2015年，微软宣布将在未来的作业系统中提供原生SSH协定支援[[3\]](https://zh.wikipedia.org/zh-tw/Secure_Shell#cite_note-3)，[Windows](https://zh.wikipedia.org/wiki/Windows) 10 1803版本已提供[OpenSSH](https://zh.wikipedia.org/wiki/OpenSSH)工具[[4\]](https://zh.wikipedia.org/zh-tw/Secure_Shell#cite_note-4)。



# 5月20日

## 尝试github SSH连接

## 读论文，[《PRIME+SCOPE》](https://dl.acm.org/doi/pdf/10.1145/3460120.3484816?casa_token=vnnM3Sf82MYAAAAA:F0ZF4Ts2mWTFRtdAoz2UxjH9nAo0RiI2_idRt1BP569L9nA5pdDr_3shhc_UEFHzqliJ-qZ4QQ)。

# 5月21日

## 读论文，[《PRIME+SCOPE》](https://dl.acm.org/doi/pdf/10.1145/3460120.3484816?casa_token=vnnM3Sf82MYAAAAA:F0ZF4Ts2mWTFRtdAoz2UxjH9nAo0RiI2_idRt1BP569L9nA5pdDr_3shhc_UEFHzqliJ-qZ4QQ)。

* abstract完事了，该introduction了。

## github SSH连接成功

* 出错原因：公钥建的太乱，github上new key后匹配本地的SSH名称时混乱，可能开始的时候执行这条命令**忘记改参数**了。

  ```shell
  ssh-keygen -t ed25519 -C "your_email@example.com"
  ```

* 心得：不要着急，也就是花了两天半的时间嘛，两天半玩也就玩过去了不会有任何痛苦，这是在弄正事为什么要瞎着急呢，做就是了


# 5月23日

## 《PRIME+SCOPE》个人部分PPT完成

* **第一篇精读论文**
* 精读了ABSTRACT和INTRODUCTION部分，开始时只看英文原版+查词翻译感觉十分晦涩难懂。无奈只好结合Google机翻对照着看。半天时间硬看一点摘要后对名词有感觉了，又用了两天时间差不多能囫囵点意思出来就把PPT写了。

# 5月24日

## 提交《智能计算系统》剩余实验

* 尽管是直接用的现成的,但提交检测还是有点问题。提交文件压缩包测试时显示找不到文件。原因是压缩了两次，解开一层压缩就好了

## 跟鹏哥复习《云计算》课程

* 两个小时学习了：

  * 特权指令、临界指令、敏感指令
  * 用户视角下不同级别的虚拟化
    * 指令级
    * 硬件级
    * 操作系统级
    * 编程语言级
    * 程序级

  * CPU虚拟化
    * 全虚拟机化
    * 半虚拟化

  * root、non-root

## 听《体系结构安全》论文汇报

* 我的3页PPT被主讲人引用了一行

  