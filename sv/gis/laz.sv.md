{
  "date" : "2023-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LAZ - komprimerad LIDAR Data Exchange File",
  "description":"Läs mer om LAZ-filformat och API:er som kan skapa och öppna LAZ-filer.",
  "linktitle" : "LAZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2023-07-18"
}

## Vad är en LAZ-fil?

LAZ-filformatet är en komprimerad version av filformatet LAS (Lidar LASer), som är speciellt utformat för att lagra lidar punktmolndata. LAZ-filer behåller samma data och struktur som LAS-filer men använder förlustfria komprimeringstekniker för att minska filstorleken samtidigt som den ursprungliga datatroheten bevaras.

## LAZ-filformat - kort historik

LAZ-filformatet utvecklades för att möta den växande efterfrågan på effektiv lagring och överföring av stora lidar-datauppsättningar. Genom att komprimera LAS-filer minskar LAZ-filerna avsevärt deras storlek, vilket gör dem lättare att hantera och överföra. Kompressionen uppnås genom att använda en kombination av olika algoritmer, såsom entropikodning och kodning med variabel längd, för att representera lidarpunktsattribut i en mer kompakt form.

## LAZ filformat

Trots komprimeringen behåller LAZ-filer möjligheten att helt återställa de ursprungliga LAS-data utan att förlora information. Detta innebär att när en LAZ-fil väl har dekomprimerats kan den bearbetas och analyseras på samma sätt som en okomprimerad LAS-fil. Komprimeringen och dekomprimeringsprocessen utförs vanligtvis med hjälp av specialiserad programvara eller bibliotek som stöder LAZ-formatet.

LAZ-filformatet bibehåller kompatibilitet med LAS-filer, vilket säkerställer interoperabilitet mellan Lidar-programvara och bearbetningsverktyg. Detta innebär att applikationer som kan läsa och bearbeta LAS-filer vanligtvis kan hantera LAZ-filer utan några ändringar. Dessutom innehåller LAZ-filer fortfarande filhuvudet, poster med variabel längd (VLR) och punktdataposter, vilket bevarar samma struktur som LAS-filer.

## Fördelar med LAZ-filformat

**Minskad filstorlek:** LAZ-komprimering minskar filstorleken avsevärt för lidar-datauppsättningar, vilket gör dem mer hanterbara och lättare att lagra och överföra.

**Dataintegritet:** LAZ-komprimering är förlustfri, vilket innebär att de dekomprimerade data är en exakt kopia av den ursprungliga LAS-datan, vilket säkerställer ingen förlust av information eller precision.

**Interoperabilitet:** LAZ-filer är kompatibla med LAS-filer, vilket möjliggör sömlös integration med befintlig Lidar-programvara och arbetsflöden.

**Effektiv bearbetning:** På grund av deras minskade storlek kan LAZ-filer laddas och bearbetas snabbare, vilket förbättrar den övergripande bearbetnings- och analystiden.

LAZ-filformatet har blivit allmänt antaget i lidar-gemenskapen som en standard för komprimerad lidar-datalagring och utbyte. Det erbjuder en balans mellan effektiv datakomprimering och dataintegritet, vilket möjliggör enklare hantering av stora lidar-datauppsättningar samtidigt som noggrannheten och kvaliteten på originaldata bibehålls.

## Referenser

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm
