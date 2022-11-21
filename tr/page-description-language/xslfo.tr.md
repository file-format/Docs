{
  "date" : "2019-10-11",
  "keywords" :[ "XSLFO", "XSL Biçimlendirme Nesneleri", "Dosya", "Uzantı", "Dosya Biçimi", "Genişletilebilir Stil Sayfası Dili"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XSLFO",
  "description":"XSLFO dosya formatı ve XSLFO dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "XSLFO",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## XSL-FO dosyası nedir? ##

XSL-FO (XSL Biçimlendirme Nesneleri), XML belgelerini biçimlendirmek için güçlü bir stil sayfası dilidir. Sınırlı kağıt formunun ve baskının semantiği, boyutlar sabitlendiğinde XSL-FO ile ifade edilir. Değişken boyutlara sahip bir tarayıcı penceresinin sınırsız biçiminin anlamını temsil eden HTML'nin aksine. XSL-FO tarafından biçimlendirilen XML belgeleri çoğunlukla PDF dosyaları oluşturmak için kullanılır. XSL (Genişletilebilir Stil Sayfası Dili), XML belgelerini ve bu dilin XSL-FO bölümünü biçimlendirmek ve değiş tokuş etmek için tasarlamayı amaçlayan bir dizi özellikli W3C teknolojisidir. XSLT ve XPath da XSL'nin diğer parçalarıdır.

XML belgelerinin öncelikle XSL-FO'ya dönüştürülmesi önerilmiştir, PDF bu kritere bir örnektir. PDF'de, sonuçlar önce XSLT ve ardından XSL-FO biçimlendirici kullanılarak işlenir. Bu şekilde, XML belgeleri rastgele biçimlendirilebilir. XSL-FO, Basamaklı Stil Sayfası (CSS) özelliklerini kullanmanın ve bunları gerçek format için gerektiğinde genişletmenin avantajını kullansa da, XSL-FO terminolojisinde ana sayfalar olarak adlandırılan sayfa şablonlarının sağlanmasını barındırır. XSL-FO ayrıca oldukça karmaşık belgeler için biçimlendirme sağlar ve dizin oluşturmayı destekler.

## Tarih ve Temel Kavramlar ##

Ocak 2012'de XSL-FO Çalışma Taslağı son kez güncellendi ve Kasım 2013'te Çalışma Grubu kapatıldı. Bir XSL stil sayfası, sınıfın bir örneğinin biçimlendirme sözlüğünü kullanan bir XML belgesine nasıl dönüştürüldüğünü açıklayarak bir XML belgeleri sınıfının sunumunu belirtir. XSL-FO, entegre bir sunum dilidir ve HTML'de kullanılan anlamsal işaretlemelere sahip değildir. Ayrıca bu dil, harici bir HTML veya XML belgesinin varsayılan ayarlarını değiştiren CSS'nin aksine, belgenin tüm verilerini kendi içinde saklar.

XSL-FO kullanmanın genel kriteri, kullanıcının bir belgeyi FO'da yazmak yerine bir XML dilinde yazmasıdır. Bundan sonra bir XSLT dönüşümü gerçekleşir. Bu XSLT dönüşümü, XML'in XSL-FO'ya dönüştürülmesinden sorumludur. XSL-FO belgesi oluşturulur oluşturulmaz, FO işlemcisi adı verilen bir uygulamaya teslim edilir. FO işlemcileri, bu belgeyi hem okunabilir hem de yazdırılabilir bir belgeye dönüştürmekten sorumludur. PDF dosyaları veya PS, XSL-FO'nun en yaygın çıktılarına örnektir. Ancak bu, FO işlemcisinin yalnızca bu iki tür formatı çıktı olarak üretebileceği anlamına gelmez. Bazı FO işlemcileri RTF dosyalarında çıktı alabilir veya hatta kullanıcının GUI'sinde bir pencere görünebilir, bu pencere sayfanın sırasını ve içeriklerini görüntüler.

Bir XSL-FO belgesi, bir PDF veya PS'den farklıdır, sonuçta farklı sayfalardaki metin düzenini tanımlamaz. Belki de sayfaları biçimlendirir ve içeriğin görüntüleneceği yerleri belirler. Ayrıca, bir FO işlemcisi, FO belgesi tarafından belirtilen sınırlar dahilinde metni düzenler. Bu spesifikasyon, farklı FO işlemcilerinin sonuçta oluşturulan sayfalara göre davranmasına bile izin verir. Bu tür davranışlara bir örnek hecelemedir, birkaç FO işlemcisi bir satır kesildiğinde yer kazanmak için sözcükleri heceleyebilirken, bazı işlemciler bu seçeneği seçmez. Gereksinimlerine uyan farklı heceleme algoritmalarını seçmek işlemcilere bağlıdır. Bu heceleme algoritmaları çok basit veya belki daha karmaşık olabilir. Bazı durumlarda, XSL-FO spesifikasyonu, düzen bağlamında bir dereceye kadar tercih edilen FO işlemcilerini açıkça onaylar.

FO işlemcileri arasındaki bu çeşitlilik, işlemcilerin genellikle ilgisiz kaldığı çeşitli sonuçlar üretir. Çünkü XSL-FO'nun genel odak noktası sayfalanmış/basılı belgeler üretmektir. XSL-FO belgelerinin kendileri tipik olarak aracı görevi görür, ana işlevleri ya PDF dosyaları ya da dağıtılacak çıktı olarak yazdırılabilecek bir belge oluşturmaktır. HTML/CSS veya XSL-FO'da, biçimlendirme dilini girmek yerine nihai sonuç olarak PDF'yi dağıtmak, alıcıların biçimlendirme dilini yorumlayanlar arasındaki farklılıklar nedeniyle ortaya çıkan çok yönlülükten etkilenmediğini gösterir. Öte yandan, bir belgenin, örneğin değişken sayfa boyutu veya istenen yazı tipi boyutu veya sayfa veya baskıya göre uyarlama gibi alıcıların farklı ihtiyaçlarını karşılamasının kolay bir yolu olmadığı açıktır.

## XSLFO Dosya Biçimi ##

SL-FO belgeleri temel olarak XML belgeleridir, ancak herhangi bir şema izlemezler. Onun yerine, SL-FO belgeleri kendi dillerinin belirtiminde tanımlanan sözdizimini takip eder. Her XSL-FO belgesinde gerekli olan iki bölüm vardır:

1. Etiketli sayfa düzenlerinin listesini belirten bir bölüm.
1. Çeşitli sayfa düzenleri aracılığıyla içeriğin farklı sayfalarda görüntülenmesini belirleyen, işaretlemeli, belge verilerinin tüm ayrıntılarını içeren bir bölüm.

Sayfanın özellikleri, belirli bir dilin kurallarına uymak için metnin organizasyonunu tanımlayabilen sayfa düzenlerinde belirtilmiştir. Ayrıca, sayfanın boyutu, kenar boşlukları ve (tek ve çift sayfalar için farklı özellikleri onaylayan) sayfa dizileri de sayfa düzenleri tarafından tanımlanır.

Belgenin veri kısmı, her akışın bir sayfa düzenine bağlı olduğu bir dizi akışa bölünmüştür. Akışlar, içlerindeki blokların bir listesini içerir. Bu blok listesi, satır içi işaretleme özelliklerini veya bir metin verisi listesini veya belki her ikisini aynı anda içerebilir. Belgenin kenar boşluklarında sayfa numaraları veya bölüm başlıkları da görüntülenebilir. Hem blokların hem de satır içi öğelerin işlevselliği CSS'deki ile aynı kalır, ancak bazı dolgu ve kenar boşluğu kuralları FO ve CSS arasında farklıdır.

Sayfa yönlendirme yönü tamamen blokların ve satır içi uzantılar için belirtilmiştir, böylece FO belgelerinin İngilizce'den farklı dillerde çalışmasını sağlar. FO belirtiminin dili, yön açıklaması için sol ve sağ yerine başlangıç ve bitiş sözcüklerini kullanır. XSL-FO'nun temel içerik biçimlendirme ve basamaklandırma kuralları CSS'den alınmıştır. XSL-FO'nun dili aşağıdaki belirtimleri kabul eder.

## Birden çok sütun ##

Bir sayfada birden çok sütun ve blok olabilir ve varsayılan olarak bir sütundan diğerine genişleyebilir. Birden çok sayfanın farklı genişliklere ve sütun sayılarına sahip olmasına izin verilir. Tüm FO özellikleri, çok sütunlu bir sayfanın sınırlarını takip eder.

### Listeler ###

Bir XSL-FO listesi, yan yana dizilmiş iki set blok tarafından oluşturulur. Kavramsal olarak, bir listede soldaki blok bir sayıyı, madde işaretini veya metin dizisini gösterirken sağ taraftaki blok beklendiği gibi çalışabilir. XSL-FO listelerinin numaralandırılması genellikle XSLT tarafından yapılır.

### Tablolar ###

Bir FO tablosu, bir HTML/CSS tablosuna benzer. Kullanıcı, her bir hücre için veri satırlarını, stil bilgilerini, arka plan rengini seçebilir. Kullanıcı, farklı stil bilgilerini kullanarak ilk satırı tablo başlık satırı olarak seçme ayrıcalığına sahiptir. FO işlemcisi, her sütunun alan belirtimi hakkında açıkça bilgilendirilebilir veya metni tabloya otomatik olarak sığdırabilir.

### İndeksleme ###

XSL-FO 1.1, uygun şekilde işaretlenmiş öğelere atıfta bulunarak bir dizin oluşturmaya yardımcı olan özelliklere sahiptir.

### Faydalar ###

* İçerik tabanlı yayıncılığa uygun
* Kullanım kolaylığı
* Düşük maliyetli

## Referanslar ##

* [XSL-FO nedir?](https://www.xml.com/articles/2017/01/01/what-is-xsl-fo/)
* [XSL Biçimlendirme Nesneleri](https://en.wikipedia.org/wiki/XSL_Formatting_Objects)

