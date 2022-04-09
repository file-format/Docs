{
  "date" : "2022-04-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "HAML File Format - Haml Source Code File",
  "description":"Learn about HAML file format and APIs that can create and open HAML file.",
  "linktitle" : "H",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2022-04-07"
}

## What is an HAML file?

An HAML file is an HTML abstraction markup language file that contains source code written in [Haml](https://haml.info/) language. It can be used as a replacement for the ERB (Ruby template scripts). HAML file contains template source code that for generating the HTML of a web document. ERB files can be replaced by simply replacing these files in the app/views folder to Haml by changing the extension of the file. HAML files can be opened with any text editor such as Microsoft Notepad, Notepad++, Apple TextEdit,

## HAML File Format

HAML files are source files saved to disc as plain text files. It contains code written in HAML syntax. HAML replaces the **<>** tags with the **%** sign to make code simpler and easier. ERB files are drop-in replaceable by HAML as shown in the following simple example.

```
app/views/account/login.html.erb → app/views/account/login.html.haml
```

### HAML Example

The following is an example Hello World example of HAML.

```
%p{:class => "sample", :id => "welcome"} Hello, World!
%p.sample#welcome Hello, World!
```
which renders to the following HTML output.

```
<p class="sample" id="welcome">Hello, World!</p>
```

## References

* [HAML - Github](https://github.com/haml/haml)
