{
  "date": "2023-09-27",
  "keywords": [
"cfg",
"cfg faylı",
"cfg wesnot işarələmə dili faylı",
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
  "title": "CFG Fayl Format - Wesnoth Markup Language File",
  "description": "CFG Wesnoth İşarələmə Dili Fayl formatı və CFG faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "CFG Wesnoth",
  "menu": {
    "docs": {
      "identifier": "game-cfg-wesnoth-az",
      "parent": "game"
}
},
  "lastmod": "2023-09-27"
}

## CFG faylı nədir?

CFG faylı **Wesnoth Markup Language (WML)** kimi də tanınır. Bu, əsasən növbəyə əsaslanan strategiya oyunu olan Battle for Wesnoth oyununda istifadə edilən xüsusi işarələmə dilidir. WML oyunun müxtəlif aspektlərini, o cümlədən ssenarilər, kampaniyalar, vahidlər və s. müəyyən etmək və fərdiləşdirmək üçün istifadə olunur. Bu modderlər və tərtibatçılar üçün oyun üçün məzmun yaratmaq üçün bir yoldur.

XML və sadə skriptin birləşməsinə bənzəyən bir formatda yazılmışdır. WML faylında tapa biləcəyiniz bəzi ümumi elementlərin və strukturların icmalı budur:

1.  **Teqlər:** WML oyunda müxtəlif elementləri müəyyən etmək üçün teqlərdən istifadə edir. Teqlər bucaqlı mötərizələrə daxil edilmişdir. Misal üçün:

```
[unit]
    type=Elvish Archer
    hitpoints=25
[/unit]
```
    
2.  **Atributlar:** Teqlər daxilində elementlə əlaqəli xassələri və ya dəyərləri təyin etmək üçün atributları təyin edə bilərsiniz. Yuxarıdakı nümunədə növ və hitpoints atributlardır.
    
3.  **Massivlər və Massivlər:** Siz vahidlərin, ərazi növlərinin və ya digər oyun elementlərinin siyahılarını müəyyən etmək üçün verilənlər massivləri və hətta massivlər yarada bilərsiniz.
    
4.  **Şərti Hesabatlar:** WML oyunun gedişatına nəzarət etmək üçün şərti ifadələri dəstəkləyir. Misal üçün:

```
[if]
    condition=have_unit
    variable=x,y
[/if]
```
    
5.  ** Döngələr:** Siz elementlərin siyahılarını təkrarlamaq və ya təkrar hərəkətlər etmək üçün döngələrdən istifadə edə bilərsiniz.
    
6.  **Daxildir:** Siz məzmununuzu təşkil etmək və modullaşdırmaq üçün digər WML fayllarını əsas WML faylına daxil edə bilərsiniz.
    
7.  **Hadisə İşləyiciləri:** Siz oyunda xüsusi hadisələr baş verdikdə hərəkətləri işə salmaq üçün hadisə idarəçilərini təyin edə bilərsiniz.
    

Fərdi vahidi təyin edən WML faylının sadələşdirilmiş nümunəsi:

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

## Wesnoth üçün döyüş

The Battle for Wesnoth populyar və açıq mənbəli növbəyə əsaslanan strategiya oyunudur. Mac, Windows, Linux və daha çox daxil olmaqla bir çox platformalar üçün mövcuddur. Xüsusi könüllülər icması tərəfindən hazırlanmış bu oyun dərin və cəlbedici oyunu, eləcə də zəngin fantaziya dünyası ilə tanınır.

The Battle for Wesnothun əsas xüsusiyyətləri bunlardır:

1.  **Fantaziya Parametri:** Oyun insanlar, elflər, cırtdanlar, orklar və s. daxil olmaqla müxtəlif irqlərin olduğu fantaziya dünyasında qurulub. Oyunun irfan və hekayətləri onun cəlbediciliyinin ayrılmaz hissəsidir.
    
2.  **Növbəyə əsaslanan Strategiya:** Oyun növbə əsaslıdır, burada oyunçular altıbucaqlı şəbəkələrdə hərəkətlərini planlaşdırmaq və yerinə yetirmək üçün vaxt ayırırlar. O, taktiki döyüşü strateji qərarların qəbulu ilə birləşdirir.
    
3.  **Kampaniyalar:** Oyun hər birinin öz hekayə xətti, personajları və çətinlikləri olan geniş tək oyunçu kampaniyaları təklif edir. Oyunçular müxtəlif hekayələri və ssenariləri araşdıra bilərlər.
    
4.  **Multiplayer:** Wesnoth oyunçulara strateji döyüşlərdə bir-biri ilə rəqabət aparmağa imkan verən onlayn multiplayer oyunu dəstəkləyir. Çox oyunçu rejimlərinə kooperativ oyun və rəqabətli matçlar daxildir.

## CFG faylını necə açmaq olar?

The Battle for Wesnoth oyununda istifadə olunan Wesnoth Markup Language (WML) ilə ümumi şəkildə əlaqəli olan CFG faylları istənilən standart mətn redaktoru ilə asanlıqla redaktə edilə bilər. Bu fayllarda ssenarilər, vahidlər və kampaniyalar da daxil olmaqla oyunun müxtəlif aspektlərini müəyyən edən WML-də yazılmış insan tərəfindən oxuna bilən kod var.

CFG fayllarını dəyişdirmək üçün istənilən mətn redaktorundan istifadə edə bilsəniz də, Emacs və Vi kimi bəzi qabaqcıl mətn redaktorlarında WML sintaksisini vurğulayan plaginlər mövcuddur. Bu plaginlər istifadəçilərin WML kodu daxilində müxtəlif elementləri və strukturları ayırd etmələrini asanlaşdırmaq üçün faydalı rəng kodlaşdırması və formatlaşdırma təmin edir.

CFG fayllarını açan və ya istinad edən proqramlar daxildir

- The Battle for Wesnoth (Pulsuz) (Windows, MAC, Linux)
- Microsoft Notepad

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
* [The Battle for Wesnoth](https://en.wikipedia.org/wiki/The_Battle_for_Wesnoth)
