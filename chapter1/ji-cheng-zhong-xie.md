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
*  查看类的层级继承关系，要查看的 **类名.\_\_mro__**





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
    print(C.__mro__)
    -----------------------------------------------------------
    >>> 1
    >>> 1 这是 A 类的 1
    >>> (<class '__main__.C'>, <class '__main__.A'>, <class '__main__.B'>, <class 'object'>)

```
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






