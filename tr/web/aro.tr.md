{
  "date" : "2021-12-09",
  "keywords" :[ "aro",".aro dosyası", "aro dosya formatı", "bir dosya türü", "dosya", "tür", ".aro dosyası nedir" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ARO Dosya Formatı - SteelArrow Web Uygulama Dosyası",
  "description" :"ARO dosyasının ne olduğu ve ARO dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "ARO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-12-09"
}

## ARO dosyası nedir?

Bir ARO dosyası, SteelArrow Web Uygulaması ile oluşturulan bir sunucu tarafı web sayfası dosyasıdır. [HTML](/tr/web/html/) ve SteelArrow etiketlerini ve komut dosyalarını içerir. Bunlar, kullanıcının tarayıcısına gönderilmeden önce eksiksiz yanıt sayfası oluşturmak için sunucuda yürütülür. ARO dosyaları, HTML içeriğinin neredeyse %95'ini içerirken geri kalanı SteelArrow kodundan oluşur. ARO dosyalarının işinize yaraması için, SteelArrow Web Uygulamaları sunucusunun web sunucusu makinesinde kurulu ve çalışır durumda olması gerekir.

## ARO Dosya Biçimi

ARO dosyaları, gömülü JavaScript kodu ve Java uygulamaları içeren HTML biçimlendirme dili dosyasında yazılır. [SteelArrow etiketleri](http://www.steelarrow.com/docs/basics1.aro), web sayfalarının geliştirilmesi için temel yapı taşlarıdır. Bunlar sayfanın görüntüsünü değiştirmese de sayfayı verilerle doldurmak için kullanılır. Ek olarak, koşullu ifadelerle çıktıyı kontrol etmek için de kullanılabilirler.

### ARO Etiketi Örneği

bu<SAOUTPUT> ARO etiketi, geliştiricilerin bir komut dosyası içindeki herhangi bir yerde veri değerlerinin çıktısını almasını sağlar. Örneğin PARAM tablosunun çıktısını almak için kullanılabilir.<SAOUTPUT VALUE=PARAM[]> HTML içinde görüntülenebilen<BODY> etiket.

## Referanslar

* [SteelArrow etiketleri](http://www.steelarrow.com/docs/basics.aro)

