{
  "date" : "2023-01-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Lär dig mer om Unreal Static Meshes VPK-filformat och API:er som kan skapa och öppna VPK-filer.",
  "title" : "VPK-fil - Unreal Static Meshes-fil",
  "linktitle" : "VPK",
  "menu" : {
    "docs" : {
      "identifier":"game-vpk-sv",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-16"
}

## Vad är VPK fil?

En .vpk-fil är ett filformat som används av **Source Engine**, en spelmotor utvecklad av Valve Corporation. VPK-filer används för att paketera spelinnehåll, såsom modeller, texturer och ljud, och används ofta i spel som Team Fortress 2, Left 4 Dead och Counter-Strike: Global Offensive. Filerna kan öppnas och extraheras med en mängd olika verktyg, såsom GCFScape och VPK Tool.

## VPK-filformat - Mer information

VPK-filer lagras på skivan som binära filer. En enda vpk-fil kan vara en del av ett VPK-paket eller kan fungera som en oberoende rå VPK-fil. Information som kan lagras i en VPK-fil inkluderar kartor, material, spelinnehåll och koreografiscener.

### Hur skapar jag en VPK-fil?

Det finns flera sätt att skapa en .vpk-fil, beroende på tillgängliga verktyg.

1. `Använda VPK-verktyget:` Detta är ett kommandoradsverktyg som kan användas för att skapa och extrahera VPK-filer. En VPK-fil kan skapas med följande kommando:
```
"vpk.exe -M <directory> <output_file.vpk>"
```
Detta kommer att skapa en VPK-fil från den angivna katalogen och spara den som den angivna utdatafilen.

1. `Använda Hammer Editor:` Hammer Editor är ett verktyg som ingår i Source SDK som kan användas för att skapa och redigera nivåer för spel som använder Source-motorn. Det inkluderar också möjligheten att skapa VPK-filer genom att högerklicka på en mapp på fliken Filsystem och välja Skapa VPK

1. `Att använda Valves VPK-skapare:` Detta är ett verktyg utvecklat av Valve som används för att paketera och distribuera spelinnehåll. Detta verktyg kan användas för att skapa VPK-filer och det är också det officiella verktyget för att skapa VPK-filer.

## Referenser

 * [Valve Software](https://www.valvesoftware.com/en/)
 * [VPK-utvecklarens resurser](https://developer.valvesoftware.com/wiki/GCF)

