{
  "date" : "2021-03-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RPL - Rapor Sayfa Düzeni",
  "keywords" :[ "rpl", "Rapor Sayfası Düzeni", "XSD", "SQL Sunucusu", "raporlama"],
  "description":"Microsoft SQL Server Reporting Services tarafından görüntüleyici denetimleriyle iletişim kurulurken kullanılan dahili bir ikili biçim olan RPL akış biçimi hakkında bilgi edinin.",
  "linktitle" : "RPL",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-02"
}

## RPL dosyası nedir? ##

RPL (Rapor Sayfası Düzeni) akış formatı, MS SQL Server Raporlama Servisleri tarafından, sunucudan istemci görüntüleyici kontrolüne yönelik işleme işinin bir kısmını azaltmak için görüntüleyici kontrolleriyle iletişim kurarken kullanılan dahili bir ikili biçimdir. Geliştiriciler, raporları görüntülemek için RPL dosyasını işleyen ve görüntüleyen özel rapor oluşturucuların yanı sıra RPL oluşturacak olan RPL'yi kullanarak özel rapor tasarımcıları oluşturabilir.

## RPL Yapıları

Bir RPL akışı, akış yapısını, rapor yapısını, rapor özelliklerini ve numaralandırmaları içerir. Her yapı aşağıdakileri içerir:

- Yapının tanımı.

- Yapı için Artırılmış Backus-Naur Formu (ABNF) grameri.

- Yapının bir bit diyagramı.

- Yapı içinde yer alan tüm alanların tanımları.

İşte bazı RPL Yapıları hakkında kısa notlar:

### Akış Yapısı
Akış yapısı bir dizi kayıttan oluşur. Bir kayıt, rapor düzenini içeren sıfır veya daha fazla yapılandırılmış alan içerir.

#### RPL Akışı
RPL akışı yalnızca bir Rapor kaydına sahip olmalı ve akış, rapor hiyerarşisini koruyan bir dizi ikili kayıt olmalıdır.

#### Kayıt
Kayıt, bir raporla ilgili bilgileri tutmak için kullanılan temel bir yapı taşıdır. Bir kayıt, değişken uzunlukta bir bayt dizisinden oluşur. Bir kayıt iki bileşenden oluşur:
- Bir kayıt türü
- O kayıt tipine özel kayıt verileri.
Kayıt türü, kayıt tarafından ne tür bilgilerin belirtildiğini ve kayda ilişkin kayıt verilerinin yapısının nasıl sıralandığını ve yapılandırıldığını tanımlayan bir bayttır. Kayıt değeri, o kayda özel veri tipine bağlıdır.

#### Basit Veri Tipi Yapıları

Aşağıdaki tablo, bir RPL akışındaki veri türlerini tanımlar.

|Açıklama| format|
---|---|
|Char|16 bit (2 bayt) sayısal (sıralı) bir değeri temsil eder.|
|Bayt|8 bitlik (1 bayt) işaretsiz bir tam sayıyı temsil eder.|
|Int16|16 bitlik (2 bayt) işaretli bir tamsayıyı temsil eder.|
|Tek|32 bit (4 bayt) tek duyarlıklı kayan nokta değerini temsil eder.|
|Ondalık|128 bit (16 bayt) veri türünü temsil eder.|
|DateTime|Bir tarih ve saat değerinin 64 bit (8 bayt) kodlamasını temsil eder.|
|Int64|64-bit (8-byte) işaretli bir tamsayıyı temsil eder.|
|Int32|32 bit (4 bayt) işaretli bir tam sayıyı temsil eder.|
|Float|32 bit (4 bayt) tek duyarlıklı kayan nokta değerini temsil eder.|
|Boolean|8 bitlik (1 baytlık) bir mantıksal Boole tipi değeri temsil eder. Geçerli değerler true (1) ve false'tur (0).|
|Uzun|64 bit (8 bayt) işaretli bir tam sayıyı temsil eder.|
|Dize|Protokol içindeki tüm Dize değerleri UNICODE UTF-16 OLMALIDIR. Varsayılan olarak, tüm String değerleri, String'in uzunluğunu tanımlayan bir tamsayı ile başlar. Dize değerleri, protokolde bir bayt dizisi olarak temsil edilir; bayt sayısı, String'deki karakter sayısının iki ile çarpımına eşit OLMALIDIR.|

### Rapor Yapıları
Rapor yapıları, ilgili yapılarının ve öğelerinin tanımlarını ve boyutlarını içerir.

Aşağıdaki liste, rapor yapılarını belirtir:

