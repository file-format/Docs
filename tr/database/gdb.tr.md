{
  "date" : "2022-05-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GDB Dosya Biçimi - ESRI Dosyası Geodatabase Dosyası",
  "description":"GDB dosya formatı ve GDB dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "GDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2022-05-08"
}

## GDB dosyası nedir?

ESRI dosyası Geodatabase (FileGDB), özellik veri kümeleri, özellik sınıfları ve ilişkili tablolar gibi ilgili jeo-uzamsal verileri tutan diskteki bir klasördeki dosyaların bir koleksiyonudur. Çalışması için başka bazı dosyaların .gdb dosyasının yanında aynı dizinde tutulması gerekir. Uzamsal ve uzamsal olmayan verileri yönetmek için .gdb dosyasında sorgular yürütülebilir.

## GDB Dosya Biçimi - Daha Fazla Bilgi

Dosya coğrafi veritabanları, yedi sistem tablosu ve kullanıcı verisinden oluşur. Kullanıcı verileri, aşağıdaki veri kümesi türlerinde saklanabilir:

* Özellik sınıfı
* Özellik veri kümesi
* Mozaik veri seti
* Tarama kataloğu
* Raster veri seti
* Şematik veri seti
* Tablo (uzaysal olmayan)
* Araç kutuları

Özellik veri kümeleri, özellik sınıflarının yanı sıra aşağıdaki veri kümesi türlerini içerebilir:

* Ekler
* Özelliklere bağlı açıklama
* Geometrik ağlar
* Ağ veri kümeleri
* Koli kumaşları
* İlişki dersleri
* araziler
* Topolojiler

Dosya coğrafi veritabanlarındaki veri kümelerinin varsayılan maksimum boyutu 1 TB'dir. Büyük veri kümeleri (genellikle raster) için maksimum boyut 256 TB'a çıkarılabilir. Bu, bir yapılandırma anahtar sözcüğü tarafından kontrol edilir. Daha fazla bilgi için bkz. Dosya coğrafi veritabanları için yapılandırma anahtar sözcükleri.

Dosya coğrafi veritabanları ayrıca alt türleri ve etki alanlarını içerebilir ve teslim alma/teslim alma çoğaltmasına ve tek yönlü çoğaltmalara katılabilir.

Bir dosya coğrafi veritabanına birkaç kullanıcı tarafından aynı anda erişilebilir. Kullanıcılar düzenleme yapıyorsa, farklı veri kümelerini düzenlemeleri gerekir.

## GDB Dosya Biçimi Özellikleri ##

Dosya GDB, ESRI'nin tescilli biçimidir ve belirtimleri herkese açık değildir. Bu nedenle, FIle GDB için dosya formatı ayrıntıları, bunu tersine mühendislikle [kısmen](https://github.com/rouault/dump_gdbtable/wiki/FGDB-Spec) yapan bazı kaynaklar dışında hiçbir yerde belgelenemedi. .

## Referanslar ##

* [FGDB Spesifikasyonları](https://github.com/rouault/dump_gdbtable/wiki/FGDB-Spec)

