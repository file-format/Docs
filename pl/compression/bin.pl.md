{
"data":"2023-07-20",
   "keywords":[
"KOSZ",
"Plik BIN",
"plik",
"rozszerzenie pliku BIN",
"rozszerzenie",
"plik"
],
   "author":{
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title":"Format pliku BIN - plik zakodowany w formacie MacBinary",
   "description":"Dowiedz się o formacie BIN i interfejsach API, które umożliwiają tworzenie i otwieranie plików BIN.",
   "linktitle":"BIN",
   "menu":{
      "docs":{
         "identifier":"compression-bin",
         "parent":"compression"
}
},
"lastmod":"2023-07-20"
}

## Czym jest plik BIN?

Plik BIN w kontekście komputerów Macintosh może odnosić się do pliku zapisanego w formacie MacBinary. MacBinary to format pliku zaprojektowany specjalnie do przesyłania plików Macintosh przez Internet, pocztę e-mail, FTP lub nośniki przenośne. Celem MacBinary jest zachowanie pełnej struktury plików i atrybutów plików Macintosha, w tym zarówno rozwidlenia danych, jak i rozwidlenia zasobów, w jednym pliku.

Format MacBinary osiąga to poprzez hermetyzację rozwidleń zasobów i rozwidleń danych systemu Macintosh Hierarchical File System (HFS) w skompresowanym pliku. Zawiera także nagłówek wyszukiwarki, który zawiera ważne metadane dotyczące pliku. Łącząc wszystkie te komponenty w jeden plik, MacBinary gwarantuje, że plik zachowa swoją integralność i będzie można go łatwo przenosić i udostępniać na różnych platformach.

Wraz z postępem w systemach plików Apple i protokołach przesyłania plików korzystanie z plików BIN i formatu MacBinary stało się mniej powszechne. Wprowadzenie formatów plików takich jak ZIP i przejście na bardziej nowoczesne systemy plików, takie jak HFS+ i APFS, zmniejszyło zapotrzebowanie na pliki zakodowane w formacie MacBinary. Te nowsze systemy plików zapewniają bardziej wydajne sposoby obsługi atrybutów plików, rozwidleń zasobów i rozwidleń danych, dzięki czemu format MacBinary jest mniej potrzebny w dzisiejszym krajobrazie komputerowym.

## Format pliku BIN — więcej informacji

Na początku komputerów Macintosh pliki były przechowywane w dwóch oddzielnych "forkach" ze względu na ograniczenia danych. "Rozwidlenie zasobów" zawierało dane strukturalne, podczas gdy "rozwidlenie danych" zawierało dane nieustrukturyzowane. Podczas gdy klasyczny system Mac OS traktował te rozwidlenia jako pojedynczy plik, przesyłanie plików do systemów innych niż Mac skutkowało utratą danych, ponieważ nie rozpoznawały one rozwidleń jako pojedynczego elementu. Aby rozwiązać ten problem, format MacBinary został stworzony przez takie osoby, jak Dennis Brothers, Harry Chesley i Yves Lempereur. MacBinary skompresował i połączył widełki w jeden plik, znany jako plik BIN, w celu przesłania go do systemów innych niż Mac. Po powrocie do systemu Mac OS widelce zostaną ponownie rozdzielone. Wraz z odejściem od HFS opartego na widełkach w 2000 roku, użycie formatu MacBinary znacznie spadło. Obecnie natrafienie na plik BIN zakodowany w formacie MacBinary jest rzadkością, chyba że natkniesz się na stary plik w systemie innym niż Mac lub pobierzesz go z Internetu.

Z biegiem czasu format MacBinary przeszedł kilka wersji, aby uwzględnić zmiany w systemach Macintosh i obsłudze plików. Oto niektóre z różnych wersji formatu MacBinary:

- **MacBinary I:** Pierwsza wersja MacBinary, wprowadzona pod koniec lat 80-tych. Połączył rozwidlenie zasobów i rozwidlenie danych w jeden plik binarny, umożliwiając międzyplatformowy transfer plików Macintosh.

- **MacBinary II:** Ta wersja, wydana na początku lat 90-tych, jest udoskonalona w stosunku do oryginalnego formatu MacBinary poprzez dodanie dodatkowych informacji, takich jak typ pliku i kod twórcy, do nagłówka pliku binarnego. Kody te pomogły zachować integralność i identyfikację plików Macintosh podczas przesyłania.

- **MacBinary III:** Format MacBinary III, wprowadzony w połowie lat 90. XX wieku, jeszcze bardziej udoskonalił poprzednie wersje, dodając w nagłówku pliku binarnego dodatkowe metadane, takie jak nazwa pliku oraz daty utworzenia i modyfikacji pliku. Pozwoliło to na pełniejsze zachowanie atrybutów plików Macintosh podczas przesyłania.

- **MacBinary IV:** MacBinary IV został opracowany w celu rozwiązania problemów ze zgodnością z systemem operacyjnym Mac OS X pojawiającym się na początku XXI wieku. Zawiera zmiany mające na celu dostosowanie się do nowej struktury systemu plików i atrybutów wprowadzonych w systemie Mac OS X.

## Jak otworzyć plik BIN?

Pliki BIN zakodowane w formacie MacBinary można otwierać za pomocą różnych narzędzi do kompresji. Dla użytkowników systemu macOS odpowiednią opcją jest **Apple Archive Utility**. Użytkownicy systemu Windows mogą korzystać z oprogramowania takiego jak **Smith Micro StuffIt Deluxe** w celu wyodrębnienia zawartości pliku BIN zakodowanego w systemie MacBinary. Inną opcją dla użytkowników systemu macOS jest **The Unarchiver**, które jest wszechstronnym narzędziem obsługującym wiele formatów plików, w tym MacBinary.

Należy zauważyć, że rozszerzenie pliku .bin jest używane przez różne formaty plików, nie tylko MacBinary. Dlatego jeśli napotkasz plik BIN, którego nie można otworzyć za pomocą wyżej wymienionych narzędzi, może on zostać zapisany w innym formacie. W takich przypadkach może być konieczne określenie konkretnego formatu pliku i użycie odpowiedniego oprogramowania lub narzędzia przeznaczonego dla tego formatu, aby uzyskać dostęp do zawartości pliku.

## Inne pliki BIN

Oto inne typy plików, które korzystają z rozszerzenia **.bin**.

- [BIN – Binarny plik obrazu dysku](/pl/disc-and-media/bin/)
- [BIN - Plik wykonywalny Uniksa](/pl/executable/bin/)
- [BIN – plik zasad IT BlackBerry](/pl/settings/bin/)
- [BIN - ROM gry Sega Genesis](/pl/game/bin/)
- [BIN - Obraz BIOS-u PSX PlayStation](/pl/game/bin-pcsx/)

## Bibliografia

* [MacBinary](https://en.wikipedia.org/wiki/MacBinary)

