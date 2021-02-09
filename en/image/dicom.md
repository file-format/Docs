{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "DICOM - Digital Imaging and Communications File Format",
  "description":"Learn about DICOM file format and APIs that can create and open DICOM files.",
  "linktitle" : "DICOM",
  "menu" : {
    "docs" : {
      "parent" : "image"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is a DICOM file?

DICOM is the acronym for Digital Imaging and Communications in Medicine and pertains to the field of Medical Informatics. DICOM is used for the integration of medical imaging devices like printers, servers, scanners etc from various vendors and also contains identification data of each patient for uniqueness. DICOM files can be shared between two parties if they are capable of receiving image data in DICOM format. The communication part of DICOM is application layer protocol and uses TCP/IP to communicate between entities. Versions supported by web services are 1.0, 1.1, 2 or later.

## History ##

DICOM was developed jointly by American College of Radiology (ACR) and National Electrical Manufacturers Association (NEMA) for the exchange and viewing of medical images like MRIs, CT scans and ultrasound images. Initially, it was hard to decode the images that the machines produced. Therefore, ACR and NEMA together formed a team in 1983 which released its first standard, ACR/NEMA 300 in 1985. The second version was released in 1988 which was more popular among vendors, but soon it was realized that second version also needs improvement. The 3rd version of the standard was released in 1993 as "DICOM". 3.0 is still the latest version but it has been continuously updated since 1993.

## DICOM File Format ##

DICOM is the combination of file format definition and a network communications protocol. DICOM uses the .DCM extension. .DCM exist in two different formats i.e. format 1.x and format 2.x. DCM Format 1.x is further available in two versions normal and extended. HTTP and HTTPS protocols are used for the web services of DICOM.

### File Header ###

The file header contains 128 byte File Preamble, and 4 byte DICOM prefix.

**Preamble # 128 Bytes**|**Prefix # 4 Bytes   “D, I, C, M**

**Preamble** is used to access the images and other data in DICOM file providing compatibility with commonly used image file formats.

**Prefix** contains the string "DICM" as uppercase characters.

### Data Set ###

Each file must contain a single data set representing SOP instance and SOP Class with related IOD. Data set is the representation of real world information. Data set contains data elements and data elements contain values of the attributes of that object. Structure of attributes is specified in IODs. A DICOM data object consists of a number of attributes, including items such as name, ID, etc., and also one special attribute containing the image pixel data.

### Data Elements ###

Data element consists data element Tag, Value length and value for the Data Element. There are 5 types of Data elements namely Type 1 Required Data elements, Type 1C Conditional Data Elements, Type 2 Required Data Elements, Type 2C Conditional Data Elements and Type 3 optional Data Elements. Basic Three types of data element structures are as follow.

**Data Element with an Explicit VR**

|Group Number|Element Number|Value Representation|Reserved|Value Length|Value Field
---|---|---|---|---|---|
|2 Bytes|2 Bytes|2 Bytes|2 Bytes # 0x00, 0x00|4 Bytes|"Value Length Bytes"

**Data Element with an Explicit VR**

|Group Number|Element Number|Value Representation|Value Length|Value Field
---|---|---|---|---|
|2 Bytes|2 Bytes|2 Bytes|2 Bytes|"Value Length Bytes"

**Data Element with an Implicit VR**


|Group Number|Element Number|Value Length|Value Field
---|---|---|---|
|2 Bytes|2 Bytes|4 Bytes|"Value Length Bytes"

1. **Data Element Tag**: An ordered integer which represents the group number and element number
1. **Value Representation VR**: VR is a character string which represents the VR of the data Element.
1. **Value Length**: is he unsigned integer represent the explicit length of the value field.
1. **Value Field**: Describes the values of the data elements.

## Transfer Syntax ##

Transfer syntax is a set of rules for encoding to unambiguously represent more abstract syntaxes. With the help of transfer syntax communicating entities negotiate on common encoding techniques which they support.

## SOPs ##

Union of IOD and DIMSE defines an SOP Class.  The SOP Class definition contains the rules and semantics which may restrict the use of the services in the DIMSE Service Group or the Attributes of the IOD. Examples of Service Elements are Store, Get, Find, Move, etc. Examples of Objects are CT images, MR images, but also include schedule lists, print queues, etc.

## Services ##

DICOM provides various services, mostly related to communication of data. Each one is briefly described below:


**Store:** The DICOM Store service send images or other objects to a picture archiving and communication system (PACS) or server.


**Storage commitment:** Storage commitment service is used for confirmation that an image has been permanently stored b a device on any type of media.


**Query/retrieve:** This service enables a workstation to find the lists of images or other objects and then retrieve them from PACS.


**Modality worklist:** The modality worklist service gives a list of imaging procedures that have been scheduled for performance by an image acquisition device.


**Print:** This service sends images to printer.

## Port numbers over IP ##

DICOM uses the following TCP and UDP ports :

1. 104
1. 2761
1. 2762
1. 11112

## References ##

* [https://en.wikipedia.org/wiki/DICOM](https://en.wikipedia.org/wiki/DICOM)
* [https://www.leadtools.com/sdk/medical/dicom-spec](https://www.leadtools.com/sdk/medical/dicom-spec)
* [https://www.dicomstandard.org/concepts/](https://www.dicomstandard.org/concepts/)
* [https://www.dicomlibrary.com/dicom/](https://www.dicomlibrary.com/dicom/)
