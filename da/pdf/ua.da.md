{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PDF/UA filformat",
  "description": "Lær om PDF/UA-filformat og API'er, der kan oprette og åbne PDF/UA-filer.",
  "linktitle": "PDF/UA",
  "menu": {
    "docs": {
      "parent": "pdf",
      "identifier": "pdf-u-daa"
}
},
  "lastmod": "2019-09-10"
}

# Hvad er PDF/UA-fil? #

PDF/UA blev udgivet som [ISO Standard 14289-1](https://en.wikipedia.org/wiki/ISO_14289) i august 2012 og er langt den første komplette definition af et sæt krav til universelt tilgængelige PDF-dokumenter. Udtrykket universelt tilgængelig refererer til forståelsen af, at oplysningerne i et [PDF](/pdf/)-dokument skal være lige og uafhængigt tilgængelige for alle i almindelighed og for mennesker med handicap i særdeleshed. Introduktion af PDF/UA-standarden kan betragtes som et vigtigt skridt for at skabe værktøjer og applikationer for at skabe og læse PDF-indhold.

## Filformatkrav ##

PDF'en/UA'en har nogle klare krav i sin base, der fungerer som essensen af denne standard. Grundlæggende er disse baseret på tagging af PDF'er, hvilket betyder, at alle PDF/UA-dokumenter skal være korrekt tagget. Det kræver også, at tags er semantisk passende og i logisk rækkefølge. Dette sikrer, at slutdokumentet, der er oprettet med PDF/UA-specifikationer, er mere pålideligt og tilgængeligt. Dette kan få PDF-forfattere til at stille spørgsmålstegn ved, om de har brug for at vide alt om alle sådanne krav? Heldigvis er det ikke sådan, da PDF/UA-overensstemmelsesværktøjerne tager ansvaret for at tilføje og bevare PDF'ens tilgængelighed.

Filformatkravene til PDF/UA er som følger.

* Indhold er kategoriseret på en af to måder: meningsfuldt indhold og artefakter såsom dekorative sideelementer. Alt meningsfuldt indhold skal tagges og integreres i strukturtræet for alle tags i et dokument. Artefakter skal derimod kun markeres som sådan.

* Meningsfuldt indhold skal markeres med tags og sammen med de øvrige tags i dokumentet skabe et komplet strukturtræ.

* Meningsfuldt indhold skal markeres med de relevante semantiske tags.

* Strukturtræet skabt af dokumentmærkerne skal afspejle dokumentets logiske læserækkefølge.

* Kun standardmærkerne defineret i PDF 1.7 må bruges; hvis der bruges andre tags, skal en rolletildelingspost registrere, hvilket standard tag hver repræsenterer.

* Information må ikke formidles ved hjælp af visuelle midler alene (f.eks. kontrast, farve eller position på siden).

* Intet flimrende, blinkende eller blinkende indhold er tilladt, hverken som effekter kontrolleret af JavaScript eller som en del af nogen videoer, der er indlejret i PDF'en.

* Der skal angives en dokumenttitel, og dokumentet skal sættes op, så titlen (frem for filnavnet) vises i vinduets titel.

* Sproget i alt indhold skal noteres, og sprogændringer skal udtrykkeligt markeres som sådan.


## PDF/UA-overensstemmelse ##

PDF/UA-standarden definerer specifikationer for indhold, læsere og hjælpeteknologi. Disse tre aspekter er forbundet med hinanden baseret på indholdet af dokumentet. Overensstemmelseskravene for hver af disse er som nævnt nedenfor.

## Overensstemmende filer ##

Files conforming to PDF/UA standard should contain features that are valid as per the [PDF 1.7 specifications](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf). However, features that are forbidden by PDF/UA specifically should be excluded.

## Overensstemmende læsere ##

En konform læser skal overholde reglerne i PDF 1.7-specifikationerne. Specifikt skal det understøtte:

* alle tags, attributter og nøgleværdier angivet for tilgængelighed. Det skal også have evnen til at behandle og repræsentere digitale signaturer, annoteringer og valgfrit indhold.

* behandle og repræsentere digitale signaturer, annoteringer og valgfrit indhold

* Naviger i dokumentet på en række forskellige måder


## Overensstemmende hjælpeteknologi ##

En passende hjælpeteknologi er bundet til at understøtte PDF/UA-funktionerne. Disse omfatter f.eks. funktioner i indholdet og læseren og bør tillade navigation efter sideetiketter, dokumentstruktur eller omrids. Det bør også lade brugeren tilsidesætte standard navigationszoom.

## Referencer ##

* [PDF/UA - Af Wikipedia](https://en.wikipedia.org/wiki/PDF/UA)

* [PDF/UA i en nøddeskal](https://pdfa.org/pdfua-in-a-nutshell/)


