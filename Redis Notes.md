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

```
