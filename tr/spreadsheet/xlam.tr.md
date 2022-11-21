---
date: 2019-12-10
keywords: xlam, .xlam, xlam dosya biçimi, .xlam dosya biçimi, .xlam uzantısı
yazar:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "XLAM dosya formatı ve XLAM dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin."
title: XLAM Dosya Biçimi
linktitle: XLAM
menu:
  docs:
    parent: "spreadsheet"
lastmod: 2021-06-01
---

## XLAM dosyası nedir? ##

XLAM, elektronik tablolara yeni işlevler eklemek için kullanılan Makro Etkin bir Eklenti dosyasıdır. Eklenti, ek kod çalıştıran ve elektronik tablolar için ek işlevsellik sağlayan tamamlayıcı bir programdır. XLAM dosyaları .xlam uzantısıyla depolanır. XLAM dosyaları, [XLSM](/tr/spreadsheet/xlsm/) ve [XLSX](/tr/spreadsheet/xlsx/) dosya biçimlerine benzer XML tabanlı dosyalardır ve genel dosya boyutunu azaltmak için ZIP sıkıştırmasıyla kaydedilir.

### Örnek ###

```cmd
Public Function Add(num1 As Double, num2 As Double)
Add = num1 + num2
End Function
```

Bundan sonra dosyayı .xlam uzantılı kaydedin.

## Referanslar ##

- [Dosya formatı referansı -](https://docs.microsoft.com/en-us/deployoffice/compat/office-file-format-reference)

