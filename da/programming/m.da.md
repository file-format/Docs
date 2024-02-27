{
  "date": "2019-10-11",
  "keywords": [
"M fil",
"M",
"udvidelse",
"format",
"M filformat"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "M - Matlab kildekodefil",
  "description": "Lær om Matlab .m kildekodefil og API'er, der kan oprette og åbne MF-filer.",
  "linktitle": "M",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming--dam"
}
},
  "lastmod": "2020-09-10"
}

# M - Matlab kildekodefiler

## Hvad er en M (Matlab) fil?

En fil med filtypenavnet .m er en kildekodefil, der bruges af Matlab, en programmerings- og numerisk beregningsplatform, der bruges til analyse, udvikling af algoritmer og simuleringsmodellering. Ligesom andre programmeringsfilformater indeholder en M-fil kildekode, der udfører Matlab-kommandoer til at plotte grafer, køre simuleringer og andre matematiske operationer. En enkelt Matlab-simulering kan strække sig over flere sådanne .m-filer, der kan klassificere applikationen i scripts, klasser, funktioner eller erklæringer. Matlab M-filer kan åbnes med enhver teksteditor.

## Matlab M filformat - flere oplysninger

Matlab .m filer er tekstfiler, der indeholder programmeringskode i Matlab programmeringssprog. Disse kan åbnes og redigeres i enhver teksteditor, og gemmes tilbage for at blive udført i Matlab-software. Matlab selv indeholder en Live Editor, der bruges til at skabe scripts, der er en kombination af kode, output og formateret tekst.

### Matlab funktionsfiler

Som andre programmeringssprog kan du oprette en .m-fil, der kun indeholder definitionen af en funktion, som kun udfører en bestemt opgave. Sådanne filer gemmes også med .m-udvidelsen og implementerer kun funktionaliteten relateret til den funktion.

### .M Fil Eksempel

Det følgende er et eksempel på en Matlab-funktionsfil, der beregner den tid, det tager for et objekt, der falder fra højden h.

```C++
function t= TimeToGround(h)  
  t=sqrt(h/4.9);
end
```

For at kalde denne funktion fra Matlab editor eller fra en anden .m fil, kan følgende kode bruges.
```C++
TimeToGround(100)
```

## Referencer

 * [Matlab - Understøttede filformater](https://www.mathworks.com/help/matlab/standard-file-formats.html)
 * [Brug af Matlab](https://www.maths.unsw.edu.au/sites/default/files/MatlabSelfPaced/lesson0/MatlabLesson0_Mfiles.html)

# M - Objective-C implementeringsfil

## Hvad er en M (Objective-C) fil?

En M-fil omtales også som implementeringsfil, der indeholder kildekoden til en klasse skrevet i Objective-C-sprog, et programmeringssprog, der bruges til at skrive softwareapplikationer til OS X og iOS. Objective-C er det vigtigste programmeringssprog, der bruges af Apples vigtigste API'er, Cocoa og Cocoa Touch, til disse platforme. En enkelt softwareapplikation udviklet på dette sprog kan indeholde flere .m-filer, der indeholder implementeringen af programklasserne. Disse kan åbnes ved hjælp af Apple XCode, jEdit og andre almindelige teksteditorer.

## Objective-C M filformat - flere oplysninger

M-filerne er skrevet i almindeligt tekstformat ved hjælp af programmeringssyntaksen for Objective-C. Hver metode i en klasse skal defineres med al den nødvendige kode i disse implementeringsfiler. Disse implementerings-M-filer kan importere en eller flere .h-header-filer i henhold til kravene. Import-sætningen fortæller compileren, hvor den header-fil, der hører til denne implementeringsfil, skal findes. Importerklæringen skrives som følger.

```C++
#import "network.h"
```

Hver M-filimplementering starter derefter med `@implementation`-direktivet, efterfulgt af implementeringsklassens filnavn. Dette efterfølges derefter af alle metoders implementering, der er erklæret i header-filen.

### M Filformat Eksempel

```C++
UrlConnection.m

#import "UrlConnection.h"

@implementation UrlConnection

(void)connect {
    // In here would be code to attempt a connection to the
    // specified URL, while possibly handling connection errors.
    //
}

 + (BOOL)canHandleRequest:(NSString \*)type
                   forUrl:(NSString \*)url {
    //And in here would be code to see if the given URL passed
    // in is capable of handling the HTTP request type specified
    // by the "type" parameter. It will return YES or NO.
 }

 @end
```

## Referencer
 * [Om mål C](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/Introduction/Introduction.html#//apple_ref/doc/uid/TP40011210-CH1-SW1)
 * [Object-C Guide](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

