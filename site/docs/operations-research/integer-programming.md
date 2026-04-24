# 📘 运筹学 - 整数规划

整数规划（Integer Programming, IP）在运筹学中具有重要地位，许多实际问题都需要离散决策，导致整数或混合整数规划问题。

## 🎯 学习目标

- 理解整数规划的分类和特点
- 掌握IP的建模技巧
- 学习分枝定界等求解算法
- 解决TSP、VRP等经典NP困难问题

## 📚 主要内容

### 1. IP模型分类
- **纯整数规划**：所有变量都是整数
- **混合整数规划**：部分变量是整数，部分是连续
- **0-1规划**：二进制变量，用于逻辑决策

### 2. 建模技巧
- 用二进制变量表示逻辑关系
- 大M方法处理if-then约束
- 目标函数的线性化技巧

### 3. 求解算法
- **分枝定界法（Branch and Bound）**
- **切割平面法（Cutting Plane）**
- **列生成法（Column Generation）**
- **优先级搜索（Priority Search）**

### 4. 经典应用问题
- **旅行商问题（TSP）**：访问所有城市且返回起点，最小化总距离
- **车辆路径问题（VRP）**：多个车辆的最优配送路线
- **设施选址问题**：选择最优的仓库或工厂位置
- **任务分配问题**：如何分配任务以最小化成本

## 💻 建模示例

```python
# VRP问题的Gurobi建模示例
from gurobipy import *
import numpy as np

# 问题数据
n_customers = 10
n_vehicles = 2
capacity = 100

# 创建模型
m = Model("VRP")

# 决策变量：x[i,j,k]=1 表示车辆k从客户i到j
x = m.addVars(n_customers, n_customers, n_vehicles, 
              vtype=GRB.BINARY, name="x")

# 约束和目标函数...
# (完整实现见Python编程模块)
```

## 🔗 相关资源

- [启发式算法](../optimization-algorithms/heuristic-algorithms.md) - 快速求解方法
- [Gurobi高级应用](../gurobi-solver/advanced-applications.md) - 工具应用
- [数据处理与分析](../python-programming/data-processing.md) - 数据准备

---

**下一步：** 学习[网络流问题](network-flows.md)和图论基础！
