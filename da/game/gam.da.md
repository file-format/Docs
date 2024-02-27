{
  "date": "2021-09-08",
  "keywords": [
"gam fil",
"gam filformat",
"hvad er en gam-fil",
"fil",
"gam eksempel",
"gam filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om GAM-filformat og API'er, der kan oprette og åbne GAM-filer.",
  "title": "GAM - Gemt spilfil",
  "linktitle": "GAM",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-ga-dam"
}
},
  "lastmod": "2021-09-08"
}

## Hvad er en GAM fil?
En fil med filtypenavnet .gam bruges af forskellige videospil til at engagere spillerne til at fortsætte, hvor de slap, næste gang programmet åbnes. Derfor betyder det, at GAM-filen gemmer oplysningerne om, hvad en bruger har gjort på hvilket tidspunkt. Disse filer kan gemmes automatisk af spilsoftwaren, eller spillerne kan blive bedt om at gemme, hvis de ønsker at fortsætte spillets tilstand, hvor de forlader.
## GAM filformat
GAM-filformat bruges grundlæggende til at opbevare spildata i gemte spil. GAM-filen gemmer ikke væsen, vareinformation eller område, i stedet gemmer den data om partimedlemmerne og de generelle eller globale variabler, som påvirker partimedlemmer.
### GAM-filens struktur
GAM-filen har følgende struktur:
- Header
- Partimedlemmer
- Partimedlem CRE fil data
- NPC'er (som ikke er med i partiet)
- NPC dræber statistik (indlejret i NPC struct)
- NPC CRE fildata
- Variabler (i det GLOBALE navneområde)
- Journalposter
- Kendte oplysninger
- Gemte lokationer
- Pocket Plane Locations
- Velkendt ekstra


 



## Referencer 

* [GAM-filformat](https://gibberlings3.github.io/iesdp/file_formats/ie_formats/gam_v2.0.htm#GAMEV2_0_Stored)



