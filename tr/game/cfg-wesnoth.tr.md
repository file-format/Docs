{
"tarih": "2023-09-27",
  "keywords": [
"cfg",
"cfg dosyası",
"cfg wesnoth biçimlendirme dili dosyası",
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
"title": "CFG Dosya Formatı - Wesnoth İşaretleme Dili Dosyası",
  "description":"CFG Wesnoth İşaretleme Dili Dosya formatı ve CFG dosyalarını oluşturup açabilen API'ler hakkında bilgi edinin.",
"linktitle" : "CFG Wesnoth",
  "menu": {
    "docs": {
      "identifier": "game-cfg-wesnoth",
      "parent": "game"
}
},
"sonmod": "2023-09-27"
}

## .CFG dosyası nedir?

CFG dosyası aynı zamanda **"Wesnoth İşaretleme Dili" (WML)** olarak da bilinir. Öncelikle sıra tabanlı bir strateji oyunu olan "Battle for Wesnoth" oyununda kullanılan özel bir işaretleme dilidir. WML, senaryolar, kampanyalar, birimler ve daha fazlası dahil olmak üzere oyunun çeşitli yönlerini tanımlamak ve özelleştirmek için kullanılır. Mod geliştiricilerin ve geliştiricilerin oyun için içerik oluşturmasının bir yoludur.

XML ve basit komut dosyası oluşturmanın birleşimine benzeyen bir formatta yazılmıştır. Bir WML dosyasında bulabileceğiniz bazı ortak öğelere ve yapılara genel bakış:

1. **Etiketler:** WML, oyundaki farklı öğeleri tanımlamak için etiketleri kullanır. Etiketler köşeli parantez içine alınmıştır. Örneğin:

```
[unit]
    type=Elvish Archer
    hitpoints=25
[/unit]
```
    










2. **Öznitelikler:** Etiketlerin içinde, öğeyle ilişkili özellikleri veya değerleri belirtmek için öznitelikler tanımlayabilirsiniz. Yukarıdaki örnekte "tür" ve "isabet noktaları" özelliklerdir.
    










3. **Diziler ve Dizi Dizileri:** Birim listelerini, arazi türlerini veya diğer oyun öğelerini tanımlamak için veri dizileri ve hatta dizi dizileri oluşturabilirsiniz.
    










4. **Koşullu İfadeler:** WML, oyunun akışını kontrol etmek için koşullu ifadeleri destekler. Örneğin:

```
[if]
    condition=have_unit
    variable=x,y
[/if]
```
    










5. **Döngüler:** Öğe listeleri arasında yineleme yapmak veya eylemleri tekrar tekrar gerçekleştirmek için döngüleri kullanabilirsiniz.
    










6. **Şunları içerir:** İçeriğinizi düzenlemek ve modüler hale getirmek için ana WML dosyasına diğer WML dosyalarını dahil edebilirsiniz.
    










7. **Olay İşleyicileri:** Oyunda belirli olaylar meydana geldiğinde eylemleri tetikleyecek olay işleyicilerini tanımlayabilirsiniz.
    











Özel bir birimi tanımlayan basitleştirilmiş bir WML dosyası örneği:

```
[unit_type]
    id=my_custom_unit
    name="Custom Unit"
    description="A unit created using WML."
    image="units/my_custom_unit.png"
    hitpoints=30
    movement_type=foot
[/unit_type]
```

## Wesnoth Savaşı

"Wesnoth Savaşı" popüler ve açık kaynaklı, sıra tabanlı bir strateji oyunudur. Mac, Windows, Linux ve daha fazlası dahil olmak üzere birden fazla platform için kullanılabilir. Gönüllülerden oluşan özel bir topluluk tarafından geliştirilen oyun, derin ve ilgi çekici oynanışının yanı sıra zengin fantastik dünyasıyla da tanınıyor.

"Wesnoth Savaşı"nın temel özellikleri şunlardır:

1. **Fantazi Ortamı:** Oyun, insanlar, elfler, cüceler, orklar ve daha fazlası dahil olmak üzere çeşitli ırkların yer aldığı bir fantezi dünyasında geçiyor. Oyunun bilgisi ve hikaye anlatımı, çekiciliğinin ayrılmaz bir parçasıdır.
    










2. **Sıra Tabanlı Strateji:** Oyun, oyuncuların altıgen ızgaralar üzerinde hareketlerini planlamak ve gerçekleştirmek için zaman ayırdığı sıra tabanlıdır. Taktik mücadeleyi stratejik karar alma ile birleştirir.
    










3. **Kampanyalar:** Oyun, her birinin kendi hikayesi, karakterleri ve zorlukları olan çok çeşitli tek oyunculu kampanyalar sunar. Oyuncular farklı anlatıları ve senaryoları keşfedebilirler.
    










4. **Çok oyunculu:** "Wesnoth" çevrimiçi çok oyunculu oyunu destekleyerek oyuncuların stratejik savaşlarda birbirleriyle rekabet etmelerine olanak tanır. Çok oyunculu modlar, işbirlikçi oyun ve rekabetçi maçları içerir.

## CFG dosyası nasıl açılır?

Genellikle "The Battle for Wesnoth" oyununda kullanılan Wesnoth İşaretleme Dili (WML) ile ilişkilendirilen CFG dosyaları, herhangi bir standart metin düzenleyici kullanılarak kolayca düzenlenebilir. Bu dosyalar, senaryolar, birimler ve kampanyalar dahil olmak üzere oyunun çeşitli yönlerini tanımlayan, WML'de yazılmış, insanlar tarafından okunabilen kod içerir.

CFG dosyalarını değiştirmek için herhangi bir metin düzenleyiciyi kullanabilseniz de, Emacs ve Vi gibi bazı gelişmiş metin düzenleyicilerde WML sözdizimi vurgulama eklentileri mevcuttur. Bu eklentiler, kullanıcıların WML kodu içindeki farklı öğeleri ve yapıları ayırt etmesini kolaylaştırmak için yararlı renk kodlaması ve biçimlendirme sağlar.

CFG dosyalarını açan veya referans veren programlar şunları içerir:

- Wesnoth Savaşı (Ücretsiz) (Windows, MAC, Linux)
- Microsoft Not Defteri

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
* [The Battle for Wesnoth](https://en.wikipedia.org/wiki/The_Battle_for_Wesnoth)
