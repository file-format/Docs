{
  "date" : "2019-10-11",
  "keywords" :[ "plik potm", "format pliku potm", "co to jest plik potm", "plik", "przykład potm", "rozszerzenie pliku potm", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"POTM - plik szablonu programu Microsoft PowerPoint z makrami",
  "description":"Poznaj format pliku POTM i interfejsy API, które mogą tworzyć i otwierać pliki POTM.",
  "linktitle" : "POTM",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik POTM?

Pliki z rozszerzeniem POTM to pliki szablonów programu Microsoft PowerPoint z obsługą makr. Pliki POTM są tworzone za pomocą programu PowerPoint 2007 lub nowszego i zawierają ustawienia domyślne, których można użyć do tworzenia kolejnych plików prezentacji. Ustawienia te mogą obejmować style, tła, paletę kolorów, czcionki i ustawienia domyślne wraz z makrami, które składają się z niestandardowych funkcji do wykonania określonego zadania. Mogą być również otwierane przez poprzednią wersję programu PowerPoint z zainstalowaną obsługą dokumentów Open XML. Pliki POTM można otwierać w programie Microsoft PowerPoint do edycji, jak każdy inny plik programu PowerPoint.

## Specyfikacje formatu plików ##

Format pliku POTM jest oparty na specyfikacjach Office OpenXML i przypomina strukturę pliku [PPTX](/pl/presentation/pptx/), który jest skompresowanym archiwum [ZIP](/pl/compression/zip/).

Slajdy w pliku POTM mogą zawierać tekst, obrazy, filmy, grafikę i inne obiekty, które można dowolnie rozmieścić na stronie. Szablony POTM są następnie używane do tworzenia wielu plików, które dziedziczą wszystkie opcje formatowania pliku. Makra zawarte w pliku POTM są zatem dziedziczone również przez inne prezentacje. Osadzanie ich w strukturze dokumentu odbywa się za pomocą Rejestratora makr zawartego w pakiecie MS Office, który może zapisywać sekwencje poleceń i tworzyć makra w celu ich automatycznej replikacji.

Pliki wygenerowane za pomocą pakietu Office Format plików Open XML to zbiór plików XML wraz z innymi plikami, które zapewniają łącza między wszystkimi plikami składowymi. Ta kolekcja jest w rzeczywistości skompresowanym archiwum, które można rozpakować, aby wyświetlić jego zawartość. Aby to zrobić, po prostu zmień nazwę rozszerzenia pliku POTM na zip i rozpakuj go, aby obserwować jego zawartość.

Poniższe sekcje rzucają trochę światła na każdy z nich.

### [Typy_zawartości].xml ###

Jest to jedyny plik znaleziony na poziomie podstawowym podczas rozpakowywania pliku ZIP. Zawiera listę typów zawartości dla części w pakiecie. Wszystkie odniesienia do plików XML zawartych w pakiecie znajdują się w tym pliku XML. Poniżej przedstawiono typ zawartości dla części slajdu:
```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```
Jeśli do pakietu trzeba dodać nowe części, można to zrobić dodając nową część i aktualizując wszelkie relacje w plikach .rels. Należy pamiętać, że przy takiej zmianie należy również zaktualizować plik Content_Types.xml.

### \_rels (folder) ###

Relacje między innymi częściami i zasobami poza pakietem są utrzymywane przez część relacji. Folder Relationships zawiera pojedynczy plik XML, w którym są przechowywane relacje na poziomie pakietu. Linki do kluczowych części plików prezentacji są zawarte w tym pliku jako identyfikatory URI. Te identyfikatory URI identyfikują typ relacji każdej kluczowej części z pakietem. Obejmuje to związek z głównym dokumentem biurowym znajdującym się jako ppt/presentation.xml oraz innymi częściami w docProps jako właściwości podstawowe i rozszerzone.
```
<Relationship Id#"rId1" Type#"http:~/~/schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
```
Każda część dokumentu, która jest źródłem jednej lub więcej relacji, będzie miała własną część relacji, gdzie każda taka część relacji znajduje się w podfolderze \_rels części i jest nazywana przez dodanie „.rels” do nazwy część. Główna część treści (presentation.xml) ma swoją własną część relacji (presentation.xml.rels). Zawiera relacje z innymi częściami treści, takimi jak slideMaster1.xml, notesMaster1.xml, handoutMaster1.xml, slide1.xml, presProps.xml, tableStyles.xml, theme1.xml, a także identyfikatory URI dla łączy zewnętrznych.

#### Jawny związek ####

W przypadku jawnej relacji odwołanie do zasobu jest przy użyciu atrybutu Id elementu a<Relationship> element. Oznacza to, że identyfikator w źródle jest odwzorowywany bezpośrednio na identyfikator elementu relacji, z wyraźnym odwołaniem do celu.

Na przykład slajd może zawierać hiperłącze, takie jak to:
```
<a:hlinkClick r:id#"rId2">
```
r:id#"rId2" odwołuje się do następującej relacji w części relacji dla slajdu (slajd1.xml.rels).
```
<Relationship Id#"rId2" Type#"http:~/~/. . ./hyperlink" Target#"http:~/~/www.google.com/" TargetMode#"External"/>
```
#### Ukryty związek ####

W przypadku relacji niejawnej nie ma takiego bezpośredniego odniesienia do `<Relationship> Identyfikator`. Zamiast tego odniesienie jest rozumiane.

### folder ppt ###

Jest to główny folder zawierający wszystkie szczegóły dotyczące zawartości Prezentacji. Domyślnie ma następujące foldery:

* \_rels
* motyw
* zjeżdżalnie
* Układy slajdów
* Mistrzowie slajdów

oraz następujące pliki xml:

* prezentacja.xml
* presProps.xml
* tableStyles.xml
* viewProps.xml

## Bibliografia ##

* [[MS-PPTX] — format pliku PPTX](https://msdn.microsoft.com/en-us/library/dd926741(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)

