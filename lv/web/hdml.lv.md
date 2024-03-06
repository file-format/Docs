{
  "date": "2021-08-21",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Rokas ierīces iezīmēšanas valodas fails",
  "description": "Uzziniet par HDML failu formātu un API, kas var izveidot un atvērt HDML failus.",
  "linktitle": "HDML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-hdm-lvl"
}
},
  "lastmod": "2021-08-21"
}

## Kas ir HDML fails?

Fails ar paplašinājumu .hdml (Handheld Device Markup Language) ir iezīmēšanas valoda, lai izveidotu tīmekļa lapas portatīvām elektroniskām ierīcēm, piemēram, rokas datoriem, viedtālruņiem un informācijas displeja ierīcēm. Tiek uzskatīts, ka HDML ir [SGML](https://en.wikipedia.org/wiki/Standard_Generalized_Markup_Language) valodas paplašinājums. HDML ir līdzīgs HTML, taču tas ir paredzēts bezvadu un rokas ierīcēm ar maziem displejiem, piemēram, PDA, mobilajiem tālruņiem un tā tālāk. Tas tika aizstāts ar WML, kuram tas darbojās kā nozīmīga ietekme.

## HDML faila formāts — vairāk informācijas

HDML ir marķēšanas valoda rokas ierīcēm, kuras pamatā ir iezīmēšanas tagi, kas līdzīgi HTML. HDML tika iesniegts W3C standartizācijai, taču tas nekad nekļuva par standartu. Tomēr tā faila formāta specifikācijas uzziņai ir pieejamas vietnē [W3 website](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html). [syntax for HDML language](https://www.w3.org/TR/hdml20-5.html#HEADING5-0) ir pieejama izstrādātāju uzziņai, un to var izmantot lietojumprogrammu izstrādes paraugam.

## HDML elementi

Tālāk ir norādīti elementi, kas nodrošina HDML izpildlaika vidi un tiek saukti par lietotāja aģentu.

|Elements|Apraksts|
---|---|
|Kartes|Šis ir HDML pamatelements, un tas parāda un ļauj lietotājam mijiedarboties ar informācijas kartēm. |
|Klāvas|HDML kartes ir sagrupētas komplektos. HDML komplekts ir līdzīgs HTML lapai, jo to identificē ar URL [RFC1738], un tā ir servera pieprasītā satura vienība, ko kešatmiņā saglabā lietotāja aģents.|
|Darbības|Darbības var būt PREV, SOFT1-SOFT8 un HELP. Tie ir abstrakti un tiek atbalstīti lietotāja saskarnē lietotāja aģentam specifiskā veidā.|
|Darbības|Darbība ir kā saistītu karšu grupa, kas veic vienu loģisku funkciju. Tie var aptvert vienu vai vairākus klājus. HDML navigācijas un stāvokļa modelis ir strukturēts, pamatojoties uz darbībām.|
|Uz vēsturi balstīta navigācija|Lietotāja aģents uztur lietotājam parādīto karšu vēsturi. Katra karte, kurai tiek piekļūts, tiek pievienota karšu vēsturei. Lietotāja aģents ļauj lietotājam viegli pāriet atpakaļ uz iepriekšējo vēstures karti.|

## Atsauces

* [HDML — Wikipedia](https://en.wikipedia.org/wiki/Handheld_Device_Markup_Language)

* [HDML specifikācijas — W3 skolas](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html)


