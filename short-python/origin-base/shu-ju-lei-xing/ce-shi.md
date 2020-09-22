




# 取出字母 python
print(a[5:]) ， 如果结束下标不写默认选取到最后
# 选取所有
print(a[:])
# 倒序排列
print(a[::-1])

```


### 字符串方法
#### 查找，查找子串在字符串中的位置或出现的次数

* 字符串序列**.find**( 子串,开始位置下标,结束位置下标 )
* 字符串序列**.rfind**( 子串,开始位置下标,结束位置下标 )，查找方向从**右侧**开始
* 开始和结束位置下标可以省略，表示在整个字符串序列中查找
* 如果存在就返回子串开始的位置下标，**否则返回 -1**

```python

mystr = 'hello world and my baby'
print(mystr.find('lo')) # 查找 lo 位置
print(mystr.find('or',2,9)) # 限定区间查找子串
print(mystr.find('ors')) # 查找不到

```

* **字符串序列.index( 子串,开始位置下标,结束位置下标 )**
* 字符串序列**.rindex**( 子串,开始位置下标,结束位置下标 )，查找方向**右侧**开始
* 开始和结束位置下标可以省略，表示在整个字符串序列中查找
* 如果存在就返回子串开始的位置下标，**否则返回错误**
* **字符串序列.count( 子串,开始位置下标，结束位置下标 )**
* 开始和结束位置下标可以省略，表示在整个字符串序列中出现的次数
* 如果存在就返回存在的次数，**否则返回 0**


#### 修改，通过函数的形式修改字符串中的数据

* 字符串序列**.replace**( 旧子串,新子串,替换次数 )
* 如果查出子串次数，则替换次数为子串出现次数
* replace 返回值是修改后的字符串(赋值给变量)，**不会修改原来字符串**

```
mystr = 'hello world and my baby'
new_str = mystr.replace('o','a',1)) # 指定次数替换
print(new_str)
```

* **字符串序列.split( 分割字符,num )**
* num表示分割字符出现的次数，即将来返回**数据**个数为 num+1 个
* split 返回是列表，会丢失分隔字符


* **字符或子串.join( 多字符串组成的子列 )**，用一个字符或子串合并字符串
* 返回新的字符串


```python
mylist = ['aa', 'bb', 'cc']
new_str = '...'.join(mylist)

```

* **其他修改函数**


```python
mystr = 'hello python and worlf'
# 将字符串第一个字符转换成大写，其他依旧小写
print(mystr.captilize())
# 将字符串每个首字母大写
print(mystr.title())
# 将字符串中小写转大写
print(mystr.upper())
# 将字符串中大写转小写
print(mystr.lower())
# 删除字符串左、右、两边空白字符
print(mytstr.lstrip/rstrip/strip() )
# 左、中、右对齐
print(mystr.ljust/rjust/center(长度,填充字符))
```

#### 判断，判断真假，返回的结果是布尔型数据类型

* **字符串序列.startswith( 子串，开始位置下标，结束位置下标 )**
* 开始和结束位置下标可以省略，表示在整个字符串序列中查找
* 检查字符串以以指定子串开头，是则返回 True，否则返回False

* **字符串序列.endswith( 子串，开始位置下标，结束位置下标 )**
* 开始和结束位置下标可以省略，表示在整个字符串序列中查找
* 检查字符串以以指定子串结尾，是则返回 True，否则返回False


* **其他判断函数**，存在返回 True，否则返回 False


```python
mystr = 'hello python and worlf'
# 判断字符串是不是字母组成，注意空格
print(mystr.isalpha())
# 判断字符串是不是数字组成，注意空格
print(mystr.isdigit())
# 判断字符串是不是数字、字母、空格组成
print(mystr.isalnum())
# 判断字符串是不是由空格(白)组成
print(mystr.isspace())
```


### 拓展
* **len()函数**，返回一个数据长度

&emsp;&emsp; 用 len 获取一个字符串的最后一个字符
```python
fruit = 'banana'
length = len(fruit)
last = fruit[length-1]

```
&emsp;&emsp; banana 这个字符在第「6」个位置是没有字母的，因为下标从 0 开始，所以一共 6 个字母的顺序是 0 到 5，因此要在字符长度上减去 1







