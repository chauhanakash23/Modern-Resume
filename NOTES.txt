Resume Notes:
-Use English-sounding names to get more callbacks/interviews. This happened because of a well-documented/researched phenomenon called name discrimination/bias. 

-Avoid using color/low-contrast color as much as possible to increase readability/avoid hiring bias. Though a color or two is probably fine.

-According to this study, https://onlinelibrary.wiley.com/doi/abs/10.1002/ejsp.2026, adding middle initial to name makes you seem more intelligent.

-Name file FirstName_LastName_Resume.pdf (or FirstName_MiddleInitial_LastName_Resume.pdf) to make it easier for employers to distinguish your resume. Underscore instead of space helps prevent incompatibility processing the file. 


Change Log:
Use CTRL + F to find exact code in file


-Changed section color to blue (145a7d)
File: resume.tex
Code: Changed hex color.
\definecolor{awesome}{HTML}{145a7d} 


-Changed section color to fully covered instead of partially covered
File: resume.tex
Code: Added new code. 
\makeatletter
\def\@sectioncolor{\color{awesome}}
\makeatother


-Changed darktext, graytext, lightext, and text to fully black (000000) to make it easier to read
File: resume.tex
Code: Changed code.
% Text types are in order except lighttext
 \definecolor{darktext}{HTML}{000000}
 \definecolor{graytext}{HTML}{000000}
 \definecolor{text}{HTML}{000000}
% Lighttext is for the address
 \definecolor{lighttext}{HTML}{000000} 
 
 
-Added link to footer
File: resume.tex
Code: Added new code. 
\usepackage{hyperref}
------------------
Code: Changed code.
\makecvfooter
 {\today}
 {\href{https://www.overleaf.com/read/dmpwdjzqddwd}{Awesome CV~~~·~~~Resume}}
 {\thepage}
  
-Changed font styles from italics and small capitals to regular/upright
File: awesome-cv.cls
Code: Removed all \slshape and \scshape from code. 


-Added ability to make bulleted columns
File: resume.tex
Code: Added code
\usepackage{multicol}
---------------------
File: relevant coursework.tex in resume folder
Code: Code template for making bulleted columns
\begin{minipage}[t]{.5\linewidth}
  \begin{cvitems}
    \item Software Engineering
    \item Neural Networks
    \item Image Processing
  \end{cvitems}
\end{minipage}%
\begin{minipage}[t]{.5\linewidth}
  \begin{cvitems}
    \item Articifial Intelligence
    \item Basketweaving
    \item Lightsaber Fighting
    
-Removed , after \honorpositionstyle{#1} from /cvhonor 
File:awesome-cv.cls
Code: Changed code
  \honordatestyle{#4} & \honorpositionstyle{#1} \honortitlestyle{#2} & \honorlocationstyle{#3} \\
}

-I forgot what these are for
File: resume.tex
Code: Added code
\usepackage{tasks}
\usepackage{comment}

-Added comments
