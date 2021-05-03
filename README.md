## purpose of this package

- You can one line in Chinese, and continue to write the next line in English, which is the translation of the preceding Chinese line
- You can print document only containing Chinese lines
- You can print document only containing English lines
- This package is useful for prepare a bilingual document with single content source but with Chinese/English language form, for example, you can write a Chinese resume with a corresponding translated English resume

## new command

- put the Chinese content in the curly braces of ```\CN{}```
- put the English content in the curly braces of ```\EN{}```
- put the content which should be always printed outside of ```\EN{}``` and ```\CN{}```

## option

you should copy ```languageSelection.sty``` to your work path or use CTAN

- produce English docuemnt: ```\usepackage[Chinese]{languageSelection}```
- produce Chinese document: ```\usepackage[English]{languageSelection}```

in order to get Chinese document

- use following package or documentclass, only one is enough
  - package: ```\usepackage{xeCJK}``` or ```\usepackage{ctex}```
  - documentclass: ```\documentclass{ctexart}```
- compile the document with Xelatex

## example

in the following two examples, the only difference in main.tex is ```\usepackage[Chinese]{languageSelection}``` vs ```\usepackage[English]{languageSelection}```

### Chinese document

main.tex

```tex
\documentclass{ctexart}
\usepackage[utf8]{inputenc}
\usepackage[Chinese]{languageSelection}
\title{test resume}
\begin{document}

\maketitle
\EN{
    \section{Introduction}
}
\CN{
    \section{介绍}
}
\EN{
    You can one line in Chinese, and continue to write the next line in English, which is the translation of the preceding Chinese line 
}
\CN{
    你可以写一行中文，然后写一行对应的英文翻译
}
\end{document}

```

pdf

![cn](image/CN.png)

### English document

main.tex

```tex
\documentclass{ctexart}
\usepackage[utf8]{inputenc}
\usepackage[English]{languageSelection}
\title{test resume}
\begin{document}

\maketitle
\EN{
    \section{Introduction}
}
\CN{
    \section{介绍}
}
\EN{
    You can one line in Chinese, and continue to write the next line in English, which is the translation of the preceding Chinese line 
}
\CN{
    你可以写一行中文，然后写一行对应的英文翻译
}
\end{document}

```

pdf

![EN](image/EN.png)
