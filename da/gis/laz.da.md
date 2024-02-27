{
  "date": "2023-07-18",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LAZ - Komprimeret LIDAR-dataudvekslingsfil",
  "description": "Lær om LAZ-filformat og API'er, der kan oprette og åbne LAZ-filer.",
  "linktitle": "LAZ",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-la-daz"
}
},
  "lastmod": "2023-07-18"
}

## Hvad er en LAZ-fil?

LAZ-filformatet er en komprimeret version af LAS-filformatet (Lidar LASer), som er specielt designet til lagring af lidar-punktskydata. LAZ-filer bevarer de samme data og struktur som LAS-filer, men anvender tabsfri komprimeringsteknikker for at reducere filstørrelsen og samtidig bevare den originale datagengivelse.

## LAZ filformat - kort historie

LAZ-filformatet blev udviklet til at imødekomme den voksende efterspørgsel efter effektiv lagring og transmission af store lidar-datasæt. Ved at komprimere LAS-filer reducerer LAZ-filer deres størrelse betydeligt, hvilket gør dem nemmere at administrere og overføre. Kompressionen opnås ved at anvende en kombination af forskellige algoritmer, såsom entropi-kodning og variabel-længde-kodning, for at repræsentere lidar-punkt-attributter i en mere kompakt form.

## LAZ filformat

På trods af komprimeringen bevarer LAZ-filer evnen til fuldt ud at gendanne de originale LAS-data uden tab af information. Det betyder, at når en LAZ-fil først er dekomprimeret, kan den behandles og analyseres på samme måde som en ukomprimeret LAS-fil. Kompressions- og dekomprimeringsprocessen udføres typisk ved hjælp af specialiseret software eller biblioteker, der understøtter LAZ-formatet.

LAZ-filformatet opretholder kompatibilitet med LAS-filer, hvilket sikrer interoperabilitet på tværs af lidar-software og behandlingsværktøjer. Det betyder, at applikationer, der kan læse og behandle LAS-filer, typisk kan håndtere LAZ-filer uden ændringer. Derudover inkluderer LAZ-filer stadig filoverskriften, variabel længde-poster (VLR'er) og punktdataposter, hvilket bevarer den samme struktur som LAS-filer.

## Fordele ved LAZ-filformat

**Reduceret filstørrelse:** LAZ-komprimering reducerer filstørrelsen på lidar-datasæt betydeligt, hvilket gør dem mere håndterbare og nemmere at gemme og overføre.

**Dataintegritet:** LAZ-komprimering er tabsfri, hvilket betyder, at de dekomprimerede data er en nøjagtig kopi af de originale LAS-data, hvilket sikrer intet tab af information eller præcision.

**Interoperabilitet:** LAZ-filer er kompatible med LAS-filer, hvilket muliggør problemfri integration med eksisterende lidar-software og arbejdsgange.

**Effektiv behandling:** På grund af deres reducerede størrelse kan LAZ-filer indlæses og behandles hurtigere, hvilket forbedrer den samlede behandlings- og analysetid.

LAZ-filformatet er blevet bredt brugt i lidar-samfundet som en standard for komprimeret lidar-datalagring og -udveksling. Det tilbyder en balance mellem effektiv datakomprimering og dataintegritet, hvilket muliggør lettere håndtering af store lidar-datasæt, samtidig med at nøjagtigheden og kvaliteten af de originale data bevares.

## Referencer

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm
