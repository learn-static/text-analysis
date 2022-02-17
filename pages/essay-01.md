---
title: Essay 1
layout: about
permalink: /essay-01.html
---

{% include feature/nav-menu.html sections="Introduction;Conclusion;Notes" %}

# My Essay Title

## Introduction

Here's some sample text, written in Markdown.
In Markdown, any text with no empty lines between will become a paragraph.

Leave an empty line between headings and paragraphs.

Font can be *Italic* or **Bold**.

Citing your work is important! [^1]

Title sections of your essay with headings, by adding a pound sign (`#`) in front of the title:

# Heading One

## Heading Two

### Heading Three, etc.

Hyperlinks look like this [GitHub Help](https://help.github.com/).

A bullet list is created using `*`, `+`, or `-`, like:

- dog
- cat
- muffin

A numbered list is created using a number + `.`, like:

1. one
2. two
6. three
2. four

A horizontal line break can be useful for separating content:

----

Include an image:

{% include feature/image.html filename="demo_001.jpg" alt="image of UI Admin building" caption="Historic photo of the University of Idaho campus" width="50" %}

Include a pdf:

{% include feature/pdf.html filename="demo_002.pdf" caption="Historic postcard" width="50" %}

## Conclusion

More documentation on how to write your essay in Markdown--as well as how to include images, pdfs, and topic visualizations--can be found at <https://learn-static.github.io/hist-320/topic-modeling.html>.

## Notes

[^1]: Katie Kitamura, A Separation (New York: Riverhead Books, 2017), 25.