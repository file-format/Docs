{
  "date": "2019-10-11",
  "keywords": [
    "ashx",
    "file",
    "extension",
    "file format",
    "ASHX",
    "ASP.NET Web Handler File"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "ASHX File Extension - An ASP.NET Web Handler File",
  "description": "Learn about what is an ASHX file and APIs that can create and open ASHX files.",
  "linktitle": "ASHX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ashx"
    }
  },
  "lastmod": "2021-06-10"
}

## What is an ASHX file?

An ASHX file is a webpage that is used by the ASP.NET HTTP Handler to serve user with the pages that are referenced inside this file. The ASP.NET HTTP Handler processes the incoming request, references the pages from the .ashx file, and sends back the compiled page back to the user's browser. The method of processing is mostly similar to that of ASPX files with the differecne that in this case, the referenced pages/documents are processed and sent back.

## ASHX File Format

The .ashx files are saved in plain text file format and contains references to other pages or documents that are sent back to user's browser upon request. These can be opened in any text editor and developer IDEs such as Xamarin Studio, Microsoft Notepad, Notepad++, and many more. The ASHX files are useful in case when you have:
 * Binary files
 * Dynamic image views
 * Performance-critical web pages
 * XML files
 * Minimal web pages

## How to dynamically compile an ASHX file?

The following steps can be used to add and compile an ASHX file using Microsoft Visual Studio.

 * add a Generic handler - Handler1.ashx in visual studio
 * delete the cs file which auto-created.
 * open ashx again,
 ** remove CodeBehind="Handler1.ashx.cs"
 ** add c# code below

```c++
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;

public class Handler1 : IHttpHandler
{
    public void ProcessRequest(HttpContext context)
    {
        context.Response.ContentType = "text/plain";
        context.Response.Write("Hello World2");
    }

    public bool IsReusable
    {
        get
        {
            return false;
        }
    }
}
```
### ASHX Example

The following ASHX code returns the image file to user's request when the ASHX file is called in internet browser.


```C++
<%@ WebHandler Language="C#" Class="QueryStringHandler" %>  

using System;  
using System.Web;  

public class QueryStringHandler : IHttpHandler   
{  
    public void ProcessRequest (HttpContext context)   
    {  
        HttpResponse r = context.Response;  
        r.ContentType = "image/png";  
        string file = context.Request.QueryString["file"];  
        if (file == "Arrow")  
        {  
            r.WriteFile("Arrow.gif");  
        }  
        else  
        {  
            r.WriteFile("Image.gif");  
        }  
    }  

    public bool IsReusable   
    {  
        get  
        {  
            return false;  
        }  
    }  
}  
```

## References

 * [Compile ASHX File](https://stackoverflow.com/questions/25510189/how-to-dynamically-compile-a-ashx-file)
 
