{
  "date" : "2019-12-13",
  "keywords" :[ "plik pptx", "format pliku pptx", "co to jest plik pptx", "plik", "przykład pptx", "rozszerzenie pliku pptx", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Poznaj format pliku PPTX i interfejsy API, które mogą tworzyć i otwierać pliki PPTX.",
  "title" :"PPTX — format pliku prezentacji programu PowerPoint",
  "linktitle" : "PPTX",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik PTX?

Pliki z rozszerzeniem PPTX to pliki prezentacyjne utworzone za pomocą popularnej aplikacji Microsoft PowerPoint. W przeciwieństwie do poprzedniej wersji formatu pliku prezentacji PPT, który był binarny, format PPTX jest oparty na otwartym formacie pliku prezentacji XML programu Microsoft PowerPoint. Plik prezentacji to zbiór slajdów, z których każdy może zawierać tekst, obrazy, formatowanie, animacje i inne multimedia. Slajdy te są prezentowane publiczności w formie pokazów slajdów z niestandardowymi ustawieniami prezentacji.

## Krótka historia

Format pliku PPTX został wprowadzony w 2007 roku i wykorzystuje standard Open XML zaadaptowany przez firmę Microsoft w 2000 roku. Przed PPTX powszechnie używanym formatem pliku był PPT, który był czysto binarnym formatem pliku. Nowy typ pliku ma dodatkowe zalety w postaci małych rozmiarów plików, mniejszej liczby zmian spowodowanych uszkodzeniem i dobrze sformatowanej reprezentacji obrazów. To było na początku 2000 roku, kiedy Microsoft zdecydował się na zmianę, aby dostosować się do standardu **Office Open XML**. Do 2007 roku ten nowy format plików stał się częścią pakietu Office 2007 i jest również stosowany w nowych wersjach pakietu Microsoft Office.

## Specyfikacje formatu plików PPTX

Pliki wygenerowane za pomocą pakietu Office Format plików Open XML to zbiór plików XML wraz z innymi plikami, które zapewniają łącza między wszystkimi plikami składowymi. Ta kolekcja jest w rzeczywistości skompresowanym archiwum, które można rozpakować, aby wyświetlić jego zawartość. Aby to zrobić, po prostu zmień nazwę rozszerzenia pliku PPTX na zip i rozpakuj go, aby obserwować jego zawartość (zobacz [Specyfikacje formatu pliku PPTX](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-pptx/ efd8bb2d-d888-4e2e-af25-cad476730c9f) firmy Microsoft).

Poniższe sekcje rzucają trochę światła na każdy z nich.

### [Typy_zawartości].xml

Jest to jedyny plik znaleziony na poziomie podstawowym podczas rozpakowywania pliku ZIP. Zawiera listę typów zawartości dla części w pakiecie. Wszystkie odniesienia do plików XML zawartych w pakiecie znajdują się w tym pliku XML. Poniżej przedstawiono typ zawartości dla części slajdu:

```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```

Jeśli do pakietu trzeba dodać nowe części, można to zrobić, dodając nową część i aktualizując wszelkie relacje w plikach .rels. Należy pamiętać, że przy takiej zmianie należy również zaktualizować plik Content_Types.xml.

### \_rels (folder) ###

Relacje między innymi częściami i zasobami poza pakietem są utrzymywane przez część relacji. Folder Relationships zawiera pojedynczy plik XML, w którym są przechowywane relacje na poziomie pakietu. Linki do kluczowych części plików PPTX są zawarte w tym pliku jako identyfikatory URI. Te identyfikatory URI identyfikują typ relacji każdej kluczowej części z pakietem. Obejmuje to związek z głównym dokumentem biurowym znajdującym się jako ppt/presentation.xml oraz inne części w docProps jako podstawowe i rozszerzone właściwości.

```
<Relationship Id#"rId1" Type#"http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
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
<Relationship Id#"rId2" Type#"http://. . ./hyperlink" Target#"http://www.google.com/" TargetMode#"External"/>
```

#### Ukryty związek ####

W przypadku relacji niejawnej nie ma takiego bezpośredniego odniesienia do `<Relationship> Identyfikator`. Zamiast tego, odniesienie jest rozumiane.

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

* [[MS-PPTX] — format pliku PPTX](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-pptx/efd8bb2d-d888-4e2e-af25-cad476730c9f)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)

