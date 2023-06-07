{
  "date" : "2023-06-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "BROWSER File - ASP.NET Browser Definition File Format",
  "description":"Learn about BROWSER file format and APIs that can create and open BROWSER files.",
  "linktitle" : "BROWSER",
  "menu" : {
    "docs" : {
      "parent" : "web",
      "identifier": "web-browser"
    }
  },
  "lastmod" : "22023-06-06"
}

## What is a BROWSER file?

A file with .browser extension is used by ASP.NET web applications to determine the capability and configuration of web browsers. It contains information about the browser's capabilities, limitations, and characteristics. These characteristics help the ASP.NET framework to recognize the requesting browser and present the webpage to users accordingly.

## BROWSER File Format

BROWSER definition files are used by the ASP.NET application to determine the capabilities of the browser. It is information contained in this file that is used by the server to generate markup and other resources that are compatible with the requesting browser. 

BROWSER files are saved in plain text file format. You can open a BROWSER file in text editors such as Notepad, Notepad++, Apple TextEdit and Visual Studio IDE.

### File Structure of BROWSER File Format

The BROWSER definition files use a hierarchical structure. Each .browser file contains an XML markup that includes the capabilities and features of a particular browser or a group of browsers. These details include characteristics such as agent string, version numbers, and support for technologies such as JavaScript, CSS, or other HTML elements. By using these browser definition files, ASP.NET developers customize user experiences based on the capabilities of different browsers.

## References

 * [Working with Files in an ASP.NET Web Pages](https://learn.microsoft.com/en-us/aspnet/web-pages/overview/data/working-with-files)


