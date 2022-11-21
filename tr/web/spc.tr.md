---
date: 2021-07-05
keywords: spc, .spc, spc dosya formatı, spc dosyaları nasıl açılır, Yazılım Yayıncısı Sertifika Dosyası
yazar:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SPC - Yazılım Yayıncısı Sertifika Dosyası
linktitle: SPC
description: "SPC dosya biçiminin ne olduğu ve SPC dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin."
menu:
  docs:
    parent: "web"
lastmod: 2021-09-30
---

## SPC dosyası nedir?

.spc uzantılı bir dosya, PKCS # 7 formatında oluşturulmuş bir dijital güvenlik sertifikası dosyasıdır. Çeşitli uygulamalar, güvenli bilgi alışverişi için bu sertifika dosyalarını oluşturun. OpenSSL ve Microsoft'un .NET Framework'üne dahil olan Signcode.exe uygulaması bu türden çok az uygulama içerir. [.cer](/tr/web/cer/), [.p7c](/tr/web/p7c/) ve [.ssp](/tr/web/ssp/) gibi diğer sertifika dosyaları gibi, SPC dosyaları da ortak anahtarı içerir özel bir anahtarla şifrelenen bilgiler. Bu ortak anahtar, gizli anahtar gizli tutulurken, kullanıcılarla genel olarak paylaşılabilir.

## SPC Dosya Biçimi - Daha Fazla Bilgi

SPC dosyaları, herhangi bir metin düzenleyicide açılabilen ancak insan tarafından okunamayan ikili dosyalar olarak diske kaydedilir. Bunlar, mevcut [RFC 2315](https://datatracker.ietf.org/doc/html/rfc2315) olan en son PKCS # 7 sürümünü temel alır.

## Referanslar

* [PKCS 7](https://en.wikipedia.org/wiki/PKCS_7)
* [SSP Referansı](https://scalate.github.io/scalate/documentation/ssp-reference.html)

