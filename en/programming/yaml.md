{
  "date" : "2019-10-11",
  "keywords" : [ "yaml", ".yaml","what is a yaml file","how to open yaml file" "extension", "file", "yaml file","yaml file format",  ".yaml extension", "yaml vs json" ],
  "author" : {
    "display_name" : "Muhammad Ahmad Chishti"
  },
  "draft" : "false",
  "toc" : true,
  "description" : " Learn about YAML file format and APIs that can create and open a YAML file.",
  "title" : "YAML File Format",
  "linktitle" : "YAML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2021-05-05"
}

## What is a YAML file? ##

**YAML file** consists of a language YAML (YAML Ain't Markup Language) which is a Unicode based data-serialization language; used for configuration files, internet messaging, object persistence, etc. YAML uses the .yaml extension for its files. Its syntax is independent of a specific programming language. Basically, the YAML is designed for human interaction and to work well with modern programming languages. Support for serializing arbitrary native data structures increased the readability of the YAML files, but it has made the parsing and file generation process complicated a little.

## Brief History ##

YAML was first proposed in 2001 and was developed by Clark Evans, Ingy döt Net, and Oren Ben-Kiki. YAML was first said to mean "Yet Another Markup Language" to indicate its purpose as a markup language. It was later repurposed as "YAML Aint Markup Language" to indicate its purpose as data-oriented.


## YAML File Format ##

YAML file consists of the following data types

- **Scalars**: Scalars are values like Strings, Integers, Booleans, etc.
- **Sequences**: Sequences are lists with each item starting with a hyphen (-). Lists can also be nested.
- **Mappings**: Mapping gives the ability to list keys with values.

### Syntax ###

- **Whitespace**: Whitespace indentation is used to indicate nesting and overall structure.

  ```yaml
  name: John Smith
  contact:
      home:   1012355532
      office:  5002586256
  address:
    street: |
              123 Tornado Alley
              Suite 16
      city:   East Centerville
      state:  KS
  ```

- **Comments**: Comments are written beginning with the "#" symbol.

  ```yaml
  # This is a YAML Comment
  ```

- **Lists**: Hyphen (-) is used to indicate list members with each member on a separate line. List members can also be enclosed in square brackets ([...]) with members separated by commas (,).

  ```yaml
  - A
  - B
  - C
  ```

  ```yaml
  [A, B, C]
  ```

- **Associative Array**: An associative array is surrounded by curly brackets ({...}). The keys and values are separated by colon(:) and each pair is separated by comma (,).

  ```yaml
  {name: John Smith, age: 20}
  ```

- **Strings**: String can be written with or without double-quotes (") or single-quotes (').

  ```yaml
  Sample String
  "Sample String"
  'Sample String'
  ```

- **Scalar Block content**: Scalar content can be written in block notation by using the following:
  - **|**: All live breaks are significant.
  - **>**: Each line break is folded to space. It removes the leading whitespace for each line.

  ```yaml
  data: |
    YAML 
      (YAML Ain't Markup Language)
    is a data-serialization language
  ```

  ```yaml
  data: ?
    YAML (YAML Ain't Markup Language)
    is a data-serialization language
  ```

- **Multiple Documents**: Multiple documents are separated by three hyphens (---) in a single stream. Hyphens indicate the start of the document. Hyphens are also used to separate directives from document content. The end of the document is indicated by three dots (...).

  ```yaml
  ---
  Document 1
  ---
  Document 2
  ...
  ```

- **Type**: To specify the type of value, double exclamation marks (!!) are used.

  ```yaml
  a: !!float 123
  b: !!str 123
  ```

- **Tag**: To assign a tag to a note, an ampersand (&) is used and to reference that node, an asterisk (*) is used.

  ```yaml
  name: John Smith
  bill-to:  &id01
    street: |
            123 Tornado Alley
            Suite 16
    city:   East Centerville
    state:  KS

  ship-to:  *id01
  ```

- **Directives**: YAML documents can be preceded by directives in a stream. Directives begin with a percent sign (%) followed by the name and then the parameters separated by spaces.

  ```yaml
  %YAML 1.2
  ---
  Document content
  ```
## YAML vs JSON
Basically, both JSON and YAML are developed to provide a human-readable data interchange format. The YAML is realized as a superset of JSON format. It means that we can parse JSON using a YAML parser. Although the practical implementation of this theory is little tricky. Therefore, some basic differences between YAML and JSON are given below:

|YAML| JSON|
---|---|
|Complex and time consuming process of parsing Serialized data |Quickly and easily parse JSON serialized data with its simpler design|
|Less community support| Larger community support and popularity|
|Supports comments| Doesn't support comments|
|Ability to use reference of other data objects| Impossible to serialize complex structures with object references|
|Hierarchy is denoted by using double space characters. Tab characters are not allowed|Objects and Arrays are denoted in braces and brackets.|
|String quotes are optional but it supports single and double quotes.|Strings must be in double quotes.|
|Root node can be any of the valid data types|Root node must either be an array or an object.|

## How to open YAML file ##

If you are not being able to open the YAML file on your computer; there may be many causes. The most important cause is that YAML supported softwares are not installed on your device. In this case you need to see the following points as a guideline:

- Install the well suited software to run the file.
- If still you are facing difficulty to open the .yaml file; you must check the version of the software and see either that is supporting .yaml files or not. Some files can be supported by the old version and some by the latest one so, must check the details.
- After installing the appropriate verion of software make sure that it is set as the default application to open YAML files.

### Softwares that can open the YAML files ###
The YAML files can be opened in the following softwares:

|Software| Operating System|
---|---|
|File Viewer Plus|Microsoft Windows|
|Microsoft Notepad|Microsoft Windows|
|Notepad++|Microsoft Windows|
|Microsoft Visual Studio Code|Microsoft Windows, MacOS, Linux|
|GitHub Atom|Microsoft Windows, MacOS, Linux|
|gVim|Microsoft Windows, Linux|
|Apple TextEdit| MacOS|
|MacroMates TextMate| MacOS|
|Alexander Blach Textastic Code Editor|iOS|
|File Viewer for Android|Android|




## References ##

- [YAML - Wikipedia](https://en.wikipedia.org/wiki/YAML)
- [YAML](https://yaml.org/spec/1.2/spec.html)
