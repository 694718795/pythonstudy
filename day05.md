## day 05-字符串

### 1 字符串特征

单引号 双引号字符串
name1 = 'Tom' 
name2 = "Rose"    

三引号字符串

```python
# 三引号
e = '''i am TOM'''
print(type(e))

f = """I 
am TOM"""
print(type(f))
print(f)     #三引号字符串支持换行
```



```python
d = 'I\'m TOM'   # \  转义
```

### 2 字符串格式化

```python
name = 'ROSE'
# 我的名字是TOM
print('我的名字是%s' % name)
print(f'我的名字是{name}')    # f表示格式化字符串  将变量格式化为字符串
```

### 3 下标

```python
str1 = 'abcdefg'
print(str1)

# 数据在程序运行过程中存储在内存
# ？ 得到数据a字符， 得到数据b字符 --   使用字符串中某个特定的数据
# 这些字符数据从0开始顺序分配一个编号 -- 使用这个编号精确找到某个字符数据 -- 下标或索引或索引值
# str1[下标]
print(str1[0])
print(str1[1])
```

### 4 切片

```python
# 序列名[开始位置的下标:结束位置的下标:步长]

str1 = '012345678'
# print(str1[2:5:1])  # 234
# print(str1[2:5:2])  # 24
# print(str1[2:5])  # 234
# print(str1[:5])  # 01234 -- 如果不写开始，默认从0开始选取
# print(str1[2:])  # 2345678 -- 如果不写结束，表示选取到最后
# print(str1[:])  # 012345678 -- 如果不写开始和结束，表示选取所有

# 负数测试
# print(str1[::-1])  # 876543210 -- 如果步长为负数，表示倒叙选取
# print(str1[-4:-1])  # 567 -- 下标-1表示最后一个数据，依次向前类推

# 终极测试
# print(str1[-4:-1:1])  # 567
print(str1[-4:-1:-1])  # 不能选取出数据：从-4开始到-1结束，选取方向为从左到右，但是-1步长：从右向左选取
# **** 如果选取方向(下标开始到结束的方向) 和 步长的方向冲突，则无法选取数据


print(str1[-1:-4:-1])  # 876
```

### 5 字符串查找

```python
mystr = "hello world and itcast and itheima and Python"

#检测某个子串是否包含在这个字符串中，如果在返回这个子串开始的位置下标，否则则返回-1
# 1. find() 
# print(mystr.find('and'))  # 12
# print(mystr.find('and', 15, 30))  # 23
# print(mystr.find('ands'))  # -1 , ands子串不存在

#index()：检测某个子串是否包含在这个字符串中，如果在返回这个子串开始的位置下标，否则报异常。
# 2.index()
# print(mystr.index('and'))  # 12
# print(mystr.index('and', 15, 30))  # 23
# print(mystr.index('ands'))  # 如果index查找子串不存在，报错

# 3.count()  统计出现的次数
# print(mystr.count('and', 15, 30))
# print(mystr.count('and'))  # 3
# print(mystr.count('ands'))  # 0

# 4.rfind()  与find相同,方向相反
# print(mystr.rfind('and'))
# print(mystr.rfind('ands'))

# 5.rindex()   与index相同,方向相反
# print(mystr.rindex('and'))
# print(mystr.rindex('ands'))
```

