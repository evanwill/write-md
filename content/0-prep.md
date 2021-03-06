---
title: Prep
nav: true
--- 

# Prep

The workshop will use a web-based editor to get hands-on with Markdown.
If you want to edit Markdown and make PDFs, you will want to install Pandoc and a text editor. 

## Install Pandoc

[Pandoc](https://pandoc.org/){:target="_blank" rel="noopener"} is a command line utility to translate between many formats and generate new output versions, such as PDFs (via LaTeX).

To create PDFs from Markdown, you will need Pandoc plus a LaTeX distribution.
Check the [Installing Pandoc](https://pandoc.org/installing.html){:target="_blank" rel="noopener"} guide for full details. 
Here is the suggested method:

{% capture win %}
1. Download and install a LaTeX distribution. These are big packages so this step can take a long time!
    - For Windows [MiKTeX](https://miktex.org/download){:target="_blank" rel="noopener"}
    - For Mac [BasicTeX](http://www.tug.org/mactex/morepackages.html){:target="_blank" rel="noopener"}.
2. Download the latest installer release for your platform from [Pandoc Releases](https://github.com/jgm/pandoc/releases){:target="_blank" rel="noopener"}. 
    - For Windows look for the extension `.msi`, e.g. `pandoc-2.10.1-windows-x86_64.msi`
    - For Mac look for the extension `.pkg`, e.g. `pandoc-2.10.1-macOS.pkg`
3. Run the Pandoc installer.
{% endcapture %}
{% include card.md text=win header="Windows and Mac" %}

{% capture lin %}
Pandoc and LaTeX are available in most distro's repositories. 
These might not be most up-to-date versions, but are the best way to install. 

On Ubuntu: `sudo apt install pandoc texlive texlive-fonts-extra texlive-xetex`
{% endcapture %}
{% include card.md text=lin header="Linux" %}

## Markdown Editor

There are many Markdown specific editors and note taking apps (see [Markdown Tools]({{ '/content/4-resources.html#markdown-tools' | relative_url }})).
These often have preview, export, and syncing options built in which can be helpful features. 
However, Markdown can be written by any text editor and most people will probably choose to write in a code editor.

For basic writing, Windows [Notepad++](https://notepad-plus-plus.org/){:target="_blank" rel="noopener"}, Mac TextEdit, or Linux Gedit are sufficient.
For larger projects or notes, a more complete code editor might be helpful.

Open-source cross platform suggestions:

- [Visual Studio Code](https://code.visualstudio.com/){:target="_blank" rel="noopener"} 
    - Preview Markdown: `Ctrl+Shift+V` 
    - Spellcheck: install "Code Spell Checker" extension
    - Extensions: checkout [markdown-preview-enhanced](https://github.com/shd101wyy/markdown-preview-enhanced){:target="_blank" rel="noopener"}
- [Atom](https://atom.io/){:target="_blank" rel="noopener"} 
    - Preview Markdown: `Ctrl+Shift+M` 
    - Spellcheck: comes built in, with cursor on misspelled word, hit `Ctrl+Shift+;` to see suggestions
    - Export: right click preview to "Save as HTML"

Remember to set your indentation to use 4 spaces (rather than tabs).
