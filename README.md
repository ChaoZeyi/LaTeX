# LaTeX
因为要准备写文章，而且马上要做数模，都需要用到LaTeX排版，所以花时间入一下门。

### 学习资料

- http://bbs.ctex.org/forum.php?mod=viewthread&tid=48244&page=1#pid337079
- 《LaTeX入门》   刘海洋

### 学习工具

- CTeX组件 + TeXworks
- 在线LaTeX编辑器：ShareLaTeX，https://cn.sharelatex.com/project（可在线编辑，支持行号显示和高亮显示等基本功能，并支持PDF预览，可下载源文件和PDF文件，适合多人合作，支持github，可导入文件进行编辑）
- https://www.codecogs.com/latex/eqneditor.php?lang=zh-cn（输入文字或公式，实时给出LaTeX语法）

### 常用规则

- \命令[可选参数]{参数}
- 注释：%
- \documentclass[UTF8]{ctexart}，用于中文类文章
- \title、\author、\date，表示标题、作者和日期，只有通过\maketitle命令才生效
- \begin{document}、\end{document}，声明document环境，里面是论文的正文部分
- \begin{abstract}摘要内容\end{abstract}
- \bibliographystyle{}，声明参考文献的格式
- \tableofcontents，输出目录
- 使用空行分段，空格没有作用，不需要缩进，不需要编号，都可以自动生成
- \footnote{脚注内容}、\emph{改变字体形状的内容}
- \begin{quote}

​        \zihao{-5}\kaishu    字号：小5，楷书

​        引用内容

​        \end{quote}

​	这里说的正文、摘要、引用指的都是一种环境，\zihao{-5}\kaishu 只对该环境内的内容起作用，或者用一对{}限定作用范围

- 声明定理环境：在导言区做定义：\newtheorem{thm}{定理}，这就定义了一个thm 的环境。

  \begin{thm}[定理名称]

  定理内容

  \end{thm}

- a--b，通常用来表示数字的范围

- 声明公式环境：\begin{equation} 公式内容 \end{equation}，行内公式：美元符 公式 $

  上标：^，下标：_

- 声明图片环境：\usepackage{graphicx} 引入宏包，行内图片：\includegraphics[width=3cm]{aaa.jpg}，浮动图片环境：

   \begin{figure}[ht]  创建图片环境

   \centering  居中
   \includegraphics[scale=0.6]{xiantu.pdf}  插入图片
   \caption{宋赵爽在《周髀算经》注中作的弦图（仿制），该图给出了勾股定理的一个极具对称美的证明。}  自动编号和标题
   \label{fig:xiantu}  标签
   \end{figure}

- 声明表格环境：\usepackage{float}引入宏包

  行内表格：

  \begin{tabular}{|rrr|}   表示只有三列，且右对齐

  \hline      生成表格横线

  直角边$a$ & 直角边$b$ & 斜边$c$ \\\\  该行的内容，以\\\\结束，以&隔开

  \hline

  3 & 4 & 5 \\\\

  5 & 12 & 13 \\\\

  \hline

  \end{tabular}

  浮动表格：

  \begin{table}[h]   创建图片环境

   \centering  居中

  \begin{tabular}{|rrr|}   插入表格

  \hline      

  直角边$a$ & 直角边$b$ & 斜边$c$ \\\\  

  \hline

  3 & 4 & 5 \\\\

  5 & 12 & 13 \\\\

  \hline

  \end{tabular}

   \caption{表名}  自动编号和标题

  \end{table}



