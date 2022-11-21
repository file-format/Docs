{
  "date" : "2021-07-30",
  "keywords" :[ "dlg dosyası", "dlg dosya biçimi", "dlg dosyası nedir", "dosya", "dlg örneği", "dlg dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DLG - Shapefile Shape Index Format",
  "description":"DLG dosya formatı ve DLG dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "DLG",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-30"
}

## DLG dosyası nedir?
.dlg uzantılı bir dosya, US Geological Survey (USGS) tarafından yönetilen, dijital vektör formunda gösterilen bir kartografik harita özelliği olan Dijital Çizgi Grafiği içerir. DLG dosyaları iki farklı formatta mevcuttur:
1. **İsteğe bağlı biçim**: 80 bayt mantıksal kayıt uzunluğu, UTM yer koordinat sistemi ve hat, düğüm ve alan öğelerinde bulunan topoloji bağlantılarını içeren, kullanımı kolay bir biçim.
2. **Mekansal Veri Aktarım Standardı (SDTS) formatı**: farklı bilgisayar sistemleri arasında mekansal veri aktarımını kolaylaştıran bir format.

## DLG Dosya Biçimi
DLG dosya formatı, USGS haritaları için tasarlanmıştır ve dokuz adede kadar farklı özellik kategorisiyle büyük, orta ve küçük ölçekte iletilir. DLG dosyaları, haritalama ve GIS uygulamalarında kullanılmak üzere topolojik olarak yapılandırılmış, isteğe bağlı ve Mekansal Veri Aktarım Standardı (SDTS) formatlarında gelir.
### DLG Dosya Biçiminin Özellikleri
DLG dosyaları üç farklı ölçekte dağıtılır:

1. **Büyük ölçek** - normalde şuna karşılık gelir:
- USGS 7,5'e 7,5 dakika
- 1:24.000 ve 1:25.000 ölçekli topografik dörtgen harita serisi
- Alaska için 1:63,360 ölçekli
- Porto Riko için 1:30.000 ölçekli
 

2. **Ara ölçek** - USGS'den türetilmiştir:

- 30- 60 dakika

- 1:100.000 ölçekli harita serisi
3. **Küçük ölçekli** - Amerika Birleşik Devletleri Ulusal Atlası'nın USGS 1:2.000.000 ölçekli kesit haritalarından alınmıştır.
### Veri Kategorileri
DLG dosyalarında dokuz farklı katman veya özellik kategorisi mevcuttur:
1. Kamu Kadastro Sistemi (PLSS)
2. Sınırlar (BD)
3. Ulaşım (TR)
4. Hidrografi (HY)
5. Hipsografi (HP)
6. Bitkisel olmayan özellikler (NV)
7. Sörvey kontrolü ve belirteçler (SM)

8. İnsan yapımı özellikler (MS)

9. Bitkisel yüzey örtüsü (SC)

Büyük ölçekli DLG dosyaları dokuz katmanın tümünü sunarken, orta ölçekli PLSS, BD, TR, HY ve HP'den oluşan beş katmanı sunar. Küçük ölçekli DLG'ler beş PLSS, BD, TR, HY ve MS katmanını sunar.

## Referanslar

* [Dijital çizgi grafiği - Wikipedia'dan)](https://en.wikipedia.org/wiki/Digital_line_graph)


