{
  "date": "2019-12-10",
  "keywords": [
"XLSB",
"fil",
"udvidelse",
"filformat",
"Excel binær regnearksfil"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Din filformatguide for at vide, hvad en XLSB-fil og API'er er, der kan oprette og åbne dem.",
  "title": "Hvad er en XLSB fil?",
  "linktitle": "XLSB",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-xls-dab"
}
},
  "lastmod": "2019-12-10"
}

## Hvad er en XLSB fil?

XLSB-filformatet specificerer det binære Excel-filformat, som er en samling af poster og strukturer, der specificerer Excel-projektmappeindhold. Indholdet kan omfatte ustrukturerede eller semistrukturerede tabeller med tal, tekst eller både tal og tekst, formler, eksterne dataforbindelser, diagrammer og billeder. I modsætning til [XLSX](/spreadsheet/xlsx/) (som er baseret på Open XML-filformat), repræsenterer XLSB en binær Excel-projektmappefil. XLSB-filer kan læses og skrives til hurtigere, hvilket gør dem nyttige til at arbejde med store filer. XLSB bruges sjældent til at gemme projektmapper, da XLSX (og tidligere [XLS](/spreadsheet/xls/)) er de mest almindelige brugervalgte filformater til at gemme projektmapper. Det kan åbnes af Microsoft Office 2007 og nyere.

## XLSB-filformatspecifikationer ##

The file format specifications for XLSB file format were made public back in 2008 as version 1.0. Siden da er specifikationerne blevet revideret adskillige gange, og den seneste version af specifikationerne (v 10.0) blev offentliggjort i april 2018. Specifikationerne er offentligt tilgængelige af Microsoft som [[MS-XLSB] - Excel Binary File Format specifications](https://msdn.microsoft.com/en-us/library/cc313133(v#office.12).aspx) og bør konsulteres af enhver for at læse eller skrive filer i XLSB-filformat.

## XLSB filstruktur ##

En XLSB-fil er en pakke, der består af en samling af dele. Disse dele indeholder oplysninger om indholdet af en projektmappe, herunder projektmappedata og pakkens struktur. Nogle dele indeholder information, der er gemt ved hjælp af binære poster, nogle som XML, mens andre indeholder information, der er gemt som en binær strøm af bytes. Hver binær post indeholder nul eller flere strukturerede felter, der indeholder projektmappedataene.

#### Pakke ####

En XLSB-pakke er et [ZIP](/compression/zip/)-arkiv, der skal indeholde præcis én projektmappedel. Denne del skal være målet for en relation i denne pakkerelationsdel. Projektmappedelen er startdelen i XLSB-dokumentet.

#### En del ####

En del er en strøm af bytes, der har en tilknyttet indholdstype, som specificerer arten og typen af indhold, der er gemt i delen. Nogle dele gemmer information i binært format, mens andre gemmer information som XML. Sektionen [parts enumeration](https://msdn.microsoft.com/en-us/library/dd924091(v#office.12).aspx) i specifikationsdokumentet viser de gyldige dele, indholdstyper og påkrævede/valgfrie relationer mellem alle dele i en pakke.

#### Forhold ####

En kilde og en målressource er forbundet med en relation. Et forhold kan være:

**Pakkeforhold:** hvor målet er en del, og kilden er pakken som helhed

**Del-til-del-forhold:** hvor målet er en del, og kilden er en del af pakken

**Eksplicit relation:** hvor der refereres til en ressource fra indholdet af en kildedel ved at henvise til ID-attributværdien for et relationselement

**implicit forhold** er et forhold, der ikke er eksplicit

**Internt forhold:** hvor målet er en del af pakken

**Eksternt forhold:** hvor målet er en ekstern ressource, der ikke er i pakken

#### Optag ####

En post er den grundlæggende byggeklods, der bruges til at gemme oplysninger om funktioner i en projektmappe. Hver binær post er en sekvens af bytes med variabel længde. En binær post består af tre komponenter:

* en rekordtype

* en rekordstørrelse, og

* de registreringsdata, der er specifikke for den pågældende posttype.


**Record Type:** Record-typen viser den type post, der er angivet af posten. Den specificerer også strukturen af postdata, der er specifikke for denne post. De gyldige posttyper er angivet i afsnittet [Record Enumeration](https://msdn.microsoft.com/en-us/library/dd953057(v#office.12).aspx) i specifikationsdokumentet. Posttypen skal være en eller to bytes og skal være større end eller lig med 128 og mindre end 16384.

**Record Size:** Poststørrelsen angiver antallet af bytes, der specificerer den samlede størrelse af postdataene. Denne værdi SKAL være en til fire bytes. Denne værdi SKAL være én byte, hvis den høje bit i den lave byte er lig med 0; ellers SKAL denne værdi være større end én byte. Hvis antallet af bytes er større end én byte, angiver den høje bit i hver efterfølgende byte, om der bruges en ekstra byte. Hvis den høje bit af den anden byte er lig med 1, SKAL denne værdi bruge en ekstra tredje byte. Hvis den høje bit af den tredje byte er lig med 1, SKAL denne værdi bruge en yderligere fjerde byte. Den høje bit af den fjerde byte SKAL ignoreres. Værdien består af de syv lave bits af hver byte kombineret. De lave, mindst signifikante bits er indeholdt i den første byte, og hver efterfølgende byte indeholder bits af højere orden end den foregående byte.

**Record Data:** Record data-komponenten indeholder felter, der svarer til en bestemt posttype og omfatter resten af posten. Rækkefølgen og strukturen af felterne for en given posttype, der er angivet i Record Enumeration, er angivet i det tilsvarende afsnit for den posttype i Records. Den samlede størrelse af postdatakomponenten SKAL være lig med poststørrelsen. Felter i postdatakomponenten kan indeholde simple værdier, arrays af værdier, strukturer af flere felter, arrays af felter og arrays af strukturer.

#### XLSB Record Eksempel ####

Følgende posttype og poststørrelse angiver en **BrtCommentText**-post med en størrelse på 200 bytes:

11111101 00000100 11001000 00000001 [Record Fields]

The first byte is 11111101, specifying a low value of 125 and that the record type requires a second byte. The second byte is 00000100, specifying a high value of 4 * 128, hvilket er lig med 512. Værdien af posttype er 125 + 512, eller 637, hvilket svarer til en **BrtCommentText** posttype. Den næste byte er 11001000, der angiver en lav værdi på 72, og at poststørrelsen kræver en anden byte. Den anden byte er 00000001, der angiver en højere værdi på 1 * 128, og at poststørrelsen ikke kræver en ekstra byte. Poststørrelsen er 72 + 128 eller 200, som angiver den samlede størrelse, i bytes, af postdatakomponenten. Felterne i postdatakomponenten er specificeret af **BrtCommentText**.

## Referencer ##

* [[MS-XLSB] - Excel (.xlsb) binært filformat](https://msdn.microsoft.com/en-us/library/cc313133(v#office.12).aspx)


