{
  "date" : "2023-01-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"OSU dosya formatı ve OSU dosyalarını oluşturup açabilen API'ler hakkında bilgi edinin.",
  "title" : "OSU Dosyası - Osu! Komut Dosyası Formatı",
  "linktitle" : "OSU",
  "menu" : {
    "docs" : {
      "identifier":"game-osu-tr",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-18"
}

## .OSU dosyası nedir?

Bir OSU dosyası, osu için yazılmış bir oyun betiğidir! ritim oyunu. Zorluk seviyesi, çalınacak şarkı ve oyuncunun müzikle senkronize etmesi gereken vurulan nesnelerin zamanlamaları gibi oyunda kullanılan bir ritim haritası hakkında bilgiler içerir. Ritim oyunu oyuncularının özel zorluklar geliştirmesine ve oyun topluluğuyla paylaşmasına olanak tanır.

**MIME OSR Dosya Formatı Türü:** x-osu-beatmap

## OSU Dosya Formatı

OSU dosyaları diske düz metin dosyaları olarak kaydedilir ve yapısı osu!'nun [OSU file format](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29) dosyasında çok açık bir şekilde tanımlanır.

### OSU Dosyasındaki Bölümler

Tipik bir OSU dosyası aşağıdaki bölümlere sahiptir.

|Bölüm |Açıklama |İçerik türü|
---|---|---|
|[Genel]| Beatmap hakkında genel bilgi| anahtar: değer çiftleri|
|[Editör]| Beatmap düzenleyicisi için kayıtlı ayarlar| anahtar: değer çiftleri|
|[Meta veriler] |Vuruş haritasını tanımlamak için kullanılan bilgiler| anahtar:değer çiftleri|
|[Zorluk] |Zorluk ayarları| anahtar:değer çiftleri|
|[Etkinlikler]| Beatmap ve storyboard grafik etkinlikleri| Virgülle ayrılmış listeler|
|[ZamanlamaPuanları]| Zamanlama ve kontrol noktaları| Virgülle ayrılmış listeler|
|[Renkler]| Kombinasyon ve ten renkleri| anahtar : değer çiftleri|
|[HitObjects]| Nesnelere çarpma| Virgülle ayrılmış listeler|

## Referanslar

* [OSU! Ritim Oyunu](https://osu.ppy.sh/home)

* [OSU dosya formatı](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29)


