# 详解对象
### 类方法
&emsp;&emsp;类中定义的函数，作为对象的行为或功能
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
             print(f'再吃{food}')
     
     dog = Animal()
     dog.eat('旺旺雪饼')                      # 传递实参
     -----------------------------------------------------
     >>> 旺旺雪饼
 ```

### 详解 self
&emsp;&emsp;self 指的是**调用该函数的对象**


```python
    class Animal(object):
        def eat(self, food):
            print(f'测试{food}')
            
    Animal.eat(dog, '提拉米苏')                  # 通过 类名.方法(实例对象, 实参) 调用方法
    ------------------------------------------------------
    >>> 提拉米苏

```





