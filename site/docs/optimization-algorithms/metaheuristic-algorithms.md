# ⚙️ 优化算法 - 元启发式算法

元启发式算法（Metaheuristic）是近年来发展最快的优化算法，模拟自然界或社会现象，具有很强的全局搜索能力。

## 🎯 主要算法

### 1. 遗传算法 (Genetic Algorithm, GA)
- 基于达尔文进化论
- 操作：选择、交叉、变异
- 应用：参数优化、组合优化

### 2. 粒子群算法 (Particle Swarm Optimization, PSO)
- 基于鸟群捕食行为
- 速度和位置更新公式
- 优点：收敛快、参数少

### 3. 模拟退火 (Simulated Annealing, SA)
- 基于固体退火过程
- 能量函数和温度参数
- 具有理论收敛性保证

### 4. 蚁群算法 (Ant Colony Optimization, ACO)
- 基于蚂蚁信息素机制
- 适合组合优化问题
- 特别是TSP和VRP

## 💻 编程示例

```python
# PSO算法框架
import numpy as np

class PSO:
    def __init__(self, n_particles, n_iterations, bounds):
        self.n_particles = n_particles
        self.n_iterations = n_iterations
        self.bounds = bounds
        
    def optimize(self, objective_func):
        # 初始化粒子位置和速度
        x = np.random.uniform(*self.bounds, 
                             (self.n_particles, len(self.bounds[0])))
        v = np.random.uniform(-1, 1, x.shape)
        
        pbest = x.copy()
        pbest_fitness = np.array([objective_func(xi) for xi in x])
        gbest = pbest[pbest_fitness.argmin()]
        
        for iteration in range(self.n_iterations):
            # 更新速度和位置
            w = 0.9 - iteration * 0.5 / self.n_iterations
            c1, c2 = 2.0, 2.0
            
            r1, r2 = np.random.rand(2)
            v = (w * v + c1 * r1 * (pbest - x) + 
                 c2 * r2 * (gbest - x))
            x = x + v
            
            # 评估新位置
            fitness = np.array([objective_func(xi) for xi in x])
            pbest = np.where(fitness < pbest_fitness, x, pbest)
            pbest_fitness = np.minimum(fitness, pbest_fitness)
            gbest = pbest[pbest_fitness.argmin()]
        
        return gbest, pbest_fitness.min()
```

---

**下一步：** 学习[高级优化方法](advanced-optimization.md)中的精确算法！
