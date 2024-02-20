{
  "date": "2020-01-10",
  "keywords": [
    "dib file",
    "dib file format",
    "what is a dib file",
    "file",
    "dib example",
    "dib file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "DIB",
  "description": "Learn about DIB file format and APIs that can create and open DIB files.",
  "linktitle": "DIB",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-dib"
    }
  },
  "lastmod": "2020-01-10"
}

## What is a DIB file?

A Device-Independent bitmap (DIB) is a raster image file that is similar in structure to the standard Bitmap files([BMP]()/image/bmp/)). It contains a color table that describes the mapping of RGB colors to the pixel values. This enables DIB to represent image on any device. It can be opened with almost all applications that can open a standard BMP file on Windows as well as macOS. DIB are binary files and have a complex file format similar to BMP. DIB images are independent of the output capabilities of rendering devices in terms of color depth and pixel-per-inch.

## DIB File Format Specifications ##
A DIB contains the following color and dimension information:

  * The color format of the device on which the rectangular image was created.
  * The resolution of the device on which the rectangular image was created.
  * The palette for the device on which the image was created.
  * An array of bits that maps red, green, blue ( RGB ) triplets to pixels in the rectangular image.
  * A data-compression identifier that indicates the data compression scheme (if any) used to reduce the size of the array of bits.

### DIB Data Block format ###

DIB comes in the context of memory block as compared to .DIB files stored on disc. The memory block comprises of structure which is in accordance with the Windows API specifications for DIBs. Actual DIB consists of:
  * A header
  * Color palette
  * Pixel Data

Practically, working with palette, header and image data is done as if they were three separate blocks of memory. A handle to this common block of memory is assigned using GlobalAlloc and is known as HDIB, which is used to extract and work with the header, color table and pixel data.

### Structures ###
Information contained in a DIB are represented by different structures. These include:

BITMAPInfo - Defines the dimension and color information for a DIBs
```
typedef struct tagBITMAPINFO {
  BITMAPINFOHEADER bmiHeader;
  RGBQUAD          bmiColors[1];
} BITMAPINFO, *LPBITMAPINFO, *PBITMAPINFO;
```
It consists of a BITMAPINFOHEADER:

```
typedef struct tagBITMAPINFOHEADER {
  DWORD biSize;
  LONG  biWidth;
  LONG  biHeight;
  WORD  biPlanes;
  WORD  biBitCount;
  DWORD biCompression;
  DWORD biSizeImage;
  LONG  biXPelsPerMeter;
  LONG  biYPelsPerMeter;
  DWORD biClrUsed;
  DWORD biClrImportant;
} BITMAPINFOHEADER, *PBITMAPINFOHEADER;
```
followed by two or more RGBQAD structures.

```
typedef struct tagRGBQUAD {
  BYTE rgbBlue;
  BYTE rgbGreen;
  BYTE rgbRed;
  BYTE rgbReserved;
} RGBQUAD;
```
### Data Bits ###
|Bits|Description|
---|---|
|1-bit format (monochrome)|Monochrome bitmaps consist of two colors (black and white). Due to this limited number of colors, these bitmaps take less space on disc. The bitBitCount returns true or false for representation of both the colors. Most of the applicaitons skip the palette completely if bitBitCount==1.
|4 bit format (VGA or 16 color)|Each byte of image data represents two pixels and bitBitCount==4. These bits representthe color of the pixel in the descending order.
|8 bit format (256 colors)|This 8-bit format can represent a maximum of 256 colors. Each byte in the image's bitmap data array represents a single pixel. The value of that byte is the number of the color palette entry to be used from the 256 entries as represented by the bmciColors.
|24 bit format (TrueColor)|These bitmaps can have a maximum of 2^24 colors (biBitCount == 24).Each three-byte sequence in the bitmap data array represents the relative intensities of the three primary hues of a pixel. The hues are described as values ranging from 0 to 255 and are stored in the three bytes in the order Blue, Green and Red. This is an important distinction, because most references to colors in Windows use the opposite order: Red/Green/Blue, so think "BGR" when working with TrueColor images instead of "RGB". A color palette can be specified to accelerate the drawing process for Windows, in which case biClrUsed will not be 0. But as you can see, it's not needed, since the pixel data itself contains the color information.
|32 bit format|32 bit images have a maximum of 2^24 colors (biBitCount == 24).

## References ##
  * [Device-Independent Bitmaps - By Microsoft](https://learn.microsoft.com/en-us/windows/win32/gdi/device-independent-bitmaps)
