---
title: Visual Markdown Demo
nav: Demo
description: The plain text code below demonstrates all the basics--click the button to view how it will look rendered into HTML.
---
<style> #markdown-frame {  } #source { display: block; } #rendered { display: none; }</style>

<button id="toggle" class="btn btn-lg btn-success">Toggle Markdown / Rendered</button> 

<div id="markdown-frame">
<div id="source" markdown="1">

```
# Heading One

Any text with no empty lines between will become a paragraph.
Leave an empty line between headings and paragraphs.

Font can be *Italic* or **Bold**.
Code can be highlighted with `backticks`.
Hyperlinks look like [GitHub Help](https://help.github.com/).
You can add footnotes.[^1]

[^1]: example footnote definition.

## Heading Two

Images look similar:

![alt text here](https://upload.wikimedia.org/wikipedia/commons/4/4b/Focus_ubt.jpeg)

### Heading Three

A bullet list is created using `-`, `*`, or `+` like:

- dog
- cat
- muffin

A numbered list is created using a number + `.` + space, like:

1. one
2. two
6. three
2. four

> Block quote.
> Continuing the quote.

Horizontal rule:

-------

```
</div>

<div id="rendered" markdown="1">

# Heading One

Any text with no empty lines between will become a paragraph.
Leave an empty line between headings and paragraphs.

Font can be *Italic* or **Bold**.
Code can be highlighted with `backticks`.
Hyperlinks look like [GitHub Help](https://help.github.com/).
You can add footnotes.[^1]

[^1]: example footnote definition.

## Heading Two

Images look similar:

![alt text here](https://upload.wikimedia.org/wikipedia/commons/4/4b/Focus_ubt.jpeg)

### Heading Three

A bullet list is created using `-`, `*`, or `+` like:

- dog
- cat
- muffin

A numbered list is created using a number + `.` + space, like:

1. one
2. two
6. three
2. four

> Block quote.
> Continuing the quote.

Horizontal rule:

-------

</div>
</div>


<script>
function markdownToggle() {
    document.getElementById("source").style.display = (document.getElementById("source").style.display === "none") ? "block" : "none";
    document.getElementById("rendered").style.display = (document.getElementById("rendered").style.display === "block") ? "none" : "block";
}
document.getElementById("toggle").onclick = function () { markdownToggle(); };
</script>
