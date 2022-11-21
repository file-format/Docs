{
  "date" : "2019-12-12",
  "keywords" :[ "EPUB", "dosya", "uzantı", "biçim", "E-Kitap", "Dijital kitap"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"EPUB dosya formatı ve EPUB dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"EPUB dosyası nedir?",
  "linktitle" : "EPUB",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2019-12-12"
}

## EPUB dosyası nedir?

.epub uzantılı dosyalar, yayıncılar ve tüketiciler için standart bir dijital yayın formatı sağlayan bir e-kitap dosya formatıdır. Format şimdiye kadar o kadar yaygın hale geldi ki birçok e-okuyucu ve yazılım uygulaması tarafından destekleniyor. Örneğin, Mac OS'de önceden yüklenmiş **Kitaplar** yazılımı bu tür dosyaları açma desteği sağlar. Ayrıca akıllı telefonlar, tabletler ve bilgisayarlar için çok sayıda uyumlu yazılım mevcuttur. EPUB dosya standartları [Uluslararası Dijital Yayıncılık Forumu](https://idpf.org/epub/30/spec/epub30-publications.html)(IDPF) tarafından sağlanmaktadır. EPUB 3 sürümü, içeriğin paketlenmesi için standartlaştırılmış en iyi uygulamalar, araştırma, bilgi ve etkinlikler konusunda lider bir kitap ticaret birliği olan Kitap Endüstrisi Çalışma Grubu (BISG) tarafından da onaylanmıştır.

## EPUB Dosya Formatının Kısa Tarihi

* **Ekim 2007** - EPUB 2.0 onaylandı
* **Eylül 2010** - Bakım güncellemesi yayınlandı
* **Ekim 2011** - EPUB 3.0 spesifikasyonları yürürlüğe girdi
* **Haziran 2014** - 3.0 sürümünün yerini alacak küçük bakım güncellemesi yayınlandı
* **Ocak 2017** - EPUB 3.1 yürürlüğe girdi

## EPUB Dosya Biçimi

EPUB dosya formatı, [ZIP](/tr/compression/zip/) uzantısı olarak yeniden adlandırılabilen bir arşivdir ve içeriği herhangi bir arşiv çıkarıcı ile çıkarılarak görüntülenebilir. Açık bir XML tabanlı biçimdir ve HTML dosyalarından, resimlerden, CSS stil sayfalarından ve diğer öğelerden oluşur. Ayrıca, çeşitli yazılım uygulamaları ve API'ler aracılığıyla PDF, Mobi ve diğer birkaç dosya biçimine dönüştürülebilir.

{{< figure src="../epub.png" alt="EPUB Dosya Biçimi" >}}

**EPUB E-Kitap, Mac OS Books Uygulaması ile açıldı**

EPUB dosya formatı aşağıdaki üç açık standarda dayanmaktadır.

### Açık Kamu Yapısı (OPS) ###

Bir EPUB 2.0 dosyası, bir yayının içeriğini oluşturmak için XHTML 1.1'i kullanır. Temelde bu, bir EPUB dosyasının bir veya daha fazla web sayfasından oluştuğu anlamına gelir. Bir kitabın veya gazetenin tüm içeriğini tek bir sayfaya sığdırabilseniz bile, böyle bir dosyanın 300K'yı geçmemesi hem performans hem de uyumluluk açısından daha iyidir. Tıpkı normal web sayfalarında olduğu gibi, stil ve düzen basamaklı stil sayfaları (CSS) kullanılarak tanımlanır. EPUB dosyalarında, CSS2'nin bir alt kümesinin (sınırlı komut dizisi) kullanılması gerekir. Yuvarlak kutular veya alt gölgeler gibi CSS3'ün yeni özelliklerinin birçoğu henüz mevcut değil. Geriye dönük uyumluluk için, bir içerik oluşturucu, içeriği kodlamak için XHTML yerine DTBook'u da kullanabilir.

### Açık Ambalaj Formatı (OPF) ###

Spesifikasyonların bu kısmı, meta veriler (yazar ve yayıncı kim, başlık nedir,..), bildirim (bir epub dosyası içindeki tüm dosyaların listesi) ve içindekiler tablosu gibi yapısal bilgilerle ilgilenir. Bu verilerin tümü XML kullanılarak gömülür.

### Açık Konteyner Biçimi (OCF) ###

Yukarıdaki açıklamaların açıklığa kavuşturması gerektiği gibi, bir EPUB belgesi bir dizi dosyadan oluşur. OCF özellikleri, tüm bu dosyaların tek bir konteyner dosyasında nasıl paketlendiğini tanımlar. Bunun için ZIP sıkıştırması kullanılır.

## Desteklenen Görüntü Dosyası Biçimleri ##

EPUB dosya formatı aşağıdaki resim dosyası formatlarını destekler.

* [GIF](/tr/image/gif/)
* [JPG](/tr/image/jpeg/)
* [PNG](/tr/image/png/)
* [SVG](/tr/page-description-language/svg/)

## Referanslar ##

* [EPUB - Wikipedia'dan](https://en.wikipedia.org/wiki/EPUB)

