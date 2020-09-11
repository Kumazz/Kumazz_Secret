# 多态
>多类指的是 一类事物有多种形态，即 一个抽象类有多个子类，因而多态的概念依赖于**继承**

*  **定义:** 多态是一种使用对象的方式，子类重写父类方法，调用不同子类对象的相同父类方法，可以产生不同的执行结果

*  **优点:** 调用灵活，做出通用编程

*  **实现方法:**
  *  定义父类，并提供公共方法
  *  定义子类，并重写父类方法
  *  传递子类对象给调用者，可以看到不同子类执行效果不同
    

### 实例
* 子类可以调用父类的属性和方法，也可以调用子类的方法



```python
    class Dog(object):                     # 定义父类
        def work(self):                    # 提供公共方法
            print('该干啥干啥')


    class ArmyDog(Dog):                    # 定义子类 A
        def work(self):                    # 重写方法
            print('追击敌人')


    class DrugDog(Dog):                    # 定义子类 B
        def work(self):
            print('追查毒品')


    class Person(object):                  # 定义另一个类
        def work_with_dog(self, dog):      # 传递子类对象
            dog.work()


    ad = ArmyDog()
    dd = DrugDog()

    p = Person()
    p.work_with_dog(dd)
    p.work_with_dog(ad)
    ------------------------------------------
    >>> 追击敌人
    >>> 追查毒品


```





