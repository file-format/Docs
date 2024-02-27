{
  "date": "2022-12-13",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om MCR-filformat og API'er, der kan oprette og åbne MCR-filer.",
  "title": "MCR - Minecraft Region File Format",
  "linktitle": "MCR",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-mc-dar"
}
},
  "lastmod": "2022-12-14"
}

## Hvad er en MCR fil?

Minecraft MCR-filformatet er et dataformat, der bruges af Minecraft til at gemme terrænstykker af en Minecraft World. Det er baseret på NBT-formatet (Named Binary Tag), som er udviklet af udviklerne af den populære open source-spilmotor, Minecraft Forge. MCR-filtypen blev introduceret i begyndelsen og blev senere erstattet af [MCA file format](/game/mca/).

## MCR filformat

MCR-filformatet er struktureret som en række navngivne binære tags, som hver indeholder en bestemt type data. Taget på øverste niveau er Level-tagget, som indeholder alle data for et enkelt spilniveau. Inden for Level-tagget er der flere andre navngivne tags, der gemmer forskellige typer data, såsom Data-tagget, som gemmer information om spilverdenen, og Entities og TileEntities-tags, som gemmer data om hhv spilobjekter og fliseenheder i verden.

## Hvad er inde i MCR-filformat?

I Minecraft MCR-filformatet er en region et 32x32 blokområde i spilverdenen. MCR-formatet opdeler spilverdenen i regioner for at administrere dataene mere effektivt og give mulighed for hurtigere indlæsning og lagring af spilniveauer. Hver region er gemt i en separat fil, og MCR-filformatet bruger et system af koordinater til at identificere hver regions position i spilverdenen. Koordinaterne for et område bestemmes af blokkoordinaterne for det nederste venstre hjørne af området. For eksempel vil en region med koordinater (-1,0) være placeret en region til venstre og nul regioner ned fra oprindelsen af spilverdenen.

## MCR filformatspecifikationer

MCR-filformatspecifikationerne er offentligt tilgængelige. Specifikationerne for NBT-formatet, som MCR-formatet er baseret på, er tilgængelige på Minecraft Forge-webstedet. Derudover har [Minecraft Wiki](https://minecraft.fandom.com/wiki/Region_file_format) også detaljerede oplysninger om MCR-filformatet, inklusive dets struktur og de forskellige datatyper, som det understøtter.

### Komprimerede data i MCR-filer

Minecraft MCR-filformatet understøtter komprimering. MCR-filformatet er baseret på The [NBT format](https://minecraft.fandom.com/wiki/NBT_format), der gør det muligt at lagre data i en komprimeret form. Dette hjælper med at reducere størrelsen af MCR-filer og gøre dem mere effektive at overføre og gemme. Dette er en vigtig egenskab ved MCR-filformatet, da det giver spillere mulighed for at dele store Minecraft World-terrændata med andre.

## Referencer

* [World Editor for Minecraft](https://www.mcedit.net/)

* [Om Minecraft](https://www.minecraft.net/)

* [Region filformat](https://minecraft.fandom.com/wiki/Region_file_format)

* [NBT-format](https://minecraft.fandom.com/wiki/NBT_format)


