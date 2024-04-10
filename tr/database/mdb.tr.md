{
  "date" : "2020-11-11",
  "keywords" :[ "MDB", "uzantı", "dosya", "dosya biçimi", "Veritabanı Dosya Türü", "Veritabanı Dosya Biçimi", "Veritabanı Dosyaları" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"MDB dosya formatı ve MDB dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"MDB Dosya Biçimi - Bir Microsoft Access Veritabanı Dosyası",
  "linktitle" : "MDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## Bir MDB dosyası nedir?

.mdb uzantılı bir dosya, İlişkisel Veritabanı Yönetim Sistemi (RDBMS) olan bir Microsoft Access veritabanı dosyasıdır. Verileri birincil ve yabancı anahtarlar aracılığıyla birbirine bağlı veritabanı tablolarında saklar. MDB dosyası, veritabanı tablolarının, sorguların, saklı yordamların eksiksiz yapısını içerir. MDB, Microsoft Access 2003 için varsayılan dosya biçimidir. Microsoft Access'in yan sürümleri, bugüne kadarki en son dosya biçimi olan [ACCDB](/tr/database/accdb/) dosya biçimlerini kullanır. MDB dosyaları Microsoft Access, MDB Viewer, MDBOpener gibi uygulamalarla açılabilir ve ACCDB, [CSV](/tr/spreadsheet/csv/), Excel formatlarına vb. dönüştürülebilir.

## MDB Dosya Biçimi

MDB formatı için genel spesifikasyonlar mevcuttur ve Microsoft'un tescilli dosya formatı olmaya devam etmektedir. Ancak Microsoft, Açık Veritabanı Bağlantısı (ODBC) standardını ve Visual Basic for Applications (VBA) kullanarak MDB dosyasına bağlantı erişimi sağlar. Resmi olmayan MDB kılavuzu, tersine mühendisliğe dayalı MDB formatının kısa resmi olmayan açıklamasını sağlar ve özellikler hakkında bilgi edinmek için başvurulabilir.

### Sayfalar

Resmi olmayan MDB kılavuzuna göre, bir MDB dosyası sabit boyutlu sayfalardan oluşur (Jeb DB3 için 2048 bayt ve Jet DB 4 için 4096 bayt). İlk bayt, sayfanın türünü belirtir. Anahtar sayfa türleri aşağıdadır:

`İlk Sayfa:` Dosyanın uyumlu olduğu Jet DB sürümünün kimliğini de içeren veritabanı başlık bilgilerini içerir. Ayrıca, dosya güvenlik bilgilerini ve sayfa kullanım haritasını da içerir.

`Tablo tanımı sayfası:` Tablo tanımı sayfası sütunları, veri türlerini, dizini ve diğer bilgileri belirtir. Gerekirse ek sayfalar kullanır ve bu tablo için satır verilerini içeren bir sayfa haritası içerir.

`Veri sayfaları:` Veri sayfaları, verilerin satırlar halinde depolandığı gerçek veri kapsayıcılarıdır. Uzun veri değerlerini depolamak için yardımcı sayfaları kullanır.

Tek bir Microsoft Access veritabanı, dosya ve tablo boyutu sınırlamalarını aşmaya izin veren birden çok dosyadan oluşabilir. Bu, formları ve kodu kullanıcının masaüstündeki bir ön uç MDB dosyasına ve verileri ağa bağlı sunuculardaki başka bir arka uç MDB dosyasına koymayı kolaylaştırır.

## Referanslar ##

* [Erişim Özellikleri](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)
