{
"data": "2023-08-03",
  "keywords": [
"usr",
"plik usr",
"co to jest plik usr",
"jak otworzyć plik usr",
"plik",
"rozszerzenie pliku usr",
"rozszerzenie"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Format pliku USR - plik danych GPS firmy Lowrance",
  "description":"Dowiedz się o formacie USR i interfejsach API, które umożliwiają tworzenie i otwieranie plików USR.",
"tytuł łącza": "USR",
  "menu": {
    "docs": {
      "identifier": "gis-usr",
      "parent": "gis"
}
},
"lastmod": "2023-08-03"
}

## Czym jest plik USR?

Rozszerzenie pliku ".usr" jest również powiązane z urządzeniami GPS firmy Lowrance. W szczególności służy do przechowywania danych GPS w formacie znanym jako "Format danych użytkownika" (format USR), który jest używany przez urządzenia GPS firmy Lowrance.

Korzystając z urządzenia GPS firmy Lowrance, możesz zapisywać punkty trasy, ślady i trasy w plikach ".usr". Pliki te zazwyczaj zawierają takie informacje, jak szerokość i długość geograficzna, wysokość nad poziomem morza, sygnatura czasowa i inne dane związane z Twoją aktywnością GPS.

Oto kilka typowych zastosowań plików .usr w urządzeniach GPS firmy Lowrance:

- **Punkty trasy:** Punkty trasy to określone lokalizacje zaznaczone na urządzeniu GPS, takie jak punkty orientacyjne, ulubione miejsca do wędkowania lub interesujące miejsca. Możesz zapisać te lokalizacje jako pliki .usr i można je importować, eksportować lub udostępniać innym użytkownikom Lowrance GPS.

- **Ślady:** Ścieżki reprezentują zarejestrowaną ścieżkę Twoich ruchów GPS. Możesz zapisać swoje ślady jako pliki .usr, co umożliwi Ci późniejsze przeglądanie i analizowanie tras lub udostępnianie ich innym.

- **Trasy:** Trasy to wstępnie zdefiniowane ścieżki, które możesz tworzyć i zapisywać na swoim urządzeniu GPS. Trasy te można również zapisać jako pliki .usr do wykorzystania w przyszłości lub udostępnienia.

Aby zarządzać plikami .usr w urządzeniu GPS firmy Lowrance, zazwyczaj korzystasz z oprogramowania, takiego jak "Insight Planner" lub "Lowrance GPS Utility" firmy Lowrance, które umożliwia importowanie, eksportowanie i manipulowanie danymi GPS.

## Format pliku USR — więcej informacji

W urządzeniach GPS iFinder firmy Lowrance pliki .usr są tworzone i zapisywane na karcie pamięci MultiMediaCard (MMC) włożonej do urządzenia. Pliki te zawierają dane użytkownika, takie jak punkty trasy, ślady i trasy.

Aby przenieść pliki .usr z MMC do komputera, możesz wykonać następujące kroki:

- **Wyjmij kartę MMC:** Ostrożnie wyjmij kartę MultiMediaCard (MMC) z urządzenia GPS Lowrance iFinder.

- **Włóż kartę MMC do komputera:** Użyj odpowiedniego czytnika kart MMC, aby włożyć kartę pamięci do gniazda czytnika kart w komputerze.

- **Zlokalizuj pliki .usr:** Po rozpoznaniu karty MMC przez komputer, dostęp do zapisanych na niej plików powinien być możliwy. Poszukaj plików .usr, które zawierają dane GPS.

- **Konwersja za pomocą GPSBabel:** Aby przekonwertować pliki .usr na inny format GPS, możesz użyć GPSBabel, które jest bezpłatnym narzędziem typu open source do pracy z różnymi formatami plików GPS. GPSBabel obsługuje szeroką gamę formatów wejściowych i wyjściowych, umożliwiając konwersję plików .usr do formatów kompatybilnych z innym oprogramowaniem lub urządzeniami GPS.

Możesz pobrać GPSBabel z oficjalnej strony internetowej (http://www.gpsbabel.org/) i zainstalować go na swoim komputerze. Po zainstalowaniu możesz użyć interfejsu wiersza poleceń programu lub graficznego interfejsu użytkownika (jeśli jest dostępny), aby przeprowadzić konwersję.

Na przykład, jeśli chcesz przekonwertować pliki .usr do formatu GPX, możesz użyć polecenia takiego jak:

```
gpsbabel -i lowranceusr -f input.usr -o gpx -F output.gpx
```

Powyższe polecenie instruuje GPSBabel, aby odczytał plik wejściowy "input.usr" w formacie Lowrance USR i zapisał plik wyjściowy "output.gpx" w formacie GPX.

- **Importowanie/używanie przekonwertowanych plików:** Po konwersji dane GPS będą dostępne w nowym formacie (np. GPX), którego można używać z innym oprogramowaniem GPS lub urządzeniami obsługującymi ten format.

## Jak otworzyć plik USR?

Programy otwierające pliki USR lub odwołujące się do nich obejmują

-GPSBabel (Windows)
- GPSBabel (Mac)
-GPSBabel (Linux)

## Bibliografia
* [Lowrance Electronics](https://en.wikipedia.org/wiki/Lowrance_Electronics)

