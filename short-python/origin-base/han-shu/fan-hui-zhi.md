# 返回值
### 作用
*  Python 每个函数都应该有一个返回值； return 语句是 Python 语言中函数返回的一个值
  *  return 返回值可以是一个数值，一个字符串，一个布尔值或者一个列表
  *  有 return 返回值才是完整的函数，不带参数值的 return 语句返回 None
  *  return 用于退出函数，选择性地向调用方返回一个表达式
  *  退出当前函数，导致 return 下方的所有代码(函数体内部)不执行



### 案例

* **返回写法**

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
    return 50

    def testB(num):                # 需定义形参用于接收返回值
        print(num)

    result = testA()

    testB(result)                  >>> 50     # 返回值作为参数传递

```

* **多个返回值写法**


```python
    def return_num():
    return 1, 2                           # 以 ，隔开

    result = return_num()
    print(result)                         # 返回的是元组

```













