{
"tarih":"2023-07-18",
   "keywords":[
"PAR",
"PAR Dosyası",
"par dosyası nasıl açılır",
"dosya",
"PAR dosya uzantısı",
"eklenti",
"dosya"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"false",
"toc":true,
"title":"PAR Dosya Formatı - Arşiv Dizin Dosyası",
   "description":"PAR dosyalarını oluşturabilen ve açabilen PAR formatı ve API'ler hakkında bilgi edinin.",
"linktitle" : "PAR",
   "menu":{
      "docs":{
         "identifier":"compression-par",
         "parent":"compression"
}
},
"lastmod":"2023-07-18"
}

## PAR dosyası nedir?

Parchive (PAR) arşivleri içinde, bir .par dosyası, bir grup eşlik birimi veya eşlik bloğu içeren bir dizin dosyasına başvurur. Bu indeks dosyası, arşivdeki bir veya daha fazla dosya kaybolduğunda veya hasar gördüğünde hata tespiti ve kurtarma amacıyla kullanılır.

Bir Parchive arşivi genellikle hem orijinal veri dosyalarından hem de karşılık gelen eşlik birimlerinden oluşur. Eşlik hacimleri, Reed-Solomon hata düzeltme algoritmaları kullanılarak oluşturulur. Bu eşlik birimleri, orijinal veri dosyalarını kurtarmak için kullanılabilecek yedek bilgiler içerir.

Eşlik birimi kümesi olarak da bilinen .par dosyası, arşiv içindeki eşlik birimlerinin yapısı ve konumu hakkında bilgiler içerir. Kurtarma işlemi için bir dizin veya harita görevi görür. Özel PAR yazılımı, .par dosyasını kullanarak hangi eşlik birimlerinin gerekli olduğunu ve eksik veya hasarlı dosyaları yeniden oluşturmak için bunların nasıl kullanılması gerektiğini belirleyebilir.

Parchive arşivindeki bir veya daha fazla dosya erişilemez veya bozulduğunda, .par dosyası, kayıp verileri kurtarmak için mevcut eşlik birimleriyle birlikte kullanılabilir. PAR yazılımı .par dosyasını okur, eksik veya hasarlı dosyaları tanımlar ve bunları yeniden oluşturmak için eşlik birimlerini kullanır.

## PAR dosyası nasıl açılır?

.par dosyalarını açmak ve kullanmak için özel PAR yazılımına ihtiyacınız olacaktır. .par dosyalarını işleyebilen birkaç popüler yazılım seçeneği şunlardır:

- **QuickPar:** QuickPar, Windows için yaygın olarak kullanılan bir PAR yazılımıdır. PAR dosyalarını oluşturmanıza, doğrulamanıza ve onarmanıza olanak tanır. Bütünlüğünü doğrulamak için bir .par dosyasını QuickPar'da açabilir veya Parchive arşivindeki hasarlı veya eksik dosyaları onarmak için kullanabilirsiniz.

- **MultiPar:** MultiPar, Windows için kullanılabilen bir başka popüler PAR yazılımıdır. Hem PAR hem de PAR2 dosya formatlarını destekler ve arşivlerin oluşturulması, doğrulanması ve onarılması için gelişmiş özellikler sağlar. MultiPar, .par dosyalarını açabilir ve sağlanan eşlik birimlerine göre hata algılama ve kurtarma işlemlerini gerçekleştirebilir.

- **MacPAR deLuxe:** MacPAR deLuxe, macOS için özel olarak tasarlanmış bir PAR yazılımıdır. PAR ve PAR2 dosya formatlarını destekler ve QuickPar ve MultiPar ile benzer işlevsellik sağlar. MacPAR deLuxe, .par dosyalarını açabilir ve arşivlerin doğrulanmasına ve hasarlı veya eksik dosyaların kurtarılmasına yardımcı olabilir.

## PAR Dosya Formatı - Daha Fazla Bilgi

Yaygın olarak Parchive olarak adlandırılan PAR dosya formatı, eşlik verileri oluşturmak ve dosya arşivlerinde hata tespiti ve kurtarma işlemini gerçekleştirmek için kullanılan özel bir dosya formatıdır. PAR dosya formatı tipik olarak üç türden oluşur: PAR, PAR2 ve PAR3.

- **PAR:** PAR1 olarak da bilinen orijinal PAR dosya formatı Parchive projesi tarafından geliştirilmiştir. Orijinal veri dosyalarından oluşturulan eşlik verilerini içerir. PAR dosyaları, temel düzeyde hata algılama ve kurtarma sağlar ancak hata düzeltme yetenekleri açısından sınırlamalara sahiptir.

- **PAR2:** PAR2, PAR dosya formatının geliştirilmiş bir sürümüdür. Daha gelişmiş hata düzeltme yetenekleri ve gelişmiş kurtarma özellikleri sunar. PAR2 dosyaları genellikle bir arşivdeki kayıp veya hasar görmüş dosyaları kurtarabilen eşlik verileri oluşturmak için kullanılır. PAR2 dosyaları veri bozulmasına karşı daha iyi koruma sağlar ve dosya arşivleme amacıyla yaygın olarak kullanılır.

- **PAR3:** PAR3, PAR dosya formatının en son sürümüdür ve hata düzeltme ve kurtarma konusunda daha fazla iyileştirme sağlar. PAR2'ye kıyasla daha yüksek seviyelerde artıklık ve hata düzeltme yetenekleri sunar. PAR3 dosyaları, arşivlerde saklanan veriler için daha sağlam koruma ve kurtarma seçenekleri sağlamak üzere tasarlanmıştır.

Hem PAR2 hem de PAR3 dosya formatları, PAR yazılımı tarafından geniş çapta desteklenir ve bir arşiv içindeki dosyaların bütünlüğünü doğrulama ve kaybolan veya hasar gören verileri kurtarma olanağı sunar. PAR ve PAR2 dosyaları hala yaygın olarak kullanılırken, PAR3 dosyaları gelişmiş hata düzeltme yetenekleri nedeniyle giderek benimsenmektedir.

## Referanslar
* [Parşiv](https://en.wikipedia.org/wiki/Parchive)

