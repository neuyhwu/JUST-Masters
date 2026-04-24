# 🐍 Python编程 - 科学计算库

科学计算库是Python在优化和机器学习领域的核心支撑。

## 📚 主要库

### NumPy
```python
import numpy as np

# 创建数组
a = np.array([[1, 2], [3, 4]])
b = np.random.rand(3, 3)

# 矩阵运算
c = np.dot(a, b.T)
d = np.linalg.inv(b)
```

### SciPy
```python
from scipy.optimize import minimize
from scipy import stats

# 无约束优化
result = minimize(lambda x: sum(x**2), x0=[1, 1])
```

### Pandas
```python
import pandas as pd

# 创建DataFrame
df = pd.read_csv('data.csv')
df.groupby('category').mean()
```

## 🔗 相关资源

- [Gurobi Python接口](../gurobi-solver/python-interface.md) - 优化求解
- [数据处理与分析](data-processing.md) - 实际应用

---

**下一步：** 学习[数据处理与分析](data-processing.md)！
