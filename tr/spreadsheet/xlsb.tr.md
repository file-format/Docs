{
  "date" : "2019-12-10",
  "keywords" :[ "XLSB", "dosya", "uzantı", "dosya formatı", "Excel İkili Hesap Tablosu Dosyası" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"XLSB dosyasının ne olduğunu ve bunları oluşturabilen ve açabilen API'leri öğrenmek için dosya biçimi kılavuzunuz.",
  "title" :"XLSB dosyası nedir?",
  "linktitle" : "XLSB",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## XLSB dosyası nedir?

XLSB dosya formatı, Excel çalışma kitabı içeriğini belirten bir kayıt ve yapı koleksiyonu olan Excel İkili Dosya Formatını belirtir. İçerik, yapılandırılmamış veya yarı yapılandırılmış sayı tabloları, metin veya hem sayı hem de metin, formüller, harici veri bağlantıları, çizelgeler ve resimler içerebilir. [XLSX](/tr/spreadsheet/xlsx/) (Açık XML dosya biçimini temel alan) aksine, XLSB ikili Excel çalışma kitabı dosyasını temsil eder. XLSB dosyaları daha hızlı okunabilir ve yazılabilir, bu da onları büyük dosyalarla çalışmak için kullanışlı kılar. XLSB, çalışma kitaplarını depolamak için nadiren kullanılır, çünkü XLSX (ve daha önce [XLS](/tr/spreadsheet/xls/)) çalışma kitaplarını kaydetmek için en yaygın kullanıcı tarafından seçilen dosya formatlarıdır. Microsoft Office 2007 ve üzeri tarafından açılabilir.

## XLSB Dosya Biçimi Özellikleri ##

XLSB dosya formatı için dosya formatı özellikleri, 2008'de sürüm 1.0 olarak halka açıldı. O zamandan beri, özellikler birkaç kez revize edildi ve özelliklerin en son sürümü (v 10.0) Nisan 2018'de yayınlandı. Özellikler Microsoft tarafından [[MS-XLSB] - Excel İkili Dosya Biçimi özellikleri](https:// /msdn.microsoft.com/en-us/library/cc313133(v#office.12).aspx) ve XLSB dosya biçimindeki dosyaları okumak veya yazmak için herkes tarafından danışılmalıdır.

## XLSB Dosya Yapısı ##

Bir XLSB dosyası, bir parça koleksiyonundan oluşan bir pakettir. Bu parçalar, çalışma kitabı verileri ve paketin yapısı da dahil olmak üzere çalışma kitabının içeriği hakkında bilgiler içerir. Bazı bölümler ikili kayıtlar kullanılarak depolanan bilgileri içerirken, bazıları XML olarak, diğerleri ise ikili bayt akışı olarak depolanan bilgileri içerir. Her ikili kayıt, çalışma kitabı verilerini içeren sıfır veya daha fazla yapılandırılmış alan içerir.

#### Paket ####

XLSB paketi, tam olarak bir çalışma kitabı bölümü içermesi gereken bir [ZIP](/tr/compression/zip/) arşividir. Bu kısım, bu paket ilişki kısmındaki bir ilişkinin hedefi olmalıdır. Çalışma kitabı bölümü, XLSB belgesindeki başlangıç bölümüdür.

#### Bölüm ####

Parça, parçada depolanan içeriğin doğasını ve türünü belirten ilişkili bir içerik türüne sahip bir bayt akışıdır. Bazı bölümler bilgileri ikili biçimde depolarken, diğerleri bilgileri XML olarak depolar. Özellikler belgesinin [parça listesi](https://msdn.microsoft.com/en-us/library/dd924091(v#office.12).aspx) bölümü, geçerli parçaları, içerik türlerini ve gerekli/isteğe bağlı ilişkileri listeler. tüm parçalar bir pakette.

#### İlişki ####

Bir kaynak ve bir hedef kaynak bir ilişki ile birbirine bağlıdır. Bir ilişki şunlar olabilir:

**Paket ilişkisi:** hedefin bir parça olduğu ve kaynağın bir bütün olarak paket olduğu

**Parçadan parçaya ilişki:** hedefin bir parça olduğu ve kaynağın paketin bir parçası olduğu

**Açık ilişki:** bir ilişki öğesinin kimlik öznitelik değerine başvurularak bir kaynak parçanın içeriğinden bir kaynağa başvurulduğu yerde

**örtük ilişki** açık olmayan bir ilişkidir

**İç ilişki:** burada hedef, paketin bir parçasıdır

**Dış ilişki:** burada hedef, pakette olmayan bir dış kaynaktır.

#### Kayıt ####

Kayıt, bir çalışma kitabındaki özellikler hakkında bilgi depolamak için kullanılan temel yapı taşıdır. Her ikili kayıt, değişken uzunluklu bir bayt dizisidir. Bir ikili kayıt üç bileşenden oluşur:

* bir kayıt türü
* bir kayıt boyutu ve
* o kayıt tipine özel kayıt verileri.

**Kayıt Türü:** Kayıt türü, kayıt tarafından belirtilen kayıt türünü gösterir. Ayrıca bu kayda özel kayıt verilerinin yapısını da belirtir. Geçerli kayıt türleri, özellikler belgesinin [Kayıt Listesi](https://msdn.microsoft.com/en-us/library/dd953057(v#office.12).aspx) bölümünde listelenmiştir. Kayıt türü bir veya iki bayt olmalı ve 128'den büyük veya ona eşit ve 16384'ten küçük olmalıdır.

**Kayıt Boyutu:** Kayıt boyutu, kayıt verilerinin toplam boyutunu belirten bayt sayısını belirtir. Bu değer bir ila dört bayt OLMALIDIR. Düşük bayttaki yüksek bit 0'a eşitse, bu değer bir bayt OLMALIDIR; aksi takdirde, bu değer bir bayttan büyük OLMALIDIR. Bayt sayısı bir bayttan büyükse, birbirini izleyen her bayttaki yüksek bit, ek bir baytın kullanılıp kullanılmayacağını belirtir. İkinci baytın yüksek biti 1'e eşitse, bu değer ek bir üçüncü bayt kullanmalıdır ZORUNLU. Üçüncü baytın yüksek biti 1'e eşitse, bu değer ek bir dördüncü bayt kullanmalıdır ZORUNLU. Dördüncü baytın yüksek biti dikkate alınmamalıdır ZORUNLU. Değer, birleştirilmiş her baytın yedi düşük bitinden oluşur. Düşük, en önemsiz bitler ilk bayt içinde bulunur ve birbirini izleyen her bayt, bir önceki bayttan daha yüksek sıralı bitler içerir.

**Kayıt Verisi:** Kayıt verisi bileşeni, belirli bir kayıt türüne karşılık gelen ve kaydın geri kalanını oluşturan alanlar içerir. Belirli bir kayıt türü için Kayıt Numaralandırma'da listelenen alanların sırası ve yapısı, Kayıtlar'da o kayıt türü için ilgili bölümde belirtilir. Kayıt veri bileşeninin toplam boyutu, kayıt boyutuna eşit OLMALIDIR. Kayıt verileri bileşenindeki alanlar, basit değerler, değer dizileri, çeşitli alanların yapıları, alan dizileri ve yapı dizileri içerebilir.

#### XLSB Kaydı Örneği ####

Aşağıdaki kayıt türü ve kayıt boyutu, 200 bayt boyutunda bir **BrtCommentText** kaydını belirtir:

11111101 00000100 11001000 00000001 [Kayıt Alanları]

İlk bayt 11111101'dir, 125 gibi düşük bir değer belirtir ve kayıt türünün ikinci bir bayt gerektirdiğini belirtir. İkinci bayt, 512'ye eşit olan 4 * 128 yüksek değerini belirten 00000100'dür. Kayıt türü değeri, **BrtCommentText** kayıt türüne karşılık gelen 125 + 512 veya 637'dir. Sonraki bayt 11001000'dir ve 72 gibi düşük bir değer belirtir ve kayıt boyutunun ikinci bir bayt gerektirdiğini belirtir. İkinci bayt 00000001'dir, 1 * 128 gibi daha yüksek bir değer belirtir ve kayıt boyutunun ek bir bayt gerektirmediğini belirtir. Kayıt boyutu, kayıt verisi bileşeninin bayt cinsinden toplam boyutunu belirten 72 + 128 veya 200'dür. Kayıt verisi bileşenindeki alanlar **BrtCommentText** tarafından belirtilir.

## Referanslar ##

* [[MS-XLSB] - Excel (.xlsb) İkili Dosya Biçimi](https://msdn.microsoft.com/en-us/library/cc313133(v#office.12).aspx)

