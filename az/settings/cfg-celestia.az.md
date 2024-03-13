{
  "date": "2023-09-27",
  "keywords": [
"cfg",
"cfg faylı",
"cfg celestia konfiqurasiya faylı",
"cfg faylı nədir",
"cfg faylını necə açmaq olar",
"fayl",
"cfg fayl uzantısı",
"uzadılması"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "CFG Fayl Format - Celestia Konfiqurasiya Faylı",
  "description": "CFG Celestia Konfiqurasiya Faylı formatı və CFG fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "CFG Celestia",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-celestia-az",
      "parent": "settings"
}
},
  "lastmod": "2023-09-27"
}

## CFG faylı nədir?

Celestia konfiqurasiya faylı Celestia, 3D kainat simulyasiya proqramı tərəfindən istifadə edilən sadə mətn faylıdır. Bu fayllar Celestia-nın necə davrandığını, hansı göy cisimlərinin göstərildiyini və proqramın necə göründüyünü fərdiləşdirmək üçün çox vacibdir. Bununla belə, bu faylları redaktə etmək diqqətli diqqət tələb edir, çünki düzgün olmayan dəyişikliklər Celestia-nın yükləmə prosesini poza və onun düzgün işləməsinə mane ola bilər.

## Selestiya

Celestia pulsuz, açıq mənbəli 3D astronomiya simulyasiya proqramıdır və istifadəçilərə kainatı yüksək dərəcədə realist və interaktiv şəkildə araşdırmağa və vizuallaşdırmağa imkan verir. Chris Laurel tərəfindən hazırlanmış və ilk dəfə 2000-ci illərin əvvəllərində buraxılmışdır. Celestia Windows, macOS və Linux əməliyyat sistemləri üçün əlçatandır.

Celestia-nın əsas xüsusiyyətləri və aspektləri bunlardır:

- **Real 3D Vizuallaşdırma:** Celestia günəş sistemimizi, həmçinin ulduzları, qalaktikaları və digər göy cisimlərini ətraflı və dəqiq təsvir edir. Vizual olaraq immersiv təcrübə yaratmaq üçün yüksək keyfiyyətli 3D modellər və fakturalardan istifadə edir.

- **Geniş Göy Məlumat Bazası:** Proqram təminatı ulduzlar, planetlər, aylar, asteroidlər, kometlər və kosmik gəmilər də daxil olmaqla məlum göy cisimlərinin geniş daxili verilənlər bazası ilə gəlir. İstifadəçilər bu obyektləri asanlıqla tapa və araşdıra bilərlər.

- **Elmi Dəqiqlik:** Celestia vizuallaşdırma vasitəsi olsa da, mövcud elmi məlumatlara əsaslanaraq, göy cisimlərini və hadisələrini mümkün qədər dəqiq şəkildə təqdim etmək məqsədi daşıyır.

## Celestia tərəfindən istifadə olunan fayl formatları

Celestia 3D astronomiya simulyasiyasının müxtəlif aspektləri üçün müxtəlif fayl formatlarından istifadə edir. Celestia tərəfindən istifadə edilən bəzi əsas fayl formatları bunlardır:

1. **Konfiqurasiya Faylları (.cel)**
- *Təsvir*: İstifadəçilərə Celestia-nın davranışını, görünüşünü və məzmununu fərdiləşdirməyə imkan verən sadə mətn faylları.
- *Məqsəd*: Parametrlərin fərdiləşdirilməsi, yerlərin müəyyən edilməsi və göy cisimlərinin təyin edilməsi.

2. **3D Modellər və Meshlər**
- *Formatlar*: [.3ds](/3d/3ds/), [.obj](/3d/obj/), [.dae](/3d/dae/), .ac
- *Təsvir*: Göy cisimlərini və kosmik gəmiləri göstərmək üçün istifadə edilən dəstəklənən 3D model fayl formatları.
- *Məqsəd*: Celestia daxilində 3D obyektlərin göstərilməsi.

