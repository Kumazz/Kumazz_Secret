### 魔法方法
 &emsp;&emsp;在 Python 中，\_\_xx__() 的函数叫做魔法方法，指的是具有特殊功能的函数。注意点是**前后是两个下划线**
 
#### \_\_init__()，初始化方法
  
* 案例
 * \_\_init__() 方法，在创建实例对象时默认被调用，不需要手动调用
 
 ```python
    class Animal(object):
        def __init__(self):
            print('我是狗崽子')
        def eat(self, food):
            print(f'正在吃{food}')
            
    dog = Animal()
    dog.eat('奶昔')
    --------------------------------------------------------------------------
    >>> 我是狗崽子                        # 创建实力对象时就自动调用了 init 方法
    >>> 正在吃奶昔                        # 普通类方法则需要通过 对象名.方法() 来进行调用类方法
 ```
 
 * \_\_init__() 方法主要用于初始化参数，解决不同类或实例调用参数
 
 ```python
    class Animal(object):
       def __init__(self, name, age):                # 初始化实例的参数 
             self.name = name                        # 将参数赋值给实例化对应的属性
             self.age = age
             
       def play(self,food):
             print(f'{self.name}正在吃{food}')
    
    dog = Animal()
    dog.play('tom', 20, '碎碎冰')
 ```

  