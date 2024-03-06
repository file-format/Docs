{
  "date": "2023-03-29",
  "keywords": [
"iestatījumu fails",
"kas ir iestatījumu fails",
"failu",
"iestatījumu faila paplašinājums",
"pagarinājumu"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "IESTATĪJUMI Faila formāts — Visual Studio iestatījumu fails",
  "description": "Uzziniet par SETTINGS formātu un API, kas var izveidot un atvērt SETTINGS failus.",
  "linktitle": "SETTINGS",
  "menu": {
    "docs": {
      "identifier": "settings-settings-lv",
      "parent": "settings"
}
},
  "lastmod": "2023-03-29"
}

## Kas ir SETTINGS fails?

Programmā Visual Studio .settings fails ir fails, kas satur lietojumprogrammu iestatījumus un ko var izmantot, lai saglabātu lietotāja preferences un konfigurācijas datus konkrētam projektam vai risinājumam. Šie iestatījumi var ietvert tādas lietas kā fontu lielums, logu izkārtojums, noklusējuma projekta iestatījumi un citas konfigurācijas opcijas. Failu .settings parasti automātiski izveido Visual Studio, kad projekts tiek izveidots un saglabāts direktorijā ar nosaukumu Properties in project folder. Pats fails ir XML fails, kas satur elementu un atribūtu kopu, kas nosaka dažādus projekta iestatījumus un vērtības.

Izstrādātāji var arī izveidot pielāgotus .settings failus projektiem un ar tiem saistītiem risinājumiem, kurus var izmantot, lai saglabātu papildu konfigurācijas datus, kas raksturīgi viņu lietojumprogrammai. Šiem pielāgotajiem .settings failiem var piekļūt un tos modificēt, izmantojot Visual Studio IDE vai kodu, izmantojot ConfigurationManager klasi .NET. .settings fails programmā Visual Studio ir svarīga IDE konfigurācijas sistēmas daļa un nodrošina veidu, kā izstrādātāji var saglabāt un pārvaldīt lietojumprogrammu iestatījumus un preferences savos projektos.

## IESTATĪJUMI Faila formāts — vairāk informācijas

The .settings file consists of several sections each containing one or more settings. Each setting is defined by a name and a value, including other attributes e.g. description or default value.

Viena no galvenajām .settings faila funkcijām ir tā, ka tas ļauj izstrādātājiem izveidot stingri drukātus iestatījumus, kas nozīmē, ka katram iestatījumam ir noteikts datu tips un tam var piekļūt un ar to var manipulēt, izmantojot kodu. Tas ļauj izstrādātājiem viegli saglabāt un izgūt lietojumprogrammu iestatījumus, nerakstot sarežģītu kodu vai manuāli pārvaldot konfigurācijas failus.

Visual Studio nodrošina iestatījumu noformētāja rīku, kas ļauj izstrādātājiem izveidot un pārvaldīt savu projektu iestatījumus, izmantojot grafisko interfeisu. Rīks ģenerē nepieciešamo kodu, lai piekļūtu iestatījumiem un mainītu tos, tādējādi izstrādātājiem atvieglojot to izmantošanu savā kodā.

Papildus noklusējuma .settings failam izstrādātāji var izveidot arī pielāgotus iestatījumu failus saviem projektiem. Šos failus var izmantot, lai saglabātu papildu konfigurācijas datus, kas ir specifiski to lietojumam, piemēram, savienojuma virknes, API atslēgas vai citus sensitīvus datus. Lai aizsargātu šos datus, izstrādātāji var šifrēt pielāgotos iestatījumu failus, izmantojot datu aizsardzības API (DPAPI), kas nodrošina datu drošību pat tad, ja fails ir apdraudēts.

## Atsauces
* [Visual Studio](https://en.wikipedia.org/wiki/Visual_Studio)


