{
  "date": "2023-03-07",
  "keywords": [
"manifest fil",
"hvad er en manifestfil",
"fil",
"manifest filtypenavn",
"udvidelse"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "MANIFEST-filformat - Windows Application Manifest-fil",
  "description": "Lær om MANIFEST-format og API'er, der kan oprette og åbne MANIFEST-filer.",
  "linktitle": "MANIFEST",
  "menu": {
    "docs": {
      "identifier": "system-manifest-da",
      "parent": "system"
}
},
  "lastmod": "2023-03-07"
}

## Hvad er en MANIFEST fil?

En manifestfil er en fil, der indeholder oplysninger om et softwareprogram eller en pakke. Filen er typisk navngivet med filtypen .manifest. Manifestfilen giver oplysninger om de filer, der er inkluderet i pakken, deres versionsnumre og eventuelle afhængigheder, som pakken har til andre softwarekomponenter.

Manifestfiler bruges almindeligvis på Windows-platformen for at sikre, at softwareapplikationer er korrekt installeret og konfigureret. De kan bruges til at specificere ting som hvilke versioner af delte biblioteker der skal bruges, hvilke konfigurationsfiler der skal inkluderes, og hvilke registreringsdatabasenøgler der skal ændres under installationen.

Ud over Windows kan manifestfiler også bruges i andre sammenhænge, såsom til webapplikationer eller Android-applikationer. Det specifikke format og indholdet af en manifestfil vil afhænge af platformen og applikationen, der pakkes.

## Mere information

Manifestfiler er i XML-format. XML er et meget brugt markup-sprog til at skabe strukturerede dokumenter og data, og det bruges ofte i softwareudvikling til at beskrive konfigurationer, indstillinger og andre metadata.

I forbindelse med softwareapplikationer indeholder en manifest XML-fil typisk oplysninger om applikationens afhængigheder, versionsoplysninger og andre konfigurationsindstillinger. Filen bruges til at sikre, at applikationen er installeret korrekt, og at den har alle de nødvendige komponenter og ressourcer til at køre korrekt.

Manifestet XML-fil kan inkluderes i applikationspakken eller som en separat fil, der downloades under installationen. Det er normalt navngivet med en .manifest filtypenavn og følger et specifikt format defineret af den platform eller ramme, som applikationen er bygget på.

For eksempel bruges en manifest XML-fil i Microsoft .NET Framework til at beskrive afhængigheder og versionsoplysninger for en applikation, og den er typisk inkluderet som en del af applikationens samling. Filen bruges af Common Language Runtime (CLR) til at bestemme de korrekte versioner af assemblies, der skal indlæses, og for at sikre, at applikationen kører korrekt.

## Referencer
* [Manifest-fil](https://en.wikipedia.org/wiki/Manifest_file)


