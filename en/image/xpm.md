{
  "date" : "2019-10-11",
  "keywords" : [ "xpm file", "xpm file format", "what is a xpm file", "file", "xpm example", "xpm file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "XPM - X PixMap File Format",
  "description":"Learn about XPM file format and APIs that can create and open XPM files.",
  "linktitle" : "XPM",
  "menu" : {
    "docs" : {
      "parent" : "image"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is an XPM file?

A file with .xpm extension is an image file format that was used by the X Windows System. It supports transparent pixels and usually targets creating icon pixmaps. It supports monochrome, gra-scale, and color pixmap data. These were designed to be editable by hand and can be included in [C](/programming/c/) code. For this purpose, XPM files are in plain text file format and follow the C programming language syntax. XPM files can be opened with a variety of image viewing application such as
CorelDRAW Graphics Suite 2020, Corel PaintShop Pro, IrfanView, and Canvas X.

## XPM File Format

The XPM file format uses C syntax in order for these to be integrated in C and C++ programs. It consists of the following six different sections.

 * \<Values>
 * \<Colors>
 * \<Pixels>
 * \<Extensions>

The sections are actually an array of strings as follow.

```
/* XPM */
static char*<variable_name>[] = {
  <Values>
  <Colors>
  <Pixels>
  <Extensions>
};
```
Following are the details of each section.

`<Values>` - This section is a string that contains four or six integers that are in base 10 and correspond to the:

 * pixmap width and height
 * number of Colors
 * number of characters per pixel
 * optional hotspot coordinates and XPMEXT tag

`<Colors>` - This section contains as many strings as there are colors. Each string is as follows:

 ```
<chars> {<key> <color>}+
 ```
`<Pixels>` - This section is composed of <height> strings and <width>\*<chars_per_pixel> characters. Every <chars_per_pixel> length string should be one of the previously defined groups in the <Colors> section.

`<Extension>` - The extension section must be labeled, if it is not empty, in the <Values> section. It may consist of several <Extension> subsections which may be of the following two types:

 * one stand alone string composed as follows: XPMEXT <extension-name> <extension-data>
 * or a block composed by several strings:XPMEXT <extension-name><related extension-data composed of several strings>

## References

* [XPM -  Wikipedia](https://en.wikipedia.org/wiki/X_PixMap)
* [XPM Manual](http://www.xfree86.org/current/xpm.pdf)
