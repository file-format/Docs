{
  "date": "2023-03-22",
  "keywords": [
"cnf fil",
"hvad er en cnf-fil",
"hvordan man åbner cnf fil",
"fil",
"cnf filtypenavn",
"udvidelse"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "CNF-filformat - MySQL-konfigurationsfil",
  "description": "Lær om CNF-format og API'er, der kan oprette og åbne CNF-filer.",
  "linktitle": "CNF",
  "menu": {
    "docs": {
      "identifier": "settings-cnf-da",
      "parent": "settings"
}
},
  "lastmod": "2023-03-22"
}

## Hvad er CNF fil?

En CNF-fil (også kendt som en konfigurationsfil) i MySQL bruges til at gemme konfigurationsindstillinger for MySQL-serveren. Placeringen af CNF-filen kan variere afhængigt af operativsystemet og den anvendte installationsmetode. Konfigurationen inkluderer typisk forskellige indstillinger som standardtegnkodning, timeouts, cache- og bufferkonfigurationer, som kan justeres for at optimere databasens ydeevne baseret på brug.

## CNF-filformat – flere oplysninger

Du kan oprette CNF ved at bruge følgende trin i MySQL:

1. Åbn en teksteditor, f.eks. Notesblok, og opret en ny fil.
2. Tilføj de ønskede konfigurationsmuligheder til filen, én pr. linje. Her er et eksempel:

```
[mysqld]
datadir=/var/lib/mysql
socket=/var/lib/mysql/mysql.sock
user=mysql
symbolic-links=0

[client]
user=root
password=password123
```

3. Gem filen med filtypenavnet .cnf, for eksempel mysql.cnf.
4. Flyt filen til den relevante mappe. For eksempel på Linux-systemer kan mappen være /etc/mysql/conf.d/ eller /etc/mysql/.
5. Genstart MySQL-serveren for at de nye konfigurationsindstillinger træder i kraft.

Sørg for at teste eventuelle ændringer i CNF-filen i et ikke-produktionsmiljø, før du implementerer dem i et produktionsmiljø.

## Hvordan åbner jeg filen CNF?

CNF-fil er en tekstfil og kan nemt åbnes ved hjælp af enhver teksteditor som Notesblok. Du kan også åbne den ved at højreklikke og vælge Åbn med fra menuen. Når filen er åben, kan du redigere konfigurationsindstillingerne efter behov. CNF indeholder forskellige indstillinger relateret til MySQL-server, f.eks. portnummer, logningsmuligheder og bufferstørrelser. Når du har redigeret indstillingerne, skal du gemme ændringerne og lukke teksteditoren. Genstart endelig MySQL-serveren for at ændringerne træder i kraft.

Bemærk, at det er vigtigt at være forsigtig, når du redigerer MySQL-konfigurationsfilen, da forkerte indstillinger kan få serveren til at opføre sig uforudsigeligt eller slet ikke starte. Det anbefales at lave en sikkerhedskopi af den originale fil, før du foretager ændringer, så du kan gendanne den, hvis det er nødvendigt.

## Referencer
* [MySQL](https://en.wikipedia.org/wiki/MySQL)


