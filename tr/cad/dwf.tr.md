{
  "date" : "2020-03-16",
  "keywords" :[ "DWF", "Dosya Biçimi", "Aç", "Oku", "Oluştur", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"DWF dosya formatı ve DWF dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"DWF Dosya Biçimi",
  "linktitle" : "DWF",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## DWF dosyası nedir?

Tasarım Web Formatı (DWF), tasarım dosyalarını görüntülemek, incelemek veya yazdırmak için sıkıştırılmış formatta 2B/3B çizimi temsil eder. Tasarım verilerinin bir parçası olarak grafik ve metin içerir ve sıkıştırılmış biçimi nedeniyle dosyanın boyutunu azaltır. Küçültülmüş dosya boyutu, zengin tasarım verilerinin dağıtımını ve iletişimini verimli hale getirir. DWF, alıcının orijinal çizimi oluşturan CAD yazılımının kullanımı hakkında bilgi sahibi olmasını gerektirmez. DWF dosya biçiminin içeriği basit olabilir ve yalnızca tek bir sayfa içerebilir veya yazı tiplerine, renklere ve resimlere sahip olacak kadar karmaşık olabilir.

## Kısa Tarih ##

Autodesk, DWF dosya biçimini 1995 yılında Netscape Navigation eklentisi WHIP'in bir parçası olarak tanıttı. Biçim, yalnızca 2B biçiminden, zaman geçtikçe 3B içerikleri içerecek şekilde gelişti. Üçüncü taraf uygulamalarının çoğu da bu biçimi kullanır.

## DWF Dosya Biçimi ##

DWF, zengin mühendislik tasarım verilerini paylaşmak için özel olarak tasarlanmış açık, güvenli bir formattır. Bu tasarım verilerini oluşturmak için kullanılan orijinal uygulama yazılımı, donanım ve işletim sisteminden bağımsızdır. Bu, CAD uygulamalarını kullanmayan ekip üyelerinin bina, GIS veya ürün tasarımlarını görüntüleyerek dijital süreçlere katılmalarını sağlar. Bir DWF dosya arşivi, [ZIP](/tr/compression/zip/) sıkıştırması ile oluşturulan sıkıştırılmış bir arşivde birlikte paketlenmiş birkaç XML ve ikili dosyadan oluşur. Bir DWF dosya uzantısını ZIP olarak yeniden adlandırabilir ve dosyanın içeriğini görüntüleyebilirsiniz. DWF paketi, 2B grafikler, 3B grafikler, paket ve kesit meta verileri ve diğer kaynak dosyaları gibi birçok türde tasarım verisi içerebilir.

**DWF meta veri dosyaları** – Meta veri ve yapıya (yazar, başlık, oluşturma zamanı, bölüm bağımlılıkları, bölüm sıralaması, kaynak dosyası açıklamaları, roller, mime türleri vb.) ve bölüme (sayfa) ilişkin bilgileri içeren XML dosyaları bilgi, tasarım meta verileri vb.). Yapısal meta veriler, mantıksal nesneler (bir parçayı veya sayfayı temsil eden dosya koleksiyonları vb.) oluşturmak için kullanılır.

**Kaynak dosyaları** – paket/bölüm meta verilerinden referans alınan ve genellikle tasarım verilerinin çeşitli biçimlerdeki sunumları olan medya veya diğer içerik dosyaları (ZGL, W2D, [JPG](/tr/image/jpeg/), [PNG](/tr/image/png/), AVI, XML, [TXT](/tr/word-processing/txt/), [DOC](/tr/word-processing/doc/), vb.)

### Dosya Biçimi Ayrıntıları ###

DWF dosyaları, aşağıda gösterildiği gibi üç ana bölüm halinde düzenlenmiştir.

* Dosya tanımlama başlığı
* Dosya veri bloğu
* Dosya sonlandırma fragmanı

#### Dosya Tanımlayıcı Başlığı ####

Dosya tanımlayıcı başlığı, DWF dosyalarının uygulamalar tarafından tanımlanmasına izin verir. Ayrıca, dosyayı kodlamak için DWF belirtimlerinin hangi sürümünün kullanıldığını da tanımlar. Aşağıdaki gibi düzenlenmiş 12 baytlık bir başlıktır:


|Bayt|0|1|2|3|4|5|6|7|8|9|10|11
--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- |
|Karakter|(|D|W|F|(boşluk)|V|0|0|.|3|0|)

İşte bu tablonun bir özeti:

* Başlığın ilk altı baytı her zaman "(DWF V" ASCII karakterlerini temsil eder.
* Aşağıdaki 5 bayt, sürüm numarası hakkında bilgi içerir, örneğin "00.30", biçimin ana ve küçük sürüm değeriyle birlikte

Bir DWF dosyası oluşturan uygulamalar, verileri düzgün bir şekilde kullanmak için bir okuyucu uygulamasının desteklemesi gereken mümkün olan en düşük sürüm numarasını belirtmelidir.

#### Dosya Veri Bloğu ####

Dosya veri bloğu, bir DWF dosyasının 13. baytında başlar ve aşağıdaki tabloda olduğu gibi bir dizi işlem kodu ve işlenen çiftidir.

|Alan 1|Alan 2|Alan 3|Alan 4|Alan 5|Alan 5
--- | --- |--- | --- |--- | --- |
|opcode|operand|opcode|operand|opcode|operand

Bir DWF dosyası, okunabilir ASCII olarak işlem kodu-işlenen çiftlerini ve ayrıca kod ikilisini veya bunların her ikisinin bir karışımını içerebilir. Tüm DWF işlemlerinin okunabilir bir ASCII işlem kodu/işlenen formu vardır ve çoğu işlemin ayrıca kodlanmış bir ikili işlem kodu/işlenen formu vardır. İşlem kodları, 200'den fazla işleme izin veren tek bayt halindedir. Genişletilmiş ASCII ve genişletilmiş ikili, istisnai durumlardır. İşlem kodlarının değerleri, bazı istisnalar dışında 0-255 arasında değişebilir. Genişletilmiş ASCII ve genişletilmiş ikili işlem kodlarının iki özel türü dışında, bir dosya okuyucunun işlenen uzunluğunu nasıl hesaplayacağını bilmesi gerekir.

##### Yasak İşlem Kodları #####

Aşağıdakiler için ASCII temsilleri işlem kodları olarak kullanılamaz:

Aşağıdaki ASCII gösterimleri işlem kodları olarak kullanılamaz:

* Boşluk (0x20)
* Sekme (0x09)
* Tire (0x2D)
* ASCII basamakları 0-9 (0x30 - 0x39)
* Satır başı (0x0D)
* Satır besleme (0x0A)
* Tek Tırnak İşareti (0x27)
* Çift tırnak işareti (0x22)
* Dönem (0x2E)
* Parantez (0x28 ve 0x29)
* Kıvrık parantezler (0x7B ve 0x7D)
* Köşeli parantezler (0x5B ve 0x5D)
* Ters eğik çizgi (0x5C)

#### Dosya Sonlandırma Fragmanı ####

DWF için dosya sonlandırma fragmanı, dosyanın sonunu gösteren özel bir işlem kodudur. Bazı uygulamalar, sonlandırma işlem kodunu izleyerek DWF olmayan verileri depolayabilir. Fragman aşağıda gösterildiği gibidir:


|Bayt|0|1|2|3|4|5|6|7|8|9
---|---|---|---|---|---|---|---|---|---|---|
|Karakter|(|E|n|d|0|f|D|W|F|)

## Referanslar ##

* [DWF - Wikipedia'dan](https://en.wikipedia.org/wiki/Design_Web_Format)
* [WHIP Veri Biçimi](http://paulbourke.net/dataformats/whip/)
* [https://learn.microsoft.com/en-us/archive/blogs/opc/adventures-in-packaging-episode-1](https://learn.microsoft.com/en-us/archive/blogs/opc/adventures-in-packaging-episode-1)
