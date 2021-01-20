 {
  "date" : "2020-01-12",
  "keywords" : [ "DGN", "File", "Format", "Open", "Read", "API", "MicroStation", "Intergraph Interactive Graphics Design System" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "DGN - CAD File Format",
  "description" : "Learn about DGN file format and APIs that can create and open DGN files.",
  "linktitle" : "DGN",
  "menu" : {
    "docs" : {
      "parent" : "cad"
    }
  },
  "lastmod" : "2020-01-12"
}

## What is a DGN file?

A file with a .dgn (Design) extension is a drawing file created by and supported by CAD applications such as MicroStation and Intergraph Interactive Graphics Design System. It is used for creating and saving designs for construction projects such as highways, bridges, and buildings. The format is similar to Autodesk's [DWG](/cad/dwg/) file format and is considered its competitor. DNG files can either be saved as Intergraph Standard File Format or V8 DGN. DGN can be converted to several other formats such as DWG, [BMP](/image/bmp/), [JPEG](/image/jpeg/), [PDF](/pdf/), [GIF](/image/gif/) and others. It can be opened with Autodesk AutoCAD, Bentley View and Bentley Systems MicroStation in addition to other software applications such as Corel PaintShop Photo Pro and IMSI TurboCAD Deluxe versions.

## V8 DGN File Format

A MicroStation V8 DGN file is composed of one or more models. A model is a container for elements. The V8 DGN removes all file format-based constraints that were present in previous versions of MicroStation. Following is a list of improvements in the DGN file format.

 * Limit on the number of levels in a DGN file has been removed, and each level is named and stored as an element.
 * The maximum physical size of the DGN file does not have any limitation and is only limited by the operating system (such as NT limit is 4 GB)
 * The maximum size of a single element is 128 KB.
 * There is no limit on the maximum size of a cell.
 * Cell names are limited to approximately 500 characters.
 * There is no limit to the number of references that can be attached to a DGN file.
 * A line string, shape, or point curve can have up to 5000 vertices.
 * There is no limit to the number of components in a complex chain or complex shape.
 * There is no limit to the number of graphic groups in a DGN file.
 * The fence is parallel to the view in which it is placed.
 * A single line of text can contain 65,535 characters.
 * There is no limit on the maximum size of a text node.
 * There is no limit to the number of text nodes in a DGN file.
 * Each element has a unique 64-bit identifier that does not change through the life-cycle of the element.
 * Each element has a time stamp that indicates the time of the most recent change.

## References

* [DNG - By Wikipedia](https://en.wikipedia.org/wiki/DGN)
* [OpenDNG](http://www.bentley.com/opendgn)
* [MicroStation V8 DGN File Format](https://web.archive.org/web/20120713013730/http://docs.bentley.com/ko/MicroStation/ustnhelp47.html)
