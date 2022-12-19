- [redis 为什么那么快？](#redis-为什么那么快)
  - [基本结构](#基本结构)
  - [分布式锁](#分布式锁)

# redis 为什么那么快？

Redis 是一个开源的内存数据存储系统，它的速度之快的原因有几个方面：

Redis 使用内存存储数据，因此读写数据的速度比磁盘快得多。

Redis 使用单线程架构，避免了多线程之间的竞争，提升了性能。

Redis 使用非阻塞 I/O 多路复用机制，可以同时处理多个客户端请求，提升了并发能力。

Redis 使用散列表和[跳跃表](https://www.baidu.com/link?url=q3MUHWviwZ-t_vMR3iY5y0uSf4eeCNKGLb0eHW1Mk7NNSmjdnI5a1d7g_mS2013a2UffcjEDGBBuqhRT9v8CeyJbMmcMJ8x5nqFhpyuqrRO&wd=&eqid=a2c86ab50000244b00000006639fcdc9)实现的数据结构，使得查找和插入数据的复杂度较低。

总之，Redis 的设计和实现使其在读写数据方面表现出色，这是其速度之快的原因。


## 基本结构
## 分布式锁