# Python教程



python3.10.5 下载地址: https://www.python.org/ftp/python/3.10.5/python-3.10.5-amd64.exe

…………………………………………………………………………

[TOC]

…………………………………………………………………………

### 第一章  输出



#### print的基本运用



##### 01. 使用方法

在python中，print是一个自带函数，函数都是由 括号 "()" 来调用，print也是如此

如下

```python
# 输出
print()
```



这里假设我们要输出一个数字，比如10，则只需要在括号内填入即可

```python
# 输出10
print(10)
```



但若是要输出一段文字，比如hello world!，则需要加上双引号

```python
# 输出hello world!
print("hello world!")
```

其他的也是一样

但是如果你坚持不写上双引号的话，结果就是...

```python
File "<stdin>", line 1
    print(hello world!)
          ^^^^^^^^^^^
SyntaxError: invalid syntax. Perhaps you forgot a comma?
```

报错！！！

当然，加上单引号(' ')也是可以的



#### print的高级运用

##### 01.更多参数

print还有一些小秘密，以下是print函数的源代码

```python
def print(self, *args, sep=' ', end='\n', file=None): # known special case of print
    """
    print(value, ..., sep=' ', end='\n', file=sys.stdout, flush=False)
    
    Prints the values to a stream, or to sys.stdout by default.
    Optional keyword arguments:
    file:  a file-like object (stream); defaults to the current sys.stdout.
    sep:   string inserted between values, default a space.
    end:   string appended after the last value, default a newline.
    flush: whether to forcibly flush the stream.
    """
    pass
```

所有参数的意思

self: (暂定无用)

*args:该参数为我们所要输出的文字

sep:几段文字之间的空格         默认参数值:(一个空格)

end:打印完文字后执行            默认参数值:'\n'             注意 在此处的'\n'并不属于 字符串 它属于换行符

file:输出文件                            默认参数值:None        (可以理解成什么都没有)



##### 02.基本方法

由01的参数，我们可以这样写

```python
print("hello", "world", end='\n') # \n相当于键盘上的Enter键
#        |        |       |
#       args     sep     end
print("hello", "world", end='\t') # \t相当于键盘上的空格键
print("hello", "world", end='\n')
print("hello", "world", end='\t')
print("hello", "world", end='\t')
print("hello", "world", end='\n')
```



运行后，就会出现这样的效果

```-
hello world
hello world	hello world
hello world	hello world	hello world
```

