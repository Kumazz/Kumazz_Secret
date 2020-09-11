# 私有权限

&emsp;&emsp;Python 中可以为实例属性和方法设置私有权限，即设置某个实例属性或实例方法不继承给子类




### 私有属性和方法
* 设置: 在 属性名 和 方法名 前面加上两个下划线 \_\_


```python
    class A(object):
        def __init__(self):
            self.num = 1
            self.__money = 10000000                   # 设置了私有属性
        def __info_print(self):
            print(f'这是私有方法')

    class B(A):
        pass

    b = B()
    print(b.num)
    print(b.money)
    -------------------------------------------
    >>> 1
    >>> 报错，AttributeError: 'B' object has no attribute 'money'
    >>> 报错，AttributeError: 'B' object has no attribute 'info_print'

```

* 获取: 在 属性名 和 方法名 前面加上两个下划线 \_\_



```python
    

```










