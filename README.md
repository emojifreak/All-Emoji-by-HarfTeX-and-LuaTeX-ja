LaTeX files listing all emoji in Unicode 12.1 by lualatex-dev + luaotfload.sty 3.11

Compilation of LaTeX sources into PDFs requires the latest versions of Segoe UI Emoji (in Windows), [Noto Color Emoji](https://github.com/googlefonts/noto-emoji) and a [TTF version of Twitter Emoji](https://github.com/mozilla/twemoji-colr), otherwise newer emoji are missing in the generated PDFs.



One can easily use emoji in a presentation by **LuaLaTeX** like the below. LuaLaTeX can handle color fonts with **RawFeature={+colr}**

```
%\RequirePackage{harfload}
\documentclass[luatex,unicode]{beamer}
\usepackage{fontspec}
\setsansfont{Segoe UI Emoji}[
%  RawFeature={mode=harf;+dist;+ccmp},
  RawFeature={+colr;+dist;+ccmp},
  BoldFont={Segoe UI Bold},
  ItalicFont={Segoe UI Italic},
  BoldItalicFont={Segoe UI Bold Italic}]
\usetheme{Madrid} 

\begin{document}
\begin{frame}{Test😃}
  Test👍\\
  \textbf{Test}👌\\
  \textit{Test}💕
\end{frame}
\end{document}
```
