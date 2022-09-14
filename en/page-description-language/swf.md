{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "keywords" : [ "SWF", "file", "extension", "format", "video format","What is an SWF file", "swf file format", "swf file player","how to open swf file"],
  "title" : "SWF File - Shockwave Flash Movie File Format",
  "description":"Learn about what is a SWF file and APIs that can create and show how to open the SWF file.",
  "linktitle" : "SWF",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is an SWF file?

An SWF file is an animation file that is created with Adobe Flash. It may contain different type of elements such as text, vector images, raster images, actionscripts, objects such as circles, lines, squares, and rectangle to create the animation. SWF files arrange these multimedia items in frames that can be played on different frames per second (fps). SWF means Short Web File but is also known has Shockwave Format.

Applications that could *open SWF files** included Adobe Flash Player(now discontinued) and Eltima Elmedia Player.

## SWF File Format - More Information

SWF files were used to be stored as binary files to disc. The SWF file format was used to develop animations and games that could be embedded in websites and played independently as well. It also supported videos and sounds that gave developers alot of choices to create interactive multimedia applications. SWF files could be played in web browsers that have Adobe Shockwave installed. Adobe Flash was discontinued December 2020 due to its short comings and security issues.

## Brief History of SWF File Format

SWF file format was originally designed by FutureWave Software, to display animations with intention to run on a player software on any system with slower network connections, while keeping the file size small. In December 1996 Macromedia owned FutureWave and converted to Macromedia Flash 1.0.

In 2005, Macromedia was acquired by Adobe, who announced the SWF as a part of its open source project in 2008. During the same year, Adobe released code to world’s popular web engines to allow them the crawling and indexing of SWF files.  However, as SWF files appears to become a standard format for publishing Flash content on the internet, the SWF has been revised to mean Small Web Format.

## SWF File Structure

Path is the basic graphical element in SWF, which is a sequence of segments of basic elements, ranging from simple lines to Bezier curves. These simple elements also help to make other additional primitives like cubes, ellipses, and even texts. The graphical primitives in SWF have similarity with the graphical elements of other formats like SVG and MPEG-4 BIFS.

Display lists and reusing/renaming already defined elements are also allowed by the format. The binary stream format of SWF can be compared to QuickTime atoms which is similar in terms of tag, size and payload. The binary stream format allows the older players to skip non-supported contents. Though original versions of SWF were limited to offer vector graphics and images, therefore new versions allow audio and video contents as well.

A new, low-level 3D API of the Flash Player named “Stage3D” was introduced in version 11. This API was envisioned to be counterpart of OpenGL or Direct3D. Stage3D defines colors in a low-level language called Adobe Graphics Assembly Language (AGAL).Following are few basic datatypes of SWF file format.

### Coordinates

X-Y coordinates in SWF file format are stored as integers and measured in a unit called a twip. A twip consists of 1/20th of a logical pixel. Logical pixel and the screen pixel are the same when the file is played without scaling at 100%.

### Integer Types and Byte Order

The signed, and unsigned integer types of 8, 16, 32 and 64 bits are allowed in SWF file format. Little- endian byte order is used to store integer values. Though within bytes, the bit order is stored in big-endian. All integer values should be byte-aligned. Signed integers are represented by using traditional 2’s -complement bit patterns.

### Fixed-point Numbers

Two types of fixed-point numbers are supported by the SWF file format i.e. 32 and 16 bit.

### Floating-Point Numbers

SWF 8 and later version use three types of floating-point numbers (FLOAT, FLOAT 16, DOUBLE) that are compatible to the IEEE Standard 754 of floating-point types.

### Encoded Integers

One type of encoded integer is supported by SWF 9 and later with variable number of bytes.

## References

* [SWF file-format](https://en.wikipedia.org/wiki/Swf)
