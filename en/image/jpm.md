{
  "date" : "2019-11-25",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "JPM - JPEG 2000 Compound File Format",
  "description":"Learn about JPM file format and APIs that can create and open JPM files.",
  "linktitle" : "JPM",
  "menu" : {
    "docs" : {
      "parent" : "image"
    }
  },
  "lastmod" : "2021-02-08"
}

## What is a JPM file?

JPM refers to JPEG 2000 image coding system Part 6 which is used for document imaging. It is based on the Mixed Raster Content Standard (ISO/IEC 16485) and contains layered still images that use JPEG 2000 and other encodings. In addition to its own specifications, JPM file format inherits features from its parent i.e. the [jp2](/image/jp2/) file format.

## JPM File Format

The JPM file format is defined by [ISO/IEC 15444-6:2003](http://www.iso.org/iso/home/store/catalogue_ics/catalogue_detail_ics.htm?csnumber=61124) -- the JPEG 2000 image coding system -- Part 6: Compound image file format. A compound image may contain scanned images, synthetic images or both, requiring a mix of continuous tone and bi-level compression methods. The JPM file format defines a composition model that describes the method of combining multiple images to generate a compound image using the multi-layer Mixed Raster Content (MRC) imaging model, defined in ITU-T T.44 | ISO/IEC 16485.

### JPM Specifications
The JPM file format standard specifies it to be a binary container to represent a compound image by which multiple images can be combined into a single image. It sets the mechanism for grouping multiple images in a hierarchy of layout objects, pages and page collections to store JPEG 2000 and other compressed image data formats. The format includes the mechanism of incorporating metadata (often referred to as structural metadata in digital library projects).

## References

 * [ITU-T Rec. T.805](http://www.itu.int/rec/T-REC-T.805/en)
 * [ISO/IEC 15444-6:2013](http://www.iso.org/iso/home/store/catalogue_ics/catalogue_detail_ics.htm?csnumber=61124)
 * [Wikipedia:JPEG 2000](http://en.wikipedia.org/wiki/JPEG_2000)
