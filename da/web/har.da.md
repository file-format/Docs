{
  "date": "2021-07-08",
  "keywords": [
"HAR",
"Fil",
"Udvidelse",
"Filformat",
"Filudvidelse",
"JSON",
"Arkiv fil"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HAR - HTTP-arkivfilformat",
  "description": "Din filformatguide for at lære, hvad en HAR-fil og API'er er, der kan oprette og åbne HAR-fil.",
  "linktitle": "HAR",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ha-dar"
}
},
  "lastmod": "2021-07-08"
}

## Hvad er en HAR fil?

En fil med .har (HTTP Archive)-fil er en HTTP-arkivfil, der gemmer sessionsdata, der overføres via mange browsere (såsom Chrome, Safari, IE, Firefox osv.) i filformatet [JSON](/web/json/). De data, der overføres over internettet mellem serveren og klienten (i dette tilfælde brugerens browser) indeholder HTTP-anmodnings- og svarheadere, der er gemt i HAR-filen. Den indeholder yderligere detaljerede oplysninger om ydeevnedata om websider, der er indlæst i browseren. HAR-filer kan åbnes i enhver teksteditor, såsom Notepad på Microsoft Windows OS og TextEdit på Apple MacOS.

## HAR-filformat - flere oplysninger

HAR-filer gemmer sessionsoplysninger i almindelig tekstfil ved hjælp af det populære JSON-format. Specifikationerne for HAR-filformatet blev produceret af Web Performance Group fra World Web Consortium (W3C), men kunne ikke offentliggøres. Det har dog med succes defineret et arkivformat for HTTP-transaktioner.

Ud over at overvåge overførslen af anmodnings- og svaroplysninger, bruges HAR-filer af udviklere til at logge webbrowserens ydeevne med hensyn til sideindlæsningshastighed, indholdsindlæsningsvarighed, indlæst indhold, forespørgsler udført for at få svaret fra browseren og mange andre .

## Hvorfor bruge HAR-filer?

HAR-filer kan være nyttige til at forbedre et websteds ydeevne ved at evaluere lange indlæsningstider, sidegengivelsestider og svartider. HAR-filer kan analyseres for at finde sådanne problemer og løse eventuelle problemer med webstedet for at forbedre ydeevnen.

## Hvordan genererer man HAR-fil?

Så hvordan genererer man en HAR-fil? Nå, dette afhænger af hvilken type browser du bruger til at generere en HAR-fil. I denne vejledning viser vi trinene til Google Chrome-browseren. Metoder til generering af HAR-filer ved hjælp af Safari, Firefox osv. kan nemt søges på internettet og følges.

### Trin til at generere HAR-fil ved hjælp af Google Chrome

Følgende trin kan udføres på en webside, hvor der er problemer.

 1. Åbn den webside i Google chrome, hvor problemet opstod.
 1. Åbn udviklerværktøjet (inspicer element).
 1. Gå til venstre i panelet for at starte filoptagelsen. Der er en lille rund rød knap i dette afsnit.
 1. Klik på Ryd ikonet for at slette eventuelle logposter i browseren.
 1. For at gemme det ønskede indhold som vist ovenfor, højreklik og klik på Gem som HAR-fil

## Referencer

* [HAR-filformat - Wikipedia](https://en.wikipedia.org/wiki/HAR_(file_format))


