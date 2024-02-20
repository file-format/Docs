{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "PCL",
  "description": "Learn about PCL file format and APIs that can create and open PCL files.",
  "linktitle": "PCL",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-pcl"
    }
  },
  "lastmod": "2019-09-10"
}

## What is a PCL file? ##

PCL stands for Printer Command Language which is a Page Description Language introduced by Hewlett Packard (HP). HP created PCL to provide an efficient way for controlling printer features across many different printing devices. The format was originally developed for HP's dot matrix and Inkjet printers, but has been part of various thermal, matrix and page printers with the passage of time. The format underwent several different revisions, resulting in different versions where each version was enhanced to meet the demands of time with respect to the printer control features. Today, PCL is the most widely spread printer language in the laster printer market.

## PCL Versions ##

PCL versions differ in functionality (e.g. font type support: bitmap fonts, scalable fonts (Intellifonts, TrueType fonts), raster graphic compression methods, HP-GL/2 graphic support).

**PCL 1:** around 1980 - Print and Space functionality is the base set of functions provided for simple, convenient, single-user workstation output.

**PCL 2:** around 1980 - EDP (Electronic Data Processing)/Transaction functionality is a superset of PCL 1. Functions were added for general purpose, multi-user system printing.

**PCL 3**: 1984 - Office Word Processing functionality is a superset of PCL 2. Functions were added for high-quality, office document production and increased dpi up to 300 dpi. It allowed for the use of a limited number of bitmapped fonts and graphics, and supported HP-GL. PCL 3 was widely imitated by other printer manufacturers and was referred to by these companies as “LaserJet Plus Emulation.”
(Printers: HP DeskJet family, HP LaserJet series printer, HP LaserJet Plus series printer)

**PCL3+:** Used by DeskJet and DesignJet family of printers.

**PCL3c:** Used by DeskJet and DesignJet family of printers.

**PCL3e**: Used by DeskJet and DesignJet family of printers. Now used in PhotoSmart also.

**PCL3GUI**: Uses RTL and is used by DeskJet and DesignJet family of printers.

**PCLSLEEK**: Uses RTL and is used by DeskJet and DesignJet family of printers.

**PCL 4**: 1985 - Page formatting functionality is a superset of PCL 3. Supported macros, larger bitmapped fonts and graphics. (Printers: HP LaserJet II, HP LaserJet IIP (PCL 4.5))

**PCL 5:** 1990 - Office Publishing functionality is a superset of PCL 4. New publishing capabilities include font scaling and HP-GL/2 (vector) graphics. (Printers: HP LaserJet III)

**PCL 5e:** 1994 - This is a major revision, which includes new features like Adaptive Compression System, 2byte character encoding, support for vector fonts and bi-directional configuration commands. Includes Logical Operations (corresponds to GDI ROPs) to improve Windows support before clipping paths. (Printers: HP LaserJet 4)

**PCL 5j:** New features like 2-byte character support for Japanese resident scalable fonts, vertical writing, Japanese paper sizes and typeface strings. (Printers: HP LaserJet 4PJ)

**PCL 5c:** 1995 - Colour support and Logical Operations was added to PCL5. PCL5c predates PCL5e. Some models also support clipping paths. (Printers: HP Colour LaserJet, HP PaintJet 300 XL (first printer with PCL5c), HP DeskJet 1200C/1600C (these model numbers have been re-used and the newer models are not PCL 5c)

**PCL 5ce:** Supports Agfa Microtype scalable typefaces. (Printers: HP 2500c Pro Printer)

**PCL 6 / XL:** 1996 - PCL 6 or PCL XL is a new format introduced in 1995, which is not compatible with any previous versions of PCL. (Printers: HP LaserJet 5, 5M and 5N)

## PCL 6 Overview ##

HP introduced PCL 6 in 1996 that was the next evolution of the PCL language and related technologies. It has following there components:

**PCL 6 Enhanced:** provides optimized version for printing from graphical user interfaces (GUIs) like MS Windows and OS/2

**PCL 6 Standard:** provides complete backward compatibility with past HP LaserJet printers

**PCL Font Synthesis:** provides scalable fonts, font management and storage of forms and fonts.

The extended version PCL XL is closer to GDI that many applications use. It makes sure that less translations take place that results in increased WYSIWYG capabilities and better performance with applications that support escapes implemented by the Enhanced driver. The output from the Enhanced (PCL XL) driver may not be the same as the output from the Standard driver. If the output is not as expected, choose the Standard (PCL5e) driver instead.

PCL 6 Enhanced commands are designed to optimally match the graphics printing requirements for GUI-based applications. In most cases, for every graphics print command that a GUI wishes to perform, there is a matching PCL 6 Enhanced command. This reduces the number of commands required to describe a graphics page. Each command in PCL 6 Enhanced is designed to require minimal data transfer from the host PC to the printer. This reduces the amount of data required to describe a page.

The Windows Printing System for most HP LaserJet printers provides two separate drivers: Standard and Enhanced. The Standard driver provides backward compatibility by using PCL 6 Standard (PCL5e) commands to print simple text or mixed text and graphics pages. The Enhanced driver utilizes the PCL 6 Enhanced commands that have been optimized for printing complex graphics pages.

## PCL 6 Class Revisions ##

#### Class 1.1 ####

**Draw tools:** Support drawing lines, arcs/ellipses/chords, (rounded) rectangles, polygons, Bezier paths, clipped paths, raster images, scanlines, raster operations.
**Colour handling:** Support 1/4/8-bit palettes, RGB/grey colour space. Support custom halftone patterns (max 256 patterns).
**Compression:** Supports RLE.
**Units of measurement:** Inch, millimetre, tenth of millimetre.
**Paper handling:** Support custom or predefined sets of paper types, including common Letter, Legal, A4, etc. Can choose paper from manual feed, trays, cassettes. Paper can be duplexed horizontally or vertically. Paper can be oriented in portrait, landscape, or 180 degree rotation of the former two.
**Font:** Supports bitmap or TrueType fonts, 8 or 16-bit code points. Choosing character set uses different symbol set code from PCL 5. When bitmap font is used, many scaling commands are unavailable. When TrueType font is used, variable length descriptors, continuation blocks are not supported. Outline font can be rotated, scaled, or sheared.

#### Class 2.0 ####

**Compression:** Added a proprietary JPEG compression called JetReady.
**Paper handling:** Media can redirected to different output bins (up to 256). Added A6 and Japanese B6 preset media sizes. Added Third cassette preset, 248 external tray media sources.
**Font:** Text can be written vertically.

#### Class 2.1 ####

**Colour handling:** Added Colour matching feature.
**Compression:** Added Delta Row.
**Paper handling:** Orientation, media size are optional when declaring a new page. Added B5, JIS 8K, JIS 16K, JIS Exec paper types.

#### Class 3.0 ####

**Colour handling:** Allow using different halftone settings for vector or raster graphics, text. Supports adaptive half-toning.
**Protocol:** Supports PCL passthrough, allowing PCL 5 features to be used by PCL 6 streams. However, some PCL 6 states are not preserved when using this feature.
**Font:** Supports PCL fonts.
**Viewer/Converter:** PCLReader (freeware) can view, convert or print any level of PCL 6 (including JetReady) to any printer.

## References ##

* [PCL - By Wikipedia](https://en.wikipedia.org/wiki/Printer_Command_Language) 
