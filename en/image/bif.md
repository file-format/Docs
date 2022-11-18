{
  "date" : "2022-11-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "BIF File - Ventana Whole Slide Image Format",
  "description":"Learn about BIF file format and APIs that can create and open BIF files.",
  "linktitle" : "BIF",
  "menu" : {
    "docs" : {
      "identifier":"image-bif",
      "parent" : "image"
    }
  },
  "lastmod" : "2022-11-17"
}

## What is a BIF file?

A BIF file is a raster image file that contains the slide specimen image. It consists multiple TIFF images that are combined by slide viewing applications into a single composite image. BIF files are created by Ventana Medical systems digital slide scanner and are fully compliant with the BigTIFF-variant of the [TIFF](/image/tiff/) v 6.0 definition.

## BIF File Format

A BIF file is saved as binary image file and consist of as many as 200,000 x 200,000 pixels. This can lead to large file sizes, breaking the 4 GB size limit imposed by the 32-bit file pointers defined by the TIF-standard. With 64-bit file pointers, however, this file-size barrier is overcome by the BigTIFF-variant of the TIFF-standard.

### Who uses BIF File?

BIF files are used by digital slide scanners to scan and create digital copies of slide specimens. If you are a Pathologist, you can open these BIF files in slide-viewing applications. With great level of details and high resolution data, you can zoom in and out a slide image to view specimen sections in more or less details. The [XML](/web/xml/) metadata file present in these files defines how the images should be combined, and the image that should be used as the file's thumbnail.

## How to Open BIF File?

You can open BIF files with:

 * OpenSlide (cross-platform)
 * ImageJ (cross-platform)
 * NetScope Viewer (Windows)

## References ##

 * [Roche Digital Pathology BIF Whitepaper](https://diagnostics.roche.com/content/dam/diagnostics/Blueprint/en/pdf/rmd/Roche-Digital-Pathology-BIF-Whitepaper.pdf)
