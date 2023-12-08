{
"datum": "2023-05-03",
  "keywords": [
"TXD-fil",
"vad är en TXD-fil",
"Vad innehåller TXD-filen",
"fil",
"txd filtillägg",
"förlängning"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "TXD-filformat - Game Texture Dictionary",
  "description":"Läs mer om TXD-format och API:er som kan skapa och öppna TXD-filer.",
  "linktitle": "TXD",
  "menu": {
    "docs": {
      "identifier": "game-txd",
      "parent": "game"
}
},
"lastmod": "2023-05-03"
}

## Vad är TXD fil?

En TXD-fil är en texturordboksfil som används av Grand Theft Auto (GTA) serie av videospel. Den innehåller spelets texturer som appliceras på 3D-objekt i spelvärlden för att skapa en realistisk miljö.

TXD-filformatet är proprietärt för GTA-spel och är inte ett standardfilformat som används i andra applikationer. Det innehåller vanligtvis flera bildfiler i olika format som BMP, PNG eller TGA som används för att skapa spelets texturer.

TXD-filer skapas och redigeras vanligtvis med hjälp av specialiserade mjukvaruverktyg utformade för modding och anpassning av GTA-spel. Dessa verktyg tillåter användare att importera sina egna texturer och modifiera befintliga för att skapa anpassade skal, fordon, byggnader och andra spelelement.

## TXD-filformat - Mer information

Filstrukturen för TXD-filen är specifik för Grand Theft Auto (GTA)-serien av videospel och är inte ett standardfilformat som används i andra applikationer. Den allmänna strukturen för TXD-filen är dock följande:

1. Rubrik
2. Texturdata
3. Palettdata
4. Mipmaps

## Vad innehåller TXD-filen?

En TXD-fil innehåller texturdata som används av Grand Theft Auto (GTA)-serien av videospel för att rendera spelvärldens 3D-objekt. Specifikt innehåller en TXD-fil följande:

- **Texturbilder:** Det primära innehållet i TXD-filen är en eller flera texturbilder i en mängd olika format som BMP, PNG eller TGA. Dessa bilder används av spelmotorn för att applicera texturer på 3D-modeller i spelvärlden som byggnader, fordon och karaktärer.
- **Texturmetadata:** Varje texturbild i TXD-filen har associerad metadata som beskriver bildens format, upplösning och komprimeringstyp. Denna metadata används av spelmotorn för att ladda och återge texturerna korrekt.
- **Mipmaps:** Förutom de primära texturbilderna kan en TXD-fil även innehålla förrenderade mindre versioner av texturerna som kallas mipmaps. Dessa mipmaps används av spelmotorn för att förbättra prestandan genom att visa versioner av texturer med lägre upplösning när objektet som renderas är längre bort.
- **Palettdata:** För indexerade färgtexturer kan en TXD-fil också innehålla en palett som mappar färgindexen i texturen till specifika RGB-färgvärden.
- **Övriga data:** Slutligen kan en TXD-fil innehålla annan data som konfigurationsinformation för spelmotorn eller information om den specifika versionen av spelet.

## Referenser
* [TXD](https://gta.fandom.com/wiki/TXD)

