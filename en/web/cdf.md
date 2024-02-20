{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "CDF - Channel Definition Format",
  "description": "Learn about what is a CDF file and APIs that can create and open CDF files.",
  "linktitle": "CDF",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-cdf"
    }
  },
  "lastmod": "2021-08-18"
}

## What is a CDF file?

A file with .cdf extension is an XLM based information distribution file format that was used to publish frequent updates as "channels". The information is published from any web server and is automatically delivered to computers with compatible receiving programs such as web browsers. Users subscribe to active channels and have scheduled updates delivered to their desktop.
CDF files were earlier used in conjunction with Microsoft's Active Channel, Active Desktop and Smart Offline Favorites technologies.

## CDF File Format

CDF files are saved as XML files that is a generic web file format for exchange of information. CDF file format is an old format now and was never widely adopted. In comparison to this, the Netscape's RSS was more famous and widely used.

### CDF File Format Example

The following is a generic exmaple of the CDF file format.

  ```
  <?xml version="1.0" encoding="UTF-8"?>
<CHANNEL HREF="http://domain/folder/pageOne.extension"
  BASE="http://domain/folder/"
  LASTMOD="1998-11-05T22:12"
  PRECACHE="YES"
  LEVEL="0">
    <TITLE>Title of Channel</TITLE>
    <ABSTRACT>Synopsis of channel's contents.</ABSTRACT>
    <SCHEDULE>
      <INTERVALTIME DAY="14"/>
    </SCHEDULE>
    <LOGO HREF="wideChannelLogo.gif" STYLE="IMAGE-WIDE"/>
    <LOGO HREF="imageChannelLogo.gif" STYLE="IMAGE"/>
    <LOGO HREF="iconChannelLogo.gif" STYLE="ICON"/>
    <ITEM HREF="pageTwo.extension"
      LASTMOD="1998-11-05T22:12"
      PRECACHE="YES"
      LEVEL="1">
        <TITLE>Page Two's Title</TITLE>
        <ABSTRACT>Synopsis of Page Two's contents.</ABSTRACT>
        <LOGO HREF="pageTwoLogo.gif" STYLE="IMAGE"/>
        <LOGO HREF="pageTwoLogo.gif" STYLE="ICON"/>
    </ITEM>
</CHANNEL>
  ```

## References

* [Channel Definition Format - By Wikipedia](https://en.wikipedia.org/wiki/Channel_Definition_Format)
