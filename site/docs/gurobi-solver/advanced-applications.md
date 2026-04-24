# 🔧 Gurobi优化求解器 - 高级应用

本章讨论Gurobi的高级功能和优化技巧。

## 🎯 高级技巧

### 1. 多目标优化
- 权重法
- ε-约束法
- 帕累托前沿

### 2. 参数调优
- 启发式求解器选择
- MIP Focus参数
- 割平面和预处理

### 3. 自定义回调
```python
def mycallback(model, where):
    if where == GRB.Callback.MIP:
        # 求解过程中处理
        pass

m.optimize(mycallback)
```

### 4. 批量求解
- 参数扫描
- 灵敏度分析
- 场景分析

---

**推荐：** 在实际项目中应用这些高级技巧！
