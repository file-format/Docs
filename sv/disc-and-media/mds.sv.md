{
  "date" : "2023-01-23",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Lär dig om MDS-filformat och API:er som kan skapa och öppna MDS-filer.",
  "title" : "MDS-filformat - Media Descriptor Sidecar-fil",
  "linktitle" : "MDS",
  "menu" : {
    "docs" : {
      "identifier":"disc-and-media-mds-sv",
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2023-01-23"
}

## Vad är MDS fil?

MDS (Media Descriptor Sidecar File) är en fil associerad med programvaran Alcohol 120% och Daemon Tools, som båda används för att skapa och hantera virtuella CD- och DVD-enheter. MDS-filen innehåller information om layouten för data på skivan, inklusive platsen för alla filer och skivans struktur. Detta gör att den virtuella enheten kan emulera beteendet hos en fysisk skiva, så att programvaran kan läsa data på den virtuella skivan som om det vore en riktig skiva.

When you want to mount an image file to a virtual drive, the MDS file is used along with the corresponding image file in a format such as ISO, BIN or CUE. The MDS file contains a description of the layout of the data on the disc, and the virtual drive software uses this information to create a virtual disc. This allows you to use the software as if you were using a physical disc, without having to physically insert the disc into the drive.

## Relation med alkohol 120%

Alcohol 120% är en populär programvara för att skapa och hantera virtuella CD- och DVD-enheter, och den använder filformatet MDS för att spara och komma åt skivbilder. MDS-filformatet ägs av Alcohol 120% och kan endast öppnas och användas av Alcohol 120% programvara eller annan programvara som stöder det.

## Hur öppnar man filen MDS?

För att öppna en MDS-fil i Alcohol 120%, måste du ha programvaran installerad på din dator. När du har installerat Alcohol 120% kan du öppna filen MDS genom att göra följande:

1. Lanseringsalkohol 120 %.
2. Klicka på Arkiv-menyn och välj Öppna.
3. Navigera till platsen för MDS-filen på din dator och välj den.
4. MDS-filen kommer nu att öppnas i Alcohol 120%, och du kommer att bli ombedd att välja motsvarande bildfil (som ISO, BIN eller CUE).
5. När du har valt bildfilen kommer Alcohol 120% att montera bilden på en virtuell enhet.

Alternativt kan du också öppna en MDS-fil genom att dubbelklicka på den, om Alcohol 120% är inställt som standardprogram för att öppna MDS-filer. Du kan också använda annan programvara som stöder MDS-format som Daemon Tools, Virtual CloneDrive, Virtual Drive Manager och MagicISO.

## Referenser
* [Alkohol 120 % - programvara för CD- och DVD-bränning](https://www.alcohol-soft.com/)


