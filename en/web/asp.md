{
  "date" : "2019-10-11",
  "keywords" : [ "asp","asp file", "asp file format", "asp file type", "file", "type", "what is an asp file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "ASP - Active Server Pages File Format",
  "description" : "Learn about what is an ASP file and APIs that can create and open them.",
  "linktitle" : "ASP",
  "menu" : {
    "docs" : {
      "parent" : "web"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is an ASP file?

ASP stands for Active Server Pages which is a development framework for creating web pages. It enables computer code to be executed by an internal server to serve the web requests. When a request is generated for an ASP file by web browser, the server reads the the file and executes any code/script inside it to generate the **[HTML](/web/html/)** result which is returned to the browser for display.

Unlike HTML pages, which are static pages served by the server, ASP files generate dynamic contents at runtime that may involve requests to data from a database. ASP pages typically use the .asp extension rather than .html. Since code/script inside an ASP file is executed on the server side, requesting browser can't see the code used to build the served page. All modern browsers are capable of displaying pages generated as result. Being built on Microsoft technology, pages built with ASP are hosted on Microsoft Internet Information Services (IIS) servers.

## Brief History of ASP File Format
ASP has gone through just few revisions util it was superseded by ASP.NET which is a more modern and more efficient way of developing and managing server side pages. Support for ASP is included by default along with Internet Information Services (IIS). ASP was published in three different versions with improvements in each one.

* ASP 1.0 was released on December 1996 as part of IIS 3.0
* ASP 2.0 was released on September 1997 as part of IIS 4.0
* ASP 3.0 was released on November 2000 as part of IIS 5.0

## ASP Functional Objects

ASP files use server side objects to process user requests and generate output pages to be served to users. Each object has a set of collections, properties and methods for processing requests and responses. These objects include:

### Request Object

When a browser asks for a page from a server, it is called a request. The Request object is used to get information from a visitor.

### Response Object

The ASP Response object is used to send output to the user from the server.

### Server Object

The ASP Server object is used to access properties and methods on the server. It allows connections to databases (ADO), filesystem, and use of components installed on the server.

### Session Object

A session object is like a link between the user's browser requesting a page from server and the server itself. This is achieved by a cookie created by ASP and sent to user's computer. The Session object stores information about, or change settings for a user session. Information is stored in a Session object are shared across all pages of an application. Common information stored in session variables are name, id, and preferences. The server creates a new Session object for each new user, and destroys the Session object when the session expires.

### Application Object

The Application object holds information that will be used by many pages in the application (like database connection information). The information can be accessed from any page. The information can also be changed in one place, and the changes will automatically be reflected on all pages. The Application object is used to store and access variables from any page, just like the Session object.

### ASPError Object

The ASPError object was implemented in ASP 3.0 and is available in IIS5 and laterThe ASPError object is used to display detailed information of any error that occurs in scripts in an ASP page.

**Note:** The ASPError object is created when Server.GetLastError is called, so the error information can only be accessed by using the Server.GetLastError method.

## References

* [ASP - By W3C](https://www.w3schools.com/asp/default.asp)
* [Creating Simple ASP Pages](https://learn.microsoft.com/en-us/previous-versions/iis/6.0-sdk/ms524741(v=vs.90))
