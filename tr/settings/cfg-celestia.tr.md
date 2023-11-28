{
"tarih": "2023-09-27",
  "keywords": [
"cfg",
"cfg dosyası",
"cfg celestia yapılandırma dosyası",
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
"title": "CFG Dosya Formatı - Celestia Yapılandırma Dosyası",
  "description":"CFG Celestia Yapılandırma Dosyası formatı ve CFG dosyalarını oluşturup açabilen API'ler hakkında bilgi edinin.",
"linktitle": "CFG Celestia",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-celestia",
      "parent": "settings"
}
},
"sonmod": "2023-09-27"
}

## .CFG dosyası nedir?

Celestia yapılandırma dosyası, 3 boyutlu evren simülasyon programı Celestia tarafından kullanılan düz metin dosyasıdır. Bu dosyalar Celestia'nın nasıl davranacağını, hangi gök cisimlerinin görüntüleneceğini ve programın nasıl görüneceğini özelleştirmek için hayati öneme sahiptir. Ancak bu dosyaları düzenlemek dikkatli bir dikkat gerektirir çünkü uygunsuz değişiklikler Celestia'nın yükleme sürecini bozabilir ve düzgün çalışmasını engelleyebilir.

## Celestia

Celestia, kullanıcıların evreni son derece gerçekçi ve etkileşimli bir şekilde keşfetmesine ve görselleştirmesine olanak tanıyan ücretsiz, açık kaynaklı 3 boyutlu astronomi simülasyon yazılımıdır. Chris Laurel tarafından geliştirildi ve ilk olarak 2000'li yılların başında piyasaya sürüldü. Celestia, Windows, macOS ve Linux işletim sistemlerinde kullanılabilir.

Celestia'nın temel özellikleri ve yönleri şunları içerir:

- **Gerçekçi 3D Görselleştirme:** Celestia, güneş sistemimizin yanı sıra yıldızların, galaksilerin ve diğer gök cisimlerinin ayrıntılı ve doğru temsilini sağlar. Görsel olarak sürükleyici bir deneyim yaratmak için yüksek kaliteli 3D modeller ve dokular kullanır.

- **Kapsamlı Göksel Veritabanı:** Yazılım, yıldızlar, gezegenler, aylar, asteroitler, kuyruklu yıldızlar ve uzay araçları da dahil olmak üzere bilinen gök cisimlerinden oluşan geniş bir yerleşik veritabanıyla birlikte gelir. Kullanıcılar bu nesneleri kolayca bulabilir ve keşfedebilir.

- **Bilimsel Doğruluk:** Celestia bir görselleştirme aracı olmakla birlikte, gök cisimlerini ve olaylarını mevcut bilimsel verilere dayanarak mümkün olduğunca doğru bir şekilde temsil etmeyi amaçlamaktadır.

## Celestia'nın Kullandığı Dosya Formatları

Celestia, 3 boyutlu astronomi simülasyonunun farklı yönleri için çeşitli dosya formatlarını kullanır. Celestia'nın kullandığı bazı önemli dosya formatları şunlardır:

1. **Yapılandırma Dosyaları (.cel)**
- *Açıklama*: Kullanıcıların Celestia'nın davranışını, görünümünü ve içeriğini özelleştirmesine olanak tanıyan düz metin dosyaları.
- *Amaç*: Ayarları özelleştirmek, konumları tanımlamak ve gök cisimlerini belirlemek.

2. **3D Modeller ve Ağlar**
- *Biçimler*: [.3ds](/tr/3d/3ds/), [.obj](/tr/3d/obj/), [.dae](/tr/3d/dae/), .ac
- *Açıklama*: Gök cisimlerini ve uzay aracını oluşturmak için kullanılan desteklenen 3D model dosya formatları.
- *Amaç*: Celestia'daki 3 boyutlu nesneleri görüntülemek.

3. **Doku Dosyaları**
- *Biçimler*: [.jpg](/tr/image/jpeg/), [.png](/tr/image/png/), [.dds](/tr/image/dds/)
- *Açıklama*: Bu dosyalar gök cisimleri için yüzey dokuları sağlar.
- *Amaç*: Gerçekçi görünüm için dokuları 3D modellere eşlemek.

