{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "MSG - Microsoft Outlook Email Format",
  "description":"Learn about MSG file format and APIs that can create and open MSG files.",
  "linktitle" : "MSG",
  "menu" : {
    "docs" : {
      "parent" : "email"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is a MSG file?

MSG is a file format used by [Microsoft Outlook](https://products.office.com/en-us/outlook/email-and-calendar-software-microsoft-outlook?rtc#1) and Exchange to store email messages, contact, appointment, or other tasks. Such messages may contain one or more email fields, with the sender, recipient, subject, date, and message body, or contact information, appointment particulars, and one or more task specifications. The properties that constitute the Message object, including are also a part of the MSG file.  MSG file has headers, main message body, and hyperlinks as plain ASCII text. MSG files are also suitable with the programs that need Microsoft's Messaging Applications Programming Interface (MAPI).

## MSG File Structure

CFB_3 format is the base of MSG file. The paradigm is based on the storages and streams concepts, quite close to directories and files. Therefore a major difference in the former is the entire hierarchy, packaged into a distinct file, called a compound file. Objects constitute the message files and consist of a single property or its collections. This ability facilitates applications to store intricate, structured data in a single file. This format also specifies multiple storages, each storage represents the Message object as a major component. These storages contain a number of streams representing a property of that component. Nesting of storage is also possible.

## Mapi Properties

At the top level of the .msg file, storages contain streams that store properties in them. Properties can be categorized as follows:

* Fixed length properties
* Variable length properties
* Multiple-valued properties

Irrespective of the category, a property is either a tagged or named. However, suitable mapping information is required for named properties as specified by their mapping storage.

## Storages

Storages constitute the key components of the Message object. MSG file format states the following storages:

## Top Level Structure

Message object represents the entire top level of the MSG file format. Depending upon the type, properties, number of recipient and Attachment objects, a message object can have different stream storages in its corresponding .MSG file.

### Relationship with Other Structures

The Msg file format has the following relationships to other structures:

* The base of .msg is Compound File Binary File Format.
* The properties used by Message and Attachment Object Protocol is used by this format.

## Scenarios to avoid MSG Formats

Message object can be shared between clients or message stores that use the .msg file system. There are few circumstances in which storing a Message object in the .msg file format would not be appropriate. For example:

* In case of upholding a large standalone archive, it is better to use a full-featured format in which views can be rendered more precisely.
* If the receiver is unknown, it is possible that the format is not supported by the receiver end and private or irrelevant might be delivered.

## MSG File Example

To get an idea of how a MSG file looks like, you can download a [sample MSG file](https://products.conholdate.app/viewer/view/AKMF7z0zyPcQ692Py/sample-msg-file.msg?preview=true.pdf) and open on your computer to view its contents.

## How to open MSG file?

On Windows Operating System, you can open a MSG file by double clicking the file. This will open the file in default email client Microsoft Outlook if it is installed on the system. Following is a list of programs that can open MSG files.

|Operating System|Programs that can open MSG files|
---|---|
|Windows|Microsoft Outlook 365, MFCMapi|
|Mac|Microsoft Outlook 365|

## References

* [[MS-OXMSG]: Outlook MSG File Format](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)
