# Python的基本数据类型

## 1. Number：数字

- 整数(int)、小数(float) ,python 3.x中没有单双精度之分，因为小数在python中支持的就是双精度浮点型

  ```python
  type(1*1)
  #int类型,无取值范围限制
  type（1*1.0）
  #float类型
  type(2/2)
  #float类型，1.0
  type(2//2)
  #int类型，结果是1，python中整数除以整数需要两个//
  ```

- 二进制以0b开头：0b11表示3

- 八进制以0o开头：0o11表示9

- 十六进制以0x开头：0x11表示17

- bool布尔类型：表示真、假 (python中bool类型包含在Number类型)

- 复数：36j在python中用小写字母j结尾表示复数

  ```python
  #进制转换
  #通过bin()方法可以将任意进制的数字转换为二进制
  bin(10)#0b1010
  bin(0o7)#0b111
  bin(0xE)#0b1110
  #通过oct()方法将任意进制的数字转换为八进制
  oct(0b111)#0o7
  oct(0xE)#0o16
  oct(888)#0o1570
  #通过int()方法将任意进制的数字转换为十进制
  int(0b111)#7
  int(0o7)#63
  int(0xE)#14
  #通过hex()方法将任意进制的数字转换为十六进制
  hex(0b111)#0x7
  hex(0o777)#0o7777
  hex(888)#0x378
  
  #
  bool(1)
  #ture
  bool(0)
  #false
  ```


## 2. str：字符

```python
#用单引号或者双引号表示字符或字符串
type('1')
#str
type("1")
#str

#使用‘’‘三引号实现多行字符串相当于使用了转义字符\n
'''
hello world
hello world
hello world
'''
'\nhello world\nhello world\nhello world\n'

#输出原始字符串，在字符串前加r
print(r"c:\northwind\northwest")
#所见即所得：c:\northwind\northwest
```

- 字符串拼接

  ```python
  #通过加号进行字符串拼接
  print("hello"+"world")
  #helloworld
  ```

- 字符串的乘法

  ```python
  #字符串乘法运算只能乘以数字
  print("hello"*3)
  #hellohellohello
  ```

- 字符提取

  ```python
  print("hello world"[0])
  #h
  print("hello world"[1])
  #e
  print("hello world"[2])
  #l
  #取值为正号时，是按字符串的下标提取字符
  
  print("hello world"[-1])
  #d
  print("hello world"[-2])
  #l
  print("hello world"[-3])
  #r
  #取值为负号时是从字符串的末尾开始提取字符
  
  #提取一段字符串可以使用 [起点：终点] 不包括终点
  print("hello world"[0:4])
  #hell
  print("hello world"[0:5])
  #hello
  
  #当终点字符为负号时，表示从字符串末尾开始数字符，然后提取剩下的字符
  print("hello world"[0:-1])
  #hello worl
  print("hello world"[0:-3])
  #hello wo
  
  print("hello world"[6:])
  #world，正数开头省略终点，表示从头开始算，第六个字符开始取后面所有字符
  
  print("hello world"[-5:])
  #world负数开头时，表示提取字符末尾开始数的那几个数字
  ```

## 3. list

```python
#python中的列表类型可以同时包含任意数据类型，甚至可以在列表中包含列表

tpye([1,2,3,4,5,6])
#list
type(["hello","world",1,9])
#list
type(["hello","world",1,9,True,False])
#list
type(["hello","world",1,9,[1,2],["wen","shui"],[True,False]])
#list


#访问列表中的元素，与数组的使用是相似的

["hello","world",1,9,[1,2],["wen","shui"]][0]
#"hello"
["hello","world",1,9,[1,2],["wen","shui"]][1]
#"world"
["hello","world",1,9,[1,2],["wen","shui"]][0:2]
#["hello","world"]   使用[x,x]的方式访问时会返回一个列表
["hello","world",1,9,[1,2],["wen","shui"]][-1：]
#["wen","shui"]

#列表的拼接/追加
["hello","world",1,9]+["hello","world",1,9,True,False]
#['hello', 'world', 1, 9, 'hello', 'world', 1, 9, True, False]

#列表的乘法
["hello","world",1,9]*3
#['hello', 'world', 1, 9, 'hello', 'world', 1, 9, 'hello', 'world', 1, 9]



```

