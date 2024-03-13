{
  "date": "2023-09-27",
  "keywords": [
"cfg",
"cfg faylı",
"cfg mugen konfiqurasiya faylı",
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
  "title": "CFG Fayl Format - MUGEN Konfiqurasiya Faylı",
  "description": "CFG MUGEN Konfiqurasiya Faylı formatı və CFG fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "CFG M.U.G.E.N",
  "menu": {
    "docs": {
      "identifier": "game-cfg-mugen-az",
      "parent": "game"
}
},
  "lastmod": "2023-09-27"
}

## CFG faylı nədir?

MUGEN kontekstindəki CFG faylı MUGEN Konfiqurasiya Faylına istinad edir. **MUGEN**, Elecbyte tərəfindən hazırlanmış fərdiləşdirilə bilən 2D döyüş oyunu mühərrikidir. İstifadəçilər CFG faylları da daxil olmaqla müxtəlif konfiqurasiya fayllarını redaktə etməklə öz simvollarını, mərhələlərini yarada və hətta oyunun davranışını və qaydalarını dəyişə bilərlər.

MUGEN `.cfg` faylında tapa biləcəyiniz əsas icmal budur:

1.  **Sistem Konfiqurasiyası**: CFG faylları çox vaxt oyun mühərrikinin ümumi davranışı ilə bağlı parametrləri ehtiva edir. Buraya ekran həlli, səs parametrləri və daxiletmə konfiqurasiyası (klaviatura, joystik və ya nəzarətçi xəritələri) kimi şeylər daxildir.
    
2.  **Xarakter və Mərhələ Defoltları**: Siz simvollar və mərhələlər üçün standart parametrləri təyin edə bilərsiniz. Məsələn, oyun başlayanda hansı simvolların və mərhələlərin yükləndiyini təyin edə bilərsiniz.
    
3.  **Oyun Seçimləri**: MUGEN `.cfg` faylları həmçinin dövrə vaxtı məhdudiyyətləri, zərərin miqyası və s. kimi müxtəlif oyun seçimlərinə nəzarət edə bilər.
    
4.  **Sazlama və İnkişaf**: Qabaqcıl istifadəçilər sazlama və inkişaf məqsədləri üçün `.cfg` fayllarından istifadə edə bilər. Bu parametrlər sazlama məlumatının ekranda necə göstərilməsinə nəzarət edə və ya inkişafla bağlı digər davranışları müəyyən edə bilər.
    
5.  **Screenpack Konfiqurasiyası**: Ekran paketləri oyunun görünüşünü və hissini dəyişən vizual mövzulardır. `.cfg` faylları hansı ekran paketinin istifadə olunduğunu təyin edə və onun müxtəlif elementlərini konfiqurasiya edə bilər.
    
6.  **AI Davranışı**: MUGEN sizə kompüter tərəfindən idarə olunan personajların (AI) döyüşlərdə necə davranacağını müəyyən etməyə imkan verir. `.cfg` fayllarında AI çətinliyi və davranışı ilə bağlı parametrlər ola bilər.

## MUGEN Konfiqurasiya Faylı 

MUGEN CFG (Konfiqurasiya) faylı xüsusi döyüş oyunları dünyasında yaradıcılar üçün mühüm komponentdir. Bu, onlara öz oyunlarının əsas qaydalarını formalaşdırmaq imkanı verir. Buraya hər raundun nə qədər davam edəcəyi, kompüter tərəfindən idarə olunan rəqiblər tərəfindən təqdim olunan problem səviyyəsi, oyunun tempi, kombinasiyaların zərərə təsir dərəcəsi və s. kimi amillər daxildir.

Bundan əlavə, CFG faylı yaradıcılara ekran həlli kimi oyunun ekran parametrlərini təyin etməyə və MUGEN-in oyun zamanı səs effektləri və musiqi ifa edib etməməsinə qərar verməyə imkan verir. MUGEN-in incəliklərini yaxşı bilənlər üçün bu fayl unikal oyun təcrübəsi yaratmaq üçün oyunla əlaqəli bir sıra digər parametrləri düzəltmək potensialını təklif edir.

Defolt olaraq MUGEN-in `mugen.cfg` kimi tanınan əsas CFG faylı proqramın məlumat qovluğunda yerləşir. Bu fayl daxilində oyunun parametrlərini birbaşa redaktə etmək mümkün olsa da, əvvəlcə ehtiyat nüsxəsini yaratmaq məsləhətdir. Bu ehtiyat tədbiri, lazım gələrsə, istənilən gözlənilməz dəyişikliklərin oyun təcrübənizi pozmasının qarşısını alaraq, MUGEN-i asanlıqla orijinal parametrlərinə qaytara biləcəyinizi təmin edir.

## MUGEN - Oyun Mühərriki

MUGEN, Elecbyte tərəfindən hazırlanmış çox yönlü və yüksək səviyyədə fərdiləşdirilə bilən 2D döyüş oyunu mühərrikidir. MUGEN adı Mugen Ultimate Game Engine deməkdir. O, ilkin olaraq 1999-cu ildə buraxıldı və o vaxtdan öz 2D döyüş oyunlarını dizayn etmək və inkişaf etdirmək üçün mühərrikdən istifadə edən istifadəçilər və yaradıcıların xüsusi icmasını qazandı.

MUGEN-in bəzi əsas xüsusiyyətləri və aspektləri bunlardır:

1.  **Özəlləşdirilə bilən personajlar:** MUGEN istifadəçilərə öz personajlarını (döyüşçülər və ya sprite kimi tanınan) yaratmağa və oyuna idxal etməyə imkan verir. Yaradıcılar bu personajlar üçün unikal hərəkət dəstləri, animasiyalar və xüsusi hücumlar tərtib edə bilər ki, bu da müxtəlif françayzinqlərdən və ya orijinal əsərlərdən faktiki olaraq istənilən personajı daxil etməyə imkan verir.
    
2.  **Mərhələlər:** Simvollara əlavə olaraq, istifadəçilər döyüşlərin baş verdiyi mərhələləri də yarada və fərdiləşdirə bilərlər. Bu mərhələlər interaktiv elementlərə və unikal fonlara malik ola bilər.
      
3.  **Screenpacks:** Screenpacks are visual themes that change overall appearance of game, including menus, character selection screens and life bars. Users can create and share their own screenpacks to give their games unique look and feel.
    
4.  **Səs və Musiqi:** Yaradıcılar öz oyunlarına səs effektləri və fon musiqisi əlavə edərək ümumi oyun təcrübəsini artıra bilərlər.
    
5.  **Scripting:** Qabaqcıl istifadəçilər mürəkkəb xarakter davranışları, unikal oyun mexanikası və xüsusi effektlər yaratmaq üçün daxili skript dilindən istifadə edə bilərlər.

## CFG faylını necə açmaq olar?

MUGEN CFG faylları onları müxtəlif mətn redaktorları ilə əlçatan edən düz mətn sənədləridir. Windows-da siz Microsoft Notepad və ya WordPad-dən istifadə edə bilərsiniz, macOS istifadəçiləri isə bu məqsədlə Apple TextEdit istifadə edə bilərlər. Bu redaktorlar istifadəçilərə asanlıqla CFG faylları daxilində konfiqurasiya parametrlərinə baxmaq və dəyişdirmək imkanı verir.

CFG fayllarını açan və ya onlara istinad edən proqramlar

- Elecbyte MUGEN
- Notepad
- TextEdit

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
* [Mugen (oyun mühərriki)](https://en.wikipedia.org/wiki/Mugen_(oyun_mühərriki))


