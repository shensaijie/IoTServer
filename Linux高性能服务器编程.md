# linux服务器程序规范

日志

用户系统

服务器后台运行

# **高性能服务器程序框架**

## 服务器模型

C/S模型（客户端/服务端）

p2p模型

## 服务器编程框架
- I/O处理单元
- 逻辑单元
- 存储单元

## i/o模型


## 高效的事件处理模式

- Reactor模式
    主线程只负责监听文件描述符上事件，工作线程处理
- Proactor模式
    所有的I/O交给主线程和内核来处理，工作线程负责业务逻辑

## 高效的并发模式
“同步”：程序完全按代码顺序执行

“异步”：程序的执行需要系统事件的驱动（中断，信号等）

- 半同步/半异步（half-sync/half-async)模式
    同步线程处理客户逻辑，异步线程处理I/O
- 领导者/追随者（Leader/Followers)模式
    多个工作线程轮流获得事件源集合，任意时刻一个领导者负责监听I/O
## 有限状态机

## 其他提高性能建议
- 池（poor)内存池、进程池、线程池、连接池
    以空间换事件，预先申请资源
- 避免不必要的数据复制
- 上下文切换和锁（进程和线程切换占用CPU时间）
