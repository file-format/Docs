{
  "date" : "2019-10-11",
  "keywords" :["xoml", "Plik", "Rozszerzenie", "Format pliku", "Rozszerzenie pliku", "Rozszerzony język znaczników obiektów"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XOML — format pliku przepływu pracy systemu Windows",
  "description":"Poznaj format pliku XOML i interfejsy API, które mogą tworzyć i otwierać pliki XOML.",
  "linktitle" : "XOML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik XOML?

XOML jest skrótem od Extensible Object Markup Language i jest formatem serializacji dla obiektów przepływu pracy Windows Workflow Foundation. Oparty na **[XAML](/pl/web/xaml/)**, jest używany głównie do tworzenia interfejsów użytkownika w zwykłym **[XML](/pl/web/xml/)**. Służą one do deklarowania przepływu pracy dla interfejsu użytkownika i są kompilowane wraz z osobnym plikiem zawierającym logikę implementacji. Zawiera strukturę opartą na drzewie, która definiuje główny węzeł przepływu pracy, zagnieżdżone elementy podrzędne i osadzone segmenty kodu. Gdy nowy przepływ pracy jest tworzony za pomocą programu Visual Studio dla .NET, istnieje możliwość wybrania, czy powinien on być w formacie Code, czy Code Separated. Jeśli wybierzesz późniejszy, IDE utworzy dla ciebie dwa pliki; jeden w formacie XOML (składający się z układu przepływu pracy i ustawień), a drugi w formacie [.CS](/pl/programming/cs/)/[.VB](/pl/programming/vb/), w którym znajduje się kod programowania.

