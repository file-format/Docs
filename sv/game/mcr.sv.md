{
  "date": "2022-12-13",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lär dig om MCR-filformat och API:er som kan skapa och öppna MCR-filer.",
  "title": "MCR - Minecraft Region File Format",
  "linktitle": "MCR",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-mc-svr"
}
},
  "lastmod": "2022-12-14"
}

## Vad är en MCR fil?

Minecraft MCR-filformatet är ett dataformat som används av Minecraft för att lagra terrängbitar av en Minecraft World. Det är baserat på NBT-formatet (Named Binary Tag), som utvecklats av utvecklarna av den populära spelmotorn med öppen källkod, Minecraft Forge. MCR-filtypen introducerades i början och ersattes senare av [MCA file format](/game/mca/).

## MCR filformat

MCR-filformatet är strukturerat som en serie namngivna binära taggar, som var och en innehåller en specifik typ av data. Toppnivåtaggen är Level-taggen, som innehåller all data för en enda spelnivå. Inom Level-taggen finns det flera andra namngivna taggar som lagrar olika typer av data, till exempel Data-taggen, som lagrar information om spelvärlden, och Entities och TileEntities-taggarna, som lagrar data om spelobjekt och brickenheter i världen, respektive.

## Vad finns i MCR-filformat?

I Minecraft MCR-filformatet är en region ett 32x32 blockområde i spelvärlden. MCR-formatet delar in spelvärlden i regioner för att hantera data mer effektivt och möjliggöra snabbare laddning och lagring av spelnivåer. Varje region lagras i en separat fil, och MCR-filformatet använder ett system av koordinater för att identifiera positionen för varje region i spelvärlden. Koordinaterna för ett område bestäms av blockkoordinaterna för regionens nedre vänstra hörn. Till exempel skulle en region med koordinater (-1,0) vara belägen en region till vänster och noll regioner ner från spelvärldens ursprung.

## MCR-filformatspecifikationer

MCR-filformatspecifikationerna är allmänt tillgängliga. Specifikationerna för NBT-formatet, som MCR-formatet är baserat på, finns på Minecraft Forge-webbplatsen. Dessutom har [Minecraft Wiki](https://minecraft.fandom.com/wiki/Region_file_format) också detaljerad information om MCR-filformatet, inklusive dess struktur och de olika datatyper som den stöder.

### Komprimerad data i MCR-filer

Minecraft MCR-filformatet stöder komprimering. MCR-filformatet är baserat på [NBT format](https://minecraft.fandom.com/wiki/NBT_format) som gör att data kan lagras i komprimerad form. Detta hjälper till att minska storleken på MCR-filer och göra dem mer effektiva att överföra och lagra. Detta är en viktig funktion i MCR-filformatet, eftersom det tillåter spelare att dela stora Minecraft World-terrängdata med andra.

## Referenser

* [World Editor för Minecraft](https://www.mcedit.net/)

* [Om Minecraft](https://www.minecraft.net/)

* [Region File Format](https://minecraft.fandom.com/wiki/Region_file_format)

* [NBT-format](https://minecraft.fandom.com/wiki/NBT_format)


