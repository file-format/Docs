{
  "date" : "2021-02-15",
  "keywords" :[ "vp6 dosyası", "vp6 dosya biçimi", "vp6 dosyası nedir", "dosya", "vp6 örneği", "vp6 dosya uzantısı","uzantı", "biçim" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VP6 - TrueMotion Video Dosyası",
  "description":"VP6 dosya formatı ve VP6 dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "VP6",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## VP6 dosyası nedir?

VP6, Mayıs 2003'te On2 teknolojileri tarafından tanıtılan kayıplı bir sıkıştırma video formatıdır. V3, V4 ve V5 dahil olmak üzere TrueMotion tarafından geliştirilen video codec serisinin bir parçasıdır. Format, BBC raporları ve QuickLink yazılımı gibi yayın alanında kısa süre kullanıldı. VP6'nın yerini Ocak 2005'te daha iyi sıkıştırma uyumluluğu ile VP7 Codec aldı.

## VP6 Dosya Biçimi

V6 dosyaları için tam özellikler herkese açık değildir. On2, özellikleri başlangıçta herkese açık hale getirdi, ancak kısa süre sonra bunlar genel kullanıcılar için kullanılamaz hale getirildi. VP6 dosya biçiminin resmi olmayan bir belgesi, geliştiricinin referansı için başvurulabilecek [multimedia wiki](https://wiki.multimedia.cx/index.php?title=On2_VP6) adresinde mevcuttur.

### Makrobloklar (MB)

MPEG-2, MPEG-4 bölüm 2 ve 10'a benzer şekilde, bir VP6 dosyasının her video karesi 16x16 makroblok (MB) dizisinden oluşur. Her MB aşağıdaki modlardan birinde olabilir:

* MB içi
* Inter MB, boş MV, önceki çerçeve referansı
* Inter MB, diferansiyel MV, önceki çerçeve referansı
* Inter MB, dört MV, önceki çerçeve referansı
* Inter MB, MV 1, önceki çerçeve referansı
* Inter MB, MV 2, önceki çerçeve referansı
* Inter MB, boş MV, yer imli çerçeve referansı
* Inter MB, diferansiyel MV, işaretli çerçeve referansı
* Inter MB, MV 1, yer imli çerçeve referansı
* Inter MB, MV 2, yer imli çerçeve referansı

### Çerçeve Başlığı

Bir VP6'nın çerçeve başlığı, big-endian bit paketlemesini izleyen aşağıda gösterildiği gibidir.

|Sözdizimi|Bit sayısı|Tür|Symantecs|
---|---|---|---|
|frame_mode|1|Enum|0x0 bir çerçeve içi anlamına gelir|
|qp |6 |İmzasız |Kuantizasyon parametresi geçerli aralık 0..63|
|işaret| 1| Sabit| 0=VP61/62, 1=VP60|
|if (çerçeve_modu == 0) { | 0 | |INTRA_FRAME'e eşittir|
|versiyon |5| Sabit| 6=VP60/61, 7=VP60(Elektronik Sanatlar), 8=VP62|
|versiyon2 |2| Sabit |0=VP60, 3=VP61/62|
|geçişmeli |1| Boolean |true (1), geçmeli kullanılacağı anlamına gelir|
|if (işaretçi==1 veya sürüm2==0) {||||
|ofset |16 |İmzasız| ikincil arabellek ofseti (arabelleğin başlangıcına göre bayt)|
|}||||
|dim_y |8| imzasız| Videonun makroblok yüksekliği|
|dim_x |8| imzasız| Videonun makroblok genişliği |
|render_y |8 |İmzasız |Videonun yüksekliği göster|
|render_x |8 |İmzasız |Video genişliğini göster|
|}başka{||||
|if (işaretçi==1 veya sürüm2==0) {||||
|offset |16 |İmzasız |İkincil arabellek ofseti (arabelleğin başlangıcına göre bayt)|
|}||||
|}||||

## Referanslar

* [VP6 Wikipedia](https://en.wikipedia.org/wiki/VP6#:~:text=On2%20TrueMotion%20VP6%20is%20a,Video%2C%20and%20JavaFX%20media%20files.)

