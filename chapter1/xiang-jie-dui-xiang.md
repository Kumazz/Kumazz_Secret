# 详解对象

### self
&emsp;&emsp;self 指的是**实例对象**


```python
    class Animal(object):
        def eat(self, food):                    # 所有 self 指的是 dog 这个实例 
            self.play('打球')                    
            print(f'测试{food}')
            
    dog = Animal()
            
    Animal.eat(dog, '提拉米苏')                  # 也可以通过 类名.方法(实例对象, 实参) 调用方法
    -----------------------------------------------------------------------------------
    >>> 打球
    >>> 测试提拉米苏



```

### 属性
&emsp;&emsp;属性即特征，比如: 实例对象的宽度、高度、重量等
&emsp;&emsp;属性分为 实例属性 和 类属性
&emsp;&emsp;属性既可以在类外面添加和获取，也能在类里面添加和获取

* **实例属性**


```python
    # 类外通过 实例名.属性名 = 值 添加实例属性
    --------------------------------------------------------------
    class Animal(object):
        def play(self):
            print('打球')                   
            
    dog = Animal()
    dog.name = 'tom'                     # 类外添加属性 
    
    --------------------------------------------------------------
    print(dog.name)                      # 通过 实例名.属性名 获取属性 

```


```python
    # 类内通过 self.属性名 添加实例属性
    --------------------------------------------------------------
    class Animal(object):
        def paly(self):
            print(f'这条狗名字叫{self.name}')              # 在类内部通过 self.属性名 添加实例属性
    
    dog = Animal()
    dog.name = 'jerry'
    dog.paly()                                           # 通过实例调用方法获取属性
    -------------------------------------------------------------
    >>> 这条狗叫 jerry
    
```

> 由于在类外添加属性或者在类内部添加属性在代码上造成混乱和冗余，灵活性不高，一般通过初始化方法 **\_\_init__()** 进行属性设置



```python
    # 类属性可以任何实例进行调用，如果该实例有自己的属性则会使用实例属性
    ---------------------------------------------------------------------
    class Animal(object):
        def __init__(self, name, age):
            self.name = name                 # 实例属性，参数有 self 用于指代实例对象
            self.age = age
            
    dog = Animal('tom', 20)                  # 通过实例化时传递参数设置属性
    print(dog.name)                  

```

   
* **类属性( 类变量 )**，就是 类对象 所拥有的属性，它被 该类的所有实力对象 所共有，类属性可以使用 类对象 或 实例对象 访问

    ```python
       class Animal(object):
           age = 5 # 类属性
            
       dog = Animal()
       print(Animal.age)                 # 通过 类名.属性名 访问
       dog.age                           # 通过 实例名.类变量 访问
       ------------------------------------------------------
       >>> 5
       >>> 5
    ```
    
  * 修改类属性
  
  ```python
     class Animal(object):
        age = 5

     dog = Animal()
     cat = Animal()

     Aninmal.age = 10                         # 通过 类对象 修改 类属性

     print(Animal.age)
     print(dog.age)                       
     print(cat.age)
     ----------------------------------------------------------
     >>> 10
     >>> 10
     >>> 10
  ```

> 类属性只能通过 类对象 修改，如果通过实例对象修改其实是创建一个实例属性并非修改类属性

### 方法
&emsp;&emsp;**类方法**，类中定义的函数，作为对象的行为或功能
*  语法


```python
    def 方法名(self, args):                 # 用 def 定义，self 是实例对象， args 是参数
        pass

```
> 类方法名与函数写法、命名规则一样，全小写或用蛇形写法，但类方法与一般函数定义不同，类方法**必须包含参数 self, 且为第一个参数**，self 代表的是类的实例

*  案例

  *  不传参数的方法

 ```python
    class Animal(object):
        def play(self):                       # 定义该类的方法
            print('旺旺')
    
    dog = Animal()                            # 生成一个实例
    dog.play()                                # 通过 实例名.类方法() 进行方法调用

 ```

 *  传递参数的方法
 
 ```python
     class Animal(object):
         def eat(self, food):                # 设置形参
             print(f'在吃{food}')
     
     dog = Animal()
     dog.eat('旺旺雪饼')                      # 传递实参，通过 实例名.方法() 进行调用
     -----------------------------------------------------
     >>> 在吃旺旺雪饼
 ```




