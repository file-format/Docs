{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "TNEF",
  "linktitle" : "TNEF",
  "menu" : {
    "docs" : {
      "parent" : "email"
    }
  },
  "lastmod" : "2019-09-10"
}

Transport Neutral Encapsulation Format (TNEF) is a Microsoft proprietary, for encapsulating email attachments based on Messaging Application Programming Interface (**MAPI**). Microsoft Outlook and Microsoft Exchange Server, entirely support TNEF while later decodes TNEF into MAPI and displays the formatted mails. An email attachment with TNEF encoding has a MIME type of MS-TNEF and stores as winmail/win.dat. The attachment in winmail .dat encapsulates the following information:


|Message|OLE objects|Outlook features
---|---|---|
|<ul><li>Original  message attachments</li><li>Original formatted version</li><li>fonts, text sizes, and text colors</li></ul>|<ul><li>embedded pictures</li><li>embedded Office documents</li></ul>|<ul><li>custom forms</li><li>voting buttons</li><li>meeting requests</li></ul>


Other email services who are not TNEF supportive, present plain text for TNEF formatted messages. Outlook embed a rich format of the message in TNEF files (OLE) or particular Outlook features (forms, polling buttons, and conference requests). Sanctioning explicit TNEF encoding within the Outlook e-mail client is not possible, however, Opting RTF format for dispatching an e-mail implicitly facilitates TNEF encoding.

## TNEF File Format ##

The TNEF data algorithm establishes a flattened structure from rich hierarchical message properties. These flattened structures then use to represent a serial data stream composed of particular properties.

In some situations, where properties occur in groups or have multiple-values, stream might include counts and paddings to enforce a specific data alignments. A distinctive situation where the use of this algorithm is advantageous is in an unsupportive messaging environment. In such environments, a rich message property is encoded into a serial data stream by a TNEF Writer. Further, the properties that do not belongs to the underlying TNEF can be encapsulated during transmission. These encapsulated properties then made available by decoding through a TNEF to ensure the availability of all properties of the original message to the client application.

In TNEF all numeric data types are little-endian and their size are greater than one byte. Handling of these numeric values on non-little-endian platforms require to accomplish the appropriate transformations to get correct values. String values are represented in Augmented Backus-Naur Form (ABNF) format according to [RFC5234] specifications. When the string terminates with null character, it is also included as well; for example, "worker@specimen.com" %x00.

{{< figure src="../TNEF.png" alt="TNEF File Format" >}}

## Attributes and Processing rules ##

The data stream in TNEF begins with a legacy version number, a signature, a primitive key value, and an attribute represent code page. This code page is generated when encoder records ANSI attributes and properties. After that, the stream became a series of attributes in which message attributes lined first and then followed by attachment attributes. Different message and attachment characteristics are contained in special attributes like attMsgProps, attAttachment, and attRecipTable. The attributes that appear in the TNEF stream, contain the structure, message properties and conversions necessary to engage them with message properties. Each attribute consist of an ID, size and data of the attribute, a checksum and a level according to its application.

## Relationship to Protocols and Other Algorithms ##

The systems that have poor mechanism to display rich message format natively need TNEF data algorithm for transport. Using the media type ms-TNEF, the output of the algorithm consists of an attachment file (winmail.dat) and a body part of MIME specified in [RFC2045]. The plain text message body is transmitted using UUENCODE according to [MSDN-UAF] specification and this message body or equivalent method decoded at the recipient end. Moreover, TNEF can transmit message data using different internet protocols like SMTP, POP3, IMAP4, and the ones, integrate MIME according to RFC2045 standard.

## Applicability Statement ##

In addition to simple message transmission, the original application of TNEF was to be created to use message classes and support additional features that have no original support in transport protocol. This application was further refined for the transmission of rich message properties and named properties that modern messaging clients use now a days. For compliance with original implementation, original attribute syntax is maintained and a special attribute holds the new message properties separately.

## References ##

* [Transport Neutral Encapsulation Format](https://en.wikipedia.org/wiki/Transport_Neutral_Encapsulation_Format)
* [Email addresses and address books in Exchange Server](https://docs.microsoft.com/en-us/exchange/email-addresses-and-address-books/email-addresses-and-address-books?view#exchserver-2019)
* [[MS-OXTNEF]: Transport Neutral Encapsulation Format (TNEF) Data Algorithm](https://msdn.microsoft.com/en-us/library/cc425498(v#exchg.80).aspx)
