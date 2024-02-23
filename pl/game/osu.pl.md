{
  "date" : "2023-01-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Dowiedz się o formacie pliku OSU i interfejsach API, które umożliwiają tworzenie i otwieranie plików OSU.",
  "title" : "Plik OSU — Osu! Format pliku skryptu",
  "linktitle" : "OSU",
  "menu" : {
    "docs" : {
      "identifier":"game-osu-pl",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-18"
}

## Czym jest plik OSU?

Plik OSU to skrypt gry napisany dla osu! gra rytmiczna. Zawiera informacje o beatmapie używanej w grze, takie jak poziom trudności, utwór do odtworzenia oraz czas trafienia obiektów, z którymi gracz musi się zsynchronizować z muzyką. Umożliwia graczom gier rytmicznych opracowywanie niestandardowych wyzwań i udostępnianie ich społeczności graczy.

**Typ MIME formatu pliku OSR:** x-osu-beatmap

## Format pliku OSU

Pliki OSU są zapisywane na dysku jako zwykłe pliki tekstowe, a ich struktura jest bardzo jasno zdefiniowana w pliku [OSU file format](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29) autorstwa osu!.

### Sekcje w pliku OSU

Typowy plik OSU składa się z następujących sekcji.

|Sekcja |Opis |Typ zawartości|
---|---|---|
|[Ogólne]| Ogólne informacje o beatmapie| klucz: pary wartości|
|[Redaktor]| Zapisane ustawienia edytora beatmap| klucz: pary wartości|
|[Metadane] |Informacje wykorzystywane do identyfikacji beatmapy| klucz:pary wartości|
|[Trudność] |Ustawienia trudności| klucz:pary wartości|
|[Wydarzenia]| Wydarzenia graficzne związane z beatmapami i scenorysami| Listy oddzielone przecinkami|
|[Punkty czasowe]| Czas i punkty kontrolne| Listy oddzielone przecinkami|
|[Kolory]| Kombinacje i kolory skóry| klucz: pary wartości|
|[HitObiekty]| Uderzaj w przedmioty| Listy oddzielone przecinkami|

## Bibliografia

* [OSU! Gra rytmiczna](https://osu.ppy.sh/home)

* [Format pliku OSU](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29)


