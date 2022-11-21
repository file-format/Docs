{
  "date" : "2019-12-12",
  "keywords" :[ "JT", "dosya", "uzantı", "biçim", "3D fbx", "" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"JT dosya formatı ve JT dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"JT - Jüpiter Mozaik Dosya Formatı",
  "linktitle" : "JT",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## .JT dosyası nedir?

**JT** (Jüpiter Tessellation), Siemens PLM Software tarafından geliştirilen verimli, endüstri odaklı ve esnek, ISO standardize edilmiş bir 3D veri formatıdır. Havacılık, otomotiv endüstrisi ve Ağır Ekipmanın mekanik CAD alanları, en önde gelen 3D görselleştirme formatı olarak JT'yi kullanır.

JT formatı, CAD'e özgü nitelikleri ve düğümleri destekleyen bir sahne grafiğidir. Yön verilerini (üçgenler) depolamak için gelişmiş sıkıştırma teknikleri kullanılır. Bu biçim, görsel nitelikleri, ürün ve üretim bilgilerini (PMI) ve Meta verileri destekleyecek şekilde yapılandırılmıştır. Eşzamansız içerik akışı için iyi bir destek var. Ağır makine endüstrisinde profesyoneller, karmaşık ürünlerin geometrisini incelemek için CAD çözümlerinde ve ürün yaşam döngüsü yönetimi (PLM) yazılım programlarında JT dosyasını kullanır.

JT, neredeyse tüm önemli 3D CAD formatlarını desteklediğinden, montajı "çoklu CAD" olarak bilinen çeşitli kombinasyonlarla başa çıkabilir. Bu çoklu CAD derlemesi her zaman iyi yönetilir ve günceldir, çünkü yerel CAD ürün açıklama dosyaları ile ilişkili JT dosyaları arasında senkronizasyon otomatik olarak gerçekleşir. JT dosyaları orijinal olarak hafiftir, dolayısıyla internet işbirlikleri için uygun kabul edilir. Şirketler, “ağır” orijinal CAD dosyalarına kıyasla medya üzerinden 3D görselleştirmeleri çok daha kolay göndererek işbirliği yaparlar. Ayrıca JT dosyaları, fikri mülkiyet paylaşımını daha güvenli hale getiren birçok güvenlik özelliği sağlar.

## JT Dosya Biçiminin Kısa Tarihi

Engineering Animation, Inc. ve Hewlett Packard, bu formatı Direct Model araç seti olarak geliştiren JT'nin orijinal tasarımcılarıydı. EAI, UGS Corp. tarafından satın alındıktan sonra JT, UGS paketinin bir parçası oldu. 2007'nin başlarında UGS, JT'yi ana 3D formatı olarak duyurdu. Aynı yıl Siemens AG, UGS'yi satın aldı ve Siemens PLM Yazılımı oldu. Siemens, ortak birlikte çalışabilirlik formatı ve veri arşivleme formatı olarak JT'yi kullanır. 2009'da ISO, JT spesifikasyonunu ISO Kamuya Açık Spesifikasyon (PAS) olarak yayınlanmak üzere kabul etti. 2010'un ortalarında ProSTEP iViP, endüstriyel düzeyde JT ve STEP AP 242 XML'in verilerde maksimum avantaj elde etmek için birlikte kullanılabileceğini duyurdu. takas senaryoları 2012 yılında, JT resmi olarak ISO standardize edilmiş (ISO 14306:2012 (ISO JT V1)) 3D görselleştirme formatı olarak ilan edildi.

## JT Dosya Biçimi ##

JT biçimindeki tüm nesneler, bir nesne tanımlayıcısı aracılığıyla temsil edilir ve nesneler arasındaki referanslar, başvurulan nesnenin tanımlayıcısı aracılığıyla işlenir. Bu nesne referanslarının bütünlüğü, işaretçilerin karıştırılması/karıştırılması yoluyla korunabilir.

Bir JT dosyası bir dizi blok olarak düzenlenir ve Başlık bloğu her zaman dosyadaki ilk veri bloğudur. Başlık bloğunu hemen bir dizi veri bölümü ve bir TOC bölümü takip eder. Bir Veri segmenti (6 LSG Segmenti), her zaman var olan bir referans uyumlu JT dosyasına sahiptir. TOC Segmenti, o dosyanın diğer tüm Veri Segmentlerinin konum bilgilerini içerir.

{{< figure src="../JT-1.png" alt="JT Dosya Biçimi" >}}

### Dosya Başlığı ###

Dosya Başlığı, JT dosyasının veri hiyerarşisindeki ilk bloktur. Sürüm oluşturma bilgisi ve TOC konum bilgisi, yükleyicilerin dosya okumasını kolaylaştıran başlık içine alınır. Dosya başlığı içerikleri aşağıdaki gibi düzenlenmiştir.

### TOC Segmenti ###

TOC Segmenti bir dosya içinde bulunmalı ve diğer tüm veri segmentlerinin kimlik ve konum bilgilerini içermelidir. TOC Segmentinin gerçek konumu, dosya başlığının TOC Offset alanı tarafından belirtilir. Ayrı ayrı adreslenebilen her Veri Segmenti, bir TOC segmentindeki TOC girişi ile temsil edilir.

### Veri Segmenti ###

JT dosyası, bir Veri Segmenti içinde saklanan tüm verileri tanımlar. Bazı Veri Segmentleri, segment içinde kalan bilgilerin tüm veri baytlarını sıkıştırabilir. Veri segmentleri aşağıdaki yapıya sahiptir:

![alt text](../JT-2.png "JT Data Segment")

Aşağıdaki tablo, farklı veri segmenti türlerini açıklamaktadır:

|Ad|Açıklama
---|---|
|LSG segmenti|LSG (yönlendirilmiş asiklik grafik yapısı) oluşturmak için yönlendirilmiş referanslar yoluyla bağlanan bir nesneler koleksiyonundan oluşur
|Şekil LOD segmenti|geometrik şekiller için tanımlayıcı verileri içerir (örn. köşeler, normaller, çokgenler, vb.)
|JT B-Rep Segmenti|Verilerin JT B-Rep formatındaki tek bir bölüm için kesin geometrik sınırı temsil etmesi için elemana sahip olmak.
|XT B-Rep segmenti|Sınır gösterimi formatında tek bir bölüm için kesin geometrik sınırı temsil edecek veri elemanına sahip olmak
|Wireframe segmenti|Belirli bir kısım için kesin 3D tel kafesi temsil eden veriler, bu segmentte yer alan bir öğe tarafından tanımlanır.
|Meta Veri segmenti|Meta verileri farklı adreslenebilir segmentlerde depolamaya izin verir.
|JT ULP segmenti|Verilerin, JT ULP biçimindeki ayrı bir bölüm için yarı kesin geometrik sınırı temsil etmesi için öğeye sahip.
|JT LWPA segmenti|Belirli bir parça için analitik verileri tanımlayan bir öğe içerir. LWPA, analitik yüzeyler koleksiyonunu parçanın b-rep tanımına dahil eder.

## Sıkıştırma ##

3B modellerin aktarım ve depolama gereksinimleri daha zordur, bu nedenle JT dosyaları sıkıştırmanın avantajlarından yararlanabilir. Bir JT veri modeli, farklı sıkıştırma teknikleri kullanan farklı dosyalardan oluşabilir, ancak sıkıştırma işlemi JT veri kullanıcısı için şeffaftır.

Şimdiye kadar, JT Open Toolkit (standart olarak) ve gelişmiş sıkıştırma, JT dosyaları tarafından kullanılan iki sıkıştırma tekniğidir. JT Open Toolkit, kolay, kayıpsız bir sıkıştırma algoritması kullanırken, gelişmiş sıkıştırma daha rafine, alana özgü bir sıkıştırma tekniği kullanır ve bu da kayıplı geometri sıkıştırmasına yol açar. Gelişmiş sıkıştırma oldukça yüksek sıkıştırma oranları sağladığından, istemci uygulamaları standart sıkıştırma yerine gelişmiş sıkıştırmayı tercih eder. Sıradan JT dosya görüntüleme uygulamalarıyla geriye dönük uyumluluk, standart sıkıştırmanın sağlanmasıyla sağlanır. Sıkıştırma formu, bir JT dosyası metin düzenleyici kullanılarak açıldığında görülebilen ve ASCII başlık bilgisi içine eklenmiş olan JT dosya formatı sürümüyle uyumlu olmalıdır.

## Referanslar ##

* [JT Dosya Biçimi Referansı](https://www.plm.automation.siemens.com/en_us/Images/JT-v10-file-format-reference-rev-B_tcm1023-233786.pdf)
* [JT (görselleştirme formatı)](https://en.wikipedia.org/wiki/JT_(visualization_format)#Data_model)

