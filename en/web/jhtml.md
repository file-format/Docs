{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "JHTML - Java HTML File",
  "description":"Learn about JHTML file format and APIs that can create and open JHTML files.",
  "linktitle" : "JHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
    }
  },
  "lastmod" : "2021-06-09"
}

## What is a JHTML file?

A file with .jhtml extension is an [HTML](/web/html/) file with [Java](/programming/java/) code that is executed on server when a client requests this page in a browser. The server processes the requests, executes the Java functions contained in the function, and returns the page to the client's browser. The Java objects embedded in the JHTML pages run on server to handle requests for pages of this type. JHTML files can also access information from database using the JDBC (Java [Database](/database/) Connectivity) connection. JHTML files can be opened in any text editor and viewed in web browsers such as Google Chrome, Firefox, and Safari.

## JHTML File Format

JHTML is a proprietary technology of ATG and may be created using the ATG (Art Technology Group) Dynamo Document Editor. JHTML files are written in plain text file format using the standard HTML and Java code. These contain standard HTML tags in addition to proprietary tags that reference Java objects. When such a page is requested by user, the HTTP server forwards the request to a Java application server. The JHTML page is converted first to .java file and compiled to generate a [.class](/programming/class/) file that is executed as a servlet. This generates a stream of standard HTTP and HTML data that is returned back to requesting browser for display to user. This is helpful to run database related queries on the server and return the finalized accumulated result to client's browser.

## References

* [The Global Structure of HTML document](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)
