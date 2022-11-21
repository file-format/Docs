---
date: 2019-10-11
keywords: prc, .prc, prc dosya formatı, prc dosyaları nasıl açılır, .prc uzantılı, prc uzantılı
yazar:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: ÇHC Dosya Biçimi
linktitle: PRC
description: "PRC dosya formatı ve PRC dosyaları oluşturabilen ve açabilen API'ler hakkında bilgi edinin."
menu:
  docs:
    parent: "3d"
lastmod: 2021-03-04
---
## PRC dosya formatları
Ürün Temsili Kompakt 3D dosya formatı ve MobiPocket tarafından bir e-kitap dosya formatı için ".prc" uzantıları kullanılmaktadır.

## Product Representation Compact (PRC) dosyası nedir?

PRC (Product Representation Compact), özellikle CAD (Computer-Aided Design) sistemlerinden gelen 3D verileri depolamak, yüklemek ve görüntülemek için optimize edilmiş bir 3D dosya formatıdır. Taşınabilir bir şekilde yazılmış sıralı bir ikili dosyadır. PRC, 3B verileri bir PDF dosyasına gömmek için kullanılabilir. PRC, montajlar ve parçalar, 3B varlıkların ağaçları, kesin geometri gösterimi, üçgenleştirilmiş gösterim ve işaretleme gibi ana CAD yapılarının çoğunu destekler. PRC, .prc uzantısını kullanır ve kullanılan internet ortam türü *model/prc*'dir.

PRC, kullanımına bağlı olarak CAD verilerini doğrudan temsil etmek için normal sıkıştırma kullanılarak veya dosya boyutunu azaltmak için yüksek sıkıştırma kullanılarak saklanabilen çok amaçlı bir dosya formatıdır. PRC formatı kullanılarak bir PDF'de depolanan 3B veriler, CAM ve CAE uygulamalarıyla birlikte çalışabilir.

### Ürün Gösterimi Kompakt (PRC) Dosya Biçimi belirtimi

Bir PRC dosyası, sonunda bir model dosyası tarafından takip edilen bir veya daha fazla dosya yapısı tarafından takip edilen bir ana başlık bölümüne sahiptir. Bir dosya yapısı, aşağıdaki veri bölümleri tarafından takip edilen bir başlığa sahiptir:

- **Globals**: Dosya yapısının her bir ağaç varlığı için başvurulan dosya yapılarını ve renkleri, çizgi stillerini ve koordinat sistemlerini içerir.
- **Ağaç**: Ürün oluşumları, parça tanımları, temsil öğeleri ve işaretleme gibi öğe ağacının açıklamasını içerir.
- **Mozaik**: Ağacın yaprak varlıklarındaki (temsil öğeleri ve işaretlemeler) mozaiklenmiş (üçgenleştirilmiş) tüm verileri içerir.
- **Geometri**: Ağacın yaprak öğelerinin (temsil öğeleri) tüm kesin geometri ve topoloji verilerini içerir.
- **Ekstra geometri**: Geometrinin özet verilerini içerir. Bu, dosyanın tüm geometriyi yüklemeden kısmen yüklenmesini sağlar.

Tipik bir PRC dosyasının yapısı aşağıdadır.

```console
PRC Header

File Structure #1
- Header for File Structure #1
- Globals for File Structure #1
- Tree for File Structure #1
- Tessellation for File Structure #1
- Geometry for File Structure #1
- Extra Geometry for File Structure #1

File Structure #2
...

File Structure #n
- Header for File Structure #n
- Globals for File Structure #n
- Tree for File Structure #n
- Tessellation for File Structure #n
- Geometry for File Structure #n
- Extra Geometry for File Structure #n

PRC model file data
```
## ÇHC uzantılı MobiPocket e-kitap dosyası nedir
**Mobipocket** adlı bir Fransız şirketi tarafından tanıtılan bir e-kitap dosya biçimi de ".prc" uzantısını kullanıyor. Başlangıçta Mobipocket, tablet bilgisayarlar, PDA'lar ve akıllı telefonlar gibi birden çok akıllı cihaz için ücretsiz bir uygulama başlattı. ".prc" uzantısı aslında .mobi ile aynıdır ancak özellikle yalnızca **.prc** veya **.pdb** uzantılarını destekleyen PDA'lar için kullanılır.

### Mobipocket PRC dosya formatı özellikleri
MobiPocket PRC dosya biçimi, XHTML kullanan Open eBook standardına dayalıdır ve ayrıca JavaScript ve çerçeveler içerebilir. Gömülü veritabanlarıyla kullanılacak yerel SQL sorguları için destek de mevcuttur.

Mobipocket Reader'ın bir ana sayfa kitaplığı vardır. Okuyucular, bir kitabın herhangi bir yerine boş sayfalar ekleyebilir ve değişken çizimler ekleyebilir. Ek Açıklamalar, yer imleri, düzeltmeler, notlar ve çizimler gibi nesneler tek bir konumdan yönetilebilir. Görüntüler GIF formatına dönüştürülür ve küçük ekranlı cep telefonları için yeterli olan maksimum 64K boyutundadır. Mobipocket Reader, elektronik yer imlerine ve yerleşik bir sözlüğe sahiptir.

Okuyucu, birçok PDA, Communicator ve Akıllı Telefon için okuma ve destek için tam ekran moduna sahiptir. Mobipocket ürünleri çoğu Palm işletim sistemini, Windows, Symbian, BlackBerry'yi destekler, ancak Android'i desteklemez. Okuyucu, WINE kullanarak Linux veya Mac OS X altında çalışır.

## Referanslar

- [ÇHC - Wikipedia](https://en.wikipedia.org/wiki/PRC_(file_format))
- [PRC Biçim Belirtimi](https://web.archive.org/web/20081202034541/http://livedocs.adobe.com/acrobat_sdk/9/Acrobat9_HTMLHelp/API_References/PRCReference/PRC_Format_Specification/index.html)
- [E-kitap biçimlerinin karşılaştırılması - Wikipedia'dan](https://en.wikipedia.org/wiki/Comparison_of_e-book_formats)

