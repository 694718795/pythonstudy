## day06-列表&元组

### 1 列表

#### 1.1 列表定义

```python
name_list = ['TOM', 'Lily', 'ROSE']
```

#### 1.2 列表下标

```python
print(name_list[1])
```

#### 1.3 列表常用方法

```python
# 1. index()   找出指定元素的下标
# print(name_list.index('TOM'))
# print(name_list.index('TOMS'))  报错 不存在

# 2. count()   统计指定元素的个数
# print(name_list.count('TOM'))   1
# print(name_list.count('TOMS'))  0

# 3.len()   统计列表的长度
print(len(name_list))

# 1. in   判断元素在列表中是否存在
# print('TOM' in name_list)
# print('TOMS' in name_list)

# 2. not in
# print('TOM' not in name_list)
print('TOMs' not in name_list)

# name_list.append('xiaoming')      ['TOM', 'Lily', 'ROSE', 'xiaoming']
name_list.append([11, 22])          ['TOM', 'Lily', 'ROSE', [11, 22]]

print(name_list)

# 1. 列表数据可改的 -- 列表可变类型
# 2. append函数追加数据的时候如果数据是一个序列，追加整个序列到列表的结尾

# name_list.extend('xiaoming')
name_list.extend(['xiaoming', 'xiaohong'])

print(name_list)

# extend() 追加数据是一个序列，把数据序列里面的数据拆开然后逐一追加到列表的结尾

# name_list.insert(下标, 数据)
name_list.insert(1, 'aaa')
print(name_list)

## 列表嵌套 
name_list = [['TOM', 'Lily', 'Rose'], ['张三', '李四', '王五'], ['xiaohong', 'xiaoming', 'xiaolv']]

# print(name_list)

# 列表嵌套的时候的数据查询
# print(name_list[0])
print(name_list[0][1])
```

### 2 元组

一个元组可以存储多个数据,元组中的数据是不可修改的

#### 2.1 元组定义

```python
# 1. 多个数据元组
t1 = (10, 20, 30)
print(type(t1))  #  <class 'tuple'>

# 2. 单个数据的元组
t2 = (10,)
print(type(t2))   #<class 'tuple'>

# 3. 如果单个数据的元组不加逗号
t3 = (10)
print(type(t3))  # <class 'int'>
```

如果定义的元组只有一个数据，那么这个数据后面也最好添加逗号，否则数据类型为唯一的这个数据的数据类型    

#### 2.2 元组的常见操作

```python
t1 = ('aa', 'bb', 'cc', 'bb')

# 1. 下标
# print(t1[0])

# 2. index()   查找到某个元组数据的下标
# print(t1.index('bb'))
# print(t1.index('bbb'))

# 3. count()   计算出某个元组数据的个数
# print(t1.count('aa'))
# print(t1.count('aaa'))

# 4. len()     计算元组的长度
print(len(t1))
```

#### 2.3 元组数据的修改

元组中的数据如果直接修改会报错

```python
tuple1 = ('aa', 'bb', 'cc', 'bb')
tuple1[0] = 'aaa'
```

但是如果元组中的数据有列表,则可以修改列表中的元素

```python
tuple2 = (10, 20, ['aa', 'bb', 'cc'], 50, 30)
print(tuple2[2]) # 访问到列列表
# 结果： (10, 20, ['aaaaa', 'bb', 'cc'], 50, 30)
tuple2[2][0] = 'aaaaa'
print(tuple2)
```

