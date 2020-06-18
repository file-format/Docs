{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "MHTML - MIME HTML File",
  "linktitle" : "MHTML - MIME HTML File",
  "menu" : {
    "docs" : {
      "parent" : "web"
    }
  },
  "lastmod" : "2019-09-10"
}

Files with MHTML extension represent a web page archive format that can be created by a number of different applications. The format is known as archive format because it saves the web **[HTML](/web/html/)** code and associated resources in a single file. These resources include anything linked to the webpage such as images, applets, animations, audio files and so on. MHTML files can be opened in a variety of applications such as Internet Explorer and Microsoft Word. Microsoft Windows uses MHTML file format for recording scenarios of problems observed during the usage of any application on Windows that raises issues. The MHTML file format encodes the page contents similar to specifications defined in message/rfc822 which is plain text email related specifications. The actual specifications of the format are as detailed by [RFC 2557](https://tools.ietf.org/html/rfc2557).

## File Format Specifications ##

MHTML is also known as MIME Encapsulation of Aggregate HTML documents for its capability to encode HTML web pages along with its resources to a single web archive. As per the RFC 2557 specifications, an aggregate document is a MIME-encoded message that contains a root resource (object) as well as other resources linked to it via URIs. Such other resources may be representation of inline pictures, style sheets, applets, etc. In addition, these can be the root of other multimedia documents. Full document specifications for MHTML file format are as detailed in the [RFC 2557](https://tools.ietf.org/html/rfc2557) and should be referred for any kind of application development for reading/writing of this file format. The standard specifies that the body parts to be referenced can be identified either by a Content-ID or by a Content-Location.

### MIME Content Headers ###

A MIME content header, Content-Location, is defined to resolve URI references to resources in other body parts. This header can occur in any message or content heading.

### Content-Location Header ###

A Content-Location is a representation of a URI that labels the contents of a body part where it is placed. Its value can be an absolute or a relative URI. It can be used to label a resource which is not retrievable by some or all recipients of a message. A single message is allowed to have a single Content-Location header only. Example of a multipart/related structure containing body parts with both Content-Location and Content-ID labels:

```
Content-Type: multipart/related; boundary#"boundary-example";
                    type#"text/html"

      --boundary-example

      Content-Type: text/html; charset#"US-ASCII"

      ... ... <IMG SRC#"fiction1/fiction2"> ... ...
      ... ... <IMG SRC#"cid:97116092811xyz@foo.bar.net"> ... ...

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092511xyz@foo.bar.net>
      Content-Location: fiction1/fiction2

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092811xyz@foo.bar.net>
      Content-Location: fiction1/fiction3

      --boundary-example--
```

### URIs of MHTML Aggregates ###

The URI of MHTML aggregate is different than that of its root URI. The Content-Location header field should apply to the whole aggregate if it is used in the heading of a multipart/related heading. Similarly, the set of resources retrieved can be different from the set of resources retrieved using the Content-Locations of its parts when the URI referring to the MHTML aggregate is used to retrieve this aggregate. For example, retrieving an MHTML aggregate may return an old version, while retrieving the root URI and its in-line linked objects may return a newer version.

## References ##

* [MIME Encapsulation of Aggregate Documents - RFC 2557](https://tools.ietf.org/html/rfc2557)
* [MHTML File Format - By Wikipedia](https://en.wikipedia.org/wiki/MHTML)
