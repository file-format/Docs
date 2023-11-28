{
"tarih": "2023-09-27",
  "keywords": [
"cfg",
"cfg dosyası",
"cfg kaynak motor yapılandırma dosyası",
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
"title": "CFG Dosya Formatı - Kaynak Motor Yapılandırma Dosyası",
  "description":"CFG Kaynak Motoru Yapılandırma Dosyası formatı ve CFG dosyalarını oluşturup açabilen API'ler hakkında bilgi edinin.",
"linktitle": "CFG Kaynak Motoru",
  "menu": {
    "docs": {
      "identifier": "game-cfg-sourceengine",
      "parent": "game"
}
},
"sonmod": "2023-09-27"
}

## .CFG dosyası nedir?

**Valve's Source Engine** bağlamındaki CFG dosyası, Half-Life 2 gibi oyunlarda görüldüğü gibi yapılandırma dosyası görevi görür. Bu dosyalar, düz metin komutları listesi aracılığıyla çeşitli oyun içi ayarları değiştirmek için kullanılır. Bu komutlar genellikle her satıra bir tane gelecek şekilde düzenlenir ve oyunun bazı yönlerinin özelleştirilmesinden sorumludur.

Oyuncular ve sunucu yöneticilerinin `.cfg` dosyasında belirtilen değişiklikleri uygulamak için birkaç seçeneği vardır:

1. **Manuel Yürütme**: Kullanıcılar CFG dosyasındaki komutları manuel olarak yürütebilir. Bu, oyunun Geliştirici Konsoluna her komutu tek tek girdikleri anlamına gelir. Bu yöntem, hangi ayarların ne zaman değiştirileceği konusunda hassas kontrol sağlar.
    





2. **Otomatik Yürütme**: Alternatif olarak, oyuncular otomatik yürütmeyi tercih edebilir. Bu, `.cfg' dosyasının uygun oyun dizinine yerleştirilmesini içerir. 'autoexec.cfg' gibi belirli '.cfg' dosyaları oyun başlatıldığında otomatik olarak yürütülür. Bu, oyun her başlatıldığında belirtilen ayarların manuel giriş gerektirmeden uygulanmasını sağlar.

## Valf Kaynağı Motoru

Genellikle basitçe **Source Engine** olarak anılan Valve Source Engine, Valve Corporation tarafından geliştirilen çok yönlü ve yaygın olarak kullanılan bir oyun motorudur. Birçok popüler video oyununun temelini oluşturdu ve çok sayıda başarılı oyuna güç verdi. Valve Source Engine ile ilgili bazı önemli noktalar şunlardır:

1. **Tarih**: Source Engine, ilk olarak 2004 yılında Valve'ın "Counter-Strike 1.6" oyununun piyasaya sürülmesiyle tanıtıldı. O zamandan bu yana birçok güncelleme ve revizyondan geçti ve en son sürümü Source 2.0 olarak biliniyor.
    





2. **Önemli Oyunlar**: Source Engine, aşağıdakiler dahil ancak bunlarla sınırlı olmamak üzere, eleştirmenlerce beğenilen çeşitli oyunlarda kullanılmıştır:
    





- "Half-Life 2" ve bölümleri
- "Portal" ve "Portal 2"
- "Takım kalesi 2"
- "Sol 4 Ölü" ve "Sol 4 Ölü 2"
- "Counter-Strike: Source" ve "Counter-Strike: Global Offensive"
- "Dota2"
3. **Özellikler**:
    





- **Esneklik**: Source Engine, geliştiricilerin birinci şahıs nişancı oyunlarından bulmaca oyunlarına ve daha fazlasına kadar çok çeşitli oyun türleri oluşturmasına olanak tanıyan esnekliğiyle bilinir.
- **Fizik**: Gerçekçi nesne etkileşimlerine ve çevresel etkilere olanak tanıyan sağlam fizik motoru içerir.
- **Modlama Desteği**: Motor, kullanıcı tarafından oluşturulan çok sayıda içerik ve oyun modunun oluşturulmasına yol açan güçlü modlama desteğine sahiptir.
- **Çok Oyunculu Yetenekler**: Source Engine, hem tek oyunculu hem de çok oyunculu oyunları geliştirmek için kullanılmıştır ve çevrimiçi oyun için kapsamlı ağ oluşturma yetenekleri sunar.
    





4. **Grafikler**: Yıllar geçtikçe Source Engine, gelişen donanım özelliklerine ayak uydurmak için grafik güncellemeleri aldı. HDR (Yüksek Dinamik Aralık) aydınlatma ve dinamik gölgeler gibi gelişmiş işleme tekniklerini destekler.

## CFG dosyası nasıl açılır?

Microsoft Visual Studio Code gibi metin düzenleyicileri veya seçtiğiniz başka bir metin düzenleyiciyi kullanarak `.cfg` dosyasını açma ve değiştirme seçeneğiniz vardır. Bu metin düzenleyicileri, '.cfg' dosyasındaki düz metin komutlarını görüntülemek ve düzenlemek için kullanıcı dostu bir arayüz sağlar ve ayarları gerektiği gibi özelleştirmenize olanak tanır.

CFG dosyalarını açan veya referans veren programlar şunları içerir:

- Microsoft Visual Studio Kodu
- Not Defteri
- Metin Düzenleme
- Herhangi bir metin editörü

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
* [Kaynak (oyun motoru)](https://en.wikipedia.org/wiki/Source_(game_engine))

