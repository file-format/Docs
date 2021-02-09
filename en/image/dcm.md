{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "DCM File Format - Digital Medical Information File",
  "description":"Learn about DCM file format and APIs that can create and open DCM files.",
  "linktitle" : "DCM",
  "menu" : {
    "docs" : {
      "parent" : "image"
    }
  },
  "lastmod" : "2020-08-03"
}

## What is a DCM file?

Files with .dcm extension represent digital image which stores medical information of patients such as MRIs, CT scans and ultrasound images. DCM files use [DICOM](/image/dicom) (Digital Imaging and Communications in Medicine) image file format and can include patient’s information for reference. It was developed by the [National Electrical Manufacturers Association](https://en.wikipedia.org/wiki/National_Electrical_Manufacturers_Association) (NEMA) and was meant to standardize the imaging file format for distribution and viewing of medical images.

## DCM File Format

DCM files store information in DICOM image format. These files store the Data Set, which is real world information, which represents a SOP instance related to a DICOM IOD. DICOM File Meta Information is stored in the file followed by the byte stream of the actual data set.

### DICOM File Meta Information ##

Every DICOM file includes an identification information header for the encapsulated data set which consists of:
   * A 128-byte File Preamble
   * 4 byte DICOM Prefix
   * File Meta Elements

This header is a must for every DICOM file.

### File Meta Elements ###
|Attribute Name|Tag|Type| Attribute Description
---|---|---|---|
|File Preamble|No Tag or Length Fields|1|A fixed 128 byte field available for Application Profile or implementation specified use. If not used by an Application Profile or a specific implementation all bytes shall be set to 00H. File-set Readers or Updaters shall not rely on the content of this Preamble to determine that this File is or is not a DICOM File.
|DICOM Prefix|No Tag or Length Fields|1|Four bytes containing the character string "DICM". This Prefix is intended to be used to recognize that this File is or not a DICOM File.
|File Meta Information Group Length|(0002,0000)|1|Number of bytes following this File Meta Element (end of the Value field) up to and including the last File Meta Element of the Group 2 File Meta Information
|File Meta Information Version|(0002,0001)|1|This is a two byte field where each bit identifies a version of this File Meta Information header. In version 1 the first byte value is 00H and the second value byte value is 01H.Implementations reading Files with Meta Information where this attribute has bit 0 (lsb) of the second byte set to 1 may interpret the File Meta Information as specified in this version of PS3.10. All other bits shall not be checked.
|Media Storage SOP Class UID|(0002,0002)|1|Uniquely identifies the SOP Class associated with the Data Set. SOP Class UIDs allowed for media storage are specified in PS3.4 - Media Storage Application Profiles.
|Media Storage SOP Instance UID|(0002,0003)|1|Uniquely identifies the SOP Instance associated with the Data Set placed in the file and following the File Meta Information.
|Transfer Syntax UID|(0002,0010)|1|Uniquely identifies the Transfer Syntax used to encode the following Data Set. This Transfer Syntax does not apply to the File Meta Information.
|Implementation Class UID|(0002,0012)|1|Uniquely identifies the implementation that wrote this file and its content. It provides an unambiguous identification of the type of implementation that last wrote the file in the event of interchange problems.
|Implementation Version Name|(0002,0013)|3|Identifies a version for an Implementation Class UID (0002,0012) using up to 16 characters of the repertoire.
|Source Application Entity Title|(0002,0016)|3|The DICOM Application Entity (AE) Title of the AE that wrote this file's content (or last updated it). If used, it allows the tracing of the source of errors in the event of media interchange problems.
|Private Information Creator UID|(0002,0100)|3|The UID of the creator of the private information (0002,0102).
|Private Information|(0002,0102)|1C|Contains Private Information placed in the File Meta Information. The creator shall be identified in (0002,0100). Required if Private Information Creator UID (0002,0100) is present.

### Data Set Encapsulation ###

A DICOM file contains a single Data Set which represents a single SOP Instance related to a single SOP Class. The Transfer Syntax UID of the DICOM File Meta Information shall be defining the Transfer Syntax used to encode the Data Set.

### Support for File Management Information ###

The Media Format Layer provides following File Management Information if necessary for a given DICOM Application Profile.

  * File content owner identification

  * File access statistics (e.g., date and time of creation)

  * Application file access control

  * Physical media access control (e.g., write protect)

## References ##
  * [DICOM Standard](https://www.dicomstandard.org/current/)
  * [DICOM File Format](http://dicom.nema.org/dicom/2013/output/chtml/part10/chapter_7.html)
