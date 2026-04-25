# 📐 LaTeX排版详解

LaTeX是一个基于TeX的文档排版系统，由Leslie Lamport在20世纪80年代开发。它特别适合撰写包含复杂数学公式、大型文档和学术论文的排版工作。本指南将详细讲解LaTeX从入门到精通的完整路径。

## 🎯 为什么选择LaTeX？

| 优势 | 说明 |
|-----|-----|
| **专业排版** | WYSIWYG的精准控制，学术出版的行业标准 |
| **数学公式** | 完美支持复杂数学表达式，排版效果无与伦比 |
| **大型文档** | 自动生成目录、索引、引用，适合长篇论文 |
| **一致性** | 统一的格式控制，不需要手动调整样式 |
| **开源免费** | 完全开源，不受商业软件限制 |
| **可重复性** | 文本格式，版本控制友好，可复现 |

---

## 📦 环境搭建

### 方案1：在线编辑器（推荐新手）

**Overleaf**（最流行的在线LaTeX编辑器）：

1. 访问 https://www.overleaf.com
2. 创建免费账户
3. 创建新项目：选择模板或从空白开始
4. 实时编译预览，无需本地安装

**优势**：
- 无需安装，开箱即用
- 实时协作，多人编辑
- 模板库丰富
- 完整的参考文献管理

### 方案2：本地安装

#### Windows

```powershell
# 方法1：使用 MikTeX（推荐）
# 下载：https://miktex.org/download
# 运行安装程序，按默认选项安装

# 方法2：使用 TeX Live
# 下载：https://www.tug.org/texlive/acquire-netinstall.html
# 解压并运行安装程序
```

#### macOS

```bash
# 使用 MacTeX
brew install --cask mactex

# 或从官网下载：https://www.tug.org/mactex/
```

#### Linux (Ubuntu/Debian)

```bash
# 安装 TeX Live
sudo apt-get update
sudo apt-get install texlive-full

# 或仅安装基础包（更轻量）
sudo apt-get install texlive texlive-xetex texlive-latex-extra
```

### 编辑器配置

```bash
# VSCode + LaTeX Workshop 扩展
# 在VSCode扩展市场搜索 "LaTeX Workshop" 并安装

# TeXstudio（专用LaTeX编辑器）
# 下载：https://www.texstudio.org/

# Vim + vim-latex
# 高效编辑，适合熟悉Vim的用户
```

---

## 📝 基础文档结构

### 最小工作示例（MWE）

```latex
\documentclass{article}
\usepackage[utf8]{inputenc}
\usepackage[Chinese]{babel}

\title{我的第一篇LaTeX文档}
\author{张三}
\date{\today}

\begin{document}

\maketitle

\section{介绍}
这是一个简单的LaTeX文档示例。

\section{内容}
这是第二个章节。

\end{document}
```

### 文档类型选择

```latex
% 文章类（article）- 用于短文章、作业、期刊文章
\documentclass{article}

% 书籍类（book）- 用于完整的书籍和长文档
\documentclass{book}

% 报告类（report）- 用于技术报告、学位论文
\documentclass{report}

% 演示文稿类（beamer）- 用于演示幻灯片
\documentclass{beamer}

% 论文类（thesis） - 需要特殊包或大学模板
\documentclass{thesis}
```

---

## ✏️ 文本格式与结构

### 标题结构

```latex
\documentclass{report}
\begin{document}

\chapter{第一章}      % 章（仅在report和book中）
\section{第一节}      % 节
\subsection{第一小节} % 小节
\subsubsection{内容}  % 次小节

\end{document}
```

### 文本格式

```latex
% 强调和字体
\textbf{粗体文本}       % 粗体
\textit{斜体文本}       % 斜体
\texttt{等宽字体}       % 代码字体
\underline{下划线}      % 下划线
\textsc{小型大写字母}   % 小型大写

% 字体大小
{\tiny 超小}
{\scriptsize 脚本大小}
{\footnotesize 脚注大小}
{\small 小}
{\normalsize 正常}
{\large 大}
{\Large 更大}
{\LARGE 更更大}
{\huge 巨大}
{\Huge 超巨大}

% 组合使用
\textbf{\textit{粗斜体}}
```

