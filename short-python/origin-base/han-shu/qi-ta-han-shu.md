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

















