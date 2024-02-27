{
  "date": "2019-10-11",
  "keywords": [
"mf filen",
"mf",
"udvidelse",
"format",
"mf filformat"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MF - Java Manifest filformat",
  "description": "Lær om MF filformat og API'er, der kan oprette og åbne MF filer.",
  "linktitle": "MF",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-m-daf"
}
},
  "lastmod": "2020-09-10"
}

## Hvad er en MF fil?

En fil med filtypenavnet .mf er en Java Manifest-fil, der indeholder oplysninger om de individuelle [JAR](/programming/jar/) filposter. Selve MF-filen er indeholdt i JAR-filen og giver alle udvidelses- og pakkerelaterede definitioner. JAR-filer kan produceres til at blive brugt som en eksekverbar fil. I sådanne tilfælde specificerer mainfest-filen applikationens hovedklasse, der indeholder **`public static void main`**-erklæring. Manifestfiler er navngivet som MANIFEST.MF og kan åbnes med enhver teksteditor på Windows, MacOS og Linux-operativsystemer.

## Manifest filformatspecifikationer

[Manifest file format specifications](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) are available by Oracle in their guide for JAR file format. A Manifest file comprises of main sections that are followed by a list of sections for individual JAR file entries. Each section follows some rules and restrictions.

### Hovedafsnit

Et hovedafsnit:

* indeholder oplysninger om sikkerhed og konfiguration om JAR-filen

* indeholder oplysninger om den applikation eller udvidelse, som filen JAR er en del af

* definerer de vigtigste egenskaber for hvert enkelt manifestelement


**Bemærk**: Ingen attribut i denne sektion kan navngives Navn.

### Individuelle sektioner

En individuel sektion definerer forskellige attributter for pakker eller filer i en JAR-fil. Hver sektion skal starte med en attribut med navnet Navn, hvis værdi skal være en relativ sti til filen eller en absolut URL, der refererer til data uden for arkivet.

### Manifest specifikationer

|Attributter|Beskrivelse|
---|---|
|manifest-fil|hovedafsnit ny linje *individuel-sektion|
|main-section|version-info newline *main-attribute|
|version-info|Manifest-version : version-nummer|
|versionsnummer|cifret+{.digit+}*|
|main-attribute|(enhver legitim hovedattribut) newline|
|individual-section|Navn : værdi newline *perentry-attribute|
|perentry-attribute|(enhver legitim perentry-attribut) newline|
|nylinje|CR LF | LF | CR (ikke efterfulgt af LF)|
|digit|{0-9}|

## Referencer

 * [Oracle - JAR File Format](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html)
 * [JAR-filformat](https://en.wikipedia.org/wiki/JAR_(filformat))

