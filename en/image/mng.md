{
  "date" : "2019-10-11",
  "keywords" : [ "mng file", "mng file format", "what is a mng file", "file", "mng example", "mng file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "MNG File Format - Multiple Image Network Graphics File Format",
  "description":"Learn about MNG file format and APIs that can create and open MNG files.",
  "linktitle" : "MNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is a MNG file?

A file with .mng extension is a Mutliple-image Network Graphics file format that is similar to [PNG](/image/png/) image format but supports animated images. It was developed to avoid overloading the PNG format with additional feature of animations. MNG is also similar to [GIF](/image/gif/) files but uses more compression and supports full alpha feature. The unofficial MIME media type for MNG files is video/x-mng. MNG files can be opened in applications such as ImageMagik and IrfanView.

## MNG File Format

MNG file format is similar to that of PNG and uses the same chunk structure as defined in the PNG specifications. A MNG decoder must be able to decode the PNG datastreams without specifying any special flags for decoding instructions. MNG groups multiple images together into a "frame", with some images used as sprite for moving from one location to another. The mechanism allows reusing image data without retransmitting it. The [MNG specifications](http://www.libpng.org/pub/mng/spec/) can be referred to for developer's reference.

### MNG Signature

The MNG datastream begins with an 8-byte signature containing:

```
138  77  78  71  13  10  26  10  - (decimal)
8a  4d  4e  47  0d  0a  1a  0a   - (hexadecimal)
\212   M   N   G  \r  \n \032 \n - (ASCII C notation)
```

This is similar to that of PNG signature but contains MNG instead of PNG.

### MNG Frame

An MNG frame consists of two-dimensional image of smaller images. Each small image can be accessed using the row and column index combination. The format is capable of storing three-dimensional "voxel" data that is arranged a series of two-dimensional planes. Each plane is represented by a PNG or Delta-PNG datastream. Each Delta-PNG datastream defines an image as the differences from the parent PNG image. This provides a much more compact way of representing subsequent images than using a complete PNG datastream for each.

## References ##

* [MNG](http://www.libpng.org/pub/mng/)
* [MNG Format v 1.0](http://www.libpng.org/pub/mng/spec/)
