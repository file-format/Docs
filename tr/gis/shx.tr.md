{
  "date" : "2021-07-29",
  "keywords" :[ "shx dosyası", "shx dosya biçimi", "shx dosyası nedir", "dosya", "shx örneği", "shx dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHX - Shapefile Şekil Dizin Biçimi",
  "description":"SHX dosya formatı ve SHX dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "SHX",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-29"
}

## SHX dosyası nedir?
SHX dosyası, hızlı bir şekilde ileri ve geri aramayı sağlamak için özellik geometrisinin konumsal bir indeksi olan şekil indeksi formatına aittir. SHX, doğrudan erişim ofset dosyasıdır. Bu dosyada veri yok, sadece ilk yüz baytın kopyası, kayıt numarası ve shp'deki o kaydın başlangıç baytına mahsup var. Lütfen .shx uzantılı dosyanın [SHP](/tr/gis/shp/) ve [DBF](/tr/database/dbf/)'yi bağlamadığına dikkat edin.

## SHX dosya formatı
SHX biçimi, özellik geometrisinin konumsal dizinini ve SHP dosyasına benzer 100 baytlık başlığı ve ardından aşağıdaki iki alanı içeren herhangi bir sayıda 8 baytlık sabit uzunluklu kaydı içerir:
| Bayt | Tür | Endianness | kullanım |
-------|-------|------------|---------------------------------|
| 0–3 | int32 | büyük | Kayıt ofseti (16 bit sözcüklerle) |
| 4–7 | int32 | büyük | Kayıt uzunluğu (16 bit kelimelerle) |

Bu dizin, önce şekil dizininde geriye doğru arama yaparak ve ardından kayıt ofsetini okuyarak şekil dosyasında geriye doğru aramayı mümkün kılar. Bu ofset, SHP dosyasında doğru konumu aramak için kullanılabilir. İleriye dönük arama da yapabilirsiniz; aynı yöntemi kullanan rastgele sayıda kayıt. Bununla birlikte, bir SHP dosyasıyla birlikte tam dizin oluşturmak mümkündür, ancak SHP dosyasının hızlı bir şekilde bozulma şansını artırabilir.


## Referanslar

* [Shapefile - Wikipedia'dan)](https://en.wikipedia.org/wiki/Shapefile)


