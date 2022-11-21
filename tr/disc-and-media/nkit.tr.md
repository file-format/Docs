{
  "date" : "2022-04-01",
  "keywords" :[ "nkit dosyası", "nkit dosya formatı", "nkit dosyası nedir", "dosya", "nkit örneği", "nkit dosya uzantısı","uzantı", "biçim", "nkit alt bilgi", "dosya nkit formatı"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"NKIT dosya formatı ve NKIT dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"NKIT - Disk Görüntüsü Dosya Biçimi",
  "linktitle" : "NKIT",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-04-01"
}

## NKIT dosyası nedir?

Bir NKIT dosyası, NintendoWii ve GameCube oyunlarından çıkarılan verilerin disk görüntüsüdür. NKIT, Nintendo Toolkit formatı içindir. Ortaya çıkan sıkıştırma [ISO](/tr/compression/iso/) dosyası, bu oyunların ana verilerini Dolphin, Swiss ve Nintendont gibi emülatör programlarıyla çalıştırmak için kullanır. NKit, her ikisi de oynanabilirlik ve boyut dikkate alınarak tasarlanmış ham (iso) ve sıkıştırılmış (gcz) dosya formatlarında gelir.

## NKIT Dosya Biçimi

NKit dosya formatı kayıpsız bir formattır ve Nintendo Wii ve GameCube görüntülerini küçültmek ve geri yüklemek için kullanılır. Formatlar, GameCube ve Wii oyunlarının her biri için ISO ve GCZ dosya formatlarında mevcuttur.

|Sistem |Biçim |Desteklenen Donanım |Dolphin Desteklenir |Geri Yüklenebilir 1:1 |Notlar|
---|---|---|---|---|---|
|Oyun Küpü| nkit.iso| Evet |Evet| Evet |Sıkıştırılmış GameCube iso ile aynı|
|Oyun Küpü| nkit.gcz| Hayır| Evet| Evet |GCZ, Dolphin'in kendi blok aranabilir sıkıştırma formatıdır|
|Wii| nkit.iso| Hayır Evet| Evet| RVT-H formatı yalnızca Dolphin|
|Wii| nkit.gcz| Hayır Evet| Evet| GCZ'de RVT-H yalnızca Dolphin'de oynanabilir|

### NKIT Başlığı

NKIT dosya formatı başlığı aşağıdaki gibidir.

|Ofset |Uzunluk |Ad|
---|---|---|
|0x200 |0x4 |NKit Başlığı 'NKIT'|
|0x204 |0x4 |NKit Sürümü ' v01'|
|0x208 |0x4 |Kaynak görüntü orijinal CRC32|
|0x20C |0x4 |NKit CRC - NKit dosyası CRC32'yi 0x208'de (GCZ'de 0x4'te) kaynak CRC'ye eşit yapar|
|0x210 |0x4 |Kaynak görüntü uzunluğu|
|0x214 |0x4 |Zorunlu Önemsiz Kimlik (Disk Kimliği farklı olduğunda - nadir - yalnızca GameCube)|
|0x218 |0x4 |Wii Dönüştürme sırasında kaldırılırsa CRC32 bölümünü güncelleyin|

## Referanslar ##

* [NKIT Dosya Biçimi - gbatemp tarafından](https://wiki.gbatemp.net/wiki/NKit/NKitFormat)

