{
  "date" : "2019-10-11",
  "keywords" :[ "exif dosyası", "exif dosya biçimi", "exif dosyası nedir", "dosya", "exif örneği", "exif dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EXIF",
  "description":"EXIF dosya formatı ve EXIF dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "EXIF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## EXIF dosyası nedir?
EXIF, ilk olarak 1985 yılında [Japan Camera Industry Association](https://en.wikipedia.org/wiki/Japan_Electronic_Industries_Development_Association) (JCIA) tarafından verilen tanım olan "Değiştirilebilir Görüntü Dosyası Formatı" anlamına gelir. Standart, Japan Electronics ve Bilgi Teknolojileri Endüstrileri Derneği (JEITA) bugün itibariyle. EXIF, esas olarak dijital kameralar ve tarayıcılar tarafından kullanılan görüntü ve ses formatlarının özellikleri için bir standarttır.

EXIF standardı, görüntü dosyasıyla birlikte etiketleme ve meta veri bilgilerini içerir. Meta veriler kamera modeli, deklanşör hızı, Tarih ve saat, diyafram, üretici, pozlama süresi, X çözünürlüğü, Y çözünürlüğü vb. gibi bilgileri içerebilir. Normalde EXIF verileri varsayılan olarak gizlidir. EXIF verilerini görüntülemek için, resim görüntüleme uygulamasında görünüm özelliklerini seçmek gerekir. Exif meta verileri, tek bir resim dosyasında teknik ve birincil resim verileriyle birlikte küçük resimler de içerebilir.

## Geçmiş ve Sürümler ##

* Ekim 1995'te JEIDA, Sürüm 1'i oluşturdu. Bu sürümde JEIDA, görüntü veri formatı ve öznitelik bilgileri ile temel etiketlerden oluşan yapıyı tanımladı.
* Kasım 1997, sürüm 1.1, sürüm 1'deki etiketlerin çoğuyla tanıtıldı, ancak isteğe bağlı öznitelik bilgileri ve biçim işlemi için hükümler de eklendi.
* Haziran 1998, sRGB renk alanı, sıkıştırılmış küçük resimler ve ses dosyaları içeren Sürüm 2.
* Aralık 1998, Sürüm 2.1, gelişmiş depolama ve öznitelik bilgileri ile.
* Şubat 2002, Sürüm 2.2, geliştirilmiş sürüm 2.1, baskı bitirme özelliği eklendi.
* Eylül 2003, Adobe RGB olarak bilinen isteğe bağlı renk alanıyla Sürüm 2.21.

## EXIF Dosya Biçimi

EXIF, belirli meta verilerin eklenmesiyle aşağıdaki dosya biçimlerini kullanır.

1. [JPEG](/tr/image/jpeg/) - sıkıştırılmış görüntü dosyaları için ayrık kosinüs dönüşümü (DCT).
1. Sıkıştırılmamış görüntü dosyaları için [TIFF](/tr/image/tiff/) Rev. 6.0 (RGB veya YCbCr).
1. Ses dosyaları için [RIFF](https://en.wikipedia.org/wiki/Resource_Interchange_File_Format) [WAV](https://en.wikipedia.org/wiki/WAV) (Doğrusal [PCM](https:/) /en.wikipedia.org/wiki/Pulse-code_modulation) veya ITU-T [G.711](https://en.wikipedia.org/wiki/G.711) sıkıştırılmamış ses verileri için μ-Law PCM ve [ IMA](https://en.wikipedia.org/wiki/Interactive_Multimedia_Association)-[ADPCM](https://en.wikipedia.org/wiki/ADPCM) sıkıştırılmış ses verileri için).

### EXIF tarafından kullanılan işaretçi ###

0xFFE0~~0xFFEF işareti, kullanıcı uygulaması tarafından kullanılan "Uygulama İşareti"dir. Örneğin, eski dijital kameralar görüntüleri depolamak için JFIF (JPEG Dosya Değişim Formatı) kullanır. JFIF, dijital kamera yapılandırma verilerini ve küçük resim görüntüsünü eklemek için APP0 (0xFFE0) İşaretçisini kullanır. Ayrıca EXIF, veri eklemek için bir Uygulama İşaretleyicisi kullanır, ancak EXIF, JFIF formatıyla bir çakışmayı önlemek için APP1 (0xFFE1) İşaretçisini kullanır. Her EXIF dosya formatı bu formattan başlar.


|SOI İşareti|APP1 İşareti|APP1 Verileri|Diğer İşaretçi
---|---|---|---|
|FFD8|FFE1|SSSS 457869660000 TTTT......|FFXX SSSS DDDD......

SOI (0xFFD8) İşaretçisinden başlar, dolayısıyla bir JPEG dosyasıdır. Ardından hemen APP1 Marker gelir. EXIF'in tüm verileri bu APP1 veri alanında saklanır. Üst tablodaki "SSSS" kısmı, APP1 veri alanının (EXIF veri alanı) boyutunu ifade eder. Lütfen "SSSS" boyutunun tanımlayıcı boyutunu da içerdiğine dikkat edin. "SSSS" den sonra APP1 verileri başlar. Birinci kısım, EXIF olup olmadığının tespiti için özel bir veri olup, ASCII karakteri "EXIF" ve 2 byte 0x00 kullanılmıştır. APP1 İşaretçisi alanından sonra diğer JPEG İşaretçileri gelir.

### Exif Veri Yapısı ###

EXIF verilerinin (APP1) kaba bir yapısı aşağıda gösterilmiştir. Yukarıda tartışıldığı gibi, EXIF verileri ASCII karakteri "EXIF" ve 2 bayt 0x00 ile başlar, ardından EXIF verileri gelir. EXIF, verileri depolamak için TIFF biçimini kullanır.


|FFE1|APP1 İşaretçisi
---|---|
|SSSS|APP1 Verileri|APP1 Veri Boyutu
|45786966 0000|Exif Başlığı
|49492A00 08000000|TIFF Başlığı
|XXXX. . . .|IFD0 (ana resim)|Dizin
|LLLLLLLL|IFD1 bağlantısı
|XXXX. . . .|IFD0'ın veri alanı
|XXXX. . . .|Exif AltIFD|Dizini
|00000000|Bağlantı Sonu
|XXXX. . . .|Exif SubIFD'nin veri alanı
|XXXX. . . .|IFD1(küçük resim)|Dizin
|00000000|Bağlantı Sonu
|XXXX. . . .|IFD1'in veri alanı
|FFD8XXXX. . . XXXXFFD9|Küçük resim

#### TIFF Başlığı ####

8 baytlık [TIFF](/tr/image/tiff/) dosya başlığı aşağıdaki bilgileri içerir:

`Bayt 0-1:` Dosya içinde kullanılan bayt sırası. Yasal değerler:“II”(4949.H)“MM” (4D4D.H).

"II" formatında bayt sırası, hem 16 bit hem de 32 bit tamsayılar için her zaman en önemsiz bayttan en önemli bayta doğrudur. Buna, küçük endian bayt sırası denir. "MM" biçiminde bayt sırası, hem 16 bit hem de 32 bit tamsayılar için her zaman en önemliden en önemsize doğrudur. Buna big-endian bayt sırası denir.

`Bayt 2-3:` Dosyayı ayrıca bir TIFF dosyası olarak tanımlayan gelişigüzel ancak dikkatle seçilmiş bir sayı (42). Bayt sırası, Bayt 0-1 değerine bağlıdır.

`Bayt 4-7:` İlk IFD'nin ofseti (bayt olarak). Dizin, başlıktan sonra dosyada herhangi bir yerde olabilir, ancak bir sözcük sınırında başlamalıdır. Özellikle bir Görüntü Dosyası Dizini, tanımladığı görüntü verilerini takip edebilir. Okuyucular işaretçileri nereye götürürlerse götürsünler takip etmelidir. Bayt ofseti terimi bu belgede her zaman TIFF dosyasının başlangıcına göre bir konumu belirtmek için kullanılmıştır. Dosyanın ilk baytının ofseti 0'dır.

#### Görüntü Dosyası Dizini ####

Bir IFD, gerçek görüntü verilerine yönelik işaretçilerin yanı sıra görüntü hakkında bilgi içerir. 2 baytlık dizin girişlerinin sayısından (yani alan sayısından) ve ardından 12 baytlık alan girişlerinden oluşur. , ardından bir sonraki IFD'nin 4 baytlık ofseti (veya yoksa 0). Bir TIFF dosyasında en az 1 IFD olmalı ve her IFD'de en az bir giriş bulunmalıdır.

##### IFD Girişi #####

Her 12 baytlık IFD Girişi aşağıdaki formattadır.


|Bayt|Açıklama
---|---|
|0-1|Alanı tanımlayan Etiket
|2-3|Alan türü
|4-7|Belirtilen türün sayısı
|8-11|Değer Uzaklığı, alanın Değerinin dosya ofseti (bayt olarak). Değerin bir sözcük sınırında başlaması beklenir; dolayısıyla karşılık gelen Değer Ofseti bir çift sayı olacaktır. Bu dosya ofseti, görüntü verisinden sonra bile dosyada herhangi bir yeri gösterebilir.

TIFF alanı, TIFF etiketi ve değerinden oluşan mantıksal bir varlıktır. Bu mantıksal konsept, bir IFD Girişi ve değer/ofset kısmına uymuyorsa gerçek değer, IFD Girişinin son 4 baytı olarak uygulanır. TIFF alanı ve IFD girişi terimleri çoğu bağlamda birbirinin yerine kullanılabilir.

#### Küçük Resim ####

Exif biçimi görüntünün küçük resmini içerir (Ricoh RDC-300Z hariç). Genellikle IFD1'in yanında bulunur. Küçük resimler için 3 biçim vardır; JPEG formatı(JPEG, YCbCr kullanır), RGB TIFF formatı, YCbCr TIFF formatı.

##### JPEG Formatında Küçük Resim #####

IFD1'deki Sıkıştırma(0x0103) Etiketinin değeri '6' ise, küçük resim formatı JPEG'dir. Exif görüntüsünün çoğu, küçük resim için JPEG formatını kullanır. Bu durumda, küçük resmin ofsetini IFD1'de JpegIFOffset(0x0201) Etiketi ile, küçük resmin boyutunu JpegIFByteCount(0x0202) Etiketi ile alabilirsiniz. Veri formatı, sıradan JPEG formatıdır, 0xFFD8'den başlar ve 0xFFD9 ile biter. Görünüşe göre JPEG formatı ve 160x120 piksel boyutu, Exif2.1 veya sonrası için önerilen küçük resim formatı.

##### TIFF Biçimi Küçük Resmi #####

IFD1'deki Sıkıştırma(0x0103) Etiketinin değeri '1' ise, küçük resim formatı sıkıştırma değildir (TIFF görüntüsü olarak adlandırılır). Küçük resim verilerinin başlangıç noktası StripOffset(0x0111) Etiketidir, küçük resim boyutu, StripByteCounts(0x0117) Etiketinin toplamıdır.

## Referanslar ##

* [EXIF - Wikipedia'dan](https://en.wikipedia.org/wiki/Exif)
* [EXIF Dosya Biçimi](https://www.media.mit.edu/pia/Research/deepview/exif.html)

