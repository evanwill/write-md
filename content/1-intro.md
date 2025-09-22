---
title: Tools for Academic Writing
nav: Intro
--- 

Scholarly writing workflows generally center around `.docx` as the defacto standard.
However, traditional word processors are *NOT* the only way to write a paper, and can impose significant limitations on how we collaborate and communicate.
Below we look at some of the options and issues as a frame, before exploring about how Markdown can be used for academic writing.

## Word Processors

- Desktop software: MS Word, [Libre Office](https://www.libreoffice.org/)
- Collaborative cloud platforms: Google Docs, Proton Docs, Nextcloud, ownCloud
- Academic focused platforms: [Authorea](https://www.authorea.com/), [SciFlow](https://www.sciflow.net/en/)

MS Word has been the standard tool for writing academic papers for many years.
However, being familiar and pervasive doesn't mean it is truly easy to use!
Anyone who has spent hours trying to figure out some odd formatting quirk, seen the entire theme disappear when pasting something in, or opened a document from an earlier software version will understand some of the limitations of these platforms.

First, in a [WYSIWYG](https://en.wikipedia.org/wiki/WYSIWYG) editor content and presentation are mixed, semantic structure of the document is easy to confuse with styling.
Formatting is hidden in the interface and can be difficult to sort out, meaning often "what you see is not what you get" and you can't figure out why.

Second, MS Word is a [proprietary](https://www.gnu.org/proprietary/proprietary.en.html) tool linked to proprietary formats.
Tools like Google Docs are proprietary platforms with unclear privacy, security, and ownership.
These situations presents challenges to collaboration, innovation, and sustainability.

## Document Preparation Systems

- Software: [LaTeX](https://www.latex-project.org/) ([ConTeXt](https://wiki.contextgarden.net/Main_Page), [LuaTeX](https://www.luatex.org/), or others that build on top of [TeX](https://tug.org/))
- Visual editor: [TeXstudio](https://www.texstudio.org/) 
- Collaborative cloud platforms: [Overleaf](https://www.overleaf.com/)

LaTeX is a system to separates the plain text content of your writing from the actual document design / typesetting presentation.

TeX and LaTeX have long been the standard for academic writing in fields that need to represent mathematical equations.
They are extremely powerful for creating PDF/print documents, but are complex with steep learning curves which can make collaboration difficult. 
The source code of LaTeX documents are not necessarily easy to read or preview until compiled.

Importantly, LaTeX was designed for high quality *PRINT* preparation--unfortunately this means the PDFs it generates are often not accessible by default and might not be the best for digital distribution.
If you are creating PDFs for courses or learning management systems, you will need to carefully ensure it meets accessibility requirements!

Some new alternatives have been developing, such as [Typst](https://typst.app/).

## Code Notebooks

- [R Markdown](https://rmarkdown.rstudio.com/) (with [Bookdown](https://bookdown.org/) for creating larger documents)
- [Jupyter Notebook](https://jupyter.org/) (share with [nbviewer](https://nbviewer.jupyter.org/) or [nbconvert](https://nbconvert.readthedocs.io/en/latest/))
- [Quarto](https://quarto.org/) (scientific publishing focus, with Python, R, Julia, or Observable code written in notebooks)

If you are writing about research involving code and visualizations, code notebooks are a great option. 
These systems integrate Markdown (or other lightweight markup language) with code blocks to create documents with live or rendered code.
However, they are situated in ecosystems that require language specific skills, and can result in "dependency hell" if not correctly packaged, which are issues for sharing and sustainability. 

## Lightweight Markup languages

Lightweight markup languages seek to be easy to write and read, while providing expressive semantic markup that can be used to transform the marked up content into different formats.
Some popular examples (other than Markdown) include:

- [Wikitext](https://en.wikipedia.org/wiki/Help:Wikitext)
- [AsciiDoc](http://asciidoc.org/)
- [reStructuredText](http://docutils.sourceforge.net/docs/ref/rst/introduction.html)
- [Org-Mode](https://orgmode.org/)
- [Textile](https://textile-lang.com/)

Opportunities:

- Simple(ish) to learn
- [Plaintext](https://en.wikipedia.org/wiki/Plain_text) and open standards -based
    - shareable and useable by any device with no special software or license needed
    - preservable / sustainable - easy digital preservation and human readable
    - version controllable - you can use the full power of Git or other version control systems
- Separation of content/semantics and presentation
    - spend less time formatting, more time writing - don't waste time in complex and frustrating formatting in Word that will be deleted by publishers anyway!
    - structure content as data = powerful
- Flexible outputs - ready for web, ebooks, blogs, not just PDFs.

Example: 
Karthik Ram, "Git can facilitate greater reproducibility and increased transparency in science", *Source Code Biol Med* 8, 7 (2013), https://doi.org/10.1186/1751-0473-8-7. Available at <https://github.com/karthik/smb_git>

# Markdown

[Markdown](https://daringfireball.net/projects/markdown/) is a quick and simple standard to create formatted documents in plaintext.

Originally developed in 2004 by John Gruber with Aaron Swartz based on how people intuitively write emails, it focuses on being human readable, yet designed to easily convert into HTML for the web.

Markdown files are plaintext, usually with the extension `.md`, and can be edited by any text editor.
Think of it as source code for your document, that can be compiled to generate outputs such as HTML, .docx, or PDF.

Because of it's simplicity and flexibility, a growing number of websites, note taking apps, publishing systems, and code notebooks use Markdown to format content, making it a powerful, cross-platform option for academic and tech writing. 

## Flavors

It is important to keep in mind that Markdown isn't a formal standard, but comes in "flavors" from various specifications or implementations that add additional features. 
Some common flavors:

- [CommonMark](https://commonmark.org/) (standardized specification)
- [GitHub Flavored Markdown (GFM)](https://github.github.com/gfm/) (popular style that can be used any where on GitHub and in Jekyll)
- [R Markdown](https://rmarkdown.rstudio.com/){:target="_blank" rel="noopener"} (RStudio's mix of R code blocks and Markdown)
- [kramdown](https://kramdown.gettalong.org/syntax.html) (the Ruby markdown parser used by Jekyll)
- [Pandoc Markdown](https://pandoc.org/MANUAL.html#pandocs-markdown) (document-centric extensions)

One of the benefits of these various Markdown parsers is that they usually allow a mix of other types of markup inside an `.md` file, including LaTeX style math, HTML elements, and code blocks making it a flexible base to write an academic document in an efficient manner.
