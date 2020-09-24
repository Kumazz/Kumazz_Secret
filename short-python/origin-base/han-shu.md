# 函数
### 作用
&emsp;&emsp;具有独立功能的代码块，封装代码，高效实现**代码重用**。通俗来说，可以理解为函数是一种做好的功能(方法)的代码，可以反复通用使用

### 定义和调用


```python
    def 函数名(参数):              # 用 def 定义
        代码1
        代码2
        ....
        
    函数名(参数)                   # 调用函数

```
&emsp;&emsp; 先用** def **定义再用** 函数名() **调用，函数名符合 Python 标识符命名规范；
&emsp;&emsp; 不同的需求，参数可有可无；
&emsp;&emsp; 调用函数时，解释器回到定义函数的地方执行下方缩进的代码，当这些代码执行完，回到调用函数的地方继续向下执行；



### 说明文档
&emsp;&emsp;函数的说明文档又叫函数的文档说明，解决代码多时无法用**注释**解释说明

*  **定义函数的说明文档**

```python
    def 函数名(参数):
        """说明文档的位置"""           # 必须在函数内第一行填写说明文档
        代码
        ......
```

*  **查看函数的说明文档**


```python
    help(函数名)
```

*  **说明文档的高级写法**


```python
    def sum_num(a, b):
    """                            # 双引号回车即可
    求和函数                        # 该函数说明
    :param a: 参数 1               # 冒号后写作用
    :param b: 参数 2
    :return: 返回值
    """
    return a + b

    help(sum_num)
    -----------------------------------
    >>> sum_num(a, b)
        求和函数
        :param a: 参数 1
        :param b: 参数 2
        :return: 返回值

```

### 嵌套函数



```python
    def testB():
        print('--testB start--')
        print('这里是 testB 函数执行的代码')
        print('-- testB end--')
        
    def testA():
        print('--testA start--')
        testB()
        print('--testA end--')
```








