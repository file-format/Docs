{
  "date": "2021-07-25",
  "keywords": [
"mand",
"fil",
"udvidelse",
"type",
"format",
"Unix manual"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MAN - Unix Manual",
  "description": "Lær om FODT filformat og API'er, der kan oprette og åbne MAN filer.",
  "linktitle": "MAN",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-ma-dan"
}
},
  "lastmod": "2021-07-25"
}

## Hvad er MAN fil?

En fil med filtypenavnet .man står for man page, som er en Unix-programmeringsbrugermanual i softwaredokumentationsform. Det bruges af 'Man'-værktøjet, inkluderet i Unix, som bruges til at se dokumentationen. Softwaredokumentationen indeholder oplysninger i sektioner og sider, der kan hentes ved hjælp af Man-værktøjet fra kommandoterminalen ved at udstede kommandoer. Da den er tilgængelig på computeren som blød kopi af dokumentation, kræver den ikke nogen udskrevet kopi eller internetforbindelse for at få adgang til den.

## Unix Manual Man-filformat - flere oplysninger

Man-sider gemmes i almindeligt tekstformat og kan oprettes og åbnes i enhver teksteditor til visning eller redigering. I UNIX hentes information fra man-siderne ved at udstede kommandoer fra terminal, der inkluderer reference til afsnit og sidenumre fra manualen.

### Afsnit og sider

Unix man er systemets manual, hvor hvert sideargument til kommandoen refererer til navnet på et program, et hjælpeprogram eller en funktion. kommandoen, hvis den leveres med sektionsoplysninger, vil søge efter siden i den specifikke sektion. Standardadfærden er dog at søge efter siden i alle sektioner og vise den første side, uanset om den findes i flere sektioner.

### Afsnitsnumre

Følgende er oplysningerne om afsnitsnumrene i manualen efterfulgt af de typer sider, de indeholder.

|Sektionsnummer|Sidetype|
---|---|
|1|Eksekverbare programmer eller shell-kommandoer|
|2|Systemkald (funktioner leveret af kernen)|
|3|Bibliotekkald (funktioner i programbiblioteker)|
|4|Særlige filer (findes normalt i /dev)|
|5|Filformater og konventioner, f.eks. /etc/passwd|
|6|Spil|
|7|Diverse (herunder makropakker og konventioner), f.eks. man(7), groff(7)|
|8|Systemadministrationskommandoer (normalt kun for root)|
|9|Kernerutiner [Ikke standard]|

## Eksempel - Hvordan læser man MAN-sider?

Her er et eksempel på, hvordan man henter informatino om MkDir-kommandoen ved hjælp af Man-kommandoen.

```
% man mkdir

MKDIR(1)    USER COMMANDS       MKDIR(1)

NAME
   mkdir - make a directory

SYNOPSIS
   mkdir [ -p ] dirname...

DESCRIPTION
   mkdir creates directories. Standard entries,`.',for the
   directory itself, and `..' for its parent, are made automat-
   ically.

   The -p flag allows missing parent directories
   to be created as needed.

   With the exception of the set-gid bit, the
   current umask(2V) setting determines the mode in which
   directories are created. The new directory inherits the set-gid
   bit of the parent directory. Modes may be modified after
   creation by using chmod(1V).

   mkdir requires write permission in the parent directory.

SEE ALSO
   chmod(1V), rm(1), mkdir(2v), umask(2V)
```

## Referencer

* [OpenDocument tekniske specifikationer - af Wikipedia](https://en.wikipedia.org/wiki/OpenDocument_technical_specification)

* [man(1) — Linux-manualside](https://man7.org/linux/man-pages/man1/man.1.html)


