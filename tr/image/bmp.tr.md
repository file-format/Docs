{
  "date" : "2019-10-11",
  "keywords" :[ "bmp dosyası", "bmp dosya formatı", "bmp dosyası nedir", "dosya", "bmp örneği", "bmp dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BMP - Görüntü Dosyası Biçimi",
  "description":"BMP dosya formatı ve BMP dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "BMP",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

# BMP dosyası nedir? #

.BMP uzantılı dosyalar, bitmap dijital görüntüleri depolamak için kullanılan Bitmap Görüntü dosyalarını temsil eder. Bu görüntüler, grafik bağdaştırıcısından bağımsızdır ve aygıttan bağımsız bit eşlem (DIB) dosya biçimi olarak da adlandırılır. Bu bağımsızlık, dosyayı Microsoft Windows ve Mac gibi birden çok platformda açma amacına hizmet eder. BMP dosya formatı, verileri çeşitli renk derinliklerine sahip hem tek renkli hem de renkli formatta iki boyutlu dijital görüntüler olarak depolayabilir.

## BMP Dosya Biçimi Özellikleri ##

Aygıttan Bağımsız Bit Eşlemler, aygıtlar ve uygulamalar arasında bit eşlem değiş tokuşuna yardımcı olur. Bu dosya biçiminin sürekli gelişimi nedeniyle, başlıklarda yer alan bilgiler Bitmap sürümüne göre farklı olabilir. Tek bir bitmap dosyası, belirli bir sıradaki sabit ve değişken boyutlu yapılardan oluşur.

Bir Bitmap dosyasındaki yapılar aşağıdaki sırayla düzenlenir:


|Yapı|Opsiyonel|Boyut|Amaç
---|---|---|---|
|Dosya Başlığı|Hayır|14|Bitmap görüntü dosyası hakkında genel bilgileri saklamak için
|DIB Başlığı|Hayır|Sabit Boyutlu|Bitmap görüntüsü hakkında ayrıntılı bilgileri depolamak ve piksel formatını tanımlamak için
|Ekstra Bit Maskeleri|Evet|12 veya 16 bayt|Piksel formatını tanımlamak için
|Renk Paleti|Yarı isteğe bağlı|Değişken boyutlu|Bitmap görüntü verileri tarafından kullanılan renkleri tanımlamak için
|Gap1|Evet|Değişken boyutlu|Yapı hizalaması
|Piksel Dizisi|Hayır|Değişken boyutlu|Piksel formatı, DIB başlığı veya Ekstra bit maskeleri tarafından tanımlanır.
|Gap2|Evet|Değişken boyutlu|Yapı hizalaması
|ICC Renk profili|Evet|Değişken boyutlu|Renk yönetimi için renk profilini tanımlamak için

Bir bitmap görüntüsü belleğe yüklendiğinde, Windows tarafından GDI API aracılığıyla kullanılan bir DIB yapısı haline gelir. Dosya başlığı bu veri yapısının parçası değildir. Renk ayrıca, açık RGB renk tanımları yerine o anda başvurulan palete dizinler oluşturan 16 bitlik girişlerden oluşabilir. Bunlardan bazılarına, özellikle de başlıklara ayrıntılı olarak bir göz atalım.

### Bitmap Dosya Başlığı ###

Bir Bitmap Dosya Başlığı, dosyayı tanımlamak için kullanılan diğer dosya başlıklarına benzer. BMP dosya formatının farklı varyantları olduğundan, BMP dosya formatının ilk 2 baytı ASCII kodlamasında "B" karakteri ve ardından "M" karakteridir. Tüm tamsayı değerleri, little-endian biçiminde saklanır.

|Ofset hex|Offset aralığı|Boyut|Amaç
---|---|---|---|
|00|0|2 bayt|BMP ve DIB dosyasını tanımlamak için kullanılan başlık alanı 0x42 0x4D'dir ve ASCII'deki BM ile aynıdır. Olası değerleri takip edebilir.* **BM** – Windows 3.1x, 95, NT, ... vb. * **BA** – OS/2 struct bitmap dizisi * **CI** – OS/2 struct renk simgesi * **CP** – OS/2 sabit renk işaretçisi * **IC** – OS/2 yapı simgesi * **PT** – OS/2 işaretçisi
|02|2|4 bayt|BMP dosyasının bayt cinsinden boyutu
|06|6|2 bayt|Ayrılmış; gerçek değer, görüntüyü oluşturan uygulamaya bağlıdır
|08|8|2 bayt|Ayrılmış; gerçek değer, görüntüyü oluşturan uygulamaya bağlıdır
|0A|10|4 bayt|Bit eşlem görüntü verilerinin (piksel dizisi) bulunabileceği baytın ofseti, yani başlangıç adresi.

#### DIB başlığı (bitmap bilgi başlığı) ####

Görüntüyle ilgili ayrıntılı bilgiler bu başlıkta gösterilir. Bu bilgilere göre görüntünün ekranda görüntülenmesi için kullanılacak uygulama belirlenir. Bu tür başlıkların tümü, boyutlarını belirten bir DWORD (32-bit) alanı içerir, böylece bir uygulama, görüntüde kullanılan başlığı kolayca belirleyebilir. Bunun temel nedeni, DIB formatının çeşitli uzantılardan geçmesidir. Listelenen alanlara sahip DIB Başlığı aşağıdadır.

#### Renk paleti ####

Bir BMP renk paleti, bir görüntüleme cihazının renk paletindeki her bir rengin RGB yoğunluk değerlerini belirten bir yapılar dizisidir. Bit eşlem verilerindeki her piksel, renk paletinde dizin olarak kullanılan tek bir değeri depolar. Bu dizindeki öğede depolanan renk bilgisi, o pikselin rengini belirtir. Bir bitmap dosyasındaki rengin kullanılabilirliği aşağıdaki gibi değişir:

* Bir, 4 ve 8 bit - her zaman bir renk paleti içermesi beklenir
* On altı, 24 ve 32 bit - asla renk paleti içermez
* On altı ve 32 bit BMP dosyaları - renk paleti yerine bit alanları maske değerleri içerir

#### Piksel Depolama ####

Bitmap pikselleri, her satırın boyutunun dolgu ile 4 baytın katına (32 bit DWORD) yuvarlandığı satırlarda paketlenmiş bitler olarak depolanır. Bir görüntünün piksellerini depolamak için gereken toplam bayt miktarı, yalnızca bitlerin sayılmasıyla doğrudan hesaplanamaz. Doldurma söz konusu olduğundan, her satırın boyutunu 4 baytın katına yuvarlama etkisi gereklidir. Satırların uzunluğunu dört baytın katına çıkarmak için satırların sonuna doldurma baytları (zorunlu olarak 0 değil) eklenmelidir. Piksel dizisi belleğe yüklendiğinde, her satır 4'ün katı olan bir bellek adresinde başlamalıdır.

Görüntü aslında piksel dizisinin 32-bit DWORD gösterimi ile tanımlanır. Genellikle pikseller "aşağıdan yukarıya", sol alt köşeden başlayarak, soldan sağa giderek ve ardından görüntünün aşağıdan yukarıya doğru sıra sıra saklanır. Piksel formatları ve etkileri aşağıda listelenmiştir:

* Piksel başına 1 bit (1bpp) biçimi, 2 farklı rengi destekler (örneğin: siyah ve beyaz).
* Piksel başına 2 bit (2bpp) biçimi, 4 farklı rengi destekler ve 1 bayt başına 4 piksel depolar; en soldaki piksel en önemli iki bitte bulunur. Her piksel değeri, 4 renge kadar bir tablonun 2 bitlik bir indeksidir.
* Piksel başına 4 bit (4bpp) formatı, 16 farklı rengi destekler ve 1 bayt başına 2 piksel depolar; en soldaki piksel daha önemli yarım bayttadır. Her piksel değeri, 16 renge kadar bir tablonun 4 bitlik bir indeksidir.
* Piksel başına 8 bit (8bpp) biçimi, 256 farklı rengi destekler ve 1 bayt başına 1 piksel depolar. Her bayt, 256 renge kadar bir tablonun indeksidir.
* Piksel başına 16 bit (16bpp) biçimi, 65536 farklı rengi destekler ve 2 bayt WORD başına 1 piksel depolar. Her WORD, pikselin alfa, kırmızı, yeşil ve mavi örneklerini tanımlayabilir.
* 24 bit piksel (24bpp) biçimi, 16.777.216 farklı rengi destekler ve 3 bayt başına 1 piksel değeri depolar. Her piksel değeri, pikselin kırmızı, yeşil ve mavi örneklerini tanımlar (RGBAX gösteriminde 8.8.8.0.0). Spesifik olarak, sırayla: mavi, yeşil ve kırmızı (her örnek için 8 bit).
* Piksel başına 32 bit (32bpp) biçimi, 4.294.967.296 farklı rengi destekler ve 4 bayt DWORD başına 1 piksel depolar. Her DWORD, pikselin alfa, kırmızı, yeşil ve mavi örneklerini tanımlayabilir.

## Referanslar ##

* [Windows Meta Dosyası Formatı](http://msdn.microsoft.com/en-us/library/cc250370.aspx)
* [BMP Dosya Biçimi](https://en.wikipedia.org/wiki/BMP_file_format)

