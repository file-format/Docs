{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "P7B - PKCS 7 Certificate File",
  "description": "Learn about P7C file format and APIs that can create and open P7C files.",
  "linktitle": "P7B",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-p7b"
    }
  },
  "lastmod": "2019-09-10"
}

## What is a P7B file?

A P7B file is a security certificate file that contains secure digital certificate for authenticating a person or a device. Similar to a [.cer](/web/cer/) certificate file, a P7B file can be installed using the "Install Certificate" option by using the right click option on the file. P7B uses different formatting option than the CER file format. It contains one or more X.509 digital certificate files that use base64 (ASCII) encoding. P7B files are received as a [ZIP](/compression/zip/) file or received from Certificate Authority.

## P7B File Format

P7B files are stored as plain ASCII files that can be opened in any text editor. It contains the public key that is an encoded string which is meaningless from readability point of view.

### P7B File Format Example

```
---- BEGIN CERTIFICATE----

XjlakuoieulalxkjflaiuEggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYQDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## References ##

* [Public Key Cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [How to Create P7C file?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)
