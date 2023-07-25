{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MXF – Format Wymiany Materiałów",
  "keywords" :["MXF", "matroska wideo", "format mkv", "jak odtwarzać pliki MXF", "SMPTE", "multimedia", "wideo" ],
  "description":"Poznaj format plików MXF i interfejsy API, które mogą tworzyć i otwierać pliki MXF.",
  "linktitle" : "MXF",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-03-01"
}

## Czym jest plik MXF?

Plik z rozszerzeniem .mxf to format kontenera multimedialnego, który zawiera cyfrowe multimedia wideo i audio wraz z informacjami o metadanych pliku. Jest zgodny ze standardem SMPTE (Society of Motion Picture and Television Engineers), który jest globalnym stowarzyszeniem profesjonalistów z dziedziny inżynierii, technologii i kadry kierowniczej pracujących w przemyśle medialnym i rozrywkowym. Pliki MXF można konwertować do innych formatów plików, takich jak [AVI](/pl/video/avi/) lub [MOV](/pl/video/mov/).

## Format pliku MXF

Pliki MXF są w rzeczywistości plikami binarnymi, które składają się z sekwencji bajtów w określonym formacie. Aplikacje dekodujące muszą być zgodne z tym formatem, aby go zrozumieć i wydobyć z niego informacje. Format umożliwia dodawanie nowych elementów bez naruszania kompatybilności wstecznej przy użyciu opisanego poniżej kodowania KLV.

* Klucz – identyfikator pierwiastka, uniwersalna etykieta SMPTE (UL)
* Długość – długość danych, czyli kodowanie o zmiennej długości stosowane w celu zmniejszenia ilości miejsca wymaganego dla tej pozycji
* Wartość – rzeczywista wartość elementu.

### Specyfikacje formatu SMPTE

Format pliku MXF został zdefiniowany przez następujące specyfikacje SMPTE.

