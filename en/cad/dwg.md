{
  "date" : "2020-03-16",
  "keywords" : [ "DWG", "File Format", "CAD", "Open", "Create" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about DWG file format and APIs that can create and open DWG files.",
  "title" : "DWG File Format",
  "linktitle" : "DWG",
  "menu" : {
    "docs" : {
      "parent" : "cad"
    }
  },
  "lastmod" : "2019-09-10"
}

# What is a DWG file? #

Files with DWG extension represent proprietary binary files used for containing 2D and 3D design data. Like DXF, which are ASCII files, DWG represent the binary file format for CAD (Computer Aided Design) drawings. It contains vector image and metadata for representation of contents of CAD files. There are free viewers available for viewing DWG files on Windows Operating System such as the Autodesk's free DWG TrueView. There are other third party applications as well that support reaching DWG files. DWG files contain user created information and includes:

* Designs
* Geometric data
* Maps and photos

This format is widely used by architects, engineers, and designers for various designing purposes.

## Brief History ##

DWG file format has evolved with the time since its formal introduction in 1982. A brief overview of the past events from history perspective is as follow.

**1982:** Autodesk licensed the DWG file format , which was developed by Mike Riddle in 1970, as the basis for AutoCAD.

**1998:** With the release of AutoCAD R14.01, Autodesk added file verification through a function called DWGCHECK that embedded a an encrypted checksum and product code, called as WaterMark by Autodesk, into DWG files created by the program.

**2006:** Autodesk modified AutoCAD 2007, to include "TrustedDWG technology" to embed text string "Autodesk DWG. This file is a Trusted DWG last saved by an Autodesk application or Autodesk licensed application" into the DWG files. The purpose of this was to help Autodesk software users ensures that these files were created by an Autodesk or RealDWG application, which should definitely help in reducing the risk of incompatibilities.

## File Structure ##

DWG has been one of the widely used file format by a range of applications and has a robust file structure. Since DWG is a binary file format, it is not human-readable like the plain ASCII [DXF](/cad/dxf/) file format. DWG files usually include information about the image coordinates and any metadata associated with it. Complete [specifications](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf) of DWG file format are available for download by OpenDesign. The file structure of DWG file format is summarized as follow.

**Header**: The file header consists of DWG Header variables and information about Cyclic Redundancy Check  (CRC) which is used for the error detection. Each subsection is a specialized vector where different lengths of bits are used to represent different labels. For instance, the first 6 bits of the DWG Header variable stands for the version string.

**Class Definitions:** A DWG file may contain numerous classes depending upon the specific .dwg file purpose. Information such as class metadata size of class data area, class number and checksum in addition to others.

**Template**: This is optional and for R15 and R15 versions, this section is below the the Object Free Space section.

**Padding**: The metadata is suffixed and postfixed with a specific number of bytes which makes the older AutoCAD software versions to be forward compatible to the new DWG file format.

**Image Data**: The metadata for this section depends on the specific .dwg type. For R14 and R15 users, this section is optional.

**Object Data**: The object data consists of a complete list of table entities, dictionary entries, etc. corresponding to the existing list of objects.

**Object Map**: Location of each object in the file is specified in this section of file. Most of the metadata in this section are file handles that play a role in identification and re-rendering of the object.

**Object Free Space**: This section is optional for all users

**Second Header**: A duplicate of the file header section towards the end of the DWG file

## References ##

* [DWG File Format Specifications](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf)
* [The DWG File Specification](https://www.scan2cad.com/dwg/file-spec/)
* [DWG - By Wikipedia](https://en.wikipedia.org/wiki/.dwg)
