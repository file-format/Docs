{
  "date": "2021-04-08",
  "keywords": [
"deb fails",
"deb faila formātā",
"kas ir deb fails",
"failu",
"deb piemērs",
"deb faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DEB — Bzip saspiestais darvas arhīvs",
  "description": "Uzziniet par DEB faila formātu un API, kas var izveidot un atvērt DEB failus.",
  "linktitle": "DEB",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-de-lvb"
}
},
  "lastmod": "2021-04-09"
}

## Kas ir DEB fails?

Fails ar paplašinājumu .deb ir Debian bināro pakotņu faila formāts, kas pieejams programmatūras pakotņu izplatīšanai operētājsistēmā Linux. Tas sastāv no diviem [TAR](/compression/tar/) arhīva failiem. DPKG nodrošina mehānismu DEB pakotņu lasīšanai un instalēšanai. DEB pakotnes var instalēt, izmantojot APT pakotņu programmatūras pārvaldības saskarni. DEB failiem interneta multivides veids ir application/vnd.debian.binary-package”.

## DEB faila formāts

DEB fails sastāv no diviem [TAR](/compression/tar/) arhīva failiem. Vienā arhīvā ir vadības informācija, bet citā - instalējamie dati.

### Pakešu organizācija

DEB fails ir **ar** arhīva fails, kura maģiskā vērtība ir `!<arch> `. Kopš Debian 0.93 DEB failu arhivēšanas mehānisms satur trīs failus noteiktā secībā.

 1. `Debian Binary` — tam ir paredzēta virkne rindu, kas atdalītas ar jaunām rindiņām. Pašlaik ir tikai viena rinda, kas apraksta versijas numuru. Pašreizējās versijas numurs ir 2.0.
 1. Vadības arhīvs — tajā ir iekļauts control.tar arhīvs, kurā ir uzturētāja skripti un metainformācija par pakotni, piemēram, pakotnes nosaukums, versija, atkarības un uzturētājs.
 1. Datu arhīvs — tas ir darvas arhīvs ar nosaukumu data.tar, un tajā ir faktiskie instalējamie multivides faili. Arhīvu var saspiest ar gz, bz2, lzma vai xz, un attiecīgi mainās datu arhīva faila paplašinājums.

### Vadības arhīvs

Vadības arhīvā var būt šāds saturs.

 * `control` - It contains a brief description of the package as well as other information such as its dependencies.
 * md5sums — tajā ir visu pakotnē esošo failu MD5 kontrolsummas, lai noteiktu bojātus vai nepilnīgus failus.
 * conffiles — tajā ir norādīti pakotnes faili, kas jāuzskata par konfigurācijas failiem. Atjaunināšanas laikā konfigurācijas faili netiek pārrakstīti, ja vien tas nav norādīts.
 * `preinst`, postinst, prerm un postrm — izvēles skripti, kas tiek izpildīti pirms vai pēc pakotnes instalēšanas vai noņemšanas
 * config ir izvēles skripts, kas atbalsta debconf konfigurācijas mehānismu.
 * shlibs — tas ir koplietotās bibliotēkas atkarību saraksts.

## Atsauces

* [DEB — Wikipedia](https://en.wikipedia.org/wiki/Deb_(file_format))

* [Debian binārās pakotnes formāts](https://manpages.debian.org/buster/dpkg-dev/deb.5.en.html)


