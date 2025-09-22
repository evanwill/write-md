---
title: Basics of Writing in Markdown
nav: Basics
---

Academic documents are organized using semantic elements such as headings, paragraphs, and lists, which are usually highlighted using different visual features such as font size, font weight, and spacing. 
Rather than intuitively marking up the semantic sections of your writing with visual features, in a markup language we explicitly tag our content using standardized syntax.

Markdown provides a set of basic conventions to mark this semantic structure more formally, while keeping it simple.

Head to the [Demo editor]({{ '/content/5-editor.html' | relative_url }}) or [Dillinger](https://dillinger.io/) web-based editor to practice some Markdown basics.

----------

## Headings
{:.mt-5}

Headings range from level one to six, with one being the most important concepts.
They should move up in order without skipping a level.

Be sure to include a blank line above and below a heading.

{% capture atxtext %}
<div class="row">
<div class="col-md-6" markdown="1">
```
# Heading One

## Heading Two

### Heading Three
```
</div>
<div class="col-md-6 md-demo" markdown="1">
# Heading One

## Heading Two

### Heading Three
</div>
</div>
{% endcapture %}
{% include card.html text=atxtext %}

*Note:* headings using the `#` are called "ATX-style". Less commonly, you may also see "Setext-style" which uses a row of equal signs below heading one and hyphens below heading two, like:

```
Header One
==========

Header Two
----------
```

## Paragraphs
{:.mt-5}

Paragraphs don't require any special markup.
Just leave an empty line between your paragraphs and any other block element.
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
{% include card.html text=par %}

## Lists
{:.mt-5}

A bullet list (i.e. **unordered list**) is created using `-` followed by a space (alternatively can use `*` or `+`).
Put each list item on a new line.
A numbered list (i.e. **ordered list**) is created using a number + `.` followed by a space.
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
<div class="col-md-6 md-demo" markdown="1">
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
<div class="col-md-6 md-demo" markdown="1">
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
<div class="col-md-6 md-demo" markdown="1">
1. dog
    - bark
    - wag
2. cat
    - meow
6. muffin
    - yum
</div>
</div>

------

Note, many platforms will also support to-do lists following the pattern: 

```
- [ ] task one
- [x] completed task
```

{% endcapture %}
{% include card.html text=lists %}

## Inline Elements
{:.mt-5}

{% capture inline %}
<div class="row">
<div class="col-md-6" markdown="1">
```
*Emphasis* or _emphasis_

**Strong** or __strong__

**_Strong and Emphasis_**
```
</div>
<div class="col-md-6 md-demo" markdown="1">
*Emphasis* or _emphasis_

**Strong** or __strong__

**_Strong and Emphasis_**
</div>
</div>
<hr>

```
[hyperlink](https://www.google.com)

image: 

![alt text](https://upload.wikimedia.org/wikipedia/commons/thumb/4/48/Markdown-mark.svg/208px-Markdown-mark.svg.png)
```

[hyperlink](https://www.google.com)

image: 

![alt text](https://upload.wikimedia.org/wikipedia/commons/thumb/4/48/Markdown-mark.svg/208px-Markdown-mark.svg.png)

--------

```
example footnote.[^1]

[^1]: footnote definition will show up at bottom.
```

example footnote.[^1]

[^1]: footnote definition will show up at bottom.

{% endcapture %}
{% include card.html text=inline %}

## Code
{:.mt-5}

{% capture code %}

    Code can be highlighted inline with `backticks`.

    {% raw %}```{% endraw %}
    Or make a code block 
    open with three backticks alone on a line 
    and close with three more on a line. 
    {% raw %}```{% endraw %}

    This makes it easier to copy unformatted code/text

----------------

Code can be highlighted inline with `backticks`.

```
Or make a code block 
open with three backticks alone on a line 
and close with three more on a line. 
```

This makes it easier to copy unformatted code/text

{% endcapture %}
{% include card.html text=code %}

## Tables
{:.mt-5}

Tables aren't supported by all Markdown converters, but can be useful for some quick structure.

{% capture table %}

```
| column1 | column2 | column3 |
| --- | --- | --- |
| value | value | value |
| value | value | value |

```

-----------

{:.table .table-bordered}
| column1 | column2 | column3 |
| --- | --- | --- |
| value | value | value |
| value | value | value |

{% endcapture %}
{% include card.html text=table %}

## Block Quotes
{:.mt-5}

{% capture bq %}
```
> Each line starts with greater-than space.
> Any other markdown can be used.
```

-------

> Each line starts with greater-than space.
> Any other markdown can be used.

{% endcapture %}
{% include card.html text=bq %}

## Horizontal Rule
{:.mt-5}

{% capture hr %}

```
Three or more dashes on a line:

----

```

Three or more dashes on a line:

----

{% endcapture %}
{% include card.html text=hr %}

## Comments
{:.mt-5}

`<!-- you can use HTML comments, they won't show up -->`

{% include alert.html text="Although Markdown is simple, it is important to remember that white space, blank lines, and tabs matter. If you are getting unexpected results when rendering, check your white space!" %}
