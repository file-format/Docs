{
  "date": "2019-10-11",
  "keywords": [
"M failą",
"M",
"pratęsimas",
"formatu",
"M failo formatas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "M – „Matlab“ šaltinio kodo failas",
  "description": "Sužinokite apie Matlab .m šaltinio kodo failą ir API, kurios gali kurti ir atidaryti MF failus.",
  "linktitle": "M",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming--ltm"
}
},
  "lastmod": "2020-09-10"
}

# M – Matlab šaltinio kodo failai

## Kas yra M (Matlab) failas?

Failas su plėtiniu .m yra šaltinio kodo failas, kurį naudoja Matlab – programavimo ir skaitmeninio skaičiavimo platforma, naudojama analizei, algoritmų kūrimui ir modeliavimo modeliavimui. Kaip ir kituose programavimo failų formatuose, M faile yra šaltinio kodas, kuris vykdo Matlab komandas, kad nubrėžtų grafikus, paleistų modeliavimą ir kitas matematines operacijas. Vienas Matlab modeliavimas gali apimti kelis tokius .m failus, kurie gali klasifikuoti programą pagal scenarijus, klases, funkcijas ar deklaracijas. Matlab M failus galima atidaryti naudojant bet kurį teksto rengyklę.

## Matlab M failo formatas – daugiau informacijos

Matlab .m failai yra tekstiniai failai, kuriuose yra programavimo kodas Matlab programavimo kalba. Juos galima atidaryti ir redaguoti bet kuriame teksto rengyklėje ir išsaugoti atgal, kad būtų galima vykdyti Matlab programinėje įrangoje. Pačiame Matlab yra Live Editor, kuri naudojama scenarijų, kurie yra kodo, išvesties ir formatuoto teksto derinys, kūrimui.

### Matlab funkcijų failai

Kaip ir kitose programavimo kalbose, galite sukurti .m failą, kuriame yra tik funkcijos, kuri atlieka tik konkrečią užduotį, apibrėžimas. Tokie failai taip pat išsaugomi su plėtiniu .m ir įgyvendina tik su ta funkcija susijusias funkcijas.

### .M failo pavyzdys

Toliau pateikiamas Matlab funkcijos failo pavyzdys, kuriame apskaičiuojamas laikas, per kurį objektas nukrenta iš aukščio h.

```C++
function t= TimeToGround(h)  
  t=sqrt(h/4.9);
end
```

Norint iškviesti šią funkciją iš Matlab redaktoriaus arba iš kito .m failo, galima naudoti šį kodą.
```C++
TimeToGround(100)
```

## Nuorodos

 * [Matlab – palaikomi failų formatai](https://www.mathworks.com/help/matlab/standard-file-formats.html)
 * [Naudojant Matlab](https://www.maths.unsw.edu.au/sites/default/files/MatlabSelfPaced/lesson0/MatlabLesson0_Mfiles.html)

# M – Objective-C įgyvendinimo failas

## Kas yra M (Objective-C) failas?

M failas taip pat vadinamas diegimo failu, kuriame yra klasės šaltinio kodas, parašytas Objective-C kalba, programavimo kalba, naudojama programinės įrangos programoms, skirtoms OS X ir iOS, rašyti. Objective-C yra pagrindinė programavimo kalba, kurią šioms platformoms naudoja pagrindinės Apple API Cocoa ir Cocoa Touch. Viena programinė įranga, sukurta šia kalba, gali turėti kelis .m failus, kuriuose yra programos klasių įgyvendinimas. Juos galima atidaryti naudojant Apple XCode, jEdit ir kitus įprastus teksto redaktorius.

## „Objective-C M“ failo formatas – daugiau informacijos

M failai parašyti paprasto teksto formatu, naudojant Objective-C programavimo sintaksę. Kiekvienas klasės metodas turi būti apibrėžtas su visu reikalingu kodu šiuose diegimo failuose. Šie įgyvendinimo M failai gali importuoti vieną ar daugiau .h antraštės failų pagal reikalavimus. Importavimo sakinys nurodo kompiliatoriui, kur rasti antraštės failą, priklausantį šiam diegimo failui. Importo pareiškimas parašytas taip.

```C++
#import "network.h"
```

Tada kiekvienas M failo diegimas prasideda direktyva @implementation, po kurios nurodomas diegimo klasės failo pavadinimas. Tada seka visi antraštės faile deklaruoti metodai.

### M failo formato pavyzdys

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

## Nuorodos
 * [Apie C tikslą](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/Introduction/Introduction.html#//apple_ref/doc/uid/TP40011210-CH1-SW1)
 * [Object-C vadovas](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

