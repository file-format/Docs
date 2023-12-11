{
"data":"2023-11-01",
   "keywords":[
"poklepać",
"plik pat",
"pat plik instalacyjny menadżera stacji dyskowej",
"jak otworzyć plik pat",
"plik",
"rozszerzenie pliku pat",
"rozszerzenie",
"plik"
],
   "author":{
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title":"Format pliku PAT - plik instalacyjny DiskStation Manager",
   "description":"Dowiedz się więcej o formacie pliku instalacyjnego PAT DiskStation Manager i interfejsach API, które umożliwiają tworzenie i otwieranie plików PAT.",
   "linktitle":"PAT",
   "menu":{
      "docs":{
         "identifier":"system-pat-diskstation",
         "parent":"system"
}
},
"lastmod":"2023-11-01"
}

## Czym jest plik PAT?

Plik PAT jest powszechnie powiązany z **DiskStation Manager (DSM)**, systemem operacyjnym używanym przez urządzenia Synology Network-Attached Storage (NAS). Plik PAT to plik instalacyjny używany do aktualizacji lub instalowania systemu DSM na serwerze Synology NAS.

## Użycie pliku PAT

Oto sposób, w jaki zazwyczaj używasz pliku PAT do instalowania lub aktualizowania DSM na serwerze Synology NAS:

1. Pobierz plik PAT: Plik PAT można uzyskać z oficjalnej strony internetowej firmy Synology lub z innych zaufanych źródeł.
    







2. Zaloguj się do swojego serwera NAS: Uzyskaj dostęp do internetowego interfejsu użytkownika serwera Synology NAS, wprowadzając jego adres IP w przeglądarce internetowej. Aby wykonać tę operację, będziesz potrzebować uprawnień administratora.
    







3. Przejdź do Centrum pakietów: W interfejsie internetowym przejdź do "Centrum pakietów". Tutaj zarządzasz aplikacjami i instalujesz je na swoim serwerze NAS.
    







4. Instalacja ręczna: W Centrum pakietów powinna być dostępna opcja "Instalacja ręczna" lub "Instalacja/aktualizacja" w zależności od używanej wersji DSM. Wybierz tę opcję.
    







5. Przeglądaj w poszukiwaniu pliku PAT: Zostaniesz poproszony o przeglądanie plików lokalnych i wybranie pobranego pliku PAT.
    







6. Zainstaluj lub zaktualizuj: Po wybraniu pliku PAT postępuj zgodnie z instrukcjami wyświetlanymi na ekranie, aby zainstalować DSM (jeśli jest to nowa instalacja) lub zaktualizować DSM (jeśli aktualizujesz do nowszej wersji).
    







7. Poczekaj na zakończenie: Proces instalacji lub aktualizacji może zająć trochę czasu, a w jego ramach serwer NAS może zostać ponownie uruchomiony. Bądź cierpliwy i poczekaj, aż to się skończy.
    







8. Konfiguracja po instalacji: Po instalacji lub aktualizacji może zaistnieć potrzeba skonfigurowania ustawień NAS zgodnie z własnymi preferencjami.

## Menedżer stacji DiskStation

DiskStation Manager, często w skrócie DSM, to system operacyjny opracowany przez firmę Synology dla jej urządzeń Network-Attached Storage (NAS). Służy jako interfejs zarządzania i kontroli dla serwerów Synology NAS. DiskStation Manager zapewnia przyjazny dla użytkownika interfejs internetowy, który umożliwia użytkownikom konfigurowanie różnych aspektów serwera NAS i zarządzanie nimi, takich jak przechowywanie danych, udostępnianie plików, rozwiązania do tworzenia kopii zapasowych, usługi multimedialne i nie tylko.

DSM jest znany ze swojej wszechstronności i rozbudowanego ekosystemu pakietów, który umożliwia użytkownikom instalowanie i uruchamianie różnych aplikacji i usług na serwerze Synology NAS, przekształcając go w wielofunkcyjny serwer do użytku domowego i biznesowego. Niektóre z typowych funkcjonalności DiskStation Manager obejmują udostępnianie plików, tworzenie kopii zapasowych i synchronizację danych, strumieniowe przesyłanie multimediów, funkcje bezpieczeństwa i obsługę wirtualizacji.

Synology regularnie publikuje aktualizacje i nowe wersje DSM w celu zwiększenia bezpieczeństwa, wydajności i funkcji. Użytkownicy mogą ręcznie zaktualizować DSM przy użyciu plików PAT lub skonfigurować automatyczne aktualizacje, aby mieć pewność, że na ich serwerze NAS działa najnowsza i najbezpieczniejsza wersja DiskStation Manager.

## Jak otworzyć plik PAT

Aby ręcznie zaktualizować DiskStation Manager, możesz użyć pliku PAT pobranego z Centrum pobierania Synology, wykonując następujące czynności:

1. Uzyskaj dostęp do Panelu sterowania DiskStation Manager.
2. Przejdź do sekcji "Aktualizacja i przywracanie" i wybierz "Aktualizacja DSM".
3. Następnie wybierz opcję "Ręczna aktualizacja DSM".
4. Kliknij przycisk "Przeglądaj", a następnie znajdź i wybierz pobrany plik PAT.
5. Aby rozpocząć aktualizację DiskStation Manager, kliknij przycisk "Zastosuj".

## Bibliografia
* [Synology](https://en.wikipedia.org/wiki/Synology)
