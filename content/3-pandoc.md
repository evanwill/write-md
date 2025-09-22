---
title: Working with Pandoc
nav: Pandoc
---

[Pandoc](https://pandoc.org/) is the "universal document converter."
It can take an myriad of input formats and produce a equally large variety of outputs--which is great for writing with Markdown!

For example, you may write an article in Markdown and use Pandoc to:

- convert it into a DOCX for the required final submission format
- export a high quality print PDF (using LaTeX)
- generate an HTML version to paste into a Canvas course

The [Pandoc User's Guide](https://pandoc.org/MANUAL.html) provides the huge range of options, however, you will probably end up using only a handful of commands. 

## Getting Started

Check the [installation documentation](https://pandoc.org/installing.html) for how to get it set up on your computer, or the notes the [Resource section]({{ '/content/4-resources.html#install-pandoc' | relative_url }}).

Download the ["markdown-demo.md"]({{ '/assets/markdown-demo.md' | relative_url }}) file to provide some demo content.

### Open a Terminal 

Pandoc is a commandline application, so to use it you will need to open a terminal: 

- Windows: open menu and search for "Git Bash" or "powershell" or "CMD"
- Mac: Applications > Utilities > Terminal, or launch Spotlight (`Command + spacebar`) and type “Terminal”
- Linux: most likely called "Terminal"

In the terminal window, type `pandoc --version` and press Enter.
If installed correctly, this should output a version number and some information!

In the terminal window, navigate to your Downloads directory, most likely `cd Downloads`, so that you can try some commands on ["markdown-demo.md"]({{ '/assets/markdown-demo.md' | relative_url }}).

### Convert a File

The basic anatomy of a Pandoc command looks like:

`pandoc` + input file name + some option flags + `-o` + output file name

For example: 

- Convert to a DOCX: `pandoc markdown-demo.md -o markdown-demo.docx`
- Convert to HTML: `pandoc markdown-demo.md -o markdown-demo.html`

Pandoc will use the extensions of the input and output file names to guess the markup format.
However, the formats can be specified if necessary, using from `-f` and to `-t` options. 
For example, `pandoc test.md -f markdown -t html -o test.html`.

### Generate a PDF

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

{% include alert.html text="The default LaTeX engine requires specifically prepared fonts (usually stored with a `.sty` extension). See [LaTeX Font Catalogue](https://tug.org/FontCatalogue/) for options. However, figuring out the fonts available on your system, and their correct names can be tricky ([suggestions](https://evanwill.github.io/_drafts/notes/pandoc.html)). " color="warning" %}

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
