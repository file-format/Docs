{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PDF/X Dosya Biçimi",
  "description":"PDF/X dosya formatı ve PDF/X dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "PDF/X",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# PDF/X dosyası nedir? #

PDF/X, 2001'de PDF işlevselliğinin bir alt kümesiyle yayınlanan bir ISO 15930 standardıdır. Standart, basım ve yayıncılık endüstrilerinin özel gereksinimlerine göre oluşturulmuş ve yayınlanmıştır. Bu standardın gereklilikleri, basım ve yayıncılık endüstrilerinin çeşitli ihtiyaçlarına göre tasarlanmıştır. PDF/X, uyumlu dosyaların eksiksiz, yani bağımsız olmasını gerektirir. Bu, sayfada kullanılan yazı tipleri gibi öğelerin belgenin parçası olmasını gerektirir. 3D veya video gibi içerikler, PDF/X belgesinin parçası olamaz. PDF/X belgesinde yer alan bilgiler, doğru olmasını gerektirir.

## PDF/X Standartları ve Revizyonları ##

PDF/X standart ailesi, her biri özel bir sonuç için tasarlanmış birkaç versiyondan oluşur. Bu standartların geliştirilmesi, basım ve yayıncılık endüstrilerinin çok çeşitli ihtiyaçlarını karşılamayı amaçlıyordu.

* `PDF/X-1a` - PDF/X ailesinin ilk standardı olarak da bilinen PDF/X-1a, yazdırılabilmesi için tüm içeriğin PDF belgesinin parçası olmasını gerektirir. Yazı tipleri, formlar, parola koruması ve görünür notlar gibi belge öğelerine izin verilmez. PDF/X-1a'nın şeffaflık ve katmanlara izin verilmesi gibi kendine özgü gereksinimleri vardır. Bunlar ayrıca, baskı öğelerinin yalnızca CMYK, gri tonlama veya nokta renkleri kullanmasını gerektirir, bu da RGB veya cihazdan bağımsız renk alanlarının kullanılmamasına neden olur. tüm dosyaların RGB veya renk yönetimli veriler olmadan CMYK (ve/veya spot renkler) olarak teslim edileceği değiş tokuşlar içindir. PDF/X-1a, tarafından istenen bilgilerin eksiksiz olması nedeniyle Tam Değişim olarak da anılır.
* `PDF/X-3` - 2002'de tanıtıldı ve PDF/X-1a'nın birçok kısıtlamasını kaldırdı. Bu, bir PDF/X-3'teki grafiklerin CMYK, grescale, RGB, Lab ve ICC tabanlı renk uzaylarını kullanmasını sağladı. Aslında [ICC profili](https://en.wikipedia.org/wiki/ICC_Profile) ile PDF standartları 1.3'e dayanmaktadır. Bir PDF belgesinde yer alan renklerle ilgili getirdiği esneklik ve kurallar nedeniyle Renk Yönetimi olarak da adlandırılır.
* `PDF/X-4` - saydamları destekler, dolayısıyla PDF-X/4 düzleştirme olmadan çıktı almak için gereken tüm verileri içerir.
* `PDF/X-5` - PDF/X-4'ü temel alır, referans XObject'ler yoluyla harici grafikler ve işleme amacı için harici n-renklendirici profilleri için destek ekler. PDF sürüm 1.6'yı kullanarak yazdırma verilerinin kısmi değişimi için kullanın

## Referanslar ##

* [PDF/X - Wikipedia'dan](https://en.wikipedia.org/wiki/PDF/X)

