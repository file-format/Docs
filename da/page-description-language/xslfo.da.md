{
  "date": "2019-10-11",
  "keywords": [
"XSLFO",
"XSL-formatering af objekter",
"Fil",
"Udvidelse",
"Filformat",
"Udvidbart stylesheet-sprog"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XSLFO",
  "description": "Lær om XSLFO-filformat og API'er, der kan oprette og åbne XSLFO-filer.",
  "linktitle": "XSLFO",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-xslf-dao"
}
},
  "lastmod": "2021-04-23"
}

## Hvad er en XSL-FO fil? ##

XSL-FO (XSL Formatting Objects) er et kraftfuldt stylesheet-sprog til formatering af XML-dokumenter. Semantikken i den afgrænsede form af papir og tryk er udtrykt ved XSL-FO, når dimensionerne er faste. I modsætning til HTML, som repræsenterer semantikken i den ubegrænsede form af et browservindue med variable dimensioner. XML-dokumenterne formateret af XSL-FO bruges mest til at generere PDF-filer. XSL (Extensible Stylesheet Language) er et sæt funktionskomplette W3C-teknologier beregnet til at designe til formatering og udveksling af XML-dokumenter og XSL-FO-delen af dette sprog. XSLT og XPath er også andre dele af XSL.

Det foreslås, at XML-dokumenter først skal transformeres til XSL-FO, PDF er et eksempel på dette kriterium. I PDF gengives resultater ved hjælp af XSLTfirst og derefter XSL-FO-formatering. På denne måde kan XML-dokumenter formateres tilfældigt. Selvom XSL-FO udnytter fordelen ved at bruge Cascading Style Sheet-egenskaber (CSS) og udvide dem, hvor det er nødvendigt for det rigtige format, huser det leveringen af sideskabeloner kaldet sidemastere i XSL-FO's terminologi. XSL-FO giver også formatering til ret sofistikerede dokumenter og understøtter indeksgenerering.

## Historie og grundlæggende begreber ##

I januar 2012 blev arbejdsudkastet til XSL-FO opdateret sidste gang, og i november 2013 var dets arbejdsgruppe blevet lukket. Et XSL-typografiark specificerer præsentationen af en klasse af XML-dokumenter ved at beskrive, hvordan en forekomst af klassen transformeres til et XML-dokument, der bruger formateringsordforrådet. XSL-FO er et integreret præsentationssprog og har ingen semantiske markeringer, som bruges i HTML. Desuden gemmer dette sprog alle dokumentets data i sig selv, i modsætning til CSS, som ændrer standardindstillingerne for et eksternt HTML- eller XML-dokument.

De generelle kriterier for at bruge XSL-FO er, at brugeren skriver et dokument i et XML-sprog i stedet for at skrive i FO. Derefter sker en XSLT-transformation. Denne XSLT-transformation er ansvarlig for konverteringen af XML til XSL-FO. Så snart XSL-FO-dokumentet er genereret, overdrages det til en applikation kaldet en FO-processor. FO-behandlere er ansvarlige for at omdanne dette dokument til et læsbart såvel som et printbart dokument. PDF-filer eller PS er eksempler på de mest almindelige output af XSL-FO. Men det betyder ikke, at FO-processor kun kan producere disse to typer formater som output. Nogle FO-processorer kan udlæse i RTF-filerne eller endda et vindue kan dukke op i brugerens GUI, dette vindue viser sidens sekvens og deres indhold.

Et XSL-FO-dokument er forskelligt fra en PDF eller en PS i den forstand, at det i sidste ende ikke definerer tekstlayoutet på forskellige sider. Måske styles siderne og bestemmer steder for at vise indholdet. Desuden organiserer en FO-behandler teksten inden for de grænser, der er angivet af FO-dokumentet. Denne specifikation tillader endda forskellige FO-processorer at opføre sig i overensstemmelse med de resulterende oprettede sider. Et eksempel på sådan adfærd er orddeling, få FO-processorer kan orddele ord for at spare plads, når et linjeskift, mens nogle processorer ikke vælger denne mulighed. Det afhænger af processorerne at vælge forskellige orddelingsalgoritmer, der matcher deres krav. Disse orddelingsalgoritmer kan være meget enkle eller måske mere komplekse. I nogle situationer sanktionerer XSL-FO-specifikationen eksplicit FO-processorer, en vis grad af valg i sammenhæng med layoutet.

