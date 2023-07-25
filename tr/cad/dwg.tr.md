{
  "date" : "2020-03-16",
  "keywords" :[ "DWG", "Dosya Biçimi", "CAD", "Aç", "Oluştur" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"DWG dosya formatı ve DWG dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"DWG Dosya Biçimi",
  "linktitle" : "DWG",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## DWG dosyası nedir?

DWG uzantılı dosyalar, 2B ve 3B tasarım verilerini içermek için kullanılan tescilli ikili dosyaları temsil eder. ASCII dosyaları olan DXF gibi, DWG de CAD (Bilgisayar Destekli Tasarım) çizimleri için ikili dosya formatını temsil eder. CAD dosyalarının içeriğinin temsili için vektör görüntüsü ve meta verileri içerir. Autodesk'in ücretsiz DWG TrueView'u gibi, Windows İşletim Sisteminde DWG dosyalarını görüntülemek için ücretsiz görüntüleyiciler mevcuttur. DWG dosyalarına ulaşmayı destekleyen başka üçüncü taraf uygulamaları da vardır. DWG dosyaları, kullanıcı tarafından oluşturulan bilgileri içerir ve şunları içerir:

* Tasarımlar
* Geometrik veriler
* Haritalar ve fotoğraflar

Bu format mimarlar, mühendisler ve tasarımcılar tarafından çeşitli tasarım amaçları için yaygın olarak kullanılmaktadır.

## Kısa Tarih ##

DWG dosya formatı, 1982'de resmi olarak tanıtılmasından bu yana zamanla gelişmiştir. Tarih perspektifinden geçmiş olaylara kısa bir genel bakış aşağıdaki gibidir.

**1982:** Autodesk, 1970 yılında Mike Riddle tarafından geliştirilen DWG dosya biçimini AutoCAD'in temeli olarak lisansladı.

**1998:** Autodesk, AutoCAD R14.01'in piyasaya sürülmesiyle, program tarafından oluşturulan DWG dosyalarına Autodesk tarafından WaterMark olarak adlandırılan şifreli bir sağlama toplamı ve ürün kodunu gömen DWGCHECK adlı bir işlev aracılığıyla dosya doğrulaması ekledi.

**2006:** Autodesk, AutoCAD 2007'yi, "Autodesk DWG. Bu dosya en son bir Autodesk uygulaması veya Autodesk lisanslı uygulaması tarafından kaydedilen Güvenilir bir DWG'dir" metin dizesini DWG dosyalarına katıştırmak üzere "TrustedDWG teknolojisini" içerecek şekilde değiştirdi. Bunun amacı, Autodesk yazılımı kullanıcılarının, bu dosyaların uyumsuzluk riskini azaltmada kesinlikle yardımcı olması gereken bir Autodesk veya RealDWG uygulaması tarafından oluşturulduklarından emin olmalarına yardımcı olmaktı.

## Dosya Yapısı ##

DWG, bir dizi uygulama tarafından yaygın olarak kullanılan dosya formatlarından biri olmuştur ve sağlam bir dosya yapısına sahiptir. DWG bir ikili dosya formatı olduğundan, düz ASCII [DXF](/tr/cad/dxf/) dosya formatı gibi insanlar tarafından okunamaz. DWG dosyaları genellikle görüntü koordinatları ve onunla ilişkili herhangi bir meta veri hakkında bilgi içerir. DWG dosya formatının eksiksiz [özellikleri](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf) OpenDesign tarafından indirilebilir. DWG dosya formatının dosya yapısı aşağıdaki gibi özetlenmiştir.

**Başlık**: Dosya başlığı, DWG Başlık değişkenlerinden ve hata tespiti için kullanılan Döngüsel Artıklık Kontrolü (CRC) hakkında bilgilerden oluşur. Her alt bölüm, farklı etiketleri temsil etmek için farklı bit uzunluklarının kullanıldığı özel bir vektördür. Örneğin, DWG Header değişkeninin ilk 6 biti sürüm dizesini ifade eder.

**Sınıf Tanımları:** Bir DWG dosyası, belirli .dwg dosyası amacına bağlı olarak çok sayıda sınıf içerebilir. Diğerlerine ek olarak, sınıf veri alanının sınıf meta veri boyutu, sınıf numarası ve sağlama toplamı gibi bilgiler.

**Şablon**: Bu isteğe bağlıdır ve R15 ve R15 sürümleri için bu bölüm Nesne Boş Alanı bölümünün altındadır.

**Doldurma**: Meta veriler, eski AutoCAD yazılım sürümlerinin yeni DWG dosya biçimiyle uyumlu olmasını sağlayan belirli sayıda baytla son eklenir ve son eklenir.

**Görüntü Verileri**: Bu bölümün meta verileri, belirli .dwg türüne bağlıdır. R14 ve R15 kullanıcıları için bu bölüm isteğe bağlıdır.

**Nesne Verileri**: Nesne verileri, mevcut nesne listesine karşılık gelen tablo varlıklarının, sözlük girişlerinin vb. tam bir listesinden oluşur.

**Nesne Haritası**: Dosyadaki her nesnenin konumu, dosyanın bu bölümünde belirtilir. Bu bölümdeki meta verilerin çoğu, nesnenin tanımlanmasında ve yeniden oluşturulmasında rol oynayan dosya tanıtıcılarıdır.

**Nesne Boş Alanı**: Bu bölüm tüm kullanıcılar için isteğe bağlıdır

**İkinci Başlık**: DWG dosyasının sonuna doğru dosya başlığı bölümünün bir kopyası

## Referanslar ##

* [DWG Dosya Biçimi Özellikleri](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf)
* [DWG Dosya Spesifikasyonu](https://www.scan2cad.com/blog/dwg/file-spec/)
* [DWG - Wikipedia Tarafından](https://en.wikipedia.org/wiki/.dwg)

