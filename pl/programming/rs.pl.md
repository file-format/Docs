{
  "date" : "2021-09-01", 

  "keywords" :["RS", "plik", "rozszerzenie", "format pliku", "Język programowania Rust", "Przewodnik programowania", "Przykład RS", "Rust", "VBScript" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RS - Plik Programowania Rusta",
  "description":"Poznaj format plików RS i interfejsy API, które mogą tworzyć i otwierać pliki RS.",
  "linktitle" : "RS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-01"
}

## Czym jest plik RS?

Plik z rozszerzeniem RS należy do języka programowania Rust, jest wielowymiarowym, wysokopoziomowym, uniwersalnym językiem programowania zaprojektowanym z myślą o użyteczności i bezpieczeństwie, a szczególnie bezpiecznej. Rust jest składniowo podobny do С++, ale może zagwarantować bezpieczeństwo pamięci dzięki użyciu sprawdzania poprawności referencji. Język Rust zapewnia bezpieczeństwo pamięci bez zbierania śmieci, a liczenie referencji jest opcjonalne.

## Format pliku RS ##

Rust został oryginalnie zaprojektowany przez Graydona Hоаre z Mozilla Research, przy współudziale Dаve'a Hermana, Brendana Eicha i innych. Zyskuje coraz większe zastosowanie w przemyśle, a firma Microsoft eksperymentuje z językiem w celu zapewnienia bezpieczeństwa i krytycznych dla bezpieczeństwa składników oprogramowania.

Rust został uznany za „najbardziej lubiany język programowania” w ankiecie Stack Þverflоw Developer Survey co roku od 2016 r., chociaż w ankiecie z 2021 r. był używany tylko przez 7% respondentów. Wraz ze standardowym trybem statycznym, przed wersją 0.4, Rust obsługiwał również tyrestaty.

System tyrestаte modeluje twierdzenia przed i po twierdzeniach programowych, poprzez użycie specjalnego zestawienia kontrolnego. Rozbieżności można wykryć w czasie rzeczywistym, a nie w czasie wykonywania, jak może to mieć miejsce w przypadku twierdzeń w kodzie С lub С++. Tyrestatyczny tekst nie był unikalny dla Rust, ponieważ został po raz pierwszy wprowadzony w języku NIL. Tyresy zostały usunięte, ponieważ w rzeczywistości były mało używane, chociaż tę samą funkcjonalność można osiągnąć, wykorzystując semantykę ruchu Rusta.

Język programowania Rust pomaga pisać szybsze i bardziej niezawodne oprogramowanie. Ergonomia wysokiego poziomu i kontrola niskiego poziomu są często sprzeczne w projektowaniu języka programowania; Wyzwania związane z rdzą. Dzięki bardzo zaawansowanej technologii i doskonałemu doświadczeniu programistycznemu, Rust daje ci możliwość kontrolowania szczegółów niskiego poziomu (takich jak użycie pamięci) bez kłopotliwej pracy z sugestią

 

## Krótka historia ##

Język wyrósł z indywidualnego projektu rozpoczętego w 2006 roku przez pracownika Mozilla, Graydona Hоаre, który stwierdził, że projekt został prawdopodobnie nazwany na cześć rodziny grzybów rdzy. Mozilla zaczęła sponsorować projekt w 2009 roku i ogłosiła go w 2010 roku. Rust 1.0, pierwsza stabilna wersja, została wydana 15 maja 2015 roku. wydaniach, a następnie testowane z wersjami beta, które trwają sześć tygodni. W dniu 6 kwietnia 2021 r. Google ogłosił wsparcie dla Rusta w ramach Androida.

## Specyfikacja techniczna ##

Rust ma być językiem dla wysoce aktualnych i bardzo bezpiecznych systemów, a także programować w dużych, to znaczy tworzyć i utrzymywać granice, które zachowują integralność dużego systemu. Doprowadziło to do zestawu funkcji z naciskiem na bezpieczeństwo, kontrolę układu pamięci i pewność.


Język Rust został zaprojektowany tak, aby był bezpieczny dla pamięci. Nie dopuszcza zerowych wskaźników, zwisających wskaźników ani ras danych. Wartości danych można zainicjować tylko za pomocą ustalonego zestawu formularzy, z których wszystkie wymagają, aby ich dane wejściowe były już zainicjowane. Aby ponownie sprawdzić, czy wartości są prawidłowe, czy też NULL, na przykład w połączonych listach lub binarnych strukturach danych drzewa, biblioteka rdzenia Rust zapewnia odpowiednią opcję. Rust dodał składnię do zarządzania wcieleniami. Niebezpieczny kod może obalić niektóre z tych ograniczeń za pomocą niebezpiecznego słowa kluczowego.


Język Rust nie używa automatycznego zbierania błędów. Pamięć i inne zasoby są zarządzane poprzez pozyskiwanie zasobów, jest to konwencja inicjalizacji, z oryginalnym liczeniem referencji.


Rust zapewnia deterministyczne zarządzanie zasobami, przy bardzo niskim koszcie ogólnym. Rust faworyzuje stos wszystkich wartości i nie oznacza ukrytego boksu. Istnieją referencje (za pomocą symbolu), które nie obejmują łączenia referencji w czasie wykonywania. Bezpieczeństwo takich wskaźników jest weryfikowane na bieżąco, zapobiegając zwisającym wskaźnikom i innym formom niezdefiniowanego zachowania.


Rust ma system własności, w którym wszystkie wartości mają unikalnego właściciela. Wartości mogą być oceniane przez niezmienne referencje, używając &T, przez zmienne referencje, używając & mut T, lub przez wartość, używając T. Kompilator Rust egzekwuje te reguły w tym samym czasie i sprawdza, czy wszystkie referencje są ważne.


## Przykład formatu pliku RS ##

```
use serde::{Serialize, Deserialize};

#[derive(Serialize, Deserialize, Debug)]
struct Point {
    x: i32,
    y: i32,
}

fn main() {
    let point = Point { x: 1, y: 2 };

    let serialized = serde_json::to_string(&point).unwrap();
    println!("serialized = {}", serialized);

    let deserialized: Point = serde_json::from_str(&serialized).unwrap();
    println!("deserialized = {:?}", deserialized);
}
```

## Odniesienie ##

* [RS – z Wikipedii](https://en.wikipedia.org/wiki/Rust_(programming_language))



