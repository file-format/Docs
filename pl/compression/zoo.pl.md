{
"data": "2023-11-09",
   "keywords":[
"ogród zoologiczny",
"plik zoo",
"skompresowany plik zoo",
"jak otworzyć plik zoo",
"plik",
"rozszerzenie pliku zoo",
"rozszerzenie",
"plik"
],
   "author":{
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title":"Plik ZOO - Co to jest plik .zoo i jak go otworzyć?",
   "description":"Dowiedz się o formacie pliku skompresowanego ZOO i interfejsach API, które umożliwiają tworzenie i otwieranie plików ZOO.",
"linktitle":"ZOO",
   "menu":{
      "docs":{
         "identifier":"compression-zoo",
         "parent":"compression"
}
},
"lastmod":"2023-11-09"
}

## Czym jest plik ZOO?

Plik `.zoo` to format archiwum używany do kompresji i przechowywania plików i katalogów; jest podobny do innych formatów archiwów, takich jak `.zip`, `.tar` i `.rar`. Format `.zoo` był popularny w początkach informatyki, ale w ostatnich latach stał się mniej powszechny. Został pierwotnie opracowany przez **Rahul Dhesi** i był używany głównie w systemach Unix i DOS.

Plik `.zoo` zazwyczaj zawiera jeden lub więcej plików i katalogów, które zostały skompresowane i zarchiwizowane w jednym pliku. Możesz tworzyć i rozpakowywać pliki `.zoo` przy użyciu różnych narzędzi programowych obsługujących ten format.

Archiwa ZOO mają unikalną funkcję, która pozwala na przechowywanie wielu wersji tego samego pliku, pod warunkiem, że każda wersja została zmodyfikowana w innym dniu. Oznacza to, że użytkownicy ZOO mogą zapisywać i otwierać poprzednie wersje pliku bezpośrednio z archiwum ZOO. Ta funkcja umożliwia użytkownikom powrót do wcześniejszej wersji pliku lub porównanie starszej wersji z nowszą, oferując wygodny sposób zarządzania wersjami plików i zmianami w czasie.

## Typowe operacje na plikach ZOO

Oto kilka typowych operacji związanych z plikami `.zoo`:

1. **Tworzenie pliku `.zoo`:** Do utworzenia pliku `.zoo` możesz użyć narzędzia wiersza poleceń, takiego jak "zoo". Na przykład następujące polecenie utworzy archiwum `.zoo` z katalogu:
    








`zoo a -c katalog Archive.zoo/`
    








W tym poleceniu "a" oznacza "add", "-c" określa kompresję, a "archive.zoo" to nazwa archiwum wyjściowego.
    








2. **Wyodrębnianie plików z pliku `.zoo`:** Aby wyodrębnić zawartość archiwum `.zoo`, możesz użyć następującego polecenia:
    








`zoo i archiwum.zoo`
    








To polecenie wyodrębni pliki z pliku `archive.zoo`.
    








3. **Lista zawartości pliku `.zoo`:** Możesz wyświetlić zawartość archiwum `.zoo` bez jego rozpakowywania, używając opcji "l":
    








    








`zoo l archiwum.zoo`

## Jak otworzyć plik ZOO?

Programy otwierające pliki ZOO obejmują

- **zoo** (bezpłatny) dla (Windows, Linux)

## Bibliografia
* [Zoo (file format)](https://en.wikipedia.org/wiki/Zoo_(file_format))
