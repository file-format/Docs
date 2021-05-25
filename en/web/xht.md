{
  "date" : "2021-05-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "XHT",
  "description":"Learn about XHT file format and APIs that can create and open XHT files.",
  "linktitle" : "XHT",
  "menu" : {
    "docs" : {
      "parent" : "web"
    }
  },
  "lastmod" : "2021-05-24"
}

## What is an XHT file?

A file with .xht extension is a web file associated with the [XHTML](/web/xhtml/) (Extended Hypertext Markup Language) file type, which itself is an [XML](/web/xml/) based markup file. Both these files are similar to HTML but have a more stringent XML-like syntax. XHT files are designed in a way to be more structured, involves less scripting, and are generic in addition to using the existing facilities of XML.

## XHT File Format

An XHT file is created and stored as a plain text file with UTF-8 encoding by default. It contains the complete source code of an XHTML document that can be opened and edited with any text editor that supports Unicode encoding. In addition to text editors, XHT file format is understandable by most of the modern web browsers and can be opened using these.

## XHT Example

The following example of an XHT document defines the XML declarations.

```
<!DOCTYPE html
     PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
    "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
  <head>
    <title>Public Property</title>
  </head>
  <body>
    <p>changed to <a href#"http://sample.com/">sample.com</a>.</p>
  </body>
</html>
```

## References ##

* [XHTML<sup>TM</sup> 1.0 The Extensible HyperText Markup Language (Second Edition)](https://www.w3.org/TR/xhtml1/#xhtml)
* [W3C Working Group Note 16 December 2010](https://www.w3.org/TR/2010/NOTE-xhtml2-20101216/introduction.html#s_intro_whatisxhtml2)
* [A History of XHTML: From the 1990s to Today](https://www.brighthub.com/internet/web-development/articles/109224.aspx)
