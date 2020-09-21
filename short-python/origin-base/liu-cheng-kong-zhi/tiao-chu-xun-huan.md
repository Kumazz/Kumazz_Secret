# 跳出循环
### break 
&emsp;&emsp; 循环中满足一定条件退出循环的两种不同方式
*  **break**，满足条件后**循环体内 break 后面**的语句就不执行了，**终止此循环**



```python
    i = 1
    while i <= 5:
        if i == 3:
            print('第 3 步后不执行')
            break
        print(f'第{i}步')
        i += 1
    print('循环结束')
    -----------------------------------------------------------
    >>> 第 1 步
    >>> 第 2 步
    >>> 第 3 步后不执行了
    >>> 循环结束                              # 循环体外部的依旧执行

```

### continue 

*  **continue**，满足条件后**退出当前循环继而执行下一句代码**，但是要在** contine 前修改计数器**进行循环否则进入死循环


```python
    i = 1
    while i <= 5:
        if i == 3:
            print('第 3 步不执行')
            i += 1
            continue
        print(f'继续第{i}步')
        i += 1
    -----------------------------------------------------------
    >>> 继续第 1 步
    >>> 继续第 2 步
    >>> 第 3 步不执行
    >>> 继续第 4 步
    >>> 继续第 5 步

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






















