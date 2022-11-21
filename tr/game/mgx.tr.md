{
  "date" : "2021-09-08",
  "keywords" :[ "mgx dosyası", "mgx dosya biçimi", "mgx dosyası nedir", "dosya", "mgx örneği", "mgx dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Age of Empires 2 Expansion Replay MGX dosya formatı ve MGX dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"MGX - Age of Empires 2 Genişletme Tekrarı",
  "linktitle" : "MGX",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## MGX dosyası nedir?

.mgx uzantılı bir dosya, Age of Empires II: The Conquerors oyunu için kaydedilmiş bir dosyadır ve Age of Empires II programında tekrar oynatılabilir. Kullanıcı tarafından oynanan kampanyanın tam kaydını içerir. Age of Empires II programında yüklenebilir ve oynatılabilir. Tekrar oynandığında oyun, kullanıcının kampanya için planladığı ve oynadığı tüm olayları ve senaryoları gösterir.

## MGX Dosya Biçimi - Daha Fazla Bilgi

MGX dosyasının dahili dosya formatı üzerinde çalışılmıştır ve [Age of Empires 2: The Conquerors — Savegame File Format Spesifikasyonu](https://github.com/stefan-kolb/aoc-mgx-) hakkında kısmen doğrulanmış bilgi olarak mevcuttur. biçim). Spesifikasyonlar, aşağıdaki bölümlerde ayrıntıları özetlemektedir.

### Yapı Tanımları

GPX dosya biçiminin yapı tanımlarının, yapılandırılmış ikili verileri okumak ve yazmak için bir yol sağlayan [BinData Ruby Gem bildirimlerine](https://github.com/dmendel/bindata/wiki) dayandığına inanılmaktadır. Bu, programcının daha sonra BinData tarafından okunan ve yazılan ikili verilerin biçimini belirlemesini sağlar.

### MGX Mesajlaşma

MGX mesajlaşması iki tür mesaja dayanmaktadır.

* GAMESTART - oyun başlatma komutlarını belirtir ve bugüne kadar doğrulanmamıştır
* CHAT - oyun içi sohbet mesajlarını açıklar. Hem oyuncular hem de oyunun kendisi (Gaia) oyun içi mesajlar gönderebilir.

### OYUN EYLEMLERİ

Alınan ve ayrıntıları mevcut olan birkaç [GAMEPLAY Eylemi](https://github.com/stefan-kolb/aoc-mgx-format/blob/master/README.md#actions) vardır.

## Referanslar

* [Age of Empires 2: The Conquerors — Savegame Dosya Biçimi Belirtimi](https://github.com/stefan-kolb/aoc-mgx-format)

