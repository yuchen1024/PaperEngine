### LaTeX神技


## 文本编辑技巧
* 文字加框: \fbox

* 数学中加方框: \boxed

* 显示行号: 
\usepackage{lineno}
\linenumbers

* 字体控制
font = 
\tiny
\scriptsize
\footnotesize
\small
\normalsize
\large
\Large
\LARGE
\huge
\Huge

* 换行技巧: \\*[0pt]


* enumerate环境设置起点编号: \setcounter{enumi}{6}

* 特殊字符: G\"odel

* 列表环境距离控制: \itemsep 1pt \parskip 0pt \parsep 0pt

* 特殊符号:「 」 


## 插图技巧

* 插图代码块
\begin{figure}[!hbth]
    \vspace*{-0.4em}
    \centering
    \includegraphics[width=2.5in]{Image/GI.png}
\caption{same graph drawn in three different ways}
\end{figure}

* 并排插入两幅图
\begin{figure}
  \centering
  \includegraphics[scale=0.5]{d.jpg}
  \hspace{1in}
  \includegraphics[scale=0.5]{c.jpg}
  \caption{两张图片并排在一个浮动体}
\end{figure}

\begin{figure}
  \begin{minipage}[t]{0.5\linewidth}
    \centering
    \includegraphics[scale=0.5]{d.jpg}
    \caption{Jay}
    \label{fig:side:a}
  \end{minipage}%
  \begin{minipage}[t]{0.5\linewidth}
    \centering
    \includegraphics[scale=0.5]{c.jpg}
    \caption{叶惠美}
    \label{fig:side:b}
  \end{minipage}
\end{figure}



## 表格技巧
* 表格代码块
\begin{table}
\begin{center}
\begin{tabular}{|c|c|c|}

\end{tabular}
\end{center}
\end{table}

* 表格内换行: \makecell[居中情况]{第1行内容 \\ 第2行内容 \\ 第3行内容 ...}

* 表格颜色: \rowcolor{Red}


## Tikz绘图技巧

* 绘图代码块
\begin{center}
\begin{tikzpicture}
\end{tikzpicture}
\end{center}

* 矩形框圆角: rounded corners=0.5cm

* \captionsetup{font=footnotesize}

* \scalebox{0.55}{}

* [scale=0.7, every node/.style={scale=0.7}]

* \draw (msk) [decorate, decoration={brace, raise=12pt, amplitude=10pt}] -- node[midway, yshift=3em] {$XXX$} (pk); 

* node中文字换行: 
\tikzset{
  every text node part/.style={align=center}
}

* 如何让文字跟随线条方向: \draw (nodeA) -- (nodeB) node [midway, above, sloped] (TextNode) {path text};


* 如何画曲线
\path [green, line, bend left] (G) edge (R);
\path [red, bend left, line]   (R) edge (B);
\path [black,line,out=135,in=225] (B) edge (G); 
% you can control the bend by manually specifying in=<angle> and out=<angle> options

* 在node中添加label
\node [label={[xshift=1.0cm, yshift=0.3cm]Label}] {Node};

* 在node下面添加label
\node [label=below:XXX] {Node};


* 对齐方式: anchor=west

## beamer技巧
* beamer中公式上下空白过多的问题
\setlength{\abovedisplayshortskip}{-1pt}
\setlength{\belowdisplayshortskip}{0pt} 

* 分栏
\begin{columns}[onlytextwidth]
\begin{column}{0.4\textwidth}
\end{column}

\begin{column}{0.6\textwidth}
\end{column}
\end{columns}

* 画外音: callout








