{
  "date" : "2019-12-10",
  "keywords" :[ "DIF", "dosya", "uzantı", "dosya formatı", "Veri Değişim Dosyası", "Elektronik Tablo"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"DIF dosya uzantısının ne olduğunu ve DIF dosyalarını oluşturabilen ve açabilen API'leri öğrenmek için dosya biçimi kılavuzunuz.",
  "title" :"DIF - Veri Değişim Dosyası Formatı",
  "linktitle" : "DIF",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## .dif dosyası nedir?

DIF, elektronik tablo verilerini farklı uygulamalar arasında içe/dışa aktarmak için kullanılan Veri Değişim Biçimi anlamına gelir. Bunlara Microsoft Excel, OpenOffice Calc, StarCalc ve diğerleri dahildir. Bu dosya biçiminin tek sınırlaması olan tek bir elektronik tabloda bulunan verileri depolar.

## DIF Dosya Formatının Kısa Tarihi ##

DIF dosya biçimi, 1980'lerin başında Software Arts, Inc. tarafından geliştirilmiştir. DIF için dosya biçimi belirtimleri, kişisel bilgisayarlar için ilk elektronik tablo programı olan VisiCalc'a dahil edildi. Bu spesifikasyonların telif hakkı 1981 yılında alınmıştır ve Software Arts Products Corp.'un tescilli ticari markasıdır.

## DIF Dosya Biçimi ##

DIF elektronik tablo içeriğini ASCII metin dosyasında saklar, bu da bir metin düzenleyiciyle görüntülenmesini ve düzenlenmesini sağlar. Biçim, veri alışverişi özellikleri nedeniyle veri serileştirme biçimleri listesindeki yerini alır. Bir DIF dosyası 2 bölümden oluşur; bir başlık ve veri.

DIF'deki her şey 2 veya 3 satırlık bir yığınla temsil edilir. Başlıklar 3 satırlık bir öbek alır; veri, 2.

* Başlık parçaları, tümü büyük harf, yalnızca alfabetik karakterler ve 32'den az harf içeren bir metin tanımlayıcıyla başlar. Aşağıdaki satır bir çift sayı olmalı ve üçüncü satır tırnaklı bir dize olmalıdır.
* Veri yığınları bir sayı çifti ile başlar ve sonraki satır alıntılanmış bir dize veya bir anahtar kelimedir.

### Değerler ###

Bir değer, ilki bir çift sayı ve ikincisi bir dize veya bir anahtar kelime olmak üzere iki satırı kaplar. Çiftin ilk sayısı türü belirtir:

* −1 – yönerge türü, ikinci sayı yoksayılır, aşağıdaki satır bu anahtar sözcüklerden biridir:
** BOT – demetin başlangıcı (sıranın başlangıcı)
** EOD – veri sonu
* 0 – sayısal tip, değer ikinci sayıdır, aşağıdaki satır bu anahtar kelimelerden biridir:
** V – geçerli
** NA – mevcut değil
** HATA – hata
** DOĞRU – gerçek boole değeri
** YANLIŞ – yanlış boole değeri
* 1 – string tipi, ikinci sayı yoksayılır, sonraki satır çift tırnak içindeki stringdir

### DIF Başlık parçası ###

Bir DIF dosyasının başlık öbeği, bir değerin iki satırı tarafından takip edilen bir tanımlayıcı satırından oluşur. Başlık parçalarındaki sayısal değerler, geçerlilik anahtar sözcükleri yerine yalnızca boş bir dize kullanır. Bu başlık parçalarının detayları aşağıdaki gibidir.

* TABLO - sürümü sayısal bir değer takip eder, değerin kullanılmayan ikinci satırı bir oluşturucu yorumu içerir
* VEKTÖRLER - sütun sayısı sayısal bir değer olarak takip eder
* TUPLES - sayısal bir değer olarak takip eden satır sayısı
* DATA - boş bir 0 sayısal değerinden sonra, tablonun verileri takip eder, her satırın önünde bir YİD değeri bulunur, tablonun tamamı bir EOD değeriyle sonlandırılır

### DIF Örneği ###

Aşağıdaki örnek, basit bir çalışma sayfasının içeriğini ve eşdeğer DIF temsilini gösterir.


|İsim|Yaş
---|---|
|Bob|34
|Sayfa|22

```
TABLE
0,1
"EXCEL"
VECTORS
0,3
""
TUPLES
0,2
""
DATA
0,0
""
-1,0
BOT
1,0
"Name"
1,0
"Age"
-1,0
BOT
1,0
"Bob"
0,34
V
-1,0
BOT
1,0
"Sheetal"
0,22
V
-1,0
EOD
```

## Referanslar ##

* [ DIF - Wikipedia'dan](https://en.wikipedia.org/wiki/Data_Interchange_Format)

