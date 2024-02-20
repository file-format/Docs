{
  "date": "2022-09-14",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "PEM File - Privacy Enhanced Mail Certificate File Format",
  "description": "Learn about PEM file format and APIs that can create and open PEM files.",
  "linktitle": "PEM",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-pem"
    }
  },
  "lastmod": "2022-09-14"
}

## What is a PEM file?

A PEM file is a security certificate file that is used to establish a secure communication channel between a web server and a browser. It is Base64-encoded and may contain a private key, server certificate, and/or a combination of other certificates. PEM files are similar to .der certificate files in terms of usage but is stored as Base64-encoded text rather than binary data. Other similar certificate file formats include [.cer](/web/cer/) and [.crt](/web/crt/) files.

Applications that can **open PEM files** include text editors such as Microsoft Notepad and Apple TextEdit.

## PEM File Format

PEM is a container file format that defines the structure and encoding type of the file used to store the data. PEM files are stored to disc as Base64-encoded file format that is not human-readable. The standard defines that a PEM file starts with:

```
-----BEGIN <type>-----
```
and ends with:
```
-----END <type>-----
```

All other content inside these is base64 encoded (uppercase and lowercase letters, digits, +, and /). A single PEM file can comprise of multiple blocks which can be used by other programs. If a PEM file contains multiple certificates, each certificate is separated by individual blocks as following:

```
-----BEGIN CERTIFICATE-----
  //end-user
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
  //intermediate
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
  //root
-----END CERTIFICATE-----
```

### PEM File Example

A PEM file with CERTIFICATE block usually looks like following:

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

A PEM file with RSA starts like following.

```
-----BEGIN RSA PRIVATE KEY-----
```

## References ##

* [Public Key Cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [How to Create P7C file?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)
