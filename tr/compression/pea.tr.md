{
  "date" : "2021-04-21",
  "keywords" :[ "bezelye dosyası", "bezelye dosyası biçimi", "bezelye dosyası nedir", "dosya", "bezelye örneği", "bezelye dosyası uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PEA - PeaZip Arşiv Dosya Biçimi",
  "description":"PEA dosya formatı ve PEA dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "PEA",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-21"
}

## PEA dosyası nedir?

Pack, Encrypt ve Authenticate'in kısaltması olan .pea uzantılı bir dosya, [PeaZip](https://peazip.github.io/) arşivleme yazılımı uygulamasıyla oluşturulmuş bir [zip](/tr/compression/zip/) arşividir. Sıkıştırma ve birden çok birim çıkışı içerir ve Doğrulanmış Şifreleme ve kriptografi yoluyla esnek bir güvenlik modeli sunar. Bu, verilerin hem gizliliğini hem de kimlik doğrulamasını sağlar. PeaZip yardımcı programı, gereksinimlere göre farklı işletim sistemleri için derlenebilen açık kaynaklı bir motor olarak mevcuttur.

## PEA Dosya Biçimi

[PEA dosya biçimi belirtimleri](https://peazip.github.io/pea_help.pdf), geliştiricinin referansı için herkese açıktır. PEA arşivleri, esnek güvenlik modeline ve sağlama toplamlarından kriptografik olarak güçlü karmalara kadar değişen yedekli bütünlük kontrollerine sahip ikili dosyalardır. Bu, kontrol edilecek üç farklı iletişim seviyesini tanımlar:

* Akışlar - birden çok girdi dosyası tarafından oluşturulan ve birden çok çıktı birimine yazılabilen gerçek çıktı veri akışı
* Nesneler - .pea arşivine gönderilen girdi dosyaları ve klasörler
* Birimler - kullanıcı tanımlı boyuta yayılabilen çıktı arşiv dosyası

Bunların her biri isteğe bağlıdır ve kullanıcı gereksinimlerine göre birleştirilebilir. PEA dosya biçimi, sınırsız nesne içeren tek bir akışı depolayabilir. Her akışın boyutu en fazla 2^64 bayttır.

PEA dosyaları, EAX veya HMAC modunda AES, alternatif olarak EAX modunda Twofish ve Serpent kullanarak isteğe bağlı bütünlük kontrolü ve kimliği doğrulanmış şifreleme sunar.

### PEA Arşiv Başlığı

Arşiv başlığı 10 bayttır ve aşağıdaki gibi yapılandırılmıştır.

|Bayt|Açıklama|
---|---|
|1 | Dosya biçimi belirsizliği giderme için sihirli bayt alanı: $EA|
|1 | Sürüm Numarası|
|1 | Revizyon Numarası|
|1 | Ses kontrol şeması|
|1 | Akışın oluşturulduğu işletim sistemini bildirme|
|1 | OS tarih ve saat kodlamasını bildirme|
|1 | Nesneleri bildirmek karakter kodlaması |
|1 | CPU tipini (7 bit olarak kodlanmış) ve endianlığı (msb cinsinden) bildirme |
|1 | Gelecekte kullanılmak üzere ayrılmıştır|

## Referanslar

* [PEA Dosya Biçimi Özellikleri](https://peazip.github.io/pea_help.pdf)
* [PEA Dosya Biçimi](https://peazip.github.io/pea-file-format.html#.pea_specifications)

