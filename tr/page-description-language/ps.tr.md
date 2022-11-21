{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PS Dosya Biçimi",
  "description":"PS dosya formatı ve PS dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "PS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## .PS dosyası nedir? ##

PostScript (PS), masaüstü ve elektronik yayıncılık işinde kullanılan genel amaçlı bir sayfa tanımlama dilidir. PostScript'in (PS) ana odak noktası, iki boyutlu grafik tasarımı kolaylaştırmaktır. Çoğu dil, kodun yürütülmesinden önce ayrı bir derleme aşaması gerektirirken, Post Script (PS) formatı bir çalışma zamanı doğrudan yorumlamayı destekler. Erken sürümü, Adobe görüntüleme modelinin kurallarına göre basılı sayfalarda veya görüntülenen sayfalarda grafik şekilleri, farklı metin görünümlerini ve modellenmiş görüntüleri tanımlar. Bir PS programı, aygıtı bağımsız ve üst düzeyde tutarak bir belge açıklamasını bir kompozisyon ve yazdırma sistemi arasında karşılıklı olarak iletebilir. Ayrıca bu program, bir ekrandaki metin ve grafiklerin görünümünü de yönetebilir.

PostScript sayfa açıklaması, aygıtın PostScript yorumlayıcısının yardımıyla yazıcıda ve diğer çıktı aygıtında oluşturulabilir, görüntülenebilir. Karakterleri, grafik şekilleri ve görüntüleri yazdırma komutları söz konusu aygıt için yorumlayıcı tarafından yürütülürken, yüksek düzeyli PostScript açıklaması düşük düzeyli raster veri formatına dönüştürülür. Genel olarak, çizerler, belge oluşturma sistemleri ve bilgisayar destekli tasarım (CAD) gibi farklı uygulamalar, PostScript sayfa açıklamaları oluşturmak için otomatikleştirilir. Genel olarak programcılar, yeni uygulamalar oluştururken PostScript programları yazmak zorundadır. Ancak bir programcı, PostScript dilinin herhangi bir uygulamada erişilemeyen yeteneklerinden, o özel durum için bir PS programı yazarak yararlanabilir.

## Kısa Tarih ##

PostScript dili kavramı ilk olarak John Warnock tarafından tanıtıldı. 1966'da New York Limanı projesi üzerinde çalışıyordu. O projenin veri tabanı için büyük bir üç boyutlu grafik için bir tercüman geliştirmeye çalışıyordu. John Warnock, bu grafikleri işlemek için Tasarım Sistemi dilini tasarladı. Bu arada Xerox PARC, ilk lazer yazıcıları için sayfa görüntülerini tanımlamanın standart bir yolunu arıyordu. Bob Sproull ve William Newman 1975-76'da lazer yazıcıları çalıştırmak için Press formatını (veri formatı) geliştirmiş olsa da, daha fazla esneklik için bir dile ihtiyaç vardı. 1978'de Warnock, Xerox PARC'ta Martin Newell'e katıldı ve daha sonra büyütülen ve Interpress diline genişletilen yorumlama dili JaM'i yeniden yazdı. Warnock, Adobe Systems'ı Aralık 1982'de Chuck Geschke, Doug Brotz, Ed Taft ve Bill Paxton ile birlikte kurdu. 1984'te ticari olarak piyasaya sürülen Interpress'e benzer PostScript adlı daha basit bir dil üzerinde çalışmaya başladılar. Apple'dan Steve Jobs onları ziyaret etti ve PostScript'i lazer yazıcıları çalıştıracak şekilde uyarlamalarını tavsiye etti.

Mart 1985'te, yerleşik bir PostScript yorumlayıcısına sahip ilk yazıcı, masaüstü yayıncılıkta (DTP) devrim yaratan Apple'ın LaserWriter ürünüydü. Teknik sağlamlık ve yaygın kullanılabilirlik, PostScript'i masaüstü ve elektronik yayıncılık için tercih edilen bir dil haline getirdi. 1990'da, PostScript dili için bir tercüman, lazer yazıcıların önemli bir parçasıydı.

## Ana Özellikler ##

PostScript dilinin etkileşimli grafikler ve sayfa açıklamalarıyla başa çıkma yetenekleri aşağıdaki özelliklere sahiptir:

**Şekiller:** Doğası gereği rastgele, hem kendi kendine hareket edebilen hem de bağlantısız (bölümlerde ve deliklerde) olabilen düz çizgiler, eğriler, kareler ve kübik eğrilerden oluşabilir.

**Boyama operatörleri:** herhangi bir kalınlıkta, renkte, dolguda şekil taslağına izin verir veya başka herhangi bir grafiğin kırpılmasına izin vermek için şeklin kırpılmış olarak çizilmesine izin verir.

**Renkler:** gri tonlama, RGB, CMYK ve CIE gibi çeşitliliğe sahiptir. Özel renk türleri, farklı özellikler olarak modellenir: spot renkler, renk eşleme, hatta gölgeleme ve yinelenen desenler.

**Metin:** grafiklerle tamamen entegre. Ayrıca, adobe görüntüleme modeli, metin karakterlerinin herhangi bir normal grafik operatörü tarafından çalıştırılabilen grafik şekiller olarak görüntülenmesini sağlar.

**Örnek görüntüler**: orijinal kaynaklardan (taranmış fotoğraflar) çıkarılır veya sentetik olarak üretilebilir. PostScript dili, görüntüleri herhangi bir çözünürlükte ve bir çıktı aygıtındaki farklı renk modellerine göre yeniden oluşturmak için çeşitli araçlar sunar.

Genel amaçlı bir programlama dili, çerçevesine Ps yerleştirerek PostScript dilinin grafik özelliklerinden yararlanabilir. Sayılar, karakterler, diziler ve dizeler gibi ilkel veri türleri; döngüler, prosedürler ve koşullar gibi kontrol ilkelleri; ve sözlükler gibi bazı alışılmadık özellikler dilde belirtilmiştir. Bu özellikler, programcıların daha üst düzey işlemleri başlatmak için komutlar yazmasını kolaylaştırır. Bu üst düzey işlemler, karmaşık uygulama ihtiyaçlarını karşılar. Bu tür bir uygulama, sabit bir dizi temel işlem kullanmaktan çok daha derli toplu ve verimlidir.

PostScript'te yazılan programlar ASCII kaynak metni biçiminde üretilebilir, iletilebilir ve yorumlanabilir. Bütün dil yazdırılabilir karakterler ve beyaz boşluk şeklinde tanımlanabilir. Bu temsil, programcıların dili kolayca oluşturmasını, manipüle etmesini ve anlamasını destekler. Ayrıca, çeşitli bilgisayarlar ve işletim sistemleri arasında dosya depolama ve aktarım, makine bağımsızlığı sayesinde uygun tutuldu.

Programın PostScript yorumlayıcısına giden tamamen şeffaf bir iletişim yolu olması garanti edildiğinde, dilin ikili kodlanmış biçimleri mümkündür. Adobe, belge alışverişi veya arşiv depolaması için PS programlarının ASCII temsiline sıkı sıkıya bağlı kalmasını tavsiye eder.

## Sürümler ##

PS(.ps), bir PostScript belgesinin dosya uzantısıdır. Birleşik Krallık Ulusal Arşivleri, PostScript dosyasının DSC sürümünde tanımlanan beş kronolojik sürümünü sınıflandırır: sürüm 1.0, 2.0, 2.1, 3.0, 3.1. Her sürüm, önemli yapılandırma açıklamalarını tanımlar. Kapsüllenmiş PostScript Dosyası (EPS), bir dikdörtgen grafiği belirtmek için dili kullanan PostScript dosyasının özel bir alt türüdür. PostScript Dil Referans Kılavuzu, bir EPS'yi şu şekilde tanımlar: "Kapsüllenmiş bir PostScript (EPS) dosyası, diğer uygulamalar tarafından kapsayıcı bir belgeye gömülmek üzere içe aktarılabilen bir biçimde en fazla tek bir sayfayı açıklayan bir PostScript programıdır." Bir PostScript belge dosyası, içindeki bir EPS dosyasını kapsülleyebilir. PostScript'in ek bir kullanımı, Display PostScript (DPS) olarak belirtilir. DPS, PostScript görüntüleme modelini ve dilini kullanan bir grafik motoru aracılığıyla ekran grafikleri oluşturur.

## Referanslar ##

* [PostScript Format Ailesi](https://www.loc.gov/preservation/digital/formats/fdd/fdd000029.shtml)

