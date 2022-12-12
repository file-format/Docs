{
  "date" : "2019-12-12",
  "keywords" :["PLY", "plik", "rozszerzenie", "format", "format pliku 3D" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format pliku PLY i interfejsy API, które mogą tworzyć i otwierać pliki PLY.",
  "title" :"PLY - Wielokątny format pliku 3D",
  "linktitle" : "PLY",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik PLY?

PLY, Polygon File Format, reprezentuje format pliku 3D, który przechowuje obiekty graficzne opisane jako zbiór wielokątów. Celem tego formatu pliku było ustanowienie prostego i łatwego typu pliku, który jest wystarczająco ogólny, aby był użyteczny dla szerokiej gamy modeli. Format pliku PLY jest dostępny w formacie ASCII, a także w formacie binarnym, co zapewnia kompaktowe przechowywanie oraz szybkie zapisywanie i ładowanie. Format pliku jest używany przez różne aplikacje obsługujące odczyt plików 3D.

Obiekty w formacie PLY są opisywane przez zbiór wierzchołków, ścian i innych elementów wraz z właściwościami, takimi jak kolor i kierunek normalny, które można dołączyć do tych elementów. Inne właściwości, które mogą być również przechowywane z obiektem, obejmują:

* Normalne powierzchniowe
* współrzędne tekstury
* przejrzystość
* Zakres pewności danych
* właściwości przedniej i tylnej części wielokąta

Obiekt reprezentowany przez format PLY może być wynikiem różnych źródeł, takich jak ręcznie zdigitalizowane obiekty, obiekty wielokątne z aplikacji do modelowania, dane o zasięgu, trójkąty z maszerujących sześcianów, dane terenu i modele radiosity.

## Krótka historia

Format PLY został opracowany w latach 90-tych przez Grega Turka i innych pracowników laboratorium graficznego Stanforda i dlatego jest również znany jako Format Trójkąta Stanforda. Format pliku ma od tego czasu wersję 1.0 i nie wprowadzono żadnych dalszych modyfikacji.

## Format pliku PLY

Prosty obiekt PLY składa się ze zbioru elementów do reprezentacji obiektu. Składa się z listy (x, y, z) trójek wierzchołków i listy ścian, które w rzeczywistości są indeksami na liście wierzchołków. Wierzchołki i ściany to dwa przykłady elementów, a większość pliku PLY składa się z tych dwóch elementów. Można również tworzyć nowe właściwości i dołączać je do elementów obiektu, ale należy je dodawać w taki sposób, aby stare programy nie ulegały awarii w przypadku napotkania tych nowych właściwości. Takie właściwości można również odrzucić, czytając aplikacje. Ponadto za pomocą tego elementu można tworzyć nowe elementy i definiować właściwości.

### Struktura plików

Struktura plików w formacie PLY jest następująca:

|Pole
---|
|Nagłówek pliku
|Lista wierzchołków
|Lista twarzy
|Lista innych elementów

#### Przykładowa struktura

Użyjemy poniższego przykładu w naszej dalszej dyskusji na temat różnych części formatu pliku PLY.

```
ply
format ascii 1.0           { ascii/binary, format version number }
comment made by Greg Turk  { comments keyword specified, like all lines }
comment this file is a cube
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
element face 6             { there are 6 "face" elements in the file }
property list uchar int vertex_index { "vertex_indices" is a list of ints }
end_header                 { delimits the end of the header }
0 0 0                      { start of vertex list }
0 0 1
0 1 1
0 1 0
1 0 0
1 0 1
1 1 1
1 1 0
4 0 1 2 3                  { start of face list }
4 7 6 5 4
4 0 4 5 1
4 1 5 6 2
4 2 6 7 3
4 3 7 4 0
```

#### Nagłówek pliku

Nagłówek formatu pliku PLY składa się z tekstu ASCII zarówno dla formatu ASCII, jak i binarnego. Początek i koniec sekcji nagłówka jest identyfikowany przez słowa kluczowe warstwy i końca nagłówka. Na początku nagłówka znajduje się magiczne słowo ply, które służy do rozpoznawania formatu pliku PLY przez czytniki. Następny wiersz pokazuje numer wersji tego pliku. Komentarze w formacie pliku PLY zaczynają się od słowa kluczowego komentarza na początku każdego wiersza komentarza.

#### Słowo kluczowe elementu

Słowo kluczowe element mówi następnie, co znajduje się w pliku. Po nim następują właściwości dla tego konkretnego typu elementu, gdzie każda właściwość ma swój typ właściwości i kolejność określoną, jak pokazano poniżej:

```
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
```

W tym konkretnym przykładzie określony element wierzchołka ma 3 właściwości typu float z określoną kolejnością.

#### Typy typów danych

Istnieją dwa typy typów danych, które może mieć właściwość.

`Scalar`: Skalarne typy danych są pokazane poniżej:

|#Nazwa|#Typ|#Liczba bajtów
|znak|znak|1
|uchar|znak bez znaku|1
|krótka|krótka liczba całkowita|2
|krótka|krótka liczba całkowita bez znaku|2
|int|liczba całkowita|4
|uint|liczba całkowita bez znaku|4
|float|liczba zmiennoprzecinkowa pojedynczej precyzji|4
|podwójny|pływak o podwójnej precyzji|8

`Lista`: Istnieje specjalna forma definicji właściwości, która wykorzystuje typ danych listy. Przykładem tego jest powyższy plik kostki:

`lista właściwości uchar int vertex_index`

Oznacza to, że właściwość „vertex_index” zawiera najpierw znak bez znaku wskazujący, ile indeksów zawiera właściwość, a następnie listę zawierającą tyle liczb całkowitych. Każda liczba całkowita na tej liście o zmiennej długości jest indeksem wierzchołka.

## Bibliografia ##

* [Format pliku PLY](http://paulbourke.net/dataformats/ply/)
* [PLY – z Wikipedii](https://en.wikipedia.org/wiki/PLY_(file_format))

