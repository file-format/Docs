{
  "date": "2019-10-11",
  "keywords": [
    "crt",
    "crt file",
    "crt file format",
    "crt file type",
    "file",
    "type",
    "what is an crt file"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "CRT - Security Certificate File Format",
  "description": "Learn about CRT file format and APIs that can create and open CRT files.",
  "linktitle": "CRT",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-crt"
    }
  },
  "lastmod": "2019-09-10"
}

## What is a CRT file?

A file with .crt extension is a security certificate file that is used by secure websites for establishing secure connections from web server to a browser. Secure websites make it possible to secure data transfers, logins, payment card transactions, and provide protected browsing to the site. If you open a secure website, you see a "lock" icon in the address bar. If you click on it, you can view the details of the installed certificate. International companies such as Verisign and Thawte distribute these SSL certificates.

## CRT File Format

CRT files are in ASCII format and can be opened in any text editor to view the contents of the certificate file. It follows the X.509 certification standard that defines the structure of the certificate. It defines the data fields that should be included in the SSL certificate. CRT belongs to the PEM format of certificates that are Base64 ASCII encoded files.

### PEM File Structure

A PEM file can have multiple certificates. In such a case, each certificate in the PEM file follows the following structure.

```
---- BEGIN CERTIFICATE----
...
...
...
Encoded string for encryption of data
...
...
...
----END CERTIFICATE----
```

### CRT File Format Example

```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## References ##

* [Public Keys, Private Keys, and Certificates](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)
