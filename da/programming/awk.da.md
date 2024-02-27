{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "AWK-filformat - AWK Script-fil",
  "description":"Lær om AWK filformat og API'er, der kan oprette og åbne AWK filer.",
  "linktitle" : "AWK",
  "menu" : {
    "docs" : {
      "identifier" : "programming-awk-da",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## Hvad er en AWK fil?

En AWK-fil er en scriptfil, der er oprettet til tekstbehandlingsapplikationen **AWK**, der leveres sammen med Unix- og Linux-operativsystemer. Den indeholder logiske instruktioner til at udføre handlinger på tekst eller indhold af en fil, såsom at matche, erstatte og udskrive tekst. Dette hjælper med at generere rapporter og formateret tekst fra inputfilen. awk-værktøjet er normalt placeret i /usr/bin/awk på de fleste linux/unix-distributioner.

## Hvordan opretter man AWK script?

En AWK-fil kan oprettes eller åbnes i en hvilken som helst teksteditor på Linux/Unix OS. En ny AWK-scriptfil kan oprettes som følger.

```
$ vi script.awk
```

Dette åbner AWK-filen i teksteditor. Indtast nogle udsagn i teksteditoren som følger.

```
#!/usr/bin/awk -f
BEGIN { printf "%s\n","Writing my first Awk executable script!" }
```
Den første linje i dette tekstindhold forklares som følger.

 * \#! – omtalt som `Shebang`, som angiver en fortolker til instruktionerne i et script
 * /usr/bin/awk – er tolken
 * -f – fortolkermulighed, bruges til at læse en programfil

## Hvordan udføres AWK script?

Gem filen og gør scriptet eksekverbart ved at udstede kommandoen nedenfor:
```
$ chmod +x script.awk
```

Scriptet kan derefter køres som følger.

```
$ ./script.awk
```

hvilket resulterer i følgende output.

```
Writing my first Awk executable script!
```

## Reference ##

* [Skriv scripts med Awk-programmeringssprog](https://www.tecmint.com/write-shell-scripts-in-awk-programming/)


