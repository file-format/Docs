{
  "date": "2021-04-08",
  "keywords": [
"dar failą",
"dar failo formatas",
"kas yra dar failas",
"failą",
"dar pavyzdys",
"dar failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DAR – disko archyvavimo failo formatas",
  "description": "Sužinokite apie DAR failo formatą ir API, kurios gali kurti ir atidaryti DAR failus.",
  "linktitle": "DAR",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-da-ltr"
}
},
  "lastmod": "2021-04-09"
}

## Kas yra DAR failas?

Failas su plėtiniu .dar yra suspaustas archyvas, sukurtas naudojant DAR disko archyvą. Jis gali sukurti viso disko ar failų grupės atsarginę kopiją / archyvą. Jis buvo sukurtas siekiant pakeisti [TAR](/compression/tar/) failo formatą UNIX OS ir gali būti sukurtas kaip padalintas archyvo failas dideliam skaičiui failų. DAR archyvas palaiko galimybę ištrinti failus iš sistemos, kurie yra susieti su pagrindiniais archyvo failais. Dėl savo galimybių kurti diferencinę, laipsnišką ir mažėjančią atsarginę kopiją jis pranašesnis už TAR failus.

## DAR failo formatas

DAR failai yra suglaudinti archyvai, kuriuose galima naudoti bet kokį failo glaudinimą, pvz., [gzip](/compression/gz/), [bzip2](/compression/bz2/), lzo, xz arba lzma. Tikslus DAR failo failo formatas priklauso nuo to, kokio tipo formatavimas naudojamas archyvo turiniui suspausti. Tai taip pat leidžia pasirinktinai Blowfish, Twofish, AES, Serpent, Camellia šifravimą ir viešojo rakto šifravimą bei parašą (OpenPGP).

### DAR funkcijos

Kai kurios DAR failo formato funkcijos yra tokios.

 * Rūpinasi bet kokio tipo inode (katalogas, paprasti failai, simboliai, specialūs įrenginiai, pavadinti vamzdžiai, lizdai, durys, ...)
 * Rūpinasi sunkiai susietais inodes (kietosios nuorodos paprastais failais, char įrenginiais, blokavimo įrenginiais, sunkiai susietomis simbolinėmis nuorodomis)
 * Rūpinasi retais failais
 * Rūpinasi Linux failo išplėstiniais atributais,
 * Rūpinasi Linux failo ACL
 * Rūpinasi Mac OS X failų šakutėmis
 * Rūpinasi kai kuriais failų sistemai būdingais atributais, pvz., HFS+ failų sistemos gimimo data ir nekintamais, duomenų žurnalų, saugaus ištrynimo, nesujungimo be uodegos, neištrinamais, noatime ext2/3/4 failų sistemos atributais.
 * Suspaudimas kiekviename faile naudojant gzip, bzip2, lzo, xz arba lzma (priešingai nei viso archyvo glaudinimas). Asmuo gali pasirinkti neglaudinti jau suglaudintų failų pagal savo failo pavadinimo priesagą.
 * Greitas failų ištraukimas iš bet kurios archyvo vietos
 * Greitas archyvo turinio sąrašas išsaugant failų katalogą archyve
 * Tiesioginė failų sistemos atsarginė kopija: aptinka, kada failas buvo pakeistas, kol buvo nuskaitytas atsarginės kopijos kūrimas, ir gali dar kartą bandyti jį išsaugoti iki nurodyto maksimalaus pakartotinių bandymų skaičiaus
 * Maišos failas (MD5, SHA1 arba SHA-512), sukurtas kiekvienam pjūviui, gautas failas yra suderinamas su md5sum arba sha1sum, kad būtų galima greitai patikrinti kiekvienos dalies vientisumą.
 * Nepriklausoma nuo failų sistemos: ji gali būti naudojama norint atkurti sistemą į kitokio dydžio skaidinį ir (arba) skaidinį su kita failų sistema[5]

## Nuorodos

* [DAR](http://dar.linux.free.fr/)

* [DAR Disk Archiver](https://en.wikipedia.org/wiki/Dar_(disk_archiver))


