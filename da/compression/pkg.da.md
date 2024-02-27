{
  "date": "2021-04-08",
  "keywords": [
"pkg fil",
"pkg filformat",
"hvad er en pkg fil",
"fil",
"pkg eksempel",
"pkg filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PKG - Extensible Archive File Format",
  "description": "Lær om PKG filformat og API'er, der kan oprette og åbne PKG filer.",
  "linktitle": "PKG",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-pk-dag"
}
},
  "lastmod": "2021-04-13"
}

## Hvad er PKG fil?

En fil med filtypenavnet .pkg er en installationspakkefil, der bruges til at installere software på macOS. Ud over Macintosh-computere bruges den også på iPhone. Det indbyggede Apple installationsprogram kan bruges til at installere indholdet af en PKG-fil. En PKG-fil ligner en MSI-fil, der bruges på Windows-operativsystemet til installation af software. Under installationen kan disse pakkefiler logge beskeder, der giver dig en idé om, hvilke ekstra ting der er installeret af denne pakke.

## PKG filformat

PKR er binære filer, der er komprimeret for at reducere den samlede filstørrelse. Siden OSX 10.5 er flade pakker med enkelte installationsfiler blevet introduceret af Apple. Disse er anderledes end de tidligere pakkeformater, der kom som bundter i stedet for enkeltfiler. Disse bundtede pakker indeholdt et struktureret mappehierarki, der lagrede filer på en måde, der letter deres hentning via en eller anden indeksfil. Det flade PKG-filformat er faktisk et [XAR](/compression/xar/)-arkiv, der har en:

 * Header - Definerer størrelse, kontrolsum og versionsoplysninger
 * Indholdsfortegnelse - Et XML-dokument, der er (og skal) kodes som UTF-8 og gemmes i begyndelsen af filen, hvilket gør det nemt at scanne gennem arkivet for at udpakke individuelle filer
 * Heap - ustruktureret bunke af data, der refereres til af TOC

## Referencer

* [Flat pakke filformat](http://s.sudre.free.fr/Stuff/Ivanhoe/FLAT.html)

* [PKG - Wikipedia](https://en.wikipedia.org/wiki/.pkg)


