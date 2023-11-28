{
  "date" : "2023-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HDR Dosyası- ESRI BIL Başlık Dosya Formatı",
  "description":"HDR dosyası nedir?",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "identifier":"gis-hdr",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-23"
}

## HDR dosyası nedir?

HDR dosyası, satıra göre serpiştirilmiş bir Bant (.BIL) dosyası için başlık bilgilerini içeren bir GIS başlık dosyasıdır. Görüntü verilerini açıklar ve görüntü dosyasıyla aynı adı taşır. Bir HDR dosyası, her biri görüntünün belirli bir özelliğini tanımlayan bir dizi girişten oluşur. HDR dosyası, ayrı bir coğrafi referans dosyasıyla birlikte gerçek dünya koordinatlarına çevrilmek üzere BIL dosyasının düzenini ve formatını açıklar.

## HDR Dosya Formatı

HDR dosyaları ASCII metin dosyası formatında kaydedilir. Her girişin görüntünün belirli bir özelliğini tanımladığı bir dizi giriş içerir. Her HDR dosyası aşağıdaki formata sahiptir:

```
<keyword> <value>
```

'<keyword> ` - Ayarlanmakta olan belirli özelliği belirtir
'<value> ` - Özelliğin ayarlandığı değerdir

Başlıktaki girişlerin sırası konusunda herhangi bir sınırlama yoktur. Ancak HDR okuyucuların kullandığı ayrıştırma yöntemine uymak için her girişin satırın ayrı bir satırında olması gerekir.

## HDR Dosyasında Kullanılan Anahtar Kelimelerin Özeti

|Anahtar Kelime |Kabul Edilebilir Değer |Varsayılan|
---|---|---|
|daralır |herhangi bir tamsayı > 0| hiçbiri
|ncols |herhangi bir tam sayı > 0| hiçbiri
|n bantlar |herhangi bir tamsayı > 0| 1
|nbit |1, 4, 8, 16, 32| 8
|byteorder| I = Intel;M = Motorola |ana makineyle aynı|
|düzen| bil, bip, bsq| bil|
|atlamabayt| herhangi bir tamsayı ≥ 0| 0
|ulxmap |herhangi bir gerçek sayı| 0|
|ulymap |herhangi bir gerçek sayı |daralır - 1|
|xdim |herhangi bir gerçek sayı| 1
|ydim |herhangi bir gerçek sayı| 1
|bandrowbayt |herhangi bir tamsayı > 0| en küçük tam sayı ≥ (ncols x nbits) / 8|
|toplamsırabayt |herhangi bir tamsayı > 0| bil için: n bant x bant genişliği baytı; bip için: en küçük tamsayı ≥ (ncol x n bant x n bit) / 8|
|bant aralığı baytı |herhangi bir tamsayı ≥ 0| 0|

## Referanslar

* [HRD Dosya Formatı - ArcGIS](https://webhelp.esri.com/arcgisdesktop/9.2/index.cfm?TopicName=BIL,_BIP,_and_BSQ_raster_files)

