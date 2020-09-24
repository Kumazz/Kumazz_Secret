# 推导式
### 认识推导式
&emsp;&emsp;用一个表达式创建一个有规律的列表或控制一个有规律的列表
&emsp;&emsp;推导式又叫生成式，返回的是对应的推导式性质
&emsp;&emsp;只有**列表推导式**、**字典推导式**、**集合推导式**

### 推导式案例

```python
    # 简单的推导式 
    list1 = [i for i in range(10)]
    print(list1)

    # 带 if 的推导式
    list2 = [i for i in range(10) if i % 2 == 0]
    print(list2)
    
    # 多个 for 循环推导式，就是 for 循环嵌套
    list3 = [(i, j) for i in range(1,2) for j in range(1,3)]
    prit(list3)
    
    # 字典推导式
    dict1 = { i: i**2 for i in range(1,5)}
    print(dict1)
    
    # 合并两个列表成为字典(列表数据个数相同)，如果数据个数不相同，len 统计数据少的列表
    dict1 = {list1[i]:list2[i] for i in range(len(list1))}
    print(dict1)
    
    # 提取字典中的目标数据
    counts = {k : v for k, v in counts.items() if 条件}
    print(counts)
    
   
    # 集合推导式，结果具有去重特点
    set1 = {i ** 2 for i in range(10)}
    print(set1) 
```


 


