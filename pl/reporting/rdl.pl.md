{
  "date" : "2021-03-01",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RDL - plik języka definicji raportu",
  "keywords" :["rdl", "język definicji raportu", "XmlTextWriter", "XSD", "element RDL"],
  "description":"Poznaj format pliku RDL, który jest reprezentacją XML definicji raportu SQL Server Reporting Services.",
  "linktitle" : "RDL",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-01"
}

## Czym jest plik RDL? ##

RDL (Report Definition Language) to wzorzec ustalony przez firmę Microsoft do definiowania raportów. Plik RDL składa się z jednego lub wielu elementów RDL. Podczas gdy element RDL składa się z jego typu danych i liczności. Element może być prosty lub złożony. Element prosty nie ma żadnych elementów podrzędnych ani atrybutów, podczas gdy element złożony ma elementy podrzędne i atrybuty opcjonalne.

## Definicja schematu RDL XML
Plik definicji schematu XML (XSD) sprawdza poprawność pliku RDL. Schemat definiuje reguły określające, gdzie elementy RDL mogą występować w pliku .rdl. Element RDL może być prosty lub złożony. Prosty element nie ma elementów podrzędnych ani atrybutów, a element złożony ma elementy podrzędne i opcjonalnie atrybuty.

## Tworzenie RDL
Ponieważ RDL jest z natury otwarty i rozszerzalny, można zbudować wiele aplikacji i narzędzi, które generują pliki RDL na podstawie swojego schematu XML. Jednym z najprostszych sposobów tworzenia RDL z aplikacji jest użycie klas Microsoft .NET Framework przestrzeni nazw **System.Xml** i przestrzeni nazw System.Linq. W szczególności klasa **XmlTextWriter** może służyć do pisania języka RDL. Możesz wygenerować pełną definicję raportu od początku do końca w dowolnej aplikacji .NET Framework za pomocą **XmlTextWriter**. Deweloperzy mogą również dodawać niestandardowe elementy raportu z niestandardowymi właściwościami, aby rozszerzyć RDL.

## Typy RDL
W poniższej tabeli wymieniono typy i atrybuty używane w elementach RDL.

|Typ|Opis|
---|---|
|Binary |Właściwość z wartością binarną zakodowaną w formacie base-64.|
|Boole'a| Właściwość z prawdą lub fałszem jako wartością obiektu. O ile nie określono inaczej, wartością pominiętego opcjonalnego obiektu logicznego jest False.|
|Data |Właściwość z w pełni określoną wartością daty lub daty i godziny określoną w formacie daty ISO8601: RRRR-MM-DD[THH:MM[:SS[.S]]].|
|Wyliczenie |Właściwość z wartością tekstową typu string, która musi być jedną z listy wyznaczonych wartości.|
|Float |Właściwość z wartością zmiennoprzecinkową. Kropka (.) jest używana jako opcjonalny separator dziesiętny.|
|Liczba całkowita |Właściwość z wartością całkowitą (int32).|
|Język |Właściwość z wartością tekstową zawierającą kod języka i kultury, na przykład „en-us” dla języka angielskiego (USA). Wartość musi być określonym językiem lub językiem neutralnym, dla którego zdefiniowano język domyślny w programie Microsoft .NET Framework.|
|Nazwa |Właściwość z wartością tekstową typu string. Nazwy muszą być unikalne w przestrzeni nazw elementu. Jeśli nie określono, przestrzeń nazw dla elementu jest najbardziej wewnętrznym obiektem zawierającym, który ma nazwę.|
|NormalizedString |Właściwość ze znormalizowaną wartością tekstową typu string.|
|Rozmiar |Element rozmiaru musi zawierać liczbę (z kropką jako opcjonalnym separatorem dziesiętnym). Po numerze musi następować oznaczenie jednostki długości CSS, takie jak cm, mm, in, pt lub pc. Spacja między liczbą a oznaczeniem jest opcjonalna. Więcej informacji na temat oznaczników rozmiaru można znaleźć w artykule CSS Values and Units Reference. W języku RDL maksymalna wartość parametru Rozmiar wynosi 160 cali. Minimalny rozmiar to 0 cali.|
|String |Właściwość z wartością tekstową typu string.|
|UnsignedInt |Właściwość z wartością całkowitą bez znaku (uint32).|
|Wariant |Właściwość z dowolnym prostym typem XML.|

## Typy danych RDL
W języku RDL DataType Enumeration definiuje typ danych atrybutu, wyrażenia lub parametru. W poniższej tabeli pokazano, jak typy danych CLR odpowiadają typom danych RDL.

|Typy CLR |Odpowiadające typy danych|
---|---|
|Boole'a| Wartość logiczna|
|DataCzas, Przesunięcie daty i godziny |DataCzas|
|Int16, Int32, UInt16, Byte, SByte |Integer|
|Pojedynczy, Podwójny |Pływający|
|Ciąg, Znak, GUID, Zakres czasu |Ciąg|


## Bibliografia ##

- [Język definicji raportu (Wikipedia)](https://en.wikipedia.org/wiki/Report_Definition_Language)
- [Język definicji raportu (SSRS)](https://docs.microsoft.com/en-us/sql/reporting-services/reports/report-definition-language-ssrs)

