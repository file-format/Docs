{
  "date": "2019-10-11",
  "keywords": [
    "gbr file",
    "gbr file format",
    "what is a gbr file",
    "file",
    "gbr example",
    "gbr file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "GBR File Format - Gerber File Format for PCB",
  "description": "Learn about GBR file format and APIs that can create and open GBR files.",
  "linktitle": "GBR",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-gbr"
    }
  },
  "lastmod": "2019-09-10"
}

## What is a GBR file?

A file with .gbr extension is a Gerber image file format for exchange of printed circuit board (PCB) design data transfer. It was developed by Ucamco. PCB design data is the main component required by the fabrication industry for handling. A GRB file contains PCB data such as copper layers, solder mask, legend, and drill and route data. It can be used to transfer data such as PCB fabrication characteristics including thickness or finish in a standardized format. All PCB design systems output Gerber files that can be handled by PCB fabrication systems. GBR files have now become the de facto standard for printed circuit board (PCB) design data transfer. Ucamco has provided a [free online viewer](https://gerber-viewer.ucamco.com/) to open and view GBR file formats.

## GBR File Format

GBR is a UTF-8 human-readable format that consists of just 27 commands. Due to this short list of commands and its compactness, GBR is easy to debug. Gerber at its core is an open vector format for 2D binary images. Meta-information is transferred with the images via Attributes. A single GRB file specifies a single image and does not require any accompanying files or external parameters to be interpreted. One image needs one file only. It uses 7-bit ASCII characters for all commands and names defined in the specification that are printable. This fully covers complete image generation.

### Example GBR File

Following is an example Gerber file that creates a circle of 1.5 mm diameter centred on the origin. There is one command per line.

```
%FSLAX26Y26*%
%MOMM*%
%ADD   100C,1.5*%
D100* X0Y0D03*
M02*
```

## References

 * [Gerber Format](https://www.ucamco.com/en/gerber)
