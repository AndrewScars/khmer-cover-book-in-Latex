# khmer-cover-book-in-Latex
\documentclass[12pt,a4papper]{book}
\usepackage{tkz-euclide}
\usepackage{tikzpeople}
\usetikzlibrary{patterns}
\usetikzlibrary{shapes.callouts}
\usepackage{bbding}
\usepackage{multicol} %brakline
\newcount\n
\def\print#1#2{%
\n=#1%
\ifnum\n<#2%
\advance\n by 1\relax%
\item\ding\n%
\expandafter\print{\n}{#2}%
\fi}
\usepackage{tikz}
\usetikzlibrary{shapes.misc}
\usepackage{fontspec}
\setmainfont{! Learn with ME 22}
\usepackage[T1]{fontenc}
\usepackage[utf8]{inputenc}
\usepackage{ucs}
\usepackage{xltxtra}
\usepackage{newpxmath}
\defaultfontfeatures{Mapping=tex-text}
\setmathrm{Times New Roman}
\newcommand{\en}{\fontspec{Times New Roman}\selectfont}
\newcommand{\kos}{\fontspec[Scale=0.84,Script=Khmer]{Khmer OS System}\selectfont}
\newcommand{\kbk}{\fontspec[Scale=0.84,Script=Khmer]{Khmer OS Bokor}\selectfont}
\newcommand{\kml}{\fontspec[Scale=0.84,Script=Khmer]{Khmer OS Muol Light}\selectfont}
\newcommand{\komp}{\fontspec[Scale=0.84,Script=Khmer]{Khmer OS Muol Pali}\selectfont}
\newcommand{\kb}{\fontspec[Scale=0.84,Script=Khmer]{Khmer OS Battambang}\selectfont}
\newcommand{\km}{\fontspec[Scale=0.84,Script=Khmer]{Khmer M2}\selectfont}
\newcommand{\kps}{\fontspec[Scale=0.84,Script=Khmer]{Khmer M2}\selectfont}
\newcommand{\ks}{\fontspec[Scale=0.84,Script=Khmer]{Khmer S2}\selectfont}
\newcommand{\KR}{\fontspec[Scale=0.84,Script=Khmer]{Kh Rayuth HD 1}\selectfont}
\newcommand{\KPS}{\fontspec[Scale=0.84,Script=Khmer]{Khmer Pen-Surin}\selectfont}
\newcommand{\KT}{\fontspec[Scale=0.84,Script=Khmer]{Khmer Telecommunication}\selectfont}
\newcommand{\LT}{\fontspec[Scale=0.84,Script=Khmer]{! Learn with ME 20}\selectfont}
\newcommand{\KA}{\fontspec[Scale=0.84,Script=Khmer]{Kh Ang Samnadaichas}\selectfont}
\newcommand{\KBS}{\fontspec[Scale=0.84,Script=Khmer]{Khmer OS Classic}\selectfont}
\newcommand{\KATT}{\fontspec[Scale=1,Script=Khmer]{Kh Ang ToaThmor 3}\selectfont}
\newcommand{\KAC}{\fontspec[Scale=1,Script=Khmer]{Kh Ang Chittbous}\selectfont}
\newcommand{\KAK}{\fontspec[Scale=1,Script=Khmer]{Kh Ang Ktomp}\selectfont}
\newcommand{\KACC}{\fontspec[Scale=1,Script=Khmer]{Kh Ang Chittbous}\selectfont}
\usepackage{newpxmath}
\everymath{\color{blue}\displaystyle}
\usepackage{xcolor}
\usepackage{graphicx}
\usepackage{tikz}
\usepackage{enumerate}
\usepackage{enumitem}
\usepackage{tocloft}
\makeatletter %khmer list
\def\@khmernum#1{\expandafter\@@khmernum\number#1\@nil}
\def\@@khmernum#1{%
\ifx#1\@nil
\else
\char\numexpr#1+"17E0\relax
\expandafter\@@khmernum\fi
}
\def\knum#1{\expandafter\@khmernum\csname c@#1\endcsname}
\def\khmernumeral#1{\@@khmernum#1\@nil}
\AddEnumerateCounter{\knum}{\@knum}{}
\makeatother
\makeatletter
\newcommand{\kalph}[1]{% \expandafter\@kalph\csname c@#1\endcsname% } \newcommand{\@kalph}[1]{%
\ifcase#1\or ក\or ខ\or គ\or ឃ\or ង\or ច\or ឆ\or ជ\or ឈ\or ញ\or ដ\or ឋ\or ឌ%
\or ឍ\or ណ\or ត\or ថ\or ទ\or ធ\or ន\or ប\or ផ\or ព\or ភ\or ម\or យ\or រ\or ល%
\or វ\or ស\or ហ\or ឡ\or អ%
\else\@ctrerr\fi%
}
\AddEnumerateCounter{\kalph}{\@kalph}{}
\makeatother
\usepackage{xcolor}
\usepackage{enumitem} %Enlish list
\SetEnumitemKey{1}{leftmargin=,labelsep=1ex,itemsep=1ex,label=\arabic.}
\SetEnumitemKey{a}{leftmargin=,labelsep=1ex,itemsep=1ex,label=\alph.}
\SetEnumitemKey{A}{leftmargin=,labelsep=1ex,itemsep=1ex,label=\Alph.}
\SetEnumitemKey{i}{leftmargin=,labelsep=1ex,itemsep=1ex,label=\roman.}
\SetEnumitemKey{I}{leftmargin=,labelsep=1ex,itemsep=1ex,label=\Roman.}
\SetEnumitemKey{L}{leftmargin=*,labelsep=1ex,itemsep=1ex,label=\NibSolidRight}
\usepackage[many]{tcolorbox}
\usepackage{geometry}
\geometry{top=1.5cm,left=.8cm,right=.8cm,bottom=1.5cm}
\usepackage{fancyhdr}
\pagestyle{fancy}
\def\theenumi{\Roman{enumi}}
\lhead{\textcolor{blue}{\KA {\large រៀបរៀង និង បង្រៀនដោយ \KT ពៅ ពេជ្រពុទ្ធិពង្ស }}}
\lfoot{\textcolor{blue}{\large \KA ទំនាក់ទំនងទូរស័ព្ទលេខ \km ០៩៦ ៧៣ ០០ ៣៩៣}}
\rhead{\color{blue}\Large \KA កម្រង់លំហាត់ជ្រើសរើសកម្រិតវិទ្យាល័យ}
\cfoot{}
\rfoot{\begin{tikzpicture}
\node [draw, rounded rectangle,rounded rectangle arc length=180,magenta,fill=magenta] {{\color{white}\KA ទំព័រទី} \textcolor{white}{\textbf{\large \thepage}}};
\end{tikzpicture}}
\makeatletter
\def\@khmernum#1{\expandafter\@@khmernum\number#1\@nil}
\def\@@khmernum#1{%
\ifx#1\@nil
\else
\KAK
\char\numexpr#1+"17E0\relax
\expandafter\@@khmernum\fi
}
%\def\khmercounter#1{\expandafter\@khmernum\csname c@#1\endcsname}
\renewcommand\@arabic{\@khmernum}% to reset number in \arabic to \khmernum
\renewcommand{\headrulewidth}{0pt}
% \renewcommand{\footrulewidth}{1pt}
\headheight = 30pt
\headsep = 5pt
\footskip =25pt
\usepackage{sectsty} % chapter,section,subsection
\renewcommand{\thesection}{\knum{section}}
\renewcommand{\thesubsection}{\knum{section}.\knum{subsection}}
\sectionfont{ \color{magenta} \KAK}
\subsectionfont{\color{blue} \km}
\subsubsectionfont{\color{cyan} \KA}
\paragraphfont{\color{green} \ks}
%%%%%sec contanc
\newtcolorbox[auto counter,number within=section]{mybox}{
enhanced,
breakable,
arc=2pt,
outer arc=2pt,
rightrule=1.5pt,
toprule=1.5pt,
bottomrule=1.5pt,
leftrule=1.5pt,
colframe=cyan,
colback=magenta!0,
attach boxed title to top left,
boxed title style={colback=blue,arc=0pt,outer arc=0pt,colupper=white}
}
\usetikzlibrary{shapes,shadows,calc}
\usepackage[explicit]{titlesec}
\definecolor{gray}{RGB}{236,236,236}
\newcommand\SecTitle[4]{%
\begin{tikzpicture}
\node[inner xsep=5pt,minimum height=1cm,text width=1\textwidth,
align=right,left color=gray,right color=white, signal to=#1,font=\KAK\Huge,anchor=#2,color=blue]
at (#3,0) {#4};
\end{tikzpicture}%
}
%\titleformat{command}[shape]{format}{label}{sep}{before-code}{after-code}
\titleformat{\section}
{\normalfont}{}{0em}
{\SecTitle{east}{west}{1\paperwidth}{#1}}
\usepackage{fontawesome}
\usepackage{pdflscape}
\usetikzlibrary{patterns}
\usetikzlibrary{calc}
\usetikzlibrary{patterns}
\usetikzlibrary{fadings}
\usetikzlibrary{decorations.shapes}
\usetikzlibrary{shadows}
\pagecolor{white}
\usetikzlibrary{patterns}
\begin{document}
\newpage
\pagecolor{black!60!gray}
\pagestyle{empty}
\begin{landscape}
\begin{tikzpicture}[overlay,remember picture]
\fill[left color=white,right color=pink]
(current page.north west) rectangle ([yshift=-15.5cm,xshift=13.2cm]current page.north east);
\node [red!60!blue] at ($(current page.west)+(41,4)$) {\fontsize{50}{100}\selectfont \KAK លីមីតនៃអនុគមន៍};
\node [white] at ($(current page.west)+(41.2,4)$) {\fontsize{50}{100}\selectfont \KAK លីមីតនៃអនុគមន៍};
\node [blue] at ($(current page.west)+(41,2)$) {\fontsize{35}{100}\selectfont \KAK ភាពជាប់នៃអនុគមន៍};
\node [white] at ($(current page.west)+(41.1,2)$) {\fontsize{35}{100}\selectfont \KAK ភាពជាប់នៃអនុគមន៍};
\node [draw, rounded rectangle,blue,fill=red!50,fill opacity = 0.5] at ($(current page.west)+(27.8,7.3)$) {\fontsize{30}{100}\selectfont \hspace{30cm} \KATT \textbf{ពៅ ពេជ្រពុទ្ធិពង្ស} \hspace{.5cm} d};
\node [yellow] at ($(current page.west)+(42,7.3)$) {\fontsize{30}{100}\selectfont \KATT ពៅ ពេជ្រពុទ្ធិពង្ស };
\node [white] at ($(current page.west)+(41,-2.2)$) {\fontsize{25}{100}\selectfont \KAC មេរៀនសង្ខេប ដំណោះស្រាយគម្រូ};
\node [white] at ($(current page.west)+(41,-4)$) {\fontsize{25}{100}\selectfont \KAC លំហាត់ និង ដំណោះស្រាយ};
\node [white] at ($(current page.west)+(42,-6)$) {\fontsize{25}{100}\selectfont \KAC លំហាត់ សម្រាប់អនុវត្តន៍};
\fillright color=blue,drop shadow,opacity = 0.3 rectangle (26,-15);
\fillright color =yellow,opacity = 0.3,drop shadow rectangle (13.4,-23);
\node [pink] at ($(current page.west)+(46,-13)$) {\fontsize{30}{100}\selectfont \KA ២០២១};
\node [blue!50!red] at ($(current page.west)+(38,-11)$) {\fontsize{30}{100}\selectfont \KA រក្សាសិទ្ធិគ្រប់យ៉ាង};
\node [blue!50!yellow] at ($(current page.west)+(38.03,-11)$) {\fontsize{30}{100}\selectfont \KA រក្សាសិទ្ធិគ្រប់យ៉ាង};
\node [yellow,opacity = 0.3] at ($(current page.west)+(27,-4)$) {\fontsize{120}{100}\selectfont \KATT លីមីត};
\node [gray!50,blue,fill=gray,rotate=90] at ($(current page.west)+(34,5)$) {\fontsize{30}{100}\selectfont \KAK រៀនដើម្បីជាទីពឹង \hspace*{5cm} s};
\end{tikzpicture} 
\end{landscape}
\end{document}
