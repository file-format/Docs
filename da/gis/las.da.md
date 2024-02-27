{
  "date": "2023-07-18",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LAS - Lidar LASer filformat",
  "description": "Lær om LAS-filformat og API'er, der kan oprette og åbne LAS-filer.",
  "linktitle": "LAS",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-la-das"
}
},
  "lastmod": "2023-07-18"
}

## Hvad er en LAS-fil?

LAS-filformatet (Lidar LASer) er et binært filformat, der er specielt designet til lagring af lidar-punktskydata. Det blev udviklet og vedligeholdt af American Society for Photogrammetry and Remote Sensing (ASPRS) som et standardiseret format til lidar-dataudveksling og interoperabilitet.

LAS-filer gemmer detaljerede oplysninger om individuelle lidar-punkter, herunder deres 3D-koordinater (x, y og z), intensitetsværdier, klassifikationskoder og yderligere attributter. Formatet understøtter både diskret retur- og lidardata i fuld bølgeform, hvilket giver mulighed for lagring af flere returneringer pr. laserpuls.

## LAS filformat

Strukturen af en LAS-fil består af tre hovedsektioner: filoverskriften, registreringerne med variabel længde (VLR'er) og punktdataposterne.

1. Filhoved: Filhovedet indeholder væsentlig information om LAS-filen, såsom dataformatversionen, punktdataformatet, antal punkter, afgrænsningsbokskoordinater, koordinatreferencesystem (CRS) og andre metadata. Det giver en oversigt over de lidar-data, der er indeholdt i filen.

2. Variable Length Records (VLRs): VLRs are optional and can store additional metadata and custom information about the lidar data. VLRs allow for flexibility in extending the format to accommodate specific user requirements. Examples of VLRs include information about the sensor system, data processing parameters, or classification schemes.

3. Punktdataregistreringer: Punktdataposterne gemmer de faktiske lidarmålinger. Hver punktdatapost repræsenterer et enkelt lidarpunkt og indeholder attributter såsom x-, y- og z-koordinater, intensitetsværdier, klassifikationskoder (f.eks. jord, vegetation, bygninger) og andre brugerdefinerede attributter. Punktregistreringerne kan også gemme tidsstempler, returtællinger og scanningsvinkler.

LAS-filer understøtter forskellige dataformater (0 til 10) for at imødekomme forskellige typer lidar-data og det nødvendige informationsniveau. For eksempel repræsenterer format 0 et simpelt punktformat med grundlæggende oplysninger, mens formaterne 1 til 3 giver mere omfattende data inklusive kurveinformation for hver retur.

LAS-filer er bredt understøttet af lidar-software og behandlingsværktøjer, hvilket gør dem til et standardformat for lidar-dataudveksling og -analyse. Derudover kan LAS-filer komprimeres ved hjælp af tabsfri komprimeringsteknikker for at reducere filstørrelsen og samtidig bevare den originale datagengivelse. Den komprimerede version af LAS-filer omtales ofte som LAZ, som tilbyder effektiv lagring og dataoverførsel.

## Referencer

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm
