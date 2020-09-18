# Bug与Debug
### Bug
&emsp;&emsp;Bug 指程序运行时出现错误，Debug 指调试 bug 纠正错误
*  **常规排查方法**， 通过控制台显示报错查看报错类型排查

![](/assets/QQ20200918-134520@2x.png)

### 常见报错类型
*  **SyntaxError: 语法错误**，代码不符合 Python 的语法规范 
 *  invalid character in identifier: 有无效标识符，检查一下中英文符号
 *  unexpected EOF while parsing: 无法解析的符号，检查一下是否多了或者少了括号 
    
            
*  **IndexError: 下标(索引)错误**，超出索引范围
 *  list index out of range: 检查列表是否正确 
      
                    
*  **TypeError: 数据类型错误**，该数据不是正确的数据类型
 *  must be str, not int: 字符串和数字直接拼接，检查一下数据类型    
    
                            
*  **IndentationError: 缩进错误**
 *  expected an indented block: 检查一下代码的缩进是否正确     
     
                       
*  **KeyError: 键错误，一般是 key 名错误或不存在**
 *  "fond": 字典中没有该的 key 对应的值，检查一下键名或者字典数据是否正常   
      
                  
*  **ValueError: 值错误**
 *  substring not found: 输入的数据类型跟要求的不符合
       
                                   
*  **NameError: 未初始化对象，变量名错误**
  *  name "a" is not defined: 变量没有被定义 
       
                                 
*  **AttributeError: 属性错误，检查一下数据类型**
  * "tuple" object has no attribute "remove": 该对象没有这个属性、方法  
      
                    
* **UnicodeDecodeError: 编、解码错误**
  * UnicodeDecodeError/UnicodeEncodeError/UnicodeTranslateError: 解码/编码/转换时的错误


* **其它错误**
  * ImportError: 导入包错误
  * NotImplementedError: 某个方法没有实现的错误
  * StopIteration: 迭代器已经到最后
  * TabError: 包含了 tab 和空格错误
  * UnicodeEncodeError: Unicode 编码错误，一般是 unicode->str 错误
  * UnicodeDecodeError: Unicode 解码错误，一般是 str->unicode 错误
  * FileNotFoundError: 文件没有找到的错误
  
       
### Debug
&emsp;&emsp; Pycharm 集成了调试程序的 Debug 工具
*  **断点调试方法:** 在要调试的代码与代码行号位置**单击**后形成红色标注即打上断点，运行 Debug 调试，快捷键: CMD + Shift + D
![](/assets/QQ20200918-135812@2x.png)

 * 调试按钮
    * step over: 跳过子函数
    * step into: 进入子函数
    * step into my code: 不执行源码的子函数执行自己的
    * step out: 跳出当前函数
    * run to cursor: 执行到光标处

*  **[pdb 调试案例](https://www.cnblogs.com/c-x-a/p/10674288.html)**，推荐用 Debug 工具调试

 



















   










       
    
    
      
