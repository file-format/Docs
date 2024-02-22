{
  "date" : "2021-09-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"OSR dosya formatı ve OSR dosyalarını oluşturup açabilen API'ler hakkında bilgi edinin.",
  "title" : "OSR Dosyası - osu! Tekrar Dosya Formatı",
  "linktitle" : "OSR",
  "menu" : {
    "docs" : {
      "identifier":"game-osr-tr",
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## OSR dosyası nedir?

An OSR file is a game replay file created by the [osu! game](https://osu.ppy.sh/home). Osu! is a rhythm game where users match mouse clicks with the music. The song played by the user, hits and misses, time and date of song played, and overall ranking is recorded in the OSR file. This OSR file can then be shared with others for replay purpose. OSR file requires the beatmap file to be present in the "Songs" folder.

**MIME OSR Dosya Formatı Türü:** x-osu-replay

## OSR Dosya Formatı

OSR dosyaları, sabit ve değişken uzunluktaki veri alanlarına sahip ikili dosyalar olarak kaydedilir.

|Veri Türü| Biçim|
---|---|
|Byte |Tekrarın oyun modu (0 = osu! Standart, 1 = Taiko, 2 = Ritmi Yakala, 3 = osu!mania)|
|Tamsayı |Tekrarın oluşturulduğu andaki oyunun sürümü (ör. 20131216)|
|Dize |osu! beatmap MD5 hash|
|Dize| Oyuncu adı|
|Dize| işte! tekrar oynatma MD5 karması (yeniden oynatmanın belirli özelliklerini içerir)|
|Kısa| 300'lü Sayı|
|Kısa| Standartta 100'lü, Taiko'da 150'li, CTB'de 100'lü, mania'da 100'lü sayı|
|Kısa| Standartta 50'li sayı, CTB'de küçük meyve, manide 50'li sayı|
|Kısa| Standart Geki sayısı, Mania'da maksimum 300|
|Kısa| Standartta Katus sayısı, manide 200'ler |
|Kısa| Kaçırılanların sayısı|
|Tamsayı| Puan raporunda görüntülenen toplam puan|
|Kısa| Skor raporunda görüntülenen en iyi kombo|
|bayt| Mükemmel/tam kombinasyon (1 = eksik yok, kaydırıcı kırılması yok ve kaydırıcının erken bitirilmesi yok)|
|Tamsayı| Kullanılan modlar. Mod değerlerinin listesi için aşağıya bakın.|
|Dize| Yaşam çubuğu grafiği: virgülle ayrılmış u/v çiftleri; burada u şarkının milisaniye cinsinden süresidir ve v, belirli bir zamanda sahip olduğunuz yaşam miktarını temsil eden 0 - 1 arasında kayan nokta değeridir (0 = yaşam çubuğu boş, 1= yaşam çubuğu dolu)|
|Uzun| Zaman damgası (Windows işaretleri)|
|Tamsayı| Sıkıştırılmış tekrar verilerinin bayt cinsinden uzunluğu|
|Bayt |Dizi Sıkıştırılmış tekrar oynatma verileri|
|Uzun| Çevrimiçi Puan Kimliği|
|Çift| Ek mod bilgileri. Yalnızca Hedef Uygulama etkinse mevcuttur.|

## Referanslar

* [OSU! Ritim Oyunu](https://osu.ppy.sh/home)

* [OSR Dosya Formatı](https://osu.ppy.sh/wiki/en/Client/File_formats/Osr_%28file_format%29#data-types)


