{
  "date" : "2020-11-11",
  "keywords" :["BAK", "rozszerzenie", "plik", "format pliku", "Typ pliku BAK", "Rozszerzenie pliku BAK", "Typ pliku bazy danych", "Format pliku bazy danych", "Pliki bazy danych" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format pliku BAK i interfejsy API, które mogą tworzyć i otwierać pliki BAK.",
  "title" :"Format Pliku BAK - Plik Kopii Zapasowej Bazy Danych",
  "linktitle" : "BAK",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-12-04"
}

## Czym jest plik BAK?

Plik z rozszerzeniem .bak jest zwykle plikiem kopii zapasowej używanym przez różne narzędzia programowe do przechowywania kopii zapasowych danych. Z perspektywy bazy danych plik BAK jest używany przez Microsoft SQL Server do przechowywania zawartości bazy danych. Wszystkie dane i pliki powiązane z bazą danych są przechowywane w tym formacie pliku, aby można je było odzyskać w przypadku uszkodzenia lub nieważności bazy danych z jakiegokolwiek powodu. Pliki kopii zapasowych mogą być przechowywane i indeksowane na innych serwerach ze względów bezpieczeństwa. Kilka aplikacji może tworzyć pliki BAK, takie jak SQL Server Management Studio, Transact-SQL i Windows PowerShell.

## Format pliku BAK

Wewnętrzne szczegóły pliku BAK nie są znane, ale powszechnie przyjmuje się, że jest on oparty na formacie Microsoft Tape Format (MTF). Specyfikacje MTF są dostępne i można się do nich odwoływać w celu zrozumienia struktury pliku. Dokument zawiera szczegółowe informacje na temat pamięci masowej MTF dla każdego, kto ma ogólną wiedzę na temat operacji zarządzania pamięcią masową, napędów taśmowych i systemów plików.

### Zestawy danych

Zestaw danych to zbiór obiektów zapisanych na nośniku pamięci (taśma, dysk optyczny itp.) podczas tworzenia kopii zapasowej lub przywracania danych. Zestawy danych składają się z wielu nośników w przypadku dużej ilości danych.

### Podstawowe elementy MTF

Plik MTF składa się z kilku podstawowych elementów, które stanowią jego elementy składowe. Te elementy to:

#### Bloki deskryptorów

Bloki deskryptorów (DBLK) służą do kontroli formatu i stanowią podstawowe podstawy pliku MTF. Pojedynczy plik MTF definiuje wiele DBLK dla każdej unikalnej roli. Każdy DBLK to blok danych o zmiennej długości, który jest podzielony na następujące cztery części:

* `Wspólny nagłówek bloku` - Struktura o stałej długości, która jest wspólna dla wszystkich DBLK. Jest to jedyny wymagany nagłówek bloku.
* `Informacje o typie DBLK` - blok o stałej długości specyficzny dla definiowanego typu DBLK
* `Operating System Data` - Konkretne dane zdefiniowane na podstawie typu DBLK i systemów operacyjnych
* `DBLK Information` - Informacje specyficzne dla DBLK o zmiennej długości, których nie można zapisać z informacjami DBLK o stałej długości.

 {{< figure src="../bak.png" alt="Format pliku kopii zapasowej Microsoft SQL" >}}

#### Strumień danych

Strumienie danych w pliku MTF służą do enkapsulacji i wyrównania danych. Składa się z nagłówka strumienia, po którym następują dane strumienia. Nagłówek strumienia może zawierać tylko jeden typ danych strumienia.

{{< figure src="../bak_datastream.png" alt="Format pliku kopii zapasowej Microsoft SQL" >}}

#### Znaki plików

Znak pliku służy do logicznej separacji i szybkiego dostępu w obrębie nośnika. Znaki plików są emulowane przez sterownik urządzenia lub przy użyciu bloku Soft Filemark Descriptor w przypadku, gdy używane urządzenie nie zapewnia znaczników plików.

## Bibliografia ##

* [[MS-BCP]: format kopiowania zbiorczego](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5?redirectedfrom=MSDN)

