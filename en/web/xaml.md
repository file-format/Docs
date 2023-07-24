{
  "date" : "2019-10-11",
  "keywords" : [ "xaml","xaml file", "xaml file format", "xaml file type", "file", "type", "what is an xaml file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "XAML - XML Based Markup Language",
  "description":"Learn about XAML file format and APIs that can create and open XAML files.",
  "linktitle" : "XAML ",
  "menu" : {
    "docs" : {
      "parent" : "web"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is a XAML file?

XAML, Extensible Application Markup Language, extension files describe the user interface elements for software applications based on Windows Presentation Foundation (WPF). Though a language, it doesn't require to be programmed as it is based on standard format of **[XML](/web/xml/)** which is easy to use and understand. XAML (pronounced as "zammel") was developed by Microsoft with specific aim for creating user interfaces. Its acronym original stood for Extensible Avalon Markup Language, where Avalon was the code-name for WPF. XAML files are sometimes saved with XOML extension as well.

## XAML Applications

XAML is choice of use in .NET Framework 3.0 and .NET Framework 4.0 technologies such as WPF, Silverlight, Windows Workflow Foundation (WF) and few others. UI elements, data bindings, events and other features are are defined by XAML forms in WPF. Similarly, workflows in WF can be defined using XAML. It is easily processed by tools for the reason that it is based on XML. Since it is a declarative language and doesn't need compilation, a lot of products are emerging that are based on the XAML-based applications. Anything that is created or implemented in XAML can be expressed using a more traditional .NET language, such as C# or Visual Basic .NET.

## XAML File Format

XAML is totally based on the XML format. The initial specifications of [XAML Object Mapping](https://download.microsoft.com/download/0/A/6/0A6F7755-9AF5-448B-907D-13985ACCF53E/%5BMS-XAML%5D.pdf) were published in 2006, followed by another [version](https://download.microsoft.com/download/0/A/6/0A6F7755-9AF5-448B-907D-13985ACCF53E/%5BMS-XAML-2009%5D.pdf) published in 2009. These specifications define two abstract information models:

* XAML Schema Information Set Model
* XAML Information Set Model

The Xaml Information Set ('Xaml Infoset' for short) defines the structure of information that a Xaml instance can represent. The Xaml Schema Information Set allows specific Xaml vocabularies to be defined. This specification also defines a set of rules for transforming an XML document into a Xaml Information Set. XML is a common format for Xaml. (The term "Xaml Document" refers to an XML document that represents a Xaml Information Set.) But while this specification does not define any other representations, any physical representation may be used as long as it can represent the information in the Xaml Information Set.

## References

* [XAML - By Wikipedia](https://en.wikipedia.org/wiki/Extensible_Application_Markup_Language)
* [XAML File Format Specifications](https://download.microsoft.com/download/0/A/6/0A6F7755-9AF5-448B-907D-13985ACCF53E/%5BMS-XAML-2009%5D.pdf)
