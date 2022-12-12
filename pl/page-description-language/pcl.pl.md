{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PCL",
  "description":"Poznaj format plików PCL i interfejsy API, które mogą tworzyć i otwierać pliki PCL.",
  "linktitle" : "PCL",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik PCL? ##

PCL to skrót od Printer Command Language, który jest językiem opisu strony wprowadzonym przez firmę Hewlett Packard (HP). Firma HP stworzyła język PCL, aby zapewnić skuteczny sposób kontrolowania funkcji drukarki w wielu różnych urządzeniach drukujących. Format został pierwotnie opracowany dla drukarek igłowych i atramentowych HP, ale z biegiem czasu stał się częścią różnych drukarek termicznych, igłowych i stronicowych. Format przeszedł kilka różnych zmian, w wyniku czego powstały różne wersje, z których każda została ulepszona, aby sprostać wymaganiom czasu w odniesieniu do funkcji sterowania drukarką. Obecnie PCL jest najbardziej rozpowszechnionym językiem drukarki na rynku drukarek laserowych.

## Wersje PCL ##

Wersje PCL różnią się funkcjonalnością (np. obsługa typów czcionek: czcionki bitmapowe, czcionki skalowalne (czcionki Intellifonts, czcionki TrueType), metody kompresji grafiki rastrowej, obsługa grafiki HP-GL/2).

**PCL 1:** ok. 1980 r. - Funkcjonalność Print and Space to podstawowy zestaw funkcji zapewniających proste, wygodne drukowanie na stacji roboczej dla jednego użytkownika.

**PCL 2:** około 1980 r. — EDP (elektroniczne przetwarzanie danych)/funkcje transakcyjne to nadzbiór języka PCL 1. Dodano funkcje do ogólnego zastosowania w systemach drukowania dla wielu użytkowników.

**PCL 3**: 1984 — funkcja Office Word Processing jest nadzbiorem języka PCL 2. Dodano funkcje zapewniające wysoką jakość produkcji dokumentów biurowych i zwiększoną rozdzielczość do 300 dpi. Pozwoliło to na użycie ograniczonej liczby bitmapowych czcionek i grafiki oraz obsługiwało HP-GL. PCL 3 był szeroko naśladowany przez innych producentów drukarek i był przez nich określany jako „LaserJet Plus Emulation”.
(Drukarki: rodzina HP DeskJet, drukarka z serii HP LaserJet, drukarka z serii HP LaserJet Plus)

**PCL3+:** Używany przez rodziny drukarek DeskJet i DesignJet.

**PCL3c:** Używany przez rodziny drukarek DeskJet i DesignJet.

**PCL3e**: Używany przez rodziny drukarek DeskJet i DesignJet. Teraz używany również w PhotoSmart.

**PCL3GUI**: Używa RTL i jest używany przez rodziny drukarek DeskJet i DesignJet.

**PCLSLEEK**: Używa RTL i jest używany przez rodziny drukarek DeskJet i DesignJet.

**PCL 4**: 1985 — funkcja formatowania strony jest nadzbiorem wersji PCL 3. Obsługiwane makra, większe czcionki bitmapowe i grafika. (Drukarki: HP LaserJet II, HP LaserJet IIP (PCL 4.5))

**PCL 5:** 1990 — funkcja Office Publishing jest nadzbiorem języka PCL 4. Nowe możliwości publikowania obejmują skalowanie czcionek i grafikę HP-GL/2 (wektorową). (Drukarki: HP LaserJet III)

**PCL 5e:** 1994 — jest to główna wersja zawierająca nowe funkcje, takie jak adaptacyjny system kompresji, kodowanie znaków 2-bajtowych, obsługę czcionek wektorowych i dwukierunkowe polecenia konfiguracyjne. Obejmuje operacje logiczne (odpowiada ROP GDI) w celu poprawy obsługi systemu Windows przed obcinaniem ścieżek. (Drukarki: HP LaserJet 4)

**PCL 5j:** Nowe funkcje, takie jak obsługa znaków 2-bajtowych dla japońskich czcionek skalowalnych, pismo pionowe, japońskie rozmiary papieru i ciągi krojów pisma. (Drukarki: HP LaserJet 4PJ)

**PCL 5c:** 1995 — Obsługa kolorów i operacje logiczne zostały dodane do języka PCL5. PCL5c poprzedza PCL5e. Niektóre modele obsługują również ścieżki przycinające. (Drukarki: HP Color LaserJet, HP PaintJet 300 XL (pierwsza drukarka z PCL5c), HP DeskJet 1200C/1600C (te numery modeli zostały ponownie wykorzystane, a nowsze modele nie obsługują języka PCL 5c)

**PCL 5ce:** obsługuje skalowalne kroje pisma Agfa Microtype. (Drukarki: drukarka HP 2500c Pro)

**PCL 6 / XL:** 1996 — PCL 6 lub PCL XL to nowy format wprowadzony w 1995 r., który nie jest zgodny z żadną poprzednią wersją PCL. (Drukarki: HP LaserJet 5, 5M i 5N)

## Przegląd PCL 6 ##

HP wprowadził język PCL 6 w 1996 r., który był kolejną ewolucją języka PCL i związanych z nim technologii. Posiada następujące elementy:

**PCL 6 Enhanced:** zapewnia zoptymalizowaną wersję do drukowania z graficznych interfejsów użytkownika (GUI), takich jak MS Windows i OS/2

**Standard PCL 6:** zapewnia pełną kompatybilność wsteczną z poprzednimi drukarkami HP LaserJet

**Synteza czcionek PCL:** zapewnia skalowalne czcionki, zarządzanie czcionkami oraz przechowywanie formularzy i czcionek.

Rozszerzona wersja PCL XL jest bliższa GDI, z którego korzysta wiele aplikacji. Zapewnia, że odbywa się mniej tłumaczeń, co skutkuje zwiększonymi możliwościami WYSIWYG i lepszą wydajnością w aplikacjach obsługujących znaki specjalne zaimplementowane przez ulepszony sterownik. Dane wyjściowe sterownika Enhanced (PCL XL) mogą różnić się od danych wyjściowych sterownika Standard. Jeśli dane wyjściowe nie są zgodne z oczekiwaniami, wybierz sterownik standardowy (PCL5e).

Polecenia PCL 6 Enhanced zostały zaprojektowane tak, aby optymalnie odpowiadały wymaganiom drukowania grafiki w aplikacjach opartych na graficznym interfejsie użytkownika. W większości przypadków dla każdego polecenia drukowania grafiki, które GUI chce wykonać, istnieje pasujące polecenie PCL 6 Enhanced. Zmniejsza to liczbę poleceń wymaganych do opisania strony graficznej. Każde polecenie w PCL 6 Enhanced zostało zaprojektowane tak, aby wymagało minimalnego transferu danych z komputera hosta do drukarki. Zmniejsza to ilość danych wymaganych do opisania strony.

System drukowania Windows dla większości drukarek HP LaserJet zawiera dwa oddzielne sterowniki: standardowy i rozszerzony. Standardowy sterownik zapewnia zgodność z poprzednimi wersjami, używając poleceń PCL 6 Standard (PCL5e) do drukowania prostego tekstu lub mieszanych stron zawierających tekst i grafikę. Sterownik Enhanced wykorzystuje polecenia PCL 6 Enhanced, które zostały zoptymalizowane pod kątem drukowania złożonych stron graficznych.

## Wersje klasy PCL 6 ##

#### Klasa 1.1 ####

**Narzędzia do rysowania:** Obsługa rysowania linii, łuków/elips/cięciw, (zaokrąglonych) prostokątów, wielokątów, ścieżek Beziera, ścieżek przyciętych, obrazów rastrowych, linii skanowania, operacji rastrowych.
**Obsługa kolorów:** obsługuje palety 1/4/8-bitowe, przestrzeń kolorów RGB/szary. Obsługa niestandardowych wzorów półtonów (maks. 256 wzorów).
**Kompresja:** Obsługuje RLE.
**Jednostki miary:** cale, milimetry, dziesiąte części milimetra.
**Obsługa papieru:** Obsługa niestandardowych lub wstępnie zdefiniowanych zestawów rodzajów papieru, w tym zwykłych Letter, Legal, A4 itp. Możliwość wyboru papieru z podajnika ręcznego, tac i kaset. Papier można drukować dwustronnie w poziomie lub w pionie. Papier może być zorientowany pionowo, poziomo lub obrócony o 180 stopni w stosunku do dwóch poprzednich.
**Czcionka:** obsługuje czcionki bitmapowe lub TrueType, 8 lub 16-bitowe punkty kodowe. Wybór zestawu znaków używa innego kodu zestawu symboli niż PCL 5. Gdy używana jest czcionka bitmapowa, wiele poleceń skalowania jest niedostępnych. Gdy używana jest czcionka TrueType, deskryptory o zmiennej długości i bloki kontynuacji nie są obsługiwane. Czcionka konturu może być obracana, skalowana lub ścinana.

#### Klasa 2.0 ####

**Kompresja:** Dodano zastrzeżoną kompresję JPEG o nazwie JetReady.
**Obsługa papieru:** Media mogą być przekierowywane do różnych pojemników wyjściowych (do 256). Dodano wstępnie ustawione rozmiary nośników A6 i japoński B6. Dodano wstępne ustawienie trzeciej kasety, 248 zewnętrznych źródeł nośników.
**Czcionka:** Tekst można pisać pionowo.

#### Klasa 2.1 ####

**Obsługa kolorów:** Dodano funkcję dopasowywania kolorów.
**Kompresja:** Dodano wiersz Delta.
**Obsługa papieru:** Orientacja, rozmiar nośnika są opcjonalne przy deklarowaniu nowej strony. Dodano typy papieru B5, JIS 8K, JIS 16K, JIS Exec.

#### Klasa 3.0 ####

**Obsługa kolorów:** Umożliwia stosowanie różnych ustawień półtonów dla grafiki wektorowej lub rastrowej, tekstu. Obsługuje adaptacyjne półtonowanie.
**Protokół:** Obsługuje przekazywanie PCL, umożliwiając korzystanie z funkcji PCL 5 w strumieniach PCL 6. Jednak niektóre stany PCL 6 nie są zachowywane podczas korzystania z tej funkcji.
**Czcionka:** obsługuje czcionki PCL.
**Przeglądarka/konwerter:** PCLReader (bezpłatny) umożliwia przeglądanie, konwertowanie lub drukowanie dowolnego poziomu języka PCL 6 (w tym JetReady) na dowolnej drukarce.

## Bibliografia ##

* [PCL – z Wikipedii](https://en.wikipedia.org/wiki/Printer_Command_Language)

