{
  "date": "2021-08-21",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "Handheld Device Markup Language File",
  "description": "Learn about HDML file format and APIs that can create and open HDML files.",
  "linktitle": "HDML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-hdml"
    }
  },
  "lastmod": "2021-08-21"
}

## What is an HDML file?

A file with .hdml (Handheld Device Markup Language) extension is a markup language for creating web pages for portable electronic devices such as handheld computers, smartphones, and information display appliances. HDML is said to be an extension of the [SGML](https://en.wikipedia.org/wiki/Standard_Generalized_Markup_Language) language. HDML is similar to HTML but for wireless and handheld devices that have small displays such as PDA, mobile phones and so on. It was replaced with WML for which it acted as an important influence.

## HDML File Format - More Information

HDML is a markup language for handheld devices that is based on markup tags similar to HTML. HDML was submitted to W3C for standardization but it never became a standard. Its file format specifications are, however, available on [W3 website](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html) for reference. The [syntax for HDML language](https://www.w3.org/TR/hdml20-5.html#HEADING5-0) is available for developer's reference and can be used for sample application development.

## HDML Elements

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