### 段落与列表

```latex
% 列表环境
\begin{enumerate}
    \item 有序项1
    \item 有序项2
    \begin{enumerate}
        \item 嵌套项2.1
        \item 嵌套项2.2
    \end{enumerate}
\end{enumerate}

% 无序列表
\begin{itemize}
    \item 无序项1
    \item 无序项2
\end{itemize}

% 描述列表
\begin{description}
    \item[术语1] 定义1
    \item[术语2] 定义2
\end{description}
```

---

## 📐 数学公式

### 行内公式

```latex
% 方法1：$ ... $
这是一个行内公式 $E = mc^2$。

% 方法2：\( ... \)
这是一个行内公式 \(a^2 + b^2 = c^2\)。
```

### 独立公式

```latex
% 方法1：$$ ... $$（无编号）
$$
E = mc^2
$$

% 方法2：equation环境（有编号）
\begin{equation}
    E = mc^2
\end{equation}

% 引用公式：\label 和 \ref
\begin{equation}
    E = mc^2 \label{eq:einstein}
\end{equation}
根据方程 \ref{eq:einstein}，我们知道...
```

### 多行公式

```latex
% align环境（每行编号）
\begin{align}
    a &= b + c \\
    d &= e + f + g
\end{align}

% align*环境（无编号）
\begin{align*}
    a &= b + c \\
    d &= e + f + g
\end{align*}

% split环境（单个编号）
\begin{equation}
    \begin{split}
        a &= b + c \\
        d &= e + f
    \end{split}
\end{equation}
```

### 数学符号与结构

```latex
% 上下标
$a^2$           % 上标
$a_i$           % 下标
$a_{ij}$        % 多字符下标
$a^2_{ij}$      % 同时有上下标

% 分数
$\frac{a}{b}$           % 分数
$\dfrac{a}{b}$          % 显示大小分数

% 根号
$\sqrt{x}$              % 平方根
$\sqrt[n]{x}$           % n次根

% 求和、积分、乘积
\sum_{i=1}^{n} a_i      % 求和
\int_0^1 f(x) dx        % 积分
\prod_{i=1}^{n} a_i     % 乘积
\lim_{x \to 0} f(x)     % 极限

% 矩阵
\begin{pmatrix}
    a & b \\
    c & d
\end{pmatrix}

% 方程组
\begin{cases}
    x + y = 1 \\
    x - y = 0
\end{cases}
```

### 复杂公式示例

```latex
\documentclass{article}
\usepackage{amsmath}

\begin{document}

\begin{equation}
    f(x) = \begin{cases}
        x^2 & \text{if } x \geq 0 \\
        -x & \text{if } x < 0
    \end{cases}
\end{equation}

\begin{align}
    \text{MSE} &= \frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2 \\
    \text{RMSE} &= \sqrt{\text{MSE}} \\
    R^2 &= 1 - \frac{\sum_{i=1}^{n} (y_i - \hat{y}_i)^2}{\sum_{i=1}^{n} (y_i - \bar{y})^2}
\end{align}

\end{document}
```

---

## 🖼️ 图表与浮动体

### 插入图片

```latex
\documentclass{article}
\usepackage{graphicx}

\begin{document}

% 简单插入
\includegraphics{myfigure.png}

% 带选项的插入
\includegraphics[width=0.8\textwidth]{myfigure.png}
\includegraphics[height=5cm]{myfigure.png}
\includegraphics[scale=0.5]{myfigure.png}

% 浮动图表
\begin{figure}[h]      % h:here, t:top, b:bottom, p:page
    \centering
    \includegraphics[width=0.7\textwidth]{myfigure.png}
    \caption{这是图表标题}
    \label{fig:myfigure}
\end{figure}

引用图表：见图 \ref{fig:myfigure}。

\end{document}
```

### 表格

```latex
\documentclass{article}

\begin{document}

% 简单表格
\begin{tabular}{l|c|r}
    左对齐 & 中心对齐 & 右对齐 \\
    \hline
    内容1 & 内容2 & 内容3 \\
    内容4 & 内容5 & 内容6
\end{tabular}

% 浮动表格
\begin{table}[h]
    \centering
    \caption{这是表格标题}
    \label{tab:mytable}
    \begin{tabular}{|l|c|r|}
        \hline
        列1 & 列2 & 列3 \\
        \hline
        数据1 & 数据2 & 数据3 \\
        数据4 & 数据5 & 数据6 \\
        \hline
    \end{tabular}
\end{table}

引用表格：见表 \ref{tab:mytable}。

\end{document}
```

