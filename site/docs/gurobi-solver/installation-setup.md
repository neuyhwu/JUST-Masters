# 🔧 Gurobi优化求解器 - 安装与配置

## 📋 安装步骤

### 1. 下载Gurobi

- 访问 https://www.gurobi.com/downloads/
- 选择对应操作系统版本

### 2. 安装

```bash
# Windows/Mac/Linux 根据系统选择
# 安装到默认目录或自定义位置
```

### 3. 获取许可证

- **学术许可证**（推荐）：访问 https://www.gurobi.com/academia/academic-program-and-licenses/
- **商业许可证**：需要购买

### 4. 激活许可证

```bash
grbgetkey [license-key]
具体操作如下：
![找到“bin”的路径](D:\BaiduSyncdisk\JUST-Masters\figs\gurobi-激活-bin.png "gurobi-激活-bin")
```

### 5. Python接口安装

```bash
pip install gurobipy
```

## ✅ 验证安装

```python
from gurobipy import *

m = Model("test")
x = m.addVar(name="x")
m.setObjective(x)
m.optimize()
print(f"Status: {m.status}")
```

---

**下一步：** 学习[Python接口](python-interface.md)！
