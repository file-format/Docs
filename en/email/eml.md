{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "EML - EMail Message",
  "linktitle" : "EML - EMail Message",
  "menu" : {
    "docs" : {
      "parent" : "email"
    }
  },
  "lastmod" : "2019-09-16"
}

# What is an EML file? #

EML file format represents email messages saved using Outlook and other relevant applications. Almost all emailing clients support this file format for its compliance with RFC-822 Internet Message Format Standard. Microsoft Outlook is the default software for opening EML message types. EML files can be used for saving to disc as well as sending out to recipients using communication protocols.

## Brief History ##

EML file format specifications are available as per [RFC 822](http://www.ietf.org/rfc/rfc0822.txt) Standard Format. Prior to RFC-822, RFC-733 governed the rules of network messages exchange until in 1982, the former was created as an improvement to lateral by establishing ARPA standards. At the same time, Microsoft created its own COM modules for the development of its own email client i.e. Outlook Express. RFC-822 took the path to be established as a proprietary format when Microsoft deviated from the open standard and created [PST](https://wiki.fileformat.com/xwiki/bin/view/Main/Emailing/PST%20File%20Format/) file format where emails are saved in a highly structured database format. This resulted in problems for users of non-Microsoft email clients when emails were forwarded from Microsoft Outlook.

It was in 2001 when the 822 standard was enhanced to 2822 - Internet Message Format which is currently in use for creating, reading and sending EML messages in MIME RFC-822 format.

## EML File Format Specifications ##

EML files comprise of two distinguished sections:

* Headers - Contains information about message header
* Message Body - Contains series of information that can include message content, embedded images and attachments

### Headers Information ###

An EML file consists of Headers information and optionally message body. Each header line in the EML has two parts separated by a colon ":". First one is called Header Name and the one following the colon is header body. For example, such headers include:

* Sender email address
* Recipient email address
* Subject of Email
* Time and date stamp of message

**Example Header**

//From: <John@bmw.eml.light.com>
To: <Andy@fileformat.com>
Date: Thu, 8 Mar 2018 10:43:37 +0100
Subject: bmw eml light//

### Message Body ###

EML message body contains the primary information of email in the form of text, hyperlinks and attachments. Email body can contain plain readable text but its not necessary. In this case, the message body can be empty or contain encoded attachments data.

Contents of the message body are described by its Content-Type which enables the reading applications to read the information in respective formats. It actually represents the nature and format of a document. The structure of a MIME type or content-type is very simple; it consists of a type and a subtype, two strings, separated by a '/'. No space is allowed. The //type// represents the category and can be a //discrete// or a //multipart// type. The //subtype// is specific to each type. The list of types, that fall in the category of Content-Type, is long but some important content-types are as follow:


|**Type**|**Description**|**Example of Subtypes**
|text|Represents format which is human-readable|text/plain, text/html, text/css, text/javascript
|image|Represents image of any type excluding videos|image/bmp, image/png, image/jpg, image/gif
|audio|Represents any audio file format|audio/mdi, audio/wav
|application|Represents any kind of binary data|application/octet-stream, application/vnd.mspowerpoint, application/xhtml+xml, application/xml, application/pdf

### Representation of Attachment in EML Body ###

EML body contains boundaries for each content-type that it contains. Attachment in the message body is identified by its Content-Type and Content-Disposition as shown in the following example:

Content-Type: text/plain; charset#"windows-1252"; name#"apple app store.txt"
Content-Disposition: attachment; filename#"apple app store.txt"
Content-Transfer-Encoding: base64
X-Attachment-Id: f_jkhztmd02

As can be seen, the Content-Disposition set to attachment enables the reading applications for getting attachment information such as attachment file name and the transfer encoding. Attachment header information is followed by encoded attachment contents that are to be read.

#### Example of SpreadSheet as Attachment ####

Content-Type: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet; name#"english_spodr.xlsx"
Content-Disposition: attachment; filename#"english_spodr.xlsx"
Content-Transfer-Encoding: base64
X-Attachment-Id: f_jkhztmd43

## See Also ##

You may also be interested in:

* [MSG](/email/msg/)
* [EMLx](/email/emlx/)
* [OFT](/email/oft/)

#### References ####

* [RFC 822](http://www.ietf.org/rfc/rfc0822.txt)