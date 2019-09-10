# LaTeX-example
هذه امثلة مأخوذة من مجموعة 
[محبي لاتكس](https://www.facebook.com/groups/latex.fans/)
على الفايسبوك
## Example-1

```latex
\documentclass[12pt,a4paper]{report}
\usepackage[utf8]{inputenc}
\usepackage[top=1cm,bottom=1cm,right=1cm,left=1cm]{geometry}
\usepackage{tikz,contour}
\usetikzlibrary{backgrounds,positioning,shadings}
\newenvironment{theo}[2]{\par\tikzpicture\node [text=white,font=\bfseries](1){\color{white}\contour{gray}{#1}};
\begin{scope}[on background layer]
\draw[double,double distance=1mm] ([xshift=-2mm]1.north west)--(1.north east)
to[bend left=45](1.south east)--([xshift=-4.5mm]1.south west);
\path[fill=#2!90!green] ([xshift=-2mm]1.north west)--(1.north east)
to[bend left=45](1.south east)--([xshift=-5mm]1.south west);
\path[double,right color=#2!90!green,left color=gray,shading angle=70,middle color=#2!90!green!80!black]
([xshift=5mm]1.north west)--([xshift=5mm]1.south west)--++(-10mm,0)--([xshift=-2mm]1.north west)--cycle;
\path [fill=#2!80!black,transform canvas={shift={(-.2mm,-.5mm)}}]([xshift=-5mm]1.south west)--
++(.18,0)--++(-.4,-.4)--cycle;
\path [fill=#2!80!black,transform canvas={shift={(-.05mm,.5mm)}}]([xshift=-2mm]1.north west)--
++(.1,0)--++(0,.25)--cycle;
\end{scope}
\node [fill=#2!5,below right = 1mm and -2mm of 1.south west,align=left,text width=.9\textwidth,inner sep=0mm](2)
\bgroup{\color{#2!90!green}\vrule width 3pt}\hskip3mm \begin{minipage}{\textwidth}\vglue3mm\rightskip=3mm
}{
\par\vskip-1mm\ \end{minipage}\egroup;\endtikzpicture
}
\pagestyle{empty}
\begin{document}
h \begin{theo}{Remarque}{blue!50!green}
text text text text text text text text text text text text text text text text text text text text text 
text text text text text text text text text text text text text text text text text text 
\end{theo}
\begin{theo}{Definition}{red}
text text text text text text text text text text text text text text text text text text text text text
text text text text text text text text text text text text text text text text text text 
\end{theo}
\begin{theo}{Remarque}{blue}
text text text text text text text text text text text text text text text text text text text text text 
text text text text text text text text text text text text text text text text text text 
\end{theo}
\end{document}
```
