{
  "date": "2019-10-11",
  "keywords": [
"mng failą",
"mng failo formatas",
"kas yra mng failas",
"failą",
"mng pavyzdys",
"mng failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MNG failo formatas – kelių vaizdų tinklo grafikos failo formatas",
  "description": "Sužinokite apie MNG failo formatą ir API, kurios gali kurti ir atidaryti MNG failus.",
  "linktitle": "MNG",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-mn-ltg"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra MNG failas?

Failas su plėtiniu .mng yra kelių vaizdų tinklo grafikos failo formatas, panašus į [PNG](/image/png/) vaizdo formatą, bet palaiko animuotus vaizdus. Jis buvo sukurtas siekiant išvengti PNG formato perkrovimo naudojant papildomą animacijos funkciją. MNG taip pat panašus į [GIF](/image/gif/) failus, bet naudojamas daugiau glaudinimo ir palaiko visą alfa funkciją. Neoficialus MNG failų MIME laikmenos tipas yra video/x-mng. MNG failus galima atidaryti tokiose programose kaip ImageMagik ir IrfanView.

## MNG failo formatas

MNG failo formatas yra panašus į PNG formatą ir naudoja tą pačią gabalo struktūrą, kaip apibrėžta PNG specifikacijose. MNG dekoderis turi sugebėti iššifruoti PNG duomenų srautus nenurodydamas jokių specialių dekodavimo instrukcijų vėliavėlių. MNG sugrupuoja kelis vaizdus į kadrą, o kai kurie vaizdai naudojami kaip sprite, norint perkelti iš vienos vietos į kitą. Mechanizmas leidžia pakartotinai naudoti vaizdo duomenis jų nepersiunčiant. Kūrėjo nuoroda gali būti nurodyta [MNG specifications](http://www.libpng.org/pub/mng/spec/).

### MNG parašas

MNG duomenų srautas prasideda 8 baitų parašu, kuriame yra:

```
138  77  78  71  13  10  26  10  - (decimal)
8a  4d  4e  47  0d  0a  1a  0a   - (hexadecimal)
\212   M   N   G  \r  \n \032 \n - (ASCII C notation)
```

Tai panašu į PNG parašą, tačiau vietoj PNG yra MNG.

### MNG rėmas

MNG rėmelį sudaro dvimatis mažesnių vaizdų vaizdas. Kiekvieną mažą vaizdą galima pasiekti naudojant eilutės ir stulpelio indekso derinį. Formatas gali saugoti trimačius vokselių duomenis, išdėstytus dvimačių plokštumų serijoje. Kiekviena plokštuma vaizduojama PNG arba Delta-PNG duomenų srautu. Kiekvienas Delta-PNG duomenų srautas apibrėžia vaizdą kaip skirtumus nuo pirminio PNG vaizdo. Tai suteikia daug kompaktiškesnį vėlesnių vaizdų vaizdavimo būdą, nei naudojant visą PNG duomenų srautą kiekvienam.

## Nuorodos Nr.

* [MNG](http://www.libpng.org/pub/mng/)

* [MNG formatas v 1.0](http://www.libpng.org/pub/mng/spec/)


