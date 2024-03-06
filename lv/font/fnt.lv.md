{
  "date": "2020-08-20",
  "keywords": [
"fnt failu",
"fnt faila formātā",
"kas ir fnt fails",
"failu",
"fnt piemērs",
"fnt faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "FNT — Windows fontu fails",
  "description": "Uzziniet par FNT faila formātu un API, kas var izveidot un atvērt FNT failus.",
  "linktitle": "FNT",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-fn-lvt"
}
},
  "lastmod": "2020-10-30"
}

## Kas ir FNT fails?

Fails ar paplašinājumu .fnt ir fonta fails, kurā tiek glabāta vispārīga fonta informācija operētājsistēmās Windows. FNT faili lielākoties ir aizstāti ar TrueType (.TTF) un OpenType (.OTF) failu formātiem, un šobrīd tas ir novecojis fontu faila formāts. Šajos failos var saglabāt vienu vērtētāja vai vektora fontu. Visi ierīču draiveri atbalsta Windows 2.x fontus. Tomēr ne visi ierīču draiveri
atbalsta Windows 3.0 versiju.

## FNT faila formāts

FNT faili spēj saglabāt vienu rastra vai vektora fontu. Vektoru formātus GDI izmanto biežāk, salīdzinot ar rastru, kur katras hartas glifs tiek definēts, izmantojot nelielu bitkarti. Acīmredzamais iemesls .fnt aizstāšanai ar .ttf un .otf ir tā rastra formāts.

### Fonta faila galvene
Gan rastra, gan vektora fontu failu sākums ir kopīgs, kam seko atšķirīga informācija katram faila veidam. Fonta faila galvenē operētājsistēmai Windows 3.0 ir iekļauti seši jauni lauki, kas ir iestatīti uz nulli, lai nodrošinātu saderību ar nākamajām Windows versijām.

 * d Karogi
 * dfAspace
 * dfBspace
 * dfCspace
 * dfColorPointer
 * dfReserved1

Lai iegūtu detalizētu informāciju par Windows 3.0 un 2.0 galvenēm, apmeklējiet vietni [Microsoft KnowledgeBase Archive](https://jeffpar.github.io/kbarchive/kb/065/Q65123/).

## Atsauces
 * [Fonta faila formāts](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)
 * [Kā instalēt vai noņemt fontu sistēmā Windows](https://support.microsoft.com/en-us/windows/how-to-install-or-remove-a-font-in-windows-f12d0657-2fc8- 7613-c76f-88d043b334b8)

