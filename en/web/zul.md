{
  "date" : "2021-05-24",
  "keywords" : ["zul", "File", "Extension", "File Format", "File Extension", "open"],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "ZUL - ZK User Interface File",
  "description":"Learn about ZUL file format and APIs that can create and open ZUL files.",
  "linktitle" : "ZUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
    }
  },
  "lastmod" : "2021-05-24"
}

## What is a ZUL file?

A file with .zul extension is a web file created with the User Interface Markup Language (ZUML) and contains definitions for user interface elements. Ajax and Java classes support using the [XML](/web/xml/)-based ZUML for developing server side files. ZUL file format was developed by ZK, a UI framework that enables you to build web and mobile applications without the knowledge of JavaScript or AJAX.

## ZUL File Format

ZUL files are XML-based, consisting of different elements to construct user interface. The ZK loader uses each XML element to create a component. The overall processing of the page elements such as page title, description, etc. are described by each XML processing instruction of ZUML.

### ZUL Example

In the following example of ZUML code, the first line specifies the page title, the second line creates a root component with title and border, and the third line creates a button with label and an event listener.

```
<?page title="Super Application"?>
<window title="Super Hello" border="normal">
    <button label="hi" onClick='alert("hi")'/>
```
The ZUL schema can be downloaded from http://www.zkoss.org/2005/zul/zul.xsd.
## References

* [ZUL - By ZK](https://www.zkoss.org/wiki/ZK_Getting_Started/Tutorial)
* [ZUL Schema](http://www.zkoss.org/2005/zul/zul.xsd)
