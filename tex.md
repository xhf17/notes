## Tex 
#### Reference: [zhihu](https://www.zhihu.com/question/49681542), [一份其实很短的 LaTeX 入门文档](https://liam.page/2014/09/08/latex-introduction/)
#### About Latex and Tex
* LaTeX 是用 TeX 写的,是指 LaTeX 是使用 TeX 这种宏语言所编写的宏集,并并作为一种格式固定下来。LaTeX 的内核（latex.ltx）就是用 TeX 语言编写的，比如 center 环境就是这样定义的：
    ```
      \def\center{\trivlist \centering\item\relax} 
      \def\endcenter{\endtrivlist}
    ```
    然后下面还能找到 \trivlist 的定义,\centering 的定义,\item 的定义,等等。LaTeX 就是一个“TeX 宏包”，它扩展了 TeX 的功能，使我们很方便的逻辑的进行创作而不是专心于字体，缩进这些烦人的东西。也就是说，每一个LaTeX 命令实际上最后都会被转换解释成几个甚至上百个TeX 命令.整个LaTeX 的代码成千上万的命令，最终会被归结到几百个 TeX primitive 命令中。这就是所谓「LaTeX 是用 TeX 写的」。
* LaTeX 则是 L. Lamport （1941年2月7日 – ） 教授开发的基于 TeX 的排版系统。实际上 LaTeX 利用 TeX 的控制命令，定义了许多新的控制命令并封装成一个可执行文件。这个可执行文件会去解释 LaTeX 新定义的命令成为 TeX 的控制命令，并最终交由 TeX 引擎进行排版。
  * 实际上，LaTeX 是基于一个叫做 plain TeX 的格式的。plain TeX 是高德纳教授为了方便用户，自己基于原始的 TeX 定义的格式，但实际上 plain TeX 的命令仍然十分晦涩。至于原始的 TeX 直接使用的人就更少了，因此 plain TeX 格式逐渐就成为了 TeX 格式的同义词，尽管他们事实上是不同的。
  * 因此在 TeX - LaTeX 组合中，最终进行断行、分页等操作的，是 TeX 引擎；LaTeX 实际上是一个工具，它将用户按照它的格式编写的文档解释成 TeX 引擎能理解的形式并交付给 TeX 引擎处理，再将最终结果返回给用户。

  * 正如 C 语言有不同的编译器一样，实现 TeX 语言的也有不同的程序。不同的实现一般被称为不同的 TeX 引擎，除了 Knuth 最早用 Pascal 语言编写的实现，有后来用 web2c 转换为 C 语言的 web2c 实现，有在 web2c 基础上继续开发得到的 pdfTeX、XeTeX、pTeX、upTeX 等等，还有不依赖于 web2c 重新编写的 LuaTeX、ApTeX 等等。这些 TeX 实现（引擎）各自都有自己的可执行程序，不同程序上也可以执行 Plain TeX、LaTeX、texinfo 等等不同格式（宏代码集）。这些可执行程序通常是通过命令行选项来确定使用哪种格式的及其他功能的，例如对于 TeX Live，编译 LaTeX 文件并输出 PDF 文件可以用：
    ```
      pdftex -fmt=latex foo.tex
    ```
    编译 Plain TeX 文件并输出 PDF 文件可以用:
    ```
      pdftex -fmt=plain foo.tex
    ```
* 关于 LaTeX 的中文支持，首先要说的是：在现在，一切教你使用 CJK 宏包的模板、人、网页、书，都是糟糕的、有害的、恼人的、邪恶的和应该摒弃的。
* XeTeX 原生支持 Unicode，并且可以方便地调用系统字体。可以说解决了困扰中国 TeX 使用者多年的大问题。至此，我们只需要使用几个简单的宏包，就能完成中文支持了。所谓宏包，就是一系列控制序列的合集。这些控制序列太常用，以至于人们会觉得每次将他们写在导言区太过繁琐，于是将他们打包放在同一个文件中，成为所谓的宏包。\usepackage{·}可以用来调用宏包。
* 刘海洋、李清维护的 CTeX 宏集一次性解决了这些问题。CTeX 宏集的优势在于，它适用于多种编译方式；在内部处理好了中文和中文版式的支持，隐藏了这些细节；并且，提供了不少中文用户需要的功能接口。
  **CTeX 宏集和 CTeX 套装是两个不同的东西。CTeX 宏集本质是 LaTeX 宏的集合，包含若干文档类（.cls 文件）和宏包（.sty 文件）。CTeX 套装是一个 TeX 系统。**
