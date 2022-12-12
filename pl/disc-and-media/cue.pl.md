{
  "date" : "2021-06-09",
  "keywords" :[ "cue", "plik", "rozszerzenie", "format", "co to jest plik cue", "muzyka", "format pliku cue", "specyfikacja formatu pliku cue", "arkusz cue", "CDRWIN" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format pliku CUE i interfejsy API, które mogą tworzyć, konwertować i otwierać pliki CUE.",
  "title" :"CUE - plik arkusza wskazań",
  "linktitle" : "CUE",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-07-01"
}

## Czym jest plik CUE?

Plik z rozszerzeniem .cue, znany również jako plik arkusza cue, to plik metadanych zawierający informacje o układzie ścieżek na płycie CD lub DVD. Są one obsługiwane przez odtwarzacze multimedialne i aplikacje do tworzenia dysków optycznych. Do głównych danych audio zapisanych na płycie CD odwołuje się plik cue, wraz ze specyfikacjami dotyczącymi długości ścieżek, tytułów płyt i wykonawców. Tak więc, jeśli pojedynczy plik audio zawiera wiele ścieżek, plik cue może zostać użyty do podzielenia audio na wiele plików lub odniesienia do różnych ścieżek.

## Format pliku CUE

Pliki CUE lub arkusze cue są przechowywane w formacie zwykłego tekstu, który jest czytelny dla człowieka. Informacje w pliku cue to polecenia z jednym lub większą liczbą parametrów. Polecenia te dotyczą całego pliku lub pojedynczej ścieżki, w zależności od konkretnego polecenia i kontekstu. Podręcznik użytkownika CDRWIN opisuje specyfikację składni i semantyki arkusza cue.

## Podstawowe polecenia arkusza CUE

|Polecenie|Opis|
---|---|
|PLIK| Odnosi się do pliku zawierającego dane i jego formatu, takiego jak [MP3](/pl/audio/mp3/), [WAV](/pl/audio/wav/) lub zwykły binarny obraz dysku)|
|TRASY| Definiuje informacje kontekstowe ścieżki, takie jak jej numer i typ lub tryb.|
|INDEKS| Reprezentuje pozycję jako indeks w PLIKU. Format to mm:ss:ff (minuta-sekunda-ramka).|
|PREGAP i POSTGAP|Wskazuje przerwę przed lub po przerwie ścieżki, która nie jest przechowywana w żadnym pliku danych. Długość jest podawana w tym samym formacie minutowo-sekundowym, jak w przypadku INDEX.|

### Przykład arkusza CUE

```
REM GENRE Electronica
REM DATE 1998
PERFORMER "Faithless"
TITLE "Live in Berlin"
FILE "Faithless - Live in Berlin.mp3" MP3
  TRACK 01 AUDIO
    TITLE "Reverence"
    PERFORMER "Faithless"
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    TITLE "She's My Baby"
    PERFORMER "Faithless"
    INDEX 01 06:42:00
  TRACK 03 AUDIO
    TITLE "Take the Long Way Home"
    PERFORMER "Faithless"
    INDEX 01 10:54:00
  TRACK 04 AUDIO
    TITLE "Insomnia"
    PERFORMER "Faithless"
    INDEX 01 17:04:00
  TRACK 05 AUDIO
    TITLE "Bring the Family Back"
    PERFORMER "Faithless"
    INDEX 01 25:44:00
  TRACK 06 AUDIO
    TITLE "Salva Mea"
    PERFORMER "Faithless"
    INDEX 01 30:50:00
  TRACK 07 AUDIO
    TITLE "Dirty Old Man"
    PERFORMER "Faithless"
    INDEX 01 38:24:00
  TRACK 08 AUDIO
    TITLE "God Is a DJ"
    PERFORMER "Faithless"
    INDEX 01 42:35:00
```
## Bibliografia

* [plik .cda – z Wikipedii](https://en.wikipedia.org/wiki/.cda_file)

