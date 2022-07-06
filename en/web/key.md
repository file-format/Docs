{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description":"Learn about KEY file format and APIs that can create and open KEY files.",
  "title" : "KEY File Format - Privacy-Enhanced Mail Private Key File",
  "linktitle" : "KEY",
  "menu" : {
    "docs" : {
      "identifier":"web-key",
      "parent" : "web"
    }
  },
  "lastmod" : "2022-07-04"
}

## What is a KEY file?

A KEY file is the private part of a security mechanism that is saved to disc in Privacy-Enhanced Mal (PEM) file format. It is used to decrypt information exchanged between a web browser and the web server that serves the browsing requests. A KEY file contains encoded strings that are useless for human eye but are the essence of encrypting/decrypting information exchange as part of SSL certificate on web servers. KEY files are automatically generated and are installed at client end.

You can open **KEY** files with any text editor such as Microsoft Notepad (Windows), Apple TextEdit (Mac), or GitHub Atom (cross-platform). KEY files are similar to [CRT](/web/crt/) and [CER](/web/cer/) file formats.

## KEY File Format - More Information

KEY files are stored to disc as plain text files but are encoded strings that are not human friendly to read. Practically, users  have zero understanding of the strings when opened in a text editor. The private key certificate is confidential and should not be shared with anyone. The complete process of securing information exchange over the internet involves a:

 * **Public Key** - used to encrypt user's information for exchange of data between the browser and the web servers
 * **Private Key** - used to decrypt the information as it is received by the web server

The SSL certificates, also known as X.509 certificates, are unique for each website. KEY files using the following syntax:

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

### KEY File Example

Following is an example of private Key file.
```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## References

* [Public Keys, Private Keys, and Certificates](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)
