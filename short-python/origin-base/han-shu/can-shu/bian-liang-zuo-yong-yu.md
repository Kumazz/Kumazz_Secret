# 变量作用域
### 定义
&emsp;&emsp;变量作用域指的是**变量生效的范围**，主要分为两类: **局部变量**和**全局变量**


### 局部变量
&emsp;&emsp;定义在**函数体内部的变量**，即只在**函数体内部生效**

```python
    def testA():
        a = 100                 # 函数体内部定义的变量
        print(a)
    testA()                      >>> 100
    print(a)                     >>> name 'a' is not defined
        

```

> 局部变量作用: 在函数体内部，临时保存数据，即当函数调用完成后，则销毁局部变量


### 全局变量
&emsp;&emsp;在**函数体内、外部生效**的变量，起到一个共用的作用


```python
    a = 150                        # 函数体外部定义的变量         

    def testA():
        print(a)
    
    def testB():
        print(a)
    
    testA()                       >>> 150
    testB()                       >>> 150

```


### 全局变量与局部变量存在
&emsp;&emsp;如果同时存在，局部变量不会受全局变量影响


```python
    a = 100

    def testA():
        print(a)
    
    def testB():
        a = 20
        print(a)
    
    testA()                      >>> 100
    testB()                      >>> 20
    print(a)                     >>> 100

```


### 局部变量转全局变量 - global
&emsp;&emsp;必须要先用 global **声明一下变量**


```python
    a = 100

    def testA():
        print(a)
        
    def testB():
        global a            # 先用 global 声明变量  
        a = 20
        print(a)
        
    testA()                  >>> 100          # 根据程序运行顺序，这一步不受影响   
    testB()                  >>> 20
    print(a)                 >>> 20

```


### 多函数的执行顺序


```python
    a = 0
    
    def testA():
        global a
        a = 100
        
    def testB():
        print(a)
        
    print(a)                >>> 0          # 打印全局变量，因为后面程序未执行
    testA()                                # 修改局部变量为全局变量，并为变量重新赋值
    testB()                 >>> 100        # 执行修改后的代码

```

> Python 程序是从上至下逐步执行







