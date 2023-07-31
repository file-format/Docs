{
  "date" : "2020-08-20",
  "keywords" :[ "cff2 dosyası", "cff2 dosya biçimi", "cff2 dosyası nedir", "dosya", "cff2 örneği", "cff2 dosya uzantısı","uzantı", "biçim" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFF2 - Kompakt Yazı Tipi Dosya Biçimi sürüm 2",
  "description":"CFF2 Dosya Biçimi ve CFF2 dosyaları oluşturmak ve açmak için API'ler hakkında bilgi edinin.",
  "linktitle" : "CFF2",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## CFF2 dosyası nedir?

CFF2 dosya formatı, CFF dosya formatının 2.0 sürümüdür ve CFF dosya formatına benzer glif anahatlarının ve meta verilerin verimli bir şekilde depolanmasına olanak tanır. CFF2, OpenType yazı tipi bağlamında CFF2 etiketli bir 'sfnt' tablosu olarak kullanılması amaçlandığından CFF'den farklıdır. Tek başına bir program olarak kullanılamaz ve diğer OpenType tablolarındaki verilere bağlıdır.

## CFF2 Dosya Biçimi

[CFF2 dosya biçimi belirtimleri](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2), dosya biçimiyle ilgili dahili veri düzeni, veri türleri, tablolar ve diğer dahili bilgiler hakkında ayrıntılar içerir. Geliştiricinin referansı için başvurulabilir. Bunlarla ilgili bazı detaylar aşağıdaki gibidir.

### Veri Düzeni

CFF2 dosya biçiminin ikili verileri, bir dizi ayrı veri yapısı olarak mantıksal olarak düzenlenir. İkili veriler içindeki düzen aşağıdaki tabloda gösterildiği gibidir.

|Giriş |Yorumlar|
---|---|
|Başlık |Sabit konum|
|Üst DICT| Sabit konum|
|Küresel Subr ENDEKSİ| Sabit konum|
|Varyasyon |Mağaza|
|FDSelect |Yalnızca Font DICT INDEX'te birden fazla Font DICT varsa gösterir.|
|Yazı tipi DICT DİZİNİ ||
|DICT Yazı Tipi Dizisi| Font DICT INDEX'e dahildir.|
|Özel DICT| Yazı Tipi DICT.|

Sadece ilk üç yapı sabit konumlara dayanmaktadır. Kalanlara ofsetler üzerinden ulaşılır ve sıraları değiştirilebilir.

### Veri tipleri

CFF2 dosya biçimi aşağıdaki veri türlerini kullanır.

|Ad |Aralık |Açıklama|
---|---|---|
|uint8 |0 - 255 |8-bit işaretsiz sayı|
|uint16 |0 - 65535| 16 bitlik işaretsiz sayı|
|uint32 |0 - 4294967295| 32-bit işaretsiz sayı|
|Ofset |değişiklik gösterir| 1, 2, 3 veya 4 bayt ofsetler (bir Dizin tablosunda OffSize alanı tarafından belirtilir)|
|OffSize |1 - 4| 1 baytlık işaretsiz sayı, Ofset alanının veya alanların boyutunu belirtir |

Tüm çok baytlı sayısal verileri ve ofset alanlarını big-endian bayt düzeninde depolar. CFF2 formatı, herhangi bir hizalama kısıtlamasına uymadığından, doldurma baytlarından muaftır.

### DICT Verileri

CFF2 dosyaları, yazı tipi sözlüğü verilerini kompakt, belirtilmiş bir biçimde anahtar-değer çiftleri olarak içerir. Sözlük anahtarları 1 veya 2 bayt operatörler olarak kodlanır ve sözlük değerleri değişken boyutlu sayısal işlenenler olarak kodlanır. DICT Veri biçimini kullanan üç yapı vardır: "Top DICT", "Font DICT" ve "Private DICT". Farklı boyutlarda bir dizi tamsayı işlenen türü tanımlanır ve aşağıdaki tabloda gösterildiği gibi kodlanır (işlenenin ilk baytı b0'dır, ikincisi b1'dir, vb.).

|Boyut |b0 aralığı |Değer aralığı |Değer hesaplaması|
---|---|---|---|
|1 |32 - 246| -107 - +107 |b0 - 139|
|2 |247 - 250| +108 - +1131 |(b0 - 247) * 256 + b1 + 108|
|2 |251 - 254| -1131'den -108'e| -(b0 - 251) * 256 - b1 - 108|
|3 |28| -32768 ila +32767| b1 << 8 | b2|
|5 |29| -(2^31) - +(2^31 - 1)| b1 << 24 \| b2 << 16 \| b3 << 8 \| b4|

### Başlık

İkili veriler, aşağıdaki Tabloda gösterilen formata sahip bir başlık ile başlar.

|Tür |Ad |Açıklama|
---|---|---|
|uint8| ana Sürüm| Ana sürümü biçimlendirin. 2'ye ayarla.|
|uint8| minörSürüm| Küçük sürümü biçimlendirin. Sıfıra ayarla.|
|uint8| başlıkBoyutu| Başlık boyutu (bayt).|
|uint16| topDictLength| Bayt cinsinden Üst DICT yapısının uzunluğu.|

## Referanslar

* [CFF2 Dosya Biçimi](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2)

