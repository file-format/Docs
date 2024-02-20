{
  "date": "2022-09-17",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "DISCO File - DISCO Discovery Document File Format",
  "description": "Learn about what is a DISCO file and APIs that can create and open DISCO files.",
  "linktitle": "DISCO",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-disco"
    }
  },
  "lastmod": "2022-09-17"
}

## What is a DISCO file?

A DISCO file is a Microsoft Discovery file format that is used for publishing and discovering Web Services. It is stored in XML file format and lets the Web Services Discovery tools to locate or discover one or more related documents for describing the available [XML](/web/xml/) services. DISCO file stores information such as discovery documents, [XSD](/programming/xsd/) schemas, and service descriptions. XML Web services use this information to get to the available XML web services at a given URL.

## DISCO File Format - More Information

DISCO files are saved in XML file format. Microsoft Discovery Tool (DISCO.exe), that comes bundled with Microsoft ASP.NET development software such as Microsoft Studio, use the DISCO files to discover the details about the XML Web services listed in a DiscoveryDocument at a specific URL. Microsoft has provided the support of reading discovery files in .NET framework.

## References

* [DISCO](https://appsource.microsoft.com/en-us/product/office/WA104381894)
* [Web Services Discovery](https://en.wikipedia.org/wiki/Web_Services_Discovery)
* [C# Example of DiscoveryClient Class](https://learn.microsoft.com/en-us/dotnet/api/system.web.services.discovery.discoveryclientprotocol?view=netframework-4.8)
