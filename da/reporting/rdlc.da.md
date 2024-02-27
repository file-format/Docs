{
  "date": "2021-03-02",
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "RDLC - Report Definition Language Client-side",
  "keywords": [
"rdlc",
"rapportdefinitionssprog",
"mkv format",
"XSD",
"rapport definition sprog klient side"
],
  "description": "Lær om RDLC-filformat, som er en XML-repræsentation af en SQL Server Reporting Services-rapportdefinition.",
  "linktitle": "RDLC",
  "menu": {
    "docs": {
      "parent": "reporting",
      "identifier": "reporting-rdl-dac"
}
},
  "lastmod": "2021-03-02"
}

## Hvad er en RDLC fil? ##

RDLC står for Report Definition Language Client side. Faktisk er det en udvidelse af rapportfilen oprettet ved hjælp af Microsofts rapporteringsteknologi. SQL Server 2005-versionen af Report Designer bruges til at oprette disse filer. **ReportViewer**-kontrollen på klientsiden kan udføre RDLC-rapporterne direkte.

## RDL VS RDLC filer
|.rdl-filer |.rdlc-filer|
---|---|
|RDL-filer er oprettet af SQL Server 2005-versionen af Report Designer|RDLC-filer er oprettet af Visual Studio 2005-versionen af Report Designer|
|Det bruges i SQL Server Reporting Services|Det bruges i Visual Studio|
|Det er en fjernrapport|Det er en lokal rapport|
|Har brug for en Reporting Services-instans for at køre den|Ingen behov for en Reporting Services-instans|

## Oprettelse af klientrapportdefinitionsfiler (.rdlc).
ReportViewer-kontrolelementet bruges til at køre klientrapportdefinitionsfiler (.rdlc) ved hjælp af kontrolelementets indbyggede behandlingsfunktion. Klienten rapporterer, at du kører i lokal behandlingstilstand, kan nemt oprettes i dit applikationsprojekt. Følgende er fremgangsmåderne til oprettelse af rapporten:

- Brug **Report Wizard** til at oprette en ny klientrapportdefinition (.rdlc).

- Opret en ny klientrapportdefinitionsfil (.rdlc) ved at bruge Visual Studio.

- Generer en rapportdefinition programmatisk.


Du kan kun få vist en rapport ved at køre den i en **ReportViewer** kontrol. Bemærk venligst, at du til enhver tid kan åbne og redigere rapportdefinitionen og derefter bygge eller implementere applikationen for at kontrollere resultaterne.

## Referencer ##

- [Creating Client Report Definition (.rdlc) Files](https://learn.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-2010/ms252067(v=vs.100))

