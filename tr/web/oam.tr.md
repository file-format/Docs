{
  "date" : "2023-01-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OAM Dosyası - Adobe Edge Animate Widget Dosya Formatı",
  "description" :"OAM dosyasının ne olduğunu ve OAM dosyasını oluşturup açabilen API'leri öğrenin.",
  "linktitle" : "OAM",
  "menu" : {
    "docs" : {
      "identifier":"web-oam",
      "parent" : "web"
}
},
  "lastmod" : "2023-01-30"
}

## .OAM dosyası nedir?

Bir .oam dosyası, Adobe Edge Animate Widget'tan dışa aktarılan animasyonlu bir widget dosyasıdır. OAM widget dosyası formatı olarak dışa aktarılan animasyonlar, InDesign Belgeleri ([INDD dosyası](/tr/page-description-language/indd/), Dreamweaver ve Muse gibi diğer Adobe uygulamalarına eklenebilir. OAM dosyaları, kolayca oluşturulabilen dağıtım paketleri gibidir. yararlanmak için diğer Adobe projelerine eklenir. OAM dosyaları, animasyonun varlıkları, davranışları ve actionscript kodu hakkında bilgiler içerir. Bir Adobe Animate projesi yayınlayarak bir OAM dosyası oluşturabilirsiniz [.AN dosyası](/tr/web/an/) .
Kullanıcılar bir Edge Animate projesinden (.AN dosyası) yayınlayarak OAM dosyaları oluşturabilir.

## OAM Dosya Formatı

Bir OAM dosyası diske sıkıştırılmış [ZIP](/tr/compression/zip/) arşivi olarak kaydedilir. Bu, dosya uzantısını .zip olarak yeniden adlandırabileceğiniz ve WinZIP veya WinRAR gibi herhangi bir sıkıştırma yardımcı programıyla ayıklayabileceğiniz anlamına gelir. Küçültülmüş dosya boyutu, animasyonun internet üzerinden diğer kullanıcılarla aktarılmasını ve paylaşılmasını kolaylaştırır.

### OAM Dosya Yapısı

Bir .oam dosyasının dahili dosya yapısı özeldir ve Adobe tarafından kamuya açık olarak belgelenmez. Ancak .oam dosyalarının, tek bir dosya halinde paketlenmiş bir dizi dosya ve kaynak (grafik, ses ve ActionScript kodu gibi) içerdiği bilinmektedir. Bir .oam dosyasının içeriği, [XML](/tr/web/xml/) dosyalarını, SWF dosyalarını ve diğer kaynak dosyalarını içerebilir. .oam dosyasının tam yapısı, onu oluşturmak için kullanılan Adobe Animate sürümünün yanı sıra dosyada bulunan animasyon ve varlıkların türüne bağlıdır.

Bir OAM dosyası aşağıdaki bilgileri içerir.

`Varlıklar:` Animasyonda kullanılan grafikler, ses ve video öğeleri hakkında bilgiler.

`Davranışlar:` Animasyonda meydana gelen eylemlerin ve etkileşimlerin açıklamaları.

`ActionScript kodu:` Animasyonun davranışını ve etkileşimini kontrol etmek için kullanılan kod.

`Yayınlama ayarları:` Animasyonun yayınlanacağı platform ve format hakkında bilgiler (HTML5 veya AIR gibi).

`Meta veriler:` Animasyonun yazarı, oluşturulma tarihi ve sürüm numarası gibi ek bilgiler.

## OAM Dosyası Nasıl Açılır?

OAM dosyalarını açmak için aşağıdaki uygulamaları kullanabilirsiniz.

* Adobe Edge Animate CC (Üretilmiyor)
*Adobe Animate 2023
* Adobe InDesign 2023
*Adobe Dreamweaver 2021

## Referanslar

* [OAM Yayınlama](https://helpx.adobe.com/animate/using/OAM-publishing.html)

