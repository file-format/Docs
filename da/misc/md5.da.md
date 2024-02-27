{
  "date": "2021-07-29",
  "keywords": [
"md5 fil",
"md5 filformat",
"hvad er en md5 fil",
"fil",
"md5 eksempel",
"md5 filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MD5 - MD5 kontrolsum fil",
  "description": "Lær om MD5-filer og API'er, der kan oprette og åbne MD5-filer.",
  "linktitle": "MD5",
  "menu": {
    "docs": {
      "parent": "misc",
      "identifier": "misc-md-da5"
}
},
  "lastmod": "2021-07-29"
}

## Hvad er en MD5 fil?

En MD5-fil er en kontrolsum-fil, der bruges til at verificere en fils integritet. Det ligner et fingeraftryk for den tilknyttede fil og er unikt genereret ved hjælp af en algoritme, der bruger antallet af bits i filen. Den bruges til at bekræfte filen med software såsom [md5sum](http://www.gnu.org/software/coreutils/manual/html_node/md5sum-invocation.html). En fordel ved at bruge MD5-filer er at kontrollere, at de downloadede filer ikke er korrupte.

## MD5 filformat - flere oplysninger

Normalt gemmes en MD5-fil med det samme navn som det originale filnavn, men med filtypenavnet .md5. For eksempel, hvis det tilknyttede filnavn er `abc_987_123456.grb`, vil det tilsvarende MD5-filnavn være `abc_987_123456.grb.md5`. MD5-filer hjælper med at identificere, at en modtaget eller downloadet fil ikke er beskadiget eller påvirket af skadeligt indhold. Kort sagt garanterer MD5-filer fuldstændigheden af en fil.


## Hvordan tjekker man MD5 Checksum?

En enkelt fil kan kontrolleres/verificeres for MD5 ved hjælp af værktøjet [md5sum](https://en.wikipedia.org/wiki/Md5sum) som følger.

```
md5sum -c abc_987_123456.grb.md5
```

## Referencer

* [md5sum - Wikipedia](https://en.wikipedia.org/wiki/Md5sum)


