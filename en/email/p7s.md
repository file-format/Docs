{
  "date" : "2022.01.31",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "P7S File - Digitally Signed Email Message",
  "description":"Learn about P7S file format and APIs that can create and open P7S files.",
  "linktitle" : "P7S",
  "menu" : {
    "docs" : {
      "parent" : "email"
    }
  },
  "lastmod" : "2022.01.31"
}

## What is a P7S file?

A P7S file is a digital signature that is received with a digitally signed email. The presence of this file as an attachment with the email verifies that the email is sent from an authentic source. This ensures that the sender has an Email Signing certificate installed on their computer. When such a signed email is sent from user's computer, the P7S file is attached with it that contains the name of the sender. Email clients supporting signed emails can see the sender's information.

## P7S File Format - More Information

S/MIME (Secure/Multipurpose Internet Mail Extensions) P7S files contain the information in plain text format that is human readable. Email clients such as Microsoft Outlook, Apple Mail, and Mozilla Thunderbird support to read the digitally signed information from an S/MIME email. Signing an email verifies the identity of the sender and tells receiver the message is authentic. When emails are downloaded from email clients (either as [EML](/email/eml/) or [MSG](/email/msg/)), these P7S files are found attached with these emails.

A P7S file contains the following information:

 * Source of origin of the email
 * Date and time when it was sent,
 * Whether it has been modified during transmission

This information is embedded using the Public-Key Cryptography Standard #7 (PKCS7) technology for digitally attaching the encrypted signatures to the email.

## References ##

* [Microsoft Sign Tool](https://learn.microsoft.com/en-us/windows-hardware/drivers/devtest/signtool)
