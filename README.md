# Knowledge
```
https://blog.csdn.net/weixin_42134789/article/details/82381828
python列表表达式和内置高阶函数（lamda， zip， enumerate， map， filter， reduce， sorted）：
List comprehension: 以一个快捷的方法对列表进行操作或运算，返回新的列表。
[表达式 for 变量 in 列表] 或者 [表达式 for 变量 in 列表 if 条件]

1.把列表解析的[]换成()得到的就是生成器表达式
2.列表解析与生成器表达式都是一种便利的编程方式，只不过生成器表达式更节省内存
3.生成器yield的表达式 ？？？
```

```
lambda匿名函数，常和sorted, map,reduce,filter一起使用。
lambda param1，param2,...,paramn : expression
>>> list1 = [ 5, -3, 1, 8, -4 ]
>>> list2 = sorted(list1, key=lambda x:abs(x))
>>> print(list2)
[1, -3, -4, 5, 8]
  
>>> flist = [lambda x:x*x for x in range(1, 3)]  #函数对象列表
>>> print(flist)
[<function <listcomp>.<lambda> at 0x03ADE2B8>, <function <listcomp>.<lambda> at 0x03ADE300>]
>>> flist[0]
<function <listcomp>.<lambda> at 0x03ADE2B8>
>>> flist[0](2)
4
```
```
zip函数：将多个列表对应元素打包成tuple，使用list方法可以将其变成列表，使用dict方法可以将其变成字典。

>>> l1 = [ 1, 2, 3 ]
>>> l2 = [ 'x', 'y', 'z']
>>> l3 = [ 'x', 'y' ]
>>> zip(l1, l2)
<zip object at 0x031D6828>
>>> print(list(zip(l1, l2)))
[(1, 'x'), (2, 'y'), (3, 'z')]
>>> print(list(zip(l1, l3)))
[(1, 'x'), (2, 'y')]
>>> print(dict(zip(l1,l3)))
{1: 'x', 2: 'y'}

实际上zip方法支持所有可迭代对象（字符串、列表、元祖、字典), 而不仅仅是列表。
>> > l1 = [1, 2, 3]
>> > str1 = "abc"
>> > print(dict(zip(l1, str1)))
{1: 'a', 2: 'b', 3: 'c'}
>> > name = ["John", "Jim", "Lucy"]
>> > year = [1983, 1985, 1995]
>> > birth_year = dict(zip(name, year))
>> > print(birth_year)
{'John': 1983, 'Jim': 1985, 'Lucy': 1995}

zip(*some_list)方法可以实现元组列表的反向解压
>>> l1 = [("John", 1995), ("Lucy", 2000), ("Max", 1985)]
>>> name, year = zip(*l1)
>>> print(name)
('John', 'Lucy', 'Max')
>>> print(year)
(1995, 2000, 1985)
```
```
enumerate()函数：

```
```
```
```
```
```
```
```
```
```
