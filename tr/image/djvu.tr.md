{
  "date" : "2019-10-11",
  "keywords" :[ "djvu dosyası", "djvu dosya biçimi", "djvu dosyası nedir", "dosya", "djvu örneği", "djvu dosya uzantısı","uzantı", "biçim" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DJVU Dosya Biçimi",
  "description":"DJVU dosya formatı ve DJVU dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "DJVU",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## DJVU dosyası nedir?

“Déjà vu” olarak telaffuz edilen DjVu, özellikle metin, çizim, resim ve fotoğraf kombinasyonunu içeren taranmış belgeler ve kitaplar için tasarlanmış bir grafik dosyası formatıdır. AT&T Labs tarafından geliştirilmiştir. Metin ve arka plan görüntülerinin görüntü katmanı ayrımı, aşamalı yükleme, aritmetik kodlama ve iki tonlu görüntüler için kayıplı sıkıştırma gibi birçok teknik kullanır. DJVU dosyası sıkıştırılmış ancak yüksek kaliteli renkli görüntüler, fotoğraflar, metin ve çizimler içerebildiğinden ve bu nedenle daha az alana kaydedilebildiğinden, web'de e-Kitaplar, kılavuzlar, gazeteler, eski belgeler vb.

DjVu, [PDF](/tr/pdf/) için üstün bir alternatif olarak derecelendirilebilir. DjVu ile ilişkili dosya uzantıları .DJVU veya .DJV'dir. DjVu, renkli belgeler için [JPEG](/tr/image/jpeg/) ve [GIF](/tr/image/gif/) gibi mevcut yöntemlerden yaklaşık 5 – 10 daha iyi ve [TIFF](/tr/image/tiff/) 'den 3 – 8 kat daha iyi sıkıştırma oranları elde edebilir. siyah beyaz belgelerde. 25 MB'a kadar tam renkli olarak 300 DPI'da taranan belgeler 30 ila 100 KB'ye kadar sıkıştırılabilir. Benzer şekilde, Siyah beyaz belgeler 5 ila 30 KB'ye kadar sıkıştırılabilir. Ortalama bir HTML sayfası 50 KB'a kadar olabilir, bu nedenle bu belgeler net olarak sorunsuz bir şekilde yüklenebilir.

## Kısa Tarih ##

DjVu teknolojisi AT&T laboratuvarlarında [Yann LeCun](https://en.wikipedia.org/wiki/Yann_LeCun), [Léon Bottou](https://en.wikipedia.org/wiki/L%C3%A9on_Bottou) tarafından geliştirilmiştir., Patrick Haffner ve Paul G 1996'dan 2001'e kadar. DjVu dosya formatı, en sonuncusu 2005'ten olmak üzere çeşitli revizyonlardan geçti.


|Sürüm|Yayın tarihi|Notlar
---|---|---|
|1–19|1996–1999|Bunlar geliştirme sürümleridir.
|20|Nisan 1999|Tek sayfa, Çoklu sayfa formatına dönüştürüldü.
|23|Temmuz 2002|CID parçası
|24|Şubat 2003|LTAnno yığın
|21|Eylül 1999|Dolaylı depolama formatı değiştirildi. Metin arama katmanı eklendi.
|22|Nisan 2001|Sayfa yönü, renkli JB2
|25|Mayıs 2003|NAVM öbeği. DjVu yer imleri için destek eklendi.
|26|Nisan 2005|Metin/satır açıklamaları

## DjVu Dosya Biçimi ##

DjVu belgeleri IFF85 dosyalarıdır. Yapı, bilgileri bir DjVu dosyasında tutan bir kapsayıcı hiyerarşisi sağlar. Bu kaplara “Parçalar” da denir. Yığın türü ve Yığın Kimliği, yığının nasıl kullanıldığını açıklar. IFF yapısı tarafından takip edilen 4 baytlık bir başlık vardır. Bir DjVu dosyasının ilk dört baytı 0x41 0x54 0x26 0x54'tür. Bu bölüm, çeşitli DjVu belgeleri türlerini ve bunları oluşturan karşılık gelen parçaları ele almaktadır.


|Yığın Kimliği|Kullanım
---|---|
|FORM|İkincil tanımlayıcı olan FORM öbeğinin ilk dört veri baytına sahip bileşik yığın.
|FORM:DJVM|Çok sayfalı bir DjVu belgesi. DIRM yığınını içeren bileşik yığın.
|FORM:DJVU|Tek sayfa DjVu belgesi. Bir djvu belgesinde bir sayfa oluşturan parçaları içeren bileşik yığın.
|FORM:DJVI|INCL öbeği aracılığıyla dahil edilen bir "paylaşılan" DjVu dosyası. Paylaşılan ek açıklamalar ve şekil sözlüğü.
|FORM:THUM|Gömülü küçük resimler olan TH44 parçalarını içeren bileşik yığın.
|DIRM|Çok sayfalı belgeler için sayfa adı bilgisi.
|NAVM|Yer imi bilgisi
|ANTa, ANTz|Hem ilk görünüm ayarları hem de yer paylaşımlı köprüler, metin kutuları vb. dahil ek açıklamalar.
|TXTa, TXTz|Unicode Metin ve düzen bilgileri.
|Djbz|Paylaşılan şekil tablosu.
|Sjbz|BZZ, maskeyi depolamak için kullanılan sıkıştırılmış JB2 bitonal verileri.
|FG44|IW44 verileri ön planı depolamak için kullanılır
|BG44|IW44 verileri arka planı depolamak için kullanılır
|TH44|IW44 verileri, gömülü küçük resimleri depolamak için kullanılır
Bir filigranı kaldırmak için |WMRM|JB2 verileri gerekir
|FGbz|Renkli JB2 verileri. Karşılık gelen Sjbz parçasındaki her biri için bir renk (blit veya şekil?) sağlar.
|BİLGİ|Bir DjVu sayfası hakkında bilgi
|INCL|Dahili bir FORM:DJVI öbeğinin kimliği.
|BGjp|JPEG kodlu arka plan
|FGjp|JPEG kodlu ön plan
|Smmr|G4 kodlu maske

### DJVU Sıkıştırma

Tek görüntü birçok farklı görüntüye bölünür ve ardından her görüntü ayrı ayrı sıkıştırılır. Bir DjVu dosyasının oluşturulması için görüntü önce arka plan, ön plan ve maske görüntüsü olmak üzere üç görüntüye ayrılır. Tipik olarak arka plan ve ön plan görüntüleri daha düşük çözünürlüklü renkli görüntülerdir; ancak maske görüntüsü daha yüksek çözünürlüklü bir görüntüdür ve genellikle metin burada depolanır. Ayırma işleminden sonra, ön plan ve arka plan görüntüleri dalgacık tabanlı sıkıştırma algoritması IW44 ile sıkıştırılırken, maske görüntüsü JB2 adı verilen başka bir yöntem kullanılarak sıkıştırılır.

JB2 kodlama yöntemi, belirli bir yazı tipindeki bir karakterin birden fazla oluşumu gibi sayfadaki aynı şekilleri tanımlayarak metin görüntüsündeki fazlalığın çoğunu ortadan kaldırır. JB2 önce benzer şekiller arasındaki fazlalıktan yararlanarak her benzersiz şeklin bit eşlemini kodlar. Ardından, her bir şeklin sayfada göründüğü konumları kodlar. Hem JB2 hem de IW44, ZP kodlayıcı adı verilen ve Shannon sınırının birkaç yüzdesi içinde kalan fazlalıkları sıkıştıran yeni bir uyarlanabilir ikili aritmetik kodlayıcı türüne güveniyor. ZP kodlayıcı uyarlanabilir ve diğer yaklaşık ikili aritmetik kodlayıcılardan daha hızlıdır.

## Referanslar ##

* [DjVu - Wikipedia](https://en.wikipedia.org/wiki/DjVu)
* [DjVu Dosya Biçimi](https://www.cuminas.jp/docs/techinfo/DjVu3Spec.pdf)

