{
  "date" : "2023-01-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Lær om Unreal Static Meshes VPK-filformat og API'er, der kan oprette og åbne VPK-filer.",
  "title" : "VPK-fil - Unreal Static Meshes-fil",
  "linktitle" : "VPK",
  "menu" : {
    "docs" : {
      "identifier":"game-vpk-da",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-16"
}

## Hvad er VPK fil?

En .vpk-fil er et filformat, der bruges af **Source Engine**, en spilmotor udviklet af Valve Corporation. VPK-filer bruges til at pakke spilindhold, såsom modeller, teksturer og lyde, og bruges ofte i spil som Team Fortress 2, Left 4 Dead og Counter-Strike: Global Offensive. Filerne kan åbnes og udpakkes ved hjælp af en række værktøjer, såsom GCFScape og VPK Tool.

## VPK-filformat - flere oplysninger

VPK-filer gemmes på disken som binære filer. En enkelt vpk-fil kan være en del af en VPK-pakke eller kan fungere som en uafhængig rå VPK-fil. Oplysninger, der kan gemmes i en VPK-fil, omfatter kort, materialer, spilindhold og koreografiscener.

### Hvordan opretter man VPK-fil?

Der er flere måder at oprette en .vpk-fil på, afhængigt af de tilgængelige værktøjer.

1. `Brug af VPK-værktøjet:` Dette er et kommandolinjeværktøj, der kan bruges til at oprette og udpakke VPK-filer. En VPK-fil kan oprettes ved hjælp af følgende kommando:
```
"vpk.exe -M <directory> <output_file.vpk>"
```
Dette vil oprette en VPK-fil fra den angivne mappe og gemme den som den specificerede outputfil.

1. `Brug af Hammer Editor:` Hammer Editor er et værktøj, der følger med Source SDK'et, som kan bruges til at oprette og redigere niveauer for spil, der bruger Source Engine. Det inkluderer også muligheden for at oprette VPK-filer ved at højreklikke på en mappe på fanen Filsystem og vælge Opret VPK

1. `Brug af Valves VPK-skaber:` Dette er et værktøj udviklet af Valve, som bruges til at pakke og distribuere spilindhold. Dette værktøj kan bruges til at oprette VPK-filer, og det er også det officielle værktøj til at oprette VPK-filer.

## Referencer

 * [Valve Software](https://www.valvesoftware.com/en/)
 * [VPK-udviklerressourcer](https://developer.valvesoftware.com/wiki/GCF)

