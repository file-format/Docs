{
  "date" : "2023-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LAS - Lidar LASer-filformat",
  "description":"Läs mer om LAS-filformat och API:er som kan skapa och öppna LAS-filer.",
  "linktitle" : "LAS",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2023-07-18"
}

## Vad är en LAS-fil?

Filformatet LAS (Lidar LASer) är ett binärt filformat speciellt utformat för att lagra lidar punktmolndata. Det utvecklades och underhålls av American Society for Photogrammetry and Remote Sensing (ASPRS) som ett standardiserat format för lidar-datautbyte och interoperabilitet.

LAS-filer lagrar detaljerad information om individuella lidarpunkter, inklusive deras 3D-koordinater (x, y och z), intensitetsvärden, klassificeringskoder och ytterligare attribut. Formatet stöder både diskret retur och fullvågslidardata, vilket möjliggör lagring av flera returer per laserpuls.

## LAS filformat

Strukturen för en LAS-fil består av tre huvudsektioner: filhuvudet, posterna med variabel längd (VLR) och punktdataposterna.

1. Filrubrik: Filhuvudet innehåller viktig information om LAS-filen, såsom dataformatversionen, punktdataformatet, antal punkter, begränsningsrutakoordinater, koordinatreferenssystem (CRS) och andra metadata. Det ger en sammanfattning av lidar-data som finns i filen.

2. Variable Length Records (VLR): VLR:er är valfria och kan lagra ytterligare metadata och anpassad information om lidardata. VLR:er möjliggör flexibilitet när det gäller att utöka formatet för att tillgodose specifika användarkrav. Exempel på VLR inkluderar information om sensorsystemet, databehandlingsparametrar eller klassificeringsscheman.

3. Punktdataposter: Punktdataposterna lagrar de faktiska lidarmätningarna. Varje punktdatapost representerar en enda lidarpunkt och innehåller attribut som x-, y- och z-koordinater, intensitetsvärden, klassificeringskoder (t.ex. mark, vegetation, byggnader) och andra användardefinierade attribut. Punktposterna kan också lagra tidsstämplar, returräkningar och skanningsvinklar.

LAS-filer stöder olika dataformat (0 till 10) för att rymma olika typer av lidar-data och den informationsnivå som behövs. Till exempel representerar format 0 ett enkelt punktformat med grundläggande information, medan format 1 till 3 ger mer omfattande data inklusive vågformsinformation för varje retur.

LAS-filer stöds brett av lidar-programvara och bearbetningsverktyg, vilket gör dem till ett standardformat för lidar-datautbyte och analys. Dessutom kan LAS-filer komprimeras med förlustfria komprimeringstekniker för att minska filstorleken samtidigt som den ursprungliga datatillförlitligheten bevaras. Den komprimerade versionen av LAS-filer kallas ofta LAZ, vilket erbjuder effektiv lagring och dataöverföringsmöjligheter.

## Referenser

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm
