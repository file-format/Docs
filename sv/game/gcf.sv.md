{
  "date" : "2023-01-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Lär dig om GCF-filformat och API:er som kan skapa och öppna GCF-filer.",
  "title" : "GCF-fil - Nadeo Game GCF-format",
  "linktitle" : "GCF",
  "menu" : {
    "docs" : {
      "identifier":"game-gcf-sv",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-19"
}

## Vad är en GCF fil?

En .gcf-fil är en spelcache-fil som används av Steam-spelplattformen. Den innehåller speldata som texturer, modeller och andra filer som används av spelet. Dessa filer lagras på användarens dator och används för att minska mängden data som behöver laddas ner vid uppdatering eller installation av ett spel. .gcf-filerna kan också användas för att skapa säkerhetskopior av ett spels installation eller för att överföra ett spel mellan datorer.

GCF-filer kan läsas och skrivas av Open Source C++ programmeringsbibliotek, **HLLib**.

## GCF filformat

GCF-filer sparas på skivan som binära filer. GCF användes ursprungligen som en akronym för Grid Cache File (Steams tidiga kodnamn var Grid), men senare togs den som Game Cache File. En GCF-fil är en arkivfil som lagrar Steam-spel. Allt officiellt innehåll laddas ner som GCF-filer. GCF-filer kan också delas mellan spel.

OBS: GCF är föregångaren till [VPK file format](/game/vpk/).
## Referenser

* [Valve Software](https://www.valvesoftware.com/en/)

* [GCF-filformat](https://developer.valvesoftware.com/wiki/GCF)

* [HLLib - Open Source C++ programmeringsbibliotek för att läsa GCF-filer](https://developer.valvesoftware.com/wiki/HLlib)


