---
title: Intro
nav: true
--- 

# Tools for Academic Writing

### Word Processors

- MS Word, [Libre Office](https://www.libreoffice.org/)
- Google Docs
- [Authorea](https://www.authorea.com/) (collaborative platform for academic writing featuring version control, math, data, code, DOIs, etc.)

Issues: 

- WYSIWYG yet "what you see is not what you get"
- [proprietary](https://www.gnu.org/proprietary/proprietary.en.html) tools and formats 
- content and formatting mixed

### Document preparation systems

- [TeX](http://tug.org/) (typesetting)
- [LaTeX](https://www.latex-project.org/) (content markup + typesetting)
- [Overleaf](https://www.overleaf.com/) (LaTeX online platform for collaboration)

Issues:

- complex with steep learning curves
- difficult to collaborate

### Code notebooks

- [R Markdown](https://rmarkdown.rstudio.com/) (with [Bookdown](https://bookdown.org/) for creating larger documents)
- [Jupyter Notebook](https://jupyter.org/) (share with [nbviewer](https://nbviewer.jupyter.org/) or [nbconvert](https://nbconvert.readthedocs.io/en/latest/))

Issues: 

- Language specific
- Dependency hell

### (Lightweight) Markup languages

- [DocBook](https://en.wikipedia.org/wiki/DocBook)
- [AsciiDoc](http://asciidoc.org/)
- [Wikitext](https://en.wikipedia.org/wiki/Help:Wikitext)
- [reStructuredText](http://docutils.sourceforge.net/docs/ref/rst/introduction.html)
- [Textile](https://textile-lang.com/)
- [Markdown](https://daringfireball.net/projects/markdown/) 

Opportunities:

- Simple to learn
- [Plaintext](https://en.wikipedia.org/wiki/Plain_text) and open standards
    - shareable and useable by any device with no special software or license needed
    - preservable / sustainable - easy digital preservation and human readable
    - version controllable - you can use the full power of Git or other version control systems
- Separation of content/semantics and presentation
    - spend less time formatting, more time writing - don't waste time in complex and frustrating formatting in Word that will be deleted by publishers anyway!
    - structure content as data = powerful

Example: 
Karthik Ram, "Git can facilitate greater reproducibility and increased transparency in science", *Source Code Biol Med* 8, 7 (2013), https://doi.org/10.1186/1751-0473-8-7. 
At <https://github.com/karthik/smb_git>

# Markdown

[Markdown](https://daringfireball.net/projects/markdown/) is a quick and simple standard to create formatted documents in plaintext, intended to be easy to write and to read.
Developed in 2004 by John Gruber with Aaron Swartz based on how people intuitively write emails, it is designed to easily convert into HTML for the web.
Because of it's simplicity, it is used by many websites and note taking apps to allow formatting notes, comments, and posts. 

Markdown files are plaintext, usually with the extension `.md`, and can be edited by any text editor.
Think of it as source code for your document, that can be compiled to generate outputs such as HTML, .docx, or PDF.

Markdown comes in "flavors" in specifications or implementations: 

- [CommonMark](https://commonmark.org/) (standardized specification)
- [GitHub Flavored Markdown (GFM)](https://github.github.com/gfm/) (popular style that can be used any where on GitHub and in Jekyll)
- [Pandoc Markdown](https://pandoc.org/MANUAL.html#pandocs-markdown)
- [kramdown](https://kramdown.gettalong.org/syntax.html) (the Ruby markdown parser used by Jekyll)
- [Markdown Extra](https://michelf.ca/projects/php-markdown/extra/) (PHP)
- [MultiMarkdown](https://fletcherpenney.net/multimarkdown/)

Markdown parsers usually allow a mix of other types of markup inside an `.md` file, including LaTeX style math, HTML elements, making it a flexible base to write a document. 
