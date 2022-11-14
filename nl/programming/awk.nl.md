{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AWK-bestandsindeling - AWK-scriptbestand",
  "description":"Meer informatie over AWK-bestandsindelingen en API's die AWK-bestanden kunnen maken en openen.",
  "linktitle" : "AWK",
  "menu" : {
    "docs" : {
      "identifier" : "programming-awk",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## Wat is een AWK-bestand?

Een AWK-bestand is een scriptbestand dat is gemaakt voor de tekstverwerkingstoepassing **AWK** die wordt geleverd met Unix- en Linux-besturingssystemen. Het bevat logische instructies om acties uit te voeren op tekst of inhoud van een bestand, zoals het matchen, vervangen en afdrukken van tekst. Dit helpt bij het genereren van rapporten en opgemaakte tekst uit het invoerbestand. Het awk-hulpprogramma bevindt zich meestal in /usr/bin/awk op de meeste linux/unix-distributies.

## Hoe maak je een AWK-script?

Een AWK-bestand kan worden gemaakt of geopend in elke teksteditor op Linux/Unix OS. Een nieuw AWK-scriptbestand kan als volgt worden gemaakt.

```
$ vi script.awk
```

Dit opent het AWK-bestand in de teksteditor. Voer enkele uitspraken als volgt in de teksteditor in.

```
#!/usr/bin/awk -f
BEGIN { printf "%s\n","Writing my first Awk executable script!" }
```
De eerste regel van deze tekstinhoud wordt als volgt uitgelegd.

* \#! – aangeduid als `Shebang`, wat een tolk specificeert voor de instructies in een script
* /usr/bin/awk – is de tolk
* -f – interpreter-optie, gebruikt om een programmabestand te lezen

## Hoe AWK-script uit te voeren?

Sla het bestand op en maak het script uitvoerbaar door de onderstaande opdracht uit te voeren:
```
$ chmod +x script.awk
```

Het script kan dan als volgt worden uitgevoerd.

```
$ ./script.awk
```

dat resulteert in de volgende uitvoer.

```
Writing my first Awk executable script!
```

## Referentie ##

* [Scripts schrijven met Awk-programmeertaal](https://www.tecmint.com/write-shell-scripts-in-awk-programming/)

