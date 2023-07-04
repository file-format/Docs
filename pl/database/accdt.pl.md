{
  "date" : "2020-11-11",
  "keywords" :["ACCDT", "rozszerzenie", "plik", "format pliku", "Typ pliku bazy danych", "Format pliku bazy danych", "Pliki bazy danych" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format pliku ACCDT i interfejsy API, które mogą tworzyć i otwierać pliki ACCDT.",
  "title" :"ACCDT — format pliku bazy danych szablonów programu Microsoft Access 2007",
  "linktitle" : "ACCDT",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-12"
}

## Czym jest plik ACDT?

Plik z rozszerzeniem .accdt to plik szablonu bazy danych programu Microsoft Access, który zawiera predefiniowane elementy bazy danych. Elementy te są zbiorem struktur, które definiują aplikacje bazy danych, takie jak schematy bazy danych do przechowywania danych, opis układu widoków danych oraz metadane opisujące bazę danych. Będąc plikami szablonów, pliki ACCDT mogą być używane do tworzenia baz danych na podstawie dostępnych w nich ustawień szablonów. Wynikowe pliki bazy danych są zapisywane jako pliki [ACCDB](/pl/database/accdb/) i wypełniane danymi w tabelach. Microsoft Access 2007 i nowsze mogą otwierać pliki ACCDT.

## Format pliku ACCDT

Pliki szablonów ACCDT są oparte na specyfikacjach Office Open XML, a wszystkie dane są zawarte w pakiecie ZIP. Informacje o strukturze i zawartości bazy danych są zawarte w plikach [XML](/pl/web/xml/) i plikach tekstowych i są ze sobą powiązane za pomocą relacji. Możesz zmienić nazwę pliku ACCDT na rozszerzenie [.zip](/pl/compression/zip/) i użyć dowolnego oprogramowania do kompresji, aby wyodrębnić zawartość archiwum ZIP.

### Struktura plików

Pliki ACCDT to pakiety zawierające kolekcję powiązanych części. Każda **część** przechowuje informacje o zawartości aplikacji bazy danych przy użyciu formatów XML, tekstowych i binarnych, które obejmują:

* Obiekty bazy danych
* Powiązane metadane
* Struktura pakietu

#### Pakiet

Pakiet to archiwum [ZIP](/pl/compression/zip/), które zawiera wiele części i jest zgodne z konwencjami otwartego pakowania określonymi w [ISO/IEC-29500-2](https://www.iso.org/standard/51459.html). Pliki ACCDT muszą zawierać co najmniej jedną część metadanych szablonu, która powinna być celem relacji. Te metadane szablonu są początkową częścią pliku ACCDT.

#### Część

Część to strumień bajtów, który ma powiązany typ określający naturę i typ przechowywanej w nim treści. Wyliczanie części określa prawidłowe części, prawidłowe typy zawartości i wymagane relacje między wszystkimi częściami w pakiecie.

#### Relacja

`Package Relationship` - gdzie cel jest częścią, a źródłem jest pakiet jako całość.

`Part-to-Part Relationship` - gdzie celem jest część, a źródłem jest część w pakiecie.

`Jawna relacja` - gdzie odwołanie do zasobu pochodzi z zawartości części źródłowej poprzez odniesienie do elementu relacji przez wartość jego atrybutu ID.

`Ukryty związek` - związek, który nie jest jawny.

`Wewnętrzna relacja` - gdzie celem jest część w pakiecie.

`Związek zewnętrzny` - gdzie celem jest zasób zewnętrzny, którego nie ma w pakiecie.

## Bibliografia ##

* [Format pliku szablonu dostępu](https://docs.microsoft.com/en-us/openspecs/sharepoint_protocols/ms-accdt/0a4a68d7-7a85-4a27-ad74-730db57862d7)

