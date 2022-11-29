{
  "date" : "2019-10-11",
  "keywords": [ "sh file", ".sh file", "extension", "format", "sh file example", "sh file format", "how to run sh file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SH - Bash Shell Script File",
  "description":"Läs mer om SH-filformat och API:er som kan skapa och öppna SH-filer.",
  "linktitle" : "SH",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-21"
}

## Vad är SH fil?

En fil med filändelsen .sh är en kommandofil för skriptspråk som innehåller datorprogram som ska köras av Unix-skalet. Den kan innehålla en serie kommandon som körs sekventiellt för att utföra operationer som filbearbetning, exekvering av program och andra sådana uppgifter. Dessa exekveras från kommandoradsgränssnittet av användare eller i batch för att utföra flera operationer samtidigt. Skriptfiler kan öppnas i textredigerare som Notepad, Notepad++, Vim, Apple Terminal och andra liknande applikationer på Windows, MacOS och Linux OS.

## SH filformat

SH-filer skrivs i vanlig text enligt den definierade syntaxen. Dessa skriptfiler stöder:

* `Kommentarer` - Kommentarer börjar med ett # och ignoreras av skalet.
* `Genvägar` - Dessa kan användas för att byta namn på ett kommando för kort och enkel exekvering.
* `Batch Jobs` - Flera kommandon kan utföras automatiskt som annars skulle behöva matas in manuellt. Detta tar bort behovet av att vänta på att en användare ska trigga varje steg i sekvensen.
* `Generalisering` - Genom att använda enkla loopar uppnås mycket mer generalisering för operationer som konvertering av bilder från en fromat till en annan.

## Exempel på SH-fil

```
$ echo '#!/bin/sh' > my-script.sh
$ echo 'echo Hello World' >> my-script.sh
$ cat my-script.sh
#!/bin/sh
echo Hello World
$ chmod 755 my-script.sh
$ ./my-script.sh
Hello World
```
## Hur kör man filen SH?
SH-filerna körs vanligtvis på Linux, även i Windows måste du ansluta till en Linux-terminal med hjälp av mjukvara som Putty för att köra sh-filerna. Följande är stegen för att köra en SH-fil på en Linux-terminal.

1. Öppna Linux-terminalen och gå till katalogen där SH-filen finns.
2. Genom att använda kommandot `chmod`, ställ in körrättigheter för ditt skript (om det inte redan är inställt).
3. Kör skriptet med något av följande
1. `./filnamn.sh`
2. `sh filnamn.sh`
3. `bash script-name-here.sh`

## Referenser

* [Bashscripting för nybörjare](https://help.ubuntu.com/community/Beginners/BashScripting)
* [Shellscript](https://www.shellscript.sh/)

