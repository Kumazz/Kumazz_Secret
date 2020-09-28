# 其它函数
### 递归函数
&emsp;&emsp;一个函数在内部调用自己本身
* **特性**
  * 必须是函数内部自己调用自己
  * 必须有一个明确的递归结束条件，即为递归出口


* **应用场景**
  * 快速排序
  * 遍历文件夹下面文件
  * 阶乘
  
```python
    def sum_nums(num):
        if num == 1:
          return 1
        return num + sum_nums(num-1)

    result = sum_nums(3)
    print(result)
```

![](/assets/QQ20200928-133117@2x.png)


### 匿名函数
&emsp;&emsp;**变量名 = lambda [参数1,参数2..] ：逻辑表达式**
*  在定义函数的时候，不想给函数起一个名字，或者一个函数有一个返回值并且只有一句代码，这个时候就可以用 lambda 来定义一个匿名函数
  *  参数：可有可无，通常以逗号分隔的变量表达式形式，也就是位置参数
  *  表达式：不能包含循环、return，可以包含 if...else...

```python
    result = lambda x, y : x + y
    print(result)                           # 返回的是函数地址
    print(result(1, 2))                     # 调用时是 变量名()
        

```



```python
    # 默认参数
    result = lambda a, b, c=100 : a + b + c
    print(result(10, 20))

```



```python
    # 可变参数
    fn = lambda *args : args
    print(fn(1, 2, 3))                     # 返回元组
    
    fn1 = lambda **kwargs : kwargs
    print(fn1(name='tom', age=12))         # 返回字典
  
```



```python
    # 带判断的 lambda
    fn = lambda a, b : a if a >b else b
    print(fn(1, 2))
    
    # 列表数据按字典 key 的值排序
    students = [
      {'name': 'tom', 'age': 20},
      {'name': 'rose', 'age': 22},
      {'name':'rose', 'age': 23}]
    
    students.sort(key = lambda x: x['name'])
    print(students)

```


# 高阶函数
&emsp;&emsp;把函数作为参数传递，这样的函数称为高阶函数，高阶函数是函数式编程的体现
&emsp;&emsp;函数式编程大量使用函数，减少了代码的重复修改

* **内置函数**
 * abs()，数字求绝对值
 * round()，数字四舍五入
    
                    
* **高阶函数体验**

```python
    def sum_num(a, b, f):                      # 形参占位
      return f(a) + f(b)            
     
    result = sum_num(-1, 2, abs)               # 将 函数名 以实参代入
    print(result)
    
    result = sum_num(-1, 2, round)             # 只需要修改传递函数就可以改变整个函数作用
    print(result)

```

* **内置高阶函数**
 * map()
 
   map(func, list)，将传入的函数（名） func **（函数功能）**作用到 list 变量的每个元素中，并将结果组成新的列表(Py2) / 迭代器(Py3)

  ```python
    # 求列表中元素的 2 次方
    list1 = [1, 2, 3, 4, 5]
    
    def func(x):                            # 定义计算 2 次方函数
      return x ** 2

    result = map(func, list1)               # 将 函数名 作为第一个参数代入

    print(result)                           # 返回迭代器内存地址
    print(list(result))                     # 转换列表
 
  ```

 * reduce()

   reduce(func, list)，其中**func 必须有两个参数**，每次 func 计算的结果继续和序列的下一个元素做**累积计算**

  ```python
    # 计算列表序列中各个数字的累加和
    import functools
    list1 = [1, 2, 3, 4, 5]
    
    def func(a, b):
    return a + b

    result = functools.reduce(func, list1)
    print(result)
  ```

 * filter()
   
   filter(func, list)，用于过滤序列，过滤掉不符合条件的元素，返回一个 filter 对象
  
 ```python
    list1 = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
    def func(x):
    return x % 2 == 0

    result = filter(func, list1)
    print(result)
    print(list(result))
```























