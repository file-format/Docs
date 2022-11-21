{
  "date" : "2021-04-08",
  "keywords" :[ "lz4 dosyası", "lz4 dosya biçimi", "lz4 dosyası nedir", "dosya", "lz4 örneği", "lz4 dosya uzantısı","uzantı", "biçim" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZ4 - LZ4 Sıkıştırılmış Dosya Formatı",
  "description":"LBR dosya formatı ve LZ4 dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "LZ4",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## LZ4 dosyası nedir?

.lz4 uzantılı bir dosya, [LZ4](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm)) sıkıştırmayı destekleyen uygulamalar/yardımcı programlar ile oluşturulan sıkıştırılmış bir arşiv dosyasıdır. LZ4 algoritması, hız ve sıkıştırma oranı arasındaki dengeye odaklanır. Sıkıştırılmış LZ4 arşivleri, LZ4 komut satırı yardımcı programı kullanılarak oluşturulabilir ve aynısı kullanılarak sıkıştırılmış dosyaları açılabilir.

## LZ4 Dosya Biçimi

LZ4 sıkıştırma algoritmasına dayanan LZ4 dosya formatı, CPU tipi, işletim sistemi, dosya sistemi ve karakter setinden bağımsızdır. LZ4 algoritmasını kullanarak dosya sıkıştırma ve akış sıkıştırma için uygundur. LZ4 formatının ilk uygulaması, 2011 yılında Yann Collet tarafından [C](/tr/programming/c/) dilinde gerçekleştirildi ve geliştiricinin [Github](https://github.com/lz4/lz4) referansı için mevcut. .

### LZ4 Çerçeve Biçimi

LZ4 dosya formatının genel yapısı aşağıda gösterildiği gibidir.

|MagicNb|F. tanımlayıcı| Blok|(...)|EndMark |C. Sağlama |
---|---|---|---|---|---|
|4 bayt| 3-15 bayt||| 4 bayt| 0-4 bayt|

#### Sihirli sayı

4 Bayt, Little endian formatı. Değer : 0x184D2204

#### Çerçeve Tanımlayıcı

Çerçeve tanımlayıcı 3 t0 15 bayttan oluşur ve belirtimlerin en önemli parçasıdır. Magic_Number ve Frame_Descriptor alanları birlikte LZ4 Çerçeve Başlığı olarak anılır ve boyutları 7 ile 19 bayt arasında değişir. Aşağıda gösterildiği gibidir.

|FLG| BD| (İçerik Boyutu)| (Sözlük Kimliği)| HC|
---|---|---|---|---|
|1 bayt| 1 bayt| 0 - 8 bayt| 0 - 4 bayt| 1 bayt|

#### Veri Blokları

Her veri bloğu aşağıdaki sırayı takip eder.

|Blok Boyutu| veri| (Blok Sağlama Toplamı)|
---|---|---|
|4 bayt| |0 - 4 bayt|

#### EndMark

Son veri bloğunun ardından 32 bitlik 0x00000000 değeri geldiğinde blok akışı sona erer.

#### İçerik Sağlama Toplamı

Content_Checksum, kodu çözülen içeriğin geçerliliğini doğrular ve xxHash-32 algoritmasının sonucu kullanılarak gerçekleştirilir. Tüm blokların başarılı bir şekilde iletilmesinin sonuçlarını doğru sırada ve hatasız olarak doğrular.

## Referanslar

* [LZ4 Çerçeve Formatı](https://github.com/lz4/lz4/blob/dev/doc/lz4_Frame_format.md)
* [LZ4 Sıkıştırma Algoritması - Wikipedia](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm))

