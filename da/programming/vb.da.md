{
  "date": "2019-10-11",
  "keywords": [
"vb",
"fil",
"udvidelse",
"filformat",
"Visual Basic",
"Programmeringsvejledning"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "VB - Visual Basic Code File",
  "description": "Lær om VB-filformat og API'er, der kan oprette og åbne VB-filer.",
  "linktitle": "VB",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-v-dab"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en VB fil?

En VB-fil er en kildekodefil, der er oprettet i Visual Basic-sproget, som blev oprettet af Microsoft til udvikling af .NET-applikationer. Et andet lignende sprog med anden syntaks er C#, hvis filer er gemt med filtypen [.CS](/programming/cs/). Filformatet giver programmeringssproget på lavt niveau til at skrive kode, der er kompileret til at generere den endelige outputfil i form af EXE eller en DLL. Disse kan oprettes og kompileres med Microsoft Visual Studio. Microsoft Visual Studio Express kan også bruges til at oprette og opdatere sådanne filer, som er en gratis IDE. Et simpelt Visual Studio-projekt [solution](/programming/sln/) oprettet med VB-sprog kan bestå af en eller flere sådanne filer. Filer, der er markeret til medtagelse i kompilering, er opført i filen [CSPROJ](/programming/csproj/), som er en del af projektet og fortæller kompilatoren at bruge de markerede filer.

## VB-filformat - flere oplysninger

VB-filer er tekstbaserede filformater, der kan åbnes i enhver teksteditor til redigering. Men når den åbnes i en understøttet IDE med korrekt syntaksfremhævning, er koden let at læse og arrangere. En simpel VB-fil indeholder:

* Namespaces declaration - For at henvise til en bestemt funktionalitet defineret af det specifikke navneområde

* Variable-deklaration - For at erklære klasseniveauvariabler for den bestemte implementering

* Metodeerklæring - At erklære metodeerklæring for den bestemte funktionalitet


## Eksempel på VB-filformat

```
Imports System
Module Module1
   'This program will display Hello World
   Sub Main()
      Console.WriteLine("Hello World")
      Console.ReadKey()
   End Sub
End Module
```



