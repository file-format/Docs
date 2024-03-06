{
  "date": "2019-10-11",
  "keywords": [
"M fails",
"M",
"pagarinājumu",
"formātā",
"M faila formāts"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "M — Matlab pirmkoda fails",
  "description": "Uzziniet par Matlab .m pirmkoda failu un API, kas var izveidot un atvērt MF failus.",
  "linktitle": "M",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming--lvm"
}
},
  "lastmod": "2020-09-10"
}

# M — Matlab pirmkoda faili

## Kas ir M (Matlab) fails?

Fails ar paplašinājumu .m ir pirmkoda fails, ko izmanto Matlab — programmēšanas un skaitļošanas platforma, ko izmanto analīzei, algoritmu izstrādei un simulācijas modelēšanai. Tāpat kā citi programmēšanas failu formāti, M fails satur avota kodu, kas izpilda Matlab komandas, lai attēlotu grafikus, palaistu simulācijas un citas matemātiskas darbības. Viena Matlab simulācija var aptvert vairākus šādus .m failus, kas var klasificēt lietojumprogrammu skriptos, klasēs, funkcijās vai deklarācijās. Matlab M failus var atvērt ar jebkuru teksta redaktoru.

## Matlab M faila formāts — vairāk informācijas

Matlab .m faili ir teksta faili, kas satur programmēšanas kodu Matlab programmēšanas valodā. Tos var atvērt un rediģēt jebkurā teksta redaktorā un saglabāt atpakaļ, lai tos izpildītu Matlab programmatūrā. Pats Matlab satur Live Editor, ko izmanto, lai izveidotu skriptus, kas ir koda, izvades un formatēta teksta kombinācija.

### Matlab funkciju faili

Tāpat kā citas programmēšanas valodas, varat izveidot .m failu, kas satur tikai tādas funkcijas definīciju, kas veic tikai noteiktu uzdevumu. Šādi faili tiek saglabāti arī ar paplašinājumu .m un īsteno tikai ar šo funkciju saistīto funkcionalitāti.

### .M faila piemērs

Tālāk ir sniegts Matlab funkcijas faila piemērs, kas aprēķina laiku, kas nepieciešams objektam, kas nokrīt no augstuma h.

```C++
function t= TimeToGround(h)  
  t=sqrt(h/4.9);
end
```

Lai izsauktu šo funkciju no Matlab redaktora vai cita .m faila, var izmantot šādu kodu.
```C++
TimeToGround(100)
```

## Atsauces

 * [Matlab — atbalstītie failu formāti](https://www.mathworks.com/help/matlab/standard-file-formats.html)
 * [Izmantojot Matlab](https://www.maths.unsw.edu.au/sites/default/files/MatlabSelfPaced/lesson0/MatlabLesson0_Mfiles.html)

# M — Objective-C ieviešanas fails

## Kas ir M (Objective-C) fails?

M fails tiek saukts arī par ieviešanas failu, kas satur klases avota kodu, kas rakstīts Objective-C valodā — programmēšanas valoda, ko izmanto, lai rakstītu OS X un iOS lietojumprogrammas. Objective-C ir galvenā programmēšanas valoda, ko šīm platformām izmanto Apple galvenās API — Cocoa un Cocoa Touch. Viena programmatūra, kas izstrādāta šajā valodā, var saturēt vairākus .m failus, kas satur programmas klases. Tos var atvērt, izmantojot Apple XCode, jEdit un citus izplatītus teksta redaktorus.

## Objective-C M faila formāts — vairāk informācijas

M faili ir rakstīti vienkārša teksta formātā, izmantojot Objective-C programmēšanas sintaksi. Šajos ieviešanas failos katrai klases metodei ir jābūt definētai ar visu tai nepieciešamo kodu. Šie ieviešanas M faili var importēt vienu vai vairākus .h galvenes failus atbilstoši prasībām. Importēšanas paziņojums norāda kompilatoram, kur atrast galvenes failu, kas pieder šim ieviešanas failam. Importa paziņojums ir uzrakstīts šādi.

```C++
#import "network.h"
```

Katra M faila ieviešana sākas ar direktīvu @implementation, kam seko ieviešanas klases faila nosaukums. Pēc tam seko visu metožu ieviešana, kas ir deklarētas galvenes failā.

### M faila formāta piemērs

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

## Atsauces
 * [Par mērķi C](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/Introduction/Introduction.html#//apple_ref/doc/uid/TP40011210-CH1-SW1)
 * [Object-C rokasgrāmata](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

