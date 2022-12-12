{
  "date" : "2022-06-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku TPSR — plik raportu z sesji pilotażowej TeamViewer",
  "description":"Poznaj format plików TPSR i interfejsy API, które mogą tworzyć i otwierać pliki TPSR.",
  "linktitle" : "TPSR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-06"
}

## Czym jest plik TSR?

TPSR to plik protokołu połączenia używany przez TeamViewer Assist AR (wcześniej znany jako TeamViewer Pilot). Informacje przechowywane w pliku TPSR są przechowywane w skompresowanym formacie pliku [ZIP](/pl/compression/zip/). TPSR zawiera szczegółową historię połączenia TeamViewer między ekspertem a technikiem w celu rozwiązania problemu i przeglądu. Informacje zawarte w pliku TPSR obejmują typ urządzenia, nazwę, identyfikator Assist AR, identyfikator eksperta, datę i godzinę oraz czas trwania połączenia. Te dane są przechowywane w pliku [JSON](/pl/web/json/) w skompresowanym archiwum TPSR.

## Format pliku TPSR

Plik TPSR jest zapisywany na dysku w formacie pliku archiwum ZIP, w którym zawartość jest przechowywana w pliku JSON. Jest generowany automatycznie po nawiązaniu połączenia Assist AR, o ile opcja raportowania połączenia jest włączona w TeamViewer.

TeamViewer Assist AR umożliwia ekspertom łączenie się z technikami w celu uzyskania transmisji NA ŻYWO ze zdalnego końca za pośrednictwem mobilnej kamery. Mogą pomóc technikom w rozwiązaniu problemu przez telefon.

## Otwórz pliki TSR

Możesz otwierać pliki TPSR za pomocą komputerowej wersji oprogramowania TeamViewer. Jeśli jest zainstalowany na komputerze, dwukrotne kliknięcie pliku TPSR otworzy go w oprogramowaniu TeamViewer. Pliki TPSR można również eksportować do plików [PDF](/pl/pdf/) lub wydrukować w celu wydrukowania kopii pliku protokołu.

## Bibliografia ##

* [TPSR](https://community.teamviewer.com/English/kb/articles/46456-using-teamviewer-assist-ar)

