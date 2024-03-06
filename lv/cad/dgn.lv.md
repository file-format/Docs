{
  "date": "2020-01-12",
  "keywords": [
"DGN",
"Fails",
"Formāts",
"Atvērt",
"Lasīt",
"API",
"MicroStation",
"Intergraph Interactive Graphics Design System"
],
  "author":{
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DGN — MicroStation CAD dizaina faila formāts",
  "description": "Uzziniet par DGN faila formātu un API, kas var izveidot un atvērt DGN failus.",
  "linktitle": "DGN",
  "menu":{
    "docs":{
      "parent": "cad",
      "identifier": "cad-dg-lvn"
}
},
  "lastmod": "2020-01-12"
}

## Kas ir DGN fails?

Fails ar paplašinājumu .dgn (dizains) ir zīmēšanas fails, ko izveido un atbalsta CAD lietojumprogrammas, piemēram, MicroStation un Intergraph Interactive Graphics Design System. To izmanto, lai izveidotu un saglabātu projektus tādiem būvniecības projektiem kā lielceļi, tilti un ēkas. Formāts ir līdzīgs Autodesk [DWG](/cad/dwg/) faila formātam un tiek uzskatīts par tā konkurentu. DNG failus var saglabāt kā Intergraph standarta faila formātu vai V8 DGN. DGN var konvertēt uz vairākiem citiem formātiem, piemēram, DWG, [BMP](/image/bmp/), [JPEG](/image/jpeg/), [PDF](/pdf/), [GIF](/image/gif/) un citiem. To var atvērt ar Autodesk AutoCAD, Bentley View un Bentley Systems MicroStation papildus citām lietojumprogrammām, piemēram, Corel PaintShop Photo Pro un IMSI TurboCAD Deluxe versijām.

## V8 DGN faila formāts

MicroStation V8 DGN fails sastāv no viena vai vairākiem modeļiem. Modelis ir konteiners elementiem. V8 DGN noņem visus uz failu formātu balstītus ierobežojumus, kas bija iepriekšējās MicroStation versijās. Tālāk ir sniegts DGN faila formāta uzlabojumu saraksts.

 * DGN faila līmeņu skaita ierobežojums ir noņemts, un katrs līmenis tiek nosaukts un saglabāts kā elements.
 * DGN faila maksimālajam fiziskajam izmēram nav nekādu ierobežojumu, un to ierobežo tikai operētājsistēma (piemēram, NT ierobežojums ir 4 GB)
 * Viena elementa maksimālais izmērs ir 128 KB.
 * Šūnas maksimālajam izmēram nav ierobežojumu.
 * Šūnu nosaukumi ir ierobežoti līdz aptuveni 500 rakstzīmēm.
 * Atsauču skaits, ko var pievienot DGN failam, nav ierobežots.
 * Līnijas virknei, formai vai punktu līknei var būt līdz 5000 virsotnēm.
 * Sarežģītās ķēdes vai sarežģītas formas sastāvdaļu skaits nav ierobežots.
 * Grafisko grupu skaits DGN failā nav ierobežots.
 * Žogs ir paralēls skatam, kurā tas ir novietots.
 * Viena teksta rindiņa var saturēt 65 535 rakstzīmes.
 * Teksta mezgla maksimālajam izmēram nav ierobežojumu.
 * Teksta mezglu skaits DGN failā nav ierobežots.
 * Katram elementam ir unikāls 64 bitu identifikators, kas nemainās elementa dzīves cikla laikā.
 * Katram elementam ir laika zīmogs, kas norāda pēdējo izmaiņu laiku.

## Atsauces

* [DNG — Wikipedia](https://en.wikipedia.org/wiki/DGN)

* [MicroStation V8 DGN File Format](https://web.archive.org/web/20120713013730/http://docs.bentley.com/ko/MicroStation/ustnhelp47.html)

