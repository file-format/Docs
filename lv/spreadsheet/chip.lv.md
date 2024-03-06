{
  "date": "2023-03-01",
  "keywords": [
"mikroshēmas fails",
"kas ir mikroshēmas fails",
"failu",
"kā atvērt mikroshēmas failu",
"mikroshēmas faila paplašinājums",
"pagarinājumu"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "CHIP faila formāts — Microarray anotācijas fails",
  "description": "Uzziniet par CHIP faila formātu un API, kas var izveidot un atvērt CHIP failus.",
  "linktitle": "CHIP",
  "menu": {
    "docs": {
      "identifier": "spreadsheet-chip-lv",
      "parent": "spreadsheet"
}
},
  "lastmod": "2023-03-01"
}

## Kas ir CHIP fails?

CHIP fails ir mikromasīva anotācijas fails un ir saistīts ar gēnu kopas bagātināšanas analīzes (GSEA) programmatūru. GSEA ir skaitļošanas metode, kas novērtē, vai iepriekš noteikta gēnu kopa (gēnu kopa) uzrāda statistiski nozīmīgas atšķirības starp diviem bioloģiskiem stāvokļiem, piemēram, veseliem un slimiem audiem vai ar zālēm apstrādātām un neapstrādātām šūnām. Lai veiktu GSEA, ir nepieciešama gēnu ekspresijas datu kopa un gēnu kopu datu bāze. Gēnu kopu datu bāze satur informāciju par gēniem gēnu kopās, piemēram, to funkciju, ceļu vai audu specifisko ekspresiju.

A CHIP file is a specific type of gene set database that is used by GSEA. It contains information about the genes and gene sets that are relevant to the microarray platform being used in the experiment. The CHIP file provides annotations for each probe on the microarray, such as the gene symbol, gene name, gene description, and chromosomal location. This information is used to match the probes with the genes in the gene expression dataset and to assign them to the appropriate gene sets for GSEA analysis.

Lai izmantotu CHIP failu pakalpojumā GSEA, tas ir jāimportē programmatūrā un jāsaista ar savu mikromasīvu datu kopu. GSEA atbalsta dažādas mikromasīvu platformas un daudzām no tām nodrošina iepriekš izveidotus CHIP failus. Tomēr jūs varat arī izveidot savu CHIP failu, izmantojot anotāciju datu bāzes no ārējiem avotiem, piemēram, NCBI vai Ensembl.

## Vairāk informācijas

CHIP fails nav izklājlapa, taču to var atvērt un rediģēt izklājlapu programmā, piemēram, Microsoft Excel vai Google Sheets. CHIP fails ir teksta faila veids, kas satur tabulēšanas atdalītus datus, kurus var viegli importēt izklājlapu programmā apskatei un rediģēšanai.

Izklājlapu programmā varat manipulēt ar datiem CHIP failā, lai pievienotu, noņemtu vai modificētu anotācijas gēniem un gēnu kopām mikromasīvā. Piemēram, varat izmantot izklājlapu programmu, lai pievienotu pielāgotas anotācijas gēniem, kas nav iekļauti sākotnējā CHIP failā, vai apvienotu vairākus CHIP failus no dažādiem avotiem vienā failā.

Tomēr ir svarīgi atzīmēt, ka CHIP failam ir īpašs formāts un struktūra, kas ir jāsaglabā, lai nodrošinātu saderību ar GSEA programmatūru. Ja modificējat CHIP faila saturu izklājlapu programmā, jums jāpārliecinās, ka modifikācijas nemaina faila formātu vai saturu tā, ka tas varētu ietekmēt GSEA analīzes precizitāti vai derīgumu.

## Kā atvērt CHIP failu?

Tā kā CHIP failā ir tabulēšanas atdalīti dati, tādēļ, ja vēlaties skatīt izklājlapas datus, varat tos atvērt programmā Microsoft Excel.

## Atsauces
* [GSEA](https://en.wikipedia.org/wiki/Gene_set_enrichment_analysis)
