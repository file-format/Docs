{
  "date" : "2020-03-16",
  "keywords" :["IFC Dosyası", "Biçim", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"IFC dosya formatı ve IFC dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"IFC Dosya Biçimi",
  "linktitle" : "IFC",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## IFC dosyası nedir?

IFC uzantılı dosyalar, yapı nesnelerini ve bunların özelliklerini içe ve dışa aktarmak için uluslararası standartları belirleyen Industry Foundation Classes (IFC) dosya biçimini ifade eder. Bu dosya biçimi, farklı yazılım uygulamaları arasında birlikte çalışabilirlik sağlar. Bu dosya formatının özellikleri, BuildingSMART International tarafından Veri Standardı olarak geliştirilmiş ve sürdürülmüştür. IFC dosya formatının nihai amacı, bir binanın yaşam döngüsü boyunca iletişimi, üretkenliği, teslimat süresini ve kaliteyi iyileştirmektir.

İnşaat endüstrisindeki ortak nesneler için belirlenmiş standartlar nedeniyle, bir uygulamadan diğerine aktarım sırasında bilgi kaybını azaltır. IFC birçok farklı meslek (mimar, elektrik, HVAC, inşaat, arazi vb.) için geometri, hesaplama, miktarlar, tesis yönetimi, fiyatlandırma vb. için verileri tutabilir.

## Kısa Tarih ##

IFC girişimi, entegre uygulama geliştirmeyi desteklemek için Autodesk tarafından 1994 yılında başlatıldı ve Honeywell, Butler Manufacturing ve AT&T gibi şirketleri içeriyordu. 1995 yılında üyelik herkese açık olarak açılmış ve adı International Alliance for Interoperability olarak değiştirilmiştir. Kâr amacı gütmeyen kuruluşun amacı, Industry Foundation Class'ı (IFC) bir AEC ürün modeli olarak yayınlamaktı. 2005 yılında, isim yeniden değiştirildi ve buildSMART artık bu ismi koruyor.

## IFC Dosya Biçimi ##

IFC dosya formatı, dosya formatı spesifikasyonları v4'e ulaşmak için geçmişte birkaç değişikliğe uğramıştır. Zaman zaman birkaç küçük değişiklik meydana geldi ve bunlar, Ekler olarak spesifikasyonların bir parçası haline getirildi. Aşağıda, geçmişte halka açık hale getirilmiş farklı dosya özellikleri sürümlerinin bir listesi bulunmaktadır.

* IFC4 Ek2 (2016)IFC4 Ek1 (2015)
* IFC4 (Mart 2013) ifcXML2x3 (Haziran 2007)
* IFC2x2 add1 (RC2) için IFC2x3 (Şubat 2006) ifcXML2
* IFC2x2 Eki 1 (Temmuz 2004)IFC2x2 (RC1) için ifcXML2
* IFC2x için IFC 2x2IFC 2x Ek 1ifcXML1 ve
* IFC2x Eki 1IFC 2xIFC 2.0IFC 1.5.1IFC 1.5

IFC dosya formatı spesifikasyonlarının en son sürümleri, buildingSMART web sitesinde her zaman mevcuttur ve geliştiriciler, geliştirmeyi planladıkları her türlü uygulama için bunlara başvurmalıdır. Bu makaleyi yazarken, sürüm 4 özellikleri çevrimiçi olarak mevcut olan en son özelliklerdir.

### IFC Veri Dosyası Biçimleri ###

IFF dosya formatı, aşağıda listelenen farklı formatları kullanan uygulamalar arasında veri alışverişini destekler:

**IFC:** Bu, varsayılan IFC değişim biçimidir ve ISO 10303-21'e göre STEP fiziksel dosya yapısını kullanır. Bu dosya formatı .ifc dosya uzantısına sahiptir ve en çok kullanılan IFC formatıdır.

**IFC-XML:** STEP-XML olarak da adlandırılan ISO 10303-28 yapısına göre gönderen uygulama tarafından doğrudan oluşturulabilen IFC'nin XML dosya biçimi sürümüdür. IFC-XML dosya formatının, XML araçları arasında birlikte çalışabilirlik için uygun olduğu düşünülmektedir. IFC dosya biçimiyle karşılaştırıldığında, IFC-XML boyut olarak %300-400 daha büyüktür.

**IFC-ZIP:** IFC veya IFC-XML'nin [ZIP](/tr/compression/zip/) sıkıştırılmış sürümüdür ve bu dosyalardan biri zip arşivinin ana dizininde yer alır. Bu biçim, bir .ifc dosyasını %60-80 ve bir .ifc XML dosyasını %90-95 oranında sıkıştırır.

### IFC Mimarisi ###

IFC spesifikasyonu, inşaat ve tesis yönetimi endüstrisi sektörünün disiplinleri, işleri ve meslekleri dahilinde kullanımdan kaynaklanan terimleri, kavramları ve veri spesifikasyonu öğelerini içerir. Terimler ve kavramlar sade İngilizce sözcükleri kullanır, veri belirtimindeki veri öğeleri bir adlandırma kuralını izler.

türler, varlıklar, kurallar ve işlevler için veri öğesi adları "Ifc" ön ekiyle başlar ve CamelCase adlandırma kuralındaki İngilizce sözcüklerle devam eder (alt çizgi yok, sözcüğün ilk harfi büyük); bir varlık içindeki öznitelik adları, önek olmadan CamelCase adlandırma kuralını izler; bu standardın parçası olan özellik seti tanımları "Pset_" ön ekiyle başlar ve CamelCase adlandırma kuralındaki İngilizce sözcüklerle devam eder; bu standardın parçası olan miktar seti tanımları "Qto_" ön ekiyle başlar ve CamelCase adlandırma kuralındaki İngilizce sözcüklerle devam eder.

IFC'nin veri şeması mimarisi dört kavramsal katman tanımlar, her bir şema tam olarak bir kavramsal katmana atanır.

**Kaynak katmanı** — en alt katman, kaynak tanımlarını içeren tüm bireysel şemaları içerir; bu tanımlar, genel olarak benzersiz bir tanımlayıcı içermez ve daha yüksek bir katmanda açıklanan bir tanımdan bağımsız olarak kullanılmamalıdır;

**Çekirdek katmanı** — sonraki katman, en genel varlık tanımlarını içeren çekirdek şemasını ve çekirdek genişletme şemalarını içerir, çekirdek katmanında veya üzerinde tanımlanan tüm varlıklar, küresel olarak benzersiz bir kimlik ve isteğe bağlı olarak sahip ve geçmiş bilgileri taşır;

**Birlikte çalışabilirlik katmanı** — sonraki katman, çeşitli disiplinlerde kullanılan genel bir ürüne, sürece veya kaynak uzmanlığına özgü varlık tanımlarını içeren şemaları içerir; bu tanımlar genellikle alanlar arası alışveriş ve inşaat bilgilerinin paylaşımı için kullanılır;

**Etki alanı katmanı** — en üst katman, belirli bir disipline özgü ürün, süreç veya kaynakların uzmanlaşması olan varlık tanımlarını içeren şemaları içerir; bu tanımlar genellikle alan içi alışveriş ve bilgi paylaşımı için kullanılır.

## Referanslar ##

* [Endüstri Temel Sınıfları - Wikipedia Tarafından](https://en.wikipedia.org/wiki/Industry_Foundation_Classes)

