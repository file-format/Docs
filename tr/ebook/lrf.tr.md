{
  "date" : "2019-12-12",
  "keywords" :[ "LRF", "dosya", "uzantı", "biçim", "eKitap", "Dijital kitap"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"LRF dosya formatı ve LRF dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"LRF Dosya Biçimi - Bir Sony Taşınabilir Okuyucu Dosyası",
  "linktitle" : "LRF",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2019-12-12"
}

## .lrf dosyası nedir?

.lrf uzantılı bir dosya, metin, resimler ve sayfalandırma verileri dahil olmak üzere bir Sony BBeB için veriler içeren bir Geniş Bant e-Kitap (BBeB) dosyasıdır. Dosya, bir başlık, belirli sayıda nesne ve bir nesne dizini içeren sıkıştırılmış bir ikili biçimde kaydedilir. LRF ve LRX dosyaları, mevcut iki BBeB kitap formatını içerir. LRF dosyaları şifrelenmemiştir ve [LRX](/tr/ebook/lrf/) dosyalarından derlenebilir. LRF dosyaları, PDF ve HTML dahil olmak üzere diğer birçok dosya türünden dönüştürülebilir. Bilgisayarınız LRF dosyasını açamıyorsa, muhtemelen LRF dosyalarını açmak veya düzenlemek için yazılım yüklememişsinizdir. LRF dosyalarını açabilen programlar Windows için Calibre, BookDesigner, Makelrf ve Canon Book Creator, Linux için Calibre, Macintosh için Calibre ve Sony Reader'dır.

## Kısa Tarihçe

LRF dosya türü, her şeyden önce [inXile Entertainment](https://en.wikipedia.org/wiki/InXile_Entertainment) tarafından Line Rider ile ilişkilendirilir. Line Rider bir internet fizik oyuncağıdır ve Eylül 2006'da Sloven üniversite öğrencisi Boštjan Čadež tarafından icat edilmiştir. Sony marka e-Kitap eOkuyucular (Sony PRS-500 okuyucular ve Sony Librie gibi), belgeleri ve metinleri için LRF dosya uzantısını kullanır. Bu tescilli dosya türü ve ilgili LRS ve LRX dosyaları artık kullanılmıyor. Bu üç dosya türü, Sony'nin e-kitaplarını EPUB formatında satmaya başladığı 2010 yılında durdurulan BroadBand e-Kitabını (BBeB) oluşturuyordu.

## LRF Dosya Biçimi

LRF dosya formatının ayrıntılı özellikleri [web arşivinde](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat) mevcuttur. Bir LRF dosyası şunlardan oluşur:
* bir başlık
* bir dizi nesne
* bir nesne dizini.

Tüm bu değerler Intel (önce LSB) düzenindedir.

### LRF başlığı

|Ofset (onaltılık) |Boyut(bayt) |Ad/anlamı| Örnek değer|
---|---|---|---|
|0 |8| LRF İmzası| 4C 00 52 00 46 00 00 00 = Unicode'da "LRF"|
|8 |2| sürüm?| Çoğu dosyada 999|
|A |2| "Sözde Şifreleme" |anahtar baytı 48|
|0C |4| KökNesneKimliği| 0x0044|
|10 |8| Nesne Sayısı |342|
|18 |8| ObjectIndexOffset| 0x00093440|
|20 |4| bilinmiyor| 0|
|24 |1| Bayraklar| (16 - arkadan öne, 1 = önden arkaya) 16|
|25 |1| bilinmeyen |(doldurma?) 0|
|26 |2| bilinmiyor| 1600|
|28 |2| bilinmiyor| (doldurma?) 0|
|2A |2| Yükseklik?| 600|
|2C |2| Genişlik?| 800|
|2E |1| bilinmiyor| 24|
|2F |1| bilinmeyen |(doldurma?) 0|
|30 |0x14| bilinmiyor| sıfırlar|
|44 |4| Yalnızca PlaneStream (0x1E) nesnesinin nesne kimliği| 0x0042|
|48 |4| bilinmeyen |0x1536|
|4C |2| XMLCompSize| 0x035C|


## Referanslar

* [LRF Dosya Biçimi](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat)
* [BBeB - Wikipedia'dan](https://en.wikipedia.org/wiki/BBeB)

