{
  "date" : "2019-10-11",
  "keywords": [ "mf file", "mf", "extension", "format", "mf file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MF — format pliku manifestu Java",
  "description":"Poznaj format plików MF i interfejsy API, które mogą tworzyć i otwierać pliki MF.",
  "linktitle" : "MF",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Czym jest plik MF?

Plik z rozszerzeniem .mf to plik manifestu Java, który zawiera informacje o poszczególnych wpisach w pliku [JAR](/pl/programming/jar/). Sam plik MF jest zawarty w pliku JAR i zawiera wszystkie definicje związane z rozszerzeniami i pakietami. Pliki JAR mogą być tworzone do użycia jako plik wykonywalny. W takim przypadku plik mainfest określa główną klasę aplikacji, która zawiera instrukcję **`public static void main`**. Pliki manifestu mają nazwę MANIFEST.MF i można je otwierać za pomocą dowolnego edytora tekstu w systemach operacyjnych Windows, MacOS i Linux.

## Specyfikacje formatu pliku manifestu

[Specyfikacje formatu plików manifestu](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) są dostępne przez firmę Oracle w jej przewodniku dotyczącym formatu plików JAR. Plik manifestu składa się z głównych sekcji, po których następuje lista sekcji dla poszczególnych wpisów pliku JAR. Każda sekcja podlega pewnym zasadom i ograniczeniom.

### Główne sekcje

Główna sekcja:

* zawiera informacje dotyczące bezpieczeństwa i konfiguracji pliku JAR
* zawiera informacje o aplikacji lub rozszerzeniu, którego częścią jest plik JAR
* definiuje główne atrybuty dla każdego pojedynczego elementu manifestu

**Uwaga**: żaden atrybut w tej sekcji nie może mieć nazwy „Nazwa”.

### Poszczególne sekcje

Pojedyncza sekcja definiuje różne atrybuty dla pakietów lub plików pliku JAR. Każda sekcja musi zaczynać się od atrybutu o nazwie „Nazwa”, którego wartością musi być ścieżka względna do pliku lub bezwzględny adres URL odnoszący się do danych poza archiwum.

### Specyfikacje manifestu

|Atrybuty|Opis|
---|---|
|plik-manifestu|sekcja-główna nowa linia *sekcja-indywidualna|
|sekcja-główna|informacje-o-wersji nowy wiersz *atrybut-główny|
|informacje o wersji|Manifest-Wersja : numer-wersji|
|numer-wersji|cyfra+{.cyfra+}*|
|atrybut-główny|(dowolny prawidłowy atrybut główny) nowa linia|
|sekcja-indywidualna|Nazwa: wartość nowej linii *atrybut-wpisu|
|atrybut_perentry|(dowolny poprawny atrybut perentry) nowa linia|
|nowa linia|CR LF | LF | CR (bez LF)|
|cyfra|{0-9}|

## Bibliografia

* [Oracle — format pliku JAR](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html)
* [Format pliku JAR](https://en.wikipedia.org/wiki/JAR_(file_format)#:~:text=A%20JAR%20(Java%20ARchive)%20is,into%20one%20file%20for% 20dystrybucja.&text=One%20są%20zbudowane%20na%20rozszerzeniu,jar%20file%20.)

