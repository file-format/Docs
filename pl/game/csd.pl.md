{
  "date" : "2022-02-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Dowiedz się więcej o formacie pliku kopii zapasowej danych gry CSD Steam i interfejsach API.",
  "title" :"Format pliku CSD — plik kopii zapasowej danych gry Steam",
  "linktitle" : "CSD",
  "menu" : {
    "docs" : {
      "identifier": "game-csd",
      "parent" : "game"
}
},
  "lastmod" : "2022-02-08"
}

## Czym jest plik CDD?

Plik CSD to plik kopii zapasowej gry generowany przez usługę gier **Steam**, która umożliwia użytkownikom pobieranie i zarządzanie grami **Valve**. Zawiera dane kopii zapasowej związane z grami, których można użyć do przywrócenia usuniętej gry. Steam może przywrócić grę z pliku CSD tylko wtedy, gdy gra została pobrana, zainstalowana i załatana przez Steam. Aby przywrócić grę z pliku CSD, użyj opcji Steam → Kopia zapasowa i przywróć Gamesteam i wybierz plik.

## Format pliku CSD — więcej informacji

Wewnętrzna struktura formatu plików CSD nie jest publicznie dostępna, a specyfikacje formatu plików nie są dostępne do wglądu dla programistów. Plikom CSD towarzyszą pliki CSM i ISS, które są również formatami plików gier Steam.

### Gdzie znaleźć pliki kopii zapasowej Steam?

Całe pliki kopii zapasowej Steam można znaleźć w następujących lokalizacjach:

* C:\Program Files (x86)\Steam\steamapps\common\<game name> \ :
* \cfg\ - Konfiguracje niestandardowe i skrypty konfiguracyjne
* \downloads\ - Niestandardowa zawartość do gier wieloosobowych
* \maps\ - Niestandardowe mapy, które zostały zainstalowane lub pobrane podczas gry wieloosobowej
* \materials\ - Niestandardowe tekstury i skórki
* \SAVE\ - Zapisane gry dla jednego gracza

Jednak lokalizacja gier stworzonych przez osoby trzecie może być inna i jest określana przez twórcę gry.

### Przywracanie z pliku kopii zapasowej CSD

Zainstaluj Steam i zaloguj się na właściwe konto Steam (zobacz Instalowanie Steam, aby uzyskać dalsze instrukcje)
* Uruchom Steama
* Kliknij „Steam” w lewym górnym rogu aplikacji Steam
* Wybierz „Utwórz kopię zapasową i przywróć gry…”
* Wybierz „Przywróć poprzednią kopię zapasową”
* Przejdź do lokalizacji plików kopii zapasowych gry
* Przejdź przez okna Steam, aby zainstalować niezbędne gry.

## Bibliografia

* [Korzystanie z funkcji kopii zapasowej Steam](https://help.steampowered.com/en/faqs/view/4593-5CB7-DC3C-64F0)

