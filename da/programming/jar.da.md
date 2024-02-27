{
  "date": "2019-10-11",
  "keywords": [
"KRUKKE",
".krukke",
"hvad er en jar-fil",
"hvordan man åbner en jar-fil",
"udvidelse",
"fil",
"jar-fil",
"jar filformat",
".jar-udvidelse"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "JAR - Java Archive File Format",
  "description": "Lær om JAR-filformat og API'er, der kan oprette og åbne JAR-fil.",
  "linktitle": "JAR",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-ja-dar"
}
},
  "lastmod": "2020-09-10"
}

## Hvad er en JAR fil?

En fil med filtypen .jar er en Java Archive-fil, der indeholder mange forskellige programrelaterede filer som en enkelt fil. Dette filformat blev oprettet for at reducere hastigheden af indlæsning af en downloadet Java-applet i browseren via HTTP-transaktion ved at undgå at oprette flere HTTP-forbindelser. En enkelt JAR-fil kan indeholde Java-klassefiler ([.class](/programming/class/)), [images](/image/) og [sounds](/audio/). Individuelle elementer inde i en JAR-fil kan signeres digitalt af applikationsudvikleren for at autentificere deres oprindelse. JAR-filer bruges regelmæssigt til at skabe funktionelle API'er, der indeholder specifik funktionalitet relateret til denne API.

## JAR filformat

JAR files are based on the popular [ZIP file format](/compression/zip/) that archives its individual content files in a single file. JAR file format supports compressions, resulting in a smaller file size for downloading and hence further improves the download time. The [JAR file specifications](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) artilce by Oracle gives complete details about the internal specifications of JAR files.

### Manifestfilen

Når en JAR-fil oprettes, oprettes der automatisk en manifestfil inde i den, der indeholder metadataoplysninger om indholdet af JAR-filen. Denne fil viser indholdet, der er pakket inde i JAR-filen. En typisk Manifest-fil ser ud som følger, som viser de mapper og klasser, der er inkluderet i JAR-filen.

```
META-INF/
META-INF/MANIFEST.MF
pack/
pack/class1.class
pack/class2.class
..
..
```

#### Manifest specifikationer

Manifestspecifikationer er defineret af Oracle som følger.

`manifest-fil`: hovedafsnit newline \*individual-section

`main-section`: version-info newline \*main-attribute

`version-info`: Manifest-Version: version-nummer

`version-nummer` : ciffer+{.digit+}*

`main-attribute`: (enhver legitim hovedattribut) newline

`individual-section`: Navn : værdi newline \*perentry-attribute

perentry-attribute: (enhver legitim perentry-attribut) newline

`nylinje` : CR LF | LF | CR (ikke efterfulgt af LF)

`cifre`: {0-9}

### Eksekverbar JAR

JAR-filer kan også bestå af et program, der kan udføres af Java Virtual Machine (JVM) svarende til enhver anden applikation på Microsoft Windows-operativsystemet. I dette tilfælde skal JVM'en vide om applikationens indgangspunkt, som er enhver klasse med en offentlig statisk void-hovedmetode. Manifestfilen identificerer en sådan klasse med Main-Class header i følgende format:

```
Main-Class: com.example.MyClassName
```



## Referencer

 * [JAR File Overview](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jarGuide.html)
 * [JAR-filformat](https://en.wikipedia.org/wiki/JAR_(filformat))

