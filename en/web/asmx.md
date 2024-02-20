{
  "date": "2019-10-11",
  "keywords": [
    "asmx",
    "asmx file",
    "asmx file format",
    "asmx file type",
    "file",
    "type",
    "what is an asmx file"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "ASMX - ASP.NET Web Service File",
  "description": "Learn about what is an ASMX file and APIs that can create and open ASMX files.",
  "linktitle": "ASMX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-asmx"
    }
  },
  "lastmod": "2021-06-10"
}

## What is an ASMX file?

A file with .asmx extensions is an ASP.NET Web Service file that provides communication between two objects over the internet using the Simple Object Access Protocol (SOAP). It is deployed as a service on the Windows-based Web Server to process incoming request and return the response. Unlike [ASPX](/web/aspx/) files which contain the code for visual display of ASP.NET webpages, ASMX files run at the server in background and perform different tasks such as connecting to database, retrieving data, and returning it in a format in which the request was made. These are used specifically for XML webs services.

## ASMX File Format

ASMX files are in plain text format and can be opened or edited in applications such as Microsoft Visual Studio or text editors. It is a proprietary file format of Microsoft and has a well-defined syntax for creation of web services. A response by an ASMX file in the form of SOAP XML has the following elements.

 * `Envelop` - A root element that identifies the XML document as a SOAP message.
 * `Header` - An optional element that contains application-specific information such as authentication data. If the Header element is present it must be the first child element of the Envelope element.
 * `Body` - Contains the SOAP message intended for the recipient.
 * `Fault` - An optional element that's used to indicate error messages. If the Fault element is present, it must be a child element of the Body element.

ASMX files can be written in .NET languages such as [C#](/programming/cs/), [Visual Basic](/programming/vb/) or JScript.

## How is ASMX different than ASPX and ASCX?

ASMX files are different than ASPX and ASCX files.

 * ASPX, Active Server Pages, files are programming files that are generated using Microsoft ASP.NET framework running on web servers. These are rendered in client's web browser when user requests to access such a page.
 * ASCX, Active Server User Control, defines user controls that are used to define reusable controls in ASP.NET web pages or entire website.

## References

 * [Consuming ASMX Service](https://learn.microsoft.com/en-us/xamarin/xamarin-forms/data-cloud/web-services/asmx)
 * [ASCX User Control](https://beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)
