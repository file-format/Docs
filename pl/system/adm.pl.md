{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Plik ADM - Format pliku szablonu administracyjnego",
  "description":"Dowiedz się o formacie pliku ADM i sposobie otwierania plików ADM.",
  "linktitle" : "ADM",
  "menu" : {
    "docs" : {
      "identifier" : "system-adm",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## Czym jest plik ADM?

Plik ADM to plik szablonu używany przez oprogramowanie zasad grupy firmy Microsoft do określenia lokalizacji ustawień zasad opartych na rejestrze w pliku rejestru. Jest używany przez administratorów systemu do definiowania polityki zarządzania grupą komputerów będących częścią grupy. Informacje te stają się częścią obiektów zasad grupy (GPO), które są tworzone w celu zarządzania grupą.

Możesz otwierać pliki ADM za pomocą Edytora obiektów zasad grupy Microsoft.

## Format pliku ADM — więcej informacji

Pliki ADM są przechowywane jako pliki tekstowe w formacie Unicode. Były one używane głównie do opisu lokalizacji ustawień zasad opartych na rejestrze w rejestrze systemów Windows Vista i Windows 7.

Pliki ADM nie są już obsługiwane i zostały zastąpione plikami [ADMX](/pl/system/admx/). GPA ignoruje następujące domyślne pliki ADM na komputerach z systemem Microsoft Windows Vista z dodatkiem Service Pack 1 lub nowszym.

* system.adm
* inetres.adm
* konf.adm
* wmplayer.adm
* wuau.adm

## Bibliografia

* [Pliki szablonów administracyjnych — ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ – zarządzanie plikami szablonów administracyjnych](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)

