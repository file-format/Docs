{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "HTML",
  "description":"Learn about HTML file format and APIs that can create and open HTML files.",
  "linktitle" : "HTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
    }
  },
  "lastmod" : "2019-09-10"
}

HTML (Hyper Text Markup Language) is the extension for web pages created for display in browsers. Known as language of the web, HTML has evolved with requirements of new information requirements to be displayed as part of web pages. The latest variant is known as HTML 5 that gives a lot of flexibility for working with the language. HTML pages are either received from server, where these are hosted, or can be loaded from local system as well. Each HTML page is made up of HTML elements such as forms, text, images, animations, links, etc. These elements are represented by tags and several others where each tag has start and end. It can also embed applications written in scripting languages such as JavaScript and Style Sheets (CSS) for overall layout representation.

## Brief History ##

Since its inception and first role out, the HTML specifications have been maintained by World Wide Web Consortium (W3C) since 1996. In 2000, it also became an international standard (ISO/IEC 15445:2000). In 1999, HTML 4.01 was published. In 2004, the Web Hypertext Application Technology Working Group (WHATWG) started working on the HTML5 version which became a joint deliverable with the W3C in 2008. It was completed and standardized on 28 Oct 2014.

## File Format Structure ##

An HTML 4 document is composed of three parts:

1. a line containing HTML version information
1. a declarative header section
1. a body, which contains the document's actual content. The body may be implemented by the BODY element or the FRAMESET element to contain the body in frames

Each section can be lead or followed by white spaces, newlines, tabs and comments. An example of a simple HTML document is as shown below:

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
   <HEAD>
      <TITLE>Understanding HTML File Format</TITLE>
   </HEAD>
   <BODY>
      <P>Hello World!
   </BODY>
</HTML>
```

### Version Information ###

The first line of code, <!DOCTYPE html>, is called a doctype declaration and tells the browser which version of HTML the page is written in. Depending upon the version of HTML, there are a number of different doctype declarations that names the document type definition (DTD) in use for the document. Each DTD differs from other in the elements it supports and differ as follow:

* HTML 4.01 Strict - includes all elements and attributes that have not been [deprecated](https://www.w3.org/TR/html401/conform.html#deprecated) or do not appear in frameset documents
* HTML 4.01 Transitional - includes everything in the strict DTD plus deprecated elements and attributes (most of which concern visual presentation
* HTML 4.01 Frameset -  includes everything in the transitional DTD plus frames as well

For **HTML5**, the version information is simply as mentioned below.

```
<!DOCTYPE html>
```

### Header Information ###

Header of an HTML document can include a number of HTML elements that are not rendered by the browser. Such elements are either metadata that describe information about the page or includes sections that are used to fetch information from external resources like CSS stylesheets or JavaScript files. Header of a page is represented by the head tag.

For setting page title, the **title** element is the only one that is required within the <head> tags. The same is used by Search engines to identify the title of a page.

### Body Information ###

This is the main section in the file that contains all the contents of the file that are rendered by browsers. Html body can contain markups that can refer to various building blocks in the shape of tags. It can contain several different types of information like text, images, colors, graphics, etc. In addition, audio and video elements can also be embedded in html body for rendering by browsers. In presence of modern style sheets application for visual representation, the presentation attributes of BODY such as background color, link color, text color, etc. have been deprecated. Thus, the same effects can be achieved using stylesheets as shown below:

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Inline Style Sheets referencing</TITLE>
 <STYLE type#"text/css">
  BODY { background: white; color: black}
  A:link { color: red }
  A:visited { color: maroon }
  A:active { color: fuchsia }
 </STYLE>
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>
```

Inline style sheets are easy to embed and for quick applications to the visual effects, external style sheets make it more convenient to deploy once and access at many places.

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Linking to External style sheets</TITLE>
 <LINK rel#"stylesheet" type#"text/css" href#"smartstyle.css">
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>

```

### HTML Elements ###

As mentioned earlier, contents inside HTML Body are represented by tags, also known as Html Elements. Each tag can have additional information in the form of attributes which are written as <tag attribute1#"value1" attribute2#"value2">, though it is not necessary to have attributes with every tag. If attributes are not mentioned, default values are used in each case. Following are some of the Element examples:

#### Header ####

```
<head>
  <title>The Title</title>
</head>
```

#### Headings ####

```
<h1>Heading level 1</h1>
<h2>Heading level 2</h2>
<h3>Heading level 3</h3>
<h4>Heading level 4</h4>
<h5>Heading level 5</h5>
<h6>Heading level 6</h6>
```

#### Paragraphs ####

```
<p>Paragraph 1</p> <p>Paragraph 2</p>
```


## References ##

* [The Global Structure of HTML document](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)
