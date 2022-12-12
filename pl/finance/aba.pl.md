{
  "date" : "2019-10-11",
  "keywords" :["plik aba", "format pliku aba", "co to jest plik aba", "plik", "przykład aba", "rozszerzenie pliku aba","rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ABA - format pliku CemText",
  "description":"Poznaj format plików ABA i interfejsy API, które mogą tworzyć i otwierać pliki ABA.",
  "linktitle" : "ABA",
  "menu" : {
    "docs" : {
      "identifier":"finance-aba",
      "parent" : "finance"
}
},
  "lastmod" : "2121-03-24"
}

## Czym jest plik ABA?

Plik z rozszerzeniem .aba to format pliku Australian Bankers Association (ABA) lub [Cemtext](https://www.cemtexaba.com/), który jest używany przez banki do transakcji wsadowych. Jest używany przez większość banków do prowadzenia dokumentacji finansowej. Znany również jako plik Direct Entry, format pliku ABA został przyjęty przez większość australijskich banków jako domyślny format transakcji wsadowych. Nadal nie został uznany za format standardowy, mimo że był używany przez Bank of Queensland, NAB i Westpac. Pliki ABA można otwierać za pomocą dowolnego edytora tekstu, takiego jak Notepad ++.


## Format pliku ABA

Plik ABA wykorzystuje format ASCII do przechowywania danych w celu przekazania lub załadowania do systemów bankowych. Format został uproszczony, aby ułatwić integrację z własnymi systemami finansowymi firm w celu przetwarzania partii transakcji. Na przykład w systemie płacowym można przesłać partię transakcji do przetworzenia w jednym działaniu. Specyfikacje formatu plików ABA są dostępne jako pełny zapis na stronie internetowej [Cemtext ABA](https://www.cemtexaba.com/aba-format/cemtex-aba-file-format-details) i można się do nich odnieść w celach informacyjnych dla programistów .

Plik ABA składa się z wielu wierszy, z których każdy jest nazywany „rekordem”. Istnieją trzy główne rekordy w pliku ABA:

* Zapis opisowy
* Rekord szczegółów
* Plik Łączny rekord

### Rekord opisowy

„Rekord opisowy” zawiera informacje, takie jak numer kolejny rolki, nazwa instytucji finansowej użytkownika, plik dostarczający nazwy użytkowania i inne informacje.

### Rekord szczegółów

Typ „Szczegółowy rekord” zawiera informacje, takie jak numer banku/stanu/oddziału, numer konta do uznania/obciążenia, wskaźnik, kod transakcji, kwota i inne informacje.

### Plik Łączny rekord

Typ „Rekord całkowity pliku” obejmuje typ rekordu 7, wypełniacz formatu BSB, łączną kwotę netto pliku (użytkownika), łączną kwotę kredytu (użytkownika), łączną kwotę debetu pliku (użytkownika) i inne informacje.

### Kody transakcji

Lista prawidłowych kodów transakcji jest następująca. Przez większość czasu w plikach ABA używany jest kod „53 - Zapłać”. Te kody transakcji obejmują obciążenia, kredyty i podatki potrącane u źródła.

|Kod|Opis transakcji|
---|---|
|13|Pozycje debetowe inicjowane z zewnątrz|
|50|Pozycje uznaniowe inicjowane z zewnątrz, z wyjątkiem pozycji opatrzonych kodami transakcji|
|51|Zainteresowania rządu australijskiego w zakresie bezpieczeństwa|
|52|Zasiłek rodzinny|
|53|Zapłać|
|54|Emerytura|
|55|Przydział|
|56|Dywidendy|
|57|Odsetki od obligacji/obligacji|

## Przykład pliku ABA

```
0                 01BQL       MY NAME                   1111111004231633  230410
1123-456157108231 530000001234S R SMITH                       TEST BATCH        062-000 12223123MY ACCOUNT      00001200
1123-783 12312312 530000002200J K MATTHEWS                    TEST BATCH        062-000 12223123MY ACCOUNT      00000030
1456-789   125123 530003123513P R JONES                       TEST BATCH        062-000 12223123MY ACCOUNT      00000000
1121-232    11422 530000002300S MASLIN                        TEST BATCH        062-000 12223123MY ACCOUNT      00000000
7999-999            000312924700031292470000000000                        000004
```
## Bibliografia

* [Cemtext ABA](https://www.cemtexaba.com/)

