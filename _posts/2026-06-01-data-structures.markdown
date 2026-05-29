---
layout: post
title: "📊 数据结构与算法入门"
date: 2026-05-25
categories: 算法 编程基础
---

## 为什么数据结构很重要？

数据结构是计算机存储、组织数据的方式。就像图书馆需要书架来管理书籍一样，程序需要数据结构来管理数据。好的数据结构能让程序更高效、更快速！

### 常见数据结构

#### 1. 数组（Array）
最基础的数据结构，就像一排整齐的储物柜：

```python
# Python中的数组（列表）
fruits = ["苹果", "香蕉", "草莓", "葡萄"]
print(fruits[0])  # 输出：苹果
print(fruits[2])  # 输出：草莓
```

#### 2. 链表（Linked List）
像一列火车，每个车厢连接下一个：

```python
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

class LinkedList:
    def __init__(self):
        self.head = None
```

#### 3. 栈（Stack）
像一叠盘子，只能从上面拿取（后进先出 LIFO）：

```python
# 使用列表模拟栈
stack = []
stack.append("盘子1")  # 入栈
stack.append("盘子2")
stack.pop()           # 出栈
```

#### 4. 队列（Queue）
像排队买奶茶，先来先服务（先进先出 FIFO）：

```python
from collections import deque
queue = deque(["小明", "小红", "小华"])
queue.append("小李")      # 入队
queue.popleft()          # 出队
```

## 算法入门

### 排序算法
排序是最基本的算法之一：

```python
# 冒泡排序
def bubble_sort(arr):
    n = len(arr)
    for i in range(n):
        for j in range(0, n-i-1):
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]
    return arr

# 测试
numbers = [64, 34, 25, 12, 22, 11, 90]
print(bubble_sort(numbers))
```

### 搜索算法
在数据中查找目标：

```python
# 二分查找（前提：数组已排序）
def binary_search(arr, target):
    left, right = 0, len(arr) - 1
    while left <= right:
        mid = (left + right) // 2
        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            left = mid + 1
        else:
            right = mid - 1
    return -1
```

## 学习建议

- 🎮 **多刷题**：LeetCode、牛客网
- 📖 **看经典书籍**：《算法导论》、《数据结构与算法之美》
- 💻 **动手实现**：不要只看不写
- 🔄 **复习巩固**：算法需要反复练习

数据结构与算法是程序员的"内功"，练好它才能写出高质量的代码！💪
