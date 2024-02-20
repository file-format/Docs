{
  "date": "2019-12-16",
  "keywords": [
    "NB",
    "file",
    "extension",
    "file format",
    "Mathematica",
    "Spreadsheet"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "description": "Learn about what is an NB file APIs that can create and open NB files.",
  "title": "NB - Mathematica Notebook File Format",
  "linktitle": "NB",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-nb"
    }
  },
  "lastmod": "2021-07-16"
}

## What is an NB file?

A file with .nb extension is a Wolfram notebook file format that saves instructions for mathematical instructions in a textual file. It can contain many different types of data such as live computation, arbitrary dynamic interfaces, full typeset input, image input, automatic code annotation, a complete high-level programmatic interface, and thousands of carefully organized functions and options. The textual instructions are Mathematica input and output that is generated and updated as the input statements are put in the file.

## Wolfram Notebook NB File Format - More Information

Wolfram Notebook NB files are saved in plain textual format which is a human-readable file format. The content of a notebook is arranged in sections as plain text where each is represented by groups of cells, similar to a Spreadsheet. The range of these groups is defined by a bracket towards the end of each cell. The style assigned to a cell determines its role within the notebook as detailed below.

### Notebooks as Wolfram Language

When it is intended to save the Notebook consisting of mathematical instructions for execution by Wolfram Language Kernal, the cells in the document are automatically assigned the `Input` text style. This tells the kernal to consider these as instructions that are executed when user issues a combination of `Shift+Return` keys. A Mathematica Notebook is as shown in the following example.

{{< figure src="../Wolfram Notebook.jpeg" alt="Wolfram Notebook File Format" >}}

### Notebooks as Documents

Mathematica Notebooks can be in document format to give a look of what you see what is what you get (WYSIWYG). These documents are the same as viewed on the screen or on a printed paper, and are interactive. For this, the `Text Style` is assigned to the cell to display the contents without executing the statements by the Kernel.

## Export Mathematica NoteBooks

Mathematica Notebooks can be exported to many different file formats such as PDF, graphics, GIS, Compressed, and Spreadsheets.

## References

* [Mathematica Notebook Basics](https://reference.wolfram.com/language/guide/NotebookBasics.html)
