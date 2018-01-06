[//]: # (qbookmarks/readme.md)

# qbookmarks

## Introduction

This is a pdflatex package for adding bookmarks on to existing PDF files.

## Usage

The usage is so young, so simple and so naïve that you can get a bookmarked PDF file quickly after you type the table-of-contents manually, save, and then run `pdflatex` twice.

A line in the main part of the `.tex` file looks like:
~~~latex
<\ch{CHAPTER_NAME}, PAGE_NUMBER>
<\sec{SECTION_NAME}, PAGE_NUMBER>
<\ch{CHAPTER_NAME}\sec{SECTION_NAME}, PAGE_NUMBER>
~~~

A more complete `.tex` file example:
~~~latex
% arara: pdflatex
% arara: pdflatex
\documentclass{article}
\usepackage{qbookmarks}
\begin{document}
\def\nameofthebook{The_TeXBook.pdf} % name of the input PDF file
<\ch{The TeXbook}, 1> % mark the beginning of a chapter
<\ch{Preface}, 6>
<\ch{Contents}, 9>
<\ch{1 The Name of the Game}, 11>
<\ch{2 Book Printing versus Ordinary Typing}, 13>
% Some more lines
<\ch{I Index}, 467>
<\ch{J Joining the TeX Community}, 493>
\cleanend % copy the rest pages after the last item
\end{document}
~~~
 
## Update History

- 2018.1.6: ver. 2, released on Github
