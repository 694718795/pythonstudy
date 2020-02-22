## day03

## 1 if

```python
"""
if 条件:
    条件成立执行的代码1
    .....
"""

money = 0
seat = 1

if money == 1:
    print('土豪，请上车')
    # 判断是否能坐下
    if seat == 1:
        print('有空座，坐下了')
    else:
        print('没有空座，站着等....')
else:
    print('朋友，没带钱，跟着跑，跑快点')
```

## 2 随机数

```python
"""
步骤
    1. 导入模块
    import random
    2. 使用这个模块中的功能
    random.randint()
"""

import random

num = random.randint(0, 2)

print(num)
```

### 3 三目运算符

```
"""
语法
条件成立执行的表达式 if 条件 else 条件不成立执行的表达式
"""
a = 1
b = 2

c = a if a > b else b  # C=a (如果) a大于b  否则就等于 b
print(c)
```

