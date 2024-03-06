{
  "date": "2019-10-11",
  "keywords": [
"xpm failu",
"xpm faila formātā",
"kas ir xpm fails",
"failu",
"xpm piemērs",
"xpm faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XPM — X PixMap faila formāts",
  "description": "Uzziniet par XPM failu formātu un API, kas var izveidot un atvērt XPM failus.",
  "linktitle": "XPM",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-xp-lvm"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir XPM fails?

Fails ar paplašinājumu .xpm ir attēla faila formāts, ko izmantoja X Windows sistēma. Tas atbalsta caurspīdīgus pikseļus un parasti ir paredzēts ikonu pikseļu karšu izveidei. Tā atbalsta vienkrāsainus, gra-scale un krāsu pixmap datus. Tie tika izstrādāti tā, lai tos varētu rediģēt ar roku, un tos var iekļaut [C](/programming/c/) kodā. Šim nolūkam XPM faili ir vienkārša teksta faila formātā un ievēro C programmēšanas valodas sintakse. XPM failus var atvērt ar dažādām attēlu skatīšanas lietojumprogrammām, piemēram
CorelDRAW Graphics Suite 2020, Corel PaintShop Pro, IrfanView un Canvas X.

## XPM faila formāts

XPM faila formāts izmanto C sintaksi, lai tos integrētu C un C++ programmās. Tas sastāv no sekojošām sešām dažādām sadaļām.

 * \<Values>
 * \<Colors>
 * \<Pixels>
 * \<Extensions>

Sadaļas faktiski ir virkņu masīvs, kā norādīts tālāk.

```
/* XPM */
static char*<variable_name>[] = {
  <Values>
  <Colors>
  <Pixels>
  <Extensions>
};
```
Tālāk ir sniegta informācija par katru sadaļu.

`<Values> ` — šī sadaļa ir virkne, kurā ir četri vai seši veseli skaitļi, kas atrodas 10. bāzē un atbilst:

 * pixmap platums un augstums
 * Krāsu skaits
 * rakstzīmju skaits pikselī
 * izvēles tīklāja koordinātas un XPMEXT tags

`<Colors> ` - Šajā sadaļā ir tik daudz virkņu, cik krāsu. Katra virkne ir šāda:

```
<chars>{<key><color> }+
```
`<Pixels> ` — šī sadaļa sastāv no<height> stīgas un<width> \*<chars_per_pixel> rakstzīmes. Katrs<chars_per_pixel> garuma virknei jābūt vienai no iepriekš definētajām grupām<Colors> sadaļā.

`<Extension> ` - Paplašinājuma sadaļai jābūt marķētai, ja tā nav tukša<Values> sadaļā. Tas var sastāvēt no vairākiem<Extension> apakšsadaļas, kas var būt divu veidu:

 * viena atsevišķa virkne, kas sastāv šādi: XPMEXT<extension-name><extension-data>
 * vai bloks, ko veido vairākas virknes: XPMEXT<extension-name><related extension-data composed of several strings>

## Atsauces

* [XPM — Wikipedia](https://en.wikipedia.org/wiki/X_PixMap)

* [XPM rokasgrāmata](http://www.xfree86.org/current/xpm.pdf)


