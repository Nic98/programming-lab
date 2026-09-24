# Programming Lab

面向课堂的 Python / IGCSE Pseudocode / AS Pseudocode 三模式编辑器。

**在线使用：<https://nic98.github.io/programming-lab/>**

直接进入：[IGCSE 0478](https://nic98.github.io/programming-lab/?mode=igcse) · [AS 9618](https://nic98.github.io/programming-lab/?mode=as) · [Python](https://nic98.github.io/programming-lab/?mode=python)

## 使用

- 在编辑器标题栏选择 Python、IGCSE Pseudocode 或 AS Pseudocode，再点击 **Run**。
- 点击标题栏 **+** 新增空白代码标签页；每种语言的标签页分别保存。单击标签切换，再次单击当前标签改名；双击任意标签也可改名。标签名就是 **Save** 使用的文件名，多个标签可左右滚动。
- 程序执行到输入语句时，在 **Console** 中输入并提交。
- **Ctrl / ⌘ S** 保存到当前浏览器；工具栏 **Save** 下载代码文件：伪代码为 `.txt`，Python 为 `.py`。
- 三个工作区分别保存源码、虚拟文件和测试。浏览器存储请配合文件备份使用。
- **Examples** 提供 16 组三种写法的核心示例、6 个 Python 扩展示例及 3 个 IGCSE 专题示例。
- 支持追踪、变量查看、虚拟文本文件、自动测试、全屏及拖动分栏。
- 光标位于行首缩进中时，**Backspace** 按四空格缩进级回退。**Full screen** 在小窗口中仅充满当前窗口；窗口已最大化时保留浏览器全屏。

## 编辑与工作区管理

- **New** 与标题栏 **+** 均创建空白标签；**Open** 支持一次打开多个源码文件，每个文件进入新的标签，不覆盖已有代码。同名文件自动添加编号。
- 标签上的 **×** 关闭标签；**⋯** 菜单提供复制、恢复刚关闭的标签、左右移动，也支持拖动排序。每种语言保留最近 20 个关闭标签，刷新后仍可恢复源码、文件和测试；运行结果和撤销记录仅在本次页面会话中保留。
- **Find** 或代码区 **Ctrl / ⌘ F** 打开查找，**Replace** 展开替换。支持大小写、整词、打开查找时的选区范围、前后匹配；Replace all 显示数量，并能在代码区一次 Undo。按 **Escape** 收起工具栏。
- 编辑器底部 **Find / View** 在全屏中同样可用；可开关缩进辅助线、空白字符及伪代码块配对高亮，偏好自动保存。显示辅助不会修正或改变源码。
- 编辑停止约 0.6 秒后自动检查语法：错误位置显示**红色波浪线**，修正后自动消失。悬停红线、点击底部 **1 issue**，或在代码区按 **F8** 查看原因和位置。支持 Python、IGCSE 和 AS；当前先显示检查器发现的第一个问题，修复后继续检查。
- 自动检查不执行代码、不改变 Console 和运行结果；中文输入法组词及运行期间暂停。Python 首次准备需要稍候，之后复用后台检查环境。**Check** 仍可手动检查；检查或运行产生的错误卡和 Console 详情保留。
- **Workspace → Export backup** 下载 `.programming-lab.json`，包含三个语言的所有打开标签、源码、虚拟文件、测试、编辑位置和显示偏好，不包含运行结果或撤销记录。
- **Workspace → Import backup** 校验文件后展示预览，再点 **Add documents** 追加。已有内容保留，重名自动加编号；导入保持本机的主题、字号、分栏和显示偏好。备份文件上限 20 MiB，损坏或不支持的内容会报错，不会静默忽略。

## 旧作业与源码文件

新版使用 `cambridge.programming.lab.v3` 保存多个代码标签页。没有 v3 数据时，优先只读迁移同一浏览器、同一站点保存的 v2；没有 v2 时读取 v1。旧工作区代码恢复为对应语言的首个标签页，v2 / v1 旧键原值均保留，不涉及独立旧版 `pseudocode_editor.html` 的数据。切换语言或标签页不会转换代码。

新建伪代码文件分别命名为 `.igcse.txt` 和 `.as.txt`，Open 会自动选择课程；旧的 `.igcse.pseudo`、`.as.pseudo` 仍可导入。从 Python 打开普通 `.pseudo` 文件时可选择课程，未标注课程的普通 `.txt` 沿用当前语言。

Save 的伪代码文件是 UTF-8 纯文本，兼容 Mac TextEdit 和 Windows 记事本，保留中文、赋值箭头与多行代码。下载副本带编码标记和 Windows 换行，重新导入时自动处理；不会改写编辑区内容。

## 伪代码教学检查

IGCSE、AS 的 Check source、Run、Tests 统一要求关键字大写、四空格块缩进，以及每个执行块有执行语句。变量名、字符串和注释不强制大写；不提供 ELIF，请使用嵌套 IF。

两套伪代码的全部用户标识符均区分大小写：`num`、`Num`、`NUM` 是三个不同名称。变量、常量、参数、过程、函数，以及 AS 记录类型与字段，声明和使用时须保持相同拼写；NEXT 也须与 FOR 计数器名称完全一致。

递减循环须明确写负 STEP，其他非 +1 的等差步长也须写出；零步长或方向背离会报错。FOR 计数器在循环中不可直接或间接修改。需要自行更新时请使用 WHILE。

Format 可修复关键字大小写与缩进，不会改变用户标识符的大小写、补代码或猜步长。已有保存代码原样保留；名称大小写不一致时需自行修正。这些是本编辑器的课堂规范，不代表 Cambridge 只接受这一种排版。

## 离线使用与浏览器

下载本仓库的 `index.html`，即可在支持的桌面浏览器中本地打开。Python 运行环境、格式化器、示例和参考内容均已内嵌，无需 CDN。文件约 19 MB，首次打开在线版时请等待下载完成。

实时 Python 输入需要浏览器支持 JSPI，并通过页面实际的暂停/恢复检测。当前桌面 Chromium 已验证。Zen / Firefox 的兼容说明见页面 **Reference**；GitHub Pages 本身不会改变浏览器能力。不支持实时输入时，不调用 `input()` 的程序仍可运行。未完成真实 iPad / Safari 设备验收。

IGCSE 模式采用 0478 2026–2028 语法；AS 模式保留 9618 2027–2029 语法。Python 模式使用真实 CPython。课程差异、兼容写法与文件教学扩展见 Reference 和 [详细对比](pseudocode_comparison.md)。

## 内嵌依赖

Pyodide 314.0.7 / CPython 3.14.2、autopep8 2.3.2、pycodestyle 2.14.0。许可证与依赖说明见页面 **Reference**。
