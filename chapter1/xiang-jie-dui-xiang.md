# 详解对象
### 方法
&emsp;&emsp;**类方法**，类中定义的函数，作为对象的行为或功能
*  语法


```python
    def 方法名(self, args):                 # 用 def 定义，self 是实例对象， args 是参数
        pass

```
> 类方法名与函数写法、命名规则一样，全小写或用蛇形写法，但类方法与一般函数定义不同，类方法**必须包含参数 self, 且为第一个参数**，self 代表的是类的实例

*  案例

  *  不传参数

 ```python
    class Animal(object):
        def play(self):                       # 定义该类的方法
            print('旺旺')
    
    dog = Animal()                            # 生成一个实例
    dog.play()                                # 通过 实例名.类方法() 进行方法调用

 ```

 *  传递参数
 
 ```python
     class Animal(object):
         def eat(self, food):                # 设置形参
             print(f'在吃{food}')
     
     dog = Animal()
     dog.eat('旺旺雪饼')                      # 传递实参，通过 实例名.方法() 进行调用
     -----------------------------------------------------
     >>> 在吃旺旺雪饼
 ```

### 详解 self
&emsp;&emsp;self 指的是**实例对象**


```python
    class Animal(object):
        def eat(self, food):                    # 所有 self 指的是 dog 这个实例 
            self.play('打球')                    
            print(f'测试{food}')
            
    Animal.eat(dog, '提拉米苏')                  # 可以通过 类名.方法(实例对象, 实参) 调用方法
    -----------------------------------------------------------------------------------
    >>> 打球
    >>> 测试提拉米苏



```

### 属性
* 实例属性


```python
    class Animal(object):
    def __init__(self, name, age):
        self.name = name                              # self.name 就是实例的属性
        self.age = age


    dog = Animal("tom", 20)
    print(dog.name)                                   # 通过 实例名.属性名 获取属性值

```


    
* 类属性





