{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PDF/UA Dosya Biçimi",
  "description":"PDF/UA dosya formatı ve PDF/UA dosyaları oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "PDF/UA",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# PDF/UA dosyası nedir? #

PDF/UA, Ağustos 2012'de [ISO Standardı 14289-1](https://en.wikipedia.org/wiki/ISO_14289) olarak yayınlandı ve evrensel olarak erişilebilir PDF belgeleri için bir dizi gereksinimin açık ara ilk tam tanımıdır. "Evrensel olarak erişilebilir" terimi, bir [PDF](/tr/pdf/) belgesinde yer alan bilgilerin genel olarak herkes ve özelde engelli kişiler tarafından eşit ve bağımsız bir şekilde erişilebilir olması gerektiği anlayışını ifade eder. PDF/UA standardının tanıtılması, PDF içeriği oluşturmak ve okumak amacıyla araçlar ve uygulamalar oluşturmak için önemli bir adım olarak kabul edilebilir.

## Dosya Biçimi Gereksinimleri ##

PDF/UA'nın temelinde, bu standardın özü olarak işlev gören bazı kesin gereksinimler vardır. Temel olarak bunlar, PDF'leri etiketlemeye dayalıdır, bu da tüm PDF/UA belgelerinin uygun şekilde etiketlenmesi gerektiği anlamına gelir. Ayrıca etiketlerin anlamsal olarak uygun ve mantıksal sırada olmasını gerektirir. Bu, PDF/UA spesifikasyonu ile oluşturulan son belgenin daha güvenilir ve erişilebilir olmasını sağlar. Bu, PDF yazarlarının tüm bu tür gereksinimler hakkında her şeyi bilmeleri gerekip gerekmediğini sorgulamasına neden olabilir. Neyse ki, PDF/UA uygunluk araçları, PDF'nin erişilebilirliğini ekleme ve koruma sorumluluğunu üstlendiğinden, durum böyle değildir.

PDF/UA için dosya biçimi gereksinimleri aşağıdaki gibidir.

* İçerik, iki yoldan biriyle kategorize edilir: anlamlı içerik ve dekoratif sayfa öğeleri gibi eserler. Tüm anlamlı içerikler etiketlenmeli ve bir belgedeki tüm etiketlerin yapı ağacına entegre edilmelidir. Öte yandan eserler, yalnızca bu şekilde işaretlenmelidir.
* Anlamlı içerik, etiketlerle işaretlenmeli ve belgedeki diğer etiketlerle birlikte eksiksiz bir yapı ağacı oluşturmalıdır.
* Anlamlı içerik uygun semantik etiketlerle işaretlenmelidir.
* Belge etiketleri tarafından oluşturulan yapı ağacı, belgenin mantıksal okuma sırasını yansıtmalıdır.
* Yalnızca PDF 1.7'de tanımlanan standart etiketler kullanılabilir; başka etiketler kullanılıyorsa, bir rol atama girişi, her birinin hangi standart etiketi temsil ettiğini kaydetmelidir.
* Bilgiler sadece görsel araçlarla aktarılamaz (örn. kontrast, renk veya sayfadaki konum).
* JavaScript tarafından kontrol edilen efektler olarak veya PDF içine gömülü herhangi bir videonun parçası olarak titreyen, yanıp sönen veya yanıp sönen içeriğe izin verilmez.
* Bir belge başlığı verilmeli ve belge başlığı (dosya adı yerine) pencere başlığında görünecek şekilde ayarlanmalıdır.
* Tüm içeriğin dili not edilmeli ve dil değişiklikleri açıkça bu şekilde işaretlenmelidir.

## PDF/UA Uyumluluğu ##

PDF/UA standardı, içerik, okuyucular ve yardımcı teknoloji için özellikleri tanımlar. Bu üç husus, belgenin içeriğine göre birbiriyle bağlantılıdır. Bunların her biri için uygunluk gereklilikleri aşağıda belirtildiği gibidir.

## Uygun Dosyalar ##

PDF/UA standardına uygun dosyalar, [PDF 1.7 belirtimlerine](http://www.adobe.com/go/pdfreference) göre geçerli olan özellikleri içermelidir. Ancak, PDF/UA tarafından özel olarak yasaklanan özellikler hariç tutulmalıdır.

## Uyumlu Okuyucular ##

Uyumlu bir okuyucu, PDF 1.7 belirtimlerinde belirtilen kurallara uymalıdır. Özellikle, şunları desteklemelidir:

* erişilebilirlik için belirtilen tüm etiketler, nitelikler ve anahtar değerler. Ayrıca dijital imzaları, ek açıklamaları ve İsteğe Bağlı İçeriği işleme ve temsil etme yeteneğine sahip olmalıdır.
* dijital imzaları, ek açıklamaları ve İsteğe Bağlı İçeriği işler ve temsil eder
* belgede çeşitli yollarla gezinin

## Uyumlu Yardımcı Teknoloji ##

PDF/UA özelliklerini desteklemek için uygun bir yardımcı teknoloji bağlıdır. Bunlar, örneğin içeriğin ve okuyucunun özelliklerini içerir ve sayfa etiketlerine, belge yapısına veya ana hatlara göre gezinmeye izin vermelidir. Ayrıca kullanıcının varsayılan gezinme yakınlaştırmasını geçersiz kılmasına izin vermelidir.

## Referanslar ##

* [PDF/UA - Wikipedia'dan](https://en.wikipedia.org/wiki/PDF/UA)
* [Özet Kabuğunda PDF/UA](http://www.pdfa.org/publication/pdfua-in-a-nutshell/)

