{
  "date" : "2021-07-29",
  "keywords" :[ "pes dosyası", "pes dosya biçimi", "pes dosyası nedir", "dosya", "pes örneği", "pes dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PES Dosya Formatı - Brother PE Nakış Formatı",
  "description":"PES dosya formatı ve PES dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "PES",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2021-07-29"
}

## PES Nakış dosyası nedir?

PES nakış dosyası, nakış/dikiş makineleri için talimatları içeren bir tasarım dosyasıdır. Brother Industries tarafından nakış makineleri için geliştirildi, ancak daha sonra genel dosya formatı olarak resmileştirildi. PES dosyaları, dikiş makineleri tarafından kumaş üzerine desen dikme talimatlarını okumak için kullanılır. Bu dosyalar iki amaca hizmet eder; ilk olarak Brother Industries tarafından geliştirilen PE-Design uygulaması için tasarım bilgisi sağlar ve ikincisi, tasarım adı, renkleri ve "durdur", "atla" ve "kırp" gibi nakış makinesi kodlarını sağlar.

## PES Dosya Biçimi - Daha Fazla Bilgi

Bir PES dosyası, ikili dosya biçiminde diske kaydedilir. Önceden tanımlanmış yöntem kullanılarak saklanan dikiş bilgilerine sahip birden çok bölüm içerir. PES dosya formatı aşağıdaki gibidir.

* Sürüm Verileri - Sürüm bilgilerini verir ve herhangi bir değer olabilir: `#PES0001`, `#PES0020`, `#PES0030`, `#PES0040`, `#PES0050`, `#PES0055`, `#PES0060`
* PEC Arama Değeri - Sürüm verilerini hemen takip eden ve tasarım ayrıntılarını içeren PEC bölümü için arama değerini temsil eden 4 baytlık bir küçük endian tamsayı Bilgi
* PSE Bölümü - Brother PE-Design ile ilgili tasarım bilgilerini içerir ve diğer dikiş uygulamaları olabilir
* PCE Bölümü - PSE dosyasında herhangi bir yerde olabilir, ancak PEC Arama Değeri tarafından referans verilir.

## PES Dosyası Kullanan Dikiş Makinalarının Türü

PES dosyaları öncelikle Brother dikiş makinelerinde kullanılan PE-Design Yazılımı tarafından oluşturulur. PES dosyalarını destekleyebilecek diğer bazı makineler, Babylock ve Bernina ev nakış makinelerini içerir.

## PSE Dosyaları Nasıl Dönüştürülür?

PE-Design yazılım uygulaması [PSE dosyasını dönüştürebilir](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/11_1088392?hl) =pes+dosya) .pes, .dst, .exp, .pcs, .hus, .vip, .shv, .jef, .sew, .csd veya .xxx gibi diğer biçimlere. Dosyayı açıp Dönüştürme biçimini seçerek PE-Design uygulaması kullanılarak yapılabilir.

## Referanslar

* [PE Tasarımı - Talimat Kılavuzu](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/)

