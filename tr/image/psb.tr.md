{
  "date" : "2019-10-11",
  "keywords" :[ "psb dosyası", "psb dosya formatı", "psb dosyası nedir", "dosya", "psb örneği", "psb dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PSB - Photoshop Büyük Resim Dosya Formatı",
  "description":"PSB dosya formatı ve PSB dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "PSB",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## .PSB dosyası nedir?
Adobe photoshop, dosyaları iki biçimde kaydeder. 30.000 x 30.000 piksel boyutundaki dosyalar PSD uzantısıyla, PSD'den büyük dosyalar ise 300.000 x 300.000 piksele kadar olan dosyalar “Photoshop Big” olarak bilinen PSB uzantısıyla kaydedilir. Daha spesifik olarak, PSB dosyaları, 300.000 piksele kadar yükseklik ve genişliğe sahip görüntülerle 4 EB (4,2 milyar GB'ın üzerinde) büyüklüğünde olabilir. PSD'ler ise maksimum 2 GB'a kadar ve 30.000 piksel görüntü boyutuna sahip olabilir.

PSB, photoshop için geniş format boyutu olarak da bilinir ve katmanlar, efektler ve filtreler gibi tüm photoshop özelliklerini destekler. Photoshop, PSB dosyasını [PSD](/tr/image/psd/), [JPG](/tr/image/jpeg/) formatına dönüştürebilir. , [PNG](/tr/image/png/), [EPS](/tr/page-description-language/eps/), [GIF](/tr/image/gif/) ve diğer biçimler. Photoshop geniş belge formatı, Photoshop'un tercihler iletişim kutusunun dosya işleme bölmesi özelliği etkinleştirildiğinde kullanılabilir.

## Dosya Biçimi Bilgileri ##

Photoshop dosya formatı, bölümler arasında hareket etmek için birçok uzunluk işaretçisi ile beş ana bölüme ayrılmıştır.

|Dosya formatı
---|
|Dosya Başlığı
|Renk Modu Verileri
| Görüntü Kaynakları
|Katman ve Maske Bilgileri
|(((
Görüntü Verileri
)))

### Dosya Başlığı ###

Dosya başlığı sabit 26 bayt uzunluğa sahiptir ve görüntünün temel özelliklerini içerir.

BAYT İmzası [4] – '8BPS'ye eşittir.

WORD Sürümü [2] – Sürüm Numarası, PSD # 1, PSB # 2.

BYTE Ayrılmıştır [6] – Ayrılmıştır ve her zaman sıfırdır.

WORD Kanalları [2] – Görüntüdeki alfa kanalları dahil renk kanallarının sayısı. Değeri 1 ile 56 arasında değişir.

LONG Rows [4] – Görüntünün piksel cinsinden yüksekliği, PSD 1-30.000, PSB 1-300.000.

UZUN Sütunlar [4] – Görüntünün piksel cinsinden genişliği, PSD 1-30.000, PSB 1-300.000.

WORD Derinliği [2] – Kanal başına bit sayısı. Desteklenen değerler 1,8,16 ve 32'dir.

WORD Modu [2] – Dosyanın Renk Modu.

#### Mod Açıklama ####


|Mod|Açıklama
---|---|
|0|Bitmap (tek renkli)
|1|Gri tonlamalı
|2|Dizine eklendi
|3|RGB
|4|CMYK
|7|Çok kanallı
|8|Çift ton (yarım ton)
|9|Laboratuvar

### Renk Modu Verileri ###

Dosya başlığı bölümünden sonra renk modu verileri bölümü gelir. Blok, bloğun uzunluğunu bayt cinsinden veren LONG Number ile başlar. Renk modu verilerinin yapısı aşağıdaki gibidir:

4 bayt – Aşağıdaki renk verilerinin uzunluğu.

Değişken – Renk Verisi

Başlık bölümündeki mod alanı değeri Dizinlenmiş Renk veya çift ton değilse blok uzunluğu 0 olur ve uzunluk alanından sonra veri olmaz.

Dizinlenmiş Renkli Görüntüler için uzunluk 768 bayt olacak ve 256 renk paleti içerecektir. Çift ton için, veriler ekran parametrelerini ve diğer ilgili bilgileri içerecektir.

### Görüntü Kaynakları ###

Renk modu veri bölümünün ardından üçüncü blok, görüntü kaynakları bölümüdür. İlk dört bayt, bloğun uzunluğunu ve ardından bir dizi kaynak bloğunu belirten UZUN bir sayıdır. Görüntü kaynak bloğunun yapısı aşağıdaki gibidir:

BAYT Türü [4] – İmza '8BIM'

WORD ID [2] – Görüntü Kaynak Kimliği. Referans bağlantısından görülebilen Kaynak Kimliklerinin bir listesi vardır.

BYTE Adı [Değişken] – Ad: Çift uzunlukta Pascal Dizisi. ** **

UZUN Boyut [4] – Aşağıdaki kaynak verilerinin Gerçek Boyutu.

BYTE Verisi [Değişken} – Kaynak verisi. Eşit boyutta olması için dolguludur.

Kaynak biçimlerinden bazıları aşağıda kısaca açıklanmıştır:

**Kılavuz ve Kılavuzlar Kaynak Biçimi:** Kılavuz ve Kılavuzlar bilgileri, kaynak bloğunda saklanır. Bu kaynak blokları, 16 baytlık ızgara ve kılavuz başlığını takiben 5 baytlık kılavuz bilgisi blokları içerir.

**Küçük Resim Kaynak Formatı:** Küçük resim bilgileri, 28 bayt başlık ve RGB'de JFIF küçük resminden oluşan önizleme ekranı için resim kaynak bloğunda saklanır.

**Renk örnekleyicileri Kaynak Biçimi:** Renk örnekleyici bilgileri, 8 baytlık bir başlık ve ardından değişken uzunlukta bir renk örnekleyici bilgisi bloğu ile görüntü kaynak bloğunda saklanır.

### Katman ve Maske Bilgileri ###

Dördüncü blok, katman ve maske bilgi bloğudur ve katmanlar ve maskeler hakkında bilgi içerir. Önce katman bilgileri, ardından maske bilgileri saklanır.

**Katman Bilgileri:** Katman bilgisi, katman bilgisinin uzunluğunu gösteren LONG değeriyle başlar. Bundan sonra, takip edilecek katman kayıtlarının sayısını gösteren WORD değeri sayısı gelir.

[8] – katmanların uzunluğu

[2] – Katman Sayısı

[Değişken] – Her katman hakkında bilgi.

[Değişken] – Kanal görüntü verileri.** **

**Maske Bilgileri:** Maske yapısı aşağıdaki biçime sahiptir:


|Veri Yapısı|Alan Adı| Tanım
---|---|---|
|SÖZ| Bindirme Renk Alanı| (belgelenmemiş)
|BAYT[8]| Renk Bileşenleri| 4x2 bayt renk bileşenleri
|SÖZ| Opaklık| 0#saydam, 1#opak
|BAYT| tür| 0#ters çevrilmiş, 1#korumalı, 128#depolanmış değeri kullan
|BAYT| dolgu| sıfıra ayarla

### Görüntü Verileri ###

Son bölüm, görüntü piksel verilerini içerir. Görüntü verileri, düzlemlerde bir dizi dizi olarak depolanır, yani önce tüm kırmızı veriler, ardından tüm yeşil veriler vb. Her satırın başındaki WORD, her bir tarama satırıyla ilgili bayt cinsinden boyutu gösterir.

[2] – Sıkıştırma yöntemi:

[Değişken] – Düzlemsel sırada Görüntü Verileri, yani RRRR, GGGG, BBBB vb.

Sıkıştırma Yöntemleri:

0 – Raw Görüntü Verileri

1 – Sıkıştırılmış RLE

2 – Tahminsiz Zip

3 – Tahminli Zip

## Referans ##

* [PSB Dosya Biçimi - Adobe Tarafından](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)
* [PSB - Wikipedia](https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)

