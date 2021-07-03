{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "ICO - Image File Format",
  "description":"Learn about ICO file format and APIs that can create and open ICO files.",
  "linktitle" : "ICO",
  "menu" : {
    "docs" : {
      "parent" : "image"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is a ICO file?

Files with ICO extension are image file types used as icon for representation of an application on [Microsoft Windows](https://docs.microsoft.com/en-us/previous-versions/ms997636(v#msdn.10)). These come in different size, colour support and resolution to suit the requirements of the display. Another similar image file format on Microsoft Windows is [CUR](/image/cur/) for cursor representation and defines a hotspot in the image header. On MacOS, ICNS file formats serve the same purpose as ICO files. Several online websites as well as applications provide the feature of creating such files and convert other image formats such as [BMP](/image/bmp/), [PNG](/image/png/), etc. to icon file format. The official IANA registered Internet media type for ICO files is image/vnd.microsoft.icon.

## Brief History ##

Icons were introduced with the launch of Microsoft Windows 1.0. These were 32x32 in size and were monochrome. With the arrival fo win32, support for icon images in true colour was introduced with up to 256x256 pixels in dimension. Windows XP was the first to provide support for 32-bit colour icon images, allowing semi-transparent areas like shadows, anti-aliasing and glass-like effects to be added to the icon. Microsoft only recommended icon sizes up to 48×48 pixels for Windows XP. Windows Vista added a 256×256-pixel icon view to Windows Explorer, as well as support for the compressed [PNG](/image/png/) format. With users using higher resolutions and high DPI modes, larger icon formats (such as 256×256) are recommended.

## ICO File Format ##

A single ICO file consists of one or more than one small images of multiple sizes and colour depths. The presence of images of multiple sizes is for appropriate scaling at different screen resolutions. All values in ICO/CUR files are represented in [little-endian](https://en.wikipedia.org/wiki/Little-endian) byte order.

The ICO file consists of an Icon header, an Icon Directory,

|Field|Description
---|---|
|Icon Header|Stores general information about the ICO file.
|Directory[1..n]|Stores general information about every image in the file.
|Icon #1|The actual "data" for the first image in old AND/XOR DIB format or newer PNG
|...|
|Icon #n|Data for the last icon image

### Header ###

|Offset|Size (in bytes)|Purpose
---|---|---|
|0|2|Reserved. Must always be 0.
|2|2|Specifies image type: 1 for icon (.ICO) image, 2 for cursor (.CUR) image. Other values are invalid.
|4|2|Specifies number of images in the file.

### Directory ###

The directory contained in an ICO file, represented as ICONDIR structure, contains an ICONDIRECTORY structure for each image in the file. The same is followed by a contiguous block of all image bitmap data. This is as shown below.

|Offset|Size|Description
---|---|---|
|0 (0)|1|Width, should be 0 if 256 pixels
|1 (1)|1|Height, should be 0 if 256 pixels
|2 (2)|1|Color count, should be 0 if more than 256 colors
|3 (3)|1|Reserved, should be 0
|4 (4)|2|Color planes when in .ICO format, should be 0 or 1, or the X hotspot when in .CUR format
|6 (6)|2|Bits per pixel when in .ICO format, or the Y hotspot when in .CUR format
|8 (8)|4|Size of the bitmap data in bytes.
|12 (C)|4|Offset in the file.

## References ##

* [ICO - By Wikipedia](https://en.wikipedia.org/wiki/ICO_(file_format))
* [IANA - vnd.microsoft.icon](http://www.iana.org/assignments/media-types/image/vnd.microsoft.icon)
