原版

https://youtu.be/uNeVQ3auRZk

搬运

<iframe src="//player.bilibili.com/player.html?aid=684910953&bvid=BV1WU4y1R77P&cid=743181465&page=1" scrolling="no" border="0" frameborder="no" height="600" framespacing="0" allowfullscreen="true"> </iframe>

# 为什么是Python?

## Python的特性

- Python适用于不同的平台(Windows、Mac、Linux、Raspberry Pi等)。
- Python具有类似于英语的简单语法。
- Python的语法允许开发人员用比其他一些编程语言更少的行数来编写程序。
- Python在解释器系统上运行，这意味着代码可以在编写后立即执行。这意味着原型制作可以非常快。
- 可以以过程方式、面向对象方式或函数方式处理Python。

## 知识点

- Python的最新主要版本是Python3,我们将在本教程中使用它。然而，Python2虽然除了安全更新之外没有进行任何更新，但仍然很受欢迎。
- 在本教程中，Python将在Jupyter Note中编写。可以在集成开发环境中编写Python,例如Thonny、Pycharm、Netbeans或Eclipse,这在管理大量Python文件时特别有用。

## Python语法和编程语言的比较

- Python是为可读性而设计的，并且与受数学影响的英语语言有一些相似之处。
- Python使用新行来完成命令，而不是其他经常使用分号或括号的编程语言。
- Python依赖缩进，使用空格来定义作用域；例如循环、函数和类的范围。其他编程语言通常使用大括号。

# Python安装

略

# Python快速入门

## Windows通过命令行进入Python交互模式

要在python中测试少量代码，有时不将代码写入文件是最快和最简单的。这是因为Python本身可以作为命令行运行。在Windows、Mac或Linux命令行中键入以下内容：

~~~
C:\User\Name>python
Python 3.10.10 (tags/v3.10.10:aad5f6a, Feb  7 2023, 17:20:36) [MSC v.1929 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>> print('hello world')
hello world
>>>

如果要退出Python交互模式，输入‘exit()’即可
~~~

## 使用一个文本编辑器来写代码

Python是一种解释型编程语言，这意味着作为开发人员，您可以在文本编辑器中编写Python(.py)文件，然后将这些文件放入Python解释器中执行。在命令行中运行python.文件的方式是这样的：

~~~
C:\User\Name>python helloworld.py
其中“helloworld.py”是您的python文件的名称。
~~~

# 基础知识

## 语法

### 1.Python缩进

- 缩进是指代码行开头的空格。
- 在其他编程语言中，代码中的缩进只是为了可读性，而Python中的缩进非常重要。
- Python使用缩进来表示代码块。
- 如果你跳过缩进，Python会给你一个错误。
- 作为程序员，空格的数量取决于您，但必须至少为一个。
- 你必须在同一个代码块中使用相同数量的空格，否则Python会给你一个错误。

### 2.Python变量

- 在Python中，当你给它赋值时会创建变量。

###3.Python注释

- Python具有用于代码文档的注释功能。注释以#开头，Python会将行的其余部分渲染为注释。

## 注释

### 1.Python注释

- 注释可用于解释Python代码.
- 注释可用于使代码更具可读性。
- 注释可用于在侧试代码时阻止执行。

### 2.创建注释

- 注释以#开头，Python会忽略它们。
- 注释可以放在一行的末尾，Python将忽略该行的其余部分
- 注释不一定是解释代码的文本，它还可以用来阻止Python执行代码

### 3.多行注释

- Python并没有真正的多行注释语法。要添加多行注释，您可以为每一行插入#
- 您可以使用多行字符串。由于Python将忽路未分配给变量的字符串文字，因此您可以在代码中添加多行字符串（三引号），并将您的注释放在其中

~~~python
'''
This is a comment
written in
more than just one line
'''
pirnt("hello world")
~~~

## 变量

### 1.Python变量

#### 1.创建变量

- Python没有用于声明变量的命令。变量在您第一次为其赋值时创建。
- 变量不需要用任何特定类型声明，甚至可以在设置后更改类型。

#### 2.强制转换

- 如果要指定变量的数据类型，可以通过强制转换来完成。

~~~python
x = str(3)	#'3'
y = int(3)	#3
z = float(3)#3.0
~~~

#### 3.获取类型

您可以使用type()函数获取变量的数据类型。

~~~python
print(type(x))
~~~

#### 4.单引号还是双引号

可以使用单引号或双引号来声明字符串变量。

#### 5.区分大小写

变量名区分大小写。

### 2.变量名

#### 1.变量名

变量可以有一个简短的名称（如x和y)或一个更具描述性的名称(age、name、total_volume)。Python变量的规则：

- 变量名必须以字母或下划线字符开头
- 变量名不能以数字开头
- 变量名称只能包含字母数字字符和下划线(A-Z、0-9和_)
- 变量名区分大小写(age、Age和AGE是三个不同的变量)

#### 2.多字变量名

包含多个单词的变量名称可能难以阅读，您可以使用多种技术使它们更具可读性。

- 骆驼形式：除了第一个单词外，每个单词都以大写字母开头。
- 帕斯卡形式：每个单词都以大写字母开头。
- 蛇形式：每个单词由下刻线字符分隔。

### 3.分配多个值

#### 1.多个变量的多个值

Python允许您在一行中为多个变量赋值。

~~~python
x,y,z='orange','banana','cherry'
print(x)
print(y)
print(z)
~~~

#### 2.多个变量的一个值

您可以在一行中为多个变量分配相同的值,

~~~python
x = y = z = 'apple'
print(x)
print(y)
print(z)
~~~

#### 3.拆分集合

如果您在列表、元组等中有一组值。Python允许您将值提取到变量中，这称为拆包。

```python
fruits = ['apple','banana','cherry']
x,y,z = fruits
print(x)
print(y)
print(z)
```

### 4.输出变量

Python打印语句通常用于输出变量，为了结合文本和变量，Python便用+字符。

```python
#代码：
x = 'awesome'
print('Python is ' + x)
#运行结果：
Python is awesome
```

您还可以使用+字符将变量添加到另一个变量。

~~~python
#代码：
x = 'Python is '
y = 'awesome'
print(x + y)
#运行结果：
Python is awesome
~~~

对于数字，+字符用作数学运算符。

~~~python
#代码：
x = 5
y = 10
print(x + y)
#运行结果：
15
~~~

如果你尝试组合一个字符串和一个数字，Python会给你一个错误。

~~~python
#代码：
x = 5
y = 'John'
print(x + y)
#运行结果：
TypeError: unsupported operand type(s) for +: 'int' and 'str'
~~~

### 5.用户输入

- Python允许用户输入。
- 这意味着我们可以要求用户输入。
- Python3.6中的方法与Python2.7中的方法略有不同。
- Python3.6使用input(0)方法。
- Python2.7使用aw_input(0)方法。

### 6.全局变量

#### 1.全局变量

- 在函数外部创建的变量（如上述所有示例中）被称为全局变量。
- 每个人都可以使用全局变量。无论是在函数内部还是外部。

~~~python
#代码：
x = 'awesome'

def myfunc():
    print('Python is ' + x)
    
myfunc()
#运行结果：
Python is awesome
~~~

- 如果在函数内部创建同名变量，该变量将是局部变量，只能在函数内部使用，具有相同名称的全局变量将保持原样，全局且具有原始值。

~~~python
#代码：
x = 'awesome'

def myfunc():
    x = 'fantastic'
    print('Python is ' + x)
    
myfunc()

print('Python is ' + x)
#运行结果：
Python is fantastic
Python is awesome
~~~

#### 2.全局变量关键字

- 通常，当您在函数内部创建变量时，该变量是局部的，并且只能在该圆数内部使用。
- 要在函数内创建全局变量，可以使用global关键字。

~~~python
#代码：
def myfunc():
    global x
    x = 'fantastic'
    
myfunc()

print('Python is ' + x)
#运行结果：
Python is fantastic
~~~

- 此外，如果要更改函数内的全局变量，请使用global关键字。

~~~python
#代码：
x = 'awesome'

def myfunc():
    global x
    x = 'fantastic'
    
myfunc()

print('Python is ' + x)
#运行结果：
Python is fantastic
~~~

## 数据类型

### 1.内置数据类型

- 在编程中，数据类型是一个重要的概念。
- 变量可以存储不同类型的数据，不同的类型可以做不同的事情。
- 默认情况下，Python具有以下内置数据类型，在这些类别中：

> 文本类型：str
> 数字类型：int,float,complex
> 序列类型：list、tuple、range
> 映射类型：dict
> 焦台类型：set、frozenset
> 布尔类型：bool
> 二进制类型：bytes、bytearray、memoryview

### 2.获取数据类型

您可以使用type()函数获取变量的数据类型。

~~~python
print(type(x))
~~~

### 3.设置数据类型

在Python中，数剧类型是在为变量赋值时设置的：

```python
# 字符串：str
x = 'Hello World'
# 整形：int
x = 20
# 浮点型：float
x = 20.5
# 复数型：complex
x = 1j
# 数组：list
x = ['apple', 'banana', 'cherry']
# 数组(一旦初始化就不能修改)：tuple
x = ('apple', 'banana', 'cherry')
# 范围数字：range
x = range(6)  # 表示6的范围数字，从0到6
# 字典型：dict
x = {'name': 'John', 'age': 36}
# dict
x = {'apple', 'banana', 'cherry'}
# frozenset
x = frozenset({'apple', 'banana', 'cherry'})
# 布尔型：bool
x = True
# bytes
x = b'Hello'
# bytearray
x = bytearray(5)
# memoryview
x = memoryview(bytes(5))
```

###4.设置特定数据类型

```python
x = str('Hello World')  # str
x = int(20)  # int
x = float(20.5)  # float
x = complex(1j)  # complex
x = list(('apple', 'banana', 'cherry'))  # list
x = tuple(('apple', 'banana', 'cherry'))  # tuple
x = range(6)  # range
x = dict(name='John', age=36)  # dict
x = set('apple', 'banana', 'cherry')  # dict
x = frozenset(('apple', 'banana', 'cherry'))  # frozenset
x = bool(5)  # bool
x = bytes(5)  # bytes
x = bytearray(5)  # bytearray
x = memoryview(bytes(5))  # memoryview
```

## 数值型

### 1.数字类型

Python共有三种数字类型：
- int
- float
- complex

数值类型的变量是在你给它们赋值时创建的。

要验证Python中任何对象的类型，请使用type()函数。

### 2.int

- lnt或integer，是一个整数，正负，不带小数，长度不平限。

### 3.float

- 浮点数是包含一位或多位小数的正数或负数。
- 浮点数也可以是带有"e"的科学数字，表示10的幂。

~~~python
x = 12E4
y = 87.21e12
~~~

###4.complex

- 复数写有"j”作为虚部

~~~python
x = 3+5j
~~~

### 5.类型转换

- 您可以使用int()、float()和complex()方法从一种类型转换为另一种类型

###6.随机数

- Python没有random()函数来生成随机数，但Python有一个名为random的内置模块，可用于生成随机数

~~~python
import random
print(random.randrange(1,10))
~~~

## 强制转换

有时您可能希望为变量指定类型。这可以通过构造函数来完成。Python是一种面向对象的语言，因此它使用类来定义数据类型，包括其原始类型。
因此，python中的转换是使用构造函数完成的：

- int()：从整数文字、浮点文字（通过删除所有小数）或字符串文字（提供字符串表示整数）构造整数
- float()：从整数文字、浮点文字或字符串文字构造浮点数（提供字符串表示浮点数或整数）
- str()：从多种数据类型构造一个字符串，包括字符串、整数文字和浮点文字

