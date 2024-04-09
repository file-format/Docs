{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PDF/A Dosya Biçimi",
  "description":"PDF/A dosya formatı ve PDF/A dosyaları oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "PDF/A",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# PDF/A nedir? #

PDF/A, elektronik belgelerin PDF biçiminde arşivlenmesi için bir ISO standart biçimidir. İlk ortaya çıkış sebebi uzun süreli arşivleme ihtiyaçlarını karşılamaktı. Standart, uygunluğu sağlamak için belge ayrılmaz parçalarına belirli sınırlamalar getirerek arşivlenmiş dosyaların uzun süre sonra bile açılmasını sağlar. Biçim artık tüm endüstrilerde geniş çapta benimsenmiştir. Adobe Acrobat Reader gibi PDFA/A görüntüleyiciler, bu formatta kaydedilen dosyaların bu Standart tarafından paylaşılan bilgilere göre gelecekte bile açılabilmesini sağlar.

## PDF/A Sürümleri ##

PDF/A, Ekim 2005'te ISO Standardı olarak kabul edildi. O zamandan beri, sürekli olarak geliştiriliyor ve zaman içinde birkaç standart daha geliştirildi. Zaman içerisinde yayınlanan PDF/A standartlarına ilişkin bilgiler ve detayları aşağıdaki gibidir:

* **PDF/A-1:** Ekim 2005'te ISO 19005-1 olarak yayınlandı ve PDF 1.4'ü temel alıyor
* **PDF/A-2:** Haziran 2011'de ISO 19005-2 olarak yayınlanmıştır ve PDF 1.7'ye (ISO 32000-1:2008) dayanmaktadır.
* **PDF/A-3:** Ekim 2012'de ISO 19005-3 olarak yayınlanmıştır ve PDF 1.7'ye (ISO 32000-1:2008) dayanmaktadır.

## PDF/A-1 ##

PDF/A-1 standardı, orijinal PDF 1.4 sürümünü temel almıştır. PDF/A-1 standardı, PDF dosyaları için iki uygunluk düzeyi tanımlar.

### PDF/A-1a ###

A Seviyesi ile uyumludur ve PDF/A-1 Standardının spesifikasyonlarındaki tüm gereklilikleri karşılar. PDF/A-1a, metnin belgeden çıkarılabilmesini sağlar. Ayrıca entegre metin materyalinin doğal okuma sürecinin bozulmadan kalmasını garanti eder. PDF/A, "etiketli PDF" olarak bilinen yeniden yapılandırılarak küçültülmüş ekranlarda metin temsili yeteneği gereksinimi getirir. Yardımcı yazılıma izin vererek, fiziksel engelli kullanıcılar için uyumlu dosyalara erişilebilirliği artırmayı amaçlıyordu.

### PDF/A-1b ###

PDF/A-1b, daha düşük bir uyumluluk düzeyidir ve ISO 19005 standardına göre elektronik belgelerin görsel görünümü ile ilgilenir. Sayfalardaki metin ve diğer içeriklerin aynı şekilde yeniden üretilmesini sağlar. Bu B Düzeyi uygunluk, uyumlu bir dosyanın işlenmiş görsel görünümünün uzun vadede korunabilir olmasını sağlamak için minimum uyumluluğu gösterir.

## PDF/A-2 ##

PDF/A-2, ISO Standardı tarafından Temmuz 2011'de ISO 32001-1 olarak bilinen yeni bir standart olarak yayınlandı. Bu yeni standart, yalnızca 1.7'ye kadar olan PDF sürümlerinin tüm özelliklerinden faydalanmakla kalmadı, aynı zamanda yeni bir standart olarak tanıtıldı. PDF/A-2, bu yeni standardın bir parçası olarak aşağıdaki özellikleri içermektedir.

* PDF/A-2, belgelerin taranması durumunda yardımcı olan [JPEG2000](/tr/image/jp2/) desteğiyle gelir.
* Diğer benzer dosyalara sahip bir kapsayıcı PDF oluşturmak için kullanılabilecek PDF/A koleksiyonlarının gömülmesini destekler
* Kısmen desteklendiği PDF/A-1 ile karşılaştırıldığında, PDF dosyalarının saydamlık özelliğini bütünüyle destekler.
* PDF/A-2, haritalama uygulamaları ve mühendislik çizimleri için yararlı olan isteğe bağlı içerik desteği sağlar. Bunlar, bakan kişinin gereksinimlerine göre görünür hale getirilebilen veya gizlenebilen katmanlar olarak da bilinir.
* Özel XMP meta verileri için gereksinimleri belirtir
* Yeni yorum türlerinden bazılarını yasaklanmış ek açıklama türleri listesine ekler. Ayrıca, metin düzenleme yorumları gibi bazı yeni yorum türleri kabul edilebilir öğeler listesine eklendi.

## PDF/A-3 ##

PDF/A-3, Düzey 2'nin tüm uyumluluk gereksinimlerini içerir ve ek dosya biçimlerinin (XML, [CSV](/tr/spreadsheet/csv/), [CAD](/tr/cad/), [kelime işlemci] gibi) gömülmesine izin verir. (/tr/word-processing/), [elektronik tablo](/tr/spreadsheet/) ve diğerleri) PDF/A uyumlu belgelere.

## Referanslar ##

* [PDF/A - Wikipedia'dan](https://en.wikipedia.org/wiki/PDF/A)
* [Teknik Belge: PDF/A – Temel Bilgiler](https://www.pdf-tools.com/public/downloads/whitepapers/whitepaper-pdfa.pdf)

