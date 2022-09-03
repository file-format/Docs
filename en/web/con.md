{
  "date" : "2022-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "CON File - Concept Application Source File Format",
  "description" : "Learn about what is an CON file and APIs that can create and open CON files.",
  "linktitle" : "CON",
  "menu" : {
    "docs" : {
      "identifier":"web-con",
      "parent" : "web"
    }
  },
  "lastmod" : "2022-08-24"
}

## What is a CON file?

A CON file is a source code file for application developed for the **Concept Application Server**. It is used for writing applications for exchange of data between the server and the user. CON files hosted on the server are accessible with a Web browser provided the Concept Client is installed on user end. Concept Application server is a webserver with small scale programming language that may have an [SQL](/database/sql/) subset database engine (TinDB).

CON files can open/run with RadGs Concept Application Server.

## CON File Format - More Information

CON files are hosted on the server and are accessed using web browser on user machine. Concept [URLs](/web/url/) are different than normal HTTP urls and begin with **concept://**.

### CON File URL Example

A CON file hosted on the Concept Application Server can be accessed via web browser using URLs such as:

```
concept://domain.server.com/web_application/main.con.
```
## References

* [Concept Application Server](https://github.com/Devronium/ConceptApplicationServer)
