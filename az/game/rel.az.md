{
  "date": "2021-09-08",
  "keywords": [
"rel faylı",
"rel fayl formatı",
"rel faylı nədir",
"fayl",
"rel misal",
"rel fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "REL faylları yarada və aça bilən REL fayl formatı və API-lər haqqında məlumat əldə edin.",
  "title": "REL - Köçürülə bilən Modul Faylı",
  "linktitle": "REL",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-re-azl"
}
},
  "lastmod": "2021-09-08"
}

## REL faylı nədir?
.rel uzantılı fayl bir neçə növ məqsəd üçün istifadə edilə bilər. Buna görə də, oyun təsnifatı baxımından o, Brawl, Super Smash Bros və Mario Kart Wii kimi bəzi Nintendo Wii oyunları tərəfindən istifadə edilən dəyişdirilə bilən modul faylı kimi tanınır. O, xarakter modelləri və mərhələləri daxil olmaqla oyun məlumatlarını ehtiva edir. REL faylları Microsoft Windows tərəfindən istifadə edilən .DLL faylları ilə eyni şəkildə işləyir.

## REL fayl formatı
REL fayl formatında fayl bir neçə bölməyə bölünür, giriş kimi qruplaşdırılır, məsələn, bir bölmədə yalnız oxunan məlumatlar, bütün icra edilə bilən kodlar digərində yerləşdirilir və s. Fayl başlıq bölməsi ilə başlayır, ardınca:
- Bölmə məlumatını ehtiva edən cədvəl.
- Bölmə məlumatları.
- Köçürmə məlumatları.

### Fayl başlığı
Fayl 0x4C bayta qədər başlıq ilə başlayır:
| Ofset | Ölçü | Sahənin adı | Təsvir |
--------------------|---------------|-------------------|---------------------------------|
| 0x00 | 4 | id | Arbitrary identification number. Must be unique amongst all RELs used by a game. Must not be 0. |
| 0x04 | 4 | növbəti | İş vaxtında doldurulmuş növbəti modula göstərici. |
| 0x08 | 4 | əvvəlki | İş vaxtında doldurulmuş əvvəlki modulun göstəricisi. |
| 0x0c | 4 | numSections | Fayldakı bölmələrin sayı. |
| 0x10 | 4 | bölməInfoOffset | Bölmə cədvəlinin başlanğıcına ofset. |
| 0x14 | 4 | nameOffset | Modulun adını ehtiva edən ASCII sətrinə ofset. NULL ola bilər. REL faylının başlanğıcına nisbətən. |
| 0x18 | 4 | adBoyut | Modul adının baytla ölçüsü. |
| 0x1c | 4 | versiya | REL fayl formatının versiya nömrəsi. |
| 0x20 | 4 | bssSize | '.bss' bölməsinin ölçüsü. |
| 0x24 | 4 | relOffset | Köçürmə cədvəlinə uyğun olaraq. |
| 0x28 | 4 | impOffset | İmplant cədvəlinə ofset. |
| 0x2c | 4 | impSize | İm cədvəlinin baytla ölçüsü. |
| 0x30 | 1 | prologSection | Index into section table which prolog is relative to. Skip if this field is 0. |
| 0x31 | 1 | epilogSection | Index into section table which epilog is relative to. Skip if this field is 0. |
| 0x32 | 1 | unresolvedSection | Index into section table which unresolved is relative to. Skip if this field is 0. |
| 0x33 | 1 | bssSection | BSS-in nisbi olduğu bölmə cədvəlinə indeksləşdirin. İş vaxtında dolduruldu! |
| 0x34 | 4 | prolog | _prolog funksiyasının müəyyən hissəsinə ofset. |
| 0x38 | 4 | epiloq | _epilog funksiyasının müəyyən hissəsinə ofset. |
| 0x3c | 4 | həll olunmamış | _həll edilməmiş funksiyanın müəyyən hissəsinə ofset. |
| 0x40 | 4 | align | Version ≥ 2 only. Alignment constraint on all sections, expressed as power of 2. |
| 0x44 | 4 | bssAlign | Version ≥ 2 only. Alignment constraint on all '.bss' section, expressed as power of 2. |
| 0x48 | 4 | fixSize | Yalnız versiya ≥ 3. REL OSLinkFixed ilə əlaqələndirilirsə (OSLink əvəzinə), bu ünvandan sonrakı boşluq digər məqsədlər üçün istifadə edilə bilər (məsələn, BSS). |

### Bölmə Məlumat Cədvəli
Bölmə məlumat cədvəlində hər 0x8 bayt uzunluğunda **numSections** daxilolmaları var:
| Ofset | Ölçü | Təsvir |
-------|------------|-------------|
| 0x0 | 30 bit | REL-in əvvəlindən bölməyə qədər ofset. Bu sıfırdırsa, bölmə açılmamış bölmədir (yəni .bss). |
| 0x3.6 | 1 bit | Naməlum. |
| 0x3.7 | 1 bit | İcra olunan bayraq; bu 1 olarsa bölmə icra edilə biləndir. |
| 0x4 | 4 | Bölmənin bayt uzunluğu. Bu sıfırdırsa, bu giriş atlanır. |
| 0x8 | Növbəti giriş | Növbəti giriş |

### Köçürmə Məlumatı
Köçürülmə məlumatları 0x8 baytlıq strukturların bir və ya bir neçə siyahısıdır. Hər bir siyahının sonu xüsusi tipli 203 kodu ilə qeyd olunur:
| Ofset | Adı | Ölçü | Təsvir |
-------|------------|------------|-----|
| 0x0 | ofset | 2 | Əvvəlki yerdəyişmədən bu yerə baytlarla ofset. Bu bölmədə ilk yerdəyişmədirsə, bu bölmənin başlanğıcına nisbətəndir. |
| 0x2 | növü | 1 | Köçürmə növü. Aşağıda təsvir edilmişdir. |
| 0x3 | bölmə | 1 | Simvolun yerini dəyişdirmək üçün bölməsi. Xüsusi yerdəyişmə növü üçün 202, əvəzinə bu faylda aşağıdakı köçürmə qeydlərinin tətbiq olunduğu bölmənin nömrəsidir. |
| 0x4 | əlavə et | 4 | Bölmənin başlanğıcına nisbətən yerini dəyişdirmək üçün simvolun baytları ilə ofset. Bu, main.dol-a qarşı yerdəyişmələr üçün mütləq ünvandır. |
| 0x8 | Növbəti giriş | Növbəti giriş | Növbəti giriş |


 



## İstinadlar 

* [Köçürülə bilən Obyekt Modulu Format](https://en.wikipedia.org/wiki/Relocatable_Object_Module_Format)



