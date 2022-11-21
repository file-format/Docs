{
  "date" : "2022-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M4S Dosyası - M4S dosyası nedir?",
  "description":"M4S dosya formatı ve M4S dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "M4S",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2022-07-18"
}

## M4S dosyası nedir?

Bir M4S dosyası, **MPEG-DASH** akış tekniği kullanılarak internet üzerinden yayınlanan bir videonun küçük bir bölümüdür. İkili veri biçiminde bir video bölümü içerir. Alıcı uygulama (genellikle bir web tarayıcısı veya medya oynatıcılar) bu bölümleri alındıkları sırayla oynatır. İlk M4S segmenti, içerdiği başlatma verileriyle tanımlanır. **Özette**, M4S dosyaları tam bir dosyanın küçük bağımsız medya bölümleridir.

## M4S Dosya Biçimi

M4S dosyaları [ISO Base Media File (ISOBMFF) formatına](https://www.w3.org/TR/mse-byte-stream-format-isobmff/) dayalıdır. Büyük bir dosyanın bu küçük bölümleri bağımsız olarak HTTP üzerinden indirilebilir. Bu nedenle, büyük bir [MP4](/tr/video/mp4/) film dosyanız varsa, MPEG-DASH (HTTP üzerinden Dinamik Uyarlamalı Akış) tekniği kullanılarak M4S segment dosyaları olarak bölümlere ayrılarak akışa alınabilir. Bu büyük film dosyası M4S olarak diske indirilirse birden fazla M4S dosyası indirilir. Tüm bu .m4s segmentleri birleştirilirse eksiksiz bir oynatılabilir dosya üretilir. Medya yürütücüler, dosyayla birlikte ilk başlatma bölümü de mevcut olmadığı sürece dosyayı oynatamaz.

## MPEG-DASH Akışı Hakkında

MPEG-DASH, internet üzerinden yüksek kaliteli medya içeriğinin akışını mümkün kılan uyarlanabilir bit hızı akış tekniğini kullanır. Bu, içeriği HTTP üzerinden akışa alınan bir dizi küçük parçaya bölerek yapılır. Film, podcast'ler veya bir spor etkinliğinin canlı yayını gibi büyük medya dosyalarının akışı bu şekilde gerçekleştirilebilir. Bu segmentler farklı bit hızlarında kodlanmıştır. MPEG-DASH özellikli ortam yürütücüler, bir bit hızı uyarlama algoritması kullanarak en yüksek bit hızına sahip bölümü otomatik olarak seçer. Bu, oynatma sırasında olayların durdurulmasını veya yeniden arabelleğe alınmasını önler.

### M4S dosyaları için Açık Kaynak API'si

M4S dosyalarını okumak ve dönüştürmek için kullanılabilecek açık kaynaklı API'ler mevcuttur.

* [libdash](https://github.com/bitmovin/libdash) - M4S dosyaları için .NET API'si
* [dash.js](https://github.com/Dash-Industry-Forum/dash.js) - M4S dosyası için Javascript istemcisi
* [Dash Dosyaları oluşturmak için Kitaplığa gidin](https://github.com/zencoder/go-dash)

### M4S'yi MP4'e Dönüştürmek için Açık Kaynak API'si

* [MFourStoMp4](https://github.com/muri11o/mfourstomp4)

## Referanslar ###

* [ISO Temel Medya Dosyası (ISOBMFF) formatı](https://www.w3.org/TR/mse-byte-stream-format-isobmff/)
* [HTTP Üzerinden Dinamik Uyarlanabilir Akış - MPEG-DASH](https://en.wikipedia.org/wiki/Dynamic_Adaptive_Streaming_over_HTTP)

