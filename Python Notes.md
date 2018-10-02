### python 基础
#### IDE
      IDLE,Pycharm,wingide,eclipse
#### 注释
    单行注释 #xxxx

    多行注释
    '''
        多行注释
    '''
#### 行连接符
     使用\作为行链接符号
     a="sdfksdkjfhskd\
     dfs"
     print(a)

#### pyhton对象
     id 标识, type 类型, value 值
     a = 3;
     id(a)
     type(a)

#### 引用
     变量称之为对象的引用
     变量在栈里面
     对象在堆里面
#### 标识符
    与java 类似
    区分大小写 字母或者_开头后续字母数字下划线  避免关键字  避免双下划线（系统使用）
#### 变量赋值
    简单赋值
    a=3
    链式赋值
    a=b=3
    解包赋值
    a,b,c=1,2,3
    利用解包赋值可以进行变量值交换(不需要定义中间变量)
    如:
    a,b=1,2
    a,b=b,a
#### 常量
    python本身不支持常量
    只能通过命名来规范定义：
    用大写加下划线MAX_VALUE=100
#### 运算符
    + - *
    / 浮点数除
    // 整数除
    ** 幂运算
    divmod(x,y)   #返回商和余数
    逻辑运算符 and or not 
    等值判断 == is ，注意==会判断实际的value值 is判断是否是同一个对象的地址
#### 整数
    *进制
    0B 开头二进制
    0o 开头八进制
    0x 开头16进制
    如：0o9是错误的 八进制应该表示为0o11
    *进制转换
    int(5.4)
    python3整数大小无限制
    python2整数位32位
    
    0xff = 15*16^1 + 16 = 255
#### 浮点数
    float  浮点数类型
    float(2) 2.0
    float("2.1") 2.1
    科学计数法
    3.14 可表示为 314E-2或者314e-2
    round(3.5) 4 四舍五入取整
#### 时间
    time ,datetime,timedelta
    time.time() 返回1970-1-1到至今的秒数
    格式化时间time.strftime()
    ```
    strftime(...)
        strftime(format[, tuple]) -> string
    ```
    字符串转化为时间 time.strptime()
    ```
      strptime(...)
        strptime(string, format) -> struct_time
    ```
    时间计算 timedelta
    
