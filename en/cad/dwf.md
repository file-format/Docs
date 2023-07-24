{
  "date" : "2020-03-16",
  "keywords" : [ "DWF", "File Format", "Open", "Read", "Create", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about DWF file format and APIs that can create and open DWF files.",
  "title" : "DWF File Format",
  "linktitle" : "DWF",
  "menu" : {
    "docs" : {
      "parent" : "cad"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is a DWF file?

Design Web Format (DWF) represents 2D/3D drawing in compressed format for viewing, reviewing or printing design files. It contains graphics and text as part of design data and reduce the size of the file due to its compressed format. The reduced file size makes the distribution and communication of rich design data efficient. DWF doesn't require the recipient to know about the usage of CAD software that created the original drawing. The contents of DWF file format can be simple and include just a single sheet or complex enough to have fonts, color, and images.

## Brief History ##

Autodesk introduced the DWF file format in 1995 as part of Netscape Navigation plug-in, WHIP. The format evolved from 2D-only format to include 3D contents with the passage of time. Many of third-party applications also make use of this format.

## DWF File Format ##

DWF is an open, secure format designed specifically for sharing rich engineering design data. It is independent of the original application software, hardware, and operating system used to create that design data. This enables team members who do not use CAD applications to participate in the digital processes by viewing building, GIS, or product designs. A DWF file archive consists of several XML and binary files that are packaged together in a compressed archive created with [ZIP](/compression/zip/) compression. You can rename a DWF file extension to ZIP and view the contents of the file. The DWF package can contain many kinds of design data such as 2D graphics, 3D graphics, package and section metadata, and other resource files.

**DWF metadata files** – XML files that contain information pertaining to metadata and structure (author, title, creation time, section dependencies, section ordering, resource file descriptions, roles, mimetypes, etc.) and pertaining to the section (page information, design metadata, etc.).  The structural metadata is used to create logical objects (collections of files to represent a part or page, etc.).

**Resource files** – media or other content files that are referenced from the package/section metadata and are usually presentations of design data in various formats (ZGL, W2D, [JPG](/image/jpeg/), [PNG](/image/png/), AVI, XML, [TXT](/word-processing/txt/), [DOC](/word-processing/doc/), etc.)

### File Format Details ###

DWF files are organized into three main sections as shown below.

* File identification header
* File data block
* File termination trailer

#### File Identifier Header ####

The file identifier header allows for identification of DWF files by applications. It also identifies which version of DWF specifications was used for encoding the file. It is a 12 byte header that is arranged as follow:


|Byte|0|1|2|3|4|5|6|7|8|9|10|11
--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- |
|Character|(|D|W|F|(space)|V|0|0|.|3|0|)

Here is a summary of this table:

* The first six bytes of the header always represent ASCII characters "(DWF V"
* The following 5 bytes contain information about the version number e.g. "00.30" with the major and minor version value of the format

Applications creating a DWF file should specify the lowest possible version number that a reader application need to support in order to properly use the data.

#### File Data Block ####

The file data block starts at the 13th byte of a DWF file, and is a series of opcode and operand pairs, as in following table.

|Field 1|Field 2|Field 3|Field 4|Field 5|Field 5
--- | --- |--- | --- |--- | --- |
|opcode|operand|opcode|operand|opcode|operand

A DWF file can contain opcode-operand pairs as readable ASCII as well as code binary or a mix of both of these. All DWF operations have a readable ASCII opcode/operand form, and most operations also have a coded binary opcode/operand form. Opcodes are in single byte allowing for over 200 operations. Extended ASCII and extended binary are exceptional cases. The values of Opcodes can range from 0-255 with some exceptions. Except for the two special types of opcodes extended ASCII and extended binary, a file reader must know how to compute the operand length.

##### Forbidden Opcodes #####

The ASCII representations for the following cannot be used as opcodes:

Following ASCII representations can not be used as opcodes:

* Space (0x20)
* Tab (0x09)
* Hyphen (0x2D)
* ASCII digits 0-9 (0x30 - 0x39)
* Carriage return (0x0D)
* Line feed (0x0A)
* Single Quotation Mark (0x27)
* Double quotation mark (0x22)
* Period (0x2E)
* Parenthesis (0x28 and 0x29)
* Curly brackets (0x7B and 0x7D)
* Square brackets (0x5B and 0x5D)
* Backwards slash (0x5C)

#### File Termination Trailer ####

The file termination trailer for DWF is simply a special opcode indicating the end of the file. Some applications can store non-DWF data following the termination opcode.The trailer is as shown below:


|Byte|0|1|2|3|4|5|6|7|8|9
---|---|---|---|---|---|---|---|---|---|---|
|Character|(|E|n|d|0|f|D|W|F|)

## References ##

* [DWF - By Wikipedia](https://en.wikipedia.org/wiki/Design_Web_Format)
* [WHIP Data Format](http://paulbourke.net/dataformats/whip/)
* [https://learn.microsoft.com/en-us/archive/blogs/opc/adventures-in-packaging-episode-1](https://learn.microsoft.com/en-us/archive/blogs/opc/adventures-in-packaging-episode-1)
