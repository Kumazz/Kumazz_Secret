# 文件操作加强

### 文件备份



```python
    # 任意文件添加 备份 样式
    old_file_name = input('请输入您要备份的文件: ')

    index = old_file_name.rfind('.')

    if index > 0:                                      # 后缀下标是大于 0 的
        postfix = old_file_name[index:]

    new_file_name = old_file_name[:index] + '[备份]' + postfix

    old_file = open(old_file_name)
    new_file = open(new_file_name, 'w')

    while True:
        con = old_file.read(1024)
        if len(con) == 0:
            break
        new_file.write(con)

    old_file.close()
    new_file.close()
```

### 文件和文件夹操作
&emsp;&emsp;在 Python 中文件和文件夹的操作要借助 **os 模块**

*  文件操作
  *  导入模块，import os
  *  os 模块方法，os.函数名()
  
  ```python
      # 重命名文件
      os.rename( 目标文件名,新文件名 )
      
      # 删除文件
      os.renove( 目标文件名 )
  ```

*  文件夹操作
  *  导入模块，import os
  *  os 模块方法，os.函数名()
  
  ```python
      # 创建文件夹
      os.mkdir(文件夹名)
      
      # 删除文件夹
      os.rmdir( 文件夹名 )
      
      # 重命名文件夹
      os.rename( 文件夹名 )
      
      # 获取当前目录，需变量接收
      os.getcwd()
      
      # 改变默认目录
      os.chdir( 目录 )
      
      # 获取目录列表，以列表的形式返回一级目录下的目录
      os.listdir( 目录 )
  ```


### 批量操作文件或文件夹
* 添加指定重命名


```python
    import os
    file_list = os.listdir()

    for i in file_list:
        new_name = 'Python' + i
        os.rename(i, new_name)

```

















