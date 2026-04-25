# 📘 运筹学 - 线性规划

线性规划（Linear Programming, LP）是运筹学中最基础也最重要的分支，广泛应用于生产计划、资源分配等领域。

## 🎯 学习目标

- 掌握LP的标准形式和建模方法
- 理解单纯形法的原理和步骤
- 学会使用Gurobi、CPLEX等求解器
- 理解对偶理论和灵敏度分析

## 📚 主要内容

### 1. LP模型基础

- 标准形式：min/max c^T x subject to Ax = b, x ≥ 0
- 图形解法（二维问题）
- 基本可行解和顶点

### 2. 单纯形法

- 初始基本可行解的获得
- 进入变量和离开变量的选择
- 退化和循环问题
- 两阶段单纯形法

### 3. 对偶理论

- 对偶问题的构造
- 弱对偶性和强对偶性
- 互补松弛条件
- 对偶的经济解释

### 4. 灵敏度分析

- 目标函数系数的敏感性
- 约束右端常数的敏感性
- 矩阵元素的敏感性

## 💻 编程实例

```python
# 使用Gurobi求解LP问题
from gurobipy import *

# 创建模型
m = Model("LP_example")

# 决策变量
x = m.addVar(name="x")
y = m.addVar(name="y")

# 目标函数：最大化 3x + 2y
m.setObjective(3*x + 2*y, GRB.MAXIMIZE)

# 约束条件
m.addConstr(x + y <= 4, "c1")
m.addConstr(x <= 2, "c2")
m.addConstr(y <= 3, "c3")

# 求解
m.optimize()

# 输出结果
print(f"最优值: {m.objVal}")
print(f"x = {x.X}, y = {y.X}")
```

## 🔗 相关资源

- [整数规划](integer-programming.md) - LP的扩展
- [Gurobi Python接口](../gurobi-solver/python-interface.md) - 求解工具
- [Python科学计算](../python-programming/scientific-computing.md) - 计算支持

---

**下一步：** 学习[整数规划](integer-programming.md)处理离散决策问题！
