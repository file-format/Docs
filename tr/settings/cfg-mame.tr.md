{
"tarih": "2023-09-27",
  "keywords": [
"cfg",
"cfg dosyası",
"cfg mame yapılandırma dosyası",
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
"title": "CFG Dosya Formatı - MAME Yapılandırma Dosyası",
  "description":"CFG MAME Yapılandırma Dosyası formatı ve CFG dosyalarını oluşturup açabilen API'ler hakkında bilgi edinin.",
"linktitle" : "CFG MAME",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-mame",
      "parent": "settings"
}
},
"sonmod": "2023-09-27"
}

## .CFG dosyası nedir?

CFG dosyası, MAME arcade video oyunu emülatörleri tarafından kullanılan bir XML klavye yapılandırma dosyasıdır. Klavye kontrollerini ve kısayol tuşlarını oyuncunun tercihlerine uyacak şekilde özelleştirmek için çok önemli bir bileşendir. Bu dosyalar, oyun oynarken klavyenin öykünücüyle nasıl etkileşime gireceğini belirleyen eşlemeleri ve ayarları saklar. Kullanıcılar, bu dosyayı düzenleyerek oyun içindeki jeton atma, başlatma, hareket ve çeşitli diğer işlevler gibi eylemlere belirli klavye tuşlarını atayarak oyun deneyimlerini kişiselleştirebilirler.

## MAME Yapılandırma Dosyası

**Multiple Arcade Machine Emulator** anlamına gelen MAME, bilgisayarınızda atari oyunlarını taklit etmenize ve oynamanıza olanak tanıyan bir yazılım uygulamasıdır. MAME, davranışını ve ayarlarını özelleştirmek için yapılandırma dosyalarını kullanır. Bu yapılandırma dosyaları genellikle MAME dizininizdeki "cfg" klasöründe bulunur.

MAME'yi kurarken ve yapılandırırken karşılaşabileceğiniz ana yapılandırma dosyaları şunlardır:

1. **mame.ini:** Bu, MAME için ana yapılandırma dosyasıdır. Tüm oyunlar için geçerli olan genel ayarları içerir. Bu dosyayı MAME kurulumunuzun kök dizininde bulabilirsiniz.

1. **default.cfg:** Bu dosya, kendi yapılandırma dosyalarına sahip olmayan tüm oyunların varsayılan ayarlarını saklar. Oyuna özel ayarlar için geri dönüş olarak kullanılır.

1. **game-spec.cfg:** Bu dosyalar ayrı oyunların ayarlarını depolamak için kullanılır. Genellikle karşılık geldikleri oyunun ROM dosyasından sonra adlandırılırlar. Örneğin, "pacman.zip" adında bir oyununuz varsa, bunun yapılandırma dosyası "pacman.cfg" olacaktır.

MAME yapılandırma dosyasında bulabileceğiniz bazı genel ayarları burada bulabilirsiniz.

1. **rompath:** Arcade oyunu ROM'larınızın bulunduğu dizini belirtir.

1. **cfg_directory:** Oyuna özel yapılandırma dosyalarının depolandığı dizini belirtir.

1. **nvram_directory:** Kalıcı RAM (NVRAM) dosyalarının depolandığı dizini belirtir. NVRAM, yüksek puanları ve oyuna özgü diğer verileri saklar.

1. **artwork_directory:** Resim dosyalarının (çerçeveler, çerçeveler ve el ilanları gibi) depolandığı dizini belirtir.

1. **samplepath:** Örnek ses dosyalarının bulunduğu dizini belirtir.

1. **cheatpath:** Hile dosyalarının bulunduğu dizini belirtir.

Ayrıca video ve ses seçenekleri, kontroller ve giriş aygıtları gibi diğer çeşitli ayarları da yapılandırabilirsiniz. Bu ayarları değiştirmek için konfigürasyon dosyasını metin editöründe açıp gerekli değişiklikleri yapabilirsiniz.

## MAME

**"Multiple Arcade Machine Emulator"** anlamına gelen MAME, eski atari makinelerinin ve atari oyun konsollarının donanımını taklit etmek ve kopyalamak için tasarlanmış bir yazılım uygulamasıdır. Kullanıcıların modern bilgisayarlarda ve diğer uyumlu cihazlarda geniş klasik atari oyunları kütüphanesini oynamasına olanak tanır. MAME, açık kaynaklı bir projedir ve atari oyunlarının zengin geçmişini korumak ve keyfini çıkarmak için başvurulacak emülatör haline gelmiştir.

1. **Emülasyon:** MAME'nin birincil amacı, merkezi işlem birimleri (CPU'lar), ses yongaları, grafik yongaları ve giriş aygıtları dahil olmak üzere atari salonu makinelerinin donanımını doğru bir şekilde taklit etmektir. Bu doğruluk düzeyi, oyunların mümkün olduğunca orijinal atari salonu deneyimine yakın davranmasını sağlar.

1. **Uyumluluk:** MAME, çok çeşitli atari oyunu ROM'larını destekler ve bu da onu mevcut en kapsamlı atari salonu emülatörlerinden biri yapar. 70'li, 80'li, 90'lı yılların klasik oyunları ve hatta daha yeni atari oyunları da dahil olmak üzere çeşitli atari platformlarındaki oyunları çalıştırabilir.

1. **Koruma:** MAME'in öncelikli görevlerinden biri atari salonu oyunlarının geçmişini korumaktır. MAME, atari salonu donanımını doğru bir şekilde taklit ederek klasik oyunların kaybolmasını önlemeye yardımcı olur ve gelecek nesillerin bu oyunları başlangıçta amaçlandığı gibi deneyimleyebilmesini sağlar.

1. **Ön Uçlar:** Birçok kullanıcı, MAME aracılığıyla oyunları yönetmek ve başlatmak için grafik arayüz sağlayan ön uç uygulamalardan yararlanır. Bu ön uçlar, MAME'in kapsamlı oyun kitaplığında gezinmeyi kolaylaştırır.

## CFG dosyası nasıl açılır?

CFG dosyalarını açan veya referans veren programlar

- MAME (Ücretsiz) (Windows)
- ExtraMAME (Deneme)
-MacMAME (MAC)

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
* [MAME](https://en.wikipedia.org/wiki/MAME)

