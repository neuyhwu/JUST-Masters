# 🔧 Gurobi优化求解器 - Python接口

Gurobi的Python接口提供了完整的建模和求解功能。

## 🎯 核心概念

### 1. 模型构建
```python
from gurobipy import *

# 创建模型
m = Model("my_model")

# 添加变量
x = m.addVar(name="x", lb=0, ub=10)
y = m.addVar(name="y", vtype=GRB.BINARY)

# 添加约束
m.addConstr(x + y >= 1)

# 设置目标函数
m.setObjective(x + 2*y, GRB.MAXIMIZE)

# 求解
m.optimize()
```

### 2. 结果分析
```python
if m.status == GRB.OPTIMAL:
    print(f"最优值: {m.objVal}")
    print(f"x = {x.X}, y = {y.X}")
else:
    print("未找到最优解")
```

### 3. 参数配置
```python
# 时间限制（秒）
m.params.TimeLimit = 300

# 优化间隙（百分比）
m.params.MIPGap = 0.01

# 线程数
m.params.Threads = 4
```

---

**下一步：** 学习[高级应用](advanced-applications.md)！
