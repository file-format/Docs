{
  "date" : "2022-01-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku LOCK - Co to jest plik blokady?",
  "description":"Poznaj format pliku LOCK i jego .",
  "linktitle" : "LOCK",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-26"
}

## Czym jest plik LOCK?

Plik **LOCK** to plik o zmienionej nazwie, który jest używany przez aplikacje i systemy operacyjne do oznaczania pliku lub urządzenia jako zablokowanego. Mówi to innym aplikacjom, aby nie używały pliku, chyba że jest on wolny od aplikacji, która go używa. W większości przypadków te pliki blokady są puste, ale w innych przypadkach mogą zawierać informacje związane z blokadą, takie jak właściwości i ustawienia.

Czasami plik .lock jest używany przez .NET Framework firmy Microsoft do tworzenia **lockeed** kopii pliku bazy danych. W takim przypadku kopia pliku bazy danych otworzy się z rozszerzeniem .lock. Nie pozwala to użytkownikowi na wprowadzanie zmian w pliku, gdy jest on używany przez innego użytkownika.

## Format pliku LOCK — więcej informacji

Plik LOCK jest tworzony przez każdą aplikację, a jego format pliku jest specyficzny dla aplikacji. Te pliki blokad można zapisać zarówno w formacie tekstowym, jak i binarnym.

Obecność plików blokujących uniemożliwia równoczesny dostęp zasobu do wielu plików próbujących uzyskać dostęp do tego zasobu. Tworzona jest kopia oryginalnego pliku z rozszerzeniem .lock do nazwy. To mówi innym aplikacjom, aby miały dostęp tylko do odczytu do pliku. Na przykład zasób.dat zmieni się zasób.data.lock.

W przypadku języka programowania Ruby możesz natknąć się na plik **gemfile.lock**. W tym miejscu Bundler zapisuje dokładne wersje, które zostały zainstalowane. Tak więc, gdy projekt/biblioteka zostanie przeniesiona na inną maszynę, uruchomiony pakiet sprawdzi plik Gemfile pod kątem dokładnej odpowiedniej wersji.

## Zablokuj plik w systemie Linux

Linux obsługuje dwa rodzaje blokad plików: blokady doradcze i blokady obowiązkowe.

* **Blokady doradcze**: Typ blokady, który nie jest wymuszany. W tym przypadku uczestniczące procesy współpracują ze sobą jawnie uzyskując blokady. Jeśli nie jest to możliwe, blokady doradcze są ignorowane.

* **Blokady obowiązkowe**: W przypadku blokowania obowiązkowego system operacyjny wymusza blokadę pliku, uniemożliwiając innym procesom odczytywanie lub zapisywanie pliku. Nie wymaga to żadnej współpracy między procesami.

obowiązkowe blokowanie nie wymaga żadnej współpracy między uczestniczącymi procesami. Po aktywowaniu obowiązkowej blokady pliku system operacyjny uniemożliwia innym procesom odczytywanie lub zapisywanie pliku.

## Bibliografia

* [GemFile i Gemfile.lock w Ruby](https://medium.com/never-hop-on-the-bandwagon/gemfile-and-gemfile-lock-in-ruby-65adc918b856)
* [Blokowanie w systemie Linux](https://www.baeldung.com/linux/file-locking)

