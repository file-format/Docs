{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OST - Outlook Depolama Dosyası Biçimi",
  "description":"OST dosya formatı ve OST dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "OST",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## OST dosyası nedir?

OST veya Çevrimdışı Depolama Dosyaları, Microsoft Outlook kullanılarak Exchange Server'a kaydolduktan sonra yerel makinede çevrimdışı modda kullanıcının posta kutusu verilerini temsil eder. Sunucuyla bağlantı üzerine Microsoft Outlook'un ilk kullanımında otomatik olarak oluşturulur. Dosya oluşturulduktan sonra, veriler e-posta sunucusuyla senkronize edilir, böylece e-posta sunucusu bağlantısının kesilmesi durumunda çevrimdışı olarak da kullanılabilir. OST dosyaları, e-postalar, kişiler, takvim bilgileri, notlar, görevler ve diğer benzer veriler gibi posta kutusu öğelerini kullanabilir. Kullanıcılar, sunucuyla bağlantı olmasa bile OST dosyasında e-postalar ve diğer veri öğeleri oluşturabilir, ancak bunlar sunucuyla senkronize edilmez. Bağlantı kurulduktan sonra, hem sunucunun hem de yerel kopyanın aynı bilgi düzeyinde olması için yerel dosya sunucuyla yeniden eşitlenir.

## OST Dosya Biçimi

OST (Çevrimdışı Depolama Tablosu) ve [PST](/tr/email/pst/) (Kişisel Depolama Tablosu) dosya biçimi, kullanıcının e-postalarını, kişilerini ve randevularını depolamaya karşılık gelen Kişisel Klasör Dosyası (PFF) biçiminden oluşur. Bir PFF dosyasındaki veriler, UTC'de FILETIME olarak gösterilen tüm tarihler ve saatler ile little-endian'da depolanır. [MS-PST] iki tip PFF tanımlar:

* 32-bit ANSI Biçimi
* 64-bit Unicode Biçimi

PST Dosya formatı [özellikler](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546), Microsoft'tan temin edildiği şekliyle, ücretsiz olarak OST dosya formatı için de geçerlidir ve Açık Spesifikasyon Sözü aracılığıyla geri alınamaz patent lisanslaması. Aşağıdaki ayırt edilebilir unsurlardan oluşur:

* Dosya başlığı
* Dosya başlığı verileri
* Dizin dal düğümü
* Dizin yaprak düğümü
* (Dosya) ofset dizini
* (Öğe) tanımlayıcı dizini
* Yerel tanımlayıcılar
* Öğe tablosu türü

### Başlık Bilgileri

OST dosyasının HEADER yapısı, dosyanın en başında 0 ofsetinde bulunur. Yukarıda açıklanan NDB Katmanı veri yapılarına erişmek için OST dosyası ve ROOT bilgileri hakkında meta veri bilgileri içerir. HEADER yapısı, OST Dosya Biçiminin Unicode ve ANSI sürümleri için farklılık gösterir.

Başlık, baytlarla (0x21, 0x42, 0x44, 0x4E) temsil edilen 4 baytlık sihirli sözcük **!BDN** ile başlar. Başka bir 2 baytlık sihirli sayı, **SM** (0x53, 0x4D), dosyanın başlangıcından itibaren 8. ofsette bulunur. Sürüm bilgisi (ANSI veya Unicode), dosyanın başlangıcından itibaren 10'luk bir uzaklıkta yer alır. Onaltılık değer (0x17), Unicode OST dosyasını belirtirken 0x0E veya 0x0F, ANSI dosya formatını temsil eder.

|Alan|Açıklama
---|---|
|dwMagic (4 bayt)|"{ 0x21, 0x42, 0x44, 0x4E } ("!BDN")" OLMALIDIR
|dwCRRCPartial (4 bayt)|wMagicClient'ten (0ffset 0x0008) başlayan 471 baytlık verinin 32 bitlik CRC değeri
|wMagicClient (2 bayt)|"{ 0x53, 0x4D }" OLMALIDIR.
|wVer (2 bayt)|Dosya biçimi sürümü. Dosya bir ANSI PST dosyasıysa bu değer 14 veya 15 OLMALIDIR ve dosya bir Unicode PST dosyasıysa 23 OLMALIDIR.
|wVerClient (2 bayt)|İstemci dosya biçimi sürümü. Bu belgede açıklanan biçime karşılık gelen sürüm 19'dur. Bu belgeyi temel alan yeni bir PST dosyası oluşturanların bu değeri 19 olarak başlatması GEREKİR.
|bPlatformCreate (1 byte)|Bu değer 0x01 olarak ayarlanmalıdır.
|bPlatformAccess (1 bayt)|Bu değer 0x01 olarak ayarlanmalıdır.
|dwAyrılmış (8 bayt)|
|bidUnused (yalnızca 8 bayt Unicode)|Unicode PST dosya formatı oluşturulduğunda kullanılmayan dolgu eklendi.
|bidNextP (Unicode: 8 bayt; ANSI: 4 bayt)|Sonraki sayfa BID. Sayfaların bidIndex değerlerini tahsis etmek için özel bir sayacı vardır. Sayfalar için BID'ler için bidIndex değeri bu sayaçtan tahsis edilir.
|bidNextB (yalnızca 4 bayt ANSI): |Sonraki BID. Bu değer, bir sonraki tahsis edilen bloğa atanacak BID'yi gösteren monoton sayaçtır. BID değerleri 4'lük artışlarla ilerler. Daha fazla ayrıntı için bkz. bölüm 2.2.2.2.
|dwBenzersiz (4 bayt)|Bu, PST dosyasının HEADER yapısı her değiştirildiğinde değişen, tekdüze artan bir değerdir. Bu değerin işlevi, benzersiz bir değer sağlamak ve her başlık değişikliğinden sonra HEADER CRC'lerinin farklı olmasını sağlamaktır.
|rgnid[](128 bayt)|Her biri 32 olası NID_TYPE'den birine karşılık gelen 32 NID'lik sabit bir dizi (NID_TYPE, NID_TYPE_NORMAL_FOLDER, NID_TYPE_SEARCH_FOLDER, NID_TYPE_NORMAL_MESSAGE,NID_TYPE_ASSOC_MESSAGE)
|qwKullanılmamış (8 bayt)|Kullanılmayan alan; Sıfır olarak ayarlanmalıdır. Yalnızca Unicode PST dosya biçimi.
|root (Unicode: 72 bayt; ANSI: 40 bayt)|Bir ROOT yapısı (bölüm 2.2.2.5).
|dwAlign (4 bayt)|Kullanılmayan hizalama baytları; Sıfır olarak ayarlanmalıdır. Yalnızca Unicode PST dosya biçimi.
|rgbFM (128 bayt)|Kullanımdan kaldırıldı FMmap. Bu artık kullanılmamaktadır ve 0xFF ile doldurulması GEREKİR. Okuyucular bu baytların değerini dikkate almamalıdırlar *ÖNERİ*.
|rgbFP (128 bayt)|Kullanımdan kaldırıldı FPMmap. Bu artık kullanılmamaktadır ve 0xFF ile doldurulması GEREKİR. Okuyucular bu baytların değerini dikkate almamalıdırlar *ÖNERİ*.
|bSentinel (1 bayt)|0x80 olarak ayarlanmalıdır ZORUNLU.
|bCryptMethod (1 bayt)|PST dosyasındaki verilerin nasıl kodlandığını gösterir. Önceden tanımlanmış değerlerden birine ayarlanmalıdır (NDB_CRYPT_NONE, NDB_CRYPT_PERMUTE, NDB_CRYPT_CYCLIC).
|rgbAyrılmış (2 bayt)| Rezerve; Sıfır olarak ayarlanmalıdır.
|bidNextB (8 bayt)|Bir sonraki kullanılabilir BID değerini gösterir. Yalnızca Unicode PST dosya biçimi.
|bidNextB (YALNIZCA Unicode: 8 bayt)|Sonraki TEKLİF. Bu değer, bir sonraki tahsis edilen bloğa atanacak BID'yi gösteren monoton sayaçtır. BID değerleri 4'lük artışlarla ilerler. Daha fazla ayrıntı için bkz. bölüm 2.2.2.2.
|dwCRCFull (4 bayt)|wMagicClient'ten bidNextB'ye (dahil) başlayan 516 baytlık verinin 32 bitlik CRC değeri. Yalnızca Unicode PST dosya biçimi.
|ullAyrılmış (8 bayt)|Ayrılmış; Sıfır olarak ayarlanmalıdır. Yalnızca ANSI PST dosya biçimi.
|dwAyrılmış (4 bayt)|Ayrılmış; Sıfır olarak ayarlanmalıdır. Yalnızca ANSI PST dosya biçimi.
|rgbReserved2 (3 bayt)|
|bAyrılmış (1 bayt) |
|rgbReserved3 (32 bayt) |

## Referanslar

* [Outlook Kişisel Klasörleri (.ost) Dosya Biçimi](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546)
* [Kişisel Klasör Dosya Biçimi Özellikleri](https://github.com/libyal/libpff/blob/main/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)

