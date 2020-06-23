{
  "date" : "2019-12-13",
  "keywords" : [ "PPTX", "file", "extension", "format", "PowerPoint", "Presentation" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Your file format guide to know what is a PPTX file and APIs that can create and open them.",
  "title" : "PPTX File Format - What is a PPTX file?",
  "linktitle" : "PPTX",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
    }
  },
  "lastmod" : "2019-09-10"
}

Files with PPTX extension are presentation files created with popular Microsoft PowerPoint application. Unlike the previous version of presentation file format PPT which was binary, the PPTX format is based on the Microsoft PowerPoint open XML presentation file format. A presentation file is a collection of slides where each slide can comprise of text, images, formatting, animations, and other media. These slides are presented to audience in the form of slideshows with custom presentation settings.

## Brief History ##

PPTX file format was introduced in 2007 and uses the Open XML standard adapted by Microsoft back in 2000. Previous to PPTX, the common file format used was PPT that was pure binary file format. The new file type has added advantages of small file sizes, less changes of corruption and well formatted images representation. It was in the early 2000 when Microsoft decided to go for the change to accommodate the standard for **Office Open XML**. By 2007, this new file format became part of Office 2007 and is carried on in the new versions of Microsoft Office as well.

## File Format Specifications ##

Files generated with office Open XML file format is a collection of XML files along with other files that provide links between all the constituent files. This collection is actually a compressed archive that can be extracted to view its contents. To do so, just rename the PPTX file extension with zip and extract it for observing its contents.

Following sections shed some light on each one of these.

### [Content_Types].xml ###

This is the only file that is found at the base level when the zip is extracted. It lists the content types for parts within the package. All references to the XML files included in the package are referenced in this XML file. Following is a content type for a slide part:

```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```

If new parts need to be added to the package, it can be done by adding the new part and update any relationships within the .rels files. It has to be kept in mind that for such a change, the Content_Types.xml must also be updated.

### \_rels (Folder) ###

Relationships between the other parts and resources outside of the package are maintained by the relationships part. The Relationships folder contains a single XML file that stores the package-level relationships. Links to the key parts of the PPTX files are contained in this file as URIs. These URIs identify the type of relationship of each key part to the package. This includes the relationship to primary office document located as ppt/presentation.xml and other parts within docProps as core and extended properties.

```
<Relationship Id#"rId1" Type#"http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
```

Each part of document that is the source of one or more relationships will have its own relationships part where each such relationship part is found within a \_rels sub-folder of the part and is named by appending '.rels' to the name of the part. The main content part (presentation.xml) has its own relationships part (presentation.xml.rels). It contains relationships to other other parts of the content such as slideMaster1.xml, notesMaster1.xml, handoutMaster1.xml, slide1.xml, presProps.xml, tableStyles.xml, theme1.xml, as well as the URIs for external links.

#### Explicit Relationship ####

For an explicit relationship, a resource is referenced using the Id attribute of a <Relationship> element. That is, the Id in the source maps directly to an Id of a relationship item, with an explicit reference to the target.

For example, a slide might contain a hyperlink such as this:

```
<a:hlinkClick r:id#"rId2">
```

The r:id#"rId2" references the following relationship within the relationships part for the slide (slide1.xml.rels).

```
<Relationship Id#"rId2" Type#"http://. . ./hyperlink" Target#"http://www.google.com/" TargetMode#"External"/>
```

#### Implicit Relationship ####

For an implicit relationship, there is no such direct reference to a `<Relationship> Id`. Instead, the reference is understood.

### ppt Folder ###


This is the main folder that contains all the details about the contents of the Presentation. By default, it has following folders:

* \_rels
* theme
* slides
* slideLayouts
* slideMasters

and following xml files:

* presentation.xml
* presProps.xml
* tableStyles.xml
* viewProps.xml

## References ##

* [[MS-PPTX] - PPTX File Format](https://msdn.microsoft.com/en-us/library/dd926741(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)
