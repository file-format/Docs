{
  "date" : "2019-10-11",
  "keywords": [ "M file", "M", "extension", "format", "M file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M - Matlab Source Code File",
  "description":"Další informace o souboru zdrojového kódu Matlab .m a rozhraních API, která mohou vytvářet a otevírat soubory MF.",
  "linktitle" : "M",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

# M - Soubory zdrojového kódu Matlab

## Co je soubor M (Matlab)?

Soubor s příponou .m je soubor zdrojového kódu, který používá Matlab, platforma pro programování a numerické výpočty používaná pro analýzu, vývoj algoritmů a simulační modelování. Stejně jako jiné formáty programovacích souborů obsahuje soubor M zdrojový kód, který spouští příkazy Matlabu k vykreslování grafů, spouštění simulací a dalších matematických operací. Jedna simulace Matlabu může zahrnovat více takových .m souborů, které mohou klasifikovat aplikaci ve skriptech, třídách, funkcích nebo deklaracích. Soubory Matlab M lze otevřít v libovolném textovém editoru.

## Formát souboru Matlab M - Další informace

Soubory Matlab .m jsou textové soubory, které obsahují programovací kód v programovacím jazyce Matlab. Ty lze otevřít a upravit v libovolném textovém editoru a uložit zpět k provedení v softwaru Matlab. Samotný Matlab obsahuje Live Editor, který se používá pro vytváření skriptů, které jsou kombinací kódu, výstupu a formátovaného textu.

### Soubory funkcí Matlab

Stejně jako jiné programovací jazyky můžete vytvořit soubor .m, který obsahuje pouze definici funkce, která provádí pouze konkrétní úlohu. Takové soubory jsou také uloženy s příponou .m a implementují funkce související pouze s touto funkcí.

### Příklad souboru .M

Následuje příklad souboru funkce Matlab, který vypočítává čas potřebný pro objekt spadlý z výšky h.

```C++
function t= TimeToGround(h)  
  t=sqrt(h/4.9);
end
```

K volání této funkce z editoru Matlab nebo z jiného souboru .m lze použít následující kód.
```C++
TimeToGround(100)
```

## Reference

* [Matlab – podporované formáty souborů](https://www.mathworks.com/help/matlab/standard-file-formats.html)
* [Pomocí Matlabu](https://www.maths.unsw.edu.au/sites/default/files/MatlabSelfPaced/lesson0/MatlabLesson0_Mfiles.html)

# M - Objective-C Implementation File

## Co je soubor M (Objective-C)?

Soubor M se také nazývá implementační soubor, který obsahuje zdrojový kód třídy napsané v jazyce Objective-C, což je programovací jazyk používaný k psaní softwarových aplikací pro OS X a iOS. Objective-C je hlavní programovací jazyk, který používají hlavní API společnosti Apple, Cocoa a Cocoa Touch, pro tyto platformy. Jedna softwarová aplikace vyvinutá v tomto jazyce může obsahovat více souborů .m obsahujících implementaci programových tříd. Ty lze otevřít pomocí Apple XCode, jEdit a dalších běžných textových editorů.

## Formát souboru Objective-C M - Další informace

Soubory M jsou zapsány ve formátu prostého textu pomocí programovací syntaxe Objective-C. Každá metoda třídy musí být definována se všemi potřebnými kódy v těchto implementačních souborech. Tyto implementační soubory M mohou importovat jeden nebo více souborů záhlaví .h podle požadavků. Příkaz import říká kompilátoru, kde má najít hlavičkový soubor, který patří tomuto souboru implementace. Příkaz importu je zapsán následovně.

```C++
#import "network.h"
```

Každá implementace souboru M pak začíná direktivou `@implementation`, za kterou následuje název souboru implementační třídy. Poté následuje implementace všech metod, které jsou deklarovány v záhlaví souboru.

### Příklad formátu souboru M

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

## Reference
* [O cíli C](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/Introduction/Introduction.html#//apple_ref/doc/uid/TP40011210-CH1-SW1)
* [Průvodce objektem C](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

