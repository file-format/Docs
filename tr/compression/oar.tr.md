{
  "date" : "2021-04-08",
  "keywords" :[ "kürek dosyası", "kürek dosyası formatı", "kürek dosyası nedir", "dosya", "kürek örneği", "kürek dosyası uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OAR - OpenSimulator Arşiv Dosya Formatı",
  "description":"OAR dosya formatı ve OAR dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "OAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-15"
}

## OAR dosyası nedir?

.oar uzantılı bir dosya, ağ üzerinden çok sayıda kullanıcının erişebileceği sanal bir ortam oluşturmak için açık kaynaklı bir 3D uygulama sunucusu olan OpenSimulator uygulaması tarafından kullanılan bir arşiv dosyasıdır. OAR dosya biçimi, araziyi, nesne dokularını ve envanterleri farklı bir sisteme tam olarak yüklemek için gereken gerekli varlık verilerini sağlar. OpenSimulator ayrıca, kullanıcıların web üzerindeki diğer OpenSimulator kurulumlarını ziyaret etmelerini sağlayan isteğe bağlı hiper ızgaraya sahiptir. OAR dosyalarında internet MIME tipi uygulama/kürek bulunur ve bir veya daha fazla arşivlenmiş dosya içerir.


## OAR Dosya Biçimi

OAR, sıkıştırılmış arşiv dosyası biçiminde depolanan ikili dosyalardır. OAR dosya biçiminin en son sürümü, önceki [sürüm 0.8'den](http://opensimulator.org/wiki/OAR_Format_0.8) önemli değişiklikler içeren [sürüm 1.0](http://opensimulator.org/wiki/OAR_Format_1.0)'dır. En son sürüm, birden çok bölgenin tek bir OAR'da depolanmasını destekler ve 0.7.5'ten önceki OpenSimulator sürümleriyle geriye dönük olarak uyumlu değildir. Bir OAR dosyası, orijinal unix tar formatında (USTAR değil) gziplenmiş bir tar dosyasıdır (tar.gz).

## OAR Bölgeleri Örneği
AOR dosyaları birden fazla bölge içerebilir. Arşivin yapısı aşağıdaki gibidir (bu örnek 4 bölge içerir):

```
archive.xml
assets/
regions/
  1_1_Arizona/
    landdata/
    objects/
    settings/
    terrain/
  2_1_New_Mexico/
    landdata/
    objects/
    settings/
    terrain/
  1_2_Utah/
    landdata/
    objects/
    settings/
    terrain/
  2_2_Colorado/
    landdata/
    objects/
    settings/
    terrain/
```
## OAR Arşivi.xml

Arşiv kontrol dosyası, gelecekteki biçim değişiklikleriyle uyumluluğu tanımlamak için bir ana sürüm numarası içerir. OAR biçimindeki varlıkların varlığı, boolean öğesiyle belirtilir.<assets_included> . Dahil edilen bölgeler hakkındaki bilgiler, kontrol dosyasında bulunan bir bildirimde bulunur. Bir Archive.xml örneği aşağıdaki gibidir.

```
<?xml version="1.0" encoding="utf-16"?>
<archive major_version="1" minor_version="0">
  <creation_info>
    <datetime>1343204139</datetime>
  </creation_info>
  <assets_included>True</assets_included>
  <regions>
    <row>
      <region>
        <id>12345678-1111-1111-1111-111111111111</id>
        <dir>1_1_Arizona</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-2222-2222-2222-222222222222</id>
        <dir>2_1_New_Mexico</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
    <row>
      <region>
        <id>12345678-3333-3333-3333-333333333333</id>
        <dir>1_2_Utah</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-4444-4444-4444-444444444444</id>
        <dir>2_2_Colorado</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
  </regions>
</archive>
```

## Referanslar

* [OAR Formatı v 1.0](http://opensimulator.org/wiki/OAR_Format_1.0)
* [OpenSimulator](http://opensimulator.org/wiki/Main_Page)

