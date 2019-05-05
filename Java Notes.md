### 集合框架

### 并发编程
    List
    CopyOnWriteList
    Queue (add offer poll peek) 
        add 和 offer的区别
        CocurrentLinkedQueue 
        BlokingQueue(put ,take)  put方法满了会阻塞
            LinkedBlockingQueue 无界队列
            ArrrayBlockingQueue 有界队列
        DelayQueue  无界队列  （应用场景 delay获取）
        TransferQueue  提供t一个transfer方法
        
#### 线程池
    Callable 有返回值，并且抛出异常
    Runnable 没有返回值 且不能抛出异常
    Excutor
    ExcutorService
    6种线程池
    ThreadPoolExcutor
    
### 问题
    Thread.sleep TimeUnits.Sesconds.sleep 区别？
    各种线程池相关的队列 ？
    各种队列的使用
    parallelStream?
    