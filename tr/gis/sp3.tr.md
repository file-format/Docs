{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SP3 - NGS SP3 Dosyası",
  "description":"SP3 dosya biçimi ve SP3 dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "SP3",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-09-29"
}

## SP3 dosyası nedir?

.sp3 uzantılı bir dosya, yörünge bilgilerini depolamak için bir Ulusal Jeodezik Araştırma (NGS) yörünge biçimidir. Bu, NGS'nin SP1 ve SP2 biçimlerinin bir uzantısıdır ve yörüngelerle eş zamanlı olarak hesaplanan uydu saati düzeltme bilgilerini içerir. Öncelikle konum ve saate dayalıdır ve hızları içermez. Format, 1989'da Remondi'de önerildi ve 1991'de kabul edildi. Uydu saati düzeltme bilgilerine ek olarak, yörünge doğruluk üsleri, yorum satırları, GPS haftası ve ilk çağla ilişkili haftanın saniyeleri gibi bilgileri içerir. SP3 dosyaları Wolfram Research Mathematica ile açılabilir.

## SP3 Dosya Biçimi - Daha Fazla Bilgi

SP3 dosyaları ASCII dosya biçiminde diske kaydedilir ve içeriği herhangi bir metin düzenleyicide açılarak görüntülenebilir. Bir SP3 dosyasının yapısı aşağıdaki görselde görüldüğü gibidir.

{{< figure src="../sp3-file-format.png" title="" >}}

## Referanslar

* [Genişletilmiş Standart Ürün 3 Orbit Formatı (SP3-c)](http://epncb.oma.be/ftp/data/format/sp3c.txt#:~:text=The%20SP3%20format%20is%20smilar ,%20daha fazla%20esnek%20başlık%20yapı)
* [Ulusal Jeodezik Araştırma Standardı GPS Yörünge Formatlarının Genişletilmesi](https://beta.ngs.noaa.gov/PUBS_LIB/Extending_the_NGS_Standard_GPS_Orbit_Formats_TR_NOS133_NGS46.pdf)

