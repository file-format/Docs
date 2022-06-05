{
  "date" : "2022-03-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "PCX File Format - Paintbrush Bitmap Image File",
  "description":"Learn about PCX file format and APIs that can create and open PCX files.",
  "linktitle" : "PCX",
  "menu" : {
    "docs" : {
      "parent" : "image"
    }
  },
  "lastmod" : "2022-03-16"
}

## What is a PCX file?

A PCX file, Picture Exchange file, is a raster image file format that was used as native file format for PC Paintbrush application. It was developed by ZSoft Corporation, USA  for DOS and Windows platforms and was adopted as the main imaging file format before the arrival of [BMP](/image/bmp/), [JPEG](/image/jpeg/), and [PNG](/image/png/) file formats. PCX files are smaller in size as they are compressed using the RLE encoding. It is used in the multi-page [DCX](/image/dcx/) file that is primarily used to create digital fax files.

## PCX File Format

PCX files are saved to disc in binary file format. The internal file format structure follows little endian byte ordering and has the following three sections:

**`PCX Header`** - A PCX Header is 128 bytes long. It contains an identifier, a version number, image dimensions, 16 palette colors, number color planes and bit depth of each plane, and a value for compression method.

PCX Header is as shown below with reference from [Encyclopedia of graphics file formats (2nd ed.)](https://dl.acm.org/doi/10.5555/231955).
```
typedef struct _PcxHeader
{
  BYTE	Identifier;        /* PCX Id Number (Always 0x0A) */
  BYTE	Version;           /* Version Number */
  BYTE	Encoding;          /* Encoding Format */
  BYTE	BitsPerPixel;      /* Bits per Pixel */
  WORD	XStart;            /* Left of image */
  WORD	YStart;            /* Top of Image */
  WORD	XEnd;              /* Right of Image
  WORD	YEnd;              /* Bottom of image */
  WORD	HorzRes;           /* Horizontal Resolution */
  WORD	VertRes;           /* Vertical Resolution */
  BYTE	Palette[48];       /* 16-Color EGA Palette */
  BYTE	Reserved1;         /* Reserved (Always 0) */
  BYTE	NumBitPlanes;      /* Number of Bit Planes */
  WORD	BytesPerLine;      /* Bytes per Scan-line */
  WORD	PaletteType;       /* Palette Type */
  WORD	HorzScreenSize;    /* Horizontal Screen Size */
  WORD	VertScreenSize;    /* Vertical Screen Size */
  BYTE	Reserved2[54];     /* Reserved (Always 0) */
} PCXHEAD;
```

**`Image Data`** - PCX image data follows just after the header. The image data may be compressed depending upon the field setting in the header. The storage of data in the PCX file depends on the number of specified colour planes. Image data is organized in rows. In case of multiple planes, these are stored by plane within row in sequential arrangement of red, green and blue data. This pattern is repeated for each line in the plane.

## References

* [PCX - By Wikipedia](https://en.wikipedia.org/wiki/PCX)
