{
  "date" : "2019-10-11",
  "keywords" : [ "ixbrl","ixbrl file", "ixbrl file format", "ixbrl file type", "file", "type", "what is an ixbrl file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "IXBRL - Business and Financial Reporting File Format",
  "description":"Learn about IXBRL file format and APIs that can create and open IXBRL files.",
  "linktitle" : "IXBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-ixbrl",
      "parent" : "finance"
    }
  },
  "lastmod" : "2021-02-25"
}

## What is an iXBRL file?

iXBRL (ilnine XBRL) file format lets [XBRL](/web/xbrl/) data to be embedded in an HTML file to make it both machine and human-readable. It is actually an [xHTML](/web/xhtml/) file that uses the XBRL tags and was developed by XBRL International to meet the requirements of the UK's HMRC. Using iXBRL, financial statements can be created keeping the layout of the original document intact. iXBRL files can be opened in any text editor such as Notepad on Windows Operating System and TextEdit on MacOS.

## iXBRL File Format

Inside the iXBRL, contents of XBRL are wrapped in xHTML file format that uses XML tags. Like XBRL, <xbrl> is the root element of iXBRL files. The XHTML format represents its contents as collection of different document types and modules. All the files in XHTML are based on XML file format and conform to the XML document standards. XHTML is the format of essential usage for operational utilization of dependent [HTML](/web/html/) Document Object Model (DOM) or the [XML](/web/xml/) Document Object Model. For the outside world, iXBRL follows the [xHTML](/web/xhtml/) file format specifications.

### iXBRL vs XBRL

XBRL can be compared to iXBRL based on the following factors:

 * Complexity
 * Formatting options
 * File Types/Extensions
 * Rendering Option
 * Filing Process

The following table illustrates these differences.

|Parameter|XBRL|iXBRL|
---|---|---|
|Complexity|More complex than iXBRL|Less complex due to the existing organization scheme of XHTML|
|Formatting Options|Limited Flexibility|High Flexibility for contents formatting|
|File Types/Extension|Formally saved with .xml extension|Usually saved as .html or .xhtml extension|
|Rendering Options|XBRL viewers required to view these|Human readable content that can be viewed in browsers|
|Filing Process| XBRL (machine-readable) and HTML (human readable) instance documents to be filed separately.|Both human readable as well as machine-readable formats are available in a single instance document|

## References

* [XBRL - By Wikipedia](https://en.wikipedia.org/wiki/XBRL)
* [iXBRL](https://www.xbrl.org/the-standard/what/ixbrl/)
