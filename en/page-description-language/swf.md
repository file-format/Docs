{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "SWF",
  "description":"Learn about SWF file format and APIs that can create and open SWF files.",
  "linktitle" : "SWF",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is a SWF file? ##

SWF is a file format used to transport text, video, vector graphics and ActionScript over the internet and supported by Adobe Flash Player. The SWF file format is designed to be a resourceful transfer format, not only for exchanging graphics but also provides supports for anti-aliasing and on-screen display. Anti-aliasing is a feature that is critical  for fast rendering of bitmap and its associated characteristics like interactive buttons, shading and animation .etc.

SWF is a tagged format provides extended feature while remains compatible with old versions of Flash Player. Stack machines are used to interpret the sequences of byte code that are within the tags. The byte codes support the language of ActionScript, whose model is provided by flash player at runtime for collaboration with servers and drawing primitives. Another characteristic of this format is its portability, it can be transported over a network having a low and unpredictable bandwidth. In a low bandwidth environment, incremental rendering through streaming and file compression techniques are used to get the maximum benefits.

The SWF file format is a binary format that keeps the file size small while bit-packing and structures are the commonly used techniques. The format keep simple to facilitate Flash Player which can be easily ported. Files themselves are self-sufficient in a way, there is no need of any external resource such as fonts. With limited resources (hardware) the files work well and can take advantage of better resources when resources improve. This capability is vital because monitors have diverse resolutions and bit depths.

## History ##

This format was originally designed by FutureWave Software, to display animations with intention to run on a player software on any system with slower network connections, while keeping the file size small. In December 1996 Macromedia owned FutureWave and converted to Macromedia Flash 1.0.

The name of SWF came out of Macromedia's efforts to produce Shockwave files for the end user. They tried to capitalize Macromedia Shockwave on the already established brand. As Flash appears to dominate the Shockwave itself, so they referred this format to be simply SWF. In 2005, Macromedia was acquired by Adobe, who announced the SWF as a part of its open source project in 2008. During the same year, Adobe released code to world’s popular web engines to allow them the crawling and indexing of SWF files.  However, as SWF files appears to become a standard format for publishing Flash content on the internet, the SWF has been revised to mean Small Web Format.

## SWF File Format ##

Path is the basic graphical element in SWF, which is a sequence of segments of basic elements, ranging from simple lines to Bezier curves. These simple elements also help to make other additional primitives like cubes, ellipses, and even texts. The graphical primitives in SWF have similarity with the graphical elements of other formats like SVG and MPEG-4 BIFS. Display lists and reusing/renaming already defined elements are also allowed by the format. The binary stream format of SWF can be compared to QuickTime atoms which is similar in terms of tag, size and payload. The binary stream format allows the older players to skip non-supported contents. Though original versions of SWF were limited to offer vector graphics and images, therefore new versions allow audio and video contents as well.

A new, low-level 3D API of the Flash Player named “Stage3D” was introduced in version 11. This API was envisioned to be counterpart of OpenGL or Direct3D. Stage3D defines colors in a low-level language called Adobe Graphics Assembly Language (AGAL).Following are few basic datatypes of SWF file format.

### Coordinates ###

 X-Y coordinates in SWF file format are stored as integers and measured in a unit called a twip. A twip consists of 1/20th of a logical pixel. Logical pixel and the screen pixel are the same when the file is played without scaling at 100%.

### Integer types and byte order ###

The signed, and unsigned integer types of 8, 16, 32 and 64 bits are allowed in SWF file format. Little- endian byte order is used to store integer values. Though within bytes, the bit order is stored in big-endian. All integer values should be byte-aligned. Signed integers are represented by using traditional 2’s -complement bit patterns.

### Fixed -point numbers ###

Two types of fixed-point numbers are supported by the SWF file format i.e. 32 and 16 bit.

### Floating-point numbers ###

SWF 8 and later version use three types of floating-point numbers (FLOAT, FLOAT 16, DOUBLE) that are compatible to the IEEE Standard 754 of floating-point types.

### Encoded integers ###

One type of encoded integer is supported by SWF 9 and later with variable number of bytes.

### Versions ###

Several versions of SWF format have been evolved so far. Newer version from SWF 5, were made to the SWF tag set. After version 6, additional new changes are made at the ActionScript level. ActionScript 3.0 language is used through the version 9, which works with the ActionScript Virtual Machine 2 (AVM2). The user who plans to use latest versions, should aware to the use of ActionScript object model that Flash Player depicts.

## References ##

* [SWF file-format specification](https://www.adobe.com/content/dam/acom/en/devnet/pdf/swf-file-format-spec.pdf)
* [SWF file-format](https://en.wikipedia.org/wiki/Swf)
