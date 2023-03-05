{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Plik AGI - format pliku interfejsu Asterisk Gateway",
  "description":"Dowiedz się, czym jest format pliku AGI, z przykładami i interfejsami API, które mogą tworzyć i otwierać pliki AGI.",
  "linktitle" : "AGI",
  "menu" : {
    "docs" : {
      "identifier": "programming-agi",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Czym jest plik AGI?

Plik AGI to plik skryptu używany przez system telefoniczny typu open source, Asterisk. Zawiera informacje, które można wykorzystać do automatyzacji procesów i dialplanu Asterisk. Za pomocą plików skryptowych AGI można nawiązywać połączenia z relacyjnymi bazami danych, takimi jak PostgreSQL lub MySQL. Ponadto skrypty AGI mogą być również używane do uzyskiwania dostępu do innych zasobów zewnętrznych. Skrypty AGI mogą przekazać kontrolę nad planem telefonicznym zewnętrznemu skryptowi AGI, umożliwiając firmie Asterisk wykonywanie złożonych zadań.

## Format pliku AGI — więcej informacji

Pliki skryptów AGI są zapisywane jako pliki tekstowe i można je otwierać w dowolnym edytorze tekstu w celu wprowadzania zmian.

### Standardowy wzorzec komunikacji AGI

Skrypt AGI ładuje zmienne i ich wartości przesłane do niego przez Asterisk. Typowy wygląd tych zmiennych jest następujący.

```
agi_request: test.py
agi_channel: Zap/1-1
agi_language: en
agi_callerid:
agi_context: default
agi_extension: 123
agi_priority: 2
```

Po tych zmiennych następuje pusta linia wysłana przez Asterisk, pokazująca, że skrypt AGI może teraz przejąć kontrolę nad planem wybierania numerów.

### Język programowania dla plików skryptów AGI

Skrypty AGI można zazwyczaj pisać w językach Perl, [PHP](/pl/programming/php/), [C](/pl/programming/c/), Pascal lub Bourne Shell.

## Bibliografia

* [Skrypt AGI z gwiazdką](https://www.oreilly.com/library/view/asterisk-the-future/9780596510480/ch09.html)

