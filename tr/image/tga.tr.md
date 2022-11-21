{
  "date" : "2019-10-11",
  "keywords" :[ "tga dosyası", "tga dosya biçimi", "tga dosyası nedir", "dosya", "tga örneği", "tga dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TGA Dosya Biçimi - Bir TARGA Grafik Görüntü Dosyası",
  "description":"TGA dosya formatı ve TGA dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "TGA",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## .tga dosyası nedir?

.tga uzantılı bir dosya bir raster grafik formatıdır ve Truevision Inc. tarafından oluşturulmuştur. TARGA (Truevision Advanced Raster Adapter) panoları için tasarlanmıştır ve IBM uyumlu PC'ler için Yüksek Renkli/gerçek renkli görüntü desteği sağlar. Piksel başına 8, 16, 24 ve 32 bit ve 8 bit alfa kanalını destekler. Görüntü boyutunu küçültmek için uygulanabilen kayıpsız RLE sıkıştırmasını da destekler. Dijital fotoğraflar ve dokular, TGA görüntü biçimini kullanır.

## Kısa Tarihçe

TGA dosya formatının oluşumu, AT&T tarafından renkli çerçeve arabellekleri için geliştirilen yeni teknolojilerin pazarlanması üzerinde çalışan AT&T EPICenter (daha sonra çıkarılan ve Truevision olarak bilinen bağımsız bir varlık olarak kurulan) tarafından 1984 yılında ortaya çıktı. EPICenter zaten ilk iki kartı olan VDA (Video Görüntü Bağdaştırıcısı) ve ICB (görüntü yakalama kartı) üzerinde çalışıyordu ve bu kartlar için .vda ve .icb adlı iki dosya türü üzerinde çalışma zaten devam ediyordu. Bu dosya formatları kodlandı ve daha az geniş spesifik dosya formatı TGA tanıtıldı. TGA, zaten kullanımda olanın bir uzantısıydı ve genişlik, yükseklik, piksel derinliği, ilişkili renk haritası ve görüntü kaynağı gibi bilgiler sağlıyordu.

1989'da yayınlanan TGA'nın 2.0 sürümü, aşağıdakiler gibi çeşitli gelişmiş özellikler içeriyordu:

* Küçük resimler
* Alfa kanalı
* Gama Değeri
* Metinsel Meta Veriler

TGA'nın 2.0 sürümüne başlıca katkıda bulunanlar arasında Truevision'dan Shawn Steiner, Kevin Fiedly ve David Spoelstra yer alıyor.

## TGA TARGA Dosya Biçimi Özellikleri

Bir TGA dosyası 2 ana bölümden oluşur:

* Başlık
* Renk Piksel bilgisi

Bir TGA dosyasındaki tüm değerler, biçim özelliklerine göre littl-endian'dadır.

### TGA Başlığı

Bir TGA dosya başlığı aşağıdaki 5 alandan oluşur.

|Alan no.|Uzunluk |Alan adı |Açıklama|
---|---|---|---|
|1| 1 bayt |Kimlik uzunluğu| Görüntü kimliği alanının uzunluğu (0-255)|
|2| 1 bayt |Renkli harita türü| Bir renkli haritanın dahil edilip edilmediği (0 - bu görüntüye hiçbir renk haritası verisinin dahil edilmediğini gösterir. 1 - bu görüntüye bir renk haritasının dahil edildiğini gösterir.)|
|3| 1 bayt |Görüntü türü| Sıkıştırma ve renk türleri (0- Görüntü Verisi Dahil Değildir. 1- Sıkıştırılmamış, Renkli eşlemeli görüntü, 2- Sıkıştırılmamış, Gerçek Renkli Görüntü, 9- Çalışma uzunluğu kodlu, Renk eşlemeli görüntü, 11- Çalışma Uzunluğu kodlu, Siyah beyaz görüntü )|
|4| 5 bayt |Renk haritası belirtimi| Renk haritasını tanımlar|
|5| 10 bayt |Görüntü belirtimi| Görüntü boyutları ve biçimi|

### Görüntü ve Renk Haritası Verileri

|Alan no. |Uzunluk |Alan |Açıklama|
---|---|---|---|
|6 |Görüntü kimlik uzunluğu alanından| Görüntü Kimliği| Tanımlayıcı bilgileri içeren isteğe bağlı alan|
|7 |Renk haritası belirtim alanından| Renk haritası verileri| Renk haritası verilerini içeren arama tablosu|
|8 |Görüntü özellikleri alanından| Görüntü verileri| Görüntü tanımlayıcısına göre saklanır|

### Geliştirici Alanı (Opsiyonel)

TGA Sürüm 2.0, birçok geliştiricinin daha fazla bilgi depolamak istediği ek geliştirmeler/ekstralar için destek sağlar. Bilgi isteğe bağlıdır, böylece bir TGA kod çözücü onu yorumlayamazsa yok sayılır.

### Genişletme Alanı (Opsiyonel)

|Alan numarası| uzunluk| Alan |Açıklama|
---|---|---|---|
|10| 2 bayt |Uzantı boyutu |Uzantı alanının bayt cinsinden boyutu, her zaman 495|
|11| 41 bayt| Yazar adı | Yazarın adı. Kullanılmazsa, baytlar NULL (\0) veya boşluklar| olarak ayarlanmalıdır.
|12| 324 bayt| Yazar yorumu| Her biri 80 karakter artı bir NULL|
|13| 12 bayt| Tarih/zaman damgası |Görüntünün oluşturulduğu tarih ve saat|
|14| 41 bayt| İş Kimliği||
|15| 6 bayt| İş süresi| Dosyayı oluşturmak için harcanan saat, dakika ve saniye (faturalandırma vb. için)|
|16| 41 bayt| Yazılım Kimliği |Dosyayı oluşturan uygulama.|
|17| 3 bayt| Yazılım versiyonu||
|18| 4 bayt| Anahtar rengi||
|19| 4 bayt| Piksel en boy oranı||
|20| 4 bayt| Gama değeri||
|21| 4 bayt| Renk düzeltme ofseti |Dosyanın başlangıcından varsa renk düzeltme tablosuna kadar olan bayt sayısı|
|22| 4 bayt| Posta pulu | Dosyanın başlangıcından varsa posta pulu görüntüsüne kadar olan bayt sayısı|
|23| 4 bayt| Tarama çizgisi ofseti| Dosyanın başlangıcından varsa tarama satırları tablosuna kadar olan bayt sayısı |
|24| 1 bayt| Öznitelikler türü| Alfa kanalını belirtir|

### Dosya Altbilgisi (İsteğe Bağlı)

Dosyanın son 26 baytı altbilgiyi temsil eder; bu, varsa muhtemelen bir TGA sürüm 2 dosyası anlamına gelir.

|Alan No.| uzunluk| alan| Açıklama|
---|---|---|---|
|28| 4 bayt| Uzatma ofseti| Dosyanın başından itibaren bayt cinsinden ofset|
|29| 4 bayt| Geliştirici alanı ofseti| Dosyanın başından itibaren bayt cinsinden ofset|
|30| 16 bayt| İmza| İçerir "TRUEVISION-XFILE"|
|31| 1 bayt| | İçerir "."|
|32| 1 bayt| | İçerir NULL|


## Referanslar

* [TGA 2.0 Dosya Biçimi Özellikleri](https://products.conholdate.app/viewer/view/rVqTeZPLAL/tga-file-format-specifications.pdf?default=view&preview = true.pdf)
* [Wikipedia'dan TGA](https://en.wikipedia.org/wiki/Truevision_TGA)

