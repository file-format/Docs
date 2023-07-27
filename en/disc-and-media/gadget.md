{
  "date" : "2021-06-24",
  "keywords": [ "GADGET file", "what is a gadget file", "extension", "format", "what is a GADGET file", "archive" ],
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
   "toc" : true,
  "description" : "Learn about GADGET file format and APIs that can create and open GADGET files.",
  "title" : "GADGET - Virtual CD File",
  "linktitle" : "GADGET",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
    }
  },
  "lastmod" : "2021-06-24"
}

## What is a GADGET file?

A GADGET file consists of a small software program that executes within the Windows Vista or Windows 7 sidebar. It compresses several web-based files and the files may comprise the [.html](/web/html/), [.css](/web/css/) or [.js](/web/js/) files, as well as other web files. GADGET files are used for small components such as search tools, news feeds, system utilities, and small games. Although GADGETs are hosted by the Sidebar, are not specific to the Sidebar area; these can be undocked and move onto the desktop as desired.

## GADGET file format

The GADGET file is a renamed [ZIP](/compression/zip/) archive containing a collection of HTML, XML, JScript, and CSS (Cascading Style Sheets) files. The installation contains downloading the .gadget file and enabling the download process to install the component or saving the .gadget file to the local system and double-clicking to start the installation process.

Basically, a GADGET contains two files:

1. **Gadget.xml**: The manifest, an XML file consisting of general presentation and configuration information for the gadget.
2. **name.html**: An HTML file, in which the name is specified in the <name> tag of the associated gadget manifest, that gives the wrapper for the gadget UI and comprises the core functionality for the gadget.

Multiple Instances of a GADGET file can be run simultaneously. For an instance, if someone wants to know the time in various time zones, they can run multiple instances of the clock gadget by setting each clock to a particular time zone.

### Discontinuation of GADGET

Since the Windows Sidebar platform in Windows 7 has serious vulnerabilities, the Gadgets are no longer available on Microsoft's official website. Later on, Microsoft retired this feature in newer releases of Windows. GADGET could be exploited to access a computer's files, harm a computer, reveal objectionable content, or change their behavior at any time.

## References 

* [Windows Sidebar - by Microsoft](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/sidebar/-sidebar-entry)
* [Developing a Gadget for Windows Sidebar Part 1](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/sidebar/-sidebar-overview-gdo)
