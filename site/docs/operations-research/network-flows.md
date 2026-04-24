# 📘 运筹学 - 网络流问题

网络流问题（Network Flow）是运筹学中的经典问题，在交通、通信、供应链等领域有广泛应用。

## 🎯 学习目标

- 理解图论的基本概念
- 掌握最短路、最大流、最小成本流等算法
- 学会建立网络模型
- 应用到实际运输和物流问题

## 📚 核心算法

### 1. 最短路问题（Shortest Path）
- **Dijkstra算法**：非负权重情况
- **Bellman-Ford算法**：允许负权重
- **Floyd-Warshall算法**：全对最短路

### 2. 最大流问题（Maximum Flow）
- **Ford-Fulkerson方法**
- **Edmonds-Karp算法**
- **Dinic算法**

### 3. 最小成本流（Minimum Cost Flow）
- 结合最短路和最大流思想
- 循环消去法
- 成本递增法

## 💡 应用案例

### 例1：配送网络优化
一个物流公司需要从多个仓库配送商品到多个门店，最小化运输成本，同时满足供应和需求约束。

### 例2：电网运行调度
在电力系统中，需要确定发电站到用户的最优能源流动路线，最小化损耗。

## 🔗 相关资源

- [整数规划](integer-programming.md) - 网络设计问题
- [优化算法](../optimization-algorithms/index.md) - 算法优化
- [Java编程](../java-programming/index.md) - 图的数据结构实现

---

**推荐进度：** 掌握这三个核心章节后，进入[优化算法](../optimization-algorithms/index.md)学习更高级的技巧！
