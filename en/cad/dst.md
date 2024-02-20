 {
  "date": "2022-01-04",
  "keywords": [
    ".dst",
    "file",
    "format",
    "extension",
    "API",
    "AutoCAD Sheet Set"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "DST - AutoCAD Sheet Set File",
  "description": "Learn about .dst file and APIs that can create and open DST files.",
  "linktitle": "DST",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-dst"
    }
  },
  "lastmod": "2022-01-04"
}

## What is a DST file?

A DST file is an AutoCAD file that contains associations and information for defining sheet sets. These are stored in the default sheet set storage folder, AutoCAD Sheet Sets. DST files do not contain the actual drawing layouts but refer to these from selected [DWG](/cad/dwg/) and [DWT](/cad/dwt/) files associated with these sheet sets. In network environment, all team members should have network access to these associated files. DST fils are saved to disc in [XML](/web/xml/) file format.

## DST File Format - More Information

DST files are created with AutoDesk Sheet Set Manager (SSM) tool. When a file is accessed by someone in team, the DST file is opened briefly and then stored back with the updated information. Simultaneous access to the same DST file is managed by the SSM tool that shows a lock icon when the file is in access.

At any particular time, the sheet status can be in any of the following state.

 * The sheet is available for editing.
 * The sheet is locked.
 * The sheet is missing or found in an unexpected folder location.

## References

* [About using DST Sheet Sets](https://help.autodesk.com/view/ACDLT/2017/ENU/?guid=GUID-577D8EA0-85F2-4829-B4F9-8CAD6F7AAACC)
* [Learn about Sheet Sets](https://help.autodesk.com/view/ACDLT/2017/ENU/?guid=GUID-34D889BC-19AD-4CD1-ADB1-F359D9B515FB)
* [Mastering AutoCAD Sheet Sets](https://damassets.autodesk.net/content/dam/autodesk/www/cad-manager-center/articles/Mastering-AutoCAD-Sheet-Sets_Preview_EN.pdf)
