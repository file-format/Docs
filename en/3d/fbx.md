{
  "date" : "2019-12-12",
  "keywords" : [ "FBX", "file", "extension", "format", "3D File Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Your file format guide to know what is an FBX file and APIs that can create and open them.",
  "title" : "What is FBX file?",
  "linktitle" : "FBX",
  "menu" : {
    "docs" : {
      "parent" : "3d"
    }
  },
  "lastmod" : "2019-09-10"
}

# What is an FBX file? #

FBX, FilmBox, is a popular 3D file format that was originally developed by Kaydara for MotionBuilder. It was acquired by Autodesk Inc in 2006 and is now one of the main 3D exchange formats as used by many 3D tools. FBX is available in both binary and ASCII file format. The format was established to provided interoperability between digital content creation applications. There are many tools available for conversion from/to FBX file format.

# FBX File Format #

FBX is a proprietary format and specifications about its binary file format are not available officially. A C++ FBX SDK is provided by Autodesk for reading, writing and conversion to/from FBX file. A Python import and export script for FBX is also available in Blender software that doesn't use the FBX SDK.

### Text-Based File Structure ###

The text-based file structure is a tree-structured documented with clearly named identifiers. It consists of a nested list of nodes arranged in hierarchy where each node has:

* A NodeType identifier (class name)
* A tuple of properties associated with it, the tuple elements are the usual primitive data types: ##float, integer, string## etc.
* A list which contains nodes in the same format (recursively).

These can be represented logically as follow:

```
NodeType: SomeProperty0a, SomeProperty0b, ... , {

 NestedNodeType1 : SomeProperty1a, ...
 NestedNodeType2 : SomeProperty2a, ... , {
 ... Sub-scope
 }

 ...
}
```

Some of the standard nodes are defined as implicit list where each item consists of a nested list. Any application, that intends to access FBX geometry, has to parse these contents and make useful meaning of it. An example of text-based FBX file is as given below:

```
; FBX ...
; Copyright (C) 1997-2008 ...
; All rights reserved.
; ----------------------------------------------------
FBXHeaderExtension: {
    FBXHeaderVersion: 1003
    FBXVersion: 6000
    CurrentCameraResolution: {
        CameraName: "Model::Producer Perspective"
        CameraResolutionMode: "Window Size"
        CameraResolutionW: 1
        CameraResolutionH: 1
    }
    CreationTimeStamp: {
    ...
    }
}
;Object definitions
;------------------------------------------------------------------
Definitions: {
    Count: 2
    ObjectType: "Model" {
    Count: 2
    }
}
...
```

## Binary File Structure ##

As stated earlier, FBX file format specifications are not available publicly for FBX. Since, Blender Foundation implements the FBX file format without using the company provided SDK, some of the details about binary file format are [available](https://code.blender.org/2013/08/fbx-binary-file-format-specification/) as part of it implementation.

The binary files structure  follows the following order:

* Header
* Object Record
* Fotter

### Header ###

The file header information is comprised of 27 bytes.

* Bytes 0 - 20: Kaydara FBX Binary  \x00 (file-magic, with 2 spaces at the end, then a NULL terminator).
* Bytes 21 - 22: [0x1A, 0x00]## (unknown but all observed files show these bytes).
* Bytes 23 - 26: unsigned int, the version number. 7300 for version 7.3 for example.

### Object Record ###

The Header is followed by an object record that is a full node record with empty name and empty property list. It recursively contains the entire file formation.

### Footer ###

The FBX Footer section lies at the end of file whose contents are unknown.

## Record Formats ##

Records in an FBX file are categorized as:

* Node Records
* Property Records

### Node Record Format ###

Each Node Record Format is named and has the following memory layout.


|Size (Bytes)|Date Type|Name
--- | ---|---|
|4|UInt32|EndOffset
|4|UInt32|NumProperties
|4|UInt32|PropertyListLen
|1|UInt8|NameLen
|NameLength|char|Name
|?|?|Property[n], where n # 0:PropertyListLen
|Optional| |
|?|?|NestedList
|13|uint8[]|Null-Record

where:

* `EndOffset` is the distance from the beginning of the file to the end of the node record (i.e. the first byte of whatever comes next). This can be used to easily skip over unknown or not required records.
* `NumProperties` is the number of properties in the value tuple associated with the node. A nested list as last element is not counted as property.
* `PropertyListLen` is the length of the property list. This is the size required for storing ##NumProperties## properties, which depends on the data type of the properties.
* `NameLen` is the length of the object name, in characters. The only case where this is 0 seems to be the lists top-level.
* `Name` is the name of the object. There is no zero-termination.
* `Property[n]` is the nth property. For the format, see section property Record Format. Properties are written sequentially and with no padding.
* `NestedList` is the nested list, presence of which is indicated by a NULL–record at the very end.

The existence of a nested list entry can be determined by checking if there are bytes left until the EndOffset is reached. If so, the next object record should be read directly following the last property. The object record then follows 13 zero bytes, which then combine with the EndOffset. The purpose or requirement of the NULL entry is not known and may point at some format feature.

### Property Record Format ###

A property Record contains details about properties that are part of Node. A property record has the following memory layout:


|Size (Bytes)|Data Type|Name
--- | --- | ---
|1|char|TypeCode
|?|?|Data

TypeCode represent character codes which are ordered in groups that require similar handling. TypeCodes can be categorized in following types and TypeCode can be one of the character codes among these types.

#### Primitive Types ####

```
Y: 2 byte signed Integer
C: 1 bit boolean (1: true, 0: false) encoded as the LSB of a 1 Byte value.
I: 4 byte signed Integer
F: 4 byte single-precision IEEE 754 number
D: 8 byte double-precision IEEE 754 number
L: 8 byte signed Integer
```

Data in the primitive scalar type record is exactly the binary representation of the value, in little-endian byte order.

#### Array Types ####

```
f: Array of 4 byte single-precision IEEE 754 number
d: Array of 8 byte double-precision IEEE 754 number
l: Array of 8 byte signed Integer
i: Array of 4 byte signed Integer
b: Array of 1 byte Booleans (always 0 or 1)
```

The Data for Array Type is more complex and is in the following structure.


|Size (Bytes)|Data Type|Name
--- | --- | ---
|4|Uint32|ArrayLength
|4|Uint32|Encoding
|4|Uint32|CompressedLength
|?|?|Contents

### Special Types ###

Following are the Special Types TypeCodes.

```
S: String
R: raw binary data
```

Both of these TypeCodes are represented as follow:


|Size (Bytes)|Data Type|Name
--- | --- | ---
|4|Uin32|Length
|Length| |

The string is not zero-terminated, and may well contain ##\0## characters (this is actually used in some FBX properties).

## References ##

* [FBX - The Autodesk SDK](http://help.autodesk.com/view/FBX/2017/ENU/?guid#__files_GUID_105ED19A_9A5A_425E_BFD7_C1BBADA67AAB_htm)
* [FBX Binary File Format Specifications](https://code.blender.org/2013/08/fbx-binary-file-format-specification/)
* [FBX - Wikipedia](https://en.wikipedia.org/wiki/FBX#File_format)
