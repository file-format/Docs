{
  "date" : "2019-10-11",
  "keywords": [ "M file", "M", "extension", "format", "M file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M - Fișierul codului sursă Matlab",
  "description":"Aflați despre fișierul Matlab .m Source Code și API-urile care pot crea și deschide fișiere MF.",
  "linktitle" : "M",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

# M - Fișiere de cod sursă Matlab

## Ce este un fișier M (Matlab)?

Un fișier cu extensia .m este un fișier de cod sursă utilizat de Matlab, o platformă de programare și calcul numeric folosită pentru analiză, dezvoltarea algoritmilor și modelarea simulării. Ca și alte formate de fișiere de programare, un fișier M conține cod sursă care execută comenzi Matlab pentru a trasa grafice, a rula simulări și alte operații matematice. O singură simulare Matlab se poate întinde pe mai multe astfel de fișiere .m care pot clasifica aplicația în scripturi, clase, funcții sau declarații. Fișierele Matlab M pot fi deschise cu orice editor de text.

## Format de fișier Matlab M - Mai multe informații

Fișierele Matlab .m sunt fișiere text care conțin cod de programare în limbajul de programare Matlab. Acestea pot fi deschise și editate în orice editor de text și salvate înapoi pentru a fi executate în software-ul Matlab. Matlab în sine conține un editor live care este folosit pentru a crea scripturi care sunt o combinație de cod, ieșire și text formatat.

### Fișiere cu funcție Matlab

Ca și alte limbaje de programare, puteți crea un fișier .m care conține doar definiția unei funcții care îndeplinește doar o anumită sarcină. Astfel de fișiere sunt, de asemenea, salvate cu extensia .m și implementează doar funcționalitatea aferentă funcției respective.

### Exemplu de fișier .M

Următorul este un exemplu de fișier cu funcție Matlab care calculează timpul necesar pentru un obiect aruncat de la înălțimea h.

```C++
function t= TimeToGround(h)  
  t=sqrt(h/4.9);
end
```

Pentru a apela această funcție din editorul Matlab sau dintr-un alt fișier .m, se poate folosi următorul cod.
```C++
TimeToGround(100)
```

## Referințe

* [Matlab - Formate de fișiere acceptate](https://www.mathworks.com/help/matlab/standard-file-formats.html)
* [Folosind Matlab](https://www.maths.unsw.edu.au/sites/default/files/MatlabSelfPaced/lesson0/MatlabLesson0_Mfiles.html)

# M - Fișier de implementare Objective-C

## Ce este un fișier M (Obiectiv-C)?

Un fișier M este denumit și fișier de implementare care conține codul sursă al unei clase scrise în limbajul Objective-C, un limbaj de programare folosit pentru a scrie aplicații software pentru OS X și iOS. Objective-C este principalul limbaj de programare care este folosit de principalele API-uri Apple, Cocoa și Cocoa Touch, pentru aceste platforme. O singură aplicație software dezvoltată în acest limbaj poate conține mai multe fișiere .m, care conțin implementarea claselor de programe. Acestea pot fi deschise folosind Apple XCode, jEdit și alte editoare de text obișnuite.

## Format de fișier Objective-C M - Mai multe informații

Fișierele M sunt scrise în format text simplu folosind sintaxa de programare a Objective-C. Fiecare metodă a unei clase trebuie să fie definită cu tot codul necesar în aceste fișiere de implementare. Aceste fișiere M de implementare pot importa unul sau mai multe fișiere antet .h conform cerințelor. Declarația de import îi spune compilatorului unde să găsească fișierul antet care aparține acestui fișier de implementare. Declarația de import este scrisă după cum urmează.

```C++
#import "network.h"
```

Fiecare implementare a fișierului M începe apoi cu directiva `@implementation`, urmată de numele fișierului clasei de implementare. Aceasta este apoi urmată de implementarea tuturor metodelor care sunt declarate în fișierul antet.

### M Exemplu de format de fișier

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

## Referințe
* [Despre Obiectivul C](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/Introduction/Introduction.html#//apple_ref/doc/uid/TP40011210-CH1-SW1)
* [Ghid pentru obiectul C](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

