{
  "date" : "2021-08-24",
  "keywords" :[ "wdb dosyası", "wdb dosya biçimi", "wdb dosyası nedir", "dosya", "wdb örneği", "wdb dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"WDB dosya formatı ve WDB dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"WDB - SQL Server İzleme Dosyası",
  "linktitle" : "WDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-24"
}

## .wdb dosyası nedir?
.wdb uzantılı bir dosya aslında Microsoft Works tarafından oluşturulan ve veritabanı yönetim sistemi gibi işlevleri yerine getirmek için kullanılan bir veritabanı dosyasıdır. WDB dosyası, Access Database ([MDB](/tr/database/mdb/)) dosyasına benzer, ancak daha az verimli ve daha büyük sınırlamalara sahiptir. WDB dosyaları Microsoft Access kullanılarak açılamıyor. Ancak, MS Access'te bir WDB dosyası açmak için WDB dosyasını Microsoft Works'te açabilir ve ardından MDB dosyasına verebilirsiniz.

## WDB dosya formatı
Microsoft Works Veritabanı, Microsoft Works ofis paketinin yerel veritabanı biçimidir. Biçimin tescilli doğası ve bazı sınırlamalar nedeniyle. WDB dosyaları, Microsoft Works dışında herhangi bir yazılımda açılamaz. Dosya biçiminde, bir NULL değeri ile sonlandırılan alanların değerlerini temsil eden ASCII metin dizelerinin her birinin önünde yinelenen, 10 baytlık bir başlık bulunabilir. Başlık genellikle bir **\x0f** baytı ve NULL ile başlar, ardından NULL'larla dönüşümlü 4 veri baytı gelir.

### Dosya yapısı

WDB dosyasının yapısı aşağıda verilmiştir:
- **1. başlık**: dosyanın başından itibaren \x25\x00\xf2 ve 244 NULL bayt ile biter
- **2. başlık**: \xffT - yani \xff\x54 ile başlayan ve 4096 bayta uzanan, sütun/alan adlarını ve diğer şeyleri içeren ve bayt konumu 6144'te başlıyor gibi görünen.
- **Alan**: değerin 10 baytlık bir başlığı vardır ve şu biçimdedir: {byte yazın} {byte yazın, bölüm 2} {veri baytı 1} \x00 {db 2} \x00 {db 3} {db 3 , bölüm 2} {db 4} \x00. veri baytı 2 alan numarasıdır, veri baytı 3 kayıt numarasıdır (256 kaydı geçtiğinde veri baytı 3, bölüm 2 eklenir).


## Referanslar ##

* [Kullanıcı:JesseW/wdb biçimi](https://en.wikipedia.org/wiki/User:JesseW/wdb_format)

