{
  "date" : "2021-01-22",
  "keywords" :[ "ASE","dosya", "biçim", "dosya türü", "uzantı","ASE dosyası nedir?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"ASE dosya formatı ve ASE dosyalarını açıp oluşturabilen API'ler hakkında bilgi edinin.",
  "title" :"ASE - Autodesk ASCII Sahne Dışa Aktarma Dosyası",
  "linktitle" : "ASE",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-01-22"
}

## ASE dosyası nedir?

.ase uzantılı bir dosya, sahne verilerini Autodesk kullanarak dışa aktarırken 2B veya 3B bilgileri içeren, bir sahnenin ASCII temsili olan bir Autodesk ASCII Sahne Dışa Aktarma dosya biçimidir. Autodesk, sahne verilerini dışa aktarırken sahne bileşenlerini dahil etmek için seçenekler sunar. Tepe noktası ve yüz bilgisi, Malzeme açıklaması, nesneler için dönüşüm animasyonu verileri, her n karenin tam ağ tanımı, kameralar ve ışıklar için animasyon verileri ve IK ortak ayarları ile birlikte Kafes tanımını dahil edebilirsiniz.

## ASE Dosya Biçimi - Daha Fazla Bilgi

ASE dosyaları, herhangi bir metin düzenleyicide açılabilen ASCII biçiminde saklanan metin dosyalarıdır. Bir ASE dosyası, Autodesk tarafından sağlanan aşağıdaki bilgi türlerini içerebilir.

### Çıktı Seçenekleri

* `Mesh Definition` - Geometrik nesneler için köşe ve yüz bilgileri dahil olmak üzere her bir ağın tanımını dışa aktarır. Ek olarak, bunu açmak, aşağıda açıklanan Kafes Seçenekleri grup kutusundaki öğeleri etkinleştirir.
* `Malzemeler` - Malzeme açıklamasını içerir. Bir nesneye bir malzeme atanmamışsa, telkafes rengi dışa aktarılır. Bir malzeme ağacının tüm seviyeleri dahil edilmiştir, dolayısıyla bu çok fazla metin üretebilir.
* `Transform Animation Keys` - Nesneler için transform animasyon verilerini içerir. Nesne bir hedef kamera veya spot ışığıysa bu, hedef animasyon verilerini içerecektir.
* `Animated Mesh` - Her n karenin eksiksiz bir ağ tanımını dışa aktarır. Frekans, aşağıda açıklanan Denetleyici Çıkış döndürücü tarafından belirlenir. Her blok, aşağıda açıklanan Kafes Seçenekleri grup kutusunda belirtilen bilgilerin aynısını içerir. Bunu açmak, küçük sahneler için bile büyük bir dosyaya neden olabilir.
* `Animasyonlu Kamera/Işık Ayarları` - Kameralar ve ışıklar için renk, yoğunluk, sapma, harita sapması vb. gibi animasyon verilerini dışa aktarır. Denetleyici Çıktı döndürücü tarafından belirtildiği gibi, her n karede bir blok çıkarır.
* `Ters Kinematik Eklemler` - Hiyerarşi dalındaki IK eklem ayarlarını dışa aktarır.

### Nesne Türleri

Buradaki öğeler, çıktıya dahil edilmesini istediğiniz nesne kategorisini belirlemenizi sağlar. Geometrik nesneleri, şekilleri, kameraları, ışıkları ve yardımcı nesneleri dahil edebilirsiniz.

* Geometrik
* Şekiller
* Kameralar
* Işıklar
* Yardımcılar

### Kafes Seçenekleri

* `Mesh Normalleri` - Yüz ve köşe normallerini dışa aktarır. Önce yüzün normali, ardından yüzü destekleyen üç köşenin normalleri listelenir. Bunu açmak çok daha büyük bir dosyayla sonuçlanır.
* 'Eşleme Koordinatları' - 3ds Max Yazılım Geliştirme Kitinde açıklanan TVert ve TVFace yapılarına göre eşleme köşeleri ve yüzlerinin bir listesini dışa aktarır. Bir nesne yüz eşleme kullanıyorsa, her yüz için UVW koordinatlarını içeren bir yüz haritası listesi dışa aktarılır.
* `Köşe Renkleri` - Köşe renklerini dışa aktarır.

### Denetleyici Çıkışı

* `Anahtarları Kullan` - Anahtar değerleri dışa aktarır. Denetleyici tuşları kullanmıyorsa Force Sample yöntemi kullanılır. Dönüştürme denetleyicileri söz konusu olduğunda, Anahtarları Kullan seçeneği yalnızca tüm dönüştürme denetleyicileri Doğrusal/TCB veya Bezier ise çalışır. Dönüşüm izlerinden biri farklı türde bir denetleyici kullanıyorsa, tüm dönüşüm izleri için Force Sample yöntemi kullanılır.
* `Force Samples` - Örnek Denetleyici Başına Çerçevelerde belirtilen frekansa göre denetleyici değerlerini örnekler.

## Referanslar

* [Autodesk - ASCII'ye Aktarma](https://help.autodesk.com/view/3DSMAX/2020/ENU/?guid=GUID-98B2388D-A3A7-4096-8E81-888A3F9D6069)

