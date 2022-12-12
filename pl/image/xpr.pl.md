{
  "date" : "2022-03-21",
  "keywords" :[ "plik xpr", "format pliku xpr", "co to jest plik xpr", "plik", "przykład xpr", "rozszerzenie pliku xpr", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku XPR — plik graficzny Microsoft Expression Design",
  "description":"Poznaj format pliku XPR i interfejsy API, które mogą tworzyć i otwierać pliki XPR.",
  "linktitle" : "XPR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-03-21"
}

## Czym jest plik XPR?

Plik XPR to plik obrazu wektorowego utworzony za pomocą obecnie wycofanego oprogramowania Microsoft Expression Graphics (EGD). Zawiera informacje graficzne, które można wykorzystać jako makietę interfejsu użytkownika. Pliki XPR zostały później zastąpione plikami .design w Microsoft Expression Design. Pliki XPR można otwierać za pomocą programu Microsoft Expression Studio, który został wycofany od dłuższego czasu.

## Luka w zabezpieczeniach formatu pliku XPR

Zidentyfikowano, że pliki XPR wykorzystują lukę w Microsoft Expression Design, umożliwiając zdalne wykonanie kodu. W zgłaszanym problemie, jeśli użytkownik otworzył prawidłowy plik .xpr, który znajduje się w katalogu sieciowym wraz z plikiem biblioteki dołączanej dynamicznie (DLL), program Microsoft Expression Design mógł podjąć próbę załadowania pliku DLL i wykonania zawartego w nim kodu. Zostało to później naprawione przez firmę Microsoft w aktualizacji zabezpieczeń.

## Bibliografia

* [Luka w zabezpieczeniach projektu wyrażenia może umożliwić zdalne wykonanie kodu (2651018)](https://docs.microsoft.com/en-us/security-updates/securitybulletins/2012/ms12-022)

