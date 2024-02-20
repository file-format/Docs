{
  "date": "2019-10-11",
  "keywords": [
    "gif file",
    "gif file format",
    "what is a gif file",
    "file",
    "gif example",
    "gif file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "GIF - Image File Format",
  "description": "Learn about GIF file format and APIs that can create and open GIF files.",
  "linktitle": "GIF",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-gif"
    }
  },
  "lastmod": "2019-09-10"
}

## What is a GIF file? ##

A GIF or Graphical Interchange Format is a type of highly compressed image. Owned by Unisys, GIF uses the LZW compression algorithm that does not degrade the image quality. For each image GIF typically allow up to 8 bits per pixel and up to 256 colours are allowed across the image. In contrast to a [JPEG](/image/jpeg/) image, which can display up to 16 million colours and fairly touches the limits of the human eye. Back when the internet emerged, GIFs remained the best choice because they required low bandwidth and compatible for the graphics that consume solid areas of colour. An animated GIF combines numerous images or frames into a single file and displays them in a sequence to generate an animated clip or a short video. The colour limitations are up to 256 for each frame and are likely to be the least suitable for reproducing other images and photographs with colour gradient.

## GIF File Format ##

Conceptually, GIF files have a fixed-sized graphical area filled by zero or more images. Some GIF files divide the fixed-sized graphical area or blocks into sub-images capable of functioning as animated frames in case of animated GIF. The GIF format uses the pixel depths of 1 to 8 bits  to store the  bitmap data. RGB colour model and palette data are always used to store the images. Depending upon the version, a fixed-length header ("GIF87a" or "GIF89a") defines the start of a typical GIF file.

Currently, two versions of GIF: 87a and 89a are available. The former is the original GIF format while the latter is the new GIF format. In this file format, the characteristics of the blocks and pixel dimensions are mentioned in a fixed-length Logical Screen Descriptor.  The existence and size of a Global Colour Table may be specified by the screen descriptor, which tracks further details if present. The trailer is the last byte of the file that holds a single byte of  an ASCII semicolon. A typical GIF87a file layout is as follow:

### Header ###

The Header holds six bytes and is used to specify the type of file as GIF. Though the Logical Screen Descriptor is separated from actual header yet sometimes it is considered as the second header. Same structure which is used to store the header may store the Logical Screen Descriptor. All GIF files start with the 3-byte signature and uses the characters” GIF” as an identifier. The version is also three bytes in size and declares the version of the GIF file.

### Logical Screen Descriptor ###

 A fixed-length Image Descriptor specifies the screen and colour information necessary to create the GIF image. The Height and Width fields enclose the smallest value of screen resolution, obligatory to show the image data. If the display device is incapable of displaying the specified resolution, scaling will be needed to suitably display the image. Screen and Colour Map Information is displayed by the four subfields of the table below (whereas bit 0 is the least significant bit):


|Bits|Subfields
---|---|
|0-2|Size of the Global Colour Table
|3|Colour Table Sort Flag
|4-6|Colour Resolution
|7|Global Colour Table Flag

#### Global Colour Table ####

An optional Global Colour Table is placed right after the Logical Screen Descriptor. This table mapped to index the pixel colour data inside the image data. In the absence of a Global Colour Table, each image in the GIF file uses its Local Colour. It's better to supply a default colour table if both Global and Local Colour Table is missing. A series of three-byte triples composes the elements of the colour table. Each byte characterizes an RGB colour value. The red, green, and blue colours are used as values of each colour table element .The entries in the Global Colour Table hits a maximum of 256 entries and always represent in a power of two.

#### Image Data ####

The image data stores a byte of unencoded symbols followed by linked-list of sub- along with the LZW-encoded data.

#### Trailer ####

Trailer represents single byte of data that is the last character in the file. The value of this byte is permanently 3Bh and specifies the end of the data stream. Every GIF file must have the trailer in the last of each file.

## References ##

* [GIF file format](https://en.wikipedia.org/wiki/GIF)