- Bildiri
- Sürüm
- Rapor Özellikleri
- Ofset Dizi Elemanı
- Sayfa içeriği
- Sayfa
- Sayfa özellikleri
- Sayfa düzeni
- Bölüm
- Basit Bölüm
- Karışık Bölüm
- Kesit Özellikleri
- Vücut Bölgesi Elemanı
- Sayfa Başlığı Öğesi
- Sayfa Alt Bilgi Öğesi
- Gövde Elemanı
- Eleman Özellikleri
- Paylaşılan Öğe Özellikleri
- Paylaşılan Öğe Özelliklerini Kullanın
- InlineSharedElementÖzellikleri
- PaylaşılmayanElementÖzellikleri
- Stil
- Paylaşılan Stil Özellikleri
- Paylaşılmayan Stil Özellikleri
- Eylem Bilgisi
- ActionInfoContent
- Eylem
- ActionImageMapAreas
- ActionInfoWithMaps
- DynamicImageData
- ImageConsolidationOffsets
- Rapor Öğesi
- Astar
- Resim
- ImageDataProperties
- UseSharedImageDataProperties
- InlineSharedImageDataProperties
- NonSharedImageDataProperties
- Görüntü Verileri
- ImageMapAreas
- Görüntü Haritası Alanı
- Çizelge
- Gösterge Paneli
- Harita
- Dikdörtgen
- Alt Rapor
- Zengin Metin Kutusu
- Paragraf İçeriği
- Metin Çalıştır
- paragraf
-RichTextBoxStructure
- Tablix
- TablixContent
- TablixStructure
- Tablix Ölçümleri
- Sütun Genişlikleri
- Sütun Bilgileri
- RowHeights
- Sıra Bilgisi
- TablixRow
- TablixRowCell
- TablixCorner
- TablixColumnHeader
- TablixRowHeader
- TablixBodyRowCells
- TablixBodyRow
- TablixBodyCell
- TablixRowMembersDef
- TablixColMembersDef
- TablixMemberDef
- Ölçümler
- Ölçüm
- ReportElementEnd

### Özellikleri
Bir RPL Akışında kullanılabilecek özelliklerin listesi aşağıdadır:

- kimlik
- Sütun Sayısı
- Sütun Aralığı
- Benzersiz Ad
- İsim
- Etiket
- Yer imi
- Araç İpucu
- Öğeyi Değiştir
- Tanım
- Konum
- ConsumeContainerWhiteSpace (RPL 10.6)
- Dil
- Uygulama vakti
- Yazar
- Otomatik yenileme
- Rapor Adı
- Sayfa Yüksekliği
- Sayfa genişliği
- MarginTop
- Sol Kenar Boşluğu
- Sağ Kenar Boşluğu
- Alt Kenar Boşluğu
- Sütunlar
- SayfaAdı (RPL 10.6)
- Eğimli
- Büyüyebilir
- CanShrink
- Değer
- Durumu Değiştir
- CanSort
- Sıralama Durumu
- formül
- IsToggleParent
- Tür kodu
- Orijinal değeri
- Basit
- İçerik Ofseti
- AkışAdı
- boyutlandırma
- LinkToChild
- İlk Sayfada Yazdır
- Bölümler Arasında Yazdır (RPL 10.4)
- FormattedValueExpressionBased
- ProcessedWithError
- ImageMIMEType
- ResimAdı
- Genişlik
- Yükseklik
- Yatay Çözünürlük
- Dikey Çözünürlük
- Ham Biçim
- köprü
- Yer İşareti Bağlantısı
- Detaylandırma Kimliği
- DrillthroughUrl
- Sınır rengi
- BorderColorLeft
- BorderColorRight
- BorderColorTop
- BorderColorBottom
- Sınır Stili
- BorderStyleLeft
- BorderStyleRight
- BorderStyleTop
- BorderStyleBottom
- Sınır Genişliği
- Sınır GenişliğiSol
- Sınır Genişliği Sağ
- Sınır GenişliğiÜst
- BorderWidthBottom
- Sola Dolgu
- DolguSağ
- Dolgu Üstü
- Alt Dolgu
- Yazı stili
- Font ailesi
- Yazı Boyutu
- Yazı Tipi Ağırlığı
- Biçim
- Metin Dekorasyonu
- Metin hizalama
- Dikey Hizalama
- Renk
- Satır yüksekliği
- Yön
- Yazma Modu
- UnicodeBiDi
- Arka plan görüntüsü
- Arka plan rengi
- Arka Plan Tekrarı
- Sayı Dili
- NumeralVariant
- Takvim
- ColumnHeaderRows
- RowHeaderColumns
- ColsBeforeRowHeader
- Düzen Yönü
- Tanım Yolu
- Seviye
- ÜyeCellIndex
- CellItemOffset
- ColSpan
- RowSpan
- DefIndex
- Sütun Dizini
- RowIndex
- Grup Etiketi
- RecursiveToggleLevel
- Liste biçimi
- Liste Seviyesi
- ParagrafNumarası
- Sağ Girinti
- Sol Girinti
- Asılı girinti
- Boşluktan Önce
- Uzaydan Sonra
- İlk satır
- İşaretleme
- İçerikÜst
- İçerikSol
- İçerik Genişliği
- İçerik Yüksekliği
- Durum
- CellItemState
- MemberDefState

### Numaralandırmalar
Aşağıdaki liste, RPL akışında kullanılabilecek numaralandırmaları gösterir:

- Sıralama Seçenekleri
- Boyutlandırma
- Şekil Türü
- ImageRawFormat
- Yazı Tipi Stilleri
- Yazı Tipi Ağırlıkları
- Metin Süslemeleri
- Metin Hizalamaları
- Dikey Hizalamalar
- Talimatlar
- Yazma Modları
- UnicodeBiDiType'lar
- Takvimler
- Sınır Stilleri
- BackgroundRepeatTypes
- Liste Stilleri
- İşaretleme Stilleri
- Tür kodu
- Durum Değerleri
- TablixMemberStateValues
- TablixMemberDefStateValues
- RPLSize





## Referanslar ##

- [Rapor Sayfası Düzeni (RPL) İkili Akış Biçimi](https://docs.microsoft.com/en-us/openspecs/sql_server_protocols/ms-rpl/9c4ff7ba-f6da-4092-9670-aa0e54e73887)

