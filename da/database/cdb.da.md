{
  "date": "2021-06-16",
  "keywords": [
"CDB",
"udvidelse",
"cdb fil",
"cdb filformat",
"Database filtype",
"Database filformat",
"hvad er en cdb-fil"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om CDB-filformat og API'er, der kan oprette og åbne CDB-filer.",
  "title": "CDB - konstant databasefil",
  "linktitle": "CDB",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-cd-dab"
}
},
  "lastmod": "2021-06-16"
}

## Hvad er CDB fil?
CDB-filerne bruges i missionskritiske applikationer som e-mail. CDB står for konstant database, en hurtig, pålidelig og enkel pakke til at oprette eller læse konstante databaser. Databaseudskiftning er sikker mod systemnedbrud. Brugere behøver ikke at holde pause under en omskrivning. CDB fungerer som et associativt array (på-disk), der knytter nøgler til værdier og gør det muligt at lagre flere værdier i en enkelt nøgle.

## CDB filformat

CDB-filformatet gemmer tal, forskydninger, længder og hashværdier i lille endian-format som usignerede 32-bit heltal. Nøgler og data menes at være uigennemsigtige byte-strenge uden særlig behandling. I begyndelsen af databasen repræsenterer headeren med fast størrelse 256 hash-tabeller ved at angive deres position i filen og deres længde i slots. Normalt lagres dataene som en sekvens af poster, hver post gemmer nøglelængde, datalængde, nøgle og data. Der er ingen sortering eller justeringsregler. Posterne efterfølges af et sæt på 256 hashtabeller af varierende længde. Da nul er en gyldig længde, kan der være færre end 256 hash-tabeller fysisk gemt i databasen, men der er intet, der anses for at være 256 tabeller. Hash-tabeller består af en række slots, som hver indeholder en hashværdi og en postoffset. Tomme pladser har en offset på nul.

### Struktur af CDB-filformat

CDB-databasen består af et helt datasæt i en enkelt computerfil. Den indeholder tre dele:
- Et header i fast størrelse
- Data
- Et sæt hashtabeller.

Opslag er kun tilgængelige for nøjagtige nøgler. Opslag fungerer ved hjælp af følgende algoritme:

- Hash nøglen.
- Bestem ved hvilken hash-tabel og slot denne post skal placeres.
- Test det angivne slot i hash-tabellen.

For opslag af nøgler med mere end én værdi kan yderligere værdier findes ved blot at genoptage søgningen ved den næste plads.

#### Funktioner

CDB-databasestrukturen giver flere funktioner:

##### Hurtige opslag
Et vellykket opslag i en enorm database kræver normalt kun to diskadgange, og et mislykket opslag kræver kun én.
##### Lav overhead
En database bruger 2048 bytes, 24 bytes pr. post og plads til nøgler og data.
##### Ingen tilfældige grænser
CDB kan administrere enhver database på op til 4 gigabyte. Da der ikke er andre begrænsninger, behøver posterne ikke engang at passe ind i hukommelsen. Databaser gemmes i et maskinuafhængigt format.
##### Hurtig udskiftning af atomdatabase
Kommandoen **cdbmake** kan omskrive en hel database i to størrelsesordener, hurtigere end andre hashing-pakker.
##### Hurtige databasedumps
**cdbdump** kan udskrive indholdet af en database i cdbmake-kompatibelt format.


## Referencer ##

* [cdb (software) - Wikipedia](https://en.wikipedia.org/wiki/Cdb_(software))

* [CDB-specifikation](http://cr.yp.to/cdb.html)


