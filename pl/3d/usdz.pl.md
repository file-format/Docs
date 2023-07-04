{
  "date" : "2021-02-01",
  "keywords" :["usdz", "plik usdz", "format pliku usdz", "format pliku", "3d","pobieranie pliku usdz"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"USDZ - Universal Scene Description ZIP Format",
  "description":"Dowiedz się o formacie pliku USDZ i interfejsach API, które mogą otwierać i tworzyć pliki USDZ.",
  "linktitle" : "USDZ",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-02-01"
}

## Czym jest plik USDZ?

Plik z rozszerzeniem .usdz to nieskompresowane i niezaszyfrowane archiwum ZIP dla formatu pliku [USD](/pl/3d/usd/) (Universal Scene Description), które zawiera i proxy dla plików innych formatów (takich jak tekstury i animacje) osadzone w archiwum i uruchamia je bezpośrednio w środowisku wykonawczym USD bez potrzeby rozpakowywania. Pliki USDZ to pakiety, których projekt opiera się na nowej abstrakcji pakietu na poziomie Ar. Usdz został zarejestrowany w IANA i ma nazwę typu nośnika modelu oraz nazwę podtypu vnd.usd+zip, a jego szczegóły można znaleźć na stronie [strona rejestracji IANA](https://www.iana.org/assignments/media-typy/model/vnd.usdz+zip).

## Format pliku USDZ

Pliki USDZ są oparte na formacie pliku ZIP, który archiwizuje poszczególne pliki w swoim kontenerze. Dzięki temu odbiornik może po prostu rozpakować zawartość i użyć normalnych plików opisu sceny USD do pracy i kontroli. Prawie wszystkie systemy operacyjne zapewniają wbudowaną obsługę formatów plików ZIP, a wybranie tego formatu archiwizacji zamiast dowolnej niestandardowej metody ułatwia wykorzystanie plików USDZ jako prostego protokołu transportowego.

### Ograniczenia ZIP

Format pliku USDZ wykorzystuje format pliku ZIP bez żadnej „kompresji” i „szyfrowania”. Miało to na celu spełnienie dwóch wymagań:

* Dla pakietu już załadowanego do pamięci lub jako pojedynczy plik na dysku, API dostępne w USD za dostęp do danych zawartych w obrazie
* Nie powinno być potrzeby wyodrębniania plików na dysk ani przydzielania większej ilości pamięci na stercie

W przypadku USDZ oba te wymagania są spełnione, ponieważ większość formatów obrazów umożliwia wewnętrzne schematy kompresji, co skutkuje niewielkimi rozmiarami plików.

### Wymagania dotyczące układu

Pakiety USDZ wymagają takiego układu plików w pakiecie, aby dane dla każdego pliku zaczynały się od wielokrotności 64 bajtów od początku pakietu. Jednak pakiet powinien zaczynać się od natywnego pliku [USD](/pl/3d/usd/) w przypadku kierowania pakietu za pomocą prostej referencji. W takim przypadku ten pierwszy plik USD jest nazywany warstwą domyślną. Klienci, którzy chcą dostarczać „treści nadające się do przesyłania strumieniowego”, mogą również rozważyć inne ograniczenia dotyczące układu.

## Pobieranie pliku USDZ
Ponieważ pliki usdz są wypełnione innymi wysokiej jakości obrazami i plikami usd, mogą zajmować więcej miejsca na dysku. Tutaj możesz znaleźć prosty i mniejszy przykładowy plik USDZ do pobrania:

- [Próbka.usdz](../sample.usdz)

## Bibliografia

* [Specyfikacja formatu pliku USDZ](https://openusd.org/release/spec_usdz.html)
