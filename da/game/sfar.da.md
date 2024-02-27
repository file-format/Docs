{
  "date": "2021-10-20",
  "keywords": [
"sfar fil",
"sfar filformat",
"hvad er en sfar fil",
"fil",
"sfar eksempel",
"Mass Effect 3 DLC Filudvidelse",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om Mass Effect 3 SFAR-filformat og API'er, der kan oprette og åbne SFAR-filer.",
  "title": "SFAR - Mass Effect 3 DLC-fil",
  "linktitle": "SFAR",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-sfa-dar"
}
},
  "lastmod": "2021-10-20"
}

## Hvad er en SFAR fil?

En fil med filtypenavnet .sfar er en spildatafil, der bruges af Mass Effect 3 til at gemme dens DLC (downloadbart indhold) i et komprimeret, proprietært arkiv. Mass Effect 3 er et spil skabt af Electronic Arts, et førende spiludviklingsfirma. DLC-indholdet, der er gemt i en SFAR-fil, bruges til at udvide spillet med yderligere indhold og funktioner.

## SFAR-filformat - flere oplysninger

SFAR-filer gemmes/gemmes som komprimerede arkivfiler i binært filformat. Disse bruger både LZX- og LZMA-komprimeringsalgoritmer til at komprimere indholdet. SFAR-filer kan åbnes ved hjælp af DLC Editor, der leveres pakket med ME3 Explorer. Ud over SFAR kan DLC Editor udpakke andre spilfiler såsom [PCC](/game/pcc/).

## SFAR filformatspecifikationer

En SFAR-fil er opdelt i følgende fire hovedstykker.

### SFAR Header

SFF Header indeholder information om de forskellige bidder, der udgør filen.

### SFAR-filtabel

SFAR-filtabellen indeholder en liste over filposter, hvor hver post er 30 byte lang.

### Tabel i blokstørrelse

Block-Size indeholder flere poster, hvor hver post er 2 byes lang. Denne værdi angiver den blokstørrelse, der svarer til en post i filtabellen.

### Blokke

Blokstykker i en SFAR-fil indeholder dataene i SFAR-filen.

## Referencer

 * [DLC SFAR File Format - Research](https://www.tapatalk.com/groups/me3explorer/current-research-dlc-sfar-fileformat-t629.html)

