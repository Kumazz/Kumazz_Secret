# 参数
### 作用
*  **参数**，函数参数的作用是传递数据给函数使用
  *  **形参**，形式上的参数，可以理解为数学的X，没有实际的值，通过别人赋值后才有意义。
  * **实参**，实际意义上的参数，是一个实际存在的参数，可以是字符串或是数字等，调用函数时用到的参数
  * **位置参数**，位置参数就是按照形参中给定的参数的顺序
  * **关键字参数**，在传递参数的时候，可以按照形参的名字给定参数
  * **默认参数**，函数定义时，为参数设置一个默认值，当函数调用时，没有传入这个参数值，直接使用这个默认值
  * **可变参数**，可变参数有两种形式：一种是 \*args,另一种是 \**kwargs

&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;\*args：这种形式表示接受任意多个实际参数将其放到一个元组中。

&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;\**kwargs：这种形式表示接受任意多个实际参数将其放到一个字典中，类似关键字参数

### 案例

* **形参与实参**  
&emsp;&emsp;形参相当于变量，定义函数时指定的参数； 实参是在调用函数时传递进去的参数，一般传递真实数据


```python
    def add_sum(a, b):          #  a 和 b (占位)参数，叫 形参
        result = a + b
        print(result)
        
    add_sum(1, 2)               # 调用函数式传入真实的数据如 1，2 ，叫做 实参

```

* **位置参数**
&emsp;&emsp;调用函数时根据函数定义的参数位置来传递参数，**传递和定义参数的顺序及个数必须一致**


```python
    def user_info(name, age, gender):
        print(f'他的名字叫{name}，今年{age}岁了，性别是{gender}')

    user_info('tom',18,'man')
    ------------------------------------------------------
    >>> 他的名字叫tom，今年18岁了，性别是man

```


* **关键字参数**
&emsp;&emsp;通过 **'键=值'** 形式传递，函数调用时，**如果有位置参数，关键字参数在位置参数后面，关键字参数之间不存在先后顺序**


```python
    def user_info(name, age, gender):
        print(f'他的名字叫{name}，今年{age}岁了，性别是{gender}')

    user_info('jerry', gender='男', age=17)           # 不报错，关键字参数之间不存在先后顺序

```


* **默认参数**
&emsp;&emsp;也叫**缺省参数**，**默认参数在位置参数后，包括函数定义和调用**



```python
    def user_info(name, age, gender='男'):
        print(f'他的名字叫{name}，今年{age}岁了，性别是{gender}')

    user_info('jerry', age=17)                              # 不传值则使用默认值

    user_info('tom', 17, gender='女')                       # 缺省参数传值则修改默认参数值

```


* **不定长参数**
&emsp;&emsp;也叫 **可变参数**，用于不确定调用的时候传递多少个参数(不传参也可以)的场景，可用包裹位置参数、关键字参数来进行参数传递
  * ** \*args**，包裹位置传递，args 相当于变量名，**返回的是元组**
  
  ```python
    def user_info(*args):             # 传递的所有参数都会被 args 变量收集
        print(args)                       

    user_info('tom')                  >>> ('tom',)
    user_info('t0m',18)               >>> ('t0m',18)

  ```

  *  **\*\*kwargs**，包裹关键字传递，kwargs 相当于变量名，**返回的是字典**，组包过程

  ```python
    def user_info(**kwargs):         # 传递的所有关键字参数都会被 kwargs 变量收集
        print(kwargs)                     

    user_info(age=18, gender='男')     >>> {'age': 18, 'gender': '男'}
  ```













