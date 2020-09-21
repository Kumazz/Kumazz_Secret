# Origin Base

### Python
&emsp;&emsp;**Python 2:** 已于 2020 年 1 月 1 日停止 Python 2 的技术支持
&emsp;&emsp;**Python 3:** Python 主流版本，性能更加丰富完善
>本文档 Python 解释器版本 3.9 ，系统环境是 Mac OS，编辑器是 Pycharm，穿插一些 windows 案例或图片

### 安装验证

* **下载:** 【 [点击下载](https://www.python.org/downloads/) 】，页面自动判断你的操作系统推荐下载对应 Python 安装程序 

![](/assets/QQ20200917-171730@2x.png)

* **安装:**
双击 Python 安装文件 —  **勾选 [ Add Python 3.9 to PATH ]** -- 点击 [ Install Now ] -- [ Next ] ，按提示操作即可
![](/assets/QQ20200917-172121@2x.png)

* **验证:** 
  * windows 系统有 2 种验证方式
   * 在 **开始菜单** 中找到 Python 安装目录，点击打开 **IDLE** ，出现选框中语句即安装成功
   ![](/assets/WechatIMG1251.png)
   * 或按住 **win + R** 键调出运行菜单输入 **cmd** 调出终端，输入 **Python** ，出现选框中语句即安装成功
   
 ![](/assets/QQ20200918-094923@2x.png)

  * Mac OS 已预装 Python2 ，在安装 Python3 后需要单独输入 **Python3** 进行调用，否则输入 Python 默认启动 Python2
  
  ![](/assets/QQ20200918-100345@2x.png)


### 解释器
&emsp;&emsp;帮助我们将 Python 代码，也就是 .py 文件，交给机器可以执行的工具
*  **Python 解释器种类** 
  * CPython，C 语⾔开发的解释器[官⽅]，应⽤广泛的解释器   
  * IPython，基于 CPython  的⼀种交互式解释器
  
  
*  **其他解释器**
 * PyPy，基于 Python 语⾔开发的解释器
 * Jython，运⾏在 Java 平台的解释器，直接把 Python 代码编译成Java字节码执⾏   
 * IronPython，运⾏在微软 .Net 平台上的 Python 解释器，把 Python 代码编译成 .Net 的字节码
  

*  **IDLE 代码含义**

```python
    Python 3.9.0b5 (v3.9.0b5:8ad7d506ca, Jul 20 2020, 14:25:25) 
    [Clang 6.0 (clang-600.0.57)] on darwin
    Type "help", "copyright", "credits" or "license" for more information.
    >>> 

```
&emsp;&emsp;上述三行代码包含了 **解释器** 和所在 **操作系统** 的信息，例子中的 3.9.0b5，使用 3 开头即运行的是 Python3 版本解释器
&emsp;&emsp;最后一行 「 >>> 」是提示符，表示解释器已经就绪，可以输入代码进行操作或者表示结果展示


### 编辑器
&emsp;&emsp; Python 自带的 IDLE 做大型开发时受到限制，可以使用如: SublimeText、VSCode、Pycharm 等专业工具做开发，建议使用 **Pycharm**
* **Pycharm:** [点击下载](https://www.jetbrains.com/pycharm/download/)， Pycharm 专业版是收费的软件，可以下载社区版进行前期学习
* **VSCode:** [点击下载](https://code.visualstudio.com/)，免费的开发编辑器，需要配合相关插件完成 Python 的相关开发，可以搜索 VSCode For Python 的视频进行补充学习


### 环境变量
> windows 系统添加 Python 环境变量，只需在安装解析器程序时勾选 Add Python 3.9 to PATH，如果忘了勾选，可以重新安装勾选一下；

【 [win7 手动添加环境变量](https://jingyan.baidu.com/article/bea41d436879a4b4c51be6f9.html) 】
【 [win10 手动添加变量](https://www.cnblogs.com/hyf20131113/p/12058994.html) 】

### 拓展
&emsp;&emsp; Mac OS 设置 Python3 为主解释器


```shell
   which python3                                   # 查询 Python3 安装位置
   vi ~/.bash_profile                              # 用 vim 打开文件
   按 i 键                                          # 在 insert 模式下写入命令
   alias python="查询的路径"
   按 esc 键，按 : ，输入 wq！                        # 保存文件
   source ~/.bash_profile                          # 文件生效

```


















