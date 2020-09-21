# 循环控制
### while 循环，又叫迭代

*  **while... 单条件**

```python
    while 条件: 
        条件成立重复执行的代码1
        条件成立重复执行的代码2
        ........
        
    # 计数器的习惯，在计算机中计数器一般默认初始值从 0 开始，这是一种(工作)习惯，可以根据实际情况设置初始值

    i = 0
    while i < 3:
        print('hello python')
        i += 1                      # 通过计数器控制，防止陷入死循环
      
```

* **while...else** ，else下方缩进的代码指的是**当循环正常结束之后要执行的代码**


```python
    while 条件:
        条件成立重复执行的代码
    else：
        循环正常结束之后要执行的代码

```

### while 嵌套


```python
    while 条件1:
        条件1成立执行的代码
        ......
        while 条件2:
            条件2成立执行的代码
            ......
            
    --------------------------------------
    # 九九乘法表
    i = 1
    while i <= 9:
        j = 1
        while j <= i:
            print(f'{j} x {i} = {i * j}',end='\t')   # \t制表符，用于对齐
            j += 1
        print()
        i += 1
```


### for 语法
* **for...in**

```python
    # 在 for 循环中 continue 不需要改变计数器 
    for 临时变量 in 序列:
        重复执行的代码1
        重复执行的代码2
        ...........
```
* **for...in...else**

```python
    for 临时变量 in 序列:
        重复执行的代码
    else:
        循环正常结束之后要执行的代码

```

### break 和 continue 
&emsp;&emsp; 循环中满足一定条件退出循环的两种不同方式
*  **break**，满足条件后**break后面**的语句就不执行了，**终止此循环**



```python
    i = 1
    while i <= 5:
        if i == 3:
            print('这一步后不执行')
            break
        print(f'继续第{i}个')
        i += 1

```


*  **continue**，满足条件后**退出当前循环继而执行下一句代码**，但是要在** contine 前修改计数器**进行循环否则进入死循环


```python
    i = 1
    while i <= 5:
        if i == 3:
            print('这一步不执行')
            i += 1
            continue
        print(f'继续第{i}个')
        i += 1

```


### 拓展
*  **while...else 与 break**

```python
    # break后面的代码一律不运行，包括else
    
    while 条件1:
        条件1成立执行的代码
        break
    else:
        条件2成立执行的代码

```

*  **while...else 与 continue**



```python
    # continue 后面的代码会被执行，包括else，但是注意在 continue 前改变计数器避免死循环
    
    while 条件1:
        条件1成立执行的代码
        计数器修改
        continue
    else:
        条件2成立执行的代码

```

*  **for...in...else 与 while 一样**，遇到 break 后面都不执行，遇到 continue 后面继续执行






















