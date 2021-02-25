{
  "date" : "2021-02-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "VP6 - TrueMotion Video File",
  "description":"Learn about VP6 file format and APIs that can create and open VP6 files.",
  "linktitle" : "VP6",
  "menu" : {
    "docs" : {
      "parent" : "video"
    }
  },
  "lastmod" : "2021-02-16"
}

## What is a VP6 file?

VP6 is a lossy compression video format that was introduced by On2 technologies in May 2003. It is a part of series of video codecs developed by TrueMotion including V3, V4 and V5. The format was used shortly in broadcasting field such as with BBC reports and QuickLink software. VP6 was succeeded by VP7 Codec in January 2005 with better compression compatibility.

## VP6 File Format

Complete specifications for V6 files are not available publicly. On2 made the specifications public initially but soon these were made non-available for general users. An unofficial documentation of the VP6 file format is available at [multimedia wiki](https://wiki.multimedia.cx/index.php?title=On2_VP6) that can be referred for developer's reference.

### Macroblocks (MB)

Similar to MPEG-2, MPEG-4 parts 2 and 10, each video frame of a VP6 file is composed of an array of 16x16 macroblocks (MB). Each MB can be in one of the following modes:

 * Intra MB
 * Inter MB, null MV, previous frame reference
 * Inter MB, differential MV, previous frame reference
 * Inter MB, four MVs, previous frame reference
 * Inter MB, MV 1, previous frame reference
 * Inter MB, MV 2, previous frame reference
 * Inter MB, null MV, bookmarked frame reference
 * Inter MB, differential MV, bookmarked frame reference
 * Inter MB, MV 1, bookmarked frame reference
 * Inter MB, MV 2, bookmarked frame reference

### Frame Header

The frame header of a VP6 is as shown below that follows the big-endian bit packing.

|Syntax|Number of bits|Type|Symantecs|
---|---|---|---|
|frame_mode|1|Enum|0x0 signifies an intra frame|
|qp	|6	|Unsigned	|Quantization parameter valid range 0..63|
|marker|	1|	Constant|	0=VP61/62, 1=VP60|
|if (frame_mode == 0) {	|		0 | |equals to INTRA_FRAME|
|version	|5|	Constant|	6=VP60/61, 7=VP60(Electronic Arts), 8=VP62|
|version2	|2|	Constant	|0=VP60, 3=VP61/62|
|interlace	|1|	Boolean	|true (1) means interlace will be used|
|if (marker==1 or version2==0) {||||
|offset	|16	|Unsigned|	secondary buffer offset (bytes releative to start of buffer)|
|}||||
|dim_y	|8|	Unsigned|	Macroblock height of video|
|dim_x	|8|	Unsigned|	Macroblock width of video|
|render_y	|8	|Unsigned	|Display height of video|
|render_x	|8	|Unsigned	|Display width of video|
|}else{||||
|if (marker==1 or version2==0) {||||
|offset	|16	|Unsigned	|Secondary buffer offset (bytes releative to start of buffer)|
|}||||
|}||||

## References

* [VP6 File Format ](https://wiki.multimedia.cx/index.php?title=On2_VP6)
* [VP6 Wikipedia](https://en.wikipedia.org/wiki/VP6#:~:text=On2%20TrueMotion%20VP6%20is%20a,Video%2C%20and%20JavaFX%20media%20files.)
