{
  "date": "2020-03-16",
  "keywords": [
    "PAT File",
    "Format",
    "CAD"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "description": "Learn about PAT file format and APIs that can create and open PAT files.",
  "title": "PAT File Format",
  "linktitle": "PAT",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-pat"
    }
  },
  "lastmod": "2020-10-25"
}

## What is a PAT file?

A file with .pat extension is a CAD file which is used by AutoCAD software. Applications that can open PAT files use the hatch pattern stored in these files get information about the texture/filling of an area. The patterns contained give information about the appearance of material to drawn objects. PAT files can be opened in applications such as Autodesk AutoCAD, CorelDRAW Graphics Suite, and Ketron Software. PAT files can be converted to different image formats such as JPG, PNG, BMP, etc.

## PAT File Format

PAT files are written in plain text format and can be opened in any text editor. The hatch patters in these files are vector-based and follow the syntax outlined by AutoCAD documentation.

All patterns start at the point 0,0, the pattern is calculated out to cover the hatching boundary.

### Pattern Definition

All pattern definitions consist of the following fields:
 * A leading ‘\*’
 * A name -  The name can have no spaces, punctuation marks, parenthesis, or slashes.
 * A description

The standard format for hatch patterns is `<\*><name><, description>`. The name and the description are separated by a comma and descriptions cannot exceed the eighty character line length. The hatch patterns are defined after this information.

### Hatch Pattern Examples
Following is an example of square pattern
```
* square, a square pattern
0,     0,0,   0,1,   1,-1
90,   0,1,   0,1,   1,-1
```
Another example showing parallelogram pattern is as follow.

```
*pgram, parallelogram pattern
0,     0,0,    1,1,                     1,-1
45,   0,0,    0,1.4142,   1.4142,-1.4142
45,   0,1,    0,1.4142,   1.4142,-1.4142
```
## References ##

 * [Hash Patterns by Autodesk](https://help.autodesk.com/view/ACDLT/2018/ENU/?guid=GUID-A6F2E6FF-1717-44B6-A476-0CA817ADD77E)
