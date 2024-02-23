{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "STR-fil - dBASE Structure List Object File - Vad är .str-fil och hur öppnar man den?",
  "description" : "Lär dig mer om STR dBASE Structure List Object File och hur du öppnar den.",
  "linktitle" : "STR",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-str-sv",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## Vad är STR fil?

STR-filformat är vanligtvis associerat med dBASE, ett databashanteringssystem. I dBASE representerar en .str-fil vanligtvis en strukturlistobjektfil. Denna fil innehåller strukturen för en databastabell, inklusive information om fält (kolumner) och deras egenskaper.

Strukturlistobjektfilen (.str) innehåller metadata som fältnamn, datatyper, fältlängder och alla andra egenskaper som är associerade med varje fält i databastabellen. Den används för att definiera strukturen för databastabellen utan att innehålla faktiska dataposter.

Program som dBASE eller andra databashanteringsverktyg kan använda den här filen för att förstå layouten av databastabellen och utföra operationer som att fråga, uppdatera eller skapa nya poster baserat på denna struktur.

Här är ett grundläggande exempel på vad en STR-fil kan innehålla:

```
Field Name    Type      Length
-----------   ------    ------
ID            Numeric   5
Name          Character 30
Age           Numeric   3
DOB           Date
```

Det här exemplet beskriver en tabell med fyra fält: ID, Namn, Ålder och DOB, tillsammans med deras respektive datatyper och längder.

## Hur öppnar man filen STR?

Det primära sättet att öppna .str-filer är att använda dBASE själv, särskilt på Windows-operativsystem. dBASE kan läsa och tolka innehållet i dessa filer, vilket gör det möjligt för användare att se och arbeta med databasstruktur.

Eftersom .str-filer i huvudsak är vanliga textfiler som innehåller information om databasens struktur, kan du också öppna dem med en textredigerare. Exempel på textredigerare inkluderar Microsoft Notepad på Windows och Apple TextEdit på Mac. När den öppnas i en textredigerare kommer du att kunna se innehållet i filen, inklusive fältnamn, datatyper och annan strukturell information, i ett läsbart format.

## Referenser
* [dBase](https://en.wikipedia.org/wiki/DBase)


