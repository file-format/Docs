{
  "date" : "2023-01-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"OSU fayl formatı və OSU fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title" : "OSU Faylı - Osu! Skript Fayl Formatı",
  "linktitle" : "OSU",
  "menu" : {
    "docs" : {
      "identifier":"game-osu-az",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-18"
}

## OSU faylı nədir?

OSU faylı osu üçün yazılmış oyun skriptidir! ritm oyunu. O, çətinlik səviyyəsi, çalınacaq mahnı və oyunçunun musiqi ilə sinxronizasiya etməli olduğu hit obyektlərin vaxtları kimi oyunda istifadə olunan beatmap haqqında məlumatları ehtiva edir. Bu, ritm oyunu oyunçularına fərdi problemlər hazırlamağa və oyun ictimaiyyəti ilə paylaşmağa imkan verir.

**OSR Fayl Formatının MIME Növü:** x-osu-beatmap

## OSU fayl formatı

OSU faylları diskdə düz mətn faylları kimi saxlanılır və onun strukturu osu! tərəfindən [OSU file format](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29)-də çox aydın şəkildə müəyyən edilmişdir.

### OSU faylındakı bölmələr

Tipik bir OSU faylında aşağıdakı bölmələr var.

|Bölmə |Təsviri |Məzmun növü|
---|---|---|
|[Ümumi]| Beatmap haqqında ümumi məlumat| açar: dəyər cütləri|
|[Redaktor]| Beatmap redaktoru üçün saxlanmış parametrlər| açar: dəyər cütləri|
|[Metadata] |Beatmap-i müəyyən etmək üçün istifadə olunan məlumat| açar:dəyər cütləri|
|[Çətinlik] |Çətinlik parametrləri| açar:dəyər cütləri|
|[Hadisələr]| Beatmap və storyboard qrafik hadisələri| Vergüllə ayrılmış siyahılar|
|[Timing Points]| Vaxt və nəzarət nöqtələri| Vergüllə ayrılmış siyahılar|
|[Rənglər]| Kombo və dəri rəngləri| açar : dəyər cütləri|
|[HitObjects]| Vuruş obyektləri| Vergüllə ayrılmış siyahılar|

## İstinadlar

* [OSU! Ritm Oyunu](https://osu.ppy.sh/home)

* [OSU fayl formatı](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29)


