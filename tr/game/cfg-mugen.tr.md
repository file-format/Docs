{
"tarih": "2023-09-27",
  "keywords": [
"cfg",
"cfg dosyası",
"cfg mugen yapılandırma dosyası",
"cfg dosyası nedir",
"cfg dosyası nasıl açılır",
"dosya",
"cfg dosya uzantısı",
"eklenti"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "CFG Dosya Formatı - MUGEN Yapılandırma Dosyası",
  "description":"CFG MUGEN Yapılandırma Dosyası formatı ve CFG dosyalarını oluşturup açabilen API'ler hakkında bilgi edinin.",
"linktitle" : "CFG M.U.G.E.N",
  "menu": {
    "docs": {
      "identifier": "game-cfg-mugen",
      "parent": "game"
}
},
"sonmod": "2023-09-27"
}

## .CFG dosyası nedir?

MUGEN bağlamındaki CFG dosyası "MUGEN Yapılandırma Dosyası" anlamına gelir. **MUGEN**, Elecbyte tarafından geliştirilen özelleştirilebilir 2D dövüş oyunu motorudur. Kullanıcılar CFG dosyaları da dahil olmak üzere çeşitli konfigürasyon dosyalarını düzenleyerek kendi karakterlerini, aşamalarını oluşturabilir ve hatta oyunun davranışını ve kurallarını değiştirebilirler.

MUGEN `.cfg` dosyasında neler bulabileceğinize dair temel bir bakış:

1. **Sistem Yapılandırması**: CFG dosyaları genellikle oyun motorunun genel davranışıyla ilgili ayarları içerir. Buna ekran çözünürlüğü, ses ayarları ve giriş yapılandırması (klavye, oyun çubuğu veya denetleyici eşlemeleri) gibi şeyler dahildir.
    








2. **Karakter ve Sahne Varsayılanları**: Karakterler ve aşamalar için varsayılan ayarları tanımlayabilirsiniz. Örneğin oyun başladığında hangi karakterlerin ve aşamaların yükleneceğini belirleyebilirsiniz.
    








3. **Oyun Seçenekleri**: MUGEN `.cfg` dosyaları aynı zamanda tur süresi sınırları, hasar ölçeklendirmesi ve daha fazlası gibi çeşitli oyun seçeneklerini de kontrol edebilir.
    








4. **Hata Ayıklama ve Geliştirme**: İleri düzey kullanıcılar, hata ayıklama ve geliştirme amacıyla `.cfg' dosyalarını kullanabilir. Bu ayarlar, hata ayıklama bilgilerinin ekranda nasıl görüntüleneceğini kontrol edebilir veya geliştirmeyle ilgili diğer davranışları tanımlayabilir.
    








5. **Ekran Paketi Yapılandırması**: Ekran paketleri, oyunun görünümünü ve hissini değiştiren görsel temalardır. `.cfg` dosyaları hangi ekran paketinin kullanıldığını belirleyebilir ve çeşitli öğelerini yapılandırabilir.
    








6. **Yapay Zeka Davranışı**: MUGEN, bilgisayar kontrollü karakterlerin (AI) savaşlarda nasıl davranacağını tanımlamanıza olanak tanır. `.cfg` dosyaları AI zorluğu ve davranışıyla ilgili ayarları içerebilir.

## MUGEN Yapılandırma Dosyası

Bir MUGEN CFG (Yapılandırma) dosyası, özel dövüş oyunları dünyasındaki yaratıcılar için çok önemli bir bileşendir. Onlara oyunlarının temel kurallarını şekillendirme gücü verir. Bu, her turun ne kadar süreceği, bilgisayar kontrollü rakiplerin sunduğu mücadele düzeyi, oyunun hızı, kombinasyonların hasarı ne ölçüde etkilediği ve çok daha fazlası gibi faktörleri içerir.

Ayrıca CFG dosyası, yaratıcıların ekran çözünürlüğü gibi oyunun görüntü ayarlarını belirlemesine ve MUGEN'in oyun sırasında ses efektleri ve müzik oynatıp oynatmayacağına karar vermesine olanak tanır. MUGEN'in inceliklerini iyi bilenler için bu dosya, benzersiz bir oyun deneyimi oluşturmak için oyunla ilgili diğer bir dizi ayarda ince ayar yapma potansiyeli sunuyor.

Varsayılan olarak MUGEN'in 'mugen.cfg' olarak bilinen birincil CFG dosyası programın veri klasöründe bulunur. Bu dosya içerisinde oyunun ayarlarını doğrudan düzenlemek mümkün olsa da, genellikle ilk önce yedek kopyanın oluşturulması tavsiye edilir. Bu önlem, gerektiğinde MUGEN'i zahmetsizce orijinal ayarlarına döndürebilmenizi ve istenmeyen değişikliklerin oyun deneyiminizi bozmasını önlemenizi sağlar.

## MUGEN - Oyun Motoru

MUGEN, Elecbyte tarafından geliştirilen çok yönlü ve son derece özelleştirilebilir 2D dövüş oyunu motorudur. "MUGEN" adı "Mugen Ultimate Game Engine" anlamına gelir. İlk olarak 1999'da piyasaya sürüldü ve o zamandan beri motoru kullanarak kendi 2D dövüş oyunlarını tasarlayan ve geliştiren özel kullanıcı ve yaratıcılardan oluşan bir topluluk kazandı.

MUGEN'in bazı temel özellikleri ve yönleri şunlardır:

1. **Özelleştirilebilir Karakterler:** MUGEN, kullanıcıların kendi karakterlerini ("savaşçılar" veya "sprite" olarak bilinir) oluşturmalarına ve oyuna aktarmalarına olanak tanır. Yaratıcılar bu karakterler için benzersiz hareket setleri, animasyonlar ve özel saldırılar tasarlayabilir; böylece çeşitli serilerden veya orijinal yaratımlardan hemen hemen her karakter dahil edilebilir.
    








2. **Aşamalar:** Kullanıcılar, karakterlerin yanı sıra savaşların gerçekleştiği aşamaları da oluşturabilir ve özelleştirebilir. Bu aşamalar etkileşimli öğelere ve benzersiz arka planlara sahip olabilir.
      









3. **Ekran Paketleri:** Ekran paketleri, menüler, karakter seçim ekranları ve yaşam çubukları da dahil olmak üzere oyunun genel görünümünü değiştiren görsel temalardır. Kullanıcılar, oyunlarına benzersiz bir görünüm ve his kazandırmak için kendi ekran paketlerini oluşturabilir ve paylaşabilirler.
    








4. **Ses ve Müzik:** İçerik oluşturucular oyunlarına ses efektleri ve arka plan müziği ekleyerek genel oyun deneyimini geliştirebilir.
    








5. **Komut Dosyası Oluşturma:** İleri düzey kullanıcılar, karmaşık karakter davranışları, benzersiz oyun mekaniği ve özel efektler oluşturmak için yerleşik komut dosyası dilini kullanabilir.

## CFG dosyası nasıl açılır?

MUGEN CFG dosyaları, çeşitli metin editörleriyle erişilebilmelerini sağlayan düz metin belgeleridir. Windows'ta Microsoft Notepad veya WordPad'i kullanabilirken, macOS kullanıcıları bu amaçla Apple TextEdit'i kullanabilir. Bu düzenleyiciler, kullanıcıların CFG dosyalarındaki yapılandırma ayarlarını kolayca görüntülemesine ve değiştirmesine olanak tanır.

CFG dosyalarını açan veya referans veren programlar

- Elecbyte MUGEN
- Not Defteri
- Metin Düzenleme

## Diğer CFG dosyaları

**.cfg** dosya uzantısını kullanan diğer dosya türleri şunlardır.

**Ayarlar**
- [CFG - Celestia Yapılandırma Dosyası](/tr/settings/cfg-celestia/)
- [CFG - Citrix Sunucusu Bağlantı Dosyası](/tr/settings/cfg-citrix/)
- [CFG - MAME Yapılandırma Dosyası](/tr/settings/cfg-mame/)
- [CFG - LightWave Yapılandırma Dosyası](/tr/settings/cfg-lightwave/)

**Oyun**
- [CFG - Wesnoth İşaretleme Dili Dosyası](/tr/game/cfg-wesnoth/)
- [CFG - MUGEN Yapılandırma Dosyası](/tr/game/cfg-mugen/)
- [CFG - Kaynak Motoru Yapılandırma Dosyası](/tr/game/cfg-sourceengine/)

**Sistem ve Çeşitli**
- [CFG - CFG Dosyası](/tr/system/cfg/)
- [CFG - Cal3D Model Yapılandırma Dosyası](/tr/misc/cfg-cal3d/)

## Referanslar
* [Mugen (oyun motoru)](https://en.wikipedia.org/wiki/Mugen_(game_engine))

