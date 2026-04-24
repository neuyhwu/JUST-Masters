# 🐍 Python编程 - 数据处理与分析

掌握Python数据处理能力是进行科学研究的重要基础。

## 📚 核心技能

### 1. 数据清洗
- 处理缺失值
- 异常值检测
- 数据类型转换

### 2. 数据可视化
- Matplotlib基础
- Seaborn统计可视化
- Plotly交互式图表

### 3. 统计分析
- 描述统计
- 假设检验
- 回归分析

## 💻 实践例子

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt

# 读取和清洗数据
df = pd.read_csv('sales.csv')
df = df.dropna()
df['date'] = pd.to_datetime(df['date'])

# 分析和可视化
monthly_sales = df.groupby(df['date'].dt.month).sum()
plt.plot(monthly_sales.index, monthly_sales['amount'])
plt.show()
```

---

**推荐：** 结合[机器学习](../machine-learning/index.md)学习高级数据分析技巧！
