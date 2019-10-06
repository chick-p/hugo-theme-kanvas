---
title: "Original Short Code"
date: 2019-10-06
categories:
  - "Development"
  - "golang"
tags:
  - "hugo"
  - "development"
---

## note
This shortcode is an admonition paragraph draws the reader's attention.

{{< highlight go "linenos=table" >}}
{{</* note type="information" */>}}
{{</* /note */>}}
{{< /highlight >}}

**Example:**
{{< note type="information" >}}
Here are the built-in admonition types:

- information
- tips
- warning
{{< /note >}}

## image
This shortcode is to show a image file.
{{< highlight go "linenos=table" >}}
{{%/* img src="cat.jpg"  width="600" height="auto" alt="sample image" */%}}
{{< /highlight >}}

The image file is seeked in same directory with `_index.md` of article.

{{< highlight shell "hl_lines=6" >}}
.
├─ ...
├── content
│   └── blog
│       └── article
│           ├── _index.md
│           └── cat.jpg
├─ ...
{{< /highlight >}}

If not found in same directory, is seeked in directory of `static`.

{{< highlight shell "hl_lines=4" >}}
.
├─ ...
├── static
│   └── cat.jpg
├─ ...
{{< /highlight >}}

**Example:**
{{% img src="../cat.jpg" width="600" height="auto" alt="sample image" %}}
