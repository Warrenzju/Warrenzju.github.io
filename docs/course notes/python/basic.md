# Python 基础语法指南

Python 是一种以其简洁明了的语法而闻名的高级编程语言。本指南旨在为初学者提供 Python 编程的核心概念和基本语法。

## 1. 变量和数据类型

变量是用于存储数据值的容器。在 Python 中，你不需要显式声明变量的类型，变量的类型是在你给它赋值时确定的。

### 基本数据类型

- **整型 (Integer)**: `x = 10`
- **浮点型 (Float)**: `y = 3.14`
- **字符串 (String)**: `name = "张三"` 或 `name = '李四'`
- **布尔型 (Boolean)**: `is_true = True` 或 `is_false = False`

你可以使用 `type()` 函数来查看任何变量的数据类型。

```python
x = 10
pi = 3.14
greeting = "你好, 世界!"

print(type(x))       # 输出: <class 'int'>
print(type(pi))      # 输出: <class 'float'>
print(type(greeting))# 输出: <class 'str'>
```

## 2. 注释

注释是代码中不会被执行的部分，用于解释代码的功能。

- **单行注释**: 使用 `#` 开头。
- **多行注释**: 使用三个单引号 `'''` 或三个双引号 `"""` 将注释内容包围起来。

```python
# 这是单行注释

'''
这是一个多行注释，
可以跨越多行。
'''
```

## 3. 输入和输出 (Input and Output)

程序需要与用户交互，接收用户的输入并向用户展示结果。

### 输出语句 (`print`)

`print()` 函数用于在控制台显示信息。

```python
# 打印固定的字符串
print("你好, 世界!")

# 打印变量
name = "爱丽丝"
age = 20
print(name)

# 打印多个项目，它们会以空格分隔
print("姓名:", name, "年龄:", age)

# 使用 f-string (格式化字符串字面值)，这是推荐的方式
print(f"你好，我叫{name}，我今年{age}岁。")
```

### 输入语句 (`input`)

`input()` 函数用于从用户那里获取键盘输入。

**重要提示**: `input()` 函数返回的所有内容**都是字符串类型**。如果你需要一个数字，你必须手动进行类型转换。

```python
# 获取用户名
name = input("请输入您的名字: ")
print(f"你好, {name}!")

# 获取年龄并转换为整数
age_str = input("请输入您的年龄: ")
try:
    age = int(age_str) # 尝试将字符串转换为整数
    print(f"您明年就 {age + 1} 岁了。")
except ValueError:
    print("无效的输入，请输入一个数字。")
```

## 4. 运算符

### 算术运算符

- 加: `+`
- 减: `-`
- 乘: `*`
- 除: `/` (结果为浮点数)
- 整除: `//` (结果为整数)
- 取模 (余数): `%`
- 幂: `**`

### 比较运算符

- 等于: `==`
- 不等于: `!=`
- 大于: `>`
- 小于: `<`
- 大于等于: `>=`
- 小于等于: `<=`

### 逻辑运算符

- 与: `and`
- 或: `or`
- 非: `not`

## 5. 数据结构

### 列表 (List)

列表是一个有序且可变的数据集合。用方括号 `[]` 定义。

```python
fruits = ["苹果", "香蕉", "橙子"]
fruits.append("葡萄")      # 添加元素
print(fruits[0])         # 访问第一个元素: "苹果"
```

### 元组 (Tuple)

元组是一个有序但不可变的数据集合。用圆括号 `()` 定义。

```python
colors = ("红色", "绿色", "蓝色")
print(colors[0]) # "红色"
```

### 字典 (Dictionary)

字典是无序的键值对 (key-value) 集合。用花括号 `{}` 定义。

```python
person = { "姓名": "王五", "年龄": 25 }
print(person["姓名"])      # "王五"
```

### 集合 (Set)

集合是一个无序、不重复的元素集。

```python
numbers = {1, 2, 3, 4, 4, 5}
print(numbers) # {1, 2, 3, 4, 5}
```

## 6. 控制流：分支与循环

控制流语句可以决定代码的执行顺序。

### 分支语句 (if, elif, else)

用于根据一个或多个条件来决定执行哪段代码。

```python
score = 85

if score >= 90:
    print("优秀")
elif score >= 80:
    print("良好")
elif score >= 60:
    print("及格")
else:
    print("不及格")
```

### for 循环

用于遍历一个序列（如列表、元组、字典、集合或字符串）或其他可迭代对象。

```python
fruits = ["苹果", "香蕉", "橙子"]
for fruit in fruits:
    print(f"我喜欢吃{fruit}")
```

### while 循环

当给定条件为真时，重复执行一段代码块。

```python
count = 0
while count < 5:
    print(f"当前数字是: {count}")
    count += 1
```

### 循环控制语句 (break 和 continue)

- `break`: 完全终止并跳出整个循环。
- `continue`: 跳过当前这次循环的剩余代码，直接开始下一次循环。

```python
# break 示例
for num in range(1, 20):
    if num % 7 == 0:
        print(f"找到了！第一个能被 7 整除的数是 {num}")
        break

# continue 示例
for num in range(10):
    if num % 2 == 0:
        continue
    print(f"奇数: {num}")
```

## 7. 函数

函数是组织好的、可重复使用的，用来实现单一或相关联功能的代码段。

```python
def greet(name):
    """这个函数向传入的名字打招呼。"""
    return f"你好, {name}!"

message = greet("小明")
print(message)
```

## 8. 模块和导入

你可以导入和使用标准库模块或你自己编写的模块。

```python
import math
print(math.sqrt(16))

from random import randint
print(randint(1, 10))
```

## 9. 异常处理

使用 `try...except` 块来处理可能发生的错误。

```python
try:
    result = 10 / 0
except ZeroDivisionError:
    print("错误：不能除以零！")
finally:
    print("这段代码总会执行。")
```

## 10. 面向对象编程 (简介)

Python 是一种面向对象的语言。你可以定义类来创建对象。

```python
class Dog:
    def __init__(self, name):
        self.name = name

    def bark(self):
        return f"{self.name} 正在叫!"

my_dog = Dog("旺财")
print(my_dog.bark())
```