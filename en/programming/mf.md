{
  "date": "2019-10-11",
  "keywords": [
    "mf file",
    "mf",
    "extension",
    "format",
    "mf file format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "MF - Java Manifest File Format",
  "description": "Learn about MF file format and APIs that can create and open MF files.",
  "linktitle": "MF",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-mf"
    }
  },
  "lastmod": "2020-09-10"
}

## What is an MF file?

A file with .mf extension is a Java Manifest file that contains information about the individual [JAR](/programming/jar/) file entries. The MF file itself is contained inside the JAR file and provides all the extension and package-related definition. JAR files can be produced to be used as an executable file. In such case, the mainfest file specifies the main class of the application that contains **`public static void main`** statement. Manifest files are named as MANIFEST.MF and can be opened with any text editor on Windows, MacOS and Linux Operating Systems.

## Manifest File Format Specifications

[Manifest file format specifications](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) are available by Oracle in their guide for JAR file format. A Manifest file comprises of main sections that are followed by a list of sections for individual JAR file entries. Each section follows some rules and restrictions.

### Main Sections

A main section:

* contains information about security and configuration about the JAR file
* contains information about the application or extension that the JAR file is part of
* defines the main attributes for each individual manifest item

**Note**: No attribute in this section can be named "Name".

### Individual Sections

An individual section defines various attributes for packages or files of a JAR file. Each section must start with an attribute named "Name" whose value must be a relative path to the file, or an absolute URL referencing data outside the archive.

### Manifest Specifications

|Attibutes|Description|
---|---|
|manifest-file|main-section newline *individual-section|
|main-section|version-info newline *main-attribute|
|version-info|Manifest-Version : version-number|
|version-number|digit+{.digit+}*|
|main-attribute|(any legitimate main attribute) newline|
|individual-section|Name : value newline *perentry-attribute|
|perentry-attribute|(any legitimate perentry attribute) newline|
|newline|CR LF | LF | CR (not followed by LF)|
|digit|{0-9}|

## References

 * [Oracle - JAR File Format](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html)
 * [JAR File Format](https://en.wikipedia.org/wiki/JAR_(file_format))
