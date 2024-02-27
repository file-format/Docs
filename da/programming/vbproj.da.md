{
  "date": "2019-10-11",
  "keywords": [
"vbproj",
"fil",
"udvidelse",
"filformat",
"VB projekt fil",
"Programmeringsvejledning"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "VBPROJ",
  "description": "Lær om VBPROJ filformat og API'er, der kan oprette og åbne VBPROJ filer.",
  "linktitle": "VBPROJ",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-vbpro-daj"
}
},
  "lastmod": "2020-09-10"
}

## Hvad er en VBPROJ fil?

En fil med filtypenavnet .vbproj er en Microsoft Visual Basic-projektfil, der bruges af Microsofts MSBuild-motor til at bygge projekterne i en Visual Studio-løsning. Den ligner [CSPROJ](/programming/csproj/)-filen for .NET-projekter skrevet i [C#](/programming/cs/). MSBuild-motoren læser information indeholdt i forskellige grupper fra VBPROJ-filerne og genererer outputfilen. En VBPROJ-fil kan indeholde information relateret til globale identifikatorer, klasser og egenskaber, der definerer projektet. VBPROJ-filer kan åbnes og redigeres ved hjælp af Microsoft Visual Studio og enhver almindelig teksteditor, såsom Notesblok på Windows- og MacOS-operativsystemer.

## VBPROJ-filformat - flere oplysninger

VBPROJ-filer er tekstfiler, der er skrevet i filformatet [XML](/web/xml/) baseret på [MSBuild XML Schema](https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference?view=vs-2019). En VBPROJ-fil indeholder information i form af XML-tags, der definerer information relateret til den pågældende gruppe af indstillinger. Det anbefales stærkt at åbne og redigere disse indstillingsfiler i Microsoft Visual Studio IDE.

### VBPROJ Elements

Komponenterne i en VB-indstillingsfil er som vist på det følgende billede.

{{< figure src="../vbproj.png" alt="VBPROJ filformat" >}}

The following table gives a brief description of these elements.

|Element|Beskrivelse|
---|---|
|Projekt| Rodelement i hver projektfil og kan inkludere attributter til at specificere indgangspunkterne for byggeprocessen ud over at identificere XML-skema for projektfilen|
|Egenskaber og betingelser| Egenskaber består af nøgle-værdi-par og er defineret i et PropertyGroup-element. Egenskabselementets navn repræsenterer egenskabsnøglen, og indholdet af elementet definerer egenskabsværdien.|
|Items and ItemGroups|Elementer i en projektfil er input til byggeprocessen, såsom filkodefiler, konfigurationsfiler, kommandofiler og andre nødvendige som en del af byggeprocessen. Elementer er og skal defineres i et ItemGroup-element.|
|Mål og opgaver| Et opgaveelement repræsenterer en individuel byggeinstruktion (eller opgave). MSBuild inkluderer et væld af foruddefinerede opgaver såsom Copy, CSC, VBC, Exec. Opgaver skal altid være indeholdt i et `Target` Element, som er et sæt af en eller flere opgaver, der udføres sekventielt, og en projektfil kan indeholde flere targets.|

## Referencer

* [Forstå projektfilen](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file)

* [MSBuild Schema Elements](https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference?view=vs-2019)


