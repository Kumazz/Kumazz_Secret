# 继承
>多个类之间的所属关系，即子类默认继承父类的所有属性和方法

### 单继承
* 子类可以调用父类的属性和方法，也可以调用子类的方法



```python
    class A(object):                        # 定义一个类 A 作为 父类
        def __init__(self):                 # 定义父类属性
            self.num = 1
        
        def info_prit(self):                # 定义父类方法
            print(self.num)


    class B(A):                             # 定义一个类 B，继承 A 形成子类
        pass
    
    result = B()                            # 生成子类实例
    print(result.num)                       # 调用父类的属性
    result.info_print()                     # 调用父类方法
    ---------------------------------------------------------
    >>> 1
    >>> 1
```



### 多继承

* 当一个类有多个父类的时候，默认使用**第一个父类**的**同名**属性和方法
* 查看类的层级继承关系，语法: 要查看的 **类名.\_\_mro__**
* 只要存在继承关系，可以多层继承


```python
    class A(object):
        def __init__(self):
            self.num = 1

        def info_print(self):
            print(f'{self.num} 这是 A 类的 1')


    class B(object):
        def __init__(self):
            self.num = 1

        def info_print(self):
            print(f'{self.num} 这是 B 类的 1')
            

    class C(A, B):                                 # 同时继承两个类，想用哪个类属性方法写在第一个参数位置
        pass

    resuly = C()
    print(resuly.num)
    resuly.info_print()
    
    print(C.__mro__)                                # 查看继承关系
    -----------------------------------------------------------
    >>> 1
    >>> 1 这是 A 类的 1
    >>> (<class '__main__.C'>, <class '__main__.A'>, <class '__main__.B'>, <class 'object'>)

```


### 重写
*  如果子类与父类有同名方法和属性则会被子类**重写**


```python
  
    class A(object):
        def __init__(self):
            self.num = 1

        def info_print(self):
            print(f'这是类 A 的 {self.num}')


    class B(object):
        def __init__(self):
            self.num = 1

        def info_print(self):
            print(f'这是类 B 的 {self.num}')


    class C(A, B):
        def __init__(self):                         # 定义与父类同名的属性
            self.num = 2

        def info_print(self):                       # 定于与父类同名的方法
            print(f'这是类 C 的{self.num}')


    result = C()
    result.info_print()
    -------------------------------------------------------------
    >>> 这是类 C 的 2                             # 重写了父类的属性和方法


```

### 不重写
&emsp;&emsp;子类既能使用自身的方法属性，同时也能使用父类同名的属性和方法

*  调用单个父类

```python
    class A(object):
        def __init__(self):
            self.num = 1

        def info_print(self):
            print(f'这是类 A 的 {self.num}')


    class B(A):
        def __init__(self):
            self.num = 2

        def info_print(self):
            print(f'这是类 B 的 {self.num}')

        def A_info_print(self):                         # 把要调用父类同名属性和方法再次封装，即可实现子类调用父类
            A.__init__(self)                            # 需再次调用init方法进行初始化属性
            A.info_print(self)                          # 封装函数注意传递 self 参数

    result = B()
    result.info_print()
    result.A_info_print()
    --------------------------------------------------------
    >>> 这是类 B 的 2
    >>> 这是类 A 的 1

```

*  一次性(全部)调用父类，复杂方法



```python
    class A(object):
        def __init__(self):
            self.num = 1

        def info_print(self):
            print(f'这是类 A 的 {self.num}')


    class B(object):
        def __init__(self):
            self.num = 1

        def info_print(self):
            print(f'这是类 B 的 {self.num}')


    class C(A, B):
        def __init__(self):
            self.num = 1

        def info_print(self):
            print(f'这是类 C 的 {self.num}')

    # 方法一: 代码冗余，父类类名如果有变化，代码需要频繁修改
        def all_info_print(self):
            A.__init__(self)
            A.info_print(self)
            B.__init__(self)
            B.info_print(self)


    resy = C()
    resy.info_print()
    resy.all_info_print()
```

*  一次性调用父类，super() 带参数写法，super(当前类名, self).函数()，因为类名不可控不推荐该写法


```python
    class A(object):
        def __init__(self):
            self.num = 1

        def info_print(self):
            print(f'这是类 A 的 {self.num}')


    class B(A):                                           # 继承 A 为父类
        def __init__(self):
            self.num = 1

        def info_print(self):
            print(f'这是类 B 的 {self.num}')

            super(B, self).__init__()                    # 调用 A 父类
            super(B, self).info_print()


    class C(B):                                          # 继承 B 为父类
        def __init__(self):
            self.num = 1

        def info_print(self):
            print(f'这是类 C 的 {self.num}')

        def all_ab_info(self):
            super(C, self).__init__()
            super(C, self).info_print()



    reay = C()
    reay.all_ab_info()                                 # 调用时会同时输出 A, B 类方法
    ------------------------------------------------------------
    >>> 这是类 B 的 1
    >>> 这是类 A 的 1


```

*  一次性调用父类，super() 无参数写法，super().函数()，因为super()能自动查找父类



```python
    class A(object):
        def __init__(self):
            self.num = 1

        def info_print(self):
            print(f'这是类 A 的 {self.num}')


    class B(A):
        def __init__(self):
            self.num = 1

        def info_print(self):
            print(f'这是类 B 的 {self.num}')

            super().__init__()
            super().info_print()


    class C(B):
        def __init__(self):
            self.num = 1

        def info_print(self):
            print(f'这是类 C 的 {self.num}')

        def all_ab_info(self):
            super().__init__()
            super().info_print()


    reay = C()
    reay.all_ab_info()
    --------------------------------------------------------------
    >>> 这是类 B 的 1
    >>> 这是类 A 的 1

```
















