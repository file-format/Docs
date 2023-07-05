{
  "date" : "2020-11-11",
  "keywords" :[ "ACCDT", "uzantı", "dosya", "dosya biçimi", "Veritabanı Dosya Türü", "Veritabanı Dosya Biçimi", "Veritabanı Dosyaları" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"ACCDT dosya formatı ve ACCDT dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"ACCDT - Microsoft Access 2007 Şablon Veritabanı Dosya Biçimi",
  "linktitle" : "ACCDT",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-12"
}

## ACCDT dosyası nedir?

.accdt uzantılı bir dosya, önceden tanımlanmış veritabanı öğelerini içeren bir Microsoft Access veritabanı şablon dosyasıdır. Bu öğeler, veri depolamak için veritabanı şemaları, veri görünümleri için düzen açıklaması ve veritabanını tanımlayan meta veriler gibi bir veritabanı uygulamalarını tanımlayan bir yapılar koleksiyonudur. Şablon dosyaları olan ACCDT dosyaları, bunlarda bulunan şablon ayarlarına dayalı veritabanları oluşturmak için kullanılabilir. Ortaya çıkan veritabanı dosyaları [ACCDB](/tr/database/accdb/) dosyaları olarak kaydedilir ve tablolardaki verilerle doldurulur. Microsoft Access 2007 ve sonrası, ACCDT dosyalarını açabilir.

## ACCDT Dosya Biçimi

ACCDT şablon dosyaları, Office Açık XML belirtimlerine dayalıdır ve tüm veriler bir ZIP paketinde yer alır. Veritabanının yapı ve içerik bilgileri [XML](/tr/web/xml/) dosyalarında ve metin dosyalarında bulunur ve ilişkiler yoluyla birbirine bağlanır. Bir ACCDT dosyasını [.zip](/tr/compression/zip/) uzantısına yeniden adlandırabilir ve ZIP arşivinin içeriğini çıkarmak için herhangi bir sıkıştırma yazılımı kullanabilirsiniz.

### Dosya yapısı

ACCDT dosyaları, ilgili parçalardan oluşan bir koleksiyon içeren paketlerdir. Her **bölüm**, XML, metin ve ikili biçimler kullanan bir veritabanı uygulamasının içeriği hakkında aşağıdakileri içeren bilgileri depolar:

* Veritabanı nesneleri
* İlişkili meta veriler
* Paketin yapısı

#### Paket

Paket, birden çok parça içeren ve [ISO/IEC-29500-2](https://www.iso.org/standard/51459.html). ACCDT dosyaları, bir ilişkinin hedefi olması gereken en az bir Şablon metadaa bölümü içermelidir. Bu Şablon Meta Verileri, bir ACCDT dosyasının başlangıç kısmıdır.

#### Bölüm

Bölüm, içinde depolanan içeriğin doğasını ve türünü belirtmek için ilişkili bir türe sahip bir bayt akışıdır. Parça numaralandırma, bir paketteki tüm parçalar arasında geçerli parçaları, geçerli içerik türlerini ve gerekli ilişkileri belirtir.

#### İlişki

"Paket İlişkisi" - burada hedef bir parçadır ve kaynak bir bütün olarak pakettir.

"Parçadan Parçaya İlişki" - hedefin bir parça olduğu ve kaynağın paketin bir parçası olduğu.

"Açık İlişki" - bir kaynağa, bir ilişki öğesine ID özniteliğinin değeriyle atıfta bulunularak bir kaynak parçanın içeriğinden başvurulduğu yer.

"Örtülü İlişki" - açık olmayan bir ilişki.

"İç ilişki" - hedefin paketin bir parçası olduğu yer.

"Dış ilişki" - burada hedef, pakette olmayan bir dış kaynaktır.

## Referanslar ##

* [Erişim Şablonu Dosya Biçimi](https://docs.microsoft.com/en-us/openspecs/sharepoint_protocols/ms-accdt/0a4a68d7-7a85-4a27-ad74-730db57862d7)

