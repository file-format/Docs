{
  "date": "2020-11-11",
  "keywords": [
"ACCDT",
"udvidelse",
"fil",
"filformat",
"Database filtype",
"Database filformat",
"Database filer"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om ACCDT filformat og API'er, der kan oprette og åbne ACCDT filer.",
  "title": "ACCDT - Microsoft Access 2007 skabelondatabasefilformat",
  "linktitle": "ACCDT",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-accd-dat"
}
},
  "lastmod": "2020-11-12"
}

## Hvad er en ACCDT fil?

A file with .accdt extension is a Microsoft Access database template file that contains pre-defined database elements. These elements are a collection of structures that define a database applications such as database schemas for storing data, layout description for views of the data, and metadata describing the database. Being template files, ACCDT files can be used to create databases based on the template settings available in these. Resultant database files are saved as [ACCDB](/database/accdb/) files and populated with data in tables. Microsoft Access 2007 and onwards can open ACCDT files.

## ACCDT filformat

ACCDT-skabelonfiler er baseret på Office Open XML-specifikationerne, og alle data er indeholdt i en ZIP-pakke. Databasens struktur og indhold er indeholdt i [XML](/web/xml/)-filerne og tekstfilerne og linket til hinanden via relationer. Du kan omdøbe en ACCDT-fil til udvidelsen [.zip](/compression/zip/) og bruge enhver komprimeringssoftware til at udpakke indholdet af ZIP-arkivet.

### Filstruktur

ACCDT-filer er pakker, der indeholder en samling af relaterede dele. Hver **del** gemmer information om indholdet af en databaseapplikation ved hjælp af XML, tekst og binære formater, der inkluderer:

 * Database objekter
 * Tilknyttede metadata
 * Pakkens opbygning

#### Pakke

En pakke er et [ZIP](/compression/zip/)-arkiv, der indeholder flere dele og er i overensstemmelse med de åbne emballagekonventioner specificeret i [ISO/IEC-29500-2](https://www.iso.org/standard/51459.html). ACCDT-filer skal indeholde mindst én Template-metadaa-del, som skal være målet for en relation. Denne skabelon-metadata er startdelen af en ACCDT-fil.

#### En del

En del er en strøm af bytes, der har en tilknyttet type til at specificere arten og typen af indhold, der er gemt i den. Opregning af dele angiver gyldige dele, gyldige indholdstyper og påkrævede relationer mellem alle dele i en pakke.

#### Forhold

`Package Relationship` - hvor målet er en del, og kilden er pakken som helhed.

`Part-to-Part Relationship` - hvor målet er en del, og kilden er en del i pakken.

Eksplicit relation - hvor der refereres til en ressource fra indholdet af en kildedel ved at henvise til et relationselement med værdien af dets ID-attribut.

`Implicit relation` - et forhold, der ikke er eksplicit.

`Intern relation` - hvor målet er en del af pakken.

`Ekstern relation` - hvor målet er en ekstern ressource, der ikke er i pakken.

## Referencer ##

* [Access Template File Format](https://learn.microsoft.com/en-us/openspecs/sharepoint_protocols/ms-accdt/0a4a68d7-7a85-4a27-ad74-730db57862d7)

