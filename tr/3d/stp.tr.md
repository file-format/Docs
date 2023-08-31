---
date: 2022-01-31
keywords: stp, .stp, stp dosya formatı, stp dosyaları nasıl açılır, .stp uzantısı, stp uzantısı
yazar:
  display_name: Kashif Iqbal
draft: false
toc: true
title: STP Dosya Biçimi
linktitle: STP
description: "STP dosya formatı ve STP dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin."
menu:
  docs:
    parent: "3d"
lastmod: 2022-01-31
---

## STP dosyası nedir?

Bir STP dosyası, CAD ve CAM uygulamaları arasında ürün verilerinin değiş tokuşu için kullanılan bir 3D CAD dosyasıdır. 3B nesneler hakkında bilgi içerir ve **STEP** dosya biçimine benzer şekilde kaydedilir. STP dosyaları, [STEP](/tr/3d/step/) Uygulama Protokolleri ISO 10303-2xx uyarınca uygulamalar arasında veri alışverişini kolaylaştırır. Bu ISO, EXPRESS veri modelleme dilinde veri gösterimi için kodlama mekanizmasını tanımlar. STP dosyaları **Autodesk Fusion 360** gibi uygulamalarda açılabilir.

## STP Dosya Biçimi - Daha Fazla Bilgi

STP dosyaları diske düz ASCII dosya biçiminde kaydedilir. Bunlar, bu modelleri yüklemek için CAD/CAM uygulamaları tarafından okunabilen düz metin olarak 3B model bilgilerini içerir.

STP dosyaları da .step uzantılı olarak kaydedilir ve bir dizi kayıttan oluşur. Bu dosyalarla ilgili göze çarpan özellikler şunları içerir:

* Karakter seti, ISO 10646'nın kod noktaları olarak tanımlanır.
* "ISO-10303-21;" ilk kayıttaki ilk karakterlerdir.
* Yorumlar "/*" ve "*/" karakterleri ile çevrilidir.
* Son kayıt "END-ISO-10303-21;" içerir. STEP dosyası 2002 versiyonuna uygunsa.
* 2016 versiyonuna uygun olması durumunda "END-ISO-10303-21;" den sonra bir veya birden fazla dijital imza olabilir; terminatör.
* Satır sonları "\N\" ile, sayfa sonları ise "\F\" ile gösterilir.

## STP Dosyalarını Aç

STP dosyaları, Metin Düzenleyicilerin yanı sıra STP Görüntüleyicilerde açılabilir.

### STP Dosyalarını STP Görüntüleyicilerle Açın

Çeşitli CAD uygulamaları, STP dosyalarını Windows, MacOS ve Linux'ta görüntülemek üzere açabilir. Bunlar şunları içerir:

* Autodesk Fusion 360 (çapraz platform)
* FreeCAD (çapraz platform)
* IMSI TurboCAD (Windows, Mac)
* Dassault Sistemleri CATIA (Windows, Linux)

### STP Dosyalarını Metin Düzenleyicilerle Açın

STP dosyaları düz metin dosyaları olarak kaydedilir. Bu, STP dosyalarını metin editörleriyle açmayı mümkün kılar. Windows işletim sisteminde Notepad ve Notepad++ ve MacOS'ta Apple TextEdit gibi popüler metin editörleri STP dosyalarını açabilir. Bir metin düzenleyicide açıldıktan sonra, kullanıcı STP dosyasının özelliklerini düzenleyebilir. Ancak, özelliklerin yanlış güncellenmesi durumunda dosyanın bozulmasına neden olabilir.

## STP dosyaları nasıl dönüştürülür

STP dosyalarını diğer dosya biçimlerine dönüştürebilen birkaç uygulama vardır. STP dosyalarını dönüştürebilen CAD uygulamaları şunları içerir:

* Autodesk Fusion 360
*IMSI TurboCAD
* Siemens Katı Kenar

Bunlara ek olarak, STP dosyalarını diğer dosya biçimlerine dönüştürebilen birkaç çevrimiçi uygulama vardır. Bu çevrimiçi uygulamalar, STP dosyanızı, istediğiniz biçime dönüştürüldükleri ve indirilmek üzere geri döndükleri bulut sunucularına yüklemenizi sağlar.

Autodesk Fusion 360, STP dosyalarını aşağıdaki 3B ve CAD dosya biçimlerine dönüştürebilir.

* [OBJ](/tr/3d/obj/)
* [3MF](/tr/3d/3mf/)
* [DWG](/tr/cad/dwg/)
* [DXF](/tr/cad/dxf/)
* [ASM](/tr/cad/asm/)
* [IGES](/tr/cad/iges/)
* [STL](/tr/cad/stl/)
* [FBX](/tr/3d/fbx/)
* F3D
* [USD](/tr/3d/usd/)

## Referanslar

* [ISO 10303-21 - Vikipedi](https://en.wikipedia.org/wiki/ISO_10303-21)
* [Autodesk Fusion 360](https://www.autodesk.com/products/fusion-360/overview)

