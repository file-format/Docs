{
  "date" : "2022-05-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OBML Dosya Biçimi - Opera Mini Kaydedilmiş Web Sayfası Dosyası",
  "description" :"OBML dosyasının ne olduğu ve OBML dosyasını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "OBML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-05-19"
}

## OBML dosyası nedir?

Bir OBML (Opera Binary Markup Language) dosyası, Opera Mini mobil web tarayıcısı tarafından kaydedilen bir web sayfasının çevrimdışı sürümüdür. Çevrimdışıyken belirli cihazlarda görüntülenmek üzere sayfanın tüm öğelerini içeren [HTML](/tr/web/html/) dosyalarının kendi kendine yeten, kompakt bir sürümüdür. OBML dosya formatı, OBML15 ve OBML16'nın genel olarak kullanıldığı çeşitli sürümlere yükseltildi. Dikkate alınması gereken önemli bir nokta, her Opera Mini sürümünün yalnızca bir OBML formatıyla uyumlu olmasıdır. Böylece, Opera Mini'nin yükseltilmesi, önceden kaydedilmiş sayfaları okunabilir durumda bırakacaktır. OBML dosyaları HTML'ye ve [PDF](/tr/pdf/)'ye dönüştürülebilir.

## OBML Dosya Biçimi

OBML dosya formatı, Opera'nın tescilli dosya formatında kaydedilir ve dosya formatı belirtimleri kamuya açık değildir. Ancak, [OMBL formatı](https://github.com/grawity/obml-parser/blob/master/obml.md) aşağıdaki gibi yapısının kodunu çözmek için tersine mühendislik yapılmıştır.

### OBML Veri Türleri

Tersine mühendislik sonuçlarına göre, OBML aşağıdaki ilkel türleri kullanır:

* `bayt` – işaretsiz tamsayı (1 bayt)
* `kısa` – işaretli tamsayı (2 bayt, büyük-endian)
* "orta" - işaretli tamsayı (3 bayt, büyük-endian)
 * `blob` – { length: short, data: byte[length] }
* `char` – ASCII karakteri içeren bir bayt
* "dize" – UTF-8 kodlu metin içeren bir damla

### OBML Başlığı

```
header := {
	(if version >= 15) {
		fake_file_size: medium = 0x02d355
		fake_version: byte     = 16
	}
	file_size: medium
	version: byte
	page_size: coords
	(if version == 16) {
		unknown: byte[3]      // always S\x00\x00
	}
	unknown: short                // always -1
	page_title: string
	unknown: blob
	page_url_base: string
	page_url: url
	(if version >= 15) {
		unknown: byte[6]
	}
	(if 6 < version <= 13) {
		unknown: byte[5]
	}
	(if version == 6) {
		unknown: byte[1]
	}
	metadata: chunk[]
	content: chunk[]
}
```
## Referanslar

* [OMBL biçimi](https://github.com/grawity/obml-parser/blob/master/obml.md)

