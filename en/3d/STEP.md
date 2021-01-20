---
date: 2019-10-11
keywords: step, .step, step file format, how to open step files, .step extension, step extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: STEP File Format
linktitle: STEP
description: Learn about STEP file format and APIs that can create and open STEP files.
menu:
  docs:
    parent: "3d"
lastmod: 2020-18-01
---

## What is a STEP file?

STEP file is a widely used data exchange format for Computer-aided design (CAD). It was standardized in 1994 by the ISO committee under the name of "ISO 10303-21". ISO 10303-21 defines the encoding mechanism for representing data in EXPRESS data modeling language. A STEP- file is also known as p21-File and STEP Physical File. The file extensions used for STEP-file are .stp and .step.

## Basic History

In 1994, the original Part 21 specification was issued. It has some bugs which were corrected by the technical corrigendum issued in 1996. The second edition was published in 2002 that included the corrigendum and extensions for several data sections. The third edition was published in 2016 that added anchor and reference sections that  allowed entities and values to be stored in external files. UTF-8 support was added of strings. Digital signatures were added to verify the contents of the file and to validate credentials. The support for compressing and storing the exchange structure using ZIP was also added.

## STEP File Format

The plain text format for a STEP-file consists of a sequence of records. The character set is defined as code points of ISO 10646. "ISO-10303-21;" are the first characters in the first record. Comments are surrounded by "/*" and "*/" characters. The last record contains "END-ISO-10303-21;" if the STEP-file is conforming to the 2002 version. In case it conforms to the 2016 version, there may be one or more digital signatures after the "END-ISO-10303-21;" terminator. Line breaks are denoted by "\N\" and page breaks are denoted by "\F\".

The STEP file is divided into sections and their names are reserved terms. All sections end with the "ENDSEC" record and must be in the order shown below.

- **HEADER**: This is a mandatory and non-repeatable section. It consists of the following entities:
  - file_description (mandatory)
  - file_name (mandatory)
  - file_schema (mandatory)
  - schema_population (optional)
  - file_population (optional)
  - section_language (optional)
  - section_context (optional)
- **ANCHOR**: It is an optional non-repeating section that was introduced in the 2016 version. It defines the external names for instances so that they can be referenced.
- **REFERENCE**: It is an optional non-repeating section that was also introduced in the 2016 version. Each entry in this section associates an entry/value instance name to an instance/value in an external file.
- **DATA**: It is an optional repeatable section the contains the core content of the model instance.
- **SIGNATURE**: It is an optional repeatable section that was introduced in the 2016 version. It holds the digital signature to verify the file's content or to validate credentials.

## References

- [ISO 10303-21 - Wikipedia](https://en.wikipedia.org/wiki/ISO_10303-21)
- [STEP-file, ISO 10303-21](https://www.loc.gov/preservation/digital/formats/fdd/fdd000448.shtml)
