{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "ICS - iCalendar File Format",
  "description":"Learn about ICS file format and APIs that can create and open ICS files.",
  "linktitle" : "ICS",
  "menu" : {
    "docs" : {
      "parent" : "email"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is an ICS file?

The Internet Calendaring and Scheduling Core Object Specification (iCalendar) is an internet standard(RFC 2445) for exchanging and deploying the calendaring events and scheduling.  The iCalendar format is interoperable, thereby ensuring the exchange of calendar information among the users having different email applications. iCalendar formats the input data as a Multipurpose Internet Mail Extensions (MIME) and facilitates the object exchanged via different transport protocols. These transport protocols can be SMTP, HTTP, point-to-point asynchronous communication, and physical media based-network transport.

iCalendar allows users to share events, date/time dependent tasks, and free/busy information via emails to other users who can respond back. iCalendar files store using suffixes  ".ics" ".iCalendar" or ".ifb" with a MIME type of "text/calendar". iCalendar is kept to be self-reliant without any transport protocol dependency. Web servers (with HTTP protocol) can transport iCalendar information and web pages can contain iCalendar data in embedded form using iCalendar.

## Brief History of ICS File Format

In 1998, the Internet Engineering Task Force (IETF) defined iCalendar as a standard (RFC 2445). The standard was documented by Frank Dawson(Lotus Notes Corporation) and Derik Stenerson ( Microsoft). In 2009, the standard was again refined by Bernard Desruisseaux (Oracle) as RFC 5545. This time some new features were added and some out dated features were deprecated. In 2016, RFC 7986 was released and augmented to original iCalendar RFC. RFC 7986 added new characteristics to the main VCALENDAR object and new supportive features were also introduced for conferencing systems.

## ICS File Format ##

The MIME type used by the data of iCalendar is “text/calendar”. Default character set for iCalendar is UTF-8, however by providing parameters in MIME, a different character set can be used. An iCalendar file contains sections, among these sections "VCALENDAR", is the global section that encapsulates all other sections.  VEVENT section defines events, VTODO lists all to-do items, VJOURNAL contains journal entries, and VTIMEZONE specifies information of time zone. multiple sections of similar category are allowed.  For numerous events, multiple VEVENT sections can be present in an iCalendar file.

### Content Lines ###

The iCalendar objects are arranged into distinct lines of text” content lines”. In this file format, CRLF sequence terminates a line whereas length of line is limited to 75 octets excluding the line break. A long data item can be spanned to many lines.

### List and Field Separators ###

Properties and parameters specify list of values that are separated by a COMMA character. Quoted-strings are used for URI based parameter values. List of parameters can be constructed by the property value. Each property parameter in this list must be separated by a SEMICOLON.

In a value list, a SEMICOLON isolate property parameters and a COMMA separate property values. Example is given below:

```
ATTENDEE;RSVP#TRUE;ROLE#REQ- contestant:mailto:
name@example.com
DATE;VALUE#DATE:20170304,20180504,2015704,201270904
```

### Multiple Values

Some properties can have multiple values. Simply generating a new content line with the property name is the basic rule for multi-valued properties. However, for a single value with multiple language variations must not use multi-valued properties.

### Binary Content

Within an iCalendar object, property value can reference a binary content data placed in an external MIME entity using a URI. Inline binary content can be used in special situations with "ENCODING" parameter, where application need to express an iCalendar object as a sole entity. The following example explain an "ATTACH" property with a URI reference:

ATTACH: https://products.conholdate.app/viewer/view/KDDURXKkLk/fileformat.doc

### Character Set

Though default charset scheme for an iCalendar is UTF-8 yet no property parameter is specified to define the charset of a property value. in MIME transfers "charset" parameter MUST be used for existing charset.

## References

* [Internet Calendaring and Scheduling Core Object Specification](https://www.ietf.org/rfc/rfc5545.txt)
* [iCalendar (RFC 5545)](https://icalendar.org/RFC-Specifications/iCalendar-RFC-5545/)
* [iCalendar](https://en.wikipedia.org/wiki/ICalendar#History_and_design)
