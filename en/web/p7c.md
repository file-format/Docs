{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "P7C - PKCS \#7 Certificate File",
  "description":"Learn about P7C file format and APIs that can create and open P7C files.",
  "linktitle" : "P7C",
  "menu" : {
    "docs" : {
      "parent" : "web"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is a P7C file?

A P7C file, like other security certificate files, is a digital certificate that is used to authenticate identity over the network. Applications using certificates authenticate identity using the public key included in these certificate files. Public-key cryptography, or asymmetric cryptography, uses pair of keys of which one is the public key and the other is known as private key. The private key is kept secure for effective security, while the public key can be shared with others. Other common certificate file formats include [crt](/web/crt/), DER, PEM, PKCS \#7,and PEM.

## P7C File Format - More Information

P7C files are saved to disc as binary files and include the public key information generated using cryptographic algorithms based on mathematical problems. These can be opened in any text editor but their content is not in human readable form. Some of the applications that can open P7C files include Apple Keychain Access, Adobe Acrobat Reader DC, Microsoft Certificate Manager, and Microsoft Windows Contacts.

### P7C File Format Example

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## References ##

* [Public Key Cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [How to Create P7C file?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)
