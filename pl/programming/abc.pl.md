
{
  "date" : "2021-12-14",
  "keywords": [ ".abc file", "extension", "format","ActionScript Byte Code File", "how to open .abc file","abc file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ABC - plik kodu bajtowego ActionScript",
  "description":"Dowiedz się, czym jest format pliku ABC z przykładami i interfejsami API, które mogą tworzyć i otwierać pliki ABC.",
  "linktitle" : "ABC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-14"
}

## Czym jest plik ABC?

Plik z rozszerzeniem .abc to plik kodu bajtowego ActionScript utworzony przez kompilator Flash w wyniku kompilacji plików skryptów ActionScript. Kod bajtowy zawarty w pliku ABC jest wykonywany przez maszynę wirtualną ActionScript (AVM i AVM2). Kod bajtowy składa się ze stałych danych, instrukcji z zestawu instrukcji AVM2 oraz różnego rodzaju metadanych. Kiedy plik ABC jest ładowany do AVM lub AVM2, przechodzi weryfikację. Jeśli nie jest zgodny z przeglądem AVM2, zostaje odrzucony. Pliki ABC można otwierać w programie Adobe Flash Player, który został wycofany dawno temu.

## Format pliku ABC — więcej informacji

Pliki ABC są zapisywane na dysku w formacie binarnym, które są czytelne dla maszyn wirtualnych AVM lub AVM2. Jego wewnętrzna struktura plików reprezentuje wykonywalny blok kodu ze wszystkimi stałymi danymi, deskryptorami typów, kodem i metadanymi.

## Struktura pliku ABC

Struktura pliku ABC jest pokazana poniżej.

```
abcFile  
{
           u16        minor_version                
           u16        major_version                
           cpool_info        constant_pool                
           u30        method_count                
           method_info        method[method_count]                
           u30        metadata_count                
           metadata_info        metadata[metadata_count]                
           u30        class_count                
           instance_info        instance[class_count]                
           class_info        class[class_count]                
           u30        script_count                
           script_info        script[script_count]               
           u30        method_body_count                
           method_body_info        method_body[method_body_count]        
}
```

### Pola pliku ABC

|Nazwa pola|Opis|
---|---|
|podrzędna_wersja, główna_wersja|Wartości głównych_wersja i podrzędna_wersja to główne i podrzędne numery wersji formatu abcFile.|
|pula_stałych|pula_stałych jest strukturą o zmiennej długości składającą się z liczb całkowitych, liczb podwójnych, ciągów znaków, przestrzeni nazw, zestawów przestrzeni nazw i wielu nazw.|
|metoda_liczba, metoda|Wartość metody_liczba to liczba wpisów w tablicy metod. Każdy wpis w tablicy metod jest strukturą o zmiennej długości method_info.|
|metadata_count, metadata|Wartość metadata_count to liczba wpisów w tablicy metadanych. Każdy wpis metadanych to metadata_infostructure, który odwzorowuje nazwę na zestaw wartości ciągu. |
|klasa_liczba, instancja, klasa|Wartość klasy_liczba to liczba wpisów w tablicy instancji i klas. |
|script_count, script|Wartość script_count to liczba wpisów w tablicy skryptów. Każda pozycja skryptu jest strukturą script_info, która definiuje charakterystykę pojedynczego skryptu w tym pliku. |
|method_body_count, method_body|Wartością metody_body_count jest liczba wpisów w tablicy method_body. Każdy method_bodyentry składa się ze struktury method_body_info o zmiennej długości, która zawiera instrukcje dla indywidualnej metody lub funkcji.|

## Bibliografia

* [Solidny ABC (ActionScript Bytecode) [Dis-]Assembler - Github](https://github.com/CyberShadow/RABCDAsm)

