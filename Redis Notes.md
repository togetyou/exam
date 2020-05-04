### redis总体架构
```
io模型
nio bio epoll
io的分阶段 1：状态 2：数据读写
6.x之前是单线程模式
6.x之后已经加入io thread 即 IO多线程

读 - 计算 - 写 这三个过程

redis存的是字节数组（二进制安全）hbase kafka的类似
```

### reids 五种value数据类型 与 使用场景
```
string list hash set sorted-set(zset)
```
#### string value类型
```
命令：help @string
String  实际存的是字节数组
  字符串操作： set get
  数值操作： incr decr
  二进制操作：setbit getbit bitop
应用场景：
  字符串：session共享 token 对象存储(序列成字节数组，可替换磁盘io)
  数值型操作： 秒杀，限流  
  二进制操作： 权限，某些情况的大数据统计 如：一个人一年的登录次数(设置一个265天的二进制数)
```



#### 待细化问题
```
数值型操作： 秒杀，限流
```  
