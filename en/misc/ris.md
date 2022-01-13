{
  "date" : "2022-01-12",
  "keywords" : [ "ris file", "ris file format", "what is an ris file", "file", "ris example", "ris file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "RIS - Research Information Systems Citation File",
  "description":"Learn about RIS file and APIs that can create and open RIS files.",
  "linktitle" : "RIS",
  "menu" : {
    "docs" : {
      "parent" : "misc"
    }
  },
  "lastmod" : "2022-01-12"
}

## What is an RIS file?

An RIS file is a tag file format for exchange of bibliographic data by citation programs. It contains multiple lines of citation data, consisting of a two-character code and corresponding value delimited by a hyphen. Citation information included in an RIS file includes data such as author, title, publication date, keywords, publisher, abstract, author address, etc. RIS files are human-readable and can be opened with any text editor such as Microsoft Notepad, Notepad++, and Apple TextEdit.

## RIS File Format - More Information

RIS files are stored as plain text file. Each line in an RIS file consists of a two letter code (also known as tags), followed by two spaces and a hyphen, and the corresponding value. Due to tags, RIS files are known as tagged format for representation of bibliographic citations. Example record in an RIS file is as shown below.

## RIS File Example

The following example from Wikipedia article shows the RIS file contents for an article: Claude E. Shannon. A mathematical theory of communication, Bell System Technical Journal, 27:379–423, July 1948.


|RIS Example|
---|
|TY  - JOUR|
|AU  - Shannon, Claude E.|
|PY  - 1948|
|DA  - July|
|TI  - A Mathematical Theory of Communication|
|T2  - Bell System Technical Journal|
|SP  - 379|
|EP  - 423|
|VL  - 27|
|ER  - |

In this example, `TY` is Type of Reference and `ER` is End of Reference.

### RIS Tags

Refer to [RIS Tags](https://web.archive.org/web/20110930172154/http://www.refman.com/support/risformat_tags_01.asp) section in File Format Specifications document.

## References

* [RIS Format Specifications](https://web.archive.org/web/20110930172154/http://www.refman.com/support/risformat_intro.asp)|
