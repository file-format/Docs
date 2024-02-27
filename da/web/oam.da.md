{
  "date" : "2023-01-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "OAM-fil - Adobe Edge Animate Widget-filformat",
  "description" : "Lær om, hvad en OAM-fil og API'er er, der kan oprette og åbne OAM-fil.",
  "linktitle" : "OAM",
  "menu" : {
    "docs" : {
      "identifier":"web-oam-da",
      "parent" : "web"
}
},
  "lastmod" : "2023-01-30"
}

## Hvad er en OAM fil?

A .oam file a an animated widget file exported from Adobe Edge Animate Widget. Animations exported as OAM widget file format can be inserted into other Adobe applications such as InDesign Documents ([INDD file](/page-description-language/indd/), Dreamweaver, and Muse. OAM files are like deployment packages that can be readily inserted into other Adobe's projects to make use of them. OAM files contain information about the animation's assets, behaviors, and actionscript code. You can create an OAM file by publishing an Adobe Animate project [.AN file](/web/an/).
Brugere kan oprette OAM-filer ved at udgive fra et Edge Animate-projekt (.AN-fil).

## OAM filformat

En OAM-fil gemmes på disken som komprimeret [ZIP](/compression/zip/)-arkiv. Dette indebærer, at du kan omdøbe filtypenavnet til .zip og udpakke med et hvilket som helst komprimeringsværktøj, såsom WinZIP eller WinRAR. Den reducerede filstørrelse gør det nemmere at overføre og dele animationen med andre brugere over internettet.

### OAM-filstruktur

Den interne filstruktur af en .oam-fil er proprietær og ikke offentligt dokumenteret af Adobe. Det er dog kendt, at .oam-filer indeholder en samling af filer og ressourcer (såsom grafik, lyd og ActionScript-kode) pakket ind i en enkelt fil. Indholdet af en .oam-fil kan omfatte [XML](/web/xml/)-filer, SWF-filer og andre ressourcefiler. Den nøjagtige struktur af .oam-filen afhænger af den specifikke version af Adobe Animate, der blev brugt til at oprette den, samt typen af animation og aktiver, der er inkluderet i filen.

En OAM-fil indeholder følgende oplysninger.

`Aktiver:` Oplysninger om de grafik-, lyd- og videoaktiver, der bruges i animationen.

Behaviors:' Beskrivelser af de handlinger og interaktioner, der forekommer i animationen.

`ActionScript-kode:` Den kode, der bruges til at kontrollere animationens adfærd og interaktivitet.

`Publiceringsindstillinger:` Oplysninger om platformen og formatet, som animationen vil blive offentliggjort i, såsom HTML5 eller AIR.

`Metadata:` Additional information such as the animation's author, creation date, and version number.

## Hvordan åbner jeg filen OAM?

Du kan bruge følgende programmer til at åbne OAM filer.

 * Adobe Edge Animate CC (udgået)
 * Adobe Animate 2023
 * Adobe InDesign 2023
 * Adobe Dreamweaver 2021

## Referencer

* [OAM Publishing](https://helpx.adobe.com/animate/using/OAM-publishing.html)


