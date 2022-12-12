{
  "date" : "2019-10-11",
  "keywords" :[ "plik pptm", "format pliku pptm", "co to jest plik pptm", "plik", "przykład pptm", "rozszerzenie pliku pptm", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PPTM — format pliku prezentacji programu PowerPoint z obsługą makr",
  "description":"Poznaj format pliku PPTM i interfejsy API, które mogą tworzyć i otwierać pliki PPTM.",
  "linktitle" : "PPTM",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

Pliki z rozszerzeniem PPTM to pliki prezentacji z obsługą makr, które są tworzone za pomocą programu Microsoft PowerPoint 2007 lub nowszego. Są podobne do plików [PPTX](/pl/presentation/pptx/) z tą różnicą, że boczne nie mogą wykonywać makr, chociaż mogą zawierać makra. Pliki PPTM można edytować, otwierając je w programie Microsoft PowerPoint i aktualizując zawartość. Innym podobnym formatem jest PPSM, ale domyślnie jest on tylko do odczytu i po otwarciu uruchamia pokaz slajdów. PPTM, podobnie jak PPTX, zawiera slajdy dla różnych elementów prezentacji, takich jak tekst, obrazy, filmy, wykresy i inne powiązane materiały.

## Krótka historia ##

Format pliku PPTM został wprowadzony w 2007 roku i wykorzystuje standard Open XML zaadaptowany przez firmę Microsoft w 2000 roku. Nowy typ pliku ma dodatkowe zalety w postaci małych rozmiarów plików, mniejszej liczby uszkodzeń i dobrze sformatowanej reprezentacji obrazów. To było na początku 2000 roku, kiedy Microsoft zdecydował się na zmianę, aby dostosować się do standardu **Office Open XML**. Do 2007 roku ten nowy format plików stał się częścią pakietu Office 2007 i jest również stosowany w nowych wersjach pakietu Microsoft Office.

## Specyfikacje formatu pliku ##

Pliki wygenerowane za pomocą pakietu Office Format plików Open XML to zbiór plików XML wraz z innymi plikami, które zapewniają łącza między wszystkimi plikami składowymi. Ta kolekcja jest w rzeczywistości skompresowanym archiwum, które można rozpakować, aby wyświetlić jego zawartość. Aby to zrobić, po prostu zmień nazwę rozszerzenia pliku PPTM na zip i rozpakuj go, aby obserwować jego zawartość.

Poniższe sekcje rzucają trochę światła na każdy z nich.

### [Typy_zawartości].xml ###

Jest to jedyny plik znaleziony na poziomie podstawowym podczas rozpakowywania pliku ZIP. Zawiera listę typów zawartości dla części w pakiecie. Wszystkie odniesienia do plików XML zawartych w pakiecie znajdują się w tym pliku XML. Poniżej przedstawiono typ zawartości dla części slajdu:
```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```
Jeśli do pakietu trzeba dodać nowe części, można to zrobić, dodając nową część i aktualizując wszelkie relacje w plikach .rels. Należy pamiętać, że przy takiej zmianie należy również zaktualizować plik Content_Types.xml.

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

