---
title: MD Basics
nav: true
---

# Write Markdown

Head to Dillinger web-based editor to practice some Markdown:

{% include button.md text="Dillinger Editor" link="https://dillinger.io/" %}

- headers
- paragraphs
- metadata yml block
- inline formatting
- lists (bullet, ordered, definition lists) nesting
- hr
- links
- images
- footnotes
- block quote, code blocks
- tables
- Math inline TeX
- writing tips
    - line breaks = better for git
    - citations bibliography .csl file BibTeX
    - `--toc` command


# Text Editor

When working with code you should have a good text editor.
Windows notepad does not handle UTF-8 encoding or UNIX line endings that are standard for cross platform applications. 
For basic editing, Windows [Notepad++](https://notepad-plus-plus.org/), Mac TextEdit, or Linux Gedit are sufficient.
However, a more complete code editor might be helpful.

Open-source cross platform suggestions:

- [Visual Studio Code](https://code.visualstudio.com/) 
    - Preview Markdown: `Ctrl+Shift+V` 
    - Spellcheck: install "Code Spell Checker" extension
    - Extensions: checkout [markdown-preview-enhanced](https://github.com/shd101wyy/markdown-preview-enhanced)
- [Atom](https://atom.io/) 
    - Preview Markdown: `Ctrl+Shift+M` 
    - Spellcheck: comes built in, with cursor on misspelled word, hit `Ctrl+Shift+;` to see suggestions
    - Export: right click preview to "Save as HTML"
