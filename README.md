
<p align="center">
  <h1>chroma-term-console</h1>
  <a href="https://pypi.org/project/chroma-term-console/"><img src="https://img.shields.io/pypi/v/chroma-term-console.svg" alt="PyPI version"></a>
  <a href="https://pypi.org/project/chroma-term-console/"><img src="https://img.shields.io/badge/Python-3.8~3.14-3776AB?logo=python&logoColor=white" alt="Python"></a>
  <a href="https://github.com/zhenzi0322-package/chroma-term-console/blob/master/LICENSE"><img src="https://img.shields.io/pypi/l/chroma-term-console.svg" alt="License"></a>
  <a href="https://tool.long920.cn/chroma-term-console"><img src="https://app.readthedocs.org/projects/zhenzi0322-tool/badge/?version=latest" alt="Documentation Status"></a>
</p>

> 轻量级 `Python ANSI` 终端色彩库，支持 `4/8/256` 色、`24` 位真 `RGB` 色彩与文本样式，用于控制台文本美化。

## 安装

```bash
pip install chroma-term-console
```

## 快速开始

### Chroma 类（推荐）

最直观的方式，直接 `Chroma.颜色名('文本')` 即可看到彩色输出：

```python
from chroma_term_console import Chroma

# 前景色
print(Chroma.red('错误'))
print(Chroma.green('成功'))
print(Chroma.yellow('警告'))
print(Chroma.blue('信息'))
print(Chroma.magenta('紫红色'))
print(Chroma.cyan('青蓝色'))

# 高亮前景色
print(Chroma.bright_red('高亮红'))
print(Chroma.bright_green('高亮绿'))

# 背景色
print(Chroma.bg_red('红色背景'))
print(Chroma.bg_green('绿色背景'))
print(Chroma.bg_yellow('黄色背景'))

# 显示方式
print(Chroma.bold('粗体'))
print(Chroma.underline('下划线'))
print(Chroma.blink('闪烁'))
print(Chroma.reverse('反显'))

# 组合样式
print(Chroma.bold_red('高亮红色'))
print(Chroma.bold_green('高亮绿色'))
print(Chroma.underline_cyan('下划线青蓝'))

# 256 色
print(Chroma.c256('橙色', fg=208))
print(Chroma.c256('粉色', fg=213))

# 24 位真彩 RGB
print(Chroma.rgb('自定义粉', fg=(255, 121, 198)))
print(Chroma.rgb('暗底亮字', fg=(255, 255, 255), bg=(40, 42, 54)))
```