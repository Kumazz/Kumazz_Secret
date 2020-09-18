# Origin Base

### Python
&emsp;&emsp;**Python 2:** 已于 2020 年 1 月 1 日停止 Python 2 的技术支持
&emsp;&emsp;**Python 3:** Python 主流版本，性能更加丰富完善
>本文档 Python 解释器版本 3.9 ，系统环境是 Mac OS，穿插一些 windows 案例或图片

### 安装验证

* **下载:** 【 [点击下载](https://www.python.org/downloads/) 】，页面自动判断你的操作系统推荐下载对应 Python 安装程序 

![](/assets/QQ20200917-171730@2x.png)

* **安装:**
双击 Python 安装文件 —  **勾选 [Add Python 3.9 to PATH ]** -- 点击 [ Install Now ] -- [ Next ]，按提示操作即可
![](/assets/QQ20200917-172121@2x.png)
> windows 系统添加 Python 环境变量，只需要在安装解析器程序时勾选 Add Python 3.9 to PATH，如果忘了勾选，可以重新安装勾选一下；Mac 系统不需要设置

* **验证:** 
  * 在**开始菜单**中找到 Python 安装目录，点击打开 **IDLE** 即可
  * 在**运行**输入 **cmd** 调出终端，输入 Python 即可调用
  * Mac OS 已预装 Python2 ，在安装 Python3 后需要单独输入 Python3 进行调用，否则输入 Python 默认启动 Python2
![](/assets/Lark20200803-111505.png)


```python
    Python 3.9.0b5 (v3.9.0b5:8ad7d506ca, Jul 20 2020, 14:25:25) 
    [Clang 6.0 (clang-600.0.57)] on darwin
    Type "help", "copyright", "credits" or "license" for more information.
    >>> 

```
&emsp;&emsp;&emsp;上述三行代码包含了**解释器**和所在**操作系统**的信息，例子中的 3.9.0b5，使用 3 开头即运行的是 Python3
&emsp;&emsp;&emsp;最后一行是提示符，表示解释器已经就绪，可以输入代码


### Pycharm
&emsp;&emsp;尽管有各种适合 Python 开发的编辑器工具，如: SublimeText、VSCode等，作为 Python 开发建议使用专业的开发工具 Pycharm
* **Pycharm:** [点击下载](https://www.jetbrains.com/pycharm/download/)， Pycharm 专业版是收费的软件，可以下载社区版进行前期学习
* **VSCode:** [点击下载](https://code.visualstudio.com/)，免费的开发编辑器，需要配合相关插件完成 Python 的相关开发，可以搜索 VSCode For Python 的视频进行补充学习

### 解释器
&emsp;&emsp;帮助我们将 Python 代码，也就是 .py 文件，交给机器可以执行的工具，即运行文件

*  **Python解释器种类** 
  * CPython，C 语⾔开发的解释器[官⽅]，应⽤广泛的解释器   
  * IPython，基于 CPython  的⼀种交互式解释器
  
  
*  **其他解释器**
  * PyPy，基于 Python 语⾔开发的解释器
  * Jython，运⾏在Java平台的解释器，直接把 Python 代码编译成Java字节码执⾏   
  * IronPython，运⾏在微软 .Net 平台上的 Python 解释器，把 Python 代码编译成 .Net 的字节码







