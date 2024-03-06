{
  "date": "2021-07-15",
  "keywords": [
"LNK",
"pagarinājumu",
"failu",
"formātā",
"sistēma",
"LNK fails",
"saite",
"LNK faili",
"LNK dokumenti",
"pieteikumu",
"programmas"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "LNK - saites faila formāts",
  "description": "Uzziniet par LNK failu formātu un API, kas var izveidot un atvērt LNK failus.",
  "linktitle": "LNK",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-ln-lvk"
}
},
  "lastmod": "2021-07-15"
}

## Kas ir LNK fails? ##

LNK fails, kas ir analogs identitātei Mac sistēmā, ir Windows alternatīva jeb saite, kas kalpo kā savienojums ar oriģinālo attēla dokumentu mapi vai programmu. Tajā ir norādīts īsinājumtaustiņu galamērķa veids, pozīcija un faila nosaukums, kā arī lietojumprogramma, kas atver mērķa dokumentu, un papildu īsinājumtaustiņš.

Operētājsistēmā Windows izveidojiet failu, mapi vai izpildāmo programmu un izvēlieties Izveidot saīsni. Faila formāta atrašanās vieta un direktorija Sākums” ir divas LNK failu pamatfunkcijas. LNK failu faila formāts ir maskēts, un izliekta bultiņa norāda, ka tie ir īsceļi.

## LNK faila formāts ##

LNK failu formātiem parasti ir tāda pati ikona kā galamērķa failiem, taču tiem ir pievienota neliela bultiņa, kas parāda, ka fails norāda uz citu atrašanās vietu. Veicot dubultklikšķi uz saīsnes, tas darbojas tā, it kā lietotājs būtu veicis dubultklikšķi uz faktiskā faila.

LNK failiem, kuros ir lietojumprogrammu saīsnes, var būt rekvizīti, kas ietekmē programmas darbību. Lai mainītu atribūtus, ar peles labo pogu noklikšķiniet uz saīsnes faila un izvēlieties **Properties**, pēc tam mainiet lauku Mērķis.

Tā vietā, lai būtu failu paplašinājumi, LNK faili ir Windows Explorer paplašinājumi. Kā termināļa paplašinājumu .lnk dokumentus var izmantot tikai programmā Windows Explorer, lai aizstātu failu, un tiem ir arī citi mērķi programmā Windows Explorer, ne tikai kā saīsne uz lokālo dokumentu. Arī šie faili sākas ar burtu L.

Lai gan saīsnes veido saites uz konkrētiem failiem un direktorijiem, tie var kļūt nedarbojami, ja mērķis tiek mainīts uz citu atrašanās vietu. Explorer sāks labot saīsnes mapi, kas norāda uz mirušu mērķi, kad tā tiks atvērta.


## Tehniskā specifikācija Nr.

Tikai tad, ja mapes skatīšanas iestatījums Paslēpt atpazīto failu tipu paplašinājumus nav atzīmēts, sistēma Windows nerāda dokumentu īsinājumtaustiņu paplašinājumu .lnk. Lai gan tas nav ieteicams, varat iespējot faila paplašinājuma rādīšanu, noņemot rekvizītu NeverShowExt no Windows reģistra vienuma HKEY_CLASSES_ROOT\lnk faila.

Lai to izdarītu, veiciet tālāk norādītās darbības.

* Atveriet Reģistrācijas redaktoru, uzdevumjoslas meklēšanas laukā ievadot Regedit un izvēloties programmu
* Lietojumprogrammā dodieties uz Computer\HKEY HKEY_CLASSES_ROOT\lnkfile atrašanās vietu
* Izveidojiet vienuma dublējumu, ar peles labo pogu noklikšķinot uz tā un izvēloties Eksportēt
* Atlasiet un izdzēsiet atribūtu NeverShowExt.
* Windows ir jārestartē


## Atsauce Nr.

* [LNK - Wikipedia](https://en.m.wikipedia.org/wiki/Shortcut_(computing))
