{
  "date": "2022-10-12",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HDM fails — rokas ierīces iezīmēšanas valodas fails",
  "description": "Uzziniet par HDM failu formātu un API, kas var izveidot un atvērt HDM failus.",
  "linktitle": "HDM",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-hd-lvm"
}
},
  "lastmod": "2022-10-12"
}

## Kas ir HDM fails?

HDM fails ir iezīmēšanas valodas tīmekļa lapas fails, kas tiek izveidots rokas ierīces iezīmēšanas valodā (HDML). Tajā ir iezīmēšanas atzīmes, kas ir līdzīgas valodai [HTML](/web/html/), taču tā ir paredzēta rokas elektroniskām ierīcēm, piemēram, viedtālruņiem un plaukstdatoriem. [HDML file format specifications](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html) tika iesniegti W3C standartizācijai, taču nevarēja kļūt par standartu. HDM pamatā ir [HDML](/web/hdml/) faila formāta specifikācijas, kas pieejamas W3 vietnē.

## HDM faila formāts — vairāk informācijas

HDM fails sastāv no iezīmēšanas tagiem, kas tiek renderēti vizuāli izstrādātā vietnē rokas ierīcēs. HDM faili tiek kopēti ierīcēs, izmantojot HDTP (Handheld Device Transport Protocol) protokolu, nevis HTTP protokolu, kas tiek izmantots HTML lapām.

## HDML failu elementi

Tālāk ir norādīti elementi, kas nodrošina HDML izpildlaika vidi un tiek saukti par lietotāja aģentu.

|Elements|Apraksts|
---|---|
|Kartes|Šis ir HDML pamatelements, un tas parāda un ļauj lietotājam mijiedarboties ar informācijas kartēm. |
|Klāvas|HDML kartes ir sagrupētas komplektos. HDML komplekts ir līdzīgs HTML lapai, jo to identificē ar URL [RFC1738], un tā ir servera pieprasītā satura vienība, ko kešatmiņā saglabā lietotāja aģents.|
|Darbības|Darbības var būt PREV, SOFT1-SOFT8 un HELP. Tie ir abstrakti un tiek atbalstīti lietotāja interfeisā lietotāja aģentam specifiskā veidā.|
|Darbības|Darbība ir kā saistītu karšu grupa, kas veic vienu loģisku funkciju. Tie var aptvert vienu vai vairākus klājus. HDML navigācijas un stāvokļa modelis ir strukturēts, pamatojoties uz darbībām.|
|Uz vēsturi balstīta navigācija|Lietotāja aģents uztur lietotājam parādīto karšu vēsturi. Katra karte, kurai tiek piekļūts, tiek pievienota karšu vēsturei. Lietotāja aģents ļauj lietotājam viegli pāriet atpakaļ uz iepriekšējo vēstures karti.|

## Atsauces

* [HDML — Wikipedia](https://en.wikipedia.org/wiki/Handheld_Device_Markup_Language)

* [HDML specifikācijas — W3 skolas](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html)


