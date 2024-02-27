{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "AGI-fil - Asterisk Gateway Interface-filformat",
  "description":"Lær om, hvad der er AGI-filformat med eksempler og API'er, der kan oprette og åbne AGI-filer.",
  "linktitle" : "AGI",
  "menu" : {
    "docs" : {
      "identifier": "programming-agi-da",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Hvad er en AGI fil?

En AGI-fil er en scriptfil, der bruges af open source-telefonisystemet, Asterisk. Den indeholder oplysninger, der kan bruges til at automatisere processer og Asterisk-opkaldsplan. Ved hjælp af AGI-scriptfiler kan forbindelser etableres med relationelle databaser såsom PostgreSQL eller MySQL. Derudover kan AGI-scripts også bruges til at få adgang til andre eksterne ressourcer. AGI-scripts kan omdanne kontrollen over opkaldsplanen til et eksternt AGI-script, hvilket gør det muligt for Asterisk at udføre komplekse opgaver.

## AGI-filformat - flere oplysninger

AGI-scriptfiler gemmes som tekstfiler og kan åbnes i enhver teksteditor for at foretage ændringer.

### Standardmønster for AGI-kommunikation

AGI-scriptet indlæser variablerne og deres værdier sendt til det af Asterisk. Et almindeligt udseende af disse variabler er som følger.

```
agi_request: test.py
agi_channel: Zap/1-1
agi_language: en
agi_callerid:
agi_context: default
agi_extension: 123
agi_priority: 2
```

Disse variabler efterfølges af en tom linje sendt af Asterisk, som viser, at AGI-scriptet kan tage kontrol over opkaldsplanen nu.

### Programmeringssprog for AGI-scriptfiler

AGI-scripts kan typisk skrives i Perl, [PHP](/programming/php/), [C](/programming/c/), Pascal eller Bourne Shell.

## Referencer

 * [Asterisk AGI Script](https://www.oreilly.com/library/view/asterisk-the-future/9780596510480/ch09.html)

