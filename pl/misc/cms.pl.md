{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku CMS - Plik profilu usługi Menedżera połączeń",
  "description":"Poznaj plik CMS i interfejsy API, które mogą tworzyć i otwierać pliki CMS.",
  "linktitle" : "CMS",
  "menu" : {
    "docs" : {
      "identifier": "misc-cms",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Czym jest plik CMS?

Plik CMS to plik danych zawierający informacje o profilu używane przez Menedżera połączeń systemu Microsoft Windows. Pozwala zdalnym użytkownikom łączyć się z siecią przy użyciu tych informacji profilowych. Informacje przechowywane w pliku CMS obejmują dane o systemie operacyjnym użytkownika i uprawnieniach, które są używane do ustanowienia połączenia między zdalnym użytkownikiem a siecią. Administratorzy CMS używają zestawu administratora Menedżera połączeń (CMAK) do generowania plików CMS.

## Format pliku CMS — więcej informacji

Pliki CMS nie są często spotykane na komputerach użytkowników. Ponieważ są one używane specjalnie w celu umożliwienia zdalnym użytkownikom dostępu do sieci, znajdziesz je na komputerach używanych do łączenia się z siecią firmową lub biurem o określonym celu. W większości przypadków służy do łączenia się z siecią organizacyjną, taką jak wirtualna sieć prywatna (VPN), która jest przeznaczona wyłącznie dla firmy. Będąc administratorem sieci, skonfigurujesz dostęp do takiej sieci za pomocą Menedżera połączeń, aby umożliwić mu dostęp do sieci firmowej ze zdalnej lokalizacji.

### Co to jest niezależny CMS?

Plik profilu CMS jest tworzony za pomocą Menedżera połączeń i jest pakowany z innymi plikami konfiguracyjnymi przed udostępnieniem użytkownikowi zdalnemu. Te dodatkowe pliki mogą zawierać plik CMP i plik INF, które są spakowane razem w pliku [EXE](/pl/plik wykonywalny/exe/). Ten kompletny pakiet jest dostarczany użytkownikowi zdalnemu w celu połączenia z siecią.

## Bibliografia

* [Zrozumienie i konfiguracja Menedżera połączeń systemu Windows](https://learn.microsoft.com/en-us/windows-hardware/drivers/mobilebroadband/understanding-and-configuring-windows-connection-manager)