## 字符串

### 1.字符串

####1.字符串

- python中的字符串被单引号或双引号包围。
- `'hello'`和`"hello"`是一样的.
- 您可以使用`print()`函数显示字符串文字：

####2.将字符串分配给变量

将字符串分配给变量是通过变量名后跟等号和字符串来完成的。

~~~python
a = 'hello'
~~~

####3.多行字符串

您可以使用三个引号将多行字符串分配给变量

~~~python
a = '''Lorem ipsum dolor sit amet
consectetur'''
~~~

#### 4.字符串是数组

- 像许多其他流行的编程语言一样，Python中的字符串是表示unicode字符的字节数组。
- 但是，Python没有字符数据类型，单个字符只是一个长度为1的字符串。
- 方括号可用于访问字符串的元素。

~~~python
#代码
a = 'hello world'
print(a[1])
#结果
e
~~~

#### 5.遍历字符串

由于字符串是数组，我们可以使用for循环遍历字符串中的字符。

~~~python
#代码
for x in 'banana':
    print(x)
#结果
b
a
n
a
n
a    
~~~

#### 6.字符串长度

要获取字符串的长度，请使用len()函数。

~~~python
#代码
a = 'hello world'
print(len(a))
#结果
11
~~~

#### 7.检查字符串

要检查字符串中是否存在某个短语或字符，我们可以使用关键字`in`、`not in`。

~~~python
#代码
txt = 'The best things in life are free!'
print('free' in txt)
#结果
Ture

#代码
txt = 'The best things in life are free!'
if 'free' in txt:
    print('yes,\'free\' is present.')
#结果
yes,'free' is present.

#代码
txt = 'The best things in life are free!'
print('expensive' not in txt)
#结果
Ture
~~~

### 2.字符串切片

#### 1.切片

您可以使用切片语法返回一系列字符。
指定开始索引和结束索引，以冒号分隔，以返回字符串的一部分。

~~~python
#代码
a = 'hello world'
print(a[2:5])
#结果
llo
~~~

#### 2.从头开始切片

通过省略开始索引，范围将从第一个字符开始。

```python
#代码
a = 'hello world'
print(a[:5])
#结果
hello
```

#### 3.切到最后

通过省略结束索引，范围将到最后。

```python
#代码
a = 'hello world'
print(a[2:])
#结果
llo world
```

#### 4.负索引

使用负索引从字符串结尾开始切片。

~~~python
#代码
a = 'hello world'
print(a[-5:-2])
#结果
wor
~~~

### 3.修改字符串

Python有一组可用于字符串的内置方法。

~~~python
#大写
#代码
a = 'hello world'
print(a.upper())
#结果
HELLO WORLD

#小写
#代码
a = 'HELLO WORLD'
print(a.lower())
#结果
hello world

#删除前后空格
#代码
a = '	hello world		'
print(a.strip())
#结果
hello world

#替换
#代码
a = 'hello world'
print(a.replace('world','python'))
#结果
hello python

#拆分字符串
#代码
a = 'hello world'
print(a.split('o'))
#结果
['hell', ' w', 'rld']
~~~

### 4.字符串连接

要连接或组合两个字符串，您可以使用+运算符。

```python
#代码
a = 'hello'
b = 'world'
c = a + b
d = a + ' ' + b
print(c)
print(d)
#结果
helloworld
hello world
```

### 5.字符串格式化

正如我们在Python变量一章中学到的，我们不能直接组合字符串和数字。但是我们可以通过使用format()方法来组合字符串和数字！

- format()方法接受传递的参数，格式化它们，并将它们放在占位符{}所在的字符串中。

```python
#代码
age = 36
txt = 'My name is John, and I am {}.'
print(txt.format(age))
#结果
My name is John, and I am 36.
```

- format()方法接受无限数量的参数，并放置在各自的占位符中。

```python
#代码
quantity = 3
itemno = 567
price = 49
myorder = 'I want {} pieces of item number {} for {:.2f} dollars.'
print(myorder.format(quantity,itemno,price))
#结果
I want 3 pieces of item number 567 for 49.00 dollars.

#代码
quantity = 3
itemno = 567
price = 49
myorder = 'I want {2} pieces of item number {0} for {1:.2f} dollars.'
print(myorder.format(quantity,itemno,price))
#结果
I want 49 pieces of item number 3 for 567.00 dollars.

#代码
myorder = 'I have a {carname}, it is a {model}.'
print(myorder.format(carname = 'Ford', model = 'Mustang'))
#结果
I have a Ford, it is a Mustang.
```

### 6.转义字符

- 要在字符串中插入非法字符，请使用转义字符。
- 转义字符是反斜杠\后跟要插入的字符。
- 非法字符的一个例子是被双引号包围的字符串中的双引号

```python
#代码
txt = "It is "it"."
#结果
SyntaxError: invalid syntax

#代码
txt = "It is \"it\"."
```

| 转义字符    | 描述                                                     |
| :---------- | :------------------------------------------------------- |
| \(在行尾时) | 续行符                                                   |
| \\          | 反斜杠符号                                               |
| \'          | 单引号                                                   |
| \"          | 双引号                                                   |
| \a          | 响铃                                                     |
| \b          | 退格(Backspace)                                          |
| \e          | 转义                                                     |
| \000        | 空                                                       |
| \n          | 换行                                                     |
| \v          | 纵向制表符                                               |
| \t          | 横向制表符                                               |
| \r          | 回车                                                     |
| \f          | 换页                                                     |
| \oyy        | 八进制数，y 代表 0~7 的字符，例如：\012 代表换行。       |
| \xyy        | 十六进制数，以 \x 开头，yy代表的字符，例如：\x0a代表换行 |
| \other      | 其它的字符以普通格式输出                                 |

### 7.字符串方法

