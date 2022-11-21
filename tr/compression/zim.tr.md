{
  "date" : "2019-12-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZIM Dosya Biçimi - OpenZIM Arşiv Dosyası",
  "description":"ZIM dosya formatı ve ZIM dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "ZIM",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-12-09"
}

## ZIM dosyası nedir? ##

.zim uzantılı dosyalar, Wiki içeriğini çevrimdışı depolamak için oluşturulan arşivlerdir. Wikipedia'yı bir USB'de depolamak için en uygun açık dosya biçimi olarak kabul edilir. Site içeriğini kompakt bir biçimde saklar. Adı, daha önceki Zeno dosya formatı olan "Zeno IMproved" den gelmektedir. ZIM, Wikimedia CH sponsorluğunda ve Wikimedia Foundation tarafından desteklenen [openZIM ](https://openzim.org/)projesi tarafından sağlanmaktadır. ZIM dosyaları, Kiwix ve ZIMReader gibi uygulamalar tarafından açılabilir. OpenZIM projesi, OpenSource topluluğunun katkısı için [Github](https://github.com/openzim) üzerinde ZIM dosya formatının uygulanmasına ev sahipliği yaptı.

## ZIM Dosya Biçimi Özellikleri

ZIM dosya formatı, [Zeno dosya formatı](https://openzim.org/wiki/Zeno_file_format) üzerinde geliştirilmiştir ve geriye dönük uyumlu değildir. ZIM dosya formatının format spesifikasyonları, geliştiricinin referansı için openZIM tarafından [çevrimiçi olarak mevcuttur](https://openzim.org/wiki/ZIM_file_format). OpenZIM, ZIM dosyalarını okumak ve yazmak için C++ açık kaynak uygulaması [LibZim](https://openzim.org/wiki/Zimlib) sağlamıştır.

ZIM dosya biçimi, içeriği kompakt hale getirmek için LZMA2 sıkıştırmasını kullanır.

{{< figure src="../ZIM_File_Format.jpeg" alt="ZIM Dosya Biçimi" >}}


### ZIM Başlığı

Bir ZIM dosyası, ofset 0'daki bir başlıkla başlar. Tüm bileşenler little-endian'a dayalıdır ve tüm tamsayılar işaretsiz tamsayılardır, yani uint_16, uint_32, uint_64.

|Alan Adı |Tür| Ofset| uzunluk| Açıklama|
---|---|---|---|---|
|sihirliNumara| tamsayı| 0| 4| Dosya biçimini tanımak için sihirli sayı 72173914 (0x44D495A)|
|ana Sürüm| tamsayı| 4| 2| ZIM dosya biçiminin ana sürümü (5 veya 6)|
|küçük Sürüm| tamsayı| 6| 2| ZIM dosya formatının küçük versiyonu|
|sıvı| tamsayı| 8| 16| bu zim dosyasının benzersiz kimliği|
|makale Sayısı| tamsayı| 24| 4| toplam makale sayısı|
|kümeSayı| tamsayı| 28| 4| toplam küme sayısı|
|urlPtrPoz| tamsayı| 32| 8| URL'ye göre sıralanan dizin işaretçi listesinin konumu|
|başlıkPtrPoz| tamsayı| 40| 8| Başlık| tarafından sıralanan dizin işaretçi listesinin konumu
|kümePtrPoz| tamsayı| 48| 8| küme işaretçisi listesinin konumu |
|mimeListPos| tamsayı| 56| 8| MIME tipi listesinin konumu (ayrıca başlık boyutu)|
|anaSayfa| tamsayı| 64| 4| ana sayfa veya ana sayfa yoksa 0xffffffff|
|düzenSayfa| tamsayı| 68| 4| düzen sayfası veya düzen sayfası yoksa 0xffffffffff|
|sağlama toplamıPoz| tamsayı| 72| 8| sağlama toplamı olmadan bu dosyanın md5checksum'una işaretçi. Bu, dosyanın bitiminden her zaman 16 baytı gösterir.|

## Referanslar ##

* [OpenZIM](https://openzim.org/)
* [C++ LibZim](https://openzim.org/wiki/Zimlib)

