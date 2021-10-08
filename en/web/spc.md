---
date: 2021-07-05
keywords: spc, .spc, spc file format, how to open spc files, Software Publisher Certificate File
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SPC - Software Publisher Certificate File
linktitle: SPC
description: Learn about what is an SPC file format and APIs that can create and open SPC files.
menu:
  docs:
    parent: "web"
lastmod: 2021-09-30
---

## What is an SPC file?

A file with .spc extension is a digital security certificate file created in the PKCS # 7 format. Several applications, create these certificate files for secure exchange of information. Few such applications include OpenSSL and the Signcode.exe application included with Microsoft's .NET Framework. Like other certificate files such as [.cer](/web/cer/), [.p7c](/web/p7c/), and [.ssp](/web/ssp/), the SPC files contain the public key information that is encrypted with a private key. This public key can be shared with users publicly while the private key is kept confidential.

## SPC File Format - More Information

The SPC files are saved to disc as binary files that can be opened in any text editor but are not human readable. These are based on latest version of PKCS # 7 which is available [RFC 2315](https://datatracker.ietf.org/doc/html/rfc2315).

## References

* [PKCS 7](https://en.wikipedia.org/wiki/PKCS_7)
* [SSP Reference](https://scalate.github.io/scalate/documentation/ssp-reference.html)
