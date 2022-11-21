{
  "date" : "2019-10-11",
  "keywords" :[ "b6z dosyası", "b6z dosya formatı", "b6z dosyası nedir", "dosya", "b6z örneği", "b6z dosya uzantısı","uzantı", "biçim" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"B6Z - B6ZIP Arşiv Dosya Formatı",
  "description":"B6Z dosya formatı ve B6Z dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "B6Z",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-05"
}

## B6Z dosyası nedir?

.b6z uzantılı bir dosya, dosyaları sıkıştırmak ve açmak için kullanılan macOS yazılım uygulaması [B6Zip](http://b6zip.com) tarafından oluşturulan sıkıştırılmış bir arşiv dosyasıdır. Daha yüksek sıkıştırma oranı sağlayan nispeten yeni bir arşiv formatıdır. B6Z açık mimariye sahiptir ve 900.000 PB'a kadar dosya boyutlarını destekler. Veri sıkıştırmayı, hata kurtarmayı ve dosya genişletmeyi destekler. B6Zip yardımcı yazılımı, B6Z dahil olmak üzere farklı türde sıkıştırılmış dosyaları açmak için MacOS'ta ücretsiz olarak mevcuttur.

## B6Z Dosya Formatı

B6Z dosya formatı açık mimariye dayalıdır ve AES-256 şifreleme algoritması ile sağlam sıkıştırma sağlar. Varsayılan sıkıştırma yöntemi olarak LZMA2'yi kullanır, ancak aşağıdaki gibi diğer sıkıştırma yöntemlerini de destekler.

|Yöntem|Açıklama|
---|---|
|LZMA |LZ77 algoritmasının optimize edilmiş versiyonu|
|LZMA2| LZMA'nın geliştirilmiş versiyonu |
|Söndür| Düzenli LZ77 algoritması|
|BZip2| Standart BWT algoritması|
|PPMD| Dmitry Shkarin'in PPMdH|

B6Zip yardımcı programı, tüm bu sıkıştırma standartlarını destekler ve yüksek hız sağlayacak şekilde yüksek oranda optimize edilmiştir. [ZIP](/tr/compression/zip/), [TAR](/tr/compression/tar/) ve [RAR](/tr/compression/rar/) dosya formatlarıyla çalışmayı destekler. B6Z dosyalarında MIME tipi uygulama/x-b6z-sıkıştırılmış bulunur.

## Referanslar

* [B6Zip](http://b6zip.com)

