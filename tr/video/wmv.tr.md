{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WMV Dosya Biçimi",
  "description":"WMV dosya formatı ve WMV dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "WMV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2019-09-16"
}

## WMV dosyası nedir?

Advanced Systems Format (ASF), öncelikle medya akışlarını depolamak ve iletmek için tasarlanmış bir dijital multimedya kabıdır. Microsoft Windows Media Video (WMV) sıkıştırılmış video biçimidir ve Microsoft Windows Media Audio (WMA), Microsoft tarafından geliştirilen ASF kapsayıcısındaki ek meta verilerle birlikte sıkıştırılmış ses biçimidir. WMV veya WMA dosyaları, Windows Media Video ve Windows Media Audio kodekleri ile kodlandıktan sonra .asf uzantılı olarak temsil edilirler. WMV, videonun kalitesini korurken bir ağ üzerinden daha iyi aktarım hızı için büyük dosyaları sıkıştırır. WMV, tüm Windows cihazlarında çalışacak şekilde özel olarak tasarlanmıştır. Sinema ve Televizyon Mühendisleri Derneği (SMPTE) tarafından standardizasyondan sonra, WMV artık açık standart bir format olarak kabul edilmektedir.

## Tarih ##

Microsoft'a ait codec bileşenlerinin yardımıyla, 1999'da MPEG-4 Bölüm 2'ye dayanan WMV7 olarak bilinen yeni sıkıştırılmış video formatı geliştirildi. Diğer iki sürümde, yani WMV8 ve 9'da iyileştirmeler eklendi. Microsoft, 9^^th^^ sürümünü sundu 2003'te standardizasyon için WMV'den SMPTE'ye geçiş ve sonunda 2006'da VC-1 olarak da bilinen SMPTE 421M olarak standartlaştırıldı. WMV'nin arkasındaki fikir, Microsoft tarafından desteklenen tüm donanım ve yazılımlar tarafından desteklenebilecek bir medya formatı geliştirmekti. Ayrıca bir diğer önemli amaç da video akışlarını internet üzerinden en uygun senaryoda iletmekti. SMPTE standardizasyonundan sonra WMV ayrıca Blu-ray diskler için bir video formatı haline geldi.

## Dosya Biçimi Özellikleri

### Konteyner

Genellikle, WMV bir ASF kapsayıcısına paketlenir, ancak buna ek olarak, Matroska veya AVI kapsayıcısı da onu sırasıyla .mkv ve .avi uzantılarıyla destekleyebilir.

### Windows Medya Videosu 9

Windows Media Video 9 serisinde dijital ortamın yazılması ve oynatılması için çeşitli ses ve video codec'leri bulunsa da, WMV-9 codec'i çok düşük bit hızlarından, yani 160 x'ten optimum sıkıştırmayı elde edebildiği için en yeni ve en iyi video codec'idir. Çeşitli HD videolar için 10 Kbps'de 120'den 4-8 Mbps'de 1920 x 1080'e.

### Codec'in Yapısı

WMV-9, 8 bit 4:2:0 dahili renk formatına sahiptir. Diğer tüm popüler video sıkıştırma standartları MPEG-1 ve H.261 gibi, WMV-9 da blok tabanlı bir hareket telafisi ve uzamsal dönüştürme şeması kullanır. Genel olarak, bu standartların uzaysal yer değiştirmeyi işaret etmek için hareket vektörü (MV) adı verilen 2 boyutlu bir nicelik yardımıyla önceki yeniden oluşturulmuş çerçeveden blok blok hareket telafisi gerçekleştirdiğini söyleyebiliriz. Mevcut blok, hareket vektörü tarafından mevcut konumundan kaydırılan aynı boyuttaki önceden yeniden oluşturulmuş çerçeveden değerlerin tahmin edilmesi yardımıyla oluşturulur. Sonunda, artık hata, hareket dengelemeli tahmin edilen blok ile gerçek blok arasındaki fark olarak hesaplanır. Bu artık hata, doğrusal bir enerji sıkıştırma dönüşümü kullanılarak dönüştürülür, ardından nicemlenir ve entropi kodlanır.

Kuantize dönüşüm katsayıları, kod çözücü tarafında kalan hatanın bir yaklaşıkını üretmek için entropi kodu çözülür, niceliği çözülür ve ters dönüştürülür; bu daha sonra yeniden yapılandırmayı oluşturmak için hareket telafili tahmine eklenir. Codec'in üst düzey açıklaması aşağıdaki resimde gösterilmektedir.

Bölümün geri kalanında, WMV-9'u MPEG standartları gibi video kodlama çözümlerinin geri kalanından ayıran yeni geliştirmeler tartışılacaktır. WMV-9, intra (I), tahmin edilen (P) ve çift yönlü tahmin edilen (B) çerçevelere sahiptir. İç çerçeveler, bağımsız olarak kodlanan ve diğer çerçevelere bağımlılığı olmayan çerçevelerdir. Öngörülen çerçeveler, geçmişte bir çerçeveye bağlı olan çerçevelerdir. Öngörülen bir çerçevenin kodunun çözülmesi, yalnızca en son (I) çerçeveden başlayarak geçerli çerçeveden önceki tüm referans çerçevelerinin kodu çözüldükten sonra gerçekleşebilir. B çerçeveleri, iki referansı olan çerçevelerdir - biri zamansal geçmişte ve diğeri zamansal gelecekte. B çerçeveleri, referanslarından sonra iletilir; bu, B çerçevelerinin, kod çözme sırasında referanslarının mevcut olmasını sağlamak için sıra dışı gönderildiği anlamına gelir. WMV-9'daki B çerçeveleri, sonraki çerçeveler için referans olarak kullanılmaz. Bu, B karelerini kod çözme döngüsünün dışına yerleştirerek, B karelerinin kodunun çözülmesi sırasında sürüklenme veya uzun vadeli görsel eserler olmadan kısayolların alınmasına izin verir. I, P ve B çerçevelerinin yukarıdaki tanımı, hem aşamalı hem de taramalı diziler için geçerlidir.

Video codec bileşenlerinin performansı, oran-bozulma (RD) grafiğiyle karşılaştırılır. Belirli bir bit hızında sıkıştırmanın ürettiği bozulmayı gösteren 2 boyutlu bir eğridir.

WMV-9, aşağıda listelenen çeşitli tekniklerin tanıtılmasıyla bu sorunu ele almıştır:

1. Uyarlanabilir blok boyutu dönüşümü

2. Sınırlı hassas dönüşüm seti

3. Hareket telafisi

4. Kuantizasyon ve dekuantizasyon

5. Gelişmiş entropi kodlaması

6. Döngü filtreleme

7. Gelişmiş B çerçeve kodlaması

8. Geçmeli kodlama

9. Örtüşen yumuşatma

10. Düşük oranlı araçlar

11. Solma telafisi

## Referanslar ##

* [https://bytescout.com/blog/2014/10/windows-media-video-format.html](https://bytescout.com/blog/2014/10/windows-media-video-format.html )
* [https://en.wikipedia.org/wiki/Windows_Media_Video](https://en.wikipedia.org/wiki/Windows_Media_Video)


