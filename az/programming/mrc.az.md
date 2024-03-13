{
  "date": "2021-09-14",
  "keywords": [
"mrc",
"fayl",
"uzadılması",
"fayl formatı",
"mrc tətbiqi",
"Proqramlaşdırma bələdçisi",
"mrc nümunəsi",
"mIRC",
"mIRC skript dili",
"INI faylları",
"mSL skript dili",
"mIRC dili",
"mIRC skriptləri",
"skript dili"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "MRC - mIRC Skript Dil Faylı",
  "description": "MRC faylları yarada və aça bilən MRC fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "MRC",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-mr-azc"
}
},
  "lastmod": "2021-09-14"
}

## MRC faylı nədir?

mIRC Windows əməliyyat sistemində IRC müştərisi (Internet Relay Chat) kimi daxil edilmiş skript dilidir. O, şəxsi və kanal istifadəsi üçün spam göndərməkdən qorunma vasitəsi təmin edir. İstifadəçi uyğunluğunun daha yaxşı təcrübəsini təmin etmək üçün bu mIRC skript dili dialoq pəncərələrinin yaradılmasına imkan verir. Əsasən düz mətn formatında skriptləri ehtiva edən fayllar MRC genişlənməsi ilə və ya [INI](/system/ini/) faylları kimi saxlanılır. Bu dilin funksiyaları əmrlər və identifikatorlar kimi tanınır (qiyməti qaytardıqda).

mIRC dili birdən çox skript faylının yüklənməsini təmin edir. Digər tərəfdən, bir fayl eyni vaxtda yükləndikdə digərinin artıq istifadə edilməməsinə səbəb ola bilər. Əmrlər saxlanılır və onlar avtomatik olaraq IRC-də mövcud ola bilər. Bu dildə istifadə olunan əmrlər və ləqəblər hər hansı simvolun üstünlüyünü təşkil etmir.

mIRC botların kanalı avtomatik idarə etməsi üçün geniş istifadə olunur, lakin o, mSL skript dili ilə də dəyişdirilə bilər. O, makrolar, musiqi ifa etmə qabiliyyəti, kiçik makrolar və funksiyalar, əsas oyunlar və ya kiçik proqramları idarə etmək kimi bir çox yeni funksiyaları təqdim edə bilər.


## Qısa tarix ##

Bu skript dili ilk dəfə 1995-ci ildə Xalid Adam Bəy tərəfindən hazırlanmışdır. Ssenari dilinin dizaynı da Xalid tərəfindən yaradılmışdır. Bu dilin hədəfi hadisəyə əsaslanan proqramlaşdırma idi. Əvvəlcə bu proqramlaşdırma dilinin faylları üçün istifadə olunan fayl uzantısı .mrc və .ini idi. Üstəlik, o, xüsusi proqram təminatının lisenziyası əsasında hazırlanmışdır.

## Texniki Spesifikasiya ##

Bəzi funksiyalar bu mIRC dili vasitəsilə xüsusi skript edilir və ləqəblər kimi tanınır. Bu ləqəblər dəyərləri qaytardıqda, onlar xüsusi identifikatorlar kimi tanınırlar. Bu mIRC dilində olan bütün dəyişənlər dinamik şəkildə yazılmışdır. Sigillər mIRC skriptləri tərəfindən istifadə olunur. Bu skript dilinin başqa bir xüsusiyyəti pop-uplardır. İstifadəçilər sadəcə onları seçməklə pop-uplara zəng edə bilərlər. Pult müəyyən hadisələr üçün təyin edilir. Nisbi hadisə baş verdikdə uzaqdan idarəetmələr çağırılır.

Bu dilin kodunun hər sətirini qırmaq üçün boşluqla ayrılmış tokenlərdən istifadə olunur. MDX (mIRC Dialoq Genişləndirilməsi) və DCX (Dialoq Nəzarət Genişləndirilməsi) kimi mIRC faylları üçün istifadə edilən bəzi digər məşhur genişləndirmələr də var. Bunların hər ikisi dialoq uzantılarıdır və nisbətən daha populyardır. Dil konstruksiyaları bu skript dilinin nomenklaturası ilə istinad edilir. mIRC dili yerli və qlobal dəyişənlər, ikili dəyişənlər, hash cədvəlləri və faylların idarə edilməsi kimi skript dilinin müxtəlif aspektlərini əhatə edir.


## MRC Fayl Format Nümunəsi ##

```

;Defines the alias 'hello' in the remote script

;Note: if this is placed in an alias script,
;the 'alias' part must be removed (result: hello {)
;Usage: /hello

alias hello {

  ;Displays(/echo) 'Hello World!' into the active window(-a)
  echo -a Hello World!

}

```

```
;Placed in a remote script

;When a user types Hello! in a channel,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:#:{ msg $chan Hello, $nick $+ ! }

;When a user types Hello! in a private message,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:?: { msg $nick Hello, $nick $+ ! }

;Here is a script which automatically gives voice to a user
;who joins a particular channel (The Bot or user should have HOP)

on *:JOIN:#?: { mode $chan +v $nick }

;A bad word script

on *:Text:die*:#: { .mode $chan +b $nick | kick $chan $nick Dont say that again }

```

## İstinad ##

* [MIRC - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/MIRC_scripting_language)