3. **Doku faylları**
- *Formatlar*: [.jpg](/image/jpeg/), [.png](/image/png/), [.dds](/image/dds/)
- *Təsvir*: Bu fayllar göy cisimləri üçün səth fakturaları təmin edir.
- *Məqsəd*: Real görünüş üçün dokuları 3D modellərə uyğunlaşdırmaq.

4. **Ulduz Kataloqları və Məlumat Faylları**
- *Formatlar*: Fərdi formatlar, [.csv](/spreadsheet/csv/), [.tsv](/spreadsheet/tsv/)
- *Təsvir*: Dəqiq simulyasiyanı təmin edən ulduzları və digər göy cisimlərini təmsil etmək üçün istifadə edilən məlumat faylları.
- *Məqsəd*: Göy cisimlərinin dəqiq təsviri.

5. **Texture Cube Xəritələri**
- *Təsvir*: Kub xəritələri qalaktikalar kimi uzaq səma cisimlərinin görünüşünü simulyasiya etmək üçün istifadə olunur.
- *Məqsəd*: Uzaq obyektləri real teksturalarla göstərmək.

6. **Skript Faylları**
- *Təsvir*: Bu fayllar Celestia-nın skript dilində yazılmış xüsusi skriptləri ehtiva edir.
- *Məqsəd*: İstifadəçilərə Celestia kainatında dinamik hadisələr və animasiyalar yaratmağa imkan vermək.

## Celestia konfiqurasiya faylı

Celestia konfiqurasiya faylı ilə nə edə biləcəyinizin əsas icmalı:

1. **Yerinizin qurulması**: Siz enlik, uzunluq və hündürlük parametrlərindən istifadə edərək Yer kürəsində yerinizi təyin edə bilərsiniz. Bu, Celestia-ya gecə səmasını mövqeyinizdən dəqiq göstərməyə imkan verir.

```
Location "My Location"
{
    Latitude 40.7128
    Longitude -74.0060
    Altitude 0
}
```

2. **Baxış Seçimlərinizin fərdiləşdirilməsi:** Siz baxış sahəsi, vaxt parametrləri və göstərmə seçimləri kimi müxtəlif baxış seçimlərini tənzimləyə bilərsiniz.

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

3. **Göy Cisimlərinin Yüklənməsi:** Siz simulyasiyanıza ulduzlar, planetlər, asteroidlər, kosmik gəmilər və s. kimi göy cisimlərini əlavə edə bilərsiniz. Hər bir obyekt öz xüsusiyyətləri ilə konfiqurasiya faylında müəyyən edilir.

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

4. **Kosmik gəmilərin müəyyən edilməsi:** Siz öz uydurma kosmik gəminizi yarada və ya mövqe, oriyentasiya və 3D modellər kimi parametrlərini göstərərək real olanlardan istifadə edə bilərsiniz.

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

5. **Skriptlərin yaradılması:** Siz dinamik hadisələr və animasiyalar yaratmaq üçün Celestia-nın xüsusi skript dilində skriptlər yaza bilərsiniz.

## CFG faylını necə açmaq olar?

CFG fayllarını açan və ya onlara istinad edən proqramlar

- Celestia (Pulsuz) (Windows, Mac, Linux) üçün

## Digər CFG faylları

**.cfg** fayl uzantısından istifadə edən digər fayl növləri bunlardır.

**Parametrlər**
- [CFG - Celestia Configuration File](/settings/cfg-celestia/)
- [CFG - Citrix Server Connection File](/settings/cfg-citrix/)
- [CFG - MAME Configuration File](/settings/cfg-mame/)
- [CFG - LightWave Configuration File](/settings/cfg-lightwave/)

**Oyun**
- [CFG - Wesnoth Markup Language File](/game/cfg-wesnoth/)
- [CFG - M.U.G.E.N Configuration File](/game/cfg-mugen/)
- [CFG - Source Engine Configuration File](/game/cfg-sourceengine/)

**Sistem və Müxtəlif**
- [CFG - CFG File](/system/cfg/)
- [CFG - Cal3D Model Configuration File](/misc/cfg-cal3d/)

## İstinadlar
* [Celestia](https://en.wikipedia.org/wiki/Celestia)


