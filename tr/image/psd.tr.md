{
  "date" : "2019-10-11",
  "keywords" :[ "psd dosyası", "psd dosya formatı", "psd dosyası nedir", "dosya", "psd örneği", "psd dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PSD - Photoshop Görüntü Dosyası Biçimi",
  "description":"PSD dosya formatı ve PSD dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "PSD",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## PSD dosyası nedir?

PSD, Photoshop Belgesi, Adobe Photoshop'un grafik tasarımı ve geliştirmesi için kullanılan yerel dosya formatını temsil eder. PSD dosyaları, görüntü katmanlarını, ayar katmanlarını, katman maskelerini, ek açıklamaları, dosya bilgilerini, anahtar sözcükleri ve diğer Photoshop'a özgü öğeleri içerebilir. Photoshop dosyalarının varsayılan uzantısı .PSD'dir ve maksimum 30.000 piksel yükseklik ve genişliğe ve iki gigabayt uzunluk sınırına sahiptir.

## PSD Dosya Biçimi Özellikleri ##

Bir PSD dosyasındaki veriler büyük endian bayt düzeninde saklanır. Bu, Windows platformunda okurken veya yazarken kısa ve uzun tam sayıların yer değiştirmesi anlamına gelir. Photoshop dosya formatı beş ana bölüme ayrılmıştır. Bir bölümden diğerine geçmek için kullanılabilecek birçok uzunluk işaretine sahiptir. Uzunluk işaretleri genellikle en yakın 2 veya 4 bayt aralığına yuvarlamak için baytlarla doldurulur. Beş ana bölüm şunlardır:

* Dosya Başlığı
* Renk Modu Verileri
* Görüntü Kaynakları
* Katman ve Maske Bilgileri
* Görüntü Verileri

Uyumluluk için, Photoshop bölümün tamamını okumaya çalışabileceğinden, bölümdeki tüm bu alanlara veri yazılmalıdır. Ayrıca bir dosyaya yazarken atlanan alanlara sıfırların yazılması anlamına gelir. Uzunlukla sınırlandırılmış bölümlerdeki uzunluk alanı, okumayı ne zaman durduracağınıza karar vermek için kullanılmalıdır. Çoğu durumda uzunluk alanı, takip eden kayıtların değil baytların sayısını gösterir. Bir dosyayı okurken aşağıdaki noktaların hatırlanması gerekir.

* Tüm tablolarda "Length" sütunundaki değerler bayt cinsindendir.
* Unicode dizesi olarak tanımlanan tüm değerler şunlardan oluşur:
* Dizedeki karakter sayısını (bayt değil) temsil eden 4 baytlık bir uzunluk alanı.
* Unicode değerleri dizisi, karakter başına iki bayt.

### Dosya Başlığı ###

Dosya başlığı, görüntünün temel özelliklerini içerir.

|Uzunluk|Açıklama
---|---|
|4|İmza: her zaman '8BPS'ye eşittir. İmza bu değerle eşleşmiyorsa dosyayı okumaya çalışmayın.
|2|Sürüm: her zaman 1'e eşittir. Sürüm bu değerle eşleşmiyorsa dosyayı okumaya çalışmayın. (~*~*PSB~*~* sürüm 2'dir.)
|6|Ayrılmış: sıfır olmalıdır.
|2|Herhangi bir alfa kanalı dahil olmak üzere görüntüdeki kanalların sayısı. Desteklenen aralık 1 ila 56'dır.
|4|Görüntünün piksel cinsinden yüksekliği. Desteklenen aralık 1 ila 30.000'dir.
|4|Görüntünün piksel cinsinden genişliği. Desteklenen aralık 1 ila 30.000'dir.
|2|Derinlik: kanal başına bit sayısı. Desteklenen değerler 1, 8, 16 ve 32'dir.
|2|Dosyanın renk modu. Desteklenen değerler şunlardır: Bitmap # 0; Gri tonlama # 1; 2 numaralı indeksli; RGB#3; CMYK#4; Çok kanallı #7; Çift ton # 8; Laboratuvar # 9.

### Renk Modu Veri Bölümü ###

Renk modu verileri bölümü şu şekilde yapılandırılmıştır:


|Uzunluk|Açıklama
---|---|
|4|Aşağıdaki Renk verilerinin uzunluğu
|değişken|Renk verileri

Renk modu verileri, Dosya Başlığı bölümündeki mod alanı tarafından tanımlandığı şekilde yalnızca dizinlenmiş renk ve çift ton için kullanılabilir. Diğer tüm modlar için bu bölüm 4 baytlık sıfırlanmış değerlerle temsil edilir. İndekslenmiş renkli görüntüler için uzunluk 768'dir ve renk verileri, görüntünün renk tablosunu serpiştirmesiz sırayla içerir. Çift ton görüntüler için, renk verileri çift ton özelliğini içerir (biçimi belgelenmemiştir). Photoshop dosyalarını okuyan diğer uygulamalar, bir çift tonlu görüntüyü gri bir görüntü olarak değerlendirebilir ve dosyayı okurken ve yazarken yalnızca çift tonlu bilgilerin içeriğini koruyabilir.

### Görüntü Kaynakları Bölümü ###

Dosyanın üçüncü bölümü görüntü kaynaklarını içerir. Bir uzunluk alanıyla başlar, ardından bir dizi kaynak bloğu gelir.


|Uzunluk|Açıklama
---|---|
|4|Görüntü kaynağı bölümünün uzunluğu. Uzunluk sıfır olabilir.
|Değişken|Görüntü Kaynakları (Görüntü Kaynak Blokları)

Görüntü kaynakları, kalem aracı yolları gibi görüntülerle ilişkili piksel olmayan verileri depolamak için kullanılır. Photoshop'un ilk sürümlerinde Macintosh'un kaynağında saklanan verileri tuttukları için kaynak blokları olarak adlandırılırlar. Görüntü kaynak bloklarının temel yapısı aşağıda gösterildiği gibidir:


|Uzunluk|Açıklama
---|---|
|4|İmza: '8BIM'
|2|Kaynak için benzersiz tanımlayıcı. Görüntü kaynak kimlikleri, Photoshop tarafından kullanılan kaynak kimliklerinin bir listesini içerir.
|Değişken|Ad: Pascal dizesi, boyutu çift yapmak için doldurulmuştur (boş ad iki bayt 0'dan oluşur)
|4|Takip eden kaynak verilerinin gerçek boyutu
|Değişken|Tek tek kaynak türleri ile ilgili bölümlerde açıklanan kaynak verileri. Boyutu eşit hale getirmek için yastıklıdır.

Görüntü kaynakları birkaç standart kimlik numarası kullanır.

### Katman ve Maske Bilgileri ###

Bir Photoshop dosyasının dördüncü bölümü, katman sayısı, katmanlardaki kanallar, karıştırma aralıkları, ayarlama katmanı tuşları, efekt katmanları ve maske parametreleri gibi katmanlar ve maskeler hakkında bilgiler içerir. Katman veya maske yoksa, bu bölüm sıfırlanmış 4 baytlık alanla temsil edilir. Sıfırlanmış değerler nedeniyle bu bölümü okurken bölümlerin uzunluğuna özel dikkat gösterilmelidir. Layer ve Mask bölümünün dizilişi şu şekildedir:


|Uzunluk|Açıklama
---|---|
|4|Katman ve maske bilgileri bölümünün uzunluğu. (PSB uzunluğu 8 bayttır.)
|Değişken|Katman bilgisi
|Değişken|Global katman maskesi bilgisi
|Değişken|Çeşitli veri türlerini içeren etiketli bloklar dizisi.

#### Katman Bilgisi ####

Aşağıdaki tablo, katman bilgilerinin üst düzey organizasyonunu gösterir.


|Uzunluk|Açıklama
---|---|
|4|Katman bilgisi bölümünün uzunluğu, 2'nin katına yuvarlanmış. (PSB uzunluğu 8 bayttır.)
|2|Katman sayısı. Negatif bir sayı ise, mutlak değeri katman sayısıdır ve ilk alfa kanalı, birleştirilmiş sonuç için saydamlık verilerini içerir.
|Değişken|Her katman hakkında bilgi. Bkz. Katman kayıtları, her katman için bu bilgilerin yapısını açıklar.
|Değişken|Kanal görüntü verileri. Her katman için bir veya daha fazla görüntü veri kaydı içerir. Katmanlar, katman bilgisindekiyle aynı sıradadır.

### Görüntü Verileri ###

Görüntü piksel verileri, dosyanın Görüntü Verileri bölümünde bulunur. Görüntü Verileri bölümündeki verilerin düzenlenmesi düzlemsel sıradadır, yani önce tüm kırmızı veriler, ardından tüm yeşil veriler vb. aşağıdaki tabloda gösterildiği gibi.

|Uzunluk|Açıklama
---|---|
|2|Sıkıştırma yöntemi: *0 = Ham görüntü verisi * 1 = RLE sıkıştırılmış görüntü verisi, her bir sayım iki baytlık bir değer olarak saklanarak tüm tarama satırları (satırlar * kanallar) için bayt sayımlarıyla başlar. Bunu RLE sıkıştırılmış verileri takip eder ve her tarama satırı ayrı ayrı sıkıştırılır. RLE sıkıştırması, Macintosh ROM rutini PackBits ve TIFF standardı tarafından kullanılan sıkıştırma algoritmasının aynısıdır. *2 = Tahminsiz ZIP *3 = Tahminli ZIP.
|Değişken|Görüntü verileri. Düzlem düzeni = RRR GGG BBB, vb.

## Referanslar ##

* [PSD Dosya Biçimi Özellikleri - Adobe Tarafından](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/#50577409_pgfId-1030196)
* [Adobe Photoshop Dosya Biçimi](https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)