* SMPTE ST 377-1:2011. Telewizja — Format wymiany materiałów (MXF) — Specyfikacja formatu plików
* SMPTE ST 377-2 (prace w toku, stan na styczeń 2012). Składnia rozszerzeń zakodowanych w KLV dla MXF.
* SMPTE ST 378:2004 (zarchiwizowane w 2010 r.). Telewizja — format wymiany materiałów (MXF) — wzorzec operacyjny 1a (pojedyncza pozycja, pojedyncza paczka)
* SMPTE ST 379-1:2009. Format wymiany materiałów (MXF) — Ogólny kontener MXF
* SMPTE ST 379-2:2010. Format wymiany materiałów (MXF) — kontener ogólny z ograniczeniami MXF
* SMPTE ST 380:2004. Telewizja — format wymiany materiałów (MXF) — opisowy schemat metadanych-1 (standardowy, dynamiczny)
* SMPTE ST 381-1:2005. Telewizja — format wymiany materiałów (MXF) — mapowanie strumieni MPEG do ogólnego kontenera MXF (dynamiczny)
* SMPTE ST 381-2:2011. Format wymiany materiałów (MXF) — mapowanie strumieni MPEG do ogólnego kontenera z ograniczeniami MXF
* SMPTE ST 382:2007. Material Exchange Format (MXF) — mapowanie strumieni AES3 i Broadcast Wave Audio do ogólnego kontenera MXF
* SMPTE ST 383:2008. Telewizja — format wymiany materiałów (MXF) — mapowanie danych DV-DIF do ogólnego kontenera MXF
* SMPTE ST 384:2005. Telewizja — format wymiany materiałów (MXF) — mapowanie nieskompresowanych obrazów do ogólnego kontenera MXF
* SMPTE ST 385:2004. Telewizja — Format wymiany materiałów (MXF) — Mapowanie esencji i metadanych SDTI-CP do ogólnego kontenera MXF
* SMPTE ST 386:2004 (zarchiwizowane w 2010 r.). Telewizja — format wymiany materiałów (MXF) — mapowanie danych esencji typu D-10 do ogólnego kontenera MXF
* SMPTE ST 387:2004 (zarchiwizowane w 2010 r.). Telewizja — format wymiany materiałów (MXF) — mapowanie danych esencji typu D-11 do ogólnego kontenera MXF
* SMPTE ST 388:2004 (zarchiwizowane w 2010 r.). Telewizja — format wymiany materiałów (MXF) — mapowanie zakodowanego dźwięku zgodnego z prawem do ogólnego kontenera MXF
* SMPTE ST 389:2005. Telewizja — Format wymiany materiałów (MXF) — MXF Generic Container System Reverse Play System Element
* SMPTE ST 390:2011. Telewizja — format wymiany materiałów (MXF) — wyspecjalizowany wzorzec operacyjny „Atom” (uproszczona reprezentacja pojedynczego elementu)
* SMPTE ST 391:2004 (zarchiwizowane w 2010 r.). Telewizja — Format wymiany materiałów (MXF) — Wzorzec operacyjny 1b (pojedyncza pozycja, pakiety łączone)
* SMPTE ST 392:2004. Telewizja — format wymiany materiałów (MXF) — wzorzec operacyjny 2a (elementy z listy odtwarzania, pojedynczy pakiet)
* SMPTE ST 393:2004. Telewizja — Format wymiany materiałów (MXF) — Wzorzec operacyjny 2b (elementy z listy odtwarzania, pakiety łączone)
* SMPTE ST 394:2006. Telewizja — format wymiany materiałów (MXF) — schemat systemu 1 dla ogólnego kontenera MXF
* SMPTE ST 405:2006. Telewizja — Format wymiany materiałów (MXF) — Elementy i poszczególne pozycje danych dla ogólnego schematu systemu pojemników MXF 1
* SMPTE ST 407:2006. Telewizja — MXF — Wzorce operacyjne 3a i 3b
* SMPTE ST 408:2006. Telewizja — MXF — Wzorce operacyjne 1c, 2c i 3c
* SMPTE ST 410: 2008. Format wymiany materiałów — ogólna partycja strumienia.
* SMPTE ST 422:2006. Format wymiany materiałów — mapowanie strumieni kodu JPEG2000 do ogólnego kontenera MXF
* SMPTE ST 429.4:2006. Opakowanie D-Cinema — aplikacja MXF JPEG 2000
* SMPTE ST 429.5:2006. Opakowanie D-Cinema — plik ścieżki tekstowej z określonym czasem
* SMPTE ST 429.6:2006. Opakowanie D-Cinema — Szyfrowanie esencji plików śledzenia MXF
* SMPTE ST 434:2006. Format wymiany materiałów — kodowanie XML dla metadanych i informacji o strukturze plików
* SMPTE ST 436:2006. Telewizja — mapowania MXF dla linii VBI i pomocniczych pakietów danych
* SMPTE ST 2019-4:2009. Mapowanie jednostek kodowania VC-3 do ogólnego kontenera MXF
* SMPTE ST 2037:2009. Mapowanie VC-1 do ogólnego kontenera MXF
* SMPTE RP 2008:2008. Format wymiany materiałów — mapowanie strumieni AVC do ogólnego kontenera MXF
* SMPTE RP 2057:2011. Tekstowe przenoszenie metadanych w formacie MXF
* SMPTE EG 41:2004. Format wymiany materiałów (MXF) — wytyczne techniczne. Uwaga: Ten dokument nie był już dostępny na stronie internetowej SMPTE, kiedy był przeglądany w styczniu 2012 r.
* SMPTE EG 42:2004. Format wymiany materiałów (MXF) — opisowe metadane MXF
* SMPTE RDD 3:2008. Specyfikacja interoperacyjności e-VTR MXF
* SMPTE RDD 9-2009. Specyfikacja interoperacyjności MXF produktów Sony MPEG Long GOP
* Menu arkusza kalkulacyjnego rejestru metadanych SMPTE.

### Strukturalne metadane MXF

Metadane strukturalne mają fundamentalne znaczenie w pliku MXF, ponieważ zawierają przydatne informacje o zawartości pliku. Metadane MXF zawierają informacje, takie jak liczba klatek na sekundę, rozmiar klatki, data utworzenia pliku i data niestandardowej modyfikacji. Metadane strukturalne opisują strukturę i możliwości pliku MXF, który obejmuje techniczny opis różnych podstawowych komponentów i przekazanie sposobu składu wyjściowej osi czasu.

## Bibliografia

* [MXF – Wikipedia](https://en.wikipedia.org/wiki/Material_Exchange_Format)
* [MXF — raport z postępów](https://tech.ebu.ch/docs/techreview/trev_2010-Q3_MXF-1.pdf)
* [Biblioteka OpenSource C++ dla MXF](http://www.freemxf.org/)

