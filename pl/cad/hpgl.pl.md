{
  "date" : "2020-07-28",
  "keywords" :[ "HPGL", "Format pliku", "Otwórz", "Odczyt", "Utwórz", "CAD"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format pliku HPGL i interfejsy API, które mogą tworzyć i otwierać pliki HPGL.",
  "title" :"Format plików HPGL — ucz się od ekspertów od formatów plików!",
  "linktitle" : "HPGL",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-07-28"
}

## Czym jest plik HPGL?

Plik HPGFL (Hewlett-Packard Graphics Language) zawiera zestaw instrukcji do sterowania ploterem opracowany przez firmę HP. Plotery HP używają tego pliku do rysowania i drukowania zawartości wektorowej i rastrowej na papierze.

### Komenda HPGL

Polecenie HPGL składa się z następujących elementów.
* Sekcja poleceń alfabetu złożona z dwóch znaków
* Sekcja parametrów
* Sekcja Terminatora

Każdy parametr w pliku musi być oddzielony separatorem w przypadku wielu parametrów.

### Przykład polecenia HPGL

```
Example :PA5000,1000;
  (command)    PA
  (parameter)  5000
  (separator)  ,
  (parameter)  1000
  (terminator) ;
```

### System współrzędnych

Układy współrzędnych składają się z dwuwymiarowych wskaźników pomiarowych umożliwiających zlokalizowanie dowolnej określonej lokalizacji. HPGL używa do tego celu zarówno układu współrzędnych plotera, jak i układu współrzędnych użytkownika.

#### Układ współrzędnych plotera

Ten układ współrzędnych jest używany do kreślenia rysunków w oparciu o ruch plotera. Typowa jednostka XY minimalnego ruchu plotera to 0,025 mm. Możliwy zakres zmian rysunku z rodzajami ploterów.

#### Układ współrzędnych użytkownika

Określony przez użytkownika układ współrzędnych można ustawić za pomocą skali i początku. Są one konwertowane na współrzędne plotera za pomocą poleceń IP i SC. Współrzędne układu plotera są używane domyślnie, jeśli ta konwersja nie jest przeprowadzana.

## Format pliku HPGL
Pliki HPGL są w formacie ASCII (plik tekstowy) i zaczynają się od kilku poleceń konfiguracyjnych. To ustawia określone parametry plotera do kreślenia. Typowy plik HPGL wygląda następująco.

|Polecenie|Znaczenie
---|---|
|IN;|inicjalizuj, rozpocznij zadanie drukowania|
|IP;|ustaw punkty skalowania (P1 i P2) w ich domyślnych pozycjach|
|SP1;|wybierz pisak 1|
|PU0,0;|podnieś pióro w górę i przejdź do punktu startowego, aby wykonać następną akcję|
|PD100,0,100,100,0,100,0,0;|odłóż pióro i przejdź do następujących miejsc (narysuj ramkę wokół strony)|
|PU50,50;|Pióro w górę i przejdź do współrzędnych X,Y 50,50|
|CI25;|narysuj okrąg o promieniu 25|
|SS;|wybierz standardowy zestaw znaków|
|DT*,1;|ustaw ogranicznik tekstu na gwiazdkę i nie drukuj ich (1 oznacza "prawda")|
|PU20,80;|podnieś pióro i przejdź do 20,80|
|LBWitaj Świecie*;|narysuj etykietę|

## Bibliografia
* [HPGL z Wikipedii](https://en.wikipedia.org/wiki/HP-GL)
* [Przewodnik referencyjny HPGL](https://www.isoplotec.co.jp/HPGL/eHPGL.htm)