Denne variation blandt FO-processorer genererer forskellige resultater, som processorer ofte forbliver ligeglade med. Fordi det generelle fokus for XSL-FO er at producere side-/printede dokumenter. XSL-FO-dokumenter fungerer typisk selv som mellemled, deres hovedfunktion er at generere enten PDF-filer eller et dokument, der kan udskrives som output, der skal distribueres. I HTML/CSS eller XSL-FO indikerer distribuering af PDF'en som slutresultat i stedet for at indtaste formateringssproget, at modtagere forbliver upåvirket af den resulterende alsidighed, som frembringes på grund af forskelle mellem fortolkere af formateringssprog. På den anden side er det tydeligt, at der ikke er nogen nem måde, at et dokument kan opfylde modtagernes forskellige behov, f.eks. variabel sidestørrelse eller ønsket skriftstørrelse, eller skræddersy til side eller print.

## XSLFO-filformat ##

SL-FO-dokumenter er grundlæggende XML-dokumenter, men de følger ikke noget skema. I stedet følger SL-FO-dokumenter den syntaks, der er defineret i specifikationen for deres eget sprog. Der er to sektioner påkrævet i hvert XSL-FO-dokument:

1. En sektion, der specificerer en liste over mærkede sidelayouts.
1. En sektion med alle detaljer om dokumentdata, med markering, der bestemmer visningen af indhold på forskellige sider gennem forskellige sidelayouts.

Sidens egenskaber er nævnt i sidelayouterne, som kan definere organiseringen af teksten, for at overholde konventionerne for det specifikke sprog. Desuden er størrelsen på siden, deres marginer og sidesekvenser (der sanktionerer forskellige egenskaber for de ulige og lige sider) også defineret af sidelayouterne.

Datadelen af dokumentet er opdelt i en række flows, hvor hvert flow er forbundet med et sidelayout. Strømmene omslutter en liste over blokke i dem. Denne liste over blokke kan indeholde inline markup-funktioner eller en liste over tekstdata, eller måske begge dele på samme tid. Dokumentets marginer kan også vise sidetal eller kapiteloverskrifter. Funktionaliteten af både blokke og inline-elementer forbliver den samme som i CSS, men nogle polstrings- og marginregler er forskellige mellem FO og CSS.

The page orientation direction is entirely specified for the extension of blocks and inlines, thus making FO documents perform under the languages different from English. The language of the FO specification uses the words start and end rather than left and right for directions description. XSL-FO's basic content markup and cascading rules are taken from CSS. XSL-FO's language agrees to the following specifications.

## Flere kolonner ##

En side kan have flere kolonner og blokke og kan som standard strække sig fra en kolonne til en anden. Flere sider må have forskellige bredder og antal kolonner. Alle FO-karakteristika følger grænserne for en side med flere kolonner.

### Lister ###

En XSL-FO-liste er etableret af to sæt blokke arrangeret kind for kæbe. Begrebsmæssigt angiver en blok til venstre på en liste et tal, et punkttegn eller en tekststreng, mens højre blok kan fungere som forventet. Nummereringen af XSL-FO lister udføres normalt af XSLT.

### Tabeller ###

En FO-tabel ligner en HTML/CSS-tabel. Brugeren kan vælge rækker af data, stilinformation, baggrundsfarve for hver enkelt celle. Ved at bruge forskellige stiloplysninger har brugeren privilegiet til at vælge den første række som en tabeloverskriftsrække. FO-processoren kan informeres eksplicit om pladsspecifikationen for hver kolonne eller automatisk tilpasse teksten i tabellen.

### Indeksering ###

XSL-FO 1.1 har funktioner, der hjælper med at generere et indeks ved at henvise til korrekt markerede elementer.

### Fordele ###

* Velegnet til indholdsbaseret udgivelse

* Brugervenlighed

* Lavpris


## Referencer ##

* [Hvad er XSL-FO?](https://www.xml.com/articles/2017/01/01/what-is-xsl-fo/)

* [XSL-formateringsobjekter](https://en.wikipedia.org/wiki/XSL_Formatting_Objects)


