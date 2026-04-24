# 🤖 机器学习 - 监督学习

监督学习在预测和分类问题中应用最广泛。

## 📚 主要算法

### 1. 线性模型
```python
from sklearn.linear_model import LinearRegression
from sklearn.preprocessing import StandardScaler

# 数据准备
X_train = [[1], [2], [3]]
y_train = [2, 4, 6]

# 模型训练
model = LinearRegression()
model.fit(X_train, y_train)

# 预测
y_pred = model.predict([[4]])
```

### 2. 支持向量机（SVM）
- 线性SVM
- 核方法（RBF、多项式）
- 超参数调优

### 3. 集成方法
- 随机森林
- 梯度提升（XGBoost、LightGBM）
- Bagging和Boosting

---

**下一步：** 学习[无监督学习](unsupervised-learning.md)！
