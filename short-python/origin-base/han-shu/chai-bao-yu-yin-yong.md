# 拆包与引用
### 拆包
*  **组包**，将多个值同时赋给一个变量时,解释器会进行自动组包操作
*  **拆包**，是将一个序列类型的数据拆开同时赋值多个变量,解释器会进行拆包操作
  *  **元组拆包**
  
  ```python
    def return_num():
    return 120, 220

    num1, num2 = return_num()
    print(num1)                           >>> 120
    print(num2)                           >>> 220
  ```
  
  * **字典拆包**
  
  ```python
    dict1 = {'name':'tom', 'age':19}
    a, b = dict                             # 字典内是两个键值对，需要两个变量接收数据
    
    print(a)                                >>> name         # 取出的是key
    print(b)                                >>> age
    
    print(dict1[a])
  ```

*  **交换变量值**


```python
    a = 10
    b = 20
    
    a, b = b, a

```


### 引用
 &emsp;&emsp;&emsp;值是靠**引用**来传递的
 &emsp;&emsp;&emsp;可以用 **id( )** 判断两个变量是否为同一个值的引用
 &emsp;&emsp;&emsp;id值理解为内存的地址标识


### 

