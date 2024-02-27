{
  "date": "2019-10-11",
  "keywords": [
"sh filen",
".sh-fil",
"udvidelse",
"format",
"sh fil eksempel",
"sh filformat",
"hvordan man kører sh-filen"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "SH - Bash Shell Script-fil",
  "description": "Lær om SH-filformat og API'er, der kan oprette og åbne SH-filer.",
  "linktitle": "SH",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-s-dah"
}
},
  "lastmod": "2021-05-21"
}

## Hvad er en SH fil?

En fil med filtypen .sh er en kommandofil i scriptsprog, der indeholder computerprogram, der skal køres af Unix-shell. Den kan indeholde en række kommandoer, der kører sekventielt for at udføre operationer såsom filbehandling, udførelse af programmer og andre sådanne opgaver. Disse udføres fra kommandolinjegrænsefladen af bruger eller i batch for at udføre flere operationer på samme tid. Scriptfiler kan åbnes i teksteditorer som Notepad, Notepad++, Vim, Apple Terminal og andre lignende programmer på Windows, MacOS og Linux OS.

## SH filformat

SH-filer skrives i almindelig tekst efter den definerede syntaks. Disse scriptfiler understøtter:

 * `Kommentarer` - Kommentarer starter med et # og ignoreres af skallen.
 * `Genveje` - Disse kan bruges til at omdøbe en kommando for kort og nem udførelse.
 * `Batch Jobs` - Adskillige kommandoer kan udføres automatisk, som ellers skulle indtastes manuelt. Dette fjerner behovet for at vente på, at en bruger udløser hvert trin i sekvensen.
 * `Generalisering` - Ved at bruge simple loops opnås meget mere generalisering for operationer såsom konvertering af billeder fra en fromat til en anden.

## Eksempel på SH-fil

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
## Hvordan kører man SH fil?
SH-filerne kører normalt på Linux, selv i Windows skal du oprette forbindelse til en Linux-terminal ved hjælp af software såsom Putty for at køre sh-filerne. Følgende er trinene til at køre en SH-fil på en Linux-terminal.

1. Åbn Linux-terminalen og gå til den mappe, hvor SH-filen er placeret.
2. Ved at bruge `chmod`-kommandoen, indstil udførelsestilladelse til dit script (hvis det ikke allerede er indstillet).
3. Kør script ved hjælp af en af følgende
	1. `./filnavn.sh`
	2.  `sh filnavn.sh`
	3.  `bash script-name-here.sh`

## Referencer

* [Bashscripting for begyndere](https://help.ubuntu.com/community/Beginners/BashScripting)

* [Shellscript](https://www.shellscript.sh/)


