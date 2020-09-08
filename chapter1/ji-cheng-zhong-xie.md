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

*  如果子类与父类有同样方法则会被**重写**


```python
    class Animal(object):
        def __init__(self, name):
            self.name = name

        def eat(self):
            print(f'{self.name}正在吃东西')

        def play(self):
            print(f'{self.name}正在玩耍')

        def sleep(self):
            print(f'{self.name}正在睡觉')


    class Dog(Animal):                              # 继承父类Animal
        def bark(self):                             # 直接调用父类的__init__() 方法
            print(f'小狗 {self.name} 旺旺叫')
        
        def eat(self):                             # 与父类拥有同样方法
            print(f'{self.name}正在吃狗粮')


    class Cat(Animal):
        def miao(self):
            print(f'小猫喵喵叫')


    dog = Dog('tom')
    print(dog.name)                               # 子类调用父类属性
    dog.play()                                    # 子类调用父类方法
    dog.eat()                                     # 子类与父类有同样方法
    dog.spark()                                   # 子类可以使用自己的方法
    --------------------------------------------------------------
    >>> tom                                       # 子类会调用父类 init 方法
    >>> tom 正在玩耍
    >>> tom 在吃东西
    >>> tom 正在吃狗粮                              # 子类会优先使用自己的方法
    >>> 小狗 tom 旺旺叫


```

*  如果子类也有 init 方法且也想调用父类 init 方法


### 单继承


```python
    

```






