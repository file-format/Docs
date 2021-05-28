{
  "date" : "2021-03-11",
  "keywords" : [ "APNX", "Amazon Page Number Index", "extension", "file", "format", "eBook", "Amazon Kindle" ],
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "description":"Learn about Amazon APNX file format and APIs that can create and open APNX files.",
  "title" : "APNX - Amazon Page Number Index",
  "linktitle" : "APNX",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
    }
  },
  "lastmod" : "2021-05-28"
}

## What is an APNX file? ##

The Amazon Page Number Index file which uses the .apnx extension is an eBook file type; used by Amazon Kindle. These files are actually known as pagination files used by Kindle devices. So the APNX files are typically created to mark the pages of Kindle eBooks. The pagination feature has been started on Amazon Kindle devices since its 3.1 firmware. It looks into the APNX file for page indexes and then maps it with the page numbers in the original print book. These files are saved into Kindle devices along with Amazon eBooks files. You can't open or edit the APNX files.

## APNX File Format Specifications ##

### Layout

|bytes|   content|             comments|
---|---|---|
|4       |00010001   |         Format identifier. Value of 65537 little-endian.|
|4       |start of next   |    The offset after ending location of the first header. Starts a new sequence of header info|
|4       |length|              Length of first header|
|N       |first header |       String containing content header. It starts next sequence|
|2       |unknown      |       Always 1|
|2       |length       |       Length of second header|
|2       |page count   |       Total number of bytes after second header that represent pages. This total includes bytes that are ignored by the pageMap.|
|2       |unknown      |       Always 32|
|N       |second header |      String containing the page mapping header|
|4*N     |padding     |        The first number given in the page mapping header indicates the number of 0 bytes.|
|4*N     |page list ||

### Content Header

The content header consists of a string enclosed in {} containing key, value pairs:

|content|             comments|
---|---|
|contentGuid|         Guid.|
|asin       |         Amazon identifier for the Kindle version of the book.|
|cdeType    |         MOBI cdeType. Should always be EBOK for ebooks.|
|fileRevisionId  |    Revision of this file.|

#### Example
```
{"contentGuid":"d8c14b0","asin":"B000JML5VM","cdeType":"EBOK","fileRevisionId":"1296874359405"}
```
### Page Mapping Header
The page mapping header consists of a string enclosed in {} containing key, value pairs.

|content     |        comments|
---|---|
|asin   |             The ISBN 10 for the paper book the pages correspond to|
|pageMap|             Three value tuple. Looks like: "(N,N,N)\
                    1) Number of bytes after header that starts the page numbering sequence\
                    2) unknown\
                    3) unknown\|
#### Example
```
{"asin":"1906694184","pageMap":"(4,a,1)"}
```

### Page List

The page list is a sequence of offsets in the raw HTML. Each
value is the start of a new page. Every entry is a 4 byte big endian
int. 



## References

* [Amazon APNX file format](https://nachtimwald.com/2011/02/09/amazon-apnx-file-format/)
* [APNX - by MobileRead Wiki](https://wiki.mobileread.com/wiki/APNX)
