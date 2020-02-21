---
title: Pandoc
nav: true
---

# Working with Pandoc

Pandoc can take an myriad of input formats and produce a equally large variety of outputs. 
Under the hood "readers" parse an input format into an internal abstract model from which a "writer" then generates the new output format.
Pandoc aims to make perfect structural conversions from anything that fits within the [Pandoc Markdown syntax](https://pandoc.org/MANUAL.html#pandocs-markdown)--other conversions might involve loss of formatting. 

The [Pandoc User's Guide](https://pandoc.org/MANUAL.html) provides the huge range of options, however, you will probably end up using only a handful of commands. 

## Getting Started

1. On Dillinger, rename your document `test.md` by clicking the "Document Name" area.
2. Download your `test.md` file from Dillinger by clicking "Export as" > "Markdown". 
3. Open a terminal in your Downloads folder. 
    - Windows: open menu and search for "Git Bash" or "powershell" or "CMD"
    - Mac: Applications > Utilities > Terminal, or launch Spotlight (`Command + spacebar`) and type “Terminal”
    - Linux: most likely called "Terminal"
3. In the terminal window, type `pandoc --version` and press return
4. Next, type `pandoc test.md -o test.html` and press return
5. Try `pandoc test.md -o test.docx` (write your draft in Markdown, then submit in `.docx`?)

These examples demonstrate the basic anatomy of Pandoc commands:

`pandoc` + input file name + some option flags + `-o` for output + output file name. 

Pandoc will use the extensions of the input and output file names to guess the markup format.
However, the formats can be specified if necessary, using from `-f` and to `-t` options. 
For example, `pandoc test.md -f markdown -t html -o test.html`.

## PDFs

Creating PDF with Pandoc requires LaTeX installed. 
Pandoc converts the document into LaTeX, then uses LaTeX typesetting engine to output the PDF. 
The first time you create a PDF, your LaTeX distribution's package manager will probably pop up asking you to install new packages multiple times--your first PDF might take awhile!

In terminal, type: `pandoc test.md -o test.pdf` 

The result should be a decent looking PDF (optimized for print).
Try adding a table of contents with the `--toc` option:

`pandoc --toc test.md -o test.pdf`

To start tweaking your PDF layout, you can pass LaTeX variables to Pandoc using the `-V` variable flag (see docs for all [LaTeX variable options](http://pandoc.org/MANUAL.html#variables-for-latex)).
If you know LaTeX, you can get fancy right away and use existing templates.
However, you can also use a few very simple options to spruce up the defaults.
For example, the default margin is very large, so you might want to use:

`pandoc -V geometry=margin=1.25in test.md -o test2.pdf`

This will use the LaTeX package `geometry` to set all the margins to 1.25 inch.

Now try a new font: 

`pandoc -V fontfamily="electrum" -V geometry=margin=1.25in -o test3.pdf test.md`

Font size can be controlled using `-V fontsize=12pt`, however, the default template only supports sizes 10, 11, or 12. 
More sizes are supported using the extsize package (8pt, 9pt, 10pt, 11pt, 12pt, 14pt, 17pt, 20pt) which can be used by adding `-V documentclass=extarticle` plus the desired `fontsize`.

{% include alert.md text="The default LaTeX engine requires specifically prepared fonts (usually stored with a `.sty` extension). See [LaTeX Font Catalogue](https://tug.org/FontCatalogue/) for options. However, figuring out the fonts available on your system, and their correct names can be tricky ([suggestions](https://evanwill.github.io/_drafts/notes/pandoc.html)). " color="warning" %}

## YAML Metadata 

Rather than setting all these options on the commandline, you can simplify by declaring the LaTeX options as metadata at the top of the document instead.
Pandoc uses a [YAML metadata block](https://pandoc.org/MANUAL.html#extension-yaml_metadata_block) for document features such as title, author, and abstract, as well as configuration variables for outputs. 

[YAML](http://www.yaml.org/) is a (*in theory*) human readable plain text data format.
It is added to the top of a documents sandwiched between a line with three hyphens `---` at the top and bottom. 
Variables are mostly key value pairs.

For example, try adding a [metadata](https://pandoc.org/MANUAL.html#metadata-variables) block to your `test.md`, then generate a new PDF:

```
---
title: Test Document
author: A. Great Writer
date: 2020-02-20
abstract: "This test document explores all you need to know about Markdown and Pandoc. Our findings suggest it is possible to create PDFs from Markdown using Pandoc."
---
```

Add [Pandoc LaTeX variables](https://pandoc.org/MANUAL.html#variables-for-latex) in the same way:

```
---
title: Test Document
author: A. Great Writer
geometry: margin=1in
documentclass: extarticle
fontfamily: accanthis
fontsize: 14pt
colorlinks: true
---
```

## Next Steps

- Add [TeX Math in Pandoc Markdown](https://pandoc.org/MANUAL.html#math) 

```
An equation in $E=mc^2$ the sentence.
Or displayed:

$$ x^n + y^n = z^n $$

```

- Code [syntax highlighting](https://pandoc.org/MANUAL.html#syntax-highlighting) 
- [Citations in Pandoc Markdown](https://pandoc.org/MANUAL.html#citations) (connect bibliography file exported from citation manager for automatic citation styles)
- Create [Slide shows](https://pandoc.org/MANUAL.html#producing-slide-shows-with-pandoc)
