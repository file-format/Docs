{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "MASTER File - ASP.NET Master Page File Format",
  "description" : "Learn about MASTER File Format and APIs to create and open MASTER files.",
  "linktitle" : "MASTER",
  "menu" : {
    "docs" : {
      "identifier":"web-master",
      "parent" : "web"
    }
  },
  "lastmod" : "2021-02-29"
}

## What is a MASTER file?

A MASTER file is a master webpage template file created with ASP.NET. It is used as a starting point for creating multiple pages that have the same layout and settings as the MASTER file. The template MASTER file includes settings for header, navigation menus, footer, font and styling information. Using a MASTER file helps create multiple webpages quickly.

You can open a MASTER file using Microsoft Visual Studio 2022 and above.

## MASTER File Format - More Information

A MASTER file is created and saved in HTML file format and is similar to any other webpage file. It is partitioned in editable and non-editable sections. The editable sections are the ones that can be modified to meet user's requirements. The non-editable sections are greyed out when the MASTER file is opened in Microsoft Visual Studio.

Master Pages consist of two pieces i.e. the master page itself and one or more content pages.

### MASTER Page

The master page has .master extension and is made in ASP.NET. It has a predefined layout that comprises of static text, HTMLtags, and server side controls. In ordinary .aspx pages, the @ Page directive is used. In case of .master files, this is replaced by @ Master directive.

### Content Pages

A content page represents the content for the master page's placeholder controls. These are .aspx pages that are actually the code-behind of the master page. Content pages are binded using the @ Page directive by including a MasterPageFile attribute pointing to the master page to be used as shown below.

```
<%@ Page Language="VB" MasterPageFile="~/MasterPages/Master2.master" Title="Content Page of Master File" %>
```

## References

* [ASP.NET Master Pages Overview](https://learn.microsoft.com/en-us/previous-versions/aspnet/wtxbf3hh(v=vs.100))
