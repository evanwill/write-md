---
title: Pandoc
nav: true
---

# Pandoc 

[Pandoc](https://pandoc.org/) is a command line utility to translate between many formats and generate new output versions, such as PDFs (via LaTeX).
The [Pandoc User's Guide](https://pandoc.org/MANUAL.html) provides the huge range of options, however, you will probably end up using only a handful of commands. 

## Install Pandoc

Check the [Installing Pandoc](https://pandoc.org/installing.html) guide for full details. 
To create PDFs from Markdown, you will need Pandoc plus a LaTeX distribution.
Here is the suggested method:

{% capture win %}
1. Download the latest installer release for your platform from [Pandoc Releases](https://github.com/jgm/pandoc/releases). Windows will be `pandoc-2.9.2-windows-x86_64.msi` and Mac `pandoc-2.9.2-macOS.pkg`.
2. Run the Pandoc installer.
3. Download and install a LaTaX distribution. For Windows [MiKTeX](https://miktex.org/download), for Mac [BasicTeX](http://www.tug.org/mactex/morepackages.html). This step can take a long time!
{% endcapture %}
{% include card.md text=win header="Windows and Mac" %}

{% capture lin %}
The easiest method is to use your distro's repositories to install both Pandoc and LaTeX. 
On Ubuntu: `sudo apt install pandoc texlive texlive-fonts-extra texlive-xetex`
{% endcapture %}
{% include card.md text=lin header="Linux" %}

## Getting Started

1. download `.md` file from Dillinger
2. open terminal in your Downloads
3. type: `pandoc --version`
4. type: `pandoc test.md -o test.html`
5. type: `pandoc test.md -o test.pdf` (when you first create a PDF, your LaTeX distro will probably ask you to install some new packages!)
