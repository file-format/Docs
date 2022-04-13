{
  "date" : "2022-04-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "RST File Format- reStructuredText File",
  "description":"Learn about RST file format and APIs that can create and open RST files.",
  "linktitle" : "RST",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2022-04-11"
}

## What is an RST file?

An RST file is a technical documentation file format, used primarily in the Python programming community. It is a text file written in the reStructuredText markup language that applies styles and formatting to plain text documents for generation of documentation. RST files use the comments and other information in Python programs code to create technical documentation of the application. However, these can also contain text that can be converted into simple webpages and [eBooks](/ebook/). Text editors such as Github Atom, GNU Emacs (cross-platform), Microsoft Notepad (Windows), Apple TextEdit (Mac) and Vim (Linux) can be used to open RST files.

## RST File Format

RST files contain code that is written in reStructuredText markup language. It is part of the Docutils project of Python Doc-SIG (Documentation Special Interest Group) that provides a set of tools for Python similar to Javadoc for Java. The parser for RST file foramt is embedded in the Docutils and can extract information from Python programs for formatting them into program documentation.

### reStructuredText RST Example

Lets take an example text written in RST file format as follow.

```
================
Document Heading
================

Heading
=======

Sub-heading
-----------

Paragraphs are separated
by a blank line.
```

When this text is input to an rST processor such as Docutils, the output is as follow.

```
<h1>Document Heading</h1>

<h2>Heading</h2>

<h3>Sub-heading</h3>

<p>Paragraphs are separated
by a blank line.</p>
```

## Reference ##

* [reStructuredText - by Wikipedia](https://en.wikipedia.org/wiki/ReStructuredText)
