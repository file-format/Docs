{
  "date" : "2021-05-24",
  "keywords" : ["xul", "File", "Extension", "File Format", "File Extension", "XML User Interface Language"],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "XUL - XML User Interface Language File",
  "description":"Learn about XUL file format and APIs that can create and open XUL files.",
  "linktitle" : "XUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
    }
  },
  "lastmod" : "2021-05-24"
}

## What is an XUL file?

A file with a .xul extension ([XUL](https://wiki.mozilla.org/XUL:Home_Page) stands for XML User Interface Language) is an [XML](/web/xml/) based markup language file for creating user interfaces. It was developed by Mozilla for developers to create graphical user interface elements similar to other markup languages used for creating web pages. XUL has been widely in use by Mozilla in its Firefox browser where it used the Mozilla codebase. XUL rendering is carried out using the
[Gecko engine](https://en.wikipedia.org/wiki/Gecko_(software)). Firefox forks such as Pale Moon, Basilisk, and Waterfox retain support for XUL add-ons. XUL files are identified with MIME type: application/vnd.mozilla.xul+xml.

## XUL File Format

XUL files are written in plain text based on XML file format and are rendered using the Gecko engine. The three main parts of a XUL structure are:

 * `Content` - This includes the declarations of the window and the user interface elements contained within them.
 * `Skin` - It includes any style sheets, images and other theme related files. The appearance of a window is described in the style sheets.
 * `Locale` - Text displayed within a window is stored separately and multiple set of language files can be used by users.

### XUL Example

The following example creates three buttons that are stacked on top of each other in vertical direction.

```
<?xml version="1.0"?>
<?xml-stylesheet href="chrome://global/skin/" type="text/css"?>

<window id="vbox example" title="Example 3...."
xmlns="http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul">
  <layout>
    <button id="yes1" label="Yes"/>
    <button id="no1" label="No"/>
    <button id="maybe1" label="Maybe"/>
  </layout>
</window>
```

## References

* [XUL - By Wikipedia](https://en.wikipedia.org/wiki/XUL)
* [XUL Archived Documentation - By Mozilla](https://wiki.mozilla.org/XUL:Home_Page)
* [XUL Planet](https://www.xulplanet.com/tutorials/xultu/)
