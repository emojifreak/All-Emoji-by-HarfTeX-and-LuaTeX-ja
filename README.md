LaTeX files listing all emoji in Unicode 12.0 by

* LuaLaTeX,
* [HarfLaTeX](https://github.com/khaledhosny/harftex), and
* [HarfLaTeX](https://github.com/khaledhosny/harftex) + LuaTeX-ja.

Compilation of LaTeX sources into PDFs requires the latest versions of Segoe UI Emoji (in Windows), [Noto Color Emoji](https://github.com/googlefonts/noto-emoji) and a [TTF version of Twitter Emoji](https://github.com/mozilla/twemoji-colr), otherwise newer emoji are missing in the generated PDFs. They also use [BXcoloremoji](https://github.com/zr-tex8r/BXcoloremoji) for Twitter Emoji.

Easier ways to install HarfLaTeX are uses of

* [TeX Live Contrib Area](https://contrib.texlive.info/), and
* [W32TeX](http://w32tex.org/index.html) which includes HarfLaTeX recently.

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
