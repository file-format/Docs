{
  "date" : "2019-10-11",
  "keywords" :[ "ixbrl","ixbrl dosyası", "ixbrl dosya biçimi", "ixbrl dosya türü", "dosya", "tür", "ixbrl dosyası nedir" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"IXBRL - İş ve Finansal Raporlama Dosya Formatı",
  "description":"IXBRL dosya formatı ve IXBRL dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "IXBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-ixbrl",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## iXBRL dosyası nedir?

iXBRL (ilnine XBRL) dosya biçimi, [XBRL](/tr/web/xbrl/) verilerinin hem makine hem de insanlar tarafından okunabilir olması için bir HTML dosyasına gömülmesine olanak tanır. Bu aslında XBRL etiketlerini kullanan bir [xHTML](/tr/web/xhtml/) dosyasıdır ve XBRL International tarafından İngiltere'nin HMRC gereksinimlerini karşılamak için geliştirilmiştir. iXBRL kullanılarak, orijinal belgenin düzeni korunarak mali tablolar oluşturulabilir. iXBRL dosyaları, Windows İşletim Sisteminde Not Defteri ve MacOS'ta TextEdit gibi herhangi bir metin düzenleyicide açılabilir.

## iXBRL Dosya Biçimi

iXBRL'nin içinde, XBRL'nin içeriği, XML etiketlerini kullanan xHTML dosya biçiminde sarılır. XBRL gibi,<xbrl> iXBRL dosyalarının kök öğesidir. XHTML biçimi, içeriğini farklı belge türlerinin ve modüllerin koleksiyonu olarak temsil eder. XHTML'deki tüm dosyalar, XML dosya biçimini temel alır ve XML belge standartlarına uygundur. XHTML, bağımlı [HTML](/tr/web/html/) Belge Nesne Modeli'nin (DOM) veya [XML](/tr/web/xml/) Belge Nesne Modeli'nin operasyonel kullanımı için temel kullanım biçimidir. Dış dünya için iXBRL, [xHTML](/tr/web/xhtml/) dosya formatı belirtimlerini takip eder.

### iXBRL ve XBRL

XBRL, aşağıdaki faktörlere dayalı olarak iXBRL ile karşılaştırılabilir:

* Karmaşıklık
* Biçimlendirme seçenekleri
* Dosya Türleri/Uzantılar
* Oluşturma Seçeneği
* Dosyalama Süreci

Aşağıdaki tablo bu farklılıkları göstermektedir.

|Parametre|XBRL|iXBRL|
---|---|---|
|Karmaşıklık|iXBRL'den daha karmaşık|XHTML'nin mevcut organizasyon şeması sayesinde daha az karmaşık|
|Biçimlendirme Seçenekleri|Sınırlı Esneklik|İçerik biçimlendirme için Yüksek Esneklik|
|Dosya Türleri/Uzantı|Resmi olarak .xml uzantısıyla kaydedilir|Genellikle .html veya .xhtml uzantısı olarak kaydedilir|
|Oluşturma Seçenekleri|Bunları görüntülemek için XBRL görüntüleyicileri gerekir|Tarayıcılarda görüntülenebilen, okunabilir insan içeriği|
|Dosyalama İşlemi| XBRL (makine tarafından okunabilen) ve HTML (insan tarafından okunabilen) örnek belgeleri ayrı ayrı dosyalanmalıdır.|Tek bir örnek belgede hem insanlar tarafından okunabilen hem de makine tarafından okunabilen biçimler mevcuttur|

## Referanslar

* [XBRL - Wikipedia Tarafından](https://en.wikipedia.org/wiki/XBRL)
* [iXBRL](https://www.xbrl.org/the-standard/what/ixbrl/)

