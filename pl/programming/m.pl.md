{
  "date" : "2019-10-11",
  "keywords": [ "M file", "M", "extension", "format", "M file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M - plik kodu źródłowego Matlab",
  "description":"Dowiedz się o pliku kodu źródłowego Matlab .m i interfejsach API, które mogą tworzyć i otwierać pliki MF.",
  "linktitle" : "M",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

# M - Pliki kodu źródłowego Matlaba

## Co to jest plik M (Matlab)?

Plik z rozszerzeniem .m to plik kodu źródłowego używany przez Matlab, platformę programowania i obliczeń numerycznych używaną do analizy, opracowywania algorytmów i modelowania symulacyjnego. Podobnie jak inne formaty plików programistycznych, plik M zawiera kod źródłowy, który wykonuje polecenia Matlaba w celu wykreślenia wykresów, uruchomienia symulacji i innych operacji matematycznych. Pojedyncza symulacja Matlaba może obejmować wiele takich plików .m, które mogą klasyfikować aplikację w postaci skryptów, klas, funkcji lub deklaracji. Pliki Matlab M można otwierać w dowolnym edytorze tekstu.

## Format pliku Matlab M — więcej informacji

Pliki Matlab .m to pliki tekstowe zawierające kod programowania w języku programowania Matlab. Można je otwierać i edytować w dowolnym edytorze tekstu oraz zapisywać z powrotem w celu wykonania w oprogramowaniu Matlab. Sam Matlab zawiera Live Editor, który służy do tworzenia skryptów będących kombinacją kodu, danych wyjściowych i sformatowanego tekstu.

### Pliki funkcyjne Matlaba

Podobnie jak inne języki programowania, możesz utworzyć plik .m, który zawiera tylko definicję funkcji wykonującej tylko określone zadanie. Takie pliki są również zapisywane z rozszerzeniem .m i realizują funkcjonalność związaną tylko z tą funkcją.

### Przykład pliku .M

Poniżej znajduje się przykład pliku funkcyjnego Matlab, który oblicza czas potrzebny na upuszczenie obiektu z wysokości h.

```C++
function t= TimeToGround(h)  
  t=sqrt(h/4.9);
end
```

Aby wywołać tę funkcję z edytora Matlab lub z innego pliku .m, można użyć następującego kodu.
```C++
TimeToGround(100)
```

## Bibliografia

* [Matlab — obsługiwane formaty plików] (https://www.mathworks.com/help/matlab/standard-file-formats.html)
* [Korzystanie z Matlaba](https://www.maths.unsw.edu.au/sites/default/files/MatlabSelfPaced/lesson0/MatlabLesson0_Mfiles.html)

# M — Plik implementacji celu-C

## Co to jest plik M (Objective-C)?

Plik M jest również określany jako plik implementacyjny, który zawiera kod źródłowy klasy napisany w języku Objective-C, języku programowania używanym do pisania aplikacji dla OS X i iOS. Objective-C jest głównym językiem programowania używanym przez główne interfejsy API Apple, Cocoa i Cocoa Touch, dla tych platform. Pojedyncza aplikacja opracowana w tym języku może zawierać wiele plików .m zawierających implementację klas programu. Można je otworzyć za pomocą Apple XCode, jEdit i innych popularnych edytorów tekstu.

## Format pliku Objective-C M — więcej informacji

Pliki M są zapisywane w formacie zwykłego tekstu przy użyciu składni programowania Objective-C. Każda metoda klasy musi być zdefiniowana wraz z całym niezbędnym kodem w tych plikach implementacyjnych. Te implementacyjne pliki M mogą importować jeden lub więcej plików nagłówkowych .h zgodnie z wymaganiami. Instrukcja import mówi kompilatorowi, gdzie znaleźć plik nagłówkowy należący do tego pliku implementacji. Instrukcja importu jest napisana w następujący sposób.

```C++
#import "network.h"
```

Każda implementacja pliku M zaczyna się od dyrektywy `@implementation`, po której następuje nazwa pliku klasy implementacji. Następnie następuje implementacja wszystkich metod, które są zadeklarowane w pliku nagłówkowym.

### Przykład formatu pliku M

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

## Bibliografia
* [Informacje o celu C](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/Introduction/Introduction.html#//apple_ref/doc/uid/TP40011210-CH1-SW1)
* [Przewodnik po języku C](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

