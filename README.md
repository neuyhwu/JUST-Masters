# 🎓 JUST-Masters知识库知识库

一个面向研究生的综合学习平台，采用MkDocs + Material主题搭建，汇集**运筹学、优化算法、编程技术和机器学习**的系统化资源。

## 📖 访问网站

[在线查看网站](https://neuyhwu.github.io/JUST-Masters/)

**网站名称**：JUST-YINGHUIWU-And-He's-Masters
**学科方向**：运筹学、优化算法、编程与机器学习

## 📁 项目结构

```
.
├── site/
│   ├── mkdocs.yml                    # MkDocs配置文件
│   └── docs/                         # 文档源文件
│       ├── index.md                  # 首页
│       ├── getting-started.md        # 入门指南
│       ├── about.md                  # 关于本知识库
│       ├── resources.md              # 学习资源汇总
│       ├── operations-research/      # 📘 运筹学模块 (4个文件)
│       ├── optimization-algorithms/  # ⚙️ 优化算法模块 (4个文件)
│       ├── python-programming/       # 🐍 Python编程模块 (4个文件)
│       ├── java-programming/         # ☕ Java编程模块 (4个文件)
│       ├── gurobi-solver/            # 🔧 Gurobi求解器模块 (4个文件)
│       └── machine-learning/         # 🤖 机器学习模块 (4个文件)
├── venv/                             # Python虚拟环境
├── .github/
│   └── workflows/
│       └── deploy.yml                # GitHub Actions自动部署工作流
├── .gitignore                        # Git忽略文件
└── README.md                         # 本文件
```

## 🚀 本地开发

### 环境要求

- Python 3.7+
- pip包管理器

### 快速开始

1. **克隆仓库**

   ```bash
   git clone https://github.com/your-username/JUST-Masters.git
   cd JUST-Masters
   ```
2. **创建虚拟环境**

   ```bash
   # Windows
   python -m venv venv
   venv\Scripts\activate

   # macOS/Linux
   python -m venv venv
   source venv/bin/activate
   ```
3. **安装依赖**

   ```bash
   pip install -r requirements.txt
   ```

   或手动安装：

   ```bash
   pip install mkdocs mkdocs-material pymdown-extensions
   ```
4. **启动本地服务**

   ```bash
   cd site
   mkdocs serve
   ```
5. **访问网站**
   打开浏览器访问 `http://localhost:8000`

### 编辑文档

编辑 `site/docs/` 目录中的markdown文件，保存后网站会自动刷新。

## 📚 六大核心模块

### 📘 运筹学模块

- **线性规划（LP）** - 单纯形法、对偶理论、灵敏度分析
- **整数规划（IP）** - 建模技巧、分支界算法、割平面法
- **网络流问题** - 最短路径、最大流、最小费用流

### ⚙️ 优化算法模块

- **启发式算法** - 贪心法、局部搜索、最近邻启发式
- **元启发式算法** - 遗传算法、粒子群优化、模拟退火、蚁群算法
- **高级优化方法** - 分支界、割平面法、列生成、拉格朗日松弛

### 🐍 Python编程模块

- **基础语法** - 数据类型、函数、面向对象、函数式编程
- **科学计算库** - NumPy、SciPy、Pandas数据处理
- **数据处理与分析** - 数据清洗、可视化、统计分析

### ☕ Java编程模块

- **面向对象编程** - 类、接口、继承、多态、设计模式
- **集合与流处理** - Collections框架、Stream API、函数式接口
- **并发编程** - Thread、锁、线程池、并发容器

### 🔧 Gurobi求解器模块

- **安装与配置** - 环境设置、许可证管理、Python集成
- **Python接口** - 模型构建、求解、参数配置、结果分析
- **高级应用** - 多目标优化、参数调优、自定义回调、性能优化

### 🤖 机器学习模块

- **监督学习** - 线性回归、逻辑回归、SVM、决策树、集成方法
- **无监督学习** - K-means聚类、层次聚类、PCA降维、异常检测
- **深度学习基础** - 神经网络、反向传播、CNN、RNN、TensorFlow/PyTorch

## � 部署流程

### 自动部署

代码会自动部署到GitHub Pages。每次推送到main分支，GitHub Actions会自动构建和部署网站。

```bash
git add .
git commit -m "更新内容"
git push origin main
```

部署通常需要2-5分钟完成。

### 本地构建

```bash
cd site
mkdocs build
```

生成的静态网站会输出到 `site/site/` 目录。

## � 学习路径建议

### 初级研究生（第一学期）

1. 从 **运筹学** 模块开始，理解优化问题的基本概念
2. 学习 **Python编程**，掌握科学计算工具链
3. 实践 **Python科学计算库**，做简单的数据分析

### 中级研究生（第二学期）

1. 深入 **优化算法** 模块，理解各类求解方法
2. 学习 **Gurobi求解器**，掌握专业优化工具
3. 入门 **机器学习**，学习监督和无监督算法

### 高级研究生（第三-四学期）

1. 研究 **高级优化** 方法，如分支界、列生成
2. 掌握 **Java并发编程**，构建高性能系统
3. 深入 **深度学习**，学习复杂的神经网络模型

## 🀽� 写作指南

### Markdown语法

网站支持以下Markdown扩展：

**1. 提示框（Admonition）**

```markdown
!!! note "提示"
    这是一个笔记框

!!! warning "警告"
    这是一个警告框

!!! success "成功"
    这是成功提示

!!! danger "危险"
    这是危险警告
```

**2. 可展开内容（Details）**

```markdown
??? question "问题"
    这是可展开的答案
```

**3. 代码高亮（Superfences）**
支持多种编程语言的代码块：

```python
def hello():
    print("Hello, World!")
```

**4. 表格**

```markdown
| 列1 | 列2 |
|-----|-----|
| 数据1 | 数据2 |
```

**5. 表情符号**
支持emoji表情，如 ✅ ❌ 📚 等

### 文件组织

- 将新文件放在相应的分类文件夹中
- 更新 `site/mkdocs.yml` 中的导航菜单
- 使用中文文件名，避免特殊字符

## 🔗 GitHub Pages配置

该仓库已配置为自动部署到GitHub Pages。每次推送到main分支，GitHub Actions会自动：

1. 拉取最新代码
2. 使用MkDocs编译网站
3. 部署到gh-pages分支
4. 发布到 https://neuyhwu.github.io/JUST-Masters/

**部署时间**：通常需要2-5分钟。

## 🎨 网站定制

### 修改网站标题

编辑 `site/mkdocs.yml`：

```yaml
site_name: JUST-YINGHUIWU-And-He's-Masters
site_description: 面向研究生的运筹学、优化算法、编程与机器学习综合学习平台
```

### 修改主题颜色

编辑 `site/mkdocs.yml` 中的 `theme.palette` 部分改变主题色。

## 🐛 故障排除

### 问题：部署失败

1. 检查 GitHub Actions 日志：

   - 仓库 → Actions → 找到失败的workflow
   - 查看详细错误信息
2. 常见原因：

   - Python依赖版本不兼容
   - mkdocs.yml 配置错误
   - 文件编码问题

### 问题：网站样式不完整

检查 `site/mkdocs.yml` 中的 `site_url` 是否正确设置为：

```yaml
site_url: https://your-username.github.io/JUST-Masters/
```

### 问题：中文搜索不工作

这是已知问题。如需支持中文搜索，需要额外配置。请提交Issue讨论。

## 📄 许可证

本项目内容采用 **CC BY-NC-SA 4.0** 许可证

- ✅ 可以分享和改编
- ⚠️ 必须署名
- ⚠️ 不能用于商业用途
- ⚠️ 改编内容必须使用相同许可证

## 🤝 贡献

欢迎提交Issue和Pull Request！

### 贡献步骤

1. Fork 本仓库
2. 创建特性分支：`git checkout -b feature/amazing-feature`
3. 提交更改：`git commit -m 'Add amazing feature'`
4. 推送到分支：`git push origin feature/amazing-feature`
5. 打开 Pull Request

## 📧 联系方式

- � GitHub: [@neuyhwu](https://github.com/neuyhwu)
- 📚 知识库: [JUST-YINGHUIWU](https://neuyhwu.github.io/JUST-Masters/)

## 📚 参考资源

- [MkDocs官方文档](https://www.mkdocs.org/)
- [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/)
- [GitHub Pages文档](https://docs.github.com/en/pages)
- [Markdown语法指南](https://www.markdownguide.org/)

---

## 📊 项目统计

- **6个核心模块** - 运筹学、优化算法、Python、Java、Gurobi、机器学习
- **24个主要章节** - 系统化的知识划分
- **100+个代码示例** - 实践导向的学习材料
- **学习路径** - 适合初/中/高级研究生的进阶计划

**最后更新**: 2026年4月25日

**在线访问**: [https://neuyhwu.github.io/JUST-Masters/](https://neuyhwu.github.io/JUST-Masters/)

**项目名称**: JUST-YINGHUIWU - 运筹优化研究生知识库
