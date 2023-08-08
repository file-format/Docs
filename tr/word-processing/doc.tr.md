{
  "date" : "2019-12-03",
  "keywords" :[ "belge", "dosya", "uzantı", "dosya formatı", "Word", "Belge"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DOC - Microsoft Word Belge Dosyası",
  "description":"DOC dosya formatı ve DOC dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "DOC",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-12-03"
}

## DOC dosyası nedir?

.doc uzantılı dosyalar, Microsoft Word tarafından oluşturulan belgeleri veya ikili dosya biçimindeki diğer kelime işlem belgelerini temsil eder. Uzantı başlangıçta birkaç farklı işletim sisteminde düz metin belgeleri için kullanıldı. Düz metin, grafikler, çizelgeler, katıştırılmış nesneler, bağlantılar, sayfalar, sayfa biçimlendirme, yazdırma ayarları ve daha pek çok şeyin yanı sıra biçimlendirilmiş görüntüler gibi birkaç farklı türde veri içerebilir. Bu biçim, kullanıcılara kılavuzlar, teklifler, şartnameler, özgeçmişler, makaleler veya benzeri belgeler yazmak için sunduğu çeşitli seçenekler nedeniyle her türlü belgeleme için popülerdi. DOC'nin güncellenmiş sürümü, özellikleri açık bir şekilde kullanılabilen Office OpenXML tabanlı [DOCX](/tr/word-processing/docx/) sürümüdür.

## Kısa Tarih ##

Bir [Corel](https://www.corel.com/en/) ürünü olan WordPerfect, DOC'u tescilli biçimlerinin uzantısı olarak kullandı. 1980'lerde WordPerfect, kolay bulunabilmesi, çoğu bilgisayar makinesine ve İşletim sistemlerine uygunluğu nedeniyle çoğu bilgisayarda kullanım tercihi olmaya devam etti. Bununla birlikte, WordPerfect, Microsoft, Microsoft Word'ü belge dosya formatı ürünü olarak tanıttığında ve tescilli formatı için DOC uzantısını seçtiğinde Windows işletim sistemindeki düşüşünü gördü. Microsoft Word giderek daha popüler hale geldikçe, DOC dosya formatı Microsoft Word 97 - 2003'ten birkaç revizyondan geçti. Varsayılan DOC dosya formatının Office Açık XML formatı (DOCX olarak bilinir) ve yeni sürümleri ile değiştirildiği yıl 2007 idi. Microsoft Word artık bu yeni uzantıyı varsayılan dosya biçimi olarak kullanıyor.

## DOC Dosya Biçimi Özellikleri - Daha Fazla Bilgi

Microsoft, DOC dosya biçimi belirtimlerini 2008 yılına kadar uzun bir süre yayınlamadı. Şubat 2008'de, Microsoft Açık Belirtim Sözü kapsamında .doc dosya biçimi için biçim belirtimleri yayımlandı. Spesifikasyon, DOC formatı tarafından kullanılan tüm özellikleri açıklamasa da, bu dosya formatıyla çalışmak için gereken bilgiler hakkında geniş bilgi verir. Yine de, mevcut bilgilerden yararlanmak için tersine mühendislik gereklidir. Spesifikasyonlar birkaç kez güncellendi ve en son [revizyon](https://msdn.microsoft.com/en-us/library/cc313153(v#office.12).aspx) Ağustos 2018 itibariyle güncellenen 8.0'dır. .

### Bazı Temel Kavramlar ###

DOC için dosya biçimi belirtimleri hakkında herhangi bir ayrıntıya girmeden önce, bu dosya biçimiyle çalışmak için bazı temel kavramları anlamak gerekir.

**Dosya Bilgi Tabanı (Fib):** Fib yapısı, belge hakkında bilgi içerir ve belgeyi oluşturan çeşitli bölümlere yönelik dosya işaretçilerini belirtir.
Fib değişken uzunluklu bir yapıdır. Boyut olarak sabitlenen temel kısım dışında, her bölümün önünde bir sonraki bölümün boyutunu belirten bir sayım alanı bulunur.

**Karakter Konumu:** CP veya Karakter Konumu, belge metninde bir karakterin sıfır tabanlı dizini işlevi gören, işaretsiz 32 bitlik bir tam sayıyı temsil eder. Dosyadaki her karakterin konumu ve boyutu doğrudan alınamaz ve önceden belirlenmiş algoritma kullanılarak hesaplanması gerekir. Karakterler şunları içerir:

* Belgenin metni
* Dipnotlar veya metin kutuları gibi nesnelerin çapaları
* Paragraf işaretleri ve tablo hücre işaretleri gibi kontrol karakterleri

**PLC:** PLC yapısı, bir veri öğeleri dizisi tarafından takip edilen bir CP dizisidir. Herhangi bir PLC için veri elemanları aynı boyutta sıfır veya daha fazla bayt olmalıdır ve bu nedenle CP sayısı, veri elemanı sayısından bir fazla olmalıdır. PLC yapıları, her türün o tür için yinelenen CP'lere izin verilip verilmediğini belirttiği farklı türlerdedir. Bir PLC yapısı şunlardan oluşur:

* **aCP (değişken uzunluk):** Bir dizi CP öğesi. **PLC** yapısının her türü, CP öğelerinin anlamını ve izin verilen aralığı belirtir.
* **aData (değişken uzunluk):** Her bir **PLC** yapısı türü, veri öğelerinin yapısını ve anlamını, veri öğelerinin sayısı üzerindeki tüm kısıtlamaları ve bunların içerdiği veriler üzerindeki tüm kısıtlamaları belirtir. Ayrıca, veri öğeleri ve karşılık gelen CP'ler arasındaki ilişkiyi de belirtir.

**Geçerli Seçim:** .DOC dosya yapıları temel olarak bir dizi CP ile tanımlanır. Böyle bir durumda uyulması için Microsoft tarafından belirtilen bir dizi [kural](https://msdn.microsoft.com/en-us/library/dd908861(v#office.12).aspx) vardır.

**STTB:** STTB, bir dizi öğe tarafından takip edilen bir başlıktan oluşan bir dize tablosudur. **cData** değeri, dizide bulunan öğelerin sayısını belirtir.

**Özellik Depolama:** Bir kelime dosyası, her birinin kendi özelliklerine sahip olabileceği metin, paragraflar, tablolar, resimler ve bölümler gibi farklı öğelere sahip olabilir. Bunların özellikleri, varsayılandan farklı olarak Word dosyasında saklanır. Bu tür farklılıklar, Tek Özellik Değiştirici (Sprm) ve işleneninden oluşan PRl tarafından belirtilir. Bir uygulama, **Prl**s listelerini uygulayarak nihai özellik kümesini belirleyebilir.

**Parola Koruması:** Word dosyaları da parola korumalı olabilir ve bunun için aşağıdaki mekanizmalardan biri kullanılabilir.

* XOR Şaşırtması
* Office ikili belge RC4 şifrelemesi
* Office ikili belge RC4 CryptoAPI şifrelemesi

FibBase.fEncrypted ve FibBase.fObfuscation'ın her ikisi de 1 ise, dosya XOR gizleme kullanılarak karartılır.

FibBase.fEncrypted 1 ve FibBase.fObfuscation 0 ise, dosya Office Binary Document RC4 Encryption veya Office Binary Document RC4 CryptoAPI Encryption kullanılarak şifrelenir ve EncryptionHeader Tablo akışının ilk FibBase.lKey baytında depolanır. EncryptionHeader.EncryptionVersionInfo, dosyayı şifrelemek için hangi şifreleme mekanizmasının kullanıldığını belirtir.

### Dosya Yapısı ###

Orijinalliğindeki bir ikili Word dosyası, birkaç depolama ve akıştan oluşan bir OLE bileşik dosyasıdır. Bu depolar ve akışlar, yazma ve okuma için parametreleri belirleyen kendi yapılarına ve boyutlarına sahiptir. Bunlar:

#### WordDocument Akışı ####

Bu akış, dosyanın diğer bölümlerinden referans verilen belge metnini ve diğer bilgileri içerir. Akış, başlangıçta zorunlu olan ve ofset 0'da olması gereken FIB dışında önceden tanımlanmış bir yapıya sahip değildir. Bu akış, 2147 MB'den büyük olmamalıdır.

#### 1TableStream veya 0TableStream ####

Bir ikili Word dosyası, 1Table akışı veya 0Table akışı olarak bilinen Tablo Akışları içerebilir. Bunlardan en az biri belgede bulunmalıdır. Ancak, bir belge hem 1Table hem de 0Table akışlarını içeriyorsa, yalnızca base.fWhichTblStm tarafından başvurulan akış kullanılır. Başvurulmayan akış dikkate alınmamalıdır ZORUNLU.
Tablo Akışı 2147 MB'den BÜYÜK OLMAMALIDIR.

#### Veri akışı ####

Veri akışının önceden tanımlanmış bir yapısı yoktur. FIB'den veya dosyanın diğer bölümlerinden başvurulan verileri içerir. Bu akışa herhangi bir referans yoksa mevcut olması gerekmez. Veri akışı 2147 MB'den BÜYÜK OLMAMALIDIR.

#### Nesne Havuzu Depolama ####

Nesne Havuzu deposu, katıştırılmış OLE nesneleri için depolar içerir. Belgede katıştırılmış OLE nesneleri yoksa, bu depolamanın mevcut olması gerekmez.

#### Özel XML Veri Depolama ####

Özel XML Veri deposu, adı "MsoDataStore" OLMALIDIR, isteğe bağlı bir depolamadır.

#### Özet Bilgi Akışı ####

Özet Bilgi akışı, adı "\005ÖzetBilgi" OLMALIDIR, burada \005 0x0005 değerine sahip karakterdir ve "\005" dizesi değil, isteğe bağlı bir akıştır.

#### Belge Özeti Bilgi Akışı ####

Belge Özeti Bilgi akışı, adı "\005DocumentSummaryInformation" OLMALIDIR, isteğe bağlı bir akıştır; burada \005, "\005" dizesi değil, 0x0005 değerine sahip karakterdir.

#### Şifreleme Akışı ####

Şifreleme akışı, adı "şifreleme" OLMALI OLMALI isteğe bağlı bir akıştır. Aşağıdaki koşulların her ikisi de karşılanmadıkça bu akış mevcut OLMAMALIDIR:

* Belge, Office Binary Document RC4 CryptoAPI Encryption ile şifrelenmiştir.
* fDocProps değeri EncryptionHeader.Flags dosyasında ayarlanır.

#### Makro Depolama ####

Makro deposu, dosya için makroları içeren isteğe bağlı bir depolama alanıdır. Varsa, bir Proje Kök Deposu OLMALIDIR.

#### XML İmza Depolama ####

XML imza deposu, adı "_xmlsignatures" OLMALIDIR, isteğe bağlı bir depodur.

#### İmza Akışı ####

İmza akışı, adı "_signatures" OLMALIDIR, isteğe bağlı bir akıştır. Bu akış dijital imzalar içerir.

#### Bilgi Hakları Yönetimi Veri Alanı Depolama ####

Bilgi Hakları Yönetimi Veri Alanı depolaması, adı "\006DataSpaces" OLMALIDIR, burada \006, "\006" dize değeri değil, 0x0006 değerine sahip karakterdir. Bu depolama mevcutsa, Korumalı İçerik Akışı da mevcut OLMALIDIR.
Bu depolama mevcutsa, bu depolama ve Korumalı İçerik Akışı dışındaki tüm belirtilen akışlar ve depolamalar, [MS-OFFCRYPTO]'da belirtildiği gibi ve bu akışlardan ve depolamalardan herhangi biri Korumalı İçeriğin dışında mevcutsa, Korumalı İçerik Akışından okunmalıdır *ÖNERİ* Akış, göz ardı edilmeleri GEREKİR.

#### Korumalı İçerik Akışı ####

Korumalı İçerik Akışı, adı "\009DRMContent" OLMALIDIR, burada \009, "\009" dize değeri değil, 0x0009 değerine sahip karakterdir.
Bu akış mevcutsa, Bilgi Hakları Yönetimi Veri Alanı Deposu da mevcut OLMALIDIR.

## Referanslar ##

* [MS-DOC Dosya Oluşturma Spesifikasyonları](https://msdn.microsoft.com/en-us/library/cc313153(v#office.12).aspx)
* [Doc Bilgi İşlem](https://en.wikipedia.org/wiki/Doc_(computing))