4. **Yıldız Katalogları ve Veri Dosyaları**
- *Biçimler*: Özel biçimler, [.csv](/tr/spreadsheet/csv/), [.tsv](/tr/spreadsheet/tsv/)
- *Açıklama*: Yıldızları ve diğer gök cisimlerini temsil etmek için kullanılan ve doğru simülasyon sağlayan veri dosyaları.
- *Amaç*: Gök cisimlerinin doğru temsili.

5. **Doku Küp Haritaları**
- *Açıklama*: Küp haritaları, galaksiler gibi uzaktaki gök cisimlerinin görünümünü simüle etmek için kullanılır.
- *Amaç*: Uzaktaki nesneleri gerçekçi dokularla oluşturmak.

6. **Komut Dosyaları**
- *Açıklama*: Bu dosyalar Celestia'nın kodlama dilinde yazılmış özel komut dosyaları içerir.
- *Amaç*: Kullanıcıların Celestia evreninde dinamik etkinlikler ve animasyonlar oluşturmasına olanak sağlamak.

## Celestia yapılandırma dosyası

İşte Celestia yapılandırma dosyasıyla neler yapabileceğinize dair temel bir genel bakış:

1. **Konumunuzu Ayarlama**: Enlem, boylam ve yükseklik parametrelerini kullanarak Dünya üzerindeki konumunuzu belirleyebilirsiniz. Bu, Celestia'nın gece gökyüzünü konumunuzdan doğru bir şekilde görüntülemesine olanak tanır.

```
Location "My Location"
{
    Latitude 40.7128
    Longitude -74.0060
    Altitude 0
}
```

2. **Görüntüleme Seçeneklerinizi Özelleştirme:** Görüş alanı, zaman ayarları ve görüntü oluşturma tercihleri gibi çeşitli görüntüleme seçeneklerini ayarlayabilirsiniz.

```
Viewpoint
{
    Location "My Location"
    Follow "Earth"
    Eye [0.0 0.0 0.0]
    Center [0.0 0.0 0.0]
    Up [0.0 1.0 0.0]
    Fov 45
}

Time
{
    Date "2023-09-25T12:00:00.000Z"
    Clock "Now"
}

Rendering
{
    Atmosphere false
    Stars 7
    Planetshine 0.25
}

```

3. **Göksel Nesneleri Yükleme:** Simülasyonunuza yıldızlar, gezegenler, asteroitler, uzay aracı ve daha fazlası gibi gök cisimlerini ekleyebilirsiniz. Her nesne konfigürasyon dosyasında özellikleriyle birlikte tanımlanır.

```
Star "Sun"
{
    RA 0
    Dec 0
    Distance 0
    AppMag -26.74
    SpectralType "G2V"
}

Planet "Earth"
{
    Parent "Sol"
    Texture "earth.jpg"
    Radius 6371
    EllipticalOrbit
    {
        Period 365.25
        SemiMajorAxis 149.6e6
        Eccentricity 0.017
        Inclination 0
        AscendingNode 0
        ArgOfPericenter 102.94
        MeanAnomaly 100.464
}
}
```

4. **Uzay Gemilerini Tanımlama:** Konum, yön ve 3 boyutlu modeller gibi parametrelerini belirterek kendi kurgusal uzay aracınızı oluşturabilir veya gerçek uzay gemilerini kullanabilirsiniz.

```
Spacecraft "Voyager 1"
{
    Parent "Sol"
    Class "spacecraft"
    Mesh "voyager.3ds"
    Radius 0.01
    EllipticalOrbit
    {
        Period 30700
        SemiMajorAxis 1.08e11
        Eccentricity 0.044
        Inclination 3.4
        AscendingNode 49.0
        ArgOfPericenter 44.0
        MeanAnomaly 35.0
}
}
```

5. **Komut Dosyaları Oluşturma:** Dinamik etkinlikler ve animasyonlar oluşturmak için Celestia'nın özel komut dosyası dilinde komut dosyaları yazabilirsiniz.

## CFG dosyası nasıl açılır?

CFG dosyalarını açan veya referans veren programlar

- (Windows, Mac, Linux) için Celestia (Ücretsiz)

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
* [Celestia](https://en.wikipedia.org/wiki/Celestia)

