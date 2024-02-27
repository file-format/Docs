{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "STR-fil - dBASE Structure List Object File - Hvad er .str-fil, og hvordan åbner man den?",
  "description" : "Lær om STR dBASE Structure List Object File og hvordan du åbner den.",
  "linktitle" : "STR",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-str-da",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## Hvad er STR fil?

STR-filformat er almindeligvis forbundet med dBASE, et databasestyringssystem. I dBASE repræsenterer en .str-fil typisk en strukturlisteobjektfil. Denne fil indeholder strukturen af en databasetabel, inklusive information om felter (kolonner) og deres egenskaber.

Strukturlisteobjektfilen (.str) indeholder metadata såsom feltnavne, datatyper, feltlængder og andre egenskaber, der er knyttet til hvert felt i databasetabellen. Det bruges til at definere strukturen af databasetabellen uden at indeholde faktiske dataposter.

Programmer som dBASE eller andre databasestyringsværktøjer kan bruge denne fil til at forstå layoutet af databasetabellen og udføre operationer såsom forespørgsel, opdatering eller oprettelse af nye poster baseret på denne struktur.

Her er et grundlæggende eksempel på, hvad en STR-fil kan indeholde:

```
Field Name    Type      Length
-----------   ------    ------
ID            Numeric   5
Name          Character 30
Age           Numeric   3
DOB           Date
```

Dette eksempel beskriver en tabel med fire felter: ID, Navn, Alder og DOB sammen med deres respektive datatyper og længder.

## Hvordan åbner jeg filen STR?

Den primære måde at åbne .str-filer på er ved at bruge selve dBASE, især på Windows-operativsystemer. dBASE er i stand til at læse og fortolke indholdet af disse filer, hvilket giver brugerne mulighed for at se og arbejde med databasestruktur.

Da .str-filer i det væsentlige er almindelige tekstfiler, der indeholder information om databasens struktur, kan du også åbne dem ved hjælp af en teksteditor. Eksempler på teksteditorer omfatter Microsoft Notesblok på Windows og Apple TextEdit på Mac. Når den åbnes i en teksteditor, vil du være i stand til at se indholdet af filen, inklusive feltnavne, datatyper og anden strukturel information, i et menneskeligt læsbart format.

## Referencer
* [dBase](https://en.wikipedia.org/wiki/DBase)


