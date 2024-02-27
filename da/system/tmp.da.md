{
  "date": "2021-07-15",
  "keywords": [
"TMP",
"udvidelse",
"fil",
"format",
"system",
"TMP fil",
"TMP dokumenter",
"TMP filer",
"Midlertidig fil",
"Ansøgning",
"programmer"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "TMP - Midlertidig filformat",
  "description": "Lær om TMP-filformat og API'er, der kan oprette og åbne TMP-filer.",
  "linktitle": "TMP",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-tm-dap"
}
},
  "lastmod": "2021-07-15"
}

## Hvad er TMP fil? ##

En TMP-fil refererer til en midlertidig sikkerhedskopiering, lagring eller andet filsystem genereret af et softwareprogram. Den oprettes af og til som en usynlig fil og bliver ofte ødelagt, når programmet afsluttes. TMP-filer kan også bruges til midlertidigt at gemme information, mens en ny fil bliver konstrueret.

## TMP filformat ##

En TMP-fil består typisk af rådata, der bruges som en fase i konverteringsprocessen af materiale fra en stil til en anden. Microsoft Word og Apple Safari er to apps, der kan producere og bruge TMP-filformat.

TMP-dokumenter, der genereres, bør i teorien automatisk fjernes, når programmet lukkes eller maskinen slukkes. I praksis er dette ikke altid tilfældet. Som følge heraf kan du, mens du navigerer gennem dit programs dokumenter, støde på forbigående filer, som ikke bruges aktivt af systemet eller anden software.

### Hjælpehukommelse ###

Virtuel hukommelse bruges i operativsystemer, men programmer, der bruger enorme mængder af information, kan have brug for at lave midlertidige dokumenter.

### Kommunikation mellem processer ###

De fleste operativsystemer giver primitiver til at overføre data mellem programmer, såsom rør, sockets eller hovedhukommelse, men den enkleste metode er at overføre filer til en midlertidig fil og rådgive den modtagende applikation om den midlertidige fils placering.


## Teknisk specifikation ##

Opnåelse af karakteristiske midlertidige dokumentnavne leveres normalt af operativsystemer og softwareprogrammer.
Midlertidige filer kan sikkert genereres på POSIX-systemer ved hjælp af biblioteksfunktionerne mkstemp eller tmpfile. Nogle systemer inkluderer den tidligere POSIX (siden væk) mktemp-applikation. Disse filer findes normalt i den almindelige midlertidige mappe på Unix-platforme i /TMP eller %TEMP% (det er specifikt for log-in) på Windows-maskiner.

Når programmet stopper, eller dokumentet lukkes, fjernes den forbigående fil, der er genereret med tmp-filen, automatisk. GetTempFileName (Windows) eller tmpnam (POSIX) kan bruges til at oprette et midlertidigt filnavn, der vil vare længere end det program, der oprettede det.

## Reference ##

* [TMP - Wikipedia](https://en.wikipedia.org/wiki/Temporary_file)