---

## 📚 参考文献与引用

### 方法1：BibTeX（推荐）

**创建参考文献文件 `references.bib`**：

```bibtex
@article{Einstein1905,
    author = {Albert Einstein},
    title = {On the Electrodynamics of Moving Bodies},
    journal = {Annalen der Physik},
    year = {1905},
    volume = {17},
    pages = {891-921}
}

@book{Knuth1984,
    author = {Donald E. Knuth},
    title = {The TeXbook},
    publisher = {Addison-Wesley},
    year = {1984}
}

@inproceedings{Smith2020,
    author = {John Smith and Jane Doe},
    title = {A New Algorithm for Problem X},
    booktitle = {Proceedings of Conference Y},
    year = {2020},
    pages = {123-135}
}
```

**在LaTeX文档中使用**：

```latex
\documentclass{article}
\usepackage{natbib}

\begin{document}

这是一个引用 \cite{Einstein1905}。

另一种引用形式 \citep{Knuth1984}。

\bibliography{references}
\bibliographystyle{plain}  % 或 ieeetr, apalike 等

\end{document}
```

**编译步骤**：

```bash
# 1. 编译LaTeX源文件
pdflatex document.tex

# 2. 编译BibTeX参考文献
bibtex document

# 3. 再次编译LaTeX（两次）
pdflatex document.tex
pdflatex document.tex
```

### 方法2：直接在文档中

```latex
\begin{thebibliography}{99}
    \bibitem{Einstein1905} Albert Einstein. 
    "On the Electrodynamics of Moving Bodies." 
    Annalen der Physik, 1905.
    
    \bibitem{Smith2020} John Smith.
    "A New Algorithm." 
    Conference Proceedings, 2020.
\end{thebibliography}
```

---

## 🎯 学位论文模板

### 完整的学位论文结构

```latex
\documentclass[12pt]{report}
\usepackage[utf8]{inputenc}
\usepackage{amsmath}
\usepackage{amssymb}
\usepackage{graphicx}
\usepackage{natbib}

\title{我的硕士学位论文题目}
\author{作者名字}
\date{\today}

\begin{document}

% 标题页
\maketitle

% 摘要
\begin{abstract}
这是论文的摘要，总结主要研究内容、方法和成果。
关键词：关键词1，关键词2，关键词3
\end{abstract}

% 目录
\tableofcontents
\listoffigures
\listoftables

% 第一章
\chapter{绪论}

\section{研究背景}
介绍研究问题的背景和意义。

\section{研究现状}
综述相关研究现状。

\section{研究内容}
说明本研究的主要内容。

% 第二章
\chapter{相关工作}

\section{理论基础}
介绍相关理论。

\section{现有方法}
总结现有方法及其优缺点。

% 第三章
\chapter{提出的方法}

\section{方法描述}
详细描述所提方法。

\subsection{模块1}
模块1的详细说明。

\subsection{模块2}
模块2的详细说明。

\section{算法伪代码}
\begin{verbatim}
Algorithm 1: Pseudocode
Input: data
Output: result
1: for each item in data do
2:    process item
3: end for
\end{verbatim}

% 第四章
\chapter{实验与结果}

\section{实验设置}
实验环境、数据集、参数设置。

\section{实验结果}

\begin{table}[h]
    \centering
    \caption{算法性能对比}
    \label{tab:results}
    \begin{tabular}{|l|c|c|c|}
        \hline
        方法 & 准确率 & 速度 & 内存 \\
        \hline
        方法A & 92.3\% & 15ms & 100MB \\
        方法B & 88.5\% & 8ms & 50MB \\
        \hline
    \end{tabular}
\end{table}

\begin{figure}[h]
    \centering
    \includegraphics[width=0.7\textwidth]{results.png}
    \caption{实验结果展示}
    \label{fig:results}
\end{figure}

% 第五章
\chapter{结论与展望}

\section{主要成果}
总结主要创新成果。

\section{存在的问题}
指出当前工作的局限性。

\section{未来工作}
展望后续研究方向。

% 参考文献
\bibliography{references}
\bibliographystyle{ieeetr}

% 附录（可选）
\appendix
\chapter{补充数据}

补充材料和数据。

\end{document}
```

