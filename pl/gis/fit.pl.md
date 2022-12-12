{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku FIT — plik aktywności Garmin",
  "description":"Poznaj format pliku FIT i interfejsy API, które mogą tworzyć i otwierać pliki FIT.",
  "linktitle" : "FIT",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## Czym jest plik FIT?

Plik FIT to plik GIS utworzony przez sportowe urządzenia do noszenia firmy Garmin. Służy do rejestrowania czynności osoby, która porusza się z tymi urządzeniami. Dane dotyczące aktywności obejmują lokalizację i czas zarejestrowane przez urządzenie GPS. Pliki FIT są również używane do przesyłania zarejestrowanych danych dotyczących aktywności za pomocą internetowych interfejsów API. To jest powód, dla którego pliki FIT są najczęściej używanym formatem plików do udostępniania danych fitness innym platformom fitness. Inne popularne formaty plików to [GPX](/pl/gis/gpx/), TCX i [KML](/pl/gis/kml/).

## Format pliku FIT — więcej informacji

Pliki FIT są zapisywane na dysku jako pliki binarne z informacjami zarejestrowanymi przez urządzenia Garmin dla danej aktywności. Informacje przechowywane w pliku FIT obejmują:

* Data i godzina
* Typy sportowe
* Dane dotyczące okrążeń i podziałów
* Ślad GPS
* Dane czujnika
* Wydarzenia dla aktywnej sesji

Dane dotyczące aktywności mogą być zapisywane w pliku w czasie rzeczywistym lub eksportowane po zakończeniu rejestracji aktywności.

### Komunikaty aktywności FIT

Plik aktywności FIT może zawierać niektóre wymagane typy komunikatów. Poniżej przedstawiono wymagane komunikaty dla pliku aktywności.

|Wiadomość|Cel|
---|---|
|Identyfikator pliku| Wiadomość Identyfikator pliku jest wymagana przez wszystkie typy plików FIT i powinna być pierwszą wiadomością w pliku. W przypadku plików Activity właściwość Type powinna być ustawiona na 4.|
|Aktywność| W pliku działania FIT wymagana jest pojedyncza wiadomość dotycząca działania. Komunikat o działaniu zawiera właściwości Local Timestamp i Session Count. Lokalna sygnatura czasowa służy do określenia przesunięcia strefy czasowej, które można zastosować do wszystkich sygnatur czasowych w pliku. Większość urządzeń zapisuje pliki FIT w czasie rzeczywistym, a liczba sesji będzie nieznana do końca nagrywania. Z tego powodu wiadomość Activity często będzie ostatnią wiadomością w pliku.|
|Sesja| Pliki aktywności będą zawierać jeden lub więcej komunikatów sesji. Komunikat sesji jest typem komunikatu podsumowującego. Czas rozpoczęcia, Całkowity czas, jaki upłynął, Całkowity czas timera i Sygnatura czasowa są polami wymaganymi dla wszystkich komunikatów podsumowujących.|
|Okrążenie| Komunikaty dotyczące okrążeń reprezentują okrążenia lub przerwy w sesji. Wiadomość okrążenia jest wiadomością typu Podsumowanie. Czas rozpoczęcia, Całkowity czas, jaki upłynął, Całkowity czas timera i Sygnatura czasowa są polami wymaganymi dla wszystkich komunikatów podsumowujących.|
|Nagraj| Rekordowe wiadomości obejmują współrzędne GPS, prędkość, dystans, tętno, moc itp. |

## Przydatne zasoby pliku FIT

* [Dekodowanie plików aktywności FIT](https://developer.garmin.com/fit/cookbook/decoding-activity-files/)
* [Kodowanie plików aktywności FIT](https://developer.garmin.com/fit/cookbook/encoding-activity-files/)
 

## Bibliografia ##

* [Plik aktywności FIT](https://developer.garmin.com/fit/file-types/activity/)

