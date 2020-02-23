## day04-循环

### 1 while 循环

```python
"""
while 条件:
    条件成立要重复执行的代码
    ......
"""

# 需求：重复打印5次媳妇儿，我错了 -- 1， 2， 3， 4， 5  6X -- 数据表示循环的次数 -- 第一次是1，最后依次5
# 1 + 1 + 1....
i = 1
while i <= 5:
    print('媳妇儿，我错了')
    i += 1  # i = i + 1
```

### 2 break && continue

```python
# continue : 当条件成立，退出当前一次循环，继而执行下一次循环
# break：当某些条件成立，退出整个循环
# 吃5个苹果 -- 循环； 吃到第3个吃出一个虫子，第三个不吃了，没吃饱，继续吃4和5个苹果 -- 只有第三个不吃
i = 1
while i <= 5:
    # 条件
    if i == 3:
        print('吃出一个大虫子，这个苹果不吃了')
        # 如果使用continue，在continue之前一定要修改计数器，否则进入死循环
        i += 1
        continue
        #break 
    print(f'吃了第{i}个苹果')
    i += 1
```

### 3 for循环

```python
"""
for 临时变量 in 序列:
    重复执行的代码
    ......
"""

"""
1. 准备一个数据序列
2. for
"""

str1 = 'itheima'
for i in str1:
    print(i)
```

### 4 while else

```python
# 需求：道歉5遍媳妇我错了，完成之后执行媳妇原谅我了
"""
1. 书写道歉的循环
2. 循环正常结束要执行的代码 -- else
"""
i = 1
while i <= 5:
    print('媳妇儿，我错了')
    i += 1
else:
    print('媳妇原谅我了，真开心呐，哈哈哈哈')
```

continue

```python
i = 1
while i <= 5:
    if i == 3:
        i += 1
        continue
    print(str(i)+'媳妇儿，我错了')
    i += 1
else:
    print('媳妇原谅我了，真开心呐，哈哈哈哈')    #程序正常结束  会执行本行代码
```

break

```python
i = 1
while i <= 5:
    if i == 3:
        break
    print(str(i)+'媳妇儿，我错了')
    i += 1
else:
    print('媳妇原谅我了，真开心呐，哈哈哈哈')  #程序未正常结束  不会执行本行代码
```

### 4 for else

```python
str1 = 'itheima'
for i in str1:
    if i == 'e':
        break
        # continue
    print(i)
else:
    #else中的代码 当循环正常结束会执行,  如果未正常结束,不会执行  比如有break 或者循环中程序报错
    print('循环正常结束执行的else的代码')    
```

