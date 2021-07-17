{
  "date" : "2019-10-11",
  "keywords" : [ "djvu file", "djvu file format", "what is a djvu file", "file", "djvu example", "djvu file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "DJVU File Format",
  "description":"Learn about DJVU file format and APIs that can create and open DJVU files.",
  "linktitle" : "DJVU",
  "menu" : {
    "docs" : {
      "parent" : "image"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is a DJVU file?

DjVu, pronounced as “déjà vu”, is a graphics file format intended for scanned documents and books especially those which contain the combination of text, drawings, images and photographs. It was developed by AT&T Labs. It uses multiple techniques like image layer separation of text and background images, progressive loading, arithmetic coding and lossy compression for bitonal images. Since DJVU file can contain compressed yet high-quality colour images, photographs, text, and drawings and can be saved in less space therefore, it's used on web as eBooks, manuals, newspapers, ancient documents, etc.

DjVu can be graded superior alternative to [PDF](/pdf/).  File extensions associated to DjVu are .DJVU or .DJV. DjVu can achieve compression ratios about 5 – 10 better than existing methods such as [JPEG](/image/jpeg/) & [GIF](/image/gif/) for colour documents and 3 – 8 times better than [TIFF](/image/tiff/) in black and white documents. Scanned documents at 300 DPI with full colour upto 25 MB can be compressed down to 30 to 100 KB. Similarly Black and white documents can be compressed upto 5 to 30 KB. Average HTML page can be up to 50 KB, therefore, these documents can be uploaded on net without any problem.

## Brief History ##

The DjVu technology was developed in AT&T labs by [Yann LeCun](https://en.wikipedia.org/wiki/Yann_LeCun), [Léon Bottou](https://en.wikipedia.org/wiki/L%C3%A9on_Bottou), Patrick Haffner, and Paul G from 1996 to 2001. The DjVu file format has passed through various revisions, the most recent being from 2005.


|Version|Release date|Notes
---|---|---|
|1–19|1996–1999|These are the developmental versions.
|20|April 1999|Single page was changed to Multipage format.
|23|July 2002|CID chunk
|24|February 2003|LTAnno chunk
|21|September 1999|Indirect storage format replaced. Text search layer was added.
|22|April 2001|Page orientation, color JB2
|25|May 2003|NAVM chunk. Support for DjVu bookmarks was added.
|26|April 2005|Text/line annotations

## DjVu File Format ##

DjVu documents are IFF85 files. The structure provides a hierarchy of containers which holds information in a DjVu file. These containers are also called “Chunks”. Chunk type and Chunk ID describes how the chunk is used. There is a 4byte header followed by IFF structure. The first four bytes of a DjVu file are 0x41 0x54 0x26 0x54. This section discusses the various kinds of DjVu documents and the corresponding chunks of which they consist.


|Chunk ID|Usage
---|---|
|FORM|The composite chunk having first four data bytes of the FORM chunk which are secondary identifier.
|FORM:DJVM|A multipage DjVu document. Composite chunk that contains the DIRM chunk.
|FORM:DJVU|Single page DjVu document. Composite chunk that contains the chunks which make up a page in a djvu document.
|FORM:DJVI|A “shared” DjVu file which is included via the INCL chunk.  Shared annotations and shape dictionary.
|FORM:THUM|Composite chunk that contains the TH44 chunks which are the embedded thumbnails.
|DIRM|Page name information for multi-page documents.
|NAVM|Bookmark information
|ANTa, ANTz|Annotations including both initial view settings and overlaid hyperlinks, text boxes, etc.
|TXTa, TXTz|Unicode Text and layout information.
|Djbz|Shared shape table.
|Sjbz|BZZ compressed JB2 bitonal data used to store mask.
|FG44|IW44 data used to store foreground
|BG44|IW44 data used to store background
|TH44|IW44 data used to store embedded thumbnail images
|WMRM|JB2 data required to remove a watermark
|FGbz|Color JB2 data. Provides a color for each (blit or shape?) in the corresponding Sjbz chunk.
|INFO|Information about the a DjVu page
|INCL|The ID of an included FORM:DJVI chunk.
|BGjp|JPEG encoded background
|FGjp|JPEG encoded foreground
|Smmr|G4 encoded mask

### DJVU Compression

Single image is divided into many different images, and then every image is compressed separately. For the creation of a DjVu file the image is first separated into three images, a background, foreground and a mask image. Typically the background and foreground images are lower-resolution color images; but the mask image is a higher-resolution image and typically the text is stored there. After the separation the foreground and background images are compressed through a wavelet based compression algorithm IW44, while the mask image is compressed using another method called JB2.

The JB2 encoding method eliminates much of the redundancy in the text image by identifying identical shapes on the page, such as multiple occurrences of a character in a particular font.  JB2 first codes the bitmap of each unique shape by taking advantage of the redundancy between similar shapes. It then codes the locations at which each shape appears on the page. Both JB2 and IW44 rely on a new type of adaptive binary arithmetic coder called the ZP-coder that squeezes out any remaining redundancy within a few percent of the Shannon limit.  The ZP-coder is adaptive, and faster than other approximate binary arithmetic coders.

## References ##

* [DjVu - Wikipedia](https://en.wikipedia.org/wiki/DjVu)
* [DjVu File Format](https://www.cuminas.jp/docs/techinfo/DjVu3Spec.pdf)
