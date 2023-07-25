{
  "date" : "2019-10-11",
  "keywords" :[ "shp dosyası", "shp dosya biçimi", "shp dosyası nedir", "dosya", "shp örneği", "shp dosya uzantısı","uzantı", "biçim" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHP - ESRI Şekil Dosyası",
  "description":"SHP dosya formatı ve SHP dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "SHP",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## .shp dosyası nedir?

SHP, ESRI Shapefile'ın temsili için kullanılan birincil dosya türlerinden birinin dosya uzantısıdır. Coğrafi Bilgi Sistemleri (CBS) uygulamaları tarafından kullanılmak üzere coğrafi bilgileri vektör verileri biçiminde temsil eder. Format, ESRI ve diğer yazılım ürünleri arasında birlikte çalışabilirliği kolaylaştırmak için açık spesifikasyonlar olarak geliştirilmiştir.

## Temsili veri

Bahsedildiği gibi, bir şekil dosyası formatı, bir veri setinin coğrafi bilgisini vektör özellikleri olarak tanımlar. Bu vektör özellikleri şunları içerir:

* puan
* çizgiler
* çokgenler

Bu özellikler kombinasyon halinde su kuyuları, ülke sınırları, uzamsal noktalar, nehirlerin akışı, göller vb. gibi hemen hemen her tür şekli temsil edebilir. Örneğin, Los Angeles şehirlerini içeren bir şekil dosyası, uzamsal verilere anlamlı bir temsil sağlayan nitelikler olarak şehir adı ve sıcaklığa sahip olabilir.

## İlişkili Dosyalar

Bağımsız bir shp dosyası, içerdiği verileri anlamlandırmak için yazılım uygulamaları tarafından kullanılamaz. Böyle bir dosyada yer alan bilgileri anlamlandırmak için, bir şekil dosyası aşağıdaki ek zorunlu dosyalardan yararlanır.

* shx dosyası - dizin dosyası
* dbf dosyası - ana dosyadaki şekillerin tüm niteliklerini saklayan bir dBASE dosyası
* prj dosyası - dosyanın proje bilgilerini saklar

Ana dosyayla aynı adı paylaşan başka isteğe bağlı dosyalar da olabilir.

## SHP Dosya Biçimi Özellikleri

Şekil dosyasının açık belirtimleri, ESRI'den [Teknik Açıklama](https://www.esri.com/content/dam/esrisites/sitecore-archive/Files/Pdfs/library/whitepapers/pdfs/shapefile.pdf) biçiminde çevrimiçi olarak edinilebilir ve dosyanın genel yapısını ayrıntılı olarak açıklar. Ana .shp dosyasındaki bilgiler başlıklardan ve kayıtlardan oluşur. Sabit uzunluklu dosya başlığını, her kaydın sabit uzunluktaki bir kayıt başlığından ve ardından değişken uzunluktaki kayıt içeriklerinden oluştuğu değişken uzunluktaki kayıtlar izler.

### Ana SHP Dosya Başlığı

Ana Dosya Başlığı, dosyanın başından başlar ve 100 bayt uzunluğundadır. Bayt konumu, değeri, türü ve bayt sırası ile birlikte bu ana dosya başlığının organizasyonu aşağıdaki tabloda gösterildiği gibidir.


|Bayt|Alan|Değer|Tür|Bayt Sırası
---|---|---|---|---|
|0-3|Dosya Kodu|9994|Tamsayı|Büyük Endian
|4-23|Kullanılmamış|0|Tamsayı|Büyük Endian
|24-27|Dosya Uzunluğu|Dosya Uzunluğu|Tamsayı|Büyük Endian
|28-31|Sürüm|1000|Tamsayı|Küçük Endian
|32-35|Şekil Türü|Şekil Türü|Tamsayı|Küçük Endian
|36-67|Minimum Sınırlayıcı Dikdörtgen|Xmin, Ymin, Xmax ve Ymax|çift|Little Endian
|68-83|Sınırlayıcı Kutu|Zmin, Zmaks|çift|Küçük Endian
|84-99|Sınırlayıcı Kutu|Mmin, Mmaks|çift|

Dosya uzunluğu değerinin, başlığı oluşturan elli adet 16 bitlik kelimeyi de içeren 16 bitlik kelimelerdeki dosyanın toplam uzunluğu olduğuna dikkat edilmelidir.

#### Şekil Türleri

Yukarıdaki tablodaki şekil türleri alanının değerleri aşağıdaki gibidir:


|Değer|Şekil Türü
---|---|
|0|Boş Şekil
|1|Puan
|3|Poliline
|5|Çokgen
|8|Çoklu Nokta
|11|Z Noktası
|13|PolyLineZ
|15|ÇokgenZ
|18|MultiPointZ
|21|M Noktası
|23|PolyLineM
|25|ÇokgenM
|28|MultiPointM
|31|Çoklu Yama

### Veri Kayıtları ###

Ana dosya başlığını değişken uzunluklu kayıtlar takip eder; burada her bir kayıt, sabit uzunlukta bir kayıt başlığı ve onu takip eden değişken uzunluktaki kayıt içeriğinden oluşur.

#### Kayıt Başlığı ####

Kayıt başlığı, kayıt numarası ve kaydın içerik uzunluğu hakkında bilgileri 8 baytlık sabit bir uzunlukta içerir. Kayıt başlığının organizasyonu aşağıda gösterildiği gibidir:


|Bayt|Alan|Değer|Tür|Bayt Sırası
---|---|---|---|---|
|0-3|Kayıt Numarası|Kayıt Numarası|Tamsayı|Büyük
|4-7|Kayıt Uzunluğu|Kayıt Uzunluğu|Tamsayı|Büyük

#### Kayıt İçeriği ####

Bir şekil dosyası kaydı içeriği, bir şekil tipinden ve ardından o şekil için geometrik verilerden oluşur. 0 şekil türü, şekil için geometrik verisi olmayan boş bir şekli temsil eder. Kayıt içeriğinin uzunluğu, şekil parçalarının ve köşelerin yansımasıdır. Bir kaydın böyle bir şekil tipi hakkında nasıl bilgi içerdiğini detaylandırmak için Nokta Şekli tipi örneğini ele alalım.

Bir nokta, her koordinatın çift kesinlikli bir değerle temsil edildiği X,Y sırasındaki belirli bir coğrafi konumu temsil eder. Aşağıdaki tablo bir Nokta şekli tipinin düzenini gösterir.


|Bayt|Şekil Tipi|Değer|Tür|Sayı|Bayt Sırası
---|---|---|---|---|---|
|0-3|Şekil Türü|1|Tamsayı|1|Küçük
|4-11|X|X|çift|1|Küçük
|12-19|E|E|çift|1|Küçük

Diğer şekil türlerinin örnekleri ESRI teknik açıklama belgesinde bulunabilir.

## Referanslar ##

* [ESRI Shapefile Teknik Açıklaması](https://www.esri.com/content/dam/esrisites/sitecore-archive/Files/Pdfs/library/whitepapers/pdfs/shapefile.pdf) by ESRI

