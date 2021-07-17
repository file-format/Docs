{
  "date" : "2019-10-11",
  "keywords" : [ "emf file", "emf file format", "what is a emf file", "file", "emf example", "emf file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "EMF - Enhanced Metafile Format",
  "description":"Learn about EMF file format and APIs that can create and open EMF files.",
  "linktitle" : "EMF",
  "menu" : {
    "docs" : {
      "parent" : "image"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is an EMF file?

**Enhanced metafile format (EMF)** stores graphical images device-independently. Metafiles of EMF comprises of variable-length records in chronological order that can render the stored image after parsing on any output device. These variable-length records can be definitions of enclosed objects, commands for drawing, and graphics properties critical to render the image accurately. When a device opens an EMF metafile using its own graphics environment, the proportions, dimensions, colors and other graphic properties of original image remains same regardless of the opening device platform.

## Brief History ##

In 1990, Microsoft designed an image file format Windows Metafile ([WMF](/image/wmf/)) for Microsoft Windows. Windows Metafiles are 16-bit format that may contain some bitmap components.WMF may consist of vector graphics and is intended to keep portable among different applications. In 1993, Win32/GDI announced the Enhanced Metafile (EMF), a newer version with enhanced flexibility and scalability. EMF also used as the graphics language commands to run the printer drivers. Microsoft now recommends the enhanced metafile format (EMF) over Windows-format (WMF). When the Windows XP was introduced, the Enhanced Metafile Format Plus (EMF+) version was released. This newer version finds its way by serializing GDI+ API calls likewise WMF/EMF records calls to GDI. There exists a gzip compressed version of EMF known as EMZ.

## EMF Metafile Format ##

Following are the essential elements of the enhanced metafile-format:

* An EMR_HEADER (version, size, the resolution of the picture at creation)
* A table for GDI objects
* A reserved palette (optional)
* Metafile records arranged in array structure (property settings, defined objects, drawing commands)
* EMR_EOF record (last record in the EMF metafile)

## EMF Versions ##
* **Original**: The original version specifies the record necessary to keep the original image and maintain its device-independent. Moreover supports the record containing graphics objects and commands for drawing.
* **Version 1**: The second version of EMF improved the flexibility and device independence by adding the record for pixel format and provision to use OpenGL command.
* **Version 2**: The third version enhanced the accuracy by adding the Metric system to measure the device surface distances, leaving the record more scalable.

## Enhanced Metafile Records ##

Metafile records are arranged in the form of array. These records have ENHMETARECORD structure and variable in length. ENHMETARECORD specifies data that define GDI functions to create a picture using enhanced metafile format. **ENHMETAHEADER** structure is always the first record in this format. This EMF header contains the following information.

Every record of enhanced metafile has two members of EMR (provides the base structure) in the beginning. The first member recognizes GDI function (parameters are used in record) which determines the type of record and is known as iType. The other member nSize define the size of each record. Remaining parameters (if any) and additional data arranged immediately below nSize. Immediately following the header an optional text description may present. The name of picture and author is recorded in that text description. The palette whose presence is an option specifies the colors used in enhanced metafile creation. The other records used to specify the GDI function which is essential in picture creation.

At least one EMF record should be present in each metafile. The traversing information from one record to other is dependent on EMF records so these records must be arranged adjacently. At any given record in the metafile except EOF_record, the length of that particular record define to move to the next record.

## Enhanced Metafile Creation ##

**CreateEnhMetaFile** function is used to create an enhanced metafile. This functions arguments are used to dimensions and storage of picture on disk/memory. Furthermore, this function requires the dimension of the device in which picture appeared first (referenced device) and context of the reference device (DC). So the arguments to handle this DC must provide when calling **CreateEnhMetaFile** function. The syntax of function is as follow:
```
HDC CreateEnhMetaFileExample(

  HDC        hdc,

  LPCSTR     lptoFilename,

  const OVAL *lprc,

  LPCSTR     lpDesc

);
```
**HDC:**  handle to a reference device.

**lptoFilename:** A pointer to the file name.

**lprc:** Pointer to oval structure specifies the picture dimensions in mm.

**lpDesc:**  a pointer to a string for the title of picture and application name that created the picture.

## Enhanced Metafile Operations ##

Following are jobs that can be accomplished using the handle to an enhanced metafile.

* Display and edit for the stored picture.
* Produce enhanced metafile copies.
* Retrieve the copy of an EMF header, optional description and binary version of an enhanced metafile
* Recapitulate the colors in the palette.

## Graphics Objects ##

In drawing and painting operations, graphics objects can be created by object creation records and can save for further use. An `EMR_SELECTOBJECT` record can retrieve these graphics objects using the playback device context. Pens, palettes, brushes, color spaces, fonts, and stock objects are some reusable object types.

## Byte Ordering ##

Little-endian format is used to store data in metafile records.

## Versioning ##

The EMF file format has been revised twice. The changed versions are original, extension 1, and extension 2. Extended versions have provision for OpenGL records and an optional descriptor for internal pixel format. A measuring facility in milliliters is added for displayed dimensions.

## References ##

* [Enhanced-Format Metafiles | Microsoft Docs](https://docs.microsoft.com/en-us/windows/desktop/gdi/enhanced-format-metafiles)
* [Enhanced Metafile Format and Specification](https://msdn.microsoft.com/en-us/library/cc230514.aspx)
