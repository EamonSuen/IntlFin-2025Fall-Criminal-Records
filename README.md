# 通用学术工作论文 LaTeX 模板 (General Working Paper Template)

本仓库是一个基于 [Chinese-ERJ](https://github.com/EthanDeng/Chinese-ERJ) 修改而来的 LaTeX 模板。

**主要修改：**
原项目是专门针对《经济研究》期刊投稿格式设计的模板。本分支（Fork）在此基础上进行了**通用化改造**，移除了期刊特定的标识和格式限制，使其更适合作为日常撰写 **学术工作论文 (Working Paper)**、课程论文或研讨会文稿的通用底稿。

## 🌟 特点

* **开箱即用**：预设了常用的宏包。
* **工作论文格式**：
    * 页眉已改为 "工作论文" 及 "年份" 样式，而非期刊名称。
    * 保留了中文封面和英文摘要页的双语结构。
* **个人定制**：预填了作者单位及相关基础信息，可随时修改。
* **参考文献**：由于本模板使用了 biblatex 定制《经济研究》的参考文献格式（chinese-erj），用户可以采用安装或者不安装的方式获取 biblatex-gb7714-2015 宏包。

## 🚀 快速开始

### 1. 创建新论文
建议使用 GitHub 的 **Template** 功能直接生成新仓库，而不要直接修改本仓库：
1. 点击页面右上角的绿色的 **"Use this template"** 按钮。
2. 选择 **"Create a new repository"**。
3. 输入你的新论文名称（如 `2025-Fall-CourseWork`）

### 2. 本地编译
下载或克隆你的新仓库后，推荐使用 **TeX Live** 环境进行编译。

**编译链（Build Chain）：** 编译方式可以选择 PDFLaTeX 或者 XeLaTeX，注意一定要在编译过程中运行 biber：

1. xelatex -> biber -> xelatex -> xelatex
2. pdflatex -> biber -> pdflatex -> pdflatex

### 3. 文件结构说明

* **`main.tex`** : 主文档，你的写作主要在这里进行。
* **`erjref.bib`**: 参考文献数据文件，请将 BibTeX 格式的引用数据放入此处。
* **`chinese-erj.cls`**: 格式定义文件（核心样式表），一般无需修改。

## 📝 常用配置修改

打开 `main.tex` 主文件，修改以下部分以适配你的新文章：

```latex
% --- 中文信息 ---
\title{你的论文标题}
\author{作者姓名}
\date{} % 留空则不显示日期，或填入具体日期
\header{工作论文} % 页眉显示的文字

% --- 英文信息 ---
\entitle{Your English Title}
\enauthor{Author Name}
\eninstitute{School of Economics, Jilin University} % 英文单位
```


## 🙏 致谢
本模板基于 EthanDeng/Chinese-ERJ 开发。感谢原作者对《经济研究》LaTeX 模板的贡献。

Last Updated: 2025-12-30.