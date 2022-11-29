{
  "date" : "2021-07-25",
  "keywords":["man","file", "extension", "type", "format", "Unix Manual"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MAN - Unix Manual",
  "description":"Lär dig om FODT-filformat och API:er som kan skapa och öppna MAN-filer.",
  "linktitle" : "MAN",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-07-25"
}

## Vad är MAN fil?

En fil med tillägget .man står för man page som är en Unix-programmeringsmanual i form av mjukvarudokumentation. Det används av verktyget "Man", som ingår i Unix, som används för att se dokumentationen. Programvarudokumentationen innehåller information i avsnitt och sidor som kan hämtas med hjälp av Man-verktyget från kommandoterminalen genom att utfärda kommandon. Eftersom den är tillgänglig i datorn som mjuk kopia av dokumentation, krävs det ingen utskriven kopia eller internetanslutning för att komma åt den.

## Unix Manual Man File Format - Mer information

Man-sidor lagras i vanligt textformat och kan skapas och öppnas i valfri textredigerare för visning eller redigering. I UNIX hämtas information från man-sidorna genom att utfärda kommandon från terminalen som inkluderar referens till avsnitt och sidnummer från manualen.

### Avsnitt och sidor

Unix man är systemets manual där varje sidargument till kommandot refererar till namnet på ett program, verktyg eller funktion. kommandot, om det tillhandahålls med avsnittsinformation, kommer att söka efter sidan i det specifika avsnittet. Standardbeteendet är dock att söka efter sidan i alla avsnitt och visa den första sidan oavsett om den finns i flera avsnitt.

### Avsnittsnummer

Följande är informationen om avsnittsnumren i manualen följt av vilka typer av sidor de innehåller.

|Sektionsnummer|Sidtyp|
---|---|
|1|Körbara program eller skalkommandon|
|2|Systemanrop (funktioner som tillhandahålls av kärnan)|
|3|Biblioteksanrop (funktioner inom programbibliotek)|
|4|Specialfiler (finns vanligtvis i /dev)|
|5|Filformat och konventioner, t.ex. /etc/passwd|
|6|Spel|
|7|Övrigt (inklusive makropaket och konventioner), t.ex. man(7), groff(7)|
|8|Systemadministrationskommandon (vanligtvis endast för root)|
|9|Kärnrutiner [icke standard]|

## Exempel - Hur läser man MAN-sidor?

Här är ett exempel på hur man hämtar information om MkDir-kommandot med Man-kommandot.

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

## Referenser

* [OpenDocument Technical Specifications - By Wikipedia](https://en.wikipedia.org/wiki/OpenDocument_technical_specification)
* [man(1) — Linux-manualsida](https://man7.org/linux/man-pages/man1/man.1.html)

