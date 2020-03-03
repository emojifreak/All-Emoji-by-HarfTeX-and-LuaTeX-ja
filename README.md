LaTeX files listing all emoji in Unicode 13.0 by lualatex-dev + luaotfload.sty 3.12 in TeXLive 2019 final.
Note that TeXLive 2019 final and TeXLive 2020 include Noto Color Emoji and Twitter Emoji.
[BXcoloremoji.sty](https://github.com/zr-tex8r/BXcoloremoji) is also needed for compilation.


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
