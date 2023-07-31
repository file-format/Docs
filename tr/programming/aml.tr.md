
{
  "date" : "2022-01-28",
  "keywords": [ ".aml file", "extension", "format","Microsoft Assistance Markup Language File", "how to open .aml file","aml file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AML Dosyası - Microsoft Yardım İşaretleme Dili Dosyası",
  "description":"AML dosyasının ne olduğu ve AML dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "AML",
  "menu" : {
    "docs" : {
      "identifier":"programming-aml",
      "parent" : "programming"
}
},
  "lastmod" : "2022-01-28"
}

# AML - Microsoft Yardım İşaretleme Dili Dosyası

## AML dosyası nedir?

Bir AML (Yardım İşaretleme Dili) dosyası, Microsoft Yardım İşaretleme Dili (MAML) ile oluşturulan bir XML dosyasıdır. Microsoft Windows işletim sistemi için çevrimiçi yardım sağlamak üzere Microsoft tarafından geliştirilmiştir. Bundan önce, Windows yardımı derlenmiş HTML [CHM](/tr/web/chm/) dosya biçiminde mevcuttu. AML dosyaları, uygulamanın kaynak kodu ve destekleyici yardım sayfaları oluşturmasına izin veren yapılandırılmış bir belge sağlar. Bu, belgelerin ve onları oluşturan unsurların bağlamlarına göre tanımlanmasına izin verir. AML yardım dosyaları çevrimiçi olarak yayınlanır ve çevrimiçi olarak sunulan paket güncellemelerinden güncellenecek şekilde yapılandırılabilir.

## MAML Dosya Yapısı

MAML kullanılarak oluşturulan AML dosyaları, çok çeşitli etkin kavramları ifade etmek için kullanılabilen [XML](/tr/web/xml/) dosyaları olarak kaydedilir. Ayrıca, adım adım sihirbazla yardım dosyasını kullanıcı için etkileşimli hale getiren rehberli yardım (etkin içerik sihirbazı) sağlayabilir.

MAML kullanılarak oluşturulan bir AML dosyası, aşağıdaki gibi bölümlere ayrılabilen yazma yapısını takip eder:

* Kavramsal
* SSS
* Sözlük
* Prosedür
* Referans
* Yeniden Kullanılabilir İçerik
* Görev
* Sorun giderme ve
* Öğretici

## MAML Dosyaları nasıl oluşturulur?

MAML dosyaları aşağıdaki yöntemlerden biri kullanılarak oluşturulabilir:

* Sandcastle Kullanımı - Yardım dosyasını oluşturmak için bir dizi şema ve yürütülebilir program kullanır. Ancak bu araç kullanımdan kaldırıldı.
* DocProject Kullanımı - Yardım içeriğini oluşturmak için Microsoft Visual Studio içinden yürütülebilen bir Microsoft Visual Studio eklentisi.

MAML dosyaları, bir .XSL şemaları ve yürütülebilir program paketi olan Sandcastle kullanılarak oluşturulabilir. Bir Microsoft Visual Studio yardım yazma aracı eklentisi olan DocProject kullanılarak da oluşturulabilirler.

## Referanslar

* [PlatyPS kullanarak XML tabanlı yardım oluşturun
](https://learn.microsoft.com/en-us/powershell/scripting/dev-cross-plat/create-help-using-platyps?view=powershell-7.2)
* [Microsoft Yardım İşaretleme Dili](https://en.wikipedia.org/wiki/Microsoft_Assistance_Markup_Language)

# AML - Arc Makro Dil Dosyası

## ARC Makro AML dosyası nedir?

Bir AML (ARC Makro Dili) dosyası, ArcInfo Workstation GIS uygulamasıyla oluşturulan bir betik dosyasıdır. ArcInfo'da GIS uygulamaları oluşturmak için özel bir üst düzey algoritmik dil olan ARC Makro Dili ile yazılmıştır. AML, 1986 yılında ESRI tarafından tasarlandı ve komut satırı ARCINFO GIS sisteminden uygulamalar oluşturma amacına hizmet etti. Komut dosyası dosyası olan AML dosyaları, kullanıcı arabirimi bileşenleri oluşturmak ve harita verilerini değiştirmek gibi bir dizi görevi gerçekleştirmek için komut dosyası komutları içerebilir.

## AML Dosya Biçimi - Daha Fazla Bilgi

Komut dosyaları olan AML, bilgileri diske düz metin dosyaları olarak kaydeder. PRIMOS işletim sisteminin CPL kabuk dilini temel alan AML sözdizimini izler. AML dili, ESRI'nin ArcGIS paketinin bir parçası olan ve VBA veya Python aracılığıyla programlama desteği sağlamak için ArcObjects kullanan coğrafi işlem çerçevesi ile değiştirilmiştir.

## Referanslar

* [ARC Makro Dili](https://en.wikipedia.org/wiki/ARC_Macro_Language)
* [Komut Dosyası Araçları ile AML Kullanımı](https://desktop.arcgis.com/en/arcmap/latest/analyze/creating-tools/using-amls-with-script-tools.htm)

