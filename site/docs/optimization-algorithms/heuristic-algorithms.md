# ⚙️ 优化算法 - 启发式算法

启发式算法是快速获得可接受解的重要方法，特别是对于NP困难问题。

## 🎯 核心概念

### 1. 贪心算法 (Greedy Algorithm)
- 每步选择局部最优
- 快速但不保证全局最优
- 应用：最小生成树(Kruskal/Prim)、活动选择等

### 2. 局部搜索 (Local Search)
- 从初始解出发，通过邻域操作改进
- 可能陷入局部最优
- 需要多次运行和初值多样化

### 3. 构造性启发式
- 从部分解逐步构建完整解
- 最近邻法（Nearest Neighbor）
- 插入法（Insertion Heuristic）

## 💻 编程实例

```python
# TSP的最近邻启发式算法
def nearest_neighbor_tsp(distances, start=0):
    n = len(distances)
    unvisited = set(range(1, n))
    current = start
    tour = [start]
    total_dist = 0
    
    while unvisited:
        nearest = min(unvisited, 
                     key=lambda x: distances[current][x])
        total_dist += distances[current][nearest]
        tour.append(nearest)
        unvisited.remove(nearest)
        current = nearest
    
    total_dist += distances[current][start]
    return tour, total_dist
```

---

**下一步：** 学习[元启发式算法](metaheuristic-algorithms.md)的强大威力！
