{
  "date" : "2019-10-11",
  "keywords" :[ "yaml", ".yaml", "co to jest plik yaml", "jak otworzyć plik yaml", "rozszerzenie", "plik", "plik yaml", "format pliku yaml", "rozszerzenie yaml" , "yaml vs json", "przykład pliku YAML", "przykład pliku docker yaml"],
  "author" : {
    "display_name" : "Muhammad Ahmad Chishti"
},
  "draft" : "false",
  "toc" : true,
  "description" :" Dowiedz się więcej o formacie pliku YAML i interfejsach API, które mogą tworzyć i otwierać plik YAML.",
  "title" :"Format Pliku YAML",
  "linktitle" : "YAML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-05"
}

## Czym jest plik YAML? ##

**Plik YAML** składa się z języka YAML (YAML Ain't Markup Language), który jest językiem serializacji danych opartym na Unicode; używany do plików konfiguracyjnych, wiadomości internetowych, trwałości obiektów itp. YAML używa rozszerzenia .yaml dla swoich plików. Jego składnia jest niezależna od konkretnego języka programowania. Zasadniczo YAML jest przeznaczony do interakcji międzyludzkich i dobrze współpracuje z nowoczesnymi językami programowania. Obsługa serializacji dowolnych natywnych struktur danych zwiększyła czytelność plików YAML, ale nieco skomplikowała proces analizowania i generowania plików.

## Krótka historia ##

YAML został po raz pierwszy zaproponowany w 2001 roku i został opracowany przez Clarka Evansa, Ingy döt Net i Oren Ben-Kiki. Po raz pierwszy powiedziano, że YAML oznacza „jeszcze inny język znaczników”, aby wskazać jego cel jako języka znaczników. Później zmieniono jego przeznaczenie na „YAML Aint Markup Language”, aby wskazać jego cel jako zorientowany na dane.


## Format pliku YAML ##

Plik YAML składa się z następujących typów danych

- **Skalarami**: Skalary to wartości takie jak ciągi znaków, liczby całkowite, wartości logiczne itp.
- **Sekwencje**: Sekwencje to listy, w których każdy element zaczyna się od myślnika (-). Listy mogą być również zagnieżdżane.
- **Mapowania**: Mapowanie daje możliwość wylistowania kluczy wraz z wartościami.

### Składnia ###

- **Biała spacja**: Wcięcie białej spacji służy do wskazania zagnieżdżenia i ogólnej struktury.

```yaml
imię i nazwisko: John Smith
kontakt:
dom: 1012355532
biuro: 5002586256
adres zamieszkania:
ulica: |
Aleja Tornada 123
Apartament 16
miasto: East Centerville
stan: K.S
```

- **Komentarze**: Komentarze są pisane zaczynając od symbolu "#".

```yaml
# To jest komentarz YAML
```

- **Listy**: łącznik (-) jest używany do wskazania członków listy z każdym elementem w osobnym wierszu. Elementy listy można również ująć w nawiasy kwadratowe ([...]) z elementami oddzielonymi przecinkami (,).

```yaml
  - A
  - B
  - C
```

```yaml
[A,B,C]
```

- **Tablica asocjacyjna**: Tablica asocjacyjna jest otoczona nawiasami klamrowymi ({...}). Klucze i wartości są oddzielone dwukropkiem (:), a każda para jest oddzielona przecinkiem (,).

```yaml
  {name: John Smith, age: 20}
```

- **Stringi**: Ciąg można zapisać z podwójnymi cudzysłowami (") lub pojedynczymi cudzysłowami (') lub bez nich.

```yaml
Przykładowy ciąg
„Przykładowy ciąg”
„Przykładowy ciąg”
```

- **Zawartość bloku skalarnego**: Zawartość skalarną można zapisać w notacji blokowej przy użyciu:
  - **|**: All live breaks are significant.
  - **>**: Each line break is folded to space. It removes the leading whitespace for each line.

```yaml
dane: |
YAML
(YAML nie jest językiem znaczników)
jest językiem serializacji danych
```

```yaml
dane: ?
YAML (YAML nie jest językiem znaczników)
jest językiem serializacji danych
```

- **Wiele dokumentów**: Wiele dokumentów jest oddzielonych trzema myślnikami (---) w jednym strumieniu. Łączniki wskazują początek dokumentu. Łączniki są również używane do oddzielania dyrektyw od treści dokumentu. Koniec dokumentu jest oznaczony trzema kropkami (...).

```yaml
  ---
Dokument 1
  ---
Dokument 2
...
```

- **Typ**: Aby określić typ wartości, używane są podwójne wykrzykniki (!!).

```yaml
a: !!liczba zmiennoprzecinkowa 123
b: !! str. 123
```

- **Tag**: Aby przypisać znacznik do notatki, używany jest znak ampersand (&), a do odniesienia do tego węzła używana jest gwiazdka (*).

```yaml
imię i nazwisko: John Smith
płatnik: &id01
ulica: |
Aleja Tornada 123
Apartament 16
miasto: East Centerville
stan: K.S

adres dostawy: *id01
```

- **Dyrektywy**: dokumenty YAML mogą być poprzedzone dyrektywami w strumieniu. Dyrektywy zaczynają się od znaku procentu (%), po którym następuje nazwa, a następnie parametry oddzielone spacjami.

```yaml
%YAML 1.2
  ---
Treść dokumentu
```
## Przykład pliku YAML
Poniżej możesz zobaczyć **przykład pliku docker yaml**:

```
topology:
database_node_name: docker_controller
docker_controller_node_name: docker_controller
self_service_portal_node_name: docker_controller
kvm_compute_node_names: kvm_compute1
docker_compute_node_names: docker_compute1
```

## YAML kontra JSON
Zasadniczo zarówno JSON, jak i YAML zostały opracowane w celu zapewnienia czytelnego dla człowieka formatu wymiany danych. YAML jest realizowany jako nadzbiór formatu JSON. Oznacza to, że możemy analizować JSON za pomocą parsera YAML. Chociaż praktyczne wdrożenie tej teorii jest trochę trudne. Dlatego poniżej podano podstawowe różnice między YAML i JSON:

|YAML| JSON|
---|---|
|Złożony i czasochłonny proces analizowania danych serializowanych |Szybko i łatwo analizuj serializowane dane JSON dzięki prostszej konstrukcji|
|Mniejsze wsparcie społeczności| Większe wsparcie społeczności i popularność|
|Obsługuje komentarze| Nie obsługuje komentarzy|
|Umiejętność korzystania z referencji innych obiektów danych| Niemożliwe serializowanie złożonych struktur z odniesieniami do obiektów|
|Hierarchia jest oznaczona podwójnymi spacjami. Znaki tabulacji są niedozwolone|Obiekty i tablice są oznaczone nawiasami klamrowymi.|
|Cytaty w ciągu są opcjonalne, ale obsługują pojedyncze i podwójne cudzysłowy.|Cypisy muszą być w podwójnych cudzysłowach.|
|Węzeł główny może być dowolnym prawidłowym typem danych|Węzeł główny musi być tablicą lub obiektem.|


## Bibliografia ##

- [YAML - Wikipedia](https://en.wikipedia.org/wiki/YAML)
- [YAML](https://yaml.org/spec/1.2/spec.html)

