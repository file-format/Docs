{
  "date": "2019-10-11",
  "keywords": [
    "xhtml",
    "File",
    "Extension",
    "File Format",
    "File Extension",
    "extensible html"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "XHTML - Extensible Hypertext Markup Language File Format",
  "description": "Learn about what is XHTML file format and APIs that can create and open XHTML files.",
  "linktitle": "XHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-xhtml"
    }
  },
  "lastmod": "2019-09-10"
}

## What is an XHTML file?

The XHTML is a text based file format with markup in the XML, using a reformulation of HTML 4.0. These files are well suited to be open or viewed in a web browser. XHTML was designed to be more structured, less scripting, generic; using all the existing facilities of XML and more device independent. XHTML provides a generally worthwhile set of elements and attributes, with extension options in combination with style sheets. The attributes are used from the metadata attributes collection. XHTML provides flexibility and accessibility by subordinating all **[HTML](/web/html/)** presentation elements to style sheets. Style sheets are more versatile than these presentational elements.  Specifications for HTML 4.01, HTML5 and XHTML are being dynamically developed by the World Wide Web Consortium (W3C).

## Brief History of XHTML File Format

The history of XHTML starts with a draft document released in December 1998 by the World Wide Web Consortium. This document refers the "Reformulating HTML in XML", a specification called XHTML 1.0.This new specification reformulated HTML in XML using the existing elements or attributes. In May 1999, W3 Consortium declared that HTML 4.0 had been re-formed as an XML application. i.e. XHTML. In January 26, 2000, the first specification that defines XHTML 1.0 was released by W3C. Further in May 31, 2001, the W3C announced XHTML as an independent language and started working on development of HTML 5.0. However, in 2005, a working group (WHATWG) was formed that aimed to improve ordinary HTML independent of XHTML. The WHATWG eventually started working on HTML5 in parallel to XHTML 2.

## XHTML File Format

XHTML is a format, which is a collection of different document types and modules that mimic, categorize, and extend HTML 4. The files in XHTML are XML based, and aimed to work with the user agents based on XML. XHTML files are XML conforming. Standard XML tools are used to view, edit and validated XHTML files. HTML Document Object Model or the XML Document Object Model [DOM] dependent applications can operate through XHTML documents. Opting XHTML today, content developers can enjoy all associated benefits of XML without worrying about their content's forward or backward compatibility.

A set of related elements build a module in XHTML. A forms or table module may contain various form or table elements that can be displayed on a webpage. The modularization aimed to isolate HTML elements into sets of numerous linked elements. So that content developers can take the advantage of module selection for different types of devices. Furthermore, modules allow user agents to select elements without losing consistency with the XHTML standard. Parsing requirements of XHTML is same as XML while HTML practices its own.

### Document Conformance

XHTML2 offer specifications conforming XHTML 1.0 documents, which uses the namespaces elements and attributes from the XML and XHTML 1.0. Document Conformance is of two types.

A Strictly Conforming Document is XML based that needs only mandatory services defined in this specification. Following criteria needs to be fulfilled for XHTML files:

* A file must conform the constraints defined in DTDs and in Appendix B.
* The base element of the file must be html.
* The base element of the file must contain declaration for the XHTML namespace and should be defined as:

```
http://www.w3.org/1999/xhtml.
```

* The base element might be written as:

```
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
```

Earlier than the base element, a DOCTYPE must be declared, whose public identifier must reference one of the three document type definition (DTDs). The system identifier may be modified to comply with the current system conventions.

```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"  "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Frameset//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-frameset.dtd">
```

In XML documents, it’s unnecessary to specify XML declarations in all documents; however content developers are enticed to use XML declarations in all their XHTML documents. These declaration are mandatory either when the character encoding of the document are different from UTF-8 /16 or no encoding was specified by a governing protocol. Following example of an XHTML document defines the XML declarations

```
<!DOCTYPE html
     PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
    "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
  <head>
    <title>Public Property</title>
  </head>
  <body>
    <p>changed to <a href#"http://sample.com/">sample.com</a>.</p>
  </body>
</html>
```

A conforming user agent must need to fulfill the following rules:

* Parsing and evaluation of XHTML document is done by a user agent that ensures its consistency with the XML 1.0 Recommendation.
* In case of validating user agent, it must check the documents validity for their referenced DTDs according to XML. When XHTML file is processed by user agent as generic XML, the features of type ID will be acknowledged as fragment identifiers.

If a user agent bumps into an unrecognized element, following are the mandatory criteria it must accomplish

* process the contents of that unknown element
* ignore the attribute and its value
* Use the value of the attribute provided as default.

When user agent come across an entity reference declaration has not been processed earlier then it should be processed as the characters (starting with the “&” sign and ending with the semi-colon).  During content processing, characters or character entity references that are predictable by the user agent but not renderable may use any alternative rendering that yields the similar meaning. In such case, the document must be displayed in a manner that make the user obvious about the fact that rendering process has not been normal. For processing whitespace, user agent need to look definition from CSS characters [CSS2].

## XHTML Backward compatibility

The back ward compatibility of XHTML 1.  documents is well versed with HTML 4 user agents, if the proper rules are followed. XHTML 1.1 is fully compatible except ruby annotations, even though they are generally ignored by the HTML 4 browsers. XHTML 2.0 is comparatively less compatible, nevertheless the problem has been addressed to some extent through the usage of scripting.

## References

* [A History of XHTML: From the 1990s to Today](https://www.brighthub.com/internet/web-development/articles/109224.aspx)
