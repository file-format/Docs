{
  "date" : "2020-03-16",
  "keywords" :[ "DXF Dosyası", "Dosya Formatı", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"DXF dosya formatı ve DXF dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"DXF Dosya Biçimi",
  "linktitle" : "DXF",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## DXF dosyası nedir?

DXF, Çizim Değişim Formatı veya Çizim Değişim Formatı, AutoCAD çizim dosyasının etiketli bir veri temsilidir. Dosyadaki her öğe, grup kodu adı verilen bir önek tamsayı numarasına sahiptir. Bu grup kodu aslında takip eden öğeyi temsil eder ve belirli bir nesne türü için bir veri öğesinin anlamını belirtir. DXF, neredeyse tüm kullanıcı tanımlı bilgilerin bir çizim dosyasında temsil edilmesini mümkün kılar.

DXF dosya formatı Autodesk tarafından AutoCAD ve diğer uygulamalar arasında veri birlikte çalışabilirliği için CAD veri dosyası formatı olarak geliştirilmiştir. Böylece veriler, DXF dosya formatı birlikte çalışabilirlik özelliklerine göre diğer formatlardan DXF'ye ve AutoCAD'e aktarılabilir.

## Kısa Tarih ##


DXF dosya biçiminin geçmişi, AutoCAD 1.0'ın bir parçası olarak tanıtıldığı 1982 yılına kadar uzanır. AutoCAD'in ilk sürümleri yalnızca DXF'nin ASCII dosya biçimini destekler. 1988'de AutoCAD'in 10. sürümünün (ve üzeri) piyasaya sürülmesiyle, AutoCAD'de hem ASCII hem de ikili DXF dosya formatı desteği tanıtıldı. Daha önceki aşamalarda, Autodesk herhangi bir dosya formatı özelliğini paylaşmadı ve bu nedenle, DXF dosyalarının doğru şekilde içe aktarılması kolay değildi. Ancak, Autodesk artık DXF spesifikasyonlarını yayınlıyor ve halka açık.

## Dosya Biçimi Özellikleri ##

DXF dosya formatı, içeriği bölümler halinde düzenlemek için grup kodu ve değer çiftlerini kullanır. Her bölüm, her kaydın bir grup kodu ve veri öğesinden oluştuğu kayıtlardan oluşur. DXF dosyasında her grup kodu ve değeri kendi satırındadır. Her bölüm bir grup kodu 0 ile başlar ve ardından SECTION dizesi gelir. Bunu bir grup kodu 2 ve bölümün adını gösteren bir dizi izler (örneğin, SECTION1). Her bölüm, öğelerini tanımlayan grup kodlarından ve değerlerinden oluşur. Bir bölüm 0 ile biter ve ardından ENDSEC dizesi gelir.

DXF dosya biçimi, nesneleri varlıklardan farklı olarak kabul eder. Nesnelerin burada grafik temsili yoktur, ancak varlıklarda vardır. Bu nedenle, DXF'deki girdilere grafik nesneler, nesneler nesnelere ise grafik olmayan nesneler denir. DXF dosyasının BLOCK ve ENTITIES bölümleri Entity'leri içerir ve bu iki bölümdeki grup kodlarının kullanımı aynıdır. Bir varlığın sonu, bir sonraki varlığı başlatan veya bölümün sonunu belirten sonraki 0 grubuyla belirtilir.

### Dosya Yapısı ###

Bir DXF dosyasındaki bölümler aşağıdaki sırayla düzenlenir:

|Bölüm|Temel açıklama
---|---|
|Başlık|Bu bölüm çizim ile ilgili genel bilgileri içerir. Bu, çizimle ilişkili farklı değişkenleri ve ilişkili değerleri içeren, telefonunuzdaki Ayarlar işlevi gibidir. Örneğin, Başlık bölümü, DXF dosyasının hangi AutoCAD sürümünü kullandığını ($ACADVER değişkeni) veya dosyadaki açıları ölçmek için kullanılan birimi ($AUNITS değişkeni) tanımlar.
|Sınıflar|SINIFLAR bölümü, örnekleri veritabanının BLOCKS, ENTITIES ve OBJECTS bölümlerinde görünen uygulama tanımlı sınıflara ilişkin bilgileri içerir.
|Tablolar|Bu bölüm, her biri bir dizi farklı sembol girişi içeren birkaç farklı tablo için tanımları içerir. Örneğin, [hat türü](https://knowledge.autodesk.com/support/autocad/learn-explore/caas/CloudHelp/cloudhelp/2016/ENU/AutoCAD-Core/files/GUID-20B4D4B3-1220-426A- 847B-5BBE36EC6FDF-htm.html) tablosu (LTYPE), DXF dosyasındaki tire, nokta, metin ve sembollerin modelini ve bunların nasıl ölçeklendiğini tanımlar. Bu bölümde bulunan tabloların tam listesi:<ul><li> Uygulama Kimliği (APPID) tablosu</li><li> Blok Kaydı (BLOCK_RECORD) tablosu</li><li> Boyut Stili (DIMSTYPE) tablosu</li><li> Katman (LAYER) tablosu</li><li> Çizgi tipi (LTYPE) tablosu</li><li> Metin stili (STYLE) tablosu</li><li> Kullanıcı Koordinat Sistemi (UCS) tablosu</li><li> Tabloyu Görüntüle (GÖRÜNÜM)</li><li> Görüntü alanı yapılandırması (VPORT) tablosu</li></ul>
|Bloklar|Bu bölüm, çizimdeki her bir blok referansını oluşturan grafik nesneleri ve çizim varlıklarını içerir.
|Entities|Bu bölüm, çizimin gerçek nesne verilerini ve grafiksel varlıklarını içerir. Bu, ham verileri içerebilir - örneğin, bir daire öğesi, kalınlığı, merkez noktası, yarıçapı ve ekstrüzyon yönü ile tanımlanır.
|Nesneler|Burada, çizimin grafik olmayan kısımlarını bulacaksınız. Örneğin, AutoCAD sözlükleri burada saklanır.

## Referanslar ##

* [DXF Dosya Spesifikasyonları](http://images.autodesk.com/adsk/files/autocad_2012_pdf_dxf-reference_enu.pdf)
* [Wikipedia'dan AutoCAD DXF](https://en.wikipedia.org/wiki/AutoCAD_DXF)

