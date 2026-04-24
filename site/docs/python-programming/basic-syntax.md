# 🐍 Python编程 - 基础语法

Python因其简洁的语法和强大的功能成为科学计算的首选语言。

## 🎯 核心内容

### 1. 数据类型和结构
- 基本数据类型：int、float、str、bool
- 容器类型：list、tuple、dict、set
- 理解可变性和不可变性

### 2. 函数和模块
- 函数定义、参数、返回值
- 列表推导和生成器
- 模块和包的导入

### 3. 面向对象编程
- 类、对象、继承
- 属性和方法
- 特殊方法（__init__、__str__等）

### 4. 函数式编程特性
- Lambda函数
- Map、filter、reduce
- 装饰器

## 💻 代码示例

```python
# 函数式编程示例
data = [1, 2, 3, 4, 5]

# 列表推导
squares = [x**2 for x in data]

# Map和filter
doubled = list(map(lambda x: x*2, data))
evens = list(filter(lambda x: x%2==0, data))

# 类定义
class OptimizationProblem:
    def __init__(self, name, dimension):
        self.name = name
        self.dimension = dimension
    
    def evaluate(self, x):
        """评估目标函数"""
        return sum(x**2)
```

---

**下一步：** 学习[科学计算库](scientific-computing.md)！
