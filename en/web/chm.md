{
  "date" : "2019-10-11",
  "keywords" : [ "chm","chm file", "chm file format", "chm file type", "file", "type", "what is a chm file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "CHM - Compiled HTML Help File Format",
  "description" : "Learn about what is an CHM file and APIs that can create and open them.",
  "linktitle" : "CHM",
  "menu" : {
    "docs" : {
      "parent" : "web"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is a CHM file?

The CHM file format represents Microsoft **[HTML](/web/html/)** help file that consists of a collection of HTML pages. It provides an index for quick accessing the topics and navigation to different parts of the help document. The CHM file can be searched for contents via the provided search option. CHM is Microsoft Proprietary online help file format that is often used for software documentation. In addition, it is used in several other applications like training guides, interactive books, and electronic newsletters. Most of the modern Microsoft Development environments support generating CHM documentation from information available in the application.

The unique ability of CHM file format to implement a combined table of contents and index makes it distinct over other standard HTML pages. The generated CHM file is relatively small in size and, hence, can easily be distributed with software packages. The help authoring tool, HTML Help Workshop, provides an easy-to-use system for creating and managing help projects and their related files. CHM files may include text, images, and hyperlinks; viewable in a Web browser; used by Windows and other programs as an online help solution.

## CHM File Format

The final form of generated CHM file depends on how the help system is designed and whether it is destined for an application or a web site. A CHM file supports data compression with LZX compression to generate the compressed HTML files. It has the built-in search engine for quick searching of contents along with the capability to merge multiple .CHM files. A CHM file consists of a set of HTML files, a linked Table of contents and an index file.

### HTML Files

Whether you are creating help topics for distribution with a program, or on the Web, the documents you author are created using a special formatting language known as Hypertext Markup Language (HTML). HTML topic files have a .htm or .html file name extension.

Although each help topic or Web page you author appears to be a document with text, graphics, or animated images on it, .htm files are actually text documents that have special HTML formatting codes. These codes, called tags, tell a browser how to display each page. Only the text that appears in a topic or Web page is actually in the .htm file. Any graphics, sounds, animated images, or other elements that appear are separate files that your HTML file points to. The browser copies or downloads the graphics, sounds, or other elements when it sees the tags telling it to do so.

### Table of Contents (TOC)
The help table of contents (.hhc) file is an HTML file that contains the topic titles for your table of contents. When a user opens the table of contents in a compiled help file (or on a Web page) and clicks a topic title, the HTML file associated with that title will open.

### Index File
The index (.hhk) file is an HTML file that contains the index entries (keywords) for your index. When a user opens the index in a compiled help file, or on a Web page, and clicks a keyword, the HTML file associated with the keyword will open.

## HTML Help Components

HTML Help is made up of several components. These include the following:

* `HTML Help Workshop`: a help authoring tool with an easy-to-use graphical interface for creating project files, HTML topic files, contents files, index files, and everything else you need to put together an online help system or Web site.
* `HTML Help ActiveX control`: a small, modular program used to insert help navigation and secondary window functionality into an HTML file.
* `The HTML Help Viewer`: a fully-functional and customizable three-paned window in which online help topics can appear.
* `Microsoft HTML Help Image Editor`: an online graphics tool for creating screen shots; and for converting, editing, and viewing image files.
* `The HTML Help Java Applet`: a small, Java-based program that can be used instead of an ActiveX control to insert help navigation into an HTML file.
* `The HTML Help executable program`: the program that displays and runs help when you click a compiled help file.
* `The HTML Help compiler`: the program that compiles project, contents, index, topic, and other files into a compiled help file.
* `The HTML Help Authoring Guide`: an online guide designed to assist help authors in using HTML Help to design a help system. The guide also contains a complete HTML Help reference for developers and an HTML tag reference for authors.

## References

* [Microsoft HTML Help](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/htmlhelp/microsoft-html-help-1-4-sdk)
* [Microsoft Compiled HTML Help](https://en.wikipedia.org/wiki/Microsoft_Compiled_HTML_Help)
