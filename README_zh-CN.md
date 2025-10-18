# 北京邮电大学物联网工程实践课程 LaTeX 报告模板

基于 ACM 格式的北京邮电大学物联网工程实践课程 LaTeX 报告模板。

[![en](https://img.shields.io/badge/lang-en-red.svg)](README.md)
[![zh-CN](https://img.shields.io/badge/lang-zh--CN-green.svg)](README_zh-CN.md)

---

## 快速开始

```bash
# 克隆仓库
git clone https://github.com/yibagaozi/iot-practice-report-latex-template.git
cd iot-practice-report-latex-template

# 编译（需要 XeLaTeX）
xelatex main.tex
bibtex main
xelatex main.tex
xelatex main.tex
```

## 安装

### macOS

1. **安装 MacTeX**
   ```bash
   # 从 https://www.tug.org/mactex/ 下载
   # 或使用 Homebrew
   brew install --cask mactex
   ```

2. **使用 TeXShop**
   - 从 `/Applications/TeX/` 打开 TeXShop
   - 从下拉菜单选择 `XeLaTeX`
   - 点击 **Typeset** 按钮

3. **配置中文字体**
   
   编辑 `main.tex` 第 15 行：
   ```latex
   \setCJKsansfont{PingFang SC}
   ```

### Windows

1. **安装 TeX Live**
   - 从 https://www.tug.org/texlive/ 下载安装

2. **安装 TeXstudio**（推荐）
   - 从 https://www.texstudio.org/ 下载

3. **配置中文字体**
   
   编辑 `main.tex` 第 15 行：
   ```latex
   \setCJKsansfont{Microsoft YaHei}
   % 或者
   \setCJKsansfont{SimHei}
   ```

### Linux (Ubuntu/Debian)

```bash
# 安装 TeX Live
sudo apt-get update
sudo apt-get install texlive-full texlive-xetex texlive-lang-chinese

# 安装中文字体
sudo apt-get install fonts-noto-cjk

# 安装编辑器
sudo apt-get install texstudio
```

编辑 `main.tex` 第 15 行：
```latex
\setCJKsansfont{Noto Sans CJK SC}
```

## 项目结构

```
iot-practice-report-latex-template/
├── README.md              # 英文文档
├── README.zh-CN.md        # 中文文档
├── main.tex               # 主 LaTeX 文件
├── references.bib         # 参考文献数据库
├── images/                # 图片文件夹
│   ├── logo.png           # 校徽
│   └── demo.jpg           # 示例图片
```

## 编译

### 命令行

```bash
# 清理旧文件
rm main.aux main.bbl main.blg main.out

# 编译
xelatex main.tex
bibtex main
xelatex main.tex
xelatex main.tex
```

**重要**：必须使用 `xelatex`，不能用 `pdflatex`！

### TeXShop (macOS)

1. 打开 `main.tex`
2. 从下拉菜单选择 `XeLaTeX`
3. 点击 **Typeset** 按钮
4. 运行 BibTeX：**宏** → **BibTeX**
5. 再点击两次 **Typeset**

### TeXstudio (Windows/Linux)

1. **选项** → **配置 TeXstudio** → **构建**
2. 设置**默认编译器**为 `XeLaTeX`
3. 设置**默认文献工具**为 `BibTeX`
4. 按 **F5** 编译

## 联系方式

如有问题或建议，请在 GitHub 上提交 issue。

---

**仓库地址**：https://github.com/yibagaozi/iot-practice-report-latex-template

**最后更新**：2025-01-18