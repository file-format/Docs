{
  "date" : "2019-10-11",
  "keywords" :[ "klasa", ".klasa", "co to jest plik klasy", "jak otworzyć plik klasy", "rozszerzenie", "plik", "plik klasy", "format pliku klasy", "rozszerzenie .klasy ", "plik klasy w Javie" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Klasa - Format pliku klasy Java",
  "description":"Dowiedz się o formacie plików klas i interfejsach API, które mogą tworzyć i otwierać pliki klas.",
  "linktitle" : "Class",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Co to jest plik klasy?

**Plik klasy w Javie** to skompilowane dane wyjściowe klasy [.java](/pl/programming/java/), które są faktycznie wykonywane przez wirtualną maszynę Java (JVM). Pliki klas mogą być uruchamiane indywidualnie, jak również mogą być częścią pliku [JAR](/pl/programming/jar/) jako pakiet wraz z innymi plikami pakietów. Można je utworzyć za pomocą polecenia **`javac`** z interfejsu wiersza poleceń. Niektóre środowiska Java IDE, takie jak [Eclipse](https://www.eclipse.org/downloads/packages/release/2020-06/r/eclipse-ide-java-developers) i NetBeans umożliwiają tworzenie plików wyjściowych .class z Javy projektu akta.

## Format pliku klasy

Plik klasy Java składa się z kodu bajtowego, który jest kodem pośrednim do uruchomienia przez JVM. Plik klasy składa się ze strumienia 8-bitowych bajtów, a wielobajtowe elementy danych są zawsze przechowywane w kolejności big-endian.

### Struktura pliku klasy

Struktura plików klas jest pokazana poniżej.
```
ClassFile {
    u4             magic;
    u2             minor_version;
    u2             major_version;
    u2             constant_pool_count;
    cp_info        constant_pool[constant_pool_count-1];
    u2             access_flags;
    u2             this_class;
    u2             super_class;
    u2             interfaces_count;
    u2             interfaces[interfaces_count];
    u2             fields_count;
    field_info     fields[fields_count];
    u2             methods_count;
    method_info    methods[methods_count];
    u2             attributes_count;
    attribute_info attributes[attributes_count];
}
```
gdzie:

* u1 = jednobajtowa ilość bez znaku
* u2 = liczba dwubajtowa bez znaku
* u4 = liczba czterobajtowa bez znaku

Szczegóły struktury pliku .class zostały również wyjaśnione w Oracle [format pliku klasy](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html) i można się do nich odnieść przez deweloperzy w celach informacyjnych. Podsumowanie tych pól jest następujące.

* `magic` - magiczny przedmiot dostarcza magiczną liczbę identyfikującą format pliku klasy; ma wartość 0xCAFEBABE.
* `minor_version`, `major_version` - Wartości elementów minor_version i major_version to numery wersji drugorzędnej i głównej tego pliku klasy.
* `constant_pool_count` - Wartość elementu fixed_pool_count jest równa liczbie wpisów w tabeli fixed_pool plus jeden. Indeks fixed_pool jest uważany za prawidłowy, jeśli jest większy od zera i mniejszy niż const_pool_count, z wyjątkiem stałych typu long i double.
* `constant_pool[]` - Constant_pool to tabela struktur (§4.4) reprezentujących różne stałe łańcuchowe, nazwy klas i interfejsów, nazwy pól i inne stałe, do których odnosi się struktura ClassFile i jej struktury podrzędne. Format każdego wpisu tabeli fixed_pool jest wskazywany przez jego pierwszy bajt „znacznika”.
* `access_flags` - Wartość elementu access_flags jest maską flag używaną do oznaczania uprawnień dostępu i właściwości tej klasy lub interfejsu.
* `this_class` — wartość elementu this_class musi być poprawnym indeksem w tabeli puli stałej.
* `super_class` — dla klasy wartość elementu super_class musi wynosić zero lub musi być prawidłowym indeksem w tabeli puli_stałej.
* `interfaces_count` - Wartość elementu interfaces_count podaje liczbę bezpośrednich superinterfejsów tej klasy lub typu interfejsu.
* `interfaces[]` - Każda wartość w tablicy interfaces musi być poprawnym indeksem w tabeli fixed_pool.
* `fields_count` - Wartość elementu Fields_count określa liczbę struktur field_info w tabeli pól.
* `fields[]` - Każda wartość w tabeli pól musi być strukturą field_info podającą pełny opis pola w tej klasie lub interfejsie.
* `methods_count` - Wartość elementu Methods_count podaje liczbę struktur method_info w tabeli metod.
* `methods[]` - Każda wartość w tabeli metod musi być strukturą method_info podającą pełny opis metody w tej klasie lub interfejsie. Jeśli żadna z flag ACC_NATIVE i ACC_ABSTRACT nie jest ustawiona w elemencie access_flags struktury method_info, dostarczane są również instrukcje Java Virtual Machine implementujące metodę.
* `attributes_count` - Wartość elementu attributes_count podaje liczbę atrybutów (§4.7) w tabeli atrybutów tej klasy.
* `attributes[]` - Każda wartość tabeli atrybutów musi być strukturą attribute_info.




## Bibliografia

* [Format pliku klasy](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html)

