# 主要记录一下自己使用vultr过程中的各种问题

## 首先是选择server 系统的问题：

这里其实有两个选择，一个是ubuntu，用户比较多，另一个是centos，community用户并没有那么多，但是后来比较以后发现（我是直接安装了两个系统做了比较，之后发现ubuntu有些慢，不知道什么原因）centos可能会更加好一些。

## REMOTE HOST IDENTIFICATION HAS CHANGED! 错误

重装了系统以后发现这个错误总是会出现，其实这个很很好了解，因为重装了系统，新系统里面没有保存本地系统的ssh密钥。

解决方法也比较简单：

代码：
``` ssh-keygen -R <host> ```
*注意其中` <host> `这里需要改成你自己的服务器的ip地址。

```ssh-keygen -R 207.246.65.186 ```


安装好了cent os ，之后安装了面板出现了很多莫名其妙的问题，之后不得不放弃centos 重新开始按安装ubuntu