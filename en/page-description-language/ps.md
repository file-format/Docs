{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "PS",
  "linktitle" : "PS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is a .PS file? ##

PostScript (PS) is a general-purpose page description language used in the business of desktop and electronic publishing. The main focus of PostScript (PS) is to facilitate the two-dimensional graphic design. Most languages require a distinct compilation stage before the code execution while Post Script (PS) format support a runtime straight forward interpretation. Its early version defines the graphical shapes, different text appearances and modelled imageries on printed pages or displayed pages, following the rules of Adobe imaging model. A program of PS is able to intercommunicate a document description between a composition and printing system keeping the device independent and high-level. Moreover this program is also capable of governing the appearance of text and graphics on a display.

PostScript page description is available to be rendered, displayed on printer and other output device with the help of the PostScript interpreter of the device. As the commands to print characters, graphical shapes and images are executed by interpreter, for that specific device, the high-level PostScript description converts into the low level raster data format. Generally, different applications such as illustrators, document composition systems and computer-aided design (CAD) are automated to generate PostScript page descriptions. Generally programmers have to write PostScript programs at the time of new applications creation.  However, a programmer can take advantage of the capabilities of the PostScript language that are not accessible in any application by writing a PS a program for that special situation.

## Brief History ##

The concept of the PostScript language was first introduced by John Warnock. In 1966 he was working on a project of New York Harbor. He was trying to develop an interpreter for a large three-dimensional graphics for the database of that project. For processing these graphics, John Warnock conceived the Design System language. Meanwhile Xerox PARC were looking for a standard means of defining page images for their first laser printer. Though Bob Sproull and William Newman in 1975-76 developed the Press format (data format) to drive laser printers yet a language was needed for more flexibility. In 1978 Warnock joined Martin Newell in Xerox PARC and rewrote the interpretive language, JaM which was later grew and extended into the Interpress language. Warnock founded Adobe Systems in December 1982 with Chuck Geschke, Doug Brotz, Ed Taft and Bill Paxton. They started working on a simpler language called PostScript similar to Interpress, which released commercially in 1984. Steve Jobs from Apple visited them and advised them to adapt PostScript to drive laser printers.

In March 1985, the first printer with an embedded PostScript interpreter was Apple’s LaserWriter, which revolutionized the desktop publishing (DTP). The technical soundness and widespread availability made PostScript, a language of choice for desktop and electronic publishing. During 1990, an interpreter for the PostScript language was an essential part of the laser printers.

## Main Features ##

The capabilities of the PostScript language to deal with interactive graphics and page description possess the following features:

**Shapes:** Arbitrary in nature, may comprise of straight lines, curves, squares, and cubic curves which can be both self-traversing and disconnected (in sections and holes).

**Painting operators:** permit the shape outline of any thickness, color, fill or allow the shape to be drawn as a clipping to allow the cropping of any other graphic.

**Colors:** have the diversity like grayscale, RGB, CMYK, and CIE. Special kinds of colors are modeled as different feature: spot colors, color mapping, even shading and repeating patterns.

**Text:** fully integrated with graphics. Moreover, adobe imaging model allows text characters to be displayed as graphical shapes that may be operated by any normal graphics operators.

**Sampled images**: extracted from original sources (scanned photographs) or may be produced synthetically. The PostScript language offers diverse means to regenerate images at any resolution and according to different color models on an output device.

A general-purpose programming language can take the advantage of graphics capabilities PostScript language by embedding Ps in its framework. The primitive datatypes, such as numbers, characters, arrays and strings; control primitives, such as, loops, procedures and conditionals; and some unconventional features, such as dictionaries are specified in the language.  These features facilitates programmers to write commands to invoke higher level operations. These high level operations fulfill the needs of complex application. Such practice is more compact and efficient rather than using a fixed set of basic operations.

Programs written in PostScript can be produced, communicated, and interpreted in the form of ASCII source text. The whole language can be defined in the form of printable characters and white space. This representation supports programmers to create, manipulate, and understand the language easily. Moreover, file storage and transmission among diverse computers and operating systems kept convenient through machine independence.

Binary encoded forms of the language is possible, when the program is guaranteed to a fully transparent communications path to the PostScript interpreter. Strict cohesiveness to the ASCII representation of PS programs is advised from Adobe for document exchange or archival storage.

## Versions ##

PS(.ps) is the file extension for a PostScript document. UK National Archives categorize five chronological versions of PostScript file, defined in the DSC version: versions 1.0, 2.0, 2.1, 3.0, 3.1. Each version defines important structuring comments. Encapsulated PostScript File (EPS) is a special subtype of PostScript file that employs the language to specify a rectangular graphic. PostScript Language Reference Manual describes an EPS as, "An encapsulated PostScript (EPS) file is a PostScript program describing at most a single page in a form that can be imported by other applications to embed within a containing document." A PostScript document file can encapsulate an EPS file in it. An added use of PostScript is mentioned as Display PostScript (DPS). DPS generates on-screen graphics through a graphics engine that make use of PostScript imaging model and language.

## References ##

* [PostScript Format Family](https://www.loc.gov/preservation/digital/formats/fdd/fdd000029.shtml)