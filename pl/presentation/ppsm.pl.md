{
  "date" : "2019-10-11",
  "keywords" :[ "plik ppsm", "format pliku ppsm", "co to jest plik ppsm", "plik", "przykład ppsm", "rozszerzenie pliku ppsm", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PPSM — plik prezentacji programu PowerPoint z obsługą makr",
  "description":"Poznaj format pliku PPSM i interfejsy API, które mogą tworzyć i otwierać pliki PPSM.",
  "linktitle" : "PPSM",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik PPS?

Pliki z rozszerzeniem PPSM reprezentują format pliku pokazu slajdów z obsługą makr utworzony za pomocą programu Microsoft PowerPoint 2007 lub nowszego. Innym podobnym formatem pliku jest [PPTM](/pl/presentation/pptm/), który różni się otwieraniem w programie Microsoft PowerPoint w formacie edytowalnym zamiast uruchamiania jako pokaz slajdów. Po uruchomieniu jako pokaz slajdów plik PPSM pokazuje slajdy prezentacji z nienaruszoną zawartością w pokazie slajdów i jest domyślnie w trybie tylko do odczytu. Pliki PPSM nadal można edytować w programie Microsoft PowerPoint, otwierając je w programie PowerPoint.

## Format pliku ##

Format pliku PPSM został wprowadzony w programie PowerPoint 2007 i jest oparty na formacie pliku OpenXML, który wykorzystuje kombinację formatu XML i [ZIP](/pl/compression/zip/) do przechowywania zawartości. Pliki wygenerowane za pomocą pakietu Office Format plików Open XML to zbiór plików XML wraz z innymi plikami, które zapewniają łącza między wszystkimi plikami składowymi. Ta kolekcja jest w rzeczywistości skompresowanym archiwum, które można rozpakować w celu wyświetlenia jego zawartości. Aby to zrobić, po prostu zmień nazwę rozszerzenia pliku PPSM na zip i rozpakuj go, aby obserwować jego zawartość.

Poniższe sekcje rzucają trochę światła na każdy z nich.

### [Typy_zawartości].xml ###

Jest to jedyny plik znaleziony na poziomie podstawowym podczas rozpakowywania pliku ZIP. Zawiera listę typów zawartości dla części w pakiecie. Wszystkie odniesienia do plików XML zawartych w pakiecie znajdują się w tym pliku XML. Poniżej przedstawiono typ zawartości dla części slajdu:
```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```
Jeśli do pakietu trzeba dodać nowe części, można to zrobić, dodając nową część i aktualizując wszelkie relacje w plikach .rels. Należy pamiętać, że przy takiej zmianie należy również zaktualizować plik Content_Types.xml.

### \_rels (folder) ###

Relacje między innymi częściami i zasobami poza pakietem są utrzymywane przez część relacji. Folder Relationships zawiera pojedynczy plik XML, w którym są przechowywane relacje na poziomie pakietu. Linki do kluczowych części plików prezentacji są zawarte w tym pliku jako identyfikatory URI. Te identyfikatory URI identyfikują typ relacji każdej kluczowej części z pakietem. Obejmuje to związek z głównym dokumentem biurowym znajdującym się jako ppt/presentation.xml oraz inne części w docProps jako podstawowe i rozszerzone właściwości.
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

* [Format pliku prezentacji OpenXML](https://msdn.microsoft.com/en-us/library/dd926741(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)

