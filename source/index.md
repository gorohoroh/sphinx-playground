# Welcome to Alemira LMS documentation!


```{toctree}
   :maxdepth: 3
   :caption: Table of Contents
   
usage/installation.md
usage/usage.md
test_folder/test.md
```

## Useful links
HEllo!!!
* [Using sphinx with Markdown instead of RST](https://stackoverflow.com/questions/2471804/using-sphinx-with-markdown-instead-of-rst)
* [The Executable Book Project](https://executablebooks.org/en/latest/)
* [Using Sphinx](https://www.sphinx-doc.org/en/master/usage/index.html)
* [Sphinx: Getting started](https://www.sphinx-doc.org/en/master/usage/quickstart.html)
* [Sphinx directives](https://www.sphinx-doc.org/en/master/usage/restructuredtext/directives.html)
* [Getting started with MyST](https://myst-parser.readthedocs.io/en/latest/using/intro.html) (a Markdown parser for Sphinx)
* [The MyST Syntax Guide](https://myst-parser.readthedocs.io/en/latest/using/syntax.html)


# Header 1

## Header 2

### Header 3

#### Header 4

##### Header 5

###### Header 6

This is a simple paragraph that lives in this document. It contains *italic* and **bold** words.

Below is a paragraph included from a different file, `myfile.txt`:

```{include} myfile.txt
```

Here's a numbered list:

1. One
1. Two
1. Three

And a bulleted list:

* One
* Two
* Three

And a mixed nested list:

* Item
    1. Subitem 1
    1. Subitem 2
    1. Subitem 3
* One more item


Here's a random quote:

> "What is this product? Why would anyone want it?" These two questions are incredibly challenging for the average technical writer, a group of people much more focused on how than what or why. I've struggled with them many times. But if you can't answer these questions, you need to go back to the research phase, because you don't understand your audience at all.

Here are various admonitions:

```{note}
This is my note.
```

```{warning}
Something went wrong.

Here's what you can do about it:
1. One
2. Two
3. Three
```

```{error}
Something went south completely.
```

This is a simple code block:

```python
print('this is python')
```

This is a code block with additional options (line numbers and line emphasis):

```{code-block} python
:lineno-start: 10
:emphasize-lines: 1, 3

a = 2
print('my 1st line')
print(f'my {a}nd line')
```

This is a simple math block:

$$
a=1
$$

Here's a more complex math block:

```{math} e^{i\pi} + 1 = 0
```


% This is a comment, and it shouldn't be visible in HTML

This is a simple table:

| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

Here's an alternative table syntax:

Markdown | Less | Pretty
--- | --- | ---
*Still* | `renders` | **nicely**
1 | 2 | 3

Editing complex tables in Markdown directly is, however, a subpar experience. However, with Sphinx, you can edit tables in a .csv file and embed the file into your Markdown:

```{csv-table}
   :file: competitors.csv
   :widths: 15, 25, 25, 25
   :header-rows: 1
```

(Not sure why words in tables don't wrap in this theme, but we'll hopefully fix this later.)

Line break:

---
