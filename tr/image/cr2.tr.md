{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CR2 Dosya Biçimi - Canon Raw 2 Görüntü Dosyası",
  "description":"CR2 dosya formatı ve CR2 dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "CR2",
  "menu" : {
    "docs" : {
      "identifier":"image-cr2",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## CR2 dosyası nedir?

CR2 (Camera RAW 2) dosyası, Canon dijital fotoğraf makineleri tarafından oluşturulan bir RAW görüntü dosyasıdır. Kamera tarafından yakalanan orijinal, işlenmemiş kayıpsız görüntü verilerini depolar. CR2 dosya formatı, Canon tarafından dijital kameraları için geliştirilmiştir ve 14 bit RGB'ye kadar yüksek kaliteli görüntüler kaydedebilir. Bu, yeterli son işleme alanıyla birlikte yüksek kaliteli görüntüler üretir. CR2 görüntü formatı Canon tarafından 350D, 20D ve 1D kamera modellerinde kullanılmıştır. CR2 dosyaları RAW dosyalarıdır ve kamera bilgileri, lens bilgileri, basamaklama bilgileri, beyaz dengesi ve diğer ayarlar gibi ek meta veri bilgileri içerir.

## CR2 Dosya Biçimi

CR2 dosyaları, kamera hafıza kartında Canon'a özel dosya biçiminde ikili dosyalar olarak depolanır. CR2 dosya formatı başlangıçta kullanılan CRW dosya formatının yerini aldı ve daha sonra Canon RAW 3 dosya formatının yerini aldı. CR2 dosya biçimi, 4 Görüntü Dosyası Dizinine (IFD'ler) sahip [TIFF](/tr/image/tiff/) belirtimlerine dayalıdır.

|Ofset |İçerik |Yorum|
---|---|---|
|0x0000 |Başlık |bayt sıralamasını, sürümü ve RAW resmine uzaklığı içerir|
|computed |IFD#0 |bu bölüm, Makernotes bölümünü içeren Exif bölümünü içerir.
resim#0| hakkında bilgi
|bilgisayarlı |resim#0 |resmin küçük versiyonu (orijinalin dörtte biri boyutunda), Jpeg formatında sıkıştırılmış|
|bilgisayarlı |IFD#1 |Resim#1 hakkında bilgi.|
|bilgisayarlı |resim#1 |resmin küçük versiyonu, Jpeg formatında sıkıştırılmış|
|bilgisayarlı |IFD#2 |Resim#2 hakkında bilgi.|
|bilgisayarlı |resim#2 |resmin küçük versiyonu, sıkıştırılmamış|
|başlıkta| IFD#3| Resim#3 hakkında bilgi, tam boyutlu RAW resim|
|bilgisayarlı |resim#3 |RAW görüntü verileri, kayıpsız Jpeg formatında sıkıştırılmış (RGB verileri değil!)|

## CR2 Dosya Biçiminin Avantajı

Resimlerin RAW formatında saklanması, Beyaz Dengesi ayarı gibi fotoğrafta birçok sonradan işlemeye izin verir. Bu, [JPEG](/tr/image/jpeg/) gibi diğer resim dosyası formatlarında çok daha zordur ve büyük bir kalite kaybına neden olur.

## CR2, JPEG'den daha mı iyi?

CR2 dosyaları, herhangi bir veri kaybı olmayan ve dolayısıyla kalite kaybı olmayan ham dosyalardır. Öte yandan JPEG, dosyayı küçültmek için bazı verileri kaybettiği için kayıplı görüntü dosyası biçimidir. Bu nedenle, CR2 dosyalarının kalitesi yüksektir ve rötuş ve geliştirmeler için daha uygundur.

## Referanslar

* [CR2 Dosya Biçimi](http://lclevy.free.fr/cr2/)

