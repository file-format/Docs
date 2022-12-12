{
  "date" : "2021-08-13",
  "keywords" :[ "plik sdi", "format pliku sdi", "co to jest plik sdi", "plik", "przykład sdi", "rozszerzenie pliku sdi", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Poznaj format plików SDI i interfejsy API, które mogą tworzyć i otwierać pliki SDI.",
  "title" :"SDI — plik obrazu wdrażania systemu Windows",
  "linktitle" : "SDI",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-13"
}

## Czym jest plik SDI?
Plik z rozszerzeniem .sdi zawiera obiekt blob ładowania, obiekt blob rozruchowy i obiekt blob części; powszechnie używany przez Windows Embedded Studio do tworzenia dysków RAM lub dysków rozruchowych do ładowania i instalowania systemu Windows. SDI jest skrótem od obrazu wdrażania systemu. Windows Embedded Studio to program służący do tworzenia obrazów dysków dla systemu Windows. Właściwie ten program zawiera program SDI File Manager i narzędzie wiersza poleceń o nazwie **sdimgr.exe**, oba mogą być używane do wdrażania, tworzenia i edytowania obrazów SDI.

## Format pliku SDI
Format pliku SDI jest szeroko stosowany, aby umożliwić użycie dysku wirtualnego do uruchamiania systemu. Niektóre wersje systemu Microsoft Windows umożliwiają **uruchamianie z pamięci RAM**, co jest ważne przy ładowaniu pliku SDI do pamięci, a następnie uruchamianiu z niego. Format pliku SDI umożliwia również uruchamianie sieciowe przy użyciu środowiska PXE (Preboot Execution Environment). Jest również używany do obrazowania dysku twardego.
### Sekcje pliku SDI
Sam plik SDI można podzielić na następujące sekcje:
- **Boot BLOB**: Zawiera aktualny program startowy, STARTROM.COM. Jest to analogiczne do sektora rozruchowego dysku twardego.
- **Załaduj obiekt BLOB**: zwykle zawiera NTLDR i jest uruchamiany przez rozruchowy obiekt BLOB.
- **Część BLOB**: zawiera rzeczywiste środowisko wykonawcze rozruchu; zawiera również pliki boot.ini i ntdetect.com, które powinny znajdować się w katalogu głównym środowiska wykonawczego.
- **Disk BLOB**: To jest płaski obraz dysku twardego zaczynający się od MBR. Służy do obrazowania dysku twardego zamiast uruchamiania. Ponadto za pomocą narzędzi firmy Microsoft można montować tylko dyskowe obiekty BLOB.


## Bibliografia

* [Obraz wdrażania systemu — według Wikipedii](https://en.wikipedia.org/wiki/System_Deployment_Image)


