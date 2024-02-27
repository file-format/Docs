{
  "date": "2019-10-11",
  "keywords": [
"cs",
"fil",
"udvidelse",
"filformat",
"CSarp",
"Programmeringssprog"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CS - CSharp Code File",
  "description": "Lær om CS-filformat og API'er, der kan oprette og åbne CS-filer.",
  "linktitle": "CS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-c-das"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en CS fil?

Filer med filtypenavnet .cs er kildekodefiler til programmeringssproget C#. Introduceret af Microsoft til brug med .NET Framework, giver filformatet lavniveau programmeringssprog til at skrive kode, der er kompileret til at generere den endelige outputfil i form af EXE eller en DLL. Disse kan oprettes og kompileres med Microsoft Visual Studio. Microsoft Visual Studio Express kan også bruges til at oprette og opdatere sådanne filer, som er en gratis IDE. CS-filer bruges til applikationsudvikling, der kan variere fra simple desktop-applikationer til mere komplekse programmer. Et simpelt Visual Studio-projekt [solution](/programming/sln/) oprettet med C#-sproget kan bestå af en eller flere sådanne filer. Filer, der er markeret til medtagelse i kompilering, er opført i filen [CSPROJ](/programming/csproj/), som er en del af projektet og fortæller kompilatoren at bruge de markerede filer.

## CS-filformat ##

CS-filer er tekstbaserede filformater, der kan åbnes i enhver teksteditor til redigering. Men når den åbnes i en understøttet IDE med korrekt syntaksfremhævning, er koden let at læse og arrangere. En simpel CS-fil indeholder:

* Namespaces declaration - For at henvise til en bestemt funktionalitet defineret af det specifikke navneområde

* Variable-deklaration - For at erklære klasseniveauvariabler for den bestemte implementering

* Metodeerklæring - At erklære metodeerklæring for den bestemte funktionalitet


### Syntaks ###

* Semikoloner bruges til at angive slutningen af et udsagn.

* Krøllede parenteser bruges til at gruppere udsagn. Udsagn er almindeligvis grupperet i metoder (funktioner), metoder i klasser og klasser i navneområder.

* Variabler tildeles ved hjælp af et lighedstegn, men sammenlignes med to på hinanden følgende lighedstegn.

* Firkantede parenteser bruges med arrays, både til at erklære dem og for at få en værdi ved et givet indeks i et af dem.


### Eksempel ###

```
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("Hello, world!");
}
}
```

## Andre CS-filer

Her er andre filtyper, der bruger filtypen **.cs**.

**Datafiler og spil**
- [CS - ColorSchemer Studio Color Scheme](/data/cs-colorschemer/)
- [CS - CLEO Custom Script](/game/cs-cleo/)

**Programmering**
- [CS - CSharp Code File](/programming/cs/)

