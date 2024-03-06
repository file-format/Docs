{
  "date" : "2022-06-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "XPI — starpplatformu instalēšanas pakotnes fails",
  "description":"Uzziniet par XPI faila formātu un API, kas var izveidot un atvērt XPI failus.",
  "linktitle" : "XPI",
  "menu" : {
    "docs" : {
    "identifier": "compression-xpi-lv",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-07"
}

## Kas ir XPI fails?

XPI fails ir instalācijas arhīvs, kas tiek saspiests, lai samazinātu faila lielumu. To izmanto Mozilla lietojumprogrammas, lai instalētu spraudņus un pievienojumprogrammas. Tas satur instalācijas skriptu vai manifestu faila saknē, kā arī vairākus datu failus. XPI failā var būt ietverti motīvi, rīkkopa vai Firefox spraudņi, kurus lietotājs var instalēt, lai kļūtu par daļu no pārlūkprogrammas Firefox, Thunderbird vai SeaMonkey.

## XPI faila formāts — vairāk informācijas

XPI faili tiek saglabāti diskā kā [ZIP](/compression/zip/) arhīvi, kas apvieno vairākus failus vienā saspiestā failā. XPI failā esošie faili var ietvert instalācijas skripta failus, piemēram, JS, un tīmekļa failus, piemēram, [CSS](/web/css/), [HTML](/web/html/) un [JSON](/web/json/). Dažreiz tajā var būt arī [PNG](/image/png/) attēlu faili, ko pievienojumprogramma izmantos kā ikonas.

### Kā apskatīt XPI faila saturu?

XPI fails praktiski ir ZIP arhīvs, kura saturu var skatīt, veicot šādas darbības.

 * Mainiet faila paplašinājumu no XPI uz ZIP
 * Izvelciet faila saturu, izmantojot jebkuru standarta dekompresijas utilītu, piemēram, WinZip (Windows, Mac), 7-Zip (Windows) vai Apple Archive Utility (Mac).

### Instalējiet XPI failu pārlūkprogrammā Firefox Android

Lielākoties cilvēki vēlas uzzināt, vai XPI failus var instalēt pārlūkprogrammā Firefox Android ierīcēs. Operētājsistēmā Android varat instalēt papildinājumu no XPI faila, atrodot failu un atverot to ar Firefox.

## Atsauces

* [XPInstall — Wikipedia](https://en.wikipedia.org/wiki/XPInstall)

* [Kā es varu atvērt XPI faila paplašinājumu?](https://support.mozilla.org/en-US/questions/1009049)


