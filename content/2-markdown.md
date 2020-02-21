---
title: Markdown
nav: true
---

# Write Markdown

Head to Dillinger web-based editor to practice some Markdown:

{% include button.md text="Dillinger Editor" link="https://dillinger.io/" color="success" %}

## Basics  

Academic documents are usually organized using Headers and Paragraphs, which correspond to semantic structure elements even though it is mostly intuitive.

**Headers** can be added in two ways, traditional setext-style or newer ATX-style.
Be sure to include a blank line above and below a header.

{% capture setext %}
<div class="row">
<div class="col-md-6" markdown="1">
```
Header One
==========

Header Two
----------
```
</div>
<div class="col-md-6" markdown="1">
Header One
==========

Header Two
----------
</div>
</div>
{% endcapture %}
{% include card.md text=setext title="Setext-style" %}

Setext style headers are intuitive, however, ATX style provides more control and are much more commonly used. 
ATX headers range from level one to six, with one being the most important.

{% capture atxtext %}
<div class="row">
<div class="col-md-6" markdown="1">
```
# Header One

## Header Two

### Header Three
```
</div>
<div class="col-md-6" markdown="1">
# Header One

## Header Two

### Header Three
</div>
</div>
{% endcapture %}
{% include card.md text=atxtext title="ATX-style" %}

**Paragraphs** don't require any special markup.
For example:

{% capture par %}
```
Any text with no empty lines between will be joined into a paragraph.
Leave an empty line between headings and paragraphs.

Since there is an empty line above, 
this will start a new paragraph.
This gives you the option to write a paragraph all on one line 
(like a word processor),
or to put each sentence on its own line.
Splitting the sentences can make editing and version control easier. 
```

----------------

Any text with no empty lines between will be joined into a paragraph.
Leave an empty line between headings and paragraphs.

Since there is an empty line above, 
this will start a new paragraph.
This gives you the option to write a paragraph all on one line 
(like a word processor),
or to put each sentence on its own line.
Splitting the sentences can make editing and version control easier. 
{% endcapture %}
{% include card.md text=par %}

A **bullet list** is created using `*`, `+`, or `-`, followed by a space.
Put each list item on a new line.
A **numbered list** is created using a number + `.`, followed by a space.
The items will be automatically renumbered correctly in outputs. 
Both kinds of lists can be nested by tabbing in a level.

{% capture lists %}
<div class="row">
<div class="col-md-6" markdown="1">
```
- dog
- cat
- muffin
```
</div>
<div class="col-md-6" markdown="1">
- dog
- cat
- muffin
</div>
</div>
<hr>
<div class="row">
<div class="col-md-6" markdown="1">
```
1. dog
2. cat
6. muffin
1. other thing
```
</div>
<div class="col-md-6" markdown="1">
1. dog
2. cat
6. muffin
1. other thing
</div>
</div>
<hr>
<div class="row">
<div class="col-md-6" markdown="1">
```
1. dog
    - bark
    - wag
2. cat
    - meow
6. muffin
    - yum
```
</div>
<div class="col-md-6" markdown="1">
1. dog
    - bark
    - wag
2. cat
    - meow
6. muffin
    - yum
</div>
</div>
{% endcapture %}
{% include card.md text=lists %}

{% include alert.md text="Although Markdown is simple, it is important to remember that white space, blank lines, and tabs matter. If you are getting unexpected results when rendering, check your white space. For example, leaving two spaces at the end of a line will insert a `<br>` break." color="warning" %}

## Inline Elements

{:.table .table-bordered}
| Markdown | HTML |
| --- | --- |
| `*Emphasis*` or `_emphasis_` | *Emphasis* or _emphasis_ |
| `**Strong**` or `__strong__` | **Strong** or __strong__ |
| `inline [hyperlink](https://www.google.com)` | inline [hyperlink](https://www.google.com) |
| `image ![alt text](https://upload.wikimedia.org/wikipedia/commons/thumb/4/48/Markdown-mark.svg/208px-Markdown-mark.svg.png)` | image ![alt text](https://upload.wikimedia.org/wikipedia/commons/thumb/4/48/Markdown-mark.svg/208px-Markdown-mark.svg.png) |
| `footnote.[^1]` | footnote.[^1] |

`[^1]: example footnote definition.`

[^1]: example footnote definition.

## Block Elements

Here are some more things to try:

```
Code can be highlighted inline with `backticks`.
Or make a code block opening with three backticks alone on a line 
and close with three more on a line. 
Add the language name next to the top backticks for highlighting.

Horizontal rule:

-------------

> Block quote.
> Continuing the quote.

Tables looks like:

| column1 | column2 | column3 |
| --- | --- | --- |
| value | value | value |
| value | value | value |

```
