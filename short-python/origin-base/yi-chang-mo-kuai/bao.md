# 包
&emsp;&emsp;有联系的模块放在同一个文件夹下，并且在这个文件夹下创建一个名字为 **\_\_init\_\_.py** 文件，那么这个文件夹称之为**包**

### 制作包

*  **pycharm 创建**
  * [New] -- [Python Package] - 输入包名 - [OK] --新建功能模块(有联系的模块)
  *  新建包后，包内部会自动创建 **\_\_init\_\_.py** 文件，这个文件控制着包的导入
  
  
*  **新建模块**


```python
    # my_module1
    print(1)

    def info_print1():
      print('my_module1') 
      
    # my_module2
    print(1)

    def info_print1():
      print('my_module1')
```

### 导入包

*  **方法一**


```python
    import 包名.模块名
    
    包名.模块名.目标
    -------------------------------------
    import my_package.my_module1
    
    my_package.my_module1.info_print1()

```


*  **方法二**
&emsp;&emsp;在 **\_\_init\_\_.py** 文件中添加 \_\_all\_\_ = []，控制允许导入的模块列表



```python
    from 包名 import *
    模块名.目标
    ------------------------------------
    from my_package import *
    my_mpdule1.info.print1()

```












