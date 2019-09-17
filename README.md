[//]: # (bookmarx/readme.md)

# bookmarx

## Introduction

This is a PDFLaTeX package for adding bookmarks on to existing PDF files.

## Usage

Manually type the lines that you want to attach to a PDF file, in the following syntax:
~~~latex
# CHAPTER_NAME	PAGE_NUMBER
	# SECTION_NAME	PAGE_NUMBER
		# SUBSECTION_NAME	PAGE_NUMBER
			......
~~~
Each line comprises some leading tabs (determining the hierarchic depth, same as YAML), a hashtag followed by a space (comment mark in YAML), the caption text (not including tabs), a tab as separator, and the page number (the real and sequential one in the PDF file).

There are two defined macros in this package: `\bookname{...}` selects the input PDF file, and `\bmxlevel{...}` controls how deep the bookmark table is opened.
 
## Update History

- 2018.1.6: v 2, in the name of `qbookmarks`
- 2019.9.17: v 01, renamed as `bookmarx`
