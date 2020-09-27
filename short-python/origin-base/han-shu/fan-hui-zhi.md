# 返回值
### 作用
*  Python 每个函数都应该有一个返回值，return 语句是 Python 语言中函数返回的一个值
  *  有 return 返回值才是完整的函数，不带参数值的 return 语句返回 None
 



### 案例

* **返回写法**
 * return 用于退出函数，选择性地向调用方返回一个表达式，同时 return 下方的所有代码(函数体内部)不执行
 
 ```python
    def buy():
        return '糖'
        print('ok')               # 运行后查看是否执行该代码
    goods = buy()                 # 使用变量保存函数返回值
    print(goods)
 ```

* **返回值作为参数传递**


```python
    def testA():
        return 50                  # 返回值可以是数值、字符串、布尔值、列表、元组

    def testB(num):                # 需定义形参用于接收返回值
        print(num)

    result = testA()

    testB(result)                  # 返回值作为参数传递
    -------------------------------------------------------------------------                
    >>> 50     

```

* **多个返回值写法**


```python
    def return_num():
        return 1, 2                           # 可以用元组返回多个值

    result = return_num()
    print(result)                             # 返回的是元组

```













