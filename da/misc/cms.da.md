{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "CMS-filformat - Connection Manager Service Profile File",
  "description":"Lær om CMS-filer og API'er, der kan oprette og åbne CMS-filer.",
  "linktitle" : "CMS",
  "menu" : {
    "docs" : {
      "identifier": "misc-cms-da",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Hvad er en CMS fil?

En CMS-fil er en datafil, der indeholder profiloplysninger, der bruges af Microsoft Windows Connection Manager. Det lader fjernbrugere oprette forbindelse til et netværk ved hjælp af disse profiloplysninger. Oplysninger gemt i en CMS-fil inkluderer data om brugerens operativsystem og tilladelser, der bruges til at etablere en forbindelse mellem en fjernbruger og netværket. CMS-administratorer bruger Connection Manager Administrator Kit (CMAK) til at generere CMS-filer.

## CMS-filformat - flere oplysninger

CMS-filer findes ikke almindeligt på brugermaskiner. Da disse bruges specifikt til at tillade fjernbrugere til et netværk, vil du finde disse på computere, der bruges til at oprette forbindelse til et firmanetværk eller et specifikt specialbygget kontor. I de fleste tilfælde bruges det til at oprette forbindelse til et organisatorisk netværk såsom Virtual Private Network (VPN), der kun er dedikeret til en virksomhed. Som netværksadministrator vil du oprette adgang til et sådant netværk med Connection Manager for at give ham adgang til virksomhedens netværk fra et eksternt sted.

### Hvad er insdie CMS?

En CMS-profilfil oprettes ved hjælp af Connection Manager og pakkes med andre konfigurationsfiler, før den leveres til fjernbrugeren. Disse yderligere filer kan omfatte en CMP- og og en INF-fil, der er pakket sammen i en [EXE](/executable/exe/)-fil. Denne komplette pakke leveres til fjernbrugeren for at oprette forbindelse til netværket.

## Referencer

* [Forstå og konfigurere Windows Connection Manager](https://learn.microsoft.com/en-us/windows-hardware/drivers/mobilebroadband/understanding-and-configuring-windows-connection-manager)


