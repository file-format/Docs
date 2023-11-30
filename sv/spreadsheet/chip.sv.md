{
"date": "2023-03-01",
  "keywords": [
"chipfil",
"vad är en chipfil",
"fil",
"hur man öppnar chipfil",
"chip filtillägg",
"förlängning"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "CHIP-filformat - Microarray-anteckningsfil",
  "description":"Läs mer om CHIP-filformat och API:er som kan skapa och öppna CHIP-filer.",
"linktitle": "CHIP",
  "menu": {
    "docs": {
      "identifier": "spreadsheet-chip",
      "parent": "spreadsheet"
}
},
"lastmod": "2023-03-01"
}

## Vad är CHIP fil?

CHIP-fil är en mikroarray-anteckningsfil och är relaterad till programvaran Gene Set Enrichment Analysis (GSEA). GSEA är en beräkningsmetod som utvärderar om en fördefinierad uppsättning gener (en genuppsättning) visar statistiskt signifikanta skillnader mellan två biologiska tillstånd, såsom frisk kontra sjuk vävnad eller läkemedelsbehandlade kontra obehandlade celler. För att utföra GSEA behöver du en genuttrycksdatabas och en genuppsättningsdatabas. Genuppsättningsdatabasen innehåller information om generna i genuppsättningarna, såsom deras funktion, väg eller vävnadsspecifikt uttryck.

En CHIP-fil är en specifik typ av genuppsättningsdatabas som används av GSEA. Den innehåller information om de gener och genuppsättningar som är relevanta för den mikroarrayplattform som används i experimentet. CHIP-filen tillhandahåller kommentarer för varje sond på mikroarrayen, såsom gensymbol, gennamn, genbeskrivning och kromosomal placering. Denna information används för att matcha proberna med generna i genuttrycksdatauppsättningen och för att tilldela dem till lämpliga genuppsättningar för GSEA-analys.

För att använda en CHIP-fil i GSEA måste du importera den till programvaran och länka den till din microarray-datauppsättning. GSEA stöder olika microarray-plattformar och tillhandahåller förbyggda CHIP-filer för många av dem. Men du kan också skapa din egen CHIP-fil med anteckningsdatabaser från externa källor, som NCBI eller Ensembl.

## Mer information

En CHIP-fil är inte ett kalkylblad, men den kan öppnas och redigeras i ett kalkylprogram som Microsoft Excel eller Google Sheets. En CHIP-fil är en typ av textfil som innehåller tabbavgränsade data, som enkelt kan importeras till ett kalkylprogram för visning och redigering.

I ett kalkylprogram kan du manipulera data i en CHIP-fil för att lägga till, ta bort eller ändra kommentarer för generna och genuppsättningarna på mikroarrayen. Du kan till exempel använda ett kalkylbladsprogram för att lägga till anpassade kommentarer för generna som inte ingår i den ursprungliga CHIP-filen, eller för att slå samman flera CHIP-filer från olika källor till en enda fil.

Det är dock viktigt att notera att en CHIP-fil har ett specifikt format och struktur som måste underhållas för kompatibilitet med GSEA-programvaran. Om du ändrar innehållet i en CHIP-fil i ett kalkylprogram bör du se till att ändringarna inte ändrar filformatet eller innehållet på ett sätt som kan påverka GSEA-analysens noggrannhet eller giltighet.

## Hur öppnar man filen CHIP?

Eftersom CHIP-filen innehåller tabbavgränsade data, så om du vill se kalkylbladsdata kan du öppna den i Microsoft Excel.

## Referenser
* [GSEA](https://en.wikipedia.org/wiki/Gene_set_enrichment_analysis)
