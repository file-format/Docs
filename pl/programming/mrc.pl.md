{
  "date" : "2021-09-14", 
  "keywords" :[ "mrc", "plik", "rozszerzenie", "format pliku", "implementacja mrc", "Przewodnik programowania", "przykład mrc", "mIRC", "język skryptowy mIRC", "pliki INI", " język skryptowy mSL", "język mIRC", "skrypty mIRC", "język skryptowy"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MRC - plik języka skryptowego mIRC",
  "description":"Poznaj format pliku MRC i interfejsy API, które mogą tworzyć i otwierać pliki MRC.",
  "linktitle" : "MRC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-14"
}

## Czym jest plik MRC?

mIRC to język skryptowy osadzony jako klient IRC (Internet Relay Chat) w systemie operacyjnym Windows. Zapewnia funkcję ochrony przed spamowaniem do użytku osobistego i kanału. Aby zapewnić lepszą kompatybilność użytkownika, ten język skryptowy mIRC umożliwia tworzenie okien dialogowych. Pliki zawierające skrypty, przeważnie w formacie zwykłego tekstu, są przechowywane z rozszerzeniem MRC lub jako pliki [INI](/pl/system/ini/). Funkcje tego języka nazywane są poleceniami i identyfikatorami (gdy zwracają wartość).

Język mIRC zapewnia jednoczesne ładowanie wielu plików skryptów. Z drugiej strony jeden plik może spowodować, że drugi nie będzie już używany, gdy zostanie załadowany jednocześnie. Polecenia są zapisywane i mogą istnieć w IRC automatycznie. Komendy i aliasy używane w tym języku nie zawierają pierwszeństwa żadnego ze znaków.

mIRC jest szeroko stosowany do automatycznego zarządzania kanałem przez boty, ale można go również modyfikować za pomocą języka skryptowego mSL. Może wprowadzać wiele nowych funkcji, takich jak makra, możliwość odtwarzania muzyki, małe makra i funkcje, podstawowe gry, czy obsługa małych aplikacji.


## Krótka historia ##

Ten język skryptowy został po raz pierwszy opracowany w 1995 roku przez Khaleda Adama Beya. Projekt języka skryptowego został również stworzony przez Khalida. Celem tego języka było programowanie sterowane zdarzeniami. Początkowo rozszerzenie pliku używane dla plików tego języka programowania to .mrc i .ini. Co więcej, został opracowany na licencji autorskiego oprogramowania.

## Specyfikacja techniczna ##

Niektóre funkcje są tworzone na zamówienie w tym języku mIRC i są znane jako aliasy. Kiedy te aliasy zwracają wartości, są znane jako identyfikatory niestandardowe. Wszystkie zmienne zawarte w tym języku mIRC są typowane dynamicznie. Sigile są używane przez skrypty mIRC. Kolejną cechą tego języka skryptowego są wyskakujące okienka. Użytkownicy mogą wywoływać wyskakujące okienka, po prostu je wybierając. Piloty są określone dla określonych zdarzeń. Piloty są wywoływane, gdy wystąpi zdarzenie względne.

Tokeny rozdzielane spacjami służą do łamania każdej linii kodu tego języka. Istnieje kilka innych popularnych rozszerzeń używanych do plików mIRC, takich jak MDX (mIRC Dialog Extension) i DCX (Dialog Control Extension). Oba są rozszerzeniami dialogowymi i są stosunkowo bardziej popularne. Konstrukcje językowe są określane przez nazewnictwo tego języka skryptowego. Język mIRC obejmuje różne aspekty języka skryptowego, takie jak zmienne lokalne i globalne, zmienne binarne, tablice skrótów i obsługa plików.


## Przykład formatu pliku MRC ##

```

;Defines the alias 'hello' in the remote script

;Note: if this is placed in an alias script,
;the 'alias' part must be removed (result: hello {)
;Usage: /hello

alias hello {

  ;Displays(/pl/echo) 'Hello World!' into the active window(-a)
  echo -a Hello World!

}

```

```
;Placed in a remote script

;When a user types Hello! in a channel,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:#:{ msg $chan Hello, $nick $+ ! }

;When a user types Hello! in a private message,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:?: { msg $nick Hello, $nick $+ ! }

;Here is a script which automatically gives voice to a user
;who joins a particular channel (The Bot or user should have HOP)

on *:JOIN:#?: { mode $chan +v $nick }

;A bad word script

on *:Text:die*:#: { .mode $chan +b $nick | kick $chan $nick Dont say that again }

```

## Odniesienie ##

* [MIRC – z Wikipedii](https://en.wikipedia.org/wiki/MIRC_scripting_language)



