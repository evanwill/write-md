---
title: Resources
nav: true
---

## Markdown Tutorials

- CommonMark [Markdown in 60 seconds](https://commonmark.org/help/) or [10 minute Markdown Tutorial](https://commonmark.org/help/tutorial/)
- [Markdown Guide](https://www.markdownguide.org/)
- [Sustainable Authorship in Plain Text using Pandoc and Markdown](https://programminghistorian.org/en/lessons/sustainable-authorship-in-plain-text-using-pandoc-and-markdown)

## Markdown Reference

- [GitHub markdown flavor](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) (can be used any where on GitHub)
- [Markdown](https://daringfireball.net/projects/markdown/) (original spec Daring Fireball / John Gruber)
- [CommonMark](https://commonmark.org/)
- [kramdown](https://kramdown.gettalong.org/syntax.html) (the Ruby markdown parser used by Jekyll)

## Markdown Tools

- Text editors: you don't need a fancy tool! Markdown can be written by any text editor. For basic writing, Windows [Notepad++](https://notepad-plus-plus.org/), Mac TextEdit, or Linux Gedit are sufficient. For larger projects or notes, a more complete code editor might be helpful such as [Visual Studio Code](https://code.visualstudio.com/).
- Web app editors:
    - [Dillinger](https://dillinger.io/) (sync with cloud services, collaborate, comments, LaTeX Math, UML diagrams, ABC notation for music)
    - [StackEdit](https://stackedit.io/) (sync with cloud services, collaborate, comments, LaTeX Math, UML diagrams, ABC notation for music)
    - [HackMD](https://hackmd.io/) Markdown realtime collaboration platform (self-hosted open source version [CodiMD](https://github.com/hackmdio/codimd))
- Publishing workflows: [Manubot](https://manubot.org/), [Quarto](https://quarto.org/)
- Note taking: [Obsidian](https://obsidian.md/), [Notable](https://notable.md/), [Simplenote](https://simplenote.com/), [Standardnotes](https://standardnotes.org/), [Joplin](https://joplinapp.org/)
- Visual editors: stand alone desktop apps with familiar GUI interface and builtin output options 
    - [Zettlr](https://www.zettlr.com/) (academic oriented, with Zotero support, spellcheck) 
    - [ghostwriter](https://ghostwriter.kde.org/), [Typora](https://www.typora.io/) (oriented towards writers)
- Libraries: the Demo editor uses [markdown-it](https://github.com/markdown-it/markdown-it) library to render Markdown using JS.

## Accessibility 

LaTeX and Pandoc: 

- Pandoc [Accessible PDFs and PDF archiving standards](https://pandoc.org/MANUAL.html#accessible-pdfs-and-pdf-archiving-standards)
- [An introduction to tagged PDF files: internals and the challenges of accessibility](https://www.overleaf.com/learn/latex/An_introduction_to_tagged_PDF_files%3A_internals_and_the_challenges_of_accessibility), Overleaf
- [LaTeX articles about PDF Accessibility](https://www.latex-project.org/publications/indexbytopic/pdf/) (improved accessibility is a focus for the LaTeX3 project, the next version of LaTeX)

Homework and LMS:

- [Making Homework Write-up Accessible](https://create.uw.edu/a11y-in-action/accessible-courses/making-homework-write-up-accessible/) (essentially, use Pandoc to create HTML rather than PDFs), University of Washington
- [Using Pandoc to Convert LaTeX to HTML and MathML](https://sc.edu/about/offices_and_divisions/digital-accessibility/toolbox/math/pandoc/), University of South Carolina
- [LaTeX Accessibility Guide](https://ets.osu.edu/digital-accessibility/latex-accessibility-guide), OSU Engineering
- [Creating Accessible LaTeX Documents](https://libguides.gvsu.edu/LaTeX/accessibility), GVSU Library


--------------------

## Install Pandoc

[Pandoc](https://pandoc.org/) is a command line utility to translate between many formats and generate new output versions, such as PDFs (via LaTeX).

To create PDFs from Markdown, you will need Pandoc plus a LaTeX distribution.
Check the [Installing Pandoc](https://pandoc.org/installing.html) guide for full details. 
Here is the suggested method:

{% capture win %}
1. Download and install a LaTeX distribution. These are big packages so this step can take a long time!
    - For Windows [MiKTeX](https://miktex.org/download)
    - For Mac [BasicTeX](http://www.tug.org/mactex/morepackages.html).
2. Download the latest installer release for your platform from [Pandoc Releases](https://github.com/jgm/pandoc/releases). 
    - For Windows look for the extension `.msi`, e.g. `pandoc-2.10.1-windows-x86_64.msi`
    - For Mac look for the extension `.pkg`, e.g. `pandoc-2.10.1-macOS.pkg`
3. Run the Pandoc installer.
{% endcapture %}
{% include card.html text=win header="Windows and Mac" %}

{% capture lin %}
Pandoc and LaTeX are available in most distro's repositories. 
These might not be most up-to-date versions, but are the best way to install. 

On Ubuntu: `sudo apt install pandoc texlive texlive-fonts-extra texlive-xetex`
{% endcapture %}
{% include card.html text=lin header="Linux" %}

- [Pandoc with GitHub Actions](https://github.com/pandoc/pandoc-action-example)
