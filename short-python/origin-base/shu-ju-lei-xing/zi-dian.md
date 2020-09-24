# 字典
### 认识字典
&emsp;&emsp;数据通过 **键值对** 形式出现，字典数据和数据顺序没有关系，即**字典不支持下标**，而是**通过键名查找数据**
&emsp;&emsp;**可变数据类型**


### 字典特征
*  **{ key1: item1, key2: item2 }**
  *  符号为**大括号{}**
  *  数据为**键值对**形式出现
  *  各个键值对之间用**逗号**隔开
  *  空字典: { } 或 dict()


### 字典方法
#### 增或改，如果 key 存在则修改 key 对应的值，如果 key 不存在则新增此键值对

* **字典序列 [key ] = valum**

#### 删除，通过函数的形式增加元组中的数据

* 字典序列**.clear**( 数据 )
  * 保留空字典
  
  
* 删除列表 -- del或del()
  * del 目标 或 del(目标)
  * del 字典[key]，可以删除指定key数据
  

#### 查找

* 通过 key 查找 value
  * 字典序列[key]
  * 存在返回值，不存在返回错误
  
  
* get()函数查找
  * 字典序列.get(key, 默认值)
  * 如果当前查找的 key 不存在则返回第二个参数(默认值)，如果省略第二个参数，则返回 None
  


```python
    dict1 = {'name': 'Tom', 'age': 20, 'gender': '男'}       
    print(dict1.get('name'))
    print(dict1.get('id', 110))
    print(dict1.get('id')) 
    --------------------------------------------------------------
    >>> Tom 
    >>> 110                                             # 设置默认值
    >>> None

```


* keys()函数查找
  * 字典序列.keys()
  * 列举出 key 名，返回可迭代对象[ 可以遍历的对象 ]
  

```python
    dict1={'name':'Tom','age':20,'gender':'男'}
    print(dict1.keys())
    ---------------------------------------------------------
    >>> (['name', 'age', 'gender'])

```
  

* values()函数查找
  * 字典序列.values()
  * 列举出所有的值，返回可迭代对象
  
  
* items()函数查找
  * 字典序列.items()
  * 列举出所有的键和值，返回可迭代对象，里面的数据是元组


#### 循环遍历
* 遍历字典的 key
  * for key in 字典序列.keys()
  


```python
    dict1 = {'name': 'Tom', 'age': 20, 'gender': '男'} 
    for key in dict1.keys():
      print(key)
    ------------------------------------------------------
    >>> name 
        age
        gender
```


  
* 遍历字典的 value
  * for value in 字典序列.values()
  
* 遍历字典的元素( key 和 value )
  * for item in 字典序列.items()
  * 返回元组，元组1是 key ，元组2是 value
  
* 遍历字典的的键值对，即 拆包
  * for key, value in 字典序列.items()




























  
  



