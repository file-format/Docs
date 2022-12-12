{
  "date" : "2019-10-11",
  "keywords" :[ "JAR", ".jar", "co to jest plik jar", "jak otworzyć plik jar", "rozszerzenie", "plik", "plik jar", "format pliku jar", "rozszerzenie .jar " ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JAR - format pliku archiwum Java",
  "description":"Poznaj format pliku JAR i interfejsy API, które mogą tworzyć i otwierać plik JAR.",
  "linktitle" : "JAR",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Co to jest plik JAR?

Plik z rozszerzeniem .jar to plik archiwum Java, który zawiera wiele różnych plików związanych z aplikacjami w jednym pliku. Ten format pliku został stworzony, aby zmniejszyć szybkość ładowania pobranego apletu Java w przeglądarce za pośrednictwem transakcji HTTP, unikając tworzenia wielu połączeń HTTP. Pojedynczy plik JAR może zawierać pliki klas Java ([.class](/pl/programming/class/)), [obrazy](/pl/image/) i [dźwięki](/pl/audio/). Poszczególne elementy w pliku JAR mogą być podpisane cyfrowo przez twórcę aplikacji w celu uwierzytelnienia ich pochodzenia. Pliki JAR są regularnie używane do tworzenia funkcjonalnych interfejsów API, które zawierają określone funkcje związane z tym interfejsem API.

## Format pliku JAR

Pliki JAR są oparte na popularnym [formacie pliku ZIP](/pl/compression/zip/), który archiwizuje poszczególne pliki zawartości w jednym pliku. Format pliku JAR obsługuje kompresję, co skutkuje mniejszym rozmiarem pliku do pobrania, a tym samym jeszcze bardziej skraca czas pobierania. Artykuł [Specyfikacja plików JAR](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) firmy Oracle zawiera szczegółowe informacje na temat wewnętrznych specyfikacji plików JAR.

### Plik manifestu

Podczas tworzenia pliku JAR automatycznie tworzony jest w nim plik manifestu, który zawiera metadane dotyczące zawartości pliku JAR. Ten plik pokazuje zawartość spakowaną w pliku JAR. Typowy plik Manifest wygląda następująco, który pokazuje foldery i klasy zawarte w pliku JAR.

```
META-INF/
META-INF/MANIFEST.MF
pack/
pack/class1.class
pack/class2.class
..
..
```

#### Specyfikacje manifestu

Specyfikacje Manifestu są zdefiniowane przez Oracle w następujący sposób.

`plik-manifestu`: nowa linia sekcji głównej \*sekcja-indywidualna

`main-section`: informacja o wersji nowa linia \*atrybut główny

`Informacje o wersji`: Manifest-Version : numer wersji

`numer-wersji` : cyfra+{.cyfra+}*

`atrybut główny`: (dowolny prawidłowy atrybut główny) nowy wiersz

`indywidualna-sekcja`: Nazwa: wartość nowej linii \*atrybut-perentry

`perentry-atrybut`: (dowolny prawidłowy atrybut perentry) nowa linia

`nowa linia` : CR LF | LF | CR (bez LF)

`digit`: {0-9}

### Wykonywalny plik JAR

Pliki JAR mogą również zawierać aplikację, która może być wykonywana przez wirtualną maszynę Java (JVM), podobnie jak każda inna aplikacja w systemie operacyjnym Microsoft Windows. W takim przypadku JVM musi wiedzieć o punkcie wejścia aplikacji, którym jest dowolna klasa z publiczną metodą static void main. Plik manifestu identyfikuje taką klasę z nagłówkiem `Main-Class` w następującym formacie:

```
Main-Class: com.example.MyClassName
```



## Bibliografia

* [Omówienie pliku JAR](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jarGuide.html)
* [Format pliku JAR](https://en.wikipedia.org/wiki/JAR_(file_format)#:~:text=A%20JAR%20(Java%20ARchive)%20is,into%20one%20file%20for% 20dystrybucja.&text=One%20są%20zbudowane%20na%20rozszerzeniu,jar%20file%20.)

