# 🤖 机器学习 - 无监督学习

无监督学习用于数据探索和特征提取。

## 📚 主要算法

### 1. 聚类算法
```python
from sklearn.cluster import KMeans

# K-means聚类
kmeans = KMeans(n_clusters=3)
labels = kmeans.fit_predict(X_data)
```

### 2. 降维技术
- PCA（主成分分析）
- t-SNE（可视化）
- 自编码器

### 3. 异常检测
- 隔离森林
- 局部异常因子（LOF）
- 统计方法

---

**下一步：** 学习[深度学习基础](deep-learning-basics.md)！
