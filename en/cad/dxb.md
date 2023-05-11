{
  "date": "2023-05-10",
  "keywords": [
    "dxb file",
    "what is a dxb file",
    "what is the format of dxb file",
    "what does dxb file contain",
    "file",
    "dxb file extension",
    "extension"
  ],
  "author": {
    "display_name": "Shakeel Faiz"
  },
  "draft": "false",
  "toc": true,
  "title": "DXB File Format - Drawing Exchange Binary",
  "description": "Learn about DXB format and APIs that can create and open DXB files.",
  "linktitle": "DXB",
  "menu": {
    "docs": {
      "identifier": "cad-dxb",
      "parent": "cad"
    }
  },
  "lastmod": "2023-05-10"
}

## What is a DXB file?

DXB stands for Drawing Exchange Binary, which is a file format used in computer-aided design (CAD) software. DXB files contain binary data that represent 2D vector graphics and are used to exchange drawings between different CAD programs. They are typically created by exporting drawing from CAD program in DXB format and then importing it into another CAD program. 

DXB format is less commonly used today than other CAD file formats like DXF or DWG. However, some older CAD programs may still use DXB as file format for exporting or importing drawings.

If you have DXB file and need to view or edit it, you will need CAD program that supports DXB format. Some examples of CAD programs that support DXB include AutoCAD, DraftSight and LibreCAD.

## DXB File Format - More Information

DXB (Drawing Exchange Binary) is a binary version of DXF (Drawing Exchange Format) file format, which is a standard format for exchanging CAD drawings between different software applications.

DXB files contain binary data that represent 2D vector graphics just like DXF files. However, DXB files are more compact and faster to load than DXF files because they are stored in binary format instead of plain text.

To create a DXB file, a CAD program can export drawing in DXB format, which generates binary file that can be read by other CAD programs that support DXB. Similarly, to import DXB file, a CAD program can read the binary data and convert it into its own internal format for editing.

## What is the format of DXB file?

DXB (Drawing Exchange Binary) file format is a binary file format, meaning that it consists of binary data that can be interpreted directly by computer.

The binary format used by DXB is more compact and faster to load than the text-based DXF (Drawing Exchange Format) file format which is also used for exchanging CAD drawings between different software applications.

The structure of DXB file consists of series of binary records each of which contains header and data that represent single object or entity in drawing. The header contains information about the type of object or entity represented by the data as well as its size and other properties.

The data in DXB file is organized hierarchically, with higher-level records containing references to lower-level records that represent sub-objects or components of drawing. For example, a record representing polyline may contain references to records representing individual line segments that make up the polyline.

## What does DXB file contain?

DXB (Drawing Exchange Binary) file contains binary data that represent 2D vector graphics such as lines, arcs, circles, text and other geometric shapes that make up CAD drawing.

When CAD program exports a drawing to DXB format, it creates binary file that contains all the information necessary to recreate the drawing in another CAD program that supports DXB. This includes information about location, size, color and style of each object in the drawing as well as any text or annotations that may be included.

Because DXB files are stored in binary format, they are typically smaller in size and faster to load than DXF (Drawing Exchange Format) files, which are stored in plain text. However, DXB files can only be read by CAD programs that support the DXB format, whereas DXF files can be read by wider range of programs.

## References
* [DXB File Format](http://web.archive.org/web/20060824054154/https://www.autodesk.com/techpubs/autocad/acadr14/dxf/the_dxb_file_format_al_u05_b.htm)
