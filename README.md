# Programming Lab

面向课堂的 Python / IGCSE Pseudocode / AS Pseudocode 三模式编辑器。

**在线使用：<https://nic98.github.io/programming-lab/>**

直接进入：[IGCSE 0478](https://nic98.github.io/programming-lab/?mode=igcse) · [AS 9618](https://nic98.github.io/programming-lab/?mode=as) · [Python](https://nic98.github.io/programming-lab/?mode=python)

## 使用

- 在编辑器标题栏选择 Python、IGCSE Pseudocode 或 AS Pseudocode，再点击 **Run**。
- 程序执行到输入语句时，在 **Console** 中输入并提交。
- **Ctrl / ⌘ S** 保存到当前浏览器；工具栏 **Save** 下载代码文件：伪代码为 `.txt`，Python 为 `.py`。
- 三个工作区分别保存源码、虚拟文件和测试。浏览器存储请配合文件备份使用。
- **Examples** 提供 16 组三种写法的核心示例、6 个 Python 扩展示例及 3 个 IGCSE 专题示例。
- 支持追踪、变量查看、虚拟文本文件、自动测试、全屏及拖动分栏。

## 旧作业与源码文件

首次使用新版会保留并迁移同一浏览器、同一站点保存的 Programming Lab v1 的 Python 和 AS 工作区；旧版保存数据不会被覆盖。IGCSE 是独立新工作区，切换不会转换或覆盖代码。新建伪代码文件分别命名为 `.igcse.txt` 和 `.as.txt`，Open 会自动选择课程；旧的 `.igcse.pseudo`、`.as.pseudo` 仍可导入。从 Python 打开普通 `.pseudo` 文件时可选择课程，未标注课程的普通 `.txt` 沿用当前语言。

Save 的伪代码文件是 UTF-8 纯文本，兼容 Mac TextEdit 和 Windows 记事本，保留中文、赋值箭头与多行代码。下载副本带编码标记和 Windows 换行，重新导入时自动处理；不会改写编辑区内容。

## 伪代码教学检查

IGCSE、AS 的 Check source、Run、Tests 统一要求关键字大写、四空格块缩进，以及每个执行块有执行语句。变量名、字符串和注释不强制大写；不提供 ELIF，请使用嵌套 IF。

递减循环须明确写负 STEP，其他非 +1 的等差步长也须写出；零步长或方向背离会报错。FOR 计数器在循环中不可直接或间接修改。需要自行更新时请使用 WHILE。

Format 可修复大小写与缩进，不会补代码或猜步长。已有保存代码原样保留，不会自动转换；修正后即可再次运行。这些是本编辑器的课堂规范，不代表 Cambridge 只接受这一种排版。

## 离线使用与浏览器

下载本仓库的 `index.html`，即可在支持的桌面浏览器中本地打开。Python 运行环境、格式化器、示例和参考内容均已内嵌，无需 CDN。文件约 19 MB，首次打开在线版时请等待下载完成。

实时 Python 输入需要浏览器支持 JSPI，并通过页面实际的暂停/恢复检测。当前桌面 Chromium 已验证。Zen / Firefox 的兼容说明见页面 **Reference**；GitHub Pages 本身不会改变浏览器能力。不支持实时输入时，不调用 `input()` 的程序仍可运行。未完成真实 iPad / Safari 设备验收。

IGCSE 模式采用 0478 2026–2028 语法；AS 模式保留 9618 2027–2029 语法。Python 模式使用真实 CPython。课程差异、兼容写法与文件教学扩展见 Reference 和 [详细对比](pseudocode_comparison.md)。

## 内嵌依赖

Pyodide 314.0.7 / CPython 3.14.2、autopep8 2.3.2、pycodestyle 2.14.0。许可证与依赖说明见页面 **Reference**。
