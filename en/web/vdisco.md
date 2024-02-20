{
  "date": "2023-01-29",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "VDISCO File - DISCO Dynamic Discovery Document File Format",
  "description": "Learn about what is a VDISCO file?",
  "linktitle": "VDISCO",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-vdisco"
    }
  },
  "lastmod": "2023-01-29"
}

## What is a VDISCO file?

A VDISCO file is a discovery file used by Microsoft Visual Studio in its Web Services. It provides information about the available Web Services such as their URLs, namespaces, and methods. VDISCO file is similar to the [DISCO](/web/disco/) file format but is generated at runtime. It is stored in the Web service application and is used by the Visual Studio to dynamically discover and use Web Services in a project. VDISCO files are used in combination with the [.asmx](/web/asmx/) file that contains the actual Web Service code.

You can open VDISCO file in any text editor such as Microsoft Notepad, Github Atom, and Apple TextEdit. It can also be opened with Microsoft Visual Studio 2012 and later for working with it.

## VDISCO File Format

A VDISCO file is saved and hosted in [XML](/web/xml/) file format which is a universal format for composition and publishing of data. It contains the service URL, namespaces and methods in standard XML tags where each tag contains respective value of its information.

## References

* [DISCO](https://appsource.microsoft.com/en-us/product/office/WA104381894)
* [Web Services Discovery](https://en.wikipedia.org/wiki/Web_Services_Discovery)
* [C# Example of DiscoveryClient Class](https://learn.microsoft.com/en-us/dotnet/api/system.web.services.discovery.discoveryclientprotocol?view=netframework-4.8)
