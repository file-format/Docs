{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EDB Dosya Biçimi - Bir Exchange Posta Veritabanı Dosyası",
  "description":"EDB dosya formatı ve EDB dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "EDB",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2020-09-16"
}

## EDB dosyası nedir?

.edb dosya uzantılı bir dosya, posta ile ilgili verileri depolamak için Microsoft Exchange Server tarafından oluşturulan posta kutusu veritabanıdır. EDB, Exchange Veritabanı, işlemde olan ve SMTP olmayan iletileri depolar. EDB, Genişletilebilir Depolama Motoru (ESE) Veritabanı dosyaları olarak da bilinir ve dosyaları b-tree yapısını kullanarak depolar. Depolama dosyaları olan EDB dosyaları, [PST](/tr/email/pst/) ve [OST](/tr/email/ost/) gibi diğer posta depolama dosyası biçimlerine dönüştürülebilir.

## EDB Dosya Biçimi

Başvurulabilecek resmi/açık EDB dosya biçimi belirtimi yoktur. Dosya biçiminin tersine mühendislik işlemine yönelik bazı ilerlemeler kaydedilmiştir ve bu da kısmi belirtimlerin kodunun çözülmesiyle sonuçlanmıştır. Bunlara göre, bir EDB dosyası şunlardan oluşur:
* Dosya Başlığı - Veritabanı dosya başlığı bilgilerini içerir
* Sabit Boyutlu Sayfalar - Tablolardan ve dizinlerden oluşan veritabanını içerir

### Veritabanı Dosya Başlığı
Veritabanı dosya başlığı, ilk veritabanı sayfasında bulunur ve en az 668 bayttır. Dosya başlığı, diğer alanlara ek olarak "Dosya Biçimi Sürümü" ve "Dosya Türü"nü içerir.

#### Dosya Türleri
|Tür|Açıklama
---|---|
|0| Veritabanı|
|1| Akış|

`Not:` Bu türler için tanımlayıcılar bilinmiyor.

#### Dosya Formatı Sürümü
EDB'nin orijinal formatı Nisan 1997'de başladı ve daha sonraki değişiklikler için gelişmeye devam etti.

|Revizyon Tarihi|Sürüm|Revizyon|açıklama
---|---|---|---|
|Nisan 1997| 0x00000620|0x00000000| Orijinal işletim sistemi Beta formatı.|
|Mayıs 1997 |0x00000620|0x00000001| Koşullu indeksleme ve ESKİ için kataloğa sütun ekleyin.|
|Haziran 1997|0x00000620|0x00000002|IDB'de fLocalizedText bayrağını ekleyin.|
|Ekim 1997|0x00000620|0x00000003|SPLIT_BUFFER'ı uzay ağacı kök sayfalarına ekleyin.|
|Ocak 1998|0x00000620|0x00000002|ESE97'nin ileri uyumlu kalması için revizyonu geri alın.|
||0x00000620|0x00000003|Kataloğa yeni etiketlenmiş sütunlar ekleyin ("CallbackData" ve "CallbackDependencies").|
|Mayıs 1998|0x00000620|0x00000004|Süper Uzun Değer (SLV) desteği: dbheader'da signSLV, fSLVExists.|
|Mayıs 1998|0x00000620|0x00000005|Yeni SLV uzay ağacı.|
|Ekim 1998|0x00000620|0x00000006|SLV uzay haritası.|
|Aralık 1998|0x00000620|0x00000007|4 bayt IDXSEG.|
|Ocak 1999|0x00000620|0x00000008|Yeni şablon sütun biçimi.|
|Haziran 1999|0x00000620|0x00000009|Sıralı şablon sütunları. Windows XP SP3'te kullanılır |
||0x00000620|0x0000000b|Exchange'te kullanılan ECC sağlama toplamını içeren sayfa başlığını içerir|
||0x00000620|0x0000000c|Windows Vista'da (SP0) kullanılır|
||0x00000620|0x00000011|2 KiB, 16 KiB ve 32 KiB sayfası desteği.Ek ECC sağlama toplamları ile genişletilmiş sayfa başlığı.Sütun sıkıştırma.Boşluk ipuçları.Windows 7'de kullanılır (SP0)|
|Mayıs 1999|0x00000623|0x00000000|Yeni Alan Yöneticisi.|

### Veritabanı Dosyaları

EDB veritabanı dosyası, veritabanındaki tüm tabloların şemasını içerir. Ayrıca, tüm veritabanı tabloları için kayıtlar ve tablolar için indeksler de içerir. Konumu aşağıdaki tanımlayıcılar tarafından belirlenir.

* JetCreateVeritabanı
* JetCreateDatabase2
* JetAttachVeritabanı
* JetAttachDatabase2

Bunlara dayanarak, veritabanının durumu aşağıdaki gibi değerlendirilebilir.

|Değer|Tanımlayıcı|Açıklama
---|---|---|
|1|JET_dbstateJustCreated|Veritabanı yeni oluşturuldu.|
|2|JET_dbstateDirtyShutdown|Veritabanı kullanılabilir veya taşınabilir hale gelmesi için donanımsal veya yazılımsal kurtarmanın çalıştırılmasını gerektirir. Veritabanlarını bu durumda taşımaya çalışmamak gerekir.|
|3|JET_dbstateCleanShutdown|Veritabanı temiz durumda. Veritabanı herhangi bir günlük dosyası olmadan eklenebilir.|
|4|JET_dbstateBeingConverted|Veritabanı yükseltiliyor.|
|5|JET_dbstateForceDetachInternal|Bu değer WindowsXP'de sunulmuştur|
 

## Referanslar
* [Genişletilebilir Depolama Motoru (ESE) Veritabanı Dosyası (EDB) Spesifikasyonları](https://github.com/libyal/libesedb/tree/main/documentation)

