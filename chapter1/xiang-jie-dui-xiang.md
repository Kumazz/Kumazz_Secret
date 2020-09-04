# 详解对象
### 类方法
&emsp;&emsp;类中定义的函数，作为对象的行为或功能
*  语法


```python
    def 方法名(self, args):                 # 与函数写法、命名规则一样，全小写或用蛇形写法
        pass

```
> 类方法与一般函数定义不同，类方法**必须包含参数 self, 且为第一个参数**，self 代表的是类的实例

*  案例



```python
    class Animal(object):
        def play(self):                       # 定义该类的方法
            print('旺旺')
    
    dog = Animal()                            # 生成一个实例
    dog.play()                                # 通过 实例名.类方法() 进行方法调用

```