| 方法                                                         | 描述                                               |
| :----------------------------------------------------------- | :------------------------------------------------- |
| [capitalize()](https://www.w3school.com.cn/python/ref_string_capitalize.asp) | 把首字符转换为大写。                               |
| [casefold()](https://www.w3school.com.cn/python/ref_string_casefold.asp) | 把字符串转换为小写。                               |
| [center()](https://www.w3school.com.cn/python/ref_string_center.asp) | 返回居中的字符串。                                 |
| [count()](https://www.w3school.com.cn/python/ref_string_count.asp) | 返回指定值在字符串中出现的次数。                   |
| [encode()](https://www.w3school.com.cn/python/ref_string_encode.asp) | 返回字符串的编码版本。                             |
| [endswith()](https://www.w3school.com.cn/python/ref_string_endswith.asp) | 如果字符串以指定值结尾，则返回 true。              |
| [expandtabs()](https://www.w3school.com.cn/python/ref_string_expandtabs.asp) | 设置字符串的 tab 尺寸。                            |
| [find()](https://www.w3school.com.cn/python/ref_string_find.asp) | 在字符串中搜索指定的值并返回它被找到的位置。       |
| [format()](https://www.w3school.com.cn/python/ref_string_format.asp) | 格式化字符串中的指定值。                           |
| format_map()                                                 | 格式化字符串中的指定值。                           |
| [index()](https://www.w3school.com.cn/python/ref_string_index.asp) | 在字符串中搜索指定的值并返回它被找到的位置。       |
| [isalnum()](https://www.w3school.com.cn/python/ref_string_isalnum.asp) | 如果字符串中的所有字符都是字母数字，则返回 True。  |
| [isalpha()](https://www.w3school.com.cn/python/ref_string_isalpha.asp) | 如果字符串中的所有字符都在字母表中，则返回 True。  |
| [isdecimal()](https://www.w3school.com.cn/python/ref_string_isdecimal.asp) | 如果字符串中的所有字符都是小数，则返回 True。      |
| [isdigit()](https://www.w3school.com.cn/python/ref_string_isdigit.asp) | 如果字符串中的所有字符都是数字，则返回 True。      |
| [isidentifier()](https://www.w3school.com.cn/python/ref_string_isidentifier.asp) | 如果字符串是标识符，则返回 True。                  |
| [islower()](https://www.w3school.com.cn/python/ref_string_islower.asp) | 如果字符串中的所有字符都是小写，则返回 True。      |
| [isnumeric()](https://www.w3school.com.cn/python/ref_string_isnumeric.asp) | 如果字符串中的所有字符都是数，则返回 True。        |
| [isprintable()](https://www.w3school.com.cn/python/ref_string_isprintable.asp) | 如果字符串中的所有字符都是可打印的，则返回 True。  |
| [isspace()](https://www.w3school.com.cn/python/ref_string_isspace.asp) | 如果字符串中的所有字符都是空白字符，则返回 True。  |
| [istitle()](https://www.w3school.com.cn/python/ref_string_istitle.asp) | 如果字符串遵循标题规则，则返回 True。              |
| [isupper()](https://www.w3school.com.cn/python/ref_string_isupper.asp) | 如果字符串中的所有字符都是大写，则返回 True。      |
| [join()](https://www.w3school.com.cn/python/ref_string_join.asp) | 把可迭代对象的元素连接到字符串的末尾。             |
| [ljust()](https://www.w3school.com.cn/python/ref_string_ljust.asp) | 返回字符串的左对齐版本。                           |
| [lower()](https://www.w3school.com.cn/python/ref_string_lower.asp) | 把字符串转换为小写。                               |
| [lstrip()](https://www.w3school.com.cn/python/ref_string_lstrip.asp) | 返回字符串的左修剪版本。                           |
| maketrans()                                                  | 返回在转换中使用的转换表。                         |
| [partition()](https://www.w3school.com.cn/python/ref_string_partition.asp) | 返回元组，其中的字符串被分为三部分。               |
| [replace()](https://www.w3school.com.cn/python/ref_string_replace.asp) | 返回字符串，其中指定的值被替换为指定的值。         |
| [rfind()](https://www.w3school.com.cn/python/ref_string_rfind.asp) | 在字符串中搜索指定的值，并返回它被找到的最后位置。 |
| [rindex()](https://www.w3school.com.cn/python/ref_string_rindex.asp) | 在字符串中搜索指定的值，并返回它被找到的最后位置。 |
| [rjust()](https://www.w3school.com.cn/python/ref_string_rjust.asp) | 返回字符串的右对齐版本。                           |
| [rpartition()](https://www.w3school.com.cn/python/ref_string_rpartition.asp) | 返回元组，其中字符串分为三部分。                   |
| [rsplit()](https://www.w3school.com.cn/python/ref_string_rsplit.asp) | 在指定的分隔符处拆分字符串，并返回列表。           |
| [rstrip()](https://www.w3school.com.cn/python/ref_string_rstrip.asp) | 返回字符串的右边修剪版本。                         |
| [split()](https://www.w3school.com.cn/python/ref_string_split.asp) | 在指定的分隔符处拆分字符串，并返回列表。           |
| [splitlines()](https://www.w3school.com.cn/python/ref_string_splitlines.asp) | 在换行符处拆分字符串并返回列表。                   |
| [startswith()](https://www.w3school.com.cn/python/ref_string_startswith.asp) | 如果以指定值开头的字符串，则返回 true。            |
| [strip()](https://www.w3school.com.cn/python/ref_string_strip.asp) | 返回字符串的剪裁版本。                             |
| [swapcase()](https://www.w3school.com.cn/python/ref_string_swapcase.asp) | 切换大小写，小写成为大写，反之亦然。               |
| [title()](https://www.w3school.com.cn/python/ref_string_title.asp) | 把每个单词的首字符转换为大写。                     |
| translate()                                                  | 返回被转换的字符串。                               |
| [upper()](https://www.w3school.com.cn/python/ref_string_upper.asp) | 把字符串转换为大写。                               |
| [zfill()](https://www.w3school.com.cn/python/ref_string_zfill.asp) | 在字符串的开头填充指定数量的 0 值。                |

**注释：**所有字符串方法都返回新值。它们不会更改原始字符串。

## 布尔型

### 1.布尔值

- 布尔值表示以下两个值之一：Ture或False。

- 在编程中，您通常需要知道表达式是 True 还是 False。
- 您可以计算 Python 中的任何表达式，并获得两个答案之一，即 True 或 False。
- 比较两个值时，将对表达式求值，Python 返回布尔值答案：

~~~python
#代码
print(10>9)
print(10<9)
#结果
True
False
~~~

- 在if语句中运行条件时，Python返回Tue或False

~~~python
#代码
a = 200
b = 33
if b > a:
    print('b is greater than a')
else:
    print('b is not greater than a')
#结果
b is not greater than a
~~~

### 2.评估值和变量

bool()函数允许您评估任何值，并返回Ture或False

~~~python
#代码
x = '3'
print(bool('hello'))
print(bool(x))
#结果
True
True
~~~

### 3.大多数值是true

- 如果它有某种内容，几乎任何值都会被评估为True。
- 任何字符串都是Ture，除了空字符串。
- 任何数字都是真，除了0。
- 任何列表、元组、集合和字典都是Tue，除了空的。

~~~python
#代码
bool('abc')
bool(123)
bool(['apple','cherry','banana'])
#结果
True
True
True
~~~

### 4.有些值是False

- 实际上，除了空值（例如()、[]、{}、""、''数字0和值None)之外，计算结果为False的值并不多。当然，值False的计算结果为False。

~~~python
#代码
bool(False)
bool(None)
bool(0)
bool('')
bool("")
bool({})
bool([])
bool(())
#结果
False
False
False
False
False
False
False
False
~~~

- 在这种情况下，还有一个值或对象的计算结果为False,也就是说，如果您有一个由具有Ien函数且返回0或False的类构成的对象

~~~python
#代码
class myclass():
    def __len__(self):
        return 0
myobj = myclass()
print(bool(myobj))
#结果
False
~~~

### 5.函数可以返回布尔值

- 您可以创建返回布尔值的函数。

~~~python
#代码
def myFunction():
    return True
print(myFunction())
#结果
True
~~~

- 您可以根据函数的布尔值来执行代码。

~~~python
#代码
def myFunction():
    return True
if myFunction():
    print('YES!')
else:
    print('NO!')
#结果
YES!
~~~

- Python也有许多返回布尔值的内置函数，例如isinstance()函数，可用于确定对象是否属于某种数据类型。

~~~python
#代码
x = 200
print(isinstance(x,int))
#结果
True
~~~

## 操作符

- 运算符用于对变量和值执行操作。
- Python将运算符分为以下几组：算术运算符、赋值运算符、比较运算符、逻辑运算符、身份运算符、成员运算符、按位运算符。

### 1.Python算术运算符

算术运算符与数值一起使用以执行常见的数学运算。

| 运算符 |       名称       |  实例  |
| :----: | :--------------: | :----: |
|   +    |        加        | x + y  |
|   -    |        减        | x - y  |
|   *    |        乘        | x * y  |
|   /    |        除        | x / y  |
|   %    |       取模       | x % y  |
|   **   |        幂        | x ** y |
|   //   | 地板除（取整除） | x // y |

~~~python
#代码
print(3+4)  # 加法
print(5-2)  # 减法
print(2*5)  # 乘法
print(5/2)  # 除法
print(5%2)  # 取余
print(5**2) # 乘方
print(5//2) # 整除
#结果
7
3
10
2.5
1
25
2
~~~

###2.Python赋值运算符

赋值运算符用于为变量赋值。

| 运算符 |  实例   |   等同于   |
| :----: | :-----: | :--------: |
|   =    |  x = 5  |   x = 5    |
|   +=   | x += 3  | x = x + 3  |
|   -=   | x -= 3  | x = x - 3  |
|   *=   | x *= 3  | x = x * 3  |
|   /=   | x /= 3  | x = x / 3  |
|   %=   | x %= 3  | x = x % 3  |
|  //=   | x //= 3 | x = x // 3 |
|  **=   | x **= 3 | x = x ** 3 |
|   &=   | x &= 3  | x = x & 3  |
|  \|=   | x \|= 3 | x = x \| 3 |
|   ^=   | x ^= 3  | x = x ^ 3  |
|  >>=   | x >>= 3 | x = x >> 3 |
|  <<=   | x <<= 3 | x = x << 3 |
### 3.Python比较运算符

比较运算符用于比较两个值。

| 运算符 |    名称    |  实例  |
| :----: | :--------: | :----: |
|   ==   |    等于    | x == y |
|   !=   |   不等于   | x != y |
|   >    |    大于    | x > y  |
|   <    |    小于    | x < y  |
|   >=   | 大于或等于 | x >= y |
|   <=   | 小于或等于 | x <= y |

~~~python
#代码
print(3==5)
print(3!=5)
print(3>5)
print(3<5)
print(3>=5)
print(3<=5)
#结果
False
True
False
True
False
True
~~~

### 4.Python逻辑运算符

逻辑运算符用于组合条件语句。

| 运算符 |                  描述                   |         实例          |
| :----: | :-------------------------------------: | :-------------------: |
|  and   |    如果两个语句都为真，则返回 True。    |   x > 3 and x < 10    |
|   or   |   如果其中一个语句为真，则返回 True。   |    x > 3 or x < 4     |
|  not   | 反转结果，如果结果为 true，则返回 False | not(x > 3 and x < 10) |

~~~python
#代码
print(3<5 and 3<10)
print(3<5 or 3<1)
print(not(3<5))
#结果
True
True
False
~~~

### 5.Python身份运算符

身份运算符用于比较对象，不是比较它们是否相等，但如果它们实际上是同一个对象，则具有相同的内存位置。

| 运算符 |                   描述                    |    实例    |
| :----: | :---------------------------------------: | :--------: |
|   is   |  如果两个变量是同一个对象，则返回 true。  |   x is y   |
| is not | 如果两个变量不是同一个对象，则返回 true。 | x is not y |

~~~python
#代码
x = y = 'qwer'
print(x is y)
print(x is not y)
#结果
True
False
~~~

### 6.Python成员运算符

成员资格运算符用于测试序列是否在对象中出现。

| 运算符 |                      描述                       |    实例    |
| :----: | :---------------------------------------------: | :--------: |
|   in   |  如果对象中存在具有指定值的序列，则返回 True。  |   x in y   |
| not in | 如果对象中不存在具有指定值的序列，则返回 True。 | x not in y |

~~~python
#代码
x = 1
y = [1,2,3]
print(x in y)
print(x not in y)
#结果
True
False
~~~

###7.Python按位运算符

位运算符用于比较（二进制）数字。

| 运算符 |         描述         |                           实例                           |
| :----: | :------------------: | :------------------------------------------------------: |
|   &    |         AND          |           如果两个位均为 1，则将每个位设为 1。           |
|   \|   |          OR          |         如果两位中的一位为 1，则将每个位设为 1。         |
|   ^    |         XOR          |       如果两个位中只有一位为 1，则将每个位设为 1。       |
|   ~    |         NOT          |                       反转所有位。                       |
|   <<   | Zero fill left shift |       通过从右侧推入零来向左移动，推掉最左边的位。       |
|   >>   |  Signed right shift  | 通过从左侧推入最左边的位的副本向右移动，推掉最右边的位。 |

~~~python
#代码
# a = 10 = 1010
# b =  4 = 0100
a = 10
b = 4
print('a & b =', a & b)
print('a | b =', a | b)
print('~a =', ~a)
print('a ^ b =', a ^ b)
#结果
a & b = 0
a | b = 14
~a = -11
a ^ b = 14

#代码
# a =   5 = 0000 0101
# b = -10 = 1111 0110
a = 5
b = -10
print(' a >> 1 =', a >> 1)  # 0000 0010
print(' a >> 2 =', a >> 2)  # 0000 0001
print(' b >> 1 =', b >> 1)  # 1111 1011
print(' b >> 2 =', b >> 2)  # 1111 1101
print(' a << 1 =', a << 1)  # 0000 1010
print(' a >> 1 =', a >> 1)  # 1110 1100
#结果
 a >> 1 = 2
 a >> 2 = 1
 b >> 1 = -5
 b >> 2 = -3
 a << 1 = 10
 a >> 1 = 2
~~~

## 列表——list

### 1.Python列表

#### 1.列表

- 列表用于在单个变量中存储多个项目。
- 列表是Python中用于存储数据集合的4种内置数据类型之一，其他3种是元组Tuple、集合Set和字典Dictionary，它们具有不同的性质和用法。
- 列表是使用方括号创建的。

```python
#代码
thislist = ['apple', 'banana', 'cherry']
print(thislist)
#结果
['apple', 'banana', 'cherry']
```

#### 2.构造函数list()

- 创建新列表时也可以使用list()构造函数。

```python
#代码
thislist = list(('apple', 'banana', 'cherry'))
print(thislist)
#结果
['apple', 'banana', 'cherry']
```

#### 3.列表项

- 列表项是有序的、可变的，并允许重复值。
- 列表项已编入索引，第一个项的索引为[0]，第二个项的索引为[1)，以此类推。

##### 1.有序的

- 当我们说列表是有序的时，这意味着项目具有定义的顺序，并且该顺序不会改变。
- 如果向列表中添加新项目，则新项目将放置在列表的末尾。

##### 2.可变的

- 列表是可变的，这意味着我们可以在创建列表后更改、添加和删除列表中的项目。

##### 3.允许重复

- 由于列表已编入索引，因此列表可以包含具有相同值的项目。

```python
#代码
thislist = ['apple', 'banana', 'cherry', 'apple', 'cherry']
print(thislist)
#结果
['apple', 'banana', 'cherry', 'apple', 'cherry']
```

#### 4.列表项-数据类型

```python
#代码
list1 = ['apple', 'banana', 'cherry']
list2 = [1, 3, 5, 7, 9]
list3 = [True, True, False]
list4 = ['abc', 34, True, 40, 'male']
print(list1 + list2 + list3 + list4)
#结果
['apple', 'banana', 'cherry', 1, 3, 5, 7, 9, True, True, False, 'abc', 34, True, 40, 'male']
```

####5.列表长度

- 要确定列表有多少项，请便用len()函数。

```python
#代码
thislist = ['apple', 'banana', 'cherry', 'apple', 'cherry']
print(len(thislist))
#结果
5
```

### 2.访问项目

- 列表项已编入索引，可以通过引用索引号来访问它们。

```python
#代码
thislist = ['apple', 'banana', 'cherry']
print(thislist[1])
#结果
banana
```

#### 1.负索引意味着从尾开始

- -1指最后一项，2指倒数第二项，以此类推。

```python
#代码
thislist = ['apple', 'banana', 'cherry']
print(thislist[-1])
#结果
cherry
```

#### 2.索引范围

- 您可以通过指定范围的开始和练束位置来指定索范围。
- 指定范围时，返回值将是具有指定项目的新列表。

```python
#代码
thislist = ['apple', 'banana', 'cherry', 'orange', 'kiwi', 'melon', 'mango']
print(thislist[2:5])
#结果
['cherry', 'orange', 'kiwi']

#代码
thislist = ['apple', 'banana', 'cherry', 'orange', 'kiwi', 'melon', 'mango']
print(thislist[:4])
#结果
['apple', 'banana', 'cherry', 'orange']

#代码
thislist = ['apple', 'banana', 'cherry', 'orange', 'kiwi', 'melon', 'mango']
print(thislist[2:])
#结果
['cherry', 'orange', 'kiwi', 'melon', 'mango']
```

####3.负索引范围

- 如果要从列表末尾开始搜索，请指定负索引。

```python
#代码
thislist = ['apple', 'banana', 'cherry', 'orange', 'kiwi', 'mango']
print(thislist[-4:-1])
#结果
['orange', 'kiwi', 'melon']
```

####4.检查项目是否存在

- 要确定列表中是否存在指定的项目，请使用in关键字。

```python
#代码
thislist = ['apple', 'banana', 'cherry']
if 'apple' in thislist:
    print("Yes, 'apple' is in the fruits list")
#结果
Yes, 'apple' is in the fruits list
```

### 3.更改项目值

- 要更改特定项目的值，请参阅察引号。

```python
#代码
thislist = ['apple', 'banana', 'cherry']
thislist[1] = 'blackcurrant'
print(thislist)
#结果
['apple', 'blackcurrant', 'cherry']
```

#### 1.更改特定范围内项目的值

- 要更改特定范围内项目的值，请定义一个包含新值的列表，并参考要插入新值的索引号范围。

```python
#代码
thislist = ['apple', 'banana', 'cherry', 'orange', 'kiwi', 'mango']
thislist[1:3] = ['blackcurrant', 'watermelon']
print(thislist)
#结果
'''
[1:3]：thislist[1]、thislist[2]被新的内容替代
[1:2]：只有thinlist[1]被新内容替代
[1:1]：没有内容会被替换，仅插入新内容
''' 
['apple', 'blackcurrant', 'watermelon', 'orange', 'kiwi', 'mango']
```

- 如果插入的项目多于替换的项目，新项目将插入您指定的位置，其余项目将相应移动。

```python
#代码
thislist = ['apple', 'banana', 'cherry']
thislist[1:2] = ['blackcurrant', 'watermelon']
print(thislist)
#结果:只有thinlist[1]被新内容替代
['apple', 'blackcurrant', 'watermelon', 'cherry']
```

- 如果您插入的项目少于替换的项目，新项目将插入您指定的位置，其余项目将相应移动。

```python
#代码
thislist = ['apple', 'banana', 'cherry']
thislist[1:3] = ['watermelon']
print(thislist)
#结果:thislist[1]、thislist[2]被新的内容替代
['apple', 'watermelon']
```

#### 2.插入项目

- 要插入新的列表项，而不替换任何现有值，我们可以使用insert()方法。
- insert())方法在指定的索引处插入一个项目。

```python
#代码
thislist = ['apple', 'banana', 'cherry']
thislist.insert(2,'watermelon')
print(thislist)
#结果：插入一个值，使其成为a[n]处的值，原来的a[n]向后移动成为a[n+1],该方法只能插入一个值
['apple', 'banana', 'watermelon', 'cherry']
```

#### 3.追加项目

- 要将项目添加到列表的末尾，请使用append()方法。

```python
#代码
thislist = ['apple', 'banana', 'cherry']
thislist.append('watermelon')
print(thislist)
#结果：该方法只能追加一个值
['apple', 'banana', 'cherry', 'watermelon']
```

#### 4.扩展列表

- 要将另一个列表中的元素附加到当前列表，请使用extend()方法。

```python
#代码
list1 = ['apple', 'banana', 'cherry']
list2 = ['mango', 'pineapple', 'papaya']
list1.extend(list2)
print(list1)
#结果
['apple', 'banana', 'cherry', 'mango', 'pineapple', 'papaya']
```

- extend()方法不必附加列表，您可以添加任何可迭代对象（元组、集合、字典等）。

```python
#代码
list1 = ['apple', 'banana', 'cherry']
list2 = ('kiwi', 'orange')
list1.extend(list2)
print(list1)
#结果:其中list2是集合
['apple', 'banana', 'cherry', 'kiwi', 'orange']
```

####5.删除指定项目

- remove()删除指定的项目。

```python
#代码
thislist = ['apple', 'banana', 'cherry']
thislist.remove('banana')
print(thislist)
#结果：该方法只能删除一个值
['apple', 'cherry']
```

#### 6.删除指定索引

- pop()方法删除指定索引。

```py
#代码
thislist = ['apple', 'banana', 'cherry']
thislist.pop(1)
print(thislist)
#结果
['apple', 'cherry']

#代码
thislist = ['apple', 'banana', 'cherry']
thislist.pop()
print(thislist)
#结果:如果不指定索引，pop()方法将删除最后一项
['apple', 'banana']
```

- del关键字也可以删除指定的索引。

```python
#代码
thislist = ['apple', 'banana', 'cherry']
del thislist[1]
print(thislist)
#结果
['apple', 'cherry']

#代码
thislist = ['apple', 'banana', 'cherry']
del thislist
#结果:del关键字可以删除整个list

```

####7.清空列表

- clear()方法清空列表。
- 不同于del删除整个列表，该列表仍然存在，但没有内容。

```python
#代码
thislist = ['apple', 'banana', 'cherry']
thislist.clear()
print(thislist)
#结果
[]
```

### 4.循环遍历列表

- 可以使用for循环遍历列表项

```python
#代码
thislist = ['apple', 'banana', 'cherry']
for x in thislist:
    print(x)
#结果
apple
banana
cherry
```

####1.遍历索引号

- 您还可以通过引用它们的索引号来循环遍历列表项。
- 便用range()和len()函数创建合适的可迭代对象。

```python
#代码
thislist = ['apple', 'banana', 'cherry']
count = range(len(thislist))
print(count)
for i in count:
    print(thislist[i])
#结果
range(0, 3)
apple
banana
cherry
```

####2.使用While循环

- 您可以使用while循环遍历列表项。
- 使用len()函数来确定列表的长度，然后从0开始并通过引用它们的索引来循环遍历列表项。
- 请记住在每次迭代后将索引增加1。

```python
#代码
thislist = ['apple', 'banana', 'cherry']
i = 0
while i < len(thislist):
    print(thislist[i])
    i = i + 1
#结果
apple
banana
cherry    
```

### 5.List Comprehension

####1.List Comprehension的作用

- 当您想要基于现有列表的值创建新列表时，List Comprehension提供了更短的语法。
- 例子：
  根据水果列表，您需要一个新列表，其中仅包含名称中带有字母'a'"的水果。
  如果没有List Comprehension，您将不得不编写一个带有条件测试的for语句。

```python
#代码
fruits = ['apple', 'banana', 'cherry', 'kiwi', 'mango']
newlist = []
for x in fruits:
    if 'a' in x:
        newlist.append(x)
print(newlist)
#结果
['apple', 'banana', 'mango']
```

####2.语法

- `newlist = [expression for item in iterable == True]`
- 返回值是一个新列表，旧列表保持不变。

```python
#代码
fruits = ['apple', 'banana', 'cherry', 'kiwi', 'mango']
newlist = [x.lower() for x in fruits if 'a' in x]
print(newlist)
#结果
['apple', 'banana', 'mango']
```

###6.排序列表

- 默认情况下，列表对象有一个sort()方法，该方法将按字母数字、升序对列表进行排序。

```python
#代码
thislist = ['banana', 'kiwi', 'orange', 'mango', 'cherry', 'apple']
thislist.sort()
print(thislist)
#结果
['apple', 'banana', 'cherry', 'kiwi', 'mango', 'orange']

#代码
thislist = [89, 894, 34, 1, 122, 12, 2]
thislist.sort()
print(thislist)
#结果:数字、字母不能混合在一起排序
[1, 2, 12, 34, 89, 122, 894]

#代码
thislist = ['banana', 'kiwi', 'Orange', 'Mango', 'cherry', 'Apple']
thislist.sort()
print(thislist)
#结果:默认情况下，sort()区分大小写，导致所有大写字母都排在小写字母前面
['Apple', 'Mango', 'Orange', 'banana', 'cherry', 'kiwi']

#代码
thislist = ['banana', 'kiwi', 'orange', 'mango', 'cherry', 'apple']
thislist.sort(reverse = True)
print(thislist)
#结果:降序排列
['orange', 'mango', 'kiwi', 'cherry', 'banana', 'apple']
```

#### 1.自定义排序函数

- 您还可以使用关键字参数key = function自定义您自己的函数。
- 该函数将返回一个用于对列表进行排序的数字（最靠近50的的数字在前）。

```python
#代码
def myfunc(n):
    return abs(n - 50)
thislist = [100, 2, 34, 89, 23, 50]
thislist.sort(key=myfunc)
print(thislist)
#结果
[50, 34, 23, 89, 2, 100]
```

#### 2.相反的顺序

- 如果您想颠倒列表的顺序，而不考虑字母表怎么办？
- reverse()方法反转元素的当前排序顺序。

```python
#代码
thislist = ['apple', 'banana', 'cherry', 'kiwi', 'orange']
thislist.reverse()
print(thislist)
#结果
['orange', 'kiwi', 'cherry', 'banana', 'apple']
```

### 7.复制列表

- 不能简单地通过键入Iist2=list1来复制列表，因为list2将只是对1ist1的引用，并且在Iist1中所做的更改也会自动在1ist2中进行。
- 有多种方法可以进行复制，一种方法是使用内置的List方法copy()。另一种方法是使用内置方法Iist()。

```python
#代码
list1 = ['apple', 'banana', 'cherry']
list2 = list1.copy()
print(list2)
#结果
['apple', 'banana', 'cherry']

#代码
list1 = ['apple', 'banana', 'cherry']
list2 = list(list1)
print(list2)
#结果
['apple', 'banana', 'cherry']
```

###8.连接两个列表

- 在Python中有多种方法可以连接或连接两个或多个列表。

```python
#代码
list1 = ['a', 'b', 'c']
list2 = [1, 2, 3]
list3 = list1 + list2
print(list3)
#结果
['a', 'b', 'c', 1, 2, 3]

#代码
list1 = ['a', 'b', 'c']
list2 = [1, 2, 3]
for x in list2:
    list1.append(x)
print(list1)
#结果
['a', 'b', 'c', 1, 2, 3]

#代码
list1 = ['a', 'b', 'c']
list2 = [1, 2, 3]
list1.extend(list2)
print(list1)
#结果
['a', 'b', 'c', 1, 2, 3]
```

## 元组——tuple

### 1.元组

- 元组用于在单个变量中存储多个项目。
- Tuple是Python中用于存储数据集合的4种内置数据类型之一，另外3种是List、Set和Dictionary,它们都有不同的性质和用法。
- 元组是有序且不可更改的集合。
- 元组是用圆括号写的。

#### 1.元组项目

- 元组项是有序的、不可更改的，并允许重复值。
- 元组项目被索引，第一个项目有索引[0]，第二个项目有索引[1]等等。

> 有序的
>
> - 当我们说元组是有序的时，这意味着项目具有定义的顺序，并且该顺序不会改变。
>
> 不可改变的
>
> - 元组是不可更改的，这意味着我们不能在元组创建后更改、添加或删除项目。
>
> 允许重复
>
> - 由于元组被索引，它们可以具有相同值的项目。

```python
#代码
thistuple = ('apple', 'banana', 'cherry', 'apple')
print(thistuple)
#结果
('apple', 'banana', 'cherry', 'apple')
```

#### 2.元组长度

要确定元组有多少项，请使用len()函数.

```python
#代码
thistuple = ('apple', 'banana', 'cherry', 'apple')
print(len(thistuple))
#结果
4
```

#### 3.使用一项创建元组

- 要创建只有一项的元组，必须在该项后添加一个逗号，否则Python不会将其识别为元组。

```python
#代码
thistuple = ('apple',)
print(type(thistuple))
thistuple = ('apple')
print(type(thistuple))
#结果
<class 'tuple'>
<class 'str'>
```

#### 4.元组项-数据类型

- 元组项可以是任何数据类型

```python
#代码
tuple1 = ('apple', 'banana', 'cherry')
tuple2 = (1, 2, 3, 4, 5)
tuple3 = (True, False, True)
tuple4 = ('abc', 23, True, "male")
print(tuple1 + tuple2 + tuple3 + tuple4)
#结果
('apple', 'banana', 'cherry', 1, 2, 3, 4, 5, True, False, True, 'abc', 23, True, 'male')
```

####5.tuple()构造函数

- 也可以使用tuple()构造函数来创建元组。

```python
#代码
thistuple = tuple(('apple', 'banana', 'cherry'))
print(thistuple)
#结果
('apple', 'banana', 'cherry')
```

### 2.访问元组项目

- 通过引用方括号内的索引号来访问元组项

```python
#代码
thistuple = tuple(('apple', 'banana', 'cherry'))
print(thistuple[1])
#结果
banana
```

#### 1.负索引

- 负系引意味着从尾开始。
- -1指最后一项，-2指倒数第二项，以此类推。

```python
#代码
thistuple = tuple(('apple', 'banana', 'cherry'))
print(thistuple[-1])
#结果
cherry
```

#### 2.索引范围

- 您可以通过指定范围的开始和结束位置来指定索引范围。
- 指定范围时，返回值将是具有指定项的新元组。

```python
#代码
thistuple = tuple(('apple', 'banana', 'cherry', 'orange', 'kiwi', 'melon', 'mango'))
print(thistuple[2:5])
#结果
('cherry', 'orange', 'kiwi')

#代码
thistuple = tuple(('apple', 'banana', 'cherry', 'orange', 'kiwi', 'melon', 'mango'))
print(thistuple[:4])
#结果:通过省略起始值，范围将从第一项开始
('apple', 'banana', 'cherry', 'orange')

#代码
thistuple = tuple(('apple', 'banana', 'cherry', 'orange', 'kiwi', 'melon', 'mango'))
print(thistuple[2:])
#结果:通过省略结束值，范围将继续到元组的末尾
('cherry', 'orange', 'kiwi', 'melon', 'mango')
```

#### 3.负索引范围

- 如果要从元组末尾开始搜索，请指定负索引。

```python
#代码
thistuple = tuple(('apple', 'banana', 'cherry', 'orange', 'kiwi', 'melon', 'mango'))
print(thistuple[-4:-1])
#结果
('orange', 'kiwi', 'melon')
```

#### 4.检查项目是否存在

- 要确定元组中是否存在指定的项目，请使用in关键字。

```python
#代码
thistuple = ('apple', 'banana', 'cherry')
if 'apple' in thistuple:
    print("Yes, 'apple' is in the fruits tuple")
#结果
Yes, 'apple' is in the fruits tuple
```

### 3.更新元组

- 元组是不可更改的，这意味着一旦创建了元组，您就无法更改、添加或删除项目。
- 但是有一些解决方法。

#### 1.更改元组值

- 一旦创建了元组，就不能更改其值。元组是不可更改的，或不可变的。
- 但是有一个解决方法。将元组转换为列表，更改列表，然后将列表转换回元组。

```python
#代码
x = ('apple', 'banana', 'cherry')
y = list(x)
y[1] = 'kiwi'
x = tuple(y)
print(x)
#结果
('apple', 'kiwi', 'cherry')
```

#### 2.添加项目

- 由于元组是不可变的，它们没有内置的append()方法，但还有其他方法可以向元组添加项。

```python
#代码
x = ('apple', 'banana', 'cherry')
y = list(x)
y.append('orange')
x = tuple(y)
print(x)
#结果:转换为列表，就像更改元组的解决方法一样，将其转换为列表，添加您的项目，然后将其转换回元组
('apple', 'banana', 'cherry', 'orange')

#代码
x = ('apple', 'banana', 'cherry')
y = ('orange',)
x += y
print(x)
#结果:将元组添加到元组。向元组添加元组，因此如果你想添加一个（或多个）项目，请使用该项目创建一个新元组，并将其添加到现有的元组中
('apple', 'banana', 'cherry', 'orange')
```

####3.删除项目

- 元组是不可更改的，因此不能从中删除项目，但可以使用与我们用于更改和添加元组项目相同的解决方法。

```python
#代码
x = ('apple', 'banana', 'cherry')
y = list(x)
y.remove('apple')
x = tuple(y)
print(x)
#结果
('banana', 'cherry')

#代码
x = ('apple', 'banana', 'cherry')
del x
#结果

```

### 4.解包元组

#### 1.如何解包元组

- 当我们创建一个元组时，我们通常会为其分配值。这称为打包元组。
- 但是，在Python中，我们也可以将值提取回变量中。这称为解包。

```python
#代码
fruits = ('apple', 'banana', 'cherry')
(green, yellow, red) = fruits
print(green)
print(yellow)
print(red)
#结果
apple
banana
cherry
```

#### 2.使用星号*

- 如果变量的数量少于值的数量，您可以在变量名后添加*，这些值将作为列表分配给变量。

```python
#代码
fruits = ('apple', 'banana', 'cherry', 'orange', 'kiwi', 'melon')
(green, yellow, *red) = fruits
print(green)
print(yellow)
print(red)
#结果
apple
banana
['cherry', 'orange', 'kiwi', 'melon']

#代码
fruits = ('apple', 'banana', 'cherry', 'orange', 'kiwi', 'melon')
(green, *tropic, red) = fruits
print(green)
print(tropic)
print(red)
#结果:如果*被添加到另一个变量名而不是最后一个，Python将为变量赋值，直到剩余的值数量与剩余的变量数匹配
apple
['banana', 'cherry', 'orange', 'kiwi']
melon
```

### 5.遍历元组

- 可以使用for循环遍历元组项。

```python
#代码
thistuple = ('apple', 'banana', 'cherry')
for x in thistuple:
    print(x)
#结果
apple
banana
cherry
```

####1.遍历索引号

- 还可以通过引用它们的索引号来循环遍历元组项。
- 使用range()和len()函数创建合适的可迭代对象。

```python
#代码
thistuple = ('apple', 'banana', 'cherry')
for i in range(len(thistuple)):
    print(thistuple[i])
#结果
apple
banana
cherry
```

####2.使用While循环

- 可以便用while循环遍历列表项。
- 使用len()函数来确定元组的长度，然后从0开始并通过引用它们的索引来循环遍历元组项。
- 请记住在每次迭代后将索引增加1。

```python
#代码
thistuple = ('apple', 'banana', 'cherry')
i = 0
while i < len(thistuple):
    print(thistuple[i])
    i = i + 1
#结果
apple
banana
cherry
```

###6.元组连接

#### 1.连接两个元组

- 要连接两个或多个元组，可以使用+运算符。

```python
#代码
tuple1 = ('a', 'b', 'c')
tuple2 = (1, 2, 3)
tuple3 = tuple1 + tuple2
print(tuple3)
#结果
('a', 'b', 'c', 1, 2, 3)
```

####2.元组乘法

- 如果要将元组的内容乘以给定次数，可以便用*运算符。

```python
#代码
fruits = ('apple', 'banana', 'cherry')
mytuple = fruits * 2
print(mytuple)
#结果
('apple', 'banana', 'cherry', 'apple', 'banana', 'cherry')
```

## 集合——Set

- 集合用于在单个变量中存储多个项目。
- Set是Python中用于存储数据集合的4种内置数据类型之一，另外3种是List、Tuple和Dictionary,它们的性质和用法各不相同。
- 集合是无序和无索引的集合。
- 集合是用大括号写的。

```python
#代码
thisset = {'apple', 'banana', 'cherry'}
print(thisset)
#结果
{'banana', 'apple', 'cherry'}
```

### 1.Set

#### 1.项目集合

- 设置项是无序的、不可更改的，并且不允许重复值。

>无序
>
>- 无序意味着集合中的项目没有定义的顺序。
>- 每次使用时，集合项可以以不同的顺序出现，并且不能通过索引或键引用。
>
>不可改变的
>
>- 集合是不可更改的，这意味着我们无法在创建集合后更改项目。
>- 创建集合后，您无法更改其项目，但可以添加新项目。
>
>不允许重复
>
>- 集合不能有两个具有相同值的项目。

```python
#代码
thisset = {'apple', 'banana', 'cherry', 'apple'}
print(thisset)
#结果
{'cherry', 'apple', 'banana'}
```

####2.获取集合的长度

- 要确定一个集合有多少个项目，请便用Ien()方法。

```python
#代码
thisset = {'apple', 'banana', 'cherry'}
print(len(thisset))
#结果
3
```

#### 3.集合项-数据类型

- 集合项可以是任何数据类型。

```python
#代码
set1 = {'apple', 'banana', 'cherry'}
set2 = {1, 3, 5, 7, 8}
set3 = {True, False, True, True}
set4 = {'abc', 22, True, "wbe"}
#结果

```

####4.set()构造函数

- 也可以使用set()构造函数来创建一个集合。

```python
#代码
thisset = set(('apple', 'banana', 'cherry'))
print(thisset)
#结果
{'banana', 'apple', 'cherry'}
```

### 2.访问项目

- 不能通过引用索引或键来问集合中的项目。
- 但是您可以使用for循环遍历集合项，或者使用in关键字询问集合中是否存在指定的值。

```python
#代码
thisset = {'apple', 'banana', 'cherry'}
for x in thisset:
    print(x)
#结果
cherry
apple
banana

#代码
thisset = {'apple', 'banana', 'cherry'}
print('banana' in thisset)
#结果
True
```

####1.添加项目

- 要将一项添动加到集合中，请使用add()方法。

```python
#代码
set1 = {'apple', 'banana', 'cherry'}
set1.add('orange')
print(set1)
#结果
{'banana', 'apple', 'orange', 'cherry'}
```

#### 2.添加集合

- 要将另一个集合中的项目添加到当前集合中，请使用update()方法。

```python
#代码
set1 = {'apple', 'banana', 'cherry'}
set2 = {1, 2, 3}
set1.update(set2)
print(set1)
#结果
{1, 'banana', 2, 3, 'cherry', 'apple'}
```

#### 3.添加任何可迭代对象

- update()方法中的对象不必是一个集合，它可以是任何可迭代对象（元组、列表、字典等）。

```python
#代码
set1 = {'apple', 'banana', 'cherry'}
set2 = [1, 2, 'six']
set1.update(set2)
print(set1)
#结果
{1, 'cherry', 2, 'banana', 'six', 'apple'}
```

#### 4.更改项目

- 创建集合后，无法更改其项目，但可以添加新项目。

####5.除去项目

- 要删除集合中的项目，请使用remove()或discard()方法，
- 如果要删除的项目不存在，remove()将引发错误。
- 如果要删除的项目不存在，discard()将不会会引发错误。

```python
#代码
set1 = {'apple', 'banana', 'cherry'}
set1.remove('apple')
print(set1)
set1.remove('apple')
#结果
{'banana', 'cherry'}
KeyError: 'apple'

#代码
set1 = {'apple', 'banana', 'cherry'}
set1.discard('apple')
print(set1)
set1.discard('apple')
#结果
{'cherry', 'banana'}
```

- 还可以使用pop()方法删除一个项目，但此方法将删除最后一个项目。清记住，集合是无序的，因此您将不知道删除了哪些项目。
- pop()方法的返回值是移除的项。

```python
#代码
set1 = {'apple', 'banana', 'cherry'}
x = set1.pop()
print(x)
print(set1)
#结果
{'apple', 'cherry'}

#代码
set1 = {'apple', 'banana', 'cherry'}
set1.clear()
print(set1)
#结果
set()

#代码
set1 = {'apple', 'banana', 'cherry'}
del set1
#结果:此时set1已被彻底删除，无法print

```

### 3.循环项目

- 可以使用和for循环遍历设置项。

```python
#代码
thisset = {'apple', 'banana', 'cherry'}
for x  in thisset:
    print(x)
#结果
cherry
apple
banana
```

### 4.连接集合

- 在Python中有几种方法可以连接两个或多个集合。
- 可以使用union()方法返回一个包含两个集合中所有项的新集合，或者使用update()方法将一个集合中的所有项插入到另一个集合中。

```python
#代码
set1 = {'apple', 'banana', 'cherry'}
set2 = {1, 2, 3}
set3 = set1.union(set2)
print(set3)
#结果
{'apple', 1, 2, 'cherry', 3, 'banana'}

#代码
set1 = {'apple', 'banana', 'cherry'}
set2 = {1, 2, 3}
set1.update(set2)
print(set1)
#结果
{1, 'banana', 2, 3, 'cherry', 'apple'}
```

## 字典

- 字典用于在键值对中存储数据值。
- 字典是有序、可变且不允许重复的集合。
- 从Python3.7版开始，字典是有序的。在Python3.6及更早版本中，字典是无序的。
- 字典是用大括号写的，有键和值。

```python
#代码
thisdict = {
    'brand': 'Ford',
    'model': 'Mustang',
    'year': 1964
}
print(thisdict)
#结果
{'branc': 'Ford', '1model': 'Mustang', 'year': 1964}
```

### 1.字典

#### 1.字典项目

- 字典项是有序的、可变的，并且不允许重复。
- 字典项以键值对的形式呈现，可以使用键名进行引用。

>有序还是无序？
>
>- 从Python3.7版开始，字典是有序的。在Python3.6及更早版本中，字典是无序的。
>- 当我们说字典是有序的时，这意味着项目有一个定义的顺序，并且这个顺序不会改变。
>- 无序意味若项目没有定义的顺序，您不能使用索引来引用项目。
>
>可变
>
>- 字典是可变的，这意味着我们可以在字典创建后更改、添加或删除项目。
>
>不允许重复
>
>- 字典不能有两个具有相同键的项目。但可以拥有两个值相同的项目。

```python
#代码
thisdict = {
    'brand': 'Ford',
    'model': 'Mustang',
    'year': 1964
    'year': 2023
}
print(thisdict)
#结果
{'brand': 'Ford', 'model': 'Mustang', 'year': 2023}

#代码
thisdict = {
    'brand': 'Ford',
    'model': 'Mustang',
    'year': 1964,
    'month': 1964
}
print(thisdict)
#结果
{'brand': 'Ford', 'model': 'Mustang', 'year': 1964, 'month': 1964}
```

####2.字典长度

- 要确定字典有多少项，请使用len()函数。

```python
#代码
thisdict = {
    'brand': 'Ford',
    'model': 'Mustang',
    'year': 1964,
    'month': 1964
}
print(len(thisdict))
#结果
4
```

####3.字典项-数据类型

- 字典中的项可以是任何数据类型。

```python
#代码
thisdict = {
    'brand': 'Ford',
    'model': 'Mustang',
    'year': 1964,
    'fruits': {1964, 'red', 'apple'},
    'colors': ['red', 'blue']
}
print(thisdict)
#结果
{'brand': 'Ford', 'model': 'Mustang', 'year': 1964, 'fruits': {'apple', 'red', 1964}, 'colors': ['red', 'blue']}
```

### 2.访问项目

- 可以通过引用方括号内的键名来访问字典的项目。

```python
#代码
thisdict = {
    'brand': 'Ford',
    'model': 'Mustang',
    'year': 1964
}
x = thisdict['model']
y = thisdict.get('model')
print(x)
print(y)
#结果
Mustang
Mustang
```

#### 1.获取key

- keys()方法将返回字典中所有键的列表。

```python
#代码
thisdict = {
    'brand': 'Ford',
    'model': 'Mustang',
    'year': 1964
}
x = thisdict.keys()
print(x)
#结果
dict_keys(['brand', 'model', 'year'])
```

#### 2.获取值

- values()方法将返回字典中所有值的列表。

```python
#代码
thisdict = {
    'brand': 'Ford',
    'model': 'Mustang',
    'fruits': {1964, 'red', 'apple'},
    'colors': ['red', 'blue']
}
x = thisdict.values()
print(x)
#结果
dict_values(['Ford', 'Mustang', {'apple', 'red', 1964}, ['red', 'blue']])
```

#### 3.获取项目

- items()方法将返回字典中的每个项目，作为列表中的元组。

```python
#代码
thisdict = {
    'brand': 'Ford',
    'fruits': [1964, 'red', 'apple'],
    'colors': ('red', 'blue'),
    'ceshi': {('wasd', 'qwer')},
    'model': 'Mustang'
}
x = thisdict.items()
print(x)
#结果
dict_items([('brand', 'Ford'), ('fruits', [1964, 'red', 'apple']), ('colors', ('red', 'blue')), ('ceshi', {('wasd', 'qwer')}), ('model', 'Mustang')])
```

####4.检查key是否存在

- 要确定字典中是否存在指定的键，请使用in关键字。

```python
#代码
thisdict = {
    'brand': 'Ford',
    'model': 'Mustang',
    'year': 1964
}
if 'model' in thisdict:
    print("Yes, 'model' is one of the keys in the thisdict dictionary")
#结果
Yes, 'model' is one of the keys in the thisdict dictionary
```

### 3.更改词典项目

#### 1.更改值

- 可以通过引用其键名来更改特定项目的值

```python
#代码
thisdict = {
    'brand': 'Ford',
    'model': 'Mustang',
    'year': 1964
}
thisdict['year'] = 2023
print(thisdict)
#结果
{'brand': 'Ford', 'model': 'Mustang', 'year': 2023}
```

#### 2.更新字典

- update()方法将使用给定参数中的项目更新字典。
- 参数必须是字典或具有键值对的可迭代对象。

```python
#代码
thisdict = {
    'brand': 'Ford',
    'model': 'Mustang',
    'year': 1964
}
thisdict.update({'year': 2023})
thisdict.update({'1': 111})
print(thisdict)
#结果
{'brand': 'Ford', 'model': 'Mustang', 'year': 2023, '1': 111}
```

### 4.添加字典项目

#### 1.添加项目

- 通过使用新的索引键并为其分配值来将项目添加到字典中。

```python
#代码
thisdict = {
    'brand': 'Ford',
    'model': 'Mustang',
    'year': 1964
}
thisdict['color'] = 1123456
print(thisdict)
#结果
{'brand': 'Ford', 'model': 'Mustang', 'year': 1964, 'color': 1123456}
```

####2.更新字典

- update()方法将使用给定参数中的项目更新字典。如果该项目不存在，则会添加该项目。
- 参数必须是字典或具有键值对的可迭代对象。

```python
#代码
thisdict = {
    'brand': 'Ford',
    'model': 'Mustang',
    'year': 1964
}
thisdict.update({'color': 2023})
print(thisdict)
#结果
{'brand': 'Ford', 'model': 'Mustang', 'year': 1964, 'color': 2023}
```

### 5.删除字典项目

- 有几种方法可以从字典中删除项目。

```python
#代码
thisdict = {
    'brand': 'Ford',
    'model': 'Mustang',
    'year': 1964
}
thisdict.pop('model')
print(thisdict)
#结果：删除指定键值对
{'brand': 'Ford', 'year': 1964}

#代码
thisdict = {
    'brand': 'Ford',
    'model': 'Mustang',
    'year': 1964
}
thisdict.popitem()
print(thisdict)
#结果：删除末尾的键值对
{'brand': 'Ford', 'model': 'Mustang'}

#代码
thisdict = {
    'brand': 'Ford',
    'model': 'Mustang',
    'year': 1964
}
del thisdict['model']
print(thisdict)
#结果：删除指定的键值对
{'brand': 'Ford', 'year': 1964}

#代码
thisdict = {
    'brand': 'Ford',
    'model': 'Mustang',
    'year': 1964
}
thisdict.clear()
print(thisdict)
#结果：删除字典里所有的键值对
{}
```

### 6.循环字典

- 可以使用for循环遍历字典。
- 循环字典时，返回值是字典的键，但也有返回值的方法。

```python
#代码
thisdict = {
    'brand': 'Ford',
    'model': 'Mustang',
    'year': 1964
}
for x in thisdict:
    print(x)
#结果
brand
model
year

#代码
thisdict = {
    'brand': 'Ford',
    'model': 'Mustang',
    'year': 1964
}
for x in thisdict.keys():
    print(x)
#结果
brand
model
year

#代码
thisdict = {
    'brand': 'Ford',
    'model': 'Mustang',
    'year': 1964
}
for x in thisdict:
    print(thisdict[x])
#结果
Ford
Mustang
1964


#代码
thisdict = {
    'brand': 'Ford',
    'model': 'Mustang',
    'year': 1964
}
for x in thisdict.values():
    print(x)
#结果
Ford
Mustang
1964

#代码
thisdict = {
    'brand': 'Ford',
    'model': 'Mustang',
    'year': 1964
}
for x, y in thisdict.items():
    print(x, y)
#结果
brand Ford
model Mustang
year 1964
```

### 7.复制字典

- 不能简单地通过键入dict2=dict1来复制字典，因为：dict2将只是对dict1的引用，并且在dict1申所做的更改也将自动在dict2中进行。
- 有多种方法可以进行复制，一种方法是使用内置的Dictionary方法copy()。另一种方法是使用内置函数dict(),

```python
#代码
dict1 = {
    'brand': 'Ford',
    'model': 'Mustang',
    'year': 1964
}
dict2 = dict1.copy()
print(dict2)
#结果
{'brand': 'Ford', 'model': 'Mustang', 'year': 1964}

#代码
dict1 = {
    'brand': 'Ford',
    'model': 'Mustang',
    'year': 1964
}
dict2 = dict(dict1)
print(dict2)
#结果
{'brand': 'Ford', 'model': 'Mustang', 'year': 1964}
```

###8.嵌套字典

- 字典可以包含字典，这称为嵌套字典。

```python
#代码
myfamily = {
    'child1': {
        'name': 'Emil',
        'year': '2004'
    },
    'child2': {
        'name': 'Tobias',
        'year': '2007'
    },
    'child3': {
        'name': 'Linus',
        'year': '2011'
    }
}
print(myfamily)
#结果
{'child1': {'name': 'Emil', 'year': '2004'}, 'child2': {'name': 'Tobias', 'year': '2007'}, 'child3': {'name': 'Linus', 'year': '2011'}}
```

## 语句

### 1.Python条件语句

#### 1.if

- Python支持数学中常见的逻辑条件：

>等于：`a==b`不等于：`a!=b`
>小于：`a<b`小于或等于：`a<=b`
>大于：`a>b`大于或等于：`a>=b`

- 这些条件可以以多种方式使用，最常见的是在"if语句"和循环中。
- "if"语句"是使用if关键字编写的。

```python
#代码
a = 33
b = 200
if b > a:
    print('b is greater than a')
#结果
b is greater than a
```

#### 2.Elif

- elif关键字是Python的说法，如果前面的条件不成立，那么久试试这个条件。

```python
#代码
a = 33
b = 33
if b > a:
    print('b is greater than a')
elif a == b:
    print('a and b are equal')
#结果
a and b are equal
```

#### 3.Else

- else关键字用于捕获任何未被上述条件捕获的内容。

```python
#代码
a = 200
b = 33
if b > a:
    print('b is greater than a')
elif a == b:
    print('a and b are equal')
else:
    print('a is greater than b')
#结果
a is greater than b
```

#### 4.简写

- 如果你只有一个语句要执行，你可以把他放在同一行

```python
if a > b: print('a is greater than b')
```

```python
#代码
a = 2
b = 330
print('A') if a > b else print('B')
#结果：如果a > b输出A，否则输出B
B

#代码
a = 330
b = 330
print('A') if a > b else print('=') if a==b else print('B')
#结果：如果a > b输出A，否则如果a == b输出=，除此之外此外输出B
=
```

####5.嵌套

- if语句中可以有if语句，这称为嵌套if语句。

```python
#代码
x = 41
if x > 10:
    print('About ten,')
    if x > 20:
        print('and also above 20!')
    else:
        print('but not above 20.')
#结果
About ten,
and also above 20!
```

### 2.Python循环语句

- Python有两个原始循环命令。
  - while循环
  - for循环

#### 1.while循环

- 使用while循环，只要条件为真，我们就可以执行一组语句。

```python
#代码
i = 1
while i < 3:
    print(i)
    i += 1
#结果
1
2
```

#### 2.For循环

- for循环用于迭代序列（即列表、元组、字典、集合或字符串）。
- 这不像其他编程语言中的for关键字，而是更像是其他面向对象编程语言中的迭代器方法，
- 使用for循环，我们可以执行一组语句，对列表、元组、集合等中的每个项目执行一次。

```python
#代码
fruits = ['apple', 'banana', 'cherry']
for x in fruits:
    print(x)
#结果
apple
banana
cherry

#代码
for x in 'banana':
    print(x)
#结果
b
a
n
a
n
a
```

#### 3.中断语句

- 使用break语句，我们可以在循环遍历所有项目之前停止循环。

```python
#代码
fruits = ['apple', 'banana', 'cherry']
for x in fruits:
    print(x)
    if x == 'banana':
        break
#结果
apple
banana

#代码
i = 0
while i < 6:
    i += 1
    print(i)
    if i == 3:
        break
#结果
1
2
3
```

#### 4.continue语句

- 使用continue语句，我么可以停止循环的当前迭代，并继续下一个。

```python
#代码
fruits = ['apple', 'banana', 'cherry']
for x in fruits:
    if x == 'banana':
        continue
    print(x)
#结果
apple
cherry

#代码
i = 0
while i < 6:
    i += 1
    print(i)
    if i == 3:
        continue
    print('aaa')
#结果
1
aaa
2
aaa
3
4
aaa
5
aaa
6
aaa

```

####5.循环中的Else

- 循环中的else关键字指定循环结束时要执行的代码块。



```python
#代码
for x in range(6):
    print(x)
else:
    print('Finally finished!')
#结果
0
1
2
3
4
5
Finally finished!

#代码
i = 1
while i < 6:
    print(i)
    i += 1
else:
    print('i is no longer less than 6')
#结果
1
2
3
4
5
i is no longer less than 6

#代码
for x in range(6):
    if x == 3: break
    print(x)
else:
    print('Finally finished!')

#结果
0
1
2
```

#### 6.range()函数

- 要循环一组代码指定的次数，我们可以使用range()函数。
- range()函数返回一个数字序列，默认情况下从0开始，递增1（默认情况下），并以指定的数字结束。

```python
#代码
for x in range(6):
    print(x)
print('-------------------------')
for x in range(2, 6):
    print(x)
print('-------------------------')
for x in range(2, 30, 3):
    print(x)
#结果
0
1
2
3
4
5
-------------------------
2
3
4
5
-------------------------
2
5
8
11
14
17
20
23
26
2
```

### 3.Try Except

- try块可让您测试代码块的错误。
- except块可让您处理错误。
- finally块允许您执行代码，而不管try-和except块的结果。

#### 1.异常处理

- 当发生错误或异常时，Python通常会停止并生成错误消息。
- 可以使用try语句处理异常。

```python
#代码
try:
    print(z)
except:
    print('An exception occurred')
#结果
An exception occurred

#代码
try:
    print(z)
except NameError:
    print('Variable z is not defined')
except :
    print('Something else went wrong')
#结果
Variable z is not defined

#代码
try:
    print('hello')
except:
    print('Something went wrong')
else:
    print('Nothing went wrong')
#结果：使用else关键字来定义在未引发错误时要执行的代码数
hello
Nothing went wrong

#代码
try:
    print(x)
except:
    print('Something went wrong')
finally:
    print("The 'try except' is finished")
#结果：如果指定了finally块，则无论try块是否引发错误，都将执行
Something went wrong
The 'try except' is finished
```

####2.引发异常

- 作为Python开发人员，您可以选择在条件发生时抛出异常。
- 要抛出（或引发）异常，请使用raise关键字

```python
#代码
x = -1
if x < 0:
    raise Exception('Sorry,no numbers below zero')
#结果
Traceback (most recent call last):
  File "C:\Users\ziqian\Desktop\1\1.py", line 3, in <module>
    raise Exception('Sorry,no numbers below zero')
Exception: Sorry,no numbers below zero

#代码
x = 'hello'
if not type(x) is int:
    raise TypeError('Only integers are allowed')
#结果
Traceback (most recent call last):
  File "C:\Users\ziqian\Desktop\1\1.py", line 3, in <module>
    raise TypeError('Only integers are allowed')
TypeError: Only integers are allowed
```

## 函数

- 函数是一个代码块，它只在被调用时运行。
- 您可以将数据（称为参数）传递给函数。
- 函数可以作为结果返回数据。

### 1.创建函数

- 在Python中，函数是使用def关键字定义的。
```python
#代码
def my_function():  
    print("Hello from a function")
#结果

```

### 2.调用函数

- 要调用函数，请使用函数名称后面跟括号。
```python
#代码
def my_function():  
    print("Hello from a function")  
my_function()
#结果
Hello from a function
```

### 3.参数

- 信息可以作为参数传递给函数。
- 参数在函数后的括号内指定。您可以根据需要添动加任意数量的参数，只需用逗号分隔它们.
- 下面的示例有一个带一个参数(fname)的函数。当函数被调用时，我们传递一个名字，在函数内部使用它来打印全名。
```python
#代码
def my_function(fname):  
    print(fname + ' Refsnes')  
my_function('Emil')  
my_function('Tobias')  
my_function('Linus')
#结果
Emil Refsnes
Tobias Refsnes
Linus Refsnes
```

### 4.Parameters（形参） or Arguments（实参）？

- 术语Parameter和Argument可以用于同一件事：传递给函数的信息。
- 从函数的角度来看：
  - Parameter是函数定义中括号内列出的变量。
  - Argument参数是在调用函数时发送给函数的值。
### 5.参数数量

- 默认情况下，必须使用正确数量的参数调用函数。这意味着如果你的函数需要2个参数，则必须使用2个参数调用该函数，不能多也不能少。
```python
#代码
def my_function(fname, lname):  
    print(fname + ' ' + lname)  
my_function('Emil', 'Refsnes')
#结果
Emil Refsnes
```

### 6.任意参数，*args

- 如果不知道有多少参数将传递到函数中，请在函数定义中的参数名你前添加一个*。
- 这样，该函数将接收一个参数元组，并可以相应地访问这些项目：
```python
#代码
def my_function(*kids):
    print('The youngest child is ' + kids[2])
my_function('Emil', 'Tobias', 'Linus')
#结果
The youngest child is Linus
```

### 7.关键字参数

- 还可以使用key = value语法发送参数。
- 这样，参数的顺序就无关紧要了。
```python
#代码
def my_function(child3, child2, child1):  
    print('The youngest child is ' + child3)  
my_function(child1='Emil', child2='Tobias', child3='Linus')
#结果
The youngest child is Linus
```

### 8.任意关键字参数，**kwargs

- 如果不知道有多少关键字参数将被传递到函数中，请在函数定义中的参数名称之前添加两个星号：**，
- 这样，该数将接收一个参数字典，并可以相应地访问这些项目：
```python
#代码
def my_function(**kid):
    print('The youngest child is ' + kid['lname'])
my_function(fname='Tobias', lname='Refsnes')
#结果
The youngest child is Refsnes
```

### 9.默认参数值

- 以下示例显示如何使用默认参数值。
- 如果我们不带参数调用函数，它使用默认值。
```python
#代码
def my_function(country='Norway'):
    print('I am from ' + country)
my_function('Sweden')
my_function('India')
my_function()
my_function('Brazil')
#结果
I am from Sweden
I am from India
I am from Norway
I am from Brazil
```

### 10.将列表作为参数传递

- 可以向函数发送任何数据类型的参数（字符串、数字、列表、字典等），它会在函数内部被视为相同的数据类型。
- 例如。如果你发送一个List作为参数，当它到达函数时它仍然是一个List。
```python
#代码
def my_function(food):
    for x in food:
        print(x)
fruits = ['appel', 'banana', 'cherry']
my_function(fruits)
#结果
appel
banana
cherry
```

### 11.返回值

- 要让函数返回值，请使用return语句。
```python
#代码
def my_function(x):
    return 5 * x
print(my_function(3))
print(my_function(7))
print(my_function(9))
#结果
15
35
45
```

### 12.pass语句

- 函数定义不能为空，但如果由于某种原因有一个没有内容的函数定义，请放入pass语句以避免出错。
```python
def my_function(x):
    pass 
```

### 13.递归

- Python也接受函数递归，这意味着定义的函数可以调用自身。
- 递归是一个常见的数学和编程慨念。这意味若函数调用自身。这意味着您可以遍历数据以得出结果。
- 开发人员应该非常小心递归，因为很容易编写一个永不终止的函数，或者一个使用过多内存或处理器能力的函数。但是，如果编写正确，递归可
  能是一种非常有效且数学上优雅的编程方法。
- 在这个例子中，tri_recursion()是一个我们定义为调用自身的函数(“recurse")。我们使用k变量作为数据，每次递归都会递减(-1)。当条件不
  大于0时（即当它为0时）递归结束。
```python
#代码
def tri_recursion(k):
    if k > 0:
        result = k + tri_recursion(k - 1)
        print(result)
    else:
        result = 0
    return result
print('\n\nRecursion Example Results')
tri_recursion(3)
#结果
Recursion Example Results
1
3
6
```

## Lamda

- Lambda函数是一个小的匿名函数。
- 一个Lambda函数可以接受任意数量的参数，但只能有一个表达式。

### 1.语法

- Lambda参数：表达式。
- 执行表达式并返回结果。

```python
#代码
x = lambda a: a + 10
print(x(5))
#结果
15

#代码
x = lambda a, b: a * b
print(x(5, 6))
#结果
30

#代码
x = lambda a, b, c: a + b + c
print(x(5, 6, 2))
#结果
13
```

### 2.为什么要使用Lambda函数？

- 当您将它们用作另一个函数中的匿名函数时，可以更好地展示lambda的力量。
- 假设您有一个接受一个参数的函数定义，并且该参数将乘以一个未知数。
```python
#代码
def myfunc(n):
    return lambda a: a * n
mydoubler = myfunc(2)
print(mydoubler(11))
mytripler = myfunc(3)
print(mytripler(11))
#结果
22
33
```

## 类

### 1.Python类/对象

- Python是一种面向对象的编程语言。
- Python中的几乎所有东西都是一个对象，有它的属性和方法。
- 类就像一个对象构适函数，或者是创建对象的"蓝图"。

#### 1.创建一个类

- 要创建一个类，请使用关键字class。

```python
#代码
class MyClass:  
    x = 5  
```

#### 2.创建对象

- 现在我们可以使用名为MyClass的类来创建对象。

```python
#代码
class MyClass:  
    x = 5  
p1 = MyClass()  
print(p1.x)
#结果
5
```

#### 3.init()函数

- 上面的例子是最简单形式的类和对象，在现实生活应用程序中并没有真正有用。
- 要理解类的含义，我们必须了解内置的init()函数。
- 所有类都有一个名为init()的函数，它总是在类被初始化时执行。
- 使用init()函数为对象属性赋值，或在创建对象时需要执行的其他操作。

```python
#代码
class Person:  
    def __init__(self, name, age):  
        self.name = name  
        self.age = age  
p1 = Person('John', 36)  
print(p1.name)  
print(p1.age)
#结果
John
36
```

#### 4.对象方法

- 对象也可以包含方法。对象中的方法是属于该对象的函数。
- 让我们在Person类中创建一个方法。

```python
#代码
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age
    def myfunc(self):
        print('Hello my name is ' + self.name)
p1 = Person('John', 36)
p1.myfunc()
#结果
Hello my name is John
```

#### 5.self参数

- self参数是对类当前实例的引用，用于访问属于该类的变量。
- 它不必命名为self，您可以随意调用它，但它必须是类中任何函数的第一个参数。

```python
#代码
class Person:  
    def __init__(mysillyobject, name, age):  
        mysillyobject.name = name  
        mysillyobject.age = age  
    def myfunc(abc):  
        print('Hello my name is ' + abc.name)  
p1 = Person('John', 36)  
p1.myfunc()
#结果
Hello my name is John
```

#### 6.修改对象属性

- 可以像这样修改对象的属性。

```python
#代码
class Person:  
    def __init__(mysillyobject, name, age):  
        mysillyobject.name = name  
        mysillyobject.age = age  
    def myfunc(abc):  
        print('Hello my name is ' + abc.name)  
p1 = Person('John', 36)  
p1.age = 19  
print(p1.age)
```

#### 7.删除对象属性

- 使用del关键字删除对象的属性。

```python
#代码
class Person:  
    def __init__(mysillyobject, name, age):  
        mysillyobject.name = name  
        mysillyobject.age = age  
    def myfunc(abc):  
        print('Hello my name is ' + abc.name)  
p1 = Person('John', 36)  
del p1.age  
print(p1.age)
```

#### 8.删除对象

- 使用del关键字删除对象。

```python
#代码
class Person:  
    def __init__(mysillyobject, name, age):  
        mysillyobject.name = name  
        mysillyobject.age = age  
  
    def myfunc(abc):  
        print('Hello my name is ' + abc.name)  
  
  
p1 = Person('John', 36)  
del p1  
print(p1)
#结果
NameError: name 'p1' is not defined
```

### 2.Python继承

- 继承允许我们定义一个从另一个类继承所有方法和属性的类。
- 父类是被继承的类，也称为基类。
- 子类是从另一个类继承的类，也称为派生类。

#### 1.创建父类

- 任何类都是父类，因此语法与创建任何其他类相同。

```python
#代码
class Person:
    def __init__(self, fname, lname):
        self.firstname = fname
        self.lastname = lname

    def pritname(self):
        print(self.firstname, self.lastname)
x = Person('John', 'Doe')
x.pritname()
#结果
John Doe
```

#### 2.创建子类

- 要创建从另一个类继承功能的类，请在创建子类时将父类作为参数发送。

```python
#代码
class Person:
    def __init__(self, fname, lname):
        self.firstname = fname
        self.lastname = lname

    def pritname(self):
        print(self.firstname, self.lastname)

class Student(Person):
    pass
x = Student('Mike', 'Olsen')
x.pritname()
#结果
John Do
```

#### 3.添加init()函数

- 到目前为止，我们已经创建了一个继承父类的属性和方法的子类。
- 我们想将init()函数添加到子类（而不是pass）

```python
#代码
class Student(Person):
    def __init__(self, fname, lname):
        Person.__init__(self, fname, lname)
```

```python
#代码
class Student(Person):
    def __init__(self, fname, lname):
        super().__init__(fname, lname)
```

#### 4.增加属性

```python
#代码
class Person:
    def __init__(self, fname, lname):
        self.firstname = fname
        self.lastname = lname

    def pritname(self):
        print(self.firstname, self.lastname)

class Student(Person):
    def __init__(self, fname, lname, year):
        super().__init__(fname, lname)
        self.graduationyear = year

x = Student('Mike', 'Olsen', 2019)
x.pritname()
#结果
Mike Olsen
```

#### 5.增加方法

```python
#代码
class Person:
    def __init__(self, fname, lname):
        self.firstname = fname
        self.lastname = lname

    def pritname(self):
        print(self.firstname, self.lastname)


class Student(Person):
    def __init__(self, fname, lname, year):
        super().__init__(fname, lname)
        self.graduationyear = year
    def welcome(self):
        print('Welcome', self.firstname, self.lastname, 'to the class of', self.graduationyear)


x = Student('Mike', 'Olsen', 2019)
x.welcome()
x.pritname()
#结果
Welcome Mike Olsen to the class of 2019
Mike Olsen
```

### 3.Python迭代器

- 迭代器是一个包含可数个值的对象。
- 迭代器是可以迭代的对象，这意味着您可以遍历所有值。
- 从技术上讲，在Python中，迭代器是一个实现迭代器协议的对象，它由方法iter()和next()组成。

#### 1.创建迭代器

- 要创建一个对象/类作为迭代器，必须实现方法iter()和next0,
- 正如上面了解到的，所有类都有一个名为init()的函数，它允许在创建对象时进行一些初始化.
- iter()方法的作用类似，可以进行操作（初始化等），但必须始终返回迭代器对象本身。
- next()方法还允许执行操作，并且必须返回序列中的下一项。

```python
#代码
class MyNumbers:
    def __iter__(self):
        self.a = 1
        return self

    def __next__(self):
        x = self.a
        self.a += 1
        return x

my = MyNumbers()
myiter = iter(my)

print(next(myiter))
print(next(myiter))
print(next(myiter))
print(next(myiter))
print(next(myiter))
#结果
1
2
3
4
5
```

#### 2.停止迭代

- 如果有足够多的next()语句，或者如果它在for循环中使用，上面的例子将永远持续下去。
- 为了防止迭代永远进行，我们可以便用StopIteration语句。
- 在next()方法中，我们可以添加终止条件以在迭代完成指定次数时引发错误。

```python
#代码
class MyNumbers:
    def __iter__(self):
        self.a = 1
        return self

    def __next__(self):
        if self.a <= 20:
            x = self.a
            self.a += 1
            return x
        else:
            raise StopIteration


my = MyNumbers()
myiter = iter(my)

for x in myiter:
    print(x)
#结果
1~20
```

## 模块

### 1.什么是模块？

- 将模块视为与代码库相同。
- 一个文件，其中包含要包含在应用程序中的一组函数。

### 2.创建模块

- 要创建模块，只需将所需的代码保存在文件拓展名为.py的文件中。

```python
#代码
#代码
# %load mymodule.py
person1 = {
    'name': 'John',
    'age': 36,
    'country': 'Norway'
}


def greeting(name):
    print('Hello, ' + name)
```

### 3.使用模块

- 现在我们可以使用我们刚创建的模块，通过使用import语句。

```python
#代码
import mymodule

mymodule.greeting('Jonathan')
#结果
Hello, Jonathan
```

### 4.模块中的变量

- 模块可以包含已经描述过的函数，也可以包含所有类型的变量（数组、字典、对象等）。

```python
#代码
import mymodule

a = mymodule.person1['age']
print(a)
#结果
36
```

### 5.从模块导入

- 可以使用from关键字选择仅从模块导入部分内容。

```python
#代码
from mymodule import person1

print(person1['age'])
#结果
36
```

## 文件

- 文件处理是任何Web应用程序的重要组成部分。
- Python具有多个用于创建、读取、更新和删除文件的函数。

### 1.文件处理

- 在Python中处理文件的关键函数是open()函数.

- open()函数有两个参数；文件名和模式.

- 打开文件有四种不同的方法（模式）：

  >"r" - 读取 - 默认值。打开一个文件进行读取，如果文件不存在则报错。
  >
  >"a" - Append - 打开一个文件进行追加，如果文件不存在则创建该文件。
  >
  >"w" - 写入 - 打开一个文件进行写入，如果文件不存在则创建该文件。
  >
  >"x" - Create - 创建指定的文件，如果文件存在则返回错误。

- 此外，您可以指定文件是否应作为二进制或文本模式处理。

  > "t" - 文本 - 默认值。文本模式。
  > "b" - 二进制 - 二进制模式（列如图像）。

```python
# %load demofile.txt
Hello! Welcome to demofile.txt
This file is for testing purposes.
Good Luck!

#代码
f = open('demofile.txt')

#代码
f = open('demofile.txt', 'rt')
```

### 2.文件读取

```python
#代码
f = open('demofile.txt', 'r')
print(f.read())
#结果
# %load demofile.txt
Hello! Welcome to demofile.txt
This file is for testing purposes.
Good Luck!

#代码
f = open('demofile.txt', 'r')
print(f.read(16))
#结果：只读文件的一部分。默认情况下，read()方法返回整个文本，但也可以指定要返回的字符数
# %load demofile

#代码
f = open('demofile.txt', 'r')
print(f.readline())
#结果：读一行
# %load demofile.txt

#代码
f = open('demofile.txt', 'r')
for x in f:
    print(x)
#结果
# %load demofile.txt

Hello! Welcome to demofile.txt

This file is for testing purposes.

Good Luck!
```

### 3.关闭文件

```python
#代码
f = open('demofile.txt', 'r')
print(f.readline())
f.close()
#结果
# %load demofile.txt
```

### 4.写入现有文件

- 要写入现有文件，您必须向Open()函数添加一个参数：

  > "a" - Append - 将追加到文件的末尾
  > "w" - 写入 - 将覆盖任何现有内容

```python
# %load demofile2.txt
aaaaaaaaaa
```
```python
#代码
f = open('demofile2.txt', 'a')
f.write('Now the file has more content!')
f.close()

f = open('demofile2.txt', 'r')
print(f.read())
f.close()
#结果
aaaaaaaaaaNow the file has more content!
```

```python
#代码
f = open('demofile2.txt', 'w')
f.write('Woops!I have deleted the content!')
f.close()

f = open('demofile2.txt', 'r')
print(f.read())
f.close()
#结果
Woops!I have deleted the content!
```

### 5.创建新文件

- 要在Python中创建新文件，请使用open()方法，并使用以下参数之一

  >"a" - Append - 打开一个文件进行追加，如果文件不存在则创建该文件。
  >
  >"w" - 写入 - 打开一个文件进行写入，如果文件不存在则创建该文件。
  >
  >"x" - Create - 创建指定的文件，如果文件存在则返回错误。

```python
#代码
f = open('myfile.txt', 'x')
```

### 6.删除文件

- 要删除文件，必须导入OS模块，并运行其os.remove()模块

```python
#代码
import os
os.remove('demofile2.txt')
```

### 7.检查文件是否存在

- 为避免出现错误，您可能需要在尝试删除文件之前检查该文件是否存在。

```python
#代码
import os
if os.path.exists('demofile.txt'):
    os.remove('demofile.txt')
else:
    print('The file does not exist')
```

