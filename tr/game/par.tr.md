{
"tarih":"2023-07-18",
   "keywords":[
"PAR",
"PAR Dosyası",
"dosya",
"PAR dosya uzantısı",
"eklenti",
"dosya"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"false",
"toc": true,
"title":"PAR Dosya Formatı - FMS Uçak Parametreleri Dosyası",
   "description":"PAR dosyalarını oluşturabilen ve açabilen PAR formatı ve API'ler hakkında bilgi edinin.",
"linktitle":"PAR",
   "menu":{
      "docs":{
         "identifier":"game-par",
         "parent":"game"
}
},
"lastmod":"2023-07-18"
}

## PAR dosyası nedir?

Yaygın olarak uçak parametreleri dosyası olarak bilinen bir PAR dosyası, özellikle Windows işletim sistemleri için tasarlanmış bir uçuş simülasyon oyunu olan FMS (Flying-Model-Simulator) tarafından kullanılır. Amacı, kütle, ağırlık merkezi ve atalet momentleri gibi özellikler de dahil olmak üzere bir uçağın geometrisi ve fiziksel özelliklerine ilişkin önemli verileri depolamaktır. Bu PAR dosyaları, oyun içinde özelleştirilmiş uçakların oluşturulmasında etkili olup, oyuncuların kendi benzersiz sanal uçaklarını doğru ve gerçekçi fizikle simüle etmelerine ve uçurmalarına olanak tanır.

## PAR Dosya Formatı - Daha Fazla Bilgi

FMS, uçaklarda navigasyon, uçuş planlaması ve otopilot fonksiyonlarına yardımcı olmak için kullanılan bir yazılım sistemidir. Genellikle PAR dosyası olarak kısaltılan FMS Uçak Parametreleri Dosyası, uçağın performans özelliklerine ve uçuş yönetimine ilişkin spesifik verileri içerir.

Bu PAR dosya formatı, Microsoft Flight Simulator veya X-Plane gibi popüler uçuş simülatörü programlarında kullanılanlar gibi uçuş simülasyon yazılımlarına özeldir. Dosya, simülatör içindeki sanal uçağın davranışını, performansını ve sistemlerini tanımlayan çeşitli parametreler ve veriler içerir.

FMS Uçak Parametreleri Dosyası genellikle aşağıdaki gibi bilgileri içerir:

- **Uçak özellikleri:** Bu, uçağın ağırlığı, boyutları, yakıt kapasitesi ve motor özellikleri gibi fiziksel özelliklerine ilişkin ayrıntıları içerir.

- **Uçuş performans verileri:** Tırmanma, seyir, alçalma ve iniş dahil olmak üzere uçuşun farklı aşamalarında uçağın performansına ilişkin verileri içerir. Bu, tırmanma oranlarını, yakıt tüketim oranlarını, hız sınırlamalarını ve performansla ilgili diğer parametreleri içerebilir.

- **Otomatik pilot ayarları:** Dosya, otomatik pilot modları, irtifa ve yön kısıtlamaları ve kontrol hassasiyetleri dahil olmak üzere hava aracına ilişkin otomatik pilot davranışını ve sınırlamalarını belirtebilir.

- **Navigasyon verileri:** Yol noktaları, hava yolları ve havaalanı verileri de dahil olmak üzere uçağın navigasyon veri tabanı gibi navigasyonla ilgili parametreleri içerebilir.

Bu PAR dosyaları genellikle, uçuş simülatörü yazılımı içerisinde gerçekçi ve doğru simülasyon deneyimleri sağlamayı amaçlayan uçak geliştiricileri veya üçüncü taraf meraklıları tarafından oluşturulur ve korunur. Dosyalar daha sonra simüle edilen uçağın davranışını ve performans özelliklerini tanımlamak için simülatöre yüklenir.

## Uçuş Simülasyon Oyunlarında PAR Dosyalarının, 3D Modellerin, Dokuların ve Seslerin Rolü

PAR dosyaları genel uçak veri paketinin yalnızca bir parçasıdır. PAR dosyalarına ek olarak, oyun içinde bir uçağın eksiksiz temsiline toplu olarak katkıda bulunan başka dosyalar da vardır. Bu ek dosyalar genellikle 3B model dosyalarını, doku bit eşlemlerini ve sesleri içerir.

- **3D Model Dosyaları:**

Uçuş simülasyon oyunları, uçağı sanal ortamda görsel olarak temsil etmek için ayrıntılı 3 boyutlu modeller gerektirir. Bu 3 boyutlu modeller, uçağın gövdesi, kanatları, iniş takımları ve diğer karmaşık parçaları gibi çeşitli bileşenlerden oluşur. 3D model dosyaları, oyundaki uçağın görünümünü ve şeklini doğru bir şekilde tasvir etmek için gerekli görsel yapıyı ve geometriyi sağlar.

- **Doku Bitmap'leri:**

Dokular veya görüntü eşlemleri olarak da bilinen doku bit eşlemleri, 3B modellere renk, yüzey ayrıntısı ve görsel gerçekçilik eklemek için kullanılır. Bu doku dosyaları boya şemaları, çıkartmalar, logolar ve metal, plastik veya kumaş gibi yüzey dokuları gibi bilgileri içerir. 3D modellere doku bit eşlemleri uygulanarak oyundaki uçak görsel olarak iyileştirilebilir, bu da daha sürükleyici ve görsel olarak çekici bir deneyime yol açar.

- **Sesler:**

Ses dosyaları, işitsel geri bildirim ve gerçekçilik sağladıkları için uçuş simülasyon oyunlarının önemli bir unsurudur. Bu dosyalar genellikle motor seslerini, kokpit seslerini, rüzgar veya yağmur gibi çevresel efektleri ve uçağa özgü diğer ses ipuçlarını içerir. Oyun, uygun ses dosyalarının dahil edilmesiyle, simüle edilen uçakla ilişkili ses ortamını doğru bir şekilde yeniden oluşturabilir ve genel sürükleyiciliği daha da artırabilir.

PAR dosyası, uçağın performansı ve uçuş yönetimi ile ilgili belirli verileri içerse de, uçuş simülasyon oyunu içinde sanal uçağa topluca hayat veren PAR dosyaları, 3D model dosyaları, doku bitmap'leri ve ses dosyalarının birleşimidir. Her dosya, uçağın kapsamlı ve gerçekçi bir temsilini oluşturmada benzersiz bir amaca hizmet ederek oyuncular için sürükleyici bir deneyim sağlar.

## PAR dosyası nasıl açılır?

PAR dosyalarını açan programlar şunları içerir:

- Uçan Model Simülatörü (FMS)
- Microsoft Uçuş Simülatörü
- X-Düzlemi

## Referanslar
* [Uçan Model Simülatörü (FMS)](https://modelsimulator.com/)
* [Microsoft Uçuş Simülatörü](https://en.wikipedia.org/wiki/Microsoft_Flight_Simulator)


