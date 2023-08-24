{
  "date" : "2021-01-21",
  "keywords" :[ "otp dosyası", "otp dosya biçimi", "otp dosyası nedir", "dosya", "otp örneği", "otp dosya uzantısı","uzantı", "biçim" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTP - OpenDocument Sunum Şablonu",
  "description":"OTP dosya formatı ve OTP dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "OTP",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2021-01-21"
}

## OTP dosyası nedir?

.otp uzantılı dosyalar, uygulamalar tarafından OASIS OpenDocument standart formatında oluşturulan sunum şablonu dosyalarını temsil eder. Böyle bir dosyanın içeriği, metin, resimler, şekiller, multimedya içeriği, geçiş efektleri ve diğer slayt öğeleri içeren slaytlar biçimindeki sunum bilgilerini içerir. Bu şablon dosyaları, şablonun kendisinde saklanan stil bilgilerine dayalı olarak hızla yeni sunumlar oluşturmak için kullanılır. OTP dosyaları, OpenOffice paketi ve Microsoft PowerPoint ile birlikte gelen Impress gibi birkaç farklı uygulama ile oluşturulabilir ve kaydedilebilir. OTP dosya formatı, Microsoft PowerPoint şablon dosyalarına [.pot](/tr/presentation/pot/) ve [.potx](/tr/presentation/potx/) benzer.

## OTP Dosya Biçimi

OTP dosya formatı, belge temsilini tek bir XML belgesi olarak ve birkaç alt belgenin [ZIP](/tr/compression/zip/) biçiminde tek bir sıkıştırılmış pakette toplanmasını destekleyen OpenDocument standardına dayanmaktadır. Dosyanın içeriği, birlikte paketlenmiş birden çok xml dosyasında dağıtılır. Bu çoklu [XML](/tr/web/xml/) dosyaları, aşağıda belirtildiği gibi belgenin stili, içeriği, meta bilgileri ve ayarları hakkında bilgiler içerir.

* `content.xml` – Belge içeriği ve içerikte kullanılan otomatik stiller.
* `styles.xml` – Belge içeriğinde kullanılan stiller ve stillerin kendisinde kullanılan otomatik stiller.
* `meta.xml` – Yazar veya son kaydetme eyleminin zamanı gibi belge meta bilgileri.
* `settings.xml` – Pencere boyutu veya yazıcı bilgisi gibi uygulamaya özel ayarlar.

## Referanslar

* [OpenDocument - Wikipedia Tarafından](https://en.wikipedia.org/wiki/OpenDocument)

