{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PST - Outlook Kişisel Bilgi Deposu Dosya Biçimi",
  "description":"PST dosya formatı ve PST dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "PST",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## PST dosyası nedir?

.pst uzantılı dosyalar, çeşitli kullanıcı bilgilerini depolayan Outlook Kişisel Depolama Dosyalarını (Kişisel Depolama Tablosu olarak da adlandırılır) temsil eder. Kullanıcı bilgileri, e-postaları, takvim öğelerini, notları, kişileri ve diğer birkaç dosya biçimini içeren farklı türlerdeki klasörlerde saklanır. PST dosyaları, daha sonra çeşitli uygulamalarda yüklenebilen ve görüntülenebilen e-posta verilerini çevrimdışı olarak arşivlemek için kullanılır.

## PST Dosya Biçimi Özellikleri

PST Dosya biçimi [özellikler](https://msdn.microsoft.com/en-us/library/ff385210(v#office.12).aspx), Microsoft'tan Açık Belirtim Sözü aracılığıyla ücretsiz ve geri alınamaz ücretsiz patent lisansı olarak edinilebilir .

### PST Biçimlerinin Türü

PST dosya biçimleri, dosya türünün kodlamasına göre iki türde kategorize edilir. ANSI kodlu PST dosyaları daha eski dosya biçimleridir ve yalnızca Outlook 2002 ve önceki sürümler tarafından desteklenir. Bu tür dosyaların maksimum boyut sınırı 2 GB'dir (2^^31^^ Bayt) ve Unicode'u desteklemez. Unicode kodlamaya dayalı daha modern bir dosya biçimi türü, dosya boyutu sınırlamasını kaldırır ve maksimum 50 GB veri boyutuna ulaşabilir.

### PST Dosya Formatının Mantıksal Organizasyonu

PST dosya biçiminin temelinde, verileri sıralı tutan ve logaritmik zamanda aramalara, sıralı erişime, eklemelere, silmelere vb. izin veren B-Tree bulunur. Bir PST dosyasının genel yapısı üç katman halinde düzenlenmiştir.

![Logical layers of a PST file](/tr/email/PST-1.png "Logical layers of a PST file")

"Düğüm Veritabanı (NDB) Katmanı" - Düğüm veritabanı katmanı, bir PST dosyasının alt düzeyinde yer alır ve düğümlerin veritabanını içerir. Bu düğümler aslında PST dosya biçiminin alt düzey depolama olanaklarını temsil eder. NDB katmanı, depolama açısından başlık, dosya ayırma bilgileri, bloklar ve BTree'lerden (Node BTree ve Block BTree) oluşur. NDB Katmanının Düğümleri ve Blokları, NID (Düğüm Kimliği), Ana NID, Veri BID (Blok BID) ve Alt Düğüm BID gibi Düğüm referansının dört özelliğinden biri olan Data BID aracılığıyla bağlanır.

`Listeler, Tablolar ve Özellikler Katmanı -` LTP katmanı, NDB üzerinde üst düzey kavramların mantıksal olarak anlaşılmasını sağlar. Diğer öğelerin yanı sıra, LTP katmanı temel olarak Özellik Bağlamı (PC) ve Tablo Bağlamı'ndan (TC) oluşur. PC bir özellikler topluluğudur, TC ise bunların varlığına karşı iki boyutlu bir özellik koleksiyonu matrisini temsil eder. PC'lerin ve TC'lerin verimli bir şekilde uygulanması olan LTP katmanı, NDB Düğümü üzerinde aşağıdaki iki tür veri yapısını kullanır:

* Düğümde Yığın (HN) - bir düğümün veri akışının küçük, değişken boyutlu parçalara alt tahsis edilmesini sağlar.
* BTree on Heap (BTH) - BTH, yukarıda açıklanan PC'ler BTH'ler olarak uygulanır ve bu nedenle bir HN yapısının içinde inşa edilerek uygulanır.

`Mesajlaşma Katmanı -` PST dosyalarıyla çalışmak için daha üst düzey kurallar ve iş mantığı bu katmanda uygulanır. Bu katmanın mantıksal çıktısı, LTP ve NDB katmanlarının birleştirilmesiyle mümkün kılınan Klasör nesneleri, Mesaj nesneleri, Ek nesneleri ve Özellikler olarak sonuçlanır. PST içeriklerini değiştirirken uyulması gereken kurallar ve gereksinimler de yine bu katmanda tanımlanır.

### PST Dosya Formatının Fiziksel Organizasyonu

PST dosyasının yüksek düzeyde dosya organizasyonu aşağıdaki şekilde gösterildiği gibidir. Bu, PST dosyasının mantıksal öğelerinden farklı kavramlara yalnızca bir genel bakıştır.

![Physical organization of the PST file format](/tr/email/PST-2.png "Physical organization of the PST file format")


#### PST Başlık Bilgileri

PST dosyasının HEADER yapısı, dosyanın en başında 0 konumunda bulunur. Yukarıda açıklanan NDB Katmanı veri yapılarına erişmek için PST dosyası ve ROOT bilgileri hakkında meta veri bilgileri içerir. HEADER yapısı, PST Dosya Biçiminin Unicode ve ANSI sürümleri için farklılık gösterir.

Başlık, baytlarla (0x21, 0x42, 0x44, 0x4E) temsil edilen 4 baytlık sihirli sözcük **!BDN** ile başlar. Başka bir 2 baytlık sihirli sayı, **SM** (0x53, 0x4D), dosyanın başlangıcından itibaren 8. ofsette bulunur. Sürüm bilgisi (ANSI veya Unicode), dosyanın başlangıcından itibaren 10'luk bir uzaklıkta yer alır. Onaltılık değer (0x17), Unicode PST dosyasını belirtirken 0x0E veya 0x0F, ANSI dosya formatını temsil eder.

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
|ullReserved (8 bayt)|Ayrılmış; Sıfır olarak ayarlanmalıdır. Yalnızca ANSI PST dosya biçimi.
|dwAyrılmış (4 bayt)|Ayrılmış; Sıfır olarak ayarlanmalıdır. Yalnızca ANSI PST dosya biçimi.
|rgbReserved2 (3 bayt)|
|bAyrılmış (1 bayt) |
|rgbReserved3 (32 bayt) |

### Veri koruması ###

Güvenlik için, PST dosyaları da parola korumalı olabilir, bu da yükleme uygulamasının görüntülenmeden önce parola uygulamasını gerektirir. PST dosyasına uygulanan şifre, mesaj deposunda saklanır. Ancak, parola mevcut araçlar tarafından kaldırılabileceğinden, bu güçlü bir veri koruması sağlamaz. Ayrıca, kullanıcı tarafından belirlenen şifre, şifreleme algoritmalarını kodlamak ve şifre çözmek için anahtarın bir parçası olarak kullanılmaz. Bu nedenle yetkisiz kişilerin erişebileceği verilerin korunmasının bir yararı yoktur. Parolanın orijinal dizgenin CRC-32 hash'i olarak saklanması da onu kaba kuvvet yaklaşımına karşı veri güvenliği için zayıf bir yöntem haline getirir.

## Referanslar ##

* [Outlook Kişisel Klasörleri (.pst) Dosya Biçimi](https://msdn.microsoft.com/en-us/library/ff385210(v#office.12).aspx)
* [Kişisel Klasör Dosya Biçimi Özellikleri](https://github.com/libyal/libpff/blob/master/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)

