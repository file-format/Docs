{
  "date" : "2019-10-11",
  "keywords" :["plik u3d", "format pliku u3d", "co to jest plik u3d", "plik", "przykład u3d", "rozszerzenie pliku u3d","rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"U3D - Uniwersalny format plików 3D",
  "description":"Poznaj format plików U3D i interfejsy API, które mogą otwierać i tworzyć pliki U3D.",
  "linktitle" : "U3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik U3D?

**U3D** (Universal 3D) to skompresowany format plików i struktura danych do grafiki komputerowej 3D. Zawiera informacje o modelu 3D, takie jak siatki trójkątów, oświetlenie, cieniowanie, dane ruchu, linie i punkty z kolorem i strukturą. Format został zaakceptowany jako standard [ECMA-363](http://www.ecma-international.org/publications/standards/Ecma-363.htm) w sierpniu 2005 r. Dokumenty 3D [PDF](/pl/pdf/) obsługują format U3D osadzanie obiektów i można je przeglądać w programie Adobe Reader (wersja 7 i nowsze).

Format U3D został opracowany z myślą o ustanowieniu uniwersalnego standardu trójwymiarowego przechowywania i wymiany danych. Jednak format znajduje swoje główne zastosowanie w kodowaniu 3D PDF, a nie jako format wymiany. Program Acrobat 3D konwertuje obsługiwany typ pliku 3D na format U3D lub PRC po konwersji do formatu PDF.

## Format pliku U3D

Pliki U3D są w formacie pliku binarnego, który przeszedł cztery edycje zgodnie z opisem w dokumencie referencyjnym [ECMA-363](http://www.ecma-international.org/publications/standards/Ecma-363.htm), co spowodowało aktualizację specyfikacji z każdą edycją. Standard pliku PDF ISO-32000 akceptuje U3D jako dozwolony typ adnotacji i multimediów.

Pierwsza edycja U3D koncentrowała się na kluczowych reprezentacjach właściwości grafiki 3D, takich jak geometria, kolor, tekstury, oświetlenie, kości i animacja oparta na transformacji. Wydanie drugie i trzecie poprawiło niektóre błędy w wydaniu pierwszym, przy czym wersja trzecia jest najczęściej używanym typem oprogramowania branżowego. Czwarta edycja zawiera definicje prymitywów wyższego rzędu (powierzchnie zakrzywione). [Specyfikacje U3D](http://www.ecma-international.org/publications/standards/Ecma-363.htm) są dostępne online do wglądu dla użytkowników na stronie internetowej ECMA.

### Typy danych w plikach U3D

Plik binarny będzie zawierał następujące typy: U8, U16, U32, U64, I16, I32, F32, F64 i String.

* U8 : 8-bitowa liczba całkowita bez znaku
* U16 : 16-bitowa liczba całkowita bez znaku
* U32 : 32-bitowa liczba całkowita bez znaku
* U64 : 64-bitowa liczba całkowita bez znaku
* I16 : 16-bitowa liczba całkowita ze znakiem
* F32: Pojedyncza precyzja zmiennoprzecinkowa IEEE.
* F64: Podwójna precyzja zmiennoprzecinkowa IEEE.
* Łańcuch: Łańcuchy w pliku U3D zaczynają się od 16-bitowej liczby całkowitej bez znaku, która określa całkowitą długość znaków w ciągu. Ciągi są zawsze przetwarzane z uwzględnieniem wielkości liter.

## Struktura plików U3D

Plik U3D zawiera sekwencję bloków. W każdym pliku U3D znajdują się 3 różne typy bloków.

* Blok nagłówka pliku
* Blok deklaracji
* Blok kontynuacji

Program ładujący określa koniec bloku, jeśli dane w tym bloku nie są wymagane lub jeśli dekoder dla tego typu bloku jest niedostępny.

{{< figure src="../u3d.png" alt="Format pliku U3D" >}}

### Blok nagłówka pliku
Blok nagłówka pliku zawiera informacje o pliku, które są używane przez ładowany plik do określenia sposobu jego odczytania.

### Blok deklaracji

Bloki deklaracji zawierają informacje o obiektach w pliku. Obiekty w bloku deklaracji muszą być zdefiniowane.

### Blok kontynuacji

Dodatkowe informacje dotyczące obiektów zadeklarowanych w bloku deklaracji znajdują się w bloku kontynuacji. Każdy blok kontynuacji musi być powiązany z blokiem deklaracji.


## Bibliografia ##

* [Format pliku U3D – Wikipedia](https://en.wikipedia.org/wiki/Universal_3D)
* [Specyfikacje formatu plików ECMA U3D](https://www.ecma-international.org/publications/standards/Ecma-363.htm)

