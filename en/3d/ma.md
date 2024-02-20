{
  "date": "2019-10-11",
  "keywords": [
    "ma",
    "ma file",
    "ma file format",
    "file format",
    "3d",
    "ma file download",
    ".ma file",
    ".ma"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "description": "Learn about MA file format and APIs that can open and create MA files.",
  "title": "MA File Format",
  "linktitle": "MA",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-ma"
    }
  },
  "lastmod": "2021-06-04"
}

## What is an MA file?

A file with .ma extension is a 3D project file created with Autodesk Maya application. It contains large list of textual commands to specify information about the file. A **.ma file** can be opened and edited in any text editor to fix any issues with the commands in case a file gets corrupt. These files contain information for defining the 3D Scene information such as geometry, lighting, animation, and rendering. 

## MA File Format

MA files are saved to disc in ASCII text format unlike the MB files that are saved in binary file format to disc. A detailed reference for MA file format is available in [Autodesk Maya Documentation](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001) and can be referred to for developer's reference.

### MA File Header

The MA file header starts with a section of comments that gives the creation information of the file and the date modified. Maya file readers ignore this block as it is just used for information purpose only. A header must start with first six characters as "//Maya" though.

ASCII file header looks like as follow.

```
//Maya ASCII 1.0 scene
//Name: solstice.ma
//Last modified: Sun, Dec 21, 97 10:18:26 AM
```
### File References

The file references section of a .ma file contains information about all other Maya files that are being referenced in this file. Each referenced file can be read using a single file command that is contained in the same file. The syntax of the file command when used for referencing is:

```
file -r -rpr prefixString fileName;
```
or

```
file -r -ns nameSpace fileName
```
Here is an example string.

```
file -r -rpr "solar" "/u/sally/work/solar.ma";
```
This example shows that the sun object contained in the file `solar` would be accessible in this file using the name "solar_sun".

### Requirements

Requirements section of a .ma file consists of a series of required commands and tells May information such as version and plugin information that is required to read the files. An example of requirements section is as follow.

```
requires maya "2.0";
requires specialPlugIn "1.2";
```


The next section specifies the requirements. This consists of a series of requires commands. This section of the file tells Maya what software is needed to load the file properly. Specifically, what version of Maya, and what plug-ins.

## MA file download
It is bit hard to find and download the MA file of a 3d model. Therefore, you can download a sample MA file from here:

- [Sample.ma](../sample.ma)


## References

* [Organization of Maya ASCII Files - Autodesk](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001)
