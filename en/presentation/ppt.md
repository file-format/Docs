{
  "date" : "2019-12-13",
  "keywords" : [ "PPT", "file", "extension", "format", "PowerPoint", "Presentation" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description":"Learn about PPT file format and APIs that can create and open PPT files.",
  "title" : "PPT File Format",
  "linktitle" : "PPT",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
    }
  },
  "lastmod" : "2019-09-10"
}

A file with PPT extension represents PowerPoint file that consists of a collection of slides for displaying as SlideShow. It specifies the Binary File Format used by Microsoft PowerPoint 97-2003. A PPT file can contain several different types of information such as text, bulleted points, images, multimedia and other embedded OLE objects. Microsoft came up with newer file format for PowerPoint, known as [PPTX](/presentation/pptx/), from 2007 onwards that is based on Office OpenXML and is different from this binary file format. Several other application programs such as OpenOffice Impress and Apple Keynote can also create PPT files.

## Brief History ##

Microsoft introduced the PPT file format with the release of PowerPoint in 1987. The stable binary format was shared as the default in PowerPoint 97-2003 for Windows. The binary file format is supported for reading and writing by the most recent versions of PowerPoint as well including the PowerPoint 2016.

## File Format Specifications ##

Since its introduction, the PPT file format has gone through several revisions for additions of new features and enhancements. The latest version specifications available are that of revision 6.0 that were published in Aug 2018 which shouldn't be mixed with the real product number of PPT file format as Microsoft no more provides modifications for this format.

### File Format Overview ###

Some of the key components of a PPT file format are as follow:

#### Slides ####

User data such as shapes, text, animations and media are added to a presentation inside a Slide. A presentation can contain one or more slides that are displayed as slideshow when a presentation is run. A presentation contains master slides and title master slides that act as template for the common visual properties of presentation slides. There is also a notes master slide and handout master slide that serves a similar purpose and provides common visual properties for all notes slides and all printed handouts.

#### Shapes ####

Shapes are objects that allow users to add a variety of content to a slide in the form of placeholder shapes, pictures and graphs. Shapes on a master slide define common data for groups of shapes.

#### Placeholders Shapes ####

These are special placeholders that serves as containers for a variety of objects. Different placeholder shapes can be used to provide clues to insert specific types of shapes such as tables or charts. Inside a slide, a placeholder shape adopts to the visual properties from a main master slide, title master slide, or notes master slide.

#### External Objects ####

External objects such as embedded and linked audio, linked video, embedded and linked OLE objects, and hyperlinks can be embedded in a slide. These objects can be used to activate linked objects for accessing external resources during a slide show.

### File Format Structures ###

PowerPoint binary file formats consist of following streams to represent the overall document structure and data.

* Current User Stream
* PowerPoint Document Stream
* Pictures Stream
* Summary Information and Document Summary Information (Optional)

The complete specifications for DOC file format can be found as provided by [Microsoft](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx) and should be consulted in reference to sections mentioned in the following details.

#### Current User Stream ####

It keeps record of last user who opened the document and its name must be "Current User".

#### PowerPoint Document Stream ####

Keeps record of all the information about a PowerPoint presentation and explains its layout and contents. It is a required stream whose name MUST be "PowerPoint Document". The contents of this stream are specified by a sequence of top-level records. Partial ordering restrictions on the record sequence are specified in the PersistDirectoryAtom and UserEditAtom records.

As container records, the DocumentContainer, MainMasterContainer (section 2.5.3), HandoutContainer (section 2.5.8), SlideContainer (section 2.5.1), and NotesContainer (section 2.5.6) records are each the root of a tree of container records and atom records. Inside any container record, other records can exist that are not explicitly listed as child records. Unknown records are identified when the recType field of the RecordHeader structure (section 2.3.1) contains a value not specified by the RecordType enumeration (section 2.13.24). These unknown records, if encountered, MUST be ignored, and MAY<1> be preserved. Unknown records can be ignored by seeking forward recLen bytes from the end of the RecordHeader structure.

Each time this stream is written, new top-level records, a user edit, can be appended to the existing stream, or the entire stream contents can be replaced with an updated sequence of top-level records. If the entire stream is not replaced, any previously existing top-level records that comprised any previous user edit, can be made obsolete by the subsequently appended top-level records that comprise the current user edit.

#### Pictures Stream ####

This is an optional stream that Contains data about the pictures contained in a PowerPoint presentation. Its name MUST be "Pictures". The contents of this stream are specified by the OfficeArtBStoreDelay record as specified in [MS-ODRAW] section 2.2.21.

#### Summary Information Stream ####

It keeps statistics about the document following Microsoft Office standard. The name of Summary Information Stream must be "\005SummaryInformation", where \005 is the character with value 0x0005, not the string literal "\005". This stream SHOULD be omitted for encrypted documents. The contents of this stream are specified in [MS-OSHARED] section 2.3.3.2.1.

#### Document Summary Information Stream ####

An optional stream whose name MUST be "\005DocumentSummaryInformation", where \005 is the character with value 0x0005, not the string literal "\005". This stream MAY<2> be omitted for encrypted documents.The contents of this stream are specified in [MS-OSHARED] section 2.3.3.2.2.

#### Encrypted Summary Information Stream ####

An optional stream whose name MUST be "EncryptedSummary". This stream exists only in an encrypted document. The contents of this stream are specified in [MS-OFFCRYPTO] section 2.3.5.4.

#### Digital Signature Storage ####

An optional storage whose name MUST be "_xmlsignatures". It MAY be omitted and MAY be ignored. The contents of this storage are specified in [MS-OFFCRYPTO] section 2.5.2.

#### Custom XML Data Storage ####

An optional storage whose name MUST be "MsoDataStore". The contents of the storage are specified in [MS-OSHARED] section 2.3.6.

#### Signatures Stream ####

An optional stream whose name MUST be "_signatures". It SHOULD be omitted and MAY be ignored. The contents of this stream are specified in [MS-OFFCRYPTO] section 2.5.1.

## References ##

* [PPT File Format specifications](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx)
* [[MS-OSHARED]: Office Common Data Types and Objects Structures](https://msdn.microsoft.com/en-us/library/office/cc313156(v#office.12).aspx)
* [[MS-OFFCRYPTO] - Office Document Cryptography Structure](https://msdn.microsoft.com/en-us/library/office/cc313071(v#office.12).aspx)
* [PowerPoint File Formats](https://en.wikipedia.org/wiki/Microsoft_PowerPoint#File_formats)
