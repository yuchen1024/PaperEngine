### LaTex写作规范

在使用 LaTeX 编写学术文档时, 遵循以下良好习惯和细节可以显著提高效率、减少错误, 并增强代码的可维护性


## 文件组织
* 主文档拆分：使用 \input{} 或 \include{} 将文档按章节拆分为子文件（如 intro.tex, method.tex），便于管理。

* 分类管理资源: 图片放在 figures/ 文件夹, 表格代码可单独存为 tables/

* 绘制图片时需要注意让文字上下左右居中, 避免换行导致文义中断不连贯

* 模板化配置: 将自定义命令、宏包加载等配置单独写入 preamble.tex, 再通过 \input{preamble} 引入主文档. 


## 有意义的标签命名

使用统一前缀标识类型, 如 fig:, tab:, eq:, sec:
* 插图索引的设置模版为\label{figure:XXX}
* 章节索引的设置模版为\label{sec:XXX} or \label{subsec:XXX}, where XXX should not contain spaces

* 自动化引用: 始终使用 \ref{} 和 \eqref{}代替手动编号。

## 缩进与换行

对嵌套环境（如列表、表格、数学公式）进行缩进：
* 段首加粗高亮关键字使用普通列表环境
\begin{trivlist}
	\item \textbf{XXXX.} YYYYYY
\end{trivlist}

* 段落分隔：用空行分隔逻辑段落，避免代码堆积。


## 参考文献管理

* BibTeX/Biblatex：用 .bib 文件管理文献，避免手动输入

* 字段规范化：确保 .bib 文件中的作者、标题、期刊等信息完整且格式统一
suggested naming format of bibitem is author-journal/conference-year

* 引用参考文献前需要加空格: using command ~\cite{XXX}

## 合作与维护
* 文档说明: 在代码开头添加注释说明项目结构、依赖宏包和编译步骤.

* 待办标记: 用 % TODO: 标注未完成内容


通过以上习惯，可以显著提升 LaTeX 文档的可维护性、协作效率和输出质量。对学术写作而言，清晰的代码结构和规范化的引用尤为重要。