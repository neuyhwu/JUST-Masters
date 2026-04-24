# JUST-Masters 知识库

一个使用MkDocs + Material主题搭建的组织化知识库网站。

## 📖 访问网站

[在线查看网站](https://your-github-username.github.io/JUST-Masters/)

> 注意：请将上面的URL中的 `your-github-username` 替换为你的GitHub用户名

## 📁 项目结构

```
.
├── site/
│   ├── mkdocs.yml          # MkDocs配置文件
│   └── docs/               # 文档源文件
│       ├── index.md        # 首页
│       ├── getting-started.md
│       ├── about.md
│       ├── philosophy/     # 哲学分类
│       ├── literature/     # 文学分类
│       ├── history/        # 历史分类
│       └── arts/          # 艺术分类
├── venv/                   # Python虚拟环境
├── .github/
│   └── workflows/
│       └── deploy.yml      # GitHub Actions自动部署工作流
├── .gitignore              # Git忽略文件
└── README.md               # 本文件
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

## 📚 包含的分类

### 🤔 哲学
- 西方哲学 - 从古希腊到现代哲学的发展历程
- 马克思主义 - 马克思主义理论和实践

### 📖 文学
- 诗歌 - 各地诗歌艺术和作品欣赏
- 小说 - 经典小说和现代文学

### 🌍 历史
- 中国历史 - 从上古到现代的中国历史
- 世界历史 - 全球历史发展和重要事件

### 🎭 艺术
- 视觉艺术 - 绘画、雕塑、摄影、建筑
- 音乐 - 音乐历史、作曲家和音乐欣赏

## 🔧 部署

### 自动部署到GitHub Pages

代码会自动部署到GitHub Pages。每次推送到main分支，GitHub Actions会自动构建和部署网站。

```bash
git add .
git commit -m "更新内容"
git push origin main
```

### 手动部署（可选）

```bash
cd site
mkdocs build
```

生成的静态网站会输出到 `site/site/` 目录。

## 📝 写作指南

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

## 🔗 配置GitHub Pages

1. 打开你的仓库：`https://github.com/your-username/JUST-Masters`
2. 点击 **Settings** 标签
3. 左侧菜单找到 **Pages**
4. 在 "Build and deployment" 部分：
   - Source 选择：`Deploy from a branch`
   - Branch 选择：`main / root`
5. 点击 **Save**

部署通常需要1-3分钟。部署完成后，你的网站会发布到：
```
https://your-username.github.io/JUST-Masters/
```

## 🎨 定制

### 修改网站标题和描述

编辑 `site/mkdocs.yml`：

```yaml
site_name: 你的网站标题
site_description: 网站描述
site_author: 你的名字
```

### 修改主题颜色

编辑 `site/mkdocs.yml` 中的 `theme` 部分：

```yaml
theme:
  palette:
    - scheme: default
      primary: blue      # 改为其他颜色
      accent: indigo
```

可用颜色：red, pink, purple, deep-purple, indigo, blue, light-blue, cyan, teal, green, light-green, lime, yellow, amber, orange, deep-orange

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

- 📧 Email: your-email@example.com
- 🐙 GitHub: [@your-username](https://github.com/your-username)
- 🐦 Twitter: [@your-twitter]

## 📚 参考资源

- [MkDocs官方文档](https://www.mkdocs.org/)
- [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/)
- [GitHub Pages文档](https://docs.github.com/en/pages)
- [Markdown语法指南](https://www.markdownguide.org/)

---

**最后更新**: 2026年4月25日

**在线访问**: [https://your-github-username.github.io/JUST-Masters/](https://your-github-username.github.io/JUST-Masters/)
