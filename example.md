# Example Page Title

## Table of Contents

- [Headings](#headings)
- [Text Formatting](#text-formatting)
- [Links](#links)
- [Images](#images)
- [Lists](#lists)
- [Blockquotes](#blockquotes)
- [Code](#code)
- [Tables](#tables)
- [Media Embeds](#media-embeds)
- [Horizontal Rule](#horizontal-rule)

---

## Headings

# Heading 1
## Heading 2
### Heading 3
#### Heading 4

---

## Text Formatting

This is a normal paragraph. Lorem ipsum dolor sit amet.

**This is bold text**

*This is italic text*

***This is bold and italic***

~~This is strikethrough~~

This is a line with a manual line break  
(two spaces at end of line above)

---

## Links

[Displacement Activities](https://displacementactivities.org)

[Link with a title tooltip](https://displacementactivities.org "Displacement Activities site")

Bare URL: <https://displacementactivities.org>

[Internal anchor link to headings section](#headings)

---

## Images

![Alt text](./images/example.jpg)

Centred image (HTML):

<p align="center">
  <img src="./images/example.jpg" alt="Alt text">
</p>

Image with a link:

[![Alt text](./images/example.jpg)](https://displacementactivities.org)

---

## Lists

Unordered:

- Item one
- Item two
  - Nested item
  - Nested item
- Item three

Ordered:

1. First item
2. Second item
3. Third item

---

## Blockquotes

> This is a blockquote. Useful for pulling out a quote or passage.

> Blockquotes can
> span multiple lines.
>
> And multiple paragraphs.

---

## Code

Inline code: `print("hello")`

Code block:

```python
def hello():
    print("hello world")
```

Plain code block (no syntax highlighting):

```
just plain
preformatted text
```

---

## Tables

| Column One | Column Two | Column Three |
|------------|:----------:|-------------:|
| Left       | Centred    | Right        |
| aligned    | aligned    | aligned      |
| text       | text       | text         |

---

## Media Embeds

Audio (HTML — renders in browser/Jekyll, not VS Code preview):

<audio controls>
  <source src="./audio/example.mp3" type="audio/mpeg">
</audio>

Video (local file):

<video controls width="100%">
  <source src="./video/example.mp4" type="video/mp4">
</video>

YouTube embed (iframe):

<iframe width="560" height="315"
  src="https://www.youtube.com/embed/VIDEO_ID"
  frameborder="0" allowfullscreen>
</iframe>

---

## Horizontal Rule

Three ways to make a rule (all equivalent):

---

***

___

---

## Jekyll Front Matter (if using for DA site posts)

Place this at the very top of the file, above everything else:

```yaml
---
layout: post
title: "Your Post Title"
date: 2026-05-12
categories: [category]
tags: [tag1, tag2]
---
```