---

## 🎨 高级功能与优化

### 自定义命令与宏

```latex
% 定义自己的命令
\newcommand{\myname}{张三}
\newcommand{\myuniversity}{某大学}

% 在文档中使用
我是 \myname，来自 \myuniversity。

% 带参数的命令
\newcommand{\highlight}[1]{\textbf{\textcolor{red}{#1}}}

% 使用
\highlight{这是重要的部分}
```

### 自定义环境

```latex
\newenvironment{myquote}
{\begin{quote}\itshape}
{\end{quote}}

% 使用
\begin{myquote}
这是一个自定义的引用环境。
\end{myquote}
```

### 颜色与设计

```latex
\usepackage{xcolor}

% 文本颜色
\textcolor{red}{红色文本}

% 背景颜色
\colorbox{yellow}{黄色背景}

% 自定义颜色
\definecolor{myblue}{RGB}{0,100,200}
\textcolor{myblue}{自定义蓝色}
```

### 页面布局

```latex
\usepackage{geometry}

% 设置页边距
\geometry{
    left=2cm,
    right=2cm,
    top=2cm,
    bottom=2cm
}

% 单面/双面打印
\geometry{twoside}
```

---

## 🔍 常见问题与解决方案

| 问题 | 原因 | 解决方案 |
|-----|-----|--------|
| 编译错误 | 语法错误或缺少包 | 检查错误信息，查看日志文件 |
| 公式显示错误 | 数学环境配置不正确 | 使用 `\usepackage{amsmath}` |
| 参考文献不显示 | BibTeX未正确编译 | 按照"参考文献"章节的完整编译步骤 |
| 图片不显示 | 路径错误或格式不支持 | 检查文件路径，使用PNG或PDF格式 |
| 中文显示乱码 | 编码问题 | 添加 `\usepackage[utf8]{inputenc}` |

---

## 🚀 工作流与自动化

### Makefile自动编译

```makefile
TEX = pdflatex
BIB = bibtex
MAIN = document

all: $(MAIN).pdf

$(MAIN).pdf: $(MAIN).tex
	$(TEX) $(MAIN)
	$(BIB) $(MAIN)
	$(TEX) $(MAIN)
	$(TEX) $(MAIN)

clean:
	rm -f *.aux *.bbl *.blg *.log *.out *.toc

view: $(MAIN).pdf
	open $(MAIN).pdf
```

### GitHub Actions自动部署

```yaml
name: LaTeX Build
on: [push]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Compile LaTeX
        uses: xu-cheng/latex-action@v2
        with:
          root_file: document.tex
      - name: Upload PDF
        uses: actions/upload-artifact@v2
        with:
          name: document.pdf
          path: document.pdf
```

---

## 📚 推荐资源

### 官方文档与教程
- [The LaTeX Project](https://www.latex-project.org/)
- [Overleaf学习资源](https://www.overleaf.com/learn)
- [The TeXbook by Donald Knuth](https://www.ctan.org/pkg/texbook)

### 在线工具
- [Detexify](http://detexify.kirelabs.org/) - 符号识别
- [Equation Editor](https://www.codecogs.com/latex/eqneditor.php) - 在线公式编辑
- [LaTeX Table Generator](https://www.tablesgenerator.com/) - 表格生成器

### 社区与论坛
- [TeX Stack Exchange](https://tex.stackexchange.com/) - 问答社区
- [CTAN](https://www.ctan.org/) - 宏包库

---

## ✨ 小结

LaTeX是学术出版的专业工具：

✅ 专业的学术排版效果  
✅ 对复杂数学公式的完美支持  
✅ 自动化文档管理（目录、索引、参考文献）  
✅ 完全可控的格式，重现性强  
✅ 适合大型项目和团队协作

**建议**：从简单的文章开始练习，逐步掌握表格、图片、参考文献等功能，最终能够独立完成学位论文的排版！
