{
  "date" : "2019-10-11",
  "keywords": [ "M file", "M", "extension", "format", "M file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M - Matlab källkodsfil",
  "description":"Läs mer om Matlab .m källkodsfil och API:er som kan skapa och öppna MF-filer.",
  "linktitle" : "M",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

# M - Matlabs källkodsfiler

## Vad är en M (Matlab) fil?

En fil med tillägget .m är en källkodsfil som används av Matlab, en programmerings- och numerisk beräkningsplattform som används för analys, algoritmutveckling och simuleringsmodellering. Liksom andra programmeringsfilformat innehåller en M-fil källkod som kör Matlab-kommandon för att rita grafer, köra simuleringar och andra matematiska operationer. En enda Matlab-simulering kan sträcka sig över flera sådana .m-filer som kan klassificera applikationen i skript, klasser, funktioner eller deklarationer. Matlab M-filer kan öppnas med vilken textredigerare som helst.

## Matlab M filformat - Mer information

Matlab .m-filer är textfiler som innehåller programmeringskod i Matlabs programmeringsspråk. Dessa kan öppnas och redigeras i vilken textredigerare som helst och sparas tillbaka för att köras i Matlabs programvara. Matlab själv innehåller en Live Editor som används för att skapa skript som är en kombination av kod, utdata och formaterad text.

### Matlab-funktionsfiler

Precis som andra programmeringsspråk kan du skapa en .m-fil som bara innehåller definitionen av en funktion som endast utför en specifik uppgift. Sådana filer sparas också med tillägget .m och implementerar endast den funktionalitet som är relaterad till den funktionen.

### .M Fil Exempel

Följande är ett exempel på en Matlab-funktionsfil som beräknar tiden det tar för ett objekt att tappa från höjden h.

```C++
function t= TimeToGround(h)  
  t=sqrt(h/4.9);
end
```

För att anropa den här funktionen från Matlab-editorn eller från en annan .m-fil kan följande kod användas.
```C++
TimeToGround(100)
```

## Referenser

* [Matlab - Filformat som stöds](https://www.mathworks.com/help/matlab/standard-file-formats.html)
* [Använda Matlab](https://www.maths.unsw.edu.au/sites/default/files/MatlabSelfPaced/lesson0/MatlabLesson0_Mfiles.html)

# M - Objective-C implementeringsfil

## Vad är en M (Objective-C) fil?

En M-fil kallas också för implementeringsfil som innehåller källkoden för en klass skriven i Objective-C-språket, ett programmeringsspråk som används för att skriva program för OS X och iOS. Objective-C är det huvudsakliga programmeringsspråket som används av Apples huvudsakliga API:er, Cocoa och Cocoa Touch, för dessa plattformar. En enskild mjukvaruapplikation utvecklad på detta språk kan innehålla flera .m-filer som innehåller implementeringen av programklasserna. Dessa kan öppnas med Apple XCode, jEdit och andra vanliga textredigerare.

## Objective-C M-filformat - Mer information

M-filerna är skrivna i vanligt textformat med hjälp av programmeringssyntaxen för Objective-C. Varje metod i en klass måste definieras med all nödvändig kod i dessa implementeringsfiler. Dessa M-filer för implementering kan importera en eller flera .h-huvudfiler enligt kraven. Importsatsen talar om för kompilatorn var huvudfilen som hör till denna implementeringsfil kan hittas. Importförklaringen skrivs enligt följande.

```C++
#import "network.h"
```

Varje M-filimplementering börjar sedan med `@implementation`-direktivet, följt av implementeringsklassens filnamn. Detta följs sedan av alla metodimplementering som deklareras i header-filen.

### M Filformat Exempel

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

## Referenser
* [Om mål C](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/Introduction/Introduction.html#//apple_ref/doc/uid/TP40011210-CH1-SW1)
* [Object-C Guide](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