#### pdfTeX - pdfLaTeX
* TeX 系统生成的文件是 dvi 格式，虽然可以用其他程序将其转换为例如 pdf 等更为常见的格式，但是毕竟不方便。
  > dvi 格式是为了排版而产生的，它本身并不支持所谓的「交叉引用」，pdfTeX 直接输出 pdf 格式的文档，这也是 pdfTeX 相对 TeX 进步（易用性方面）的地方。二者最主要的差别就是 pdfTeX 直接输出 pdf 格式文档，而 TeX 引擎则输出 dvi 格式的文档。
* pdfLaTeX 这个程序的主要工作依旧是将 LaTeX 格式的文档进行解释，不过此次是将解释之后的结果交付给 pdfTeX 引擎处理。
#### XeTeX - XeLaTeX
* TeX 将每个字符用一个框包括起来（这被称为盒子）然后将一个个的盒子按照一定规则排列起来，因而 TeX 的算法理论上适用于任何字符。为了能让 TeX 系统排版中文，国人曾使用了 天元、CCT、CJK 等手段处理中文。其中天元和CCT现在已经基本不用，CJK 因为使用时间长且效果相对较好，现在还有人使用。
* 不同于 CJK 等方式使用 TeX 和 pdfTeX 这两个不直接支持 Unicode 字符的引擎，XeTeX 引擎直接支持 Unicode 字符。也就是说现在不使用 CJK 也能排版中日韩文的文档了，并且这种方式要比之前的方式更加优秀。XeLaTeX 和 XeTeX 的关系与 pdfLaTeX 和 pdfTeX 的关系类似.使用 XeTeX 引擎需要使用 UTF-8 编码。
#### LuaTeX是正在开发完善的一个 TeX 引擎
#### CTeX - MiKTeX - TeX Live
之前介绍了 TeX, LaTeX, pdfTeX, pdfLaTeX, XeTeX, XeLaTeX, LuaTeX 等，他们都是 TeX 家族的一部分。但是作为一个能够使用的 TeX 系统，仅仅有他们还是不够的。CTeX, MiKTeX, TeX Live 都是被称为「发行」的软件合集。他们包括了上述各种引擎的可执行程序，以及一些文档类、模板、字体文件、辅助程序等等。其中 CTeX 是建立在 MiKTeX 的基础之上的。
#### 总结
TeX - pdfTeX - XeTeX - LuaTeX 都是排版引擎，按照先进程度递增（LuaTeX 尚未完善）。
LaTeX 是一种格式，基于 TeX 格式定义了很多更方便使用的控制命令。上述四个引擎都有对应的程序将 LaTeX 格式解释成引擎能处理的内容。
CTeX, MiKTeX, TeX Live 都是 TeX 的发行，他们是许许多多东西的集合。
#### [addition](https://liam.page/texlive/)
CTeX 套装是科学院吴凌云研究员的个人作品。在 CTeX 套装刚刚问世之时，因其解决了繁琐的中文字体安装工作，所以广受欢迎。但是，一方面 CTeX 套装已经很久不更新，内里的宏包、工具陈旧；另一方面，随着 XeLaTeX 的发展，以及 xeCJK 等技术的成熟，上述这些繁琐的工作已经没有必要而失去意义；因此，现在不推荐使用 CTeX 套装。

虽然它的名字也是「CTeX」，但是 CTeX 宏集和 CTeX 套装是两个不同的东西。CTeX 宏集是集成了中文支持、操作系统判定、字体选择、版式预设为一体的一组宏包和文档类的合集。我们推荐在任何情况下，优先使用 CTeX 宏集处理中文。
#### 发行版


#### 编辑器
