---
date: 2019-12-10
keywords: xlam, .xlam, xlam-filformat, .xlam-filformat, .xlam-tillägg
författare:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Lär dig om XLAM-filformat och API:er som kan skapa och öppna XLAM-filer." 
title: XLAM filformat
linktitle: XLAM
menu:
  docs:
    parent: "spreadsheet"
lastmod: 2021-06-01
---

## Vad är en XLAM fil? ##

XLAM är en makroaktiverad tilläggsfil som används för att lägga till nya funktioner i kalkylblad. Ett tillägg är ett tilläggsprogram som kör ytterligare kod och ger ytterligare funktionalitet för kalkylblad. XLAM-filer lagras med tillägget .xlam. XLAM-filer är XML-baserade filer som liknar filformaten [XLSM](/sv/spreadsheet/xlsm/) och [XLSX](/sv/spreadsheet/xlsx/) och sparas med ZIP-komprimering för att minska den totala filstorleken.

### Exempel ###

```cmd
Public Function Add(num1 As Double, num2 As Double)
Add = num1 + num2
End Function
```

Efter detta sparar du filen med filtillägget .xlam.

## Referenser ##

- [Filformatreferens - ](https://docs.microsoft.com/en-us/deployoffice/compat/office-file-format-reference)

