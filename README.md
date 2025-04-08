# LaTeX 作业模板

自用 LaTeX 模板。

## 项目结构

```
LaTeXHomework/
├── Commented version/       # 带详细注释的模板版本
│   ├── slight.tex           # 主模板文件（带注释）
│   └── figure/              # 图像资源目录
│       ├── badge.pdf        # 封面校徽
│       └── badge-horizonal.pdf  # 页眉校徽
├── No comment version/      # 无注释的模板版本
│   ├── slight.tex           # 主模板文件（无注释）
│   └── figure/
├── test/                    # 测试文件夹（自用）
│   ├── test.tex
│   └── figure/
└── README.md
```

## 使用指南

### 快速开始

1. 选择合适的模板版本：
   - `Commented version` 包含详细注释，下次忘了再学学怎么用
   - `No comment version` 无注释，直接用
2. 修改个人信息：
   打开 `slight.tex` 文件，找到 "个人信息设置区域" 部分（约在 30-40 行），修改以下内容：

   ```tex
   \newcommand{\school}{你的学院}
   \newcommand{\major}{你的年级专业}
   \newcommand{\righthead}{页眉标题}
   \newcommand{\maintitle}{报告主标题}
   \newcommand{\course}{课程名称}
   \newcommand{\teacher}{指导老师}
   \newcommand{\expnumber}{报告编号/类型}
   \newcommand{\name}{你的姓名}
   \newcommand{\id}{你的学号}
   \newcommand{\customdate}{提交日期}   # 也可使用\today自动生成当前日期
   ```

3. 编辑正文内容：
   在文件中 "正文内容开始" 部分后开始编写你的报告内容。

4. 添加参考文献：
   在项目根目录创建一个 `main.bib` 文件，添加你的参考文献信息，然后在文中使用 `\cite{}` 命令引用。

### 编译方法

TeXStudio 真王朝了

## 特殊功能依赖

Python + Pygments（用于代码高亮，minted 包需要）

## 常见问题

1. **编译出错 "cannot run the command"**：

   - 确认已安装 Python 和 Pygments
   - 编译时添加 `--shell-escape` 参数

2. **图片无法显示**：

   - 检查图片路径是否正确
   - 确认图片格式支持（推荐使用 PDF、PNG 或 JPG 格式）

3. **参考文献无法显示**：
   - 确认创建了 main.bib 文件
   - 确认完成了完整的编译流程（pdflatex → bibtex → pdflatex → pdflatex）

##
