{
  "date": "2022-05-09",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om PYC filformat og API'er, der kan oprette og åbne PYC filer.",
  "title": "PYC-filformat - Python-kompileret fil",
  "linktitle": "PYC",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-py-dac"
}
},
  "lastmod": "2022-05-09"
}

## Hvad er en PYC fil?

En PYC-fil er en kompileret outputfil, der er genereret fra kildekode skrevet i Python-programmeringssproget. Når PY-filen køres ved hjælp af Python-fortolker, konverteres den til bytekode til udførelse. Samtidig gemmes den kompilerede bytekode også som .pyc-fil, så den kan genbruges fra cachen på et senere tidspunkt, hvis det er relevant.

## Struktur af PYC-filformat

PYC-filer er i bytekode, og deres filformatspecifikationer er ikke offentligt tilgængelige. Undersøgelser fra nogle kilder viser dog, at [structure of a PYC file](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html) består af:

 * `Et fire-byte magisk tal` - Simpelthen to bytes, der ændres med hver ændring af rangeringskoden, og derefter to bytes af 0d0a.
 * `A fire-byte modification timestamp` - Unix-modifikationstidsstempel for kildefilen, der genererede .pyc, så den kan genkompileres, hvis kilden ændres.
 * `A marshalled code object` - outputtet af marshal.dump af kodeobjektet, der er et resultat af kompilering af kildefilen.

## Ofte stillede spørgsmål

1. **Hvordan genereres en PYC-fil?** En PYC-fil oprettes, når Python-kildekoden kompileres ved hjælp af Python-fortolkeren. Den kompilerede kode gemmes derefter i PYC-filen.

1. **Er PYC hurtigere end py?** PYC-filer gemmes, efter at python-kildekoden er kompileret. Da disse allerede er fortolket, er disse filer hurtigere end .py-filer.

1. **Hvad er forskellen mellem py- og pyc-fil?** PY-filer indeholder Python-kildekodefil til et program, mens .pyc-filer indeholder fortolket bytekode for et program.

1. **Er PYC en binær fil?** Ja, PYC-filen er en binær fil, der indeholder et 4-byte magisk tal, et 4-byte modifikationstidsstempel og et samlekodeobjekt.

1. **Kan vi konvertere .pyc til .py?** Ja, det er muligt at konvertere pyc-filer til py. Decompilere såsom Decompyle++ kan bruges til at oversætte kompileret Python-byte-kode tilbage til gyldig og menneskelig læsbar Python-kildekode.

## Referencer

* [Strukturen af .pyc-filer](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html)


