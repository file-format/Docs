{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "RTF - Rich Text Format",
  "description":"Learn about RTF file format and APIs that can create and open RTF files.",
  "linktitle" : "RTF",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is a RTF file?

Introduced and documented by Microsoft, the Rich Text Format (**RTF**) represents a method of encoding formatted text and graphics for use within applications. The format facilitates cross-platform document exchange with other Microsoft Products, thus serving the purpose of interoperability. This capability makes it a standard of data transfer between word processing software and, hence, contents can be transferred from one operating system to another without losing document formatting. The file format specifications are available by Microsoft for public [download](https://www.microsoft.com/en-us/download/details.aspx?id#10725) and can be referred to from developer's perspective.

## Brief History ##

RTF file format has underwent several revisions since its publication. Its official version for read/write was published as part of Microsoft Word 3.0 for Macintosh with version 1.0 specifications. The final version of specifications, 1.9.1 was published by Microsoft in Mar 2008. No more enhancements to the specifications are made after this. At present, almost all operating systems have more feature rich applications that have minimized/eradicated the use of RTF file format.

## File Format Specifications ##

RTF serves as a standard of data transfer between word processing software and transfer of content from one operating system to another. This is achieved using control words that were introduced by Microsoft Office Word up through 2007. A standard RTF file consists of ASCII to represent rich text and with non-ASCII characters that is converted to appropriate code values. Newer versions of Word can read RTF files generated with previous versions, while the older versions ignore control words and groups they don't understand.

### Understanding the Foundations ###

RTF files use 7-bit ASCII plain text, consisting of:

* control words
* control symbols, and
* groups.

These act as the building blocks for representation of RTF data as understandable text and character encoding.

#### Control Word ####

These represent specially formatted command used to mark characters for display and can not be longer than 32 letters. A control word is defined by:

\<ASCII Letter Sequence>//<//Delimiter//>//

Each control word is case sensitive and starts with a backslash. The ASCII Letter Sequence can contain ASCII Alphabets (a through z and A through Z). The <Delimite> marks the end of the control word's name and can be one of the following:

* A space. This serves only to delimit a control word and is ignored in subsequent processing.
* A numeric digit or an ASCII minus sign ![delete](https://wiki.fileformat.com/resources/icons/silk/delete.png "delete"), which indicates that a numeric parameter is associated with the control word. The subsequent digital sequence is then delimited by any character other than an ASCII digit (commonly another control word that begins with a backslash). The parameter can be a positive or negative decimal number. The range of the values for the number is nominally –32768 through 32767, i.e., a signed 16-bit integer. A small number of control words take values in the range‌ −2,147,483,648 to 2,147,483,647 (32-bit signed integer). These control words include **\binN**, **\revdttmN//**, **\rsidN** related control words and some picture properties like **\bliptagN**. Here **N** stands for the numeric parameter. An RTF parser must allow for up to 10 digits optionally preceded by a minus sign. If the delimiter is a space, it is discarded, that is, it’s not included in subsequent processing.
* Any character other than a letter or a digit. In this case, the delimiting character terminates the control word and is not part of the control word. Such as a backslash “\”, which means a new control word or a control symbol follows.

#### Control Symbol ####

A Control Symbol represents a special occurrence that has specific meaning depending upon its contents. It consists of a backslash followed by a special character (non-alphabetical character) and don't have any delimiters.

#### Group ####

A group can consist of text, control words, or control symbols enclosed in braces (**{ }**). The opening brace (**{** ) indicates the start of the group and the closing brace ( **}**) indicates the end of the group. Each group specifies the text affected by the group and the different attributes of that text.

### RTF File Structure ###

An RTF file has the following Standard syntax:

Introduced and documented by Microsoft, the Rich Text Format (**RTF**) represents a method of encoding formatted text and graphics for use within applications. The format facilitates cross-platform document exchange with other Microsoft Products, thus serving the purpose of interoperability. This capability makes it a standard of data transfer between word processing software and, hence, contents can be transferred from one operating system to another without losing document formatting. The file format specifications are available by Microsoft for public [download](https://www.microsoft.com/en-us/download/details.aspx?id#10725) and can be referred to from developer's perspective.

## Brief History ##

RTF file format has underwent several revisions since its publication. Its official version for read/write was published as part of Microsoft Word 3.0 for Macintosh with version 1.0 specifications. The final version of specifications, 1.9.1 was published by Microsoft in Mar 2008. No more enhancements to the specifications are made after this. At present, almost all operating systems have more feature rich applications that have minimized/eradicated the use of RTF file format.

## File Format Specifications ##

RTF serves as a standard of data transfer between word processing software and transfer of content from one operating system to another. This is achieved using control words that were introduced by Microsoft Office Word up through 2007. A standard RTF file consists of ASCII to represent rich text and with non-ASCII characters that is converted to appropriate code values. Newer versions of Word can read RTF files generated with previous versions, while the older versions ignore control words and groups they don't understand.

### Understanding the Foundations ###

RTF files use 7-bit ASCII plain text, consisting of:

* control words
* control symbols, and
* groups.

These act as the building blocks for representation of RTF data as understandable text and character encoding.

#### Control Word ####

These represent specially formatted command used to mark characters for display and can not be longer than 32 letters. A control word is defined by:

\<ASCII Letter Sequence>//<//Delimiter//>//

Each control word is case sensitive and starts with a backslash. The ASCII Letter Sequence can contain ASCII Alphabets (a through z and A through Z). The <Delimite> marks the end of the control word's name and can be one of the following:

* A space. This serves only to delimit a control word and is ignored in subsequent processing.
* A numeric digit or an ASCII minus sign (-), which indicates that a numeric parameter is associated with the control word. The subsequent digital sequence is then delimited by any character other than an ASCII digit (commonly another control word that begins with a backslash). The parameter can be a positive or negative decimal number. The range of the values for the number is nominally –32768 through 32767, i.e., a signed 16-bit integer. A small number of control words take values in the range‌ −2,147,483,648 to 2,147,483,647 (32-bit signed integer). These control words include **\binN//**, **\revdttmN**, **\rsidN** related control words and some picture properties like **\bliptagN**. Here **N** stands for the numeric parameter. An RTF parser must allow for up to 10 digits optionally preceded by a minus sign. If the delimiter is a space, it is discarded, that is, it’s not included in subsequent processing.
* Any character other than a letter or a digit. In this case, the delimiting character terminates the control word and is not part of the control word. Such as a backslash “\”, which means a new control word or a control symbol follows.

#### Control Symbol ####

A Control Symbol represents a special occurrence that has specific meaning depending upon its contents. It consists of a backslash followed by a special character (non-alphabetical character) and don't have any delimiters.

#### Group ####

A group can consist of text, control words, or control symbols enclosed in braces (**{ }**). The opening brace (**{** ) indicates the start of the group and the closing brace ( **}**) indicates the end of the group. Each group specifies the text affected by the group and the different attributes of that text.

### RTF File Structure ###

An RTF file has the following Standard syntax:

|Field|Description
---|---|
|\<File>|{\<header>\<document>}

By standard, we mean that any RTF reader must be able to correctly read the RTF written to this syntax, provided that they should be able to ignore the unknown or unused control words. This also implies that the RTF readers should be robust enough to handle some variations that are generated by RTF writers without conforming to this syntax.

#### RTF Header ####

An RTF Header has the following representation.

|Field|Description
---|---|
|\<header>|**\rtf1\fbidis**? \<character set> \<from>? \<deffont> \<deflang> \<fonttbl>? \<filetbl>? \<colortbl>? \<stylesheet>? \<stylerestrictions>? \<listtables>? \<revtbl>? \<rsidtable>? \<mathprops>? \<generator>?

Header tables must appear in this order if they exist. The RTF file can include groups for fonts, styles, screen color, pictures, footnotes, comments (annotations), headers and footers, summary information, fields, bookmarks, document-, section-, paragraph- and character-formatting properties, mathematics, images, and objects. If the font, file, style, color, revision mark, and summary-information groups and document-formatting properties are included in the file, they must appear in the RTF header, which precedes the RTF body. If the content of any group is not used, the group can be omitted. Any group that uses the properties defined in another group must appear after the group that defines those properties. For example, colour and font properties must precede the style group.

#### RTF Version ####

An RTF document must start out with these six characters:

```
{\rtf1
```
where the 1 shows the RTF version number.

#### Character Set ####

After the {\rtf1, the document should declare what character set it uses. The way to declare a character set is with one of these commands:

`\ansi` - The document is in the ANSI character set, also known as Code Page 1252, the usual MSWindows character set.

`\mac` - The document is in the MacAscii character set, the usual character set under old (pre-10) versions of Mac OS.

`\pc` - The document is in DOS Code Page 437, the default character set for MS-DOS. Typists with good muscle-memory will note that this is the character set that is still used for interpreting “Alt numeric” codes—i.e., when you hold down Alt and type “130” on the numeric keypad, it produces a é, because character 130 in CP437 is an é. That is about the only use that CP437 sees these days.

`\pca` - The document is in DOS Code Page 850, also known as the MS-DOS Multilingual Code Page.

#### Font Command ####

The Character set definition is followed by the `\deffN` command. This defines that the font number N is the default font for this document. The font number N is referred from the font table. The command `\deffN` is technically optional, but it should be there to be on the safe side as a common prolog like following picks font 0 as the default font.

`{\rtf1\ansi\deff0`

#### Font Table ####

All the fonts that can be used in a document are listed in a font table where each font is represented by a font number. Document must have a font table though some programs will work without that as well.

The syntax for a font table is {\fonttbl //...declarations//...}, in which each declaration has this basic syntax:

`{\fnumber\familycommand Fontname;}`

A font table with four declarations is as follow:

```
{\fonttbl
{\f0\froman Times;}
{\f1\fswiss Arial;}
{\f2\fmodern Courier New;}
}
```

In a document with that font table, `{\f2 stuff}` would print “stuff” in Courier New. A font can't be used in a document until it is listed in the font table.

### End of Document ###

Every RTF document must end with a }, to close the group opened by the { that is the first character in the document. Nothing can follow the final }, except possibly a newline.

## References ##

* [RTF 1.9.1 Specifications](https://www.microsoft.com/en-us/download/details.aspx?id#10725)
* [Rich Text Format](https://en.wikipedia.org/wiki/Rich_Text_Format)
