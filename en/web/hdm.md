{
  "date": "2022-10-12",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "HDM File - Handheld Device Markup Language File",
  "description": "Learn about HDM file format and APIs that can create and open HDM files.",
  "linktitle": "HDM",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-hdm"
    }
  },
  "lastmod": "2022-10-12"
}

## What is an HDM file?

An HDM file is a markup language webpage file that is created in the Handheld Device Markup Language (HDML). It contains markup tags similar to [HTML](/web/html/) language, but is designed for handheld electronic devices such as smartphones and PDAs. The [HDML file format specifications](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html) were submitted to W3C for standardization but couldn't become a standard. HDM is based on the [HDML](/web/hdml/) file format specifications available at W3 website.

## HDM File Format - More Information

HDM file consists of markup tags that are rendered to visually designed website on handheld devices. HDM files are copied to devices using the HDTP (Handheld Device Transport Protocol) protocol instead of the HTTP protocol which is used for HTML pages.

## HDML File Elements

Following is a lit of elements that provide run-time environment for HDML and is referred to as teh user agent.

|Element|Description|
---|---|
|Cards|This is the fundamental building block of HDML, and displays and allows the user to interact with cards of information. |
|Decks|HDML cards are grouped together into decks. An HDML deck is similar to an HTML page in that it is identified by URL [RFC1738] and is the unit of content requested from a server and cached by the user agent.|
|Actions|Actions can be of PREV, SOFT1-SOFT8, and HELP type. These are abstract and are supported in the user interface in a user agent specific manner.|
|Activities|An activity is like a group of related cards that perform one logical function. These may span one or more decks. The HDML navigation and state model is structured around activities.|
|History-based navigation|The user agent maintains a history of the cards displayed to the user. Each card that is accessed is added to the card history. The user agent allows the user to easily navigate back to the previous card in the history.|

## References

* [HDML - Wikipedia](https://en.wikipedia.org/wiki/Handheld_Device_Markup_Language)
* [HDML Specifications - W3 Schools](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html)
