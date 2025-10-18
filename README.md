# iot-practice-report-latex-template
A LaTeX report template based on ACM format for the Internet of Things Engineering Practice course at Beijing University of Posts and Telecommunications.

[![en](https://img.shields.io/badge/lang-en-red.svg)](README.md)
[![zh-CN](https://img.shields.io/badge/lang-zh--CN-green.svg)](README.zh-CN.md)

---

## Quick Start

```bash
# Clone the repository
git clone https://github.com/yibagaozi/iot-practice-report-latex-template.git
cd iot-practice-report-latex-template

# Compile (requires XeLaTeX)
xelatex main.tex
bibtex main
xelatex main.tex
xelatex main.tex
```

## Installation

### macOS

1. **Install MacTeX**
   ```bash
   # Download from https://www.tug.org/mactex/
   # Or use Homebrew
   brew install --cask mactex
   ```

2. **Use TeXShop**
   - Open TeXShop from `/Applications/TeX/`
   - Select `XeLaTeX` from dropdown
   - Click **Typeset**

3. **Configure Chinese Font**
   
   Edit line 15 in `main.tex`:
   ```latex
   \setCJKsansfont{PingFang SC}
   ```

### Windows

1. **Install TeX Live**
   - Download from https://www.tug.org/texlive/

2. **Install TeXstudio** (Recommended)
   - Download from https://www.texstudio.org/

3. **Configure Chinese Font**
   
   Edit line 15 in `main.tex`:
   ```latex
   \setCJKsansfont{Microsoft YaHei}
   % or
   \setCJKsansfont{SimHei}
   ```

### Linux (Ubuntu/Debian)

```bash
# Install TeX Live
sudo apt-get update
sudo apt-get install texlive-full texlive-xetex texlive-lang-chinese

# Install Chinese fonts
sudo apt-get install fonts-noto-cjk

# Install editor
sudo apt-get install texstudio
```

Edit line 15 in `main.tex`:
```latex
\setCJKsansfont{Noto Sans CJK SC}
```

## Project Structure

```
iot-practice-report-latex-template/
├── README.md              # English documentation
├── README.zh-CN.md        # Chinese documentation
├── main.tex               # Main LaTeX file
├── references.bib         # Bibliography database
├── images/                # Image folder
│   ├── logo.png           # University logo
│   └── demo.jpg           # Demo image
```

## Compilation

### Command Line

```bash
# Clean old files
rm main.aux main.bbl main.blg main.out

# Compile
xelatex main.tex
bibtex main
xelatex main.tex
xelatex main.tex
```

**Important**: Must use `xelatex`, not `pdflatex`!

### TeXShop (macOS)

1. Open `main.tex`
2. Select `XeLaTeX` from dropdown menu
3. Click **Typeset**
4. Run BibTeX: **Macros** → **BibTeX**
5. Click **Typeset** twice more

### TeXstudio (Windows/Linux)

1. **Options** → **Configure TeXstudio** → **Build**
2. Set **Default Compiler** to `XeLaTeX`
3. Set **Default Bibliography Tool** to `BibTeX`
4. Press **F5** to compile

## Contact

For questions or suggestions, please open an issue on GitHub.

---

**Repository**: https://github.com/yibagaozi/iot-practice-report-latex-template

**Last Updated**: 2025-10-18