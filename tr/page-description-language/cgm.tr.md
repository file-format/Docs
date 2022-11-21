{
  "date" : "2019-10-11",
  "keywords" :[ "CGM", "Bilgisayar Grafikleri Meta Dosyası", "Dosya", "Uzantı", "Dosya Formatı", "Vektör Grafikleri", "Meta Dosyası Tanımlayıcı"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CGM Dosya Biçimi",
  "description":"CGM dosya formatı ve CGM dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "CGM",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## .cgm dosyası nedir? ##

Bilgisayar Grafikleri Meta Dosyası (CGM), vektör grafikleri (2B), raster grafikleri ve metni depolamak ve değiş tokuş etmek için ücretsiz, platformdan bağımsız, uluslararası standart bir meta dosyası biçimidir. CGM, görüntü üretimi için nesne yönelimli bir yaklaşım ve birçok işlev provizyonu kullanır. CGM, bir görüntüyü oluşturmak için grafik öğeleri yeniden kalıplamak için bu nesne yönelimli özellikleri kullanır. Bir meta dosyası, diğer dosyaları tanımlayan gerekli bilgileri içerir. CGM'de, metin tabanlı bir kaynak dosya, daha sonra bir ikili dosyada derlenebilecek tüm grafik öğeleri içerir. Temel olarak CGM, herhangi bir platformdan veya cihazdan bağımsız olarak 2B grafik veri alışverişini kolaylaştırmanın bir yoludur.

CGM formatı, işlevleri gerçekleştirmek için farklı öğeler sağlar ve geometrik ilkelleri ve grafik bilgileri ayarlamak için nesneleri belirtir. Web sayfaları tarafından iyi desteklenmediği için web sayfalarında grafik sanatları görüntülemek için CGM'nin yerini başka biçimler almış olsa da, endüstriyel, havacılık ve diğer teknik uygulamalar arasında hala çok popülerdir. World Wide Web Konsorsiyumu, Web'de CGM kullanımına alternatif bir yaklaşım olan WebCGM'yi geliştirmiştir. Birincil CGM uygulaması, Grafik Çekirdek Sisteminin (GKS) temel işlemleri dizisinin bir gösterimiydi. Profesyonel tasarımlarda pek benimsenmedi, ancak yerini büyük ölçüde DXF ve SVG gibi diğer formatlar aldı.

## Tarih ##

CGM, 1987'de uluslararası bir standart haline geldi (ISO 8632-1987) ve ayrıca İngiltere'de BSI ve ABD'de ANSI tarafından ulusal bir standart olarak kabul edildi. 1991'deki bir dizi değişiklikten sonra, 1992'de gözden geçirilmiş bir CGM standardı yayınlandı (ISO 8632:1992). 2001 yılında, World Wide Web Konsorsiyumu, web sayfalarıyla birlikte kullanılmak üzere gelişmiş kapasiteye sahip WebCGM'yi geliştirdi. 2007'de WebCGM'nin ikinci versiyonu piyasaya sürüldü ve üçüncü versiyonu 2010'da gelişmiş yeteneklerle piyasaya sürüldü.

## CGM Dosya Biçimi ##

Bilgisayar grafiği meta dosyaları temel olarak grafik bilgi için veri tabanıdır ve grafik verinin yakalanması, saklanması ve iletilmesi için araçlar sağlar. Sonuç olarak, bir uygulamanın bir meta dosyası biçiminde yürütülmesi ile birlikte veritabanını aynı anda oluşturmak için bir grafik sistem bileşeni olmalıdır. Çoğu durumda, bu bileşen Meta Dosya oluşturucusudur. Bunun yanı sıra, bir meta dosyasındaki grafik verileri getirebilen, yorumlayabilen ve işleyebilen başka bir bileşene ihtiyaç vardır. Bu ihtiyaç, bir meta dosyası yorumlayıcısının varlığıyla karşılanır. Aşağıdaki şekilde, grafiksel meta dosyası çalışma ortamı gösterilmektedir.

CGM'nin tipik bir grafik sisteminin diğer bileşenleri ile ilişkisi yukarıdaki şekilde gösterilmektedir. Meta dosyasının işlevselliğinin nihai aygıt çıktısına bağlı olmadığı da şekilden açıkça görülmektedir.

Genellikle iki meta dosyası kategorisi vardır: **bölüm yakalama** ve **resim yakalama**. Resim yakalama meta dosyasının birincil işlevi, cihazdan bağımsız, çoklu resim tanımlarının yakalanmasıdır. Oturum yakalama meta dosyaları, bir grafik sistemdeki çıktı diyaloğunu yakalamak için sistem arayüzünü kullanır. CGM, statik resim yakalama meta dosyaları kategorisine aittir. CGM, iki seviyeli bir yapıya sahip bileşenlerin iyi organize edilmiş bir düzenlemesini sağlar.

1. Meta dosya tanımlayıcısı
1. Mantıksal olarak bağımsız görüntülerden oluşan bir havuz

Her resim, bir resim tanımlayıcıları koleksiyonu ve bir resim tanımı içeren bir resim gövdesidir. meta dosyası tanımlayıcısı, o meta dosyasının tüm resimlerine eşit şekilde uygulanan tanımlayıcı bilgileri tanımlar. Bu bilgi, yorumlayıcının bir meta dosyasını doğru bir şekilde ayrıştırmasına ve bir resmin doğru şekilde işlenmesi için gereken kaynakları tanımasına yardımcı olur. Resim tanımlayıcı aynı zamanda tanımlayıcı bilgileri içermesine rağmen, yalnızca tanımlayıcının bulunduğu resmi tanıyabilir. Bu dosya biçiminde, her bir resim tanımı bağımsızdır ve mantıksal olarak bağımsızdır. Bir dosyadaki diğer tüm resim tanımlarından bağımsızdırlar. Meta-tanımlayıcının yorumlanmasından hemen sonra, resimlere rastgele erişilebilir ve yorumlanabilir. Önceki resimlerin durumundaki değişiklik, onların haleflerini etkilemez. Bu resim bağımsızlığı, CGM.CGM'nin öne çıkan diğer bir özelliğidir. Sanal aygıt koordinatları olarak adlandırılan 2B Kartezyen koordinatlar olan ve aralığı ve ayrıntıyı temsil eden sayı veya kesinlik yoluyla temsil edilebilen koordinatlar alanından oluşur. CGM, hem doğrudan renk seçimini hem de indeks tabanlı seçimi belirtir. İlkinde, renk belirtici bir RGB üçlüsünden oluşurken, daha sonra renk belirtici bir renk tablosuna bir dizin gösterir.

CGM matches the needs of both communication-dependent as well as performance-dependent applications. Centralized and distributed graphics systems can use CGM in an unlimited number of ways.  It can be tailored to access graphics devices using a spooling system.
