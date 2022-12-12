{
  "date" : "2022-06-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPI - plik pakietu instalatora międzyplatformowego",
  "description":"Poznaj format pliku XPI i interfejsy API, które mogą tworzyć i otwierać pliki XPI.",
  "linktitle" : "XPI",
  "menu" : {
    "docs" : {
    "identifier": "compression-xpi",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-07"
}

## Czym jest plik XPI?

Plik XPI to archiwum instalacyjne, które jest kompresowane w celu zmniejszenia rozmiaru pliku. Jest używany przez aplikacje Mozilli do instalacji wtyczek i plików dodatków. Zawiera skrypt instalacyjny lub manifest w katalogu głównym pliku wraz z pewną liczbą plików danych. Plik XPI może zawierać motywy, zestaw narzędzi lub wtyczki Firefox, które użytkownik może zainstalować, aby stać się częścią przeglądarki Firefox, Thunderbird lub SeaMonkey.

## Format pliku XPI — więcej informacji

Pliki XPI są zapisywane na dysku jako archiwa [ZIP](/pl/compression/zip/), które łączą wiele plików w jeden skompresowany plik. Pliki w pliku XPI mogą zawierać plik skryptu instalacyjnego, taki jak JS, oraz pliki internetowe, takie jak [CSS](/pl/web/css/), [HTML](/pl/web/html/) i [JSON](/pl/web/json/ ). Czasami może również zawierać pliki obrazów [PNG](/pl/image/png/), które mają być używane jako ikony przez dodatek.

### Jak wyświetlić zawartość pliku XPI?

Plik XPI jest praktycznie archiwum ZIP, którego zawartość można przeglądać, wykonując następujące czynności.

* Zmień rozszerzenie pliku z XPI na ZIP
* Wyodrębnij zawartość pliku za pomocą dowolnego standardowego narzędzia do dekompresji, takiego jak WinZip (Windows, Mac), 7-Zip (Windows) lub Apple Archive Utility (Mac).

### Zainstaluj plik XPI w przeglądarce Firefox na Androida

Przeważnie ludzie są ciekawi, czy pliki XPI można zainstalować w Firefoksie na urządzeniach z Androidem. W systemie Android możesz zainstalować dodatek z pliku XPI, lokalizując plik i otwierając go w przeglądarce Firefox.

## Bibliografia

* [XPInstall - Wikipedia](https://en.wikipedia.org/wiki/XPInstall)
* [Jak mogę otworzyć rozszerzenie pliku XPI?](https://support.mozilla.org/en-US/questions/1009049)

