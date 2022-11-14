{
  "date" : "2019-10-11",
  "keywords": [ "sh file", ".sh file", "extension", "format", "sh file example", "sh file format", "how to run sh file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SH - Bash Shell-scriptbestand",
  "description":"Meer informatie over SH-bestandsindeling en API's die SH-bestanden kunnen maken en openen.",
  "linktitle" : "SH",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-21"
}

## Wat is een SH-bestand?

Een bestand met de extensie .sh is een commandobestand voor scripttaal dat een computerprogramma bevat dat door Unix-shell moet worden uitgevoerd. Het kan een reeks opdrachten bevatten die opeenvolgend worden uitgevoerd om bewerkingen uit te voeren zoals het verwerken van bestanden, het uitvoeren van programma's en andere soortgelijke taken. Deze worden uitgevoerd vanaf de opdrachtregelinterface door de gebruiker of in batch om meerdere bewerkingen tegelijkertijd uit te voeren. Scriptbestanden kunnen worden geopend in teksteditors zoals Notepad, Notepad++, Vim, Apple Terminal en andere vergelijkbare applicaties op Windows, MacOS en Linux OS.

## SH-bestandsindeling

SH-bestanden worden in platte tekst geschreven volgens de gedefinieerde syntaxis. Deze scriptbestanden ondersteunen:

* `Opmerkingen` - Opmerkingen beginnen met een # en worden genegeerd door de shell.
* `Snelkoppelingen` - Deze kunnen worden gebruikt om een opdracht te hernoemen voor een korte en gemakkelijke uitvoering.
* `Batch Jobs` - Verschillende opdrachten kunnen automatisch worden uitgevoerd die anders handmatig zouden moeten worden ingevoerd. Dit elimineert de noodzaak om te wachten tot een gebruiker elke fase van de reeks activeert.
* `Veralgemening` - Met behulp van eenvoudige lussen wordt veel meer veralgemening bereikt voor bewerkingen zoals het converteren van afbeeldingen van de ene naar de andere.

## SH-bestand voorbeeld

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
## Hoe het SH-bestand uit te voeren?
De SH-bestanden worden meestal op Linux uitgevoerd, zelfs in Windows moet u verbinding maken met een Linux-terminal met software zoals Putty om de sh-bestanden uit te voeren. Hieronder volgen de stappen om een SH-bestand op een Linux-terminal uit te voeren.

1. Open de Linux-terminal en ga naar de map waar het SH-bestand zich bevindt.
2. Door de opdracht `chmod` te gebruiken, stelt u de uitvoermachtiging in op uw script (indien nog niet ingesteld).
3. Voer het script uit met een van de volgende:
1. `./bestandsnaam.sh`
2. `sh bestandsnaam.sh`
3. `bash script-naam-hier.sh`

## Referenties

* [Bashscripting voor beginners](https://help.ubuntu.com/community/Beginners/BashScripting)
* [Shellscript](https://www.shellscript.sh/)

