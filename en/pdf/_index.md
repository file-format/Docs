{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "categories" : [ "fundamentals" ],
  "description": "Portable Document Format (PDF) is a standard representation of documents independent of software, hardware, and OS. PDF standards include PDF/A, PDF/E, PDF/UA, PDF/VT and PDF/X.",
  "title" : "PDF File Format - What is a PDF file?",
  "linktitle" : "PDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf",
      "weight" : "01"
    }
  },
  "lastmod" : "2019-09-10"
}

Portable Document Format (PDF) is a type of document created by Adobe back in 1990s. The purpose of this file format was to introduce a standard for representation of documents and other reference material in a format that is independent of application software, hardware as well as Operating System. The PDF file format has full capability to contain information like text, images, hyperlinks, form-fields, rich media, digital signatures, attachments, metadata, Geospatial features and 3D objects in it that can become as part of source document.

In most of the cases, existing documents are converted to PDF rather than creating a new PDF from scratch. But that doesn't mean there are no software for creation or manipulation of PDF files.

(Have to share something about PDF file format? You can post your findings in [PDF File Format News](https://news.fileformat.com/t/PDF) section.)

## PDF File Format - Brief History

A quick go-through the timeline about the PDF file formation in terms of timeline is as follow:

**1993** - Adobe Systems made the PDF specifications available free of charge

**2008** - PDF was released as an open standard on July 1, 2008 and was published by the International Organization for Standardization as **ISO 32000-1:2008**.

**2008** - Adobe published a Public Patent License to ISO 32000-1 format royalty-free rights for all patents owned by Adobe that are necessary to make, use, sell and distribute PDF compliant implementations.

The first version of PDF designated as PDF 1.0 which later went through revisions up to PDF 1.7. PDF 1.7, which became the ISO 32000-1, include some non-standardized proprietary technologies as well like Adobe XML Forms Architecture (XFA) and JavaScript extension for Acrobat. It was on July 28, 2017 when PDF 2.0, known as ISO 32000-2:2017 was published which doesn't include any non-standardized technologies.

## PDF File Format Specifications

A PDF file is a set of bytes that can be grouped in to tokens according to syntax rules defined by PDF specifications. Once or more tokens are combined to form higher-level syntactic entities, principally objects, which are the basic data values from which a PDF document is constructed.

### File Structure of PDF Files

PDF file contents are arranged in the following sequence inside the file.

|Header
|Body
|Cross-Reference Table
|Trailer

#### PDF File Header ####

Irrespective of the PDF version, a PDF file starts with a header containing unique identifier for PDF and the version of the format such as %PDF-1.x where x ranges from 1-7.

#### File Body ####

The body of a PDF file consists of a sequence of indirect objects representing the contents of a document. The objects, as described above, represent components of the document such as fonts, pages and sampled images. Beginning with PDF 1.5, the body can also contain object streams, each of which contains a sequence of indirect objects.

#### Cross-Reference Table ####

The cross-reference table contains information that permits random access to indirect objects within the file so that the entire file need not be read to locate any particular object. The table shall contain a one-line entry for each indirect object, specifying the byte offset of that object within the body of the file. (Beginning with PDF 1.5, some or all of the cross-reference information may alternatively be contained in cross-reference streams.

#### File Trailer ####

The trailer of a PDF file enables a conforming reader to quickly find the cross-reference table and certain special objects. Conforming readers should read a PDF file from its end. The last line of the file shall contain only the end-of-file marker, %%EOF. The two preceding lines shall contain, one per line and in order, the keyword startxref and the byte offset in the decoded stream from the beginning of the file to the beginning of the xref keyword in the last cross-reference section.

### PDF Objects ###

A PDF file includes several different type of objects that are of following types

* Boolean values - representing conditional true or false
* Numbers - Integer and Real values
* Strings - contains characters within parentheses
* Names - start with a forward / character e.g. /ASomewhatLongerName results in ASomewhatLongerName
* Arrays - PDF supports one dimensional arrays. Arrays of higher dimensions can be constructed by using arrays as nested elements
* Dictionaries - collection of objects as key-value pairs. It can have zero entries.
* Streams - represents sequence of bytes which can be of unlimited length as well
* Null Object - represents a null value

There can be other other objects like comments which are introduced with the % sign and may contain 8-bit characters.

### Indirect Objects ###

Any object in a PDF file may be labelled as an indirect object. Indirect objects are given unique object identifier by which other objects can refer to it. Cross-referencing to these are maintained in an index table and marked with the xref keyword which follows the main body and gives the byte offset of each indirect object from the start of file.

### Linear and Non-Linear PDF Layouts ###

PDF layouts are categorized as Llnear and non-linear depending upon the target applications and other factors.

Non-Linear - Non-linear PDF files use less disk space as compared to linear PDF files. PDF pages of the document reside in scattered form across the PDF file and that is why non-linear files are slower as compared to linear files.

Linear PDF - Targeting online PDF viewers, Linear PDF files are constructed in such a way that they are written to disk in a linear fashion. This doesn't required browser plugins for whole document to load first before display.

### Objects Overview ###

As mentioned, PDF body is a collection of objects mentioned above. PDF is largely based on PostScript without the control features of programming languages like if and loop commands. Commands issued by Postscript code to generate graphical contents are collected and tokenized in addition to any files, graphics or fonts referred by the document. All these contents are accumulated to a single file, resulting in composed PostScript output.

#### Text ####

Text in PDF is represented by text elements which are actually displayed with glyphs from fonts.   A  glyph  is  a  graphical  shape  and  is  subject  to  all  graphical  manipulations,  such  as  coordinate transformation. Because of the importance of text in most page descriptions, PDF provides higher-level facilities to describe, select, and render glyphs conveniently and efficiently.

#### Graphics ####

The  graphics  operators  used  in  PDF  content  streams  describe  the  appearance  of  pages  that  are  to  be  reproduced on a raster output device. The facilities are intended for both printer and display applications. The graphics operators form six main groups:

* Graphics  state  operators  manipulate  the  data  structure  called  the  graphics  state,  the  global  framework  within which the other graphics operators execute. The graphics state includes the current transformation matrix (CTM), which maps user space coordinates used within a PDF content stream into output device coordinates. It also includes the current colour, the current clipping path, and many other parameters that are implicit operands of the painting operators.
* Path  construction  operators  specify  paths,  which  define  shapes,  line  trajectories,  and  regions  of  various  sorts. They include operators for beginning a new path, adding line segments and curves to it, and closing it.
* Path-painting operators fill a path with a colour, paint a stroke along it, or use it as a clipping boundary.
* Other  painting  operators  paint  certain  self-describing  graphics  objects.  These  include  sampled  images,  geometrically  defined  shadings,  and  entire  content  streams  that  in  turn  contain  sequences  of  graphics  operators.
* Text operators select and show character glyphs from fonts (descriptions of typefaces for representing text characters). Because PDF treats glyphs as general graphical shapes, many of the text operators could be grouped with the graphics state or painting operators. However, the data structures and mechanisms for dealing with glyph and font descriptions are sufficiently specialized.
* Marked-content  operators  associate  higher-level  logical  information  with  objects  in  the  content  stream.  This information does not affect the rendered appearance of the content; it is useful to applications that use PDF for document interchange.

## References ##

* [PDF File Format: Basic Structure](https://resources.infosecinstitute.com/pdf-file-format-basic-structure/)
* [PDF - Wikipedia](https://en.wikipedia.org/wiki/PDF)
* [PDF Reference - Adobe](https://www.adobe.com/content/dam/acom/en/devnet/pdf/pdf_reference_archive/pdf_reference_1-7.pdf)
