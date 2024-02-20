{
  "date": "2019-10-11",
  "keywords": [
    "ascx",
    "ascx file",
    "ascx file format",
    "ascx file type",
    "file",
    "type",
    "what is an ascx file"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "ASCX File Format",
  "description": "Learn about what is an ASCX file and APIs that can create and open ASCX files.",
  "linktitle": "ASCX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ascx"
    }
  },
  "lastmod": "2020-09-10"
}

## What is an ASCX file?

A file with .ascx extension is a user control that is used as a reusable component in webpages. It is referenced in any ASP website by dragging it from the control box to the page. ASCX users controls are added to the project as a central source, resulting in any change in the user control to be reflected across the whole website. Unlike ASMX files which define a mechanism to communicate within 2 objects over the internet, ASCX files are user controls for embedding in pages or website.

## ASCX File Format

ASCX files are writting in plain text format and can use code behind feature like web pages which ends with .ascx.cs. Markup code of user controls starts with @Control directive as shown in the following example.

```
<%@ Control Language="VB" AutoEventWireup="false" CodeFile="WebUserControl.ascx.vb" Inherits="WebUserControl" %>
<p>A simple web user control with static HTML only.</p>
```

This web user control can be reused on many pages such as page footer, header or some kind of site navigation. Web user controls have properties, methods and events like any other contorl which make them useful in setting their visual behaviour.

### Example of Registering user controls in web.config

In order to use a single user control on many pages, the web control can be registered in web.config. This allows to use the control over all the website instead of registering on each page individually. The following sample code defines how to register a web control in web.config to be displayed as footer on entire website.

```
<configuration>
  <system.web>
    <pages>
      <controls>
        <add src="Footer.ascx" tagPrefix="bs" tagName="footer" />
      </controls >
    </pages >
  </system.web>
</configuration>
```
## References

 * [ASCX vs ASMX](https://social.msdn.microsoft.com/Forums/en-US/a27d4c2f-b972-439e-a7fe-f4b7e3637700/how-to-work-with-ascx-files?forum=aspwebforms)
 * [ASCX User Control](https://beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)
