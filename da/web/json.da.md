---
date: 2019-10-11
keywords: json, .json, json file format, how to open json files, javascript object notation, json data format, .json file format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JSON-filformat - Hvad er en JSON-file?
linktitle: JSON
description: Ltjene om JSON-filformat og API'er, der kan oprette og åbne JSON-fils.
menu:
  docs:
    parent: "web"
lastmod: 2020-04-12
---

## Hvad er en JSON fil?

JSON (JavaScript Object Notation) er et åbent standard filformat til deling af data, der bruger menneskelig læsbar tekst til at gemme og overføre data. JSON-filer gemmes med filtypenavnet .json. JSON kræver mindre formatering og er et godt alternativ til [XML](/web/xml/). JSON er afledt af JavaScript, men er et sproguafhængigt dataformat. Generering og parsing af JSON understøttes af mange moderne programmeringssprog. *application/json* er den medietype, der bruges til JSON.

## JSON-filformat - kort historie

There was a need for real-time server to client communication that lead to the creation of JSON. The JSON format was first specified by Douglas Crockford in March 2001. JSON var baseret på Standard ECMA-262 3rd Edition—december 1999, som er en delmængde af JavaScript.

The first edition of JSON standard ECMA-404 was published in October 2013 by Ecma International. RFC 7159 became the main reference for JSON's Internet uses in 2014. I november 2017 blev ISO/IEC 21778:2017 udgivet som en international standard. RFC 8259 blev offentliggjort den 13. december 2017 af The Internet Engineering Task Force, som er den aktuelle version af Internet Standard STD 90.

## JSON filstruktur

JSON-data er skrevet i **nøgle/værdi**-par. Nøglen og værdien er adskilt af et kolon(:) i midten med tasten til venstre og værdien til højre. Forskellige nøgle/værdi-par er adskilt af et komma(,). Nøglen er en streng omgivet af dobbelte anførselstegn for eksempel navn. Værdierne kan være af følgende typer.

- `Nummer`
- `String`: Rækkefølge af Unicode-tegn omgivet af dobbelte anførselstegn.
- 'Boolesk': Sandt eller falsk.
- `Array`: En liste over værdier omgivet af firkantede parenteser, for eksempel

``` json
[ Æble, Banan, Orange ]
```

- `Objekt`: En samling nøgle/værdi-par omgivet af krøllede seler, for eksempel

``` json
{name: Jack, age: 30, favoriteSport : Fodbold}
```

JSON-objekter kan også indlejres for at repræsentere strukturen af dataene. Nedenstående er et eksempel på et JSON-objekt.

### Eksempel på JSON-format

```json
{
   "name":"Jack",
   "age":30,
   "contactNumbers":[
      {
         "type":"Home",
         "number":"123 123-123"
      },
      {
         "type":"Office",
         "number":"321 321-321"
      }
   ],
   "spouse":null,
   "favoriteSports":[
      "Football",
      "Cricket"
   ]
}
```

## Hvad er den maksimale størrelse på JSON-filen?

Der er praktisk talt ingen grænse for den maksimale størrelse af en JSON-fil. Den kan være lige så lang som den plads, der kræves af indholdet, der skal opbevares.

Når det kommer til at bruge JSON-filformat til overførsel af data over internettet, skal man være forsigtig med de tilgængelige ressourcer på computeren. Hvis store JSON-data overføres, vil overførslen blive påvirket, hvis klientbrowseren har begrænset hukommelse.


Der er ingen hård grænse defineret af specifikationen, men du skal være forsigtig med ikke at udtømme ressourcer på dine brugeres computere, da det hurtigt vil forringe deres brugeroplevelse, og de vil sandsynligvis forlade din app.

## JSON vs XML

**XML** er et andet almindeligt og meget brugt filformat til udveksling af data over internettet. Når det kommer til udveksling af data mellem applikationer, har udviklere mulighed for at bruge både XML- og JSON-filformater. JSON er dog vedtaget som den mest bekvemme måde til dataudveksling mellem applikationer over internettet på grund af følgende årsager.

 1. JSON giver en klar og lettere at læse visning af data sammenlignet med XML-filformater
 1. JSON reducerer omkostningerne ved dataoverførsel over internettet, da det har færre antal tegn til at definere det samme datasæt sammenlignet med XML
 1. Moderne programmeringssprog giver indbyggede parsere til at parse JSON-svaret over nettet.

## Ofte stillede spørgsmål

 * **Hvad bruges JSON-filen til?** JSON-filformatet kan bruges som et mellemfilformat til lagring af datagenererede data, f.eks. fra en indsendt formular på et websted. Det bruges også som en dataformatfil til ethvert programmeringssprog og giver interoperabilitet mellem forskellige typer data.
 * **Er JSON- og XML-filen den samme?** Ikke rigtig. JSON adskiller sig fra XML ved, at JSON er kortere, kan læses og rettes hurtigt, kan bruge arrays, og den bruger ikke sluttag.
 * **Can I convert JSON to CSV?** Yes, there are certain online converter apps such as **GroupDocs Conversion apps** that can [convert JSON to CSV](https://products.groupdocs.app/conversion/json-to-csv).
 * **Hvordan konverteres JSON til PDF?** Du kan bruge online-apps såsom Asopse.app for Cells til at [konvertere JSON-fil til PDF](https://products.aspose.app/cells/conversion/json-to- pdf).
 * **Hvordan åbner man en JSON-fil i Word?** Du kan bruge online-apps såsom Aspose.app for Words til [konverter JSON-fil til Word](Konverter JSON-format til WORD i Android via Java).

## Vidste du?

You can become a contributor at FileFormat.com to keep the file format community up to date with your findings. If you have to share anything about JSON or Web file formats, you can post your findings in [Web File Format News](https://news.fileformat.com/t/Web) section for people to learn more form these.

## Referencer

- [JSON - Wikipedia](https://en.wikipedia.org/wiki/CSS)
- [An Introduction to JSON](https://www.digitalocean.com/community/tutorials/an-introduction-to-json)

