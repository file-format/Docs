{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Plik ADMX - Format pliku szablonu administracyjnego zasad grupy",
  "description":"Dowiedz się o formacie pliku ADMX i o tym, jak otwierać pliki ADMX.",
  "linktitle" : "ADMX",
  "menu" : {
    "docs" : {
      "identifier" : "system-admx",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## Czym jest plik ADMX?

Plik ADMX to plik konfiguracyjny zasad używany przez oprogramowanie zasad grupy Microsoft Windows, które zarządza grupą komputerów w grupie. Jest to plik szablonu administracyjnego oparty na formacie XML i został wprowadzony w dodatku Service Pack 1 dla systemu Windows Vista. Pliki ADMX zawierają ustawienia konfiguracyjne dla kont użytkowników, konfiguracji systemu operacyjnego i aplikacji. Pliki ADMX służą do przechowywania i wdrażania konfiguracji do scentralizowanego zarządzania wieloma systemami komputerowymi.

Możesz tworzyć lub edytować pliki ADMX za pomocą dowolnego edytora tekstu zgodnego z XML, dowolnego edytora tekstu lub edytora obiektów zasad grupy Microsoft.

## Format pliku ADMX — więcej informacji

Pliki ADMX są przechowywane w uniwersalnym formacie pliku [XML](/pl/web/xml/), który jest czytelny dla człowieka. Jest to wielojęzyczny format pliku i umożliwia administratorom systemu z różnych języków pracę z tymi samymi plikami ADMX. Pliki ADMX zastąpiły stary format pliku [ADM](/pl/system/adm/), który jest formatem pliku tekstowego w formacie Unicode. Pliki ADMX określają klucze rejestru, które ulegają zmianie po zmianie określonego ustawienia zasad grupy.

### Co mogę zrobić z plikiem ADMX?

Pliki ADMX definiują, jakie akcje mają być dozwolone komputerom użytkowników będącym częścią grupy. Polityka grupowa narzuca reguły ustawione w połączeniu z oprogramowaniem Active Directory. Pliki ADMX są zarządzane z centralnego magazynu w systemie operacyjnym Windows, który jest centralną lokalizacją w domenie.

Plik ADMX wdrożony w środowisku roboczym może pozwolić administratorom wdrożyć takie zasady, jak:

* Kontroluj korzystanie z Internetu
* Pobieranie niektórych typów plików
* Korzystanie z urządzeń wymiennych w systemach

## Bibliografia

* [Pliki szablonów administracyjnych — ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ – zarządzanie plikami szablonów administracyjnych](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)

