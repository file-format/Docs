{
  "date" : "2021-07-13",
  "keywords" : [ "CER", "extension", "file", "format", "web", "certificate", "language" ],
  "author" : {
    "display_name" : "Sami Cheema"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "CER - Certificate File Format",
  "description":"Learn about CER file format and APIs that can create and open CER files.",
  "linktitle" : "CER",
  "menu" : {
    "docs" : {
      "parent" : "web"
    }
  },
  "lastmod" : "2021-07-13"
}

## What is a CER file? ##

A file with an extension .cer is responsible for storing some information about the owner certificate and the specific public key. This format of files cannot store the private keys and have the capacity to store only one certificate which is x509. The specifically secured certificate authorities are those which belong to HTTPS, a trusted and secured protocol for browsing  
The CER is a certificate of your server. It is usually received by the certificate authority for the domain. CER is mostly considered the same as [CRT](/web/crt/), although both are the same format of SSL certificate but are different filename extensions. 
These can be used on operating systems by simply opening a browser and checking the security of the browser or website being used.

## Brief History ##

In 1995, Thawte became the first authority of certification for resolving the issue of public SSL (secured socket link) certs out of the US. After that, there is a series of such authorities which was founded from 1995 to 2020.

## CER File Format ##

These files can be simply
*	The PKC S#7 comprise Base64 ASCII encoding
*	Its file extensions are p7b or p7cZ
*	For binary content, the certificate would be DER or pkcs12/pfx.
There are many types of certificate files with some unique specifications:
*	.pem, When an organization usThawteificate chaining this format is well known to create certificates
*	.arm, when the method to extract a certification assists self-signed, is required, the specified format for this purpose is .arm. It is represented in base-64 ASCII encoding.
*	.der, It consists of binary data. This means it can be used for a single certificate only
*	.pfx (PKC512), It consists of a private key corresponding to a certificate issued by CA or a self-signed certificate. This format is well known for the conversion of one SSL implementation to the other.

