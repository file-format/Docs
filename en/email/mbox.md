{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "MBOX - Email Mailbox File",
  "description":"Learn about MBOX file format and APIs that can create and open MBOX files.",
  "linktitle" : "MBOX",
  "menu" : {
    "docs" : {
      "parent" : "email"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is an MBOX file?

MBox file format is a generic term that represents a container for collection of electronic mail messages. The messages are stored inside the container along with their attachments. Messages from an entire folder are saved in a single database file and new messages are appended to the end of the file. Numerous applications and API provide support for MBox file format such as Apple Mail and Mozilla Thunderbird.

## MBOX File Format ##

The MBox file format remained non-standardized for quite long time until 2005 when the application/mbox  was standardized as [RFC 4155.](https://tools.ietf.org/rfc/rfc4155.txt) Messages, in RFC 2822 format, are concatenated inside MBox file format one after another. Each message begins with a separator line that identifies the message sender, and also identifies the date and time at which the message was received by the final recipient (either the last-hop system in the transfer path, or the system which serves as the recipient's mailstore). Each message is typically terminated by an empty line. The end of the database is usually recognized by either the absence of any additional data, or by the presence of an explicit end-of-file marker.

## Reading a Message from MBox File ##

A reader scans through an mbox file looking for From_ lines. Any From_ line marks the beginning of a message. The reader should not attempt to take advantage of the fact that every From_ line (past the beginning of the file) blank line. Once the reader finds a message, it extracts a (possibly corrupted)  envelope  sender  and  delivery  date out of the From_ line. It then reads until the next From_ line or  end of  file,  whichever  comes  first. It strips off the final blank line and deletes  the  quoting  of  >From_ lines and >>From_ lines and so on.  The result is an RFC 822 message.

## Encoding Considerations ##

The contents of an MBox file can become irreversibly intermingled when an email received contains an Mbox file as attachment and is saved in another Mbox file. To avoid this, messaging systems must encode an mbox database with non-transparent transfer encoding (such as BASE64 or Quoted-Printable) whenever such an object is transferred via messaging protocols.  Implementers should also be prepared to encode mbox data locally if non-compliant data is received.

## How to open MBOX file?

MBOX files can be opened using the following programs.

 |Operating System|Program that opens MBOX file|
 ---|---|
 |Windows|Mozilla Thunderbird, Microsoft Outlook 365|
 |Linux| Mozilla Thunderbird|
 |MacOS|Mozilla Thunderbird, Apple Mail, Microsoft Outlook 365|


## References ##

* [MBox - RFC4155](https://tools.ietf.org/rfc/rfc4155.txt)
* [Mbox - Wikipedia](https://en.wikipedia.org/wiki/Mbox)
