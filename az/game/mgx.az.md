{
  "date": "2021-09-08",
  "keywords": [
"mgx faylı",
"mgx fayl formatı",
"mgx faylı nədir",
"fayl",
"mgx nümunəsi",
"mgx fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Age of Empires 2 Expansion Replay MGX fayl formatı və MGX faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "MGX - Age of Empires 2 genişləndirilməsi təkrarı",
  "linktitle": "MGX",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-mg-azx"
}
},
  "lastmod": "2021-09-08"
}

## MGX faylı nədir?

.mgx uzantısı olan fayl Age of Empires II: The Conquerors oyunu üçün qeydə alınmış fayldır və Age of Empires II proqramı çərçivəsində təkrar oynana bilər. İstifadəçinin oynadığı kampaniyanın tam qeydini ehtiva edir. O, Age of Empires II proqramında yüklənə və səsləndirilə bilər. Yenidən oynanıldıqdan sonra oyun istifadəçinin kampaniya üçün planlaşdırdığı və oynadığı bütün hadisələri və ssenariləri göstərir.

## MGX Fayl Format - Ətraflı Məlumat

The internal file format of the MGX file have been worked out and available as partially validated information on [Age of Empires 2: The Conquerors — Savegame File Format Specification](https://github.com/stefan-kolb/aoc-mgx-format). The specifications outline the details in the following sections.

### Struktur Tərifləri

GPX fayl formatının struktur təriflərinin strukturlaşdırılmış ikili verilənləri oxumaq və yazmaq üçün bir yol təmin edən [BinData Ruby Gem declarations](https://github.com/dmendel/bindata/wiki)-ə əsaslandığı güman edilir. Bu, proqramçıya BinData tərəfindən oxunan və yazılan ikili məlumatların formatını təyin etməyə imkan verir.

### MGX Mesajlaşma

MGX mesajlaşması iki növ mesaja əsaslanır.

 * GAMESTART - oyunun başlama əmrlərini təyin edir və bu günə qədər təsdiqlənməyib
 * CHAT - oyundaxili söhbət mesajlarını təsvir edir. Həm oyunçular, həm də oyunun özü (Gaia) oyundaxili mesajlar yaya bilər.

### OYUN AKSİYASI

Əldə edilmiş və təfərrüatları əlçatan olan bir neçə [GAMEPLAY Actions](https://github.com/stefan-kolb/aoc-mgx-format/blob/master/README.md#actions) var.

## İstinadlar

* [Age of Empires 2: The Conquerors — Savegame File Format Specification](https://github.com/stefan-kolb/aoc-mgx-format)


