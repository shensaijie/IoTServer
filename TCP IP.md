# socket
## TCP套接字编程
socket -> bind -> listen -> accept -> read/write

# TCP IP网络编程

# DNS域名

域名一般不换，IP地址可能会常换

`hostent`结构体存储域名IP信息

[gethostbyname()](TCPIP/gethostbyname.c), gethostbyaddr()

# 套接字可选项和I/O缓冲大小

getsockopt & setsockopt 设置和查看套接字设置

## I/O缓冲

SO_SNDBUF & SO_RCVBUF

输入缓冲大小 & 输出缓冲大小

## SO_REUSERADDR
    设置为1，允许重分配Time-wai端口
四次握手过程中先断开链接的主机会经过 #Time-wait 状态，此时端口号会占用，而服务端端口固定的，因此不能立即重启。

Nagle算法 & TCP_NODELAY
1时禁用
