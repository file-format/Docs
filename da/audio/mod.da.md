{
  "date": "2021-08-04",
  "keywords": [
"mod",
"mp3",
"fil",
"udvidelse",
"format",
"hvad er mod filformat",
"musik",
"mod filformat",
"mod mod MP3",
"mod filformatspecifikation"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om MOD-filformat og API'er, der kan oprette, konvertere og åbne MOD-filer.",
  "title": "MOD - Musikmodulfil",
  "linktitle": "MOD",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-mo-dad"
}
},
  "lastmod": "2021-08-04"
}

## Hvad er en MOD-fil?
En fil med filtypenavnet .mod er en musikmodulfil oprettet ved at bruge standardmusikmodulformatet, som er baseret på **Amiga-modulformatet** udviklet af Karsten Obarski og udgivet med **Ultimate Soundtracker**-softwaren til Commodore Amiga system. I lighed med en [MIDI](/audio/mid/)-fil består den af nodemønstre og lydeksempler, der repræsenterer forskellige instrumenter, der afspilles i overensstemmelse med noderne. MOD-filer bruges især i videospil som baggrundsmusik og i **demoscene** computerkunst-subkulturen.

## MOD filformat

MOD er et computerfilformat, der bruges til at repræsentere musik, og det var det første modulfilformat. MOD-filer bruger filtypen .mod, undtagen på **Amiga**, som læser en fils header for at bestemme filtypen, så den er ikke afhængig af filtypenavne. En MOD-fil består af et sæt af forskellige instrumenter i form af samples, et antal mønstre, der angiver hvordan og hvornår samplerne skal spilles, og en liste over hvilke mønstre der skal spilles i hvilken rækkefølge.

### MOD-filformatspecifikationer

Et MOD-filmønster er faktisk designet i en sequencer-brugergrænseflade som en tabel med en kolonne pr. kanal, så denne tabel har fire kolonner (en for hver Amiga-hardwarekanal. Hver kolonne har 64 rækker).

En celle i tabellen kan forårsage, at en af følgende handlinger sker på dens kolonnes kanal, når dens rækkes tid er nået:

- Start et instrument med at spille en ny tone i denne kanal ved en given lydstyrke, eventuelt med en speciel effekt på den
- Skift lydstyrken eller specialeffekten, der anvendes på den aktuelle node
- Skift mønsterflow; spring til en bestemt sang eller mønsterposition eller loop inde i et mønster
- Gøre ingenting; enhver eksisterende note, der afspilles på denne kanal, fortsætter med at spille

Et instrument er en enkelt prøve sammen med en valgfri specifikation af, hvilken del af prøven, der kan gentages for at holde en solid tone.

### Timing
Den mindste tidsramme var 0,02 sekunder i den originale MOD-fil, eller et vertical blanking (VSync) interval, fordi den originale software brugte VSync-timingen på skærmen, der kørte ved 50 Hz (for PAL) eller 60 Hz (for NTSC) til timing.

## Referencer

* [MOD (filformat) - af Wikipedia](https://en.wikipedia.org/wiki/MOD_(file_format))


