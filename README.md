# NJUST Beamer 幻灯片模板

南京理工大学学术报告 Beamer 模板，基于 SimplePlus 主题修改。

## 文件结构

```
├── NJUSTSlides.tex          # 主模板文件
├── README.md                # 本说明文件
├── .latexmkrc               # latexmk 编译配置
└── njustbeamer/             # 资源文件夹
    ├── beamerthemeSimplePlus.sty  # 主题样式
    ├── reference.bib              # 参考文献（示例）
    ├── NJUSTLOGO.jpg              # 校徽（JPG）
    ├── NJUSTtextlogo.png          # 校名横排标志
    └── logo/                      # TikZ 矢量校徽
        ├── NJUST.tex
        └── NJUST2.tex
```

## 编译方法

需要 **XeLaTeX** 编译器。推荐使用以下编译链：

```bash
# 方式一：latexmk（推荐，全自动）
latexmk -xelatex NJUSTSlides.tex

# 方式二：手动编译（含参考文献）
xelatex NJUSTSlides.tex
biber NJUSTSlides
xelatex NJUSTSlides.tex
xelatex NJUSTSlides.tex
```

> **注意**：若无参考文献，可直接 `xelatex NJUSTSlides.tex` 单次编译即可。

### VS Code 编译

安装 [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop) 扩展后，打开 `NJUSTSlides.tex`，点击右上角编译按钮即可。文件首行已包含 `% !TEX program = xelatex` 指示。

## 字体要求

- 中文字体：**微软雅黑** (`Microsoft YaHei`)
- 英文字体：**Arial**
- 等宽字体：**Courier New**

Windows 系统默认已安装上述字体。macOS/Linux 用户请自行安装对应字体或修改 `beamerthemeSimplePlus.sty` 中的字体设置。

## 自定义

1. 修改 `NJUSTSlides.tex` 中的 `\title`、`\author`、`\institute`、`\date` 等信息
2. 替换各 `frame` 内的内容
3. 参考文献放入 `njustbeamer/reference.bib`
4. 如需调整配色，编辑 `njustbeamer/beamerthemeSimplePlus.sty` 中的颜色定义

## 许可

基于 [SimplePlus Beamer Theme](https://github.com/pm25/SimplePlus-BeamerTheme)，Unlicense 许可。
