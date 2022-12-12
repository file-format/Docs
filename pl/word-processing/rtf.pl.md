{
  "date" : "2019-10-11",
  "keywords" :[ "plik rtf", "format pliku rtf", "co to jest plik rtf", "plik", "przykład rtf", "rozszerzenie pliku rtf", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RTF - format tekstu sformatowanego",
  "description":"Poznaj format plików RTF i interfejsy API, które mogą tworzyć i otwierać pliki RTF.",
  "linktitle" : "RTF",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik RTF?

Wprowadzony i udokumentowany przez firmę Microsoft format tekstu sformatowanego (**RTF**) reprezentuje metodę kodowania sformatowanego tekstu i grafiki do użytku w aplikacjach. Format ułatwia międzyplatformową wymianę dokumentów z innymi produktami firmy Microsoft, służąc w ten sposób interoperacyjności. Ta funkcja sprawia, że jest to standard przesyłania danych między programami do edycji tekstu, dzięki czemu zawartość może być przenoszona z jednego systemu operacyjnego do drugiego bez utraty formatowania dokumentu. Specyfikacje formatu plików są dostępne przez firmę Microsoft do [pobrania](https://www.microsoft.com/en-us/download/details.aspx?id#10725) i można się do nich odwoływać z perspektywy programisty.

## Krótka historia formatu plików RTF ##

Format pliku RTF przeszedł kilka zmian od czasu jego publikacji. Jego oficjalna wersja do odczytu/zapisu została opublikowana jako część programu Microsoft Word 3.0 dla komputerów Macintosh ze specyfikacją wersji 1.0. Ostateczna wersja specyfikacji, 1.9.1, została opublikowana przez firmę Microsoft w marcu 2008 r. Od tego czasu nie wprowadza się już żadnych ulepszeń specyfikacji. Obecnie prawie wszystkie systemy operacyjne mają bogatsze w funkcje aplikacje, które zminimalizowały/wyeliminowały użycie formatu plików RTF.

## Specyfikacje formatu pliku RTF ##

RTF służy jako standard przesyłania danych między programami do edycji tekstu i przesyłania treści z jednego systemu operacyjnego do drugiego. Osiąga się to za pomocą słów kontrolnych, które zostały wprowadzone przez Microsoft Office Word do 2007 roku. Standardowy plik RTF składa się z ASCII reprezentującego tekst sformatowany oraz ze znaków innych niż ASCII, które są konwertowane na odpowiednie wartości kodowe. Nowsze wersje programu Word mogą odczytywać pliki RTF wygenerowane w poprzednich wersjach, podczas gdy starsze wersje ignorują słowa kontrolne i grupy, których nie rozumieją.

### Zrozumienie podstaw formatu RTF ###

Pliki RTF używają 7-bitowego zwykłego tekstu ASCII, składającego się z:

* słowa kontrolne
* symbole kontrolne i
* grupy.

Działają one jako elementy składowe do reprezentacji danych RTF jako zrozumiałego tekstu i kodowania znaków.

#### Słowo kontrolne ####

Reprezentują one specjalnie sformatowane polecenia używane do oznaczania znaków do wyświetlenia i nie mogą być dłuższe niż 32 litery. Słowo kontrolne jest definiowane przez:

\<ASCII Letter Sequence> //<//Delimiter//> //

W każdym słowie kontrolnym rozróżniana jest wielkość liter i zaczyna się od ukośnika odwrotnego. Sekwencja liter ASCII może zawierać alfabety ASCII (od a do z oraz od A do Z). The<Delimite> oznacza koniec nazwy słowa kontrolnego i może być jednym z następujących:

* Przestrzeń. Służy to jedynie do odgraniczenia słowa kontrolnego i jest ignorowane w dalszym przetwarzaniu.
* Cyfra numeryczna lub znak minus ASCII, który wskazuje, że parametr numeryczny jest powiązany ze słowem sterującym. Kolejna cyfrowa sekwencja jest następnie ograniczana przez dowolny znak inny niż cyfra ASCII (zwykle inne słowo kontrolne rozpoczynające się ukośnikiem odwrotnym). Parametr może być dodatnią lub ujemną liczbą dziesiętną. Zakres wartości dla liczby jest nominalnie od –32768 do 32767, tj. 16-bitowa liczba całkowita ze znakiem. Niewielka liczba słów kontrolnych przyjmuje wartości z zakresu od -2 147 483 648 do 2 147 483 647 (32-bitowa liczba całkowita ze znakiem). Te słowa kontrolne obejmują słowa kontrolne powiązane z **\binN**, **\revdttmN//**, **\rsidN** oraz niektóre właściwości obrazu, takie jak **\bliptagN**. Tutaj **N** oznacza parametr numeryczny. Parser RTF musi dopuszczać do 10 cyfr opcjonalnie poprzedzonych znakiem minus. Jeśli separatorem jest spacja, jest on odrzucany, to znaczy nie jest uwzględniany w dalszym przetwarzaniu.
* Dowolny znak inny niż litera lub cyfra. W tym przypadku znak ograniczający kończy słowo kontrolne i nie jest częścią słowa kontrolnego. Na przykład ukośnik odwrotny „\”, co oznacza, że następuje nowe słowo kontrolne lub symbol kontrolny.

#### Symbol kontrolny ####

Symbol kontrolny reprezentuje specjalne wystąpienie, które ma określone znaczenie w zależności od jego zawartości. Składa się z ukośnika odwrotnego, po którym następuje znak specjalny (znak niealfabetyczny) i nie ma żadnych ograniczników.

#### Grupa ####

Grupa może składać się z tekstu, słów kontrolnych lub symboli kontrolnych ujętych w nawiasy klamrowe (**{ }**). Nawias otwierający (**{** ) wskazuje początek grupy, a nawias zamykający ( **}**) wskazuje koniec grupy. Każda grupa określa tekst, na który ma wpływ grupa, oraz różne atrybuty tego tekstu.

### Struktura pliku RTF ###

Plik RTF ma następującą standardową składnię:

Wprowadzony i udokumentowany przez firmę Microsoft format tekstu sformatowanego (**RTF**) reprezentuje metodę kodowania sformatowanego tekstu i grafiki do użytku w aplikacjach. Format ułatwia międzyplatformową wymianę dokumentów z innymi produktami firmy Microsoft, służąc w ten sposób interoperacyjności. Ta funkcja sprawia, że jest to standard przesyłania danych między programami do edycji tekstu, dzięki czemu zawartość może być przenoszona z jednego systemu operacyjnego do drugiego bez utraty formatowania dokumentu. Specyfikacje formatu plików są dostępne przez firmę Microsoft do [pobrania](https://www.microsoft.com/en-us/download/details.aspx?id#10725) i można się do nich odwoływać z perspektywy programisty.

#### Nagłówek RTF ####

Nagłówek RTF ma następującą reprezentację.

|Pole|Opis
---|---|
|\<header> |**\rtf1\fbidis**? \<character set> \<from> ? \<deffont> \<deflang> \<fonttbl> ? \<filetbl> ? \<colortbl> ? \<stylesheet> ? \<stylerestrictions> ? \<listtables> ? \<revtbl> ? \<rsidtable> ? \<mathprops> ? \<generator> ?

Tabele nagłówków muszą pojawiać się w tej kolejności, jeśli istnieją. Plik RTF może zawierać grupy czcionek, stylów, kolorów ekranu, obrazów, przypisów, komentarzy (adnotacji), nagłówków i stopek, informacji podsumowujących, pól, zakładek, właściwości formatowania dokumentów, sekcji, akapitów i znaków, matematyki, obrazy i obiekty. Jeśli plik zawiera czcionkę, plik, styl, kolor, znak rewizji i grupy informacji podsumowujących oraz właściwości formatowania dokumentu, muszą one pojawić się w nagłówku RTF, który poprzedza treść RTF. Jeśli zawartość jakiejkolwiek grupy nie jest używana, grupę można pominąć. Każda grupa, która używa właściwości zdefiniowanych w innej grupie, musi występować po grupie, która definiuje te właściwości. Na przykład właściwości koloru i czcionki muszą poprzedzać grupę stylów.

#### Wersja RTF ####

Dokument RTF musi zaczynać się od tych sześciu znaków:

```
{\rtf1
```
gdzie 1 oznacza numer wersji RTF.

#### Zestaw znaków ####

Po {\rtf1 dokument powinien zadeklarować jakiego zestawu znaków używa. Sposobem na zadeklarowanie zestawu znaków jest użycie jednego z następujących poleceń:

`\ansi` — dokument jest zapisany w zestawie znaków ANSI, znanym również jako strona kodowa 1252, typowym zestawie znaków systemu MSWindows.

`\mac` — dokument jest w zestawie znaków MacAscii, typowym zestawie znaków w starych wersjach systemu Mac OS (sprzed 10).

`\pc` — dokument jest w DOS Code Page 437, domyślnym zestawie znaków dla MS-DOS. Maszynistki z dobrą pamięcią mięśniową zauważą, że jest to zestaw znaków, który jest nadal używany do interpretacji kodów „Alt numerycznych” — tzn. gdy przytrzymasz Alt i wpiszesz „130” na klawiaturze numerycznej, pojawi się é, ponieważ znak 130 w CP437 to é. To chyba jedyne zastosowanie, jakie obecnie widzi CP437.

`\pca` — dokument jest na stronie kodowej DOS 850, znanej również jako wielojęzyczna strona kodowa MS-DOS.

#### Czcionka Polecenie ####

Po definicji zestawu znaków następuje polecenie `\deffN`. To określa, że czcionka o numerze N jest domyślną czcionką dla tego dokumentu. Numer czcionki N pochodzi z tabeli czcionek. Polecenie `\deffN` jest technicznie opcjonalne, ale powinno być po bezpiecznej stronie, ponieważ wspólny prolog, taki jak poniższy, wybiera czcionkę 0 jako czcionkę domyślną.

`{\rtf1\ansi\deff0`

#### Tabela czcionek ####

Wszystkie czcionki, których można użyć w dokumencie, są wymienione w tabeli czcionek, w której każda czcionka jest reprezentowana przez numer czcionki. Dokument musi mieć tabelę czcionek, chociaż niektóre programy również będą działać bez niej.

Składnia tabeli czcionek to {\fonttbl //...deklaracje//...}, w której każda deklaracja ma następującą podstawową składnię:

`{\fnumber\familycommand Nazwa czcionki;}`

Tabela czcionek z czterema deklaracjami wygląda następująco:

```
{\fonttbl
{\f0\froman Times;}
{\f1\fswiss Arial;}
{\f2\fmodern Courier New;}
}
```

W dokumencie z tą tablicą czcionek, `{\f2 rzeczy}` wydrukuje "rzeczy" w Courier New. Czcionki nie można użyć w dokumencie, dopóki nie zostanie wymieniona w tabeli czcionek.

### Koniec dokumentu ###

Każdy dokument RTF musi kończyć się znakiem }, aby zamknąć grupę otwartą przez znak {, który jest pierwszym znakiem w dokumencie. Nic nie może następować po końcowym }, z wyjątkiem być może nowej linii.

## Bibliografia ##

* [Specyfikacje RTF 1.9.1](https://www.microsoft.com/en-us/download/details.aspx?id#10725)
* [Rich_Text_Format](https://en.wikipedia.org/wiki/Rich_Text_Format)

