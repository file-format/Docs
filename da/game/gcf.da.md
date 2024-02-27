{
  "date" : "2023-01-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Lær om GCF-filformat og API'er, der kan oprette og åbne GCF-filer.",
  "title" : "GCF-fil - Nadeo Game GCF-format",
  "linktitle" : "GCF",
  "menu" : {
    "docs" : {
      "identifier":"game-gcf-da",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-19"
}

## Hvad er en GCF fil?

En .gcf-fil er en spilcache-fil, der bruges af Steam-spilplatformen. Det indeholder spildata såsom teksturer, modeller og andre filer, der bruges af spillet. Disse filer gemmes på brugerens computer og bruges til at reducere mængden af data, der skal downloades, når et spil opdateres eller installeres. .gcf-filerne kan også bruges til at lave sikkerhedskopier af et spils installation eller til at overføre et spil mellem computere.

GCF-filer kan læses og skrives af Open Source C++ programmeringsbiblioteket, **HLLib**.

## GCF filformat

GCF-filer gemmes på disken som binære filer. GCF blev oprindeligt brugt som et akronym for Grid Cache File (Steams tidlige kodenavn var Grid), men senere blev det taget som Game Cache File. En GCF-fil er en arkivfil, der gemmer Steam-spil. Alt officielt indhold downloades som GCF-filer. GCF-filer kan også deles mellem spil.

BEMÆRK: GCF er forgængeren til [VPK file format](/game/vpk/).
## Referencer

* [Valve Software](https://www.valvesoftware.com/en/)

* [GCF-filformat](https://developer.valvesoftware.com/wiki/GCF)

* [HLLib - Open Source C++-programmeringsbibliotek til læsning af GCF-filer](https://developer.valvesoftware.com/wiki/HLlib)


