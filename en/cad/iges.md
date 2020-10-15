{
  "date" : "2020-03-16",
  "keywords" : [ "IGES File", "File Format", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about IGES file format and APIs that can create and open IGES files.",
  "title" : "IGES File Format",
  "linktitle" : "IGES",
  "menu" : {
    "docs" : {
      "parent" : "cad"
    }
  },
  "lastmod" : "2020-07-28"
}

## What is an IGES file?

A file with .iges extension is used to exchange design information between computer-aided design (CAD) applications. IGES stands for Initial Graphics Exchange Specifications. Information exchanged using IGES includes circuit diagram, wireframe, freeform surface or solid modeling representations. IGES finds its applications in traditional engineering drawings, models analysis, and manufacturing functions. The format can exchange both 2D or 3D design information between CAD programs. IGES files can be opened with several CAD applications such as Autodesk and CADSoftTools ABViewer. There are also several APIs available to open and convert IGES files programatically.

## File Format

IGES files are in ASCII text format and can be opened in any text editor to view the contents of the file. Textual information in an IGES file is represnted in "Hollerith" format. A common IGES file can contain thousands of lines to represent the 2D or 3D information that can be exchanged as per this format. An IGES file is split into five sections, denoted by the specific upper case letter in the 73rd column. Those sections are `Start` (S), `Global` (G), `Data Entry` (D), `Parameter Data` (P), and `Terminate` (T) sections. The Data Entry and Parameter Data sections are commonly abbreviated DE and PD, respectively.

### File Header

The Start and Global sections contain basic information about:
 * Name of the file and its source
 * Delimiters for the Parameter Data section
 * Author of the file, and other general information.

Start and Global sections from the example document on Wikipedia are as follow.
```
S      1
1H,,1H;,4HSLOT,37H$1$DUA2:[IGESLIB.BDRAFT.B2I]SLOT.IGS;,                G      1
17HBravo3 BravoDRAFT,31HBravo3->IGES V3.002 (02-Oct-87),32,38,6,38,15,  G      2
4HSLOT,1.,1,4HINCH,8,0.08,13H871006.192927,1.E-06,6.,                   G      3
31HD. A. Harrod, Tel. 313/995-6333,24HAPPLICON - Ann Arbor, MI,4,0;     G      4
```
As can be seen, the start field contains human readable descriptions of the file, and my have any characters in columns 1-72, with the line ending with the section header and section line number. There must be at least 1 line of the Start section. The global section contains preprocessor data. It also must be present in the file and end with the G000000# format.


## References
 * [IGES by WikiPedia](https://en.wikipedia.org/wiki/IGES)
