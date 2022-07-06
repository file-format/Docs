{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description":"Learn about KIT file format and APIs that can create and open KIT files.",
  "title" : "KIT File Format - CodeKit File",
  "linktitle" : "KIT",
  "menu" : {
    "docs" : {
      "identifier":"web-kit",
      "parent" : "web"
    }
  },
  "lastmod" : "2022-07-04"
}

## What is a KIT file?

A file with .kit extension is an HTML file that is created with the [CodeKit](https://codekitapp.com/) programming language application. It contains `imports` and `variables` in addition to existing [HTML](/web/html/) files, making it ideal for static sites. CodeKit compiles KIT files to HTML that can be readily used as static website files.

## KIT File Format

KIT files are HTML files that additionally include imports and variables. These are stored as plain text files and can be opened with any text editor or web file editors.

### KIT File Imports

Almost any type of file can be imported into a Kit file. Following is the import syntax used to import files into a .kit file.

```
<!-- @import "someFile.kit" -->
<!-- @import "file.html" -->
```

When an import is added to a KIT file and saved, it is replaced with the text of the file being imported. You can also use @include instead of @import.

### Multiple Imports in a KIT file

You may also import more than one file at a time by using a comma-separated list:

```
<!-- @import someFile, otherFile.html, ../thirdFile.kit -->
```

## References

* [What Is Kit?](https://codekitapp.com/help/kit/)
